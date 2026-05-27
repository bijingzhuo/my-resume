---
title: Personal Resume Website
description: A personal resume/portfolio site built with Astro. Content and code are separated — updating experience or projects only requires editing Markdown files.
startDate: 2026-05-01
status: in-progress
tags: [Astro, CSS, GitHub Pages, Markdown]
repo: https://github.com/bijingzhuo/my-resume
featured: true
draft: false
---

A personal resume website built from scratch with Astro. The core goal is separation of content and code — all resume content lives in Markdown files, so updating experience or projects only requires editing `.md` files, never touching code.

## Tech choices

Astro was chosen for its native Content Collections support. Combined with Zod schemas, it validates Markdown frontmatter at build time, catching missing required fields early. Styles are hand-written in plain CSS with CSS custom properties for theming — no UI frameworks, keeping the bundle small.

## Features

- Project showcase: card list with detail pages, status badges (In Progress / Completed / Archived), and tag filtering
- Work experience: timeline layout with solid accent dots
- Education: timeline layout with hollow dots to visually distinguish from experience
- Light/dark mode: toggled via a `data-theme` attribute on `<html>`, preference persisted to localStorage, no flash on load

## Deployment

A GitHub Actions workflow watches for pushes to `main`, builds the site automatically, and publishes to GitHub Pages — no manual steps needed.
