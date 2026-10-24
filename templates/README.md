# Templates de produção

O catálogo oficial está em [`CATALOGO.md`](CATALOGO.md). Use somente IDs cujos arquivos existam na branch `main`.

## Template disponível

- `TPL-MOCKUP-HISTORIA` — mockup de uma história bíblica em estilo de quadrinhos; aceita coleção Novo ou Antigo Testamento. Arquivo: [`mockup-template.md`](mockup-template.md).

## Como executar

```text
Gerar com template TPL-MOCKUP-HISTORIA
Coleção: Antigo Testamento
História: 001. Deus cria o mundo
```

Ou:

```text
Gerar com template TPL-MOCKUP-HISTORIA
Coleção: Novo Testamento
História: 002. O anjo Gabriel aparece a Zacarias
Método preferido: ChatGPT
```

O exemplo é apenas ilustrativo; antes da geração, confira o título e o conteúdo na fonte narrativa oficial. Não use um número/título de exemplo sem conferir a fonte.

## Como criar um novo template

Todo template deve declarar:

1. ID único e versão;
2. coleção e ativo;
3. entrada obrigatória;
4. fontes canônicas e caminhos atuais;
5. roteiro de execução;
6. regras visuais/técnicas e quantidade;
7. critérios de validação;
8. regras de status e relatório final.

Depois de criar o arquivo, atualize `CATALOGO.md` e verifique todos os links. Não listar como disponível um template cujo arquivo não exista.

## Responsabilidades

- Fonte narrativa: fatos, personagens, acontecimentos e sequência.
- Template: escopo, entrada, composição, execução e validação específica.
- Roteador mestre: aponta para os documentos operacionais.
- Rota geral: ordena o fluxo.
- Skill: auxilia a execução técnica quando realmente disponível.
- Manifesto de status: registra apenas estados confirmados.
