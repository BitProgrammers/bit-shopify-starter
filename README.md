# Bit Programmers Shopify Starter Theme

A production-ready Shopify Online Store 2.0 starter theme optimized for high-performance builds. Based on Shopify Dawn, this repository is enhanced with strict development tooling and scalable, reusable components.

## Features
- **Architecture:** Built on standard Shopify Online Store 2.0 guidelines.
- **Development Tooling:** Shopify CLI, Theme Check, and Prettier integration.
- **CI/CD Pipeline:** Automated GitHub Actions for code linting and formatting validation.
- **Reusable Components:** Pre-built, modular Liquid sections and snippets designed for rapid deployment.

## Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/BitProgrammers/bit-shopify-starter.git
   ```
2. **Navigate to the project directory:**
   ```bash
   cd bit-shopify-starter
   ```
3. **Install dependencies:**
   ```bash
   npm install
   ```
4. **Authenticate with Shopify:**
   ```bash
   shopify auth login
   ```

## Development Commands

| Command | Description |
|---|---|
| `shopify theme dev` | Starts the local development server connected to your store. |
| `npm run format` | Runs Prettier to automatically format all Liquid, JS, CSS, and JSON files. |
| `shopify theme check` | Lints the theme code to ensure Shopify best practices. |
| `shopify theme pull` | Pulls the latest theme files from the connected store. |

## Folder Structure

```text
├── .github/             # GitHub workflows, issue templates, and contribution guidance
├── assets/              # Theme styles, scripts, and media files
├── config/              # Theme configuration and settings data
├── docs/                # Project documentation and supporting references
├── layout/              # Base layout files such as theme.liquid
├── locales/             # Storefront translation files
├── sections/            # Reusable section templates
├── snippets/            # Reusable UI snippets and components
├── templates/           # JSON templates for pages and storefront views
├── CHANGELOG.md         # Version history of the project
├── LICENSE.md           # Project license information
├── package.json         # Project scripts and development dependencies
├── README.md            # Main project documentation
└── release-notes.md     # Release summary notes
```

## Deployment

1. Ensure all local changes are committed, formatted, and pushed to `main`.
2. Verify that GitHub Actions (Lint & Theme Check) have passed successfully.
3. Use the Shopify GitHub integration in the target store's admin panel (**Online Store** > **Themes** > **Add theme** > **Connect from GitHub**) to pull the `main` branch.


## License

Based on the Shopify Dawn theme. Copyright (c) 2021-present Shopify Inc. See [LICENSE](/LICENSE.md) for further details.