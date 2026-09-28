# Sarvamūla — data branch

Static datasets the reader fetches over jsDelivr. **Not a checkout of the
site**: this branch shares no history with `main` and is never merged into it.

| path | what it is |
|---|---|
| `manifest.json`, `postings/`, `units/`, `vocab/`, `words/` | the global search index |
| `_wordnet/` | Sanskrit WordNet |
| `_sandhi/` | sandhi-split database |
| `kavya_alankara/` | kāvya apparatus |

Served as `https://cdn.jsdelivr.net/gh/Tribhuvanachar/Sarvamula@<commit>/…`,
pinned to a commit so a reader's cached copy is never invalidated by an
unrelated push. `js/global-search.js`, `js/intellisense.js`, `js/ai.js`,
`js/kavya.js` and `js/config.js` hold those URLs.

## Why this branch exists

These four datasets used to be served from commits in the old `bhumandala`
repository (renamed to `JagatTest`) that **no branch pointed at any more**.
They survived only because GitHub had not yet garbage-collected them: fetchable
by SHA, reachable through a rename redirect, and one repository deletion away
from taking the site's search, WordNet, sandhi and kāvya features down with no
warning. A branch is a ref, and a ref is a promise.
