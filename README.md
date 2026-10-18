# Project Mercury, every flight (interactive)

An interactive version of the Project Mercury flowing timeline: all 26 launches from 1959 to 1963 plus the Mercury
Seven's introduction, on one line that climbs with each flight's time in the air. Built from Chart Studio.

| File | What it is |
|---|---|
| `index.html` | The whole page in one file: chart, data, photos and the Chart Studio runtime inline. d3 loads from cdnjs. |
| `preview.png` | 1200 × 630 image for link previews (Reddit, social). |
| `.nojekyll` | Tells GitHub Pages to serve the files as they are. |

On phones (under 640 px wide) the cards sit on one side of the line at full width. On wider screens they alternate
sides, as in the Studio chart.

## Publishing on GitHub Pages

1. Put these files at the root of the repository, or in `docs/`.
2. In the repository's **Settings → Pages**, choose **Deploy from a branch**, pick the branch and the folder (`/` or `/docs`).
3. The page appears at `https://<user>.github.io/<repo>/` after a minute or two.

For a link preview with the image, set `PAGE_URL` in `../build_pages.py` to that address (ending in `/`), run
`python build_pages.py` again and commit the new `index.html`.

## Rebuilding

The page is generated; don't edit `index.html` by hand. After changing the chart in the Chart Studio library, run
`python split_render.py` (for the preview image) and then `python build_pages.py` in `stories/project-mercury/`.

Sources: NASA, Project Mercury Uncrewed Missions (2004); Mercury Crewed Flights Summary (2006). Photos: NASA.
