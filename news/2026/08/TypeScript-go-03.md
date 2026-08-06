# Report for 2026-08-03 (Monday, August 3rd, 2026)

19 different users commented on 18 different issues.

## Recommended Actions

 * Response Recommended
    * @Princesseuh provided examples and explanation of TS/JS blocks behavior in Astro files in [microsoft/TypeScript-go#2824](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-5170503808)
    * @jasonlyu123 asked for feedback on completion position mapping and overlapping span constraints in [microsoft/TypeScript-go#4712](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5175223764)
    * @rkistner asked if @haines saw the same high CPU usage and delay after building in [microsoft/TypeScript-go#4795](https://github.com/microsoft/TypeScript-go/issues/4795#issuecomment-5177559893)
    * @rkistner reported that using 7.1.0-dev.20260804.1 resolved the issue in [microsoft/TypeScript-go#4795](https://github.com/microsoft/TypeScript-go/issues/4795#issuecomment-5177625279)
    * @mj026 offered to provide a PR for suggested implementation in [microsoft/TypeScript-go#4809](https://github.com/microsoft/TypeScript-go/issues/4809#issuecomment-5181165788)
    * @typescript-automation[bot] provided perf run results as requested in [microsoft/TypeScript-go#4825](https://github.com/microsoft/TypeScript-go/pull/4825#issuecomment-5175461378)

## Activity Summary

### [Issue microsoft/TypeScript-go#2824](https://github.com/microsoft/TypeScript-go/issues/2824) (Open, `Domain: API and Extensibility`, **andrewbranch**)

**API usage patterns for complex editor extensions**

*Exploring IPC-based API features for a Go TS server to replace TS Server plugins and support Vue editor extensions*

 * [6 days ago](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-5108638364) **Princesseuh** clarified that Astro supports script tags of multiple languages within a file, works like HTML, and noted it was a blocker
 * [6 days ago](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-5109564324) **DanielRosenwasser** asked if resources or examples were available for multiple TS/JS blocks in an Astro file and what an importer received when handling them
 * [today](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-5166713919) **Mad-Kat** described migrating TS Server plugins and distribution challenges, contrasted current tsconfig-based integration with LSP-plus-editor extensions, and asked if a sidecar model would be on the table
 * [today](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-5170503808) **Princesseuh** apologized for the late answer and explained how multiple TS/JS script blocks in an Astro file share scope or isolate modules and compile to a single default export
 * [today](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-5170697901) **NullVoxPopuli** explained Ember component format in glimmer-ts preserving block scope semantics and provided code examples

### [PR microsoft/TypeScript-go#4309](https://github.com/microsoft/TypeScript-go/pull/4309) (Closed)

**feat\(4294\): report deprecated diagnostics for contextual props**

*Report deprecation diagnostics for contextual props in the TypeScript compiler.*

 * [7 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4309#issuecomment-4711946557) **typescript-automation[bot]** reported that the perf test job started and provided status and results links
 * [7 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4309#issuecomment-4712154519) **typescript-automation[bot]** provided the requested performance run comparison report
 * (5 days ago) **weswigham** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/4309#issuecomment-5171747621) **jakebailey** said "This PR is causing some sort of OOM per @walkerdb so probably needs to be reverted. Not sure if we have a test case yet."
 * [today](https://github.com/microsoft/TypeScript-go/pull/4309#issuecomment-5172296443) **jakebailey** said "I think I have a fix through deferring these diags until later. Though, it might use too much memory..."

### [PR microsoft/TypeScript-go#4313](https://github.com/microsoft/TypeScript-go/pull/4313) (Open)

**Assign checkers with cost/import\-aware algorithm**

*Develop a cost- and import-aware algorithm to assign diagnostic checkers more efficiently.*

 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/4313#issuecomment-5149687534) **jakebailey** said "@typescript-bot perf test this faster"
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/4313#issuecomment-5149687767) **typescript-automation[bot]** reported that perf test started and provided build and results links
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/4313#issuecomment-5149784101) **typescript-automation[bot]** reported the performance run results in a comparison report
 * [today](https://github.com/microsoft/TypeScript-go/pull/4313#issuecomment-5172557530) **walkerdb** reported that after reverting PR 4309, the build ran ~10% faster and used ~10% less RAM on a large monorepo

### [PR microsoft/TypeScript-go#4712](https://github.com/microsoft/TypeScript-go/pull/4712) (Open)

**Content mappers**

*Enable TypeScript content mappers to integrate unsupported file types by transforming and mapping them through tsconfig configuration.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5078512064) **mikearnaldi** explained that patch 0002 was incomplete, described mapping ambiguity at span boundaries requiring left/right affinity, and noted that his patch enabled completions at file end but might not be correct
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5086629187) **jasonlyu123** inquired whether the LSP-connected IPC API parameters should use generated or source positions and if purely generated positions could be requested
 * [6 days ago](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5109758000) **remcohaszing** praised the PR's start and offered feedback on content-mapped file emission, suggesting handling for MDX and declaration maps, questioning how emit should work with mapped files, and noting SpanMapping length differences and potential Volar compatibility issues
 * [today](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5175223764) **jasonlyu123** described issues with completion position mapping and span mapping constraints in Svelte transformations and asked for feedback on treating completion positions as range ends and on overlapping segment rules
 * [later](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5180574756) **andrewbranch** acknowledged the same mapping issue, noted a stashed fix, thanked for the example, asked if spans should be broken into tokens or kept contiguous, and recommended using minimal spans

### [PR microsoft/TypeScript-go#4714](https://github.com/microsoft/TypeScript-go/pull/4714) (Open, **andrewbranch**)

**feat\(47595\): allow using private fields in type queries**

*Enable referencing private class fields in TypeScript type queries.*

 * created by **a-tarasyuk**
 * **RyanCavanaugh** assigned to **andrewbranch**

### [Issue microsoft/TypeScript-go#4795](https://github.com/microsoft/TypeScript-go/issues/4795) (Open, `Needs More Info`)

**\`tsc \-\-watch\` doesn't recompile on file change**

*TypeScript 7.0.2 stops tsc --build --watch from detecting file changes in a monorepo*

 * created by **haines**
 * (3 days ago) **RyanCavanaugh** added label `Needs More Info`, and set milestone to `Need More Info`
 * [later](https://github.com/microsoft/TypeScript-go/issues/4795#issuecomment-5177559893) **rkistner** provided reproduction steps and described a 45s hang after tsc -b -w, then asked if the maintainer saw the same high CPU usage and delay
 * [later](https://github.com/microsoft/TypeScript-go/issues/4795#issuecomment-5177578927) **jakebailey** said "Can you please try the nightly instead of 7.0.2?"
 * [later](https://github.com/microsoft/TypeScript-go/issues/4795#issuecomment-5177625279) **rkistner** said "@jakebailey Using 7.1.0-dev.20260804.1 appears to resolve the issue for me: No high CPU usage after building; detecting changes and Ctrl+C run instantly."
 * [later](https://github.com/microsoft/TypeScript-go/issues/4795#issuecomment-5177810224) **haines** confirmed the high CPU usage after building and noted that the dev version resolved the issue for them

### [Issue microsoft/TypeScript-go#4809](https://github.com/microsoft/TypeScript-go/issues/4809) (Open, `Crash`, **jakebailey**, **Copilot**)

**LSP exits when parent process PID is not found**

*LSP’s parent-PID watchdog terminates the server when the PID can’t be found in Docker, with a CLI flag to disable it.*

 * (3 days ago) **jakebailey** assigned to **Copilot**, **jakebailey**
 * **RyanCavanaugh** added to milestone `Post-7.0`
 * [later](https://github.com/microsoft/TypeScript-go/issues/4809#issuecomment-5181165788) **mj026** noted that vscode language servers have similar behavior with a parent process watchdog and suggested using the --clientProcessId option instead of removing it; offered to provide a PR

### [PR microsoft/TypeScript-go#4813](https://github.com/microsoft/TypeScript-go/pull/4813) (Closed)

**Avoid false symlink mappings for physical dependencies**

*Declaration emit incorrectly reused unrelated JSDoc imports after physical dependencies were falsely mapped as symlinks, now fixed.*

 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/4813#issuecomment-5149895116) **typescript-automation[bot]** posted CI job status updates with links to build results
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/4813#issuecomment-5149982230) **typescript-automation[bot]** reported the requested performance run results including tsc comparison metrics
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/4813#issuecomment-5150134780) **typescript-automation[bot]** reported that running tsc on the top 400 repos showed no differences between main and the PR merge
 * (today) **weswigham** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/4813#issuecomment-5173745809) **platypii** said "thanks for fixing this so quickly! this fixes the issue I was hitting with my published libraries 🙌 "

### [Issue microsoft/TypeScript-go#4819](https://github.com/microsoft/TypeScript-go/issues/4819) (Closed)

**tsgo never terminates on a single three\.js TSL method call \(works in 5\.9\.3 and 6\.0\.3\)**

*tsgo 7.x hangs indefinitely on a single three.js TSL vec3(...).mul(2) call, while TypeScript 5.9.3 and 6.0.3 complete quickly*

 * created by **alexcz-a11y**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4819#issuecomment-5170414607) **RyanCavanaugh** guessed the issue stemmed from using a conditional type instead of a lookup type and linked to the relevant code segment
 * [today](https://github.com/microsoft/TypeScript-go/issues/4819#issuecomment-5175031885) **ahejlsberg** said "Looks related to (if not a duplicate of) #4528."

### [PR microsoft/TypeScript-go#4820](https://github.com/microsoft/TypeScript-go/pull/4820) (Closed)

**Order variance computation by associated type symbol**

*Variance computation is now ordered by associated type symbol to ensure stable results for circular generic types.*

 * created by **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4820#issuecomment-5169094497) **ahejlsberg** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4820#issuecomment-5169095560) **typescript-automation[bot]** reported CI jobs as started and provided links to results
 * [today](https://github.com/microsoft/TypeScript-go/pull/4820#issuecomment-5169384709) **typescript-automation[bot]** posted the results of the requested performance run including a comparison report for compiler metrics
 * [today](https://github.com/microsoft/TypeScript-go/pull/4820#issuecomment-5169847286) **typescript-automation[bot]** reported that running tsc on the top 400 repos comparing main and the pull request merge showed everything looked good
 * [today](https://github.com/microsoft/TypeScript-go/pull/4820#issuecomment-5175460718) **ahejlsberg** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4820#issuecomment-5175461343) **typescript-automation[bot]** reported CI jobs status and provided results links
 * [later](https://github.com/microsoft/TypeScript-go/pull/4820#issuecomment-5175676225) **typescript-automation[bot]** provided the perf run results requested by @ahejlsberg
 * [later](https://github.com/microsoft/TypeScript-go/pull/4820#issuecomment-5176061745) **typescript-automation[bot]** reported that running tsc on the top 400 repos comparing main and the pull request merge showed everything looked good

### [PR microsoft/TypeScript-go#4821](https://github.com/microsoft/TypeScript-go/pull/4821) (Closed, **RyanCavanaugh**, **Copilot**)

**Fix TS1308 suppressed for \`await\` in computed property names of exported namespace classes**

*TS1308 errors were incorrectly suppressed for await in computed property names of exported namespace classes.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**

### [Issue microsoft/TypeScript-go#4822](https://github.com/microsoft/TypeScript-go/issues/4822) (Open, `Needs Investigation`, **andrewbranch**)

**Add batched assignability checks into the \`Checker API\`**

*Add batched type assignability checks and optional quantifiers to the Checker API for improved performance.*

 * created by **artem1458**

### [PR microsoft/TypeScript-go#4823](https://github.com/microsoft/TypeScript-go/pull/4823) (Open, **RyanCavanaugh**, **Copilot**)

**Preserve await context for exported classes in nested containers**

*Restrict await context for exported classes to top-level declarations while preserving it within async functions and generators.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4823#issuecomment-5171393580) **Copilot** explained that export class was removed from invalid test locations and updated tests to use plain class in nested contexts while retaining export class only where syntactically legal

### [Issue microsoft/TypeScript-go#4824](https://github.com/microsoft/TypeScript-go/issues/4824) (Open, `bug`, **jakebailey**)

**ram use regression from new @deprecated diagnostics**

*A recent @deprecated diagnostics change nearly doubled tsgo’s memory usage causing OOM errors on large monorepos.*

 * created by **walkerdb**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4824#issuecomment-5172376557) **jakebailey** demonstrated that issue #4309 triggered unexpected diagnostics and provided a test case

### [PR microsoft/TypeScript-go#4825](https://github.com/microsoft/TypeScript-go/pull/4825) (Open)

**Fix deprecated contextual property memory regression**

*Update deprecation diagnostics to prevent memory ballooning from deferred processing and discard duplicate entries.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4825#issuecomment-5172669357) **walkerdb** tested the branch on a large private repo and reported it fixed the RAM regression with memory usage similar to main
 * [today](https://github.com/microsoft/TypeScript-go/pull/4825#issuecomment-5173533460) **weswigham** suggested reusing checkNodeDeferred in checkObjectLiteral and checkJsxAttributes and implementing checkDeferredNode to handle contextual types and deprecated property checks
 * [today](https://github.com/microsoft/TypeScript-go/pull/4825#issuecomment-5175249558) **jakebailey** confirmed that it worked while using more memory and requested the TypeScript bot to run a performance test
 * [today](https://github.com/microsoft/TypeScript-go/pull/4825#issuecomment-5175250058) **typescript-automation[bot]** indicated that performance tests started and provided links to status and results
 * [today](https://github.com/microsoft/TypeScript-go/pull/4825#issuecomment-5175461378) **typescript-automation[bot]** posted requested perf run results

### [Issue microsoft/TypeScript-go#4826](https://github.com/microsoft/TypeScript-go/issues/4826) (Open, `bug`, **RyanCavanaugh**, **iisaduan**, **Copilot**)

**\[lsp\] Go to Definition returns sources\[0\] of the declaration map instead of the mapped source file**

*Go to Definition returns the first declaration map source instead of the mapped source file in TypeScript LSP.*

 * created by **flosrn**

### [Issue microsoft/TypeScript-go#4827](https://github.com/microsoft/TypeScript-go/issues/4827) (Closed, `Type Ordering`)

**Generic type argument inferred from the wrong inference slot \(cyclic union\-of\-intersections\); larger programs show scheduling\-dependent diagnostics**

*tsgo incorrectly infers a generic type argument from the wrong inference slot in a cyclic union-of-intersections, leading to inconsistent diagnostics in larger programs.*

 * created by **bel0v**

### [PR microsoft/TypeScript-go#4828](https://github.com/microsoft/TypeScript-go/pull/4828) (Open, `dependencies`, `javascript`)

**Bump undici from 7\.28\.0 to 7\.29\.0**

*Upgrade undici from 7.28.0 to 7.29.0 to address high and medium severity security vulnerabilities.*

 * created by **dependabot[bot]**
 * (later) **dependabot[bot]** added labels `dependencies`, `javascript`, `dependencies`, `javascript`

