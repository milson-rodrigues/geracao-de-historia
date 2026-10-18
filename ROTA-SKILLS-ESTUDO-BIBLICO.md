# PROMPT-1.1.2 — ROTA-SKILLS-ESTUDO-BIBLICO

-   **ID:** PROMPT-ESTUDO-BIBLICO-ROTA-SKILLS
-   **Versão:** 1.1.2
-   **Status:** Instrução operacional
-   **Objetivo:** produzir as histórias ilustradas do Novo Testamento
    mantendo o padrão visual aprovado, os nomes canônicos dos arquivos e
    um relatório com uma linha por história.
-   **Idioma:** português brasileiro

## 1. Arquivos e destinos oficiais

Biblioteca/Estudo Bíblico/ - `historia-novo-testamento.md` --- fonte
narrativa oficial; somente leitura. - `status-criacao-historia.md` ---
relatório central; uma linha por história. -
`ROTA-SKILLS-ESTUDO-BIBLICO.md` --- este documento de instruções. -
`imagens/` --- destino das imagens finais.

As imagens de referência aprovadas ficam em:

-   `Biblioteca/Estudo Bíblico/imagens/001-mundo-antes-do-nascimento-de-jesus.png`
-   `Biblioteca/Estudo Bíblico/imagens/002-anjo-gabriel-aparece-a-zacarias.png`

Antes de gerar uma história, abrir e consultar visualmente essas duas
imagens quando estiverem acessíveis. Elas são as referências oficiais de
composição, tipografia, molduras, paleta, densidade visual e estilo. Não
depender somente de uma descrição textual quando os arquivos puderem ser
inspecionados.

## 2. Padrão obrigatório de nome

O nome oficial de cada arquivo deve seguir exatamente:

`NNN-slug-do-titulo-oficial.png`

Regras: 1. `NNN` é o número da história com três dígitos: `001`, `002`,
..., `232`. 2. Usar o título oficial da história em
`historia-novo-testamento.md`. 3. Converter o título em minúsculas,
remover acentos e pontuação e separar palavras por hífens. 4. Usar
extensão `.png`. 5. Não usar nomes genéricos, nomes automáticos da
ferramenta, traduções livres, títulos inventados, espaços, sufixos como
`-v2`, `-final2` ou timestamps. 6. Exemplos canônicos: -
`001-mundo-antes-do-nascimento-de-jesus.png` -
`002-anjo-gabriel-aparece-a-zacarias.png` 7. Para a História 003,
confirmar o título oficial na fonte e então gerar o slug correspondente.
Não deduzir ou inventar o título. 8. Salvar a única imagem final em
`Biblioteca/Estudo Bíblico/imagens/`.

Não criar imagens finais fora dessa pasta. Não criar cópias extras na
pasta pai. Não manter alternativas, prévias ou versões duplicadas na
pasta oficial.

## 3. Referência visual obrigatória

A imagem final deve corresponder ao padrão visual das Histórias 001 e
002:

-   prancha horizontal em proporção aproximada de 16:9;
-   ilustração bíblica infantil com aparência 3D, detalhada, acolhedora
    e colorida;
-   paleta quente, luz clara e contraste suficiente para leitura;
-   cabeçalho superior decorativo de pergaminho, com número e título;
-   molduras de pergaminho coerentes entre os quadros;
-   exatamente seis quadros narrativos principais em duas linhas de três;
-   cada quadro deve conter uma ilustração e uma legenda narrativa curta, integrada ao próprio quadro e legível; numerar os quadros sem incluir a legenda não atende ao padrão;
-   as seis legendas devem ser redigidas antes da geração, em ordem narrativa, e conferidas contra a entrada exata da história na fonte oficial;
-   não omitir as legendas nem acrescentar fatos, falas ou motivações não sustentados pela história solicitada;
-   três painéis pedagógicos na faixa inferior, com os títulos exatos:
    -   `O QUE APRENDEMOS`
    -   `PERGUNTAS PARA A CRIANÇA`
    -   `ORAÇÃO`
-   folhagens e detalhes ornamentais nas bordas, sem prejudicar o
    conteúdo;
-   tipografia serifada, legível e visualmente compatível com as
    referências;
-   texto em português brasileiro, com ortografia revisada;
-   continuidade visual dos personagens recorrentes quando aplicável.

Não mudar para estilo de quadrinhos realista, mangá, pintura escura,
colagem fotográfica ou outra linguagem visual sem autorização explícita.
Não imitar os acontecimentos das Histórias 001 e 002: copiar o padrão
visual, não a narrativa.

## 4. Processo obrigatório por história

### 4.1 Comandos e fases

O fluxo tem duas fases obrigatórias e separadas. O mockup NÃO é a imagem final.

- `Gere a História NNN`: iniciar somente a Fase 1 — mockup para aprovação. Produzir exatamente um mockup e parar, esperando o usuário aprovar ou pedir alterações. Não gerar a imagem final neste turno.
- `Aprovado`, `Aprovado. Gere a imagem final da História NNN` ou confirmação inequívoca equivalente, após o mockup da história correta: autoriza a Fase 2 — gerar a imagem final. Só executar depois de confirmar que a aprovação corresponde ao mockup correto.
- `Refaça o mockup da História NNN`: produzir um único mockup substituto e parar novamente para aprovação.
- `Gere novamente a História NNN`: se existe imagem final aprovada, iniciar a Fase 1 com um novo mockup para revisão antes de substituir a versão aprovada. Não gerar diretamente a imagem final nem apagar a versão existente.
- Se o usuário reprovar ou apontar erro no mockup, não gerar outro automaticamente. Corrigir as orientações e aguardar um pedido explícito para refazer o mockup.

### 4.2 Consulta e identidade narrativa

1. Ler os arquivos da branch `main` através de uma ferramenta/conexão GitHub autenticada. Abrir ou citar links sem recuperar o conteúdo não conta como consulta. Se não houver acesso, informar o bloqueio e não presumir o conteúdo.
2. Consultar a entrada exata em `historia-novo-testamento.md` e copiar o número e o título oficiais.
3. Consultar `status-criacao-historia.md` e confirmar número, título, estado e existência do arquivo canônico.
4. Se a linha estiver ausente, confirmar a história na fonte e verificar se existe imagem final. Se não houver arquivo, criar apenas o registro da história solicitada como `PENDENTE | — | validacao: NÃO_INICIADA`; se existir arquivo não registrado, interromper para reconciliar sem sobrescrever.
5. Isolar a entrada narrativa da história solicitada até o próximo título de história. Não usar os tópicos de histórias vizinhas como conteúdo.
6. Antes de cada chamada de imagem, preparar um roteiro com título oficial literal, seis legendas numeradas, descrição visual por quadro e textos dos três painéis pedagógicos. Validar o roteiro contra a fonte e incluir esse conteúdo explicitamente no prompt enviado ao gerador.
7. Para a História 003, o título é `Isabel descobre que está grávida`. Conteúdo narrativo autorizado pelos tópicos: Isabel, Zacarias, gravidez, alegria e seis meses de gravidez. Não incluir a anunciação a Maria, Gabriel anunciando Jesus, Filho do Altíssimo, trono de Davi ou outros acontecimentos da História 004.

### 4.3 Fase 1 — mockup para aprovação

1. Gerar exatamente uma imagem de mockup, com cabeçalho `MOCKUP PARA APROVAÇÃO — NÃO É A IMAGEM FINAL` claramente visível, mantendo número, título, seis quadros com legendas e os três painéis pedagógicos.
2. Uma solicitação = uma única chamada de imagem. Não pedir múltiplas imagens, variantes, lote, chamadas paralelas, nem repetir a chamada automaticamente.
3. Mostrar o mockup ao usuário e resumir número, título, seis cenas/legendas previstas e eventuais limitações.
4. Atualizar o status para `MOCKUP_PARA_APROVACAO`, caminho final `—`, validação `PENDENTE`, se a escrita no GitHub estiver disponível. O mockup não pode ser registrado como imagem final nem salvo no nome canônico.
5. Parar e aguardar a decisão do usuário. Não iniciar a Fase 2 sem aprovação explícita.

### 4.4 Fase 2 — imagem final após aprovação

1. Confirmar que a aprovação corresponde ao mockup da história solicitada.
2. Executar uma única chamada destinada à imagem final, sem selo/etiqueta de mockup, com quantidade `1` quando suportada.
3. Validar título literal, narrativa exclusiva da história, seis legendas, três painéis pedagógicos, ortografia e legibilidade.
4. Se a imagem estiver errada, rejeitar e parar. Não tentar novamente, não abrir outra chamada e não gerar variações sem um novo comando explícito.
5. Salvar a imagem no nome canônico somente depois de validada. Atualizar o status para `CONCLUIDA` / `APROVADA` apenas com confirmação de salvamento e atualização do registro.
6. Se alguma operação não estiver disponível, informar a limitação sem afirmar que o arquivo foi salvo.

### REGRA CRÍTICA — UMA ÚNICA IMAGEM FINAL

Cada comando que solicita uma imagem permite **uma única chamada de geração e uma única imagem**. A primeira chamada gera somente o mockup; a imagem final exige aprovação explícita em um turno posterior. Não solicite variações, lotes ou chamadas paralelas. Não repita chamadas automaticamente após falha ou reprovação. Se a ferramenta retornar múltiplas imagens em uma única chamada, apresente no máximo uma como candidata, não a aprove automaticamente e não chame o gerador de novo sem comando explícito. Preserve toda imagem final aprovada até que uma substituta tenha sido aprovada e salva.

**Critério de entrega:** Fase 1 = mockup aguardando aprovação; Fase 2 = uma imagem final validada. O mockup nunca é a imagem oficial.

## 5. Controle de duplicatas e substituições

-   Uma história deve ter apenas um arquivo final oficial na pasta
    `imagens/`.
-   Antes de salvar, verificar se já existe um arquivo com o nome
    canônico.
-   Se o arquivo existente estiver aprovado, não o sobrescrever sem
    autorização explícita.
-   Se a história ainda estiver em revisão, corrigir a imagem de
    trabalho e manter apenas um arquivo oficial final. Não criar nomes
    alternativos como `v2`, `nova`, `final`, `final2` ou nomes
    automáticos.
-   Não excluir arquivos nem substituir uma imagem aprovada sem
    autorização.
-   Se forem encontradas duplicatas existentes, relatar os nomes
    encontrados e solicitar autorização antes de excluí-las. Não apagar
    automaticamente.

## 6. Relatório central de progresso

O arquivo `status-criacao-historia.md` é a fonte oficial do estado de produção e deve ser consultado diretamente na branch `main` do GitHub antes de cada execução.

### Formato efetivamente publicado

Cada registro usa uma única linha delimitada por barras verticais, neste formato:

```text
NNN | Título oficial | ESTADO | caminho/arquivo.png ou — | validacao: VALOR
```

Colunas obrigatórias: número com três dígitos; título oficial; estado de produção; caminho canônico da imagem ou `—`; validação editorial. Não converter o arquivo para outro formato, adicionar colunas ou reescrever seus registros sem uma alteração explícita e controlada.

Estados permitidos: `PENDENTE`, `EM_GERACAO`, `MOCKUP_PARA_APROVACAO`, `GERADA_A_VALIDAR`, `CONCLUIDA` e `BLOQUEADA`.

Valores de validação: `NÃO_INICIADA`, `PENDENTE`, `APROVADA` e `REPROVADA`.

### Regras de leitura e atualização

- Compare número e título com a entrada exata de `historia-novo-testamento.md`. Se houver divergência, interrompa e informe os dois valores.
- `PENDENTE` permite iniciar a Fase 1 (mockup), não a imagem final. `MOCKUP_PARA_APROVACAO` exige aguardar aprovação explícita; não gerar a imagem final automaticamente. `validacao: REPROVADA` descreve uma tentativa anterior e não bloqueia uma nova Fase 1 após novo comando.
- Se a história estiver `CONCLUIDA`, `Gere a História NNN` deve solicitar confirmação antes de substituir a imagem; `Gere novamente a História NNN` já é a confirmação explícita e deve prosseguir sem perguntar de novo.
- Se a linha não existir, consultar novamente o GitHub e a fonte narrativa. Se a história existir e não houver imagem no caminho canônico, o comando explícito do usuário autoriza criar a linha como `PENDENTE | — | validacao: NÃO_INICIADA` e continuar. Se existir uma imagem não registrada, interromper para reconciliar sem sobrescrevê-la.
- `EM_GERACAO` impede chamadas paralelas. Uma chamada por comando, sem loops de retry. Se falhar, relatar o problema e aguardar novo comando explícito.
- `BLOQUEADA` só deve impedir a geração enquanto persistir um impedimento real, como divergência narrativa, fonte inacessível ou arquivo preexistente não reconciliado. Uma imagem reprovada já excluída não é, por si só, motivo para permanecer bloqueada.
- Atualize somente a linha correspondente, sem duplicar registros nem alterar outras histórias. Marque `CONCLUIDA` e `APROVADA` somente após validação, salvamento confirmado e atualização confirmada do relatório.
- Se o gerador não permitir salvar ou não houver permissão de escrita, informar a limitação e manter o estado real.

### Integridade do relatório

A meta do projeto é registrar uma linha por história, para as 232 histórias. Não preencher em lote as linhas ausentes. Quando o usuário pedir explicitamente uma história cuja linha ainda não exista, aplicar a recuperação individual descrita na seção 4.2: confirmar o título na fonte e conferir o caminho canônico; se não houver arquivo de imagem, criar a linha como `PENDENTE | — | validacao: NÃO_INICIADA` e prosseguir. Se já houver arquivo não registrado, parar para reconciliar sem sobrescrever.

## 7. Critérios para aprovação

A história só pode ser marcada `CONCLUIDA` quando todos os itens forem confirmados:

- número e título correspondem à fonte oficial;
- a narrativa e a sequência dos acontecimentos estão corretas;
- a prancha mantém o padrão visual aprovado;
- existem exatamente seis quadros narrativos em duas linhas de três;
- **cada um dos seis quadros contém uma legenda narrativa curta, integrada e legível, além da ilustração e da numeração**;
- as seis legendas correspondem à história solicitada, sem mistura de narrativas ou detalhes não sustentados pela fonte;
- os três painéis inferiores estão presentes e os títulos estão corretos;
- todos os textos estão legíveis e revisados;
- existe uma única imagem final oficial no destino;
- nome e caminho canônicos estão corretos;
- salvamento e atualização da linha correspondente do relatório foram confirmados.

Quadro ilustrado sem legenda narrativa é falha editorial, mesmo quando a imagem visual é adequada. Se houver erro, use `GERADA_A_VALIDAR` enquanto a avaliação estiver pendente ou `BLOQUEADA` quando a falha impedir a continuação segura. Não aprove apenas porque a imagem foi gerada.

## 8. Roteamento de skills e recursos visuais

A escolha dos recursos deve ser orientada pela tarefa. Os links abaixo são fontes oficiais dos projetos externos indicados; consultá-los não significa que uma skill esteja instalada nem que tenha sido executada.

### 8.1 Skill principal de geração — `higgsfield-generate`

- Repositório: [higgsfield-ai/skills](https://github.com/higgsfield-ai/skills)
- Instruções da skill: [higgsfield-generate/SKILL.md](https://github.com/higgsfield-ai/skills/blob/main/higgsfield-generate/SKILL.md)

**Uso:** recurso principal para geração ou edição de imagem quando a skill e a ferramenta associada estiverem realmente disponíveis no ambiente. Antes de usar, consultar as instruções atuais da skill e verificar os parâmetros de geração suportados. Para cada história, solicitar uma única imagem final por chamada e definir quantidade igual a `1` quando houver esse parâmetro.

Se a skill não estiver instalada ou a ferramenta não estiver acessível, não declarar que foi executada. Usar apenas a ferramenta de geração realmente disponível e informar a limitação quando relevante.

### 8.2 Direção artística complementar — `taste-skill`

- Repositório: [Leonxlnx/taste-skill](https://github.com/Leonxlnx/taste-skill)

**Uso complementar:** consultar quando for necessário avaliar direção de arte, referências visuais, hierarquia de composição ou reduzir resultados genéricos. Aplicar somente os princípios compatíveis com a identidade visual já aprovada do projeto.

A taste-skill não substitui a fonte narrativa, o prompt visual oficial nem a ferramenta de geração. Não deve introduzir outro estilo a cada história nem autorizar a criação de múltiplas alternativas.

### 8.3 Recurso opcional para exploração visual — `open-design`

- Repositório: [nexu-io/open-design](https://github.com/nexu-io/open-design)

**Uso opcional:** considerar somente em tarefas específicas de exploração, organização ou discussão de conceitos e referências visuais, quando o ambiente realmente disponibilizar esse recurso e a tarefa se beneficiar dele.

`open-design` não é requisito para a geração normal de cada história e não deve ser acionado automaticamente para todas as execuções. Não substitui `higgsfield-generate` nem altera o requisito de produzir uma única prancha final por história.

### 8.4 Ordem de precedência

1. `historia-novo-testamento.md` determina exclusivamente a narrativa.
2. `ROTA-SKILLS-ESTUDO-BIBLICO.md` e `prompt-geracao-imagem.md` determinam o procedimento e o padrão visual do projeto.
3. As imagens aprovadas 001 e 002 determinam as referências visuais disponíveis.
4. As skills e ferramentas externas ajudam a executar ou avaliar o trabalho, mas não podem contrariar os itens anteriores.

Verificar a disponibilidade real de cada recurso antes de utilizá-lo. Nunca afirmar instalação, consulta ou execução sem evidência. Se uma skill estiver indisponível, seguir com os recursos de fato acessíveis e declarar a limitação; não inventar operações nem resultados.

## 9. Fonte de verdade e precedência

- O GitHub é a fonte oficial versionada dos arquivos do projeto. A Biblioteca do ChatGPT é uma cópia de trabalho, salvo se uma integração explícita determinar o contrário.
- Para o conteúdo narrativo, `historia-novo-testamento.md` é a fonte de verdade; para estado de produção, `status-criacao-historia.md` é a fonte de verdade. Como o repositório pode ser privado, é necessário acesso GitHub autorizado no ambiente que executa o comando; URLs públicas ou links na instrução não concedem essa autorização.
- A rota controla o procedimento; `prompt-geracao-imagem.md` detalha roteiro visual e validação. Em conflito entre esses dois documentos, a regra mais restritiva de identidade narrativa e uma imagem final prevalece, e a inconsistência deve ser resolvida sem inventar conteúdo.
- Não misturar conteúdo recuperado do GitHub com uma cópia da Biblioteca que possa estar desatualizada. Registrar a origem consultada em cada execução e informar indisponibilidade.

## 10. Integridade

-   Não alterar `historia-novo-testamento.md`.
-   Preservar as demais linhas do relatório.
-   Não inventar conteúdo, caminhos, datas, execução de ferramentas ou
    resultados.
-   Não declarar sucesso sem evidência de geração, salvamento e
    atualização.
-   Se a Biblioteca não estiver acessível para escrita, fornecer o
    arquivo resultante para importação manual e dizer claramente que a
    gravação direta ficou pendente.

## 11. Instrução de execução

Ao receber `Gere a História NNN`, executar exclusivamente a Fase 1: consultar a fonte e o status, preparar o roteiro, gerar um único mockup, registrar `MOCKUP_PARA_APROVACAO` e aguardar. Não gerar a imagem final no mesmo turno. Somente após aprovação explícita, executar a Fase 2 com uma única chamada de imagem. `Gere novamente a História NNN` também começa por um mockup de revisão quando já existe uma imagem final aprovada. Não executar chamadas automáticas repetidas.

**Resultado esperado:** uma história = uma imagem final na pasta
`imagens/` + uma única linha correspondente no relatório.
