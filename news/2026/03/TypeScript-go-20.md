# Report for 2026-03-20 (Friday, March 20th, 2026)

9 different users commented on 29 different issues.

## Activity Summary

### [PR microsoft/TypeScript-go#1693](https://github.com/microsoft/TypeScript-go/pull/1693) (Closed)

**Port \`\-\-isolatedDeclarations\` related node builder logic**

*Refactor and port isolatedDeclarations node builder logic to Go by adding a pseudochecker abstraction and enhancing reuseNode validation.*

 * [10 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1693#issuecomment-3726460827) **jakebailey** noted nothing objectionable, asked if pseudo concepts formalized previous logic, and pointed out a wrong emitMethodCalledNew diff
 * [10 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1693#issuecomment-3726625796) **weswigham** provided updates on bugfixes, PR #2459 baseline update, and explained the pseudo type comparison logic with future improvements
 * [10 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1693#issuecomment-3726656248) **weswigham** noted that --isolatedDeclarations support was partial and that error generation logic still needed porting; offered to add it but cautioned about large baseline diffs
 * [today](https://github.com/microsoft/TypeScript-go/pull/1693#issuecomment-4100529012) **jakebailey** said "Closing given the version with baselines updated were added in #2459."
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2427](https://github.com/microsoft/TypeScript-go/issues/2427) (Closed, `bug`)

**\`isolatedDeclarations\` is not yet implemented**

*tsgo does not implement the isolatedDeclarations compiler option, so it fails to report missing annotations unlike tsc 5.9.*

 * [10 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2427#issuecomment-3720630512) **jakebailey** said "See also #1693, #2459"
 * [9 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2427#issuecomment-3731130416) **jakebailey** said "To be clear, the linked issue adds some of the code to start getting us there, but not the errors."
 * [7 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2427#issuecomment-3816683513) **valentinmelusson** asked for a rough ETA on adding isolated declarations errors support
 * [today](https://github.com/microsoft/TypeScript-go/issues/2427#issuecomment-4100315005) **jakebailey** said "#2459 is now merged. This does the errors, but does not do the fixes yet."
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#2459](https://github.com/microsoft/TypeScript-go/pull/2459) (Closed)

**Port \-\-isolatedDeclarations related node builder logic, with baseline updates**

*Port node builder logic for the --isolatedDeclarations option and apply baseline updates for review.*

 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/2459#issuecomment-4086041403) **gabritto** suggested adding a sort to the script
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2459#issuecomment-4093041808) **jakebailey** identified the missing error in isolatedDeclarationErrorsExpressions.errors.txt.diff as the only remaining potential problem and noted other issues were minor
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2459#issuecomment-4093042956) **jakebailey** said "Well, that and, updating baselines again, it seems."
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript-go#2929](https://github.com/microsoft/TypeScript-go/pull/2929) (Closed, **RyanCavanaugh**, **Copilot**)

**Add high\-quality SKILL for compiler and fourslash tests**

*Create a comprehensive SKILL.md guide documenting compiler and fourslash test workflows with proper formatting and integrated review feedback.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2929#issuecomment-3974292707) **Copilot** notified that the skill lacked the proper header and moved it to .github/skills/compiler-and-fourslash-tests/SKILL.md with YAML frontmatter
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2929#issuecomment-3974740167) **RyanCavanaugh** said "@copilot+claude-opus-4.6 integrate everyone's feedback and push a new commit"
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2929#issuecomment-3974776460) **Copilot** integrated feedback and pushed commit 45bec897, removing unnecessary sections, updating syntax, and adjusting commands
 * [today](https://github.com/microsoft/TypeScript-go/pull/2929#issuecomment-4100094179) **Copilot** revised the skill document based on comments, tested all --tests patterns, and updated examples with explanation of Go's -run regex matching
 * [today](https://github.com/microsoft/TypeScript-go/pull/2929#issuecomment-4100402075) **Copilot** added explicit guidance to run all tests as the first step and updated workflow sections to use `npx hereby test`
 * [today](https://github.com/microsoft/TypeScript-go/pull/2929#issuecomment-4100504000) **RyanCavanaugh** said "@copilot+claude-opus-4.6 do what he says"
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#2944](https://github.com/microsoft/TypeScript-go/pull/2944) (Open)

**\[draft\] more formatting tests **

*Add draft formatting tests to validate and troubleshoot the repository’s testing pipelines.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/2944#issuecomment-4027129682) **typescript-bot** reported that the test top100 job failed to queue due to validation errors or warnings
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2944#issuecomment-4093375627) **typescript-bot** said "@@iisaduan, the perf run you requested failed. You can check the log here."
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2944#issuecomment-4093891403) **typescript-bot** said "@iisaduan, the perf run you requested failed. You can check the log here."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2944#issuecomment-4100406855) **typescript-bot** said "@iisaduan, the perf run you requested failed. You can check the log here."

### [PR microsoft/TypeScript-go#3110](https://github.com/microsoft/TypeScript-go/pull/3110) (Closed)

**Big omnibus of JS emit differences**

*Addresses miscellaneous JavaScript emit differences by extracting destructuring code to ensure consistent CommonJS output.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3121](https://github.com/microsoft/TypeScript-go/issues/3121) (Open, `Needs More Info`)

**extension gets uninstalled after around an hour on vscodium**

*The TypeScript Native Preview extension installed in VSCodium on Linux is uninstalled after about an hour for being flagged problematic.*

 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/3121#issuecomment-4076484678) **RyanCavanaugh** said "Download from where?"
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/3121#issuecomment-4077173146) **huseeiin** recommended downloading the VSIX via VS Code’s extensions tab instead of VSCodium and provided a screenshot
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/3121#issuecomment-4087140542) **mjbvz** asked how they set up the marketplace in vscodium and whether they connected to the official marketplace or a different one
 * **RyanCavanaugh** added label `Needs More Info`

### [PR microsoft/TypeScript-go#3126](https://github.com/microsoft/TypeScript-go/pull/3126) (Closed, **RyanCavanaugh**, **Copilot**)

**Emit TS6053 error for missing reference directive files**

*Emit TS6053 error for missing triple-slash reference files in the Go compiler, align noResolve behavior, and update baselines.*

 * created by **Copilot**
 * (3 days ago) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3126#issuecomment-4099495030) **Copilot** skipped referenced files and type reference directive processing when noResolve was set
 * [today](https://github.com/microsoft/TypeScript-go/pull/3126#issuecomment-4099873499) **Copilot** addressed the code review comment in commit f224b98e, updating the File_0_not_found diagnostic to use the original reference directive string instead of the resolved absolute path, matching TypeScript's output

### [PR microsoft/TypeScript-go#3135](https://github.com/microsoft/TypeScript-go/pull/3135) (Closed)

**Misc CHANGES\.md additions**

*Add miscellaneous changelog entries to CHANGES.md covering most .errors.txt.diffs with submoduleAccepted.txt PR forthcoming.*

 * created by **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3135#issuecomment-4099720882) **RyanCavanaugh** said "More misses than hits in this one"
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#3157](https://github.com/microsoft/TypeScript-go/pull/3157) (Closed)

**Fix named export aliases merging with \`export =\`**

*Combining named export aliases with export = skips alias resolution, resulting in missing errors and silent failures.*

 * created by **andrewbranch**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3157#issuecomment-4090825312) **andrewbranch** said "Hey look, a diff was deleted!"
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#3162](https://github.com/microsoft/TypeScript-go/pull/3162) (Closed)

**Organize imports comment duplication**

*OrganizeImports source action duplicated comments above export statements, resulting in repeated comment blocks.*

 * created by **johnfav03**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3162#issuecomment-4099037027) **bradleyayers** clarified that the problem was with exports rather than imports
 * [today](https://github.com/microsoft/TypeScript-go/pull/3162#issuecomment-4099443518) **johnfav03** explained that the bug existed for imports in their initial implementation but was fixed in PR review and that they must have overlooked the export case

### [PR microsoft/TypeScript-go#3167](https://github.com/microsoft/TypeScript-go/pull/3167) (Open)

**Fix: skip CommonJS export binding when module or exports is a local variable**

*Skips binding CommonJS exports when module or exports is locally defined to avoid shadowing ESM exports and spurious diagnostics.*

 * created by **Muhammad-Bin-Ali**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3167#issuecomment-4093018437) **Muhammad-Bin-Ali** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3167#issuecomment-4099806795) **jakebailey** questioned clearing the CJS indicator mid walk and suggested guarding the initial assignment instead
 * [today](https://github.com/microsoft/TypeScript-go/pull/3167#issuecomment-4100028136) **Muhammad-Bin-Ali** agreed with the suggestion to guard the assignment and said they would implement it

### [PR microsoft/TypeScript-go#3168](https://github.com/microsoft/TypeScript-go/pull/3168) (Closed)

**Add all\-checks task to hereby**

*Add an all-checks task to hereby to run lint and tests together while excluding API-package and generate checks*

 * created by **gabritto**
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript-go#3170](https://github.com/microsoft/TypeScript-go/pull/3170) (Closed)

**fix: nil pointer deref when accessing module exports in name resolver**

*Optional chaining for Symbol is missing in Corsa's name resolver, causing nil pointer dereferences when accessing module exports*

 * created by **camc314**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3170#issuecomment-4099734974) **jakebailey** described difficulty figuring out a test and speculated about a JS parsing and await reparsing interaction issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/3170#issuecomment-4099847189) **jakebailey** stated inability to test the change and suggested labeling it as misported and merging it
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3174](https://github.com/microsoft/TypeScript-go/issues/3174) (Closed, `enhancement`, **andrewbranch**)

**ThrottleGorup Semaphore ussage**

*Refactor the ThrottleGroup implementation to use errgroup.SetLimit instead of a custom semaphore for concurrency control.*

 * created by **code-ghoost**
 * (today) **RyanCavanaugh** added label `enhancement`, and assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3174#issuecomment-4099362973) **andrewbranch** explained that the errgroup-based rewrite limited concurrency per group, causing the npm install cap to be exceeded when processing multiple snapshot updates
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#3176](https://github.com/microsoft/TypeScript-go/pull/3176) (Open)

**Fix ref count cache inconsistencies**

*Revert cache ref-count simplification so parse cache entries start with refCount 1 and prevent premature deletion.*

 * created by **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3176#issuecomment-4100719056) **jakebailey** said "Then again, the copilot comments do sound plausible"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3176#issuecomment-4100787880) **andrewbranch** noted that the last commit was a solution but disliked it and discussed the complexity of implementing snapshot reference counting
 * [today](https://github.com/microsoft/TypeScript-go/pull/3176#issuecomment-4100823417) **jakebailey** explained that their PR was headed toward using a wrapper closure for disposing language service objects but they didn't commit that code after opting against that approach and expressed flexibility so long as things work
 * [today](https://github.com/microsoft/TypeScript-go/pull/3176#issuecomment-4100855656) **gabritto** asked if parsing temporary files that didn't make it into a program is possible
 * [today](https://github.com/microsoft/TypeScript-go/pull/3176#issuecomment-4101015139) **andrewbranch** clarified UpdateProgram’s file acquisition and cloning behavior and explained the missing deref caused a memory leak, exemplifying why building programs without reffing then reffing at the end is easier
 * [today](https://github.com/microsoft/TypeScript-go/pull/3176#issuecomment-4101228488) **gabritto** explained the UpdateProgram file acquisition logic and acknowledged that there was no ideal solution
 * [today](https://github.com/microsoft/TypeScript-go/pull/3176#issuecomment-4101468121) **andrewbranch** expressed frustration and suggested reverting to snapshot ref counts while noting that some complications would remain

### [PR microsoft/TypeScript-go#3177](https://github.com/microsoft/TypeScript-go/pull/3177) (Closed)

**Accept diffs where the only difference is quotes**

*Permit diffs that only change quotation marks when the original source and generated output share the same quote style.*

 * created by **RyanCavanaugh**
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#3178](https://github.com/microsoft/TypeScript-go/pull/3178) (Closed)

**Accept diffs where the only difference is union ordering**

*Enable diffs to be accepted when the only changes are the ordering of union types.*

 * created by **RyanCavanaugh**
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#3179](https://github.com/microsoft/TypeScript-go/pull/3179) (Open)

**Fix issue \#3014 **

*In tsgo watch mode, an empty tsconfig files array prevented the initial build and TS18002 diagnostic, causing a silent hang.*

 * created by **JaskiratAnand**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3179#issuecomment-4100894508) **JaskiratAnand** said "@microsoft-github-policy-service agree"
 * (today) **JaskiratAnand** closed the issue
 * (today) **JaskiratAnand** reopened the issue

### [Issue microsoft/TypeScript-go#3180](https://github.com/microsoft/TypeScript-go/issues/3180) (Open)

**Union ordering printback differs due to some lack of node reuse**

*Printback output for union types varies in ordering because nodes are not consistently reused.*

 * created by **RyanCavanaugh**

### [Issue microsoft/TypeScript-go#3181](https://github.com/microsoft/TypeScript-go/issues/3181) (Open)

**\`\| undefined\` in optional parameters/properties unexpectedly printed back in types / \.d\.ts emit**

*TypeScript unexpectedly includes `| undefined` in emitted declaration files for optional parameters and properties.*

 * created by **RyanCavanaugh**

### [PR microsoft/TypeScript-go#3182](https://github.com/microsoft/TypeScript-go/pull/3182) (Closed)

**Accept diffs which add/remove \`\| undefined\` from optional bindings**

*Accept diffs that solely add or remove `| undefined` annotations from optional type bindings.*

 * created by **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3182#issuecomment-4101115425) **RyanCavanaugh** said "n.b. This is based on the previous PR to avoid merge conflicts in submoduleaccepted.txt"
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#3183](https://github.com/microsoft/TypeScript-go/pull/3183) (Open)

**Accept diffs that just reduce error elaboration**

*Accept diffs reducing error message elaboration for the baselines instanceofOperatorWithInvalidOperands.es2015, usingDeclarations.14, and usingDeclarationsWithIteratorObject.*

 * created by **RyanCavanaugh**

### [PR microsoft/TypeScript-go#3184](https://github.com/microsoft/TypeScript-go/pull/3184) (Closed)

**Use NodeIsMissing in typeeraser\.go where Strada did**

*Implement NodeIsMissing error handling in typeeraser.go to match Strada's implementation.*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#3185](https://github.com/microsoft/TypeScript-go/pull/3185) (Closed)

**Ensure tsconfig is passed to dts emit compile tests**

*Pass the TypeScript configuration to dts emit compile tests to prevent detached errors.*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#3186](https://github.com/microsoft/TypeScript-go/pull/3186) (Closed)

**Accept changes solely due to \_jsxFileName**

*Inconsistent absolute paths in _jsxFileName cause spurious test diffs that should be accepted as non-functional changes.*

 * created by **jakebailey**

### [Issue microsoft/TypeScript-go#3187](https://github.com/microsoft/TypeScript-go/issues/3187) (Closed)

**\[ServerErrors\]\[TypeScript\] main vs **

*The TypeScript main branch pipeline analyzed 262 of 300 repositories, reporting 23 changes, timeouts, clone failures, and unknown errors.*

 * created by **typescript-bot**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3187#issuecomment-4101730840) **typescript-bot** reported a panic in textDocument/formatting with debug failure "False expression: Token end is child end" and provided a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/3187#issuecomment-4101730891) **typescript-bot** reported a panic due to invalid memory address during textDocument/rename and included a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/3187#issuecomment-4101730949) **typescript-bot** reported panic with stack trace for textDocument/rename due to nil pointer dereference
 * [today](https://github.com/microsoft/TypeScript-go/issues/3187#issuecomment-4101730971) **typescript-bot** reported a panic during textDocument/rename due to a nil pointer dereference in cross-project handling
 * [today](https://github.com/microsoft/TypeScript-go/issues/3187#issuecomment-4101731042) **typescript-bot** reported a panic during textDocument/rename handling caused by an invalid memory address or nil pointer dereference
 * [today](https://github.com/microsoft/TypeScript-go/issues/3187#issuecomment-4101731070) **typescript-bot** reported a panic during textDocument/rename due to an invalid memory address or nil pointer dereference
 * [today](https://github.com/microsoft/TypeScript-go/issues/3187#issuecomment-4101731103) **typescript-bot** reported a panic in textDocument/formatting due to a debug assertion failure and attached the stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/3187#issuecomment-4101731130) **typescript-bot** reported a panic during cross-project handling of textDocument/rename request
 * [today](https://github.com/microsoft/TypeScript-go/issues/3187#issuecomment-4101731171) **typescript-bot** reported a panic in handling request textDocument/formatting with a Debug failure: False expression: Token end is child end
 * [today](https://github.com/microsoft/TypeScript-go/issues/3187#issuecomment-4101731213) **typescript-bot** reported that the server connection closed prematurely with undefined error and provided affected repos, last requests, and repro steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/3187#issuecomment-4101731233) **typescript-bot** reported a server connection closed prematurely error and provided repro steps and logs for t4t5/sweetalert
 * [today](https://github.com/microsoft/TypeScript-go/issues/3187#issuecomment-4101731253) **typescript-bot** reported a server connection closed prematurely error with the GrapesJS repo and provided repro steps and logs
 * [today](https://github.com/microsoft/TypeScript-go/issues/3187#issuecomment-4101731329) **typescript-bot** reported that the server connection closed prematurely with undefined and provided affected repos, raw error text, replay commands, last requests, and repro steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/3187#issuecomment-4101731371) **typescript-bot** reported a server connection closed prematurely error and provided affected repo details and logs
 * [today](https://github.com/microsoft/TypeScript-go/issues/3187#issuecomment-4101731418) **typescript-bot** reported server connection closed prematurely error with undefined and included related artifacts for socketio/socket.io
 * [today](https://github.com/microsoft/TypeScript-go/issues/3187#issuecomment-4101731479) **typescript-bot** reported a premature server connection closure error and provided affected repo, raw error logs, replay commands, last requests, and repro steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/3187#issuecomment-4101731569) **typescript-bot** reported a panic during cross-project handling of textDocument/implementation due to invalid memory address or nil pointer dereference
 * [today](https://github.com/microsoft/TypeScript-go/issues/3187#issuecomment-4101731639) **typescript-bot** reported a panic handling request textDocument/implementation caused by invalid memory address or nil pointer dereference

