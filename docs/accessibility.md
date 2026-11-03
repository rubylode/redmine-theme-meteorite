# Contrast

Meteorite aims at WCAG 2.2 AA in dark and in the white print: 4.5:1 for text (3:1 for large text), and 3:1 for the parts of a
control that identify it (field borders) and for focus indicators.

## How it is measured

- The page check (`npm run check`) loads 29 pages in light and dark, at 1280px and 390px wide, and measures every visible
  piece of text against the colour stacked behind it. On 2026-11-02 against Redmine 7.0.2 with the Rubylode plugins mounted it
  measured 4,807 text pairs across the 58 desktop runs and 5,769 across the 58 phone runs, and found none below AA: 116 of 116
  gated runs clean.
- The tokens, one pair at a time, below (`tokens.css` for the white print and the dark values that follow it in the same file).
  The check skips text over a gradient or an image (1,975 pairs on desktop and 1,195 on phone), and it does not see field borders or focus rings, so those are measured here. Chip colours are the mixes
  the stylesheet makes (`color-mix`), worked out on the colour of the row they sit on: the panel, a stripe or a hovered row.
  The header is a flat colour, so its text is measured on that colour.
- The page has a faint grid and a glow behind it, and a drawing of rings and ticks in 1px lines at 30 percent opacity in dark and
  40 percent in the white print. They are decoration, a line is thin, and the ratios below are measured against the flat colour
  of the page, the panel or the row.

## Light (the white print)

| Pair | Foreground | Background | Ratio |
|---|---|---|---|
| Body text on a panel | `#0e0f12` | `#fafaf6` | 18.32 |
| Body text on the page | `#0e0f12` | `#f6f6f1` | 17.68 |
| Body text on a sunken panel or stripe | `#0e0f12` | `#f1f1ec` | 16.91 |
| Secondary text on a panel | `#23262e` | `#fafaf6` | 14.46 |
| Muted text on the page | `#4b4f5b` | `#f6f6f1` | 7.54 |
| Muted text on a panel | `#4b4f5b` | `#fafaf6` | 7.81 |
| Muted text on a sunken panel or stripe | `#4b4f5b` | `#f1f1ec` | 7.22 |
| Muted text on a hovered row | `#4b4f5b` | `#e8f0fb` | 7.12 |
| Link on a panel | `#154a94` | `#fafaf6` | 8.23 |
| Link on a sunken panel or stripe | `#154a94` | `#f1f1ec` | 7.60 |
| Link on a hovered row | `#154a94` | `#e8f0fb` | 7.50 |
| Text on the primary | `#ffffff` | `#1b5fbf` | 6.11 |
| Text on the primary, hovered | `#ffffff` | `#154a94` | 8.61 |
| Button text | `#23262e` | `#fafaf6` | 14.46 |
| Delete button text | `#a4242d` | `#fbe9ea` | 6.26 |
| Header links | `#3a3e49` | `#f6f6f1` | 9.86 |
| Sidebar item | `#3a3e49` | `#f6f6f1` | 9.86 |
| Sidebar selected item | `#0e0f12` | `#d3dee9` | 14.05 |
| Code block (kept light) | `#0e0f12` | `#ebebe5` | 16.01 |
| Closed or up message | `#1d5a33` | `#e3f2e8` | 7.08 |
| Warning or unavailable message | `#7a4f05` | `#fbf2e1` | 6.41 |
| Success flash | `#1d5a33` | `#e7f4ec` | 7.24 |
| Warning flash | `#6f4d0b` | `#fbf2e1` | 6.89 |
| Chip New, on a panel | `#40444f` | `#e6e7e6` | 7.85 |
| Chip New, on a stripe | `#40444f` | `#dedfdd` | 7.28 |
| Chip New, on a hovered row | `#40444f` | `#d7deea` | 7.20 |
| Chip In Progress, on a panel | `#103973` | `#dbe4ee` | 8.81 |
| Chip In Progress, on a stripe | `#103973` | `#d3dde6` | 8.22 |
| Chip In Progress, on a hovered row | `#103973` | `#cbdcf3` | 8.13 |
| Chip Resolved, on a panel | `#1c532f` | `#deeade` | 7.27 |
| Chip Resolved, on a stripe | `#1c532f` | `#d6e3d6` | 6.80 |
| Chip Resolved, on a hovered row | `#1c532f` | `#cee2e3` | 6.71 |
| Chip Feedback, on a panel | `#6a490b` | `#f0e8d6` | 6.70 |
| Chip Feedback, on a stripe | `#6a490b` | `#e8e0cd` | 6.21 |
| Chip Feedback, on a hovered row | `#6a490b` | `#e0dfda` | 6.12 |
| Chip Closed, on a panel | `#2d2f37` | `#e2e2e0` | 10.29 |
| Chip Closed, on a stripe | `#2d2f37` | `#dadad8` | 9.53 |
| Chip Closed, on a hovered row | `#2d2f37` | `#d2d9e5` | 9.40 |
| Chip Rejected, on a panel | `#6c150e` | `#f0dcd7` | 9.09 |
| Chip Rejected, on a stripe | `#6c150e` | `#e8d4ce` | 8.42 |
| Chip Rejected, on a hovered row | `#6c150e` | `#e1d3db` | 8.30 |
| Chip High, on a panel | `#79530b` | `#f3ead6` | 5.74 |
| Chip High, on a stripe | `#79530b` | `#ebe3cd` | 5.37 |
| Chip High, on a hovered row | `#79530b` | `#e4e2da` | 5.30 |
| Chip Urgent, on a panel | `#78272d` | `#f3e0de` | 7.77 |
| Chip Urgent, on a stripe | `#78272d` | `#ebd8d5` | 7.20 |
| Chip Urgent, on a hovered row | `#78272d` | `#e4d8e2` | 7.16 |
| White on priority Immediate (issue page chip) | `#ffffff` | `#a4242d` | 7.32 |
| White on an avatar or initials disc | `#ffffff` | `#2a3140` | 13.03 |
| Field border on a panel (control) | `#75756b` | `#fafaf6` | 4.45 |
| Field border on the page (control) | `#75756b` | `#f6f6f1` | 4.29 |
| Focus ring on a panel | `#1b5fbf` | `#fafaf6` | 5.84 |

## Dark (the default)

| Pair | Foreground | Background | Ratio |
|---|---|---|---|
| Body text on a panel | `#eef2f8` | `#090b0f` | 17.53 |
| Body text on the page | `#eef2f8` | `#06070a` | 17.93 |
| Body text on a sunken panel or stripe | `#eef2f8` | `#0e1116` | 16.83 |
| Secondary text on a panel | `#dde3ee` | `#090b0f` | 15.28 |
| Muted text on the page | `#98a2b5` | `#06070a` | 7.84 |
| Muted text on a panel | `#98a2b5` | `#090b0f` | 7.66 |
| Muted text on a sunken panel or stripe | `#98a2b5` | `#0e1116` | 7.36 |
| Muted text on a hovered row | `#98a2b5` | `#0f2230` | 6.32 |
| Link on a panel | `#8fd0f7` | `#090b0f` | 11.75 |
| Link on a sunken panel or stripe | `#8fd0f7` | `#0e1116` | 11.29 |
| Link on a hovered row | `#8fd0f7` | `#0f2230` | 9.70 |
| Text on the primary | `#06121c` | `#a8dcff` | 12.91 |
| Text on the primary, hovered | `#06121c` | `#c7e8ff` | 14.77 |
| Button text | `#dde3ee` | `#0e1116` | 14.68 |
| Delete button text | `#ffa8b0` | `#2a1519` | 9.41 |
| Header links | `#aab3c4` | `#06070a` | 9.55 |
| Sidebar item | `#aab3c4` | `#08090d` | 9.43 |
| Sidebar selected item | `#ffffff` | `#252f39` | 13.60 |
| Code block (kept light) | `#0e1116` | `#eef2f8` | 16.83 |
| Closed or up message | `#8fd3a6` | `#10261c` | 9.15 |
| Warning or unavailable message | `#f0c67a` | `#2a2110` | 9.87 |
| Success flash | `#a6dcb9` | `#0f2a20` | 9.88 |
| Warning flash | `#f0c67a` | `#2a2110` | 9.87 |
| Chip New, on a panel | `#c6ccd6` | `#23262d` | 9.38 |
| Chip New, on a stripe | `#c6ccd6` | `#272b33` | 8.79 |
| Chip New, on a hovered row | `#c6ccd6` | `#283948` | 7.35 |
| Chip In Progress, on a panel | `#b0d7f6` | `#1b2a37` | 9.70 |
| Chip In Progress, on a stripe | `#b0d7f6` | `#1f2f3d` | 9.07 |
| Chip In Progress, on a hovered row | `#b0d7f6` | `#203d52` | 7.51 |
| Chip Resolved, on a panel | `#b0e5c6` | `#1b2e27` | 10.14 |
| Chip Resolved, on a stripe | `#b0e5c6` | `#1f332d` | 9.47 |
| Chip Resolved, on a hovered row | `#b0e5c6` | `#204143` | 7.83 |
| Chip Feedback, on a panel | `#eed49f` | `#30291b` | 9.98 |
| Chip Feedback, on a stripe | `#eed49f` | `#342e20` | 9.34 |
| Chip Feedback, on a hovered row | `#eed49f` | `#353c36` | 7.86 |
| Chip Closed, on a panel | `#b8bec9` | `#1e2228` | 8.55 |
| Chip Closed, on a stripe | `#b8bec9` | `#22262e` | 8.12 |
| Chip Closed, on a hovered row | `#b8bec9` | `#233443` | 6.84 |
| Chip Rejected, on a panel | `#f7bfc4` | `#332227` | 9.44 |
| Chip Rejected, on a stripe | `#f7bfc4` | `#37272d` | 8.86 |
| Chip Rejected, on a hovered row | `#f7bfc4` | `#383542` | 7.52 |
| Chip High, on a panel | `#eecb96` | `#302618` | 9.62 |
| Chip High, on a stripe | `#eecb96` | `#342b1e` | 9.02 |
| Chip High, on a hovered row | `#eecb96` | `#353933` | 7.63 |
| Chip Urgent, on a panel | `#f7b1b5` | `#331d22` | 8.89 |
| Chip Urgent, on a stripe | `#f7b1b5` | `#372228` | 8.38 |
| Chip Urgent, on a hovered row | `#f7b1b5` | `#38303d` | 7.18 |
| White on priority Immediate (issue page chip) | `#ffffff` | `#b3123f` | 6.83 |
| White on an avatar or initials disc | `#ffffff` | `#2a3140` | 13.03 |
| Field border on a panel (control) | `#6f7a8d` | `#090b0f` | 4.54 |
| Field border on the page (control) | `#6f7a8d` | `#06070a` | 4.65 |
| Focus ring on a panel | `#a8dcff` | `#090b0f` | 13.45 |

## Not covered

- Redmine's own avatar colours with white initials: the three that fall below 4.5:1 (red, orange, pink) are darkened; the rest
  are Redmine's. Meteorite draws every avatar as a dark disc with a ring, so white on that disc is measured above.
- Syntax highlighting inside code blocks is Redmine's, made for a light background, which is why code blocks stay light in dark.
- Colour is never the only signal: the status orbit and the priority bars sit beside the status and priority names, and the
  bars change in length with the level.
