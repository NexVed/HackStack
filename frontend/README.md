# HackStack: Frontend

A directory for choosing a frontend stack for hackathons and prototypes. Start with a framework or UI library, then pick a styling approach and components that fit it. The project links point to official docs or repositories for installation and licensing.

- [Core frontend frameworks and libraries](#1-core-frontend-frameworks-and-libraries)
- [App frameworks and static site tools](#2-app-frameworks-and-static-site-tools)
- [Styling and CSS](#3-styling-and-css)
- [Headless components and source-owned kits](#4-headless-components-and-source-owned-kits)
- [Styled UI libraries and design systems](#5-styled-ui-libraries-and-design-systems)
- [Build tools](#6-build-tools)
- [Prebuilt component sites, blocks, and templates](#7-prebuilt-component-sites-blocks-and-templates)
- [Design inspiration](#8-design-inspiration)
- [Animation, scrolling, and graphics](#9-animation-scrolling-and-graphics)
- [Routing and navigation](#10-routing-and-navigation)
- [State, data fetching, and realtime](#11-state-data-fetching-and-realtime)
- [Forms, validation, and identity](#12-forms-validation-and-identity)
- [Data grids, charts, maps, and editors](#13-data-grids-charts-maps-and-editors)
- [Icons, fonts, and media](#14-icons-fonts-and-media)
- [Accessibility and internationalization](#15-accessibility-and-internationalization)
- [Testing, mocking, and component development](#16-testing-mocking-and-component-development)
- [Build, lint, format, and package tooling](#17-build-lint-format-and-package-tooling)
- [Performance, SEO, and browser diagnostics](#18-performance-seo-and-browser-diagnostics)
- [Offline, storage, and browser APIs](#19-offline-storage-and-browser-apis)
- [Hosting and release workflows](#20-hosting-and-release-workflows)
- [Web fundamentals and security](#21-web-fundamentals-and-security)
- [Frontend launch checklist](#frontend-launch-checklist)

| If you need… | Start with |
|---|---|
| A client-side app with a ready-made UI | Vite + React + Mantine |
| A React app with custom component styling | Next.js + Tailwind CSS + shadcn/ui |
| Typed styles compiled at build time | StyleX, Panda CSS, or vanilla-extract |
| A Vue app with server rendering | Nuxt + Nuxt UI |
| A Svelte app with editable components | SvelteKit + shadcn-svelte |
| A content-heavy landing page | Astro + Tailwind CSS |
| A dashboard with tables and forms | Angular + PrimeNG, or Vue + PrimeVue |

## 1. Core frontend frameworks and libraries

| Tool | Type or ecosystem | Best for |
|---|---|---|
| [React](https://react.dev/learn) | Component library | Interactive apps with a broad ecosystem |
| [Vue](https://vuejs.org/guide/introduction.html) | Framework | Progressive adoption and single-file components |
| [Angular](https://angular.dev/overview) | Framework | Structured apps with built-in routing and dependency injection |
| [Svelte](https://svelte.dev/docs/svelte/overview) | Compiler framework | Components with built-in reactivity and scoped styles |
| [SolidJS](https://github.com/solidjs/solid) | UI library | Fine-grained reactivity with JSX |
| [Preact](https://preactjs.com/guide/v10/getting-started/) | UI library | Small React-compatible UI layer |
| [Qwik](https://qwik.dev/docs/) | Framework | Resumable rendering and deferred JavaScript |
| [Lit](https://lit.dev/docs/) | Web component library | Reusable custom elements across frameworks |
| [Alpine.js](https://alpinejs.dev/start-here) | UI library | Small interactions directly in HTML |
| [htmx](https://htmx.org/docs/) | HTML enhancement | Fetch and swap server-rendered HTML |
| [Ember](https://guides.emberjs.com/) | Framework | Convention-driven web applications |

## 2. App frameworks and static site tools

| Tool | Type or ecosystem | Best for |
|---|---|---|
| [Next.js](https://nextjs.org/docs) | React | Server rendering, route handlers, and React Server Components |
| [Nuxt](https://nuxt.com/docs) | Vue | File-based routing and hybrid rendering |
| [SvelteKit](https://svelte.dev/docs/kit) | Svelte | Routing, server loads, and deployment adapters |
| [Astro](https://docs.astro.build/) | Multi-framework | Content sites with selectively hydrated islands |
| [React Router](https://reactrouter.com/start/framework/installation) | React | Route modules, data loading, and server rendering |
| [TanStack Start](https://tanstack.com/start/latest) | React and Solid | Type-safe routing and server functions |
| [Remix](https://docs.remix.run/) | TypeScript | Web standards based full-stack apps |
| [SolidStart](https://docs.solidjs.com/solid-start) | Solid | Solid apps with server rendering |
| [Fresh](https://fresh.deno.dev/docs) | Deno and Preact | Server-rendered apps with islands |
| [Analog](https://analogjs.org/docs) | Angular | File-based routing and hybrid rendering |
| [RedwoodSDK](https://docs.rwsdk.com/) | React and Cloudflare | React apps built for Cloudflare |

## 3. Styling and CSS

| Tool | Type or ecosystem | Best for |
|---|---|---|
| [Tailwind CSS](https://tailwindcss.com/docs) | Utility CSS | Build designs by composing utility classes |
| [StyleX](https://stylexjs.com/) | Compiled styling | Author styles in JavaScript and extract atomic CSS |
| [UnoCSS](https://unocss.dev/) | Atomic CSS engine | Generate utilities on demand with configurable presets |
| [Panda CSS](https://panda-css.com/docs) | Build-time CSS-in-JS | Typed tokens, recipes, and design systems |
| [vanilla-extract](https://vanilla-extract.style/documentation/) | CSS-in-TypeScript | Typed themes and statically generated stylesheets |
| [CSS Modules](https://github.com/css-modules/css-modules) | Scoped CSS convention | Locally scoped class names with plain CSS syntax |
| [Emotion](https://emotion.sh/docs/introduction) | CSS-in-JS | Dynamic styles through JavaScript |
| [styled-components](https://styled-components.com/docs) | CSS-in-JS | Component-level styles in React |
| [Sass](https://sass-lang.com/documentation/) | Preprocessor | Mixins, modules, and reusable styles |
| [PostCSS](https://postcss.org/) | CSS transform tool | Plugin-based CSS processing |
| [Lightning CSS](https://lightningcss.dev/) | CSS transform tool | Compile, transform, and minify CSS |
| [Bootstrap](https://getbootstrap.com/docs/) | Styled CSS framework | Responsive layouts and familiar components |
| [Bulma](https://bulma.io/documentation/) | CSS framework | Flexbox layouts and CSS-only components |

## 4. Headless components and source-owned kits

| Tool | Type or ecosystem | Best for |
|---|---|---|
| [shadcn/ui](https://ui.shadcn.com/docs) | React | Add editable component source to your project |
| [Radix Primitives](https://www.radix-ui.com/primitives/docs/overview/introduction) | React | Unstyled dialogs, menus, and other primitives |
| [Base UI](https://base-ui.com/) | React | Unstyled components for custom design systems |
| [Headless UI](https://headlessui.com/) | React and Vue | Unstyled interactive controls |
| [React Aria](https://react-aria.adobe.com/) | React | Accessibility and interaction primitives |
| [Ark UI](https://ark-ui.com/) | Multiple frameworks | Headless controls built on state machines |
| [Reka UI](https://reka-ui.com/) | Vue | Unstyled component primitives for Vue |
| [Bits UI](https://bits-ui.com/docs) | Svelte | Headless components for Svelte |
| [shadcn-svelte](https://shadcn-svelte.com/) | Svelte | Editable component source with Tailwind |

## 5. Styled UI libraries and design systems

| Tool | Type or ecosystem | Best for |
|---|---|---|
| [Material UI (MUI)](https://mui.com/material-ui/) | React | Material Design components |
| [Chakra UI](https://chakra-ui.com/docs/get-started) | React | Composable components and design tokens |
| [Mantine](https://mantine.dev/) | React | Components, hooks, and forms |
| [Ant Design](https://ant.design/) | React | Data-heavy dashboards and enterprise forms |
| [React Bootstrap](https://react-bootstrap.netlify.app/) | React | React components styled with Bootstrap |
| [PrimeVue](https://primevue.dev/) | Vue | Data tables, forms, and interactive components |
| [Vuetify](https://vuetifyjs.com/) | Vue | Material Design components for Vue |
| [Nuxt UI](https://ui.nuxt.com/) | Vue and Nuxt | Tailwind-based components and themes |
| [Quasar](https://quasar.dev/) | Vue | Component suite and multi-target app tooling |
| [Skeleton](https://www.skeleton.dev/) | React and Svelte | Tailwind themes and UI components |
| [Angular Material](https://material.angular.dev/) | Angular | Material components backed by Angular CDK |
| [PrimeNG](https://primeng.dev/) | Angular | Data-heavy UI and widgets |
| [daisyUI](https://daisyui.com/docs/) | Tailwind CSS | Themeable components via CSS class names |
| [Flowbite](https://github.com/themesberg/flowbite) | Tailwind CSS | Ready-made components and interaction scripts |
| [Web Awesome](https://webawesome.com/) | Web components | Styled custom elements across frameworks |
| [Ionic Framework](https://ionicframework.com/docs) | Web components | Mobile-style interfaces for web and hybrid apps |

## 6. Build tools

| Tool | Type or ecosystem | Best for |
|---|---|---|
| [Vite](https://vite.dev/guide/) | Build tool | Start a client-side app with framework templates |

## 7. Prebuilt component sites, blocks, and templates

Use these catalogs to browse live examples and find reusable UI. Some entries are standalone components, while blocks combine components into sections such as hero banners, pricing tables, and dashboards.


### React animations and component effects

| Site | Stack | What to browse |
|---|---|---|
| [React Bits](https://www.reactbits.dev) | React | Animated text, backgrounds, and interactive effects |
| [React Bits Pro](https://pro.reactbits.dev) | React | Commercial blocks and templates from React Bits |
| [Skiper UI](https://skiper-ui.com/components) | React | Animated components and interactions |
| [Aceternity UI](https://ui.aceternity.com/explore) | React and Tailwind CSS | Animated landing page components, blocks, and templates |
| [Magic UI](https://magicui.design) | React | Animated components and effects for product sites |
| [Animate UI](https://animate-ui.com) | React | Animated interactive primitives and components |
| [Kokonut UI](https://kokonutui.com) | React and Tailwind CSS | Copyable effects and application components |
| [](https://undefined) | undefined | undefined |

### Component registries and design kits

| Site | Stack | What to browse |
|---|---|---|
| [21st.dev](https://21st.dev) | React | Community catalog of components, themes, and templates |
| [shadcn Registry Directory](https://ui.shadcn.com/docs/directory) | shadcn registries | Official index of third-party registries |
| [Registry Directory](https://registry.directory) | shadcn registries | Independent search across registries |
| [coss ui](https://coss.com/ui/docs/get-started) | React | Components from the Cal.com design system |
| [Shadcnblocks](https://www.shadcnblocks.com) | React and shadcn/ui | Ready-made page sections and templates |
| [Untitled UI](https://www.untitledui.com) | React and Figma | Matching design assets and React components |
| [Creative Tim](https://www.creative-tim.com) | Multiple stacks | Dashboards, starter kits, and full-page templates |
| [Relume](https://www.relume.ai) | Design and site building | Marketing site sections and page layouts |
| [](https://undefined) | undefined | undefined |

### Tailwind and plain CSS snippets

| Site | Stack | What to browse |
|---|---|---|
| [Tailwind Plus](https://tailwindcss.com/blog/tailwind-plus) | Tailwind CSS | Commercial UI blocks and templates, formerly Tailwind UI |
| [HyperUI](https://hyperui.dev) | Tailwind CSS | Free marketing, ecommerce, and application snippets |
| [Preline UI](https://preline.co) | Tailwind CSS | Styled blocks and interactive components |
| [Tailblocks](https://tailblocks.cc) | Tailwind CSS | Copyable page sections |
| [Mamba UI](https://mambaui.com) | Tailwind CSS | Free blocks and templates |
| [Meraki UI](https://merakiui.com) | Tailwind CSS | Responsive sections and controls |
| [TailGrids](https://tailgrids.com) | React and Tailwind CSS | Application and marketing components |
| [FlyonUI](https://flyonui.com) | Tailwind CSS | Styled interactive components |
| [Sailboat UI](https://sailboatui.com) | Tailwind CSS | Common layouts and components |
| [Uiverse](https://uiverse.io) | CSS and Tailwind CSS | Community snippets for buttons, loaders, and effects |
| [](https://undefined) | undefined | undefined |

### Vue and Svelte collections

| Site | Stack | What to browse |
|---|---|---|
| [Inspira UI](https://inspira-ui.com/docs/en/components) | Vue and Nuxt | Animated sections and effects |
| [Vue Bits](https://vue-bits.dev) | Vue | Animated text, backgrounds, and interactions |
| [shadcn-vue](https://shadcn-vue.com) | Vue | Editable component source and examples |
| [shadcn-svelte](https://shadcn-svelte.com) | Svelte | Editable components and blocks |

Check the license of the specific component, block, or template before using it. Free previews and commercial downloads can have different terms. Check framework, Tailwind, and animation dependencies when copying source.

## 8. Design inspiration

Use these galleries to explore a visual direction, compare page layouts, or study how real products handle a task.

| Site | Best for |
|---|---|
| [Pinterest](https://www.pinterest.com/) | Mood boards, color palettes, and visual references |
| [Dribbble](https://dribbble.com/) | UI concepts, illustrations, and motion studies |
| [Behance](https://www.behance.net/) | Branding projects, portfolios, and design case studies |
| [Are.na](https://www.are.na/) | Collecting references into themed channels |
| [Designspiration](https://www.designspiration.com/) | Visual references across typography, art, and photography |
| [Awwwards](https://www.awwwards.com/) | Awarded websites, creative layouts, and web interactions |
| [CSS Design Awards](https://www.cssdesignawards.com/) | Website showcases and interactive design |
| [Siteinspire](https://www.siteinspire.com/) | Curated websites organized by style and subject |
| [Landbook](https://land-book.com/) | Landing pages, portfolios, and product websites |
| [Lapa Ninja](https://www.lapa.ninja/) | Landing page layouts and marketing sections |
| [One Page Love](https://onepagelove.com/) | One-page portfolios, product launches, and landing pages |
| [Landingfolio](https://www.landingfolio.com/) | Landing pages and individual sections such as pricing or headers |
| [Mobbin](https://mobbin.com/) | Real mobile and web app screens and user flows |
| [Page Flows](https://pageflows.com/) | Recorded product flows such as onboarding and checkout |
| [Refero](https://refero.design/) | UI patterns from real web and mobile products |
| [SaaSFrame](https://www.saasframe.io/) | SaaS marketing pages and product interfaces |
| [Really Good Emails](https://reallygoodemails.com/) | Welcome, transactional, and marketing email layouts |
| [Typewolf](https://www.typewolf.com/) | Typeface pairings and typography on real websites |
| [Fonts In Use](https://fontsinuse.com/) | Examples of typefaces in branding, print, and digital work |

For a hackathon, start with Pinterest or Are.na for a mood board, Landbook or Lapa Ninja for page structure, and Mobbin or Page Flows for interactions. Check reuse terms before copying images, fonts, or templates from a reference.

## 9. Animation, scrolling, and graphics

| Library | Type | Best for |
|---|---|---|
| [GSAP](https://gsap.com/) | JavaScript animation engine | Coordinating multi-step animations, SVG motion, and scroll-linked timelines with ScrollTrigger |
| [Anime.js](https://animejs.com/) | JavaScript animation engine | Animating DOM elements, SVGs, and JavaScript values with timelines and staggered effects |
| [Animate.css](https://animate.style/) | CSS animation presets | Adding common entrance, exit, and attention effects with class names |
| [Motion](https://motion.dev/) | JavaScript and React animation | Gestures, layout transitions, and spring animations in interactive UIs |
| [React Spring](https://www.react-spring.dev/) | React animation library | Physics-based movement with configurable springs |
| [AutoAnimate](https://auto-animate.formkit.com/) | Layout animation utility | Animating list items as they enter, leave, or reorder |
| [Lenis](https://lenis.dev/) | Smooth scrolling library | Smoothing page scroll and coordinating scroll position with animation |
| [ScrollReveal](https://scrollrevealjs.org/) | Scroll reveal library | Revealing elements as they enter the viewport |
| [Lottie Web](https://github.com/airbnb/lottie-web) | Animation player | Playing exported Lottie JSON animations on the web |
| [Rive](https://rive.app/) | Animation editor and runtimes | Playing interactive animations driven by state machines |
| [Three.js](https://threejs.org/) | 3D graphics library | Building custom browser scenes, model viewers, and visual effects |
| [React Three Fiber](https://r3f.docs.pmnd.rs/) | React renderer for Three.js | Building and updating Three.js scenes with React components |
| [Babylon.js](https://www.babylonjs.com/) | 3D engine | Building interactive 3D experiences with engine tooling |
| [PixiJS](https://pixijs.com/) | 2D graphics renderer | Rendering sprites, particles, and interactive 2D scenes |
| [Remotion](https://www.remotion.dev/) | React video framework | Composing and rendering programmatic video |

Use **GSAP** for choreographed sequences, **Motion** for React UI transitions, and **Lenis** when you need smooth scrolling. Use **Three.js** or **React Three Fiber** for 3D scenes. Honor the user's reduced-motion preference and test scroll effects with keyboard navigation and on touch devices.

## 10. Routing and navigation

| Resource | Best for |
|---|---|
| [TanStack Router](https://tanstack.com/router/latest) | Type-safe React and Solid routing |
| [Vue Router](https://router.vuejs.org/) | Official routing for Vue |
| [Angular Router](https://angular.dev/guide/routing) | Angular navigation, guards, and route loading |

## 11. State, data fetching, and realtime

| Resource | Best for |
|---|---|
| [TanStack Query](https://tanstack.com/query/latest) | Server-state caching and invalidation |
| [SWR](https://swr.vercel.app/) | React data fetching and revalidation |
| [Redux Toolkit](https://redux-toolkit.js.org/) | Structured shared React or JavaScript state |
| [Zustand](https://zustand.docs.pmnd.rs/) | Small shared state stores |
| [Pinia](https://pinia.vuejs.org/) | Vue application state |
| [XState](https://stately.ai/docs) | State machines for complex flows |
| [Apollo Client](https://apollographql.com/docs/react) | GraphQL queries and normalized caching |
| [Socket.IO Client](https://socket.io/docs/v4/client-api/) | Realtime events with a compatible Socket.IO server |

## 12. Forms, validation, and identity

| Resource | Best for |
|---|---|
| [React Hook Form](https://react-hook-form.com/docs) | React forms with validation and controlled inputs |
| [TanStack Form](https://tanstack.com/form/latest) | Typed form state and validation |
| [VeeValidate](https://vee-validate.logaretm.com/) | Form validation for Vue |
| [Zod](https://zod.dev/) | TypeScript schemas and data validation |
| [Valibot](https://valibot.dev/) | Modular schema validation |
| [Auth.js](https://authjs.dev/) | Session and sign-in integration with supported frameworks |
| [Clerk](https://clerk.com/docs) | Hosted identity with prebuilt sign-in components |

## 13. Data grids, charts, maps, and editors

| Resource | Best for |
|---|---|
| [TanStack Table](https://tanstack.com/table/latest) | Headless table logic |
| [TanStack Virtual](https://tanstack.com/virtual/latest) | Render visible rows in large lists |
| [AG Grid](https://ag-grid.com/) | Feature-rich grids with Community and Enterprise editions |
| [Chart.js](https://www.chartjs.org/docs/latest/) | Common charts on canvas |
| [Apache ECharts](https://echarts.apache.org/) | Interactive charts and dashboards |
| [D3](https://d3js.org/) | Custom data visualizations |
| [Leaflet](https://leafletjs.com/) | Interactive web maps |
| [MapLibre GL JS](https://maplibre.org/maplibre-gl-js/docs/) | Vector maps and map styling |
| [Tiptap](https://tiptap.dev/docs) | Rich-text editing with extensible schemas |
| [Lexical](https://lexical.dev/docs/intro) | Extensible rich-text editor framework |
| [Monaco Editor](https://microsoft.github.io/monaco-editor/) | Browser code editing |
| [CodeMirror](https://codemirror.net/) | Configurable code editing |
| [React Flow](https://reactflow.dev/) | Node-based diagrams and workflow editors |
| [Uppy](https://uppy.io/docs/) | File upload UI and resumable upload integrations |

## 14. Icons, fonts, and media

| Resource | Best for |
|---|---|
| [Lucide](https://lucide.dev/) | Consistent SVG icons |
| [Heroicons](https://heroicons.com/) | Outline and solid SVG icons |
| [Iconify](https://iconify.design/) | Access to many icon collections |
| [Fontsource](https://fontsource.org/) | Self-hosted font packages |
| [Google Fonts](https://fonts.google.com/) | Browse typefaces and their licenses |
| [Unsplash](https://unsplash.com/license) | Photography with published reuse terms |
| [SVGOMG](https://jakearchibald.github.io/svgomg/) | Optimize SVG files in the browser |
| [Squoosh](https://squoosh.app/) | Compress and compare image formats |

## 15. Accessibility and internationalization

| Resource | Best for |
|---|---|
| [WCAG](https://w3.org/WAI/standards-guidelines/wcag/) | Accessibility standards and guidance |
| [ARIA Authoring Practices Guide](https://w3.org/WAI/ARIA/apg/) | Keyboard and focus patterns for common widgets |
| [axe-core](https://github.com/dequelabs/axe-core) | Automated accessibility checks |
| [Accessibility Insights](https://accessibilityinsights.io/) | Browser accessibility checks and guided assessments |
| [i18next](https://www.i18next.com/) | Translation resources and localization |
| [FormatJS](https://formatjs.github.io/) | Locale-aware messages, dates, and numbers |
| [Vue I18n](https://vue-i18n.intlify.dev/) | Translations and formatting for Vue |

## 16. Testing, mocking, and component development

| Resource | Best for |
|---|---|
| [Vitest](https://vitest.dev/) | Unit and integration tests in Vite-based projects |
| [Jest](https://jestjs.io/docs/getting-started) | JavaScript test runner and mocks |
| [Testing Library](https://testing-library.com/) | Component tests based on user interactions |
| [Playwright](https://playwright.dev/docs/intro) | Cross-browser end-to-end and screenshot tests |
| [Cypress](https://docs.cypress.io/) | End-to-end and component tests |
| [Mock Service Worker](https://mswjs.io/) | Mock network requests in development and tests |
| [Storybook](https://storybook.js.org/docs) | Develop and document components in isolation |
| [Chromatic](https://chromatic.com/docs/) | Hosted visual review and regression testing |
| [agent-qa](https://vostride.com) | Natural-language web, Android and iOS QA with persistent [memidex memory](https://vostride.com/docs/agent-qa/memory.md), validated [self-improvement](https://vostride.com/docs/agent-qa/self-improvement.md), and recorded evidence via CLI, local dashboard or MCP. Early-stage; [FSL-1.1-ALv2](https://vostride.com/license.md) restricts competing use. Software is free for permitted use; model/infrastructure costs are separate ([pricing](https://vostride.com/pricing.md), checked 2026-11-08). |

## 17. Build, lint, format, and package tooling

| Resource | Best for |
|---|---|
| [TypeScript](https://www.typescriptlang.org/docs/handbook/intro) | Static checking for JavaScript projects |
| [ESLint](https://eslint.org/docs/latest/) | Configurable lint rules |
| [Prettier](https://prettier.io/docs/) | Consistent code formatting |
| [Biome](https://biomejs.dev/) | Formatting and linting in one tool |
| [pnpm](https://pnpm.io/) | Package management and workspaces |
| [Webpack](https://webpack.js.org/) | Configurable bundling |
| [Rollup](https://rollupjs.org/) | Bundling reusable libraries |
| [Rspack](https://rspack.rs/) | Webpack-compatible bundling for many projects |

## 18. Performance, SEO, and browser diagnostics

| Resource | Best for |
|---|---|
| [Lighthouse](https://developer.chrome.com/docs/lighthouse/overview) | Audit performance, accessibility, and SEO |
| [PageSpeed Insights](https://pagespeed.web.dev/) | Lab results and field data when available |
| [web-vitals](https://github.com/GoogleChrome/web-vitals) | Measure Core Web Vitals in production |
| [Chrome DevTools](https://developer.chrome.com/docs/devtools/) | Inspect network, rendering, and runtime behavior |
| [Google Search Central](https://developers.google.com/search/docs) | Crawling, indexing, and structured data guidance |
| [Schema.org](https://schema.org/) | Vocabulary for structured data |
| [Sentry](https://docs.sentry.io/platforms/javascript/) | Frontend error reporting and performance monitoring |

## 19. Offline, storage, and browser APIs

| Resource | Best for |
|---|---|
| [Workbox](https://developer.chrome.com/docs/workbox/) | Service-worker caching and offline workflows |
| [Dexie](https://dexie.org/) | IndexedDB wrapper for browser storage |
| [MDN Service Workers](https://developer.mozilla.org/en-US/docs/Web/API/Service_Worker_API) | Offline behavior and background request handling |
| [MDN Web Workers](https://developer.mozilla.org/en-US/docs/Web/API/Web_Workers_API) | Move CPU-heavy work off the UI thread |
| [MDN Web App Manifest](https://developer.mozilla.org/en-US/docs/Web/Progressive_web_apps/Manifest) | Install metadata for web apps |

## 20. Hosting and release workflows

| Resource | Best for |
|---|---|
| [GitHub Pages](https://docs.github.com/en/pages) | Static sites published from a repository |
| [Cloudflare Pages](https://developers.cloudflare.com/pages/) | Static deployments and supported functions |
| [Netlify](https://docs.netlify.com/) | Git-based deploys and preview URLs |
| [Vercel](https://vercel.com/docs) | Preview and production deploys for supported frameworks |
| [GitHub Actions](https://docs.github.com/en/actions) | Automate builds, checks, and releases |

## 21. Web fundamentals and security

| Resource | Best for |
|---|---|
| [MDN Learn Web Development](https://developer.mozilla.org/en-US/docs/Learn_web_development) | HTML, CSS, JavaScript, and browser fundamentals |
| [MDN Responsive Design](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/CSS_layout/Responsive_Design) | Layouts that adapt to different screens |
| [MDN Network Requests](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Scripting/Network_requests) | Fetch and browser network requests |
| [OWASP XSS Prevention](https://cheatsheetseries.owasp.org/cheatsheets/Cross_Site_Scripting_Prevention_Cheat_Sheet.html) | Safe output handling and HTML sanitization |
| [OWASP Content Security Policy](https://cheatsheetseries.owasp.org/cheatsheets/Content_Security_Policy_Cheat_Sheet.html) | Restrict which resources and scripts the browser can load |

## Frontend launch checklist

- Make sure routes work after a refresh and test a missing route on the deployed preview.
- Add loading, empty, error, and success states to key screens. Verify form validation on both the client and server.
- Test on a narrow screen, with a keyboard, and with reduced motion enabled. Check focus order, contrast, and form labels.
- Keep private API keys out of browser bundles. Enforce permissions on the server and sanitize untrusted HTML.
- Check image sizes, layout shifts, and the loading time of the main screen. Add page titles and social previews for pages people will share.
- Run a browser test for the demo's main flow against a preview deployment. Check production error reporting if the project will stay online.
- Add offline support, translations, analytics, or complex shared state when the project needs them.

See the [API catalog](../api/README.md), [database catalog](../database/README.md), and [deployment guide](../deploy/README.md) for services that connect to the frontend.

### Project notes

- Remix v2 apps have an upgrade path into React Router Framework Mode. The current Remix project has its own TypeScript framework documentation. [Remix v2 docs](https://remix.run/docs/en/main) · [Current Remix docs](https://docs.remix.run/)
- shadcn/ui provides editable source code and supports multiple component foundations. Check which foundation a component uses before following its examples. [shadcn/ui architecture](https://ui.shadcn.com/docs)
- Headless libraries supply behavior and interaction patterns. Styled kits include visual defaults. Test keyboard navigation, focus, and contrast after customizing either.
- Core packages, premium themes, templates, and hosting can have separate terms. Check the license for the package or asset you use.

