# npm-typescript-template

A little template repository for NPM packages that use Typescript.

Use the template, make sure to fill out the `package.json` and get going!

## Scripts

- `npm run build`
- `npm run release`

## FAQ

- Typescript cannot find the library?
  That's because this uses the [`"export"` field in the `package.json`](https://www.typescriptlang.org/docs/handbook/esm-node.html#packagejson-exports-imports-and-self-referencing). Go to your `tsconfig.json`, or create one if there is none, and set
```json
{
    "compilerOptions": {
        /* This tells Typescript that we're working with the new importing mechanisms */
        "module": "nodenext", 
    }
}
```
Make sure to read [the documentation](https://www.typescriptlang.org/docs/handbook/esm-node.html) for what that means, among other things all the imports in your code might need a file extension.
