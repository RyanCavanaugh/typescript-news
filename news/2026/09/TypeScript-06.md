# Report for 2026-09-06 (Sunday, September 6th, 2026)

11 different users commented on 33 different issues.

## Recommended Actions

 * Response Recommended
    * @vikr01 asked what could be done to get the feature change accepted in [microsoft/TypeScript#54022](https://github.com/microsoft/TypeScript/issues/54022#issuecomment-5562408015)
    * @devanshj asked for maintainer thoughts on the likelihood of this change landing in [microsoft/TypeScript#64091](https://github.com/microsoft/TypeScript/issues/64091#issuecomment-5567890699)
    * @remcohaszing provided repro steps in [microsoft/TypeScript#64182](https://github.com/microsoft/TypeScript/issues/64182#issuecomment-5567326791)

## Activity Summary

### [Issue microsoft/TypeScript#42905](https://github.com/microsoft/TypeScript/issues/42905) (Closed, `Bug`, `Fixed`, `Domain: Declaration Emit`, `Has Repro`, `Needs Human Review`)

**Broken emit when \`Infinity\` or \`‑Infinity\` ends up in a type position**

*TypeScript erroneously emits Infinity and -Infinity in type positions, producing invalid declaration files.*

 * [2.7 years ago](https://github.com/microsoft/TypeScript/issues/42905#issuecomment-1838026465) **typescript-bot** reported that the repro encountered a TS5107 deprecation error for moduleResolution=node10
 * [1.5 years ago](https://github.com/microsoft/TypeScript/issues/42905#issuecomment-2697046345) **lionel-rowe** questioned whether emitting `1e999` or another literal representing infinity would preserve the original type better than emitting `number`
 * **RyanCavanaugh** added label `Domain: Declaration Emit`
 * [today](https://github.com/microsoft/TypeScript/issues/42905#issuecomment-5560448347) **RyanCavanaugh** reported that current native TypeScript 7.1.0-dev.20260906.1 fixed the declaration emission issue by preserving large exponent values
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#43061](https://github.com/microsoft/TypeScript/issues/43061) (Closed, `Bug`, `Fixed`, `Help Wanted`, `Domain: tsc -b`, `Needs Human Review`)

**tsc fails with TypeError when I specify rootDirs:null with composite:true in an extended tsconfig**

*Specifying rootDirs:null in an extended tsconfig with composite:true causes tsc to throw a TypeError.*

 * (5.5 years ago) **RyanCavanaugh** added labels `help wanted`, `Domain: tsc -b`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/43061#issuecomment-5560775877) **RyanCavanaugh** noted that the crash no longer occurred in versions 4.3.0-dev.20210417, TypeScript 6.0.3, and the current native compiler after fix #43695
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#43120](https://github.com/microsoft/TypeScript/issues/43120) (Closed, `Bug`, `Help Wanted`, `Domain: tsc -b`, `Needs Human Review`)

**TypeScript 4\.2 caches cwd between builds when using the programatic api **

*Using the TypeScript 4.2 programmatic API caches the current working directory between runs, leading to tsconfig.json not found errors.*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [5.5 years ago](https://github.com/microsoft/TypeScript/issues/43120#issuecomment-797734849) **sheetalkamat** clarified that it was not a bug and explained host behavior allowing method overrides, referring to issue #43158
 * **RyanCavanaugh** added label `Domain: tsc -b`
 * [today](https://github.com/microsoft/TypeScript/issues/43120#issuecomment-5560886637) **RyanCavanaugh** advised creating the host with getCurrentDirectory bound to process.cwd instead of using the cached ts.sys current directory and noted the global reset/new-system API was declined and the pre-TypeScript-7 API is no longer developed
 * **RyanCavanaugh** added label `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#43362](https://github.com/microsoft/TypeScript/issues/43362) (Closed, `Bug`, `Fixed`, `Domain: JavaScript`, `Needs Human Review`)

**Can't use \`arguments\` property name within arrow function in JS**

*TypeScript incorrectly flags object properties named 'arguments' inside arrow functions as undefined references in JavaScript.*

 * [5.4 years ago](https://github.com/microsoft/TypeScript/issues/43362#issuecomment-806154713) **RyanCavanaugh** offered a workaround for the first issue by quoting 'arguments' and explained that 'arguments' isn't a legal strict-mode identifier, making it a corner case
 * [5.4 years ago](https://github.com/microsoft/TypeScript/issues/43362#issuecomment-806157781) **eyelidlessness** said "Thanks! I didn't know that about strict mode, I've edited the issue to remove that example so it doesn't confuse others."
 * **RyanCavanaugh** added label `Domain: JavaScript`
 * [today](https://github.com/microsoft/TypeScript/issues/43362#issuecomment-5562894975) **RyanCavanaugh** explained that the issue was fixed by PR #45814 and listed affected and fixed versions and commits
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#43395](https://github.com/microsoft/TypeScript/issues/43395) (Closed, `Bug`, `Fixed`, `Domain: check: Type Inference`, `Needs Human Review`)

**Error on named property assignment on nested function object**

*TypeScript errors when assigning a named property to a nested function unless a previous non-named property assignment exists.*

 * (5.4 years ago) **RyanCavanaugh** added labels `Bug`, `Domain: Type Inference`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/43395#issuecomment-5563154664) **RyanCavanaugh** noted that the issue was fixed in PR #54726 and that nested literal computed assignments reported errors through 5.2.0-dev.20230720 but compiled starting in 5.2.0-dev.20230721
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#43429](https://github.com/microsoft/TypeScript/issues/43429) (Closed, `Bug`, `Domain: check: Type Inference`, `Needs Human Review`)

**Spread Tuple Union In Function Errors**

*Spreading a union of fixed-length tuples into function parameters incorrectly triggers a TypeScript error by treating the tuple as empty.*

 * (5.4 years ago) **RyanCavanaugh** added label `Domain: Type Inference`, and set milestone to `Backlog`
 * [14 weeks ago](https://github.com/microsoft/TypeScript/issues/43429#issuecomment-4583036195) **jacekkopecky** demonstrated a simpler reproduction where a union of constant tuples was not recognized as a tuple type and triggered a spread argument error
 * [today](https://github.com/microsoft/TypeScript/issues/43429#issuecomment-5563324448) **RyanCavanaugh** marked the issue as a duplicate of #42508 regarding tuple union spreading causing TS2556
 * **RyanCavanaugh** added label `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#43458](https://github.com/microsoft/TypeScript/issues/43458) (Closed, `Bug`, `Fixed`, `Domain: check: Control Flow`, `Needs Human Review`)

**Multiple cases inside of a switch statement not narrowing the type**

*TypeScript does not narrow types in switch statements for multiple fall-through cases unless they are listed first.*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [3.9 years ago](https://github.com/microsoft/TypeScript/issues/43458#issuecomment-1278059770) **mhluongo** said "Any progress here? Small but unfortunate bug for heavy union users"
 * **RyanCavanaugh** added label `Domain: Control Flow`
 * [today](https://github.com/microsoft/TypeScript/issues/43458#issuecomment-5563398297) **RyanCavanaugh** reported that the issue was fixed in 5.4.0-dev.20231114 and current native TypeScript thanks to PR #56358, noting that earlier dev versions 4.3.0-dev.20210331 and 5.4.0-dev.20231113 had produced TS2339 errors
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#43613](https://github.com/microsoft/TypeScript/issues/43613) (Open, `Bug`, `Domain: This-Typing`, `Needs Human Review`)

**Interface definition utilizing \`this\` type errors out only in specific cases and only when a member is accessed, not before**

*TypeScript regression emits erroneous circular-reference errors for interfaces using the this type in intersection types only upon member access.*

 * (5.4 years ago) **andrewbranch** added label `Bug`, and set milestone to `Backlog`
 * **RyanCavanaugh** added label `Domain: This-Typing`
 * [today](https://github.com/microsoft/TypeScript/issues/43613#issuecomment-5563517615) **RyanCavanaugh** explained that intersection['a'] triggered a circular type-checking path through foo<string> & foo<number>, causing TS2502 errors to appear depending on checking and caching order, and noted that related this-type intersection behavior was covered by issues #40928 and #40967
 * **RyanCavanaugh** added label `Needs Human Review`

### [Issue microsoft/TypeScript#43779](https://github.com/microsoft/TypeScript/issues/43779) (Closed, `Bug`, `Fixed`, `Domain: JSDoc`, `Needs Human Review`)

**One duplicate error message for each jsdoc comment**

*Syntax errors for unfinished arrow functions are duplicated for each JSDoc comment block.*

 * (5.3 years ago) **RyanCavanaugh** added labels `Bug`, `Domain: JSDoc`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/43779#issuecomment-5565016069) **RyanCavanaugh** described that the unfinished arrow diagnostic issue was fixed in 4.3.0-dev.20210422, that 5.0.0-dev.20221209 and later builds report only two parser diagnostics after merging PR #51594, and noted current releases behave correctly
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#43869](https://github.com/microsoft/TypeScript/issues/43869) (Closed, `Bug`, `Fixed`, `Effort: Moderate`, `Domain: JSDoc`, `Rescheduled`, `Needs Human Review`, **orta**)

**JSDoc @link not resolved across modules**

*JSDoc @link tags referencing imported classes across modules fail to resolve as clickable links.*

 * (2.1 years ago) **RyanCavanaugh** added label `Domain: JSDoc`, and set milestone to `TypeScript 5.7.0`
 * [29 weeks ago](https://github.com/microsoft/TypeScript/issues/43869#issuecomment-3892252160) **nikelborm** reported facing the same problem and shared a workaround by explicitly exporting referenced local types, and described unsuccessful import type and export type approaches
 * [today](https://github.com/microsoft/TypeScript/issues/43869#issuecomment-5565653831) **RyanCavanaugh** explained that the TS6133 error was caused by noUnusedLocals and was fixed by PR #47822, noting that recent dev builds no longer report it
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#43894](https://github.com/microsoft/TypeScript/issues/43894) (Closed, `Bug`, `Fixed`, `Domain: JSDoc`, `Rescheduled`, `Needs Human Review`, **sandersn**)

**JSDoc can't reference global\-injected types declared in an ES module**

*JSDoc fails to recognize globally injected ES module namespace types, requiring verbose InstanceType annotations.*

 * **RyanCavanaugh** added to milestone `TypeScript 5.7.0`
 * [2 years ago](https://github.com/microsoft/TypeScript/issues/43894#issuecomment-2308211008) **sisou** reported the issue only occurred with TS v5.5 and asked how to make their namespace type annotation work without wrapping types in InstanceType
 * **RyanCavanaugh** added label `Domain: JSDoc`
 * [today](https://github.com/microsoft/TypeScript/issues/43894#issuecomment-5566047892) **RyanCavanaugh** clarified that TypeScript now resolves Types.ClassOne in Quick Info and that PR 21974 originated the namespace lookup rule, not the fix
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#44005](https://github.com/microsoft/TypeScript/issues/44005) (Closed, `Bug`, `Domain: Comment Emit`, `Needs Human Review`)

**Comments leak into transformer\-syntesized lists\.**

*Trailing comments are misattached to elements inside synthesized comma lists in transformer-generated AST nodes.*

 * [5.3 years ago](https://github.com/microsoft/TypeScript/issues/44005#issuecomment-836969082) **RyanCavanaugh** said "Feel free to put up a PR and we can assess what's going on. Seems bad 🙂"
 * [5.2 years ago](https://github.com/microsoft/TypeScript/issues/44005#issuecomment-847547402) **andrew-z** reported that after upgrading to 4.2.4 trailing comments on the last array elements leaked into the generated JavaScript output
 * **RyanCavanaugh** added label `Domain: Comment Emit`
 * [later](https://github.com/microsoft/TypeScript/issues/44005#issuecomment-5567393384) **RyanCavanaugh** explained that the behavior was in the obsolete pre-TypeScript-7 JavaScript Compiler API, noted that a proposed change was closed unmerged due to regressions, and stated that the issue cannot be completed on that API surface
 * **RyanCavanaugh** added label `Needs Human Review`
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#44191](https://github.com/microsoft/TypeScript/issues/44191) (Closed, `Bug`, `Fixed`, `Help Wanted`, `Domain: lib.d.ts`, `Needs Human Review`)

**Update \`TypedArray\` constructors to disallow invalid \`\(typedArray, byteOffset, byteLength\)\`**

*Correct TypeScript’s TypedArray constructor definitions to forbid specifying byteOffset and byteLength when constructing from another TypedArray.*

 * **RyanCavanaugh** added to milestone `Backlog`
 * **typescript-bot** added label `Fix Available`
 * **jakebailey** removed label `Fix Available`
 * [later](https://github.com/microsoft/TypeScript/issues/44191#issuecomment-5567688126) **RyanCavanaugh** described that the constructor call was rejected with TS2769 in TypeScript 6.0.3 and 7.1.0-dev because the overload requires an ArrayBuffer or ArrayBufferLike, whereas TypeScript 4.3.2 previously accepted it ignoring offset and length arguments
 * (later) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#44245](https://github.com/microsoft/TypeScript/issues/44245) (Closed, `Bug`, `Help Wanted`, `Domain: lib.d.ts`, `Needs Human Review`)

**URL interface is not part of the Window object**

*Window interface in TypeScript lacks URL definitions, causing window.URL to remain undefined.*

 * (5.2 years ago) **RyanCavanaugh** added labels `Domain: lib.d.ts`, `help wanted`, and set milestone to `Backlog`
 * [later](https://github.com/microsoft/TypeScript/issues/44245#issuecomment-5567850843) **RyanCavanaugh** explained that Window['URL'] versus global window.URL behavior stemmed from global declarations and suggested typing injected window-like values as Window & typeof globalThis to access global constructors such as URL
 * **RyanCavanaugh** added label `Needs Human Review`
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#44289](https://github.com/microsoft/TypeScript/issues/44289) (Closed, `Bug`, `Domain: Module Resolution`, `Needs Human Review`)

**Plugin module resolve should respect yarn link**

*TypeScript plugin module resolution ignores Yarn links and fails to load linked plugin packages.*

 * (5.2 years ago) **RyanCavanaugh** added labels `Bug`, `Domain: Module Resolution`, and set milestone to `Backlog`
 * [later](https://github.com/microsoft/TypeScript/issues/44289#issuecomment-5567971271) **RyanCavanaugh** stated that classic tsserver server plugins are no longer supported in TypeScript 7 and that the yarn-linked plugin-resolution behavior falls under that deprecated API and is therefore not actionable
 * **RyanCavanaugh** added label `Needs Human Review`
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#44333](https://github.com/microsoft/TypeScript/issues/44333) (Closed, `Bug`, `Fixed`, `Domain: check: Control Flow`, `Needs Human Review`)

**Symbol in object not treated as a narrowing type guard**

*TypeScript fails to narrow union types when using the in operator with symbol keys, unlike string keys.*

 * [5.2 years ago](https://github.com/microsoft/TypeScript/issues/44333#issuecomment-857920591) **RyanCavanaugh** called it a bug and noted the need to write const symb: unique symbol = Symbol()
 * [5.2 years ago](https://github.com/microsoft/TypeScript/issues/44333#issuecomment-860160923) **pushkine** described that narrowing using the in operator didn't work with identifiers even for const string literals
 * **RyanCavanaugh** added label `Domain: Control Flow`
 * [later](https://github.com/microsoft/TypeScript/issues/44333#issuecomment-5568171343) **RyanCavanaugh** noted `in`-operator narrowing for symbol and numeric keys was fixed in the 4.9.0-dev.20220920 build by PR #50666
 * (later) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#44334](https://github.com/microsoft/TypeScript/issues/44334) (Open, `Bug`, `Needs More Info`, `Domain: lib.d.ts`, `Needs Human Review`)

**Breaking change 4\.3 RC: TS2488: Build:Type 'SomeArrayType' must have a '\[Symbol\.iterator\]\(\)' method that returns an iterator\.**

*TypeScript 4.3 RC incorrectly errors TS2488 on array spread when SymbolConstructor is moved to a custom namespace.*

 * (5.2 years ago) **RyanCavanaugh** added labels `Bug`, `Domain: lib.d.ts`, and set milestone to `Backlog`
 * [later](https://github.com/microsoft/TypeScript/issues/44334#issuecomment-5568399979) **RyanCavanaugh** requested the complete custom library and build configuration to reproduce the TS2488 issue
 * (later) **RyanCavanaugh** added labels `Needs Human Review`, `Needs More Info`

### [Issue microsoft/TypeScript#44975](https://github.com/microsoft/TypeScript/issues/44975) (Open, `Bug`, `Domain: Conditional Types`, `Needs Human Review`)

**Two way assignability condition with generic params is not working as expected**

*A TypeScript conditional type that should resolve to number for two identical generic parameters incorrectly rejects numeric assignments.*

 * (5.1 years ago) **RyanCavanaugh** added labels `Bug`, `Domain: Conditional Types`, and set milestone to `Backlog`
 * [later](https://github.com/microsoft/TypeScript/issues/44975#issuecomment-5571254663) **RyanCavanaugh** explained that equal generic arguments did not make nested distributive conditional types universally number, illustrated with NumberIfExtends examples, noted alias assignment rejection across TypeScript versions, and linked to relevant documentation
 * **RyanCavanaugh** added label `Needs Human Review`

### [Issue microsoft/TypeScript#54022](https://github.com/microsoft/TypeScript/issues/54022) (Open, `Suggestion`, `Awaiting More Feedback`)

**Add an intrinsic "module reference" types that allow definition of type\-checked module path strings and return types**

*Add an intrinsic module reference type for type-checking module path strings and their return types in TypeScript*

 * (3.2 years ago) **RyanCavanaugh** added labels `Suggestion`, `Awaiting More Feedback`
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/54022#issuecomment-5536210336) **LeonxLJX** offered to implement an intrinsic ModuleReference type, explained the design gap around treating module specifiers as opaque strings, outlined alternative approaches, and asked whether the type should be callable or support dynamic-import propagation
 * [today](https://github.com/microsoft/TypeScript/issues/54022#issuecomment-5562408015) **vikr01** asked what could be done to get the feature change accepted and suggested a plugin architecture

### [Issue microsoft/TypeScript#61713](https://github.com/microsoft/TypeScript/issues/61713) (Closed, `Bug`, `Help Wanted`, `Domain: lib.d.ts`)

**Missing Intl\.Locale\.prototype\.getWeekInfo\(\)**

*Intl.Locale.prototype.getWeekInfo is absent from ESNext's type definitions despite being supported in major browsers and Node.js.*

 * [1.3 years ago](https://github.com/microsoft/TypeScript/issues/61713#issuecomment-2888467031) **wlib** said "There's also this related PR that's been on hold https://github.com/microsoft/TypeScript/pull/58084"
 * [1 year ago](https://github.com/microsoft/TypeScript/issues/61713#issuecomment-3234065303) **mauroviniciussilva** said "Any updates on this issue or in the related pull request? As I've seen, the latest update on the mentioned pull request is from 2024."
 * [38 weeks ago](https://github.com/microsoft/TypeScript/issues/61713#issuecomment-3641060663) **json-derulo** noted that Firefox did not support the function and provided a link to the issue tracker
 * [later](https://github.com/microsoft/TypeScript/issues/61713#issuecomment-5569377698) **HolgerJeromin** mentioned that the API was included in TS7 under the ESNext.Intl library
 * (later) **jakebailey** closed the issue

### [PR microsoft/TypeScript#63591](https://github.com/microsoft/TypeScript/pull/63591) (Closed, `For Backlog Bug`)

**lib\(esnext\.intl\): add missing minimalDays to WeekInfo interface**

*Include the minimalDays property in the WeekInfo interface of the esnext.intl TypeScript lib definitions.*

 * created by **smedavarapu1**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/63591#issuecomment-5569514494) **HolgerJeromin** noted that minimalDays was no longer part of the API, that the referenced bug didn’t cover this property and was resolved with TypeScript 7, and recommended closing the PR
 * (later) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#63979](https://github.com/microsoft/TypeScript/issues/63979) (Closed, `Out of Scope`, `Docs`)

**Official guidelines to build complex types**

*Proposal to add official TypeScript guidelines detailing supported tips, patterns, and pitfalls for constructing complex type definitions.*

 * [1 week ago](https://github.com/microsoft/TypeScript/issues/63979#issuecomment-5448739708) **denis-migdal** critiqued the bot’s two-day response window as too short and explained being busy
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/63979#issuecomment-5456795894) **MartinJohns** said "The issue is not locked. You can still take your time and comment later."
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/63979#issuecomment-5457409158) **RyanCavanaugh** said "Regardless, the scope of the project is not really something you're going to change by commenting on an issue whether it's closed or open"
 * [today](https://github.com/microsoft/TypeScript/issues/63979#issuecomment-5566337634) **denis-migdal** proposed collecting TypeScript tips and suggested using interfaces instead of concrete types, defining capacity-based interfaces, and employing symbols to hide internal data

### [Issue microsoft/TypeScript#64091](https://github.com/microsoft/TypeScript/issues/64091) (Open, `Suggestion`)

**Feature request: Dependent contextual inference**

*Enable dependent contextual inference in TypeScript to iteratively refine generic type arguments in self-referencing functions until convergence.*

 * created by **devanshj**
 * **RyanCavanaugh** added label `Suggestion`
 * [later](https://github.com/microsoft/TypeScript/issues/64091#issuecomment-5567890699) **devanshj** said "@RyanCavanaugh Can I get your thoughts on this? I'd like to know the likelihood of this ever landing (so that I know if I should invest on building on top of this or not)... Thanks for your time!"

### [Issue microsoft/TypeScript#64136](https://github.com/microsoft/TypeScript/issues/64136) (Closed, `Not a Defect`)

**Regression to \#35004**

*Assertion functions fail with wildcard destructuring imports after upgrading to TypeScript 7, triggering TS2775 errors.*

 * [3 days ago](https://github.com/microsoft/TypeScript/issues/64136#issuecomment-5525601715) **jcalz** explained that assertion functions require explicit type annotations and that destructuring assignment cannot support them, and suggested framing a feature request as 'allow destructuring assignment of assertion functions'
 * **RyanCavanaugh** added label `Not a Defect`
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/64136#issuecomment-5543397736) **RyanCavanaugh** provided a minimal reproduction and stated that the error TS2775 is expected and not a bug or regression
 * [today](https://github.com/microsoft/TypeScript/issues/64136#issuecomment-5563737594) **typescript-automation[bot]** said "This issue has been marked as "Not a Defect" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-automation[bot]** closed the issue

### [Issue microsoft/TypeScript#64182](https://github.com/microsoft/TypeScript/issues/64182) (Open, `Domain: Content Mappers`, **andrewbranch**)

**Allow content\-mappers to return declarations instead of source files**

*Allow TypeScript content mappers to return declaration files (.d.ts, .d.cts, .d.mts) instead of source files to bypass module syntax restrictions.*

 * created by **remcohaszing**
 * [later](https://github.com/microsoft/TypeScript/issues/64182#issuecomment-5567326791) **remcohaszing** explained that TypeScript allowed CJS syntax in .cts files with module=esnext but the content-mapper treated them as .ts and provided a reproduction link

### [PR microsoft/TypeScript#64183](https://github.com/microsoft/TypeScript/pull/64183) (Open, `For Backlog Bug`)

**fix\(auto\-import\): don't suggest module specifiers under shadowed export/import conditions**

*Prevent auto-import from suggesting module specifiers from later conditional export or import entries once an earlier runtime condition applies.*

 * created by **erantianantha**
 * (today) **typescript-automation[bot]** added labels `For Backlog Bug`, `For Backlog Bug`

### [PR microsoft/TypeScript#64184](https://github.com/microsoft/TypeScript/pull/64184) (Open, `For Uncommitted Bug`, **andrewbranch**)

**Fix RefCountCache\.Ref panic race between concurrent snapshot builds**

*Concurrent snapshot building in the TypeScript language server can cause RefCountCache.Ref to panic due to a cache entry race condition.*

 * created by **NAVEENKUMARKR777**
 * (today) **typescript-automation[bot]** added label `For Uncommitted Bug`, and assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript/pull/64184#issuecomment-5563109701) **NAVEENKUMARKR777** said "@microsoft-github-policy-service agree"

### [Issue microsoft/TypeScript#64185](https://github.com/microsoft/TypeScript/issues/64185) (Open)

**Parenthesized computed method names change import\-alias resolution and emitted JavaScript after namespace merging**

*Parenthesizing a computed static method name leads to import alias removal and incorrect emitted JavaScript behavior.*

 * created by **magic-akari**

### [Issue microsoft/TypeScript#64186](https://github.com/microsoft/TypeScript/issues/64186) (Open)

**Narrowing of generic this is inconsistent with variable narrowing**

*TypeScript narrows generic this types inconsistently compared to generic parameters, resulting in unexpected union narrowing behavior.*

 * created by **Andarist**

### [PR microsoft/TypeScript#64187](https://github.com/microsoft/TypeScript/pull/64187) (Open, `For Uncommitted Bug`)

**Fix narrowing of generic this parameters**

*Fix incorrect narrowing of generic this parameters to restore expected type inference behavior.*

 * created by **Andarist**
 * (later) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`

### [PR microsoft/TypeScript#64188](https://github.com/microsoft/TypeScript/pull/64188) (Open, `For Uncommitted Bug`)

**Skip object classification for shared type facts**

*Skip object classification checks for shared type facts to reduce redundant isEmptyObjectType and isFunctionObjectType calls.*

 * created by **Andarist**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/64188#issuecomment-5568531975) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."

