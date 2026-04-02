# Report for 2026-02-06 (Friday, February 6th, 2026)

12 different users commented on 22 different issues.

## Recommended Actions

 * Response Recommended
    * @mabels provided a link that might help answer the question in [microsoft/TypeScript-go#2699](https://github.com/microsoft/TypeScript-go/issues/2699#issuecomment-3861930896)
    * @mabels provided build logs and file listings demonstrating the issue in [microsoft/TypeScript-go#2699](https://github.com/microsoft/TypeScript-go/issues/2699#issuecomment-3861987821)
    * @chriskrycho provided additional exploration results regarding canReuseTypeNode() behavior in [microsoft/TypeScript-go#2701](https://github.com/microsoft/TypeScript-go/issues/2701#issuecomment-3861931441)
    * @chriskrycho confirmed the fix and reported a ~95% performance improvement in [microsoft/TypeScript-go#2701](https://github.com/microsoft/TypeScript-go/issues/2701#issuecomment-3863092956)

## Activity Summary

### [PR microsoft/TypeScript-go#2620](https://github.com/microsoft/TypeScript-go/pull/2620) (Closed)

**Bring back async API, allow API connection to LSP process**

*Reintroduce a decoupled async JSON-RPC API client and server in the LSP to enable external extensions to query TypeScript state.*

 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/2620#issuecomment-3843140487) **gabritto** explained that the API requires explicit cleanup of symbols and types across remote calls, provided a using-syntax example, and asked what happens to returned objects when the project changes
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/2620#issuecomment-3843551857) **andrewbranch** explained that the client controlled when to adopt the latest LSP session snapshot, allowing it to retain older objects indefinitely and reuse source files and symbols, and postponed implementing automatic purging for simplicity
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/2620#issuecomment-3850390977) **andrewbranch** asked what version of tinybench was installed, noted v3.1.1 lacked that many lines, and mentioned that Jake changed it in main
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#2630](https://github.com/microsoft/TypeScript-go/issues/2630) (Closed, `Domain: Editor`, **andrewbranch**)

**Multiple Language Client instances persist after TSDK switch**

*Switching to the TypeScript native-preview SDK in VS Code leaves duplicate language client instances, showing the previous fix was incomplete.*

 * created by **rubenferreira97**
 * **rubenferreira97** added label `Domain: Editor`
 * **andrewbranch** assigned to **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#2655](https://github.com/microsoft/TypeScript-go/issues/2655) (Open, `wontfix`)

**Incorrect type error when assigning to an index in a \`{}\[\]\`\-typed field where the index is any\-typed and field is defined in a base class in a JS file**

*tsgo wrongly reports type errors when assigning to an any-indexed element of a {}[] field in a JS base class.*

 * created by **peetklecha**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2655#issuecomment-3861558989) **ahejlsberg** explained that the error was intended, clarifying that the {} in the inferred {}[] type represented the internal anyFunctionType wildcard, described tsgo's stricter subtype rules, and noted that a recent PR would cause the example to error in TS 6.0 with inferred (() => void)[], aligning tsgo behavior
 * **ahejlsberg** added label `wontfix`

### [PR microsoft/TypeScript-go#2680](https://github.com/microsoft/TypeScript-go/pull/2680) (Closed, **andrewbranch**, **Copilot**)

**Fix module resolver bug exposed by malformed package\.json import patterns**

*Fix module resolver bug that crashed the language server with malformed package.json wildcard import patterns*

 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/2680#issuecomment-3849529032) **andrewbranch** pointed out that the panic was correct in the first if block and shouldn't be changed, noted a misleading panic message in the second block, and suggested fixing it in the module resolver
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/2680#issuecomment-3849562676) **Copilot** explained that the panic exposed a module resolver bug where the TS extension flag was set from the package.json pattern instead of the original module specifier and noted its fix in commit 90aa27c0
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/2680#issuecomment-3849602497) **Copilot** restored both panics and explained that the first was correct and the second is now a valid assertion after the module resolver fix
 * [today](https://github.com/microsoft/TypeScript-go/pull/2680#issuecomment-3862596709) **andrewbranch** said "@copilot tests failed"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2680#issuecomment-3862627198) **Copilot** fixed test failures by adding missing reference baselines
 * [today](https://github.com/microsoft/TypeScript-go/pull/2680#issuecomment-3863080260) **Copilot** explained that all tests now passed after adding missing baselines

### [Issue microsoft/TypeScript-go#2686](https://github.com/microsoft/TypeScript-go/issues/2686) (Open, `Domain: Editor`, **andrewbranch**)

**Packages \`pnpm link\`ed from outside the workspace trigger no watch events when changed**

*Linked external packages don’t trigger watch events on changes, preventing diagnostic updates until the server restarts.*

 * created by **andrewbranch**
 * **andrewbranch** added label `Domain: Editor`
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/2686#issuecomment-3850202915) **sheetalkamat** described how Strada watched `node_modules/package` for links and otherwise `node_modules` for failed lookups and linked the relevant pull request
 * **andrewbranch** assigned to **andrewbranch**

### [Issue microsoft/TypeScript-go#2690](https://github.com/microsoft/TypeScript-go/issues/2690) (Closed, `Crash`, **andrewbranch**)

**Panic \- inlayHint \- bad line number \- from autofix/auto\-formatting setup**

*The language server panics during inlayHint requests because an autofix formatting change produces an out-of-range line number.*

 * [today](https://github.com/microsoft/TypeScript-go/issues/2690#issuecomment-3859284870) **gggdomi** concurred that they started seeing the same error today on macOS while using eslint and prettier
 * [today](https://github.com/microsoft/TypeScript-go/issues/2690#issuecomment-3860622182) **lukpsaxo** reproduced the issue consistently on longer files but not on smaller ones and said they would create a standalone repro
 * [today](https://github.com/microsoft/TypeScript-go/issues/2690#issuecomment-3860791698) **lukpsaxo** described making a standalone repo and that the error occurred only once under rapid edits, linking the repo and noting larger repos fail more often
 * [today](https://github.com/microsoft/TypeScript-go/issues/2690#issuecomment-3863002996) **andrewbranch** said "@lukpsaxo that's a 404 for me. Is it a private repo?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2690#issuecomment-3863780432) **lukpsaxo** said "Sorry, made it public now."

### [Issue microsoft/TypeScript-go#2697](https://github.com/microsoft/TypeScript-go/issues/2697) (Closed, `Crash`, `Needs More Info`, **ahejlsberg**)

**Crash compiling TypeScript tests**

*Typescript-Go checker panics with index out-of-range error in TupleNormalizer.normalize during TypeScript test compilation*

 * created by **andrewbranch**
 * **andrewbranch** added label `Crash`
 * **ahejlsberg** assigned to **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2697#issuecomment-3861208874) **ahejlsberg** observed that the repro steps produced a TS18003 error indicating no inputs were found in tsconfig.all.json
 * **ahejlsberg** added label `Needs More Info`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2697#issuecomment-3861613785) **andrewbranch** said "@ahejlsberg sorry, I meant do that in the microsoft/TypeScript repo 😄 "

### [Issue microsoft/TypeScript-go#2699](https://github.com/microsoft/TypeScript-go/issues/2699) (Open)

**tsgo resolves inherited include/exclude globs differently than tsc when using extends**

*tsgo resolves inherited include globs relative to the child config rather than the parent, causing a different output structure than tsc.*

 * created by **mabels**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2699#issuecomment-3861216354) **jakebailey** explained that includes/excludes/files aren’t inherited, described rootDir inference change due to PRs, suggested setting rootDir to ./app to fix and noted a repro is needed for config interplay
 * [today](https://github.com/microsoft/TypeScript-go/issues/2699#issuecomment-3861265168) **jakebailey** said "(though I don't know where "app" is in your example; this is why a repro we can test is helpful)"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2699#issuecomment-3861930896) **mabels** noted that there was no app in a specific directory and suggested a link to the large app repository
 * [today](https://github.com/microsoft/TypeScript-go/issues/2699#issuecomment-3861948071) **jakebailey** provided a link to the repro directory, suggested setting rootDir to "../../", and noted that includes are not inherited
 * [today](https://github.com/microsoft/TypeScript-go/issues/2699#issuecomment-3861987821) **mabels** ran builds with tsc and tsgo and demonstrated that tsgo scattered .js and .js.map files throughout the monorepo

### [Issue microsoft/TypeScript-go#2700](https://github.com/microsoft/TypeScript-go/issues/2700) (Closed)

**\`"module": "nodenext"\` no longer infers \`"target": "esnext"\` in v7\.0\.0\-dev\.20260206\.1**

*In v7.0.0-dev.20260206.1, specifying module: nodenext no longer implicitly targets ESNext, causing Set.difference to be unrecognized.*

 * created by **abrahamguo**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2700#issuecomment-3861177485) **jakebailey** explained that the target no longer depended on module to avoid a cycle and that ES2025 will become the default in a later update to include those types again
 * [today](https://github.com/microsoft/TypeScript-go/issues/2700#issuecomment-3861275681) **jakebailey** said "(Your issue says you tested 6.0, but this should have also happened there this week.)"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2700#issuecomment-3861776755) **abrahamguo** said "Ah, I must have unintentionally tested against 5.9 rather than 6. Thanks for clarifying!"
 * (today) **abrahamguo** closed the issue

### [Issue microsoft/TypeScript-go#2701](https://github.com/microsoft/TypeScript-go/issues/2701) (Open)

**Declaration emit for named inferred types used in further inference inlines inferred types instead of naming them**

*tsgo inlines inferred types in declaration emit even when named, causing slower type checking in consuming packages.*

 * created by **chriskrycho**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2701#issuecomment-3861931441) **chriskrycho** provided additional exploration showing that patching canReuseTypeNode() in Strada to always return false inlined types instead of reusing references
 * [today](https://github.com/microsoft/TypeScript-go/issues/2701#issuecomment-3861992981) **jakebailey** said "I would expect this to be fixed by #1693 / #2459, then."
 * [today](https://github.com/microsoft/TypeScript-go/issues/2701#issuecomment-3863092956) **chriskrycho** confirmed that the change fixes the issue and reduces type-check time by ~95% (from ~469s to ~24s)

### [PR microsoft/TypeScript-go#2702](https://github.com/microsoft/TypeScript-go/pull/2702) (Closed)

**Fix race when copying lazy computed values for updateProgram**

*Fix race condition when updateProgram copies lazily computed values.*

 * created by **sheetalkamat**

### [Issue microsoft/TypeScript-go#2703](https://github.com/microsoft/TypeScript-go/issues/2703) (Closed, `bug`, `Domain: JSX`, **ahejlsberg**)

**JSX render prop children incorrectly intersects with \`{}\`**

*ts-go erroneously intersects JSX render prop children with {} leading to assignment errors absent in TypeScript 6.0.*

 * created by **karmeleon**

### [PR microsoft/TypeScript-go#2704](https://github.com/microsoft/TypeScript-go/pull/2704) (Closed)

**Allow invalid UTF\-8**

*Update JSON marshalling to accept invalid UTF-8 so internal symbol prefixes no longer cause crashes.*

 * created by **gabritto**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2704#issuecomment-3862508414) **sheetalkamat** updated branch with pre-leave tests, referenced the tsc test for incremental checks, and suggested updating the baseline sanitizer to support symbol IDs in names

### [Issue microsoft/TypeScript-go#2705](https://github.com/microsoft/TypeScript-go/issues/2705) (Closed, **andrewbranch**, **Copilot**)

**Missing error for overload signature visibility disagreement**

*tsgo fails to report an error for mixed private and public constructor overload signatures that TypeScript 6.0 correctly flags*

 * created by **andrewbranch**
 * (today) **andrewbranch** assigned to **Copilot**, **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#2706](https://github.com/microsoft/TypeScript-go/pull/2706) (Closed, **andrewbranch**, **Copilot**)

**Fix missing TS2385 error for constructor overload visibility disagreement**

*Implements a fallback in checker.go to report TS2385 errors for mismatched constructor overload visibility modifiers*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2706#issuecomment-3862994355) **andrewbranch** said "@copilot delete the new test and baselines because it looks like an existing submodule test was fixed."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2706#issuecomment-3863008380) **Copilot** deleted the new test case and baselines and included only the code change with the corrected submodule baseline
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#2707](https://github.com/microsoft/TypeScript-go/pull/2707) (Closed)

**Update NOTICE for go\-winio**

*Update go-winio NOTICE file to include dependencies and correct JSON and xxhash entries misidentified by the NOTICE tool*

 * created by **jakebailey**

### [Issue microsoft/TypeScript-go#2708](https://github.com/microsoft/TypeScript-go/issues/2708) (Open, **jakebailey**, **Copilot**)

**tsgo emits files next to source instead of outDir when include references parent directories via \.\./**

*tsgo emits files from parent-directory includes next to their sources instead of respecting the configured outDir.*

 * created by **Cellule**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2708#issuecomment-3863666446) **jakebailey** said "Can you please compare against the 6.0 nightly instead of 5.9?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2708#issuecomment-3863669710) **jakebailey** said "(I was assuming it was rootDir, but it probably isn't)"

