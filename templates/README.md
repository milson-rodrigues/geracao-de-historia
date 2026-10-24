# Templates de produção

Os templates são os pontos de entrada para cada tipo de produção visual. Cada template define coleção/testamento, objetivo narrativo, fonte de contexto, tipo de ativo, roteiro, regras visuais e validação específica.

## Convenção de ID

Use um identificador estável, legível e único:

- `TPL-HNT-HISTORIA` — história ilustrada do Novo Testamento.
- `TPL-HAT-HISTORIA` — história ilustrada do Antigo Testamento.
- `TPL-HNT-SPRITE` — sprite derivado de conteúdo do Novo Testamento.
- `TPL-HAT-SPRITE` — sprite derivado de conteúdo do Antigo Testamento.

Esses IDs são a proposta de catálogo inicial. Para adicionar um template, criar seu arquivo e registrar no [catálogo](CATALOGO.md). Não reutilizar ID para um objetivo diferente.

## Como executar

O usuário informa o ID do template e o título/conteúdo a produzir, por exemplo:

```text
Gerar com template TPL-HNT-HISTORIA
Título: O anjo Gabriel aparece a Maria
```

O template encaminha o agente à fonte narrativa da coleção e às regras globais/locais. O título é um identificador de trabalho, não permissão para inventar fatos. Se a narrativa oficial necessária não puder ser identificada sem ambiguidade, parar e pedir o dado mínimo ausente.

## Conteúdo de cada template

Todo template deve declarar: ID/versão, coleção, ativo pretendido, entrada esperada, fontes canônicas, contexto, etapas do roteiro, regras de imagem, requisitos de quantidade, proibições, critérios de validação e formato do relatório final.

## Separação de responsabilidades

- O template da coleção determina narrativa e contexto.
- Regras globais determinam integridade, skills e qualidade básica.
- Regras específicas do ativo definem composição e requisitos técnicos.
- A skill de geração é a execução técnica principal quando realmente acessível.
- A validação decide aprovação; geração sozinha não aprova o resultado.
