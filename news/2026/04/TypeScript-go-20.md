# Report for 2026-04-20 (Monday, April 20th, 2026)

16 different users commented on 27 different issues.

## Recommended Actions

 * Response Recommended
    * @nileshpatil6 asked if adding a module-level cache and submitting a PR would be worthwhile in [microsoft/TypeScript-go#2836](https://github.com/microsoft/TypeScript-go/issues/2836#issuecomment-4284229955)
    * @liby provided verbose server logs and panic instances for debugging in [microsoft/TypeScript-go#3441](https://github.com/microsoft/TypeScript-go/issues/3441#issuecomment-4285743482)

## Activity Summary

### [Issue microsoft/TypeScript-go#2780](https://github.com/microsoft/TypeScript-go/issues/2780) (Closed, `Domain: Editor`, `Needs More Info`, **andrewbranch**)

**High memory consumption in a large pnpm monorepo**

*PR #2502 causes minor edits in a large pnpm monorepo to spike the TypeScript extension memory from ~700MB to ~35GB.*

 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-4262619314) **andrewbranch** said "@AndreiTS I think the issue in your video is #3423."
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-4267836701) **AndreiTS** confirmed that the issue matched #3423 and reported it was fixed in the new tsgo version with about 1.3 GiB RAM usage
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-4276975338) **shinichy** described a proposed fix for getPackageRealpathFuncs to follow node_modules symlinks, provided a commit link and observed a reduced memory increase, and asked if the fix makes sense
 * [today](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-4283748988) **andrewbranch** incorporated the provided test with per-package-directory substitution and instructed users to collect heap profiles if issues persisted
 * (today) **andrewbranch** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-4285767799) **shinichy** said "I confirmed that the main fixed this issue on my side! Thank you! I'm excited to start using tsgo again!"

### [Issue microsoft/TypeScript-go#2836](https://github.com/microsoft/TypeScript-go/issues/2836) (Open, `possible improvement`)

**Cache \`getExePath\(\)\` for performance reasons**

*Cache getExePath results to avoid redundant lookups and improve tsgo invocation performance.*

 * [8 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2836#issuecomment-3928421769) **jakebailey** said "If the import is that slow, we could switch to using plain FS lookups, since peer deps must be "peers" in a parent dir..."
 * (3 weeks ago) **RyanCavanaugh** added label `possible improvement`, and set milestone to `Possible Improvement`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2836#issuecomment-4284229955) **nileshpatil6** apologized for the noise on #3450, acknowledged the FS walk approach was wrong, suggested adding a module-level cache around import.meta.resolve/require.resolve logic, and asked if a PR would be worthwhile
 * [today](https://github.com/microsoft/TypeScript-go/issues/2836#issuecomment-4284246802) **jakebailey** noted that multiple tsgo invocations would not be helped by that cache form and guessed that paths might be hardcoded due to missing code
 * [today](https://github.com/microsoft/TypeScript-go/issues/2836#issuecomment-4286470961) **tido64** apologized for the delay and clarified that they stored the exec path in node_modules/.cache/tsgo, noted that the file location did not affect the architecture, and described using getExePath with persisting to disk (link provided)
 * [today](https://github.com/microsoft/TypeScript-go/issues/2836#issuecomment-4286516248) **jakebailey** said "I'm beyond surprised that this helps at all, given both hit the disk and "importing a module" should be the least of anyone's concerns. I'll have to try it and see..."

### [PR microsoft/TypeScript-go#3328](https://github.com/microsoft/TypeScript-go/pull/3328) (Closed, **andrewbranch**, **Copilot**)

**Fix auto\-imports inserting \`import\` in CJS files when \`moduleDetection\` is \`force\`**

*When moduleDetection is forced, auto-imports wrongly generate import statements in CommonJS files instead of require calls.*

 * created by **Copilot**
 * (2 weeks ago) **Copilot** assigned to **Copilot**, **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3328#issuecomment-4285088068) **Copilot** implemented detectSyntax/detectSyntaxIndicators utility to properly handle moduleDetection force and non-force scenarios, updated fallback behaviors, and added a test for --module preserve + --moduleDetection force + JS require-only files

### [PR microsoft/TypeScript-go#3427](https://github.com/microsoft/TypeScript-go/pull/3427) (Closed, **ahejlsberg**, **Copilot**)

**Fix isDeeplyNestedType false positive for concrete TypeReferences in multi\-checker mode**

*Use concrete type instances as recursion identities to eliminate false-positive type compatibility in tsgo’s multi-checker mode.*

 * (4 days ago) **RyanCavanaugh** set milestone to `TypeScript 7.0 RC`, assigned to **ahejlsberg**, and unassigned **RyanCavanaugh**
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#3438](https://github.com/microsoft/TypeScript-go/issues/3438) (Closed, `Crash`, **jakebailey**, **Copilot**)

**Referencing a \`\.d\.ts\` file on disk via \`\.ts\` in a paths entry crashes**

*Referencing a `.d.ts` file via a `.ts` path mapping in the TypeScript configuration causes a panic in the type checker.*

 * **Mike-Dax** added label `Crash`
 * (3 days ago) **jakebailey** assigned to **Copilot**, **jakebailey**
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#3439](https://github.com/microsoft/TypeScript-go/pull/3439) (Closed, **jakebailey**, **Copilot**)

**Fix crash when paths entry references \.d\.ts file via \.ts extension**

*Corrects module resolution to prevent crashes when a paths entry specifies a .ts extension but resolves to a .d.ts file.*

 * created by **Copilot**
 * (3 days ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3439#issuecomment-4284239059) **DanielRosenwasser** said "Would prefer for Copilot to make the change."
 * (today) **DanielRosenwasser** closed the issue

### [Issue microsoft/TypeScript-go#3441](https://github.com/microsoft/TypeScript-go/issues/3441) (Closed, **jakebailey**, **Copilot**)

**Panic handling textDocument/semanticTokens/{full,range}: slice bounds out of range and token\-spans\-multiple\-lines**

*Semantic tokens full and range handlers panic due to slice bounds out-of-range errors and multi-line token spans.*

 * created by **liby**
 * (yesterday) **jakebailey** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3441#issuecomment-4283203554) **jakebailey** said "@liby Do you have the files where this happens?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/3441#issuecomment-4285743482) **liby** clarified inability to share original files due to private codebase, corrected that both files were ASCII-only and that the panic was deterministic within a session, and provided verbose server logs with two panic instances showing semantic tokens spanning multiple lines errors

### [PR microsoft/TypeScript-go#3443](https://github.com/microsoft/TypeScript-go/pull/3443) (Closed)

**Provide more accurate rename range in \`prepareRename\` LSP response**

*prepareRename returns ranges with leading trivia because it uses node.getStart instead of node.pos, causing mismatches with rename.*

 * created by **auvred**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3443#issuecomment-4281810956) **jakebailey** said "This seems fine but, no tests change?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3443#issuecomment-4282576036) **auvred** noted no tests changed and asked whether to update fourslash helpers to save results to the baseline
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3444](https://github.com/microsoft/TypeScript-go/pull/3444) (Closed, `dependencies`, `github_actions`)

**Bump the github\-actions group across 1 directory with 2 updates**

*Bump actions/setup-node to v6.4.0 and update github/codeql-action in the root directory.*

 * (today) **dependabot[bot]** added labels `github_actions`, `dependencies`, `github_actions`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3445](https://github.com/microsoft/TypeScript-go/pull/3445) (Closed)

**Improve recursion identity for direct type instantiations**

*Prevent false-positive generative recursion by excluding AST-resolved type references from using their symbol as recursion identity in isDeeplyNestedType.*

 * [today](https://github.com/microsoft/TypeScript-go/pull/3445#issuecomment-4282152795) **typescript-bot** provided automated CI build status updates for various commands
 * [today](https://github.com/microsoft/TypeScript-go/pull/3445#issuecomment-4282308420) **typescript-bot** reported performance run results for requested comparison
 * [today](https://github.com/microsoft/TypeScript-go/pull/3445#issuecomment-4282349186) **typescript-bot** reported the test results comparing main with refs/pull/3445/merge, noted a git clone infrastructure failure, and confirmed everything else looked good
 * [today](https://github.com/microsoft/TypeScript-go/pull/3445#issuecomment-4282370968) **jakebailey** said "Looks like this causes 30% more allocs in mui."
 * [today](https://github.com/microsoft/TypeScript-go/pull/3445#issuecomment-4282656475) **typescript-bot** reported that the comparison of tsc runs on the top 400 repos between main and refs/pull/3445/merge looked good
 * [today](https://github.com/microsoft/TypeScript-go/pull/3445#issuecomment-4283090004) **ahejlsberg** noted that a test run showed check time slightly down but parse time up by 42%.
 * [today](https://github.com/microsoft/TypeScript-go/pull/3445#issuecomment-4283095158) **ahejlsberg** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3445#issuecomment-4283095634) **typescript-bot** posted an automated build status update
 * [today](https://github.com/microsoft/TypeScript-go/pull/3445#issuecomment-4283224037) **typescript-bot** provided the performance run results requested by @ahejlsberg
 * [today](https://github.com/microsoft/TypeScript-go/pull/3445#issuecomment-4283405902) **ahejlsberg** noted that PR #63415 implemented the same change in the Strada code base, observed a failure in one of the top 400 repos caused by duplicate Plugin copies from two vite packages, and remarked that Corsa better eliminated the duplication

### [PR microsoft/TypeScript-go#3446](https://github.com/microsoft/TypeScript-go/pull/3446) (Closed)

**Switch to ubuntu\-slim for small CI jobs**

*Adopt the new ubuntu-slim GitHub Actions runner for small CI jobs to improve resource efficiency.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3447](https://github.com/microsoft/TypeScript-go/pull/3447) (Closed)

**Fix external package realpath during auto\-import collection**

*Fix auto-import realpath resolution to infer external package file paths using per-package directory symlink heuristics and reduce redundant Realpath calls.*

 * created by **andrewbranch**
 * (today) **andrewbranch** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/3447#issuecomment-4285460308) **ozyx** said "Awesome! Thanks for resolving this!"

### [Issue microsoft/TypeScript-go#3448](https://github.com/microsoft/TypeScript-go/issues/3448) (Open)

**\[ServerErrors\]\[JavaScript\] main vs **

*Pipeline analysis of main across 300 popular TypeScript repositories reported server errors, clone failures, timeouts, and other failures.*

 * created by **typescript-bot**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3448#issuecomment-4283766282) **typescript-bot** reported a panic during textDocument/rangeFormatting due to a false expression 'Token end is child end' and included a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/3448#issuecomment-4283766414) **typescript-bot** reported the server connection closed prematurely with undefined for tastejs/todomvc and provided raw error text, replay commands, and repro steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/3448#issuecomment-4283766524) **typescript-bot** reported that the server connection closed prematurely and supplied error details and repro steps for usebruno/bruno
 * [today](https://github.com/microsoft/TypeScript-go/issues/3448#issuecomment-4283766646) **typescript-bot** reported that the server connection closed prematurely with undefined error and provided logs for mui/material-ui
 * [today](https://github.com/microsoft/TypeScript-go/issues/3448#issuecomment-4283766710) **typescript-bot** reported a panic handling request textDocument/diagnostic due to runtime error: invalid memory address or nil pointer dereference

### [PR microsoft/TypeScript-go#3449](https://github.com/microsoft/TypeScript-go/pull/3449) (Closed)

**Remap JS type nodes in declaration emit to TS constructs or fallback to serialization**

*Consolidate JS type node remapping into parse/reparse stage for declaration emit with serialization fallback.*

 * created by **weswigham**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3449#issuecomment-4284178740) **ahejlsberg** said "I'm not familiar with the "the js node remapping logic in the node builder". What does it do?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3449#issuecomment-4284250764) **weswigham** explained that the js node remapping logic in nodecopy.go’s visitExistingNodeTreeSymbolsWorker remapped JSDoc node kinds to TS ones, handled js-only type patterns, and included partial-serialization fallbacks while noting some outdated comments and potential dead code
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript-go#3450](https://github.com/microsoft/TypeScript-go/pull/3450) (Closed)

**perf: replace slow module resolution with FS walk and cache result in getExePath**

*Improve getExePath performance in large monorepos by replacing slow Node resolution with an FS walk and caching.*

 * created by **nileshpatil6**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3450#issuecomment-4284178089) **jakebailey** pointed out that the upward directory walk approach was incorrect based on a linked PR discussion
 * [today](https://github.com/microsoft/TypeScript-go/pull/3450#issuecomment-4284180735) **jakebailey** said "Can you please tell me how you found this issue and what tool was used to send this PR?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3450#issuecomment-4284209430) **nileshpatil6** said "Hi, I used Claude Code to help find and implement this. The approach turned out to be incorrect and the code has bugs so closing this. Sorry for the noise."
 * (today) **nileshpatil6** closed the issue

### [PR microsoft/TypeScript-go#3451](https://github.com/microsoft/TypeScript-go/pull/3451) (Open)

**perf: add TSGO\_BINARY env var and fast\-path sibling check in getExePath**

*Introduce TSGO_BINARY override and a fast-path sibling binary check in getExePath to avoid repeated import.meta.resolve calls and boost performance.*

 * created by **nileshpatil6**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3451#issuecomment-4284655558) **jakebailey** said "If someone has this path, why wouldn't they just run it directly? This seems really special case-y."

### [PR microsoft/TypeScript-go#3452](https://github.com/microsoft/TypeScript-go/pull/3452) (Closed)

**Add submoduleTriaged\.txt**

*Introduce a new ‘triaged’ submoduleTriaged.txt file to segregate and track pending differences awaiting identification and resolution*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3453](https://github.com/microsoft/TypeScript-go/pull/3453) (Closed)

**Error if files do not exist in submoduleAccepted/submoduleTriaged, clean**

*Build fails with an error when expected files are missing in the Accepted/submoduleTriaged submodule.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3454](https://github.com/microsoft/TypeScript-go/pull/3454) (Closed)

**Cancel auto\-import cache warming if changes come in while building**

*Cancel ongoing auto-import cache warming when interim snapshot changes occur to avoid rebuilding outdated registries.*

 * created by **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3454#issuecomment-4284680879) **andrewbranch** requested top100 and perf tests from the typescript bot
 * [today](https://github.com/microsoft/TypeScript-go/pull/3454#issuecomment-4284681146) **typescript-bot** provided automated build status update with test job links
 * [today](https://github.com/microsoft/TypeScript-go/pull/3454#issuecomment-4284762390) **typescript-bot** reported the requested performance run results comparing baseline to pr
 * [today](https://github.com/microsoft/TypeScript-go/pull/3454#issuecomment-4284819032) **gabritto** said "@typescript-bot test tsserver top100"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3454#issuecomment-4284819316) **typescript-bot** reported start of build jobs and provided status and result links
 * [today](https://github.com/microsoft/TypeScript-go/pull/3454#issuecomment-4284866659) **andrewbranch** said "Ah, I thought memory was reported in the LSP section of the perf tests. Oh well."
 * [today](https://github.com/microsoft/TypeScript-go/pull/3454#issuecomment-4284967207) **typescript-bot** reported that running tsc on the top 400 repos comparing main and refs/pull/3454/merge showed no issues
 * [today](https://github.com/microsoft/TypeScript-go/pull/3454#issuecomment-4284985231) **andrewbranch** said "Nobody said 400 🤔 "
 * [today](https://github.com/microsoft/TypeScript-go/pull/3454#issuecomment-4284991574) **jakebailey** said "The bot does min(request, 400) now, since people kept doing top100 and expecting to get much back 😄 "
 * [today](https://github.com/microsoft/TypeScript-go/pull/3454#issuecomment-4285138809) **andrewbranch** stated that the previous approach was wrong, noted that the latest commit halved the runtime of the elastic/kibana replay script but did not affect peak memory usage, and requested tsserver top400 tests
 * [today](https://github.com/microsoft/TypeScript-go/pull/3454#issuecomment-4285138992) **typescript-bot** posted CI job status update with links to build and result details
 * [today](https://github.com/microsoft/TypeScript-go/pull/3454#issuecomment-4285342822) **typescript-bot** reported that a timeout error no longer occurred in tsserver tests on the top 200 repos and included reproduction details
 * [today](https://github.com/microsoft/TypeScript-go/pull/3454#issuecomment-4285342891) **typescript-bot** reported a runtime error due to invalid memory address or nil pointer dereference during textDocument/hover, including a detailed stack trace
 * [today](https://github.com/microsoft/TypeScript-go/pull/3454#issuecomment-4285342976) **typescript-bot** reported a panic during a textDocument/hover request caused by an unhandled case in Type.Target
 * [today](https://github.com/microsoft/TypeScript-go/pull/3454#issuecomment-4285343062) **typescript-bot** reported a panic due to invalid memory address or nil pointer dereference in textDocument/hover while running the top 200 repos suite
 * [today](https://github.com/microsoft/TypeScript-go/pull/3454#issuecomment-4285343126) **typescript-bot** shared panic details and stack trace for textDocument/hover from testing the top 200 repos
 * [today](https://github.com/microsoft/TypeScript-go/pull/3454#issuecomment-4285343191) **typescript-bot** reported a runtime panic in textDocument/hover and provided a detailed stack trace
 * [today](https://github.com/microsoft/TypeScript-go/pull/3454#issuecomment-4285343259) **typescript-bot** reported a panic in textDocument/hover handling caused by invalid memory address or nil pointer dereference
 * [today](https://github.com/microsoft/TypeScript-go/pull/3454#issuecomment-4285883217) **typescript-bot** reported a panic in semantic tokens handling during tsserver tests comparing branches and asked for review
 * [today](https://github.com/microsoft/TypeScript-go/pull/3454#issuecomment-4285883261) **typescript-bot** reported a panic in hover request due to an unhandled case in Type.Target
 * [today](https://github.com/microsoft/TypeScript-go/pull/3454#issuecomment-4285883307) **typescript-bot** provided a panic stack trace from textDocument/hover when running the top 400 repos suite
 * [today](https://github.com/microsoft/TypeScript-go/pull/3454#issuecomment-4285883343) **typescript-bot** shared more changes from running the top 400 repos suite, including a panic handling request for textDocument/hover
 * [today](https://github.com/microsoft/TypeScript-go/pull/3454#issuecomment-4285883387) **typescript-bot** reported a panic in textDocument/hover with a stack trace indicating an unreachable condition during the top 400 repos suite run
 * [today](https://github.com/microsoft/TypeScript-go/pull/3454#issuecomment-4285883432) **typescript-bot** reported a panic handling request textDocument/hover due to a nil pointer dereference
 * [today](https://github.com/microsoft/TypeScript-go/pull/3454#issuecomment-4285883470) **typescript-bot** reported a panic handling error in textDocument/hover due to an invalid memory address or nil pointer dereference
 * [today](https://github.com/microsoft/TypeScript-go/pull/3454#issuecomment-4285883520) **typescript-bot** reported a runtime panic in textDocument/hover during top 400 repos suite run
 * [today](https://github.com/microsoft/TypeScript-go/pull/3454#issuecomment-4285883568) **typescript-bot** reported a runtime panic in textDocument/hover when running the top 400 repos suite, including a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/pull/3454#issuecomment-4285883613) **typescript-bot** provided additional panic stack trace details from running the top 400 repos suite
 * [today](https://github.com/microsoft/TypeScript-go/pull/3454#issuecomment-4285883659) **typescript-bot** reported a panic handling in textDocument/hover due to an unhandled Type.Target case with accompanying stack trace
 * [today](https://github.com/microsoft/TypeScript-go/pull/3454#issuecomment-4285883696) **typescript-bot** reported a 'Server connection closed prematurely: undefined' error when running the top 400 repos suite, listing affected repos (continuedev/continue), old server result, last few requests, and repro steps
 * [today](https://github.com/microsoft/TypeScript-go/pull/3454#issuecomment-4285883749) **typescript-bot** reported a server connection closed prematurely error for elastic/kibana with raw error text, replay commands, last requests, and repro steps
 * [today](https://github.com/microsoft/TypeScript-go/pull/3454#issuecomment-4285883781) **typescript-bot** reported a server connection closed prematurely error for t4t5/sweetalert with affected repos, raw error logs, last requests, and repro steps
 * [today](https://github.com/microsoft/TypeScript-go/pull/3454#issuecomment-4285883821) **typescript-bot** reported a debug failure in textDocument/formatting due to a false expression: Token end is child end
 * [today](https://github.com/microsoft/TypeScript-go/pull/3454#issuecomment-4285883867) **typescript-bot** reported a panic during textDocument/hover handling due to an invalid memory address or nil pointer dereference
 * [today](https://github.com/microsoft/TypeScript-go/pull/3454#issuecomment-4285883907) **typescript-bot** reported a panic in textDocument/hover due to an unhandled case in Type.Target during the top 400 repos suite run

### [Issue microsoft/TypeScript-go#3455](https://github.com/microsoft/TypeScript-go/issues/3455) (Closed, `Domain: Editor`, **jakebailey**, **Copilot**)

**Wrong highlight in hover for generic func type with \`property\` and \`accessor\` prefix**

*Hovering over generic property or accessor functions loses syntax highlighting after the closing angle bracket.*

 * created by **Withered-Flower-0422**
 * **Withered-Flower-0422** added label `Domain: Editor`
 * (later) **jakebailey** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#3456](https://github.com/microsoft/TypeScript-go/issues/3456) (Open, `Domain: Declaration Emit`, **weswigham**)

**JS declaration emit ignores properties declared through \`this\.xxx\` assignments**

*Declaration emission for JavaScript ignores properties declared through this.xxx assignments in constructors and methods.*

 * created by **ahejlsberg**
 * (later) **ahejlsberg** added label `Domain: Declaration Emit`, set milestone to `TypeScript 7.0 RC`, and assigned to **weswigham**
 * [later](https://github.com/microsoft/TypeScript-go/issues/3456#issuecomment-4289186020) **Andarist** suggested adding tests for static properties declared in static blocks because Strada emitted an empty class for them

### [PR microsoft/TypeScript-go#3457](https://github.com/microsoft/TypeScript-go/pull/3457) (Closed)

**Fixed crash when resolving declaration spaces on merged symbols resolving to export assignment**

*Fix crash when resolving declaration spaces for merged symbols assigned through an export assignment.*

 * created by **Andarist**

### [PR microsoft/TypeScript-go#3458](https://github.com/microsoft/TypeScript-go/pull/3458) (Closed, **jakebailey**, **Copilot**)

**Use \`typescript\` instead of \`tsx\` for hover code block language**

*Change hover tooltip code blocks to typescript instead of tsx to fix generic type highlighting issues.*

 * created by **Copilot**
 * (later) **Copilot** assigned to **Copilot**, **jakebailey**
 * [later](https://github.com/microsoft/TypeScript-go/pull/3458#issuecomment-4289326792) **jakebailey** confirmed expectation and linked to the relevant code in hover.ts

### [PR microsoft/TypeScript-go#3459](https://github.com/microsoft/TypeScript-go/pull/3459) (Closed)

**Baseline diff triaging**

*Reassign tests to accepted and triaged categories and update the CHANGES.md file.*

 * created by **ahejlsberg**

