# Report for 2026-04-24 (Friday, April 24th, 2026)

19 different users commented on 65 different issues.

## Recommended Actions

 * Response Recommended
    * @winrid provided repro steps and details for a tsgo file-order augmentation bug in [microsoft/TypeScript-go#3571](https://github.com/microsoft/TypeScript-go/issues/3571#issuecomment-4315355813)
    * @hkleungai asked if tsgo could throw TS5025 instead of TS5023 in this case in [microsoft/TypeScript-go#3589](https://github.com/microsoft/TypeScript-go/pull/3589#issuecomment-4318121984)

## Activity Summary

### [PR microsoft/TypeScript-go#2302](https://github.com/microsoft/TypeScript-go/pull/2302) (Closed)

**API over LSP implementation**

*Implements a TS-Go API over the Language Server Protocol using custom messages and lazy-loaded types and symbols.*

 * [19 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2302#issuecomment-3631616041) **aleksei-berezkin** said "@microsoft-github-policy-service agree company="JetBrains""
 * [9 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2302#issuecomment-3930927747) **nnnnoel** asked if a linked PR would be helpful to support typescript-go in WebStorm
 * [8 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2302#issuecomment-3932853572) **aleksei-berezkin** explained how to configure WebStorm to use TypeScript-Go via a dependency and npm install, and noted that the Service-Powered Type Engine is not yet implemented but available in a fork
 * [later](https://github.com/microsoft/TypeScript-go/pull/2302#issuecomment-4318548224) **aleksei-berezkin** closed the PR after using it as an example implementation and decided to focus on supporting the upstream TS-Go API instead of their fork
 * (later) **aleksei-berezkin** closed the issue

### [Issue microsoft/TypeScript-go#2582](https://github.com/microsoft/TypeScript-go/issues/2582) (Closed, `Domain: Editor`, **andrewbranch**)

**Auto\-import does not suggest updates from symlinked monorepo package sources**

*VS Code’s auto-import feature does not suggest updated symbols from symlinked packages in a monorepo workspace*

 * **ericnorris** added label `Domain: Editor`
 * **andrewbranch** assigned to **andrewbranch**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * (today) **andrewbranch** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/issues/2582#issuecomment-4315486600) **jakebailey** said "The fix is being reverted in #3587, I'm afraid; it has a data race."
 * (today) **jakebailey** reopened the issue
 * (today) **andrewbranch** closed the issue
 * (today) **jakebailey** reopened the issue
 * [today](https://github.com/microsoft/TypeScript-go/issues/2582#issuecomment-4316268131) **jakebailey** said "Ah, sorry, #3590 did reapply the change."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2914](https://github.com/microsoft/TypeScript-go/pull/2914) (Closed)

**adds tracing \(\-\-generateTrace\)**

*Implement a tracing feature with --generateTrace to output types.json and trace.json files using a context-based approach.*

 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/2914#issuecomment-4297568355) **dimitropoulos** rebased the branch onto origin/main, addressed remaining review feedback in follow-up commits, ran tests, lint, build, and format, and force-pushed the rebased branch
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/2914#issuecomment-4297573073) **dimitropoulos** rebased the branch onto origin/main, addressed remaining review feedback in follow-up commits, ran tests, lint, build, and format, and force-pushed the rebased branch
 * (today) **jakebailey** closed the issue
 * (today) **jakebailey** reopened the issue
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3057](https://github.com/microsoft/TypeScript-go/pull/3057) (Closed)

**fix: invalidate symlinked packages in auto\-import cache**

*Auto-import cache now invalidates correctly for symlinked packages by including them in its tracking map.*

 * created by **ericnorris**
 * [1 month ago](https://github.com/microsoft/TypeScript-go/pull/3057#issuecomment-4143747988) **ericnorris** said "@microsoft-github-policy-service agree company="Etsy""
 * [today](https://github.com/microsoft/TypeScript-go/pull/3057#issuecomment-4314554294) **ericnorris** thanked @andrewbranch for the feedback and asked for a second review of the latest commit
 * (today) **andrewbranch** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/3057#issuecomment-4315466762) **jakebailey** said "The data races on main and in other PRs are actually coming from this PR."
 * [today](https://github.com/microsoft/TypeScript-go/pull/3057#issuecomment-4315504155) **ericnorris** apologized and asked where the data races occur
 * [today](https://github.com/microsoft/TypeScript-go/pull/3057#issuecomment-4315552180) **andrewbranch** said "I think this was a pre-existing issue that was just under-exercised (at least in tests) the way the old code worked. I'm working on a fix!"

### [Issue microsoft/TypeScript-go#3530](https://github.com/microsoft/TypeScript-go/issues/3530) (Closed, `wontfix`)

**Regression: yup\.ObjectSchema\<T\> no longer assignable to ObjectSchema\<any\> \(20260423\.1\)**

*Regression in @typescript/native-preview@7.0.0-dev.20260423.1 makes yup.ObjectSchema<T> incompatible with ObjectSchema<any>, triggering type errors in yupResolver calls.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3530#issuecomment-4307118537) **Andarist** provided a self-isolated reproduction snippet
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3530#issuecomment-4307464949) **Andarist** explained that a recent PR improved correctness by unmasking the real issue in the user's code, described how Partial distributes and suggested using a different accepts constraint
 * **ahejlsberg** added label `wontfix`
 * [today](https://github.com/microsoft/TypeScript-go/issues/3530#issuecomment-4314639923) **modosc** said "thanks @Andarist - should i close this out and open an issue upstream with yup? nm, i see. closing out. "
 * (today) **modosc** closed the issue

### [PR microsoft/TypeScript-go#3540](https://github.com/microsoft/TypeScript-go/pull/3540) (Closed)

**Triage or accept \.js and \.d\.ts diffs**

*Review and decide on accepting .js and .d.ts baseline file diffs, with .types updates to follow.*

 * created by **RyanCavanaugh**
 * (today) **jakebailey** closed the issue
 * (today) **jakebailey** reopened the issue
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#3542](https://github.com/microsoft/TypeScript-go/issues/3542) (Open, `Domain: Declaration Emit`)

**Baselines: JS declaration emit adds \`export import\` modifier for require\-style import assignments**

*JS declaration emit adds export import modifiers to require-style assignments, changing the public API by exposing internal imports.*

 * created by **RyanCavanaugh**
 * **ahejlsberg** added label `Domain: Declaration Emit`

### [Issue microsoft/TypeScript-go#3543](https://github.com/microsoft/TypeScript-go/issues/3543) (Open, `Domain: Declaration Emit`)

**Baselines: CJS \`module\.exports = {}\` now emits \`export = \_default\` with inlined object type instead of named exports**

*CJS module.exports patterns now emit export = _default with inlined object types instead of named exports, requiring semantic validation*

 * created by **RyanCavanaugh**
 * **ahejlsberg** added label `Domain: Declaration Emit`

### [Issue microsoft/TypeScript-go#3544](https://github.com/microsoft/TypeScript-go/issues/3544) (Open, `Domain: Declaration Emit`)

**Baselines: CJS class expression exports emit anonymous constructor types instead of named class declarations**

*CJS class expression exports emit anonymous constructor types in .d.ts files, producing malformed import types and TypeScript errors.*

 * created by **RyanCavanaugh**
 * **ahejlsberg** added label `Domain: Declaration Emit`

### [Issue microsoft/TypeScript-go#3545](https://github.com/microsoft/TypeScript-go/issues/3545) (Open, `Domain: Declaration Emit`)

**Baselines: CJS export alias and element access patterns changed**

*Declaration output now differs for CommonJS export aliases and module.exports element access patterns, including duplicate assignments.*

 * created by **RyanCavanaugh**
 * **ahejlsberg** added label `Domain: Declaration Emit`

### [Issue microsoft/TypeScript-go#3547](https://github.com/microsoft/TypeScript-go/issues/3547) (Open, `Domain: Declaration Emit`)

**Baselines: Namespace\-to\-const restructuring with DtsFileErrors \(redeclaration errors\)**

*Namespace-to-const transformation in baselines erroneously produces invalid .d.ts files with TS2451 redeclaration errors.*

 * created by **RyanCavanaugh**
 * **ahejlsberg** added label `Domain: Declaration Emit`

### [Issue microsoft/TypeScript-go#3549](https://github.com/microsoft/TypeScript-go/issues/3549) (Open, `Domain: Declaration Emit`)

**Baselines: Missing generic type arguments no longer auto\-filled with any \(produces TS2314 errors\)**

*Generic types without explicit parameters now emit bare types instead of defaulting to any, causing TS2314 errors*

 * created by **RyanCavanaugh**
 * **ahejlsberg** added label `Domain: Declaration Emit`

### [Issue microsoft/TypeScript-go#3550](https://github.com/microsoft/TypeScript-go/issues/3550) (Open, `wontfix`, `Domain: Declaration Emit`)

**Baselines: Optional property types in JS declarations drop \| undefined**

*Optional property types in JS declarations are incorrectly simplified by removing | undefined from the type signature.*

 * created by **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3550#issuecomment-4316107656) **ahejlsberg** said "New declaration emit looks reasonable to me."
 * **ahejlsberg** added label `Domain: Declaration Emit`
 * [today](https://github.com/microsoft/TypeScript-go/issues/3550#issuecomment-4316567837) **RyanCavanaugh** said "Yeah, this is the right behavior under EOPT=false since it's local to the function"
 * **RyanCavanaugh** added label `wontfix`

### [Issue microsoft/TypeScript-go#3551](https://github.com/microsoft/TypeScript-go/issues/3551) (Open, `Domain: Declaration Emit`)

**Baselines: Output file ordering changed \+ declaration types resolve to any instead of typeof references**

*Declaration emit with package exports tests now reorder output file sections and produce declaration types as any rather than typeof references*

 * created by **RyanCavanaugh**
 * **ahejlsberg** added label `Domain: Declaration Emit`

### [Issue microsoft/TypeScript-go#3552](https://github.com/microsoft/TypeScript-go/issues/3552) (Open, `Domain: Declaration Emit`, **andrewbranch**, **RyanCavanaugh**, **Copilot**)

**Baselines: export = a reordered; ESM side\-effect import replaces export {}**

*Baseline diffs indicate that CommonJS export assignments are reordered after declarations and empty ES exports are replaced by side-effect imports.*

 * created by **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3552#issuecomment-4316083587) **ahejlsberg** said "New declaration emit seems reasonable and closer to the original source."
 * **ahejlsberg** added label `Domain: Declaration Emit`
 * [today](https://github.com/microsoft/TypeScript-go/issues/3552#issuecomment-4316474497) **RyanCavanaugh** agreed and demonstrated the diff showing moving export = and retaining import "fs" to remove export {}
 * **RyanCavanaugh** added label `wontfix`
 * [today](https://github.com/microsoft/TypeScript-go/issues/3552#issuecomment-4316483827) **jakebailey** said "Shouldn't we be eliding that unused import?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/3552#issuecomment-4316606320) **RyanCavanaugh** asked for thoughts on an input code snippet showing different module configurations

### [Issue microsoft/TypeScript-go#3553](https://github.com/microsoft/TypeScript-go/issues/3553) (Closed, `Domain: Emit`, **DanielRosenwasser**, **Copilot**)

**Baselines: JSX factory call changed from indirect \(0, \_a\.jsx\)\(\.\.\.\) to direct \_jsx\(\.\.\.\) call**

*JSX emit now uses direct _jsx(...) function calls instead of comma-expression indirection for factory invocations.*

 * created by **RyanCavanaugh**
 * **ahejlsberg** added label `Domain: Emit`
 * (today) **DanielRosenwasser** assigned to **Copilot**, **DanielRosenwasser**, **Copilot**, and unassigned **Copilot**
 * (today) **DanielRosenwasser** closed the issue

### [Issue microsoft/TypeScript-go#3554](https://github.com/microsoft/TypeScript-go/issues/3554) (Closed, `wontfix`, **ahejlsberg**)

**Baselines: null\-initialized variable inferred as any instead of null type**

*Variables initialized with null are incorrectly inferred as any instead of null type.*

 * [today](https://github.com/microsoft/TypeScript-go/issues/3554#issuecomment-4314143927) **ahejlsberg** identified an issue in Strada where the auto-typed variable `l11` was mis-serialized as non-auto-typed because of its null initializer
 * (today) **ahejlsberg** added label `wontfix`, and removed label `Domain: Type Checking`
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#3555](https://github.com/microsoft/TypeScript-go/issues/3555) (Open, `Domain: Declaration Emit`)

**Baselines: @overload handling changes in JS declaration emit**

*JS declaration emit for JSDoc @overload alters overload output by removing or duplicating comments, losing type parameters, and collapsing signatures.*

 * created by **RyanCavanaugh**
 * **ahejlsberg** added label `Domain: Declaration Emit`

### [Issue microsoft/TypeScript-go#3556](https://github.com/microsoft/TypeScript-go/issues/3556) (Open, `Domain: Declaration Emit`)

**Baselines: @callback/@overload tags reordered and restructured in declaration emit**

*Declaration emit reorders callback and overload tags, simplifies type definitions, and mistakenly changes rest parameters from string[] to string.*

 * created by **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3556#issuecomment-4316034492) **ahejlsberg** said "I dont think conformance/callbackTagNestedParameter.js.diff is related to this issue."
 * **ahejlsberg** added label `Domain: Declaration Emit`

### [Issue microsoft/TypeScript-go#3557](https://github.com/microsoft/TypeScript-go/issues/3557) (Open, `Domain: Parser`)

**Baselines: @satisfies tag handling changes: functions become const declarations**

*Functions annotated with @satisfies now become declare const arrow functions with changed parameter types and added @param/@satisfies annotations*

 * created by **RyanCavanaugh**
 * **ahejlsberg** added label `Domain: Parser`

### [Issue microsoft/TypeScript-go#3558](https://github.com/microsoft/TypeScript-go/issues/3558) (Open, `Domain: Declaration Emit`, **DanielRosenwasser**, **Copilot**)

**Baselines: Labeled statement followed by export declaration loses original text**

*Labeled statements followed by export declarations lose their original semicolon in emitted baselines*

 * created by **RyanCavanaugh**
 * **ahejlsberg** added label `Domain: Declaration Emit`
 * (today) **DanielRosenwasser** assigned to **Copilot**, **DanielRosenwasser**

### [Issue microsoft/TypeScript-go#3559](https://github.com/microsoft/TypeScript-go/issues/3559) (Open, `Domain: Declaration Emit`)

**Baselines: CJS exports pattern changes in declaration emit**

*CommonJS declaration emit restructuring changed baselines, causing some files to lose exports entirely.*

 * created by **RyanCavanaugh**
 * **ahejlsberg** added label `Domain: Declaration Emit`

### [Issue microsoft/TypeScript-go#3560](https://github.com/microsoft/TypeScript-go/issues/3560) (Open, `Domain: Declaration Emit`)

**Baselines: exportNonInitializedVariables crash in declaration emit**

*Declaration emit crashes when exporting non-initialized variables in commonjs module baselines tests.*

 * created by **RyanCavanaugh**
 * **ahejlsberg** added label `Domain: Declaration Emit`

### [Issue microsoft/TypeScript-go#3561](https://github.com/microsoft/TypeScript-go/issues/3561) (Open, `wontfix`, `Domain: Declaration Emit`)

**Baselines: noImplicitThis functions returning this now fully expand the object type**

*Functions returning this under noImplicitThis now emit fully expanded object types instead of any, changing type contracts.*

 * created by **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3561#issuecomment-4316006820) **ahejlsberg** said "The new emit doesn't seem unreasonable."
 * **ahejlsberg** added label `Domain: Declaration Emit`
 * [today](https://github.com/microsoft/TypeScript-go/issues/3561#issuecomment-4316537499) **RyanCavanaugh** demonstrated Strada bailing at one level and Corsa at two, and showed the resulting type declaration diff
 * **RyanCavanaugh** added label `wontfix`

### [Issue microsoft/TypeScript-go#3562](https://github.com/microsoft/TypeScript-go/issues/3562) (Open, `Domain: Type Checking`)

**Baselines: JSDoc module namepath module:A emits as unresolved module instead of any**

*JSDoc module namepath syntax (module:A) now emits an unresolved module rather than any, producing type errors.*

 * created by **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3562#issuecomment-4315989334) **ahejlsberg** said "Seems like we should more gracefully handle JSDoc namepaths (even if we don't support them)."
 * **ahejlsberg** added label `Domain: Type Checking`

### [Issue microsoft/TypeScript-go#3563](https://github.com/microsoft/TypeScript-go/issues/3563) (Open, **ahejlsberg**)

**Baselines: definiteAssignment shorthand in object literal loses optional modifier**

*Optional method properties in object literal shorthand lose their optional modifier when emitted with definite assignment assertions.*

 * created by **RyanCavanaugh**
 * **ahejlsberg** assigned to **ahejlsberg**

### [Issue microsoft/TypeScript-go#3564](https://github.com/microsoft/TypeScript-go/issues/3564) (Open, `Domain: Type Checking`)

**Baselines: Generic function parameter inference change**

*Baseline tests updated to reflect generic function parameter inference changing x3’s type from any[] to any[][].*

 * created by **RyanCavanaugh**
 * **ahejlsberg** added label `Domain: Type Checking`

### [Issue microsoft/TypeScript-go#3565](https://github.com/microsoft/TypeScript-go/issues/3565) (Open, `Domain: Declaration Emit`)

**Baselines: Declaration emit trailing comma changes in destructuring parameters**

*Declaration emit baselines remove extra trailing commas after omitted elements in destructuring parameters.*

 * created by **RyanCavanaugh**
 * **ahejlsberg** added label `Domain: Declaration Emit`

### [Issue microsoft/TypeScript-go#3566](https://github.com/microsoft/TypeScript-go/issues/3566) (Open, `Domain: Declaration Emit`)

**Baselines: Late\-bound computed property \[prop\] preserved instead of resolved to plain prop**

*Late-bound computed property [prop] syntax is preserved instead of being resolved to plain prop*

 * created by **RyanCavanaugh**
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3566#issuecomment-4309176683) **RyanCavanaugh** said "This seems like a won't fix, actually. Both emits are equivalent."
 * **ahejlsberg** added label `Domain: Declaration Emit`

### [Issue microsoft/TypeScript-go#3567](https://github.com/microsoft/TypeScript-go/issues/3567) (Open, `Domain: Declaration Emit`)

**Baselines: Symbol getter/setter declaration emit change**

*Declaration outputs now change the return type of symbol getters/setters to undefined and introduce a new Symbol.toPrimitive overload.*

 * created by **RyanCavanaugh**
 * **ahejlsberg** added label `Domain: Declaration Emit`

### [Issue microsoft/TypeScript-go#3568](https://github.com/microsoft/TypeScript-go/issues/3568) (Open, `Domain: Declaration Emit`)

**Baselines: export as namespace added or restructured in declaration emit**

*Add or restructure ‘export as namespace GLO’ in declaration emit baselines to update module global visibility and public API contract.*

 * created by **RyanCavanaugh**
 * **ahejlsberg** added label `Domain: Declaration Emit`

### [Issue microsoft/TypeScript-go#3569](https://github.com/microsoft/TypeScript-go/issues/3569) (Open, `Domain: Declaration Emit`)

**Baselines: Declaration emit simplification of class extending built\-in Array**

*Declaration emit now simplifies classes extending built-in Array by dropping the generic parameter and removing inherited constructor overloads.*

 * created by **RyanCavanaugh**
 * **ahejlsberg** added label `Domain: Declaration Emit`

### [Issue microsoft/TypeScript-go#3570](https://github.com/microsoft/TypeScript-go/issues/3570) (Open, `Domain: Declaration Emit`)

**Baselines: Declaration emit type parameter renaming bug \(regression\)**

*Declaration emit incorrectly renames type parameters to T_1, leading to undefined types and TS2304 errors*

 * created by **RyanCavanaugh**
 * **ahejlsberg** added label `Domain: Declaration Emit`

### [Issue microsoft/TypeScript-go#3571](https://github.com/microsoft/TypeScript-go/issues/3571) (Closed, **ahejlsberg**)

**Module augmentation not merged when upstream \.d\.ts uses top\-level \`export interface\` \+ self\-referential \`declare module \.\.\. export =\`**

*tsgo doesn't merge module augmentations for packages whose .d.ts combine a top-level export interface with export= declarations*

 * created by **winrid**
 * **ahejlsberg** assigned to **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3571#issuecomment-4315205590) **ahejlsberg** reported inability to reproduce the issue, noted both tsc and tsgo compiled the minimal repro without errors, observed that skipLibCheck produced TS2666 errors indicating an unsupported feature, and mentioned not finding a self-referential module augmentation in @aws-lite/client
 * [today](https://github.com/microsoft/TypeScript-go/issues/3571#issuecomment-4315225875) **winrid** said "@ahejlsberg will work on a reproducer repo today"
 * [today](https://github.com/microsoft/TypeScript-go/issues/3571#issuecomment-4315355813) **winrid** described a tsgo bug where file discovery order caused interface augmentation to be dropped despite skipLibCheck and shared a full reproducer
 * [today](https://github.com/microsoft/TypeScript-go/issues/3571#issuecomment-4315700194) **ahejlsberg** noted that upgrading @aws-lite/client from 0.23.2 to 0.23.6 fixed the compile errors and asked if any scenarios remain broken without errors
 * [today](https://github.com/microsoft/TypeScript-go/issues/3571#issuecomment-4315845698) **winrid** said "@ahejlsberg thanks for the fast turnaround on this, looks like you're right, closing."
 * (today) **winrid** closed the issue

### [Issue microsoft/TypeScript-go#3576](https://github.com/microsoft/TypeScript-go/issues/3576) (Closed)

**\[Proposal\] strictArrayVariance: opt\-in invariance for mutable Array\<T\> element type \(post\-7\.0 discussion\)**

*Introduce a strictArrayVariance compiler option to enforce invariant element types on mutable arrays, preventing unsound covariance.*

 * created by **JustFly1984**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3576#issuecomment-4313817349) **jakebailey** said "This is most certainly the wrong repo to file this in. We are not adding new features in 7.0. Those need to wait for 7.1, and will not be taken in this repo."
 * (today) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/issues/3576#issuecomment-4314994623) **RyanCavanaugh** noted that invariant arrays brought a huge host of problems not addressed in the issue and referenced microsoft/TypeScript#18770

### [PR microsoft/TypeScript-go#3577](https://github.com/microsoft/TypeScript-go/pull/3577) (Closed)

**feat\(checker\): strictArrayVariance flag — invariant mutable Array\<T\> element type \(DRAFT for post\-7\.0 discussion\)**

*Add a draft compiler option strictArrayVariance to enforce invariant element types for mutable arrays and tuples.*

 * [today](https://github.com/microsoft/TypeScript-go/pull/3577#issuecomment-4312569206) **JustFly1984** said "@microsoft-github-policy-service agree [company="JustFly1984"]"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3577#issuecomment-4312578118) **JustFly1984** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3577#issuecomment-4312579805) **JustFly1984** said "@microsoft-github-policy-service agree company="JustFly1984""
 * **RyanCavanaugh** added to milestone `Post-7.0`
 * [today](https://github.com/microsoft/TypeScript-go/pull/3577#issuecomment-4315136809) **jakebailey** said "https://github.com/microsoft/typescript-go/issues/3576#issuecomment-4314994623"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3582](https://github.com/microsoft/TypeScript-go/pull/3582) (Closed)

**Move test to accepted bucket**

*Reclassify the test by moving it from its current location into the accepted bucket.*

 * created by **ahejlsberg**
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#3583](https://github.com/microsoft/TypeScript-go/issues/3583) (Closed, **jakebailey**, **Copilot**)

**Support disabling ATA via VS Code settings for inferred projects**

*Native Preview TypeScript language server ignores VS Code Automatic Type Acquisition disable settings for inferred projects, causing unwanted type installs.*

 * [today](https://github.com/microsoft/TypeScript-go/issues/3583#issuecomment-4314421930) **jakebailey** identified missing user preferences and suggested adding options with JSON snippets and provided precedence logic
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3584](https://github.com/microsoft/TypeScript-go/pull/3584) (Closed, **jakebailey**, **Copilot**)

**Support disabling ATA via VS Code settings for inferred projects**

*Add VS Code settings to disable automatic type acquisition in inferred projects with dynamic refresh handling and tests.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3584#issuecomment-4314778334) **jakebailey** said "@copilot+claude-opus-4.6 what happens if the user changes this setting? See other pref update code."
 * [today](https://github.com/microsoft/TypeScript-go/pull/3584#issuecomment-4314878530) **Copilot** added refreshATAIfNeeded in Configure to schedule diagnostics refresh when ATA disable preference changed
 * [today](https://github.com/microsoft/TypeScript-go/pull/3584#issuecomment-4315131801) **jakebailey** said "@copilot+claude-opus-4.6 address review comments. make sure you review your own code next time"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3584#issuecomment-4315215499) **Copilot** addressed review comments in commit 63d152e3, adjusted refreshATAIfNeeded to only trigger on disabled→enabled transitions, updated comments on AutomaticTypeAcquisitionEnabled and the TODO with actual config tag paths, and refactored ATA disabled tests to a table-driven format
 * [today](https://github.com/microsoft/TypeScript-go/pull/3584#issuecomment-4315425156) **jakebailey** requested investigation of a data race from CI and provided a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/pull/3584#issuecomment-4315469637) **jakebailey** said "This PR is actually fine, it's #3057 which has data races not caught in its own CI run."
 * (today) **jakebailey** closed the issue
 * (today) **jakebailey** reopened the issue
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3585](https://github.com/microsoft/TypeScript-go/issues/3585) (Open)

**Remove extraneous \`declare\` in \.d\.ts output to better match strada**

*Remove extraneous declare modifiers from .d.ts output for both TypeScript and JavaScript*

 * created by **RyanCavanaugh**

### [PR microsoft/TypeScript-go#3587](https://github.com/microsoft/TypeScript-go/pull/3587) (Closed)

**Revert "fix: invalidate symlinked packages in auto\-import cache"**

*Revert the symlinked package cache invalidation fix after discovering an undetected data race.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3588](https://github.com/microsoft/TypeScript-go/issues/3588) (Open, **jakebailey**, **Copilot**)

**Behaviour differences observed when varying tsconfig option key letter cases randomly**

*Lowercasing tsconfig compilerOptions keys causes unknown option and build-only errors in TypeScript 6.0*

 * created by **hkleungai**
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#3589](https://github.com/microsoft/TypeScript-go/pull/3589) (Open, **jakebailey**, **Copilot**)

**Make tsconfig option name lookup case\-sensitive with "Did you mean" suggestions**

*Enforce case-sensitive tsconfig.json option names and emit Did you mean suggestions for incorrectly cased entries.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue
 * (today) **jakebailey** reopened the issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/3589#issuecomment-4318121984) **hkleungai** said "Is it possible to make tsgo throw TS5025 instead of TS5023 in this case? 🤔 "
 * [today](https://github.com/microsoft/TypeScript-go/pull/3589#issuecomment-4318145199) **jakebailey** said "@copilot look into the above, as a "did you mean" is preferred "
 * [today](https://github.com/microsoft/TypeScript-go/pull/3589#issuecomment-4318172881) **Copilot** updated the implementation to emit TS5025 "Did you mean" diagnostics for case-insensitive matches and added support helpers

### [PR microsoft/TypeScript-go#3590](https://github.com/microsoft/TypeScript-go/pull/3590) (Closed)

**Fix auto\-import bucket state race and CreateProgram/UpdateProgram race**

*Added deep cloning of mutable pointer fields in RegistryBucket.Clone to fix auto-import bucket state and CreateProgram/UpdateProgram race conditions.*

 * created by **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#3591](https://github.com/microsoft/TypeScript-go/pull/3591) (Closed, **DanielRosenwasser**, **Copilot**)

**Accept direct JSX runtime factory call baseline**

*Update test baselines to accept direct JSX runtime factory calls (_jsx(...)) in CommonJS automatic runtime*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3591#issuecomment-4316632557) **DanielRosenwasser** said "This is hilariously bad."
 * (today) **DanielRosenwasser** closed the issue
 * (today) **DanielRosenwasser** reopened the issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/3591#issuecomment-4316816947) **DanielRosenwasser** clarified that the test illustrated undefined behavior and noted that #3594 aligned the output, but the output remained nonsensical due to references to non-existent identifiers
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#3592](https://github.com/microsoft/TypeScript-go/pull/3592) (Open, **DanielRosenwasser**, **Copilot**)

**Fix CommonJS emit of export declarations in nested statement contexts**

*CommonJS transformer now properly strips and transpiles export modifiers on nested variable statements in labeled and conditional blocks.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **DanielRosenwasser**

### [Issue microsoft/TypeScript-go#3593](https://github.com/microsoft/TypeScript-go/issues/3593) (Open)

**\[ServerErrors\]\[JavaScript\] main vs **

*Azure pipeline run on main branch encountered JavaScript server errors when analyzing 300 popular TypeScript repositories, resulting in various failures and timeouts.*

 * created by **typescript-bot**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3593#issuecomment-4316621438) **typescript-bot** reported a panic in handling textDocument/implementation due to invalid memory address or nil pointer dereference
 * [today](https://github.com/microsoft/TypeScript-go/issues/3593#issuecomment-4316621489) **typescript-bot** reported a panic due to invalid memory address or nil pointer dereference with an accompanying stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/3593#issuecomment-4316621528) **typescript-bot** reported a panic handling request textDocument/hover due to an unhandled TypeNode KindTypeParameter
 * [today](https://github.com/microsoft/TypeScript-go/issues/3593#issuecomment-4316621572) **typescript-bot** reported a premature server connection closure error and included affected repo details and repro steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/3593#issuecomment-4316621604) **typescript-bot** reported that the server connection closed prematurely with undefined for tastejs/todomvc and provided logs, replay commands, and reproduction steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/3593#issuecomment-4316621655) **typescript-bot** reported server connection closed prematurely with undefined error and provided affected repo details, logs, requests, and repro steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/3593#issuecomment-4316621698) **typescript-bot** reported a premature server connection closure error with undefined reason and provided details for mrdoob/three.js
 * [today](https://github.com/microsoft/TypeScript-go/issues/3593#issuecomment-4316621736) **typescript-bot** reported a panic handling textDocument/hover due to unhandled TypeNode KindTypeParameter

### [PR microsoft/TypeScript-go#3594](https://github.com/microsoft/TypeScript-go/pull/3594) (Closed, **DanielRosenwasser**, **Copilot**)

**\[WIP\] Fix baselines for JSX factory call change**

*Modify the CommonJS module transformer to apply JSX factory call substitutions in non-module files and update baselines accordingly.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#3595](https://github.com/microsoft/TypeScript-go/pull/3595) (Closed)

**Don't cancel refresh except on file change**

*Cancel diagnostics refresh only on client file-change notifications instead of open/close/save events to prevent stale diagnostics.*

 * created by **gabritto**

### [Issue microsoft/TypeScript-go#3596](https://github.com/microsoft/TypeScript-go/issues/3596) (Open)

**TS2883 regression in \-\-build with project references on inferred export from referenced package**

*tsgo --build now fails with TS2883 on inferred exports referencing types from a project-referenced package in a pnpm monorepo*

 * created by **kbrooks**

### [Issue microsoft/TypeScript-go#3597](https://github.com/microsoft/TypeScript-go/issues/3597) (Open, **jakebailey**, **Copilot**)

**Broken JSDoc codeblock parsing**

*JSDoc fenced code blocks with embedded tags like @Embed are misparsed by tsgo, producing incorrect HTML rendering.*

 * created by **LukeAbby**
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#3598](https://github.com/microsoft/TypeScript-go/pull/3598) (Open, **jakebailey**, **Copilot**)

**Fix JSDoc codeblock parsing: preserve fenced code block state across newlines**

*Update JSDoc parser to preserve fenced code block state across newlines and pass related tests*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3598#issuecomment-4316990736) **jakebailey** said "@copilot+claude-opus-4.6 This PR should have a hover test."
 * [today](https://github.com/microsoft/TypeScript-go/pull/3598#issuecomment-4317058374) **Copilot** added a fourslash hover test in quickInfoJSDocCodefenceAtSign_test.go to verify that @ symbols inside fenced code blocks render as literal text and that @param after the closing fence is parsed as a JSDoc tag

### [Issue microsoft/TypeScript-go#3599](https://github.com/microsoft/TypeScript-go/issues/3599) (Closed)

**\[ServerErrors\]\[TypeScript\] main vs **

*An Azure pipeline run on TypeScript main analyzed 300 GitHub repositories, finding 14 interesting changes, clone failures, and timeouts.*

 * created by **typescript-bot**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3599#issuecomment-4317050008) **typescript-bot** reported a debug failure panic during textDocument/formatting request
 * [today](https://github.com/microsoft/TypeScript-go/issues/3599#issuecomment-4317050045) **typescript-bot** displayed a panic with debug failure and stack trace during textDocument/formatting
 * [today](https://github.com/microsoft/TypeScript-go/issues/3599#issuecomment-4317050073) **typescript-bot** reported a panic with an invalid memory address or nil pointer dereference during cross-project handling
 * [today](https://github.com/microsoft/TypeScript-go/issues/3599#issuecomment-4317050100) **typescript-bot** reported a panic while handling textDocument/rangeFormatting due to a debug assertion failure
 * [today](https://github.com/microsoft/TypeScript-go/issues/3599#issuecomment-4317050130) **typescript-bot** reported a panic handling textDocument/formatting due to a debug failure assertion
 * [today](https://github.com/microsoft/TypeScript-go/issues/3599#issuecomment-4317050158) **typescript-bot** reported that the server connection closed prematurely and supplied error details, affected repo information, last requests, and repro steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/3599#issuecomment-4317050200) **typescript-bot** reported a server connection closed prematurely error for t4t5/sweetalert and provided logs, artifact links, last requests, and repro steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/3599#issuecomment-4317050238) **typescript-bot** reported server connection closed prematurely error for element-plus and provided repro steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/3599#issuecomment-4317050284) **typescript-bot** reported a server connection closed prematurely error with details, affected repo, last requests, and repro steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/3599#issuecomment-4317050309) **typescript-bot** reported that the server connection closed prematurely with an undefined error and provided repro steps for babel/babel
 * [today](https://github.com/microsoft/TypeScript-go/issues/3599#issuecomment-4317050349) **typescript-bot** reported a premature server connection closure with associated logs, affected repo details, recent requests, and repro steps

### [Issue microsoft/TypeScript-go#3600](https://github.com/microsoft/TypeScript-go/issues/3600) (Closed, `bug`, `Domain: Type Checking`, **ahejlsberg**)

**Behaviour differences observed when plain js class getter return null in conditional branch**

*TypeScript and tsgo differ in inferring nullability of JavaScript class getters, causing inconsistent errors on property access.*

 * created by **hkleungai**
 * **ahejlsberg** assigned to **ahejlsberg**
 * [later](https://github.com/microsoft/TypeScript-go/issues/3600#issuecomment-4319705569) **ahejlsberg** said "Looks like tsgo isn't picking up the JSDoc annotation on k1."
 * (later) **ahejlsberg** added labels `bug`, `Domain: Type Checking`

### [Issue microsoft/TypeScript-go#3601](https://github.com/microsoft/TypeScript-go/issues/3601) (Closed)

**Restart Server: "Stopping timed out" on first click when server is hung**

*TypeScript Native Preview's Restart Server command times out on first attempt when server hangs and only succeeds on retry.*

 * created by **ekazakov14**

### [PR microsoft/TypeScript-go#3602](https://github.com/microsoft/TypeScript-go/pull/3602) (Closed)

**Recover from shutdown timeout in tryRestart**

*Wrap restart in try/catch to fall back to a forced TypeScript language server start when graceful shutdown times out.*

 * created by **ekazakov14**

### [PR microsoft/TypeScript-go#3603](https://github.com/microsoft/TypeScript-go/pull/3603) (Closed)

**Fix go to implementation crash on invalid CJS shorthand exports**

*Prevent go to implementation crashes on invalid CommonJS shorthand exports.*

 * created by **Andarist**

### [PR microsoft/TypeScript-go#3604](https://github.com/microsoft/TypeScript-go/pull/3604) (Closed)

**Fix rename panic on unresolved reexports**

*Add handling to prevent rename operation panics caused by unresolved reexports*

 * created by **Andarist**

### [Issue microsoft/TypeScript-go#3605](https://github.com/microsoft/TypeScript-go/issues/3605) (Closed, `Domain: Editor`)

**Missing generic param displayed in hover**

*Hovering over a method in a defaulted generic class fails to display its generic parameter in tsgo while TypeScript 6.0 shows it.*

 * created by **Withered-Flower-0422**
 * **Withered-Flower-0422** added label `Domain: Editor`

### [Issue microsoft/TypeScript-go#516](https://github.com/microsoft/TypeScript-go/issues/516) (Open, `Domain: API and Extensibility`)

**Transformer Plugin or Compiler API**

*Requesting TypeScript team feedback on reintroducing a transformer plugin API versus continuing with the compiler API amid JS-Go integration challenges.*

 * [44 weeks ago](https://github.com/microsoft/TypeScript-go/issues/516#issuecomment-2981283047) **lppedd** mentioned that Nx has been shifting away from path aliases but still supports them for legacy reasons, noted pending Angular support and transformer issues, and requested maintaining compatibility with the previous implementation to avoid further workspace restructuring
 * [31 weeks ago](https://github.com/microsoft/TypeScript-go/issues/516#issuecomment-3292165922) **goloveychuk** proposed providing a typescript-builder npm package that would download the Go compiler and build TypeScript and plugins with remote caching
 * **RyanCavanaugh** added to milestone `Post-7.0`
 * [later](https://github.com/microsoft/TypeScript-go/issues/516#issuecomment-4318635327) **samchon** explained that they built `ttsc` to support `typia` with transformer plugins by wrapping `@typescript/native-preview`, providing a tsconfig-driven plugin host and a custom tsx-style runner using go:linkname shims

