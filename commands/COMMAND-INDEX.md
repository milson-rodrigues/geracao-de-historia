# Command Index — AI Creative Hub

**Versão:** 0.1.0  
**Estado:** catálogo documental inicial; comandos ainda não registrados em um runtime de execução.  
**Idioma:** pt-BR  
**Ponto de entrada estável:** [ROUTER-MESTRE.md](../ROUTER-MESTRE.md)

Este índice é a lista canônica dos comandos conversacionais planejados para o AI Creative Hub. Ele descreve a interface pretendida; a existência de uma linha aqui não significa que o comando esteja registrado como slash command nativo em ChatGPT, Claude Code ou outro host.

## Como interpretar os estados

- **Fluxo documental existente:** há documentação operacional correspondente no repositório, mas o alias slash ainda não tem parser/dispatcher próprio.
- **Especificado:** contrato inicial documentado; bridge, provider ou runtime ainda precisam ser implementados/validados.
- **Planejado:** ideia registrada para evolução, sem contrato operacional suficiente.

## Entradas de bridge

Os comandos de bridge selecionam um domínio e mantêm o contexto da conversa. Não geram mídia sozinhos.

| Comando canônico | Alias aceito | Domínio | Responsabilidade | Estado |
|---|---|---|---|---|
| `/image-bridge` | `/criar-imagem-bridge` | Image | Imagem, edição, composição e identidade visual | Especificado |
| `/comic-bridge` | — | Comic | Narrativa visual, storyboard e histórias em quadrinhos | Fluxo documental existente |
| `/video-bridge` | `/criar-video-bridge` | Video | Geração, edição e animação de vídeo | Especificado |
| `/voice-bridge` | `/criar-voz-bridge` | Voice | Fala, narração, TTS, transcrição e dublagem | Especificado |
| `/audio-bridge` | `/criar-audio-bridge` | Audio | Música, efeitos, ambientes, edição e pós-produção sonora | Especificado |
| `/sprite-bridge` | `/criar-sprite-bridge` | Sprite | Sprites, sprite sheets e animação quadro a quadro | Especificado |

## Image Bridge

| Comando | Descrição | Estado |
|---|---|---|
| `/criar-imagem` | Gerar imagem a partir de briefing | Especificado |
| `/editar-imagem` | Editar imagem fornecida ou selecionada | Especificado |
| `/criar-personagem` | Definir personagem e identidade visual | Especificado |
| `/criar-cenario` | Criar cenário/ambiente | Especificado |
| `/criar-concept-art` | Explorar conceito visual | Planejado |
| `/criar-thumbnail` | Criar thumbnail/capa de vídeo | Especificado |
| `/criar-poster` | Criar pôster/cartaz | Planejado |
| `/validar-imagem` | Verificar requisitos visuais e técnicos | Especificado |

## Comic Bridge

| Comando | Descrição | Estado |
|---|---|---|
| `/criar-historia-quadrinho` | Criar HQ a partir de narrativa/roteiro | Fluxo documental existente |
| `/criar-prancha` | Produzir uma página/prancha | Fluxo documental existente |
| `/criar-storyboard` | Planejar quadros e sequência visual | Especificado |
| `/criar-quadro` | Criar painel individual | Especificado |
| `/criar-tirinha` | Criar tirinha curta | Planejado |
| `/criar-webtoon` | Criar HQ vertical | Planejado |
| `/validar-historia-quadrinho` | Validar narrativa, leitura e continuidade | Especificado |

**Regra de compatibilidade:** o fluxo bíblico atual continua vinculado ao `TPL-MOCKUP-UNIVERSAL`, à fonte narrativa canônica e às regras específicas já existentes. Os comandos genéricos de Comic Bridge não removem nem flexibilizam esses requisitos.

## Video Bridge

| Comando | Descrição | Estado |
|---|---|---|
| `/criar-video` | Criar vídeo conforme briefing | Especificado |
| `/criar-video-cinema` | Vídeo com direção cinematográfica | Especificado |
| `/criar-video-desenho` | Vídeo em estilo cartoon/animação | Especificado |
| `/criar-video-anime` | Vídeo em estilo anime | Planejado |
| `/criar-video-realista` | Vídeo fotorrealista | Planejado |
| `/criar-video-publicitario` | Vídeo publicitário/comercial | Especificado |
| `/criar-trailer` | Trailer/teaser | Especificado |
| `/animar-imagem` | Image-to-video | Especificado |
| `/editar-video` | Editar, estender ou reenquadrar vídeo | Especificado |
| `/validar-video` | Validar duração, formato e requisitos | Especificado |

## Voice Bridge

| Comando | Descrição | Estado |
|---|---|---|
| `/gerar-narracao` | Gerar narração falada | Especificado |
| `/gerar-voz` | Síntese de fala/TTS | Especificado |
| `/criar-identidade-vocal` | Definir perfil e direção vocal | Planejado |
| `/dublar-video` | Dublagem e sincronização | Especificado |
| `/clonar-voz` | Clonagem somente com autorização verificável | Planejado |
| `/transcrever-audio` | Speech-to-text | Especificado |
| `/traduzir-audio` | Tradução de fala preservando segmentação | Planejado |
| `/validar-voz` | Validar inteligibilidade, pronúncia e sincronismo | Especificado |

Voice é dedicado à fala e à identidade vocal. Música, efeitos e ambientes pertencem à Audio Bridge.

## Audio Bridge

| Comando | Descrição | Estado |
|---|---|---|
| `/criar-musica` | Gerar música | Especificado |
| `/criar-trilha-sonora` | Compor trilha para cena, HQ ou vídeo | Especificado |
| `/criar-efeitos-sonoros` | Criar efeitos pontuais/Foley | Especificado |
| `/criar-ambiente-sonoro` | Criar paisagem sonora/ambiente | Especificado |
| `/criar-sound-design` | Projetar identidade e narrativa sonora | Especificado |
| `/editar-audio` | Cortar, limpar ou transformar áudio | Planejado |
| `/mixar-audio` | Mixar voz, música e efeitos | Especificado |
| `/masterizar-audio` | Finalizar loudness e entrega | Especificado |
| `/validar-audio` | Validar formato, clipping, loudness e inteligibilidade | Especificado |

## Sprite Bridge

| Comando | Descrição | Estado |
|---|---|---|
| `/criar-sprite` | Criar sprite individual | Especificado |
| `/criar-sprite-sheet` | Criar folha de sprites | Especificado |
| `/animar-sprite` | Criar sequência de frames | Especificado |
| `/criar-personagem-game` | Criar personagem para jogo | Planejado |
| `/criar-animacao-2d` | Criar animação 2D | Planejado |
| `/validar-sprite` | Validar recorte, dimensões, alpha e frames | Especificado |

## Comandos transversais

| Comando | Descrição | Estado |
|---|---|---|
| `/validar-ativo` | Aplicar QA conforme tipo de mídia | Especificado |
| `/exportar-ativo` | Preparar formato de entrega | Planejado |
| `/consultar-provedores` | Listar providers compatíveis e disponibilidade conhecida | Planejado |
| `/status-criacao` | Consultar estado documentado de um trabalho | Planejado |

## Regras de governança

1. Um comando tem um identificador canônico, uma bridge proprietária e um contrato documentado.
2. Aliases apontam para o comando canônico; não duplicam workflows.
3. Comandos não escolhem diretamente um modelo/provedor sem consultar capacidade, disponibilidade, restrições e custo.
4. A ausência de provider compatível deve resultar em bloqueio explícito, não em substituição silenciosa.
5. A execução só pode ser marcada como concluída após evidência do provider e validação do ativo.
6. Alterações de comandos devem atualizar este índice, o manual e os contratos afetados.
7. Não declarar comando como executável até existir dispatcher/runtime e teste de integração.
