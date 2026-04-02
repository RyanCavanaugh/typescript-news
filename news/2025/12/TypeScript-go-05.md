# Report for 2025-12-05 (Friday, December 5th, 2025)

14 different users commented on 28 different issues.

## Activity Summary

### [Issue microsoft/TypeScript-go#1465](https://github.com/microsoft/TypeScript-go/issues/1465) (Closed, `Crash`, `Domain: Program`, **sheetalkamat**)

**Intermittent crash with \-\-incremental**

*tsgo intermittently crashes when run with --incremental on large projects in frequent CI pipelines*

 * [12 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1465#issuecomment-3272538693) **paperclover** reported that after rebasing onto master, tsgo now consistently triggered a stack overflow and provided the commit range that caused it
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/1465#issuecomment-3572146695) **sheetalkamat** said "Can you please use nightly and see if this is fixed. "
 * [today](https://github.com/microsoft/TypeScript-go/issues/1465#issuecomment-3615895910) **justinsmid** described encountering the issue consistently on a specific branch after switching to tsgo, provided reproduction steps, and noted that disabling incremental or changing the @typescript/native-preview version worked around it
 * [today](https://github.com/microsoft/TypeScript-go/issues/1465#issuecomment-3617919357) **sheetalkamat** said "I think #2051 and #2070 would have fixed this. So if this repros again, please file new issue with repro steps. "
 * (today) **sheetalkamat** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/issues/1465#issuecomment-3617924178) **jakebailey** said "The above user was testing yesterdays build, but I will extract that to a new issue"

### [PR microsoft/TypeScript-go#2049](https://github.com/microsoft/TypeScript-go/pull/2049) (Closed)

**Update vscode\-languageclient to v10**

*Updating the vscode-languageclient to v10 fixes client bugs but moves logging to stderr and hides LSP logs by default.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2049#issuecomment-3617844395) **jakebailey** suggested implementing a custom LogOutputChannel but found it incompatible with log level/event emitter and decided to acquiesce
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2218](https://github.com/microsoft/TypeScript-go/issues/2218) (Closed, `Domain: Type Checking`, `Crash`, **ahejlsberg**, **Copilot**)

**Panic on initial attempt of existing JavaScript \+ JSDoc project**

*typescript-go crashes with a nil pointer dereference panic when processing an existing JavaScript and JSDoc project.*

 * **jakebailey** assigned to **Copilot**
 * (today) **ahejlsberg** added label `Domain: Type Checking`, and assigned to **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2218#issuecomment-3617748744) **jakebailey** mentioned dumping method overloads into the source file for object methods and questioned whether TypeScript legally supports that syntax
 * [today](https://github.com/microsoft/TypeScript-go/issues/2218#issuecomment-3617788907) **sandersn** said "I am against hacks. It should be added as a TS language feature in 7.1 if it's important enough of a feature, and then the jsdoc reparsing can be fixed up as needed then for it to work in JS."

### [PR microsoft/TypeScript-go#2221](https://github.com/microsoft/TypeScript-go/pull/2221) (Closed, **jakebailey**, **Copilot**)

**Fix panic by restricting @overload to legal contexts in JSDoc**

*Restrict JSDoc @overload to function, class, and interface methods to prevent AST panics and report errors for invalid contexts.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2221#issuecomment-3613801808) **jakebailey** noted that the fix was just a band-aid and suggested that the reparser's overload handling was causing an incorrect AST node hierarchy
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2221#issuecomment-3613902307) **Copilot** stated that the reparser was incorrectly creating synthetic MethodDeclaration nodes for @overload tags and fixed it in commit 7d45569 by keeping overload information in the JSDoc structure
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2221#issuecomment-3613919781) **jakebailey** questioned whether overloads on object literal methods are allowed in TypeScript and if they should be banned in JS
 * [today](https://github.com/microsoft/TypeScript-go/pull/2221#issuecomment-3617808745) **jakebailey** suggested changing the reparser to ban @overload in contexts where TypeScript disallows overloads
 * [today](https://github.com/microsoft/TypeScript-go/pull/2221#issuecomment-3617909725) **Copilot** reported that the fix was applied in commit cf45e9c, restricting @overload to function declarations and class/interface methods, ignoring object literal methods, and restoring function overload baselines
 * [today](https://github.com/microsoft/TypeScript-go/pull/2221#issuecomment-3617930092) **jakebailey** said "@copilot This should not be a silent error. We have a mechanism to issue JSDoc errors in parsing; use that."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2221#issuecomment-3618123001) **Copilot** described the fix that now reports error TS8110 for @overload on object literal methods using the PCObjectLiteralMembers parsing context

### [Issue microsoft/TypeScript-go#2228](https://github.com/microsoft/TypeScript-go/issues/2228) (Open, `Domain: Editor`, **gabritto**)

**No JS Doc template completions**

*The ts-go extension lacks support for the JSDoc template completion feature introduced in TypeScript 6.0 for VSCode.*

 * created by **mjbvz**
 * **gabritto** assigned to **gabritto**

### [PR microsoft/TypeScript-go#2235](https://github.com/microsoft/TypeScript-go/pull/2235) (Closed)

**Implementations, CodeLens, IncomingCalls across projects**

*Enable CodeLens, Implementations, and IncomingCalls features to work across multiple projects.*

 * created by **sheetalkamat**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2235#issuecomment-3618991016) **sheetalkamat** said "Failure is because of not correctly calling recover to assign request for panic. will take a look . "

### [Issue microsoft/TypeScript-go#2238](https://github.com/microsoft/TypeScript-go/issues/2238) (Open, `Crash`)

**fatal error: concurrent map read and map write**

*A fatal concurrent map read/write panic occurs in the Typescript-Go link store while resolving import aliases.*

 * created by **charlag**
 * **charlag** added label `Crash`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2238#issuecomment-3617676644) **jakebailey** said "It seems like we are still somehow concurrency unsafe through HandleNoEmitOnError. Incremental is still not doing the expected locking."

### [Issue microsoft/TypeScript-go#2239](https://github.com/microsoft/TypeScript-go/issues/2239) (Open, `Needs More Info`)

**take too much memory**

*tsgo extension consumes about 17GB of RAM on macOS M1, causing heavy swapping and slowing VS Code.*

 * created by **maxired**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3617221627) **jakebailey** said "Do you have a repo where this reproduces?"
 * **RyanCavanaugh** added label `Needs More Info`

### [Issue microsoft/TypeScript-go#2241](https://github.com/microsoft/TypeScript-go/issues/2241) (Closed, `Crash`, **gabritto**, **Copilot**)

**Crash when code contains disposer logic\. Request textDocument/inlayHint failed\.**

*The TypeScript Go LSP panics on inlayHint requests for disposer logic code after encountering an unexpected PropertyAccessExpression.*

 * created by **jinliming2**
 * **jinliming2** added label `Crash`
 * **jakebailey** assigned to **Copilot**
 * **gabritto** assigned to **gabritto**

### [PR microsoft/TypeScript-go#2242](https://github.com/microsoft/TypeScript-go/pull/2242) (Closed, **jakebailey**, **Copilot**)

**Fix panic in inlay hints when visiting PropertyAccessExpression nodes**

*Add support for PropertyAccessExpression nodes in inlay hints to prevent panics when handling computed property names like Symbol.dispose.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2242#issuecomment-3618956095) **gabritto** said "BTW this crash doesn't happen in a TS file, only in a JS file, so pretty sure this PR is wrong. Gonna try and fix it myself."
 * (today) **gabritto** closed the issue

### [Issue microsoft/TypeScript-go#2243](https://github.com/microsoft/TypeScript-go/issues/2243) (Open, `Crash`)

**Crash in incremental**

*Tsgo incremental crashes on a specific branch, temporarily fixed by disabling incremental or switching @typescript/native-preview versions.*

 * created by **jakebailey**
 * **jakebailey** added label `Crash`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2243#issuecomment-3617927202) **jakebailey** said "I have access to this repo, but will need to reclone and so on..."

### [Issue microsoft/TypeScript-go#2244](https://github.com/microsoft/TypeScript-go/issues/2244) (Open, `Domain: Editor`)

**Port \`update imports on file rename/move\` support**

*Request to port support for automatically updating imports when files are renamed or relocated*

 * created by **mjbvz**
 * **mjbvz** added label `Crash`
 * **gabritto** removed label `Crash`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2244#issuecomment-3619129053) **mmgeorge** said "Just tried tsgo's ls today and ran into this as well. It's unbelievably faster on our codebase though! Tempted to stick with it for now and just swap ls when I need to do a bunch of file renaming. "

### [Issue microsoft/TypeScript-go#2245](https://github.com/microsoft/TypeScript-go/issues/2245) (Open, `Domain: JS`, `Crash`, **navya9singh**)

**Folding range crash in JS file for \`exports\.property = CallExpression\(ObjectLiteral\)\`**

*The TypeScript Go LSP panics computing folding ranges for an export assignment call expression with an object literal.*

 * created by **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2245#issuecomment-3618910449) **DanielRosenwasser** noted a similar issue using module.exports = {} that caused a token cache mismatch error

### [Issue microsoft/TypeScript-go#2246](https://github.com/microsoft/TypeScript-go/issues/2246) (Open, `node10 resolution`)

**TS2307 with \`@octokit/core\` in tsgo but not tsc**

*tsgo fails to resolve the '@octokit/core/dist-types/types' module causing TS2307, while tsc with TypeScript 5.9 succeeds.*

 * created by **jfirebaugh**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2246#issuecomment-3619020896) **jakebailey** explained that the import succeeded only due to an older deprecated resolution mode and recommended importing `/types` based on the package's export map
 * **jakebailey** added label `node10 resolution`

### [Issue microsoft/TypeScript-go#2247](https://github.com/microsoft/TypeScript-go/issues/2247) (Open, `Domain: Editor`)

**Auto\-imports insert \`import\` statement into CJS files**

*TypeScript auto-imports ES module syntax into CommonJS .js files with nodeXX module settings instead of require() despite type commonjs.*

 * created by **gebsh**
 * **gebsh** added label `Domain: Editor`

### [Issue microsoft/TypeScript-go#2248](https://github.com/microsoft/TypeScript-go/issues/2248) (Closed, `Crash`, **DanielRosenwasser**)

**Crash from ATA followed by request with no file\-watching client capability**

*TypeScript language server crashes when handling documentSymbol requests after initializing without file-watching capabilities and repeatedly opening and closing a file.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** added label `Crash`, and assigned to **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2248#issuecomment-3619501950) **DanielRosenwasser** attributed the crash to WatchedFiles not being initialized due to a missing didChangeWatchedFiles in his script and noted uncertainty about why earlier snapshot creation didn’t crash
 * [today](https://github.com/microsoft/TypeScript-go/issues/2248#issuecomment-3619508434) **DanielRosenwasser** said "Looks like it's not about repeating the operation, it's about waiting until ATA finishes. If you run the commands and wait long enough after running, it triggers the crash. I have a fix."

### [Issue microsoft/TypeScript-go#2249](https://github.com/microsoft/TypeScript-go/issues/2249) (Closed)

**Performance regression: ~3x slowdown after commit c86b8604**

*A recent commit (c86b8604) in typescript-go makes type-checking large codebases about three times slower.*

 * created by **litenjacob**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2249#issuecomment-3619665272) **jakebailey** said "Yikes, I don't know how I missed this."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2250](https://github.com/microsoft/TypeScript-go/pull/2250) (Closed)

**Revert "Make Program diagnostic API clearer \(\#2197\)"**

*Revert commit c86b860 clarifying the Program diagnostic API to rethink the approach and address #2249*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2251](https://github.com/microsoft/TypeScript-go/pull/2251) (Open)

**  Fix: Add mutex protection for projects map to prevent race conditions**

*Add mutex-based read and write locking for the API projects map to prevent concurrent data races.*

 * created by **Catsayer-Chan**
 * [later](https://github.com/microsoft/TypeScript-go/pull/2251#issuecomment-3619729436) **microsoft-github-policy-service[bot]** reminded the contributor to read and agree to the Contributor License Agreement by replying with the specified command
 * [later](https://github.com/microsoft/TypeScript-go/pull/2251#issuecomment-3619742802) **Catsayer-Chan** said " @microsoft-github-policy-service agree"

### [PR microsoft/TypeScript-go#2252](https://github.com/microsoft/TypeScript-go/pull/2252) (Closed)

**Make \`\(\*WatchedFiles\[T\]\)\.Clone\` propagate \`nil\`**

*Modify the Clone method of WatchedFiles[T] to return nil when the receiver is nil.*

 * created by **DanielRosenwasser**

### [Issue microsoft/TypeScript-go#2253](https://github.com/microsoft/TypeScript-go/issues/2253) (Open, `Domain: JS`, `Crash`, **Copilot**)

**Crash completing beginning of property name when preceded by JSDoc**

*Completion requests at the start of a JSDoc-preceded property name cause a nil pointer dereference crash in the TypeScript service.*

 * created by **DanielRosenwasser**
 * **DanielRosenwasser** added label `Crash`

### [Issue microsoft/TypeScript-go#2254](https://github.com/microsoft/TypeScript-go/issues/2254) (Closed, `Crash`, **Copilot**)

**Completions crash in call to \`new Map\(\.\.\.\)\`\.**

*Requesting completions at array element positions in new Map(...) triggers an index-out-of-range panic in the typescript-go LSP server.*

 * created by **DanielRosenwasser**
 * **DanielRosenwasser** added label `Crash`

### [PR microsoft/TypeScript-go#2257](https://github.com/microsoft/TypeScript-go/pull/2257) (Open)

**fix\(2212\): make enum constant inlining consistent with Strada behavior**

*Adjust enum constant inlining implementation to match Strada behavior and resolve related inconsistencies.*

 * created by **a-tarasyuk**

