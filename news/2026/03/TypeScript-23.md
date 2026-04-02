# Report for 2026-03-23 (Monday, March 23rd, 2026)

12 different users commented on 49 different issues.

## Recommended Actions

 * Response Recommended
    * @danciudev asked whether VS Code's autocomplete supports subpath imports in [microsoft/TypeScript#62844](https://github.com/microsoft/TypeScript/pull/62844#issuecomment-4113605129)
    * @amanmahajan7 asked whether TypeScript 6.0’s package.json imports fully replace tsconfig.paths or if tsconfig.paths are still required for type checking in [microsoft/TypeScript#62844](https://github.com/microsoft/TypeScript/pull/62844#issuecomment-4114694076)
    * @BillionClaw offered to submit a fix for the misleading Chinese translation in [microsoft/TypeScript#63274](https://github.com/microsoft/TypeScript/issues/63274#issuecomment-4115353850)

## Activity Summary

### [Issue microsoft/TypeScript#53968](https://github.com/microsoft/TypeScript/issues/53968) (Closed, `Bug`, `Help Wanted`, `Domain: JS Emit`)

**AMD translation for export \* as ns is wrong**

*The AMD emitter generates incorrect code for export * as x, referencing an undeclared identifier x.*

 * (2.9 years ago) **RyanCavanaugh** added labels `Help Wanted`, `Domain: JS Emit`, and set milestone to `Backlog`
 * [later](https://github.com/microsoft/TypeScript/issues/53968#issuecomment-4117999807) **Jack-Works** said "amd is deprecated"
 * (later) **Jack-Works** closed the issue

### [Issue microsoft/TypeScript#60082](https://github.com/microsoft/TypeScript/issues/60082) (Open, `Needs Investigation`)

**autoImportSpecifierExcludeRegexes needs a window refresh for changes to take effect**

*Changes to autoImportSpecifierExcludeRegexes in VSCode settings only apply after reloading the window instead of immediately.*

 * [50 weeks ago](https://github.com/microsoft/TypeScript/issues/60082#issuecomment-2780630473) **tusharsnx** noted that restarting the TS server also applied autoImportSpecifierExcludeRegexes changes
 * **mjbvz** unassigned **mjbvz**
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/60082#issuecomment-4049066466) **jedwards1211** asked if the setting did not work anymore even after restarting VSCode
 * [today](https://github.com/microsoft/TypeScript/issues/60082#issuecomment-4112009034) **craig-jennings** said "@jedwards1211 I'm seeing the same. Looks like this setting is broken."

### [PR microsoft/TypeScript#62844](https://github.com/microsoft/TypeScript/pull/62844) (Closed, `For Milestone Bug`)

**Allow subpath imports that start with \`\#/\`**

*Allow subpath imports starting with '#/' in package.json imports to mirror matching exports entries.*

 * (14 weeks ago) **andrewbranch** closed the issue
 * [14 weeks ago](https://github.com/microsoft/TypeScript/pull/62844#issuecomment-3638995505) **Scalahansolo** said "Excuse my ignorance, but for a PR like this that is marked for TS 6.0, when / what is the process for this landing in TS 7?"
 * [14 weeks ago](https://github.com/microsoft/TypeScript/pull/62844#issuecomment-3639169765) **RyanCavanaugh** said "Great question! It needs to be ported now. I started https://github.com/microsoft/typescript-go/pull/2330 and we'll see how that goes"
 * [today](https://github.com/microsoft/TypeScript/pull/62844#issuecomment-4113605129) **danciudev** said "I can't get VS Code's autocomplete to work with subpath imports. Is it possible that it doesn't support this yet?"
 * [today](https://github.com/microsoft/TypeScript/pull/62844#issuecomment-4114694076) **amanmahajan7** asked whether TypeScript 6.0’s package.json imports could fully replace tsconfig.paths or if tsconfig.paths remain required for type checking
 * [later](https://github.com/microsoft/TypeScript/pull/62844#issuecomment-4119107621) **andrewbranch** explained that subpath imports have been supported for type checking since TypeScript 4.7, eliminating the need to duplicate Node.js imports in tsconfig paths and that Node.js 20+ and TypeScript 6.0+ simply expand the valid syntax

### [Issue microsoft/TypeScript#63085](https://github.com/microsoft/TypeScript/issues/63085) (Open, `Planning`)

**TypeScript 6\.0 Iteration Plan**

*The TypeScript 6.0 iteration plan details milestone dates and scheduled compiler additions, language improvements, breaking changes, and deprecations.*

 * [4 days ago](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-4094003838) **simonbuchan** joked about looking like a fool for promising the release on the 17th
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-4099966321) **RyanCavanaugh** said "We hit some issues when testing in Visual Studio, so 23 is the new 17"
 * [today](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-4111624942) **RyanCavanaugh** said "6.0.0 RC was already released, see https://devblogs.microsoft.com/typescript/announcing-typescript-6-0-rc/ or npm install typescript@rc"
 * [today](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-4112022731) **RyanCavanaugh** said "https://devblogs.microsoft.com/typescript/announcing-typescript-6-0/"

### [PR microsoft/TypeScript#63246](https://github.com/microsoft/TypeScript/pull/63246) (Closed, **DanielRosenwasser**)

**🤖 Pick PR \#63239 \(Fix missing lib files in reused pro\.\.\.\) into release\-6\.0**

*Cherry-pick PR #63239 into the release-6.0 branch to restore missing library files.*

 * created by **typescript-bot**
 * **typescript-bot** assigned to **DanielRosenwasser**
 * (1 week ago) **RyanCavanaugh** closed the issue
 * **DanielRosenwasser** added to milestone `TypeScript 6.0.2`

### [Issue microsoft/TypeScript#63259](https://github.com/microsoft/TypeScript/issues/63259) (Closed, `Duplicate`)

**Type narrowing incorrect when providing some function generics when default generics present**

*Functions with default generic parameters don’t correctly narrow union-based argument types when only some generics are explicitly provided.*

 * created by **ChromeQ**
 * [6 days ago](https://github.com/microsoft/TypeScript/issues/63259#issuecomment-4079131983) **MartinJohns** stated that generic type inference is all or none and marked the issue as duplicate of #26242
 * **RyanCavanaugh** added label `Duplicate`

### [Issue microsoft/TypeScript#63269](https://github.com/microsoft/TypeScript/issues/63269) (Open, `Bug`, `Domain: check: Type Circularity`)

**Regression: RangeError: Maximum call stack size exceeded in instantiateTypeWorker with recursive intersections and invalid type queries**

*Recursive intersection and invalid type query patterns cause a RangeError maximum call stack size exceeded in instantiateTypeWorker in TypeScript 5.7.3 through 5.9.3 and nightly builds.*

 * (4 days ago) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`
 * [4 days ago](https://github.com/microsoft/TypeScript/issues/63269#issuecomment-4093876109) **RyanCavanaugh** said "Confirmed repro in TS7"
 * **RyanCavanaugh** added label `Domain: check: Type Circularity`

### [Issue microsoft/TypeScript#63270](https://github.com/microsoft/TypeScript/issues/63270) (Open, `Bug`, `Domain: check: Type Circularity`)

**Crash: RangeError: Maximum call stack size exceeded in isRelatedTo with recursive tuple types and spread elements**

*TypeScript's type checker overflows the call stack when processing recursive variadic tuple types with spread elements.*

 * created by **na7ure-a**
 * (4 days ago) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`
 * **RyanCavanaugh** added label `Domain: check: Type Circularity`

### [Issue microsoft/TypeScript#63271](https://github.com/microsoft/TypeScript/issues/63271) (Open, `Bug`, `Domain: Crashes`)

**Crash: RangeError: Invalid string length in addSpans during instantiation of recursive template literal types**

*TypeScript crashes with a RangeError due to exponential string growth in deeply recursive template literal type instantiation*

 * created by **na7ure-a**
 * (3 days ago) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`
 * **RyanCavanaugh** added label `Domain: Crashes`

### [Issue microsoft/TypeScript#63273](https://github.com/microsoft/TypeScript/issues/63273) (Open, `Bug`, `Domain: check: Type Circularity`)

**Crash: RangeError: Maximum call stack size exceeded in getNameOfSymbolAsWritten via recursive conditional ReturnType**

*The TypeScript compiler crashes with a maximum call stack size exceeded error when handling a recursive conditional ReturnType in a clone function.*

 * created by **na7ure-a**
 * (3 days ago) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`
 * **RyanCavanaugh** added label `Domain: check: Type Circularity`

### [Issue microsoft/TypeScript#63274](https://github.com/microsoft/TypeScript/issues/63274) (Open, `Bug`, `Domain: Error Messages`, `i18n`)

**\[Localization\] Misleading Chinese translation for TS2561 error message**

*The Chinese translation for TS2561 error message incorrectly swaps the property and type relationship, causing confusion and requiring correction.*

 * created by **HHaoWang**
 * (3 days ago) **RyanCavanaugh** added labels `Bug`, `i18n`
 * **RyanCavanaugh** added label `Domain: Error Messages`
 * [today](https://github.com/microsoft/TypeScript/issues/63274#issuecomment-4115353850) **BillionClaw** said "I've been looking into the Chinese translation for TS2561 — happy to submit a fix for the misleading text."

### [Issue microsoft/TypeScript#63276](https://github.com/microsoft/TypeScript/issues/63276) (Closed)

**Missing \`undefined\` for hover**

*VSCode's hover tooltip for a type with several optional properties only displays '| undefined' on the first property, omitting it on the others when exactOptionalPropertyTypes is false.*

 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63276#issuecomment-4097328396) **ace-tk** said "Can u please review the fixes i made."
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63276#issuecomment-4106954431) **AlejandroGispert** offered to look at and fix the issue if still open
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63276#issuecomment-4107444408) **Withered-Flower-0422** said "I think the fixes @ace-tk made should work."
 * [today](https://github.com/microsoft/TypeScript/issues/63276#issuecomment-4112968346) **RyanCavanaugh** said "We're not taking cosmetic fixes for 6.0 at this point, see #62827 / #62963. Please log an issue in the typescript-go repo if this repros in TS 7 preview"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63281](https://github.com/microsoft/TypeScript/issues/63281) (Open, `Suggestion`, `Awaiting More Feedback`)

**RegExpIndicesArray \- Named group indices can be undefined**

*TypeScript’s RegExpIndicesArray incorrectly assumes named regex group index arrays are always defined, missing errors for undefined groups.*

 * created by **TomStrepsil**
 * [today](https://github.com/microsoft/TypeScript/issues/63281#issuecomment-4113099347) **RyanCavanaugh** said "I think this falls under #32098"
 * [today](https://github.com/microsoft/TypeScript/issues/63281#issuecomment-4113654374) **TomStrepsil** clarified that strong key typing for named capture groups is a larger change and unrelated to the undefined value issue

### [PR microsoft/TypeScript#63288](https://github.com/microsoft/TypeScript/pull/63288) (Closed)

**Fix crash when inferring from tuple with middle rest and trailing variadic elements**

*Add null checks to prevent compiler crashes when inferring types from tuples with middle rest and trailing variadic elements.*

 * created by **ongjin**
 * [today](https://github.com/microsoft/TypeScript/pull/63288#issuecomment-4115560016) **ongjin** said "@microsoft-github-policy-service agree"

### [Issue microsoft/TypeScript#63289](https://github.com/microsoft/TypeScript/issues/63289) (Closed)

**Unexpected Canonical Type Produced for Intersected Optional Property with Array**

*TypeScript fails to canonicalize an intersected optional array property union, producing a stray undefined in the resulting type.*

 * created by **sinclairzx81**

### [PR microsoft/TypeScript#63290](https://github.com/microsoft/TypeScript/pull/63290) (Closed)

**fix: handle inspector session leak on Profiler\.enable/start failure**

*Failure to handle errors in Profiler.enable and Profiler.start leads to lingering inspector sessions, so callbacks should disconnect on error.*

 * created by **buley**

### [Issue microsoft/TypeScript#63291](https://github.com/microsoft/TypeScript/issues/63291) (Open, `Needs Investigation`, **ahejlsberg**)

**Removing optional modifier in a mapped type behaves inconsistently b/w array vs object**

*Under exactOptionalPropertyTypes, mapped array types lose undefined unions when removing optional modifiers, unlike object types.*

 * created by **juhort**

