# Report for 2026-08-14 (Friday, August 14th, 2026)

17 different users commented on 132 different issues.

## Recommended Actions

 * Response Recommended
    * @typescript-automation[bot] provided perf run results as requested in [microsoft/TypeScript-go#4102](https://github.com/microsoft/TypeScript-go/pull/4102#issuecomment-5298557303)
    * @typescript-automation[bot] provided perf run results as requested in [microsoft/TypeScript-go#4598](https://github.com/microsoft/TypeScript-go/pull/4598#issuecomment-5299152020)
    * @mt-bt asked if the fix would be backported to the 7.0.x release line in [microsoft/TypeScript-go#4614](https://github.com/microsoft/TypeScript-go/issues/4614#issuecomment-5298798901)
    * @typescript-automation[bot] provided perf run results as requested in [microsoft/TypeScript-go#4703](https://github.com/microsoft/TypeScript-go/pull/4703#issuecomment-5299251811)
    * @remcohaszing suggested that content mappers provide explicit auto-import insertion locations in [microsoft/TypeScript-go#4712](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5297091106)
    * @typescript-automation[bot] provided requested perf run results in [microsoft/TypeScript-go#4726](https://github.com/microsoft/TypeScript-go/pull/4726#issuecomment-5297865842)

## Activity Summary

### [Issue microsoft/TypeScript-go#1042](https://github.com/microsoft/TypeScript-go/issues/1042) (Closed, `Domain: JS`, **sandersn**, **RyanCavanaugh**, **Copilot**)

**Improve \`@overload\` error message to mention name of host function**

*Improve the @overload error message to include the function’s name when missing a return-type annotation.*

 * (18 weeks ago) **RyanCavanaugh** set milestone to `Post-7.0`, assigned to **Copilot**, and unassigned **Copilot**
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#1966](https://github.com/microsoft/TypeScript-go/pull/1966) (Open, `No linked issue`, `Unmigrated PR`)

**Add Yarn PnP support**

*Add native Yarn Plug'n'Play support to TypeScript Go with VFS integration and manifest handling following PnP specification.*

 * [8 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1966#issuecomment-4709751672) **SerenModz21** suggested adding "Closes #460" to the PR description to properly link the issue and provided a documentation link
 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1966#issuecomment-4905614254) **proyectoramirez** said "What is a good way to try this PR in a yarn project?"
 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1966#issuecomment-4926997057) **GGomez99** suggested cloning the repository and following the How to build and run section of the contributing doc
 * **RyanCavanaugh** added label `Unmigrated PR`

### [Issue microsoft/TypeScript-go#2279](https://github.com/microsoft/TypeScript-go/issues/2279) (Closed, `Domain: Editor`, **gabritto**)

**Add snippet completions for methods**

*Implement snippet completions in ts-go so selecting a base class method suggestion inserts its full signature and stub.*

 * **gabritto** assigned to **gabritto**
 * **jakebailey** added label `Domain: Editor`
 * **RyanCavanaugh** added to milestone `Post-7.0`
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript-go#2417](https://github.com/microsoft/TypeScript-go/pull/2417) (Closed, `No linked issue`)

**Support \-\-pprofDir option with \-\-watch**

*Add --pprofDir support to the --watch mode to allow profiling of active processes.*

 * (17 weeks ago) **RyanCavanaugh** added label `No linked issue`, and set milestones to `Possible Improvement`, `Possible Improvement`
 * [today](https://github.com/microsoft/TypeScript-go/pull/2417#issuecomment-5295865401) **RyanCavanaugh** said "Sounds like no"
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#2602](https://github.com/microsoft/TypeScript-go/pull/2602) (Closed)

**feat: comprehensive Type Hierarchy LSP support**

*Adds comprehensive LSP-based Type Hierarchy support in TypeScript language service for navigating class, interface, and type alias supertypes and subtypes.*

 * created by **kbrilla**
 * **RyanCavanaugh** added to milestone `Possible Improvement`
 * [today](https://github.com/microsoft/TypeScript-go/pull/2602#issuecomment-5295875126) **RyanCavanaugh** said "Closing Draft PRs in preparation for our move back to the TypeScript repo. See you there!"
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#2908](https://github.com/microsoft/TypeScript-go/pull/2908) (Closed, **DanielRosenwasser**, **Copilot**)

**Add regression test for inlay hints crash on reparsed nodes \(\#2460\)**

*Add a regression test to ensure computing inlay hints on reparsed AST nodes in a JS module.exports function prevents panics.*

 * [14 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2908#issuecomment-4403509887) **DanielRosenwasser** said "@copilot try building and fix and build errors."
 * [14 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2908#issuecomment-4403591216) **Copilot** fixed the build error by replacing bool true with core.TSTrue, adding the core import, and updating the baseline to reflect the correct output after the crash fix
 * **RyanCavanaugh** added to milestone `Possible Improvement`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2944](https://github.com/microsoft/TypeScript-go/pull/2944) (Closed)

**\[draft\] more formatting tests **

*A draft pull request addresses formatting bug fixes and adds tests, with more tests to follow post-7.0.*

 * [17 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2944#issuecomment-4238228195) **typescript-bot** provided performance run results
 * [17 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2944#issuecomment-4238257454) **typescript-bot** said "@iisaduan, the perf run you requested failed. You can check the log here."
 * **iisaduan** added to milestone `Post-7.0`
 * (today) **iisaduan** closed the issue

### [PR microsoft/TypeScript-go#3220](https://github.com/microsoft/TypeScript-go/pull/3220) (Closed)

**Preserve error elaboration for indexed access type assignments**

*Improve TypeScript diagnostic messages by preserving specific error details for assignments to indexed access types.*

 * [20 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3220#issuecomment-4127991153) **jakebailey** said "Maybe I don't have context here, but, I don't find the new messages more helpful than the existing one..."
 * [20 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3220#issuecomment-4131552782) **gary-donut** provided an example demonstrating that assignment via this['faa'] yields less precise error messages than direct assignment
 * **RyanCavanaugh** added to milestone `Possible Improvement`
 * [today](https://github.com/microsoft/TypeScript-go/pull/3220#issuecomment-5295922193) **RyanCavanaugh** said "Failing CI - can try this again in the TypeScript repo once we move"
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#3228](https://github.com/microsoft/TypeScript-go/pull/3228) (Closed, **DanielRosenwasser**, **Copilot**)

**Track file extension in LSP request failure telemetry**

*Include an optional fileExtension field in LSP request failure telemetry to capture the affected file type.*

 * [19 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3228#issuecomment-4156546121) **DanielRosenwasser** said "@copilot+claude-sonnet-4.6 merge from main and resolve conflicts"
 * [19 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3228#issuecomment-4156638191) **Copilot** merged from main and resolved two conflicts in server.go
 * **RyanCavanaugh** added to milestone `Possible Improvement`
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#3264](https://github.com/microsoft/TypeScript-go/pull/3264) (Closed, `Unmigrated PR`, **gabritto**)

**support quick info and go to definition on mapped keys**

*Enable quick info and go to definition features for mapped keys in the TypeScript language service.*

 * [12 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3264#issuecomment-4523942459) **geekeren** said "do we have any beta version to validate?"
 * (9 weeks ago) **RyanCavanaugh** set milestone to `Post-7.0`, and removed from milestone `TypeScript 7.0 RC`
 * [today](https://github.com/microsoft/TypeScript-go/pull/3264#issuecomment-5295940687) **RyanCavanaugh** said "Closing due to impending repo move - looks like this could get picked back up in the TypeScript repo once comments are addressed. Thanks!"
 * (today) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** added label `Unmigrated PR`

### [PR microsoft/TypeScript-go#3271](https://github.com/microsoft/TypeScript-go/pull/3271) (Closed, `No linked issue`)

**Fix for a snapshot update with a nil CommandLine**

*Add a nil check in NewProjectResponse to prevent panics when handling projects with nil CommandLine during snapshot updates.*

 * (9 weeks ago) **RyanCavanaugh** added label `No linked issue`, set milestone to `Post-7.0`, and removed from milestone `TypeScript 7.0 RC`
 * [today](https://github.com/microsoft/TypeScript-go/pull/3271#issuecomment-5296523688) **navya9singh** said "Issue was fixed in another PR"
 * (today) **navya9singh** closed the issue

### [PR microsoft/TypeScript-go#3277](https://github.com/microsoft/TypeScript-go/pull/3277) (Closed, **DanielRosenwasser**, **Copilot**)

**Implement "find file references"**

*Implement cross-project 'find file references' for JS/TS in VS Code by adding a custom LSP request and core reference logic.*

 * (20 weeks ago) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * **RyanCavanaugh** added to milestone `Possible Improvement`
 * [today](https://github.com/microsoft/TypeScript-go/pull/3277#issuecomment-5298230947) **RyanCavanaugh** said "Closing as it's conflicted and still in draft, we can re-vibe post-move"
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#3297](https://github.com/microsoft/TypeScript-go/pull/3297) (Open, `No linked issue`, **weswigham**)

**Allow global Symbol computed names during pseudochecker object literal serialization**

*Support global Symbol computed property names in pseudochecker object literal serialization to match Strada’s behavior.*

 * (9 weeks ago) **RyanCavanaugh** added label `No linked issue`, set milestone to `Post-7.0`, and removed from milestone `TypeScript 7.0 RC`
 * **RyanCavanaugh** assigned to **weswigham**

### [PR microsoft/TypeScript-go#3309](https://github.com/microsoft/TypeScript-go/pull/3309) (Closed)

**Don't strip release binaries**

*Disable stripping of release binaries to retain debug symbols for easier debugging and tooling support despite larger package size*

 * created by **jakebailey**
 * **RyanCavanaugh** added to milestone `Possible Improvement`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3331](https://github.com/microsoft/TypeScript-go/pull/3331) (Open, `Unmigrated PR`)

**Use trie for removeStringLiteralsMatchedByTemplateLiterals**

*Adopt a trie-based implementation for removeStringLiteralsMatchedByTemplateLiterals to resolve TypeScript issue 63342.*

 * created by **eps1lon**
 * **RyanCavanaugh** added to milestone `Possible Improvement`
 * [today](https://github.com/microsoft/TypeScript-go/pull/3331#issuecomment-5297607770) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3331#issuecomment-5297608752) **typescript-automation[bot]** started build jobs and posted status and results links
 * [today](https://github.com/microsoft/TypeScript-go/pull/3331#issuecomment-5297880991) **typescript-automation[bot]** posted perf run results for the requested tsc performance comparison

### [PR microsoft/TypeScript-go#3362](https://github.com/microsoft/TypeScript-go/pull/3362) (Open, `Unmigrated PR`)

**Replace most ID usage with pointers**

*Propose replacing most ID fields with pointers in Go to leverage pointer comparability and reduce overhead.*

 * [6 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3362#issuecomment-4870099786) **jakebailey** said "@typescript-bot perf test this"
 * [6 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3362#issuecomment-4870100315) **typescript-automation[bot]** reported that performance tests had started and provided links to build status and results
 * [6 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3362#issuecomment-4870283060) **typescript-automation[bot]** reported the performance comparison results for the requested perf run
 * **jakebailey** added label `Unmigrated PR`

### [PR microsoft/TypeScript-go#3369](https://github.com/microsoft/TypeScript-go/pull/3369) (Open, `No linked issue`, `Unmigrated PR`)

**Limit loader/emitter to GOMAXPROCS**

*Limit parsing and emitting workloads to a GOMAXPROCS-sized goroutine pool to prevent unbounded concurrency and stack growth.*

 * [6 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3369#issuecomment-4847634269) **jakebailey** said "@typescript-bot perf test this"
 * [6 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3369#issuecomment-4847634796) **typescript-automation[bot]** reported that performance test jobs started and provided links to build status and results
 * [6 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3369#issuecomment-4847820197) **typescript-automation[bot]** provided the perf run results as requested
 * **jakebailey** added label `Unmigrated PR`

### [PR microsoft/TypeScript-go#3385](https://github.com/microsoft/TypeScript-go/pull/3385) (Open, `Unmigrated PR`)

**Restore CommaListExpression support**

*Proposal to restore the CommaListExpression optimization removed in PR #3367 that prevented excessively nested comma binary expressions.*

 * created by **jakebailey**
 * **jakebailey** added label `Unmigrated PR`

### [PR microsoft/TypeScript-go#3432](https://github.com/microsoft/TypeScript-go/pull/3432) (Closed)

**Enable allowJs when inferred project has root JS files**

*Automatically enable allowJs for inferred projects with root JS files and introduce a @noDefaultOpen option to prevent default file openings in fourslash tests.*

 * [17 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3432#issuecomment-4271642537) **andrewbranch** confirmed that session.compilerOptionsForInferredProjects was never set in real VS Code and that project.go default options always included --allowJs
 * [17 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3432#issuecomment-4271924781) **jakebailey** mentioned that the issue wasn't urgent, said they would investigate adjusting tests to use defaults, and noted the need to support the VS Code options for those defaults
 * **RyanCavanaugh** added to milestone `Post-7.0`
 * [today](https://github.com/microsoft/TypeScript-go/pull/3432#issuecomment-5296504662) **jakebailey** said "I think this PR is not going to go forward, but we can use it as a reference for a future fix"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3515](https://github.com/microsoft/TypeScript-go/pull/3515) (Open, `No linked issue`, **navya9singh**)

**Expose formatNodeForInsertion in internal API**

*Add the formatNodeForInsertion function to the library’s internal API to enable its use by external modules.*

 * (9 weeks ago) **RyanCavanaugh** added label `No linked issue`, set milestone to `Possible Improvement`, and removed from milestone `TypeScript 7.0 RC`
 * [today](https://github.com/microsoft/TypeScript-go/pull/3515#issuecomment-5298704595) **RyanCavanaugh** said "Do we still need this?"

### [PR microsoft/TypeScript-go#3619](https://github.com/microsoft/TypeScript-go/pull/3619) (Open, `No linked issue`, `Unmigrated PR`)

**perf: Make \`NodeArray\` no longer inherit from \`Array\`**

*Detach NodeArray from Array prototype to prevent direct array method usage and achieve significant performance gains.*

 * (9 weeks ago) **RyanCavanaugh** added label `No linked issue`, set milestone to `Possible Improvement`, and removed from milestone `Post-7.0`
 * [today](https://github.com/microsoft/TypeScript-go/pull/3619#issuecomment-5296902234) **jakebailey** said "Is this still needed? Did we end up doing this another way?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3619#issuecomment-5297822444) **andrewbranch** described making improvements to preserve array element access while noting the proposal still performs better but sacrifices direct indexing

### [PR microsoft/TypeScript-go#3726](https://github.com/microsoft/TypeScript-go/pull/3726) (Open, **DanielRosenwasser**, **Copilot**)

**Preserve original stack traces in cross\-project panic handling**

*Wrap panics in PanicWithStack to capture and propagate original stack traces for cross-project panic handling.*

 * **RyanCavanaugh** added to milestone `Possible Improvement`
 * [9 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3726#issuecomment-4652511528) **RyanCavanaugh** said "@copilot address the merge conflicts"
 * [1 month ago](https://github.com/microsoft/TypeScript-go/pull/3726#issuecomment-5005763801) **RyanCavanaugh** said "Just doing some Copilot testing here, please ignore reviews"
 * (today) **jakebailey** closed the issue
 * (today) **jakebailey** reopened the issue

### [PR microsoft/TypeScript-go#3728](https://github.com/microsoft/TypeScript-go/pull/3728) (Open, `No linked issue`, `Unmigrated PR`)

**Fix keyof deferred for non\-generic substitution types \(\#2186\)**

*Resolve keyof immediately for non-generic substitution types to correct indexed access assignability and quick info*

 * [14 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3728#issuecomment-4402998409) **jakebailey** said "If this fixes #2186, can you write "Fixes #2186" in the description?"
 * (14 weeks ago) **RyanCavanaugh** added label `No linked issue`, and set milestone to `Post-7.0`
 * [today](https://github.com/microsoft/TypeScript-go/pull/3728#issuecomment-5298451660) **jakebailey** said "Checked, and this does fix #2186"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3728#issuecomment-5298456281) **jakebailey** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3728#issuecomment-5298456989) **typescript-automation[bot]** reported build start and completion statuses for test top400 and perf test this faster
 * [today](https://github.com/microsoft/TypeScript-go/pull/3728#issuecomment-5298657492) **typescript-automation[bot]** reported performance run results for the requested baseline..pr comparison, including errors, symbols, types, memory usage, and memory allocations
 * [today](https://github.com/microsoft/TypeScript-go/pull/3728#issuecomment-5298948718) **typescript-automation[bot]** reported that everything looked good after comparing main and the pull request across the top 400 repositories with tsc

### [PR microsoft/TypeScript-go#3840](https://github.com/microsoft/TypeScript-go/pull/3840) (Closed, `No linked issue`)

**Don't send bundled file watchers to client**

*Filter out bundled TypeScript library file patterns from LSP server watch requests to prevent invalid client watchers.*

 * (9 weeks ago) **RyanCavanaugh** added label `No linked issue`, set milestone to `Post-7.0`, and removed from milestone `Possible Improvement`
 * [today](https://github.com/microsoft/TypeScript-go/pull/3840#issuecomment-5298701653) **RyanCavanaugh** said "This needs both a test and a linked issue. Closing; feel free to open once the repo moves back to TypeScript along with the required other parts."
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#3871](https://github.com/microsoft/TypeScript-go/pull/3871) (Closed, **sandersn**, **RyanCavanaugh**, **Copilot**)

**Use named\-function overload diagnostic for JSDoc \`@overload\` return\-type omissions**

*Use named-function TS7010 diagnostics for JSDoc @overload return-type omissions when function is named, fallback to TS7012, updating tests and baselines.*

 * **RyanCavanaugh** added to milestone `Post-7.0`
 * [10 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3871#issuecomment-4607015077) **jakebailey** said "@copilot+gpt-5.5 merge main and update baselines"
 * [10 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3871#issuecomment-4607140237) **Copilot** merged main and updated the conflicted baseline, ran tests successfully
 * [today](https://github.com/microsoft/TypeScript-go/pull/3871#issuecomment-5297852122) **Copilot** addressed the review comments by removing the redundant local test and relying on the existing jsFileMethodOverloads3 coverage with updated baselines
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#3935](https://github.com/microsoft/TypeScript-go/pull/3935) (Open, `No linked issue`, `Unmigrated PR`)

**Narrow keyword completions for concise arrow expression bodies**

*Port keyword completion filtering to Go so concise arrow function bodies only suggest expression keywords.*

 * created by **DhineshPonnarasan**
 * (10 weeks ago) **RyanCavanaugh** added label `No linked issue`, and set milestone to `Post-7.0`
 * [today](https://github.com/microsoft/TypeScript-go/pull/3935#issuecomment-5298337051) **jakebailey** said "I think this PR would have been fine, had it added a test for what it was trying to do."

### [PR microsoft/TypeScript-go#3949](https://github.com/microsoft/TypeScript-go/pull/3949) (Closed)

**feat: completion snippets**

*Add completion snippets functionality to enable snippet-based code suggestions during development.*

 * (12 weeks ago) **a-tarasyuk** closed the issue
 * (9 weeks ago) **a-tarasyuk** reopened the issue
 * **RyanCavanaugh** added to milestone `Post-7.0`
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript-go#3989](https://github.com/microsoft/TypeScript-go/pull/3989) (Closed, `No linked issue`)

**lsp: emit VS\-internal HiddenInEditor tag for unnecessary diagnostics**

*Emit Visual Studio’s HiddenInEditor tag for Unnecessary diagnostics when vs_supportsVisualStudioExtensions is enabled so unused code fades in the editor*

 * created by **joj**
 * (9 weeks ago) **RyanCavanaugh** added label `No linked issue`, and set milestone to `Possible Improvement`
 * [today](https://github.com/microsoft/TypeScript-go/pull/3989#issuecomment-5297707612) **joj** said "Closing for now, will reopen if there's need"
 * (today) **joj** closed the issue

### [PR microsoft/TypeScript-go#3990](https://github.com/microsoft/TypeScript-go/pull/3990) (Closed, **joj**, **Copilot**)

**lsproto: separate VS diagnostic tag constant from CodeActionKind block**

*Relocate VSDiagnosticTagHiddenInEditor from the CodeActionKind constant block into a dedicated DiagnosticTag block to improve protocol organization.*

 * created by **Copilot**
 * (12 weeks ago) **Copilot** assigned to **Copilot**, **joj**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4003](https://github.com/microsoft/TypeScript-go/pull/4003) (Closed, **joj**, **Copilot**)

**Add VS hidden\-in\-editor tag for Unnecessary diagnostics and cover with manual fourslash tests**

*Enable Visual Studio hidden-in-editor tag for unnecessary diagnostics and add manual fourslash tests for both VS and non-VS scenarios.*

 * created by **Copilot**
 * (12 weeks ago) **Copilot** assigned to **Copilot**, **joj**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4003#issuecomment-5295879655) **RyanCavanaugh** said "Closing for repo move"
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#4007](https://github.com/microsoft/TypeScript-go/pull/4007) (Closed, `No linked issue`)

**Accepted symbol baselines**

*Establish accepted symbol baselines before addressing bugs and investigations in a later pull request.*

 * created by **RyanCavanaugh**
 * (9 weeks ago) **RyanCavanaugh** added label `No linked issue`, and set milestone to `Possible Improvement`
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#4102](https://github.com/microsoft/TypeScript-go/pull/4102) (Open)

**Cache alias candidates for symbol accessibility**

*Cache alias candidates to optimize symbol accessibility resolution.*

 * created by **Zzzen**
 * **RyanCavanaugh** added to milestone `Possible Improvement`
 * [today](https://github.com/microsoft/TypeScript-go/pull/4102#issuecomment-5298327583) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4102#issuecomment-5298328172) **typescript-automation[bot]** posted a build status update with job start and result links
 * [today](https://github.com/microsoft/TypeScript-go/pull/4102#issuecomment-5298557303) **typescript-automation[bot]** provided the requested performance run results in a detailed report

### [PR microsoft/TypeScript-go#4112](https://github.com/microsoft/TypeScript-go/pull/4112) (Closed)

**Use json/v2 package in Go 1\.27\+**

*Switch to the Go 1.27+ json/v2 package after evaluating compatibility with the tip release.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4158](https://github.com/microsoft/TypeScript-go/pull/4158) (Closed, **jakebailey**, **Copilot**)

**Preserve source text for negative numeric literals in declaration emit**

*Preserve original source text for top-level negative numeric const literals in TypeScript declaration emit instead of canonicalizing them.*

 * [10 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4158#issuecomment-4595951958) **Copilot** added a compiler test covering negative and positive numeric literal behaviors with baselines
 * [8 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4158#issuecomment-4744666084) **jakebailey** said "@copilot+gpt-5.5 Merge main and update tests"
 * [8 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4158#issuecomment-4744848306) **Copilot** merged origin/main and resolved pseudotypenodebuilder.go conflict by combining flag handling and reused-literal state, ran tests successfully with no compiler baseline updates needed
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4160](https://github.com/microsoft/TypeScript-go/pull/4160) (Closed, **jakebailey**, **Copilot**)

**Preserve inline parameter comments on inferred function types in declaration emit**

*Restore inline parameter comments when emitting declarations for inferred function types by preserving parameter positions.*

 * **Copilot** assigned to **jakebailey**
 * [8 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4160#issuecomment-4744667296) **jakebailey** said "@copilot+gpt-5.5 Merge main and update tests"
 * [8 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4160#issuecomment-4744925609) **Copilot** merged main and updated the affected baselines
 * [today](https://github.com/microsoft/TypeScript-go/pull/4160#issuecomment-5296515809) **jakebailey** said "@copilot+gpt-5.6-sol Merge main and update tests"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4211](https://github.com/microsoft/TypeScript-go/pull/4211) (Open, `Unmigrated PR`)

**Optimize bin by replacing node\_modules/\.bin/tsgo with a symlink**

*Replace the node_modules/.bin/tsgo shim with a direct symlink to the actual binary to improve startup performance.*

 * [10 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4211#issuecomment-4636140027) **jakebailey** said "Seems to work!"
 * [9 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4211#issuecomment-4638058619) **JoostK** proposed spawning native tsgo before attempting optimization to avoid unnecessary optimizeBin overhead, noted this isn’t feasible with process.execve not forking, and questioned whether the overhead is significant
 * [9 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4211#issuecomment-4638069692) **JoostK** suggested invoking tsgo with an --optimize-bin flag to move optimization into the native binary, but noted it was probably not worth it
 * **jakebailey** added label `Unmigrated PR`

### [PR microsoft/TypeScript-go#4240](https://github.com/microsoft/TypeScript-go/pull/4240) (Closed, `No linked issue`)

**Inline \`GetCombinedNodeFlags\` and \`GetCombinedModifierFlags\` bodies**

*Inline flag computations by replacing generic helper with direct node field reads, boosting performance by about 27%.*

 * [7 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4240#issuecomment-4770844703) **jakebailey** said "I'm still not sure; obviously it's measurable, but there's a balance between code duplication and how much this benefits real-world code."
 * [7 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4240#issuecomment-4772686404) **mds-ant** said "Yeah, that's fair. I'm happy to close this one out if you'd rather not take on the duplication."
 * (7 weeks ago) **mds-ant** closed the issue
 * (today) **jakebailey** reopened the issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/4240#issuecomment-5295827279) **jakebailey** said "With optimizations I'm trying in #4903, this turns out to actually help!"
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4267](https://github.com/microsoft/TypeScript-go/issues/4267) (Closed, `Crash`, **DanielRosenwasser**, **Copilot**)

**Unknown file type\(?\) triggers fatal server crash**

*Loading a file with an unrecognized type intermittently triggers a fatal server crash during parsing.*

 * (9 weeks ago) **DanielRosenwasser** added label `Crash`, and assigned to **DanielRosenwasser**
 * **RyanCavanaugh** added to milestone `Post-7.0`
 * [today](https://github.com/microsoft/TypeScript-go/issues/4267#issuecomment-5299045592) **jakebailey** said "Going to preemptively say that #4628 fixes this"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4268](https://github.com/microsoft/TypeScript-go/pull/4268) (Closed, **DanielRosenwasser**, **Copilot**)

**Avoid project crash for unknown file types**

*Default unknown file script kinds to TypeScript to prevent parser panics when opening unrecognized file types.*

 * created by **Copilot**
 * (9 weeks ago) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4268#issuecomment-5299046043) **jakebailey** said "Going to preemptively say that #4628 fixes this"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4328](https://github.com/microsoft/TypeScript-go/pull/4328) (Closed, `dependencies`, `javascript`)

**Bump form\-data from 4\.0\.5 to 4\.0\.6**

*Bumps form-data from v4.0.5 to v4.0.6, adding escapes for CR, LF, and quotes in field names and updating dependencies.*

 * (8 weeks ago) **dependabot[bot]** added labels `dependencies`, `javascript`
 * **RyanCavanaugh** added to milestone `Post-7.0`
 * (today) **jakebailey** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/4328#issuecomment-5298394332) **dependabot[bot]** explained how to ignore dependency update notifications or reopen the PR to resolve conflicts

### [PR microsoft/TypeScript-go#4364](https://github.com/microsoft/TypeScript-go/pull/4364) (Closed)

**Add default\.pgo file for main entrypoint**

*Add a default.pgo file for the main entrypoint to utilize the new performance infrastructure*

 * [8 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4364#issuecomment-4743658006) **jakebailey** said "@typescript-bot perf test this faster"
 * [8 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4364#issuecomment-4743658692) **typescript-automation[bot]** notified of job start and provided links to build status and results
 * [8 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4364#issuecomment-4743897697) **typescript-automation[bot]** reported the requested perf run results
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4365](https://github.com/microsoft/TypeScript-go/pull/4365) (Closed, **jakebailey**, **Copilot**)

**Preserve typedef comments in declaration emit**

*Preserve descriptive JSDoc comments on typedefs and callbacks in emitted declaration files while preventing duplicate comment output*

 * **Copilot** assigned to **jakebailey**
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4365#issuecomment-5111400237) **dkamins** confirmed the PR output matched expectations and provided a summary table of JSDoc typedef behaviors with a repro archive
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4365#issuecomment-5146369402) **jakebailey** said "@copilot+gpt-5.6-sol Merge main and fix baselines. Also consider the above"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4365#issuecomment-5296457910) **jakebailey** said "I think this PR is just very weird and wrong, not worth merging right now"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4401](https://github.com/microsoft/TypeScript-go/pull/4401) (Closed)

**Default to GOGC=50**

*Default the Go garbage collector threshold (GOGC) to 50 to achieve substantial memory savings without degrading performance.*

 * [7 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4401#issuecomment-4773774427) **typescript-automation[bot]** notified that the requested performance run results were available
 * [7 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4401#issuecomment-4773780014) **jakebailey** said "Huh... Worse?"
 * [7 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4401#issuecomment-4773785662) **jakebailey** said "Well, more worse than I was expecting anyway"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4409](https://github.com/microsoft/TypeScript-go/pull/4409) (Closed)

**\[feature request\] Support type predicate getters for control flow narrowing**

*Support type predicate getters so accessing getters can narrow receiver types in control flow checks*

 * created by **js2me**
 * [7 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4409#issuecomment-4779021262) **js2me** said "@microsoft-github-policy-service agree"
 * **RyanCavanaugh** added to milestone `Possible Improvement`
 * [today](https://github.com/microsoft/TypeScript-go/pull/4409#issuecomment-5299060762) **jakebailey** expressed confusion about the absence of a proposal or feature request before merging
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4430](https://github.com/microsoft/TypeScript-go/pull/4430) (Closed)

**Match Strada's behavior to allow satisfying recursive indexed access**

*Align Corsa’s base-constraint caching with Strada’s two-tier model to restore correct recursive indexed-access constraint resolution.*

 * created by **RyanCavanaugh**
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#4444](https://github.com/microsoft/TypeScript-go/pull/4444) (Closed, **RyanCavanaugh**, **Copilot**)

**Handle recursive aliases in named tuple rest elements**

*Enable recursive type aliases in named tuple rest elements by extending alias resolution to ArrayType to avoid circularity errors.*

 * (7 weeks ago) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * **RyanCavanaugh** added to milestone `Post-7.0`
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#4449](https://github.com/microsoft/TypeScript-go/pull/4449) (Open)

**restore JSDoc member name check for private identifier references**

*Restores the JSDoc member name validation for private identifiers in isValidReferencePosition by implementing the missing helper.*

 * [7 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4449#issuecomment-4805882923) **jakebailey** said "This needs tests that show this does something; it might not due to reparsing"
 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4449#issuecomment-4906335658) **jakebailey** said "What is this for? You're making the baselines worse?"
 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4449#issuecomment-4917489457) **aamoghS** fixed the parser to retain private identifier nodes in JSDoc @see tags, tightened up isJSDocMemberName to avoid normal this.#x matches, updated the checker to resolve private identifiers, and refreshed the baselines
 * [today](https://github.com/microsoft/TypeScript-go/pull/4449#issuecomment-5297852487) **aamoghS** rebased onto latest main and explained that the fourslash baseline for TestFindAllReferencesJSDocPrivateIdentifier showed bidirectional references between the #field declaration and @see C.#field, and clarified that isJSDocMemberName remains limited to JSDoc QualifiedName contexts so ordinary this.#x is unchanged

### [PR microsoft/TypeScript-go#4515](https://github.com/microsoft/TypeScript-go/pull/4515) (Closed)

**Test and fix nonlocal callable variance cycles**

*Add tests and fixes for nonlocal callable variance cycles caused by specific checker associations and ordering*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4515#issuecomment-5157034423) **ahejlsberg** said "What exactly happened with xstate and variance that this PR fixes? And is there a way to reproduce to help reasoning about it?"
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4515#issuecomment-5158608693) **jakebailey** said "This nasty test was the best I could get, the other option being to take #4313 and undo the checker changes and then build xstate"
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4515#issuecomment-5158611148) **jakebailey** said "I'll try to get something more minimal when I have a chance"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4551](https://github.com/microsoft/TypeScript-go/pull/4551) (Closed)

**Preserve pseudotype when serializing autoType declarations**

*Declaration serialization incorrectly emits ‘any’ for auto-typed variables initialized with null or undefined instead of preserving their pseudotypes.*

 * created by **revyh**
 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4551#issuecomment-4899558059) **revyh** said "@microsoft-github-policy-service agree"
 * (today) **jakebailey** closed the issue
 * (today) **jakebailey** reopened the issue
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4592](https://github.com/microsoft/TypeScript-go/pull/4592) (Open)

**Improve responsiveness of \`tsc build\` to interruption**

*Enhance tsc build responsiveness to SIGINT and SIGTERM by threading cancellation contexts through compilation, exiting with proper codes, and adding tests.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4592#issuecomment-5063525613) **jakebailey** said "The further this goes, the more I wonder if we should simply stop handling signals except in the LS or something. Obviously we never set up any signal handlers in tsc, right?"
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4592#issuecomment-5064330139) **lukesandberg** noted that skipping signal handlers causes crashes with partial outputs and suggested propagating context.Context for LSP timeouts for consistency
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/4592#issuecomment-5269980557) **lukesandberg** asked whether to abandon the approach, described how removing signal handlers breaks ctrl-c handling in tsc --watch by causing goroutine panics, and proposed possible solutions
 * [today](https://github.com/microsoft/TypeScript-go/pull/4592#issuecomment-5296197926) **jakebailey** suggested limiting or omitting signal handling and aiming to fix it in a patch release

### [PR microsoft/TypeScript-go#4598](https://github.com/microsoft/TypeScript-go/pull/4598) (Closed)

**Fix optionality stripping when mapping over tuples under EOPT**

*Ensure mapping over tuples under EOPT preserves optionality instead of incorrectly stripping it*

 * created by **Andarist**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4598#issuecomment-5298987858) **jakebailey** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4598#issuecomment-5298988302) **typescript-automation[bot]** provided automated update on build statuses for `test top400` and `perf test this faster`
 * [today](https://github.com/microsoft/TypeScript-go/pull/4598#issuecomment-5299152020) **typescript-automation[bot]** provided the requested performance run results
 * [today](https://github.com/microsoft/TypeScript-go/pull/4598#issuecomment-5299389527) **typescript-automation[bot]** reported that the tsc run on the top 400 repos comparing main and the pull request merge looked good

### [PR microsoft/TypeScript-go#4603](https://github.com/microsoft/TypeScript-go/pull/4603) (Closed)

**fix\(checker\): avoid computed enum member stack overflow**

*Prevent stack overflow by skipping dynamic computed enum member names in declared-type construction while preserving TS1164 errors.*

 * created by **ZhiyaoWen999**
 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4603#issuecomment-4942053581) **ZhiyaoWen999** said "@microsoft-github-policy-service agree"
 * (today) **jakebailey** closed the issue
 * (today) **jakebailey** reopened the issue
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4605](https://github.com/microsoft/TypeScript-go/pull/4605) (Closed)

**Fix hover crash for generic members of merged aliases**

*Prevents hover crashes when inspecting generic members of merged type aliases.*

 * created by **Andarist**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4605#issuecomment-5298523489) **jakebailey** said "#4894"
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4614](https://github.com/microsoft/TypeScript-go/issues/4614) (Closed, `Needs Investigation`, **johnfav03**)

**\`tsc \-b \-\-watch\` takes tens of seconds to start watching on a large project\-references solution \(\`computeDesiredWatches\` is O\(files × dirs\)\)**

*tsc -b --watch stalls for tens of seconds on large project-reference solutions because computeDesiredWatches’s O(files×dirs) logic delays filesystem watch registration*

 * (1 month ago) **RyanCavanaugh** set milestone to `TypeScript 7.1`, and assigned to **johnfav03**
 * (2 weeks ago) **johnfav03** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/issues/4614#issuecomment-5298798901) **mt-bt** asked if there were plans to backport the fix to 7.0.x after reporting high CPU usage in watch mode and confirming the issue was resolved in nightly builds
 * [today](https://github.com/microsoft/TypeScript-go/issues/4614#issuecomment-5298805195) **jakebailey** said "Yes, after #4876"

### [Issue microsoft/TypeScript-go#4618](https://github.com/microsoft/TypeScript-go/issues/4618) (Closed, `Domain: Editor`, **jakebailey**, **Copilot**)

**Some imports are not updated after a file rename, in composite projects**

*TypeScript 7 composite projects do not update imports in unloaded subprojects when renaming files, unlike TypeScript 6.*

 * (3 weeks ago) **jakebailey** assigned to **Copilot**, **jakebailey**
 * **RyanCavanaugh** added to milestone `Post-7.0`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4623](https://github.com/microsoft/TypeScript-go/pull/4623) (Closed)

**Fix continueOnError casing in pipeline YAML and The indentation**

*Updated pipeline YAML to correct continueOnError casing, fix indentation, and improve task display name.*

 * created by **joaquinjulca26**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4623#issuecomment-5298877607) **RyanCavanaugh** said "We'd prefer to not have non-team-members editing these yaml files, as they are highly sensitive. There's no end-user impact of this, so closing."
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#4646](https://github.com/microsoft/TypeScript-go/pull/4646) (Closed, `Voight-Kampff Anomaly`, `Unmigrated PR`)

**Fix hover documentation for intersected properties**

*Enhance TypeScript hover tooltips for intersection properties by aggregating JSDoc from all declarations.*

 * created by **cuishuang**
 * [1 month ago](https://github.com/microsoft/TypeScript-go/pull/4646#issuecomment-4979689386) **Andarist** said "this issue is already being fixed by my older PR: https://github.com/microsoft/typescript-go/pull/3663"
 * **RyanCavanaugh** added label `Voight-Kampff Anomaly`
 * **RyanCavanaugh** added label `Unmigrated PR`

### [PR microsoft/TypeScript-go#4649](https://github.com/microsoft/TypeScript-go/pull/4649) (Closed, **RyanCavanaugh**, **Copilot**)

**Fix declaration emit synthesizing extensionless import\(\) specifier under allowImportingTsExtensions \+ nodenext**

*Declaration emit under allowImportingTsExtensions and nodenext stripped .js extensions from import() specifiers, causing TS2307 errors.*

 * created by **Copilot**
 * (1 month ago) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4649#issuecomment-5298429121) **jakebailey** said "#4662"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4653](https://github.com/microsoft/TypeScript-go/pull/4653) (Open, `Unmigrated PR`)

**Error with a suggestion of '\.' for empty project reference paths**

*Report empty project reference paths with a new TS18052 diagnostic suggesting '.' instead of the generic TS18051 error message.*

 * created by **KlyneChrysler**
 * **RyanCavanaugh** added label `Unmigrated PR`

### [PR microsoft/TypeScript-go#4666](https://github.com/microsoft/TypeScript-go/pull/4666) (Open, `Voight-Kampff Anomaly`, `Unmigrated PR`)

**POC: ambient module declarations keyed on import attributes**

*Proof-of-concept for ambient module declarations keyed by import attributes to support text or bytes file imports in TypeScript's Go port.*

 * created by **bartlomieju**
 * [1 month ago](https://github.com/microsoft/TypeScript-go/pull/4666#issuecomment-5004893772) **bartlomieju** said "@microsoft-github-policy-service agree"
 * **RyanCavanaugh** added label `Voight-Kampff Anomaly`
 * **RyanCavanaugh** added label `Unmigrated PR`

### [PR microsoft/TypeScript-go#4670](https://github.com/microsoft/TypeScript-go/pull/4670) (Closed, `dependencies`, `javascript`)

**Bump adm\-zip from 0\.5\.17 to 0\.6\.0**

*Bump adm-zip from 0.5.17 to 0.6.0 to fix CVE-2026-39244, resolve bugs, add TypeScript types, and improve extraction behavior.*

 * (1 month ago) **dependabot[bot]** added labels `javascript`, `dependencies`, `javascript`
 * (today) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/4670#issuecomment-5298301368) **dependabot[bot]** explained how to ignore dependency update notifications or reopen the PR to resolve conflicts

### [PR microsoft/TypeScript-go#4674](https://github.com/microsoft/TypeScript-go/pull/4674) (Open, `Voight-Kampff Anomaly`, `Unmigrated PR`)

**Preserve JSDoc @property comments when reconstructing typedef types**

*Preserve JSDoc @property comments on typedefs when reconstructing inline types in generated .d.ts files.*

 * created by **veksa**
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4674#issuecomment-5016285782) **veksa** said "@microsoft-github-policy-service agree"
 * **RyanCavanaugh** added label `Voight-Kampff Anomaly`
 * **RyanCavanaugh** added label `Unmigrated PR`

### [PR microsoft/TypeScript-go#4676](https://github.com/microsoft/TypeScript-go/pull/4676) (Closed)

**Fix parsing of \`as\`/\`satisfies\` between \`\*\*\` operators**

*Account for right-associative exponentiation when rejecting unsafe as/satisfies expressions and add regression coverage.*

 * created by **magic-akari**
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#4677](https://github.com/microsoft/TypeScript-go/issues/4677) (Closed, `Domain: Editor`)

**JSDoc \(TSDoc ???\) is not shown for object literal properties on hover**

*In TypeScript 7, VS Code stops displaying JSDoc comments on hover for const object literal properties, losing per-property documentation.*

 * **nazmul-nhb** added label `Domain: Editor`
 * **RyanCavanaugh** added to milestone `Possible Improvement`
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/4677#issuecomment-5042964606) **jinxiangqiang** said "Release it as soon as possible. Thank you."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4685](https://github.com/microsoft/TypeScript-go/pull/4685) (Closed)

**fix\(4677\): preserve JSDoc for mapped type properties in hover**

*Ensure JSDoc comments for mapped type properties are retained and displayed in hover tooltips.*

 * created by **a-tarasyuk**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4695](https://github.com/microsoft/TypeScript-go/pull/4695) (Closed, **jakebailey**, **Copilot**)

**Update imports in unloaded composite projects after file rename**

*Load full composite project tree before renaming files to update imports in unopened projects.*

 * created by **Copilot**
 * (3 weeks ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4695#issuecomment-5297091536) **andrewbranch** said "@copilot it makes sense that we would need to load the project tree, but can you explain why this doesn't need to use the cross-project orchestrator like rename and find-all-references?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4695#issuecomment-5297129033) **Copilot** explained why file rename didn't require the cross-project orchestrator and detailed the differences between path-keyed sweeps and position-anchored searches
 * [today](https://github.com/microsoft/TypeScript-go/pull/4695#issuecomment-5297171451) **gabritto** clarified that the file rename algorithm was meaningfully different from the cross-project orchestrator
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4696](https://github.com/microsoft/TypeScript-go/pull/4696) (Closed)

**Fix merged polymorphic this reference analysis**

*Improves merged polymorphic this reference analysis by selecting the correct declaration to prevent runaway type instantiation and adding regression tests.*

 * created by **MatthewHarrigan**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4696#issuecomment-5295907754) **RyanCavanaugh** said "Closing Draft PRs in preparation for our move back to the TypeScript repo. See you there!"
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#4703](https://github.com/microsoft/TypeScript-go/pull/4703) (Open, `Unmigrated PR`)

**Store value symbol links inline on checker\-created symbols**

*Value symbol links for checker-created symbols are stored inline to eliminate paged store overhead and improve check performance.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4703#issuecomment-5072037478) **typescript-automation[bot]** reported CI job start and result status with links
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4703#issuecomment-5072314381) **typescript-automation[bot]** posted the performance run results
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4703#issuecomment-5072638607) **jakebailey** said "It does seem 3% faster on vscode, at least."
 * [today](https://github.com/microsoft/TypeScript-go/pull/4703#issuecomment-5299086842) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4703#issuecomment-5299087312) **typescript-automation[bot]** announced that performance tests had started and provided links to build status and results
 * [today](https://github.com/microsoft/TypeScript-go/pull/4703#issuecomment-5299251811) **typescript-automation[bot]** provided perf run results in a detailed comparison report

### [PR microsoft/TypeScript-go#4712](https://github.com/microsoft/TypeScript-go/pull/4712) (Open)

**Content mappers**

*Enable TypeScript to integrate unsupported file types through configurable external content mappers specified in tsconfig.json*

 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5279235915) **remcohaszing** suggested adding logging support via a `tsc --verbose` flag and LSP `log` notifications for both editor and CLI
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5287957894) **andrewbranch** said "Bikeshed request: I don’t love the name "tsContentMapper" for the mapper package.json key. Any better ideas?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5290710912) **remcohaszing** suggested using a JSONC snippet with a typescript.contentMapper namespace for future reuse
 * [today](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5296274770) **andrewbranch** listed environment variable logging behavior and renamed command flag and configuration key
 * [today](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5296486726) **andrewbranch** described making one final change to the shape of diagnosticDirectives before finishing
 * [today](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5297091106) **remcohaszing** ported most of the MDX Volar mapper to a content mapper, identified a break in TypeScript content mapper handling an empty mapping, and suggested that content mappers provide explicit auto-import insertion locations
 * [today](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5297226162) **andrewbranch** suggested investigating a change to skip incompatible spans when inserting imports in virtual text files
 * [today](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5297254750) **andrewbranch** corrected performance results and reported a 2x speed improvement over typescript-native-bridge
 * [today](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5298147329) **andrewbranch** referenced a commit showing extensions can contribute a JSON schema for content mapper options merged into the tsconfig schema
 * [later](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5302949742) **uhyo** reported that tsc hung when the content mapper used a Volta-managed node shim leaving the real node process alive and stderr open

### [Issue microsoft/TypeScript-go#4715](https://github.com/microsoft/TypeScript-go/issues/4715) (Closed, **jakebailey**)

**Request for support for Android**

*Enable straightforward installation and execution of the TypeScript compiler via npm in Android Termux without extra workarounds*

 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/4715#issuecomment-5062840275) **jakebailey** said "There's basically no way we're going to ship the entire repo in the package."
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/4715#issuecomment-5068954049) **thunder-coding** suggested packaging the repo separately or adding package.json scripts to download and build from the git tarball via gitHead
 * **RyanCavanaugh** added to milestone `Possible Improvement`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4716](https://github.com/microsoft/TypeScript-go/pull/4716) (Open, `Unmigrated PR`)

**Restore Strada\-style escaped symbol names**

*Revert to Strada-style symbol name escaping and benchmark its performance and usability for valid string serialization.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4716#issuecomment-5059238940) **jakebailey** said "@typescript-bot perf test this"
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4716#issuecomment-5059239589) **typescript-automation[bot]** reported that performance tests started and provided status links
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4716#issuecomment-5059531138) **typescript-automation[bot]** reported the perf run results requested by jakebailey
 * **jakebailey** added label `Unmigrated PR`

### [PR microsoft/TypeScript-go#4721](https://github.com/microsoft/TypeScript-go/pull/4721) (Closed, **jakebailey**, **Copilot**)

**Honor ts\-ignore directives on multiline JSX in dependencies**

*Extend ts-ignore directive matching to properly suppress multiline JSX attribute errors in dependency source files.*

 * created by **Copilot**
 * (3 weeks ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4721#issuecomment-5296527707) **jakebailey** said "Hopefully we don't need this"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4726](https://github.com/microsoft/TypeScript-go/pull/4726) (Open)

**Skip declaration emit without a prior signature**

*Skip emitting TypeScript declaration files for declarations that lack an existing signature*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4726#issuecomment-5297614746) **jakebailey** said "@typescript-bot perf test this"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4726#issuecomment-5297615606) **typescript-automation[bot]** reported that the performance test job started and provided status and results links
 * [today](https://github.com/microsoft/TypeScript-go/pull/4726#issuecomment-5297865842) **typescript-automation[bot]** posted the performance run results for the requested comparison

### [PR microsoft/TypeScript-go#4729](https://github.com/microsoft/TypeScript-go/pull/4729) (Closed)

**add android prebuilt binary support**

*Add Android prebuilt binary support by requiring the Android NDK in PATH and hardcoding the nativePreviewReleaseVersion to build all targets.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4729#issuecomment-5073026810) **jakebailey** said ""portable" to us meant "we can port our code to it", because our TS was structurally similar to Go. Has nothing to do with platform specific code."
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4729#issuecomment-5073653412) **robertkirkman** explained that building the Go binary so its file output matches the given ELF 64-bit LSB shared object for ARM aarch64 built by NDK r29 will work properly
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4729#issuecomment-5073663868) **jakebailey** said "I don't think it's required; I am putting up another PR that's the simplified version of this which perhaps you all could check. But, it'll only work for arm64."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4730](https://github.com/microsoft/TypeScript-go/pull/4730) (Closed, `dependencies`, `javascript`)

**Bump linkify\-it from 5\.0\.1 to 5\.0\.2**

*Upgrade linkify-it dependency from 5.0.1 to 5.0.2 to fix a mailto: DoS issue and enforce user/pass length limits.*

 * (3 weeks ago) **dependabot[bot]** added labels `javascript`, `dependencies`, `javascript`
 * (today) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/4730#issuecomment-5298283286) **dependabot[bot]** explained how to ignore dependency update notifications or reopen the PR to resolve conflicts

### [PR microsoft/TypeScript-go#4733](https://github.com/microsoft/TypeScript-go/pull/4733) (Open, `Unmigrated PR`)

**Add wasip1 npm build target**

*Add a wasip1 npm build target that assumes external mounting of lib.d.ts files rather than bundling them in the binary.*

 * created by **jakebailey**
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4733#issuecomment-5073968665) **jakebailey** said "wasip1 lacks os.Executable, so this breaks, currently."
 * **jakebailey** added label `Unmigrated PR`

### [PR microsoft/TypeScript-go#4734](https://github.com/microsoft/TypeScript-go/pull/4734) (Closed)

**Add Android ARM64 release target**

*Add Android ARM64 release target to the build configuration*

 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/4734#issuecomment-5271186367) **sylirre** said "https://github.com/microsoft/typescript-go/issues/4718 will be resolved on the proot side in pending release."
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4734#issuecomment-5287189401) **jakebailey** said "Ok, I have this PR where I want it, besides the artifact uploading. If you can, please test it before I remove the artifact stuff and go for a merge."
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4734#issuecomment-5288657980) **robertkirkman** said "I have tested this again, and it continues to work as expected in both F-Droid Termux and Google Play Termux."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4756](https://github.com/microsoft/TypeScript-go/pull/4756) (Closed, `dependencies`, `github_actions`)

**Bump the github\-actions group across 1 directory with 5 updates**

*Bump five GitHub Actions dependencies in the root directory, updating checkout, setup-node, and CodeQL actions.*

 * (2 weeks ago) **dependabot[bot]** added labels `github_actions`, `dependencies`, `github_actions`
 * (today) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/4756#issuecomment-5298283370) **dependabot[bot]** notified that closing the pull request will not ignore dependencies in future and directed to configure ignore rules in dependabot.yml

### [PR microsoft/TypeScript-go#4767](https://github.com/microsoft/TypeScript-go/pull/4767) (Closed)

**Fix package ID collisions for remapped inputs**

*Fix package ID collisions by ensuring remapped input references like “set” are correctly resolved instead of mapping to “get”.*

 * created by **jakebailey**
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4767#issuecomment-5095394442) **jakebailey** said "I might have been bamboozled, I think this bug only happens if packageDirectory is / which the test case can make happen, but is very likely not reality for the real repro."
 * (today) **jakebailey** closed the issue

