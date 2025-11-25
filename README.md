# Trans in Hinckley – Content

This repository contains the content for the Trans in Hinckley website. It is consumed by the main site repository as a Git submodule and then synced into `src/content` and `public/images`.

## Structure

```text
content/
├── files/
│   ├── blog/              # Blog posts (MD/MDX)
│   ├── help/
│   │   ├── businesses/        # Guidance for businesses and organisations
│   │   ├── familyandfriends/  # Guidance for family and friends
│   │   └── you/               # Guidance for trans and questioning people
│   └── legal/
│       ├── privacy-policy.mdx
│       └── safeguarding.mdx
└── images/
    └── blog/              # Images referenced by content (copied to public/images)
```

## Editing content

- Edit or add `.md`/`.mdx` files in the appropriate folder.
- Keep filenames and frontmatter (if used) stable where possible, as the site may rely on them for routing.

### Layouts for legal/help and blog content

MDX files can specify a layout in their frontmatter. The main site repo provides two layouts:

Example for a legal/help page:

```mdx
---
title: "Safeguarding"
---

Content…
```

Example for a blog post:

```mdx
---
title: "My First Post"
date: 2025-11-25
---

Post content…
```

## Using with the main site

The main site repository (`Trans-In-Hinckley/site`) includes this repo as a submodule at `site/content`. A sync script then:

- Copies `content/files/**` → `site/src/content/**` (for Astro Content Collections).
- Copies `content/images/**` → `site/public/images/**` (so paths like `/images/blog/...` work).

Typical workflow:

1. Edit markdown/MDX and other files under `content/files/`.
2. Add or update images under `content/images/`.
3. In the site repo, run `pnpm sync:content`.
4. Commit changes in both repositories as needed.

## Contributing

If you’re contributing content:

- Use clear, inclusive language.
- Prefer UK English spelling.
- Avoid including personal data or identifying information about individuals.
