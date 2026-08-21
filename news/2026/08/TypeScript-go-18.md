# Report for 2026-08-18 (Tuesday, August 18th, 2026)

13 different users commented on 42 different issues.

## Recommended Actions

 * Response Recommended
    * @typescript-automation[bot] provided perf run results in [microsoft/TypeScript-go#4596](https://github.com/microsoft/TypeScript-go/pull/4596#issuecomment-5333925721)
    * @typescript-automation[bot] asked to review tsc comparison results and investigate the highlighted errors in [microsoft/TypeScript-go#4596](https://github.com/microsoft/TypeScript-go/pull/4596#issuecomment-5334466683)
    * @remcohaszing suggested adding a shorthand option '-x' for execute external in [microsoft/TypeScript-go#4712](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5339365820)
    * @nikeedw asked for a CI approval run in [microsoft/TypeScript-go#4846](https://github.com/microsoft/TypeScript-go/pull/4846#issuecomment-5340578727)
    * @typescript-automation provided performance run results as requested in [microsoft/TypeScript-go#4900](https://github.com/microsoft/TypeScript-go/pull/4900#issuecomment-5336853630)

## Activity Summary

### [PR microsoft/TypeScript-go#3630](https://github.com/microsoft/TypeScript-go/pull/3630) (Closed, **DanielRosenwasser**, **Copilot**)

**Fix formatting failure when whitespace\-only line exists between single\-line comments**

*Ensure startPos only advances to fix formatting failures when whitespace-only lines occur between single-line comments.*

 * [14 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3630#issuecomment-4400770306) **DanielRosenwasser** said "@copilot investigate and make sure we are testing variations of TrimTrailingWhitespace for this"
 * [14 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3630#issuecomment-4400890083) **Copilot** added a test variant that disables TrimTrailingWhitespace and verified whitespace preservation; confirmed both variations pass
 * **RyanCavanaugh** added to milestone `Post-7.0`
 * [today](https://github.com/microsoft/TypeScript-go/pull/3630#issuecomment-5333724706) **DanielRosenwasser** said "Let's just port the original bug to the new repo and see if we can get a fix later."
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#3690](https://github.com/microsoft/TypeScript-go/pull/3690) (Closed, `Unmigrated PR`)

**fix: handle symlink workspace roots in project reference redirects**

*Ensure project reference redirects correctly resolve symlinked workspace roots in TypeScript*

 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3690#issuecomment-5321189158) **jakebailey** said "I tested this and yeah, https://github.com/microsoft/TypeScript/issues/63819#issuecomment-4408371311 is correct, this adds a lot of realpath checks that I think we need to be caching"
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3690#issuecomment-5321197739) **jakebailey** described asking Copilot locally to implement the parent directory realpath cache, noted it worked well, and suggested reopening on the main TS repo if this repo closes first
 * **jakebailey** added label `Unmigrated PR`
 * [today](https://github.com/microsoft/TypeScript-go/pull/3690#issuecomment-5332256532) **jakebailey** shared a diff patch that added a realpathDirectoryCache field to projectReferenceParser and initialized it in initMapper

### [PR microsoft/TypeScript-go#3726](https://github.com/microsoft/TypeScript-go/pull/3726) (Closed, `Unmigrated PR`, **DanielRosenwasser**, **Copilot**)

**Preserve original stack traces in cross\-project panic handling**

*Add PanicWithStack to wrap and re-panic panics with their original stack traces in cross-project goroutine recovery for accurate logging.*

 * [1 month ago](https://github.com/microsoft/TypeScript-go/pull/3726#issuecomment-5005763801) **RyanCavanaugh** said "Just doing some Copilot testing here, please ignore reviews"
 * (4 days ago) **jakebailey** closed the issue
 * (4 days ago) **jakebailey** reopened the issue
 * **RyanCavanaugh** added label `Unmigrated PR`

### [PR microsoft/TypeScript-go#3826](https://github.com/microsoft/TypeScript-go/pull/3826) (Closed, `No linked issue`)

**Add version & a common session identifier to events from LS clients**

*Include version and common session ID in language server client events to improve version-specific error tracking and correlate diagnostics.*

 * [13 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3826#issuecomment-4444367810) **DanielRosenwasser** noted no indication that dotted names are illegal for end users and acknowledged possible error
 * (10 weeks ago) **RyanCavanaugh** added label `No linked issue`, and set milestone to `Possible Improvement`
 * [today](https://github.com/microsoft/TypeScript-go/pull/3826#issuecomment-5333876397) **DanielRosenwasser** said "I'm not merging this one in in time for the repo move, but we should do it."
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#3996](https://github.com/microsoft/TypeScript-go/pull/3996) (Closed, `No linked issue`, `Unmigrated PR`)

**Extract tscInput tests to individual per\-scenario files with imperative edits to improve debuggability**

*Extract tscInput tests into individual scenario files with imperative edits, remove intra-test parallelism, simplify debugging while preserving original tests.*

 * [12 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3996#issuecomment-4500751011) **weswigham** asked if others preferred keeping test duplication for debuggability or the new test format and offered to delete originals and the extraction script
 * (10 weeks ago) **RyanCavanaugh** added label `No linked issue`, and set milestone to `Possible Improvement`
 * **RyanCavanaugh** added label `Unmigrated PR`

### [PR microsoft/TypeScript-go#4102](https://github.com/microsoft/TypeScript-go/pull/4102) (Closed, `Unmigrated PR`)

**Cache alias candidates for symbol accessibility**

*Cache alias candidate symbols to speed up symbol accessibility checks*

 * [4 days ago](https://github.com/microsoft/TypeScript-go/pull/4102#issuecomment-5298327583) **jakebailey** said "@typescript-bot perf test this faster"
 * [4 days ago](https://github.com/microsoft/TypeScript-go/pull/4102#issuecomment-5298328172) **typescript-automation[bot]** posted a build status update with job start and result links
 * [4 days ago](https://github.com/microsoft/TypeScript-go/pull/4102#issuecomment-5298557303) **typescript-automation[bot]** provided the requested performance run results in a detailed report
 * **RyanCavanaugh** added label `Unmigrated PR`

### [PR microsoft/TypeScript-go#4200](https://github.com/microsoft/TypeScript-go/pull/4200) (Closed, `Unmigrated PR`)

**Negated Types**

*Introduce 'not T' negated types to capture type complements and preserve conditional false-branch information for improved control flow analysis.*

 * created by **weswigham**
 * **RyanCavanaugh** added label `Unmigrated PR`

### [PR microsoft/TypeScript-go#4248](https://github.com/microsoft/TypeScript-go/pull/4248) (Closed, **DanielRosenwasser**, **Copilot**)

**Fix fatal panic on non\-absolute path in VFS**

*Update VFS RootLength, SplitPath, and RootAndPath to return defaults for non-absolute paths instead of panicking.*

 * [10 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4248#issuecomment-4662531216) **Copilot** investigated compiler and fourslash test normalization and determined that no real-world test could reproduce the panic without giving false confidence
 * (yesterday) **jakebailey** closed the issue
 * (yesterday) **jakebailey** reopened the issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/4248#issuecomment-5333882705) **DanielRosenwasser** said "Can't fix this in time for the repo move."
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#4336](https://github.com/microsoft/TypeScript-go/pull/4336) (Closed, **jakebailey**, **Copilot**)

**Fix JS declaration emit for dangling top\-level block comments**

*Use NotEmittedStatement nodes to preserve dangling top-level block comments in TypeScript declaration output, including CommonJS modules.*

 * **Copilot** assigned to **jakebailey**
 * **RyanCavanaugh** added to milestone `Post-7.0`
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4336#issuecomment-5318280872) **jakebailey** prompted Copilot to think better and threatened to discard the PR if it didn’t work
 * [today](https://github.com/microsoft/TypeScript-go/pull/4336#issuecomment-5334718196) **jakebailey** said "Let's just defer this for now"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4418](https://github.com/microsoft/TypeScript-go/pull/4418) (Closed, `Unmigrated PR`)

**Infer void for statement\-less function bodies in \`isolatedDeclarations\` syntactic inference**

*Syntactically infer void return types for statement-less functions to avoid isolatedDeclarations errors.*

 * [1 month ago](https://github.com/microsoft/TypeScript-go/pull/4418#issuecomment-4984042065) **RyanCavanaugh** said "Looks OK, fix merge conflicts?"
 * [1 month ago](https://github.com/microsoft/TypeScript-go/pull/4418#issuecomment-4984582065) **andrewbranch** recalled that they omitted this originally to allow room for future design changes around issue 42709 without breaking third-party isolatedDeclarations emitters
 * [1 month ago](https://github.com/microsoft/TypeScript-go/pull/4418#issuecomment-4984961465) **weswigham** considered that changing the inference would require updating the isolatedDeclarations rule and wouldn't be worse for third-party emitters or preclude future changes
 * **RyanCavanaugh** added label `Unmigrated PR`

### [PR microsoft/TypeScript-go#4422](https://github.com/microsoft/TypeScript-go/pull/4422) (Closed, `Unmigrated PR`)

**Use auto\-imports for \`isolatedDeclarations\` fixes**

*Add auto-import suggestions for fixes applied to code under the isolatedDeclarations setting.*

 * created by **DanielRosenwasser**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4422#issuecomment-5320580628) **DanielRosenwasser** suggested auto-import logic bounded by the current program and fallback behavior when imports aren't available
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4422#issuecomment-5321315528) **DanielRosenwasser** said "@copilot tests are failing"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4422#issuecomment-5333823355) **jakebailey** said "Copilot started, then gave up? Maybe during the outage"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4422#issuecomment-5333889443) **DanielRosenwasser** said "@copilot make sure build/test/format is clean and working."
 * [today](https://github.com/microsoft/TypeScript-go/pull/4422#issuecomment-5334043216) **Copilot** confirmed build, test, and lint passed, noted formatting check failure due to DNS blockage in sandbox, verified Go formatting compliance with gofmt and gofumpt
 * **RyanCavanaugh** added label `Unmigrated PR`

### [PR microsoft/TypeScript-go#4442](https://github.com/microsoft/TypeScript-go/pull/4442) (Closed, **RyanCavanaugh**, **Copilot**)

**Fix false implicit\-return/unreachable diagnostics in \`try/finally\` with logical assignment \(\`\|\|=\`\)**

*Adjust TypeScript’s reachability caching to prevent erroneous missing-return and unreachable-code diagnostics in try/finally blocks using logical assignment.*

 * **Copilot** assigned to **RyanCavanaugh**
 * [7 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4442#issuecomment-4800960525) **RyanCavanaugh** said "@typescript-bot test top999"
 * [7 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4442#issuecomment-4800961276) **typescript-automation[bot]** reported starting build jobs with initial status for test top999
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#4446](https://github.com/microsoft/TypeScript-go/pull/4446) (Closed, `Unmigrated PR`)

**fix: Corsa differences in \`export=\` module augmentation**

*Corsa’s emit-phase visibility marking skips export= namespaces, leaving type T invisible and causing a false TS4060 error.*

 * [7 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4446#issuecomment-4803988303) **typescript-automation[bot]** announced performance test start with status and result links
 * [7 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4446#issuecomment-4804157001) **typescript-automation[bot]** reported the requested performance run results for tsc comparing baseline and PR
 * [7 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4446#issuecomment-4804369952) **pratheeknathani** pushed a commit removing a stale submoduleTriaged.txt entry to fix CI failures and verified tests locally
 * **jakebailey** added label `Unmigrated PR`

### [PR microsoft/TypeScript-go#4496](https://github.com/microsoft/TypeScript-go/pull/4496) (Closed, `Unmigrated PR`)

**fix\(lsp\): support TypeScript source action kinds**

*Advertise and support TypeScript-specific source action kinds suffixed with .ts in the LSP server while maintaining generic kinds for backward compatibility.*

 * [7 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4496#issuecomment-4848080613) **jakebailey** suggested looking at the vscode repo's typescript-language-features extension and questioned whether implementing the feature was critical since old extensions could not do it
 * [7 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4496#issuecomment-4848251335) **TorinAsakura** rechecked vscode and explained that the PR targets multi-server LSP scenarios rather than matching the current extension and wires actual handling to support generic source.removeUnusedImports as an escape hatch for clients
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4496#issuecomment-5321335781) **jakebailey** observed that only the TypeScript language server and similar JS tools add these suffixes, while pyright/pylance, gopls, and rust-analyzer do not
 * [today](https://github.com/microsoft/TypeScript-go/pull/4496#issuecomment-5333253192) **TorinAsakura** asked where to land with the PR and suggested using .ts

### [Issue microsoft/TypeScript-go#4502](https://github.com/microsoft/TypeScript-go/issues/4502) (Closed, `Domain: API and Extensibility`, **andrewbranch**)

**\`Program\` is missing \`\.getSourceFiles\(\)\` getter**

*Add a getSourceFiles() getter to Program to return all SourceFile instances and ease filtering.*

 * **andrewbranch** assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4502#issuecomment-5330761493) **mrazauskas** thanked Andrew Branch, noted that retrieving every SourceFile was a mistake, suggested that getSourceFileMetadata include isDeclarationFile instead, and said they would open a new issue to request it
 * (today) **mrazauskas** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/issues/4502#issuecomment-5330914862) **andrewbranch** said "That seems reasonable to include, though a declaration file can always be recognized from its filename too. I don't think we ported the isDeclarationFileName helper yet, which would be useful."

### [PR microsoft/TypeScript-go#4596](https://github.com/microsoft/TypeScript-go/pull/4596) (Closed, `Unmigrated PR`)

**Fixed mapped types not being considered as homomorphic with substitution constraints**

*Mapped types are now correctly recognized as homomorphic when using substitution constraints in TypeScript.*

 * created by **Andarist**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4596#issuecomment-5333647830) **jakebailey** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4596#issuecomment-5333648608) **typescript-automation[bot]** posted CI job start statuses with links to status and results
 * [today](https://github.com/microsoft/TypeScript-go/pull/4596#issuecomment-5333925721) **typescript-automation[bot]** reported the results of the requested performance run
 * [today](https://github.com/microsoft/TypeScript-go/pull/4596#issuecomment-5334466683) **typescript-automation[bot]** reported tsc errors in the top 400 repos when comparing main and the pull request, highlighted mismatches in type-fest tests, and requested a review
 * [today](https://github.com/microsoft/TypeScript-go/pull/4596#issuecomment-5334725057) **jakebailey** said "Hmmmm, this is a break?"
 * **jakebailey** added label `Unmigrated PR`
 * [later](https://github.com/microsoft/TypeScript-go/pull/4596#issuecomment-5340259588) **Andarist** explained that distributive homomorphic types require a specific mapped type form, demonstrated a repro case, noted that the PR fix changed behavior and broke type-fest’s implementation, added tests and workarounds, and offered to submit a type-fest fix once merged

### [PR microsoft/TypeScript-go#4597](https://github.com/microsoft/TypeScript-go/pull/4597) (Closed, `Unmigrated PR`)

**Normalize \`NoInfer\`red tuple types in rest/spread positions**

*Normalize NoInferred tuple types used in rest and spread operations to resolve related TypeScript inference issues.*

 * created by **Andarist**
 * **jakebailey** added label `Unmigrated PR`

### [PR microsoft/TypeScript-go#4600](https://github.com/microsoft/TypeScript-go/pull/4600) (Closed, `Unmigrated PR`)

**Deduplicate repeated declarations on union/intersection properties**

*Remove duplicate property declarations from union and intersection types.*

 * created by **Andarist**
 * **jakebailey** added label `Unmigrated PR`

### [PR microsoft/TypeScript-go#4650](https://github.com/microsoft/TypeScript-go/pull/4650) (Closed, **RyanCavanaugh**, **Copilot**)

**Fix: experimentalDecorators renames class name in object literal key/member name positions**

*Prevent experimentalDecorators from renaming class names in object literal keys and member names by skipping identifier substitution in declaration positions.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4650#issuecomment-5321088559) **Copilot** investigated the CR comment on computed class-element names, verified tsgo matches tsc behavior, and concluded the suggested change was incorrect
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4650#issuecomment-5321100529) **jakebailey** said "Yikes, if Strada (and Corsa right now) is wrong, then we should first commit the test showing the bug, and then commit the fix + baseline update"
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4650#issuecomment-5321106723) **jakebailey** said "That is, if it's actually a bug, given ordering matters; definitely needs a spec read"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4650#issuecomment-5331877001) **RyanCavanaugh** said "Opened https://github.com/microsoft/TypeScript/issues/63758"
 * (today) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/4650#issuecomment-5331980856) **jakebailey** said "Shouldn't we merge this, as it at least gives Strada equivalence?"

### [PR microsoft/TypeScript-go#4712](https://github.com/microsoft/TypeScript-go/pull/4712) (Closed)

**Content mappers**

*Implement content mappers that enable TypeScript to include unsupported file types by transforming them via tsconfig settings.*

 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5309110710) **remcohaszing** published an experimental MDX content mapper, reported false positive mapping errors during type checking, and asked whether the bug was in this PR or his implementation
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5309348759) **escaton** shared early testing results and included project cloc statistics and tsconfig.json configuration
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5318587603) **andrewbranch** explained that the mapper bug was caused by using UTF-8 offsets with JS’s UTF-16 string indexing and recommended using UTF-16
 * [today](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5333464611) **andrewbranch** added options diagnostics to openProject responses and unified mapper configuration by removing duplicate TransformParameters fields and requiring mappers to store options per projectHandle
 * [today](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5333508923) **escaton** suggested dropping the --runExternalCode requirement for direct CLI usage since manual code execution implies consent
 * [today](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5333849939) **andrewbranch** argued that allowing arbitrary code execution in tsc would expand its trust boundary, create a significant security risk, and break existing safety assumptions
 * [today](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5334123430) **escaton** challenged the given safety examples, arguing that any CLI command is risky regardless of flags and noting that agents would simply re-run commands with the --runExternalCode flag
 * [today](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5334280074) **andrewbranch** asserted that running tsc on untrusted code is safe since it doesn’t execute code, contrasted it with npm install and the unsafe --runExternalCode flag, and described plans for a diagnostic to require human acknowledgment for agent scenarios
 * [later](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5339365820) **remcohaszing** appreciated the explanation of security considerations and suggested adding a shorthand option '-x' for execute external

### [PR microsoft/TypeScript-go#4723](https://github.com/microsoft/TypeScript-go/pull/4723) (Closed, **jakebailey**, **Copilot**)

**Preserve comments when downleveling arrow expression bodies**

*Adjust arrow function downleveling to preserve comment placement by applying original source ranges to synthesized return statements.*

 * **Copilot** assigned to **jakebailey**
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4723#issuecomment-5243175220) **jakebailey** provided a test case from another issue comment for optional chaining
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4723#issuecomment-5318108076) **jakebailey** said "You're definitely right, but Strada double sets too: https://github.com/microsoft/TypeScript/blob/5848bc5157b22ff7f4e3369f4645a514a433b15f/src/compiler/factory/nodeConverters.ts#L54-L60"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4723#issuecomment-5334711884) **jakebailey** said "@copilot+gpt-5.6-sol Please address the above :)"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4723#issuecomment-5334941134) **Copilot** addressed suggestions in commits aca5f3b0 and 70c3165f, shared ConvertToFunctionBlock between VisitFunctionBody and the async transform while preserving async-only node attribution, and covered the regression test case in commit de6d68f6 with verbatim inclusion and comment placement validation

### [PR microsoft/TypeScript-go#4726](https://github.com/microsoft/TypeScript-go/pull/4726) (Closed, `Unmigrated PR`)

**Skip declaration emit without a prior signature**

*Skip emitting TypeScript declaration files for declarations that lack an existing signature*

 * [4 days ago](https://github.com/microsoft/TypeScript-go/pull/4726#issuecomment-5297614746) **jakebailey** said "@typescript-bot perf test this"
 * [4 days ago](https://github.com/microsoft/TypeScript-go/pull/4726#issuecomment-5297615606) **typescript-automation[bot]** reported that the performance test job started and provided status and results links
 * [4 days ago](https://github.com/microsoft/TypeScript-go/pull/4726#issuecomment-5297865842) **typescript-automation[bot]** posted the performance run results for the requested comparison
 * **jakebailey** added label `Unmigrated PR`

### [PR microsoft/TypeScript-go#4779](https://github.com/microsoft/TypeScript-go/pull/4779) (Closed, `Unmigrated PR`)

**Fix incremental builder re\-emitting entire import closure on non\-shape\-changing edits**

*Incremental builder computes real .d.ts signatures on fresh builds to avoid re-emitting full import closures on non-shape-changing edits.*

 * created by **johnfav03**
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4779#issuecomment-5243834859) **jakebailey** said "Eagerly doing dts emit seems scary, but I don't quite know if I can tell if that gut feeling is wrong or not"
 * **johnfav03** added label `Unmigrated PR`

### [Issue microsoft/TypeScript-go#4807](https://github.com/microsoft/TypeScript-go/issues/4807) (Closed, `bug`, **ahejlsberg**)

**False “Excessive stack depth” on circular types linked through arrays \(regression from \#3445\)**

*tsgo 7.0.2 erroneously reports excessive stack depth comparing circular interfaces connected via optional arrays, a regression from TypeScript 6.0*

 * [today](https://github.com/microsoft/TypeScript-go/issues/4807#issuecomment-5329498520) **ahejlsberg** explained that the 100-level stack depth error is unnecessary and proposed stopping type relating instead of erroring, and said they would submit a PR to implement the change
 * (today) **ahejlsberg** added label `bug`, and removed label `Needs Investigation`
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#4834](https://github.com/microsoft/TypeScript-go/issues/4834) (Closed, `bug`, **RyanCavanaugh**, **Copilot**)

**Default concurrent mode misses TS2307 that \`\-\-singleThreaded\` \(and TS 6\.0\) report, for import/export declarations inside non\-scope blocks**

*TypeScript's default concurrent mode omits TS2307 "Cannot find module" errors for import/export declarations inside non-scope blocks, unlike singleThreaded mode and TS 6.0.*

 * (1 week ago) **RyanCavanaugh** assigned to **Copilot**, and unassigned **Copilot**
 * [6 days ago](https://github.com/microsoft/TypeScript-go/issues/4834#issuecomment-5275662911) **itibbers** reported non-deterministic type-checking output in TypeScript 7.0.2 when using multi-threaded mode with allowJs true and provided repro data showing determinism when single-threaded or allowJs false
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#4836](https://github.com/microsoft/TypeScript-go/pull/4836) (Closed, **RyanCavanaugh**, **Copilot**)

**Preserve nested module resolution diagnostics in concurrent mode**

*Restore TS2307 diagnostics for import/export declarations in non-scoped blocks during concurrent mode by deferring module resolution and updating CLI baselines.*

 * (1 week ago) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * [4 days ago](https://github.com/microsoft/TypeScript-go/pull/4836#issuecomment-5296161717) **jakebailey** said "I have no idea why GitHub thinks I'm the last pusher"
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#4846](https://github.com/microsoft/TypeScript-go/pull/4846) (Closed, `Unmigrated PR`)

**Fix crash when a call signature's type parameter cannot be reused**

*TypeScript Go printer crashes when reuseNode fails and inserts a nil type parameter into a call signature.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4846#issuecomment-5222019357) **nikeedw** explained that the crash matched a previous bug, described how the earlier PR fixed one producer by adding a guard against nil nodes, showed the analogous fix in this PR, and warned that other unchecked node-builder paths could still yield nil and cause similar SIGSEGV crashes
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4846#issuecomment-5222176600) **nikeedw** provided a detailed static and dynamic survey showing that on main, NodeList constructions produce no nil elements in the test suite and only one nil in the two-file repro scenario
 * **RyanCavanaugh** added label `Unmigrated PR`
 * [today](https://github.com/microsoft/TypeScript-go/pull/4846#issuecomment-5334713140) **weswigham** said "Rough, looks like some semantic merge conflicts with main. This might have to get reopened post repo migration."
 * [later](https://github.com/microsoft/TypeScript-go/pull/4846#issuecomment-5340578727) **nikeedw** reported pushing a fix that reduced TS2527 errors, updated the baseline, and requested a CI approval run

### [Issue microsoft/TypeScript-go#4850](https://github.com/microsoft/TypeScript-go/issues/4850) (Closed, `Needs Investigation`, **weswigham**)

**Difference in behavior of enum used as field key in emit vs non\-emit type check**

*Enum-based record keys resolve as enum types internally but emit as string literals in declaration files.*

 * (1 week ago) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `Post-7.0`, and assigned to **weswigham**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4852](https://github.com/microsoft/TypeScript-go/pull/4852) (Closed)

**Preserve enum computed property names in declarations**

*Retain enum computed property names in declarations to prevent inlining values from breaking enum types.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4858](https://github.com/microsoft/TypeScript-go/pull/4858) (Closed, `Unmigrated PR`)

**Keep JSDoc on expando hosts declared as arrows or function expressions**

*JSDoc on expando hosts declared as arrow functions or function expressions is omitted in generated .d.ts files.*

 * created by **yogesh968**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4858#issuecomment-5333573893) **jakebailey** said "We can't really do anything with this unless the CLA is signed"
 * **jakebailey** added label `Unmigrated PR`

### [PR microsoft/TypeScript-go#4865](https://github.com/microsoft/TypeScript-go/pull/4865) (Closed, `Unmigrated PR`)

**Avoid expensive incremental reconciliation after dependency paths move**

*Detect moved dependency paths in the TypeScript compiler's incremental builds and perform a cold-build snapshot to avoid expensive reconciliation.*

 * created by **johnfav03**
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4865#issuecomment-5243653489) **jakebailey** asked to split the changes into two commits and expressed uncertainty about the heuristic approach
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4865#issuecomment-5244367310) **johnfav03** split the changes into two commits and explained that the pre-fix baseline forced .d.ts computation and signature updates while the post-fix cold-build baseline showed no signature reconciliation
 * **johnfav03** added label `Unmigrated PR`

### [Issue microsoft/TypeScript-go#4875](https://github.com/microsoft/TypeScript-go/issues/4875) (Closed, `Needs Investigation`, **weswigham**, **Copilot**)

**\`@augments\` JSDoc tag causes compilation error in generated declaration file**

*A JSDoc @augments tag mismatched with the extends clause in generated declaration files triggers ts(8023) errors under tsgo.*

 * [6 days ago](https://github.com/microsoft/TypeScript-go/issues/4875#issuecomment-5272301744) **jakebailey** said "I don't even know why this is happening in .ts files at all?"
 * [6 days ago](https://github.com/microsoft/TypeScript-go/issues/4875#issuecomment-5272315368) **weswigham** said "Also a good point! Honestly, I don't know why we're checking this at all! This is, AFAIK, a lint-consistency level error, at most."
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/4875#issuecomment-5292276241) **dragomirtitian** noted that jsdoc checks in ts files were unexpected and suggested it was only a lint-consistency level error
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4889](https://github.com/microsoft/TypeScript-go/pull/4889) (Closed, **weswigham**, **Copilot**)

**Use semantic type identity for JSDoc augments checks**

*Use semantic type identity for JSDoc @augments checks to avoid false mismatches when extending through aliases.*

 * **Copilot** assigned to **weswigham**
 * [5 days ago](https://github.com/microsoft/TypeScript-go/pull/4889#issuecomment-5286070875) **weswigham** said "Actually @copilot also limit the check to JS files only - we shouldn't be issuing this (lint?) in .d.ts or .ts files at all anyway."
 * [5 days ago](https://github.com/microsoft/TypeScript-go/pull/4889#issuecomment-5286284754) **Copilot** implemented augments/extends mismatch validation to apply only to JavaScript source files
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4900](https://github.com/microsoft/TypeScript-go/pull/4900) (Closed, **DanielRosenwasser**, **Copilot**)

**Prevent crash when computing emit output paths**

*Prevent panics in computing emit output paths by delegating to a canonical prefix-based worker and removing invalid containment checks*

 * **Copilot** assigned to **DanielRosenwasser**
 * [4 days ago](https://github.com/microsoft/TypeScript-go/pull/4900#issuecomment-5296019507) **DanielRosenwasser** said "@copilot this really needs an integration/compiler test as well."
 * [4 days ago](https://github.com/microsoft/TypeScript-go/pull/4900#issuecomment-5296249214) **Copilot** added compiler regression coverage reproducing the pre-fix slice bounds out of range panic and verified it passed with the fix
 * [today](https://github.com/microsoft/TypeScript-go/pull/4900#issuecomment-5335401483) **weswigham** said "@copilot can you find and add regression tests for the new sites you updated to use TrimFilePathPrefix that prove the necessity of the changes to fix crashes?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4900#issuecomment-5335562620) **Copilot** added two regression tests demonstrating slice bounds panics fixed by TrimFilePathPrefix
 * [today](https://github.com/microsoft/TypeScript-go/pull/4900#issuecomment-5336656981) **DanielRosenwasser** said "@typescript-bot perf test this"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4900#issuecomment-5336657446) **typescript-automation[bot]** announced that the 'perf test this' job started and provided status and results links
 * [today](https://github.com/microsoft/TypeScript-go/pull/4900#issuecomment-5336853630) **typescript-automation[bot]** reported the requested performance run results

### [Issue microsoft/TypeScript-go#4908](https://github.com/microsoft/TypeScript-go/issues/4908) (Closed, `bug`, `Domain: Editor`, **DanielRosenwasser**, **Copilot**)

**Go\-to\-definition does not work at the right edge of a JSX tag name**

*Go-to-definition fails when invoked at the right edge of a JSX tag name in the updated codebase.*

 * (yesterday) **DanielRosenwasser** added label `Domain: Editor`, and assigned to **Copilot**, **DanielRosenwasser**
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#4909](https://github.com/microsoft/TypeScript-go/pull/4909) (Closed, **DanielRosenwasser**, **Copilot**)

**Fix go\-to\-definition functionality at JS JSX tag edge**

*Align go-to-definition token selection at JSX tag name edges and add focused tests and validations*

 * (yesterday) **DanielRosenwasser** reopened the issue
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4909#issuecomment-5320593803) **DanielRosenwasser** said "@copilot+gpt-5.6-sol you added the test but not the fix."
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4909#issuecomment-5320856805) **Copilot** implemented the touching-token fix, refined existing completion behavior, and added an accepted definition baseline for the JSX go-to-definition test
 * [today](https://github.com/microsoft/TypeScript-go/pull/4909#issuecomment-5334661758) **andrewbranch** said "Does this need an equivalent change in astnav.ts?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4909#issuecomment-5334707584) **jakebailey** said "Probably, yeah; we should have some sort of review tool that double checks that we have them in sync-ish (not sure how such a tool would work...)"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4909#issuecomment-5334824318) **andrewbranch** said "I was avoiding review poisoning myself but I guess I can do it and let you review again. @copilot see if astnav.ts needs an equivalent change."
 * [today](https://github.com/microsoft/TypeScript-go/pull/4909#issuecomment-5335026540) **Copilot** ported the equivalent change to astnav.ts in commit 21626c98 and confirmed that tests passed
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#4913](https://github.com/microsoft/TypeScript-go/pull/4913) (Closed)

**Improve recursion identities and \`isDeeplyNestedType\`**

*Refine recursion identities for indexed access types and eliminate excessive stack depth errors in isDeeplyNestedType.*

 * [today](https://github.com/microsoft/TypeScript-go/pull/4913#issuecomment-5330407109) **ahejlsberg** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4913#issuecomment-5330408300) **typescript-automation[bot]** reported that CI jobs started and updated their statuses with links to results
 * [today](https://github.com/microsoft/TypeScript-go/pull/4913#issuecomment-5330768512) **typescript-automation[bot]** provided performance run results
 * [today](https://github.com/microsoft/TypeScript-go/pull/4913#issuecomment-5331389137) **typescript-automation[bot]** reported that running the TypeScript compiler on the top 400 repos showed no regressions between main and the PR merge
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#4914](https://github.com/microsoft/TypeScript-go/pull/4914) (Closed, `Unmigrated PR`)

**createProgram**

*Introduce a createProgram API that constructs or incrementally updates TypeScript programs using snapshots and optional oldProgram changes.*

 * created by **gabritto**
 * **gabritto** added label `Unmigrated PR`

### [PR microsoft/TypeScript-go#4915](https://github.com/microsoft/TypeScript-go/pull/4915) (Closed)

**Generate TS API from Go source**

*Auto-generate a strongly typed TypeScript API client by parsing Go Session HandleRequest methods and custom annotations*

 * created by **weswigham**

