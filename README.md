A single-page, one-column resume for software developers. It uses the base latex templates and fonts to provide ease of use and installation when trying to update the resume. The different sections are clearly documented and custom commands are used to provide consistent formatting. The three main sections in the resume are education, experience, and projects.

Based on the "Jake's Resume" template originally created by Sourabh Bajaj (MIT License), adapted here for Christopher Paraizo.

### Structure

```
resumes/
  christopher_paraizo_resume.tex   # generic resume, tracked in git
  tailored/                        # company-tailored variants, gitignored (local only)
```

Company-tailored versions live under `resumes/tailored/` and are excluded from version control (see `.gitignore`) so this public repo only ever shows the generic resume.

### Build using Docker

```sh
docker build -t latex .
docker run --rm -i -v "$PWD":/data latex pdflatex -output-directory=resumes resumes/christopher_paraizo_resume.tex
```

Or simply:

```sh
./build.sh
```

### License

Format is MIT; original template by Sourabh Bajaj. Resume content belongs to Christopher Paraizo.
