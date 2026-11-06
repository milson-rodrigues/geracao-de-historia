# Rota geral — produção por templates

**Versão:** 3.1.0  
**Idioma:** português brasileiro  
**Repositório canônico:** `milson-rodrigues/geracao-de-historia`, branch `main`.

## 1. Objetivo

Definir fluxo universal para produzir mockups, imagens e outros ativos a partir de Template ID, sem amarrar o processo a uma coleção específica.

## 2. Entrada e autoridade operacional

O ponto de entrada estável é [`ROUTER-MESTRE.md`](../ROUTER-MESTRE.md). Ele encaminha para [`00_GUIA-DE-CONFIGURACAO.md`](../00_GUIA-DE-CONFIGURACAO.md), que é a fonte operacional mutável e define a ordem vigente de consulta.

Para cada produção, consultar o guia atual no GitHub, branch `main`, e seguir sua sequência. Este documento detalha regras gerais de produção, mas não substitui o guia nem o bootstrap estável.

Consulte primeiro [`templates/CATALOGO.md`](../templates/CATALOGO.md). Se o ID não existir ou o arquivo estiver ausente, pare e informe.

## 3. Consulta obrigatória e bloqueios

Toda nova solicitação começa com consulta direta ao repositório canônico. Repetir em cada solicitação/sessão. Memória, conversas anteriores, cópias locais e instruções antigas não substituem a versão atual.

Não iniciar geração sem concluir a ordem de consulta, confirmar os arquivos e ler a narrativa oficial. Se o GitHub ou uma fonte essencial estiver indisponível, interromper e informar o bloqueio; não completar lacunas por suposição.

## 4. Ordem de consulta

Seguir a ordem completa definida em [`00_GUIA-DE-CONFIGURACAO.md`](../00_GUIA-DE-CONFIGURACAO.md). Em linhas gerais: catálogo e template exato; fonte narrativa; manifesto aplicável; regras de skills, visual e validação; documentação atual da ferramenta principal e referências complementares pertinentes.

## 5. Contrato de fontes e duplicidade

O mesmo identificador de coleção deve ser usado na fonte narrativa e no manifesto quando ambos existirem. Padrões esperados:

- `historias/historias-<nome-colecao>.md`
- `historias/status-criacao-historia.<nome-colecao>.md`

Não assumir que o arquivo existe; validar caminho, conteúdo, coleção e correspondência. A narrativa define fatos e sequência; status define somente o progresso registrado.

Antes de gerar, consultar o manifesto e procurar o ID exato da história. Se já houver registro de imagem gerada, validada ou aprovada, não gerar outra automaticamente; exigir solicitação explícita de nova versão. Se o manifesto estiver ausente, vazio ou incompleto, classificar o histórico como desconhecido.

## 6. Idioma, ferramentas e validação

O idioma padrão é português brasileiro (pt-BR). Aplicar as regras atuais de skills, direção visual, proporção, requisitos pedagógicos e validação definidas no guia operacional, no template e nos documentos especializados.

Uma skill publicada não prova que a ferramenta esteja instalada, conectada ou operacional. Declarar somente o método efetivamente utilizado. Geração não equivale a aprovação.

## 7. Estado e persistência

Não declarar caminho, salvamento, aprovação, commit ou status atualizado sem evidência. Imagens finais não devem ser enviadas, commitadas ou armazenadas no GitHub. O repositório mantém fontes, templates, regras e registros textuais autorizados.

## 8. Relatório

Informar Template ID/versão; título/coleção; fontes consultadas; documentação/skills consultadas; método/ferramenta realmente utilizada; parâmetros/quantidade; validação; caminho real do arquivo, se salvo; mudanças de status confirmadas e pendências.


## 9. Gate de confirmação antes de qualquer imagem

Não gerar, pesquisar nem exibir imagens de prévia antes de concluir a consulta às fontes, identificar o template, verificar o manifesto e resolver ambiguidades materiais.

Se o tipo de saída não estiver inequívoco (por exemplo, mockup de quadrinhos ou ilustração única), apresentar a pergunta de esclarecimento em texto e aguardar a resposta. Enquanto aguarda, não chamar gerador de imagens, não pesquisar imagens ilustrativas e não exibir referências visuais. Não criar imagem demonstrativa para explicar opções.

Quando o escopo estiver claro, realizar uma única geração final, quantidade 1 quando suportada. Pesquisar/exibir imagens externas somente quando o usuário solicitar referências; identificá-las como referências externas e nunca como resultado gerado. Imagens com marca d'água ou de terceiros não podem ser apresentadas como ativos do projeto.
