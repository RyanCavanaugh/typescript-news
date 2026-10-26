# Report for 2026-10-22 (Thursday, October 22nd, 2026)

18 different users commented on 25 different issues.

## Recommended Actions

 * Response Recommended
    * @Pomax reported that super() return type contradicts ECMA-262 spec and persists in v7.0.2 in [microsoft/TypeScript#59959](https://github.com/microsoft/TypeScript/issues/59959#issuecomment-6347138506)
    * @gadcam asked for thoughts on the PR after clean test run in [microsoft/TypeScript#64729](https://github.com/microsoft/TypeScript/pull/64729#issuecomment-6363202221)
    * @tbknl noted missing library-only test coverage and requested a human review in [microsoft/TypeScript#64901](https://github.com/microsoft/TypeScript/pull/64901#issuecomment-6348455387)

## Activity Summary

### [Issue microsoft/TypeScript#59959](https://github.com/microsoft/TypeScript/issues/59959) (Open, `Suggestion`, `Awaiting More Feedback`)

**super\(\) typed as returning void**

*TypeScript incorrectly types super() in class constructors as void instead of the instance, preventing method chaining.*

 * **RyanCavanaugh** added label `Awaiting More Feedback`
 * [2 years ago](https://github.com/microsoft/TypeScript/issues/59959#issuecomment-2349307078) **RyanCavanaugh** asked why this is clearer than `super(); this.func();`
 * [2 years ago](https://github.com/microsoft/TypeScript/issues/59959#issuecomment-2349352190) **MartinJohns** said "Sounds like a duplicate of #37847 / #42298 to me."
 * [today](https://github.com/microsoft/TypeScript/issues/59959#issuecomment-6347138506) **Pomax** pointed out that super() returns the constructed instance per the ECMA-262 spec and that TypeScript's type checker incorrectly types it as void

### [Issue microsoft/TypeScript#62919](https://github.com/microsoft/TypeScript/issues/62919) (Closed, `Suggestion`, `Awaiting More Feedback`)

**Feature: Const\-literal typing for import\-attribute imports**

*Import attributes should support const-literal typing for JSON imports to preserve literal value types instead of general primitives.*

 * (41 weeks ago) **RyanCavanaugh** added labels `Suggestion`, `Awaiting More Feedback`
 * [39 weeks ago](https://github.com/microsoft/TypeScript/issues/62919#issuecomment-3776373053) **sinclairzx81** referenced related pull requests
 * [today](https://github.com/microsoft/TypeScript/issues/62919#issuecomment-6347275037) **sinclairzx81** closed the issue, noting that Content Mappers in 7.1 provide a better mechanism to derive types from remote content
 * (today) **sinclairzx81** closed the issue

### [Issue microsoft/TypeScript#64195](https://github.com/microsoft/TypeScript/issues/64195) (Closed, `Needs Investigation`, **johnfav03**)

**LSP: file contents are not re\-read when \`didChangeWatchedFiles\` reports \`Created\` \(type 1\) for a file already in the program**

*LSP server fails to reload existing files when a Created file watcher event occurs, leading to stale content.*

 * created by **shuto-masuda**
 * (5 weeks ago) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **johnfav03**
 * (today) **johnfav03** closed the issue

### [PR microsoft/TypeScript#64679](https://github.com/microsoft/TypeScript/pull/64679) (Open, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Add createFileSystemFromSnapshot\(oldSnapshot, extraFSLayer\)**

*Implement createFileSystemFromSnapshot to reapply a previous snapshot’s synthetic file system onto a new snapshot with optional layering.*

 * [3 days ago](https://github.com/microsoft/TypeScript/pull/64679#issuecomment-6279317955) **andrewbranch** suggested renaming the API to use snapshot.update({ fileSystem: ... }) with createFileSystemWithBase for layering synthetic file system updates
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/64679#issuecomment-6302584141) **weswigham** asked which additional data should be merged in a snapshot "rebase" and noted that reusing ASTs would require reworking program construction
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/64679#issuecomment-6303338637) **andrewbranch** described concerns about ambiguity in the rebase API's unspecified base snapshot and potential confusion when using it on non-LSP snapshots
 * [today](https://github.com/microsoft/TypeScript/pull/64679#issuecomment-6347271080) **weswigham** realized that the FS structure only reused the final state rather than replaying all intermediate snapshots and proposed renaming the API and updating the PR
 * [today](https://github.com/microsoft/TypeScript/pull/64679#issuecomment-6348197362) **weswigham** said "@andrewbranch does createFileSystemFromSnapshot like this work for you? Makes sense to me."

### [PR microsoft/TypeScript#64695](https://github.com/microsoft/TypeScript/pull/64695) (Open, `For Milestone Bug`, **ahejlsberg**)

**\[experiment\] Skip incompatible discriminants when inferring**

*Experimentally skip incompatible discriminant properties during TypeScript union type inference to reduce workload and validate via tests.*

 * [today](https://github.com/microsoft/TypeScript/pull/64695#issuecomment-6340156079) **typescript-automation[bot]** reported tsc user test results and confirmed everything looked good
 * [today](https://github.com/microsoft/TypeScript/pull/64695#issuecomment-6340173641) **typescript-automation[bot]** posted performance comparison results for the requested perf run
 * [today](https://github.com/microsoft/TypeScript/pull/64695#issuecomment-6341131824) **typescript-automation[bot]** reported that running the top 400 repos tsc comparison between baseline and pr succeeded without issues
 * [later](https://github.com/microsoft/TypeScript/pull/64695#issuecomment-6363499747) **Andarist** said "@jakebailey could u rerun perf tests here?"

### [PR microsoft/TypeScript#64729](https://github.com/microsoft/TypeScript/pull/64729) (Open, `For Milestone Bug`, **gabritto**)

**Dedupe identical object literal types before subtype reduction**

*Deduplicate identical object literal types before subtype reduction to prevent O(n²) performance blow-ups when type-checking large JSON arrays*

 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64729#issuecomment-6133846968) **typescript-automation[bot]** notified that the DT test results were ready and unchanged
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64729#issuecomment-6134012975) **typescript-automation[bot]** reported tsc user test results and confirmed everything looked good
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64729#issuecomment-6134415656) **typescript-automation[bot]** reported that running the top 400 repos tsc comparison between baseline and pr succeeded without issues
 * [later](https://github.com/microsoft/TypeScript/pull/64729#issuecomment-6363202221) **gadcam** said "@jakebailey The Oct 12 test run came back clean (perf neutral, DT / user tests / top400 unchanged). What do you think about this PR?"

### [PR microsoft/TypeScript#64901](https://github.com/microsoft/TypeScript/pull/64901) (Open, `For Backlog Bug`)

**fix: map constructor param type**

*Correct map constructor parameter type inference and align its overload definitions across collection and iterable libraries.*

 * created by **tbknl**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64901#issuecomment-6318429701) **tbknl** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript/pull/64901#issuecomment-6348455387) **tbknl** noted that global standard-library overload changes warranted human review due to lacking collection-only inference regression coverage and missing specific library-only tests

### [PR microsoft/TypeScript#64909](https://github.com/microsoft/TypeScript/pull/64909) (Closed, `Author: Team`, `For Uncommitted Bug`, **johnfav03**)

**Reload cached files for \`Created\` watch events**

*Ensure files replaced by atomic saves trigger cache invalidation on Created events to prevent stale diagnostics.*

 * (yesterday) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **johnfav03**
 * (today) **johnfav03** closed the issue

### [PR microsoft/TypeScript#64915](https://github.com/microsoft/TypeScript/pull/64915) (Closed, `Author: Team`, `For Uncommitted Bug`, **ahejlsberg**)

**Lazy member resolution for class and interface types**

*Add lazy member resolution to classes and interfaces using shared member layouts and improved tuple numeric and length sorting.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/64915#issuecomment-6328661469) **jakebailey** said "@typescript-bot perf test this faster"
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64915#issuecomment-6328662673) **typescript-automation[bot]** started the perf test job and provided status and result links
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64915#issuecomment-6329080526) **typescript-automation[bot]** posted the requested perf run results with detailed comparison metrics
 * [today](https://github.com/microsoft/TypeScript/pull/64915#issuecomment-6349241094) **ahejlsberg** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/64915#issuecomment-6349242907) **typescript-automation[bot]** reported CI build statuses for test jobs with links to their start and results pages
 * [today](https://github.com/microsoft/TypeScript/pull/64915#issuecomment-6349734505) **jakebailey** demonstrated a broken TypeScript case where property accesses report missing properties despite compiling on main
 * [today](https://github.com/microsoft/TypeScript/pull/64915#issuecomment-6349744108) **typescript-automation[bot]** notified that the results of running the DT tests were ready and unchanged
 * [today](https://github.com/microsoft/TypeScript/pull/64915#issuecomment-6349837889) **typescript-automation[bot]** reported requested performance run results for tsc including error, symbol, type, and memory usage metrics
 * [today](https://github.com/microsoft/TypeScript/pull/64915#issuecomment-6349850475) **typescript-automation[bot]** provided tsc user test results and indicated everything looked good
 * [today](https://github.com/microsoft/TypeScript/pull/64915#issuecomment-6350799211) **typescript-automation[bot]** reported TypeScript compilation results for the top 400 repositories comparing the baseline and the pull request, noting build failures and detailed errors for the reactive-resume project
 * [today](https://github.com/microsoft/TypeScript/pull/64915#issuecomment-6351388573) **jakebailey** said "Hm, that top test failure didn't appear in the other alternative PRs"
 * [today](https://github.com/microsoft/TypeScript/pull/64915#issuecomment-6351639387) **jakebailey** provided a minimized reproduction example in TypeScript
 * [later](https://github.com/microsoft/TypeScript/pull/64915#issuecomment-6366078775) **ahejlsberg** said "@typescript-bot test it"
 * [later](https://github.com/microsoft/TypeScript/pull/64915#issuecomment-6366080814) **typescript-automation[bot]** reported CI jobs status updates with links
 * [later](https://github.com/microsoft/TypeScript/pull/64915#issuecomment-6366566074) **typescript-automation[bot]** notified that DT test results were ready and unchanged
 * [later](https://github.com/microsoft/TypeScript/pull/64915#issuecomment-6366698444) **typescript-automation[bot]** provided tsc user test results and indicated everything looked good
 * [later](https://github.com/microsoft/TypeScript/pull/64915#issuecomment-6366727765) **typescript-automation[bot]** reported the performance run results including errors, symbols, types, and memory usage for baseline vs PR
 * [later](https://github.com/microsoft/TypeScript/pull/64915#issuecomment-6367670438) **typescript-automation[bot]** reported successful tsc comparison between baseline and pr on the top 400 repos
 * [later](https://github.com/microsoft/TypeScript/pull/64915#issuecomment-6367775820) **ahejlsberg** said "Latest commit uses layout properties to compute keyof T and discriminate contextual types. Should help defer more work."
 * [later](https://github.com/microsoft/TypeScript/pull/64915#issuecomment-6367780366) **ahejlsberg** said "@typescript-bot test it"
 * [later](https://github.com/microsoft/TypeScript/pull/64915#issuecomment-6367782328) **typescript-automation[bot]** posted a CI status update with tests started and results linked
 * [later](https://github.com/microsoft/TypeScript/pull/64915#issuecomment-6368274598) **typescript-automation[bot]** notified that the DT test results were ready and that everything looked the same
 * [later](https://github.com/microsoft/TypeScript/pull/64915#issuecomment-6368373714) **typescript-automation[bot]** provided tsc user test results and indicated everything looked good
 * [later](https://github.com/microsoft/TypeScript/pull/64915#issuecomment-6368409617) **typescript-automation[bot]** provided the requested performance run results
 * [later](https://github.com/microsoft/TypeScript/pull/64915#issuecomment-6368663386) **ahejlsberg** said "@typescript-bot perf test this faster"
 * [later](https://github.com/microsoft/TypeScript/pull/64915#issuecomment-6368665114) **typescript-automation[bot]** reported that performance test jobs started and provided status and results links
 * [later](https://github.com/microsoft/TypeScript/pull/64915#issuecomment-6368672452) **ahejlsberg** said "Ok, I think this one is good to go now."

### [PR microsoft/TypeScript#64926](https://github.com/microsoft/TypeScript/pull/64926) (Closed, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Add copilot instructions to avoid excessive change summaries**

*Add Copilot instructions to prevent generating overly long or excessive change summaries.*

 * created by **weswigham**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `Author: Team`, `For Uncommitted Bug`, and assigned to **weswigham**
 * (today) **weswigham** closed the issue

### [Issue microsoft/TypeScript#64927](https://github.com/microsoft/TypeScript/issues/64927) (Open)

**augmentExportEquals2 fixture has a duplicate @filename directive**

*A duplicate @filename directive in the augmentExportEquals2 fixture causes file3.ts to be overwritten and errors to be ignored, which the PR corrects.*

 * created by **mahesh-desu**

### [PR microsoft/TypeScript#64928](https://github.com/microsoft/TypeScript/pull/64928) (Open, `For Uncommitted Bug`)

**Reuse token lookup visitor across AST descent**

*Reuse a single NodeVisitor for each token lookup to reduce allocations and improve getTokenAtPosition performance.*

 * created by **Tom4ikss**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64928#issuecomment-6350288151) **Tom4ikss** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript/pull/64928#issuecomment-6350320210) **jakebailey** said "This is a microbenchmark but how did you decide to try and work on this?"
 * [today](https://github.com/microsoft/TypeScript/pull/64928#issuecomment-6350406819) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [today](https://github.com/microsoft/TypeScript/pull/64928#issuecomment-6350722523) **Tom4ikss** described experimenting with native API type queries in a build-time i18n plugin to reduce type analysis cost, isolated repeated visitor construction in a benchmark, and reported reduced allocations and faster microbenchmark lookups but no clear full-workload timing improvement

### [Issue microsoft/TypeScript#64929](https://github.com/microsoft/TypeScript/issues/64929) (Open)

**Native token lookup allocates a visitor on each AST descent step**

*astnav.getTokenAtPosition repeatedly allocates new NodeVisitor instances during AST descent, causing high allocations and performance overhead mitigated by reusing the visitor*

 * created by **Tom4ikss**

### [Issue microsoft/TypeScript#64930](https://github.com/microsoft/TypeScript/issues/64930) (Open)

**7\.1 regression: circular type alias accepts an assignment it should reject \(opposite of \#64891\)**

*TypeScript 7.1 regressively accepts circular type alias assignments that should trigger TS2322 errors.*

 * created by **Nabil372**

### [PR microsoft/TypeScript#64931](https://github.com/microsoft/TypeScript/pull/64931) (Open, `For Uncommitted Bug`)

**LS/API: align parameter JSDoc resolution with the classic services semantics**

*Align Go API's parameter JSDoc resolution with the classic compiler to fix inconsistent @param inheritance and tag retrieval*

 * created by **WinterYukky**
 * (today) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`

### [Issue microsoft/TypeScript#64932](https://github.com/microsoft/TypeScript/issues/64932) (Open)

**Allow content mappers emit diagnostics with different severity levels**

*Enable content mappers to emit diagnostics with varying severity levels, including warnings.*

 * created by **blt-r**

### [PR microsoft/TypeScript#64933](https://github.com/microsoft/TypeScript/pull/64933) (Open, `For Uncommitted Bug`)

**Fix: Improve error message for non\-module JSX files**

*Clarify that non-module scripts cannot use automatic JSX runtime and recommend export {} to convert them to modules.*

 * created by **Dipak-coder-06**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/64933#issuecomment-6361854501) **microsoft-github-policy-service[bot]** prompted the contributor to read and agree to the Contributor License Agreement by replying with a specific command

### [PR microsoft/TypeScript#64934](https://github.com/microsoft/TypeScript/pull/64934) (Open, `For Uncommitted Bug`)

**Skip discriminant lookups for unions that cannot be narrowed**

*Optimize union type checking by skipping discriminant lookups for unions that cannot be narrowed.*

 * created by **Andarist**
 * (later) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/64934#issuecomment-6363070994) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."

### [PR microsoft/TypeScript#64935](https://github.com/microsoft/TypeScript/pull/64935) (Open, `For Uncommitted Bug`)

**Don't measure type parameters as independent through circular variance lookups**

*Correct circular variance computation to disallow incompatible assignments between mutually recursive type aliases.*

 * created by **jasleenkaur-qed42**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/64935#issuecomment-6365722241) **microsoft-github-policy-service[bot]** prompted the user to review and agree to the Contributor License Agreement by replying with the appropriate command

### [PR microsoft/TypeScript#64936](https://github.com/microsoft/TypeScript/pull/64936) (Open, `For Backlog Bug`)

**Avoid rebuilding later LSP project references**

*Skip rebuilding project references in LSP when the opened file is already included, pruning redundant later candidates.*

 * created by **chengchuu**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/64936#issuecomment-6368320130) **chengchuu** said "@microsoft-github-policy-service agree"

