# Prompt de geração de imagem — rota universal

> **Versão:** 2.0.0  
> **Estado:** rota operacional alinhada ao Template ID universal  
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
Gerar mockup com template TPL-MOCKUP-UNIVERSAL
História: [título ou ID oficial]
Fonte: historias/historias-<nome-historia>.md
Método preferido: ChatGPT
```

## Relatório

Registrar Template ID/versão, história, fonte, skill/documentação consultada, ferramenta realmente usada, quantidade, validação, caminho real do arquivo, estado confirmado e pendências.
