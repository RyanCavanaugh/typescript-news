# Report for 2026-03-04 (Wednesday, March 4th, 2026)

19 different users commented on 43 different issues.

## Recommended Actions

 * Response Recommended
    * @rubnogueira noted that expandable hovers from TypeScript 5.9 are not implemented in tsgo in [microsoft/TypeScript-go#2457](https://github.com/microsoft/TypeScript-go/issues/2457#issuecomment-4005963689)
    * @justinsmid provided feedback about memory usage after upgrading to the latest nightly in [microsoft/TypeScript-go#2780](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-4005082708)
    * @dbrxnds reported memory usage improvements and reduced peaks in [microsoft/TypeScript-go#2780](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-4005159769)
    * @psznm provided updated repro steps and indicated that subpath import suggestion still fails in [microsoft/TypeScript-go#2974](https://github.com/microsoft/TypeScript-go/issues/2974#issuecomment-3999487766)
    * @psznm asked if moduleResolution nodenext was causing the import issue in [microsoft/TypeScript-go#2984](https://github.com/microsoft/TypeScript-go/issues/2984#issuecomment-4004322347)

## Activity Summary

### [Issue microsoft/TypeScript-go#2212](https://github.com/microsoft/TypeScript-go/issues/2212) (Open, `Domain: Emit`, **jakebailey**)

**Incorrect import elision when enum value references another enum from a different module**

*tsgo wrongly elides imports when an enum references values from another module's enum, causing undefined runtime errors.*

 * [12 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2212#issuecomment-3615034725) **thaoula** said "I have updated my original post because my cut down example was actually incorrect"
 * [12 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2212#issuecomment-3617371086) **a-tarasyuk** asked whether the extracted evaluator should evaluate the expression or preserve imports, noting that entity evaluation currently didn’t support alias resolution or import preservation
 * [12 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2212#issuecomment-3617384891) **jakebailey** explained that enums were initially handled without const inlining but recommended restoring the previous behavior
 * (today) **jakebailey** added label `Domain: Emit`, and assigned to **jakebailey**

### [Issue microsoft/TypeScript-go#2260](https://github.com/microsoft/TypeScript-go/issues/2260) (Open, `Domain: Editor`)

**Inherited methods not merging JSDoc comments**

*tsgo fails to merge inherited JSDoc comments into overridden methods, showing only new @remarks tags.*

 * [12 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2260#issuecomment-3628872763) **LukeAbby** indicated that the PR didn't fully work due to literal JSDoc concatenation and suggested restoring old behavior or adding an opt-in for merging docs with @inheritDoc
 * **jakebailey** added label `Domain: Editor`
 * [11 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2260#issuecomment-3645658993) **a-tarasyuk** provided a test case and sample QuickInfo output demonstrating JSDoc inheritDocTag behavior
 * [today](https://github.com/microsoft/TypeScript-go/issues/2260#issuecomment-4001095282) **a-tarasyuk** said "I’m still unclear about what the expected behavior should be. Should we consider this as working as by design?  "

### [Issue microsoft/TypeScript-go#2265](https://github.com/microsoft/TypeScript-go/issues/2265) (Closed)

**Sourcemap generation consuming significant resources while sourcemaps are disabled**

*tsgo build spends the majority of CPU time in source map emission functions despite sourceMap and declarationMap being disabled.*

 * [12 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2265#issuecomment-3629282410) **aem** explained that the issue was caused by a misconfigured project reference and asked whether to keep the issue open or rename/close and open a new one to address source map generation performance costs
 * [12 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2265#issuecomment-3629367097) **jakebailey** noted that another repo with dts source map emit enabled would speed progress, mentioned TS string encoding benefits, and acknowledged the code was wrong
 * [12 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2265#issuecomment-3629373435) **aem** said "Makes sense. Let me see if I can minimally repro the performance diff between "declarationMaps": true and "declarationMaps": false and I'll update here if I can do so"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2265#issuecomment-4001798597) **jakebailey** said "I think this should be fixed as of #2872."
 * (today) **jakebailey** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/issues/2265#issuecomment-4002117072) **aem** said "Indeed, looks like with the old setup we're down from 113s to 57s in our repo, thanks! Sorry I dropped the ball on getting you a repro, glad someone else was able to help out"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2265#issuecomment-4002217738) **jakebailey** said "Hm, isn't that still pretty bad?"

### [Issue microsoft/TypeScript-go#2457](https://github.com/microsoft/TypeScript-go/issues/2457) (Open)

**Proposal: Prettified type display in hover output**

*Add optional settings to display prettified, expanded types in hover output for better readability.*

 * created by **sQVe**
 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/2457#issuecomment-3974008251) **EvgenyOrekhov** stated that VS Code now supports this natively and showed how to increase hover verbosity by clicking '+'
 * [later](https://github.com/microsoft/TypeScript-go/issues/2457#issuecomment-4005963689) **rubnogueira** said "This is part of TypeScript 5.9: https://devblogs.microsoft.com/typescript/announcing-typescript-5-9-beta/#expandable-hovers-(preview) but it's not implemented in tsgo."

### [Issue microsoft/TypeScript-go#2675](https://github.com/microsoft/TypeScript-go/issues/2675) (Closed)

**Untitled files only respect \`javascript\.\` settings**

*Untitled TypeScript files ignore typescript.inlayHints settings under tsgo and only respect JavaScript inlay hint configurations.*

 * created by **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2675#issuecomment-4001789857) **jakebailey** said "This should now be fixed due to the fallback setting behavior."
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2767](https://github.com/microsoft/TypeScript-go/issues/2767) (Closed, **jakebailey**, **Copilot**)

**Spreading variable of \`RegExpIndicesArray\` type will cause error**

*Spreading a RegExpIndicesArray in tsgo triggers a spurious iterator error that does not occur in TypeScript 6.0.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2767#issuecomment-3899836262) **jakebailey** said "The reason the website differs is silly. It was stuck at 6.0.0-dev.20260204, two days before the mentioned PR was merged. Builds are running to fix that now."
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2767#issuecomment-3900185050) **ahejlsberg** explained that their elaboration logic drills down to the precise syntax node to reveal that `undefined` isn't iterable instead of showing the entire union type
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2767#issuecomment-3900198768) **jakebailey** noted that neither option shows a tower of elaboration or a standard assignability error and provided a Playground link
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2778](https://github.com/microsoft/TypeScript-go/issues/2778) (Closed, `Domain: Editor`)

**\[ServerErrors\]\[TypeScript\] linux\-x64\-7\.0\.0\-dev\.20260212\.1 vs **

*The linux-x64-7.0.0-dev.20260212.1 TypeScript error-delta pipeline run experienced 158 timeouts, five git clone failures, and one unknown failure while analyzing 300 popular repositories.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2778#issuecomment-3894722715) **typescript-bot** reported server connection closure prematurely and provided diagnostics including affected repository, LSP requests, and repro steps
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2778#issuecomment-3898324478) **gabritto** suggested that server connection closed prematurely errors were due to OOMs based on pipeline logs
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2778#issuecomment-3898535476) **gabritto** summarized Copilot-produced possible existing crash issues and their statuses in a table
 * **jakebailey** added label `Domain: Editor`

### [Issue microsoft/TypeScript-go#2780](https://github.com/microsoft/TypeScript-go/issues/2780) (Open, `Domain: Editor`, `Needs More Info`, **andrewbranch**)

**High memory consumption in a large pnpm monorepo**

*PR #2502 causes minor edits in a large pnpm monorepo to spike the TypeScript extension memory from ~700MB to ~35GB.*

 * [today](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-3996536169) **goloveychuk** proposed adding a condition to skip package names starting with '.' in extractPackages to prevent .store-fuse-unplugged from being included
 * [today](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-3996574831) **jakebailey** asked the reporter to test with the latest nightly, noting that #2965 contained fixes
 * [today](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-3996771372) **goloveychuk** confirmed the fix works in the main branch, analysed the root cause of package name resolution falling back to .store-fuse-unplugged due to a nested package.json without a name, and suggested improving the search logic
 * [today](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-3998781784) **andrewbranch** said "Can others who were having issues try the latest nightly and see if it fixes things for you as well?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-4002312683) **shinichy** said "I tried the latest nightly, but it doesn't fix the issue for me."
 * [later](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-4005082708) **justinsmid** reported that after upgrading to the latest nightly yesterday afternoon, they have not observed memory usage spikes though lacking a consistent reproduction path
 * [later](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-4005159769) **dbrxnds** reported memory usage improvements with averages of 3-5GB and reduced peaks to 10-15GB, clearing faster than the previous 40-50GB

### [Issue microsoft/TypeScript-go#2829](https://github.com/microsoft/TypeScript-go/issues/2829) (Closed, `Domain: Editor`)

**\[ServerErrors\]\[TypeScript\] linux\-x64\-7\.0\.0\-dev\.20260218\.1 vs **

*The linux-x64-7.0.0-dev.20260218.1 TypeScript pipeline reported 76 interesting changes, 59 unchanged results, 6 clone failures, 158 timeouts, and 1 unknown failure when analyzing 300 popular repositories.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2829#issuecomment-3924076907) **typescript-bot** reported a server connection closed prematurely error on facebook/docusaurus with related logs, requests, and reproduction steps
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2829#issuecomment-3924126975) **gabritto** said ""panic handling request completionItem/resolve: completion list needs auto imports" is in #2827"
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2829#issuecomment-3924192677) **gabritto** noted that 'Server connection closed prematurely: undefined' errors seemed to be OOMs and said they would update the message accordingly, pointed to PR #2826 for debugging replays, and described manual fixes to replay files due to a fuzzer issue
 * **jakebailey** added label `Domain: Editor`

### [Issue microsoft/TypeScript-go#2871](https://github.com/microsoft/TypeScript-go/issues/2871) (Closed, `Domain: Editor`)

**\[ServerErrors\]\[TypeScript\] linux\-x64\-7\.0\.0\-dev\.20260222\.1 vs **

*The linux-x64 TypeScript 7.0.0-dev pipeline run encountered multiple errors—including timeouts, clone failures, and unknown failures—while analyzing popular repositories.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/2871#issuecomment-3941898753) **typescript-bot** reported a server connection closed prematurely error and provided affected repos, artifact links, request logs, and repro steps
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/2871#issuecomment-3941898776) **typescript-bot** reported a premature server connection closure error and supplied reproduction steps for the HumanSignal/label-studio repo
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/2871#issuecomment-3941898803) **typescript-bot** reported that the server connection closed prematurely with undefined and listed affected repos and logs
 * **jakebailey** added label `Domain: Editor`

### [Issue microsoft/TypeScript-go#2881](https://github.com/microsoft/TypeScript-go/issues/2881) (Closed, `Domain: Editor`)

**\[ServerErrors\]\[JavaScript\] linux\-x64\-7\.0\.0\-dev\.20260223\.1 vs **

*The linux-x64-7.0.0-dev.20260223.1 pipeline on 300 TypeScript repos detected three interesting changes, two clone failures, nineteen timeouts, and three unknown failures.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/2881#issuecomment-3947789231) **typescript-bot** reported a panic during cross-project handling for textDocument/references due to an unexpected KindIdentifier in a KindFunctionExpression's trivia
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/2881#issuecomment-3947789265) **typescript-bot** reported server connection closed prematurely with undefined error and listed the affected repository and recent requests
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/2881#issuecomment-3947789311) **typescript-bot** reported a server connection closed prematurely error with affected repository details, last requests, and repro steps
 * **jakebailey** added label `Domain: Editor`

### [Issue microsoft/TypeScript-go#2917](https://github.com/microsoft/TypeScript-go/issues/2917) (Closed, `Crash`, **ahejlsberg**)

**Memory leak when using recursive type with template literal**

*A recursive template literal conditional type causes the TypeScript compiler to leak memory and OOM.*

 * created by **james-pre**
 * **james-pre** added label `Crash`
 * **ahejlsberg** assigned to **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2917#issuecomment-4001236879) **ahejlsberg** noted that the repro caused "Excessive stack depth comparing types XXX and YYY" errors, suggested adding a truncation length check in NodeBuilderImpl.conditionalTypeToTypeNode, and announced a forthcoming PR
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#2924](https://github.com/microsoft/TypeScript-go/pull/2924) (Closed)

**Delete empty dirs in baseline\-accept task**

*Add automatic deletion of empty directories in the baseline-accept task to streamline comparison results.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2931](https://github.com/microsoft/TypeScript-go/pull/2931) (Closed, **gabritto**, **Copilot**)

**Port PR \#63200: Add symbol name to unsafe import error \(TS2883\)**

*Ports symbol name support in unsafe import error (TS2883) by updating SymbolTracker interface, implementations, and call sites.*

 * created by **Copilot**
 * (5 days ago) **Copilot** assigned to **Copilot**, **gabritto**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2931#issuecomment-3999860819) **jakebailey** said "https://github.com/microsoft/TypeScript/pull/63200"
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript-go#2934](https://github.com/microsoft/TypeScript-go/pull/2934) (Closed)

**fix\(2932\): handle parameter\-property ref to method with same name**

*Ensure parameter-property references to methods with the same name are resolved correctly.*

 * created by **a-tarasyuk**
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/2934#issuecomment-3986255673) **DanielRosenwasser** said "It seems with the latest commits, we're no longer testing find-all-refs on usages as well."
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/2934#issuecomment-3986428480) **a-tarasyuk** said "@DanielRosenwasser, I updated test to use ranges. Did you mean this, or were you referring to adding the additional cases?"
 * (today) **a-tarasyuk** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/2934#issuecomment-4001051841) **DanielRosenwasser** said "@a-tarasyuk you don't have to close the PR, I just wanted to spend a bit longer understanding it"
 * (later) **a-tarasyuk** reopened the issue

### [Issue microsoft/TypeScript-go#2935](https://github.com/microsoft/TypeScript-go/issues/2935) (Closed, `Crash`, **ahejlsberg**, **jakebailey**, **Copilot**)

**Stack overflow in type instantiation with recursive function and generic type params**

*A recursive generic camelCase transformation using type-fest triggers a tsgo stack overflow from v4.38.0 onward, while tsc compiles it.*

 * (4 days ago) **jakebailey** assigned to **jakebailey**, **ahejlsberg**
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/2935#issuecomment-3987301887) **jakebailey** mentioned that issue #2940 implied they were running out of stack where they hadn’t before and speculated this could be due to heavy stack allocation for performance unlike JS’s nursery allocations
 * [today](https://github.com/microsoft/TypeScript-go/issues/2935#issuecomment-3999733454) **ahejlsberg** identified that #1795 didn't fully port the changes, initiated PR #2979 to complete the port, and confirmed that it fixed the issue
 * [today](https://github.com/microsoft/TypeScript-go/issues/2935#issuecomment-4000819597) **ahejlsberg** said "Fixed by #2979. Closing."
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#2944](https://github.com/microsoft/TypeScript-go/pull/2944) (Open)

**\[draft\] more formatting tests **

*Add draft formatting tests to validate and troubleshoot the repository’s testing pipelines.*

 * created by **iisaduan**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2944#issuecomment-4001168893) **iisaduan** said "@typescript-bot test top 100"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2944#issuecomment-4001173930) **iisaduan** said "@typescript-bot test top100"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2944#issuecomment-4001174323) **typescript-bot** said "Hey @iisaduan, this PR is in an unmergable state, so is missing a merge commit to run against; please resolve conflicts and try again."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2944#issuecomment-4001359290) **iisaduan** said "@typescript-bot test top100"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2944#issuecomment-4001359480) **typescript-bot** reported that the top100 tests failed to queue due to validation errors or warnings

### [Issue microsoft/TypeScript-go#2945](https://github.com/microsoft/TypeScript-go/issues/2945) (Closed, `Domain: Editor`)

**\[ServerErrors\]\[TypeScript\] linux\-x64\-7\.0\.0\-dev\.20260301\.1 vs **

*Automated linux-x64-7.0.0-dev.20260301.1 build on 300 popular TypeScript repositories reported errors, timeouts, and clone failures.*

 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/2945#issuecomment-3981326660) **typescript-bot** reported a server connection closed prematurely error with undefined, listed affected repo, last requests, and repro steps
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/2945#issuecomment-3981326680) **typescript-bot** reported that the server connection closed prematurely with an undefined error and listed affected repos and recent requests
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/2945#issuecomment-3981326706) **typescript-bot** reported server connection closed prematurely and provided error details, affected repository links, recent requests, and repro steps
 * **jakebailey** added label `Domain: Editor`

### [PR microsoft/TypeScript-go#2946](https://github.com/microsoft/TypeScript-go/pull/2946) (Closed)

**Improve CommonJS support, round 2**

*Enable overlaying of type and namespace declarations on CommonJS export assignments, allow multiple module.exports unions, and align Corsa with Strada behavior*

 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2946#issuecomment-3992782126) **ahejlsberg** noted that the latest commits fixed the example issue but reported that nested module.exports assignments weren't handled by the declaration emitter and declined to fix it in this PR
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2946#issuecomment-3992862722) **weswigham** clarified that the corsa stub is unused and explained the need for new declaration emitter logic for non-top-level export assignments
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2946#issuecomment-3992889610) **jakebailey** said "I think we have been gradually backing off on that logic, as we discover more things that the reparser can't do (e.g., the defineProperties stuff)."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2946#issuecomment-4000555754) **ahejlsberg** recapped that they agreed to merge the PR and create a separate PR to issue errors when generating declaration files for CommonJS modules with unsupported constructs, including multiple module.exports assignments, nested module.exports assignments, nested exports.xxx assignments, and nested Object.defineProperty(module.exports) calls
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#2963](https://github.com/microsoft/TypeScript-go/pull/2963) (Open, **andrewbranch**, **Copilot**)

**Port FindNextToken and FindPrecedingToken from Go to TypeScript**

*Port findNextToken and findPrecedingToken from Go to the TypeScript AST package and validate behavior against Go baselines.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2963#issuecomment-3993748508) **Copilot** stated that formatting was completed in commit 12ef49c4
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2963#issuecomment-3994311130) **andrewbranch** said "@copilot see review feedback, failing tests, and carefully compare your implementation against tokens.go. Run tests and format before committing."
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2963#issuecomment-3994516934) **Copilot** described fixes implemented in commit a4777eb2 including always returning scanned tokens in findNextToken, adding scanner-based scanning in findRightmostValidToken, adding JSDoc support in findPrecedingTokenImpl, and removing an incorrect test
 * [today](https://github.com/microsoft/TypeScript-go/pull/2963#issuecomment-3998613280) **andrewbranch** proposed adding baseline generation to Go tests for FindNextToken and FindPrecedingToken and replacing manual TS tests with ones checking their behavior against Go baselines
 * [today](https://github.com/microsoft/TypeScript-go/pull/2963#issuecomment-3999209824) **andrewbranch** said "@copilot you were interrupted by an error but pushed your work in progress. Please continue."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2963#issuecomment-3999352126) **Copilot** reported passing baseline-based tests and described two bug fixes in findPrecedingTokenImpl and findRightmostValidToken

### [Issue microsoft/TypeScript-go#2964](https://github.com/microsoft/TypeScript-go/issues/2964) (Closed, `Domain: Editor`)

**\[ServerErrors\]\[JavaScript\] linux\-x64\-7\.0\.0\-dev\.20260303\.1 vs **

*The linux-x64-7.0.0-dev.20260303.1 CI run reported 12 notable changes among 216 successful analyses and various failures across 300 TypeScript repositories.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2964#issuecomment-3993188076) **typescript-bot** reported a 'server connection closed prematurely: undefined' error and included reproduction steps
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2964#issuecomment-3993188145) **typescript-bot** reported server connection closed prematurely error with repro steps and artifacts for videojs/video.js
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2964#issuecomment-3993188217) **typescript-bot** reported that the TS server connection closed prematurely with undefined error during analysis of mui/material-ui
 * **jakebailey** added label `Domain: Editor`

### [PR microsoft/TypeScript-go#2972](https://github.com/microsoft/TypeScript-go/pull/2972) (Closed)

**\[@typescript/api\] Add a few more checker APIs**

*Add TypeScript checker API methods for context sensitivity, type retrieval, base types, properties, index infos, constraints, and type arguments.*

 * created by **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#2974](https://github.com/microsoft/TypeScript-go/issues/2974) (Open, `Domain: Editor`)

**Missing auto\-import for subpath imports of other local packages**

*VS Code TypeScript auto-imports fail to recognize subpath imports from sibling local workspace packages.*

 * created by **psznm**
 * **psznm** added label `Domain: Editor`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2974#issuecomment-3999163817) **andrewbranch** said "I think this is “working as intended” because the other packages aren’t listed as dependencies. Does it work as you expect if you add them to pkg1's package.json "dependencies"?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2974#issuecomment-3999487766) **psznm** tried the suggested changes, added the dependency and moved imports, observed the package import suggestion appear but the subpath import suggestion remain missing

### [PR microsoft/TypeScript-go#2975](https://github.com/microsoft/TypeScript-go/pull/2975) (Closed)

**Fix document highlight panic on nested \`require\` destructuring**

*Prevent document highlight from panicking on nested require destructuring patterns.*

 * created by **Andarist**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2976](https://github.com/microsoft/TypeScript-go/pull/2976) (Closed)

**Preserve the original parameter\-list range when injecting reparsed \`this\` parameter**

*Preserve the original parameter-list range when injecting a reparsed this parameter to avoid crashes.*

 * created by **Andarist**
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript-go#2977](https://github.com/microsoft/TypeScript-go/pull/2977) (Closed)

**Add \`assert\` option to hereby**

*Introduce an assert flag to hereby to enable assertions in fuzzer builds without disabling optimizations.*

 * created by **gabritto**
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript-go#2978](https://github.com/microsoft/TypeScript-go/pull/2978) (Open, **andrewbranch**, **Copilot**)

**Fix auto\-import type modifier and formatting issues in type\-only import statements**

*Prevent auto-import from adding inline 'type' modifiers to type-only imports and fix formatting and indentation to match TypeScript*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2978#issuecomment-3999339974) **andrewbranch** suggested expanding the work’s scope to fix underlying formatting issues causing type-only import tests to fail and compare the implementation against _submodules/TypeScript
 * [today](https://github.com/microsoft/TypeScript-go/pull/2978#issuecomment-3999610825) **Copilot** fixed formatting issues in change tracker by adding missing spaces, implementing type-only specifier re-sorting, improving import specifier insertion, corrected tests, and removed three failing tests
 * [today](https://github.com/microsoft/TypeScript-go/pull/2978#issuecomment-3999848724) **andrewbranch** explained that generated fourslash tests cannot be modified directly and that the convertFourslash.mts script must be updated if preferences are missing
 * [today](https://github.com/microsoft/TypeScript-go/pull/2978#issuecomment-4000204118) **andrewbranch** said "@copilot+claude-opus-4.6 you got interrupted by an error; please continue"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2978#issuecomment-4000348236) **Copilot** added organizeImportsTypeOrder support to parseUserPreferences, regenerated tests, and fixed a multiline indentation bug in InsertNodeInListAfter
 * [today](https://github.com/microsoft/TypeScript-go/pull/2978#issuecomment-4000801195) **andrewbranch** said "@copilot+claude-opus-4.6 your infrastructure is very flaky today ☹️ Please pick up where you left off before there was an error"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2978#issuecomment-4000949474) **andrewbranch** said "@copilot+claude-opus-4.6 keep trying 😕 "
 * [today](https://github.com/microsoft/TypeScript-go/pull/2978#issuecomment-4001282331) **andrewbranch** said "@copilot I would stop this if you didn't keep making good progress each time, but you are, so keep going"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2978#issuecomment-4001356213) **Copilot** described changes in commit 31661e1: aligned InsertNodeInListAfter and InsertImportSpecifierAtIndex implementations with TS, removed workaround indentation prefix, and confirmed all tests passed
 * [today](https://github.com/microsoft/TypeScript-go/pull/2978#issuecomment-4001375518) **andrewbranch** said "@copilot+claude-opus-4.6 you added a bunch to crashingTests.txt. Either it's out of date, or you need to fix the crashes."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2978#issuecomment-4001504251) **Copilot** fixed crashes in FindNextToken by using tokenFullStart to match TS behavior, causing all 12 previously crashing tests to work (11 removed from both crashing and failing lists and one retaining a wrong-answer failure)

### [PR microsoft/TypeScript-go#2979](https://github.com/microsoft/TypeScript-go/pull/2979) (Closed, **ahejlsberg**, **Copilot**)

**Complete port of TS PR \#61668: revert \#57403 remnants missing from Go port**

*The Go port of TypeScript PR #61668 missed reverting PR #57403 changes, leaving dead checker code.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2979#issuecomment-4000320601) **ahejlsberg** said "I have manually verified that this adds the missing parts of TS PR #61668."
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#2980](https://github.com/microsoft/TypeScript-go/pull/2980) (Closed)

**Add comments, shebang, chmod scripts in repo**

*Add shebang lines, comments, and executable permissions to scripts so Copilot stops running them with tsx.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2980#issuecomment-3999886156) **jakebailey** noted wanting to add the `DO NOT EDIT` header to fourslash tests and planned to handle the associated tooling fixes in a separate PR
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2981](https://github.com/microsoft/TypeScript-go/pull/2981) (Closed)

**Make auto\-import test more realistic**

*Updated the auto-import test to more accurately replicate the failure scenario without relying on a nameless package.json*

 * created by **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#2982](https://github.com/microsoft/TypeScript-go/issues/2982) (Closed)

**Publish to Open VSX**

*Publish the TypeScriptTeam.native-preview extension to Open VSX so users can receive automatic updates.*

 * created by **peaklabs-dev**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2982#issuecomment-4000668158) **jakebailey** linked two related issues
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2983](https://github.com/microsoft/TypeScript-go/pull/2983) (Closed)

**Add DO NOT EDIT comment to generated fourslash files**

*Add a “DO NOT EDIT” comment to generated fourslash files to discourage accidental modifications in PRs.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2983#issuecomment-4000774320) **jakebailey** said "Ugh, once again, hit by the DO NOT EDIT formatting exception."
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2984](https://github.com/microsoft/TypeScript-go/issues/2984) (Open, `Domain: Editor`)

**Auto\-import with subpath imports always prioritizes relative imports**

*VSCode TypeScript auto-import suggestions ignore package.json subpath mappings and default to relative paths even when configured for shortest or non-relative imports*

 * created by **danilofuchs**
 * **danilofuchs** added label `Domain: Editor`
 * [later](https://github.com/microsoft/TypeScript-go/issues/2984#issuecomment-4004322347) **psznm** suggested that moduleResolution nodenext might cause node imports to be looked up in the build directory and asked if the build/* did not contain the import, linking to a related issue

### [Issue microsoft/TypeScript-go#2985](https://github.com/microsoft/TypeScript-go/issues/2985) (Open, `Crash`)

**panic: "project bucket missing" in completions**

*Code completions panic with 'project bucket missing' error due to unprepared autoimport registry.*

 * created by **DanielRosenwasser**
 * **DanielRosenwasser** added label `Crash`

### [PR microsoft/TypeScript-go#2986](https://github.com/microsoft/TypeScript-go/pull/2986) (Open, **andrewbranch**, **Copilot**)

**Add \`symbol\.getExportSymbol\(\)\` and export \`Type\` from API**

*Add asynchronous and synchronous getExportSymbol() methods to the Symbol API and re-export Type in API modules.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **andrewbranch**

### [PR microsoft/TypeScript-go#2987](https://github.com/microsoft/TypeScript-go/pull/2987) (Closed)

**Add truncation length check in \`conditionalTypeToTypeNode\`**

*Add a truncation length check in the conditionalTypeToTypeNode function to prevent generating excessively long type representations.*

 * created by **ahejlsberg**
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#2988](https://github.com/microsoft/TypeScript-go/issues/2988) (Open, `Domain: Editor`)

**\[ServerErrors\]\[TypeScript\] main vs **

*TypeScript main pipeline encountered server errors in 62 of 300 repos and detected 163 interesting changes among the 238 analyzed.*

 * created by **typescript-bot**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4001335728) **typescript-bot** reported a panic with debug failure 'False expression: Token end is child end' during a textDocument/formatting request
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4001335778) **typescript-bot** reported a panic during textDocument/formatting due to a debug failure assertion
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4001335830) **typescript-bot** reported a panic in handling textDocument/prepareCallHierarchy due to a failed assertion for a reference node
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4001335883) **typescript-bot** reported a panic during handling of textDocument/rangeFormatting due to a debug failure
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4001335927) **typescript-bot** reported a panic during cross-project handling of a textDocument/implementation request with a Debug failure and accompanying stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4001335971) **typescript-bot** reported a panic in textDocument/rangeFormatting due to bad line number
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4001336009) **typescript-bot** reported a panic during textDocument/rangeFormatting due to debug failure: False expression: Token end is child end
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4001336058) **typescript-bot** provided a panic stack trace for textDocument/rangeFormatting showing a debug failure: False expression: Token end is child end
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4001336111) **typescript-bot** reported a panic in textDocument/rangeFormatting due to a debug assertion failure: Token end is child end
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4001336156) **typescript-bot** reported a panic with 'False expression: Token end is child end' during textDocument/rangeFormatting including a Go stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4001336206) **typescript-bot** reported a panic during textDocument/formatting due to a failed assertion 'Token end is child end' with stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4001336249) **typescript-bot** reported a panic with debug failure 'False expression: Token end is child end' during textDocument/rangeFormatting
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4001336302) **typescript-bot** reported a panic with a debug failure during textDocument/formatting
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4001336380) **typescript-bot** reported a panic during textDocument/rangeFormatting request due to a debug assertion failure
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4001336526) **typescript-bot** reported a panic with debug failure during textDocument/rangeFormatting, including a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4001336573) **typescript-bot** reported a panic handling request textDocument/rangeFormatting due to a debug failure 'Token end is child end'
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4001336607) **typescript-bot** reported a panic handling a textDocument/rangeFormatting request due to an internal debug assertion failure 'Token end is child end'
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4001336656) **typescript-bot** reported a panic in textDocument/rangeFormatting due to a debug failure (False expression: Token end is child end)
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4001336701) **typescript-bot** reported a panic during textDocument/rangeFormatting due to a debug failure 'Token end is child end' and included a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4001336743) **typescript-bot** reported a panic handling request textDocument/rangeFormatting due to a debug failure: Token end is child end, including a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4001336781) **typescript-bot** reported a panic in textDocument/formatting due to a debug failure: False expression: Token end is child end
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4001336810) **typescript-bot** reported a panic handling request textDocument/rangeFormatting due to debug failure 'False expression: Token end is child end'
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4001336856) **typescript-bot** reported a panic due to a debug assertion failure while handling textDocument/rangeFormatting
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4001336888) **typescript-bot** reported a panic handling request textDocument/rangeFormatting due to a debug failure "False expression: Token end is child end" and included a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4001336924) **typescript-bot** reported a panic handling request textDocument/rangeFormatting due to debug failure: False expression: Token end is child end
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4001336956) **typescript-bot** reported a panic handling a textDocument/rangeFormatting request due to a debug failure in token end child boundaries
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4001337008) **typescript-bot** reported a panic in textDocument/rangeFormatting due to a debug failure False expression: Token end is child end
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4001337062) **typescript-bot** reported a panic and stack trace during textDocument/rangeFormatting due to a failed debug assertion
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4001337109) **typescript-bot** reported a panic during cross-project handling of textDocument/implementation due to a debug failure
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4001337151) **typescript-bot** reported a panic handling textDocument/rangeFormatting due to a debug failure "Token end is child end"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4001337211) **typescript-bot** reported a panic handling request textDocument/rangeFormatting due to debug failure 'Token end is child end' and included the stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4001337338) **typescript-bot** reported a panic handling the textDocument/rangeFormatting request due to a debug failure with a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4001337381) **typescript-bot** reported a panic during textDocument/formatting with a debug failure and provided a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4001337428) **typescript-bot** reported a panic during handling of textDocument/rangeFormatting due to a debug failure: Token end is child end
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4001337474) **typescript-bot** reported a panic handling a textDocument/rangeFormatting request with a false expression and stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4001337510) **typescript-bot** reported a panic during textDocument/rangeFormatting with debug failure False expression: Token end is child end and stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4001337556) **typescript-bot** reported a panic during textDocument/rangeFormatting due to a debug failure "Token end is child end"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4001337612) **typescript-bot** reported a panic during textDocument/rangeFormatting due to a false expression assertion
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4001337640) **typescript-bot** showed a panic stack trace for textDocument/rangeFormatting indicating a false expression 'Token end is child end'
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4001337679) **typescript-bot** reported a debug failure panic in textDocument/rangeFormatting with a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4001337708) **typescript-bot** reported a panic during textDocument/rangeFormatting due to a debug assertion failure 'Token end is child end'
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4001337742) **typescript-bot** reported a panic handling textDocument/rangeFormatting request due to a false expression: Token end is child end
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4001337777) **typescript-bot** reported a panic when processing textDocument/formatting request
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4001337805) **typescript-bot** showed a panic handling textDocument/formatting due to a failed debug assertion: Token end is child end
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4001337852) **typescript-bot** reported a panic handling textDocument/rangeFormatting with debug failure: False expression: Token end is child end
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4001337902) **typescript-bot** reported a panic during textDocument/formatting request due to a debug failure ('Token end is child end')
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4001337958) **typescript-bot** reported a panic during handling textDocument/rangeFormatting due to a debug failure 'False expression: Token end is child end'
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4001337986) **typescript-bot** reported a panic in textDocument/rangeFormatting due to a failed assertion and included a Go stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4001338040) **typescript-bot** reported an internal panic during textDocument/rangeFormatting due to failed assertion 'Token end is child end'
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4001338083) **typescript-bot** reported a panic during textDocument/rangeFormatting with a debug failure 'Token end is child end' and provided a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4001338129) **typescript-bot** reported a panic due to debug failure 'Token end is child end' when handling textDocument/rangeFormatting, including stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4001338179) **typescript-bot** described a panic with debug failure during a textDocument/rangeFormatting request
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4001338285) **typescript-bot** reported a panic handling textDocument/rangeFormatting request with a debug failure and accompanying stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4001338397) **typescript-bot** reported a debug failure panic with stack trace during textDocument/formatting
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4001338445) **typescript-bot** reported a panic during textDocument/rangeFormatting due to a debug failure assertion
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4001338494) **typescript-bot** reported a panic during textDocument/rangeFormatting due to a debug false expression: Token end is child end
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4001338537) **typescript-bot** reported a panic when handling a textDocument/rangeFormatting request due to a Debug failure
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4001338578) **typescript-bot** reported a panic handling textDocument/formatting request due to a failed assertion 'Token end is child end'
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4001338611) **typescript-bot** reported a panic handling textDocument/rangeFormatting with a debug failure and stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4001338662) **typescript-bot** reported a panic during textDocument/rangeFormatting due to a debug failure 'False expression: Token end is child end' and included a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4001338707) **typescript-bot** reported a panic error during textDocument/rangeFormatting with a debug failure and stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4001338742) **typescript-bot** reported a panic during textDocument/rangeFormatting with a failed assertion 'Token end is child end'
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4001338781) **typescript-bot** reported a panic with a debug failure during textDocument/rangeFormatting
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4001338806) **typescript-bot** reported a debug failure panic during textDocument/rangeFormatting
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4001338845) **typescript-bot** reported a panic in textDocument/rangeFormatting due to a debug failure of 'False expression: Token end is child end'
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4001338872) **typescript-bot** reported a panic during textDocument/implementation handling due to a debug failure and included a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4001338901) **typescript-bot** reported panic handling request textDocument/rangeFormatting with debug failure 'False expression: Token end is child end'
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4001338933) **typescript-bot** reported a panic handling request textDocument/rangeFormatting due to a debug failure ‘False expression: Token end is child end’, including a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4001338979) **typescript-bot** reported a panic during textDocument/formatting with a debug failure and included a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4001339018) **typescript-bot** reported a panic during textDocument/rangeFormatting due to a false expression (`Token end is child end`), including a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4001339097) **typescript-bot** reported a panic handling the textDocument/rangeFormatting request due to a debug failure (“False expression: Token end is child end”)
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4001339206) **typescript-bot** reported a panic handling textDocument/definition due to a debug assertion failure 'start and end should be in same file'
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4001339271) **typescript-bot** reported a panic handling textDocument/definition request due to a debug assertion failure
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4001339325) **typescript-bot** reported a panic handling textDocument/definition request due to a false expression: start and end should be in same file
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4001339372) **typescript-bot** reported a panic handling textDocument/formatting with a debug failure and stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4001339419) **typescript-bot** reported a panic handling a rangeFormatting request due to a debug failure 'Token end is child end' and provided a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4001339469) **typescript-bot** reported a debug failure panic during textDocument/rangeFormatting
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4001339501) **typescript-bot** reported a panic handling request for textDocument/rangeFormatting due to a debug failure
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4001339552) **typescript-bot** reported a panic during textDocument/rangeFormatting with a debug failure and stack trace
 * **jakebailey** added label `Domain: Editor`

### [PR microsoft/TypeScript-go#2989](https://github.com/microsoft/TypeScript-go/pull/2989) (Closed)

**Fixed a crash when reformatting \`JsxNamespacedName\`**

*Resolves a crash when reformatting JsxNamespacedName nodes in the code formatter.*

 * created by **Andarist**

### [Issue microsoft/TypeScript-go#2990](https://github.com/microsoft/TypeScript-go/issues/2990) (Closed)

**"function\(\)" in @param JSDoc tag is not parsed properly**

*tsgo fails to parse JSDoc @param function() syntax, yielding a '}' expected error, unlike TypeScript 6.*

 * created by **rwalle**
 * [later](https://github.com/microsoft/TypeScript-go/issues/2990#issuecomment-4005913960) **jakebailey** mentioned that the syntax had been removed and provided an updated example
 * (later) **rwalle** closed the issue

