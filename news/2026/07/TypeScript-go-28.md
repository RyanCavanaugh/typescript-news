# Report for 2026-07-28 (Tuesday, July 28th, 2026)

20 different users commented on 53 different issues.

## Recommended Actions

 * Response Recommended
    * @remcohaszing asked if there are instances where a single non-TS file maps into multiple distinct files in [microsoft/TypeScript-go#2824](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-5108341014)
    * @Princesseuh provided important information about Astro's script tag behavior and its impact in [microsoft/TypeScript-go#2824](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-5108638364)
    * @dkamins provided repro steps and summary table in [microsoft/TypeScript-go#4365](https://github.com/microsoft/TypeScript-go/pull/4365#issuecomment-5111400237)
    * @swotvibe asked whether the moved-files list was derived from oldToNew tracking or required a separate pass in [microsoft/TypeScript-go#4610](https://github.com/microsoft/TypeScript-go/issues/4610#issuecomment-5118640325)
    * @remcohaszing asked about how emit should work with mapped files and suggested handling strategies in [microsoft/TypeScript-go#4712](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5109758000)
    * @valentinmelusson provided important fix details and regression tests in [microsoft/TypeScript-go#4758](https://github.com/microsoft/TypeScript-go/issues/4758#issuecomment-5118037769)
    * @ljharb asked for clarification on whether the change is a regression in JS in [microsoft/TypeScript-go#4768](https://github.com/microsoft/TypeScript-go/issues/4768#issuecomment-5114355431)
    * @KiYugadgeter asked whether the issue duplicates #4669 in [microsoft/TypeScript-go#4780](https://github.com/microsoft/TypeScript-go/issues/4780#issuecomment-5109228171)
    * @KiYugadgeter reported that the server did not respond to hover requests in [microsoft/TypeScript-go#4780](https://github.com/microsoft/TypeScript-go/issues/4780#issuecomment-5111450281)
    * @typescript-automation[bot] provided perf run results as requested in [microsoft/TypeScript-go#4781](https://github.com/microsoft/TypeScript-go/pull/4781#issuecomment-5110063340)
    * @typescript-automation[bot] provided test results confirming everything looks good in [microsoft/TypeScript-go#4781](https://github.com/microsoft/TypeScript-go/pull/4781#issuecomment-5110441698)
    * @typescript-automation[bot] provided requested performance results in [microsoft/TypeScript-go#4781](https://github.com/microsoft/TypeScript-go/pull/4781#issuecomment-5120141943)
    * @typescript-automation provided test results comparing main and pull request in [microsoft/TypeScript-go#4785](https://github.com/microsoft/TypeScript-go/pull/4785#issuecomment-5119967692)

## Activity Summary

### [Issue microsoft/TypeScript-go#2824](https://github.com/microsoft/TypeScript-go/issues/2824) (Open, `Domain: API and Extensibility`, **andrewbranch**)

**API usage patterns for complex editor extensions**

*Exploring IPC-based API features for a Go TS server to replace TS Server plugins and support Vue editor extensions*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-5096586511) **DanielRosenwasser** said "Question for API integrators - are there any instances today where a single non-TS file actually maps into multiple distinct files?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-5103502275) **padcom** described how .vue single-file components map into multiple generated files
 * [today](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-5103707400) **pikax** explained that file mapping depends on integration, noted that vue can split a SFC into multiple files or as one with adjustments, questioned who should handle the <i18n> block, and described an unrelated test-file use case about SFC imports requiring different mapper options
 * [today](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-5108341014) **remcohaszing** asked whether any instances exist where a single non-TS file maps into multiple distinct files and noted that Volar supports this via the language server but not the TS plugin, mentioning HTML module scripts as an example and suggesting module declarations
 * [today](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-5108638364) **Princesseuh** clarified that Astro supports script tags of multiple languages within a file, works like HTML, and noted it was a blocker
 * [today](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-5109564324) **DanielRosenwasser** asked if resources or examples were available for multiple TS/JS blocks in an Astro file and what an importer received when handling them

### [PR microsoft/TypeScript-go#4239](https://github.com/microsoft/TypeScript-go/pull/4239) (Closed, `No linked issue`)

**Replace ForEachReturnStatement closure with direct kind\-switched walk**

*Replace ForEachReturnStatement closure with a direct kind-switched recursive function to reduce allocations and improve performance.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4239#issuecomment-4906526669) **DanielRosenwasser** said "This would still save the closure allocation and visit fewer child nodes, right?"
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4239#issuecomment-4906575654) **jakebailey** said "No, this should get stack allocated"
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4239#issuecomment-5097903321) **jakebailey** reevaluated the refactor as not worth it and suggested adding a canContainReturnStatement function to skip nodes that can't contain return statements
 * (later) **mds-ant** closed the issue

### [PR microsoft/TypeScript-go#4365](https://github.com/microsoft/TypeScript-go/pull/4365) (Open, **jakebailey**, **Copilot**)

**Preserve typedef comments in declaration emit**

*Preserve descriptive JSDoc comments on typedefs and callbacks in emitted declaration files while preventing duplicate comment output*

 * created by **Copilot**
 * (5 weeks ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4365#issuecomment-5111400237) **dkamins** confirmed the PR output matched expectations and provided a summary table of JSDoc typedef behaviors with a repro archive

### [PR microsoft/TypeScript-go#4584](https://github.com/microsoft/TypeScript-go/pull/4584) (Closed)

**binder: fix stack overflow in CFA when for\-loop initializer is unreachable**

*Prevent stack overflow in control-flow analysis when a for-loop initializer is unreachable by bailing out early to avoid cyclic CFGs.*

 * created by **ibesuperv**
 * (later) **ibesuperv** closed the issue

### [Issue microsoft/TypeScript-go#4589](https://github.com/microsoft/TypeScript-go/issues/4589) (Closed, `Domain: Editor`, `Needs Investigation`, **johnfav03**)

**workspace/diagnostic/refresh is triggered for watch events that cannot affect type checking**

*The VS Code TypeScript language server erroneously triggers diagnostic refreshes for unrelated .svg file changes in node_modules.*

 * (1 week ago) **RyanCavanaugh** added label `Needs Investigation`, and set milestone to `Post-7.0`
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/4589#issuecomment-5030035555) **ibesuperv** investigated the root cause of CPU spikes during noisy filesystem activity, identified that Session.DidChangeWatchedFiles unconditionally triggered diagnostics refresh for all file events, reproduced the issue, and contrasted PR #4604’s extension-based filter with PR #4637’s content-hash comparison
 * (today) **johnfav03** closed the issue

### [PR microsoft/TypeScript-go#4604](https://github.com/microsoft/TypeScript-go/pull/4604) (Closed)

**fix: prevent unnecessary diagnostic refreshes on irrelevant watch events \(\#4589\)**

*Optimize file watch handling by scheduling diagnostics refresh only for relevant TypeScript files and directories, reducing CPU and RPC overhead.*

 * created by **ibesuperv**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4604#issuecomment-5098994242) **ibesuperv** said "@johnfav03 Applied, thanks for the catch!"
 * (today) **johnfav03** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/4604#issuecomment-5107369635) **ibesuperv** thanked @johnfav03 for the review and merge and said they learned a lot
 * [today](https://github.com/microsoft/TypeScript-go/pull/4604#issuecomment-5107449407) **johnfav03** said "Thanks, it was good working with you too! Glad the review was helpful, I learned a lot from your work as well"

### [Issue microsoft/TypeScript-go#4610](https://github.com/microsoft/TypeScript-go/issues/4610) (Closed, `Domain: Editor`, `Needs Investigation`, **johnfav03**)

**Renaming a file can be very slow in some edge cases**

*VSCode tsgo file renames can be slow because a third-party .d.ts with repeated imports triggers quadratic path-updater scans.*

 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/4610#issuecomment-5077957506) **swotvibe** asked whether the issue was still open for someone else to pick up and whether memoizing computed import specifiers would resolve the repeated-computation performance issue
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/4610#issuecomment-5094530293) **johnfav03** explained that he implemented a fix precomputing the moved-files set once per rename to optimize unresolved import scanning and described why this approach was chosen based on resolutionMode differences
 * (yesterday) **johnfav03** closed the issue
 * [later](https://github.com/microsoft/TypeScript-go/issues/4610#issuecomment-5118640325) **swotvibe** explained that resolutionMode can differ between import syntaxes and advocated precomputing the moved-files list for renaming; asked if the moved-files list was derived from oldToNew tracking or required a separate pass

### [PR microsoft/TypeScript-go#4661](https://github.com/microsoft/TypeScript-go/pull/4661) (Open)

**Fall back to inotify when filesystem has errors in fanotify \(fix watch in Docker\)**

*Automatically switch to inotify backend when fanotify fails on Docker filesystems to detect file changes.*

 * created by **johnfav03**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4661#issuecomment-5107156400) **jakebailey** said "I think this approach is probably okay, though I do wonder if the fanotify watch backend should just internally fall back to inotify..."

### [PR microsoft/TypeScript-go#4667](https://github.com/microsoft/TypeScript-go/pull/4667) (Closed, **RyanCavanaugh**, **Copilot**)

**Copilot test PR, do not merge**

*Change 'are subject' to 'is subject' for correct singular subject-verb agreement with 'any use'.*

 * **Copilot** assigned to **RyanCavanaugh**
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4667#issuecomment-5005824257) **sandersn** said "@copilot Make an additional correction"
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4667#issuecomment-5005854778) **Copilot** fixed plural possessive in README.md trademarks section
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#4690](https://github.com/microsoft/TypeScript-go/pull/4690) (Closed, `dependencies`, `javascript`)

**Bump brace\-expansion from 5\.0\.6 to 5\.0\.7**

*The brace-expansion dependency is updated from version 5.0.6 to 5.0.7.*

 * (1 week ago) **dependabot[bot]** added labels `javascript`, `dependencies`, `javascript`
 * [today](https://github.com/microsoft/TypeScript-go/pull/4690#issuecomment-5108255982) **dependabot[bot]** said "Superseded by #4777."
 * (today) **dependabot[bot]** closed the issue

### [Issue microsoft/TypeScript-go#4706](https://github.com/microsoft/TypeScript-go/issues/4706) (Open, `bug`, **jakebailey**)

**wasip1: LSP over node:wasi hangs after \`initialize\` — signal watcher starves the scheduler \(fix included\)**

*The wasip1-built LSP server on Node WASI hangs after initialize because its signal-watcher busy-spins; skipping signal.NotifyContext on wasip1 fixes this.*

 * created by **calvinrp**
 * [6 days ago](https://github.com/microsoft/TypeScript-go/issues/4706#issuecomment-5048976529) **jakebailey** said "By all means, send a PR with this change; I definitely have similar changes locally"
 * (today) **RyanCavanaugh** added label `bug`, set milestone to `TypeScript 7.1`, and assigned to **jakebailey**

### [Issue microsoft/TypeScript-go#4709](https://github.com/microsoft/TypeScript-go/issues/4709) (Open, `bug`, **weswigham**)

**\`javascript\.validation\.enabled\` editor setting controls typescript validation as well**

*Disabling JavaScript validation also disables TypeScript validation unintentionally due to unified configuration handling.*

 * created by **weswigham**
 * [6 days ago](https://github.com/microsoft/TypeScript-go/issues/4709#issuecomment-5051455317) **jakebailey** said "Yeah, so the fix here is going to be to start doing language-scoped settings, but I think we could probably special case just this one thing?"
 * [6 days ago](https://github.com/microsoft/TypeScript-go/issues/4709#issuecomment-5051660283) **weswigham** said "IMO, this and format.enabled are the big "wait, why do these toggle unexpected file extensions, too"."
 * (today) **RyanCavanaugh** added label `bug`, set milestone to `Post-7.0`, and assigned to **weswigham**

### [PR microsoft/TypeScript-go#4710](https://github.com/microsoft/TypeScript-go/pull/4710) (Closed)

**Add an LSP init flag that enables flaky diagnostics tracking**

*Add a trackFlakyDiagnostics LSP init flag and matching JS/TS server option to log or panic on intermittent diagnostic inconsistencies.*

 * created by **weswigham**
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript-go#4711](https://github.com/microsoft/TypeScript-go/pull/4711) (Closed)

**Optimize \`getAssignmentReducedType\` in CFA**

*Optimize getAssignmentReducedType to eliminate quadratic performance when processing large union types in control flow analysis.*

 * [6 days ago](https://github.com/microsoft/TypeScript-go/pull/4711#issuecomment-5053241532) **ahejlsberg** said "Nice win in compiler-unions test, which does indeed contain a number of large unions that are reduced by other large unions in CFA."
 * [6 days ago](https://github.com/microsoft/TypeScript-go/pull/4711#issuecomment-5053422688) **typescript-automation[bot]** reported results of running the top 400 repos with tsc and found everything looked good
 * (5 days ago) **ahejlsberg** closed the issue
 * [later](https://github.com/microsoft/TypeScript-go/pull/4711#issuecomment-5119861650) **ahejlsberg** said "@typescript-bot perf test this faster"
 * [later](https://github.com/microsoft/TypeScript-go/pull/4711#issuecomment-5119862426) **typescript-automation[bot]** started a performance test job and posted an initial build status table

### [PR microsoft/TypeScript-go#4712](https://github.com/microsoft/TypeScript-go/pull/4712) (Open)

**Content mappers**

*Add support for external content mapper packages in TypeScript configuration to transform unsupported file types into valid TypeScript syntax.*

 * [4 days ago](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5076887616) **andrewbranch** provided an update before vacation and asked for feedback from implementers on the SpanMapPurpose classification
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5078512064) **mikearnaldi** explained that patch 0002 was incomplete, described mapping ambiguity at span boundaries requiring left/right affinity, and noted that his patch enabled completions at file end but might not be correct
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5086629187) **jasonlyu123** inquired whether the LSP-connected IPC API parameters should use generated or source positions and if purely generated positions could be requested
 * [today](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5109758000) **remcohaszing** praised the PR's start and offered feedback on content-mapped file emission, suggesting handling for MDX and declaration maps, questioning how emit should work with mapped files, and noting SpanMapping length differences and potential Volar compatibility issues

### [Issue microsoft/TypeScript-go#4713](https://github.com/microsoft/TypeScript-go/issues/4713) (Open, `Needs Investigation`, **johnfav03**)

**tsconfig/jsconfig diagnostic doesn't refresh after file saved**

*tsgo fails to refresh tsconfig/jsconfig diagnostics after saving compilerOptions changes.*

 * created by **sharpchen**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `Post-7.0`, and assigned to **johnfav03**

### [Issue microsoft/TypeScript-go#4715](https://github.com/microsoft/TypeScript-go/issues/4715) (Open, **jakebailey**)

**Request for support for Android**

*Enable straightforward installation and execution of the TypeScript compiler via npm in Android Termux without extra workarounds*

 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/4715#issuecomment-5062606171) **thunder-coding** noted that the build pipeline is defined in Herebyfile.mjs, suggested adding the missing platform configuration and implementing a source-built-binary fallback similar to sharp
 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/4715#issuecomment-5062840275) **jakebailey** said "There's basically no way we're going to ship the entire repo in the package."
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/4715#issuecomment-5068954049) **thunder-coding** suggested packaging the repo separately or adding package.json scripts to download and build from the git tarball via gitHead
 * **RyanCavanaugh** added to milestone `Possible Improvement`

### [Issue microsoft/TypeScript-go#4718](https://github.com/microsoft/TypeScript-go/issues/4718) (Closed)

**Panic at startup and mass module\-resolution failures under PRoot link2symlink \(Termux proot\-distro on Android\)**

*TypeScript 7's compiler fails with panic and module-resolution errors under Termux PRoot link2symlink due to broken path handling*

 * created by **dlecan**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4718#issuecomment-5108209676) **RyanCavanaugh** said "Closing for now per discussion in the PR"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#4719](https://github.com/microsoft/TypeScript-go/issues/4719) (Closed, **jakebailey**, **Copilot**)

**tsgo reports type errors in external\-library \(node\_modules\) source files that tsc suppresses**

*tsgo reports type errors in .ts and .tsx files within external dependencies despite skipLibCheck, while tsc suppresses them.*

 * (5 days ago) **jakebailey** assigned to **Copilot**, **jakebailey**
 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/4719#issuecomment-5063509787) **jakebailey** pointed out that non-declaration files from node_modules seemed incorrect and suggested the error was a new ordering issue unrelated to node_modules
 * [today](https://github.com/microsoft/TypeScript-go/issues/4719#issuecomment-5108339358) **RyanCavanaugh** said "This package is pretty messed up in terms of typings. It should not be exposing .ts files from package.json https://arethetypeswrong.github.io/?p=%40ladle%2Freact%405.1.1"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#4720](https://github.com/microsoft/TypeScript-go/issues/4720) (Open, `Needs Investigation`, **andrewbranch**)

**Auto import suggestions break with circular workspace dependencies**

*Auto-import suggestions in tsgo fail for relative imports within workspaces involved in a circular dependency chain.*

 * created by **iansan5653**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `Post-7.0`, and assigned to **andrewbranch**

### [Issue microsoft/TypeScript-go#4722](https://github.com/microsoft/TypeScript-go/issues/4722) (Open, `bug`, **jakebailey**, **Copilot**)

**Nested nullish coalescing \+ comment \+ ES2018 causes function body to be ignored**

*Transpiling nested nullish coalescing with comments targeting ES2018 misplaces the return statement causing function body to be ignored*

 * created by **kamsar**
 * (5 days ago) **jakebailey** assigned to **Copilot**, **jakebailey**
 * (today) **RyanCavanaugh** added label `bug`, and set milestone to `TypeScript 7.1`

### [Issue microsoft/TypeScript-go#4738](https://github.com/microsoft/TypeScript-go/issues/4738) (Open, **johnfav03**)

**\[ServerErrors\]\[TypeScript\] main vs **

*TypeScript's main pipeline analyzed 300 popular repos, succeeded on 199, found six interesting changes, and experienced timeouts and clone failures.*

 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/4738#issuecomment-5075535700) **typescript-automation[bot]** reported a server connection closed prematurely error and provided affected repo, error details, last requests, and repro steps
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/4738#issuecomment-5075535744) **typescript-automation[bot]** reported that the server connection closed prematurely for nuxt/nuxt and provided logs and repro steps
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/4738#issuecomment-5075535782) **typescript-automation[bot]** reported a server connection closed prematurely error and provided affected repository details, logs, and repro steps
 * (today) **RyanCavanaugh** set milestone to `Post-7.0`, and assigned to **johnfav03**

### [Issue microsoft/TypeScript-go#4748](https://github.com/microsoft/TypeScript-go/issues/4748) (Open, `Needs More Info`)

**Panic: nil pointer in NodeList\.HasTrailingComma during incremental rebuild \(build\-mode declaration printer\) — 7\.0\.2 and current nightly**

*A nil pointer dereference in NodeList.HasTrailingComma triggers a panic during incremental build-mode declaration printing in TypeScript.*

 * created by **nikeedw**
 * (today) **RyanCavanaugh** added label `Needs More Info`, and set milestone to `Need More Info`

### [Issue microsoft/TypeScript-go#4752](https://github.com/microsoft/TypeScript-go/issues/4752) (Open, `Crash`, **jakebailey**, **Copilot**)

**\`tsconfig\.json\`: \`{"" }\` causes a panic, and more TS errors than v6**

*An empty tsconfig.json literal {} crashes the compiler with a 'negative Repeat count' panic and produces more errors than TypeScript v6.*

 * **abrahamguo** added label `Crash`
 * (yesterday) **jakebailey** assigned to **Copilot**, **jakebailey**
 * **RyanCavanaugh** added to milestone `TypeScript 7.1`

### [Issue microsoft/TypeScript-go#4758](https://github.com/microsoft/TypeScript-go/issues/4758) (Closed)

**disableSourceOfProjectReferenceRedirect causes lodash per\-method submodule import to resolve to the wrong function**

*Enabling disableSourceOfProjectReferenceRedirect in a referenced TypeScript project causes lodash/get imports to resolve as lodash/set under tsgo.*

 * created by **valentinmelusson**
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/4758#issuecomment-5095511022) **jakebailey** requested OS and package manager details, tsconfig configurations, and diagnostic outputs to reproduce the issue
 * [today](https://github.com/microsoft/TypeScript-go/issues/4758#issuecomment-5101846289) **valentinmelusson** provided OS and package manager details, shared tsconfig.json configurations, and reported errors persisted across local and CI environments
 * [today](https://github.com/microsoft/TypeScript-go/issues/4758#issuecomment-5106800705) **jakebailey** questioned whether the user was testing the prototype PR as Yarn PnP isn't supported, and noted the package ID issue resembled a bug he found and required a better repro
 * [today](https://github.com/microsoft/TypeScript-go/issues/4758#issuecomment-5107123401) **jakebailey** said "Are you running an old version? I think this was fixed in #4008. Are you running an old build for PnP or something?"
 * [later](https://github.com/microsoft/TypeScript-go/issues/4758#issuecomment-5114848844) **valentinmelusson** explained they were testing the prototype PR in their Datadog frontend repo, noted everything else worked and they were investigating whether the error was on their side, and confirmed their binary included commits through July 15
 * [later](https://github.com/microsoft/TypeScript-go/issues/4758#issuecomment-5118037769) **valentinmelusson** described finding the root cause in Yarn PnP integration and implementing a fix with regression tests

### [PR microsoft/TypeScript-go#4764](https://github.com/microsoft/TypeScript-go/pull/4764) (Closed)

**Remove unused classifiable name tracking**

*Removes unused classifiable name tracking to improve binder performance and reduce memory usage by up to 5%.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4764#issuecomment-5106666060) **jakebailey** said "Main changed and caused a semantic merge conflict, so this needs a reapproval"
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4768](https://github.com/microsoft/TypeScript-go/issues/4768) (Closed)

**TS7023 false positive: contextual return type ignored when a recursive call is assigned to a union\-annotated local**

*TypeScript incorrectly reports TS7023 on a contextually typed recursive function when assigning its call to a union-typed variable.*

 * **RyanCavanaugh** removed label `Needs More Info`
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/4768#issuecomment-5098140502) **RyanCavanaugh** noted that CHANGES.md already describes JSDoc support as being more based on TS and that changes aligning with TS behavior need no additional justification unless there's a strong positive case
 * (yesterday) **RyanCavanaugh** closed the issue
 * [later](https://github.com/microsoft/TypeScript-go/issues/4768#issuecomment-5114355431) **ljharb** expressed confusion about the behavior change across TypeScript versions and suggested that failing in JS constitutes a regression

### [PR microsoft/TypeScript-go#4772](https://github.com/microsoft/TypeScript-go/pull/4772) (Closed, **RyanCavanaugh**, **Copilot**)

**Select "types returned by" vs "types of" from the merged dotted name in relation errors**

*Fix error message condensation in tsgo to match tsc by selecting “types returned by” or “types of” based on the merged dotted name suffix*

 * created by **Copilot**
 * (yesterday) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#4773](https://github.com/microsoft/TypeScript-go/issues/4773) (Closed)

**Consumer\-side TS2595 for a dependency \`\.d\.ts\` that mixes \`export =\` with named exports and suppresses its own TS2309**

*tsgo falsely reports TS2595 on consumer imports from a dependency whose .d.ts file mixes export= with named exports, unlike tsc.*

 * created by **Togetic**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4773#issuecomment-5103648348) **Togetic** noted that consola@3.4.2 has a separate issue and that dependencies suppressing their own TS2309 errors leave consumers with unsuppressable errors
 * [today](https://github.com/microsoft/TypeScript-go/issues/4773#issuecomment-5109330430) **RyanCavanaugh** said "This is fully the same as #2781 - mixing named imports and export =, which is not supported."
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#4774](https://github.com/microsoft/TypeScript-go/issues/4774) (Open)

**Document that \`@typescript/typescript6\` ships the API under \`@typescript/old\` \(path\-based tooling\)**

*Document that the TypeScript 6 API from @typescript/typescript6 resides under @typescript/old and requires updating path-based tooling ignores accordingly.*

 * created by **Akshay090**
 * **RyanCavanaugh** added to milestone `Possible Improvement`

### [PR microsoft/TypeScript-go#4775](https://github.com/microsoft/TypeScript-go/pull/4775) (Closed)

**Retain uninitialized binding patterns for variable declarations in declaration emit**

*Retain uninitialized binding patterns in declaration emit to support exporting binding patterns as isolatedDeclarations.*

 * created by **weswigham**
 * **weswigham** added to milestone `TypeScript 7.1`

### [PR microsoft/TypeScript-go#4776](https://github.com/microsoft/TypeScript-go/pull/4776) (Closed)

**Remove easily\-removable wasted work in parse/bind**

*Eliminate redundant ASCII scans in parse/bind by leveraging existing line mapping, yielding around 2.5% faster parsing.*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#4777](https://github.com/microsoft/TypeScript-go/pull/4777) (Open, `dependencies`, `javascript`)

**Bump brace\-expansion from 5\.0\.6 to 5\.0\.8**

*Upgrade brace-expansion dependency from version 5.0.6 to 5.0.8.*

 * created by **dependabot[bot]**
 * (today) **dependabot[bot]** added labels `dependencies`, `javascript`, `dependencies`, `javascript`

### [PR microsoft/TypeScript-go#4778](https://github.com/microsoft/TypeScript-go/pull/4778) (Closed)

**Fix "Not a subspan" crash in signature help on error\-recovered JSX**

*Improper scanning of a closing tag after an incomplete JSX attribute causes a 'Not a subspan' crash in signature help.*

 * created by **johnfav03**

### [PR microsoft/TypeScript-go#4779](https://github.com/microsoft/TypeScript-go/pull/4779) (Open)

**Fix incremental builder re\-emitting entire import closure on non\-shape\-changing edits**

*Incremental builder computes real .d.ts signatures on fresh builds to avoid re-emitting full import closures on non-shape-changing edits.*

 * created by **johnfav03**

### [Issue microsoft/TypeScript-go#4780](https://github.com/microsoft/TypeScript-go/issues/4780) (Closed, `Needs More Info`)

**textDocument/hover doesn't work on TypeScript 7\.0\.2**

*textDocument/hover requests in TypeScript 7.0.2 LSP produce no responses when used with vim-lsp.*

 * created by **KiYugadgeter**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4780#issuecomment-5109228171) **KiYugadgeter** said "Probably This is duplication of #4669?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/4780#issuecomment-5109524201) **RyanCavanaugh** requested a concrete LSP command sequence and noted no crash was visible in the provided log
 * (today) **RyanCavanaugh** added label `Needs More Info`, and set milestone to `Need More Info`
 * [today](https://github.com/microsoft/TypeScript-go/issues/4780#issuecomment-5111450281) **KiYugadgeter** said "It looks like the server do not response to hover request"

### [PR microsoft/TypeScript-go#4781](https://github.com/microsoft/TypeScript-go/pull/4781) (Open)

**Optimize \`narrowTypeByEquality\` and \`narrowTypeBySwitchOnDiscriminant\`**

*Improve performance of control flow analysis by optimizing narrowTypeByEquality and narrowTypeBySwitchOnDiscriminant functions.*

 * created by **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4781#issuecomment-5109864825) **ahejlsberg** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4781#issuecomment-5109865459) **typescript-automation[bot]** reported statuses and result links for CI jobs test top400 and perf test this faster
 * [today](https://github.com/microsoft/TypeScript-go/pull/4781#issuecomment-5110063340) **typescript-automation[bot]** reported the requested performance run results including errors, symbols, types, memory usage, and memory allocations
 * [today](https://github.com/microsoft/TypeScript-go/pull/4781#issuecomment-5110441698) **typescript-automation[bot]** reported test results for the top 400 repos with tsc on main versus the pull request merge and found everything looked good
 * [later](https://github.com/microsoft/TypeScript-go/pull/4781#issuecomment-5119829958) **ahejlsberg** said "@typescript-bot perf test this faster"
 * [later](https://github.com/microsoft/TypeScript-go/pull/4781#issuecomment-5119830782) **typescript-automation[bot]** reported CI build start status with links to build and result details
 * [later](https://github.com/microsoft/TypeScript-go/pull/4781#issuecomment-5120141943) **typescript-automation[bot]** provided the requested performance run results

### [Issue microsoft/TypeScript-go#4782](https://github.com/microsoft/TypeScript-go/issues/4782) (Closed, `Domain: Editor`, **iisaduan**)

**Bug: Rename trigger span is off by one column in module specifiers**

*Rename spans for module specifiers in non-VSCode LSP editors are shifted one column too far left.*

 * created by **lixiaoyan**

### [PR microsoft/TypeScript-go#4783](https://github.com/microsoft/TypeScript-go/pull/4783) (Closed)

**Fix module specifier rename trigger spans**

*Remove leading trivia from module-specifier rename trigger spans to correct their offset during prepareRename*

 * created by **lixiaoyan**
 * [later](https://github.com/microsoft/TypeScript-go/pull/4783#issuecomment-5115116377) **lixiaoyan** said "@microsoft-github-policy-service agree"

### [PR microsoft/TypeScript-go#4784](https://github.com/microsoft/TypeScript-go/pull/4784) (Open)

**Build checker cache keys in an inline buffer with one\-shot hashing**

*Use a small inline buffer and one-shot xxh3 hashing in the checker cache key builder to reduce overhead.*

 * created by **mds-ant**
 * [later](https://github.com/microsoft/TypeScript-go/pull/4784#issuecomment-5119106834) **jakebailey** complained that Claude was addicted to introducing one-off test files and requested a perf test from the TypeScript bot
 * [later](https://github.com/microsoft/TypeScript-go/pull/4784#issuecomment-5119107775) **typescript-automation[bot]** reported the start of performance tests with links to build and results
 * [later](https://github.com/microsoft/TypeScript-go/pull/4784#issuecomment-5119135843) **mds-ant** explained that they asked Claude to add a test ensuring the resulting hash remained identical and offered to remove it if unnecessary
 * [later](https://github.com/microsoft/TypeScript-go/pull/4784#issuecomment-5119247572) **jakebailey** mentioned uncertainty about maintenance cost, said he would review the test file, and noted that key builder logic might become obsolete in a future Go release
 * [later](https://github.com/microsoft/TypeScript-go/pull/4784#issuecomment-5120023481) **jakebailey** said "Mainly, we already have checker_test.go. It just really loves adding new files"
 * [later](https://github.com/microsoft/TypeScript-go/pull/4784#issuecomment-5120254247) **typescript-automation[bot]** posted the requested performance run results with detailed comparison metrics

### [PR microsoft/TypeScript-go#4785](https://github.com/microsoft/TypeScript-go/pull/4785) (Closed)

**Skip the speculative expression parse in the async arrow lookahead**

*Replace speculative parsing with a token check for unparenthesized async arrows, improving parse speed and reducing memory usage.*

 * created by **mds-ant**
 * [later](https://github.com/microsoft/TypeScript-go/pull/4785#issuecomment-5119018357) **jakebailey** said "@typescript-bot test it"
 * [later](https://github.com/microsoft/TypeScript-go/pull/4785#issuecomment-5119019262) **typescript-automation[bot]** published automated CI build status for tests
 * [later](https://github.com/microsoft/TypeScript-go/pull/4785#issuecomment-5119376540) **typescript-automation[bot]** posted the requested performance run results in a detailed comparison report
 * [later](https://github.com/microsoft/TypeScript-go/pull/4785#issuecomment-5119967692) **typescript-automation[bot]** provided test results comparing main and pull request showing everything looked good

### [PR microsoft/TypeScript-go#4786](https://github.com/microsoft/TypeScript-go/pull/4786) (Open)

**Shrink \`ast\.Symbol\` from 96 to 80 bytes**

*Move unused ast.Symbol fields into a lazily allocated extra struct to shrink symbol size and reduce memory usage.*

 * created by **mds-ant**
 * [later](https://github.com/microsoft/TypeScript-go/pull/4786#issuecomment-5118975538) **jakebailey** said "@typescript-bot perf test this"
 * [later](https://github.com/microsoft/TypeScript-go/pull/4786#issuecomment-5118976636) **typescript-automation[bot]** started build jobs and posted links to status and results
 * [later](https://github.com/microsoft/TypeScript-go/pull/4786#issuecomment-5119351637) **typescript-automation[bot]** provided the performance run results requested by @jakebailey

### [PR microsoft/TypeScript-go#4787](https://github.com/microsoft/TypeScript-go/pull/4787) (Closed)

**Check the arrow\-function line\-terminator rule without the line map**

*Modify arrow-function line-terminator checks to scan preceding trivia rather than building the complete line map, reducing memory overhead.*

 * created by **mds-ant**

### [PR microsoft/TypeScript-go#4788](https://github.com/microsoft/TypeScript-go/pull/4788) (Closed)

**Embed zero\-size marker bases first in generated AST structs**

*Embed zero-size marker bases first in generated Go AST structs to eliminate trailing padding and reduce overall struct size.*

 * created by **mds-ant**
 * [later](https://github.com/microsoft/TypeScript-go/pull/4788#issuecomment-5119071906) **jakebailey** said "@typescript-bot perf test this"
 * [later](https://github.com/microsoft/TypeScript-go/pull/4788#issuecomment-5119072868) **typescript-automation[bot]** noted that performance test build jobs had started and would update with results
 * [later](https://github.com/microsoft/TypeScript-go/pull/4788#issuecomment-5119513682) **typescript-automation[bot]** posted the results of the requested performance run
 * (later) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4789](https://github.com/microsoft/TypeScript-go/issues/4789) (Closed)

**Parser should reject import\.defer?\.\('x'\) optional invocation**

*TypeScript incorrectly permits optional invocation of import.defer (‘import.defer?.(…)’) despite other parsers rejecting it.*

 * created by **BhariGowda**
 * [later](https://github.com/microsoft/TypeScript-go/issues/4789#issuecomment-5119968242) **jakebailey** said "We do not need duplicate issues filed here; the tracking issue linked above is just fine"
 * (later) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4790](https://github.com/microsoft/TypeScript-go/pull/4790) (Open)

**Skip stale overlay paths in markProjectsAffectedByConfigChanges**

*markProjectsAffectedByConfigChanges panics when stale overlay paths in affectedFiles cause nil pointer dereference*

 * created by **blixt**

