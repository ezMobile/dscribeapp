# dScribe Website

Static production-ready website for **dScribe** (`dscribeapp.com`) to support Android/Google Play launch.

Tagline: **Describe your thoughts. Stay organized.**

## Project purpose

- Provide the public landing page for dScribe.
- Host required policy and support pages for Google Play listing compliance.
- Stay lightweight, fast, and GitHub Pages compatible (no build tools, no React, no npm).

## File structure

```text
dscribeWeb/
|-- index.html
|-- privacy-policy.html
|-- terms-of-service.html
|-- support.html
|-- styles.css
|-- CNAME
`-- assets/
    |-- logo.png
    |-- favicon.ico
    |-- qr/
    |   |-- android-playstore-qr.svg
    |   `-- ios-appstore-qr.svg
    `-- screenshots/
        |-- notes.png
        |-- todo.png
        |-- reminders.png
        |-- vault.png
        |-- settings.png
        `-- example.png
```

## Asset placeholders

Copy your real image files to:

- `assets/logo.png`
- `assets/favicon.ico`
- `assets/qr/android-playstore-qr.svg` (replace with real Android QR)
- `assets/qr/ios-appstore-qr.svg` (replace with real iOS QR when App Store URL is available)
- `assets/screenshots/notes.png`
- `assets/screenshots/todo.png`
- `assets/screenshots/reminders.png`
- `assets/screenshots/vault.png`
- `assets/screenshots/settings.png`
- `assets/screenshots/example.png`

## Run locally

Since this is plain static HTML/CSS, you can run it in either way:

1. Open `index.html` directly in your browser.
2. Or serve with a local HTTP server:

```bash
python -m http.server 8080
```

Then open `http://localhost:8080` from the `dscribeWeb` folder.

## Publish to GitHub Pages

1. Push this folder contents to your GitHub Pages source branch (commonly `main`).
2. In GitHub repository settings, open **Pages**.
3. Set source to your deployment branch/folder.
4. Confirm the `CNAME` file contains exactly:

```text
dscribeapp.com
```

5. Wait for GitHub Pages to publish.

## DNS records for custom domain

Set these DNS records with your domain provider:

### A records (apex/root `@`)

- `185.199.108.153`
- `185.199.109.153`
- `185.199.110.153`
- `185.199.111.153`

### CNAME record

- `www` -> `<github-username>.github.io`

## Important GitHub Pages setting

- Enable **Enforce HTTPS** in GitHub Pages settings after DNS is configured.
