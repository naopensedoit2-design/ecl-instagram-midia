# Mídia do Instagram — @eucaseidelafer

Imagens e vídeos dos posts do Instagram da Eu Casei de Lafer (MP Lafer 1980, casamentos e ensaios na Serra Gaúcha), com links públicos para o agendamento no Metricool.

## Calendário

| Data | Hora | Post | Formato | Metricool | Pasta |
|---|---|---|---|---|---|
| 29/10/2026 | 18:00 | Ele nasceu numa fábrica de móveis | Carrossel · 7 imagens | agendado | [P1](posts/2026-10-29_P1_historia-mplafer) |
| 05/11/2026 | 18:00 | Letícia & Marcello · a chegada | Carrossel · 6 imagens | agendado | [P2](posts/2026-11-05_P2_leticia-marcello-chegada) |
| 12/11/2026 | 18:00 | Ana & Rodrigo · pré-wedding | Carrossel · 6 imagens | agendado | [P3](posts/2026-11-12_P3_ana-rodrigo-prewedding) |
| 19/11/2026 | 18:00 | Letícia & Marcello · fim de tarde | Reel · 12 s | rascunho | [P4](posts/2026-11-19_P4_reel-leticia-marcello-fim-de-tarde) |
| 26/11/2026 | 18:00 | Daniela & Mateus · bastidores | Carrossel · 7 imagens | rascunho | [P5](posts/2026-11-26_P5_daniela-mateus-bastidores) |
| 03/12/2026 | 18:00 | Editorial Classic Bride | Carrossel · 7 imagens | rascunho | [D1](posts/2026-12-03_D1_editorial-classic-bride) |
| 10/12/2026 | 18:00 | Como reservar o Lafer | Carrossel · 6 imagens | rascunho | [D2](posts/2026-12-10_D2_como-reservar) |
| 17/12/2026 | 18:00 | Os detalhes também contam a história | Carrossel · 6 imagens | rascunho | [D3](posts/2026-12-17_D3_detalhes-leticia-marcello) |
| 24/12/2026 | 10:00 | Boas festas | Foto única | rascunho | [D4](posts/2026-12-24_D4_boas-festas) |
| 31/12/2026 | 10:00 | Obrigado por cada história | Carrossel · 6 imagens | rascunho | [D5](posts/2026-12-31_D5_obrigado-por-cada-historia) |
| Qui · 7 jan | — | E se chover no dia do ensaio? | Carrossel | ideia | — |
| Qui · 14 jan | — | O que está incluso no carro da noiva | Carrossel | ideia | — |
| Qui · 21 jan | — | Casamento de dezembro: a chegada da noiva | Carrossel | ideia | — |
| Qui · 28 jan | — | Bastidores em vídeo | Reel | ideia | — |

"agendado" = vai ao ar sozinho no horário. "rascunho" = está no Metricool esperando aprovação. A versão completa, com status e links, está em [`calendario.csv`](calendario.csv).

## Estrutura

- `posts/AAAA-MM-DD_ID_assunto/` — um post por pasta: imagens na ordem do carrossel (`01.jpg`, `02.jpg`…) ou `reel.mp4` + `capa.jpg`, e `legenda.txt` com legenda, texto alternativo, créditos e horário.
- `stories/` — telas de stories (1080 × 1920).
- `destaques/` — capas dos destaques do perfil.
- `calendario.csv` — calendário editorial com status, colaboradores e o primeiro arquivo de cada post.

## Fluxo

1. As peças são produzidas no painel do Instagram (no Claude) e aprovadas lá.
2. O script `preparar_lote.py` (kit da rotina) copia a mídia para cá, escreve as legendas e monta o lote do Metricool.
3. O Claude cria os posts no Metricool pelos links públicos daqui: aprovados vão agendados; o resto vai como rascunho.
4. O Metricool guarda a própria cópia da mídia no momento do agendamento.

## Regras

- Formato do feed 1080 × 1350; reels e stories 1080 × 1920.
- Fotos de casais só com autorização do casal e crédito do fotógrafo. O chofer não aparece nas fotos.
- Nada de preço nos posts. Até 5 hashtags.
- Os arquivos ficam públicos enquanto estiverem aqui. Depois que um post for ao ar, a pasta pode ser apagada.

Link direto de um arquivo: `https://raw.githubusercontent.com/naopensedoit2-design/ecl-instagram-midia/main/<caminho>`
