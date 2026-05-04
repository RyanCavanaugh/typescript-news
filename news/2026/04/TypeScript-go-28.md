# Report for 2026-04-28 (Tuesday, April 28th, 2026)

11 different users commented on 39 different issues.

## Recommended Actions

 * Response Recommended
    * @Swiftwork reported experiencing the same issue for the last 1-2 weeks in [microsoft/TypeScript-go#3621](https://github.com/microsoft/TypeScript-go/issues/3621#issuecomment-4342371254)

## Activity Summary

### [Issue microsoft/TypeScript-go#3437](https://github.com/microsoft/TypeScript-go/issues/3437) (Closed)

**\[ServerErrors\]\[TypeScript\] main vs **

*The TypeScript error-delta pipeline on the main branch analyzed 300 popular GitHub repos, succeeding on 201 with 8 interesting changes and various failures.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/3437#issuecomment-4271898817) **typescript-bot** reported a premature server connection closure and provided logs, affected repos, last requests, and repro steps
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/3437#issuecomment-4271898868) **typescript-bot** reported that the server connection closed prematurely with an undefined error for the n8n repository and provided artifact links, recent editor requests, and repro steps
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/3437#issuecomment-4271898938) **typescript-bot** reported a panic failure in textDocument/formatting handling due to false expression Token end is child end
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript-go#3497](https://github.com/microsoft/TypeScript-go/pull/3497) (Open)

**Widen types assigned to auto\-typed variables**

*Widen the types assigned to automatically-typed variables to improve type coverage and flexibility.*

 * [6 days ago](https://github.com/microsoft/TypeScript-go/pull/3497#issuecomment-4300255694) **ahejlsberg** said "Looks like we're fine on perf, but wondering what the changes in user tests and top 400 are about?"
 * [5 days ago](https://github.com/microsoft/TypeScript-go/pull/3497#issuecomment-4303092861) **Andarist** shared a webpack reproduction and noted that the union Record<string, CodeValue> | {} now reduces to {} due to JSLiteral flag differences affecting subtype reduction, and said they would investigate further
 * [5 days ago](https://github.com/microsoft/TypeScript-go/pull/3497#issuecomment-4306383124) **Andarist** said "New tests are in now."
 * [today](https://github.com/microsoft/TypeScript-go/pull/3497#issuecomment-4338203608) **ahejlsberg** questioned whether the proposed change would cause property accesses (x.a, x.b, w.a, w.b) to error and argued this is undesirable
 * [today](https://github.com/microsoft/TypeScript-go/pull/3497#issuecomment-4339455258) **Andarist** demonstrated a TypeScript repro where accessing x.a should error but doesn’t, noted that the displayed type doesn’t reflect this, and said they would review all cases and propose a design over the upcoming weekend

### [PR microsoft/TypeScript-go#3505](https://github.com/microsoft/TypeScript-go/pull/3505) (Open)

**integrated filewatcher with lsp**

*Refactor vfswatch.FileWatcher for use by both CLI and LSP, integrating polling for clients without didChangeWatchedFiles support.*

 * created by **johnfav03**
 * [later](https://github.com/microsoft/TypeScript-go/pull/3505#issuecomment-4345380442) **andrewbranch** suggested trying usePollingWatcher and noted that the LSP client watcher still ran, observed that it scanned the .git directory causing slow performance, started profiling and recommended manual testing

### [Issue microsoft/TypeScript-go#3599](https://github.com/microsoft/TypeScript-go/issues/3599) (Closed)

**\[ServerErrors\]\[TypeScript\] main vs **

*An Azure pipeline run on TypeScript main analyzed 300 GitHub repositories, finding 14 interesting changes, clone failures, and timeouts.*

 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/3599#issuecomment-4317050284) **typescript-bot** reported a server connection closed prematurely error with details, affected repo, last requests, and repro steps
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/3599#issuecomment-4317050309) **typescript-bot** reported that the server connection closed prematurely with an undefined error and provided repro steps for babel/babel
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/3599#issuecomment-4317050349) **typescript-bot** reported a premature server connection closure with associated logs, affected repo details, recent requests, and repro steps
 * (today) **gabritto** closed the issue

### [Issue microsoft/TypeScript-go#3600](https://github.com/microsoft/TypeScript-go/issues/3600) (Closed, `bug`, `Domain: Type Checking`, **ahejlsberg**)

**Behaviour differences observed when plain js class getter return null in conditional branch**

*TypeScript and tsgo differ in inferring nullability of JavaScript class getters, causing inconsistent errors on property access.*

 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/3600#issuecomment-4321250824) **hkleungai** observed that moving the map assignment into the constructor caused errors in tsgo but not in tsc and updated the comment to include both cases
 * (yesterday) **ahejlsberg** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/issues/3600#issuecomment-4333661647) **hkleungai** reported that 7.0.0-dev.20260428.1 only partially resolved the issue, shared new tsgo errors, and asked whether to reopen the issue or open a new one
 * [today](https://github.com/microsoft/TypeScript-go/issues/3600#issuecomment-4339794541) **ahejlsberg** stated that the issue was fixed by #3648

### [Issue microsoft/TypeScript-go#3601](https://github.com/microsoft/TypeScript-go/issues/3601) (Closed)

**Restart Server: "Stopping timed out" on first click when server is hung**

*TypeScript Native Preview's Restart Server command times out on first attempt when server hangs and only succeeds on retry.*

 * created by **ekazakov14**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#3602](https://github.com/microsoft/TypeScript-go/pull/3602) (Closed)

**Recover from shutdown timeout in tryRestart**

*Wrap restart in try/catch to fall back to a forced TypeScript language server start when graceful shutdown times out.*

 * created by **ekazakov14**
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#3605](https://github.com/microsoft/TypeScript-go/issues/3605) (Closed, `Domain: Editor`)

**Missing generic param displayed in hover**

*Hovering over a method in a defaulted generic class fails to display its generic parameter in tsgo while TypeScript 6.0 shows it.*

 * created by **Withered-Flower-0422**
 * **Withered-Flower-0422** added label `Domain: Editor`
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript-go#3606](https://github.com/microsoft/TypeScript-go/pull/3606) (Closed)

**fix\(3605\): Missing generic param displayed in hover**

*Restore display of missing generic parameters in hover tooltips to prevent related crash.*

 * created by **a-tarasyuk**
 * (today) **gabritto** closed the issue

### [Issue microsoft/TypeScript-go#3611](https://github.com/microsoft/TypeScript-go/issues/3611) (Open)

**Elevated CPU usage in \`\-\-watch\` mode when idle \(compared to tsc\)**

*tsgo --watch mode consistently consumes 5-10% CPU while idle, whereas tsc --watch mode remains at 0%.*

 * created by **alexswan93**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3611#issuecomment-4339900462) **DanielRosenwasser** described that the current strategy was naive polling at a fixed frequency and mentioned that @jakebailey was implementing perf infrastructure in the typescript-go repo

### [Issue microsoft/TypeScript-go#3613](https://github.com/microsoft/TypeScript-go/issues/3613) (Closed, `bug`, `Domain: Type Checking`, **ahejlsberg**)

**Behaviour difference: merging \`interface\`s with identically named getter/setter pair and field**

*Merging interfaces with identical getter/setter and property definitions triggers duplicate identifier errors in tsgo but not in TypeScript 6.0.*

 * created by **mcpower**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3613#issuecomment-4340199480) **ahejlsberg** said "Strada doesn't really get this one right either. If you reverse the two interface declarations, Strada also errors. Corsa is at least consistent here in that it always errors."

### [Issue microsoft/TypeScript-go#3621](https://github.com/microsoft/TypeScript-go/issues/3621) (Open, `Crash`)

**Panic Alert Notification when Cursor edits some file and opening that file causes panic\.**

*Opening or editing a file causes a panic in the semanticTokens request because a token improperly spans multiple lines.*

 * created by **RealHaris**
 * **RealHaris** added label `Crash`
 * [later](https://github.com/microsoft/TypeScript-go/issues/3621#issuecomment-4342371254) **Swiftwork** said "Observing same issue for the last 1-2 weeks"

### [PR microsoft/TypeScript-go#3628](https://github.com/microsoft/TypeScript-go/pull/3628) (Open, **andrewbranch**, **Copilot**)

**Fix server hang after "Running scheduled diagnostics refresh"**

*Unbounded diagnostic and watch waits causing server hangs are fixed by non-blocking refresh, timed rollback, and a watch registry.*

 * (yesterday) **Copilot** assigned to **Copilot**, **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3628#issuecomment-4336939973) **andrewbranch** said "@copilot fix review comments"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3628#issuecomment-4337091047) **Copilot** addressed all review comments by updating RefreshDiagnostics to check ctx.Err(), creating the timeout context after acquiring watchesMu, and rolling back session.watches on WatchFiles failures with a single retry after 1s
 * [today](https://github.com/microsoft/TypeScript-go/pull/3628#issuecomment-4337840587) **Copilot** addressed all review comments across e2074f9e, ccd56581, and 60619b9d
 * [today](https://github.com/microsoft/TypeScript-go/pull/3628#issuecomment-4338359955) **andrewbranch** said "@copilot write a test for the updateWatch timeout and retry. I think you should be able to mock the client implementation using synctest."
 * [today](https://github.com/microsoft/TypeScript-go/pull/3628#issuecomment-4338480676) **Copilot** added synctest subtests verifying that a slow client triggers timeout and rollback and that a subsequent call succeeds
 * [today](https://github.com/microsoft/TypeScript-go/pull/3628#issuecomment-4339083623) **Copilot** rewrote the test for updateWatch timeout and retry using real session operations and synctest, mocking WatchFilesFunc to block on the first batch and verifying that after a timeout-induced rollback the registry remained clean for re-registration

### [PR microsoft/TypeScript-go#3636](https://github.com/microsoft/TypeScript-go/pull/3636) (Closed)

**Fix signature help crash in WIP JSX text on opening \`\<\`**

*Resolve a crash in TypeScript signature help triggered by typing an opening “<” in work-in-progress JSX text*

 * created by **Andarist**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3636#issuecomment-4338030726) **andrewbranch** said "Is this fix a missing port from Strada? It's always helpful to know what the root cause is if Strada doesn't crash/error, because there could be more stuff that's wrong or missing deeper in the stack."
 * [today](https://github.com/microsoft/TypeScript-go/pull/3636#issuecomment-4338285175) **DanielRosenwasser** suggested that Strada discarded the << token in createChildren/addSyntheticNodes because its end exceeded the containing node's end position
 * [today](https://github.com/microsoft/TypeScript-go/pull/3636#issuecomment-4339385269) **Andarist** recalled that the children syntax list was reparsed on demand in Strada, agreed that the `textPos <= end` check prevented the issue, reconsidered a similar bounds check, and confirmed that Strada missed the first token in node.getChildren() due to that check

### [Issue microsoft/TypeScript-go#3639](https://github.com/microsoft/TypeScript-go/issues/3639) (Closed, `bug`, `Domain: Type Checking`, **ahejlsberg**)

**Behaviour differences: plain js's ternary assignment of objects in different shapes confuses tsgo**

*tsgo does not detect a missing 'message' property error when destructuring objects assigned with a ternary operator in JavaScript code, unlike TypeScript 6*

 * created by **hkleungai**
 * (today) **ahejlsberg** added labels `bug`, `Domain: Type Checking`, and assigned to **ahejlsberg**
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#3640](https://github.com/microsoft/TypeScript-go/pull/3640) (Closed)

**Restore \#3529**

*Restore PR #3529 which was accidentally reverted due to a merge queue bug.*

 * created by **gabritto**
 * (today) **gabritto** closed the issue

### [Issue microsoft/TypeScript-go#3641](https://github.com/microsoft/TypeScript-go/issues/3641) (Closed, `bug`, `Domain: Type Checking`, **ahejlsberg**)

**Behavior difference: Callback\-first promise resolve\(\) gives inconsistent error**

*TypeScript and tsgo produce conflicting error messages when calling Promise resolve without arguments in JavaScript.*

 * created by **hkleungai**
 * (today) **ahejlsberg** added labels `Domain: Type Checking`, `bug`, and assigned to **ahejlsberg**
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#3642](https://github.com/microsoft/TypeScript-go/issues/3642) (Closed, `bug`, `Domain: Type Checking`)

**Behavior difference: False positive on plain\-js class attribute spread assignment**

*tsgo raises a false-positive TS2322 error on spreading into a JavaScript class property, while plain tsc reports no error.*

 * created by **hkleungai**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3642#issuecomment-4338728174) **ahejlsberg** said "This is caused by the same issue as #3639."
 * (today) **ahejlsberg** added labels `bug`, `Domain: Type Checking`
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#3643](https://github.com/microsoft/TypeScript-go/pull/3643) (Open, **andrewbranch**, **Copilot**)

**Fix isInitialized not restored after tryRestart**

*tryRestart doesn’t reset the isInitialized flag or trigger initialization events after restart, preventing new listeners from firing.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **andrewbranch**

### [Issue microsoft/TypeScript-go#3644](https://github.com/microsoft/TypeScript-go/issues/3644) (Closed, `wontfix`)

**Behavior difference: Bracket is missing when generic argument is put as a parameter for another generic**

*tsgo omits parentheses around function-type generic arguments when nested in another generic, unlike TypeScript 6.0.*

 * created by **hkleungai**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3644#issuecomment-4338744896) **ahejlsberg** said "This is by design. The parentheses aren't necessary so Corsa doesn't include them."
 * **ahejlsberg** added label `wontfix`
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#3645](https://github.com/microsoft/TypeScript-go/issues/3645) (Open, `Domain: Editor`, `Crash`, **andrewbranch**, **Copilot**)

**Auto\-imports for JSX tag trigger assertion violation when React is type\-imported\.**

*Automatic JSX tag imports crash with an assertion violation when React is imported only as a type*

 * created by **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3645#issuecomment-4339305888) **DanielRosenwasser** suggested applying the promotion from type-only to regular import for returned names and falling back to usual auto-import logic when that fails
 * (today) **DanielRosenwasser** assigned to **Copilot**, **DanielRosenwasser**

### [PR microsoft/TypeScript-go#3646](https://github.com/microsoft/TypeScript-go/pull/3646) (Closed)

**Handle type parameter declaration as type node in printer**

*Handle type parameter declarations as type nodes in the printer to prevent crashes and correctly display bounded type arguments in hover output.*

 * created by **gabritto**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3646#issuecomment-4338377820) **gabritto** realized that the correct fix was in PR #3606 and explained that replacement of type parameter references with declarations should only occur in type argument expressions
 * (today) **gabritto** closed the issue

### [Issue microsoft/TypeScript-go#3647](https://github.com/microsoft/TypeScript-go/issues/3647) (Closed, `bug`, `Domain: Declaration Emit`, **weswigham**)

**Behavior difference: TS7053 union count is slightly off in tsgo**

*tsgo miscounts large unions under stableTypeOrdering and inconsistently applies TS7053 index errors compared with tsc*

 * created by **hkleungai**
 * **ahejlsberg** assigned to **weswigham**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3647#issuecomment-4338766493) **ahejlsberg** said "Yeah, looks like the counts are one off."
 * (today) **ahejlsberg** added labels `bug`, `Domain: Declaration Emit`, and set milestone to `TypeScript 7.0 RC`
 * (later) **gabritto** closed the issue

### [PR microsoft/TypeScript-go#3648](https://github.com/microsoft/TypeScript-go/pull/3648) (Closed)

**Always widen resulting type in \`getWidenedTypeForAssignmentDeclaration\`**

*Always widen the resulting type in getWidenedTypeForAssignmentDeclaration for assignment declarations*

 * created by **ahejlsberg**
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#3649](https://github.com/microsoft/TypeScript-go/pull/3649) (Closed, **RyanCavanaugh**, **Copilot**)

**Add TS\_GO\_DEBUG\_STACK\_LIMIT to cap goroutine stack size at entry points**

*Add an opt-in TS_GO_DEBUG_STACK_LIMIT environment variable to configure and enforce goroutine stack size caps at startup.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3649#issuecomment-4339647092) **RyanCavanaugh** tested stack limit thresholds and observed instant failure at 1,000,000 with 3,000 elided frames and fast execution at 5,000,000 with 28,000 elided frames, recommending the latter for local development

### [PR microsoft/TypeScript-go#3650](https://github.com/microsoft/TypeScript-go/pull/3650) (Open, **DanielRosenwasser**, **Copilot**)

**Fix assertion violation in auto\-imports for JSX tag when React is type\-imported**

*Refactor symbol import logic to handle type-only React imports and prevent JSX auto-import assertion failures.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3650#issuecomment-4339635488) **DanielRosenwasser** asked if each fix was discrete and could be combined and noted that `isJsxNamespaceFix` was never set

### [Issue microsoft/TypeScript-go#3651](https://github.com/microsoft/TypeScript-go/issues/3651) (Open, `Domain: Editor`, **andrewbranch**)

**"Native Preview: Disable" does not re\-activate built\-in extension**

*Disabling the native preview fails to restore the built-in TypeScript extension in VS Code.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** added label `Domain: Editor`, and assigned to **andrewbranch**

### [PR microsoft/TypeScript-go#3652](https://github.com/microsoft/TypeScript-go/pull/3652) (Closed, **andrewbranch**, **Copilot**)

**Fix "Disable" not reactivating built\-in TypeScript extension**

*A command ID conflict between the TypeScript native preview and the built-in extension prevents it from reactivating when disabled.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3652#issuecomment-4339701108) **andrewbranch** said "@copilot add a command palette menu item for this in package.json. It should say "TypeScript Native Preview: Select TypeScript Version...""
 * [today](https://github.com/microsoft/TypeScript-go/pull/3652#issuecomment-4339723939) **Copilot** added a command palette menu item named "TypeScript Native Preview: Select TypeScript Version..." in package.json and noted it appears when the server is running
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#3653](https://github.com/microsoft/TypeScript-go/pull/3653) (Closed)

**Port code to issue JS specific error for promises**

*Port code to generate JavaScript-specific error messages for promise handling*

 * created by **ahejlsberg**
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#3654](https://github.com/microsoft/TypeScript-go/issues/3654) (Open, **DanielRosenwasser**)

**Harden rescan strategy for astnav**

*Identify and optimize necessary astnav rescan points to prevent redundant rescans already handled by the formatting scanner.*

 * created by **DanielRosenwasser**
 * **DanielRosenwasser** assigned to **DanielRosenwasser**

### [Issue microsoft/TypeScript-go#3655](https://github.com/microsoft/TypeScript-go/issues/3655) (Open)

**Behavior difference: Pattern matching against \`extends { \[P in K\]?: unknown }\` emit slightly different error in tsgo**

*tsgo inconsistently expands mapped type constraint { [P in K]?: unknown } in generics, causing different errors than tsc*

 * created by **hkleungai**

### [Issue microsoft/TypeScript-go#3656](https://github.com/microsoft/TypeScript-go/issues/3656) (Closed, `bug`, `Domain: Type Checking`, **ahejlsberg**)

**Behavior difference: Optional marking with jsdoc does not correctly treat param as undefined**

*JSDoc optional parameter marking in tsgo fails to include undefined in the parameter type, causing null assignment errors.*

 * created by **hkleungai**
 * (later) **ahejlsberg** added labels `bug`, `Domain: Type Checking`, set milestone to `TypeScript 7.0 RC`, and assigned to **ahejlsberg**

### [Issue microsoft/TypeScript-go#3657](https://github.com/microsoft/TypeScript-go/issues/3657) (Closed, `wontfix`)

**Behavior difference: TS2349 error does not tell resolution\-mode in tsgo**

*tsgo’s TS2349 error output omits the resolution-mode annotation that tsc includes under nodenext module resolution.*

 * created by **hkleungai**
 * [later](https://github.com/microsoft/TypeScript-go/issues/3657#issuecomment-4345351366) **jakebailey** said "I have no idea why 6.0 would print it that way, when the import statement does not have  resolution-mode written?"

### [PR microsoft/TypeScript-go#3658](https://github.com/microsoft/TypeScript-go/pull/3658) (Closed)

**Fix off\-by\-one truncation in union type display**

*Fixes an off-by-one truncation error in the display of union types.*

 * created by **Andarist**
 * (later) **gabritto** closed the issue

### [Issue microsoft/TypeScript-go#3659](https://github.com/microsoft/TypeScript-go/issues/3659) (Open)

**Behavior difference: JSDoc comments are stripped for mapped types**

*Mapped types in TypeScript 7 beta strip JSDoc comments from original properties, unlike TypeScript 6.0.3.*

 * created by **andrewzolotukhin**

