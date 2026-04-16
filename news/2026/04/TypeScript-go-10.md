# Report for 2026-04-10 (Friday, April 10th, 2026)

9 different users commented on 38 different issues.

## Recommended Actions

 * Response Recommended
    * @ekazakov14 provided reproduction details and version info in [microsoft/TypeScript-go#3120](https://github.com/microsoft/TypeScript-go/issues/3120#issuecomment-4229269618)

## Activity Summary

### [Issue microsoft/TypeScript-go#2147](https://github.com/microsoft/TypeScript-go/issues/2147) (Closed, `Domain: Module Resolution`, `Domain: Program`, **RyanCavanaugh**, **Copilot**)

**VSCode extension does not appear to work with typeRoots**

*The TSGo extension ignores typeRoots configuration in a monorepo-like layout, preventing proper type resolution.*

 * **jakebailey** added label `Domain: Program`
 * (1 week ago) **RyanCavanaugh** assigned to **Copilot**, **RyanCavanaugh**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2188](https://github.com/microsoft/TypeScript-go/issues/2188) (Closed, `Domain: Editor`, **jakebailey**, **Copilot**)

**Mixins Overrides Drop Documentation**

*TypeScript fails to inherit JSDoc comments when a mixin-derived class overrides a static method.*

 * (18 weeks ago) **jakebailey** added label `Domain: Editor`, and assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2201](https://github.com/microsoft/TypeScript-go/issues/2201) (Closed, `Domain: Editor`, **Copilot**)

**Bad formatting of multiline ternary expression**

*Formatting multiline ternary expressions with tabs results in inconsistent mixing of tabs and spaces.*

 * **mjbvz** added label `Crash`
 * **jakebailey** assigned to **Copilot**
 * [7 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2201#issuecomment-3929174370) **antichris** described additional misalignment issues in formatting of arrow functions and ternary expressions with leading and trailing commas, providing code examples of incorrect indentation
 * [today](https://github.com/microsoft/TypeScript-go/issues/2201#issuecomment-4226498434) **DanielRosenwasser** said "I think all of these should be fixed."
 * (today) **DanielRosenwasser** closed the issue
 * (today) **DanielRosenwasser** added label `Domain: Editor`, and removed label `Crash`

### [Issue microsoft/TypeScript-go#2780](https://github.com/microsoft/TypeScript-go/issues/2780) (Open, `Domain: Editor`, `Needs More Info`, **andrewbranch**)

**High memory consumption in a large pnpm monorepo**

*PR #2502 causes minor edits in a large pnpm monorepo to spike the TypeScript extension memory from ~700MB to ~35GB.*

 * [1 month ago](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-4047475814) **dbrxnds** said "Update: Unfortunately I just seemed to have gotten last time when I said things improved. These past 2 days have been the same as before."
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-4158120316) **ozyx** reported experiencing a massive memory leak in a large pnpm monorepo when using tsgo and offered to gather debug info
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-4205839648) **xenokratos** reported experiencing the same issue on a large monorepo and attached a screenshot
 * [today](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-4228201267) **shinichy** explained why Strada language service didn’t exhibit the issue, implemented the same NodeResolutionFeaturesExports check in Corsa with code and tsconfig updates, and observed reduced memory usage before offering to submit a PR

### [Issue microsoft/TypeScript-go#3120](https://github.com/microsoft/TypeScript-go/issues/3120) (Closed, `Crash`, **iisaduan**)

**thread exhaustion \- program exceeds 10000\-thread limit \- one off error**

*An unreproducible Go runtime crash arises when the program exceeds the 10000-thread limit.*

 * created by **lukpsaxo**
 * **lukpsaxo** added label `Crash`
 * **RyanCavanaugh** assigned to **iisaduan**
 * [later](https://github.com/microsoft/TypeScript-go/issues/3120#issuecomment-4229269618) **ekazakov14** reported experiencing the same intermittent error in CI/CD with a large project and provided their tsgo version

### [PR microsoft/TypeScript-go#3161](https://github.com/microsoft/TypeScript-go/pull/3161) (Closed, **jakebailey**, **Copilot**)

**Fix documentation inheritance for static method overrides on mixin intersection types**

*Restore inherited documentation for static methods overridden in classes extending mixin intersection types by improving base type resolution*

 * **Copilot** assigned to **jakebailey**
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3161#issuecomment-4092774358) **jakebailey** said "@copilot+claude-opus-4.6 address feedback"
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3161#issuecomment-4092865304) **Copilot** addressed feedback by replacing getAllSuperTypeNodes with ast.GetClassExtendsHeritageElement and adding foundInBase tracking to avoid unnecessary work
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3196](https://github.com/microsoft/TypeScript-go/pull/3196) (Closed, **gabritto**)

**Fixes a crash when renaming import path of a JSON file**

*Renaming a JSON file’s import path causes the compiler to crash in TypeScript-Go and Strada.*

 * created by **Andarist**
 * **gabritto** assigned to **gabritto**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3196#issuecomment-4227438785) **gabritto** said "Superseded by #3358"
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript-go#3199](https://github.com/microsoft/TypeScript-go/pull/3199) (Closed, **jakebailey**, **Copilot**)

**Fix declaration emit readonly tuple regression from \`as const satisfies\`**

*Fix regression that wrongly adds readonly to tuple declarations when using as const satisfies by updating pseudotype builder logic.*

 * created by **Copilot**
 * (2 weeks ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3203](https://github.com/microsoft/TypeScript-go/pull/3203) (Closed, **jakebailey**, **Copilot**)

**Fix missing symbol equality check in getExternalModuleMember**

*Add missing symbol equality check in getExternalModuleMember to avoid nil pointer crash when merging module and variable symbols*

 * (2 weeks ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3203#issuecomment-4119360088) **andrewbranch** demonstrated that the code sample still crashed and mentioned an alternative was forthcoming
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3300](https://github.com/microsoft/TypeScript-go/pull/3300) (Closed)

**Rename core\.Pool to core\.Arena**

*Propose renaming core.Pool to core.Arena to accurately reflect its bump allocator functionality.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3306](https://github.com/microsoft/TypeScript-go/pull/3306) (Closed, **RyanCavanaugh**, **Copilot**)

**Implement \`resolveFromTypeRoot\` fallback in module resolution**

*Implement TypeScript’s resolveFromTypeRoot fallback in the Go module resolver to correctly load types from custom typeRoots.*

 * created by **Copilot**
 * (1 week ago) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3355](https://github.com/microsoft/TypeScript-go/pull/3355) (Open)

**Switch to new CI runner system**

*Adopt a new CI runner system to address current issues, leveraging its compatibility with our single-image pools.*

 * created by **jakebailey**
 * [4 days ago](https://github.com/microsoft/TypeScript-go/pull/3355#issuecomment-4195301938) **jakebailey** said "This won't work without a pool change (so far)"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3355#issuecomment-4226977450) **jakebailey** said "This will fail until I can update the pool config, but I can't do that until nobody's running jobs, which sounds like a weekend merge."

### [PR microsoft/TypeScript-go#3363](https://github.com/microsoft/TypeScript-go/pull/3363) (Closed)

**Make LS checkers time out after being idle, segment based on use**

*Refactor the checker pool to categorize and configure diagnostic, temporary, and API checkers with idle-timeout cleanup via channels.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3363#issuecomment-4225544676) **andrewbranch** reported no negative effects after testing and concluded the approach is fine, then asked if any Copilot feedback is important
 * [today](https://github.com/microsoft/TypeScript-go/pull/3363#issuecomment-4225553228) **jakebailey** said "Yeah, it all seems plausible; I will look at it (was just preoccupied with other stuff and accidentally archived the email with these comments)."
 * [today](https://github.com/microsoft/TypeScript-go/pull/3363#issuecomment-4225848239) **jakebailey** mentioned that they fixed the comments but were uncertain how the changes should work for API users or tsgolint
 * [today](https://github.com/microsoft/TypeScript-go/pull/3363#issuecomment-4226698206) **jakebailey** said "@camc314 Do you know how this might affect your usage of these checkers? Is there some sort of setting that would make this not break you, if so?"
 * [later](https://github.com/microsoft/TypeScript-go/pull/3363#issuecomment-4229263846) **camc314** tested the branch on tsgolint and reported it worked fine

### [PR microsoft/TypeScript-go#3367](https://github.com/microsoft/TypeScript-go/pull/3367) (Closed)

**Codegen Go and TypeScript SyntaxKinds, ASTs, factories, visitors, type guards, encoders, decoders**

*Implement various updates to Go and TypeScript AST code generation, including SyntaxKind renames, factory adjustments, and structural enhancements.*

 * created by **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3367#issuecomment-4225048512) **andrewbranch** said "There are things that I'd like to improve and additional things I'd like to generate, but need to get some more time-sensitive stuff out of the way first."
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#3369](https://github.com/microsoft/TypeScript-go/pull/3369) (Closed)

**Limit loader/emitter to GOMAXPROCS**

*Limit loader and emitter concurrency to GOMAXPROCS to reduce overhead from excessive parallelism*

 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/3369#issuecomment-4210075226) **jakebailey** expressed suspicion and requested perf testing by @typescript-bot
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/3369#issuecomment-4210075529) **typescript-bot** reported that perf test jobs started and provided links to the build and results
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/3369#issuecomment-4210183826) **typescript-bot** posted the requested performance run results
 * [today](https://github.com/microsoft/TypeScript-go/pull/3369#issuecomment-4227790293) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3369#issuecomment-4227790485) **typescript-bot** posted update indicating performance test jobs started with status links
 * [today](https://github.com/microsoft/TypeScript-go/pull/3369#issuecomment-4227905032) **typescript-bot** shared the requested performance run results

### [Issue microsoft/TypeScript-go#3372](https://github.com/microsoft/TypeScript-go/issues/3372) (Closed, **jakebailey**, **Copilot**)

**Not having dependency for type should make tsgo error**

*tsgo does not report an error when required Node type definitions are missing despite tsconfig specifying them, unlike tsc.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3372#issuecomment-4216044558) **jakebailey** said "Hm, we must be missing the code that actually validates that all parts of types can be resolved."
 * (yesterday) **jakebailey** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3373](https://github.com/microsoft/TypeScript-go/pull/3373) (Closed, **jakebailey**, **Copilot**)

**Report "Cannot find type definition file" error for unresolved types in compilerOptions**

*Add diagnostics for failed type directive resolution and fix filesparser propagation to report unresolved type definition errors in tsgo*

 * created by **Copilot**
 * (yesterday) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3382](https://github.com/microsoft/TypeScript-go/pull/3382) (Closed)

**Support LSP \`source\.fixAll\`**

*Enable source.fixAll LSP code action in the TypeScript VS Code extension by porting code and enhancing import handling.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3383](https://github.com/microsoft/TypeScript-go/pull/3383) (Closed)

**Fix see/link hover scoping**

*Port container-setting functions for JSDoc see/link hover scoping while preserving comments at removed calls.*

 * created by **jakebailey**

### [Issue microsoft/TypeScript-go#3384](https://github.com/microsoft/TypeScript-go/issues/3384) (Open, `Crash`, **andrewbranch**)

**Crash in adjusting positions for folding ranges**

*Adjusting folding range end positions in the Go language service now crashes due to LineAndCharacterToPosition conversion errors.*

 * created by **DanielRosenwasser**
 * **DanielRosenwasser** added label `Crash`
 * [today](https://github.com/microsoft/TypeScript-go/issues/3384#issuecomment-4226576283) **jakebailey** said "that's very odd, given that implies the line map itself is wrong..."
 * [today](https://github.com/microsoft/TypeScript-go/issues/3384#issuecomment-4226609473) **jakebailey** said "What is the actual message?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/3384#issuecomment-4226616160) **DanielRosenwasser** said "No idea - we only keep the stack around."
 * [today](https://github.com/microsoft/TypeScript-go/issues/3384#issuecomment-4227398094) **DanielRosenwasser** suspected the issue stemmed from the snapshotfs implementation because reloadEntry methods didn’t update certain fields and noted difficulty reproducing it end-to-end

### [PR microsoft/TypeScript-go#3385](https://github.com/microsoft/TypeScript-go/pull/3385) (Open)

**Restore CommaListExpression support**

*Proposal to restore the CommaListExpression optimization removed in PR #3367 that prevented excessively nested comma binary expressions.*

 * created by **jakebailey**

### [Issue microsoft/TypeScript-go#3386](https://github.com/microsoft/TypeScript-go/issues/3386) (Closed)

**\[ServerErrors\]\[TypeScript\] main vs **

*TypeScript CI reported errors in 300 repos, finding 14 changes, 193 unchanged, and 93 clone, timeout, or unknown failures.*

 * created by **typescript-bot**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3386#issuecomment-4227338270) **typescript-bot** reported a panic during textDocument/formatting with a debug failure and provided a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/3386#issuecomment-4227338302) **typescript-bot** reported a panic during handling of textDocument/rename due to nil pointer dereference
 * [today](https://github.com/microsoft/TypeScript-go/issues/3386#issuecomment-4227338348) **typescript-bot** reported a panic during cross-project handling of textDocument/rename with stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/3386#issuecomment-4227338391) **typescript-bot** reported a panic during cross-project handling of a textDocument/rename request due to a nil pointer dereference
 * [today](https://github.com/microsoft/TypeScript-go/issues/3386#issuecomment-4227338415) **typescript-bot** reported a panic handling textDocument/formatting with a debug failure and stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/3386#issuecomment-4227338443) **typescript-bot** reported a panic with 'unimplemented' and accompanying stack trace in typescript-go internal project
 * [today](https://github.com/microsoft/TypeScript-go/issues/3386#issuecomment-4227338467) **typescript-bot** reported a panic due to invalid memory address or nil pointer dereference and included a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/3386#issuecomment-4227338503) **typescript-bot** reported a panic during handling of textDocument/formatting due to a debug failure 'False expression: Token end is child end' and included a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/3386#issuecomment-4227338528) **typescript-bot** reported a panic while handling textDocument/rangeFormatting due to a debug failure: False expression: Token end is child end
 * [today](https://github.com/microsoft/TypeScript-go/issues/3386#issuecomment-4227338550) **typescript-bot** reported that the server connection closed prematurely and provided error details, artifacts, and replay commands for t4t5/sweetalert
 * [today](https://github.com/microsoft/TypeScript-go/issues/3386#issuecomment-4227338579) **typescript-bot** reported that the server connection closed prematurely with undefined, listed the affected repo, provided links to raw error text and replay commands, and showed the last few requests
 * [today](https://github.com/microsoft/TypeScript-go/issues/3386#issuecomment-4227338609) **typescript-bot** reported that the server connection closed prematurely with undefined for n8n-io/n8n, included raw error text, artifact links, recent protocol requests, and reproduction steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/3386#issuecomment-4227338657) **typescript-bot** reported a panic when handling a textDocument/formatting request due to a debug failure: False expression: Token end is child end
 * [today](https://github.com/microsoft/TypeScript-go/issues/3386#issuecomment-4227338675) **typescript-bot** reported a panic in textDocument/formatting request due to a debug failure and included the stack trace

### [PR microsoft/TypeScript-go#3387](https://github.com/microsoft/TypeScript-go/pull/3387) (Closed)

**Typecheck scripts, fix convertFourslash**

*Enable typechecking of scripts in CI and incorporate the convertFourslash fix from PR 3304.*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#3388](https://github.com/microsoft/TypeScript-go/pull/3388) (Closed)

**No reparsing of CommonJS constructs**

*Remove re-parsing of CommonJS constructs and instead handle module.exports and exports in the binder and checker, ignoring CJS in ES modules.*

 * created by **ahejlsberg**

