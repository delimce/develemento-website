# Repository Guidelines

## Project Structure & Media

The static website lives in `www/` and starts at `www/index.html`. Shared media remains at the repository root: brand files in `logo/` (component images in `logo/partes/`), other visual media in `images/`, and the supplied font in `fonts/`. Preserve source formats such as PSD files when adding optimized web exports. Use clear, descriptive filenames and avoid machine-specific or temporary files.

## Build, Test, and Development

The site is plain static HTML with no build or test toolchain. Preview it from the repository root with `python3 -m http.server 8000`, then open `http://localhost:8000/www/`. Keep page files and site-specific styles or scripts in `www/`. For changes, inspect the page in a browser and confirm referenced media paths resolve. Document any future build or test commands here if a toolchain is introduced.

## Style & Naming

Write repository documentation in English, with concise Markdown headings and direct instructions. Use lowercase, descriptive directory names and consistent filename conventions; retain existing names where renaming could break references. Keep original design files alongside exports when they are useful source material. Avoid committing duplicate exports unless they serve a distinct purpose.

## Website Images

Store images used by the finished website in `www/`. Choose formats, dimensions, and compression that preserve the visual quality needed at the rendered size while keeping file sizes efficient. Do not ship unnecessarily large originals when an appropriately optimized export will do; retain editable source files in the existing asset folders when needed.

## Testing Guidelines

No testing framework or coverage requirement is configured. For image changes, verify that files open correctly, have the intended dimensions and transparency, and are suitable for their intended use. For documentation-only changes, review the rendered Markdown and check links and paths.

## Commits & Pull Requests

The small Git history uses short, imperative summaries with an optional conventional prefix (for example, `docs: raw media files`). Follow that pattern: state the change clearly and keep commits focused. Pull requests should explain what was added or changed, identify affected asset paths, and include before/after screenshots when visual changes are involved. Link a related issue when one exists.

## Security & Configuration

Security comes first: never add, commit, print, summarize, or otherwise expose secret values in this repository. This includes API keys, access tokens, passwords, private keys, and credentials in examples, screenshots, logs, or configuration files. Use environment variables or an approved secret manager for runtime secrets, and use clearly fake placeholders in documentation. Keep private data, machine-specific configuration, caches, and temporary files out of the repository. If a secret is found in tracked files or Git history, treat it as exposed and follow the project's credential-rotation process; deleting the visible value alone is not sufficient.
