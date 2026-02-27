# Repository Guidelines

## Project Structure & Module Organization
- Root content for this site lives in `_pages/`, `_posts/`, `_data/`, `assets/`, and `_config.yml`.
- Theme internals are in `_includes/`, `_layouts/`, and `_sass/minimal-mistakes/`.
- `docs/` contains the theme’s documentation/demo site; `test/` contains fixture content used for local theme validation.
- Generated output goes to `_site/` (and `test/_site/` during preview); do not hand-edit generated files.

## Build, Test, and Development Commands
- `bundle install`: install Ruby gems for local development.
- `bundle exec rake preview`: run the local preview server using `test/` as source at `http://localhost:4000/test/`.
- `bundle exec rake js`: rebuild `assets/js/main.min.js` from `assets/js/_main.js` and plugin/vendor files.
- `bundle exec rake`: run maintenance tasks (`copyright`, `changelog`, `js`, `version`).
- `bundle exec jekyll build --source test --destination test/_site`: one-off build check for theme changes.

## Coding Style & Naming Conventions
- Follow `.editorconfig`: 2-space indentation, LF line endings, UTF-8.
- Keep Markdown filenames and slugs lowercase with hyphens (example: `2026-01-30-easter-egg-hunt.md`).
- Use Jekyll naming conventions: dated posts in `_posts/`, reusable snippets in `_includes/`.
- Edit source files (`assets/js/_main.js`, Sass partials, layouts/includes), then regenerate compiled assets.

## Testing Guidelines
- This repository relies on integration-style validation (Jekyll build/preview) rather than unit tests.
- Before opening a PR, run `bundle exec rake preview` and confirm changed pages render correctly in `test/`.
- For JS or asset pipeline changes, run `bundle exec rake js` and verify no regressions in navigation/search behavior.

## Commit & Pull Request Guidelines
- Match existing history: short, imperative commit subjects (examples: `Update index`, `Remove emoji`, `Use png`).
- Keep commits focused by concern (content, layout, JS build, docs).
- PRs should include:
  - A concise summary of what changed.
  - Context or linked issue(s) when relevant.
  - Screenshots for UI/content layout changes.
- Base branches from `master` and use descriptive branch names (example: `fix/event-og-image`).
