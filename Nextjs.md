# Next.js Fundamentals
- **React Framework**: Production-ready React with additional features.
- **Hybrid Rendering**: Supports SSG, SSR, ISR, and CSR in one app.
- **File-based Routing**: Files in `pages/` become routes (moved to `app/` in v13+).
- **Zero Config**: Automatic code splitting, bundling, and compilation.

# Core Features
- **Server Components**: Default in App Router (reduce client bundle size).
- **Client Components**: "use client" directive for interactivity.
- **Edge Runtime**: Run at edge locations for low latency.
- **Image Optimization**: Automatic resizing/optimization via `next/image`.
- **Font Optimization**: Automatic font face CSS with `next/font`.
- **Script Optimization**: Control third-party script loading with `next/script`.

# Rendering Strategies
- **Static Site Generation (SSG)**: Pre-render at build time (`getStaticProps`).
- **Server-Side Rendering (SSR)**: Render on each request (`getServerSideProps`).
- **Incremental Static Regeneration (ISR)**: Update static content after build.
- **Client-Side Rendering (CSR)**: Traditional React in-browser rendering.
- **Partial Prerendering**: New hybrid approach (experimental).

# Routing (App Router)
- **Folder Structure**: Routes map to `app/[route]/page.js` files.
- **Layouts**: Shared UI between routes (`layout.js`).
- **Loading States**: Automatic suspense boundaries (`loading.js`).
- **Error Handling**: Route-level error boundaries (`error.js`).
- **Route Groups**: Organize routes without affecting URL (`(group)`).
- **Dynamic Routes**: `[slug]` folders for parameterized routes.
- **Parallel Routes**: Simultaneously render multiple pages in same layout.
- **Intercepting Routes**: Show route in current context (modals).

# Data Fetching
- **Server Components**: Direct async components (no useEffect).
- **API Routes**: Create backend endpoints in `pages/api/` or `app/api/`.
- **fetch()**: Extended Web API with caching/revalidation.
- **Caching**: Control with `cache` and `next.revalidate` options.
- **Data Cache**: Persistent across deployments (configurable).
- **Router Cache**: Client-side cache of server payloads.

# Styling
- **CSS Modules**: Scoped styles (`*.module.css`).
- **Tailwind CSS**: First-class support with PostCSS.
- **Styled Components**: Requires client component and special config.
- **Sass**: Built-in support for `.scss` files.
- **CSS-in-JS**: Works with various libraries (emotion, styled-jsx).

# Optimization
- **Image Component**: Automatic lazy loading and placeholders.
- **Dynamic Imports**: Lazy load components (`next/dynamic`).
- **Bundle Analyzer**: Visualize bundle size (`@next/bundle-analyzer`).
- **Middleware**: Run code before requests (auth, redirects, etc.).

# API Features
- **Route Handlers**: Replace API Routes in App Router (`route.js`).
- **Server Actions**: Call server functions directly from components.
- **Edge API Routes**: Lightweight endpoints for edge runtime.

# Deployment
- **Static Export**: `next export` for fully static sites.
- **Node.js Server**: Traditional server deployment.
- **Vercel**: Optimized platform for Next.js.
- **Docker**: Containerized deployments supported.
- **ISR**: Revalidate content without redeploying.

# Authentication Patterns
- **Middleware**: Protect routes before rendering.
- **Auth.js**: NextAuth.js rebranded (OAuth, email, credentials).
- **Clerk**: Modern auth provider.
- **Supabase**: Integrated auth with Postgres.

# Best Practices
- **App Router**: Preferred over Pages Router for new projects.
- **Static First**: Use SSG/ISR whenever possible.
- **Client Boundaries**: Isolate interactivity to specific components.
- **Error Handling**: Implement route-level and global error boundaries.
- **TypeScript**: Fully supported with excellent DX.

# Common Patterns
- **Internationalization**: Built-in i18n routing or third-party libs.
- **Theming**: CSS variables + React context.
- **Analytics**: Vercel Analytics or third-party.
- **Preview Mode**: Bypass static generation for drafts.

# Troubleshooting
- **Hydration Mismatches**: Ensure server/client consistency.
- **Bundle Size**: Analyze with `@next/bundle-analyzer`.
- **Caching Issues**: Clear Next.js caches during development.
- **Legacy Behavior**: Check docs when migrating between versions.
