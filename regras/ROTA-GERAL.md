# Rota geral — produção por templates

**Versão:** 2.0.0  
**Idioma:** português brasileiro  
**Fonte:** branch `main` do repositório `milson-rodrigues/geracao-de-historia`.

## 1. Objetivo

Organizar a geração de imagens e sprites por Template ID. Cada template define coleção, fonte narrativa, contexto, ativo pretendido, etapas, restrições e validação. Esta rota distribui o trabalho entre template, regras globais e skills; não substitui o conteúdo dos templates.

## 2. Entrada do fluxo

O usuário deve informar, no mínimo, o Template ID e o título/nome do que será produzido. Exemplos:

```text
Gerar com template TPL-HNT-HISTORIA
Título: O anjo Gabriel aparece a Maria
```

```text
Gerar com template TPL-HNT-SPRITE
Elemento: Maria — sprite individual
História de origem: O anjo Gabriel aparece a Maria
```

Consulte primeiro [templates/CATALOGO.md](../templates/CATALOGO.md). No catálogo atual, o único template disponível é `TPL-MOCKUP-HISTORIA`, apontando para `templates/mockup-template.md`; os IDs antigos estão marcados como indisponíveis até que seus arquivos sejam recriados. Se o ID não existir, estiver duplicado ou não corresponder ao tipo de ativo solicitado, pare e informe. Não selecione silenciosamente outro template.

## 3. Ordem obrigatória de consulta

1. `ROUTER-MESTRE.md`, `regras/00-LEIA-PRIMEIRO.md` e `templates/CATALOGO.md`.
2. Template exato do catálogo.
3. Arquivo narrativo da coleção: `historias/historia-novo-testamento.md` ou `historias/historias-antigo-testamento.md`.
4. Manifesto específico da coleção, se aplicável: `historias/status-criacao-historia.novo-testamento.md` ou `historias/status-criacao-historia.antigo-testamento.md`; usar `templates/status-criacao-historia.template.md` como esquema. O manifesto legado não deve ser automaticamente migrado.
5. `regras/SKILLS-E-RECURSOS.md`.
6. Regras globais de composição/validação e quaisquer anexos apontados pelo template.
7. Skills externas atuais aplicáveis, com evidência real de consulta e disponibilidade.
8. Referências visuais/técnicas, somente se o arquivo realmente existir e estiver acessível.

Se o arquivo necessário não puder ser consultado, relatar o bloqueio. Não tratar memória, links ou nomes de arquivos como evidência de conteúdo acessível.

## 4. Separação de fontes de verdade

- **Fonte narrativa:** determina fatos, personagens, acontecimentos, cenário narrativo, sequência e ensinamento.
- **Template:** determina entrada, contexto de produção, formato do ativo, etapas e critérios específicos.
- **Regras globais:** determinam integridade, roteamento, limitações, qualidade e registro.
- **Skill:** ajuda a executar o processo técnico quando disponível; não pode alterar conteúdo narrativo nem substituir as exigências do template.
- **Status/manifesto de ativos:** determina o estado apenas se existir, estiver atualizado e tiver relação explícita com o tipo de ativo. Não usar o status legado do Novo Testamento para presumir estado de outros templates ou sprites.

## 5. Porta de entrada e bloqueios

Antes da chamada de geração, validar:
- Template ID e versão;
- coleção e fonte narrativa correta;
- título/elemento sem ambiguidade;
- contexto e sequência bloqueados;
- requisitos técnicos do ativo definidos;
- status/autorização, quando o template usar controle de progresso;
- skill/ferramenta e parâmetros disponíveis.

Se faltar informação que altera materialmente o resultado — por exemplo, sprite individual versus sprite sheet, transparência, quantidade de frames, dimensões ou perspectiva — faça uma pergunta objetiva antes de gerar. Não invente o dado.

## 6. Skill routing obrigatório

- **Principal para geração:** `higgsfield-generate` do repositório https://github.com/higgsfield-ai/skills, no caminho https://github.com/higgsfield-ai/skills/blob/main/higgsfield-generate/SKILL.md.
- Consultar a versão atual a cada execução de geração quando a fonte estiver acessível. Se não estiver, seguir apenas uma alternativa explicitamente permitida no template e declarar a limitação.
- A cópia `.agents/skills/higgsfield-generate/SKILL.md` é uma cópia de trabalho; não prova disponibilidade de CLI, integração, credenciais ou execução.
- `taste-skill` é complementar para direção artística; `open-design` é opcional para exploração visual.
- Nunca declarar que instalou, consultou ou executou skill sem evidência.

## 7. Uma saída final por solicitação

Para uma solicitação de ativo final, fazer uma única chamada destinada à saída final e configurar quantidade 1 quando houver controle. Não criar variantes, lotes ou chamadas paralelas, salvo se o template aprovado especificar explicitamente outra coisa. Se o gerador não permitir controlar quantidade, informar. Se retornar vários resultados apesar da configuração, não aprovar todos automaticamente.

## 8. Padrão visual e validação

Aplicar as regras específicas do template primeiro, junto às regras globais em [PADRAO-VISUAL-E-COMPOSICAO.md](PADRAO-VISUAL-E-COMPOSICAO.md) e [VALIDACAO-FINAL.md](VALIDACAO-FINAL.md). Não aplicar o layout de prancha 3×2 a sprites quando isso for incompatível com o template.

Validar contra o tipo de ativo solicitado: fidelidade, composição, anatomia, continuidade, cor, legibilidade e/ou requisitos de sprite. Separar validação editorial de validação técnica.

## 9. Registro e encerramento

Não declarar arquivo salvo, caminho, aprovação, commit ou status atualizado sem comprovação. Não sobrescrever ativo aprovado sem autorização. Se a ferramenta não permitir salvar no repositório, entregar o artefato e registrar claramente que o upload/registro continua pendente.

Relatório final: Template ID/versão; título/elemento; fontes consultadas; skill/ferramenta realmente usada; parâmetros/quantidade; resultado da validação; arquivo e caminho reais; mudanças de status realmente confirmadas; pendências.
