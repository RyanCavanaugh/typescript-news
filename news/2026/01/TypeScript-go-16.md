# Report for 2026-01-16 (Friday, January 16th, 2026)

13 different users commented on 24 different issues.

## Recommended Actions

 * Response Recommended
    * @OliverJAsh reported facing the same issue and provided a screenshot in [microsoft/TypeScript-go#2239](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3761933622)

## Activity Summary

### [Issue microsoft/TypeScript-go#1465](https://github.com/microsoft/TypeScript-go/issues/1465) (Closed, `Crash`, `Domain: Program`, **sheetalkamat**)

**Intermittent crash with \-\-incremental**

*tsgo intermittently crashes when run with --incremental on large projects in frequent CI pipelines*

 * [6 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1465#issuecomment-3617919357) **sheetalkamat** said "I think #2051 and #2070 would have fixed this. So if this repros again, please file new issue with repro steps. "
 * (6 weeks ago) **sheetalkamat** closed the issue
 * [6 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1465#issuecomment-3617924178) **jakebailey** said "The above user was testing yesterdays build, but I will extract that to a new issue"
 * (today) **sheetalkamat** reopened the issue

### [Issue microsoft/TypeScript-go#2223](https://github.com/microsoft/TypeScript-go/issues/2223) (Open, `Domain: Editor`)

**Request textDocument/foldingRange failed\.**

*The TypeScript language server panics with a token cache mismatch error when requesting folding ranges in a compiled JavaScript file.*

 * **eamodio** added label `Domain: Editor`
 * [6 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2223#issuecomment-3614758634) **jakebailey** described also encountering the issue in a .ncurc.cjs file and struggling to integrate it into a fourslash test suite
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/2223#issuecomment-3730907291) **jfirebaugh** provided a minimal reproduction snippet
 * [later](https://github.com/microsoft/TypeScript-go/issues/2223#issuecomment-3763299411) **jycouet** provided an additional code snippet with an import statement for Page from '@playwright/test'

### [Issue microsoft/TypeScript-go#2239](https://github.com/microsoft/TypeScript-go/issues/2239) (Closed, `Needs More Info`)

**take too much memory**

*tsgo extension consumes about 17GB of RAM on macOS M1, causing heavy swapping and slowing VS Code.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3756760084) **jakebailey** provided two heap and alloc profiles showing memory usage around 29GB and 13GB and noted that the second run held 9.23GB with about 4GB unused space largely in ASTs
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3757992862) **Neo0724** reported that after restarting the language server memory usage dropped significantly but then increased during editing and did not decrease with garbage collection
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3758010438) **talldan** attached heap and alloc profiles from before and after restarting the language server
 * [today](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3761933622) **OliverJAsh** reported facing the same issue and attached a screenshot

### [PR microsoft/TypeScript-go#2499](https://github.com/microsoft/TypeScript-go/pull/2499) (Closed)

**Fix potential deadlock in case of lsp shutdown**

*Background tasks can block indefinitely sending messages to the outgoingQueue after the writeLoop exits, causing LSP shutdown deadlock.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2499#issuecomment-3755196588) **fubhy** said "The latest CI error is again caused by this: https://github.com/microsoft/typescript-go/pull/2485"
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2499#issuecomment-3755752364) **jakebailey** said "I don't know how you're hitting these races in CI so often when I don't even remember seeing them anywhere until now 😅"
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2499#issuecomment-3755836045) **fubhy** joked about triggering more CI runs due to inexperience with the codebase and Go
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#2511](https://github.com/microsoft/TypeScript-go/issues/2511) (Closed)

**Stale diagnostics on file reload**

*tsgo diagnostics remain stale in Neovim after reloading a changed file until it’s manually edited*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2511#issuecomment-3756594416) **jakebailey** requested the user test the code in their editor with added logging to confirm
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2511#issuecomment-3757108569) **frangio** confirmed the previous theory was wrong, identified the actual cause in overlayfs.go, and noted that removing events.closeChange = nil and handling closeChange before openChange fixed the bug but was unsure of the proper fix
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2511#issuecomment-3757256154) **jakebailey** said "I have a fix, but the test infra is very flaky on this because it's nondeterministic how these changes get batched together..."
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#2513](https://github.com/microsoft/TypeScript-go/pull/2513) (Closed)

**Support \`Object\.defineProperty\` for expando properties and CommonJS exports in JS files**

*Support Object.defineProperty for expando properties and CommonJS exports in JS files, with type, caching, and emit fixes.*

 * created by **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2513#issuecomment-3761959834) **jakebailey** said "Are you planning on putting more into this PR or is it ready?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2513#issuecomment-3762200063) **ahejlsberg** stated the PR was ready, detailed issues in declaration emit, and suggested addressing them in separate PRs

### [PR microsoft/TypeScript-go#2520](https://github.com/microsoft/TypeScript-go/pull/2520) (Closed)

**Fix missing content change during consecutive didClose/didOpen**

*Fixes missing content changes during consecutive didClose/didOpen events but tests remain flaky due to inconsistent event merging.*

 * created by **jakebailey**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2520#issuecomment-3757609285) **frangio** said "I can confirm that this fixes #2511 for me."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2520#issuecomment-3761146478) **andrewbranch** said "Seems good in principle but I really want to know why all those server baselines changed 🤔 "
 * [today](https://github.com/microsoft/TypeScript-go/pull/2520#issuecomment-3761152176) **jakebailey** said "Yeah 🫤"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2520#issuecomment-3761251123) **andrewbranch** said "I think I fixed it"
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#2521](https://github.com/microsoft/TypeScript-go/pull/2521) (Closed)

**Port rootDir default to configFile directory and some module resoluton fixes**

*Port default rootDir to the config file directory and implement several module resolution fixes*

 * created by **sheetalkamat**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2521#issuecomment-3761156007) **andrewbranch** said "Should we get https://github.com/microsoft/TypeScript/pull/62418 in the porting branch of the submodule first so the diffs are clean?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2521#issuecomment-3761175039) **jakebailey** suggested targeting TS 6.0 in the porting branch next week and allowing a few diffs in the meantime
 * (today) **sheetalkamat** closed the issue

### [PR microsoft/TypeScript-go#2524](https://github.com/microsoft/TypeScript-go/pull/2524) (Open)

**feat: detect deprecated via JSDoc and flag deprecated property access**

*Add deprecation detection to Go checker by using JSDoc tags to flag deprecated property access.*

 * created by **AyomiCoder**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2524#issuecomment-3760735963) **AyomiCoder** said "I accept"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2524#issuecomment-3760746607) **AyomiCoder** said "@microsoft-github-policy-service agree"

### [PR microsoft/TypeScript-go#2525](https://github.com/microsoft/TypeScript-go/pull/2525) (Closed, **RyanCavanaugh**, **Copilot**)

**Fix stack overflow when checking destructuring with self\-referencing shorthand**

*Shorthand self-referencing in object destructuring with a union type causes infinite recursion and stack overflow.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**

### [PR microsoft/TypeScript-go#2526](https://github.com/microsoft/TypeScript-go/pull/2526) (Closed, **RyanCavanaugh**, **Copilot**)

**\[WIP\] Fix stack overflow in type checking code**

*WIP pull request fixes stack overflow in TypeScript type checker during union-typed destructuring.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#2527](https://github.com/microsoft/TypeScript-go/issues/2527) (Closed, `bug`, **ahejlsberg**)

**tsgo incorrectly emits both ESM and CJS exports when compiling \`\.js\` files containing \`exports\.xxx\` statements**

*tsgo emits both ES module and CommonJS export definitions when compiling JavaScript files containing exports.xxx statements.*

 * created by **psm14**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2527#issuecomment-3761473819) **jakebailey** said "I suspect this is fixed by one of the fixes in https://github.com/microsoft/typescript-go/pull/2513"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2527#issuecomment-3761948756) **ahejlsberg** confirmed that the fix in the referenced PR resolved the issue
 * (today) **ahejlsberg** added label `bug`, and assigned to **ahejlsberg**

### [PR microsoft/TypeScript-go#2528](https://github.com/microsoft/TypeScript-go/pull/2528) (Open, **RyanCavanaugh**, **Copilot**)

**\[WIP\] Fix stack overflow in code type checking**

*Resolve stack overflow in TypeScript strict type checking for destructured union types with circular references.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**

### [PR microsoft/TypeScript-go#2529](https://github.com/microsoft/TypeScript-go/pull/2529) (Closed)

**Skip macOS in PR CI**

*Skip macOS CI jobs on pull requests and rely on Linux builds, running macOS tests only on the main branch.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2530](https://github.com/microsoft/TypeScript-go/pull/2530) (Open)

**Disable Go CI caching**

*Request to disable Go CI caching due to limited storage and questionable performance benefits.*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#2531](https://github.com/microsoft/TypeScript-go/pull/2531) (Closed)

**Remove output dts additions to program when moduleKind is none as its removed now**

*Remove output dts additions when moduleKind is none since .dts emission is no longer supported.*

 * created by **sheetalkamat**
 * (today) **sheetalkamat** closed the issue

### [PR microsoft/TypeScript-go#2532](https://github.com/microsoft/TypeScript-go/pull/2532) (Closed)

**Incremental fixes**

*Resolve stack overflow errors caused by reference cycles with const enum usage through incremental fixes.*

 * created by **sheetalkamat**

### [Issue microsoft/TypeScript-go#2533](https://github.com/microsoft/TypeScript-go/issues/2533) (Open, `bug`, `Domain: Declaration Emit`, **weswigham**)

**Multiple differences in declaration emit for CommonJS exports**

*TypeScript’s declaration emitter for CommonJS exports uses typeof module.exports, emits duplicate var declarations, and emits var instead of const.*

 * created by **ahejlsberg**
 * (today) **ahejlsberg** added labels `bug`, `Domain: Declaration Emit`, and assigned to **weswigham**

### [PR microsoft/TypeScript-go#2534](https://github.com/microsoft/TypeScript-go/pull/2534) (Closed)

**Fix extended config cache race condition by reordering ref operations**

*Reorder extended config cache reference operations to the start of Clone and introduce RefIfExists to prevent race-condition panics.*

 * created by **maschwenk**
 * (today) **maschwenk** closed the issue

### [PR microsoft/TypeScript-go#2535](https://github.com/microsoft/TypeScript-go/pull/2535) (Closed)

**Fix extended config cache panic by gracefully handling missing entries**

*Gracefully skip missing extended config cache entries to prevent panics and add nil checks in disposal logging.*

 * created by **maschwenk**
 * (today) **maschwenk** closed the issue

### [Issue microsoft/TypeScript-go#2536](https://github.com/microsoft/TypeScript-go/issues/2536) (Closed, `Crash`)

**textDocument/documentHighlight: interface conversion**

*The document highlight feature crashes due to an incorrect conversion of a method node to a function node in the AST.*

 * created by **sanny-io**
 * **sanny-io** added label `Crash`

### [PR microsoft/TypeScript-go#2537](https://github.com/microsoft/TypeScript-go/pull/2537) (Closed)

**Add deprecation suggestion and code fix for computed enum member names**

*Add a deprecation warning and auto-fix to replace computed enum member property names with simple string literals.*

 * created by **magic-akari**
 * (later) **magic-akari** closed the issue

### [PR microsoft/TypeScript-go#2538](https://github.com/microsoft/TypeScript-go/pull/2538) (Closed)

**fix\(2536\): avoid unsafe cast in documentHighlight parent function lookup**

*Avoid unsafe casting during parent function lookup in the documentHighlight feature implementation.*

 * created by **a-tarasyuk**

