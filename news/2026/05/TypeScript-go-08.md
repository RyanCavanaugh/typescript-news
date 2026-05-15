# Report for 2026-05-08 (Friday, May 8th, 2026)

16 different users commented on 63 different issues.

## Recommended Actions

 * Response Recommended
    * @kuishou68 offered to add a side-by-side Go/reference test to verify the fix in [microsoft/TypeScript-go#3618](https://github.com/microsoft/TypeScript-go/pull/3618#issuecomment-4411656223)
    * @Apollon77 provided repro steps as requested in [microsoft/TypeScript-go#3747](https://github.com/microsoft/TypeScript-go/issues/3747#issuecomment-4412313550)
    * @usernein reported the same issue happening with tsconfig.json in [microsoft/TypeScript-go#3768](https://github.com/microsoft/TypeScript-go/issues/3768#issuecomment-4411321552)
    * @dougludlow clarified that the issue occurs with pnpm’s enableGlobalVirtualStore in TypeScript v6/v7 but not v5.9.3 in [microsoft/TypeScript-go#3788](https://github.com/microsoft/TypeScript-go/issues/3788#issuecomment-4412927439)

## Activity Summary

### [Issue microsoft/TypeScript-go#1685](https://github.com/microsoft/TypeScript-go/issues/1685) (Open, `Domain: Type Checking`, `Domain: JS`, **sandersn**)

**\`ts\-check\` used with \`@typedef\` causes an error on \`module\.exports = \.\.\.\`**

*Combining @ts-check and @typedef in a CommonJS file causes a TS2309 export assignment error with tsgo.*

 * [1 month ago](https://github.com/microsoft/TypeScript-go/issues/1685#issuecomment-4218922623) **jbeaudoin-lf** said "Thanks, gonna give it a try tomorrow then !"
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1685#issuecomment-4236896401) **jbeaudoin-lf** asked which version was used and provided the version output and resulting error messages
 * [today](https://github.com/microsoft/TypeScript-go/issues/1685#issuecomment-4406356310) **jbeaudoin-lf** reported the same issue on Version 7.0.0-dev.20260508.1 and asked to reopen the issue
 * (today) **RyanCavanaugh** reopened the issue
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [Issue microsoft/TypeScript-go#2533](https://github.com/microsoft/TypeScript-go/issues/2533) (Open, `bug`, `Domain: Declaration Emit`, **weswigham**)

**Multiple differences in declaration emit for CommonJS exports**

*TypeScript’s declaration emitter for CommonJS exports uses typeof module.exports, emits duplicate var declarations, and emits var instead of const.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2533#issuecomment-4247896788) **ahejlsberg** noted support for multiple assignments to module.exports and exports.XXX and recommended emitting only the first occurrence to prevent duplicate declarations
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2533#issuecomment-4247979575) **ahejlsberg** described other JS declaration emit issues, noting missing x and y properties in class C and duplicate namespace declarations for obj and f
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2533#issuecomment-4263797893) **weswigham** explained that the last two items were intentional to align with the reparsing strategy, outlined how to align with the old emit by duplicating binder work, and identified the first issue as a bug likely caused by overzealous node reuse
 * [today](https://github.com/microsoft/TypeScript-go/issues/2533#issuecomment-4409207996) **weswigham** discussed the pros and cons of emitting duplicate declarations for multiple module export assignments and questioned whether to merge or error on them, concluding that emitting duplicates mirrors TS var redeclarations
 * [today](https://github.com/microsoft/TypeScript-go/issues/2533#issuecomment-4409859940) **RyanCavanaugh** said "@weswigham is what I'm hearing "wontfix"? I tend to agree if so. @ahejlsberg good w/ you too?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2533#issuecomment-4409931266) **weswigham** suggested to retag and track separate issues individually

### [Issue microsoft/TypeScript-go#2953](https://github.com/microsoft/TypeScript-go/issues/2953) (Closed, `Crash`, **ahejlsberg**, **Copilot**)

**Inlay hints triggers crash during checker initialization**

*Inlay hints cause the TypeScript checker to crash during initialization in the editor.*

 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * (yesterday) **DanielRosenwasser** assigned to **ahejlsberg**, and unassigned **DanielRosenwasser**
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#3477](https://github.com/microsoft/TypeScript-go/issues/3477) (Closed, `Needs Investigation`, **weswigham**)

**Remaining diffs in isolatedDeclarations**

*Remaining differences in isolatedDeclarations have been identified in submoduleTriaged.txt and await an upcoming PR.*

 * (3 days ago) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.0 RC`, and unassigned **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3477#issuecomment-4409250862) **weswigham** said "@RyanCavanaugh what group is the linked group this issue is meant to correlate with?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/3477#issuecomment-4409890589) **RyanCavanaugh** said "Disregard, I ended up making new issues in the other format."
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#3479](https://github.com/microsoft/TypeScript-go/issues/3479) (Closed, `Needs Investigation`, **andrewbranch**)

**Untriaged differences in self\-package resolution \(possibly test harness only\)**

*Untriaged differences in TypeScript self-package resolution tests for NodeNext import mode and outDir scenarios possibly originate from the test harness.*

 * (3 days ago) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.0 RC`, and assigned to **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#3545](https://github.com/microsoft/TypeScript-go/issues/3545) (Closed, `Domain: Declaration Emit`, `Needs Investigation`, **weswigham**, **RyanCavanaugh**, **Copilot**)

**Baselines: CJS export alias and element access patterns changed**

*Declaration output now differs for CommonJS export aliases and module.exports element access patterns, including duplicate assignments.*

 * (3 days ago) **RyanCavanaugh** set milestone to `TypeScript 7.0 RC`, and assigned to **weswigham**
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3545#issuecomment-4400155946) **weswigham** suggested relaxing checking to allow non-identifier export/import aliases in declaration files across all target levels and asked for @RyanCavanaugh's thoughts
 * [today](https://github.com/microsoft/TypeScript-go/issues/3545#issuecomment-4408235998) **RyanCavanaugh** said "@copilot make a PR to accept these baselines (add to submoduleAccepted.txt with a brief summary of the above comment)"
 * (today) **RyanCavanaugh** assigned to **Copilot**, **RyanCavanaugh**

### [Issue microsoft/TypeScript-go#3547](https://github.com/microsoft/TypeScript-go/issues/3547) (Closed, `Domain: Declaration Emit`, `Needs Investigation`, **weswigham**)

**Baselines: Namespace\-to\-const restructuring with DtsFileErrors \(redeclaration errors\)**

*Namespace-to-const transformation in baselines erroneously produces invalid .d.ts files with TS2451 redeclaration errors.*

 * (3 days ago) **RyanCavanaugh** set milestone to `TypeScript 7.0 RC`, and assigned to **weswigham**
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3547#issuecomment-4400324552) **weswigham** suggested skipping namespace merge members when host declarations for expandos had type annotations or full signatures, contrasted strada’s and corsa’s approaches, and noted that issue #3741 included a small fix
 * (today) **weswigham** closed the issue

### [Issue microsoft/TypeScript-go#3549](https://github.com/microsoft/TypeScript-go/issues/3549) (Closed, `Domain: Declaration Emit`, `Needs Investigation`, **weswigham**)

**Baselines: Missing generic type arguments no longer auto\-filled with any \(produces TS2314 errors\)**

*Generic types without explicit parameters now emit bare types instead of defaulting to any, causing TS2314 errors*

 * (3 days ago) **RyanCavanaugh** set milestone to `TypeScript 7.0 RC`, and assigned to **weswigham**
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3549#issuecomment-4400657746) **weswigham** noted the restoration of fewer-than-required type argument allowances for Array, Promise, and Object, referenced related TODOs, and opened #3745 with a fix
 * (today) **weswigham** closed the issue

### [Issue microsoft/TypeScript-go#3556](https://github.com/microsoft/TypeScript-go/issues/3556) (Closed, `Domain: Declaration Emit`, `Needs Investigation`, **sandersn**, **weswigham**)

**Baselines: @callback/@overload tags reordered and restructured in declaration emit**

*Declaration emit reorders callback and overload tags, simplifies type definitions, and mistakenly changes rest parameters from string[] to string.*

 * (3 days ago) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.0 RC`, and assigned to **weswigham**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3556#issuecomment-4408820643) **weswigham** explained a change in the jsdoc reparser that altered how `...T` is interpreted and asked if the new behavior was intentional or a bug
 * [today](https://github.com/microsoft/TypeScript-go/issues/3556#issuecomment-4408832253) **weswigham** said "@sandersn and @ahejlsberg - where did you land on how to interpret ...T jsdoc types? Like strada jsdoc, or like a TS variadic param?"
 * **RyanCavanaugh** assigned to **sandersn**

### [Issue microsoft/TypeScript-go#3559](https://github.com/microsoft/TypeScript-go/issues/3559) (Closed, `Domain: Declaration Emit`, `Needs Investigation`, **weswigham**, **RyanCavanaugh**, **Copilot**)

**Baselines: CJS exports pattern changes in declaration emit**

*CommonJS declaration emit restructuring changed baselines, causing some files to lose exports entirely.*

 * (3 days ago) **RyanCavanaugh** set milestone to `TypeScript 7.0 RC`, and assigned to **weswigham**
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3559#issuecomment-4401208763) **weswigham** said "AFAIK we intentionally no longer bind nested js exports, which is why we also don't traverse them for declarations, unless we've backpedaled on that?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/3559#issuecomment-4408871073) **weswigham** explained that this was an intentional change and that a new declaration emit error for nested CommonJS export constructs exists, noting that the first example test didn't show it due to ts-nocheck
 * (today) **RyanCavanaugh** assigned to **Copilot**, **RyanCavanaugh**

### [Issue microsoft/TypeScript-go#3562](https://github.com/microsoft/TypeScript-go/issues/3562) (Closed, `Domain: Type Checking`, `Needs Investigation`, **sandersn**, **jakebailey**, **Copilot**)

**Baselines: JSDoc module namepath module:A emits as unresolved module instead of any**

*JSDoc module namepath syntax (module:A) now emits an unresolved module rather than any, producing type errors.*

 * (yesterday) **jakebailey** reopened the issue
 * (yesterday) **jakebailey** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3566](https://github.com/microsoft/TypeScript-go/issues/3566) (Closed, `Domain: Declaration Emit`, `Needs Investigation`, **weswigham**, **RyanCavanaugh**, **Copilot**)

**Baselines: Late\-bound computed property \[prop\] preserved instead of resolved to plain prop**

*Late-bound computed property [prop] syntax is preserved instead of being resolved to plain prop*

 * (3 days ago) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.0 RC`, and assigned to **weswigham**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3566#issuecomment-4408960638) **weswigham** said "I agree, both are equivalent and now we use the []s because we're actually traversing the input nodes (which use brackets) instead of generating the type whole-cloth from symbol information."
 * (today) **RyanCavanaugh** assigned to **Copilot**, **RyanCavanaugh**

### [Issue microsoft/TypeScript-go#3567](https://github.com/microsoft/TypeScript-go/issues/3567) (Closed, `Domain: Declaration Emit`, `Needs Investigation`, **weswigham**, **RyanCavanaugh**, **Copilot**)

**Baselines: Symbol getter/setter declaration emit change**

*Declaration outputs now change the return type of symbol getters/setters to undefined and introduce a new Symbol.toPrimitive overload.*

 * (3 days ago) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.0 RC`, and assigned to **weswigham**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3567#issuecomment-4409041197) **weswigham** described that the new output was preferable but retained duplicate declarations per the garbage-in-garbage-out principle and identified a Strada bug conflating getters and methods and eliding the method due to overload detection
 * (today) **RyanCavanaugh** assigned to **Copilot**, **RyanCavanaugh**

### [Issue microsoft/TypeScript-go#3568](https://github.com/microsoft/TypeScript-go/issues/3568) (Closed, `wontfix`, `Domain: Declaration Emit`, **weswigham**, **jakebailey**, **Copilot**)

**Baselines: export as namespace added or restructured in declaration emit**

*Add or restructure ‘export as namespace GLO’ in declaration emit baselines to update module global visibility and public API contract.*

 * (yesterday) **jakebailey** reopened the issue
 * (yesterday) **jakebailey** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3569](https://github.com/microsoft/TypeScript-go/issues/3569) (Closed, `Domain: Declaration Emit`, `Needs Investigation`, **weswigham**, **RyanCavanaugh**, **Copilot**)

**Baselines: Declaration emit simplification of class extending built\-in Array**

*Declaration emit now simplifies classes extending built-in Array by dropping the generic parameter and removing inherited constructor overloads.*

 * (3 days ago) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.0 RC`, and assigned to **weswigham**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3569#issuecomment-4408936938) **weswigham** explained that the outputs were functionally identical and the new output better matched the input source, noted improvements in static block this assignment declarations, and clarified why <any> was generated for extends positions
 * (today) **RyanCavanaugh** assigned to **Copilot**, **RyanCavanaugh**

### [Issue microsoft/TypeScript-go#3585](https://github.com/microsoft/TypeScript-go/issues/3585) (Closed, `wontfix`, **weswigham**, **RyanCavanaugh**, **Copilot**)

**Remove extraneous \`declare\` in \.d\.ts output to better match strada**

*Remove extraneous declare modifiers from .d.ts output for both TypeScript and JavaScript*

 * (2 days ago) **RyanCavanaugh** added label `bug`, set milestone to `TypeScript 7.0 RC`, and assigned to **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3585#issuecomment-4409108636) **weswigham** noted that the issue concerned removing all redundant `declare` modifiers from declaration file generation and expressed concern about introducing noisy diffs alongside bugfix changes
 * (today) **RyanCavanaugh** added label `wontfix`, and removed label `bug`

### [PR microsoft/TypeScript-go#3618](https://github.com/microsoft/TypeScript-go/pull/3618) (Open)

**fix: prevent wildcard pattern from overriding exact match in FindBestPatternMatch**

*Assign math.MaxInt for exact matches in FindBestPatternMatch to ensure wildcard patterns cannot override exact matches.*

 * created by **kuishou68**
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3618#issuecomment-4323606759) **jakebailey** said "This will require a test, preferably one we can cross check with the old code to double check it"
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3618#issuecomment-4331007584) **DanielRosenwasser** said "As far as I remember, this code path isn't supposed to be hit for an exact match. Did you actually run into a problem with a specific project?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3618#issuecomment-4411656223) **kuishou68** identified that the Go port compared StarIndex instead of prefixLength, causing wildcard matches to overwrite exact matches, and offered to add a side-by-side test to verify the fix

### [PR microsoft/TypeScript-go#3643](https://github.com/microsoft/TypeScript-go/pull/3643) (Closed, **andrewbranch**, **Copilot**)

**Fix isInitialized not restored after tryRestart**

*tryRestart doesn’t reset the isInitialized flag or trigger initialization events after restart, preventing new listeners from firing.*

 * created by **Copilot**
 * (1 week ago) **Copilot** assigned to **Copilot**, **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#3651](https://github.com/microsoft/TypeScript-go/issues/3651) (Closed, `Domain: Editor`, **andrewbranch**)

**"Native Preview: Disable" does not re\-activate built\-in extension**

*Disabling the native preview fails to restore the built-in TypeScript extension in VS Code.*

 * (1 week ago) **DanielRosenwasser** added label `Domain: Editor`, and assigned to **andrewbranch**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * [today](https://github.com/microsoft/TypeScript-go/issues/3651#issuecomment-4408432477) **andrewbranch** said "This was fixed by #3652 "
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#3662](https://github.com/microsoft/TypeScript-go/issues/3662) (Closed, `bug`, **iisaduan**)

**Behavior difference: tsgo wrongly allows \`include\` to contain files that is not under \`rootDir\` from tsconfig**

*tsgo incorrectly permits including files outside the configured rootDir in tsconfig without reporting errors.*

 * (3 days ago) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.0 RC`, and assigned to **iisaduan**
 * (today) **iisaduan** added label `bug`, and removed label `Needs Investigation`

### [Issue microsoft/TypeScript-go#3686](https://github.com/microsoft/TypeScript-go/issues/3686) (Closed, `bug`, `Domain: Declaration Emit`, **weswigham**)

**Unnecessary declaration in \.d\.ts**

*tsgo emits declarations for a non-exported function and its namespace in the .d.ts file that should be omitted.*

 * (3 days ago) **weswigham** added label `Domain: Declaration Emit`, and assigned to **weswigham**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * (today) **weswigham** closed the issue

### [Issue microsoft/TypeScript-go#3689](https://github.com/microsoft/TypeScript-go/issues/3689) (Open, `Needs Investigation`, **andrewbranch**)

**project reference resolution fails when workspace is opened through a symlinked root path**

*tsgo fails to resolve project references and reports TS2307 errors when the workspace root is opened via a symlink*

 * (2 days ago) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.0 RC`, and assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3689#issuecomment-4408371311) **andrewbranch** said "N.B. the error occurs both in Corsa and in Strada. The fix looks behaviorally correct but I need to check performance impact."
 * (today) **andrewbranch** set milestone to `Post-7.0`, and removed from milestone `TypeScript 7.0 RC`

### [PR microsoft/TypeScript-go#3711](https://github.com/microsoft/TypeScript-go/pull/3711) (Closed)

**Narrow String\#toLowerCase/toUpperCase return types via Lowercase/Uppercase**

*Narrow String.prototype.toLowerCase and toUpperCase return types to literal strings using Lowercase and Uppercase generics.*

 * created by **ljharb**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3711#issuecomment-4409899596) **RyanCavanaugh** said "TypeScript is the correct originating repo for lib changes; no need to PR here."
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#3716](https://github.com/microsoft/TypeScript-go/pull/3716) (Closed)

**Only include \_visible\_ expando functions in declaration emit output**

*Restrict declaration emit output to include only visible expando functions.*

 * created by **weswigham**
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript-go#3728](https://github.com/microsoft/TypeScript-go/pull/3728) (Open)

**Fix keyof deferred for non\-generic substitution types \(\#2186\)**

*Resolve keyof immediately for non-generic substitution types, fixing indexed access assignability and unsimplified quick info.*

 * created by **adavila0703**
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/3728#issuecomment-4390943530) **adavila0703** quoted the Contributor License Agreement and instructions for agreeing
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3728#issuecomment-4402998409) **jakebailey** said "If this fixes #2186, can you write "Fixes #2186" in the description?"
 * **RyanCavanaugh** added to milestone `Post-7.0`

### [Issue microsoft/TypeScript-go#3733](https://github.com/microsoft/TypeScript-go/issues/3733) (Open, `Domain: Editor`, `Needs More Info`)

**No autocomplete for local symbols and some global types when creating a new file**

*VS Code fails to autocomplete or auto-import local symbols and ESNext types like Temporal in new TypeScript files until restart.*

 * created by **jansedlon**
 * **jansedlon** added label `Domain: Editor`
 * [today](https://github.com/microsoft/TypeScript-go/issues/3733#issuecomment-4408882714) **RyanCavanaugh** said "We really need concrete file contents in order to investigate these kinds of things."
 * **RyanCavanaugh** added label `Needs More Info`

### [Issue microsoft/TypeScript-go#3734](https://github.com/microsoft/TypeScript-go/issues/3734) (Closed, `Crash`, `Needs More Info`)

**Entering "ai\.messages\.find\(m =\> m\.\)" will cause the language server to crash\.**

*Typing ai.messages.find(m => m.) triggers an internal token-end mismatch panic that crashes the language server*

 * **RyanCavanaugh** unassigned **Copilot**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3734#issuecomment-4405918795) **ShenHongFei** reported that they couldn't reproduce the issue in a new project, noted the crash occurred when entering "m." possibly due to monaco-editor import, and said they would provide a reproducible example
 * [today](https://github.com/microsoft/TypeScript-go/issues/3734#issuecomment-4406047516) **ShenHongFei** attempted to reproduce the issue in a new project with monaco-editor 0.55.1 but couldn’t, gave up and decided to avoid using “m.”
 * [today](https://github.com/microsoft/TypeScript-go/issues/3734#issuecomment-4408357849) **RyanCavanaugh** said "OK, please log a new issue if it comes up again and there's a repro. Thanks!"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#3739](https://github.com/microsoft/TypeScript-go/issues/3739) (Closed, `bug`, `Domain: Type Checking`, **ahejlsberg**)

**Behavior difference: Variable with type \`{}\` can be "wrongly" assigned to Record in tsgo but not in tsc**

*tsgo does not report errors when assigning {} to typed Record<string, ...> types in JavaScript, whereas tsc correctly flags the type mismatch.*

 * created by **hkleungai**
 * **ahejlsberg** assigned to **ahejlsberg**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and set milestone to `TypeScript 7.0 RC`

### [PR microsoft/TypeScript-go#3741](https://github.com/microsoft/TypeScript-go/pull/3741) (Closed)

**Only transform expando assignments that wont be represented elsewhere in the emit already**

*Ensure expando property assignments are only transformed when not already emitted elsewhere*

 * created by **weswigham**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3741#issuecomment-4408757850) **jakebailey** said "This must be conflicting with main at this point"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3741#issuecomment-4408774431) **weswigham** noted that one of the new tests from a recent PR was further fixed by this one after conflicting with main
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript-go#3745](https://github.com/microsoft/TypeScript-go/pull/3745) (Closed)

**Add missing type argument count sanity check to handle nodes from js …**

*Add a missing sanity check to validate type argument counts for JavaScript-derived builtin aliases like Array and Promise*

 * created by **weswigham**
 * (today) **weswigham** closed the issue

### [Issue microsoft/TypeScript-go#3747](https://github.com/microsoft/TypeScript-go/issues/3747) (Closed)

**Regression in 20260506\.1: generic substitution lost through method\-returned mapped type**

*tsgo CLI in version 7.0.0-dev.20260506.1 incorrectly loses generic substitutions for method-returned mapped types, defaulting to constraint defaults.*

 * created by **Apollon77**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3747#issuecomment-4404886819) **Andarist** said "Please prepare a self-contained repro that somebody could investigate. This kind of an issue should be easily reproducible with code fitting a TS playground."
 * [later](https://github.com/microsoft/TypeScript-go/issues/3747#issuecomment-4412313550) **Apollon77** described efforts to reproduce the bug against matter.js source and provided steps showing that tsgo v7.0.0-dev.20260506.1 and later fail while earlier versions succeed

### [Issue microsoft/TypeScript-go#3748](https://github.com/microsoft/TypeScript-go/issues/3748) (Closed, `wontfix`)

**Behavior difference: type testing, order**

*Migrating to tsgo caused the order of union and object type members to differ from TypeScript's output.*

 * created by **terrablue**
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3748#issuecomment-4401108029) **jakebailey** said "This is not guaranteed, and you should see the same if you use 6.0 and pass --stableTypeOrdering."
 * **RyanCavanaugh** added label `wontfix`
 * [today](https://github.com/microsoft/TypeScript-go/issues/3748#issuecomment-4408366162) **RyanCavanaugh** said "https://stackoverflow.com/a/55128956/1704166"
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#3751](https://github.com/microsoft/TypeScript-go/pull/3751) (Closed, **gabritto**, **Copilot**)

**Implement checkExternalEmitHelpers for tslib helper validation**

*Implement checkExternalEmitHelpers and its supporting logic for tslib helper validation, exclude certain built-in helpers, and refresh baselines.*

 * created by **Copilot**
 * (yesterday) **Copilot** assigned to **Copilot**, **gabritto**
 * (today) **gabritto** closed the issue

### [Issue microsoft/TypeScript-go#3753](https://github.com/microsoft/TypeScript-go/issues/3753) (Open, `bug`, **iisaduan**)

**Missing error for non\-existent root files**

*tsgo silently ignores missing root files specified in tsconfig.json instead of reporting an error.*

 * created by **DanielRosenwasser**
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3753#issuecomment-4401709100) **DanielRosenwasser** said "Found from https://github.com/microsoft/typescript-go/issues/3376"
 * **RyanCavanaugh** added label `bug`

### [Issue microsoft/TypeScript-go#3758](https://github.com/microsoft/TypeScript-go/issues/3758) (Open, `bug`, **RyanCavanaugh**, **Copilot**)

**File argument of \`@\` crashes CLI**

*Providing `@` with no file path to tsgo crashes the CLI with a “path "" is not absolute” panic.*

 * created by **DanielRosenwasser**
 * (today) **RyanCavanaugh** added label `bug`, set milestone to `TypeScript 7.0 RC`, and assigned to **Copilot**, **RyanCavanaugh**

### [PR microsoft/TypeScript-go#3763](https://github.com/microsoft/TypeScript-go/pull/3763) (Closed, **jakebailey**, **Copilot**)

**Move jsDeclarationsExportFormsErr baseline from submoduleTriaged to submoduleAccepted**

*The jsDeclarationsExportFormsErr ES2015 diff has been moved from submoduleTriaged to submoduleAccepted to acknowledge correct ‘export as namespace’ preservation in declaration emits*

 * created by **Copilot**
 * (yesterday) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3764](https://github.com/microsoft/TypeScript-go/pull/3764) (Closed, **jakebailey**, **Copilot**)

**Move jsDeclarationsModuleReferenceHasEmit baseline from submoduleTriaged to submoduleAccepted**

*Moved the jsDeclarationsModuleReferenceHasEmit baseline and diff files from submoduleTriaged to submoduleAccepted to reflect correct unresolved JSDoc module reference behavior.*

 * created by **Copilot**
 * (yesterday) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3766](https://github.com/microsoft/TypeScript-go/issues/3766) (Closed, `Crash`, **DanielRosenwasser**)

**Completions failure when \`from\` occurs on next line in \`import\`**

*The TypeScript-Go language server crashes during completions when the 'from' keyword in an import statement is placed on a new line.*

 * (yesterday) **DanielRosenwasser** added label `Crash`, set milestone to `TypeScript 7.0 RC`, and assigned to **DanielRosenwasser**
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#3767](https://github.com/microsoft/TypeScript-go/pull/3767) (Closed)

**Fix crash on completing default import identifiers when \`from\` is on following line**

*Adds missing nil checks to import completion functions to prevent crashes when default import and from clause span separate lines.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** closed the issue

### [Issue microsoft/TypeScript-go#3768](https://github.com/microsoft/TypeScript-go/issues/3768) (Open, `Crash`, **andrewbranch**, **Copilot**)

**Panic in overlayfs\.go when switching back to a TS file after saving package\.json**

*Saving package.json then switching back to a TypeScript file triggers a panic in typescript-go’s overlayFS due to a missing overlay.*

 * created by **kouovo**
 * **kouovo** added label `Crash`
 * [today](https://github.com/microsoft/TypeScript-go/issues/3768#issuecomment-4411321552) **usernein** reported the same issue with tsconfig.json after modifying it

### [PR microsoft/TypeScript-go#3770](https://github.com/microsoft/TypeScript-go/pull/3770) (Closed)

**Defer global ambient module merging in \`initializeChecker\`**

*Defer merging of global ambient module declarations during initializeChecker to improve predictability and minimize impact.*

 * created by **ahejlsberg**
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#3771](https://github.com/microsoft/TypeScript-go/pull/3771) (Open, **RyanCavanaugh**, **Copilot**)

**Accept CJS export alias and element access pattern baseline diffs**

*Accept five baseline diffs reflecting Corsa’s correct export alias and element access handling over Strada’s mangled outputs.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**

### [PR microsoft/TypeScript-go#3772](https://github.com/microsoft/TypeScript-go/pull/3772) (Closed, **RyanCavanaugh**, **Copilot**)

**Fix panic on bare \`@\` CLI argument**

*tsgo now handles bare '@' CLI arguments without panicking by updating VFS ReadFile to fail non-absolute paths and adding tests.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3772#issuecomment-4408616683) **RyanCavanaugh** said "@copilot listen to Jake"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3772#issuecomment-4408789264) **RyanCavanaugh** said "@copilot listen to Jake"

### [PR microsoft/TypeScript-go#3773](https://github.com/microsoft/TypeScript-go/pull/3773) (Closed)

**Add PR template for Copilot**

*Add a PR template for Copilot that places the issue link at the top to avoid scrolling.*

 * created by **RyanCavanaugh**
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#3774](https://github.com/microsoft/TypeScript-go/issues/3774) (Closed, `wontfix`)

**Behavior difference: tsgo emit different error codes when it comes to assignability**

*tsgo and tsc produce different TypeScript error codes for identical assignability errors in JavaScript files.*

 * created by **hkleungai**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3774#issuecomment-4409007324) **RyanCavanaugh** said "This is intended - generally, skipping these produces cleaner output"

### [Issue microsoft/TypeScript-go#3775](https://github.com/microsoft/TypeScript-go/issues/3775) (Open, **andrewbranch**)

**Add \`rootDir\` to self\-name tests after moving tests out of submodule and into Go codebase**

*Add rootDir configuration to several self-name tests moved into the Go codebase from a submodule*

 * created by **andrewbranch**
 * (today) **andrewbranch** set milestone to `Post-7.0`, and assigned to **andrewbranch**

### [PR microsoft/TypeScript-go#3776](https://github.com/microsoft/TypeScript-go/pull/3776) (Closed)

**Fix package index fallback edge case, accept self\-name resolution errors under ambiguous project root**

*Fix package index fallback and permit self-name resolution errors when project root is ambiguous.*

 * created by **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#3777](https://github.com/microsoft/TypeScript-go/pull/3777) (Closed)

**Port checks for tslib helpers**

*tslib helper checks now always validate emit helpers and cache requestedExternalEmitHelpers per file for consistent diagnostics.*

 * created by **gabritto**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3777#issuecomment-4410186212) **jakebailey** said "This seems 1:1 but I think the copilot comments are worth addresssing"

### [PR microsoft/TypeScript-go#3778](https://github.com/microsoft/TypeScript-go/pull/3778) (Closed, **RyanCavanaugh**, **Copilot**)

**Accept symbolDeclarationEmit12\.js baseline change**

*Accept the updated symbolDeclarationEmit12.js baseline to preserve duplicate [Symbol.toPrimitive] overloads and correct getter versus method return types*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**

### [PR microsoft/TypeScript-go#3779](https://github.com/microsoft/TypeScript-go/pull/3779) (Closed, **RyanCavanaugh**, **Copilot**)

**Accept late\-bound computed property baseline diffs**

*Accept baseline diffs for late-bound computed property tests as won’t-fix given semantically equivalent bracket notation*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**

### [PR microsoft/TypeScript-go#3780](https://github.com/microsoft/TypeScript-go/pull/3780) (Closed, **RyanCavanaugh**, **Copilot**)

**Accept baseline: declaration emit simplification of class extending built\-in Array**

*Baseline update simplifies JavaScript Array subclass declarations by removing redundant generics and overloads and correctly emitting static assignments.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**

### [PR microsoft/TypeScript-go#3781](https://github.com/microsoft/TypeScript-go/pull/3781) (Closed, **RyanCavanaugh**, **Copilot**)

**Accept CJS exports pattern baseline diffs**

*Accepted and relocated CommonJS export pattern baseline diffs to reflect new nested export declaration errors.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**

### [Issue microsoft/TypeScript-go#3782](https://github.com/microsoft/TypeScript-go/issues/3782) (Closed)

**\[ServerErrors\]\[JavaScript\] main vs **

*A main-branch pipeline run analyzing 300 popular TypeScript repositories encountered 15 interesting changes, 28 timeouts, one clone failure, and 18 unknown failures out of 253 successful analyses.*

 * created by **typescript-bot**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3782#issuecomment-4410161866) **typescript-bot** reported a panic handling textDocument/signatureHelp due to an unhandled case in Node.Initializer
 * [today](https://github.com/microsoft/TypeScript-go/issues/3782#issuecomment-4410161916) **typescript-bot** reported a panic in handling textDocument/hover due to an unhandled case in Node.Initializer
 * [today](https://github.com/microsoft/TypeScript-go/issues/3782#issuecomment-4410161954) **typescript-bot** reported a panic in handling textDocument/definition due to an unhandled case in Node.Initializer
 * [today](https://github.com/microsoft/TypeScript-go/issues/3782#issuecomment-4410162011) **typescript-bot** reported a panic handling textDocument/diagnostic due to an unhandled case in Node.Initializer
 * [today](https://github.com/microsoft/TypeScript-go/issues/3782#issuecomment-4410162084) **typescript-bot** reported a panic handling textDocument/completion due to an unhandled case in Node.Initializer
 * [today](https://github.com/microsoft/TypeScript-go/issues/3782#issuecomment-4410162117) **typescript-bot** reported a panic during cross-project handling due to an unhandled case in Node.Text and included a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/3782#issuecomment-4410162168) **typescript-bot** reported a panic during textDocument/completion due to an unhandled Node.Initializer and included a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/3782#issuecomment-4410162218) **typescript-bot** reported a panic handling textDocument/formatting request with a false expression error and stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/3782#issuecomment-4410162267) **typescript-bot** reported that the server connection closed prematurely and provided affected repos, logs, recent requests, and repro steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/3782#issuecomment-4410162318) **typescript-bot** reported a server connection closed prematurely error and provided reproduction steps for gchq/CyberChef
 * [today](https://github.com/microsoft/TypeScript-go/issues/3782#issuecomment-4410162371) **typescript-bot** reported a premature server connection closure error and provided repro steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/3782#issuecomment-4410162410) **typescript-bot** reported a server connection closed prematurely error and provided related logs, affected repo, old server result, and last requests
 * [today](https://github.com/microsoft/TypeScript-go/issues/3782#issuecomment-4410162452) **typescript-bot** reported a panic handling textDocument/diagnostic due to an unhandled case in Node.Initializer

### [PR microsoft/TypeScript-go#3783](https://github.com/microsoft/TypeScript-go/pull/3783) (Closed)

**check that files specified in tsconfig\.json "include" is located in "rootdir"**

*Validate that files listed in tsconfig.json include patterns are located within the configured rootDir.*

 * created by **iisaduan**

### [Issue microsoft/TypeScript-go#3784](https://github.com/microsoft/TypeScript-go/issues/3784) (Closed)

**\[ServerErrors\]\[TypeScript\] main vs **

*The TypeScript main branch error-delta pipeline encountered server errors, timeouts, and failures while analyzing 300 repositories and detected 20 changes.*

 * created by **typescript-bot**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3784#issuecomment-4410588062) **typescript-bot** reported a panic in handling textDocument/signatureHelp due to a Debug failure: Not a subspan (Child: KindLessThanSlashToken, parent: KindJsxAttribute)
 * [today](https://github.com/microsoft/TypeScript-go/issues/3784#issuecomment-4410588086) **typescript-bot** reported a panic during textDocument/implementation request with an unhandled case in Node.Initializer and included a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/3784#issuecomment-4410588126) **typescript-bot** reported a panic handling textDocument/signatureHelp due to an unhandled Node.Initializer case and included a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/3784#issuecomment-4410588154) **typescript-bot** reported panic handling textDocument/signatureHelp due to unhandled Node.Initializer case
 * [today](https://github.com/microsoft/TypeScript-go/issues/3784#issuecomment-4410588189) **typescript-bot** reported a panic during textDocument/implementation due to an unhandled case in Node.Initializer
 * [today](https://github.com/microsoft/TypeScript-go/issues/3784#issuecomment-4410588217) **typescript-bot** reported a panic handling textDocument/signatureHelp due to an unhandled case in Node.Initializer and included a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/3784#issuecomment-4410588250) **typescript-bot** reported a panic when handling textDocument/completion due to an unhandled case in Node.Initializer
 * [today](https://github.com/microsoft/TypeScript-go/issues/3784#issuecomment-4410588277) **typescript-bot** reported a panic during textDocument/rangeFormatting with a debug failure 'Token end is child end' and provided a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/3784#issuecomment-4410588298) **typescript-bot** reported a panic in textDocument/formatting due to a debug failure: Token end is child end
 * [today](https://github.com/microsoft/TypeScript-go/issues/3784#issuecomment-4410588321) **typescript-bot** reported a panic during cross-project handling with an unhandled case in Node.Initializer and provided a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/3784#issuecomment-4410588348) **typescript-bot** reported a panic handling textDocument/signatureHelp request due to an unhandled Node.Initializer case
 * [today](https://github.com/microsoft/TypeScript-go/issues/3784#issuecomment-4410588383) **typescript-bot** reported a panic during cross-project handling of textDocument/implementation due to an unhandled Node.Initializer case
 * [today](https://github.com/microsoft/TypeScript-go/issues/3784#issuecomment-4410588441) **typescript-bot** reported a panic stack trace for textDocument/completion due to an unhandled case in Node.Initializer
 * [today](https://github.com/microsoft/TypeScript-go/issues/3784#issuecomment-4410588469) **typescript-bot** reported a premature server connection closure error with undefined cause for elastic/kibana and provided reproduction steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/3784#issuecomment-4410588501) **typescript-bot** reported a server connection closed prematurely error 'undefined' and included affected repo details, raw error artifacts, recent LSP requests, and reproduction steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/3784#issuecomment-4410588530) **typescript-bot** reported server connection closed prematurely error for babel/babel and provided logs and repro steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/3784#issuecomment-4410588561) **typescript-bot** reported a server connection closed prematurely: undefined for the socketio/socket.io repo and provided last requests and repro steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/3784#issuecomment-4410588597) **typescript-bot** reported server connection closed prematurely for the n8n-io/n8n CI run

### [PR microsoft/TypeScript-go#3785](https://github.com/microsoft/TypeScript-go/pull/3785) (Open, `dependencies`, `javascript`)

**Bump fast\-uri from 3\.1\.0 to 3\.1\.2**

*Update fast-uri dependency to v3.1.2 to incorporate security fixes and improve malformed fragment error handling*

 * created by **dependabot[bot]**
 * (today) **dependabot[bot]** added labels `dependencies`, `javascript`

### [PR microsoft/TypeScript-go#3786](https://github.com/microsoft/TypeScript-go/pull/3786) (Closed)

**Fix crashes related to call hierarchy container names for computed properties**

*Resolves crashes due to incorrect call hierarchy container naming for computed properties.*

 * created by **Andarist**

### [Issue microsoft/TypeScript-go#3787](https://github.com/microsoft/TypeScript-go/issues/3787) (Open, `Needs More Info`)

**tsgo and tsc diverge on incomplete composite\-ref declaration cache: TS2305 vs filterable TS6305**

*tsgo reports TS2305 errors instead of TS6305 missing-declaration errors when the composite declaration cache is incomplete.*

 * created by **XavierGeerinck**

### [Issue microsoft/TypeScript-go#3788](https://github.com/microsoft/TypeScript-go/issues/3788) (Closed)

**Behavior difference: callback contextual typing — \`tsc@5\.9\.3\` passes, \`tsc@6\.0\.3\` / \`tsgo\` fail**

*TypeScript 6.0.3 and tsgo misinfer callback parameter types under pnpm enableGlobalVirtualStore symlinks, causing TS7031 errors that 5.9.3 did not produce.*

 * created by **dougludlow**
 * [later](https://github.com/microsoft/TypeScript-go/issues/3788#issuecomment-4412914876) **Andarist** said "It would be great if you could pull all of the relevant 3rd party types into a single file - a good repro usually can be created in a single import-less TS playground."
 * [later](https://github.com/microsoft/TypeScript-go/issues/3788#issuecomment-4412927439) **dougludlow** expressed uncertainty and specified that the import issue occurred only with pnpm’s enableGlobalVirtualStore, working in TypeScript v5.9.3 but failing in v6/v7

