# @rollup/plugin-commonjs ChangeLog

## v28.0.6

_2025-06-17_

### Bugfixes

- fix: fix crash with invalidated proxy modules (#1876)

## v28.0.5

_2025-06-14_

### Bugfixes

- fix: crawl dynamicRequireRoot outside cwd (#1859)

## v28.0.4

_2025-06-14_

### Bugfixes

- fix: try/catch instanceof in getAugmentedNamespace (#1868)

## v28.0.3

_2025-03-06_

### Bugfixes

- fix: fix error when bundle contains require() of module with falsy `__esModule` export (#1850)

## v28.0.2

_2024-12-15_

### Updates

- docs: `output.exports` recommendation also applies to IIFE (#1810)

## v28.0.1

_2024-10-16_

### Updates

- chore: upgrade picomatch (#1775)

## v28.0.0

_2024-09-23_

### Breaking Changes

- chore: switch to fdir for fewer dependencies (#1741)

## v27.0.0

_2024-09-23_

### Breaking Changes

- feat!: default strictRequires to true (#1639)
- fix!: replace top-level this with exports name (#1618)

## v26.0.3

_2024-09-23_

### Updates

- chore: revert #1618 (e98927b)

## v26.0.1

_2024-06-05_

### Bugfixes

- fix: correct import of glob (04a15b5)

## v26.0.0

_2024-06-05_

### Breaking Changes

- chore!: bump glob's version (#1695)

## v25.0.8

_2024-05-22_

### Bugfixes

- fix: preserve the class body property keys even if they are special keywords (#1688)

## v25.0.7

_2023-10-15_

### Bugfixes

- fix: bump magic-string version [#1596](https://github.com/rollup/plugins/pull/1596)

## v25.0.6

_2023-10-15_

### Bugfixes

- fix: Keep the shebang at the top of the file content [#1610](https://github.com/rollup/plugins/pull/1610)

## v25.0.5

_2023-10-05_

### Bugfixes

- fix: ensure rollup 4 compatibility [#1595](https://github.com/rollup/plugins/pull/1595)

## v25.0.4

_2023-08-11_

### Updates

- docs: update docs [#1545](https://github.com/rollup/plugins/pull/1545)

## v25.0.3

_2023-07-15_

### Bugfixes

- fix: preserve `this` reference in the child class [#1537](https://github.com/rollup/plugins/pull/1537)

## v25.0.2

_2023-06-19_

### Bugfixes

- fix: add classBodyDepth flag [#1507](https://github.com/rollup/plugins/pull/1507)

## v25.0.1

_2023-06-10_

### Bugfixes

- fix: change dynamicRequireRoot to normalizedDynamicRequireRoot && tweak related tests [#1508](https://github.com/rollup/plugins/pull/1508)

## v25.0.0

_2023-05-12_

### Breaking Changes

- fix: dynamic require root check was broken in some cases [#1461](https://github.com/rollup/plugins/pull/1461)

## v24.1.0

_2023-04-11_

### Features

- feat: Do not use getters for module.exports [#1455](https://github.com/rollup/plugins/pull/1455)

## v24.0.1

_2023-01-20_

### Bugfixes

- fix: types should come first in exports [#1403](https://github.com/rollup/plugins/pull/1403)

## v24.0.0

_2022-12-18_

### Breaking Changes

- fix: check if defaultIsModuleExports is auto for getDefaultExportFromCjs [#1358](https://github.com/rollup/plugins/pull/1358)

## v23.0.7

_2022-12-17_

### Bugfixes

- fix: produce code which works when \_\_esModule is already defined [#1379](https://github.com/rollup/plugins/pull/1379)

## v23.0.6

_2022-12-17_

### Bugfixes

- fix: update magic-string [#1373](https://github.com/rollup/plugins/pull/1373)

## v23.0.5

_2022-12-15_

### Bugfixes

- fix: resolve export exports not found [#1363](https://github.com/rollup/plugins/pull/1363)

## v23.0.4

_2022-12-07_

### Bugfixes

- fix: declaration tag @default for ignoreTryCatch + fix some typos [#1370](https://github.com/rollup/plugins/pull/1370)

## v23.0.3

_2022-11-27_

### Bugfixes

- fix: correctly wrap a default class export from cjs module [#1350](https://github.com/rollup/plugins/pull/1350)

## v23.0.2

_2022-10-21_

### Updates

- chore: update rollup dependencies ([3038271](https://github.com/rollup/plugins/commit/303827191ede6b2e4eade96c6968ed16a587683f))

## v23.0.1

_Skipped for repo rebase_

## v23.0.0

_2022-10-09_

### Breaking Changes

- fix: prepare for Rollup 3 [#1300](https://github.com/rollup/plugins/pull/1300)

## v22.0.2

_2022-08-05_

### Bugfixes

- fix: Exclude multi-line template strings from indent (#1229)

## v22.0.1

_2022-06-24_

### Bugfixes

- fix: Only proxy detected commonjs entry points (#1180)

## v22.0.0

_2022-04-24_

### Breaking Changes

- fix: add heuristic to deoptimize requires after calling imported function (requires rollup@2.68.0) (#1038)
- feat: reimplement dynamic import handling (requires Node 12, no longer supports require.cache) (#1038)

### Bugfixes

- fix: support CJS modules re-exporting transpiled ESM modules (#1165)
- fix: Warn when plugins do not pass options to resolveId (#1038)
- fix: Do not change semantics when removing requires in if statements (#1038)
- fix: handle external dependencies when using the cache (#1038)
- fix: proxy all entries to not break legacy polyfill plugins (#1038)
- fix: use correct version and add package exports (#1038)
- fix: validate node-resolve peer version (#1038)
- fix: inject module name into dynamic require function (#1038)
- fix: do not transform "typeof exports" for mixed modules (#1038)
- fix: attach correct plugin meta-data to commonjs modules (#1038)

### Features

- feat: expose plugin version (#1038)
- feat: throw for dynamic requires from outside the configured root (#1038)
- feat: add dynamicRequireRoot option (#1038)
- feat: auto-detect conditional requires (#1038)
- feat: limit ignoreTryCatch to external requires (#1038)
- feat: make namespace callable when requiring ESM with function default (#1038)
- feat: Infer type for unidentified modules (#1038)
- feat: automatically wrap cyclic modules (#1038)
- feat: add strictRequires option to wrap modules (#1038)

### Updates

- refactor: deconflict helpers only once globals are known (#1038)

## v21.1.0

_2022-04-15_

### Features

- feat: make defaultIsModuleExports as funtion to config defaultIsModuleExports for each source (#1052)

## v21.0.3

_2022-03-27_

### Updates

- docs: sync required rollup version (#1118)

## v21.0.2

_2022-02-23_

### Updates

- chore: transpile dynamic helper to ES5 (#1082)

## v21.0.1

_2021-10-19_

### Bugfixes

- fix: pass on isEntry and custom resolve options (#1018)

## v21.0.0

_2021-10-01_

### Breaking Changes

- fix: use safe default value for ignoreTryCatch (#1005)

## v20.0.0

_2021-07-30_

### Breaking Changes

- fix: Correctly infer module name for any separator (#924)

## v19.0.2

_2021-07-26_

### Bugfixes

- fix convert module.exports with `__esModule` property(#939) (#942)

## v19.0.1

_2021-07-15_

### Bugfixes

- fix: short-circuit to actual module entry point when using circular ref through a different entry (#888)

## v19.0.0

_2021-05-07_

### Breaking Changes

- feat!: Add support for circular dependencies (#658)

## v18.1.0

_2021-05-04_

### Bugfixes

- fix: idempotence issue (#871)

### Features

- feat: Add `defaultIsModuleExports` option to match Node.js behavior (#838)

## v18.0.0

_2021-03-26_

### Breaking Changes

- feat!: Add ignore-dynamic-requires option (#819)

### Bugfixes

- fix: `isRestorableCompiledEsm` should also trigger code transform (#816)

## v17.1.0

_2021-01-29_

### Bugfixes

- fix: correctly replace shorthand `require` (#764)

### Features

- feature: load dynamic commonjs modules from es `import` (#766)
- feature: support cache/resolve access inside dynamic modules (#728)
- feature: allow keeping `require` calls inside try-catch (#729)

### Updates

- chore: fix lint error (#719)

## v17.0.0

_2020-11-30_

### Breaking Changes

- feat!: reconstruct real es module from \_\_esModule marker (#537)

## v16.0.0

_2020-10-27_

### Breaking Changes

- feat!: Expose cjs detection and support offline caching (#604)

### Bugfixes

- fix: avoid wrapping `commonjsRegister` call in `createCommonjsModule(...)` (#602)
- fix: register dynamic modules when a different loader (i.e typescript) loads the entry file (#599)
- fix: fixed access to node_modules dynamic module with subfolder (i.e 'logform/json') (#601)

### Features

- feat: pass type of import to node-resolve (#611)

## v15.1.0

_2020-09-21_

### Features

- feat: inject \_\_esModule marker into ES namespaces and add Object prototype (#552)
- feat: add requireReturnsDefault to types (#579)

## v15.0.0

_2020-08-13_

### Breaking Changes

- feat!: return the namespace by default when requiring ESM (#507)
- fix!: fix interop when importing CJS that is transpiled ESM from an actual ESM (#501)

### Bugfixes

- fix: add .cjs to default file extensions. (#524)

### Updates

- chore: update dependencies (fe399e2)

## v14.0.0

_2020-07-13_

### Release Notes

This restores the fixes from v13.0.1, but as a semver compliant major version.

## v13.0.2

_2020-07-13_

### Rollback

Rolls back breaking change in v13.0.1 whereby the exported `unwrapExports` method was removed.

## v13.0.1

_2020-07-12_

### Bugfixes

- fix: prevent rewrite require.resolve (#446)
- fix: Support \_\_esModule packages with a default export (#465)

## v13.0.0

_2020-06-05_

### Breaking Changes

- fix!: remove namedExports from types (#410)
- fix!: do not create fake named exports (#427)

### Bugfixes

- fix: \_\_moduleExports in multi entry + inter dependencies (#415)

## v12.0.0

_2020-05-20_

### Breaking Changes

- feat: add kill-switch for mixed es-cjs modules (#358)
- feat: set syntheticNamedExports for commonjs modules (#149)

### Bugfixes

- fix: expose the virtual `require` function on mock `module`. fixes #307 (#326)
- fix: improved shouldWrap logic. fixes #304 (#355)

### Features

- feat: support for explicit module.require calls. fixes #310 (#325)

## v11.1.0

_2020-04-12_

### Bugfixes

- fix: produce legal variable names from filenames containing hyphens. (#201)

### Features

- feat: support dynamic require (#206)
- feat: export properties defined using Object.defineProperty(exports, ..) (#222)

### Updates

- chore: snapshot mismatch running tests before publish (d6bbfdd)
- test: add snapshots to all "function" tests (#218)

## v11.0.2

_2020-02-01_

### Updates

- docs: fix link for plugin-node-resolve (#170)
- chore: update dependencies (5405eea)
- chore: remove jsnext:main (#152)

## v11.0.1

_2020-01-04_

### Bugfixes

- fix: module.exports object spread (#121)

## 11.0.0

_2019-12-13_

- **Breaking:** Minimum compatible Rollup version is 1.20.0
- **Breaking:** Minimum supported Node version is 8.0.0
- Published as @rollup/plugin-commonjs

## 10.1.0

_2019-08-27_

- Normalize ids before looking up in named export map ([#406](https://github.com/rollup/rollup-plugin-commonjs/issues/406))
- Update README.md with note on symlinks ([#405](https://github.com/rollup/rollup-plugin-commonjs/issues/405))

## 10.0.2

_2019-08-03_

- Support preserveSymlinks: false ([#401](https://github.com/rollup/rollup-plugin-commonjs/issues/401))

## 10.0.1

_2019-06-27_

- Make tests run with Node 6 again and update dependencies ([#389](https://github.com/rollup/rollup-plugin-commonjs/issues/389))
- Handle builtins appropriately for resolve 1.11.0 ([#395](https://github.com/rollup/rollup-plugin-commonjs/issues/395))

## 10.0.0

_2019-05-15_

- Use new Rollup@1.12 context functions, fix issue when resolveId returns an object ([#387](https://github.com/rollup/rollup-plugin-commonjs/issues/387))

## 9.3.4

_2019-04-04_

- Make "extensions" optional ([#384](https://github.com/rollup/rollup-plugin-commonjs/issues/384))
- Use same typing for include and exclude properties ([#385](https://github.com/rollup/rollup-plugin-commonjs/issues/385))

## 9.3.3

_2019-04-04_

- Remove colon from module prefixes ([#371](https://github.com/rollup/rollup-plugin-commonjs/issues/371))

## 9.3.2

_2019-04-04_

- Use shared extractAssignedNames, fix destructuring issue ([#303](https://github.com/rollup/rollup-plugin-commonjs/issues/303))

## 9.3.1

_2019-04-04_

- Include typings in release ([#382](https://github.com/rollup/rollup-plugin-commonjs/issues/382))

## 9.3.0

_2019-04-03_

- Add TypeScript types ([#363](https://github.com/rollup/rollup-plugin-commonjs/issues/363))

## 9.2.3

_2019-04-02_

- Improve support for ES3 browsers ([#364](https://github.com/rollup/rollup-plugin-commonjs/issues/364))
- Add note about monorepo usage to readme ([#372](https://github.com/rollup/rollup-plugin-commonjs/issues/372))
- Add .js extension to generated helper file ([#373](https://github.com/rollup/rollup-plugin-commonjs/issues/373))

## 9.2.2

_2019-03-25_

- Handle array destructuring assignment ([#379](https://github.com/rollup/rollup-plugin-commonjs/issues/379))

## 9.2.1

_2019-02-23_

- Use correct context when manually resolving ids ([#370](https://github.com/rollup/rollup-plugin-commonjs/issues/370))

## 9.2.0

_2018-10-10_

- Fix missing default warning, produce better code when importing known ESM default exports ([#349](https://github.com/rollup/rollup-plugin-commonjs/issues/349))
- Refactor code and add prettier ([#346](https://github.com/rollup/rollup-plugin-commonjs/issues/346))

## 9.1.8

_2018-09-18_

- Ignore virtual modules created by other plugins ([#327](https://github.com/rollup/rollup-plugin-commonjs/issues/327))
- Add "location" and "process" to reserved words ([#330](https://github.com/rollup/rollup-plugin-commonjs/issues/330))

## 9.1.6

_2018-08-24_

- Keep commonJS detection between instantiations ([#338](https://github.com/rollup/rollup-plugin-commonjs/issues/338))

## 9.1.5

_2018-08-09_

- Handle object form of input ([#329](https://github.com/rollup/rollup-plugin-commonjs/issues/329))

## 9.1.4

_2018-07-27_

- Make "from" a reserved word ([#320](https://github.com/rollup/rollup-plugin-commonjs/issues/320))

## 9.1.3

_2018-04-30_

- Fix a caching issue ([#316](https://github.com/rollup/rollup-plugin-commonjs/issues/316))

## 9.1.2

_2018-04-30_

- Re-publication of 9.1.0

## 9.1.1

_2018-04-30_

- Fix ordering of modules when using rollup 0.58 ([#302](https://github.com/rollup/rollup-plugin-commonjs/issues/302))

## 9.1.0

- Do not automatically wrap modules with return statements in top level arrow functions ([#302](https://github.com/rollup/rollup-plugin-commonjs/issues/302))

## 9.0.0

- Make rollup a peer dependency with a version range ([#300](https://github.com/rollup/rollup-plugin-commonjs/issues/300))

## 8.4.1

- Re-release of 8.3.0 as #287 was actually a breaking change

## 8.4.0

- Better handle non-CJS files that contain CJS keywords ([#285](https://github.com/rollup/rollup-plugin-commonjs/issues/285))
- Use rollup's plugin context`parse` function ([#287](https://github.com/rollup/rollup-plugin-commonjs/issues/287))
- Improve error handling ([#288](https://github.com/rollup/rollup-plugin-commonjs/issues/288))

## 8.3.0

- Handle multiple entry points ([#283](https://github.com/rollup/rollup-plugin-commonjs/issues/283))
- Extract named exports from exported object literals ([#272](https://github.com/rollup/rollup-plugin-commonjs/issues/272))
- Fix when `options.external` is modified by other plugins ([#264](https://github.com/rollup/rollup-plugin-commonjs/issues/264))
- Recognize static template strings in require statements ([#271](https://github.com/rollup/rollup-plugin-commonjs/issues/271))

## 8.2.4

- Don't import default from ES modules that don't export default ([#206](https://github.com/rollup/rollup-plugin-commonjs/issues/206))

## 8.2.3

- Prevent duplicate default exports ([#230](https://github.com/rollup/rollup-plugin-commonjs/pull/230))
- Only include default export when it exists ([#226](https://github.com/rollup/rollup-plugin-commonjs/pull/226))
- Deconflict `require` aliases ([#232](https://github.com/rollup/rollup-plugin-commonjs/issues/232))

## 8.2.1

- Fix magic-string deprecation warning

## 8.2.0

- Avoid using `index` as a variable name ([#208](https://github.com/rollup/rollup-plugin-commonjs/pull/208))

## 8.1.1

- Compatibility with 0.48 ([#220](https://github.com/rollup/rollup-plugin-commonjs/issues/220))

## 8.1.0

- Handle `options.external` correctly ([#212](https://github.com/rollup/rollup-plugin-commonjs/pull/212))
- Support top-level return ([#195](https://github.com/rollup/rollup-plugin-commonjs/pull/195))

## 8.0.2

- Fix another `var` rewrite bug ([#181](https://github.com/rollup/rollup-plugin-commonjs/issues/181))

## 8.0.1

- Remove declarators within a var declaration correctly ([#179](https://github.com/rollup/rollup-plugin-commonjs/issues/179))

## 8.0.0

- Prefer the names dependencies are imported by for the common `var foo = require('foo')` pattern ([#176](https://github.com/rollup/rollup-plugin-commonjs/issues/176))

## 7.1.0

- Allow certain `require` statements to pass through unmolested ([#174](https://github.com/rollup/rollup-plugin-commonjs/issues/174))

## 7.0.2

- Handle duplicate default exports ([#158](https://github.com/rollup/rollup-plugin-commonjs/issues/158))

## 7.0.1

- Fix exports with parentheses ([#168](https://github.com/rollup/rollup-plugin-commonjs/issues/168))

## 7.0.0

- Rewrite `typeof module`, `typeof module.exports` and `typeof exports` as `'object'` ([#151](https://github.com/rollup/rollup-plugin-commonjs/issues/151))

## 6.0.1

- Don't overwrite globals ([#127](https://github.com/rollup/rollup-plugin-commonjs/issues/127))

## 6.0.0

- Rewrite top-level `define` as `undefined`, so AMD-first UMD blocks do not cause breakage ([#144](https://github.com/rollup/rollup-plugin-commonjs/issues/144))
- Support ES2017 syntax ([#132](https://github.com/rollup/rollup-plugin-commonjs/issues/132))
- Deconflict exported reserved keywords ([#116](https://github.com/rollup/rollup-plugin-commonjs/issues/116))

## 5.0.5

- Fix parenthesis wrapped exports ([#120](https://github.com/rollup/rollup-plugin-commonjs/issues/120))

## 5.0.4

- Ensure named exports are added to default export in optimised modules ([#112](https://github.com/rollup/rollup-plugin-commonjs/issues/112))

## 5.0.3

- Respect custom `namedExports` in optimised modules ([#35](https://github.com/rollup/rollup-plugin-commonjs/issues/35))

## 5.0.2

- Replace `require` (outside call expressions) with `commonjsRequire` helper ([#77](https://github.com/rollup/rollup-plugin-commonjs/issues/77), [#83](https://github.com/rollup/rollup-plugin-commonjs/issues/83))

## 5.0.1

- Deconflict against globals ([#84](https://github.com/rollup/rollup-plugin-commonjs/issues/84))

## 5.0.0

- Optimise modules that don't need to be wrapped in a function ([#106](https://github.com/rollup/rollup-plugin-commonjs/pull/106))
- Ignore modules containing `import` and `export` statements ([#96](https://github.com/rollup/rollup-plugin-commonjs/pull/96))

## 4.1.0

- Ignore dead branches ([#93](https://github.com/rollup/rollup-plugin-commonjs/issues/93))

## 4.0.1

- Fix `ignoreGlobal` option ([#86](https://github.com/rollup/rollup-plugin-commonjs/pull/86))

## 4.0.0

- Better interop and smaller output ([#92](https://github.com/rollup/rollup-plugin-commonjs/pull/92))

## 3.3.1

- Deconflict export and local module ([rollup/rollup#554](https://github.com/rollup/rollup/issues/554))

## 3.3.0

- Keep the order of execution for require calls ([#43](https://github.com/rollup/rollup-plugin-commonjs/pull/43))
- Use interopDefault as helper ([#42](https://github.com/rollup/rollup-plugin-commonjs/issues/42))

## 3.2.0

- Use named exports as a function when no default export is defined ([#524](https://github.com/rollup/rollup/issues/524))

## 3.1.0

- Replace `typeof require` with `'function'` ([#38](https://github.com/rollup/rollup-plugin-commonjs/issues/38))
- Don't attempt to resolve entry file relative to importer ([#63](https://github.com/rollup/rollup-plugin-commonjs/issues/63))

## 3.0.2

- Handle multiple references to `global`

## 3.0.1

- Return a `name`

## 3.0.0

- Make `transform` stateless ([#71](https://github.com/rollup/rollup-plugin-commonjs/pull/71))
- Support web worker `global` ([#50](https://github.com/rollup/rollup-plugin-commonjs/issues/50))
- Ignore global with `options.ignoreGlobal` ([#48](https://github.com/rollup/rollup-plugin-commonjs/issues/48))

## 2.2.1

- Prevent false positives with `namedExports` ([#36](https://github.com/rollup/rollup-plugin-commonjs/issues/36))

## 2.2.0

- Rewrite top-level `this` expressions to mean the same as `global` ([#31](https://github.com/rollup/rollup-plugin-commonjs/issues/31))

## 2.1.0

- Optimised module wrappers ([#20](https://github.com/rollup/rollup-plugin-commonjs/pull/20))
- Allow control over named exports via `options.namedExports` ([#18](https://github.com/rollup/rollup-plugin-commonjs/issues/18))
- Handle bare imports correctly ([#23](https://github.com/rollup/rollup-plugin-commonjs/issues/23))
- Blacklist all reserved words as export names ([#21](https://github.com/rollup/rollup-plugin-commonjs/issues/21))
- Configure allowed file extensions via `options.extensions` ([#27](https://github.com/rollup/rollup-plugin-commonjs/pull/27))

## 2.0.0

- Support for transpiled modules – `exports.default` is used as the default export in place of `module.exports`, if applicable, and `__esModule` is not exported ([#16](https://github.com/rollup/rollup-plugin-commonjs/pull/16))

## 1.4.0

- Generate sourcemaps by default

## 1.3.0

- Handle references to `global` ([#6](https://github.com/rollup/rollup-plugin-commonjs/issues/6))

## 1.2.0

- Generate named exports where possible ([#5](https://github.com/rollup/rollup-plugin-commonjs/issues/5))
- Handle shadowed `require`/`module`/`exports`

## 1.1.0

- Handle dots in filenames ([#3](https://github.com/rollup/rollup-plugin-commonjs/issues/3))
- Wrap modules in IIFE for more readable output

## 1.0.0

- Stable release, now that Rollup supports plugins

## 0.2.1

- Allow mixed CommonJS/ES6 imports/exports
- Use `var` instead of `let`

## 0.2.0

- Sourcemap support
- Support `options.include` and `options.exclude`
- Bail early if module is obviously not a CommonJS module

## 0.1.1

Add dist files to package (whoops!)

## 0.1.0

- First release
