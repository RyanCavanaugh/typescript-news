# Report for 2026-05-05 (Tuesday, May 5th, 2026)

19 different users commented on 84 different issues.

## Recommended Actions

 * Response Recommended
    * @Jelcoo asked if there's a manual way to take a profile in [microsoft/TypeScript-go#3692](https://github.com/microsoft/TypeScript-go/issues/3692#issuecomment-4385893760)
    * @GrygrFlzr provided reproduction steps and commit range for the error in [microsoft/TypeScript-go#3709](https://github.com/microsoft/TypeScript-go/issues/3709#issuecomment-4381470213)

## Activity Summary

### [Issue microsoft/TypeScript-go#1570](https://github.com/microsoft/TypeScript-go/issues/1570) (Closed, `bug`, `Domain: Declaration Emit`, **weswigham**)

**Nondeterministic declaration emit in test nodeModulesExportsSourceTs**

*The nodeModulesExportsSourceTs (nodenext) test’s baseline comparison is failing due to nondeterministic declaration file emits that omit inner module .d.ts files.*

 * **jakebailey** added label `Domain: Declaration Emit`
 * (5 weeks ago) **RyanCavanaugh** set milestone to `TypeScript 7.0 RC`, and assigned to **weswigham**
 * [today](https://github.com/microsoft/TypeScript-go/issues/1570#issuecomment-4382165914) **weswigham** asked if the failure has reoccurred since and reported no reproductions under extended race testing, suggesting recent concurrency fixes may have resolved it
 * (today) **weswigham** closed the issue

### [Issue microsoft/TypeScript-go#2328](https://github.com/microsoft/TypeScript-go/issues/2328) (Closed, `bug`, **weswigham**, **Copilot**)

**Declaration emit with \`\-\-noResolve\` differs from tsc**

*tsgo incorrectly emits ‘any’ for default exports under --noResolve whereas tsc preserves the original types.*

 * (3 weeks ago) **RyanCavanaugh** added label `bug`, set milestone to `TypeScript 7.0 RC`, and assigned to **weswigham**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2328#issuecomment-4382039264) **weswigham** said "This either got fixed in #2459 or a followup PR because it no longer repros."
 * (today) **weswigham** closed the issue

### [Issue microsoft/TypeScript-go#2522](https://github.com/microsoft/TypeScript-go/issues/2522) (Closed, `Domain: Declaration Emit`, `Crash`, **weswigham**)

**Reexporting @types/micromatch@4\.0\.10 from a \.cjs file crashes**

*Re-exporting @types/micromatch@4.0.10 from a .cjs file crashes the TypeScript declaration transformer with a ‘Diagnostic emitted without context’ panic.*

 * (3 weeks ago) **RyanCavanaugh** set milestone to `TypeScript 7.0 RC`, and unassigned **jakebailey**, **Copilot**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2522#issuecomment-4382238147) **weswigham** said "Aside from the long-fixed panic, the new error mentioned doesn't repro anymore. Presumably this was fixed by #3449 properly enabling node reuse of the type annotation on the let."
 * (today) **weswigham** closed the issue

### [Issue microsoft/TypeScript-go#3318](https://github.com/microsoft/TypeScript-go/issues/3318) (Open, `Domain: Editor`, **iisaduan**)

**Missing \`addMissingImports\` code action/code fix**

*VSCode’s editor.codeActionOnSave lacks implementation of TypeScript’s addMissingImports code action and code fix.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3318#issuecomment-4373717770) **iisaduan** described the addition of the 'fix all autoimports' functionality via PR 3382 and asked which trigger methods were relied on
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3318#issuecomment-4373817264) **dhoulb** described that code actions on save no longer automatically add missing imports, causing red squiggles and manual steps and lamented the loss of the previous smooth workflow
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3318#issuecomment-4374763168) **iisaduan** noted that the behavior would resume with the old configuration after naming fixes and suggested adding editor.codeActionsOnSave.source.fixAll set to always or explicit to replicate it now
 * [today](https://github.com/microsoft/TypeScript-go/issues/3318#issuecomment-4383894046) **dhoulb** said "That's amazing, thanks so much @iisaduan — can confirm I tested and it worked."

### [Issue microsoft/TypeScript-go#3338](https://github.com/microsoft/TypeScript-go/issues/3338) (Open, `possible improvement`, **mjbvz**)

**TSGO: command 'typescript\.restartTsServer' not found**

*Enabling the TypeScript native preview feature in VSCode 1.113.0 removes the 'typescript.restartTsServer' command.*

 * **RyanCavanaugh** added label `possible improvement`
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/3338#issuecomment-4268557698) **jeff-computers** said "@jakebailey thank you kindly - in the meantime how should we trigger a restart?"
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/3338#issuecomment-4268631646) **sbetav** mentioned a specific command to restart the TypeScript Go server
 * [later](https://github.com/microsoft/TypeScript-go/issues/3338#issuecomment-4388148710) **Elagoht** said "@sbetav thanks!"

### [Issue microsoft/TypeScript-go#3405](https://github.com/microsoft/TypeScript-go/issues/3405) (Open, `Domain: Editor`, **jakebailey**, **Copilot**)

**JSDoc disapprears after type calculation**

*Hovering over a parameter from an intersection type no longer shows its JSDoc comment after TS type calculation.*

 * **Withered-Flower-0422** added label `Domain: Editor`
 * (3 weeks ago) **jakebailey** assigned to **Copilot**, **jakebailey**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [Issue microsoft/TypeScript-go#3406](https://github.com/microsoft/TypeScript-go/issues/3406) (Closed, `Crash`)

**Unbounded memory and unbounded CPU leads to OOM or crashes container**

*Build process consumes all available CPU and memory, causing container OOM errors or SIGTERM failures.*

 * created by **sroussey**
 * **sroussey** added label `Crash`
 * [today](https://github.com/microsoft/TypeScript-go/issues/3406#issuecomment-4383399093) **RyanCavanaugh** said "I'm guessing this was a stack overflow that has since been fixed. Please log a new issue with a repro if possible. Thanks!"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#3413](https://github.com/microsoft/TypeScript-go/issues/3413) (Open, `Domain: JS`, `Domain: Parser`, **ahejlsberg**)

**\`?\` can be used as a standalone JSDoc type when followed by \`\|\`**

*? used standalone in JSDoc unions is treated as null or never, resulting in unexpected type inference.*

 * (2 weeks ago) **DanielRosenwasser** added labels `Domain: Parser`, `Domain: JS`, and assigned to **ahejlsberg**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [Issue microsoft/TypeScript-go#3448](https://github.com/microsoft/TypeScript-go/issues/3448) (Closed)

**\[ServerErrors\]\[JavaScript\] main vs **

*Pipeline analysis of main across 300 popular TypeScript repositories reported server errors, clone failures, timeouts, and other failures.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/3448#issuecomment-4283766524) **typescript-bot** reported that the server connection closed prematurely and supplied error details and repro steps for usebruno/bruno
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/3448#issuecomment-4283766646) **typescript-bot** reported that the server connection closed prematurely with undefined error and provided logs for mui/material-ui
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/3448#issuecomment-4283766710) **typescript-bot** reported a panic handling request textDocument/diagnostic due to runtime error: invalid memory address or nil pointer dereference
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#3475](https://github.com/microsoft/TypeScript-go/issues/3475) (Open)

**Test harness doesn't report errors from unrecognized compiler options**

*The test harness fails to report errors for unrecognized compiler options, resulting in empty error outputs.*

 * created by **RyanCavanaugh**
 * **RyanCavanaugh** added to milestone `Post-7.0`

### [Issue microsoft/TypeScript-go#3476](https://github.com/microsoft/TypeScript-go/issues/3476) (Open, `Needs Investigation`, **gabritto**)

**No error reported when tslib helpers aren't found**

*The TypeScript compiler fails to report errors when tslib helper functions are missing, causing undetected issues.*

 * created by **RyanCavanaugh**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.0 RC`, and assigned to **gabritto**

### [Issue microsoft/TypeScript-go#3477](https://github.com/microsoft/TypeScript-go/issues/3477) (Open, `Needs Investigation`, **weswigham**)

**Remaining diffs in isolatedDeclarations**

*Remaining differences in isolatedDeclarations have been identified in submoduleTriaged.txt and await an upcoming PR.*

 * created by **RyanCavanaugh**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.0 RC`, assigned to **RyanCavanaugh**, **weswigham**, and unassigned **RyanCavanaugh**

### [Issue microsoft/TypeScript-go#3478](https://github.com/microsoft/TypeScript-go/issues/3478) (Open)

**Wasm build**

*Request for a WebAssembly build of tsgo to enable experimentation in the online playground.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/3478#issuecomment-4291015910) **jakebailey** said "Eventually, but I would be interested in knowing exactly what you're looking for, as everyone wants Wasm differently."
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/3478#issuecomment-4291489874) **justinfagnani** described maintaining several TypeScript-based browser projects, notably lit.dev/playground, which compiles code, retrieves diagnostics, and uses language service APIs without custom transforms, and mentioned assuming that custom transforms would require a custom binary
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/3478#issuecomment-4291509836) **jakebailey** noted that integrating the language server with Monaco and enabling API access entailed many moving parts, including process access and a full JS API
 * **RyanCavanaugh** added to milestone `Post-7.0`

### [Issue microsoft/TypeScript-go#3479](https://github.com/microsoft/TypeScript-go/issues/3479) (Open, `Needs Investigation`, **andrewbranch**)

**Untriaged differences in self\-package resolution \(possibly test harness only\)**

*Untriaged differences in TypeScript self-package resolution tests for NodeNext import mode and outDir scenarios possibly originate from the test harness.*

 * created by **RyanCavanaugh**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.0 RC`, and assigned to **andrewbranch**

### [Issue microsoft/TypeScript-go#3491](https://github.com/microsoft/TypeScript-go/issues/3491) (Open, **ahejlsberg**)

**Excess\-property check fires on a nested object literal that is later assigned to an annotated return type, where tsc 6\.0 does not**

*TS7 incorrectly flags excess-property errors on nested object literals assigned via an untyped variable to a typed return, unlike TS6*

 * created by **tomquist**
 * **ahejlsberg** assigned to **ahejlsberg**
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/3491#issuecomment-4296214357) **Andarist** described having a fix for the issue, provided sample code illustrating the problem, and reconsidered when to call getWidenedType before submitting the PR
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [Issue microsoft/TypeScript-go#3520](https://github.com/microsoft/TypeScript-go/issues/3520) (Closed, **jakebailey**, **Copilot**)

**\`isolatedDeclarations\` with arrow functions that have default parameters**

*Using isolatedDeclarations with arrow functions that have default parameters in TSGo 7.0 causes declaration emit errors requiring explicit type annotations.*

 * created by **walkerburgin**
 * (1 week ago) **jakebailey** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3521](https://github.com/microsoft/TypeScript-go/pull/3521) (Closed, **jakebailey**, **Copilot**)

**Fix isolatedDeclarations errors for arrow functions with default parameters**

*Fix isolatedDeclarations errors and optimize performance by improving pseudochecker default parameter handling and undefined recognition for arrow functions*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3521#issuecomment-4308730391) **Copilot** resolved the reported issues by adding lastRequiredParamIndex to precompute the last required parameter’s position for O(1) lookups and updated typeFromParameter, cloneParameters, and the untyped-initializer branch accordingly
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3521#issuecomment-4308776401) **jakebailey** said "@copilot+claude-opus-4.6 continue addressing comments"
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3521#issuecomment-4308858686) **Copilot** addressed remaining comments by fixing the `lastRequiredParamIndex` doc comment and adding an early-return fast path in `typeFromParameter`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3542](https://github.com/microsoft/TypeScript-go/issues/3542) (Open, `Domain: Declaration Emit`, `Needs Investigation`, **weswigham**)

**Baselines: JS declaration emit adds \`export import\` modifier for require\-style import assignments**

*JS declaration emit adds export import modifiers to require-style assignments, changing the public API by exposing internal imports.*

 * created by **RyanCavanaugh**
 * **ahejlsberg** added label `Domain: Declaration Emit`
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and set milestone to `TypeScript 7.0 RC`

### [Issue microsoft/TypeScript-go#3543](https://github.com/microsoft/TypeScript-go/issues/3543) (Open, `Domain: Declaration Emit`, `Needs Investigation`, **weswigham**)

**Baselines: CJS \`module\.exports = {}\` now emits \`export = \_default\` with inlined object type instead of named exports**

*CJS module.exports patterns now emit export = _default with inlined object types instead of named exports, requiring semantic validation*

 * created by **RyanCavanaugh**
 * **ahejlsberg** added label `Domain: Declaration Emit`
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and set milestone to `TypeScript 7.0 RC`

### [Issue microsoft/TypeScript-go#3544](https://github.com/microsoft/TypeScript-go/issues/3544) (Open, `Domain: Declaration Emit`, `Needs Investigation`, **weswigham**)

**Baselines: CJS class expression exports emit anonymous constructor types instead of named class declarations**

*CJS class expression exports emit anonymous constructor types in .d.ts files, producing malformed import types and TypeScript errors.*

 * created by **RyanCavanaugh**
 * **ahejlsberg** added label `Domain: Declaration Emit`
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and set milestone to `TypeScript 7.0 RC`

### [Issue microsoft/TypeScript-go#3545](https://github.com/microsoft/TypeScript-go/issues/3545) (Open, `Domain: Declaration Emit`, `Needs Investigation`, **weswigham**)

**Baselines: CJS export alias and element access patterns changed**

*Declaration output now differs for CommonJS export aliases and module.exports element access patterns, including duplicate assignments.*

 * created by **RyanCavanaugh**
 * **ahejlsberg** added label `Domain: Declaration Emit`
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and set milestone to `TypeScript 7.0 RC`

### [Issue microsoft/TypeScript-go#3547](https://github.com/microsoft/TypeScript-go/issues/3547) (Open, `Domain: Declaration Emit`, `Needs Investigation`, **weswigham**)

**Baselines: Namespace\-to\-const restructuring with DtsFileErrors \(redeclaration errors\)**

*Namespace-to-const transformation in baselines erroneously produces invalid .d.ts files with TS2451 redeclaration errors.*

 * created by **RyanCavanaugh**
 * **ahejlsberg** added label `Domain: Declaration Emit`
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and set milestone to `TypeScript 7.0 RC`

### [Issue microsoft/TypeScript-go#3549](https://github.com/microsoft/TypeScript-go/issues/3549) (Open, `Domain: Declaration Emit`, `Needs Investigation`, **weswigham**)

**Baselines: Missing generic type arguments no longer auto\-filled with any \(produces TS2314 errors\)**

*Generic types without explicit parameters now emit bare types instead of defaulting to any, causing TS2314 errors*

 * created by **RyanCavanaugh**
 * **ahejlsberg** added label `Domain: Declaration Emit`
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and set milestone to `TypeScript 7.0 RC`

### [Issue microsoft/TypeScript-go#3551](https://github.com/microsoft/TypeScript-go/issues/3551) (Open, `Domain: Declaration Emit`, `Needs Investigation`, **weswigham**)

**Baselines: Output file ordering changed \+ declaration types resolve to any instead of typeof references**

*Declaration emit with package exports tests now reorder output file sections and produce declaration types as any rather than typeof references*

 * created by **RyanCavanaugh**
 * **ahejlsberg** added label `Domain: Declaration Emit`
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and set milestone to `TypeScript 7.0 RC`

### [Issue microsoft/TypeScript-go#3555](https://github.com/microsoft/TypeScript-go/issues/3555) (Open, `Domain: Declaration Emit`, `Needs Investigation`, **weswigham**)

**Baselines: @overload handling changes in JS declaration emit**

*JS declaration emit for JSDoc @overload alters overload output by removing or duplicating comments, losing type parameters, and collapsing signatures.*

 * created by **RyanCavanaugh**
 * **ahejlsberg** added label `Domain: Declaration Emit`
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and set milestone to `TypeScript 7.0 RC`

### [Issue microsoft/TypeScript-go#3556](https://github.com/microsoft/TypeScript-go/issues/3556) (Open, `Domain: Declaration Emit`, `Needs Investigation`, **weswigham**)

**Baselines: @callback/@overload tags reordered and restructured in declaration emit**

*Declaration emit reorders callback and overload tags, simplifies type definitions, and mistakenly changes rest parameters from string[] to string.*

 * created by **RyanCavanaugh**
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/3556#issuecomment-4316034492) **ahejlsberg** said "I dont think conformance/callbackTagNestedParameter.js.diff is related to this issue."
 * **ahejlsberg** added label `Domain: Declaration Emit`
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and set milestone to `TypeScript 7.0 RC`

### [Issue microsoft/TypeScript-go#3558](https://github.com/microsoft/TypeScript-go/issues/3558) (Open, `Domain: Declaration Emit`, **DanielRosenwasser**, **Copilot**)

**Baselines: Labeled statement followed by export declaration loses original text**

*Labeled statements followed by export declarations lose their original semicolon in emitted baselines*

 * **ahejlsberg** added label `Domain: Declaration Emit`
 * (1 week ago) **DanielRosenwasser** assigned to **Copilot**, **DanielRosenwasser**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [Issue microsoft/TypeScript-go#3559](https://github.com/microsoft/TypeScript-go/issues/3559) (Open, `Domain: Declaration Emit`, `Needs Investigation`, **weswigham**)

**Baselines: CJS exports pattern changes in declaration emit**

*CommonJS declaration emit restructuring changed baselines, causing some files to lose exports entirely.*

 * created by **RyanCavanaugh**
 * **ahejlsberg** added label `Domain: Declaration Emit`
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and set milestone to `TypeScript 7.0 RC`

### [Issue microsoft/TypeScript-go#3560](https://github.com/microsoft/TypeScript-go/issues/3560) (Open, `Domain: Declaration Emit`, `Needs Investigation`, **weswigham**)

**Baselines: exportNonInitializedVariables crash in declaration emit**

*Declaration emit crashes when exporting non-initialized variables in commonjs module baselines tests.*

 * created by **RyanCavanaugh**
 * **ahejlsberg** added label `Domain: Declaration Emit`
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and set milestone to `TypeScript 7.0 RC`

### [Issue microsoft/TypeScript-go#3563](https://github.com/microsoft/TypeScript-go/issues/3563) (Open, **ahejlsberg**)

**Baselines: definiteAssignment shorthand in object literal loses optional modifier**

*Optional method properties in object literal shorthand lose their optional modifier when emitted with definite assignment assertions.*

 * created by **RyanCavanaugh**
 * **ahejlsberg** assigned to **ahejlsberg**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [Issue microsoft/TypeScript-go#3565](https://github.com/microsoft/TypeScript-go/issues/3565) (Closed, `Domain: Declaration Emit`, `Needs Investigation`)

**Baselines: Declaration emit trailing comma changes in destructuring parameters**

*Declaration emit baselines remove extra trailing commas after omitted elements in destructuring parameters.*

 * created by **RyanCavanaugh**
 * **ahejlsberg** added label `Domain: Declaration Emit`
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and set milestone to `TypeScript 7.0 RC`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3566](https://github.com/microsoft/TypeScript-go/issues/3566) (Open, `Domain: Declaration Emit`, `Needs Investigation`, **weswigham**)

**Baselines: Late\-bound computed property \[prop\] preserved instead of resolved to plain prop**

*Late-bound computed property [prop] syntax is preserved instead of being resolved to plain prop*

 * created by **RyanCavanaugh**
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/3566#issuecomment-4309176683) **RyanCavanaugh** said "This seems like a won't fix, actually. Both emits are equivalent."
 * **ahejlsberg** added label `Domain: Declaration Emit`
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and set milestone to `TypeScript 7.0 RC`

### [Issue microsoft/TypeScript-go#3567](https://github.com/microsoft/TypeScript-go/issues/3567) (Open, `Domain: Declaration Emit`, `Needs Investigation`, **weswigham**)

**Baselines: Symbol getter/setter declaration emit change**

*Declaration outputs now change the return type of symbol getters/setters to undefined and introduce a new Symbol.toPrimitive overload.*

 * created by **RyanCavanaugh**
 * **ahejlsberg** added label `Domain: Declaration Emit`
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and set milestone to `TypeScript 7.0 RC`

### [Issue microsoft/TypeScript-go#3568](https://github.com/microsoft/TypeScript-go/issues/3568) (Open, `Domain: Declaration Emit`, `Needs Investigation`, **weswigham**)

**Baselines: export as namespace added or restructured in declaration emit**

*Add or restructure ‘export as namespace GLO’ in declaration emit baselines to update module global visibility and public API contract.*

 * created by **RyanCavanaugh**
 * **ahejlsberg** added label `Domain: Declaration Emit`
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and set milestone to `TypeScript 7.0 RC`

### [Issue microsoft/TypeScript-go#3569](https://github.com/microsoft/TypeScript-go/issues/3569) (Open, `Domain: Declaration Emit`, `Needs Investigation`, **weswigham**)

**Baselines: Declaration emit simplification of class extending built\-in Array**

*Declaration emit now simplifies classes extending built-in Array by dropping the generic parameter and removing inherited constructor overloads.*

 * created by **RyanCavanaugh**
 * **ahejlsberg** added label `Domain: Declaration Emit`
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and set milestone to `TypeScript 7.0 RC`

### [Issue microsoft/TypeScript-go#3570](https://github.com/microsoft/TypeScript-go/issues/3570) (Closed, `Domain: Declaration Emit`, `Needs Investigation`)

**Baselines: Declaration emit type parameter renaming bug \(regression\)**

*Declaration emit incorrectly renames type parameters to T_1, leading to undefined types and TS2304 errors*

 * created by **RyanCavanaugh**
 * **ahejlsberg** added label `Domain: Declaration Emit`
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and set milestone to `TypeScript 7.0 RC`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3572](https://github.com/microsoft/TypeScript-go/pull/3572) (Closed)

**Enter signature scope in SerializeReturnTypeForSignature**

*Add signature scope support to SerializeReturnTypeForSignature for accurate return type serialization*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3573](https://github.com/microsoft/TypeScript-go/pull/3573) (Closed)

**Optimize type variable scope map cloning with CoW**

*Reintroduce copy-on-write for type variable scope maps to cut 720k allocations in the test suite.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3573#issuecomment-4383719204) **jakebailey** said "Not a bad idea to formalize this, I'll give it a go"

### [PR microsoft/TypeScript-go#3574](https://github.com/microsoft/TypeScript-go/pull/3574) (Closed)

**fix\(3565\): preserve trailing commas in declaration\-emitted array binding patterns**

*Ensure trailing commas are retained in array binding patterns generated in declarations.*

 * created by **a-tarasyuk**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3588](https://github.com/microsoft/TypeScript-go/issues/3588) (Open, **jakebailey**, **Copilot**)

**Behaviour differences observed when varying tsconfig option key letter cases randomly**

*Lowercasing tsconfig compilerOptions keys causes unknown option and build-only errors in TypeScript 6.0*

 * created by **hkleungai**
 * (1 week ago) **jakebailey** assigned to **Copilot**, **jakebailey**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [Issue microsoft/TypeScript-go#3593](https://github.com/microsoft/TypeScript-go/issues/3593) (Closed)

**\[ServerErrors\]\[JavaScript\] main vs **

*Azure pipeline run on main branch encountered JavaScript server errors when analyzing 300 popular TypeScript repositories, resulting in various failures and timeouts.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/3593#issuecomment-4316621655) **typescript-bot** reported server connection closed prematurely with undefined error and provided affected repo details, logs, requests, and repro steps
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/3593#issuecomment-4316621698) **typescript-bot** reported a premature server connection closure error with undefined reason and provided details for mrdoob/three.js
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/3593#issuecomment-4316621736) **typescript-bot** reported a panic handling textDocument/hover due to unhandled TypeNode KindTypeParameter
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#3597](https://github.com/microsoft/TypeScript-go/issues/3597) (Open, **jakebailey**, **Copilot**)

**Broken JSDoc codeblock parsing**

*JSDoc fenced code blocks with embedded tags like @Embed are misparsed by tsgo, producing incorrect HTML rendering.*

 * created by **LukeAbby**
 * (1 week ago) **jakebailey** assigned to **Copilot**, **jakebailey**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [Issue microsoft/TypeScript-go#3615](https://github.com/microsoft/TypeScript-go/issues/3615) (Closed, **andrewbranch**, **Copilot**)

**Server stops responding after \`Running scheduled diagnostics refresh\`**

*The TypeScript language server hangs after running scheduled diagnostics refresh in large monorepos with many open editors and file system event bursts.*

 * created by **ekazakov14**
 * (1 week ago) **andrewbranch** assigned to **Copilot**, **andrewbranch**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [Issue microsoft/TypeScript-go#3617](https://github.com/microsoft/TypeScript-go/issues/3617) (Open, `Needs Investigation`, **iisaduan**)

**fix: FindBestPatternMatch incorrectly allows wildcard pattern to override exact match**

*FindBestPatternMatch misuses StarIndex so exact matches set longestMatchPrefixLength to -1, allowing later wildcard patterns to override exact matches.*

 * created by **kuishou68**
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/3617#issuecomment-4323559489) **kuishou68** filed PR #3618 with a fix that sets longestMatchPrefixLength to math.MaxInt on exact matches to prevent wildcard override, matching original TypeScript behavior
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.0 RC`, and assigned to **iisaduan**

### [PR microsoft/TypeScript-go#3628](https://github.com/microsoft/TypeScript-go/pull/3628) (Closed, **andrewbranch**, **Copilot**)

**Fix server hang after "Running scheduled diagnostics refresh"**

*Convert scheduled diagnostics refresh to non-blocking and introduce per-request timeouts, watcher deduplication, and registry encapsulation to prevent server deadlocks.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3628#issuecomment-4339083623) **Copilot** rewrote the test for updateWatch timeout and retry using real session operations and synctest, mocking WatchFilesFunc to block on the first batch and verifying that after a timeout-induced rollback the registry remained clean for re-registration
 * [6 days ago](https://github.com/microsoft/TypeScript-go/pull/3628#issuecomment-4345426618) **andrewbranch** said "@copilot address review comments"
 * [6 days ago](https://github.com/microsoft/TypeScript-go/pull/3628#issuecomment-4345569244) **Copilot** addressed all five review comments in commit 22abe61, including changes to refcount rollback on error, consistent locking requirements, per-request timeouts, duplicate-pattern deduplication, and stronger test assertions
 * [today](https://github.com/microsoft/TypeScript-go/pull/3628#issuecomment-4382929180) **andrewbranch** asked for clarification on the dedupe watchers by key and refcount behavior
 * [today](https://github.com/microsoft/TypeScript-go/pull/3628#issuecomment-4382977344) **Copilot** explained the rollback path refcount inflation caused by deduping watchers and offered to switch to tracking all acquired watchers for release instead
 * [today](https://github.com/microsoft/TypeScript-go/pull/3628#issuecomment-4383276265) **andrewbranch** said "@copilot understood. Instead, let's move the deduplication into WatchedFiles itself so the session code is simplified."
 * [today](https://github.com/microsoft/TypeScript-go/pull/3628#issuecomment-4383400405) **Copilot** described moving deduplication into WatchedFiles and updating Watchers() to deduplicate via slices.Compact and removing updateWatch logic
 * [today](https://github.com/microsoft/TypeScript-go/pull/3628#issuecomment-4383467093) **andrewbranch** said "@copilot move mutex locking into watchRegistry methods."
 * [today](https://github.com/microsoft/TypeScript-go/pull/3628#issuecomment-4383561544) **Copilot** moved mutex locking into watchRegistry methods and removed external lock calls from session.go

### [Issue microsoft/TypeScript-go#3631](https://github.com/microsoft/TypeScript-go/issues/3631) (Open, `Domain: Editor`, **DanielRosenwasser**)

**New untitled files are not correctly managed by config file status bar indicator**

*Unsaved TypeScript buffers in VS Code erroneously display the previous project's tsconfig.json status until editor focus changes, after which they show “No tsconfig”.*

 * created by **DanielRosenwasser**
 * (1 week ago) **DanielRosenwasser** added label `Domain: Editor`, and assigned to **DanielRosenwasser**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [Issue microsoft/TypeScript-go#3651](https://github.com/microsoft/TypeScript-go/issues/3651) (Open, `Domain: Editor`, **andrewbranch**)

**"Native Preview: Disable" does not re\-activate built\-in extension**

*Disabling the native preview fails to restore the built-in TypeScript extension in VS Code.*

 * created by **DanielRosenwasser**
 * (1 week ago) **DanielRosenwasser** added label `Domain: Editor`, and assigned to **andrewbranch**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [Issue microsoft/TypeScript-go#3654](https://github.com/microsoft/TypeScript-go/issues/3654) (Open, **DanielRosenwasser**)

**Harden rescan strategy for astnav**

*Identify and optimize necessary astnav rescan points to prevent redundant rescans already handled by the formatting scanner.*

 * created by **DanielRosenwasser**
 * **DanielRosenwasser** assigned to **DanielRosenwasser**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [Issue microsoft/TypeScript-go#3655](https://github.com/microsoft/TypeScript-go/issues/3655) (Open, `Needs Investigation`, **iisaduan**)

**Behavior difference: Pattern matching against \`extends { \[P in K\]?: unknown }\` emit slightly different error in tsgo**

*tsgo inconsistently expands mapped type constraint { [P in K]?: unknown } in generics, causing different errors than tsc*

 * created by **hkleungai**
 * [6 days ago](https://github.com/microsoft/TypeScript-go/issues/3655#issuecomment-4346081658) **ahejlsberg** said "I think the tsgo behavior is quite reasonable here. In general, tsgo tries harder to print back what was actually written."
 * [6 days ago](https://github.com/microsoft/TypeScript-go/issues/3655#issuecomment-4346415073) **hkleungai** expressed doubt about the intent, provided a code example, and noted that the printed output's type syntax was complex and harder to comprehend than TS 6's output
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.0 RC`, and assigned to **iisaduan**

### [Issue microsoft/TypeScript-go#3661](https://github.com/microsoft/TypeScript-go/issues/3661) (Open, `Needs Investigation`, **iisaduan**)

**Behavior difference: tsgo emits an "extra" TS7006 along with TS2769 at the same line in case of overload mismatch**

*tsgo redundantly emits both TS2769 and TS7006 errors for an overload mismatch call, unlike tsc.*

 * created by **hkleungai**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.0 RC`, and assigned to **iisaduan**

### [Issue microsoft/TypeScript-go#3662](https://github.com/microsoft/TypeScript-go/issues/3662) (Open, `Needs Investigation`, **iisaduan**)

**Behavior difference: tsgo wrongly allows \`include\` to contain files that is not under \`rootDir\` from tsconfig**

*tsgo incorrectly permits including files outside the configured rootDir in tsconfig without reporting errors.*

 * created by **hkleungai**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.0 RC`, and assigned to **iisaduan**

### [Issue microsoft/TypeScript-go#3665](https://github.com/microsoft/TypeScript-go/issues/3665) (Open, `Needs Investigation`, **iisaduan**)

**Behavior difference: jsdoc typing on child class member overrides parent class's type in tsgo but not in tsc**

*tsgo incorrectly reports an error when a child class’s JSDoc-typed state property overrides its parent class’s type, while tsc accepts it.*

 * created by **hkleungai**
 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/3665#issuecomment-4354512469) **Andarist** described that the error matched the old TypeScript compiler behavior and noted that an implicitly inferred derived class type shouldn’t override an explicitly typed base property
 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/3665#issuecomment-4355450508) **hkleungai** argued that even though TS7 is a native port on TS6, subtle type-checking discrepancies were worth fixing and suggested scheduling fixes for the Post 7.0 milestone
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.0 RC`, and assigned to **iisaduan**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3665#issuecomment-4384208278) **ahejlsberg** described inconsistent JSDoc @type behavior between Strada and Corsa and concluded no change was needed
 * [today](https://github.com/microsoft/TypeScript-go/issues/3665#issuecomment-4385084347) **hkleungai** speculated that 'unknown' is uncommon in plain JavaScript, observed that some developers prefer using Object types, and suggested TS7 inherit some TS6 behavior

### [Issue microsoft/TypeScript-go#3666](https://github.com/microsoft/TypeScript-go/issues/3666) (Closed, `Needs Investigation`, **iisaduan**)

**Behavior difference: tsgo does not \(fully\) respect jsdoc \`@extend\` clause**

*tsgo fails to report mismatched JSDoc @extends errors for JS classes, unlike tsc which correctly flags them.*

 * created by **hkleungai**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.0 RC`, and assigned to **iisaduan**

### [Issue microsoft/TypeScript-go#3676](https://github.com/microsoft/TypeScript-go/issues/3676) (Open, **gabritto**)

**tsconfig diagnostics not refreshed if no TS/JS files are open**

*Diagnostic errors for a removed 'baseUrl' option in tsconfig.json fail to clear when no TS or JS files are open.*

 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/3676#issuecomment-4360644660) **DanielRosenwasser** said "I'm not sure if there really is a great fix here given how pull diagnostics works, but I think it's worth investigating here."
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/3676#issuecomment-4360656283) **DanielRosenwasser** said "Maybe we can do something custom with our extension's client when a config file changes?"
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/3676#issuecomment-4360821353) **jakebailey** recommended pushing an empty diagnostic set when a project became unreferenced after all files were closed
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [Issue microsoft/TypeScript-go#3679](https://github.com/microsoft/TypeScript-go/issues/3679) (Closed)

**\[ServerErrors\]\[JavaScript\] main vs **

*The main pipeline analyzed JavaScript errors across 300 TypeScript repositories, successfully processing 255 and reporting 7 changes, timeouts, and failures.*

 * created by **typescript-bot**
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/3679#issuecomment-4361805001) **typescript-bot** reported that the server connection closed prematurely and provided error details, last requests, and repro steps for BoostIO/BoostNote-Legacy
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#3681](https://github.com/microsoft/TypeScript-go/issues/3681) (Closed)

**\[ServerErrors\]\[TypeScript\] main vs **

*The main TypeScript branch’s Azure pipeline run on 300 popular GitHub repositories encountered server errors, clone failures, and timeouts.*

 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/3681#issuecomment-4362138944) **typescript-bot** described a premature server connection closure error for the payloadcms/payload repo, listed related requests and provided reproduction steps
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/3681#issuecomment-4362138979) **typescript-bot** reported server connection closed prematurely error for cypress-io/cypress and shared logs, request details, and reproduction steps
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/3681#issuecomment-4362139013) **typescript-bot** reported server connection closed prematurely error and provided logs and repro steps for n8n-io/n8n
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#3685](https://github.com/microsoft/TypeScript-go/pull/3685) (Closed)

**Fix flake in TestRegistryLifecycle pnpm\-style symlink test**

*Intermittent failure of TestRegistryLifecycle’s pnpm-style symlinks test due to bucket not marked dirty after package change*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3685#issuecomment-4384064630) **jakebailey** said "Hit again in https://github.com/microsoft/typescript-go/actions/runs/25408217704/job/74523886466"
 * (later) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3686](https://github.com/microsoft/TypeScript-go/issues/3686) (Open, `bug`, `Domain: Declaration Emit`, **weswigham**)

**Unnecessary declaration in \.d\.ts**

*tsgo emits declarations for a non-exported function and its namespace in the .d.ts file that should be omitted.*

 * created by **Withered-Flower-0422**
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/3686#issuecomment-4363259768) **Withered-Flower-0422** demonstrated that the emitted .d.ts files differed between TypeScript 6.0 and tsgo for an exported function with a property
 * (today) **weswigham** added labels `bug`, `Domain: Declaration Emit`, and assigned to **weswigham**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [Issue microsoft/TypeScript-go#3688](https://github.com/microsoft/TypeScript-go/issues/3688) (Closed)

**Behavior difference: const T extends string = string binds to default instead of inferring never**

*tsgo's native preview defaults generic T to string instead of inferring never, causing via's conditional type to error.*

 * created by **birkskyum**
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/3688#issuecomment-4365074002) **jakebailey** said "Have you tested with --stableTypeOrdering in 6.0?"
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/3688#issuecomment-4366254698) **birkskyum** tested various compiler commands including tsc and tsgo with and without stableTypeOrdering and found the type-check divergence persisted
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#3692](https://github.com/microsoft/TypeScript-go/issues/3692) (Open, `Needs More Info`)

**Excessive CPU usage**

*WebStorm’s ts-go server often consumes 80-100% CPU when adding new imports in a monorepo frontend until restarted.*

 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/3692#issuecomment-4365889287) **Jelcoo** said "While writing this issue I was working on https://github.com/calagopus/panel/commit/2db0200f2c03ab2174db6f012363fe0a49a7c967, but it has been happening with all sorts of other changes."
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3692#issuecomment-4374556539) **jakebailey** said "I have no idea how WebStorm works, but in VS Code, we have a command that can take a profile and you could upload that."
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3692#issuecomment-4374635334) **andrewbranch** explained that briefly spiking to 80–100% CPU usage when adding imports was not unusual, and that only sustained high usage would be abnormal
 * [later](https://github.com/microsoft/TypeScript-go/issues/3692#issuecomment-4385893760) **Jelcoo** mentioned that the issue did not occur in VS Code, asked how to manually capture a profile, and noted that CPU spikes halted autocomplete

### [Issue microsoft/TypeScript-go#3694](https://github.com/microsoft/TypeScript-go/issues/3694) (Closed, `wontfix`, **DanielRosenwasser**, **iisaduan**, **Copilot**)

**Behavior difference: jsdoc \`@param\` referencing object attribute value throws TS2749 in tsc but throws TS2503 in tsgo**

*When using jsdoc @param to reference an object property, tsgo throws TS2503 instead of TS2749 like tsc*

 * (yesterday) **DanielRosenwasser** assigned to **Copilot**, **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3694#issuecomment-4377297602) **hkleungai** described how they found issues by diffing tsc and tsgo outputs, noted the productivity of the manual process, and requested better documentation of expected differences
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.0 RC`, and assigned to **iisaduan**

### [PR microsoft/TypeScript-go#3695](https://github.com/microsoft/TypeScript-go/pull/3695) (Closed)

**Fix inference from never into union targets**

*Adjust type inference to correctly exclude never types from union targets, aligning behavior with Strada code.*

 * created by **Andarist**
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#3701](https://github.com/microsoft/TypeScript-go/issues/3701) (Open, **jakebailey**, **Copilot**)

**When using \`module=commonjs\`, Array destructuring is transpiled with wrong \(non\-iterator\) behavior**

*Compiling with module=commonjs wrongly transpiles exported array destructuring into fixed index access instead of iterator logic.*

 * created by **blickly**
 * (yesterday) **jakebailey** assigned to **Copilot**, **jakebailey**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [PR microsoft/TypeScript-go#3705](https://github.com/microsoft/TypeScript-go/pull/3705) (Open, **jakebailey**, **Copilot**)

**Preserve native destructuring for CommonJS exports to keep iterator semantics**

*Emit native destructuring for CommonJS exports and generate separate export assignments per identifier to preserve iterator semantics.*

 * (yesterday) **Copilot** assigned to **Copilot**, **jakebailey**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3705#issuecomment-4374885896) **jakebailey** noted uncertainty about its impact on cjs-module-lexer scanning and asked if it was the intended change
 * [today](https://github.com/microsoft/TypeScript-go/pull/3705#issuecomment-4381122415) **blickly** mentioned that they expected destructuring syntax but acknowledged the current version was correct and an improvement
 * [today](https://github.com/microsoft/TypeScript-go/pull/3705#issuecomment-4381182266) **jakebailey** endorsed the suggestion as it avoids the lexer problem and asked the bots to try it
 * [today](https://github.com/microsoft/TypeScript-go/pull/3705#issuecomment-4381330720) **Copilot** reworked the code emission to output a lexer-friendly form that preserves array destructuring and emits exports assignments for each declared identifier

### [Issue microsoft/TypeScript-go#3708](https://github.com/microsoft/TypeScript-go/issues/3708) (Closed, **sandersn**, **Copilot**)

**\#3402 breaks CHANGES\.md badly**

*Pull request #3402 introduced incorrect documentation in CHANGES.md claiming prototype property assignments fail for constructor functions and should be reverted.*

 * created by **sandersn**
 * (today) **sandersn** assigned to **sandersn**, **Copilot**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3708#issuecomment-4381528364) **sandersn** requested restoring specific table rows and replacing documentation wording while preserving the section title
 * (today) **sandersn** assigned to **Copilot**, and unassigned **Copilot**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3708#issuecomment-4383300062) **ahejlsberg** mentioned that prototype property assignment didn't work in Corsa and that getAssignmentDeclarationKind lacked the Prototype and PrototypeProperty kinds and associated logic wasn't ported
 * [today](https://github.com/microsoft/TypeScript-go/issues/3708#issuecomment-4383377910) **sandersn** said "You're right. I was going off my old notes where it was pencilled in as "do last, cut if it makes sense" and I mis-remembered it as not cut."
 * (today) **sandersn** closed the issue

### [Issue microsoft/TypeScript-go#3709](https://github.com/microsoft/TypeScript-go/issues/3709) (Closed, **ahejlsberg**)

**Regression: error TS2322: Type OBJECT\_LITERAL is not assignable to type 'Record\<string, \.\.\.\>'\.**

*tsgo now produces TS2322 errors when assigning {} to a Record<string, boolean>, regressing behavior from TypeScript 6.0*

 * created by **7nik**
 * **jakebailey** assigned to **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3709#issuecomment-4381470213) **GrygrFlzr** narrowed down the commit range where the TypeScript error first appeared using the tsgo playground
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#3710](https://github.com/microsoft/TypeScript-go/pull/3710) (Closed, **sandersn**, **Copilot**)

**revert: restore CHANGES\.md to pre\-\#3402 state**

*Revert CHANGES.md to pre-#3402 state by removing the incorrect expando table row and restoring the original prototype assignment description.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **sandersn**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3710#issuecomment-4381367437) **sandersn** requested removal of uppercase synonym and jsdoc index signature rows from the table and suggested changing 'any' back to 'most'
 * [today](https://github.com/microsoft/TypeScript-go/pull/3710#issuecomment-4381401523) **Copilot** removed the uppercase synonym and JSDoc index signature rows and changed 'any' back to 'most'
 * [today](https://github.com/microsoft/TypeScript-go/pull/3710#issuecomment-4381407922) **sandersn** said "@copilot oh, also keep the compact format so it's easier to read the diff "
 * [today](https://github.com/microsoft/TypeScript-go/pull/3710#issuecomment-4381455115) **Copilot** implemented the compact single-line format for all three tables in commit 22878a46
 * [today](https://github.com/microsoft/TypeScript-go/pull/3710#issuecomment-4381502654) **sandersn** said "This diff is too hard to read. I'm going to try again from a fresh prompt."
 * (today) **sandersn** closed the issue

### [PR microsoft/TypeScript-go#3711](https://github.com/microsoft/TypeScript-go/pull/3711) (Open)

**Narrow String\#toLowerCase/toUpperCase return types via Lowercase/Uppercase**

*Narrow String.prototype.toLowerCase and toUpperCase return types to literal strings using Lowercase and Uppercase generics.*

 * created by **ljharb**

### [PR microsoft/TypeScript-go#3712](https://github.com/microsoft/TypeScript-go/pull/3712) (Closed)

**fix: use utf8\.DecodeLastRuneInString to correctly handle multi\-byte runes in setLastNonTriviaPosition**

*Use utf8.DecodeLastRuneInString to handle multi-byte runes correctly in setLastNonTriviaPosition.*

 * created by **a-tarasyuk**
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript-go#3713](https://github.com/microsoft/TypeScript-go/pull/3713) (Closed, **sandersn**, **Copilot**)

**Restore constructor\-function guidance in CHANGES\.md without broad revert**

*Restore original constructor-function prototype assignment guidance in CHANGES.md while preserving other editorial updates.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **sandersn**
 * (today) **sandersn** closed the issue

### [PR microsoft/TypeScript-go#3714](https://github.com/microsoft/TypeScript-go/pull/3714) (Closed)

**Declaration with type annotation and \`{}\` initializer isn't expando object**

*Variables declared with a type annotation and an empty object initializer are not treated as expando objects.*

 * created by **ahejlsberg**
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#3715](https://github.com/microsoft/TypeScript-go/issues/3715) (Closed, `wontfix`)

**Behavior difference: tsgo cannot typecheck es3 prototype\-style OOP code correctly**

*tsgo fails to infer prototype-style ES3 class types, treating instance properties and methods as any.*

 * created by **hkleungai**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3715#issuecomment-4383373869) **RyanCavanaugh** said "ES3 class inference has been removed, see https://github.com/microsoft/typescript-go/blob/main/CHANGES.md#assigning-to-the-prototype-property-of-a-function-no-longer-makes-it-a-constructor-function"
 * [today](https://github.com/microsoft/TypeScript-go/issues/3715#issuecomment-4383710012) **ahejlsberg** apologized for confusion and clarified that prototype-style constructor functions are being deprecated in favor of classes and that the guidance will be clarified in issue #3718
 * **ahejlsberg** added label `wontfix`
 * (today) **ahejlsberg** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/issues/3715#issuecomment-4384923551) **hkleungai** said "Thank you for your effort on this. 🫡"

### [PR microsoft/TypeScript-go#3716](https://github.com/microsoft/TypeScript-go/pull/3716) (Open)

**Only include \_visible\_ expando functions in declaration emit output**

*Restrict declaration emit output to include only visible expando functions.*

 * created by **weswigham**

### [PR microsoft/TypeScript-go#3717](https://github.com/microsoft/TypeScript-go/pull/3717) (Open)

**Proposed actions for symbol baseline diffs**

*Place 'needs investigation' groups at the top of symbol baseline diffs, mirroring the previous procedure.*

 * created by **RyanCavanaugh**

### [PR microsoft/TypeScript-go#3718](https://github.com/microsoft/TypeScript-go/pull/3718) (Closed)

**Update JS documentation in CHANGES\.md:**

*Update JS documentation in CHANGES.md to note that constructor functions are no longer supported and list newly supported features.*

 * created by **sandersn**
 * (later) **sandersn** closed the issue

### [Issue microsoft/TypeScript-go#3719](https://github.com/microsoft/TypeScript-go/issues/3719) (Open, `bug`, **iisaduan**)

**Support localized user\-facing strings in VS Code extension**

*Add localization support by moving user-facing strings into package.nls.json and using vscode-l10n tools.*

 * created by **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3719#issuecomment-4383830006) **jakebailey** said "You mean for extension strings, right?"

### [PR microsoft/TypeScript-go#3720](https://github.com/microsoft/TypeScript-go/pull/3720) (Open)

**Prompt after 5 consecutive server restarts in a session**

*Add a prompt after five consecutive server restarts to gather non-developer users’ reasons, with a possible phased rollout.*

 * created by **DanielRosenwasser**

### [Issue microsoft/TypeScript-go#3721](https://github.com/microsoft/TypeScript-go/issues/3721) (Closed, `wontfix`)

**tsgo drops re\-exported names when declare module combines export = X with a type\-only export**

*tsgo incorrectly omits re-exported members when an export = X module augmentation includes a type-only export.*

 * created by **vasilev-alex**
 * [later](https://github.com/microsoft/TypeScript-go/issues/3721#issuecomment-4389411834) **ahejlsberg** explained that removing skipLibCheck reveals errors due to mixing export = with regular exports and suggested properly augmenting the module by making the declaration file a module with export {} and a declare module 'react'

### [Issue microsoft/TypeScript-go#3722](https://github.com/microsoft/TypeScript-go/issues/3722) (Open, `Domain: Editor`)

**custom tsgo path is now ignored**

*VS Code's TypeScript native-preview ignores the configured custom tsgo path and launches its bundled tsgo instead.*

 * created by **loynoir**
 * **loynoir** added label `Domain: Editor`

