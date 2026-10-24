# Template — sprite do Novo Testamento

- **Template ID:** `TPL-HNT-SPRITE`
- **Versão:** 1.0.0
- **Coleção:** Novo Testamento
- **Ativo:** sprite ou elemento visual isolado
- **Estado:** INICIAL — especificação técnica precisa ser confirmada por tipo de uso

## Entrada

Título/nome do elemento; história de origem (ID/título); uso pretendido (por exemplo, personagem, objeto ou elemento de cenário); dimensões, proporção, fundo/transparência e requisitos de animação, se houver.

Se algum requisito técnico mudar a geração (ex.: sprite sheet versus sprite individual, transparência, número de frames, perspectiva ou escala), pergunte antes de gerar em vez de assumir.

## Fontes e contexto

Consulte a narrativa correspondente em [historia-novo-testamento.md](../../historia-novo-testamento.md) e as regras globais. A narrativa define o que o elemento representa; ela não define automaticamente dimensões técnicas. Não invente detalhes biográficos ou visuais como fatos bíblicos.

## Roteiro

1. Identificar elemento e história de origem.
2. Definir se a saída é um sprite individual ou um sprite sheet; obter confirmação se isso não estiver explícito.
3. Bloquear silhueta, pose, perspectiva, paleta, escala e atributos estáveis relevantes para continuidade.
4. Usar `higgsfield-generate` como skill principal de geração, se operacional; consultar as instruções atuais e registrar evidência.
5. Fazer uma única chamada para a saída aprovada. Quantidade 1 quando suportada. Não criar coleções/variações automaticamente.
6. Validar recorte, bordas, silhueta, anatomia, consistência, fundo/transparência e dimensões requeridas, de acordo com os requisitos confirmados.

## Proibições

Não assumir transparência, tamanho, pivot, número de frames ou direção de animação sem informação. Não confundir imagem ilustrativa com sprite pronto para engine. Não afirmar fundo transparente ou conformidade técnica sem inspecionar o arquivo.

## Relatório

Template ID/versão; elemento; história de origem; requisitos técnicos confirmados; ferramenta/skill realmente usada; dimensões reais; transparência observada; validação; caminho do ativo e pendências.
