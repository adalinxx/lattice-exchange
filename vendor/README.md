`lattice-sdk.js` is `@0xLattice/lattice-sdk` (github.com/0xLattice/lattice-sdk at
512e704) bundled for the browser (ESM, its `@noble` dependencies included).
`lattice-sdk.d.ts` types the part these pages use.

```sh
# in a lattice-sdk checkout: npm ci && npm run build
printf 'export * from "<lattice-sdk>/packages/sdk/dist/index.js";\n' > entry.mjs
npx esbuild@0.24.0 entry.mjs --bundle --format=esm --platform=browser --minify --outfile=lattice-sdk.js
```
