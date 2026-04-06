# Report for 2026-03-31 (Tuesday, March 31st, 2026)

10 different users commented on 51 different issues.

## Recommended Actions

 * Response Recommended
    * @vetptzru provided root cause analysis and suggested a solution in [microsoft/TypeScript-go#3139](https://github.com/microsoft/TypeScript-go/issues/3139#issuecomment-4170466384)
    * @virtulis asked about the significance of namespace blocks becoming modules after a roundtrip in [microsoft/TypeScript-go#3195](https://github.com/microsoft/TypeScript-go/pull/3195#issuecomment-4163900331)
    * @virtulis requested preview versions of the NPM packages in [microsoft/TypeScript-go#3195](https://github.com/microsoft/TypeScript-go/pull/3195#issuecomment-4168388915)

## Activity Summary

### [Issue microsoft/TypeScript-go#1057](https://github.com/microsoft/TypeScript-go/issues/1057) (Open, `Domain: Type Checking`, `Type Ordering`, **ahejlsberg**, **Copilot**)

**Inconsistency involving discriminated union and flatMap**

*flatMap callback returning either InputOp[] or remove-only arrays causes a TypeScript discriminated union inference error*

 * **ahejlsberg** added label `Type Ordering`
 * (yesterday) **RyanCavanaugh** assigned to **Copilot**, **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript-go/issues/1057#issuecomment-4164924448) **jakebailey** said "The above suggestion causes just one break: https://github.com/microsoft/TypeScript/pull/63328#issuecomment-4164789350"
 * (today) **RyanCavanaugh** assigned to **ahejlsberg**, and unassigned **RyanCavanaugh**

### [Issue microsoft/TypeScript-go#1100](https://github.com/microsoft/TypeScript-go/issues/1100) (Closed, `Domain: Type Checking`, `Type Ordering`)

**tsgo regression: TS2590: Expression produces a union type that is too complex to represent\.**

*A recent tsgo regression causes TS2590 errors in StackBlitz when encountering an overly complex union type representation.*

 * [41 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1100#issuecomment-2981837391) **ahejlsberg** described how inferring type arguments for Object.entries(rules) triggered subtype reduction on a large union type and caused an N^2 explosion in checks that exceeded the 1M operation threshold
 * **ahejlsberg** added label `Type Ordering`
 * [23 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1100#issuecomment-3429598496) **chkimes** requested instructions to generate estimate values for comparing tsc and tsgo in their codebase
 * [today](https://github.com/microsoft/TypeScript-go/issues/1100#issuecomment-4166336153) **RyanCavanaugh** said "You'd have to set a breakpoint at look at the relevant calculation; this value is not observable from the outside."
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#1507](https://github.com/microsoft/TypeScript-go/issues/1507) (Closed, `Needs More Info`, `Domain: Performance`)

**TypeScript\-Go Performance Issue in ci \(github action\)**

*TypeScript-Go’s GitHub Actions CI build runs only 28% faster (57s vs 79s) than tsc instead of the expected 10× speedup*

 * [16 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1507#issuecomment-3621277862) **aem** noted that source map-related functions consumed significant CPU time despite being disabled and provided profiling data
 * [16 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1507#issuecomment-3621363638) **jakebailey** said "Everyone is posting different problems in this thread. If you are having perf issues, I would suggest opening a new issue and also uploading the profiles created by --pprofDir."
 * [16 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1507#issuecomment-3621450307) **aem** offered to open a new issue and explained the CI vs local resource constraint differences
 * [today](https://github.com/microsoft/TypeScript-go/issues/1507#issuecomment-4166363737) **RyanCavanaugh** suggested opening an issue with a repro or pprof profile if problems persist
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#1530](https://github.com/microsoft/TypeScript-go/issues/1530) (Open, `Domain: Type Checking`, `Domain: JSX`, **weswigham**, **RyanCavanaugh**, **Copilot**)

**jsx Prop on \<style\> Tag Not Recognized**

*typescript-go does not recognize the styled-jsx jsx prop on <style> tags despite React interface augmentation*

 * created by **iolathief108**
 * (33 weeks ago) **jakebailey** added labels `Domain: Type Checking`, `Domain: JSX`
 * (today) **RyanCavanaugh** assigned to **weswigham**, **Copilot**, **RyanCavanaugh**

### [Issue microsoft/TypeScript-go#1724](https://github.com/microsoft/TypeScript-go/issues/1724) (Open, `Domain: Editor`, **DanielRosenwasser**, **iisaduan**, **Copilot**)

**"Sort Imports" & "Remove Unused Imports" commands are missing**

*When using tsgo with TypeScript 5.8, the Sort Imports and Remove Unused Imports commands are missing from the VSCode command palette.*

 * **jakebailey** added label `Domain: Editor`
 * (5 days ago) **DanielRosenwasser** set milestone to `TypeScript 7.0 RC`, and assigned to **iisaduan**
 * [today](https://github.com/microsoft/TypeScript-go/issues/1724#issuecomment-4166252274) **DanielRosenwasser** said "I think at this point the only thing that needs to be done is add individual commands for the extension. The tests all seem ported."
 * (today) **DanielRosenwasser** assigned to **Copilot**, **DanielRosenwasser**

### [Issue microsoft/TypeScript-go#1789](https://github.com/microsoft/TypeScript-go/issues/1789) (Open, `Domain: Type Checking`, `Type Ordering`, **ahejlsberg**)

**Inference fails form unions of arrays of different depths \(T\[\] \| T\[\]\[\]\)**

*A generic flat function fails to infer type T for T[]|T[][] arguments under tsgo, though TypeScript 5.8 succeeds.*

 * **ahejlsberg** added label `Type Ordering`
 * [25 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1789#issuecomment-3378611677) **jakebailey** said "This function is something defined in lib.d.ts. It seems unfortunate that we'd have to define this special type to work around this inference case."
 * [25 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1789#issuecomment-3378695181) **jakebailey** corrected his previous statement and showed the TypeScript lib.d.ts implementation of flat without a union
 * **RyanCavanaugh** assigned to **ahejlsberg**

### [Issue microsoft/TypeScript-go#1874](https://github.com/microsoft/TypeScript-go/issues/1874) (Closed, `Domain: Editor`, **johnfav03**)

**\[LSP\] Remove Unused Imports**

*Re-implement the language server’s functionality for automatically removing unused imports.*

 * created by **marioparaschiv**
 * **jakebailey** added label `Domain: Editor`
 * **RyanCavanaugh** assigned to **johnfav03**

### [Issue microsoft/TypeScript-go#1885](https://github.com/microsoft/TypeScript-go/issues/1885) (Closed, `Crash`, **jakebailey**)

**go to definition panic \(windows, wsl\)**

*go to definition on Windows or WSL triggers a nil pointer panic in typescript-go’s snapshot clone*

 * [20 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1885#issuecomment-3493150114) **RyanCavanaugh** said "We could realize use a concrete repro for this. Do you have steps that reliably cause it?"
 * [18 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1885#issuecomment-3567730224) **43081j** reported inability to reproduce the issue manually since the server crashed constantly on WSL with Neovim and provided crash logs
 * **RyanCavanaugh** assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/issues/1885#issuecomment-4167459395) **jakebailey** said "It's been a few months; I'm pretty sure all code related to this has been rewritten and I do not think it should be happening anymore."
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#1946](https://github.com/microsoft/TypeScript-go/issues/1946) (Open, `Domain: Editor`, **mjbvz**)

**Support workspace specific typescript version**

*Allow the extension to use a workspace-specific TypeScript version rather than a global one.*

 * [16 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1946#issuecomment-3605893813) **thien-do** corrected that it should be the directory rather than the file
 * [16 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1946#issuecomment-3607681749) **jakebailey** said "You shouldn't have to put the platform specific things in there; unless there's a bug, it should work to point it to node_modules/@typescript/native-preview itself..."
 * [14 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1946#issuecomment-3677550797) **VdustR** said "node_modules/@typescript/native-preview works great for me."
 * (today) **RyanCavanaugh** added label `Domain: Editor`, removed label `Domain: Editor`, and assigned to **mjbvz**

### [PR microsoft/TypeScript-go#1990](https://github.com/microsoft/TypeScript-go/pull/1990) (Open)

**Implement semantic tokens**

*Implement semantic tokens in the VS Code extension while coordinating multiple checker functionalities for doc highlights, diagnostics, and inlay hints.*

 * [21 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1990#issuecomment-3471333902) **DanielRosenwasser** asked if the same behavior applied to document highlights and semantic tokens and whether it felt reasonable in a larger codebase
 * [21 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1990#issuecomment-3471339983) **DanielRosenwasser** said "Ah, but we didn't make more checkers."
 * [19 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1990#issuecomment-3543481582) **jakebailey** said "Drafting this for now, until we can improve the checker situation IMO"
 * [today](https://github.com/microsoft/TypeScript-go/pull/1990#issuecomment-4166299067) **DanielRosenwasser** said "If you can add fuzzing support at https://github.com/microsoft/typescript-error-deltas that would be swell. I guess you'd have to wait for the next publish though?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/1990#issuecomment-4166430646) **jakebailey** said "I'll look into the fuzzing, though this is sort of an irritating call due to the full/range/delta split"

### [Issue microsoft/TypeScript-go#2147](https://github.com/microsoft/TypeScript-go/issues/2147) (Open, `Domain: Module Resolution`, `Domain: Program`, **RyanCavanaugh**, **Copilot**)

**VSCode extension does not appear to work with typeRoots**

*The TSGo extension ignores typeRoots configuration in a monorepo-like layout, preventing proper type resolution.*

 * (18 weeks ago) **jakebailey** added labels `Domain: Module Resolution`, `Domain: Program`, and removed label `Domain: Editor`
 * (today) **RyanCavanaugh** assigned to **Copilot**, **RyanCavanaugh**

### [PR microsoft/TypeScript-go#2322](https://github.com/microsoft/TypeScript-go/pull/2322) (Closed)

**Remove GetOptionsDiagnostics, expose global diags in LSP**

*Remove the redundant GetOptionsDiagnostics API, expose separate config file parsing and real-time global diagnostics in the LSP.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2322#issuecomment-4057866971) **jakebailey** said "Ah. I think we still can report global diagnostics on things like "Iterable is missing", which only happens when you finally ask for it somewhere. Would need to recheck."
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2322#issuecomment-4057914264) **andrewbranch** suggested having a diagnostics bucket for checker initialization, noted that the change was fine as-is, clarified the scope of global diagnostics in the LSP, and offered approval once undrafted
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2322#issuecomment-4158591198) **jakebailey** said "Probably should just take #3285"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2461](https://github.com/microsoft/TypeScript-go/pull/2461) (Closed, **RyanCavanaugh**, **Copilot**)

**Port TypeScript PR \#62950: Ignore computed name parents when looking up containing functions**

*Port PR #62950 to skip computed name nodes when finding containing functions, preventing recursion and fixing yield/await errors in Go.*

 * **Copilot** assigned to **RyanCavanaugh**
 * [10 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2461#issuecomment-3757055052) **Copilot** explained why getContainingFunctionDeclaration wasn't ported due to having no callers and added two new tests (yieldInComputedNameOfContextuallyTypedObjectNoCrash1.ts, classStaticBlock29.ts) in commit c0af02c6
 * [10 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2461#issuecomment-3757097683) **Copilot** confirmed removal of getContainingClassStaticBlock in commit c0af02c6
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2530](https://github.com/microsoft/TypeScript-go/pull/2530) (Closed)

**Disable Go CI caching**

*Request to disable Go CI caching due to limited storage and questionable performance benefits.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2530#issuecomment-4165753736) **jakebailey** said "From my comparison, the caching is doing nothing for us. I don't think it's worth having all of this stuff around anymore."
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2936](https://github.com/microsoft/TypeScript-go/issues/2936) (Closed, **jakebailey**, **Copilot**)

**\[bug\] JSX parsing fails with spurious syntax errors in ternary expression with nested JSX and multi\-property object literals**

*tsgo 7.0.0-dev misparses nested JSX inside a ternary with object literal props, producing spurious syntax errors.*

 * created by **hou-pu**
 * (1 month ago) **jakebailey** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2937](https://github.com/microsoft/TypeScript-go/pull/2937) (Closed, **jakebailey**, **Copilot**)

**Fix JSX parsing failures in ternary expressions with nested JSX attributes**

*Refactor JSX parser helpers and node list logic to fix nested ternary expression parsing errors and add tests*

 * created by **Copilot**
 * (1 month ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2944](https://github.com/microsoft/TypeScript-go/pull/2944) (Open)

**\[draft\] more formatting tests **

*Add draft formatting tests to validate and troubleshoot the repository’s testing pipelines.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2944#issuecomment-4158717642) **gabritto** said "@typescript-bot test tsserver top10"
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2944#issuecomment-4158717868) **typescript-bot** reported that the test tsserver top10 job failed to queue due to validation errors or warnings
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2944#issuecomment-4158719196) **typescript-bot** said "@iisaduan, the perf run you requested failed. You can check the log here."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2944#issuecomment-4165272941) **typescript-bot** provided the results of the requested perf run, including a detailed comparison report and metrics
 * [today](https://github.com/microsoft/TypeScript-go/pull/2944#issuecomment-4165297450) **typescript-bot** said "@iisaduan, the perf run you requested failed. You can check the log here."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2944#issuecomment-4166370276) **typescript-bot** provided the requested performance run results including a detailed comparison report table
 * [today](https://github.com/microsoft/TypeScript-go/pull/2944#issuecomment-4166390637) **typescript-bot** said "@iisaduan, the perf run you requested failed. You can check the log here."

### [Issue microsoft/TypeScript-go#3139](https://github.com/microsoft/TypeScript-go/issues/3139) (Open, `Needs More Info`)

**runtime: failed to create new OS thread**

*Running tsgo on a large macFUSE-mounted TypeScript project exhausts OS threads and crashes the Go runtime.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/3139#issuecomment-4089083039) **vetptzru** provided screenshots showing the peak thread count the tsgo process reached before crashing
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/3139#issuecomment-4096913604) **vetptzru** said "@DanielRosenwasser do you need any more information from me, or is this enough?"
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/3139#issuecomment-4123683587) **jakebailey** expressed uncertainty about reproducing the issue, suggested runtime tracing might help, and asked why the issue had so many reactions
 * [later](https://github.com/microsoft/TypeScript-go/issues/3139#issuecomment-4170466384) **vetptzru** dug into the codebase and identified that the file parser spawns unbounded goroutines which block on readSema, causing OS thread exhaustion on slow filesystems, and suggested using a pre-spawn semaphore approach
 * [later](https://github.com/microsoft/TypeScript-go/issues/3139#issuecomment-4170683318) **jakebailey** questioned how the cause was determined and challenged the explanation of the Go scheduler

### [PR microsoft/TypeScript-go#3195](https://github.com/microsoft/TypeScript-go/pull/3195) (Open)

**API encode/decode fixes**

*Fixed API encoder/decoder by adding missing node properties, assigning a HeritageClause token type, and extending isTypeNode to recognize type keywords.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3195#issuecomment-4113555719) **virtulis** suggested generating a full list of properties with the generateFactory script and using defineProperty to dynamically define getters on RemoteNode to avoid manual listings and solve the optional vs empty NodeList issue
 * [6 days ago](https://github.com/microsoft/TypeScript-go/pull/3195#issuecomment-4129065241) **virtulis** said "Added the roundtrip test, made it go through everything and print each error since there's multiple different failures present."
 * [5 days ago](https://github.com/microsoft/TypeScript-go/pull/3195#issuecomment-4138050178) **virtulis** described adding output comparisons to roundtrip tests, flooding the console with diffs, fixing a broken TypeOperator, and noting disappearing object spreads
 * [today](https://github.com/microsoft/TypeScript-go/pull/3195#issuecomment-4163900331) **virtulis** fixed most remaining issues and removed input/output comparison, leaving tests to only check for crashes; noted that namespace blocks become modules after a roundtrip and was unsure of its significance given the confusing AST structure
 * [today](https://github.com/microsoft/TypeScript-go/pull/3195#issuecomment-4165876279) **andrewbranch** thanked the team and mentioned beginning the "codegen everything" PR ahead of schedule, planning to include the tests for validation
 * [later](https://github.com/microsoft/TypeScript-go/pull/3195#issuecomment-4168388915) **virtulis** removed code comparing input/output contents after regex cleanup failed, suggested using AST node comparison via a different parser, and requested preview NPM package releases

### [PR microsoft/TypeScript-go#3237](https://github.com/microsoft/TypeScript-go/pull/3237) (Closed)

**Lint when t\.Cleanup closes over t**

*Introduce a lint rule to detect closures capturing t in t.Cleanup and automatically fix the identified case.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3252](https://github.com/microsoft/TypeScript-go/pull/3252) (Open, **DanielRosenwasser**, **Copilot**)

**Fix signature help assertion failure by marking all DeepCloneReparse descendants as reparsed**

*Mark all DeepCloneReparse descendants as reparsed to prevent signature help assertion failures from JSDoc-derived node positions.*

 * created by **Copilot**
 * (5 days ago) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3252#issuecomment-4164496027) **DanielRosenwasser** said "I actually can't repro the crash with the test case here."

### [PR microsoft/TypeScript-go#3270](https://github.com/microsoft/TypeScript-go/pull/3270) (Closed, **DanielRosenwasser**, **Copilot**)

**Fix declarationMap panic on cross\-file reused nodes**

*Add bounds checks to prevent slice bounds panics when emitting declaration maps for AST nodes reused from other files.*

 * **Copilot** assigned to **DanielRosenwasser**
 * [4 days ago](https://github.com/microsoft/TypeScript-go/pull/3270#issuecomment-4144391482) **DanielRosenwasser** said "This is not a good fix. You can only emit a position if a given node belongs to the containing tree, and that's not always the case."
 * [4 days ago](https://github.com/microsoft/TypeScript-go/pull/3270#issuecomment-4144421535) **jakebailey** said "This is wrong. #3274"
 * (today) **DanielRosenwasser** closed the issue

### [Issue microsoft/TypeScript-go#3280](https://github.com/microsoft/TypeScript-go/issues/3280) (Closed)

**\[ServerErrors\]\[TypeScript\] main vs **

*The TypeScript main branch pipeline analyzing 300 popular GitHub repositories encountered server errors and yielded mixed analysis outcomes.*

 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/3280#issuecomment-4145864719) **typescript-bot** reported that the server connection closed prematurely with undefined and provided affected repository details, raw error text, replay commands, recent requests, and repro steps
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/3280#issuecomment-4145864751) **typescript-bot** reported a server connection closed prematurely error with affected repos and replay commands
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/3280#issuecomment-4145864801) **typescript-bot** reported a runtime panic while handling textDocument/completion due to index out of range
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#3281](https://github.com/microsoft/TypeScript-go/issues/3281) (Closed)

**\[ServerErrors\]\[TypeScript\] main vs **

*The TypeScript error-deltas pipeline reported errors, timeouts, and failures while analyzing 300 popular GitHub repositories on main.*

 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/3281#issuecomment-4145960967) **typescript-bot** reported a server connection closed prematurely error and provided affected repos, request logs, and repro steps
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/3281#issuecomment-4145961000) **typescript-bot** reported a premature server connection closure error with undefined message and provided affected repos, error artifacts, recent requests, and repro steps
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/3281#issuecomment-4145961026) **typescript-bot** reported a panic during textDocument/formatting due to a debug failure "False expression: Token end is child end"
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#3285](https://github.com/microsoft/TypeScript-go/pull/3285) (Closed)

**Remove GetOptionsDiagnostics, global diags in editor, restore checker affinity**

*Remove GetOptionsDiagnostics, expose global diagnostics to the editor, restore consistent checker affinity, and simplify the CheckerPool interface.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3285#issuecomment-4164933461) **andrewbranch** said "This looks good to me, except I don't really know how to evaluate the --incremental baseline changes. Have you validated that they look right/acceptable?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3285#issuecomment-4165027220) **jakebailey** explained that GetDiagnosticsOfAnyProgram checked the length of diagnostics slices causing GetOptionsDiagnostics to duplicate diagnostics and fail the length check, and noted that tsbuildinfo encodes files that weren't checked
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3299](https://github.com/microsoft/TypeScript-go/pull/3299) (Closed)

**Refactor and improve generated LSP code**

*Refactor the generated LSP protocol code to eliminate redundant JSON decoding by improving union discrimination and registration option typing.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3301](https://github.com/microsoft/TypeScript-go/pull/3301) (Open, **RyanCavanaugh**, **Copilot**)

**Fix type inference ordering inconsistency with discriminated unions and flatMap**

*Replace subtype-based tiebreaker with asymmetric assignability to fix inconsistent discriminated union inference in flatMap.*

 * created by **Copilot**
 * (yesterday) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3301#issuecomment-4164919761) **jakebailey** said "This caused one break: https://github.com/microsoft/TypeScript/pull/63328#issuecomment-4164789350"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3301#issuecomment-4165820632) **typescript-bot** reported that user tests showed one Git clone failure likely unrelated to the change and that everything else looked good

### [Issue microsoft/TypeScript-go#3302](https://github.com/microsoft/TypeScript-go/issues/3302) (Closed, `Needs More Info`)

**panic crash**

*The TypeScript-Go language server panics with a slice bounds out of range error when processing hover requests.*

 * created by **ShenHongFei**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3302#issuecomment-4163969829) **DanielRosenwasser** said "Do you remember what you were hovering your mouse over? Any chance you could provide a minimal repro?"
 * **RyanCavanaugh** added label `Needs More Info`
 * [today](https://github.com/microsoft/TypeScript-go/issues/3302#issuecomment-4166341697) **RyanCavanaugh** asked for a repro and detailed investigation of a panic in LineAndCharacterToPosition due to out-of-sync line map and text
 * [today](https://github.com/microsoft/TypeScript-go/issues/3302#issuecomment-4166815054) **ShenHongFei** said "Sorry, I'm unable to reproduce this problem right now. I'll resubmit the relevant code files if it occurs again."
 * (today) **ShenHongFei** closed the issue

### [PR microsoft/TypeScript-go#3303](https://github.com/microsoft/TypeScript-go/pull/3303) (Open)

**Restore fine\-grained ID errors**

*Store fine-grained ID inference errors in inferred types for precise quickfix location reporting.*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#3304](https://github.com/microsoft/TypeScript-go/pull/3304) (Open)

**Add isolatedDeclarations quickfix**

*Port fourslash generator code to implement an isolatedDeclarations quickfix for improved code fixes.*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#3305](https://github.com/microsoft/TypeScript-go/pull/3305) (Open, **DanielRosenwasser**, **Copilot**)

**Add "Sort Imports" &amp; "Remove Unused Imports" commands to VS Code extension**

*Register sort and remove unused imports commands in the VS Code extension using TypeScript/JavaScript IDs to invoke built-in source actions.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **DanielRosenwasser**

### [PR microsoft/TypeScript-go#3306](https://github.com/microsoft/TypeScript-go/pull/3306) (Open, **RyanCavanaugh**, **Copilot**)

**Implement \`resolveFromTypeRoot\` fallback in module resolution**

*Implement resolveFromTypeRoot fallback in the Go module resolver to match TypeScript's typeRoots resolution behavior.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**

### [PR microsoft/TypeScript-go#3307](https://github.com/microsoft/TypeScript-go/pull/3307) (Open, **RyanCavanaugh**, **Copilot**)

**Add test coverage for styled\-jsx \`jsx\` prop on \`\<style\>\` elements via module augmentation**

*Add a regression test ensuring module augmentation properly recognizes styled-jsx’s jsx and global props on <style> elements without errors.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**

### [PR microsoft/TypeScript-go#3308](https://github.com/microsoft/TypeScript-go/pull/3308) (Closed)

**Add GH CLI to \`devcontainer\.json\`\.**

*Include the GitHub CLI in the devcontainer.json configuration to ensure the development container has GH CLI installed.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#3309](https://github.com/microsoft/TypeScript-go/pull/3309) (Open)

**Don't strip release binaries**

*Disable stripping of release binaries to retain debug symbols for easier debugging and tooling support despite larger package size*

 * created by **jakebailey**

### [Issue microsoft/TypeScript-go#3310](https://github.com/microsoft/TypeScript-go/issues/3310) (Open, `Domain: Declaration Emit`, **weswigham**)

**Non\-exported interfaces triggers a "cannot be named" error**

*Exported variable using a type alias based on a non-exported interface triggers a "cannot be named" error in TypeScript 7.*

 * created by **DanielRosenwasser**

### [PR microsoft/TypeScript-go#3311](https://github.com/microsoft/TypeScript-go/pull/3311) (Open)

**Add expandable hover**

*Implement an expandable hover feature in VSCode by adding a custom API over LSP and swapping hover providers.*

 * created by **jakebailey**

### [Issue microsoft/TypeScript-go#3312](https://github.com/microsoft/TypeScript-go/issues/3312) (Closed, `Domain: Editor`)

**latest release \[0\.20260401\.1\] breaks LSP on VS code**

*Version 0.20260401.1 of the extension fails to load in VS Code 1.113.0 on Linux due to a missing typescript.native-preview-enable command*

 * created by **christophe-g**
 * **christophe-g** added label `Domain: Editor`

