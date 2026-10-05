# Report for 2026-10-03 (Saturday, October 3rd, 2026)

7 different users commented on 13 different issues.

## Recommended Actions

 * Response Recommended
    * @im-alok74 asked @rictic, @gmoothart, and @Peeja to review in [microsoft/TypeScript#64480](https://github.com/microsoft/TypeScript/pull/64480#issuecomment-5978605461)

## Activity Summary

### [Issue microsoft/TypeScript#62954](https://github.com/microsoft/TypeScript/issues/62954) (Closed, `Suggestion`, `In Discussion`, `Experimentation Needed`)

**Explicit variance annotations for built\-in \.d\.ts files**

*Proposal to include explicit variance annotations in built-in .d.ts definitions to speed up TypeScript type checking.*

 * (38 weeks ago) **DanielRosenwasser** added labels `Suggestion`, `In Discussion`, `Experimentation Needed`
 * (today) **akaltar** closed the issue

### [Issue microsoft/TypeScript#63879](https://github.com/microsoft/TypeScript/issues/63879) (Open, `Suggestion`)

**feat\(contentmapper\): support whole\-symbol rename edit projection**

*Support safe whole-symbol rename projections in the Content Mapper protocol to correctly map renamed symbols between authored and generated code*

 * (5 weeks ago) **RyanCavanaugh** added label `Suggestion`, removed label `Needs Investigation`, and unassigned **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript/issues/63879#issuecomment-5971241226) **leonidaz** explained that TSRX syntax compiles to virtual TSX and that no printer can reconstruct the original formatting, illustrating the issue with code examples

### [PR microsoft/TypeScript#64469](https://github.com/microsoft/TypeScript/pull/64469) (Open, `For Uncommitted Bug`, **johnfav03**)

**Speed up first incremental rebuilds after shared dependency edits**

*Introduce a cached export-lookup index and parallel signature computations to accelerate first incremental rebuilds after shared dependency edits.*

 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64469#issuecomment-5847125871) **resure** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript/pull/64469#issuecomment-5969259018) **gwkline** provided independent performance benchmarks applying the PR’s checker changes to a large monorepo, reported byte-identical outputs, noted speedups and minor memory increase, described optional incremental changes, highlighted a merge conflict, and offered further tests with a public repro
 * [today](https://github.com/microsoft/TypeScript/pull/64469#issuecomment-5969338823) **gwkline** provided a link to their final implementation commit
 * **typescript-automation[bot]** assigned to **johnfav03**

### [PR microsoft/TypeScript#64480](https://github.com/microsoft/TypeScript/pull/64480) (Open, `For Backlog Bug`)

**Fix incorrect error location when a spread overrides an explicit property \(\#51376\)**

*Attribute type assignability errors to overriding spread expressions rather than the earlier explicit properties in object literals.*

 * (6 days ago) **typescript-automation[bot]** added labels `For Backlog Bug`, `For Backlog Bug`
 * [6 days ago](https://github.com/microsoft/TypeScript/pull/64480#issuecomment-5856112934) **im-alok74** said "@microsoft-github-policy-service agree"
 * [later](https://github.com/microsoft/TypeScript/pull/64480#issuecomment-5978605461) **im-alok74** asked @rictic, @gmoothart, and @Peeja to look at this

### [PR microsoft/TypeScript#64581](https://github.com/microsoft/TypeScript/pull/64581) (Open, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**Add content mapper output extensions**

*Add support for specifying content mapper output file extension mappings in TypeScript configs and package manifests.*

 * (2 days ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript/pull/64581#issuecomment-5971700909) **leonidaz** thanked andrewbranch and argued that TypeScript should allow extensionless resolution for mapper-supported formats when configured to match bundler behavior

### [PR microsoft/TypeScript#64583](https://github.com/microsoft/TypeScript/pull/64583) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**Allow other VS Code extensions to install LSP middleware on language feature responses**

*Enable third-party VS Code extensions to register custom LSP middleware for TypeScript language feature responses*

 * (2 days ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`
 * (yesterday) **andrewbranch** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/64583#issuecomment-5971044194) **insilications** said "@andrewbranch Thanks so much for support this use case! This will unlock a lot of interesting things."

### [Issue microsoft/TypeScript#64589](https://github.com/microsoft/TypeScript/issues/64589) (Closed, `Bug`, **ahejlsberg**)

**TS 7: declaration emit prints union members in a different order from run to run**

*TS 7’s declaration emitter produces union types with non-deterministic member ordering across runs, causing unstable declaration files.*

 * (yesterday) **ahejlsberg** added label `Bug`, set milestone to `TypeScript 7.1.0 Beta`, and assigned to **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript/issues/64589#issuecomment-5971023277) **ahejlsberg** identified that getInferTypeParameters iterated a locals map in random order, leading to unstable CompareTypes behavior
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript#64621](https://github.com/microsoft/TypeScript/pull/64621) (Closed, `Author: Team`, `For Milestone Bug`, **ahejlsberg**)

**Ensure stable ordering in \`getInferTypeParameters\` result**

*Guarantee deterministic ordering of inferred type parameters returned by getInferTypeParameters.*

 * created by **ahejlsberg**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Milestone Bug`, and assigned to **ahejlsberg**
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript#64622](https://github.com/microsoft/TypeScript/issues/64622) (Open)

**\[ServerErrors\]\[JavaScript\] main vs **

*The main JavaScript server pipeline analyzed 300 popular TypeScript repos, reporting four interesting changes among 205 successes and various failures.*

 * created by **typescript-automation[bot]**
 * [today](https://github.com/microsoft/TypeScript/issues/64622#issuecomment-5972853612) **typescript-automation[bot]** described a server connection closed prematurely error for tastejs/todomvc and provided logs, last requests, and repro steps
 * [today](https://github.com/microsoft/TypeScript/issues/64622#issuecomment-5972854026) **typescript-automation[bot]** reported a server connection closed prematurely error for gchq/CyberChef and provided error details, last requests, and repro steps
 * [today](https://github.com/microsoft/TypeScript/issues/64622#issuecomment-5972854485) **typescript-automation[bot]** reported a panic in textDocument/formatting due to a debug failure and included a stack trace
 * [today](https://github.com/microsoft/TypeScript/issues/64622#issuecomment-5972854878) **typescript-automation[bot]** reported panic handling request for textDocument/diagnostic with stack trace and affected repo details

### [Issue microsoft/TypeScript#64623](https://github.com/microsoft/TypeScript/issues/64623) (Open)

**\[ServerErrors\]\[TypeScript\] main vs **

*The TypeScript main branch pipeline analyzing 300 popular GitHub repositories encountered server errors, timeouts, and multiple clone failures.*

 * created by **typescript-automation[bot]**
 * [today](https://github.com/microsoft/TypeScript/issues/64623#issuecomment-5973552095) **typescript-automation[bot]** reported a panic error due to invalid memory address or nil pointer dereference in the workspace/symbol handler
 * [today](https://github.com/microsoft/TypeScript/issues/64623#issuecomment-5973552498) **typescript-automation[bot]** reported a premature server connection closure with undefined error for openclaw/openclaw, including error artifacts, recent requests, and repro steps
 * [today](https://github.com/microsoft/TypeScript/issues/64623#issuecomment-5973552907) **typescript-automation[bot]** reported a panic handling request textDocument/diagnostic for withastro/astro due to flaky diagnostics

### [PR microsoft/TypeScript#64624](https://github.com/microsoft/TypeScript/pull/64624) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Fix idle cache clean timer never being stored on Session**

*The idle cache clean timer isn't saved to session, so cancelIdleCacheClean can't stop it and Close blocks until it fires.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [Issue microsoft/TypeScript#64625](https://github.com/microsoft/TypeScript/issues/64625) (Open)

**Declaration emit re\-walks a package\.json \`exports\` map for every declaration \(module specifier cache not shared across node builders\)**

*Declaration emit repeatedly walks the package.json exports map for each declaration, causing significant performance regressions.*

 * created by **novacoole**

