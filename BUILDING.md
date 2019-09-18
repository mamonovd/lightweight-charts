# Building Lightweight Charts

The minimal supported version of [NodeJS](https://nodejs.org/) for development is 10.12.0.

## Install Dependencies

- `npm install global npm-run-all`
- `npm i tslib ttypescript typescript ts-node ts-transformer-minify-privates rollup rollup-plugin-terser rollup-plugin-node-resolve rollup-plugin-replace dts-bundle-generator -D`

## Compiling

- `npm run tsc` - compiles the source code only (excluding tests)
- `npm run tsc-watch` - runs the TypeScript compiler in the watch mode for source code (same as `tsc`, but in the watch mode)
- `npm run tsc-all` - compiles everything (source code and tests)
- `npm run tsc-all-watch` - runs the TypeScript compiler in watch mode for source code and tests (same as `tsc-all`, but in watch mode)

## Bundling

- `npm run rollup` - runs Rollup to bundle code
- `npm run build` - compiles source code and bundles it (as one word for `npm run tsc && npm run rollup`)
- `npm run build:prod` - the same as `npm run build`, but also bundles production (minified) builds

## Testing

- `npm run lint` - runs lint for the code
- `npm run test` - runs unit-tests

## Tips

- You can use the following command to make sure that your local copy passes all (almost) available checks:

    `npm run verify`

- If you want to play with a locally built package, you can create a `debug.html` page: `cp debug.html.example debug.html`.

    This file (`debug.html`) is under gitignore, so you don't need to worry about changing it and you can modify it as you wish.
