# Report for 2026-10-28 (Wednesday, October 28th, 2026)

16 different users commented on 47 different issues.

## Recommended Actions

 * Response Recommended
    * @YevheniiKotyrlo provided repro steps as requested in [microsoft/TypeScript#63854](https://github.com/microsoft/TypeScript/issues/63854#issuecomment-6489142249)
    * @Phil2812 asked whether the reviver parameter of JSON.parse should remain optional in [microsoft/TypeScript#64096](https://github.com/microsoft/TypeScript/pull/64096#issuecomment-6497064437)

## Activity Summary

### [Issue microsoft/TypeScript#22682](https://github.com/microsoft/TypeScript/issues/22682) (Closed, `Bug`, `Help Wanted`, `Effort: Casual`, `Domain: Parser`)

**Missing error if ClassDeclaration is used in Statement position**

*Class and enum declarations inside an if statement don't trigger compile errors, leading to runtime failures when transpiled to ES2015+.*

 * [4.8 years ago](https://github.com/microsoft/TypeScript/issues/22682#issuecomment-999211721) **nicdard** said "I would like to try to help with this one"
 * **RyanCavanaugh** added label `Domain: Parser`
 * [51 weeks ago](https://github.com/microsoft/TypeScript/issues/22682#issuecomment-3470036734) **RyanCavanaugh** clarified the repro by showing a file with a syntax error
 * [today](https://github.com/microsoft/TypeScript/issues/22682#issuecomment-6485660368) **TimonGaertner** offered to work on the issue and described a fix that reports TS1156 for class declarations outside blocks
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63854](https://github.com/microsoft/TypeScript/issues/63854) (Open, `Needs More Info`)

**Identical resolved program produces 157 vs 662,155 diagnostics depending on whether the tsconfig is passed directly or through a pass\-through extends**

*Using a pass-through tsconfig that simply extends the main config results in drastically more TypeScript diagnostics than direct config usage.*

 * created by **michaeldanish**
 * **RyanCavanaugh** added label `Needs More Info`
 * [15 weeks ago](https://github.com/microsoft/TypeScript/issues/63854#issuecomment-5351507057) **RyanCavanaugh** suggested using the repro reduction skill and linked to the TypeScript Maintainer Skills repository
 * [today](https://github.com/microsoft/TypeScript/issues/63854#issuecomment-6489142249) **YevheniiKotyrlo** provided a dependency-free repro demonstrating TS2859 on identical types after extensive comparisons, including a generation script, reproduction commands, and error outputs on TS versions 7.1.0-dev and 7.0.2

### [PR microsoft/TypeScript#64096](https://github.com/microsoft/TypeScript/pull/64096) (Closed, `For Milestone Bug`, **DanielRosenwasser**)

**feat: add es2026 as a valid target and lib**

*Add ES2026 as a recognized compilation target and library option in TypeScript.*

 * [1 month ago](https://github.com/microsoft/TypeScript/pull/64096#issuecomment-5827319061) **typescript-automation[bot]** notified that DT tests results were ready and unchanged
 * [1 month ago](https://github.com/microsoft/TypeScript/pull/64096#issuecomment-5874852728) **DanielRosenwasser** expressed happiness about lib tests and noted baseline merge conflicts
 * (1 month ago) **DanielRosenwasser** closed the issue
 * [later](https://github.com/microsoft/TypeScript/pull/64096#issuecomment-6497064437) **Phil2812** asked whether the reviver parameter should remain optional in JSON.parse's type definition
 * [later](https://github.com/microsoft/TypeScript/pull/64096#issuecomment-6501537953) **jakebailey** said "@Phil2812 please file an issue"

### [PR microsoft/TypeScript#64169](https://github.com/microsoft/TypeScript/pull/64169) (Open, `For Backlog Bug`)

**Preserve \`\<\` in \`getChildren\(\)\` when type arguments begin with \`\<\`**

*Update getChildren() to preserve the leading “<” token when type arguments begin with “<”*

 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/64169#issuecomment-6156966758) **jakebailey** said "Is there an equivalent to this in Corsa?"
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64169#issuecomment-6314625081) **Andarist** said "@jakebailey i doublechecked with Strada and it had the same bug"
 * [today](https://github.com/microsoft/TypeScript/pull/64169#issuecomment-6483055513) **andrewbranch** interpreted Jake as asking whether an equivalent change needed to happen in the Go code

### [PR microsoft/TypeScript#64174](https://github.com/microsoft/TypeScript/pull/64174) (Closed, `Author: Team`, `For Milestone Bug`, **jakebailey**)

**Add wasip1 support, enabling CLI, API, browser, sync/async**

*Add experimental wasip1-based WebAssembly build of tsc enabling CLI, LSP, and sync/async API use in Node and browser environments.*

 * [6 weeks ago](https://github.com/microsoft/TypeScript/pull/64174#issuecomment-5703651081) **NullVoxPopuli** expressed surprise at the globalThis.fs interface, asked about standards, and suggested passing fs access options or using a global mock fs
 * [6 weeks ago](https://github.com/microsoft/TypeScript/pull/64174#issuecomment-5704509646) **NullVoxPopuli** indicated that the feature worked somewhat and attached screenshots
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64174#issuecomment-6328669720) **jakebailey** announced readiness for review and that they had dropped the “tsc falls back to wasm” idea because Node’s WASI host did not work on Windows
 * [today](https://github.com/microsoft/TypeScript/pull/64174#issuecomment-6483054352) **jakebailey** proposed follow-up work to avoid bundling libs in the binary by adding a new flag for the lib directory and to enable vscode.dev
 * [today](https://github.com/microsoft/TypeScript/pull/64174#issuecomment-6484053015) **jakebailey** said "Hm, concerning test timeout "

### [PR microsoft/TypeScript#64266](https://github.com/microsoft/TypeScript/pull/64266) (Open, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Improve performance of batched requests**

*Automatically batch requests across all API endpoints with code generation, remove hardcoded entrypoints, switch to struct-of-arrays layout for better performance.*

 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [6 weeks ago](https://github.com/microsoft/TypeScript/pull/64266#issuecomment-5687798292) **weswigham** explained that they updated the server to support efficient batch requests with shared parameters for all protocol methods, avoiding maintaining separate singular and bulk wire protocol implementations
 * **jakebailey** added label `Domain: Performance`
 * [today](https://github.com/microsoft/TypeScript/pull/64266#issuecomment-6482459760) **RyanCavanaugh** said "Moving to draft due to merge conflicts + unclear if this change is approved in principle"

### [PR microsoft/TypeScript#64502](https://github.com/microsoft/TypeScript/pull/64502) (Closed, `For Backlog Bug`)

**Fix false circularity for static fields in generic class expressions**

*Avoid treating contextual property lookups as circular in generic class expressions, preventing incorrect TS7022 on static fields.*

 * [1 month ago](https://github.com/microsoft/TypeScript/pull/64502#issuecomment-5874793429) **Fugu0141** said "@microsoft-github-policy-service agree"
 * [1 month ago](https://github.com/microsoft/TypeScript/pull/64502#issuecomment-5887522333) **Andarist** reopened a prior PR to TS 6.0 with a simpler fix and suggested using another test case to advocate for the current approach
 * [1 month ago](https://github.com/microsoft/TypeScript/pull/64502#issuecomment-5887759684) **Fugu0141** acknowledged that issue #64525 was more targeted and offered to close the change in its favor unless maintainers preferred the broader approach
 * [today](https://github.com/microsoft/TypeScript/pull/64502#issuecomment-6477645038) **Fugu0141** said "Closing this PR in favor of #64525, which has already been merged and resolves #62552."
 * (today) **Fugu0141** closed the issue

### [Issue microsoft/TypeScript#64532](https://github.com/microsoft/TypeScript/issues/64532) (Closed, `Needs Investigation`, **andrewbranch**)

**\[API\] \`getImmediateAliasedSymbol\` returns a different symbol than classic \`tsc\`**

*getImmediateAliasedSymbol for namespace imports in TypeScript 7 returns a cloned symbol instead of the original file symbol when a module has a default export.*

 * **RyanCavanaugh** added to milestone `TypeScript 7.1.1 RC`
 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/64532#issuecomment-6151189735) **andrewbranch** said "We have checker.getTargetSymbol(symbol). Does that not address this?"
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/64532#issuecomment-6271815914) **dragomirtitian** said "@andrewbranch Does not seem to. getTargetSymbol returns the same symbol. "
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#64679](https://github.com/microsoft/TypeScript/pull/64679) (Closed, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Add createFileSystemFromSnapshot\(oldSnapshot, extraFSLayer\)**

*Implement createFileSystemFromSnapshot to reapply a previous snapshot’s synthetic file system onto a new snapshot with optional layering.*

 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64679#issuecomment-6303338637) **andrewbranch** described concerns about ambiguity in the rebase API's unspecified base snapshot and potential confusion when using it on non-LSP snapshots
 * [6 days ago](https://github.com/microsoft/TypeScript/pull/64679#issuecomment-6347271080) **weswigham** realized that the FS structure only reused the final state rather than replaying all intermediate snapshots and proposed renaming the API and updating the PR
 * [6 days ago](https://github.com/microsoft/TypeScript/pull/64679#issuecomment-6348197362) **weswigham** said "@andrewbranch does createFileSystemFromSnapshot like this work for you? Makes sense to me."
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript#64695](https://github.com/microsoft/TypeScript/pull/64695) (Open, `Domain: Performance`, `For Milestone Bug`, **ahejlsberg**)

**\[experiment\] Skip incompatible discriminants when inferring**

*Experimentally skip incompatible discriminant properties during TypeScript union type inference to reduce workload and validate via tests.*

 * [4 days ago](https://github.com/microsoft/TypeScript/pull/64695#issuecomment-6384191000) **typescript-automation[bot]** reported starting of performance test jobs and provided links to status and results
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/64695#issuecomment-6384500825) **typescript-automation[bot]** posted the requested performance run results comparing baseline to PR metrics
 * **jakebailey** added label `Domain: Performance`
 * [later](https://github.com/microsoft/TypeScript/pull/64695#issuecomment-6500291770) **jakebailey** said "@typescript-bot perf test this faster"
 * [later](https://github.com/microsoft/TypeScript/pull/64695#issuecomment-6500294727) **typescript-automation[bot]** started jobs and updated status table with build links
 * [later](https://github.com/microsoft/TypeScript/pull/64695#issuecomment-6501621156) **typescript-automation[bot]** posted the requested perf run results

### [PR microsoft/TypeScript#64699](https://github.com/microsoft/TypeScript/pull/64699) (Open, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Intern symbol names as pointer\-free IDs**

*Symbol names are now represented as pointer-free 64-bit interned IDs to improve memory efficiency and reduce GC overhead.*

 * [today](https://github.com/microsoft/TypeScript/pull/64699#issuecomment-6471257938) **jakebailey** requested that the TypeScript bot run performance tests faster before another refactor
 * [today](https://github.com/microsoft/TypeScript/pull/64699#issuecomment-6471260423) **typescript-automation[bot]** started jobs and posted a status table linking to the build and results
 * [today](https://github.com/microsoft/TypeScript/pull/64699#issuecomment-6472224109) **typescript-automation[bot]** provided the requested performance run results
 * [today](https://github.com/microsoft/TypeScript/pull/64699#issuecomment-6474668587) **jakebailey** clarified that the perceived regression in 64-bit was due to a symbol table layout change rather than this PR and noted that reverting to 32-bit yields no change
 * [today](https://github.com/microsoft/TypeScript/pull/64699#issuecomment-6474766454) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/64699#issuecomment-6474768614) **typescript-automation[bot]** reported that performance tests started and provided links to build status and results
 * [today](https://github.com/microsoft/TypeScript/pull/64699#issuecomment-6476079627) **typescript-automation[bot]** said "@jakebailey, the perf run you requested failed. You can check the log here."
 * [today](https://github.com/microsoft/TypeScript/pull/64699#issuecomment-6476744338) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/64699#issuecomment-6476746594) **typescript-automation[bot]** reported that the perf test job was started and provided links to the build status and results
 * [today](https://github.com/microsoft/TypeScript/pull/64699#issuecomment-6477932753) **typescript-automation[bot]** provided the requested performance run results
 * [today](https://github.com/microsoft/TypeScript/pull/64699#issuecomment-6481348111) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/64699#issuecomment-6481349927) **typescript-automation[bot]** said "Hey @jakebailey, this PR is in an unmergable state, so is missing a merge commit to run against; please resolve conflicts and try again."
 * [today](https://github.com/microsoft/TypeScript/pull/64699#issuecomment-6481498131) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/64699#issuecomment-6481499919) **typescript-automation[bot]** started CI performance test jobs and posted build status and result links
 * [today](https://github.com/microsoft/TypeScript/pull/64699#issuecomment-6482436840) **typescript-automation[bot]** reported the performance run results requested by @jakebailey
 * [today](https://github.com/microsoft/TypeScript/pull/64699#issuecomment-6482505500) **jakebailey** mentioned that reducing parse time via interning cost required complex methods and still leaked 32-bit worth of names, amounting to about 2 billion names
 * [today](https://github.com/microsoft/TypeScript/pull/64699#issuecomment-6482754322) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/64699#issuecomment-6482756042) **typescript-automation[bot]** reported the start of performance test builds and provided links to results
 * [today](https://github.com/microsoft/TypeScript/pull/64699#issuecomment-6483710274) **typescript-automation[bot]** posted the performance run results with a detailed tsc comparison report

### [Issue microsoft/TypeScript#64740](https://github.com/microsoft/TypeScript/issues/64740) (Open, `Needs Investigation`, **andrewbranch**)

**\[API\] \`ConditionalType\` has no counterpart to \`root\` of TypeScript 6 \(the node it was declared with\)**

*TypeScript 7's ConditionalType API lacks a counterpart to the TS6 root property, preventing retrieval of the original conditional type declaration node.*

 * created by **MARCROCK22**
 * (1 week ago) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **andrewbranch**
 * **andrewbranch** added to milestone `TypeScript 7.1.1 RC`

### [PR microsoft/TypeScript#64748](https://github.com/microsoft/TypeScript/pull/64748) (Closed, `For Backlog Bug`)

**Fix broken augmentExportEquals2 test fixture**

*Removed duplicate //@filename: file3.ts directive in augmentExportEquals2 test to restore expected diagnostics.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/64748#issuecomment-6123625457) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (2 days ago) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64750](https://github.com/microsoft/TypeScript/pull/64750) (Open, `For Uncommitted Bug`)

**Add support for Jujutsu conflict markers**

*Enhance the compiler scanner to recognize Jujutsu VCS conflict markers, handle varied marker lengths, and manage section state.*

 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64750#issuecomment-6237153149) **rf-** questioned whether the couldStartTrivia function was vestigial dead code in Go and suggested its removal
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64750#issuecomment-6278628845) **jakebailey** said "I think we can probably just do the simple easy version of this and it be sufficient; this is a best effort recovery after all so I think that's ok."
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/64750#issuecomment-6405051289) **rf-** explained that they implemented the correct solution and pushed an update addressing the issues
 * [today](https://github.com/microsoft/TypeScript/pull/64750#issuecomment-6480864675) **jakebailey** requested typescript-bot to test
 * [today](https://github.com/microsoft/TypeScript/pull/64750#issuecomment-6480866587) **typescript-automation[bot]** reported build job statuses
 * [today](https://github.com/microsoft/TypeScript/pull/64750#issuecomment-6481495370) **typescript-automation[bot]** notified that the DT test results were ready and unchanged
 * [today](https://github.com/microsoft/TypeScript/pull/64750#issuecomment-6481926307) **typescript-automation[bot]** reported the results of the requested perf run
 * [today](https://github.com/microsoft/TypeScript/pull/64750#issuecomment-6482079949) **typescript-automation[bot]** reported tsc user test results and confirmed everything looked good
 * [today](https://github.com/microsoft/TypeScript/pull/64750#issuecomment-6483130269) **typescript-automation[bot]** reported that running the top 400 repos tsc comparison between baseline and pr succeeded without issues

### [PR microsoft/TypeScript#64867](https://github.com/microsoft/TypeScript/pull/64867) (Closed, `Author: Team`, `For Milestone Bug`, **andrewbranch**)

**Restore behavior of getImmediateAliasedSymbol**

*Restore getImmediateAliasedSymbol’s previous behavior to ensure consistent TypeScript 6 API semantics.*

 * (1 week ago) **typescript-automation[bot]** added labels `Author: Team`, `For Milestone Bug`, and assigned to **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#64871](https://github.com/microsoft/TypeScript/pull/64871) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Speed up short\-lived checker caches**

*Optimize short-lived checker caches by replacing costly Go map clears with generation-counter tables and simpler key hashing for speed improvements.*

 * [5 days ago](https://github.com/microsoft/TypeScript/pull/64871#issuecomment-6376264609) **typescript-automation[bot]** reported starting of perf test job and provided status and results links
 * [5 days ago](https://github.com/microsoft/TypeScript/pull/64871#issuecomment-6379059712) **typescript-automation[bot]** provided performance run results for the requested comparison
 * **jakebailey** added label `Domain: Performance`
 * [today](https://github.com/microsoft/TypeScript/pull/64871#issuecomment-6481785120) **ahejlsberg** said "This one seems to have some nice effects."
 * [today](https://github.com/microsoft/TypeScript/pull/64871#issuecomment-6481824179) **jakebailey** said "Yeah, I'm just maybe a little unnerved by the manual fiddling with the hashes."

### [PR microsoft/TypeScript#64906](https://github.com/microsoft/TypeScript/pull/64906) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Add tests for check order dependence**

*Add tests that expose and document order-dependent behaviors in checks to ensure consistency.*

 * (1 week ago) **typescript-automation[bot]** added labels `Author: Team`, `Author: Team`, `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64906#issuecomment-6481649710) **jakebailey** said "Drafting for now, as I need to update this with the plethora of new cases I've found"

### [Issue microsoft/TypeScript#64917](https://github.com/microsoft/TypeScript/issues/64917) (Closed, `Domain: Error Messages`, `Possible Improvement`)

**"Content mapper file extension '\.const\.json' is a built\-in extension and cannot be registered by a content mapper\." error is misleading**

*Error message incorrectly labels .const.json as a built-in extension instead of clarifying its conflict with .json or supporting .const.json patterns*

 * (2 days ago) **RyanCavanaugh** added labels `Domain: Error Messages`, `Possible Improvement`, and set milestone to `Backlog`
 * (later) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#64921](https://github.com/microsoft/TypeScript/pull/64921) (Closed, `For Backlog Bug`)

**Clarify error when content mapper extension ends in a built\-in extension**

*Change TS18066 diagnostic to clarify that content mapper extensions ending in built-in extensions are disallowed.*

 * [6 days ago](https://github.com/microsoft/TypeScript/pull/64921#issuecomment-6339608951) **govardhanchinta99** said "@microsoft-github-policy-service agree"
 * (2 days ago) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64921#issuecomment-6488680995) **govardhanchinta99** asked for re-approval after restoring generated localization bundles and merging main
 * (later) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#64922](https://github.com/microsoft/TypeScript/pull/64922) (Open, `For Uncommitted Bug`)

**Emit the files of each checker in a deterministic order**

*Ensure each checker emits its files in a consistent, deterministic order to eliminate non-determinism.*

 * [6 days ago](https://github.com/microsoft/TypeScript/pull/64922#issuecomment-6343818376) **jakebailey** said "@typescript-bot perf test this faster"
 * [6 days ago](https://github.com/microsoft/TypeScript/pull/64922#issuecomment-6343820685) **typescript-automation[bot]** announced that the perf test job started and provided links to build status and results
 * [6 days ago](https://github.com/microsoft/TypeScript/pull/64922#issuecomment-6344528856) **typescript-automation[bot]** reported the requested performance run results
 * [today](https://github.com/microsoft/TypeScript/pull/64922#issuecomment-6481056079) **jakebailey** asked the TypeScript bot to rerun performance tests faster after benchmarks updated
 * [today](https://github.com/microsoft/TypeScript/pull/64922#issuecomment-6481057840) **typescript-automation[bot]** said "Hey @jakebailey, this PR was updated less than two minutes before this command. Please wait until it has been unchanged for two minutes and try again."
 * [today](https://github.com/microsoft/TypeScript/pull/64922#issuecomment-6481143095) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/64922#issuecomment-6481145064) **typescript-automation[bot]** reported that CI jobs started and provided links to statuses
 * [today](https://github.com/microsoft/TypeScript/pull/64922#issuecomment-6482059622) **typescript-automation[bot]** reported the performance run results comparing baseline to PR for tsc metrics
 * [today](https://github.com/microsoft/TypeScript/pull/64922#issuecomment-6489190356) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [today](https://github.com/microsoft/TypeScript/pull/64922#issuecomment-6489410209) **jakebailey** requested the TypeScript bot to run performance tests faster
 * [today](https://github.com/microsoft/TypeScript/pull/64922#issuecomment-6489411417) **typescript-automation[bot]** reported CI job start status for the perf test this faster command
 * [later](https://github.com/microsoft/TypeScript/pull/64922#issuecomment-6490336444) **typescript-automation[bot]** posted perf run results comparing baseline and PR metrics, including errors, symbols, types, memory usage, and allocations

### [Issue microsoft/TypeScript#64927](https://github.com/microsoft/TypeScript/issues/64927) (Closed, `Bug`)

**augmentExportEquals2 fixture has a duplicate @filename directive**

*A duplicate @filename directive in the augmentExportEquals2 fixture causes file3.ts to be overwritten and errors to be ignored, which the PR corrects.*

 * created by **mahesh-desu**
 * (2 days ago) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64928](https://github.com/microsoft/TypeScript/pull/64928) (Closed, `Domain: Performance`, `For Backlog Bug`)

**Reuse token lookup visitor across AST descent**

*Reuse a single NodeVisitor for each token lookup to reduce allocations and improve getTokenAtPosition performance.*

 * (2 days ago) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`
 * **jakebailey** added label `Domain: Performance`
 * [today](https://github.com/microsoft/TypeScript/pull/64928#issuecomment-6489938948) **DanielRosenwasser** said "@typescript-bot perf test this"
 * [today](https://github.com/microsoft/TypeScript/pull/64928#issuecomment-6489940768) **typescript-automation[bot]** reported that the performance test build started and provided links to status and results
 * [later](https://github.com/microsoft/TypeScript/pull/64928#issuecomment-6490794458) **typescript-automation[bot]** provided the results of the requested performance run

### [Issue microsoft/TypeScript#64948](https://github.com/microsoft/TypeScript/issues/64948) (Closed, `Won't Fix`)

**Stack overflow in getEffectsSignature for long comma\-separated call chains \(e\.g\. minified bundles with allowJs\)**

*Very long comma-separated call chains in minified JS with allowJs cause getEffectsSignature to overflow the call stack.*

 * [5 days ago](https://github.com/microsoft/TypeScript/issues/64948#issuecomment-6379725408) **AbbasFullstack** said "If you need any type help tell me I am 24/7  for help"
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/64948#issuecomment-6424079965) **RyanCavanaugh** noted the issue was fixed in version 7.0, called static analysis of heavily minified files largely useless, and recommended using a different parser for degenerate inputs
 * **RyanCavanaugh** added label `Won't Fix`
 * [today](https://github.com/microsoft/TypeScript/issues/64948#issuecomment-6485075349) **typescript-automation[bot]** said "This issue has been marked as "Won't Fix" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-automation[bot]** closed the issue

### [Issue microsoft/TypeScript#64957](https://github.com/microsoft/TypeScript/issues/64957) (Closed, `Question`)

**type Exclude on class hierarchy resolves to never**

*Excluding a subclass from a union of structurally identical classes unexpectedly resolves to never in TypeScript.*

 * [3 days ago](https://github.com/microsoft/TypeScript/issues/64957#issuecomment-6401436606) **irfanstract** suggested adding private fields to classes to preserve type soundness without bloating runtime properties
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/64957#issuecomment-6401749375) **jcalz** offered an alternative using type-only class fields and asked for a concrete use case to justify distinguishing structurally identical types
 * **RyanCavanaugh** added label `Question`
 * [today](https://github.com/microsoft/TypeScript/issues/64957#issuecomment-6485074545) **typescript-automation[bot]** said "This issue has been marked as "Question" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-automation[bot]** closed the issue

### [PR microsoft/TypeScript#64969](https://github.com/microsoft/TypeScript/pull/64969) (Closed, `For Uncommitted Bug`)

**Add a regression test for narrowing NoInfer union constituents of non\-generic aliases**

*Add a regression test to cover narrowing NoInfer union constituents in non-generic type aliases*

 * created by **Andarist**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/64969#issuecomment-6415926070) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64973](https://github.com/microsoft/TypeScript/pull/64973) (Open, `Author: Team`, `For Uncommitted Bug`, **johnfav03**)

**Fix non\-root dependency tracking in build watch mode**

*Enable build watch mode to detect changes in non-root imported files even when incremental builds are disabled.*

 * (2 days ago) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/64973#issuecomment-6429603044) **jakebailey** described a Go test case demonstrating stale output due to coalesced directory delete/recreate events and noted a fix by removing an early return
 * [today](https://github.com/microsoft/TypeScript/pull/64973#issuecomment-6480991125) **jakebailey** said "I'm sort of having a hard time trying to review this; is this potentially possible to rebase into a few commits? Or is it definitely that all is required and one single fix?"

### [PR microsoft/TypeScript#64984](https://github.com/microsoft/TypeScript/pull/64984) (Open, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Add distributive conditional type relationship rules**

*Add distributive conditional type relationship rules with a function type mapper to ensure correct assignability and inference handling.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/64984#issuecomment-6458048810) **jakebailey** said "@typescript-bot perf test this faster"
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64984#issuecomment-6458050513) **typescript-automation[bot]** posted an automated build status update
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64984#issuecomment-6458501848) **typescript-automation[bot]** posted the requested performance run results for tsc
 * [today](https://github.com/microsoft/TypeScript/pull/64984#issuecomment-6480774378) **weswigham** said "@typescript-bot test this"
 * [today](https://github.com/microsoft/TypeScript/pull/64984#issuecomment-6480776424) **typescript-automation[bot]** reported CI build statuses and result links for various jobs
 * [today](https://github.com/microsoft/TypeScript/pull/64984#issuecomment-6481496993) **typescript-automation[bot]** noted that the DT test results were ready and unchanged
 * [today](https://github.com/microsoft/TypeScript/pull/64984#issuecomment-6481642310) **typescript-automation[bot]** reported new TS2578 errors for unused '@ts-expect-error' directives in ai-docgen and effect packages
 * [today](https://github.com/microsoft/TypeScript/pull/64984#issuecomment-6481736767) **typescript-automation[bot]** posted the requested perf run comparison report
 * [today](https://github.com/microsoft/TypeScript/pull/64984#issuecomment-6483074145) **typescript-automation[bot]** reported that tsc runs on the top 400 repos comparing baseline and pr succeeded

### [PR microsoft/TypeScript#64986](https://github.com/microsoft/TypeScript/pull/64986) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Add a default PGO profile for the compiler**

*Add a default PGO profile generated from representative compiler scenarios using the TypeScript benchmarking workflow.*

 * [today](https://github.com/microsoft/TypeScript/pull/64986#issuecomment-6463007496) **typescript-automation[bot]** reported that performance tests started and provided links to status and results
 * [today](https://github.com/microsoft/TypeScript/pull/64986#issuecomment-6463839333) **typescript-automation[bot]** posted performance results for the requested run including baseline-to-PR comparison metrics for tsc
 * **jakebailey** added label `Domain: Performance`
 * [today](https://github.com/microsoft/TypeScript/pull/64986#issuecomment-6480242608) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/64986#issuecomment-6480244436) **typescript-automation[bot]** posted automated build status update
 * [today](https://github.com/microsoft/TypeScript/pull/64986#issuecomment-6481225139) **typescript-automation[bot]** posted performance run results comparing baseline and PR metrics for tsc
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64993](https://github.com/microsoft/TypeScript/pull/64993) (Open, `For Uncommitted Bug`)

**Drop statements a top\-level await reparse consumed to the end of the file**

*Prevent top-level await reparsing from copying original statements past EOF to avoid overlapping parsed statements.*

 * created by **roninjin10**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64993#issuecomment-6481192897) **roninjin10** said "@microsoft-github-policy-service agree company="Tevm Inc""

### [PR microsoft/TypeScript#64994](https://github.com/microsoft/TypeScript/pull/64994) (Open, `For Uncommitted Bug`)

**Format Document: shift the indenters a moved line break carries along**

*Adding line breaks before tokens makes document formatting non-idempotent by shifting nested indenters due to stale deltas and improper resets.*

 * created by **roninjin10**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64994#issuecomment-6469533497) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [today](https://github.com/microsoft/TypeScript/pull/64994#issuecomment-6481193353) **roninjin10** said "@microsoft-github-policy-service agree company="Tevm Inc""

### [PR microsoft/TypeScript#64996](https://github.com/microsoft/TypeScript/pull/64996) (Open, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Inline storage for small symbol tables**

*Adding inline storage for four entries in small symbol tables reduces allocations by 33% and improves binding performance by 10%.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/64996#issuecomment-6476445627) **Copilot** informed that custom setup steps failed and advised checking the workflow run and fixing the configuration
 * **jakebailey** added label `Domain: Performance`
 * [today](https://github.com/microsoft/TypeScript/pull/64996#issuecomment-6476742992) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/64996#issuecomment-6476744867) **typescript-automation[bot]** started performance test jobs and linked build status and results
 * [today](https://github.com/microsoft/TypeScript/pull/64996#issuecomment-6477758972) **typescript-automation[bot]** posted perf run results for the requested comparison
 * [today](https://github.com/microsoft/TypeScript/pull/64996#issuecomment-6478892575) **jakebailey** said "Definitely fewer allocs but a bit unclear how much it matters."
 * [today](https://github.com/microsoft/TypeScript/pull/64996#issuecomment-6481704128) **ahejlsberg** said "Yeah, not sure this one is worth it."
 * [today](https://github.com/microsoft/TypeScript/pull/64996#issuecomment-6481733678) **DanielRosenwasser** suggested using stack-allocated symbol table variants and deferring to a general SymbolMap when tables need to escape
 * [today](https://github.com/microsoft/TypeScript/pull/64996#issuecomment-6482409075) **ahejlsberg** stated that most symbol tables escape to the heap because they’re attached to AST nodes or symbols and suggested placing them there initially
 * [today](https://github.com/microsoft/TypeScript/pull/64996#issuecomment-6482423627) **jakebailey** said "Yeah, I just tried, and it doesn't seem to help (or makes things worse), because the compiler just isn't smart enough."
 * [later](https://github.com/microsoft/TypeScript/pull/64996#issuecomment-6490412806) **DanielRosenwasser** clarified using the stack as temporary storage and allocating precise size afterwards

### [PR microsoft/TypeScript#64997](https://github.com/microsoft/TypeScript/pull/64997) (Open, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Scanner simd**

*Enable default SIMD scanning and introduce a CI worker to benchmark non-SIMD code performance uplift.*

 * created by **weswigham**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **weswigham**
 * [today](https://github.com/microsoft/TypeScript/pull/64997#issuecomment-6477088521) **weswigham** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/64997#issuecomment-6477090058) **typescript-automation[bot]** said "Hey @weswigham, this PR is in an unmergable state, so is missing a merge commit to run against; please resolve conflicts and try again."
 * [today](https://github.com/microsoft/TypeScript/pull/64997#issuecomment-6477415372) **weswigham** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/64997#issuecomment-6477426560) **typescript-automation[bot]** reported CI jobs started and provided links to status and results
 * [today](https://github.com/microsoft/TypeScript/pull/64997#issuecomment-6478482703) **typescript-automation[bot]** provided the requested perf run comparison report
 * [today](https://github.com/microsoft/TypeScript/pull/64997#issuecomment-6479572850) **weswigham** expressed uncertainty about which helpers are invoked in large-scale performance checks and noted that microbenchmark optimizations did not regress overall performance
 * **weswigham** added label `Domain: Performance`

### [Issue microsoft/TypeScript#64998](https://github.com/microsoft/TypeScript/issues/64998) (Open)

**declaration emit depends on checker assignment; a type alias becomes \`any\` with no error**

*When using multiple checkers, TypeScript's declaration emit nondeterministically infers a type alias as any in .d.ts files.*

 * created by **blickly**

### [Issue microsoft/TypeScript#64999](https://github.com/microsoft/TypeScript/issues/64999) (Open)

**Top\-level await reparse keeps statements it already consumed when it reaches the end of the file**

*TypeScript's top-level await reparse retains already consumed statements at file end, causing overlapping parse nodes.*

 * created by **roninjin10**

### [Issue microsoft/TypeScript#65000](https://github.com/microsoft/TypeScript/issues/65000) (Open)

**Format Document is not idempotent when a line break moves a token that enclosing nodes start at**

*TypeScript's document formatter isn't idempotent when line breaks shift tokens of enclosing nodes, causing extra indentation on reformat.*

 * created by **roninjin10**

### [PR microsoft/TypeScript#65001](https://github.com/microsoft/TypeScript/pull/65001) (Open, `Author: Team`, `For Uncommitted Bug`, `dependencies`, `javascript`)

**Bump qs from 6\.16\.0 to 6\.17\.1**

*Upgrade qs from 6.16.0 to 6.17.1 to incorporate bug fixes and improvements.*

 * created by **dependabot[bot]**
 * (today) **dependabot[bot]** added labels `dependencies`, `javascript`
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/65001#issuecomment-6481703030) **jakebailey** said "Well, see you in a week"

### [PR microsoft/TypeScript#65002](https://github.com/microsoft/TypeScript/pull/65002) (Open, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Formatter perf improvements**

*Enhances the TypeScript formatting scanner with reduced allocations and SIMD optimizations, achieving about 30% speedup.*

 * created by **weswigham**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`, and assigned to **weswigham**

### [PR microsoft/TypeScript#65003](https://github.com/microsoft/TypeScript/pull/65003) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Report process CPU time in extended diagnostics**

*Add reporting of process CPU time in extended diagnostics to capture actual CPU usage by the process.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/65003#issuecomment-6482540229) **jakebailey** asked the typescript-bot to run performance tests faster
 * [today](https://github.com/microsoft/TypeScript/pull/65003#issuecomment-6482542217) **typescript-automation[bot]** reported that performance test jobs had started and provided links to the build and results
 * [today](https://github.com/microsoft/TypeScript/pull/65003#issuecomment-6482549212) **jakebailey** asked the TypeScript bot to run performance tests faster and suggested running it twice for comparison
 * [today](https://github.com/microsoft/TypeScript/pull/65003#issuecomment-6482550959) **typescript-automation[bot]** reported that performance tests started and provided links to build and results
 * [today](https://github.com/microsoft/TypeScript/pull/65003#issuecomment-6483489524) **typescript-automation[bot]** reported the requested perf run results including a detailed comparison table
 * [today](https://github.com/microsoft/TypeScript/pull/65003#issuecomment-6483634710) **typescript-automation[bot]** provided the requested performance run results
 * [today](https://github.com/microsoft/TypeScript/pull/65003#issuecomment-6483652625) **jakebailey** said "Hm, benchmarker does not understand this"

### [PR microsoft/TypeScript#65004](https://github.com/microsoft/TypeScript/pull/65004) (Open, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Allow builds to skip source generation**

*Add a build flag to skip source generation and shorten the benchmark preparation phase.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#65005](https://github.com/microsoft/TypeScript/pull/65005) (Closed, `For Backlog Bug`)

**Report an error for class declarations in statement position**

*The compiler now emits TS1156 for class declarations used directly as if, loop, or labeled statement bodies.*

 * created by **TimonGaertner**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/65005#issuecomment-6486321253) **TimonGaertner** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript/pull/65005#issuecomment-6489373507) **RyanCavanaugh** said "@TimonGaertner this is an unusually good test, what model and reasoning effort were you using?"
 * (later) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#65006](https://github.com/microsoft/TypeScript/pull/65006) (Closed, `Author: Team`, `For Uncommitted Bug`, **RyanCavanaugh**)

**Fix hang in signature help due to loop in findPrecedingMatchingToken**

*Signature help hangs during LSP performance tests when findPrecedingMatchingToken loops infinitely without automatic parenthesis insertion.*

 * created by **RyanCavanaugh**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **RyanCavanaugh**
 * (today) **RyanCavanaugh** closed the issue

