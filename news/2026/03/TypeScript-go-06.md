# Report for 2026-03-06 (Friday, March 6th, 2026)

10 different users commented on 28 different issues.

## Recommended Actions

 * Response Recommended
    * @caomingpei reported high memory usage and suggested adding resource limits in [microsoft/TypeScript-go#2125](https://github.com/microsoft/TypeScript-go/issues/2125#issuecomment-4012842570)
    * @SibtainOcn provided a proposed fix with PR #2857 in [microsoft/TypeScript-go#2857](https://github.com/microsoft/TypeScript-go/issues/2857#issuecomment-4016355936)

## Activity Summary

### [PR microsoft/TypeScript-go#1550](https://github.com/microsoft/TypeScript-go/pull/1550) (Open)

**Reduce string copies and allocations when emitting inlined sourcemaps**

*Optimize the emission of inlined sourcemaps by minimizing string copying and memory allocations.*

 * created by **dzbarsky**
 * [29 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1550#issuecomment-3172290822) **dzbarsky** said "@microsoft-github-policy-service agre"
 * [29 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1550#issuecomment-3172291031) **dzbarsky** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript-go/pull/1550#issuecomment-4013304463) **jakebailey** clarified that the PR already used string concatenation for the sourceMappingURL in the WriteComment call

### [PR microsoft/TypeScript-go#1551](https://github.com/microsoft/TypeScript-go/pull/1551) (Closed)

**Avoid copying content when writing files**

*Update WriteFile to accept byte slices directly and avoid mutating or copying input data.*

 * created by **dzbarsky**
 * [29 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1551#issuecomment-3172320838) **jakebailey** noted that refactoring file writing to use []byte would be a lot of changes and asked to see benchmarks for the PR
 * [13 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1551#issuecomment-3605003415) **jakebailey** said "@dzbarsky Did you have benchmarks for this, by chance? Not against the change, but I want any use of unsafe to be well-justified."
 * [today](https://github.com/microsoft/TypeScript-go/pull/1551#issuecomment-4013693140) **jakebailey** said "It turns out that we can just use a different signature. I then did more reading and decided to go futher: #3008"
 * (today) **jakebailey** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/1551#issuecomment-4013738467) **dzbarsky** said "Cool, thanks!"

### [Issue microsoft/TypeScript-go#2125](https://github.com/microsoft/TypeScript-go/issues/2125) (Open)

**Unbounded memory consumption with recursive conditional types causes compilation OOM**

*Recursive conditional types on large numeric and string unions lead the TypeScript compiler to run out of memory and crash.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2125#issuecomment-4010014443) **caomingpei** explained that recursive type expansion led to unbounded growth and compared behavior of tsc and ts-go, linking to related issues
 * [today](https://github.com/microsoft/TypeScript-go/issues/2125#issuecomment-4011388398) **dougludlow** suggested adding an upper memory usage limit to terminate the tsgo process when it grows unbounded, reporting that it used 20–30+ GB and caused daily unresponsiveness
 * [today](https://github.com/microsoft/TypeScript-go/issues/2125#issuecomment-4011601474) **jakebailey** said "Editor growth is probably unrelated, and if you have a repro that would be very appreciated in a new issue."
 * [today](https://github.com/microsoft/TypeScript-go/issues/2125#issuecomment-4012842570) **caomingpei** noted that the tsgo process triggered by VS Code consumed 20–30+ GB of memory causing unresponsiveness, suggested constraining editor/plugin integrations with explicit resource limits or startup parameters, and highlighted a difference between tsc and ts-go default behaviors

### [PR microsoft/TypeScript-go#2419](https://github.com/microsoft/TypeScript-go/pull/2419) (Open)

**Fix: Handle Negative VLQ Offsets in Source Maps for VSCode Jump to Definition**

*Clamp inverted ranges caused by negative VLQ offsets in source maps to restore correct VSCode jump to definition behavior.*

 * [10 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2419#issuecomment-3684054114) **sethconvex** agreed company affiliation as Convex, Inc.
 * [9 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2419#issuecomment-3695863591) **sethconvex** asked if there was a path to getting this into main and for instructions on adding spec behavior fixes to the roadmap
 * [8 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2419#issuecomment-3720619871) **jakebailey** said "We were all on vacation 🙂 "
 * [today](https://github.com/microsoft/TypeScript-go/pull/2419#issuecomment-4014752158) **jakebailey** said "This PR needs to be updated after #3005 fixed a bug in this same code. @sethconvex are you willing to do it, or should I push to your PR?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2419#issuecomment-4014846681) **sethconvex** mentioned that he would take a look next week

### [PR microsoft/TypeScript-go#2524](https://github.com/microsoft/TypeScript-go/pull/2524) (Closed)

**feat: detect deprecated via JSDoc and flag deprecated property access**

*Add deprecation detection to Go checker by using JSDoc tags to flag deprecated property access.*

 * created by **AyomiCoder**
 * [7 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2524#issuecomment-3760735963) **AyomiCoder** said "I accept"
 * [7 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2524#issuecomment-3760746607) **AyomiCoder** said "@microsoft-github-policy-service agree"
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2857](https://github.com/microsoft/TypeScript-go/issues/2857) (Open, `Domain: Editor`)

**Formatters get stuck**

*The extension’s LSP-based formatter intermittently hangs during format-on-save on MacOS, never returning a response.*

 * created by **mjbvz**
 * **mjbvz** added label `Domain: Editor`
 * [later](https://github.com/microsoft/TypeScript-go/issues/2857#issuecomment-4016355936) **SibtainOcn** investigated lock contention in snapshotUpdateMu causing dispatch loop stalls and proposed moving GetLanguageService into an async goroutine with PR #2857
 * [later](https://github.com/microsoft/TypeScript-go/issues/2857#issuecomment-4016378111) **jakebailey** said "That suggestion would just re-break the bugs fixed by #2765..."

### [PR microsoft/TypeScript-go#2926](https://github.com/microsoft/TypeScript-go/pull/2926) (Closed)

**Implement ES decorator transform \(ESNext \-\> ES2022\)**

*Implement ESNext to ES2022 decorator transformation in tsgo to resolve issue #2354 blocking its adoption.*

 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/2926#issuecomment-3993216772) **AlCalzone** said "Cool, let me know when that PR is done and I'll see what I need to change here."
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2926#issuecomment-4007972403) **AlCalzone** fixed two more issues with ES decorators and default export function naming, and updated the submodule to reflect the changes
 * [today](https://github.com/microsoft/TypeScript-go/pull/2926#issuecomment-4010723492) **weswigham** suggested having the esDecorator transformer do nothing when experimentalDecorators is set and noted that class fields transformer options logic could be moved later
 * [today](https://github.com/microsoft/TypeScript-go/pull/2926#issuecomment-4013965759) **jakebailey** suggested using a gist to bulk mark PR diffs as read and offered to perform a one-to-one comparison
 * [today](https://github.com/microsoft/TypeScript-go/pull/2926#issuecomment-4013983533) **AlCalzone** said "Yeah, I'm looking at those right now. 👍🏻"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2926#issuecomment-4014779355) **jakebailey** asked whether @AlCalzone still wanted to finish the work or if they should push fixes instead
 * [today](https://github.com/microsoft/TypeScript-go/pull/2926#issuecomment-4015138380) **jakebailey** said "I think I have fixes for a lot of these, very annoying substitutions "
 * [later](https://github.com/microsoft/TypeScript-go/pull/2926#issuecomment-4016311903) **AlCalzone** offered that others could push changes or take over and asked how to proceed

### [PR microsoft/TypeScript-go#2995](https://github.com/microsoft/TypeScript-go/pull/2995) (Closed)

**Fix call hierarchy crash on anonymous classes/functions**

*Call hierarchy was crashing for anonymous classes or functions and has now been fixed.*

 * created by **Andarist**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3001](https://github.com/microsoft/TypeScript-go/pull/3001) (Closed)

**Implement missing deprecated property check**

*Implements the missing deprecated property check, updates fourslash deprecation tests, and marks two tests manual due to improved signature messages.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3002](https://github.com/microsoft/TypeScript-go/pull/3002) (Closed)

**Finish porting reportMergeSymbolError**

*Finalize the reportMergeSymbolError migration by deleting outdated commented code, keeping IsPlainJSFile checks, and clearing all TODO(TS-TO-GO) comments.*

 * created by **jakebailey**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3002#issuecomment-4009741103) **connorshea** joked that they should close the issue tracker since they did it
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3004](https://github.com/microsoft/TypeScript-go/pull/3004) (Closed)

**Fixed parsing of multiline string JSX attributes with whitespace present after \`=\`**

*The parser now handles multiline JSX string attributes with whitespace after '=' without crashing.*

 * created by **Andarist**
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript-go#3005](https://github.com/microsoft/TypeScript-go/pull/3005) (Closed)

**Allow start and end positions to be in different files in \`getMappedLocation\`**

*Allow getMappedLocation to map start and end positions across separate files to prevent crashes.*

 * created by **Andarist**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3005#issuecomment-4013174533) **jakebailey** said "I think this is the same bug as https://github.com/microsoft/typescript-go/pull/2419"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3005#issuecomment-4013178162) **jakebailey** said "Can you pull that PR's test into this one and see if it now passes?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3005#issuecomment-4013753276) **Andarist** said "@jakebailey it doesn't crash here (but perhaps it didn't before Seth's PR either) - but the baseline result is different. I think both PRs have to be considered separately"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3006](https://github.com/microsoft/TypeScript-go/pull/3006) (Closed)

**Fixed a crash related to a dynamic \`import\(\)\` of an UMD module**

*Fixes a crash that occurred when using dynamic import() to load a UMD module.*

 * created by **Andarist**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3007](https://github.com/microsoft/TypeScript-go/pull/3007) (Closed)

**Speed up iofs file writes, fix BOM**

*Improve iofs file write performance by updating the signature and correcting incorrect BOM output*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3007#issuecomment-4013673082) **jakebailey** said "Actually, I have another change I want to do instead (dropping writeByteOrderMark entirely)"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3008](https://github.com/microsoft/TypeScript-go/pull/3008) (Closed)

**Speed up iofs file writes, remove writeByteOrderMark entirely**

*Remove the writeByteOrderMark option and improve iofs file write performance by prepending the BOM during the emit phase.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3009](https://github.com/microsoft/TypeScript-go/pull/3009) (Closed)

**Remove some unused / noop emit flags**

*Remove unused or no-op compiler emit flags rendered redundant by dropping ES5 support and restructuring imports*

 * created by **jakebailey**

### [Issue microsoft/TypeScript-go#3010](https://github.com/microsoft/TypeScript-go/issues/3010) (Open, `Domain: Editor`, `Crash`, **DanielRosenwasser**)

**nil pointer dereference for contextual constraint completions in JSDoc**

*A nil pointer dereference occurs during constraint-based completions in JSDoc-annotated JavaScript files in the TypeScript language service.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** added labels `Domain: Editor`, `Crash`, and assigned to **DanielRosenwasser**

### [PR microsoft/TypeScript-go#3011](https://github.com/microsoft/TypeScript-go/pull/3011) (Open)

**Fix completions for contextually constrained types in JSDoc**

*Ensure completions for contextually constrained JSDoc types correctly handle missing reparsed nodes by falling back to syntax node names.*

 * created by **DanielRosenwasser**

### [Issue microsoft/TypeScript-go#3012](https://github.com/microsoft/TypeScript-go/issues/3012) (Open)

**\[ServerErrors\]\[TypeScript\] main vs **

*The main branch Azure pipeline reported clone failures, timeouts, and server errors during analysis of 300 TypeScript repositories, yielding 53 significant changes.*

 * created by **typescript-bot**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3012#issuecomment-4015172960) **typescript-bot** reported a panic during textDocument/formatting due to a failed debug assertion
 * [today](https://github.com/microsoft/TypeScript-go/issues/3012#issuecomment-4015172984) **typescript-bot** reported a panic handling textDocument/formatting due to a false expression 'Token end is child end'
 * [today](https://github.com/microsoft/TypeScript-go/issues/3012#issuecomment-4015173008) **typescript-bot** reported a panic when handling a textDocument/formatting request due to a failed debug assertion and provided a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/3012#issuecomment-4015173044) **typescript-bot** reported a panic during textDocument/formatting due to a debug failure assertion “Token end is child end” and provided a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/3012#issuecomment-4015173075) **typescript-bot** reported a panic during textDocument/formatting due to a debug failure (False expression: Token end is child end)
 * [today](https://github.com/microsoft/TypeScript-go/issues/3012#issuecomment-4015173103) **typescript-bot** reported a panic in textDocument/formatting with debug failure 'False expression: Token end is child end'
 * [today](https://github.com/microsoft/TypeScript-go/issues/3012#issuecomment-4015173118) **typescript-bot** reported a panic in textDocument/formatting due to a debug failure and included a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/3012#issuecomment-4015173143) **typescript-bot** reported a panic handling textDocument/formatting request due to a debug failure 'False expression: Token end is child end'
 * [today](https://github.com/microsoft/TypeScript-go/issues/3012#issuecomment-4015173160) **typescript-bot** reported a panic in textDocument/formatting due to a failed debug assertion 'Token end is child end' and provided a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/3012#issuecomment-4015173183) **typescript-bot** reported a panic on textDocument/formatting due to a debug failure with stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/3012#issuecomment-4015173219) **typescript-bot** reported a panic with a debug failure during document formatting
 * [today](https://github.com/microsoft/TypeScript-go/issues/3012#issuecomment-4015173235) **typescript-bot** reported a panic during textDocument/formatting due to a debug failure "False expression: Token end is child end" with accompanying stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/3012#issuecomment-4015173248) **typescript-bot** reported a panic handling textDocument/formatting with debug failure: False expression: Token end is child end
 * [today](https://github.com/microsoft/TypeScript-go/issues/3012#issuecomment-4015173273) **typescript-bot** reported a panic in textDocument/formatting due to Debug failure: False expression: Token end is child end
 * [today](https://github.com/microsoft/TypeScript-go/issues/3012#issuecomment-4015173297) **typescript-bot** reported a panic during textDocument/formatting due to a debug failure "Token end is child end" with an accompanying stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/3012#issuecomment-4015173313) **typescript-bot** reported a runtime panic in textDocument/implementation due to invalid memory address or nil pointer dereference
 * [today](https://github.com/microsoft/TypeScript-go/issues/3012#issuecomment-4015173326) **typescript-bot** reported a panic handling textDocument/implementation due to invalid memory address or nil pointer dereference
 * [today](https://github.com/microsoft/TypeScript-go/issues/3012#issuecomment-4015173344) **typescript-bot** reported a panic during handling of a textDocument/implementation request
 * [today](https://github.com/microsoft/TypeScript-go/issues/3012#issuecomment-4015173363) **typescript-bot** reported a panic in textDocument/implementation caused by an invalid memory address or nil pointer dereference
 * [today](https://github.com/microsoft/TypeScript-go/issues/3012#issuecomment-4015173386) **typescript-bot** reported a panic during textDocument/implementation due to invalid memory address or nil pointer dereference
 * [today](https://github.com/microsoft/TypeScript-go/issues/3012#issuecomment-4015173406) **typescript-bot** reported a panic due to nil pointer dereference during cross-project handling of textDocument/implementation
 * [today](https://github.com/microsoft/TypeScript-go/issues/3012#issuecomment-4015173428) **typescript-bot** reported a panic handling request textDocument/rangeFormatting with a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/3012#issuecomment-4015173447) **typescript-bot** reported a panic in textDocument/rangeFormatting due to inability to create token from reparsed node of kind KindTypeLiteral
 * [today](https://github.com/microsoft/TypeScript-go/issues/3012#issuecomment-4015173459) **typescript-bot** reported a panic handling textDocument/rangeFormatting request due to inability to create a token from a reparsed node of kind KindTypeLiteral and provided a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/3012#issuecomment-4015173482) **typescript-bot** reported a panic and stack trace during a textDocument/formatting request
 * [today](https://github.com/microsoft/TypeScript-go/issues/3012#issuecomment-4015173494) **typescript-bot** reported panic handling textDocument/formatting request with debug failure and included stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/3012#issuecomment-4015173511) **typescript-bot** reported a panic handling textDocument/formatting due to a debug failure: false expression 'Token end is child end'
 * [today](https://github.com/microsoft/TypeScript-go/issues/3012#issuecomment-4015173532) **typescript-bot** reported a server connection closed prematurely with undefined and provided affected repos, error artifacts, recent requests, and repro steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/3012#issuecomment-4015173555) **typescript-bot** reported a premature server connection closure error and included affected repository details, request logs, and reproduction steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/3012#issuecomment-4015173576) **typescript-bot** reported a premature server connection closure and provided error details, artifact links, request logs, and repro steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/3012#issuecomment-4015173600) **typescript-bot** reported the server connection closed prematurely
 * [today](https://github.com/microsoft/TypeScript-go/issues/3012#issuecomment-4015173627) **typescript-bot** reported that the server connection closed prematurely for socketio/socket.io and provided logs, recent requests, and repro steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/3012#issuecomment-4015173650) **typescript-bot** reported a panic during textDocument/formatting due to a debug failure: False expression: Token end is child end
 * [today](https://github.com/microsoft/TypeScript-go/issues/3012#issuecomment-4015173670) **typescript-bot** reported a panic during textDocument/formatting with Debug failure: False expression: Token end is child end and included a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/3012#issuecomment-4015173688) **typescript-bot** reported a panic during textDocument/formatting due to debug failure 'Token end is child end'
 * [today](https://github.com/microsoft/TypeScript-go/issues/3012#issuecomment-4015173710) **typescript-bot** reported a panic during textDocument/formatting due to debug failure 'False expression: Token end is child end'
 * [today](https://github.com/microsoft/TypeScript-go/issues/3012#issuecomment-4015173736) **typescript-bot** reported a panic handling a textDocument/formatting request with debug failure 'False expression: Token end is child end' and provided a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/3012#issuecomment-4015173761) **typescript-bot** reported a panic during textDocument/formatting with a debug failure and stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/3012#issuecomment-4015173777) **typescript-bot** reported a panic during textDocument/formatting due to a debug failure: False expression: Token end is child end
 * [today](https://github.com/microsoft/TypeScript-go/issues/3012#issuecomment-4015173799) **typescript-bot** reported a panic handling textDocument/formatting request due to a debug failure: Token end is child end
 * [today](https://github.com/microsoft/TypeScript-go/issues/3012#issuecomment-4015173817) **typescript-bot** reported a panic in textDocument/formatting due to a false expression 'Token end is child end' with a stack trace

### [PR microsoft/TypeScript-go#3013](https://github.com/microsoft/TypeScript-go/pull/3013) (Closed)

**Report errors on unsupported CJS constructs in declaration emit**

*Generate errors during declaration file emission for multiple or nested CommonJS exports and defineProperty calls.*

 * created by **ahejlsberg**
 * [later](https://github.com/microsoft/TypeScript-go/pull/3013#issuecomment-4016612558) **ahejlsberg** explained that the only change in the symbol tracker was the addition of two error reporting methods, serving as the conduit for error reporting in the declaration transformer

### [Issue microsoft/TypeScript-go#3014](https://github.com/microsoft/TypeScript-go/issues/3014) (Open)

**\`tsgo \-\-watch\` hangs if given a tsconfig\.json with no files**

*tsgo --watch hangs indefinitely when run on a tsconfig.json configuration that specifies no files*

 * created by **DanielRosenwasser**

### [Issue microsoft/TypeScript-go#3015](https://github.com/microsoft/TypeScript-go/issues/3015) (Open, `Crash`)

**panic on \`\-\-watch\` and \`\-\-explainFiles\`**

*Using tsgo with --watch and --explainFiles flags triggers a nil pointer dereference panic.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** added labels `Crash`, `Crash`

### [PR microsoft/TypeScript-go#3016](https://github.com/microsoft/TypeScript-go/pull/3016) (Closed)

**fix: move GetLanguageService to async closure to prevent dispatch loop blocking**

*Relocate GetLanguageService invocation into an asynchronous closure to prevent dispatch loop blocking.*

 * created by **SibtainOcn**
 * [later](https://github.com/microsoft/TypeScript-go/pull/3016#issuecomment-4016380598) **jakebailey** said "Does this not just undo #2765?"

### [PR microsoft/TypeScript-go#3017](https://github.com/microsoft/TypeScript-go/pull/3017) (Closed)

**Fixed a rescanning crash related to \`JsxNamespacedName\` with dashes**

*A crash occurring during rescanning of JSX namespaced names with dashes has been resolved.*

 * created by **Andarist**

