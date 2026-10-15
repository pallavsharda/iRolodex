# iRolodex ◈

An offline-first, client-side Personal CRM progressive web application built for private Git-backed Markdown repositories.

iRolodex connects directly to your private GitHub notes repository, downloads structured Markdown and YAML frontmatter into client-side IndexedDB, and enables instant search, taxonomy filtering, and wikilink navigation on iOS and modern browsers without sending your private notes to third-party servers.

---

## Highlights

- **Offline-First via IndexedDB:** Your entire vault is cached locally. Search, filter, and read in Airplane Mode with zero latency.
- **Client-Side Git Trees API:** Pulls notes directly from your GitHub private repository using a fine-grained Personal Access Token.
- **Wikilink Resolution:** Obsidian-style `[[Target Note]]` and `[[Target Note|Alias]]` links resolve into in-app transitions with full back-stack history.
- **Dynamic Taxonomy:** Automatically derives Category and Tag filters from frontmatter metadata without preconfiguration.
- **Theme Adaptive:** Includes high-contrast Light and Dark palettes designed for mobile readability.
- **Zero Server Footprint:** 100% static client. Runs on GitHub Pages, Cloudflare Pages, or any static file host.

---

## Frontmatter Schema

iRolodex parses standard YAML frontmatter blocks into structured header metadata and categorizes them automatically:

```markdown
---
name: Alex Rivera
category: Advisory       # or 'type' (e.g., Person, Org, Advisory, Partner)
organization: Datadog
role: Principal Engineer
email: alex@datadog.com
tags: [infra, cloud, advisory]
last_contact: 2026-09-15
---

### Context
Met at Systems Conf 2024. Connected through [[Elena Rostova]].

### Interaction History
- 2026-09-15: Discussion on distributed storage engines.
