# Report for 2026-01-13 (Tuesday, January 13th, 2026)

15 different users commented on 24 different issues.

## Recommended Actions

 * Response Recommended
    * @trueadm provided repro steps as requested in [microsoft/TypeScript-go#1952](https://github.com/microsoft/TypeScript-go/issues/1952#issuecomment-3749948756)
    * @PaulRBerg reported that the issue persisted and could not provide repro steps in [microsoft/TypeScript-go#1967](https://github.com/microsoft/TypeScript-go/issues/1967#issuecomment-3748520962)
    * @talldan reported high memory usage on the WordPress/gutenberg project and included a screenshot in [microsoft/TypeScript-go#2239](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3747982109)
    * @gggdomi followed up about a reported ~2x slowdown and provided repro details in [microsoft/TypeScript-go#2341](https://github.com/microsoft/TypeScript-go/issues/2341#issuecomment-3746122283)
    * @pedro757 provided package.json dependencies as requested in [microsoft/TypeScript-go#2473](https://github.com/microsoft/TypeScript-go/issues/2473#issuecomment-3745606596)
    * @christophe-g provided the closest package.json as requested in [microsoft/TypeScript-go#2473](https://github.com/microsoft/TypeScript-go/issues/2473#issuecomment-3745786414)
    * @rubenferreira97 reported the error and asked for help reproducing it in [microsoft/TypeScript-go#2501](https://github.com/microsoft/TypeScript-go/issues/2501#issuecomment-3747026777)

## Activity Summary

### [Issue microsoft/TypeScript-go#1531](https://github.com/microsoft/TypeScript-go/issues/1531) (Open, `Crash`, `Domain: Program`, **sheetalkamat**)

**tsgo panics with invalid UTF\-8 when marshalling build info**

*tsgo panics during build info marshalling because it encounters invalid UTF-8 in diagnostic messages.*

 * [22 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1531#issuecomment-3177160268) **jakebailey** explained that internal symbols appearing publicly were bugs and noted that some internal symbols used a `=` prefix, suggesting that his PR might be correct enough
 * **jakebailey** added label `Domain: Program`
 * **RyanCavanaugh** assigned to **sheetalkamat**
 * [today](https://github.com/microsoft/TypeScript-go/issues/1531#issuecomment-3746812464) **gabritto** said "Related: #2336"

### [Issue microsoft/TypeScript-go#1952](https://github.com/microsoft/TypeScript-go/issues/1952) (Closed, `Crash`, `Needs More Info`, **DanielRosenwasser**, **weswigham**)

**Declaration emit crash**

*The declaration emitter panics with ‘Unknown parent for parameter: KindArrowFunction’ during compilation.*

 * [6 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1952#issuecomment-3589398392) **trueadm** provided a minimal reproduction and noted it worked fine with tsc
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1952#issuecomment-3675234201) **trueadm** said "@DanielRosenwasser if you get time, please could you let me know if that repro is of any use, if not, I can try and come up with another."
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/1952#issuecomment-3730952976) **jakebailey** said "@trueadm I tried out your repro on main and it did not crash. Is this fixed for you in the past few weeks?"
 * [later](https://github.com/microsoft/TypeScript-go/issues/1952#issuecomment-3749948756) **trueadm** said "@jakebailey Unfortunately, it still repros for me using 7.0.0-dev.20260114.1. If you follow the steps in the README.md it should repro for you too."

### [Issue microsoft/TypeScript-go#1967](https://github.com/microsoft/TypeScript-go/issues/1967) (Open, `Crash`, **andrewbranch**)

**Request textDocument/documentSymbol failed\.**

*The TypeScript language server intermittently fails textDocument/documentSymbol requests with “no project found for URI” errors when saving files in a monorepo.*

 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/1967#issuecomment-3725018741) **tmcdo1** reported encountering the same RequestedLanguageService (project not loaded) error in a monorepo with TS Native Preview extension and provided logs and configuration details
 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/1967#issuecomment-3726528187) **andrewbranch** said "I think I probably fixed this in #2456, but without a repro, there’s no way of knowing."
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/1967#issuecomment-3728472084) **rubnogueira** said "Thank you! This was still happening frequently in our codebase, but I just updated to 0.20260109.1 and I will report back if the fix is working."
 * [later](https://github.com/microsoft/TypeScript-go/issues/1967#issuecomment-3748520962) **PaulRBerg** reported that the issue persisted with version 7.0.0-dev.20260113.1 when AI agents modified many files and that they could not provide a repro

### [PR microsoft/TypeScript-go#2020](https://github.com/microsoft/TypeScript-go/pull/2020) (Open)

**Support for custom configurations**

*Update tsgo LSP to support passing custom configurations via a rebased version of the previous PR.*

 * created by **johnnycheng0210**
 * [9 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2020#issuecomment-3493021126) **jakebailey** said "I'm not sure what happened with your PRs, but can you keep the one you intend us to look at open and keep pushing to that one?"
 * [9 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2020#issuecomment-3499951692) **johnnycheng0210** said "ah sorry - i was rebasing PR's - i will close the previous PR and use this one instead"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2020#issuecomment-3746994608) **jakebailey** said "One thing this might be missing is some handling of on-change events; (*Session).Configure handles things; maybe pendingConfigChanges is sufficient to catch this?"

### [Issue microsoft/TypeScript-go#2239](https://github.com/microsoft/TypeScript-go/issues/2239) (Open, `Needs More Info`)

**take too much memory**

*tsgo extension consumes about 17GB of RAM on macOS M1, causing heavy swapping and slowing VS Code.*

 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3628246716) **maxired** confirmed that running vscode with the GOMEMLIMIT variable set worked, noted that 2048MiB was sufficient, and said they would report any further crashes
 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3631565394) **maxired** said "Actually even with GOMEMLIMIT=2048MiB, after half a day working, my tsgo would eat 13GB of ram, while I have only 6 files opened in vscode"
 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3633459027) **abelcha** explained that the setting did not apply with the native preview extension, noted that Node was not involved in launching the language server, suggested tsgo was not enabled, proposed a cursor issue, and attached process samples
 * [today](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3747982109) **talldan** reported experiencing high memory usage up to 50GB while using the native preview plugin for VS Code on the WordPress/gutenberg project and noted it increased further after restarting

### [Issue microsoft/TypeScript-go#2341](https://github.com/microsoft/TypeScript-go/issues/2341) (Closed)

**Performance regression with \`\-\-incremental\` between \`native\-preview\-0\.20251211\.1\` and \`0\.20251209\.1\`**

*First-run incremental type checking in native-preview-0.20251211.1 is three times slower than in native-preview-0.20251209.1.*

 * [1 month ago](https://github.com/microsoft/TypeScript-go/issues/2341#issuecomment-3663549411) **jakebailey** requested profiling data by having the user set --pprofDir and upload the profiles, and asked for access to the relevant code
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2341#issuecomment-3666472700) **gggdomi** reproduced a 1.7x slowdown on Mikro-ORM after commit #2314, suggested CI performance snapshots to detect regressions, and provided repro steps
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2341#issuecomment-3677655142) **hg** reported that commit b0fed9f5bb0d29327e5ee8ba8e0051592cd76639 introduced a twofold slowdown compared to e93d36401a3f6c19a5e7384abbbf40aa210d7cda and provided benchmark details
 * [today](https://github.com/microsoft/TypeScript-go/issues/2341#issuecomment-3746122283) **gggdomi** followed up about a ~2x slowdown affecting all projects and noted a repro in the first open source repo tried
 * [today](https://github.com/microsoft/TypeScript-go/issues/2341#issuecomment-3746172630) **jakebailey** said "I did, it's in my inbox, I just haven't gotten to this item yet"

### [Issue microsoft/TypeScript-go#2426](https://github.com/microsoft/TypeScript-go/issues/2426) (Closed, `bug`, `Domain: Editor`)

**goToDefinition for pattern ambient module no longer goes to implementation**

*Using tsgo, goToDefinition on pattern ambient CSS modules navigates to the ambient declaration instead of the CSS file implementation.*

 * created by **aaronadamsCA**
 * (2 weeks ago) **DanielRosenwasser** added labels `bug`, `Domain: Editor`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2429](https://github.com/microsoft/TypeScript-go/pull/2429) (Closed)

**fix\(2426\): goToDefinition for pattern ambient module no longer goes to implementation **

*goToDefinition for pattern-based ambient modules no longer navigates to their implementation.*

 * created by **a-tarasyuk**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2429#issuecomment-3741086466) **jakebailey** said "PR is failing because the failing tests need to be updated"
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2473](https://github.com/microsoft/TypeScript-go/issues/2473) (Closed, `Crash`, **andrewbranch**)

**Autocompletion panics**

*Autocompletion and autoimport suggestions trigger a panic due to an unexpected internal symbol name in export.*

 * [today](https://github.com/microsoft/TypeScript-go/issues/2473#issuecomment-3743143024) **lukpsaxo** reported that after issue #2482 was fixed, tsgo now frequently panics with 'unexpected internal symbol name in export'
 * [today](https://github.com/microsoft/TypeScript-go/issues/2473#issuecomment-3743155751) **christophe-g** confirmed same behavior after fix to #2482 and apologized for inability to produce a repro
 * [today](https://github.com/microsoft/TypeScript-go/issues/2473#issuecomment-3743892331) **pedro757** reported that the issue was still present in version 7.0.0-dev.20260113.1
 * [today](https://github.com/microsoft/TypeScript-go/issues/2473#issuecomment-3745522473) **andrewbranch** requested package.json dependency data from users experiencing the crash
 * **andrewbranch** assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2473#issuecomment-3745606596) **pedro757** provided the closest package.json snippet showing dependencies
 * [today](https://github.com/microsoft/TypeScript-go/issues/2473#issuecomment-3745786414) **christophe-g** provided the closest package.json snapshot
 * [today](https://github.com/microsoft/TypeScript-go/issues/2473#issuecomment-3746071241) **DanielRosenwasser** provided repro steps for the issue
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#2477](https://github.com/microsoft/TypeScript-go/pull/2477) (Closed)

**Simplify getGlobalTypingsCacheLocation**

*Simplify getGlobalTypingsCacheLocation by relying solely on os.UserCacheDir instead of manual fallback logic.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2478](https://github.com/microsoft/TypeScript-go/pull/2478) (Open)

**Exit LSP process if parent process stops existing**

*Implement periodic parent process ID checks in the LSP server to terminate the server when the parent process exits.*

 * created by **jakebailey**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2478#issuecomment-3741141626) **DanielRosenwasser** said "If the parent process no longer exists, won't we get an EOF on standard input or something?"
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2478#issuecomment-3741155153) **jakebailey** said "Yeah, I guess that's probably the case..."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2478#issuecomment-3746460286) **DanielRosenwasser** said "https://github.com/microsoft/typescript-go/pull/2499 might explain why an EOF was not sufficient for shutting down."

### [Issue microsoft/TypeScript-go#2489](https://github.com/microsoft/TypeScript-go/issues/2489) (Closed, `Crash`, **andrewbranch**)

**Unprompted panic from auto\-import indexing**

*Language server auto-import indexing panics with “Cannot index entry with empty name” during stress testing on the webpack repository*

 * **DanielRosenwasser** added label `Crash`
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2489#issuecomment-3741608996) **DanielRosenwasser** provided reproduction steps for a panic in the typescript-native-preview output pane when editing generate-wasm-code.js in the webpack repository
 * **DanielRosenwasser** assigned to **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#2492](https://github.com/microsoft/TypeScript-go/issues/2492) (Closed, `Crash`, **DanielRosenwasser**, **Copilot**)

**Signature help crash for signature with binding pattern parameters**

*Signature help panics when encountering binding pattern parameters in function signatures due to an unhandled AST case.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2492#issuecomment-3741762237) **DanielRosenwasser** suggested that a missing test might explain the lack of graceful printing of binding patterns and their types, as was done in the old codebase
 * (yesterday) **DanielRosenwasser** assigned to **Copilot**, **DanielRosenwasser**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2494](https://github.com/microsoft/TypeScript-go/pull/2494) (Closed, **DanielRosenwasser**, **Copilot**)

**Fix signature help crash for binding pattern parameters**

*Fixes a crash in signature help when encountering binding pattern parameters by adding pattern checks and comprehensive tests.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2494#issuecomment-3742381878) **DanielRosenwasser** said "@copilot actually make it possible to review what the signature help is - use VerifyBaselineSignatureHelp (or create it if it doesn't yet exist)."
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2494#issuecomment-3742429568) **Copilot** updated the test to use VerifyBaselineSignatureHelp and added a baseline file showing signature help output for all binding pattern cases
 * [today](https://github.com/microsoft/TypeScript-go/pull/2494#issuecomment-3742871708) **DanielRosenwasser** said "@copilot address."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2495](https://github.com/microsoft/TypeScript-go/pull/2495) (Closed)

**Fix race condition between flush and snapshot update**

*A race condition between flush and snapshot updates caused stale completions and test failures, now resolved by adding a mutex.*

 * created by **fubhy**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2496](https://github.com/microsoft/TypeScript-go/issues/2496) (Closed)

**Crashes on every syntax error**

*TypeScript-native server crashes whenever syntax errors occur, requiring a restart for each error.*

 * created by **sjtsh**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2496#issuecomment-3743149995) **lukpsaxo** said "the actual panic i think is missing from your snippet but it looks the same as #2473"
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#2497](https://github.com/microsoft/TypeScript-go/issues/2497) (Closed)

**LSP panic in autoimport: unexpected internal symbol name in export**

*LSP autoimport feature panics with 'unexpected internal symbol name in export' during code completion.*

 * created by **adri1wald**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2497#issuecomment-3744162368) **bessey** reported experiencing the same panic error and clarified using zod@4 instead of posthog-node
 * [today](https://github.com/microsoft/TypeScript-go/issues/2497#issuecomment-3744908092) **christophe-g** said "Probably same as #2473"
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#2499](https://github.com/microsoft/TypeScript-go/pull/2499) (Closed)

**Fix potential deadlock in case of lsp shutdown**

*Background tasks can block indefinitely sending messages to the outgoingQueue after the writeLoop exits, causing LSP shutdown deadlock.*

 * created by **fubhy**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2499#issuecomment-3746598756) **jakebailey** thanked for looking into the issue and suggested plumbing a proper context instead of using Background() for long-running operations
 * [later](https://github.com/microsoft/TypeScript-go/pull/2499#issuecomment-3749326802) **fubhy** proposed an example for plumbing proper context and asked if it aligned with the suggestion

### [PR microsoft/TypeScript-go#2500](https://github.com/microsoft/TypeScript-go/pull/2500) (Closed)

**Fix auto imports crashes from bad names**

*Improve export name generation and skip invalid namespace or re-exports to prevent auto-import crashes from bad or missing names.*

 * created by **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#2501](https://github.com/microsoft/TypeScript-go/issues/2501) (Open, `Crash`)

**textDocument/completion: runtime error: slice bounds out of range \[:2615\] with length 2590**

*The TypeScript-Go language server panics with a slice bounds out of range error during textDocument/completion requests.*

 * created by **sanny-io**
 * **sanny-io** added label `Crash`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2501#issuecomment-3747026777) **rubenferreira97** reported experiencing the error but was unable to reproduce it

### [PR microsoft/TypeScript-go#2502](https://github.com/microsoft/TypeScript-go/pull/2502) (Closed)

**Fix module specifier cache misses in symlinked package directories**

*Fix module specifier cache misses in symlinked package directories to reduce completion times from 8.3 seconds to 120ms.*

 * created by **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2502#issuecomment-3747135586) **andrewbranch** said "I need to look closer at the project reference specific code. @jansedlon’s draft pointed out that we want those to take the slow path, but I want to see if that’s really necessary."
 * [later](https://github.com/microsoft/TypeScript-go/pull/2502#issuecomment-3748858762) **rubnogueira** said "@andrewbranch happy to provide additional context if needed, thank you!"

### [Issue microsoft/TypeScript-go#2503](https://github.com/microsoft/TypeScript-go/issues/2503) (Open)

**Autocomplete and auto\-import is slower in JSX context**

*JSX tag autocomplete and auto-import in TypeScript monorepos remains slow (~1s vs ~100ms) due to expensive contextual type computation.*

 * created by **jansedlon**

