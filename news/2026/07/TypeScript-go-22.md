# Report for 2026-07-22 (Wednesday, July 22nd, 2026)

18 different users commented on 41 different issues.

## Recommended Actions

 * Response Recommended
    * @robertkirkman provided a summary of ELF binary performance and compatibility on Android in [microsoft/TypeScript-go#2424](https://github.com/microsoft/TypeScript-go/issues/2424#issuecomment-5058178699)
    * @pedroGoffi provided details about tsconfig usage and linting behavior in [microsoft/TypeScript-go#4587](https://github.com/microsoft/TypeScript-go/issues/4587#issuecomment-5054801963)
    * @lukesandberg asked if signal handlers should be removed given that interruption reports success in watch mode in [microsoft/TypeScript-go#4592](https://github.com/microsoft/TypeScript-go/pull/4592#issuecomment-5049741466)
    * @calvinrp provided follow-up details on the shim crash and filed issue #4706 for the LSP mode hang in [microsoft/TypeScript-go#4633](https://github.com/microsoft/TypeScript-go/issues/4633#issuecomment-5048946486)
    * @typescript-automation[bot] provided perf run results as requested in [microsoft/TypeScript-go#4703](https://github.com/microsoft/TypeScript-go/pull/4703#issuecomment-5058758042)
    * @typescript-automation[bot] reported performance run results in [microsoft/TypeScript-go#4711](https://github.com/microsoft/TypeScript-go/pull/4711#issuecomment-5053180468)
    * @mikearnaldi asked whether the limitations of Emit were temporary or intentional in [microsoft/TypeScript-go#4712](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5056997160)
    * @typescript-automation[bot] provided perf run results as requested in [microsoft/TypeScript-go#4716](https://github.com/microsoft/TypeScript-go/pull/4716#issuecomment-5059531138)

## Activity Summary

### [Issue microsoft/TypeScript-go#2424](https://github.com/microsoft/TypeScript-go/issues/2424) (Closed, `possible improvement`)

**Request for support for additional architectures**

*Support and a roadmap are requested for riscv64, ppc64le, and loong64 architectures in typescript-go.*

 * [1 month ago](https://github.com/microsoft/TypeScript-go/issues/2424#issuecomment-4748935526) **darkyzhou** said "Thanks!"
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/2424#issuecomment-4954972211) **dannycreations** asked about Android platform support for Termux after encountering a TypeScript resolution error
 * [today](https://github.com/microsoft/TypeScript-go/issues/2424#issuecomment-5047903008) **jakebailey** said "Interesting; I didn't realize that node / android would actually select something different than linux. We can probably do that."
 * [later](https://github.com/microsoft/TypeScript-go/issues/2424#issuecomment-5058178699) **robertkirkman** explained compatibility and performance trade-offs of various Linux ELF binary linking strategies on Android via Termux

### [Issue microsoft/TypeScript-go#2824](https://github.com/microsoft/TypeScript-go/issues/2824) (Open, `Domain: API and Extensibility`, **andrewbranch**)

**API usage patterns for complex editor extensions**

*Exploring IPC-based API features for a Go TS server to replace TS Server plugins and support Vue editor extensions*

 * [6 days ago](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-4994605079) **andrewbranch** said "https://github.com/microsoft/typescript/issues/45886 is basically that."
 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-5004116575) **shining-mind** asked if the proposal should be moved to the typescript-go repo
 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-5005913332) **andrewbranch** said "No, development will move back to microsoft/TypeScript soon and typescript-go will be archived."
 * [today](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-5054092971) **andrewbranch** said "@johnsoncodehk, @remcohaszing, @dummdidumm, and anyone else working on this kind of ecosystem tooling: I would really appreciate your input on #4712."

### [PR microsoft/TypeScript-go#3616](https://github.com/microsoft/TypeScript-go/pull/3616) (Closed, `No linked issue`)

**API \`emit\` support to generate \.d\.ts / \.js files from sources**

*Expose compiler emit in TSGO API and TypeScript client to generate .js and .d.ts files using virtual FS*

 * (9 weeks ago) **RyanCavanaugh** added label `No linked issue`, and set milestone to `Possible Improvement`
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3616#issuecomment-4892435405) **pfumagalli** said "Updated and resolved conflicts with upstream..."
 * [later](https://github.com/microsoft/TypeScript-go/pull/3616#issuecomment-5060354541) **pfumagalli** said "Picked up by @andrewbranch in #4699 , closing this one as it's obsolete!"
 * (later) **pfumagalli** closed the issue

### [PR microsoft/TypeScript-go#4329](https://github.com/microsoft/TypeScript-go/pull/4329) (Closed)

**Paged link stores with fallback from array to map representation**

*Optimize paged link stores by using fixed-size array pages with map fallback and streamlined link storage*

 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4329#issuecomment-4713101324) **jakebailey** said "@typescript-bot perf test this faster"
 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4329#issuecomment-4713101617) **typescript-automation[bot]** reported that performance tests had started and provided status and result links
 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4329#issuecomment-4713246884) **typescript-automation[bot]** provided the requested performance run results comparing baseline to PR
 * [today](https://github.com/microsoft/TypeScript-go/pull/4329#issuecomment-5048542236) **ahejlsberg** said "Latest commit hardens implementation for 32-bit architectures and automatically switches between page list and page map based on magnitude of key values."
 * [today](https://github.com/microsoft/TypeScript-go/pull/4329#issuecomment-5048546801) **ahejlsberg** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4329#issuecomment-5048547421) **typescript-automation[bot]** noted that build jobs started and provided links to their status and results
 * [today](https://github.com/microsoft/TypeScript-go/pull/4329#issuecomment-5048814887) **typescript-automation[bot]** posted the requested performance run results including a comparison report of baseline vs PR metrics
 * [today](https://github.com/microsoft/TypeScript-go/pull/4329#issuecomment-5048922849) **jakebailey** said "LGTM but the two copilot comments I believe are accurate."
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#4557](https://github.com/microsoft/TypeScript-go/pull/4557) (Open)

**Get incremental mode closer to Strada**

*Align tsgo's incremental build file tracking and performance reporting with tsc's Strada mode to fix accounting mismatches.*

 * created by **jakebailey**
 * (later) **jakebailey** closed the issue
 * (later) **jakebailey** reopened the issue

### [Issue microsoft/TypeScript-go#4571](https://github.com/microsoft/TypeScript-go/issues/4571) (Closed, `Domain: Editor`, **RyanCavanaugh**, **Copilot**)

**Organize imports command doesn't respect tabSize/insertSpaces settings**

*Organize imports always uses a four-space indent for multiline named imports instead of honoring tabSize and insertSpaces settings*

 * (5 days ago) **RyanCavanaugh** set milestone to `TypeScript 7.1`, and assigned to **Copilot**, **RyanCavanaugh**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4572](https://github.com/microsoft/TypeScript-go/issues/4572) (Closed, `Needs Investigation`, **ahejlsberg**)

**Overloaded assertion in inferred\-return function expression loses destructured discriminant narrowing**

*An overloaded assert in an arrow function without a return type annotation prevents TypeScript from narrowing a destructured discriminant property.*

 * (1 week ago) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.1`, and assigned to **ahejlsberg**
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#4587](https://github.com/microsoft/TypeScript-go/issues/4587) (Closed, `Needs More Info`, **weswigham**)

**TSX files do not report TypeScript diagnostics, while TS files work correctly \(autocomplete still works\)**

*Enabling tsgo in VS Code’s TypeScript 7 extension causes .tsx files to omit diagnostics while .ts files report errors normally.*

 * **weswigham** added label `Needs More Info`
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/4587#issuecomment-5037332201) **weswigham** explained that the behavior was working as intended and not new, and noted that the issue report lacked standalone reproduction details
 * [today](https://github.com/microsoft/TypeScript-go/issues/4587#issuecomment-5047689267) **elramus** clarified that the issue was caused by a user setting disabling validation and apologized for the false alarm
 * (today) **weswigham** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/issues/4587#issuecomment-5054801963) **pedroGoffi** said "used the same tsconfig for both everything was inside project include, but the linting was working only in the .ts files tho"

### [PR microsoft/TypeScript-go#4592](https://github.com/microsoft/TypeScript-go/pull/4592) (Open)

**Improve responsiveness of \`tsc build\` to interruption**

*Enhance tsc build responsiveness to SIGINT and SIGTERM by threading cancellation contexts through compilation, exiting with proper codes, and adding tests.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4592#issuecomment-4939791695) **lukesandberg** said "@microsoft-github-policy-service agree [company="Vercel"]"
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4592#issuecomment-4939873881) **lukesandberg** agreed that the company was Vercel
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4592#issuecomment-5036518306) **jakebailey** questioned whether Ctrl+C was handled previously or was unhandled in the old compiler
 * [today](https://github.com/microsoft/TypeScript-go/pull/4592#issuecomment-5049741466) **lukesandberg** asked if Ctrl+C was handled by default in the old compiler and suggested removing the signal handlers given that interruption reports success in watch mode

### [PR microsoft/TypeScript-go#4602](https://github.com/microsoft/TypeScript-go/pull/4602) (Closed)

**fix\(lsp\): respect editor formatting in organize imports**

*Update the organize imports function to apply the editor's tabSize and indentation settings.*

 * created by **TorinAsakura**
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4602#issuecomment-4942220540) **jakebailey** questioned why the existing code using LS formatting options did not work and why patching the LSP with middlewares was necessary
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4602#issuecomment-4946957648) **TorinAsakura** noted that the custom plumbing was unnecessary and said they would strip it out, keeping only the small fix and regression test
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4606](https://github.com/microsoft/TypeScript-go/pull/4606) (Closed, **ahejlsberg**)

**Keep dependent destructuring narrowing during re\-entrant checks**

*Preserve dependent destructuring type narrowing across re-entrant type-checking operations.*

 * created by **Andarist**
 * **RyanCavanaugh** assigned to **ahejlsberg**
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#4613](https://github.com/microsoft/TypeScript-go/issues/4613) (Closed, `bug`, **ahejlsberg**)

**Exhaustive switch on co\-narrowed tuple's \`\.length\` does not terminate fallthrough control flow \(works in TS 6\.0\)**

*TypeScript 7.0 misidentifies an exhaustive inner switch on a co-narrowed tuple’s length as non-terminating, leading to incorrect type inference.*

 * (1 week ago) **RyanCavanaugh** added label `bug`, set milestone to `TypeScript 7.1`, and assigned to **ahejlsberg**
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#4618](https://github.com/microsoft/TypeScript-go/issues/4618) (Open, `Domain: Editor`, **jakebailey**, **Copilot**)

**Some imports are not updated after a file rename, in composite projects**

*TypeScript 7 composite projects do not update imports in unloaded subprojects when renaming files, unlike TypeScript 6.*

 * **pascalspadone** added label `Domain: Editor`
 * (yesterday) **jakebailey** assigned to **Copilot**, **jakebailey**
 * **RyanCavanaugh** added to milestone `Post-7.0`

### [Issue microsoft/TypeScript-go#4633](https://github.com/microsoft/TypeScript-go/issues/4633) (Open, `Needs Investigation`, **jakebailey**)

**Publish an official wasip1 \(WASI\) build artifact of tsgo**

*Publish an official Go WASI (wasip1) WebAssembly build artifact of tsgo alongside native binaries in releases.*

 * **RyanCavanaugh** added to milestone `Possible Improvement`
 * [today](https://github.com/microsoft/TypeScript-go/issues/4633#issuecomment-5047893676) **jakebailey** asked about the expectation for distributing a .wasm file on npm, noted that special-casing it is feasible as esbuild does, and suggested falling back to Node's WASI shim when no native binary exists despite observed crashes
 * [today](https://github.com/microsoft/TypeScript-go/issues/4633#issuecomment-5048059112) **calvinrp** proposed publishing a versioned .wasm package per release and adding CI-built artifacts, and suggested decoupling the Node WASI-shim fallback as a separate issue
 * [today](https://github.com/microsoft/TypeScript-go/issues/4633#issuecomment-5048946486) **calvinrp** followed up on the shim crash, explained that it was a Node bug fixed in Node 23+, confirmed that the fallback works under node >= 23, and reported that the LSP mode hang was a tsgo-side issue filed as #4706

### [PR microsoft/TypeScript-go#4660](https://github.com/microsoft/TypeScript-go/pull/4660) (Closed, **DanielRosenwasser**, **Copilot**)

**Respect configured TypeScript diagnostic locale**

*Respect js/ts.locale and typescript.locale overrides for TypeScript diagnostics, restart the language server on changes, and fallback to auto display language.*

 * (6 days ago) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4660#issuecomment-5035657322) **jakebailey** said "Maybe it's cleaner to just have a Client hook that sets the current locale, and we update that on user pref change and plumb it that way?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4660#issuecomment-5052112712) **DanielRosenwasser** said "Sure, @copilot do what Jake suggested."
 * [today](https://github.com/microsoft/TypeScript-go/pull/4660#issuecomment-5052157543) **Copilot** implemented locale resolution once in Client.start(), passed it to NativePreviewLanguageClient, optimized getLocale(), and ensured client restart picks up locale changes
 * [today](https://github.com/microsoft/TypeScript-go/pull/4660#issuecomment-5053242677) **jakebailey** said "It didn't understand what I said, I meant the Client in the server, as in project.Client"

### [Issue microsoft/TypeScript-go#4664](https://github.com/microsoft/TypeScript-go/issues/4664) (Closed, `Needs Investigation`, **johnfav03**)

**\`tsgo \-\-build\` incremental reports no errors after a dependency update batch that includes a global\-scope \.d\.ts change \(clean build errors\)**

*tsgo --build incremental mode fails to report newly introduced type errors after updating dependencies including a global-scope .d.ts change*

 * created by **martijnwalraven**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `Post-7.0`, and assigned to **johnfav03**
 * (later) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4665](https://github.com/microsoft/TypeScript-go/pull/4665) (Closed)

**Return all files from getFilesAffectedBy when a changed file affects global scope**

*Update getFilesAffectedBy to return all non-default-library files for global-scope changes to fix incremental invalidation.*

 * created by **martijnwalraven**
 * [5 days ago](https://github.com/microsoft/TypeScript-go/pull/4665#issuecomment-5001814259) **martijnwalraven** said "@microsoft-github-policy-service agree"
 * (later) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4668](https://github.com/microsoft/TypeScript-go/pull/4668) (Closed, **RyanCavanaugh**, **Copilot**)

**Respect editor tab/space settings when parsing formatting prefs used by organize imports**

*Map editor tabSize and insertSpaces settings to formatting indentSize and convertTabsToSpaces so organizeImports honors editor indentation preferences.*

 * (5 days ago) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4668#issuecomment-5035895275) **jakebailey** said "This is identical to #4602"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#4678](https://github.com/microsoft/TypeScript-go/issues/4678) (Closed, `Working As Intended`, **RyanCavanaugh**, **Copilot**)

**skipLibCheck doesn't suppress TS2320 "cannot simultaneously extend" for module augmentation of a \`\.d\.ts\` interface \(repro has no any\)**

*skipLibCheck:true does not suppress TS2320 cannot simultaneously extend errors during module augmentation of a .d.ts interface.*

 * (yesterday) **RyanCavanaugh** added label `Working As Intended`, and assigned to **Copilot**, **RyanCavanaugh**
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#4681](https://github.com/microsoft/TypeScript-go/issues/4681) (Closed, `duplicate`)

**skipLibCheck doesn't suppress TS18042/TS2693 when a \.d\.ts's own export = points to a type instead of a value**

*skipLibCheck does not prevent tsgo from reporting TS18042 and TS2693 errors when a .d.ts file’s export= incorrectly refers to a type instead of a value.*

 * created by **valentinmelusson**
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/4681#issuecomment-5039618337) **RyanCavanaugh** said "Same answer as #4678"
 * **RyanCavanaugh** added label `duplicate`
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#4693](https://github.com/microsoft/TypeScript-go/pull/4693) (Closed, **RyanCavanaugh**, **Copilot**)

**Add regression test for TS7030 false positive with never\-returning function in switch default**

*Add regression tests verifying that calls to never-returning functions in switch defaults don't trigger TS7030 errors*

 * created by **Copilot**
 * (yesterday) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#4698](https://github.com/microsoft/TypeScript-go/pull/4698) (Closed, **RyanCavanaugh**, **Copilot**)

**Document and lock in TS7 skipLibCheck behavior for merged\-interface heritage conflicts**

*Document and enforce TS7 skipLibCheck behavior retaining TS2320 errors for merged-interface heritage conflicts involving user augmentations*

 * created by **Copilot**
 * (yesterday) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4698#issuecomment-5048754347) **Copilot** addressed the feedback by removing the testcase and associated baselines and keeping only the CHANGES.md edit
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#4699](https://github.com/microsoft/TypeScript-go/pull/4699) (Closed)

**API emit**

*Add program.emit, program.emitToString, getJavaScriptEmit, and getDeclarationEmit methods for flexible file system and in-memory emissions.*

 * created by **andrewbranch**
 * [later](https://github.com/microsoft/TypeScript-go/pull/4699#issuecomment-5056103727) **pfumagalli** said "@andrewbranch, shall I then close #3616 as it's incorporated into this one? So looking forward for this to hit the registries!!!"
 * [later](https://github.com/microsoft/TypeScript-go/pull/4699#issuecomment-5059826896) **andrewbranch** said "@pfumagalli yes, go ahead, thanks!"

### [PR microsoft/TypeScript-go#4703](https://github.com/microsoft/TypeScript-go/pull/4703) (Open)

**Store value symbol links inline on checker\-created symbols**

*Value symbol links for checker-created symbols are stored inline to eliminate paged store overhead and improve check performance.*

 * [today](https://github.com/microsoft/TypeScript-go/pull/4703#issuecomment-5045300017) **jakebailey** said "@typescript-bot perf test this"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4703#issuecomment-5045301019) **typescript-automation[bot]** reported that perf test jobs had started and provided links to build and result statuses
 * [today](https://github.com/microsoft/TypeScript-go/pull/4703#issuecomment-5045689255) **typescript-automation[bot]** provided perf run results to @jakebailey
 * [later](https://github.com/microsoft/TypeScript-go/pull/4703#issuecomment-5058461229) **jakebailey** said "@typescript-bot perf test this"
 * [later](https://github.com/microsoft/TypeScript-go/pull/4703#issuecomment-5058461902) **typescript-automation[bot]** reported build jobs starting and provided status and results links
 * [later](https://github.com/microsoft/TypeScript-go/pull/4703#issuecomment-5058758042) **typescript-automation[bot]** reported the performance run results as requested by jakebailey
 * [later](https://github.com/microsoft/TypeScript-go/pull/4703#issuecomment-5059253316) **jakebailey** said "Seems like it's in the noise?"

### [Issue microsoft/TypeScript-go#4704](https://github.com/microsoft/TypeScript-go/issues/4704) (Closed)

**\`new super\(\)\` in static method does not cause error**

*new super() in static methods or blocks is incorrectly allowed without error instead of being flagged as invalid*

 * created by **Withered-Flower-0422**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4704#issuecomment-5048719524) **RyanCavanaugh** said "We can continue tracking this at the linked issue. Thanks!"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#4705](https://github.com/microsoft/TypeScript-go/issues/4705) (Open, `Domain: API and Extensibility`, **andrewbranch**)

**\`hasTrailingComma\` property is not implemented in \`RemoteNodeList\` class in the API**

*The RemoteNodeList class in the API declares a hasTrailingComma property that is never assigned or implemented.*

 * created by **mrazauskas**
 * (today) **RyanCavanaugh** set milestone to `Post-7.0`, and assigned to **andrewbranch**
 * **andrewbranch** added label `Domain: API and Extensibility`

### [Issue microsoft/TypeScript-go#4706](https://github.com/microsoft/TypeScript-go/issues/4706) (Open)

**wasip1: LSP over node:wasi hangs after \`initialize\` — signal watcher starves the scheduler \(fix included\)**

*The wasip1-built LSP server on Node WASI hangs after initialize because its signal-watcher busy-spins; skipping signal.NotifyContext on wasip1 fixes this.*

 * created by **calvinrp**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4706#issuecomment-5048976529) **jakebailey** said "By all means, send a PR with this change; I definitely have similar changes locally"

### [PR microsoft/TypeScript-go#4707](https://github.com/microsoft/TypeScript-go/pull/4707) (Closed)

**Describe downstream impact of consistent decl errors under skipLibCheck**

*Explain how consistent declaration errors under skipLibCheck affect downstream code and builds.*

 * created by **RyanCavanaugh**
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#4708](https://github.com/microsoft/TypeScript-go/pull/4708) (Closed)

**Add lint rule for identifying common patterns in the checker that lead to inconsistent diagnostic output**

*Add a lint rule to detect and fix inherited TS-1 diagnostic inconsistencies by always checking children for consistent error reporting*

 * created by **weswigham**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4708#issuecomment-5053743000) **jakebailey** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4708#issuecomment-5053743419) **typescript-automation[bot]** posted CI job status updates with links for test top400 and perf test this faster
 * [today](https://github.com/microsoft/TypeScript-go/pull/4708#issuecomment-5053877415) **typescript-automation[bot]** posted the requested performance run results
 * [today](https://github.com/microsoft/TypeScript-go/pull/4708#issuecomment-5054169607) **typescript-automation[bot]** reported that running tsc on the top 400 repos comparing main and the PR merge returned no issues

### [Issue microsoft/TypeScript-go#4709](https://github.com/microsoft/TypeScript-go/issues/4709) (Open)

**\`javascript\.validation\.enabled\` editor setting controls typescript validation as well**

*Disabling JavaScript validation also disables TypeScript validation unintentionally due to unified configuration handling.*

 * created by **weswigham**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4709#issuecomment-5051455317) **jakebailey** said "Yeah, so the fix here is going to be to start doing language-scoped settings, but I think we could probably special case just this one thing?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/4709#issuecomment-5051660283) **weswigham** said "IMO, this and format.enabled are the big "wait, why do these toggle unexpected file extensions, too"."

### [PR microsoft/TypeScript-go#4710](https://github.com/microsoft/TypeScript-go/pull/4710) (Open)

**Add an LSP boot flag that enables flaky diagnostics tracking**

*Add an LSP init flag and JS/TS setting to track and optionally panic or log flaky diagnostics.*

 * created by **weswigham**

### [PR microsoft/TypeScript-go#4711](https://github.com/microsoft/TypeScript-go/pull/4711) (Closed)

**Optimize \`getAssignmentReducedType\` in CFA**

*Optimize getAssignmentReducedType to eliminate quadratic performance when processing large union types in control flow analysis.*

 * created by **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4711#issuecomment-5053052193) **ahejlsberg** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4711#issuecomment-5053052636) **typescript-automation[bot]** posted an automated status update showing CI job progress
 * [today](https://github.com/microsoft/TypeScript-go/pull/4711#issuecomment-5053180468) **typescript-automation[bot]** provided performance run results as requested
 * [today](https://github.com/microsoft/TypeScript-go/pull/4711#issuecomment-5053241532) **ahejlsberg** said "Nice win in compiler-unions test, which does indeed contain a number of large unions that are reduced by other large unions in CFA."
 * [today](https://github.com/microsoft/TypeScript-go/pull/4711#issuecomment-5053422688) **typescript-automation[bot]** reported results of running the top 400 repos with tsc and found everything looked good
 * (later) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#4712](https://github.com/microsoft/TypeScript-go/pull/4712) (Open)

**Content mappers**

*Add support for external content mapper packages in TypeScript configuration to transform unsupported file types into valid TypeScript syntax.*

 * created by **andrewbranch**
 * [later](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5056511449) **nikelborm** said "Hi, @ryanrasti, I think this would land perfectly for your typenix project"
 * [later](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5056997160) **mikearnaldi** said "Are the limitations of Emit temporary or intentional? it would be helpful to have TS emit both JS and mapped declarations so one could build foo.X to foo.d.ts / foo.js"
 * [later](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5059453768) **andrewbranch** asked for real-world use cases before lifting the limitation, suggested using --rewriteRelativeImportExtensions, and noted that TS content in Vue components may not produce useful JS output

### [Issue microsoft/TypeScript-go#4713](https://github.com/microsoft/TypeScript-go/issues/4713) (Open)

**tsconfig/jsconfig diagnostic doesn't refresh after file saved**

*tsgo fails to refresh tsconfig/jsconfig diagnostics after saving compilerOptions changes.*

 * created by **sharpchen**

### [PR microsoft/TypeScript-go#4714](https://github.com/microsoft/TypeScript-go/pull/4714) (Open)

**feat\(47595\): allow using private fields in type queries**

*Enable referencing private class fields in TypeScript type queries.*

 * created by **a-tarasyuk**

### [Issue microsoft/TypeScript-go#4715](https://github.com/microsoft/TypeScript-go/issues/4715) (Open, **jakebailey**)

**Request for support for Android**

*Enable straightforward installation and execution of the TypeScript compiler via npm in Android Termux without extra workarounds*

 * created by **robertkirkman**
 * **jakebailey** assigned to **jakebailey**

### [PR microsoft/TypeScript-go#4716](https://github.com/microsoft/TypeScript-go/pull/4716) (Open)

**Restore Strada\-style escaped symbol names**

*Revert to Strada-style symbol name escaping and benchmark its performance and usability for valid string serialization.*

 * created by **jakebailey**
 * [later](https://github.com/microsoft/TypeScript-go/pull/4716#issuecomment-5059238940) **jakebailey** said "@typescript-bot perf test this"
 * [later](https://github.com/microsoft/TypeScript-go/pull/4716#issuecomment-5059239589) **typescript-automation[bot]** reported that performance tests started and provided status links
 * [later](https://github.com/microsoft/TypeScript-go/pull/4716#issuecomment-5059531138) **typescript-automation[bot]** reported the perf run results requested by jakebailey

### [PR microsoft/TypeScript-go#4717](https://github.com/microsoft/TypeScript-go/pull/4717) (Closed)

**bundled/nativepath: survive kernel\-reported paths that the process cannot see \(PRoot link2symlink\)**

*tsgo crashes and fails module resolution inside PRoot's link2symlink environment due to inaccessible kernel-reported paths.*

 * created by **dlecan**
 * [later](https://github.com/microsoft/TypeScript-go/pull/4717#issuecomment-5059907205) **jakebailey** questioned the explanation's clarity and asked why an issue wasn't filed first
 * [later](https://github.com/microsoft/TypeScript-go/pull/4717#issuecomment-5059950310) **dlecan** said "@microsoft-github-policy-service agree"
 * [later](https://github.com/microsoft/TypeScript-go/pull/4717#issuecomment-5060234733) **dlecan** apologized for going straight to the PR, filed issue #4718 and rewrote the PR description; clarified the trust-but-verify approach using /proc/self/fd with a POSIX fallback and noted the bundled change mirrors a previous Windows fix; said they would address inline comments

### [Issue microsoft/TypeScript-go#4718](https://github.com/microsoft/TypeScript-go/issues/4718) (Open)

**Panic at startup and mass module\-resolution failures under PRoot link2symlink \(Termux proot\-distro on Android\)**

*TypeScript 7's compiler fails with panic and module-resolution errors under Termux PRoot link2symlink due to broken path handling*

 * created by **dlecan**

