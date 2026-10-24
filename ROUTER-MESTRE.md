# ROUTER-MESTRE.md — ponto de entrada estável

**Política:** não alterar em atualizações rotineiras. Mudanças na arquitetura de roteamento exigem autorização explícita do responsável pelo projeto.

Repositório canônico: https://github.com/milson-rodrigues/geracao-de-historia — branch `main`.

## Roteamento obrigatório

1. Leia [`regras/00-LEIA-PRIMEIRO.md`](regras/00-LEIA-PRIMEIRO.md).
2. Consulte [`templates/CATALOGO.md`](templates/CATALOGO.md) e confirme que o Template ID está disponível.
3. Abra o arquivo exato do template. No estado atual, o template disponível é [`templates/mockup-template.md`](templates/mockup-template.md), ID `TPL-MOCKUP-HISTORIA`.
4. Consulte a fonte narrativa correspondente:
   - Novo Testamento: [`historias/historia-novo-testamento.md`](historias/historia-novo-testamento.md).
   - Antigo Testamento: [`historias/historias-antigo-testamento.md`](historias/historias-antigo-testamento.md).
5. Consulte o manifesto de status aplicável, quando a tarefa exigir registro:
   - [Status do Novo Testamento](historias/status-criacao-historia.novo-testamento.md).
   - [Status do Antigo Testamento](historias/status-criacao-historia.antigo-testamento.md).
   - Esquema: [`templates/status-criacao-historia.template.md`](templates/status-criacao-historia.template.md).
6. Siga [`regras/ROTA-GERAL.md`](regras/ROTA-GERAL.md), [`regras/SKILLS-E-RECURSOS.md`](regras/SKILLS-E-RECURSOS.md), [padrão visual](regras/PADRAO-VISUAL-E-COMPOSICAO.md) e [validação final](regras/VALIDACAO-FINAL.md).
7. Consulte referências visuais somente quando os arquivos estiverem realmente presentes e acessíveis.

## Precedência

A fonte narrativa define os fatos; o template define o ativo e a composição; as regras definem o fluxo e a qualidade; a skill auxilia a execução técnica. Skills não podem contradizer a fonte ou o template.

## Integridade

- Não inventar IDs, arquivos, fontes, imagens salvas, status, commits ou execução de ferramentas.
- Se um destino estiver ausente ou ambíguo, parar e informar o bloqueio.
- Não mover nem excluir fontes canônicas sem plano de migração e revisão de links.
- Não afirmar que existem imagens de referência no GitHub: a estrutura atual não contém uma pasta de referências visuais catalogada.
- Uma imagem exibida no chat não prova que foi salva no repositório.
- Não aprovar um ativo sem inspeção real e confirmação do arquivo final.

## Política de mudança

Atualizações comuns devem ocorrer nos templates, manifestos e regras especializadas. Para alterar este roteador, explicar o motivo, obter autorização explícita e conferir os links antes do commit.

**Limite técnico:** a convenção não torna o arquivo imutável no GitHub. Para bloqueio técnico, configurar regras de proteção da branch e revisão obrigatória para alterações neste caminho.
