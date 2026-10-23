# ROTA-GERAL — Projeto Estudo Bíblico

- Versão: 1.0.0
- Status: regra operacional
- Idioma: português brasileiro
- Fonte oficial: branch `main` deste repositório

## Objetivo

Orientar a criação e validação consistente de pranchas ilustradas infantis, evitando erros anatômicos, repetição involuntária de pessoas/cenas, saturação fora do padrão, contaminação narrativa e registros falsos de conclusão.

## Estrutura oficial

- `historias/novo-testamento.md`: narrativa do Novo Testamento.
- `historias/antigo-testamento.md`: narrativa do Antigo Testamento.
- `regras/ROTA-GERAL.md`: este roteador.
- `regras/PADRAO-VISUAL.md`: direção visual canônica.
- `regras/VALIDACAO-ANATOMICA.md`: critérios de anatomia.
- `regras/VALIDACAO-VISUAL.md`: cor, contraste, pele, iluminação e legibilidade.
- `regras/CONTINUIDADE-PERSONAGENS.md`: identidade consistente de personagens.
- `regras/ANTI-REPETICAO.md`: duplicações e contaminação entre histórias.
- `regras/ROTEIRO-E-COMPOSICAO.md`: seis quadros e três painéis pedagógicos.
- `regras/VALIDACAO-FINAL.md`: checklist de aprovação/reprovação.
- `regras/SKILLS-E-REFERENCIAS.md`: fontes externas e requisitos de disponibilidade.
- `status-criacao-historia.md`: registro oficial de progresso.
- `imagens/`: destino dos ativos finais aprovados e referências visuais canônicas.

Os documentos existentes na raiz serão preservados durante a transição. Não mova, apague ou renomeie arquivos existentes sem revisar links e dependências.

## Ordem obrigatória antes de qualquer geração

1. Identificar exatamente testamento/coleção e número solicitado.
2. Ler diretamente no GitHub, na branch `main`, a fonte narrativa aplicável e `status-criacao-historia.md`.
3. Ler este roteador e os documentos especializados listados acima. Se algum arquivo ainda não existir ou não puder ser lido, registrar o bloqueio; não afirmar que foi consultado.
4. Comparar número e título literal entre fonte e status. Se houver divergência, parar.
5. Verificar estado de produção e existência do arquivo canônico. Respeitar o fluxo de mockup/aprovação definido nas regras atuais. Não sobrescrever nem apagar imagem aprovada sem autorização.
6. Quando acessíveis, inspecionar visualmente as referências oficiais 001 e 002. Referências visuais determinam estilo, nunca conteúdo narrativo.
7. Criar o bloco `ROTEIRO BLOQUEADO`: número, título literal, personagens, locais, eventos, sequência, seis títulos de quadros, seis legendas e texto dos três painéis inferiores. Incluir uma lista explícita de elementos proibidos de histórias vizinhas.
8. Validar o roteiro contra a fonte antes de gerar.
9. Verificar que a ferramenta real de geração está disponível. Consultar a skill principal atual somente se o recurso e a ferramenta estiverem realmente acessíveis. Nunca fingir instalação, execução ou controle de quantidade.
10. Executar uma única chamada por comando, uma única prancha. Definir quantidade 1 se houver parâmetro. Sem lote, variações, chamadas paralelas ou retry automático.
11. Inspecionar o resultado usando `VALIDACAO-ANATOMICA.md`, `VALIDACAO-VISUAL.md`, `ANTI-REPETICAO.md`, `PADRAO-VISUAL.md` e `VALIDACAO-FINAL.md`.
12. Se houver falha material, rejeitar e parar; relatar o erro e aguardar um novo comando explícito. Não tentar corrigir por geração automática.
13. Salvar apenas no destino canônico, se a ferramenta permitir, depois de validar. Atualizar apenas a linha existente do status (ou aplicar a regra oficial para registro ausente); confirmar cada operação realmente executada.
14. Informar resultado real, arquivo/path confirmado e qualquer etapa pendente. Exibir uma imagem no chat não prova salvamento.

## Bloqueios obrigatórios

Parar sem gerar se:
- GitHub/branch principal ou arquivos oficiais estiverem inacessíveis;
- número/título divergir entre fonte e status;
- houver outro processo registrado como `EM_GERACAO`;
- existir imagem final sem registro e não for possível reconciliar com segurança;
- skill/ferramenta for requisito explícito da solicitação e não estiver disponível;
- as regras visuais especializadas exigidas não puderem ser consultadas.

Se a geração estiver disponível por outra ferramenta real, a indisponibilidade de uma skill opcional não deve ser escondida: informar a limitação e só prosseguir se o procedimento permitir.

## Fonte de verdade e precedência

1. Arquivo narrativo correspondente define o que contar.
2. `status-criacao-historia.md` decide se pode iniciar e qual é o estado atual.
3. Regras especializadas em `regras/` definem controles de composição e qualidade.
4. Referências visuais aprovadas definem apenas estilo e continuidade visual.
5. Skills externas apoiam a execução e não podem contrariar as regras anteriores.

## Regra de integridade

Não inventar consulta, skill, chamada, validação, salvamento ou atualização. Uma conclusão só é válida quando a imagem final foi visualmente validada, o arquivo foi salvo no destino canônico e o status foi atualizado com confirmação.
