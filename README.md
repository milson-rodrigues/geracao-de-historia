<div align="center">

# Estudo Bíblico — Image & Sprite Lab

**Templates universais para mockups e produção visual rastreável**

[Roteador mestre](ROUTER-MESTRE.md) · [Catálogo](templates/CATALOGO.md) · [Regras](regras/00-LEIA-PRIMEIRO.md) · [Instruções do Projeto ChatGPT](configuracao-projeto-prompt-instrucao/PROMPT-PROJETO.md)

</div>

## Como começar

1. Leia [`ROUTER-MESTRE.md`](ROUTER-MESTRE.md).
2. Consulte [`templates/CATALOGO.md`](templates/CATALOGO.md) e escolha um ID existente.
3. Leia o template e a fonte narrativa atual.
4. Consulte as regras e a versão atual das skills externas.
5. Gere o ativo, valide-o e registre apenas estados confirmados.

## Template universal

[`TPL-MOCKUP-UNIVERSAL`](templates/mockup-template.md) — mockup de história com balões de fala, caixas retangulares de narração e layout adaptável.

**Direção visual aprovada:** padrão horizontal 16:9 (mínimo 1920 × 1080) e variante vertical 9:16 (mínimo 1080 × 1920, somente se solicitada). Os dois modelos estão juntos na pasta `mockups/`.

## Convenção universal das fontes

Para cada identificador `<nome-historia>`, mantenha o par de arquivos:

- **Narrativa:** `historias/historias-<nome-historia>.md`
- **Status:** `historias/status-criacao-historia.<nome-historia>.md`

O segmento deve ser idêntico nos dois nomes, em minúsculas, sem espaços e preferencialmente separado por hífens. Confirme os caminhos na árvore atual do GitHub; não presuma que arquivos existem apenas porque seguem o padrão.

Arquivos canônicos presentes:
- [`historias/historias-novo-testamento.md`](historias/historias-novo-testamento.md)
- [`historias/status-criacao-historia.novo-testamento.md`](historias/status-criacao-historia.novo-testamento.md)
- [`historias/historias-antigo-testamento.md`](historias/historias-antigo-testamento.md)
- [`historias/status-criacao-historia.antigo-testamento.md`](historias/status-criacao-historia.antigo-testamento.md)

## Estrutura documental

| Caminho | Função |
|---|---|
| [`ROUTER-MESTRE.md`](ROUTER-MESTRE.md) | Ponto de entrada estável |
| [`regras/00-LEIA-PRIMEIRO.md`](regras/00-LEIA-PRIMEIRO.md) | Ordem de consulta |
| [`templates/CATALOGO.md`](templates/CATALOGO.md) | IDs disponíveis |
| [`templates/mockup-template.md`](templates/mockup-template.md) | Template de mockup universal |
| [`mockups/mockup-template-universal.svg`](mockups/mockup-template-universal.svg) | Modelo principal 16:9, 1920 × 1080 |
| [`mockups/mockup-template-universal-9x16.svg`](mockups/mockup-template-universal-9x16.svg) | Variante 9:16, 1080 × 1920; somente sob solicitação |
| [`templates/status-criacao-historia.template.md`](templates/status-criacao-historia.template.md) | Esquema dos manifestos |
| [`regras/ROTA-GERAL.md`](regras/ROTA-GERAL.md) | Fluxo operacional |
| [`regras/SKILLS-E-RECURSOS.md`](regras/SKILLS-E-RECURSOS.md) | Skills e recursos complementares |
| [`regras/PADRAO-VISUAL-E-COMPOSICAO.md`](regras/PADRAO-VISUAL-E-COMPOSICAO.md) | Direção visual e tipografia |
| [`regras/VALIDACAO-FINAL.md`](regras/VALIDACAO-FINAL.md) | Checklist de validação |
| [`configuracao-projeto-prompt-instrucao/PROMPT-PROJETO.md`](configuracao-projeto-prompt-instrucao/PROMPT-PROJETO.md) | Instruções internas do Projeto ChatGPT |

## Idioma e ortografia

Todo texto editorial deve usar **português brasileiro (pt-BR)**: títulos, falas, narração, legendas, instruções, documentação e relatórios. Revisar ortografia, acentuação, pontuação, concordância e legibilidade antes de aprovar.

## Skills

- **Principal para geração:** [Higgsfield Generate](https://github.com/higgsfield-ai/skills/blob/main/higgsfield-generate/SKILL.md). Consultar a versão atual no repositório oficial antes de cada geração.
- **Complementar para referência de prompts e estilos:** [awesome-gpt-image-2](https://github.com/freestylefly/awesome-gpt-image-2), incluindo a [GPT-Image2 Style Library](https://github.com/freestylefly/awesome-gpt-image-2/blob/main/agents/skills/gpt-image-2-style-library/SKILL.md).

A biblioteca complementar ajuda a descobrir estilos e estruturar prompts; não substitui a narrativa canônica nem a documentação atual da ferramenta de geração. Não presumir que uma CLI ou integração está operacional apenas porque existe uma skill no GitHub.

## Integridade

Não inventar fontes, imagens salvas, status ou resultados. Uma imagem exibida no chat não prova que foi salva no GitHub. Não marcar um ativo aprovado sem inspeção real e validação do usuário quando requerida.


## Cópias locais de skills

A pasta `.agents/skills/` contém arquivos locais de apoio e pode ficar defasada. Para qualquer produção, consulte primeiro a versão atual publicada no repositório oficial indicado em `regras/SKILLS-E-RECURSOS.md`. Não trate a cópia local como autoridade de versão e não declare uma ferramenta operacional apenas pela presença de arquivos locais.
