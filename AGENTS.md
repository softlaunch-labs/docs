# Documentation project instructions

## About this project

- This is the documentation site for **Softlaunch**, a feature flag management platform.
- Built on [Mintlify](https://mintlify.com). Pages are MDX files with YAML frontmatter; site configuration lives in `docs.json`.
- For Mintlify product knowledge (components, configuration, writing standards), see the skills under `.agents/skills/` or the Mintlify MCP server `https://mintlify.com/docs/mcp`.

## Terminology

- **Organization** (or **org**) — the top-level account container. Match the app UI; do not use "workspace" or "project".
- **Environment** — an isolated set of flag configuration (for example, Production, Staging).
- **Flag** — a feature flag. Has a type (boolean, string, integer, numeric, or JSON).
- **Variation** — a possible value a flag can return.
- **Targeting rule** — a rule that serves a variation to a matching set of users. Use "targeting rule", never the internal term "assignment".
- **Audience** — a reusable, named group defined by targeting conditions.
- **Rollout** — a percentage-based gradual release.
- **SDK key** — the key an SDK uses to connect. A **client key** is safe for public clients; a **server key** is for trusted backends.
- **Subject** — the user or entity a flag is evaluated for, identified by a **subject key** with optional **attributes**.

## Style preferences

- Use active voice and second person ("you").
- Keep sentences concise — one idea per sentence.
- Use sentence case for headings.
- Neutral, professional tone. No marketing hype, superlatives, or competitor comparisons.
- Bold for UI elements: open **Settings**.
- Code formatting for file names, commands, paths, package names, and code references.
- Prefer Mintlify built-in components (`Steps`, `Tabs`, `CodeGroup`, `Card`, `CardGroup`, `Note`, `Tip`, `Warning`) over custom markup.
- Internal links are root-relative without an extension, for example `/sdks/react`.

## Content boundaries

- **Product-facing only.** Document what a user does and observes — never internal implementation, architecture internals, or engineering decisions.
- **Abstract the data layer.** Describe database-per-tenant isolation and CDN-backed local evaluation conceptually. Do not name the underlying database, storage, or infrastructure vendors.
- **No UI walkthroughs or screenshots yet.** The dashboard UI is evolving; keep dashboard steps high-level and text-only.
- **No CLI docs yet** — the CLI is in progress and will be documented separately.
- **No self-hosting docs yet** — covered later, once there is a tested guide.
- Only document shipped SDKs (`@softlaunch/react`, `@softlaunch/js`). Reference other SDKs as "coming soon" only.
