# Catálogo de templates

O catálogo lista os templates disponíveis na branch `main`. Confirme que o arquivo existe antes de usar um ID.

| Template ID | Escopo | Ativo | Arquivo | Estado |
|---|---|---|---|---|
| `TPL-MOCKUP-UNIVERSAL` | Qualquer história/coleção com fonte canônica | Mockup visual universal | [mockup-template.md](mockup-template.md) | DIREÇÃO VISUAL APROVADA; SVG 16:9 E 9:16 DISPONÍVEIS |

## Contrato universal das fontes

Cada história/coleção identificada usa o par:

- Narrativa: `historias/historias-<nome-historia>.md`
- Status: `historias/status-criacao-historia.<nome-historia>.md`

O identificador deve ser igual nos dois arquivos, estável, minúsculo e sem espaços, preferencialmente separado por hífens. Exemplos existentes hoje: `novo-testamento` e `antigo-testamento`. Para novas coleções, verifique os nomes reais na árvore do GitHub e mantenha o par consistente.

Direção visual aprovada pelo usuário: padrão horizontal 16:9 (1920 × 1080 mínimo) e variante vertical 9:16 (1080 × 1920 mínimo, somente quando solicitada). Ambos os SVGs ficam juntos em `mockups/`. O catálogo não substitui a fonte narrativa nem o manifesto. Não declare que uma história foi gerada/aprovada com base apenas no mockup de validação visual.
