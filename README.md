# Build Notes

An editorial development blog, published as a public notebook. The portfolio-story draft is grounded in the project summary supplied for this build (four days, 29 iterations, JavaScript to pure CSS). Its first essay is an anonymous builder's diary (four days, 29 iterations, JavaScript to pure CSS). Two other cards are outlines on the desk, marked as such.

Live: https://aditya2375.github.io/working-notes/

## Run
`npm install && npm run dev`; `npm run build` to generate production files.

## Edit
Articles and preview outlines live in `src/posts.js`. The first essay is published; the other entries are outlines on the desk.

## Deployment and checks

Build with `npm ci && npm run build -- --base=/working-notes/`. The `gh-pages`
branch serves the resulting static files at the live link above. Fonts are
self-hosted; the notebook makes no API call and stores no reader data.

The remote-post experiment is not active: the notebook uses the checked-in
`src/posts.js` content. Outlines stay marked as unpublished. There is no login,
private storage, payment flow or hosted backend. GitHub Pages controls response
headers; the page adds a meta CSP but cannot add framing protection headers.

To repeat browser QA: `npm ci && npm run build`, start `npm run preview`, then run `npm test` in another terminal. Set `CHROME_PATH` if Chrome is not at `/usr/bin/google-chrome`.
