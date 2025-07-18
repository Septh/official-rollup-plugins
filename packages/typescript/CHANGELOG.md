# @rollup/plugin-typescript ChangeLog

## v12.1.4

_2025-06-28_

### Bugfixes

- fix: revert #1653 (#1880)

## v12.1.3

_2025-06-17_

### Bugfixes

- fix: fixes #1652 compile when source exists anywhere in the working directory (#1653)

## v12.1.2

_2024-12-15_

### Bugfixes

- fix: path validation issue in validatePaths function (#1800)

## v12.1.1

_2024-10-16_

### Bugfixes

- fix: allow for files to be nested in folders within outDir (#1783)

## v12.1.0

_2024-09-22_

### Features

- feat: add transformers factory. (#1668)

## v12.0.0

_2024-09-22_

### Breaking Changes

- fix!: correctly resolve filenames of declaration files for `output.file` (#1728)

## v11.1.6

_2024-01-09_

### Bugfixes

- fix: Ensure rollup 4 compatibility (#1658)

## v11.1.5

_2023-10-05_

### Bugfixes

- fix: ensure rollup 4 compatibility [#1595](https://github.com/rollup/plugins/pull/1595)

## v11.1.4

_2023-09-25_

### Bugfixes

- fix: fix sourcemap sourcecontent referencing non-existent files [#1571](https://github.com/rollup/plugins/pull/1571)

## v11.1.3

_2023-08-26_

### Bugfixes

- fix: emit declaration files for type-only source files that are not explicitly included [#1555](https://github.com/rollup/plugins/pull/1555)

## v11.1.2

_2023-06-28_

### Bugfixes

- fix: change the value of isExternalLibraryImport to false if the resolvedModule should be compiled [#1521](https://github.com/rollup/plugins/pull/1521)

## v11.1.1

_2023-05-12_

### Bugfixes

- fix: Allow for using `compilerOptions.moduleResolution` [#1453](https://github.com/rollup/plugins/pull/1453)

## v11.1.0

_2023-04-04_

### Features

- feat: write declaration files in configured directory for `output.file` [#1378](https://github.com/rollup/plugins/pull/1378)

## v11.0.0

_2023-01-06_

### Breaking Changes

- fix: don't resolve filtered files [#1267](https://github.com/rollup/plugins/pull/1267) (#1310)

## v10.0.1

_2022-11-28_

### Bugfixes

- fix: emit assets when watchMode is false. fixes #1354 ([5c88274](https://github.com/rollup/plugins/commit/5c882743475a4480cb82e42253de9290b7329511))

## v10.0.0

_2022-11-27_

### Breaking Changes

- fix: incorrect declarations directory ([a5c90d1](https://github.com/rollup/plugins/commit/a5c90d1032390f9f6160d95c42171aa3014b3d6b))

## v9.0.2

_2022-10-21_

### Updates

- chore: update rollup dependencies ([3038271](https://github.com/rollup/plugins/commit/303827191ede6b2e4eade96c6968ed16a587683f))

## v9.0.1

_2022-10-11_

### Bugfixes

- fix: fix ESM build [#1311](https://github.com/rollup/plugins/pull/1311)

## v9.0.0

_2022-10-10_

### Breaking Changes

- fix: prepare for Rollup 3 [#1282](https://github.com/rollup/plugins/pull/1282)

## v8.5.0

_2022-09-06_

### Features

- feat: support 4.7 nodenext (#1194)

## v8.4.0

_2022-08-23_

### Features

- feat: allow override of forced `noEmit` and `emitDeclarationOnly` compiler options (#1242)

## v8.3.4

_2022-07-28_

### Bugfixes

- fix: fix declaration file generation for single file outputs (#1201)

## v8.3.3

_2022-06-10_

### Bugfixes

- fix: allow tslib peerDependency to be optional for npm and pnpm (#1191)

## v8.3.2

_2022-04-13_

### Bugfixes

- fix: Drive letter casing on win32 platforms. fixes #1133 (#1134)

## v8.3.1

_2022-02-23_

### Bugfixes

- fix: allow explicity compilerOptions (#1045)

### Updates

- docs: readme copy/paste mistake (#1086)

## v8.3.0

_2021-10-15_

### Features

- feat: add resolve options (#1015)

## v8.2.5

_2021-07-30_

### Bugfixes

- fix: incremental typescript cache (#963)

## v8.2.4

_2021-07-29_

### Updates

- docs: declaration file output to same directory. fixes #934 (702c855)

## v8.2.3

_2021-07-15_

### Bugfixes

- fix: restart watch program on each build (#861)

### Updates

- docs: add link for @rollup/plugin-commonjs (#889)

## v8.2.2

_2021-07-15_

### Bugfixes

- fix: restart watch program on each build (#861)

### Updates

- docs: add link for @rollup/plugin-commonjs (#889)

## v8.2.1

_2021-03-26_

### Bugfixes

- fix: bump TypeScript version (#818)
- fix: update readme and peerDeps version (#830)

## v8.2.0

_2021-02-14_

### Features

- feat: error when no tsconfig and no rootDir (#794)
- feat: better error when tslib is not installed (#793)
- feat: warn when compilerOptions.module is not esnext (#788)

### Updates

- test: move declaration tests, use typescript (#791)
- test: fix TypeScript src-dir test (#789)

## v8.1.1

_2021-01-29_

### Bugfixes

- fix: fix plugin type declarations (#647)
- fix: only emit tsbuildinfo file when there is something to emit (#771)

## v8.1.0

_2020-12-14_

### Features

- feat: support multiple output targets with declarations (#687)

### Updates

- chore: fix TypeScript warnings (#673)
- test: code in src sub-directory (#682)
- chore: use TypeScript 4 (#674)

## v8.0.0

_2020-11-30_

### Breaking Changes

- fix: pick up new files in watch mode (#657)

### Bugfixes

- fix: add missing imports (#633)
- fix: normalize returned module ids (#653)

### Features

- feat: Implement cached incremental code (#535)

### Updates

- docs: fix minor markdown syntax in transformers-section (#624)

## v7.0.0

_2020-11-30_

### Breaking Changes

- fix: pick up new files in watch mode (#657)

### Bugfixes

- fix: add missing imports (#633)
- fix: normalize returned module ids (#653)

### Features

- feat: Implement cached incremental code (#535)

### Updates

- docs: fix minor markdown syntax in transformers-section (#624)

## v6.1.0

_2020-10-27_

### Bugfixes

- fix: add composite to validation checks (#618)

### Features

- feat: Add CustomTransformers support (#280)

### Updates

- docs: More informative error messages (#619)

## v6.0.0

_2020-09-09_

### Breaking Changes

- fix!: Change `noEmitOnError` default to false (#544)

### Updates

- test: add generating declarations with non-default rootDir (#553)
- chore: update dependencies (9e52818)

## v5.0.2

_2020-07-12_

### Bugfixes

- fix: utilize 'this.meta.watchMode' (#449)

### Updates

- chore: linting update (410ceb8)

## v5.0.1

_2020-06-28_

### Bugfixes

- fix: load empty emitted files (#476)

## v5.0.0

_2020-06-22_

### Breaking Changes

- fix!: sync rollup and typescript file watch (#425)

### Bugfixes

- fix: Fix peer dep version (#461)

## v4.1.2

_2020-05-20_

### Bugfixes

- fix: memory leak. fixes #322 (#352)

### Updates

- docs: update readme examples (#391)
- docs: update link to @rollup/plugin-babel in README.md (#372)

## v4.1.1

_2020-04-12_

### Bugfixes

- fix: sourcemap generated as null (#276)
- fix: use parsedOptions.fileNames for emit declaration files (#270) (#271)

## v4.1.0

_2020-04-12_

### Features

- feat: Refine options interface (#284)

## v4.0.0

### Bugfixes

- fix: Use builtin extends resolution (#199)

### Features

- feat: Move to BuilderProgram API (#217)

### Breaking Changes

Please see https://github.com/rollup/plugins/pull/217 for more information.

## v3.1.0

_2020-03-05_

_Note: This was a bad release due to breaking changes. v3.1.1 has been published to revert the latest 3.x.x version to a non-breaking state. For the changes in this erroneous version, please use v4.0.0._

### Updates

- test: Add preserveModules test (#234)
- chore: refactor compiler host (#214)
- test: Add test for optional chaining (#207)
- chore: Use typechecking (4bb8753)

## v3.0.0

_2020-01-27_

### Breaking Changes

- feat: Add typechecking! (#177)

### Bugfixes

- fix: extended config file path (#157)

### Updates

- core: Add note about old behaviour (#181)
- chore: Always use ParsedCommandLine (#162)
- chore: update devDeps (96c45ff)
- chore: Remove resolveHost (#148)

## v2.1.0

_2020-01-07_

### Features

- feat: Warning objects for type errors (#144)
- feat: Find tslib asynchronously (#131)

### Updates

- chore: Use ts.findConfigFile helper (#145)

## v2.0.2

_2020-01-04_

### Bugfixes

- fix: Use this.warn for ts errors (#129)

### Updates

- refactor: use typescript in typescript plugin (#122)
- chore: update changelog (b723f92)
- chore: misc linting updates (4de10f0)

## 2.0.1

_2019-12-04_

- fix(typescript): import from scoped utils (#78)

## 2.0.0

_2019-11-25_

- **Breaking:** Minimum compatible Rollup version is 1.20.0
- **Breaking:** Minimum supported Node version is 8.0.0
- Published as @rollup/plugin-typescript

## 1.0.1

_2019-03-24_

- Update dependencies ([#136](https://github.com/rollup/rollup-plugin-typescript/issues/136))

## 1.0.0

_2018-09-16_

- Major update for TypeScript 2/3, Rollup 1 compatibility, lots of fixes ([#124](https://github.com/rollup/rollup-plugin-typescript/issues/124))
- Require TypeScript as peer dependency ([#121](https://github.com/rollup/rollup-plugin-typescript/issues/121))
- Also test on Node 10 ([#119](https://github.com/rollup/rollup-plugin-typescript/issues/119))
- Fix example in readme ([#98](https://github.com/rollup/rollup-plugin-typescript/issues/98))

## 0.8.1

- Ignore typescript-helpers in source maps ([#61](https://github.com/rollup/rollup-plugin-typescript/issues/61))

## 0.8.0

- Fix the rollup breaking change with paths ([#52](https://github.com/rollup/rollup-plugin-typescript/issues/52))
- Don't fail without source maps ([#57](https://github.com/rollup/rollup-plugin-typescript/pull/57))

## 0.7.7

- Add missing `__assign` helper ([#49](https://github.com/rollup/rollup-plugin-typescript/issues/49))

## 0.7.6

- Ignore the `declaration` option ([#45](https://github.com/rollup/rollup-plugin-typescript/issues/45))
- Disable `strictNullChecks` with a warning for TypeScript versions that don't support it ([#46](https://github.com/rollup/rollup-plugin-typescript/issues/46))

## 0.7.5

- Ensure NPM doesn't ignore typescript-helpers

## 0.7.4

- Resolve typescript-helpers to a file in the filesystem.

## 0.7.3

- Update Tippex to ^2.1.1

## 0.7.2

- Don't error if both `sourceMap` and `inlineSourceMap` are specified

## 0.7.1

- No plugin specific options should be forwarded to TypeScript

## 0.7.0

- Use `compilerOptions` from `tsconfig.json` if found ([#39](https://github.com/rollup/rollup-plugin-typescript/pull/32))

## 0.6.1

- Upgrade Tippex to ^2.1.0
- Upgrade TypeScript to ^1.8.9

## 0.6.0

- Upgrade to TypeScript ^1.8.7
- Update `__awaiter` helper to support TypeScript 1.8.x ([#32](https://github.com/rollup/rollup-plugin-typescript/pull/32))
- Update `ts.nodeModuleNameResolver` to support both 1.7.x and 1.8.x ([#31](https://github.com/rollup/rollup-plugin-typescript/issues/31))

## 0.5.0

- Do not duplicate TypeScript's helpers ([#24](https://github.com/rollup/rollup-plugin-typescript/issues/24))
- Handle `export abstract class` ([#23](https://github.com/rollup/rollup-plugin-typescript/issues/23))

## 0.4.1

- Does not attempt resolve or transform `.d.ts` files ([#22](https://github.com/rollup/rollup-plugin-typescript/pull/22))

## 0.4.0

- Work around TypeScript 1.7.5's transpilation issues ([#9](https://github.com/rollup/rollup-plugin-typescript/issues/9))
- Overridable TypeScript version when transpiling ([#4](https://github.com/rollup/rollup-plugin-typescript/issues/4))
- Add `jsx` support ([#11](https://github.com/rollup/rollup-plugin-typescript/issues/11))

## 0.3.0

- Author plugin in TypeScript
- Report diagnostics
- Resolve identifiers using `ts.nodeModuleNameResolver`

## 0.2.1

- Upgrade to TypeScript ^1.7.5
- Enable source maps per default

## 0.2.0

- Use (_prerelease version of_) TypeScript 1.7.0 to generate ES5 while preserving ES2015 imports for efficient bundling.

## 0.1.0

- Initial release
