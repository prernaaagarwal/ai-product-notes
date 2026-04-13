# CLAUDE.md — AI Product Thinking

Rules for maintaining this blog. Follow all of these every time a post is published or the repo is updated.

---

## Repo Structure

```
ai-product-notes/
├── README.md          ← full post index, always current
├── CLAUDE.md          ← this file
└── posts/             ← all posts, slug-only filenames
```

---

## Rules — Always Follow When Publishing a Post

### 1. Filename format
- Always: `slug-only.md` — no date prefix
- Date lives in frontmatter `date:` field and in README table
- Wrong: `2026-04-14-product-ai-fit.md`
- Right: `product-ai-fit.md`

### 2. Blog README update (required on every publish)
- Add new post to the `## All Posts` table in `README.md`
- Position: newest first
- Format: `| YYYY-MM-DD | [Full Post Title](posts/slug.md) | tag1, tag2, tag3 |`
- Never leave a post out of the index

### 3. GitHub profile README (`prernaaagarwal/prernaaagarwal` repo)
- Update on every publish: add new post to writing section if relevant
- Link format: full GitHub URL with slug-only path
  - `https://github.com/prernaaagarwal/ai-product-notes/blob/main/posts/slug.md`

### 4. Cross-linking — mandatory on every publish
When a new post is published:

**Step A — link FROM the new post to existing posts:**
- Read the new post's topic and tags
- Identify 2-4 existing posts that are topically related
- Add them to the frontmatter `related:` list

**Step B — link TO the new post from existing posts:**
- For each related post identified in Step A, read its `related:` list
- If the new post is relevant to that existing post's reader, add a link back
- Update the frontmatter `related:` list
- Prioritize: posts covering the same theme, posts that provide complementary perspectives

### 5. Internal link format
- Always relative paths from the post's location: `slug.md` (same directory) or `../README.md`
- Never absolute GitHub URLs inside post bodies
- Never date-prefixed paths

---

## Quality Bar — Every Post Before Pushing

Run a quick check against these before every commit:

- [ ] Filename is slug-only (no date)
- [ ] Frontmatter has: title, date, tags, related
- [ ] Post has at least 2-3 related posts in frontmatter
- [ ] Blog README updated
- [ ] Profile README updated (if applicable)
- [ ] Existing posts updated with backlinks where relevant

---

## Content Guidelines

### What Belongs in This Repo

- AI product strategy and thinking
- Failure patterns and lessons learned
- System design for AI products
- Practical tradeoffs in AI product decisions
- Frameworks for evaluating AI fit

### What Does Not Belong

- Model benchmarks or technical comparisons
- Tool reviews or recommendations
- Hype cycle commentary
- Tutorial-style content
- Theory without practical application

### Writing Style

- Start with the problem or pattern
- Use concrete examples where possible
- Write for PMs who work with AI, not AI researchers
- Focus on decisions and tradeoffs, not abstractions
- Keep posts between 800-1500 words
- Use clear section headers for scannability

---

## Thought Process — Why These Rules Exist

**Why slug-only filenames?**
The GitHub file browser shows raw filenames. `product-ai-fit.md` reads like a post. `2026-04-14-product-ai-fit.md` reads like a dev log. The date prefix adds no value — it is already in the frontmatter and the README table.

**Why mandatory cross-linking?**
A blog where no posts know about each other is a collection, not a system. Cross-linking builds a reading path: someone who finds one post should be able to find everything related without going back to the index.

**Why bidirectional links?**
Unidirectional links mean old posts never benefit from new posts. Every time a new post is published, it usually extends or challenges an older post's ideas. That older post's reader deserves to know the conversation continued.
