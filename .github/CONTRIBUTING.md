# Engineering Standards: Bit Programmers Starter Theme

This repository serves as the foundational architecture for all custom Shopify builds at Bit Programmers. We prioritize performance, scalable components, and clean Liquid structure.

## 1. Branching Convention
Always branch off `main` using strict naming conventions:
* `feat/` - New components, sections, or utilities (e.g., `feat/sticky-add-to-cart`)
* `fix/` - Bug resolutions (e.g., `fix/drawer-overflow`)
* `chore/` - Tooling, documentation, or dependency updates

## 2. Code Quality & Tooling
Code is not subjective; it is mechanically enforced.
* **Prettier:** Run `npm run format` before every commit. Unformatted code will fail CI checks.
* **Theme Check:** Run `shopify theme check` locally to ensure Liquid best practices are met.

## 3. Pull Request Protocol
1. Push your branch and open a PR against `main`.
2. Complete the Pull Request template entirely.
3. Ensure automated GitHub Actions (Lint & Theme Check) pass.
4. Obtain at least one code review approval from another developer before merging.