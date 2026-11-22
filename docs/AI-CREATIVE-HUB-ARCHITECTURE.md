# AI Creative Hub — arquitetura-alvo

**Versão:** 0.1.0  
**Estado:** arquitetura documental proposta; não representa runtime implementado.  
**Repositório:** `milson-rodrigues/geracao-de-historia`, branch `main`.

## 1. Visão

Evoluir o repositório de uma coleção de fluxos de histórias em quadrinhos/imagens e sprites para um hub multimodal que orquestra criação de imagem, quadrinhos, vídeo, voz, áudio e sprites por meio de comandos consistentes, bridges especializadas, skills versionadas e adapters de provedores.

O nome **AI Creative Hub** é o nome de trabalho da arquitetura. O nome do repositório GitHub permanece inalterado nesta etapa.

## 2. Princípios

1. Command não é Bridge; Bridge não é Skill; Skill não é Provider.
2. O usuário solicita uma intenção; o orquestrador escolhe workflow e capacidades.
3. Providers são substituíveis por adapters; evitar acoplamento do comando a um fornecedor.
4. Skills próprias guardam políticas, critérios e conhecimento específico do projeto.
5. Skills de terceiros são referenciadas ou adaptadas após auditoria de licença e segurança.
6. A fonte narrativa canônica prevalece sobre prompts e skills.
7. Uma geração não equivale a validação ou aprovação.
8. Toda execução deve ser rastreável.
9. A arquitetura deve suportar execução por agentes/CLI e futura interface visual sem depender de uma única plataforma.

## 3. Domínios/bridges

| Bridge | Responsabilidade | Fronteira |
|---|---|---|
| Image | Imagens estáticas, edição, composição, identidade visual | Não é responsável por sequenciar páginas completas de HQ |
| Comic | Narrativa visual, roteiro, storyboard, painéis, páginas e continuidade | Pode consumir imagens e personagens; mantém regras narrativas próprias |
| Video | Geração, edição, animação, shots e montagem | Pode consumir imagens, storyboard, áudio e voz |
| Voice | Fala, TTS, voz, transcrição, tradução e dublagem | Não é responsável por trilha musical ou efeitos não verbais |
| Audio | Música, trilha, SFX, Foley, ambiente, edição, mixagem e masterização | Não é responsável por síntese de fala |
| Sprite | Sprites individuais, sheets, frames, animação e validação técnica | Exige contrato explícito de dimensões, alpha, frames e destino |

## 4. Camadas

- **Command Interface:** nomes canônicos, aliases e contratos de entrada.
- **Command Router:** reconhecimento e normalização.
- **Creative Orchestrator:** plano de execução e dependências.
- **Bridge Layer:** regras e contratos por modalidade.
- **Workflow Layer:** sequência de etapas reutilizáveis.
- **Skill Registry/Resolver:** descoberta, versão, procedência e carregamento sob demanda.
- **Capability Registry:** capacidades de providers, formatos e limites.
- **Provider Adapters:** integração concreta com APIs/CLIs.
- **Quality Assurance:** validação por modalidade.
- **Asset & Provenance Registry:** metadados, resultados, versões e evidências.

## 5. Estrutura documental e futura estrutura de implementação

A adaptação inicial organiza documentos sem fingir que diretórios vazios são módulos executáveis. Estrutura-alvo:

```text
.
├── ROUTER-MESTRE.md
├── 00_GUIA-DE-CONFIGURACAO.md
├── README.md
├── commands/
│   ├── COMMAND-INDEX.md
│   ├── COMMAND-MANUAL.md
│   └── COMMAND-CONTRACT.md
├── core/                         # runtime futuro
│   ├── command-router/
│   ├── creative-orchestrator/
│   ├── skill-registry/
│   ├── capability-registry/
│   └── workflow-engine/
├── bridges/                      # contratos por domínio
│   ├── image/
│   ├── comic/
│   ├── video/
│   ├── voice/
│   ├── audio/
│   └── sprite/
├── workflows/
├── skills/                       # skills próprias/adaptadas
│   ├── image/
│   ├── comic/
│   ├── video/
│   ├── voice/
│   ├── audio/
│   ├── sprite/
│   └── quality-assurance/
├── .agents/skills/               # skills locais existentes/espelhadas
├── providers/                    # adapters futuros
├── external/
│   └── SKILL-REGISTRY.md
├── schemas/
├── templates/
├── historias/
├── regras/
└── docs/
```

A estrutura de implementação só deve ser criada quando houver código, contratos ou arquivos necessários. Não criar diretórios vazios apenas para aparentar que os módulos existem.

## 6. Compatibilidade com o fluxo bíblico atual

O fluxo atual de histórias bíblicas permanece como workflow especializado dentro da Comic Bridge:
- manter `TPL-MOCKUP-UNIVERSAL` e seu catálogo;
- manter fontes narrativas e manifestos por coleção;
- manter regras editoriais, visuais e de validação;
- manter o gate de consulta de fontes e prevenção de duplicidade;
- manter a política específica da ferramenta nativa de imagens definida no guia atual;
- não exigir os providers multimodais do novo hub para executar esse fluxo;
- não permitir que regras genéricas de vídeo/áudio alterem o conteúdo bíblico.

O AI Creative Hub amplia a arquitetura; não apaga o histórico nem altera contratos já aprovados.

## 7. Fronteiras iniciais dos providers

A presença de uma skill local Higgsfield Generate indica documentação para geração multimodal via CLI, mas não comprova autenticação, instalação ou disponibilidade. A skill consultada descreve geração de imagem, vídeo, 3D e áudio, mas declara que não é para TTS.

Portanto:
- Higgsfield pode ser avaliado como adapter de Image, Video e Audio após validação de modelo/schema e autenticação;
- Voice requer pesquisa e homologação de provider TTS/dubbing separado;
- Sprite requer avaliação de capacidades de transparência, dimensões, atlas e frames; não presumir que qualquer gerador de imagem satisfaça esses requisitos;
- Comic pode orquestrar múltiplas capacidades sem ser reduzido a um único provider.

## 8. Fases de evolução

1. **Fundação documental:** índice/manual de comandos, contratos, registry e arquitetura (esta etapa).
2. **Contratos formais:** schemas de comando, skill metadata e capability registry.
3. **Runtime mínimo:** parser/dispatcher, normalizador e roteamento de bridges.
4. **Adapters:** integrar providers um domínio por vez, com testes e gate de autorização.
5. **QA e ativos:** validação automatizável, provenance e versionamento de resultados.
6. **Interface visual:** canvas/board de criação, jobs, assets e continuidade.

## 9. Fora do escopo desta etapa

- Não implementar parser/dispatcher de produção.
- Não instalar CLIs nem configurar credenciais.
- Não fazer chamadas pagas a providers.
- Não copiar novas skills de terceiros.
- Não alterar o nome do repositório, fontes narrativas, templates ou ativos aprovados.
- Não modificar `ROUTER-MESTRE.md`.
