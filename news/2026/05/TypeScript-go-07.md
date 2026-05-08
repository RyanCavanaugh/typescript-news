# Report for 2026-05-07 (Thursday, May 7th, 2026)

20 different users commented on 111 different issues.

## Recommended Actions

 * Response Recommended
    * @jbeaudoin-lf asked to reopen the issue in [microsoft/TypeScript-go#1685](https://github.com/microsoft/TypeScript-go/issues/1685#issuecomment-4406356310)
    * @ShenHongFei reported troubleshooting details and promised to provide a reproducible project in [microsoft/TypeScript-go#3734](https://github.com/microsoft/TypeScript-go/issues/3734#issuecomment-4405918795)

## Activity Summary

### [Issue microsoft/TypeScript-go#1685](https://github.com/microsoft/TypeScript-go/issues/1685) (Closed, `Domain: Type Checking`, `Domain: JS`, **sandersn**)

**\`ts\-check\` used with \`@typedef\` causes an error on \`module\.exports = \.\.\.\`**

*Combining @ts-check and @typedef in a CommonJS file causes a TS2309 export assignment error with tsgo.*

 * (1 month ago) **RyanCavanaugh** closed the issue
 * [1 month ago](https://github.com/microsoft/TypeScript-go/issues/1685#issuecomment-4218922623) **jbeaudoin-lf** said "Thanks, gonna give it a try tomorrow then !"
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1685#issuecomment-4236896401) **jbeaudoin-lf** asked which version was used and provided the version output and resulting error messages
 * [later](https://github.com/microsoft/TypeScript-go/issues/1685#issuecomment-4406356310) **jbeaudoin-lf** reported the same issue on Version 7.0.0-dev.20260508.1 and asked to reopen the issue

### [Issue microsoft/TypeScript-go#2437](https://github.com/microsoft/TypeScript-go/issues/2437) (Closed, `Domain: Editor`, **sandersn**, **Copilot**)

**TSGo prioritizes \`tsconfig\.json\` over \`jsconfig\.json\` in the same directory, even for file types the former excludes**

*TypeScript server in VS Code gives precedence to tsconfig.json over jsconfig.json for JavaScript files in the same directory, ignoring tsconfig.json’s exclusions.*

 * **Bertie690** added label `Domain: Editor`
 * (5 weeks ago) **RyanCavanaugh** set milestone to `TypeScript 7.0 RC`, and assigned to **sandersn**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2437#issuecomment-4400061458) **sandersn** described that tsc and tsgo behaved the same way and that renaming tsconfig.json and using -p jsconfig.json showed a difference in the project system
 * **sandersn** assigned to **Copilot**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2437#issuecomment-4400569363) **Bertie690** said "Correct - this bug (to my knowledge) is limited exclusively to the LSP's project inference."
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#2478](https://github.com/microsoft/TypeScript-go/pull/2478) (Closed)

**Exit LSP process if parent process stops existing**

*Implement periodic parent process ID checks in the LSP server to terminate the server when the parent process exits.*

 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/2478#issuecomment-4372407010) **andrewbranch** said "I ended last week with 7 orphaned tsgo processes, so I guess we do still need this."
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/2478#issuecomment-4372807985) **DanielRosenwasser** noted that the behavior seemed like a bug, observed it didn’t occur with Strada or the VS Code built-in, suggested investigating the latest language client, and proposed that sending events to a closed file descriptor could crash the process
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/2478#issuecomment-4373756615) **jakebailey** questioned the concern, stating that if the client died without closing the child it wasn’t their bug and if the client is still alive accumulating tsgo processes it’s a client bug unaffected by the PR
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2621](https://github.com/microsoft/TypeScript-go/issues/2621) (Open, `bug`, **iisaduan**, **Copilot**)

**Fourslash is broken when making requests in unconfigured \.js files**

*Fourslash requests in unconfigured .js files fail with “no project found” errors, breaking tests such as auto-import completion.*

 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2621#issuecomment-4269361026) **jakebailey** investigated an issue with fourslash tests and explained why the new runner’s server-based approach loads JS files and alters behavior compared to Strada
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2621#issuecomment-4270442818) **DanielRosenwasser** suggested switching to use the "state baselining" infrastructure if needed
 * (today) **iisaduan** set milestone to `Post-7.0`, and removed from milestone `TypeScript 7.0 RC`

### [Issue microsoft/TypeScript-go#2857](https://github.com/microsoft/TypeScript-go/issues/2857) (Open, `Domain: Editor`, `Needs Investigation`, **andrewbranch**)

**Formatters get stuck**

*The extension’s LSP-based formatter intermittently hangs during format-on-save on MacOS, never returning a response.*

 * (6 weeks ago) **DanielRosenwasser** set milestone to `TypeScript 7.0 RC`, and assigned to **andrewbranch**
 * [6 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2857#issuecomment-4138974027) **DanielRosenwasser** said "I haven't seen this in a while - maybe with assertions on we'll uncover more of these."
 * **andrewbranch** added label `Needs Investigation`

### [PR microsoft/TypeScript-go#2908](https://github.com/microsoft/TypeScript-go/pull/2908) (Open, **DanielRosenwasser**, **Copilot**)

**Add regression test for inlay hints crash on reparsed nodes \(\#2460\)**

*Add a regression test to ensure computing inlay hints on reparsed AST nodes in a JS module.exports function prevents panics.*

 * **Copilot** assigned to **DanielRosenwasser**
 * (2 weeks ago) **jakebailey** closed the issue
 * (2 weeks ago) **jakebailey** reopened the issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/2908#issuecomment-4403509887) **DanielRosenwasser** said "@copilot try building and fix and build errors."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2908#issuecomment-4403591216) **Copilot** fixed the build error by replacing bool true with core.TSTrue, adding the core import, and updating the baseline to reflect the correct output after the crash fix

### [PR microsoft/TypeScript-go#2944](https://github.com/microsoft/TypeScript-go/pull/2944) (Open)

**\[draft\] more formatting tests **

*A draft pull request addresses formatting bug fixes and adds tests, with more tests to follow post-7.0.*

 * [1 month ago](https://github.com/microsoft/TypeScript-go/pull/2944#issuecomment-4195501446) **typescript-bot** posted the requested performance run results
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2944#issuecomment-4238228195) **typescript-bot** provided performance run results
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2944#issuecomment-4238257454) **typescript-bot** said "@iisaduan, the perf run you requested failed. You can check the log here."
 * **iisaduan** added to milestone `Post-7.0`

### [PR microsoft/TypeScript-go#2962](https://github.com/microsoft/TypeScript-go/pull/2962) (Closed, **DanielRosenwasser**, **Copilot**)

**Fix nil dereference crash in checker initialization with array types**

*Guard against nil global array types during symbol merging to prevent checker initialization crashes.*

 * created by **Copilot**
 * (9 weeks ago) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2962#issuecomment-4403512592) **DanielRosenwasser** said "Linking back to #2953"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2962#issuecomment-4403516257) **DanielRosenwasser** said "Closing in favor of #2970."
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#2970](https://github.com/microsoft/TypeScript-go/pull/2970) (Closed, **ahejlsberg**)

**Fix nil dereference crash during checker initialization when resolving array types**

*Introduce lazy global array type initialization and transient symbol handling to prevent nil dereference crashes during checker initialization*

 * created by **Andarist**
 * (2 weeks ago) **RyanCavanaugh** set milestone to `TypeScript 7.0 RC`, and assigned to **ahejlsberg**
 * (later) **Andarist** closed the issue

### [PR microsoft/TypeScript-go#3369](https://github.com/microsoft/TypeScript-go/pull/3369) (Open)

**Limit loader/emitter to GOMAXPROCS**

*Limit parsing and emitting workloads to a GOMAXPROCS-sized goroutine pool to prevent unbounded concurrency and stack growth.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3369#issuecomment-4227905032) **typescript-bot** shared the requested performance run results
 * (3 weeks ago) **jakebailey** closed the issue
 * (2 weeks ago) **jakebailey** reopened the issue
 * **RyanCavanaugh** added to milestone `Possible Improvement`

### [Issue microsoft/TypeScript-go#3376](https://github.com/microsoft/TypeScript-go/issues/3376) (Open, `Crash`, **DanielRosenwasser**, **Copilot**)

**nil pointer dereference during diagnostics request**

*A nil pointer dereference occurs during diagnostics requests when resolving a SourceFile path.*

 * (1 month ago) **DanielRosenwasser** assigned to **Copilot**, and unassigned **Copilot**
 * **RyanCavanaugh** added to milestone `Possible Improvement`
 * [today](https://github.com/microsoft/TypeScript-go/issues/3376#issuecomment-4401530807) **DanielRosenwasser** verified a test case from issue #3380 and reproduced a nil pointer panic when only one of two conflicting files existed

### [PR microsoft/TypeScript-go#3377](https://github.com/microsoft/TypeScript-go/pull/3377) (Closed, **DanielRosenwasser**, **Copilot**)

**Fix nil pointer dereference in explainRedirectAndImpliedFormat during diagnostics**

*Add an early nil check and cached nil diagnostics in explainRedirectAndImpliedFormat to prevent panics when GetSourceFileByPath returns nil.*

 * created by **Copilot**
 * (1 month ago) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * (today) **DanielRosenwasser** closed the issue

### [Issue microsoft/TypeScript-go#3378](https://github.com/microsoft/TypeScript-go/issues/3378) (Open, `Crash`, **jakebailey**, **Copilot**)

**LSP request failure for diagnostics during type serialization**

*The TypeScript language server fails to generate diagnostics during type serialization due to symbol accessibility errors.*

 * (1 month ago) **DanielRosenwasser** assigned to **Copilot**, **DanielRosenwasser**
 * **RyanCavanaugh** added to milestone `Possible Improvement`
 * (today) **DanielRosenwasser** set milestone to `TypeScript 7.0 RC`, removed from milestone `Possible Improvement`, assigned to **jakebailey**, and unassigned **DanielRosenwasser**

### [PR microsoft/TypeScript-go#3380](https://github.com/microsoft/TypeScript-go/pull/3380) (Open, **DanielRosenwasser**, **Copilot**)

**Fix nil pointer dereference in explainRedirectAndImpliedFormat**

*Add nil guard in explainRedirectAndImpliedFormat to prevent panics when GetSourceFileByPath returns nil and add test for case-sensitive file path mismatches.*

 * **Copilot** assigned to **DanielRosenwasser**
 * [1 month ago](https://github.com/microsoft/TypeScript-go/pull/3380#issuecomment-4217222862) **DanielRosenwasser** said "@copilot try to figure out a test case for this."
 * [1 month ago](https://github.com/microsoft/TypeScript-go/pull/3380#issuecomment-4217303834) **Copilot** added a test case for file casing diagnostics on case-sensitive filesystems and verified it reproduced the nil pointer dereference and passed with the fix
 * [today](https://github.com/microsoft/TypeScript-go/pull/3380#issuecomment-4401715750) **DanielRosenwasser** said "This is a good find. I'm not sure if it's the best way to write the test. Also, #3753 seems related (it seems odd that we don't error earlier around files not being found)."
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [Issue microsoft/TypeScript-go#3413](https://github.com/microsoft/TypeScript-go/issues/3413) (Closed, `Domain: JS`, `Domain: Parser`, **DanielRosenwasser**)

**\`?\` can be used as a standalone JSDoc type when followed by \`\|\`**

*Using standalone `?` in JSDoc union types leads to incorrect inferred union types and hover tooltips.*

 * (3 weeks ago) **DanielRosenwasser** added labels `Domain: Parser`, `Domain: JS`
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * (today) **DanielRosenwasser** assigned to **DanielRosenwasser**, and unassigned **ahejlsberg**
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#3435](https://github.com/microsoft/TypeScript-go/pull/3435) (Open)

**Make LS checkers time out after being idle, segment based on use \(take 2\)**

*Reintroduce idle timeouts and usage-based segmentation for language server checkers to improve performance.*

 * created by **jakebailey**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * [today](https://github.com/microsoft/TypeScript-go/pull/3435#issuecomment-4400569102) **RyanCavanaugh** said "For context, this is a fix for #2115"
 * (today) **RyanCavanaugh** set milestone to `Possible Improvement`, and removed from milestone `TypeScript 7.0 RC`
 * [today](https://github.com/microsoft/TypeScript-go/pull/3435#issuecomment-4400627207) **jakebailey** said "It also technically fixes #3638"

### [PR microsoft/TypeScript-go#3440](https://github.com/microsoft/TypeScript-go/pull/3440) (Closed)

**\[internal/compiler/js\_exports\.go\] Export symbols for ts\-morph**

*Proposes exporting symbols for ts-morph in internal/compiler/js_exports.go to facilitate integration and notes wasm size reduction when switching to typescript-go.*

 * created by **SamuelMarks**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3440#issuecomment-4400575776) **RyanCavanaugh** said "Closing for housekeeping. We're definitely interested in WASM, just trying to scope for 7.0"
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#3451](https://github.com/microsoft/TypeScript-go/pull/3451) (Closed)

**perf: add TSGO\_BINARY env var and fast\-path sibling check in getExePath**

*Introduce TSGO_BINARY override and a fast-path sibling binary check in getExePath to avoid repeated import.meta.resolve calls and boost performance.*

 * created by **nileshpatil6**
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3451#issuecomment-4284655558) **jakebailey** said "If someone has this path, why wouldn't they just run it directly? This seems really special case-y."
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3451#issuecomment-4333762563) **nileshpatil6** proposed dropping TSGO_BINARY and asked whether to push a revised version with only the sibling check
 * [today](https://github.com/microsoft/TypeScript-go/pull/3451#issuecomment-4400589309) **RyanCavanaugh** closed the issue for now due to scoping concerns and expressed skepticism about the profiling results
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#3489](https://github.com/microsoft/TypeScript-go/issues/3489) (Open, `bug`, **iisaduan**)

**Lowercase\<"İ"\>\` differs between tsgo and tsc \(Go strings\.ToLower vs JS String\.prototype\.toLowerCase\)**

*tsgo’s Lowercase intrinsic uses Go’s strings.ToLower rather than ECMAScript’s full Unicode case mapping, causing mismatched lowercase results for characters like 'İ'*

 * created by **tomquist**
 * (yesterday) **RyanCavanaugh** added label `bug`, and set milestone to `TypeScript 7.0 RC`
 * **RyanCavanaugh** assigned to **iisaduan**

### [Issue microsoft/TypeScript-go#3491](https://github.com/microsoft/TypeScript-go/issues/3491) (Open, `Needs Investigation`, **ahejlsberg**)

**Excess\-property check fires on a nested object literal that is later assigned to an annotated return type, where tsc 6\.0 does not**

*TS7 incorrectly flags excess-property errors on nested object literals assigned via an untyped variable to a typed return, unlike TS6*

 * **ahejlsberg** assigned to **ahejlsberg**
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/3491#issuecomment-4296214357) **Andarist** described having a fix for the issue, provided sample code illustrating the problem, and reconsidered when to call getWidenedType before submitting the PR
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * **RyanCavanaugh** added label `Needs Investigation`

### [PR microsoft/TypeScript-go#3495](https://github.com/microsoft/TypeScript-go/pull/3495) (Open)

**Use JS\-compatible Unicode casing for intrinsic string mappings**

*Implement JavaScript-compatible Unicode casing rules in TypeScript’s intrinsic string mapping functions.*

 * created by **Andarist**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [PR microsoft/TypeScript-go#3497](https://github.com/microsoft/TypeScript-go/pull/3497) (Open, **ahejlsberg**)

**Widen types assigned to auto\-typed variables**

*Widen the types assigned to automatically-typed variables to improve type coverage and flexibility.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3497#issuecomment-4306383124) **Andarist** said "New tests are in now."
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3497#issuecomment-4338203608) **ahejlsberg** questioned whether the proposed change would cause property accesses (x.a, x.b, w.a, w.b) to error and argued this is undesirable
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3497#issuecomment-4339455258) **Andarist** demonstrated a TypeScript repro where accessing x.a should error but doesn’t, noted that the displayed type doesn’t reflect this, and said they would review all cases and propose a design over the upcoming weekend
 * (today) **RyanCavanaugh** set milestone to `TypeScript 7.0 RC`, and assigned to **ahejlsberg**

### [PR microsoft/TypeScript-go#3499](https://github.com/microsoft/TypeScript-go/pull/3499) (Open)

**feat\(2280\): Port implement interface quick fix**

*Port the implement interface quick fix feature to support automatic interface implementation.*

 * created by **a-tarasyuk**
 * **RyanCavanaugh** added to milestone `Post-7.0`
 * [today](https://github.com/microsoft/TypeScript-go/pull/3499#issuecomment-4401907480) **jakebailey** mentioned tests were ungenerated due to unrecognized fourslash statements and suggested excluding them from the PR
 * [today](https://github.com/microsoft/TypeScript-go/pull/3499#issuecomment-4401910486) **jakebailey** said "Though I asked copilot to help me find missing tests (since it's hard to do by hand) and it started trying to implement them, so, maybe it is possible 😄 "
 * [today](https://github.com/microsoft/TypeScript-go/pull/3499#issuecomment-4402886388) **jakebailey** shared a diff that added filename prefixes for allowed rangeAfterCodeFix tests and updated validateCodeFixCommands to accept a filename
 * [later](https://github.com/microsoft/TypeScript-go/pull/3499#issuecomment-4405520208) **a-tarasyuk** thanked Jake Bailey and mentioned pushing changes that add .not.codeFixAvailable support and remove unrelated generated tests

### [Issue microsoft/TypeScript-go#3504](https://github.com/microsoft/TypeScript-go/issues/3504) (Closed, `Crash`, **weswigham**, **Copilot**)

**Crash in declaration emit for JavaScript Test262 reserved\-words**

*Emitting declaration files panics with a nil pointer dereference when processing JavaScript Test262 reserved-word expando assignments.*

 * (yesterday) **RyanCavanaugh** set milestone to `TypeScript 7.0 RC`, assigned to **RyanCavanaugh**, and unassigned **RyanCavanaugh**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3505](https://github.com/microsoft/TypeScript-go/pull/3505) (Open, **johnfav03**)

**integrated filewatcher with lsp**

*Refactor vfswatch.FileWatcher for use by both CLI and LSP, integrating polling for clients without didChangeWatchedFiles support.*

 * created by **johnfav03**
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3505#issuecomment-4345380442) **andrewbranch** suggested trying usePollingWatcher and noted that the LSP client watcher still ran, observed that it scanned the .git directory causing slow performance, started profiling and recommended manual testing
 * (today) **RyanCavanaugh** set milestone to `TypeScript 7.0 RC`, and assigned to **johnfav03**

### [PR microsoft/TypeScript-go#3515](https://github.com/microsoft/TypeScript-go/pull/3515) (Open, **navya9singh**)

**Expose formatNodeForInsertion in internal API**

*Add the formatNodeForInsertion function to the library’s internal API to enable its use by external modules.*

 * created by **andrewbranch**
 * (today) **RyanCavanaugh** set milestone to `TypeScript 7.0 RC`, and assigned to **navya9singh**

### [PR microsoft/TypeScript-go#3518](https://github.com/microsoft/TypeScript-go/pull/3518) (Open)

**fix\(native\-preview\): preserve lone surrogate string literals**

*Encode and decode lone UTF-16 surrogates with WTF-8 in native-preview string and template literals and bump protocol to v6*

 * created by **TorinAsakura**
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3518#issuecomment-4301346088) **TorinAsakura** agreed to the CLA with no company specified
 * **RyanCavanaugh** added to milestone `Possible Improvement`

### [PR microsoft/TypeScript-go#3524](https://github.com/microsoft/TypeScript-go/pull/3524) (Closed)

**Fix hover verbosity for nested generic namespace merges**

*Adjust hover verbosity handling in nested generic namespace merges to prevent crashes during hover operations.*

 * created by **Andarist**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3524#issuecomment-4401789004) **gabritto** said "Fixed in https://github.com/microsoft/typescript-go/pull/3606."
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript-go#3528](https://github.com/microsoft/TypeScript-go/pull/3528) (Closed)

**chore: fix some minor issues in comments**

*Fix minor typos and inconsistencies in code comments.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3528#issuecomment-4306115325) **purelualight** quoted the Contributor License Agreement and provided instructions on how to agree with it
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3528#issuecomment-4306116514) **purelualight** said "@microsoft-github-policy-service agree"
 * [6 days ago](https://github.com/microsoft/TypeScript-go/pull/3528#issuecomment-4360385161) **purelualight** said "@gabritto Hi, Could you please review this PR at your convenience? Thank you very much."
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#3531](https://github.com/microsoft/TypeScript-go/pull/3531) (Open, **weswigham**)

**Preserve escaped identifier spelling in unresolved name diagnostics**

*Preserve original escaped identifier spelling in unresolved name diagnostics to improve error message clarity.*

 * created by **Andarist**
 * (today) **RyanCavanaugh** set milestone to `Possible Improvement`, and assigned to **weswigham**

### [Issue microsoft/TypeScript-go#3542](https://github.com/microsoft/TypeScript-go/issues/3542) (Open, `Domain: Declaration Emit`, `Needs Investigation`, **RyanCavanaugh**)

**Baselines: JS declaration emit adds \`export import\` modifier for require\-style import assignments**

*JS declaration emit adds export import modifiers to require-style assignments, changing the public API by exposing internal imports.*

 * **ahejlsberg** added label `Domain: Declaration Emit`
 * (2 days ago) **RyanCavanaugh** added label `Needs Investigation`, and set milestone to `TypeScript 7.0 RC`
 * **RyanCavanaugh** assigned to **weswigham**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3542#issuecomment-4399918237) **weswigham** stated the new output is correct and strada output is wrong, explained the cause, said they didn't care to match strada behavior, and suggested that @RyanCavanaugh decide whether to move this change to the accepted diff
 * (today) **weswigham** assigned to **RyanCavanaugh**, and unassigned **weswigham**

### [Issue microsoft/TypeScript-go#3543](https://github.com/microsoft/TypeScript-go/issues/3543) (Open, `Domain: Declaration Emit`, `Needs Investigation`, **RyanCavanaugh**)

**Baselines: CJS \`module\.exports = {}\` now emits \`export = \_default\` with inlined object type instead of named exports**

*CJS module.exports patterns now emit export = _default with inlined object types instead of named exports, requiring semantic validation*

 * **ahejlsberg** added label `Domain: Declaration Emit`
 * (2 days ago) **RyanCavanaugh** added label `Needs Investigation`, and set milestone to `TypeScript 7.0 RC`
 * **RyanCavanaugh** assigned to **weswigham**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3543#issuecomment-4399985812) **weswigham** explained that merging namespaces was unnecessary and local name swaps were nonfunctional, and suggested retriaging or opening a PR to adjust the emitted name
 * (today) **weswigham** assigned to **RyanCavanaugh**, and unassigned **weswigham**

### [Issue microsoft/TypeScript-go#3544](https://github.com/microsoft/TypeScript-go/issues/3544) (Open, `Domain: Declaration Emit`, `Needs Investigation`, **johnfav03**)

**Baselines: CJS class expression exports emit anonymous constructor types instead of named class declarations**

*CJS class expression exports emit anonymous constructor types in .d.ts files, producing malformed import types and TypeScript errors.*

 * **ahejlsberg** added label `Domain: Declaration Emit`
 * (2 days ago) **RyanCavanaugh** added label `Needs Investigation`, and set milestone to `TypeScript 7.0 RC`
 * **RyanCavanaugh** assigned to **weswigham**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3544#issuecomment-4400094208) **weswigham** explained that transformCommonJSExport needed to handle class expressions by treating them like aliases and hoisting them, or by adjusting the enclosing declaration logic
 * (today) **weswigham** assigned to **johnfav03**, and unassigned **weswigham**

### [Issue microsoft/TypeScript-go#3545](https://github.com/microsoft/TypeScript-go/issues/3545) (Open, `Domain: Declaration Emit`, `Needs Investigation`, **weswigham**)

**Baselines: CJS export alias and element access patterns changed**

*Declaration output now differs for CommonJS export aliases and module.exports element access patterns, including duplicate assignments.*

 * **ahejlsberg** added label `Domain: Declaration Emit`
 * (2 days ago) **RyanCavanaugh** added label `Needs Investigation`, and set milestone to `TypeScript 7.0 RC`
 * **RyanCavanaugh** assigned to **weswigham**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3545#issuecomment-4400155946) **weswigham** suggested relaxing checking to allow non-identifier export/import aliases in declaration files across all target levels and asked for @RyanCavanaugh's thoughts

### [Issue microsoft/TypeScript-go#3547](https://github.com/microsoft/TypeScript-go/issues/3547) (Open, `Domain: Declaration Emit`, `Needs Investigation`, **weswigham**)

**Baselines: Namespace\-to\-const restructuring with DtsFileErrors \(redeclaration errors\)**

*Namespace-to-const transformation in baselines erroneously produces invalid .d.ts files with TS2451 redeclaration errors.*

 * **ahejlsberg** added label `Domain: Declaration Emit`
 * (2 days ago) **RyanCavanaugh** added label `Needs Investigation`, and set milestone to `TypeScript 7.0 RC`
 * **RyanCavanaugh** assigned to **weswigham**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3547#issuecomment-4400324552) **weswigham** suggested skipping namespace merge members when host declarations for expandos had type annotations or full signatures, contrasted strada’s and corsa’s approaches, and noted that issue #3741 included a small fix

### [Issue microsoft/TypeScript-go#3548](https://github.com/microsoft/TypeScript-go/issues/3548) (Closed, `bug`, **weswigham**)

**Baselines: Decorator metadata reflects stable union type ordering**

*Reflect.getMetadata design:type for T|null unions now reports the non-null type instead of Object due to updated decorator metadata ordering.*

 * (yesterday) **RyanCavanaugh** added label `bug`, set milestone to `TypeScript 7.0 RC`, and assigned to **weswigham**
 * (today) **weswigham** closed the issue

### [Issue microsoft/TypeScript-go#3549](https://github.com/microsoft/TypeScript-go/issues/3549) (Open, `Domain: Declaration Emit`, `Needs Investigation`, **weswigham**)

**Baselines: Missing generic type arguments no longer auto\-filled with any \(produces TS2314 errors\)**

*Generic types without explicit parameters now emit bare types instead of defaulting to any, causing TS2314 errors*

 * **ahejlsberg** added label `Domain: Declaration Emit`
 * (2 days ago) **RyanCavanaugh** added label `Needs Investigation`, and set milestone to `TypeScript 7.0 RC`
 * **RyanCavanaugh** assigned to **weswigham**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3549#issuecomment-4400657746) **weswigham** noted the restoration of fewer-than-required type argument allowances for Array, Promise, and Object, referenced related TODOs, and opened #3745 with a fix

### [Issue microsoft/TypeScript-go#3551](https://github.com/microsoft/TypeScript-go/issues/3551) (Open, `bug`, `Domain: Declaration Emit`, `Needs Investigation`, **weswigham**)

**Baselines: Output file ordering changed \+ declaration types resolve to any instead of typeof references**

*Declaration emit with package exports tests now reorder output file sections and produce declaration types as any rather than typeof references*

 * **ahejlsberg** added label `Domain: Declaration Emit`
 * (2 days ago) **RyanCavanaugh** added label `Needs Investigation`, and set milestone to `TypeScript 7.0 RC`
 * **RyanCavanaugh** assigned to **weswigham**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3551#issuecomment-4400735718) **weswigham** highlighted that file reordering was unimportant but the ': any' on package self-name import references was important, asked whether another issue existed for messed-up self-name refs, and noted that this issue required investigation as it indicated a checking pipeline problem
 * **weswigham** added label `bug`

### [Issue microsoft/TypeScript-go#3552](https://github.com/microsoft/TypeScript-go/issues/3552) (Closed, `Domain: Declaration Emit`, **andrewbranch**, **RyanCavanaugh**, **Copilot**)

**Baselines: export = a reordered; ESM side\-effect import replaces export {}**

*Baseline diffs indicate that CommonJS export assignments are reordered after declarations and empty ES exports are replaced by side-effect imports.*

 * (1 week ago) **RyanCavanaugh** set milestone to `TypeScript 7.0 RC`, and assigned to **RyanCavanaugh**
 * [6 days ago](https://github.com/microsoft/TypeScript-go/issues/3552#issuecomment-4361735218) **andrewbranch** acknowledged that JS elision behavior was unique to the Strada JS declaration emitter and suggested standardizing on the TS emitter, possibly marking the issue as wontfix
 * (today) **andrewbranch** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/issues/3552#issuecomment-4401947085) **andrewbranch** said "Reopening until I move the baselines into submoduleAccepted"
 * (today) **andrewbranch** reopened the issue
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#3555](https://github.com/microsoft/TypeScript-go/issues/3555) (Open, `Domain: Declaration Emit`, `Needs Investigation`, **weswigham**)

**Baselines: @overload handling changes in JS declaration emit**

*JS declaration emit for JSDoc @overload alters overload output by removing or duplicating comments, losing type parameters, and collapsing signatures.*

 * **ahejlsberg** added label `Domain: Declaration Emit`
 * (2 days ago) **RyanCavanaugh** added label `Needs Investigation`, and set milestone to `TypeScript 7.0 RC`
 * **RyanCavanaugh** assigned to **weswigham**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3555#issuecomment-4400834104) **weswigham** noted that the diffs were due to missing `declare` modifiers, jsdoc comments, or reordered declarations and said no further action was needed

### [Issue microsoft/TypeScript-go#3556](https://github.com/microsoft/TypeScript-go/issues/3556) (Open, `Domain: Declaration Emit`, `Needs Investigation`, **weswigham**)

**Baselines: @callback/@overload tags reordered and restructured in declaration emit**

*Declaration emit reorders callback and overload tags, simplifies type definitions, and mistakenly changes rest parameters from string[] to string.*

 * **ahejlsberg** added label `Domain: Declaration Emit`
 * (2 days ago) **RyanCavanaugh** added label `Needs Investigation`, and set milestone to `TypeScript 7.0 RC`
 * **RyanCavanaugh** assigned to **weswigham**

### [Issue microsoft/TypeScript-go#3557](https://github.com/microsoft/TypeScript-go/issues/3557) (Closed, `Domain: Parser`, `Needs Investigation`, **sandersn**, **Copilot**)

**Baselines: @satisfies tag handling changes: functions become const declarations**

*Functions annotated with @satisfies now become declare const arrow functions with changed parameter types and added @param/@satisfies annotations*

 * (yesterday) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.0 RC`, and assigned to **sandersn**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3557#issuecomment-4400703648) **sandersn** noted that the .js uses consts with arrow types and emitting as const was correct, explained that the issue repros in the editor, and guessed that the reparser incorrectly attaches `satisfies` to the variable declaration instead of the arrow expression
 * **sandersn** assigned to **Copilot**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3557#issuecomment-4401323163) **sandersn** said "Later: nope it was the other way round. satisfies' synthetic expression blocked the later attachment of param tags."
 * (today) **sandersn** closed the issue

### [Issue microsoft/TypeScript-go#3559](https://github.com/microsoft/TypeScript-go/issues/3559) (Open, `Domain: Declaration Emit`, `Needs Investigation`, **weswigham**)

**Baselines: CJS exports pattern changes in declaration emit**

*CommonJS declaration emit restructuring changed baselines, causing some files to lose exports entirely.*

 * **ahejlsberg** added label `Domain: Declaration Emit`
 * (2 days ago) **RyanCavanaugh** added label `Needs Investigation`, and set milestone to `TypeScript 7.0 RC`
 * **RyanCavanaugh** assigned to **weswigham**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3559#issuecomment-4401208763) **weswigham** said "AFAIK we intentionally no longer bind nested js exports, which is why we also don't traverse them for declarations, unless we've backpedaled on that?"

### [Issue microsoft/TypeScript-go#3560](https://github.com/microsoft/TypeScript-go/issues/3560) (Closed, `Domain: Declaration Emit`, `Needs Investigation`, **weswigham**)

**Baselines: exportNonInitializedVariables crash in declaration emit**

*Declaration emit crashes when exporting non-initialized variables in commonjs module baselines tests.*

 * **ahejlsberg** added label `Domain: Declaration Emit`
 * (2 days ago) **RyanCavanaugh** added label `Needs Investigation`, and set milestone to `TypeScript 7.0 RC`
 * **RyanCavanaugh** assigned to **weswigham**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3562](https://github.com/microsoft/TypeScript-go/issues/3562) (Open, `Domain: Type Checking`, `Needs Investigation`, **sandersn**, **jakebailey**, **Copilot**)

**Baselines: JSDoc module namepath module:A emits as unresolved module instead of any**

*JSDoc module namepath syntax (module:A) now emits an unresolved module rather than any, producing type errors.*

 * (yesterday) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.0 RC`, and assigned to **sandersn**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3562#issuecomment-4400024663) **sandersn** stated that module:X syntax is unsupported and treated as an Unresolved type in Corsa and Strada, argued that module namepaths are rarely used, and noted that proper emission for /** @type {module:A} */ should be A not any
 * (today) **sandersn** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/issues/3562#issuecomment-4400050413) **jakebailey** said "We need to move the baselines into accepted if this is accepted"
 * (today) **jakebailey** reopened the issue
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#3566](https://github.com/microsoft/TypeScript-go/issues/3566) (Open, `Domain: Declaration Emit`, `Needs Investigation`, **weswigham**)

**Baselines: Late\-bound computed property \[prop\] preserved instead of resolved to plain prop**

*Late-bound computed property [prop] syntax is preserved instead of being resolved to plain prop*

 * **ahejlsberg** added label `Domain: Declaration Emit`
 * (2 days ago) **RyanCavanaugh** added label `Needs Investigation`, and set milestone to `TypeScript 7.0 RC`
 * **RyanCavanaugh** assigned to **weswigham**

### [Issue microsoft/TypeScript-go#3567](https://github.com/microsoft/TypeScript-go/issues/3567) (Open, `Domain: Declaration Emit`, `Needs Investigation`, **weswigham**)

**Baselines: Symbol getter/setter declaration emit change**

*Declaration outputs now change the return type of symbol getters/setters to undefined and introduce a new Symbol.toPrimitive overload.*

 * **ahejlsberg** added label `Domain: Declaration Emit`
 * (2 days ago) **RyanCavanaugh** added label `Needs Investigation`, and set milestone to `TypeScript 7.0 RC`
 * **RyanCavanaugh** assigned to **weswigham**

### [Issue microsoft/TypeScript-go#3568](https://github.com/microsoft/TypeScript-go/issues/3568) (Open, `wontfix`, `Domain: Declaration Emit`, **weswigham**, **jakebailey**, **Copilot**)

**Baselines: export as namespace added or restructured in declaration emit**

*Add or restructure ‘export as namespace GLO’ in declaration emit baselines to update module global visibility and public API contract.*

 * **ahejlsberg** added label `Domain: Declaration Emit`
 * (2 days ago) **RyanCavanaugh** added label `Needs Investigation`, and set milestone to `TypeScript 7.0 RC`
 * **RyanCavanaugh** assigned to **weswigham**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3568#issuecomment-4400950930) **weswigham** rated the issue as wontfix and explained that the erroneous input should remain in the output because Strada only skipped it due to traversal constraints
 * (today) **weswigham** closed the issue
 * (today) **weswigham** added label `wontfix`, and removed label `Needs Investigation`
 * [today](https://github.com/microsoft/TypeScript-go/issues/3568#issuecomment-4400976797) **jakebailey** said "We need to move the baselines to accepted if this is not a real issue"
 * (today) **jakebailey** reopened the issue
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#3569](https://github.com/microsoft/TypeScript-go/issues/3569) (Open, `Domain: Declaration Emit`, `Needs Investigation`, **weswigham**)

**Baselines: Declaration emit simplification of class extending built\-in Array**

*Declaration emit now simplifies classes extending built-in Array by dropping the generic parameter and removing inherited constructor overloads.*

 * **ahejlsberg** added label `Domain: Declaration Emit`
 * (2 days ago) **RyanCavanaugh** added label `Needs Investigation`, and set milestone to `TypeScript 7.0 RC`
 * **RyanCavanaugh** assigned to **weswigham**

### [PR microsoft/TypeScript-go#3575](https://github.com/microsoft/TypeScript-go/pull/3575) (Closed)

**Avoid over\-expanding recursive constraints in \`getBaseSignature\`**

*Prevent excessive expansion of recursive type constraints in the getBaseSignature function.*

 * created by **Andarist**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3575#issuecomment-4392766649) **ahejlsberg** said "Looks like we need conformance/genericFunctionParameters.js.diff removed from submoduleTriaged.txt."
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * (later) **Andarist** closed the issue

### [PR microsoft/TypeScript-go#3578](https://github.com/microsoft/TypeScript-go/pull/3578) (Closed)

**Preserve JSDoc parameter types on functions wrapped by \`@satisfies\`**

*Functions wrapped by @satisfies currently lose their JSDoc parameter types and require preservation.*

 * created by **Andarist**
 * [later](https://github.com/microsoft/TypeScript-go/pull/3578#issuecomment-4406755071) **sandersn** said "Sorry, didn't see this yesterday because I was moving too fast. #3746 is basically this PR but slightly easier to read."
 * (later) **sandersn** closed the issue

### [Issue microsoft/TypeScript-go#3588](https://github.com/microsoft/TypeScript-go/issues/3588) (Closed, **jakebailey**, **Copilot**)

**Behaviour differences observed when varying tsconfig option key letter cases randomly**

*Lowercasing tsconfig compilerOptions keys causes unknown option and build-only errors in TypeScript 6.0*

 * (1 week ago) **jakebailey** assigned to **Copilot**, **jakebailey**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3589](https://github.com/microsoft/TypeScript-go/pull/3589) (Closed, **jakebailey**, **Copilot**)

**Make tsconfig option name lookup case\-sensitive with "Did you mean" suggestions**

*Enable case-sensitive tsconfig option name lookup with "Did you mean" suggestions and remove redundant nil checks.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3589#issuecomment-4318121984) **hkleungai** said "Is it possible to make tsgo throw TS5025 instead of TS5023 in this case? 🤔 "
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3589#issuecomment-4318145199) **jakebailey** said "@copilot look into the above, as a "did you mean" is preferred "
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3589#issuecomment-4318172881) **Copilot** updated the implementation to emit TS5025 "Did you mean" diagnostics for case-insensitive matches and added support helpers
 * [today](https://github.com/microsoft/TypeScript-go/pull/3589#issuecomment-4400172944) **jakebailey** said "@copilot please address review comments"
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3596](https://github.com/microsoft/TypeScript-go/issues/3596) (Closed, `Needs Investigation`, **andrewbranch**, **Copilot**)

**TS2883 regression in \-\-build with project references on inferred export from referenced package**

*tsgo --build now fails with TS2883 on inferred exports referencing types from a project-referenced package in a pnpm monorepo*

 * (yesterday) **RyanCavanaugh** added label `Needs Investigation`, and set milestone to `TypeScript 7.0 RC`
 * **andrewbranch** assigned to **Copilot**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3596#issuecomment-4400739781) **andrewbranch** explained why Corsa intentionally differs from Strada in symlink detection and declaration emit portability errors and noted that the behavior aligns with Strada's intended design
 * [today](https://github.com/microsoft/TypeScript-go/issues/3596#issuecomment-4400823285) **andrewbranch** described the intended user-side fix to unhide `types.ts` by updating tsconfig.json paths or package.json exports
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#3597](https://github.com/microsoft/TypeScript-go/issues/3597) (Closed, **jakebailey**, **Copilot**)

**Broken JSDoc codeblock parsing**

*JSDoc fenced code blocks with embedded tags like @Embed are misparsed by tsgo, producing incorrect HTML rendering.*

 * (1 week ago) **jakebailey** assigned to **Copilot**, **jakebailey**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3598](https://github.com/microsoft/TypeScript-go/pull/3598) (Closed, **jakebailey**, **Copilot**)

**Fix JSDoc codeblock parsing: preserve fenced code block state across newlines**

*Update JSDoc parser to preserve fenced code block state across newlines and pass related tests*

 * **Copilot** assigned to **jakebailey**
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3598#issuecomment-4316990736) **jakebailey** said "@copilot+claude-opus-4.6 This PR should have a hover test."
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3598#issuecomment-4317058374) **Copilot** added a fourslash hover test in quickInfoJSDocCodefenceAtSign_test.go to verify that @ symbols inside fenced code blocks render as literal text and that @param after the closing fence is parsed as a JSDoc tag
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3617](https://github.com/microsoft/TypeScript-go/issues/3617) (Open, `Needs Investigation`, **iisaduan**)

**fix: FindBestPatternMatch incorrectly allows wildcard pattern to override exact match**

*FindBestPatternMatch misuses StarIndex so exact matches set longestMatchPrefixLength to -1, allowing later wildcard patterns to override exact matches.*

 * (2 days ago) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.0 RC`, and assigned to **iisaduan**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3617#issuecomment-4401880065) **RyanCavanaugh** said "@kuishou68 how does this manifest? There's no external-visible behavorial description nor testcase in that PR, so it's hard to know the severity/priority of this"

### [PR microsoft/TypeScript-go#3619](https://github.com/microsoft/TypeScript-go/pull/3619) (Open)

**perf: Make \`NodeArray\` no longer inherit from \`Array\`**

*Detach NodeArray from Array prototype to prevent direct array method usage and achieve significant performance gains.*

 * created by **liuxingbaoyu**
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3619#issuecomment-4329156551) **andrewbranch** asked what made inheriting from Array expensive for materialization and guessed it was due to removing numeric index getters
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3619#issuecomment-4329869917) **liuxingbaoyu** said "Yes, the issue is that Object.defineProperty is slow."
 * **RyanCavanaugh** added to milestone `Post-7.0`

### [PR microsoft/TypeScript-go#3624](https://github.com/microsoft/TypeScript-go/pull/3624) (Closed, **RyanCavanaugh**, **Copilot**)

**Elide bare side\-effect imports in JS declaration emit**

*Omit bare side-effect imports from JS file .d.ts outputs while preserving them for TS files.*

 * created by **Copilot**
 * (1 week ago) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#3630](https://github.com/microsoft/TypeScript-go/pull/3630) (Open, **DanielRosenwasser**, **Copilot**)

**Fix formatting failure when whitespace\-only line exists between single\-line comments**

*A whitespace-only line between single-line comments causes the formatter to produce overlapping delete edits due to unguarded startPos updates.*

 * (1 week ago) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3630#issuecomment-4331257440) **Copilot** reported the fix in commit 22e4165a by replacing the compiler test with a fourslash formatting test
 * [today](https://github.com/microsoft/TypeScript-go/pull/3630#issuecomment-4400770306) **DanielRosenwasser** said "@copilot investigate and make sure we are testing variations of TrimTrailingWhitespace for this"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3630#issuecomment-4400890083) **Copilot** added a test variant that disables TrimTrailingWhitespace and verified whitespace preservation; confirmed both variations pass

### [Issue microsoft/TypeScript-go#3645](https://github.com/microsoft/TypeScript-go/issues/3645) (Closed, `Domain: Editor`, `Crash`, **andrewbranch**, **Copilot**)

**Auto\-imports for JSX tag trigger assertion violation when React is type\-imported\.**

*Automatic JSX tag imports crash with an assertion violation when React is imported only as a type*

 * (6 days ago) **andrewbranch** added labels `Domain: Editor`, `Crash`, and set milestone to `TypeScript 7.0 RC`
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#3650](https://github.com/microsoft/TypeScript-go/pull/3650) (Closed, **DanielRosenwasser**, **Copilot**)

**Fix assertion violation in auto\-imports for JSX tag when React is type\-imported**

*Refactor symbol import logic to handle type-only React imports and prevent JSX auto-import assertion failures.*

 * [6 days ago](https://github.com/microsoft/TypeScript-go/pull/3650#issuecomment-4361646191) **andrewbranch** said "@copilot ^"
 * [6 days ago](https://github.com/microsoft/TypeScript-go/pull/3650#issuecomment-4361828952) **andrewbranch** suggested modifying getSymbolNamesToImport to return richer info and described handling of type-only imports to avoid duplicates or improve correlation
 * [6 days ago](https://github.com/microsoft/TypeScript-go/pull/3650#issuecomment-4361891178) **Copilot** refactored getSymbolNamesToImport to return symbolNameInfo with name and isTypeOnly fields, adjusted type-only and auto-import filters, reverted needsJsxNamespaceFix, and included component name when type-only
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#3664](https://github.com/microsoft/TypeScript-go/pull/3664) (Closed)

**Align dependency symlink handling with TS6 for module specifiers**

*Align tsgo’s dependency symlink cache with TypeScript 6 by using normal module resolution to respect paths mappings in declaration emits.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3664#issuecomment-4347464727) **kbrooks** agreed with the policy service and indicated affiliation with Snap Inc.
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3664#issuecomment-4347528448) **kbrooks** agreed to policy request and specified company as Snap Inc.
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3664#issuecomment-4393623807) **kbrooks** asked for someone to review when they had bandwidth
 * [today](https://github.com/microsoft/TypeScript-go/pull/3664#issuecomment-4400050597) **andrewbranch** explained that the proposed approach was off track due to design requirements for symlink discovery and stated he would take over the fix
 * [today](https://github.com/microsoft/TypeScript-go/pull/3664#issuecomment-4400267500) **kbrooks** said "Ok thanks for taking the time to look at it. "
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#3670](https://github.com/microsoft/TypeScript-go/pull/3670) (Open, **johnfav03**)

**Watcher build mode efficiency updates**

*Refactors tsc --build --watch to use a shared FileWatcher and trackingVFS structure, reducing code duplication and redundant dependency scanning.*

 * created by **johnfav03**
 * (today) **RyanCavanaugh** set milestone to `TypeScript 7.0 RC`, and assigned to **johnfav03**

### [PR microsoft/TypeScript-go#3703](https://github.com/microsoft/TypeScript-go/pull/3703) (Open, **jakebailey**)

**Fixes to \-\-generateTrace to make analyze\-trace work**

*Fix the --generateTrace option to ensure analyze-trace functions correctly.*

 * created by **jakebailey**
 * (today) **RyanCavanaugh** set milestone to `Possible Improvement`, and assigned to **jakebailey**

### [Issue microsoft/TypeScript-go#3719](https://github.com/microsoft/TypeScript-go/issues/3719) (Open, `bug`, **iisaduan**)

**Support localized user\-facing strings in VS Code extension**

*Add localization support by moving user-facing strings into package.nls.json and using vscode-l10n tools.*

 * created by **DanielRosenwasser**
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/3719#issuecomment-4383830006) **jakebailey** said "You mean for extension strings, right?"
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * (today) **RyanCavanaugh** added label `bug`, and assigned to **iisaduan**

### [Issue microsoft/TypeScript-go#3722](https://github.com/microsoft/TypeScript-go/issues/3722) (Open, `Domain: Editor`, **jakebailey**, **Copilot**)

**custom tsgo path is now ignored**

*VS Code's TypeScript native-preview ignores the configured custom tsgo path and launches its bundled tsgo instead.*

 * created by **loynoir**
 * **loynoir** added label `Domain: Editor`
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#3723](https://github.com/microsoft/TypeScript-go/pull/3723) (Closed, **RyanCavanaugh**, **Copilot**)

**Fix nil pointer in transformExpandoAssignment for element access expressions**

*Replace left.Name().Text() with the computed property variable to prevent nil pointer panics on JS expando element access assignments.*

 * created by **Copilot**
 * (yesterday) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3727](https://github.com/microsoft/TypeScript-go/issues/3727) (Open, `Domain: Editor`, `possible improvement`)

**Unify tsdk between built\-in and native preview extensions**

*Share the built-in tsdk setting with the native preview and choose the TypeScript server based on useTsGo and tsdk directory.*

 * (yesterday) **RyanCavanaugh** added labels `possible improvement`, `Domain: Editor`, and set milestone to `Possible Improvement`
 * [today](https://github.com/microsoft/TypeScript-go/issues/3727#issuecomment-4399622023) **DanielRosenwasser** said "We may need some sort of marker file to tell us "this is a TS7 directory"."

### [PR microsoft/TypeScript-go#3728](https://github.com/microsoft/TypeScript-go/pull/3728) (Open)

**Fix keyof deferred for non\-generic substitution types \(\#2186\)**

*Resolve keyof immediately for non-generic substitution types, fixing indexed access assignability and unsimplified quick info.*

 * created by **adavila0703**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3728#issuecomment-4390943530) **adavila0703** quoted the Contributor License Agreement and instructions for agreeing
 * [today](https://github.com/microsoft/TypeScript-go/pull/3728#issuecomment-4402998409) **jakebailey** said "If this fixes #2186, can you write "Fixes #2186" in the description?"

### [PR microsoft/TypeScript-go#3730](https://github.com/microsoft/TypeScript-go/pull/3730) (Closed, **andrewbranch**, **Copilot**)

**Fix TS2883 regression in \-\-build with project references on inferred export from non\-index file**

*Add fallback module specifier generation in --build to prevent TS2883 errors for inferred types from non-index files in project references*

 * created by **Copilot**
 * (yesterday) **Copilot** assigned to **Copilot**, **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#3732](https://github.com/microsoft/TypeScript-go/pull/3732) (Closed)

**fix\(3560\): fix nested export variable transformation in if/labeled statements**

*Correct nested export variable transformation in if and labeled statements.*

 * created by **a-tarasyuk**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3734](https://github.com/microsoft/TypeScript-go/issues/3734) (Open, `Crash`, `Needs More Info`)

**Entering "ai\.messages\.find\(m =\> m\.\)" will cause the language server to crash\.**

*Typing ai.messages.find(m => m.) triggers an internal token-end mismatch panic that crashes the language server*

 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * [today](https://github.com/microsoft/TypeScript-go/issues/3734#issuecomment-4399058775) **RyanCavanaugh** reported inability to reproduce the issue and requested the content of ai.ts
 * (today) **RyanCavanaugh** added label `Needs More Info`, removed from milestone `TypeScript 7.0 RC`, and unassigned **jakebailey**, **Copilot**
 * [later](https://github.com/microsoft/TypeScript-go/issues/3734#issuecomment-4405918795) **ShenHongFei** reported that they couldn't reproduce the issue in a new project, noted the crash occurred when entering "m." possibly due to monaco-editor import, and said they would provide a reproducible example
 * [later](https://github.com/microsoft/TypeScript-go/issues/3734#issuecomment-4406047516) **ShenHongFei** attempted to reproduce the issue in a new project with monaco-editor 0.55.1 but couldn’t, gave up and decided to avoid using “m.”

### [Issue microsoft/TypeScript-go#3735](https://github.com/microsoft/TypeScript-go/issues/3735) (Closed)

**Behavior difference: tsgo fails to emit error on class field's unmatched params between jsdoc & js code**

*tsgo reports unmatched JSDoc '@param' errors for methods but not for class field arrow functions, unlike TypeScript.*

 * [today](https://github.com/microsoft/TypeScript-go/issues/3735#issuecomment-4398617779) **a-tarasyuk** said "@hkleungai could you add simplified repro? Thanks "
 * [today](https://github.com/microsoft/TypeScript-go/issues/3735#issuecomment-4398629943) **hkleungai** said "Sorry just notice that. "
 * [today](https://github.com/microsoft/TypeScript-go/issues/3735#issuecomment-4398645120) **a-tarasyuk** said "Thanks, I’ll check the issue "
 * (later) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#3736](https://github.com/microsoft/TypeScript-go/pull/3736) (Closed, **jakebailey**, **Copilot**)

**Investigate format crash during auto\-import completion resolve**

*Resolving auto-import completions crashes the Go language server due to assertion failures from mutated node positions during formatting*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3737](https://github.com/microsoft/TypeScript-go/pull/3737) (Closed)

**fix\(3735\): fix unmatched jsdoc param errors missing for arrow function class fields**

*Add missing unmatched JSDoc parameter error reporting for arrow function class fields.*

 * created by **a-tarasyuk**
 * (later) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#3738](https://github.com/microsoft/TypeScript-go/pull/3738) (Open, **gabritto**, **Copilot**)

**Implement pre\-emit/post\-emit diagnostic count mismatch detection \(TS\-1\)**

*Implement TS-1 diagnostic in Go test harness to detect and report mismatches between pre-emit and post-emit diagnostic counts.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **gabritto**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3738#issuecomment-4400192625) **jakebailey** said "I think this is technically a dupe of #1301 but it's been a while so I think we don't need some of the fixes in that PR?"

### [Issue microsoft/TypeScript-go#3739](https://github.com/microsoft/TypeScript-go/issues/3739) (Open, **ahejlsberg**)

**Behavior difference: Variable with type \`{}\` can be "wrongly" assigned to Record in tsgo but not in tsc**

*tsgo does not report errors when assigning {} to typed Record<string, ...> types in JavaScript, whereas tsc correctly flags the type mismatch.*

 * created by **hkleungai**
 * **ahejlsberg** assigned to **ahejlsberg**

### [PR microsoft/TypeScript-go#3740](https://github.com/microsoft/TypeScript-go/pull/3740) (Closed, **sandersn**, **Copilot**)

**Fix tsconfig/jsconfig priority for JS files when both configs coexist in same directory**

*Fix config file resolution to detect jsconfig.json for JavaScript files in directories containing both tsconfig.json and jsconfig.json.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **sandersn**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#3741](https://github.com/microsoft/TypeScript-go/pull/3741) (Open)

**Only transform expando assignments that wont be represented elsewhere in the emit already**

*Ensure expando property assignments are only transformed when not already emitted elsewhere*

 * created by **weswigham**

### [Issue microsoft/TypeScript-go#3742](https://github.com/microsoft/TypeScript-go/issues/3742) (Open)

**Behavior difference: tsgo skip reporting invalid jsdoc type when param is missing from function signature**

*tsgo omits the generic type argument error for invalid JSDoc types when a @param name is missing from the function signature, unlike tsc.*

 * created by **hkleungai**

### [PR microsoft/TypeScript-go#3743](https://github.com/microsoft/TypeScript-go/pull/3743) (Closed)

**Add missing parens in type serializer**

*Add missing parentheses in the type serializer to correctly format serialized types.*

 * created by **weswigham**
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript-go#3744](https://github.com/microsoft/TypeScript-go/pull/3744) (Closed)

**Change parsing precedence for JSDoc prefix \`?\` and \`\!\` operators**

*Bind JSDoc `?` and `!` prefixes tighter than unions and intersections, disallowing standalone `?` and permitting `!` before types.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#3745](https://github.com/microsoft/TypeScript-go/pull/3745) (Open)

**Add missing type argument count sanity check to handle nodes from js …**

*Add a missing sanity check to validate type argument counts for JavaScript-derived builtin aliases like Array and Promise*

 * created by **weswigham**

### [PR microsoft/TypeScript-go#3746](https://github.com/microsoft/TypeScript-go/pull/3746) (Closed, **sandersn**, **Copilot**)

**Fix @satisfies tag preventing @param types from being applied to arrow functions**

*Unwrap @satisfies expressions in JSDoc and update function detection so @param annotations apply correctly to arrow functions.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **sandersn**
 * (today) **sandersn** closed the issue

### [Issue microsoft/TypeScript-go#3747](https://github.com/microsoft/TypeScript-go/issues/3747) (Open)

**Regression in 20260506\.1: generic substitution lost through method\-returned mapped type**

*tsgo CLI in version 7.0.0-dev.20260506.1 incorrectly loses generic substitutions for method-returned mapped types, defaulting to constraint defaults.*

 * created by **Apollon77**
 * [later](https://github.com/microsoft/TypeScript-go/issues/3747#issuecomment-4404886819) **Andarist** said "Please prepare a self-contained repro that somebody could investigate. This kind of an issue should be easily reproducible with code fitting a TS playground."

### [Issue microsoft/TypeScript-go#3748](https://github.com/microsoft/TypeScript-go/issues/3748) (Open)

**Behavior difference: type testing, order**

*Migrating to tsgo caused the order of union and object type members to differ from TypeScript's output.*

 * created by **terrablue**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3748#issuecomment-4401108029) **jakebailey** said "This is not guaranteed, and you should see the same if you use 6.0 and pass --stableTypeOrdering."

### [PR microsoft/TypeScript-go#3749](https://github.com/microsoft/TypeScript-go/pull/3749) (Closed)

**Don't hold snapshotUpdateMu while running GC\(\)**

*Avoid holding the snapshotUpdateMu lock during garbage collection to prevent minor performance slowdowns.*

 * created by **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3749#issuecomment-4401373186) **andrewbranch** said "We don't recover from panics that happen during snapshot updates anyway 🤷 "
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#3750](https://github.com/microsoft/TypeScript-go/issues/3750) (Open, `possible improvement`)

**Experiment with alternative values of \`GOGC\`**

*Evaluate how different GOGC settings affect compile times, language server responsiveness, and peak memory usage.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** added label `possible improvement`, and set milestone to `Possible Improvement`

### [PR microsoft/TypeScript-go#3751](https://github.com/microsoft/TypeScript-go/pull/3751) (Open, **gabritto**, **Copilot**)

**Implement checkExternalEmitHelpers for tslib helper validation**

*Implement checkExternalEmitHelpers and its supporting logic for tslib helper validation, exclude certain built-in helpers, and refresh baselines.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **gabritto**

### [PR microsoft/TypeScript-go#3752](https://github.com/microsoft/TypeScript-go/pull/3752) (Closed)

**Update vscode\-tas\-client\.**

*Upgrade the vscode-tas-client package now that PR 102 has been merged and published.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** closed the issue

### [Issue microsoft/TypeScript-go#3753](https://github.com/microsoft/TypeScript-go/issues/3753) (Open)

**Missing error for non\-existent root files**

*tsgo silently ignores missing root files specified in tsconfig.json instead of reporting an error.*

 * created by **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3753#issuecomment-4401709100) **DanielRosenwasser** said "Found from https://github.com/microsoft/typescript-go/issues/3376"

### [Issue microsoft/TypeScript-go#3754](https://github.com/microsoft/TypeScript-go/issues/3754) (Closed, **DanielRosenwasser**)

**Crash when async functions return non\-PromiseLike thenables\.**

*Returning a non-PromiseLike thenable from an async function triggers a nil pointer dereference crash in the TypeScript-Go checker.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** set milestone to `TypeScript 7.0 RC`, and assigned to **DanielRosenwasser**
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#3755](https://github.com/microsoft/TypeScript-go/pull/3755) (Closed)

**Port missing \`nil\` check in \`getContextualTypeForReturnExpression\`**

*Port a missing nil check into getContextualTypeForReturnExpression to fix potential nil dereference.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#3756](https://github.com/microsoft/TypeScript-go/pull/3756) (Closed)

**Accept JS declaration emit preserving side effect imports**

*Enable JavaScript declaration file emission while preserving side-effect imports.*

 * created by **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#3757](https://github.com/microsoft/TypeScript-go/issues/3757) (Open, **jakebailey**, **Copilot**)

**Declaration emit renames a method's shadowed type parameter to the outer class generic \(\`Table\` \-\> \`Table\_1\`\)**

*Declaration emit incorrectly renames a method’s shadowed type parameter to the outer class generic, resulting in incorrect .d.ts return types.*

 * created by **Cellule**
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#3758](https://github.com/microsoft/TypeScript-go/issues/3758) (Open)

**File argument of \`@\` crashes CLI**

*Providing `@` with no file path to tsgo crashes the CLI with a “path "" is not absolute” panic.*

 * created by **DanielRosenwasser**

### [Issue microsoft/TypeScript-go#3759](https://github.com/microsoft/TypeScript-go/issues/3759) (Closed, `Crash`, **DanielRosenwasser**)

**Crash for array destructuring under noUncheckedIndexedAccess & noLib**

*Array destructuring under noUncheckedIndexedAccess and noLib causes the TypeScript compiler to crash.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** added label `Crash`, set milestone to `TypeScript 7.0 RC`, and assigned to **DanielRosenwasser**
 * (today) **DanielRosenwasser** closed the issue

