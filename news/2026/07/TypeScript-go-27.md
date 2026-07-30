# Report for 2026-07-27 (Monday, July 27th, 2026)

19 different users commented on 44 different issues.

## Recommended Actions

 * Response Recommended
    * @padcom provided details on .vue file mapping in [microsoft/TypeScript-go#2824](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-5103502275)
    * @pikax asked who is responsible for the <i18n> block in [microsoft/TypeScript-go#2824](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-5103707400)
    * @Ijtihed asked if there was anything left for them to do in [microsoft/TypeScript-go#4218](https://github.com/microsoft/TypeScript-go/pull/4218#issuecomment-5104213104)
    * @johnnyreilly asked if project references were supported yet in [microsoft/TypeScript-go#4699](https://github.com/microsoft/TypeScript-go/pull/4699#issuecomment-5103710645)
    * @valentinmelusson provided requested environment and configuration details in [microsoft/TypeScript-go#4758](https://github.com/microsoft/TypeScript-go/issues/4758#issuecomment-5101846289)
    * @ljharb asked whether the change in JS behavior under checkJs was intentional and suggested documenting it in the migration docs in [microsoft/TypeScript-go#4768](https://github.com/microsoft/TypeScript-go/issues/4768#issuecomment-5098096280)

## Activity Summary

### [Issue microsoft/TypeScript-go#2824](https://github.com/microsoft/TypeScript-go/issues/2824) (Open, `Domain: API and Extensibility`, **andrewbranch**)

**API usage patterns for complex editor extensions**

*Exploring IPC-based API features for a Go TS server to replace TS Server plugins and support Vue editor extensions*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-5004116575) **shining-mind** asked if the proposal should be moved to the typescript-go repo
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-5005913332) **andrewbranch** said "No, development will move back to microsoft/TypeScript soon and typescript-go will be archived."
 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-5054092971) **andrewbranch** said "@johnsoncodehk, @remcohaszing, @dummdidumm, and anyone else working on this kind of ecosystem tooling: I would really appreciate your input on #4712."
 * [today](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-5096586511) **DanielRosenwasser** said "Question for API integrators - are there any instances today where a single non-TS file actually maps into multiple distinct files?"
 * [later](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-5103502275) **padcom** described how .vue single-file components map into multiple generated files
 * [later](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-5103707400) **pikax** explained that file mapping depends on integration, noted that vue can split a SFC into multiple files or as one with adjustments, questioned who should handle the <i18n> block, and described an unrelated test-file use case about SFC imports requiring different mapper options

### [PR microsoft/TypeScript-go#3102](https://github.com/microsoft/TypeScript-go/pull/3102) (Closed, **DanielRosenwasser**)

**Fix a formatting crash caused by template literal in parser\-recovered property signature**

*Fix formatting crash caused by skipped error nodes in recovered property signatures mis-scanning template literal tokens.*

 * (6 weeks ago) **RyanCavanaugh** set milestone to `Post-7.0`, and removed from milestone `TypeScript 7.0 RC`
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3102#issuecomment-4939912425) **Andarist** said "@DanielRosenwasser I missed the notification in what was a particularly busy month for me - I just fixed those conflicts"
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript-go#4218](https://github.com/microsoft/TypeScript-go/pull/4218) (Open, `Voight-Kampff Anomaly`)

**Allow lone & in Unicode sets regexp classes**

*Update native scanner to allow lone & in Unicode Set regex character classes while preserving && intersections.*

 * [1 month ago](https://github.com/microsoft/TypeScript-go/pull/4218#issuecomment-4792508870) **RyanCavanaugh** said "@graphemecluster in case you want to see it"
 * [1 month ago](https://github.com/microsoft/TypeScript-go/pull/4218#issuecomment-4796094461) **graphemecluster** noted the small fix looked fine but mentioned preferring to port PR #62716 if its scope met expectations
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4218#issuecomment-4969251422) **Ijtihed** said "so what's the consensus here? :) I can close if needed"
 * [later](https://github.com/microsoft/TypeScript-go/pull/4218#issuecomment-5104213104) **Ijtihed** asked if there was anything left for them to do

### [PR microsoft/TypeScript-go#4239](https://github.com/microsoft/TypeScript-go/pull/4239) (Closed, `No linked issue`)

**Replace ForEachReturnStatement closure with direct kind\-switched walk**

*Replace ForEachReturnStatement closure with a direct kind-switched recursive function to reduce allocations and improve performance.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4239#issuecomment-4906347760) **jakebailey** said "In #4395 I optimized ForEachChild to avoid the interfaces; is this still helpful?"
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4239#issuecomment-4906526669) **DanielRosenwasser** said "This would still save the closure allocation and visit fewer child nodes, right?"
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4239#issuecomment-4906575654) **jakebailey** said "No, this should get stack allocated"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4239#issuecomment-5097903321) **jakebailey** reevaluated the refactor as not worth it and suggested adding a canContainReturnStatement function to skip nodes that can't contain return statements

### [Issue microsoft/TypeScript-go#4481](https://github.com/microsoft/TypeScript-go/issues/4481) (Open, `Domain: Editor`, **DanielRosenwasser**, **Copilot**)

**Auto\-imports hits unimplemented \`GetSourceOfProjectReferenceIfOutputIncluded\`**

*The auto-import process crashes with a stack trace due to the unimplemented GetSourceOfProjectReferenceIfOutputIncluded method.*

 * (1 month ago) **DanielRosenwasser** assigned to **Copilot**, **DanielRosenwasser**
 * **RyanCavanaugh** added to milestone `Post-7.0`
 * [today](https://github.com/microsoft/TypeScript-go/issues/4481#issuecomment-5097985779) **DanielRosenwasser** shared two Copilot-generated tests but noted inability to drive them

### [Issue microsoft/TypeScript-go#4581](https://github.com/microsoft/TypeScript-go/issues/4581) (Open, `bug`, **RyanCavanaugh**, **Copilot**)

**TS2719/TS2322 false positive on a generic type forwarded through an interface \`extends\` boundary \(tsc clean, tsgo fails\)**

*tsgo wrongly reports a TS2719/TS2322 type mismatch when extending and forwarding a library’s generic props interface despite tsc accepting it*

 * created by **alekseigoloviichuk**
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/4581#issuecomment-5066070667) **alscotty-fox** said "+1 on this issue"
 * [today](https://github.com/microsoft/TypeScript-go/issues/4581#issuecomment-5096743244) **RyanCavanaugh** provided a minimal reproduction case demonstrating a TS2719 error about two unrelated types with the same name for defaultColumn.Cell
 * (today) **RyanCavanaugh** added label `bug`, set milestone to `TypeScript 7.1`, assigned to **Copilot**, **RyanCavanaugh**, **Copilot**, **RyanCavanaugh**, and unassigned **RyanCavanaugh**, **Copilot**

### [PR microsoft/TypeScript-go#4582](https://github.com/microsoft/TypeScript-go/pull/4582) (Closed)

**Call IsDirCoveredByWatch less often to improve performance**

*Improve tsc --watch performance by reducing redundant IsDirCoveredByWatch calls and optimizing directory caching*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4582#issuecomment-4936667616) **AkisArou** tested the PR with tsgo --build --watch in a large monorepo and observed that watches were not installed after five minutes; prepared a proof-of-concept branch adding an indexed DirectorySet and updating orchestrator.go to use the index, which made watch initialization immediate
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4582#issuecomment-4937051430) **terite** clarified that the PR only affected the tsgo --watch code path and explained reasons for not modifying the --build code path due to its prototype status and personal lack of usage
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4582#issuecomment-4975044627) **terite** said "@microsoft-github-policy-service agree"
 * [later](https://github.com/microsoft/TypeScript-go/pull/4582#issuecomment-5106507276) **terite** said "Closing this in favor of #4658"
 * (later) **terite** closed the issue

### [PR microsoft/TypeScript-go#4604](https://github.com/microsoft/TypeScript-go/pull/4604) (Closed)

**fix: prevent unnecessary diagnostic refreshes on irrelevant watch events \(\#4589\)**

*Optimize file watch handling by scheduling diagnostics refresh only for relevant TypeScript files and directories, reducing CPU and RPC overhead.*

 * created by **ibesuperv**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4604#issuecomment-5098994242) **ibesuperv** said "@johnfav03 Applied, thanks for the catch!"

### [Issue microsoft/TypeScript-go#4610](https://github.com/microsoft/TypeScript-go/issues/4610) (Closed, `Domain: Editor`, `Needs Investigation`, **johnfav03**)

**Renaming a file can be very slow in some edge cases**

*VSCode tsgo file renames can be slow because a third-party .d.ts with repeated imports triggers quadratic path-updater scans.*

 * (1 week ago) **RyanCavanaugh** added label `Needs Investigation`, and set milestone to `TypeScript 7.1`
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/4610#issuecomment-5077957506) **swotvibe** asked whether the issue was still open for someone else to pick up and whether memoizing computed import specifiers would resolve the repeated-computation performance issue
 * [today](https://github.com/microsoft/TypeScript-go/issues/4610#issuecomment-5094530293) **johnfav03** explained that he implemented a fix precomputing the moved-files set once per rename to optimize unresolved import scanning and described why this approach was chosen based on resolutionMode differences
 * (today) **johnfav03** closed the issue

### [Issue microsoft/TypeScript-go#4672](https://github.com/microsoft/TypeScript-go/issues/4672) (Closed, `bug`, **johnfav03**)

**is Watch out of the prototype phase?**

*Query whether the --watch mode is production-ready given incremental rechecking support and if the README requires updating.*

 * **RyanCavanaugh** added label `bug`
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/4672#issuecomment-5027748004) **RyanCavanaugh** said "Watch is fully supported; we forgot to update the readme"
 * **RyanCavanaugh** added to milestone `TypeScript 7.1`
 * (today) **johnfav03** closed the issue

### [Issue microsoft/TypeScript-go#4697](https://github.com/microsoft/TypeScript-go/issues/4697) (Closed, `Working As Intended`)

**Behavior difference: import \* as x of an export = callable loses call signatures without esModuleInterop \(TS2349\)**

*Without esModuleInterop, tsgo’s import * from an export= callable incorrectly drops the call signature, causing TS2349 errors.*

 * created by **greg-flux**
 * [6 days ago](https://github.com/microsoft/TypeScript-go/issues/4697#issuecomment-5037651107) **jakebailey** observed that esModuleInterop being disabled was unsupported and inquired if it defaulted to true
 * **RyanCavanaugh** added label `Working As Intended`
 * [today](https://github.com/microsoft/TypeScript-go/issues/4697#issuecomment-5096761382) **RyanCavanaugh** said "Yeah, this should have never worked in the first place. An import * is never callable and TS was wrong to treat is as such."
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#4699](https://github.com/microsoft/TypeScript-go/pull/4699) (Closed)

**API emit**

*Add program.emit, program.emitToString, getJavaScriptEmit, and getDeclarationEmit methods for flexible file system and in-memory emissions.*

 * [4 days ago](https://github.com/microsoft/TypeScript-go/pull/4699#issuecomment-5063044729) **andrewbranch** noted that source maps were already included in program.emit and program.emitToString outputs, added tests, and asked whether getters for source map emit and declaration source map emit should be added
 * [4 days ago](https://github.com/microsoft/TypeScript-go/pull/4699#issuecomment-5063469921) **jakebailey** said "Would anyone ever want the source map for a file output they don't have? I assume not, so those two wouldn't be needed?"
 * (3 days ago) **andrewbranch** closed the issue
 * **DanielRosenwasser** added to milestone `TypeScript 7.1`
 * [later](https://github.com/microsoft/TypeScript-go/pull/4699#issuecomment-5103710645) **johnnyreilly** said "As far as I can tell, there's no support for project references as yet - am I reading that correctly? asking for https://github.com/TypeStrong/ts-loader/pull/1704"
 * [later](https://github.com/microsoft/TypeScript-go/pull/4699#issuecomment-5105156480) **pfumagalli** asked what was meant by “project references” and explained that type checking across referenced projects works like createProgram but a solution builder (tsc --build) is not implemented yet

### [PR microsoft/TypeScript-go#4731](https://github.com/microsoft/TypeScript-go/pull/4731) (Closed)

**Lazily collect source file identifiers**

*Delay source file identifier collection until requested and eliminate unnecessary interning code to boost performance and reduce memory overhead.*

 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/4731#issuecomment-5075318768) **DanielRosenwasser** said "@typescript-bot perf test this"
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/4731#issuecomment-5075319263) **typescript-automation[bot]** posted CI status update with build start and result links
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/4731#issuecomment-5075541566) **typescript-automation[bot]** provided performance run results requested by @DanielRosenwasser
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4743](https://github.com/microsoft/TypeScript-go/issues/4743) (Closed, **DanielRosenwasser**)

**Panic: Stack overflow during contextual typing of yield in a computed property name**

*Native TypeScript compiler stack overflows during contextual typing of a computed property name containing a yield expression in a generator method.*

 * created by **HuzaifaAbdulRehman**
 * **DanielRosenwasser** assigned to **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4743#issuecomment-5096597599) **RyanCavanaugh** said "We don't need an additional copy of the issue in this repo. Tracking at 62941 is fine."
 * (today) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/issues/4743#issuecomment-5096607865) **RyanCavanaugh** said "@HuzaifaAbdulRehman to be clear: do not replicate additional copies of upstream repo issues into this repo"

### [PR microsoft/TypeScript-go#4744](https://github.com/microsoft/TypeScript-go/pull/4744) (Closed)

**Reorganize AST to prevent duplicate fields**

*Restructure AST definitions to eliminate duplicate struct fields such as UnionTypeNode and reduce memory usage.*

 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/4744#issuecomment-5081194414) **jakebailey** said "@typescript-bot perf test this faster"
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/4744#issuecomment-5081194612) **typescript-automation[bot]** reported the start of CI jobs and provided links to status and results
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/4744#issuecomment-5081278216) **typescript-automation[bot]** provided the perf run results for the requested benchmarks
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4746](https://github.com/microsoft/TypeScript-go/pull/4746) (Closed)

**fix: emit missing TS7059 errors**

*Add missing logic ported from TypeScript to emit TS7059 diagnostic errors in oxc.*

 * created by **camc314**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4746#issuecomment-5083806727) **camc314** said "@codex review"
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4753](https://github.com/microsoft/TypeScript-go/issues/4753) (Closed, **jakebailey**, **Copilot**)

**Putting a compiler option at the top level instead of in \`compilerOptions\` no longer reports**

*Top-level compiler options in tsconfig.json no longer produce errors with tsgo, unlike TypeScript 6.0.*

 * created by **abrahamguo**
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4754](https://github.com/microsoft/TypeScript-go/issues/4754) (Closed, **jakebailey**, **Copilot**)

**TS5092 no longer has a file/line/column**

*TS5092 error reported by tsgo lacks file, line, and column location information compared to TypeScript 6.0*

 * created by **abrahamguo**
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4755](https://github.com/microsoft/TypeScript-go/issues/4755) (Closed, **jakebailey**, **Copilot**)

**TS no longer reports "Did you mean" for misspelled \`tsconfig\.json\` options**

*tsgo no longer suggests corrections for misspelled tsconfig compiler options like TypeScript 6.0 did*

 * created by **abrahamguo**
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4758](https://github.com/microsoft/TypeScript-go/issues/4758) (Closed)

**disableSourceOfProjectReferenceRedirect causes lodash per\-method submodule import to resolve to the wrong function**

*Enabling disableSourceOfProjectReferenceRedirect in a referenced TypeScript project causes lodash/get imports to resolve as lodash/set under tsgo.*

 * created by **valentinmelusson**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4758#issuecomment-5095511022) **jakebailey** requested OS and package manager details, tsconfig configurations, and diagnostic outputs to reproduce the issue
 * [later](https://github.com/microsoft/TypeScript-go/issues/4758#issuecomment-5101846289) **valentinmelusson** provided OS and package manager details, shared tsconfig.json configurations, and reported errors persisted across local and CI environments

### [PR microsoft/TypeScript-go#4759](https://github.com/microsoft/TypeScript-go/pull/4759) (Closed, **jakebailey**, **Copilot**)

**Restore spelling suggestions for unknown tsconfig options**

*Reapply spelling suggestions for unknown tsconfig.json options by using the suggestion algorithm in JSON parsing and emitting TS5025.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4760](https://github.com/microsoft/TypeScript-go/pull/4760) (Closed, **jakebailey**, **Copilot**)

**Restore source location for TS5092**

*Associate TS5092 diagnostics with the root expression in tsconfig.json to restore file position and add test coverage for array-valued configs.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4761](https://github.com/microsoft/TypeScript-go/pull/4761) (Closed, **jakebailey**, **Copilot**)

**Report compiler options misplaced at the tsconfig root**

*Implement diagnostic TS6258 and nonzero exit status for misplaced tsconfig compiler options outside compilerOptions*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4763](https://github.com/microsoft/TypeScript-go/pull/4763) (Closed)

**Fix unused type parameter diagnostic message**

*Improve the diagnostic message for unused type parameters to provide clear and accurate information*

 * created by **camc314**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4763#issuecomment-5094074835) **jakebailey** explained that the behavior was intentional and that submoduleAccepted entries indicate manual inspection
 * [today](https://github.com/microsoft/TypeScript-go/pull/4763#issuecomment-5094134743) **camc314** said "Ah gotcha, thanks for the context 🙂 "
 * (today) **camc314** closed the issue

### [PR microsoft/TypeScript-go#4764](https://github.com/microsoft/TypeScript-go/pull/4764) (Closed)

**Remove unused classifiable name tracking**

*Removes unused classifiable name tracking to improve binder performance and reduce memory usage by up to 5%.*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#4765](https://github.com/microsoft/TypeScript-go/pull/4765) (Closed)

**Fix quadratic slowdown when renaming files with duplicate unresolved imports**

*Precomputing moved file candidates to eliminate quadratic slowdown when renaming files with duplicate unresolved imports*

 * created by **johnfav03**
 * (today) **johnfav03** closed the issue

### [PR microsoft/TypeScript-go#4766](https://github.com/microsoft/TypeScript-go/pull/4766) (Closed)

**Update watcher status in readme**

*Update the README to reflect the current watcher status.*

 * created by **johnfav03**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4766#issuecomment-5094916497) **jakebailey** said "I feel like the readme needs a total redo, or, we should just purge this before we archive the repo"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4766#issuecomment-5094934054) **johnfav03** asked whether to close the attached issue or how to handle the readme redo suggestion
 * (today) **johnfav03** closed the issue

### [PR microsoft/TypeScript-go#4767](https://github.com/microsoft/TypeScript-go/pull/4767) (Open)

**Fix package ID collisions for remapped inputs**

*Fix package ID collisions by ensuring remapped input references like “set” are correctly resolved instead of mapping to “get”.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4767#issuecomment-5095394442) **jakebailey** said "I might have been bamboozled, I think this bug only happens if packageDirectory is / which the test case can make happen, but is very likely not reality for the real repro."

### [Issue microsoft/TypeScript-go#4768](https://github.com/microsoft/TypeScript-go/issues/4768) (Closed)

**TS7023 false positive: contextual return type ignored when a recursive call is assigned to a union\-annotated local**

*TypeScript incorrectly reports TS7023 on a contextually typed recursive function when assigning its call to a union-typed variable.*

 * created by **ljharb**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `Post-7.0`, and assigned to **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4768#issuecomment-5097521326) **ahejlsberg** reported inability to reproduce the issue and explained that contextual types don’t prevent resolution of expression types, so circular return type inference still occurs
 * (today) **ahejlsberg** added label `Needs More Info`, and removed label `Needs Investigation`
 * [today](https://github.com/microsoft/TypeScript-go/issues/4768#issuecomment-5097543804) **ahejlsberg** explained that the type annotation on equal causes circularity because control flow analysis narrows its union type based on whyH’s return type, which doesn’t occur without the annotation
 * (today) **RyanCavanaugh** set milestone to `Need More Info`, removed from milestone `Post-7.0`, and unassigned **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4768#issuecomment-5098096280) **ljharb** clarified that the error regression occurs only in JavaScript with JSDoc @type under checkJs, asked whether this change was intentional and suggested noting it in the migration docs
 * (today) **RyanCavanaugh** removed label `Needs More Info`, and removed from milestone `Need More Info`
 * [today](https://github.com/microsoft/TypeScript-go/issues/4768#issuecomment-5098140502) **RyanCavanaugh** noted that CHANGES.md already describes JSDoc support as being more based on TS and that changes aligning with TS behavior need no additional justification unless there's a strong positive case
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#4769](https://github.com/microsoft/TypeScript-go/pull/4769) (Closed, **RyanCavanaugh**, **Copilot**)

**Fix TS2719 false positive for same\-origin recursive generic conditionals across \`interface extends\` forwarding**

*Refactor TypeScript’s conditional type checks to normalize same-origin recursive generics and fix TS2719 false positives on interface-extended forwarded options*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4769#issuecomment-5098106048) **RyanCavanaugh** said "@copilot I seriously doubt this is the correct fix, but I suppose anything is possible. Did TS 6 have this code? If so, where? If not, why didn't it need it?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4769#issuecomment-5098243719) **Copilot** described that TS6 did not include the extra code block, explained that reverting the change in tsgo reproduces errors and false positives due to port divergence, and noted that baseline updates for tests were pushed in commit 543213bc
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#4770](https://github.com/microsoft/TypeScript-go/pull/4770) (Closed)

**Fix rewritten CJS dynamic import arguments**

*Fix rewriting of arguments passed to dynamic imports in CommonJS modules.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4771](https://github.com/microsoft/TypeScript-go/issues/4771) (Closed)

**Module reference dropped for imported name referenced inside \`import\(\)\` with \`rewriteRelativeImportExtensions\`**

*tsgo's rewriteRelativeImportExtensions transform drops the imported pathToFileURL inside dynamic import, causing a runtime undefined error.*

 * created by **ecraig12345**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4772](https://github.com/microsoft/TypeScript-go/pull/4772) (Closed, **RyanCavanaugh**, **Copilot**)

**Select "types returned by" vs "types of" from the merged dotted name in relation errors**

*Fix error message condensation in tsgo to match tsc by selecting “types returned by” or “types of” based on the merged dotted name suffix*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**

### [Issue microsoft/TypeScript-go#4773](https://github.com/microsoft/TypeScript-go/issues/4773) (Closed)

**Consumer\-side TS2595 for a dependency \`\.d\.ts\` that mixes \`export =\` with named exports and suppresses its own TS2309**

*tsgo falsely reports TS2595 on consumer imports from a dependency whose .d.ts file mixes export= with named exports, unlike tsc.*

 * created by **Togetic**
 * [later](https://github.com/microsoft/TypeScript-go/issues/4773#issuecomment-5103648348) **Togetic** noted that consola@3.4.2 has a separate issue and that dependencies suppressing their own TS2309 errors leave consumers with unsuppressable errors

### [Issue microsoft/TypeScript-go#4774](https://github.com/microsoft/TypeScript-go/issues/4774) (Open)

**Document that \`@typescript/typescript6\` ships the API under \`@typescript/old\` \(path\-based tooling\)**

*Document that the TypeScript 6 API from @typescript/typescript6 resides under @typescript/old and requires updating path-based tooling ignores accordingly.*

 * created by **Akshay090**

