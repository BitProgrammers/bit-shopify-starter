# Engineering Standards: Bit Programmers Starter Theme

This repository serves as the foundational architecture for all custom Shopify builds at Bit Programmers. We prioritize performance, scalable components, and clean Liquid structure.

## 1. Branching Convention
Never push directly to `main`. Always branch off `main` using strict naming conventions:
* `feature/` - New components, sections, or utilities (e.g., `feature/sticky-add-to-cart`)
* `fix/` - Bug resolutions (e.g., `fix/drawer-overflow`)
* `chore/` - Tooling, dependency updates, or pipeline changes
* `docs/` - Documentation updates (e.g., `docs/update-readme`)
* `release/` - Tagging a new production version (e.g., `release/v1.0.0`)

## 2. Code Quality & Tooling
Code is not subjective; it is mechanically enforced.
* **Prettier:** Run `npm run format` before every commit. Unformatted code will fail CI checks.
* **Theme Check:** Run `shopify theme check` locally to ensure Liquid best practices are met.
* **Coding Standards:** Review our strict [Coding Standards](docs/CODING_STANDARDS.md) for Liquid, JS, CSS, and Accessibility before writing code.

## 3. The Development Lifecycle & Pull Request Protocol
1. **Sync:** Pull the latest `main` branch (`git pull origin main`).
2. **Branch:** Create your working branch (`git checkout -b feature/your-feature-name`).
3. **Develop & Format:** Write clean code and run `npm run format` locally.
4. **Push:** Push your branch to the remote repository.
5. **Open a PR:** Open a Pull Request against `main` and complete the PR template entirely.
6. **Merge Requirements:** 
   * Automated GitHub Actions (Lint & Theme Check) must pass.
   * Obtain at least one code review approval from another engineer.