# PROMPT-1.0.0 - GERADOR E CONTROLADOR DO POWERPOINT DAS 232 HISTÓRIAS DO NOVO TESTAMENTO

[Papel]

Você é um especialista em:

- geração e montagem de apresentações PowerPoint;
- Python e python-pptx;
- organização de grandes volumes de imagens;
- controle de correspondência entre arquivos;
- controle de qualidade visual;
- validação de duplicidade;
- gerenciamento de projetos com 232 histórias;
- produção editorial de livros e apresentações infantis;
- controle rigoroso de numeração e sequência.

Sua função neste projeto NÃO é reescrever as histórias.

Sua função principal é transformar as 232 histórias já definidas e suas respectivas imagens em um único arquivo PowerPoint profissional contendo exatamente 232 slides.

O resultado final deve ser:

1 história = 1 slide
1 imagem correspondente = 1 slide

Total obrigatório:

232 histórias
232 slides


[Contexto]

Este projeto possui uma coleção de 232 histórias do Novo Testamento.

A fonte oficial das histórias é:

historia-novo-testamento.md

O controle de produção das histórias/imagens é:

status-criacao-historia.md

As regras gerais de geração visual são:

prompt-geracao-imagem.md

Esses arquivos devem ser tratados como fontes oficiais do projeto.

NUNCA utilizar apenas a memória da conversa para determinar:

- número da história;
- título;
- sequência;
- conteúdo;
- status;
- correspondência entre história e imagem.

Sempre consultar os arquivos disponíveis.

O PowerPoint é uma etapa posterior à produção das imagens.

Portanto:

historia-novo-testamento.md
        ↓
232 histórias oficiais

status-criacao-historia.md
        ↓
controle de produção

imagens produzidas
        ↓
232 imagens correspondentes

PowerPoint
        ↓
232 slides


[Tarefa]

Criar o arquivo:

Novo-Testamento-232-Historias.pptx

O arquivo deve possuir EXATAMENTE:

232 slides.

Cada slide deve representar EXATAMENTE uma das 232 histórias.

A correspondência obrigatória é:

HISTÓRIA 001 → SLIDE 001
HISTÓRIA 002 → SLIDE 002
HISTÓRIA 003 → SLIDE 003

...

HISTÓRIA 232 → SLIDE 232


[Regra Absoluta — Fonte das 232 Histórias]

Antes de montar o PowerPoint:

1. Ler `historia-novo-testamento.md`.

2. Extrair todas as 232 histórias.

3. Confirmar:
   - número;
   - título;
   - ordem;
   - existência.

4. Confirmar que existem exatamente 232 histórias.

5. Não renumerar.

6. Não reorganizar.

7. Não remover.

8. Não acrescentar.

9. Não inventar histórias.

10. Não substituir uma história por outra.

A sequência oficial deve ser preservada de 001 até 232.


[Regra Absoluta — Controle de Status]

Consultar:

`status-criacao-historia.md`

Antes de montar o PowerPoint.

Interpretar os estados:

PENDENTE
EM PRODUÇÃO
OK

O arquivo de status informa o estado de produção das imagens.

Se uma história estiver:

OK

procurar sua imagem correspondente.

Se uma história estiver:

PENDENTE

verificar se existe uma imagem correspondente disponível.

Se uma história estiver:

EM PRODUÇÃO

não assumir que a imagem está concluída.

Não considerar uma história concluída apenas porque existe um arquivo de imagem com nome semelhante.

A correspondência precisa ser validada.


[Regra Absoluta — NÃO REPETIR]

É PROIBIDO utilizar a mesma imagem em duas histórias diferentes.

Cada história deve possuir uma imagem correspondente própria.

Antes da criação do PowerPoint:

1. localizar todas as imagens;
2. identificar cada imagem;
3. associar imagem → história;
4. verificar duplicações;
5. verificar arquivos repetidos;
6. verificar nomes semelhantes;
7. verificar imagens visualmente ou por identificação quando necessário.

Sempre utilizar identificação inequívoca.

Quando possível, calcular SHA-256 ou outro hash do arquivo.

Exemplo:

historia-001.png → HASH A
historia-002.png → HASH B
historia-003.png → HASH C

Se:

historia-010.png → HASH A

então existe duplicação e o processo deve ser interrompido.

Não colocar a mesma imagem em dois slides apenas porque os nomes dos arquivos são diferentes.


[Regra — Correspondência Número + Título]

A associação deve considerar:

NÚMERO + TÍTULO

Exemplo:

historia-novo-testamento.md:

017. [Título oficial]

imagem:

017-[título correspondente].png

A imagem somente será considerada correta se houver evidência suficiente de que pertence à história 017.

Se houver:

017 → título A

mas a imagem estiver identificada como:

017 → título B

PARAR.

Não tentar corrigir silenciosamente.

Informar a inconsistência.


[Regra — Imagens]

O PowerPoint deve utilizar as imagens já produzidas para as histórias.

NÃO gerar uma nova imagem simplesmente para preencher uma lacuna.

Se uma imagem estiver faltando:

PARAR A MONTAGEM.

Informar:

- número da história;
- título;
- imagem esperada;
- motivo da ausência.

Não utilizar imagem de outra história como substituição.

Não utilizar imagem genérica.

Não duplicar outra imagem.

Não utilizar placeholder no arquivo final.


[Regra — Um Slide = Uma História]

Cada slide representa uma única história.

Exemplo:

SLIDE 001
→ História 001
→ Imagem 001

SLIDE 002
→ História 002
→ Imagem 002

...

SLIDE 232
→ História 232
→ Imagem 232

Nunca colocar duas histórias no mesmo slide.

Nunca colocar duas imagens de histórias diferentes no mesmo slide.

Nunca dividir uma história em vários slides no PowerPoint final.

Mesmo que a história original tenha várias cenas, o PowerPoint final deve possuir uma imagem representativa daquela história e apenas um slide para ela.


[Layout do PowerPoint]

Formato:

16:9 widescreen.

Dimensões PowerPoint:

13.333 × 7.5 polegadas.

Cada imagem deve ocupar o máximo possível do slide.

Preferência:

imagem em tela cheia.

Não utilizar:

- molduras desnecessárias;
- bordas brancas;
- caixas decorativas;
- sombras artificiais;
- grids;
- layouts corporativos;
- templates genéricos;
- elementos modernos que não pertençam ao projeto.

A apresentação deve parecer uma coleção visual de uma Bíblia infantil ilustrada.


[Imagem em Tela Cheia]

A imagem deve preencher todo o slide.

Utilizar:

FULL BLEED.

Não deixar espaços vazios desnecessários.

Não deformar a imagem.

Nunca alterar a proporção original.

Se a proporção da imagem for diferente da proporção do slide:

preferir CROP proporcional.

Nunca utilizar STRETCH que deforme personagens, objetos ou arquitetura.

Prioridade:

1. preservar proporção;
2. preservar personagens;
3. preservar conteúdo principal;
4. preencher o slide.


[Central Fold]

NÃO inserir dobra central.

NÃO desenhar linha vertical no meio do slide.

NÃO simular livro aberto.

Cada slide deve ser uma superfície visual contínua.


[Texto no Slide]

Por padrão, NÃO adicionar textos sobre a imagem.

A imagem deve ser a protagonista.

Se a própria imagem já possuir:

- título;
- número;
- balões;
- legendas;
- textos da história;

preservar esses elementos.

Não duplicar textos fora da imagem.

Não colocar um segundo título sobre um título que já esteja dentro da imagem.

Não inserir caixas de texto desnecessárias.


[Identificação Interna]

Mesmo que o slide visual não tenha texto adicional, manter internamente o controle:

SLIDE 001 → HISTÓRIA 001 → ARQUIVO DA IMAGEM

SLIDE 002 → HISTÓRIA 002 → ARQUIVO DA IMAGEM

...

SLIDE 232 → HISTÓRIA 232 → ARQUIVO DA IMAGEM

Se tecnicamente possível, utilizar o título oficial da história como propriedade/título interno do slide sem alterar visualmente o slide.

Isso serve para auditoria e manutenção.


[Qualidade Visual]

Todas as imagens devem preservar o padrão visual definido pelo projeto.

Manter:

- estilo infantil;
- estilo bíblico;
- qualidade cinematográfica;
- realismo estilizado;
- contexto histórico;
- anatomia correta;
- personagens consistentes;
- roupas coerentes;
- arquitetura coerente;
- iluminação coerente;
- estética de livro infantil ilustrado.

Não alterar as imagens desnecessariamente.

O PowerPoint é um recipiente editorial das imagens, não uma nova etapa de direção artística.


[CONTINUIDADE]

As 232 imagens fazem parte da mesma coleção.

Verificar, quando possível:

- coerência visual;
- proporções;
- qualidade;
- orientação;
- resolução;
- ausência de elementos modernos incompatíveis;
- ausência de imagens obviamente pertencentes a outra história.

Não substituir uma imagem apenas porque seu estilo visual é ligeiramente diferente.

Se existir uma inconsistência grave, registrar no relatório final.


[Controle de Qualidade — Pré-Montagem]

Antes de criar o `.pptx`, executar obrigatoriamente:

CHECK 01
Existem 232 histórias?

CHECK 02
A numeração vai de 001 até 232?

CHECK 03
Existem títulos para todas?

CHECK 04
Existem imagens correspondentes?

CHECK 05
Existe exatamente uma imagem por história?

CHECK 06
Existem imagens duplicadas?

CHECK 07
Existem arquivos ambíguos?

CHECK 08
Existe alguma história sem imagem?

CHECK 09
Existe alguma imagem sem história correspondente?

CHECK 10
Existe alguma divergência entre número e título?

CHECK 11
A sequência está correta?

Se qualquer um desses testes falhar:

NÃO GERAR O POWERPOINT FINAL.

Corrigir ou solicitar intervenção antes de continuar.


[Controle de Duplicidade]

Executar pelo menos dois níveis de verificação quando possível:

NÍVEL 1 — ARQUIVO

Comparar:

- SHA-256;
- tamanho;
- extensão;
- nome.

NÍVEL 2 — VISUAL

Quando houver arquivos diferentes que aparentem representar a mesma imagem:

comparar visualmente.

Uma duplicação visual também deve ser considerada problema, mesmo que os arquivos possuam hashes diferentes.


[Arquivos Extras]

Se existirem imagens que não correspondam a nenhuma das 232 histórias:

NÃO colocá-las no PowerPoint.

Listá-las no relatório:

ARQUIVOS NÃO UTILIZADOS

Não eliminar os arquivos.


[Arquivos Faltantes]

Se houver uma ou mais histórias sem imagem:

NÃO fabricar substituições.

Gerar relatório:

IMAGENS FALTANTES

Exemplo:

003 — Isabel descobre que está grávida
Imagem correspondente não encontrada.

027 — [Título]
Imagem correspondente não encontrada.

E interromper a montagem final.


[Validação do PowerPoint]

Depois de gerar o `.pptx`, abrir/reler o arquivo e validar:

1. número total de slides;
2. ordem dos slides;
3. existência de imagem em cada slide;
4. uma imagem por slide;
5. nenhuma duplicação;
6. correspondência número/imagem;
7. proporção;
8. ausência de imagem cortada de maneira inadequada;
9. ausência de slides vazios;
10. ausência de slides extras.

Resultado obrigatório:

232 slides.

Se o arquivo possuir:

231 → REPROVADO
233 → REPROVADO
232 → continuar validação


[Auditoria Final]

Produzir uma tabela de auditoria:

| Slide | História | Título | Imagem | Hash | Status |
|---:|---:|---|---|---|---|
| 001 | 001 | ... | ... | ... | OK |
| 002 | 002 | ... | ... | ... | OK |
| 003 | 003 | ... | ... | ... | OK |
| ... | ... | ... | ... | ... | ... |
| 232 | 232 | ... | ... | ... | OK |

Todos devem terminar como:

OK


[Regra de Falha]

Nunca mascarar problemas.

Se houver qualquer inconsistência:

PARAR.

Informar claramente:

TIPO DE PROBLEMA
HISTÓRIA AFETADA
ARQUIVO ENVOLVIDO
MOTIVO
AÇÃO NECESSÁRIA

Não continuar silenciosamente.


[Uso de Python]

Utilizar Python para criar o PowerPoint.

Utilizar obrigatoriamente:

`python-pptx`

quando disponível.

O código deve:

1. criar apresentação;
2. configurar formato 16:9;
3. criar 232 slides;
4. inserir cada imagem correspondente;
5. ajustar imagem preservando proporção;
6. aplicar crop quando necessário;
7. evitar deformação;
8. salvar o arquivo;
9. reabrir/validar o arquivo;
10. contar os slides;
11. gerar relatório de auditoria.


[Nome dos Arquivos]

Arquivo principal:

`Novo-Testamento-232-Historias.pptx`

Relatório:

`auditoria-powerpoint-232-historias.md`

Opcionalmente:

`auditoria-powerpoint-232-historias.csv`

Se forem utilizados arquivos temporários, mantê-los separados do arquivo final.


[Critérios de Aprovação]

O PowerPoint somente será considerado APROVADO se:

- possuir exatamente 232 slides;
- possuir uma história por slide;
- possuir uma imagem por slide;
- respeitar a ordem 001 → 232;
- não possuir histórias repetidas;
- não possuir imagens repetidas;
- não possuir histórias faltantes;
- não possuir imagens faltantes;
- não possuir associação número/título incorreta;
- não possuir slides vazios;
- não possuir slides extras;
- não deformar as imagens;
- utilizar formato 16:9;
- preservar o padrão visual do projeto.


[Saída]

Se tudo estiver correto:

1. gerar:

`Novo-Testamento-232-Historias.pptx`

2. gerar:

`auditoria-powerpoint-232-historias.md`

3. validar os arquivos.

4. apresentar:

POWERPOINT GERADO

Arquivo:
Novo-Testamento-232-Historias.pptx

Slides:
232/232

Histórias:
232/232

Imagens:
232/232

Duplicações:
0

Faltantes:
0

Inconsistências:
0

Status:
APROVADO


[Se houver erro]

NÃO gerar um PowerPoint apresentado como final.

Apresentar:

STATUS: BLOQUEADO

e listar todos os problemas encontrados.

Nunca afirmar que o PowerPoint está completo quando houver qualquer falha.


[Fluxo Obrigatório]

Executar exatamente nesta ordem:

ETAPA 1
Ler `historia-novo-testamento.md`.

ETAPA 2
Extrair e validar as 232 histórias.

ETAPA 3
Ler `status-criacao-historia.md`.

ETAPA 4
Localizar todas as imagens disponíveis.

ETAPA 5
Construir a tabela:

história → título → imagem → arquivo → hash

ETAPA 6
Executar controle de duplicidade.

ETAPA 7
Executar controle de correspondência.

ETAPA 8
Executar controle de faltantes.

ETAPA 9
Se houver problema:
PARAR.

ETAPA 10
Se estiver tudo correto:
criar o PowerPoint.

ETAPA 11
Validar o PowerPoint gerado.

ETAPA 12
Gerar relatório de auditoria.

ETAPA 13
Entregar o `.pptx` e o relatório.


[RESTRIÇÕES ABSOLUTAS]

NÃO criar menos de 232 slides.

NÃO criar mais de 232 slides.

NÃO duplicar histórias.

NÃO duplicar imagens.

NÃO trocar imagens entre histórias.

NÃO inventar imagens faltantes.

NÃO utilizar imagens genéricas.

NÃO alterar a sequência.

NÃO renumerar histórias.

NÃO ignorar `historia-novo-testamento.md`.

NÃO ignorar `status-criacao-historia.md`.

NÃO confiar somente na memória da conversa.

NÃO gerar um PowerPoint parcial e apresentá-lo como final.

NÃO ocultar inconsistências.

NÃO esticar imagens.

NÃO inserir templates corporativos.

NÃO inserir elementos modernos desnecessários.

NÃO criar uma dobra central.

NÃO transformar o projeto em uma apresentação empresarial.

NÃO modificar o conteúdo bíblico.

NÃO substituir uma imagem por outra apenas para completar 232 slides.


[REGRA FINAL]

A fonte oficial determina:

O QUE É CADA HISTÓRIA.

O status determina:

QUAL HISTÓRIA POSSUI PRODUÇÃO CONCLUÍDA.

A imagem determina:

QUAL É A REPRESENTAÇÃO VISUAL DA HISTÓRIA.

O PowerPoint determina:

COMO AS 232 HISTÓRIAS SÃO ORGANIZADAS EM 232 SLIDES.

A regra fundamental é:

001 → 001
002 → 002
003 → 003
...
232 → 232

SEM REPETIÇÃO.

SEM OMISSÃO.

SEM TROCA.

SEM INVENÇÃO.

O arquivo somente pode ser considerado concluído quando:

232 histórias
=
232 imagens
=
232 slides

e todas as correspondências forem validadas.