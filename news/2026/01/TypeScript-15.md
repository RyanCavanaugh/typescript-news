# Report for 2026-01-15 (Thursday, January 15th, 2026)

16 different users commented on 24 different issues.

## Recommended Actions

 * Response Recommended
    * @nh2 asked whether the issue was solved and what the fix was in [microsoft/TypeScript#46420](https://github.com/microsoft/TypeScript/issues/46420#issuecomment-3760229956)
    * @uli-a asked whether the ancestor directory loop should stop at the top level of the workspace or network share root in [microsoft/TypeScript#62960](https://github.com/microsoft/TypeScript/issues/62960#issuecomment-3756234243)
    * @uli-a asked whether searching outside the workspace could be made configurable in [microsoft/TypeScript#62960](https://github.com/microsoft/TypeScript/issues/62960#issuecomment-3757316720)
    * @nmain provided a simplified repro with a Playground link in [microsoft/TypeScript#62995](https://github.com/microsoft/TypeScript/issues/62995#issuecomment-3760579093)

## Activity Summary

### [Issue microsoft/TypeScript#46420](https://github.com/microsoft/TypeScript/issues/46420) (Closed, `Needs More Info`, `Needs Investigation`, `Domain: Performance`)

**Slow performance in incremental mode with no changes**

*TypeScript's incremental mode still re-parses every file on unchanged runs, causing slow type-check performance in large projects.*

 * [4.1 years ago](https://github.com/microsoft/TypeScript/issues/46420#issuecomment-972215380) **JelleZijlstra** reported that disabling incremental and tsBuildInfoFile yielded the trace and revealed that findSourceFile remained slow and type checking consumed significant time
 * [4.1 years ago](https://github.com/microsoft/TypeScript/issues/46420#issuecomment-978209865) **samuliasmala** described experiencing the same issue with the incremental flag and provided reproduction steps and timing measurements
 * (1.4 years ago) **RyanCavanaugh** closed the issue
 * [later](https://github.com/microsoft/TypeScript/issues/46420#issuecomment-3760229956) **nh2** said "@RyanCavanaugh Was this solved? What was the fix?"

### [Issue microsoft/TypeScript#56239](https://github.com/microsoft/TypeScript/issues/56239) (Closed, `Domain: Mapped Types`, `Possible Improvement`)

**\`keyof FilteringMappedType\` can't compute its constraint**

*Using a mapped type with an ‘as’ clause causes keyof to produce a string|number|symbol union, violating the string-only constraint on ProvidedActor.src.*

 * [48 weeks ago](https://github.com/microsoft/TypeScript/issues/56239#issuecomment-2649348758) **Andarist** explained that the case worked as expected, clarified that GetRecord’s constraint only required Record<PropertyKey, any>, and noted that Key is not guaranteed to be assignable to string
 * [48 weeks ago](https://github.com/microsoft/TypeScript/issues/56239#issuecomment-2649600427) **StreetStrider** confirmed that Record creates an open type and that Record<number, any> extends Record<string, any> evaluates to true because objects can be indexed by both
 * **RyanCavanaugh** added label `Domain: Mapped Types`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#60476](https://github.com/microsoft/TypeScript/issues/60476) (Closed, `Bug`, `Help Wanted`, `Domain: check: Type Circularity`)

**Regression: Mapped type with recursive key remapping crashes tsc with "RangeError: Maximum call stack size exceeded" in TS@5\.4\+**

*A recursive mapped type for flattening nested object keys now crashes the TypeScript 5.4+ compiler with a call stack overflow.*

 * (1.1 years ago) **RyanCavanaugh** added labels `Help Wanted`, `Domain: Type Circularity`, and set milestone to `Backlog`
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#60528](https://github.com/microsoft/TypeScript/pull/60528) (Closed, `For Backlog Bug`)

**Fixed crash related to index type deferral on generic mapped types with name types**

*Fixed a compiler crash when deferring index types in generic mapped types that use name types.*

 * [1.1 years ago](https://github.com/microsoft/TypeScript/pull/60528#issuecomment-2497354754) **typescript-bot** reported that the user tests with tsc comparing main and the PR merge looked good
 * [1.1 years ago](https://github.com/microsoft/TypeScript/pull/60528#issuecomment-2497404106) **typescript-bot** notified that the requested performance run results were available with a detailed comparison report
 * [1.1 years ago](https://github.com/microsoft/TypeScript/pull/60528#issuecomment-2497652634) **typescript-bot** provided results of running the top 400 repos with tsc comparing main and the pull request and reported that everything looked good
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#62194](https://github.com/microsoft/TypeScript/issues/62194) (Closed, `Suggestion`, `Breaking Change`, `Committed`, `Fix Available`, **sheetalkamat**)

**Assume \`rootDir\` is the current configuration directory**

*TypeScript will default rootDir to the tsconfig.json directory instead of inferring it from files, speeding builds and simplifying file resolution.*

 * **typescript-bot** added label `Fix Available`
 * [16 weeks ago](https://github.com/microsoft/TypeScript/issues/62194#issuecomment-3335267813) **DanielRosenwasser** noted that in projects with tsconfig.json outside the main source directory, omitting rootDir causes TypeScript to include the src folder in the output directory
 * [7 weeks ago](https://github.com/microsoft/TypeScript/issues/62194#issuecomment-3572397173) **DanielRosenwasser** explained that they decided to error when the inferred source root and tsconfig directory differ, requiring users to specify `rootDir` explicitly
 * (today) **sheetalkamat** closed the issue

### [Issue microsoft/TypeScript#62887](https://github.com/microsoft/TypeScript/issues/62887) (Closed, `Needs Investigation`, **sheetalkamat**)

**TS Server Crash Loop: Copilot Chat virtual files \('vscode\-chat\-code\-block'\) trigger infinite Directory Watcher recursion on InferredProject**

*Copilot Chat’s virtual “vscode-chat-code-block” files cause the TypeScript server to enter infinite directory watcher recursion, spike CPU, and crash repeatedly.*

 * **RyanCavanaugh** added label `Needs Investigation`
 * [1 month ago](https://github.com/microsoft/TypeScript/issues/62887#issuecomment-3649495289) **code-forge-temple** identified the bug's introduction around mid-May 2025 and recommended reviewing changes from that period; criticized Microsoft for ignoring critical bugs and expressed intent to cancel Copilot subscription due to corporate priorities
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/62887#issuecomment-3739775406) **cleversonferreira** asked about when the PR with the bug fix would be published
 * (today) **sheetalkamat** closed the issue

### [PR microsoft/TypeScript#62894](https://github.com/microsoft/TypeScript/pull/62894) (Closed, `Author: Team`, `For Uncommitted Bug`, **sheetalkamat**)

**Handle resolution watching when its dynamic scriptInfo**

*Stop watching failed lookup paths, inferred typeRoots, and typing installer locations for dynamic scripts using unwatchable or default directories.*

 * (1 month ago) **typescript-bot** added labels `Author: Team`, `For Uncommitted Bug`
 * [1 month ago](https://github.com/microsoft/TypeScript/pull/62894#issuecomment-3656739718) **jakebailey** asked what constituted a dynamic script and whether custom file extensions would be affected, and whether the fix should be backported to 5.9 given the 6.0 timeline
 * [today](https://github.com/microsoft/TypeScript/pull/62894#issuecomment-3756419053) **sheetalkamat** clarified that dynamic scripts referred to unsaved files and linked the relevant code
 * [today](https://github.com/microsoft/TypeScript/pull/62894#issuecomment-3756442720) **jakebailey** said "@typescript-bot cherry-pick this to release-5.9"
 * [today](https://github.com/microsoft/TypeScript/pull/62894#issuecomment-3756443043) **typescript-bot** started jobs and updated build statuses for the 'cherry-pick this to release-5.9' command
 * (today) **sheetalkamat** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/62894#issuecomment-3756517481) **typescript-bot** said "Hey, @jakebailey! I've created #62990 for you. This involved updating baselines; please check the diff."
 * [today](https://github.com/microsoft/TypeScript/pull/62894#issuecomment-3756530078) **jakebailey** reran CI and requested the bot to cherry-pick to release-5.9
 * [today](https://github.com/microsoft/TypeScript/pull/62894#issuecomment-3756530296) **typescript-bot** reported starting CI jobs for cherry-pick to release-5.9 with status and result links
 * [today](https://github.com/microsoft/TypeScript/pull/62894#issuecomment-3756580844) **typescript-bot** said "Hey, @jakebailey! I've updated #62990 for you. This involved updating baselines; please check the diff."

### [Issue microsoft/TypeScript#62960](https://github.com/microsoft/TypeScript/issues/62960) (Open, `Needs More Info`)

**Initializing tsconfig\.json hangs**

*VS Code hangs indefinitely initializing tsconfig.json for Vue projects on network shares, disabling IntelliSense and error reporting.*

 * [1 week ago](https://github.com/microsoft/TypeScript/issues/62960#issuecomment-3720924568) **uli-a** tried changing the watch configuration but observed no improvement; described the network and hardware environment and ruled out performance issues; asked how to determine what tsserver is doing or waiting for
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/62960#issuecomment-3740668755) **RyanCavanaugh** noted that there is no way to inspect what tsserver is doing or waiting for without attaching a debugger
 * **RyanCavanaugh** added label `Needs More Info`
 * [today](https://github.com/microsoft/TypeScript/issues/62960#issuecomment-3756234243) **uli-a** described debugging the forEachAncestorDirectory function and asked if the loop should stop at the workspace or network share root to avoid slow traversal
 * [today](https://github.com/microsoft/TypeScript/issues/62960#issuecomment-3757316720) **uli-a** revealed that directoryProbablyExists in loadModuleFromImmediateNodeModulesDirectory was slow, questioned whether always searching outside the workspace should be configurable, and noted a workaround using an empty network share

### [Issue microsoft/TypeScript#62967](https://github.com/microsoft/TypeScript/issues/62967) (Open, `Suggestion`, `Help Wanted`, `Experience Enhancement`)

**JSDoc comments for async\_hooks are confusing/misleading**

*JSDoc comments in the async_hooks module misleadingly discourage its use while recommending AsyncLocalStorage, causing confusion in TypeScript.*

 * (2 days ago) **RyanCavanaugh** added labels `Help Wanted`, `Experience Enhancement`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/62967#issuecomment-3757602066) **pranamya123** said "Hi @a-non-a-mouse  I’ve opened a PR in DefinitelyTyped to clarify the async_hooks JSDoc warning so it doesn’t read as discouraging the module while recommending AsyncLocalStorage from the same import."

### [Issue microsoft/TypeScript#62972](https://github.com/microsoft/TypeScript/issues/62972) (Closed, `Not a Defect`)

**\`errorType\` does not propagate with non\-distributive conditional types**

*Non-distributive conditional types in TypeScript fail to propagate errorType, unlike distributive conditional types.*

 * [3 days ago](https://github.com/microsoft/TypeScript/issues/62972#issuecomment-3737630505) **Andarist** clarified that eagerly reducing those constructs would degrade the in-IDE experience and compared { prop: ErrorType } to ErrorType
 * **RyanCavanaugh** added label `Not a Defect`
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/62972#issuecomment-3746022448) **RyanCavanaugh** clarified that the reported behavior should never occur and that no guarantees are made beyond the first line
 * [today](https://github.com/microsoft/TypeScript/issues/62972#issuecomment-3757681174) **typescript-bot** said "This issue has been marked as "Not a Defect" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-bot** closed the issue

### [Issue microsoft/TypeScript#62975](https://github.com/microsoft/TypeScript/issues/62975) (Closed, `Working as Intended`)

**SkipLibCheck isn't working on erasableSyntaxCheck**

*SkipLibCheck fails to suppress errors in external index.d.ts files defining enums and namespaces under erasableSyntaxCheck*

 * [3 days ago](https://github.com/microsoft/TypeScript/issues/62975#issuecomment-3740368499) **RyanCavanaugh** said "Lib-ness is not transitive; the check is based only on filename. This package is misconfigured."
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/62975#issuecomment-3740376562) **wparad** said "Can you point us to some reference docs that explain what the configuration is supposed to be?"
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/62975#issuecomment-3741298292) **RyanCavanaugh** noted that PR #67 contains the correct fix and referenced documentation on publishing declaration files to npm
 * [today](https://github.com/microsoft/TypeScript/issues/62975#issuecomment-3757681246) **typescript-bot** said "This issue has been marked as "Working as Intended" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-bot** closed the issue

### [Issue microsoft/TypeScript#62976](https://github.com/microsoft/TypeScript/issues/62976) (Closed, `Duplicate`)

**Nested Branded type does not error**

*TypeScript fails to enforce branded type distinctions in nested Records, allowing incompatible nested branded types to be assigned without error.*

 * created by **nitzcard**
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/62976#issuecomment-3739117679) **jcalz** said "Duplicate of or related to #43852 "
 * **RyanCavanaugh** added label `Duplicate`
 * [today](https://github.com/microsoft/TypeScript/issues/62976#issuecomment-3757681108) **typescript-bot** said "This issue has been marked as "Duplicate" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-bot** closed the issue

### [Issue microsoft/TypeScript#62977](https://github.com/microsoft/TypeScript/issues/62977) (Closed, `Suggestion`, `Out of Scope`)

**\`disallowClassExpressions\`**

*Add a TypeScript compiler option to disallow class expressions for stricter type checking and error prevention.*

 * **RyanCavanaugh** added label `Out of Scope`
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/62977#issuecomment-3740274634) **valler** thanked the reviewer and noted that although the compiler option won’t solve all issues, the language still improved user experience and may help avoid design limitations
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/62977#issuecomment-3740450411) **valler** observed that the option, being scoped to expressions, wouldn't affect declarations in closures and thus was less useful than initially expected
 * [today](https://github.com/microsoft/TypeScript/issues/62977#issuecomment-3757681330) **typescript-bot** said "This issue has been marked as "Out of Scope" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-bot** closed the issue

### [Issue microsoft/TypeScript#62988](https://github.com/microsoft/TypeScript/issues/62988) (Open, `Suggestion`, `Awaiting More Feedback`, `Domain: Performance`)

**Use LazyBarrel to improve IDE performance**

*Add an experimental LazyBarrel optimization to the TypeScript Language Server to improve IDE performance with barrel files*

 * created by **mgfalzon**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/62988#issuecomment-3753100806) **DanielRosenwasser** explained that full-program loading is necessary for builds and language service features, described optimizations for v7.0, and expressed willingness to consider future enhancements
 * [today](https://github.com/microsoft/TypeScript/issues/62988#issuecomment-3755403191) **mgfalzon** thanked the maintainer and reported that de-barreling led to 27% and 30% reductions in type highlight duration at Atlassian, and said they will de-barrel their component library after migrating to tsgo
 * (today) **RyanCavanaugh** added labels `Suggestion`, `Awaiting More Feedback`, `Domain: Performance`

### [PR microsoft/TypeScript#62989](https://github.com/microsoft/TypeScript/pull/62989) (Closed, `Author: Team`, `For Uncommitted Bug`, **DanielRosenwasser**)

**Prepare tests for \`\-\-noImplicitAny\`**

*A script prepends // @strict: false to tests whose error outputs changed when enabling default --noImplicitAny.*

 * (yesterday) **typescript-bot** added labels `Author: Team`, `For Uncommitted Bug`
 * [yesterday](https://github.com/microsoft/TypeScript/pull/62989#issuecomment-3753134272) **DanielRosenwasser** said "This history is already a nightmare..."
 * [today](https://github.com/microsoft/TypeScript/pull/62989#issuecomment-3756883789) **jakebailey** said "On one hand, I feel bad locking so many tests into a mode we basically don't want anyone using, but on the other, that is what they were testing before, so, there's not much difference...."
 * [today](https://github.com/microsoft/TypeScript/pull/62989#issuecomment-3757078321) **DanielRosenwasser** described wanting to annotate error baselines to explain why they’re off and noted that forward migration might not happen

### [PR microsoft/TypeScript#62990](https://github.com/microsoft/TypeScript/pull/62990) (Open, `For Uncommitted Bug`, **DanielRosenwasser**)

**🤖 Pick PR \#62894 \(Handle resolution watching when its\.\.\.\) into release\-5\.9**

*Cherry-pick PR #62894 into release-5.9 to handle resolution watching and update baselines for review.*

 * created by **typescript-bot**
 * (today) **typescript-bot** added label `For Uncommitted Bug`, and assigned to **DanielRosenwasser**

### [Issue microsoft/TypeScript#62991](https://github.com/microsoft/TypeScript/issues/62991) (Open, `Bug`, `Domain: Parser`)

**Not currectly parse superClass starts with \`{}\`**

*Expressions beginning with {} such as {}.Foo and {}! are not correctly parsed as class superclasses.*

 * created by **fisker**
 * [today](https://github.com/microsoft/TypeScript/issues/62991#issuecomment-3758129886) **MartinJohns** said "Is this real and useful code or just code trying to break the compiler?"
 * [today](https://github.com/microsoft/TypeScript/issues/62991#issuecomment-3758248210) **fisker** stated that the code was not real or useful and noted it was found in the Prettier test suite

### [Issue microsoft/TypeScript#62992](https://github.com/microsoft/TypeScript/issues/62992) (Open, `Suggestion`, `Awaiting More Feedback`)

**generics in constructor**

*Add support for generic type parameters on class constructors to enforce parameter type constraints.*

 * created by **y-nk**
 * [later](https://github.com/microsoft/TypeScript/issues/62992#issuecomment-3760042724) **jcalz** inquired about the type of instances of a class with a generic constructor parameter and questioned if the issue duplicated earlier tickets

### [Issue microsoft/TypeScript#62993](https://github.com/microsoft/TypeScript/issues/62993) (Open, `Bug`, `Help Wanted`, `Fix Available`, `Domain: Crashes`, **RyanCavanaugh**, **Copilot**)

**Crash: RangeError: Maximum call stack size exceeded in addTypesToUnion when using incomplete keyof type annotation on object destructuring**

*Compiler crashes with a RangeError in addTypesToUnion when destructuring an object with an incomplete keyof annotation under strict mode*

 * created by **na7ure-a**
 * [later](https://github.com/microsoft/TypeScript/issues/62993#issuecomment-3759331169) **Andarist** provided a shorter repro snippet

### [Issue microsoft/TypeScript#62994](https://github.com/microsoft/TypeScript/issues/62994) (Closed, `Duplicate`)

**Typescript Playground Set interval Bug**

*Repeatedly executing setInterval code in the TypeScript Playground fails to clear previous intervals unless the page is reloaded*

 * created by **IamStaple**
 * [later](https://github.com/microsoft/TypeScript/issues/62994#issuecomment-3760010266) **MartinJohns** suggested using the TypeScript-Website repo and explained that the playground is intended only for quick snippets rather than a fresh environment
 * [later](https://github.com/microsoft/TypeScript/issues/62994#issuecomment-3760349874) **MartinJohns** said "Duplicate of https://github.com/microsoft/TypeScript-Website/issues/2541."

### [Issue microsoft/TypeScript#62995](https://github.com/microsoft/TypeScript/issues/62995) (Closed, `Fixed`)

**Bug with type argument inference if it has default value \`= undefined\` and actual value is object with non\-arrow function**

*TypeScript incorrectly infers generic type arguments defaulting to undefined when given an inline object with non-arrow functions.*

 * created by **termi**
 * [later](https://github.com/microsoft/TypeScript/issues/62995#issuecomment-3760579093) **nmain** simplified the reproduction case and provided a playground link
 * [later](https://github.com/microsoft/TypeScript/issues/62995#issuecomment-3760618285) **MartinJohns** said "Likely a duplicate of #47599."
 * [later](https://github.com/microsoft/TypeScript/issues/62995#issuecomment-3760689845) **termi** explained that their example uses three generic parameters to demonstrate the necessity of the D=undefined default and contrasted it with a simpler case where the default can be removed
 * [later](https://github.com/microsoft/TypeScript/issues/62995#issuecomment-3760706496) **termi** clarified that the issue was related to #47599 but not a duplicate and noted that adding '=undefined' in a generic parameter caused a problem

