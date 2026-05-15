# Report for 2026-05-14 (Thursday, May 14th, 2026)

15 different users commented on 48 different issues.

## Recommended Actions

 * Moderation
    * @Okanlawon2259 posted unrelated content in [microsoft/TypeScript-go#3815](https://github.com/microsoft/TypeScript-go/issues/3815#issuecomment-4456030799)
 * Response Recommended
    * @blickly asked for clarification on the meaning of 'the current (array-assuming) emit.' in [microsoft/TypeScript-go#3705](https://github.com/microsoft/TypeScript-go/pull/3705#issuecomment-4455898533)

## Activity Summary

### [Issue microsoft/TypeScript-go#3094](https://github.com/microsoft/TypeScript-go/issues/3094) (Open, `bug`, **weswigham**)

**Declaration emit proceeds in the presence of TS7056**

*TypeScript emits declarations despite TS7056 errors caused by deeply nested conditional and tag-branded utility types.*

 * [8 weeks ago](https://github.com/microsoft/TypeScript-go/issues/3094#issuecomment-4068324272) **hkleungai** noted that the TS4053 error resembled a previously reported issue, argued that ts6 and ts7 should resolve the type reference without error, and referenced related issues #2504 and #3027
 * [6 weeks ago](https://github.com/microsoft/TypeScript-go/issues/3094#issuecomment-4158824453) **weswigham** provided a status update on declaration emit behaviour in corsa versus strada, mentioned a 4-line diff to align implementations, and noted ongoing debugging of -b unit test failures
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * [today](https://github.com/microsoft/TypeScript-go/issues/3094#issuecomment-4455307998) **weswigham** noted that the "inferred type of this node exceeds the maximum length the compiler will serialize" error indicates truncated output and isn’t a workaround for TS roundtrip validity

### [Issue microsoft/TypeScript-go#3508](https://github.com/microsoft/TypeScript-go/issues/3508) (Open, `Needs Investigation`)

**Corsa no longer emits the TS\-1 internal diagnostic about pre\-emit/post\-emit diagnostic count mismatches**

*Corsa no longer emits TS-1 diagnostics for mismatched pre-emit and post-emit diagnostic counts in certain test files.*

 * (1 week ago) **RyanCavanaugh** added label `Needs Investigation`, and set milestone to `TypeScript 7.0 RC`
 * **gabritto** assigned to **Copilot**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3508#issuecomment-4453074769) **gabritto** analyzed the challenges in reintegrating the consistency check and recommended postponing it until post-7.0
 * [today](https://github.com/microsoft/TypeScript-go/issues/3508#issuecomment-4453326555) **weswigham** clarified that emit wasn't supposed to depend on a full check and explained consistency errors arose when checker methods were invoked out of order, suggested skipping or exception approaches, and noted that while CLI usage was unaffected, fixing these would be important for the API
 * (today) **RyanCavanaugh** set milestone to `Possible Improvement`, removed from milestone `TypeScript 7.0 RC`, and unassigned **gabritto**, **Copilot**

### [Issue microsoft/TypeScript-go#3511](https://github.com/microsoft/TypeScript-go/issues/3511) (Closed, `Needs Investigation`, **weswigham**)

**Unicode escapes in identifier names now displayed as literal characters**

*Identifier names containing Unicode escape sequences are now shown as their literal characters in conformance test outputs.*

 * (1 week ago) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.0 RC`, and assigned to **weswigham**
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript-go#3531](https://github.com/microsoft/TypeScript-go/pull/3531) (Closed, **weswigham**)

**Preserve escaped identifier spelling in unresolved name diagnostics**

*Preserve original escaped identifier spelling in unresolved name diagnostics to improve error message clarity.*

 * created by **Andarist**
 * (1 week ago) **RyanCavanaugh** set milestone to `Possible Improvement`, and assigned to **weswigham**
 * (today) **weswigham** closed the issue

### [Issue microsoft/TypeScript-go#3555](https://github.com/microsoft/TypeScript-go/issues/3555) (Closed, `Domain: Declaration Emit`, `Needs Investigation`, **weswigham**)

**Baselines: @overload handling changes in JS declaration emit**

*JS declaration emit for JSDoc @overload alters overload output by removing or duplicating comments, losing type parameters, and collapsing signatures.*

 * (1 week ago) **RyanCavanaugh** set milestone to `TypeScript 7.0 RC`, and assigned to **weswigham**
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/3555#issuecomment-4400834104) **weswigham** noted that the diffs were due to missing `declare` modifiers, jsdoc comments, or reordered declarations and said no further action was needed
 * (today) **weswigham** closed the issue

### [Issue microsoft/TypeScript-go#3556](https://github.com/microsoft/TypeScript-go/issues/3556) (Closed, `Domain: Declaration Emit`, `Needs Investigation`, **sandersn**, **weswigham**)

**Baselines: @callback/@overload tags reordered and restructured in declaration emit**

*Declaration emit reorders callback and overload tags, simplifies type definitions, and mistakenly changes rest parameters from string[] to string.*

 * [6 days ago](https://github.com/microsoft/TypeScript-go/issues/3556#issuecomment-4408820643) **weswigham** explained a change in the jsdoc reparser that altered how `...T` is interpreted and asked if the new behavior was intentional or a bug
 * [6 days ago](https://github.com/microsoft/TypeScript-go/issues/3556#issuecomment-4408832253) **weswigham** said "@sandersn and @ahejlsberg - where did you land on how to interpret ...T jsdoc types? Like strada jsdoc, or like a TS variadic param?"
 * **RyanCavanaugh** assigned to **sandersn**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3556#issuecomment-4454651925) **sandersn** explained that the behavior was intentional per the referenced PR and justified it based on prevalent usage, expression limitations for certain tuple types, and similarity to TypeScript
 * [today](https://github.com/microsoft/TypeScript-go/issues/3556#issuecomment-4454724574) **sandersn** suggested stopping the conversion of `...` on parameters to array types and instead limiting the operator to only validate usage, noting the balance between backward compatibility and expressiveness
 * [today](https://github.com/microsoft/TypeScript-go/issues/3556#issuecomment-4454840757) **weswigham** said "Weird that where we landed isn't interpreting it like a TS construct or like strada did (or even like ...T outside a @callback), but ok. Opened #3851 to just accept the diff."
 * (today) **weswigham** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/issues/3556#issuecomment-4455184154) **sandersn** assessed corsa's current state as strada with some cuts and suggested changing the usual alias usage instead of the JSDoc signature

### [Issue microsoft/TypeScript-go#3564](https://github.com/microsoft/TypeScript-go/issues/3564) (Closed, `Domain: Type Checking`, `Needs Investigation`, **ahejlsberg**)

**Baselines: Generic function parameter inference change**

*Baseline tests updated to reflect generic function parameter inference changing x3’s type from any[] to any[][].*

 * (1 week ago) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.0 RC`, and assigned to **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3564#issuecomment-4454981793) **ahejlsberg** said "Fixed by #3769."
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#3621](https://github.com/microsoft/TypeScript-go/issues/3621) (Closed, `Crash`, `Needs More Info`)

**Panic Alert Notification when Cursor edits some file and opening that file causes panic\.**

*Opening or editing a file causes a panic in the semanticTokens request because a token improperly spans multiple lines.*

 * **RyanCavanaugh** added label `Needs More Info`
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/3621#issuecomment-4373908974) **RyanCavanaugh** suggested opening in VS Code with the TypeScript Native Preview to verify whether the issue persisted and asked for a minimal LSP trace to reproduce the crash
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3621#issuecomment-4440078505) **Swiftwork** said "I believe that Cursor uses OpenVSX which has an out of date native preview. So you probably need to manually update it to the latest version."
 * [today](https://github.com/microsoft/TypeScript-go/issues/3621#issuecomment-4454444252) **RyanCavanaugh** said "Closing due to lack of repro. If anyone's encountering this, please include a VS Code or LSP-based invocation sequence, and ensure you're on latest bits."
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#3668](https://github.com/microsoft/TypeScript-go/issues/3668) (Closed, `Domain: Editor`, **johnfav03**)

**Enable/Disable Native Preview commands don't work when user & workspace settings are both configured**

*Disabling native preview with conflicting user and workspace js/ts.experimental.useTsgo settings ignores workspace override, causing duplicate results and no enable command.*

 * (1 week ago) **DanielRosenwasser** added label `Domain: Editor`, set milestone to `TypeScript 7.0 RC`, and assigned to **johnfav03**
 * (today) **johnfav03** closed the issue

### [Issue microsoft/TypeScript-go#3701](https://github.com/microsoft/TypeScript-go/issues/3701) (Open, **jakebailey**, **Copilot**)

**When using \`module=commonjs\`, Array destructuring is transpiled with wrong \(non\-iterator\) behavior**

*Compiling with module=commonjs wrongly transpiles exported array destructuring into fixed index access instead of iterator logic.*

 * (1 week ago) **jakebailey** assigned to **Copilot**, **jakebailey**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * [today](https://github.com/microsoft/TypeScript-go/issues/3701#issuecomment-4455680011) **jakebailey** asked for an explanation of necessity and queried if it was due to dropping ES5 and downlevelIteration

### [PR microsoft/TypeScript-go#3705](https://github.com/microsoft/TypeScript-go/pull/3705) (Open, **jakebailey**, **Copilot**)

**Preserve native destructuring for CommonJS exports to keep iterator semantics**

*Preserve native destructuring semantics in CommonJS exports by reusing nodes, suppressing source maps, adding tests, and refining implementation.*

 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/3705#issuecomment-4425472560) **Copilot** explained that the binding pattern node is only placed once and clones are used for export assignments, mirroring existing patterns, and clarified reason for sharing visitedName
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/3705#issuecomment-4425533988) **jakebailey** said "@copilot+claude-opus-4.6 Address feedback. Also, any new .diff files this PR introduces should be put into submoduleAccepted, with a link back to https://github.com/microsoft/typescript-go/issues/3701"
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/3705#issuecomment-4425642750) **Copilot** addressed feedback by renaming the `name` parameter to `pattern`, correcting the alias exports comment, relocating new .diff files to submoduleAccepted, and updating submoduleAccepted.txt with a link to issue #3701
 * [today](https://github.com/microsoft/TypeScript-go/pull/3705#issuecomment-4455456271) **weswigham** described breaking export visibility timing when transforming destructured exports and provided a test case
 * [today](https://github.com/microsoft/TypeScript-go/pull/3705#issuecomment-4455898533) **blickly** questioned the need to follow both the iterator protocol and export ordering, noted that TypeScript 6 already had the same timing caveats with downlevelIteration, and asked for clarification on the meaning of 'the current (array-assuming) emit.'
 * [today](https://github.com/microsoft/TypeScript-go/pull/3705#issuecomment-4456069964) **jakebailey** suggested using destructuring and dummy zero-based assignments to declare exports similar to esbuild
 * [today](https://github.com/microsoft/TypeScript-go/pull/3705#issuecomment-4456094511) **jakebailey** noted that the complex code wasn’t needed and suggested using simple destructuring for exports since they are already declared

### [Issue microsoft/TypeScript-go#3722](https://github.com/microsoft/TypeScript-go/issues/3722) (Open, `Domain: Editor`, **jakebailey**, **Copilot**)

**custom tsgo path is now ignored**

*VS Code's TypeScript native-preview ignores the configured custom tsgo path and launches its bundled tsgo instead.*

 * **loynoir** added label `Domain: Editor`
 * (1 week ago) **jakebailey** assigned to **Copilot**, **jakebailey**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [Issue microsoft/TypeScript-go#3727](https://github.com/microsoft/TypeScript-go/issues/3727) (Open, `Domain: Editor`, `possible improvement`, **jakebailey**)

**Unify tsdk between built\-in and native preview extensions**

*Share the built-in tsdk setting with the native preview and choose the TypeScript server based on useTsGo and tsdk directory.*

 * (1 week ago) **RyanCavanaugh** added label `Domain: Editor`, and set milestone to `Possible Improvement`
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/3727#issuecomment-4399622023) **DanielRosenwasser** said "We may need some sort of marker file to tell us "this is a TS7 directory"."
 * (today) **DanielRosenwasser** set milestone to `TypeScript 7.0 RC`, and removed from milestone `Possible Improvement`
 * **RyanCavanaugh** assigned to **jakebailey**

### [Issue microsoft/TypeScript-go#3739](https://github.com/microsoft/TypeScript-go/issues/3739) (Closed, `bug`, `Domain: Type Checking`, **ahejlsberg**)

**Behavior difference: Variable with type \`{}\` can be "wrongly" assigned to Record in tsgo but not in tsc**

*tsgo does not report errors when assigning {} to typed Record<string, ...> types in JavaScript, whereas tsc correctly flags the type mismatch.*

 * (3 days ago) **ahejlsberg** added labels `bug`, `Domain: Type Checking`
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/3739#issuecomment-4424600997) **ahejlsberg** said "I will put up a PR that consistently implements implied index signatures for expando object literals."
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#3742](https://github.com/microsoft/TypeScript-go/issues/3742) (Open, `Needs Investigation`, **iisaduan**)

**Behavior difference: tsgo skip reporting invalid jsdoc type when param is missing from function signature**

*tsgo omits the generic type argument error for invalid JSDoc types when a @param name is missing from the function signature, unlike tsc.*

 * created by **hkleungai**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.0 RC`, and assigned to **iisaduan**

### [Issue microsoft/TypeScript-go#3747](https://github.com/microsoft/TypeScript-go/issues/3747) (Closed)

**Regression in 20260506\.1: generic substitution lost through method\-returned mapped type**

*tsgo CLI in version 7.0.0-dev.20260506.1 incorrectly loses generic substitutions for method-returned mapped types, defaulting to constraint defaults.*

 * created by **Apollon77**
 * [6 days ago](https://github.com/microsoft/TypeScript-go/issues/3747#issuecomment-4404886819) **Andarist** said "Please prepare a self-contained repro that somebody could investigate. This kind of an issue should be easily reproducible with code fitting a TS playground."
 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/3747#issuecomment-4412313550) **Apollon77** described efforts to reproduce the bug against matter.js source and provided steps showing that tsgo v7.0.0-dev.20260506.1 and later fail while earlier versions succeed
 * [today](https://github.com/microsoft/TypeScript-go/issues/3747#issuecomment-4455298605) **RyanCavanaugh** asked to disable skipLibCheck to confirm and explained a declaration emit bug with a minimal repro and conditions
 * [today](https://github.com/microsoft/TypeScript-go/issues/3747#issuecomment-4455324118) **RyanCavanaugh** verified that the issue was fixed in 7.0.0-dev.20260514.1 and requested confirmation from Apollon77
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#3768](https://github.com/microsoft/TypeScript-go/issues/3768) (Open, `Crash`, **andrewbranch**, **Copilot**)

**Panic in overlayfs\.go when switching back to a TS file after saving package\.json**

*Saving package.json then switching back to a TypeScript file triggers a panic in typescript-go’s overlayFS due to a missing overlay.*

 * created by **kouovo**
 * **kouovo** added label `Crash`
 * [6 days ago](https://github.com/microsoft/TypeScript-go/issues/3768#issuecomment-4411321552) **usernein** reported the same issue with tsconfig.json after modifying it
 * (today) **RyanCavanaugh** set milestone to `TypeScript 7.0 RC`, assigned to **Copilot**, **RyanCavanaugh**, **andrewbranch**, and unassigned **RyanCavanaugh**

### [Issue microsoft/TypeScript-go#3787](https://github.com/microsoft/TypeScript-go/issues/3787) (Open, `Needs More Info`)

**tsgo and tsc diverge on incomplete composite\-ref declaration cache: TS2305 vs filterable TS6305**

*tsgo reports TS2305 errors instead of TS6305 missing-declaration errors when the composite declaration cache is incomplete.*

 * created by **XavierGeerinck**
 * **RyanCavanaugh** added label `Needs More Info`
 * [today](https://github.com/microsoft/TypeScript-go/issues/3787#issuecomment-4454473597) **RyanCavanaugh** requested a concrete repro and explained that TS6305 is advisory for misconfigurations and not for build scheduling; recommended build tools analyze the project graph themselves

### [Issue microsoft/TypeScript-go#3792](https://github.com/microsoft/TypeScript-go/issues/3792) (Open, `Needs Investigation`, **andrewbranch**)

**\[lsp\] Experimental server capabilities should be defined on "experimental" object**

*Align server capabilities with the LSP specification by defining experimental features under the "experimental" property*

 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/3792#issuecomment-4415636188) **jakebailey** asked if not doing this was causing issues and stated that VS-related settings could not be changed
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/3792#issuecomment-4415658755) **rchl** pointed out a spec violation and suggested moving the properties to an experimental object and phasing out the root ones
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/3792#issuecomment-4415691581) **jakebailey** said "The VS ones are pretty locked in stone "
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.0 RC`, and assigned to **andrewbranch**

### [Issue microsoft/TypeScript-go#3800](https://github.com/microsoft/TypeScript-go/issues/3800) (Open, `bug`, `Domain: Editor`, `Crash`, **DanielRosenwasser**, **Copilot**)

**Error when auto\-importing relative \.css augmentation from ESM file with package\.json**

*Auto-importing a relative CSS augmentation in a NodeNext ESM project triggers a panic due to the unknown .css extension.*

 * (3 days ago) **DanielRosenwasser** added labels `bug`, `Domain: Editor`, `Crash`
 * (today) **DanielRosenwasser** assigned to **Copilot**, **DanielRosenwasser**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [Issue microsoft/TypeScript-go#3801](https://github.com/microsoft/TypeScript-go/issues/3801) (Open, `bug`, `Domain: Editor`, `Crash`, **RyanCavanaugh**, **gabritto**, **Copilot**)

**Unhandled case when auto\-completing decorator on private method under \-\-experimentalDecorators**

*Autocompleting a decorator on a private class method with experimentalDecorators enabled causes a panic due to an unhandled case in getClassElementPropertyKeyType.*

 * (2 days ago) **RyanCavanaugh** assigned to **gabritto**, **Copilot**, **RyanCavanaugh**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [PR microsoft/TypeScript-go#3808](https://github.com/microsoft/TypeScript-go/pull/3808) (Closed)

**Provide implicit index signatures for JS expando object literals**

*Consistently provide implicit index signatures for JavaScript expando object literals to catch circularity errors with noImplicitAny enabled.*

 * created by **ahejlsberg**
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#3810](https://github.com/microsoft/TypeScript-go/issues/3810) (Closed, `Domain: Editor`, **gabritto**)

**Deprecated members still shown in dropdown menu with \`editor\.suggest\.showDeprecated\` set to \`false\`**

*Deprecated object member 'a' still appears in the VS Code suggestion dropdown even though editor.suggest.showDeprecated is disabled.*

 * created by **Withered-Flower-0422**
 * **Withered-Flower-0422** added label `Domain: Editor`
 * (today) **RyanCavanaugh** set milestone to `TypeScript 7.0 RC`, and assigned to **gabritto**
 * (today) **gabritto** closed the issue

### [Issue microsoft/TypeScript-go#3815](https://github.com/microsoft/TypeScript-go/issues/3815) (Open)

**\`skipLibCheck\` does not suppress TS2320 when module augmentation in \`\.ts\` triggers interface merging conflict from \`\.d\.ts\`**

*skipLibCheck doesn't suppress TS2320 error caused by module augmentation in .ts exposing conflicting check signatures from .d.ts*

 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/3815#issuecomment-4433253772) **jakebailey** said "We have to issue it this way due to the multi-checker constraint; before it was nondeterministic which location we reported this, so now we report this consistently no matter the ordering."
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/3815#issuecomment-4433258910) **jakebailey** said "Is it just the = any?"
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/3815#issuecomment-4433834754) **jfirebaugh** said "It repros without = any."
 * [today](https://github.com/microsoft/TypeScript-go/issues/3815#issuecomment-4456030799) **Okanlawon2259** said "It's just any seem others are perfect "

### [PR microsoft/TypeScript-go#3824](https://github.com/microsoft/TypeScript-go/pull/3824) (Closed)

**Collect telemetry on recovered notification panics and stderr on unrecovered panics**

*Add telemetry for notification-based recovered panics and capture the last 40 stderr lines on unrecovered panics.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3824#issuecomment-4445444969) **andrewbranch** described that a specific commit restricted processing to lines between `panic:` and `Server exited` and ported the server-side stack sanitization
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3824#issuecomment-4445819430) **jakebailey** said "right, but I'm more thinking about if there's a panic followed by more text that some other goroutine is logging, interleaved. Maybe it just works?"
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3824#issuecomment-4445903738) **andrewbranch** said "The sanitizer redacts lines that don't match a recognized pattern."
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#3828](https://github.com/microsoft/TypeScript-go/pull/3828) (Closed)

**fix\(3810\): handle deprecated tags in completions**

*Add support for properly handling deprecated tags in code completions*

 * created by **a-tarasyuk**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3828#issuecomment-4444720376) **DanielRosenwasser** said "Is there some non-converted test that this should fix?"
 * (today) **gabritto** closed the issue

### [Issue microsoft/TypeScript-go#3829](https://github.com/microsoft/TypeScript-go/issues/3829) (Open, `Needs Investigation`, **ahejlsberg**)

**Behavior difference: tsgo fails to report TS8022 as tsc does**

*tsgo does not emit TS8022 errors for JSDoc '@extends' on non-class declarations in JavaScript files, unlike tsc*

 * created by **hkleungai**
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3829#issuecomment-4440059685) **hkleungai** mentioned that TS8022 appears to be a known issue and asked whether it is marked as `wontfix`
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.0 RC`, and assigned to **ahejlsberg**

### [PR microsoft/TypeScript-go#3835](https://github.com/microsoft/TypeScript-go/pull/3835) (Closed)

**Update README with current jsdoc/declarations status**

*Update the README’s JSDoc and type declarations status table with current completion details and encourage bug reports.*

 * created by **weswigham**
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript-go#3836](https://github.com/microsoft/TypeScript-go/pull/3836) (Open)

**fix\(workspace/symbol\): use name span in ProvideWorkspaceSymbols**

*ProvideWorkspaceSymbols now uses the identifier name span rather than the full declaration span to fix VS selection*

 * created by **joj**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3836#issuecomment-4445955151) **andrewbranch** described that the PR makes workspace symbols align with document symbols by including the name range so the cursor snaps to the name
 * [today](https://github.com/microsoft/TypeScript-go/pull/3836#issuecomment-4452730448) **jakebailey** said "You modified generated tests which isn't allowed; the top of the generated tests says how to manually modify them."

### [PR microsoft/TypeScript-go#3837](https://github.com/microsoft/TypeScript-go/pull/3837) (Open)

**Update snapshot and projects on file close**

*Update snapshots and clear closed projects upon file close to promptly remove stale diagnostics*

 * created by **gabritto**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3837#issuecomment-4453306181) **andrewbranch** asked how tsconfig diagnostics work in relation to project closure behavior in Strada
 * [today](https://github.com/microsoft/TypeScript-go/pull/3837#issuecomment-4453590148) **gabritto** noted that Strada did not clean up config diagnostics when a project closed

### [PR microsoft/TypeScript-go#3838](https://github.com/microsoft/TypeScript-go/pull/3838) (Closed)

**Speed up realpath on Linux and macOS**

*Opening files with O_PATH on Linux/macOS avoids EvalSymlinks and reduces realpath latency and memory allocations by over 50%.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3839](https://github.com/microsoft/TypeScript-go/pull/3839) (Closed)

**Don't double count approximateLength during tryReuseExistingNodeHelper**

*Resolve TS7056 error by avoiding double counting of approximateLength in tryReuseExistingNodeHelper*

 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3839#issuecomment-4447301257) **jakebailey** described the TypeScript call chain traversal and explained how reuse of type nodes failed due to fresh type object identity mismatches
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3839#issuecomment-4447560168) **jakebailey** demonstrated that using a recovery boundary to save and restore approximateLength corrected the double-counting issue
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3839#issuecomment-4448005111) **jakebailey** said "I have maybe a test, but it doesn't work because of the pre/post emit thing I think"
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3841](https://github.com/microsoft/TypeScript-go/issues/3841) (Closed, `wontfix`)

**Behavior difference: tsgo prints namespace in TS2740 but tsc does not**

*tsgo prints namespace-qualified types (fake.Mock) in TS2740 errors, whereas tsc prints unqualified type names (Mock).*

 * created by **hkleungai**
 * **RyanCavanaugh** added label `wontfix`
 * [today](https://github.com/microsoft/TypeScript-go/issues/3841#issuecomment-4454295866) **RyanCavanaugh** said "This is just better behavior; Mock is not a name in scope at that location, fake.Mock is"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#3842](https://github.com/microsoft/TypeScript-go/issues/3842) (Open)

**Missing support for namespaces in JSDoc types**

*Reinstate nested JSDoc typedef namespace support in tsgo, as the .d.ts workaround breaks single-file typing workflows.*

 * created by **remcohaszing**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3842#issuecomment-4453095244) **DanielRosenwasser** addressed conflict by suggesting using a non-declaration TypeScript file containing only ambient/emitless code
 * [today](https://github.com/microsoft/TypeScript-go/issues/3842#issuecomment-4454048561) **DanielRosenwasser** said "In this code, are you relying on others on the outside to reference simplematter as a type? Or is it just for local clarity?"
 * [later](https://github.com/microsoft/TypeScript-go/issues/3842#issuecomment-4458520862) **remcohaszing** explained that declaration emit permits a non-declaration TypeScript file with ambient code but doesn’t allow merging value and type-only namespaces in exports; justified exporting related types alongside values for import convenience; noted the dual role of @typedef and suggested TypeScript 7 could introduce local-only type support via a breaking change

### [Issue microsoft/TypeScript-go#3843](https://github.com/microsoft/TypeScript-go/issues/3843) (Closed, **andrewbranch**, **Copilot**)

**Add \`unstable\` to \`exports\` in \`package\.json\`**

*Add an unstable exports entry in package.json to expose the development API that may change before v7.0.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** set milestone to `TypeScript 7.0 RC`, and assigned to **andrewbranch**
 * **andrewbranch** assigned to **Copilot**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#3844](https://github.com/microsoft/TypeScript-go/pull/3844) (Closed, **andrewbranch**, **Copilot**)

**Add \`unstable\` to API \`exports\` in \`package\.json\`**

*Prefix all JavaScript API export paths with "unstable" in package.json and update test imports accordingly.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#3845](https://github.com/microsoft/TypeScript-go/pull/3845) (Open, **DanielRosenwasser**, **Copilot**)

**Fix panic when auto\-importing relative \.css augmentation from ESM file**

*Auto-importing ESM .css module augmentations panicked due to unrecognized extension, fixed by leaving filenames unchanged.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **DanielRosenwasser**

### [PR microsoft/TypeScript-go#3846](https://github.com/microsoft/TypeScript-go/pull/3846) (Open)

**Find all references API endpoints**

*Request to implement API endpoints that return all references for specified code symbols.*

 * created by **navya9singh**

### [PR microsoft/TypeScript-go#3847](https://github.com/microsoft/TypeScript-go/pull/3847) (Closed)

**Fixed user/workspace priority ordering for 'useTsgo' vscode setting**

*Enforce useTsgo configuration priority so workspace settings override user-level settings when determining its value.*

 * created by **johnfav03**
 * (today) **johnfav03** closed the issue

### [Issue microsoft/TypeScript-go#3848](https://github.com/microsoft/TypeScript-go/issues/3848) (Open, `Domain: Editor`, **DanielRosenwasser**)

**Issue warning when extensions try to contribute TSServer plugins that while \`useTsgo\` is on**

*Warn users when extensions contribute TSServer plugins with useTsgo enabled, offering Dismiss, Disable Native Preview, and Don't Show Again options.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** added label `Domain: Editor`, set milestone to `TypeScript 7.0 RC`, and assigned to **DanielRosenwasser**

### [PR microsoft/TypeScript-go#3849](https://github.com/microsoft/TypeScript-go/pull/3849) (Open, **RyanCavanaugh**, **Copilot**)

**Fix panic in overlayfs when saving a file without an overlay**

*Update overlayfs to gracefully treat saves on files without overlays as disk changes instead of panicking and add a test.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**

### [PR microsoft/TypeScript-go#3850](https://github.com/microsoft/TypeScript-go/pull/3850) (Open)

**Fixed CJS class expression exports emit anonymous constructor types**

*Exports of class expressions in CommonJS modules produce anonymous constructor types in the emitted output.*

 * created by **johnfav03**

### [PR microsoft/TypeScript-go#3851](https://github.com/microsoft/TypeScript-go/pull/3851) (Closed)

**Move @callback variadic baseline to accepted**

*Move the @callback variadic baseline default from 'baseline' to 'accepted'.*

 * created by **weswigham**
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript-go#3852](https://github.com/microsoft/TypeScript-go/pull/3852) (Closed)

**Accept @overload tag declaration changes**

*Disallow @overload tags on declarations that lack TypeScript overloads and eliminate redundant comments.*

 * created by **weswigham**
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript-go#3853](https://github.com/microsoft/TypeScript-go/pull/3853) (Closed)

**Use original node text when reporting cannot find name errors where possible**

*Use the original node text when reporting 'cannot find name' errors to improve error clarity.*

 * created by **weswigham**
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript-go#3854](https://github.com/microsoft/TypeScript-go/pull/3854) (Open)

**check that all files in \`"files"\` in tsconfig exist**

*Implement a check during tsconfig root file loading to confirm that all "files" entries exist.*

 * created by **iisaduan**

