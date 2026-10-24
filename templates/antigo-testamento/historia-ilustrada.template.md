# Template — história ilustrada do Antigo Testamento

- **Template ID:** `TPL-HAT-HISTORIA`
- **Versão:** 1.0.0
- **Coleção:** Antigo Testamento
- **Ativo de saída:** uma prancha ilustrada infantil
- **Estado do template:** INICIAL — validar em teste antes de produção aprovada

## Entrada do usuário

- **Título solicitado:** obrigatório.
- **Referência/trecho bíblico:** opcional quando o título tiver correspondência inequívoca.
- **Número/ID oficial:** obrigatório se já houver catálogo; não inventar.

## Fontes canônicas

Usar o documento narrativo do Antigo Testamento atualmente existente em [historias-antigo-testamento.md](../../historias-antigo-testamento.md). Controlar o progresso em [status-criacao-historia.antigo-testamento.md](../../status-criacao-historia.antigo-testamento.md), usando o esquema [status-criacao-historia.template.md](../../status-criacao-historia.template.md). Não presumir que a fonte tenha o mesmo esquema de IDs ou status do Novo Testamento. Antes da produção, verificar se há catálogo/status específico para esta coleção. Se faltar um controle necessário, registrar como pendência e não inventar uma linha.

Consultar também [rota geral](../../regras/ROTA-GERAL.md), [skills](../../regras/SKILLS-E-RECURSOS.md), [padrão visual](../../regras/PADRAO-VISUAL-E-COMPOSICAO.md) e [validação](../../regras/VALIDACAO-FINAL.md).

## Roteiro

1. Confirmar o ID `TPL-HAT-HISTORIA` e o título solicitado.
2. Encontrar a narrativa completa no arquivo oficial do Antigo Testamento e identificar a unidade exata.
3. Verificar se há status/catalogação para essa entrada. Se não houver ou houver ambiguidade, não criar números nem assumir autorização de produção; registrar a pendência e pedir referência mínima.
4. Bloquear personagens, acontecimentos, contexto e ordem narrativa.
5. Extrair seis momentos visuais em sequência fiel, sem inventar acontecimentos.
6. Preparar textos curtos e legíveis em português brasileiro.
7. Roteamento técnico principal: `higgsfield-generate`, conforme [SKILLS-E-RECURSOS.md](../../regras/SKILLS-E-RECURSOS.md), se disponível.
8. Fazer uma única chamada destinada a uma única prancha final; configurar quantidade 1 se suportada.
9. Inspecionar e validar a imagem; registrar só resultados verificados.

## Direção visual

- Linguagem de quadrinhos bíblicos: balões para falas de personagens e caixas retangulares para narração/contexto; manter clara a distinção entre fala e narração.
- Não inventar falas como citações bíblicas nem atribuir fala a personagem incorreta. Seguir a fonte narrativa oficial.
- A imagem pode ser gerada no ChatGPT ou por CLI/ferramenta externa, se disponível. Registrar apenas o método realmente utilizado.

## Direção visual

Manter o padrão global infantil: prancha horizontal próxima de 16:9, cabeçalho oficial, seis quadros em grade 3×2 e três painéis pedagógicos no rodapé. Garantir contexto cultural/histórico coerente sem alterar a narrativa. Personagens e cenários devem ser distintos quando o texto os define como distintos.

## Proibições e relatório

Não misturar narrativas de testamentos/coleções; não usar o arquivo de status do Novo Testamento como se cobrisse o Antigo sem prova; não inventar fonte, número, status, referência ou resultado. O relatório final deve identificar template, fonte narrativa, status/catalogação consultados, ferramenta e skill reais, validação, caminho salvo e pendências.
