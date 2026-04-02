# Report for 2025-12-10 (Wednesday, December 10th, 2025)

20 different users commented on 47 different issues.

## Recommended Actions

 * Moderation
    * @Paul-16098 posted irrelevant debug log in [microsoft/TypeScript-go#2236](https://github.com/microsoft/TypeScript-go/issues/2236#issuecomment-3640382400)
 * Response Recommended
    * @maxkostow asked whether the change would impact the LSP or if a separate issue should be filed in [microsoft/TypeScript-go#1622](https://github.com/microsoft/TypeScript-go/issues/1622#issuecomment-3638700009)
    * @MisterJimson reported that tsgo fails to apply module augmentations for SST v2 projects, causing TS2339 errors in [microsoft/TypeScript-go#2234](https://github.com/microsoft/TypeScript-go/issues/2234#issuecomment-3642213777)
    * @Hemantvetal provided repro steps as requested in [microsoft/TypeScript-go#2340](https://github.com/microsoft/TypeScript-go/issues/2340#issuecomment-3640634938)
    * @jgsheppa provided CLA agreement as requested in [microsoft/TypeScript-go#2342](https://github.com/microsoft/TypeScript-go/pull/2342#issuecomment-3642030501)

## Activity Summary

### [Issue microsoft/TypeScript-go#1622](https://github.com/microsoft/TypeScript-go/issues/1622) (Open, `Crash`, `Domain: Program`, `Domain: Performance`, **sheetalkamat**)

**\[bug\] \`tsgo \-\-build\` uses extreme amounts of memory**

*tsgo --build exhausts over 100GB of memory and crashes when building large monorepos with thousands of TypeScript projects*

 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/1622#issuecomment-3628462817) **maxkostow** mentioned that the LSP lacked --singleThreaded support, described tuning GOGC/GOMEMLIMIT via the VS Code extension, and suggested exposing these settings until better defaults exist
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/1622#issuecomment-3632620368) **Knagis** reported the same issue with high memory usage and OOM when building ~1000 TS projects and noted that using --singleThreaded worked fine and remained faster than tsc
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/1622#issuecomment-3633202774) **jakebailey** said "@sheetalkamat Can you resurrect your change to limit the number of concurrent project builds? We have --checkers, but I think we were also wanting to add --builders to control that number."
 * [today](https://github.com/microsoft/TypeScript-go/issues/1622#issuecomment-3638634504) **jakebailey** requested that they try build mode with `--builders 1`
 * [today](https://github.com/microsoft/TypeScript-go/issues/1622#issuecomment-3638700009) **maxkostow** said "Is that expected to impact the LSP or should there be a separate issue for the LSP?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/1622#issuecomment-3638704557) **jakebailey** dismissed that as unrelated to the thread, clarified that build mode wasn't part of the language server, pointed to issue #2239, and suggested filing separate issues for distinct cases

### [Issue microsoft/TypeScript-go#2234](https://github.com/microsoft/TypeScript-go/issues/2234) (Open)

**tsgo eagerly resolve the type of inferred function Expression**

*tsgo eagerly resolves inferred function expression types, causing Record<keyof TestInterface, string> to collapse to Record<never, string> without explicit annotations.*

 * [6 days ago](https://github.com/microsoft/TypeScript-go/issues/2234#issuecomment-3614675362) **jakebailey** said "They are "the same" in that they both involve the fact that declaration emit used to reuse nodes when possible, but currently does not. But the underlying cause is not the same, no."
 * [6 days ago](https://github.com/microsoft/TypeScript-go/issues/2234#issuecomment-3614689338) **brokenmass** apologized for misunderstanding 'reusing nodes' and asked for clarification, expressed willingness to provide more info, and argued that the emitter shouldn't resolve keyof an exported interface
 * [6 days ago](https://github.com/microsoft/TypeScript-go/issues/2234#issuecomment-3614692174) **jakebailey** observed that the emitter resolved keyof exported interfaces until somewhat recently
 * [later](https://github.com/microsoft/TypeScript-go/issues/2234#issuecomment-3642213777) **MisterJimson** explained that tsgo failed to apply SST’s module augmentations, causing TS2339 errors on Config.STAGE and Config.API_URL and making tsgo unusable for SST v2 projects

### [Issue microsoft/TypeScript-go#2236](https://github.com/microsoft/TypeScript-go/issues/2236) (Open, `Crash`)

**Crashing when project path contains Chinese characters\.**

*VSCode TypeScript Native plugin crashes with a regex compile error when project paths include Chinese characters*

 * **CryUshio** added label `Crash`
 * [6 days ago](https://github.com/microsoft/TypeScript-go/issues/2236#issuecomment-3615214493) **jakebailey** said "Likely this would be fixed by #1947."
 * [6 days ago](https://github.com/microsoft/TypeScript-go/issues/2236#issuecomment-3615214820) **jakebailey** said "A full backtrace would be helpful."
 * [today](https://github.com/microsoft/TypeScript-go/issues/2236#issuecomment-3640382400) **Paul-16098** posted a debug log of configuration settings

### [Issue microsoft/TypeScript-go#2260](https://github.com/microsoft/TypeScript-go/issues/2260) (Open, `Domain: Editor`)

**Inherited methods not merging JSDoc comments**

*tsgo fails to merge inherited JSDoc comments into overridden methods, showing only new @remarks tags.*

 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/2260#issuecomment-3623586239) **LukeAbby** mentioned they had assumed the behavior was intentional and requested a way to simulate the old behavior with @inheritDoc, noting the pattern’s extensive use and clarifying the summary/remarks merging behavior
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/2260#issuecomment-3628460459) **jakebailey** said "FWIW there is a PR for this in #2262. @LukeAbby does it do what you expect?"
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/2260#issuecomment-3628872763) **LukeAbby** indicated that the PR didn't fully work due to literal JSDoc concatenation and suggested restoring old behavior or adding an opt-in for merging docs with @inheritDoc
 * **jakebailey** added label `Domain: Editor`

### [Issue microsoft/TypeScript-go#2271](https://github.com/microsoft/TypeScript-go/issues/2271) (Closed, `bug`, `Domain: Declaration Emit`, **weswigham**)

**Invalid declaration emit for enum value type**

*tsgo generates invalid declaration files by emitting enum references as import(...).A instead of import(...).Teams.A, causing a namespace error.*

 * (2 days ago) **ahejlsberg** added labels `Domain: Declaration Emit`, `bug`, and assigned to **weswigham**
 * (today) **gabritto** closed the issue

### [Issue microsoft/TypeScript-go#2275](https://github.com/microsoft/TypeScript-go/issues/2275) (Open, `Domain: Editor`, **sheetalkamat**)

**Race condition detected between program updates and ATA\(?\)**

*Concurrent program updates and automatic type acquisition operations trigger a race condition, causing unexpected completion responses.*

 * created by **DanielRosenwasser**
 * **DanielRosenwasser** assigned to **sheetalkamat**
 * **jakebailey** added label `Domain: Editor`

### [Issue microsoft/TypeScript-go#2280](https://github.com/microsoft/TypeScript-go/issues/2280) (Open, `Domain: Editor`, **gabritto**)

**Port \`implement interface\` quick fix**

*Port the implement interface quick fix from TypeScript to TS-Go to provide automated interface implementation support.*

 * created by **mjbvz**
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2280#issuecomment-3632504763) **Tyriar** said "This is up there with most used quick fixes."
 * **jakebailey** added label `Domain: Editor`
 * **gabritto** assigned to **gabritto**

### [Issue microsoft/TypeScript-go#2282](https://github.com/microsoft/TypeScript-go/issues/2282) (Open)

**Request for official prebuilt Windows binaries \(tsgo\.exe\) published via GitHub Releases, without requiring npm\.**

*Officially distribute Windows tsgo.exe binaries via GitHub Releases to enable TypeScript use without npm.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2282#issuecomment-3630893984) **PaulHuizer** pondered delivering TsGo.exe via NuGet as an MsBuild target and suggested a tsgo.exe integrating into MsBuild to compile TypeScript
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2282#issuecomment-3631797657) **jakebailey** said "If you're using vue or any other lib, isn't it implied that you already are using npm?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2282#issuecomment-3636626028) **PaulHuizer** explained that they used Blazor SSR, Vue Global, and ES Modules, preferring TypeScript via TsGen for the BFF API, and that Node.js was only needed for TS compilation, with TsGo potentially eliminating the Node.js requirement
 * [today](https://github.com/microsoft/TypeScript-go/issues/2282#issuecomment-3638056870) **joj** asked how Blazor dependencies were being managed, how Vue was integrated, and which IDE was used, and mentioned working on a nuget package for tsgo.exe without npm/node dependencies but without an ETA
 * [today](https://github.com/microsoft/TypeScript-go/issues/2282#issuecomment-3638425819) **PaulHuizer** praised tsgo.exe as a NuGet package without npm/node dependencies

### [Issue microsoft/TypeScript-go#2285](https://github.com/microsoft/TypeScript-go/issues/2285) (Open, `Domain: Editor`)

**Backticked JSDOC \`{@link}\`s in tagless descriptions docblocks are broken**

*Backticked JSDoc {@link} tags in tagless description comments fail to render properly in VS Code hover tooltips.*

 * (2 days ago) **mjbvz** removed labels `bug`, `javascript`, and unassigned **mjbvz**
 * **jakebailey** added label `Domain: Editor`

### [Issue microsoft/TypeScript-go#2299](https://github.com/microsoft/TypeScript-go/issues/2299) (Open, `Crash`, **sheetalkamat**)

**Crash on find\-all\-references on \`this\`**

*VS Code's find-all-references on the `this` keyword panics with a slice bounds out of range error.*

 * created by **DanielRosenwasser**
 * **DanielRosenwasser** added label `Crash`
 * **DanielRosenwasser** assigned to **sheetalkamat**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2299#issuecomment-3639548679) **DanielRosenwasser** said "Also happens on the this at https://github.com/microsoft/TypeScript/blob/366da34ae60b458e97c880fedf33298d6842ddd6/src/server/project.ts#L945"

### [Issue microsoft/TypeScript-go#2300](https://github.com/microsoft/TypeScript-go/issues/2300) (Closed, `Crash`)

**Inlay hints crash with element access name**

*TypeScript’s inlay hints feature crashes when encountering element access property names like Symbol['dispose'].*

 * created by **DanielRosenwasser**
 * **DanielRosenwasser** added label `Crash`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2300#issuecomment-3639547070) **DanielRosenwasser** said "I got this from a test file after trying out #2273, but I guess I was running an old version?"
 * (today) **DanielRosenwasser** closed the issue

### [Issue microsoft/TypeScript-go#2306](https://github.com/microsoft/TypeScript-go/issues/2306) (Closed, `Domain: Editor`, **ahejlsberg**)

**The \`@see\` JSDoc tag cannot create links from URLs**

*Hover tooltips for JSDoc @see URLs are rendered incorrectly and not clickable in the TS Native Preview extension.*

 * [today](https://github.com/microsoft/TypeScript-go/issues/2306#issuecomment-3637419123) **csvn** suggested starting a PR and linking to the issue since non-maintainers are not usually assigned issues
 * [today](https://github.com/microsoft/TypeScript-go/issues/2306#issuecomment-3637524090) **jakebailey** said "You can't assign a non-member, no, and even if so: https://github.com/microsoft/TypeScript/blob/main/CONTRIBUTING.md#issue-claiming"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2306#issuecomment-3637583842) **csvn** said "Ah, sorry. I hadn't read that part 😅 "
 * [today](https://github.com/microsoft/TypeScript-go/issues/2306#issuecomment-3637913437) **maishivamhoo123** apologized for missing the CONTRIBUTING.md point, confirmed reading the issue-claiming section, and stated intent to open a PR if able to fix it
 * **jakebailey** added label `Domain: Editor`

### [PR microsoft/TypeScript-go#2307](https://github.com/microsoft/TypeScript-go/pull/2307) (Closed)

**Add \-\-builders to limit number of projects can build concurrently**

*Introduce a --builders flag to limit how many projects can be built concurrently.*

 * created by **sheetalkamat**
 * (today) **sheetalkamat** closed the issue

### [PR microsoft/TypeScript-go#2311](https://github.com/microsoft/TypeScript-go/pull/2311) (Closed)

**Genericize ref counting caches; fix extended config cache bug**

*Make reference-counted caches generic for shared use and fix a bug in extended config caching.*

 * created by **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#2312](https://github.com/microsoft/TypeScript-go/issues/2312) (Closed, `Crash`, **Copilot**)

**Signature help crash on call target when nested call has trailing comma**

*Quickly requesting signature help on a nested call expression with a trailing comma causes an index out-of-range panic.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2312#issuecomment-3635060135) **DanielRosenwasser** speculated that a semantic command raced with signature help causing it to sometimes use resolved data and making the issue hard to reproduce in the editor
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2312#issuecomment-3635144716) **DanielRosenwasser** provided a minimal repro example requesting signature help at a marker with generic outer and inner calls having trailing commas
 * **DanielRosenwasser** assigned to **Copilot**
 * (today) **DanielRosenwasser** closed the issue

### [Issue microsoft/TypeScript-go#2313](https://github.com/microsoft/TypeScript-go/issues/2313) (Closed, `bug`, `Domain: Editor`, **ahejlsberg**)

**Bare TypeScript code in \`@example\` is interpreted as Markdown/HTML**

*Unfenced TypeScript code in JSDoc @example tags is parsed as Markdown/HTML under tsgo, causing formatting issues.*

 * created by **tats-u**
 * **jakebailey** added label `Domain: Editor`
 * (today) **ahejlsberg** added label `bug`, and assigned to **ahejlsberg**
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#2314](https://github.com/microsoft/TypeScript-go/pull/2314) (Closed)

**Reapply Program diagnostic func update, CheckerPool cleanup**

*Reapply program diagnostic updates with concurrent per-file checking, thread-safe diagnostics collection, and CheckerPool cleanup.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2314#issuecomment-3638209755) **jakebailey** said "I'm going to merge this as-is; I have a followup about options diags and another for the GetTypeChecker thing but they are not critical."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2315](https://github.com/microsoft/TypeScript-go/pull/2315) (Closed, **DanielRosenwasser**, **Copilot**)

**Fix signature help crash when nested call has trailing comma**

*Signature help requests crash in nested calls with trailing commas due to an out-of-bounds argument index*

 * (yesterday) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2315#issuecomment-3635766541) **Copilot** fixed the test to use the minimal repro with the correct marker position to reproduce the crash
 * (today) **DanielRosenwasser** closed the issue

### [Issue microsoft/TypeScript-go#2317](https://github.com/microsoft/TypeScript-go/issues/2317) (Open)

**Console is not cleared in watch mode \(also does not show the 0 error count output\)**

*tsgo’s watch mode fails to clear the console between builds and omits the “Found 0 errors” message*

 * created by **gitter-me**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2317#issuecomment-3638431035) **jakebailey** said "This comes down to us not using a diagnostic message in DoCycle, and so TryClearScreen does not detect the starting message and does not issue the screen clearing codes."
 * [today](https://github.com/microsoft/TypeScript-go/issues/2317#issuecomment-3638438200) **jakebailey** said "Well, rather, I think the watch mode for non-build-mode is just not using the right messages."

### [PR microsoft/TypeScript-go#2319](https://github.com/microsoft/TypeScript-go/pull/2319) (Closed)

**fix\(2271\): Invalid declaration emit for enum value type**

*Corrects invalid enum value type declaration emissions to produce accurate declaration files.*

 * created by **a-tarasyuk**
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript-go#2320](https://github.com/microsoft/TypeScript-go/pull/2320) (Closed)

**Don't use file GetOrCreateToken for change tracker**

*file.GetOrCreateToken should only materialize existing file tokens and not be used to create missing tokens.*

 * created by **gabritto**
 * (today) **gabritto** closed the issue

### [Issue microsoft/TypeScript-go#2321](https://github.com/microsoft/TypeScript-go/issues/2321) (Open, `Domain: Type Checking`)

**Inference from variable reference produces different type argument**

*tsgo's generic inference for deepEqual retains undefined properties from a variable type, causing type errors when passing a narrower literal.*

 * created by **dragomirtitian**
 * **jakebailey** added label `Domain: Type Checking`
 * [later](https://github.com/microsoft/TypeScript-go/issues/2321#issuecomment-3642054391) **Andarist** identified that the issue bisected to a TypeScript 6.0 port and explained how prioritizing non-literal candidates improved type selection

### [PR microsoft/TypeScript-go#2322](https://github.com/microsoft/TypeScript-go/pull/2322) (Open)

**Remove GetOptionsDiagnostics**

*Remove GetOptionsDiagnostics and replace it with separate GetConfigFileParsingDiagnostics and GetGlobalDiagnostics to prevent redundant diagnostic aggregation.*

 * created by **jakebailey**

### [Issue microsoft/TypeScript-go#2323](https://github.com/microsoft/TypeScript-go/issues/2323) (Closed, `Domain: Emit`, `Domain: Declaration Emit`, **Copilot**)

**JSDoc comment removed from default export**

*tsgo removes JSDoc comments from default exports whereas TypeScript 5.9 preserves them*

 * created by **dragomirtitian**
 * (today) **jakebailey** added labels `Domain: Emit`, `Domain: Declaration Emit`, and assigned to **Copilot**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2324](https://github.com/microsoft/TypeScript-go/pull/2324) (Closed, **jakebailey**, **Copilot**)

**Fix JSDoc comment preservation on default export in declaration emit**

*Fix preserveJsDoc to correctly copy JSDoc comments for default exports in declaration file emission.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2325](https://github.com/microsoft/TypeScript-go/issues/2325) (Closed, `Domain: Emit`)

**Extra parentheses added when type assertion is used in arrow function with object literal**

*tsgo incorrectly adds an extra pair of parentheses around object literals when type assertions are used in arrow functions.*

 * created by **dragomirtitian**
 * **jakebailey** added label `Domain: Emit`

### [Issue microsoft/TypeScript-go#2326](https://github.com/microsoft/TypeScript-go/issues/2326) (Closed, **Copilot**)

**JSX emit does not preserve string delimiters**

*tsgo’s JSX emitter always replaces single-quoted attribute values with double quotes, failing to preserve the original delimiters.*

 * created by **dragomirtitian**
 * **jakebailey** assigned to **Copilot**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2326#issuecomment-3638461266) **jakebailey** asked whether the observed fidelity difference mattered for the work or was just noticed in a comparison
 * [today](https://github.com/microsoft/TypeScript-go/issues/2326#issuecomment-3638488356) **dragomirtitian** noted that it was a minor issue, allowed closing, and mentioned it hindered spotting JS differences via text comparison
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2327](https://github.com/microsoft/TypeScript-go/pull/2327) (Closed, **jakebailey**, **Copilot**)

**Fix JSX emit to preserve string delimiters**

*Preserve original single or double quotes when emitting JSX attribute string literals in React.createElement calls.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2328](https://github.com/microsoft/TypeScript-go/issues/2328) (Open)

**Declaration emit with \`\-\-noResolve\` differs from tsc**

*tsgo incorrectly emits ‘any’ for default exports under --noResolve whereas tsc preserves the original types.*

 * created by **jfirebaugh**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2328#issuecomment-3638539421) **jakebailey** pointed out that --noCheck isn't fully supported yet and requires parts of the checker to run before emit
 * [today](https://github.com/microsoft/TypeScript-go/issues/2328#issuecomment-3638542067) **jakebailey** mentioned that --noResolve complicated things and suggested it might be a no node reuse case

### [PR microsoft/TypeScript-go#2329](https://github.com/microsoft/TypeScript-go/pull/2329) (Closed)

**Properly format \`@example\` in quick info**

*Ensure @example tags are properly formatted and displayed in quick info tooltips.*

 * created by **ahejlsberg**
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#2330](https://github.com/microsoft/TypeScript-go/pull/2330) (Closed, **RyanCavanaugh**, **Copilot**)

**Port TypeScript PR \#62844: Gate \`\#/\` subpath imports on NodeNext and Bundler**

*Enable '#/' subpath imports for NodeNext and Bundler modes while preserving Node16 compatibility via a new feature flag.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2330#issuecomment-3639378095) **jakebailey** said "Sad there's no test but it's correct, so"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2330#issuecomment-3639506353) **Copilot** added compiler test cases from the original PR and did not port the requested fourslash test
 * [today](https://github.com/microsoft/TypeScript-go/pull/2330#issuecomment-3639698114) **magic-akari** asked whether combining the error cases into a single test would be better
 * [today](https://github.com/microsoft/TypeScript-go/pull/2330#issuecomment-3639731399) **jakebailey** said "Yeah, it makes separate baselines, so is a pretty good solution to this."

### [PR microsoft/TypeScript-go#2331](https://github.com/microsoft/TypeScript-go/pull/2331) (Open)

**Organize Imports**

*Implement functionality to automatically organize and sort imports within source files.*

 * created by **johnfav03**

### [Issue microsoft/TypeScript-go#2332](https://github.com/microsoft/TypeScript-go/issues/2332) (Closed, `Crash`, **DanielRosenwasser**)

**Crash in JSX tag when spread element is non\-structured type**

*TypeScript language service panics during JSX attribute completions when using a non-structured spread prop*

 * created by **DanielRosenwasser**
 * **DanielRosenwasser** added label `Crash`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2332#issuecomment-3639628899) **DanielRosenwasser** noted that /*number*/ crashes but /*boolean*/ does not because it's a union
 * **DanielRosenwasser** assigned to **DanielRosenwasser**
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#2333](https://github.com/microsoft/TypeScript-go/pull/2333) (Closed)

**Add token flags parameter to token creation functions**

*Implement a token flags parameter in token creation functions, propagate flags as in Strada, and prevent issues like #2326.*

 * created by **gabritto**

### [Issue microsoft/TypeScript-go#2334](https://github.com/microsoft/TypeScript-go/issues/2334) (Open)

**Questionable code lenses for object type members on a single line**

*Suppress code lenses on object type members defined inline when their parent and siblings share the same line.*

 * created by **DanielRosenwasser**

### [PR microsoft/TypeScript-go#2335](https://github.com/microsoft/TypeScript-go/pull/2335) (Closed)

**Fix completions in JSX tag with unstructured spreads**

*Enable accurate code completions within JSX tags that include unstructured spread attributes.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** closed the issue

### [Issue microsoft/TypeScript-go#2336](https://github.com/microsoft/TypeScript-go/issues/2336) (Open, `Crash`, **Copilot**)

**Crash for signature help in arrow function parameters**

*Signature help invoked on arrow function parameters crashes the TypeScript server without a stack trace*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** added label `Crash`, and assigned to **Copilot**

### [PR microsoft/TypeScript-go#2337](https://github.com/microsoft/TypeScript-go/pull/2337) (Open, **DanielRosenwasser**, **Copilot**)

**\[WIP\] Fix crash for signature help in arrow function parameters**

*Fix crash in TypeScript language server when requesting signature help within arrow function parameters*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **DanielRosenwasser**

### [PR microsoft/TypeScript-go#2338](https://github.com/microsoft/TypeScript-go/pull/2338) (Closed)

**Fix unquote**

*Fix the misported regex in the unquote implementation.*

 * created by **gabritto**

### [PR microsoft/TypeScript-go#2339](https://github.com/microsoft/TypeScript-go/pull/2339) (Closed)

**Port many more fourslash functions**

*Port a suite of missing fourslash testing functions for error counting, existence checks at ranges and markers, and content validation.*

 * created by **jakebailey**

### [Issue microsoft/TypeScript-go#2340](https://github.com/microsoft/TypeScript-go/issues/2340) (Open)

**In mono repo, tsgo not picking types from custom packages**

*Tsgo in a monorepo setup fails to resolve and compile types from custom packages.*

 * created by **Hemantvetal**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2340#issuecomment-3640601629) **jakebailey** said "This isn't enough information; do you have a repo you can share?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2340#issuecomment-3640634938) **Hemantvetal** provided minimal reproduction steps for a pnpm-based monorepo TypeScript import error

### [Issue microsoft/TypeScript-go#2341](https://github.com/microsoft/TypeScript-go/issues/2341) (Open)

**Performance regression with \`\-\-incremental\` between \`native\-preview\-0\.20251211\.1\` and \`0\.20251209\.1\`**

*First-run incremental type checking in native-preview-0.20251211.1 is three times slower than in native-preview-0.20251209.1.*

 * created by **gggdomi**

### [PR microsoft/TypeScript-go#2342](https://github.com/microsoft/TypeScript-go/pull/2342) (Open)

**fix: Crash for completions after JSDoc \* on line following string\-named property signature**

*Allow JSDoc comments to include property signatures and other type elements to fix completion crashes after string-named properties*

 * created by **jgsheppa**
 * [later](https://github.com/microsoft/TypeScript-go/pull/2342#issuecomment-3642030501) **jgsheppa** agreed to the Contributor License Agreement using the microsoft-github-policy-service command

### [PR microsoft/TypeScript-go#2343](https://github.com/microsoft/TypeScript-go/pull/2343) (Closed)

**\-\-experimentalDecorators and \-\-emitDecoratorMetadata**

*Implement decorator and metadata emit flags in TypeScript-Go, resolve sourcemap test mismatches, and review pending feature emits.*

 * created by **weswigham**

