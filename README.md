# Dumpa

> A dark-themed, 16-module CSS design system engineered with glassmorphism surfaces, responsive layout primitives, fluid typography, and hardware-accelerated micro-interactions. Zero JavaScript runtime dependencies.

![CSS3](https://img.shields.io/badge/CSS3-Vanilla-1572B6?logo=css3&logoColor=white)
![HTML5](https://img.shields.io/badge/HTML5-Semantic-E34F26?logo=html5&logoColor=white)
![Responsive](https://img.shields.io/badge/Responsive-Mobile--First-4CAF50)
![Dependencies](https://img.shields.io/badge/Dependencies-Zero-success)
![License](https://img.shields.io/badge/License-MIT-blue)

---

## Table of Contents

- [Overview](#overview)
- [Key Features](#key-features)
- [Tech Stack](#tech-stack)
- [Module Architecture](#module-architecture)
- [Module Index](#module-index)
- [Design Tokens](#design-tokens)
- [Getting Started](#getting-started)
- [Usage Examples](#usage-examples)
- [Interactive Showcase](#interactive-showcase)
- [Browser Compatibility](#browser-compatibility)
- [Performance](#performance)
- [Repository Structure](#repository-structure)
- [License](#license)

## Overview

Dumpa is a modular CSS design framework created for building modern, high-performance web dashboards and applications. Designed with an obsidian-dark aesthetic, it pairs deep background layers with translucent frosted-glass panels, vivid indigo-to-purple gradient accents, and subtle elevation glows.

The system is organized into 16 discrete stylesheets. Developers can load individual modules independently or import the unified `dumpa.css` master bundle.

## Key Features

- **Dark Glassmorphism Architecture** — Multi-layered surfaces utilizing backdrop blur and translucent borders.
- **16 Atomic Modules** — Highly decoupled stylesheets covering foundations, controls, layout, navigation, and feedback.
- **Master Bundle Included** — Load all modules in correct cascade order via `dumpa.css`.
- **Zero JavaScript Overhead** — Pure CSS components with zero build step, zero compiler, and zero runtime dependencies.
- **Responsive Layout Engine** — 12-column grid, auto-fit repeaters, and flexbox utilities that adapt to all screen sizes.
- **Interactive States** — Polished focus rings, hover lifts, glow shadows, skeleton shimmer loaders, and keyframe animations.
- **Accessible & Semantic** — Built-in focus-visible rings, screen reader utility classes, and semantic tag compatibility.
- **Single-Source Design Tokens** — Over 40 CSS custom properties for easy white-label theming and customization.

## Tech Stack

| Domain | Technology |
|---|---|
| Core Language | Vanilla CSS3 |
| Markup Standard | HTML5 Semantic |
| Design Tokens | CSS Custom Properties |
| Layout Engines | CSS Grid & Flexbox |
| Animations | Native CSS @keyframes |
| Dependencies | None |

## Module Architecture

```
dumpa.css (Master Bundle)
├── global1.css   ─── Foundations, Resets & Design Tokens
├── global2.css   ─── Typography, Scales & Text Gradients
├── global3.css   ─── Surfaces, Glassmorphism & Elevation Glows
├── global4.css   ─── Buttons, Actions & Loading Spinners
├── global5.css   ─── Form Controls, Inputs, Toggles & Selects
├── global6.css   ─── Cards, Stat Widgets & Interactive Panels
├── global7.css   ─── Sticky Top Navigation & Breadcrumbs
├── global8.css   ─── Vertical Sidebar & Responsive Navigation
├── global9.css   ─── Avatars, Status Indicators, Badges & Chips
├── global10.css  ─── Data Tables, List Groups & Feed Items
├── global11.css  ─── Modal Dialogs, Backdrops & Popups
├── global12.css  ─── Tabs, Segmented Switchers & Accordions
├── global13.css  ─── Tooltips, Dropdowns & Popovers
├── Global14.css  ─── Alerts, Banners & Floating Toast Notifications
├── global15.css  ─── 12-Column Grid, Auto-Fit & Layout Helpers
└── global16.css  ─── Animations, Skeleton Loaders & Micro-Interactions
```

## Module Index

| # | Stylesheet | Purpose & Included Classes |
|---|---|---|
| 01 | `global1.css` | Box reset, typography resets, root color variables, elevation tokens, spacing scale |
| 02 | `global2.css` | Heading scales `h1`-`h6`, `.lead`, `.text-gradient`, `.truncate`, `.line-clamp-2` |
| 03 | `global3.css` | `.glass`, `.glass-accent`, `.border-glow`, `.border-gradient`, `.shadow-glow` |
| 04 | `global4.css` | `.btn`, `.btn-primary`, `.btn-secondary`, `.btn-outline`, `.btn-loading`, `.btn-group` |
| 05 | `global5.css` | `.form-control`, `.form-select`, `.form-switch`, `.input-with-icon`, `.is-invalid` |
| 06 | `global6.css` | `.card`, `.card-interactive`, `.stat-card`, `.stat-value`, `.stat-trend` |
| 07 | `global7.css` | `.navbar`, `.navbar-brand`, `.nav-link`, `.breadcrumbs`, `.navbar-actions` |
| 08 | `global8.css` | `.sidebar`, `.sidebar-menu`, `.sidebar-link`, `.sidebar-footer`, responsive collapse |
| 09 | `global9.css` | `.avatar`, `.avatar-status`, `.avatar-group`, `.badge`, `.badge-pill`, `.chip` |
| 10 | `global10.css` | `.table`, `.table-striped`, `.table-container`, `.list-group`, `.list-group-item` |
| 11 | `global11.css` | `.modal-backdrop`, `.modal-dialog`, `.modal-header`, `.modal-close`, `.modal-body` |
| 12 | `global12.css` | `.tabs-nav`, `.tab-link`, `.segmented-control`, `.accordion`, `.accordion-summary` |
| 13 | `global13.css` | `[data-tooltip]`, `.dropdown`, `.dropdown-menu`, `.dropdown-item`, `.dropdown-divider` |
| 14 | `Global14.css` | `.alert`, `.alert-primary`, `.alert-success`, `.alert-danger`, `.toast-container` |
| 15 | `global15.css` | `.container`, `.grid-12`, `.grid-auto-fit`, `.col-6`, `.flex`, `.justify-between` |
| 16 | `global16.css` | `.animate-fade-in`, `.animate-pulse-glow`, `.skeleton`, `.hover-lift`, `.hover-glow` |

## Design Tokens

All variables are scoped under `:root` in `global1.css`:

```css
:root {
  --dumpa-bg: #090a10;
  --dumpa-surface: #11121c;
  --dumpa-surface-card: #181926;
  --dumpa-surface-elevated: #202234;
  --dumpa-surface-glass: rgba(24, 25, 38, 0.72);
  --dumpa-primary: #6366f1;
  --dumpa-secondary: #a855f7;
  --dumpa-accent: #06b6d4;
  --dumpa-gradient-brand: linear-gradient(135deg, #6366f1 0%, #a855f7 50%, #ec4899 100%);
  --dumpa-success: #10b981;
  --dumpa-warning: #f59e0b;
  --dumpa-danger: #ef4444;
  --dumpa-text: #f8fafc;
  --dumpa-text-muted: #94a3b8;
  --dumpa-border: rgba(255, 255, 255, 0.09);
  --dumpa-radius-md: 10px;
  --dumpa-radius-lg: 16px;
}
```

## Getting Started

### 1. Clone Repository

```bash
git clone https://github.com/Kumar44developer/dumpa.git
cd dumpa
```

### 2. View Live Showcase

Open `index.html` in any web browser:

```bash
start index.html
```

Or run via a local static server:

```bash
npx serve .
```

### 3. Integrate into an Existing Project

Option A: Load the all-in-one bundle:

```html
<link rel="stylesheet" href="dumpa.css" />
```

Option B: Load specific standalone modules:

```html
<link rel="stylesheet" href="global1.css" />
<link rel="stylesheet" href="global2.css" />
<link rel="stylesheet" href="global4.css" />
<link rel="stylesheet" href="global6.css" />
```

## Usage Examples

### Gradient Action Buttons

```html
<button class="btn btn-primary">Launch Project</button>
<button class="btn btn-secondary">Documentation</button>
<button class="btn btn-outline">Outline Glass</button>
<button class="btn btn-primary btn-loading">Submitting</button>
```

### Stat Metric Card

```html
<div class="stat-card hover-lift">
  <div class="stat-icon">
    <svg width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="currentColor">
      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z"/>
    </svg>
  </div>
  <div class="stat-value">99.98%</div>
  <div class="stat-label">System Uptime</div>
  <div class="stat-trend trend-up">+0.4% from last week</div>
</div>
```

### Form Input with Icon Slot

```html
<div class="form-group">
  <label class="form-label">Email Address</label>
  <div class="input-with-icon">
    <span class="input-icon">@</span>
    <input type="email" class="form-control" placeholder="developer@dumpa.dev" />
  </div>
</div>
```

### Feedback Alert Banner

```html
<div class="alert alert-success">
  <div class="alert-content">
    <div class="alert-title">Deployment Complete</div>
    <div class="alert-message">All 16 styles compiled and active on production CDN.</div>
  </div>
</div>
```

## Interactive Showcase

An interactive demo environment is bundled in `index.html`. It demonstrates:

1. Responsive dual-panel layout with collapsible sidebar
2. Sticky frosted topbar with integrated search and breadcrumb trail
3. Live stat metrics with trend badges
4. Complete button catalog across all states and sizes
5. Glassmorphic form inputs with custom toggle switches
6. Styled data table with status pill indicators
7. Toast notification banners and tag chips

## Browser Compatibility

| Browser | Supported Versions | Notes |
|---|---|---|
| Google Chrome | 88+ | Full support for backdrop-filter and CSS custom properties |
| Mozilla Firefox | 85+ | Full support |
| Apple Safari | 14+ | Full support for -webkit-backdrop-filter |
| Microsoft Edge | 88+ | Full support |
| Mobile Browsers | iOS 14+, Android 88+ | Tested on touch screens and viewport transitions |

## Performance

- **Zero JS Dependencies** — No polyfills, no runtime scripts, zero main-thread blocking.
- **Hardware-Accelerated** — Transforms and opacity transitions leverage GPU compositing.
- **Tree-Shakable by Design** — Drop in only the specific stylesheets required by your application.

## Repository Structure

```
dumpa/
├── dumpa.css
├── global1.css
├── global2.css
├── global3.css
├── global4.css
├── global5.css
├── global6.css
├── global7.css
├── global8.css
├── global9.css
├── global10.css
├── global11.css
├── global12.css
├── global13.css
├── Global14.css
├── global15.css
├── global16.css
├── globa16.css
├── index.html
├── .gitignore
└── README.md
```

## License

This project is licensed under the MIT License.
