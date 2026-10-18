# Repository Guidelines

## Project Structure & Source of Truth

This is an editorial asset project for 232 illustrated New Testament stories. The canonical story sequence, titles, and scene requirements live in `historia-novo-testamento.md`. Production state belongs exclusively in `status-criacao-historia.md`; use only `PENDENTE`, `EM PRODUÇÃO`, and `OK`. Image-generation rules are in `prompt-geracao-imagem.md`, while `prompt-geracao-imagem-slide.md` defines the later 232-slide PowerPoint assembly.

Project-scoped Higgsfield skills are installed under `.agents/skills/`. Use `higgsfield-generate` for every new or regenerated image; select another installed Higgsfield skill only when its specialized purpose applies (for example, `higgsfield-soul-id` for repeatable character identity). Do not bypass these skills with a different image generator.

## Image Production Workflow

Before each image, read both the status file and the exact numbered entry in `historia-novo-testamento.md`. Validate that number and title agree. A story marked `OK` requires explicit user confirmation before regeneration; `EM PRODUÇÃO` requires a decision to resume or restart. After a successful, visually reviewed generation only, add or update its ordered status entry to `OK`.

Follow the prompt’s required continuous horizontal children’s-book layout: at least six narrative/visual blocks, Brazilian Portuguese text, no central fold, and sections for **O QUE APRENDEMOS**, child-focused questions, and a short prayer. Preserve visual continuity for recurring people and historical settings. Never invent biblical events or substitute one story for another.

## Commands & Validation

There is no application build or automated test suite. Use PowerShell for repository checks:

```powershell
rg --files
Get-Content -Raw -Encoding utf8 historia-novo-testamento.md
```

Before slide assembly, verify 232 ordered story headings, one distinct image per story, and no missing or duplicate assets. The Higgsfield CLI must be installed and authenticated before its first use: `.\\.tools\\higgsfield\\hf.exe auth login`.

## Editing and Naming

Keep Markdown in UTF-8, retain the three-digit format (`001` through `232`), and write concise Brazilian Portuguese content. Do not rename the four canonical Markdown files. Name produced images with their three-digit story number and a descriptive slug, for example `001-mundo-antes-do-nascimento-de-jesus.png`.

## Version Control

This directory currently has no Git history. If Git is initialized, use short imperative commits (for example, `Add image for story 001`) and include the story number, title, resulting asset, and status update in pull-request descriptions.
