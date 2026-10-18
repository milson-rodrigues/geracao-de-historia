# PROMPT-1.0.3 --- ROTA-SKILLS-ESTUDO-BIBLICO

-   **ID:** PROMPT-ESTUDO-BIBLICO-ROTA-SKILLS
-   **Versão:** 1.0.4
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

1.  Identificar o número solicitado.
2.  Ler diretamente a entrada completa da história exata em
    `historia-novo-testamento.md`.
3.  Consultar a linha dessa história em `status-criacao-historia.md`.
4.  Se já estiver `CONCLUIDA`, não gerar novamente sem solicitação
    explícita. Em caso de status ausente ou divergente, não deduzir o estado: conferir fonte e relatório, e registrar a incerteza.
5.  Consultar visualmente as imagens 001 e 002 como referência.
6.  Criar uma única prancha final com seis quadros narrativos e os três
    painéis pedagógicos.
7.  Revisar fidelidade narrativa, sequência, ortografia, legibilidade,
    composição e consistência visual.
8.  Salvar uma única imagem final no caminho canônico calculado a partir
    do título oficial.
9.  Confirmar que o arquivo existe no destino correto e que seu nome
    está correto.
10. Atualizar a linha existente da história no relatório. Nunca
    adicionar uma segunda linha para o mesmo número.
11. Informar o resultado, o caminho confirmado e o estado real da
    validação.

Se a ferramenta produzir várias opções, selecionar somente uma para
validação e gravação. Não declarar que há uma imagem salva se o ambiente
apenas a exibiu no chat.

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

## 6. Relatório com uma linha por história

`status-criacao-historia.md` deve conter uma tabela Markdown com uma
linha por história. Não escrever blocos de parágrafos por história, não
criar relatórios paralelos e não duplicar linhas.

Modelo:

  -------------------------------------------------------------------------------------------------------------------------
              Nº Título       Estado      Arquivo                                              Validação      Observações
                 oficial                                                                                      
  -------------- ------------ ----------- ---------------------------------------------------- -------------- -------------
             001 O mundo      CONCLUIDA   imagens/001-mundo-antes-do-nascimento-de-jesus.png   APROVADA       ---
                 antes do                                                                                     
                 nascimento                                                                                   
                 de Jesus                                                                                     

             002 O anjo       CONCLUIDA   imagens/002-anjo-gabriel-aparece-a-zacarias.png      APROVADA       ---
                 Gabriel                                                                                      
                 aparece a                                                                                    
                 Zacarias                                                                                     

             003 Confirmar na PENDENTE    ---                                                  NÃO_INICIADA   ---
                 fonte                                                                                        
                 oficial                                                                                      
  -------------------------------------------------------------------------------------------------------------------------

As linhas acima são exemplos de formato; confirmar o conteúdo e o estado
reais antes de adotá-las.

Colunas obrigatórias: - `Nº`: número com três dígitos. -
`Título oficial`: copiar exatamente da fonte narrativa. - `Estado`:
estado atual. - `Arquivo`: caminho relativo a partir de
`Biblioteca/Estudo Bíblico/`. - `Validação`: estado da revisão
editorial. - `Observações`: nota curta ou `—`, sempre na mesma linha da
tabela.

Estados permitidos: - `PENDENTE` - `EM_GERACAO` - `GERADA_A_VALIDAR` -
`CONCLUIDA` - `BLOQUEADA`

Valores de validação: - `NÃO_INICIADA` - `PENDENTE` - `APROVADA` -
`REPROVADA`

Ao atualizar: - editar a linha existente do número solicitado; - não
inserir uma segunda linha para o mesmo número; - manter cada história em
uma única linha de tabela; - atualizar a data geral do relatório apenas
com a data real; - usar o caminho canônico do arquivo; - marcar
`CONCLUIDA` somente após salvamento confirmado e validação aprovada; -
se a gravação falhar, informar que o relatório não foi atualizado.

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
