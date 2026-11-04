# Report for 2026-10-30 (Friday, October 30th, 2026)

17 different users commented on 56 different issues.

## Recommended Actions

 * Response Recommended
    * @denis-migdal asked if improving `infer` could solve the issue in [microsoft/TypeScript#40179](https://github.com/microsoft/TypeScript/issues/40179#issuecomment-6532881578)
    * @brian-xu-vlt asked if there was any progress on the issue and offered to help in [microsoft/TypeScript#64108](https://github.com/microsoft/TypeScript/pull/64108#issuecomment-6541367677)
    * @artile provided repro steps and detailed version comparison in [microsoft/TypeScript#64757](https://github.com/microsoft/TypeScript/issues/64757#issuecomment-6544123377)
    * @ycmjason reported a panic in API's createSnapshot for .ts files and provided repro steps in [microsoft/TypeScript#65054](https://github.com/microsoft/TypeScript/issues/65054#issuecomment-6533833790)
    * @el-j asked a maintainer to approve pending workflows and review the updated PR in [microsoft/TypeScript#65058](https://github.com/microsoft/TypeScript/pull/65058#issuecomment-6527518658)
    * @el-j asked a maintainer to re-review and enable required CI checks in [microsoft/TypeScript#65058](https://github.com/microsoft/TypeScript/pull/65058#issuecomment-6528188256)

## Activity Summary

### [Issue microsoft/TypeScript#40179](https://github.com/microsoft/TypeScript/issues/40179) (Open, `Suggestion`, `Awaiting More Feedback`)

**Add type operators that can answer "given function type T, what is the type of its return value when arguments P are passed in?"**

*Propose new TypeScript type operators to infer a function’s return type for given arguments, including overloads.*

 * [3.9 years ago](https://github.com/microsoft/TypeScript/issues/40179#issuecomment-1336607003) **jcalz** cross-linked issue #17961
 * [3.3 years ago](https://github.com/microsoft/TypeScript/issues/40179#issuecomment-1634391715) **Autumn-one** said "From the user's point of view, this function is very useful, I hope the official can be more from the user's point of view"
 * [3.1 years ago](https://github.com/microsoft/TypeScript/issues/40179#issuecomment-1685152670) **jcalz** said "Cross-linking to https://github.com/microsoft/TypeScript/issues/52035#issuecomment-1402795342 and specifically the term "call types""
 * [today](https://github.com/microsoft/TypeScript/issues/40179#issuecomment-6532881578) **denis-migdal** mentioned simulating HKT features, provided example code, and asked if improving `infer` could solve the issue

### [Issue microsoft/TypeScript#59979](https://github.com/microsoft/TypeScript/issues/59979) (Closed, `Bug`, `Help Wanted`, `Domain: LS: Inlay Hints`, `7.0 LS Migration`)

**Inlay parameter hints don't account for trailing required parameters**

*Inlay hints for rest parameters typed as tuples incorrectly place labels and fail to account for trailing required elements.*

 * [2.1 years ago](https://github.com/microsoft/TypeScript/issues/59979#issuecomment-2354883410) **dappduck** said "Hello @Andarist I started looking at this issue"
 * (1 year ago) **RyanCavanaugh** added labels `Domain: Inlay Hints`, `7.0 LS Migration`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64108](https://github.com/microsoft/TypeScript/pull/64108) (Closed, `Author: Team`, `For Uncommitted Bug`, **RyanCavanaugh**, **Copilot**)

**Fix call hierarchy file node paths**

*Display file basenames with project-relative directories in call hierarchy nodes instead of absolute file paths.*

 * (8 weeks ago) **typescript-automation[bot]** added label `For Uncommitted Bug`, and removed label `For Milestone Bug`
 * [8 weeks ago](https://github.com/microsoft/TypeScript/pull/64108#issuecomment-5498368978) **jakebailey** mentioned that the old VS Code extension made paths relative to the workspace root and suggested plumbing that info from the init message
 * [later](https://github.com/microsoft/TypeScript/pull/64108#issuecomment-6541367677) **brian-xu-vlt** said "Hi! As OP on the issue #64097, I was wondering if there is any progress on this issue? Can I help in any way? "
 * [later](https://github.com/microsoft/TypeScript/pull/64108#issuecomment-6542437743) **jakebailey** said "@copilot+gpt-6.1-sol merge main and do better per the above"
 * **typescript-automation[bot]** added label `Author: Team`
 * [later](https://github.com/microsoft/TypeScript/pull/64108#issuecomment-6542774931) **Copilot** merged main and updated call hierarchy to use initialized workspace folders with typed paths, noted build, tests, lint, and format passed but CodeQL was blocked by a Git diff timeout

### [PR microsoft/TypeScript#64363](https://github.com/microsoft/TypeScript/pull/64363) (Closed, `For Backlog Bug`)

**Fix inlay hints for trailing required rest elements**

*Adjust inlay parameter name hint mapping for rest parameters with trailing required tuple elements and skip destructured parameters*

 * created by **yksr-melt**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64410](https://github.com/microsoft/TypeScript/pull/64410) (Closed, `Author: Team`, `For Backlog Bug`, **jakebailey**)

**Align inlay hints with trailing tuple arguments**

*Adjust inlay hint positioning to align correctly with trailing tuple arguments.*

 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [5 weeks ago](https://github.com/microsoft/TypeScript/pull/64410#issuecomment-5800423567) **jakebailey** mentioned that trailing fixed elements were still mapped incorrectly when tuples contained multiple generic variadic elements and suggested a closer look
 * [5 weeks ago](https://github.com/microsoft/TypeScript/pull/64410#issuecomment-5803962530) **jakebailey** said "Leave it to copilot review to keep finding weird edge cases, sigh"
 * [today](https://github.com/microsoft/TypeScript/pull/64410#issuecomment-6530363537) **andrewbranch** said "Looks like this needs a merge with main."
 * [today](https://github.com/microsoft/TypeScript/pull/64410#issuecomment-6530794126) **jakebailey** said "Should be fixed now"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64500](https://github.com/microsoft/TypeScript/pull/64500) (Open, `For Uncommitted Bug`, **andrewbranch**)

**Add support for setting emit flags and synthetic comments**

*Enable configuring emit flags and injecting synthetic comments into the compiler’s output.*

 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [1 month ago](https://github.com/microsoft/TypeScript/pull/64500#issuecomment-5873403732) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * **typescript-automation[bot]** assigned to **andrewbranch**
 * [later](https://github.com/microsoft/TypeScript/pull/64500#issuecomment-6541748893) **el-j** notified maintainers of overlap between this PR and #65058, advocated for this PR’s design to land, outlined its advantages, offered to contribute additional tests, and clarified no action was needed from the author

### [Issue microsoft/TypeScript#64757](https://github.com/microsoft/TypeScript/issues/64757) (Open, `Needs Investigation`, **ahejlsberg**)

**Regression in 7\.1 \(\#64553\): R inferred as unknown through a generic type alias call signature with a nested same\-type argument**

*A TypeScript 7.1 regression makes R infer as unknown rather than Req in a nested generic type alias call signature.*

 * (1 week ago) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **ahejlsberg**
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/64757#issuecomment-6319872131) **kennysarnoski-jarvis** ran the repro locally and confirmed regression TS2571 on nightly builds, described inference failure conditions and downstream tool impact
 * [later](https://github.com/microsoft/TypeScript/issues/64757#issuecomment-6544123377) **artile** provided a third real-world example highlighting a TypeScript inference failure in nested generic interfaces, added two distinguishing details, and demonstrated which 7.1.0-dev versions failed using code, tsconfig, and a results table

### [PR microsoft/TypeScript#64868](https://github.com/microsoft/TypeScript/pull/64868) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Compare names before symbols when matching flow references**

*Compare declaration and reference names before symbol lookup to reduce analysis overhead and improve performance.*

 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64868#issuecomment-6272839100) **typescript-automation[bot]** started performance tests and posted links to build status and results
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64868#issuecomment-6273381312) **typescript-automation[bot]** provided the requested performance run results
 * **jakebailey** added label `Domain: Performance`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64869](https://github.com/microsoft/TypeScript/pull/64869) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Store merged symbols in a paged symbol link store**

*Use a paged symbol link store indexed by dense symbol IDs to avoid getMergedSymbol map misses and improve performance.*

 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64869#issuecomment-6273347159) **typescript-automation[bot]** started build jobs and posted status and results links
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64869#issuecomment-6274004601) **typescript-automation[bot]** posted the requested performance run results including a comparison report of tsc metrics such as errors, symbols, types, memory used, and memory allocations
 * **jakebailey** added label `Domain: Performance`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64922](https://github.com/microsoft/TypeScript/pull/64922) (Closed, `For Uncommitted Bug`)

**Emit the files of each checker in a deterministic order**

*Ensure each checker emits its files in a consistent, deterministic order to eliminate non-determinism.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/64922#issuecomment-6490336444) **typescript-automation[bot]** posted perf run results comparing baseline and PR metrics, including errors, symbols, types, memory usage, and allocations
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64922#issuecomment-6506518606) **jakebailey** reported merge failures due to changed baseline files in generateTrace tests
 * [today](https://github.com/microsoft/TypeScript/pull/64922#issuecomment-6520433459) **Andarist** explained adding an emitPrint tracing event and resolving the missing logs so the changes are landable
 * [today](https://github.com/microsoft/TypeScript/pull/64922#issuecomment-6533000613) **jakebailey** requested the typescript-bot to perform a faster performance test
 * [today](https://github.com/microsoft/TypeScript/pull/64922#issuecomment-6533002379) **typescript-automation[bot]** posted an automated CI status update indicating performance tests had started with links to build status and results
 * [today](https://github.com/microsoft/TypeScript/pull/64922#issuecomment-6533881634) **typescript-automation[bot]** provided the perf run results including detailed metrics for tsc such as errors, symbols, types, memory used, and memory allocs
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#64974](https://github.com/microsoft/TypeScript/issues/64974) (Open, `Bug`)

**7\.1: destructured parameter with a \`= {}\` default loses its contextual type \(TS7031\)**

*TypeScript 7.1 regression causes destructured parameters with a default {} to lose their contextual types and trigger implicit any errors.*

 * created by **raimonade**
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/64974#issuecomment-6447340132) **jltrv** reported two additional regression variants in TypeScript 7.1.0-dev affecting nested default-initialized patterns and non-empty object literal defaults and quantified their impact
 * (today) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`

### [PR microsoft/TypeScript#64978](https://github.com/microsoft/TypeScript/pull/64978) (Open, `For Backlog Bug`)

**fix\(64974\): fix contextual typing for destructured parameter defaults**

*Correct contextual type inference for destructured parameters with default values.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/64978#issuecomment-6506497425) **timurzvural** opened an alternative PR (#65016) covering #65011 with contextual-type guards for object and array padding and added JSDoc returns, casts, and annotated .ts cases from #65011 atop #64974 scenarios
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64978#issuecomment-6512865798) **nrjdalal** provided an additional repro case with code and described how binding elements with defaults behaved across TypeScript versions
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64978#issuecomment-6513976139) **timurzvural** explained the regression behavior on TS 7.1 for object literals with defaults and proposed PR #65016 as an alternative solution
 * (today) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`

### [Issue microsoft/TypeScript#64980](https://github.com/microsoft/TypeScript/issues/64980) (Closed, `Bug`)

**\`\-\-experimentalDecorators\`: decorated \`abstract\` property is emitted as a class field \(regression in 7\.0\)**

*TypeScript 7.0 regressively emits a class field for decorated abstract properties, shadowing prototype decorators instead of erasing the field.*

 * created by **simleb**
 * (today) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#64981](https://github.com/microsoft/TypeScript/issues/64981) (Closed, `Bug`, **RyanCavanaugh**, **Copilot**)

**TS7\+ drops required parentheses in \`new \(f\(\) as T\)\.C\(\)\`, emitting incorrectly as \`new f\(\)\.C\(\)\`**

*TypeScript 7 emits new expressions without required parentheses when using type assertions, causing incorrect new f().C() invocation*

 * (3 days ago) **RyanCavanaugh** added label `Bug`, and assigned to **Copilot**, **RyanCavanaugh**
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#64982](https://github.com/microsoft/TypeScript/pull/64982) (Closed, `For Backlog Bug`)

**erase decorated abstract properties under experimentalDecorators with define semantics**

*Prevent decorated abstract class properties from emitting instance fields under experimentalDecorators with useDefineForClassFields.*

 * created by **1-DARK**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (today) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`

### [PR microsoft/TypeScript#64992](https://github.com/microsoft/TypeScript/pull/64992) (Closed, `Domain: Performance`, `For Uncommitted Bug`)

**Speedup keywords lookup with a perfect hash table in GetIdentifierToken**

*Replace the general-purpose Go map with a dedicated perfect hash table for static keyword lookup, boosting parsing speed by about 3%.*

 * [today](https://github.com/microsoft/TypeScript/pull/64992#issuecomment-6526064873) **typescript-automation[bot]** said "Hey @jakebailey, this PR was updated less than two minutes before this command. Please wait until it has been unchanged for two minutes and try again."
 * [today](https://github.com/microsoft/TypeScript/pull/64992#issuecomment-6526797614) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/64992#issuecomment-6526800123) **typescript-automation[bot]** reported that the perf test this faster job started with links to the build and results
 * [today](https://github.com/microsoft/TypeScript/pull/64992#issuecomment-6527963638) **typescript-automation[bot]** provided the requested performance run results
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#65004](https://github.com/microsoft/TypeScript/pull/65004) (Open, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Allow builds to skip source generation**

*Add a build flag to skip source generation and shorten the benchmark preparation phase.*

 * (2 days ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`
 * **jakebailey** added label `Domain: Performance`
 * [today](https://github.com/microsoft/TypeScript/pull/65004#issuecomment-6533247410) **jakebailey** said "I'm realizing that this also has to apply to run dt, the top tests, error deltas, in addition to the perf run. So maybe just gating this on CI is the correct move."

### [PR microsoft/TypeScript#65015](https://github.com/microsoft/TypeScript/pull/65015) (Closed, `For Uncommitted Bug`, **RyanCavanaugh**)

**Fix new\-expression emit parentheses after type erasure \(\#64981\)**

*Ensure the TypeScript emitter parenthesizes new-expressions with type assertions to prevent incorrect runtime emits.*

 * created by **timurzvural**
 * (yesterday) **typescript-automation[bot]** added label `For Uncommitted Bug`, and assigned to **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript/pull/65015#issuecomment-6528348250) **RyanCavanaugh** said "Closing in favor of #65060 which has more exhaustive test coverage"
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#65017](https://github.com/microsoft/TypeScript/pull/65017) (Open, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Skip non\-scope ancestors quickly in NameResolver\.Resolve**

*Refactor NameResolver.Resolve to classify node kinds and skip non-scope ancestors for faster scope resolution.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/65017#issuecomment-6506905853) **typescript-automation[bot]** started CI jobs and updated the comment with a status table and links
 * **jakebailey** added label `Domain: Performance`
 * [yesterday](https://github.com/microsoft/TypeScript/pull/65017#issuecomment-6507971544) **typescript-automation[bot]** posted the results of the requested performance run including comparison metrics
 * [today](https://github.com/microsoft/TypeScript/pull/65017#issuecomment-6531358576) **jakebailey** said "This also seems like virtually no difference..."

### [PR microsoft/TypeScript#65019](https://github.com/microsoft/TypeScript/pull/65019) (Open, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Split link store lookups into inlineable fast paths**

*Move entry creation logic to getSlow methods so LinkStore.Get and PagedLinkStore.Get fast-path lookups can be inlined.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/65019#issuecomment-6507010241) **typescript-automation[bot]** reported that performance test jobs had started and provided status and results links
 * **jakebailey** added label `Domain: Performance`
 * [yesterday](https://github.com/microsoft/TypeScript/pull/65019#issuecomment-6508179552) **typescript-automation[bot]** posted performance run results for the requested perf run
 * [today](https://github.com/microsoft/TypeScript/pull/65019#issuecomment-6531349374) **jakebailey** said "Hm, seems like virtually no difference."

### [PR microsoft/TypeScript#65024](https://github.com/microsoft/TypeScript/pull/65024) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Add lint rule requiring SAFETY comments on unsafe operations**

*Add a lint rule requiring explicit SAFETY comments to document invariants for unsafe operations.*

 * (yesterday) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#65025](https://github.com/microsoft/TypeScript/pull/65025) (Open, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Pre\-size member, export, and locals symbol tables**

*Pre-size member, export, and local symbol tables based on declaration counts to avoid repetitive resizing and improve allocation efficiency*

 * **jakebailey** added label `Domain: Performance`
 * [yesterday](https://github.com/microsoft/TypeScript/pull/65025#issuecomment-6508738862) **typescript-automation[bot]** shared the results of the requested performance run
 * [yesterday](https://github.com/microsoft/TypeScript/pull/65025#issuecomment-6508803056) **Copilot** noted failure of custom setup steps in the Copilot code review run
 * [today](https://github.com/microsoft/TypeScript/pull/65025#issuecomment-6531121550) **jakebailey** said "This does not feel super worth it based on the benchmarks and the amount of code"

### [PR microsoft/TypeScript#65027](https://github.com/microsoft/TypeScript/pull/65027) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Report overflow when ReadDirectoryChangesW returns zero bytes**

*ReadDirectoryChangesW returns zero bytes and drops all events on buffer overflow rather than signaling ErrOverflow.*

 * (yesterday) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#65043](https://github.com/microsoft/TypeScript/pull/65043) (Open, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Speed up property and index signature lookups**

*Optimize property and index signature lookup processes to improve performance.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/65043#issuecomment-6510120464) **typescript-automation[bot]** reported that perf test jobs started and provided links to build status and results
 * **jakebailey** added label `Domain: Performance`
 * [yesterday](https://github.com/microsoft/TypeScript/pull/65043#issuecomment-6511137405) **typescript-automation[bot]** posted perf run results as requested
 * [today](https://github.com/microsoft/TypeScript/pull/65043#issuecomment-6531267073) **jakebailey** said "FWIW this looks way better if you view each commit without whitespace, or at least the whole thing https://github.com/microsoft/TypeScript/pull/65043/changes?w=1"

### [PR microsoft/TypeScript#65045](https://github.com/microsoft/TypeScript/pull/65045) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Reject non\-access targets early when matching access references**

*Move logic to reject non-access targets early in access reference matching to improve efficiency.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/65045#issuecomment-6510970606) **typescript-automation[bot]** announced that performance test jobs had started and provided links to their status and results
 * **jakebailey** added label `Domain: Performance`
 * [yesterday](https://github.com/microsoft/TypeScript/pull/65045#issuecomment-6511745493) **typescript-automation[bot]** reported the performance run results for tsc comparing baseline and pr
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#65054](https://github.com/microsoft/TypeScript/issues/65054) (Open)

**API server panics in acquireConfigForFile when opening a JS file a tsconfig does not include**

*TypeScript sync API server panics when opening a JS file not included in tsconfig starting in version 7.1.0-beta.*

 * created by **0x80**
 * [today](https://github.com/microsoft/TypeScript/issues/65054#issuecomment-6533833790) **ycmjason** reported panic in the TypeScript sync API’s createSnapshot for .ts files when the nearest tsconfig.json had no matching files

### [PR microsoft/TypeScript#65055](https://github.com/microsoft/TypeScript/pull/65055) (Closed, `For Uncommitted Bug`)

**fix\(65053\): cover protected optional property completion**

*Enable code completion support for protected optional class properties.*

 * created by **a-tarasyuk**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#65056](https://github.com/microsoft/TypeScript/pull/65056) (Open, `Domain: Performance`, `For Uncommitted Bug`)

**Avoid resolving property types that cannot be unit types when looking for key properties**

*Prevent resolution of property types that cannot be unit types when searching for key properties.*

 * [today](https://github.com/microsoft/TypeScript/pull/65056#issuecomment-6526317046) **jakebailey** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/65056#issuecomment-6526319316) **typescript-automation[bot]** posted automated build status updates
 * [today](https://github.com/microsoft/TypeScript/pull/65056#issuecomment-6527098197) **typescript-automation[bot]** informed that the DT test results were ready and remained unchanged
 * [today](https://github.com/microsoft/TypeScript/pull/65056#issuecomment-6527257709) **typescript-automation[bot]** reported tsc user test results and confirmed everything looked good
 * **jakebailey** added label `Domain: Performance`
 * [today](https://github.com/microsoft/TypeScript/pull/65056#issuecomment-6527601543) **typescript-automation[bot]** reported the results of the requested perf run including metrics for errors, symbols, types, memory usage, and allocations
 * [today](https://github.com/microsoft/TypeScript/pull/65056#issuecomment-6528497241) **typescript-automation[bot]** reported that running the top 400 repos tsc comparison between baseline and pr succeeded without issues

### [PR microsoft/TypeScript#65058](https://github.com/microsoft/TypeScript/pull/65058) (Open, `For Uncommitted Bug`)

**feat\(printer\): implement JSDoc node emission in AST printer**

*Implement canonical JSDoc block and tag emission in AST printer with synthetic comment support in JS and Go printNode APIs.*

 * created by **el-j**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/65058#issuecomment-6527458799) **el-j** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript/pull/65058#issuecomment-6527518658) **el-j** mentioned addressing all review threads, validating tests locally, and requesting maintainer approval of pending workflows and review of the updated PR
 * [today](https://github.com/microsoft/TypeScript/pull/65058#issuecomment-6528188256) **el-j** addressed five new review comments, resolved all review threads, passed local tests, and requested maintainer re-review and CI enabling

### [PR microsoft/TypeScript#65059](https://github.com/microsoft/TypeScript/pull/65059) (Closed, `Author: Team`, `For Milestone Bug`, **ahejlsberg**, **gabritto**)

**Allow accessing named declared members during a type's resolution**

*Enable accessing both declared and inherited named members during lazy type resolution*

 * **typescript-automation[bot]** added label `For Milestone Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/65059#issuecomment-6527083233) **ahejlsberg** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/65059#issuecomment-6527085078) **typescript-automation[bot]** posted automated build status updates with command statuses and results links
 * [today](https://github.com/microsoft/TypeScript/pull/65059#issuecomment-6527790536) **typescript-automation[bot]** reported that the DT test results were ready and unchanged
 * [today](https://github.com/microsoft/TypeScript/pull/65059#issuecomment-6528046805) **typescript-automation[bot]** provided tsc user test results and indicated everything looked good
 * [today](https://github.com/microsoft/TypeScript/pull/65059#issuecomment-6528403907) **typescript-automation[bot]** provided detailed performance run results for the requested comparison report
 * [today](https://github.com/microsoft/TypeScript/pull/65059#issuecomment-6529242815) **typescript-automation[bot]** reported successful tsc comparison between baseline and pr on the top 400 repos
 * [today](https://github.com/microsoft/TypeScript/pull/65059#issuecomment-6530952312) **jakebailey** mentioned that their branch making the checker order-independent and idempotent fixed the problem and said they would open a PR soon
 * [today](https://github.com/microsoft/TypeScript/pull/65059#issuecomment-6531469952) **ahejlsberg** asked how the branch making the checker order-independent/idempotent fixed the problem
 * [today](https://github.com/microsoft/TypeScript/pull/65059#issuecomment-6531776091) **jakebailey** described resolution behavior, noted matching behavior, and said they were rebasing their branch to share for testing
 * [today](https://github.com/microsoft/TypeScript/pull/65059#issuecomment-6533262468) **jakebailey** said "I sent #65064 just to at least have something out there to point at."
 * [today](https://github.com/microsoft/TypeScript/pull/65059#issuecomment-6534072734) **jakebailey** admitted a previous mistake, confirmed that his branch's behavior matched, and questioned whether the PR was order dependent
 * [today](https://github.com/microsoft/TypeScript/pull/65059#issuecomment-6535488463) **ahejlsberg** asked what the branch's behavior matched
 * [today](https://github.com/microsoft/TypeScript/pull/65059#issuecomment-6535526457) **jakebailey** said "This PR's, since I had already "fixed" this unknowingly."
 * [today](https://github.com/microsoft/TypeScript/pull/65059#issuecomment-6535714848) **ahejlsberg** observed that issue #65064 included complex code guarded by a new `ObjectFlagsMembersResolving` flag and first installed a member layout without base classes then replaced it with the full layout while questioning how it avoided inconsistencies
 * [today](https://github.com/microsoft/TypeScript/pull/65059#issuecomment-6535835030) **ahejlsberg** excluded class/interface types from isStringIndexSignatureOnlyType to avoid issues with indexed access simplification
 * [today](https://github.com/microsoft/TypeScript/pull/65059#issuecomment-6535839967) **ahejlsberg** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/65059#issuecomment-6535841362) **typescript-automation[bot]** reported build statuses and results links for CI jobs
 * [today](https://github.com/microsoft/TypeScript/pull/65059#issuecomment-6536314622) **typescript-automation[bot]** notified that DT test results were ready and unchanged
 * [today](https://github.com/microsoft/TypeScript/pull/65059#issuecomment-6536427374) **typescript-automation[bot]** provided tsc user test results and indicated everything looked good
 * [today](https://github.com/microsoft/TypeScript/pull/65059#issuecomment-6536525512) **typescript-automation[bot]** provided performance run results to @ahejlsberg
 * [today](https://github.com/microsoft/TypeScript/pull/65059#issuecomment-6537056606) **typescript-automation[bot]** reported successful tsc comparison between baseline and pr on the top 400 repos
 * [later](https://github.com/microsoft/TypeScript/pull/65059#issuecomment-6544531196) **ahejlsberg** said "No effects on performance and all tests are clear. I think this one is good to go."

### [PR microsoft/TypeScript#65060](https://github.com/microsoft/TypeScript/pull/65060) (Closed, `Author: Team`, `For Uncommitted Bug`, **RyanCavanaugh**)

**Parenthesize new\-expression callees when needed**

*Ensure that new-expression callees are parenthesized when required to maintain valid syntax and semantics.*

 * created by **RyanCavanaugh**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **RyanCavanaugh**
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#65061](https://github.com/microsoft/TypeScript/pull/65061) (Open, `Domain: Performance`, `For Uncommitted Bug`)

**Speed up \`removeSubtypes\` by looking up each target's key property type once per key property name**

*Optimize removeSubtypes to improve performance by caching each key property type per property name.*

 * created by **Andarist**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/65061#issuecomment-6529718523) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/65061#issuecomment-6529720917) **typescript-automation[bot]** indicated that the performance test job had started and provided links to build status and results
 * **jakebailey** added label `Domain: Performance`
 * [today](https://github.com/microsoft/TypeScript/pull/65061#issuecomment-6530887553) **typescript-automation[bot]** provided the results of the requested performance run
 * [later](https://github.com/microsoft/TypeScript/pull/65061#issuecomment-6541174030) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."

### [PR microsoft/TypeScript#65062](https://github.com/microsoft/TypeScript/pull/65062) (Open, `For Backlog Bug`)

**Preserve single\-line emit hints for nodes returned by the API**

*Extend the TypeScript API to serialize and preserve single-line emit hints in node flags for accurate single-line printing.*

 * created by **1-DARK**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [PR microsoft/TypeScript#65063](https://github.com/microsoft/TypeScript/pull/65063) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**Fix AST optionality**

*Update AST node definitions to make type-related properties and tokens optional or non-null as needed.*

 * created by **andrewbranch**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript/pull/65063#issuecomment-6532131676) **RyanCavanaugh** questioned why IndexSignatureDeclaration.type being optional is the only syntax error in the list
 * [today](https://github.com/microsoft/TypeScript/pull/65063#issuecomment-6532745343) **andrewbranch** clarified that the error is a grammar error and proposed either keeping the node optional or making it a parse error with a missing identifier

### [PR microsoft/TypeScript#65064](https://github.com/microsoft/TypeScript/pull/65064) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**\[experiment\] fully order independent type checking**

*Make the type checker fully order independent by replacing ID-based caching with content-based memos and order-variant tests.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6532748831) **jakebailey** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6532750796) **typescript-automation[bot]** reported started build jobs with statuses and links
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6533468761) **typescript-automation[bot]** reported DT test failures for the d3-selection package
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6533497319) **typescript-automation[bot]** reported user test results with new TypeScript errors and requested review
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6533969647) **typescript-automation[bot]** provided the requested performance run results
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6534283900) **jakebailey** said "Well, that's a little bleak."

### [PR microsoft/TypeScript#65065](https://github.com/microsoft/TypeScript/pull/65065) (Closed, `For Uncommitted Bug`)

**fix\(65052\): keep inherited member order from the base type**

*Preserve base-type declaration order for inherited interface members to correct variance assignment errors in empty subtypes.*

 * created by **timurzvural**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [PR microsoft/TypeScript#65066](https://github.com/microsoft/TypeScript/pull/65066) (Closed, `Domain: Performance`, `For Uncommitted Bug`)

**Add getSymbolDocumentations and getMembersOfType for API surface extraction**

*Add getSymbolDocumentations and getMembersOfType to batch-fetch JSDoc documentation and filtered type members in one request for efficient API surface extraction.*

 * created by **timurzvural**
 * (today) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#65067](https://github.com/microsoft/TypeScript/pull/65067) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Avoid allocating a bool for cached computed names**

*Replace the allocated boolean pointer for cached computed names with a tristate to eliminate unnecessary allocation.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * **jakebailey** added label `Domain: Performance`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#65068](https://github.com/microsoft/TypeScript/issues/65068) (Open)

**\[ServerErrors\]\[TypeScript\] main**

*The main TypeScript error-deltas pipeline run on 300 popular repositories reported numerous timeouts and failures, completing only 139 successful analyses.*

 * created by **typescript-automation[bot]**
 * [today](https://github.com/microsoft/TypeScript/issues/65068#issuecomment-6536542206) **typescript-automation[bot]** reported a panic in handling a textDocument/completion request caused by a path containing a URL query or fragment
 * [today](https://github.com/microsoft/TypeScript/issues/65068#issuecomment-6536542857) **typescript-automation[bot]** reported a panic error indicating path must not contain a URL query or fragment along with a stack trace
 * [today](https://github.com/microsoft/TypeScript/issues/65068#issuecomment-6536543540) **typescript-automation[bot]** reported a panic handling request textDocument/completion due to path containing a URL query or fragment and included a stack trace
 * [today](https://github.com/microsoft/TypeScript/issues/65068#issuecomment-6536544192) **typescript-automation[bot]** reported a server connection closed prematurely error for floating-ui/floating-ui and included logs, last requests, and repro steps

### [Issue microsoft/TypeScript#65069](https://github.com/microsoft/TypeScript/issues/65069) (Open)

**7\.1: array\-destructured parameter with a \`= \[\]\` default loses its contextual type \(TS7031\)**

*In TypeScript 7.1, array-destructured parameters with a default empty array lose their contextual tuple types, causing implicit any errors.*

 * created by **timurzvural**

### [PR microsoft/TypeScript#65070](https://github.com/microsoft/TypeScript/pull/65070) (Open, `For Backlog Bug`)

**fix\(65069\): preserve contextual types for array\-destructured parameter defaults**

*Ensure that array-destructured function parameters with default empty arrays retain their contextual tuple types by only padding missing elements when no contextual type is present.*

 * created by **timurzvural**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [Issue microsoft/TypeScript#65071](https://github.com/microsoft/TypeScript/issues/65071) (Open)

**API: \`closeProjects\` then \`openFiles\` crashes tsgo \(nil ChangeIf in \`acquireConfigForFile\`\)**

*Invoking closeProjects then openFiles in the TypeScript sync API causes a nil pointer dereference in acquireConfigForFile’s ChangeIf.*

 * created by **timurzvural**

### [PR microsoft/TypeScript#65072](https://github.com/microsoft/TypeScript/pull/65072) (Closed, `For Uncommitted Bug`)

**fix\(65071\): resurrect dirty\.SyncMap entries after Delete in LoadOrStore**

*Resurrect deleted dirty.SyncMap entries in LoadOrStore to prevent nil returns after tombstones.*

 * created by **timurzvural**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [PR microsoft/TypeScript#65073](https://github.com/microsoft/TypeScript/pull/65073) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Compute CommonJSModuleIndicator in the parser**

*Move CommonJSModuleIndicator computation from the binding phase into the parser to enable earlier, consistent file reuse without race conditions.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/65073#issuecomment-6540223174) **jakebailey** said "Uh. Interesting"

### [PR microsoft/TypeScript#65074](https://github.com/microsoft/TypeScript/pull/65074) (Closed, `For Uncommitted Bug`)

**Temporary validation branch \(draft; will be closed\)**

*A draft pull request using a temporary validation branch tests repository automation and will be closed without merging.*

 * created by **bribes**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (later) **bribes** closed the issue
 * (later) **typescript-automation[bot]** added labels `For Backlog Bug`, `For Uncommitted Bug`, `For Backlog Bug`, `For Uncommitted Bug`, and removed labels `For Uncommitted Bug`, `For Backlog Bug`, `For Uncommitted Bug`, `For Backlog Bug`

### [Issue microsoft/TypeScript#65075](https://github.com/microsoft/TypeScript/issues/65075) (Open, `Duplicate`)

**typescript/ast/scanner: scan\(\) never advances past \`\#\` not followed by an identifier start \(7\.1\.0\-beta\)**

*TypeScript 7.1.0-beta’s AST scanner scan method fails to advance past '#' not followed by an identifier, causing infinite loops.*

 * created by **ilterugur**
 * [later](https://github.com/microsoft/TypeScript/issues/65075#issuecomment-6544425849) **MartinJohns** said "Duplicate of #64490."

