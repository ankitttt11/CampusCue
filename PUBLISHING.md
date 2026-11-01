# Publishing CampusCue with GitHub Pages

The repository and public website URL have **not** been created yet. These steps require access to your GitHub account; do not share your password or access token with anyone.

## 1. Test locally first

1. Extract the project ZIP.
2. Open the `CampusCue` folder in VS Code.
3. Choose **Terminal → New Terminal**.
4. Run:

   ```bash
   python -m http.server 8000
   ```

5. Open <http://localhost:8000> in your browser.
6. Add a sample task, mark it complete, switch filters, refresh the page, and confirm it remains saved. Delete the sample task afterwards.
7. Test the page at desktop width and a narrow mobile width using your browser's responsive/device toolbar.
8. Stop the server with `Ctrl+C`.

## 2. Create a public GitHub repository

1. Sign in to GitHub in your browser.
2. Create a **new public repository** named `campuscue`.
3. Do not add a README, license, or `.gitignore` on GitHub if you will push this existing folder; the project already has a README.
4. Copy the repository's HTTPS URL. It should look like `https://github.com/YOUR_USERNAME/campuscue.git`.

## 3. Push the local project

Open a terminal in the extracted `CampusCue` folder and run these commands, replacing `YOUR_USERNAME` with your GitHub username:

```bash
git init
git add .
git commit -m "Build CampusCue student deadline planner"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/campuscue.git
git push -u origin main
```

If Git says a remote named `origin` already exists, inspect it with `git remote -v`; do not add a second remote blindly. If authentication is requested, use GitHub's supported browser sign-in/credential flow. Never put a password or token into source code or commit it to the repository.

If you do not have Git installed or do not want to use the terminal, you can upload the extracted project files through the GitHub website instead. Make sure `index.html`, `README.md`, `DESIGN_RATIONALE.md`, `PUBLISHING.md`, `WALKTHROUGH.md`, and `TEST_REPORT.md` are in the repository root.

## 4. Enable GitHub Pages

1. Open the `campuscue` repository on GitHub.
2. Go to **Settings → Pages**.
3. Under **Build and deployment**, select **Deploy from a branch**.
4. Select branch `main` and folder `/(root)`, then save.
5. Wait for GitHub Pages to finish publishing. The URL normally follows this pattern: `https://YOUR_USERNAME.github.io/campuscue/`.
6. Copy the actual URL shown in the Pages settings. Do not submit the example URL.

## 5. Verify the public deployment

1. Open the actual Pages URL in a private/incognito window where you are not signed into GitHub.
2. Confirm the page loads, add a task, use filters, mark it complete, undo it, delete it, and refresh to test browser persistence.
3. Check desktop and mobile layouts.
4. Open the repository URL in a private/incognito window to confirm it is public.
5. Add the verified repository URL and live URL to your submission form.

GitHub Pages may take several minutes to publish the first time. If the URL returns a 404, check the Pages deployment status and confirm that `index.html` is in the repository root.
