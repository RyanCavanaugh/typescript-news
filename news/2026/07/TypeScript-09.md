# Report for 2026-07-09 (Thursday, July 9th, 2026)

5 different users commented on 16 different issues.

## Activity Summary

### [Issue microsoft/TypeScript#63092](https://github.com/microsoft/TypeScript/issues/63092) (Open, `Bug`, `Help Wanted`, `Domain: check: Control Flow`)

**Crash: RangeError: Maximum call stack size exceeded in isReachableFlowNodeWorker with complex for loop headers**

*TypeScript's compiler crashes with a maximum call stack size exceeded error when analyzing reachability in complex for loop headers.*

 * **RyanCavanaugh** added label `Domain: check: Control Flow`
 * [1 month ago](https://github.com/microsoft/TypeScript/issues/63092#issuecomment-4663552465) **RyanCavanaugh** referred to the contributing guidelines and reminded the user to develop in the typescript-go repo because the bug didn't meet the 6.0 patch bar
 * [1 month ago](https://github.com/microsoft/TypeScript/issues/63092#issuecomment-4679263794) **ibesuperv** submitted a fix in the typescript-go repository and asked for review
 * [later](https://github.com/microsoft/TypeScript/issues/63092#issuecomment-4935118862) **ibesuperv** explained that they accidentally synced their fork’s main branch and force-pushed over their work, causing the PR to close, and opened a fresh PR with an improved fix addressing all prior feedback

### [Issue microsoft/TypeScript#63129](https://github.com/microsoft/TypeScript/issues/63129) (Open, `Suggestion`, `Awaiting More Feedback`)

**TSC should not error on valid subpath specifier syntax \(TS2877\)**

*TypeScript 5.7 erroneously rejects valid non-relative subpath imports with '.ts' extensions by raising TS2877 errors.*

 * [20 weeks ago](https://github.com/microsoft/TypeScript/issues/63129#issuecomment-3899645745) **valler** said "Edit: no longer relevant. the best workaround so far follows in a later comment."
 * [20 weeks ago](https://github.com/microsoft/TypeScript/issues/63129#issuecomment-3899713546) **valler** said "Edit: no longer relevant. the best workaround so far follows in a later comment."
 * [20 weeks ago](https://github.com/microsoft/TypeScript/issues/63129#issuecomment-3900495979) **valler** said "Edit: no longer relevant. the best workaround so far follows in a later comment."
 * [today](https://github.com/microsoft/TypeScript/issues/63129#issuecomment-4928703170) **valler** described a workaround using an explicit .ts mapping to allow specifiers to end in .ts

### [Issue microsoft/TypeScript#63628](https://github.com/microsoft/TypeScript/issues/63628) (Open, `Bug`, `Domain: Error Messages`)

**Incorrect diagnostic message in TS2814**

*TS2814’s misleading error “Function with bodies can only merge with ambient classes” is shown when merging a body-less function declaration with a class.*

 * (2 days ago) **RyanCavanaugh** added label `Bug`, removed label `Not a Defect`, and set milestone to `Backlog`
 * **RyanCavanaugh** added label `Domain: Error Messages`

### [Issue microsoft/TypeScript#63637](https://github.com/microsoft/TypeScript/issues/63637) (Closed, `Question`)

**v7 missing GitHub releases**

*TypeScript v7.0.2 is missing from the main repository's GitHub releases page and appears only under typescript-go.*

 * [today](https://github.com/microsoft/TypeScript/issues/63637#issuecomment-4923612893) **hyunbinseo** asked about migration plans or interim package.json configuration
 * [today](https://github.com/microsoft/TypeScript/issues/63637#issuecomment-4923638845) **jakebailey** said "Bugs are fine to file here and that's the main place the project lives; is this causing a problem for you in some way?"
 * [today](https://github.com/microsoft/TypeScript/issues/63637#issuecomment-4923690763) **hyunbinseo** mentioned confusion about how to follow up with the v7 release and updated the issue body with a tl;dr section
 * **RyanCavanaugh** added label `Question`

### [PR microsoft/TypeScript#63638](https://github.com/microsoft/TypeScript/pull/63638) (Closed, `For Backlog Bug`, `Voight-Kampff Anomaly`)

**Fix inconsistent \`typeof this\` when \`this\` parameter comes from a contextual signature \(\#63616\)**

*TypeScript incorrectly resolves typeof this as the enclosing type instead of the contextual this in type queries.*

 * (today) **typescript-automation[bot]** added labels `For Backlog Bug`, `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63638#issuecomment-4924177988) **AmariahAK** said "@microsoft-github-policy-service agree"
 * **RyanCavanaugh** added label `Voight-Kampff Anomaly`

### [Issue microsoft/TypeScript#63640](https://github.com/microsoft/TypeScript/issues/63640) (Open)

**JSDoc for properties of intersected types is no longer merged**

*TypeScript 7.0.2 no longer merges JSDoc comments for identical properties in intersected types.*

 * created by **theblueplum**

### [Issue microsoft/TypeScript#63641](https://github.com/microsoft/TypeScript/issues/63641) (Open)

**Proposal: Export multiple, runtime\-specific declaration files**

*Enable exporting multiple runtime-specific TypeScript declaration files via package.json exports for platform-specific typing.*

 * created by **yassernasc**

### [Issue microsoft/TypeScript#63642](https://github.com/microsoft/TypeScript/issues/63642) (Open, `Bug`, `Domain: check: Control Flow`)

**TS2871 'always nullish' false positive on binding destructured from \.map over spread\-of\-union \(regression 5\.9\.3 → 6\.0\.3; also in 7\.0\.2\)**

*TypeScript 6.0.3 and 7.0.2 incorrectly report a map-destructured ternary over a spread union as always nullish.*

 * created by **nejim123**

