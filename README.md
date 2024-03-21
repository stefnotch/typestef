# Typestef

Various utilities that should be in the JS standard library. Feel free to copy-paste the code instead of using this as a library.

Dual licensed under the Apache License Version 2.0 and CC0.

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
