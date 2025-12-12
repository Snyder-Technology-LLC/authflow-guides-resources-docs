# Authflow Documentation Style Guide

This guide defines the standards for all documentation in the Authflow docs repository.

---

## Document Header Format

Every document **must** begin with a standardized header:

```md
# Document Title

🟢 **Beginner** · ⏱️ ~5 min · 📘 Guide  
One-sentence description of what this document covers.

---
```

### Components

1. **Title** — Clear, action-oriented when possible
2. **Meta line** — Difficulty + Time + Category (single line, separated by ` · `)
3. **Description** — One sentence explaining the document's purpose
4. **Divider** — Horizontal rule before content begins

---

## Emoji Vocabulary

Use **only** these emojis. No exceptions.

### Difficulty Levels

| Emoji | Level | Use When |
|-------|-------|----------|
| 🟢 | Beginner | No prior knowledge needed |
| 🟡 | Intermediate | Some familiarity expected |
| 🔴 | Advanced | Expert-level content |

### Time Estimates

| Format | Examples |
|--------|----------|
| ⏱️ ~X min | ⏱️ ~2 min, ⏱️ ~5 min, ⏱️ ~10 min, ⏱️ ~15 min, ⏱️ ~20 min |

Round to nearest common increment: 1, 2, 3, 4, 5, 7, 10, 15, 20 minutes.

### Document Categories

| Emoji | Category | Use For |
|-------|----------|---------|
| 📂 | FAQ | Frequently asked questions |
| 📘 | Guide | Step-by-step walkthroughs, tutorials |
| 🧭 | Overview | Conceptual introductions, what/why content |
| 🛠️ | How-To | Task-focused instructions, troubleshooting |
| ⚙️ | Reference | Technical specs, API docs, settings |

---

## What NOT to Do

- ❌ Multiple emojis in the meta line
- ❌ Emojis in section headings (H2, H3, etc.)
- ❌ YAML frontmatter
- ❌ Badge images in content docs
- ❌ Repeating metadata throughout the document

---

## Section Headings

Use standard markdown headings without emojis:

```md
## Prerequisites       ✅ Good
## 🔧 Prerequisites    ❌ Bad (emoji in heading)
```

Exception: The main README.md uses emojis in headings for visual hierarchy — this is intentional for the landing page only.

---

## Examples

### Beginner Guide

```md
# Create Your First Paywall

🟢 **Beginner** · ⏱️ ~5 min · 📘 Guide  
Step-by-step guide to creating and configuring a paywall for your GPT.

---

## Navigate to Create Paywall
...
```

### Intermediate How-To

```md
# Instructions Character Limit

🟡 **Intermediate** · ⏱️ ~5 min · 🛠️ How-To  
Managing the 8,000 character limit for GPT instructions.

---

## Understanding the Limit
...
```

### Reference Document

```md
# Authflow Pricing Plans

🟢 **Beginner** · ⏱️ ~4 min · ⚙️ Reference  
Understanding Authflow's pricing tiers and choosing the right plan.

---

## Plan Comparison
...
```

---

## File Organization

```
content/
├── faq/
│   └── faq.md
├── getting-started/
│   ├── introduction.md
│   ├── create-account.md
│   └── ...
├── integration/
│   ├── custom-gpt-overview.md
│   └── ...
├── paywalls/
│   └── ...
└── troubleshooting/
    └── ...
```

- Group related docs in folders
- Use kebab-case for filenames: `create-paywall.md`, `gpt-authentication.md`
- No `_index.yaml` files — we use GitHub-native markdown only

---

## Writing Guidelines

1. **Lead with value** — Tell readers what they'll accomplish
2. **Be concise** — Shorter is better
3. **Use tables** — For comparisons and quick reference
4. **Use callouts** — GitHub blockquotes with `> **Note:**` or `> **⚠️ Important:**`
5. **Link generously** — Connect related docs

---

## Updating This Guide

If you need to add new emoji categories or modify standards, update this file and ensure all existing docs conform to the changes.
