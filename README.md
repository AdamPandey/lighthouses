# lighthouses

A small static website, "Lighthouses of Ireland": a home page with a short history of Irish lighthouses and four pages about individual lighthouses. Plain HTML and CSS, no JavaScript, no build step.

## Pages

- `index.html`: the history of Irish lighthouses, from Hook Head to the 21st century, as a nested list by century.
- `tuskar.html`: Tuskar Rock (the longest page).
- `fastnet.html`: Fastnet Rock.
- `tory.html`: Tory Island.
- `rathlin.html`: Rathlin East.

Each page has the same layout: a hero banner, a sidebar linking to the four lighthouse pages, a sidebar of outside links (met.ie, marine.ie, irishlights.ie), the main text, and a footer. The footer says the content can be freely distributed and adapted as long as the same rights are kept on derived works. There is no separate LICENSE file.

## Viewing it

Open `index.html` in a browser. All paths are relative, so no server is needed. If you prefer one:

    python3 -m http.server

then go to http://localhost:8000.

I checked that every page, stylesheet and image reference resolves to a file in the repo.

## Structure

    index.html, tuskar.html, fastnet.html, tory.html, rathlin.html
    assets/css/
        grid.css          page layout (CSS grid), breakpoints at 500px and 600px
        background.css    banner image, box and sidebar/footer colours
        navigation.css    sidebar link styles
        text.css          heading margins
    assets/images/        photos and the copyleft icon

`grid.css` is a single column on narrow screens, two columns from 500px, and three columns (sidebar, content, sidebar) from 600px with a 1200px maximum width.

## Known gaps

- Every page has an empty `<title>`.
- All five pages show `donaghadee.jpg` above the text. `fastnet.jpg`, `rathlin.jpg`, `tory.jpg` and `tuskar.jpg` are in `assets/images/` but nothing references them. `skelligs.jpg` is only used as the banner background.
- The images are not given alt text.
- A few characters in `tuskar.html` are garbled (for example "keepers¡¦ families" and "1856¡V57"), which look like a bad encoding conversion of the original text.
- There is no `.gitignore` at the moment (see below).

## History

The git history is by John Dempsey (also committing as john-dempsey): an initial commit on 2020-09-25 followed by small wording and colour changes the same day ("derivative" to "secondary" in the footer, "mariners" to "sailors" in `rathlin.html`, and so on), then two `.gitignore` commits in January 2024, the last of which deletes the file. The text and layout come from that history; this copy has no commits of its own.
