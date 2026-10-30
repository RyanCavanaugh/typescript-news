# Report for 2026-10-25 (Sunday, October 25th, 2026)

18 different users commented on 41 different issues.

## Recommended Actions

 * Response Recommended
    * @gadcam asked for CI reapproval in [microsoft/TypeScript#64729](https://github.com/microsoft/TypeScript/pull/64729#issuecomment-6420325668)
    * @rf- reported that they pushed an update addressing all issues in [microsoft/TypeScript#64750](https://github.com/microsoft/TypeScript/pull/64750#issuecomment-6405051289)

## Activity Summary

### [PR microsoft/TypeScript#64729](https://github.com/microsoft/TypeScript/pull/64729) (Open, `Domain: Performance`, `For Milestone Bug`, **gabritto**)

**Dedupe identical object literal types before subtype reduction**

*Deduplicate identical object literal types before subtype reduction to prevent O(n²) performance blow-ups when type-checking large JSON arrays*

 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64729#issuecomment-6134012975) **typescript-automation[bot]** reported tsc user test results and confirmed everything looked good
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64729#issuecomment-6134415656) **typescript-automation[bot]** reported that running the top 400 repos tsc comparison between baseline and pr succeeded without issues
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/64729#issuecomment-6363202221) **gadcam** said "@jakebailey The Oct 12 test run came back clean (perf neutral, DT / user tests / top400 unchanged). What do you think about this PR?"
 * [later](https://github.com/microsoft/TypeScript/pull/64729#issuecomment-6420325668) **gadcam** thanked gabritto for kicking off CI, explained failures from the recent merge, merged main and switched to accessors, confirmed tests passed, and asked for CI reapproval

### [PR microsoft/TypeScript#64748](https://github.com/microsoft/TypeScript/pull/64748) (Closed, `For Backlog Bug`)

**Fix broken augmentExportEquals2 test fixture**

*Removed duplicate //@filename: file3.ts directive in augmentExportEquals2 test to restore expected diagnostics.*

 * (1 week ago) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64748#issuecomment-6123625457) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (later) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`

### [PR microsoft/TypeScript#64750](https://github.com/microsoft/TypeScript/pull/64750) (Open, `For Uncommitted Bug`)

**Add support for Jujutsu conflict markers**

*Enhance the compiler scanner to recognize Jujutsu VCS conflict markers, handle varied marker lengths, and manage section state.*

 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64750#issuecomment-6159916825) **rf-** said "Good points, thanks @jakebailey! Apologies for not covering all of the possible formats, it definitely makes sense to do them all at once. I'll open an issue to ref in the PR."
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64750#issuecomment-6237153149) **rf-** questioned whether the couldStartTrivia function was vestigial dead code in Go and suggested its removal
 * [6 days ago](https://github.com/microsoft/TypeScript/pull/64750#issuecomment-6278628845) **jakebailey** said "I think we can probably just do the simple easy version of this and it be sufficient; this is a best effort recovery after all so I think that's ok."
 * [today](https://github.com/microsoft/TypeScript/pull/64750#issuecomment-6405051289) **rf-** explained that they implemented the correct solution and pushed an update addressing the issues

### [PR microsoft/TypeScript#64872](https://github.com/microsoft/TypeScript/pull/64872) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Use paged link stores for all symbol links**

*Use paged link stores for all symbol link types to reduce map lookups and improve performance at minimal memory cost.*

 * [6 days ago](https://github.com/microsoft/TypeScript/pull/64872#issuecomment-6273530369) **jakebailey** said "@typescript-bot perf test this faster"
 * [6 days ago](https://github.com/microsoft/TypeScript/pull/64872#issuecomment-6273532095) **typescript-automation[bot]** started CI jobs and provided a status table
 * [6 days ago](https://github.com/microsoft/TypeScript/pull/64872#issuecomment-6274246320) **typescript-automation[bot]** reported the results of the requested perf run
 * [later](https://github.com/microsoft/TypeScript/pull/64872#issuecomment-6413051384) **jakebailey** said "Closing; perf results don't justify it."
 * (later) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#64911](https://github.com/microsoft/TypeScript/issues/64911) (Open, `Bug`, `Domain: API`, `Crash`)

**API: \`snapshot\.update\` with both \`removePrograms\` and \`createPrograms\` crashes tsgo \(nil dereference in \`ProjectCollectionBuilder\.HandleAPIRequest\`\)**

*Using snapshot.update with both removePrograms and createPrograms causes a nil dereference panic in the TypeScript sync API*

 * created by **johnnyreilly**
 * (later) **RyanCavanaugh** added labels `Bug`, `Crash`, `Domain: API`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#64912](https://github.com/microsoft/TypeScript/issues/64912) (Open, `Needs Investigation`, **andrewbranch**)

**Content mappers: pass an import's query or attributes to \`transform\`**

*Allow content mappers to opt in to receiving import query parameters or import attributes in their transform calls to handle module variants.*

 * created by **colinhacks**
 * (later) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **andrewbranch**

### [Issue microsoft/TypeScript#64917](https://github.com/microsoft/TypeScript/issues/64917) (Closed, `Domain: Error Messages`, `Possible Improvement`)

**"Content mapper file extension '\.const\.json' is a built\-in extension and cannot be registered by a content mapper\." error is misleading**

*Error message incorrectly labels .const.json as a built-in extension instead of clarifying its conflict with .json or supporting .const.json patterns*

 * created by **DetachHead**
 * (later) **RyanCavanaugh** added labels `Domain: Error Messages`, `Possible Improvement`, and set milestone to `Backlog`

### [PR microsoft/TypeScript#64921](https://github.com/microsoft/TypeScript/pull/64921) (Closed, `For Backlog Bug`)

**Clarify error when content mapper extension ends in a built\-in extension**

*Change TS18066 diagnostic to clarify that content mapper extensions ending in built-in extensions are disallowed.*

 * (3 days ago) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/64921#issuecomment-6339608951) **govardhanchinta99** said "@microsoft-github-policy-service agree"
 * (later) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`

### [PR microsoft/TypeScript#64924](https://github.com/microsoft/TypeScript/pull/64924) (Closed, `For Backlog Bug`)

**Reuse this\-independent interface member instantiations**

*Reuse instantiations of interface members that don’t depend on `this` to avoid redundant allocations.*

 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/64924#issuecomment-6341312406) **777genius** said "@microsoft-github-policy-service agree"
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/64924#issuecomment-6344056899) **jakebailey** said "Are there any real world codebases that hit this? Note how none of our benchmarks were affected by that other PR"
 * (later) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`

### [Issue microsoft/TypeScript#64925](https://github.com/microsoft/TypeScript/issues/64925) (Open, `Domain: Performance`, `Possible Improvement`)

**Excess synthetic\-this member allocations in nongeneric mapped interface inheritance**

*The TypeScript compiler performs excessive synthetic 'this' member instantiations for nongeneric mapped interface inheritance, leading to unnecessary allocations.*

 * created by **777genius**
 * (later) **RyanCavanaugh** added labels `Possible Improvement`, `Domain: Performance`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#64927](https://github.com/microsoft/TypeScript/issues/64927) (Closed, `Bug`)

**augmentExportEquals2 fixture has a duplicate @filename directive**

*A duplicate @filename directive in the augmentExportEquals2 fixture causes file3.ts to be overwritten and errors to be ignored, which the PR corrects.*

 * created by **mahesh-desu**
 * (later) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`

### [PR microsoft/TypeScript#64928](https://github.com/microsoft/TypeScript/pull/64928) (Closed, `Domain: Performance`, `For Backlog Bug`)

**Reuse token lookup visitor across AST descent**

*Reuse a single NodeVisitor for each token lookup to reduce allocations and improve getTokenAtPosition performance.*

 * [3 days ago](https://github.com/microsoft/TypeScript/pull/64928#issuecomment-6350320210) **jakebailey** said "This is a microbenchmark but how did you decide to try and work on this?"
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/64928#issuecomment-6350406819) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/64928#issuecomment-6350722523) **Tom4ikss** described experimenting with native API type queries in a build-time i18n plugin to reduce type analysis cost, isolated repeated visitor construction in a benchmark, and reported reduced allocations and faster microbenchmark lookups but no clear full-workload timing improvement
 * (later) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`

### [Issue microsoft/TypeScript#64929](https://github.com/microsoft/TypeScript/issues/64929) (Closed, `Possible Improvement`)

**Native token lookup allocates a visitor on each AST descent step**

*astnav.getTokenAtPosition repeatedly allocates new NodeVisitor instances during AST descent, causing high allocations and performance overhead mitigated by reusing the visitor*

 * created by **Tom4ikss**
 * (later) **RyanCavanaugh** added label `Possible Improvement`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#64930](https://github.com/microsoft/TypeScript/issues/64930) (Open, `Bug`)

**7\.1 regression: circular type alias accepts an assignment it should reject \(opposite of \#64891\)**

*TypeScript 7.1 regressively accepts circular type alias assignments that should trigger TS2322 errors.*

 * created by **Nabil372**
 * (later) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`

### [PR microsoft/TypeScript#64935](https://github.com/microsoft/TypeScript/pull/64935) (Open, `For Backlog Bug`)

**Don't measure type parameters as independent through circular variance lookups**

*Correct circular variance computation to disallow incompatible assignments between mutually recursive type aliases.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/64935#issuecomment-6386240501) **typescript-automation[bot]** provided perf run results for @ahejlsberg
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64935#issuecomment-6386252039) **typescript-automation[bot]** reported differences in user test results comparing baseline and PR and requested review
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64935#issuecomment-6386813789) **typescript-automation[bot]** reported build errors for DIYgod/RSSHub and every-app/open-seo when comparing baseline and pr
 * (later) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/64935#issuecomment-6419965044) **microsoft-github-policy-service[bot]** prompted the user to review and agree to the Contributor License Agreement by replying with the appropriate command
 * [later](https://github.com/microsoft/TypeScript/pull/64935#issuecomment-6419965104) **microsoft-github-policy-service[bot]** prompted the user to review and agree to the Contributor License Agreement by replying with the appropriate command

### [Issue microsoft/TypeScript#64937](https://github.com/microsoft/TypeScript/issues/64937) (Open, `Bug`, `Domain: LS: Signature Help`)

**Signature help shows no JSDoc for a \`const\` with a function type annotation**

*Signature help in TypeScript 7 fails to display JSDoc descriptions for parameters of a const variable declared with a function type annotation.*

 * created by **andreww2012**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/64937#issuecomment-6382147151) **MadalinWolf** opened a PR to add a fallback for JSDoc retrieval from const declarations, added a regression test, and confirmed the focused test passed
 * (later) **RyanCavanaugh** added labels `Bug`, `Domain: LS: Signature Help`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#64938](https://github.com/microsoft/TypeScript/issues/64938) (Open, `Suggestion`)

**Defining a type with inferred generic parameters**

*Allow an infer keyword in generic type definitions to automatically inherit parameter constraints and defaults from referenced types.*

 * created by **denis-migdal**
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/64938#issuecomment-6371549094) **MartinJohns** said "Duplicate of #29469."
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/64938#issuecomment-6380324447) **denis-migdal** proposed a type inference proposal for generic constraints, outlined potential issues with backwards flow of constraints, and presented alternative syntax solutions
 * **RyanCavanaugh** added label `Suggestion`

### [Issue microsoft/TypeScript#64939](https://github.com/microsoft/TypeScript/issues/64939) (Open, `Bug`)

**Formatter README links rules\.ts and names createRulesMap, which the Go port does not have**

*The formatter README links to rules.ts and createRulesMap, which aren't in the Go port that uses rules.go, getRules, and buildRulesMap.*

 * created by **lgriffin**
 * (later) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`

### [PR microsoft/TypeScript#64940](https://github.com/microsoft/TypeScript/pull/64940) (Open, `For Backlog Bug`)

**Fix/format readme go names**

*Update internal/format/README.md to correct Go formatter links and rule names and add a test verifying README matches code*

 * created by **lgriffin**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/64940#issuecomment-6372282108) **lgriffin** said "@microsoft-github-policy-service agree"
 * (later) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`

### [PR microsoft/TypeScript#64941](https://github.com/microsoft/TypeScript/pull/64941) (Open, `For Backlog Bug`)

**Don't reuse removed synthetic program IDs in the same update**

*Ensure synthetic program IDs removed earlier in the same snapshot update aren’t reused to prevent nil dereference crashes*

 * created by **jackeddisciple**
 * (2 days ago) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * (later) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`

### [PR microsoft/TypeScript#64949](https://github.com/microsoft/TypeScript/pull/64949) (Open, `For Backlog Bug`)

**Fix signature help docs for const function types**

*Add fallback documentation lookup so JSDoc comments on const function type annotations appear in signature help.*

 * (yesterday) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64949#issuecomment-6382102547) **MadalinWolf** said "@microsoft-github-policy-service agree"
 * (later) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`

### [Issue microsoft/TypeScript#64957](https://github.com/microsoft/TypeScript/issues/64957) (Closed, `Question`)

**type Exclude on class hierarchy resolves to never**

*Excluding a subclass from a union of structurally identical classes unexpectedly resolves to never in TypeScript.*

 * created by **xtnw**
 * [today](https://github.com/microsoft/TypeScript/issues/64957#issuecomment-6398117465) **jcalz** explained that TypeScript uses structural typing, linked to the handbook, and stated that the observed behavior is intentional and not a bug
 * [today](https://github.com/microsoft/TypeScript/issues/64957#issuecomment-6401013445) **xtnw** noted that the behavior was intended and suggested closing the bug as wontfix
 * [today](https://github.com/microsoft/TypeScript/issues/64957#issuecomment-6401436606) **irfanstract** suggested adding private fields to classes to preserve type soundness without bloating runtime properties
 * [today](https://github.com/microsoft/TypeScript/issues/64957#issuecomment-6401749375) **jcalz** offered an alternative using type-only class fields and asked for a concrete use case to justify distinguishing structurally identical types

### [PR microsoft/TypeScript#64958](https://github.com/microsoft/TypeScript/pull/64958) (Closed, `For Uncommitted Bug`)

**Skip the narrowable\-reference walk of unions known to contain no type variables**

*Bypass narrowable-reference traversal for union types that contain no type variables to avoid unnecessary processing*

 * created by **Andarist**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64958#issuecomment-6399866512) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (later) **Andarist** closed the issue

### [Issue microsoft/TypeScript#64959](https://github.com/microsoft/TypeScript/issues/64959) (Open, `Suggestion`)

**Preserve narrowing in closures for imports that resolve to \`const\` variables**

*Extend TypeScript’s constant variable narrowing inside nested closures to apply to imported values that resolve to const bindings.*

 * created by **mcmimik**

### [PR microsoft/TypeScript#64960](https://github.com/microsoft/TypeScript/pull/64960) (Closed, `For Backlog Bug`)

** Fix auto\-import not offering unsaved exports after auto\-imports were computed**

*Delay bucket cleanup until multiple files are dirty to ensure auto-import suggestions include unsaved exports*

 * created by **1-DARK**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64960#issuecomment-6401269835) **1-DARK** said "@microsoft-github-policy-service agree"

### [Issue microsoft/TypeScript#64961](https://github.com/microsoft/TypeScript/issues/64961) (Open, `Possible Improvement`)

**/\*\* \*/ Style comments in code examples don't convert correctly**

*JavaDoc code snippets with inline /** */ comments are incorrectly rendered with escape characters instead of proper comment delimiters.*

 * created by **adligo**

### [PR microsoft/TypeScript#64962](https://github.com/microsoft/TypeScript/pull/64962) (Open, `For Backlog Bug`)

** Fix this type in object literal methods returned from async functions**

*Exclude PromiseLike from contextual types when returning object literals in async functions to fix incorrect this typing*

 * created by **1-DARK**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [PR microsoft/TypeScript#64963](https://github.com/microsoft/TypeScript/pull/64963) (Open, `For Backlog Bug`)

**fix\(64954\): exclude PromiseLike from contextual this in object literal methods**

*Exclude PromiseLike from the contextual this type in object literal methods returned by async functions.*

 * created by **servusdei2018**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [PR microsoft/TypeScript#64964](https://github.com/microsoft/TypeScript/pull/64964) (Closed, `Domain: Performance`, `For Uncommitted Bug`)

**Speed up union subset checks by scanning sorted constituents**

*Optimize subset checks on unions by scanning sorted constituent elements to improve performance.*

 * created by **Andarist**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64964#issuecomment-6404509771) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [later](https://github.com/microsoft/TypeScript/pull/64964#issuecomment-6410410676) **jakebailey** said "@typescript-bot perf test this faster"
 * [later](https://github.com/microsoft/TypeScript/pull/64964#issuecomment-6410412053) **typescript-automation[bot]** provided automated build status update including job start and result links
 * [later](https://github.com/microsoft/TypeScript/pull/64964#issuecomment-6410524011) **typescript-automation[bot]** said "@jakebailey, the perf run you requested failed. You can check the log here."

### [PR microsoft/TypeScript#64965](https://github.com/microsoft/TypeScript/pull/64965) (Open, `For Backlog Bug`)

**Fix assignment\-target detection through type assertions**

*Enable correct detection of assignments through 'as' and angle-bracket type assertions to prevent false TS2454 errors.*

 * created by **chengchuu**
 * (today) **typescript-automation[bot]** added labels `For Backlog Bug`, `For Backlog Bug`

### [PR microsoft/TypeScript#64966](https://github.com/microsoft/TypeScript/pull/64966) (Open, `For Uncommitted Bug`)

**Fix stale incremental diagnostics after UMD declaration changes**

*Ensure TypeScript’s incremental build invalidates diagnostics correctly after UMD ‘export as namespace’ declaration changes.*

 * created by **Dunqing**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64966#issuecomment-6409653023) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."

### [Issue microsoft/TypeScript#64967](https://github.com/microsoft/TypeScript/issues/64967) (Open, `Bug`, `Domain: tsc: --incremental`)

**Incremental builds miss diagnostics after UMD declaration changes**

*Incremental TypeScript builds fail to report updated type errors when UMD namespace declarations change.*

 * created by **Dunqing**

### [Issue microsoft/TypeScript#64968](https://github.com/microsoft/TypeScript/issues/64968) (Closed, `Duplicate`)

**API scanner: a \`\#\` not followed by an identifier never advances, so \`scan\(\)\` loops forever**

*TypeScript's API scanner in 7.x loops infinitely on an isolated '#' because the token position isn't advanced properly.*

 * created by **knutwannheden**
 * [later](https://github.com/microsoft/TypeScript/issues/64968#issuecomment-6417855009) **MartinJohns** said "Sounds like a duplicate of #64490."
 * **RyanCavanaugh** added label `Duplicate`

### [PR microsoft/TypeScript#64969](https://github.com/microsoft/TypeScript/pull/64969) (Closed, `For Uncommitted Bug`)

**Add a regression test for narrowing NoInfer union constituents of non\-generic aliases**

*Add a regression test to cover narrowing NoInfer union constituents in non-generic type aliases*

 * created by **Andarist**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/64969#issuecomment-6415926070) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."

### [PR microsoft/TypeScript#64970](https://github.com/microsoft/TypeScript/pull/64970) (Open, `For Backlog Bug`)

**Fix target library hints for readonly interfaces and tuples**

*Add missing target library hints for readonly interfaces and tuples to improve missing-property diagnostics.*

 * created by **maheshrijal**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/64970#issuecomment-6418171644) **maheshrijal** said "@microsoft-github-policy-service agree"

