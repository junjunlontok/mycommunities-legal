# MyCommunities — Legal Documents Site

Publicly accessible **Terms and Conditions** and **Privacy Policy** for the
MyCommunities platform, hosted on **GitHub Pages**.

These pages exist **outside the app** so we can link to them from the Google Play
Store listing (required for Google Play policy compliance).

## Files

| File | Purpose |
| ---- | ------- |
| `index.html` | Landing page linking both documents |
| `privacy.html` | Privacy Policy (10 sections) |
| `terms.html` | Terms and Conditions (15 sections) |
| `assets/style.css` | Shared stylesheet (brand colors from the app theme) |

> The legal text mirrors `lib/features/legal/legal_content.dart` in the main
> Flutter repo (`legalLastUpdatedDate = August 8, 2026`).

## How to deploy (one-time setup)

### 1. Create the GitHub repository

1. Go to <https://github.com/new>
2. Repository name: **`mycommunities-legal`**
3. Visibility: **Public**
4. Do **not** tick "Add a README" (this repo already has one)
5. Click **Create repository**

### 2. Push this folder to GitHub

Open a terminal in this folder (`legal-site/`) and run:

```powershell
git init -b main
git add .
git commit -m "Add MyCommunities legal documents site (Terms + Privacy)"
git branch -M main
git remote add origin https://github.com/<YOUR_USERNAME>/mycommunities-legal.git
git push -u origin main
```

### 3. Enable GitHub Pages

1. On GitHub, open the **`mycommunities-legal`** repo
2. Go to **Settings → Pages**
3. Under **Build and deployment → Source**, choose **Deploy from a branch**
4. Select branch **`main`**, folder **`/` (root)**, then **Save**
5. Wait ~1 minute — your site goes live at:

```
https://<YOUR_USERNAME>.github.io/mycommunities-legal/
https://<YOUR_USERNAME>.github.io/mycommunities-legal/privacy.html
https://<YOUR_USERNAME>.github.io/mycommunities-legal/terms.html
```

## Use in the Google Play listing

In Google Play Console (**Store listing → App content → Privacy Policy**), enter
the **Privacy Policy** URL:

```
https://<YOUR_USERNAME>.github.io/mycommunities-legal/privacy.html
```

You can also add the Terms URL to your listing's app description or Data safety
form where needed.

## How to update the content

1. Edit the `.html` files (or copy updated text from
   `lib/features/legal/legal_content.dart`)
2. Update the "Last updated" date in the `updated-banner` if the text changed
3. Commit and push — GitHub Pages publishes automatically:

```powershell
git add .
git commit -m "Update legal text"
git push
```

## Local preview

```powershell
python -m http.server 8080
# then open http://localhost:8080
```

## Contact

support@mycommunities.app
