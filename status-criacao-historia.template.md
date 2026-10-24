# Template — status de criação de histórias

**Versão:** 1.0.0  
**Finalidade:** modelo estrutural para os manifestos de produção do Novo e do Antigo Testamento.  
**Este arquivo é um esquema; não é o status real de nenhuma história.**

## Regras de manutenção

- Manter um registro por história e não duplicar IDs.
- Copiar número e título exatamente da fonte narrativa oficial da coleção.
- Registrar a referência bíblica somente quando indicada ou verificada na fonte.
- Não inferir que uma imagem foi gerada, salva ou aprovada.
- O caminho do arquivo final só pode ser preenchido depois de confirmar que o arquivo existe e abre.
- Usar `APROVADA` apenas após validar a imagem final; uma imagem exibida no chat não prova que foi salva no GitHub.
- Registrar se a geração foi feita pelo ChatGPT, por uma CLI/ferramenta externa ou por outro fluxo real. Não registrar ferramentas que não foram utilizadas.
- Se houver bloqueio narrativo, técnico ou de autorização, descrever a pendência e usar `BLOQUEADA`.
- Atualizar somente a linha da história correspondente e conferir o manifesto após a alteração.

## Estados permitidos

| Estado | Significado |
|---|---|
| `PENDENTE` | Ainda não foi iniciada; pode seguir para análise. |
| `EM_PREPARACAO` | Fonte narrativa, roteiro visual ou prompt estão sendo preparados. |
| `PRONTA_PARA_GERACAO` | Fonte, layout e requisitos foram verificados. |
| `EM_GERACAO` | A ferramenta está gerando o ativo. |
| `GERADA_A_VALIDAR` | Existe uma saída gerada que aguarda inspeção. |
| `AJUSTES_NECESSARIOS` | A saída foi inspecionada e precisa ser corrigida. |
| `APROVADA` | Imagem final validada e caminho real confirmado. |
| `BLOQUEADA` | Uma dependência essencial impede continuar. |

## Campos do registro

| Campo | Regra |
|---|---|
| ID | Número/ID oficial da história, copiado da fonte. |
| Título oficial | Copiado sem alteração da fonte narrativa. |
| Referência bíblica | Referência explicitamente informada ou verificada. |
| Estado | Um dos estados permitidos acima. |
| Método de geração | ChatGPT, CLI/ferramenta específica ou `NÃO DEFINIDO`; registrar somente o método real. |
| Prompt/execução | Caminho do prompt ou identificador de execução, se existir. Não inventar logs. |
| Arquivo final | Caminho relativo confirmado no repositório; `—` se não estiver salvo. |
| Validação | `NÃO_INICIADA`, `PENDENTE`, `APROVADA` ou `REPROVADA`. |
| Pendências/observações | Falhas, dúvidas e próximos passos objetivos. |

## Tabela-base

Copiar esta estrutura para o manifesto de cada coleção e preencher os registros a partir da fonte oficial:

| ID | Título oficial | Referência bíblica | Estado | Método de geração | Prompt/execução | Arquivo final | Validação | Pendências/observações |
|---:|---|---|---|---|---|---|---|---|
