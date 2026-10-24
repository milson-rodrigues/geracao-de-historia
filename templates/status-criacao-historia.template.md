# Template universal — status de criação

**Versão:** 1.1.1  
**Uso:** esquema para manifestos de produção de qualquer coleção/história.  
**Não é um manifesto preenchido e não prova que nenhum ativo foi produzido.**

## Convenção de arquivos

Para o mesmo identificador `<nome-historia>`:

- Fonte narrativa: `historias/historias-<nome-historia>.md`
- Status: `historias/status-criacao-historia.<nome-historia>.md`

O identificador deve ser igual, minúsculo, sem espaços e preferencialmente separado por hífens. Confira os caminhos reais na árvore atual do GitHub antes de usar ou criar um manifesto.

## Regras

- Manter um registro por história; não duplicar IDs.
- Copiar número e título exatamente da fonte narrativa oficial.
- Registrar referência de origem somente quando confirmada na fonte.
- Todo texto editorial deve usar **português brasileiro (pt-BR)**, salvo pedido expresso de outro idioma. Revisar ortografia, acentuação, pontuação e concordância.
- Nunca inferir que uma imagem foi gerada, salva ou aprovada.
- Preencher o caminho final apenas depois de confirmar que o arquivo existe e abre.
- `APROVADA` só após inspeção da imagem final; uma imagem exibida no chat não prova que foi salva no GitHub.
- Registrar o método de geração real: ChatGPT, CLI/ferramenta externa específica ou `NÃO DEFINIDO`.
- Se houver impedimento, descrever a pendência e usar `BLOQUEADA`.
- Atualizar somente os registros afetados e conferir o manifesto após a mudança.

## Estados permitidos

| Estado | Significado |
|---|---|
| `PENDENTE` | Ainda não iniciada. |
| `EM_PREPARACAO` | Fonte, roteiro ou prompt em preparação. |
| `PRONTA_PARA_GERACAO` | Requisitos conferidos. |
| `EM_GERACAO` | Geração em andamento. |
| `GERADA_A_VALIDAR` | Saída gerada, aguardando inspeção. |
| `AJUSTES_NECESSARIOS` | Saída inspecionada que requer correções. |
| `APROVADA` | Arquivo final inspecionado, validado e caminho confirmado. |
| `BLOQUEADA` | Dependência essencial impede continuar. |

## Tabela-base para cada manifesto

| ID | Título oficial | Referência | Estado | Método de geração | Prompt/execução | Arquivo final | Validação | Pendências |
|---:|---|---|---|---|---|---|---|---|
