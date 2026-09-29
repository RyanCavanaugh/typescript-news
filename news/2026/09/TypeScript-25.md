# Report for 2026-09-25 (Friday, September 25th, 2026)

19 different users commented on 49 different issues.

## Recommended Actions

 * Response Recommended
    * @resure provided repro steps and benchmark results in [microsoft/TypeScript#63830](https://github.com/microsoft/TypeScript/issues/63830#issuecomment-5845592914)
    * @adilalperenciftci asked for feedback on the revised getUnionSignatures arity expansion in [microsoft/TypeScript#64360](https://github.com/microsoft/TypeScript/pull/64360#issuecomment-5843031820)
    * @typescript-automation[bot] reported a server panic during textDocument/diagnostic in [microsoft/TypeScript#64456](https://github.com/microsoft/TypeScript/issues/64456#issuecomment-5840616053)
    * @typescript-automation[bot] provided repro steps and error report in [microsoft/TypeScript#64456](https://github.com/microsoft/TypeScript/issues/64456#issuecomment-5840616939)
    * @typescript-automation[bot] reported a server connection error during analysis in [microsoft/TypeScript#64456](https://github.com/microsoft/TypeScript/issues/64456#issuecomment-5840617420)
    * @typescript-automation[bot] reported a server connection closed prematurely error for parcel-bundler/parcel in [microsoft/TypeScript#64456](https://github.com/microsoft/TypeScript/issues/64456#issuecomment-5840617867)
    * @typescript-automation[bot] reported a panic in textDocument/diagnostic logs in [microsoft/TypeScript#64456](https://github.com/microsoft/TypeScript/issues/64456#issuecomment-5840618913)
    * @typescript-automation[bot] posted an error stack trace in [microsoft/TypeScript#64458](https://github.com/microsoft/TypeScript/issues/64458#issuecomment-5841264031)
    * @typescript-automation[bot] reported a panic in textDocument/diagnostic in [microsoft/TypeScript#64458](https://github.com/microsoft/TypeScript/issues/64458#issuecomment-5841264366)
    * @typescript-automation[bot] reported a panic in textDocument/diagnostic that needs investigation in [microsoft/TypeScript#64458](https://github.com/microsoft/TypeScript/issues/64458#issuecomment-5841264706)
    * @typescript-automation[bot] reported a panic in textDocument/diagnostic due to unhandled ast.KeywordExpression in [microsoft/TypeScript#64458](https://github.com/microsoft/TypeScript/issues/64458#issuecomment-5841265072)
    * @typescript-automation[bot] reported a panic crash in [microsoft/TypeScript#64458](https://github.com/microsoft/TypeScript/issues/64458#issuecomment-5841265407)
    * @typescript-automation[bot] reported a runtime panic stack trace in [microsoft/TypeScript#64458](https://github.com/microsoft/TypeScript/issues/64458#issuecomment-5841265724)
    * @typescript-automation[bot] reported a panic stack trace in [microsoft/TypeScript#64458](https://github.com/microsoft/TypeScript/issues/64458#issuecomment-5841266065)
    * @typescript-automation[bot] reported a debug failure panic in [microsoft/TypeScript#64458](https://github.com/microsoft/TypeScript/issues/64458#issuecomment-5841266398)
    * @typescript-automation posted panic report for textDocument/diagnostic in [microsoft/TypeScript#64458](https://github.com/microsoft/TypeScript/issues/64458#issuecomment-5841266768)
    * @typescript-automation reported a panic stack trace during type checking in [microsoft/TypeScript#64458](https://github.com/microsoft/TypeScript/issues/64458#issuecomment-5841267073)
    * @typescript-automation[bot] reported a panic in textDocument/diagnostic in [microsoft/TypeScript#64458](https://github.com/microsoft/TypeScript/issues/64458#issuecomment-5841267766)
    * @typescript-automation[bot] reported a panic in JSX transformer in [microsoft/TypeScript#64458](https://github.com/microsoft/TypeScript/issues/64458#issuecomment-5841268082)
    * @typescript-automation[bot] reported panic logs for textDocument/diagnostic on transloadit/uppy in [microsoft/TypeScript#64458](https://github.com/microsoft/TypeScript/issues/64458#issuecomment-5841268409)
    * @typescript-automation[bot] reported a server connection closed prematurely error in [microsoft/TypeScript#64458](https://github.com/microsoft/TypeScript/issues/64458#issuecomment-5841268718)
    * @typescript-automation[bot] reported a server connection closed prematurely error in [microsoft/TypeScript#64458](https://github.com/microsoft/TypeScript/issues/64458#issuecomment-5841268998)
    * @typescript-automation[bot] provided repro steps in [microsoft/TypeScript#64458](https://github.com/microsoft/TypeScript/issues/64458#issuecomment-5841269376)
    * @typescript-automation[bot] provided error report and repro steps in [microsoft/TypeScript#64458](https://github.com/microsoft/TypeScript/issues/64458#issuecomment-5841269708)
    * @typescript-automation[bot] reported server connection closed prematurely error in [microsoft/TypeScript#64458](https://github.com/microsoft/TypeScript/issues/64458#issuecomment-5841270070)
    * @typescript-automation[bot] reported panic in JSX transformer due to KindBinaryExpression in [microsoft/TypeScript#64458](https://github.com/microsoft/TypeScript/issues/64458#issuecomment-5841270413)

## Activity Summary

### [Issue microsoft/TypeScript#63807](https://github.com/microsoft/TypeScript/issues/63807) (Open, `Possible Improvement`)

**Proposal: Flatten the AST to speed up tsgo**

*Proposes flattening tsgo’s AST into a flat array to reduce garbage collection scanning overhead and improve performance.*

 * [26 weeks ago](https://github.com/microsoft/TypeScript/issues/63807#issuecomment-5351502165) **ahejlsberg** suggested disabling GC for command-line compiles due to minimal GC-eligible allocations
 * [26 weeks ago](https://github.com/microsoft/TypeScript/issues/63807#issuecomment-5351502186) **no-yan** clarified that the goal was reducing GC scan cost rather than DoD/locality, explained that GC still scans contiguous nodes containing pointers, suggested making large pointer-free regions to avoid scanning, and recommended disabling or tuning GC for command-line compiles
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63807#issuecomment-5826174145) **no-yan** reported migrating TypeScript's AST to a store-based representation, highlighted performance improvements, and solicited feedback on the design
 * [today](https://github.com/microsoft/TypeScript/issues/63807#issuecomment-5840843205) **RyanCavanaugh** observed that parsing is trivially parallelizable but overall pipeline performance gains require refactoring the checker due to increased memory traffic and potential Store+index bugs
 * [today](https://github.com/microsoft/TypeScript/issues/63807#issuecomment-5841085160) **andrewbranch** mentioned that the binary format resembles the API’s AST encoder output, expressed regret about not parsing directly into a buffer for zero-copy NAPI usage, and suggested the proposal is almost sufficient to share storage with a JS client

### [Issue microsoft/TypeScript#63830](https://github.com/microsoft/TypeScript/issues/63830) (Open, `Needs More Info`)

**Declaration emit spends significant CPU in getAliasForSymbolInContainer / getAlternativeContainingModules**

*Declaration emit spends excessive CPU time in getAlternativeContainingModules and getAliasForSymbolInContainer, causing slow builds.*

 * [16 weeks ago](https://github.com/microsoft/TypeScript/issues/63830#issuecomment-5351504786) **jakebailey** said "It would be good to be able to get access to this, I'm not really sure I like the way microsoft/typescript-go#4102 looks..."
 * **RyanCavanaugh** added label `Needs More Info`
 * [15 weeks ago](https://github.com/microsoft/TypeScript/issues/63830#issuecomment-5351504818) **Zzzen** thanked maintainers, explained inability to share private code, offered sanitized profiling data and benchmark runs, and offered to rework the PR or treat it as evidence for the hotspot
 * [later](https://github.com/microsoft/TypeScript/issues/63830#issuecomment-5845592914) **resure** provided a public synthetic repro in issue #64464 and reported performance metrics across multiple versions, noting build shape differences

### [PR microsoft/TypeScript#64130](https://github.com/microsoft/TypeScript/pull/64130) (Open, `For Uncommitted Bug`)

**Implement workspace/diagnostics**

*Implement workspace/diagnostics LSP support in the TypeScript server with feature-flagged dynamic registration to avoid default VSCode polling overhead.*

 * created by **eagarwal-notion**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [3 weeks ago](https://github.com/microsoft/TypeScript/pull/64130#issuecomment-5501310074) **eagarwal-notion** said "@microsoft-github-policy-service agree company="Notion""
 * [today](https://github.com/microsoft/TypeScript/pull/64130#issuecomment-5841112113) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."

### [PR microsoft/TypeScript#64158](https://github.com/microsoft/TypeScript/pull/64158) (Closed, `Author: Team`, `For Uncommitted Bug`, **iisaduan**)

**Build Orchestrator API **

*Introduce a BuildOrchestrator API in TS7.1 replacing SolutionBuilder to perform project builds, cleans, and their references with customizable options.*

 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64158#issuecomment-5732995165) **andrewbranch** described how declaration file AST caching now works automatically via strategic program snapshots, referenced Jake’s prototype commit, and mentioned developing a snapshot-backed incremental program prototype for future testing
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/64158#issuecomment-5766275697) **dragomirtitian** acknowledged automatic parse cache behavior, noted uncertainty about its reliability, and expressed eagerness to try the upcoming prototype
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/64158#issuecomment-5786468443) **andrewbranch** said "@dragomirtitian I have a draft up at https://github.com/microsoft/TypeScript/pull/64401; it probably has some bugs, but can you see if that direction meets your needs?"
 * [today](https://github.com/microsoft/TypeScript/pull/64158#issuecomment-5839239607) **andrewbranch** said "It would probably be worthwhile to update the PR description to reflect the latest review changes since PRs are all the docs we have for the moment."
 * (today) **iisaduan** closed the issue

### [PR microsoft/TypeScript#64360](https://github.com/microsoft/TypeScript/pull/64360) (Open, `For Backlog Bug`)

**Fix union overload signature ordering instability**

*Generate exact-arity variants for union signatures with optional parameters to ensure stable overload resolution without ad-hoc sorting.*

 * [5 days ago](https://github.com/microsoft/TypeScript/pull/64360#issuecomment-5748296015) **adilalperenciftci** said "@microsoft-github-policy-service agree"
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/64360#issuecomment-5766137973) **jakebailey** said "This seems a bit too ad-hoc and out of place for the kind of thing we normally do. It is suspicious that nothing else changed, either, and that it's purely additive?"
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/64360#issuecomment-5767834549) **adilalperenciftci** dropped the post-sorting approach and replaced it with expanding optional-parameter signatures into exact-arity variants in getUnionSignatures so findMatchingSignatures matches without extra sorting
 * [today](https://github.com/microsoft/TypeScript/pull/64360#issuecomment-5843031820) **adilalperenciftci** rebased cleanly on current main and asked if the revised getUnionSignatures arity expansion was preferable or if union overload matching should be handled differently

### [PR microsoft/TypeScript#64401](https://github.com/microsoft/TypeScript/pull/64401) (Open, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**\[api\] Add createIncrementalProgram**

*Implement createIncrementalProgram API enabling emit to update program state by returning a new snapshot and program.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/64401#issuecomment-5816166836) **andrewbranch** asked for elaboration and explained how VFS applies to snapshots and how to manage program disposal
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64401#issuecomment-5817588790) **andrewbranch** noted that bypassing snapshots via the convenience method can be confusing and that proper snapshot management is required when using an incremental program
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64401#issuecomment-5820882076) **dragomirtitian** stated that manually managing the snapshot was acceptable and that the convenience method was not useful to them but might benefit others not using a VFS
 * [today](https://github.com/microsoft/TypeScript/pull/64401#issuecomment-5840280714) **dragomirtitian** said "I tested our build tool with the changes in this PR. Shape of the API works for us. Everything seems to work. "
 * [today](https://github.com/microsoft/TypeScript/pull/64401#issuecomment-5840884268) **andrewbranch** said "Great! Do you see performance improvements over using non-incremental programs?"

### [PR microsoft/TypeScript#64404](https://github.com/microsoft/TypeScript/pull/64404) (Open, `Author: Team`, `For Milestone Bug`, **jakebailey**)

**Watch alias invalidation**

*Introduce a watchalias lookup to match filesystem paths with compiler-recognized file names so watch mode detects changes through symlinks.*

 * (3 days ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **typescript-automation[bot]** added label `For Milestone Bug`, and removed label `For Uncommitted Bug`

### [Issue microsoft/TypeScript#64405](https://github.com/microsoft/TypeScript/issues/64405) (Closed, `Needs Investigation`, **johnfav03**)

**Incremental check emits locationless TS2589 after a comment\-only edit in TypeScript 7**

*TypeScript 7’s incremental compiler erroneously emits a locationless TS2589 error after a comment-only edit despite cold and fresh checks passing.*

 * [2 days ago](https://github.com/microsoft/TypeScript/issues/64405#issuecomment-5807553357) **jakebailey** mentioned having a branch with broad fixes, said they would check later if the new repro was related, and suspected someone else would need to verify due to its complexity
 * [yesterday](https://github.com/microsoft/TypeScript/issues/64405#issuecomment-5811839641) **rexdotsh** said "Sure, appreciate it!"
 * [today](https://github.com/microsoft/TypeScript/issues/64405#issuecomment-5829231426) **mhalikosen** described a recursive JSON type mapping failure in Hono v7.1.0-dev.20260924.1 compared to v6.0.3 and supplied a minimal TypeScript repro
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#64421](https://github.com/microsoft/TypeScript/issues/64421) (Open, `Bug`, **weswigham**)

**panic: unexpected Expression: KindArrayBindingPattern \[recovered, repanicked\]**

*TypeScript’s compiler unexpectedly panics with an unexpected KindArrayBindingPattern error when printing nested array destructuring using a spread element.*

 * created by **YuanchengJiang**
 * (today) **RyanCavanaugh** added label `Bug`, set milestone to `Backlog`, and assigned to **weswigham**

### [PR microsoft/TypeScript#64422](https://github.com/microsoft/TypeScript/pull/64422) (Open, `For Milestone Bug`, **weswigham**)

**fix\(64421\): convert nested rest bindings to assignment targets**

*Convert nested rest bindings into valid assignment targets to correct destructuring behavior.*

 * created by **a-tarasyuk**
 * (yesterday) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * (today) **typescript-automation[bot]** added labels `For Backlog Bug`, `For Milestone Bug`, removed labels `For Uncommitted Bug`, `For Backlog Bug`, and assigned to **weswigham**

### [Issue microsoft/TypeScript#64424](https://github.com/microsoft/TypeScript/issues/64424) (Open, **johnfav03**)

**\`tsc \-b \-\-watch\` doesn't rebuild when an imported file changes, unless \`incremental\` is on**

*The tsc build watch mode fails to rebuild when imported files change unless incremental or composite compilation is enabled.*

 * created by **Generalsimus**
 * **RyanCavanaugh** assigned to **johnfav03**

### [Issue microsoft/TypeScript#64425](https://github.com/microsoft/TypeScript/issues/64425) (Open, **johnfav03**)

**\`tsc \-\-watch\` doesn't pick up changes when the project is in a shallow folder like \`/app\`**

*TypeScript watch mode stops detecting changes in shallow project folders like /app after a new path-depth check introduced in v7*

 * created by **Generalsimus**
 * **RyanCavanaugh** assigned to **johnfav03**

### [Issue microsoft/TypeScript#64429](https://github.com/microsoft/TypeScript/issues/64429) (Open, `API Request`, **andrewbranch**)

**\[api\] Add back missing: \`setEmitFlags\` and \`addSynthetic\*Comment\`**

*Add missing Go API support for TypeScript's EmitFlags and synthetic comment functions to control node emission.*

 * created by **dragomirtitian**
 * (today) **RyanCavanaugh** added label `API Request`, and assigned to **andrewbranch**

### [Issue microsoft/TypeScript#64430](https://github.com/microsoft/TypeScript/issues/64430) (Open, `Needs Investigation`)

**Declarations in \`declare global\` can have \`export\` modifiers**

*TypeScript permits export modifiers on declarations inside declare global blocks, prompting questions about whether this behavior is intentional.*

 * created by **DanielRosenwasser**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and set milestone to `Backlog`

### [PR microsoft/TypeScript#64432](https://github.com/microsoft/TypeScript/pull/64432) (Open, `Author: Team`, `For Backlog Bug`, **jakebailey**, **johnfav03**)

**Fixes for recursive declarations, elided placeholders, cycles**

*Error on elided placeholders, detect deferred type cycles, and preserve recursive and reverse-mapped types during TypeScript declaration emit.*

 * [today](https://github.com/microsoft/TypeScript/pull/64432#issuecomment-5829950122) **typescript-automation[bot]** reported build comparison results between main and the pull request merge for top 1000 repositories, noting several build failures due to cyclic type inference errors
 * [today](https://github.com/microsoft/TypeScript/pull/64432#issuecomment-5829950675) **typescript-automation[bot]** reported build errors from running the top 1000 repos suite for NomicFoundation/hardhat
 * [today](https://github.com/microsoft/TypeScript/pull/64432#issuecomment-5829951254) **typescript-automation[bot]** reported that 144 of 147 projects failed to build with the old tsc and highlighted a cyclic type inference error in teableio/teable
 * [today](https://github.com/microsoft/TypeScript/pull/64432#issuecomment-5836809889) **jakebailey** said "Thanks for the info. I guess more stuff to figure out."
 * [today](https://github.com/microsoft/TypeScript/pull/64432#issuecomment-5839341604) **jakebailey** noted that after talking with @ahejlsberg he submitted #64452 instead and said he would split out other parts of the big PR

### [Issue microsoft/TypeScript#64433](https://github.com/microsoft/TypeScript/issues/64433) (Open, `Bug`, `Help Wanted`)

**empty mappings in \.d\.ts\.map for export default of a non\-identifier expression**

*Exporting an anonymous object literal as default in TypeScript 7.0 yields empty .d.ts.map mappings, unlike previous versions or named exports.*

 * created by **dragomirtitian**
 * (today) **RyanCavanaugh** added labels `Bug`, `Help Wanted`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#64435](https://github.com/microsoft/TypeScript/issues/64435) (Open, `Bug`, **weswigham**)

**Declaration emit: expando alias assignment \(\`F\.x = someIdentifier\`\) un\-exports the other expando members in the generated namespace**

*tsgo emits alias assignments in namespaces as export declarations, which inadvertently un-exports other expando members in the generated .d.ts file.*

 * created by **trevorade**
 * (today) **RyanCavanaugh** added label `Bug`, set milestone to `TypeScript 7.1.1 RC`, and assigned to **weswigham**

### [Issue microsoft/TypeScript#64436](https://github.com/microsoft/TypeScript/issues/64436) (Closed, `Not a Defect`)

**\`\-\-experimentalDecorators\`: leading comment on a decorated constructor parameter is emitted in JS output \(tsc drops it\)**

*With experimentalDecorators enabled, tsgo emits JSDoc comments on decorated constructor parameters in JavaScript output while tsc omits them.*

 * created by **trevorade**
 * **RyanCavanaugh** added label `Not a Defect`
 * [yesterday](https://github.com/microsoft/TypeScript/issues/64436#issuecomment-5823701251) **RyanCavanaugh** clarified that comment emit is best effort and suggested tooling read the upstream source to determine comment applicability
 * [today](https://github.com/microsoft/TypeScript/issues/64436#issuecomment-5839843954) **trevorade** said "Thanks Ryan. We added a workaround in tsickle for this case."
 * (today) **trevorade** closed the issue

### [Issue microsoft/TypeScript#64437](https://github.com/microsoft/TypeScript/issues/64437) (Open)

**\`keyof\` over computed property keys yields widening literal types, unlike the same object with literal keys**

*TypeScript’s keyof on computed property keys widens to string instead of the expected literal union types like literal keys.*

 * [yesterday](https://github.com/microsoft/TypeScript/issues/64437#issuecomment-5823625228) **RyanCavanaugh** said "Can you explain more on the .d.ts / enum scenario? I don't think E.A | E.B -> E is a widening behavior, at least not as I understand it in this context"
 * **RyanCavanaugh** added label `Needs More Info`
 * [yesterday](https://github.com/microsoft/TypeScript/issues/64437#issuecomment-5826258900) **trevorade** explained how keyof on enum-keyed maps now widens enum literals due to .d.ts changes and described potential workarounds
 * **RyanCavanaugh** removed label `Needs More Info`

### [PR microsoft/TypeScript#64439](https://github.com/microsoft/TypeScript/pull/64439) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**Add AST helpers used by api\-extractor**

*Add AST helpers isExternalModule, getCombinedModifierFlags, and getNameOfDeclaration for api-extractor use.*

 * (yesterday) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#64440](https://github.com/microsoft/TypeScript/pull/64440) (Open, `For Uncommitted Bug`, **RyanCavanaugh**, **Copilot**)

**Fix false implicit\-any errors in annotated nested bindings**

*Nested object destructuring defaults were erroneously reported as implicit any even with parameter type annotations.*

 * (yesterday) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64440#issuecomment-5835281784) **RyanCavanaugh** said "@copilot mcfly this and also explain why this is a correct fix"
 * [today](https://github.com/microsoft/TypeScript/pull/64440#issuecomment-5836318835) **trevorade** reported that the fix passed their codebase tests and preserved nested callback types, but identified two regressions in object binding patterns and a missing baseline annotation in the tests

### [PR microsoft/TypeScript#64442](https://github.com/microsoft/TypeScript/pull/64442) (Open, `For Milestone Bug`, **RyanCavanaugh**)

**Loosen lib types for string methods that internally call %Symbol\.\*% methods**

*Loosen TypeScript string method type definitions to preserve parameter and return types for custom objects implementing well-known symbol methods.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/64442#issuecomment-5824693554) **typescript-automation[bot]** reported test results comparing main and pull request merge, noted infrastructure failures and new type errors in puppeteer and webpack
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64442#issuecomment-5825098380) **typescript-automation[bot]** reported build results comparing main and pull request on the top 400 repositories, noted errors in several projects, and requested review
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64442#issuecomment-5827335704) **typescript-automation[bot]** reported that the DT test results were ready and unchanged
 * [today](https://github.com/microsoft/TypeScript/pull/64442#issuecomment-5840289429) **graphemecluster** said "Does the mui-docs regression look related? Should I try removing the this parameters?"

### [PR microsoft/TypeScript#64446](https://github.com/microsoft/TypeScript/pull/64446) (Closed, `Author: Team`, `For Uncommitted Bug`, **RyanCavanaugh**)

**Clarify mcfly instructions**

*Clarify mcfly instructions to specify that pre-fix baselines must be included in the pre-fix commit.*

 * created by **RyanCavanaugh**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **RyanCavanaugh**
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#64447](https://github.com/microsoft/TypeScript/pull/64447) (Open, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**\[api\] Improve callback FS**

*Callback-based file system now mandates explicit implementations for all functions and moves createVirtualFileSystem to test utilities.*

 * created by **andrewbranch**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript/pull/64447#issuecomment-5836793512) **jakebailey** mentioned that requiring every key hinders interface expansion and asked if there’s a way to allow selective call inspection
 * [today](https://github.com/microsoft/TypeScript/pull/64447#issuecomment-5836919279) **andrewbranch** explained semver constraints on adding new keys before a major version bump and asked for clarification on inspecting specific calls
 * [today](https://github.com/microsoft/TypeScript/pull/64447#issuecomment-5837028973) **DanielRosenwasser** said "Is there a reason why you delegate to a symbol instead of providing the "native" function? Is it because that'd involve an extra back-and-forth in sending the same arguments to the API server?"
 * [today](https://github.com/microsoft/TypeScript/pull/64447#issuecomment-5837049212) **andrewbranch** said "Yes, exactly. The idea is if you can name a well-known server implementation, you can save a lot of round trips."

### [Issue microsoft/TypeScript#64448](https://github.com/microsoft/TypeScript/issues/64448) (Closed, `Needs Investigation`, **johnfav03**)

**\`tsc \-\-watch\` 7\.x does not detect edits to files under a symlinked directory inside the project \(6\.0\.3 did\)**

*In TypeScript 7.x, tsc --watch no longer detects edits in symlinked project directories as it did in version 6.0.3.*

 * created by **joac**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.1.1 RC`, and assigned to **johnfav03**
 * [today](https://github.com/microsoft/TypeScript/issues/64448#issuecomment-5838101834) **jakebailey** asked if this was a duplicate of #64351 and #64404 and expressed confusion about the filing process
 * [today](https://github.com/microsoft/TypeScript/issues/64448#issuecomment-5840697858) **joac** clarified the issue concerned only undetected edits on symlinked directories and apologized for the premature PR submission
 * [today](https://github.com/microsoft/TypeScript/issues/64448#issuecomment-5840747807) **jakebailey** said "I checked your case on my mac, and my PR does fix it."
 * [today](https://github.com/microsoft/TypeScript/issues/64448#issuecomment-5840796889) **joac** said "I just tested and you are right, sorry for the noise."
 * (today) **joac** closed the issue

### [PR microsoft/TypeScript#64449](https://github.com/microsoft/TypeScript/pull/64449) (Closed, `For Milestone Bug`, **johnfav03**)

**Watch the physical directory of files reached through a symlinked directory**

*Allow TypeScript watchers to detect changes in symlinked directories by monitoring their real paths and mapping events to logical paths.*

 * created by **joac**
 * (today) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64449#issuecomment-5837872807) **joac** said "@microsoft-github-policy-service agree"
 * (today) **typescript-automation[bot]** added label `For Milestone Bug`, removed label `For Uncommitted Bug`, and assigned to **johnfav03**
 * [today](https://github.com/microsoft/TypeScript/pull/64449#issuecomment-5840801683) **joac** said "This was already fixed on https://github.com/microsoft/TypeScript/pull/64404"
 * (today) **joac** closed the issue

### [Issue microsoft/TypeScript#64450](https://github.com/microsoft/TypeScript/issues/64450) (Open)

**createWatchProgram\(\)\.close\(\) does not cancel the pending program update timer**

*close() does not cancel the pending program update timer in createWatchProgram, causing updates to run after closure and preventing process exit.*

 * created by **sdjayna**

### [PR microsoft/TypeScript#64451](https://github.com/microsoft/TypeScript/pull/64451) (Open, `For Uncommitted Bug`)

**ES\-conformant symbol typing**

*Add ES-standard symbol typing support in TypeScript by introducing a RegisteredSymbol intrinsic, deferred registry keys, and preserved unique symbol types.*

 * created by **michaelfig**
 * [today](https://github.com/microsoft/TypeScript/pull/64451#issuecomment-5838892634) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64451#issuecomment-5839205369) **typescript-automation[bot]** said "The TypeScript team hasn't accepted the linked issue #27524. If you can get it accepted, this PR will have a better chance of being reviewed."

### [PR microsoft/TypeScript#64452](https://github.com/microsoft/TypeScript/pull/64452) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Match Strada's global diagnostic collection, hide non\-diag global errors in editor**

*Adopt Strada's global diagnostic tracking for file checks and hide non-diagnostic global errors in the editor.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/64452#issuecomment-5840569784) **jakebailey** said "I have the cleanup prepared; sorry, didn't intend for you to look at it quite yet."
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#64453](https://github.com/microsoft/TypeScript/issues/64453) (Open)

**\`EFNoLeadingComments\` suppresses synthesized leading comments in tsgo; Strada only suppresses source comments**

*In tsgo, the EFNoLeadingComments emit flag also suppresses synthesized leading comments, unlike TypeScript’s NoLeadingComments which only suppresses source comments.*

 * created by **trevorade**

### [PR microsoft/TypeScript#64454](https://github.com/microsoft/TypeScript/pull/64454) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Replace vscode l10n\-dev with local localization generator**

*Replace @vscode/l10n-dev with lighter in-repo tooling for string extraction and pseudo-localization, removing 85 dependencies and an npm warning*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#64455](https://github.com/microsoft/TypeScript/pull/64455) (Closed, `For Uncommitted Bug`, **andrewbranch**)

**Add getJSDocCommentsAndTags back with functionality of 6\.0**

*Reintroduce getJSDocCommentsAndTags with its full TypeScript 6.0 functionality.*

 * created by **dragomirtitian**
 * (today) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64455#issuecomment-5840244978) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * **typescript-automation[bot]** assigned to **andrewbranch**

### [Issue microsoft/TypeScript#64456](https://github.com/microsoft/TypeScript/issues/64456) (Open)

**\[ServerErrors\]\[JavaScript\] main vs **

*The main branch JavaScript ServerErrors pipeline run processed 196 of 300 popular TypeScript repositories, encountering clone failures, timeouts, and detecting seven interesting changes.*

 * created by **typescript-automation[bot]**
 * [today](https://github.com/microsoft/TypeScript/issues/64456#issuecomment-5840616053) **typescript-automation[bot]** reported a panic in the language server during a textDocument/diagnostic request with stack trace affecting mozilla/pdf.js
 * [today](https://github.com/microsoft/TypeScript/issues/64456#issuecomment-5840616489) **typescript-automation[bot]** reported a server connection closed prematurely error for apache/pouchdb with raw error text, replay commands, request logs, and repro steps
 * [today](https://github.com/microsoft/TypeScript/issues/64456#issuecomment-5840616939) **typescript-automation[bot]** reported server connection closed prematurely and provided repro steps for rollup/rollup
 * [today](https://github.com/microsoft/TypeScript/issues/64456#issuecomment-5840617420) **typescript-automation[bot]** reported that the server connection closed prematurely with an undefined error for the Z-Siqi/Clash-for-Windows_Chinese repository
 * [today](https://github.com/microsoft/TypeScript/issues/64456#issuecomment-5840617867) **typescript-automation[bot]** reported server connection closed prematurely error for parcel-bundler/parcel and included last requests and repro steps
 * [today](https://github.com/microsoft/TypeScript/issues/64456#issuecomment-5840618336) **typescript-automation[bot]** logged a panic when handling textDocument/diagnostic request, including a stack trace and affected repository details
 * [today](https://github.com/microsoft/TypeScript/issues/64456#issuecomment-5840618913) **typescript-automation[bot]** reported a panic handling request for textDocument/diagnostic with a stack trace and build artifact details

### [PR microsoft/TypeScript#64457](https://github.com/microsoft/TypeScript/pull/64457) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Generate compiler option definitions, create JSON schema**

*Generate compiler option metadata to code-generate Go and TypeScript bindings and include a JSON schema in the package*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [Issue microsoft/TypeScript#64458](https://github.com/microsoft/TypeScript/issues/64458) (Open)

**\[ServerErrors\]\[TypeScript\] main vs **

*The TypeScript error-delta Azure pipeline on main encountered server errors, failures, and timeouts across 300 repository analyses.*

 * created by **typescript-automation[bot]**
 * [today](https://github.com/microsoft/TypeScript/issues/64458#issuecomment-5841264031) **typescript-automation[bot]** reported an unhandled node kind panic with stack trace
 * [today](https://github.com/microsoft/TypeScript/issues/64458#issuecomment-5841264366) **typescript-automation[bot]** reported a panic in handling a textDocument/diagnostic request with a stack trace and linked artifacts
 * [today](https://github.com/microsoft/TypeScript/issues/64458#issuecomment-5841264706) **typescript-automation[bot]** reported a panic handling a textDocument/diagnostic request with a stack trace
 * [today](https://github.com/microsoft/TypeScript/issues/64458#issuecomment-5841265072) **typescript-automation[bot]** reported a panic with an unhandled case in Node.Text during a textDocument/diagnostic request along with a stack trace
 * [today](https://github.com/microsoft/TypeScript/issues/64458#issuecomment-5841265407) **typescript-automation[bot]** reported a panic due to interface conversion error with stack trace
 * [today](https://github.com/microsoft/TypeScript/issues/64458#issuecomment-5841265724) **typescript-automation[bot]** reported a runtime panic due to index out of range in the TypeScript-Go checker
 * [today](https://github.com/microsoft/TypeScript/issues/64458#issuecomment-5841266065) **typescript-automation[bot]** reported panic due to unhandled node kind KindBinaryExpression in JSX initializer with accompanying stack trace
 * [today](https://github.com/microsoft/TypeScript/issues/64458#issuecomment-5841266398) **typescript-automation[bot]** reported a debug failure panic and stack trace
 * [today](https://github.com/microsoft/TypeScript/issues/64458#issuecomment-5841266768) **typescript-automation[bot]** reported a panic handling request for textDocument/diagnostic with a stack trace affecting sequelize/sequelize
 * [today](https://github.com/microsoft/TypeScript/issues/64458#issuecomment-5841267073) **typescript-automation[bot]** reported a panic with an interface conversion error and accompanying stack trace
 * [today](https://github.com/microsoft/TypeScript/issues/64458#issuecomment-5841267416) **typescript-automation[bot]** reported panic handling request textDocument/diagnostic with a stack trace and affected repositories
 * [today](https://github.com/microsoft/TypeScript/issues/64458#issuecomment-5841267766) **typescript-automation[bot]** reported a panic in handling textDocument/diagnostic with stack trace and affected repos
 * [today](https://github.com/microsoft/TypeScript/issues/64458#issuecomment-5841268082) **typescript-automation[bot]** reported a panic due to an unhandled node kind in JSX initializer with stack trace
 * [today](https://github.com/microsoft/TypeScript/issues/64458#issuecomment-5841268409) **typescript-automation[bot]** reported panic handling request textDocument/diagnostic with stack trace and artifact links for transloadit/uppy
 * [today](https://github.com/microsoft/TypeScript/issues/64458#issuecomment-5841268718) **typescript-automation[bot]** reported a premature server connection closure with undefined error and provided affected repo, logs, and repro steps
 * [today](https://github.com/microsoft/TypeScript/issues/64458#issuecomment-5841268998) **typescript-automation[bot]** reported a server connection closed prematurely error affecting the iOfficeAI/AionUi repository
 * [today](https://github.com/microsoft/TypeScript/issues/64458#issuecomment-5841269376) **typescript-automation[bot]** reported that the server connection closed prematurely and provided error details, affected repo information, request logs, and reproduction steps
 * [today](https://github.com/microsoft/TypeScript/issues/64458#issuecomment-5841269708) **typescript-automation[bot]** reported server connection closed prematurely with undefined error and provided affected repo details, error artifacts, last requests, and repro steps
 * [today](https://github.com/microsoft/TypeScript/issues/64458#issuecomment-5841270070) **typescript-automation[bot]** reported a 'Server connection closed prematurely: undefined' error for openclaw/openclaw
 * [today](https://github.com/microsoft/TypeScript/issues/64458#issuecomment-5841270413) **typescript-automation[bot]** reported a panic in JSX transformer due to unhandled node kind KindBinaryExpression and included a stack trace

### [Issue microsoft/TypeScript#64459](https://github.com/microsoft/TypeScript/issues/64459) (Open)

**Publish \`fswatch\` Go package**

*Publish fswatch as a standalone Go package by dropping its internal flag and adding a go.mod for filesystem event monitoring.*

 * created by **emersion**

### [PR microsoft/TypeScript#64460](https://github.com/microsoft/TypeScript/pull/64460) (Open, `For Backlog Bug`)

**Fix declaration maps for export assignment expressions**

*Assign original source-map ranges to synthesized export default and export= statements in declaration maps to restore missing mappings.*

 * created by **maricastroc**
 * (today) **typescript-automation[bot]** added labels `For Backlog Bug`, `For Backlog Bug`

### [PR microsoft/TypeScript#64461](https://github.com/microsoft/TypeScript/pull/64461) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Report cyclic structures and truncation during declaration emit**

*Enhance declaration emit to detect and report cyclic type structures and truncation instead of silently returning elided anys*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/64461#issuecomment-5842504613) **jakebailey** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/64461#issuecomment-5842505397) **typescript-automation[bot]** reported build statuses for test top400, user test this, run dt, and perf test this faster jobs
 * [today](https://github.com/microsoft/TypeScript/pull/64461#issuecomment-5842673907) **typescript-automation[bot]** posted performance run results for baseline and PR metrics
 * [today](https://github.com/microsoft/TypeScript/pull/64461#issuecomment-5842706490) **typescript-automation[bot]** reported test results comparing main and the pull request merge, noted infrastructure failures but indicated everything else looked good
 * [today](https://github.com/microsoft/TypeScript/pull/64461#issuecomment-5842766246) **typescript-automation[bot]** reported DT test run failure and pointed to the log
 * [today](https://github.com/microsoft/TypeScript/pull/64461#issuecomment-5842957733) **typescript-automation[bot]** reported build comparison results for top 400 repos between main and the pull request and highlighted failures for review

### [Issue microsoft/TypeScript#64462](https://github.com/microsoft/TypeScript/issues/64462) (Closed)

**Codex\.lunix{program\.null\.dull}**

*The .vscode/extensions.json file contains a malformed recommendation 'Codex.lunix{program.null.dull}' at line 4.*

 * created by **anno24075-bit**

### [Issue microsoft/TypeScript#64463](https://github.com/microsoft/TypeScript/issues/64463) (Open)

**\[LSP\] Memory of configured projects is never released, even after didClose of all files — ~70 MB retained per project \(7\.0\.2 and 7\.1\.0\-dev\.20260926\.1\)**

*TypeScript LSP never frees memory for closed projects, retaining about 70MB per project and causing memory bloat.*

 * created by **talkstream**

### [Issue microsoft/TypeScript#64464](https://github.com/microsoft/TypeScript/issues/64464) (Open, `Needs Investigation`, **johnfav03**)

**First incremental rebuild after a clean build is up to 75× slower than a full check**

*First incremental rebuild after a clean build can be up to 75× slower than a full type check in TypeScript*

 * created by **resure**

### [Issue microsoft/TypeScript#64465](https://github.com/microsoft/TypeScript/issues/64465) (Open)

**Language server retains the pre\-edit program and its checkers for the rest of the session after the first edit**

*The Go-based TypeScript language server leaks memory by retaining pre-edit Program and checker pools via closure-captured options after edits.*

 * created by **ghost2023**

### [PR microsoft/TypeScript#64466](https://github.com/microsoft/TypeScript/pull/64466) (Open, `For Uncommitted Bug`)

**Fix language server retaining pre\-edit program and its checkers after program clone**

*Prevent TypeScript language server cloned programs from retaining previous program checker pools to reduce memory leaks.*

 * created by **ghost2023**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/64466#issuecomment-5846290311) **ghost2023** said "@microsoft-github-policy-service agree"

### [Issue microsoft/TypeScript#64467](https://github.com/microsoft/TypeScript/issues/64467) (Open)

**getTypeAtLocation crashes on the ImportClause of a type\-only import**

*getTypeAtLocation crashes on type-only ImportClause due to missing symbol causing nil pointer or undefined property errors.*

 * created by **lsh4711**

### [PR microsoft/TypeScript#64468](https://github.com/microsoft/TypeScript/pull/64468) (Open, `For Uncommitted Bug`)

**Prevent getTypeAtLocation crash on type\-only import clause**

*TypeScript's getTypeAtLocation crashes on type-only import clauses without default bindings due to missing symbol guard.*

 * created by **lsh4711**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/64468#issuecomment-5846956201) **lsh4711** said "@microsoft-github-policy-service agree"

### [PR microsoft/TypeScript#64469](https://github.com/microsoft/TypeScript/pull/64469) (Open, `For Uncommitted Bug`)

**Speed up first incremental rebuilds after shared dependency edits**

*Introduce a cached export-lookup index and parallel signature computations to accelerate first incremental rebuilds after shared dependency edits.*

 * created by **resure**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/64469#issuecomment-5847125871) **resure** said "@microsoft-github-policy-service agree"

