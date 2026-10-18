# PROMPT-1.0.6 — ROTA-SKILLS-ESTUDO-BIBLICO

-   **ID:** PROMPT-ESTUDO-BIBLICO-ROTA-SKILLS
-   **Versão:** 1.0.6
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
-   seis quadros narrativos principais em duas linhas de três;
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

1. Identificar o número solicitado.
2. Consultar a branch `main` do GitHub e ler a entrada completa da história exata em `historia-novo-testamento.md`.
3. Consultar a linha correspondente em `status-criacao-historia.md`.
4. Comparar número e título entre fonte narrativa e relatório. Se houver divergência, interromper e informar os dois valores.
5. Se a linha não existir no relatório, interromper e informar; não deduzir o estado nem criar uma linha automaticamente.
6. Se estiver `CONCLUIDA`, não gerar novamente sem solicitação explícita. Se estiver `EM_GERACAO`, `GERADA_A_VALIDAR` ou `BLOQUEADA`, interromper e informar o estado; somente `PENDENTE` permite iniciar nova geração.
7. Consultar visualmente as imagens de referência 001 e 002 quando estiverem acessíveis. Se não puderem ser acessadas, declarar a limitação.
8. Preparar uma única prancha horizontal com exatamente seis quadros narrativos em duas linhas de três e os três painéis pedagógicos obrigatórios.
9. Fazer uma única chamada destinada à imagem final, configurando quantidade igual a 1 quando a ferramenta permitir. Não pedir alternativas nem executar chamadas paralelas.
10. Validar identidade narrativa, sequência, ortografia, legibilidade, composição e consistência visual.
11. Salvar uma única imagem final no nome canônico calculado a partir do título oficial, desde que a ferramenta e o ambiente permitam a gravação.
12. Confirmar o arquivo e o nome no destino. Não declarar que a imagem foi salva se só tiver sido exibida no chat.
13. Atualizar somente a linha existente do relatório após a validação e o salvamento confirmados.
14. Informar resultado, caminho confirmado e estado real. Se alguma operação não puder ser executada, declarar a limitação; nunca inventar uma confirmação.

### REGRA CRÍTICA — UMA ÚNICA IMAGEM FINAL

Para cada comando `Gere a História NNN`, o resultado esperado é exatamente uma imagem final.

1. Configure a ferramenta para produzir uma única imagem por chamada, quando o parâmetro estiver disponível.
2. Faça uma única chamada destinada à composição final. Não solicite quatro variações nem execute chamadas paralelas para a mesma história.
3. Todos os quadros narrativos e os três painéis pedagógicos devem estar integrados na mesma imagem.
4. Se a ferramenta retornar várias imagens apesar da configuração solicitada, não as trate como entregas finais múltiplas. Avalie no máximo uma candidata, sem aprová-la automaticamente.
5. Confira a identidade narrativa da candidata antes de salvá-la. Se representar outra história ou misturar histórias, rejeite-a.
6. Não gere alternativas automaticamente. Antes de uma nova tentativa, identifique e corrija a falha anterior.
7. Preserve imagens já aprovadas. Não sobrescreva nem exclua arquivos existentes sem autorização explícita.
8. Se não for possível controlar tecnicamente a quantidade, informe essa limitação; não afirme que a geração única foi garantida.

**Critério de entrega:** uma história solicitada, uma imagem final aprovada e um único arquivo oficial. Imagens de trabalho não equivalem a imagens aprovadas.

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

Estados permitidos: `PENDENTE`, `EM_GERACAO`, `GERADA_A_VALIDAR`, `CONCLUIDA` e `BLOQUEADA`.

Valores de validação: `NÃO_INICIADA`, `PENDENTE`, `APROVADA` e `REPROVADA`.

### Regras de leitura e atualização

- Compare número e título com a entrada exata de `historia-novo-testamento.md`. Se houver divergência, interrompa e informe ambos os valores.
- Só inicie uma nova geração quando a linha existente estiver `PENDENTE`. Se estiver `CONCLUIDA`, não regenere sem solicitação explícita; se estiver `EM_GERACAO`, `GERADA_A_VALIDAR` ou `BLOQUEADA`, interrompa e informe o estado.
- Se a história não possuir linha no relatório, não deduza seu estado e não crie uma linha automaticamente. Interrompa e solicite regularização do relatório.
- Atualize somente a linha existente correspondente à história solicitada. Não duplique registros nem altere as outras histórias.
- Marque `CONCLUIDA` e `APROVADA` somente após geração efetiva, validação editorial, salvamento confirmado do arquivo canônico e atualização confirmada do relatório.
- Se o gerador não permitir salvar o arquivo ou não houver permissão para atualizar o relatório, descreva a limitação e mantenha o estado real; nunca declare uma conclusão não confirmada.

### Integridade do relatório

A meta do projeto é registrar uma linha por história, para as 232 histórias. O arquivo atualmente publicado contém somente os registros 001, 002 e 003. Não invente nem preencha automaticamente as 229 linhas ausentes: a expansão ou normalização do relatório é uma ação separada, que exige conferir os títulos oficiais e definir os estados reais. Até que isso seja regularizado, uma história sem registro está bloqueada para geração.

## 7. Critérios para aprovação

A história só pode ser marcada `CONCLUIDA` quando: - número e título
conferem com a fonte; - a narrativa e a ordem dos acontecimentos estão
corretas; - a prancha segue a composição e o estilo visual das
referências 001 e 002; - os seis quadros narrativos e os três painéis
inferiores estão presentes; - os três títulos pedagógicos estão escritos
corretamente; - textos estão legíveis e revisados; - existe uma única
imagem final oficial no destino; - nome e caminho estão corretos; - a
linha correspondente do relatório foi atualizada com sucesso.

Se houver erro, usar `GERADA_A_VALIDAR` ou `BLOQUEADA`, conforme o caso.
Não aprovar apenas porque a imagem foi gerada.

## 8. Skills e ferramentas

-   Consultar [Higgsfield
    Skills](https://github.com/higgsfield-ai/skills) como referência de
    skills de criação visual, caso a skill adequada esteja disponível no
    ambiente.
-   Verificar a skill e a ferramenta reais antes de afirmar que foram
    instaladas ou executadas.
-   Se a skill não estiver disponível, usar a ferramenta de geração de
    imagens disponível e declarar essa limitação. Não inventar execução
    de skill.
-   A ferramenta deve receber instruções explícitas para seguir as
    imagens de referência aprovadas, o nome canônico e a composição
    especificada.

## 9. Fonte de verdade e precedência

- O GitHub é a fonte oficial versionada dos arquivos do projeto. A Biblioteca do ChatGPT é uma cópia de trabalho, salvo se uma integração explícita determinar o contrário.
- Para o conteúdo narrativo, `historia-novo-testamento.md` é a fonte de verdade; para estado de produção, `status-criacao-historia.md` é a fonte de verdade.
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

Ao receber `Gere a História NNN`, processar apenas a história
solicitada. Consultar a fonte oficial, verificar o status, consultar as
referências 001 e 002, gerar uma única prancha no padrão aprovado,
salvar com o nome canônico e atualizar apenas a linha correspondente do
relatório.

**Resultado esperado:** uma história = uma imagem final na pasta
`imagens/` + uma única linha correspondente no relatório.
