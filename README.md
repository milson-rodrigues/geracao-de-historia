<div align="center">

# 📖 Estudo Bíblico — Image & Sprite Lab
### Templates versionados para produção de imagens bíblicas

**Narrativa contextualizada · Skills roteadas · Saídas controladas · Validação verificável**

[Roteador estável](ROUTER.md) · [Catálogo de templates](templates/CATALOGO.md) · [Rota geral](regras/ROTA-GERAL.md) · [Skills](regras/SKILLS-E-RECURSOS.md) · [Instruções do ChatGPT](PROMPT-PROJETO-CHATGPT.md)

</div>

---

## Conceito atual

Este repositório organiza a produção visual por **template ID**, não apenas por um número de história. Cada template especifica coleção/testamento, tipo de ativo, fontes canônicas, contexto, roteiro de execução, regras de composição e critérios de validação.

Os principais tipos iniciais são histórias ilustradas e sprites para Novo e Antigo Testamento. O catálogo pode crescer com novos tipos de saída sem misturar as regras de cada um.

## Início rápido

Informe um template ID e o título/elemento desejado:

```text
Gerar com template TPL-HNT-HISTORIA
Título: O anjo Gabriel aparece a Maria
```

Para sprite:

```text
Gerar com template TPL-HNT-SPRITE
Elemento: Maria — sprite individual
História de origem: O anjo Gabriel aparece a Maria
```

O agente deve resolver o contexto a partir da fonte canônica, verificar se a entrada é inequívoca, ler o roteiro do template e as regras de skills, e interromper caso falte algum dado técnico ou narrativo essencial. Não assumir parâmetros técnicos de sprite que não foram fornecidos.

## Arquitetura de documentação

| Caminho | Responsabilidade |
|---|---|
| [`templates/CATALOGO.md`](templates/CATALOGO.md) | Inventário dos Template IDs, coleção, ativo e estado |
| [`templates/README.md`](templates/README.md) | Convenção para criar e executar templates |
| [`templates/novo-testamento/`](templates/novo-testamento/historia-ilustrada.template.md) | Roteiros para imagens/sprites do Novo Testamento |
| [`templates/antigo-testamento/`](templates/antigo-testamento/historia-ilustrada.template.md) | Roteiros para imagens/sprites do Antigo Testamento |
| [`regras/ROTA-GERAL.md`](regras/ROTA-GERAL.md) | Roteador global e política de execução |
| [`regras/SKILLS-E-RECURSOS.md`](regras/SKILLS-E-RECURSOS.md) | Skill principal e skills complementares |
| [`regras/PADRAO-VISUAL-E-COMPOSICAO.md`](regras/PADRAO-VISUAL-E-COMPOSICAO.md) | Padrão global para pranchas ilustradas |
| [`regras/VALIDACAO-FINAL.md`](regras/VALIDACAO-FINAL.md) | Checklist de qualidade editorial/visual |
| `historia-novo-testamento.md` | Fonte narrativa do Novo Testamento atualmente na raiz |
| `historias-antigo-testamento.md` | Fonte narrativa do Antigo Testamento atualmente na raiz |
| `status-criacao-historia.md` | Status de produção que existe para o fluxo anterior; sua aplicabilidade deve ser verificada por template |
| [`PROMPT-PROJETO-CHATGPT.md`](PROMPT-PROJETO-CHATGPT.md) | Instruções de projeto para colar manualmente |

## Skill routing

1. **Principal para geração:** [`higgsfield-generate`](https://github.com/higgsfield-ai/skills/blob/main/higgsfield-generate/SKILL.md), no repositório oficial [higgsfield-ai/skills](https://github.com/higgsfield-ai/skills). A cópia local está em [`.agents/skills/higgsfield-generate/SKILL.md`](.agents/skills/higgsfield-generate/SKILL.md).
2. **Complementar de direção artística:** [`taste-skill`](https://github.com/Leonxlnx/taste-skill).
3. **Opcional para exploração visual:** [`open-design`](https://github.com/nexu-io/open-design).

A skill é consultada antes da geração quando acessível; sua presença no GitHub não prova que a integração/CLI ou autenticação esteja operacional. Declare apenas ferramentas realmente usadas. A skill complementar pode apoiar direção artística, mas não pode substituir contexto narrativo, template ou regras globais.

## Princípios de execução

- Template define coleção, ativo, contexto e roteiro.
- A fonte narrativa define os fatos; o agente não completa lacunas com suposições.
- Uma solicitação de saída final = uma única chamada destinada ao ativo final; usar quantidade 1 se suportado.
- Não gerar variantes/lotes, a menos que isso esteja explicitamente previsto no template aprovado.
- Validar antes de declarar aprovado; salvar/registrar apenas quando essas operações forem realmente realizadas.
- Não sobrescrever ativo aprovado sem autorização.
- Separar critérios de ilustração editorial de critérios técnicos de sprite. Uma imagem ilustrativa não é automaticamente um sprite pronto para engine.

## Estado da migração

Os arquivos narrativos antigos continuam na raiz para preservar caminhos e histórico. Na árvore consultada não havia diretório `imagens/`; portanto, não presumir que ativos de referência/finais estejam arquivados no repositório. Uma migração para uma estrutura de coleção/ativos deve ser feita em etapa separada, depois de verificar conteúdo, links, status e binários reais.

---

<sub>O catálogo de templates é a entrada operacional. Fontes narrativas são autoridade de conteúdo; templates governam o fluxo; skills executam tarefas quando disponíveis; validação estabelece o resultado.</sub>
