# Report for 2026-07-31 (Friday, July 31st, 2026)

14 different users commented on 28 different issues.

## Recommended Actions

 * Response Recommended
    * @robertkirkman asked where the Android binary in the downloaded artifact is in [microsoft/TypeScript-go#4734](https://github.com/microsoft/TypeScript-go/pull/4734#issuecomment-5147008980)
    * @robertkirkman reported the cause of and workaround for the path detection error on Google Play Termux in [microsoft/TypeScript-go#4734](https://github.com/microsoft/TypeScript-go/pull/4734#issuecomment-5151566500)
    * @skidlucas clarified that the code was hand-written TypeORM entities, not generated code in [microsoft/TypeScript-go#4807](https://github.com/microsoft/TypeScript-go/issues/4807#issuecomment-5146409765)
    * @typescript-automation[bot] provided performance results as requested in [microsoft/TypeScript-go#4813](https://github.com/microsoft/TypeScript-go/pull/4813#issuecomment-5149982230)
    * @typescript-automation[bot] reported a panic handling textDocument/diagnostic request in [microsoft/TypeScript-go#4814](https://github.com/microsoft/TypeScript-go/issues/4814#issuecomment-5148472812)
    * @typescript-automation[bot] reported a panic with unhandled node kind in JSX initializer in [microsoft/TypeScript-go#4814](https://github.com/microsoft/TypeScript-go/issues/4814#issuecomment-5148472877)
    * @typescript-automation[bot] reported a panic debug failure in [microsoft/TypeScript-go#4814](https://github.com/microsoft/TypeScript-go/issues/4814#issuecomment-5148472909)
    * @typescript-automation[bot] reported a panic error in automated checks in [microsoft/TypeScript-go#4814](https://github.com/microsoft/TypeScript-go/issues/4814#issuecomment-5148472988)
    * @typescript-automation[bot] reported a panic in textDocument/diagnostic handling in [microsoft/TypeScript-go#4814](https://github.com/microsoft/TypeScript-go/issues/4814#issuecomment-5148473024)
    * @typescript-automation[bot] reported a server connection closed prematurely error with reproduction steps in [microsoft/TypeScript-go#4814](https://github.com/microsoft/TypeScript-go/issues/4814#issuecomment-5148473059)
    * @typescript-automation[bot] provided repro steps and error details in [microsoft/TypeScript-go#4814](https://github.com/microsoft/TypeScript-go/issues/4814#issuecomment-5148473085)
    * @typescript-automation[bot] provided repro steps as requested in [microsoft/TypeScript-go#4814](https://github.com/microsoft/TypeScript-go/issues/4814#issuecomment-5148473126)
    * @typescript-automation[bot] reported a server connection closed prematurely error in [microsoft/TypeScript-go#4814](https://github.com/microsoft/TypeScript-go/issues/4814#issuecomment-5148473164)
    * @typescript-automation reported a server connection error and provided repro steps in [microsoft/TypeScript-go#4814](https://github.com/microsoft/TypeScript-go/issues/4814#issuecomment-5148473206)
    * @typescript-automation[bot] reported server connection closed prematurely for remotion-dev/remotion in [microsoft/TypeScript-go#4814](https://github.com/microsoft/TypeScript-go/issues/4814#issuecomment-5148473241)
    * @typescript-automation[bot] provided repro steps as requested in [microsoft/TypeScript-go#4814](https://github.com/microsoft/TypeScript-go/issues/4814#issuecomment-5148473276)
    * @typescript-automation[bot] reported panic handling request textDocument/diagnostic in [microsoft/TypeScript-go#4814](https://github.com/microsoft/TypeScript-go/issues/4814#issuecomment-5148473308)
    * @typescript-automation[bot] reported a panic during textDocument/diagnostic handling in [microsoft/TypeScript-go#4814](https://github.com/microsoft/TypeScript-go/issues/4814#issuecomment-5148473376)
    * @typescript-automation[bot] reported a panic in textDocument/diagnostic that needs investigation in [microsoft/TypeScript-go#4814](https://github.com/microsoft/TypeScript-go/issues/4814#issuecomment-5148473447)
    * @typescript-automation[bot] reported a panic in textDocument/diagnostic handling in [microsoft/TypeScript-go#4814](https://github.com/microsoft/TypeScript-go/issues/4814#issuecomment-5148473477)
    * @typescript-automation[bot] reported a panic in JSX transformer in [microsoft/TypeScript-go#4814](https://github.com/microsoft/TypeScript-go/issues/4814#issuecomment-5148473518)

## Activity Summary

### [PR microsoft/TypeScript-go#4313](https://github.com/microsoft/TypeScript-go/pull/4313) (Open)

**Assign checkers with cost/import\-aware algorithm**

*Develop a cost- and import-aware algorithm to assign diagnostic checkers more efficiently.*

 * [1 month ago](https://github.com/microsoft/TypeScript-go/pull/4313#issuecomment-4848474935) **typescript-automation[bot]** reported the start of performance test jobs and provided status and results links
 * [1 month ago](https://github.com/microsoft/TypeScript-go/pull/4313#issuecomment-4848601089) **typescript-automation[bot]** reported the performance run results including comparisons for errors, symbols, types, and memory usage
 * [1 month ago](https://github.com/microsoft/TypeScript-go/pull/4313#issuecomment-4848626121) **jakebailey** said "Uh oh, xstate has some checker association dependence."
 * [today](https://github.com/microsoft/TypeScript-go/pull/4313#issuecomment-5146994914) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4313#issuecomment-5146995482) **typescript-automation[bot]** started build jobs and posted a status table with links to results
 * [today](https://github.com/microsoft/TypeScript-go/pull/4313#issuecomment-5147092329) **jakebailey** presented preliminary performance results showing reductions in check time, total time, symbols, types, instantiations, memory used, and allocations for VS Code and Strada compiler runs
 * [today](https://github.com/microsoft/TypeScript-go/pull/4313#issuecomment-5147214752) **typescript-automation[bot]** reported the requested performance run results
 * [today](https://github.com/microsoft/TypeScript-go/pull/4313#issuecomment-5148138322) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4313#issuecomment-5148138619) **typescript-automation[bot]** announced performance test jobs started with links to the build and results
 * [today](https://github.com/microsoft/TypeScript-go/pull/4313#issuecomment-5148273133) **typescript-automation[bot]** posted performance run results for the requested tsc comparison
 * [today](https://github.com/microsoft/TypeScript-go/pull/4313#issuecomment-5149687534) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4313#issuecomment-5149687767) **typescript-automation[bot]** reported that perf test started and provided build and results links
 * [today](https://github.com/microsoft/TypeScript-go/pull/4313#issuecomment-5149784101) **typescript-automation[bot]** reported the performance run results in a comparison report

### [PR microsoft/TypeScript-go#4365](https://github.com/microsoft/TypeScript-go/pull/4365) (Open, **jakebailey**, **Copilot**)

**Preserve typedef comments in declaration emit**

*Preserve descriptive JSDoc comments on typedefs and callbacks in emitted declaration files while preventing duplicate comment output*

 * (6 weeks ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/4365#issuecomment-5111400237) **dkamins** confirmed the PR output matched expectations and provided a summary table of JSDoc typedef behaviors with a repro archive
 * [today](https://github.com/microsoft/TypeScript-go/pull/4365#issuecomment-5146369402) **jakebailey** said "@copilot+gpt-5.6-sol Merge main and fix baselines. Also consider the above"

### [Issue microsoft/TypeScript-go#4528](https://github.com/microsoft/TypeScript-go/issues/4528) (Closed, `Domain: Type Checking`, `Type Ordering`)

**tsgo appears to loop until OOM on three/tsl Fn callback that TypeScript accepts**

*tsgo enters an infinite type-checking loop and exhausts memory when processing a three/tsl Fn callback that tsc accepts*

 * **ahejlsberg** added label `Type Ordering`
 * [1 month ago](https://github.com/microsoft/TypeScript-go/issues/4528#issuecomment-4879046574) **ahejlsberg** suggested refactoring Node<TNodeType> into a NodeExtras mapping with specific extensions per type
 * (2 weeks ago) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/issues/4528#issuecomment-5145766352) **mrcljx** said "@ahejlsberg thank you for the suggestion. Got it merged and released in @types/three@0.185.2.  "

### [Issue microsoft/TypeScript-go#4581](https://github.com/microsoft/TypeScript-go/issues/4581) (Closed, `bug`, **RyanCavanaugh**, **Copilot**)

**TS2719/TS2322 false positive on a generic type forwarded through an interface \`extends\` boundary \(tsc clean, tsgo fails\)**

*tsgo wrongly reports a TS2719/TS2322 type mismatch when extending and forwarding a library’s generic props interface despite tsc accepting it*

 * (4 days ago) **RyanCavanaugh** assigned to **Copilot**, **RyanCavanaugh**, and unassigned **Copilot**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4581#issuecomment-5145434843) **RyanCavanaugh** provided a minimal repro showing a TS2719 type assignment error difference between TS6 and TS7
 * [today](https://github.com/microsoft/TypeScript-go/issues/4581#issuecomment-5147004059) **RyanCavanaugh** provided a minimal reproduction snippet illustrating a TS2719 type error in tsgo and outlined the code conditions required to trigger it
 * (today) **RyanCavanaugh** assigned to **Copilot**, **Copilot**, and unassigned **Copilot**, **Copilot**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4581#issuecomment-5147938548) **RyanCavanaugh** said "The agents were having a hard time fixing this bug because it's already been fixed in nightly 🫠"
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#4661](https://github.com/microsoft/TypeScript-go/pull/4661) (Open)

**Fall back to inotify when filesystem has errors in fanotify \(fix watch in Docker\)**

*Automatically switch to inotify backend when fanotify fails on Docker filesystems to detect file changes.*

 * created by **johnfav03**
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/4661#issuecomment-5107156400) **jakebailey** said "I think this approach is probably okay, though I do wonder if the fanotify watch backend should just internally fall back to inotify..."
 * [today](https://github.com/microsoft/TypeScript-go/pull/4661#issuecomment-5145562548) **johnfav03** embedded the inotify fallback into the fanotify backend and asked if it matched the suggestion

### [PR microsoft/TypeScript-go#4734](https://github.com/microsoft/TypeScript-go/pull/4734) (Open)

**Add Android ARM64 release target**

*Add Android ARM64 release target to the build configuration*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4734#issuecomment-5075800807) **robertkirkman** said "Is there a way I can download the GitHub Actions CI artifact from this PR?"
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4734#issuecomment-5075829438) **jakebailey** said "No, but I could temporarily enable that (it'd be too big overall to have on always)"
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4734#issuecomment-5075861964) **robertkirkman** said "If it's not too much trouble I would like to test it, but if it would take too long then don't worry about it."
 * [today](https://github.com/microsoft/TypeScript-go/pull/4734#issuecomment-5146419360) **jakebailey** said "Temporarily made this upload artifacts; will undo when you've checked."
 * [today](https://github.com/microsoft/TypeScript-go/pull/4734#issuecomment-5147008980) **robertkirkman** asked where the Android binary in the downloaded artifact was and provided extra information about .vsix compatibility with Android VSCode ports
 * [today](https://github.com/microsoft/TypeScript-go/pull/4734#issuecomment-5147074433) **jakebailey** stated that they would only publish vsce-supported VSIXes and said they would add Android to CI
 * [later](https://github.com/microsoft/TypeScript-go/pull/4734#issuecomment-5151566500) **robertkirkman** explained that typescript-go’s os.Executable fails on Google Play Termux due to Android’s targetSdkVersion restrictions and suggested using the TERMUX_EXEC__PROC_SELF_EXE environment variable
 * [later](https://github.com/microsoft/TypeScript-go/pull/4734#issuecomment-5151664489) **robertkirkman** provided context that the error is specific to Google Play Termux and noted the binary has the correct interpreter and passes the static linking check

### [PR microsoft/TypeScript-go#4777](https://github.com/microsoft/TypeScript-go/pull/4777) (Closed, `dependencies`, `javascript`)

**Bump brace\-expansion from 5\.0\.6 to 5\.0\.8**

*Upgrade brace-expansion dependency from version 5.0.6 to 5.0.8.*

 * (3 days ago) **dependabot[bot]** added labels `javascript`, `dependencies`, `javascript`
 * [later](https://github.com/microsoft/TypeScript-go/pull/4777#issuecomment-5150765709) **dependabot[bot]** said "Superseded by #4816."
 * (later) **dependabot[bot]** closed the issue

### [Issue microsoft/TypeScript-go#4795](https://github.com/microsoft/TypeScript-go/issues/4795) (Open, `Needs More Info`)

**\`tsc \-\-watch\` doesn't recompile on file change**

*TypeScript 7.0.2 stops tsc --build --watch from detecting file changes in a monorepo*

 * created by **haines**
 * (today) **RyanCavanaugh** added label `Needs More Info`, and set milestone to `Need More Info`

### [PR microsoft/TypeScript-go#4798](https://github.com/microsoft/TypeScript-go/pull/4798) (Closed)

**Avoid temporary composite mapper allocations**

*Avoiding temporary composite mapper allocations reduced runtime by 2.7%, peak RSS by 5.5%, and memory allocations by 21%.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4798#issuecomment-5135950642) **jakebailey** said "@typescript-bot perf test this faster"
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4798#issuecomment-5135951442) **typescript-automation[bot]** announced that performance test jobs had started and provided status and results links
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4798#issuecomment-5136183114) **typescript-automation[bot]** reported the results of the requested performance run
 * [today](https://github.com/microsoft/TypeScript-go/pull/4798#issuecomment-5144887108) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4798#issuecomment-5144888502) **typescript-automation[bot]** posted build status update with job command, status, and results links
 * [today](https://github.com/microsoft/TypeScript-go/pull/4798#issuecomment-5145156373) **typescript-automation[bot]** posted the requested performance run results
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4801](https://github.com/microsoft/TypeScript-go/issues/4801) (Open, `Needs Investigation`, **johnfav03**)

**\[ServerErrors\]\[TypeScript\] main vs **

*The Azure pipeline run on TypeScript’s main branch across 300 GitHub repos reported 34 changes, 102 timeouts and various failures.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/4801#issuecomment-5137229469) **typescript-automation[bot]** reported a panic during handling textDocument/diagnostic and listed affected repos and artifacts
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/4801#issuecomment-5137229548) **typescript-automation[bot]** reported a panic during textDocument/diagnostic with stack trace for honojs/hono
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/4801#issuecomment-5137229621) **typescript-automation[bot]** reported a panic during textDocument/diagnostic with stack trace and repro commands for date-fns/date-fns
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.1`, and assigned to **johnfav03**

### [Issue microsoft/TypeScript-go#4802](https://github.com/microsoft/TypeScript-go/issues/4802) (Open)

**workspace/symbol returns results from projects outside the workspace folder**

*The TypeScript language server’s workspace/symbol command erroneously returns symbols from external project folders, leading to duplicates, slow queries, and high memory usage.*

 * created by **stewartmcgown**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4802#issuecomment-5145002995) **jakebailey** said "We were missing js/ts.workspaceSymbols.scope support; #4805 adds it, at the expense of an LSP extension."
 * **RyanCavanaugh** added to milestone `Possible Improvement`

### [Issue microsoft/TypeScript-go#4804](https://github.com/microsoft/TypeScript-go/issues/4804) (Open, **andrewbranch**)

**\`checker\.getTypeAtLocation\` panics for an array literal contextually typed by an empty tuple**

*checker.getTypeAtLocation panics on array literals typed by empty tuples due to an incorrect type assertion.*

 * created by **artem1458**
 * (today) **RyanCavanaugh** set milestone to `TypeScript 7.1`, and assigned to **andrewbranch**

### [PR microsoft/TypeScript-go#4805](https://github.com/microsoft/TypeScript-go/pull/4805) (Open)

**Support js/ts\.workspaceSymbols\.scope and extra textDocument param on workspace/symbol request**

*Add js/ts.workspaceSymbols.scope support and an extra textDocument parameter to filter workspace symbol requests to a document’s projects.*

 * created by **jakebailey**

### [Issue microsoft/TypeScript-go#4806](https://github.com/microsoft/TypeScript-go/issues/4806) (Open, `Crash`, `Needs Investigation`, **johnfav03**)

**LSP watcher panics when Close races with WatchFiles**

*TypeScript LSP file watcher's concurrent Close and WatchFiles calls race, triggering a panic from nil map assignment.*

 * created by **jinyongp**
 * **jinyongp** added label `Crash`
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.1`, and assigned to **johnfav03**

### [Issue microsoft/TypeScript-go#4807](https://github.com/microsoft/TypeScript-go/issues/4807) (Open, `Needs Investigation`, **ahejlsberg**)

**False “Excessive stack depth” on circular types linked through arrays \(regression from \#3445\)**

*tsgo 7.0.2 erroneously reports excessive stack depth comparing circular interfaces connected via optional arrays, a regression from TypeScript 6.0*

 * created by **skidlucas**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4807#issuecomment-5146109590) **ahejlsberg** asked if the issue surfaces in real-world scenarios and then noted it originated from ORM-generated code
 * [today](https://github.com/microsoft/TypeScript-go/issues/4807#issuecomment-5146409765) **skidlucas** clarified that the code was hand-written TypeORM entities implementing interfaces, not generated by ORM
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `Post-7.0`, and assigned to **ahejlsberg**

### [PR microsoft/TypeScript-go#4808](https://github.com/microsoft/TypeScript-go/pull/4808) (Open)

**Add a parentWatchdogEnabled CLI flag**

*Add a parentWatchdogEnabled CLI flag to allow disabling the watchdog via command line.*

 * created by **mj026**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4808#issuecomment-5145994813) **jakebailey** said "Why? Parent watching is in the spec. Can you explain your needs?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4808#issuecomment-5146003158) **jakebailey** said "Ah, PR first, issue second..."
 * [today](https://github.com/microsoft/TypeScript-go/pull/4808#issuecomment-5146011598) **mj026** praised the quick reply and referenced a previously described issue (#4809) about inaccurate parent process detection

### [Issue microsoft/TypeScript-go#4809](https://github.com/microsoft/TypeScript-go/issues/4809) (Open, `Crash`, **jakebailey**, **Copilot**)

**LSP exits when parent process PID is not found**

*LSP’s parent-PID watchdog terminates the server when the PID can’t be found in Docker, with a CLI flag to disable it.*

 * created by **mj026**
 * **mj026** added label `Crash`
 * [today](https://github.com/microsoft/TypeScript-go/issues/4809#issuecomment-5146006730) **jakebailey** said "If you don't want the parent watching, why send the PID at all?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/4809#issuecomment-5146253643) **mj026** explained that not all LSP implementations allow manual flag or config changes, cited SublimeLSP as an example, and noted they were unaware of the LSP spec’s parent process watchdog and that this was the first server they’d seen to implement it
 * [today](https://github.com/microsoft/TypeScript-go/issues/4809#issuecomment-5146278789) **jakebailey** noted that spec violations were annoying and possibly not worth the complexity, mentioned the original motivation was to prevent orphaned processes, and expressed hope that stdin closing would still occur
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**
 * **RyanCavanaugh** added to milestone `Post-7.0`

### [PR microsoft/TypeScript-go#4810](https://github.com/microsoft/TypeScript-go/pull/4810) (Closed, **RyanCavanaugh**, **Copilot**)

**Add minimal regression for TS2719 false\-positive across \`interface extends\` \+ spread generic forwarding**

*A new test demonstrates a tsgo-only TS2719 false-positive when extending and spreading a generic interface into a generic function call.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#4811](https://github.com/microsoft/TypeScript-go/pull/4811) (Open, **jakebailey**, **Copilot**)

**Remove the LSP parent process watchdog**

*Remove LSP parent process monitoring and watchdog to prevent erroneous exits across containers, relying instead on stdio and signal lifecycle.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#4812](https://github.com/microsoft/TypeScript-go/pull/4812) (Closed, **RyanCavanaugh**, **Copilot**)

**\[WIP\] Fix false positive on generic type forwarded through interface**

*Fix compiler false positives when forwarding generic types through interfaces, including regression tests and code validation.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#4813](https://github.com/microsoft/TypeScript-go/pull/4813) (Closed)

**Avoid false symlink mappings for physical dependencies**

*Declaration emit incorrectly reused unrelated JSDoc imports after physical dependencies were falsely mapped as symlinks, now fixed.*

 * created by **platypii**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4813#issuecomment-5148134473) **platypii** said "@microsoft-github-policy-service agree company="Hyperparam""
 * [today](https://github.com/microsoft/TypeScript-go/pull/4813#issuecomment-5149894818) **jakebailey** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4813#issuecomment-5149895116) **typescript-automation[bot]** posted CI job status updates with links to build results
 * [today](https://github.com/microsoft/TypeScript-go/pull/4813#issuecomment-5149982230) **typescript-automation[bot]** reported the requested performance run results including tsc comparison metrics
 * [today](https://github.com/microsoft/TypeScript-go/pull/4813#issuecomment-5150134780) **typescript-automation[bot]** reported that running tsc on the top 400 repos showed no differences between main and the PR merge

### [Issue microsoft/TypeScript-go#4814](https://github.com/microsoft/TypeScript-go/issues/4814) (Open, `bug`, **johnfav03**)

**\[ServerErrors\]\[TypeScript\] main vs **

*TypeScript’s main branch CI pipeline encountered server errors and timeouts analyzing 300 popular GitHub repositories, processing only 190.*

 * created by **typescript-automation[bot]**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4814#issuecomment-5148472771) **typescript-automation[bot]** reported a panic during a textDocument/diagnostic request, including a stack trace and affected repository information
 * [today](https://github.com/microsoft/TypeScript-go/issues/4814#issuecomment-5148472812) **typescript-automation[bot]** reported a panic in textDocument/diagnostic handling with stack trace and affected repo TanStack/query
 * [today](https://github.com/microsoft/TypeScript-go/issues/4814#issuecomment-5148472850) **typescript-automation[bot]** logged panic handling for textDocument/diagnostic and provided stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/4814#issuecomment-5148472877) **typescript-automation[bot]** reported a panic due to an unhandled node kind in a JSX initializer
 * [today](https://github.com/microsoft/TypeScript-go/issues/4814#issuecomment-5148472909) **typescript-automation[bot]** reported a panic due to a failed debug assertion and included the stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/4814#issuecomment-5148472949) **typescript-automation[bot]** reported a panic during textDocument/diagnostic handling with a stack trace and listed affected repos and logs
 * [today](https://github.com/microsoft/TypeScript-go/issues/4814#issuecomment-5148472988) **typescript-automation[bot]** reported a runtime panic stack trace indicating an index out of range error
 * [today](https://github.com/microsoft/TypeScript-go/issues/4814#issuecomment-5148473024) **typescript-automation[bot]** reported a panic handling a textDocument/diagnostic request with a stack trace and identified the affected repo
 * [today](https://github.com/microsoft/TypeScript-go/issues/4814#issuecomment-5148473059) **typescript-automation[bot]** reported a server connection closed prematurely error with logs, recent requests, and reproduction steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/4814#issuecomment-5148473085) **typescript-automation[bot]** reported that the server connection closed prematurely for QwenLM/qwen-code and provided error details, last requests, and repro steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/4814#issuecomment-5148473126) **typescript-automation[bot]** reported a server connection closed prematurely and provided repro steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/4814#issuecomment-5148473164) **typescript-automation[bot]** reported a server connection closed prematurely error and included affected repository, raw error text, recent requests, and repro steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/4814#issuecomment-5148473206) **typescript-automation[bot]** reported a server connection closed prematurely error for KeygraphHQ/shannon and provided error details, affected repos, recent requests, and reproduction steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/4814#issuecomment-5148473241) **typescript-automation[bot]** reported a premature server connection closure (undefined) and supplied affected repo, error logs, recent requests, and reproduction steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/4814#issuecomment-5148473276) **typescript-automation[bot]** reported a premature server connection closure for microsoft/vscode and provided error artifacts and repro steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/4814#issuecomment-5148473308) **typescript-automation[bot]** reported a panic while handling a textDocument/diagnostic request with stack trace and affected repo details
 * [today](https://github.com/microsoft/TypeScript-go/issues/4814#issuecomment-5148473334) **typescript-automation[bot]** reported a panic handling textDocument/diagnostic with a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/4814#issuecomment-5148473376) **typescript-automation[bot]** reported a panic during textDocument/diagnostic handling with stack trace and affected repository
 * [today](https://github.com/microsoft/TypeScript-go/issues/4814#issuecomment-5148473407) **typescript-automation[bot]** reported a panic while handling textDocument/diagnostic with stack trace and affected repository details
 * [today](https://github.com/microsoft/TypeScript-go/issues/4814#issuecomment-5148473447) **typescript-automation[bot]** reported a panic while handling textDocument/diagnostic with stack trace and affected repository details
 * [today](https://github.com/microsoft/TypeScript-go/issues/4814#issuecomment-5148473477) **typescript-automation[bot]** reported a panic handling textDocument/diagnostic request and provided a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/4814#issuecomment-5148473518) **typescript-automation[bot]** reported a panic due to an unhandled KindBinaryExpression node kind in a JSX initializer

### [Issue microsoft/TypeScript-go#4815](https://github.com/microsoft/TypeScript-go/issues/4815) (Open, `Domain: API and Extensibility`, **andrewbranch**)

**\[API\] Expose globals declared by a source file**

*Expose SourceFile.Locals in the TypeScript JS API to more reliably retrieve global symbols declared in a source file.*

 * created by **Gerrit0**

### [PR microsoft/TypeScript-go#4816](https://github.com/microsoft/TypeScript-go/pull/4816) (Open, `dependencies`, `javascript`)

**Bump brace\-expansion from 5\.0\.6 to 5\.0\.9**

*Update brace-expansion dependency from version 5.0.6 to 5.0.9.*

 * created by **dependabot[bot]**
 * (later) **dependabot[bot]** added labels `dependencies`, `javascript`, `dependencies`, `javascript`

