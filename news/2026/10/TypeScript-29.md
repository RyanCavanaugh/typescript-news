# Report for 2026-10-29 (Thursday, October 29th, 2026)

29 different users commented on 92 different issues.

## Recommended Actions

 * Response Recommended
    * @NullVoxPopuli reported opening a fix for go-to-definition behavior (#65009) in [microsoft/TypeScript#64828](https://github.com/microsoft/TypeScript/issues/64828#issuecomment-6504336488)
    * @nrjdalal provided an additional test case and expected behavior in [microsoft/TypeScript#64978](https://github.com/microsoft/TypeScript/pull/64978#issuecomment-6512865798)
    * @timurzvural agreed to the Contributor License Agreement in [microsoft/TypeScript#65013](https://github.com/microsoft/TypeScript/pull/65013#issuecomment-6506178921)
    * @aetherxeg-source asked about adding a differential regression fixture to compare API paths and suggested specific test scenarios in [microsoft/TypeScript#65051](https://github.com/microsoft/TypeScript/issues/65051#issuecomment-6518847399)
    * @wjnotl indicated the issue was resolved and the issue can be closed in [microsoft/TypeScript#65053](https://github.com/microsoft/TypeScript/issues/65053#issuecomment-6526659382)

## Activity Summary

### [Issue microsoft/TypeScript#3136](https://github.com/microsoft/TypeScript/issues/3136) (Closed, `Suggestion`, `Committed`)

**Feature Request: F\# style Type Provider support?**

*Add F#-style type providers to TypeScript for compile-time generation of type-safe API clients and document bindings.*

 * [5 years ago](https://github.com/microsoft/TypeScript/issues/3136#issuecomment-956060620) **trusktr** suggested closing the issue because ES Module syntax and URL imports via Deno/Node are standard and sufficient
 * [5 years ago](https://github.com/microsoft/TypeScript/issues/3136#issuecomment-956135618) **Dessix** questioned the reason for closing the issue and asked for an example demonstrating generating types for a database target at design time via server-side introspection
 * [5 years ago](https://github.com/microsoft/TypeScript/issues/3136#issuecomment-956635457) **infogulch** clarified the purpose of F#-style Type Providers, noting that they derive new types at design time rather than import existing code
 * (today) **RyanCavanaugh** added label `Committed`, and removed label `Needs Proposal`
 * [today](https://github.com/microsoft/TypeScript/issues/3136#issuecomment-6503025751) **RyanCavanaugh** said "https://devblogs.microsoft.com/typescript/announcing-typescript-7-1-beta/#content-mappers"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63858](https://github.com/microsoft/TypeScript/issues/63858) (Closed, `Infrastructure`, `Needs Investigation`, **jakebailey**)

**Publish an official wasip1 \(WASI\) build artifact of tsgo**

*Publish an official Go WASI (wasip1) WebAssembly build artifact of tsgo alongside native binaries in releases.*

 * [13 weeks ago](https://github.com/microsoft/TypeScript/issues/63858#issuecomment-5351507607) **jakebailey** said "Not sure, I think it will also depend on what we do in the playground."
 * [9 weeks ago](https://github.com/microsoft/TypeScript/issues/63858#issuecomment-5400907269) **trobertson-graymatterllc** described that this approach could enable in-browser compilation, eliminate pre-compilation for development and live design, and support TypeScript as a first-tier language replacement for JavaScript
 * **jakebailey** added label `Infrastructure`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#63862](https://github.com/microsoft/TypeScript/issues/63862) (Closed, `Bug`, **jakebailey**)

**wasip1: LSP over node:wasi hangs after \`initialize\` — signal watcher starves the scheduler \(fix included\)**

*LSP over node:wasi hangs after initialize due to Go signal watcher busy-spin starvation, fixed by skipping signal.NotifyContext on wasip1.*

 * (13 weeks ago) **RyanCavanaugh** added label `Bug`, set milestone to `TypeScript 7.1`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64120](https://github.com/microsoft/TypeScript/pull/64120) (Closed, `For Uncommitted Bug`, **andrewbranch**)

**Add the outputExtension compiler option**

*Add an outputExtension compiler option to specify the external build's file extension for emitted declaration files and specifier rewrites.*

 * (8 weeks ago) **typescript-automation[bot]** added label `For Uncommitted Bug`, and assigned to **andrewbranch**
 * [8 weeks ago](https://github.com/microsoft/TypeScript/pull/64120#issuecomment-5495605864) **NullVoxPopuli-ai-agent** reworked outputExtension as a program-wide compiler option, required noEmit or emitDeclarationOnly, and updated the PR description
 * [today](https://github.com/microsoft/TypeScript/pull/64120#issuecomment-6503087866) **NullVoxPopuli** said "Closing this because #64581 replaced it. #64581 added outputExtensions for content mappers and closed #64053, which is the issue this PR was for."
 * (today) **NullVoxPopuli-ai-agent** closed the issue

### [PR microsoft/TypeScript#64174](https://github.com/microsoft/TypeScript/pull/64174) (Closed, `Author: Team`, `For Milestone Bug`, **jakebailey**)

**Add wasip1 support, enabling CLI, API, browser, sync/async**

*Add experimental wasip1-based WebAssembly build of tsc enabling CLI, LSP, and sync/async API use in Node and browser environments.*

 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64174#issuecomment-6328669720) **jakebailey** announced readiness for review and that they had dropped the “tsc falls back to wasm” idea because Node’s WASI host did not work on Windows
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64174#issuecomment-6483054352) **jakebailey** proposed follow-up work to avoid bundling libs in the binary by adding a new flag for the lib directory and to enable vscode.dev
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64174#issuecomment-6484053015) **jakebailey** said "Hm, concerning test timeout "
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64318](https://github.com/microsoft/TypeScript/pull/64318) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Cherry\-pick tsgo PR 4658 into release\-7\.0**

*Cherry-pick PR 4658 from tsgo into the release-7.0 branch to resolve issue 64262.*

 * (6 weeks ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`
 * **jakebailey** added label `Domain: Performance`
 * (later) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64360](https://github.com/microsoft/TypeScript/pull/64360) (Closed, `For Backlog Bug`)

**Fix union overload signature ordering instability**

*Ensure consistent union overload resolution by ordering synthesized candidates based on each constituent’s signature precedence.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/64360#issuecomment-6154780445) **jakebailey** said "I don't think this PR is right but can't put my finger on why. Figuring out why it feels wrong probably means I have to figure out a fix myself, which defeats the purpose a bit."
 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/64360#issuecomment-6186149807) **adilalperenciftci** removed the exact-arity signature expansion, preserved union-signature matching by using constituents’ reorderCandidates precedence, and reported successful test and build validation
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64360#issuecomment-6289784750) **adilalperenciftci** updated the PR description and asked for another review and approval of pending workflows
 * [today](https://github.com/microsoft/TypeScript/pull/64360#issuecomment-6515804989) **adilalperenciftci** closed the revision, agreed that the current ordering mechanism changed checker precedence too broadly, and refocused on core runtime and identity work with plans to revisit only with a smaller invariant-preserving change
 * (today) **adilalperenciftci** closed the issue

### [Issue microsoft/TypeScript#64424](https://github.com/microsoft/TypeScript/issues/64424) (Open, **johnfav03**)

**\`tsc \-b \-\-watch\` doesn't rebuild when an imported file changes, unless \`incremental\` is on**

*The tsc build watch mode fails to rebuild when imported files change unless incremental or composite compilation is enabled.*

 * created by **Generalsimus**
 * **RyanCavanaugh** assigned to **johnfav03**
 * [today](https://github.com/microsoft/TypeScript/issues/64424#issuecomment-6507331010) **andrewbranch** noted that the issue was previously closed as working as intended and characterized it as a design change rather than a bug

### [Issue microsoft/TypeScript#64463](https://github.com/microsoft/TypeScript/issues/64463) (Closed, `Bug`)

**\[LSP\] Memory of configured projects is never released, even after didClose of all files — ~70 MB retained per project \(7\.0\.2 and 7\.1\.0\-dev\.20260926\.1\)**

*TypeScript LSP never frees memory for closed projects, retaining about 70MB per project and causing memory bloat.*

 * [1 month ago](https://github.com/microsoft/TypeScript/issues/64463#issuecomment-5873826780) **jakebailey** explained that the test verifies longstanding behavior of not closing the project on file close to avoid reloads and asked if the same was tried on TS 6.0
 * (3 weeks ago) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64603](https://github.com/microsoft/TypeScript/pull/64603) (Closed, `Domain: Performance`, `Author: Team`, `For Backlog Bug`, **RyanCavanaugh**)

**Release unused LSP configured projects during idle cleanup**

*Unused LSP-configured projects are released during idle cleanup to free resources.*

 * (3 weeks ago) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`
 * **jakebailey** added label `Domain: Performance`
 * [today](https://github.com/microsoft/TypeScript/pull/64603#issuecomment-6505004895) **jakebailey** reiterated a link and asked whether the behavior was intentional
 * [today](https://github.com/microsoft/TypeScript/pull/64603#issuecomment-6505250440) **andrewbranch** said "That's correct, but we also never had an idle timer triggering cleanup. It seems reasonable to me to discard things on the timer."
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#64605](https://github.com/microsoft/TypeScript/issues/64605) (Open, `Needs Investigation`, **gabritto**)

**TS5115 in published Zod 4\.5–4\.6 types after \#64372**

*Zod 4.5.0–4.6.5 z.json() types cause TS5115 infinite circularity errors in TypeScript 7.1 nightlies after PR #64372, impacting ~62M weekly downloads.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/64605#issuecomment-6084855435) **rsnodgrass** confirmed the issue reproduced with TypeScript 7.1.0-dev and Zod 4.6.5, provided minimal reproduction code and version comparison, and requested review
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/64605#issuecomment-6299246463) **salemkode** confirmed reproduction on typescript@7.1.0-beta with a standalone zod example and provided reproduction steps and error output
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/64605#issuecomment-6426420558) **ebidel** demonstrated that postcss-selector-parser's type definitions still produced TS5115 infinite circular instantiation errors in recent builds and provided reproduction steps and build comparisons
 * [today](https://github.com/microsoft/TypeScript/issues/64605#issuecomment-6504485324) **jakebailey** said "@ebidel Anders posted a change that fixes that package, was it missed?: https://github.com/microsoft/TypeScript/pull/64372#issuecomment-5804602336"
 * [today](https://github.com/microsoft/TypeScript/issues/64605#issuecomment-6505184494) **jakebailey** said "I think the thing we don't get is why someone would update to TS 7.1, but then not also be updating zod or a transitive dep on zod?"

### [PR microsoft/TypeScript#64712](https://github.com/microsoft/TypeScript/pull/64712) (Open, `Author: Team`, `For Backlog Bug`, **jakebailey**)

** Fix compiler option invalidation in incremental builds**

*Audit and fix incorrect incremental build invalidation for compiler options, build-info persistence, global file ordering, and deletions.*

 * (2 weeks ago) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Backlog Bug`, and removed label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/64712#issuecomment-6525329437) **RyanCavanaugh** said "ping @johnfav03"

### [PR microsoft/TypeScript#64789](https://github.com/microsoft/TypeScript/pull/64789) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Share complete union and intersection property cache entries**

*Share complete property cache entries between augmented and non-augmented lookups to reduce duplicate entries, memory usage, and GC scanning overhead.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/64789#issuecomment-6174014470) **typescript-automation[bot]** reported build jobs started and provided status and results links
 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/64789#issuecomment-6174849745) **typescript-automation[bot]** provided the requested performance run results
 * **jakebailey** added label `Domain: Performance`
 * [today](https://github.com/microsoft/TypeScript/pull/64789#issuecomment-6505514916) **jakebailey** said "@typescript-bot perf test"
 * [today](https://github.com/microsoft/TypeScript/pull/64789#issuecomment-6505516776) **typescript-automation[bot]** announced that performance test jobs had started and provided status and results links
 * [today](https://github.com/microsoft/TypeScript/pull/64789#issuecomment-6506647082) **typescript-automation[bot]** provided the requested performance run results
 * (later) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64791](https://github.com/microsoft/TypeScript/pull/64791) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Lint writes to protected record kind fields**

*Introduce a custom lint analyzer that marks record kind fields as protected and rejects unsafe writes or copies.*

 * (2 weeks ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`
 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/64791#issuecomment-6157230696) **jakebailey** described that layout lint is a best-effort guard, noted that checked casts panic on mismatched kinds, fixed shadowed `kind` and copy/variadic `append` cases, and remarked that further Go-level value tracking is out of scope for the PR
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#64828](https://github.com/microsoft/TypeScript/issues/64828) (Open, `Needs Investigation`, **andrewbranch**)

**Content mappers: go\-to\-definition on an module specifier returns nothing when the target file has more than one span\-map segment**

*Go-to-definition on module specifiers no longer finds .gts files containing multiple span-map segments after content mapper updates.*

 * **andrewbranch** added to milestone `TypeScript 7.1.1 RC`
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/64828#issuecomment-6276004130) **NullVoxPopuli-ai-agent** provided a minimal reproduction without Ember or Glint, corrected the trigger to export-from statements, and showed span-mapping outputs across TypeScript versions
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/64828#issuecomment-6328616011) **colinhacks** reported that non-relative import specifiers also broke go to definition under TS 7.1.0-beta and provided repro steps
 * [today](https://github.com/microsoft/TypeScript/issues/64828#issuecomment-6504336488) **NullVoxPopuli** opened a fix adjusting go-to-definition behavior for SourceFile declarations in content-mapped files and added tests for export-from and paths alias imports

### [PR microsoft/TypeScript#64858](https://github.com/microsoft/TypeScript/pull/64858) (Closed, `Author: Team`, `For Uncommitted Bug`, `dependencies`, `github_actions`)

**Bump the github\-actions group across 1 directory with 4 updates**

*Upgrade four GitHub Actions in the repository root—codeql-action init, codeql-action analyze, upload-sarif, and ossf/scorecard-action—to their latest versions.*

 * (1 week ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64871](https://github.com/microsoft/TypeScript/pull/64871) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Speed up short\-lived checker caches**

*Optimize short-lived checker caches by replacing costly Go map clears with generation-counter tables and simpler key hashing for speed improvements.*

 * **jakebailey** added label `Domain: Performance`
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64871#issuecomment-6481785120) **ahejlsberg** said "This one seems to have some nice effects."
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64871#issuecomment-6481824179) **jakebailey** said "Yeah, I'm just maybe a little unnerved by the manual fiddling with the hashes."
 * (later) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64907](https://github.com/microsoft/TypeScript/pull/64907) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Add extra tests for various uncovered parts of the code**

*Add tests for untested code behaviors identified during a recent code review session*

 * (1 week ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (later) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64914](https://github.com/microsoft/TypeScript/pull/64914) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Cherry\-pick PR 64276 to release\-7\.0**

*Apply PR 64276 to the release-7.0 branch to prevent the unstable 7.0 API from logging 'context cancelled' on exit.*

 * (1 week ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (later) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64922](https://github.com/microsoft/TypeScript/pull/64922) (Open, `For Uncommitted Bug`)

**Emit the files of each checker in a deterministic order**

*Ensure each checker emits its files in a consistent, deterministic order to eliminate non-determinism.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/64922#issuecomment-6489410209) **jakebailey** requested the TypeScript bot to run performance tests faster
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64922#issuecomment-6489411417) **typescript-automation[bot]** reported CI job start status for the perf test this faster command
 * [today](https://github.com/microsoft/TypeScript/pull/64922#issuecomment-6490336444) **typescript-automation[bot]** posted perf run results comparing baseline and PR metrics, including errors, symbols, types, memory usage, and allocations
 * [today](https://github.com/microsoft/TypeScript/pull/64922#issuecomment-6506518606) **jakebailey** reported merge failures due to changed baseline files in generateTrace tests
 * [later](https://github.com/microsoft/TypeScript/pull/64922#issuecomment-6520433459) **Andarist** explained adding an emitPrint tracing event and resolving the missing logs so the changes are landable

### [PR microsoft/TypeScript#64928](https://github.com/microsoft/TypeScript/pull/64928) (Closed, `Domain: Performance`, `For Backlog Bug`)

**Reuse token lookup visitor across AST descent**

*Reuse a single NodeVisitor for each token lookup to reduce allocations and improve getTokenAtPosition performance.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/64928#issuecomment-6489938948) **DanielRosenwasser** said "@typescript-bot perf test this"
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64928#issuecomment-6489940768) **typescript-automation[bot]** reported that the performance test build started and provided links to status and results
 * [today](https://github.com/microsoft/TypeScript/pull/64928#issuecomment-6490794458) **typescript-automation[bot]** provided the results of the requested performance run
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#64929](https://github.com/microsoft/TypeScript/issues/64929) (Closed, `Possible Improvement`)

**Native token lookup allocates a visitor on each AST descent step**

*astnav.getTokenAtPosition repeatedly allocates new NodeVisitor instances during AST descent, causing high allocations and performance overhead mitigated by reusing the visitor*

 * created by **Tom4ikss**
 * (3 days ago) **RyanCavanaugh** added label `Possible Improvement`, and set milestone to `Backlog`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64973](https://github.com/microsoft/TypeScript/pull/64973) (Open, `Author: Team`, `For Uncommitted Bug`, **johnfav03**)

**Fix non\-root dependency tracking in build watch mode**

*Enable build watch mode to detect changes in non-root imported files even when incremental builds are disabled.*

 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/64973#issuecomment-6429603044) **jakebailey** described a Go test case demonstrating stale output due to coalesced directory delete/recreate events and noted a fix by removing an early return
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64973#issuecomment-6480991125) **jakebailey** said "I'm sort of having a hard time trying to review this; is this potentially possible to rebase into a few commits? Or is it definitely that all is required and one single fix?"
 * [today](https://github.com/microsoft/TypeScript/pull/64973#issuecomment-6504825286) **jakebailey** said "Maybe @andrewbranch can internalize this better than i can though"
 * [today](https://github.com/microsoft/TypeScript/pull/64973#issuecomment-6505557681) **johnfav03** said "@jakebailey I split it up into 3 commits, let me know if this is easier to review or if there's something else I can do"
 * [today](https://github.com/microsoft/TypeScript/pull/64973#issuecomment-6507442036) **andrewbranch** mentioned that the previous behavior was intentional in Strada and argued that reconsideration would require extensive analysis and planning as a feature rather than a bug fix

### [PR microsoft/TypeScript#64978](https://github.com/microsoft/TypeScript/pull/64978) (Open, `For Backlog Bug`)

**fix\(64974\): fix contextual typing for destructured parameter defaults**

*Correct contextual type inference for destructured parameters with default values.*

 * created by **a-tarasyuk**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64978#issuecomment-6506497425) **timurzvural** opened an alternative PR (#65016) covering #65011 with contextual-type guards for object and array padding and added JSDoc returns, casts, and annotated .ts cases from #65011 atop #64974 scenarios
 * [today](https://github.com/microsoft/TypeScript/pull/64978#issuecomment-6512865798) **nrjdalal** provided an additional repro case with code and described how binding elements with defaults behaved across TypeScript versions
 * [today](https://github.com/microsoft/TypeScript/pull/64978#issuecomment-6513976139) **timurzvural** explained the regression behavior on TS 7.1 for object literals with defaults and proposed PR #65016 as an alternative solution

### [PR microsoft/TypeScript#64992](https://github.com/microsoft/TypeScript/pull/64992) (Open, `Domain: Performance`, `For Uncommitted Bug`)

**Speedup keywords lookup with a perfect hash table in GetIdentifierToken**

*Replace the general-purpose Go map with a dedicated perfect hash table for static keyword lookup, boosting parsing speed by about 3%.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/64992#issuecomment-6470852722) **typescript-automation[bot]** reported start of performance tests with status and results links
 * **jakebailey** added label `Domain: Performance`
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64992#issuecomment-6471936203) **typescript-automation[bot]** reported the requested performance run results
 * [today](https://github.com/microsoft/TypeScript/pull/64992#issuecomment-6510307354) **jakebailey** suggested refactoring IdentifierToKeywordKind to use a keyword lookup helper and adding a panic for out-of-range keywords
 * [later](https://github.com/microsoft/TypeScript/pull/64992#issuecomment-6526062147) **jakebailey** said "@typescript-bot perf test this faster"
 * [later](https://github.com/microsoft/TypeScript/pull/64992#issuecomment-6526064873) **typescript-automation[bot]** said "Hey @jakebailey, this PR was updated less than two minutes before this command. Please wait until it has been unchanged for two minutes and try again."
 * [later](https://github.com/microsoft/TypeScript/pull/64992#issuecomment-6526797614) **jakebailey** said "@typescript-bot perf test this faster"
 * [later](https://github.com/microsoft/TypeScript/pull/64992#issuecomment-6526800123) **typescript-automation[bot]** reported that the perf test this faster job started with links to the build and results

### [PR microsoft/TypeScript#64996](https://github.com/microsoft/TypeScript/pull/64996) (Open, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Inline storage for small symbol tables**

*Adding inline storage for four entries in small symbol tables reduces allocations by 33% and improves binding performance by 10%.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/64996#issuecomment-6482409075) **ahejlsberg** stated that most symbol tables escape to the heap because they’re attached to AST nodes or symbols and suggested placing them there initially
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64996#issuecomment-6482423627) **jakebailey** said "Yeah, I just tried, and it doesn't seem to help (or makes things worse), because the compiler just isn't smart enough."
 * [today](https://github.com/microsoft/TypeScript/pull/64996#issuecomment-6490412806) **DanielRosenwasser** clarified using the stack as temporary storage and allocating precise size afterwards
 * [later](https://github.com/microsoft/TypeScript/pull/64996#issuecomment-6525157790) **ahejlsberg** said "@RyanCavanaugh Not really sure why we'd take this. It generally increases memory by 0.5% and has no positive effect on performance."

### [PR microsoft/TypeScript#65002](https://github.com/microsoft/TypeScript/pull/65002) (Open, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Formatter perf improvements**

*Enhances the TypeScript formatting scanner with reduced allocations and SIMD optimizations, achieving about 30% speedup.*

 * (yesterday) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#65004](https://github.com/microsoft/TypeScript/pull/65004) (Open, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Allow builds to skip source generation**

*Add a build flag to skip source generation and shorten the benchmark preparation phase.*

 * (yesterday) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * **jakebailey** added label `Domain: Performance`

### [Issue microsoft/TypeScript#65007](https://github.com/microsoft/TypeScript/issues/65007) (Closed)

**es2026 lib makes \`JSON\.parse\` \`reviver\` parameter required for \`Parameters\`, \`\.call\` and \`\.apply\`**

*ES2026 JSON.lib makes JSON.parse’s reviver required instead of optional, causing type inference and strictBindCallApply errors.*

 * created by **Phil2812**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#65008](https://github.com/microsoft/TypeScript/issues/65008) (Open)

**lib\.dom\.d\.ts: Transformer is missing the \`cancel\` member that WHATWG Streams defines**

*The Transformer interface in lib.dom.d.ts lacks the WHATWG Streams-defined cancel method, causing valid TransformStream implementations to fail compilation.*

 * created by **HouMinXi**
 * [today](https://github.com/microsoft/TypeScript/issues/65008#issuecomment-6504429596) **HouMinXi** investigated the absence of Transformer.cancel in lib.dom.d.ts, explained it was removed due to lack of browser implementation per generator rules, and suggested a local declaration workaround
 * [today](https://github.com/microsoft/TypeScript/issues/65008#issuecomment-6507251988) **timurzvural** opened a fix pull request adding Transformer.cancel / TransformerCancelCallback to lib.dom.d.ts and lib.webworker.d.ts with a compiler regression test

### [PR microsoft/TypeScript#65009](https://github.com/microsoft/TypeScript/pull/65009) (Open, `For Milestone Bug`, **andrewbranch**)

**Go to a content\-mapped file from its module specifier**

*Go-to-definition on module specifiers for content-mapped files now returns a zero-length location at the file start instead of nothing.*

 * created by **NullVoxPopuli**
 * (today) **typescript-automation[bot]** added label `For Milestone Bug`, and assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript/pull/65009#issuecomment-6504340709) **NullVoxPopuli** said "@microsoft-github-policy-service agree"

### [PR microsoft/TypeScript#65010](https://github.com/microsoft/TypeScript/pull/65010) (Open, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Negated Types: Constrain Promise\<T\> to forbid Thenable T**

*Add a constraint to Promise<T> to exclude thenable types and prevent primitive intersections causing invalid Promise instantiations.*

 * created by **weswigham**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **weswigham**
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6504482555) **weswigham** requested the TypeScript bot to run tests
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6504485003) **typescript-automation[bot]** posted automated build status updates listing commands, statuses, and result links
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6505315116) **typescript-automation[bot]** reported an error when publishing results from the DT run and provided a link to the log
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6505423690) **typescript-automation[bot]** reported new TypeScript errors in axios tests when comparing baseline and PR
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6505424642) **typescript-automation[bot]** reported TS2344 errors from running the user tests suite on puppeteer and test tsconfig.json files
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6505425873) **typescript-automation[bot]** reported additional type errors from running the user tests suite on the type-fest project
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6505426974) **typescript-automation[bot]** provided additional TS2344 errors from running the user tests suite on webpack’s tsconfig.json and related files
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6505428164) **typescript-automation[bot]** reported new TS2344 type constraint errors in xterm.js tsconfig-library-base.json from user tests
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6505620712) **typescript-automation[bot]** provided requested performance run results including a comparison report
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506847972) **typescript-automation[bot]** reported build comparison results for top 400 repos between baseline and pr and asked for review
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506848898) **typescript-automation[bot]** described additional changes from the top 400 repos suite and reported build failures and TypeScript errors in alibaba/page-agent
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506849877) **typescript-automation[bot]** reported build failures in ant-design/ant-design when running the top 400 repos suite with the old tsc, listing TS2344 errors in multiple files
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506850853) **typescript-automation[bot]** reported build failures in anthropics/claude-quickstarts due to TS2344 errors for 'Response' and 'void' types
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506851894) **typescript-automation[bot]** reported TS2344 constraint errors for Response, Request, and void in apify/crawlee when running the top 400 repos suite
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506852906) **typescript-automation[bot]** reported findings from running the top 400 repos suite and listed build errors in basarat/typescript-book and bendlang/bend
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506853991) **typescript-automation[bot]** reported TypeScript build failures for browserbase/stagehand with multiple TS2344 errors in sdk-ts/src/browser/index.ts
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506855002) **typescript-automation[bot]** reported build failures and TS2344 constraint errors in Budibase from the top 400 repos suite
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506855989) **typescript-automation[bot]** reported build failures in the cheaper-inference/OmniRoute project after running the top 400 repos suite, listing TS2344 errors across several files
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506857023) **typescript-automation[bot]** reported build failures in the cheeriojs/cheerio project, highlighting TS2344 and TS2322 errors in benchmark, scripts, and source files
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506857918) **typescript-automation[bot]** reported build failures and TS2344 errors in DayuanJiang/next-ai-draw-io from running the top 400 repos suite
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506858922) **typescript-automation[bot]** reported additional TypeScript errors from running the top 400 repos suite against directus/directus
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506859953) **typescript-automation[bot]** reported multiple TS2344 type constraint errors in DIYgod/RSSHub after running the top 400 repos suite
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506860950) **typescript-automation[bot]** reported build failures in Dokploy/dokploy due to TS2344 type constraint errors in server package files
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506861998) **typescript-automation[bot]** posted automated analysis results showing TypeScript build errors in dream-num/univer from the top 400 repos suite
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506862992) **typescript-automation[bot]** reported additional TypeScript errors for dzhng/deep-research from the top 400 repos suite
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506863982) **typescript-automation[bot]** reported build failures due to type errors in earendil-works/pi's tui package
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506864964) **typescript-automation[bot]** listed TS2344 constraint errors in the Egonex-AI/Understand-Anything plugin build
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506865929) **typescript-automation[bot]** reported build failures in the open-seo project due to TS2344 errors
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506866900) **typescript-automation[bot]** reported type errors in EveryInc/compound-engineering-plugin from the top 400 repos suite
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506867872) **typescript-automation[bot]** reported TypeScript build errors for fabricjs/fabric.js from the top 400 repos suite
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506868803) **typescript-automation[bot]** reported additional TypeScript TS2344 constraint errors from feder-cr/invisible_dots
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506869762) **typescript-automation[bot]** reported build errors in the firecrawl repository from running the top 400 repos suite
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506870740) **typescript-automation[bot]** reported type constraint errors in getpaseo/paseo’s relay package when running the top 400 repos suite
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506871728) **typescript-automation[bot]** reported more compilation errors for getredash/redash from running the top 400 repos suite
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506872688) **typescript-automation[bot]** reported build failures and TS2344 errors in grafana/grafana from the top 400 repos suite
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506873646) **typescript-automation[bot]** reported build failures in graphql/graphql-js from the top 400 repos suite run
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506874572) **typescript-automation[bot]** reported TS2344 'void' constraint errors across multiple lines in homebridge/homebridge api.ts and bridgeService.ts
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506875573) **typescript-automation[bot]** reported TypeScript build failures in hoppscotch from the top 400 repos suite run
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506876559) **typescript-automation[bot]** reported build failures in Infisical/infisical with the old tsc, listing TS2344, TS2677, and TS2322 errors
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506877644) **typescript-automation[bot]** reported additional build failures for karakeep-app/karakeep from running the top 400 repos suite
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506878666) **typescript-automation[bot]** reported build failures and TypeScript errors in koala73/worldmonitor when running the top 400 repos suite
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506879692) **typescript-automation[bot]** reported build errors in the kortix-ai/suna project from running the top 400 repos suite
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506880742) **typescript-automation[bot]** reported build failures in langfuse/langfuse when running the top 400 repos suite with the new tsc
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506881846) **typescript-automation[bot]** provided build failure details from running the top 400 repos suite on linshenkx/prompt-optimizer
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506882956) **typescript-automation[bot]** reported type constraint errors from running the top 400 repos suite across multiple repositories
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506884020) **typescript-automation[bot]** reported type errors in marktext/marktext when running the top 400 repos suite
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506885191) **typescript-automation[bot]** reported build failures and type errors for meta/docusaurus plugin-rsdoctor from the top 400 repos suite
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506886273) **typescript-automation[bot]** reported TypeScript constraint errors in microsoft/vscode from the top 400 repos suite run
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506887394) **typescript-automation[bot]** reported type constraint errors from running the top 400 repos suite on mihomo-party-org/clash-party
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506888428) **typescript-automation[bot]** listed TypeScript TS2344 errors from mksglu/context-mode when running the top 400 repos suite
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506889558) **typescript-automation[bot]** reported additional compilation errors for modelcontextprotocol/servers in the top 400 repos suite
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506890643) **typescript-automation[bot]** reported TS build failures for moeru-ai/airi from the top 400 repos suite
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506891734) **typescript-automation[bot]** reported TypeScript build errors for the monkeytypegame/monkeytype project's util package and tests
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506892793) **typescript-automation[bot]** provided detailed build failure information for nanocoai/nanoclaw
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506893876) **typescript-automation[bot]** reported TypeScript constraint errors in nashsu/llm_wiki's mcp-server project from the top 400 repos suite
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506894953) **typescript-automation[bot]** reported additional TS2345 type errors from running the top 400 repos suite on neoclide/coc.nvim
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506896059) **typescript-automation[bot]** reported additional build errors from the top 400 repos suite for nestjs/nest samples
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506897137) **typescript-automation[bot]** reported more interesting changes from running the top 400 repos suite, including TS2344 errors in nexu-io/open-design
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506898171) **typescript-automation[bot]** reported type constraint errors in nilbuild/developer-roadmap from the top 400 repos suite
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506899262) **typescript-automation[bot]** reported TS2344 errors in outline/outline from top 400 repos suite run
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506900329) **typescript-automation[bot]** reported build failures in palantir/blueprint with the old tsc and detailed TS2344 errors in test-commons/vitest-utils.ts
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506901441) **typescript-automation[bot]** reported additional build failures in paperclipai/paperclip from the top 400 repos suite, noting TS2344 errors in multiple locations of startup-timing.ts and execution-phase.ts
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506902498) **typescript-automation[bot]** reported TypeScript errors from running the top 400 repos suite on pear-devs/pear-desktop, detailing TS2344 errors and locations
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506903527) **typescript-automation[bot]** reported additional TS2344 type constraint errors in pingdotgg/t3code from the top 400 repos suite run
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506904568) **typescript-automation[bot]** reported build failures and TS2344 errors for pixijs/pixijs from the top 400 repos suite
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506905641) **typescript-automation[bot]** reported TypeScript TS2344 errors in promptfoo/promptfoo after running the top 400 repos suite
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506906660) **typescript-automation[bot]** reported build failures in pubkey/rxdb with old tsc showing TS2344 errors in multiple files
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506907674) **typescript-automation[bot]** reported build failures in puppeteer/puppeteer when running top 400 repos suite
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506908794) **typescript-automation[bot]** described build failures and TypeScript TS2344 errors for QwenLM/qwen-code from the top 400 repos suite
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506909803) **typescript-automation[bot]** reported type errors in radix-ui/primitives e2e helpers from the top 400 repos suite run
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506910904) **typescript-automation[bot]** reported more interesting changes from running the top 400 repos suite and listed build failures for react-navigation/react-navigation
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506911960) **typescript-automation[bot]** reported TypeScript TS2344 constraint errors from running the top 400 repos suite against reactive-resume
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506912984) **typescript-automation[bot]** provided build failure details from the top 400 repos suite for readest/readest
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506913994) **typescript-automation[bot]** reported TypeScript constraint errors for refined-github repository from the top 400 repos suite run
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506915044) **typescript-automation[bot]** reported build failures and TypeScript errors for remix-run/react-router from running the top 400 repos suite
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506916151) **typescript-automation[bot]** reported build failures in responsively-org/responsively-app due to TS2344 constraint errors
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506917217) **typescript-automation[bot]** reported that two of twenty-one projects failed to build with type constraint errors in RSSNext/Folo when running the top 400 repos suite
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506918345) **typescript-automation[bot]** reported additional TypeScript errors from running top 400 repos suite on SBoudrias/Inquirer.js
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506919326) **typescript-automation[bot]** reported build failures and TypeScript errors in sequelize/sequelize from running the top 400 repos suite
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506920400) **typescript-automation[bot]** reported build failures and TypeScript constraint errors in the stablyai/orca project from the top 400 repos suite run
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506921462) **typescript-automation[bot]** provided automated build error details from the top 400 repos suite for Stirling-Tools/Stirling-PDF
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506922552) **typescript-automation[bot]** reported build failures and TS2344 errors in the supabase/supabase project from the top 400 repos suite
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506923633) **typescript-automation[bot]** reported build failures from running the top 400 repos suite on super-productivity, detailing TS2344 constraint errors in packages/plugin-api
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506924663) **typescript-automation[bot]** listed TS2344 build errors in TanStack/query from running the top 400 repos suite
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506925670) **typescript-automation[bot]** provided TypeScript compilation error details from running the top 400 repos suite on the Bilibili-Evolved project
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506926630) **typescript-automation[bot]** reported additional interesting changes from running the top 400 repos suite and listed build errors for thedotmack/claude-mem
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506927619) **typescript-automation[bot]** reported build errors for THU-MAIC/OpenMAIC from the top 400 repos suite
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506928587) **typescript-automation[bot]** reported more build failures for tldraw/tldraw with the old tsc, listing TS2344, TS2322, and TS2345 errors in internal scripts and apps modules
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506929587) **typescript-automation[bot]** reported more changes from running the top 400 repos suite, showing TS2344 type errors in tobi/qmd’s tsconfig.build.json
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506930608) **typescript-automation[bot]** reported compile errors from running the top 400 repos suite, detailing TS2344 errors in toon-format/toon
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506931521) **typescript-automation[bot]** reported TS2344 errors in TryGhost/Ghost's adapters/route-settings-base package when running the top 400 repos suite
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506932490) **typescript-automation[bot]** reported build failures and TypeScript errors in upstash/context7
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506933473) **typescript-automation[bot]** reported compilation errors in vercel/ai and the zai package when running the top 400 repos suite with the new tsc
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506934472) **typescript-automation[bot]** reported TypeScript errors from running the top 400 repos suite, detailing constraint violations in vercel/chatbot’s tsconfig.json and various source files
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506935501) **typescript-automation[bot]** reported TypeScript constraint errors from top 400 repos suite for the oh-my-claudecode repository
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506936436) **typescript-automation[bot]** reported TypeScript errors for Yeachan-Heo/oh-my-codex from running the top 400 repos suite

### [Issue microsoft/TypeScript#65011](https://github.com/microsoft/TypeScript/issues/65011) (Closed)

**Regression in 7\.1: contextual parameter type is lost for a destructuring pattern with a default \(TS7031\)**

*TypeScript 7.1 regression loses contextual typing for defaulted destructured parameters in checkJs, resulting in TS7031 errors.*

 * created by **mkpoli**
 * [today](https://github.com/microsoft/TypeScript/issues/65011#issuecomment-6506496999) **timurzvural** opened an alternative fix in PR 65016 that skipped object/tuple padding in checkDeclarationInitializer when the parameter already had a contextual type, guarded array binding patterns, and added compiler tests for JSDoc @returns, cast, and .ts shapes
 * [today](https://github.com/microsoft/TypeScript/issues/65011#issuecomment-6506731902) **MartinJohns** said "Duplicate of #64974."
 * (today) **mkpoli** closed the issue

### [PR microsoft/TypeScript#65012](https://github.com/microsoft/TypeScript/pull/65012) (Closed, `For Uncommitted Bug`)

**fix: keep JSON\.parse reviver optional in es2026**

*Preserve the optional reviver parameter for JSON.parse in ES2026 type definitions.*

 * created by **a-tarasyuk**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#65013](https://github.com/microsoft/TypeScript/pull/65013) (Closed, `For Backlog Bug`, **RyanCavanaugh**)

**Fix escaped keyword ASI \(\#64883\) and new\-expression emit parens \(\#64981\)**

*Fixes parsing of Unicode-escaped in and instanceof after class field initializers and preserves parentheses in emitted new-expressions.*

 * created by **timurzvural**
 * (today) **typescript-automation[bot]** added label `For Backlog Bug`, and assigned to **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript/pull/65013#issuecomment-6506168187) **jakebailey** said "Why are there two fixes in one PR"
 * [today](https://github.com/microsoft/TypeScript/pull/65013#issuecomment-6506178921) **timurzvural** agreed to the Contributor License Agreement by replying with the required command
 * [today](https://github.com/microsoft/TypeScript/pull/65013#issuecomment-6506239448) **timurzvural** closed the combined PR in favor of two single-issue PRs and requested review of them
 * [today](https://github.com/microsoft/TypeScript/pull/65013#issuecomment-6506239790) **timurzvural** said "Replaced by focused PRs #65014 (#64883) and #65015 (#64981)."
 * (today) **timurzvural** closed the issue

### [PR microsoft/TypeScript#65014](https://github.com/microsoft/TypeScript/pull/65014) (Open, `For Backlog Bug`)

**Fix escaped keyword ASI after class field initializers \(\#64883\)**

*Treat Unicode-escaped in and instanceof as identifiers instead of operators after class field initializers to allow ASI.*

 * created by **timurzvural**
 * **typescript-automation[bot]** added label `For Backlog Bug`

### [PR microsoft/TypeScript#65015](https://github.com/microsoft/TypeScript/pull/65015) (Closed, `For Uncommitted Bug`, **RyanCavanaugh**)

**Fix new\-expression emit parentheses after type erasure \(\#64981\)**

*Ensure the TypeScript emitter parenthesizes new-expressions with type assertions to prevent incorrect runtime emits.*

 * created by **timurzvural**
 * (today) **typescript-automation[bot]** added label `For Uncommitted Bug`, and assigned to **RyanCavanaugh**

### [PR microsoft/TypeScript#65016](https://github.com/microsoft/TypeScript/pull/65016) (Open, `For Uncommitted Bug`)

**fix\(65011\): preserve contextual types for destructured parameter defaults**

*TS 7.1 destructured defaults lose contextual types and trigger TS7031 errors, so padding now occurs only without contextual type.*

 * created by **timurzvural**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [PR microsoft/TypeScript#65017](https://github.com/microsoft/TypeScript/pull/65017) (Open, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Skip non\-scope ancestors quickly in NameResolver\.Resolve**

*Refactor NameResolver.Resolve to classify node kinds and skip non-scope ancestors for faster scope resolution.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/65017#issuecomment-6506904017) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/65017#issuecomment-6506905853) **typescript-automation[bot]** started CI jobs and updated the comment with a status table and links
 * **jakebailey** added label `Domain: Performance`
 * [today](https://github.com/microsoft/TypeScript/pull/65017#issuecomment-6507971544) **typescript-automation[bot]** posted the results of the requested performance run including comparison metrics

### [Issue microsoft/TypeScript#65018](https://github.com/microsoft/TypeScript/issues/65018) (Closed)

**importHelpers: true reports TS2354 for private fields that emit no helper**

*Enabling importHelpers in TypeScript erroneously requires tslib for private class fields despite no helper usage.*

 * created by **JounQin**
 * [today](https://github.com/microsoft/TypeScript/issues/65018#issuecomment-6506986533) **JounQin** closed the issue as a duplicate of #63728, corrected the TypeScript version to 7.0.2, and explained the build failure with importHelpers on native private fields
 * (today) **JounQin** closed the issue

### [PR microsoft/TypeScript#65019](https://github.com/microsoft/TypeScript/pull/65019) (Open, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Split link store lookups into inlineable fast paths**

*Move entry creation logic to getSlow methods so LinkStore.Get and PagedLinkStore.Get fast-path lookups can be inlined.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/65019#issuecomment-6507008447) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/65019#issuecomment-6507010241) **typescript-automation[bot]** reported that performance test jobs had started and provided status and results links
 * **jakebailey** added label `Domain: Performance`
 * [today](https://github.com/microsoft/TypeScript/pull/65019#issuecomment-6508179552) **typescript-automation[bot]** posted performance run results for the requested perf run

### [Issue microsoft/TypeScript#65020](https://github.com/microsoft/TypeScript/issues/65020) (Open)

**JSDoc: a nested @property with a type that does not parse drops every nested @property after it**

*A nested JSDoc @property with an unsupported function signature fails to parse and drops subsequent properties.*

 * created by **NullVoxPopuli**
 * [today](https://github.com/microsoft/TypeScript/issues/65020#issuecomment-6507846950) **timurzvural** opened a pull request recovering through leftover parentheses after an unparseable braced Closure-style type, preserving property name parsing, and added regression and parser tests

### [PR microsoft/TypeScript#65021](https://github.com/microsoft/TypeScript/pull/65021) (Open, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Probe links without creating them on read\-only paths**

*On read-only checker paths, switch from calling Get to TryGet and handle nil receivers to prevent creating unused link records.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/65021#issuecomment-6507057477) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/65021#issuecomment-6507059446) **typescript-automation[bot]** provided build status update with job commands and results links
 * **jakebailey** added label `Domain: Performance`
 * [today](https://github.com/microsoft/TypeScript/pull/65021#issuecomment-6508463556) **typescript-automation[bot]** provided the requested performance run results comparing baseline and PR metrics for tsc

### [PR microsoft/TypeScript#65022](https://github.com/microsoft/TypeScript/pull/65022) (Open, `For Uncommitted Bug`)

**Keep nested JSDoc properties after a property with a missing name**

*Preserve nested JSDoc @property tags after an unparsable property type to avoid losing subsequent properties.*

 * created by **NullVoxPopuli**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [PR microsoft/TypeScript#65023](https://github.com/microsoft/TypeScript/pull/65023) (Closed)

**fix\(65008\): add Transformer\.cancel to DOM and webworker libs**

*Add an optional cancel method to the Transformer interface in DOM and WebWorker library definitions to align with the WHATWG Streams spec and prevent TS2353 errors.*

 * created by **timurzvural**
 * [today](https://github.com/microsoft/TypeScript/pull/65023#issuecomment-6507252124) **typescript-automation[bot]** noted that the pull request updates generated declaration files, requested the change in the generator repository, and stated the pull request would be closed
 * (today) **typescript-automation[bot]** closed the issue

### [PR microsoft/TypeScript#65024](https://github.com/microsoft/TypeScript/pull/65024) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Add lint rule requiring SAFETY comments on unsafe operations**

*Add a lint rule requiring explicit SAFETY comments to document invariants for unsafe operations.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#65025](https://github.com/microsoft/TypeScript/pull/65025) (Open, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Pre\-size member, export, and locals symbol tables**

*Pre-size member, export, and local symbol tables based on declaration counts to avoid repetitive resizing and improve allocation efficiency*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/65025#issuecomment-6507376710) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/65025#issuecomment-6507378639) **typescript-automation[bot]** reported that the performance test build started and provided links to status and results
 * **jakebailey** added label `Domain: Performance`
 * [today](https://github.com/microsoft/TypeScript/pull/65025#issuecomment-6508738862) **typescript-automation[bot]** shared the results of the requested performance run
 * [today](https://github.com/microsoft/TypeScript/pull/65025#issuecomment-6508803056) **Copilot** noted failure of custom setup steps in the Copilot code review run

### [PR microsoft/TypeScript#65026](https://github.com/microsoft/TypeScript/pull/65026) (Open, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Create decl emit accessibility diagnostic closures lazily**

*Optimize declaration emit performance by lazily creating accessibility diagnostic closures only when needed and storing context in a lightweight struct.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/65026#issuecomment-6507379528) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/65026#issuecomment-6507381323) **typescript-automation[bot]** announced that performance tests had started and provided links to build status and results
 * **jakebailey** added label `Domain: Performance`
 * [today](https://github.com/microsoft/TypeScript/pull/65026#issuecomment-6508622525) **typescript-automation[bot]** reported the results of the requested performance run

### [PR microsoft/TypeScript#65027](https://github.com/microsoft/TypeScript/pull/65027) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Report overflow when ReadDirectoryChangesW returns zero bytes**

*ReadDirectoryChangesW returns zero bytes and drops all events on buffer overflow rather than signaling ErrOverflow.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#65028](https://github.com/microsoft/TypeScript/pull/65028) (Open, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Reuse scratch node lists in the parser**

*Reuse parser scratch buffers for nested list parsing to minimize heap allocations and memory garbage.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/65028#issuecomment-6507596054) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/65028#issuecomment-6507597977) **typescript-automation[bot]** notified that performance tests started and linked to build status and results
 * **jakebailey** added label `Domain: Performance`
 * [today](https://github.com/microsoft/TypeScript/pull/65028#issuecomment-6508835852) **typescript-automation[bot]** provided the performance run results requested by the user
 * [today](https://github.com/microsoft/TypeScript/pull/65028#issuecomment-6508863691) **jakebailey** said "Hm, no great effect."

### [PR microsoft/TypeScript#65029](https://github.com/microsoft/TypeScript/pull/65029) (Closed, `For Uncommitted Bug`)

**fix\(65020\): recover nested JSDoc @property after unparseable type**

*Improve JSDoc parser to recover nested @property tags after encountering unparseable types so subsequent properties are not dropped.*

 * created by **timurzvural**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/65029#issuecomment-6507858755) **timurzvural** said "Closing: #65020 is already closed, so this PR is being withdrawn."
 * (today) **timurzvural** closed the issue

### [PR microsoft/TypeScript#65030](https://github.com/microsoft/TypeScript/pull/65030) (Open, `For Uncommitted Bug`, **ahejlsberg**)

**Preserve reliability flags for cached relations during variance measurement**

*Include reliability flags in cached relation fast-path results during variance measurement to maintain correct variance assignments*

 * created by **1-DARK**
 * (today) **typescript-automation[bot]** added label `For Uncommitted Bug`, and assigned to **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript/pull/65030#issuecomment-6508601042) **ahejlsberg** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/65030#issuecomment-6508602945) **typescript-automation[bot]** reported build statuses for four CI commands with links to started jobs and results
 * [today](https://github.com/microsoft/TypeScript/pull/65030#issuecomment-6509284615) **typescript-automation[bot]** notified that DT test results were ready and unchanged
 * [today](https://github.com/microsoft/TypeScript/pull/65030#issuecomment-6509414012) **typescript-automation[bot]** provided tsc user test results and indicated everything looked good
 * [today](https://github.com/microsoft/TypeScript/pull/65030#issuecomment-6509830896) **typescript-automation[bot]** reported the requested performance run results
 * [today](https://github.com/microsoft/TypeScript/pull/65030#issuecomment-6510759318) **typescript-automation[bot]** reported successful tsc comparison between baseline and pr on the top 400 repos

### [PR microsoft/TypeScript#65031](https://github.com/microsoft/TypeScript/pull/65031) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Size new arena chunks from the previous chunk's capacity**

*Modify Arena.NewSlice to use previous chunk capacity instead of length for doubling new chunk sizes.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/65031#issuecomment-6508007122) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/65031#issuecomment-6508008771) **typescript-automation[bot]** started CI jobs and posted build status and results links
 * [today](https://github.com/microsoft/TypeScript/pull/65031#issuecomment-6508013357) **jakebailey** said "This one's definitely an oops on my part"
 * [today](https://github.com/microsoft/TypeScript/pull/65031#issuecomment-6508105253) **Copilot** reported failing custom setup steps during the Copilot code review run
 * **jakebailey** added label `Domain: Performance`
 * [today](https://github.com/microsoft/TypeScript/pull/65031#issuecomment-6509016118) **typescript-automation[bot]** provided the performance run results and comparison report for baseline vs pr
 * (later) **jakebailey** closed the issue

### [PR microsoft/TypeScript#65032](https://github.com/microsoft/TypeScript/pull/65032) (Open, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Speed up keyword lookup, identifier scanning, and whitespace skipping in the scanner**

*Optimize the scanner’s performance by improving keyword lookup, identifier scanning, and whitespace skipping.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * **jakebailey** added label `Domain: Performance`
 * [today](https://github.com/microsoft/TypeScript/pull/65032#issuecomment-6508851917) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/65032#issuecomment-6508853497) **typescript-automation[bot]** announced that performance test jobs started and provided links to build status and results
 * [today](https://github.com/microsoft/TypeScript/pull/65032#issuecomment-6510095162) **typescript-automation[bot]** provided the requested performance run results including detailed metrics for errors, symbols, types, and memory usage

### [PR microsoft/TypeScript#65033](https://github.com/microsoft/TypeScript/pull/65033) (Open, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Speed up union construction with sorted\-run merging and cheaper membership check**

*Introduce sorted-run merging and cheaper membership checks to improve union construction performance.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * **jakebailey** added label `Domain: Performance`
 * [today](https://github.com/microsoft/TypeScript/pull/65033#issuecomment-6508404590) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/65033#issuecomment-6508406394) **typescript-automation[bot]** posted CI status update with build start and results links
 * [today](https://github.com/microsoft/TypeScript/pull/65033#issuecomment-6509471610) **typescript-automation[bot]** provided perf run results in a comparison report
 * [later](https://github.com/microsoft/TypeScript/pull/65033#issuecomment-6524379365) **RyanCavanaugh** said "Not sure if this one is worth it if it's only 1% on compiler-unions"

### [PR microsoft/TypeScript#65034](https://github.com/microsoft/TypeScript/pull/65034) (Open, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Negated Types: Make conditional type produce substitutions with negated constraints in \(some\) false branches **

*Enable conditional types to substitute negated primitive constraints in false branches when type parameters exactly partition.*

 * created by **weswigham**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **weswigham**
 * [today](https://github.com/microsoft/TypeScript/pull/65034#issuecomment-6508118401) **weswigham** said "@typescript-bot test this"
 * [today](https://github.com/microsoft/TypeScript/pull/65034#issuecomment-6508120467) **typescript-automation[bot]** provided build status updates for test top400, user test this, run dt, and perf test this faster
 * [today](https://github.com/microsoft/TypeScript/pull/65034#issuecomment-6508831682) **typescript-automation[bot]** reported DT test results showing a TS1110 type expected compile error in the regex-not package and linked full logs
 * [today](https://github.com/microsoft/TypeScript/pull/65034#issuecomment-6508963229) **typescript-automation[bot]** reported user test results comparing baseline and pr and highlighted new type errors in effect and lodash
 * [today](https://github.com/microsoft/TypeScript/pull/65034#issuecomment-6509138446) **typescript-automation[bot]** provided the requested performance run results
 * [today](https://github.com/microsoft/TypeScript/pull/65034#issuecomment-6510105307) **typescript-automation[bot]** reported TSC build comparison results for the top 400 repos and noted unexpected errors in cheaper-inference/OmniRoute

### [PR microsoft/TypeScript#65035](https://github.com/microsoft/TypeScript/pull/65035) (Open, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Avoid unnecessary work and allocations when instantiating type**

*Optimize type instantiation to avoid unnecessary work and memory allocations.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * **jakebailey** added label `Domain: Performance`
 * [today](https://github.com/microsoft/TypeScript/pull/65035#issuecomment-6508411427) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/65035#issuecomment-6508413133) **typescript-automation[bot]** started CI build jobs and posted status links
 * [today](https://github.com/microsoft/TypeScript/pull/65035#issuecomment-6509421755) **typescript-automation[bot]** reported the performance run results for compiler-unions native scenario
 * [today](https://github.com/microsoft/TypeScript/pull/65035#issuecomment-6509451347) **jakebailey** said "This helps a little, but, not really that much? Certainly alloc count though."

### [PR microsoft/TypeScript#65036](https://github.com/microsoft/TypeScript/pull/65036) (Open, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Avoid allocations and no\-op work during type inference**

*Optimize type inference by eliminating unnecessary allocations and no-op operations*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/65036#issuecomment-6508251991) **Copilot** noted that custom setup steps failed during the Copilot code review run and provided a link to the workflow run for details
 * **jakebailey** added label `Domain: Performance`
 * [today](https://github.com/microsoft/TypeScript/pull/65036#issuecomment-6508416005) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/65036#issuecomment-6508417718) **typescript-automation[bot]** reported that perf test jobs had started
 * [today](https://github.com/microsoft/TypeScript/pull/65036#issuecomment-6509640773) **typescript-automation[bot]** provided the requested perf run results including a comparison of baseline and pr metrics

### [PR microsoft/TypeScript#65037](https://github.com/microsoft/TypeScript/pull/65037) (Open, `Author: Team`, `For Uncommitted Bug`, **iisaduan**)

**Adds missing methods from checker api **

*Adds missing promise-based methods to the Checker API for symbol lookup, type queries, and literal types.*

 * created by **iisaduan**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **iisaduan**

### [PR microsoft/TypeScript#65038](https://github.com/microsoft/TypeScript/pull/65038) (Open, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Inline the common fast\-fail of isSimpleTypeRelatedTo**

*Refactor isSimpleTypeRelatedTo to inline common fast-fail checks and delegate full logic to a worker*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/65038#issuecomment-6508725087) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/65038#issuecomment-6508727049) **typescript-automation[bot]** posted build job status update with links to results
 * **jakebailey** added label `Domain: Performance`
 * [today](https://github.com/microsoft/TypeScript/pull/65038#issuecomment-6510081003) **typescript-automation[bot]** provided the performance run results for the baseline and PR comparison

### [PR microsoft/TypeScript#65039](https://github.com/microsoft/TypeScript/pull/65039) (Open, `For Uncommitted Bug`)

**fix\(64998\): defer index signature value types for keyof circularity**

*Multi-checker builds emit index signature value types as any from circular eager resolution, now using deferred and lazy resolution.*

 * created by **timurzvural**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [PR microsoft/TypeScript#65040](https://github.com/microsoft/TypeScript/pull/65040) (Open, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Avoid allocations and redundant work when checking calls and object literals**

*Eliminate unnecessary memory allocations and redundant processing when validating function calls and object literals.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/65040#issuecomment-6509788953) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/65040#issuecomment-6509791640) **typescript-automation[bot]** started performance test jobs and posted status and results links
 * **jakebailey** added label `Domain: Performance`
 * [today](https://github.com/microsoft/TypeScript/pull/65040#issuecomment-6510782162) **typescript-automation[bot]** reported the results of the requested performance run

### [PR microsoft/TypeScript#65041](https://github.com/microsoft/TypeScript/pull/65041) (Open, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Avoid closure and slice allocations in core helpers and type filtering**

*Remove closures and slice allocations from core helpers and type filtering to optimize performance.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/65041#issuecomment-6509796444) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/65041#issuecomment-6509798630) **typescript-automation[bot]** announced that performance tests started and that the comment will be updated with build results
 * **jakebailey** added label `Domain: Performance`
 * [today](https://github.com/microsoft/TypeScript/pull/65041#issuecomment-6510939371) **typescript-automation[bot]** shared the requested performance run results including detailed metrics

### [PR microsoft/TypeScript#65042](https://github.com/microsoft/TypeScript/pull/65042) (Open, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Cache type classification answers on types**

*Implement caching for type-based classification answers to enhance performance.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/65042#issuecomment-6510073594) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/65042#issuecomment-6510076005) **typescript-automation[bot]** started perf test jobs and provided build status and results links
 * **jakebailey** added label `Domain: Performance`
 * [today](https://github.com/microsoft/TypeScript/pull/65042#issuecomment-6511048296) **typescript-automation[bot]** provided the performance run results for the requested comparison

### [PR microsoft/TypeScript#65043](https://github.com/microsoft/TypeScript/pull/65043) (Open, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Speed up property and index signature lookups**

*Optimize property and index signature lookup processes to improve performance.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/65043#issuecomment-6510117828) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/65043#issuecomment-6510120464) **typescript-automation[bot]** reported that perf test jobs started and provided links to build status and results
 * **jakebailey** added label `Domain: Performance`
 * [today](https://github.com/microsoft/TypeScript/pull/65043#issuecomment-6511137405) **typescript-automation[bot]** posted perf run results as requested

### [PR microsoft/TypeScript#65044](https://github.com/microsoft/TypeScript/pull/65044) (Open, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Speed up node lookup by position, import scanning, and node allocation**

*Optimize node lookup performance by enhancing position-based searches, import scanning, and node allocation.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/65044#issuecomment-6510267016) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/65044#issuecomment-6510268748) **typescript-automation[bot]** posted automated build start notification
 * **jakebailey** added label `Domain: Performance`
 * [today](https://github.com/microsoft/TypeScript/pull/65044#issuecomment-6511266091) **typescript-automation[bot]** reported the requested performance run results for tsc

### [PR microsoft/TypeScript#65045](https://github.com/microsoft/TypeScript/pull/65045) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Reject non\-access targets early when matching access references**

*Move logic to reject non-access targets early in access reference matching to improve efficiency.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/65045#issuecomment-6510969442) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/65045#issuecomment-6510970606) **typescript-automation[bot]** announced that performance test jobs had started and provided links to their status and results
 * **jakebailey** added label `Domain: Performance`
 * [today](https://github.com/microsoft/TypeScript/pull/65045#issuecomment-6511745493) **typescript-automation[bot]** reported the performance run results for tsc comparing baseline and pr

### [PR microsoft/TypeScript#65046](https://github.com/microsoft/TypeScript/pull/65046) (Open, `Author: Team`, `For Uncommitted Bug`, `dependencies`, `javascript`)

**Bump @azure/msal\-node and @azure/identity**

*Bump @azure/msal-node from version 6.0.0 to 7.1.2 alongside @azure/identity to keep dependencies in sync.*

 * created by **dependabot[bot]**
 * (today) **dependabot[bot]** added labels `dependencies`, `javascript`
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/65046#issuecomment-6525738215) **RyanCavanaugh** said "Need to get CI green here first"

### [PR microsoft/TypeScript#65047](https://github.com/microsoft/TypeScript/pull/65047) (Open, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**Allow content mapper registrations to filter their files with an \`include\` glob, inherit default \`extension\` from manifest**

*Enable content mapper registrations to filter files using an include glob and inherit the default extension from the manifest.*

 * created by **andrewbranch**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **andrewbranch**

### [Issue microsoft/TypeScript#65048](https://github.com/microsoft/TypeScript/issues/65048) (Closed)

**Default parameter symbol lookup incorrectly selects a body function declaration**

*TypeScript’s compiler API resolves a default parameter symbol to an inner function instead of the outer variable binding.*

 * created by **CaliLuke**
 * [later](https://github.com/microsoft/TypeScript/issues/65048#issuecomment-6522192118) **RyanCavanaugh** said "If a human ever reads this agent-reported issue: the 6.0 API is no longer maintained and there's no repro for this."
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#65049](https://github.com/microsoft/TypeScript/issues/65049) (Open)

**sync API: the client and the server spend more time waiting for each other's next message than handling it; a small change to how both wait**

*A proposed adjustment to TypeScript’s sync API client-server waiting mechanism aims to reduce CPU idle exit latency and improve out-of-process round-trip performance.*

 * created by **WinterYukky**

### [PR microsoft/TypeScript#65050](https://github.com/microsoft/TypeScript/pull/65050) (Closed, `Author: Team`, `For Uncommitted Bug`)

**Update localization files**

*Update localization files and regenerate corresponding runtime artifacts.*

 * created by **typescript-automation[bot]**
 * (later) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`
 * (later) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#65051](https://github.com/microsoft/TypeScript/issues/65051) (Open)

**API: coarse\-grained checker queries for tools that extract a whole API surface \(\`getSymbolDocumentations\`, \`getMembersOfType\`\)**

*Add batch methods for retrieving JSDoc and member details of whole types to reduce checker round trips for API extractors.*

 * created by **WinterYukky**
 * [later](https://github.com/microsoft/TypeScript/issues/65051#issuecomment-6518847399) **aetherxeg-source** proposed adding a differential regression fixture to compare coarse- and fine-grained getMembersOfType results across various member scenarios
 * [later](https://github.com/microsoft/TypeScript/issues/65051#issuecomment-6519041664) **WinterYukky** said "Thanks, good suggestion. I'll add a differential fixture comparing both paths on the same program to the PR."

### [Issue microsoft/TypeScript#65052](https://github.com/microsoft/TypeScript/issues/65052) (Open)

**7\.0 regression: inherited members are sorted by position, so an empty subinterface changes assignability**

*TypeScript 7.0 regresses interface assignability by sorting inherited members by position, wrongly allowing assignments in empty subinterfaces.*

 * created by **pearofducks**

### [Issue microsoft/TypeScript#65053](https://github.com/microsoft/TypeScript/issues/65053) (Closed)

**TypeScript 7 VS Code extension: Member completion in derived class does not scaffold full property signature**

*TypeScript 7 VS Code extension’s member completion in derived classes fails to scaffold full inherited property signatures.*

 * created by **wjnotl**
 * [later](https://github.com/microsoft/TypeScript/issues/65053#issuecomment-6525196616) **a-tarasyuk** asked which TypeScript version was being used, noted that support landed in PR #3949 and the beta, provided a config snippet, opened a verification PR, and offered to revisit reproduction steps if needed
 * [later](https://github.com/microsoft/TypeScript/issues/65053#issuecomment-6526659382) **wjnotl** acknowledged the version issue, updated TypeScript to 7.1.0-beta, confirmed the fix, thanked and suggested closing
 * (later) **wjnotl** closed the issue

### [Issue microsoft/TypeScript#65054](https://github.com/microsoft/TypeScript/issues/65054) (Open)

**API server panics in acquireConfigForFile when opening a JS file a tsconfig does not include**

*TypeScript sync API server panics when opening a JS file not included in tsconfig starting in version 7.1.0-beta.*

 * created by **0x80**

### [PR microsoft/TypeScript#65055](https://github.com/microsoft/TypeScript/pull/65055) (Open, `For Uncommitted Bug`)

**fix\(65053\): cover protected optional property completion**

*Enable code completion support for protected optional class properties.*

 * created by **a-tarasyuk**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [PR microsoft/TypeScript#65056](https://github.com/microsoft/TypeScript/pull/65056) (Open, `Domain: Performance`, `For Uncommitted Bug`)

**\[experiment\] Avoid resolving property types that cannot be unit types when looking for key properties**

*Skip resolving property types that aren’t unit types when identifying key properties.*

 * created by **Andarist**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/65056#issuecomment-6526164087) **jakebailey** said "@typescript-bot test it"
 * [later](https://github.com/microsoft/TypeScript/pull/65056#issuecomment-6526166358) **typescript-automation[bot]** said "Hey @jakebailey, this PR was updated less than two minutes before this command. Please wait until it has been unchanged for two minutes and try again."
 * [later](https://github.com/microsoft/TypeScript/pull/65056#issuecomment-6526317046) **jakebailey** said "@typescript-bot test it"
 * [later](https://github.com/microsoft/TypeScript/pull/65056#issuecomment-6526319316) **typescript-automation[bot]** posted automated build status updates
 * [later](https://github.com/microsoft/TypeScript/pull/65056#issuecomment-6527098197) **typescript-automation[bot]** informed that the DT test results were ready and remained unchanged

### [Issue microsoft/TypeScript#65057](https://github.com/microsoft/TypeScript/issues/65057) (Open)

**Native printer panics when printing JSDoc AST nodes**

*TypeScript 7’s native printer panics with a “not implemented” error when printing JSDoc AST nodes directly.*

 * created by **el-j**

### [PR microsoft/TypeScript#65058](https://github.com/microsoft/TypeScript/pull/65058) (Open, `For Uncommitted Bug`)

**feat\(printer\): implement JSDoc node emission in AST printer**

*Implements JSDoc node emission in the AST printer, supporting blocks, tags, parameter types, inline links, and adds related tests.*

 * created by **el-j**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [PR microsoft/TypeScript#65059](https://github.com/microsoft/TypeScript/pull/65059) (Open, `Author: Team`, `For Milestone Bug`, **ahejlsberg**, **gabritto**)

**Allow accessing named declared members during a type's resolution**

*Enable accessing both declared and inherited named members during lazy type resolution*

 * created by **ahejlsberg**
 * (later) **typescript-automation[bot]** added labels `Author: Team`, `For Milestone Bug`, `For Milestone Bug`, and assigned to **ahejlsberg**, **gabritto**
 * [later](https://github.com/microsoft/TypeScript/pull/65059#issuecomment-6527083233) **ahejlsberg** said "@typescript-bot test it"
 * [later](https://github.com/microsoft/TypeScript/pull/65059#issuecomment-6527085078) **typescript-automation[bot]** posted automated build status updates with command statuses and results links

