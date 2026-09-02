# personal site

personal site, built with [zola](https://www.getzola.org/), a fast static
site generator written in rust. zola takes the markdown files in `content/`
plus a theme (templates + css) and compiles the whole thing into plain html. no build step, no js framework, no server required to run it.

## theme

the theme ([terminus](https://github.com/ebkalderon/terminus)) lives in
`themes/terminus/` as a **git submodule**, not vendored/copied in directly.
that means this repo only tracks *which commit* of the theme to use, and the
actual theme code is pulled from its own upstream repo.

`config.toml` points at it with:

```toml
theme = "terminus"
```

### cloning this repo (submodules included)

submodules aren't cloned by default, so use one of:

```bash
git clone --recurse-submodules <this-repo-url>
```

or, if you already cloned without that flag:

```bash
git submodule update --init
```

### updating the theme

to pull in whatever's newest upstream on the theme's default branch:

```bash
git submodule update --remote themes/terminus
```

that updates the submodule's checked-out commit. review the diff, then commit
the bump like any other change:

```bash
git add themes/terminus
git commit -m "update terminus theme"
```

### adding a theme as a submodule (for reference)

this is how `themes/terminus` was set up in the first place, in case this
ever needs to be redone or repeated for a different theme:

```bash
git submodule add https://github.com/ebkalderon/terminus.git themes/terminus
```

then set `theme = "<name>"` in `config.toml` to match the folder name.

## commands

install zola first (see [getzola.org](https://www.getzola.org/documentation/getting-started/installation/)).
this site is built/tested against zola **0.22.x** — the theme currently
breaks on 0.23+ due to a tera macro-import change, so avoid installing latest
until that's fixed upstream.

```bash
# local dev server with live-reload, http://127.0.0.1:1111
zola serve

# one-off build into public/
zola build

# build into a specific directory instead (e.g. for github pages'
# "serve from /docs" option)
zola build -o docs

# validate content/links without writing any files
zola check
```

## structure

```
config.toml          site config (title, nav, taxonomies, theme, etc.)
content/              your actual pages/posts (markdown + toml frontmatter)
themes/terminus/       theme submodule — don't edit directly, changes won't persist
```
