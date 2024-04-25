# Curriculum-Vitae

This repository contains the source code for my curriculum vitae (CV) built using the R programming language with the vitae package. The vitae package provides a collection of LaTeX templates specifically designed to create CVs beautifully and easily directly from R Markdown files.

# Project Structure
* **cv.Rmd**: The main R Markdown file where the CV is written. It includes YAML front-matter for configurations and Markdown mixed with LaTeX for detailed entries.
* **cv.pdf**: The output CV file is in PDF format and was generated from the R Markdown file.

# Prerequisites
Before you can build the CV on your local machine, ensure you have the following installed:
* R
* RStudio (optional but helpful for editing R Markdown files)
* LaTeX (required for PDF generation)

# Building the CV
To build the CV to a PDF file, you can use the following R command:

```R
rmarkdown::render("cv.Rmd") 
```

This command will compile the R Markdown document into a PDF using LaTeX.

# Automating Build with GitHub Actions
This project uses GitHub Actions to automate the building of the CV. Whenever changes are pushed to the repository, GitHub Actions will run a workflow that executes the build process and updates the **cv.pdf** file.

# Workflow
The **.github/workflows/build_cv.yml** file contains the GitHub Actions workflow configuration. Here's what it does:
1. Set up R environment.
2. Install the required R packages.
3. Build the CV using R Markdown.
4. Commit the updated **cv.pdf** back to the repository if there are changes.

# Usage
To use this repository for your CV:
1. Fork the repository.
2. Clone your forked repository to your local machine.
3. Make your changes to the **cv.Rmd** file.
4. Push your changes back to GitHub to trigger the GitHub Actions workflow.

# License
This project is open-sourced under the MIT License.
