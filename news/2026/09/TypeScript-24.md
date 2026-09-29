# Report for 2026-09-24 (Thursday, September 24th, 2026)

23 different users commented on 61 different issues.

## Recommended Actions

 * Response Recommended
    * @no-yan asked for feedback on the Store design in [microsoft/TypeScript#63807](https://github.com/microsoft/TypeScript/issues/63807#issuecomment-5826174145)
    * @mhalikosen provided reproduction steps and variant test results in [microsoft/TypeScript#64405](https://github.com/microsoft/TypeScript/issues/64405#issuecomment-5829231426)
    * @colinhacks provided repro steps and detailed explanation in [microsoft/TypeScript#64415](https://github.com/microsoft/TypeScript/issues/64415#issuecomment-5824032707)
    * @Amatewasu provided requested error logs in [microsoft/TypeScript#64423](https://github.com/microsoft/TypeScript/issues/64423#issuecomment-5828271795)
    * @Amatewasu provided repro steps and detailed investigation findings in [microsoft/TypeScript#64423](https://github.com/microsoft/TypeScript/issues/64423#issuecomment-5828937397)
    * @typescript-automation[bot] reported an access denied error for the run dt job in [microsoft/TypeScript#64432](https://github.com/microsoft/TypeScript/pull/64432#issuecomment-5822648561)
    * @typescript-automation[bot] asked to review build results and investigate failures in [microsoft/TypeScript#64432](https://github.com/microsoft/TypeScript/pull/64432#issuecomment-5823485789)
    * @typescript-automation[bot] asked to check the DT test run log for failure details in [microsoft/TypeScript#64432](https://github.com/microsoft/TypeScript/pull/64432#issuecomment-5827364888)
    * @typescript-automation[bot] requested review of test result changes in [microsoft/TypeScript#64432](https://github.com/microsoft/TypeScript/pull/64432#issuecomment-5827456449)
    * @typescript-automation[bot] reported a failed test run and asked to check the logs in [microsoft/TypeScript#64432](https://github.com/microsoft/TypeScript/pull/64432#issuecomment-5827557632)
    * @typescript-automation[bot] requested review of tsc comparison results in [microsoft/TypeScript#64432](https://github.com/microsoft/TypeScript/pull/64432#issuecomment-5827995661)
    * @typescript-automation posted build comparison results between main and PR in [microsoft/TypeScript#64432](https://github.com/microsoft/TypeScript/pull/64432#issuecomment-5829950122)
    * @typescript-automation[bot] reported build errors in hardhat project in [microsoft/TypeScript#64432](https://github.com/microsoft/TypeScript/pull/64432#issuecomment-5829950675)
    * @typescript-automation[bot] reported build failures and error details for teableio/teable in [microsoft/TypeScript#64432](https://github.com/microsoft/TypeScript/pull/64432#issuecomment-5829951254)
    * @sh011 asked to be assigned the issue in [microsoft/TypeScript#64438](https://github.com/microsoft/TypeScript/issues/64438#issuecomment-5826551653)
    * @typescript-automation[bot] provided perf run results as requested in [microsoft/TypeScript#64442](https://github.com/microsoft/TypeScript/pull/64442#issuecomment-5824628416)
    * @typescript-automation[bot] reported test failures requiring investigation in [microsoft/TypeScript#64442](https://github.com/microsoft/TypeScript/pull/64442#issuecomment-5824693554)
    * @typescript-automation[bot] reported build errors in several projects and requested review in [microsoft/TypeScript#64442](https://github.com/microsoft/TypeScript/pull/64442#issuecomment-5825098380)

## Activity Summary

### [Issue microsoft/TypeScript#36922](https://github.com/microsoft/TypeScript/issues/36922) (Closed, `Bug`, `Needs More Info`, `Domain: Module Resolution`)

**tsconfig paths not work if dir name start with dot\.**

*Tsconfig path aliases fail to resolve imports when mapped to a directory starting with a dot.*

 * (3 weeks ago) **RyanCavanaugh** added labels `Needs Human Review`, `Needs More Info`
 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/36922#issuecomment-5536210016) **LeonxLJX** offered to fix the tsconfig.paths resolution bug and asked for maintainer guidance on intended behavior for dot-prefixed directories
 * (today) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#37100](https://github.com/microsoft/TypeScript/issues/37100) (Closed, `Bug`, `Needs More Info`, `Domain: check: Type Inference`, `Needs Human Review`)

**Any type is inferred when function input parameter is set to some value**

*TypeScript infers any for abc’s generic return type when its optional continuation parameter is undefined.*

 * (3 weeks ago) **RyanCavanaugh** added labels `Needs Human Review`, `Needs More Info`
 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/37100#issuecomment-5536209673) **LeonxLJX** offered to take the issue and described the repro as a narrowed-then-reused trap, diagnosed the root cause in strict flow analysis, outlined workarounds, and suggested confirming reproduction on TS 5.6+ before drafting a focused repro
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#49526](https://github.com/microsoft/TypeScript/issues/49526) (Closed, `Bug`, `Help Wanted`, `Domain: lib.d.ts`, `Docs`)

**Document the Iterator, Iterable, IterableIterator types**

*Document TypeScript’s standard Iterator, Iterable, and IterableIterator interfaces to clarify their usage.*

 * (4.2 years ago) **RyanCavanaugh** added labels `Docs`, `Needs Human Review`, and set milestone to `Backlog`
 * **RyanCavanaugh** removed label `Needs Human Review`
 * [today](https://github.com/microsoft/TypeScript/issues/49526#issuecomment-5821416693) **RyanCavanaugh** said "This doesn't seem to be a common problem"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#49561](https://github.com/microsoft/TypeScript/issues/49561) (Open, `Help Wanted`, `Domain: lib.d.ts`, `Docs`)

**Docs of \`charCodeAt\` and \`codePointAt\` are flipped**

*JSDoc descriptions for charCodeAt and codePointAt are reversed in TypeScript’s standard library definitions.*

 * (2.5 years ago) **RyanCavanaugh** added labels `Docs`, `Needs Human Review`, and set milestone to `Backlog`
 * (today) **RyanCavanaugh** removed labels `Bug`, `Needs Human Review`

### [Issue microsoft/TypeScript#51376](https://github.com/microsoft/TypeScript/issues/51376) (Open, `Bug`, `Help Wanted`, `Domain: Related Error Spans`)

**Spread operator with wrong optional property raises error on incorrect source line**

*TypeScript misreports error location when spreading an object with an optional property into a stricter type*

 * (6 days ago) **RyanCavanaugh** added labels `Needs Human Review`, `Needs More Info`
 * [4 days ago](https://github.com/microsoft/TypeScript/issues/51376#issuecomment-5755811601) **laverdet** questioned if maintainers were using the same playground link and confirmed the repro on TS v6 and v7; provided code showing a confusing TS2322 error for attribute: "" under strict mode
 * (today) **RyanCavanaugh** removed labels `Needs More Info`, `Needs Human Review`
 * [today](https://github.com/microsoft/TypeScript/issues/51376#issuecomment-5821544888) **RyanCavanaugh** provided a clearer repro example illustrating that the error span remained on the property instead of the spread and suggested highlighting the entire literal when a spread may contribute to the type

### [Issue microsoft/TypeScript#51885](https://github.com/microsoft/TypeScript/issues/51885) (Closed, `Bug`, `Fixed`, `Help Wanted`, `Domain: lib.d.ts`)

**\[type bug\] fontfaces property is missing from loadingdone event object**

*Update FontFaceSet's onloadingdone handler type from Event to FontFaceSetLoadEvent to expose fontfaces property.*

 * **RyanCavanaugh** added label `Needs Human Review`
 * (6 days ago) **RyanCavanaugh** closed the issue
 * [6 days ago](https://github.com/microsoft/TypeScript/issues/51885#issuecomment-5739748405) **TechQuery** asked which version the fix would be released in
 * [today](https://github.com/microsoft/TypeScript/issues/51885#issuecomment-5821554744) **RyanCavanaugh** said "That PR shipped in 5.7 or 5.8"
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#54099](https://github.com/microsoft/TypeScript/issues/54099) (Open, `Bug`, `Help Wanted`, `Domain: Decorators`)

**Unknown interface "ClassMethodDecoratorFunction" in documentation for 5\.0\.4 lib\.decorators\.d\.ts**

*TypeScript 5.0.4 decorators.d.ts documentation incorrectly references a non-existent ClassMethodDecoratorFunction interface instead of ClassMethodDecoratorContext.*

 * (49 weeks ago) **RyanCavanaugh** added labels `Domain: Decorators`, `Docs`, `Needs Human Review`
 * (today) **RyanCavanaugh** removed labels `Docs`, `Needs Human Review`

### [Issue microsoft/TypeScript#54338](https://github.com/microsoft/TypeScript/issues/54338) (Open, `Bug`, `Help Wanted`, `Domain: Decorators`)

**Comment referencing an undefined \`ClassDecoratorFunction\` type**

*decorators.d.ts references an undefined ClassDecoratorFunction type in the library definitions*

 * (49 weeks ago) **RyanCavanaugh** added labels `Domain: Decorators`, `Docs`, `Needs Human Review`
 * (today) **RyanCavanaugh** removed labels `Docs`, `Needs Human Review`

### [Issue microsoft/TypeScript#56669](https://github.com/microsoft/TypeScript/issues/56669) (Open, `Bug`, `Help Wanted`, `Domain: JSX/TSX`)

**Mirror cursor for JSX stops working in some case**

*JSX mirrored cursor editing stops duplicating edits after deleting and typing characters in a component tag*

 * [1.9 years ago](https://github.com/microsoft/TypeScript/issues/56669#issuecomment-2392530712) **iisaduan** described how parsing recovery no longer recognized JSX tags with props and noted that #57127 fixed the case without props
 * (49 weeks ago) **RyanCavanaugh** added labels `Domain: JSX/TSX`, `Needs Human Review`
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#63807](https://github.com/microsoft/TypeScript/issues/63807) (Open, `Possible Improvement`)

**Proposal: Flatten the AST to speed up tsgo**

*Proposes flattening tsgo’s AST into a flat array to reduce garbage collection scanning overhead and improve performance.*

 * [25 weeks ago](https://github.com/microsoft/TypeScript/issues/63807#issuecomment-5351502144) **DanielRosenwasser** explained that replacing pointers with indexes would complicate API by requiring arena context and noted that slimming down nodeData was risky with minimal savings
 * [25 weeks ago](https://github.com/microsoft/TypeScript/issues/63807#issuecomment-5351502165) **ahejlsberg** suggested disabling GC for command-line compiles due to minimal GC-eligible allocations
 * [25 weeks ago](https://github.com/microsoft/TypeScript/issues/63807#issuecomment-5351502186) **no-yan** clarified that the goal was reducing GC scan cost rather than DoD/locality, explained that GC still scans contiguous nodes containing pointers, suggested making large pointer-free regions to avoid scanning, and recommended disabling or tuning GC for command-line compiles
 * [today](https://github.com/microsoft/TypeScript/issues/63807#issuecomment-5826174145) **no-yan** reported migrating TypeScript's AST to a store-based representation, highlighted performance improvements, and solicited feedback on the design

### [Issue microsoft/TypeScript#63906](https://github.com/microsoft/TypeScript/issues/63906) (Closed, `Needs Investigation`, **andrewbranch**)

**\[7\.1 API\] SymbolFlags\.All has different value in TS vs GO**

*SymbolFlags.All is evaluated differently in Go and TypeScript due to operator precedence causing mismatched values.*

 * created by **dragomirtitian**
 * (5 weeks ago) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript/issues/63906#issuecomment-5819599254) **andrewbranch** said "Fixed in https://github.com/microsoft/TypeScript/pull/64083"
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#64096](https://github.com/microsoft/TypeScript/pull/64096) (Closed, `For Milestone Bug`, **DanielRosenwasser**)

**feat: add es2026 as a valid target and lib**

*Add ES2026 as a recognized compilation target and library option in TypeScript.*

 * created by **a-tarasyuk**
 * (3 weeks ago) **typescript-automation[bot]** added label `For Milestone Bug`, and assigned to **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript/pull/64096#issuecomment-5822821539) **DanielRosenwasser** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/64096#issuecomment-5822822759) **typescript-automation[bot]** reported CI job statuses with links to build results
 * [today](https://github.com/microsoft/TypeScript/pull/64096#issuecomment-5823146851) **typescript-automation[bot]** reported perf run results as requested
 * [today](https://github.com/microsoft/TypeScript/pull/64096#issuecomment-5823200282) **typescript-automation[bot]** reported test results against main and PR merge showing infrastructure failures and a lodash type error
 * [today](https://github.com/microsoft/TypeScript/pull/64096#issuecomment-5823632574) **typescript-automation[bot]** reported that running the top 400 repos with tsc comparing main and the pull request merge produced no issues
 * [today](https://github.com/microsoft/TypeScript/pull/64096#issuecomment-5827319061) **typescript-automation[bot]** notified that DT tests results were ready and unchanged

### [Issue microsoft/TypeScript#64152](https://github.com/microsoft/TypeScript/issues/64152) (Open, `Bug`, `Breaking Change`, **DanielRosenwasser**, **Copilot**)

**No error when exporting from global augmentations**

*Exporting bindings introduced via global augmentations incorrectly succeeds instead of erroring like other non-local exports.*

 * (3 weeks ago) **DanielRosenwasser** added label `Breaking Change`, and assigned to **Copilot**, **DanielRosenwasser**
 * (today) **DanielRosenwasser** set milestones to `TypeScript 4.7.2`, `TypeScript 7.2.0 Beta`, and removed from milestone `TypeScript 4.7.2`

### [PR microsoft/TypeScript#64330](https://github.com/microsoft/TypeScript/pull/64330) (Open, `For Uncommitted Bug`, **RyanCavanaugh**, **Copilot**)

**Accept union replacement values in String\.replace**

*Enable String.prototype.replace and custom [Symbol.replace] methods to accept replacement arguments typed as string or function unions.*

 * (6 days ago) **typescript-automation[bot]** added labels `For Milestone Bug`, `For Uncommitted Bug`, and removed label `For Milestone Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64330#issuecomment-5824369770) **graphemecluster** said "An identical patch should be applied to replaceAll (I did in #64442, but even if my fix weren't desirable after all, aligning replace with replaceAll would still be worthwhile.)"

### [Issue microsoft/TypeScript#64368](https://github.com/microsoft/TypeScript/issues/64368) (Open, `Needs Investigation`, **andrewbranch**)

**Content mapper: allowing document highlight result from other language\-servers**

*Propose returning null instead of empty arrays for content-mapper document highlight results to enable fallback from other language servers.*

 * created by **jasonlyu123**
 * (2 days ago) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **andrewbranch**
 * **andrewbranch** added to milestone `TypeScript 7.1.0 Beta`

### [Issue microsoft/TypeScript#64370](https://github.com/microsoft/TypeScript/issues/64370) (Closed, `Won't Fix`)

**Native compiler \(tsgo\) aborts with "fatal error: stack overflow" on deeply nested expressions**

*tsgo compiler crashes with a fatal stack overflow when parsing extremely deeply nested parentheses, brackets, or type arguments due to unbounded parser recursion.*

 * [3 days ago](https://github.com/microsoft/TypeScript/issues/64370#issuecomment-5768184242) **RyanCavanaugh** marked the PR as Won't Fix and closed it, noting the invariant doesn't exist and the proposed fix was overly complex
 * **RyanCavanaugh** added label `Won't Fix`
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/64370#issuecomment-5772918346) **kajaaz** said "Hi @jakebailey @RyanCavanaugh, ok I understand, this makes sense. Thank you for your time"
 * [today](https://github.com/microsoft/TypeScript/issues/64370#issuecomment-5825123149) **typescript-automation[bot]** said "This issue has been marked as "Won't Fix" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-automation[bot]** closed the issue

### [PR microsoft/TypeScript#64385](https://github.com/microsoft/TypeScript/pull/64385) (Open, `For Backlog Bug`)

**Fix panic when declaration emit resolves an oversized tuple type**

*Declaration-only mode panics with a nil pointer when resolving tuple types exceeding size limits.*

 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/64385#issuecomment-5787625510) **jakebailey** said "@weswigham Do you have any thoughts about this?"
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/64385#issuecomment-5788183773) **weswigham** identified potential instability in the currentNode error-reporting mechanism under arbitrary entrypoints and suggested reporting diagnostics on the type symbol's declaration to remove currentNode dependence
 * [later](https://github.com/microsoft/TypeScript/pull/64385#issuecomment-5831934164) **mohit-nayak** described a caching issue where an error type was cached causing later type checks to skip normalization, prototyped a fix by adjusting currentNode around SerializeTypeForDeclaration, noted test results and caveats, and asked whether to split the context node fix into a separate PR or include it in this one

### [PR microsoft/TypeScript#64401](https://github.com/microsoft/TypeScript/pull/64401) (Open, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**\[api\] Add createIncrementalProgram**

*Implement createIncrementalProgram API enabling emit to update program state by returning a new snapshot and program.*

 * [today](https://github.com/microsoft/TypeScript/pull/64401#issuecomment-5815323902) **dragomirtitian** noted that createIncrementalProgram didn’t accept a VFS and described a workaround using createSnapshot while warning that it relies on internal APIs
 * [today](https://github.com/microsoft/TypeScript/pull/64401#issuecomment-5816166836) **andrewbranch** asked for elaboration and explained how VFS applies to snapshots and how to manage program disposal
 * [today](https://github.com/microsoft/TypeScript/pull/64401#issuecomment-5817588790) **andrewbranch** noted that bypassing snapshots via the convenience method can be confusing and that proper snapshot management is required when using an incremental program
 * [today](https://github.com/microsoft/TypeScript/pull/64401#issuecomment-5820882076) **dragomirtitian** stated that manually managing the snapshot was acceptable and that the convenience method was not useful to them but might benefit others not using a VFS

### [Issue microsoft/TypeScript#64405](https://github.com/microsoft/TypeScript/issues/64405) (Closed, `Needs Investigation`, **johnfav03**)

**Incremental check emits locationless TS2589 after a comment\-only edit in TypeScript 7**

*TypeScript 7’s incremental compiler erroneously emits a locationless TS2589 error after a comment-only edit despite cold and fresh checks passing.*

 * [yesterday](https://github.com/microsoft/TypeScript/issues/64405#issuecomment-5807077937) **rexdotsh** provided a stronger repro showing TS2589 on b.ts and described its behavior on rebuilds
 * [yesterday](https://github.com/microsoft/TypeScript/issues/64405#issuecomment-5807553357) **jakebailey** mentioned having a branch with broad fixes, said they would check later if the new repro was related, and suspected someone else would need to verify due to its complexity
 * [today](https://github.com/microsoft/TypeScript/issues/64405#issuecomment-5811839641) **rexdotsh** said "Sure, appreciate it!"
 * [later](https://github.com/microsoft/TypeScript/issues/64405#issuecomment-5829231426) **mhalikosen** described a recursive JSON type mapping failure in Hono v7.1.0-dev.20260924.1 compared to v6.0.3 and supplied a minimal TypeScript repro

### [PR microsoft/TypeScript#64409](https://github.com/microsoft/TypeScript/pull/64409) (Closed, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Onboard the \`lib\` task to code generation caching and include it in \`generate\`**

*Integrate the lib task into code generation caching and the generate command to prevent missing diffs in CI.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/64409#issuecomment-5799603718) **jakebailey** said "I'm surprised this is needed, isn't it just a copy? What diffs do you mean?"
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64409#issuecomment-5802179227) **weswigham** explained that the script also deleted outdated lib files, noted the target libs aren’t in git, and suggested including the deletion process in the codegen task set
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64409#issuecomment-5803155730) **jakebailey** explained that there is no code generation beyond copying from the DOM lib generator and questioned if this process qualifies as codegen since other generators produce committed artifacts
 * [today](https://github.com/microsoft/TypeScript/pull/64409#issuecomment-5818725139) **weswigham** said "Alright, we can just leave it as-is, not like it saves any real amount time to make a basic copy option incremental anyway."
 * (today) **weswigham** closed the issue

### [Issue microsoft/TypeScript#64412](https://github.com/microsoft/TypeScript/issues/64412) (Open)

**Crash in getLocalModuleSpecifier when formatting a type: normalizeSlashes receives undefined \(regression in 6\.0\)**

*TypeScript 6.0.3 regression crash in getLocalModuleSpecifier because normalizeSlashes gets undefined after ESLint fix-dry-run.*

 * created by **AlexisDevMaster**
 * [today](https://github.com/microsoft/TypeScript/issues/64412#issuecomment-5826112137) **yksr-melt** identified the cause of a TypeError in getLocalModuleSpecifier due to an undefined base directory when imports resolution is enabled without paths or baseUrl, reproduced it in a unit test, and proposed a one-line fallback patch while asking if a PR against release-6.0 would be accepted

### [PR microsoft/TypeScript#64413](https://github.com/microsoft/TypeScript/pull/64413) (Closed, `For Backlog Bug`)

**Defer constraint checks on inferred type arguments that mention an unresolved accessor**

*Eager constraint checking of inferred Zod type arguments referencing unresolved accessors triggers TS7023 recursion errors.*

 * created by **colinhacks**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64413#issuecomment-5804517605) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (today) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`

### [Issue microsoft/TypeScript#64415](https://github.com/microsoft/TypeScript/issues/64415) (Closed, `Possible Improvement`)

**Constraint check resolves an un\-annotated accessor while its object literal is still being inferred**

*Constraint checking in TypeScript prematurely resolves an unannotated accessor while its object literal type is still being inferred.*

 * created by **colinhacks**
 * [today](https://github.com/microsoft/TypeScript/issues/64415#issuecomment-5817314329) **ahejlsberg** explained that the `this` references in the `"~standard"` property inject an extra type parameter causing sensitivity to circularities
 * (today) **RyanCavanaugh** added label `Possible Improvement`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/64415#issuecomment-5824032707) **colinhacks** explained that removing `this` from the base cleared the small repro but not the library because ZodType and each classic schema interface redeclare “~standard” through a subtype which resolves during the check, and provided a detailed repro closer to the library
 * [today](https://github.com/microsoft/TypeScript/issues/64415#issuecomment-5824083540) **ahejlsberg** explained why the “~standard” property caused an issue and proposed heuristics to avoid unnecessary member resolution in intersection reduction checks
 * [later](https://github.com/microsoft/TypeScript/issues/64415#issuecomment-5834499211) **colinhacks** said "Thanks Anders!"

### [Issue microsoft/TypeScript#64416](https://github.com/microsoft/TypeScript/issues/64416) (Closed, `Crash`, **DanielRosenwasser**, **Copilot**)

**Fatal language server crash during auto\-imports**

*Language server crashes with a fatal internal error while auto-importing JSX runtime specifiers.*

 * (yesterday) **DanielRosenwasser** added label `Crash`, and assigned to **Copilot**, **DanielRosenwasser**
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript#64417](https://github.com/microsoft/TypeScript/pull/64417) (Closed, `For Uncommitted Bug`, **DanielRosenwasser**, **Copilot**)

**Prevent auto\-import crash with automatic JSX runtime**

*Add missing runtime-specifier handling in aliasResolver to avoid crashes during auto-import with automatic JSX runtime*

 * [today](https://github.com/microsoft/TypeScript/pull/64417#issuecomment-5816459024) **andrewbranch** instructed the tool to determine possible paths between the call stack top and auto-import checker functions and to create a fourslash test for the failure
 * [today](https://github.com/microsoft/TypeScript/pull/64417#issuecomment-5816946290) **andrewbranch** said "Since it stopped with an error, I wonder if the test actually fails without the fix 🤔 "
 * [today](https://github.com/microsoft/TypeScript/pull/64417#issuecomment-5816954487) **Copilot** described the production path for auto-import processing, noted the commit that addressed it, and confirmed that the new fourslash completion test and validation passed
 * [today](https://github.com/microsoft/TypeScript/pull/64417#issuecomment-5819423908) **Copilot** added a project-reference test case and verified that it fails with the old implementation and passes with the fix
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript#64419](https://github.com/microsoft/TypeScript/pull/64419) (Open, `For Uncommitted Bug`, **DanielRosenwasser**, **Copilot**)

**Prevent nil dereference during package export resolution**

*Package export/import resolution treats absent tables as empty to avoid nil dereferences during program construction.*

 * (yesterday) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64419#issuecomment-5823308975) **DanielRosenwasser** said "@copilot you need a realistic test case that is not just a unit test"

### [Issue microsoft/TypeScript#64423](https://github.com/microsoft/TypeScript/issues/64423) (Open, `Needs More Info`)

**TypeScript 7\.0\.2 silently runs out of memory while typechecking a project that TypeScript 6\.0\.3 checks successfully**

*TypeScript 7.0.2’s typechecker exhausts memory and fails on a project that compiles successfully under TypeScript 6.0.3.*

 * created by **Amatewasu**
 * [today](https://github.com/microsoft/TypeScript/issues/64423#issuecomment-5818775324) **ahejlsberg** said "Can you try TS6 with the --stableTypeOrdering flag to see if this is related to type ordering?"
 * **RyanCavanaugh** added label `Needs More Info`
 * [today](https://github.com/microsoft/TypeScript/issues/64423#issuecomment-5828271795) **Amatewasu** provided TypeScript compiler output showing a fatal heap out of memory error
 * [later](https://github.com/microsoft/TypeScript/issues/64423#issuecomment-5828937397) **Amatewasu** reported LLM-generated investigation findings including measurements and a minimal reproduction for a TypeScript 7.0.2 OOM issue

### [PR microsoft/TypeScript#64426](https://github.com/microsoft/TypeScript/pull/64426) (Open, `For Uncommitted Bug`)

**Type a recursive call\-initialized object literal property lazily**

*Enable object literal properties initialized by function calls to be typed lazily to handle recursive types.*

 * created by **ethndotsh**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64426#issuecomment-5817989945) **ethndotsh** said "@microsoft-github-policy-service agree"

### [PR microsoft/TypeScript#64427](https://github.com/microsoft/TypeScript/pull/64427) (Closed, `For Uncommitted Bug`)

**Feature/module expressions**

*Introduce module expressions to allow modules to be used as first-class expressions in code.*

 * created by **adrianhunter**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64427#issuecomment-5818047556) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (today) **adrianhunter** closed the issue

### [PR microsoft/TypeScript#64428](https://github.com/microsoft/TypeScript/pull/64428) (Open, `For Uncommitted Bug`, **andrewbranch**, **Copilot**)

**Deduplicate content\-mapped inlay hints**

*Remove duplicate inlay hints from split content-mapped ranges by deduplicating their serialized LSP representations and adding tests.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **andrewbranch**
 * (today) **typescript-automation[bot]** added labels `For Milestone Bug`, `For Milestone Bug`, `For Uncommitted Bug`, and removed label `For Milestone Bug`

### [Issue microsoft/TypeScript#64429](https://github.com/microsoft/TypeScript/issues/64429) (Open, `API Request`, **andrewbranch**)

**\[api\] Add back missing: \`setEmitFlags\` and \`addSynthetic\*Comment\`**

*Add missing Go API support for TypeScript's EmitFlags and synthetic comment functions to control node emission.*

 * created by **dragomirtitian**

### [Issue microsoft/TypeScript#64430](https://github.com/microsoft/TypeScript/issues/64430) (Open, `Needs Investigation`)

**Declarations in \`declare global\` can have \`export\` modifiers**

*TypeScript permits export modifiers on declarations inside declare global blocks, prompting questions about whether this behavior is intentional.*

 * created by **DanielRosenwasser**

### [Issue microsoft/TypeScript#64431](https://github.com/microsoft/TypeScript/issues/64431) (Open, `Bug`, **RyanCavanaugh**, **Copilot**)

**TS7031 false positive for nested object binding pattern with \`= {}\` default in an annotated parameter \(regression from \#64043\)**

*Nested object destructuring with default {} in a typed parameter erroneously triggers TS7031 errors after PR #64043*

 * created by **trevorade**
 * (today) **RyanCavanaugh** added label `Bug`, and assigned to **Copilot**, **RyanCavanaugh**

### [PR microsoft/TypeScript#64432](https://github.com/microsoft/TypeScript/pull/64432) (Open, `Author: Team`, `For Backlog Bug`, **jakebailey**, **johnfav03**)

**Fixes for recursive declarations, elided placeholders, cycles**

*Error on elided placeholders, detect deferred type cycles, and preserve recursive and reverse-mapped types during TypeScript declaration emit.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Backlog Bug`, and assigned to **jakebailey**, **johnfav03**
 * [today](https://github.com/microsoft/TypeScript/pull/64432#issuecomment-5822647441) **jakebailey** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/64432#issuecomment-5822648561) **typescript-automation[bot]** reported build job statuses and encountered an access denied error for the 'run dt' job
 * [today](https://github.com/microsoft/TypeScript/pull/64432#issuecomment-5822729486) **jakebailey** requested the typescript-bot to run dt as a test
 * [today](https://github.com/microsoft/TypeScript/pull/64432#issuecomment-5822730634) **typescript-automation[bot]** reported that jobs had started and that the comment would be updated as builds progress
 * [today](https://github.com/microsoft/TypeScript/pull/64432#issuecomment-5822967924) **typescript-automation[bot]** provided the requested performance run results
 * [today](https://github.com/microsoft/TypeScript/pull/64432#issuecomment-5823043234) **typescript-automation[bot]** reported user tests results comparing main and the pull request merge, noted infrastructure failures and type errors in puppeteer and webpack
 * [today](https://github.com/microsoft/TypeScript/pull/64432#issuecomment-5823485789) **typescript-automation[bot]** reported results of running tsc on the top 400 repos comparing main and the PR merge and highlighted build failures in different-ai/openwork and facebook/docusaurus due to TS5088 cyclic type errors
 * [today](https://github.com/microsoft/TypeScript/pull/64432#issuecomment-5826928778) **jakebailey** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/64432#issuecomment-5826929667) **typescript-automation[bot]** posted build job status updates
 * [today](https://github.com/microsoft/TypeScript/pull/64432#issuecomment-5827194747) **typescript-automation[bot]** reported the requested perf run results including compiler-union metrics
 * [today](https://github.com/microsoft/TypeScript/pull/64432#issuecomment-5827364888) **typescript-automation[bot]** notified that the DT test run failed and provided a link to the log
 * [today](https://github.com/microsoft/TypeScript/pull/64432#issuecomment-5827456449) **typescript-automation[bot]** reported tsc comparison results against main, highlighted infrastructure failures and new type errors in Puppeteer and Webpack, and requested review
 * [today](https://github.com/microsoft/TypeScript/pull/64432#issuecomment-5827557632) **typescript-automation[bot]** notified that the DT test run failed and linked to the logs
 * [today](https://github.com/microsoft/TypeScript/pull/64432#issuecomment-5827995661) **typescript-automation[bot]** posted tsc comparison results for top 400 repos and requested review
 * [later](https://github.com/microsoft/TypeScript/pull/64432#issuecomment-5828424780) **jakebailey** said "@typescript-bot test top1000"
 * [later](https://github.com/microsoft/TypeScript/pull/64432#issuecomment-5828425855) **typescript-automation[bot]** reported that the test top1000 job started and provided status and results links
 * [later](https://github.com/microsoft/TypeScript/pull/64432#issuecomment-5829950122) **typescript-automation[bot]** reported build comparison results between main and the pull request merge for top 1000 repositories, noting several build failures due to cyclic type inference errors
 * [later](https://github.com/microsoft/TypeScript/pull/64432#issuecomment-5829950675) **typescript-automation[bot]** reported build errors from running the top 1000 repos suite for NomicFoundation/hardhat
 * [later](https://github.com/microsoft/TypeScript/pull/64432#issuecomment-5829951254) **typescript-automation[bot]** reported that 144 of 147 projects failed to build with the old tsc and highlighted a cyclic type inference error in teableio/teable

### [Issue microsoft/TypeScript#64433](https://github.com/microsoft/TypeScript/issues/64433) (Open, `Bug`, `Help Wanted`)

**empty mappings in \.d\.ts\.map for export default of a non\-identifier expression**

*Exporting an anonymous object literal as default in TypeScript 7.0 yields empty .d.ts.map mappings, unlike previous versions or named exports.*

 * created by **dragomirtitian**

### [PR microsoft/TypeScript#64434](https://github.com/microsoft/TypeScript/pull/64434) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**\[api\] Give standalone created files a tracked identity and incorporate with the parse cache**

*Modify createSourceFile API to use a global parse cache and return disposable leases for identity consistency.*

 * created by **andrewbranch**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`, and assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript/pull/64434#issuecomment-5823148741) **jakebailey** said "What if you just want a throwaway AST and don't care about equality or reuse?"
 * [today](https://github.com/microsoft/TypeScript/pull/64434#issuecomment-5823204073) **andrewbranch** said "Then using it or otherwise dispose it when you're ready to throw it away, or don't and it will get released when you close the API"
 * [today](https://github.com/microsoft/TypeScript/pull/64434#issuecomment-5823240240) **andrewbranch** described that binder symbol follow-up creates a confusing bifurcation because untracked throwaway SourceFiles cannot fetch or assign binder symbols using server identity methods
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript#64435](https://github.com/microsoft/TypeScript/issues/64435) (Open, `Bug`, **weswigham**)

**Declaration emit: expando alias assignment \(\`F\.x = someIdentifier\`\) un\-exports the other expando members in the generated namespace**

*tsgo emits alias assignments in namespaces as export declarations, which inadvertently un-exports other expando members in the generated .d.ts file.*

 * created by **trevorade**

### [Issue microsoft/TypeScript#64436](https://github.com/microsoft/TypeScript/issues/64436) (Closed, `Not a Defect`)

**\`\-\-experimentalDecorators\`: leading comment on a decorated constructor parameter is emitted in JS output \(tsc drops it\)**

*With experimentalDecorators enabled, tsgo emits JSDoc comments on decorated constructor parameters in JavaScript output while tsc omits them.*

 * created by **trevorade**
 * **RyanCavanaugh** added label `Not a Defect`
 * [today](https://github.com/microsoft/TypeScript/issues/64436#issuecomment-5823701251) **RyanCavanaugh** clarified that comment emit is best effort and suggested tooling read the upstream source to determine comment applicability

### [Issue microsoft/TypeScript#64437](https://github.com/microsoft/TypeScript/issues/64437) (Open)

**\`keyof\` over computed property keys yields widening literal types, unlike the same object with literal keys**

*TypeScript’s keyof on computed property keys widens to string instead of the expected literal union types like literal keys.*

 * created by **trevorade**
 * [today](https://github.com/microsoft/TypeScript/issues/64437#issuecomment-5823578128) **RyanCavanaugh** pointed out that using literal types for keys also provides consistency and questioned why the proposed consistency is more important than the current one
 * [today](https://github.com/microsoft/TypeScript/issues/64437#issuecomment-5823625228) **RyanCavanaugh** said "Can you explain more on the .d.ts / enum scenario? I don't think E.A | E.B -> E is a widening behavior, at least not as I understand it in this context"
 * **RyanCavanaugh** added label `Needs More Info`
 * [today](https://github.com/microsoft/TypeScript/issues/64437#issuecomment-5826258900) **trevorade** explained how keyof on enum-keyed maps now widens enum literals due to .d.ts changes and described potential workarounds

### [Issue microsoft/TypeScript#64438](https://github.com/microsoft/TypeScript/issues/64438) (Open, `Bug`, `Help Wanted`, `Good First Issue`)

**Incorrect/unhelpful error message for non\-module jsx file**

*TypeScript shows misleading missing module errors for JSX in non-module scripts instead of stating scripts cannot import modules.*

 * created by **calebegg**
 * [today](https://github.com/microsoft/TypeScript/issues/64438#issuecomment-5823431352) **DanielRosenwasser** acknowledged the suggestion and recommended specifying "moduleDetection": "force" to emulate "jsx": "preserve" behavior and suggested updating the docs
 * (today) **DanielRosenwasser** added labels `Bug`, `Help Wanted`, `Good First Issue`
 * [today](https://github.com/microsoft/TypeScript/issues/64438#issuecomment-5826551653) **sh011** said "Hi @calebegg @DanielRosenwasser I went through the issue and found that the diagnostic chain needs to be looked up properly. I would like to work on this issue, can you please assign it to me. Thanks!"

### [PR microsoft/TypeScript#64439](https://github.com/microsoft/TypeScript/pull/64439) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**Add AST helpers used by api\-extractor**

*Add AST helpers isExternalModule, getCombinedModifierFlags, and getNameOfDeclaration for api-extractor use.*

 * created by **andrewbranch**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **andrewbranch**

### [PR microsoft/TypeScript#64440](https://github.com/microsoft/TypeScript/pull/64440) (Open, `For Uncommitted Bug`, **RyanCavanaugh**, **Copilot**)

**Fix false implicit\-any errors in annotated nested bindings**

*Nested object destructuring defaults were erroneously reported as implicit any even with parameter type annotations.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * (today) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/64440#issuecomment-5835281784) **RyanCavanaugh** said "@copilot mcfly this and also explain why this is a correct fix"

### [PR microsoft/TypeScript#64441](https://github.com/microsoft/TypeScript/pull/64441) (Closed, `Author: Team`, `For Uncommitted Bug`, **RyanCavanaugh**)

**Rename restack \-\> McFly**

*Rename restack to McFly to avoid unintentional invocation.*

 * created by **RyanCavanaugh**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **RyanCavanaugh**
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#64442](https://github.com/microsoft/TypeScript/pull/64442) (Open, `For Milestone Bug`, **RyanCavanaugh**)

**Loosen lib types for string methods that internally call %Symbol\.\*% methods**

*Loosen TypeScript string method type definitions to preserve parameter and return types for custom objects implementing well-known symbol methods.*

 * created by **graphemecluster**
 * (today) **typescript-automation[bot]** added label `For Milestone Bug`, and assigned to **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript/pull/64442#issuecomment-5824386785) **DanielRosenwasser** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/64442#issuecomment-5824387728) **typescript-automation[bot]** posted build job statuses with commands and result links
 * [today](https://github.com/microsoft/TypeScript/pull/64442#issuecomment-5824628416) **typescript-automation[bot]** reported performance run results comparing baseline and PR metrics
 * [today](https://github.com/microsoft/TypeScript/pull/64442#issuecomment-5824693554) **typescript-automation[bot]** reported test results comparing main and pull request merge, noted infrastructure failures and new type errors in puppeteer and webpack
 * [today](https://github.com/microsoft/TypeScript/pull/64442#issuecomment-5825098380) **typescript-automation[bot]** reported build results comparing main and pull request on the top 400 repositories, noted errors in several projects, and requested review
 * [today](https://github.com/microsoft/TypeScript/pull/64442#issuecomment-5827335704) **typescript-automation[bot]** reported that the DT test results were ready and unchanged

### [PR microsoft/TypeScript#64443](https://github.com/microsoft/TypeScript/pull/64443) (Open, `For Backlog Bug`)

**Report the member name instead of the signature in deprecation suggestions**

*Change deprecation suggestion logic to display member names for calls on non-plain receivers by stripping parentheses instead of showing signatures.*

 * created by **gonappuccino**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64443#issuecomment-5827010920) **gonappuccino** said "@microsoft-github-policy-service agree"

### [PR microsoft/TypeScript#64444](https://github.com/microsoft/TypeScript/pull/64444) (Closed, `For Uncommitted Bug`)

**Add regression test for JSX runtime resolution in scripts**

*Add regression test for script-based JSX runtime resolution using jsxImportSource to ensure correct JSX.Element resolution without misleading diagnostics*

 * created by **germanao**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/64444#issuecomment-5832793745) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [later](https://github.com/microsoft/TypeScript/pull/64444#issuecomment-5832953146) **germanao** said "@microsoft-github-policy-service agree"
 * (later) **germanao** closed the issue

### [PR microsoft/TypeScript#64445](https://github.com/microsoft/TypeScript/pull/64445) (Open, `For Uncommitted Bug`)

**Improve diagnostic for implicit JSX runtime imports in non\-module files**

*Add a new diagnostic TS2884 to provide clearer error messages for implicit JSX runtime imports in non-module files.*

 * created by **sh011**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/64445#issuecomment-5833304536) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [later](https://github.com/microsoft/TypeScript/pull/64445#issuecomment-5833335173) **sh011** said "@microsoft-github-policy-service agree"

