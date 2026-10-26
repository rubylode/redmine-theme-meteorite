# Changelog

All notable changes to this theme. The format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).

## [1.0.0] - 2026-10-26

### Added

- Meteorite: a space print. Near black, hairlines, an instrument drawn behind the page (rings, ticks, a crosshair, starbursts), a thin frame with a dot at each corner, and small monospaced labels, in the Open Color variables Redmine 7 is built on.
- On screens 1100px and wider, all navigation moves into a dark left sidebar, in plain CSS. Narrower screens and the login page keep Redmine's own layout.
- Status as an orbit icon (a ring with a point, glowing for what is in progress), priority as a row of five bars lit by level, a ring round the assignee's initials, status group headers in a box, and Issues, Gantt, Calendar and Activity as tabs above the list. The initials and the tabs come from one small script, `javascripts/theme.js`, which only reads the page; the orbits and the bars are CSS.
- A white print for the system light setting (black lines on white paper), in one block at the end of the stylesheet. Meteorite is dark first.
- The theme skeleton, the demo Redmine, the page check, the screenshot script and the recorder.
- Tested on Redmine 7.0.2 and the 7.0 line, in both schemes, at desktop and phone width: no console errors, no failed requests, no sideways scrolling, and text at AA contrast on the pages that matter, including the wiki, the activity page and the Rubylode to-do page.
