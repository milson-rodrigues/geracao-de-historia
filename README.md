# Estudo Bíblico — 232 histórias ilustradas do Novo Testamento

Projeto para produzir uma coleção de pranchas bíblicas infantis com narrativa fiel à fonte oficial, identidade visual consistente, validação editorial e controle explícito de progresso.

> **Regra central:** uma história solicitada = uma única prancha final. O conteúdo vem da história correspondente na fonte oficial; as imagens aprovadas anteriores servem como referência visual, não como fonte narrativa.

## Início rápido

No ChatGPT, dentro do projeto **Estudo Bíblico**, o comando normal é:

```text
Gere a História 003
```

A rota do projeto deve fazer o restante: consultar a versão atual dos arquivos na branch `main` por acesso GitHub autenticado, verificar o status, localizar a história exata, preparar e validar o roteiro de seis legendas, aplicar as instruções visuais, gerar e validar a imagem e só então registrar o resultado. Como o repositório é privado, se o ambiente não tiver acesso autenticado, a geração deve parar com aviso de permissão; apenas incluir o link não concede acesso.

Para uma história que já esteja concluída, use um pedido explícito de regeneração, por exemplo:

```text
Gere novamente a História 003
```

Se a rota detectar que a história já está concluída, deve confirmar a intenção antes de gerar outra imagem. Não sobrescreva uma imagem aprovada sem autorização.

**Atenção:** a instrução textual não garante, sozinha, que uma ferramenta de imagem produza apenas um arquivo. Configure a quantidade como `1` quando a ferramenta permitir, não faça chamadas paralelas nem solicite variações. Se a ferramenta não permitir controlar a quantidade, declare a limitação.

## A memória durável do projeto

Neste projeto, a “memória de criação” não deve depender apenas do histórico da conversa ou da memória interna de um modelo. A memória durável é formada pelos arquivos versionados no GitHub e pelos ativos visuais aprovados.

| Elemento de memória | Arquivo ou local | Para que serve |
|---|---|---|
| Memória narrativa | `historia-novo-testamento.md` | Define o número, o título, os personagens e os acontecimentos de cada história. É a fonte narrativa oficial e não deve ser alterada durante a geração de imagens. |
| Memória de progresso | `status-criacao-historia.md` | Registra o estado de produção, o caminho da imagem e o estado de validação. Deve ser consultado antes de toda geração. |
| Memória de procedimento | `ROTA-SKILLS-ESTUDO-BIBLICO.md` | Define a ordem de execução, os bloqueios, as regras de salvamento e o tratamento de falhas. |
| Memória de direção visual | `prompt-geracao-imagem.md` | Define a composição, o estilo, os painéis pedagógicos e os critérios de validação. |
| Memória visual aprovada | `imagens/001-mundo-antes-do-nascimento-de-jesus.png` e `imagens/002-anjo-gabriel-aparece-a-zacarias.png` | Preserva o padrão visual de referência. Consultar as imagens quando estiverem acessíveis. |
| Memória de alterações | Histórico de commits do GitHub | Permite rastrear mudanças nos arquivos e recuperar versões anteriores. |

### Como utilizar essa memória corretamente

1. **Leia a fonte atual a cada execução.** Não use apenas o que o modelo lembra de outra conversa, história ou sessão.
2. **Leia o status atual na branch `main`.** O status determina se a geração pode iniciar.
3. **Bloqueie a identidade narrativa.** Fixe o número, título e conteúdo da entrada exata antes de gerar. Não misture cenas, legendas, orações ou ensinamentos de outra história.
4. **Use as imagens anteriores somente para identidade visual.** Elas orientam composição, paleta, molduras e continuidade dos personagens; não autorizam copiar suas narrativas.
5. **Registre o resultado no arquivo de progresso.** A execução seguinte deve consultar a linha atualizada, não inferir o resultado pelo histórico do chat.
6. **Se o GitHub não estiver acessível, informe a limitação.** Não presuma que uma cópia local ou da Biblioteca do ChatGPT está atualizada.
7. **Mantenha uma fonte oficial.** O GitHub é a fonte versionada oficial. A Biblioteca do ChatGPT pode ser usada como apoio visual ou cópia de trabalho, mas não deve divergir silenciosamente do repositório.

A memória do projeto só é confiável quando o registro corresponde ao que realmente foi gerado, validado e salvo. Não marque uma imagem como concluída com base apenas na geração ou na exibição no chat.

## Arquivos principais

- [`historia-novo-testamento.md`](historia-novo-testamento.md) — fonte narrativa das 232 histórias.
- [`status-criacao-historia.md`](status-criacao-historia.md) — controle de produção e validação.
- [`ROTA-SKILLS-ESTUDO-BIBLICO.md`](ROTA-SKILLS-ESTUDO-BIBLICO.md) — roteador operacional.
- [`prompt-geracao-imagem.md`](prompt-geracao-imagem.md) — instruções do gerador e controlador de imagens.
- [`imagens/`](imagens/) — imagens finais e referências visuais aprovadas.


## Roteamento de skills e recursos visuais

A rota do projeto define quando consultar cada recurso. Os links abaixo são repositórios de referência; a existência de um link não comprova que a skill esteja instalada nem que tenha sido executada.

1. **Principal para geração de imagens — [`higgsfield-generate`](https://github.com/higgsfield-ai/skills/blob/main/higgsfield-generate/SKILL.md).** Consultar suas instruções atuais para geração/edição de imagem quando a skill e a ferramenta associada estiverem disponíveis. Solicitar uma única imagem por chamada, configurando quantidade `1` quando suportada.
2. **Complementar para direção artística — [`taste-skill`](https://github.com/Leonxlnx/taste-skill).** Consultar seletivamente para referências, hierarquia visual e avaliação de estilo, sem contrariar as referências aprovadas nem o prompt oficial do projeto.
3. **Opcional para exploração visual — [`open-design`](https://github.com/nexu-io/open-design).** Considerar apenas para tarefas específicas de exploração, organização ou discussão de referências visuais, quando disponível. Não é requisito para cada geração e não substitui a ferramenta de imagem.

Consulte a [rota operacional](ROTA-SKILLS-ESTUDO-BIBLICO.md) antes de decidir qual recurso usar. Nunca declare uma skill instalada, consultada ou executada sem evidência. A narrativa oficial, o padrão visual do projeto e a regra de uma única imagem final têm prioridade sobre qualquer orientação externa.

## Fluxo de produção por história

Antes de agir, a execução precisa conseguir ler a branch `main` por acesso GitHub autenticado. O repositório pode ser privado; citar ou abrir um link sem recuperar o conteúdo atual não é consulta. Se não houver acesso autorizado, o agente deve informar o bloqueio e não alegar que validou a fonte.

1. Identificar exatamente o número solicitado.
2. Ler a entrada completa em `historia-novo-testamento.md` e confirmar título e tópicos.
3. Consultar `status-criacao-historia.md` e conferir número/título.
4. Interpretar o comando:
   - `Gere a História NNN`: iniciar diretamente quando estiver `PENDENTE`, inclusive após uma tentativa reprovada e excluída.
   - `Gere novamente a História NNN`: autorização explícita para regenerar; não perguntar novamente se o usuário deseja.
   - Se estiver `CONCLUIDA`, o comando simples exige confirmação antes de substituir a imagem aprovada.
5. Se não houver linha no status, conferir a história e o caminho canônico. Se a história existir e o arquivo final também estiver ausente, criar apenas a linha daquela história como `PENDENTE | — | validacao: NÃO_INICIADA` e prosseguir. Se houver arquivo sem registro, reconciliar antes de sobrescrever.
6. Isolar somente a entrada da história solicitada até o próximo título de história. Preparar um roteiro antes da geração: título oficial literal, seis legendas narrativas numeradas, descrição visual de cada quadro e lista de conteúdo proibido das histórias vizinhas. Conferir o roteiro contra a fonte oficial.
7. Gerar uma única prancha em uma única chamada, usando quantidade `1` quando houver parâmetro. Não pedir alternativas nem fazer chamadas paralelas.
8. Validar número, título literal, fidelidade narrativa, seis legendas, três painéis pedagógicos, ortografia, legibilidade e consistência visual. Se aparecer conteúdo de outra história, rejeitar, corrigir o prompt e repetir sequencialmente, uma imagem por tentativa, até duas tentativas corrigidas.
9. Salvar com o nome canônico e confirmar o arquivo. Não declarar que a imagem foi salva se apenas apareceu no chat.
10. Atualizar uma única linha do status conforme o resultado real. Uma imagem reprovada que foi excluída volta para `PENDENTE` com validação `NÃO_INICIADA`; uma reprovação anterior não bloqueia indefinidamente uma nova tentativa.
11. Marcar `CONCLUIDA` / `APROVADA` apenas quando a imagem correta estiver validada, salva e o status tiver sido atualizado com sucesso.

**Regra específica da História 003:** o título literal é “Isabel descobre que está grávida”. Não usar acontecimentos da História 004 (“O anjo Gabriel aparece a Maria”), incluindo a anunciação a Maria, Gabriel, Nazaré nesse contexto, Filho do Altíssimo ou trono de Davi. Se o gerador devolver esses elementos, rejeitar a imagem e corrigir o prompt antes de nova tentativa.

## Padrão da imagem final

Cada prancha deve seguir as instruções completas em `ROTA-SKILLS-ESTUDO-BIBLICO.md` e `prompt-geracao-imagem.md`. O padrão visual inclui:

- formato horizontal, próximo de 16:9;
- ilustração bíblica infantil colorida, detalhada e acolhedora;
- cabeçalho com número e título oficiais;
- exatamente seis quadros narrativos, organizados em duas fileiras de três;
- cada quadro contém uma ilustração e uma legenda narrativa curta, integrada e legível; a numeração não substitui a legenda;
- todas as seis legendas devem corresponder à história oficial e não acrescentar fatos sem sustentação;
- três painéis inferiores com os títulos exatos **O QUE APRENDEMOS**, **PERGUNTAS PARA A CRIANÇA** e **ORAÇÃO**;
- texto em português brasileiro, apropriado para crianças e revisado;
- continuidade visual de personagens recorrentes, quando aplicável;
- contexto histórico coerente, sem contradizer ou ampliar indevidamente a narrativa oficial.

A composição deve integrar todos os quadros e painéis em uma única imagem. Não produzir uma imagem independente por quadro.

## Nome e local do arquivo

O nome oficial segue o formato:

```text
NNN-slug-do-titulo-oficial.png
```

Exemplo de nome confirmado:

```text
001-mundo-antes-do-nascimento-de-jesus.png
```

Para uma nova história, copie o título da fonte oficial e gere o slug a partir dele: minúsculas, sem acentos ou pontuação e com palavras separadas por hífen. O destino oficial no repositório é `imagens/`.

Não salvar alternativas, prévias ou versões duplicadas na pasta oficial. Não apagar nem sobrescrever arquivos aprovados sem autorização.

## Critérios de validação

Antes de marcar como `CONCLUIDA`, confirme:

- número e título correspondem à fonte narrativa;
- todos os acontecimentos representados pertencem à história atual e respeitam sua sequência;
- não há mistura de histórias;
- os seis quadros narrativos e os três painéis pedagógicos estão presentes;
- cada um dos seis quadros contém legenda narrativa legível, além da ilustração e do número;
- as legendas correspondem à fonte oficial e não misturam histórias;
- os três títulos pedagógicos estão corretos;
- textos relevantes são legíveis e ortograficamente adequados;
- personagens e estilo estão consistentes;
- existe um único arquivo final com nome e caminho canônicos;
- o salvamento foi confirmado;
- a linha correspondente do relatório foi atualizada com sucesso.

Se a imagem foi gerada, mas ainda aguarda validação, use `GERADA_A_VALIDAR` com validação pendente. Se houver erro que impeça a continuação, use `BLOQUEADA` e registre o motivo. Nunca declare conclusão sem evidência.

## Formato do relatório de progresso

Cada história deve ocupar uma única linha, no formato:

```text
NNN | Título oficial | ESTADO | caminho/arquivo.png ou — | validacao: VALOR
```

Estados oficiais: `PENDENTE`, `EM_GERACAO`, `GERADA_A_VALIDAR`, `CONCLUIDA`, `BLOQUEADA`.

Valores de validação: `NÃO_INICIADA`, `PENDENTE`, `APROVADA`, `REPROVADA`.

Mantenha uma linha por número, preserve a ordem e altere somente o registro da história em processamento. Se houver divergências no status, não as corrija silenciosamente; informe o problema.

## Situação registrada atualmente

Na versão consultada para a criação deste README:

- História 001 — **CONCLUIDA / APROVADA**
- História 002 — **CONCLUIDA / APROVADA**
- História 003 — **PENDENTE / NÃO_INICIADA** — *Isabel descobre que está grávida*

O arquivo de status atualmente contém os registros 001, 002 e 003. Para histórias posteriores sem linha, não é necessário criar todo o relatório em lote: quando o usuário solicitar explicitamente um número, a rota confirma o título na fonte e verifica se já existe uma imagem no caminho canônico; se não existir imagem, cria apenas a linha daquela história como `PENDENTE` e continua. Se houver uma imagem não registrada, a execução para para reconciliar antes de sobrescrever. Este resumo é uma fotografia do estado atual; consulte sempre o status na branch `main` antes de agir.

## Comandos recomendados

| Objetivo | Comando |
|---|---|
| Gerar ou tentar novamente uma história `PENDENTE` (incluindo tentativa anterior reprovada e descartada) | `Gere a História 003` |
| Regenerar explicitamente uma história, inclusive concluída | `Gere novamente a História 003` |
| Verificar o estado sem gerar | `Verifique o status da História 003` |
| Diagnosticar bloqueios do projeto | `Diagnostique o fluxo de geração do projeto Estudo Bíblico, sem gerar imagens` |

Os comandos são exemplos. A rota consulta a fonte e o status na branch `main` em cada execução. Uma reprovação anterior não bloqueia uma nova tentativa quando a imagem foi descartada e o estado é `PENDENTE`. `Gere novamente a História NNN` é autorização explícita e não deve gerar uma segunda pergunta de confirmação. O número no comando não substitui a consulta aos arquivos.

## Uso em ChatGPT, Codex, Claude e Antigravity

Para manter o mesmo comportamento entre ambientes:

1. Disponibilize o repositório e os arquivos atuais ao agente.
2. Configure as instruções do projeto para tratar `ROTA-SKILLS-ESTUDO-BIBLICO.md` como roteador operacional e `prompt-geracao-imagem.md` como especificação visual.
3. Oriente o agente a consultar a branch `main` em cada execução, em vez de confiar em memória de conversa ou cópias antigas.
4. Confirme que o ambiente consegue ler arquivos, consultar imagens de referência, gerar imagens e salvar/atualizar os arquivos necessários.
5. Se alguma capacidade estiver ausente, peça que o agente informe o bloqueio, sem alegar que salvou ou sincronizou arquivos.

As instruções em Markdown não concedem permissões nem criam integração automática. Cada ambiente precisa ter acesso real ao GitHub, às referências e às ferramentas de geração/salvamento.

## Princípio final

**A fonte narrativa define o que contar; as referências aprovadas definem como ilustrar; o status define se a geração pode começar; a validação define se o resultado pode ser considerado concluído.**

Uma história = uma identidade narrativa bloqueada = um roteiro explícito enviado ao gerador = uma imagem final validada = uma linha de progresso.
