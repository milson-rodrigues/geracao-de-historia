# Rota geral — produção por templates

**Versão:** 3.0.0  
**Idioma:** português brasileiro  
**Repositório canônico:** `milson-rodrigues/geracao-de-historia`, branch `main`.

## 1. Objetivo

Definir fluxo universal para produzir mockups, imagens e outros ativos a partir de Template ID, sem amarrar o processo a uma coleção específica.

## 2. Entrada

O usuário fornece o Template ID e a história/ativo. Campos adicionais dependem do template. Para mockup universal, o ID é `TPL-MOCKUP-UNIVERSAL`.

Consulte primeiro [`templates/CATALOGO.md`](../templates/CATALOGO.md). Se o ID não existir ou o arquivo estiver ausente, pare e informe.

## 3. Regra de bloqueio — consulta obrigatória ao GitHub

O `ROUTER-MESTRE.md` é o ponto de entrada estável e não deve receber alterações rotineiras. Ele encaminha para `regras/00-LEIA-PRIMEIRO.md`, que governa a sequência de consulta. Este documento define os detalhes da produção; não substitui nem reescreve a rota de entrada. Atualizações operacionais devem ocorrer aqui ou nas regras/templates especializados.

Toda nova solicitação de produção começa com consulta direta ao repositório canônico no GitHub, branch `main`. Repetir a consulta em cada solicitação/sessão. Memória, contexto de conversas anteriores, cópias locais e instruções antigas não substituem a versão atual.

Não iniciar geração sem concluir a ordem de consulta, confirmar os arquivos e ler a narrativa oficial. Se o GitHub ou uma fonte essencial estiver indisponível, interromper e informar o bloqueio; não completar lacunas por suposição.

## 3. Ordem obrigatória de consulta

1. `ROUTER-MESTRE.md` já consultado como ponto de entrada; seguir [`regras/00-LEIA-PRIMEIRO.md`](00-LEIA-PRIMEIRO.md).
2. Catálogo e template exato.
3. Fonte narrativa atual: `historias/historias-<nome-historia>.md`.
4. Manifesto da mesma coleção: `historias/status-criacao-historia.<nome-historia>.md`, se aplicável.
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

## 4A. Controle de repetição

Antes de gerar, consultar o manifesto de status da coleção e procurar o identificador exato da história. Se já houver registro de imagem gerada, validada ou aprovada, não gerar outra automaticamente; pedir confirmação ou aguardar solicitação explícita de nova versão. Se o manifesto estiver ausente, vazio ou incompleto, classificar o histórico como desconhecido, nunca como prova de que não houve geração anterior.

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

## 10. Registro e persistência no GitHub

O objetivo principal é gerar a imagem fiel à história. Criar uma cópia individual do roteiro no repositório é **opcional**, útil para rastreabilidade, e não deve bloquear a geração se a fonte canônica já estiver disponível e puder ser consultada.

### Antes da geração

1. Verificar a árvore atual do GitHub e ler a fonte narrativa que contém a história.
2. Se o usuário forneceu um arquivo `.md`, usar esse arquivo como fonte da tarefa; compará-lo com a fonte canônica quando houver uma correspondência clara.
3. Não criar uma cópia individual automaticamente. Fazê-lo quando o usuário solicitar ou quando houver benefício concreto de rastreio e acesso de escrita.
4. Nunca sobrescrever arquivo existente sem ler e preservar conteúdo não relacionado.

### Depois da geração

1. Se o estado da história mudou (por exemplo, imagem gerada, validada, aprovada ou com pendência), atualizar o manifesto de status da coleção correspondente, caso haja acesso autorizado ao GitHub.
2. Se foi solicitada uma cópia individual, gravá-la em `historias/` com nome claro e origem indicada. Não usar a cópia como substituto silencioso da fonte canônica.
3. Reabrir os arquivos alterados e confirmar conteúdo, caminho e commit antes de declarar que foram salvos.
4. Se não houver acesso de escrita, fornecer o conteúdo ou diff e informar que a gravação está pendente. A geração da imagem não depende de criar a cópia opcional.

### Convenção dos arquivos de rastreio

- Fontes de coleção: `historias/historias-<nome-colecao>.md`.
- Manifestos de status por coleção: `historias/status-criacao-historia.<nome-colecao>.md`.
- Cópia individual opcional: nome descritivo em `historias/`, sem sobrescrever arquivos existentes.

O identificador de coleção deve ser consistente entre a fonte e o manifesto quando ambos existirem. Não inventar status nem commits.

## 11. Política de armazenamento de imagens

Imagens finais geradas não devem ser enviadas, commitadas ou armazenadas no GitHub. O repositório é a fonte de verdade para narrativas, templates, regras e controle textual de status. Quando autorizado e possível, atualizar somente o manifesto textual da coleção e confirmar a gravação. A imagem exibida no chat não equivale a arquivo salvo no GitHub.

## Proporção e qualidade padrão

Se o template ou o usuário não determinar outra coisa, gerar em 16:9 horizontal com mínimo Full HD (1920 × 1080); preferir resolução nativa maior quando suportada. O formato vertical 9:16 (mínimo 1080 × 1920) só deve ser usado quando solicitado explicitamente. Consultar os modelos pareados em `mockups/` e manter claro qual é o padrão e qual é a variante. Antes de declarar qualidade, verificar as dimensões reais da saída raster. Para SVG, registrar a prancheta vetorial e as dimensões usadas na exportação.
