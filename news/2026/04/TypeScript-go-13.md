# Report for 2026-04-13 (Monday, April 13th, 2026)

9 different users commented on 29 different issues.

## Recommended Actions

 * Response Recommended
    * @vetptzru offered to run further tests on either PR in [microsoft/TypeScript-go#3139](https://github.com/microsoft/TypeScript-go/issues/3139#issuecomment-4243894760)

## Activity Summary

### [Issue microsoft/TypeScript-go#1317](https://github.com/microsoft/TypeScript-go/issues/1317) (Closed, `Domain: CLI`, `Domain: Performance`, **johnfav03**)

**High CPU usage with \-\-watch when idling on MacOS**

*Running tsgo in watch mode on MacOS consumes abnormally high CPU (120–170%) even when idle, unlike tsc -w.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1317#issuecomment-4124796852) **alexswan93** reported similar idle CPU usage on Windows in watch mode with @typescript/native-preview v7.0.0-dev.20260324.1 and noted using tsgo as a workaround
 * (2 weeks ago) **RyanCavanaugh** set milestone to `TypeScript 7.0 RC`, and assigned to **johnfav03**
 * (today) **johnfav03** closed the issue

### [Issue microsoft/TypeScript-go#2317](https://github.com/microsoft/TypeScript-go/issues/2317) (Closed, `bug`, **johnfav03**)

**Console is not cleared in watch mode \(also does not show the 0 error count output\)**

*tsgo’s watch mode fails to clear the console between builds and omits the “Found 0 errors” message*

 * [17 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2317#issuecomment-3638438200) **jakebailey** said "Well, rather, I think the watch mode for non-build-mode is just not using the right messages."
 * (2 weeks ago) **RyanCavanaugh** added label `bug`, and assigned to **johnfav03**
 * (today) **johnfav03** closed the issue

### [Issue microsoft/TypeScript-go#2457](https://github.com/microsoft/TypeScript-go/issues/2457) (Closed, `feature parity`, **jakebailey**)

**Proposal: Prettified type display in hover output**

*Add optional settings to display prettified, expanded types in hover output for better readability.*

 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2457#issuecomment-4005963689) **rubnogueira** said "This is part of TypeScript 5.9: https://devblogs.microsoft.com/typescript/announcing-typescript-5-9-beta/#expandable-hovers-(preview) but it's not implemented in tsgo."
 * (2 weeks ago) **RyanCavanaugh** added label `feature parity`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2637](https://github.com/microsoft/TypeScript-go/issues/2637) (Closed, `Domain: Editor`, **johnfav03**)

**Update import via Quick Fix breaks import formatting**

*Quick Fix import update breaks one-line named import formatting by adding an extra newline and misplacing the closing bracket.*

 * created by **erengeez**
 * **erengeez** added label `Domain: Editor`
 * **RyanCavanaugh** assigned to **johnfav03**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2637#issuecomment-4239045580) **johnfav03** said "﻿Fixed by #2978 and #2869"
 * (today) **johnfav03** closed the issue

### [Issue microsoft/TypeScript-go#2640](https://github.com/microsoft/TypeScript-go/issues/2640) (Closed, `bug`, **johnfav03**)

**tsgo \-\-watch is lagging and sometimes not emitting at all**

*tsgo watch mode intermittently fails to emit updates promptly or at all when source files change*

 * created by **tharakadesilva**
 * (2 weeks ago) **RyanCavanaugh** added label `bug`, and assigned to **johnfav03**
 * (today) **johnfav03** closed the issue

### [Issue microsoft/TypeScript-go#2656](https://github.com/microsoft/TypeScript-go/issues/2656) (Closed, `bug`, **ahejlsberg**)

**Exports are no longer recognized in js modules which contain functions with parameter called \`module\` which have \`module\.exports =\` in their body**

*A function parameter named module with module.exports in it prevents tsgo from recognizing exports while TypeScript 5.9 accepts them.*

 * created by **peetklecha**
 * (2 weeks ago) **RyanCavanaugh** added label `bug`, and assigned to **ahejlsberg**
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#2780](https://github.com/microsoft/TypeScript-go/issues/2780) (Open, `Domain: Editor`, `Needs More Info`, **andrewbranch**)

**High memory consumption in a large pnpm monorepo**

*PR #2502 causes minor edits in a large pnpm monorepo to spike the TypeScript extension memory from ~700MB to ~35GB.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-4158120316) **ozyx** reported experiencing a massive memory leak in a large pnpm monorepo when using tsgo and offered to gather debug info
 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-4205839648) **xenokratos** reported experiencing the same issue on a large monorepo and attached a screenshot
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-4228201267) **shinichy** explained why Strada language service didn’t exhibit the issue, implemented the same NodeResolutionFeaturesExports check in Corsa with code and tsconfig updates, and observed reduced memory usage before offering to submit a PR
 * [today](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-4238016842) **andrewbranch** explained the registry was working as intended with hard-coded options and could not depend on project compiler options since its contents are shared across projects, noted that building registry contents per node_modules directory with the first project’s options would be incomplete for other projects, and mentioned that `--moduleResolution node` is deprecated in 6.0 and unsupported in 7.0
 * [today](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-4241230123) **shinichy** said "Hmm, does that mean there's no way to limit the entry point search scope to just the main entry point in tsgo?"
 * [later](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-4244950544) **andrewbranch** stated that the issue was likely caused by a fixable logic bug in a code path only exercised by an entrypoint included via "exports", rather than by scanning too many legitimate entrypoints

### [PR microsoft/TypeScript-go#2944](https://github.com/microsoft/TypeScript-go/pull/2944) (Open)

**\[draft\] more formatting tests **

*Add draft formatting tests to validate and troubleshoot the repository’s testing pipelines.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/2944#issuecomment-4195436692) **iisaduan** said "@typescript-bot perf test this"
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/2944#issuecomment-4195437043) **typescript-bot** noted that CI build started and posted status update
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/2944#issuecomment-4195501446) **typescript-bot** posted the requested performance run results
 * [today](https://github.com/microsoft/TypeScript-go/pull/2944#issuecomment-4238228195) **typescript-bot** provided performance run results
 * [today](https://github.com/microsoft/TypeScript-go/pull/2944#issuecomment-4238257454) **typescript-bot** said "@iisaduan, the perf run you requested failed. You can check the log here."

### [Issue microsoft/TypeScript-go#3014](https://github.com/microsoft/TypeScript-go/issues/3014) (Closed, `bug`, **johnfav03**)

**\`tsgo \-\-watch\` hangs if given a tsconfig\.json with no files**

*tsgo --watch hangs indefinitely when run on a tsconfig.json configuration that specifies no files*

 * created by **DanielRosenwasser**
 * (2 weeks ago) **RyanCavanaugh** added label `bug`, and assigned to **johnfav03**
 * (today) **johnfav03** closed the issue

### [Issue microsoft/TypeScript-go#3015](https://github.com/microsoft/TypeScript-go/issues/3015) (Closed, `Crash`, **johnfav03**)

**panic on \`\-\-watch\` and \`\-\-explainFiles\`**

*Using tsgo with --watch and --explainFiles flags triggers a nil pointer dereference panic.*

 * (5 weeks ago) **DanielRosenwasser** added labels `Crash`, `Crash`
 * **RyanCavanaugh** assigned to **johnfav03**
 * (today) **johnfav03** closed the issue

### [Issue microsoft/TypeScript-go#3120](https://github.com/microsoft/TypeScript-go/issues/3120) (Open, `Crash`, **iisaduan**)

**thread exhaustion \- program exceeds 10000\-thread limit \- one off error**

*An unreproducible Go runtime crash arises when the program exceeds the 10000-thread limit.*

 * **lukpsaxo** added label `Crash`
 * **RyanCavanaugh** assigned to **iisaduan**
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/3120#issuecomment-4229269618) **ekazakov14** reported experiencing the same intermittent error in CI/CD with a large project and provided their tsgo version
 * [today](https://github.com/microsoft/TypeScript-go/issues/3120#issuecomment-4239471509) **jakebailey** said "It's possible that this would be fixed in the same way as #3139."
 * [today](https://github.com/microsoft/TypeScript-go/issues/3120#issuecomment-4239474401) **jakebailey** said "@ekazakov14 Can you try https://github.com/microsoft/typescript-go/pull/3369 or https://github.com/microsoft/typescript-go/pull/3394?"

### [Issue microsoft/TypeScript-go#3139](https://github.com/microsoft/TypeScript-go/issues/3139) (Open, `Needs More Info`)

**runtime: failed to create new OS thread**

*Running tsgo on a large macFUSE-mounted TypeScript project exhausts OS threads and crashes the Go runtime.*

 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/3139#issuecomment-4215101482) **jakebailey** said "I'm not sure if that's going to be the fix, as it very much hurts everyone else's perf."
 * [today](https://github.com/microsoft/TypeScript-go/issues/3139#issuecomment-4235424817) **vetptzru** proposed making the concurrency limit configurable to allow teams using macFUSE to opt in while keeping default unbounded performance for native filesystems
 * [today](https://github.com/microsoft/TypeScript-go/issues/3139#issuecomment-4237328560) **jakebailey** rejected adding a flag and asked to retry the PR after recent changes
 * [today](https://github.com/microsoft/TypeScript-go/issues/3139#issuecomment-4237844283) **vetptzru** tested the latest changes on macFUSE and reported that everything worked correctly
 * [today](https://github.com/microsoft/TypeScript-go/issues/3139#issuecomment-4238182509) **jakebailey** said "Can you also try https://github.com/microsoft/typescript-go/pull/3394?"
 * [later](https://github.com/microsoft/TypeScript-go/issues/3139#issuecomment-4243894760) **vetptzru** tested PR #3394 on macFUSE and confirmed it resolved the issue without crashing, observed normal thread counts, and offered to run further tests

### [PR microsoft/TypeScript-go#3167](https://github.com/microsoft/TypeScript-go/pull/3167) (Closed)

**Fix: skip CommonJS export binding when module or exports is a local variable**

*Skips binding CommonJS exports when module or exports is locally defined to avoid shadowing ESM exports and spurious diagnostics.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3167#issuecomment-4099806795) **jakebailey** questioned clearing the CJS indicator mid walk and suggested guarding the initial assignment instead
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3167#issuecomment-4100028136) **Muhammad-Bin-Ali** agreed with the suggestion to guard the assignment and said they would implement it
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3167#issuecomment-4105043960) **Muhammad-Bin-Ali** explained that there was no clean way to solve the problem earlier in the walk and modified the approach and added tests to address the issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/3167#issuecomment-4239882286) **jakebailey** said "Superseded by #3388"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3217](https://github.com/microsoft/TypeScript-go/pull/3217) (Closed)

**Watch cli efficiency update**

*Watch CLI efficiency improvements implement debouncing, configuration caching, and dependency parsing to avoid unnecessary recompilations.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3217#issuecomment-4194915866) **johnfav03** thanked for the race tests and added mutexes to the Watcher and FileWatcher structs to fix race conditions and confirmed no race warnings with Copilot tests
 * [5 days ago](https://github.com/microsoft/TypeScript-go/pull/3217#issuecomment-4208738400) **jakebailey** suggested not blocking the PR on LSP support, recommended using dotnet's built-in watcher for manual watch requests, and asked @joj and @navya9singh about feasibility
 * [4 days ago](https://github.com/microsoft/TypeScript-go/pull/3217#issuecomment-4215918343) **johnfav03** combined SetWildcardDirectories and UpdateWatchedFiles into UpdateWatchState and stated plans to open a new PR for the second suggestion after feedback
 * (today) **johnfav03** closed the issue

### [PR microsoft/TypeScript-go#3311](https://github.com/microsoft/TypeScript-go/pull/3311) (Closed)

**Add expandable hover**

*Implement an expandable hover feature in VSCode by adding a custom API over LSP and swapping hover providers.*

 * created by **jakebailey**
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3311#issuecomment-4173489594) **jakebailey** suggested that symbolTableToDeclarationStatements might need a rethink now that JS declaration emit has changed
 * [today](https://github.com/microsoft/TypeScript-go/pull/3311#issuecomment-4238287036) **gabritto** asked whether there is a guarantee that expandable type references will always lack a resolved symbol so that the algorithm computes canIncreaseVerbosity correctly
 * [today](https://github.com/microsoft/TypeScript-go/pull/3311#issuecomment-4238635664) **jakebailey** explained that nil falls through to typeToTypeNode and non-nil goes through walkNodeForExpandability, and asked if there was another scenario they might be missing
 * [today](https://github.com/microsoft/TypeScript-go/pull/3311#issuecomment-4238796042) **gabritto** understood how the logic flow works
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3345](https://github.com/microsoft/TypeScript-go/pull/3345) (Closed)

**Reparse CJS export assignments only when not shadowed by locals**

*Parser now tracks local module and exports shadowing to prevent misparsing CommonJS export assignments.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3345#issuecomment-4194649465) **ahejlsberg** explained that cjs-module-lexer didn't perform scope analysis and discussed complications with module detection in TypeScript regarding mixed CJS/ESM code
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3345#issuecomment-4194814881) **jakebailey** noted that reparsing was problematic because ESM constructs may appear later, mentioned that PR #3167 attempted to solve it in the binder, and expressed dissatisfaction with doing binder-esque work in the parser
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3345#issuecomment-4194857584) **ahejlsberg** agreed and suggested eliminating JSExportAssignment and CommonJSExport reparsing in reparseCommonJS and instead binding and checking them as in Strada, ignoring CJS constructs in ESM modules
 * [today](https://github.com/microsoft/TypeScript-go/pull/3345#issuecomment-4239881854) **jakebailey** said "Superseded by #3388"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3358](https://github.com/microsoft/TypeScript-go/pull/3358) (Open, **gabritto**)

**Implement LSP\-based code edits with file renaming**

*Implement LSP willRenameFiles support to perform file renames with module specifier updates and arbitrary extension handling.*

 * created by **Andarist**
 * **gabritto** assigned to **gabritto**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3358#issuecomment-4238669742) **jakebailey** said "This also closes #1882, yes?"

### [Issue microsoft/TypeScript-go#3370](https://github.com/microsoft/TypeScript-go/issues/3370) (Open, `duplicate`)

**Bad inference for param of type T\[\] \| T\[\]\[\]**

*tsgo misinfers the generic type as an extra array level when narrowing T[] | T[][]*

 * created by **jsnajdr**
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/3370#issuecomment-4213268869) **JoostK** said "Sounds like https://github.com/microsoft/typescript-go/issues/1789"
 * **ahejlsberg** added label `duplicate`

### [PR microsoft/TypeScript-go#3383](https://github.com/microsoft/TypeScript-go/pull/3383) (Closed)

**Fix see/link hover scoping**

*Port container-setting functions for JSDoc see/link hover scoping while preserving comments at removed calls.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3384](https://github.com/microsoft/TypeScript-go/issues/3384) (Open, `Crash`)

**Crash in adjusting positions for folding ranges**

*Adjusting folding range end positions in the Go language service now crashes due to LineAndCharacterToPosition conversion errors.*

 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/3384#issuecomment-4226609473) **jakebailey** said "What is the actual message?"
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/3384#issuecomment-4226616160) **DanielRosenwasser** said "No idea - we only keep the stack around."
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/3384#issuecomment-4227398094) **DanielRosenwasser** suspected the issue stemmed from the snapshotfs implementation because reloadEntry methods didn’t update certain fields and noted difficulty reproducing it end-to-end
 * [today](https://github.com/microsoft/TypeScript-go/issues/3384#issuecomment-4239589443) **jakebailey** said "Not overwriting those definitely feels like a bug. We should probably shove those off into a sidecar that can be overwritten with a new object each time the content changes."

### [PR microsoft/TypeScript-go#3388](https://github.com/microsoft/TypeScript-go/pull/3388) (Closed)

**No reparsing of CommonJS constructs**

*Remove re-parsing of CommonJS constructs and instead handle module.exports and exports in the binder and checker, ignoring CJS in ES modules.*

 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/3388#issuecomment-4229964129) **ahejlsberg** identified that the dprint issue occurred when the drive letter in the working directory was lower-case c: but succeeded when it was upper-case C:
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/3388#issuecomment-4230235843) **jakebailey** noted that PowerShell does not allow changing into a lowercase drive and asked if adding a directory change workaround at the top of Herebyfile.mjs would fix it
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/3388#issuecomment-4230326122) **ahejlsberg** confirmed that adding the code at the top of Herebyfile.mjs made it work
 * [today](https://github.com/microsoft/TypeScript-go/pull/3388#issuecomment-4239345804) **ahejlsberg** described that the binder now automatically declares module and exports in CJS modules, improving statement completion, symbol baselines, and simplifying the name resolver
 * [today](https://github.com/microsoft/TypeScript-go/pull/3388#issuecomment-4239446132) **jakebailey** said "There's a merge conflict in the generated code that needs to be resolved."
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#3389](https://github.com/microsoft/TypeScript-go/issues/3389) (Closed, `Domain: API and Extensibility`, **andrewbranch**)

**Factory statement and type declaration nodes do not emit export modifier**

*Factory-created type alias declarations and statements fail to include the export modifier when printed due to missing createNodeArray calls for modifiers.*

 * created by **virtulis**
 * (today) **andrewbranch** added label `Domain: API and Extensibility`, and assigned to **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#3390](https://github.com/microsoft/TypeScript-go/pull/3390) (Closed)

**Coerce factory modifiers argument to NodeArray**

*Automatically coerce the modifiers argument for factory functions into a NodeArray*

 * created by **virtulis**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#3394](https://github.com/microsoft/TypeScript-go/pull/3394) (Open)

**Limit all OS FS calls with semaphores**

*Use semaphores to limit concurrent OS file system calls as an alternative to #3369 and to resolve issue #3139.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3394#issuecomment-4238183278) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3394#issuecomment-4238183692) **typescript-bot** reported starting CI jobs and provided links to status and results
 * [today](https://github.com/microsoft/TypeScript-go/pull/3394#issuecomment-4238322677) **typescript-bot** provided the requested perf run results

### [PR microsoft/TypeScript-go#3395](https://github.com/microsoft/TypeScript-go/pull/3395) (Open)

**Fix watching files outside the workspace and realpaths symlinked into programs**

*Use relative path patterns for file watching and reverse-map realpaths to symlink locations to support npm-linked dependencies outside the workspace.*

 * created by **andrewbranch**

### [PR microsoft/TypeScript-go#3396](https://github.com/microsoft/TypeScript-go/pull/3396) (Open)

**Use methods for client cap resolution**

*Replace top-level functions with methods for client cap resolution to simplify implementation and shorten names.*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#3397](https://github.com/microsoft/TypeScript-go/pull/3397) (Open)

**Use GHA runners instead of custom runners**

*Benchmarking shows GitHub-hosted runners run jobs roughly twice as slow as custom runners, questioning their necessity.*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#3398](https://github.com/microsoft/TypeScript-go/pull/3398) (Open)

**Update dependencies**

*Update project dependencies to resolve npm audit vulnerabilities and clean up related package issues.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3398#issuecomment-4241355402) **jakebailey** said "Failing due to https://github.com/microsoft/vscode-extension-telemetry/issues/244"

### [Issue microsoft/TypeScript-go#3399](https://github.com/microsoft/TypeScript-go/issues/3399) (Open, `duplicate`)

**instance of narrowing loses property type for a class returned from a generic factory**

*TypeScript fails to narrow a generic factory-produced class’s property type after an instanceof check, allowing invalid assignments.*

 * created by **kljnepk**
 * [later](https://github.com/microsoft/TypeScript-go/issues/3399#issuecomment-4244743808) **ahejlsberg** identified the issue as a duplicate of issue #17253, explained that runtime type information is absent so the compiler substitutes any for generic parameters, and agreed that substituting unknown would be safer though unsound for contravariant positions
 * **ahejlsberg** added label `duplicate`

