# Índice do projeto — produção por templates

**Projeto:** Estudo Bíblico — Image & Sprite Lab  
**Repositório:** https://github.com/milson-rodrigues/geracao-de-historia  
**Branch:** `main`

## Conceito

O ponto de entrada da produção é um Template ID que determina coleção e tipo de ativo. O usuário informa também o título/elemento. O template direciona fontes narrativas, contexto, roteiro de execução, regras visuais/técnicas, validação e relatório.

## Entradas canônicas

- Catálogo: `templates/CATALOGO.md`
- Regras para novos templates: `templates/README.md`
- Rota geral: `regras/ROTA-GERAL.md`
- Skills: `regras/SKILLS-E-RECURSOS.md`
- Padrão de prancha: `regras/PADRAO-VISUAL-E-COMPOSICAO.md`
- Validação final global: `regras/VALIDACAO-FINAL.md`
- Instruções do ChatGPT: `PROMPT-PROJETO-CHATGPT.md`

## Fontes narrativas legadas

- Novo Testamento: `historia-novo-testamento.md`
- Antigo Testamento: `historias-antigo-testamento.md`

Esses arquivos permanecem na raiz até uma migração deliberada. A aplicabilidade do status legado deve ser verificada por template.

## Templates iniciais

- `TPL-HNT-HISTORIA`
- `TPL-HAT-HISTORIA`
- `TPL-HNT-SPRITE`
- `TPL-HAT-SPRITE`

Consulte `templates/CATALOGO.md` para os caminhos e o estado.

## Skill principal

`higgsfield-generate`: https://github.com/higgsfield-ai/skills/blob/main/higgsfield-generate/SKILL.md  
Complementar: https://github.com/Leonxlnx/taste-skill  
Opcional: https://github.com/nexu-io/open-design

## Pendências de estrutura

- Confirmar tecnicamente os parâmetros exigidos para cada tipo de sprite (dimensão, fundo, pivot, frames, escala e engine, se aplicável).
- Decidir se status/manifests de produção serão separados por coleção e tipo de ativo.
- Migrar ou catalogar os ativos visuais somente após confirmação de quais arquivos aprovados realmente existem.
- Revisar e harmonizar os documentos operacionais legados antes de removê-los ou mudar seus caminhos.
