# Git commands for publication

## Initial publication from this folder

Create an empty repository named `data-mining-course-projects` under your GitHub account first. Open a terminal inside the extracted project folder, then run:

```bash
git init -b main
git config user.name "Arian Abdollahi"
git config user.email "ari000ab000@gmail.com"
git add README.md requirements.txt .gitignore .gitattributes docs
git commit -m "Add course overview and reproducibility documentation"
git add projects/01-adult-income-pca
git commit -m "Add Adult census analysis and PCA coursework"
git add projects/02-regression-and-association-rules
git commit -m "Add regression and association rule mining coursework"
git add projects/03-shopper-purchase-intention
git commit -m "Add shopper purchase intention coursework"
git remote add origin https://github.com/Arian-Abdollahi/data-mining-course-projects.git
git push -u origin main
```

GitHub HTTPS authentication uses a supported credential manager, GitHub CLI login, or a personal access token rather than your account password. Do not put a token or password in a command, repository, notebook, or README. If you prefer private commit email, substitute your exact GitHub-provided noreply email from account settings before committing.

These initial commands are for a genuinely empty remote. If the repository already contains uploaded files, clone it instead of creating unrelated history:

```bash
git clone https://github.com/Arian-Abdollahi/data-mining-course-projects.git
cd data-mining-course-projects
# Edit files, then stage only the changes you intend to share.
git add README.md
git commit -m "Update course project documentation"
git push
```
