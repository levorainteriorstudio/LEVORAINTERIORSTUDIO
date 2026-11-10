# LEVORA INTERIOR — GitHub Pages package

## Included
- `index.html` — updated website, contact form integration and dynamic project display
- `add-project.html` — browser-based helper to prepare new portfolio project files
- `projects.json` — data file for projects added using the helper
- `robots.txt` and `sitemap.xml` — search-engine crawl/indexing hints

## 1. Publish on GitHub Pages
1. Create/open your GitHub repository.
2. Upload the **contents** of this folder to the repository root (not the ZIP itself).
3. In GitHub, open **Settings → Pages**.
4. Choose **Deploy from a branch**, select `main` and `/ (root)`, then Save.
5. GitHub will show your public website address. Replace the placeholder URL in `index.html`, `robots.txt`, and `sitemap.xml` with that exact address.

## 2. Make enquiry emails arrive in Gmail
The form is configured to send to: `levora.interorstudio@gmail.com`.
1. Publish the website first.
2. Submit one test enquiry from the live website.
3. FormSubmit will send an activation/verification email to the inbox above. Open it and confirm activation.
4. Submit another test enquiry and check Inbox and Spam.
5. If the address written in the request was intended to be different from `levora.interorstudio@gmail.com`, change the recipient in the form `action` inside `index.html` before publishing.

**Note:** FormSubmit is a third-party form relay. The first activation email must be confirmed. Do not put a Gmail password or private API key in website code.

## 3. Add a new project
1. Open `add-project.html` on the published website.
2. Enter project details and choose a project image.
3. If you already added projects before, select the current `projects.json` file so earlier additions are preserved.
4. Press **Prepare project files**. Two files download: the image and an updated `projects.json`.
5. In your GitHub repository, upload the image into `assets/projects/` and replace `projects.json` in the root.
6. GitHub Pages publishes the update automatically after the commit.

The add-project page prepares files in your browser; it does not directly write to GitHub. Direct upload/publishing would require a secure server or GitHub App/OAuth backend. Never place a GitHub access token in public HTML or JavaScript.

## 4. Google Search indexing
1. Verify the live website in Google Search Console (URL-prefix property).
2. Add the verification meta tag Google gives you inside the `<head>` of `index.html`.
3. Submit the sitemap URL: `https://YOUR-GITHUB-USERNAME.github.io/YOUR-REPOSITORY/sitemap.xml`.
4. Use URL Inspection → Request Indexing for the homepage.
5. Keep the site public, reachable, and with accurate page titles/descriptions.

Indexing is not guaranteed or instant. `robots.txt` and a sitemap help Google discover pages; they cannot guarantee a ranking or immediate appearance.

## Before publishing
- Replace `YOUR-GITHUB-USERNAME` and `YOUR-REPOSITORY` in the canonical URL, `robots.txt`, and `sitemap.xml`.
- Check the email recipient is correct.
- Confirm the FormSubmit activation email after the first test.
- Check all displayed business details and images are correct.
