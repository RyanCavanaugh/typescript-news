# Report for 2026-07-15 (Wednesday, July 15th, 2026)

15 different users commented on 47 different issues.

## Recommended Actions

 * Response Recommended
    * @shining-mind asked why CLI support was not planned in [microsoft/TypeScript-go#2824](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-4982699924)
    * @nikelborm provided a relevant report link in [microsoft/TypeScript-go#2824](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-4983029792)
    * @shining-mind asked whether there were plans to create a dedicated feature request for CLI support for typechecking Vue, Svelte, and string template literals in [microsoft/TypeScript-go#2824](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-4991793665)
    * @chikujoyayabo asked to reconsider bringing back the ts.locale override feature in [microsoft/TypeScript-go#4017](https://github.com/microsoft/TypeScript-go/issues/4017#issuecomment-4988337023)
    * @anthonyshew provided additional context on hang behavior with pnpm run dev:ts in [microsoft/TypeScript-go#4620](https://github.com/microsoft/TypeScript-go/issues/4620#issuecomment-4983072567)
    * @typescript-automation[bot] provided perf run results as requested in [microsoft/TypeScript-go#4640](https://github.com/microsoft/TypeScript-go/pull/4640#issuecomment-4983761218)

## Activity Summary

### [Issue microsoft/TypeScript-go#2228](https://github.com/microsoft/TypeScript-go/issues/2228) (Closed, `Domain: Editor`, **gabritto**)

**No JS Doc template completions**

*The ts-go extension lacks support for the JSDoc template completion feature introduced in TypeScript 6.0 for VSCode.*

 * **gabritto** assigned to **gabritto**
 * **jakebailey** added label `Domain: Editor`
 * **RyanCavanaugh** added to milestone `Post-7.0`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2228#issuecomment-4985385037) **gabritto** said "Fixed by #4505."
 * (today) **gabritto** closed the issue

### [Issue microsoft/TypeScript-go#2824](https://github.com/microsoft/TypeScript-go/issues/2824) (Open, `Domain: API and Extensibility`, **andrewbranch**)

**API usage patterns for complex editor extensions**

*Exploring IPC-based API features for a Go TS server to replace TS Server plugins and support Vue editor extensions*

 * [6 days ago](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-4928456800) **andrewbranch** explained that parse errors in raw TS script blocks should be mapped correctly rather than treated as invalid plugin states
 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-4933547787) **remcohaszing** suggested expecting plugins to be executable and determined by their shebang, recommended against using 'bin' due to package manager symlinks, suggested a special field for browser import usage, and questioned how plugin execution should work on Windows
 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-4935519462) **bartlomieju** described Deno's need for a scheme-aware static mapping API for module resolution and declaration files and explained current workaround and its limitations
 * [today](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-4982699924) **shining-mind** asked why CLI support wasn't planned and emphasized its importance for CI and agent-based scenarios
 * [today](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-4983029792) **nikelborm** shared a report evaluating and comparing a matrix of bridging strategies
 * [today](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-4983158061) **andrewbranch** clarified that the issue aimed to achieve TS 7 parity with TS 6 by proposing LSP-only plugins, noted feedback that certain CLI capabilities require central tsc coordination, and argued against expanding to a broad CLI plugin scope to avoid delaying parity
 * [later](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-4991793665) **shining-mind** agreed and asked whether there were plans to create a dedicated feature request for CLI support for typechecking Vue, Svelte, and string template literals

### [Issue microsoft/TypeScript-go#4017](https://github.com/microsoft/TypeScript-go/issues/4017) (Closed, `Domain: Editor`, `possible improvement`)

**Extension does not respect \`js/ts\.locale\`**

*The extension ignores js/ts.locale settings and always displays English error messages because it does not send locale to the server.*

 * [8 weeks ago](https://github.com/microsoft/TypeScript-go/issues/4017#issuecomment-4505111440) **DanielRosenwasser** noted that the feature automatically takes effect when using "Configure Display Language" and suggested gathering feedback before considering overrides
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/4017#issuecomment-4897652991) **DanielRosenwasser** said "We'll reopen if people provide feedback."
 * (1 week ago) **DanielRosenwasser** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/issues/4017#issuecomment-4988337023) **chikujoyayabo** requested reinstating the ability to override the TypeScript server locale to English separate from the global VS Code language due to poor Simplified Chinese translations

### [PR microsoft/TypeScript-go#4418](https://github.com/microsoft/TypeScript-go/pull/4418) (Open)

**Infer void for statement\-less function bodies in \`isolatedDeclarations\` syntactic inference**

*Syntactically infer void return types for statement-less functions to avoid isolatedDeclarations errors.*

 * created by **weswigham**
 * **weswigham** added to milestone `Post-7.0`
 * [today](https://github.com/microsoft/TypeScript-go/pull/4418#issuecomment-4984042065) **RyanCavanaugh** said "Looks OK, fix merge conflicts?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4418#issuecomment-4984582065) **andrewbranch** recalled that they omitted this originally to allow room for future design changes around issue 42709 without breaking third-party isolatedDeclarations emitters
 * [today](https://github.com/microsoft/TypeScript-go/pull/4418#issuecomment-4984961465) **weswigham** explained that changing the inference would only require updating the isolatedDeclarations inference rule and wouldn't hinder third-party emitters any more than adding a new syntax construct, and that it likely wouldn't preclude future changes

### [PR microsoft/TypeScript-go#4443](https://github.com/microsoft/TypeScript-go/pull/4443) (Open, **andrewbranch**)

**Fixed build mode false negative from export\-star facade**

*Fix false negative TypeScript build-mode error caused by export-star facade usage.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4443#issuecomment-4847080467) **johnfav03** agreed that marking the issue for post-7.0 was appropriate because it also existed in 6.0 and wasn't time-critical
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4443#issuecomment-4847081152) **jakebailey** acknowledged the referenced issue and clarified that they had thought it was a new bug
 * **johnfav03** added to milestone `Post-7.0`
 * **RyanCavanaugh** assigned to **andrewbranch**

### [PR microsoft/TypeScript-go#4565](https://github.com/microsoft/TypeScript-go/pull/4565) (Open, **weswigham**)

**Fix stack overflow in \`checkTypeExpandability\(\)\`**

*checkTypeExpandability fails to track reference type arguments, causing infinite recursion and stack overflow*

 * created by **johnfav03**
 * **RyanCavanaugh** assigned to **weswigham**

### [Issue microsoft/TypeScript-go#4572](https://github.com/microsoft/TypeScript-go/issues/4572) (Open, `Needs Investigation`, **ahejlsberg**)

**Overloaded assertion in inferred\-return function expression loses destructured discriminant narrowing**

*An overloaded assert in an arrow function without a return type annotation prevents TypeScript from narrowing a destructured discriminant property.*

 * created by **adri1wald**
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/4572#issuecomment-4947548278) **Andarist** said "bisects to https://github.com/microsoft/typescript-go/pull/2542 , potential fix at https://github.com/microsoft/typescript-go/pull/4606"
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.1`, and assigned to **ahejlsberg**

### [Issue microsoft/TypeScript-go#4573](https://github.com/microsoft/TypeScript-go/issues/4573) (Open, `Needs Investigation`, **andrewbranch**)

**Add ability to get emit output from the API**

*Enable TypeScript API's program.emit to return JS, declaration, and source map outputs for multiple files in one call.*

 * created by **dragomirtitian**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `Possible Improvement`, and assigned to **andrewbranch**

### [PR microsoft/TypeScript-go#4577](https://github.com/microsoft/TypeScript-go/pull/4577) (Open, **iisaduan**)

**Fix stack overflow in inherited JSDoc resolution**

*Resolving inherited JSDoc without cycle detection can cause infinite recursion and stack overflow on circular class references.*

 * created by **johnfav03**
 * **RyanCavanaugh** assigned to **iisaduan**

### [Issue microsoft/TypeScript-go#4585](https://github.com/microsoft/TypeScript-go/issues/4585) (Open, `Domain: Editor`, `Needs Investigation`, **andrewbranch**)

**Local auto\-imports disappear when a Yarn workspace dependency resolves a subpath back to the current project**

*TypeScript 7 in VS Code fails to suggest local auto-imports when a Yarn workspace dependency resolves a subpath back to the project.*

 * created by **sashamorozov**
 * **sashamorozov** added label `Domain: Editor`
 * (today) **RyanCavanaugh** set milestone to `Post-7.0`, and assigned to **andrewbranch**
 * **andrewbranch** added label `Needs Investigation`

### [Issue microsoft/TypeScript-go#4593](https://github.com/microsoft/TypeScript-go/issues/4593) (Closed, `Domain: Editor`)

**File change events always trigger project recheck even if file content hasn't actually changed**

*File watcher change events for unchanged files always trigger a full TypeScript project recheck.*

 * created by **mjbvz**
 * **mjbvz** added label `Domain: Editor`
 * (today) **johnfav03** closed the issue

### [PR microsoft/TypeScript-go#4594](https://github.com/microsoft/TypeScript-go/pull/4594) (Closed)

**Fix "Token end is child end" crash when range formatting is inside a JSDoc comment**

*Formatting inside JSDoc causes the scanner to parse backticks as an unclosed template literal, crashing on token end mismatch.*

 * created by **johnfav03**
 * (today) **johnfav03** closed the issue

### [Issue microsoft/TypeScript-go#4595](https://github.com/microsoft/TypeScript-go/issues/4595) (Closed, `Domain: Editor`, **johnfav03**)

**File watch events can cause a check/cancel/re\-check storm**

*Batch file watch events in a TypeScript project trigger repeated diagnostic cancellations and re-checks, leading to sustained high CPU usage.*

 * **RyanCavanaugh** assigned to **johnfav03**
 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/4595#issuecomment-4939520056) **RyanCavanaugh** said "@mjbvz I thought I was done getting editor bugs from you! 😜"
 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/4595#issuecomment-4940126284) **mjbvz** said "Ha sorry but looks like you're still stuck with me. Always finding new ways to stress test TypeScript 🙃 "
 * (today) **johnfav03** closed the issue

### [Issue microsoft/TypeScript-go#4601](https://github.com/microsoft/TypeScript-go/issues/4601) (Open, `bug`, **johnfav03**)

**\[ServerErrors\]\[TypeScript\] main vs **

*Server errors were reported on the main TypeScript branch during an Azure pipeline run analyzing 300 popular GitHub repositories.*

 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/4601#issuecomment-4940320969) **typescript-automation[bot]** reported that the server connection closed prematurely with an undefined error for the babel/babel repo
 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/4601#issuecomment-4940320996) **typescript-automation[bot]** reported a premature server connection closure error and provided logs, artifact links, and repro steps for cypress-io/cypress
 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/4601#issuecomment-4940321025) **typescript-automation[bot]** reported a server connection closed prematurely error for strapi/strapi
 * (today) **RyanCavanaugh** added label `bug`, and assigned to **johnfav03**

### [PR microsoft/TypeScript-go#4606](https://github.com/microsoft/TypeScript-go/pull/4606) (Open, **ahejlsberg**)

**Keep dependent destructuring narrowing during re\-entrant checks**

*Preserve dependent destructuring type narrowing across re-entrant type-checking operations.*

 * created by **Andarist**
 * **RyanCavanaugh** assigned to **ahejlsberg**

### [Issue microsoft/TypeScript-go#4607](https://github.com/microsoft/TypeScript-go/issues/4607) (Open, `Crash`, `Needs More Info`)

**TypeScript 7\.0 Can't compile \`webpack\`**

*TypeScript 7.0 compiler panics with unexpected JSTypeAliasDeclaration nodes while compiling webpack*

 * created by **avivkeller**
 * **avivkeller** added label `Crash`
 * [today](https://github.com/microsoft/TypeScript-go/issues/4607#issuecomment-4985037244) **RyanCavanaugh** asked for ideas after reporting TypeScript compilation errors and version details
 * **RyanCavanaugh** added label `Needs More Info`
 * [today](https://github.com/microsoft/TypeScript-go/issues/4607#issuecomment-4986414764) **avivkeller** said "Hi! Sorry! It looks like I had declaration: true locally which was a requirement of the error, it seems. I'm still looking for a minimal repro."

### [Issue microsoft/TypeScript-go#4609](https://github.com/microsoft/TypeScript-go/issues/4609) (Open, `bug`)

**Extensionless root file panics the compiler: "ScriptKind must be specified when parsing source file"**

*TypeScript 7's compiler panics with a 'ScriptKind must be specified' error when parsing extensionless root files.*

 * created by **elibarzilay**
 * (today) **RyanCavanaugh** added label `bug`, and set milestone to `Post-7.0`

### [Issue microsoft/TypeScript-go#4612](https://github.com/microsoft/TypeScript-go/issues/4612) (Closed, `duplicate`)

**Checker memory explosion from repeated cross\-product distribution \(repro: @types/three TSL\)**

*Repeated cross-product distribution in @types/three TSL types causes the TypeScript Go checker to consume excessive memory.*

 * created by **Skykill**
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/4612#issuecomment-4959089348) **ahejlsberg** said "This appears to be a duplicate of #4528. The fix I suggest there also fixes this issue."
 * **ahejlsberg** added label `duplicate`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#4613](https://github.com/microsoft/TypeScript-go/issues/4613) (Open, `bug`, **ahejlsberg**)

**Exhaustive switch on co\-narrowed tuple's \`\.length\` does not terminate fallthrough control flow \(works in TS 6\.0\)**

*TypeScript 7.0 misidentifies an exhaustive inner switch on a co-narrowed tuple’s length as non-terminating, leading to incorrect type inference.*

 * created by **sergey-shandar**
 * (today) **RyanCavanaugh** added label `bug`, set milestone to `TypeScript 7.1`, and assigned to **ahejlsberg**

### [Issue microsoft/TypeScript-go#4614](https://github.com/microsoft/TypeScript-go/issues/4614) (Open, `Needs Investigation`, **johnfav03**)

**\`tsc \-b \-\-watch\` takes tens of seconds to start watching on a large project\-references solution \(\`computeDesiredWatches\` is O\(files × dirs\)\)**

*tsc -b --watch stalls for tens of seconds on large project-reference solutions because computeDesiredWatches’s O(files×dirs) logic delays filesystem watch registration*

 * created by **dyantako**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.1`, and assigned to **johnfav03**

### [Issue microsoft/TypeScript-go#4616](https://github.com/microsoft/TypeScript-go/issues/4616) (Open, `bug`, **andrewbranch**, **RyanCavanaugh**, **Copilot**)

**Behavior difference: declaration emit synthesizes extensionless \`import\(\)\` specifier under \`allowImportingTsExtensions\`, invalid in nodenext**

*Using allowImportingTsExtensions with module nodenext, tsgo's declaration emit drops file extensions, producing invalid import() specifiers.*

 * created by **dario-causaly**
 * (today) **RyanCavanaugh** added label `bug`, set milestone to `TypeScript 7.1`, and assigned to **andrewbranch**, **Copilot**, **RyanCavanaugh**

### [Issue microsoft/TypeScript-go#4617](https://github.com/microsoft/TypeScript-go/issues/4617) (Open, `Needs Investigation`, **weswigham**)

**Behavior difference: TS4023 on declaration emit when a spread of a symbol\-branded object is unioned with the original \(pattern used by zod \`\.brand\(\)\`\)**

*Unioning a symbol-branded object with its spread causes tsgo to inline the brand symbol and error TS4023, unlike tsc.*

 * created by **dario-causaly**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.1`, and assigned to **weswigham**

### [Issue microsoft/TypeScript-go#4620](https://github.com/microsoft/TypeScript-go/issues/4620) (Open, `Needs Investigation`, **jakebailey**)

**tsc is not resposive to \`ctrl\-c\`**

*tsc fails to respond to ctrl-c due to incomplete propagation of signal handlers in typescript-go*

 * created by **lukesandberg**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4620#issuecomment-4983072567) **anthonyshew** described that pnpm run dev:ts hung on one Ctrl+C and required three to exit, whereas pnpm exec tsc exited immediately

### [Issue microsoft/TypeScript-go#4622](https://github.com/microsoft/TypeScript-go/issues/4622) (Closed, `Non-regression`)

**High memory usage for packages such as \`@microsoft/teams\.graph\-endpoints\`**

*Importing @microsoft/teams.graph-endpoints in a minimal TypeScript project spikes memory usage by approximately 300 MB, prompting investigation into potential TypeScript-side optimizations.*

 * created by **mjbvz**
 * **RyanCavanaugh** added label `Non-regression`
 * [today](https://github.com/microsoft/TypeScript-go/issues/4622#issuecomment-4983769231) **RyanCavanaugh** argued that increased memory usage with many files was reasonable under current global typing rules
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#4629](https://github.com/microsoft/TypeScript-go/issues/4629) (Closed, `Crash`, **weswigham**)

**panic: Unknown parent for parameter: KindArrowFunction**

*typescript-go crashes with panic 'Unknown parent for parameter: KindArrowFunction' during declaration transformation.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/4629#issuecomment-4973928142) **RyanCavanaugh** provided a minimal repro example with JS and TS code
 * [today](https://github.com/microsoft/TypeScript-go/issues/4629#issuecomment-4978918590) **tido64** confirmed that the example was a minimal repro and noted that inlining the type prevented the panic
 * **RyanCavanaugh** assigned to **weswigham**
 * (today) **weswigham** closed the issue

### [Issue microsoft/TypeScript-go#4630](https://github.com/microsoft/TypeScript-go/issues/4630) (Open, `Needs More Info`)

**"Type instantiation is excessively deep and possibly infinite" error with tsgo in v7**

*Typechecking with tsgo and TypeScript v7.0.2 intermittently fails with excessive stack depth and infinite type instantiation errors, unlike v6.0.*

 * created by **justinsmid**
 * **RyanCavanaugh** added label `Needs More Info`
 * [today](https://github.com/microsoft/TypeScript-go/issues/4630#issuecomment-4982461122) **RyanCavanaugh** suggested attaching a debugger and inspecting the call stack, noted TypeScript lacks source file positioning at the error frame, and recommended using the TypeScript-Maintainer-Skills repro reduction tool to provide a reproduction
 * [later](https://github.com/microsoft/TypeScript-go/issues/4630#issuecomment-4989796747) **justinsmid** thanked RyanCavanaugh and said he would move the issue to the tsgo repo after isolating a minimal reproduction

### [Issue microsoft/TypeScript-go#4631](https://github.com/microsoft/TypeScript-go/issues/4631) (Closed, `Working As Intended`)

**Error TS2590 after migration to Typescript 7\.**

*Migrating a React MUI project to TypeScript 7 causes TS2590 due to excessively complex union types*

 * created by **aleks-elkin**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4631#issuecomment-4981780700) **ahejlsberg** explained that a bug in TS6 caused the issue due to skipLibCheck logic, that it was fixed in TS7, and suggested disabling skipLibCheck to reproduce the error in TS6
 * **ahejlsberg** added label `Working As Intended`
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#4632](https://github.com/microsoft/TypeScript-go/issues/4632) (Open, `bug`, **RyanCavanaugh**, **Copilot**)

**experimentalDecorators: a class name used as an object literal key is renamed to the self\-reference alias**

*TypeScript 7.0.2 with experimentalDecorators wrongly renames object literal keys matching a decorated class name to its alias.*

 * created by **omairvaiyani**
 * (today) **RyanCavanaugh** added label `bug`, set milestone to `Post-7.0`, and assigned to **Copilot**, **RyanCavanaugh**

### [Issue microsoft/TypeScript-go#4633](https://github.com/microsoft/TypeScript-go/issues/4633) (Open, `Needs Investigation`, **jakebailey**)

**Publish an official wasip1 \(WASI\) build artifact of tsgo**

*Publish an official Go WASI (wasip1) WebAssembly build artifact of tsgo alongside native binaries in releases.*

 * created by **calvinrp**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `Possible Improvement`, and assigned to **jakebailey**

### [Issue microsoft/TypeScript-go#4635](https://github.com/microsoft/TypeScript-go/issues/4635) (Open, `bug`)

**Semantic tokens: defaultLibrary modifier never set on case\-insensitive filesystems \(macOS/Windows\)**

*TypeScript Native Preview extension on macOS/Windows case-insensitive filesystems omits defaultLibrary semantic token modifier for library globals causing incorrect theming*

 * created by **philiplindberg**
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/4635#issuecomment-4971925016) **philiplindberg** clarified that the issue reproduced identically on the released typescript@7.0.2 GA with zero tokens in both preview and GA binaries
 * (today) **RyanCavanaugh** added label `bug`, and set milestone to `Possible Improvement`

### [PR microsoft/TypeScript-go#4636](https://github.com/microsoft/TypeScript-go/pull/4636) (Closed)

**Fix emit mistakenly marking enums used in their own emit as used for unused refs errors**

*Prevent the emit process from mistakenly treating self-referencing enums as used, thereby avoiding false unused reference errors.*

 * created by **weswigham**
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript-go#4637](https://github.com/microsoft/TypeScript-go/pull/4637) (Closed)

**Skip project recheck for no\-op file watch events**

*Skip unnecessary program rechecks and diagnostic refresh storms by only invalidating type-check state when watched files actually change.*

 * created by **johnfav03**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4637#issuecomment-4984047767) **andrewbranch** said "@johnfav03 did you measure the difference parallelizing made? I'm curious how much it ends up mattering."
 * [today](https://github.com/microsoft/TypeScript-go/pull/4637#issuecomment-4984255212) **johnfav03** reported a 1.5-2x speed-up from parallelizing depending on file size
 * (today) **johnfav03** closed the issue

### [PR microsoft/TypeScript-go#4639](https://github.com/microsoft/TypeScript-go/pull/4639) (Closed)

**Make JSX missing module error span be issued at a stable location**

*Adjust JSX missing module error spans to consistently point at the file’s first tag for stable diagnostics.*

 * created by **weswigham**
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript-go#4640](https://github.com/microsoft/TypeScript-go/pull/4640) (Closed)

**Always accumulate deferred diagnostics**

*Ensure deferred diagnostics are always accumulated to fix dropped and bogus circularity errors and add caching for getTypeOfExpression*

 * created by **weswigham**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4640#issuecomment-4974242890) **jakebailey** said "Yeah I thought this was very intentionally introduced into this codebase"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4640#issuecomment-4983217592) **weswigham** explained that deferred diagnostics were reintroduced due to required deferral for circularities, outlined issues with the saveDeferredDiagnostics approach in arbitrary-check-order contexts, and stated that this PR fixes the resulting bug
 * [today](https://github.com/microsoft/TypeScript-go/pull/4640#issuecomment-4983556669) **gabritto** said "@typescript-bot perf test this"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4640#issuecomment-4983557319) **typescript-automation[bot]** announced the start of performance tests and provided links to build status and results
 * [today](https://github.com/microsoft/TypeScript-go/pull/4640#issuecomment-4983761218) **typescript-automation[bot]** provided the performance run results comparing baseline and pr metrics
 * [today](https://github.com/microsoft/TypeScript-go/pull/4640#issuecomment-4983775085) **gabritto** said "Forgot we don't yet measure memory for server scenarios 🙁"
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript-go#4641](https://github.com/microsoft/TypeScript-go/pull/4641) (Closed)

**Fix computed name error emit reusing the name expression cache**

*Use a separate resolved type cache for computed property names to ensure proper error emission.*

 * created by **weswigham**
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript-go#4642](https://github.com/microsoft/TypeScript-go/pull/4642) (Closed)

**Add \`runWithTemporaryFileUpdate\` to API**

*Add runWithTemporaryFileUpdate method to the API to enable single-file speculative edits on snapshots, supporting the Strada use case.*

 * created by **gabritto**
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript-go#4644](https://github.com/microsoft/TypeScript-go/pull/4644) (Closed)

**fix: include static private identifier properties in matching**

*Removed an early continue in relater.go to include static private identifier properties in getUnmatchedPropertiesWorker matching, fixing privateNamesAndStaticFields behavior*

 * created by **joaquinjulca26**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4644#issuecomment-4975473912) **joaquinjulca26** listed testing commands
 * [today](https://github.com/microsoft/TypeScript-go/pull/4644#issuecomment-4985727592) **joaquinjulca26** said "View: #4652 "
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#4645](https://github.com/microsoft/TypeScript-go/pull/4645) (Closed)

**Fix compiler panic on arrow function visibility diagnostics \(Fixes \#4629\)**

*Add early guard for arrow functions and fallback for anonymous declarations to prevent compiler panics during visibility diagnostics*

 * created by **islamfahmy**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4645#issuecomment-4978580316) **islamfahmy** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4645#issuecomment-4983650255) **weswigham** said "Closing in favor of https://github.com/microsoft/typescript-go/pull/4648 - this approach is fundamentally a workaround that layers hackiness up just to cover for a simple missing case, unfortunately."
 * (today) **weswigham** closed the issue

### [Issue microsoft/TypeScript-go#4647](https://github.com/microsoft/TypeScript-go/issues/4647) (Open, `Type Ordering`)

**Root file order causes tsgo to miss recursive conditional type assignability error**

*Reordering root files causes tsgo to miss recursive conditional type assignability errors.*

 * created by **tomquist**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4647#issuecomment-4980029614) **jakebailey** said "You should also check 6.0 with --stableTypeOrdering"
 * [today](https://github.com/microsoft/TypeScript-go/issues/4647#issuecomment-4980864285) **tomquist** reported that reversing the compilation root file order prevented the TS2322 error and that tsgo succeeded in both orders, confirming the root-order-dependent difference under stable type ordering
 * [today](https://github.com/microsoft/TypeScript-go/issues/4647#issuecomment-4982990887) **RyanCavanaugh** clarified that resilience to ordering changes is a TS7 feature, not a bug, and suggested using a simpler repro for order-dependent behavior mirroring TS6
 * (today) **RyanCavanaugh** added label `Type Ordering`, and set milestone to `Possible Improvement`

### [PR microsoft/TypeScript-go#4648](https://github.com/microsoft/TypeScript-go/pull/4648) (Closed)

**Fix declaration emit crash on export assigned arrow function using external name**

*Prevent declaration emit crash by transforming export-assigned arrow functions with external names into variable statements using reused type nodes.*

 * created by **weswigham**
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript-go#4649](https://github.com/microsoft/TypeScript-go/pull/4649) (Open, **RyanCavanaugh**, **Copilot**)

**Fix declaration emit synthesizing extensionless import\(\) specifier under allowImportingTsExtensions \+ nodenext**

*Declaration emit under allowImportingTsExtensions and nodenext stripped .js extensions from import() specifiers, causing TS2307 errors.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**

### [PR microsoft/TypeScript-go#4650](https://github.com/microsoft/TypeScript-go/pull/4650) (Open, **RyanCavanaugh**, **Copilot**)

**Fix: experimentalDecorators renames class name in object literal key/member name positions**

*experimentalDecorators incorrectly renames class names in object literal keys and member names, fixed by skipping non-computed property and member identifiers.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**

### [PR microsoft/TypeScript-go#4651](https://github.com/microsoft/TypeScript-go/pull/4651) (Open)

**Do not issue diagnostics when fetching parameter types for context\-sensitive parameters**

*Stop issuing incorrect diagnostics for context-sensitive parameters when their types are fetched out of context.*

 * created by **weswigham**

### [PR microsoft/TypeScript-go#4652](https://github.com/microsoft/TypeScript-go/pull/4652) (Closed)

**Remove TODO comment in getUnmatchedPropertiesWorker**

*Remove the TODO comment in getUnmatchedPropertiesWorker to improve code cleanliness.*

 * created by **joaquinjulca26**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4652#issuecomment-4985887256) **RyanCavanaugh** said "This seems unlikely to be a correct fix absent more context. What issue is this intended to solve? What's the observable behavior?"
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#4653](https://github.com/microsoft/TypeScript-go/pull/4653) (Open)

**Error with a suggestion of '\.' for empty project reference paths**

*Report empty project reference paths with a new TS18052 diagnostic suggesting '.' instead of the generic TS18051 error message.*

 * created by **KlyneChrysler**

### [PR microsoft/TypeScript-go#4654](https://github.com/microsoft/TypeScript-go/pull/4654) (Open)

**Use canonical paths for the semantic tokens defaultLibrary check**

*Adjust semantic tokens handler to use canonical file paths for default library detection on case-insensitive file systems.*

 * created by **KlyneChrysler**

