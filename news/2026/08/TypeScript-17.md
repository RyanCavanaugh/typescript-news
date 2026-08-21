# Report for 2026-08-17 (Monday, August 17th, 2026)

11 different users commented on 27 different issues.

## Recommended Actions

 * Response Recommended
    * @snarbles2 asked why a feature should be removed in [microsoft/TypeScript#31670](https://github.com/microsoft/TypeScript/issues/31670#issuecomment-5319453797)
    * @rjgotten asked why there's a flag for banning `private` but not for other syntactic features such as `any` in [microsoft/TypeScript#31670](https://github.com/microsoft/TypeScript/issues/31670#issuecomment-5319919020)
    * @Arashiryuu provided repro steps as requested in [microsoft/TypeScript#63754](https://github.com/microsoft/TypeScript/issues/63754#issuecomment-5327648214)
    * @bun-unsafe requested applying the existing contextual-`this` rule to generator function expressions in [microsoft/TypeScript#63755](https://github.com/microsoft/TypeScript/issues/63755#issuecomment-5324016464)
    * @Pomax asked why the issue was closed as 'not planned' and why the README pointed to the wrong repository in [microsoft/TypeScript#63756](https://github.com/microsoft/TypeScript/issues/63756#issuecomment-5330372426)

## Activity Summary

### [Issue microsoft/TypeScript#10564](https://github.com/microsoft/TypeScript/issues/10564) (Closed, `Bug`, `Help Wanted`, `Effort: Moderate`, `Domain: check: Control Flow`)

**Strange boolean\-discriminant narrowing with strictNullChecks off**

*Using if(res.success) fails to narrow the union type correctly unlike explicit comparisons to true or false.*

 * **sandersn** unassigned **sandersn**
 * [6 years ago](https://github.com/microsoft/TypeScript/issues/10564#issuecomment-663879330) **Tanja-4732** provided a workaround using a switch statement to access an optional property in a discriminated union
 * **RyanCavanaugh** added label `Domain: Control Flow`
 * [today](https://github.com/microsoft/TypeScript/issues/10564#issuecomment-5323619714) **RyanCavanaugh** said "This now works as expected"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#11243](https://github.com/microsoft/TypeScript/issues/11243) (Closed, `Bug`, `Domain: Binder`)

**Ambient class augmentation with export =**

*Augmenting an ambient module declared with export = causes a TS2309 error when adding interface declarations.*

 * **mhegazy** removed from milestone `TypeScript 2.1`
 * [8.2 years ago](https://github.com/microsoft/TypeScript/issues/11243#issuecomment-394424822) **nevir** said "Also running into this one when trying to break typings for a large library into multiple files for better organization :("
 * **RyanCavanaugh** added label `Domain: Binder`
 * [today](https://github.com/microsoft/TypeScript/issues/11243#issuecomment-5323635972) **RyanCavanaugh** said "This no longer errors"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#31670](https://github.com/microsoft/TypeScript/issues/31670) (Closed, `Discussion`)

**The future of the "private" keyword**

*Discussion of TypeScript’s plan to retain its existing private keyword while supporting new JavaScript private fields (#fields) and associated rules.*

 * [21 weeks ago](https://github.com/microsoft/TypeScript/issues/31670#issuecomment-4088397826) **Finesse** asked about using a TypeScript flag to prepend '#' to private fields for minification benefits and inquired why const enum emit is allowed
 * [21 weeks ago](https://github.com/microsoft/TypeScript/issues/31670#issuecomment-4090013416) **snarbles2** explained that transpiling private to # is not simple due to semantic differences, backward-compatibility concerns, and potential confusion, and clarified that const enums are permitted because they are grandfathered from before TypeScript's type-directed emit stance
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/31670#issuecomment-5299225184) **irfanstract** warned that the private visibility modifier can be dangerous and suggested migrating to ES Private Fields; asked why const enum is allowed, speculating that some transpilers might drop const
 * [today](https://github.com/microsoft/TypeScript/issues/31670#issuecomment-5318213437) **RyanCavanaugh** said "You can add a lint rule if you don't want to use private. We're not going to break huge amounts of code for a "warning" that doesn't do anything."
 * [today](https://github.com/microsoft/TypeScript/issues/31670#issuecomment-5318341442) **ljharb** said "What about a tsconfig option that removes it entirely?"
 * [today](https://github.com/microsoft/TypeScript/issues/31670#issuecomment-5319453797) **snarbles2** questioned why it should be removed and stated its semantics remain useful
 * [today](https://github.com/microsoft/TypeScript/issues/31670#issuecomment-5319867982) **RyanCavanaugh** said "Why have a flag for banning private vs any other syntactic feature you might not like? I don't get the distinction"
 * [today](https://github.com/microsoft/TypeScript/issues/31670#issuecomment-5319919020) **rjgotten** asked why a flag for banning private exists but not for any and argued private causes more real-world harm than any
 * [today](https://github.com/microsoft/TypeScript/issues/31670#issuecomment-5320459312) **ljharb** argued that banning a type-space syntax differed qualitatively from banning a non-standard value-space syntax with false encapsulation and that the proposed `private` keyword offered no practical benefits over existing JavaScript patterns
 * [later](https://github.com/microsoft/TypeScript/issues/31670#issuecomment-5327867983) **snarbles2** pointed out that TypeScript's private has capabilities unavailable to #private and suggested using a linter
 * [later](https://github.com/microsoft/TypeScript/issues/31670#issuecomment-5328307514) **mbrowne** suggested marking the private keyword as deprecated in the official docs due to its non-standard status and availability of native alternatives

### [Issue microsoft/TypeScript#3715](https://github.com/microsoft/TypeScript/issues/3715) (Closed, `Bug`, `ES6`, `Domain: JS Emit`)

**Down\-level destructuring in \`for\.\.in\` statement**

*Support and correctly transpile destructured variable declarations in for..in loops by emitting a temporary variable and separate assignment.*

 * **RyanCavanaugh** unassigned **yuit**
 * [2.4 years ago](https://github.com/microsoft/TypeScript/issues/3715#issuecomment-1961969996) **RyanCavanaugh** suggested simplifying by keeping it an error when downleveling to avoid ballooning the ES5 transform
 * **RyanCavanaugh** added label `Domain: JS Emit`
 * [today](https://github.com/microsoft/TypeScript/issues/3715#issuecomment-5323612195) **RyanCavanaugh** said "This is moot due to ES5 deprecation"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63092](https://github.com/microsoft/TypeScript/issues/63092) (Closed, `Bug`, `Help Wanted`, `Domain: check: Control Flow`, **ahejlsberg**)

**Crash: RangeError: Maximum call stack size exceeded in isReachableFlowNodeWorker with complex for loop headers**

*TypeScript's compiler crashes with a maximum call stack size exceeded error when analyzing reachability in complex for loop headers.*

 * [9 weeks ago](https://github.com/microsoft/TypeScript/issues/63092#issuecomment-4663552465) **RyanCavanaugh** referred to the contributing guidelines and reminded the user to develop in the typescript-go repo because the bug didn't meet the 6.0 patch bar
 * [9 weeks ago](https://github.com/microsoft/TypeScript/issues/63092#issuecomment-4679263794) **ibesuperv** submitted a fix in the typescript-go repository and asked for review
 * [5 weeks ago](https://github.com/microsoft/TypeScript/issues/63092#issuecomment-4935118862) **ibesuperv** explained that they accidentally synced their fork’s main branch and force-pushed over their work, causing the PR to close, and opened a fresh PR with an improved fix addressing all prior feedback
 * **RyanCavanaugh** assigned to **ahejlsberg**
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript#63640](https://github.com/microsoft/TypeScript/issues/63640) (Closed, `Bug`, `Help Wanted`, `Domain: LS: Quick Info`)

**JSDoc for properties of intersected types is no longer merged**

*TypeScript 7.0.2 no longer merges JSDoc comments for identical properties in intersected types.*

 * (5 weeks ago) **RyanCavanaugh** added labels `Help Wanted`, `Domain: LS: Quick Info`, and set milestone to `Backlog`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#63682](https://github.com/microsoft/TypeScript/issues/63682) (Closed, `Bug`, `Help Wanted`, `Domain: Parser`)

**ES2025 regex syntax \(duplicate named groups, pattern modifiers\) is not gated by \`target\`**

*TypeScript does not enforce target-based errors for ES2025 regex features such as duplicate named groups and pattern modifiers.*

 * **RyanCavanaugh** added label `Help Wanted`
 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/63682#issuecomment-5116907655) **BhariGowda** described the root cause of the issue, endorsed the fix in #63689, suggested verifying the version gate covers both scanner-level and regex reuse paths, and recommended adding a test case for the specific regex reuse scenario to prevent regressions
 * **RyanCavanaugh** added label `Domain: Parser`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#63717](https://github.com/microsoft/TypeScript/pull/63717) (Closed, `For Uncommitted Bug`, `Voight-Kampff Anomaly`)

**Pin GitHub Actions to full\-length commit SHAs**

*Pin GitHub Actions workflows to immutable full-length commit SHAs and set a 7-day Dependabot cooldown for improved security and reproducibility.*

 * [1 week ago](https://github.com/microsoft/TypeScript/pull/63717#issuecomment-5181808795) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/63717#issuecomment-5181808821) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * **RyanCavanaugh** added label `Voight-Kampff Anomaly`
 * (later) **OssSecurityBot** closed the issue

### [Issue microsoft/TypeScript#63726](https://github.com/microsoft/TypeScript/issues/63726) (Closed, `Bug`, `Domain: JSDoc`, `Fix Available`, **sandersn**)

**Poorly formed output with JSDoc typedef**

*JSDoc typedef produces malformed TypeScript definitions embedding stray asterisks in the union type.*

 * **typescript-automation[bot]** added label `Fix Available`
 * (6 days ago) **RyanCavanaugh** added label `Domain: JSDoc`, and assigned to **sandersn**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#63742](https://github.com/microsoft/TypeScript/issues/63742) (Closed, `Needs More Info`)

**Rest\-parameter mapped\-type wrapping breaks tuple\-literal inference once real\-world complexity is added**

*The use of a rest-parameter mapped type to inject ThisType in jml’s signature prevents tuple literal inference in complex scenarios.*

 * **RyanCavanaugh** added label `Needs More Info`
 * [5 days ago](https://github.com/microsoft/TypeScript/issues/63742#issuecomment-5274662621) **brettz9** clarified that the $setStyles function should be available on sel and that this in $setStyles should be an HTMLSelectElement with a $setStyles method
 * [today](https://github.com/microsoft/TypeScript/issues/63742#issuecomment-5314222854) **Andarist** expressed interest in reverse mapped types and asked for a simplified example to assess the issue
 * [today](https://github.com/microsoft/TypeScript/issues/63742#issuecomment-5321128039) **brettz9** explained that further investigation revealed expected behavior and a code bug, fixed it, and closed the issue
 * (today) **brettz9** closed the issue

### [Issue microsoft/TypeScript#63747](https://github.com/microsoft/TypeScript/issues/63747) (Open, `Docs`)

**Update wiki "Using the Compiler API" for TypeScript v7**

*Update the Using the Compiler API wiki documentation to cover new types and patterns in TypeScript v7.*

 * **RyanCavanaugh** added to milestone `TypeScript 7.1`
 * **typescript-automation[bot]** added label `Fix Available`
 * [6 days ago](https://github.com/microsoft/TypeScript/issues/63747#issuecomment-5259820023) **RyanCavanaugh** said "I don't see how it's possible for someone external to have the necessary context on this. The API isn't even ready to be documented."
 * [today](https://github.com/microsoft/TypeScript/issues/63747#issuecomment-5318686105) **DanielRosenwasser** said "I've at least noted that 7.1 will have a very different API."

### [Issue microsoft/TypeScript#63752](https://github.com/microsoft/TypeScript/issues/63752) (Closed)

**extraFileExtensions cannot declare an extension as TypeScript, so TS\-flavoured files are charged to maxProgramSizeForNonTsFiles**

*extraFileExtensions files are not recognized as TypeScript and thus are measured against maxProgramSizeForNonTsFiles, disabling them when large*

 * created by **wagenet**
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63752#issuecomment-5299504677) **wagenet** explained a workaround shipping in the Ember parser that lies to ts.sys.getFileSize by reporting .gts files as zero bytes and stated a preference for extraFileExtensions
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63752#issuecomment-5300461978) **MartinJohns** noted that the suggested fix applied to nonexistent files and cautioned against trusting the AI given that TypeScript 5.7 is almost two years old
 * [today](https://github.com/microsoft/TypeScript/issues/63752#issuecomment-5318045351) **wagenet** apologized for suggesting an incorrect upstream fix and noted they hadn’t verified it and the issue was in their own app
 * (today) **wagenet** closed the issue

### [Issue microsoft/TypeScript#63753](https://github.com/microsoft/TypeScript/issues/63753) (Closed, `Docs`)

**TypeScript doesn't add "node" to "types" in compilerOptions, even though node\_modules/@types/node exists**

*TypeScript does not automatically include the @types/node definitions from node_modules, leading to ‘process’ not being recognized.*

 * created by **karl-police**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63753#issuecomment-5309998234) **MartinJohns** said "The documentation is outdated. See this: https://www.typescriptlang.org/docs/handbook/release-notes/typescript-6-0.html#types-now-defaults-to-"
 * (today) **RyanCavanaugh** added label `Docs`, and set milestone to `Backlog`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63754](https://github.com/microsoft/TypeScript/issues/63754) (Open, `Bug`)

**Diagnostic code 8030 being incorrectly generated using JSDoc \`@type\` on a function\.**

*TypeScript 7.0.2's JSDoc @type on a function wrongly triggers diagnostic 8030 by appending '| undefined' to the referenced interface method type.*

 * created by **Arashiryuu**
 * [today](https://github.com/microsoft/TypeScript/issues/63754#issuecomment-5321512243) **RyanCavanaugh** reported inability to reproduce the issue on the provided files and asked for a self-contained repro including Example visibility, method declaration, and tsconfig options
 * **RyanCavanaugh** added label `Needs More Info`
 * [later](https://github.com/microsoft/TypeScript/issues/63754#issuecomment-5327648214) **Arashiryuu** provided reproduction steps with tsconfig and code demonstrating incorrect hover type info for an optional method in TS 7.0.2

### [Issue microsoft/TypeScript#63755](https://github.com/microsoft/TypeScript/issues/63755) (Closed, `Suggestion`, `Awaiting More Feedback`)

**Contextually type \`this\` inside \`function\*\` from a leading thisArg**

*Implement contextual this typing for generator function expressions based on a leading thisArg to infer the enclosing instance type.*

 * created by **bun-unsafe**
 * (today) **RyanCavanaugh** added labels `Suggestion`, `Awaiting More Feedback`
 * [today](https://github.com/microsoft/TypeScript/issues/63755#issuecomment-5320745088) **RyanCavanaugh** said "I'm a little surprised this doesn't work already. If it's a ~one-line fix we should just do it; maybe there were unforeseen complications originally"
 * [today](https://github.com/microsoft/TypeScript/issues/63755#issuecomment-5324016464) **bun-unsafe** clarified that contextual `this` works for plain functions but not for generator functions and requested applying the existing contextual-`this` rule to function* expressions

### [Issue microsoft/TypeScript#63756](https://github.com/microsoft/TypeScript/issues/63756) (Closed)

**There are no 7\.x branches or tags**

*NPM lists 7.x releases for the package but the repository contains no corresponding 7.x branches, tags, or source code.*

 * created by **Pomax**
 * [today](https://github.com/microsoft/TypeScript/issues/63756#issuecomment-5320506353) **RyanCavanaugh** said "7.0 development was staged at https://github.com/microsoft/TypeScript-go and is moving back into this repo."
 * (today) **RyanCavanaugh** closed the issue
 * [later](https://github.com/microsoft/TypeScript/issues/63756#issuecomment-5330372426) **Pomax** questioned why the issue was closed as not planned, pointed out that the README linked to the wrong repository, and stated that the current 7.x release was untrustworthy due to a bungled process

### [Issue microsoft/TypeScript#63889](https://github.com/microsoft/TypeScript/issues/63889) (Open, `Needs Investigation`, **johnfav03**)

**\[ServerErrors\]\[TypeScript\] main vs **

*The TypeScript main branch pipeline analyzed 300 popular GitHub repositories, reporting 29 detected changes, 147 no-changes, and several clone, timeout, and unknown failures.*

 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63889#issuecomment-5351511112) **typescript-automation[bot]** reported a panic in the textDocument/diagnostic handler with stack trace for makeplane/plane
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63889#issuecomment-5351511148) **typescript-automation[bot]** reported a panic due to invalid memory address or nil pointer dereference with stack trace
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63889#issuecomment-5351511171) **typescript-automation[bot]** reported a panic during a textDocument/diagnostic request, including a stack trace and details for pubkey/rxdb
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **johnfav03**

