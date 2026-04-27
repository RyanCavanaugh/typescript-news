# Report for 2026-04-23 (Thursday, April 23rd, 2026)

18 different users commented on 77 different issues.

## Recommended Actions

 * Response Recommended
    * @hkleungai asked if any other past PRs/commits were erased by merge racing and suggested re-merging the PR in [microsoft/TypeScript-go#3519](https://github.com/microsoft/TypeScript-go/issues/3519#issuecomment-4312182507)
    * @mikeduminy asked if the variable errors in tsgo are due to the type checker no longer bailing on deeply nested or recursive types in [microsoft/TypeScript-go#3526](https://github.com/microsoft/TypeScript-go/issues/3526#issuecomment-4306039149)
    * @mikeduminy asked if the team had seen similar behavior in [microsoft/TypeScript-go#3526](https://github.com/microsoft/TypeScript-go/issues/3526#issuecomment-4306059276)
    * @mikeduminy reported that tsgo output is non-deterministic without singleThreaded mode in [microsoft/TypeScript-go#3526](https://github.com/microsoft/TypeScript-go/issues/3526#issuecomment-4306078237)
    * @mikeduminy reported variable results with --checkers 1 in [microsoft/TypeScript-go#3526](https://github.com/microsoft/TypeScript-go/issues/3526#issuecomment-4306327062)
    * @mikeduminy provided a solution for stable error counts by removing trailing slashes in imports in [microsoft/TypeScript-go#3526](https://github.com/microsoft/TypeScript-go/issues/3526#issuecomment-4306425166)
    * @mikeduminy asked whether type checking output should be the same with and without the singleThreaded flag in [microsoft/TypeScript-go#3526](https://github.com/microsoft/TypeScript-go/issues/3526#issuecomment-4307298772)

## Activity Summary

### [Issue microsoft/TypeScript-go#2555](https://github.com/microsoft/TypeScript-go/issues/2555) (Closed, `Domain: Editor`, **andrewbranch**)

**Installing Native Preview broke TS Imports**

*Installing VS Code’s Native Preview TypeScript extension on macOS breaks TypeScript auto-import suggestions despite reverting settings and reinstalling the editor.*

 * [12 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2555#issuecomment-3809296472) **DanielRosenwasser** informed that a PR addressing the autocomplete issue had been submitted
 * (3 weeks ago) **RyanCavanaugh** set milestone to `TypeScript 7.0 RC`, and assigned to **andrewbranch**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3369](https://github.com/microsoft/TypeScript-go/pull/3369) (Open)

**Limit loader/emitter to GOMAXPROCS**

*Limit parsing and emitting workloads to a GOMAXPROCS-sized goroutine pool to prevent unbounded concurrency and stack growth.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3369#issuecomment-4227790485) **typescript-bot** posted update indicating performance test jobs started with status links
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3369#issuecomment-4227905032) **typescript-bot** shared the requested performance run results
 * (1 week ago) **jakebailey** closed the issue
 * (today) **jakebailey** reopened the issue

### [PR microsoft/TypeScript-go#3436](https://github.com/microsoft/TypeScript-go/pull/3436) (Closed)

**feat: add textDocument/\_vs\_onAutoInsert handler for VS closing tag auto\-insertion**

*Implement Visual Studio–specific _vs_onAutoInsert LSP handler and protocol types to auto-insert closing HTML/JSX tags and fix code generator jsonName bug.*

 * created by **lucygramley**
 * [6 days ago](https://github.com/microsoft/TypeScript-go/pull/3436#issuecomment-4271790692) **jakebailey** noted overlap between the code and existing tagClosing.ts and suggested consolidating instead of adding new code
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3436#issuecomment-4300584883) **jakebailey** pushed changes that deduplicated the code by using the VS style API, simplifying the implementation without affecting editor responsiveness
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3487](https://github.com/microsoft/TypeScript-go/issues/3487) (Closed)

**tsgo reports downstream TS2339 in ignored for\-of over non\-iterable union that tsc 6\.0\.2 does not**

*tsgo incorrectly emits TS2339 for property access in a for...of loop over a non-iterable union despite @ts-ignore, unlike tsc 6.0.2*

 * created by **songkeys**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3496](https://github.com/microsoft/TypeScript-go/pull/3496) (Closed)

**Fix error propagation through non\-iterable unions**

*Ensure errors are correctly propagated when handling non-iterable union types.*

 * created by **Andarist**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3497](https://github.com/microsoft/TypeScript-go/pull/3497) (Open)

**Widen types assigned to auto\-typed variables**

*Widen inferred types for auto-typed variables to accept a broader range of assignments.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3497#issuecomment-4298082276) **typescript-bot** reported build comparison results between main and pull request for the top 400 repos and highlighted a TS2339 error in RooCodeInc/Roo-Code
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3497#issuecomment-4300255694) **ahejlsberg** said "Looks like we're fine on perf, but wondering what the changes in user tests and top 400 are about?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3497#issuecomment-4303092861) **Andarist** shared a webpack reproduction and noted that the union Record<string, CodeValue> | {} now reduces to {} due to JSLiteral flag differences affecting subtype reduction, and said they would investigate further
 * [today](https://github.com/microsoft/TypeScript-go/pull/3497#issuecomment-4306383124) **Andarist** said "New tests are in now."

### [Issue microsoft/TypeScript-go#3506](https://github.com/microsoft/TypeScript-go/issues/3506) (Closed, `Crash`, **gabritto**)

**Verbose quick info crash when base type constructs an intersection**

*Requesting verbose quick info on a class extending an intersection-based mixin crashes the language server.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3506#issuecomment-4299456045) **DanielRosenwasser** said "That should make the fix in my PR more understandable."
 * (yesterday) **DanielRosenwasser** assigned to **gabritto**, and unassigned **DanielRosenwasser**
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript-go#3507](https://github.com/microsoft/TypeScript-go/pull/3507) (Closed)

**Avoid constructing empty \`extends\` clauses in hovers**

*Prevent hover tooltips from including empty extends clauses to improve code readability.*

 * created by **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3507#issuecomment-4306785054) **DanielRosenwasser** said "Closing, @gabritto has another fix in mind."
 * (today) **DanielRosenwasser** closed the issue

### [Issue microsoft/TypeScript-go#3509](https://github.com/microsoft/TypeScript-go/issues/3509) (Closed, **ahejlsberg**)

**TS2690 \(with "Did you mean 'P in K'?" mapped type suggestion\) changed to TS2693 \(generic "refers to a type, but is being used as a value"\) — mapped type suggestion lost**

*The TypeScript compiler replaced TS2690 with TS2693 for type-used-as-value errors, dropping the mapped type suggestion.*

 * created by **RyanCavanaugh**
 * **ahejlsberg** assigned to **ahejlsberg**
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#3510](https://github.com/microsoft/TypeScript-go/issues/3510) (Closed)

**JS: \`{} == {}\` loose equality now also flagged with TS2839**

*Loose equality comparison of two empty object literals ({} == {}) is now flagged as a TS2839 error in conformance tests.*

 * created by **RyanCavanaugh**
 * (today) **DanielRosenwasser** closed the issue

### [Issue microsoft/TypeScript-go#3519](https://github.com/microsoft/TypeScript-go/issues/3519) (Closed)

**Behaviour differences observed as react stuffs on a js file gets imported into another ts file**

*tsgo incorrectly reports type errors for React components and context imported from a JS file into a TSX file, whereas TypeScript 6.0 accepts them.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3519#issuecomment-4301970825) **jakebailey** assumed the default type parameter changed to unknown, noted the absence of the change in CHANGES.md, and asked why the code depended on code that errors
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3519#issuecomment-4301973165) **jakebailey** said "Ah, I just didn't notice: https://github.com/microsoft/typescript-go/blob/main/CHANGES.md#stradas-js-specific-rules-for-inferring-type-arguments-no-longer-apply-in-corsa"
 * [today](https://github.com/microsoft/TypeScript-go/issues/3519#issuecomment-4302542081) **hkleungai** explained that the code originated from very old JavaScript sources and was difficult to fully migrate to TypeScript, causing many minor syntax issues that consumers would need to patch or ignore, potentially hindering v7 adoption
 * (today) **jakebailey** closed the issue
 * [later](https://github.com/microsoft/TypeScript-go/issues/3519#issuecomment-4312182507) **hkleungai** pointed out that a commit reverted the changes from PR #3522 due to merge queue racing, wondered if other PRs were erased unnoticed, and suggested re-merging the PR
 * [later](https://github.com/microsoft/TypeScript-go/issues/3519#issuecomment-4313787867) **jakebailey** said "There was some big merge queue bug yesterday on GitHub, so we have to vet the merges :("

### [PR microsoft/TypeScript-go#3521](https://github.com/microsoft/TypeScript-go/pull/3521) (Open, **jakebailey**, **Copilot**)

**Fix isolatedDeclarations errors for arrow functions with default parameters**

*Fix isolatedDeclarations errors and optimize performance by improving pseudochecker default parameter handling and undefined recognition for arrow functions*

 * created by **Copilot**
 * (yesterday) **Copilot** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3521#issuecomment-4308665637) **jakebailey** said "@copilot+claude-opus-4.6 please resolve the reported issues; there is also similar code elsewhere like this with likely the same problem"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3521#issuecomment-4308730391) **Copilot** resolved the reported issues by adding lastRequiredParamIndex to precompute the last required parameter’s position for O(1) lookups and updated typeFromParameter, cloneParameters, and the untyped-initializer branch accordingly
 * [today](https://github.com/microsoft/TypeScript-go/pull/3521#issuecomment-4308776401) **jakebailey** said "@copilot+claude-opus-4.6 continue addressing comments"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3521#issuecomment-4308858686) **Copilot** addressed remaining comments by fixing the `lastRequiredParamIndex` doc comment and adding an early-return fast path in `typeFromParameter`

### [PR microsoft/TypeScript-go#3522](https://github.com/microsoft/TypeScript-go/pull/3522) (Closed)

**Bring any back as default type param in JS files**

*Discuss reinstating 'any' as the default type parameter in JavaScript files, weighing its pros and cons.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3523](https://github.com/microsoft/TypeScript-go/pull/3523) (Closed)

**Fix hover expansion for aliased default function exports**

*Corrects a crash occurring when expanding hover information for aliased default function exports.*

 * created by **Andarist**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3523#issuecomment-4306163169) **Andarist** said "oops, I had it and forgot to commit 🫠 fixed it now!"
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript-go#3525](https://github.com/microsoft/TypeScript-go/pull/3525) (Closed)

**fix\(3510\): handle object\-equality diagnostics**

*Implement correct diagnostic handling for object equality comparisons.*

 * created by **a-tarasyuk**
 * (today) **DanielRosenwasser** closed the issue

### [Issue microsoft/TypeScript-go#3526](https://github.com/microsoft/TypeScript-go/issues/3526) (Closed)

**Non\-deterministic error count in multi\-threaded mode**

*tsgo’s multi-threaded mode produces non-deterministic module resolution errors across runs due to race conditions, while single-threaded runs remain stable.*

 * created by **mikeduminy**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3526#issuecomment-4305923621) **jakebailey** asked for a test repository to diagnose the problem, criticized the AI summary as too generic, and clarified that --stableTypeOrdering is a noop and suggested erroring on false
 * [today](https://github.com/microsoft/TypeScript-go/issues/3526#issuecomment-4306039149) **mikeduminy** described that running tsgo on a large monorepo produced variable errors compared to tsc and asked if it was due to the type checker not bailing on deeply nested or recursive types
 * [today](https://github.com/microsoft/TypeScript-go/issues/3526#issuecomment-4306059276) **mikeduminy** said "I'll see if I can create a repro. In the meantime I thought I should report it in case others are experiencing the same thing, or perhaps your team has seen similar behavior?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/3526#issuecomment-4306061520) **jakebailey** pointed out that this was a different issue than inconsistent module resolution, suggested filing a separate bug, and requested error details
 * [today](https://github.com/microsoft/TypeScript-go/issues/3526#issuecomment-4306078237) **mikeduminy** explained that tsgo output was non-deterministic without singleThreaded mode, causing a variable number of errors and module resolution failures
 * [today](https://github.com/microsoft/TypeScript-go/issues/3526#issuecomment-4306327062) **mikeduminy** said "Interestingly when I run with --checkers 1 I also get variable results"
 * [today](https://github.com/microsoft/TypeScript-go/issues/3526#issuecomment-4306349726) **jakebailey** clarified that the described variable results are module resolution errors unrelated to the checker count
 * [today](https://github.com/microsoft/TypeScript-go/issues/3526#issuecomment-4306360673) **jakebailey** said "Can you post your tsconfig? Do you have incremental mode enabled?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/3526#issuecomment-4306378699) **DanielRosenwasser** said "Also, if --incremental is on, knowing specifically what is varying in your .tsbuildinfo files between builds would be helpful."
 * [today](https://github.com/microsoft/TypeScript-go/issues/3526#issuecomment-4306425166) **mikeduminy** described fixing the issue by removing trailing slashes from package imports, which stabilized error counts in multi-threaded mode
 * [today](https://github.com/microsoft/TypeScript-go/issues/3526#issuecomment-4306774981) **jakebailey** said "I think I might have identified the bug with the above note. Can you build https://github.com/microsoft/typescript-go/pull/3534 and see if it works for you?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/3526#issuecomment-4307298772) **mikeduminy** thanked and said they would test when it was out in the nightlies, and asked whether type checking output should be the same with and without the singleThreaded flag
 * [today](https://github.com/microsoft/TypeScript-go/issues/3526#issuecomment-4307372614) **jakebailey** said "Best case yes, but you have overlap I'm sure means you'll drop down to 12 errors both ways. File a new issue for that one with more info"
 * (today) **jakebailey** closed the issue
 * [later](https://github.com/microsoft/TypeScript-go/issues/3526#issuecomment-4312300979) **mikeduminy** notified that the trailing slash problem was fixed in version 7.0.0-dev.20260424.1 and thanked

### [PR microsoft/TypeScript-go#3527](https://github.com/microsoft/TypeScript-go/pull/3527) (Closed)

**Add CLI and LSP attach to launch\.template**

*Add CLI and LSP server attach configurations to the Go launch.template for easier debugging of LSP processes*

 * created by **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#3528](https://github.com/microsoft/TypeScript-go/pull/3528) (Open)

**chore: fix some minor issues in comments**

*Fix minor typos and inconsistencies in code comments.*

 * created by **purelualight**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3528#issuecomment-4306110575) **purelualight** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3528#issuecomment-4306115325) **purelualight** quoted the Contributor License Agreement and provided instructions on how to agree with it
 * [today](https://github.com/microsoft/TypeScript-go/pull/3528#issuecomment-4306116514) **purelualight** said "@microsoft-github-policy-service agree"

### [PR microsoft/TypeScript-go#3529](https://github.com/microsoft/TypeScript-go/pull/3529) (Closed)

**Fix \`maybeMappedType\` function**

*Correct the maybeMappedType function to properly handle mapped types and resolve related errors.*

 * created by **ahejlsberg**
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#3530](https://github.com/microsoft/TypeScript-go/issues/3530) (Closed, `wontfix`)

**Regression: yup\.ObjectSchema\<T\> no longer assignable to ObjectSchema\<any\> \(20260423\.1\)**

*Regression in @typescript/native-preview@7.0.0-dev.20260423.1 makes yup.ObjectSchema<T> incompatible with ObjectSchema<any>, triggering type errors in yupResolver calls.*

 * created by **modosc**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3530#issuecomment-4307118537) **Andarist** provided a self-isolated reproduction snippet
 * [today](https://github.com/microsoft/TypeScript-go/issues/3530#issuecomment-4307464949) **Andarist** explained that a recent PR improved correctness by unmasking the real issue in the user's code, described how Partial distributes and suggested using a different accepts constraint
 * **ahejlsberg** added label `wontfix`

### [PR microsoft/TypeScript-go#3531](https://github.com/microsoft/TypeScript-go/pull/3531) (Open)

**Preserve escaped identifier spelling in unresolved name diagnostics**

*Preserve original escaped identifier spelling in unresolved name diagnostics to improve error message clarity.*

 * created by **Andarist**

### [PR microsoft/TypeScript-go#3532](https://github.com/microsoft/TypeScript-go/pull/3532) (Closed)

**Fix missing slices\.Clone**

*An unnoticed bug in the Clone method results in lost slices, discovered accidentally with unknown effects.*

 * created by **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#3533](https://github.com/microsoft/TypeScript-go/issues/3533) (Closed, **jakebailey**, **Copilot**)

**Duplicate fixes for isolatedDeclarations code actions**

*TypeScript language service returns three identical quickfix suggestions for function property assignments with --isolatedDeclarations enabled*

 * created by **DanielRosenwasser**
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3534](https://github.com/microsoft/TypeScript-go/pull/3534) (Closed)

**Remove trailing dir separator in loadModuleFromSpecificNodeModulesDirectory**

*Remove the unnecessary trailing directory separator in loadModuleFromSpecificNodeModulesDirectory to improve module resolution*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3535](https://github.com/microsoft/TypeScript-go/pull/3535) (Closed, **jakebailey**, **Copilot**)

**Fix duplicate isolatedDeclarations code actions for expando functions**

*Deduplicate identical type annotation code actions for expando function properties under isolatedDeclarations*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3535#issuecomment-4307014209) **jakebailey** said "@copilot+claude-opus-4.6 This deduplicates based on description, but, are we certain that they are actually the same fixes outside their strings?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3535#issuecomment-4307110638) **Copilot** acknowledged the issue and updated the deduplication logic to compare full code action content
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3536](https://github.com/microsoft/TypeScript-go/pull/3536) (Closed)

**Include compilerOptions\.types in auto\-import packages**

*Include TypeScript compilerOptions.types entries when generating auto-import packages.*

 * created by **andrewbranch**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3537](https://github.com/microsoft/TypeScript-go/pull/3537) (Closed)

**Work around overzealous stack telemetry redaction**

*Work around VS Code telemetry client’s overzealous regex that redacts entire payloads on encountering strings like getSignature( or GeyKey(.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3538](https://github.com/microsoft/TypeScript-go/pull/3538) (Closed)

**Print heritage clause elements as declared in expandable hover**

*Change expandable hover to display heritage clause elements exactly as declared instead of reconstructing their types.*

 * created by **gabritto**
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript-go#3539](https://github.com/microsoft/TypeScript-go/pull/3539) (Closed)

**Document changes in \.js \-\> \.d\.ts emit**

*Document recent changes in the .d.ts output generated from .js source files.*

 * created by **RyanCavanaugh**
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#3540](https://github.com/microsoft/TypeScript-go/pull/3540) (Closed)

**Triage or accept \.js and \.d\.ts diffs**

*Review and decide on accepting .js and .d.ts baseline file diffs, with .types updates to follow.*

 * created by **RyanCavanaugh**

### [PR microsoft/TypeScript-go#3541](https://github.com/microsoft/TypeScript-go/pull/3541) (Open)

**Collect this property assignments in JS declaration emit and transform them to TS declarations**

*Expand JS declaration emit to support 'this' assignments, require imports, module.exports class hoisting, and static block expando tests.*

 * created by **weswigham**

### [Issue microsoft/TypeScript-go#3542](https://github.com/microsoft/TypeScript-go/issues/3542) (Open, `Domain: Declaration Emit`)

**Baselines: JS declaration emit adds \`export import\` modifier for require\-style import assignments**

*JS declaration emit adds export import modifiers to require-style assignments, changing the public API by exposing internal imports.*

 * created by **RyanCavanaugh**

### [Issue microsoft/TypeScript-go#3543](https://github.com/microsoft/TypeScript-go/issues/3543) (Open, `Domain: Declaration Emit`)

**Baselines: CJS \`module\.exports = {}\` now emits \`export = \_default\` with inlined object type instead of named exports**

*CJS module.exports patterns now emit export = _default with inlined object types instead of named exports, requiring semantic validation*

 * created by **RyanCavanaugh**

### [Issue microsoft/TypeScript-go#3544](https://github.com/microsoft/TypeScript-go/issues/3544) (Open, `Domain: Declaration Emit`)

**Baselines: CJS class expression exports emit anonymous constructor types instead of named class declarations**

*CJS class expression exports emit anonymous constructor types in .d.ts files, producing malformed import types and TypeScript errors.*

 * created by **RyanCavanaugh**

### [Issue microsoft/TypeScript-go#3545](https://github.com/microsoft/TypeScript-go/issues/3545) (Open, `Domain: Declaration Emit`)

**Baselines: CJS export alias and element access patterns changed**

*Declaration output now differs for CommonJS export aliases and module.exports element access patterns, including duplicate assignments.*

 * created by **RyanCavanaugh**

### [Issue microsoft/TypeScript-go#3546](https://github.com/microsoft/TypeScript-go/issues/3546) (Open, `bug`, `Domain: Declaration Emit`, **weswigham**)

**Declaration emit doesn't property handle CJS imports**

*tsgo’s declaration emitter for CommonJS modules omits necessary import statements, resulting in incorrect .d.ts output.*

 * created by **ahejlsberg**
 * (today) **ahejlsberg** added labels `bug`, `Domain: Declaration Emit`, set milestone to `TypeScript 7.0 RC`, and assigned to **weswigham**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3546#issuecomment-4309229554) **weswigham** referenced PR #3541 as already fixing the issue

### [Issue microsoft/TypeScript-go#3547](https://github.com/microsoft/TypeScript-go/issues/3547) (Open, `Domain: Declaration Emit`)

**Baselines: Namespace\-to\-const restructuring with DtsFileErrors \(redeclaration errors\)**

*Namespace-to-const transformation in baselines erroneously produces invalid .d.ts files with TS2451 redeclaration errors.*

 * created by **RyanCavanaugh**

### [Issue microsoft/TypeScript-go#3548](https://github.com/microsoft/TypeScript-go/issues/3548) (Open)

**Baselines: Decorator metadata reflects stable union type ordering**

*Reflect.getMetadata design:type for T|null unions now reports the non-null type instead of Object due to updated decorator metadata ordering.*

 * created by **RyanCavanaugh**

### [Issue microsoft/TypeScript-go#3549](https://github.com/microsoft/TypeScript-go/issues/3549) (Open, `Domain: Declaration Emit`)

**Baselines: Missing generic type arguments no longer auto\-filled with any \(produces TS2314 errors\)**

*Generic types without explicit parameters now emit bare types instead of defaulting to any, causing TS2314 errors*

 * created by **RyanCavanaugh**

### [Issue microsoft/TypeScript-go#3550](https://github.com/microsoft/TypeScript-go/issues/3550) (Open, `wontfix`, `Domain: Declaration Emit`)

**Baselines: Optional property types in JS declarations drop \| undefined**

*Optional property types in JS declarations are incorrectly simplified by removing | undefined from the type signature.*

 * created by **RyanCavanaugh**

### [Issue microsoft/TypeScript-go#3551](https://github.com/microsoft/TypeScript-go/issues/3551) (Open, `Domain: Declaration Emit`)

**Baselines: Output file ordering changed \+ declaration types resolve to any instead of typeof references**

*Declaration emit with package exports tests now reorder output file sections and produce declaration types as any rather than typeof references*

 * created by **RyanCavanaugh**

### [Issue microsoft/TypeScript-go#3552](https://github.com/microsoft/TypeScript-go/issues/3552) (Open, `wontfix`, `Domain: Declaration Emit`)

**Baselines: export = a reordered; ESM side\-effect import replaces export {}**

*Baseline diffs indicate that CommonJS export assignments are reordered after declarations and empty ES exports are replaced by side-effect imports.*

 * created by **RyanCavanaugh**

### [Issue microsoft/TypeScript-go#3553](https://github.com/microsoft/TypeScript-go/issues/3553) (Closed, `Domain: Emit`, **DanielRosenwasser**, **Copilot**)

**Baselines: JSX factory call changed from indirect \(0, \_a\.jsx\)\(\.\.\.\) to direct \_jsx\(\.\.\.\) call**

*JSX emit now uses direct _jsx(...) function calls instead of comma-expression indirection for factory invocations.*

 * created by **RyanCavanaugh**

### [Issue microsoft/TypeScript-go#3554](https://github.com/microsoft/TypeScript-go/issues/3554) (Closed, `wontfix`, **ahejlsberg**)

**Baselines: null\-initialized variable inferred as any instead of null type**

*Variables initialized with null are incorrectly inferred as any instead of null type.*

 * created by **RyanCavanaugh**
 * (today) **ahejlsberg** added label `Domain: Type Checking`, and assigned to **ahejlsberg**
 * [later](https://github.com/microsoft/TypeScript-go/issues/3554#issuecomment-4314143927) **ahejlsberg** identified an issue in Strada where the auto-typed variable `l11` was mis-serialized as non-auto-typed because of its null initializer
 * (later) **ahejlsberg** added label `wontfix`, and removed label `Domain: Type Checking`

### [Issue microsoft/TypeScript-go#3555](https://github.com/microsoft/TypeScript-go/issues/3555) (Open, `Domain: Declaration Emit`)

**Baselines: @overload handling changes in JS declaration emit**

*JS declaration emit for JSDoc @overload alters overload output by removing or duplicating comments, losing type parameters, and collapsing signatures.*

 * created by **RyanCavanaugh**

### [Issue microsoft/TypeScript-go#3556](https://github.com/microsoft/TypeScript-go/issues/3556) (Open, `Domain: Declaration Emit`)

**Baselines: @callback/@overload tags reordered and restructured in declaration emit**

*Declaration emit reorders callback and overload tags, simplifies type definitions, and mistakenly changes rest parameters from string[] to string.*

 * created by **RyanCavanaugh**

### [Issue microsoft/TypeScript-go#3557](https://github.com/microsoft/TypeScript-go/issues/3557) (Open, `Domain: Parser`)

**Baselines: @satisfies tag handling changes: functions become const declarations**

*Functions annotated with @satisfies now become declare const arrow functions with changed parameter types and added @param/@satisfies annotations*

 * created by **RyanCavanaugh**

### [Issue microsoft/TypeScript-go#3558](https://github.com/microsoft/TypeScript-go/issues/3558) (Open, `Domain: Declaration Emit`, **DanielRosenwasser**, **Copilot**)

**Baselines: Labeled statement followed by export declaration loses original text**

*Labeled statements followed by export declarations lose their original semicolon in emitted baselines*

 * created by **RyanCavanaugh**

### [Issue microsoft/TypeScript-go#3559](https://github.com/microsoft/TypeScript-go/issues/3559) (Open, `Domain: Declaration Emit`)

**Baselines: CJS exports pattern changes in declaration emit**

*CommonJS declaration emit restructuring changed baselines, causing some files to lose exports entirely.*

 * created by **RyanCavanaugh**

### [Issue microsoft/TypeScript-go#3560](https://github.com/microsoft/TypeScript-go/issues/3560) (Open, `Domain: Declaration Emit`)

**Baselines: exportNonInitializedVariables crash in declaration emit**

*Declaration emit crashes when exporting non-initialized variables in commonjs module baselines tests.*

 * created by **RyanCavanaugh**

### [Issue microsoft/TypeScript-go#3561](https://github.com/microsoft/TypeScript-go/issues/3561) (Open, `wontfix`, `Domain: Declaration Emit`)

**Baselines: noImplicitThis functions returning this now fully expand the object type**

*Functions returning this under noImplicitThis now emit fully expanded object types instead of any, changing type contracts.*

 * created by **RyanCavanaugh**

### [Issue microsoft/TypeScript-go#3562](https://github.com/microsoft/TypeScript-go/issues/3562) (Open, `Domain: Type Checking`)

**Baselines: JSDoc module namepath module:A emits as unresolved module instead of any**

*JSDoc module namepath syntax (module:A) now emits an unresolved module rather than any, producing type errors.*

 * created by **RyanCavanaugh**

### [Issue microsoft/TypeScript-go#3563](https://github.com/microsoft/TypeScript-go/issues/3563) (Open, **ahejlsberg**)

**Baselines: definiteAssignment shorthand in object literal loses optional modifier**

*Optional method properties in object literal shorthand lose their optional modifier when emitted with definite assignment assertions.*

 * created by **RyanCavanaugh**

### [Issue microsoft/TypeScript-go#3564](https://github.com/microsoft/TypeScript-go/issues/3564) (Open, `Domain: Type Checking`)

**Baselines: Generic function parameter inference change**

*Baseline tests updated to reflect generic function parameter inference changing x3’s type from any[] to any[][].*

 * created by **RyanCavanaugh**

### [Issue microsoft/TypeScript-go#3565](https://github.com/microsoft/TypeScript-go/issues/3565) (Open, `Domain: Declaration Emit`)

**Baselines: Declaration emit trailing comma changes in destructuring parameters**

*Declaration emit baselines remove extra trailing commas after omitted elements in destructuring parameters.*

 * created by **RyanCavanaugh**

### [Issue microsoft/TypeScript-go#3566](https://github.com/microsoft/TypeScript-go/issues/3566) (Open, `Domain: Declaration Emit`)

**Baselines: Late\-bound computed property \[prop\] preserved instead of resolved to plain prop**

*Late-bound computed property [prop] syntax is preserved instead of being resolved to plain prop*

 * created by **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3566#issuecomment-4309176683) **RyanCavanaugh** said "This seems like a won't fix, actually. Both emits are equivalent."

### [Issue microsoft/TypeScript-go#3567](https://github.com/microsoft/TypeScript-go/issues/3567) (Open, `Domain: Declaration Emit`)

**Baselines: Symbol getter/setter declaration emit change**

*Declaration outputs now change the return type of symbol getters/setters to undefined and introduce a new Symbol.toPrimitive overload.*

 * created by **RyanCavanaugh**

### [Issue microsoft/TypeScript-go#3568](https://github.com/microsoft/TypeScript-go/issues/3568) (Open, `Domain: Declaration Emit`)

**Baselines: export as namespace added or restructured in declaration emit**

*Add or restructure ‘export as namespace GLO’ in declaration emit baselines to update module global visibility and public API contract.*

 * created by **RyanCavanaugh**

### [Issue microsoft/TypeScript-go#3569](https://github.com/microsoft/TypeScript-go/issues/3569) (Open, `Domain: Declaration Emit`)

**Baselines: Declaration emit simplification of class extending built\-in Array**

*Declaration emit now simplifies classes extending built-in Array by dropping the generic parameter and removing inherited constructor overloads.*

 * created by **RyanCavanaugh**

### [Issue microsoft/TypeScript-go#3570](https://github.com/microsoft/TypeScript-go/issues/3570) (Open, `Domain: Declaration Emit`)

**Baselines: Declaration emit type parameter renaming bug \(regression\)**

*Declaration emit incorrectly renames type parameters to T_1, leading to undefined types and TS2304 errors*

 * created by **RyanCavanaugh**

### [Issue microsoft/TypeScript-go#3571](https://github.com/microsoft/TypeScript-go/issues/3571) (Closed, **ahejlsberg**)

**Module augmentation not merged when upstream \.d\.ts uses top\-level \`export interface\` \+ self\-referential \`declare module \.\.\. export =\`**

*tsgo doesn't merge module augmentations for packages whose .d.ts combine a top-level export interface with export= declarations*

 * created by **winrid**

### [PR microsoft/TypeScript-go#3572](https://github.com/microsoft/TypeScript-go/pull/3572) (Open)

**Enter signature scope in SerializeReturnTypeForSignature**

*Add signature scope support to SerializeReturnTypeForSignature for accurate return type serialization*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#3573](https://github.com/microsoft/TypeScript-go/pull/3573) (Open)

**Optimize type variable scope map cloning with CoW**

*Reintroduce copy-on-write for type variable scope maps to cut 720k allocations in the test suite.*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#3574](https://github.com/microsoft/TypeScript-go/pull/3574) (Open)

**fix\(3565\): preserve trailing commas in declaration\-emitted array binding patterns**

*Ensure trailing commas are retained in array binding patterns generated in declarations.*

 * created by **a-tarasyuk**

### [PR microsoft/TypeScript-go#3575](https://github.com/microsoft/TypeScript-go/pull/3575) (Open)

**Avoid over\-expanding recursive constraints in \`getBaseSignature\`**

*Prevent excessive expansion of recursive type constraints in the getBaseSignature function.*

 * created by **Andarist**

### [Issue microsoft/TypeScript-go#3576](https://github.com/microsoft/TypeScript-go/issues/3576) (Closed)

**\[Proposal\] strictArrayVariance: opt\-in invariance for mutable Array\<T\> element type \(post\-7\.0 discussion\)**

*Introduce a strictArrayVariance compiler option to enforce invariant element types on mutable arrays, preventing unsound covariance.*

 * created by **JustFly1984**
 * [later](https://github.com/microsoft/TypeScript-go/issues/3576#issuecomment-4313817349) **jakebailey** said "This is most certainly the wrong repo to file this in. We are not adding new features in 7.0. Those need to wait for 7.1, and will not be taken in this repo."

### [PR microsoft/TypeScript-go#3577](https://github.com/microsoft/TypeScript-go/pull/3577) (Closed)

**feat\(checker\): strictArrayVariance flag — invariant mutable Array\<T\> element type \(DRAFT for post\-7\.0 discussion\)**

*Add a draft compiler option strictArrayVariance to enforce invariant element types for mutable arrays and tuples.*

 * created by **JustFly1984**
 * [later](https://github.com/microsoft/TypeScript-go/pull/3577#issuecomment-4312569206) **JustFly1984** said "@microsoft-github-policy-service agree [company="JustFly1984"]"
 * [later](https://github.com/microsoft/TypeScript-go/pull/3577#issuecomment-4312578118) **JustFly1984** said "@microsoft-github-policy-service agree"
 * [later](https://github.com/microsoft/TypeScript-go/pull/3577#issuecomment-4312579805) **JustFly1984** said "@microsoft-github-policy-service agree company="JustFly1984""

### [PR microsoft/TypeScript-go#3578](https://github.com/microsoft/TypeScript-go/pull/3578) (Open)

**Preserve JSDoc parameter types on functions wrapped by \`@satisfies\`**

*Functions wrapped by @satisfies currently lose their JSDoc parameter types and require preservation.*

 * created by **Andarist**

### [Issue microsoft/TypeScript-go#3580](https://github.com/microsoft/TypeScript-go/issues/3580) (Closed, `Domain: Editor`)

**No code actions available when attempting to use refactorings in VS Code with new typescript\-go preview**

*TypeScript Native Preview's refactoring context menu fails to show in VS Code, displaying “No code actions available”.*

 * created by **jpierson-at-riis**
 * **jpierson-at-riis** added label `Domain: Editor`
 * [later](https://github.com/microsoft/TypeScript-go/issues/3580#issuecomment-4313762911) **jakebailey** said "#2227 "
 * (later) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3581](https://github.com/microsoft/TypeScript-go/pull/3581) (Closed)

**Restore \#3522 and \#3516**

*Restore pull requests #3522 and #3516 that were dropped by yesterday’s GitHub merge queue bug.*

 * created by **jakebailey**
 * [later](https://github.com/microsoft/TypeScript-go/pull/3581#issuecomment-4314307272) **jakebailey** said "@andrewbranch I think those comments might be correct for #3516, reading..."
 * (later) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3582](https://github.com/microsoft/TypeScript-go/pull/3582) (Closed)

**Move test to accepted bucket**

*Reclassify the test by moving it from its current location into the accepted bucket.*

 * created by **ahejlsberg**

### [Issue microsoft/TypeScript-go#3583](https://github.com/microsoft/TypeScript-go/issues/3583) (Closed, **jakebailey**, **Copilot**)

**Support disabling ATA via VS Code settings for inferred projects**

*Native Preview TypeScript language server ignores VS Code Automatic Type Acquisition disable settings for inferred projects, causing unwanted type installs.*

 * created by **ekazakov14**
 * [later](https://github.com/microsoft/TypeScript-go/issues/3583#issuecomment-4314421930) **jakebailey** identified missing user preferences and suggested adding options with JSON snippets and provided precedence logic
 * (later) **jakebailey** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#3584](https://github.com/microsoft/TypeScript-go/pull/3584) (Closed, **jakebailey**, **Copilot**)

**Support disabling ATA via VS Code settings for inferred projects**

*Add VS Code settings to disable automatic type acquisition in inferred projects with dynamic refresh handling and tests.*

 * created by **Copilot**
 * (later) **Copilot** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#919](https://github.com/microsoft/TypeScript-go/issues/919) (Closed, `Domain: Editor`)

**extension: command 'typescript\.goToSourceDefinition' not found**

*Using VSCode's Go to Source Definition with the tsgo extension fails with 'typescript.goToSourceDefinition' command not found error.*

 * created by **tmm1**
 * **jakebailey** added label `Domain: LSP`
 * **RyanCavanaugh** added to milestone `Post-7.0`
 * (today) **DanielRosenwasser** closed the issue

