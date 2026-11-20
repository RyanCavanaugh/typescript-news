# Report for 2026-11-16 (Monday, November 16th, 2026)

18 different users commented on 81 different issues.

## Recommended Actions

 * Response Recommended
    * @kaya3 provided a clarification and reproduction demonstrating that a generic `fn<T>(x: T & 'a')` produced the same error in [microsoft/TypeScript#36772](https://github.com/microsoft/TypeScript/issues/36772#issuecomment-6925822684)
    * @sosoba asked whether the 7.1 release plan would be updated in [microsoft/TypeScript#63703](https://github.com/microsoft/TypeScript/issues/63703#issuecomment-6949297487)
    * @poveu reported that the memory leak also occurred in PhpStorm on Windows in [microsoft/TypeScript#64568](https://github.com/microsoft/TypeScript/issues/64568#issuecomment-6948739115)
    * @wickstudio provided the requested commit split and reported passing local tests in [microsoft/TypeScript#64900](https://github.com/microsoft/TypeScript/pull/64900#issuecomment-6938782055)
    * @pawangopallavudya-commits asked about the reason for closing PR #65527 and whether the fix was still needed in [microsoft/TypeScript#65527](https://github.com/microsoft/TypeScript/pull/65527#issuecomment-6951019295)
    * @Flarette reported a behavior change between versions 6.0.3 and 7.x that should be acknowledged in [microsoft/TypeScript#65530](https://github.com/microsoft/TypeScript/issues/65530#issuecomment-6927233524)
    * @zhengdaodeguL reported a fix with regression coverage and passing test results in [microsoft/TypeScript#65530](https://github.com/microsoft/TypeScript/issues/65530#issuecomment-6942120093)
    * @joshbarros provided the requested commit organization, expanded test coverage, and compiler-suite results in [microsoft/TypeScript#65539](https://github.com/microsoft/TypeScript/pull/65539#issuecomment-6926717230)

## Activity Summary

### [Issue microsoft/TypeScript#36772](https://github.com/microsoft/TypeScript/issues/36772) (Open, `Bug`, `Domain: check: Control Flow`, `Rescheduled`)

**Type not narrowed by === when equivalent type guard works**

*TypeScript fails to narrow a generic type parameter with a literal equality check, despite equivalent user-defined type guards narrowing it correctly.*

 * **typescript-bot** added label `Fix Available`
 * **jakebailey** removed label `Fix Available`
 * [yesterday](https://github.com/microsoft/TypeScript/issues/36772#issuecomment-6903191130) **gameroman** reported that narrowing only broke when the narrowed generic value was assigned to a new variable, and provided a TypeScript reproduction
 * [today](https://github.com/microsoft/TypeScript/issues/36772#issuecomment-6925822684) **kaya3** clarified that the reported narrowing issue differed from the example and showed that making `fn` generic reproduced the same error

### [Issue microsoft/TypeScript#63703](https://github.com/microsoft/TypeScript/issues/63703) (Open, `Planning`)

**TypeScript 7\.1 Iteration Plan**

*The TypeScript 7.1 iteration plan outlines release milestones and planned compiler, editor, library, API, and performance improvements.*

 * [1 month ago](https://github.com/microsoft/TypeScript/issues/63703#issuecomment-6276993692) **typescript-automation[bot]** said "Hey, @DanielRosenwasser! I've pulled main into release-7.1 for you."
 * [1 month ago](https://github.com/microsoft/TypeScript/issues/63703#issuecomment-6285163659) **erlichmen** asked when the TypeScript 7.1.0 beta would be published and whether users should build it from the `release-7.1` branch
 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/63703#issuecomment-6297602298) **DanielRosenwasser** announced that the beta was published, the blog post was available, and the v7.1-beta tag had been created
 * [later](https://github.com/microsoft/TypeScript/issues/63703#issuecomment-6949297487) **sosoba** asked whether the 7.1 RC and stable release plan would be updated

### [PR microsoft/TypeScript#64239](https://github.com/microsoft/TypeScript/pull/64239) (Closed, `For Uncommitted Bug`, **ahejlsberg**)

**Fixed a crash related to variadic tuple elements with intersections containing \`InstantiableNonPrimitive\`**

*Fixes a crash when variadic tuple elements involve intersections containing `InstantiableNonPrimitive`.*

 * created by **Andarist**
 * (9 weeks ago) **typescript-automation[bot]** added label `For Uncommitted Bug`, and assigned to **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript/pull/64239#issuecomment-6940209441) **jakebailey** suggested adding a test case for the issue found in #65064 and described the differing inferred types on main versus the proposed fix

### [Issue microsoft/TypeScript#64431](https://github.com/microsoft/TypeScript/issues/64431) (Closed, `Bug`, **RyanCavanaugh**, **Copilot**)

**TS7031 false positive for nested object binding pattern with \`= {}\` default in an annotated parameter \(regression from \#64043\)**

*Regression causes TS7031 false positives for nested object destructuring defaults in explicitly annotated parameters.*

 * [5 weeks ago](https://github.com/microsoft/TypeScript/issues/64431#issuecomment-6041533127) **Konan69** reported that TS7031 also affected unannotated but contextually typed top-level destructured parameters, provided reproduction cases and version details, and noted that PRs #64440 and #64671 resolved the cases while suggesting additional tests
 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/64431#issuecomment-6297398470) **connorshea** reported encountering the same issue in a work application with TypeScript 7.1, noting it was absent in the 7.0 native preview and was their only observed regression
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/64431#issuecomment-6610691604) **connorshea** provided a reproduction case showing that TypeScript 7.1.0-dev reported implicit-`any` errors for nested destructured properties that were error-free in TypeScript 7.0.2, and mentioned a non-ideal type-cast workaround
 * [today](https://github.com/microsoft/TypeScript/issues/64431#issuecomment-6926736232) **abrahamguo** reported that the regression reproduced without annotations when a parameter type came from context, bisected it to #64043, and asked whether it could be fixed or reverted before the 7.1.0 release
 * [today](https://github.com/microsoft/TypeScript/issues/64431#issuecomment-6926949090) **jakebailey** said "I did not even know about this issue or that I caused it. I will take a look."
 * [today](https://github.com/microsoft/TypeScript/issues/64431#issuecomment-6927187337) **trevorade** mentioned that validation of tsgo against Google’s TypeScript codebase uncovered potentially overlooked regressions and linked issues 64437, 64673, and 64453 for review

### [Issue microsoft/TypeScript#64568](https://github.com/microsoft/TypeScript/issues/64568) (Closed)

**Bug Report: Severe memory leak triggered by "TypeScript \(Native Preview\)" extension**

*The TypeScript Native Preview extension causes an unrecoverable memory leak in empty projects near other Git repositories, unless a package.json exists.*

 * [1 week ago](https://github.com/microsoft/TypeScript/issues/64568#issuecomment-6751667502) **RyanCavanaugh** reported that many memory issues had been fixed and that long synthetic LSP sessions showed stable memory usage, then requested a new issue with a concrete reproduction if the problem persisted
 * (1 week ago) **RyanCavanaugh** closed the issue
 * [6 days ago](https://github.com/microsoft/TypeScript/issues/64568#issuecomment-6772488856) **KostyaTretyak** confirmed that the issue remained relevant and expressed frustration about having to repeat the report
 * [later](https://github.com/microsoft/TypeScript/issues/64568#issuecomment-6948739115) **poveu** mentioned that the same memory leak issue occurred in PhpStorm on Windows and included a screenshot

### [Issue microsoft/TypeScript#64692](https://github.com/microsoft/TypeScript/issues/64692) (Closed, `Domain: Performance`, `Possible Improvement`, **ahejlsberg**)

**\[7\.0 regression\] Object literal passed to a method on a large union creates exponentially many types \(type order dependent\)**

*TypeScript 7.0 regresses when contextualizing object literals for methods on large unions, causing type explosions, excessive memory use, and order-dependent performance.*

 * created by **ctriley**
 * (5 weeks ago) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **ahejlsberg**
 * (today) **ahejlsberg** added labels `Domain: Performance`, `Possible Improvement`, and removed label `Needs Investigation`
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript#64900](https://github.com/microsoft/TypeScript/pull/64900) (Open, `For Backlog Bug`)

**Fix unused renaming detection in function types**

*Correct unused-renaming detection so type-only references in generic function types do not suppress diagnostics for unused destructured value bindings.*

 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [3 weeks ago](https://github.com/microsoft/TypeScript/pull/64900#issuecomment-6317648836) **wickstudio** said "@microsoft-github-policy-service agree"
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/64900#issuecomment-6862090261) **jakebailey** suggested splitting the changes into separate commits for the failing test and baseline, followed by the fix and updated baseline
 * [today](https://github.com/microsoft/TypeScript/pull/64900#issuecomment-6938782055) **wickstudio** split the changes into two commits, adding the regression test with the original baseline first and the fix with the updated baseline second, and reported that all local tests passed

### [Issue microsoft/TypeScript#64998](https://github.com/microsoft/TypeScript/issues/64998) (Open, `Bug`, `Domain: check: Order Dependence`)

**declaration emit depends on checker assignment; a type alias becomes \`any\` with no error**

*Multi-threaded declaration emit nondeterministically infers a type alias as `any` without diagnostics, unlike single-threaded emit.*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [6 days ago](https://github.com/microsoft/TypeScript/issues/64998#issuecomment-6782159932) **RyanCavanaugh** said "Should be fixed by #65293"
 * [6 days ago](https://github.com/microsoft/TypeScript/issues/64998#issuecomment-6782173572) **jakebailey** said "Sadly @blickly already confirmed it does not, which is scary"
 * [today](https://github.com/microsoft/TypeScript/issues/64998#issuecomment-6932850442) **blickly** reported that #65293 fixed the issue at commit 9a2e423, but identified a separate checker-count-dependent issue and filed it as #65543

### [PR microsoft/TypeScript#65026](https://github.com/microsoft/TypeScript/pull/65026) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Create decl emit accessibility diagnostic closures lazily**

*Optimize declaration emit by lazily creating accessibility diagnostic closures and replacing per-node cleanup closures with compact saved context.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/65026#issuecomment-6507381323) **typescript-automation[bot]** reported that the performance test job had started and linked to its build results
 * **jakebailey** added label `Domain: Performance`
 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/65026#issuecomment-6508622525) **typescript-automation[bot]** provided the requested performance run results, including a baseline-to-PR comparison for the TypeScript compiler
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#65064](https://github.com/microsoft/TypeScript/pull/65064) (Open, `Author: Team`, `For Milestone Bug`, `For Backlog Bug`, **jakebailey**)

**\[experiment\] fully order independent type checking**

*Proposes making type checking fully order-independent, with randomized ordering tests and extensive fixes for cache, traversal, and identifier-dependent behavior.*

 * [3 days ago](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6872486023) **typescript-automation[bot]** reported that the DT tests completed and exposed a branch-only TypeScript compile error in d3-selection involving incompatible TransitionLike element types
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6872500310) **typescript-automation[bot]** reported new TypeScript test errors in `SchemaAST.ts` when comparing the baseline and PR results, and asked maintainers to investigate
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6873157202) **typescript-automation[bot]** said "@jakebailey, the perf run you requested failed. You can check the log here."
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6933487784) **jakebailey** requested TypeScript bot runs for dt, user testing, top1000 testing, and performance testing
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6933490045) **typescript-automation[bot]** reported that automated jobs started, with results available for differential testing, user testing, top-1000 testing, and performance testing; the performance test reported failure
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6934032348) **typescript-automation[bot]** reported that the DT tests produced a new d3-selection type-checking error at d3-selection-tests.ts:1502 involving an incompatible TransitionLike<HTMLParagraphElement, number> return type
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6934396913) **typescript-automation[bot]** reported new TypeScript errors found when comparing user test results between the baseline and pull request, and asked Jake Bailey to investigate
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6935291785) **typescript-automation[bot]** said "@jakebailey, the perf run you requested failed. You can check the log here."
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6936707599) **typescript-automation[bot]** reported unexpected baseline-versus-PR `tsc` changes found while testing the top 1,000 repositories and asked @jakebailey to investigate

### [Issue microsoft/TypeScript#65118](https://github.com/microsoft/TypeScript/issues/65118) (Open, `Suggestion`)

**Let a module augmentation with a wildcard add to every file it matches**

*Allow wildcard module augmentations to add declared exports to every matching resolved module, supporting build-tool-generated exports.*

 * created by **alvaro-cuesta**
 * **RyanCavanaugh** added label `Suggestion`

### [Issue microsoft/TypeScript#65300](https://github.com/microsoft/TypeScript/issues/65300) (Open, `Bug`, `Domain: API`)

**\[api\] Concurrent createSnapshot calls can deadlock on projects entering one extends cycle**

*Concurrent asynchronous createSnapshot calls can deadlock when projects reference configurations involved in a circular extends chain.*

 * created by **cplieger**
 * (today) **RyanCavanaugh** added labels `Bug`, `Domain: API`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#65301](https://github.com/microsoft/TypeScript/issues/65301) (Open, `Bug`, `Domain: API`)

**\[api\] createSnapshot drops options a project inherits through a circular extends chain**

*The synchronous createSnapshot API loses inherited compiler options such as strict when projects use circular extends chains and are opened together.*

 * created by **cplieger**
 * (today) **RyanCavanaugh** added labels `Bug`, `Domain: API`, and set milestone to `Backlog`

### [PR microsoft/TypeScript#65302](https://github.com/microsoft/TypeScript/pull/65302) (Open, `For Backlog Bug`)

**\[api\] Parse a new owner cache entry without holding its lock**

*Avoid deadlocks in OwnerCache by parsing new or expired entries without holding their locks, while preserving first-stored values.*

 * created by **cplieger**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (today) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`

### [PR microsoft/TypeScript#65303](https://github.com/microsoft/TypeScript/pull/65303) (Open, `For Backlog Bug`)

**\[api\] Reparse extended configs cached under another resolution stack**

*Reparse cached extended configurations when resolution-stack cycles differ, preventing circular extends from producing incomplete compiler options in the API.*

 * created by **cplieger**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (today) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`

### [Issue microsoft/TypeScript#65313](https://github.com/microsoft/TypeScript/issues/65313) (Open, `Suggestion`)

**Content mappers for tagged template literals**

*Request support for content mappers that type-check embedded languages in tagged template literals without changing emitted JavaScript.*

 * created by **OliverJAsh**
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/65313#issuecomment-6632676916) **hkleungai** suggested considering existing IDE syntax-highlighting extensions and supporting jsdoc-style directives on ordinary multiline strings in addition to tagged template literals
 * **RyanCavanaugh** added label `Suggestion`

### [Issue microsoft/TypeScript#65339](https://github.com/microsoft/TypeScript/issues/65339) (Closed, `Bug`, `Domain: lib.d.ts`)

**ESNext\.SharedMemory still declares the removed Atomics\.pause parameter**

*Update the ESNext.SharedMemory declaration so Atomics.pause() accepts no arguments, matching the ECMAScript specification.*

 * (1 week ago) **RyanCavanaugh** added labels `Bug`, `Domain: lib.d.ts`, and set milestone to `Backlog`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#65352](https://github.com/microsoft/TypeScript/pull/65352) (Closed, `For Backlog Bug`)

**lib: remove obsolete Atomics\.pause parameter**

*Remove the obsolete optional parameter from the Atomics.pause declaration and update conformance baselines to expect TS2554 for argument-bearing calls.*

 * (1 week ago) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/65352#issuecomment-6819927705) **JemmyIndex** reported that the concurrent test job failed due to a transient download error from proxy.golang.org, noted that all other checks passed, and requested rerunning the failed jobs
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#65354](https://github.com/microsoft/TypeScript/pull/65354) (Closed, `Author: Team`, `For Uncommitted Bug`)

**Update localization files**

*Update localization handbacks and regenerate their corresponding runtime artifacts.*

 * created by **typescript-automation[bot]**
 * (1 week ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#65454](https://github.com/microsoft/TypeScript/pull/65454) (Closed, `For Backlog Bug`)

**fix: detect Unicode line separators in ASI diagnostics**

*Fix accidental-call diagnostics to recognize multi-byte Unicode line separators by decoding the final UTF-8 rune before ASI checks.*

 * created by **falakahuja**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/65454#issuecomment-6828429172) **falakahuja** said "@microsoft-github-policy-service agree"
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#65459](https://github.com/microsoft/TypeScript/pull/65459) (Closed, `For Uncommitted Bug`)

**Fix checker crash when sync iteration awaits an invalid thenable**

*Fixes a checker crash when sync iteration awaits invalid thenables by supplying construct-specific diagnostics for yield*, for-await, and direct yield.*

 * created by **joshbarros**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/65459#issuecomment-6838051625) **joshbarros** said "@microsoft-github-policy-service agree"
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#65460](https://github.com/microsoft/TypeScript/pull/65460) (Closed, `For Uncommitted Bug`)

**Preserve U\+FEFF when Wtf8Decoder reads payload text**

*Make Wtf8Decoder preserve leading U+FEFF characters, including those following lone surrogates, by defaulting ignoreBOM to true.*

 * **joshbarros** added label `For Uncommitted Bug`
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/65460#issuecomment-6838052128) **joshbarros** said "@microsoft-github-policy-service agree"
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/65460#issuecomment-6838095276) **joshbarros** said "This PR references #65458 (Fixes #65458 in the description), so it already has a linked issue."
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#65461](https://github.com/microsoft/TypeScript/pull/65461) (Closed, `For Backlog Bug`)

**Fix ASI diagnostics for Unicode line separators \(U\+2028 and U\+2029\)**

*Fix ASI diagnostics and source-position tracking for ECMAScript Unicode line separators U+2028 and U+2029 across compiler and language services.*

 * created by **amr807**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/65461#issuecomment-6841292026) **amr807** said "@microsoft-github-policy-service agree"
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#65467](https://github.com/microsoft/TypeScript/pull/65467) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Bind every destructured parameter in node\-builder scopes**

*Ensure all destructured parameters are bound in node-builder scopes to prevent incorrect declaration emission and global name resolution.*

 * (4 days ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#65510](https://github.com/microsoft/TypeScript/pull/65510) (Open, `Domain: Performance`, `For Milestone Bug`, `For Backlog Bug`, **johnfav03**)

**Reject structurally incomplete type arguments in expressions**

*Reject structurally incomplete speculative type arguments so relational expressions parse correctly while preserving valid generics, diagnostics, and parser performance.*

 * (yesterday) **typescript-automation[bot]** added labels `For Backlog Bug`, `For Milestone Bug`, and assigned to **johnfav03**
 * [today](https://github.com/microsoft/TypeScript/pull/65510#issuecomment-6936175496) **magic-akari** acknowledged that the implementation was more complex than expected because it needed to preserve TypeScript’s error recovery and invalid-input compatibility

### [Issue microsoft/TypeScript#65513](https://github.com/microsoft/TypeScript/issues/65513) (Open, `Bug`)

**Object\-rest for\-of lowering skips transformations on direct body statements**

*Object-rest lowering skips transformations for direct statements in for-of bodies, producing invalid loop initializers and broken function declarations.*

 * created by **Vl4dC**
 * (today) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`

### [PR microsoft/TypeScript#65519](https://github.com/microsoft/TypeScript/pull/65519) (Closed, `For Backlog Bug`)

**Fix object rest for\-of lowering skipping direct body statement transformation**

*Fix for-of lowering to transform direct body statements, correctly handling nested object-rest loops and function declarations for pre-ES2018 targets.*

 * created by **zhengdaodeguL**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (today) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`

### [PR microsoft/TypeScript#65522](https://github.com/microsoft/TypeScript/pull/65522) (Closed, `For Uncommitted Bug`)

**Remove GetProjectReferenceFromSource from printer\.EmitHost**

*Remove GetProjectReferenceFromSource from printer.EmitHost to prevent unnecessary dependencies and case-insensitive vendoring conflicts.*

 * created by **zhengdaodeguL**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#65527](https://github.com/microsoft/TypeScript/pull/65527) (Closed, `For Backlog Bug`)

**Fix semicolon hints after Unicode line separators**

*Update SkipTriviaEx to recognize Unicode line separators and decode runes so semicolon hints appear correctly, with regression tests for U+2028 and U+2029.*

 * created by **pawangopallavudya-commits**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * (today) **RyanCavanaugh** closed the issue
 * [later](https://github.com/microsoft/TypeScript/pull/65527#issuecomment-6951019295) **pawangopallavudya-commits** asked why PR #65527 was closed without being merged and offered to make changes based on feedback
 * [later](https://github.com/microsoft/TypeScript/pull/65527#issuecomment-6953243859) **RyanCavanaugh** said "@pawangopallavudya-commits read the issue that you are fixing..."

### [PR microsoft/TypeScript#65528](https://github.com/microsoft/TypeScript/pull/65528) (Closed, `Author: Team`, `For Uncommitted Bug`, **RyanCavanaugh**)

**Update repo docs re: AI activity**

*Update repository documentation to clarify acceptable AI-assisted contributions, discourage spam and excessive issue text, and add AGENTS.md guidance.*

 * created by **RyanCavanaugh**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript/pull/65528#issuecomment-6923315228) **jakebailey** said "Unfortunately I worry that strengthening these instructions will be just hurt local dev, as it did for DT"

### [PR microsoft/TypeScript#65529](https://github.com/microsoft/TypeScript/pull/65529) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **ahejlsberg**)

**Optimize \`getPropertiesOfUnionOrIntersectionType\`**

*Optimize union property resolution by using the constituent with the fewest properties and no index signatures as the representative.*

 * created by **ahejlsberg**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript/pull/65529#issuecomment-6922467827) **ahejlsberg** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/65529#issuecomment-6922471527) **typescript-automation[bot]** reported that the requested test jobs started, with three completing successfully and the performance test completing with errors
 * [today](https://github.com/microsoft/TypeScript/pull/65529#issuecomment-6923235248) **typescript-automation[bot]** reported that the user tests comparing the baseline and PR with tsc passed and everything looked good
 * [today](https://github.com/microsoft/TypeScript/pull/65529#issuecomment-6923260138) **typescript-automation[bot]** reported that the DT test results were ready and unchanged, with a link to the build log
 * [today](https://github.com/microsoft/TypeScript/pull/65529#issuecomment-6924571642) **typescript-automation[bot]** reported that testing the top 400 repositories with `tsc` showed no differences between the baseline and PR and that everything looked good
 * [today](https://github.com/microsoft/TypeScript/pull/65529#issuecomment-6924717055) **ahejlsberg** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/65529#issuecomment-6924719298) **typescript-automation[bot]** reported that the performance test job started and produced results
 * [today](https://github.com/microsoft/TypeScript/pull/65529#issuecomment-6924746663) **typescript-automation[bot]** said "@ahejlsberg, the perf run you requested failed. You can check the log here."
 * [today](https://github.com/microsoft/TypeScript/pull/65529#issuecomment-6926666692) **typescript-automation[bot]** reported that the requested performance run results were available and included compiler comparison metrics for the baseline and PR
 * [today](https://github.com/microsoft/TypeScript/pull/65529#issuecomment-6926749115) **typescript-automation[bot]** said "@ahejlsberg, the perf run you requested failed. You can check the log here."
 * [today](https://github.com/microsoft/TypeScript/pull/65529#issuecomment-6931104133) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/65529#issuecomment-6931106373) **typescript-automation[bot]** reported that the performance test job started and linked to its results
 * (today) **ahejlsberg** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/65529#issuecomment-6931828087) **typescript-automation[bot]** provided the requested performance run results comparing the baseline and PR, including compiler metrics

### [Issue microsoft/TypeScript#65530](https://github.com/microsoft/TypeScript/issues/65530) (Open, `Bug`, `Domain: check: Contextual Types`)

**TS7 regression: callback parameter loses contextual type \(TS7006\) for a computed \`string\` key when the type parameter's constraint references itself**

*TypeScript 7 introduces a regression where callbacks for computed string keys lose contextual typing and trigger TS7006 under self-referential constraints.*

 * created by **Flarette**
 * [today](https://github.com/microsoft/TypeScript/issues/65530#issuecomment-6927233524) **Flarette** explained that the issue no longer blocked them because the library removed the circular constraint, while reporting a behavior change between 6.0.3 and 7.x on identical input
 * [today](https://github.com/microsoft/TypeScript/issues/65530#issuecomment-6942120093) **zhengdaodeguL** reported that #65546 fixed erroneous index-signature synthesis for circular mapped-type constraints, preserved legitimate behaviors, and added passing regression tests

### [PR microsoft/TypeScript#65531](https://github.com/microsoft/TypeScript/pull/65531) (Closed, `For Uncommitted Bug`)

**Compare document highlight URIs by file path**

*Compare document highlight URIs by normalized file path to preserve highlights for paths containing unescaped characters such as `@`.*

 * created by **joshbarros**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#65532](https://github.com/microsoft/TypeScript/pull/65532) (Closed, `For Uncommitted Bug`)

**Return null from the remaining content\-mapper fallbacks**

*Extend content-mapper fallback handling so additional LSP requests return null when mappers are unregistered while files remain open.*

 * created by **joshbarros**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#65533](https://github.com/microsoft/TypeScript/pull/65533) (Closed, `For Uncommitted Bug`)

**Deduplicate call hierarchy call\-site ranges**

*Deduplicate identical call-site ranges in call hierarchy incoming and outgoing call responses.*

 * created by **joshbarros**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#65534](https://github.com/microsoft/TypeScript/pull/65534) (Closed, `For Uncommitted Bug`)

**Ignore the synthetic this parameter when matching JSDoc params**

*Fix JSDoc parameter matching to ignore synthetic or explicit `this` parameters, preventing false diagnostics and missing types for subsequent parameters.*

 * created by **joshbarros**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#65535](https://github.com/microsoft/TypeScript/pull/65535) (Closed, `For Uncommitted Bug`)

**Use the symbol name for the rename placeholder**

*Use the unquoted symbol name as the prepare-rename placeholder for quoted or computed property names.*

 * created by **joshbarros**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#65536](https://github.com/microsoft/TypeScript/pull/65536) (Closed, `For Uncommitted Bug`)

**Visit each dynamic import once when the specifier contains import**

*Ensure dynamic imports are visited once when specifiers contain “import,” preventing duplicate edits and overlapping-change panics during file renames.*

 * created by **joshbarros**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#65537](https://github.com/microsoft/TypeScript/pull/65537) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Parse JSDoc \`@augments\` and \`@implements\` as TypeReference**

*Parse JSDoc `@augments` and `@implements` tags as `TypeReference` nodes, simplifying AST handling and correcting invalid `@extends` diagnostics.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#65538](https://github.com/microsoft/TypeScript/pull/65538) (Closed, `For Uncommitted Bug`)

**Guard the string table reuse bounds for normalized literals**

*Prevent string table reuse from slicing with negative bounds when normalized numeric literals exceed their source spelling.*

 * created by **joshbarros**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#65539](https://github.com/microsoft/TypeScript/pull/65539) (Closed, `For Milestone Bug`)

**Pass undefined for jsxDEV self inside super arguments**

*Fix the react-jsxdev transform to pass `void 0` instead of `this` for `__self` when JSX appears in `super()` arguments.*

 * created by **joshbarros**
 * **typescript-automation[bot]** added label `For Milestone Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/65539#issuecomment-6926566990) **jakebailey** suggested splitting the changes into separate commits for the failing test and baseline, followed by the fix and updated baseline
 * [today](https://github.com/microsoft/TypeScript/pull/65539#issuecomment-6926717230) **joshbarros** split the changes into separate test/baseline and fix commits, added coverage for nested super and this-scope cases, and reported that the full compiler suite passed
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#65540](https://github.com/microsoft/TypeScript/pull/65540) (Closed, `For Uncommitted Bug`)

**Use an indirect call for wrapped imported callees**

*Ensure CommonJS transforms emit indirect calls for imported functions wrapped in parentheses, assertions, non-null, satisfies, or tagged-template expressions.*

 * created by **joshbarros**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#65541](https://github.com/microsoft/TypeScript/pull/65541) (Closed, `For Uncommitted Bug`)

**PERMISSION PROBE**

*Requests a permission probe without providing additional context or specifying an intended change.*

 * created by **zhengdaodeguL**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/65541#issuecomment-6928544987) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (today) **zhengdaodeguL** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/65541#issuecomment-6928783756) **RyanCavanaugh** said "?"

### [PR microsoft/TypeScript#65542](https://github.com/microsoft/TypeScript/pull/65542) (Closed, `Author: Team`, `For Backlog Bug`, **jakebailey**, **RyanCavanaugh**)

**Skip default padding for params with declared/contextual types**

*Skip padding object and tuple defaults for parameters with declared, JSDoc, or contextual types to prevent spurious implicit-any errors and incorrect inferred types.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Backlog Bug`, and assigned to **jakebailey**, **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript/pull/65542#issuecomment-6933468445) **jakebailey** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/65542#issuecomment-6933470351) **typescript-automation[bot]** reported the start and results of automated test, user test, DefinitelyTyped, and performance test jobs
 * [today](https://github.com/microsoft/TypeScript/pull/65542#issuecomment-6933981260) **typescript-automation[bot]** reported that the DT test results were ready and unchanged
 * [today](https://github.com/microsoft/TypeScript/pull/65542#issuecomment-6934051151) **typescript-automation[bot]** reported that user tests comparing the baseline and PR with tsc passed successfully
 * [today](https://github.com/microsoft/TypeScript/pull/65542#issuecomment-6934206407) **typescript-automation[bot]** reported that the requested performance run results were available and included a baseline-versus-PR comparison
 * [today](https://github.com/microsoft/TypeScript/pull/65542#issuecomment-6935214503) **typescript-automation[bot]** reported that testing the top 400 repositories with tsc showed no differences between the baseline and PR, with everything looking good

### [Issue microsoft/TypeScript#65543](https://github.com/microsoft/TypeScript/issues/65543) (Open, `Bug`, `Domain: check: Order Dependence`, **jakebailey**)

**TS2322 missed with 3\+ checkers: \`keyof\` depends on checker assignment when an interface's index signature uses its own \`keyof\`**

*TypeScript inconsistently misses TS2322 for a self-referential `keyof` index signature depending on the number of parallel checkers.*

 * created by **blickly**
 * [today](https://github.com/microsoft/TypeScript/issues/65543#issuecomment-6933973667) **jakebailey** said "This is a one line fix in #65293 but I don't think it's fixable in main in the same way."
 * [today](https://github.com/microsoft/TypeScript/issues/65543#issuecomment-6934293160) **blickly** said "Great to hear.  I can't wait for https://github.com/microsoft/TypeScript/pull/65293"
 * [today](https://github.com/microsoft/TypeScript/issues/65543#issuecomment-6934301340) **jakebailey** said "Unfortunately I wouldn't expect it for 7.1"

### [PR microsoft/TypeScript#65544](https://github.com/microsoft/TypeScript/pull/65544) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**, **RyanCavanaugh**)

**Bound printing of deferred array and tuple references by their node**

*Ensure deferred array and tuple type references are bounded by their node after type references are checked first.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**, **RyanCavanaugh**

### [PR microsoft/TypeScript#65545](https://github.com/microsoft/TypeScript/pull/65545) (Closed, `Author: Team`, `For Uncommitted Bug`)

**Update localization files**

*Update localization handbacks and regenerate their corresponding runtime artifacts.*

 * created by **typescript-automation[bot]**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`

### [PR microsoft/TypeScript#65546](https://github.com/microsoft/TypeScript/pull/65546) (Closed, `For Backlog Bug`)

**Fix contextual typing loss for computed string keys under circular mapped\-type key constraints \(Fixes \#65530\)**

*Fix contextual typing for computed string keys by preventing circular mapped-type constraints from generating spurious undefined index signatures.*

 * created by **zhengdaodeguL**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [Issue microsoft/TypeScript#65547](https://github.com/microsoft/TypeScript/issues/65547) (Closed, `Bug`, `Domain: Content Mappers`, **DanielRosenwasser**, **Copilot**)

**LSP panics with "slice bounds out of range" after a content mapper fails**

*The LSP panics with a slice-bounds error when handling hover or inlay hints after a content mapper fails during project opening.*

 * created by **auvred**

### [PR microsoft/TypeScript#65548](https://github.com/microsoft/TypeScript/pull/65548) (Open, `Domain: Performance`, `For Uncommitted Bug`)

**Skip the combined\-constraint check for a dedicated variance relationship**

*Introduce a dedicated variance-assignability relationship to prevent unbounded combined-constraint recursion and out-of-memory failures during variance measurement.*

 * created by **Amatewasu**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

