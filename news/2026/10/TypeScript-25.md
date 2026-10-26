# Report for 2026-10-25 (Sunday, October 25th, 2026)

16 different users commented on 20 different issues.

## Recommended Actions

 * Response Recommended
    * @rf- reported that they pushed an update addressing all issues in [microsoft/TypeScript#64750](https://github.com/microsoft/TypeScript/pull/64750#issuecomment-6405051289)

## Activity Summary

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

### [Issue microsoft/TypeScript#64957](https://github.com/microsoft/TypeScript/issues/64957) (Open)

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

### [Issue microsoft/TypeScript#64959](https://github.com/microsoft/TypeScript/issues/64959) (Open)

**Preserve narrowing in closures for imports that resolve to \`const\` variables**

*Extend TypeScript’s constant variable narrowing inside nested closures to apply to imported values that resolve to const bindings.*

 * created by **mcmimik**

### [PR microsoft/TypeScript#64960](https://github.com/microsoft/TypeScript/pull/64960) (Open, `For Uncommitted Bug`)

** Fix auto\-import not offering unsaved exports after auto\-imports were computed**

*Delay bucket cleanup until multiple files are dirty to ensure auto-import suggestions include unsaved exports*

 * created by **1-DARK**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64960#issuecomment-6401269835) **1-DARK** said "@microsoft-github-policy-service agree"

### [Issue microsoft/TypeScript#64961](https://github.com/microsoft/TypeScript/issues/64961) (Open)

**/\*\* \*/ Style comments in code examples don't convert correctly**

*JavaDoc code snippets with inline /** */ comments are incorrectly rendered with escape characters instead of proper comment delimiters.*

 * created by **adligo**

### [PR microsoft/TypeScript#64962](https://github.com/microsoft/TypeScript/pull/64962) (Open, `For Uncommitted Bug`)

** Fix this type in object literal methods returned from async functions**

*Exclude PromiseLike from contextual types when returning object literals in async functions to fix incorrect this typing*

 * created by **1-DARK**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [PR microsoft/TypeScript#64963](https://github.com/microsoft/TypeScript/pull/64963) (Open, `For Uncommitted Bug`)

**fix\(64954\): exclude PromiseLike from contextual this in object literal methods**

*Exclude PromiseLike from the contextual this type in object literal methods returned by async functions.*

 * created by **servusdei2018**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [PR microsoft/TypeScript#64964](https://github.com/microsoft/TypeScript/pull/64964) (Open, `For Uncommitted Bug`)

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

### [Issue microsoft/TypeScript#64967](https://github.com/microsoft/TypeScript/issues/64967) (Open)

**Incremental builds miss diagnostics after UMD declaration changes**

*Incremental TypeScript builds fail to report updated type errors when UMD namespace declarations change.*

 * created by **Dunqing**

### [Issue microsoft/TypeScript#64968](https://github.com/microsoft/TypeScript/issues/64968) (Open)

**API scanner: a \`\#\` not followed by an identifier never advances, so \`scan\(\)\` loops forever**

*TypeScript's API scanner in 7.x loops infinitely on an isolated '#' because the token position isn't advanced properly.*

 * created by **knutwannheden**
 * [later](https://github.com/microsoft/TypeScript/issues/64968#issuecomment-6417855009) **MartinJohns** said "Sounds like a duplicate of #64490."

### [PR microsoft/TypeScript#64969](https://github.com/microsoft/TypeScript/pull/64969) (Open, `For Uncommitted Bug`)

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

