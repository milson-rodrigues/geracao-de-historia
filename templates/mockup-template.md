# Template de mockup — história bíblica em quadrinhos

- **Template ID:** `TPL-MOCKUP-HISTORIA`
- **Versão:** 1.0.0
- **Estado:** INICIAL — precisa de teste visual
- **Ativo:** mockup/prancha ilustrada de uma história bíblica
- **Idioma:** português brasileiro
- **Saída:** uma imagem final por solicitação; quantidade 1 quando o gerador permitir

## 1. Objetivo

Produzir um mockup de página em estilo de história em quadrinhos bíblica. A composição combina ilustrações narrativas, balões para falas de personagens e caixas retangulares para narração/contexto.

O mockup é um modelo visual de produção, não uma fonte narrativa. A fonte oficial da coleção determina os acontecimentos, personagens, título, sequência e referências.

## 2. Entrada obrigatória

O usuário informa:

- **Coleção:** Novo Testamento ou Antigo Testamento.
- **História:** número e/ou título oficial.
- **Referência visual:** opcional; pode ser uma imagem anexada à conversa ou um arquivo acessível no repositório.
- **Método preferido:** ChatGPT ou CLI/ferramenta externa; se não especificado, verificar as opções reais disponíveis e escolher a opção operacional adequada.

Se a coleção ou a história estiver ambígua, faça uma pergunta objetiva antes de continuar. Não invente número, título ou referência bíblica.

## 3. Fontes canônicas e rotas

1. Roteador estável: [`ROUTER-MESTRE.md`](../ROUTER-MESTRE.md).
2. Fonte do Novo Testamento: [`historias/historia-novo-testamento.md`](../historias/historia-novo-testamento.md).
3. Fonte do Antigo Testamento: [`historias/historias-antigo-testamento.md`](../historias/historias-antigo-testamento.md).
4. Regras visuais: [`regras/PADRAO-VISUAL-E-COMPOSICAO.md`](../regras/PADRAO-VISUAL-E-COMPOSICAO.md).
5. Validação: [`regras/VALIDACAO-FINAL.md`](../regras/VALIDACAO-FINAL.md).
6. Skills e ferramentas: [`regras/SKILLS-E-RECURSOS.md`](../regras/SKILLS-E-RECURSOS.md).
7. Manifesto de status, quando o trabalho envolver rastreamento de produção:
   - Novo Testamento: [`historias/status-criacao-historia.novo-testamento.md`](../historias/status-criacao-historia.novo-testamento.md).
   - Antigo Testamento: [`historias/status-criacao-historia.antigo-testamento.md`](../historias/status-criacao-historia.antigo-testamento.md).
   - Esquema: [`templates/status-criacao-historia.template.md`](status-criacao-historia.template.md).

Antes de produzir, consulte a versão atual dos arquivos no GitHub. Não confie em caminhos antigos da raiz. Se a fonte necessária não estiver acessível, pare e informe o bloqueio.

## 4. Bloqueio narrativo

Antes de compor o mockup, extraia da entrada oficial:

- número e título exatos;
- personagens citados;
- acontecimentos e sua sequência;
- referência bíblica, se fornecida pela fonte;
- ensinamento, somente quando presente ou explicitamente requerido.

Os tópicos da fonte narrativa não são necessariamente citações bíblicas literais. Não invente acontecimentos, falas diretas, versículos ou atribuições de diálogo. Se a fala exata não estiver na fonte, use narração em retângulo ou uma paráfrase claramente não literal, adequada ao contexto.

## 5. Direção visual e composição

- Estilo de quadrinhos bíblicos coloridos, com cenas expressivas e leitura sequencial clara.
- Usar **balões de fala** para diálogo de personagens; o balão deve apontar visualmente para quem fala.
- Usar **caixas retangulares de narração** para contexto, lugar, passagem do tempo e descrição de acontecimentos.
- Diferenciar graficamente balões e narração; não colocar texto narrativo em um balão como se fosse fala de personagem.
- Manter os textos curtos, em português brasileiro, com acentuação correta e alto contraste.
- Organizar quadros, balões e caixas na ordem natural de leitura; evitar cruzamentos e sobreposição de textos.
- Preservar rostos, mãos e ações importantes sem obstrução.
- Manter continuidade de roupas, idade aparente, aparência e objetos entre quadros da mesma história.
- Respeitar o contexto histórico sem transformar suposições visuais em fatos narrativos.
- Não exigir automaticamente seis quadros, proporção 16:9 ou rodapé pedagógico: aplicar esse layout apenas se o usuário ou outro template ativo o solicitar.
- Se o texto renderizado pelo gerador ficar ilegível, registrar a falha. Quando possível, preferir ilustração com espaços reservados para inserir o texto depois, em vez de aceitar letras defeituosas.

## 6. Método de geração

A imagem pode ser criada:

- diretamente pelo gerador de imagens do ChatGPT, se disponível na sessão; ou
- por CLI/ferramenta externa, se instalada, configurada, autorizada e operacional.

Rota principal de skill: [`higgsfield-generate`](https://github.com/higgsfield-ai/skills/blob/main/higgsfield-generate/SKILL.md). Consultar a versão atual quando acessível. A existência da skill no GitHub não prova que a CLI ou credenciais estão disponíveis.

Não alegar que uma ferramenta foi usada sem evidência. Uma imagem mostrada na conversa não prova que foi salva no GitHub.

## 7. Quantidade e saída

- Uma solicitação de mockup final corresponde a uma saída final.
- Configurar quantidade 1 quando houver suporte.
- Não gerar variações ou lotes, a menos que o usuário peça explicitamente.
- Não declarar um caminho de arquivo final até confirmar que o arquivo foi realmente salvo e pode ser aberto.
- Se a ferramenta gerar a imagem apenas na conversa, informar que o salvamento no repositório continua pendente.

## 8. Validação obrigatória

- [ ] Número e título conferem com a fonte oficial.
- [ ] A cena corresponde à coleção/testamento selecionado.
- [ ] Personagens e acontecimentos são fiéis à narrativa.
- [ ] A sequência visual é compreensível.
- [ ] Balões correspondem às personagens que falam.
- [ ] Caixas retangulares contêm narração/contexto, não falas falsamente atribuídas.
- [ ] Textos estão em português brasileiro e legíveis.
- [ ] Não há anomalias anatômicas graves nem sobreposições involuntárias.
- [ ] A composição mantém espaços adequados para texto.
- [ ] O método de geração foi registrado corretamente.
- [ ] O arquivo final e seu caminho foram confirmados, caso se declare salvamento.

Estado final possível: `APROVADA`, `AJUSTES_NECESSARIOS`, `PENDENTE` ou `BLOQUEADA`. Nunca marcar como aprovada somente porque o gerador retornou uma imagem.

## 9. Relatório de execução

Informar:

- Template ID/versão;
- coleção, número e título oficial;
- fontes consultadas;
- método de geração e ferramenta realmente utilizada;
- quantidade configurada e quantidade retornada;
- resultado da validação;
- caminho real do arquivo, se salvo;
- status alterado, se houver confirmação;
- pendências restantes.
