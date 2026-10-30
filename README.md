# Next.js + WordPress (Headless)

A headless WordPress site rendered with Next.js. The homepage content is queried from WordPress through WPGraphQL with Apollo Client at build time (`getStaticProps`), and Gutenberg blocks are rendered as React components. Built while following the Udemy course "Next JS & WordPress".

## Features

- Fetches the WordPress page at `/` and its Gutenberg blocks via GraphQL
- Block cleanup/transform utility (`utils/cleanAndTransformBlocks.js`)
- `BlockRenderer` that maps blocks to React components (currently `core/cover` → `Cover`)
- Static generation with `getStaticProps`
- Tailwind CSS styling

## Tech stack

Next.js (Pages Router) · React · Apollo Client · GraphQL · WordPress + WPGraphQL · Tailwind CSS

## Project structure

```
client.js                     # Apollo Client (WP_GRAPHQL_URL)
pages/index.js                # homepage query + render
components/BlockRenderer/     # block → component mapping
components/Cover/             # cover block component
utils/cleanAndTransformBlocks.js
next.config.js                # allowed image domain (WP_IMAGES_URL)
```

## Getting started

Requires a WordPress site with WPGraphQL (and a plugin exposing `blocks` on pages).

```bash
npm install
# create .env.local with the variables below
npm run dev        # http://localhost:3000
npm run build && npm start
```

## Environment variables

`WP_GRAPHQL_URL`, `WP_IMAGES_URL`

## Credits

Based on the starter from the Udemy course "Next JS & WordPress: Build rapid NextJS sites with Next & WP".
## Screenshots

_Screenshots coming soon._

## License

No license file has been added to this repository yet.
