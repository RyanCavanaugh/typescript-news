# Report for 2026-03-01 (Sunday, March 1st, 2026)

12 different users commented on 19 different issues.

## Recommended Actions

 * Response Recommended
    * @zurmokeeper asked when the issue would be resolved in [microsoft/TypeScript-go#2692](https://github.com/microsoft/TypeScript-go/issues/2692#issuecomment-3981831054)
    * @GGomez99 reported the issue was resolved by disabling the extension and opened a ticket in [microsoft/TypeScript-go#2910](https://github.com/microsoft/TypeScript-go/issues/2910#issuecomment-3983406859)

## Activity Summary

### [Issue microsoft/TypeScript-go#2360](https://github.com/microsoft/TypeScript-go/issues/2360) (Closed, `wontfix`, `Domain: Editor`)

**Setting useTsgo=true with the plugin disabled will prevent you from jumping to the type definition in Cursor**

*Enabling typescript.experimental.useTsgo with the TypeScript Native Preview plugin disabled prevents jumping to type definitions.*

 * (11 weeks ago) **RyanCavanaugh** closed the issue
 * [7 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2360#issuecomment-3731121124) **pouyarezvani** questioned the meaning of the previous comment and noted that enabling useTsgo broke go-to definitions
 * [7 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2360#issuecomment-3731172796) **RyanCavanaugh** said "You can't turn on the "use the tsgo plugin" setting while also disabling the tsgo plugin and expect that to work"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2360#issuecomment-3982426644) **wygkzqa** clarified that toggling the tsgo plugin was a user choice rather than a conflict

### [Issue microsoft/TypeScript-go#2612](https://github.com/microsoft/TypeScript-go/issues/2612) (Closed, `Crash`)

**tsgo crashes**

*tsgo crashes with a stack trace when running deno check on ignore_test.ts with DENO_UNSTABLE_TSGO enabled in Deno 2.6.6.*

 * [1 month ago](https://github.com/microsoft/TypeScript-go/issues/2612#issuecomment-3830412825) **amyssnippet** ran the provided commands and reported that they still did not encounter the error
 * [1 month ago](https://github.com/microsoft/TypeScript-go/issues/2612#issuecomment-3830419234) **sigmaSd** diagnosed caching prevented deno check from running and suggested editing the file or running "deno clean"
 * [1 month ago](https://github.com/microsoft/TypeScript-go/issues/2612#issuecomment-3830432114) **amyssnippet** asked if they should start working on the reported fatal error after a concurrent map read and write panic
 * [later](https://github.com/microsoft/TypeScript-go/issues/2612#issuecomment-3983145813) **sigmaSd** said "https://github.com/denoland/deno/issues/32259#issuecomment-3983132678"
 * (later) **sigmaSd** closed the issue

### [Issue microsoft/TypeScript-go#2692](https://github.com/microsoft/TypeScript-go/issues/2692) (Closed, **jakebailey**, **Copilot**)

**tsgo does not respect \`esModuleInterop\` in certain cases**

*tsgo ignores the esModuleInterop setting when importing named exports from CommonJS JavaScript files with allowJs enabled, causing TS2497 errors.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2692#issuecomment-3854498259) **jakebailey** said "Feels like https://github.com/microsoft/typescript-go/issues/1054, potentially "
 * (3 weeks ago) **jakebailey** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2692#issuecomment-3981831054) **zurmokeeper** said "@jakebailey When might this issue be resolved? It's been quite some time now. For TypeScript code referencing common.js, TypeScript 7's type checking fails outright, rendering it completely unusable."

### [PR microsoft/TypeScript-go#2874](https://github.com/microsoft/TypeScript-go/pull/2874) (Closed, `dependencies`, `github_actions`)

**Bump github/codeql\-action from 4\.32\.3 to 4\.32\.4 in the github\-actions group across 1 directory**

*Bump github/codeql-action from 4.32.3 to 4.32.4 to update the default CodeQL bundle and enhance proxy certificate handling and diagnostics.*

 * (6 days ago) **dependabot[bot]** added labels `github_actions`, `dependencies`, `github_actions`
 * [later](https://github.com/microsoft/TypeScript-go/pull/2874#issuecomment-3983798399) **dependabot[bot]** said "Looks like github/codeql-action is updatable in another way, so this is no longer needed."
 * (later) **dependabot[bot]** closed the issue

### [PR microsoft/TypeScript-go#2893](https://github.com/microsoft/TypeScript-go/pull/2893) (Closed)

**Improve CommonJS support**

*Enhance Corsa’s CommonJS support by allowing multiple module.exports assignments, supporting JSDoc typedef imports, and aligning export behavior with Strada.*

 * created by **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2893#issuecomment-3981382205) **ahejlsberg** said "Closing in favor of #2946."
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#2910](https://github.com/microsoft/TypeScript-go/issues/2910) (Closed, `Domain: Editor`)

**Abnormal RAM/swap and CPU usage**

*Enabling the experimental tsgo TypeScript server in VSCode consumes excessive CPU and RAM/swap, making macOS sluggish.*

 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/2910#issuecomment-3972146716) **andzdroid** reported issue persisted across versions when running tsgo --watch idle after initial build
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/2910#issuecomment-3973086152) **GGomez99** reproduced excessive memory and CPU usage in the TypeScript-Go LSP, provided reproduction steps, attempted fixes, and a heap profile, and asked if cached data/config might be triggering the issue
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/2910#issuecomment-3975829460) **JoostK** reported high memory and CPU usage by the TypeScript LSP with repro steps, heap profile, and attempted fixes, and asked if cached data or another extension could be causing the issue
 * [later](https://github.com/microsoft/TypeScript-go/issues/2910#issuecomment-3983406859) **GGomez99** thanked the suggestion, disabled the turbo-console-log extension, confirmed the issue was resolved, and opened a ticket on that extension's repository
 * (later) **Spookywy** closed the issue

### [PR microsoft/TypeScript-go#2933](https://github.com/microsoft/TypeScript-go/pull/2933) (Closed)

**Fix deadlock in LSPClient**

*Formatting tests for LSPClient are hanging indefinitely because NewLSPClient’s goroutines deadlock on a WaitGroup.*

 * created by **gabritto**
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/2933#issuecomment-3975090670) **jakebailey** asked why cancellation was not exiting the writeLoop select loop
 * [today](https://github.com/microsoft/TypeScript-go/pull/2933#issuecomment-3981496116) **gabritto** asked why cancellation did not exit the writeLoop and suggested it was blocking on writing to the buffered channel
 * (today) **gabritto** closed the issue

### [Issue microsoft/TypeScript-go#2942](https://github.com/microsoft/TypeScript-go/issues/2942) (Closed, `Crash`)

**tsgo \-\-api: DocumentIdentifier JSON unmarshaling panics**

*tsgo’s API panics when trying to unmarshal a DocumentIdentifier from JSON due to an invalid jsontext.Token*

 * created by **ajmacd**
 * **ajmacd** added label `Crash`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2942#issuecomment-3980818345) **ajmacd** said "Looks like this should fix it: https://github.com/microsoft/typescript-go/pull/2943"

### [PR microsoft/TypeScript-go#2943](https://github.com/microsoft/TypeScript-go/pull/2943) (Closed)

**fix\(api\): DocumentIdentifier JSON unmarshaling panic**

*Save JSON object keys before reading values and handle "fileName" to fix DocumentIdentifier unmarshal panic.*

 * created by **ajmacd**

### [PR microsoft/TypeScript-go#2944](https://github.com/microsoft/TypeScript-go/pull/2944) (Open)

**\[draft\] more formatting tests **

*Add draft formatting tests to validate and troubleshoot the repository’s testing pipelines.*

 * created by **iisaduan**

### [Issue microsoft/TypeScript-go#2945](https://github.com/microsoft/TypeScript-go/issues/2945) (Closed, `Domain: Editor`)

**\[ServerErrors\]\[TypeScript\] linux\-x64\-7\.0\.0\-dev\.20260301\.1 vs **

*Automated linux-x64-7.0.0-dev.20260301.1 build on 300 popular TypeScript repositories reported errors, timeouts, and clone failures.*

 * created by **typescript-bot**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2945#issuecomment-3981326336) **typescript-bot** reported a panic handling textDocument/definition due to an unhandled case in getDiagnosticHeadMessageForDecoratorResolution
 * [today](https://github.com/microsoft/TypeScript-go/issues/2945#issuecomment-3981326357) **typescript-bot** reported panic handling textDocument/definition due to an unhandled case in getDiagnosticHeadMessageForDecoratorResolution
 * [today](https://github.com/microsoft/TypeScript-go/issues/2945#issuecomment-3981326377) **typescript-bot** reported a panic during textDocument/definition handling due to an unhandled case in getDiagnosticHeadMessageForDecoratorResolution
 * [today](https://github.com/microsoft/TypeScript-go/issues/2945#issuecomment-3981326401) **typescript-bot** reported a panic in textDocument/implementation due to an invalid memory address or nil pointer dereference
 * [today](https://github.com/microsoft/TypeScript-go/issues/2945#issuecomment-3981326421) **typescript-bot** reported a panic during textDocument/implementation due to an invalid memory address or nil pointer dereference
 * [today](https://github.com/microsoft/TypeScript-go/issues/2945#issuecomment-3981326436) **typescript-bot** reported a panic during textDocument/implementation request due to invalid memory address or nil pointer dereference
 * [today](https://github.com/microsoft/TypeScript-go/issues/2945#issuecomment-3981326460) **typescript-bot** reported a panic due to invalid memory address or nil pointer dereference during cross-project handling of textDocument/implementation
 * [today](https://github.com/microsoft/TypeScript-go/issues/2945#issuecomment-3981326479) **typescript-bot** reported a panic due to an invalid memory address or nil pointer dereference in textDocument/implementation with a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/2945#issuecomment-3981326498) **typescript-bot** reported a panic during cross-project handling for textDocument/implementation
 * [today](https://github.com/microsoft/TypeScript-go/issues/2945#issuecomment-3981326510) **typescript-bot** reported a panic with an invalid memory address or nil pointer dereference during cross-project textDocument/implementation handling
 * [today](https://github.com/microsoft/TypeScript-go/issues/2945#issuecomment-3981326527) **typescript-bot** reported a runtime panic in textDocument/formatting due to slice bounds out of range
 * [today](https://github.com/microsoft/TypeScript-go/issues/2945#issuecomment-3981326555) **typescript-bot** reported a panic during request handling for textDocument/implementation caused by a slice bounds out of range error
 * [today](https://github.com/microsoft/TypeScript-go/issues/2945#issuecomment-3981326571) **typescript-bot** reported a runtime panic during textDocument/formatting due to slice bounds out of range
 * [today](https://github.com/microsoft/TypeScript-go/issues/2945#issuecomment-3981326595) **typescript-bot** reported panic handling request textDocument/formatting due to runtime error: slice bounds out of range
 * [today](https://github.com/microsoft/TypeScript-go/issues/2945#issuecomment-3981326614) **typescript-bot** reported server connection closed prematurely error and provided reproduction steps and artifact details for t4t5/sweetalert
 * [today](https://github.com/microsoft/TypeScript-go/issues/2945#issuecomment-3981326637) **typescript-bot** reported a server connection closing prematurely and provided affected repos and repro steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/2945#issuecomment-3981326660) **typescript-bot** reported a server connection closed prematurely error with undefined, listed affected repo, last requests, and repro steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/2945#issuecomment-3981326680) **typescript-bot** reported that the server connection closed prematurely with an undefined error and listed affected repos and recent requests
 * [today](https://github.com/microsoft/TypeScript-go/issues/2945#issuecomment-3981326706) **typescript-bot** reported server connection closed prematurely and provided error details, affected repository links, recent requests, and repro steps

### [PR microsoft/TypeScript-go#2946](https://github.com/microsoft/TypeScript-go/pull/2946) (Closed)

**Improve CommonJS support, round 2**

*Enable overlaying of type and namespace declarations on CommonJS export assignments, allow multiple module.exports unions, and align Corsa with Strada behavior*

 * created by **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2946#issuecomment-3981689855) **ahejlsberg** mentioned an existing issue with declaration file generation for CommonJS modules with module.exports assignments, noted that the initial bug was fixed, and highlighted that multiple and nested module.exports assignments remain unhandled

### [PR microsoft/TypeScript-go#2947](https://github.com/microsoft/TypeScript-go/pull/2947) (Closed, `dependencies`, `github_actions`)

**Bump the github\-actions group across 1 directory with 2 updates**

*Bump the github-actions group in the repository root by upgrading actions/upload-artifact to v7.0.0 and updating github/codeql-action.*

 * created by **dependabot[bot]**
 * (later) **dependabot[bot]** added labels `dependencies`, `github_actions`, `dependencies`, `github_actions`

### [PR microsoft/TypeScript-go#2948](https://github.com/microsoft/TypeScript-go/pull/2948) (Closed)

**Don't re\-do \`merge\_group\` work on \`push: main\`**

*Avoid re-running merge_group work on pushes to the main branch.*

 * created by **Andarist**
 * [later](https://github.com/microsoft/TypeScript-go/pull/2948#issuecomment-3985152514) **jakebailey** noted that jobs differ between PRs, merge queues, and pushes to main, pointed out that the change would cease macOS testing, and asked what motivated it

### [PR microsoft/TypeScript-go#2949](https://github.com/microsoft/TypeScript-go/pull/2949) (Closed)

**Fix formatting panic when first line is all whitespace**

*Formatting in TypeScript-Go panics if the first line contains only whitespace.*

 * created by **Andarist**

### [PR microsoft/TypeScript-go#2950](https://github.com/microsoft/TypeScript-go/pull/2950) (Closed)

**Fix formatting crash on files with tab indentation near end of file**

*Fix formatting crash triggered by files that end with tab-based indentation.*

 * created by **Andarist**

