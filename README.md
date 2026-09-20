# Resume Content — Demo

Sample resume content for [abdounikarim/resume](https://github.com/abdounikarim/resume),
a [JSON Resume](https://jsonresume.org/) build tool. This repo is included there as a git
submodule and used as the default `RESUME_CONTENT_DIR` — so `make html`/`make pdf` have
something to render right after installing, with no setup.

It's the classic "Richard Hendricks" JSON Resume sample (from the show *Silicon Valley*),
provided in two languages.

## Files

| File | Language |
|---|---|
| `resume.template.en.json` | English |
| `resume.template.fr.json` | French |

Each is a complete [JSON Resume](https://jsonresume.org/schema/) document — the same
format used for your own resume in the main project's `resume-content/` directory.

## Editing

Edit the JSON files directly; each key maps to a resume section (`basics`, `work`,
`education`, `skills`, etc. — see the [schema](https://jsonresume.org/schema/) for the
full list). Keep both language files in sync when you change one, since they're meant to
show the same person's resume in two languages, not two different resumes.

## Using this content

From the main project, with this repo checked out as its `resume-content-demo` submodule:

```bash
RESUME_CONTENT_DIR=resume-content-demo JSON_RESUMED_LANG=en make html
RESUME_CONTENT_DIR=resume-content-demo JSON_RESUMED_LANG=fr make html
```

Or set `RESUME_CONTENT_DIR=resume-content-demo` in `.env` (the default) and just run
`make html` / `make pdf` / `make watch`.
