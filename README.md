---
languages: git, markdown
tags: github, profile, readme, personal-branding
resources: 3
---

# Git Profile README

![GitHub Profile](https://img.shields.io/badge/GitHub_Profile_README-181717?logo=github&logoColor=white&style=for-the-badge)
![Markdown](https://img.shields.io/badge/Markdown-000000?logo=markdown&logoColor=white&style=for-the-badge)
![Difficulty](https://img.shields.io/badge/difficulty-%E2%98%85%E2%98%86%E2%98%86%E2%98%86%E2%98%86-green?style=for-the-badge)

## Background

Every GitHub user can create a "profile README" - a Markdown file that renders at the top of their profile page. It's the first thing recruiters, collaborators, and your instructor see when they land on `github.com/<your-username>`.

The trick: GitHub treats any **public repository whose name matches your username exactly** as your profile repo, and displays its `README.md` on your profile.

- Username `jane-doe` → public repo named `jane-doe` → the README inside renders on the profile.
- Username `jsmith42` → public repo named `jsmith42` → same deal.

Companion handbook page: [Module 1 - Program Setup, Git & GitHub](https://lgcc.github.io/modules/01-setup).

## Objectives

By the end of this exercise you will have:

1. Created the special `<username>/<username>` repo that shows on your profile
2. Personalized it with your own bio, what you're learning, and how to reach you
3. Verified it renders correctly at `https://github.com/<your-username>`
4. Submitted notes + a screenshot back to this lab repo

## Instructions

### 1. Create the profile repo on GitHub

1. Go to [github.com/new](https://github.com/new).
2. **Repository name:** type your GitHub username **exactly**. GitHub shows a banner: *"You found a secret! This repository will be featured on your profile."* If you don't see that banner, the name doesn't match your username.
3. **Visibility:** Public (required - private repos don't render on the profile).
4. **Check** "Add a README file".
5. Click **Create repository**.

### 2. Clone your profile repo locally

```bash
cd ~/Desktop   # or wherever you keep your work
git clone git@github.com:<your-username>/<your-username>.git
cd <your-username>
```

### 3. Personalize the README

Copy [`template.md`](./template.md) from this lab into your profile repo as `README.md`, then fill in every `<PLACEHOLDER>`.

Minimum requirements:

- A one-line intro
- What you're currently learning (3+ items)
- How to reach you (email, LinkedIn, or portfolio URL)

### 4. Commit and push

```bash
git status                                   # verify what changed
git add README.md
git commit -m "docs: personalize profile readme"
git push
```

### 5. Verify it rendered

Open `https://github.com/<your-username>` in a browser. Your README should appear above your pinned repositories. If it doesn't render:

- Is the repo public?
- Does the repo name match your username exactly (case-sensitive)?
- Is `README.md` at the root of the repo, not inside a folder?

### 6. Submit your work to this lab

Clone **this** repo (the one you're reading now), create a branch named after your GitHub username, and push your submission.

```bash
# clone the lab repo
git clone git@github.com:ttpr-lgcc/git-profile-readme-lagcc-002.git
cd git-profile-readme-lagcc-002

# create a branch named after your username
git checkout -b <your-username>

# create your submission folder
mkdir -p submissions/<your-username>
```

Add two files inside `submissions/<your-username>/`:

1. **`notes.md`** - one paragraph: what you put on your profile and why you chose those sections.
2. **`screenshot.png`** - a screenshot of your rendered GitHub profile page. (macOS: `Cmd + Shift + 4` → drag to capture a region.)

Commit and push:

```bash
git add submissions/<your-username>/
git commit -m "feat: add profile readme submission for <your-username>"
git push -u origin <your-username>
```

Your branch is your submission. Your instructor pulls it to review - no pull request needed.

## Checklist

- [ ] Public repo named exactly `<my-username>/<my-username>` exists
- [ ] Every placeholder in the template is replaced with real text
- [ ] My profile page shows the rendered README
- [ ] `submissions/<my-username>/notes.md` explains my choices
- [ ] `submissions/<my-username>/screenshot.png` shows the live profile
- [ ] Everything is pushed to a branch named `<my-username>` on the lab repo

## Stretch goals (optional)

- Add a [GitHub Stats card](https://github.com/anuraghazra/github-readme-stats) that updates automatically.
- Add badges for the technologies you're learning via [shields.io](https://shields.io).
- Embed a screenshot or GIF of a project you built.
- Add a "Now" section you commit to updating monthly.

## Resources

- [GitHub Docs](https://docs.github.com/) - [Managing your profile README](https://docs.github.com/en/account-and-profile/setting-up-and-managing-your-github-profile/customizing-your-profile/managing-your-profile-readme)
- [Awesome GitHub Profile READMEs](https://github.com/abhisheknaiidu/awesome-github-profile-readme) - examples for inspiration
- [Markdown Guide](https://www.markdownguide.org/basic-syntax/) - the syntax you'll use in the README
