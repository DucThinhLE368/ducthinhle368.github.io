# Duc Thinh Le — Personal Website

Personal academic website of **Duc Thinh Le**, Lecturer in Control Engineering and Automation and Robot Engineering and Intelligent Systems at Thuyloi University, Vietnam.

🔗 Live site: [ducthinhle368.github.io](https://ducthinhle368.github.io)

## About this repository

This site is built with [Jekyll](https://jekyllrb.com/) on top of the [al-folio](https://github.com/alshedivat/al-folio) starter theme for academic websites, and deploys automatically to GitHub Pages on every push to `main`.

Content lives in data/markdown files, not templates:

- [`_data/cv.yml`](_data/cv.yml) — CV (education, experience, awards, publications, references)
- [`_bibliography/papers.bib`](_bibliography/papers.bib) — publication list
- [`_pages/about.md`](_pages/about.md) — homepage bio
- [`_teachings/`](_teachings/) — courses taught
- [`_config.yml`](_config.yml) — site-wide settings

## Local development

```bash
bundle install
bundle exec jekyll serve                      # dev server → http://localhost:4000/
bundle exec jekyll build --baseurl /al-folio   # production-style build
```

## Credits & License

Built on [al-folio](https://github.com/alshedivat/al-folio) (originally based on the [\*folio theme](https://github.com/bogoli/-folio) by [Lia Bogoev](https://liabogoev.com)), available under the [MIT License](LICENSE).

Personal content on this site (biography, CV, publications, photos) belongs to Duc Thinh Le and is not covered by that license.
