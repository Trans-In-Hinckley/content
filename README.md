# Trans in Hinckley – Content

This repository contains the content for the Trans in Hinckley website. It is consumed by the main site repository and synced into `src/content`.

## Structure

```text
content/
├── blog/              # Blog posts (MD/MDX)
├── help/
│   ├── businesses/        # Guidance for businesses and organisations
│   ├── familyandfriends/  # Guidance for family and friends
│   └── you/               # Guidance for trans and questioning people
└── legal/
    ├── privacy-policy.mdx
    └── safeguarding.mdx
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

The main site repository (`Trans-In-Hinckley/site`) syncs this content into its `src/content` directory for use with Astro Content Collections.

Typical workflow:

1. Edit content in this repository under `content/`.
2. In the site repo, run your sync step or copy updated files into `src/content` (for example `src/content/blog`, `src/content/legal`, etc.).
3. Commit changes in both repositories as needed.

## Contributing

If you’re contributing content:

- Use clear, inclusive language.
- Prefer UK English spelling.
- Avoid including personal data or identifying information about individuals.
