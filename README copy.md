# architect

**Architecture Simplified** — https://abhishekvermax.github.io/architect/

## Publishing

Drop a `.md` file into a section folder, commit, push. GitHub Pages rebuilds automatically.

```
_ai-infrastructure/nccl-explained.md   →   /architect/ai-infrastructure/nccl-explained/
```

Minimum frontmatter:

```yaml
---
title: NCCL Explained
---
```

Optional: `subsection` (groups entries under a heading), `order` (lower sorts first, default 50), `summary`.

## Sections

| Layer | Folder | Section |
|---|---|---|
| 1 | `_foundations` | Foundations |
| 2 | `_distributed-systems` | Distributed Systems |
| 3 | `_data-engineering` | Data Engineering |
| 4 | `_data-platform` | Data Platform Architecture |
| 5 | `_platform` | Cloud & Platform Engineering |
| 6 | `_ai-infrastructure` | AI Infrastructure |
| 7 | `_genai` | Applied GenAI |
| 8 | `_mathematics` | Mathematics & Theory |
| 9 | `_economics` | Economics of Architecture |
| 10 | `_practice` | Architecture Practice |

Sub-sections need no folder — use the `subsection:` field.

## Adding a new section

1. Create `_new-section/` with a `.gitkeep`
2. Add it to `collections:` and `defaults:` in `_config.yml`
3. Add an entry to `_data/sections.yml`

## Enabling the site

Repo → Settings → Pages → Source: **Deploy from a branch** → `main` / `/ (root)`.

## Local preview (optional)

```bash
bundle install
bundle exec jekyll serve
```
