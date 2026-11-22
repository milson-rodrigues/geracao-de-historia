# Command Manual — AI Creative Hub

**Versão:** 0.1.0  
**Estado:** especificação de uso; não é um parser nem registra slash commands no host.  
**Índice oficial:** [COMMAND-INDEX.md](COMMAND-INDEX.md)  
**Contrato de roteamento:** [COMMAND-CONTRACT.md](COMMAND-CONTRACT.md)

## 1. Sintaxe geral

A forma recomendada é:

```text
/<comando> [briefing e parâmetros em linguagem natural]
```

Exemplo:

```text
/criar-video-cinema
Tema: A travessia do Mar Vermelho
Duração desejada: 30 segundos
Formato: 16:9
Estética: épica, cinematográfica
Narração: português brasileiro
Trilha: orquestral
```

O usuário não precisa preencher todos os parâmetros. O roteador deve recuperar o que já foi informado na conversa e perguntar somente por lacunas que alterem materialmente o resultado.

## 2. Seleção de bridge versus comando de produção

- Use `/<dominio>-bridge` quando quiser estabelecer o domínio de trabalho ou explorar suas capacidades.
- Use `/criar-...`, `/editar-...`, `/animar-...` ou `/validar-...` para solicitar uma operação concreta.
- Um comando de produção pode acionar a bridge diretamente, sem exigir que o usuário selecione a bridge antes.

Exemplos:

```text
/image-bridge
Quais operações de imagem estão disponíveis?

/comic-bridge
/criar-historia-quadrinho
Título: O anjo Gabriel aparece a Maria
Fonte: coleção Novo Testamento

/video-bridge
/criar-video-cinema
Tema: Uma cidade bíblica ao amanhecer
Duração: 12 segundos

/audio-bridge
/criar-trilha-sonora
Cena: chegada de uma caravana ao deserto
Duração: 40 segundos
```

## 3. Campos comuns de briefing

Os campos abaixo são convenções de linguagem natural. Um futuro runtime deverá normalizá-los para o schema definido em `schemas/command-request.schema.json`.

| Campo | Uso |
|---|---|
| `objetivo` | O que precisa ser produzido |
| `briefing` | Descrição narrativa/funcional |
| `referencias` | Arquivos, URLs ou IDs fornecidos pelo usuário |
| `estilo` | Direção estética |
| `formato` | Aspect ratio, codec ou tipo de arquivo |
| `duracao` | Duração desejada, quando aplicável |
| `resolucao` | Resolução pretendida |
| `idioma` | Idioma de texto/fala |
| `voz` | Características vocais, quando aplicável |
| `audio` | Música, efeitos, ambiente e mixagem |
| `destino` | Destino de entrega, quando definido |
| `restricoes` | Limites e elementos proibidos |

## 4. Requisitos por bridge

### Image

Entradas típicas: objetivo, assunto, referência visual, estilo, composição, proporção, resolução e texto exato a renderizar.

O fluxo deve distinguir geração, edição, composição, identidade de personagem e imagem com texto. Não presumir que um modelo seja bom em todas essas operações.

### Comic

Entradas típicas: fonte narrativa/roteiro, título, personagens, sequência, quantidade de páginas/pranchas, idioma, estilo e proporção.

Para histórias bíblicas do fluxo existente:
- consultar primeiro o roteador e o guia operacional atuais;
- confirmar Template ID no catálogo;
- ler a narrativa canônica e o manifesto aplicável;
- seguir integralmente o `TPL-MOCKUP-UNIVERSAL` e suas regras;
- manter uma geração final por solicitação, quando a ferramenta suportar;
- não substituir a fonte narrativa por conhecimento geral.

Os comandos genéricos de Comic Bridge não revogam esse procedimento especializado.

### Video

Entradas típicas: conceito, roteiro, duração, proporção, resolução, estilo, movimento de câmera, cenas/shots, continuidade, áudio e referências.

O roteador deve classificar o trabalho como text-to-video, image-to-video, video-to-video, extensão, edição ou montagem. Deve validar limites do modelo/provedor antes da submissão.

### Voice

Entradas típicas: texto, idioma, pronúncia, perfil vocal, emoção, ritmo, pausas, formato e sincronização.

Clonagem de voz exige autorização adequada da pessoa cuja voz será reproduzida. Não presumir consentimento a partir do envio de um arquivo de áudio.

### Audio

Entradas típicas: finalidade, gênero/referência musical, duração, BPM quando relevante, instrumentos, clima, estrutura, stems, efeitos, ambiente, formato e loudness alvo.

Separar música, efeitos pontuais, Foley, ambiente, edição, mixagem e masterização. Não tratar geração de música como sinônimo de TTS.

### Sprite

Entradas típicas: sprite individual ou sheet, dimensões, escala, transparência, orientação, quantidade de frames, ações, FPS, engine/destino e convenção de atlas.

Se uma dimensão essencial não estiver definida, perguntar antes da geração. Não inventar dimensões, transparência ou compatibilidade com engine.

## 5. Perguntas e defaults

1. Reutilizar dados já informados na conversa.
2. Aplicar defaults documentados e identificá-los no resumo do trabalho.
3. Perguntar apenas quando a resposta alterar substancialmente a saída ou evitar falha técnica.
4. Não abrir questionário extenso quando uma pergunta direta for suficiente.
5. Não iniciar geração final enquanto faltar requisito obrigatório do template ou do provider.

## 6. Saída padrão

Ao concluir uma operação, retornar:
- comando e bridge acionados;
- resumo dos parâmetros efetivamente usados;
- skill(s) carregadas e suas versões/fontes, quando aplicável;
- provider/modelo realmente utilizado;
- quantidade de ativos solicitada e gerada;
- validações executadas e resultados;
- links/caminhos reais dos ativos;
- limitações, pendências e estado de aprovação.

Não afirmar geração, exportação, salvamento ou aprovação sem evidência.

## 7. Erros e estados

| Estado | Significado |
|---|---|
| `RECEIVED` | Solicitação recebida |
| `ROUTED` | Bridge/workflow selecionado |
| `NEEDS_INPUT` | Falta informação bloqueante |
| `BLOCKED` | Ferramenta, permissão ou requisito indisponível |
| `RUNNING` | Execução confirmada em andamento |
| `GENERATED` | Provider retornou ativo |
| `VALIDATING` | QA em execução |
| `PASS` | Critérios aplicáveis atendidos |
| `FIX_REQUIRED` | Correções necessárias |
| `FAILED` | Execução falhou |
| `APPROVED` | Aprovação explícita quando exigida |

O estado `GENERATED` não implica `PASS`; `PASS` não implica aprovação humana quando esta for exigida.

## 8. Limite de implementação

Este manual define uma interface conversacional. Para que os comandos sejam realmente executáveis como slash commands, será necessário implementar e testar um dispatcher no host escolhido (por exemplo, agente CLI, harness ou aplicação). Documentação no GitHub, isoladamente, não registra comandos em plataformas externas.
