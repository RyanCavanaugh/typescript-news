# Report for 2026-06-29 (Monday, June 29th, 2026)

14 different users commented on 65 different issues.

## Recommended Actions

 * Response Recommended
    * @rubenferreira97 asked if there was a rough estimate for when the fix might be merged in [microsoft/TypeScript-go#4301](https://github.com/microsoft/TypeScript-go/pull/4301#issuecomment-4834683150)
    * @rubenferreira97 asked whether the hanging-case assumption was incorrect and if a separate issue should be opened in [microsoft/TypeScript-go#4301](https://github.com/microsoft/TypeScript-go/pull/4301#issuecomment-4837554376)
    * @typescript-automation[bot] provided test results indicating everything looked good in [microsoft/TypeScript-go#4468](https://github.com/microsoft/TypeScript-go/pull/4468#issuecomment-4836089465)
    * @vborioni-onit provided a link to the reproduction repository in [microsoft/TypeScript-go#4469](https://github.com/microsoft/TypeScript-go/issues/4469#issuecomment-4841327866)
    * @Alex-Bond asked whether they should move the feature request to the main TS repo in [microsoft/TypeScript-go#4475](https://github.com/microsoft/TypeScript-go/issues/4475#issuecomment-4837530879)

## Activity Summary

### [PR microsoft/TypeScript-go#1686](https://github.com/microsoft/TypeScript-go/pull/1686) (Closed)

**Use package\.json locations to determine uptodate ness**

*Add support for using package.json file paths to determine update status, porting upstream and watch mode enhancements.*

 * created by **sheetalkamat**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2666](https://github.com/microsoft/TypeScript-go/issues/2666) (Closed, `Needs Investigation`, **johnfav03**)

**\`tsgo \-\-build\` fails to invalidate incremental cache after dependency update**

*tsgo's --build incremental cache does not detect updated dependency types and ignores resulting type errors.*

 * [9 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2666#issuecomment-4300070293) **rubenferreira97** described a hanging issue with tsgo --build due to stale .tsbuildinfo cache between versions and asked if they should open a new issue without a solid reproduction
 * (3 weeks ago) **RyanCavanaugh** set milestone to `Post-7.0`, and removed from milestone `TypeScript 7.0 RC`
 * (today) **DanielRosenwasser** set milestone to `TypeScript 7.0 Stable`, and removed from milestone `Post-7.0`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3391](https://github.com/microsoft/TypeScript-go/pull/3391) (Closed, **ahejlsberg**)

**Fix inference from unions of arrays with different nesting depths**

*Add a matching pass to infer equally nested arrays first, correcting generic type inference for unions like T[] | T[][]*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3391#issuecomment-4696630928) **typescript-automation[bot]** reported that the tsc results for the top 400 repos comparing main and the pull request merge looked good
 * (1 week ago) **jakebailey** set milestone to `TypeScript 7.0 Stable`, and removed from milestone `TypeScript 7.0 RC`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3518](https://github.com/microsoft/TypeScript-go/pull/3518) (Closed)

**fix\(native\-preview\): preserve lone surrogate string literals**

*Preserve lone UTF-16 surrogate literals in native-preview by adding WTF-8 decoding for binary AST while retaining UTF-8 fallback*

 * created by **TorinAsakura**
 * [9 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3518#issuecomment-4301346088) **TorinAsakura** agreed to the CLA with no company specified
 * **RyanCavanaugh** added to milestone `Possible Improvement`
 * [today](https://github.com/microsoft/TypeScript-go/pull/3518#issuecomment-4837029679) **jakebailey** asked for confirmation that only the text decoder changed, suggested no version bump, and requested a performance comparison
 * [later](https://github.com/microsoft/TypeScript-go/pull/3518#issuecomment-4843209284) **TorinAsakura** confirmed reading correctly, removed the protocol version bump, added a fast path for native TextDecoder, provided microbenchmarks comparing native and WTF-8 decoders, and concluded the change is a client-side bugfix without a protocol change

### [PR microsoft/TypeScript-go#4176](https://github.com/microsoft/TypeScript-go/pull/4176) (Closed)

**Cache more in getAlternativeContainingModules**

*Expand caching in getAlternativeContainingModules to reduce redundant computations and improve performance.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4257](https://github.com/microsoft/TypeScript-go/pull/4257) (Closed)

**Don't add global diags when not checking a file**

*Avoid storing global diagnostics for files that are not being checked to improve performance.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4301](https://github.com/microsoft/TypeScript-go/pull/4301) (Closed)

**Use package\.json locations for build up\-to\-date checks**

*Up-to-date build checks now leverage package.json locations for change detection.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4301#issuecomment-4834683150) **rubenferreira97** asked for a rough estimate for when the fix might be merged and highlighted the bug’s impact on larger codebases
 * (today) **jakebailey** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/4301#issuecomment-4837238374) **jakebailey** said "@rubenferreira97 In retrospect, I am very confused about your commentary; when I test your case, it also breaks in 6.0. How is this a problem for you with 7.0 specifically such that this is critical?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4301#issuecomment-4837554376) **rubenferreira97** asked whether the hanging-case assumption was incorrect and if a separate issue should be opened after describing two repro cases and plans to test the nightly build

### [PR microsoft/TypeScript-go#4313](https://github.com/microsoft/TypeScript-go/pull/4313) (Open)

**Assign checkers with cost/import\-aware algorithm**

*Use longest-processing-time scheduling combined with bounded import-graph refinement to assign files to checkers, reducing memory usage and improving type-checking performance.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4313#issuecomment-4723995071) **typescript-automation[bot]** posted a build status update with a table of command status and results links
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4313#issuecomment-4724128046) **typescript-automation[bot]** reported the results of the requested performance run
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4313#issuecomment-4724162463) **jakebailey** said "Weird. Simplifying the algorithm to just use text made it a lot worse in time?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4313#issuecomment-4838562747) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4313#issuecomment-4838563652) **typescript-automation[bot]** started perf test jobs and provided status and results links
 * [today](https://github.com/microsoft/TypeScript-go/pull/4313#issuecomment-4838688100) **typescript-automation[bot]** posted the requested perf run results with tsc comparison metrics

### [PR microsoft/TypeScript-go#4330](https://github.com/microsoft/TypeScript-go/pull/4330) (Closed)

**Move everything to new VS Code extension**

*Consolidate all current functionality and resources into the newly created VS Code extension.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4357](https://github.com/microsoft/TypeScript-go/pull/4357) (Closed)

**Lint on all OSs**

*Run lint checks on all operating systems in CI to simplify maintenance and avoid omissions.*

 * created by **jakebailey**
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4357#issuecomment-4744155276) **jakebailey** said "45 minutes, yikes"
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4358](https://github.com/microsoft/TypeScript-go/issues/4358) (Closed, `bug`, **jakebailey**, **Copilot**)

**SourceFile\.ContainsNonASCII can be false for non\-ASCII in string literal fast path**

*Non-ASCII characters inside simple string literals bypass detection in SourceFile.ContainsNonASCII, resulting in incorrect UTF-16 position mapping.*

 * **jakebailey** assigned to **jakebailey**
 * (6 days ago) **RyanCavanaugh** added label `bug`, and set milestone to `TypeScript 7.0 Stable`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4370](https://github.com/microsoft/TypeScript-go/issues/4370) (Closed, `Domain: Editor`, **jakebailey**, **Copilot**)

**\`js/ts\.preferences\.useAliasesForRenames\` not respected**

*Disabling js/ts.preferences.useAliasesForRenames has no effect in VS Code’s native TypeScript extension, causing renamed imports to be aliased rather than updated at their source.*

 * (1 week ago) **jakebailey** assigned to **Copilot**, **jakebailey**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 Stable`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4391](https://github.com/microsoft/TypeScript-go/issues/4391) (Closed, `bug`, **ahejlsberg**)

**const type parameter doesn't capture string\-literal property when the parameter type is wrapped in Omit\<\.\.\.\>**

*A const type parameter on interface call signatures loses string-literal property inference when the parameter type uses Omit<…>.*

 * **RyanCavanaugh** added to milestone `TypeScript 7.0 Stable`
 * (today) **ahejlsberg** added label `bug`, and removed label `Needs Investigation`
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#4395](https://github.com/microsoft/TypeScript-go/pull/4395) (Closed)

**Devirtualize ForEachChild and IterChildren**

*Generate specialized implementations for ForEachChild and IterChildren to eliminate interface calls and improve inlining.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4395#issuecomment-4770210933) **jakebailey** said "@typescript-bot perf test this"
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4395#issuecomment-4770211791) **typescript-automation[bot]** started jobs and provided build status and result links
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4395#issuecomment-4770451413) **typescript-automation[bot]** provided the results of the requested performance run with a detailed comparison report
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4437](https://github.com/microsoft/TypeScript-go/issues/4437) (Closed)

**\`checkJs\` seems to default to true erroneously**

*tsgo implicitly enables checkJs by default, leading to erroneous JSDoc modifier errors in JavaScript files unless checkJs is explicitly disabled.*

 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/4437#issuecomment-4794121041) **freshp86** asked why certain errors were suppressed when checkJs was false despite explicit configuration
 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/4437#issuecomment-4796606071) **danyalahmed1995** noted that the errors occur during the JSDoc reparse process and asked whether validation should move or reparsed JSDoc modifiers should skip grammar diagnostics for JS/JSX
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/4437#issuecomment-4804727384) **RyanCavanaugh** explained that checkJs has tristate behavior in TS 6 and illustrated it with an example showing different errors for false, unspecified, and true settings
 * [today](https://github.com/microsoft/TypeScript-go/issues/4437#issuecomment-4836493237) **Zelys-DFKH** noted that PR #4448 addressed the issue and asked if it could be closed
 * [today](https://github.com/microsoft/TypeScript-go/issues/4437#issuecomment-4836501102) **jakebailey** said "Yes, not sure why it was not linked."
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4439](https://github.com/microsoft/TypeScript-go/issues/4439) (Closed, `bug`, **andrewbranch**, **Copilot**)

**Feature Request: Permit backward\-compatible version checks at main export**

*Add a main package export for TypeScript 7 to enable backward-compatible version checks and avoid load errors.*

 * (4 days ago) **RyanCavanaugh** added label `bug`, and set milestone to `TypeScript 7.0 Stable`
 * **andrewbranch** assigned to **Copilot**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4443](https://github.com/microsoft/TypeScript-go/pull/4443) (Open)

**Fixed build mode false negative from export\-star facade**

*Fix false negative TypeScript build-mode error caused by export-star facade usage.*

 * created by **johnfav03**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4443#issuecomment-4836710462) **jakebailey** noted that the proposal seemed reasonable but contained a lot of text for the key and requested a vibe check from @andrewbranch

### [Issue microsoft/TypeScript-go#4462](https://github.com/microsoft/TypeScript-go/issues/4462) (Open, **ahejlsberg**)

**Regression \(7\.0\.0\-dev\.20260624\.1\): intersection type member dropped in generic position — TanStack Router \`stripSearchParams\` rejected \(TS2322\), clean in tsc \+ 20260623\.1**

*Upgrading to @typescript/native-preview 7.0.0-dev.20260624.1 drops members from intersection types in generics, triggering TS2322 errors in TanStack Router.*

 * created by **meabed**
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/4462#issuecomment-4822638054) **meabed** provided a runnable reproduction repository with instructions demonstrating the error
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/4462#issuecomment-4823299573) **jakebailey** said "Bisects to #4389 @ahejlsberg "
 * **ahejlsberg** assigned to **ahejlsberg**

### [Issue microsoft/TypeScript-go#4463](https://github.com/microsoft/TypeScript-go/issues/4463) (Closed, `bug`, **ahejlsberg**)

**Regression in 20260613\.1 pertaining to conditional types**

*tsgo 7.0.0-dev.20260613.1 introduces a regression that causes valid conditional JSONSchema types to fail compilation.*

 * (today) **ahejlsberg** added label `bug`, set milestone to `TypeScript 7.0 Stable`, and assigned to **ahejlsberg**
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#4464](https://github.com/microsoft/TypeScript-go/issues/4464) (Open, `Type Ordering`)

**Wrong type\-argument inference from a union of arrays when one member is absorbed by a fixed arm of the target**

*tsgo infers V as MyError instead of {event:number} by absorbing the MyError[] arm into Error in a union of arrays*

 * created by **shkreios**
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/4464#issuecomment-4827716621) **jakebailey** said "You should test 6.0 with --stableTypeOrdering"
 * [today](https://github.com/microsoft/TypeScript-go/issues/4464#issuecomment-4831897515) **shkreios** said "testing 6.0 with --stableTypeOrdering reproduces it exactly. So this isn't tsgo-specific; it's the stable type ordering that tsgo defaults to."
 * **ahejlsberg** added label `Type Ordering`

### [Issue microsoft/TypeScript-go#4465](https://github.com/microsoft/TypeScript-go/issues/4465) (Open, `Type Ordering`)

**False TS2321 "Excessive stack depth comparing types" for a hand\-rolled UnionToTuple recursion evaluated in a generic context**

*tsgo incorrectly reports an excessive stack depth error for a generic UnionToTuple recursion that tsc accepts*

 * created by **shkreios**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4465#issuecomment-4831896563) **shkreios** said "testing 6.0 with --stableTypeOrdering reproduces it exactly. So this isn't tsgo-specific; it's the stable type ordering that tsgo defaults to."
 * **ahejlsberg** added label `Type Ordering`

### [PR microsoft/TypeScript-go#4466](https://github.com/microsoft/TypeScript-go/pull/4466) (Closed)

**investigation: nil pointer dereference in completions after JSDoc comment**

*Requesting completions at class or interface members preceded by JSDoc comments causes a nil pointer dereference panic.*

 * created by **vscodenpa**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4468](https://github.com/microsoft/TypeScript-go/pull/4468) (Closed)

**Add conditional type base constraint limiter**

*Revert the previous implementation and introduce a base constraint limiter to cap distributive conditional type exploration at depth 100.*

 * created by **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4468#issuecomment-4835536992) **jakebailey** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4468#issuecomment-4835537507) **typescript-automation[bot]** posted CI build status update for test top400 and perf test this faster jobs
 * [today](https://github.com/microsoft/TypeScript-go/pull/4468#issuecomment-4835731496) **typescript-automation[bot]** posted automated performance run results
 * [today](https://github.com/microsoft/TypeScript-go/pull/4468#issuecomment-4836089465) **typescript-automation[bot]** reported test results for the top 400 repos and indicated that everything looked good
 * [today](https://github.com/microsoft/TypeScript-go/pull/4468#issuecomment-4837518780) **ahejlsberg** noted that they hadn’t seen Copilot suggest that solution and said the approach, though not ideal, matched existing limiters and worked without semantic changes
 * [today](https://github.com/microsoft/TypeScript-go/pull/4468#issuecomment-4837553709) **jakebailey** said "I am unfortunately confusing it for one of the other many PRs copilot has opened to add a limiter"
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#4469](https://github.com/microsoft/TypeScript-go/issues/4469) (Closed)

**const enum in ambient declare namespace causes import alias to be incorrectly elided in emitted JS**

*Declaring a const enum in an ambient namespace causes an import alias to be omitted from emitted JavaScript.*

 * created by **vborioni-onit**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4469#issuecomment-4836985207) **jakebailey** said "Can you make a repo for this instead of uploading a zip to OneDrive? Hard to trust an arbitrary download and zip file 😄 "
 * [later](https://github.com/microsoft/TypeScript-go/issues/4469#issuecomment-4841327866) **vborioni-onit** shared a link to the reproduction repository on GitHub

### [PR microsoft/TypeScript-go#4470](https://github.com/microsoft/TypeScript-go/pull/4470) (Closed)

**Don't expose internal symbol name prefix in sig help, node printing**

*Prevent exposing internal symbol name prefixes in signature help and restore unescaped names in node printing to match previous behavior*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4471](https://github.com/microsoft/TypeScript-go/pull/4471) (Closed)

**Reduce code size of lsproto package, use JSON roundtripping in fourslash**

*Reduce lsproto binary size by 580KB by deferring type decoding, employing JSON roundtrips in fourslash, and using reflection-based unmarshalling.*

 * created by **jakebailey**

### [Issue microsoft/TypeScript-go#4472](https://github.com/microsoft/TypeScript-go/issues/4472) (Closed, `Domain: API and Extensibility`, **andrewbranch**, **Copilot**)

**visitNodeArray visits child nodes twice**

*visitNodeArray in tsgo's TypeScript unstable API traverses child nodes twice, causing duplicate visits.*

 * created by **acutmore**
 * (today) **andrewbranch** added label `Domain: API and Extensibility`, and assigned to **andrewbranch**, **Copilot**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#4473](https://github.com/microsoft/TypeScript-go/pull/4473) (Closed, **andrewbranch**, **Copilot**)

**Fix RemoteNode\.forEachChild visiting array children twice when a visitList callback is supplied**

*Fix RemoteNode.forEachChild’s double-traversal of NodeArray children by making visitList and per-node iteration exclusive*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#4474](https://github.com/microsoft/TypeScript-go/pull/4474) (Open)

**Big string union optimizations**

*Deferring sorting and disabling suggestion generation in large string unions speeds up tsgo type checking by 3–5×.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4474#issuecomment-4836932883) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4474#issuecomment-4836933649) **typescript-automation[bot]** posted build status update with links to job start and results
 * [today](https://github.com/microsoft/TypeScript-go/pull/4474#issuecomment-4837145515) **typescript-automation[bot]** posted the requested performance run results
 * [today](https://github.com/microsoft/TypeScript-go/pull/4474#issuecomment-4837348305) **jakebailey** said "Sort of what I was expecting; nothing in our actual test suite."

### [Issue microsoft/TypeScript-go#4475](https://github.com/microsoft/TypeScript-go/issues/4475) (Open)

**Feature request: machine\-readable \(JSONL\) diagnostics output**

*Add a JSONL output flag to the TypeScript compiler to provide machine-readable diagnostics in watch and noEmit modes.*

 * created by **Alex-Bond**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4475#issuecomment-4837443797) **jakebailey** referred to two TypeScript issues, noted uncertainty about the correct repo for the feature request, mentioned Google also requested it, and indicated it likely wouldn't be implemented in v7.0
 * [today](https://github.com/microsoft/TypeScript-go/issues/4475#issuecomment-4837530879) **Alex-Bond** asked whether to move the feature request to the main TS repo and suggested creating adapters for customizable outputs while keeping current flags until 8.0
 * [today](https://github.com/microsoft/TypeScript-go/issues/4475#issuecomment-4837568101) **jakebailey** doubted that adapters would be supported or included in version 7.0 and suggested moving the feature while relying on the API
 * [today](https://github.com/microsoft/TypeScript-go/issues/4475#issuecomment-4837661744) **Alex-Bond** agreed to target the change for version 7.1 to avoid additional cleanup, acknowledged overengineering by considering SARIF, JSONL, and template outputs, and explained the adapter motivation

### [Issue microsoft/TypeScript-go#4476](https://github.com/microsoft/TypeScript-go/issues/4476) (Open, `Domain: Editor`, **gabritto**)

**Only show notifications for failed LSP responses in VS Code Insiders**

*Only surface failed language server response notifications by default in VS Code Insiders, with an optional setting for others.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** added label `Domain: Editor`, set milestone to `TypeScript 7.0 Stable`, and assigned to **gabritto**

### [PR microsoft/TypeScript-go#4477](https://github.com/microsoft/TypeScript-go/pull/4477) (Closed)

**Update submodule**

*Update the submodule to pull in upstream lib.d.ts and test changes.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4478](https://github.com/microsoft/TypeScript-go/issues/4478) (Closed, **DanielRosenwasser**, **Copilot**)

**Crash from nil Contents of package\.json resolved through peerDependencies**

*The Go module resolver panics when attempting to read peerDependencies from a nil package.json.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** assigned to **Copilot**, **DanielRosenwasser**

### [PR microsoft/TypeScript-go#4479](https://github.com/microsoft/TypeScript-go/pull/4479) (Closed, **DanielRosenwasser**, **Copilot**)

**Avoid nil package\.json crash when resolving peer dependencies**

*The resolver now treats nil-content peer dependency package.json entries as missing metadata to prevent panics during resolution.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **DanielRosenwasser**

### [PR microsoft/TypeScript-go#4480](https://github.com/microsoft/TypeScript-go/pull/4480) (Closed)

**Run symbol\-returning completion on the API checker**

*Use CheckerLifetimeAPI in handleGetCompletionsAtPosition to ensure consistent symbol resolution, avoid nil-pointer panics, and add documentation and a regression test.*

 * created by **Vorobey31415**
 * [later](https://github.com/microsoft/TypeScript-go/pull/4480#issuecomment-4841415885) **Vorobey31415** said "@microsoft-github-policy-service agree company="JetBrains""

### [Issue microsoft/TypeScript-go#4481](https://github.com/microsoft/TypeScript-go/issues/4481) (Open, `Domain: Editor`, **DanielRosenwasser**, **Copilot**)

**Auto\-imports hits unimplemented \`GetSourceOfProjectReferenceIfOutputIncluded\`**

*The auto-import process crashes with a stack trace due to the unimplemented GetSourceOfProjectReferenceIfOutputIncluded method.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** added labels `Domain: Editor`, `blocked`, and removed label `blocked`
 * [today](https://github.com/microsoft/TypeScript-go/issues/4481#issuecomment-4840687832) **DanielRosenwasser** said "Probably similar to #4322"
 * (today) **DanielRosenwasser** assigned to **Copilot**, **DanielRosenwasser**

### [PR microsoft/TypeScript-go#4482](https://github.com/microsoft/TypeScript-go/pull/4482) (Open, **DanielRosenwasser**, **Copilot**)

**Fix auto\-imports crash in GetSourceOfProjectReferenceIfOutputIncluded**

*Prevent aliasResolver panics in GetSourceOfProjectReferenceIfOutputIncluded by returning file.FileName() and adding a regression test*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **DanielRosenwasser**

### [PR microsoft/TypeScript-go#4483](https://github.com/microsoft/TypeScript-go/pull/4483) (Closed)

**Handle unloaded projects in API snapshot responses**

*Prevent nil pointer panics in updateSnapshot by properly handling unloaded ancestor tsconfig projects lacking command line data.*

 * created by **ulitink**
 * [later](https://github.com/microsoft/TypeScript-go/pull/4483#issuecomment-4842344803) **ulitink** said "@microsoft-github-policy-service agree company="JetBrains""

### [Issue microsoft/TypeScript-go#4484](https://github.com/microsoft/TypeScript-go/issues/4484) (Open)

**project reference { "path": "" } is ignored**

*tsgo build ignores project references with an empty path (""), while tsc correctly includes them unless changed to "./".*

 * created by **HolgerJeromin**

