# Report for 2026-10-11 (Sunday, October 11th, 2026)

16 different users commented on 27 different issues.

## Recommended Actions

 * Response Recommended
    * @mahesh-desu requested to be assigned to the issue in [microsoft/TypeScript#63814](https://github.com/microsoft/TypeScript/issues/63814#issuecomment-6123446810)

## Activity Summary

### [Issue microsoft/TypeScript#33866](https://github.com/microsoft/TypeScript/issues/33866) (Open, `Bug`, `Help Wanted`, `Domain: lib.d.ts`)

**Add types for window\.performance\.getEntriesByType**

*Add definitions to TypeScript’s standard library for window.performance.getEntriesByType to return properly typed PerformanceMark, PerformanceMeasure, and PerformanceResourceTiming entries.*

 * [1.2 years ago](https://github.com/microsoft/TypeScript/issues/33866#issuecomment-3120028664) **RyanCavanaugh** confirmed that the requested specialization was still absent in version 5.9 and pointed out that the OP's code example used `.navigator` instead of `.performance`, suggesting clarification of the current behavior
 * [1.1 years ago](https://github.com/microsoft/TypeScript/issues/33866#issuecomment-3125929003) **DerGernTod** highlighted that performance.getEntriesByName supports a second argument for entry type and suggested typing its return types accordingly
 * [today](https://github.com/microsoft/TypeScript/issues/33866#issuecomment-6110643262) **Ankith-B** offered to implement the change in TypeScript-DOM-lib-generator using additionalSignatures and described the prepared overloads for Performance entries, noted tests passed, and asked whether to proceed with a PR or use a different approach
 * [today](https://github.com/microsoft/TypeScript/issues/33866#issuecomment-6112332718) **Ankith-B** said "   Opened microsoft/TypeScript-DOM-lib-generator#2572."

### [Issue microsoft/TypeScript#54201](https://github.com/microsoft/TypeScript/issues/54201) (Closed, `Suggestion`, `Awaiting More Feedback`)

**Feature Request: Update wrong defined import statements?**

*Automatically delete or update import statements referencing moved or undefined functions in VSCode.*

 * **mjbvz** unassigned **mjbvz**
 * (3.4 years ago) **RyanCavanaugh** added labels `Suggestion`, `Awaiting More Feedback`
 * (today) **b13nxx** closed the issue

### [Issue microsoft/TypeScript#63814](https://github.com/microsoft/TypeScript/issues/63814) (Open, `Help Wanted`)

**Corsa differences in \`export=\` module augmentation**

*Corsa changes how export= module augmentation works, causing differences in exported name visibility.*

 * [5 weeks ago](https://github.com/microsoft/TypeScript/issues/63814#issuecomment-5492447311) **LeonxLJX** said "I'd like to take this one (Corsa differences in export= module augmentation). I'll look into the root cause and follow up with a PR. (claiming via @LeonxLJX)"
 * [5 weeks ago](https://github.com/microsoft/TypeScript/issues/63814#issuecomment-5492966557) **LeonxLJX** said "I'd like to take this one (Corsa differences in export= module augmentation). I'll dig into the root cause and follow up with a PR shortly. (claiming via @LeonxLJX)"
 * [5 weeks ago](https://github.com/microsoft/TypeScript/issues/63814#issuecomment-5492967709) **LeonxLJX** said "I'd like to take this one (Corsa differences in export= module augmentation). I'll look into the root cause and follow up with a PR. (claiming via @LeonxLJX)"
 * [later](https://github.com/microsoft/TypeScript/issues/63814#issuecomment-6123446810) **mahesh-desu** offered to fix duplicate filename directive in the augmentExportEquals2 fixture and requested assignment

### [PR microsoft/TypeScript#64307](https://github.com/microsoft/TypeScript/pull/64307) (Open, `For Milestone Bug`, **ahejlsberg**)

**Normalize distributed type parameters in conditional type relationships**

*Ensure target types in TypeScript conditional type relationships are instantiated to properly normalize distributed type parameters.*

 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [3 weeks ago](https://github.com/microsoft/TypeScript/pull/64307#issuecomment-5712772919) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/64307#issuecomment-6042790880) **trevorade** requested adding `Fixes #64673` to the PR description to link the issue
 * [today](https://github.com/microsoft/TypeScript/pull/64307#issuecomment-6112091454) **trevorade** described that the identity relation still fails for uninstantiated distributive conditional types and provided reproduction code and code references
 * (later) **typescript-automation[bot]** added label `For Milestone Bug`, removed label `For Uncommitted Bug`, and assigned to **ahejlsberg**
 * [later](https://github.com/microsoft/TypeScript/pull/64307#issuecomment-6121069156) **Andarist** said "thanks @trevorade for extra test cases! :)"

### [PR microsoft/TypeScript#64310](https://github.com/microsoft/TypeScript/pull/64310) (Closed, `For Uncommitted Bug`)

**Normalize distributed type parameters during conditional type inference**

*Normalize distributed type parameters during conditional type inference to address a regression introduced in PR 64237*

 * created by **Andarist**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [3 weeks ago](https://github.com/microsoft/TypeScript/pull/64310#issuecomment-5717056601) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [later](https://github.com/microsoft/TypeScript/pull/64310#issuecomment-6121603222) **Andarist** said "I folded this work into https://github.com/microsoft/TypeScript/pull/64307"
 * (later) **Andarist** closed the issue

### [PR microsoft/TypeScript#64487](https://github.com/microsoft/TypeScript/pull/64487) (Closed, `For Uncommitted Bug`, `dependencies`, `github_actions`)

**Bump the github\-actions group across 1 directory with 3 updates**

*Bump GitHub CodeQL Action init, analyze, and upload-sarif actions in the root directory to their newest versions*

 * (2 weeks ago) **dependabot[bot]** added labels `dependencies`, `github_actions`
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64487#issuecomment-6116717865) **dependabot[bot]** said "Looks like these dependencies are updatable in another way, so this is no longer needed."
 * (today) **dependabot[bot]** closed the issue

### [PR microsoft/TypeScript#64695](https://github.com/microsoft/TypeScript/pull/64695) (Open, `For Milestone Bug`, **ahejlsberg**)

**\[experiment\] Skip incompatible discriminants when inferring**

*Experimentally skip incompatible discriminant properties during TypeScript union type inference to reduce workload and validate via tests.*

 * [3 days ago](https://github.com/microsoft/TypeScript/pull/64695#issuecomment-6065889237) **typescript-automation[bot]** reported performance run results for the requested comparison
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/64695#issuecomment-6066282755) **weswigham** noted that previous JS codebase type comparisons were costly, acknowledged the perf suite improvements, and suggested using discriminateTypeByDiscriminableItems for consistent discrimination method
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/64695#issuecomment-6066595594) **typescript-automation[bot]** reported that running the top 400 repos tsc comparison between baseline and pr succeeded without issues
 * [today](https://github.com/microsoft/TypeScript/pull/64695#issuecomment-6113604981) **Andarist** requested a full test rerun to evaluate performance

### [Issue microsoft/TypeScript#64727](https://github.com/microsoft/TypeScript/issues/64727) (Open)

**TS 7: declaration emit property order depends on which other files are in the program**

*TypeScript 7’s declaration emitter produces inconsistent property ordering in generated d.ts files depending on which files are included in the program.*

 * created by **maschwenk**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/64727#issuecomment-6099523263) **maschwenk** said "I have no idea if this is something we care about or not so please feel free to dismiss"
 * [later](https://github.com/microsoft/TypeScript/issues/64727#issuecomment-6123975636) **jakebailey** said "This is definitely something to fix yes"
 * [later](https://github.com/microsoft/TypeScript/issues/64727#issuecomment-6125491855) **maschwenk** provided a link to a possible fix in a pull request

### [Issue microsoft/TypeScript#64730](https://github.com/microsoft/TypeScript/issues/64730) (Open)

**TS 7\.0 reports declaration\-emit diagnostics \(e\.g\. TS2527\) under \-\-noEmit when other semantic errors exist; TS 6\.0 does not \(undocumented difference\)**

*TypeScript 7.0 reports declaration-emit diagnostics under --noEmit when other semantic errors are present, unlike 6.0.*

 * created by **seunghyun-24**
 * [later](https://github.com/microsoft/TypeScript/issues/64730#issuecomment-6123969870) **jakebailey** said "Is this a problem, or something you just happened to notice?"

### [PR microsoft/TypeScript#64734](https://github.com/microsoft/TypeScript/pull/64734) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Various memory optimizations**

*Combined memory optimizations reduce memory usage by 22–29% and allocation counts by 3.6–16.6% across nine test scenarios.*

 * [today](https://github.com/microsoft/TypeScript/pull/64734#issuecomment-6110569980) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/64734#issuecomment-6110570961) **typescript-automation[bot]** posted build status update with links to started jobs and results
 * [today](https://github.com/microsoft/TypeScript/pull/64734#issuecomment-6110842190) **typescript-automation[bot]** posted the requested performance comparison report for the baseline versus PR
 * [today](https://github.com/microsoft/TypeScript/pull/64734#issuecomment-6110989346) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/64734#issuecomment-6110990190) **typescript-automation[bot]** posted an automated build status update
 * [today](https://github.com/microsoft/TypeScript/pull/64734#issuecomment-6111269552) **typescript-automation[bot]** reported the requested perf run results
 * [today](https://github.com/microsoft/TypeScript/pull/64734#issuecomment-6112203698) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/64734#issuecomment-6112204448) **typescript-automation[bot]** started CI jobs and posted initial build status
 * [today](https://github.com/microsoft/TypeScript/pull/64734#issuecomment-6112471932) **typescript-automation[bot]** reported performance run results with comparison metrics
 * [today](https://github.com/microsoft/TypeScript/pull/64734#issuecomment-6115362733) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/64734#issuecomment-6115363634) **typescript-automation[bot]** posted a status update indicating that the ‘perf test this faster’ build started with links to the build and results
 * [today](https://github.com/microsoft/TypeScript/pull/64734#issuecomment-6115620544) **typescript-automation[bot]** provided the requested performance run results
 * [today](https://github.com/microsoft/TypeScript/pull/64734#issuecomment-6117692661) **jakebailey** said "CPU regression appears to be due to #64735"
 * [today](https://github.com/microsoft/TypeScript/pull/64734#issuecomment-6118217789) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/64734#issuecomment-6118218693) **typescript-automation[bot]** announced that performance tests had started with links to build status and results
 * [today](https://github.com/microsoft/TypeScript/pull/64734#issuecomment-6118526287) **typescript-automation[bot]** provided perf run results including a comparison report with metrics on errors, symbols, types, and memory usage
 * [later](https://github.com/microsoft/TypeScript/pull/64734#issuecomment-6126968288) **jakebailey** said "@typescript-bot perf test this faster"
 * [later](https://github.com/microsoft/TypeScript/pull/64734#issuecomment-6126970184) **typescript-automation[bot]** announced start of performance test jobs and provided build and result links
 * [later](https://github.com/microsoft/TypeScript/pull/64734#issuecomment-6127473879) **typescript-automation[bot]** posted the performance run results for the requested comparison

### [PR microsoft/TypeScript#64735](https://github.com/microsoft/TypeScript/pull/64735) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Resolve instantiated object members through a shared worker**

*Allow instantiated object members to be resolved properly when used inside shared workers.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/64735#issuecomment-6111932716) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/64735#issuecomment-6111933678) **typescript-automation[bot]** announced that performance test jobs started and would be updated as builds progress
 * [today](https://github.com/microsoft/TypeScript/pull/64735#issuecomment-6112187980) **typescript-automation[bot]** provided the requested performance run results including a detailed baseline vs pr comparison report

### [PR microsoft/TypeScript#64736](https://github.com/microsoft/TypeScript/pull/64736) (Open, `For Backlog Bug`)

**Copy synthetic comments in SetOriginal and emit them once in TS trasforms**

*Extend tsgo’s emitNode.copyFrom to preserve synthetic comments and clear duplicates so they’re emitted only once during TypeScript transforms.*

 * created by **trevorade**
 * **typescript-automation[bot]** added label `For Backlog Bug`

### [PR microsoft/TypeScript#64737](https://github.com/microsoft/TypeScript/pull/64737) (Open, `For Backlog Bug`)

**Avoid exponential base type search in hasBaseType**

*Change hasBaseType to avoid exponential exploration of shared interface base types, reducing type-checking time on deep inheritance chains.*

 * created by **fitchmultz**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64737#issuecomment-6113684319) **fitchmultz** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript/pull/64737#issuecomment-6118738793) **DanielRosenwasser** said "@typescript-bot perf test this"
 * [today](https://github.com/microsoft/TypeScript/pull/64737#issuecomment-6118739780) **typescript-automation[bot]** announced that performance test build jobs started and provided links to status and results
 * [today](https://github.com/microsoft/TypeScript/pull/64737#issuecomment-6119059459) **typescript-automation[bot]** provided the requested performance run results in a detailed comparison table

### [PR microsoft/TypeScript#64738](https://github.com/microsoft/TypeScript/pull/64738) (Closed, `For Uncommitted Bug`)

**Keep \`this\` inside functions nested in downleveled static blocks**

*Fix downleveled static blocks incorrectly rewriting this in nested functions to the class alias by using the active visitor.*

 * created by **trevorade**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [PR microsoft/TypeScript#64739](https://github.com/microsoft/TypeScript/pull/64739) (Closed, `Author: Team`, `For Uncommitted Bug`, **ahejlsberg**)

**Shrink \`ValueSymbolLinks\` by 16 bytes**

*Relocating a boolean into a separate set reduces ValueSymbolLinks memory by 16 bytes (1%) when compiling VS Code.*

 * created by **ahejlsberg**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript/pull/64739#issuecomment-6115561958) **ahejlsberg** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/64739#issuecomment-6115562754) **typescript-automation[bot]** indicated that the performance test job started and provided status and results links
 * [today](https://github.com/microsoft/TypeScript/pull/64739#issuecomment-6115800643) **typescript-automation[bot]** posted performance run results for the requested comparison on the PR

### [Issue microsoft/TypeScript#64740](https://github.com/microsoft/TypeScript/issues/64740) (Open)

**\[API\] \`ConditionalType\` has no counterpart to \`root\` of TypeScript 6 \(the node it was declared with\)**

*TypeScript 7's ConditionalType API lacks a counterpart to the TS6 root property, preventing retrieval of the original conditional type declaration node.*

 * created by **MARCROCK22**

### [PR microsoft/TypeScript#64741](https://github.com/microsoft/TypeScript/pull/64741) (Closed, `For Uncommitted Bug`, `dependencies`, `github_actions`)

**Bump the github\-actions group across 1 directory with 6 updates**

*Upgrades six GitHub Actions (setup-node, upload/download-artifact, and CodeQL) in the project root to newer versions.*

 * created by **dependabot[bot]**
 * (today) **dependabot[bot]** added labels `dependencies`, `github_actions`
 * (today) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`

### [Issue microsoft/TypeScript#64742](https://github.com/microsoft/TypeScript/issues/64742) (Open, `Bug`)

**Language server \(tsc \-\-lsp\) exits with code 1 after \`shutdown\` and \`exit\`**

*TypeScript 7's LSP server unexpectedly exits with code 1 after receiving shutdown and exit notifications*

 * created by **creasty**

### [PR microsoft/TypeScript#64743](https://github.com/microsoft/TypeScript/pull/64743) (Open, `For Backlog Bug`)

**Fix enum crash when namespace and enum share a name**

*Guard enum value computation and treat ModuleBlock as a member container to prevent compiler panic when a namespace and enum share the same name.*

 * created by **smg99**
 * **typescript-automation[bot]** added label `For Backlog Bug`

### [PR microsoft/TypeScript#64744](https://github.com/microsoft/TypeScript/pull/64744) (Open, `For Backlog Bug`)

**Fix missing syntax errors for optional property access in plain JS**

*Restore syntax errors for optional property access assignments in plain JavaScript by allowlisting TS2777, TS2778, TS2779, TS2780, and TS2781.*

 * created by **mahesh-desu**
 * **typescript-automation[bot]** added label `For Backlog Bug`

### [PR microsoft/TypeScript#64745](https://github.com/microsoft/TypeScript/pull/64745) (Open, `For Uncommitted Bug`, **DanielRosenwasser**, **Copilot**)

**Include default exports in export star, continue erroring on immediate conflicts**

*Implement the TC39 export-star-default proposal to include default exports in export * while resolving conflicts and prioritizing explicit defaults.*

 * created by **Copilot**
 * (later) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * (later) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/64745#issuecomment-6119506045) **DanielRosenwasser** requested the TypeScript bot to run top1000, user, and dt tests
 * [later](https://github.com/microsoft/TypeScript/pull/64745#issuecomment-6119507426) **typescript-automation[bot]** posted a status update of CI job results
 * [later](https://github.com/microsoft/TypeScript/pull/64745#issuecomment-6119850785) **typescript-automation[bot]** reported DT test results and compile errors in redux-form
 * [later](https://github.com/microsoft/TypeScript/pull/64745#issuecomment-6119851024) **typescript-automation[bot]** reported DT test results for carbon-components-react including an unused '@ts-expect-error' directive and a 'no overload matches this call' compile error
 * [later](https://github.com/microsoft/TypeScript/pull/64745#issuecomment-6119910026) **typescript-automation[bot]** reported that user tests passed with no differences between baseline and PR
 * [later](https://github.com/microsoft/TypeScript/pull/64745#issuecomment-6119968257) **jakebailey** said "This is truly a cursed spec change"
 * [later](https://github.com/microsoft/TypeScript/pull/64745#issuecomment-6121296640) **typescript-automation[bot]** reported the tsc comparison results for the top 1000 repositories, highlighting build failures in doocs/md and nolimits4web/swiper

### [PR microsoft/TypeScript#64746](https://github.com/microsoft/TypeScript/pull/64746) (Open, `For Backlog Bug`)

**fix: Fix MemberList panic on merged enum element access**

*Only constant-evaluate element-access expressions for actual enum members to prevent MemberList panics on merged namespace enums.*

 * created by **andre-fajar-n**
 * **typescript-automation[bot]** added label `For Backlog Bug`

### [PR microsoft/TypeScript#64747](https://github.com/microsoft/TypeScript/pull/64747) (Open, `For Uncommitted Bug`, **DanielRosenwasser**, **Copilot**)

**Include default exports in export\-star and error on access to conflicts**

*Enable inclusion of default exports in export-star resolution and CommonJS export-star emit, with error reporting on conflicting accesses.*

 * created by **Copilot**
 * (later) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * (later) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/64747#issuecomment-6120156426) **DanielRosenwasser** requested the TypeScript bot to run top1000, user, and dt tests
 * [later](https://github.com/microsoft/TypeScript/pull/64747#issuecomment-6120157850) **typescript-automation[bot]** reported statuses of automated build jobs for commands with links to their start and result logs
 * [later](https://github.com/microsoft/TypeScript/pull/64747#issuecomment-6120180147) **DanielRosenwasser** said "@typescript-bot perf test this"
 * [later](https://github.com/microsoft/TypeScript/pull/64747#issuecomment-6120181518) **typescript-automation[bot]** notified that CI jobs had started and would be updated
 * [later](https://github.com/microsoft/TypeScript/pull/64747#issuecomment-6120529654) **typescript-automation[bot]** reported that the DT tests results remained unchanged and provided a link to the logs
 * [later](https://github.com/microsoft/TypeScript/pull/64747#issuecomment-6120593505) **typescript-automation[bot]** reported that user tests passed with no differences between baseline and PR
 * [later](https://github.com/microsoft/TypeScript/pull/64747#issuecomment-6120686164) **typescript-automation[bot]** reported the results of the requested performance run including metrics for errors, symbols, types, memory usage, and allocations
 * [later](https://github.com/microsoft/TypeScript/pull/64747#issuecomment-6122115834) **typescript-automation[bot]** reported that running tsc on the top 1000 repos showed everything looked good

### [PR microsoft/TypeScript#64748](https://github.com/microsoft/TypeScript/pull/64748) (Open, `For Uncommitted Bug`)

**Fix broken augmentExportEquals2 test fixture**

*Remove duplicate @filename directive in the augmentExportEquals2 test fixture to restore expected diagnostics.*

 * created by **mahesh-desu**
 * (later) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/64748#issuecomment-6123625457) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."

