# ts init

Minimalist TypeScript packages initializer - like `npm init`, but for TS.

Install globally:
```sh
npm i -g ts-init
```

From now, whenever you want to create a new TypeScript project, just run:
```sh
npm init
ts-init
```

**What does it actually do?** Well, not a lot! It will:

1. Install dev dependencies: [typescript](https://github.com/Microsoft/TypeScript), [ts-node](https://www.npmjs.com/package/ts-node) and [rimraf](https://github.com/isaacs/rimraf) (for cross-platform `rm -rf`).
2. Create scripts to generate `es` (ES6) and `lib` (CommonJS ES5 + `*.d.ts` declaration files) builds and a script to run your project with `ts-node`. Those build files will be also properly declared in your `package.json` and added to `.gitignore`.
3. Create a minimalist `tsconfig.json` file with sane defaults: ES6 with the following flags set to true: `alwaysStrict`, `strictNullChecks`, `noImplicitAny`.

## Motivation

> Almost every JavaScript library should be written in TypeScript.

This project is meant to provide everything you need in order to create an npm library (and potentially any other JS project) with modern TypeScript compiler. This way you can use modern ES6 features and static types without any cost.

In the same time, it tries not to force you to use something which is just an opinionated tool. **It doesn't include** a linter, testing library like Jest or some heavy TS configuration. Everything is kept as minimal as it's possible.

## License

MIT
