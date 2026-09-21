# Kanji Atlas

Kanji Atlas is a static web application for learning the kanji used in Japanese prefecture names.

**Live demo:** <https://neoraph.github.io/kanji-atlas/>

It includes:

- A study mode for all 47 prefectures
- Japanese readings in hiragana
- A missing-kanji quiz
- Correct-answer tracking and learner progress
- A prefecture map challenge using real prefecture boundaries
- Map completion and accuracy percentages
- Multiple learner profiles stored in the browser
- A study-card mini-map showing each prefecture's location

## Run locally

No build tools or package installation are required.

```bash
python3 -m http.server 4173
```

Open <http://localhost:4173> in a browser.

## Deploy to GitHub Pages

This project is fully static and can be hosted directly with GitHub Pages.

1. Create a GitHub repository.
2. Copy or push this project into the repository.
3. In the repository, open **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Select the branch containing the project and the `/ (root)` folder.
6. Save the settings and wait for GitHub Pages to publish the site.

The application entry point is `index.html`. The `japan.geojson` file must remain in the same directory as `index.html`, because the application loads it at runtime.

## Technical notes

This application does not use a backend, server-side runtime, database, framework, or build step. It consists of:

- `index.html` — application markup
- `styles.css` — layout and visual styling
- `app.js` — application logic and prefecture data
- `japan.geojson` — prefecture boundary data used by the maps

Learner profiles and progress are saved with browser `localStorage`. This means progress is available on the same browser and device, but is not synchronized across devices or browsers. Shared accounts and cloud synchronization would require a backend service.

## AI-generated code

This project was created with assistance from AI-generated code. The implementation should be reviewed, tested, and adapted before being used in a production or educational environment.
