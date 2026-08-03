# Report for 2026-07-29 (Wednesday, July 29th, 2026)

12 different users commented on 34 different issues.

## Recommended Actions

 * Response Recommended
    * @typescript-automation[bot] provided the requested performance results in [microsoft/TypeScript-go#4781](https://github.com/microsoft/TypeScript-go/pull/4781#issuecomment-5121063379)

## Activity Summary

### [Issue microsoft/TypeScript-go#4294](https://github.com/microsoft/TypeScript-go/issues/4294) (Closed, `possible improvement`)

**Object literal properties checked against a contextual type don't get \`@deprecated\` suggestions**

*Object literal properties checked against a deprecated contextual type do not trigger deprecation suggestions.*

 * created by **u9g**
 * (6 weeks ago) **RyanCavanaugh** added label `possible improvement`, and set milestone to `Possible Improvement`
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript-go#4309](https://github.com/microsoft/TypeScript-go/pull/4309) (Closed)

**feat\(4294\): report deprecated diagnostics for contextual props**

*Report deprecation diagnostics for contextual props in the TypeScript compiler.*

 * [6 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4309#issuecomment-4711945750) **jakebailey** said "@typescript-bot perf test this"
 * [6 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4309#issuecomment-4711946557) **typescript-automation[bot]** reported that the perf test job started and provided status and results links
 * [6 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4309#issuecomment-4712154519) **typescript-automation[bot]** provided the requested performance run comparison report
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript-go#4399](https://github.com/microsoft/TypeScript-go/pull/4399) (Closed)

**Watcher performance improvements**

*Implement single-file program reuse, skip redundant operations, and track rebuild requirements with watchSetDirty to improve watcher performance.*

 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4399#issuecomment-4773796433) **jakebailey** said "Do you have any data about how this affects things?"
 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4399#issuecomment-4780787469) **johnfav03** provided benchmark results showing single-file edits had a 50% rebuild time decrease and higher-volume edits saw about 10% improvement
 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4399#issuecomment-4783318074) **jakebailey** provided two focused tests that reproduced correctness regressions in the watcher fast path
 * (today) **johnfav03** closed the issue

### [Issue microsoft/TypeScript-go#4525](https://github.com/microsoft/TypeScript-go/issues/4525) (Closed, `possible improvement`, `Needs Investigation`, **weswigham**)

**Follow\-up on issues/4254: \`typeof\` emit does not happen in \`export const { \.\.\. } = default\`**

*tsgo’s declaration emitter incorrectly inlines function signatures instead of using typeof when destructuring and exporting properties from a default export.*

 * [6 days ago](https://github.com/microsoft/TypeScript-go/issues/4525#issuecomment-5061625407) **weswigham** asked if there was no bug and if the proposal was to stop flattening binding patterns in declaration emit
 * [6 days ago](https://github.com/microsoft/TypeScript-go/issues/4525#issuecomment-5062019310) **hkleungai** acknowledged correctness of current implementation, questioned the legitimacy of the export declare syntax, and suggested a code fix to avoid duplicating the bar declaration that breaks typeof emit reuse
 * **weswigham** added label `possible improvement`
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript-go#4555](https://github.com/microsoft/TypeScript-go/pull/4555) (Open)

**Add batched version for several API functions\.**

*Add batched versions of several API functions to reduce IPC overhead and improve performance.*

 * created by **dragomirtitian**
 * [later](https://github.com/microsoft/TypeScript-go/pull/4555#issuecomment-5129174620) **dragomirtitian** agreed that a generic batching API would be useful, noted that their sync API use precludes next-tick batching, and described their existing batching library

### [PR microsoft/TypeScript-go#4577](https://github.com/microsoft/TypeScript-go/pull/4577) (Closed, **iisaduan**)

**Fix stack overflow in inherited JSDoc resolution**

*Resolving inherited JSDoc without cycle detection can cause infinite recursion and stack overflow on circular class references.*

 * created by **johnfav03**
 * **RyanCavanaugh** assigned to **iisaduan**
 * (today) **johnfav03** closed the issue

### [Issue microsoft/TypeScript-go#4579](https://github.com/microsoft/TypeScript-go/issues/4579) (Closed)

**tsgo typechecks slower than TS6**

*tsgo typechecking is over five times slower than TypeScript 6 on the same codebase.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/4579#issuecomment-4970222219) **ahejlsberg** said "@XiNiHa Yes, the behavior is expected. TS6 would similarly slow down if the changes in #3445 were applied to that codebase. The core problem is the complexity and expense of the types."
 * (1 week ago) **RyanCavanaugh** closed the issue
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/4579#issuecomment-5000192828) **igalklebanov** described simplified helper function variants that reduced TypeScript instantiation counts without losing type safety
 * [later](https://github.com/microsoft/TypeScript-go/issues/4579#issuecomment-5130306466) **koskimas** described working on a fix for Kysely that accelerates TypeScript 7 performance, removed infinite recursion from types, and directed to issue #1947 for progress

### [Issue microsoft/TypeScript-go#4610](https://github.com/microsoft/TypeScript-go/issues/4610) (Closed, `Domain: Editor`, `Needs Investigation`, **johnfav03**)

**Renaming a file can be very slow in some edge cases**

*VSCode tsgo file renames can be slow because a third-party .d.ts with repeated imports triggers quadratic path-updater scans.*

 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/4610#issuecomment-5094530293) **johnfav03** explained that he implemented a fix precomputing the moved-files set once per rename to optimize unresolved import scanning and described why this approach was chosen based on resolutionMode differences
 * (2 days ago) **johnfav03** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/issues/4610#issuecomment-5118640325) **swotvibe** explained that resolutionMode can differ between import syntaxes and advocated precomputing the moved-files list for renaming; asked if the moved-files list was derived from oldToNew tracking or required a separate pass
 * [today](https://github.com/microsoft/TypeScript-go/issues/4610#issuecomment-5121696152) **johnfav03** explained that oldToNew didn't track paths and described using an O(files) upfront pass to collect moved files, noted the performance improvement over the previous O(files × imports) approach, and linked to the merged PR diff

### [Issue microsoft/TypeScript-go#4614](https://github.com/microsoft/TypeScript-go/issues/4614) (Closed, `Needs Investigation`, **johnfav03**)

**\`tsc \-b \-\-watch\` takes tens of seconds to start watching on a large project\-references solution \(\`computeDesiredWatches\` is O\(files × dirs\)\)**

*tsc -b --watch stalls for tens of seconds on large project-reference solutions because computeDesiredWatches’s O(files×dirs) logic delays filesystem watch registration*

 * (2 weeks ago) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.1`, and assigned to **johnfav03**
 * (today) **johnfav03** closed the issue

### [PR microsoft/TypeScript-go#4658](https://github.com/microsoft/TypeScript-go/pull/4658) (Closed)

**Fix build mode setup stall on large solutions**

*Introduce DirWatchSet to optimize computeDesiredWatches and reduce filesystem watch registration time in large tsc -b --watch solutions.*

 * created by **johnfav03**
 * (today) **johnfav03** closed the issue

### [PR microsoft/TypeScript-go#4699](https://github.com/microsoft/TypeScript-go/pull/4699) (Closed)

**API emit**

*Add program.emit, program.emitToString, getJavaScriptEmit, and getDeclarationEmit methods for flexible file system and in-memory emissions.*

 * **DanielRosenwasser** added to milestone `TypeScript 7.1`
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4699#issuecomment-5103710645) **johnnyreilly** said "As far as I can tell, there's no support for project references as yet - am I reading that correctly? asking for https://github.com/TypeStrong/ts-loader/pull/1704"
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4699#issuecomment-5105156480) **pfumagalli** asked what was meant by “project references” and explained that type checking across referenced projects works like createProgram but a solution builder (tsc --build) is not implemented yet
 * [today](https://github.com/microsoft/TypeScript-go/pull/4699#issuecomment-5123395586) **johnnyreilly** clarified he referred to the old createSolutionBuilder API, noted the new API worked well outside of custom transformers and project references, and shared a link to a PR

### [PR microsoft/TypeScript-go#4711](https://github.com/microsoft/TypeScript-go/pull/4711) (Closed)

**Optimize \`getAssignmentReducedType\` in CFA**

*Optimize getAssignmentReducedType to eliminate quadratic performance when processing large union types in control flow analysis.*

 * (6 days ago) **ahejlsberg** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/4711#issuecomment-5119861650) **ahejlsberg** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4711#issuecomment-5119862426) **typescript-automation[bot]** started a performance test job and posted an initial build status table
 * [today](https://github.com/microsoft/TypeScript-go/pull/4711#issuecomment-5120807868) **ahejlsberg** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4711#issuecomment-5120808792) **typescript-automation[bot]** reported that the 'perf test this faster' job started and would update status as builds progressed

### [Issue microsoft/TypeScript-go#4748](https://github.com/microsoft/TypeScript-go/issues/4748) (Open, `Needs More Info`)

**Panic: nil pointer in NodeList\.HasTrailingComma during incremental rebuild \(build\-mode declaration printer\) — 7\.0\.2 and current nightly**

*A nil pointer dereference in NodeList.HasTrailingComma triggers a panic during incremental build-mode declaration printing in TypeScript.*

 * created by **nikeedw**
 * (yesterday) **RyanCavanaugh** added label `Needs More Info`, and set milestone to `Need More Info`
 * [today](https://github.com/microsoft/TypeScript-go/issues/4748#issuecomment-5121048546) **RyanCavanaugh** requested repro steps and suggested bisecting to an anonymized code subset

### [Issue microsoft/TypeScript-go#4758](https://github.com/microsoft/TypeScript-go/issues/4758) (Closed)

**disableSourceOfProjectReferenceRedirect causes lodash per\-method submodule import to resolve to the wrong function**

*Enabling disableSourceOfProjectReferenceRedirect in a referenced TypeScript project causes lodash/get imports to resolve as lodash/set under tsgo.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/4758#issuecomment-5107123401) **jakebailey** said "Are you running an old version? I think this was fixed in #4008. Are you running an old build for PnP or something?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/4758#issuecomment-5114848844) **valentinmelusson** explained they were testing the prototype PR in their Datadog frontend repo, noted everything else worked and they were investigating whether the error was on their side, and confirmed their binary included commits through July 15
 * [today](https://github.com/microsoft/TypeScript-go/issues/4758#issuecomment-5118037769) **valentinmelusson** described finding the root cause in Yarn PnP integration and implementing a fix with regression tests
 * [today](https://github.com/microsoft/TypeScript-go/issues/4758#issuecomment-5121056093) **RyanCavanaugh** said "Thanks!"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#4768](https://github.com/microsoft/TypeScript-go/issues/4768) (Closed)

**TS7023 false positive: contextual return type ignored when a recursive call is assigned to a union\-annotated local**

*TypeScript incorrectly reports TS7023 on a contextually typed recursive function when assigning its call to a union-typed variable.*

 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/4768#issuecomment-5098140502) **RyanCavanaugh** noted that CHANGES.md already describes JSDoc support as being more based on TS and that changes aligning with TS behavior need no additional justification unless there's a strong positive case
 * (2 days ago) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/issues/4768#issuecomment-5114355431) **ljharb** expressed confusion about the behavior change across TypeScript versions and suggested that failing in JS constitutes a regression
 * [today](https://github.com/microsoft/TypeScript-go/issues/4768#issuecomment-5122501079) **RyanCavanaugh** emphasized that JS support should be consistent with TS semantics to avoid maintaining two sets of semantics

### [PR microsoft/TypeScript-go#4775](https://github.com/microsoft/TypeScript-go/pull/4775) (Closed)

**Retain uninitialized binding patterns for variable declarations in declaration emit**

*Retain uninitialized binding patterns in declaration emit to support exporting binding patterns as isolatedDeclarations.*

 * created by **weswigham**
 * **weswigham** added to milestone `TypeScript 7.1`
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript-go#4776](https://github.com/microsoft/TypeScript-go/pull/4776) (Closed)

**Remove easily\-removable wasted work in parse/bind**

*Eliminate redundant ASCII scans in parse/bind by leveraging existing line mapping, yielding around 2.5% faster parsing.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4778](https://github.com/microsoft/TypeScript-go/pull/4778) (Closed)

**Fix "Not a subspan" crash in signature help on error\-recovered JSX**

*Improper scanning of a closing tag after an incomplete JSX attribute causes a 'Not a subspan' crash in signature help.*

 * created by **johnfav03**
 * (today) **gabritto** closed the issue

### [Issue microsoft/TypeScript-go#4780](https://github.com/microsoft/TypeScript-go/issues/4780) (Closed, `Needs More Info`)

**textDocument/hover doesn't work on TypeScript 7\.0\.2**

*textDocument/hover requests in TypeScript 7.0.2 LSP produce no responses when used with vim-lsp.*

 * (yesterday) **RyanCavanaugh** added label `Needs More Info`, and set milestone to `Need More Info`
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/4780#issuecomment-5111450281) **KiYugadgeter** said "It looks like the server do not response to hover request"
 * [today](https://github.com/microsoft/TypeScript-go/issues/4780#issuecomment-5121173433) **RyanCavanaugh** said "We would need a concrete LSP command sequence that shows where something is failing (or not responding). Please log a new issue if that information becomes available. Thanks!"
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#4781](https://github.com/microsoft/TypeScript-go/pull/4781) (Closed)

**Optimize \`narrowTypeByEquality\` and \`narrowTypeBySwitchOnDiscriminant\`**

*Improve performance of control flow analysis by optimizing narrowTypeByEquality and narrowTypeBySwitchOnDiscriminant functions.*

 * [today](https://github.com/microsoft/TypeScript-go/pull/4781#issuecomment-5119829958) **ahejlsberg** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4781#issuecomment-5119830782) **typescript-automation[bot]** reported CI build start status with links to build and result details
 * [today](https://github.com/microsoft/TypeScript-go/pull/4781#issuecomment-5120141943) **typescript-automation[bot]** provided the requested performance run results
 * [today](https://github.com/microsoft/TypeScript-go/pull/4781#issuecomment-5120800509) **ahejlsberg** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4781#issuecomment-5120801313) **typescript-automation[bot]** reported CI build jobs started and provided status and result links
 * [today](https://github.com/microsoft/TypeScript-go/pull/4781#issuecomment-5121063379) **typescript-automation[bot]** provided the requested performance run results
 * [today](https://github.com/microsoft/TypeScript-go/pull/4781#issuecomment-5124768102) **ahejlsberg** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4781#issuecomment-5124768620) **typescript-automation[bot]** reported jobs starting and provided a status table with links to build and results
 * [today](https://github.com/microsoft/TypeScript-go/pull/4781#issuecomment-5125362369) **typescript-automation[bot]** provided the performance run results comparing baseline to pr

### [Issue microsoft/TypeScript-go#4782](https://github.com/microsoft/TypeScript-go/issues/4782) (Closed, `Domain: Editor`, **iisaduan**)

**Bug: Rename trigger span is off by one column in module specifiers**

*Rename spans for module specifiers in non-VSCode LSP editors are shifted one column too far left.*

 * created by **lixiaoyan**
 * (today) **RyanCavanaugh** added label `Domain: Editor`, set milestone to `Post-7.0`, and assigned to **iisaduan**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4783](https://github.com/microsoft/TypeScript-go/pull/4783) (Closed)

**Fix module specifier rename trigger spans**

*Remove leading trivia from module-specifier rename trigger spans to correct their offset during prepareRename*

 * created by **lixiaoyan**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4783#issuecomment-5115116377) **lixiaoyan** said "@microsoft-github-policy-service agree"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4785](https://github.com/microsoft/TypeScript-go/pull/4785) (Closed)

**Skip the speculative expression parse in the async arrow lookahead**

*Replace speculative parsing with a token check for unparenthesized async arrows, improving parse speed and reducing memory usage.*

 * [today](https://github.com/microsoft/TypeScript-go/pull/4785#issuecomment-5119019262) **typescript-automation[bot]** published automated CI build status for tests
 * [today](https://github.com/microsoft/TypeScript-go/pull/4785#issuecomment-5119376540) **typescript-automation[bot]** posted the requested performance run results in a detailed comparison report
 * [today](https://github.com/microsoft/TypeScript-go/pull/4785#issuecomment-5119967692) **typescript-automation[bot]** provided test results comparing main and pull request showing everything looked good
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4787](https://github.com/microsoft/TypeScript-go/pull/4787) (Closed)

**Check the arrow\-function line\-terminator rule without the line map**

*Modify arrow-function line-terminator checks to scan preceding trivia rather than building the complete line map, reducing memory overhead.*

 * created by **mds-ant**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4787#issuecomment-5122239992) **DanielRosenwasser** said "@typescript-bot perf test this"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4787#issuecomment-5122240869) **typescript-automation[bot]** announced performance test build start with status and links
 * [today](https://github.com/microsoft/TypeScript-go/pull/4787#issuecomment-5122477073) **typescript-automation[bot]** posted the requested perf run results
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4791](https://github.com/microsoft/TypeScript-go/pull/4791) (Open)

**Add getSymbolOfSourceFile to the API**

*Introduce getSymbolOfSourceFile to directly retrieve a source file’s symbol without loading its AST*

 * created by **dragomirtitian**

### [PR microsoft/TypeScript-go#4792](https://github.com/microsoft/TypeScript-go/pull/4792) (Closed)

**Fix program reuse across resolution mode changes**

*Update program equality checks to include usage mode for correct reuse across resolution mode changes*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4793](https://github.com/microsoft/TypeScript-go/pull/4793) (Closed)

**chore: Fix typo in variable name for diagnostic context setup\.**

*Correct a typo in the variable name used during diagnostic context setup.*

 * created by **connorshea**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4794](https://github.com/microsoft/TypeScript-go/pull/4794) (Closed)

**fix\(parser\): disallow optional chaining on import\.defer**

*Add a parser check and diagnostic TS18062 to disallow optional chaining invocation on import.defer.*

 * created by **BhariGowda**
 * (later) **BhariGowda** closed the issue

### [Issue microsoft/TypeScript-go#4795](https://github.com/microsoft/TypeScript-go/issues/4795) (Open, `Needs More Info`)

**\`tsc \-\-watch\` doesn't recompile on file change**

*TypeScript 7.0.2 stops tsc --build --watch from detecting file changes in a monorepo*

 * created by **haines**

