# Report for 2026-06-08 (Monday, June 8th, 2026)

13 different users commented on 68 different issues.

## Recommended Actions

 * Response Recommended
    * @hkleungai asked if the feature could be added back to TS7 in [microsoft/TypeScript-go#4230](https://github.com/microsoft/TypeScript-go/issues/4230#issuecomment-4656519612)
    * @typescript-automation[bot] provided requested perf run results in [microsoft/TypeScript-go#4234](https://github.com/microsoft/TypeScript-go/pull/4234#issuecomment-4653159218)
    * @typescript-automation[bot] provided perf run results as requested in [microsoft/TypeScript-go#4239](https://github.com/microsoft/TypeScript-go/pull/4239#issuecomment-4652072023)
    * @mds-ant asked whether to close the PR due to duplication concerns in [microsoft/TypeScript-go#4240](https://github.com/microsoft/TypeScript-go/pull/4240#issuecomment-4658350219)

## Activity Summary

### [Issue microsoft/TypeScript-go#1685](https://github.com/microsoft/TypeScript-go/issues/1685) (Closed, `Domain: Type Checking`, `Domain: JS`, **sandersn**)

**\`ts\-check\` used with \`@typedef\` causes an error on \`module\.exports = \.\.\.\`**

*Combining @ts-check and @typedef in a CommonJS file causes a TS2309 export assignment error with tsgo.*

 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/1685#issuecomment-4636409370) **ahejlsberg** explained the errors in the example were a known TS7 restriction and referenced CHANGES.md describing the Corsa module.exports assignment rule
 * [today](https://github.com/microsoft/TypeScript-go/issues/1685#issuecomment-4650033848) **jbeaudoin-lf** said "@ahejlsberg I guess we gonna have to find an alternative and migrate away from this pattern... Thanks anyways"
 * **RyanCavanaugh** removed from milestone `TypeScript 7.0 RC`
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#1966](https://github.com/microsoft/TypeScript-go/pull/1966) (Open, `No linked issue`)

**Add Yarn PnP support**

*Implement native Yarn Plug'n'Play support in TypeScript Go with PnP VFS, API, and manifest handling.*

 * [20 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1966#issuecomment-3756917844) **jakebailey** clarified that deciding on the approach and long-term implications, not PR review, was the blocker
 * [20 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1966#issuecomment-3758895612) **wojtekmaj** supported adding native Plug’n’Play support to typescript-go, cited growing Yarn usage statistics, and explained how patch-based solutions cause maintenance overhead
 * **RyanCavanaugh** added to milestone `Possible Improvement`
 * **RyanCavanaugh** added label `No linked issue`

### [Issue microsoft/TypeScript-go#2227](https://github.com/microsoft/TypeScript-go/issues/2227) (Open, `Domain: Editor`)

**Port \`move to file\` refactoring**

*Reintroduce the Move to file refactoring from TypeScript 6 into the language server to restore essential automated code relocation functionality.*

 * (9 weeks ago) **RyanCavanaugh** set milestone to `TypeScript 7.0 RC`, assigned to **RyanCavanaugh**, and unassigned **RyanCavanaugh**
 * (today) **RyanCavanaugh** set milestone to `Post-7.0`, removed from milestone `TypeScript 7.0 RC`, and unassigned **Copilot**

### [PR microsoft/TypeScript-go#2417](https://github.com/microsoft/TypeScript-go/pull/2417) (Open, `No linked issue`)

**Support \-\-pprofDir option with \-\-watch**

*Add --pprofDir support to the --watch mode to allow profiling of active processes.*

 * [7 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2417#issuecomment-4264088120) **jakebailey** said "#1317 is closed and this PR is out of date; are you planning on updating it?"
 * (7 weeks ago) **RyanCavanaugh** set milestones to `Possible Improvement`, `Possible Improvement`
 * **RyanCavanaugh** added label `No linked issue`

### [Issue microsoft/TypeScript-go#2666](https://github.com/microsoft/TypeScript-go/issues/2666) (Open, `Needs Investigation`, **johnfav03**)

**\`tsgo \-\-build\` fails to invalidate incremental cache after dependency update**

*tsgo's --build incremental cache does not detect updated dependency types and ignores resulting type errors.*

 * [7 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2666#issuecomment-4247911575) **RyanCavanaugh** said "Confirmed repro, thanks @rubenferreira97 "
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * [6 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2666#issuecomment-4300070293) **rubenferreira97** described a hanging issue with tsgo --build due to stale .tsbuildinfo cache between versions and asked if they should open a new issue without a solid reproduction
 * (today) **RyanCavanaugh** set milestone to `Post-7.0`, and removed from milestone `TypeScript 7.0 RC`

### [PR microsoft/TypeScript-go#2907](https://github.com/microsoft/TypeScript-go/pull/2907) (Closed, **RyanCavanaugh**, **Copilot**)

**Fix issue 63192: infinite recursion when destructuring loop variables with defaults**

*Prevent infinite recursion in flow analysis of destructured loop variables with defaults by excluding binding elements from tryGetNameFromEntityNameExpression*

 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * [6 days ago](https://github.com/microsoft/TypeScript-go/pull/2907#issuecomment-4607912692) **RyanCavanaugh** said "@ahejlsberg 🔔"
 * [5 days ago](https://github.com/microsoft/TypeScript-go/pull/2907#issuecomment-4613084511) **ahejlsberg** said "The cause of the issue (i.e. the cause of the circularity) is https://github.com/microsoft/TypeScript/pull/56347."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2907#issuecomment-4652511791) **RyanCavanaugh** said "@copilot address the merge conflicts"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2907#issuecomment-4652624570) **Copilot** resolved merge conflicts in commit 4647bcc and adopted the main branch fix excluding binding elements in tryGetNameFromEntityNameExpression, dropping the earlier reentrancy guard for a simpler solution
 * [today](https://github.com/microsoft/TypeScript-go/pull/2907#issuecomment-4652969026) **ahejlsberg** said "This was fixed by #4191."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3271](https://github.com/microsoft/TypeScript-go/pull/3271) (Open, `No linked issue`)

**Fix for a snapshot update with a nil CommandLine**

*Add a nil check in NewProjectResponse to prevent panics when handling projects with nil CommandLine during snapshot updates.*

 * (7 weeks ago) **RyanCavanaugh** set milestones to `Post-7.0`, `TypeScript 7.0 RC`, and removed from milestone `Post-7.0`
 * (today) **RyanCavanaugh** added label `No linked issue`, set milestone to `Post-7.0`, and removed from milestone `TypeScript 7.0 RC`

### [PR microsoft/TypeScript-go#3297](https://github.com/microsoft/TypeScript-go/pull/3297) (Open, `No linked issue`)

**Allow global Symbol computed names during pseudochecker object literal serialization**

*Support global Symbol computed property names in pseudochecker object literal serialization to match Strada’s behavior.*

 * created by **Andarist**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * (today) **RyanCavanaugh** added label `No linked issue`, set milestone to `Post-7.0`, and removed from milestone `TypeScript 7.0 RC`

### [PR microsoft/TypeScript-go#3369](https://github.com/microsoft/TypeScript-go/pull/3369) (Open, `No linked issue`)

**Limit loader/emitter to GOMAXPROCS**

*Limit parsing and emitting workloads to a GOMAXPROCS-sized goroutine pool to prevent unbounded concurrency and stack growth.*

 * (7 weeks ago) **jakebailey** closed the issue
 * (6 weeks ago) **jakebailey** reopened the issue
 * **RyanCavanaugh** added to milestone `Possible Improvement`
 * **RyanCavanaugh** added label `No linked issue`

### [Issue microsoft/TypeScript-go#3491](https://github.com/microsoft/TypeScript-go/issues/3491) (Open, `Domain: Type Checking`, `Type Ordering`, **ahejlsberg**)

**Excess\-property check fires on a nested object literal that is later assigned to an annotated return type, where tsc 6\.0 does not**

*TS7 incorrectly flags excess-property errors on nested object literals assigned via an untyped variable to a typed return, unlike TS6*

 * (2 weeks ago) **ahejlsberg** added labels `Domain: Type Checking`, `Type Ordering`
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/3491#issuecomment-4491479178) **ahejlsberg** said "This appears to be a type ordering issue. Error also occurs with TS6 when compiled with --stableTypeOrdering."
 * (today) **ahejlsberg** added label `possible improvement`, removed label `possible improvement`, set milestone to `Possible Improvement`, and removed from milestone `TypeScript 7.0 RC`

### [PR microsoft/TypeScript-go#3505](https://github.com/microsoft/TypeScript-go/pull/3505) (Open, **johnfav03**)

**integrated filewatcher with lsp**

*Refactor vfswatch.FileWatcher for use by both CLI and LSP, integrating polling for clients without didChangeWatchedFiles support.*

 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3505#issuecomment-4345380442) **andrewbranch** suggested trying usePollingWatcher and noted that the LSP client watcher still ran, observed that it scanned the .git directory causing slow performance, started profiling and recommended manual testing
 * (1 month ago) **RyanCavanaugh** set milestone to `TypeScript 7.0 RC`, and assigned to **johnfav03**
 * **johnfav03** removed from milestone `TypeScript 7.0 RC`

### [PR microsoft/TypeScript-go#3515](https://github.com/microsoft/TypeScript-go/pull/3515) (Open, `No linked issue`, **navya9singh**)

**Expose formatNodeForInsertion in internal API**

*Add the formatNodeForInsertion function to the library’s internal API to enable its use by external modules.*

 * created by **andrewbranch**
 * (1 month ago) **RyanCavanaugh** set milestone to `TypeScript 7.0 RC`, and assigned to **navya9singh**
 * (today) **RyanCavanaugh** added label `No linked issue`, set milestone to `Possible Improvement`, and removed from milestone `TypeScript 7.0 RC`

### [PR microsoft/TypeScript-go#3616](https://github.com/microsoft/TypeScript-go/pull/3616) (Open, `No linked issue`)

**API \`emit\` support to generate \.d\.ts / \.js files from sources**

*Expose compiler emit in TSGO API and TypeScript client to generate .js and .d.ts files using virtual FS*

 * [1 month ago](https://github.com/microsoft/TypeScript-go/pull/3616#issuecomment-4418086735) **hegrec** asked if the PR would be merged and explained their use case for wrapping the emission pipeline with the virtual file system to capture d.ts content
 * [1 month ago](https://github.com/microsoft/TypeScript-go/pull/3616#issuecomment-4420025854) **pfumagalli** said "Resolved conflicts with upstream..."
 * **RyanCavanaugh** added to milestone `Possible Improvement`
 * **RyanCavanaugh** added label `No linked issue`

### [PR microsoft/TypeScript-go#3619](https://github.com/microsoft/TypeScript-go/pull/3619) (Open, `No linked issue`)

**perf: Make \`NodeArray\` no longer inherit from \`Array\`**

*Detach NodeArray from Array prototype to prevent direct array method usage and achieve significant performance gains.*

 * [6 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3619#issuecomment-4329156551) **andrewbranch** asked what made inheriting from Array expensive for materialization and guessed it was due to removing numeric index getters
 * [6 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3619#issuecomment-4329869917) **liuxingbaoyu** said "Yes, the issue is that Object.defineProperty is slow."
 * **RyanCavanaugh** added to milestone `Post-7.0`
 * (today) **RyanCavanaugh** added label `No linked issue`, set milestone to `Possible Improvement`, and removed from milestone `Post-7.0`

### [PR microsoft/TypeScript-go#3627](https://github.com/microsoft/TypeScript-go/pull/3627) (Open, `No linked issue`)

**Runtime tracing, flight recording**

*Integrate Go runtime/trace support and flight recording into the VS Code extension similarly to pprof profiling.*

 * created by **jakebailey**
 * **RyanCavanaugh** added to milestone `Possible Improvement`
 * **RyanCavanaugh** added label `No linked issue`

### [PR microsoft/TypeScript-go#3670](https://github.com/microsoft/TypeScript-go/pull/3670) (Open, **johnfav03**)

**Watcher build mode efficiency updates**

*Refactors tsc --build --watch to use a shared FileWatcher and trackingVFS structure, reducing code duplication and redundant dependency scanning.*

 * (1 month ago) **RyanCavanaugh** set milestone to `TypeScript 7.0 RC`, and assigned to **johnfav03**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3670#issuecomment-4642936422) **rubenferreira97** shared a test-only branch with two regression tests and described failures in dependency invalidation and path casing when building and watching
 * [today](https://github.com/microsoft/TypeScript-go/pull/3670#issuecomment-4652921979) **jakebailey** said "This PR's just out of date and needs a rethink after #3980 and co, so I wouldn't test it quite yet"
 * **johnfav03** removed from milestone `TypeScript 7.0 RC`

### [PR microsoft/TypeScript-go#3726](https://github.com/microsoft/TypeScript-go/pull/3726) (Open, **DanielRosenwasser**, **Copilot**)

**Preserve original stack traces in cross\-project panic handling**

*Wrap panics in PanicWithStack to capture and propagate original stack traces for cross-project panic handling.*

 * [1 month ago](https://github.com/microsoft/TypeScript-go/pull/3726#issuecomment-4392374682) **DanielRosenwasser** asked whether duplicate parts of the stack trace could be omitted
 * [1 month ago](https://github.com/microsoft/TypeScript-go/pull/3726#issuecomment-4392475333) **Copilot** fixed NewPanicWithStack to strip recovery infrastructure frames from the captured stack to prevent duplication in telemetry output
 * **RyanCavanaugh** added to milestone `Possible Improvement`
 * [today](https://github.com/microsoft/TypeScript-go/pull/3726#issuecomment-4652511528) **RyanCavanaugh** said "@copilot address the merge conflicts"

### [PR microsoft/TypeScript-go#3728](https://github.com/microsoft/TypeScript-go/pull/3728) (Open, `No linked issue`)

**Fix keyof deferred for non\-generic substitution types \(\#2186\)**

*Resolve keyof immediately for non-generic substitution types, fixing indexed access assignability and unsimplified quick info.*

 * [1 month ago](https://github.com/microsoft/TypeScript-go/pull/3728#issuecomment-4390943530) **adavila0703** quoted the Contributor License Agreement and instructions for agreeing
 * [1 month ago](https://github.com/microsoft/TypeScript-go/pull/3728#issuecomment-4402998409) **jakebailey** said "If this fixes #2186, can you write "Fixes #2186" in the description?"
 * **RyanCavanaugh** added to milestone `Post-7.0`
 * **RyanCavanaugh** added label `No linked issue`

### [PR microsoft/TypeScript-go#3826](https://github.com/microsoft/TypeScript-go/pull/3826) (Open, `No linked issue`)

**Add version & a common session identifier to events from LS clients**

*Include version and common session ID in language server client events to improve version-specific error tracking and correlate diagnostics.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3826#issuecomment-4442659320) **jakebailey** said "I don't think dotted names are legal names for end users of this?"
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3826#issuecomment-4444367810) **DanielRosenwasser** noted no indication that dotted names are illegal for end users and acknowledged possible error
 * **RyanCavanaugh** added to milestone `Possible Improvement`
 * **RyanCavanaugh** added label `No linked issue`

### [PR microsoft/TypeScript-go#3832](https://github.com/microsoft/TypeScript-go/pull/3832) (Closed)

**Add recursion limiter for \`TypeToString\`**

*Limit TypeToString recursion to two levels by returning "?" and discarding diagnostics to prevent infinite recursion and stack overflows.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3832#issuecomment-4443930434) **weswigham** explained that the root cause was allocating a new NodeBuilder on every XToString invocation which defeated circularity guards and opened issue #3833 with a fix
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3832#issuecomment-4445661370) **ahejlsberg** said "Closing in favor of #3833."
 * (3 weeks ago) **ahejlsberg** closed the issue
 * (today) **ahejlsberg** reopened the issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/3832#issuecomment-4653778017) **ahejlsberg** said "This also fixes https://github.com/microsoft/TypeScript/issues/63273, so I'm reopening. I think we should merge this as it is a general solution to an unknown number of latent circularities."

### [PR microsoft/TypeScript-go#3840](https://github.com/microsoft/TypeScript-go/pull/3840) (Open, `No linked issue`)

**Don't send bundled file watchers to client**

*Filter out bundled TypeScript library file patterns from LSP server watch requests to prevent invalid client watchers.*

 * (5 days ago) **RyanCavanaugh** set milestones to `TypeScript 7.0 RC`, `Possible Improvement`, and removed from milestone `TypeScript 7.0 RC`
 * (today) **RyanCavanaugh** added label `No linked issue`, set milestone to `Post-7.0`, and removed from milestone `Possible Improvement`

### [PR microsoft/TypeScript-go#3846](https://github.com/microsoft/TypeScript-go/pull/3846) (Closed, `No linked issue`)

**Find all references API endpoints**

*Request to implement API endpoints that return all references for specified code symbols.*

 * created by **navya9singh**
 * (today) **RyanCavanaugh** added label `No linked issue`, and set milestone to `Possible Improvement`

### [PR microsoft/TypeScript-go#3854](https://github.com/microsoft/TypeScript-go/pull/3854) (Closed)

**check that all files in \`"files"\` in tsconfig exist**

*Implement a check during tsconfig root file loading to confirm that all "files" entries exist.*

 * created by **iisaduan**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * [today](https://github.com/microsoft/TypeScript-go/pull/3854#issuecomment-4654368434) **iisaduan** implemented a new fix based on andrewbranch’s comments and requested a review, explaining the tsconfig-based file resolution with a cwd fallback

### [PR microsoft/TypeScript-go#3935](https://github.com/microsoft/TypeScript-go/pull/3935) (Open, `No linked issue`)

**Narrow keyword completions for concise arrow expression bodies**

*Port keyword completion filtering to Go so concise arrow function bodies only suggest expression keywords.*

 * created by **DhineshPonnarasan**
 * **RyanCavanaugh** added to milestone `Post-7.0`
 * **RyanCavanaugh** added label `No linked issue`

### [PR microsoft/TypeScript-go#3943](https://github.com/microsoft/TypeScript-go/pull/3943) (Open, `No linked issue`)

**Fix crash inferring constrained variadic tuples with optional elements**

*Fix compiler crash during inference of constrained variadic tuples with optional elements*

 * created by **Andarist**
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3943#issuecomment-4479716867) **jakebailey** said "We have a couple of PRs touching this same code, e.g. #3917, #2928; I feel a little unclear what combo is correct in all of these"
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * (today) **RyanCavanaugh** added label `No linked issue`, set milestone to `Post-7.0`, and removed from milestone `TypeScript 7.0 RC`

### [PR microsoft/TypeScript-go#3949](https://github.com/microsoft/TypeScript-go/pull/3949) (Open)

**feat: completion snippets**

*Add completion snippets functionality to enable snippet-based code suggestions during development.*

 * created by **a-tarasyuk**
 * (2 weeks ago) **a-tarasyuk** closed the issue
 * (later) **a-tarasyuk** reopened the issue

### [PR microsoft/TypeScript-go#3989](https://github.com/microsoft/TypeScript-go/pull/3989) (Open, `No linked issue`)

**lsp: emit VS\-internal HiddenInEditor tag for unnecessary diagnostics**

*Emit Visual Studio’s HiddenInEditor tag for Unnecessary diagnostics when vs_supportsVisualStudioExtensions is enabled so unused code fades in the editor*

 * created by **joj**
 * (today) **RyanCavanaugh** added label `No linked issue`, and set milestone to `Possible Improvement`

### [PR microsoft/TypeScript-go#3994](https://github.com/microsoft/TypeScript-go/pull/3994) (Open, **DanielRosenwasser**, **Copilot**)

**Fix external helper crash after module\-status updates**

*Ensure incremental program reuse refreshes synthetic tslib imports to prevent helper-resolution crashes when files change to modules.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3994#issuecomment-4492293827) **DanielRosenwasser** said "@copilot"
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3994#issuecomment-4492417437) **Copilot** addressed the request by adding a fourslash test and verifying it failed without the production fix
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * [today](https://github.com/microsoft/TypeScript-go/pull/3994#issuecomment-4652861463) **jakebailey** questioned the excessive code complexity and asked if a more compact, copyable form with deferred node creation could be used
 * [today](https://github.com/microsoft/TypeScript-go/pull/3994#issuecomment-4653255886) **DanielRosenwasser** said "@copilot explore @jakebailey's feedback."
 * [today](https://github.com/microsoft/TypeScript-go/pull/3994#issuecomment-4653468836) **jakebailey** said "I have no idea what copilot is doing. this is even more complicated and the large updateImportHelpersImportSpecifier remains"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3994#issuecomment-4653504695) **Copilot** addressed feedback by updating program reuse to store a compact lazy importHelpers specifier wrapper and defer creating the synthetic tslib AST node until first access while still updating resolution/include side tables

### [PR microsoft/TypeScript-go#3996](https://github.com/microsoft/TypeScript-go/pull/3996) (Open, `No linked issue`)

**Extract tscInput tests to individual per\-scenario files with imperative edits to improve debuggability**

*Extract tscInput tests into individual scenario files with imperative edits, remove intra-test parallelism, simplify debugging while preserving original tests.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3996#issuecomment-4500666020) **weswigham** said "The filename shouldn't start with a capital T but the function should, go figure. Fixed."
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3996#issuecomment-4500751011) **weswigham** asked if others preferred keeping test duplication for debuggability or the new test format and offered to delete originals and the extraction script
 * **RyanCavanaugh** added to milestone `Possible Improvement`
 * **RyanCavanaugh** added label `No linked issue`

### [PR microsoft/TypeScript-go#4007](https://github.com/microsoft/TypeScript-go/pull/4007) (Open, `No linked issue`)

**Accepted symbol baselines**

*Establish accepted symbol baselines before addressing bugs and investigations in a later pull request.*

 * created by **RyanCavanaugh**
 * (today) **RyanCavanaugh** added label `No linked issue`, and set milestone to `Possible Improvement`

### [PR microsoft/TypeScript-go#4024](https://github.com/microsoft/TypeScript-go/pull/4024) (Closed)

**Allow nil\-ing out arenas to break the GC link between nodes and the arena they came from**

*Allow arenas to be nilled out to sever GC links between nodes and their originating arenas, reducing diagnostic memory retention.*

 * created by **weswigham**
 * **RyanCavanaugh** added to milestone `Possible Improvement`
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript-go#4026](https://github.com/microsoft/TypeScript-go/pull/4026) (Open)

**Rebuilt CLI watcher around new \`fswatch\` package**

*The CLI watch command was rewritten to use OS-level fswatch events instead of polling, reducing idle CPU usage to under 1%.*

 * created by **johnfav03**
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4026#issuecomment-4521711233) **DanielRosenwasser** noted that the branch was based on the fswatch branch and that relevant changes start at commit 8230a72, then retracted the suggestion to use a stacked PR due to lacking access
 * (today) **RyanCavanaugh** added label `No linked issue`, and set milestone to `Possible Improvement`
 * **johnfav03** removed label `No linked issue`

### [PR microsoft/TypeScript-go#4058](https://github.com/microsoft/TypeScript-go/pull/4058) (Open)

**Reparse non\-identifier jsdoc names where possible, error otherwise**

*The parser now reparses non-identifier JSDoc names when possible and errors on unsupported nameless typedef patterns.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4058#issuecomment-4556668076) **weswigham** clarified that keywords were allowed as identifiers and that the check concerned only actual allowed characters in JS identifiers
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/4058#issuecomment-4635078850) **DanielRosenwasser** asked whether backtick-wrapped property names still work with the PR
 * [today](https://github.com/microsoft/TypeScript-go/pull/4058#issuecomment-4652004433) **weswigham** said "IIRC, it should - we parse both backticks and square brackets as jsdoc member name "quotes" (not changed here)."

### [Issue microsoft/TypeScript-go#4066](https://github.com/microsoft/TypeScript-go/issues/4066) (Closed, `Domain: Editor`, `Crash`, **DanielRosenwasser**, **gabritto**)

**Panic on file rename with solution\-style \`tsconfig\.json\`**

*File renaming with a solution-style tsconfig.json causes a nil pointer dereference panic in the Go-based TypeScript language service.*

 * (1 week ago) **DanielRosenwasser** added label `Crash`, and assigned to **gabritto**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#4067](https://github.com/microsoft/TypeScript-go/pull/4067) (Closed)

**Fix file rename crashes when dealing with solution configuration files**

*Prevent crashes when renaming solution configuration files by improving file rename handling.*

 * created by **DanielRosenwasser**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#4179](https://github.com/microsoft/TypeScript-go/pull/4179) (Open, `No linked issue`)

** Add custom/projectFiles LSP request**

*Add a custom LSP request to return all loaded projects and their source files for workspace initialization.*

 * created by **navya9singh**
 * [6 days ago](https://github.com/microsoft/TypeScript-go/pull/4179#issuecomment-4606298832) **gabritto** asked how Visual Studio would use the project information and whether having only partial project info was acceptable
 * [6 days ago](https://github.com/microsoft/TypeScript-go/pull/4179#issuecomment-4606882567) **navya9singh** explained how Visual Studio uses partial project information from the snapshot to populate the Roslyn workspace for the Task List and why partial data suffices
 * (today) **RyanCavanaugh** added label `No linked issue`, and set milestone to `Possible Improvement`

### [PR microsoft/TypeScript-go#4197](https://github.com/microsoft/TypeScript-go/pull/4197) (Open, `No linked issue`)

**prevent bundled library paths from being watched in resolution lookup**

*Skip watching embedded bundled library paths in resolution lookup glob patterns while still including real library directories.*

 * [5 days ago](https://github.com/microsoft/TypeScript-go/pull/4197#issuecomment-4619659269) **RyanCallahan312** said "@microsoft-github-policy-service agree"
 * [5 days ago](https://github.com/microsoft/TypeScript-go/pull/4197#issuecomment-4619743837) **RyanCallahan312** explained he was unsure why bundled mode was used, promised to provide a minimal reproduction, and summarized his Neovim setup and project configuration
 * [4 days ago](https://github.com/microsoft/TypeScript-go/pull/4197#issuecomment-4620753357) **jakebailey** asked how the build was obtained
 * (today) **RyanCavanaugh** added label `No linked issue`, and set milestone to `Post-7.0`

### [PR microsoft/TypeScript-go#4212](https://github.com/microsoft/TypeScript-go/pull/4212) (Closed, `No linked issue`)

**Update dependencies**

*Update dependencies to include the newly released LSP libraries.*

 * created by **jakebailey**
 * (today) **RyanCavanaugh** added label `No linked issue`, and set milestone to `Possible Improvement`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4214](https://github.com/microsoft/TypeScript-go/issues/4214) (Closed)

**Behavior difference: tsgo & tsc throw differently when spreading variable with type \`{}\`**

*tsgo and tsc report property-not-found errors on different destructuring patterns involving default empty object assignments.*

 * created by **hkleungai**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and set milestone to `Post-7.0`
 * [today](https://github.com/microsoft/TypeScript-go/issues/4214#issuecomment-4654615602) **ahejlsberg** explained that a bug in TS6 caused inconsistent errors between .js and .ts files and was fixed in TS7
 * **ahejlsberg** removed label `Needs Investigation`
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#4215](https://github.com/microsoft/TypeScript-go/issues/4215) (Open, `Domain: API and Extensibility`)

**\`SourceFile\` is missing \`\.getLineStarts\(\)\` and \`\.getLineAndCharacterOfPosition\(\)\`**

*Add getLineStarts() and getLineAndCharacterOfPosition() getters to SourceFile for convenient API usage.*

 * created by **mrazauskas**
 * (today) **RyanCavanaugh** added label `Domain: API and Extensibility`, and set milestone to `Post-7.0`

### [Issue microsoft/TypeScript-go#4216](https://github.com/microsoft/TypeScript-go/issues/4216) (Open, `Domain: API and Extensibility`)

**\`Node\` is missing \`getFullStart\(\)\`, \`getStart\(\)\` and other getters**

*Add missing getters (getFullStart, getStart, getFullWidth, getWidth, getLeadingTriviaWidth, getFullText, getText) to Node to improve API usability.*

 * created by **mrazauskas**
 * (today) **RyanCavanaugh** added label `Domain: API and Extensibility`, and set milestone to `Post-7.0`

### [Issue microsoft/TypeScript-go#4217](https://github.com/microsoft/TypeScript-go/issues/4217) (Closed, `wontfix`)

**Behavior difference: TS2741 diagnostic misalignment observed for nested array / object literals**

*tsgo fails to report TS2741 for nested object literal assignments missing the required 'missing' property, unlike tsc.*

 * created by **hkleungai**
 * **RyanCavanaugh** added label `wontfix`
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#4218](https://github.com/microsoft/TypeScript-go/pull/4218) (Open)

**Allow lone & in Unicode sets regexp classes**

*Update native scanner to allow lone & in Unicode Set regex character classes while preserving && intersections.*

 * created by **Ijtihed**
 * **RyanCavanaugh** added to milestone `Post-7.0`

### [Issue microsoft/TypeScript-go#4222](https://github.com/microsoft/TypeScript-go/issues/4222) (Closed, `wontfix`)

**isolatedDeclarations: TS9007/TS9008 replaced by TS9039/TS9013 on the return expression**

*tsgo’s isolatedDeclarations option emits TS9039 and TS9013 errors on return expressions instead of expected TS9007/TS9008 errors.*

 * created by **mds-ant**
 * **RyanCavanaugh** added label `wontfix`
 * [today](https://github.com/microsoft/TypeScript-go/issues/4222#issuecomment-4652184076) **RyanCavanaugh** said "We're generally OK with error spans moving around. These seem equally good."
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#4225](https://github.com/microsoft/TypeScript-go/issues/4225) (Closed, `possible improvement`, **jakebailey**, **Copilot**)

**'Expected N type arguments' position does not skip trivia after '\<'**

*tsgo incorrectly reports error positions by not skipping whitespace after '<' when determining type argument counts.*

 * created by **mds-ant**
 * (2 days ago) **jakebailey** assigned to **Copilot**, **jakebailey**
 * (today) **RyanCavanaugh** added label `possible improvement`, and set milestone to `Possible Improvement`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4226](https://github.com/microsoft/TypeScript-go/pull/4226) (Open, `No linked issue`)

**Convert \`valueSymbolLinks\` and \`symbolNodeLinks\` to id\-paged arrays**

*Replace valueSymbolLinks and symbolNodeLinks map stores with ID-paged arrays to reduce hash lookup costs and improve typechecking performance*

 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/4226#issuecomment-4639982017) **ahejlsberg** highlighted performance gains and memory trade-offs of using dense node and symbol IDs, noting potential costs for less common links and increasing memory usage over long sessions
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/4226#issuecomment-4640495531) **mds-ant** tried converting a handful more stores to the page array scheme but observed increased memory usage, suggested converting only valueSymbolLinks and symbolNodeLinks for performance gains, asked if there was precedent for enabling optimizations only for batch compilations and retaining the existing link store for the language server use case
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/4226#issuecomment-4640630251) **jakebailey** suggested that it'd require a runtime switch but could be noted on Program or Checker creation, though found it weird
 * (today) **RyanCavanaugh** added label `No linked issue`, and set milestone to `Possible Improvement`

### [Issue microsoft/TypeScript-go#4230](https://github.com/microsoft/TypeScript-go/issues/4230) (Open, `documentation`)

**Behavior difference: tsgo no longer infer variadic \`args\` type when \`arguments\[\.\.\.\]\` is referenced inside plain js function body**

*tsgo no longer infers variadic args in plain JS functions referencing 'arguments', causing missing rest parameter types.*

 * created by **hkleungai**
 * **RyanCavanaugh** added label `documentation`
 * [today](https://github.com/microsoft/TypeScript-go/issues/4230#issuecomment-4652287482) **RyanCavanaugh** said "Let's just add this (no more arguments-based ...args) inference to CHANGES.md"
 * **RyanCavanaugh** added to milestone `Possible Improvement`
 * [today](https://github.com/microsoft/TypeScript-go/issues/4230#issuecomment-4654215064) **ahejlsberg** said "@RyanCavanaugh Agreed. Specifically, in Strada, when a function body references arguments somewhere in an expression, we include a ...args parameter. We no longer do this in Corsa."
 * [today](https://github.com/microsoft/TypeScript-go/issues/4230#issuecomment-4656519612) **hkleungai** asked if it was possible to add it back to TS7 and explained issues with arguments inference and jsdoc typing errors

### [PR microsoft/TypeScript-go#4231](https://github.com/microsoft/TypeScript-go/pull/4231) (Closed, **jakebailey**, **Copilot**)

**Skip trivia after '\<' in type\-argument arity error spans**

*Modifies TypeScript's type-argument arity diagnostics to skip trivia after '<' so error spans start at the first type argument.*

 * created by **Copilot**
 * (2 days ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * **RyanCavanaugh** added to milestone `Possible Improvement`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4234](https://github.com/microsoft/TypeScript-go/pull/4234) (Open, `No linked issue`)

**Skip mark/rewind in \`tryParseTypeArgumentsInExpression\` when token isn't \`\<\`**

*Optimize tryParseTypeArgumentsInExpression by skipping parser mark/rewind overhead when the token isn't '<', improving performance.*

 * created by **mds-ant**
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/4234#issuecomment-4640652269) **jakebailey** said "Do you have a benchmark that would show where this matters? And how often it matters?"
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/4234#issuecomment-4640655237) **mds-ant** committed to adding a benchmark before marking the PR ready for review
 * (today) **RyanCavanaugh** added label `No linked issue`, and set milestone to `Possible Improvement`
 * [today](https://github.com/microsoft/TypeScript-go/pull/4234#issuecomment-4652925956) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4234#issuecomment-4652926633) **typescript-automation[bot]** noted CI jobs started and linked to results
 * [today](https://github.com/microsoft/TypeScript-go/pull/4234#issuecomment-4653159218) **typescript-automation[bot]** provided the requested performance run results

### [Issue microsoft/TypeScript-go#4235](https://github.com/microsoft/TypeScript-go/issues/4235) (Closed, `bug`)

**Behavior difference: tsgo no longer emits comment on \`@typedef\` style object attributes**

*tsgo no longer preserves JSDoc comments on object properties defined via @typedef, causing missing documentation in emitted types.*

 * created by **hkleungai**
 * (today) **RyanCavanaugh** added label `bug`, and set milestone to `Post-7.0`

### [Issue microsoft/TypeScript-go#4236](https://github.com/microsoft/TypeScript-go/issues/4236) (Open, `possible improvement`)

**\[Post\-7\.0\] Improve readability of \`Array\.from\` / \`TypedArray\.from\` \`mapFn\` parameters**

*Rename Array.from and TypedArray.from mapFn parameter names from v and k to element and index for improved IDE tooltip readability.*

 * created by **AXT-AyaKoto**
 * (today) **RyanCavanaugh** added label `possible improvement`, set milestones to `Post-7.0`, `Possible Improvement`, and removed from milestone `Post-7.0`

### [Issue microsoft/TypeScript-go#4237](https://github.com/microsoft/TypeScript-go/issues/4237) (Closed, `Domain: API and Extensibility`, **jakebailey**, **Copilot**)

**Consider shipping API enums without the \`const\` modifier**

*Ship API enums without the const modifier to prevent compile-time inlining and align with Strada*

 * created by **mrazauskas**
 * (today) **RyanCavanaugh** added label `Domain: API and Extensibility`, and set milestone to `Post-7.0`
 * [today](https://github.com/microsoft/TypeScript-go/issues/4237#issuecomment-4652895867) **jakebailey** suggested not shipping const enums in d.ts files and tolerating performance overhead until proven necessary
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4238](https://github.com/microsoft/TypeScript-go/pull/4238) (Open, `No linked issue`)

**Several performance optimizations for the scanner's hot path**

*Fast-path scanner optimizations, including ASCII byte handling and a scanASCIIWhile helper, reduce parse times by ~7.5%.*

 * created by **mds-ant**
 * (today) **RyanCavanaugh** added label `No linked issue`, and set milestone to `Possible Improvement`
 * [today](https://github.com/microsoft/TypeScript-go/pull/4238#issuecomment-4652885657) **jakebailey** criticized the hand-inlining in recent commits and asked to reorganize charAndSize to use outlined slow path with fast inlined path
 * [today](https://github.com/microsoft/TypeScript-go/pull/4238#issuecomment-4653588903) **mds-ant** said "That's good feedback. Let me see if we can leverage the "outlined" optimization approach here."
 * [later](https://github.com/microsoft/TypeScript-go/pull/4238#issuecomment-4658478731) **mds-ant** introduced a new scanASCIIWhile helper to efficiently advance the scanner over ASCII bytes when other inlining approaches exceeded the 80-byte budget

### [PR microsoft/TypeScript-go#4239](https://github.com/microsoft/TypeScript-go/pull/4239) (Open, `No linked issue`)

**Replace ForEachReturnStatement closure with direct kind\-switched walk**

*Replace ForEachReturnStatement closure with a direct kind-switched recursive function to reduce allocations and improve performance.*

 * created by **mds-ant**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4239#issuecomment-4650627368) **jakebailey** mentioned that the hyperfine benchmark comparison was omitted and suspected the difference might be within noise
 * [today](https://github.com/microsoft/TypeScript-go/pull/4239#issuecomment-4651179882) **jakebailey** said "This is probably fine, but an alternative approach would have been to copy the parent pointer code where we just reuse the closure, I think."
 * [today](https://github.com/microsoft/TypeScript-go/pull/4239#issuecomment-4651829699) **DanielRosenwasser** said "@typescript-bot perf test this"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4239#issuecomment-4651830244) **typescript-automation[bot]** displayed the start of perf test builds with status and result links
 * [today](https://github.com/microsoft/TypeScript-go/pull/4239#issuecomment-4652072023) **typescript-automation[bot]** provided requested performance run results including a tsc metrics comparison report
 * (today) **RyanCavanaugh** added label `No linked issue`, and set milestone to `Possible Improvement`

### [PR microsoft/TypeScript-go#4240](https://github.com/microsoft/TypeScript-go/pull/4240) (Open, `No linked issue`)

**Inline \`GetCombinedNodeFlags\` and \`GetCombinedModifierFlags\` bodies**

*Inline flag computations by replacing generic helper with direct node field reads, boosting performance by about 27%.*

 * created by **mds-ant**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4240#issuecomment-4651191129) **jakebailey** said "This is a microoptimization; do you have anything that says this is hot code? The old times are already microseconds."
 * (today) **RyanCavanaugh** added label `No linked issue`, and set milestone to `Possible Improvement`
 * [today](https://github.com/microsoft/TypeScript-go/pull/4240#issuecomment-4652510901) **mds-ant** noted that a small but measurable performance win from a codebase audit was worth landing since it didn't add complexity or maintenance burden
 * [today](https://github.com/microsoft/TypeScript-go/pull/4240#issuecomment-4652521791) **jakebailey** said "Hm, but as the copilot comment notes, this involves a copy paste"
 * [later](https://github.com/microsoft/TypeScript-go/pull/4240#issuecomment-4658350219) **mds-ant** noted that code duplication was necessary to enable the optimization, explained the trade-offs of a shared helper, and offered to close the PR if the duplication is unwanted

### [PR microsoft/TypeScript-go#4242](https://github.com/microsoft/TypeScript-go/pull/4242) (Open)

**Fix stack overflow crash in base constraint resolution**

*Add recursion limiting to base constraint resolution for conditional types to prevent stack overflow crashes.*

 * created by **ahejlsberg**
 * **RyanCavanaugh** added to milestone `Post-7.0`

### [PR microsoft/TypeScript-go#4243](https://github.com/microsoft/TypeScript-go/pull/4243) (Closed, **jakebailey**, **Copilot**)

**Ship API enums without the const modifier**

*Convert API enums in the native-preview package from const enums to regular enums to prevent value inlining.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4244](https://github.com/microsoft/TypeScript-go/issues/4244) (Open, `Crash`, `Needs More Info`)

**Fatal server error: nil Session from \`flushChangesLocked\(\)\`**

*Server crashes with a fatal nil pointer dereference in Session.flushChangesLocked caused by an unexpected nil session.*

 * created by **DanielRosenwasser**
 * **DanielRosenwasser** added label `Crash`
 * **RyanCavanaugh** added label `Needs More Info`

### [Issue microsoft/TypeScript-go#4245](https://github.com/microsoft/TypeScript-go/issues/4245) (Closed, `Crash`, **DanielRosenwasser**, **Copilot**)

**Fatal error in \`onPropertySet\` in \`parseOwnConfigOfJsonSourceFile\`**

*A fatal error in onPropertySet within parseOwnConfigOfJsonSourceFile causes crashes when parsing tsconfig JSON files.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** added label `Crash`, and assigned to **Copilot**, **DanielRosenwasser**
 * (later) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#4246](https://github.com/microsoft/TypeScript-go/pull/4246) (Closed, **DanielRosenwasser**, **Copilot**)

**Fix nil value panic in getExtendsConfigPathOrArray**

*Add a nil check in getExtendsConfigPathOrArray to prevent panics on null extends values and produce proper error diagnostics.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4246#issuecomment-4654380475) **Copilot** moved the regression from the compiler testcase into an execute-level tsc unit test and removed the compiler case/baselines
 * (later) **DanielRosenwasser** closed the issue

### [Issue microsoft/TypeScript-go#4247](https://github.com/microsoft/TypeScript-go/issues/4247) (Open, `Crash`, **DanielRosenwasser**, **Copilot**)

**Fatal error during resolution through \`RootLength\`**

*A non-absolute path passed to vfs/internal.RootLength triggers a panic and aborts module resolution.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** added label `Crash`, and assigned to **Copilot**, **DanielRosenwasser**

### [PR microsoft/TypeScript-go#4248](https://github.com/microsoft/TypeScript-go/pull/4248) (Open, **DanielRosenwasser**, **Copilot**)

**Fix fatal panic on non\-absolute path in VFS**

*Update VFS RootLength, SplitPath, and RootAndPath to return defaults for non-absolute paths instead of panicking.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * [later](https://github.com/microsoft/TypeScript-go/pull/4248#issuecomment-4661380146) **DanielRosenwasser** said "@copilot+gpt-5.5 you did not add a test"
 * [later](https://github.com/microsoft/TypeScript-go/pull/4248#issuecomment-4661516807) **Copilot** added a focused regression test covering ResolveModuleName('./foo', '', ...) to exercise the non-absolute VFS lookup path that previously panicked; noted in commit f7f88aae

### [Issue microsoft/TypeScript-go#4249](https://github.com/microsoft/TypeScript-go/issues/4249) (Open, `Domain: API and Extensibility`)

**\`\.getProgramDiagnostics\(\)\` is missing in the API**

*Add an API method like program.getProgramDiagnostics or project.getProjectDiagnostics to retrieve missing compiler options diagnostics.*

 * created by **mrazauskas**

### [PR microsoft/TypeScript-go#4250](https://github.com/microsoft/TypeScript-go/pull/4250) (Closed, **weswigham**)

**preserve jsdoc prop descriptions in declaration emit**

*Retain JSDoc property descriptions when emitting TypeScript declaration files.*

 * created by **a-tarasyuk**

### [Issue microsoft/TypeScript-go#4251](https://github.com/microsoft/TypeScript-go/issues/4251) (Closed, `bug`, **jakebailey**, **Copilot**)

**Triple slash reference does not emit files from referenced ts projects**

*tsgo omits triple slash reference paths in generated declaration files for referenced TypeScript projects, unlike tsc.*

 * created by **HolgerJeromin**

