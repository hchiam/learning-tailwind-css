# Learning [Tailwind CSS](https://tailwindcss.com/)

Just one of the things I'm learning. <https://github.com/hchiam/learning>

A CSS utility framework. Don't look like a standard Bootstrap site. Configurable with a JS config file. Extendible with custom classes. (Customizability built in, but the documentation has a lot of examples of elements with classes.)

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

## Notes:

- **Just write your styles in the HTML files:** SASS style hierarchy tends to match the markup structure anyways. Leverage the markup structure.
- Vue (and Svelte? scoped styles still make you keep adding CSS, but frameworks should let you write less CSS.
- Tailwind is a PostCSS plugin, which processes your CSS, modifies it with JavaScript, and generates the CSS. (Also need another plugin PurgeCSS to remove unused classes from the generated ones.)
- Instead of classes named by component, classes look like CSS properties. Just put them into the HTML markup.
- You can even write media queries: `w-16 md:w-32 lg:w-48`
- Also `yarn add postcss-cli autoprefixer`
- But if a customer changes their mind about a style, how do you update styles on all elements? Update each element in HTML? No! **Set custom (re)-definitions/extensions of existing class names in your JavaScript config file!**
- It seems like a lot of classes on the markup, but the alternative has more friction: you have to go to a separate file, and actually read more code, and you don't have to figure out which styles apply to which components.
- To scale, how do you group together classes? **Config!**
- How do you integrate with frameworks like Vue? **Config!** You can write JS code in the config to return a different style: `computed: { canSubmit() { return this.name && this.password; } }`
- Can you get just what you need from Tailwind (avoid bloat)? Yes! **Config!** Example: <https://tailwindcss.com/docs/font-weight/#disabling>

## research later:

purgecss

`<style scoped></style>`

```css
/* how does @apply work? */
.some-grouping-class {
  @apply bg-yellow-400 flex items-center p-20;
}
```

<https://www.meetup.com/KWJavaScript/events/268537370>

## Other notes:

[![generator-hchiam-learning](https://img.shields.io/badge/built%20with-generator--hchiam--learning-brightgreen.svg)](https://github.com/hchiam/generator-hchiam-learning)

You can generate a [dependency graph](https://github.com/hchiam/learning-dependency-cruiser) with `npm run deps` (which runs `bash show_dep_graph.sh`).

You can run in-browser tests using [Cypress](https://github.com/hchiam/learning-cypress) with `npm run cypress`.

You can get a report on accessibility, best practices, etc. with `npm run lighthouse` (see [example usage notes](https://github.com/hchiam/learning-lighthouse-ci) for more info on `lighthouse`, or `@lhci/cli` for more advanced CLI stuff).

You can publish a live site to [surge](https://github.com/hchiam/learning-surge) with `bash publish_live_site.sh` (Just go into the relevant enclosing `src` or `public` folder of your site files - a CNAME file is there for convenience).

You can zip the current folder with `npm run zip`.

This file was first created using the Yeoman generator [`generator-hchiam-learning`](https://www.npmjs.com/package/generator-hchiam-learning).
