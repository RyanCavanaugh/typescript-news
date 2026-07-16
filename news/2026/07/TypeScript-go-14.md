# Report for 2026-07-14 (Tuesday, July 14th, 2026)

18 different users commented on 32 different issues.

## Recommended Actions

 * Response Recommended
    * @zaesur asked if missing refactoring suggestions was due to a configuration problem in [microsoft/TypeScript-go#3580](https://github.com/microsoft/TypeScript-go/issues/3580#issuecomment-4979518813)
    * @philiplindberg reported that the issue reproduces on TypeScript 7.0.2 GA as well in [microsoft/TypeScript-go#4635](https://github.com/microsoft/TypeScript-go/issues/4635#issuecomment-4971925016)
    * @joaquinjulca26 provided repro steps as requested in [microsoft/TypeScript-go#4644](https://github.com/microsoft/TypeScript-go/pull/4644#issuecomment-4975473912)
    * @tomquist provided reproduction steps and test results confirming the issue in [microsoft/TypeScript-go#4647](https://github.com/microsoft/TypeScript-go/issues/4647#issuecomment-4980864285)

## Activity Summary

### [Issue microsoft/TypeScript-go#3580](https://github.com/microsoft/TypeScript-go/issues/3580) (Closed, `Domain: Editor`)

**No code actions available when attempting to use refactorings in VS Code with new typescript\-go preview**

*TypeScript Native Preview's refactoring context menu fails to show in VS Code, displaying “No code actions available”.*

 * **jpierson-at-riis** added label `Domain: Editor`
 * [11 weeks ago](https://github.com/microsoft/TypeScript-go/issues/3580#issuecomment-4313762911) **jakebailey** said "#2227 "
 * (11 weeks ago) **jakebailey** closed the issue
 * [later](https://github.com/microsoft/TypeScript-go/issues/3580#issuecomment-4979518813) **zaesur** asked if the lack of refactoring suggestions and 'No code actions available' messages was due to a configuration problem

### [PR microsoft/TypeScript-go#4274](https://github.com/microsoft/TypeScript-go/pull/4274) (Open, **ahejlsberg**)

**Fix CFA stack overflow crash in for loops where initializer throws**

*Add an early bailout in for-loop binding to avoid stack overflow when the initializer throws*

 * **RyanCavanaugh** added to milestone `Post-7.0`
 * (5 days ago) **ibesuperv** closed the issue
 * [4 days ago](https://github.com/microsoft/TypeScript-go/pull/4274#issuecomment-4935124288) **ibesuperv** explained that they accidentally synced and force-pushed their fork’s main branch, which closed the PR, and opened a new improved PR addressing previous review feedback
 * (today) **ibesuperv** reopened the issue

### [PR microsoft/TypeScript-go#4280](https://github.com/microsoft/TypeScript-go/pull/4280) (Closed, `possible improvement`)

**VS enhanced hover support**

*Restores Visual Studio enhanced hover support by attaching raw classification tokens and icon metadata to LSP hover responses when VSSupportsVisualStudioExtensions is enabled.*

 * created by **navya9singh**
 * **navya9singh** added label `possible improvement`
 * [today](https://github.com/microsoft/TypeScript-go/pull/4280#issuecomment-4972289924) **navya9singh** said "Addressing these comments with a better implementation in https://github.com/microsoft/typescript-go/pull/4625"
 * (today) **navya9singh** closed the issue

### [PR microsoft/TypeScript-go#4582](https://github.com/microsoft/TypeScript-go/pull/4582) (Open)

**Call IsDirCoveredByWatch less often to improve performance**

*Improve tsc --watch performance by reducing redundant IsDirCoveredByWatch calls and optimizing directory caching*

 * created by **terite**
 * [4 days ago](https://github.com/microsoft/TypeScript-go/pull/4582#issuecomment-4936667616) **AkisArou** tested the PR with tsgo --build --watch in a large monorepo and observed that watches were not installed after five minutes; prepared a proof-of-concept branch adding an indexed DirectorySet and updating orchestrator.go to use the index, which made watch initialization immediate
 * [4 days ago](https://github.com/microsoft/TypeScript-go/pull/4582#issuecomment-4937051430) **terite** clarified that the PR only affected the tsgo --watch code path and explained reasons for not modifying the --build code path due to its prototype status and personal lack of usage
 * [today](https://github.com/microsoft/TypeScript-go/pull/4582#issuecomment-4975044627) **terite** said "@microsoft-github-policy-service agree"

### [Issue microsoft/TypeScript-go#4608](https://github.com/microsoft/TypeScript-go/issues/4608) (Open, `Needs More Info`)

**Identical resolved program produces 157 vs 662,155 diagnostics depending on whether the tsconfig is passed directly or through a pass\-through extends**

*Using a pass-through tsconfig that simply extends the main config results in drastically more TypeScript diagnostics than direct config usage.*

 * created by **michaeldanish**
 * **RyanCavanaugh** added label `Needs More Info`
 * [later](https://github.com/microsoft/TypeScript-go/issues/4608#issuecomment-4982366337) **RyanCavanaugh** suggested using the repro reduction skill and linked to the TypeScript Maintainer Skills repository

### [Issue microsoft/TypeScript-go#4619](https://github.com/microsoft/TypeScript-go/issues/4619) (Open, `possible improvement`, **andrewbranch**)

**Improve API performance when using virtual file system**

*Include inline file content and precomputed directory listings in updateSnapshot to eliminate virtual file system IPC calls and improve performance.*

 * created by **dragomirtitian**
 * (later) **RyanCavanaugh** added label `possible improvement`, and assigned to **andrewbranch**

### [Issue microsoft/TypeScript-go#4620](https://github.com/microsoft/TypeScript-go/issues/4620) (Open, `Needs Investigation`, **jakebailey**)

**tsc is not resposive to \`ctrl\-c\`**

*tsc fails to respond to ctrl-c due to incomplete propagation of signal handlers in typescript-go*

 * created by **lukesandberg**
 * (later) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **jakebailey**

### [Issue microsoft/TypeScript-go#4629](https://github.com/microsoft/TypeScript-go/issues/4629) (Closed, `Crash`, **weswigham**)

**panic: Unknown parent for parameter: KindArrowFunction**

*typescript-go crashes with panic 'Unknown parent for parameter: KindArrowFunction' during declaration transformation.*

 * created by **tido64**
 * **tido64** added label `Crash`
 * [today](https://github.com/microsoft/TypeScript-go/issues/4629#issuecomment-4973928142) **RyanCavanaugh** provided a minimal repro example with JS and TS code
 * [later](https://github.com/microsoft/TypeScript-go/issues/4629#issuecomment-4978918590) **tido64** confirmed that the example was a minimal repro and noted that inlining the type prevented the panic
 * **RyanCavanaugh** assigned to **weswigham**

### [Issue microsoft/TypeScript-go#4630](https://github.com/microsoft/TypeScript-go/issues/4630) (Open, `Needs More Info`)

**"Type instantiation is excessively deep and possibly infinite" error with tsgo in v7**

*Typechecking with tsgo and TypeScript v7.0.2 intermittently fails with excessive stack depth and infinite type instantiation errors, unlike v6.0.*

 * created by **justinsmid**
 * **RyanCavanaugh** added label `Needs More Info`
 * [later](https://github.com/microsoft/TypeScript-go/issues/4630#issuecomment-4982461122) **RyanCavanaugh** suggested attaching a debugger and inspecting the call stack, noted TypeScript lacks source file positioning at the error frame, and recommended using the TypeScript-Maintainer-Skills repro reduction tool to provide a reproduction

### [Issue microsoft/TypeScript-go#4631](https://github.com/microsoft/TypeScript-go/issues/4631) (Closed, `Working As Intended`)

**Error TS2590 after migration to Typescript 7\.**

*Migrating a React MUI project to TypeScript 7 causes TS2590 due to excessively complex union types*

 * created by **aleks-elkin**
 * [later](https://github.com/microsoft/TypeScript-go/issues/4631#issuecomment-4981780700) **ahejlsberg** explained that a bug in TS6 caused the issue due to skipLibCheck logic, that it was fixed in TS7, and suggested disabling skipLibCheck to reproduce the error in TS6
 * **ahejlsberg** added label `Working As Intended`

### [PR microsoft/TypeScript-go#4634](https://github.com/microsoft/TypeScript-go/pull/4634) (Closed)

**Fix markLinkedReferences visiting a couple types of otherwise unchecked nodes**

*Update markLinkedReferences to filter unhinted entrypoints like the checker’s forward pass to skip unchecked nodes.*

 * created by **weswigham**
 * (today) **weswigham** closed the issue

### [Issue microsoft/TypeScript-go#4635](https://github.com/microsoft/TypeScript-go/issues/4635) (Open, `bug`)

**Semantic tokens: defaultLibrary modifier never set on case\-insensitive filesystems \(macOS/Windows\)**

*TypeScript Native Preview extension on macOS/Windows case-insensitive filesystems omits defaultLibrary semantic token modifier for library globals causing incorrect theming*

 * created by **philiplindberg**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4635#issuecomment-4971925016) **philiplindberg** clarified that the issue reproduced identically on the released typescript@7.0.2 GA with zero tokens in both preview and GA binaries

### [PR microsoft/TypeScript-go#4636](https://github.com/microsoft/TypeScript-go/pull/4636) (Closed)

**Fix emit mistakenly marking enums used in their own emit as used for unused refs errors**

*Prevent the emit process from mistakenly treating self-referencing enums as used, thereby avoiding false unused reference errors.*

 * created by **weswigham**

### [PR microsoft/TypeScript-go#4637](https://github.com/microsoft/TypeScript-go/pull/4637) (Closed)

**Skip project recheck for no\-op file watch events**

*Skip unnecessary program rechecks and diagnostic refresh storms by only invalidating type-check state when watched files actually change.*

 * created by **johnfav03**

### [PR microsoft/TypeScript-go#4638](https://github.com/microsoft/TypeScript-go/pull/4638) (Open)

**fix\(declarations\): prevent panic for KindArrowFunction parameter visibility**

*Prevent panics by adding KindArrowFunction and KindFunctionExpression to parameter visibility diagnostics.*

 * created by **kimyeongrae23**

### [PR microsoft/TypeScript-go#4639](https://github.com/microsoft/TypeScript-go/pull/4639) (Closed)

**Make JSX missing module error span be issued at a stable location**

*Adjust JSX missing module error spans to consistently point at the file’s first tag for stable diagnostics.*

 * created by **weswigham**

### [PR microsoft/TypeScript-go#4640](https://github.com/microsoft/TypeScript-go/pull/4640) (Closed)

**Always accumulate deferred diagnostics**

*Ensure deferred diagnostics are always accumulated to fix dropped and bogus circularity errors and add caching for getTypeOfExpression*

 * created by **weswigham**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4640#issuecomment-4974242890) **jakebailey** said "Yeah I thought this was very intentionally introduced into this codebase"

### [PR microsoft/TypeScript-go#4641](https://github.com/microsoft/TypeScript-go/pull/4641) (Closed)

**Fix computed name error emit reusing the name expression cache**

*Use a separate resolved type cache for computed property names to ensure proper error emission.*

 * created by **weswigham**

### [PR microsoft/TypeScript-go#4642](https://github.com/microsoft/TypeScript-go/pull/4642) (Closed)

**Add \`runWithTemporaryFileUpdate\` to API**

*Add runWithTemporaryFileUpdate method to the API to enable single-file speculative edits on snapshots, supporting the Strada use case.*

 * created by **gabritto**

### [PR microsoft/TypeScript-go#4643](https://github.com/microsoft/TypeScript-go/pull/4643) (Closed)

**\[api\] Use super\(length\) to avoid RemoteNodeArray array subclass deopt**

*Use super(length) in RemoteNodeArray to avoid array subclass deoptimization, boosting materialization benchmarks by ~30%.*

 * created by **andrewbranch**
 * (later) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#4644](https://github.com/microsoft/TypeScript-go/pull/4644) (Closed)

**fix: include static private identifier properties in matching**

*Removed an early continue in relater.go to include static private identifier properties in getUnmatchedPropertiesWorker matching, fixing privateNamesAndStaticFields behavior*

 * created by **joaquinjulca26**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4644#issuecomment-4975473912) **joaquinjulca26** listed testing commands

### [PR microsoft/TypeScript-go#4645](https://github.com/microsoft/TypeScript-go/pull/4645) (Closed)

**Fix compiler panic on arrow function visibility diagnostics \(Fixes \#4629\)**

*Add early guard for arrow functions and fallback for anonymous declarations to prevent compiler panics during visibility diagnostics*

 * created by **islamfahmy**
 * [later](https://github.com/microsoft/TypeScript-go/pull/4645#issuecomment-4978580316) **islamfahmy** said "@microsoft-github-policy-service agree"

### [PR microsoft/TypeScript-go#4646](https://github.com/microsoft/TypeScript-go/pull/4646) (Open)

**Fix hover documentation for intersected properties**

*Enhance TypeScript hover tooltips for intersection properties by aggregating JSDoc from all declarations.*

 * created by **cuishuang**
 * [later](https://github.com/microsoft/TypeScript-go/pull/4646#issuecomment-4979689386) **Andarist** said "this issue is already being fixed by my older PR: https://github.com/microsoft/typescript-go/pull/3663"

### [Issue microsoft/TypeScript-go#4647](https://github.com/microsoft/TypeScript-go/issues/4647) (Open, `Type Ordering`)

**Root file order causes tsgo to miss recursive conditional type assignability error**

*Reordering root files causes tsgo to miss recursive conditional type assignability errors.*

 * created by **tomquist**
 * [later](https://github.com/microsoft/TypeScript-go/issues/4647#issuecomment-4980029614) **jakebailey** said "You should also check 6.0 with --stableTypeOrdering"
 * [later](https://github.com/microsoft/TypeScript-go/issues/4647#issuecomment-4980864285) **tomquist** reported that reversing the compilation root file order prevented the TS2322 error and that tsgo succeeded in both orders, confirming the root-order-dependent difference under stable type ordering

