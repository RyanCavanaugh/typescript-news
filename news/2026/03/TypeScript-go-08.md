# Report for 2026-03-08 (Sunday, March 8th, 2026)

13 different users commented on 14 different issues.

## Recommended Actions

 * Response Recommended
    * @s-h-a-d-o-w asked if this should also be a todo for tsgo in [microsoft/TypeScript-go#3023](https://github.com/microsoft/TypeScript-go/issues/3023#issuecomment-4019462263)
    * @connorshea asked if the warning color was always used intentionally in [microsoft/TypeScript-go#3026](https://github.com/microsoft/TypeScript-go/issues/3026#issuecomment-4020459388)
    * @connorshea suggested updating the icon placement and styling to better indicate experimental status in [microsoft/TypeScript-go#3026](https://github.com/microsoft/TypeScript-go/issues/3026#issuecomment-4021367208)
    * @simonbuchan reported another styled-components variant that may exhibit the same TS issue in [microsoft/TypeScript-go#3027](https://github.com/microsoft/TypeScript-go/issues/3027#issuecomment-4020873172)

## Activity Summary

### [PR microsoft/TypeScript-go#2688](https://github.com/microsoft/TypeScript-go/pull/2688) (Closed, **RyanCavanaugh**, **Copilot**)

**Port TypeScript PR \#63054: Default \`types\` to \`\[\]\`, support \`"\*"\` wildcard**

*Default the types compiler option to an empty array and support a "*" wildcard for automatic type package discovery*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2688#issuecomment-3930903832) **DanielRosenwasser** asked if an error update for core/built-in modules for Node.js was missing
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2688#issuecomment-3930910609) **jakebailey** said "@copilot Look into this; recheck the original PR for missing bits."
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2688#issuecomment-3930958354) **Copilot** added the missing getCannotResolveModuleNameErrorForSpecificModule function, included beforeEach in test runner cases and NodeJS in node cases, and fixed in commit 6a48e64
 * [today](https://github.com/microsoft/TypeScript-go/pull/2688#issuecomment-4021328498) **DanielRosenwasser** said "@copilot merge from main, update the submodule, accept baselines"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2688#issuecomment-4021401123) **Copilot** merged from main, verified submodule contains PR #63054, and accepted baselines in commit df0db5c

### [PR microsoft/TypeScript-go#3019](https://github.com/microsoft/TypeScript-go/pull/3019) (Closed)

**Fix out\-of\-range document symbol error**

*Typing 'export =' followed by a space in an empty TypeScript file triggers documentSymbol to fail due to out-of-range selection.*

 * created by **ahejlsberg**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3019#issuecomment-4017989682) **Copilot** said "@DanielRosenwasser I've opened a new pull request, #3020, to work on those changes. Once the pull request is ready, I'll request review from you."
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#3020](https://github.com/microsoft/TypeScript-go/pull/3020) (Closed, **DanielRosenwasser**, **Copilot**)

**Add regression test for incomplete \`export =\` document symbol crash**

*Add a regression test to ensure textDocument/documentSymbol handles incomplete export = without crashing and reports valid selection ranges*

 * created by **Copilot**
 * (yesterday) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * (today) **DanielRosenwasser** closed the issue

### [Issue microsoft/TypeScript-go#3023](https://github.com/microsoft/TypeScript-go/issues/3023) (Closed)

**tsc needs \`"types": \["node"\]\`, tsgo doesn't**

*tsc requires adding node types to tsconfig to recognize process globals, whereas tsgo doesn’t produce errors.*

 * created by **s-h-a-d-o-w**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3023#issuecomment-4019324969) **ahejlsberg** said "This is an intended change. See https://devblogs.microsoft.com/typescript/announcing-typescript-6-0-rc/#types-now-defaults-to-[]."
 * [today](https://github.com/microsoft/TypeScript-go/issues/3023#issuecomment-4019434495) **s-h-a-d-o-w** said "Oh, thanks!"
 * (today) **s-h-a-d-o-w** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/issues/3023#issuecomment-4019462263) **s-h-a-d-o-w** questioned whether this should also be a todo for tsgo and noted it might already be tracked elsewhere
 * [today](https://github.com/microsoft/TypeScript-go/issues/3023#issuecomment-4021409895) **jakebailey** said "#2688"

### [Issue microsoft/TypeScript-go#3025](https://github.com/microsoft/TypeScript-go/issues/3025) (Open)

**\[ServerErrors\]\[TypeScript\] main vs **

*An Azure Pipeline run on the TypeScript main branch encountered server errors and mixed results across 300 popular GitHub repositories.*

 * created by **typescript-bot**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3025#issuecomment-4020210016) **typescript-bot** reported a panic handling a textDocument/formatting request due to debug failure 'False expression: Token end is child end'
 * [today](https://github.com/microsoft/TypeScript-go/issues/3025#issuecomment-4020210036) **typescript-bot** reported a panic during textDocument/formatting due to a debug failure assertion ‘Token end is child end’
 * [today](https://github.com/microsoft/TypeScript-go/issues/3025#issuecomment-4020210053) **typescript-bot** reported a panic due to invalid memory address or nil pointer dereference during handling of textDocument/implementation request
 * [today](https://github.com/microsoft/TypeScript-go/issues/3025#issuecomment-4020210073) **typescript-bot** reported a panic due to invalid memory address or nil pointer dereference during textDocument/implementation
 * [today](https://github.com/microsoft/TypeScript-go/issues/3025#issuecomment-4020210137) **typescript-bot** reported a panic during textDocument/implementation handling with a stack trace indicating an invalid memory address or nil pointer dereference
 * [today](https://github.com/microsoft/TypeScript-go/issues/3025#issuecomment-4020210171) **typescript-bot** reported a panic in textDocument/implementation due to invalid memory address or nil pointer dereference
 * [today](https://github.com/microsoft/TypeScript-go/issues/3025#issuecomment-4020210196) **typescript-bot** reported a panic during textDocument/implementation with a nil pointer dereference and accompanying stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/3025#issuecomment-4020210214) **typescript-bot** reported a panic during textDocument/implementation handling due to an invalid memory address or nil pointer dereference and included the stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/3025#issuecomment-4020210229) **typescript-bot** reported a panic in textDocument/implementation due to an invalid memory address or nil pointer dereference and provided the stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/3025#issuecomment-4020210249) **typescript-bot** reported a panic handling textDocument/rangeFormatting due to inability to create a token from a reparsed KindTypeLiteral node
 * [today](https://github.com/microsoft/TypeScript-go/issues/3025#issuecomment-4020210267) **typescript-bot** reported a panic handling request textDocument/rangeFormatting and included a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/3025#issuecomment-4020210279) **typescript-bot** reported a panic handling textDocument/rangeFormatting due to inability to create a token from a reparsed node of kind KindTypeLiteral
 * [today](https://github.com/microsoft/TypeScript-go/issues/3025#issuecomment-4020210298) **typescript-bot** reported a panic handling request textDocument/rangeFormatting due to inability to create token from reparsed node of kind KindTypeLiteral
 * [today](https://github.com/microsoft/TypeScript-go/issues/3025#issuecomment-4020210314) **typescript-bot** reported that the TypeScript server connection closed prematurely with undefined
 * [today](https://github.com/microsoft/TypeScript-go/issues/3025#issuecomment-4020210333) **typescript-bot** reported server connection closed prematurely with undefined error and provided logs, affected repo details, and repro steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/3025#issuecomment-4020210345) **typescript-bot** reported that the server connection closed prematurely and provided error details and last requests
 * [today](https://github.com/microsoft/TypeScript-go/issues/3025#issuecomment-4020210365) **typescript-bot** reported server connection closed prematurely and provided affected repo details, raw error text, replay commands, and repro steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/3025#issuecomment-4020210383) **typescript-bot** reported that the server connection closed prematurely with an undefined error for the colinhacks/zod repository
 * [today](https://github.com/microsoft/TypeScript-go/issues/3025#issuecomment-4020210395) **typescript-bot** reported a server connection closing prematurely with undefined and provided affected repos and reproduction steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/3025#issuecomment-4020210407) **typescript-bot** reported a panic handling textDocument/rangeFormatting due to a debug failure

### [Issue microsoft/TypeScript-go#3026](https://github.com/microsoft/TypeScript-go/issues/3026) (Closed, `Domain: Editor`)

**TypeScript Native Preview VS Code extension status bar color is confusing**

*The TypeScript Native Preview VS Code extension shows a yellow status bar for subdirectory projects despite correct tsconfig resolution.*

 * created by **connorshea**
 * **connorshea** added label `Domain: Editor`
 * [today](https://github.com/microsoft/TypeScript-go/issues/3026#issuecomment-4020459388) **connorshea** asked if the status bar always used the warning color even when nothing was wrong
 * [today](https://github.com/microsoft/TypeScript-go/issues/3026#issuecomment-4021355125) **DanielRosenwasser** explained that the warning always appeared when native previews were enabled and mentioned plans to replace it with a new non-warning status item
 * [today](https://github.com/microsoft/TypeScript-go/issues/3026#issuecomment-4021367208) **connorshea** recommended using the beaker icon for experimental status and suggested moving it into the language status with a changed background after assuming it was broken

### [Issue microsoft/TypeScript-go#3027](https://github.com/microsoft/TypeScript-go/issues/3027) (Open)

**New TS2883 "\.\.\. cannot be named \.\.\." error exporting an arrow function\.**

*Arrow-exported functions with CSSProperties['cursor'] return types trigger TS2883 in TS 7.0 preview due to unnamed csstype dependencies, unlike function declarations.*

 * created by **simonbuchan**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3027#issuecomment-4020873172) **simonbuchan** highlighted another styled-components variant that may be harder to workaround and noted uncertainty about its TypeScript behavior
 * [today](https://github.com/microsoft/TypeScript-go/issues/3027#issuecomment-4020989945) **hkleungai** noted a potential duplicate of issues #2911 and #2504 and expressed hope for more attention from the TypeScript team
 * [today](https://github.com/microsoft/TypeScript-go/issues/3027#issuecomment-4021083531) **simonbuchan** said "Those are TS4023 and TS4053 so they are at least hitting a different code path, but there does seem to be some relation."

### [PR microsoft/TypeScript-go#3028](https://github.com/microsoft/TypeScript-go/pull/3028) (Closed)

**fix: pass Config to EmitInput in watch mode to prevent nil panic**

*Ensure Config is passed to EmitInput in watch mode to prevent nil pointer panics.*

 * created by **SibtainOcn**

### [PR microsoft/TypeScript-go#3029](https://github.com/microsoft/TypeScript-go/pull/3029) (Closed)

**Add missing \`declarations\` property for \`VariableDeclarationList\` in IPC API**

*Include the missing declarations property in the IPC API definition for VariableDeclarationList to ensure complete interface support.*

 * created by **auvred**

### [PR microsoft/TypeScript-go#3030](https://github.com/microsoft/TypeScript-go/pull/3030) (Closed)

**docs: correct setting key for Tsgo in README**

*Correct the Tsgo setting key in the README documentation.*

 * created by **9romise**
 * [later](https://github.com/microsoft/TypeScript-go/pull/3030#issuecomment-4022323674) **9romise** said "@microsoft-github-policy-service agree"

### [PR microsoft/TypeScript-go#3031](https://github.com/microsoft/TypeScript-go/pull/3031) (Closed, `dependencies`, `github_actions`)

**Bump the github\-actions group across 1 directory with 2 updates**

*Upgrade GitHub Actions in the root directory by bumping actions/setup-node to v6.3.0 and updating github/codeql-action.*

 * created by **dependabot[bot]**
 * (later) **dependabot[bot]** added labels `dependencies`, `github_actions`, `dependencies`, `github_actions`

### [Issue microsoft/TypeScript-go#3032](https://github.com/microsoft/TypeScript-go/issues/3032) (Closed, `Domain: Editor`, `Needs More Info`)

**tsgo \-\-lsp memory leak on large projects / triggers OOM**

*The tsgo LSP process in the TypeScript Native Preview extension leaks memory when handling large projects, causing OOM on low-RAM Linux machines.*

 * created by **huseeiin**
 * **huseeiin** added label `Domain: Editor`

