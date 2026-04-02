# Report for 2026-03-19 (Thursday, March 19th, 2026)

13 different users commented on 32 different issues.

## Recommended Actions

 * Response Recommended
    * @vetptzru asked if more information was needed or if the provided information was sufficient in [microsoft/TypeScript-go#3139](https://github.com/microsoft/TypeScript-go/issues/3139#issuecomment-4096913604)

## Activity Summary

### [Issue microsoft/TypeScript-go#1498](https://github.com/microsoft/TypeScript-go/issues/1498) (Closed, `Domain: Editor`, **jakebailey**, **Copilot**)

**\[lsp\] Typescript generics type error**

*TypeScript LSP plugin lacks generic type completions and inference suggestions for Array<> similar to the existing TS plugin.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/1498#issuecomment-4088114756) **jakebailey** noted that trigger characters were not set correctly and provided a link and code snippet
 * (yesterday) **jakebailey** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2445](https://github.com/microsoft/TypeScript-go/issues/2445) (Closed, `bug`, **andrewbranch**, **Copilot**)

**resolvePackageJsonExports false ignored in tsgo, works in v5\.9 and v6**

*tsgo ignores resolvePackageJsonExports:false causing incorrect import paths in generated d.ts files, unlike TypeScript 5.9 and 6 preview*

 * (10 weeks ago) **RyanCavanaugh** added label `bug`, and assigned to **andrewbranch**
 * **andrewbranch** assigned to **Copilot**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#2459](https://github.com/microsoft/TypeScript-go/pull/2459) (Closed)

**Port \-\-isolatedDeclarations related node builder logic, with baseline updates**

*Port node builder logic for the --isolatedDeclarations option and apply baseline updates for review.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2459#issuecomment-4085847334) **weswigham** suggested that unparsedTests.txt contents might depend on file inode ordering, noting regenerated file differed only in line order from main
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2459#issuecomment-4086013319) **jakebailey** mentioned that unparsedTests.txt ordering varied due to inode ordering and suggested adding a sort in the script
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2459#issuecomment-4086041403) **gabritto** suggested adding a sort to the script
 * [today](https://github.com/microsoft/TypeScript-go/pull/2459#issuecomment-4093041808) **jakebailey** identified the missing error in isolatedDeclarationErrorsExpressions.errors.txt.diff as the only remaining potential problem and noted other issues were minor
 * [today](https://github.com/microsoft/TypeScript-go/pull/2459#issuecomment-4093042956) **jakebailey** said "Well, that and, updating baselines again, it seems."

### [Issue microsoft/TypeScript-go#2661](https://github.com/microsoft/TypeScript-go/issues/2661) (Closed, `Domain: Editor`, **andrewbranch**, **Copilot**)

**auto\-import adds inline type modifier to existing import type statement**

*Auto-import incorrectly adds inline type modifiers to named imports in an import type statement, causing a TS2206 error.*

 * **andrewbranch** assigned to **andrewbranch**
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2661#issuecomment-3995729836) **tats-u** said "Bumped into this. This is a regression from Strada, as the description suggests. It does not occur while "TypeScript Native Preview: Disable"'d."
 * **andrewbranch** assigned to **Copilot**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#2944](https://github.com/microsoft/TypeScript-go/pull/2944) (Open)

**\[draft\] more formatting tests **

*Add draft formatting tests to validate and troubleshoot the repository’s testing pipelines.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2944#issuecomment-4001359480) **typescript-bot** reported that the top100 tests failed to queue due to validation errors or warnings
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/2944#issuecomment-4027129395) **iisaduan** said "@typescript-bot test top100"
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/2944#issuecomment-4027129682) **typescript-bot** reported that the test top100 job failed to queue due to validation errors or warnings
 * [today](https://github.com/microsoft/TypeScript-go/pull/2944#issuecomment-4093375627) **typescript-bot** said "@@iisaduan, the perf run you requested failed. You can check the log here."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2944#issuecomment-4093891403) **typescript-bot** said "@iisaduan, the perf run you requested failed. You can check the log here."

### [PR microsoft/TypeScript-go#2978](https://github.com/microsoft/TypeScript-go/pull/2978) (Closed, **andrewbranch**, **Copilot**)

**Fix auto\-import type modifier and formatting issues in type\-only import statements**

*Fix inline type modifiers, formatting, indentation, token handling, and import ordering in type-only import statements.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/2978#issuecomment-4049824447) **andrewbranch** said "I wasn't ready yet!"
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2978#issuecomment-4087562964) **jakebailey** said "bad main merge?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2978#issuecomment-4090944486) **andrewbranch** said "new test in main asserting incorrect formatting (intended just to assert no crash)"
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#3139](https://github.com/microsoft/TypeScript-go/issues/3139) (Open, `Needs More Info`)

**runtime: failed to create new OS thread**

*Running tsgo on a large macFUSE-mounted TypeScript project exhausts OS threads and crashes the Go runtime.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3139#issuecomment-4085354173) **DanielRosenwasser** said "I guess on that note, do you see any differences if you pass a flag like --singleThreaded? And how are you building it today? Are you passing something like --watch?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/3139#issuecomment-4089048689) **vetptzru** described that running with the --singleThreaded flag prevented crashes, mentioned currently building with that flag in VS Code and asked how to pass it there, and stated that they were not using --watch
 * [today](https://github.com/microsoft/TypeScript-go/issues/3139#issuecomment-4089083039) **vetptzru** provided screenshots showing the peak thread count the tsgo process reached before crashing
 * [later](https://github.com/microsoft/TypeScript-go/issues/3139#issuecomment-4096913604) **vetptzru** said "@DanielRosenwasser do you need any more information from me, or is this enough?"

### [PR microsoft/TypeScript-go#3145](https://github.com/microsoft/TypeScript-go/pull/3145) (Closed)

**Refactor debug package to be inlinable, always enabled**

*Refactor Go debug package to always enable inlined debug asserts by eliminating reflect, interface indirection, and un-inlinable tests.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3145#issuecomment-4092317917) **jakebailey** said "I'm refactoring this package even more, down to just having Assert as a boolean taking function. And, just deleting nodebug now."

### [PR microsoft/TypeScript-go#3152](https://github.com/microsoft/TypeScript-go/pull/3152) (Closed)

**Defer diagnostics in order to fix flaky test**

*Defer diagnostics during type resolution to avoid circularity errors and stabilize the flaky for-of29.ts test.*

 * created by **ahejlsberg**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3152#issuecomment-4085530742) **ahejlsberg** noted that the callback passed to someSymbolTableInScope from getWithAlternativeContainers iterated a map, causing random choice when multiple matches existed
 * [today](https://github.com/microsoft/TypeScript-go/pull/3152#issuecomment-4090861496) **ahejlsberg** said "With latest commit we save deferred diagnostics only when doing a full type check. Also, the logic for initiating unused identifier checks now ensures that the check happens only once."
 * [today](https://github.com/microsoft/TypeScript-go/pull/3152#issuecomment-4091750543) **ahejlsberg** clarified that the reintroduction aimed at correctness rather than saving work
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#3155](https://github.com/microsoft/TypeScript-go/pull/3155) (Closed, **andrewbranch**, **Copilot**)

**Fix \`resolvePackageJsonExports: false\` being ignored in module specifier generation**

*Fix module specifier generation to respect resolvePackageJsonExports:false by changing the guard in tryDirectoryWithPackageJson.*

 * created by **Copilot**
 * (yesterday) **Copilot** assigned to **Copilot**, **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#3156](https://github.com/microsoft/TypeScript-go/pull/3156) (Closed)

**Update \`module: "none"\` cross project references test**

*Revise the module:none cross-project references test to add explicit project references following deprecation of file merging behavior*

 * created by **gabritto**
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript-go#3158](https://github.com/microsoft/TypeScript-go/pull/3158) (Closed)

**Stop suggesting @strict in copilot instructions**

*Copilot instructions should no longer suggest @strict as it’s outdated and spams regular pull requests.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3159](https://github.com/microsoft/TypeScript-go/pull/3159) (Open, **jakebailey**, **Copilot**)

**Fix format selection deleting comments when selection ends inside comment trivia**

*Formatting a code selection that ends inside a block comment removes the comment entirely.*

 * created by **Copilot**
 * (yesterday) **Copilot** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3159#issuecomment-4092429944) **jakebailey** said "@copilot+claude-opus-4.6 you must not have run the tests. you broke formatSelectionEditAtEndOfRange_test"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3159#issuecomment-4092680089) **Copilot** fixed broken formatSelectionEditAtEndOfRange_test by capping previousRangeTriviaEnd before comment trivia in consumeTokenAndAdvanceScanner and verified tests pass

### [PR microsoft/TypeScript-go#3160](https://github.com/microsoft/TypeScript-go/pull/3160) (Closed, **jakebailey**, **Copilot**)

**Add \`\<\` trigger and \`\)\` retrigger characters for signature help**

*Include '<' as a signature help trigger and ')' as a retrigger character to match VS Code's TypeScript extension*

 * created by **Copilot**
 * (yesterday) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3161](https://github.com/microsoft/TypeScript-go/pull/3161) (Open, **jakebailey**, **Copilot**)

**Fix documentation inheritance for static method overrides on mixin intersection types**

*Overridden static methods on mixin intersection classes lose inherited documentation due to incomplete base type resolution of static members*

 * created by **Copilot**
 * (yesterday) **Copilot** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3161#issuecomment-4092774358) **jakebailey** said "@copilot+claude-opus-4.6 address feedback"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3161#issuecomment-4092865304) **Copilot** addressed feedback by replacing getAllSuperTypeNodes with ast.GetClassExtendsHeritageElement and adding foundInBase tracking to avoid unnecessary work

### [PR microsoft/TypeScript-go#3162](https://github.com/microsoft/TypeScript-go/pull/3162) (Closed)

**Organize imports comment duplication**

*OrganizeImports source action duplicated comments above export statements, resulting in repeated comment blocks.*

 * created by **johnfav03**
 * [later](https://github.com/microsoft/TypeScript-go/pull/3162#issuecomment-4099037027) **bradleyayers** clarified that the problem was with exports rather than imports

### [PR microsoft/TypeScript-go#3163](https://github.com/microsoft/TypeScript-go/pull/3163) (Closed)

**Support implicit jsx and tslib imports in find all refs**

*Enable find-all-references to support implicit JSX and tslib imports from program-level storage with cancellation support.*

 * created by **gabritto**
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript-go#3164](https://github.com/microsoft/TypeScript-go/pull/3164) (Closed)

**Fix misport in \`getMeaningFromLocation\`**

*Fix incorrect import in getMeaningFromLocation that leads to wrong semantic meaning assignments.*

 * created by **gabritto**
 * (today) **gabritto** closed the issue

### [Issue microsoft/TypeScript-go#3165](https://github.com/microsoft/TypeScript-go/issues/3165) (Closed, **DanielRosenwasser**)

**Crash when importing JSON file with multiple top\-level values**

*The TypeScript compiler crashes when importing a JSON module with multiple top-level values.*

 * created by **DanielRosenwasser**
 * **DanielRosenwasser** assigned to **DanielRosenwasser**
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#3166](https://github.com/microsoft/TypeScript-go/pull/3166) (Closed)

**Set synthesized array literal's parent in malformed JSON files**

*Set the parent of synthesized array literals created for multiple top-level expressions in malformed JSON files.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#3167](https://github.com/microsoft/TypeScript-go/pull/3167) (Open)

**Fix: skip CommonJS export binding when module or exports is a local variable**

*Skips binding CommonJS exports when module or exports is locally defined to avoid shadowing ESM exports and spurious diagnostics.*

 * created by **Muhammad-Bin-Ali**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3167#issuecomment-4093018437) **Muhammad-Bin-Ali** said "@microsoft-github-policy-service agree"

### [PR microsoft/TypeScript-go#3168](https://github.com/microsoft/TypeScript-go/pull/3168) (Closed)

**Add all\-checks task to hereby**

*Add an all-checks task to hereby to run lint and tests together while excluding API-package and generate checks*

 * created by **gabritto**

### [PR microsoft/TypeScript-go#3169](https://github.com/microsoft/TypeScript-go/pull/3169) (Closed)

**Submodule accept some find all refs diffs**

*Accept most Strada find-all-references baseline diffs caused by context ranges, with exceptions for parser and filename bugs.*

 * created by **gabritto**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3169#issuecomment-4093597590) **jakebailey** said "I trust you  😄 "
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript-go#3170](https://github.com/microsoft/TypeScript-go/pull/3170) (Closed)

**fix: nil pointer deref when accessing module exports in name resolver**

*Optional chaining for Symbol is missing in Corsa's name resolver, causing nil pointer dereferences when accessing module exports*

 * created by **camc314**

### [PR microsoft/TypeScript-go#3171](https://github.com/microsoft/TypeScript-go/pull/3171) (Open, **ahejlsberg**, **RyanCavanaugh**, **Copilot**)

**Fix stack overflow in relater's skipCaching path for recursive tuple types**

*Add depth counters to prevent unbounded recursion and stack overflow in the relater skipCaching path for recursive tuple types.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * **RyanCavanaugh** assigned to **ahejlsberg**
 * [later](https://github.com/microsoft/TypeScript-go/pull/3171#issuecomment-4099158802) **RyanCavanaugh** said "@ahejlsberg this seems like two fixes when only one is needed, but I'm not sure which is preferable (or maybe there's a third option)"

### [PR microsoft/TypeScript-go#3172](https://github.com/microsoft/TypeScript-go/pull/3172) (Open, **RyanCavanaugh**, **Copilot**)

**Fix stack overflow in instantiateTypeWorker with recursive intersections \(TypeScript\#63269\)**

*Enforce the recursion depth limit in instantiateTypeWorker by setting instantiationCount high to avoid stack overflows in recursive intersections.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**

### [Issue microsoft/TypeScript-go#3173](https://github.com/microsoft/TypeScript-go/issues/3173) (Open, `Domain: Editor`)

**When two imports have the same url, updates always apply to the first one\.**

*Auto-import merges additions into the first identical-module import statement instead of updating the appropriate type or value import.*

 * created by **xyhxx**
 * **xyhxx** added label `Domain: Editor`

### [Issue microsoft/TypeScript-go#3174](https://github.com/microsoft/TypeScript-go/issues/3174) (Closed, `enhancement`, **andrewbranch**)

**ThrottleGorup Semaphore ussage**

*Refactor the ThrottleGroup implementation to use errgroup.SetLimit instead of a custom semaphore for concurrency control.*

 * created by **code-ghoost**

### [PR microsoft/TypeScript-go#3175](https://github.com/microsoft/TypeScript-go/pull/3175) (Open, **ahejlsberg**, **RyanCavanaugh**, **Copilot**)

**Fix template literal type exponential blowup in addSpans**

*Add growth limits in addSpans to prevent exponential template literal type expansion causing memory exhaustion.*

 * created by **Copilot**
 * (later) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * **RyanCavanaugh** assigned to **ahejlsberg**

