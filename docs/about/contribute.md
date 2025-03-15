# Contributing to This Documentation

Welcome! We’re thrilled to have you contribute to the Hubzilla documentation. This guide explains how to submit changes to our documentation, hosted at `https://github.com/saiwal/hubzilla-docs`. Whether you’re fixing a typo, adding a section, or improving clarity, your input makes a difference. Here’s how to get started.

## How Versioning Works

Our documentation uses a versioning system where each version (e.g., `10.0.8`) has its own branch in the repository. Changes should be made to the branch corresponding to the version you’re documenting (e.g., `10.0.8`). A maintainer will later merge these changes into the `main` branch for publishing. This keeps version-specific docs organized and up-to-date.

## Prerequisites

- A GitHub account (sign up at [github.com](https://github.com) if you don’t have one).
- Basic knowledge of Markdown (our docs are written in this format—check out a [Markdown guide](https://www.markdownguide.org/) if you’re new to it).
- Optional: Familiarity with Git and MkDocs (no worries if not—we’ll cover web-based editing too!).

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
- Make your changes using Markdown (e.g., add text, headers with `#`, lists with `-`, or code blocks with ```).
- If creating a new file, name it descriptively (e.g., `new-feature.md`) and add your content.

#### Preview Your Changes

- Use the “Preview” tab above the editor to see how your Markdown will look.

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

If you prefer working locally and previewing the site, use this method.

#### Fork the Repository

- Go to `https://github.com/saiwal/hubzilla-docs`.
- Click “Fork” to create a copy under your GitHub account.

#### Clone Your Fork

- Open a terminal and run:  
  ```bash
  git clone https://github.com/YOUR-USERNAME/hubzilla-docs.git
  ```
  Replace `YOUR-USERNAME` with your GitHub username.
- Navigate into the folder:  
  ```bash
  cd hubzilla-docs
  ```

#### Switch to the Version Branch

- Check out the branch for the version you’re editing:  
  ```bash
  git checkout 10.0.8
  ```
  - If it doesn’t exist locally, fetch it:  
    ```bash
    git fetch origin
    git checkout 10.0.8
    ```
  - If the branch isn’t in the repo yet, create it:  
    ```bash
    git checkout -b 10.0.8
    ```

#### Set Up MkDocs Locally

- Ensure Python is installed ([python.org](https://www.python.org/)).
- Install MkDocs:  
  ```bash
  pip install mkdocs
  ```
  If a theme like `mkdocs-material` is used, check `mkdocs.yml` and install it (e.g., `pip install mkdocs-material`).

#### Preview the Site

- Run:  
  ```bash
  mkdocs serve
  ```
- Visit `http://localhost:8000` to see the live site as you edit.

#### Make Your Changes

- Edit or create `.md` files in the `docs/` folder.
- Stage and commit your changes:  
  ```bash
  git add .
  git commit -m "Updated 10.0.8 install instructions"
  ```

#### Push to Your Fork

- Push to the version branch in your fork:  
  ```bash
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
  ```yaml
  nav:
    - Home: index.md
    - New Page: new-feature.md  # Your new file
  ```

### Submit the Change

- Submit this change via a pull request or direct commit to the version branch as described above.

## Tips for Success

- **Target the Right Branch**: Always make changes in the version branch (e.g., `10.0.8`), not `main`.
- **Keep it Clear**: Write simply and concisely for all Hubzilla users.
- **Test Locally**: Use `mkdocs serve` to preview your edits if possible.
- **Ask for Help**: Stuck? Open an issue on the repo or contact the community (add contact info if applicable).

## After Submission

Once your changes are merged into the version branch (e.g., `10.0.8`), a maintainer will handle merging them into `main` for publishing. Your contribution will then go live at [insert live site URL here, if available]. Thank you for improving Hubzilla’s documentation!

---

