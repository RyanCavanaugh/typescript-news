# Report for 2026-04-22 (Wednesday, April 22nd, 2026)

19 different users commented on 45 different issues.

## Recommended Actions

 * Response Recommended
    * @rubenferreira97 asked if they should open a new issue without a solid reproduction in [microsoft/TypeScript-go#2666](https://github.com/microsoft/TypeScript-go/issues/2666#issuecomment-4300070293)
    * @Withered-Flower-0422 reported that the issue could be closed as fixed by #3410 in [microsoft/TypeScript-go#3411](https://github.com/microsoft/TypeScript-go/issues/3411#issuecomment-4298317598)
    * @TorinAsakura provided the CLA agreement as requested in [microsoft/TypeScript-go#3518](https://github.com/microsoft/TypeScript-go/pull/3518#issuecomment-4301346088)
    * @hkleungai asked if TypeScript 7 should suppress inter-file errors like TS 6 in [microsoft/TypeScript-go#3519](https://github.com/microsoft/TypeScript-go/issues/3519#issuecomment-4301827880)

## Activity Summary

### [Issue microsoft/TypeScript-go#2247](https://github.com/microsoft/TypeScript-go/issues/2247) (Closed, `Domain: Editor`, **andrewbranch**, **Copilot**)

**Auto\-imports insert \`import\` statement into CJS files**

*TypeScript auto-imports ES module syntax into CommonJS .js files with nodeXX module settings instead of require() despite type commonjs.*

 * **RyanCavanaugh** assigned to **andrewbranch**
 * **andrewbranch** assigned to **Copilot**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2666](https://github.com/microsoft/TypeScript-go/issues/2666) (Open, `Needs Investigation`, **johnfav03**)

**\`tsgo \-\-build\` fails to invalidate incremental cache after dependency update**

*tsgo's --build incremental cache does not detect updated dependency types and ignores resulting type errors.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2666#issuecomment-4161580561) **rubenferreira97** provided a minimal reproduction repository for the build bug using local dependencies
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/2666#issuecomment-4247911575) **RyanCavanaugh** said "Confirmed repro, thanks @rubenferreira97 "
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2666#issuecomment-4300070293) **rubenferreira97** described a hanging issue with tsgo --build due to stale .tsbuildinfo cache between versions and asked if they should open a new issue without a solid reproduction

### [PR microsoft/TypeScript-go#3328](https://github.com/microsoft/TypeScript-go/pull/3328) (Closed, **andrewbranch**, **Copilot**)

**Fix auto\-imports inserting \`import\` in CJS files when \`moduleDetection\` is \`force\`**

*When moduleDetection is forced, auto-imports wrongly generate import statements in CommonJS files instead of require calls.*

 * (2 weeks ago) **Copilot** assigned to **Copilot**, **andrewbranch**
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/3328#issuecomment-4285088068) **Copilot** implemented detectSyntax/detectSyntaxIndicators utility to properly handle moduleDetection force and non-force scenarios, updated fallback behaviors, and added a test for --module preserve + --moduleDetection force + JS require-only files
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3411](https://github.com/microsoft/TypeScript-go/issues/3411) (Closed, `Domain: Editor`)

**Missing generic type description in hover**

*tsgo hover omits showing instantiated generic types in inherited method signatures, unlike TypeScript 6.0.*

 * created by **Withered-Flower-0422**
 * **Withered-Flower-0422** added label `Domain: Editor`
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/3411#issuecomment-4253180257) **jakebailey** said "Yes I'm pretty sure this is exactly the same as that linked issue"
 * [today](https://github.com/microsoft/TypeScript-go/issues/3411#issuecomment-4298317598) **Withered-Flower-0422** said "Close as #3410 fixed."
 * (today) **Withered-Flower-0422** closed the issue

### [Issue microsoft/TypeScript-go#3426](https://github.com/microsoft/TypeScript-go/issues/3426) (Closed, `possible improvement`, **ahejlsberg**)

**tsc produces error, tsgo doesn't with sufficiently nested type**

*TypeScript 6 reports a nested type incompatibility between input and output APIs that tsgo overlooks until a layer is removed.*

 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/3426#issuecomment-4271613649) **joshcartme** inquired whether differentiating between generic and concrete types in Copilot's PR was reasonable after building and testing it against his repro and noting tsgo reported the error
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/3426#issuecomment-4273579488) **ahejlsberg** pointed out that the proposed fix was invalid because generative recursive type references such as Deep<Deep<T>> can lack generic types after instantiation but still require detection
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/3426#issuecomment-4274224844) **joshcartme** acknowledged understanding after explanation
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#3430](https://github.com/microsoft/TypeScript-go/pull/3430) (Closed)

**Move @typescript/api and @typescript/ast into @typescript/native\-preview for publishing**

*Merge @typescript/api and @typescript/ast into @typescript/native-preview to prevent version mismatches and simplify publishing ahead of TypeScript 7.0.*

 * created by **andrewbranch**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * [today](https://github.com/microsoft/TypeScript-go/pull/3430#issuecomment-4298489649) **jakebailey** asked about excluding vendored code from formatting and bundling it with esbuild
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#3436](https://github.com/microsoft/TypeScript-go/pull/3436) (Open)

**feat: add textDocument/\_vs\_onAutoInsert handler for VS closing tag auto\-insertion**

*Implement Visual Studio–specific _vs_onAutoInsert LSP handler and protocol types to auto-insert closing HTML/JSX tags and fix code generator jsonName bug.*

 * created by **lucygramley**
 * [5 days ago](https://github.com/microsoft/TypeScript-go/pull/3436#issuecomment-4271790692) **jakebailey** noted overlap between the code and existing tagClosing.ts and suggested consolidating instead of adding new code
 * [today](https://github.com/microsoft/TypeScript-go/pull/3436#issuecomment-4300584883) **jakebailey** pushed changes that deduplicated the code by using the VS style API, simplifying the implementation without affecting editor responsiveness

### [PR microsoft/TypeScript-go#3445](https://github.com/microsoft/TypeScript-go/pull/3445) (Closed)

**Improve recursion identity for direct type instantiations**

*Prevent false-positive generative recursion by excluding AST-resolved type references from using their symbol as recursion identity in isDeeplyNestedType.*

 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/3445#issuecomment-4283095634) **typescript-bot** posted an automated build status update
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/3445#issuecomment-4283224037) **typescript-bot** provided the performance run results requested by @ahejlsberg
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/3445#issuecomment-4283405902) **ahejlsberg** noted that PR #63415 implemented the same change in the Strada code base, observed a failure in one of the top 400 repos caused by duplicate Plugin copies from two vite packages, and remarked that Corsa better eliminated the duplication
 * (today) **ahejlsberg** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/3445#issuecomment-4300433402) **Polymath-Kaila** said "Excellent🔥"

### [PR microsoft/TypeScript-go#3454](https://github.com/microsoft/TypeScript-go/pull/3454) (Closed)

**Cancel auto\-import cache warming if changes come in while building**

*Cancel ongoing auto-import cache warming when interim snapshot changes occur to avoid rebuilding outdated registries.*

 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/3454#issuecomment-4285883821) **typescript-bot** reported a debug failure in textDocument/formatting due to a false expression: Token end is child end
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/3454#issuecomment-4285883867) **typescript-bot** reported a panic during textDocument/hover handling due to an invalid memory address or nil pointer dereference
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/3454#issuecomment-4285883907) **typescript-bot** reported a panic in textDocument/hover due to an unhandled case in Type.Target during the top 400 repos suite run
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#3455](https://github.com/microsoft/TypeScript-go/issues/3455) (Closed, `Domain: Editor`, **jakebailey**, **Copilot**)

**Wrong highlight in hover for generic func type with \`property\` and \`accessor\` prefix**

*Hovering over generic property or accessor functions loses syntax highlighting after the closing angle bracket.*

 * **Withered-Flower-0422** added label `Domain: Editor`
 * (yesterday) **jakebailey** assigned to **Copilot**, **jakebailey**
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript-go#3458](https://github.com/microsoft/TypeScript-go/pull/3458) (Closed, **jakebailey**, **Copilot**)

**Use \`typescript\` instead of \`tsx\` for hover code block language**

*Change hover tooltip code blocks to typescript instead of tsx to fix generic type highlighting issues.*

 * **Copilot** assigned to **jakebailey**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3458#issuecomment-4289326792) **jakebailey** confirmed expectation and linked to the relevant code in hover.ts
 * [today](https://github.com/microsoft/TypeScript-go/pull/3458#issuecomment-4297516959) **jakebailey** said "That would still end up causing the miscolorization of generic signatures in those files, though; otherwise I don't think we ever emit JSX-looking stuff?"
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript-go#3486](https://github.com/microsoft/TypeScript-go/pull/3486) (Closed)

**Updates to accepted/triaged submodule diffs**

*Updated accepted and triaged submodule diffs for compiler and conformance error files, excluding most JavaScript diffs.*

 * created by **RyanCavanaugh**
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#3490](https://github.com/microsoft/TypeScript-go/issues/3490) (Open, `wontfix`)

**TS2411 reported on properties declared in \`node\_modules\` \`\.d\.ts\` files \(e\.g\. @types/jsdom DOMWindow\), where tsc 6\.0 silently allows them**

*TypeScript native-preview 7.0 reports TS2411 conflicts for @types/jsdom DOMWindow properties in node_modules that tsc 6.0 silently allows.*

 * created by **tomquist**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3490#issuecomment-4298063413) **jakebailey** explained that the behavior was intentional to enable concurrent compilation since error details might vary with checking order
 * [later](https://github.com/microsoft/TypeScript-go/issues/3490#issuecomment-4305256978) **ahejlsberg** described a bug in Strada where index signature compatibility checks ran only on the first declaration encountered, causing missed diagnostics depending on file order, and noted that it was fixed in Corsa
 * **ahejlsberg** added label `wontfix`

### [Issue microsoft/TypeScript-go#3492](https://github.com/microsoft/TypeScript-go/issues/3492) (Open)

**tsgo rejects unknown JSX props that appear before a \`{\.\.\.spread}\` and are accepted by tsc 6\.0**

*tsgo incorrectly flags unknown JSX props before a spread operator as errors while TypeScript 6.0 accepts them*

 * created by **tomquist**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3492#issuecomment-4298335966) **jakebailey** explained that the code errored previously, noted a non-ideal fix for preserving spread ordering, and suggested avoiding the error by casting the object

### [Issue microsoft/TypeScript-go#3493](https://github.com/microsoft/TypeScript-go/issues/3493) (Closed, **andrewbranch**)

**\`maxNodeModuleJsDepth\` \+ \`allowJs\` does not load types from a CommonJS dependency in \`node\_modules\` \(TS7016 vs tsc 6\.0 success\)**

*tsgo fails to load types from CommonJS dependencies in node_modules with allowJs and maxNodeModuleJsDepth, causing TS7016 errors unlike tsc 6.0.*

 * (today) **ahejlsberg** assigned to **ahejlsberg**, **andrewbranch**, and unassigned **ahejlsberg**
 * **andrewbranch** added to milestone `TypeScript 7.0 RC`
 * [today](https://github.com/microsoft/TypeScript-go/issues/3493#issuecomment-4298017852) **jakebailey** clarified that the bug was due to config options parsing rather than module resolution or program loading
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3494](https://github.com/microsoft/TypeScript-go/issues/3494) (Closed, `bug`, `Domain: Type Checking`, **ahejlsberg**)

**\`keyof this\` is computed too narrowly on a subclass that passes itself as its own type parameter, causing TS2345 / TS2322 variance failure**

*Using a subclass as its own type parameter causes keyof this to exclude base class members, causing TS2322/TS2345 errors.*

 * (today) **ahejlsberg** added labels `bug`, `Domain: Type Checking`
 * [today](https://github.com/microsoft/TypeScript-go/issues/3494#issuecomment-4297199869) **ahejlsberg** confirmed that `keyof` computation was triggered on incomplete members and explained that the fix adds a member resolution status flag to the cache key
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#3497](https://github.com/microsoft/TypeScript-go/pull/3497) (Open)

**Widen types assigned to auto\-typed variables**

*Widen inferred types for auto-typed variables to accept a broader range of assignments.*

 * [today](https://github.com/microsoft/TypeScript-go/pull/3497#issuecomment-4297504524) **typescript-bot** posted automated build status updates
 * [today](https://github.com/microsoft/TypeScript-go/pull/3497#issuecomment-4297663352) **typescript-bot** posted performance run results requested by @ahejlsberg
 * [today](https://github.com/microsoft/TypeScript-go/pull/3497#issuecomment-4297722737) **typescript-bot** reported automated test results indicating potential infrastructure failures and new TS7053 errors in webpack's EnvironmentPlugin.js
 * [today](https://github.com/microsoft/TypeScript-go/pull/3497#issuecomment-4298082276) **typescript-bot** reported build comparison results between main and pull request for the top 400 repos and highlighted a TS2339 error in RooCodeInc/Roo-Code
 * [today](https://github.com/microsoft/TypeScript-go/pull/3497#issuecomment-4300255694) **ahejlsberg** said "Looks like we're fine on perf, but wondering what the changes in user tests and top 400 are about?"
 * [later](https://github.com/microsoft/TypeScript-go/pull/3497#issuecomment-4303092861) **Andarist** shared a webpack reproduction and noted that the union Record<string, CodeValue> | {} now reduces to {} due to JSLiteral flag differences affecting subtype reduction, and said they would investigate further

### [PR microsoft/TypeScript-go#3500](https://github.com/microsoft/TypeScript-go/pull/3500) (Closed)

**Include member resolution status in \`getLiteralTypeFromProperties\` key**

*Include member resolution status in the getLiteralTypeFromProperties key to properly differentiate literal types by resolution state.*

 * created by **ahejlsberg**
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#3502](https://github.com/microsoft/TypeScript-go/pull/3502) (Closed)

**Handle numbers in tsconfig parsing**

*Add support for correctly parsing integer compiler options like maxNodeModuleJsDepth in tsconfig.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3502#issuecomment-4298067939) **jakebailey** said "No, the feature works, it's just that they all go through // @maxNodeModuleJsDepth: 3 etc parsing."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3503](https://github.com/microsoft/TypeScript-go/pull/3503) (Closed)

**Fix the recursion identity for tuples from type nodes too**

*Update recursion identity logic to properly handle tuples generated from type nodes.*

 * created by **ahejlsberg**
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#3504](https://github.com/microsoft/TypeScript-go/issues/3504) (Open, `Crash`)

**Crash in declaration emit for JavaScript Test262 reserved\-words**

*Emitting declaration files panics with a nil pointer dereference when processing JavaScript Test262 reserved-word expando assignments.*

 * created by **turadg**
 * **turadg** added label `Crash`

### [PR microsoft/TypeScript-go#3505](https://github.com/microsoft/TypeScript-go/pull/3505) (Open)

**integrated filewatcher with lsp**

*Refactor vfswatch.FileWatcher for use by both CLI and LSP, integrating polling for clients without didChangeWatchedFiles support.*

 * created by **johnfav03**

### [Issue microsoft/TypeScript-go#3506](https://github.com/microsoft/TypeScript-go/issues/3506) (Open, `Crash`, **gabritto**)

**Verbose quick info crash when base type constructs an intersection**

*Requesting verbose quick info on a class extending an intersection-based mixin crashes the language server.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** added label `Crash`, and assigned to **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3506#issuecomment-4299381610) **jakebailey** said "I thought I fixed this in #3464, interesting"
 * [today](https://github.com/microsoft/TypeScript-go/issues/3506#issuecomment-4299427635) **DanielRosenwasser** said "Uh, did you mean to link to a different PR?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/3506#issuecomment-4299438244) **jakebailey** said "Technically, no, since it fixed #3466, but this is probably just a different part of the code hitting the same thing"
 * [today](https://github.com/microsoft/TypeScript-go/issues/3506#issuecomment-4299452613) **DanielRosenwasser** apologized and explained that he reported the wrong stack trace because he was running an old language server
 * [today](https://github.com/microsoft/TypeScript-go/issues/3506#issuecomment-4299456045) **DanielRosenwasser** said "That should make the fix in my PR more understandable."
 * (today) **DanielRosenwasser** assigned to **gabritto**, and unassigned **DanielRosenwasser**

### [PR microsoft/TypeScript-go#3507](https://github.com/microsoft/TypeScript-go/pull/3507) (Open)

**Avoid constructing empty \`extends\` clauses in hovers**

*Prevent hover tooltips from including empty extends clauses to improve code readability.*

 * created by **DanielRosenwasser**

### [Issue microsoft/TypeScript-go#3508](https://github.com/microsoft/TypeScript-go/issues/3508) (Open)

**Corsa no longer emits the TS\-1 internal diagnostic about pre\-emit/post\-emit diagnostic count mismatches**

*Corsa no longer emits TS-1 diagnostics for mismatched pre-emit and post-emit diagnostic counts in certain test files.*

 * created by **RyanCavanaugh**

### [Issue microsoft/TypeScript-go#3509](https://github.com/microsoft/TypeScript-go/issues/3509) (Open)

**TS2690 \(with "Did you mean 'P in K'?" mapped type suggestion\) changed to TS2693 \(generic "refers to a type, but is being used as a value"\) — mapped type suggestion lost**

*The TypeScript compiler replaced TS2690 with TS2693 for type-used-as-value errors, dropping the mapped type suggestion.*

 * created by **RyanCavanaugh**

### [Issue microsoft/TypeScript-go#3510](https://github.com/microsoft/TypeScript-go/issues/3510) (Open)

**JS: \`{} == {}\` loose equality now also flagged with TS2839**

*Loose equality comparison of two empty object literals ({} == {}) is now flagged as a TS2839 error in conformance tests.*

 * created by **RyanCavanaugh**

### [Issue microsoft/TypeScript-go#3511](https://github.com/microsoft/TypeScript-go/issues/3511) (Open)

**Unicode escapes in identifier names now displayed as literal characters**

*Identifier names containing Unicode escape sequences are now shown as their literal characters in conformance test outputs.*

 * created by **RyanCavanaugh**

### [Issue microsoft/TypeScript-go#3512](https://github.com/microsoft/TypeScript-go/issues/3512) (Closed)

**\[ServerErrors\]\[TypeScript\] main vs **

*TypeScript's main build pipeline encountered server errors during analysis of 300 GitHub repositories, yielding 31 interesting changes and various failures.*

 * created by **typescript-bot**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3512#issuecomment-4299730402) **typescript-bot** reported a panic during textDocument/formatting with a debug failure and provided the stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/3512#issuecomment-4299730483) **typescript-bot** reported a runtime panic in textDocument/hover handling due to invalid memory address or nil pointer dereference
 * [today](https://github.com/microsoft/TypeScript-go/issues/3512#issuecomment-4299730551) **typescript-bot** reported a panic due to invalid memory address or nil pointer dereference while handling a textDocument/hover request and included a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/3512#issuecomment-4299730639) **typescript-bot** reported a panic handling textDocument/hover request due to an unhandled KindPropertyAccessExpression and included a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/3512#issuecomment-4299730713) **typescript-bot** reported a runtime panic due to invalid memory address or nil pointer dereference
 * [today](https://github.com/microsoft/TypeScript-go/issues/3512#issuecomment-4299730772) **typescript-bot** reported a panic handling textDocument/hover due to an unhandled KindFunctionDeclaration case in getTargetOfAliasDeclaration
 * [today](https://github.com/microsoft/TypeScript-go/issues/3512#issuecomment-4299730865) **typescript-bot** reported a panic with a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/3512#issuecomment-4299730924) **typescript-bot** reported a panic handling textDocument/formatting due to a debug failure 'False expression: Token end is child end' and provided a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/3512#issuecomment-4299730989) **typescript-bot** reported a runtime panic due to an invalid memory address or nil pointer dereference when handling textDocument/hover
 * [today](https://github.com/microsoft/TypeScript-go/issues/3512#issuecomment-4299731062) **typescript-bot** reported a panic handling textDocument/hover due to invalid memory address or nil pointer dereference
 * [today](https://github.com/microsoft/TypeScript-go/issues/3512#issuecomment-4299731128) **typescript-bot** reported a runtime panic during textDocument/hover
 * [today](https://github.com/microsoft/TypeScript-go/issues/3512#issuecomment-4299731197) **typescript-bot** reported a runtime panic due to an invalid memory address or nil pointer dereference when handling textDocument/hover
 * [today](https://github.com/microsoft/TypeScript-go/issues/3512#issuecomment-4299731271) **typescript-bot** reported a panic handling textDocument/hover due to invalid memory address or nil pointer dereference
 * [today](https://github.com/microsoft/TypeScript-go/issues/3512#issuecomment-4299731331) **typescript-bot** reported a panic due to invalid memory address or nil pointer dereference during textDocument/hover handling
 * [today](https://github.com/microsoft/TypeScript-go/issues/3512#issuecomment-4299731398) **typescript-bot** reported a panic handling textDocument/formatting request due to a debug failure assertion
 * [today](https://github.com/microsoft/TypeScript-go/issues/3512#issuecomment-4299731480) **typescript-bot** reported server connection closed prematurely with undefined error for elastic/kibana
 * [today](https://github.com/microsoft/TypeScript-go/issues/3512#issuecomment-4299731534) **typescript-bot** reported a premature server connection closure with undefined error, listed the affected repo and included logs and repro steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/3512#issuecomment-4299731591) **typescript-bot** reported a premature server connection closure error with logs, affected repository details, and reproduction steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/3512#issuecomment-4299731666) **typescript-bot** reported server connection closed prematurely with undefined error and provided affected repos, logs, and repro steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/3512#issuecomment-4299731746) **typescript-bot** reported a premature server connection closure error for socketio/socket.io and provided repro steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/3512#issuecomment-4299731825) **typescript-bot** reported that the TypeScript server connection closed prematurely with undefined and included affected repository details, logs, and recent VS Code request traces
 * [today](https://github.com/microsoft/TypeScript-go/issues/3512#issuecomment-4299731914) **typescript-bot** reported a panic in textDocument/hover due to invalid memory address or nil pointer dereference
 * [today](https://github.com/microsoft/TypeScript-go/issues/3512#issuecomment-4299732006) **typescript-bot** reported a panic with 'invalid memory address or nil pointer dereference' during textDocument/hover handling and included a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/3512#issuecomment-4299732077) **typescript-bot** reported a panic handling textDocument/hover due to a nil pointer dereference
 * [today](https://github.com/microsoft/TypeScript-go/issues/3512#issuecomment-4299732162) **typescript-bot** logged a panic in hover request due to unhandled TypeNode KindTypeParameter
 * [today](https://github.com/microsoft/TypeScript-go/issues/3512#issuecomment-4299732243) **typescript-bot** reported a panic due to an invalid memory address or nil pointer dereference and included a stack trace
 * (later) **gabritto** closed the issue

### [PR microsoft/TypeScript-go#3513](https://github.com/microsoft/TypeScript-go/pull/3513) (Closed)

**Reenable semantic tokens**

*Reenable semantic tokens now that desync-based crashes have been resolved.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3514](https://github.com/microsoft/TypeScript-go/issues/3514) (Open)

**Illegally constructing a private/protected constructor from outside the class does not resolve to \`any\` for non\-generic classes**

*Under tsgo, illegal instantiation of a private constructor yields any for generics but retains proper type for non-generic classes.*

 * created by **Bertie690**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3514#issuecomment-4300077335) **Andarist** noted that baseline diffs already show this and suggested treating the change as intentional
 * [today](https://github.com/microsoft/TypeScript-go/issues/3514#issuecomment-4300374534) **Bertie690** noted that the inconsistency was likely accidental as `GenericA` remained typed as `any` and observed that error-suppression tools undermined the rule against making assumptions about code with errors

### [PR microsoft/TypeScript-go#3515](https://github.com/microsoft/TypeScript-go/pull/3515) (Open)

**Expose formatNodeForInsertion in internal API**

*Add the formatNodeForInsertion function to the library’s internal API to enable its use by external modules.*

 * created by **andrewbranch**

### [PR microsoft/TypeScript-go#3516](https://github.com/microsoft/TypeScript-go/pull/3516) (Closed)

**Miscellaneous extension improvements**

*Adds persistent TypeScript version picker, configurable SDK locations, debug info in server menu, and corrects diagnostic owner naming.*

 * created by **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#3517](https://github.com/microsoft/TypeScript-go/pull/3517) (Closed)

**Fix printing of property access expressions**

*Update the printer to correctly render property access expressions used in type positions when instantiation expressions are enabled.*

 * created by **gabritto**
 * (later) **gabritto** closed the issue

### [PR microsoft/TypeScript-go#3518](https://github.com/microsoft/TypeScript-go/pull/3518) (Open)

**fix\(native\-preview\): preserve lone surrogate string literals**

*Add WTF-8 support and update protocol version to preserve lone UTF-16 surrogate string literals in native-preview*

 * created by **TorinAsakura**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3518#issuecomment-4301346088) **TorinAsakura** agreed to the CLA with no company specified

### [Issue microsoft/TypeScript-go#3519](https://github.com/microsoft/TypeScript-go/issues/3519) (Open)

**Behaviour differences observed as react stuffs on a js file gets imported into another ts file**

*tsgo incorrectly reports type errors for React components and context imported from a JS file into a TSX file, whereas TypeScript 6.0 accepts them.*

 * created by **hkleungai**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3519#issuecomment-4301827880) **hkleungai** suggested a relation to issue #977, noted different errors when merging files causing consistent tsc and tsgo errors, and asked if TypeScript 7 should suppress inter-file errors like TS 6
 * [today](https://github.com/microsoft/TypeScript-go/issues/3519#issuecomment-4301970825) **jakebailey** assumed the default type parameter changed to unknown, noted the absence of the change in CHANGES.md, and asked why the code depended on code that errors
 * [today](https://github.com/microsoft/TypeScript-go/issues/3519#issuecomment-4301973165) **jakebailey** said "Ah, I just didn't notice: https://github.com/microsoft/typescript-go/blob/main/CHANGES.md#stradas-js-specific-rules-for-inferring-type-arguments-no-longer-apply-in-corsa"
 * [later](https://github.com/microsoft/TypeScript-go/issues/3519#issuecomment-4302542081) **hkleungai** explained that the code originated from very old JavaScript sources and was difficult to fully migrate to TypeScript, causing many minor syntax issues that consumers would need to patch or ignore, potentially hindering v7 adoption

### [Issue microsoft/TypeScript-go#3520](https://github.com/microsoft/TypeScript-go/issues/3520) (Open, **jakebailey**, **Copilot**)

**\`isolatedDeclarations\` with arrow functions that have default parameters**

*Using isolatedDeclarations with arrow functions that have default parameters in TSGo 7.0 causes declaration emit errors requiring explicit type annotations.*

 * created by **walkerburgin**
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#3521](https://github.com/microsoft/TypeScript-go/pull/3521) (Open, **jakebailey**, **Copilot**)

**Fix isolatedDeclarations errors for arrow functions with default parameters**

*Update pseudochecker optionality and undefined inference for default arrow function parameters to fix spurious isolatedDeclarations errors.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#3522](https://github.com/microsoft/TypeScript-go/pull/3522) (Open)

**Bring any back as default type param in JS files**

*Discuss reinstating 'any' as the default type parameter in JavaScript files, weighing its pros and cons.*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#3523](https://github.com/microsoft/TypeScript-go/pull/3523) (Open)

**Fix hover expansion for aliased default function exports**

*Corrects a crash occurring when expanding hover information for aliased default function exports.*

 * created by **Andarist**

### [PR microsoft/TypeScript-go#3524](https://github.com/microsoft/TypeScript-go/pull/3524) (Open)

**Fix hover verbosity for nested generic namespace merges**

*Adjust hover verbosity handling in nested generic namespace merges to prevent crashes during hover operations.*

 * created by **Andarist**

### [PR microsoft/TypeScript-go#3525](https://github.com/microsoft/TypeScript-go/pull/3525) (Open)

**fix\(3510\): handle object\-equality diagnostics**

*Implement correct diagnostic handling for object equality comparisons.*

 * created by **a-tarasyuk**

