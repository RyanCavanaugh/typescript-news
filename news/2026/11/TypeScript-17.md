# Report for 2026-11-17 (Tuesday, November 17th, 2026)

12 different users commented on 132 different issues.

## Recommended Actions

 * Response Recommended
    * @Sipixer provided reproduction details and regression impact for the related `@tanstack/db` typing issue in [microsoft/TypeScript#64930](https://github.com/microsoft/TypeScript/issues/64930#issuecomment-6982595670)
    * @zhengdaodeguL reported an important checker crash fix and included regression-test coverage in [microsoft/TypeScript#65452](https://github.com/microsoft/TypeScript/issues/65452#issuecomment-6981493723)

## Activity Summary

### [Issue microsoft/TypeScript#17873](https://github.com/microsoft/TypeScript/issues/17873) (Open, `Bug`, `Domain: check: Type Inference`, `Has Repro`, `Domain: check: Order Dependence`)

**Error inferring types of promise function**

*TypeScript fails to infer generic types for a promise-based function involving ES6 Maps, incorrectly rejecting a valid assignment.*

 * **typescript-bot** added label `Has Repro`
 * [2.6 years ago](https://github.com/microsoft/TypeScript/issues/17873#issuecomment-1987830128) **typescript-bot** reported that the repro failed on nightly TypeScript because the deprecated `moduleResolution=node10` option triggered TS5107
 * **RyanCavanaugh** added label `Domain: Type Inference`
 * **jakebailey** added label `Domain: check: Order Dependence`

### [Issue microsoft/TypeScript#30982](https://github.com/microsoft/TypeScript/issues/30982) (Open, `Bug`, `Domain: Indexed Access Types`, `Domain: check: Order Dependence`)

**Declaring index signature based on property type gives invalid error**

*TypeScript incorrectly reports a missing index signature when an interface references a derived property type in its index signature.*

 * **RyanCavanaugh** added label `Bug`
 * [7.6 years ago](https://github.com/microsoft/TypeScript/issues/30982#issuecomment-483888409) **RyanCavanaugh** said "Current behavior dates back to 2.1"
 * **RyanCavanaugh** added label `Domain: Indexed Access Types`
 * **jakebailey** added label `Domain: check: Order Dependence`

### [Issue microsoft/TypeScript#34099](https://github.com/microsoft/TypeScript/issues/34099) (Open, `Bug`, `Domain: check: Type Inference`, `Domain: check: Order Dependence`)

**Sorting an array removes type inference**

*TypeScript loses generic type inference when sorting an array created from a flattened iterable, incorrectly producing `unknown[]`.*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [7 years ago](https://github.com/microsoft/TypeScript/issues/34099#issuecomment-548107842) **RyanCavanaugh** said "Presumably generic inference isn't lining up the this through the return type of sort to produce an inference candidate for flatten"
 * **RyanCavanaugh** added label `Domain: Type Inference`
 * **jakebailey** added label `Domain: check: Order Dependence`

### [Issue microsoft/TypeScript#38460](https://github.com/microsoft/TypeScript/issues/38460) (Open, `Needs Investigation`, `Rescheduled`, `Domain: check: Order Dependence`, **weswigham**)

**\[3\.9\.2\] Regression \- combination of mapped type, intersection and generic produces error under infer**

*TypeScript 3.9.2 regression causes errors when inferring generic extensions from mapped types intersected with a base structure.*

 * (2.7 years ago) **RyanCavanaugh** set milestones to `TypeScript 5.5.0`, `TypeScript 5.7.0`, and removed from milestone `TypeScript 5.5.0`
 * **jakebailey** added label `Domain: check: Order Dependence`

### [Issue microsoft/TypeScript#41977](https://github.com/microsoft/TypeScript/issues/41977) (Closed, `Bug`, `Domain: check: Order Dependence`)

**Unexpected behavior when static methods are used in an array**

*TypeScript inconsistently checks an array combining static and regular methods, with an unrelated type alias affecting whether an assignment error is reported.*

 * (1 year ago) **RyanCavanaugh** added label `Domain: Error Instability`, and unassigned **RyanCavanaugh**
 * **jakebailey** removed label `Fix Available`
 * [today](https://github.com/microsoft/TypeScript/issues/41977#issuecomment-6970178405) **jakebailey** said "This is fixed in TS7."
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#42175](https://github.com/microsoft/TypeScript/issues/42175) (Open, `Bug`, `Domain: This-Typing`, `Domain: check: Order Dependence`)

**Assertion signature on contextual 'this'\-parameter doesn't narrow and has no error**

*Contextual `this` methods with assertion or `never` return signatures fail to narrow variables or report missing annotations consistently.*

 * (5.8 years ago) **RyanCavanaugh** added labels `Bug`, `Domain: This-Typing`, and set milestone to `Backlog`
 * **jakebailey** added label `Domain: check: Order Dependence`

### [Issue microsoft/TypeScript#43948](https://github.com/microsoft/TypeScript/issues/43948) (Open, `Needs Investigation`, `Rescheduled`, `Domain: check: Order Dependence`, **weswigham**)

**Unable to infer method property but able to infer arrow function property**

*TypeScript fails to infer a method property’s type in objects passed through Object.fromEntries, while arrow function properties infer correctly.*

 * (2.7 years ago) **RyanCavanaugh** set milestones to `TypeScript 5.5.0`, `TypeScript 5.7.0`, and removed from milestone `TypeScript 5.5.0`
 * **jakebailey** added label `Domain: check: Order Dependence`

### [Issue microsoft/TypeScript#45258](https://github.com/microsoft/TypeScript/issues/45258) (Closed, `Bug`, `Rescheduled`, `Domain: check: Order Dependence`, **armanio123**)

**unused type declaration causes totally unrelated error \(Index signatures are incompatible\)**

*An unused type alias unexpectedly causes an unrelated argument type error involving incompatible index signatures.*

 * (2.3 years ago) **RyanCavanaugh** added label `Domain: Error Instability`, set milestone to `TypeScript 5.7.0`, and removed from milestone `TypeScript 5.5.0`
 * [today](https://github.com/microsoft/TypeScript/issues/45258#issuecomment-6970177729) **jakebailey** said "This is fixed in TS7."
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#49280](https://github.com/microsoft/TypeScript/issues/49280) (Open, `Bug`, `Cursed?`, `Domain: check: Order Dependence`, `Domain: check: Type Circularity`)

**4\.7 regression: Array\.flat\(infinity\) leads to "Type instantiation is excessively deep and possibly infinite\." error**

*TypeScript 4.7 causes `Array.flat(Infinity)` on recursively nested arrays to trigger an excessively deep type instantiation error.*

 * [45 weeks ago](https://github.com/microsoft/TypeScript/issues/49280#issuecomment-3702824366) **tadhgmister** explained that recursive loops, rather than only direct recursive references, caused the type system to recurse infinitely; provided a failing Playground example and a counter-based solution that tracked previously seen structures.
 * [45 weeks ago](https://github.com/microsoft/TypeScript/issues/49280#issuecomment-3702960332) **tadhgmister** highlighted that the counter-based solution might mishandle fractional and negative indices, recommended distinguishing them from large flattening values, and suggested more thorough testing
 * **RyanCavanaugh** removed label `Help Wanted`
 * **jakebailey** added label `Domain: check: Order Dependence`

### [Issue microsoft/TypeScript#52313](https://github.com/microsoft/TypeScript/issues/52313) (Closed, `Bug`, `Domain: check: Type Inference`, `Has Repro`, `Union Order Dependence`)

**Order of ReadonlySet/ReadonlyMap in union causes differing key inference**

*ReadonlySet/ReadonlyMap union member order affects key type inference, causing valid calls to fail when ReadonlySet appears first.*

 * **RyanCavanaugh** added label `Domain: Type Inference`
 * [25 weeks ago](https://github.com/microsoft/TypeScript/issues/52313#issuecomment-4535746169) **wolfe8105** reported that the reproduction compiled cleanly on current main with correct inference for both union orders and asked whether the issue should be closed
 * [25 weeks ago](https://github.com/microsoft/TypeScript/issues/52313#issuecomment-4546013771) **RyanCavanaugh** said "@wolfe8105 how are you checking? I still see an error in the Playground on 6.0"
 * [today](https://github.com/microsoft/TypeScript/issues/52313#issuecomment-6970207469) **jakebailey** said "This is fixed in TS7."
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#52892](https://github.com/microsoft/TypeScript/issues/52892) (Open, `Needs Investigation`, `Rescheduled`, **jakebailey**)

**Instantiation expression inside nested classes produces unexpected circular reference error**

*TypeScript reports an unexpected circular reference when an instantiation expression references a nested class inside its enclosing generic class.*

 * **RyanCavanaugh** added to milestone `TypeScript 5.7.0`
 * **typescript-bot** added label `Fix Available`
 * **jakebailey** removed label `Fix Available`
 * (today) **jakebailey** added label `Domain: check: Order Dependence`, and removed label `Domain: check: Order Dependence`

### [Issue microsoft/TypeScript#55069](https://github.com/microsoft/TypeScript/issues/55069) (Open, `Needs Investigation`, `Domain: check: Order Dependence`, **sheetalkamat**)

**Incorrect errors reported if typeckecking only single file**

*TypeScript reports incorrect errors when incrementally type-checking only the modified server project file instead of the entire project.*

 * created by **sheetalkamat**
 * (3.3 years ago) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **sheetalkamat**
 * **jakebailey** added label `Domain: check: Order Dependence`

### [Issue microsoft/TypeScript#55640](https://github.com/microsoft/TypeScript/issues/55640) (Open, `Possible Improvement`, `Domain: check: Order Dependence`, `Domain: check: Type Circularity`)

**Typescript has more trouble resolving circular class references when using mixins / through function invocations**

*TypeScript struggles to resolve circular class references when mixins are created through generic function invocations.*

 * (3.1 years ago) **RyanCavanaugh** added label `Domain: Type Circularity`, removed label `Help Wanted`, and set milestone to `Backlog`
 * **jakebailey** added label `Domain: check: Order Dependence`

### [Issue microsoft/TypeScript#57037](https://github.com/microsoft/TypeScript/issues/57037) (Closed, `Domain: Error Messages`, `Possible Improvement`)

**Misleading error message when interface tries to extend constrained type parameter**

*TypeScript 3.7.5 reports a misleading generic constraint error when an interface extends an object-constrained type parameter, replacing a clearer diagnostic.*

 * (2.8 years ago) **RyanCavanaugh** added label `Domain: Error Messages`, removed label `Help Wanted`, and set milestone to `Backlog`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#58351](https://github.com/microsoft/TypeScript/issues/58351) (Closed, `Possible Improvement`, `Domain: check: Order Dependence`)

**Strange runtime caching bug involving \`as const\` and \`const T\` generic**

*TypeScript inconsistently caches generic type-checking results, causing code to compile only after temporarily adding and removing `as const`.*

 * (2.5 years ago) **RyanCavanaugh** added label `Domain: Error Instability`, removed label `Help Wanted`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/58351#issuecomment-6970176872) **jakebailey** said "This is fixed in TS7."
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#59920](https://github.com/microsoft/TypeScript/issues/59920) (Open, `Bug`, `Domain: JavaScript`, **jakebailey**)

**function object parameter destructure field without default value will be ignored**

*TypeScript 5.6+ incorrectly omits the required destructured `username` parameter field from inferred JavaScript function types, causing valid calls to fail.*

 * **RyanCavanaugh** added label `Domain: JavaScript`
 * [11 weeks ago](https://github.com/microsoft/TypeScript/issues/59920#issuecomment-5432044798) **jakebailey** explained that a proposed fix unnecessarily special-cased checked JavaScript files and said he would try Anders’ more reasonable suggestion instead
 * (8 weeks ago) **jakebailey** closed the issue
 * (today) **jakebailey** reopened the issue

### [Issue microsoft/TypeScript#60453](https://github.com/microsoft/TypeScript/issues/60453) (Open, `Bug`, `Domain: check: Variance Relationships`, `Domain: check: Order Dependence`)

**Error not generated for nested generic array**

*TypeScript fails to report an error when assigning nested generic array types with incompatible type parameters, a regression since version 4.5.5.*

 * [2 years ago](https://github.com/microsoft/TypeScript/issues/60453#issuecomment-2463305143) **thscott** reported that the workaround did not consistently work when assigning names to generic types and provided a TypeScript Playground reproduction showing the error only appeared when certain lines were uncommented
 * (1 year ago) **RyanCavanaugh** added label `Domain: Variance Relationships`, and removed label `Help Wanted`
 * **jakebailey** added label `Domain: check: Order Dependence`

### [Issue microsoft/TypeScript#61711](https://github.com/microsoft/TypeScript/issues/61711) (Open, `Possible Improvement`, `Domain: check: Order Dependence`, `Domain: check: Type Circularity`)

**Resolution order dependent circular heritage**

*TypeScript inconsistently reports circular heritage errors depending on declaration resolution order, particularly involving mixins, aliases, and dependent base types.*

 * (1.5 years ago) **RyanCavanaugh** added label `Domain: Type Circularity`, removed label `Help Wanted`, and set milestone to `Backlog`
 * **jakebailey** added label `Domain: check: Order Dependence`

### [Issue microsoft/TypeScript#61721](https://github.com/microsoft/TypeScript/issues/61721) (Open, `Possible Improvement`, `Domain: check: Order Dependence`, `Domain: check: Type Circularity`)

**Mixing base class defeats circularity protection**

*TypeScript incorrectly reports circularity errors when a mixin’s return type includes an internal class while extending a base class referencing the derived class.*

 * (1.5 years ago) **RyanCavanaugh** added label `Domain: Type Circularity`, removed label `Help Wanted`, and set milestone to `Backlog`
 * **jakebailey** added label `Domain: check: Order Dependence`

### [Issue microsoft/TypeScript#61982](https://github.com/microsoft/TypeScript/issues/61982) (Open, `Bug`, `Domain: check: Variance Relationships`, `Domain: check: Order Dependence`)

**Missing constraint error in instantiation expression for a nested class**

*TypeScript fails to report an invalid constraint when instantiating a nested class expression, a regression from version 5.6.*

 * [1.3 years ago](https://github.com/microsoft/TypeScript/issues/61982#issuecomment-3047743458) **MYRAA3110** provided a TypeScript example demonstrating generic constraints and usage of the nested class
 * (1 year ago) **RyanCavanaugh** added label `Domain: Variance Relationships`, and removed label `Help Wanted`
 * **jakebailey** added label `Domain: check: Order Dependence`

### [Issue microsoft/TypeScript#62181](https://github.com/microsoft/TypeScript/issues/62181) (Closed, `Bug`, `Domain: check: Order Dependence`)

**Ghost error in a circular situation**

*Circular mapped-type inference in a Zod-like schema produces inconsistent ghost errors depending on whether getter quick info is requested.*

 * (1 year ago) **RyanCavanaugh** added label `Domain: Type Circularity`, and removed labels `Domain: Type Circularity`, `Help Wanted`
 * [today](https://github.com/microsoft/TypeScript/issues/62181#issuecomment-6970176129) **jakebailey** said "This is fixed in TS7."
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#63854](https://github.com/microsoft/TypeScript/issues/63854) (Open, `Needs More Info`, `Domain: check: Order Dependence`)

**Identical resolved program produces 157 vs 662,155 diagnostics depending on whether the tsconfig is passed directly or through a pass\-through extends**

*TypeScript produces dramatically different, deterministic diagnostic counts for identical programs depending on tsconfig indirection and include composition, including massive spurious complexity errors.*

 * **RyanCavanaugh** added label `Needs More Info`
 * [17 weeks ago](https://github.com/microsoft/TypeScript/issues/63854#issuecomment-5351507057) **RyanCavanaugh** requested a reproducible case and suggested using the repro reduction skill
 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/63854#issuecomment-6489142249) **YevheniiKotyrlo** provided a dependency-free reproduction of TS2859 showing that comparisons of identical types began failing after sufficient preceding type-checking work, including generator commands, compiler versions, and observed errors
 * **jakebailey** added label `Domain: check: Order Dependence`

### [Issue microsoft/TypeScript#63949](https://github.com/microsoft/TypeScript/issues/63949) (Open, `Bug`, `Domain: check: Order Dependence`)

**\[7\.0 regression\] Type parameter default is ignored when the call sits inside a callback passed to a generic function**

*TypeScript 7.0 regression ignores default generic type parameters in callbacks, causing spurious assignability errors when invoking generic functions.*

 * (12 weeks ago) **RyanCavanaugh** assigned to **RyanCavanaugh**, and unassigned **RyanCavanaugh**, **Copilot**
 * **jakebailey** added label `Domain: check: Order Dependence`

### [Issue microsoft/TypeScript#64037](https://github.com/microsoft/TypeScript/issues/64037) (Closed, `Bug`, **johnfav03**)

**npx tsc \-w is triggering itself after each build**

*TypeScript watch mode repeatedly retriggers compilation when JavaScript outputs are written alongside source files, despite exclusion and watchOptions settings.*

 * (5 weeks ago) **RyanCavanaugh** added label `Bug`, removed label `Needs More Info`, and assigned to **johnfav03**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#64278](https://github.com/microsoft/TypeScript/issues/64278) (Open, `Possible Improvement`, `Domain: check: Order Dependence`)

**enhance: Add tests for premature caching of contextual parameter types**

*Add regression tests ensuring contextual parameter types are not cached prematurely when later widened during default-value checking.*

 * (9 weeks ago) **RyanCavanaugh** added label `Possible Improvement`, and set milestone to `Backlog`
 * [9 weeks ago](https://github.com/microsoft/TypeScript/issues/64278#issuecomment-5685058818) **RyanCavanaugh** said "Sure, go for it"
 * **jakebailey** added label `Domain: check: Order Dependence`

### [Issue microsoft/TypeScript#64384](https://github.com/microsoft/TypeScript/issues/64384) (Closed, `Bug`)

**Panic in \`TupleNormalizer\.normalize\` \(nil \`currentNode\`\) when declaration emit resolves an oversized tuple type under \`\-\-noCheck\`**

*Declaration-only emission with `--noCheck` panics in `TupleNormalizer.normalize` when resolving an oversized tuple type.*

 * created by **YuanchengJiang**
 * (8 weeks ago) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64385](https://github.com/microsoft/TypeScript/pull/64385) (Closed, `For Backlog Bug`)

**Fix panic when declaration emit resolves an oversized tuple type**

*Prevent declaration-only emit from panicking when resolving tuple types exceeding the 10,000-element limit without prior type checking.*

 * [8 weeks ago](https://github.com/microsoft/TypeScript/pull/64385#issuecomment-5787625510) **jakebailey** said "@weswigham Do you have any thoughts about this?"
 * [8 weeks ago](https://github.com/microsoft/TypeScript/pull/64385#issuecomment-5788183773) **weswigham** warned that suppressing emit-time diagnostics could cache state that prevents later typechecks from reporting them, and suggested anchoring diagnostics to the type symbol’s declaration instead of the checker’s current node
 * [7 weeks ago](https://github.com/microsoft/TypeScript/pull/64385#issuecomment-5831934164) **mohit-nayak** reported that caching caused emit to permanently cache an error type and suppress a later diagnostic, confirmed that restoring the declaration as the context node preserved the error without test regressions, and outlined caveats and options for addressing additional emit-resolver entry points
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#64431](https://github.com/microsoft/TypeScript/issues/64431) (Closed, `Bug`, **RyanCavanaugh**, **Copilot**)

**TS7031 false positive for nested object binding pattern with \`= {}\` default in an annotated parameter \(regression from \#64043\)**

*Regression causes TS7031 false positives for nested object destructuring defaults in explicitly annotated parameters.*

 * [yesterday](https://github.com/microsoft/TypeScript/issues/64431#issuecomment-6926736232) **abrahamguo** reported that the regression reproduced without annotations when a parameter type came from context, bisected it to #64043, and asked whether it could be fixed or reverted before the 7.1.0 release
 * [yesterday](https://github.com/microsoft/TypeScript/issues/64431#issuecomment-6926949090) **jakebailey** said "I did not even know about this issue or that I caused it. I will take a look."
 * [yesterday](https://github.com/microsoft/TypeScript/issues/64431#issuecomment-6927187337) **trevorade** mentioned that validation of tsgo against Google’s TypeScript codebase uncovered potentially overlooked regressions and linked issues 64437, 64673, and 64453 for review
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64440](https://github.com/microsoft/TypeScript/pull/64440) (Closed, `For Uncommitted Bug`, **RyanCavanaugh**, **Copilot**)

**Fix false implicit\-any errors in annotated nested bindings**

*Fix false TS7031 implicit-any errors for nested object bindings whose types are supplied by enclosing parameter annotations.*

 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [7 weeks ago](https://github.com/microsoft/TypeScript/pull/64440#issuecomment-5835281784) **RyanCavanaugh** said "@copilot mcfly this and also explain why this is a correct fix"
 * [7 weeks ago](https://github.com/microsoft/TypeScript/pull/64440#issuecomment-5836318835) **trevorade** reported that the fix passed the tested cases and nested callback typing, identified two remaining differences from 6.0.3 involving contextual `any` and partially typed object bindings, and noted missing `.types`/`.symbols` baseline updates
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#64635](https://github.com/microsoft/TypeScript/issues/64635) (Open, `Needs Investigation`, `Domain: check: Order Dependence`, **andrewbranch**)

**API server reports TS2345 for a call that tsc accepts on the same project**

*The TypeScript API server inconsistently reports TS2345 for code that tsc accepts, apparently depending on program construction or type-checking order.*

 * (6 weeks ago) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.1.1 RC`, and assigned to **andrewbranch**
 * **jakebailey** added label `Domain: check: Order Dependence`

### [PR microsoft/TypeScript#64671](https://github.com/microsoft/TypeScript/pull/64671) (Closed, `For Uncommitted Bug`, **RyanCavanaugh**)

**Do not pad binding elements that the parameter's type already types**

*Fix `padObjectLiteralType` to preserve annotated or contextually typed binding element types, including nested patterns, while padding only untyped elements.*

 * created by **Konan69**
 * (5 weeks ago) **typescript-automation[bot]** added label `For Uncommitted Bug`, and assigned to **RyanCavanaugh**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#64710](https://github.com/microsoft/TypeScript/issues/64710) (Open, `Domain: check: Order Dependence`, **johnfav03**)

**\[ServerErrors\]\[JavaScript\] main**

*Reports JavaScript server errors detected during analysis of 300 popular TypeScript repositories, with three repositories showing notable changes.*

 * [5 weeks ago](https://github.com/microsoft/TypeScript/issues/64710#issuecomment-6090297018) **typescript-automation[bot]** reported a premature server connection closure affecting apache/pouchdb and provided error artifacts, recent requests, and reproduction steps
 * [5 weeks ago](https://github.com/microsoft/TypeScript/issues/64710#issuecomment-6090297648) **typescript-automation[bot]** reported a premature server connection closure affecting vuejs/vue-cli and provided reproduction details and request traces
 * **RyanCavanaugh** assigned to **johnfav03**
 * **jakebailey** added label `Domain: check: Order Dependence`

### [Issue microsoft/TypeScript#64757](https://github.com/microsoft/TypeScript/issues/64757) (Open, `Needs Investigation`, `Domain: check: Order Dependence`, **ahejlsberg**)

**Regression in 7\.1 \(\#64553\): R inferred as unknown through a generic type alias call signature with a nested same\-type argument**

*TypeScript 7.1 regression causes generic type inference to resolve a nested effect’s type parameter as unknown instead of Req.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/64757#issuecomment-6544123377) **artile** provided a minimized reproduction showing a TypeScript 7.1 regression where inference changed from `never` to `unknown` for instantiated generic-interface methods when the outer type parameter was used in a nested type, and narrowed the regression to builds between 7.1.0-dev.20260930.4 and 7.1.0-dev.20261001.1
 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/64757#issuecomment-6546851553) **kennysarnoski-jarvis** reported that #65077 identified and fixed the regression caused by an overly broad recursion check in #64553, added compiler coverage for the affected cases, and restored correct inference across the reported repros
 * [4 days ago](https://github.com/microsoft/TypeScript/issues/64757#issuecomment-6849600158) **meehow-m** reported a regression where generic object type aliases infer `T` as `unknown`, allowing invalid writes through `Promise<AsyncIterable<T>>`, and provided reproduction steps, version results, and analysis
 * **jakebailey** added label `Domain: check: Order Dependence`

### [Issue microsoft/TypeScript#64849](https://github.com/microsoft/TypeScript/issues/64849) (Open, `Needs Investigation`, `Domain: check: Order Dependence`)

**\[ServerErrors\]\[JavaScript\] main**

*Main reports JavaScript server errors detected while analyzing 300 popular TypeScript repositories, with results from 225 successfully analyzed repositories.*

 * [1 month ago](https://github.com/microsoft/TypeScript/issues/64849#issuecomment-6226258746) **typescript-automation[bot]** reported a premature server connection closure for trekhleb/javascript-algorithms, including affected requests and reproduction details
 * [1 month ago](https://github.com/microsoft/TypeScript/issues/64849#issuecomment-6226259334) **typescript-automation[bot]** reported a panic while handling textDocument/diagnostic for chartjs/Chart.js and provided a stack trace, affected repository details, and replay artifacts
 * **RyanCavanaugh** added label `Needs Investigation`
 * **jakebailey** added label `Domain: check: Order Dependence`

### [PR microsoft/TypeScript#64900](https://github.com/microsoft/TypeScript/pull/64900) (Open, `For Backlog Bug`)

**Fix unused renaming detection in function types**

*Correct unused-renaming detection so type-only references in generic function types do not suppress diagnostics for unused destructured value bindings.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript/pull/64900#issuecomment-6317648836) **wickstudio** said "@microsoft-github-policy-service agree"
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/64900#issuecomment-6862090261) **jakebailey** suggested splitting the changes into separate commits for the failing test and baseline, followed by the fix and updated baseline
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64900#issuecomment-6938782055) **wickstudio** split the changes into two commits, adding the regression test with the original baseline first and the fix with the updated baseline second, and reported that all local tests passed
 * [today](https://github.com/microsoft/TypeScript/pull/64900#issuecomment-6958085785) **jakebailey** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/64900#issuecomment-6958087928) **typescript-automation[bot]** reported that the requested test and performance jobs started, with results available or still pending
 * [today](https://github.com/microsoft/TypeScript/pull/64900#issuecomment-6958771794) **typescript-automation[bot]** reported that the DT test results were ready and unchanged, and linked the build log
 * [today](https://github.com/microsoft/TypeScript/pull/64900#issuecomment-6958958296) **typescript-automation[bot]** provided the requested performance results comparing the baseline and PR
 * [today](https://github.com/microsoft/TypeScript/pull/64900#issuecomment-6959215523) **typescript-automation[bot]** reported that user tests comparing the baseline and PR with tsc passed successfully
 * [today](https://github.com/microsoft/TypeScript/pull/64900#issuecomment-6960122889) **typescript-automation[bot]** reported that testing the top 400 repositories with tsc showed no differences between the baseline and PR, with everything looking good

### [Issue microsoft/TypeScript#64930](https://github.com/microsoft/TypeScript/issues/64930) (Open, `Bug`)

**7\.1 regression: circular type alias accepts an assignment it should reject \(opposite of \#64891\)**

*TypeScript 7.1 regresses by allowing incompatible circular generic handler assignments that should produce TS2322 errors.*

 * created by **Nabil372**
 * (3 weeks ago) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`
 * [later](https://github.com/microsoft/TypeScript/issues/64930#issuecomment-6982595670) **Sipixer** reported that version 7.1 also broke untyped `@tanstack/db` collections by inferring `Collection<never, …>`, provided a reproduction showing thousands of production errors, and confirmed the issue persisted in the latest nightly after #65030

### [Issue microsoft/TypeScript#64974](https://github.com/microsoft/TypeScript/issues/64974) (Closed, `Bug`)

**7\.1: destructured parameter with a \`= {}\` default loses its contextual type \(TS7031\)**

*TypeScript 7.1 regresses contextual typing for destructured optional parameters with `{}` defaults, incorrectly reporting binding elements as implicitly `any`.*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/64974#issuecomment-6610623048) **connorshea** said "I think this may be the same issue as #64431?"
 * [6 days ago](https://github.com/microsoft/TypeScript/issues/64974#issuecomment-6801596375) **maschwenk** reported that the original snippet regressed from clean to TS7031 between nightly builds, bisected the change to commit 07d1338bac, and noted that several related PR heads cleared the issue while the #65070 array example also reproduced the error in earlier releases
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64978](https://github.com/microsoft/TypeScript/pull/64978) (Closed, `For Backlog Bug`)

**fix\(64974\): fix contextual typing for destructured parameter defaults**

*Fix contextual typing for destructured function parameters that include default values.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/64978#issuecomment-6513976139) **timurzvural** explained that the regression caused missing properties in defaulted destructured parameters to become implicit `any`, confirmed the contextual-type guard restored the expected `string | undefined` and `number` types, and noted that #65016 would add mixed-shape regression coverage
 * (2 weeks ago) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#64998](https://github.com/microsoft/TypeScript/issues/64998) (Open, `Bug`, `Domain: check: Order Dependence`)

**declaration emit depends on checker assignment; a type alias becomes \`any\` with no error**

*Multi-threaded declaration emit nondeterministically infers a type alias as `any` without diagnostics, unlike single-threaded emit.*

 * [1 week ago](https://github.com/microsoft/TypeScript/issues/64998#issuecomment-6782159932) **RyanCavanaugh** said "Should be fixed by #65293"
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/64998#issuecomment-6782173572) **jakebailey** said "Sadly @blickly already confirmed it does not, which is scary"
 * [yesterday](https://github.com/microsoft/TypeScript/issues/64998#issuecomment-6932850442) **blickly** reported that #65293 fixed the issue at commit 9a2e423, but identified a separate checker-count-dependent issue and filed it as #65543
 * **jakebailey** added label `Domain: check: Order Dependence`

### [PR microsoft/TypeScript#65070](https://github.com/microsoft/TypeScript/pull/65070) (Closed, `For Backlog Bug`)

**fix\(65069\): preserve contextual types for array\-destructured parameter defaults**

*Preserve contextual types for array-destructured parameter defaults like `= []` to prevent erroneous TS7031 binding-element errors.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/65070#issuecomment-6592543087) **typescript-automation[bot]** reported that user tests comparing the baseline and PR with tsc passed without issues
 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/65070#issuecomment-6592747094) **typescript-automation[bot]** reported that the requested performance run results were available, including a baseline-to-PR compiler comparison
 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/65070#issuecomment-6593418913) **typescript-automation[bot]** reported that testing the top 400 repositories with tsc showed no differences between the baseline and PR, with everything looking good
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#65087](https://github.com/microsoft/TypeScript/issues/65087) (Open, `Bug`, `Domain: API`)

**Native API: formatDiagnosticsWithColorAndContext drops related information without a file location**

*Native diagnostic formatting omits related information without file locations, unlike TypeScript 6.0.3, and should preserve its text.*

 * created by **emerardd**
 * (today) **RyanCavanaugh** added labels `Bug`, `Domain: API`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#65098](https://github.com/microsoft/TypeScript/issues/65098) (Open, `Bug`, **gabritto**)

**TS7\.1 importing \.json with type: something still parses the JSON file even though ambient module declaration is used**

*TypeScript 7.1 unnecessarily parses JSON imports even when matching ambient module declarations with import attributes provide their types.*

 * created by **Knagis**
 * (today) **RyanCavanaugh** added label `Bug`, set milestone to `TypeScript 7.1.1 RC`, and assigned to **gabritto**

### [PR microsoft/TypeScript#65293](https://github.com/microsoft/TypeScript/pull/65293) (Open, `Author: Team`, `For Milestone Bug`, `For Backlog Bug`, **jakebailey**)

**Make checker behavior order independent**

*Refactor checker state and cycle handling to make diagnostics, variance calculations, and instantiation limits deterministic regardless of query or processing order.*

 * (4 days ago) **typescript-automation[bot]** added labels `For Backlog Bug`, `For Milestone Bug`, and removed label `For Milestone Bug`
 * **typescript-automation[bot]** added label `For Milestone Bug`

### [Issue microsoft/TypeScript#65333](https://github.com/microsoft/TypeScript/issues/65333) (Closed, `Bug`, **weswigham**, **RyanCavanaugh**, **Copilot**)

**Downlevel \`this\.\#x &&= v\` / \`\|\|=\` / \`??=\` on a private accessor always calls the setter**

*Downleveling private accessor logical assignments unconditionally invokes setters instead of preserving short-circuit behavior for &&=, ||=, and ??=.*

 * [1 week ago](https://github.com/microsoft/TypeScript/issues/65333#issuecomment-6665295542) **morluto** said "nice."
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/65333#issuecomment-6677488799) **trackoor** described using a formally verified TypeScript compiler and runtime as a ground truth, differential fuzzing to find bugs, and AI to triage and report them; emphasized the importance of accurate specifications and invariants
 * **RyanCavanaugh** assigned to **weswigham**
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#65335](https://github.com/microsoft/TypeScript/pull/65335) (Closed, `Author: Team`, `For Uncommitted Bug`, **RyanCavanaugh**, **Copilot**)

**Preserve short\-circuiting in downlevel private logical assignments**

*Preserve short-circuiting when downleveling private logical assignments by avoiding setter calls when assignments are skipped.*

 * (1 week ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/65335#issuecomment-6965081378) **weswigham** said "(yes)"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#65348](https://github.com/microsoft/TypeScript/issues/65348) (Open, `Suggestion`)

**Content mappers: let openProject watch a directory or glob, so a file added later reloads the mapper**

*Allow content mappers’ openProject results to watch directories or globs so adding matching files reloads the mapper and prevents stale output.*

 * created by **toiroakr**
 * **RyanCavanaugh** added label `Suggestion`

### [Issue microsoft/TypeScript#65350](https://github.com/microsoft/TypeScript/issues/65350) (Open, `Bug`, `Domain: Content Mappers`)

**Content mappers: TS7016 suggestion for a mapped file reached through a package in node\_modules**

*Content-mapped TypeScript files resolved through node_modules incorrectly trigger a TS7016 implicit-any suggestion in the language server.*

 * created by **toiroakr**
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/65350#issuecomment-6678765354) **toiroakr** provided a concrete reproduction and proposed skipping TS7016 for external-library files resolved through content mappers while preserving TS2322
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/65350#issuecomment-6678783036) **toiroakr** provided a concrete reproduction and proposed a fix to suppress the incorrect TS7016 suggestion for files resolved through a content mapper while preserving TS2322
 * (today) **RyanCavanaugh** added labels `Bug`, `Domain: Content Mappers`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#65355](https://github.com/microsoft/TypeScript/issues/65355) (Open, `Suggestion`)

**Remote declaration resolution**

*Request support for resolving remote TypeScript declaration files in browser-based, bundler-free ESM projects without installing runtime dependencies.*

 * [6 days ago](https://github.com/microsoft/TypeScript/issues/65355#issuecomment-6811360610) **typescript-automation[bot]** said "This issue has been marked as "Duplicate" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (6 days ago) **typescript-automation[bot]** closed the issue
 * [4 days ago](https://github.com/microsoft/TypeScript/issues/65355#issuecomment-6863152676) **alshdavid** said "It's is not a duplicate. That other ticket is similar but different"
 * (today) **RyanCavanaugh** reopened the issue
 * (today) **RyanCavanaugh** added label `Suggestion`, and removed label `Duplicate`

### [Issue microsoft/TypeScript#65358](https://github.com/microsoft/TypeScript/issues/65358) (Open, `Bug`, `Domain: tsc -b`)

**Circular project references cause tsc \-\-noEmit to silently skip type errors and exit successfully**

*TypeScript 7.0.2 silently skips type errors and exits successfully when projects contain circular references, regressing from TypeScript 6.0.3.*

 * created by **camc314**
 * (today) **RyanCavanaugh** added labels `Bug`, `Domain: tsc -b`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#65363](https://github.com/microsoft/TypeScript/issues/65363) (Open, `Bug`, `Domain: Decorators`)

**ES decorator metadata emit throws when a decorated class extends null**

*Standard decorator metadata emit crashes for classes extending null instead of safely inheriting null-prototype metadata.*

 * created by **yusufyildiz34**
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/65363#issuecomment-6716396003) **visualkhh** provided a reproduction on TypeScript 5.9.3, narrowed the bug to standard decorators, explained the null superclass metadata failure, proposed a fix using the constructor prototype chain, and suggested regression-test coverage
 * (today) **RyanCavanaugh** added labels `Bug`, `Domain: Decorators`, and set milestone to `Backlog`

### [PR microsoft/TypeScript#65364](https://github.com/microsoft/TypeScript/pull/65364) (Open, `For Backlog Bug`)

**Fix ES decorator metadata crash when class extends null**

*Fix decorator metadata emission for classes extending null by safely providing null parent metadata instead of throwing.*

 * created by **yusufyildiz34**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (today) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`

### [Issue microsoft/TypeScript#65370](https://github.com/microsoft/TypeScript/issues/65370) (Open, `Bug`, `Domain: lib.d.ts`)

**Iterator\.prototype\.flatMap accepts primitive string results**

*Update `Iterator.prototype.flatMap` typings to reject primitive string mapper results while preserving arrays, iterators, and boxed strings.*

 * created by **dvkam**
 * (today) **RyanCavanaugh** added labels `Bug`, `Domain: lib.d.ts`, and set milestone to `Backlog`

### [PR microsoft/TypeScript#65372](https://github.com/microsoft/TypeScript/pull/65372) (Open, `For Backlog Bug`)

**lib: reject primitive strings from iterator flatMap mappers**

*Require Iterator.prototype.flatMap mappers to return iterator or iterable objects, rejecting primitive strings while preserving valid iterable results.*

 * created by **dvkam**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/65372#issuecomment-6699528779) **dvkam** said "@microsoft-github-policy-service agree"
 * (today) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`

### [Issue microsoft/TypeScript#65374](https://github.com/microsoft/TypeScript/issues/65374) (Open, `Bug`, `Domain: lib.d.ts`)

**Array\.fromAsync mapper types unwrap promises yielded by async iterables**

*Correct Array.fromAsync mapper typings so async iterables pass yielded promises directly, while sync and array-like inputs continue unwrapping values.*

 * created by **dvkam**
 * (today) **RyanCavanaugh** added labels `Bug`, `Domain: lib.d.ts`, and set milestone to `Backlog`

### [PR microsoft/TypeScript#65375](https://github.com/microsoft/TypeScript/pull/65375) (Open, `For Backlog Bug`)

**lib: type Array\.fromAsync mapper inputs by source protocol**

*Update Array.fromAsync typing so mapper inputs and results are correctly awaited based on the source protocol.*

 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/65375#issuecomment-6700216556) **dvkam** said "I reproduced the finding locally with strictNullChecks disabled and am looking into it."
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/65375#issuecomment-6710623422) **dvkam** reordered overloads to select the synchronous mapper type for nullish async iterator methods when `strictNullChecks` was disabled, and added regression tests covering nullish methods and dual-protocol sources
 * (today) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`

### [Issue microsoft/TypeScript#65380](https://github.com/microsoft/TypeScript/issues/65380) (Open, `Bug`, `Domain: Declaration Emit`)

**\`readonly\` dropped from a function\-valued property under a \`const\` type parameter**

*TypeScript 7.x declaration emit incorrectly drops readonly from nested function-valued properties inferred under const type parameters.*

 * created by **trackoor**
 * (1 week ago) **trackoor** closed the issue
 * (1 week ago) **trackoor** reopened the issue
 * (today) **RyanCavanaugh** added labels `Bug`, `Domain: Declaration Emit`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#65385](https://github.com/microsoft/TypeScript/issues/65385) (Open, `Needs Investigation`, **joj**)

**VisualStudio 2026 \- Razor Class Library**

*Adding Microsoft.TypeScript.MSBuild 7.0.1 to Razor or Blazor projects causes Visual Studio to repeatedly detect changes, prompt reloads, or prevent applications from running.*

 * [1 week ago](https://github.com/microsoft/TypeScript/issues/65385#issuecomment-6750712289) **RyanCavanaugh** requested a minimal Razor/Blazor project, the exact Visual Studio version, reproduction steps, the project file, and relevant build or ActivityLog output for the reload loop
 * [6 days ago](https://github.com/microsoft/TypeScript/issues/65385#issuecomment-6799205771) **ghorner2** provided reproduction steps for a Blazor WASM project using Microsoft.Typescript.MSBuild and a sample tsconfig.json
 * [6 days ago](https://github.com/microsoft/TypeScript/issues/65385#issuecomment-6804272038) **ghorner2** provided a GitHub repository link to demonstrate the issue
 * (today) **RyanCavanaugh** added label `Needs Investigation`, removed label `Needs More Info`, and assigned to **joj**

### [PR microsoft/TypeScript#65405](https://github.com/microsoft/TypeScript/pull/65405) (Open, `For Milestone Bug`, `For Backlog Bug`, **weswigham**)

**Preserve readonly properties when reusing declaration syntax**

*Ensure readonly property modifiers are preserved when declaration syntax is reused.*

 * created by **Andarist**
 * (1 week ago) **typescript-automation[bot]** added label `For Milestone Bug`, and assigned to **weswigham**
 * **typescript-automation[bot]** added label `For Backlog Bug`

### [PR microsoft/TypeScript#65409](https://github.com/microsoft/TypeScript/pull/65409) (Open, `Author: Team`, `For Uncommitted Bug`, **RyanCavanaugh**, **Copilot**)

**Add flow path for a falsy, non\-nullish left operand of \`??\` and \`??=\`**

*Add flow analysis for falsy, non-nullish operands of ?? and ??= to prevent false reachability errors and incorrect narrowing.*

 * [1 week ago](https://github.com/microsoft/TypeScript/pull/65409#issuecomment-6751887408) **Copilot** asked for clarification about whether the 🚲 emoji meant addressing the earlier review findings
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/65409#issuecomment-6752443527) **RyanCavanaugh** said "@copilot do another "cycle" of work on this - you have high-priority comments, and failing CI!"
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/65409#issuecomment-6753030269) **Copilot** added missing compiler baselines and regression cases, fixed reachability and optional-chain routing issues, and reported successful validation while noting that CodeQL was skipped due to database size limits
 * [today](https://github.com/microsoft/TypeScript/pull/65409#issuecomment-6958104276) **jakebailey** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/65409#issuecomment-6958106836) **typescript-automation[bot]** reported that the requested test jobs started and provided links to their build results
 * [today](https://github.com/microsoft/TypeScript/pull/65409#issuecomment-6958812996) **typescript-automation[bot]** reported that the DT test results were ready and unchanged, and linked the build log
 * [today](https://github.com/microsoft/TypeScript/pull/65409#issuecomment-6959251563) **typescript-automation[bot]** reported that the requested performance run results were available and included baseline-versus-PR comparison metrics
 * [today](https://github.com/microsoft/TypeScript/pull/65409#issuecomment-6959388671) **typescript-automation[bot]** reported that user tests comparing the baseline and PR with tsc passed successfully
 * [today](https://github.com/microsoft/TypeScript/pull/65409#issuecomment-6960952769) **typescript-automation[bot]** reported that testing the top 400 repositories with tsc showed no differences between the baseline and PR, with everything looking good

### [Issue microsoft/TypeScript#65413](https://github.com/microsoft/TypeScript/issues/65413) (Open, `Bug`, `Domain: JS Emit`)

**Downlevel \`for \(this\.\#x of \.\.\.\)\` / \`for \(this\.\#x in \.\.\.\)\` emits \`\_\_classPrivateFieldGet\(\.\.\.\)\` as the loop target**

*Downlevel compilation incorrectly emits private-field getters as invalid for-in/for-of loop targets, causing generated JavaScript to fail parsing.*

 * created by **trackoor**
 * (today) **RyanCavanaugh** added labels `Bug`, `Domain: JS Emit`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#65414](https://github.com/microsoft/TypeScript/issues/65414) (Open, `Bug`, `Domain: JS Emit`)

**CommonJS emit gives an imported function the wrong \`this\` when the callee is wrapped**

*CommonJS emit incorrectly preserves the imported module object as `this` when an imported function call is wrapped in parentheses or expressions.*

 * created by **trackoor**
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/65414#issuecomment-6882653761) **sundeep8967** reported a reproducible emitter issue involving wrapped imported callees and offered to prepare a fix with regression tests
 * (today) **RyanCavanaugh** added labels `Bug`, `Domain: JS Emit`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#65424](https://github.com/microsoft/TypeScript/issues/65424) (Open, `Suggestion`)

**Native API: expose inferred type arguments of a resolved signature**

*Expose inferred type arguments for resolved signatures through the native synchronous and asynchronous TypeScript Checker APIs.*

 * created by **darkyeg**
 * **RyanCavanaugh** added label `Suggestion`

### [Issue microsoft/TypeScript#65425](https://github.com/microsoft/TypeScript/issues/65425) (Open, `Bug`, `Domain: LS: Symbol Navigation`)

**References code lens missing on export default in the native language server**

*The native language server no longer shows references code lenses for identifiers in `export default` or `export =` assignments.*

 * created by **k1tbyte**
 * (today) **RyanCavanaugh** added labels `Bug`, `Domain: LS: Symbol Navigation`, and set milestone to `Backlog`

### [PR microsoft/TypeScript#65426](https://github.com/microsoft/TypeScript/pull/65426) (Open, `For Backlog Bug`)

**Show references code lens on export assignments in native language server**

*Show references code lenses for `export default` expressions and `export =` assignments in the native language server.*

 * created by **k1tbyte**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/65426#issuecomment-6765369390) **k1tbyte** said "@microsoft-github-policy-service agree"
 * (today) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`

### [PR microsoft/TypeScript#65427](https://github.com/microsoft/TypeScript/pull/65427) (Open, `For Backlog Bug`)

**Fix downlevel emit for private names in for\-in/for\-of assignment targets**

*Fix downlevel emission of private-name and destructuring targets in for-in, for-of, and for-await loops by assigning through temporaries per iteration.*

 * created by **RealThanhNguyxn**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (today) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`

### [Issue microsoft/TypeScript#65429](https://github.com/microsoft/TypeScript/issues/65429) (Open, `Bug`, **weswigham**)

**Native printer panics when printing JSDoc AST nodes \(emitJSDocNode not implemented\)**

*Native printer panics when emitting JSDoc AST nodes because emitJSDocNode is unimplemented, preventing formatted JSDoc output.*

 * created by **el-j**
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/65429#issuecomment-6772658578) **el-j** mentioned that the fix was available in #65430, linked related context, and asked @RyanCavanaugh to review it for inclusion in 7.1
 * (today) **RyanCavanaugh** added label `Bug`, set milestone to `TypeScript 7.1.1 RC`, and assigned to **weswigham**

### [PR microsoft/TypeScript#65430](https://github.com/microsoft/TypeScript/pull/65430) (Open, `For Milestone Bug`, **weswigham**)

**feat\(printer\): implement JSDoc node emission**

*Implement JSDoc AST node emission in the printer, including comments, tags, layouts, type expressions, and qualified names without crashes.*

 * created by **el-j**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/65430#issuecomment-6773726732) **el-j** reported that the change fixed an `emitJSDocNode` printer crash also present in 7.1 Beta and asked whether it could be cherry-picked to `release-7.1` after landing on `main`
 * (today) **typescript-automation[bot]** added label `For Milestone Bug`, removed label `For Uncommitted Bug`, and assigned to **weswigham**

### [Issue microsoft/TypeScript#65440](https://github.com/microsoft/TypeScript/issues/65440) (Open, `Needs Investigation`, `Domain: check: Order Dependence`, **ahejlsberg**, **jakebailey**)

**7\.1 regression: bounded recursive types report TS5115 when inferred through a closure**

*TypeScript 7.1 regresses by reporting TS5115/TS2589 for bounded recursive types inferred through closures, despite valid code.*

 * created by **RomainLanz**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **ahejlsberg**, **jakebailey**
 * **jakebailey** added label `Domain: check: Order Dependence`

### [Issue microsoft/TypeScript#65444](https://github.com/microsoft/TypeScript/issues/65444) (Open, `Bug`, `Domain: LS: Refactorings`)

**7\.0 regression: \`prepareRename\` placeholder includes quotes and brackets**

*TypeScript 7.0 regresses `prepareRename` by including quotes and brackets in property rename placeholders, producing invalid syntax when renamed.*

 * created by **mizdra**
 * (today) **RyanCavanaugh** added labels `Bug`, `Domain: LS: Refactorings`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#65451](https://github.com/microsoft/TypeScript/issues/65451) (Open, `Bug`, `Domain: API`)

**Native API createSourceFile panics for numeric literals whose normalized text is longer than the source**

*Native API createSourceFile panics when numeric literals normalize to text longer than their original source spelling.*

 * created by **AkisArou**
 * (today) **RyanCavanaugh** added labels `Bug`, `Domain: API`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#65452](https://github.com/microsoft/TypeScript/issues/65452) (Open, `Bug`, `Domain: Crashes`)

**Checker crashes on yield\* of a synchronous iterable containing an invalid thenable**

*TypeScript crashes while checking `yield*` over a synchronous iterable containing an invalid thenable instead of reporting a diagnostic.*

 * created by **AkisArou**
 * (today) **RyanCavanaugh** added labels `Bug`, `Domain: Crashes`, and set milestone to `Backlog`
 * [later](https://github.com/microsoft/TypeScript/issues/65452#issuecomment-6981493723) **zhengdaodeguL** reported that #65561 fixed a checker crash by preserving diagnostic context, correctly reporting TS1322 and TS1320, and adding a regression test

### [Issue microsoft/TypeScript#65453](https://github.com/microsoft/TypeScript/issues/65453) (Open, `Suggestion`)

**\[Formatter\] add new options for blank lines**

*Add formatter options to remove unnecessary blank lines and limit consecutive blank lines in TypeScript code.*

 * created by **jmevel**
 * **RyanCavanaugh** added label `Suggestion`

### [PR microsoft/TypeScript#65456](https://github.com/microsoft/TypeScript/pull/65456) (Open, `For Backlog Bug`)

**Fix prepareRename placeholders for quoted and computed properties**

*Fix rename placeholders for quoted and computed properties by using the source node’s name while preserving existing range and fallback behavior.*

 * created by **rafamolina1**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (today) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`

### [Issue microsoft/TypeScript#65457](https://github.com/microsoft/TypeScript/issues/65457) (Open, `Bug`, `Domain: API`)

**\`typescript/async\`: getSourceFile\(\) returns a NumberKeyword for a typeToTypeNode\(\) result**

*`typeToTypeNode()` synthesizes a `NumberKeyword` whose `getSourceFile()` incorrectly returns the node itself instead of a `SourceFile`.*

 * created by **mathcovax**
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/65457#issuecomment-6898492365) **markstone111** expressed willingness to investigate synthesized node handling in getSourceFile(), add regression tests, and implement a fix
 * (today) **RyanCavanaugh** added labels `Bug`, `Domain: API`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#65458](https://github.com/microsoft/TypeScript/issues/65458) (Open, `Bug`, `Domain: API`)

**Native API: Wtf8Decoder drops U\+FEFF from string literals and template text**

*Wtf8Decoder incorrectly strips U+FEFF from leading positions in string literals and template text when using the native TypeScript API.*

 * created by **mrousavy**
 * (today) **RyanCavanaugh** added labels `Bug`, `Domain: API`, and set milestone to `Backlog`

### [PR microsoft/TypeScript#65464](https://github.com/microsoft/TypeScript/pull/65464) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Check the preceding rune before recognizing conflict markers**

*Update conflict-marker detection to decode the preceding rune for line-boundary checks while preserving the ASCII fast path.*

 * (5 days ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#65475](https://github.com/microsoft/TypeScript/pull/65475) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**, **johnfav03**)

**Prevent emitted files from retriggering native watch builds**

*Prevent generated output files from triggering native watch-mode rebuilds.*

 * (5 days ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **johnfav03**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#65482](https://github.com/microsoft/TypeScript/pull/65482) (Open, `For Backlog Bug`)

**fix\(api\): avoid encoder panic on normalized numeric literals**

*Prevent the API encoder from panicking when normalized numeric literals produce negative source offsets, preserving existing fallback behavior and wire format.*

 * created by **JemmyIndex**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (today) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`

### [Issue microsoft/TypeScript#65483](https://github.com/microsoft/TypeScript/issues/65483) (Open, `Bug`, `Domain: check: Order Dependence`)

**7\.1 regression: TS2339 in a self\-referencing object literal is dropped when another file on the same checker hits the same error first**

*A 7.1 regression drops TS2339 diagnostics in self-referencing object literals when another file reports the same error first under single-threaded checking.*

 * created by **meehow-m**
 * (today) **RyanCavanaugh** added labels `Bug`, `Domain: check: Error Instability`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#65485](https://github.com/microsoft/TypeScript/issues/65485) (Open, `Bug`, `Domain: API`)

**API: \`generateTrace\` compiler option is accepted but no trace files are written for programs created through \`typescript/sync\`**

*The typescript/sync API accepts generateTrace but fails to write trace files for configured or synthetic programs.*

 * created by **johnnyreilly**
 * (today) **RyanCavanaugh** added labels `Bug`, `Domain: API`, and set milestone to `Backlog`

### [PR microsoft/TypeScript#65489](https://github.com/microsoft/TypeScript/pull/65489) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Fix incorrect node type annotations**

*Correct inaccurate node type annotations identified during an audit.*

 * (4 days ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#65490](https://github.com/microsoft/TypeScript/pull/65490) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Match typed\-path lint URL detection to runtime roots**

*Update typed-path lint URL detection to match the runtime’s configured roots.*

 * (4 days ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#65491](https://github.com/microsoft/TypeScript/pull/65491) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Keep formatting fragments out of source\-file statement lists**

*Ensure formatting fragments are excluded from source-file statement lists to comply with their declared types.*

 * (4 days ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#65495](https://github.com/microsoft/TypeScript/pull/65495) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Fix kqueue descriptor ownership across watch replacement**

*Ensure kqueue watch replacements update descriptor ownership so stale subscriptions cannot close unrelated files or leak current descriptors.*

 * (4 days ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#65499](https://github.com/microsoft/TypeScript/pull/65499) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Fix JSDoc node types**

*Correct inaccurate JSDoc AST node type declarations, including restoring Identifier as a possible ModuleBody type in Strada.*

 * (4 days ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#65500](https://github.com/microsoft/TypeScript/pull/65500) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Preserve JSON\-RPC error details in string formatting**

*Correct the reversed JSON-RPC error string formatting logic so error details are preserved.*

 * (4 days ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#65503](https://github.com/microsoft/TypeScript/issues/65503) (Open, `Bug`, `Domain: API`)

**API client: concurrent \`Program\.getSourceFile\` calls for one file stampede the cache, each fetching the file whole**

*Concurrent `Program.getSourceFile` calls for the same file bypass in-flight caching, redundantly fetching and decoding the file multiple times.*

 * created by **SalvatorePreviti**
 * (today) **RyanCavanaugh** added labels `Bug`, `Domain: API`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#65505](https://github.com/microsoft/TypeScript/issues/65505) (Open, `Bug`, `Domain: LS: TSServer`)

**\`workspace/willRenameFiles\` panics with "changes overlap" when the renamed file is loaded by \`import\(\)\` with a \`\.ts\` specifier**

*Renaming a TypeScript file referenced by a dynamic `.ts` import causes `workspace/willRenameFiles` to generate overlapping edits and panic.*

 * created by **SalvatorePreviti**
 * (today) **RyanCavanaugh** added labels `Bug`, `Domain: LS: TSServer`, and set milestone to `Backlog`

### [PR microsoft/TypeScript#65506](https://github.com/microsoft/TypeScript/pull/65506) (Closed, `For Backlog Bug`)

**Clarify the error when an interface extends a constrained type parameter**

*Update TypeScript to report TS2884 identifying the type parameter when an interface extending a constrained type parameter fails base-type assignability.*

 * (3 days ago) **typescript-automation[bot]** added labels `For Backlog Bug`, `For Backlog Bug`
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/65506#issuecomment-6884129559) **Lior-Altarescu** said "@microsoft-github-policy-service agree"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#65507](https://github.com/microsoft/TypeScript/issues/65507) (Open, `Bug`, `Domain: JSDoc`)

**JSDoc \`\#\` link resolution behavior broke in TS 7**

*TypeScript 7 incorrectly resolves both JSDoc {@link Foo.member} and {@link Foo#member} links to the static member instead of distinguishing static and instance properties.*

 * created by **Gerrit0**
 * (today) **RyanCavanaugh** added labels `Bug`, `Domain: JSDoc`, and set milestone to `Backlog`

