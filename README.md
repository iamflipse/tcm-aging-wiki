# TCM Anti-Aging Wiki

A curated wiki distilling the 2026 JCMM review *"Traditional Chinese Medicine Formulas in Delaying Aging"* (Jin et al., DOI 10.1111/jcmm.71371, open access, PMC13620404).

**Public copy:** https://iamflipse.github.io/tcm-aging-wiki/ (read-only; static build served from the `gh-pages` branch)

## Contents

- **Concepts** (6 pages): classical TCM aging theories; TCM→14-hallmarks mapping (incl. proteomic aging clocks); four TCM formula mechanistic groups (ZGP/YGP, KXS, GQS, BYHWD, LWDHW, BZBC, GEG, SJZD, YSHSG); bioactive constituents & multi-compound synergy (saponins, flavonoids, polysaccharides, organic acids); methodological innovations (AI + network pharmacology, multi-omics, multi-level validation ladder); challenges & translational roadmap.
- **Source**: the paper's full text (incl. 261 references) at `src/sources/pmc-13620404-fulltext.md`.

## Corrections (2026-11-05)

The first build misread a few names and broke two tables while copying the paper. The source pages and `book/` are already fixed. The public site still serves the old build until `gh-pages` is updated. Do not regenerate these pages from the paper.

- **Guiqi Shen (GQS).** The formula page called GQS a Guilu Erxian Jiao lineage formula and stopped there. The paper's name for the modern oral liquid is Guiqi Shen. The paper does say it was refined from the Ming-dynasty Guilu Erxian Jiao. Guilu Erxian Jiao remains the separate formula, GEG.
- **Buyang Huanwu Decoction (BYHWD).** The page spelled it Buyang Huanwen.
- **Bazi Bushen Capsules (BZBC).** The page described the trial and left the formula unnamed.
- **Journal code.** The home page, about page, and this README said JCMMS. The journal is JCMM, *Journal of Cellular and Molecular Medicine*.
- **14 hallmarks.** The review lists 14 and attributes them to López-Otín. The 2023 López-Otín paper lists 12. The two this review adds are changes in the extracellular matrix and social-psychological isolation. The hallmarks page and the home page now say that. The paper's own sentences were left as written.
- **Full text.** The abbreviation list kept the long names and dropped the short forms (AD, GQS, BYHWD, and the rest). Those short forms were put back from the names the paper uses in the text. In Tables 1 and 2, 22 continuation rows had lost their first column, so a hallmark sat on the mechanism's row. Those rows were realigned. The paper's wording, including its own typos, was not rewritten.

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
