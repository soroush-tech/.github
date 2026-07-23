<div align="center">

[![Typing SVG](https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=700&size=28&duration=2600&pause=900&color=00FC40&center=true&vCenter=true&width=900&lines=soroush.tech;Design+systems%2C+tooling+%26+the+web;Built+in+the+open)](https://soroush.tech)

**Open-source building blocks for the modern web.**

Small, focused, fully-typed TypeScript packages — each one ships its own types, a license, and 100% test coverage.

<a href="https://www.npmjs.com/org/soroush.tech"><img alt="npm org" src="https://img.shields.io/badge/npm-@soroush.tech-CB3837?style=for-the-badge&logo=npm&logoColor=white"></a>
<a href="https://soroush.tech"><img alt="Website" src="https://img.shields.io/badge/soroush.tech-00FC40?style=for-the-badge&logo=googlechrome&logoColor=black"></a>

</div>

---

## 📦 Packages

Reusable pieces published to npm under the [`@soroush.tech`](https://www.npmjs.com/org/soroush.tech) scope.

### [`@soroush.tech/styled-system`](https://www.npmjs.com/package/@soroush.tech/styled-system)

[![npm](https://img.shields.io/npm/v/%40soroush.tech%2Fstyled-system?color=00FC40&label=npm)](https://www.npmjs.com/package/@soroush.tech/styled-system)
[![downloads](https://img.shields.io/npm/dm/%40soroush.tech%2Fstyled-system?color=181717&label=downloads)](https://www.npmjs.com/package/@soroush.tech/styled-system)

A type-safe styled-props design system. Build components from theme tokens with `system()` — spacing,
color, typography, and variants, all inferred from your theme with zero manual union types.

### [`@soroush.tech/design-system`](https://www.npmjs.com/package/@soroush.tech/design-system)

[![npm](https://img.shields.io/npm/v/%40soroush.tech%2Fdesign-system?color=00FC40&label=npm)](https://www.npmjs.com/package/@soroush.tech/design-system)
[![downloads](https://img.shields.io/npm/dm/%40soroush.tech%2Fdesign-system?color=181717&label=downloads)](https://www.npmjs.com/package/@soroush.tech/design-system)

A themeable React component library powered by `@soroush.tech/styled-system` and its own styling
engine — token-driven light/dark theming, `createTheme` with per-component defaults and style
overrides, and accessible primitives from `Button` to `Modal`.

### [`@soroush.tech/markdown`](https://www.npmjs.com/package/@soroush.tech/markdown)

[![npm](https://img.shields.io/npm/v/%40soroush.tech%2Fmarkdown?color=00FC40&label=npm)](https://www.npmjs.com/package/@soroush.tech/markdown)
[![downloads](https://img.shields.io/npm/dm/%40soroush.tech%2Fmarkdown?color=181717&label=downloads)](https://www.npmjs.com/package/@soroush.tech/markdown)

Headless, composable markdown editing and rendering for the design system — a controlled editor,
a themed preview renderer, and lazy-loaded mermaid diagrams.

### [`@soroush.tech/vite-plugin-msw-server`](https://www.npmjs.com/package/@soroush.tech/vite-plugin-msw-server)

[![npm](https://img.shields.io/npm/v/%40soroush.tech%2Fvite-plugin-msw-server?color=00FC40&label=npm)](https://www.npmjs.com/package/@soroush.tech/vite-plugin-msw-server)
[![downloads](https://img.shields.io/npm/dm/%40soroush.tech%2Fvite-plugin-msw-server?color=181717&label=downloads)](https://www.npmjs.com/package/@soroush.tech/vite-plugin-msw-server)

🎭 **Made for end-to-end tests.** Mock the *server side* of your app — runs an `msw/node` server inside
Vite so SSR data loaders and SSG prerendering resolve against your mocks. No network flake, no seeded backend.

### [`@soroush.tech/playwright-coverage`](https://www.npmjs.com/package/@soroush.tech/playwright-coverage)

[![npm](https://img.shields.io/npm/v/%40soroush.tech%2Fplaywright-coverage?color=00FC40&label=npm)](https://www.npmjs.com/package/@soroush.tech/playwright-coverage)
[![downloads](https://img.shields.io/npm/dm/%40soroush.tech%2Fplaywright-coverage?color=181717&label=downloads)](https://www.npmjs.com/package/@soroush.tech/playwright-coverage)

Collect V8 coverage from your Playwright runs and fold it into your coverage report — so e2e counts
toward the same 100% bar as unit and component tests.

### [`@soroush.tech/bench`](https://www.npmjs.com/package/@soroush.tech/bench)

[![npm](https://img.shields.io/npm/v/%40soroush.tech%2Fbench?color=00FC40&label=npm)](https://www.npmjs.com/package/@soroush.tech/bench)
[![downloads](https://img.shields.io/npm/dm/%40soroush.tech%2Fbench?color=181717&label=downloads)](https://www.npmjs.com/package/@soroush.tech/bench)

Run A/B function and package-version benchmarks inside a CPU/RAM-pinned Docker sandbox —
stable numbers on noisy machines, results as markdown tables.

---

## ⚙️ Actions

### [`soroush-tech/bench-action`](https://github.com/soroush-tech/bench-action)

A benchmark gate for CI: discovers your `*.bench.ts` files, runs them with `@soroush.tech/bench`
in a pinned-CPU sandbox, fails the job when a case drops below your minimum speed ratio, and
keeps one sticky PR comment with the results — posted as the bench bot via an OIDC-verified
relay, zero token setup.

```yaml
- uses: soroush-tech/bench-action@v1
  with:
    bench-dir: bench
    baseline-case: previous
    min-ratio: '80'
```

---

## 🎯 How we build

- **Fully typed** — strict TypeScript, no `any`, types inferred not hand-written.
- **100% coverage** — every published package, enforced. No ignore pragmas.
- **Zero-bloat deps** — packages stay decoupled; you own your framework and versions.
- **Open by default** — MIT-licensed, developed in the open.

## 🧰 Built with

<p>
<img alt="TypeScript" src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white">
<img alt="React" src="https://img.shields.io/badge/React-149ECA?style=flat-square&logo=react&logoColor=white">
<img alt="Vite" src="https://img.shields.io/badge/Vite-646CFF?style=flat-square&logo=vite&logoColor=white">
<img alt="Vitest" src="https://img.shields.io/badge/Vitest-6E9F18?style=flat-square&logo=vitest&logoColor=white">
<img alt="Playwright" src="https://img.shields.io/badge/Playwright-2EAD33?style=flat-square&logo=playwright&logoColor=white">
<img alt="MSW" src="https://img.shields.io/badge/MSW-FF6A33?style=flat-square&logo=mockserviceworker&logoColor=white">
<img alt="pnpm" src="https://img.shields.io/badge/pnpm-F69220?style=flat-square&logo=pnpm&logoColor=white">
</p>

<div align="center">

**[🌐 soroush.tech](https://soroush.tech)** · **[📦 npm](https://www.npmjs.com/org/soroush.tech)**

</div>
