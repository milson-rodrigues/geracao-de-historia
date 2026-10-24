# ROUTER-MESTRE.md — ponto de entrada estável

**Política:** não alterar em atualizações rotineiras. Mudanças exigem autorização explícita do responsável pelo projeto.

Repositório canônico: https://github.com/milson-rodrigues/geracao-de-historia — branch `main`.

## Roteamento

1. [Catálogo de templates](templates/CATALOGO.md): confirmar Template ID.
2. Abrir o arquivo exato indicado pelo catálogo.
3. Consultar a fonte narrativa oficial indicada no template.
4. Seguir [regras/ROTA-GERAL.md](regras/ROTA-GERAL.md).
5. Aplicar [regras/SKILLS-E-RECURSOS.md](regras/SKILLS-E-RECURSOS.md).
6. Consultar regras globais e validação. Para status, usar o manifesto específico da coleção: [Novo Testamento](status-criacao-historia.novo-testamento.md) ou [Antigo Testamento](status-criacao-historia.antigo-testamento.md), seguindo o esquema [status-criacao-historia.template.md](status-criacao-historia.template.md).

## Precedência

A fonte narrativa define fatos; o template define o ativo, contexto e roteiro; a rota geral define o fluxo; o documento de skills define os recursos técnicos. Skills não podem contrariar a narrativa nem o template.

## Regras de integridade

- Não inventar Template IDs, fontes, arquivos, imagens salvas, status, commits ou execução de ferramentas.
- Se um destino estiver ausente ou ambíguo, parar e informar.
- Não mover nem excluir fontes canônicas sem migração planejada e revisão dos links.
- Não afirmar que imagens de referência existem: elas ainda não foram adicionadas ao repositório.
- Uma solicitação de ativo final usa uma única chamada destinada à saída final e quantidade 1 quando suportada.
- Não aprovar sem inspeção real e confirmação do arquivo final.

## Skills

A skill principal para geração é `higgsfield-generate`: https://github.com/higgsfield-ai/skills/blob/main/higgsfield-generate/SKILL.md. Consultar a versão atual quando acessível e confirmar que a ferramenta está disponível antes de declarar execução. `taste-skill` é complementar; `open-design` é opcional. Ver [SKILLS-E-RECURSOS.md](regras/SKILLS-E-RECURSOS.md).

## Política de mudança

Atualizar templates e documentos especializados sem alterar este roteador. Se a arquitetura de roteamento precisar mudar, solicitar autorização, alterar este arquivo em commit dedicado e verificar todos os destinos.

**Nota técnica:** este arquivo não fica imutável apenas por convenção. Para bloquear alterações no GitHub, configurar regras de proteção da branch e revisão obrigatória para mudanças neste caminho.
