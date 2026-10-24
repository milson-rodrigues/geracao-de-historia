# Templates de produção

O catálogo oficial é [`CATALOGO.md`](CATALOGO.md). Use somente IDs cujo arquivo realmente exista na branch `main`.

## Template disponível

- `TPL-MOCKUP-UNIVERSAL` — imagem-mockup de história independente da coleção. Arquivo: [`mockup-template.md`](mockup-template.md).

## Convenção universal

Cada coleção/história deve ter dois arquivos com o mesmo identificador `<nome-historia>`:

- Fonte narrativa: `historias/historias-<nome-historia>.md`
- Manifesto de produção: `historias/status-criacao-historia.<nome-historia>.md`

O identificador deve ser estável, minúsculo, sem espaços, preferencialmente com hífens. Essa é uma convenção de nomes, não evidência de que o arquivo existe. Sempre consulte a árvore do repositório atual, os links do roteador e o conteúdo dos arquivos.

## Como criar uma nova coleção

1. Criar a fonte narrativa em `historias/historias-<nome-historia>.md`.
2. Criar o manifesto correspondente em `historias/status-criacao-historia.<nome-historia>.md`.
3. Confirmar que o identificador é idêntico nos dois caminhos.
4. Atualizar índice/catalogação se aplicável e testar os links.
5. Não copiar estados de outra coleção sem conferir cada registro.

## Convenção para novos templates

Todo template declara ID/versão, escopo, entrada, fontes, execução, requisitos visuais/técnicos, quantidade, validação e relatório final. Após criar o arquivo, registrar no catálogo e validar todos os destinos.

## Idioma

Todo texto narrativo, balão, legenda, título, instrução visual e relatório destinado ao usuário final deve usar **português brasileiro**, salvo quando o usuário pedir outro idioma. Revisar ortografia, acentos, pontuação, concordância e consistência terminológica.
