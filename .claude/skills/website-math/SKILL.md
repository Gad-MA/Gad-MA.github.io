---
name: website-math
description: How to write LaTeX math in this Hugo Blox (legacy Academic/Wowchemy) site so it renders correctly on desktop and phones. Use whenever writing, editing, converting or reviewing equations in any blog post, project page or other content under content/ (e.g. porting LaTeX to Markdown).
---

# Writing math on this website

The site is an old **Hugo Blox / Wowchemy (Academic) bootstrap theme** (`blox-bootstrap/v5@v5.9.6`), not the new Tailwind Hugo Blox. Legacy docs apply; customization goes in `assets/scss/custom.scss`, `assets/js/`, `data/`, and `layouts/` overrides, never in the theme module.

## How math is wired up (project overrides)

- **MathJax 4** (`mathjax@4/tex-chtml.js`), loaded through `data/assets.toml`. That file is a full copy of the theme's `assets.toml` with only `js.mathJax` changed; a partial file would replace the whole theme file and break the build. Do not shrink it.
- `assets/js/mathjax-config.js`: copy of the theme config plus `output: { displayOverflow: 'linebreak', linebreaks: { inline: false, width: '100%' } }`.
  - Long **display** equations break automatically (at `+`, `=`, relations).
  - **Inline** math never wraps.
- `assets/scss/custom.scss`: `mjx-container[display="true"] { overflow-x: auto; overflow-y: hidden; max-width: 100% }`. The theme's `.article-style` has `overflow: hidden`, so without this, anything too wide is silently clipped. With it, wide equations scroll sideways.
- After editing SCSS, restart `hugo server` (it may not recompile) and hard-refresh the browser (the CSS is cached).

## Syntax rules

- Inline: `$x_i$`. Display: `$$ ... $$`.
- **Wrap every display equation in the shortcode**, so Markdown does not touch the LaTeX (`\\`, `_`, `*`, `{`):
  ```
  {{< math >}}
  $$
  E(x,y) = D\!\left(s_y,\, P(s_x)\right)
  $$
  {{< /math >}}
  ```
- **Escape underscores in inline math as `\_`** (`$s\_x$`, `$f\_{\theta\_y}$`). Otherwise Markdown pairs underscores into `<em>` and mangles the formula. This also applies inside tables and list items. The backslash is consumed by Markdown, so MathJax sees `_`.
- Use `\text{ion}` / `\mathrm{...}` for word subscripts (`I_\text{Na}`), as in the Hodgkin-Huxley post.
- Multi-line derivations (genuinely several equations or steps) use `\begin{align} ... \\ ... \end{align}` inside `{{< math >}}`; one term per line with `&` alignment (see `content/post/synaptic-dynamics-with-hodgkin-huxley/index.md`).
- No `\label`/`\eqref`/`\ref`; refer to equations in words. No `booktabs`; tables are plain Markdown tables with inline math.
- Prefer `\bigl( ... \bigr)` etc. over `\left ... \right` for long groups (see below).

## Don't hand-break equations

The author **does not want manual line breaks** (`align*` + `\\`) on equations that fit or that should read as one unit (e.g. computational graphs, definitions). Let MathJax wrap and let the scroll fallback catch the rest. Only use `align`/`\\` when the source LaTeX is a real multi-step derivation.

## What MathJax cannot split (the usual cause of clipped/too-wide equations)

Automatic breaking happens only **between** pieces of an equation. These pieces are atomic:

- `\left( ... \right)` (stretchy groups): use `\bigl( ... \bigr)` (fixed size) for long groups so the contents stay breakable. Short groups can keep `\left/\right`.
- `\underbrace{...}_{\text{long label}}`: the label sets the term's width. Keep labels short (a word or two).
- `\frac`, `\sqrt{...}`, `\sum_{...}^{...}`: a long `\sqrt{...}` stacks its radical across lines when broken. Protect it (below).
- Inline math (never wraps): keep it under roughly 30 glyphs; move long formulas to a display block.

## Preventing a break

- `\hbox{$ ... $}` (or `\mbox{$...$}`): keeps a whole equation on one line. Use for chains/graphs such as `x \xrightarrow{} s_x \xrightarrow{} ...`. If the equation is wider than the screen it scrolls.
- `\begin{array}{c} ... \end{array}`: also unbreakable; good for a long `\sqrt{}`.
- `\nobreak` does **not** work reliably; don't rely on it.
- Wrapping changes only that equation; do not apply it to equations that wrap nicely.

## Known caveat: iPhone Safari

On the author's iPhone (Safari), long display equations (the InfoNCE and the four-term objective in the JEPA post) were **not** wrapped, they showed a single clipped line. The same page wraps fine in the Chromium preview. So never assume wrapping works on iOS; the scroll fallback is the guarantee. Prefer fitting what you can and tell the author to check on the phone.

## Testing checklist

1. `hugo server` (port 1313 is the author's; use another port for experiments) and open the page in the built-in browser.
2. Resize to **320px** wide (narrower than any iPhone) and to 402px (iPhone 17).
3. Measure instead of eyeballing: for each `mjx-container[display="true"]`, compare the max `right` of all descendants (`querySelectorAll('*')`) to the container's `right`. Anything wider should be scrollable (`overflow-x: auto`, `scrollWidth > clientWidth`) and the document must not scroll sideways (`document.documentElement.scrollWidth === innerWidth`). Checking only `mjx-math` width misses clipped sub-pieces.
4. No `mjx-merror` elements on the page.
5. When touching the MathJax or CSS setup, spot-check older math posts (`pinns`, `synaptic-dynamics-with-hodgkin-huxley`, `sliding-window-inference`).

## Scope

- Only change the post the author asked about. Site-wide math settings are already done; don't re-tune them per post.
- Reset any emulated viewport (`resize_window` preset `desktop`) when finished.
