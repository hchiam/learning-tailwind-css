# Another tutorial

Slightly old YouTube crash course: <https://www.youtube.com/watch?v=8k165Y0qBN0>

Examples of deviations/updates since that video:

- I think `.bg-gray-lighter` is deprecated in favour of something like `.bg-gray-200`
- `.text-blue` has to have a number appended, like `.text-blue-500`
- Using that CDN link, `h1` tags default to inherit text size, which is a deliberate design decision to make font size a more conscious decision on your part, since different browsers may have different defaults.

```bash
node init -y
npm install --save-dev tailwindcss postcss postcss-cli cssnano @fullhuman/postcss-purgecss autoprefixer watch
npx tailwind init tailwind.js
npx tailwind build ./src/style.css -c ./tailwind.js -o ./dist/output.css
npm run build:css
```

```bash
cd another-tutorial
npm i
npm run watch # postcss will auto-run a few CSS plugins
# Get VSCode extension: Live Server
# Right-click on index.html and open it with Live Server
# Don't forget to turn off Live Server when you're done
```
