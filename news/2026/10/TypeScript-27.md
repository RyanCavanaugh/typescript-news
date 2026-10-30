# Report for 2026-10-27 (Tuesday, October 27th, 2026)

20 different users commented on 100 different issues.

## Recommended Actions

 * Response Recommended
    * @z0rimo asked for a review of the revised approach in [microsoft/TypeScript#64257](https://github.com/microsoft/TypeScript/pull/64257#issuecomment-6458080251)
    * @Shriraj1901 asked if another contributor is working on the issue in [microsoft/TypeScript#64438](https://github.com/microsoft/TypeScript/issues/64438#issuecomment-6468222987)
    * @jltrv provided additional repro variants of the regression in [microsoft/TypeScript#64974](https://github.com/microsoft/TypeScript/issues/64974#issuecomment-6447340132)

## Activity Summary

### [Issue microsoft/TypeScript#35909](https://github.com/microsoft/TypeScript/issues/35909) (Open, `Suggestion`, `Awaiting More Feedback`)

**Can't evaluate equality of symbols made by Symbol\.for**

*TypeScript treats Symbol.for calls as distinct types, causing erroneous type errors on equality comparisons and assignments.*

 * [20 weeks ago](https://github.com/microsoft/TypeScript/issues/35909#issuecomment-4626919034) **lygstate** said "It's a bug, can it fixed? As Symbol.for("literal") basically act like "literal" with symbol attribute"
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/35909#issuecomment-6277055373) **michaelfig** encouraged people following the issue to review PR #64451 and provide feedback
 * [today](https://github.com/microsoft/TypeScript/issues/35909#issuecomment-6438798683) **Richiban** proposed adding a literal symbol type in TypeScript for matching specific sentinels
 * [later](https://github.com/microsoft/TypeScript/issues/35909#issuecomment-6471498698) **cowboyd** concurred

### [PR microsoft/TypeScript#63895](https://github.com/microsoft/TypeScript/pull/63895) (Open, `Domain: Performance`, `For Uncommitted Bug`)

**Reduce allocations on hot path\-normalization and overlay\-update paths**

*Optimize hot normalization and overlay-update code paths to reduce allocation churn and improve GC scan density.*

 * created by **no-yan**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [9 weeks ago](https://github.com/microsoft/TypeScript/pull/63895#issuecomment-5352580868) **no-yan** said "@microsoft-github-policy-service agree"
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#63896](https://github.com/microsoft/TypeScript/pull/63896) (Open, `Domain: Performance`, `For Uncommitted Bug`)

**Add fast paths to CombinePaths and defer path canonicalization in checkSourceFilesBelongToPath**

*Optimize CombinePaths to return absolute paths directly and postpone canonicalization in checkSourceFilesBelongToPath, reducing allocations and improving performance.*

 * created by **no-yan**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [9 weeks ago](https://github.com/microsoft/TypeScript/pull/63896#issuecomment-5352656263) **no-yan** said "@microsoft-github-policy-service agree"
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#63897](https://github.com/microsoft/TypeScript/pull/63897) (Open, `Domain: Performance`, `For Uncommitted Bug`)

**Cache repeated computations in program construction hot paths**

*Add caching for file path normalization and resolver conditions to reduce allocation churn on program construction hot paths.*

 * created by **no-yan**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#63898](https://github.com/microsoft/TypeScript/pull/63898) (Open, `Domain: Performance`, `For Uncommitted Bug`)

**Avoid wrapping the queued function in an extra closure in parallelWorkGroup**

*Remove redundant closure wrapping in parallelWorkGroup.Queue to reduce per-task allocations by passing functions directly to sync.WaitGroup.Go.*

 * created by **no-yan**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#63900](https://github.com/microsoft/TypeScript/pull/63900) (Open, `Domain: Performance`, `For Uncommitted Bug`)

**Use trie for removeStringLiteralsMatchedByTemplateLiterals**

*Use a prefix trie to optimize removeStringLiteralsMatchedByTemplateLiterals template literal matching and improve performance.*

 * created by **eps1lon**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64014](https://github.com/microsoft/TypeScript/pull/64014) (Closed, `Author: Team`, `For Backlog Bug`, **RyanCavanaugh**)

**Matching Strada order of operations in recursive signature resolution**

*Ensure the Go checker returns the cached source-order signature during recursive generic call resolution to prevent incorrect type inference.*

 * (8 weeks ago) **typescript-automation[bot]** added labels `Author: Team`, `For Backlog Bug`, and assigned to **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript/pull/64014#issuecomment-6452770018) **RyanCavanaugh** said "Closing in favor of other fix(es)"
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#64044](https://github.com/microsoft/TypeScript/pull/64044) (Open, `Domain: Performance`, `Author: Team`, `For Milestone Bug`, **jakebailey**)

**Speed up narrowing of literal unions**

*Optimizes narrowing of literal unions, cutting user CPU time from around 11 seconds to under 0.1 second.*

 * (8 weeks ago) **typescript-automation[bot]** added labels `Author: Team`, `For Milestone Bug`, and assigned to **jakebailey**
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64138](https://github.com/microsoft/TypeScript/pull/64138) (Open, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **RyanCavanaugh**, **Copilot**)

**Speed up source map emit for large single\-line object literals**

*Optimize source map emission by caching UTF-16 column calculations to avoid quadratic scanning for large single-line object literals.*

 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [7 weeks ago](https://github.com/microsoft/TypeScript/pull/64138#issuecomment-5517346468) **jakebailey** said "Interesting, I think we have this same optimization somewhere else? I had thought for this specifically, actually."
 * [7 weeks ago](https://github.com/microsoft/TypeScript/pull/64138#issuecomment-5554242611) **DanielRosenwasser** listed related issues and pull requests
 * **jakebailey** added label `Domain: Performance`
 * **typescript-automation[bot]** added label `Author: Team`

### [PR microsoft/TypeScript#64188](https://github.com/microsoft/TypeScript/pull/64188) (Open, `Domain: Performance`, `For Uncommitted Bug`)

**Skip object classification for shared type facts**

*Skip object classification checks for shared type facts to reduce redundant isEmptyObjectType and isFunctionObjectType calls.*

 * [7 weeks ago](https://github.com/microsoft/TypeScript/pull/64188#issuecomment-5589784192) **typescript-automation[bot]** reported the performance run results in a detailed comparison report
 * [7 weeks ago](https://github.com/microsoft/TypeScript/pull/64188#issuecomment-5589784504) **typescript-automation[bot]** reported user test results, noted infrastructure failures unrelated to the change, and confirmed everything else looked good
 * [7 weeks ago](https://github.com/microsoft/TypeScript/pull/64188#issuecomment-5590335811) **typescript-automation[bot]** reported that running the top 400 repos with tsc comparing main and refs/pull/64188/merge looked good
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64257](https://github.com/microsoft/TypeScript/pull/64257) (Open, `For Backlog Bug`)

**Fix non\-null discriminant narrowing consistency**

*Ensure discriminant narrowing preserves nullable constituents consistently in both small and large unions.*

 * [6 weeks ago](https://github.com/microsoft/TypeScript/pull/64257#issuecomment-5657958944) **z0rimo** agreed with microsoft-github-policy-service
 * [6 weeks ago](https://github.com/microsoft/TypeScript/pull/64257#issuecomment-5662956364) **z0rimo** addressed both #62511 and #64260 by reworking mutation analysis around invocation sites and adding tests for union-size inconsistency and stale-fact cases
 * [1 month ago](https://github.com/microsoft/TypeScript/pull/64257#issuecomment-5883585069) **z0rimo** reworked the fix based on feedback and asked for another review
 * [today](https://github.com/microsoft/TypeScript/pull/64257#issuecomment-6458080251) **z0rimo** requested another review after revising the implementation to use the general discriminant narrowing path and documenting benchmark results

### [PR microsoft/TypeScript#64266](https://github.com/microsoft/TypeScript/pull/64266) (Open, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Improve performance of batched requests**

*Automatically batch requests across all API endpoints with code generation, remove hardcoded entrypoints, switch to struct-of-arrays layout for better performance.*

 * (6 weeks ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`
 * [6 weeks ago](https://github.com/microsoft/TypeScript/pull/64266#issuecomment-5687798292) **weswigham** explained that they updated the server to support efficient batch requests with shared parameters for all protocol methods, avoiding maintaining separate singular and bulk wire protocol implementations
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64317](https://github.com/microsoft/TypeScript/pull/64317) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Cherry\-pick tsgo PR 4535 into release\-7\.0**

*Cherry-pick TypeScript-Go PR 4535 into the release-7.0 branch.*

 * (5 weeks ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64318](https://github.com/microsoft/TypeScript/pull/64318) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Cherry\-pick tsgo PR 4658 into release\-7\.0**

*Cherry-pick PR 4658 from tsgo into the release-7.0 branch to resolve issue 64262.*

 * (5 weeks ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64321](https://github.com/microsoft/TypeScript/pull/64321) (Open, `Domain: Performance`, `For Uncommitted Bug`)

**perf: preallocate inherited member symbol table**

*Preallocate the inherited member symbol table using its known size to avoid unnecessary reallocations.*

 * [5 weeks ago](https://github.com/microsoft/TypeScript/pull/64321#issuecomment-5724566154) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [5 weeks ago](https://github.com/microsoft/TypeScript/pull/64321#issuecomment-5725605595) **jakebailey** asked how many hints are too large and whether Go map default sizing matters
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64327](https://github.com/microsoft/TypeScript/pull/64327) (Open, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Preserve inferred project ATA state**

*Preserve and reapply automatic type acquisition state for inferred projects to prevent error flashing when files reopen.*

 * (5 weeks ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64380](https://github.com/microsoft/TypeScript/pull/64380) (Closed, `Author: Team`, `For Uncommitted Bug`, **RyanCavanaugh**)

**Revise 'restack' instructions in SKILL\.md**

*Revise the SKILL.md restack instructions to prevent them from being applied to unrelated operations.*

 * (5 weeks ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript/pull/64380#issuecomment-6452891955) **RyanCavanaugh** said "Solved this by renaming it entirely"
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#64400](https://github.com/microsoft/TypeScript/pull/64400) (Closed, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Run code generation on build**

*Automatically run code generation during both build and watch processes to eliminate manual regeneration steps.*

 * (5 weeks ago) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [5 weeks ago](https://github.com/microsoft/TypeScript/pull/64400#issuecomment-5788559466) **weswigham** removed integration-style tests from generatedFile.test.mts as they didn’t focus on caching functionality
 * [today](https://github.com/microsoft/TypeScript/pull/64400#issuecomment-6449959678) **jakebailey** observed that running 'hereby build' twice took 28 seconds because generators touched files and invalidated the go build cache, and suggested silencing output and addressing the critical path
 * [today](https://github.com/microsoft/TypeScript/pull/64400#issuecomment-6455175225) **weswigham** granted silence and attached a screenshot
 * (later) **weswigham** closed the issue

### [PR microsoft/TypeScript#64404](https://github.com/microsoft/TypeScript/pull/64404) (Open, `Domain: Performance`, `Author: Team`, `For Milestone Bug`, **jakebailey**)

**Watch alias invalidation**

*Introduce a watchalias lookup to match filesystem paths with compiler-recognized file names so watch mode detects changes through symlinks.*

 * (5 weeks ago) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Milestone Bug`, and removed label `For Uncommitted Bug`
 * **jakebailey** added label `Domain: Performance`

### [Issue microsoft/TypeScript#64438](https://github.com/microsoft/TypeScript/issues/64438) (Open, `Bug`, `Help Wanted`, `Good First Issue`)

**Incorrect/unhelpful error message for non\-module jsx file**

*TypeScript shows misleading missing module errors for JSX in non-module scripts instead of stating scripts cannot import modules.*

 * [1 month ago](https://github.com/microsoft/TypeScript/issues/64438#issuecomment-5826551653) **sh011** said "Hi @calebegg @DanielRosenwasser I went through the issue and found that the diagnostic chain needs to be looked up properly. I would like to work on this issue, can you please assign it to me. Thanks!"
 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/64438#issuecomment-5911162732) **SiddhantShedge45** offered to work on the issue by investigating JSX diagnostic generation, improving the error message, adding a regression test, and verifying existing behavior
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/64438#issuecomment-6260062351) **vivan070707-ctrl** asked if the issue was still available for investigation and offered to implement a fix with a regression test
 * [later](https://github.com/microsoft/TypeScript/issues/64438#issuecomment-6468222987) **Shriraj1901** offered to help reproduce diagnostics, trace compiler checks, and add regression tests, and asked if another contributor is already working on it

### [PR microsoft/TypeScript#64475](https://github.com/microsoft/TypeScript/pull/64475) (Open, `Domain: Performance`, `For Uncommitted Bug`, **ahejlsberg**)

**build member tables of instantiated classes/interfaces lazily**

*Implement lazy construction of class and interface member tables to avoid unneeded instantiations and improve performance and memory usage.*

 * [1 month ago](https://github.com/microsoft/TypeScript/pull/64475#issuecomment-5885611567) **maschwenk** thanked the maintainer for landing the PR and reported code size reductions and performance improvements across various projects, noted non-determinism in the never-reduction check and submitted a fix via PR #64521
 * [3 weeks ago](https://github.com/microsoft/TypeScript/pull/64475#issuecomment-5918854781) **ahejlsberg** thanked @maschwenk for the research, acknowledged potential wins from selective member resolution, and suggested combining the disparate code paths into a single implementation
 * [3 weeks ago](https://github.com/microsoft/TypeScript/pull/64475#issuecomment-5918890839) **maschwenk** said "@ahejlsberg totally understand! thank you! was just making sure it didn't drop off notifications ❤️ "
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64528](https://github.com/microsoft/TypeScript/pull/64528) (Open, `Domain: Performance`, `For Uncommitted Bug`)

**Prevent unbounded combined\-constraint recursion during variance measurement**

*Skipping combined-constraint checks during variance measurement prevents unbounded recursion and memory exhaustion in TypeScript 7.*

 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [1 month ago](https://github.com/microsoft/TypeScript/pull/64528#issuecomment-5892189219) **Amatewasu** verified the fix against a private React 19+R3F+TSX project, reported memory and time benchmarks for unpatched TS7, patched TS7, and TS6, and noted diagnostics parity and caveats
 * [3 weeks ago](https://github.com/microsoft/TypeScript/pull/64528#issuecomment-5992092873) **Amatewasu** said "@microsoft-github-policy-service agree company="BALYO""
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64539](https://github.com/microsoft/TypeScript/pull/64539) (Open, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Fuse local syntax lowerings into one traversal**

*Combining local syntax lowerings into one transformer traversal to boost performance and reduce memory usage pending benchmarks.*

 * [1 month ago](https://github.com/microsoft/TypeScript/pull/64539#issuecomment-5897198748) **typescript-automation[bot]** provided the requested perf run results
 * [1 month ago](https://github.com/microsoft/TypeScript/pull/64539#issuecomment-5897621618) **jakebailey** said "No change???"
 * [3 weeks ago](https://github.com/microsoft/TypeScript/pull/64539#issuecomment-5937115274) **weswigham** described his plan to update transformers.Chain to track the full transform stack during traversal and perform walk-fusion
 * **jakebailey** added label `Domain: Performance`

### [Issue microsoft/TypeScript#64593](https://github.com/microsoft/TypeScript/issues/64593) (Closed, `Needs Investigation`, **gabritto**)

**Reverse\-mapped inference exposes private members as public; since \#63932 this rejects \`f\<T\>\(\) as C\`**

*Since PR #63932, reverse-mapped type inference exposes private members as public, causing errors when casting Readonly<Account & T> to Account.*

 * (3 weeks ago) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.1.1 RC`, and assigned to **gabritto**
 * [today](https://github.com/microsoft/TypeScript/issues/64593#issuecomment-6449003992) **gabritto** provided a simpler repro preceding issue #63932
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript#64594](https://github.com/microsoft/TypeScript/pull/64594) (Closed, `For Milestone Bug`, **gabritto**)

**Skip non\-public members when resolving reverse\-mapped types**

*Skip non-public class members when resolving reverse-mapped types to prevent them from becoming erroneously public.*

 * (3 weeks ago) **typescript-automation[bot]** added label `For Milestone Bug`, removed label `For Uncommitted Bug`, and assigned to **gabritto**
 * [today](https://github.com/microsoft/TypeScript/pull/64594#issuecomment-6449220255) **gabritto** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/64594#issuecomment-6449223659) **typescript-automation[bot]** reported CI build statuses for test top400, user test this, run dt, and perf test this faster
 * [today](https://github.com/microsoft/TypeScript/pull/64594#issuecomment-6449823854) **typescript-automation[bot]** notified that the DT test results were ready and unchanged
 * [today](https://github.com/microsoft/TypeScript/pull/64594#issuecomment-6450365429) **typescript-automation[bot]** reported test results and indicated everything looked good
 * [today](https://github.com/microsoft/TypeScript/pull/64594#issuecomment-6450622248) **typescript-automation[bot]** reported the provisional hosted-runner performance results comparing baseline to PR for tsc
 * [today](https://github.com/microsoft/TypeScript/pull/64594#issuecomment-6451538812) **kirkouimet** said "@gabritto fun to see this process"
 * [today](https://github.com/microsoft/TypeScript/pull/64594#issuecomment-6451652755) **typescript-automation[bot]** reported the results of running the top 400 repos with tsc comparing `baseline` and `pr` and noted that everything looked good
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript#64603](https://github.com/microsoft/TypeScript/pull/64603) (Closed, `Domain: Performance`, `Author: Team`, `For Backlog Bug`, **RyanCavanaugh**)

**Release unused LSP configured projects during idle cleanup**

*Unused LSP-configured projects are released during idle cleanup to free resources.*

 * (3 weeks ago) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Backlog Bug`, and removed label `For Uncommitted Bug`
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64644](https://github.com/microsoft/TypeScript/pull/64644) (Closed, `For Uncommitted Bug`)

**Fix crash in formatter on comment lookalikes in JSX closing tags**

*A fix for formatter crashes triggered by JSX closing tags resembling comments.*

 * created by **Andarist**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [3 weeks ago](https://github.com/microsoft/TypeScript/pull/64644#issuecomment-5998060040) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript#64654](https://github.com/microsoft/TypeScript/pull/64654) (Open, `Domain: Performance`, `For Uncommitted Bug`, **ahejlsberg**)

**check the target of a type reference in isWeakType**

*Modify isWeakType to check the target of type references instead of instantiating generic members, reducing memory usage by 19%.*

 * [4 days ago](https://github.com/microsoft/TypeScript/pull/64654#issuecomment-6374940097) **typescript-automation[bot]** posted the requested performance run results including detailed comparison metrics between baseline and PR
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/64654#issuecomment-6375132212) **typescript-automation[bot]** provided tsc user test results and indicated everything looked good
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/64654#issuecomment-6375679362) **typescript-automation[bot]** reported successful tsc comparison between baseline and pr on the top 400 repos
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64659](https://github.com/microsoft/TypeScript/pull/64659) (Open, `Domain: Performance`, `For Uncommitted Bug`, **johnfav03**)

**Compute signatures of dependent files in parallel on incremental rebuilds**

*Declaration signatures for files dependent on an edited file are now computed in parallel during incremental rebuilds to significantly reduce build times.*

 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64659#issuecomment-6272927629) **typescript-automation[bot]** provided the results of the performance run with a detailed comparison report
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64659#issuecomment-6273501427) **typescript-automation[bot]** reported that test results comparing baseline and PR looked good
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64659#issuecomment-6274117618) **typescript-automation[bot]** reported that tsc runs on the top 400 repos comparing baseline and pr succeeded
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64684](https://github.com/microsoft/TypeScript/pull/64684) (Open, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **DanielRosenwasser**)

**Use \`link\[T\]\` in place of \`\*Node\` in syntax nodes\.**

*AST node child references now use 32-bit link indices with generated accessor methods instead of 64-bit pointers to reduce memory and CPU overhead under Go’s garbage collector.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/64684#issuecomment-6054635129) **DanielRosenwasser** said "@typescript-bot perf test this"
 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/64684#issuecomment-6054636949) **typescript-automation[bot]** reported that performance test jobs had started and provided status links
 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/64684#issuecomment-6055105743) **typescript-automation[bot]** reported the requested perf run results comparing baseline to PR, showing unchanged errors, symbols, and types, and a 4.39% memory usage improvement
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64695](https://github.com/microsoft/TypeScript/pull/64695) (Open, `Domain: Performance`, `For Milestone Bug`, **ahejlsberg**)

**\[experiment\] Skip incompatible discriminants when inferring**

*Experimentally skip incompatible discriminant properties during TypeScript union type inference to reduce workload and validate via tests.*

 * [3 days ago](https://github.com/microsoft/TypeScript/pull/64695#issuecomment-6384190137) **jakebailey** said "@typescript-bot perf test this faster"
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/64695#issuecomment-6384191000) **typescript-automation[bot]** reported starting of performance test jobs and provided links to status and results
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/64695#issuecomment-6384500825) **typescript-automation[bot]** posted the requested performance run results comparing baseline to PR metrics
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64698](https://github.com/microsoft/TypeScript/pull/64698) (Open, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**AST nodes as handles, offsets into areanas**

*Add support for representing AST nodes as compact handles by using offsets into arenas*

 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/64698#issuecomment-6069775426) **jakebailey** said "@typescript-bot perf test this"
 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/64698#issuecomment-6069776858) **typescript-automation[bot]** noted that performance tests started and that the comment would be updated as builds progressed
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64699](https://github.com/microsoft/TypeScript/pull/64699) (Open, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Intern symbol names as pointer\-free IDs**

*Symbol names are now represented as pointer-free 64-bit interned IDs to improve memory efficiency and reduce GC overhead.*

 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64699#issuecomment-6200413139) **jakebailey** said "@typescript-bot perf test this faster"
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64699#issuecomment-6200415223) **typescript-automation[bot]** reported that the performance test started and provided links for build status and results
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64699#issuecomment-6201018025) **typescript-automation[bot]** posted the results of the requested performance run including comparison metrics
 * [today](https://github.com/microsoft/TypeScript/pull/64699#issuecomment-6450707500) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/64699#issuecomment-6450710095) **typescript-automation[bot]** reported that the performance test job had started and provided links to the build and results
 * [today](https://github.com/microsoft/TypeScript/pull/64699#issuecomment-6451440930) **typescript-automation[bot]** reported the performance results for the requested perf run, presenting provisional hosted-runner metrics for tsc including errors, symbols, types, and memory usage comparisons
 * **jakebailey** added label `Domain: Performance`
 * [today](https://github.com/microsoft/TypeScript/pull/64699#issuecomment-6452896833) **jakebailey** said "Hmm, will have to see if that perf slowdown is still real (I thought it was fixed) and if it can be improved."
 * [later](https://github.com/microsoft/TypeScript/pull/64699#issuecomment-6471257938) **jakebailey** requested that the TypeScript bot run performance tests faster before another refactor
 * [later](https://github.com/microsoft/TypeScript/pull/64699#issuecomment-6471260423) **typescript-automation[bot]** started jobs and posted a status table linking to the build and results
 * [later](https://github.com/microsoft/TypeScript/pull/64699#issuecomment-6472224109) **typescript-automation[bot]** provided the requested performance run results

### [PR microsoft/TypeScript#64703](https://github.com/microsoft/TypeScript/pull/64703) (Open, `For Backlog Bug`)

**Preserve computed property names in isolated declaration emit**

*Preserve computed identifier and dotted property names in declaration files under --isolatedDeclarations without inferring index signatures and with existing diagnostics.*

 * created by **Trighap52**
 * (2 weeks ago) **typescript-automation[bot]** added labels `For Backlog Bug`, `For Backlog Bug`
 * **weswigham** added to milestone `TypeScript 7.2.0 Beta`

### [PR microsoft/TypeScript#64722](https://github.com/microsoft/TypeScript/pull/64722) (Open, `Domain: Performance`, `For Backlog Bug`)

**Merge export \* tables without per\-name collision trackers**

*Improve performance of export * by merging tables directly, pre-sizing them, and only tracking collisions when needed.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/64722#issuecomment-6100021037) **gwkline** said "@microsoft-github-policy-service agree"
 * (6 days ago) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64729](https://github.com/microsoft/TypeScript/pull/64729) (Open, `Domain: Performance`, `For Milestone Bug`, **gabritto**)

**Dedupe identical object literal types before subtype reduction**

*Deduplicate identical object literal types before subtype reduction to prevent O(n²) performance blow-ups when type-checking large JSON arrays*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/64729#issuecomment-6134415656) **typescript-automation[bot]** reported that running the top 400 repos tsc comparison between baseline and pr succeeded without issues
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/64729#issuecomment-6363202221) **gadcam** said "@jakebailey The Oct 12 test run came back clean (perf neutral, DT / user tests / top400 unchanged). What do you think about this PR?"
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64729#issuecomment-6420325668) **gadcam** thanked gabritto for kicking off CI, explained failures from the recent merge, merged main and switched to accessors, confirmed tests passed, and asked for CI reapproval
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64737](https://github.com/microsoft/TypeScript/pull/64737) (Open, `Domain: Performance`, `For Backlog Bug`)

**Avoid exponential base type search in hasBaseType**

*Change hasBaseType to avoid exponential exploration of shared interface base types, reducing type-checking time on deep inheritance chains.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/64737#issuecomment-6118738793) **DanielRosenwasser** said "@typescript-bot perf test this"
 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/64737#issuecomment-6118739780) **typescript-automation[bot]** announced that performance test build jobs started and provided links to status and results
 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/64737#issuecomment-6119059459) **typescript-automation[bot]** provided the requested performance run results in a detailed comparison table
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64756](https://github.com/microsoft/TypeScript/pull/64756) (Open, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **DanielRosenwasser**)

**Try using a map for resolved write\-side types\.**

*Use a map data structure to manage resolved write-side types more efficiently.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/64756#issuecomment-6134730254) **DanielRosenwasser** said "@typescript-bot perf test this"
 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/64756#issuecomment-6134731268) **typescript-automation[bot]** indicated that performance test jobs started and provided links to build status and results
 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/64756#issuecomment-6135074438) **typescript-automation[bot]** posted the requested perf run results with a comparison report including metrics for errors, symbols, types, memory usage, and allocations
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64767](https://github.com/microsoft/TypeScript/pull/64767) (Open, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Replace most ID usage with pointers**

*Replace ID references with direct pointers to eliminate atomic ID loads, enhance locality, and reduce overhead.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/64767#issuecomment-6143646033) **jakebailey** said "@typescript-bot perf test this faster"
 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/64767#issuecomment-6143647694) **typescript-automation[bot]** announced that performance test jobs had started and provided status and results links
 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/64767#issuecomment-6144129514) **typescript-automation[bot]** posted the requested performance run results
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64775](https://github.com/microsoft/TypeScript/pull/64775) (Open, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Compress paged link\-store references**

*Convert pointer-sized page entries in dense checker link stores to four-byte arena indexes, halving storage and eliminating pointers.*

 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64775#issuecomment-6174011605) **typescript-automation[bot]** reported that performance tests started and provided status and results links
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64775#issuecomment-6174935260) **typescript-automation[bot]** provided perf run results as requested
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64775#issuecomment-6175006477) **jakebailey** said "This one's a bit pitiful. Basically the strategy is to make stores hold indexes into a dense array instead of always placing in sparse. But it's more complicated."
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64781](https://github.com/microsoft/TypeScript/pull/64781) (Open, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Index structured type members without redundant symbol maps**

*Remove redundant name-to-symbol maps for resolved object types by using property lists and indexed slots, reducing memory usage.*

 * [3 days ago](https://github.com/microsoft/TypeScript/pull/64781#issuecomment-6391335368) **jakebailey** said "@typescript-bot perf test"
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/64781#issuecomment-6391336124) **typescript-automation[bot]** started perf test jobs and provided status and result links
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/64781#issuecomment-6391649443) **typescript-automation[bot]** provided the performance run results
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64788](https://github.com/microsoft/TypeScript/pull/64788) (Open, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Store ordinary relationship keys as exact type ID pairs**

*Store ordinary comparison keys as 64-bit type ID pairs instead of 128-bit hashes, improving memory usage.*

 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64788#issuecomment-6174010677) **jakebailey** said "@typescript-bot perf test this faster"
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64788#issuecomment-6174013513) **typescript-automation[bot]** provided an update that the performance test had started with links to build and results
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64788#issuecomment-6174651792) **typescript-automation[bot]** posted requested performance run results
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64789](https://github.com/microsoft/TypeScript/pull/64789) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Share complete union and intersection property cache entries**

*Share complete property cache entries between augmented and non-augmented lookups to reduce duplicate entries, memory usage, and GC scanning overhead.*

 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64789#issuecomment-6174011075) **jakebailey** said "@typescript-bot perf test this faster"
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64789#issuecomment-6174014470) **typescript-automation[bot]** reported build jobs started and provided status and results links
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64789#issuecomment-6174849745) **typescript-automation[bot]** provided the requested performance run results
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64808](https://github.com/microsoft/TypeScript/pull/64808) (Open, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **DanielRosenwasser**)

**Share a single cache for all type relationships and propagate results hierarchically**

*Proposes consolidating separate type relationship caches into a unified hierarchical cache to reduce redundancy and overlap in cached results.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/64808#issuecomment-6162005757) **DanielRosenwasser** said "@typescript-bot perf test this"
 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/64808#issuecomment-6162006945) **typescript-automation[bot]** reported that perf test jobs had started and included status and results links
 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/64808#issuecomment-6162361810) **typescript-automation[bot]** reported the results of the requested performance run including compiler metrics such as errors, symbols, types, and memory usage
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64815](https://github.com/microsoft/TypeScript/pull/64815) (Open, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Avoid short\-lived allocations in union and intersection property handling**

*Optimize union and intersection property enumeration by eliminating short-lived allocations, reducing memory usage and improving performance.*

 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64815#issuecomment-6174011628) **jakebailey** said "@typescript-bot perf test this faster"
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64815#issuecomment-6174015419) **typescript-automation[bot]** indicated the start of performance test jobs and provided links to the build status and results
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64815#issuecomment-6174755572) **typescript-automation[bot]** posted the requested perf run results for tsc comparing baseline and PR
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64819](https://github.com/microsoft/TypeScript/pull/64819) (Open, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **DanielRosenwasser**, **Copilot**)

**Recycle type checkers under a configurable memory budget**

*Introduce an opt-in maxMemory option to recycle type checkers and cap memory usage during non-incremental type checking*

 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64819#issuecomment-6179426965) **DanielRosenwasser** said "@typescript-bot perf test this"
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64819#issuecomment-6179428536) **typescript-automation[bot]** said "Hey @DanielRosenwasser, this PR was updated less than two minutes before this command. Please wait until it has been unchanged for two minutes and try again."
 * **jakebailey** added label `Domain: Performance`
 * **typescript-automation[bot]** added label `Author: Team`

### [PR microsoft/TypeScript#64826](https://github.com/microsoft/TypeScript/pull/64826) (Closed, `Author: Team`, `For Uncommitted Bug`)

**Update localization files**

*Update localization files and regenerate corresponding runtime artifacts.*

 * created by **typescript-automation[bot]**
 * (1 week ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64847](https://github.com/microsoft/TypeScript/pull/64847) (Open, `Domain: Performance`, `For Uncommitted Bug`)

**Check referenced project sources before probing their declaration outputs**

*Prioritize referenced project source files before checking built declaration outputs to eliminate redundant filesystem lookups.*

 * created by **guru-irl**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64847#issuecomment-6223607821) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64856](https://github.com/microsoft/TypeScript/pull/64856) (Closed, `For Uncommitted Bug`)

**Report implicit any errors in function type binding patterns during checking**

*Enable TypeScript to detect and report implicit any types in function binding patterns during type checking.*

 * created by **Andarist**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64856#issuecomment-6248514169) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript#64868](https://github.com/microsoft/TypeScript/pull/64868) (Open, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Compare names before symbols when matching flow references**

*Compare declaration and reference names before symbol lookup to reduce analysis overhead and improve performance.*

 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64868#issuecomment-6272836805) **jakebailey** said "@typescript-bot perf test this faster"
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64868#issuecomment-6272839100) **typescript-automation[bot]** started performance tests and posted links to build status and results
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64868#issuecomment-6273381312) **typescript-automation[bot]** provided the requested performance run results
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64869](https://github.com/microsoft/TypeScript/pull/64869) (Open, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Store merged symbols in a paged symbol link store**

*Use a paged symbol link store indexed by dense symbol IDs to avoid getMergedSymbol map misses and improve performance.*

 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64869#issuecomment-6273344912) **jakebailey** said "@typescript-bot perf test this faster"
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64869#issuecomment-6273347159) **typescript-automation[bot]** started build jobs and posted status and results links
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64869#issuecomment-6274004601) **typescript-automation[bot]** posted the requested performance run results including a comparison report of tsc metrics such as errors, symbols, types, memory used, and memory allocations
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64870](https://github.com/microsoft/TypeScript/pull/64870) (Open, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Checker affinity tweaks**

*Tweak checker affinity settings to optimize resource allocation and improve performance*

 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64870#issuecomment-6297488734) **jakebailey** said "@typescript-bot perf test this faster"
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64870#issuecomment-6297490582) **typescript-automation[bot]** reported that the perf test started and provided links to build status and results
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64870#issuecomment-6298053666) **typescript-automation[bot]** reported the performance run results requested by @jakebailey
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64871](https://github.com/microsoft/TypeScript/pull/64871) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Speed up short\-lived checker caches**

*Optimize short-lived checker caches by replacing costly Go map clears with generation-counter tables and simpler key hashing for speed improvements.*

 * [4 days ago](https://github.com/microsoft/TypeScript/pull/64871#issuecomment-6376262146) **jakebailey** said "@typescript-bot perf test"
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/64871#issuecomment-6376264609) **typescript-automation[bot]** reported starting of perf test job and provided status and results links
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/64871#issuecomment-6379059712) **typescript-automation[bot]** provided performance run results for the requested comparison
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64876](https://github.com/microsoft/TypeScript/pull/64876) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Count intersection property names with a plain map and slice**

*Count intersection property names using a plain map and slice, benchmark performance differences, and note conflict with issue #64815.*

 * [3 days ago](https://github.com/microsoft/TypeScript/pull/64876#issuecomment-6391181434) **jakebailey** said "@typescript-bot perf test"
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/64876#issuecomment-6391182586) **typescript-automation[bot]** announced that the perf test build job started and linked to its status and results
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/64876#issuecomment-6391487648) **typescript-automation[bot]** posted performance run results including a detailed comparison report of compiler metrics between baseline and pr
 * **jakebailey** added label `Domain: Performance`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64877](https://github.com/microsoft/TypeScript/pull/64877) (Open, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**LSP perf optimizations**

*LSP performance optimizations in the TypeScript compiler reduce time, memory, and allocations in VSCode benchmarks by up to 43%.*

 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64877#issuecomment-6277582400) **andrewbranch** said "@typescript-bot perf test"
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64877#issuecomment-6277584246) **typescript-automation[bot]** reported that CI jobs for perf test started and provided links to build results
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64877#issuecomment-6278207578) **typescript-automation[bot]** posted the requested performance run results
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64878](https://github.com/microsoft/TypeScript/pull/64878) (Open, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Skip assignments when narrowing identifiers**

*Skip assignment operations during identifier narrowing to improve filtering accuracy.*

 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64878#issuecomment-6276912429) **jakebailey** said "@typescript-bot perf test this faster"
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64878#issuecomment-6276914193) **typescript-automation[bot]** posted automated build start status for `perf test this faster` command
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64878#issuecomment-6277464418) **typescript-automation[bot]** reported the requested perf run results including a baseline vs PR comparison table
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64880](https://github.com/microsoft/TypeScript/pull/64880) (Open, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Memoize repeated inference walks**

*Implement memoization to cache and reuse results of repeated inference walks for performance improvement.*

 * [3 days ago](https://github.com/microsoft/TypeScript/pull/64880#issuecomment-6391181190) **jakebailey** said "@typescript-bot perf test"
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/64880#issuecomment-6391182173) **typescript-automation[bot]** reported that performance test jobs started and provided status and results links
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/64880#issuecomment-6391679634) **typescript-automation[bot]** provided the requested performance run results in a detailed comparison report
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64888](https://github.com/microsoft/TypeScript/pull/64888) (Open, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**\[api\] Reduce allocations and megamorphic object penalty from generator methods**

*Optimize generator methods to reduce object allocations and megamorphic call penalties, improving microbenchmark performance.*

 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64888#issuecomment-6297633598) **andrewbranch** said "@typescript-bot perf test api"
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64888#issuecomment-6297635506) **typescript-automation[bot]** noted that the perf test api job started and provided links to build status and results
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64888#issuecomment-6298203638) **typescript-automation[bot]** reported performance results for the requested perf run to andrewbranch
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64916](https://github.com/microsoft/TypeScript/pull/64916) (Closed, `Domain: Performance`, `For Uncommitted Bug`)

**Make symbol tables insertion\-ordered**

*Use insertion-ordered symbol tables to eliminate nondeterministic iteration and ensure consistent diagnostics, declaration emissions, and type ID assignments.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/64916#issuecomment-6425766196) **typescript-automation[bot]** reported that the perf test build had started and provided status and results links
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64916#issuecomment-6430075994) **typescript-automation[bot]** said "@ahejlsberg, the perf run you requested failed. You can check the log here."
 * [today](https://github.com/microsoft/TypeScript/pull/64916#issuecomment-6439707277) **typescript-automation[bot]** provided the requested perf run results including a provisional hosted-runner comparison report for tsc
 * **jakebailey** added label `Domain: Performance`
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript#64928](https://github.com/microsoft/TypeScript/pull/64928) (Closed, `Domain: Performance`, `For Backlog Bug`)

**Reuse token lookup visitor across AST descent**

*Reuse a single NodeVisitor for each token lookup to reduce allocations and improve getTokenAtPosition performance.*

 * [5 days ago](https://github.com/microsoft/TypeScript/pull/64928#issuecomment-6350722523) **Tom4ikss** described experimenting with native API type queries in a build-time i18n plugin to reduce type analysis cost, isolated repeated visitor construction in a benchmark, and reported reduced allocations and faster microbenchmark lookups but no clear full-workload timing improvement
 * (yesterday) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64934](https://github.com/microsoft/TypeScript/pull/64934) (Open, `Domain: Performance`, `For Uncommitted Bug`)

**Skip discriminant lookups for unions that cannot be narrowed**

*Optimize union type checking by skipping discriminant lookups for unions that cannot be narrowed.*

 * [3 days ago](https://github.com/microsoft/TypeScript/pull/64934#issuecomment-6384201731) **jakebailey** said "@typescript-bot perf test this faster"
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/64934#issuecomment-6384202614) **typescript-automation[bot]** triggered performance test jobs and provided status and result links
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/64934#issuecomment-6385070155) **typescript-automation[bot]** provided the requested performance run results
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64936](https://github.com/microsoft/TypeScript/pull/64936) (Open, `Domain: Performance`, `For Backlog Bug`)

**Avoid rebuilding later LSP project references**

*Skip rebuilding project references in LSP when the opened file is already included, pruning redundant later candidates.*

 * created by **chengchuu**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/64936#issuecomment-6368320130) **chengchuu** said "@microsoft-github-policy-service agree"
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64942](https://github.com/microsoft/TypeScript/pull/64942) (Open, `Domain: Performance`, `For Uncommitted Bug`)

**Add program\.getAllDependencies to the API**

*Add program.getAllDependencies(file) to TypeScript's APIs to retrieve a file's full dependency graph using tsc's incremental builder data.*

 * created by **jackeddisciple**
 * (4 days ago) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64946](https://github.com/microsoft/TypeScript/pull/64946) (Open, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Remove checker pointer from Type**

*Removing the checker pointer from the Type structure and placing it in LazyState reduces Type’s memory footprint from 40 to 32 bytes.*

 * [4 days ago](https://github.com/microsoft/TypeScript/pull/64946#issuecomment-6376208030) **typescript-automation[bot]** reported start of performance tests and provided build status links
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/64946#issuecomment-6376663737) **typescript-automation[bot]** reported perf run results requested by @jakebailey
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/64946#issuecomment-6376728957) **jakebailey** said "Pretty disappointing, but I also didn't check the size class, and then also I don't think we allocate these in arenas"
 * **jakebailey** added label `Domain: Performance`

### [Issue microsoft/TypeScript#64953](https://github.com/microsoft/TypeScript/issues/64953) (Closed, `Bug`)

**Unsaved export not offered for auto\-import after reopening the importing file**

*TypeScript does not offer auto-import suggestions or import edits for functions defined in unsaved files when reopening the importing file.*

 * created by **johnsoncodehk**
 * (yesterday) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#64960](https://github.com/microsoft/TypeScript/pull/64960) (Closed, `For Backlog Bug`)

** Fix auto\-import not offering unsaved exports after auto\-imports were computed**

*Delay bucket cleanup until multiple files are dirty to ensure auto-import suggestions include unsaved exports*

 * [2 days ago](https://github.com/microsoft/TypeScript/pull/64960#issuecomment-6401269835) **1-DARK** said "@microsoft-github-policy-service agree"
 * (yesterday) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#64964](https://github.com/microsoft/TypeScript/pull/64964) (Closed, `Domain: Performance`, `For Uncommitted Bug`)

**Speed up union subset checks by scanning sorted constituents**

*Optimize subset checks on unions by scanning sorted constituent elements to improve performance.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/64964#issuecomment-6425158178) **typescript-automation[bot]** reported CI jobs starting and linking status URLs
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64964#issuecomment-6430143516) **typescript-automation[bot]** said "@jakebailey, the perf run you requested failed. You can check the log here."
 * [today](https://github.com/microsoft/TypeScript/pull/64964#issuecomment-6439425517) **typescript-automation[bot]** reported the requested performance run results
 * **jakebailey** added label `Domain: Performance`
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript#64972](https://github.com/microsoft/TypeScript/pull/64972) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Only pre\-size the printer buffer when printing a whole file**

*The printer buffer should only be pre-sized when printing an entire file to avoid wasting memory.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/64972#issuecomment-6429198483) **typescript-automation[bot]** said "@jakebailey, the perf run you requested failed. You can check the log here."
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64972#issuecomment-6430924112) **typescript-automation[bot]** said "@jakebailey, the perf run you requested failed. You can check the log here."
 * [today](https://github.com/microsoft/TypeScript/pull/64972#issuecomment-6439402180) **typescript-automation[bot]** provided the requested performance run results including comparison metrics
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#64974](https://github.com/microsoft/TypeScript/issues/64974) (Open, `Bug`)

**7\.1: destructured parameter with a \`= {}\` default loses its contextual type \(TS7031\)**

*TypeScript 7.1 regression causes destructured parameters with a default {} to lose their contextual types and trigger implicit any errors.*

 * created by **raimonade**
 * [today](https://github.com/microsoft/TypeScript/issues/64974#issuecomment-6447340132) **jltrv** reported two additional regression variants in TypeScript 7.1.0-dev affecting nested default-initialized patterns and non-empty object literal defaults and quantified their impact

### [Issue microsoft/TypeScript#64975](https://github.com/microsoft/TypeScript/issues/64975) (Closed)

**Missing namespace qualifier in \`import =\` emit across merged namespaces**

*TypeScript 7 fails to qualify import-equals aliases in merged namespaces, causing runtime ReferenceError due to missing namespace qualifier.*

 * created by **magic-akari**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64976](https://github.com/microsoft/TypeScript/pull/64976) (Closed, `For Uncommitted Bug`)

**Qualify merged namespace references in import\-equals emit**

*Qualify merged namespace references in import-equals emit with explicit namespace names and add conformance tests.*

 * created by **magic-akari**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64979](https://github.com/microsoft/TypeScript/pull/64979) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **ahejlsberg**)

**Optimized insertion\-ordered symbol tables**

*Reduce symbol table memory usage by storing entries as pointers and using proxy symbols for renamed entries.*

 * created by **ahejlsberg**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`, and assigned to **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript/pull/64979#issuecomment-6449154058) **ahejlsberg** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/64979#issuecomment-6449157583) **typescript-automation[bot]** reported CI job statuses with links to build results
 * [today](https://github.com/microsoft/TypeScript/pull/64979#issuecomment-6449881971) **typescript-automation[bot]** reported that the DT test results were ready with no changes
 * [today](https://github.com/microsoft/TypeScript/pull/64979#issuecomment-6449966857) **typescript-automation[bot]** provided tsc user test results and indicated everything looked good
 * [today](https://github.com/microsoft/TypeScript/pull/64979#issuecomment-6450542833) **typescript-automation[bot]** reported the requested performance run results for baseline and PR, indicating no change in errors, symbols, or types and decreased memory usage
 * **jakebailey** added label `Domain: Performance`
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript#64980](https://github.com/microsoft/TypeScript/issues/64980) (Open, `Bug`)

**\`\-\-experimentalDecorators\`: decorated \`abstract\` property is emitted as a class field \(regression in 7\.0\)**

*TypeScript 7.0 regressively emits a class field for decorated abstract properties, shadowing prototype decorators instead of erasing the field.*

 * created by **simleb**

### [Issue microsoft/TypeScript#64981](https://github.com/microsoft/TypeScript/issues/64981) (Open, `Bug`, **RyanCavanaugh**, **Copilot**)

**TS7\+ drops required parentheses in \`new \(f\(\) as T\)\.C\(\)\`, emitting incorrectly as \`new f\(\)\.C\(\)\`**

*TypeScript 7 emits new expressions without required parentheses when using type assertions, causing incorrect new f().C() invocation*

 * created by **blickly**
 * (today) **RyanCavanaugh** added label `Bug`, and assigned to **Copilot**, **RyanCavanaugh**

### [PR microsoft/TypeScript#64982](https://github.com/microsoft/TypeScript/pull/64982) (Open, `For Backlog Bug`)

**erase decorated abstract properties under experimentalDecorators with define semantics**

*Prevent decorated abstract class properties from emitting instance fields under experimentalDecorators with useDefineForClassFields.*

 * created by **1-DARK**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [Issue microsoft/TypeScript#64983](https://github.com/microsoft/TypeScript/issues/64983) (Open)

**Module resolution: imports in a referenced \`nodenext\` ESM project resolve in CJS mode when the referencing project uses \`bundler\`**

*ESM module imports in a nodenext project incorrectly resolve to CJS files when referenced by a bundler-resolved project.*

 * created by **joshkel**

### [PR microsoft/TypeScript#64984](https://github.com/microsoft/TypeScript/pull/64984) (Open, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Add distributive conditional type relationship rules**

*Add distributive conditional type relationship rules with a function type mapper to ensure correct assignability and inference handling.*

 * created by **weswigham**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`, `For Uncommitted Bug`, and assigned to **weswigham**
 * [today](https://github.com/microsoft/TypeScript/pull/64984#issuecomment-6454176538) **weswigham** said "@typescript-bot test this"
 * [today](https://github.com/microsoft/TypeScript/pull/64984#issuecomment-6454178389) **typescript-automation[bot]** reported CI job statuses and results for multiple test commands
 * [today](https://github.com/microsoft/TypeScript/pull/64984#issuecomment-6454680183) **typescript-automation[bot]** informed that DT test results were ready and unchanged and provided a log link
 * [today](https://github.com/microsoft/TypeScript/pull/64984#issuecomment-6454801326) **typescript-automation[bot]** reported TSC test results with new TS2578 unused '@ts-expect-error' errors in Option.ts and Result.ts, and a TS2379 type mismatch error under exactOptionalPropertyTypes in effect.ts
 * [today](https://github.com/microsoft/TypeScript/pull/64984#issuecomment-6454851558) **typescript-automation[bot]** said "@weswigham, the perf run you requested failed. You can check the log here."
 * [today](https://github.com/microsoft/TypeScript/pull/64984#issuecomment-6455820711) **typescript-automation[bot]** provided build comparison results for top 400 repos between baseline and pr and highlighted errors in fabricjs/fabric.js
 * [today](https://github.com/microsoft/TypeScript/pull/64984#issuecomment-6458048810) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/64984#issuecomment-6458050513) **typescript-automation[bot]** posted an automated build status update
 * [today](https://github.com/microsoft/TypeScript/pull/64984#issuecomment-6458501848) **typescript-automation[bot]** posted the requested performance run results for tsc

### [PR microsoft/TypeScript#64985](https://github.com/microsoft/TypeScript/pull/64985) (Closed, `Author: Team`, `For Uncommitted Bug`, **RyanCavanaugh**, **Copilot**)

**\[WIP\] Fix TS7\+ emission of new expression parentheses**

*Add regression tests and fix TS7+ new-expression parenthesization while performing security and repository validation.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#64986](https://github.com/microsoft/TypeScript/pull/64986) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Add a default PGO profile for the compiler**

*Add a default PGO profile generated from representative compiler scenarios using the TypeScript benchmarking workflow.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/64986#issuecomment-6454427871) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/64986#issuecomment-6454430030) **typescript-automation[bot]** reported that performance test jobs started and provided status and result links
 * [today](https://github.com/microsoft/TypeScript/pull/64986#issuecomment-6455180420) **typescript-automation[bot]** posted performance run results including provisional hosted-runner metrics and a tsc comparison report
 * [today](https://github.com/microsoft/TypeScript/pull/64986#issuecomment-6456804734) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/64986#issuecomment-6456807495) **typescript-automation[bot]** announced that performance tests started and provided status and result links
 * [today](https://github.com/microsoft/TypeScript/pull/64986#issuecomment-6457508015) **typescript-automation[bot]** said "@jakebailey, the perf run you requested failed. You can check the log here."
 * [today](https://github.com/microsoft/TypeScript/pull/64986#issuecomment-6458048512) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/64986#issuecomment-6458049817) **typescript-automation[bot]** reported that the perf test this faster build started and provided status and results links
 * [today](https://github.com/microsoft/TypeScript/pull/64986#issuecomment-6458586693) **typescript-automation[bot]** posted the requested performance run results for tsc
 * [today](https://github.com/microsoft/TypeScript/pull/64986#issuecomment-6460332583) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/64986#issuecomment-6460333783) **typescript-automation[bot]** reported the start of a performance test job and provided a status table
 * [today](https://github.com/microsoft/TypeScript/pull/64986#issuecomment-6460816180) **typescript-automation[bot]** reported the results of the requested performance run
 * [later](https://github.com/microsoft/TypeScript/pull/64986#issuecomment-6463005992) **jakebailey** said "@typescript-bot perf test this faster"
 * [later](https://github.com/microsoft/TypeScript/pull/64986#issuecomment-6463007496) **typescript-automation[bot]** reported that performance tests started and provided links to status and results
 * [later](https://github.com/microsoft/TypeScript/pull/64986#issuecomment-6463839333) **typescript-automation[bot]** posted performance results for the requested run including baseline-to-PR comparison metrics for tsc
 * **jakebailey** added label `Domain: Performance`

### [Issue microsoft/TypeScript#64987](https://github.com/microsoft/TypeScript/issues/64987) (Open)

**LSP: newly created file is assigned to the wrong project when the project path contains '\[' / '{' \(or include differs only by case\)**

*Newly created files under directories with square brackets or case-insensitive name differences are assigned to the wrong TypeScript project.*

 * created by **1-DARK**
 * [later](https://github.com/microsoft/TypeScript/issues/64987#issuecomment-6473611408) **jakebailey** asked if the reporter personally encountered the bug or used an AI agent to find it
 * [later](https://github.com/microsoft/TypeScript/issues/64987#issuecomment-6473912586) **1-DARK** reproduced the issue end-to-end with the tsgo LSP binary in bracketed directories, observed a false TS2550 error, and offered a repro script while noting it may be an edge case

### [PR microsoft/TypeScript#64988](https://github.com/microsoft/TypeScript/pull/64988) (Open, `Author: Team`, `For Uncommitted Bug`, **iisaduan**)

**Add missing Program and Project Methods**

*Add several missing Program API methods (for counts, diagnostics and references) and Project API methods for file and configuration access.*

 * created by **iisaduan**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **iisaduan**

### [PR microsoft/TypeScript#64989](https://github.com/microsoft/TypeScript/pull/64989) (Open, `Domain: Performance`, `For Uncommitted Bug`)

**Check ASCII identifier bytes with a lookup table**

*A lookup table for ASCII identifier checks speeds BenchmarkParse by 1-3% on M1 and yields larger gains for longer identifiers.*

 * created by **Andarist**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/64989#issuecomment-6465043739) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [later](https://github.com/microsoft/TypeScript/pull/64989#issuecomment-6466036426) **jakebailey** said "@typescript-bot perf test this faster"
 * [later](https://github.com/microsoft/TypeScript/pull/64989#issuecomment-6466038314) **typescript-automation[bot]** reported CI jobs start and linked build results
 * [later](https://github.com/microsoft/TypeScript/pull/64989#issuecomment-6466967535) **typescript-automation[bot]** provided the requested performance run results for tsc, including a provisional hosted-runner comparison table indicating no significant changes
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#64990](https://github.com/microsoft/TypeScript/pull/64990) (Open, `Domain: Performance`, `For Uncommitted Bug`)

**Find the end of multi\-line comments with a substring search after the first line break**

*Optimize multi-line comment parsing with substring search after the first line break to speed JSDoc-heavy files by 7%.*

 * created by **Andarist**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/64990#issuecomment-6465828466) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [later](https://github.com/microsoft/TypeScript/pull/64990#issuecomment-6466052836) **jakebailey** said "@typescript-bot perf test this faster"
 * [later](https://github.com/microsoft/TypeScript/pull/64990#issuecomment-6466054741) **typescript-automation[bot]** reported start of perf test and linked build status and results
 * [later](https://github.com/microsoft/TypeScript/pull/64990#issuecomment-6467119211) **typescript-automation[bot]** posted the results of the requested perf run
 * **jakebailey** added label `Domain: Performance`

### [Issue microsoft/TypeScript#64991](https://github.com/microsoft/TypeScript/issues/64991) (Open)

**\`typescript/sync\`: tuples and type literals from \`checker\.typeToTypeNode\` print multi\-line \(SingleLine flag lost\)**

*With TypeScript/sync 7.1.0-dev, checker.typeToTypeNode prints tuple and object type literals as multi-line nodes, losing single-line formatting.*

 * created by **todor-a**

### [PR microsoft/TypeScript#64992](https://github.com/microsoft/TypeScript/pull/64992) (Open, `Domain: Performance`, `For Uncommitted Bug`)

**Speedup keywords lookup with a perfect hash table in GetIdentifierToken**

*Replace the general-purpose Go map with a dedicated perfect hash table for static keyword lookup, boosting parsing speed by about 3%.*

 * created by **Andarist**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/64992#issuecomment-6467051663) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [later](https://github.com/microsoft/TypeScript/pull/64992#issuecomment-6470850421) **jakebailey** said "@typescript-bot perf test this faster"
 * [later](https://github.com/microsoft/TypeScript/pull/64992#issuecomment-6470852722) **typescript-automation[bot]** reported start of performance tests with status and results links
 * **jakebailey** added label `Domain: Performance`
 * [later](https://github.com/microsoft/TypeScript/pull/64992#issuecomment-6471936203) **typescript-automation[bot]** reported the requested performance run results

### [PR microsoft/TypeScript#64993](https://github.com/microsoft/TypeScript/pull/64993) (Open, `For Uncommitted Bug`)

**Drop statements a top\-level await reparse consumed to the end of the file**

*Prevent top-level await reparsing from copying original statements past EOF to avoid overlapping parsed statements.*

 * created by **roninjin10**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [PR microsoft/TypeScript#64994](https://github.com/microsoft/TypeScript/pull/64994) (Open, `For Uncommitted Bug`)

**Format Document: shift the indenters a moved line break carries along**

*Adding line breaks before tokens makes document formatting non-idempotent by shifting nested indenters due to stale deltas and improper resets.*

 * created by **roninjin10**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/64994#issuecomment-6469533497) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."

### [Issue microsoft/TypeScript#64995](https://github.com/microsoft/TypeScript/issues/64995) (Open)

**Generic class in a reference cycle measured invariant in 7\.1: \`Link\<Sub\>\` no longer assignable to \`Link\<EntityBase\>\` \(@sap\-cloud\-sdk/odata\-common\)**

*Upgrading to @sap-cloud-sdk/odata-common v7.1 introduced an invariant generic regression that prevents Link<Sub> from being assignable to Link<EntityBase>.*

 * created by **todor-a**

