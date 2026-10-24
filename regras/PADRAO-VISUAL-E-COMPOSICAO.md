# Padrão visual e composição

## Princípio universal

A linguagem visual deve acompanhar a narrativa e o template selecionado. Não impor a todos os tipos de história uma contagem fixa de quadros, proporção ou painel pedagógico sem requisito explícito.

## Quadrinhos e storytelling

- Composição editorial clara, quadros sequenciais e pontos focais definidos.
- **Balões de fala:** exclusivamente para fala atribuída a personagem; posicionar o bico do balão para indicar quem fala.
- **Caixas retangulares:** para narração, contexto, local, passagem do tempo ou resumo de acontecimentos.
- Deixar evidente a diferença visual entre fala e narração.
- Ordenar os quadros e os textos para facilitar a leitura da esquerda para a direita e de cima para baixo, salvo layout intencionalmente diferente.
- Manter textos curtos e espaço suficiente dentro de balões e caixas.
- Não apresentar paráfrases como citações literais; não inventar diálogo como se fosse bíblico.
- Manter consistência das personagens entre cenas e evitar sobreposição que obscureça ações importantes.

## Idioma e revisão textual

O padrão do projeto é **português brasileiro (pt-BR)**. Títulos, diálogos, legendas, narrações e painéis devem usar ortografia brasileira, acentuação, pontuação e concordância corretas. Evitar mistura com formas do português europeu. Revisar o texto antes da geração e inspecioná-lo na imagem final.

Se o gerador deformar o texto, não considerar a imagem aprovada. Quando tecnicamente possível, criar a ilustração com áreas vazias para adicionar o texto posteriormente.

## Direção de arte

- Paleta equilibrada, luz coerente, silhuetas legíveis e composição sem excesso visual.
- Anatomia plausível: revisar mãos, dedos, braços, pernas, rostos, olhos e proporções.
- Figurino, arquitetura e cenário podem apoiar o contexto histórico, mas não devem contradizer a narrativa.
- Referências enviadas na conversa só valem como referência durante aquela sessão, salvo se estiverem arquivadas em local acessível e confirmadas.
- Biblioteca comunitária de prompts pode ajudar a encontrar estilos, mas não é uma fonte narrativa.

## Layout pedagógico

Se o template pedir prancha pedagógica padrão, aplicar seus requisitos exatos (por exemplo, seis quadros e painéis inferiores). Caso contrário, adaptar a composição ao conteúdo.


## Proporção e resolução padrão

- Se o usuário não especificar formato, produzir em **16:9 horizontal**.
- A saída raster deve ter no mínimo **1920 × 1080 (Full HD)**; usar resolução nativa maior quando disponível e apropriada.
- Produzir em **9:16 vertical, mínimo 1080 × 1920**, somente quando o usuário pedir explicitamente ou selecionar o template vertical.
- Manter variantes nomeadas e lado a lado no diretório de mockups: `mockup-template-universal.svg` (padrão horizontal) e `mockup-template-universal-9x16.svg` (vertical).
- Planejar primeiro as áreas de texto para que personagens, cenários, mãos e objetos não as encubram. O texto deve caber na composição, nunca ser escondido para caber na imagem.
