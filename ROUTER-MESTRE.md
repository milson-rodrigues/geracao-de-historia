# ROUTER-MESTRE.md — memória operacional para criar histórias em quadrinhos

**Função:** ponto de entrada estável para qualquer ChatGPT, agente local/remoto ou pessoa que produza uma história em quadrinhos ilustrada neste repositório.

**Repositório canônico:** https://github.com/milson-rodrigues/geracao-de-historia — branch `main`.

Este arquivo registra o fluxo essencial. As regras detalhadas ficam nos templates e documentos especializados para poderem evoluir sem exigir alterações constantes aqui.

## Pedido do usuário

A forma natural do pedido pode ser, por exemplo:

```text
Gere a imagem da história.
Título: 001 - Deus cria o mundo
Coleção: antigo-testamento
```

O usuário também pode fornecer um arquivo `.md` com o roteiro ou indicar um arquivo de história existente. Não obrigar o usuário a decorar Template IDs ou nomes internos. Se o formato solicitado não estiver claro, confirmar apenas o detalhe que impede a execução.

## Regra de bloqueio: GitHub primeiro

**Toda solicitação de produção deve começar pela consulta ao repositório canônico no GitHub, branch `main`.** Essa consulta é obrigatória em toda sessão e em toda nova história/ativo; não reutilizar rotas, templates, fontes narrativas, manifestos ou instruções lembrados de conversas anteriores como substitutos da versão atual.

- Confirmar acesso ao repositório e ler este roteador atualizado.
- Seguir integralmente a ordem de consulta abaixo e o fluxo descrito nos documentos referenciados.
- Confirmar existência, conteúdo e correspondência de cada arquivo antes de usá-lo.
- Se GitHub, fonte essencial, template ou manifesto aplicável estiver inacessível, interromper a produção e informar exatamente o bloqueio. Não gerar com base em memória, cópia local antiga ou contexto presumido.
- Não iniciar geração enquanto a identificação da história, a leitura narrativa e a verificação de duplicidade/status não estiverem concluídas.

## Rota obrigatória antes da geração

1. Leia [regras/00-LEIA-PRIMEIRO.md](regras/00-LEIA-PRIMEIRO.md).
2. Consulte a árvore atual do GitHub e leia [templates/CATALOGO.md](templates/CATALOGO.md); confirme o template adequado. Para uma prancha em quadrinhos, use `TPL-MOCKUP-UNIVERSAL` e [templates/mockup-template.md](templates/mockup-template.md).
3. Localize e leia a história pedida na fonte narrativa real em `historias/`. Os arquivos atuais incluem:
   - [Novo Testamento](historias/historias-novo-testamento.md)
   - [Antigo Testamento](historias/historias-antigo-testamento.md)
   Não presuma que essa lista é completa; novas coleções podem ser acrescentadas.
4. Identifique a entrada exata pelo número e título. Preserve os fatos, personagens, referência bíblica e sequência; não invente acontecimentos para preencher quadros. Consulte o manifesto de status da coleção e verifique se já existe registro gerado, validado ou aprovado. Se houver registro, não gere novamente sem solicitação explícita de nova versão. Se o manifesto estiver ausente, vazio ou incompleto, trate o histórico como desconhecido; não conclua que a história nunca foi produzida.
5. Leia [regras/ROTA-GERAL.md](regras/ROTA-GERAL.md), [regras/SKILLS-E-RECURSOS.md](regras/SKILLS-E-RECURSOS.md), [regras/PADRAO-VISUAL-E-COMPOSICAO.md](regras/PADRAO-VISUAL-E-COMPOSICAO.md) e [regras/VALIDACAO-FINAL.md](regras/VALIDACAO-FINAL.md).
6. Consulte no GitHub a versão atual das skills e documentações externas indicadas, principalmente [Higgsfield Generate](https://github.com/higgsfield-ai/skills/blob/main/higgsfield-generate/SKILL.md) e, como complemento, [awesome-gpt-image-2](https://github.com/freestylefly/awesome-gpt-image-2). Verifique se a ferramenta necessária está realmente disponível antes de afirmar que a usou.
7. Gere uma única imagem final por pedido, salvo solicitação explícita de variações. Por padrão, 16:9 horizontal e Full HD mínimo (1920 × 1080); 9:16 vertical somente quando pedido.
8. Revise contexto, sequência, composição, falas, balões, caixas de narração, ortografia pt-BR, legibilidade e resolução real.
9. As imagens finais geradas devem permanecer fora do GitHub: não fazer upload, commit ou armazenamento de imagens no repositório. Se houver acesso autorizado, atualize somente registros textuais de status quando o estado mudar e confirme a gravação. A cópia individual do roteiro é opcional. Nunca diga que salvou algo sem verificar.

## Saída e conteúdo pedagógico obrigatório

Para histórias bíblicas destinadas a crianças, incluir no conteúdo editorial pelo menos três perguntas de compreensão/reflexão, específicas da história, e uma oração desenvolvida, normalmente com 4 a 7 frases, em linguagem infantil e relacionada ao ensinamento narrado. A oração deve terminar exatamente com: **“Em nome de Jesus, Amém!”**. Não usar perguntas genéricas repetidas mecanicamente.

As imagens finais não devem ser armazenadas no GitHub. O repositório mantém fontes, templates, regras e registros textuais; a imagem entregue no chat ou em outro destino autorizado não deve ser confundida com um arquivo versionado.

## Fonte narrativa e cópia opcional

A fonte principal pode ser uma coleção em `historias/historias-<nome-colecao>.md`, um arquivo de roteiro fornecido pelo usuário ou outra fonte canônica identificada no pedido/template.

- **Não é obrigatório copiar cada roteiro individual para o GitHub.** A cópia serve para rastreabilidade e pode ser criada quando útil ou solicitada.
- Se for feita uma cópia individual, use um nome claro dentro de `historias/` e mantenha a origem identificável; não substitua nem fragmente a fonte canônica sem necessidade.
- Os manifestos `historias/status-criacao-historia.<nome-colecao>.md` são registros de progresso por coleção. Atualize-os quando houver mudança real de estado e acesso de escrita autorizado; não invente registros.
- Se o roteiro necessário não estiver no repositório e não tiver sido fornecido, peça a fonte ou esclarecimento. Não fabrique contexto a partir apenas do título.

## Precedência

1. Fonte narrativa canônica: fatos, personagens, acontecimentos e sequência.
2. Template selecionado: tipo de ativo, composição e requisitos específicos.
3. Regras do projeto: qualidade, idioma, segurança e validação.
4. Skills/documentação de ferramentas: execução técnica, sem poder contradizer as fontes anteriores.
5. Manifesto de status: estado de produção confirmado, não fonte narrativa.

## Idioma e integridade

- Idioma padrão: português brasileiro (pt-BR), salvo pedido expresso em contrário.
- Revisar ortografia, acentuação, pontuação, concordância e naturalidade dos diálogos.
- Não inventar fontes, arquivos, imagens salvas, commits, estados, resolução ou execução de ferramenta.
- Uma imagem exibida no chat não prova que foi salva no GitHub.
- Se faltar fonte essencial, ferramenta operacional ou permissão necessária, declarar o bloqueio com precisão.

## Mudanças neste roteador

Este arquivo deve mudar raramente. Atualize primeiro templates, rotas especializadas e regras de validação. Se o próprio fluxo principal mudar, edite este documento e verifique todos os links internos após a alteração.
