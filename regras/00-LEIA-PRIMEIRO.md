# Estudo Bíblico — leia primeiro

**Repositório canônico:** `milson-rodrigues/geracao-de-historia`, branch `main`.

## Regra obrigatória de entrada — GitHub primeiro

`ROUTER-MESTRE.md` é o ponto de entrada estável e deve ser tratado como imutável na manutenção rotineira. Sua função é encaminhar para este documento; não duplicar nele regras operacionais. Evoluções do fluxo devem ser feitas neste arquivo ou nos documentos especializados indicados abaixo. Só alterar o roteador se o próprio contrato de navegação precisar mudar, mediante autorização explícita do usuário.

Antes de responder a qualquer pedido de geração, consulte o repositório canônico diretamente no GitHub, na branch `main`. Faça isso novamente a cada nova solicitação; não use memória, histórico de conversa ou cópias locais como substitutos dos arquivos atuais.

**Se não conseguir acessar o GitHub ou ler uma fonte essencial, pare e informe o bloqueio. Não gere imagem por suposição.** A geração só pode começar depois de concluir a sequência de leitura abaixo, identificar a história exata e verificar o status/possível duplicidade.

## Ordem de leitura

1. Este documento (`regras/00-LEIA-PRIMEIRO.md`) — executar a rota detalhada indicada pelo roteador mestre.
2. [`README.md`](../README.md) — visão geral.
3. [`templates/CATALOGO.md`](../templates/CATALOGO.md) — confirmar o template.
4. Abrir o template exato, normalmente [`templates/mockup-template.md`](../templates/mockup-template.md) para histórias em quadrinhos.
5. Consultar a fonte narrativa oficial atual em `historias/` e localizar a entrada exata pelo número e título.
6. Consultar o manifesto de status aplicável e verificar duplicidade; histórico ausente/incompleto é desconhecido.
7. Ler as regras gerais, de skills, visuais e de validação.
8. Consultar as versões atuais das skills externas no GitHub antes de gerar.

## Fluxo curto

**Pedido → localizar história → ler fonte → ler template e regras → consultar skills atuais → gerar uma imagem → validar → atualizar status se o estado mudou e houver acesso.**

O usuário pode pedir em linguagem natural, por exemplo: `Gere a imagem da história. Título: 001 - Deus cria o mundo. Coleção: antigo-testamento.` Não exigir que ele conheça IDs internos se o objetivo estiver claro.

## Fontes e cópia opcional

As coleções narrativas vivem em `historias/historias-<nome-colecao>.md`. Os nomes atualmente encontrados incluem `historias-novo-testamento.md` e `historias-antigo-testamento.md`; confirme sempre a árvore atual do GitHub.

Copiar um roteiro para um arquivo individual em `historias/` é **opcional** e serve para facilitar rastreio. Não obrigar a criar `historias/historia-<nome>.md` para cada pedido. Se o usuário fornecer um roteiro individual, use-o como fonte da tarefa e copie-o para o GitHub apenas quando isso for útil ou solicitado, preservando a origem e sem sobrescrever arquivos existentes sem revisão.

Os manifestos `historias/status-criacao-historia.<nome-colecao>.md` rastreiam o progresso por coleção. Atualize o manifesto relevante quando o estado de produção realmente mudar, se houver acesso autorizado. Não invente estados nem afirme que houve atualização sem verificar o arquivo no GitHub.

## Verificação de duplicidade e persistência

- Consulte o manifesto da coleção antes de gerar e procure o ID da história.
- Se houver registro de imagem já gerada, validada ou aprovada, não repetir automaticamente; solicitar confirmação se o usuário quiser uma nova versão.
- Manifesto ausente ou sem registro significa histórico desconhecido, não prova de que a história nunca foi produzida.
- Nunca enviar imagens finais ao GitHub. O repositório recebe apenas alterações textuais autorizadas, como regras e status.

## Integridade

- Preserve número, título, personagens, referência bíblica e sequência da fonte.
- Escreva e revise textos em português brasileiro.
- Não invente arquivos, referências, imagens, commits ou resultados de ferramentas.
- A existência de uma skill no GitHub não prova que o CLI ou integração esteja operacional.
- Se faltar a fonte essencial, peça o arquivo ou esclarecimento em vez de completar por memória.
- Não mover nem apagar fontes canônicas sem necessidade e sem verificar impactos.

## Padrão de proporção e qualidade

Por padrão, imagem horizontal 16:9, mínimo 1920 × 1080 (Full HD); prefira resolução maior quando a ferramenta suportar. Use 9:16 vertical (mínimo 1080 × 1920) somente se o usuário pedir explicitamente. Verifique dimensões reais antes de declarar a resolução final.
