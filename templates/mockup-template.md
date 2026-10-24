# Template para mockup visual — modelo universal

- **Template ID:** `TPL-MOCKUP-UNIVERSAL`
- **Versão:** 1.0.1
- **Estado:** AGUARDANDO APROVAÇÃO VISUAL DO USUÁRIO
- **Finalidade:** produzir uma imagem-mockup para validar a linguagem visual e a composição antes da produção de histórias finais.
- **Escopo:** qualquer coleção que possua uma fonte `historias/historias-<nome-historia>.md`.

## 1. Objetivo

Gerar uma página-mockup visual para o usuário avaliar. A linguagem deve combinar ilustrações sequenciais, **balões de fala** para diálogos e **caixas retangulares** para narração/contexto. O layout deve ser adaptável a histórias diferentes, sem impor uma quantidade fixa de quadros.

O mockup é uma proposta para aprovação visual, não uma história final aprovada. Não altera o status de produção de nenhuma história real.

## 2. Entrada

Definir o tema/título do mockup, e se usará uma história real ou uma demonstração visual genérica. Quando usar uma história real, informe o identificador da coleção ou o caminho da fonte. Método preferido pode ser ChatGPT ou ferramenta externa, conforme disponibilidade real.

Se o tema não for definido, não atribua falas inventadas a figuras bíblicas identificáveis nem apresente elementos sintéticos como fatos canônicos. Identifique claramente a demonstração visual.

## 3. Contrato universal de fontes

Cada coleção/história deve usar o mesmo identificador estável nos dois arquivos:

- Fonte narrativa: `historias/historias-<nome-historia>.md`
- Manifesto de produção: `historias/status-criacao-historia.<nome-historia>.md`

O identificador deve ser igual nos dois caminhos, em minúsculas, sem espaços e preferencialmente separado por hífens.

Exemplos atuais:
- `historias/historias-novo-testamento.md`
- `historias/status-criacao-historia.novo-testamento.md`
- `historias/historias-antigo-testamento.md`
- `historias/status-criacao-historia.antigo-testamento.md`

O padrão de nome não prova que o arquivo existe. O agente deve consultar a árvore atual do GitHub, abrir os arquivos reais e verificar que narrativa e manifesto pertencem à mesma coleção. Não depender de nomes antigos ou de rotas memorizadas.

## 4. Leitura obrigatória antes de gerar

1. Consultar `ROUTER-MESTRE.md` no repositório canônico, na branch `main`.
2. Ler `regras/00-LEIA-PRIMEIRO.md`.
3. Verificar `templates/CATALOGO.md` e confirmar que `TPL-MOCKUP-UNIVERSAL` está disponível.
4. Ler a versão atual deste template.
5. Para uma história real, localizar e ler a fonte `historias/historias-<nome-historia>.md`.
6. Se for tarefa de produção rastreada, ler o manifesto par `historias/status-criacao-historia.<nome-historia>.md`.
7. Ler `regras/ROTA-GERAL.md`, `regras/SKILLS-E-RECURSOS.md`, `regras/PADRAO-VISUAL-E-COMPOSICAO.md` e `regras/VALIDACAO-FINAL.md`.
8. Consultar documentação atual das skills externas no GitHub antes da geração.
9. Usar referências visuais apenas quando realmente acessíveis. Uma imagem anexada ao chat não é automaticamente um arquivo no repositório.

Se qualquer fonte essencial estiver ausente ou inacessível, informar o bloqueio. Não preencher lacunas com memória ou suposições.

## 5. Direção visual universal

- Layout de quadrinhos/graphic novel com sequência legível e quadros delimitados.
- **Balões de fala** para falas de personagens; o bico do balão deve apontar para quem está falando.
- **Caixas retangulares** para narração, lugar, contexto, passagem do tempo e resumo de ações.
- Deixar clara a distinção entre fala e narração.
- Composição adaptável à quantidade de cenas necessária; não impor seis quadros ou rodapé pedagógico sem exigência explícita.
- Título com hierarquia visual clara.
- Textos curtos, legíveis, com alto contraste e margens internas.
- Não sobrepor texto a rostos, gestos ou objetos importantes.
- Manter anatomia plausível, silhuetas claras, paleta equilibrada e continuidade visual.
- A arte não pode introduzir fatos narrativos ausentes da fonte.

O primeiro mockup é avaliado sobretudo por legibilidade, hierarquia, composição, fluxo de leitura, adequação dos balões/retângulos e potencial de reutilização.

## 6. Idioma obrigatório: português brasileiro

Todo conteúdo editorial gerado pelo projeto deve estar em **português brasileiro (pt-BR)**, salvo pedido expresso de outro idioma. Isso se aplica a títulos, balões, narrações, legendas, painéis pedagógicos, instruções exibidas na imagem, documentação e relatório final.

Antes da geração e antes da aprovação, revisar:
- ortografia e acentuação;
- pontuação;
- concordância nominal e verbal;
- naturalidade do diálogo em português brasileiro;
- consistência de nomes, termos e formas de tratamento;
- texto que não corresponda ao que foi planejado.

Não misturar formas brasileiras e europeias de maneira inconsistente. Não considerar texto deformado ou ilegível como aprovado. Se a ferramenta falhar ao renderizar letras, registrar a falha e, se viável, inserir o texto em uma etapa de diagramação posterior.

## 7. Skills e ferramentas

### Principal: Higgsfield

- Repositório oficial: https://github.com/higgsfield-ai/skills
- Skill de geração: https://github.com/higgsfield-ai/skills/blob/main/higgsfield-generate/SKILL.md

Consultar a versão atual diretamente no GitHub antes de cada geração e ler as instruções relevantes. Uma cópia local pode estar desatualizada e não é a autoridade da versão. Confirmar que CLI/integração e credenciais estão realmente operacionais antes de declarar execução.

### Complemento: GPT Image 2 Prompt Library

- Repositório: https://github.com/freestylefly/awesome-gpt-image-2
- Skill: https://github.com/freestylefly/awesome-gpt-image-2/blob/main/agents/skills/gpt-image-2-style-library/SKILL.md

Usar quando útil para procurar exemplos e modelos de prompt por categoria, estilo, cena, composição e tratamento de texto. É uma biblioteca comunitária complementar, não substitui a narrativa, as regras do template ou a documentação oficial da ferramenta de geração. Adaptar exemplos ao objetivo e revisar o conteúdo em português brasileiro; não copiar automaticamente estruturas irrelevantes.

### Método de saída

A geração pode ser feita pelo ChatGPT ou por uma ferramenta externa realmente disponível. Registrar apenas o método que foi de fato utilizado. Um link ou uma skill no GitHub não prova instalação ou execução.

## 8. Quantidade e estado

- Uma solicitação de mockup final = uma chamada destinada à saída final; usar quantidade 1 quando suportada.
- Não gerar variantes/lotes sem solicitação explícita.
- O estado permanece `AGUARDANDO APROVAÇÃO VISUAL DO USUÁRIO` até aprovação ou pedido de ajustes.
- Não marcar a história demonstrativa como concluída.
- Não afirmar salvamento no GitHub sem confirmar o arquivo e o caminho real.

## 9. Checklist de aprovação

- [ ] Linguagem visual adequada ao propósito.
- [ ] Balões e caixas retangulares são visualmente distintos.
- [ ] É fácil identificar quem fala e a ordem de leitura.
- [ ] Texto em português brasileiro correto e legível, ou com áreas adequadas para composição posterior.
- [ ] Layout pode adaptar-se a histórias diversas.
- [ ] Composição tem hierarquia e espaço visual suficiente.
- [ ] Anatomia, rostos, mãos e objetos não apresentam falhas graves.
- [ ] Conteúdo sintético não é apresentado como fato canônico.
- [ ] Fontes/skills e método real de geração estão registrados.
- [ ] Estado de aprovação permanece pendente até a validação do usuário.

## 10. Relatório

Informar Template ID/versão, tema, fontes consultadas, versão e URL da skill Higgsfield consultada, uso (ou não) da biblioteca GPT Image 2, ferramenta efetivamente utilizada, resultado da inspeção, estado de aprovação e caminho real do arquivo caso tenha sido salvo.
