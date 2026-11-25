# Annotate.js redesign

This is Sherman Wright's portfolio fork of [annotate.js](https://github.com/reviewjs/annotate), an open-source visual feedback layer that lets reviewers comment directly on a website. This fork presents a functional UI redesign of the original project.

## Redesign

- Compact floating toolbar with grouped shape tools and keyboard shortcuts.
- Updated comment markers, previews, and comment popovers.
- Neutral annotation styling with clearer contrast across light and dark themes.
- Interactive demo with a light/dark preview toggle.

The annotation engine and integrations are based on the upstream project. The redesign changes are by Sherman Wright; the original project and its contributors remain credited below.

## Screenshots

Product overview:

![Annotate.js on a sample review page](./og-image.png)

Redesigned toolbar, dark theme:

![Dark theme toolbar](./assets/annotate-toolbar-dark.svg)

## Run the demo

Requires Node.js 20 or later.

```bash
git clone https://github.com/shermanwright/annotate.git
cd annotate
npm ci
npm start
```

Open [http://localhost:4200](http://localhost:4200) to try the demo. To add this fork's build to another page, host `annotate.js` alongside that page and include:

```html
<script src="/annotate.js" data-project="my-site" defer></script>
```

For a script hosted directly from this public fork, use jsDelivr:

```html
<script src="https://cdn.jsdelivr.net/gh/shermanwright/annotate@main/annotate.js" data-project="my-site" defer></script>
```

## Usage

The toolbar appears at the bottom-right by default. Select a tool, then annotate the page. Open the comments panel with `A` to review, resolve, export, or import comments. The layer can also be configured from the script tag:

```html
<script
  src="/annotate.js"
  data-project="marketing-site"
  data-theme="auto"
  data-start-open="true"
  defer
></script>
```

For framework projects, install the upstream package and initialize it after mount:

```js
import Annotate from "@reviewjs/annotate";

Annotate.init({ project: "my-app", spa: true });
// Call Annotate.destroy() when the component unmounts.
```

The npm package is published by the upstream project and does not contain this fork's redesign. Use the local or jsDelivr-hosted fork build to try these changes.

## Attribution and license

Original project: [reviewjs/annotate](https://github.com/reviewjs/annotate), created by Akash Goswami and its contributors. This repository is an independent portfolio fork and is not an official upstream release. Sherman Wright's contributions here are the visual redesign, demo refinements, and related documentation and examples.

The upstream MIT license is preserved in [`LICENSE`](./LICENSE). The original copyright and license terms apply to the upstream work.
