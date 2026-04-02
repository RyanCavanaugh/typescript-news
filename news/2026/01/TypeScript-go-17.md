# Report for 2026-01-17 (Saturday, January 17th, 2026)

4 different users commented on 8 different issues.

## Recommended Actions

 * Response Recommended
    * @chesterbait88 asked if maintainers were working on the memory issue in [microsoft/TypeScript-go#2239](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3764459330)
    * @so1ve asked about integrating colored and formatted tsgo help text into the CLI's help in [microsoft/TypeScript-go#2540](https://github.com/microsoft/TypeScript-go/issues/2540#issuecomment-3765403442)

## Activity Summary

### [Issue microsoft/TypeScript-go#2239](https://github.com/microsoft/TypeScript-go/issues/2239) (Closed, `Needs More Info`)

**take too much memory**

*tsgo extension consumes about 17GB of RAM on macOS M1, causing heavy swapping and slowing VS Code.*

 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3757992862) **Neo0724** reported that after restarting the language server memory usage dropped significantly but then increased during editing and did not decrease with garbage collection
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3758010438) **talldan** attached heap and alloc profiles from before and after restarting the language server
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3761933622) **OliverJAsh** reported facing the same issue and attached a screenshot
 * [today](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3764459330) **chesterbait88** reported that TSGO consumed 60 GB, crashed the system, and asked if maintainers were investigating

### [PR microsoft/TypeScript-go#2513](https://github.com/microsoft/TypeScript-go/pull/2513) (Closed)

**Support \`Object\.defineProperty\` for expando properties and CommonJS exports in JS files**

*Support Object.defineProperty for expando properties and CommonJS exports in JS files, with type, caching, and emit fixes.*

 * created by **ahejlsberg**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2513#issuecomment-3761959834) **jakebailey** said "Are you planning on putting more into this PR or is it ready?"
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2513#issuecomment-3762200063) **ahejlsberg** stated the PR was ready, detailed issues in declaration emit, and suggested addressing them in separate PRs
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#2527](https://github.com/microsoft/TypeScript-go/issues/2527) (Closed, `bug`, **ahejlsberg**)

**tsgo incorrectly emits both ESM and CJS exports when compiling \`\.js\` files containing \`exports\.xxx\` statements**

*tsgo emits both ES module and CommonJS export definitions when compiling JavaScript files containing exports.xxx statements.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2527#issuecomment-3761948756) **ahejlsberg** confirmed that the fix in the referenced PR resolved the issue
 * (yesterday) **ahejlsberg** added label `bug`, and assigned to **ahejlsberg**
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#2536](https://github.com/microsoft/TypeScript-go/issues/2536) (Closed, `Crash`)

**textDocument/documentHighlight: interface conversion**

*The document highlight feature crashes due to an incorrect conversion of a method node to a function node in the AST.*

 * created by **sanny-io**
 * **sanny-io** added label `Crash`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2538](https://github.com/microsoft/TypeScript-go/pull/2538) (Closed)

**fix\(2536\): avoid unsafe cast in documentHighlight parent function lookup**

*Avoid unsafe casting during parent function lookup in the documentHighlight feature implementation.*

 * created by **a-tarasyuk**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2539](https://github.com/microsoft/TypeScript-go/pull/2539) (Open)

**Add support for importing JSON modules "as const"**

*Enable an opt-in compiler option importJsonAsConst to import JSON modules with const semantics.*

 * created by **james-pre**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2539#issuecomment-3764651309) **james-pre** said "@microsoft-github-policy-service agree"

### [Issue microsoft/TypeScript-go#2540](https://github.com/microsoft/TypeScript-go/issues/2540) (Open)

**Should handle \`FORCE\_COLOR\` environment variable**

*Support the FORCE_COLOR environment variable to override TTY detection and enable colored output for exec calls*

 * created by **so1ve**
 * [later](https://github.com/microsoft/TypeScript-go/issues/2540#issuecomment-3765354673) **jakebailey** questioned why this was needed now given the old codebase didn't do it
 * [later](https://github.com/microsoft/TypeScript-go/issues/2540#issuecomment-3765403442) **so1ve** described the difference between vue-tsc and vue-tsgo and requested colored and formatted tsgo help text appended to the CLI's help text like tsx

