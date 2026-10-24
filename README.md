<div align="center">

# Estudo Bíblico — Image & Sprite Lab

**Templates versionados para mockups e imagens bíblicas**

[Navegação estável](ROUTER-MESTRE.md) · [Catálogo de templates](templates/CATALOGO.md) · [Regras de trabalho](regras/00-LEIA-PRIMEIRO.md) · [Instruções do Projeto ChatGPT](configuracao-projeto-prompt-instrucao/PROMPT-PROJETO.md)

</div>

---

## Como começar

1. Leia [`ROUTER-MESTRE.md`](ROUTER-MESTRE.md).
2. Confira o [catálogo](templates/CATALOGO.md) e use apenas um Template ID disponível.
3. Abra o template escolhido e consulte a fonte narrativa oficial da coleção.
4. Siga as regras de geração e validação.
5. Registre o resultado no manifesto correto, se aplicável.

### Template disponível

O template ativo no catálogo é [`TPL-MOCKUP-HISTORIA`](templates/mockup-template.md). Ele define uma prancha/mockup de história bíblica em estilo de quadrinhos, com balões de fala e retângulos de narração.

Exemplo:

```text
Gerar com template TPL-MOCKUP-HISTORIA
Coleção: Antigo Testamento
História: 001. Deus cria o mundo
Método preferido: ChatGPT
```

O exemplo não substitui a conferência do título e da sequência na fonte oficial.

## Estrutura atual

| Caminho | Responsabilidade |
|---|---|
| [`ROUTER-MESTRE.md`](ROUTER-MESTRE.md) | Ponto de entrada estável |
| [`regras/00-LEIA-PRIMEIRO.md`](regras/00-LEIA-PRIMEIRO.md) | Ordem de consulta |
| [`templates/CATALOGO.md`](templates/CATALOGO.md) | Template IDs existentes e planejados |
| [`templates/mockup-template.md`](templates/mockup-template.md) | Template de mockup em quadrinhos |
| [`templates/status-criacao-historia.template.md`](templates/status-criacao-historia.template.md) | Esquema dos registros de produção |
| [`historias/historia-novo-testamento.md`](historias/historia-novo-testamento.md) | Fonte narrativa do Novo Testamento |
| [`historias/historias-antigo-testamento.md`](historias/historias-antigo-testamento.md) | Fonte narrativa do Antigo Testamento |
| [`historias/status-criacao-historia.novo-testamento.md`](historias/status-criacao-historia.novo-testamento.md) | Manifesto do Novo Testamento |
| [`historias/status-criacao-historia.antigo-testamento.md`](historias/status-criacao-historia.antigo-testamento.md) | Manifesto do Antigo Testamento |
| [`regras/ROTA-GERAL.md`](regras/ROTA-GERAL.md) | Fluxo operacional |
| [`regras/SKILLS-E-RECURSOS.md`](regras/SKILLS-E-RECURSOS.md) | Skills e ferramentas |
| [`regras/PADRAO-VISUAL-E-COMPOSICAO.md`](regras/PADRAO-VISUAL-E-COMPOSICAO.md) | Direção visual |
| [`regras/VALIDACAO-FINAL.md`](regras/VALIDACAO-FINAL.md) | Checklist de validação |
| [`configuracao-projeto-prompt-instrucao/PROMPT-PROJETO.md`](configuracao-projeto-prompt-instrucao/PROMPT-PROJETO.md) | Instruções para configurar manualmente o Projeto ChatGPT |

## Estilo visual

O mockup usa linguagem de quadrinhos bíblicos:
- balões para falas de personagens;
- retângulos para narração e contexto;
- ordem de leitura clara;
- texto legível em português brasileiro;
- fidelidade à fonte narrativa.

As imagens enviadas em uma conversa podem servir como referência durante aquela tarefa, mas não são automaticamente arquivos de referência do GitHub.

## Geração e integridade

A imagem pode ser criada no ChatGPT ou por CLI/ferramenta externa se o recurso estiver realmente disponível. A skill prevista como principal é [`higgsfield-generate`](https://github.com/higgsfield-ai/skills/blob/main/higgsfield-generate/SKILL.md); sua existência não prova que a CLI ou credenciais estejam operacionais.

Não inventar arquivos, IDs, status, commits ou caminhos. Não declarar aprovação sem inspeção real e não declarar salvamento sem confirmar o arquivo.

## Nota sobre templates planejados

O catálogo lista os IDs antigos de histórias e sprites como indisponíveis porque seus arquivos específicos não estão presentes na estrutura atual. Reative-os somente após recriar os arquivos, verificar suas fontes e atualizar o catálogo e as rotas.
