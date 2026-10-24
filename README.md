<div align="center">

# Estudo Bíblico — Image & Sprite Lab

**Templates universais para mockups e produção visual rastreável**

[Roteador mestre](ROUTER-MESTRE.md) · [Catálogo](templates/CATALOGO.md) · [Regras](regras/00-LEIA-PRIMEIRO.md) · [Instruções do Projeto ChatGPT](configuracao-projeto-prompt-instrucao/PROMPT-PROJETO.md)

</div>

## Como começar

1. Leia [`ROUTER-MESTRE.md`](ROUTER-MESTRE.md).
2. Consulte [`templates/CATALOGO.md`](templates/CATALOGO.md) e escolha um ID existente.
3. Leia o template atual e consulte a fonte narrativa correspondente.
4. Leia as regras e a documentação atual das skills externas.
5. Gere o ativo, valide-o e registre apenas estados confirmados.

### Template universal atual

[`TPL-MOCKUP-UNIVERSAL`](templates/mockup-template.md) — modelo de mockup de histórias com balões de fala, caixas retangulares de narração e layout adaptável.

## Convenção de fontes por história/coleção

Para cada identificador `<nome-historia>`, mantenha o par:

- **Narrativa:** `historias/historias-<nome-historia>.md`
- **Status:** `historias/status-criacao-historia.<nome-historia>.md`

O identificador precisa ser o mesmo nos dois nomes, em minúsculas, sem espaços e preferencialmente separado por hífens. A convenção é universal; os caminhos precisam ser confirmados na árvore atual do GitHub antes de cada produção.

Exemplos atuais:

- `historias/historias-novo-testamento.md`
- `historias/status-criacao-historia.novo-testamento.md`
- `historias/historias-antigo-testamento.md`
- `historias/status-criacao-historia.antigo-testamento.md`

Não presuma que outros arquivos existem com base apenas no padrão.

## Estrutura documental

| Caminho | Função |
|---|---|
| [`ROUTER-MESTRE.md`](ROUTER-MESTRE.md) | Ponto de entrada estável |
| [`regras/00-LEIA-PRIMEIRO.md`](regras/00-LEIA-PRIMEIRO.md) | Ordem de consulta |
| [`templates/CATALOGO.md`](templates/CATALOGO.md) | IDs de templates disponíveis |
| [`templates/mockup-template.md`](templates/mockup-template.md) | Mockup visual universal |
| [`templates/status-criacao-historia.template.md`](templates/status-criacao-historia.template.md) | Esquema de status |
| [`regras/ROTA-GERAL.md`](regras/ROTA-GERAL.md) | Fluxo operacional |
| [`regras/SKILLS-E-RECURSOS.md`](regras/SKILLS-E-RECURSOS.md) | Higgsfield e recursos complementares |
| [`regras/PADRAO-VISUAL-E-COMPOSICAO.md`](regras/PADRAO-VISUAL-E-COMPOSICAO.md) | Direção visual e tipográfica |
| [`regras/VALIDACAO-FINAL.md`](regras/VALIDACAO-FINAL.md) | Checklist |
| [`historias/historia-novo-testamento.md`](historias/historia-novo-testamento.md) | Narrativa existente do Novo Testamento |
| [`historias/historias-antigo-testamento.md`](historias/historias-antigo-testamento.md) | Narrativa existente do Antigo Testamento |
| [`historias/status-criacao-historia.novo-testamento.md`](historias/status-criacao-historia.novo-testamento.md) | Manifesto do Novo Testamento |
| [`historias/status-criacao-historia.antigo-testamento.md`](historias/status-criacao-historia.antigo-testamento.md) | Manifesto do Antigo Testamento |
| [`configuracao-projeto-prompt-instrucao/PROMPT-PROJETO.md`](configuracao-projeto-prompt-instrucao/PROMPT-PROJETO.md) | Instruções do Projeto ChatGPT |

## Idioma e ortografia

Todo texto editorial deve usar **português brasileiro (pt-BR)**: título, diálogo, narração, legendas, instruções, documentação e relatório. Revise acentos, pontuação, ortografia, concordância e naturalidade antes de aprovar uma imagem.

## Skills e ferramentas

- **Principal para geração:** [Higgsfield Generate](https://github.com/higgsfield-ai/skills/blob/main/higgsfield-generate/SKILL.md). Consulte a versão atual no repositório oficial antes de cada geração.
- **Complementar para exemplos/prompts:** [awesome-gpt-image-2](https://github.com/freestylefly/awesome-gpt-image-2), incluindo a [GPT-Image2 Style Library](https://github.com/freestylefly/awesome-gpt-image-2/blob/main/agents/skills/gpt-image-2-style-library/SKILL.md).

A biblioteca complementar ajuda na escolha de estilos e na estrutura de prompts; não substitui a narrativa canônica nem comprova que a ferramenta está operacional. Não depender de cópias locais para saber se houve atualização upstream.

## Integridade

Não inventar arquivos, status ou resultados. Não marcar uma imagem aprovada sem inspeção visual real. Uma imagem exibida no chat não prova que foi salva no GitHub. Não sobrescrever ativos aprovados sem autorização.
