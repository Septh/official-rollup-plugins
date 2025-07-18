# @rollup/pluginutils ChangeLog

## v5.2.0

_2025-06-17_

### Features

- feat: add `exactRegex` and `prefixRegex` (#1865)

## v5.1.4

_2024-12-15_

### Updates

- refactor: replace `test` with `includes` (#1787)

## v5.1.3

_2024-10-23_

### Bugfixes

- fix: upgrade picomatch (#1796)

## v5.1.2

_2024-09-23_

### Bugfixes

- fix: optimize `createFilter` and `normalizePath` (#1750)

## v5.1.1

_2024-09-22_

### Bugfixes

- fix: improve regex performance (#1753)

## v5.1.0

_2023-11-28_

### Features

- feat: add `includeArbitraryNames: true` to `dataToEsm` (#1635)

### Updates

- doc: correct the return type of createFilter (#1633)

## v5.0.5

_2023-10-05_

### Bugfixes

- fix: ensure rollup 4 compatibility [#1595](https://github.com/rollup/plugins/pull/1595)

## v5.0.4

_2023-08-26_

### Updates

- docs: configure correct options [#1563](https://github.com/rollup/plugins/pull/1563)

## v5.0.3

_2023-08-13_

### Bugfixes

- fix: add current working dirctory when pattern starts with one \* [#1547](https://github.com/rollup/plugins/pull/1547)

## v5.0.2

_2022-10-21_

### Updates

- chore: update rollup dependencies ([3038271](https://github.com/rollup/plugins/commit/303827191ede6b2e4eade96c6968ed16a587683f))

## v5.0.1

_2022-10-13_

### Bugfixes

- fix: Move `@types/estree` to dependencies (fixes #1315) [#1320](https://github.com/rollup/plugins/pull/1320)

## v5.0.0

_2022-10-10_

### Breaking Changes

- fix: prepare for Rollup 3 [#1287](https://github.com/rollup/plugins/pull/1287)

## v4.2.1

_2022-04-13_

### Bugfixes

- fix: fix path normalisation for createFilter on absolute and \* paths (#1161)

## v4.2.0

_2022-03-07_

### Features

- feat: support bigint and symbol in dataToEsm (#1047)

## v4.1.2

_2021-12-13_

### Bugfixes

- fix: correct minimatch to picomatch in TSDoc (#1057)

## v4.1.1

_2021-07-16_

### Bugfixes

- fix: remove extraneous peer dependency requirement (#845)

## v4.1.0

_2020-10-27_

### Bugfixes

- fix: attach scope object to for-loop (#616)

### Features

- feat: normalizePath (#550)

### Updates

- refactor: improve readability of attachScopes test (#551)

## v4.0.0

_2020-08-13_

### Breaking Changes

- fix!: don't add cwd to absolute or patterns that start with a glob (#517)

### Bugfixes

- fix: resolve relative paths starting with "./" (#180)

### Features

- feat: add native node es modules support (#419)

### Updates

- docs: Correct minimatch to picomatch (#525)
- chore: update dependencies (9f56d37)
- refactor: replace micromatch with picomatch. (#306)
- chore: Don't bundle micromatch (#220)
- chore: add missing typescript devDep (238b140)
- chore: Use readonly arrays, add TSDoc (#187)
- chore: Use typechecking (2ae08eb)

## v3.1.0

_2020-06-05_

### Bugfixes

- fix: resolve relative paths starting with "./" (#180)

### Features

- feat: add native node es modules support (#419)

### Updates

- refactor: replace micromatch with picomatch. (#306)
- chore: Don't bundle micromatch (#220)
- chore: add missing typescript devDep (238b140)
- chore: Use readonly arrays, add TSDoc (#187)
- chore: Use typechecking (2ae08eb)

## v3.0.10

_2020-05-02_

### Bugfixes

- fix: resolve relative paths starting with "./" (#180)

### Updates

- refactor: replace micromatch with picomatch. (#306)
- chore: Don't bundle micromatch (#220)
- chore: add missing typescript devDep (238b140)
- chore: Use readonly arrays, add TSDoc (#187)
- chore: Use typechecking (2ae08eb)

## v3.0.9

_2020-04-12_

### Updates

- chore: support Rollup v2

## v3.0.8

_2020-02-01_

### Bugfixes

- fix: resolve relative paths starting with "./" (#180)

### Updates

- chore: add missing typescript devDep (238b140)
- chore: Use readonly arrays, add TSDoc (#187)
- chore: Use typechecking (2ae08eb)

## v3.0.7

_2020-02-01_

### Bugfixes

- fix: resolve relative paths starting with "./" (#180)

### Updates

- chore: Use readonly arrays, add TSDoc (#187)
- chore: Use typechecking (2ae08eb)

## v3.0.6

_2020-01-27_

### Bugfixes

- fix: resolve relative paths starting with "./" (#180)

## v3.0.5

_2020-01-25_

### Bugfixes

- fix: bring back named exports (#176)

## v3.0.4

_2020-01-10_

### Bugfixes

- fix: keep for(const..) out of scope (#151)

## v3.0.3

_2020-01-07_

### Bugfixes

- fix: createFilter Windows regression (#141)

### Updates

- test: fix windows path failure (0a0de65)
- chore: fix test script (5eae320)

## v3.0.2

_2020-01-04_

### Bugfixes

- fix: makeLegalIdentifier - potentially unsafe input for blacklisted identifier (#116)

### Updates

- docs: Fix documented type of createFilter's include/exclude (#123)
- chore: update minor linting correction (bcbf9d2)

## 3.0.1

- fix: Escape glob characters in folder (#84)

## 3.0.0

_2019-11-25_

- **Breaking:** Minimum compatible Rollup version is 1.20.0
- **Breaking:** Minimum supported Node version is 8.0.0
- Published as @rollup/plugins-image

## 2.8.2

_2019-09-13_

- Handle optional catch parameter in attachScopes ([#70](https://github.com/rollup/rollup-pluginutils/pulls/70))

## 2.8.1

_2019-06-04_

- Support serialization of many edge cases ([#64](https://github.com/rollup/rollup-pluginutils/issues/64))

## 2.8.0

_2019-05-30_

- Bundle updated micromatch dependency ([#60](https://github.com/rollup/rollup-pluginutils/issues/60))

## 2.7.1

_2019-05-17_

- Do not ignore files with a leading "." in createFilter ([#62](https://github.com/rollup/rollup-pluginutils/issues/62))

## 2.7.0

_2019-05-15_

- Add `resolve` option to createFilter ([#59](https://github.com/rollup/rollup-pluginutils/issues/59))

## 2.6.0

_2019-04-04_

- Add `extractAssignedNames` ([#59](https://github.com/rollup/rollup-pluginutils/issues/59))
- Provide dedicated TypeScript typings file ([#58](https://github.com/rollup/rollup-pluginutils/issues/58))

## 2.5.0

_2019-03-18_

- Generalize dataToEsm type ([#55](https://github.com/rollup/rollup-pluginutils/issues/55))
- Handle empty keys in dataToEsm ([#56](https://github.com/rollup/rollup-pluginutils/issues/56))

## 2.4.1

_2019-02-16_

- Remove unnecessary dependency

## 2.4.0

_2019-02-16_
Update dependencies to solve micromatch vulnerability ([#53](https://github.com/rollup/rollup-pluginutils/issues/53))

## 2.3.3

_2018-09-19_

- Revert micromatch update ([#43](https://github.com/rollup/rollup-pluginutils/issues/43))

## 2.3.2

_2018-09-18_

- Bumb micromatch dependency ([#36](https://github.com/rollup/rollup-pluginutils/issues/36))
- Bumb dependencies ([#41](https://github.com/rollup/rollup-pluginutils/issues/41))
- Split up tests ([#40](https://github.com/rollup/rollup-pluginutils/issues/40))

## 2.3.1

_2018-08-06_

- Fixed ObjectPattern scope in attachScopes to recognise { ...rest } syntax ([#37](https://github.com/rollup/rollup-pluginutils/issues/37))

## 2.3.0

_2018-05-21_

- Add option to not generate named exports ([#32](https://github.com/rollup/rollup-pluginutils/issues/32))

## 2.2.1

_2018-05-21_

- Support `null` serialization ([#34](https://github.com/rollup/rollup-pluginutils/issues/34))

## 2.2.0

_2018-05-11_

- Improve white-space handling in `dataToEsm` and add `prepare` script ([#31](https://github.com/rollup/rollup-pluginutils/issues/31))

## 2.1.1

_2018-05-09_

- Update dependencies

## 2.1.0

_2018-05-08_

- Add `dataToEsm` helper to create named exports from objects ([#29](https://github.com/rollup/rollup-pluginutils/issues/29))
- Support literal keys in object patterns ([#27](https://github.com/rollup/rollup-pluginutils/issues/27))
- Support function declarations without id in `attachScopes` ([#28](https://github.com/rollup/rollup-pluginutils/issues/28))

## 2.0.1

_2017-01-03_

- Don't add extension to file with trailing dot ([#14](https://github.com/rollup/rollup-pluginutils/issues/14))

## 2.0.0

_2017-01-03_

- Use `micromatch` instead of `minimatch` ([#19](https://github.com/rollup/rollup-pluginutils/issues/19))
- Allow `createFilter` to take regexes ([#5](https://github.com/rollup/rollup-pluginutils/issues/5))

## 1.5.2

_2016-08-29_

- Treat `arguments` as a reserved word ([#10](https://github.com/rollup/rollup-pluginutils/issues/10))

## 1.5.1

_2016-06-24_

- Add all declarators in a var declaration to scope, not just the first

## 1.5.0

_2016-06-07_

- Exclude IDs with null character (`\0`)

## 1.4.0

_2016-06-07_

- Workaround minimatch issue ([#6](https://github.com/rollup/rollup-pluginutils/pull/6))
- Exclude non-string IDs in `createFilter`

## 1.3.1

_2015-12-16_

- Build with Rollup directly, rather than via Gobble

## 1.3.0

_2015-12-16_

- Use correct path separator on Windows

## 1.2.0

_2015-11-02_

- Add `attachScopes` and `makeLegalIdentifier`

## 1.1.0

2015-10-24\*

- Add `addExtension` function

## 1.0.1

_2015-10-24_

- Include dist files in package

## 1.0.0

_2015-10-24_

- First release
