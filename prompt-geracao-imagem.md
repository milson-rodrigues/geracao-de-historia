# Prompt de geração de imagem — rota universal

> **Versão:** 2.2.0  
> **Estado:** rota operacional com limites de armazenamento explícitos  
> **Idioma padrão:** português brasileiro (pt-BR)

Este documento substitui a antiga instrução vinculada exclusivamente às 232 histórias do Novo Testamento. O arquivo foi mantido no mesmo caminho para evitar links quebrados.

## Antes de cada geração

1. Consultar [`ROUTER-MESTRE.md`](ROUTER-MESTRE.md) no GitHub, branch `main`.
2. Ler [`regras/00-LEIA-PRIMEIRO.md`](regras/00-LEIA-PRIMEIRO.md).
3. Confirmar o Template ID em [`templates/CATALOGO.md`](templates/CATALOGO.md).
4. Ler o template exato e a fonte narrativa oficial.
5. Seguir a convenção de fonte e status indicada pelo template e pelo roteador; não presumir que um manifesto se aplica a todas as coleções.
6. Ler as regras visuais, de skill e validação.
7. Consultar a versão atual da skill Higgsfield: https://github.com/higgsfield-ai/skills/blob/main/higgsfield-generate/SKILL.md.
8. Consultar a biblioteca GPT Image 2 quando relevante: https://github.com/freestylefly/awesome-gpt-image-2.
9. Confirmar qual ferramenta de geração e quais operações reais de arquivos estão disponíveis nesta execução.

## Preparação e armazenamento das imagens

O projeto já possui sua própria pasta principal. **Não crie, renomeie ou altere a pasta do projeto.** Não fixe o nome do projeto nem use caminhos absolutos codificados no prompt.

### Destinos pretendidos

O destino depende do método realmente usado:

- **Imagem gerada no ChatGPT**
  - Em análise: `Biblioteca/<pasta-do-projeto>/imagens-analise/`
  - Aprovada: `Biblioteca/<pasta-do-projeto>/imagens-aprovadas/`
- **Imagem gerada por agente/ferramenta externa**
  - Em análise: `<pasta-do-projeto>/imagens-analise/`
  - Aprovada: `<pasta-do-projeto>/imagens-aprovadas/`

Esses caminhos descrevem a organização desejada; **não provam que o ChatGPT ou o agente consegue operar esses destinos**. A Biblioteca do ChatGPT e o sistema de arquivos local/repositório são ambientes distintos.

### Criar somente as subpastas ausentes

No destino que a ferramenta realmente consegue acessar, verifique `imagens-analise/` e `imagens-aprovadas/` antes de gerar:

| `imagens-analise/` | `imagens-aprovadas/` | Ação |
|---|---|---|
| Não existe | Não existe | Criar as duas |
| Existe | Não existe | Criar somente `imagens-aprovadas/` |
| Não existe | Existe | Criar somente `imagens-analise/` |
| Existe | Existe | Não criar nem modificar diretórios |

Não crie a pasta principal do projeto. Não recrie, limpe ou sobrescreva pastas existentes.

**Se a ferramenta não conseguir verificar ou criar pastas no destino pretendido, não simule a operação.** Informe que a preparação não foi executada e indique a ação manual necessária. Em particular, não afirme que uma imagem foi salva dentro de uma pasta da Biblioteca do ChatGPT apenas porque ela aparece como anexo na conversa.

### Regras contra duplicatas e para aprovação

1. Antes de gerar, verifique no repositório ou destino acessível se já existe uma imagem aprovada para a mesma história. Se não houver acesso para verificar, declare essa limitação; não afirme que a verificação foi concluída.
2. Uma solicitação final de geração deve produzir uma única imagem final, quantidade 1 quando houver suporte. Não gerar uma segunda imagem para tentar corrigir o local de armazenamento.
3. Use um nome estável derivado do número e título oficiais, por exemplo `hist-004_caim_e_abel.png`. Obtenha o número e o título da fonte oficial; não os invente.
4. A imagem recém-gerada deve ser encaminhada para `imagens-analise/` **somente se a ferramenta puder realmente salvar ou mover o arquivo para esse destino**. Caso contrário, apresente o arquivo gerado, identifique o destino pendente e forneça instruções de organização manual.
5. Após aprovação explícita, mover o mesmo arquivo para `imagens-aprovadas/` se houver uma ferramenta com acesso real ao arquivo e ao destino. **Mover significa não manter a imagem também na pasta de análise. Não criar uma cópia nem gerar outro arquivo apenas para simular a movimentação.**
6. Ao aprovar, preserve o nome do arquivo. Não crie uma segunda versão com sufixo de resolução, a menos que o usuário peça expressamente renomeação ou exportação adicional.
7. Se a imagem for reprovada, excluir somente o arquivo reprovado se houver acesso real e autorização operacional. Caso contrário, explicar que a exclusão precisa ser feita manualmente. Não alegar exclusão sem confirmação.
8. Não sobrescrever nem apagar imagens aprovadas. Se já existir uma imagem aprovada para a história, interromper antes de gerar e pedir orientação, salvo se o usuário tiver solicitado explicitamente uma nova versão.
9. A Biblioteca do ChatGPT pode exigir que o usuário crie pastas ou mova/organize os itens manualmente. Só declarar criação, movimentação ou exclusão concluída quando a ferramenta confirmar a operação.
10. Se houver dois arquivos semelhantes para a mesma história, não excluir nenhum automaticamente: identificar a possível duplicidade e pedir confirmação sobre qual manter.

## Regras de conteúdo e geração

- A narrativa oficial define os fatos; o template define o contexto e o formato. Nenhuma referência estética pode contradizê-los.
- Não inventar fatos, personagens, falas, citações, números, títulos ou referências.
- Usar balões para falas atribuídas a personagens e retângulos para narração/contexto quando exigido pelo template.
- Todo texto editorial deve estar em português brasileiro, com revisão de ortografia, acentuação, pontuação e concordância.
- Não impor quantidade fixa de quadros, proporção ou rodapé pedagógico se o template não exigir.
- Fazer uma única chamada de geração destinada à saída final e configurar quantidade 1 quando houver suporte.
- Não alegar ferramenta, skill, salvamento, validação, movimentação, exclusão ou mudança de status sem evidência real.

## Entrada recomendada

```text
Gerar imagem com template TPL-MOCKUP-UNIVERSAL
História: [título ou ID oficial]
Coleção: [nome da coleção]
Método preferido: ChatGPT
```

## Relatório final

Informar Template ID/versão, história e fonte oficial, skill/documentação consultada, ferramenta realmente usada, quantidade, validação realizada, arquivo gerado, destino efetivamente confirmado, caminho real, estado de aprovação e pendências. Separar claramente o destino desejado do destino confirmado.
