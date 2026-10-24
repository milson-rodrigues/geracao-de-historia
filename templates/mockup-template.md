# Template para mockup visual — modelo universal

- **Template ID:** `TPL-MOCKUP-UNIVERSAL`
- **Versão:** 1.0.0
- **Estado:** AGUARDANDO APROVAÇÃO VISUAL DO USUÁRIO
- **Finalidade:** criar uma imagem-mockup para o usuário avaliar a linguagem visual e a composição antes de gerar histórias reais.
- **Escopo:** qualquer coleção/história declarada por uma fonte narrativa `historias/historias-<nome-historia>.md`.

## 1. Objetivo

Gerar uma imagem de mockup representativa e reutilizável para validar o padrão gráfico. O mockup deve demonstrar como uma página de história combina ilustrações sequenciais, balões de fala e caixas retangulares de narração.

Esta peça é de avaliação visual; não é uma história final aprovada, não deve ser marcada como concluída e não deve alterar o status de produção de uma história real.

## 2. Entrada

Para criar o primeiro mockup, o responsável pode definir uma história de demonstração ou autorizar um exemplo visual sintético. Identifique claramente a fonte usada. Não apresente fatos, personagens ou falas inventados como conteúdo de uma história bíblica real.

Definir antes de cada mockup:
- coleção ou nome da história;
- fonte narrativa oficial, se usar uma história real;
- título de apresentação;
- proporção/layout, se definido;
- método preferido: ChatGPT ou ferramenta externa, conforme disponibilidade real.

Se o tema ainda não foi definido, usar uma demonstração visual genérica e não atribuir falas inventadas a figuras bíblicas identificáveis. Registrar que se trata de demonstração visual.

## 3. Arquitetura universal de fontes

Cada coleção/história deve seguir a convenção:

- Fonte narrativa: `historias/historias-<nome-historia>.md`
- Manifesto de produção: `historias/status-criacao-historia.<nome-historia>.md`

O identificador `<nome-historia>` deve ser estável, em minúsculas, sem espaços e preferencialmente com hífens. O mesmo identificador deve aparecer nos dois arquivos.

Exemplos atuais:
- `historias/historias-novo-testamento.md`
- `historias/status-criacao-historia.novo-testamento.md`
- `historias/historias-antigo-testamento.md`
- `historias/status-criacao-historia.antigo-testamento.md`

Novas coleções devem seguir a convenção sem exigir mudanças neste template. O agente deve descobrir o arquivo consultando a árvore atual do repositório GitHub e seguir os links do roteador/catálogo. Não inferir que um caminho existe apenas porque segue o padrão.

## 4. Consulta obrigatória antes de gerar

1. Consultar a versão atual de `ROUTER-MESTRE.md` no repositório canônico.
2. Ler `regras/00-LEIA-PRIMEIRO.md`.
3. Consultar `templates/CATALOGO.md` e confirmar que este template está disponível.
4. Ler a versão atual deste arquivo.
5. Para uma história real, identificar e ler integralmente `historias/historias-<nome-historia>.md`.
6. Consultar `historias/status-criacao-historia.<nome-historia>.md` se o trabalho envolver uma história rastreada.
7. Ler `regras/ROTA-GERAL.md`, `regras/SKILLS-E-RECURSOS.md`, `regras/PADRAO-VISUAL-E-COMPOSICAO.md` e `regras/VALIDACAO-FINAL.md`.
8. Consultar a documentação atual das skills/ferramentas externas, especialmente a skill oficial Higgsfield no GitHub.
9. Consultar referências visuais apenas quando realmente acessíveis. Anexos do chat não equivalem a arquivos salvos no repositório.

Se uma fonte essencial estiver ausente ou inacessível, declarar o bloqueio. Não preencher lacunas com memória ou suposições.

## 5. Direção visual

A composição é universal e ajustável ao conteúdo, sem impor um número fixo de quadros a todos os tipos de história.

- Página com leitura sequencial clara e quadros delimitados.
- Ilustrações detalhadas, expressivas e consistentes ao longo da página.
- **Balões de fala** para diálogos atribuídos à personagem que fala.
- **Caixas retangulares** para narração, contexto, localização, passagem de tempo e ações descritas.
- Texto curto, com alto contraste, português brasileiro correto e margens internas.
- Balões e caixas organizados segundo a ordem de leitura, sem cobrir rostos ou ações importantes.
- Título visível, hierarquia clara e espaço adequado para texto.
- Se a tipografia gerada ficar deformada, preferir espaços limpos para compor o texto depois e registrar a limitação.
- Paleta equilibrada, anatomia plausível, silhuetas claras e continuidade de personagens.
- A direção artística não pode introduzir fatos narrativos ausentes da fonte.

O primeiro mockup destina-se à avaliação do usuário. Priorizar legibilidade, hierarquia, composição e distinção visual entre fala e narração, não a cobertura integral de uma história.

## 6. Roteamento de geração

### Skill principal: Higgsfield

Fonte oficial: https://github.com/higgsfield-ai/skills  
Skill de geração: https://github.com/higgsfield-ai/skills/blob/main/higgsfield-generate/SKILL.md

Antes de cada execução, consultar a versão atual no GitHub e os documentos relevantes da skill. Não depender de cópia local desatualizada como fonte normativa. Confirmar que o CLI ou a integração está operacional antes de declarar execução.

### Complemento: GPT Image 2 Prompt Library

Repositório: https://github.com/freestylefly/awesome-gpt-image-2

Usar como biblioteca complementar de exemplos, estruturas de prompt e padrões visuais. Não é substituto da skill principal, da narrativa canônica nem das regras do projeto. Os exemplos devem ser avaliados quanto à relevância e adaptados, nunca copiados automaticamente.

### Ferramenta de saída

A imagem poderá ser gerada no ChatGPT ou por ferramenta externa realmente disponível e autorizada. Registrar apenas a ferramenta usada. Um link para a ferramenta não comprova instalação ou execução.

## 7. Quantidade e estado

- Uma solicitação de mockup final deve resultar em uma única tentativa de saída final, com quantidade 1 quando suportada.
- Não criar variantes/lotes sem solicitação explícita.
- O estado do template permanece `AGUARDANDO APROVAÇÃO VISUAL DO USUÁRIO` até aprovação ou pedido de ajustes.
- Não marcar a história usada como concluída: o mockup não representa a produção final.
- Não afirmar que a imagem foi salva no GitHub sem confirmar arquivo e caminho.

## 8. Checklist de aprovação

- [ ] O estilo atende ao uso pretendido.
- [ ] Caixas retangulares são distintas dos balões.
- [ ] É fácil identificar quem está falando.
- [ ] A ordem de leitura é intuitiva.
- [ ] Textos são legíveis ou há espaço para inseri-los depois.
- [ ] A composição não está excessivamente carregada.
- [ ] Anatomia, rostos e mãos não apresentam defeitos graves.
- [ ] O layout pode adaptar-se a histórias diversas, sem ficar preso a seis quadros.
- [ ] Conteúdo fictício não é apresentado como canônico.
- [ ] Método de geração e estado do arquivo foram informados honestamente.

## 9. Relatório

Informar Template ID/versão, tema, fontes consultadas, versão da skill Higgsfield consultada, uso ou não da biblioteca GPT Image 2, ferramenta realmente utilizada, validação, estado da aprovação e caminho real do arquivo quando salvo.
