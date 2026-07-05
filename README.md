# GitHub Pages Hosting Guide & Plan

This directory stores the source code and configuration for your public-facing business homepage, which will be hosted on **GitHub Pages** using your custom domain.

## 📋 Next Steps

To build the website using modern web development standards and visual styling guidelines (such as glassmorphism, responsive forms, and optimized layouts), run the following search command to retrieve relevant best-practice guides:

```bash
npx -y modern-web-guidance@latest search "glassmorphism form layout"
```

Once a relevant guide ID is found, retrieve it using:
```bash
npx -y modern-web-guidance@latest retrieve <guide-id>
```

---

## 🚀 Setup Steps

### 1. Initialize Git Repository
To host on GitHub Pages, the project must be version-controlled with Git and pushed to a public GitHub repository.

```bash
git init
git add .
git commit -m "Initial commit"
```

### 2. Create a GitHub Repository
1. Go to [github.com](https://github.com) and create a new repository.
2. Name it (e.g., `element71-website`).
3. Keep the repository **Public** (required for free GitHub Pages).
4. Link it and push your local code:
   ```bash
   git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPO-NAME.git
   git branch -M main
   git push -u origin main
   ```

### 3. Enable GitHub Pages
1. Go to your repository settings on GitHub.
2. Select **Pages** from the left sidebar.
3. Under **Build and deployment**, set the source to **Deploy from a branch**.
4. Select the `main` branch and folder `/ (root)` and click **Save**.

### 4. Configure Your Custom Domain
To point your custom domain (e.g., `yourdomain.com`) to this GitHub Pages site:

1. **In GitHub Settings:**
   * Go back to the **Pages** settings in your repository.
   * Under **Custom domain**, type your domain name (e.g., `yourdomain.com`) and click **Save**.
   * This creates a `CNAME` file in your repository.
2. **In Your Domain Registrar (e.g., Namecheap, Porkbun, Cloudflare):**
   * Configure **DNS records** to point your domain to GitHub's servers:
     * **A Records** (point to GitHub's IPs):
       * `185.199.108.153`
       * `185.199.109.153`
       * `185.199.110.153`
       * `185.199.111.153`
     * **CNAME Record** (for `www` subdomain):
       * Host: `www`
       * Value: `YOUR-USERNAME.github.io.` (make sure to include the trailing dot).
3. **Enable HTTPS:**
   * Once DNS propagates, go back to GitHub Pages settings and check **Enforce HTTPS** (this is free and automatic).

---

## 📂 Project Structure

Here is the initial setup we will build:
* `index.html` - The main entry point (home page).
* `styles.css` - The modern stylesheet featuring clean typography, grid layouts, and smooth animations.
* `CNAME` - A configuration file specifying your custom domain.

---

## Navigation
* Return to element71 home: **[element71/README.md](file:///Users/jason/Library/CloudStorage/GoogleDrive-jasonlu71@gmail.com/My%20Drive/element71/projects/element71/README.md)**
* Return to projects list: **[projects/README.md](file:///Users/jason/Library/CloudStorage/GoogleDrive-jasonlu71@gmail.com/My%20Drive/element71/projects/README.md)**

---

> [!NOTE]
> **Workspace Sync Rule:** Whenever this file is updated, you must ensure the root master [README.md](file:///Users/jason/Library/CloudStorage/GoogleDrive-jasonlu71@gmail.com/My%20Drive/element71/README.md) is updated and synchronized.
