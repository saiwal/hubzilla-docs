# Contributing to This Documentation

Welcome! We’re thrilled to have you contribute to the Hubzilla documentation. This guide explains how to submit changes to our documentation, hosted at `https://github.com/saiwal/hubzilla-docs`. Built with MkDocs and the `mkdocs-material` theme, our docs are community-maintainable, and your input—whether fixing a typo, adding a section, or improving clarity—makes a difference. Here’s how to get started.

## How Versioning Works

Our documentation uses a versioning system where each version (e.g., `10.0.8`) has its own branch in the repository. Changes should be made to the branch corresponding to the version you’re documenting (e.g., `10.0.8`). A maintainer will later merge these changes into the `main` branch for publishing. This keeps version-specific docs organized and up-to-date.

## Prerequisites

- A GitHub account (sign up at [github.com](https://github.com) if you don’t have one).
- Basic knowledge of Markdown (our docs are written in this format—check out a [Markdown guide](https://www.markdownguide.org/) if you’re new to it).
- Optional: Familiarity with Git, MkDocs, and `mkdocs-material` (no worries if not—we’ll cover web-based editing too!).

## Step-by-Step Guide

### Option 1: Contribute Using GitHub’s Web Interface (No Software Required)

This is the simplest way to make changes without installing anything.

#### Visit the Repository

- Go to `https://github.com/saiwal/hubzilla-docs`.
- You’ll see the project files, including a `docs/` folder where the documentation lives.

#### Switch to the Correct Version Branch

- Click the branch dropdown (it defaults to `main`).
- Select the branch for the version you’re editing (e.g., `10.0.8`). If it doesn’t exist yet, a maintainer may need to create it—open an issue to request it.

#### Find or Create a File

- Navigate to the `docs/` folder in the selected branch to edit an existing file (e.g., `index.md`).
- To add a new page, click “Create new file” at the top-right after navigating to `docs/`.

#### Edit the File

- Click the pencil icon (✏️) in the top-right corner of any `.md` file to edit.
- Make your changes using Markdown (e.g., add text, headers with `#`, lists with `-`, or code blocks with ```). The `mkdocs-material` theme supports rich formatting—see its [reference](https://squidfunk.github.io/mkdocs-material/reference/) for options like admonitions or tables.
- If creating a new file, name it descriptively (e.g., `new-feature.md`) and add your content.

#### Preview Your Changes

- Use the “Preview” tab above the editor to see how your Markdown will look (note: GitHub’s preview lacks `mkdocs-material` styling, so local testing is ideal for full accuracy).

#### Submit Your Changes

- Scroll to the “Commit changes” section.
- Write a short description (e.g., “Fixed typo in 10.0.8 install guide”).
- Ensure “Commit directly to the `[version]` branch” (e.g., `10.0.8`) is selected, *or* select “Create a new branch” if you’re proposing a new feature branch (e.g., `10.0.8-fix-typo`).
- Click “Commit changes.”

#### Open a Pull Request

- If you committed directly to the version branch (e.g., `10.0.8`), you’re done—maintainers will handle merging to `main` later.
- If you created a new branch, go to the “Pull requests” tab, click “New pull request,” set the base branch to your version (e.g., `10.0.8`), and submit it with a description.

#### Wait for Review

- A maintainer will review your changes. Once approved, they’ll merge your contribution into the version branch and eventually into `main` for publishing.

### Option 2: Contribute Using Git Locally (For Advanced Users)

If you prefer working locally and previewing the site with `mkdocs-material`, use this method.

#### Fork the Repository

- Go to `https://github.com/saiwal/hubzilla-docs`.
- Click “Fork” to create a copy under your GitHub account.

#### Clone Your Fork

- Open a terminal and run:  
  ```
  git clone https://github.com/YOUR-USERNAME/hubzilla-docs.git
  ```
  Replace `YOUR-USERNAME` with your GitHub username.
- Navigate into the folder:  
  ```
  cd hubzilla-docs
  ```

#### Switch to the Version Branch

- Check out the branch for the version you’re editing:  
  ```
  git checkout 10.0.8
  ```
  - If it doesn’t exist locally, fetch it:  
    ```
    git fetch origin
    git checkout 10.0.8
    ```
  - If the branch isn’t in the repo yet, create it:  
    ```
    git checkout -b 10.0.8
    ```

#### Set Up MkDocs and MkDocs-Material Locally

- Ensure Python is installed ([python.org](https://www.python.org/)).
- Install MkDocs and `mkdocs-material`:  
  ```
  pip install mkdocs mkdocs-material
  ```

#### Preview the Site

- Run:  
  ```
  mkdocs serve
  ```
- Visit `http://localhost:8000` to see the live site with `mkdocs-material` styling as you edit.

#### Make Your Changes

- Edit or create `.md` files in the `docs/` folder.
- Use `mkdocs-material` features like admonitions (e.g., `!!! note`) or tabs—see the [docs](https://squidfunk.github.io/mkdocs-material/).
- Stage and commit your changes:  
  ```
  git add .
  git commit -m "Updated 10.0.8 install instructions"
  ```

#### Push to Your Fork

- Push to the version branch in your fork:  
  ```
  git push origin 10.0.8
  ```

#### Create a Pull Request

- Go to your fork on GitHub (`https://github.com/YOUR-USERNAME/hubzilla-docs`).
- Click “Compare & pull request,” setting the base branch to `saiwal/hubzilla-docs`’s version branch (e.g., `10.0.8`).
- Add details and submit!

## Updating the Navigation

To add a new page to the site’s navigation:

### Open the Configuration File

- Open `mkdocs.yml` in the version branch (e.g., `10.0.8`).

### Modify the Navigation Section

- Find the `nav` section and add your page, e.g.:  
  ```
  nav:
    - Home: index.md
    - New Page: new-feature.md  # Your new file
  ```
- The `mkdocs-material` theme will reflect this in the sidebar.

### Submit the Change

- Submit this change via a pull request or direct commit to the version branch as described above.

## Tips for Success

- **Target the Right Branch**: Always make changes in the version branch (e.g., `10.0.8`), not `main`.
- **Leverage MkDocs-Material**: Explore its [features](https://squidfunk.github.io/mkdocs-material/) for rich formatting.
- **Keep it Clear**: Write simply and concisely for all Hubzilla users.
- **Test Locally**: Use `mkdocs serve` to preview with `mkdocs-material` styling.
- **Ask for Help**: Stuck? Open an issue on the repo or contact the community.

## After Submission

Once your changes are merged into the version branch (e.g., `10.0.8`), a maintainer will handle merging them into `main` for publishing. Your contribution will then go live at <https://saiwal.github.io/hubzilla-docs/>, styled beautifully with `mkdocs-material`. Thank you for improving Hubzilla’s documentation!

---
