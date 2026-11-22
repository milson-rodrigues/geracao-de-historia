# Skill Registry — fontes locais e externas

**Versão:** 0.1.0  
**Estado:** inventário documental inicial, baseado na árvore da branch `main`.  
**Regra:** este registro não prova que uma CLI, conta, API ou provider esteja operacional.

## 1. Política de incorporação

Usar três modalidades:

- **INTERNAL:** skill escrita e mantida pelo projeto; código e documentação sob controle do repositório.
- **ADAPTED:** conhecimento/fluxo externo revisado e reescrito para os contratos e políticas do projeto, com atribuição e licença verificadas.
- **REFERENCE:** skill permanece na fonte original; o projeto mantém link, versão verificada e instruções de carregamento sob demanda.

Não copiar integralmente skills externas por padrão. Antes de qualquer cópia, verificar licença, copyright, dependências, comandos, permissões, telemetria, segredos e compatibilidade com o runtime.

## 2. Skills locais detectadas em `.agents/skills/`

A árvore da branch `main` contém as seguintes pastas:

| Skill local | Uso indicado pelo nome/documentação | Diretriz |
|---|---|---|
| `higgsfield-generate` | Geração multimodal por Higgsfield CLI | Manter como skill externa espelhada/local; revalidar upstream e CLI antes de uso |
| `higgsfield-brandkit` | Sistemas de identidade visual e brandbooks | Manter; acionar somente em tarefas de identidade de marca |
| `higgsfield-marketplace-cards` | Cards/listagens de marketplace | Manter como especialidade específica |
| `higgsfield-product-photoshoot` | Fotografia de produto | Manter como especialidade específica |
| `higgsfield-soul-id` | Identidade/consistência de personagem | Manter; verificar limites e consentimento para pessoas reais |
| `higgsfield-video-explainer` | Vídeos explicativos | Manter; classificar como workflow especializado de vídeo |
| `higgsfield-websites` | Sites e experiências web; inclui materiais de game/3D conforme módulos | Não tratar como provider genérico de sprite; inspecionar o módulo exato antes de encaminhar |
| `higgsfield-youtube-thumbnail` | Thumbnails/capas de vídeo | Manter; especialidade de Image/Video |

Esses arquivos locais são cópias versionadas no repositório e podem divergir do upstream. Não presumir que sejam a versão mais recente.

## 3. Fonte externa principal atualmente referenciada

| Fonte | URL | Modalidade | Observação |
|---|---|---|---|
| Higgsfield Skills | https://github.com/higgsfield-ai/skills | REFERENCE / cópia local existente | Consultar o arquivo oficial específico e a versão atual quando a tarefa exigir Higgsfield |
| GPT Image 2 Prompt Library | https://github.com/freestylefly/awesome-gpt-image-2 | REFERENCE | Curadoria complementar; verificar licença e conteúdo antes de adaptar |
| Taste Skill | https://github.com/Leonxlnx/taste-skill | REFERENCE | Direção artística complementar |
| Open Design | https://github.com/nexu-io/open-design | REFERENCE | Exploração visual opcional |

A política operacional atual do fluxo bíblico de HQ deve ser lida em `00_GUIA-DE-CONFIGURACAO.md` e `regras/SKILLS-E-RECURSOS.md`. Este registro não altera a ferramenta principal já definida para esse fluxo.

## 4. Cobertura por domínio

| Domínio | Skills internas necessárias (propostas) | Skills externas a avaliar |
|---|---|---|
| Image | prompt composition, image QA, visual consistency | Higgsfield Generate, Brandkit, Product Photoshoot, GPT Image style library |
| Comic | narrative fidelity, panel composition, continuity QA | Toonflow e ferramentas de storyboard; avaliar licenças antes de adoção |
| Video | cinematic direction, shot planning, video QA | Higgsfield Generate, Video Explainer, outros provedores a auditar |
| Voice | TTS direction, pronunciation QA, dubbing QA, consent gate | Provedores TTS/dubbing a pesquisar; ainda não homologados |
| Audio | music direction, SFX design, ambience, mixing/mastering QA | Higgsfield Generate e provedores especializados; validar capacidades e licenças |
| Sprite | sprite specification, alpha/frame QA, sheet layout | Ferramentas de sprite/game asset a auditar |

A lista de skills internas é backlog arquitetural, não declaração de que esses módulos já foram implementados.

## 5. Registro obrigatório para cada nova skill

Manter estes campos em uma entrada de registry:
- nome e identificador;
- domínio/bridge;
- tipo (INTERNAL, ADAPTED ou REFERENCE);
- repositório e URL de origem;
- versão/tag/commit verificado;
- licença e atribuição;
- data da última verificação;
- dependências e permissões exigidas;
- capacidades e limitações;
- runtime compatível;
- comandos/workflows consumidores;
- testes de compatibilidade;
- estado: candidate, reviewed, approved, deprecated.

## 6. Gate de adoção

Uma skill externa só pode ser copiada/adaptada após:
1. leitura integral do material relevante;
2. identificação de licença e condições de redistribuição;
3. inspeção de scripts, dependências e chamadas externas;
4. análise de segredos, telemetria e permissões;
5. definição do que será reutilizado e do que será reescrito;
6. registro de proveniência;
7. testes em ambiente controlado.

Se a licença não estiver clara ou não permitir redistribuição, manter apenas referência e criar implementação independente baseada em requisitos observáveis, sem copiar expressão protegida.
