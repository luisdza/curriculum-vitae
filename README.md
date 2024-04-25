# Curriculum Vitae Project

## Overview
This project is designed to create and maintain a professional Curriculum Vitae (CV), resume, and cover letter using the R programming language. It utilises the vitae library to format these documents beautifully and leverages GitHub Actions for automated builds, ensuring that the latest versions of the documents are always available.

## Prerequisites
Before you begin, ensure you have the following installed:
*	R and RStudio
* The `vitae` package and other required packages. Install them using the following command in R:
```R
install.packages("vitae", dependencies = TRUE)
```

## Project Structure
* **cv.Rmd**: R Markdown file is used to create the Curriculum Vitae.
* **resume.Rmd**: R Markdown file is used to create a concise resume.
* **cover-letter.Rmd**: R Markdown file is used to create a cover letter.

Each of these files can be customised with personal information and professional details to generate PDFs or HTML documents.

## Getting Started
1. Clone the repository:
```bash
git clone https://github.com/luisdza/curriculum-vitae.git
``` 
2. Open the RStudio project file curriculum-vitae.Rproj.
3. Modify cv.Rmd, resume.Rmd, and cover-letter.Rmd with your details.
4. Render the documents locally using RStudio or use you can use the following R commands:

```R
rmarkdown::render("cv.Rmd")  # Generate only the CV
rmarkdown::render("resume.Rmd")  # Generate only the resume
rmarkdown::render("cover-letter.Rmd") # Generate only the cover letter 
```

## Automation with GitHub Actions
The project uses GitHub Actions to automatically build the PDFs or HTML documents whenever changes are pushed to the repository. The workflow is defined in `.github/workflows/build.yml`, which installs necessary R dependencies, renders the R Markdown files, and pushes the output files back to the repository or another specified location.

## Notes on Markdown Files
* `cv.Rmd`: Tailor this file with sections like education, experience, skills, etc. The vitae package will help format these sections.
* `resume.Rmd`: A more concise version of your CV, focusing on the most important achievements.
* `cover-letter.Rmd`: Includes placeholders for the job application specifics. Customise this document for each job application to address the particular requirements and how your skills and experiences align with them.

## Contributing
Contributions to this project are welcome! Feel free to fork the repository, make changes, and submit a pull request.

## License
This project is open-source and available under the MIT License.
