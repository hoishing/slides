---
marp: true
class: invert
math: mathjax
---

# marp

> quick slides generation with markdown

---

# divider

> how to define new slide

- by front matter
  - `headingDivider: 1` <-- use H1 to create new slide
  - `headingDivider: 2` <-- use both H1 and H2

- by markdown divider
  - `---`

---

# formatting

- format single page with HTML comment started with `_`
`<!-- _class: invert -->` color inversion = dark mode
`<!-- _class: lead -->` centering page for gaia theme

- header and footer, any **quoted** markdown

  ```yaml
  header: '[⬆](#1 " ")'  # emoji link to 1st page
  footer: '[](http://www.christopherhahne.de)'
  ```

---

# LaTeX support

- inline `$ ... $`

  write equation $ax^2+bc+c$ inline like this

- block `$$ ... $$`

$$ \int_0^1 \frac{dx}{e^x} = \frac{e-1}{e} $$

---

# front matter directives

> ref: https://marpit.marp.app/directives

- headingDivider: `int`
- theme: `default | gaia | uncover`
- style: `css`
- paginate: `bool`
- header: `markdown`
- footer: `markdown`
- class: class name, eg. `invert`
- color: `str` hex or html color

---

# front matter example

> global setup

```yaml
---
theme: gaia     # built-in theme
class: invert   # dark theme
style: |        # multiline support
  header {color: yellow;}
  footer a {color: pink;}
footer: '[![github-icon]][hoishing]' # quote markdown
---

[github-icon]: https://api.iconify.design/mdi/github.svg
[hoishing]: https://hoishing.github.io
```

---

# export

- single html
  - easy to deploy on any static host 👍
- pdf
  - well formatted
- pptx
  - can't edit text ⚠️
  - just static images embed in pptx

---

# ecosystem

- vscode plugin: https://github.com/marp-team/marp-vscode
- obsidian plugin: https://github.com/JichouP/obsidian-marp-plugin
- marp to github page: https://github.com/ralexander-phi/marp-to-pages
- marp-core: https://github.com/marp-team/marp-core
