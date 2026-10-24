# Prompt de geração de imagem — rota universal

> **Versão:** 2.1.0  
> **Estado:** rota operacional alinhada ao Template ID universal e às regras de armazenamento  
> **Idioma padrão:** português brasileiro (pt-BR)

Este documento substitui a antiga instrução vinculada exclusivamente às 232 histórias do Novo Testamento. O arquivo foi mantido no mesmo caminho para evitar links quebrados.

## Antes de cada geração

1. Consultar [`ROUTER-MESTRE.md`](ROUTER-MESTRE.md) no GitHub, branch `main`.
2. Ler [`regras/00-LEIA-PRIMEIRO.md`](regras/00-LEIA-PRIMEIRO.md).
3. Confirmar o Template ID em [`templates/CATALOGO.md`](templates/CATALOGO.md).
4. Ler o template exato e a fonte narrativa oficial.
5. Seguir a convenção:
   - Fonte: `historias/historias-<nome-historia>.md`
   - Status: `historias/status-criacao-historia.<nome-historia>.md`
6. Ler as regras visuais, de skill e validação.
7. Consultar a versão atual da skill Higgsfield no GitHub: https://github.com/higgsfield-ai/skills/blob/main/higgsfield-generate/SKILL.md.
8. Consultar a biblioteca GPT Image 2 quando ela puder ajudar a escolher estilo ou estruturar o prompt: https://github.com/freestylefly/awesome-gpt-image-2.
9. Confirmar se o método real de geração (ChatGPT ou CLI externa) está disponível.

## Preparação e armazenamento das imagens

O projeto já possui sua própria pasta principal. **Não crie, renomeie ou altere a pasta do projeto.** Não fixe o nome do projeto nem use caminhos absolutos codificados no prompt.

O destino depende do método realmente usado:

- **Imagem gerada no ChatGPT**
  - Em análise: `Biblioteca/<pasta-do-projeto>/imagens-analise/`
  - Aprovada: `Biblioteca/<pasta-do-projeto>/imagens-aprovadas/`
- **Imagem gerada por agente/ferramenta externa**
  - Em análise: `<pasta-do-projeto>/imagens-analise/`
  - Aprovada: `<pasta-do-projeto>/imagens-aprovadas/`

Antes da geração, verifique a existência das duas subpastas no destino correspondente e aplique exatamente esta lógica:

| `imagens-analise/` | `imagens-aprovadas/` | Ação |
|---|---|---|
| Não existe | Não existe | Criar as duas |
| Existe | Não existe | Criar somente `imagens-aprovadas/` |
| Não existe | Existe | Criar somente `imagens-analise/` |
| Existe | Existe | Não criar nem modificar diretórios |

Regras adicionais:

1. A imagem recém-gerada fica inicialmente em `imagens-analise/`.
2. Após aprovação explícita do usuário, mover o arquivo para `imagens-aprovadas/`; não manter uma cópia duplicada na pasta de análise.
3. Se o usuário reprovar a imagem, excluir somente essa imagem reprovada. Não afetar outros arquivos nem imagens aprovadas.
4. Antes de gerar, verificar se já existe imagem aprovada para a mesma história. Não sobrescrever nem duplicar uma imagem aprovada automaticamente.
5. Usar nomes de arquivo claros e estáveis, por exemplo `hist-002_adao_e_eva_no_jardim_do_eden.png`. Não inventar o número ou título oficial; obtê-los da fonte narrativa.
6. Se não houver permissão ou ferramenta operacional para listar, criar, mover ou excluir arquivos no destino aplicável, declarar a limitação. Não simular operações nem afirmar que o arquivo foi salvo, movido ou excluído sem confirmação.
7. A Biblioteca do ChatGPT e o sistema de arquivos do agente são destinos diferentes. Não alegar que um arquivo foi transferido entre eles sem uma operação real e confirmada.
8. A preparação de diretórios não pode limpar, recriar, sobrescrever ou excluir conteúdo existente.

## Regras do prompt

- Narrativa e template têm precedência sobre qualquer referência estética.
- Não inventar fatos, personagens, falas, citações, números, títulos ou referências.
- Balões para falas atribuídas a personagens; retângulos para narração/contexto.
- Todo texto editorial deve estar em português brasileiro, com revisão de ortografia, acentuação, pontuação e concordância.
- Não impor quantidade fixa de quadros, proporção ou rodapé pedagógico se o template não exigir.
- Uma solicitação final corresponde a uma chamada de geração destinada à saída final e quantidade 1 quando suportada.
- Não alegar ferramenta, skill, salvamento, validação ou mudança de status sem evidência real.

## Entrada recomendada

```text
Gerar imagem com template TPL-MOCKUP-UNIVERSAL
História: [título ou ID oficial]
Coleção: [nome da coleção]
Método preferido: ChatGPT
```

## Relatório

Registrar Template ID/versão, história, fonte, skill/documentação consultada, ferramenta realmente usada, quantidade, validação, destino e caminho real do arquivo, estado confirmado e pendências.
