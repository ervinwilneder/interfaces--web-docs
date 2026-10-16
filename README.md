# POF

[![CI](https://github.com/ervinwilneder/interfaces--web-docs/actions/workflows/ci.yml/badge.svg)](https://github.com/ervinwilneder/interfaces--web-docs/actions/workflows/ci.yml)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

**Portable Organization Format**: a whole organization as one bundle of
Markdown files with YAML frontmatter (its roles, skills, policies,
objectives, routines, channels and connections, with the links between
them and, optionally, their history), readable by a person, an agent or
another system that imports it.

**📖 Full documentation: [pof.dev](https://pof.dev)**

## What this repo is

The documentation site for POF: the spec (revision 2026-10-16) and the
thinking behind it. A static [Nextra](https://nextra.site) site with no
backend of its own; its examples come from a real exported bundle.

The shape of a bundle:

```
POF.md                      manifest: type Bundle, format pof, revision
COMMITS.md                  the commits (optional)
roles/<team>/<slug>/ROLE.md
skills/<slug>/SKILL.md
policies/<slug>/POLICY.md
objectives/<slug>/OBJECTIVE.md
routines/<slug>/ROUTINE.md
channels/<slug>/CHANNEL.md
connections/<slug>/CONNECTION.md
extensions/<system>/        other systems' data, namespaced
```

## Local development

```bash
npm install
npm run dev    # http://localhost:3003
```

```bash
npm run build  # production build
npm run lint   # eslint
```

## Deployment

`pof.dev` is deployed manually via the Vercel CLI (`npm run deploy`), not
on every push to `main`: the Vercel project has no Git integration, and
connecting it for auto-deploy is a one-time step outside this repo's
control. A push here updates the source of truth; publishing it is a
separate, deliberate step.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md). Most useful contributions here
are corrections — if a page claims something about the format that
doesn't match reality, that's a real bug in documentation, not a
nitpick.

## License

[MIT](LICENSE)
