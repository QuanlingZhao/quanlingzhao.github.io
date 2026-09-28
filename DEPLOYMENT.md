# Deploying the Minimal Light academic homepage

## Recommended: user site at quanlingzhao.github.io

1. On GitHub, create a **public** repository named exactly:

   `QuanlingZhao.github.io`

2. Upload the contents of this folder to the repository root, or from a terminal run:

```bash
git init
git add .
git commit -m "Initial academic homepage"
git branch -M main
git remote add origin https://github.com/QuanlingZhao/QuanlingZhao.github.io.git
git push -u origin main
```

3. Open the repository on GitHub and go to:

   **Settings → Pages**

4. Under **Build and deployment**, choose **Deploy from a branch**.

5. Select:

   - Branch: `main`
   - Folder: `/ (root)`

6. Save. GitHub will build the Jekyll site using the Minimal Light remote theme.

7. The site should appear at:

   `https://quanlingzhao.github.io/`

## If you want to keep the existing /website URL

Create or update a repository named `website` instead. Your URL will be:

`https://quanlingzhao.github.io/website/`

Then change this line in `_config.yml`:

```yaml
canonical: https://quanlingzhao.github.io/website/
```

## Local preview (optional)

GitHub Pages can build the site without a local Ruby installation. If you want local preview, install Ruby/Jekyll and use the Minimal Light instructions at:

https://github.com/yaoyao-liu/minimal-light
