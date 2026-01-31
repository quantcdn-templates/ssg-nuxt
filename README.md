# Nuxt 3 Static Site Template for QuantCDN

A Nuxt 3 static site template with Vue 3, configured for deployment to QuantCDN.

[![Deploy to QuantCDN](https://www.quantcdn.io/img/quant-deploy-btn-sml.svg)](https://dashboard.quantcdn.io/projects/add/jamstack?template=nuxt)

## Features

- **Nuxt 3** - Latest version with Vue 3
- **Static Generation** - Pre-rendered HTML for blazing-fast performance
- **File-based Routing** - Automatic route generation from pages directory
- **Auto-imports** - Components, composables, and utilities auto-imported
- **TypeScript** - Full type safety
- **Automated Deployment** - GitHub Actions workflow for CI/CD

## Quick Start

1. Clone this repository
2. Install dependencies: `npm install`
3. Run locally: `npm run dev`
4. Visit `http://localhost:3000`

## Project Structure

```
.
├── .github/
│   └── workflows/
│       └── deploy.yml       # Automated deployment workflow
├── pages/
│   └── index.vue            # Home page
├── public/                  # Static assets
├── app.vue                  # Root component
├── nuxt.config.ts           # Nuxt configuration
├── package.json
└── README.md
```

## Deployment

This template includes a GitHub Actions workflow that automatically:
1. Builds your Nuxt site on every push to `main`
2. Deploys the static files to QuantCDN
3. Purges the CDN cache for instant updates

### Environment Variables

The following are automatically configured by QuantCDN:
- `QUANT_CUSTOMER` - Your Quant customer ID (repository variable)
- `QUANT_PROJECT` - Your Quant project ID (repository variable)
- `QUANT_TOKEN` - Your Quant API token (secret)

## Customization

### Adding Pages

Create new pages in the `pages/` directory:

```bash
touch pages/about.vue
```

The route will be automatically available at `/about`.

### Adding Components

Create components in the `components/` directory:

```bash
mkdir components
touch components/Header.vue
```

Components are auto-imported and can be used without explicit imports.

### Static Generation Configuration

This template uses `nuxt generate` for static site generation. Note that some Nuxt features require a server and won't work with static generation:

- API Routes (server routes)
- Dynamic routes without `prerender` configuration
- Server-only features

For dynamic routes, add them to `nuxt.config.ts`:

```typescript
export default defineNuxtConfig({
  nitro: {
    prerender: {
      routes: ['/blog/post-1', '/blog/post-2']
    }
  }
})
```

## Learn More

- [Nuxt 3 Documentation](https://nuxt.com/docs)
- [Nuxt Static Generation](https://nuxt.com/docs/getting-started/deployment#static-hosting)
- [Vue 3 Documentation](https://vuejs.org/)
- [Quant Documentation](https://docs.quantcdn.io/)
