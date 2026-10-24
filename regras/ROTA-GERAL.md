# Rota geral — produção por templates

**Versão:** 3.0.0  
**Idioma:** português brasileiro  
**Repositório canônico:** `milson-rodrigues/geracao-de-historia`, branch `main`.

## 1. Objetivo

Definir fluxo universal para produzir mockups, imagens e outros ativos a partir de Template ID, sem amarrar o processo a uma coleção específica.

## 2. Entrada

O usuário fornece o Template ID e a história/ativo. Campos adicionais dependem do template. Para mockup universal, o ID é `TPL-MOCKUP-UNIVERSAL`.

Consulte primeiro [`templates/CATALOGO.md`](../templates/CATALOGO.md). Se o ID não existir ou o arquivo estiver ausente, pare e informe.

## 3. Ordem obrigatória de consulta

1. [`ROUTER-MESTRE.md`](../ROUTER-MESTRE.md) e [`regras/00-LEIA-PRIMEIRO.md`](00-LEIA-PRIMEIRO.md).
2. Catálogo e template exato.
3. Fonte narrativa atual: `historias/historias-<nome-historia>.md`.
4. Manifesto da mesma coleção: `historias/status-criacao-historia.<nome-historia>.md), se aplicável.
5. Regras de skills, visual e validação.
6. Documentação atual da skill/ferramenta principal no repositório oficial, quando acessível.
7. Recursos complementares aprovados pelo template, por exemplo a biblioteca `awesome-gpt-image-2`.
8. Referências visuais apenas se realmente acessíveis.

Verifique a árvore atual e leia os arquivos no GitHub antes da geração. Não confie em caminhos memorizados ou cópias locais como fonte da versão atual.

## 4. Contrato de fontes

O mesmo identificador `<nome-historia>` deve ser usado no arquivo narrativo e no manifesto. O padrão esperado é:

- `historias/historias-<nome-historia>.md`
- `historias/status-criacao-historia.<nome-historia>.md`

Não assumir que o arquivo existe; validar caminho, conteúdo, coleção e correspondência entre os arquivos. A narrativa define fatos e sequência; status define somente o progresso registrado para essa coleção.

## 5. Idioma e ortografia

O idioma padrão do projeto é **português brasileiro (pt-BR)**. Isso vale para títulos, legendas, falas, narrações, textos dentro da imagem, nomes de campos, relatórios e documentação criada para o usuário.

Revisar antes de gerar/aprovar: ortografia, acentuação, pontuação, concordância nominal/verbal, pronomes, naturalidade do diálogo e consistência dos termos. Não misturar português europeu e brasileiro. Não apresentar texto deformado/ilegível como válido; quando a geração de texto em imagem falhar, registrar o problema e preferir diagramação posterior se possível.

## 6. Separação de autoridade

- Narrativa canônica: fatos, personagens, acontecimentos, ordem.
- Template: formato do ativo, contexto, parâmetros e critérios específicos.
- Regras globais: integridade e qualidade.
- Skill principal: método técnico de geração quando acessível e operacional.
- Biblioteca complementar: inspiração/estruturas de prompt, não fonte de verdade da narrativa.
- Manifesto: estado de produção confirmado.

## 7. Roteamento de ferramentas

### Principal

Consultar a versão atual da skill oficial Higgsfield: https://github.com/higgsfield-ai/skills/blob/main/higgsfield-generate/SKILL.md. Verificar documentação, ferramenta/CLI, autenticação e parâmetros disponíveis. Uma página no GitHub não prova execução no ambiente atual.

### Complementar: GPT Image 2

Consultar, quando útil, https://github.com/freestylefly/awesome-gpt-image-2 e sua skill `agents/skills/gpt-image-2-style-library/SKILL.md`. Usá-lo para procurar estruturas de prompt, estilos e exemplos relevantes. Não tratar esse repositório comunitário como substituto da documentação oficial da ferramenta nem copiar um prompt incompatível sem adaptação.

### Método de saída

A imagem pode ser gerada no ChatGPT ou por ferramenta externa realmente disponível. Declarar somente o método usado de fato. Para cada solicitação final, fazer uma única chamada de geração destinada à saída final e usar quantidade 1 quando suportada; não produzir variantes sem solicitação explícita.

## 8. Validação

Aplicar critérios específicos do template e consultar [padrão visual](PADRAO-VISUAL-E-COMPOSICAO.md) e [validação final](VALIDACAO-FINAL.md). Verificar fidelidade, sequência, composição, anatomia, consistência, ortografia pt-BR, legibilidade e requisitos específicos do ativo.

## 9. Estado, salvamento e relatório

Geração não é aprovação. Não declarar caminho, salvamento, aprovação, commit ou status atualizado sem evidência. Não sobrescrever ativos aprovados sem autorização.

Relatório: Template ID/versão; título/coleção; fontes consultadas; versões de skills/documentação consultadas; método/ferramenta realmente usada; parâmetros/quantidade; validação; arquivo/caminho confirmado; mudança de status confirmada e pendências.

## 10. Escrita obrigatória de volta no GitHub

Esta regra vale para qualquer executor: ChatGPT, agente local, agente remoto ou pessoa, desde que tenha acesso autorizado ao GitHub. Não existe fluxo especial que permita criar ou alterar conteúdo narrativo e ignorar o registro canônico.

### Contrato de gravação pareada

Sempre que criar ou modificar uma história, atualizar os dois arquivos correspondentes:

1. Narrativa: `historias/historias-<nome-historia>.md`.
2. Status: `historias/status-criacao-historia.<nome-historia>.md`.

O identificador `<nome-historia>` deve ser idêntico nos dois caminhos. Atualizar ambos na mesma tarefa e, sempre que possível, no mesmo commit. O arquivo de narrativa recebe o conteúdo narrativo revisado; o manifesto registra o estado real, a referência, as alterações e as pendências. Não substituir a narrativa por um resumo de status nem colocar o status apenas na narrativa.

### Protocolo de escrita

1. Ler a versão atual de ambos os arquivos e verificar a árvore da branch de destino.
2. Preservar conteúdo existente não relacionado e verificar se a história já existe; não criar duplicatas.
3. Preparar as alterações dos dois arquivos, mantendo consistência entre título, identificador, referência e estado.
4. Gravar os dois arquivos no GitHub com acesso autorizado. Se a ferramenta permitir apenas commits separados, registrar ambos e verificar os dois resultados.
5. Reabrir os arquivos atualizados e confirmar o conteúdo, os caminhos e os commits. Só então informar que o GitHub foi atualizado.
6. Se não houver acesso, autorização ou ferramenta funcional para gravar, não afirmar que os arquivos foram atualizados: fornecer o conteúdo/diff e marcar a gravação como pendente.
7. Se apenas um arquivo puder ser gravado, informar a inconsistência explicitamente e concluir a gravação do par antes de declarar a tarefa concluída. Não inventar status nem caminhos.

A geração de uma imagem sem alteração da narrativa ainda exige atualizar o manifesto quando o estado de produção mudar. Não alterar a narrativa sem necessidade apenas para produzir um commit artificial. A criação de um novo registro de história exige criar o par de arquivos.


## Proporção e qualidade padrão

Se o template ou o usuário não determinar outra coisa, gerar em 16:9 horizontal com mínimo Full HD (1920 × 1080); preferir resolução nativa maior quando suportada. O formato vertical 9:16 (mínimo 1080 × 1920) só deve ser usado quando solicitado explicitamente. Consultar os modelos pareados em `mockups/` e manter claro qual é o padrão e qual é a variante. Antes de declarar qualidade, verificar as dimensões reais da saída raster. Para SVG, registrar a prancheta vetorial e as dimensões usadas na exportação.
