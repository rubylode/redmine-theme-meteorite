# Changelog

All notable changes to this theme. The format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).

## [1.0.0] - 2026-10-26

### Added

- Meteorite theme: near black, hairlines, an instrument drawn behind the page (rings, ticks, a crosshair, starbursts), a thin frame with a dot at each corner and small monospaced labels. The colours come from the Open Color variables Redmine 7 uses.
- On screens 1100px and wider, all navigation moves into a dark left sidebar, in plain CSS. Narrower screens and the login page keep Redmine's own layout.
- Status shows as an orbit icon (a ring with a point, glowing for in progress) and priority as a row of five bars lit by level. Assignee initials get a ring and status group headers a box. The orbits and bars are CSS.
- Issues, Gantt, Calendar and Activity appear as tabs above the issue list. The tabs and the initials come from `javascripts/theme.js`, which only reads the page.
- A white print for the system light setting (black lines on white paper), in one block at the end of the stylesheet.
- The theme skeleton, the demo Redmine, the page check, the screenshot script and the recorder.
- Tested on Redmine 7.0.2 and the 7.0 line, in light and dark, at desktop and phone width. No console errors, failed requests or sideways scrolling, and text at AA contrast on the pages that matter: the wiki, the activity page and the Rubylode to-do page.
