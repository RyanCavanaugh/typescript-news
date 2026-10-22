# Report for 2026-10-18 (Sunday, October 18th, 2026)

11 different users commented on 17 different issues.

## Recommended Actions

 * Response Recommended
    * @vivan070707-ctrl asked if the issue was still available for contribution in [microsoft/TypeScript#64438](https://github.com/microsoft/TypeScript/issues/64438#issuecomment-6260062351)
    * @mbarinov asked if any additional feedback or checks were needed before merging in [microsoft/TypeScript#64732](https://github.com/microsoft/TypeScript/pull/64732#issuecomment-6264594274)

## Activity Summary

### [Issue microsoft/TypeScript#17002](https://github.com/microsoft/TypeScript/issues/17002) (Open, `Suggestion`, `In Discussion`, `Domain: lib.d.ts`)

**Array\.isArray type narrows to any\[\] for ReadonlyArray\<T\>**

*Array.isArray fails to correctly narrow a union including ReadonlyArray<T>, resulting in an any[] type instead of ReadonlyArray<T>.*

 * [15 weeks ago](https://github.com/microsoft/TypeScript/issues/17002#issuecomment-4885934843) **daishuge** submitted a minimal fix in PR #63609 that added an overload in es5.d.ts to preserve readonly input types without affecting unknown narrowing
 * [14 weeks ago](https://github.com/microsoft/TypeScript/issues/17002#issuecomment-4896931936) **anderson-pete** noted that the proposed fix would break a lot of existing code
 * **jakebailey** removed label `Fix Available`
 * [later](https://github.com/microsoft/TypeScript/issues/17002#issuecomment-6270372250) **WORMSS** explained that Array.isArray could not distinguish mutable from readonly arrays and suggested filtering out both

### [Issue microsoft/TypeScript#64438](https://github.com/microsoft/TypeScript/issues/64438) (Open, `Bug`, `Help Wanted`, `Good First Issue`)

**Incorrect/unhelpful error message for non\-module jsx file**

*TypeScript shows misleading missing module errors for JSX in non-module scripts instead of stating scripts cannot import modules.*

 * **DanielRosenwasser** added label `Good First Issue`
 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/64438#issuecomment-5826551653) **sh011** said "Hi @calebegg @DanielRosenwasser I went through the issue and found that the diagnostic chain needs to be looked up properly. I would like to work on this issue, can you please assign it to me. Thanks!"
 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/64438#issuecomment-5911162732) **SiddhantShedge45** offered to work on the issue by investigating JSX diagnostic generation, improving the error message, adding a regression test, and verifying existing behavior
 * [today](https://github.com/microsoft/TypeScript/issues/64438#issuecomment-6260062351) **vivan070707-ctrl** asked if the issue was still available for investigation and offered to implement a fix with a regression test

### [PR microsoft/TypeScript#64527](https://github.com/microsoft/TypeScript/pull/64527) (Open, `For Uncommitted Bug`)

**Fix checkJs behavior for \.mjs and \.cjs files next to declarations**

*Ensure checkJs wildcard include consistently prefers declaration files over corresponding .js, .mjs, and .cjs implementations.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/64527#issuecomment-5926959590) **hardikkaurani** thanked ljharb for clarifying the compatibility concern and asked weswigham to clarify the intended compatibility semantics for wildcard resolution
 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/64527#issuecomment-5937764268) **weswigham** stated they would either retain or remove the legacy dual .js/.d.ts include lookup behavior and would not break .mjs/.cjs includes
 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/64527#issuecomment-5938085680) **hardikkaurani** thanked weswigham for clarification and explained focusing on removing legacy .js/.d.ts wildcard behavior without extending it to .mjs and .cjs and aligning regression coverage
 * [today](https://github.com/microsoft/TypeScript/pull/64527#issuecomment-6259970448) **ljharb** asked why the .js behavior was broken and why files with corresponding dts files are implicitly not typechecked

### [PR microsoft/TypeScript#64695](https://github.com/microsoft/TypeScript/pull/64695) (Open, `For Milestone Bug`, **ahejlsberg**)

**\[experiment\] Skip incompatible discriminants when inferring**

*Experimentally skip incompatible discriminant properties during TypeScript union type inference to reduce workload and validate via tests.*

 * (5 days ago) **typescript-automation[bot]** added label `For Milestone Bug`, removed label `For Uncommitted Bug`, and assigned to **ahejlsberg**
 * [later](https://github.com/microsoft/TypeScript/pull/64695#issuecomment-6269790663) **weswigham** noted a neutral to +8% performance impact, suggested caching discriminable item results or re-adding an optional prop fast path to improve performance, and asked for test cases demonstrating improved inference results, referencing a prior PR
 * [later](https://github.com/microsoft/TypeScript/pull/64695#issuecomment-6270098644) **Andarist** mentioned having implemented the optional prop fast path locally and planning to push it and request a fresh rerun; noted having some test cases and intending to push them later this week; said they would review the linked PR and its tests

### [PR microsoft/TypeScript#64732](https://github.com/microsoft/TypeScript/pull/64732) (Open, `For Backlog Bug`)

**Fix inline JSDoc links in optional type positions**

*Ensure inline link, linkcode, and linkplain tags after @throws and @returns are parsed as links instead of type expressions.*

 * [6 days ago](https://github.com/microsoft/TypeScript/pull/64732#issuecomment-6131086083) **typescript-automation[bot]** reported the perf run results in a detailed comparison report
 * [6 days ago](https://github.com/microsoft/TypeScript/pull/64732#issuecomment-6131105060) **typescript-automation[bot]** reported tsc user test results and confirmed everything looked good
 * [6 days ago](https://github.com/microsoft/TypeScript/pull/64732#issuecomment-6131812308) **typescript-automation[bot]** reported that running the top 400 repos tsc comparison between baseline and pr succeeded without issues
 * [later](https://github.com/microsoft/TypeScript/pull/64732#issuecomment-6264594274) **mbarinov** said "Hi @jakebailey, thanks for running the additional tests. Do you have any feedback or additional checks you'd like me to run before this is ready to merge?"

### [PR microsoft/TypeScript#64858](https://github.com/microsoft/TypeScript/pull/64858) (Open, `Author: Team`, `For Uncommitted Bug`, `dependencies`, `github_actions`)

**Bump the github\-actions group with 4 updates**

*Update four GitHub Actions (CodeQL init, analyze, upload-sarif, and OSSF Scorecard) to their latest versions.*

 * created by **dependabot[bot]**
 * (today) **dependabot[bot]** added labels `dependencies`, `github_actions`
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`

### [Issue microsoft/TypeScript#64859](https://github.com/microsoft/TypeScript/issues/64859) (Open, `Bug`, **andrewbranch**, **RyanCavanaugh**, **Copilot**)

**\[API\] Printer attaches source comments to synthesized nodes because the node encoder sends pos \-1 as 0**

*TypeScript’s sync API printer wrongly attaches existing source comments to synthesized nodes when their negative positions are clamped to zero.*

 * created by **Smrtnyk**

### [Issue microsoft/TypeScript#64860](https://github.com/microsoft/TypeScript/issues/64860) (Open, `Needs Investigation`, **andrewbranch**)

**\[api\] Add back missing: factory\.createUniqueName / createTempVariable \(generated identifiers\)**

*Add createUniqueName, createTempVariable, and related generated identifier functions to TypeScript’s AST factory to restore automatic collision-free name generation.*

 * created by **Smrtnyk**

### [Issue microsoft/TypeScript#64861](https://github.com/microsoft/TypeScript/issues/64861) (Open, `Needs Investigation`, **andrewbranch**)

**\[api\] No replacement for ts\.transform / TransformationContext / custom transformers in program\.emit**

*Requesting custom transformer support in TypeScript 7's native emit API or guidance on a long-term transform-and-emit workflow.*

 * created by **Smrtnyk**

### [Issue microsoft/TypeScript#64862](https://github.com/microsoft/TypeScript/issues/64862) (Open, `Bug`)

**TS7 LSP: every didOpen rebuilds and deletes a non\-matching referenced project**

*TypeScript 7's LSP rebuilds every referenced project on didOpen and deletes non-matching ones before selecting the correct project.*

 * created by **Kiborgik**

### [Issue microsoft/TypeScript#64863](https://github.com/microsoft/TypeScript/issues/64863) (Open, `Bug`, **weswigham**, **RyanCavanaugh**, **Copilot**)

**Panic in \`getSignaturesOfType\` on a decorator's contextual type in JS API**

*Calling checker.getSignaturesOfType on a decorator expression’s contextual type in the TypeScript JS API triggers a Go runtime panic due to a nil pointer dereference*

 * created by **auvred**

### [Issue microsoft/TypeScript#64864](https://github.com/microsoft/TypeScript/issues/64864) (Open, **andrewbranch**, **Copilot**)

**Some JS API types don't match their runtime values**

*Several TypeScript JS API type definitions in the sync and AST packages misrepresent actual runtime property types, causing mismatches.*

 * created by **auvred**

### [PR microsoft/TypeScript#64865](https://github.com/microsoft/TypeScript/pull/64865) (Closed, `For Backlog Bug`)

**Fix TS2367 false positive when comparing generic constructor types with concrete constructors**

*Treat unconstrained type parameter targets as potentially overlapping to prevent spurious TS2367 errors when comparing generic constructors with concrete ones.*

 * created by **RXVEN-1907**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * (later) **RXVEN-1907** closed the issue

