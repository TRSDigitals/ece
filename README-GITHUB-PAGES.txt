ECE GENIUS — GitHub Pages 404 FIX

WHY THE 404 HAPPENED
GitHub Pages publishes the configured folder's root. The original project kept index.html inside public/, so if the repository root was published, Pages could not find /index.html.

WHAT THIS PACKAGE FIXES
- Puts index.html at the publish root.
- Puts styles.css and app.js beside index.html.
- Uses relative asset paths (./styles.css and ./app.js).
- Includes data/syllabi.json and .nojekyll.

DEPLOY TO https://trsdigitals.github.io/
1. Open the GitHub repository named exactly: trsdigitals.github.io
2. Extract this ZIP on your computer.
3. Upload the CONTENTS of this folder to the repository root (not the folder itself, and not into public/).
4. Ensure index.html is visible in the repository's top-level file list.
5. Commit to the branch selected under Settings → Pages (usually main, folder /root).
6. In Settings → Pages, select Deploy from a branch → main → /(root), then Save.
7. Wait for the Pages deployment to finish, then hard-refresh the website (Ctrl+F5).

IMPORTANT: GitHub Pages only hosts static files. It cannot run the Node.js/Express server. The website shell and local browser features can load from Pages, but AI chat, file analysis, syllabus API search, and server-side exports require the Node backend to be deployed separately (for example, on a Node-compatible host). Then configure the frontend API base URL to that backend and enable CORS for https://trsdigitals.github.io. Never put OPENAI_API_KEY in app.js or any public file.

If your repository is NOT named trsdigitals.github.io and is instead a project repository, the URL usually includes /REPOSITORY-NAME/. This package's relative CSS/JS paths support that arrangement too, but set Pages to publish the repository root.
