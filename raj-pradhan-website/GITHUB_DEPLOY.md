# Deploy Raj Pradhan website through GitHub Pages

1. Create a **public** repository on GitHub (for example `raj-pradhan-website`). GitHub Pages availability on private repos depends on plan.
2. Upload **the contents of this folder** to the repository's `main` branch, preserving `.github/workflows/deploy.yml`. The GitHub website upload UI may not preserve hidden folders reliably: use GitHub Desktop or `git` to push all files if the workflow is missing.
3. In repository **Settings → Pages → Build and deployment → Source**, choose **GitHub Actions**.
4. Open the **Actions** tab. If necessary, run **Deploy website to GitHub Pages** manually. The build and publish steps run on GitHub; the first build has not been locally verified in this environment.
5. When successful, Pages provides a URL like `https://YOUR-USERNAME.github.io/raj-pradhan-website/`.
6. Navigation uses hash URLs such as `/#/journal` for reliable refreshes on GitHub Pages. For clean URLs and better article SEO, migrate to a host with rewrite support or static site generation.
7. When ready, in **Settings → Pages → Custom domain** enter `rajpradhan.com.np`. Set DNS to GitHub Pages following GitHub's verified custom-domain instructions, then enable **Enforce HTTPS** once certificates are issued. Don't change DNS until preview is approved.

This deployment publishes the website publicly. Do not include secrets, drafts meant to stay private, or client information without permission. There is no CMS/backend yet.
