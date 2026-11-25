# Report for 2026-11-22 (Sunday, November 22nd, 2026)

11 different users commented on 16 different issues.

## Recommended Actions

 * Response Recommended
    * @michal-kocarek provided a workaround and relevant information about stale outputs and watch-mode support in [microsoft/TypeScript#61056](https://github.com/microsoft/TypeScript/issues/61056#issuecomment-7082034693)
    * @mhmdazkanfl provided detailed reproduction steps and identified a likely Windows file URI encoding difference causing the document highlight failure in [microsoft/TypeScript#64758](https://github.com/microsoft/TypeScript/issues/64758#issuecomment-7094041981)
    * @mhmdazkanfl asked whether a maintainer could assign the Backlog milestone to indicate that a community pull request was welcome in [microsoft/TypeScript#64758](https://github.com/microsoft/TypeScript/issues/64758#issuecomment-7094508196)
    * @MAST1999 provided confirmation, detailed reproduction and impact data for the TypeScript 7.1.0-beta regression, and shared a workaround for @tanstack/db users in [microsoft/TypeScript#64930](https://github.com/microsoft/TypeScript/issues/64930#issuecomment-7095234173)

## Activity Summary

### [Issue microsoft/TypeScript#61056](https://github.com/microsoft/TypeScript/issues/61056) (Closed, `Suggestion`, `Out of Scope`)

**Tsc does not behave correctly when files are moved or deleted**

*Tsc fails to remove outputs for deleted or moved source files, causing stale artifacts to override new modules, especially in watch mode.*

 * [1.8 years ago](https://github.com/microsoft/TypeScript/issues/61056#issuecomment-2620057509) **bdwain** explained that the behavior was widely used and supported by TypeScript, but offered to close the issue and build a custom watcher if it would not be supported
 * [1.8 years ago](https://github.com/microsoft/TypeScript/issues/61056#issuecomment-2626097932) **typescript-bot** said "This issue has been marked as "Out of Scope" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (1.8 years ago) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/issues/61056#issuecomment-7082034693) **michal-kocarek** shared a tool called tsc-after that removed stale output files while preserving incremental build artifacts, and mentioned a promising watch-mode PR

### [Issue microsoft/TypeScript#64690](https://github.com/microsoft/TypeScript/issues/64690) (Closed, `Bug`, **ahejlsberg**)

**TS2322: \`const\` type parameter infers \`readonly \[\]\`, rejected through a union return type \(7\.1\.0\-dev regression from typescript\-go\#4591\)**

*TypeScript 7.1 nightly regresses by inferring `ok([])` as `Ok<readonly []>`, rejecting valid assignment to `Ok<string[]> | Err<string>`.*

 * (5 weeks ago) **RyanCavanaugh** added label `Bug`, set milestone to `TypeScript 7.1.1 RC`, and assigned to **ahejlsberg**
 * (later) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript#64758](https://github.com/microsoft/TypeScript/issues/64758) (Open, `Bug`)

**TS7 LSP: documentHighlight returns nothing when the file path contains '@'**

*TS7 LSP documentHighlight returns no results when file paths contain unencoded `@` due to mismatched URI encoding.*

 * created by **snapwich**
 * **RyanCavanaugh** added label `Bug`
 * [today](https://github.com/microsoft/TypeScript/issues/64758#issuecomment-7094041981) **mhmdazkanfl** reproduced the Windows `textDocument/documentHighlight` issue with TypeScript 7.0.2, provided detailed environment and reproduction steps, and reported that Zed returned no highlights while VS Code returned three due to differences in Windows file URI encoding
 * [today](https://github.com/microsoft/TypeScript/issues/64758#issuecomment-7094508196) **mhmdazkanfl** said "I want to open a pull request to fix this issue. The issue has no milestone. If the team wants a community pull request for this issue, can a maintainer assign the Backlog milestone?"

### [Issue microsoft/TypeScript#64930](https://github.com/microsoft/TypeScript/issues/64930) (Open, `Bug`, `Domain: check: Order Dependence`, **ahejlsberg**)

**7\.1 regression: circular type alias accepts an assignment it should reject \(opposite of \#64891\)**

*TypeScript 7.1 regresses by allowing incompatible circular generic handler assignments that should produce TS2322 errors.*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [4 days ago](https://github.com/microsoft/TypeScript/issues/64930#issuecomment-6982595670) **Sipixer** reported that version 7.1 also broke untyped `@tanstack/db` collections by inferring `Collection<never, …>`, provided a reproduction showing thousands of production errors, and confirmed the issue persisted in the latest nightly after #65030
 * **RyanCavanaugh** assigned to **ahejlsberg**
 * **ahejlsberg** added label `Domain: check: Order Dependence`
 * [later](https://github.com/microsoft/TypeScript/issues/64930#issuecomment-7095234173) **MAST1999** confirmed that TypeScript 7.1.0-beta introduced a regression causing the repro to lose TS2322, explained that it made @tanstack/db collections infer as Collection<never> and caused 538 application errors, and provided an invariant-hook-alias workaround

### [PR microsoft/TypeScript#65064](https://github.com/microsoft/TypeScript/pull/65064) (Open, `Author: Team`, `For Milestone Bug`, `For Backlog Bug`, **jakebailey**)

**\[experiment\] fully order independent type checking**

*Overhauls type checking to produce consistent behavior regardless of traversal, file, cache, or cycle-processing order, with extensive randomized ordering tests.*

 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-7077760712) **typescript-automation[bot]** reported new TS7023 TypeScript errors in Effect's SchemaAST.ts when comparing baseline and PR user-test results, and asked the maintainer to investigate
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-7077761260) **typescript-automation[bot]** reported additional user-test-suite TypeScript errors in webpack, including incorrect `LogType` usage and `WeakTupleMap`/`MemCache` incompatibilities
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-7077869452) **typescript-automation[bot]** reported the requested performance-run results, including compiler metrics comparing the baseline with the pull request
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-7087164133) **jakebailey** requested TypeScript bot runs for dt, user testing, top1000 testing, and performance testing
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-7087165737) **typescript-automation[bot]** reported that the requested validation jobs had started and linked to their build results
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-7087544649) **typescript-automation[bot]** reported that the DT tests completed and revealed a branch-only TypeScript overload error in d3-selection involving an incompatible TransitionLike<HTMLParagraphElement, number> return type
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-7087724698) **typescript-automation[bot]** reported changed user-test results for the `uglify-js` project, including a new TS2339 error and a missing TS2322 error in `compress.js`
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-7087892531) **typescript-automation[bot]** reported the requested performance run results, including compiler metric comparisons showing increased symbols and memory usage
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-7089376443) **typescript-automation[bot]** reported top-1000 repository comparison results between the baseline and PR, highlighting changed build errors for review
 * [later](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-7095520093) **jakebailey** requested TypeScript bot runs for dt, user testing, top1000 testing, and performance testing
 * [later](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-7095523008) **typescript-automation[bot]** reported that the requested build, user test, top-1000 test, and performance test jobs had started and provided links to their results
 * [later](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-7096074264) **typescript-automation[bot]** reported that the DT tests produced a branch-only TypeScript error in the d3-selection package at d3-selection-tests.ts:1502
 * [later](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-7096397631) **typescript-automation[bot]** reported changed user-test results for the `uglify-js` project, including a new TS2339 error and a missing TS2322 error in `compress.js`
 * [later](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-7096678371) **typescript-automation[bot]** provided the requested performance results, showing increased symbols and memory usage in the Compiler-Unions native benchmark
 * [later](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-7099241405) **typescript-automation[bot]** reported results from comparing the baseline and PR across the top 1,000 repositories, highlighting new TypeScript build errors in PeerTube and Unleash and asking for investigation

### [PR microsoft/TypeScript#65617](https://github.com/microsoft/TypeScript/pull/65617) (Closed, `Author: Team`, `For Milestone Bug`, **ahejlsberg**)

**Produce union types when instantiating generic contextual types**

*Produce union types instead of selecting individual inference candidates when instantiating generic contextual types inferred from return types.*

 * [today](https://github.com/microsoft/TypeScript/pull/65617#issuecomment-7081461100) **typescript-automation[bot]** reported that the DT tests completed with unchanged results and provided a link to the build log
 * [today](https://github.com/microsoft/TypeScript/pull/65617#issuecomment-7081509378) **typescript-automation[bot]** reported that the user tests comparing the baseline and PR with tsc passed and everything looked good
 * [today](https://github.com/microsoft/TypeScript/pull/65617#issuecomment-7081653554) **typescript-automation[bot]** provided the requested performance results comparing the baseline and PR
 * [today](https://github.com/microsoft/TypeScript/pull/65617#issuecomment-7082223670) **typescript-automation[bot]** reported that testing the top 400 repositories with `tsc` showed no differences between the baseline and PR and that everything looked good
 * (later) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript#65621](https://github.com/microsoft/TypeScript/pull/65621) (Open, `Author: Team`, `For Backlog Bug`, **ahejlsberg**, **jakebailey**)

**Order types, symbols, and nodes by content instead of by ID**

*Order types, symbols, and nodes deterministically by content rather than creation IDs, interning identical types and eliminating ID-dependent output.*

 * [today](https://github.com/microsoft/TypeScript/pull/65621#issuecomment-7077621262) **typescript-automation[bot]** reported new TS2589 errors in type-fest user tests when comparing the baseline and PR, and asked @jakebailey to investigate
 * [today](https://github.com/microsoft/TypeScript/pull/65621#issuecomment-7077728264) **typescript-automation[bot]** reported the requested performance run results, including baseline-versus-PR compiler metrics
 * [today](https://github.com/microsoft/TypeScript/pull/65621#issuecomment-7078975032) **typescript-automation[bot]** reported results from comparing baseline and PR tsc runs across the top 1000 repositories, including new deep-instantiation errors in type-fest and build failures in BlockNote
 * [today](https://github.com/microsoft/TypeScript/pull/65621#issuecomment-7087163874) **jakebailey** requested TypeScript bot runs for dt, user testing, top1000 testing, and performance testing
 * [today](https://github.com/microsoft/TypeScript/pull/65621#issuecomment-7087165112) **typescript-automation[bot]** reported the statuses and results of automated build, test, and performance jobs
 * [today](https://github.com/microsoft/TypeScript/pull/65621#issuecomment-7087502982) **typescript-automation[bot]** reported that the DT test results were ready and unchanged, and linked the build log
 * [today](https://github.com/microsoft/TypeScript/pull/65621#issuecomment-7087559635) **typescript-automation[bot]** reported that user tests comparing the baseline and PR with tsc passed successfully
 * [today](https://github.com/microsoft/TypeScript/pull/65621#issuecomment-7087684258) **typescript-automation[bot]** provided the requested performance benchmark results comparing the baseline and pull request
 * [today](https://github.com/microsoft/TypeScript/pull/65621#issuecomment-7089302222) **typescript-automation[bot]** reported that testing the top 1,000 repositories found a changed result in tambo-ai/tambo, where two projects produced TS2589 errors involving packages/db/src/schema.ts
 * [later](https://github.com/microsoft/TypeScript/pull/65621#issuecomment-7095519672) **jakebailey** requested TypeScript bot runs for dt, user testing, top1000 testing, and performance testing
 * [later](https://github.com/microsoft/TypeScript/pull/65621#issuecomment-7095521805) **typescript-automation[bot]** reported that automated validation jobs had started and linked their build results, with performance test results still under review
 * [later](https://github.com/microsoft/TypeScript/pull/65621#issuecomment-7096033389) **typescript-automation[bot]** reported that the DefinitelyTyped test results were ready and unchanged, linking to the build log
 * [later](https://github.com/microsoft/TypeScript/pull/65621#issuecomment-7096142787) **typescript-automation[bot]** reported that user tests comparing the baseline and PR with tsc passed successfully
 * [later](https://github.com/microsoft/TypeScript/pull/65621#issuecomment-7096316261) **typescript-automation[bot]** reported the requested performance-run results comparing the baseline and pull request, including compiler metrics and memory changes
 * [later](https://github.com/microsoft/TypeScript/pull/65621#issuecomment-7099218572) **typescript-automation[bot]** reported that the top 1,000 repositories showed no differences between the baseline and PR when run with tsc

### [Issue microsoft/TypeScript#65627](https://github.com/microsoft/TypeScript/issues/65627) (Open)

**Declaration emit omits \`resolution\-mode\` when an import type names a \`\.d\.cts\` file of a dual package from an ES module**

*Declaration emit in TypeScript 7.x omits the required `resolution-mode` when referencing `.d.cts` files from ES modules, producing incorrect or unresolvable types.*

 * created by **ktfth**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/65627#issuecomment-7073105902) **hkleungai** said "A duplicate of https://github.com/microsoft/typescript-go/issues/3657."
 * [today](https://github.com/microsoft/TypeScript/issues/65627#issuecomment-7085224726) **ktfth** acknowledged that the issue was a duplicate and thanked the commenter for pointing it out

### [PR microsoft/TypeScript#65634](https://github.com/microsoft/TypeScript/pull/65634) (Open, `Author: Team`, `For Uncommitted Bug`, `dependencies`, `github_actions`)

**Bump ossf/scorecard\-action from 2\.5\.0 to 2\.6\.0 in the github\-actions group**

*Upgrade ossf/scorecard-action from v2.5.0 to v2.6.0, incorporating Scorecard v5.7.0 and updated workflow examples.*

 * created by **dependabot[bot]**
 * (today) **dependabot[bot]** added labels `dependencies`, `github_actions`
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`

### [PR microsoft/TypeScript#65635](https://github.com/microsoft/TypeScript/pull/65635) (Open, `For Backlog Bug`)

**Fix panic when computing emit signature for fileless diagnostics**

*Prevent a compiler panic when incremental declaration emit processes fileless diagnostics from failed output writes.*

 * created by **Shubham02022002**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/65635#issuecomment-7093080688) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (today) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/65635#issuecomment-7093333371) **Shubham02022002** said "@microsoft-github-policy-service agree"

### [PR microsoft/TypeScript#65636](https://github.com/microsoft/TypeScript/pull/65636) (Open, `For Backlog Bug`)

**Allow undefined in Error\.stack under exactOptionalPropertyTypes**

*Update Error.stack’s declaration to explicitly allow undefined under exactOptionalPropertyTypes, while documenting compatibility trade-offs and testing broader impact.*

 * created by **MartinFerret**
 * **typescript-automation[bot]** added label `For Backlog Bug`

### [Issue microsoft/TypeScript#65637](https://github.com/microsoft/TypeScript/issues/65637) (Open)

**Malformed UTF\-8 causes indices to be out of sync with the source text**

*Malformed UTF-8 in comments causes AST node positions and text extraction to misalign with the original source.*

 * created by **paldepind**

### [Issue microsoft/TypeScript#65638](https://github.com/microsoft/TypeScript/issues/65638) (Open)

**Opening or closing an unsaved dependency leaves stale diagnostics after a large file\-watch batch**

*Large file-watch batches cause stale diagnostics when an imported dependency is opened with unsaved changes or closed without saving.*

 * created by **mrousavy**

