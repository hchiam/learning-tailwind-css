# Learning [Tailwind CSS](https://tailwindcss.com/)

Just one of the things I'm learning. <https://github.com/hchiam/learning>

A CSS utility framework. Don't look like a standard Bootstrap site. Configurable with a JS config file. Extendible with custom classes.

```bash
yarn add tailwindcss # or: npm install tailwindcss
```

```css
/* inject styles into CSS: */
@tailwind base;
@tailwind components;
@tailwind utilities;
```

```bash
# create config file (optional):
npx tailwindcss init
```

## Other notes:

[![generator-hchiam-learning](https://img.shields.io/badge/built%20with-generator--hchiam--learning-brightgreen.svg)](https://github.com/hchiam/generator-hchiam-learning)

You can generate a [dependency graph](https://github.com/hchiam/learning-dependency-cruiser) with `npm run deps` (which runs `bash show_dep_graph.sh`).

You can run in-browser tests using [Cypress](https://github.com/hchiam/learning-cypress) with `npm run cypress`.

You can get a report on accessibility, best practices, etc. with `npm run lighthouse` (see [example usage notes](https://github.com/hchiam/learning-lighthouse-ci) for more info on `lighthouse`, or `@lhci/cli` for more advanced CLI stuff).

You can publish a live site to [surge](https://github.com/hchiam/learning-surge) with `bash publish_live_site.sh` (Just go into the relevant enclosing `src` or `public` folder of your site files - a CNAME file is there for convenience).

You can zip the current folder with `npm run zip`.

This file was first created using the Yeoman generator [`generator-hchiam-learning`](https://www.npmjs.com/package/generator-hchiam-learning).
