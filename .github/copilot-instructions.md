# Copilot Instructions for djdarien.serveblog.net

This document provides guidance for AI coding agents working on the `djdarien.serveblog.net` codebase. It outlines the architecture, workflows, and conventions specific to this project to ensure productive contributions.

## Project Overview
- **Purpose**: This repository powers the `djdarien.serveblog.net` website, hosting various HTML pages, games, tools, and downloadable scripts.
- **Structure**:
  - Root directory contains primary HTML pages (e.g., `index.html`, `about.html`) and scripts.
  - `apps/` contains SWF files for Flash-based applications.
  - `files/` includes stylesheets and installer scripts.
  - `SPTT4/` is a subproject for a game, with its own `index.html`, `game.js`, and `styles.css`.
  - `uploads/` stores user-uploaded content in a nested directory structure.

## Key Conventions
- **HTML Pages**: Each page is standalone, with minimal shared components. Updates to one page do not automatically propagate to others.
- **CSS**: Styles are primarily defined in `files/main_style.css` and `SPTT4/styles.css`. Maintain consistency with existing styles.
- **JavaScript**: Scripts like `speedtest.js` and `SPTT4/game.js` are self-contained. Avoid introducing dependencies unless necessary.
- **File Organization**: Keep new files in their relevant directories (e.g., scripts in `files/`, styles in `files/theme/`).

## Developer Workflows
- **Testing**: Open HTML files in a browser to verify functionality. No automated tests are currently set up.
- **Debugging**: Use browser developer tools to debug JavaScript and inspect styles.
- **Deployment**: Changes are live once pushed to the `main` branch. Ensure thorough testing before committing.

## Integration Points
- **External Dependencies**:
  - `swfobject.js` is used for embedding Flash content.
  - `CNAME` configures the custom domain.
- **Cross-Component Communication**: Minimal. Each component (e.g., `SPTT4/`, `files/`) operates independently.

## Examples
- **Adding a New Page**:
  1. Create an HTML file in the root directory.
  2. Link necessary styles from `files/main_style.css`.
  3. Test the page in a browser.
- **Updating Styles**:
  1. Modify `files/main_style.css` or `SPTT4/styles.css`.
  2. Test changes across all affected pages.

## Notes for AI Agents
- Avoid introducing frameworks or libraries unless explicitly requested.
- Maintain the lightweight, static nature of the site.
- Document any significant changes in the commit message.

For questions or clarifications, consult the repository owner or contributors.