# Barebone Tailwind Setup

This is just a bare minimum [tailwindcss](https://tailwindcss.com/) configuration as a small demonstration for compiling tailwind without any heavy framework or webpack integration / setup. Primarily threw this together to mess around and experiment with [tailwind customisation](https://tailwindcss.com/docs/configuration) (themes, variants, plugins, etc).

It follows the [standard installation guide](https://tailwindcss.com/docs/installation) with some basic configuration tweaks:

  - [Dark mode](https://tailwindcss.com/docs/dark-mode#basic-usage) is set to `class`
  - [Purge](https://tailwindcss.com/docs/optimizing-for-production#enabling-manually) is enabled by default based on `./public/**/*.html`

Read the linked documentation to understand what these configuration properties mean.

The included html is based on [tailwindtoolbox/Profile-Card](https://github.com/tailwindtoolbox/Profile-Card), but I have updated it to use tailwinds built in dark variant classes instead. I also updated it to use the latest popper and tippy scripts at the time (6 and 2 respectively).

## Usage

After running `npm install`

```
npm run build
```
This will compile the `src/css/precompiled.css` into `public/css/compiled.css`

Only the classes that are used in html files under the public directory will be included in the compiled tailwind output as per the purge configuration mentioned above.

```
npm run watch
```
Same as build but will watch the precompiled css and tailwind configuration files for saved changes and automatically recompile.

Inspect the output css or edit and view `public/index.html` as you see fit.