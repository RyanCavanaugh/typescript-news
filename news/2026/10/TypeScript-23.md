# Report for 2026-10-23 (Friday, October 23rd, 2026)

17 different users commented on 41 different issues.

## Recommended Actions

 * Moderation
    * @mrlubos posted spam content in [microsoft/TypeScript#64944](https://github.com/microsoft/TypeScript/pull/64944#issuecomment-6374657128)
 * Response Recommended
    * @Eptagone asked if there were any updates on the issue in [microsoft/TypeScript#36981](https://github.com/microsoft/TypeScript/issues/36981#issuecomment-6370969938)
    * @jasonkuhrt reported a sync client unhandled error bug and offered a patch with tests in [microsoft/TypeScript#63885](https://github.com/microsoft/TypeScript/issues/63885#issuecomment-6384523001)
    * @denis-migdal asked about using `implements` for function definitions in [microsoft/TypeScript#64399](https://github.com/microsoft/TypeScript/issues/64399#issuecomment-6383893332)
    * @jasonkuhrt asked if @maricastroc was still planning to open her PR now that the issue is in Backlog in [microsoft/TypeScript#64706](https://github.com/microsoft/TypeScript/issues/64706#issuecomment-6384522740)
    * @jasonkuhrt asked whether including nested package manifests in the signature would fit the PR and offered to add a test case in [microsoft/TypeScript#64841](https://github.com/microsoft/TypeScript/pull/64841#issuecomment-6384522466)
    * @MadalinWolf opened a PR to fix signature help docs and added a regression test in [microsoft/TypeScript#64937](https://github.com/microsoft/TypeScript/issues/64937#issuecomment-6382147151)
    * @AbbasFullstack offered to fix the issue in [microsoft/TypeScript#64948](https://github.com/microsoft/TypeScript/issues/64948#issuecomment-6379651574)
    * @matej21 provided repro steps and detailed analysis in [microsoft/TypeScript#64950](https://github.com/microsoft/TypeScript/issues/64950#issuecomment-6385437712)

## Activity Summary

### [Issue microsoft/TypeScript#36981](https://github.com/microsoft/TypeScript/issues/36981) (Open, `Needs Investigation`, `Rescheduled`, **weswigham**)

**\`Omit\`  helper loses type information when used with extended Records\.**

*Using Omit on an interface extending Record<string, any> causes all property types, including explicitly defined ones, to be replaced with any.*

 * (2.2 years ago) **RyanCavanaugh** set milestone to `TypeScript 5.7.0`, and removed from milestone `TypeScript 5.5.0`
 * **jakebailey** removed label `Fix Available`
 * [today](https://github.com/microsoft/TypeScript/issues/36981#issuecomment-6370969938) **Eptagone** said "This is still happening. Any updates?"

### [Issue microsoft/TypeScript#420](https://github.com/microsoft/TypeScript/issues/420) (Open, `Suggestion`, `Help Wanted`)

**Allow a module to implement an interface**

*Allow TypeScript modules to implement interfaces using an implements clause to enforce type compatibility.*

 * [2.2 years ago](https://github.com/microsoft/TypeScript/issues/420#issuecomment-2218402783) **fdaciuk** said "Maybe @RyanCavanaugh can help answer this =)"
 * [1.9 years ago](https://github.com/microsoft/TypeScript/issues/420#issuecomment-2494918759) **Ayc0** bumped the issue for an additional use case: verifying that all four entries in package.json exports expose the same interface
 * [1 year ago](https://github.com/microsoft/TypeScript/issues/420#issuecomment-3416668782) **AgentEnder** described their use case implementing a typed NxPlugin and how they worked around limitations
 * [later](https://github.com/microsoft/TypeScript/issues/420#issuecomment-6381859041) **denis-migdal** suggested a zero-runtime-footprint approach using import type and a Satisfies type alias

### [Issue microsoft/TypeScript#63885](https://github.com/microsoft/TypeScript/issues/63885) (Open, `Possible Improvement`)

**Bad tsserverPath in the unstable/sync API client surfaces as bare "EPIPE: broken pipe, write" instead of naming the executable**

*Invalid tsserverPath in unstable/sync API client yields a generic EPIPE error instead of naming the missing executable*

 * created by **smm-h**
 * (10 weeks ago) **RyanCavanaugh** added labels `Possible Improvement`, `Possible Improvement`
 * [later](https://github.com/microsoft/TypeScript/issues/63885#issuecomment-6384523001) **jasonkuhrt** demonstrated that the sync client failed to handle child process error events causing process exit on EPIPE and offered a patch with tests

### [Issue microsoft/TypeScript#63979](https://github.com/microsoft/TypeScript/issues/63979) (Closed, `Out of Scope`, `Docs`)

**Official guidelines to build complex types**

*Proposal to add official TypeScript guidelines detailing supported tips, patterns, and pitfalls for constructing complex type definitions.*

 * [8 weeks ago](https://github.com/microsoft/TypeScript/issues/63979#issuecomment-5456795894) **MartinJohns** said "The issue is not locked. You can still take your time and comment later."
 * [8 weeks ago](https://github.com/microsoft/TypeScript/issues/63979#issuecomment-5457409158) **RyanCavanaugh** said "Regardless, the scope of the project is not really something you're going to change by commenting on an issue whether it's closed or open"
 * [6 weeks ago](https://github.com/microsoft/TypeScript/issues/63979#issuecomment-5566337634) **denis-migdal** proposed collecting TypeScript tips and suggested using interfaces instead of concrete types, defining capacity-based interfaces, and employing symbols to hide internal data
 * [later](https://github.com/microsoft/TypeScript/issues/63979#issuecomment-6382208348) **denis-migdal** provided several TypeScript tricks and tips including type assertions, casting avoidance, static hooks, and parameter bags

### [Issue microsoft/TypeScript#64399](https://github.com/microsoft/TypeScript/issues/64399) (Open, `Design Notes`)

**Design Meeting Notes, 2026\-09\-22**

*Exploring syntax proposals to support satisfies-style whole-signature annotations on TypeScript function declarations.*

 * created by **DanielRosenwasser**
 * **DanielRosenwasser** added label `Design Notes`
 * [later](https://github.com/microsoft/TypeScript/issues/64399#issuecomment-6383893332) **denis-migdal** questioned using `implements` for function definitions and suggested it would align with classes, inherit JSDoc, and support multiple type implementations

### [PR microsoft/TypeScript#64654](https://github.com/microsoft/TypeScript/pull/64654) (Open, `Domain: Performance`, `For Uncommitted Bug`, **ahejlsberg**)

**check the target of a type reference in isWeakType**

*Modify isWeakType to check the target of type references instead of instantiating generic members, reducing memory usage by 19%.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/64654#issuecomment-6021565310) **typescript-automation[bot]** posted performance run results with a comparison report of baseline versus PR metrics
 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/64654#issuecomment-6021637755) **typescript-automation[bot]** reported tsc user test results and confirmed everything looked good
 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/64654#issuecomment-6022484982) **typescript-automation[bot]** reported that running the top 400 repos tsc comparison between baseline and pr succeeded without issues
 * [today](https://github.com/microsoft/TypeScript/pull/64654#issuecomment-6374304244) **ahejlsberg** said "This likely is no longer relevant now that #64915 is in main. With that PR, isWeakType operates on uninstantiated member layout properties. "
 * [today](https://github.com/microsoft/TypeScript/pull/64654#issuecomment-6374347255) **ahejlsberg** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/64654#issuecomment-6374348951) **typescript-automation[bot]** said "Hey @ahejlsberg, this PR was updated less than two minutes before this command. Please wait until it has been unchanged for two minutes and try again."
 * [today](https://github.com/microsoft/TypeScript/pull/64654#issuecomment-6374430099) **ahejlsberg** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/64654#issuecomment-6374431579) **typescript-automation[bot]** reported CI job statuses for test top400, user test this, run dt, and perf test this faster
 * [today](https://github.com/microsoft/TypeScript/pull/64654#issuecomment-6374817423) **typescript-automation[bot]** informed that the DT test results were ready and unchanged
 * [today](https://github.com/microsoft/TypeScript/pull/64654#issuecomment-6374940097) **typescript-automation[bot]** posted the requested performance run results including detailed comparison metrics between baseline and PR
 * [today](https://github.com/microsoft/TypeScript/pull/64654#issuecomment-6375132212) **typescript-automation[bot]** provided tsc user test results and indicated everything looked good
 * [today](https://github.com/microsoft/TypeScript/pull/64654#issuecomment-6375679362) **typescript-automation[bot]** reported successful tsc comparison between baseline and pr on the top 400 repos

### [PR microsoft/TypeScript#64695](https://github.com/microsoft/TypeScript/pull/64695) (Open, `Domain: Performance`, `For Milestone Bug`, **ahejlsberg**)

**\[experiment\] Skip incompatible discriminants when inferring**

*Experimentally skip incompatible discriminant properties during TypeScript union type inference to reduce workload and validate via tests.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/64695#issuecomment-6340173641) **typescript-automation[bot]** posted performance comparison results for the requested perf run
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64695#issuecomment-6341131824) **typescript-automation[bot]** reported that running the top 400 repos tsc comparison between baseline and pr succeeded without issues
 * [today](https://github.com/microsoft/TypeScript/pull/64695#issuecomment-6363499747) **Andarist** said "@jakebailey could u rerun perf tests here?"
 * [later](https://github.com/microsoft/TypeScript/pull/64695#issuecomment-6384190137) **jakebailey** said "@typescript-bot perf test this faster"
 * [later](https://github.com/microsoft/TypeScript/pull/64695#issuecomment-6384191000) **typescript-automation[bot]** reported starting of performance test jobs and provided links to status and results
 * [later](https://github.com/microsoft/TypeScript/pull/64695#issuecomment-6384500825) **typescript-automation[bot]** posted the requested performance run results comparing baseline to PR metrics

### [Issue microsoft/TypeScript#64706](https://github.com/microsoft/TypeScript/issues/64706) (Open, `Bug`)

**Declaration emit renames value references when a shadowed type parameter shares its parameter's name**

*TypeScript declaration emit incorrectly renames value references in nested functions when inner and outer type parameters share the same name.*

 * [1 week ago](https://github.com/microsoft/TypeScript/issues/64706#issuecomment-6101243821) **maricastroc** reproduced the issue on main, traced it to declaration emit identifier rewriting, and prepared a fix and regression tests while awaiting issue triage before opening a PR per the contribution guidelines
 * (1 week ago) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`
 * [later](https://github.com/microsoft/TypeScript/issues/64706#issuecomment-6384522740) **jasonkuhrt** asked if maricastroc was still planning to open her PR now that the issue was in Backlog and provided ten test cases demonstrating declaration errors and binding issues
 * [later](https://github.com/microsoft/TypeScript/issues/64706#issuecomment-6384981163) **maricastroc** reported opening #64951 with all ten cases added to the regression test and verification of emitted declarations with skipLibCheck: false showing correct behavior

### [PR microsoft/TypeScript#64765](https://github.com/microsoft/TypeScript/pull/64765) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Resolve class and interface members through shared layouts**

*Introduce shared member layouts and lazy resolution for class and interface instantiations to significantly reduce memory usage and symbol creation.*

 * [2 days ago](https://github.com/microsoft/TypeScript/pull/64765#issuecomment-6329169034) **jakebailey** said "@typescript-bot perf test this faster"
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/64765#issuecomment-6329170294) **typescript-automation[bot]** reported that perf test jobs started and shared links to status and results
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/64765#issuecomment-6329797206) **typescript-automation[bot]** provided the performance run results as requested
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64841](https://github.com/microsoft/TypeScript/pull/64841) (Open, `For Backlog Bug`)

**Invalidate declaration state when linked packages change**

*Store signatures of symlinked package directories and package.json entry fields to force declaration rebuilds when linked packages change.*

 * created by **jackeddisciple**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64841#issuecomment-6210106648) **jackeddisciple** said "@microsoft-github-policy-service agree"
 * [later](https://github.com/microsoft/TypeScript/pull/64841#issuecomment-6384522466) **jasonkuhrt** thanked maintainers, described a stale declaration case involving nested package.json files, and asked whether including nested manifests in the PR signature would be appropriate while offering to add a test case
 * [later](https://github.com/microsoft/TypeScript/pull/64841#issuecomment-6384595844) **jackeddisciple** acknowledged the missing nested manifest case and said they would investigate how to include relevant manifests and add a regression test

### [PR microsoft/TypeScript#64871](https://github.com/microsoft/TypeScript/pull/64871) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Speed up short\-lived checker caches**

*Optimize short-lived checker caches by replacing costly Go map clears with generation-counter tables and simpler key hashing for speed improvements.*

 * [4 days ago](https://github.com/microsoft/TypeScript/pull/64871#issuecomment-6273514770) **jakebailey** said "@typescript-bot perf test this faster"
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/64871#issuecomment-6273516583) **typescript-automation[bot]** posted automated build status update
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/64871#issuecomment-6274131092) **typescript-automation[bot]** posted perf run results for baseline..pr including metrics for compiler unions - native scenario such as errors, symbols, types, memory usage, and memory allocations
 * [today](https://github.com/microsoft/TypeScript/pull/64871#issuecomment-6376262146) **jakebailey** said "@typescript-bot perf test"
 * [today](https://github.com/microsoft/TypeScript/pull/64871#issuecomment-6376264609) **typescript-automation[bot]** reported starting of perf test job and provided status and results links
 * [today](https://github.com/microsoft/TypeScript/pull/64871#issuecomment-6379059712) **typescript-automation[bot]** provided performance run results for the requested comparison

### [PR microsoft/TypeScript#64873](https://github.com/microsoft/TypeScript/pull/64873) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Don't resolve mapped type members to find their signatures**

*Avoid resolving mapped type members for signature checks to prevent unnecessary property building and improve compiler performance.*

 * [4 days ago](https://github.com/microsoft/TypeScript/pull/64873#issuecomment-6273551956) **jakebailey** said "@typescript-bot perf test this faster"
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/64873#issuecomment-6273553933) **typescript-automation[bot]** announced that performance tests had started and provided links to status and results
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/64873#issuecomment-6274310316) **typescript-automation[bot]** posted the requested perf run results including a comparison report and detailed metrics
 * [today](https://github.com/microsoft/TypeScript/pull/64873#issuecomment-6376751550) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/64873#issuecomment-6376752833) **typescript-automation[bot]** started the perf test job and posted links to build status and results
 * [today](https://github.com/microsoft/TypeScript/pull/64873#issuecomment-6377132981) **typescript-automation[bot]** posted the performance run results including a detailed comparison report

### [PR microsoft/TypeScript#64915](https://github.com/microsoft/TypeScript/pull/64915) (Closed, `Author: Team`, `For Uncommitted Bug`, **ahejlsberg**)

**Lazy member resolution for class and interface types**

*Add lazy member resolution to classes and interfaces using shared member layouts and improved tuple numeric and length sorting.*

 * [today](https://github.com/microsoft/TypeScript/pull/64915#issuecomment-6368663386) **ahejlsberg** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/64915#issuecomment-6368665114) **typescript-automation[bot]** reported that performance test jobs started and provided status and results links
 * [today](https://github.com/microsoft/TypeScript/pull/64915#issuecomment-6368672452) **ahejlsberg** said "Ok, I think this one is good to go now."
 * [today](https://github.com/microsoft/TypeScript/pull/64915#issuecomment-6369376871) **typescript-automation[bot]** reported successful tsc comparison between baseline and pr on the top 400 repos
 * [today](https://github.com/microsoft/TypeScript/pull/64915#issuecomment-6369533883) **typescript-automation[bot]** provided the results of the requested performance run
 * [today](https://github.com/microsoft/TypeScript/pull/64915#issuecomment-6372477794) **ahejlsberg** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/64915#issuecomment-6372479624) **typescript-automation[bot]** posted an automated build status update with job commands and their statuses and results
 * [today](https://github.com/microsoft/TypeScript/pull/64915#issuecomment-6372892850) **typescript-automation[bot]** reported that the DT tests completed with no changes
 * [today](https://github.com/microsoft/TypeScript/pull/64915#issuecomment-6372985218) **typescript-automation[bot]** provided tsc user test results and indicated everything looked good
 * [today](https://github.com/microsoft/TypeScript/pull/64915#issuecomment-6373034810) **typescript-automation[bot]** posted performance run results in a detailed comparison table
 * (today) **ahejlsberg** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/64915#issuecomment-6373888937) **typescript-automation[bot]** reported successful tsc comparison between baseline and pr on the top 400 repos

### [PR microsoft/TypeScript#64934](https://github.com/microsoft/TypeScript/pull/64934) (Open, `Domain: Performance`, `For Uncommitted Bug`)

**Skip discriminant lookups for unions that cannot be narrowed**

*Optimize union type checking by skipping discriminant lookups for unions that cannot be narrowed.*

 * (today) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64934#issuecomment-6363070994) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [later](https://github.com/microsoft/TypeScript/pull/64934#issuecomment-6384201731) **jakebailey** said "@typescript-bot perf test this faster"
 * [later](https://github.com/microsoft/TypeScript/pull/64934#issuecomment-6384202614) **typescript-automation[bot]** triggered performance test jobs and provided status and result links
 * [later](https://github.com/microsoft/TypeScript/pull/64934#issuecomment-6385070155) **typescript-automation[bot]** provided the requested performance run results

### [PR microsoft/TypeScript#64935](https://github.com/microsoft/TypeScript/pull/64935) (Open, `For Backlog Bug`)

**Don't measure type parameters as independent through circular variance lookups**

*Correct circular variance computation to disallow incompatible assignments between mutually recursive type aliases.*

 * created by **jasleenkaur-qed42**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/64935#issuecomment-6385915607) **ahejlsberg** said "@typescript-bot test it"
 * [later](https://github.com/microsoft/TypeScript/pull/64935#issuecomment-6385916749) **typescript-automation[bot]** reported CI jobs as started and provided links to results
 * [later](https://github.com/microsoft/TypeScript/pull/64935#issuecomment-6386179655) **typescript-automation[bot]** reported DT test results and branch-only TypeScript compile errors for react-relay
 * [later](https://github.com/microsoft/TypeScript/pull/64935#issuecomment-6386240501) **typescript-automation[bot]** provided perf run results for @ahejlsberg
 * [later](https://github.com/microsoft/TypeScript/pull/64935#issuecomment-6386252039) **typescript-automation[bot]** reported differences in user test results comparing baseline and PR and requested review

### [Issue microsoft/TypeScript#64937](https://github.com/microsoft/TypeScript/issues/64937) (Open, `Bug`, `Domain: LS: Signature Help`)

**Signature help shows no JSDoc for a \`const\` with a function type annotation**

*Signature help in TypeScript 7 fails to display JSDoc descriptions for parameters of a const variable declared with a function type annotation.*

 * created by **andreww2012**
 * [later](https://github.com/microsoft/TypeScript/issues/64937#issuecomment-6382147151) **MadalinWolf** opened a PR to add a fallback for JSDoc retrieval from const declarations, added a regression test, and confirmed the focused test passed

### [Issue microsoft/TypeScript#64938](https://github.com/microsoft/TypeScript/issues/64938) (Open, `Suggestion`)

**Defining a type with inferred generic parameters**

*Allow an infer keyword in generic type definitions to automatically inherit parameter constraints and defaults from referenced types.*

 * created by **denis-migdal**
 * [today](https://github.com/microsoft/TypeScript/issues/64938#issuecomment-6371549094) **MartinJohns** said "Duplicate of #29469."
 * [today](https://github.com/microsoft/TypeScript/issues/64938#issuecomment-6380324447) **denis-migdal** proposed a type inference proposal for generic constraints, outlined potential issues with backwards flow of constraints, and presented alternative syntax solutions

### [Issue microsoft/TypeScript#64939](https://github.com/microsoft/TypeScript/issues/64939) (Open, `Bug`)

**Formatter README links rules\.ts and names createRulesMap, which the Go port does not have**

*The formatter README links to rules.ts and createRulesMap, which aren't in the Go port that uses rules.go, getRules, and buildRulesMap.*

 * created by **lgriffin**

### [PR microsoft/TypeScript#64940](https://github.com/microsoft/TypeScript/pull/64940) (Open, `For Backlog Bug`)

**Fix/format readme go names**

*Update internal/format/README.md to correct Go formatter links and rule names and add a test verifying README matches code*

 * created by **lgriffin**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64940#issuecomment-6372282108) **lgriffin** said "@microsoft-github-policy-service agree"

### [PR microsoft/TypeScript#64941](https://github.com/microsoft/TypeScript/pull/64941) (Open, `For Backlog Bug`)

**Don't reuse removed synthetic program IDs in the same update**

*Ensure synthetic program IDs removed earlier in the same snapshot update aren’t reused to prevent nil dereference crashes*

 * created by **jackeddisciple**
 * (today) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`

### [PR microsoft/TypeScript#64942](https://github.com/microsoft/TypeScript/pull/64942) (Open, `Domain: Performance`, `For Uncommitted Bug`)

**Add program\.getAllDependencies to the API**

*Add program.getAllDependencies(file) to TypeScript's APIs to retrieve a file's full dependency graph using tsc's incremental builder data.*

 * created by **jackeddisciple**
 * (today) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`

### [Issue microsoft/TypeScript#64943](https://github.com/microsoft/TypeScript/issues/64943) (Open)

**File changed on disk with a content\-mapped or \`\.d\.ts\` extension never triggers workspace/diagnostic/refresh**

*Modifying disk files with content-mapped or .d.ts extensions fails to trigger diagnostic refresh notifications in the TypeScript server*

 * created by **mrlubos**

### [PR microsoft/TypeScript#64944](https://github.com/microsoft/TypeScript/pull/64944) (Open, `For Uncommitted Bug`)

**Refresh diagnostics when a content\-mapped or declaration file changes on disk**

*Ensure diagnostics are refreshed when content-mapped or .d.ts files change on disk, correcting path.Extension misdetection*

 * created by **mrlubos**
 * (today) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64944#issuecomment-6374657128) **mrlubos** said "@microsoft-github-policy-service agree company="Hey API""

### [PR microsoft/TypeScript#64945](https://github.com/microsoft/TypeScript/pull/64945) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Avoid re\-sorting spread members from scratch**

*Optimize spread member sorting to avoid complete re-sorts from scratch and improve performance.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/64945#issuecomment-6376031946) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/64945#issuecomment-6376033139) **typescript-automation[bot]** started CI perf test jobs and provided status and results links
 * [today](https://github.com/microsoft/TypeScript/pull/64945#issuecomment-6376472740) **typescript-automation[bot]** provided the performance run results
 * [today](https://github.com/microsoft/TypeScript/pull/64945#issuecomment-6376570279) **jakebailey** said "Yeah no"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64946](https://github.com/microsoft/TypeScript/pull/64946) (Open, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Remove checker pointer from Type**

*Removing the checker pointer from the Type structure and placing it in LazyState reduces Type’s memory footprint from 40 to 32 bytes.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/64946#issuecomment-6376206901) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/64946#issuecomment-6376208030) **typescript-automation[bot]** reported start of performance tests and provided build status links
 * [today](https://github.com/microsoft/TypeScript/pull/64946#issuecomment-6376663737) **typescript-automation[bot]** reported perf run results requested by @jakebailey
 * [today](https://github.com/microsoft/TypeScript/pull/64946#issuecomment-6376728957) **jakebailey** said "Pretty disappointing, but I also didn't check the size class, and then also I don't think we allocate these in arenas"

### [Issue microsoft/TypeScript#64947](https://github.com/microsoft/TypeScript/issues/64947) (Open, `Needs Investigation`)

**\[ServerErrors\]\[JavaScript\] main**

*The main CI pipeline detected server errors during JavaScript analysis of 300 popular TypeScript repositories, yielding 4 interesting changes, 226 unchanged results, 42 timeouts, and 28 failures.*

 * created by **typescript-automation[bot]**
 * [today](https://github.com/microsoft/TypeScript/issues/64947#issuecomment-6376748522) **typescript-automation[bot]** reported a panic in textDocument/diagnostic handling and provided logs for the affected repo
 * [today](https://github.com/microsoft/TypeScript/issues/64947#issuecomment-6376749193) **typescript-automation[bot]** reported that the server connection closed prematurely with undefined error and included affected repos, raw error text, last requests, and repro steps
 * [today](https://github.com/microsoft/TypeScript/issues/64947#issuecomment-6376749773) **typescript-automation[bot]** reported a server connection closing prematurely with undefined error and included affected repo details, artifacts, old results, and recent requests
 * [today](https://github.com/microsoft/TypeScript/issues/64947#issuecomment-6376750359) **typescript-automation[bot]** reported a server connection closed prematurely error with logs and repro steps for nosir/cleave.js

### [Issue microsoft/TypeScript#64948](https://github.com/microsoft/TypeScript/issues/64948) (Closed, `Won't Fix`)

**Stack overflow in getEffectsSignature for long comma\-separated call chains \(e\.g\. minified bundles with allowJs\)**

*Very long comma-separated call chains in minified JS with allowJs cause getEffectsSignature to overflow the call stack.*

 * created by **u9g**
 * [today](https://github.com/microsoft/TypeScript/issues/64948#issuecomment-6379651574) **AbbasFullstack** said "I would like to fix it "
 * [today](https://github.com/microsoft/TypeScript/issues/64948#issuecomment-6379712381) **AbbasFullstack** said "Ah, I see you already have a patch ready on your branch — I'll leave this one to you. Looking forward to the fix!"
 * [today](https://github.com/microsoft/TypeScript/issues/64948#issuecomment-6379725408) **AbbasFullstack** said "If you need any type help tell me I am 24/7  for help"

### [PR microsoft/TypeScript#64949](https://github.com/microsoft/TypeScript/pull/64949) (Open, `For Backlog Bug`)

**Fix signature help docs for const function types**

*Add fallback documentation lookup so JSDoc comments on const function type annotations appear in signature help.*

 * created by **MadalinWolf**
 * (later) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/64949#issuecomment-6382102547) **MadalinWolf** said "@microsoft-github-policy-service agree"

### [Issue microsoft/TypeScript#64950](https://github.com/microsoft/TypeScript/issues/64950) (Open, `Bug`)

**7\.1 regression: comparing a recursive \`\-?\` mapped type is quadratic in the number of properties and hits TS2589 \(since typescript\-go\#4820\)**

*A TypeScript 7.1 regression makes comparing recursive '-?' mapped types incur quadratic instantiation growth and hit TS2589 errors.*

 * created by **matej21**
 * [later](https://github.com/microsoft/TypeScript/issues/64950#issuecomment-6385437712) **matej21** provided follow-up analysis of TypeScript 7.0/7.1 variance measurement issue, demonstrated how declaration order and -? mapped types affect soundness and performance, related it to issues #64930 and #64935, and suggested declaring variance to restore performance

### [PR microsoft/TypeScript#64951](https://github.com/microsoft/TypeScript/pull/64951) (Open, `For Backlog Bug`)

**Fix declaration emit renaming value references to shadowed type parameters**

*Limits declaration emit renaming to type parameters only to avoid incorrect renaming of value references to shadowed type parameters.*

 * created by **maricastroc**
 * **typescript-automation[bot]** added label `For Backlog Bug`

### [PR microsoft/TypeScript#64952](https://github.com/microsoft/TypeScript/pull/64952) (Open, `For Backlog Bug`)

**Fix declaration emit crash on inaccessible heritage types**

*Handle inaccessible heritage types in exported interfaces to prevent declaration emit crashes and reuse diagnostics*

 * created by **chengchuu**
 * **typescript-automation[bot]** added label `For Backlog Bug`

