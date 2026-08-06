# Report for 2026-08-05 (Wednesday, August 5th, 2026)

10 different users commented on 11 different issues.

## Recommended Actions

 * Response Recommended
    * @aweebit proposed introducing strictLookupTypes and asked how to solve the issue without reverting #41921 in [microsoft/TypeScript#63709](https://github.com/microsoft/TypeScript/issues/63709#issuecomment-5199270589)
    * @aweebit provided additional context and examples from a related issue in [microsoft/TypeScript#63709](https://github.com/microsoft/TypeScript/issues/63709#issuecomment-5204328086)
    * @goutamadwant asked for feedback on the proposed fix in [microsoft/TypeScript#63718](https://github.com/microsoft/TypeScript/issues/63718#issuecomment-5200200361)
    * @wartab reported a potential bug regarding Uppercase<string> type narrowing in [microsoft/TypeScript#63724](https://github.com/microsoft/TypeScript/issues/63724#issuecomment-5204072640)
    * @aweebit provided a minimal reproducing demonstration of the issue in [microsoft/TypeScript#63725](https://github.com/microsoft/TypeScript/issues/63725#issuecomment-5205092689)

## Activity Summary

### [Issue microsoft/TypeScript#42219](https://github.com/microsoft/TypeScript/issues/42219) (Open, `Suggestion`, `Awaiting More Feedback`)

**\[Feature\] Import non\-js content as const string**

*Enable importing non-JS file content as const string with compile-time TypeScript types via import.meta.content.*

 * [29 weeks ago](https://github.com/microsoft/TypeScript/issues/42219#issuecomment-3732822567) **valler** said "This should be compatible with type stripping, so it should be a JS feature really. The request is not so much about typing, but to reduce the need for custom loaders and/or intermediary build steps."
 * [17 weeks ago](https://github.com/microsoft/TypeScript/issues/42219#issuecomment-4177548196) **linusg** mentioned that importing modules as plain text was being standardized in TC39 via import attributes and linked to the stage 3 proposal
 * [8 weeks ago](https://github.com/microsoft/TypeScript/issues/42219#issuecomment-4619886824) **mariusGundersen** noted that importing as text is now supported in Bun, Deno, and Firefox Nightly and linked a blog post
 * [later](https://github.com/microsoft/TypeScript/issues/42219#issuecomment-5201545056) **mariusGundersen** noted that importing as text was now supported in Firefox 153

### [Issue microsoft/TypeScript#50466](https://github.com/microsoft/TypeScript/issues/50466) (Open, `Needs Investigation`, **weswigham**)

**NodeNext resolution failed to resolve dual\-package correctly**

*NodeNext resolution incorrectly resolves a dual-package by selecting the CommonJS export instead of the type definitions, causing a TS2349 error.*

 * [3.6 years ago](https://github.com/microsoft/TypeScript/issues/50466#issuecomment-1346916117) **justinhelmer** described adding dual package exports solution for TypeScript including package.json and tsconfig configurations and the requirement of separate *.d.cts files for CJS consumers
 * [2.5 years ago](https://github.com/microsoft/TypeScript/issues/50466#issuecomment-1880582216) **kerambit** mentioned encountering the same problem, referenced a linked solution, and noted that consumer code must use CJS although docs recommend nodenext
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/50466#issuecomment-5172407186) **miami-man** said "Has this been resolved yet? I've been using a command line tool to automate this process for a few years now, so have lost track of status. "
 * [today](https://github.com/microsoft/TypeScript/issues/50466#issuecomment-5195005662) **andrewbranch** said "I don’t know why this wasn’t closed as “Working as Intended.”"

### [Issue microsoft/TypeScript#63709](https://github.com/microsoft/TypeScript/issues/63709) (Open, `Fix Available`, `Cursed?`, `Possible Improvement`)

**Property lookups on arguments to type parameters constrained by string index signatures can violate other constraints because undefined is included for optional properties**

*Property lookups on generics constrained by string index signatures include undefined for optional properties, allowing type constraint violations to go undetected.*

 * (yesterday) **RyanCavanaugh** added label `Possible Improvement`, and set milestone to `Dormant`
 * **typescript-automation[bot]** added label `Fix Available`
 * [today](https://github.com/microsoft/TypeScript/issues/63709#issuecomment-5199270589) **aweebit** explained reasons why index signatures should assume optionality and proposed introducing a new tsconfig option strictLookupTypes to enforce strict checking of lookup types
 * [later](https://github.com/microsoft/TypeScript/issues/63709#issuecomment-5204328086) **aweebit** demonstrated that the same issue with undefined in lookup types due to optional keys occurs in another TypeScript example and linked to the related issue

### [Issue microsoft/TypeScript#63718](https://github.com/microsoft/TypeScript/issues/63718) (Open, `Bug`, `Help Wanted`)

**TS1518 depends on operand order in negated v\-mode class unions**

*TS1518 detection for negated v-mode RegExp character class unions is order-dependent, failing to flag invalid patterns when the string-pattern operand is second.*

 * created by **mohsen1**
 * (today) **RyanCavanaugh** added labels `Bug`, `Help Wanted`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/63718#issuecomment-5200200361) **goutamadwant** opened pull request #63723 with a fix and regression baselines, explained it evaluates every ClassUnion operand for MayContainStrings and reports TS1518 regardless of operand order, and asked for feedback

### [Issue microsoft/TypeScript#63719](https://github.com/microsoft/TypeScript/issues/63719) (Closed, `Not a Defect`)

**ReDoS via typesMap\.json regex injection in loadTypesMap\(\)**

*Unsanitized regex patterns in typesMap.json cause ReDoS in the TypeScript language server.*

 * created by **bolverk**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63719#issuecomment-5187697061) **MartinJohns** argued that the described vulnerability was a non-issue because a supply chain compromise posed a greater risk than regex exhaustion
 * **RyanCavanaugh** added label `Not a Defect`
 * [today](https://github.com/microsoft/TypeScript/issues/63719#issuecomment-5198540748) **RyanCavanaugh** said "typesMaps.json is just as modifiable as tsserver.js. If the attacker has control at this scope, a delay is the least of your worries -- they're able to run arbitrary code."
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63721](https://github.com/microsoft/TypeScript/issues/63721) (Closed)

**ReDoS via autoImportSpecifierExcludeRegexes in stringToRegex\(\)**

*User regex patterns in autoImportSpecifierExcludeRegexes are passed unsanitized to new RegExp, causing ReDoS and hanging the TypeScript language server.*

 * created by **bolverk**
 * [today](https://github.com/microsoft/TypeScript/issues/63721#issuecomment-5191792705) **nmain** noted that the Go rewrite uses RE2-based regex immune to ReDoS and mentioned that the AI thought the issue was already fixed
 * [today](https://github.com/microsoft/TypeScript/issues/63721#issuecomment-5195085515) **RyanCavanaugh** said "Yeah, sounds like it's fixed"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63722](https://github.com/microsoft/TypeScript/issues/63722) (Open, `Help Wanted`, `Domain: lib.d.ts`)

**\`Array\.prototype\.at\` docs use "code unit" instead of "item"**

*Array.prototype.at documentation mistakenly uses 'code unit' instead of 'item' or 'element' terminology.*

 * created by **grundb**
 * **RyanCavanaugh** added label `Domain: lib.d.ts`
 * [today](https://github.com/microsoft/TypeScript/issues/63722#issuecomment-5195100359) **RyanCavanaugh** said "Copyediting for correctness in lib.d.ts is fine"
 * (today) **RyanCavanaugh** added label `Help Wanted`, and set milestone to `Backlog`

### [PR microsoft/TypeScript#63723](https://github.com/microsoft/TypeScript/pull/63723) (Closed, `For Backlog Bug`)

**Fix string detection across regex class union operands**

*Accumulate string detection across regex class union operands, report TS1518 for negated Unicode sets, and add related tests.*

 * created by **goutamadwant**
 * (today) **typescript-automation[bot]** added labels `For Backlog Bug`, `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63723#issuecomment-5200212249) **goutamadwant** agreed with microsoft-github-policy-service
 * [later](https://github.com/microsoft/TypeScript/pull/63723#issuecomment-5201508996) **MartinJohns** directed the user to read the contributing guidelines and explained that only critical 6.0 fixes in the typescript-go repo would be merged

### [Issue microsoft/TypeScript#63724](https://github.com/microsoft/TypeScript/issues/63724) (Open, `Bug`, `Help Wanted`)

**Type narrowing not working correctly with Uppercase\<string\> & Lowercase\<string\>**

*TypeScript cannot narrow Uppercase<string> or Lowercase<string> to specific string literal unions after equality checks, causing assignment errors.*

 * created by **wartab**
 * [later](https://github.com/microsoft/TypeScript/issues/63724#issuecomment-5203818351) **alex-vukov** explained that the error arose because Uppercase<string> cannot be narrowed to the specific union type and removing the cast resolves it
 * [later](https://github.com/microsoft/TypeScript/issues/63724#issuecomment-5204072640) **wartab** observed inconsistent type narrowing with Uppercase<string> and concluded it was a bug
 * [later](https://github.com/microsoft/TypeScript/issues/63724#issuecomment-5204340986) **alex-vukov** explained that using the `satisfies Uppercase<string>` check performed a single uppercase validation on each string literal, making it more efficient than parsing each union member’s casing separately
 * [later](https://github.com/microsoft/TypeScript/issues/63724#issuecomment-5204420107) **MartinJohns** said "The actual issue is that the compiler can't narrow down Uppercase to Uppercase when comparing to such a string. I don't know if there's an open issue for this specifically."
 * [later](https://github.com/microsoft/TypeScript/issues/63724#issuecomment-5205037210) **jcalz** described that Uppercase<string> could not be narrowed via equality check and demonstrated a user-defined type guard as a workaround

### [Issue microsoft/TypeScript#63725](https://github.com/microsoft/TypeScript/issues/63725) (Open)

**Type argument with a subset of the parameter constraint's optional keys incorrectly reported as unassignable to constraint**

*TypeScript reports an incorrect constraint error when a mapped type uses an optional subset of keys from keyof T.*

 * created by **aweebit**
 * [later](https://github.com/microsoft/TypeScript/issues/63725#issuecomment-5205092689) **aweebit** described a serious bug affecting a library and provided a minimal reproducible example

### [Issue microsoft/TypeScript#63726](https://github.com/microsoft/TypeScript/issues/63726) (Open)

**Poorly formed output with JSDoc typedef**

*JSDoc typedef output includes embedded asterisks, producing malformed TypeScript declaration files.*

 * created by **brettz9**

