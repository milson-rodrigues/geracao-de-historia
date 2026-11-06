# Validação final de ativos visuais

A geração não equivale a aprovação. Preencha a checklist conforme o tipo de ativo e evidências observadas no arquivo final. A sequência operacional vigente está em [00_GUIA-DE-CONFIGURACAO.md](../00_GUIA-DE-CONFIGURACAO.md).

## Checklist comum

- [ ] Template ID, título, coleção e fonte correspondem ao pedido.
- [ ] Os fatos, personagens e eventos seguem a fonte narrativa correta.
- [ ] A composição é legível e apropriada ao tipo de ativo.
- [ ] Balões de fala identificam corretamente quem está falando.
- [ ] Caixas retangulares são usadas para narração/contexto.
- [ ] Textos usam português brasileiro correto: ortografia, acentos, pontuação e concordância.
- [ ] Não há texto deformado ou ininteligível apresentado como aprovado.
- [ ] Anatomia, rostos, mãos e objetos não têm falhas graves.
- [ ] Paleta, contraste e continuidade visual são coerentes.
- [ ] Requisitos específicos do template foram atendidos.
- [ ] O arquivo está realmente salvo e abre, quando se declara salvamento.
- [ ] O manifesto da mesma coleção foi atualizado e relido, se houve alteração de status.

## Verificações obrigatórias antes da geração

- [ ] O bootstrap estável `ROUTER-MESTRE.md` e o guia mutável `00_GUIA-DE-CONFIGURACAO.md` foram consultados no GitHub, branch `main`.
- [ ] A ordem vigente do guia foi seguida; o roteador mestre não foi alterado para manutenção operacional.
- [ ] O ID e título foram confirmados na fonte oficial.
- [ ] O manifesto da coleção foi consultado para detectar geração anterior ou aprovação.
- [ ] Se o histórico estava ausente/incompleto, foi marcado como desconhecido, sem presumir ausência de geração.
- [ ] A geração não foi iniciada quando uma fonte essencial ou o GitHub estava inacessível.

## Validação pedagógica de histórias infantis

- [ ] Existem pelo menos três perguntas específicas de compreensão/reflexão.
- [ ] A oração tem desenvolvimento adequado (normalmente 4 a 7 frases), linguagem infantil e relação com a história.
- [ ] A oração termina exatamente com **“Em nome de Jesus, Amém!”**.
- [ ] Nenhuma pergunta ou trecho da oração foi removido para acomodar o layout; se necessário, o conteúdo completo acompanha a imagem.

## Política de armazenamento

- [ ] A imagem final não foi enviada nem commitada no GitHub.
- [ ] Qualquer alteração no GitHub limita-se a arquivos textuais autorizados, como manifesto de status.

## Para pranchas que exijam layout fixo

Aplicar somente quando o template exigir seis quadros em grade 3×2 e três painéis inferiores (`O QUE APRENDEMOS`, `PERGUNTAS PARA A CRIANÇA`, `ORAÇÃO`). Não impor esse formato a um mockup universal ou a sprites por padrão.

## Decisão

- **APROVADA:** critérios críticos atendidos e arquivo final inspecionado; salvamento confirmado se declarado.
- **AJUSTES_NECESSARIOS:** falhas corrigíveis detectadas.
- **PENDENTE:** aguardando avaliação ou evidência.
- **BLOQUEADA:** fonte, ferramenta ou dependência essencial indisponível.

Nunca marcar como aprovada só porque uma imagem foi exibida no chat.

## Proporção e resolução

- [ ] Proporção correta: 16:9 por padrão; 9:16 somente se solicitado.
- [ ] Imagem raster final tem no mínimo 1920 × 1080 para 16:9 ou 1080 × 1920 para 9:16.
- [ ] Se a ferramenta oferecer resolução nativa maior adequada, foi considerada/preferida.
- [ ] Arquivo salvo sob o nome e caminho corretos, sem confundir as duas variantes de mockup.
- [ ] O texto permanece legível e totalmente desobstruído pelos personagens e elementos de cena.


## Gate de pré-geração — validação obrigatória

- [ ] Consulta ao GitHub, fontes, template e manifesto concluída antes de qualquer operação visual.
- [ ] A saída de história foi tratada como prancha em quadrinhos, sem perguntar se o usuário prefere ilustração única.
- [ ] Requisitos especiais não definidos que alterem materialmente a prancha foram esclarecidos antes da geração, quando aplicável.
- [ ] Nenhuma ferramenta de geração foi chamada antes da confirmação necessária.
- [ ] Nenhuma imagem ilustrativa, thumbnail, rascunho ou referência externa foi pesquisada/exibida como prévia não solicitada.
- [ ] Se referências externas foram explicitamente solicitadas, estão identificadas como referências, com origem, e não como resultado gerado.
- [ ] Foi realizada apenas uma chamada de geração final, com quantidade 1 quando suportada.
- [ ] Nenhuma imagem com marca d'água ou de terceiros foi apresentada como ativo gerado pelo projeto.

Falha em qualquer item aplicável impede classificar o ativo como aprovado.


## Validação específica do layout de referência

- [ ] Canvas único horizontal 16:9, sem moldura de interface ou margens externas.
- [ ] Cabeçalho em pergaminho contém número, título oficial e referência bíblica.
- [ ] Existem seis quadros narrativos em grade 3×2, em sequência cronológica.
- [ ] Cada quadro tem narração legível em área reservada, sem encobrir a ação.
- [ ] Os três painéis inferiores estão presentes e alinhados: O QUE APRENDEMOS, PERGUNTAS PARA A CRIANÇA e ORAÇÃO.
- [ ] Os painéis pedagógicos têm cabeçalhos coloridos distintos, ícones temáticos e contraste adequado.
- [ ] Há pelo menos três perguntas específicas da história.
- [ ] A oração está desenvolvida e termina exatamente com “Em nome de Jesus, Amém!”.
- [ ] Ilustração, personagens, cenários e sequência são fiéis à fonte oficial, sem elementos copiados da história-exemplo.
- [ ] Não há placeholders, marca d'água, texto de interface ou conteúdo de outra história.
