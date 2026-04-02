# Contributing

## Wiki

The wiki is a Git repo. Clone it, make changes, and push.

```bash
git clone https://github.com/your-org/wiki.wiki.git
cd wiki.wiki
git add .
git commit -m "docs: update <page name>"
git push origin master
```

To add a page, create a `.md` file and link to it from [Home](Home) or the relevant section page.

## Repositories

### Branches

```
main        — production
develop     — integration
feature/*   — new features
fix/*       — bug fixes
```

### Pull Requests

1. Branch from `develop`
2. Open a PR with a clear description
3. Get at least one approval
4. Ensure CI passes before merging

### Commits

Use [Conventional Commits](https://www.conventionalcommits.org):

```
feat: add login page
fix: correct date formatting
docs: update readme
chore: bump dependencies
```

---
[Home](Home) | [Getting Started](Getting-Started)
