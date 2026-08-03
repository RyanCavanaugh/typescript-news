# Report for 2026-07-30 (Thursday, July 30th, 2026)

9 different users commented on 21 different issues.

## Recommended Actions

 * Response Recommended
    * @typescript-automation[bot] provided perf run results as requested in [microsoft/TypeScript-go#4786](https://github.com/microsoft/TypeScript-go/pull/4786#issuecomment-5136330132)
    * @typescript-automation[bot] provided perf run results as requested in [microsoft/TypeScript-go#4786](https://github.com/microsoft/TypeScript-go/pull/4786#issuecomment-5138487457)
    * @typescript-automation[bot] provided perf run results as requested in [microsoft/TypeScript-go#4797](https://github.com/microsoft/TypeScript-go/pull/4797#issuecomment-5136541195)
    * @typescript-automation[bot] provided performance run results as requested in [microsoft/TypeScript-go#4798](https://github.com/microsoft/TypeScript-go/pull/4798#issuecomment-5136183114)
    * @typescript-automation[bot] reported a panic during JSX attribute transformation in [microsoft/TypeScript-go#4801](https://github.com/microsoft/TypeScript-go/issues/4801#issuecomment-5137228627)
    * @typescript-automation[bot] reported a panic in textDocument/diagnostic handling in [microsoft/TypeScript-go#4801](https://github.com/microsoft/TypeScript-go/issues/4801#issuecomment-5137228670)
    * @typescript-automation[bot] reported a panic in textDocument/diagnostic in [microsoft/TypeScript-go#4801](https://github.com/microsoft/TypeScript-go/issues/4801#issuecomment-5137228731)
    * @typescript-automation[bot] reported a panic runtime error that should be investigated in [microsoft/TypeScript-go#4801](https://github.com/microsoft/TypeScript-go/issues/4801#issuecomment-5137228787)
    * @typescript-automation[bot] reported a panic in the textDocument/diagnostic request in [microsoft/TypeScript-go#4801](https://github.com/microsoft/TypeScript-go/issues/4801#issuecomment-5137228959)
    * @typescript-automation[bot] reported panic in textDocument/diagnostic request in [microsoft/TypeScript-go#4801](https://github.com/microsoft/TypeScript-go/issues/4801#issuecomment-5137229005)
    * @typescript-automation[bot] reported a server connection closed prematurely error in [microsoft/TypeScript-go#4801](https://github.com/microsoft/TypeScript-go/issues/4801#issuecomment-5137229044)
    * @typescript-automation[bot] reported server connection closed prematurely error in [microsoft/TypeScript-go#4801](https://github.com/microsoft/TypeScript-go/issues/4801#issuecomment-5137229130)
    * @typescript-automation[bot] reported a server connection error requiring investigation in [microsoft/TypeScript-go#4801](https://github.com/microsoft/TypeScript-go/issues/4801#issuecomment-5137229182)
    * @typescript-automation[bot] reported server connection closed prematurely error for TriliumNext/Trilium in [microsoft/TypeScript-go#4801](https://github.com/microsoft/TypeScript-go/issues/4801#issuecomment-5137229231)
    * @typescript-automation[bot] reported server connection closed prematurely for babel/babel in [microsoft/TypeScript-go#4801](https://github.com/microsoft/TypeScript-go/issues/4801#issuecomment-5137229281)
    * @typescript-automation[bot] reported a panic in textDocument/signatureHelp due to a nil pointer dereference in [microsoft/TypeScript-go#4801](https://github.com/microsoft/TypeScript-go/issues/4801#issuecomment-5137229418)
    * @typescript-automation[bot] reported a panic during textDocument/diagnostic in [microsoft/TypeScript-go#4801](https://github.com/microsoft/TypeScript-go/issues/4801#issuecomment-5137229469)
    * @typescript-automation[bot] reported a panic in textDocument/diagnostic for honojs/hono in [microsoft/TypeScript-go#4801](https://github.com/microsoft/TypeScript-go/issues/4801#issuecomment-5137229548)
    * @typescript-automation[bot] reported a panic in textDocument/diagnostic with repro information in [microsoft/TypeScript-go#4801](https://github.com/microsoft/TypeScript-go/issues/4801#issuecomment-5137229621)

## Activity Summary

### [Issue microsoft/TypeScript-go#4380](https://github.com/microsoft/TypeScript-go/issues/4380) (Closed, `Needs Investigation`, **johnfav03**)

**\[ServerErrors\]\[TypeScript\] main vs **

*Server errors occurred in the TypeScript main branch pipeline while analyzing 300 popular GitHub repositories, causing timeouts and other failures.*

 * **RyanCavanaugh** added to milestone `Post-7.0`
 * (1 month ago) **johnfav03** closed the issue
 * (3 weeks ago) **johnfav03** reopened the issue
 * (today) **johnfav03** closed the issue

### [Issue microsoft/TypeScript-go#4459](https://github.com/microsoft/TypeScript-go/issues/4459) (Closed, `Needs Investigation`, **johnfav03**)

**\[ServerErrors\]\[TypeScript\] main vs **

*The TypeScript main branch pipeline analyzed 300 repositories and reported 12 changes alongside timeouts, clone failures, and other errors.*

 * (3 weeks ago) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `Post-7.0`, and assigned to **johnfav03**
 * (today) **johnfav03** closed the issue

### [Issue microsoft/TypeScript-go#4532](https://github.com/microsoft/TypeScript-go/issues/4532) (Closed, `Needs Investigation`, **johnfav03**)

**\[ServerErrors\]\[TypeScript\] main vs **

*The main branch's pipeline analyzing 300 popular TypeScript repositories detected 11 interesting changes and encountered errors, timeouts, and cloning failures.*

 * (3 weeks ago) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.1`, and assigned to **johnfav03**
 * (today) **johnfav03** closed the issue

### [PR microsoft/TypeScript-go#4555](https://github.com/microsoft/TypeScript-go/pull/4555) (Open)

**Add batched version for several API functions\.**

*Add batched versions of several API functions to reduce IPC overhead and improve performance.*

 * created by **dragomirtitian**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4555#issuecomment-5129174620) **dragomirtitian** agreed that a generic batching API would be useful, noted that their sync API use precludes next-tick batching, and described their existing batching library
 * [today](https://github.com/microsoft/TypeScript-go/pull/4555#issuecomment-5134149432) **weswigham** explained that using a single checker/LS instance for the whole batch caches diagnostics and negates benefits of a bespoke entrypoint

### [PR microsoft/TypeScript-go#4655](https://github.com/microsoft/TypeScript-go/pull/4655) (Closed)

**Fix stack overflow in \`getExplicitTypeOfSymbol\(\)\` for self\-referential \`for\.\.\.of\`**

*A self-referential for…of loop where the loop variable iterates over itself causes unbounded recursion in getExplicitTypeOfSymbol and leads to a stack overflow.*

 * created by **johnfav03**
 * (today) **johnfav03** closed the issue

### [Issue microsoft/TypeScript-go#4713](https://github.com/microsoft/TypeScript-go/issues/4713) (Closed, `Needs Investigation`, **johnfav03**)

**tsconfig/jsconfig diagnostic doesn't refresh after file saved**

*tsgo fails to refresh tsconfig/jsconfig diagnostics after saving compilerOptions changes.*

 * (2 days ago) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `Post-7.0`, and assigned to **johnfav03**
 * (today) **johnfav03** closed the issue

### [PR microsoft/TypeScript-go#4739](https://github.com/microsoft/TypeScript-go/pull/4739) (Closed)

**Refresh config file diagnostics when a config file is saved**

*Saving tsconfig or jsconfig files now triggers a debounced snapshot update to immediately refresh diagnostics.*

 * created by **UditDewan**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4739#issuecomment-5136455638) **johnfav03** said "Closing in favor of #4799 "
 * (today) **johnfav03** closed the issue

### [PR microsoft/TypeScript-go#4781](https://github.com/microsoft/TypeScript-go/pull/4781) (Closed)

**Optimize \`narrowTypeByEquality\` and \`narrowTypeBySwitchOnDiscriminant\`**

*Improve performance of control flow analysis by optimizing narrowTypeByEquality and narrowTypeBySwitchOnDiscriminant functions.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4781#issuecomment-5124768102) **ahejlsberg** said "@typescript-bot perf test this faster"
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4781#issuecomment-5124768620) **typescript-automation[bot]** reported jobs starting and provided a status table with links to build and results
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4781#issuecomment-5125362369) **typescript-automation[bot]** provided the performance run results comparing baseline to pr
 * [today](https://github.com/microsoft/TypeScript-go/pull/4781#issuecomment-5135962621) **ahejlsberg** disputed the need for regression coverage for intersection constituents in the primitive-union guard
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#4786](https://github.com/microsoft/TypeScript-go/pull/4786) (Open)

**Shrink \`ast\.Symbol\` from 96 to 80 bytes**

*Move unused ast.Symbol fields into a lazily allocated extra struct to shrink symbol size and reduce memory usage.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4786#issuecomment-5118975538) **jakebailey** said "@typescript-bot perf test this"
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4786#issuecomment-5118976636) **typescript-automation[bot]** started build jobs and posted links to status and results
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4786#issuecomment-5119351637) **typescript-automation[bot]** provided the performance run results requested by @jakebailey
 * [today](https://github.com/microsoft/TypeScript-go/pull/4786#issuecomment-5136115169) **jakebailey** reran perf tests after tweaking benchstat math
 * [today](https://github.com/microsoft/TypeScript-go/pull/4786#issuecomment-5136115883) **typescript-automation[bot]** updated CI status with build and results links
 * [today](https://github.com/microsoft/TypeScript-go/pull/4786#issuecomment-5136330132) **typescript-automation[bot]** posted the requested performance run results comparing baseline and PR metrics
 * [today](https://github.com/microsoft/TypeScript-go/pull/4786#issuecomment-5137698676) **jakebailey** requested the typescript-bot to run a performance test with isolation enabled
 * [today](https://github.com/microsoft/TypeScript-go/pull/4786#issuecomment-5137699345) **typescript-automation[bot]** posted automated build status update
 * [today](https://github.com/microsoft/TypeScript-go/pull/4786#issuecomment-5138121016) **typescript-automation[bot]** reported the requested performance run results including a comparison of compilation metrics
 * [today](https://github.com/microsoft/TypeScript-go/pull/4786#issuecomment-5138267278) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4786#issuecomment-5138267835) **typescript-automation[bot]** announced start of performance tests and linked to build status and results
 * [today](https://github.com/microsoft/TypeScript-go/pull/4786#issuecomment-5138487457) **typescript-automation[bot]** posted the requested perf run results including a detailed comparison report

### [PR microsoft/TypeScript-go#4796](https://github.com/microsoft/TypeScript-go/pull/4796) (Closed)

**Fix O\(K^2\) OOM issue in go\-to\-implementation**

*Deduplicate go-to-implementation worklist entries to reduce memory complexity from O(K^2) to O(K).*

 * created by **johnfav03**
 * (today) **johnfav03** closed the issue

### [PR microsoft/TypeScript-go#4797](https://github.com/microsoft/TypeScript-go/pull/4797) (Open)

**Split heritage clause expression and type nodes**

*Propose splitting heritage clause nodes into distinct expression and type variants to accurately represent type space usage in the AST*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4797#issuecomment-5135975688) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4797#issuecomment-5135976418) **typescript-automation[bot]** announced start of perf test CI jobs and included status links
 * [today](https://github.com/microsoft/TypeScript-go/pull/4797#issuecomment-5136157447) **Gerrit0** acknowledged that there were two cases he hadn't considered before and agreed it was a good idea
 * [today](https://github.com/microsoft/TypeScript-go/pull/4797#issuecomment-5136541195) **typescript-automation[bot]** provided the requested performance run results

### [PR microsoft/TypeScript-go#4798](https://github.com/microsoft/TypeScript-go/pull/4798) (Closed)

**Avoid temporary composite mapper allocations**

*Avoiding temporary composite mapper allocations reduced runtime by 2.7%, peak RSS by 5.5%, and memory allocations by 21%.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4798#issuecomment-5135950642) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4798#issuecomment-5135951442) **typescript-automation[bot]** announced that performance test jobs had started and provided status and results links
 * [today](https://github.com/microsoft/TypeScript-go/pull/4798#issuecomment-5136183114) **typescript-automation[bot]** reported the results of the requested performance run

### [PR microsoft/TypeScript-go#4799](https://github.com/microsoft/TypeScript-go/pull/4799) (Closed)

**Refresh tsconfig/jsconfig diagnostics without relying on the client to re\-pull**

*Schedule debounced snapshot updates on config file changes so tsconfig/jsconfig diagnostics refresh independently of client requests.*

 * created by **johnfav03**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4799#issuecomment-5136024308) **jakebailey** said "I assume this is #4739 ++?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4799#issuecomment-5136128921) **johnfav03** explained that this PR hooks didChangeWatchedFiles instead of DidSaveFile and scopes detections to registry-tracked configs to address downsides in the other PR
 * (today) **johnfav03** closed the issue

### [PR microsoft/TypeScript-go#4800](https://github.com/microsoft/TypeScript-go/pull/4800) (Open)

**Don't report TS1293 for destructured require under \-\-module preserve**

*Prevent TS1293 errors on destructured require bindings in CommonJS modules when module setting is preserve.*

 * created by **AMR5210**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4800#issuecomment-5136885164) **AMR5210** said "@microsoft-github-policy-service agree"

### [Issue microsoft/TypeScript-go#4801](https://github.com/microsoft/TypeScript-go/issues/4801) (Open, `Needs Investigation`, **johnfav03**)

**\[ServerErrors\]\[TypeScript\] main vs **

*The Azure pipeline run on TypeScript’s main branch across 300 GitHub repos reported 34 changes, 102 timeouts and various failures.*

 * created by **typescript-automation[bot]**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4801#issuecomment-5137228627) **typescript-automation[bot]** reported a panic due to an unhandled node kind in JSX initializer and included a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/4801#issuecomment-5137228670) **typescript-automation[bot]** reported a panic in textDocument/diagnostic handling with a stack trace and affected repository details
 * [today](https://github.com/microsoft/TypeScript-go/issues/4801#issuecomment-5137228731) **typescript-automation[bot]** reported a panic handling request for textDocument/diagnostic including a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/4801#issuecomment-5137228787) **typescript-automation[bot]** reported a panic runtime error with index out of range in the internal checker
 * [today](https://github.com/microsoft/TypeScript-go/issues/4801#issuecomment-5137228837) **typescript-automation[bot]** reported a panic handling request for textDocument/diagnostic with a stack trace and affected repository details
 * [today](https://github.com/microsoft/TypeScript-go/issues/4801#issuecomment-5137228959) **typescript-automation[bot]** reported a panic in textDocument/diagnostic request with stack trace for siyuan-note/siyuan
 * [today](https://github.com/microsoft/TypeScript-go/issues/4801#issuecomment-5137229005) **typescript-automation[bot]** logged a panic in textDocument/diagnostic and provided stack trace and artifact details
 * [today](https://github.com/microsoft/TypeScript-go/issues/4801#issuecomment-5137229044) **typescript-automation[bot]** reported a premature server connection closure and provided affected repos, request logs, and repro steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/4801#issuecomment-5137229077) **typescript-automation[bot]** reported that the server connection closed prematurely for QwenLM/qwen-code and included error details, last requests, and repro steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/4801#issuecomment-5137229130) **typescript-automation[bot]** reported server connection closed prematurely error and provided repro steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/4801#issuecomment-5137229182) **typescript-automation[bot]** reported server connection closed prematurely with undefined error and provided affected repo details, raw error artifact links, recent request logs, and reproduction steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/4801#issuecomment-5137229231) **typescript-automation[bot]** reported a server connection closed prematurely error with repro steps and artifact links
 * [today](https://github.com/microsoft/TypeScript-go/issues/4801#issuecomment-5137229281) **typescript-automation[bot]** reported a premature server connection closure error when testing babel/babel
 * [today](https://github.com/microsoft/TypeScript-go/issues/4801#issuecomment-5137229341) **typescript-automation[bot]** reported that the server connection closed prematurely with an undefined error and provided the affected repository, error logs, and repro steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/4801#issuecomment-5137229379) **typescript-automation[bot]** reported that the server connection closed prematurely with an undefined error and provided affected repo details, last few requests, and repro steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/4801#issuecomment-5137229418) **typescript-automation[bot]** reported a panic handling request for textDocument/signatureHelp due to a nil pointer dereference and provided a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/4801#issuecomment-5137229469) **typescript-automation[bot]** reported a panic during handling textDocument/diagnostic and listed affected repos and artifacts
 * [today](https://github.com/microsoft/TypeScript-go/issues/4801#issuecomment-5137229548) **typescript-automation[bot]** reported a panic during textDocument/diagnostic with stack trace for honojs/hono
 * [today](https://github.com/microsoft/TypeScript-go/issues/4801#issuecomment-5137229621) **typescript-automation[bot]** reported a panic during textDocument/diagnostic with stack trace and repro commands for date-fns/date-fns

### [Issue microsoft/TypeScript-go#4802](https://github.com/microsoft/TypeScript-go/issues/4802) (Open)

**workspace/symbol returns results from projects outside the workspace folder**

*The TypeScript language server’s workspace/symbol command erroneously returns symbols from external project folders, leading to duplicates, slow queries, and high memory usage.*

 * created by **stewartmcgown**

### [PR microsoft/TypeScript-go#4803](https://github.com/microsoft/TypeScript-go/pull/4803) (Open)

**Fix panic when serializing empty tuple array literal types**

*tsgo panics when serializing an empty tuple array literal because cloned type references incorrectly retain tuple flags.*

 * created by **artem1458**
 * [later](https://github.com/microsoft/TypeScript-go/pull/4803#issuecomment-5144209590) **artem1458** said "@microsoft-github-policy-service agree"

### [Issue microsoft/TypeScript-go#4804](https://github.com/microsoft/TypeScript-go/issues/4804) (Open, **andrewbranch**)

**\`checker\.getTypeAtLocation\` panics for an array literal contextually typed by an empty tuple**

*checker.getTypeAtLocation panics on array literals typed by empty tuples due to an incorrect type assertion.*

 * created by **artem1458**

