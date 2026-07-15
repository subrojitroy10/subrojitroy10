# Replicating the Self-Hosted GitHub Analytics Setup

To display your accurate **326+ contributions** and private repository statistics on your profile README without rate limits, you must deploy your own private instances of the analytics generators. 

Follow this step-by-step guide to complete the migration.

---

## Step 1: Generate a GitHub Personal Access Token (PAT)

Your self-hosted servers need a token to read your private repository statistics.

1. Go to your GitHub account **Settings** $\to$ **Developer Settings** $\to$ **Personal Access Tokens** $\to$ **Tokens (classic)**.
2. Click **Generate new token** (classic).
3. Set the Note to `github-readme-stats-server`.
4. Select the following scopes:
   *   `repo` (Full control of private repositories)
   *   `read:user` (Read user profile data)
5. Click **Generate token** and copy the resulting string (starts with `ghp_`). Keep this safe.

---

## Step 2: Deploy GitHub Readme Stats to Vercel

This hosts the stats and top languages cards.

1. Visit the source repository: [anuraghazra/github-readme-stats](https://github.com/anuraghazra/github-readme-stats).
2. Scroll down to the **Deploy** section and click the **Deploy with Vercel** button.
3. Log in to Vercel with your GitHub account.
4. When configuring the deployment, add an **Environment Variable**:
   *   **Name**: `PAT_1`
   *   **Value**: *Paste your generated GitHub PAT (`ghp_...`)*
5. Click **Deploy**.
6. Once deployed, note your custom Vercel subdomain (e.g., `github-readme-stats-yourname.vercel.app`).

---

## Step 3: Deploy Streak Stats to Vercel

This hosts the daily streak calendar card.

1. Visit the source repository: [github-readme-streak-stats](https://github.com/denvercoder1/github-readme-streak-stats).
2. Scroll down to the **Deployment** section and click **Deploy to Vercel**.
3. Log in to Vercel.
4. Add the **Environment Variable**:
   *   **Name**: `PAT_1`
   *   **Value**: *Paste your generated GitHub PAT (`ghp_...`)*
5. Click **Deploy**.
6. Note your custom streak subdomain (e.g., `github-readme-streak-stats-yourname.vercel.app`).

---

## Step 4: Update your Profile README.md

Once your servers are live, open your [README.md](file:///d:/PolyNovea/PolyNovea/Docx/Company%20Docx/github/README.md) and replace the placeholders in the **GitHub Analytics** section with your newly created Vercel domains:

```markdown
<!-- Replace 'your-stats-subdomain' and 'your-streak-subdomain' with your active Vercel domains -->

## 📊 GitHub Analytics

<p align="center">
  <img src="https://your-stats-subdomain.vercel.app/api?username=subrojitroy10&show_icons=true&theme=tokyonight" alt="Subrojit's GitHub Stats" width="48%" />
  &nbsp;
  <img src="https://your-stats-subdomain.vercel.app/api/top-langs/?username=subrojitroy10&layout=compact&theme=tokyonight" alt="Top Languages" width="48%" />
</p>

<p align="center">
  <img src="https://your-streak-subdomain.vercel.app/?user=subrojitroy10&theme=tokyonight" alt="GitHub Streak" width="97%" />
</p>
```
