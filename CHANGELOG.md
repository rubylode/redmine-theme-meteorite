# Changelog

All notable changes to this theme. The format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).

## [2.0.3] - 2026-11-03

### Added

- The theme now has a Rubylode thumbnail, shown at the top of the README. The theme itself is unchanged.

## [2.0.2] - 2026-11-03

### Changed

- The chart colours are now a muted editorial set.

## [2.0.1] - 2026-11-02

### Added

- The theme defines the chart colour tokens the Stats plugin reads.

## [2.0.0] - 2026-11-02

### Changed

- The theme is built on the shared Rubylode theme base. The single stylesheet is now `tokens.css`, `structure.css`, `plugins.css`, `sidebar-layout.css`, `light.css`, `flourishes.css`, `fonts.css`, `application.css` and `responsive.css`, and `javascripts/theme.js` holds the base script and Meteorite's own.
- Every page the other Rubylode themes cover is styled: the issue page and its history, the roadmap, My page, the wiki and its editor, spent time, Gantt, the calendar, project settings and administration, the context menu, dropdowns and pagination.
- The Rubylode plugins are styled: Home, Projects, Stats, To-do, the New issue button, Uptime Kuma, Beszel, GlitchTip and Windmill.
- Meteorite is still dark first, with the white print for a light system setting. Both sets are now tokens: the white print in `tokens.css` and the dark values in `dark.css`, built into `tokens.css` as the default and `light.css` as the system-setting override.
- The text font is Noto Sans, bundled in `meteorite/fonts/` with Noto Sans Mono, under the SIL Open Font License 1.1. The 1.0.0 stack (IBM Plex Mono, then the system monospace) is dropped. Titles keep a monospace look through `--theme-title-font`, which is Noto Sans Mono.
- Text is 16px, up from 12px, and every other size follows it (the token is `--theme-font-size`). Lists, table headings and buttons are larger than in 1.0.0 as a result.
- The navigation is the sidebar layout of the base. The search, the project switcher, the global links and your avatar are in a bar across the top, and the sidebar, 232px wide, holds the project name and its menu. In 1.0.0 all of them were in the sidebar.
- The sidebar holds the global links on pages with no project menu, such as My page and the welcome page. The sign-in page keeps the two top rows at every width.
- The selected sidebar item keeps the pale gradient and the bar at its edge. The project name keeps its wide-spaced capitals, and the tile before it is a ring.
- The accent in dark is deeper at step 6 (`#2b6cb0`), so the white text that Redmine and the plugins hard-code on the accent reads. The main button, the focus ring and the links keep the pale blue.
- The status colours in dark are lighter and a little more saturated, and Closed is a grey blue. They colour the chips on the issue page and the dots in plugin blocks.
- Avatars are a dark disc with a ring in both modes, as before.
- The drawing behind the page is a file, `images/instrument.svg`, with white lines. The white print inverts it through `--theme-instrument-filter` and draws it at 40 percent, down from 60.
- The title on a phone has less letter-spacing, so a long title wraps in fewer lines.
- Contrast was measured again in both modes: every text pair is 4.5:1 or more. See `docs/accessibility.md`.
- The workflows and `docs/ci.md` are the current ones, with the manual-run guard on `main` and a release job that runs after the check.

### Kept from 1.0.0

- The instrument drawn behind the page, the faint grid, the glow at the top left and the thin frame with a dot at each corner.
- Square corners, hairlines, dashed lines between rows and columns of a list, and the near black page.
- Status as an orbit (a ring with a point, glowing for In Progress) and priority as a row of five bars lit by level, as plain cells in the issue list.
- A small square before the tracker, a box round the group name in a grouped list, and a ring with initials in place of an assignee's name (with the name in the tooltip).
- Issues, Gantt, Calendar and Activity as tabs above the issue list, from `javascripts/theme.js`.
- Outlined fields and buttons, with the buttons in wide-spaced capitals.
- The white print for a light system setting.

### Removed

- The colour hook on status group headers (`data-group`) that the script set. The base marks those rows with a status dot instead.
- The all-monospace text and the small list text. Both are replaced by the base type scale.

### Token names changed

Custom overrides of the 1.0.0 names need the new ones. The 1.0.0 stylesheet also set Redmine's own variables (`--oc-*`, `--fonts-main`, `--color-*`) directly; they now come from the tokens.

| 1.0.0 | 2.0.0 |
|---|---|
| `--meteorite-accent-0` to `-9` | `--theme-accent-0` to `-9` |
| `--meteorite-page` | `--theme-page` |
| `--meteorite-ink` | `--theme-ink` |
| `--meteorite-radius` | `--theme-radius`, `--theme-radius-small` and the other `--theme-radius-*` |
| `--meteorite-rail` | `--theme-sidebar-background` |
| `--meteorite-rail-width` | `--theme-sidebar-width` |
| `--meteorite-rail-ink`, `--meteorite-rail-ink-strong`, `--meteorite-rail-dim` | `--theme-header-link`, `--theme-ink`, `--theme-ink-muted` |
| `--meteorite-rail-hover` | `--theme-sidebar-hover-background` |
| `--meteorite-rail-selected`, `--meteorite-rail-selected-ink` | `--theme-sidebar-selected-background`, `--theme-sidebar-selected-ink` |
| `--meteorite-rail-line` | `--theme-sidebar-line`, `--theme-frame-line` and `--theme-line` |
| `--meteorite-rail-field`, `--meteorite-rail-field-line` | `--theme-header-field-background`, `--theme-header-field-border` |
| `--meteorite-phone-menu`, `--meteorite-phone-menu-ink` | `--theme-header-background-solid`, `--theme-header-link` |
| `--meteorite-shadow` | `--theme-shadow-popup` |
| `--meteorite-line-faint` | `--theme-grid-line` and `--theme-row-line` |
| `--meteorite-glow` | `--theme-glow` |
| `--meteorite-instrument` | `--theme-instrument-image` |
| `--meteorite-instrument-filter` | `--theme-instrument-filter` |
| `--meteorite-status-ring` | `--theme-status-ring` |
| `--oc-gray-0` to `-9`, `--oc-white` | `--theme-neutral-0` to `-9`, `--theme-redmine-white` |
| `--fonts-main` | `--theme-font` |

## [1.0.0] - 2026-10-26

### Added

- Meteorite theme: near black, hairlines, an instrument drawn behind the page (rings, ticks, a crosshair, starbursts), a thin frame with a dot at each corner and small monospaced labels. The colours come from the Open Color variables Redmine 7 uses.
- On screens 1100px and wider, all navigation moves into a dark left sidebar, in plain CSS. Narrower screens and the login page keep Redmine's own layout.
- Status shows as an orbit icon (a ring with a point, glowing for in progress) and priority as a row of five bars lit by level. Assignee initials get a ring and status group headers a box. The orbits and bars are CSS.
- Issues, Gantt, Calendar and Activity appear as tabs above the issue list. The tabs and the initials come from `javascripts/theme.js`, which only reads the page.
- A white print for the system light setting (black lines on white paper), in one block at the end of the stylesheet.
- The theme skeleton, the demo Redmine, the page check, the screenshot script and the recorder.
- Tested on Redmine 7.0.2 and the 7.0 line, in light and dark, at desktop and phone width. No console errors, failed requests or sideways scrolling, and text at AA contrast on the pages that matter: the wiki, the activity page and the Rubylode to-do page.
