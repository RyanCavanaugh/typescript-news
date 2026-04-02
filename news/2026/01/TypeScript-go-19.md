# Report for 2026-01-19 (Monday, January 19th, 2026)

7 different users commented on 11 different issues.

## Recommended Actions

 * Response Recommended
    * @rubnogueira reported a panic occurrence without repro in [microsoft/TypeScript-go#2077](https://github.com/microsoft/TypeScript-go/issues/2077#issuecomment-3772204936)
    * @rubnogueira reported IDE sluggishness due to RAM usage with pnpm + tsconfig project references in [microsoft/TypeScript-go#2239](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3772234647)
    * @jogibear9988 asked for ideas on how to proceed in [microsoft/TypeScript-go#2402](https://github.com/microsoft/TypeScript-go/issues/2402#issuecomment-3771891076)
    * @TheArcaneBrony suggested adding a warning message in [microsoft/TypeScript-go#2545](https://github.com/microsoft/TypeScript-go/issues/2545#issuecomment-3770938188)
    * @TheArcaneBrony reported a MODULE_NOT_FOUND error after the change in [microsoft/TypeScript-go#2545](https://github.com/microsoft/TypeScript-go/issues/2545#issuecomment-3770951841)

## Activity Summary

### [Issue microsoft/TypeScript-go#2077](https://github.com/microsoft/TypeScript-go/issues/2077) (Open, `Crash`, **jakebailey**)

**Inlayhint panic**

*The inlay hint provider panics when handling textDocument/inlayHint requests due to an out-of-range line number.*

 * [6 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2077#issuecomment-3603910306) **rubnogueira** reported a panic with 'Token cache mismatch: parent' error and included a stack trace
 * [6 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2077#issuecomment-3607740977) **jakebailey** said "That is an unrelated panic. #2193"
 * **RyanCavanaugh** assigned to **jakebailey**
 * [later](https://github.com/microsoft/TypeScript-go/issues/2077#issuecomment-3772204936) **rubnogueira** reported experiencing a panic with version 0.20260119.1 but could not reproduce it

### [Issue microsoft/TypeScript-go#2239](https://github.com/microsoft/TypeScript-go/issues/2239) (Closed, `Needs More Info`)

**take too much memory**

*tsgo extension consumes about 17GB of RAM on macOS M1, causing heavy swapping and slowing VS Code.*

 * [today](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3767082349) **OliverJAsh** said "The first bad commit is 38353bd4d704efd6d00ec277087bbca5a7d050ff."
 * [today](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3767242958) **dream2333** said "same"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3768557703) **MartinCura** described experiencing increasing memory usage in tsgo on each save, tested it, attached a heap profile and screenshot, and suggested periodic restarts
 * [later](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3772234647) **rubnogueira** described IDE performance degrading over time due to high RAM usage with pnpm and tsconfig project references after fixes #2390 and #2502

### [Issue microsoft/TypeScript-go#2362](https://github.com/microsoft/TypeScript-go/issues/2362) (Open)

**LSP diagnostics not working in Emacs's eglot**

*tsgo LSP server fails to publish diagnostics to Emacs’s eglot unlike typescript-language-server, possibly due to client capabilities mismatch.*

 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2362#issuecomment-3652274978) **joaotavora** reported that tsgo LSP implementation does not provide diagnostics for related documents via relatedDocumentSupport
 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2362#issuecomment-3652555217) **jakebailey** compared the new language server’s diagnostic behavior to tsserver, noting it only showed diagnostics for opened files and referenced issue #2169 for unopened files
 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2362#issuecomment-3654617423) **joaotavora** explained that he had two open documents and expected the language server to maintain a dependency graph for diagnostic pulls, criticized VSCode's approach as inefficient, and noted having long ago left JavaScript land
 * [today](https://github.com/microsoft/TypeScript-go/issues/2362#issuecomment-3769773262) **dstaley** noted that Nova currently only supports textDocument.publishDiagnostics and expressed doubt that supporting push diagnostics would be justified

### [Issue microsoft/TypeScript-go#2402](https://github.com/microsoft/TypeScript-go/issues/2402) (Open, `Crash`)

**tsgo takes forever to compile, 325seconds vs typescript 42seconds**

*tsgo watch compilation takes 325s versus TypeScript’s 42s, and the reporter requests help diagnosing and resolving the slowdown.*

 * [1 month ago](https://github.com/microsoft/TypeScript-go/issues/2402#issuecomment-3671370893) **jakebailey** said "#2411 for the 18.1 hang"
 * [1 month ago](https://github.com/microsoft/TypeScript-go/issues/2402#issuecomment-3673779704) **jogibear9988** asked how to track down which files cause the issue and whether they could share via a private repo; noted that reverting to yesterday’s version did not resolve it
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2402#issuecomment-3703426438) **jogibear9988** reported that the newest version still errored, observed that disabling sourcemaps reduced ts-go build time to 13s versus 32s for normal TypeScript, and noted a ~5s startup delay before the build message
 * [later](https://github.com/microsoft/TypeScript-go/issues/2402#issuecomment-3771891076) **jogibear9988** said "Any ideas how we could proceed with this?"

### [Issue microsoft/TypeScript-go#2523](https://github.com/microsoft/TypeScript-go/issues/2523) (Closed, `bug`, **ahejlsberg**)

**Type inference in a discriminated union with jsx**

*JSX discriminated union incorrectly infers child value as any in tsgo instead of boolean in TypeScript 5.9*

 * created by **domarmstrong**
 * (today) **ahejlsberg** added label `bug`, and assigned to **ahejlsberg**
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#2544](https://github.com/microsoft/TypeScript-go/pull/2544) (Closed)

**Fix issue in \`discriminateContextualTypeByJSXAttributes\`**

*Remove redundant empty map check for uninitialized Members in discriminateContextualTypeByJSXAttributes because nil map lookups are safe.*

 * created by **ahejlsberg**
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#2545](https://github.com/microsoft/TypeScript-go/issues/2545) (Closed)

**\`tsgo \-b \-v\` differs in output directory**

*tsgo’s `-b -v` build command emits output into dist/src/ rather than the expected dist/ directory.*

 * created by **TheArcaneBrony**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2545#issuecomment-3770671780) **jakebailey** listed related issues and recommended setting rootDir, then asked if an error was expected
 * [today](https://github.com/microsoft/TypeScript-go/issues/2545#issuecomment-3770938188) **TheArcaneBrony** confirmed that setting rootDir fixed the issue and suggested adding a warning message
 * [today](https://github.com/microsoft/TypeScript-go/issues/2545#issuecomment-3770951841) **TheArcaneBrony** reported that the change omitted some code, causing a MODULE_NOT_FOUND error for a missing file
 * [today](https://github.com/microsoft/TypeScript-go/issues/2545#issuecomment-3770956577) **jakebailey** asked for the full repro and noted that warning messages hadn’t historically been used
 * [today](https://github.com/microsoft/TypeScript-go/issues/2545#issuecomment-3770967313) **TheArcaneBrony** said "Ah, I figured it out... i was doing rm -rf dist/*, but tsconfig.tsbuildinfo was moved from dist/ to ./, which was causing it to skip compilation at all..."

### [Issue microsoft/TypeScript-go#2546](https://github.com/microsoft/TypeScript-go/issues/2546) (Closed)

**\[Typo\] Possible typo in JSDoc string for \`Math\.trunc\(…\)\` function \(lib\.es2015\.core\.d\.ts\)**

*Correct the JSDoc in lib.es2015.core.d.ts to fix ‘the a numeric expression’ typo in the Math.trunc comment.*

 * created by **o-m12a**

### [PR microsoft/TypeScript-go#2547](https://github.com/microsoft/TypeScript-go/pull/2547) (Closed)

**Fix a typo in the JSDoc of \`Math\.trunc\(…\)\`**

*Corrects a typo in the JSDoc comment for the Math.trunc function.*

 * created by **o-m12a**

### [PR microsoft/TypeScript-go#2548](https://github.com/microsoft/TypeScript-go/pull/2548) (Closed)

**Remove code related to dead compiler options**

*Remove obsolete compiler option handling by dropping related code and associated diffs.*

 * created by **jakebailey**

