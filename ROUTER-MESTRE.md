# ROUTER-MESTRE.md — ponto de entrada estável

**Política:** não alterar em atualizações rotineiras. Mudanças na arquitetura de roteamento exigem autorização explícita do responsável pelo projeto.

Repositório canônico: https://github.com/milson-rodrigues/geracao-de-historia — branch `main`.

## Roteamento obrigatório

1. Leia [`regras/00-LEIA-PRIMEIRO.md`](regras/00-LEIA-PRIMEIRO.md).
2. Consulte [`templates/CATALOGO.md`](templates/CATALOGO.md) e confirme que o Template ID existe.
3. Abra o arquivo exato do template selecionado. Para o mockup universal, use [`templates/mockup-template.md`](templates/mockup-template.md), ID `TPL-MOCKUP-UNIVERSAL`.
4. Identifique a fonte narrativa correspondente na árvore atual do repositório: `historias/historias-<nome-historia>.md`. Não presuma que um arquivo existe só porque segue o padrão.
5. Para tarefas rastreadas, identifique o manifesto par: `historias/status-criacao-historia.<nome-historia>.md`.
6. Siga [`regras/ROTA-GERAL.md`](regras/ROTA-GERAL.md), [`regras/SKILLS-E-RECURSOS.md`](regras/SKILLS-E-RECURSOS.md), [padrão visual](regras/PADRAO-VISUAL-E-COMPOSICAO.md) e [validação final](regras/VALIDACAO-FINAL.md).
7. Consulte a documentação atual das skills externas e referências visuais quando acessíveis.

## Contrato universal das fontes

Para cada identificador estável `<nome-historia>`:

- Narrativa: `historias/historias-<nome-historia>.md`
- Status: `historias/status-criacao-historia.<nome-historia>.md`

Use exatamente o mesmo identificador nos dois arquivos. O padrão não prova que o arquivo existe; verifique a árvore e leia o arquivo. Nunca associe uma narrativa a um manifesto de outra coleção.

## Precedência

A narrativa canônica define fatos, personagens, acontecimentos e sequência. O template define o ativo e sua composição. As regras definem o fluxo. As skills apoiam a execução técnica e não podem contrariar as fontes anteriores.

## Integridade

- Não inventar IDs, arquivos, fontes, imagens salvas, status, commits ou execuções de ferramentas.
- Se uma fonte essencial estiver ausente ou inacessível, informar o bloqueio em vez de completar por memória.
- Não afirmar que imagens de referência existem no GitHub sem verificar os arquivos.
- Uma imagem exibida no chat não prova que foi salva no repositório.
- Não aprovar um ativo sem inspeção real e confirmação do arquivo final.

## Política de mudança

Atualizações comuns devem ocorrer nos templates, manifestos e regras especializadas. Alterar este roteador exige explicar o motivo, obter autorização explícita e conferir os links antes do commit.

**Limite técnico:** esta convenção não torna o arquivo imutável no GitHub. Para bloqueio técnico, configure proteção da branch e revisão obrigatória para alterações neste caminho.
