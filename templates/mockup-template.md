# Template para mockup visual — modelo universal

- **Template ID:** `TPL-MOCKUP-UNIVERSAL`
- **Versão:** 1.1.1
- **Estado:** DIREÇÃO VISUAL APROVADA PELO USUÁRIO
- **Finalidade:** produzir uma imagem-mockup para validar a linguagem visual e a composição antes da produção de histórias finais.
- **Escopo:** qualquer coleção que possua uma fonte `historias/historias-<nome-historia>.md`.

## Artefatos vetoriais sincronizados no GitHub

A direção visual foi aprovada pelo usuário: banner superior de pergaminho, seis quadros narrativos, três painéis pedagógicos inferiores, paleta menos saturada, caixas retangulares de narração e balões de diálogo. Os dois SVGs estão no diretório `mockups/`: [`mockup-template-universal.svg`](../mockups/mockup-template-universal.svg) é o padrão horizontal 16:9 (1920 × 1080); [`mockup-template-universal-9x16.svg`](../mockups/mockup-template-universal-9x16.svg) é a variante vertical 9:16 (1080 × 1920). Os textos demonstrativos não são canônicos.

## 1. Objetivo

Gerar uma página-mockup visual para o usuário avaliar. A linguagem deve combinar ilustrações sequenciais, **balões de fala** para diálogos e **caixas retangulares** para narração/contexto. O layout deve ser adaptável a histórias diferentes, sem impor uma quantidade fixa de quadros.

A direção visual do mockup está aprovada; isso não aprova histórias finais, textos narrativos nem imagens produzidas para histórias específicas. Não altera o status de produção de nenhuma história real.

## 2. Entrada

Entrada natural recomendada: **“Gere a imagem da história. Título: 001 - Deus cria o mundo. Coleção: antigo-testamento.”** O usuário também pode anexar ou indicar um roteiro `.md`; não exigir que ele saiba o Template ID.

Localize a história no repositório antes de gerar. Se o usuário só informar o título, procure correspondência exata na coleção apropriada. Se houver mais de uma correspondência ou a coleção for necessária para decidir a fonte, pergunte apenas o detalhe que falta. Se o roteiro não existir no GitHub nem tiver sido fornecido, peça a fonte em vez de inventar contexto.

O método pode ser ChatGPT ou ferramenta externa, conforme disponibilidade real. Mockups demonstrativos sem história real devem ser identificados como demonstração, não como narrativa canônica.

## 3. Contrato universal de fontes

Fontes narrativas de coleção seguem o padrão `historias/historias-<nome-colecao>.md`. O manifesto para rastrear produção da coleção, quando utilizado, segue `historias/status-criacao-historia.<nome-colecao>.md`. O identificador deve ser consistente quando ambos existem.

O usuário também pode fornecer um roteiro individual em Markdown. **Copiar esse roteiro para o GitHub não é obrigatório**: a cópia em `historias/` serve para facilitar rastreabilidade e só deve ser criada quando solicitada ou útil. Não inventar convenção como se fosse obrigatória, não substituir a fonte da coleção e não sobrescrever arquivos existentes sem revisão.

O padrão de nome não prova que um arquivo existe. Consulte a árvore atual do GitHub e abra a fonte real; não dependa de nomes memorizados.

## 4. Leitura obrigatória antes de gerar

1. Consultar `ROUTER-MESTRE.md` no repositório canônico, na branch `main`.
2. Ler `regras/00-LEIA-PRIMEIRO.md`.
3. Verificar `templates/CATALOGO.md` e confirmar que `TPL-MOCKUP-UNIVERSAL` está disponível.
4. Ler a versão atual deste template.
5. Para uma história real, localizar e ler a fonte narrativa atual que contém o número e o título solicitados; normalmente é uma coleção `historias/historias-<nome-colecao>.md` ou um roteiro fornecido pelo usuário.
6. Ler o manifesto de status da coleção se existir e for relevante para o estado da produção. Sua ausência não bloqueia a geração quando a fonte narrativa é suficiente.
7. Ler `regras/ROTA-GERAL.md`, `regras/SKILLS-E-RECURSOS.md`, `regras/PADRAO-VISUAL-E-COMPOSICAO.md` e `regras/VALIDACAO-FINAL.md`.
8. Consultar documentação atual das skills externas no GitHub antes da geração.
9. Usar referências visuais apenas quando realmente acessíveis. Uma imagem anexada ao chat não é automaticamente um arquivo no repositório.

Se qualquer fonte essencial estiver ausente ou inacessível, informar o bloqueio. Não preencher lacunas com memória ou suposições.

## 5. Direção visual universal

- Layout de quadrinhos/graphic novel com sequência legível e quadros delimitados.
- **Balões de fala** para falas de personagens; o bico do balão deve apontar para quem está falando.
- **Caixas retangulares** para narração, lugar, contexto, passagem do tempo e resumo de ações.
- Deixar clara a distinção entre fala e narração.
- Composição adaptável à narrativa, mantendo como base aprovada seis quadros em grade 3 × 2 e os três painéis pedagógicos inferiores para histórias bíblicas infantis. Ajustar a quantidade de quadros somente quando a narrativa exigir e sem eliminar as perguntas ou a oração obrigatórias.
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

## 6A. Conteúdo pedagógico obrigatório para histórias infantis

Para cada história bíblica destinada a crianças, preparar no painel pedagógico:

- **Perguntas para a criança:** no mínimo três perguntas, específicas dos fatos e ensinamentos da história. Variar as perguntas para avaliar compreensão, reflexão e aplicação; não repetir um conjunto genérico em todas as histórias.
- **Oração:** oração desenvolvida, preferencialmente com 4 a 7 frases, em linguagem simples e adequada à idade, conectada à narrativa e ao ensinamento. Não entregar oração excessivamente curta ou genérica.
- **Encerramento obrigatório:** a última expressão da oração deve ser exatamente **“Em nome de Jesus, Amém!”**.

Revisar perguntas e oração antes da geração. Se o espaço da imagem não comportar todo o conteúdo com legibilidade, reorganizar o layout ou apresentar o conteúdo completo junto da imagem; não cortar perguntas nem abreviar a oração para caber.

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

## 7A. Consulta ao GitHub e prevenção de repetição

Antes de cada geração, consultar a versão atual deste repositório na branch `main`, seguir o roteador e a ordem de leitura obrigatória, confirmar o template e ler a narrativa oficial completa. Consultar o manifesto da coleção e verificar o ID exato. Se a história já estiver registrada como gerada/validada/aprovada, não repetir sem pedido explícito de nova versão. Manifesto vazio ou ausente significa histórico desconhecido.

Se GitHub ou fonte essencial estiver inacessível, bloquear a geração e informar o motivo; não usar memória ou cópias antigas como substituto.

## 8. Quantidade e estado

- Uma solicitação de mockup final = uma chamada destinada à saída final; usar quantidade 1 quando suportada.
- Não gerar variantes/lotes sem solicitação explícita.
- A direção visual do template está aprovada. Cada imagem final de história continua exigindo validação própria.
- Não marcar a história demonstrativa como concluída.
- Não enviar, commitar ou armazenar imagens finais no GitHub. O manifesto textual pode ser atualizado quando autorizado.
- Não afirmar salvamento em qualquer destino sem confirmar o arquivo e o caminho real.

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
- [x] Direção visual universal aprovada pelo usuário. (A aprovação de uma história final é independente.)

## 10. Relatório

Informar Template ID/versão, tema, fontes consultadas, versão e URL da skill Higgsfield consultada, uso (ou não) da biblioteca GPT Image 2, ferramenta efetivamente utilizada, resultado da inspeção, estado de aprovação e caminho real do arquivo caso tenha sido salvo.


## Regras de composição aprovadas

- **Formato:** horizontal 16:9.
- **Cabeçalho:** banner de pergaminho com número/identificador, título da história e referência bíblica.
- **Quadros narrativos:** seis quadros como composição-base, em grade 3 × 2; ajustar somente quando a narrativa exigir e o template específico permitir.
- **Painéis inferiores:** “O QUE APRENDEMOS”, “PERGUNTAS PARA A CRIANÇA” e “ORAÇÃO”.
- **Paleta:** tons quentes e naturais, com saturação moderada; evitar cores excessivamente vivas.
- **Narração:** caixas retangulares de pergaminho em área reservada. A quantidade de texto deve caber na caixa; redigir ou dimensionar o bloco antes de compor a ilustração.
- **Não obstruir texto:** personagens, cabelo, mãos, roupas, objetos e efeitos nunca podem cobrir títulos, narração, legendas ou balões. A área de texto deve ser planejada antes da ilustração.
- **Diálogos:** balões com cauda apontando inequivocamente para o falante; não posicionar entre personagens se houver ambiguidade.
- **Continuidade:** manter ficha visual de cada personagem e verificar rosto, cabelo, idade aparente, roupas e acessórios entre quadros. Não duplicar acidentalmente personagens no mesmo quadro.
- **Fidelidade narrativa:** cada quadro deve representar o trecho correspondente da fonte oficial e respeitar a ordem dos acontecimentos. Não repetir uma cena só para preencher espaço.
- **Idioma:** português brasileiro (pt-BR), com revisão de ortografia, acentuação, pontuação, concordância e legibilidade.
- **Revisão final:** inspecionar a imagem inteira e cada quadro ampliado; corrigir texto encoberto, balões ambíguos, personagens repetidos indevidamente e erros de contexto antes de aprovar um ativo final.


## 11. Proporção e qualidade de saída

- **Padrão obrigatório:** horizontal 16:9 quando o usuário não especificar outra proporção.
- **Qualidade mínima:** Full HD, 1920 × 1080 pixels para 16:9. Se a ferramenta suportar uma resolução nativa maior com boa qualidade, usar a maior opção adequada.
- **Exceção vertical:** usar 9:16 somente quando o usuário solicitar; mínimo 1080 × 1920 pixels.
- Os modelos vetoriais correspondentes ficam juntos em `mockups/`: `mockup-template-universal.svg` (padrão 16:9) e `mockup-template-universal-9x16.svg` (variante 9:16).
- Não inferir que o arquivo é Full HD apenas pela aparência. Conferir as dimensões da imagem raster final. SVG é escalável; para exportação, respeitar as dimensões mínimas acima.
- Ao entregar ambos os formatos, manter o arquivo horizontal como principal e rotular claramente a variante vertical.


## 12. Confirmação de escopo e bloqueio de prévias

Neste projeto, toda solicitação de geração de uma história bíblica tem como saída uma **prancha em quadrinhos** seguindo este template. Não perguntar se o usuário deseja prancha em quadrinhos ou ilustração única. O template universal define o formato de saída padrão.

- Não solicitar confirmação sobre prancha versus ilustração única: a prancha em quadrinhos é obrigatória para histórias.
- Antes dessa confirmação, não gerar imagem, não buscar imagens ilustrativas e não exibir referências ou prévias visuais.
- Não criar imagem de demonstração para explicar as opções.
- Perguntar apenas sobre requisitos especiais não definidos que alterem materialmente a prancha, como proporção excepcional ou composição específica.
- Após escopo definido e todas as fontes verificadas, fazer uma única geração final, quantidade 1 quando suportada.
- Imagens externas só podem ser exibidas como referências quando solicitadas explicitamente; devem ser identificadas como externas e nunca confundidas com resultado gerado.
