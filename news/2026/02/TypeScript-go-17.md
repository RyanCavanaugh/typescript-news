# Report for 2026-02-17 (Tuesday, February 17th, 2026)

9 different users commented on 50 different issues.

## Recommended Actions

 * Response Recommended
    * @kan-o-ash reported that Asana is also affected by this issue in their codebase in [microsoft/TypeScript-go#2648](https://github.com/microsoft/TypeScript-go/issues/2648#issuecomment-3916218533)

## Activity Summary

### [PR microsoft/TypeScript-go#2259](https://github.com/microsoft/TypeScript-go/pull/2259) (Closed, **DanielRosenwasser**, **Copilot**)

**Fix nil pointer dereference in completion at property start after JSDoc**

*Prevent nil pointer dereference in completions at JSDoc-preceded property starts by fixing assignment and adding a nil check.*

 * **Copilot** assigned to **DanielRosenwasser**
 * [10 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2259#issuecomment-3634678530) **DanielRosenwasser** requested the location of the tests and suggested merging from upstream and rerunning `hereby generate`
 * [10 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2259#issuecomment-3634739558) **Copilot** added a test in TestCompletionJSDocBeforePropertyNoCrash for the crash scenario and merged from main with code generation run
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2337](https://github.com/microsoft/TypeScript-go/pull/2337) (Closed, **DanielRosenwasser**, **Copilot**)

**\[WIP\] Fix crash for signature help in arrow function parameters**

*Fix crash in TypeScript language server when requesting signature help within arrow function parameters*

 * created by **Copilot**
 * (9 weeks ago) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2491](https://github.com/microsoft/TypeScript-go/pull/2491) (Closed, **DanielRosenwasser**, **Copilot**)

**Fix nil pointer panic in JSDoc callable type completions**

*Completing JSDoc callable type signatures with parameters causes a nil pointer panic due to missing symbol nil check.*

 * [1 month ago](https://github.com/microsoft/TypeScript-go/pull/2491#issuecomment-3775047626) **Copilot** described exporting GetReparsedNodeForNode and using it in getSignatureFromDeclaration to fix the reparsed parameter node issue
 * [1 month ago](https://github.com/microsoft/TypeScript-go/pull/2491#issuecomment-3775306263) **DanielRosenwasser** said "We think the call to getReparsedNodeForNode should have happened at a "more general" place and not exported from the package. @copilot try to figure something else out."
 * [1 month ago](https://github.com/microsoft/TypeScript-go/pull/2491#issuecomment-3775355912) **Copilot** investigated a non-exported use of getReparsedNodeForNode, identified performance issues during type checking, and applied a minimal nil check fix in commit f000b0e6
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2519](https://github.com/microsoft/TypeScript-go/pull/2519) (Closed, **RyanCavanaugh**, **Copilot**)

**Port TypeScript PR \#60528: Fix crash on index type deferral for generic mapped types with name types**

*Port PR #60528 to simplify index type resolution and prevent crashes for generic mapped types with name types, adding tests.*

 * (1 month ago) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * [1 month ago](https://github.com/microsoft/TypeScript-go/pull/2519#issuecomment-3757187898) **Copilot** added two regression tests from the upstream PR to verify that the type checker didn't crash on complex mapped types
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2577](https://github.com/microsoft/TypeScript-go/pull/2577) (Closed)

**Add \-\-release flag to emulate real released binaries, rename build tag to noassert, test release in CI**

*Add a --release flag to produce stripped binaries, rename the build tag to ‘noassert’, and test release builds in CI.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2577#issuecomment-3793261911) **jakebailey** said they thought the name was funny, couldn't think of a better name, suggested leaving it as release and questioned flipping code in release mode
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2577#issuecomment-3800621851) **jakebailey** said "Thinking more, we should have a --nodebug like --noembed, except that aliases another flag too. So, it's probably a bad build tag name and release was fine. Maybe..."
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/2577#issuecomment-3855769882) **jakebailey** said "Also TODO, going to add a task which actually exercises the release procedure, for CI testing."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2577#issuecomment-3917589117) **DanielRosenwasser** asked where all the build flags are tracked and if they can be toggled ad-hoc
 * [today](https://github.com/microsoft/TypeScript-go/pull/2577#issuecomment-3918157955) **jakebailey** described the behavior of `noembed` and `noassert` build tags across default, debug, and release build modes and noted other test-related flags

### [PR microsoft/TypeScript-go#2601](https://github.com/microsoft/TypeScript-go/pull/2601) (Closed, **DanielRosenwasser**, **Copilot**)

**Display "\(\+N overload\)" suffix for function overloads in hover**

*Hover tooltips for TypeScript functions, methods, and constructors now include a (+N overload) suffix when additional overloads exist.*

 * created by **Copilot**
 * (3 weeks ago) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2648](https://github.com/microsoft/TypeScript-go/issues/2648) (Closed, `Crash`, **andrewbranch**, **iisaduan**, **Copilot**)

**panic handling request textDocument/codeAction: textDocument/codeAction returned ErrNeedsAutoImports even after enabling auto imports**

*TypeScript LSP panics on codeAction requests returning ErrNeedsAutoImports despite auto imports being enabled*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2648#issuecomment-3841032189) **tomredman** removed autoImport excludes to resolve the error and suggested the issue was a duplicate of microsoft/typescript-go#2598
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2648#issuecomment-3842197513) **pattobrien** confirmed that removing autoImport excludes fixed the error and noted that the issue persisted after the PR merge
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2648#issuecomment-3842484579) **andrewbranch** said "@iisaduan looks like #2616 wasn't sufficient ☹️ "
 * [today](https://github.com/microsoft/TypeScript-go/issues/2648#issuecomment-3916218533) **kan-o-ash** said "Asana is running into this in our codebase as well."
 * (today) **andrewbranch** assigned to **andrewbranch**, **iisaduan**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2648#issuecomment-3917113783) **apendua** investigated panic triggered by exclude patterns update and found that registryBuilder.updateIndexes() skipped rebuilding buckets, preventing fileExcludePatterns from updating
 * [today](https://github.com/microsoft/TypeScript-go/issues/2648#issuecomment-3917587268) **pattobrien** noted that the panic was reproducible on one developer's local machine despite others not encountering it
 * **andrewbranch** assigned to **Copilot**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2662](https://github.com/microsoft/TypeScript-go/pull/2662) (Closed, `dependencies`, `javascript`)

**Bump @isaacs/brace\-expansion from 5\.0\.0 to 5\.0\.1**

*Bump @isaacs/brace-expansion dependency from version 5.0.0 to 5.0.1.*

 * (2 weeks ago) **dependabot[bot]** added labels `javascript`, `dependencies`, `javascript`
 * [today](https://github.com/microsoft/TypeScript-go/pull/2662#issuecomment-3917618591) **dependabot[bot]** said "Looks like @isaacs/brace-expansion is no longer a dependency, so this is no longer needed."
 * (today) **dependabot[bot]** closed the issue

### [Issue microsoft/TypeScript-go#2684](https://github.com/microsoft/TypeScript-go/issues/2684) (Closed, `Crash`, **andrewbranch**, **Copilot**)

**nil source file in aliasResolve\.GetSourceFile**

*A nil source file causes a segmentation fault in aliasResolver.GetSourceFile during module resolution.*

 * created by **jakebailey**
 * **jakebailey** added label `Crash`
 * **andrewbranch** assigned to **andrewbranch**
 * **andrewbranch** assigned to **Copilot**

### [PR microsoft/TypeScript-go#2712](https://github.com/microsoft/TypeScript-go/pull/2712) (Closed)

**Replace unsafe\.Pointer for seen symbol tables with unique ID**

*Use existing Node or Symbol IDs plus metadata instead of unsafe.Pointer to optimize symbol table tracking.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2716](https://github.com/microsoft/TypeScript-go/pull/2716) (Closed)

**Implement sync API without NAPI**

*A pure JavaScript synchronous child process API using fs.readSync/writeSync replaces the napi-rs module with comparable performance.*

 * created by **jakebailey**
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/2716#issuecomment-3873671799) **jakebailey** said "Seemingly this does not work on Windows, which hangs. I didn't exactly test there, so, fair."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2728](https://github.com/microsoft/TypeScript-go/pull/2728) (Closed, **jakebailey**, **Copilot**)

**Port TypeScript\#62676: Fix slow sync iteration types spoiling cached async iteration types**

*Prevents sync iteration type resolution from caching before async resolution, ensuring correct for-await loop typing.*

 * **Copilot** assigned to **jakebailey**
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/2728#issuecomment-3881156531) **jakebailey** said "Hm, this does nothing. Maybe we avoid the problem entirely now?"
 * [5 days ago](https://github.com/microsoft/TypeScript-go/pull/2728#issuecomment-3894199035) **jakebailey** suggested pulling a linked PR to fix a potential ordering issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/2728#issuecomment-3917477160) **jakebailey** said "See above; this is type order dependent. I don't think I can effectively come up with something that walks this in just the right order to cause the problem again without a lot of effort..."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2728#issuecomment-3917484716) **DanielRosenwasser** asked for clarification on how the change is union-order dependent and which union it affects
 * [today](https://github.com/microsoft/TypeScript-go/pull/2728#issuecomment-3917559163) **jakebailey** instructed copilot to create a failing test for the Go code prior to the fix by reverting the change locally and to stop if unable to find one
 * [today](https://github.com/microsoft/TypeScript-go/pull/2728#issuecomment-3917611903) **Copilot** explained that they could not find a failing test in the Go code because Go uses a centralized iterationTypesCache with distinct keys preventing stale data, verified that reverting the fix produced identical results, and confirmed the structural change is correct for TypeScript parity
 * [today](https://github.com/microsoft/TypeScript-go/pull/2728#issuecomment-3917719045) **DanielRosenwasser** said "So is there no test diff removal because we haven't updated the submodule? Therefore, there's nothing being tested?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2728#issuecomment-3917722943) **jakebailey** explained that the test existed but had no diff due to caching differences and argued that the code style should match
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2751](https://github.com/microsoft/TypeScript-go/pull/2751) (Closed, **jakebailey**, **Copilot**)

**Port TS\#63043: Implement walkBindingPattern for declaration emit of destructured parameter properties**

*Port PRs 63043 and 63154 to implement walkBindingPattern in Go declaration transform, fixing destructured parameter property crashes and aligning baselines.*

 * (1 week ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * [5 days ago](https://github.com/microsoft/TypeScript-go/pull/2751#issuecomment-3894913105) **jakebailey** said "It's sort of debatable whether or not this is a good behavior or not. This is a type error we somehow still produce a decent declaration file for."
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#2760](https://github.com/microsoft/TypeScript-go/pull/2760) (Closed, **jakebailey**, **Copilot**)

**Error on modules\-as\-namespaces**

*Enforce parsing errors on module namespace declarations, report one error per dotted name, and update code and tests.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/2760#issuecomment-3882864264) **Copilot** updated the parser to emit TS1540 parse errors on each identifier for illegal module namespace declarations and aligned baselines by deleting diff files
 * [6 days ago](https://github.com/microsoft/TypeScript-go/pull/2760#issuecomment-3885570532) **jakebailey** said "I guess this is fine, though I think I was hoping to hard remove it and not even have this diagnostic, as though module foo { were entirely illegal."
 * [6 days ago](https://github.com/microsoft/TypeScript-go/pull/2760#issuecomment-3885934528) **DanielRosenwasser** recommended gracefully parsing and issuing a parse error
 * [today](https://github.com/microsoft/TypeScript-go/pull/2760#issuecomment-3917568878) **jakebailey** said "@copilot this is failing tests, you didn't run the whole suite"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2760#issuecomment-3917636937) **Copilot** fixed the failing tests by updating the test file to use `namespace` instead of `module` to match the submodule version

### [PR microsoft/TypeScript-go#2777](https://github.com/microsoft/TypeScript-go/pull/2777) (Closed)

**Assume alwaysStrict**

*Assume alwaysStrict is true by default, eliminating SourceFileAffectingCompilerOptions and retaining only ExternalModuleIndicatorOptions for AST configuration.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2788](https://github.com/microsoft/TypeScript-go/pull/2788) (Closed)

**Fix function/constructor/enum checks that relied on walking the "first declaration"**

*Extend the fix for concurrent checking failures in controlFlowFunctionLikeCircular1 to other function, constructor, and enum declaration checks.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2797](https://github.com/microsoft/TypeScript-go/issues/2797) (Closed, **ahejlsberg**)

**TS2488: Generic type parameter not inferred from JSX props, falls back to default**

*A tsgo bug prevents inferring a generic JSX component's type parameter from its selector prop, incorrectly triggering TS2488.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2797#issuecomment-3910903910) **theoludwig** noted that the PR altered `[Symbol.iterator]()` behavior, referenced its implementation in TypeScript v6, and suggested it might help
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2797#issuecomment-3910984219) **theoludwig** identified the problematic commit and confirmed that reverting it resolves the errors
 * **jakebailey** assigned to **ahejlsberg**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2801](https://github.com/microsoft/TypeScript-go/pull/2801) (Closed)

**Parse JSDoc lazily in TS files, eliminate JSDocParsingMode**

*Eliminate the JSDocParsingMode setting and defer parsing of JSDoc in TypeScript files until needed to streamline AST caching*

 * created by **jakebailey**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2801#issuecomment-3911746991) **jakebailey** explained that the current implementation hurts check and requested a variant returning only precalculated/eager JSDoc
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2802](https://github.com/microsoft/TypeScript-go/issues/2802) (Closed)

**JSX with generics loses type inference on \`children\` if its a callback**

*A regression in tsgo v7.0.0-dev.20260213.1 breaks type inference for generic JSX components’ callback children props but not for other callbacks.*

 * created by **Gabrola**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2803](https://github.com/microsoft/TypeScript-go/pull/2803) (Closed)

**Fixed JSX context\-sensitive children discrimination for generic signatures**

*Fixes context-sensitive children discrimination in JSX generic signatures to address two related typescript-go issues.*

 * created by **Andarist**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2804](https://github.com/microsoft/TypeScript-go/pull/2804) (Closed)

**Fix panic in organizeImports for \.d\.ts files with unused imports matching module augmentations**

*OrganizeImports crashes on .d.ts files with unused imports matching module augmentations.*

 * created by **Andarist**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2805](https://github.com/microsoft/TypeScript-go/pull/2805) (Closed)

**Fix crash in import statement completions**

*Resolve crash occurring during import statement completions in the TypeScript-Go integration.*

 * created by **Andarist**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2805#issuecomment-3916865299) **Andarist** clarified that the link worked for them and posted the gitroomhq/postiz-app crash stack trace
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#2806](https://github.com/microsoft/TypeScript-go/pull/2806) (Closed)

**Update dependencies**

*Update project dependencies to resolve npm audit issues and integrate Go 1.26 golangci-lint and json/v2 updates*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2807](https://github.com/microsoft/TypeScript-go/pull/2807) (Closed, **jakebailey**, **Copilot**)

**Port TS\#61534: correct source location when react\-jsx and whitespace before jsx**

*Skip leading whitespace trivia when computing JSX source locations in react-jsxdev to correct column numbers matching TypeScript output.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2808](https://github.com/microsoft/TypeScript-go/pull/2808) (Closed, **jakebailey**, **Copilot**)

**Port ES2025 ScriptTargetFeatures and fix ES2025 transformer mapping**

*Ports missing ES2025 ScriptTargetFeatures entries and fixes the ES2025 transformer mapping to apply correct downlevel transforms*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#2809](https://github.com/microsoft/TypeScript-go/pull/2809) (Closed, **jakebailey**, **Copilot**)

**Port proposal\-upsert methods to getScriptTargetFeatures**

*Add esnext proposal-upsert methods to Map and WeakMap, remove invalid ES2015 iterable properties, and pass tests.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2809#issuecomment-3917512893) **DanielRosenwasser** said "https://github.com/microsoft/TypeScript/pull/62612"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2810](https://github.com/microsoft/TypeScript-go/pull/2810) (Closed, **jakebailey**, **Copilot**)

**Port PR \#62628: Add Date\.toTemporalInstant to getScriptTargetFeatures**

*Add Date.toTemporalInstant entry to getFeatureMap in getScriptTargetFeatures to enable correct target library diagnostics*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2810#issuecomment-3917551271) **DanielRosenwasser** said "https://github.com/microsoft/TypeScript/pull/62628"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2811](https://github.com/microsoft/TypeScript-go/pull/2811) (Closed)

**Fixed completion crash on JSDoc nodes created by \`reparseJSDocComment\`**

*Resolves a code completion crash occurring on JSDoc nodes created by reparseJSDocComment.*

 * created by **Andarist**
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#2812](https://github.com/microsoft/TypeScript-go/pull/2812) (Closed, **andrewbranch**, **Copilot**)

**Fix ErrNeedsAutoImports panic when autoImportFileExcludePatterns changes**

*Include fileExcludePatterns in updateIndexes rebuild checks to ensure autoimport buckets refresh and prevent ErrNeedsAutoImports panics.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2812#issuecomment-3918432650) **andrewbranch** said "This is a stopgap before we remove support for this preference being able to differ between TS and JS, but it is a valid correction to the way it was set up to work now."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2813](https://github.com/microsoft/TypeScript-go/pull/2813) (Closed)

**New IPC API client features**

*Updates the TypeScript IPC API client to use immutable snapshots for state and lifecycle management and adds Go support code.*

 * created by **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2813#issuecomment-3918014132) **andrewbranch** said "My handling of SourceFileAffectingOptions needs to be updated after Jake's changes in main. I think it wasn't quite right before, anyway."

### [PR microsoft/TypeScript-go#2814](https://github.com/microsoft/TypeScript-go/pull/2814) (Closed, **andrewbranch**, **Copilot**)

**Fix nil pointer dereference in aliasResolver\.GetSourceFile**

*aliasResolver.GetSourceFile crashes when host.GetSourceFile returns nil due to symlink path mismatches in the auto-import cache*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2814#issuecomment-3918724221) **Copilot** rejected the race explanation and documented the file existence caching, symlink path mismatch theory, and nil-unsafe binder fix in commit 720f0d6b

### [Issue microsoft/TypeScript-go#2815](https://github.com/microsoft/TypeScript-go/issues/2815) (Closed, `bug`, `Crash`, **DanielRosenwasser**, **Copilot**)

**Panic in signatureHelp for contextual signature help on methods/function expressions**

*Requesting contextual signature help on a constructor method expression triggers an index out of range panic.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** added labels `bug`, `Crash`, and assigned to **Copilot**, **DanielRosenwasser**

### [PR microsoft/TypeScript-go#2816](https://github.com/microsoft/TypeScript-go/pull/2816) (Closed, **DanielRosenwasser**, **Copilot**)

**Fix panic in signature help for contextual signatures with only construct signatures**

*Use a length check to prevent index out of range panics in signature help when only construct signatures exist.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **DanielRosenwasser**

### [PR microsoft/TypeScript-go#2817](https://github.com/microsoft/TypeScript-go/pull/2817) (Open, **jakebailey**, **Copilot**)

**Port TypeScript PR \#62338: Deprecate \-\-moduleResolution node10**

*Deprecate node10 moduleResolution in the Go codebase by removing it, adding require-pattern utilities, and updating tests.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#2818](https://github.com/microsoft/TypeScript-go/pull/2818) (Open, **jakebailey**, **Copilot**)

**Port TS PR \#62669: Deprecate \-\-module amd, umd, system, none; \-\-moduleResolution classic**

*Port deprecation of amd, umd, system, and none module options and classic module resolution removal diagnostic to the Go port.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#2819](https://github.com/microsoft/TypeScript-go/pull/2819) (Open, **jakebailey**, **Copilot**)

**Port TS PR \#62418: Add diagnostic when rootDir inference changes output layout**

*Add TS5011 diagnostic in Go compiler when inferred rootDir layout differs from computed common source directory.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#2820](https://github.com/microsoft/TypeScript-go/pull/2820) (Open, **jakebailey**, **Copilot**)

**Port TypeScript\#63071: Mark downlevelIteration as removed**

*In the Go port of TypeScript, mark the downlevelIteration compiler option as removed by emitting a removed-option diagnostic, skipping related tests, and deleting obsolete baselines.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#2821](https://github.com/microsoft/TypeScript-go/pull/2821) (Closed)

**Remove redundant JSDoc flag checks**

*Remove redundant flag checks in JSDoc and EagerJSDoc since both already perform this check and return nil.*

 * created by **jakebailey**

### [Issue microsoft/TypeScript-go#2822](https://github.com/microsoft/TypeScript-go/issues/2822) (Open, `Domain: Editor`, **andrewbranch**)

**Harden LSP against requests for files that don't have open projects**

*Enhance the LSP to gracefully handle requests for files not in open projects to avoid errors.*

 * created by **andrewbranch**
 * (today) **andrewbranch** added label `Domain: Editor`, and assigned to **andrewbranch**

