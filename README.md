# TCM Anti-Aging Wiki

A curated wiki distilling the 2026 JCMMS review *"Traditional Chinese Medicine Formulas in Delaying Aging"* (Jin et al., DOI 10.1111/jcmm.71371, open access, PMC13620404).

**Public copy:** https://iamflipse.github.io/tcm-aging-wiki/ (read-only; static build served from the `gh-pages` branch)

## Contents

- **Concepts** (6 pages): classical TCM aging theories; TCM→14-hallmarks mapping (incl. proteomic aging clocks); four TCM formula mechanistic groups (ZGP/YGP, KXS, GQS, BYHWD, LWDHW, BZBC, GEG, SJZD, YSHSG); bioactive constituents & multi-compound synergy (saponins, flavonoids, polysaccharides, organic acids); methodological innovations (AI + network pharmacology, multi-omics, multi-level validation ladder); challenges & translational roadmap.
- **Source**: the paper's full text (incl. 261 references) at `src/sources/pmc-13620404-fulltext.md`.

## Layout

- `src/` — markdown source pages (`index.md`, `about.md`, `concepts/`, `sources/`)
- `book/` — mdbook-generated static site (committed so GitHub Pages can serve it)
- `tools/mdbook` — mdbook v0.4.21 binary (aarch64 Linux, built from source)

## Rebuild + republish

```sh
./tools/mdbook build -d book
git add -A && git commit -m "update" && git push origin main
# republish: orphan gh-pages branch with book files at root, force push (see branch history)
```
