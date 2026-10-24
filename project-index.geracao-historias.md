# Índice do projeto — Geração das histórias do Novo Testamento

Catálogo de contexto para a produção das 232 pranchas ilustradas. Atualizado em: 2026-10-21.

## 1. Identificação

- **Sigla:** HNT
- **Objetivo:** produzir uma prancha infantil ilustrada para cada história do Novo Testamento, com narrativa fiel e identidade visual consistente.
- **Público:** crianças, famílias e estudos bíblicos infantis.
- **Fase atual:** produção da Parte 1 — O NASCIMENTO E A INFÂNCIA DE JESUS.
- **Local do projeto:** `N:\@Geral\_Milson\_Vendas-Ebooks\Historia Novo Testamento`

## 2. Fontes canônicas

| Arquivo/local | Função |
|---|---|
| `historia-novo-testamento.md` | Fonte narrativa oficial; não alterar durante a geração. |
| `status-criacao-historia.md` | Estado de produção e validação por história. |
| `ROTA-SKILLS-ESTUDO-BIBLICO.md` | Procedimento operacional e regras de segurança. |
| `prompt-geracao-imagem.md` | Modelo de prompt, direção visual e critérios editoriais. |
| `imagens/001-*.png` e `imagens/002-*.png` | Referências visuais aprovadas. |
| `.agents/skills/` | Skills locais usadas como base de execução. |

## 3. Regra de produção

- Cada número corresponde a uma história e a uma imagem independente.
- O intervalo 003–022 contém **20 histórias**.
- Cada história deve ter exatamente seis quadros narrativos e três painéis pedagógicos inferiores.
- O fluxo é individual: mockup único para aprovação; depois, mediante aprovação explícita, uma única imagem final.
- Não gerar lote, variantes ou chamadas paralelas.
- Não misturar acontecimentos de histórias vizinhas.

## 4. Direção visual aprovada

- Prancha horizontal 16:9, página contínua, sem dobra central.
- Moldura de pergaminho dourado, folhagens verdes e ornamentos orgânicos.
- Cabeçalho em pergaminho enrolado com `HISTÓRIA NNN` e título oficial literal.
- Grade 3×2: cada quadro tem título temático, ilustração e caixa de narrativa legível integrada.
- Rodapé com `O QUE APRENDEMOS`, `PERGUNTAS PARA A CRIANÇA` e `ORAÇÃO`.
- Ilustração 3D infantil polida, expressiva, detalhada e acolhedora; paleta creme, dourado, castanho, azul e verde.
- Texto em português brasileiro, com acentuação e margens seguras.

## 5. Mapa da Parte 1

| Faixa | Histórias | Estado conhecido |
|---|---:|---|
| Parte 1 — O NASCIMENTO E A INFÂNCIA DE JESUS | 001–022 | 001 e 002 concluídas; 003–022 em produção individual |

## 6. Convenções de arquivo

- Imagens finais: `imagens/NNN-slug-do-titulo-oficial.png`.
- Não criar `v2`, `final2`, `nova` ou duplicatas.
- Só marcar `CONCLUIDA | APROVADA` depois de validar e confirmar o salvamento.

## 7. Executor e skills

- **Executor atual:** geração nativa de imagens do Codex.
- **Base de direção:** `.agents/skills/higgsfield-generate/SKILL.md`, sem instalar ou executar a CLI Higgsfield.
- **Skill de imagem:** `imagegen`, usando geração nativa e referências locais quando necessário.

## 8. Próximo trabalho

Iniciar a História 003 — `Isabel descobre que está grávida`, com conteúdo exclusivo: Isabel, Zacarias, gravidez, alegria e seis meses de gravidez. É proibido inserir Gabriel, Maria, anúncio do nascimento de Jesus, Herodes, magos ou fuga para o Egito.
