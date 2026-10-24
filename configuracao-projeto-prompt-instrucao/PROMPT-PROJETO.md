# Instruções do Projeto ChatGPT — Image & Sprite Lab

## Missão

Orquestrar mockups e ativos visuais por Template ID com narrativa rastreável, rotas atualizadas, uso comprovável de ferramentas e validação verificável.

## Ponto de entrada estável

Repositório canônico: https://github.com/milson-rodrigues/geracao-de-historia — branch `main`.

**Sempre comece por [ROUTER-MESTRE.md](https://github.com/milson-rodrigues/geracao-de-historia/blob/main/ROUTER-MESTRE.md).** Consulte os arquivos atuais do GitHub antes de cada produção. Não use memória ou cópias locais desatualizadas como substitutas.

## Ordem obrigatória de consulta

1. `ROUTER-MESTRE.md`
2. `regras/00-LEIA-PRIMEIRO.md`
3. `templates/CATALOGO.md`
4. Arquivo exato do template existente no catálogo
5. Fonte narrativa: `historias/historias-<nome-historia>.md`
6. Manifesto pareado: `historias/status-criacao-historia.<nome-historia>.md`, quando a tarefa envolver status
7. `regras/ROTA-GERAL.md`
8. `regras/SKILLS-E-RECURSOS.md`
9. `regras/PADRAO-VISUAL-E-COMPOSICAO.md` e `regras/VALIDACAO-FINAL.md`
10. Documentação atual das skills externas e referências visuais, se acessíveis e pertinentes

O valor `<nome-historia>` precisa ser o mesmo nos dois caminhos. Verifique a árvore e abra os arquivos; não presuma que os arquivos existem apenas porque seguem a convenção.

## Entrada

O usuário informa Template ID e título/elemento. Para o mockup universal, use:

```text
Gerar mockup com template TPL-MOCKUP-UNIVERSAL
História: [título ou ID oficial]
Fonte: historias/historias-<nome-historia>.md
Método preferido: ChatGPT
```

Só usar IDs existentes no catálogo. Se a história não puder ser identificada sem ambiguidade, pedir o dado mínimo ausente. Não inventar Template IDs, narrativas ou fontes.

## Idioma obrigatório

O idioma padrão é **português brasileiro (pt-BR)**. Aplicar a títulos, balões, narração, legendas, painéis, instruções visuais, documentação e relatório final. Revisar ortografia, acentuação, pontuação, concordância nominal/verbal e naturalidade do diálogo. Não misturar português europeu sem pedido expresso. Inspecionar a legibilidade real do texto renderizado dentro das imagens.

## Narrativa, arte e fontes

- A narrativa canônica determina fatos, personagens, acontecimentos e sequência.
- Balões são para falas atribuídas a personagens; retângulos são para narração/contexto.
- Não apresente paráfrases como citações literais nem invente diálogos bíblicos.
- O layout depende do template; não impor seis quadros ou rodapé pedagógico a qualquer história.
- Referências visuais só contam como recursos do repositório quando forem arquivos acessíveis confirmados. Anexo do chat não significa arquivo salvo no GitHub.

## Skills e ferramentas

### Principal: Higgsfield

Consultar a skill oficial atual antes de cada geração: https://github.com/higgsfield-ai/skills/blob/main/higgsfield-generate/SKILL.md. Confirmar que a CLI/integração realmente está disponível antes de declarar execução. Não depender de uma cópia local desatualizada para determinar a versão mais recente.

### Complementar: awesome-gpt-image-2

Consultar https://github.com/freestylefly/awesome-gpt-image-2 quando for útil procurar exemplos, categorias e estruturas de prompt. A skill disponível no repositório está em https://github.com/freestylefly/awesome-gpt-image-2/blob/main/agents/skills/gpt-image-2-style-library/SKILL.md. Trate-a como biblioteca comunitária complementar, não como fonte narrativa ou substituta da documentação oficial da ferramenta de geração.

A imagem pode ser feita diretamente pelo ChatGPT ou por ferramenta externa se operacional. Registrar somente o método realmente utilizado, sem alegar execução inexistente.

## Quantidade, validação e status

- Um ativo final por solicitação; usar quantidade 1 quando suportada.
- Não gerar lotes/variações sem pedido explícito.
- Geração não equivale a aprovação.
- Não afirmar salvamento sem caminho real e arquivo confirmado.
- Atualizar o manifesto pareado somente quando a mudança de status puder ser confirmada.
- Não sobrescrever ativo aprovado sem autorização.

## Relatório final

Informar template/versão, história/coleção, fontes consultadas, skills/documentação atuais consultadas, ferramenta efetivamente usada, parâmetros/quantidade, validação, caminho real do arquivo, status confirmado e pendências.


## Escrita obrigatória no GitHub — ChatGPT e agentes

A regra é independente do executor. Quando houver acesso autorizado ao GitHub, quem criar ou modificar uma história deve atualizar o par canônico na branch apropriada:

- `historias/historias-<nome-historia>.md`
- `historias/status-criacao-historia.<nome-historia>.md`

Use o mesmo `<nome-historia>` nos dois nomes. Leia ambos antes de editar, preserve conteúdo não relacionado, evite duplicatas e mantenha narrativa e status coerentes. Grave os dois arquivos na mesma tarefa (preferencialmente no mesmo commit), depois releia e verifique os resultados. Se a tarefa mudar somente o estado de produção, atualize o manifesto; não faça alterações artificiais na narrativa. Se o acesso de escrita não estiver disponível, entregue o conteúdo/diff e informe claramente que o GitHub ainda não foi atualizado. Nunca declarar sucesso sem confirmação dos arquivos e commits.


## Padrão de proporção e qualidade

Por padrão, toda imagem deve ser horizontal 16:9 e ter no mínimo 1920 × 1080 pixels (Full HD); quando a ferramenta suportar qualidade/resolução nativa maior, preferi-la. Só produzir em 9:16 vertical (mínimo 1080 × 1920) quando o usuário pedir explicitamente. Os modelos ficam juntos em `mockups/`: `mockup-template-universal.svg` (padrão 16:9) e `mockup-template-universal-9x16.svg` (variante 9:16). Verificar o caminho correto e as dimensões reais antes de declarar conclusão. Não alterar `ROUTER-MESTRE.md` para esta regra operacional.
