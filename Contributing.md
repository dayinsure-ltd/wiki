# Contributing

Guidelines for contributing to this wiki and the organisation's repositories.

## Contributing to the Wiki

The wiki is backed by a Git repository. To make changes:

```bash
# Clone the wiki repo
git clone https://github.com/your-org/wiki.wiki.git
cd wiki.wiki

# Make your changes, then commit and push
git add .
git commit -m "docs: update <page name>"
git push origin master
```

### Adding a New Page

1. Create a new `.md` file in the root of the wiki repo
2. Use a descriptive name with hyphens (e.g. `My-New-Page.md`)
3. Link to it from [Home](Home) or another relevant page
4. Push the changes

### Style Guide

- Use `#` for the page title, `##` for sections, `###` for sub-sections
- Use tables for structured data
- Use fenced code blocks with a language tag for all code examples
- Keep pages focused — link to other pages rather than duplicating content

---

## Contributing to Repositories

### Branching Strategy

```
main / master   — production-ready code
develop         — integration branch
feature/<name>  — new features
fix/<name>      — bug fixes
chore/<name>    — maintenance tasks
```

### Pull Request Process

1. Branch off `develop` (or `main` for hotfixes)
2. Make your changes with clear, atomic commits
3. Open a PR with a descriptive title and summary
4. Request at least one reviewer
5. Ensure all CI checks pass before merging

### Commit Message Format

Follow [Conventional Commits](https://www.conventionalcommits.org/):

```
feat: add new feature
fix: resolve bug
docs: update documentation
chore: update dependencies
refactor: improve code structure
test: add missing tests
```

---

## See Also

- [Getting Started](Getting-Started)
- [Home](Home)
