# Report for 2026-04-21 (Tuesday, April 21st, 2026)

12 different users commented on 55 different issues.

## Activity Summary

### [Issue microsoft/TypeScript-go#2836](https://github.com/microsoft/TypeScript-go/issues/2836) (Open, `possible improvement`)

**Cache \`getExePath\(\)\` for performance reasons**

*Cache getExePath results to avoid redundant lookups and improve tsgo invocation performance.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2836#issuecomment-4284246802) **jakebailey** noted that multiple tsgo invocations would not be helped by that cache form and guessed that paths might be hardcoded due to missing code
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2836#issuecomment-4286470961) **tido64** apologized for the delay and clarified that they stored the exec path in node_modules/.cache/tsgo, noted that the file location did not affect the architecture, and described using getExePath with persisting to disk (link provided)
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2836#issuecomment-4286516248) **jakebailey** said "I'm beyond surprised that this helps at all, given both hit the disk and "importing a module" should be the least of anyone's concerns. I'll have to try it and see..."
 * [today](https://github.com/microsoft/TypeScript-go/issues/2836#issuecomment-4291900328) **jakebailey** provided a CommonJS wrapper script that improved performance and noted that caching the path did not help much

### [PR microsoft/TypeScript-go#2914](https://github.com/microsoft/TypeScript-go/pull/2914) (Open)

**adds tracing \(\-\-generateTrace\)**

*Implement a tracing feature with --generateTrace to output types.json and trace.json files using a context-based approach.*

 * (4 days ago) **RyanCavanaugh** set milestones to `Possible Improvement`, `TypeScript 7.0 RC`, and removed from milestone `Possible Improvement`
 * [later](https://github.com/microsoft/TypeScript-go/pull/2914#issuecomment-4297568355) **dimitropoulos** rebased the branch onto origin/main, addressed remaining review feedback in follow-up commits, ran tests, lint, build, and format, and force-pushed the rebased branch
 * [later](https://github.com/microsoft/TypeScript-go/pull/2914#issuecomment-4297573073) **dimitropoulos** rebased the branch onto origin/main, addressed remaining review feedback in follow-up commits, ran tests, lint, build, and format, and force-pushed the rebased branch

### [PR microsoft/TypeScript-go#3216](https://github.com/microsoft/TypeScript-go/pull/3216) (Closed)

**fix: clean up failed pprof startup files**

*Use a start hook to remove partially created CPU profile files on BeginProfiling failures, adding a unit test for cleanup.*

 * **RyanCavanaugh** added to milestone `Possible Improvement`
 * [4 days ago](https://github.com/microsoft/TypeScript-go/pull/3216#issuecomment-4270006802) **RyanCavanaugh** said "Hardening internal debug/profiling codepaths against benign failures isn't a great use of churn/risk. It's fine if a local dev has to delete this file manually after killing the process or whatever."
 * (4 days ago) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/3216#issuecomment-4292266508) **buley** said "Copy that - thanks for the clear answer @RyanCavanaugh "

### [Issue microsoft/TypeScript-go#3410](https://github.com/microsoft/TypeScript-go/issues/3410) (Closed, `bug`, `Domain: Editor`, **weswigham**)

**Type serializer omits type arguments of outer functions**

*The tsgo type serializer drops outer function generic arguments when hovering on returned classes, displaying makeBox.Box instead of makeBox<string>.Box.*

 * [6 days ago](https://github.com/microsoft/TypeScript-go/issues/3410#issuecomment-4253846287) **jakebailey** suggested using ExpressionWithTypeArguments as a modern fix, noting the old approach relied on weird mutations and that printing predates instantiation expressions
 * [6 days ago](https://github.com/microsoft/TypeScript-go/issues/3410#issuecomment-4253860186) **ahejlsberg** agreed that using ExpressionWithTypeArguments was the modern fix
 * [6 days ago](https://github.com/microsoft/TypeScript-go/issues/3410#issuecomment-4254159917) **weswigham** agreed on using ExpressionWithTypeArguments and suggested adding a node builder flag and leveraging the existing AST for type argument data
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript-go#3412](https://github.com/microsoft/TypeScript-go/pull/3412) (Closed)

**fix\(3410\): preserve type arguments in hover for qualified names**

*Qualified name hover tooltips now correctly display preserved type arguments.*

 * [5 days ago](https://github.com/microsoft/TypeScript-go/pull/3412#issuecomment-4261910421) **ahejlsberg** clarified that ExpressionWithTypeArguments is now parsed for instantiation expressions and can occur in regular expressions
 * [5 days ago](https://github.com/microsoft/TypeScript-go/pull/3412#issuecomment-4263833864) **weswigham** explained that type nodes only allow expressions at the end of a typeof query and illustrated with parsing examples
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * (today) **weswigham** closed the issue

### [Issue microsoft/TypeScript-go#3441](https://github.com/microsoft/TypeScript-go/issues/3441) (Closed, **jakebailey**, **Copilot**)

**Panic handling textDocument/semanticTokens/{full,range}: slice bounds out of range and token\-spans\-multiple\-lines**

*Semantic tokens full and range handlers panic due to slice bounds out-of-range errors and multi-line token spans.*

 * **jakebailey** assigned to **jakebailey**
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3441#issuecomment-4283203554) **jakebailey** said "@liby Do you have the files where this happens?"
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3441#issuecomment-4285743482) **liby** clarified inability to share original files due to private codebase, corrected that both files were ASCII-only and that the panic was deterministic within a session, and provided verbose server logs with two panic instances showing semantic tokens spanning multiple lines errors
 * [today](https://github.com/microsoft/TypeScript-go/issues/3441#issuecomment-4292366992) **jakebailey** said "I suspect #3483 will actually fix this. We'll see tomorrow."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3442](https://github.com/microsoft/TypeScript-go/pull/3442) (Closed, **jakebailey**, **Copilot**)

**Fix utf8\.RuneLen bug in LineAndCharacterToPosition for invalid UTF\-8 sequences**

*Fixes utf8.RuneLen handling of invalid UTF-8 sequences in LineAndCharacterToPosition, adds position-mapping tests, and restores URI-filename conversion tests.*

 * (2 days ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/3442#issuecomment-4278352667) **jakebailey** said "This is certainly a bug, but I don't think it's the actual bug"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3457](https://github.com/microsoft/TypeScript-go/pull/3457) (Closed)

**Fixed crash when resolving declaration spaces on merged symbols resolving to export assignment**

*Fix crash when resolving declaration spaces for merged symbols assigned through an export assignment.*

 * created by **Andarist**
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript-go#3458](https://github.com/microsoft/TypeScript-go/pull/3458) (Closed, **jakebailey**, **Copilot**)

**Use \`typescript\` instead of \`tsx\` for hover code block language**

*Change hover tooltip code blocks to typescript instead of tsx to fix generic type highlighting issues.*

 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3458#issuecomment-4289326792) **jakebailey** confirmed expectation and linked to the relevant code in hover.ts
 * [later](https://github.com/microsoft/TypeScript-go/pull/3458#issuecomment-4297516959) **jakebailey** said "That would still end up causing the miscolorization of generic signatures in those files, though; otherwise I don't think we ever emit JSX-looking stuff?"

### [PR microsoft/TypeScript-go#3459](https://github.com/microsoft/TypeScript-go/pull/3459) (Closed)

**Baseline diff triaging**

*Reassign tests to accepted and triaged categories and update the CHANGES.md file.*

 * created by **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3459#issuecomment-4290519865) **jakebailey** said "I removed this from the merge queue, I still want to review it"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3460](https://github.com/microsoft/TypeScript-go/pull/3460) (Closed)

**Temporarily disable semantic tokens**

*Temporarily stop declaring semantic tokens support to the client to prevent frequent crashes.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3461](https://github.com/microsoft/TypeScript-go/issues/3461) (Closed, `Crash`, **gabritto**)

**panic handling request textDocument/completion: Cannot create token from reparsed node of kind KindHeritageClause**

*The TypeScript-Go language server panics on completion requests because it cannot create a token from a reparsed KindHeritageClause node.*

 * created by **gabritto**
 * (today) **gabritto** added label `Crash`, and assigned to **gabritto**
 * (today) **gabritto** closed the issue

### [Issue microsoft/TypeScript-go#3462](https://github.com/microsoft/TypeScript-go/issues/3462) (Closed, `Crash`)

**panic handling request textDocument/documentHighlight: runtime error: invalid memory address or nil pointer dereference**

*A nil pointer dereference causes a runtime panic when processing textDocument/documentHighlight requests in the TypeScript-Go language server.*

 * created by **gabritto**
 * **gabritto** added label `Crash`
 * (today) **gabritto** closed the issue
 * (today) **gabritto** reopened the issue
 * (later) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#3463](https://github.com/microsoft/TypeScript-go/issues/3463) (Closed)

**panic handling request textDocument/formatting: Debug failure\. False expression: Token end is child end**

*The typescript-go language server panics on textDocument/formatting requests due to a failed "Token end is child end" debug assertion.*

 * created by **gabritto**
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript-go#3464](https://github.com/microsoft/TypeScript-go/pull/3464) (Closed)

**Fix hover crash in hoverExpressionWithTypeArguments**

*Fix hoverExpressionWithTypeArguments crash caused by casting non-TypeReference objects with an undefined target property*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3465](https://github.com/microsoft/TypeScript-go/issues/3465) (Closed, `Crash`, **gabritto**)

**panic handling request textDocument/hover: Should be unreachable\.**

*Hover requests in the TypeScript-Go LSP server panic due to an unreachable code path in type node serialization.*

 * created by **gabritto**
 * (today) **gabritto** added label `Crash`, and assigned to **gabritto**
 * (today) **gabritto** closed the issue

### [Issue microsoft/TypeScript-go#3466](https://github.com/microsoft/TypeScript-go/issues/3466) (Closed, `Crash`, **jakebailey**)

**panic handling request textDocument/hover: Unhandled case in Type\.Target**

*A panic in the Microsoft TypeScript-Go language server’s textDocument/hover request due to an unhandled Type.Target case affects numerous repositories.*

 * created by **gabritto**
 * **jakebailey** assigned to **jakebailey**
 * **gabritto** added label `Crash`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3467](https://github.com/microsoft/TypeScript-go/issues/3467) (Closed, `Crash`)

**panic handling request textDocument/hover: runtime error: invalid memory address or nil pointer dereference in \`HasTrailingComma\`**

*Runtime panic in the TypeScript-Go LSP hover handler caused by a nil pointer dereference in HasTrailingComma.*

 * created by **gabritto**
 * **gabritto** added label `Crash`
 * (later) **gabritto** closed the issue

### [Issue microsoft/TypeScript-go#3468](https://github.com/microsoft/TypeScript-go/issues/3468) (Closed)

**panic handling request textDocument/rangeFormatting: Debug failure\. False expression: Token end is child end**

*A panic in textDocument/rangeFormatting due to a false token boundary assertion in the TypeScript language server across multiple repositories.*

 * created by **gabritto**
 * (today) **gabritto** closed the issue

### [Issue microsoft/TypeScript-go#3469](https://github.com/microsoft/TypeScript-go/issues/3469) (Closed)

**panic handling request textDocument/semanticTokens/full: semantic tokens: token spans multiple lines: start=\(40,24\) end=\(41,5\) for token at offset 1532**

*A semanticTokens/full request handler panics when encountering a token whose span crosses line boundaries, as reported in multiple repositories.*

 * created by **gabritto**
 * (today) **gabritto** closed the issue

### [Issue microsoft/TypeScript-go#3470](https://github.com/microsoft/TypeScript-go/issues/3470) (Closed, `Crash`)

**panic handling request textDocument/semanticTokens/full: semantic tokens: token spans multiple lines: start=\(15,34\) end=\(16,12\) for token at offset 617**

*The language server panics handling textDocument/semanticTokens/full when a semantic token spans lines 15:34 to 16:12.*

 * created by **gabritto**
 * **gabritto** added label `Crash`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3471](https://github.com/microsoft/TypeScript-go/issues/3471) (Closed)

**panic handling request textDocument/semanticTokens/full: semantic tokens: token spans multiple lines: start=\(5,20\) end=\(6,5\) for token at offset 222**

*The language server panics on a full semantic tokens request when a token spans multiple lines (from 5:20 to 6:5).*

 * created by **gabritto**
 * (today) **gabritto** closed the issue

### [Issue microsoft/TypeScript-go#3472](https://github.com/microsoft/TypeScript-go/issues/3472) (Closed)

**Server connection closed prematurely: undefined**

*TypeScript Go bot’s PR #3454 is causing “Server connection closed prematurely: undefined” errors across 14 different repositories.*

 * created by **gabritto**
 * (today) **gabritto** closed the issue

### [Issue microsoft/TypeScript-go#3473](https://github.com/microsoft/TypeScript-go/issues/3473) (Closed, `Crash`, **jakebailey**)

**panic handling request textDocument/hover: runtime error: invalid memory address or nil pointer dereference in \`getTypeArguments\`**

*Hover requests trigger a nil pointer dereference panic in the getTypeArguments function of the typescript-go language server*

 * created by **gabritto**
 * **gabritto** added label `Crash`
 * **jakebailey** assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3474](https://github.com/microsoft/TypeScript-go/pull/3474) (Closed)

**Fix \`getTokenAtPosition\` crash on reparsed \`prevSubtree\`**

*Ensure getTokenAtPosition verifies prevSubtree nodes haven't been reparsed before assignment to prevent subsequent crashes.*

 * created by **gabritto**
 * (today) **gabritto** closed the issue

### [Issue microsoft/TypeScript-go#3475](https://github.com/microsoft/TypeScript-go/issues/3475) (Open)

**Test harness doesn't report errors from unrecognized compiler options**

*The test harness fails to report errors for unrecognized compiler options, resulting in empty error outputs.*

 * created by **RyanCavanaugh**

### [Issue microsoft/TypeScript-go#3476](https://github.com/microsoft/TypeScript-go/issues/3476) (Open)

**No error reported when tslib helpers aren't found**

*The TypeScript compiler fails to report errors when tslib helper functions are missing, causing undetected issues.*

 * created by **RyanCavanaugh**

### [Issue microsoft/TypeScript-go#3477](https://github.com/microsoft/TypeScript-go/issues/3477) (Open)

**Remaining diffs in isolatedDeclarations**

*Remaining differences in isolatedDeclarations have been identified in submoduleTriaged.txt and await an upcoming PR.*

 * created by **RyanCavanaugh**

### [Issue microsoft/TypeScript-go#3478](https://github.com/microsoft/TypeScript-go/issues/3478) (Open)

**Wasm build**

*Request for a WebAssembly build of tsgo to enable experimentation in the online playground.*

 * created by **justinfagnani**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3478#issuecomment-4291015910) **jakebailey** said "Eventually, but I would be interested in knowing exactly what you're looking for, as everyone wants Wasm differently."
 * [today](https://github.com/microsoft/TypeScript-go/issues/3478#issuecomment-4291489874) **justinfagnani** described maintaining several TypeScript-based browser projects, notably lit.dev/playground, which compiles code, retrieves diagnostics, and uses language service APIs without custom transforms, and mentioned assuming that custom transforms would require a custom binary
 * [today](https://github.com/microsoft/TypeScript-go/issues/3478#issuecomment-4291509836) **jakebailey** noted that integrating the language server with Monaco and enabling API access entailed many moving parts, including process access and a full JS API

### [Issue microsoft/TypeScript-go#3479](https://github.com/microsoft/TypeScript-go/issues/3479) (Open)

**Untriaged differences in self\-package resolution \(possibly test harness only\)**

*Untriaged differences in TypeScript self-package resolution tests for NodeNext import mode and outDir scenarios possibly originate from the test harness.*

 * created by **RyanCavanaugh**

### [Issue microsoft/TypeScript-go#3480](https://github.com/microsoft/TypeScript-go/issues/3480) (Open)

**Missing error about jsx\-runtime package**

*Error messages for missing jsx-runtime package are not reported in legacy module detection tests for react-jsx and react-jsxdev*

 * created by **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3480#issuecomment-4291050128) **jakebailey** said "This comes down to us not detecting that this is a module due to other changes, which then changes how JSX behaves, IIRC"

### [Issue microsoft/TypeScript-go#3481](https://github.com/microsoft/TypeScript-go/issues/3481) (Open)

**Corsa differences in \`export=\` module augmentation**

*Corsa changes how export= module augmentation works, causing differences in exported name visibility.*

 * created by **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3481#issuecomment-4291838613) **ahejlsberg** said "The issue in augmentExportEquals2.errors.txt.diff is actually that the test is broken. There are two // @filename: file3.ts in a row, which we apparently no longer handle."

### [PR microsoft/TypeScript-go#3482](https://github.com/microsoft/TypeScript-go/pull/3482) (Closed)

**Don't expand empty enum**

*Prevent expansion of empty enums in the code generation process.*

 * created by **gabritto**
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript-go#3483](https://github.com/microsoft/TypeScript-go/pull/3483) (Closed)

**Mark file as changed when didOpen content differs from disk content**

*Mark files as changed when the content opened in the editor differs from the on-disk version.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3483#issuecomment-4292210975) **jakebailey** identified that differences between disk and didOpen caused additional crashes
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3484](https://github.com/microsoft/TypeScript-go/issues/3484) (Open)

**Static property conflicts with built\-in Function properties \(TS2699\) no longer reported when useDefineForClassFields is false**

*TypeScript does not report TS2699 errors for static class properties conflicting with built-in Function properties when useDefineForClassFields is false.*

 * created by **RyanCavanaugh**

### [PR microsoft/TypeScript-go#3485](https://github.com/microsoft/TypeScript-go/pull/3485) (Closed)

**Fix hover crash on classes with anonymous base class**

*Hovering over classes inheriting from anonymous base classes causes the hover feature to crash.*

 * created by **Andarist**
 * (later) **gabritto** closed the issue

### [PR microsoft/TypeScript-go#3486](https://github.com/microsoft/TypeScript-go/pull/3486) (Closed)

**Updates to accepted/triaged submodule diffs**

*Updated accepted and triaged submodule diffs for compiler and conformance error files, excluding most JavaScript diffs.*

 * created by **RyanCavanaugh**

### [Issue microsoft/TypeScript-go#3487](https://github.com/microsoft/TypeScript-go/issues/3487) (Open)

**tsgo reports downstream TS2339 in ignored for\-of over non\-iterable union that tsc 6\.0\.2 does not**

*tsgo incorrectly emits TS2339 for property access in a for...of loop over a non-iterable union despite @ts-ignore, unlike tsc 6.0.2*

 * created by **songkeys**

### [Issue microsoft/TypeScript-go#3488](https://github.com/microsoft/TypeScript-go/issues/3488) (Closed)

**Repeated identical conditional return type triggers TS2719 \("Two different types with this name exist"\) under tsgo**

*Inlining identical conditional return types in a generic function triggers TS2719 under tsgo, while a named alias workaround avoids it.*

 * created by **tomquist**
 * (later) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#3489](https://github.com/microsoft/TypeScript-go/issues/3489) (Open)

**Lowercase\<"İ"\>\` differs between tsgo and tsc \(Go strings\.ToLower vs JS String\.prototype\.toLowerCase\)**

*tsgo’s Lowercase intrinsic uses Go’s strings.ToLower rather than ECMAScript’s full Unicode case mapping, causing mismatched lowercase results for characters like 'İ'*

 * created by **tomquist**

### [Issue microsoft/TypeScript-go#3490](https://github.com/microsoft/TypeScript-go/issues/3490) (Open, `wontfix`)

**TS2411 reported on properties declared in \`node\_modules\` \`\.d\.ts\` files \(e\.g\. @types/jsdom DOMWindow\), where tsc 6\.0 silently allows them**

*TypeScript native-preview 7.0 reports TS2411 conflicts for @types/jsdom DOMWindow properties in node_modules that tsc 6.0 silently allows.*

 * created by **tomquist**

### [Issue microsoft/TypeScript-go#3491](https://github.com/microsoft/TypeScript-go/issues/3491) (Open, **ahejlsberg**)

**Excess\-property check fires on a nested object literal that is later assigned to an annotated return type, where tsc 6\.0 does not**

*TS7 incorrectly flags excess-property errors on nested object literals assigned via an untyped variable to a typed return, unlike TS6*

 * created by **tomquist**
 * **ahejlsberg** assigned to **ahejlsberg**
 * [later](https://github.com/microsoft/TypeScript-go/issues/3491#issuecomment-4296214357) **Andarist** described having a fix for the issue, provided sample code illustrating the problem, and reconsidered when to call getWidenedType before submitting the PR

### [Issue microsoft/TypeScript-go#3492](https://github.com/microsoft/TypeScript-go/issues/3492) (Open)

**tsgo rejects unknown JSX props that appear before a \`{\.\.\.spread}\` and are accepted by tsc 6\.0**

*tsgo incorrectly flags unknown JSX props before a spread operator as errors while TypeScript 6.0 accepts them*

 * created by **tomquist**

### [Issue microsoft/TypeScript-go#3493](https://github.com/microsoft/TypeScript-go/issues/3493) (Closed, **andrewbranch**)

**\`maxNodeModuleJsDepth\` \+ \`allowJs\` does not load types from a CommonJS dependency in \`node\_modules\` \(TS7016 vs tsc 6\.0 success\)**

*tsgo fails to load types from CommonJS dependencies in node_modules with allowJs and maxNodeModuleJsDepth, causing TS7016 errors unlike tsc 6.0.*

 * created by **tomquist**
 * (later) **ahejlsberg** assigned to **ahejlsberg**, **andrewbranch**, and unassigned **ahejlsberg**

### [Issue microsoft/TypeScript-go#3494](https://github.com/microsoft/TypeScript-go/issues/3494) (Closed, `bug`, `Domain: Type Checking`, **ahejlsberg**)

**\`keyof this\` is computed too narrowly on a subclass that passes itself as its own type parameter, causing TS2345 / TS2322 variance failure**

*Using a subclass as its own type parameter causes keyof this to exclude base class members, causing TS2322/TS2345 errors.*

 * created by **tomquist**
 * [later](https://github.com/microsoft/TypeScript-go/issues/3494#issuecomment-4295167376) **Andarist** explained that the error was caused by keyof computation on incomplete members before inherited members were added and that Corsa’s cache in getLiteralTypeFromProperties prolonged the incomplete value, leading to the error
 * (later) **ahejlsberg** added labels `bug`, `Domain: Type Checking`, and assigned to **ahejlsberg**
 * [later](https://github.com/microsoft/TypeScript-go/issues/3494#issuecomment-4297199869) **ahejlsberg** confirmed that `keyof` computation was triggered on incomplete members and explained that the fix adds a member resolution status flag to the cache key

### [PR microsoft/TypeScript-go#3495](https://github.com/microsoft/TypeScript-go/pull/3495) (Open)

**Use JS\-compatible Unicode casing for intrinsic string mappings**

*Implement JavaScript-compatible Unicode casing rules in TypeScript’s intrinsic string mapping functions.*

 * created by **Andarist**

### [PR microsoft/TypeScript-go#3496](https://github.com/microsoft/TypeScript-go/pull/3496) (Open)

**Fix error propagation through non\-iterable unions**

*Ensure errors are correctly propagated when handling non-iterable union types.*

 * created by **Andarist**

### [PR microsoft/TypeScript-go#3497](https://github.com/microsoft/TypeScript-go/pull/3497) (Open)

**Widen types assigned to auto\-typed variables**

*Widen inferred types for auto-typed variables to accept a broader range of assignments.*

 * created by **Andarist**
 * [later](https://github.com/microsoft/TypeScript-go/pull/3497#issuecomment-4297503973) **ahejlsberg** said "@typescript-bot test it"
 * [later](https://github.com/microsoft/TypeScript-go/pull/3497#issuecomment-4297504524) **typescript-bot** posted automated build status updates
 * [later](https://github.com/microsoft/TypeScript-go/pull/3497#issuecomment-4297663352) **typescript-bot** posted performance run results requested by @ahejlsberg
 * [later](https://github.com/microsoft/TypeScript-go/pull/3497#issuecomment-4297722737) **typescript-bot** reported automated test results indicating potential infrastructure failures and new TS7053 errors in webpack's EnvironmentPlugin.js

### [PR microsoft/TypeScript-go#3498](https://github.com/microsoft/TypeScript-go/pull/3498) (Closed)

**Avoid crash in getReferencedSymbolsForNode on export assignments in malformed sources**

*Prevent crashes in getReferencedSymbolsForNode when processing export assignments in malformed TypeScript sources.*

 * created by **Andarist**
 * (later) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#3499](https://github.com/microsoft/TypeScript-go/pull/3499) (Open)

**feat\(2280\): Port implement interface quick fix**

*Port the implement interface quick fix feature to support automatic interface implementation.*

 * created by **a-tarasyuk**

### [PR microsoft/TypeScript-go#3500](https://github.com/microsoft/TypeScript-go/pull/3500) (Closed)

**Include member resolution status in \`getLiteralTypeFromProperties\` key**

*Include member resolution status in the getLiteralTypeFromProperties key to properly differentiate literal types by resolution state.*

 * created by **ahejlsberg**

### [PR microsoft/TypeScript-go#3501](https://github.com/microsoft/TypeScript-go/pull/3501) (Closed)

**Fix conditional instantiation cache key mismatch for unresolved conditional types**

*Ensure conditional instantiation cache keys are correctly generated for unresolved conditional types.*

 * created by **Andarist**
 * (later) **ahejlsberg** closed the issue

