# Repository Guidelines

## Project Structure & Module Organization

This repository is a dependency-free static site containing Chinese study notes about C pointers. All published files live at the repository root:

- `index.html` is the landing page and chapter directory.
- `C语言基础指针.html`, `C语言指针大小与内存地址.html`, and `C语言数组与指针.html` are standalone chapters.
- Each page keeps its CSS in an inline `<style>` block; there are currently no separate asset, source, or test directories.

When adding a chapter, create a descriptively named `.html` file and update the chapter links and ordering in `index.html` and the shared sidebar navigation on every chapter page.

## Build, Test, and Development Commands

No build step or package installation is required. Open `index.html` directly, or serve the repository locally to test links consistently:

```powershell
python -m http.server 8000
```

Then visit `http://localhost:8000/`. Before submitting changes, use `git diff --check` to detect whitespace errors and `git status --short` to confirm that only intended files changed.

## Coding Style & Naming Conventions

Use HTML5 with `<!doctype html>`, `lang="zh-CN"`, UTF-8 encoding, and the existing two-space indentation. Keep CSS declarations one per line and reuse the established custom properties such as `--paper`, `--ink`, and `--green`. Preserve the notebook-like visual language, responsive layout, and sidebar structure across chapters. Use semantic headings in order (`h1`, then `h2`, then `h3`) and meaningful fragment IDs. Chapter filenames should be concise Chinese topic names, following `C语言主题.html`.

## Testing Guidelines

There is no automated test framework or coverage target. Manually verify the landing page and every changed chapter in a browser at desktop and narrow viewport widths. Check that Chinese text renders correctly, navigation links and in-page anchors resolve, code examples remain readable, and no content overflows. For a new chapter, test links both from `index.html` and from each sidebar.

## Commit & Pull Request Guidelines

Recent commits use short, imperative Chinese summaries, for example `添加数组与指针笔记` and `调整笔记顺序并添加左侧导航`. Follow that style and keep each commit focused on one content or layout change.

Pull requests should summarize the affected chapters, explain content or navigation changes, and list manual checks performed. Include screenshots for visual or responsive-layout changes, and link the relevant issue when one exists.
