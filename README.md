# The CLIMADA Teaching Materials Collection

This project collects all materials for learning climate risk assessment with CLIMADA and compiles them into an (interactive) [Jupyter Book](https://jupyterbook.org/).

Main version rendered here: https://climada-project.github.io/learn-climada/

## Build Instructions

To build the book locally, follow these instructions (assuming you have Mamba installed):

1. Install Jupyter Book into a suitable environment:

   ```
   mamba install -n <my-env> "jupyter-book"
   ```

2. Enter the environment:

   ```
   mamba activate <my-env>
   ```

3. Set up a local server hosting the book:

   ```
   jupyter book start
   ```

The URL to the server will be displayed. By default, it's `http://localhost:3000`.
You can access the book via this URL with your browser.
Any changes to the book source files will trigger a rebuild of the affected pages, automatically updating the output.

## Repository Structure

This repository uses a dedicated branch to deploy the rendered book on [GitHub Pages](https://docs.github.com/en/pages), called `gh-pages`.
Contrary to typical Git branches, which are intended to be merged into `main` at one point, `gh-pages` is a *deployment branch* that does not have any files in common with `main`.
Instead, it only contains the Jupyter Book output files needed for rendering the website.

In general, **do not push to `gh-pages` yourself!**

### Automated Deployment

Any pushes to `gh-pages` will trigger an automated GitHub Action that deploys these files to the final website.
These pushes do **not** happen manually but through the GitHub Action pipelines defined in other branches (mostly: `main`).

Pull requests trigger a slightly different pipeline.
The built output from PRs are pushed into `pr-preview/pr-NUM` subdirectories in the `gh-pages` branch.
From there, they are deployed to https://climada-project.github.io/learn-climada/pr-preview/pr-NUM/ for preview (in both cases, `NUM` is replaced by the PR number).
