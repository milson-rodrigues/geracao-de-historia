# 00_GUIA-DE-CONFIGURACAO.md — guia operacional mutável

**Função:** concentrar o fluxo operacional vigente para produção de histórias em quadrinhos, mockups e sprites neste repositório.

**Repositório canônico:** `milson-rodrigues/geracao-de-historia`, branch `main`.

**Ponto de entrada estável:** [ROUTER-MESTRE.md](ROUTER-MESTRE.md). Este guia é a fonte operacional mutável. Atualizações de processo devem ocorrer aqui ou nos documentos especializados, nunca no roteador mestre durante manutenção rotineira.

## 1. Regra de consulta obrigatória

Toda solicitação de produção começa pela consulta direta ao GitHub, branch `main`. Repetir a consulta a cada nova solicitação; memória, conversas anteriores, cópias locais e instruções antigas não substituem os arquivos atuais.

Se o GitHub, a fonte narrativa, o template ou outra dependência essencial estiver inacessível, interromper a produção e informar o bloqueio. Não gerar por suposição nem preencher lacunas com memória.

## 2. Ordem de consulta

Para cada produção:

1. Ler este guia atualizado no GitHub.
2. Consultar a árvore atual do repositório e ler [README.md](README.md) quando necessário para entender a estrutura.
3. Ler [templates/CATALOGO.md](templates/CATALOGO.md) e confirmar que o Template ID existe e corresponde ao tipo de ativo.
4. Ler o arquivo exato do template selecionado. Para mockup universal, consultar [templates/mockup-template.md](templates/mockup-template.md), Template ID `TPL-MOCKUP-UNIVERSAL`.
5. Localizar e ler integralmente a fonte narrativa oficial em `historias/` ou o roteiro fornecido pelo usuário. Confirmar número, título, coleção, referência bíblica, personagens, fatos e sequência.
6. Consultar o manifesto de status aplicável à coleção, quando existir, e verificar o identificador exato para evitar repetição.
7. Ler as regras especializadas aplicáveis:
   - [regras/00-LEIA-PRIMEIRO.md](regras/00-LEIA-PRIMEIRO.md) — ponte de compatibilidade/entrada legada;
   - [regras/ROTA-GERAL.md](regras/ROTA-GERAL.md);
   - [regras/SKILLS-E-RECURSOS.md](regras/SKILLS-E-RECURSOS.md);
   - [regras/PADRAO-VISUAL-E-COMPOSICAO.md](regras/PADRAO-VISUAL-E-COMPOSICAO.md);
   - [regras/VALIDACAO-FINAL.md](regras/VALIDACAO-FINAL.md).
8. Identificar e utilizar prioritariamente a ferramenta nativa de geração de imagens disponibilizada pelo próprio GPT personalizado que está executando o fluxo. Não exigir Higgsfield, CLI externa, integração ou credenciais de terceiros como pré-condição quando a ferramenta nativa estiver disponível. Consultar skills externas somente como referências complementares, se pertinentes.
9. Aplicar os requisitos específicos do template, gerar e validar o ativo.
10. Atualizar somente registros textuais de status quando houver mudança real, autorização e acesso de escrita. Reabrir o arquivo e confirmar a gravação.

Não ler o repositório inteiro por padrão. Consultar apenas os arquivos exigidos pelo fluxo e suas dependências.

## 3. Identificação e prevenção de duplicidade

- Não inventar Template IDs. Se o ID não existir no catálogo ou não corresponder ao ativo solicitado, parar e informar.
- Identificar a história pelo número/ID e título oficial na fonte narrativa; não usar apenas semelhança de título.
- Consultar o manifesto da coleção antes de gerar.
- Se a história já estiver registrada como gerada, validada ou aprovada, não gerar novamente sem solicitação explícita de nova versão.
- Manifesto ausente, vazio ou incompleto significa histórico desconhecido; não prova que a história nunca foi produzida.
- Se o histórico for desconhecido e a prevenção de repetição for material, esclarecer com o usuário antes de prosseguir.

## 4. Autoridade das fontes

1. **Fonte narrativa canônica:** fatos, personagens, acontecimentos, referência e sequência.
2. **Template selecionado:** tipo de ativo, contexto, composição e requisitos específicos.
3. **Regras do projeto:** qualidade, idioma, integridade e validação.
4. **Skills/documentação de ferramentas:** execução técnica; não podem contradizer as fontes anteriores.
5. **Manifesto de status:** estado de produção confirmado; não é fonte narrativa.

Se o usuário fornecer um roteiro, ele pode ser usado como fonte da tarefa. Não substituir silenciosamente a fonte canônica; sinalizar divergências relevantes.

## 5. Requisitos editoriais para histórias bíblicas infantis

Para cada história bíblica destinada a crianças:

- Incluir pelo menos **três perguntas** específicas dos fatos e ensinamentos da história. Variar entre compreensão, reflexão e aplicação; não repetir perguntas genéricas mecanicamente.
- Incluir uma **oração desenvolvida**, normalmente com 4 a 7 frases, em linguagem infantil e relacionada à narrativa.
- A oração deve terminar exatamente com **“Em nome de Jesus, Amém!”**.
- Não remover perguntas nem encurtar a oração para acomodar a imagem. Reorganizar a composição ou apresentar o conteúdo completo junto da imagem.

## 6. Imagens, armazenamento e quantidade

- Imagens finais geradas devem permanecer fora do GitHub. Não fazer upload, commit ou armazenamento de imagens no repositório.
- O GitHub mantém fontes narrativas, templates, regras e registros textuais autorizados.
- Uma imagem exibida no chat não prova que foi salva em outro destino.
- Uma solicitação de ativo final corresponde a uma única geração final, quantidade 1 quando suportada. Não criar lotes ou variações, salvo pedido explícito.
- Não sobrescrever ativo aprovado sem autorização.
- Não afirmar salvamento, caminho, resolução ou aprovação sem evidência verificável.

## 7. Proporção e qualidade

- Padrão: horizontal 16:9, mínimo raster de 1920 × 1080.
- Vertical 9:16 somente quando solicitado explicitamente, mínimo raster de 1080 × 1920.
- Preferir resolução nativa maior quando a ferramenta suportar e for adequada.
- Conferir dimensões reais do arquivo final; não inferir resolução pela aparência.
- Seguir a composição e as exceções definidas no template específico. Não impor layout fixo de uma prancha a sprites ou outros ativos.

## 8. Skills e ferramentas

- **Ferramenta principal:** ferramenta nativa de geração de imagens do GPT personalizado “Gerar imagem bíblica”, quando disponível na sessão. Ela é o mecanismo de execução esperado para produzir a prancha diretamente no ChatGPT.
- Higgsfield não é ferramenta obrigatória nem dependência do fluxo. Não bloquear a geração porque Higgsfield, sua CLI, integração ou credenciais não estão disponíveis.
- Só utilizar Higgsfield se o usuário solicitar explicitamente essa ferramenta e ela estiver realmente disponível.
- Skills e bibliotecas externas (incluindo Higgsfield e GPT Image 2 Prompt Library) são referências complementares de técnica e direção visual; não substituem nem condicionam a ferramenta nativa do GPT.
- Consultar [awesome-gpt-image-2](https://github.com/freestylefly/awesome-gpt-image-2) como complemento de direção artística e estruturação de prompts, quando relevante.
- Taste Skill e Open Design são complementares/opcionais, conforme [regras/SKILLS-E-RECURSOS.md](regras/SKILLS-E-RECURSOS.md).
- Documentação pública ou presença de arquivos não prova que CLI, integração, credenciais ou ferramenta estejam operacionais.
- Declarar somente a ferramenta e o método realmente utilizados. Se a ferramenta nativa do GPT gerar a imagem, identificá-la como ferramenta de geração de imagens do próprio GPT; nunca atribuir a geração ao Higgsfield.

## 9. Validação

Aplicar [regras/VALIDACAO-FINAL.md](regras/VALIDACAO-FINAL.md) e os critérios do template. Verificar, conforme o ativo:

- fidelidade à fonte e sequência narrativa;
- contexto, personagens e continuidade;
- composição, silhueta, anatomia e legibilidade;
- balões, caixas de narração e ordem de leitura;
- ortografia, acentuação, pontuação e naturalidade em pt-BR;
- perguntas e oração completas, quando aplicáveis;
- dimensões e proporção reais;
- ausência de falhas críticas.

Geração não equivale a aprovação. Usar os estados definidos na regra de validação e não marcar como aprovado sem inspeção real.

## 10. Status, persistência e relatório

Atualizar o manifesto textual da coleção somente quando o estado mudar de fato, houver autorização e o acesso de escrita estiver disponível. Registrar apenas fatos confirmados. Depois da gravação, reler o arquivo e confirmar conteúdo, caminho e commit.

O relatório final deve informar, conforme aplicável: Template ID/versão, título/elemento e coleção, fontes consultadas, skill/documentação consultada, ferramenta realmente utilizada, parâmetros e quantidade, validação, caminho real do arquivo se salvo fora do GitHub, alteração de status confirmada e pendências.

## 11. Manutenção deste guia

Este é o documento mutável de configuração operacional. Atualize-o quando o fluxo, a ordem de consulta, o roteamento de ferramentas ou as regras transversais mudarem. Atualize também os documentos especializados afetados e verifique consistência dos links.

**Não altere o `ROUTER-MESTRE.md` para mudanças operacionais comuns.** Ele permanece como bootstrap estável e aponta para este guia.


## 12. Gate de confirmação e proibição de prévia antecipada

**Toda solicitação de criação de história bíblica neste projeto significa produzir uma prancha em quadrinhos.** Esse formato é padrão fixo e não deve ser questionado nem comparado com a opção de ilustração única.

Nenhuma imagem deve ser gerada, pesquisada ou exibida como prévia antes de concluir as verificações obrigatórias.

1. Primeiro, concluir a consulta ao GitHub, a leitura das fontes, a identificação do template, a verificação do manifesto e a preparação do conteúdo.
2. Não perguntar se o usuário deseja prancha em quadrinhos ou ilustração única: para histórias, a saída é sempre uma prancha em quadrinhos. Perguntar somente sobre lacunas realmente não definidas que alterem materialmente a prancha (por exemplo, proporção diferente do padrão ou requisitos especiais). Pedidos explícitos de sprites seguem o template de sprite correspondente e podem exigir esclarecimentos próprios.
3. Enquanto aguarda confirmação, não chamar ferramenta de geração de imagem, não pesquisar imagens para ilustrar a resposta e não exibir imagens de referência como se fossem prévias do resultado.
4. Não produzir uma imagem demonstrativa para tentar explicar a diferença entre opções. Descrever as opções em texto.
5. Quando o pedido e o template já definirem inequivocamente a saída, não pedir confirmação redundante: seguir diretamente para a única geração final autorizada.
6. Depois da confirmação (quando necessária), fazer uma única chamada de geração destinada ao ativo final, com quantidade 1 quando suportada. Não gerar rascunhos, thumbnails, testes visuais ou variações intermediárias.
7. Imagens externas só podem ser pesquisadas/exibidas quando o usuário pedir explicitamente referências visuais ou pesquisa de imagens. Identificá-las claramente como referências externas, com origem; nunca apresentá-las como resultado gerado.
8. Não usar imagens com marcas d'água ou de terceiros como se fossem ativos produzidos pelo projeto. A presença de uma imagem na resposta não comprova geração, validação ou salvamento.

A sequência obrigatória para histórias é: **consulta e validação das fontes → preparar a prancha em quadrinhos e seu conteúdo → esclarecer apenas requisitos especiais não definidos → uma geração final → inspeção e validação → registro textual de status autorizado**.


## 13. Referência visual canônica da prancha

A referência visual fornecida pelo usuário nesta conversa define a apresentação esperada das pranchas bíblicas. A especificação reproduzível está em `templates/mockup-template.md`, seção 13, e em `regras/PADRAO-VISUAL-E-COMPOSICAO.md`.

Resumo obrigatório: canvas 16:9 sem interface externa; cabeçalho de pergaminho com número/título/referência; seis quadros em grade 3×2, cada um com narração legível; três painéis pedagógicos inferiores alinhados (O QUE APRENDEMOS, PERGUNTAS PARA A CRIANÇA, ORAÇÃO), com cabeçalhos coloridos e ícones; acabamento de quadrinhos/graphic novel com cenários coerentes, iluminação cinematográfica, paleta natural expressiva e continuidade de personagens.

A imagem de referência determina somente o estilo e a composição. Não copiar o conteúdo da história que aparece nela. A narrativa oficial do GitHub determina integralmente os fatos, personagens e sequência.

**A coleção Antigo Testamento também segue este padrão visual de produção.** A nota editorial da fonte narrativa é contextual e não deve ser interpretada como bloqueio à produção de pranchas solicitadas pelo usuário; a política operacional de produção está neste guia.


## 14. Proibição de imagens soltas e de resultados substitutos

Em uma solicitação de história bíblica, **não gerar, buscar, anexar ou exibir imagens isoladas de cenas, paisagens, personagens ou referências visuais como resposta parcial**. O usuário solicitou uma prancha completa, não imagens avulsas.

- Não usar pesquisa de imagens, resultados de sites, imagens de bancos externos, miniaturas, galerias ou componentes de imagem para ilustrar a resposta.
- Não produzir uma imagem de criação mundial, céu, mar, personagem ou qualquer cena individual como substituto de uma prancha.
- Não exibir duas ou mais imagens independentes para sugerir que a prancha foi produzida.
- A única saída visual autorizada para uma solicitação de história é **uma única imagem final contendo a prancha completa**, com cabeçalho, seis quadros e os três painéis pedagógicos definidos no template.
- A geração deve ser feita pela ferramenta nativa de geração de imagens do próprio GPT personalizado. Não substituir essa chamada por pesquisa web, imagens externas, SVG demonstrativo ou descrição textual acompanhada de imagens.
- Se a ferramenta nativa não estiver disponível ou falhar, informar claramente que a prancha não foi gerada. Não preencher a resposta com imagens ilustrativas, resultados externos ou prévias.
- Texto de preparação, fontes e validação podem ser apresentados sem imagens enquanto a geração não ocorrer.
- Não declarar que houve geração se a ferramenta não retornou a prancha completa.

**Critério de saída:** zero imagens isoladas + uma única prancha completa. Qualquer saída visual diferente disso é falha de execução e não pode ser registrada como geração concluída.


## 15. Expansão arquitetural — AI Creative Hub

O repositório passa a documentar uma arquitetura-alvo multimodal denominada **AI Creative Hub**, sem renomear o repositório GitHub nesta etapa. O escopo de domínio contempla Image, Comic, Video, Voice, Audio e Sprite.

Documentos de referência:
- [Arquitetura AI Creative Hub](docs/AI-CREATIVE-HUB-ARCHITECTURE.md)
- [Índice de comandos](commands/COMMAND-INDEX.md)
- [Manual de comandos](commands/COMMAND-MANUAL.md)
- [Contrato do Command Router](commands/COMMAND-CONTRACT.md)
- [Registro de skills](external/SKILL-REGISTRY.md)

O fluxo de histórias bíblicas permanece especializado na Comic Bridge e continua sujeito ao template, fontes, manifesto e regras deste guia. A expansão multimídia não altera retroativamente esses requisitos.

## 16. Comandos, bridges e skills

Os comandos documentados são uma interface conversacional especificada, não comandos slash já registrados em um host. Não declarar que um comando é executável até existir parser/dispatcher integrado e testes de integração.

Separação obrigatória:
- **Command:** intenção solicitada pelo usuário.
- **Bridge:** domínio responsável pela operação.
- **Workflow:** sequência de etapas.
- **Skill:** conhecimento/instruções especializadas carregadas sob demanda.
- **Provider/Adapter:** ferramenta externa ou nativa que efetivamente executa a operação.

A pasta `.agents/skills/` já contém skills locais. Não duplicar essas pastas em `skills/`. Usar `external/SKILL-REGISTRY.md` para registrar procedência, versão, licença, compatibilidade e estratégia (INTERNAL, ADAPTED ou REFERENCE). Skills externas só podem ser copiadas/adaptadas após auditoria de licença, dependências, scripts, permissões e segurança.

Não presumir que a presença de uma skill local prova instalação, autenticação ou disponibilidade de provider. Consultar a fonte oficial e validar o contrato técnico quando a tarefa exigir.

## 17. Política de providers por domínio

A seleção de provider deve ser baseada em capacidade, schema atual, disponibilidade, entradas, saída exigida, política e custo conhecido. Não fixar um provider no nome do comando.

- Image, Video e Audio podem avaliar adapters documentados na skill Higgsfield Generate, após validação operacional.
- Voice exige homologação específica de TTS/dublagem; a skill Higgsfield Generate local declara que não atende TTS.
- Sprite exige validação de dimensões, transparência, frames e formato de exportação.
- Comic orquestra narrativa, storyboard, imagens e QA; não é sinônimo de um gerador de imagem.

As regras específicas do fluxo bíblico continuam prevalecendo sobre defaults genéricos de providers e skills.
