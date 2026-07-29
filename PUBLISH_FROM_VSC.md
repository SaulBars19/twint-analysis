# How to Publish This Analysis from VS Code

## 1. Set Up Git

Open the project folder in VS Code and launch the integrated terminal:

```bash
git --version
```

If Git is installed correctly, you'll see the installed version.

Configure your identity only if you haven't done it before:

```bash
git config --global user.name "Saul Barrientos"
git config --global user.email "YOUR_GITHUB_EMAIL"
```

---

## 2. Create the GitHub Repository

On GitHub:

1. Click **New repository**.

2. Name it something like `twint-analysis`.

3. Add a short description, for example:

   ```
   Interactive fundamental and strategic analysis of TWINT AG.
   ```

4. Choose **Public**.

5. **Do not** initialize the repository with a README, license, or `.gitignore`, as these files are already included.

6. Click **Create repository**.

---

## 3. Upload the Project from VS Code

Inside the integrated terminal, while located in the project folder, run:

```bash
git init
git add .
git commit -m "Publish TWINT fundamental and strategic analysis"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/twint-analysis.git
git push -u origin main
```

Replace `YOUR_USERNAME` with your actual GitHub username.

---

## 4. Enable GitHub Pages

In your GitHub repository:

1. Open **Settings**.
2. Go to **Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**.
4. Select the **main** branch.
5. Select the **/ (root)** folder.
6. Click **Save**.

Your website will usually be available at:

```text
https://YOUR_USERNAME.github.io/twint-analysis/
```

---

## 5. Update the README

In `README.md`, replace:

```text
https://<your-github-username>.github.io/twint-analysis/
```

with your actual GitHub Pages URL.

Then commit the change:

```bash
git add README.md
git commit -m "Add live GitHub Pages link"
git push
```

---

## 6. Publishing Future Updates

Whenever you modify the analysis:

```bash
git add .
git commit -m "Briefly describe your changes"
git push
```

GitHub Pages will automatically redeploy the updated version.

---

# Best Practices for a Professional Repository

* Add a screenshot of the dashboard to the README once the live website is available.
* Write a concise and informative description in the repository's **About** section.
* Add relevant topics such as:

  * `finance`
  * `fintech`
  * `payments`
  * `twint`
  * `data-analysis`
  * `equity-research`
  * `chartjs`
* Pin the repository to your GitHub profile.
* Share the GitHub Pages URL on your CV, LinkedIn profile, and job applications.

---

# Troubleshooting

### The website shows a blank page

Make sure the main file is named **`index.html`** and is located in the root directory of the repository.

---

### Charts are not displayed

The dashboard loads **Chart.js** from a CDN. Verify that your browser has an internet connection and that no browser extension or firewall is blocking external scripts.

---

### Git rejects the push

Check that your remote repository URL is correct:

```bash
git remote -v
```

To update it:

```bash
git remote set-url origin https://github.com/YOUR_USERNAME/twint-analysis.git
```

