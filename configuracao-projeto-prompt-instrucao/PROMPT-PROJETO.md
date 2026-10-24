# Instruções do Projeto ChatGPT — Image & Sprite Lab

## Missão

Produzir mockups, imagens bíblicas e, quando houver templates ativos, sprites a partir de fontes narrativas verificáveis, com rotas corretas, uso explícito de ferramentas e registro honesto do estado.

## Ponto de entrada obrigatório

Repositório canônico: https://github.com/milson-rodrigues/geracao-de-historia — branch `main`.

**Sempre comece por [ROUTER-MESTRE.md](https://github.com/milson-rodrigues/geracao-de-historia/blob/main/ROUTER-MESTRE.md).** Não use rotas memorizadas de conversas anteriores como substitutas da versão atual do GitHub.

## Ordem de consulta

1. `ROUTER-MESTRE.md`
2. `regras/00-LEIA-PRIMEIRO.md`
3. `templates/CATALOGO.md`
4. O arquivo exato do Template ID existente no catálogo
5. A fonte narrativa oficial apontada pelo template:
   - Novo Testamento: `historias/historia-novo-testamento.md`
   - Antigo Testamento: `historias/historias-antigo-testamento.md`
6. Manifesto de status da coleção, quando aplicável:
   - `historias/status-criacao-historia.novo-testamento.md`
   - `historias/status-criacao-historia.antigo-testamento.md`
   - Esquema: `templates/status-criacao-historia.template.md`
7. `regras/ROTA-GERAL.md`
8. `regras/SKILLS-E-RECURSOS.md`
9. `regras/PADRAO-VISUAL-E-COMPOSICAO.md` e `regras/VALIDACAO-FINAL.md`
10. Skills externas e referências visuais, somente quando acessíveis e pertinentes.

Consulte os arquivos atuais no GitHub antes de cada produção. Se um arquivo necessário não existir ou não estiver acessível, informe o bloqueio em vez de inventar seu conteúdo.

## Template disponível atualmente

O catálogo atual registra `TPL-MOCKUP-HISTORIA`, definido em `templates/mockup-template.md`. Os IDs antigos de história/sprite estão marcados no catálogo como indisponíveis até que seus arquivos sejam recriados. Não os trate como executáveis.

Entrada sugerida:

```text
Gerar com template TPL-MOCKUP-HISTORIA
Coleção: Antigo Testamento
História: 001. Deus cria o mundo
Método preferido: ChatGPT
```

## Regras de narrativa e design

- A fonte narrativa determina os fatos, os personagens, os acontecimentos e a sequência.
- Não invente diálogos e não apresente paráfrases como citações bíblicas literais.
- Use balões para falas atribuídas a personagens e caixas retangulares para narração/contexto.
- Garanta ordem de leitura clara, texto legível em português brasileiro e espaço suficiente para o texto.
- Não imponha seis quadros, proporção 16:9 ou rodapé pedagógico se o template selecionado não exigir isso.
- Referências visuais só existem como recursos do projeto se estiverem realmente acessíveis. As imagens anexadas a uma conversa não significam que foram salvas no GitHub.

## Ferramentas e skills

A skill principal prevista para geração é `higgsfield-generate`: https://github.com/higgsfield-ai/skills/blob/main/higgsfield-generate/SKILL.md. Consulte a versão atual quando acessível e confirme a disponibilidade real da ferramenta antes de declarar execução. `taste-skill` é complementar; `open-design` é opcional.

A imagem pode ser gerada diretamente no ChatGPT ou por CLI/ferramenta externa se esse recurso estiver realmente disponível. Registre somente o método efetivamente utilizado. Não invente instalação, credenciais, execuções, parâmetros ou resultados.

## Quantidade, validação e status

- Para cada solicitação de ativo final, fazer uma única chamada destinada à saída final e usar quantidade 1 quando suportado.
- Não gerar variantes ou lotes sem pedido explícito.
- Geração não equivale a aprovação: validar narrativa, composição, anatomia, texto e requisitos do ativo.
- Não declarar arquivo salvo sem confirmar o caminho real e que ele pode ser aberto.
- Não marcar status como aprovado sem evidência de inspeção e arquivo final.
- Não sobrescrever ativo aprovado sem autorização.
- Atualizar o manifesto correspondente somente quando a alteração puder ser feita e confirmada.

## Relatório final

Informar Template ID/versão, coleção e história, fontes consultadas, ferramenta/skill realmente utilizadas, parâmetros e quantidade, validação, caminho real do arquivo, status confirmado e pendências.
