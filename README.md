# Recipe Assistant test site

A small static site, published with GitHub Pages, for end-to-end testing of the Recipe Assistant widget. It isn't a real food blog; the recipes are original sample content, and every page is marked `noindex`.

| Page | Purpose | Expected |
|---|---|---|
| `index.html`, `about.html` | Non-recipe pages | No widget, zero network requests to the API |
| `recipes/lemon-coconut-slice/` | Recipe with JSON-LD and a Notes section | Widget appears once the site is active; author notes are used |
| `recipes/brown-butter-oat-biscuits/` | Recipe without JSON-LD | Widget appears via the HTML fallback |
| `sponsored/honey-yoghurt-loaf/` | Recipe for testing exclusions | Hidden once `/recipe-test-site/sponsored/*` is excluded in the dashboard |

Every page loads the widget from `https://whisk-and-wordsmith.lovable.app/widget/v1/recipe-assistant.js` using the site's public ID.
