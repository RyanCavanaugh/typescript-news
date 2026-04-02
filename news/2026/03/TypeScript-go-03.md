# Report for 2026-03-03 (Tuesday, March 3rd, 2026)

16 different users commented on 35 different issues.

## Recommended Actions

 * Response Recommended
    * @tats-u provided information about regression condition and workaround in [microsoft/TypeScript-go#2661](https://github.com/microsoft/TypeScript-go/issues/2661#issuecomment-3995729836)
    * @goloveychuk asked if the code snippet was correct in [microsoft/TypeScript-go#2780](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-3992810985)
    * @goloveychuk proposed a code change to skip package names starting with '.' in [microsoft/TypeScript-go#2780](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-3996536169)
    * @goloveychuk provided root cause analysis and reproduction steps in [microsoft/TypeScript-go#2780](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-3996771372)

## Activity Summary

### [Issue microsoft/TypeScript-go#1054](https://github.com/microsoft/TypeScript-go/issues/1054) (Closed, `Domain: Module Resolution`, **ahejlsberg**)

**\`tsgo\` doesn't allow importing from a commonJS module in a way that \`tsc\` does allow\.**

*tsgo errors when importing named exports from a CommonJS module without esModuleInterop enabled, whereas tsc compiles it successfully.*

 * created by **joshcartme**
 * **jakebailey** added label `Domain: Module Resolution`
 * **ahejlsberg** assigned to **ahejlsberg**
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#2447](https://github.com/microsoft/TypeScript-go/pull/2447) (Closed, **jakebailey**, **Copilot**)

**Fix decorated class methods with Symbol names to emit valid code**

*tsgo emits invalid JavaScript for decorated class methods with computed Symbol names, causing a ReferenceError due to an undefined variable.*

 * created by **Copilot**
 * (7 weeks ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/2447#issuecomment-3992951004) **jakebailey** said "I independently discovered this in #2956."

### [Issue microsoft/TypeScript-go#2476](https://github.com/microsoft/TypeScript-go/issues/2476) (Closed)

**TS4020 error with @ts\-ignore on imports needed for declaration emit**

*Using @ts-ignore on an import required for declaration emit causes tsgo to incorrectly report TS4020 errors.*

 * created by **fubhy**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2476#issuecomment-3992570515) **gabritto** said "Fixed in #2475."
 * (today) **gabritto** closed the issue

### [Issue microsoft/TypeScript-go#2661](https://github.com/microsoft/TypeScript-go/issues/2661) (Open, `Domain: Editor`, **andrewbranch**)

**auto\-import adds inline type modifier to existing import type statement**

*Auto-import incorrectly adds inline type modifiers to named imports in an import type statement, causing a TS2206 error.*

 * **mrvissercb** added label `Domain: Editor`
 * [1 month ago](https://github.com/microsoft/TypeScript-go/issues/2661#issuecomment-3843462895) **mrvissercb** said "Originally reported here: https://github.com/microsoft/vscode/issues/292038"
 * **andrewbranch** assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2661#issuecomment-3995729836) **tats-u** said "Bumped into this. This is a regression from Strada, as the description suggests. It does not occur while "TypeScript Native Preview: Disable"'d."

### [PR microsoft/TypeScript-go#2693](https://github.com/microsoft/TypeScript-go/pull/2693) (Closed, **jakebailey**, **Copilot**)

**Fix esModuleInterop not being respected for JS CommonJS imports**

*tsgo incorrectly reports TS2497 for named exports from CommonJS JavaScript files despite esModuleInterop being enabled*

 * created by **Copilot**
 * (3 weeks ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2780](https://github.com/microsoft/TypeScript-go/issues/2780) (Open, `Domain: Editor`, `Needs More Info`, **andrewbranch**)

**High memory consumption in a large pnpm monorepo**

*PR #2502 causes minor edits in a large pnpm monorepo to spike the TypeScript extension memory from ~700MB to ~35GB.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-3986620084) **JacobNWolf** reported experiencing the same issue at beehiiv that crashed his Mac until he disabled the TypeScript Native extension, described his large PNPM monorepo setup, and offered to help debug under NDA
 * [today](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-3991640806) **goloveychuk** reported that hovering on the Browser symbol caused the LSP to hang and consume excessive memory in a pnpm layout under Yarn
 * [today](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-3991968372) **goloveychuk** reported that the patch fixed the issue for them, shared the output after waiting, and asked if it searched all files for symbols
 * [today](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-3992616595) **andrewbranch** said "@goloveychuk thanks for all the investigations. Can you post the full path of one of those? I think I'm getting an idea of what's happening."
 * [today](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-3992788882) **apendua** explained that pnpm creates many symbolic links and suggested that recursive directory paths could cause infinite cache growth
 * [today](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-3992810985) **goloveychuk** provided code snippet with imports and asked if it was correct
 * [today](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-3993192441) **andrewbranch** suggested logging bucket.DependencyNames and adding a panic guard to diagnose why `.store-fuse-unplugged` was treated as a package
 * [today](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-3993218413) **goloveychuk** stated they would check tomorrow and suggested providing a build with disabled auto imports so others could test for the same root cause
 * [today](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-3995534162) **shinichy** debugged computeDependenciesForNodeModulesDirectory and confirmed it only adds direct dependencies, explained the earlier nil was due to a premature breakpoint, and noted that extractPackages never completes because extractor.extractFromFile(entrypoint) gets stuck
 * [later](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-3996536169) **goloveychuk** proposed adding a condition to skip package names starting with '.' in extractPackages to prevent .store-fuse-unplugged from being included
 * [later](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-3996574831) **jakebailey** asked the reporter to test with the latest nightly, noting that #2965 contained fixes
 * [later](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-3996771372) **goloveychuk** confirmed the fix works in the main branch, analysed the root cause of package name resolution falling back to .store-fuse-unplugged due to a nested package.json without a name, and suggested improving the search logic

### [Issue microsoft/TypeScript-go#2781](https://github.com/microsoft/TypeScript-go/issues/2781) (Open)

**resolving library types with import assignment \`import = require\(\)\` fails**

*Named and default type exports from @sendgrid/mail included via import assignment work in TypeScript 6.0 but tsgo reports missing members and default-only import errors.*

 * **RyanCavanaugh** added label `wontfix`
 * [6 days ago](https://github.com/microsoft/TypeScript-go/issues/2781#issuecomment-3963151561) **RyanCavanaugh** said "Yeah, this isn't any sort of maintainable invariant"
 * (6 days ago) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/issues/2781#issuecomment-3992979711) **jakebailey** said "Opening this as we're currently discussing this, though it's definitely not correct to export type space like this even with #2946"
 * (today) **jakebailey** reopened the issue
 * **jakebailey** removed label `wontfix`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2781#issuecomment-3992980470) **jakebailey** said "Related: https://github.com/microsoft/typescript-go/issues/1380"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2781#issuecomment-3993660455) **ahejlsberg** confirmed that even with PR #2946 the `@sendgrid/mail` package would error due to both exported value symbols and an export assignment

### [PR microsoft/TypeScript-go#2925](https://github.com/microsoft/TypeScript-go/pull/2925) (Closed)

**Misc source map fixes**

*Extract miscellaneous source map fixes from the ES2022 branch to reduce diffs.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2926](https://github.com/microsoft/TypeScript-go/pull/2926) (Open)

**Implement ES decorator transform \(ESNext \-\> ES2022\)**

*Add ESNext-to-ES2022 decorator transform support in tsgo to unblock its adoption.*

 * created by **AlCalzone**
 * [4 days ago](https://github.com/microsoft/TypeScript-go/pull/2926#issuecomment-3975214922) **AlCalzone** said "Thanks for the thorough review - I'll see what I can do about it."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2926#issuecomment-3989835921) **AlCalzone** said "@weswigham @jakebailey I think I've addressed everything now."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2926#issuecomment-3992277016) **jakebailey** said "I want to wait for #2956 before looking into this; there is some overlap and that one is basically complete."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2926#issuecomment-3993216772) **AlCalzone** said "Cool, let me know when that PR is done and I'll see what I need to change here."

### [PR microsoft/TypeScript-go#2943](https://github.com/microsoft/TypeScript-go/pull/2943) (Closed)

**fix\(api\): DocumentIdentifier JSON unmarshaling panic**

*Save JSON object keys before reading values and handle "fileName" to fix DocumentIdentifier unmarshal panic.*

 * created by **ajmacd**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2943#issuecomment-3989087477) **ajmacd** said "@microsoft-github-policy-service agree"
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2943#issuecomment-3989097248) **ajmacd** thanked the reviewer for catching the missing fileName field, added a test for documentation, and asked if it should be removed
 * [today](https://github.com/microsoft/TypeScript-go/pull/2943#issuecomment-3995528735) **ajmacd** said "Apologies, had to fix some CI failures. I think I was able to run everything successfully locally this time, so the latest commit should be good."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2946](https://github.com/microsoft/TypeScript-go/pull/2946) (Closed)

**Improve CommonJS support, round 2**

*Enable overlaying of type and namespace declarations on CommonJS export assignments, allow multiple module.exports unions, and align Corsa with Strada behavior*

 * created by **ahejlsberg**
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/2946#issuecomment-3981689855) **ahejlsberg** mentioned an existing issue with declaration file generation for CommonJS modules with module.exports assignments, noted that the initial bug was fixed, and highlighted that multiple and nested module.exports assignments remain unhandled
 * [today](https://github.com/microsoft/TypeScript-go/pull/2946#issuecomment-3992782126) **ahejlsberg** noted that the latest commits fixed the example issue but reported that nested module.exports assignments weren't handled by the declaration emitter and declined to fix it in this PR
 * [today](https://github.com/microsoft/TypeScript-go/pull/2946#issuecomment-3992862722) **weswigham** clarified that the corsa stub is unused and explained the need for new declaration emitter logic for non-top-level export assignments
 * [today](https://github.com/microsoft/TypeScript-go/pull/2946#issuecomment-3992889610) **jakebailey** said "I think we have been gradually backing off on that logic, as we discover more things that the reparser can't do (e.g., the defineProperties stuff)."

### [PR microsoft/TypeScript-go#2952](https://github.com/microsoft/TypeScript-go/pull/2952) (Closed)

**Fixed a go\-to\-def crash on decorators attached to invalid targets**

*Fixed a go-to-definition crash triggered by decorators attached to invalid targets.*

 * created by **Andarist**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2952#issuecomment-3985784294) **jakebailey** said "CI is failing, unfortunately."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2952#issuecomment-3989797672) **Andarist** said "@jakebailey that was just caused by my last-minute test file renaming 😬 I fixed that, it should be good to go now"
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2953](https://github.com/microsoft/TypeScript-go/issues/2953) (Open, `Crash`, **DanielRosenwasser**, **Copilot**)

**Inlay hints triggers crash during checker initialization**

*Inlay hints cause the TypeScript checker to crash during initialization in the editor.*

 * created by **DanielRosenwasser**
 * **DanielRosenwasser** added label `Crash`
 * (today) **DanielRosenwasser** assigned to **Copilot**, **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2953#issuecomment-3992836790) **Andarist** shared a contrived Go fourslash test that reproduced an earlier crash and noted it also crashed in Strada requiring esModuleInterop
 * [today](https://github.com/microsoft/TypeScript-go/issues/2953#issuecomment-3993412640) **Andarist** provided a TypeScript code snippet illustrating correct augmentation resolution

### [PR microsoft/TypeScript-go#2955](https://github.com/microsoft/TypeScript-go/pull/2955) (Closed)

**Clean up disk file caches more often, force GC**

*Propose more frequent disk file cache cleanup and forced garbage collection to reduce memory usage and prevent open files backlog in agent mode sessions.*

 * created by **andrewbranch**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2955#issuecomment-3987869693) **jakebailey** said "I think we could do the GC without any options, yeah."
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#2957](https://github.com/microsoft/TypeScript-go/pull/2957) (Closed)

**Log runtime/metrics on UpdateSnapshot**

*Add runtime and metrics logging to UpdateSnapshot to help diagnose memory issues.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2958](https://github.com/microsoft/TypeScript-go/issues/2958) (Closed)

**Regression from Strada: IntelliSense does not work properly inside \`{}\` following \`@throws\`**

*IntelliSense suggestions for error types inside braces after an @throws annotation are missing in tsgo but present in TypeScript 6.0.*

 * created by **tats-u**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2960](https://github.com/microsoft/TypeScript-go/pull/2960) (Closed)

**Fixes a crash when requesting implementations on a tripleslash directive**

*Requesting code implementations for a tripleslash directive caused the compiler to crash and this update prevents it.*

 * created by **Andarist**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2961](https://github.com/microsoft/TypeScript-go/pull/2961) (Closed)

**Skip all tests with alwaysStrict=false**

*Skip all variant tests marked alwaysStrict=false because they do not affect coverage.*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#2962](https://github.com/microsoft/TypeScript-go/pull/2962) (Open, **DanielRosenwasser**, **Copilot**)

**Fix nil dereference crash in checker initialization with array types**

*Guard against nil global array types during symbol merging to prevent checker initialization crashes.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **DanielRosenwasser**

### [PR microsoft/TypeScript-go#2963](https://github.com/microsoft/TypeScript-go/pull/2963) (Open, **andrewbranch**, **Copilot**)

**Port FindNextToken and FindPrecedingToken from Go to TypeScript**

*Port findNextToken and findPrecedingToken from Go to the TypeScript AST package and validate behavior against Go baselines.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2963#issuecomment-3993679555) **andrewbranch** said "@copilot+claude-sonnet-4.6 also do FindPrecedingToken"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2963#issuecomment-3993719559) **Copilot** added findPrecedingToken public export to astnav.ts and added four tests in the API test files
 * [today](https://github.com/microsoft/TypeScript-go/pull/2963#issuecomment-3993731747) **andrewbranch** said "@copilot+claude-sonnet-4.6 hereby format"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2963#issuecomment-3993748508) **Copilot** stated that formatting was completed in commit 12ef49c4
 * [today](https://github.com/microsoft/TypeScript-go/pull/2963#issuecomment-3994311130) **andrewbranch** said "@copilot see review feedback, failing tests, and carefully compare your implementation against tokens.go. Run tests and format before committing."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2963#issuecomment-3994516934) **Copilot** described fixes implemented in commit a4777eb2 including always returning scanned tokens in findNextToken, adding scanner-based scanning in findRightmostValidToken, adding JSDoc support in findPrecedingTokenImpl, and removing an incorrect test

### [Issue microsoft/TypeScript-go#2964](https://github.com/microsoft/TypeScript-go/issues/2964) (Closed, `Domain: Editor`)

**\[ServerErrors\]\[JavaScript\] linux\-x64\-7\.0\.0\-dev\.20260303\.1 vs **

*The linux-x64-7.0.0-dev.20260303.1 CI run reported 12 notable changes among 216 successful analyses and various failures across 300 TypeScript repositories.*

 * created by **typescript-bot**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2964#issuecomment-3993187586) **typescript-bot** reported panic during textDocument/implementation handling due to unexpected nil in getImmediateAliasedSymbol with stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/2964#issuecomment-3993187631) **typescript-bot** reported a panic in textDocument/implementation request handling with a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/2964#issuecomment-3993187702) **typescript-bot** reported a panic due to nil pointer dereference during handling of textDocument/implementation
 * [today](https://github.com/microsoft/TypeScript-go/issues/2964#issuecomment-3993187749) **typescript-bot** reported a panic handling textDocument/definition due to an unhandled case in getDiagnosticHeadMessageForDecoratorResolution
 * [today](https://github.com/microsoft/TypeScript-go/issues/2964#issuecomment-3993187811) **typescript-bot** reported a panic in handling textDocument/documentHighlight due to unexpected KindFunctionExpression trivia
 * [today](https://github.com/microsoft/TypeScript-go/issues/2964#issuecomment-3993187876) **typescript-bot** reported a panic during handling of textDocument/documentHighlight due to an unexpected nil in getImmediateAliasedSymbol
 * [today](https://github.com/microsoft/TypeScript-go/issues/2964#issuecomment-3993187942) **typescript-bot** reported a premature server connection closure error with raw error text, replay commands, recent requests, and repro steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/2964#issuecomment-3993188017) **typescript-bot** reported server connection closed prematurely and provided affected repo details, LSP request logs, and repro steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/2964#issuecomment-3993188076) **typescript-bot** reported a 'server connection closed prematurely: undefined' error and included reproduction steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/2964#issuecomment-3993188145) **typescript-bot** reported server connection closed prematurely error with repro steps and artifacts for videojs/video.js
 * [today](https://github.com/microsoft/TypeScript-go/issues/2964#issuecomment-3993188217) **typescript-bot** reported that the TS server connection closed prematurely with undefined error during analysis of mui/material-ui

### [PR microsoft/TypeScript-go#2965](https://github.com/microsoft/TypeScript-go/pull/2965) (Closed)

**Allow turning auto\-imports off; some edge case fixes**

*Add support for disabling JS/TS auto-import suggestions and implement safeguards against edge-case node_modules paths and unparseable package.json files.*

 * created by **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#2966](https://github.com/microsoft/TypeScript-go/pull/2966) (Open)

**Clamp received \`lsproto\.Position\`s**

*Clamp received lsproto.Position values to valid line and character boundaries.*

 * created by **Andarist**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2966#issuecomment-3993975441) **DanielRosenwasser** noted that they plan to possibly implement this or silently error in the future but currently want to identify issues in request handling or the VS Code language server client

### [PR microsoft/TypeScript-go#2967](https://github.com/microsoft/TypeScript-go/pull/2967) (Closed)

**Fix various namespace diffs**

*Several fixes address import elision errors and other inconsistencies in namespace handling.*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#2968](https://github.com/microsoft/TypeScript-go/pull/2968) (Closed)

**Update submodule for TS 6\.0 RC**

*Update the project’s submodule to point to the TypeScript 6.0 release candidate*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2969](https://github.com/microsoft/TypeScript-go/pull/2969) (Closed)

**Remove outdated ES module check**

*Remove the outdated ES module check to simplify module identification and improve compatibility.*

 * created by **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2969#issuecomment-3994162187) **ahejlsberg** said "No need for regression test, we already had multiple failing tests with the same pattern."
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#2970](https://github.com/microsoft/TypeScript-go/pull/2970) (Open)

**Fix nil dereference crash during checker initialization when resolving array types**

*Introduce lazy global array type initialization and transient symbol handling to prevent nil dereference crashes during checker initialization*

 * created by **Andarist**

### [PR microsoft/TypeScript-go#2971](https://github.com/microsoft/TypeScript-go/pull/2971) (Closed)

**Support JSDoc \`@throws\`**

*Add support for JSDoc @throws tags when generating Go code from TypeScript.*

 * created by **Andarist**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2972](https://github.com/microsoft/TypeScript-go/pull/2972) (Closed)

**\[@typescript/api\] Add a few more checker APIs**

*Add TypeScript checker API methods for context sensitivity, type retrieval, base types, properties, index infos, constraints, and type arguments.*

 * created by **andrewbranch**

### [PR microsoft/TypeScript-go#2973](https://github.com/microsoft/TypeScript-go/pull/2973) (Closed)

**Fix quick info display for \`@throws\` tag's \`typeExpression\`**

*Fix quick info display of @throws tag typeExpression by aligning display parts format with markdown baselines*

 * created by **Andarist**
 * [later](https://github.com/microsoft/TypeScript-go/pull/2973#issuecomment-3996291503) **jakebailey** explained that the LSP no longer includes display parts
 * (later) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2974](https://github.com/microsoft/TypeScript-go/issues/2974) (Open, `Domain: Editor`)

**Missing auto\-import for subpath imports of other local packages**

*VS Code TypeScript auto-imports fail to recognize subpath imports from sibling local workspace packages.*

 * created by **psznm**
 * **psznm** added label `Domain: Editor`

### [PR microsoft/TypeScript-go#2975](https://github.com/microsoft/TypeScript-go/pull/2975) (Closed)

**Fix document highlight panic on nested \`require\` destructuring**

*Prevent document highlight from panicking on nested require destructuring patterns.*

 * created by **Andarist**

