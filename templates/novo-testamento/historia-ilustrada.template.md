# Template — história ilustrada do Novo Testamento

- **Template ID:** `TPL-HNT-HISTORIA`
- **Versão:** 1.0.0
- **Coleção:** Novo Testamento
- **Ativo de saída:** uma prancha ilustrada infantil
- **Estado do template:** INICIAL — validar em teste antes de produção aprovada

## Entrada do usuário

- **Título solicitado:** obrigatório.
- **Referência/trecho bíblico:** opcional se houver título único e inequívoco na fonte narrativa.
- **Número/ID da história:** obrigatório quando existir catalogação oficial; não inventar número.

## Fontes canônicas

1. [Histórias do Novo Testamento](../../historia-novo-testamento.md) — narrativa oficial atual na raiz.
2. [Manifesto de status do Novo Testamento](../../status-criacao-historia.novo-testamento.md) — controle de produção desta coleção. O arquivo legado `status-criacao-historia.md` não deve ser tratado como substituído até que sua migração seja conferida.
3. [Rota geral](../../regras/ROTA-GERAL.md), [skills](../../regras/SKILLS-E-RECURSOS.md), [padrão visual](../../regras/PADRAO-VISUAL-E-COMPOSICAO.md) e [validação](../../regras/VALIDACAO-FINAL.md).

Não use conhecimento geral ou memória para substituir a narrativa oficial. Se o título não localizar uma entrada exata e inequívoca, pare e peça o ID/referência que falta.

## Roteiro

1. Confirmar template ID, título oficial, número (se houver) e versão.
2. Ler a entrada narrativa completa e o status atual.
3. Bloquear a sequência: personagens, locais, ações, causa e consequência, ensinamentos e limite da história.
4. Extrair seis momentos visuais em ordem, sem acrescentar cenas não sustentadas pelo texto.
5. Escrever textos curtos, infantis, em português brasileiro; revisar ortografia e consistência entre legenda e quadro.
6. Roteamento técnico principal: `higgsfield-generate`, conforme [SKILLS-E-RECURSOS.md](../../regras/SKILLS-E-RECURSOS.md). Confirmar disponibilidade real da ferramenta.
7. Gerar uma única prancha final em uma única chamada e definir quantidade 1 se o gerador suportar. Não criar lotes ou variações.
8. Validar a imagem visualmente e registrar evidências. Não marcar aprovada sem inspeção real e arquivo salvo confirmado.

## Direção visual

- Linguagem de quadrinhos bíblicos: usar balões para falas de personagens e caixas retangulares para narração/contexto, distinguindo visualmente as duas funções.
- Não atribuir fala à pessoa errada nem apresentar paráfrases como citações literais. Respeitar a fonte narrativa e a referência bíblica.
- A imagem pode ser gerada no ChatGPT ou por CLI/ferramenta externa, conforme disponibilidade real. Registrar o método efetivamente usado no manifesto; não presumir que CLIs estão instaladas.

## Direção visual

- Paisagem próxima de 16:9.
- Cabeçalho com número/ID quando oficial e título literal.
- Exatamente seis quadros, grade duas fileiras × três colunas.
- Faixa inferior com exatamente três painéis: `O QUE APRENDEMOS`, `PERGUNTAS PARA A CRIANÇA`, `ORAÇÃO`.
- Ilustração bíblica infantil acolhedora, colorida e detalhada; texto grande, de alto contraste e legível.
- Continuidade de personagens definida pelas referências aprovadas que realmente estiverem disponíveis.
- Evitar anatomia quebrada, membros/dedos extras ou faltantes, clones involuntários, paleta fluorescente, saturação excessiva, tons de pele artificiais e texto deformado.

## Proibições

Não alterar fatos bíblicos para melhorar a composição; não copiar o conteúdo narrativo de outra história; não supor referências visuais inexistentes; não sobrescrever ativos aprovados sem autorização; não declarar uso de skill/ferramenta, salvamento ou validação sem evidência.

## Relatório final

Template ID/versão; história/título e fontes consultadas; skill/ferramenta efetivamente usada; quantidade configurada e retornada; checklist de fidelidade, composição, anatomia, cor e texto; caminho real do ativo; status de validação; pendências.
