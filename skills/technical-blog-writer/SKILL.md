---
name: technical-blog-writer
description: Write developer-focused technical blog posts that rank in search and get cited by AI answer engines. Use when the user asks for a tutorial, how-to, comparison or explainer on programming, AI engineering, DevOps or web development.
---

# Technical Blog Writer

## Before writing
Confirm: target keyword and search intent, reader level (beginner, working dev, senior), stack and versions, and the one outcome the reader should get. If missing, assume a working developer and state the assumption in one line.

## Structure
1. **Title**: specific, includes the keyword, promises an outcome.
2. **Answer first**: 2-3 sentences that solve or summarise the problem before any backstory.
3. **Prerequisites**: versions and tools, as a short list.
4. **Steps**: each H2 is one action. Show the code, then explain why in 1-3 sentences.
5. **Common errors**: real error messages and fixes.
6. **Comparison or trade-offs**: a table when choosing between approaches.
7. **FAQ**: 3-5 questions real developers search, one-paragraph answers.
8. **Next steps**: links to related posts and docs.

## Quality bar
- All code must be complete enough to run. Pin versions. Mark anything you did not run as untested.
- No filler intros ("In today's fast-paced world"). No claims without a source or a reproducible example.
- Prefer concrete numbers over adjectives. Cite official docs for API behaviour.
- Short paragraphs, descriptive headings, one idea per section.

## Output
Return: SEO title, meta description (155 chars max), URL slug, the full post in Markdown, and suggested JSON-LD (`BlogPosting` + `FAQPage`).
