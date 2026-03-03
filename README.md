# nuxt-fsd

An agent skill for applying [Feature-Sliced Design](https://feature-sliced.design/) (FSD) architecture in [Nuxt 4+](https://nuxt.com/) projects.

## Install

```bash
npx skills add adamkasper/nuxt-fsd-skills
```

Or with a direct URL:

```bash
npx skills add https://github.com/adamkasper/nuxt-fsd-skills
```

## What it does

This skill teaches AI coding agents how to structure Nuxt 4+ projects using Feature-Sliced Design methodology. It covers:

- **Core principle**: FSD lives exclusively in `src/`, while Nuxt `app/` is the runtime shell that consumes it
- **Layer hierarchy**: `pages → widgets → features → entities → shared` (all in `src/`)
- **Thin page pattern**: `app/pages/` contains routing shells that delegate to FSD page slices in `src/pages/`
- **Import rules**: Strict downward-only imports with public API enforcement via `index.ts`, using `~~/src/` prefix
- **Pages-first workflow**: Start in `src/pages/`, extract only when reuse is proven (3+ usages)
- **Widget vs Feature decisions**: Coupled logic+UI (widget) vs standalone logic (feature)
- **TypeScript configuration**: Including `src/` in Nuxt's generated tsconfigs
- **Migration guide**: Adopting FSD in existing Nuxt projects

## When it activates

The skill activates when the agent encounters:

- Architecture decisions in a Nuxt project
- Questions about where to place new code
- Creating new pages, features, entities, or widgets
- Mentions of FSD, feature-sliced, layers, or slices
- Cross-module import decisions
- Code extraction and refactoring

## License

MIT
