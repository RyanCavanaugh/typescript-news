# Report for 2026-09-21 (Monday, September 21st, 2026)

22 different users commented on 50 different issues.

## Recommended Actions

 * Response Recommended
    * @typescript-automation[bot] asked to retry tests after PR changed in [microsoft/TypeScript#63926](https://github.com/microsoft/TypeScript/pull/63926#issuecomment-5764773253)
    * @johnnyreilly provided repro steps as requested in [microsoft/TypeScript#64204](https://github.com/microsoft/TypeScript/pull/64204#issuecomment-5771872346)
    * @typescript-automation[bot] reported regression build failures and requested review in [microsoft/TypeScript#64372](https://github.com/microsoft/TypeScript/pull/64372#issuecomment-5766063918)
    * @typescript-automation asked to review the tsc comparison results and build failures in [microsoft/TypeScript#64375](https://github.com/microsoft/TypeScript/pull/64375#issuecomment-5766455684)
    * @typescript-automation[bot] asked to retry tests after PR changed in [microsoft/TypeScript#64376](https://github.com/microsoft/TypeScript/pull/64376#issuecomment-5765207254)
    * @Abdellox asked for steps to reproduce, expected vs actual behavior, and environment details in [microsoft/TypeScript#64387](https://github.com/microsoft/TypeScript/issues/64387#issuecomment-5778059891)

## Activity Summary

### [Issue microsoft/TypeScript#27070](https://github.com/microsoft/TypeScript/issues/27070) (Open, `Suggestion`, `In Discussion`, `Domain: LS: Refactorings`)

**Inline function refactoring**

*Add a refactoring feature to inline selected functions into their call sites and optionally delete their definitions.*

 * [2.4 years ago](https://github.com/microsoft/TypeScript/issues/27070#issuecomment-2084441844) **sduzair** expressed excitement and mentioned the resource's usefulness for understanding nested functions and refactoring towards clean code abstractions
 * [2.3 years ago](https://github.com/microsoft/TypeScript/issues/27070#issuecomment-2109748591) **ukslim** noted that inline constant expressions are already supported via the inline variable command and requested inline function refactoring
 * [2.3 years ago](https://github.com/microsoft/TypeScript/issues/27070#issuecomment-2109761101) **ukslim** suggested refusing inline function refactoring on variable naming conflicts and providing a clear error message naming the conflict
 * [today](https://github.com/microsoft/TypeScript/issues/27070#issuecomment-5764662328) **princeeze** bumped the issue and suggested the refactor as a basic IDE feature

### [Issue microsoft/TypeScript#36299](https://github.com/microsoft/TypeScript/issues/36299) (Closed, `Bug`, `Domain: lib.d.ts`)

**Typo in \`String\#match\` \(lib\.es2015\.symbol\.wellknown\)**

*A misplaced parameter description appears in the String#match declaration of lib.es2015.symbol.wellknown.*

 * **RyanCavanaugh** added label `Domain: lib.d.ts`
 * [6.5 years ago](https://github.com/microsoft/TypeScript/issues/36299#issuecomment-587653436) **G-Rath** reported a similar typo in the RegExp interface comments in es5.lib and compared it to the #match method comment
 * [6.5 years ago](https://github.com/microsoft/TypeScript/issues/36299#issuecomment-595733648) **sebmjoll** pointed out that the replace() doc comment was misleading about occurrence replacement behavior with string versus regex
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#57564](https://github.com/microsoft/TypeScript/issues/57564) (Closed, `Bug`, `Won't Fix`, `Needs More Info`, `Has Repro`, `Domain: Something Else`)

**Error not issued when global type is an alias of an object type literal**

*Custom global Array<T> alias as object literal prevents expected type errors for T[] satisfy checks.*

 * (3 days ago) **RyanCavanaugh** added labels `Needs Human Review`, `Needs More Info`
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/57564#issuecomment-5742046277) **rotu** asked where TS2317 was appearing in the Workbench linked in the writeup
 * (today) **RyanCavanaugh** added label `Won't Fix`, and removed label `Needs Human Review`
 * [today](https://github.com/microsoft/TypeScript/issues/57564#issuecomment-5767104327) **RyanCavanaugh** apologized for earlier noise, noted the error was rare, suggested documenting invariants for noLib if more users encountered it, and warned that global lib changes were unpredictable
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#59777](https://github.com/microsoft/TypeScript/issues/59777) (Open, `Bug`, `Help Wanted`, `Domain: Binder`)

**Multi\-line top\-level \`await\` causes duplicate declaration error**

*A multi-line top-level await expression triggers a false duplicate identifier error on the following export class declaration.*

 * (2 years ago) **RyanCavanaugh** added labels `Help Wanted`, `Domain: Binder`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/59777#issuecomment-5766407033) **joshuablac** investigated the duplicate identifier error in TypeScript 6.0.3, traced it to a misalignment in reparseTopLevelAwait, and noted that TypeScript 7 fixes the issue

### [PR microsoft/TypeScript#63926](https://github.com/microsoft/TypeScript/pull/63926) (Closed, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Negated Types**

*Add support for a 'not T' negated type operator with canonical simplification rules and enhanced control flow handling*

 * [4 days ago](https://github.com/microsoft/TypeScript/pull/63926#issuecomment-5720818089) **typescript-automation[bot]** reported that the test top1000 build jobs had started and that it would update status as they complete
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/63926#issuecomment-5721053286) **jakebailey** fixed the user test runner using an old version of node and reran tests
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/63926#issuecomment-5721054932) **typescript-automation[bot]** reported that the test top1000 job started and indicated the comment will be updated with build results
 * [today](https://github.com/microsoft/TypeScript/pull/63926#issuecomment-5764772053) **weswigham** said "@typescript-bot test top1000 because it looks like go install failed on a worker :("
 * [today](https://github.com/microsoft/TypeScript/pull/63926#issuecomment-5764773253) **typescript-automation[bot]** said "Hey @weswigham, this PR changed while I was preparing the test run. Please try again."
 * [today](https://github.com/microsoft/TypeScript/pull/63926#issuecomment-5764823209) **jakebailey** said "No it didn't, ha, I'll look into that"
 * (today) **weswigham** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/63926#issuecomment-5765034985) **weswigham** said "Superseded by https://github.com/microsoft/TypeScript/pull/64375, since I can only stack PRs actually on the repo, and not from forks."

### [PR microsoft/TypeScript#63934](https://github.com/microsoft/TypeScript/pull/63934) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Optimize LSP discriminated union decoding**

*Optimize LSP discriminated union decoding by bypassing buffering and using streaming when the discriminator is first for faster performance.*

 * (1 month ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64158](https://github.com/microsoft/TypeScript/pull/64158) (Open, `Author: Team`, `For Uncommitted Bug`, **iisaduan**)

**Build Orchestrator API **

*Implement a BuildOrchestrator API to programmatically build, clean, and manage project references in TypeScript 7.1 without watch mode.*

 * [4 days ago](https://github.com/microsoft/TypeScript/pull/64158#issuecomment-5723381271) **andrewbranch** asked which incremental-specific Program APIs were needed beyond altered construction/emit behavior and whether they used emitBuildInfo(), getSemanticDiagnosticsOfNextAffectedFile(), emitNextAffectedFile(), or others
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/64158#issuecomment-5729268673) **dragomirtitian** explained their usage of the incremental program APIs and workflow, including creating an incremental compiler host, caching ASTs, invoking diagnostics, and emitting changed files
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/64158#issuecomment-5732995165) **andrewbranch** described how declaration file AST caching now works automatically via strategic program snapshots, referenced Jake’s prototype commit, and mentioned developing a snapshot-backed incremental program prototype for future testing
 * [today](https://github.com/microsoft/TypeScript/pull/64158#issuecomment-5766275697) **dragomirtitian** acknowledged automatic parse cache behavior, noted uncertainty about its reliability, and expressed eagerness to try the upcoming prototype

### [PR microsoft/TypeScript#64160](https://github.com/microsoft/TypeScript/pull/64160) (Open, `For Uncommitted Bug`, **jakebailey**, **Copilot**)

**Exclude top\-level imports from document symbols**

*Modify LSP documentSymbol results to omit top-level import and import-equals declarations, aligning with VS Code Outline behavior.*

 * **Copilot** assigned to **jakebailey**
 * (2 weeks ago) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64160#issuecomment-5765997553) **jakebailey** said "Marking as ready for review, but we need to make sure this doesn't regress VS. @joj @navya9singh for awareness."

### [PR microsoft/TypeScript#64204](https://github.com/microsoft/TypeScript/pull/64204) (Closed, `Author: Team`, `For Milestone Bug`, **andrewbranch**)

**Replace \`api\.updateSnapshot\`**

*Refactor snapshot API by removing api.updateSnapshot and introducing createSnapshot, getCurrentLanguageServerSnapshot, and snapshot.update operations.*

 * [4 days ago](https://github.com/microsoft/TypeScript/pull/64204#issuecomment-5721629954) **andrewbranch** described the existing test coverage from sibling snapshots, auto-import snapshots, and temporary file update snapshots that have reinforced immutability guarantees
 * (4 days ago) **andrewbranch** closed the issue
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/64204#issuecomment-5741152262) **johnnyreilly** migrated ts-loader branch to the new API and reported a potential regression
 * [today](https://github.com/microsoft/TypeScript/pull/64204#issuecomment-5764737200) **andrewbranch** explained that ts-loader used `App.vue.ts` for openFiles and asked the recipient to double-check their implementation
 * [today](https://github.com/microsoft/TypeScript/pull/64204#issuecomment-5765834968) **johnnyreilly** described partial solution with changes, confirmed and fixed a bug on their side, identified a second Windows-only repro panic scenario, corrected their original repro assumptions, and explained their workaround
 * [today](https://github.com/microsoft/TypeScript/pull/64204#issuecomment-5766425880) **andrewbranch** said "Hm, I've investigated, but I can't reproduce that. Can you get Claude to generate a contained repro, or even repro instructions tied to a specific commit of your PR?"
 * [today](https://github.com/microsoft/TypeScript/pull/64204#issuecomment-5771867307) **johnnyreilly** wondered if the issue only surfaced on Windows, noted that Claude had reproduced it, and linked the Windows failure
 * [today](https://github.com/microsoft/TypeScript/pull/64204#issuecomment-5771872346) **johnnyreilly** provided a minimal ts-loader/webpack-free repro with instructions that reproduces the issue only on Windows

### [PR microsoft/TypeScript#64220](https://github.com/microsoft/TypeScript/pull/64220) (Open, `For Milestone Bug`, **johnfav03**)

**Schedule tsc \-b projects by dependency depth to reduce builder idle time on upstream projects**

*Sort topologically built TypeScript projects by dependency depth rather than references-first to reduce builder idle time and speed up large monorepo builds.*

 * [6 days ago](https://github.com/microsoft/TypeScript/pull/64220#issuecomment-5685830448) **typescript-automation[bot]** reported build jobs starting and provided links to status and results
 * [6 days ago](https://github.com/microsoft/TypeScript/pull/64220#issuecomment-5686328009) **typescript-automation[bot]** posted performance run results for tsc comparing baseline to pr
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64220#issuecomment-5749572773) **Freakazo** tested the branch on a large monorepo and observed performance gains (median 38.24s to 28.39s) with increased memory usage (~5.4GB to ~6.9GB), and noted most benchmarks don’t use the -b flag
 * [today](https://github.com/microsoft/TypeScript/pull/64220#issuecomment-5766071230) **jakebailey** clarified that only the xstate benchmark used -b, where the optimization had the biggest impact

### [Issue microsoft/TypeScript#64270](https://github.com/microsoft/TypeScript/issues/64270) (Closed)

**Auto\-import completions are not shown inside named imports with TypeScript 7 / tsgo**

*Named import auto-completions are missing in VS Code with TypeScript 7’s native tsgo language server, though they work in TypeScript 6.*

 * created by **devvitor67**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#64279](https://github.com/microsoft/TypeScript/issues/64279) (Closed, **jakebailey**, **Copilot**)

**JSDoc \`@type\` on a function: the type in a type predicate is never checked \(unused \`@import\` reported, missing names not reported\)**

*TypeScript 7.0.2+ erroneously flags imported types used solely in JSDoc @type function type predicates as unused, causing TS6196 errors.*

 * [4 days ago](https://github.com/microsoft/TypeScript/issues/64279#issuecomment-5720619357) **ljharb** said "also, the types for a function expression vs declaration shouldn't behave differently - they're basically the same thing."
 * [4 days ago](https://github.com/microsoft/TypeScript/issues/64279#issuecomment-5720649019) **jakebailey** said "I don't follow; do you have an example where this is broken?"
 * [4 days ago](https://github.com/microsoft/TypeScript/issues/64279#issuecomment-5720674636) **ljharb** clarified that he was replying to a previous comment and asserted that every function should accept @type regardless of declaration or expression
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64303](https://github.com/microsoft/TypeScript/pull/64303) (Closed, `For Uncommitted Bug`, **jakebailey**, **Copilot**)

**Check JSDoc function type predicates**

*Fully validate JSDoc @type function predicate signatures to correctly resolve predicate types and imports.*

 * **Copilot** assigned to **jakebailey**
 * (5 days ago) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64303#issuecomment-5769316746) **jakebailey** requested a cherry-pick to release-7.0 despite anticipating failure
 * [today](https://github.com/microsoft/TypeScript/pull/64303#issuecomment-5769317416) **typescript-automation[bot]** reported that cherry-pick to release-7.0 failed because PR #64303 had not been merged
 * (today) **jakebailey** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/64303#issuecomment-5769642935) **jakebailey** said "@typescript-bot cherry-pick this to release-7.0"
 * [today](https://github.com/microsoft/TypeScript/pull/64303#issuecomment-5769643585) **typescript-automation[bot]** reported build jobs starting and status updates
 * [today](https://github.com/microsoft/TypeScript/pull/64303#issuecomment-5769664827) **typescript-automation[bot]** said "Hey, @jakebailey! I've created #64382 for you."

### [PR microsoft/TypeScript#64323](https://github.com/microsoft/TypeScript/pull/64323) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Remove implicit floating\-point FMAs**

*A lint rule scans Go code for implicit floating-point FMAs on ARM to avoid unexpected behavior from Go 1.27.*

 * (3 days ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/64323#issuecomment-5735568380) **jakebailey** noted that no built-in solution existed, suggested using GOCOMPILERDEBUG but considered a full OS+arch matrix a waste, and considered removing the lint rule
 * [today](https://github.com/microsoft/TypeScript/pull/64323#issuecomment-5765873721) **jakebailey** said "I killed the lint rule. It was too hard to get right. I'll leave that to some experts somewhere else."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64326](https://github.com/microsoft/TypeScript/pull/64326) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**\[api\] Make optional properties of project references optional**

*Ensure optional project reference properties are correctly marked as optional in the API.*

 * (3 days ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#64331](https://github.com/microsoft/TypeScript/pull/64331) (Closed, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Make all the codegen we do incremental**

*Add incremental caching to all repository code generation tasks to reduce generate subtasks runtime by up to 80%.*

 * (3 days ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **weswigham**
 * [today](https://github.com/microsoft/TypeScript/pull/64331#issuecomment-5765489874) **weswigham** pushed changes to move code generation into scripts, reported performance improvements, and re-requested review
 * [today](https://github.com/microsoft/TypeScript/pull/64331#issuecomment-5766745226) **jakebailey** suggested improving logging to display command details and package listings instead of generic messages
 * [today](https://github.com/microsoft/TypeScript/pull/64331#issuecomment-5766922572) **weswigham** said "That's pretty fair - the logging got simplified as I merged helpers from the first version and it got a wee bit too simple."
 * [today](https://github.com/microsoft/TypeScript/pull/64331#issuecomment-5767488842) **weswigham** said "@jakebailey There ya go, output of the cache layer's a bit more verbose."
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript#64337](https://github.com/microsoft/TypeScript/pull/64337) (Closed, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Stop including API benchmarks in validate**

*Run API benchmarks in a separate CI test subtask instead of in the main validate suite, mirroring go benchmarks.*

 * (3 days ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **weswigham**
 * (today) **weswigham** closed the issue

### [Issue microsoft/TypeScript#64351](https://github.com/microsoft/TypeScript/issues/64351) (Open)

**tsc \-\-watch never recompiles on macOS since 7\.1\.0\-dev\.20260811\.1**

*On macOS with TypeScript 7.1.0-dev.20260811.1 and later nightly builds, tsc --watch stops detecting file changes and never recompiles.*

 * created by **leonidaz**
 * [later](https://github.com/microsoft/TypeScript/issues/64351#issuecomment-5772532438) **jakebailey** said "Can you try #64210 just to see?"

### [PR microsoft/TypeScript#64352](https://github.com/microsoft/TypeScript/pull/64352) (Closed, `For Backlog Bug`)

**Remove misplaced parameter description from RegExp\#source JSDoc**

*Remove the misplaced 'regExp' parameter description from the read-only RegExp.source JSDoc in lib.es5.d.ts*

 * created by **hikmetba-bit**
 * (2 days ago) **typescript-automation[bot]** added labels `For Backlog Bug`, `For Backlog Bug`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#64355](https://github.com/microsoft/TypeScript/issues/64355) (Closed, `Working as Intended`)

**TypeScript 7 VS Code extension never activates for workspaces where only content\-mapped files are opened**

*The TypeScript 7 VS Code extension never activates for content-mapped file types unless a native TypeScript or JavaScript file is opened.*

 * created by **leonidaz**
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/64355#issuecomment-5746828846) **leonidaz** described that activation alone was insufficient and suggested pairing activation with project loading or syncing already-open mapped documents
 * [today](https://github.com/microsoft/TypeScript/issues/64355#issuecomment-5766497124) **andrewbranch** said "Have you read the “LSP Activation” section of https://github.com/microsoft/typescript-go/pull/4712? I think everything you've described sounds like it's working as intended."
 * **andrewbranch** added label `Working as Intended`
 * [today](https://github.com/microsoft/TypeScript/issues/64355#issuecomment-5769590507) **leonidaz** clarified that their own patching removed the activation code and that activation only occurred when opening a .ts file, explaining the confusion
 * (today) **leonidaz** closed the issue

### [PR microsoft/TypeScript#64357](https://github.com/microsoft/TypeScript/pull/64357) (Closed, `For Uncommitted Bug`)

**Fix import statement completion filtering in tsgo**

*Use the generated import statement as filterText for tsgo import completions to fix filtering inside named imports.*

 * created by **yksr-melt**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/64357#issuecomment-5747866962) **yksr-melt** said "@microsoft-github-policy-service agree"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64360](https://github.com/microsoft/TypeScript/pull/64360) (Open, `For Backlog Bug`)

**Fix union overload signature ordering instability**

*Generate exact-arity variants for union signatures with optional parameters to ensure stable overload resolution without ad-hoc sorting.*

 * (yesterday) **typescript-automation[bot]** added labels `For Backlog Bug`, `For Backlog Bug`
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64360#issuecomment-5748296015) **adilalperenciftci** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript/pull/64360#issuecomment-5766137973) **jakebailey** said "This seems a bit too ad-hoc and out of place for the kind of thing we normally do. It is suspicious that nothing else changed, either, and that it's purely additive?"
 * [today](https://github.com/microsoft/TypeScript/pull/64360#issuecomment-5767834549) **adilalperenciftci** dropped the post-sorting approach and replaced it with expanding optional-parameter signatures into exact-arity variants in getUnionSignatures so findMatchingSignatures matches without extra sorting

### [PR microsoft/TypeScript#64365](https://github.com/microsoft/TypeScript/pull/64365) (Closed, `For Uncommitted Bug`)

**fix\(vscode\-typescript\): activate for content\-mapped\-only workspaces**

*Permit VS Code TypeScript extension to activate for content-mapped-only workspaces by adding workspace activation events and syncing open files.*

 * created by **snhsish**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64365#issuecomment-5752493767) **snhsish** said "@microsoft-github-policy-service agree"
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#64366](https://github.com/microsoft/TypeScript/pull/64366) (Open, `For Uncommitted Bug`)

**Watch project directories that are close to the filesystem root**

*tsc --watch doesn’t detect changes in projects near the filesystem root because it ignores directories with under five path components.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/64366#issuecomment-5753121877) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64366#issuecomment-5753293920) **Generalsimus** quoted the policy service directive for Microsoft
 * [today](https://github.com/microsoft/TypeScript/pull/64366#issuecomment-5759505773) **Generalsimus** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript/pull/64366#issuecomment-5765888929) **jakebailey** expressed concern about lack of testing in a real codebase and asked whether the behavior derived from a Strada rule, requesting a reference to that code

### [PR microsoft/TypeScript#64367](https://github.com/microsoft/TypeScript/pull/64367) (Closed, `For Uncommitted Bug`, `dependencies`, `github_actions`)

**Bump the github\-actions group across 1 directory with 4 updates**

*Bump codecov/codecov-action to v7.1.1 and github/codeql-action init, analyze, and upload-sarif to v4.38.1 in the repository root*

 * (yesterday) **dependabot[bot]** added labels `dependencies`, `github_actions`
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#64370](https://github.com/microsoft/TypeScript/issues/64370) (Open, `Won't Fix`)

**Native compiler \(tsgo\) aborts with "fatal error: stack overflow" on deeply nested expressions**

*tsgo compiler crashes with a fatal stack overflow when parsing extremely deeply nested parentheses, brackets, or type arguments due to unbounded parser recursion.*

 * created by **kajaaz**
 * [today](https://github.com/microsoft/TypeScript/issues/64370#issuecomment-5763747721) **jakebailey** described that crash safety is documented on the TypeScript security page, expressed desire to improve handling without setting arbitrary limits, and suggested that the Zorya tool isn’t threat-model aware
 * [today](https://github.com/microsoft/TypeScript/issues/64370#issuecomment-5768184242) **RyanCavanaugh** marked the PR as Won't Fix and closed it, noting the invariant doesn't exist and the proposed fix was overly complex
 * **RyanCavanaugh** added label `Won't Fix`
 * [later](https://github.com/microsoft/TypeScript/issues/64370#issuecomment-5772918346) **kajaaz** said "Hi @jakebailey @RyanCavanaugh, ok I understand, this makes sense. Thank you for your time"

### [PR microsoft/TypeScript#64371](https://github.com/microsoft/TypeScript/pull/64371) (Closed, `For Uncommitted Bug`)

**parser: bound recursion depth to avoid stack overflow on deeply nested input**

*Bound parser recursion with a 40000-depth limit and new TS1700 diagnostic to prevent stack overflows on deeply nested input.*

 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64371#issuecomment-5762820056) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [today](https://github.com/microsoft/TypeScript/pull/64371#issuecomment-5763313376) **kajaaz** said "@microsoft-github-policy-service agree company="Ledger""
 * [today](https://github.com/microsoft/TypeScript/pull/64371#issuecomment-5763762546) **jakebailey** rejected setting an arbitrary maximum as a fix and noted upcoming parser restructuring changes to reduce recursion
 * [today](https://github.com/microsoft/TypeScript/pull/64371#issuecomment-5768190783) **RyanCavanaugh** said "Closing per linked discussion; this PR attempts to enforce an invariant that is documented as explicitly not existing."
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#64372](https://github.com/microsoft/TypeScript/pull/64372) (Open, `Author: Team`, `For Milestone Bug`, **ahejlsberg**)

**Restore idempotency to \`resolveObjectTypeMembers\`**

*Restore resolveObjectTypeMembers idempotency by preventing base type arguments from accessing partially resolved class or interface members*

 * [today](https://github.com/microsoft/TypeScript/pull/64372#issuecomment-5763107668) **typescript-automation[bot]** reported CI build statuses for multiple commands and noted an access denied error for the 'run dt' pipeline
 * [today](https://github.com/microsoft/TypeScript/pull/64372#issuecomment-5763296299) **jakebailey** said "I fixed the DT error (forgot to grant a perm), but note that DT doesn't check 7.0 or 7.1 quite yet."
 * [today](https://github.com/microsoft/TypeScript/pull/64372#issuecomment-5763474607) **typescript-automation[bot]** provided the requested performance run results with a comparison report
 * [today](https://github.com/microsoft/TypeScript/pull/64372#issuecomment-5765231233) **ahejlsberg** invoked typescript-bot to run tests
 * [today](https://github.com/microsoft/TypeScript/pull/64372#issuecomment-5765232314) **typescript-automation[bot]** reported CI job statuses and result links
 * [today](https://github.com/microsoft/TypeScript/pull/64372#issuecomment-5765261701) **ahejlsberg** said "Trying tests again..."
 * [today](https://github.com/microsoft/TypeScript/pull/64372#issuecomment-5765610733) **typescript-automation[bot]** reported test results comparing main to the pull request merge, noted two unrelated infrastructure failures, and confirmed that everything else looked good
 * [today](https://github.com/microsoft/TypeScript/pull/64372#issuecomment-5766063918) **typescript-automation[bot]** reported tsc comparison results for the top 400 repos and highlighted build failures in stablyai/orca

### [PR microsoft/TypeScript#64373](https://github.com/microsoft/TypeScript/pull/64373) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**Preserve snapshot identity across no\-op updates**

*Preserve snapshot identity across no-op updates to prevent unnecessary snapshot replacements.*

 * created by **andrewbranch**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#64374](https://github.com/microsoft/TypeScript/pull/64374) (Closed, `For Uncommitted Bug`, **andrewbranch**, **Copilot**)

**Return an API error when opened files cannot be loaded into a project**

*Ensure the API rejects attempts to open files not belonging to a project by returning an error instead of crashing.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **andrewbranch**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#64375](https://github.com/microsoft/TypeScript/pull/64375) (Open, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Negated Types**

*Add a 'not T' primitive type for TypeScript to represent negated types and preserve control-flow filtering.*

 * created by **weswigham**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **weswigham**
 * [today](https://github.com/microsoft/TypeScript/pull/64375#issuecomment-5765204612) **weswigham** said "@typescript-bot test top1000"
 * [today](https://github.com/microsoft/TypeScript/pull/64375#issuecomment-5765206104) **typescript-automation[bot]** reported starting the test top1000 job and provided links to status and results
 * [today](https://github.com/microsoft/TypeScript/pull/64375#issuecomment-5766455684) **typescript-automation[bot]** reported tsc comparison results across the top 1000 repos and noted build failures in alibaba/hooks and Companion-Inc/feynman

### [PR microsoft/TypeScript#64376](https://github.com/microsoft/TypeScript/pull/64376) (Open, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Negated Types: Change the meaning of \`{}\` to \`unknown & not null & not undefined\`**

*Redefine {} as non-null unknown instead of unknown, null, or undefined and enhance type-origin tracking for literal unions.*

 * created by **weswigham**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`, and assigned to **weswigham**
 * (today) **weswigham** closed the issue
 * (today) **weswigham** reopened the issue
 * [today](https://github.com/microsoft/TypeScript/pull/64376#issuecomment-5765206099) **weswigham** said "@typescript-bot test top1000"
 * [today](https://github.com/microsoft/TypeScript/pull/64376#issuecomment-5765207254) **typescript-automation[bot]** said "Hey @weswigham, this PR changed while I was preparing the test run. Please try again."

### [Issue microsoft/TypeScript#64378](https://github.com/microsoft/TypeScript/issues/64378) (Open)

**Performance: exponential check time as a chain of generic calls grows \(index signature in the inferred spec type\)**

*A string index signature in a generic command spec type causes exponentially slower TypeScript checks for long call chains.*

 * created by **alan-albuquerque**

### [PR microsoft/TypeScript#64379](https://github.com/microsoft/TypeScript/pull/64379) (Open, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Add the \`concurrency\` option to node tests**

*Introduce a concurrency option to Node tests to improve performance of filtered runs without impacting full-suite execution.*

 * created by **weswigham**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`, and assigned to **weswigham**

### [PR microsoft/TypeScript#64380](https://github.com/microsoft/TypeScript/pull/64380) (Open, `Author: Team`, `For Uncommitted Bug`, **RyanCavanaugh**)

**Revise 'restack' instructions in SKILL\.md**

*Revise the SKILL.md restack instructions to prevent them from being applied to unrelated operations.*

 * created by **RyanCavanaugh**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **RyanCavanaugh**

### [PR microsoft/TypeScript#64381](https://github.com/microsoft/TypeScript/pull/64381) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Move enum generator into tools scripts**

*Relocate the enum generator from the Herebyfile into the scripts directory alongside other TypeScript code generators.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#64382](https://github.com/microsoft/TypeScript/pull/64382) (Open, `For Uncommitted Bug`, **DanielRosenwasser**)

**🤖 Pick PR \#64303 \(Check JSDoc function type predicate\.\.\.\) into release\-7\.0**

*Cherry-pick PR #64303 for JSDoc function type predicate checks into the release-7.0 branch.*

 * created by **typescript-automation[bot]**
 * (today) **typescript-automation[bot]** added label `For Uncommitted Bug`, and assigned to **DanielRosenwasser**

### [PR microsoft/TypeScript#64383](https://github.com/microsoft/TypeScript/pull/64383) (Open, `For Uncommitted Bug`)

**LEGO: Pull request from lego/hb\_5378966c\-b857\-470a\-8675\-daebef4a6da1\_20260922092326260 to main**

*Merge localized LCL files from LEGO branch hb_5378966c-b857-470a-8675-daebef4a6da1_20260922092326260 into main.*

 * created by **csigs**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [Issue microsoft/TypeScript#64384](https://github.com/microsoft/TypeScript/issues/64384) (Open)

**Panic in \`TupleNormalizer\.normalize\` \(nil \`currentNode\`\) when declaration emit resolves an oversized tuple type under \`\-\-noCheck\`**

*Under --noCheck declaration emit, resolving an oversized recursive tuple type triggers a nil pointer dereference panic in TupleNormalizer.normalize.*

 * created by **YuanchengJiang**

### [PR microsoft/TypeScript#64385](https://github.com/microsoft/TypeScript/pull/64385) (Open, `For Uncommitted Bug`)

**Fix panic when declaration emit resolves an oversized tuple type**

*Declaration-only mode panics with a nil pointer when resolving tuple types exceeding size limits.*

 * created by **mohit-nayak**
 * (later) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/64385#issuecomment-5778789346) **jakebailey** suggested that the user had not run npm install recently
 * [later](https://github.com/microsoft/TypeScript/pull/64385#issuecomment-5779242206) **mohit-nayak** acknowledged that node_modules was stale, ran npm ci, confirmed formatting and tests passed, and updated the checklist

### [Issue microsoft/TypeScript#64386](https://github.com/microsoft/TypeScript/issues/64386) (Open)

**\`\-\-incremental\` retains stale diagnostics when augmenting a re\-exported interface**

*TypeScript incremental builds with a re-exported interface augmentation incorrectly retain stale diagnostics until the build cache is cleared.*

 * created by **infomiho**

### [Issue microsoft/TypeScript#64387](https://github.com/microsoft/TypeScript/issues/64387) (Open)

**SyncRpcChannel reads private \`stdout\.\_handle\.fd\`, breaking the sync API on non\-Node runtimes \(Bun\)**

*SyncRpcChannel’s reliance on Node’s private stdout._handle.fd breaks on non-Node runtimes like Bun, so the issue proposes using POSIX FIFOs for a public blocking file descriptor instead.*

 * created by **cairn-intern**
 * [later](https://github.com/microsoft/TypeScript/issues/64387#issuecomment-5778059891) **Abdellox** offered to help investigate and asked for steps to reproduce, expected vs actual behavior, and environment details

### [PR microsoft/TypeScript#64388](https://github.com/microsoft/TypeScript/pull/64388) (Open, `For Uncommitted Bug`)

**\[perf\]\[experiment\] fix\(64378\): add a cache to avoid repeated type arg inference**

*Adding a cache for type argument inference eliminates redundant computations and reduces check time from 91.6 seconds to 0.004 seconds.*

 * created by **a-tarasyuk**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

