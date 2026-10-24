# Estudo Bíblico — leia primeiro

**Repositório canônico:** `milson-rodrigues/geracao-de-historia`, branch `main`.

## Ordem de leitura

1. [`ROUTER-MESTRE.md`](../ROUTER-MESTRE.md) — ponto de entrada estável.
2. [`README.md`](../README.md) — visão geral.
3. [`templates/CATALOGO.md`](../templates/CATALOGO.md) — confirmar que o Template ID existe.
4. Abrir o arquivo exato do template.
5. Consultar a fonte narrativa correspondente: `historias/historias-<nome-historia>.md`.
6. Consultar o manifesto pareado quando o fluxo exigir status: `historias/status-criacao-historia.<nome-historia>.md`.
7. Ler [rota geral](ROTA-GERAL.md), [skills](SKILLS-E-RECURSOS.md), [padrão visual](PADRAO-VISUAL-E-COMPOSICAO.md) e [validação final](VALIDACAO-FINAL.md).
8. Consultar as versões atuais das skills e ferramentas externas indicadas no template, quando acessíveis.

## Convenção de fontes

O segmento `<nome-historia>` deve ser o mesmo no arquivo narrativo e no manifesto de status. Descubra os arquivos reais pela árvore atual do GitHub; não monte caminhos apenas por convenção nem use caminhos antigos memorizados.

## Integridade

- Escreva e revise todo texto editorial em português brasileiro.
- Preserve acentuação, pontuação e concordância. Não considerar texto de imagem válido sem inspeção legível.
- Não invente arquivos, IDs, fontes, imagens de referência, resultados ou estados.
- Se uma dependência estiver ausente, pare e informe o bloqueio.
- A existência de uma skill no GitHub não prova que o CLI, integração ou credenciais estejam operacionais.
- Não mover nem apagar fontes canônicas sem migração planejada e verificada.

## Regra de persistência obrigatória

ChatGPT, agente ou pessoa com acesso autorizado ao GitHub deve manter o par narrativo/status sincronizado ao criar ou modificar uma história: `historias/historias-<nome-historia>.md` e `historias/status-criacao-historia.<nome-historia>.md`. Aplicar o protocolo de escrita e verificação de [Rota Geral](ROTA-GERAL.md). Sem acesso de escrita, não alegar que o repositório foi atualizado.


## Padrão de proporção e qualidade

Por padrão, toda imagem deve ser horizontal 16:9 e ter no mínimo 1920 × 1080 pixels (Full HD); quando a ferramenta suportar qualidade/resolução nativa maior, preferi-la. Só produzir em 9:16 vertical (mínimo 1080 × 1920) quando o usuário pedir explicitamente. Os modelos ficam juntos em `mockups/`: `mockup-template-universal.svg` (padrão 16:9) e `mockup-template-universal-9x16.svg` (variante 9:16). Verificar o caminho correto e as dimensões reais antes de declarar conclusão. Não alterar `ROUTER-MESTRE.md` para esta regra operacional.
