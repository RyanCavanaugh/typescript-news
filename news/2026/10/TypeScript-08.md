# Report for 2026-10-08 (Thursday, October 8th, 2026)

18 different users commented on 35 different issues.

## Recommended Actions

 * Response Recommended
    * @lex00 asked if this approach could work for tsconfig and requested implementation details in [microsoft/TypeScript#57486](https://github.com/microsoft/TypeScript/issues/57486#issuecomment-6070880841)
    * @ehoogeveen-medweb suggested adding missing optional-access diagnostic codes to the plainJSErrors list and updating the Go implementation in [microsoft/TypeScript#57640](https://github.com/microsoft/TypeScript/issues/57640#issuecomment-6078924694)
    * @hkleungai asked whether the PR would affect issue #3665 in [microsoft/TypeScript#64696](https://github.com/microsoft/TypeScript/pull/64696#issuecomment-6066958664)

## Activity Summary

### [Issue microsoft/TypeScript#57486](https://github.com/microsoft/TypeScript/issues/57486) (Open, `Suggestion`, `In Discussion`, **sheetalkamat**)

**Proposal for merging array or object options in tsconfig file**

*Allow tsconfig file inheritance to merge array and object compilerOptions like paths and typeRoots rather than overriding them.*

 * [1 year ago](https://github.com/microsoft/TypeScript/issues/57486#issuecomment-3304835142) **pcfreak30** suggested reusing base compilerOptions.paths across monorepo packages, advocated for ESM JS configs to future-proof and argued against redefining them
 * (48 weeks ago) **RyanCavanaugh** added labels `Suggestion`, `In Discussion`
 * [today](https://github.com/microsoft/TypeScript/issues/57486#issuecomment-6070880841) **lex00** proposed allowing tsconfig to be authored in a restricted subset of TypeScript using the typescript-as-data spec and asked if this approach could work

### [Issue microsoft/TypeScript#57640](https://github.com/microsoft/TypeScript/issues/57640) (Open, `Bug`, `Help Wanted`, `Domain: Parser`)

**JS \| Optional chaining left hand assignment not detected as syntax error\.**

*VS Code fails to flag invalid left-hand assignment using optional chaining in JavaScript files.*

 * [1.7 years ago](https://github.com/microsoft/TypeScript/issues/57640#issuecomment-2566292163) **Andarist** stated the issue was not actionable and explained that TypeScript reports some syntax errors as grammar errors during checking, provided an example, and noted that only a new check mode could isolate grammar errors
 * [1.7 years ago](https://github.com/microsoft/TypeScript/issues/57640#issuecomment-2568447792) **RyanCavanaugh** said "I think it'd still be preferable if we saw grammar errors in JS, it just means this is a bigger work item than this specific issue"
 * **RyanCavanaugh** added label `Domain: Parser`
 * [later](https://github.com/microsoft/TypeScript/issues/57640#issuecomment-6078924694) **ehoogeveen-medweb** described that plain JS files already run the full checker and that optional-access diagnostics were being filtered out due to missing codes in the plainJSErrors allowlist, listed the five relevant diagnostic codes, explained a local patch adding them which reported no extra errors, and suggested applying the same five-line change in the Go implementation while noting a limitation for TS2780 cases

### [PR microsoft/TypeScript#64411](https://github.com/microsoft/TypeScript/pull/64411) (Open, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Preserve primitive literal union origins without special intersections**

*Preserve literal union origins for string, number, and bigint in completions and quick info without special intersections.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/64411#issuecomment-6047533096) **typescript-automation[bot]** posted the results of the requested performance run
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64411#issuecomment-6047591133) **typescript-automation[bot]** reported that test results comparing baseline and PR looked good
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64411#issuecomment-6048381655) **typescript-automation[bot]** reported build results for the top 400 repos comparing baseline and PR and highlighted failures in pixijs
 * [today](https://github.com/microsoft/TypeScript/pull/64411#issuecomment-6065878245) **weswigham** explained that test failures were expected follow-ons from removing mapped type behavior and suggested rewriting code to avoid denormalized union behavior

### [Issue microsoft/TypeScript#64585](https://github.com/microsoft/TypeScript/issues/64585) (Closed, `Duplicate`)

**TS Symbol typing clashes with standard, idiomatic JS**

*TypeScript’s symbol typing model conflicts with JavaScript’s native Symbol behavior, hindering idiomatic JS symbol usage.*

 * [6 days ago](https://github.com/microsoft/TypeScript/issues/64585#issuecomment-5956824676) **RyanCavanaugh** said "This seems like a straightforward duplicate of #35909, not a separate request"
 * [6 days ago](https://github.com/microsoft/TypeScript/issues/64585#issuecomment-5959601794) **michaelfig** identified the issue as a duplicate of #35909, offered to close it if the Related Work section of #64451 sufficed, and noted uncertainty about satisfying @typescript-automation
 * **RyanCavanaugh** added label `Duplicate`
 * [today](https://github.com/microsoft/TypeScript/issues/64585#issuecomment-6072469185) **typescript-automation[bot]** said "This issue has been marked as "Duplicate" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-automation[bot]** closed the issue

### [PR microsoft/TypeScript#64657](https://github.com/microsoft/TypeScript/pull/64657) (Open, `For Milestone Bug`, **weswigham**)

**Show the JSDoc written on an \`import x = a\.x\` alias in hover and completions**

*Enable display of alias-specific JSDoc comments on import aliases during hover and completions.*

 * (2 days ago) **typescript-automation[bot]** added label `For Milestone Bug`, and assigned to **weswigham**
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64657#issuecomment-6048754588) **patrickkettner** offered to widen the PR to show the whole chain on both refs, noting preference for that approach and explaining prior decision to maintain parity with version 6.0
 * [today](https://github.com/microsoft/TypeScript/pull/64657#issuecomment-6065773879) **weswigham** said "Yeah, if we're gonna change anything here, I'd wanna make it consistent across reference site kinds and include all the docs possible, for sure."
 * [today](https://github.com/microsoft/TypeScript/pull/64657#issuecomment-6069469752) **patrickkettner** asked whether hover should display both @since tags from alias and implementation or if the alias wins

### [PR microsoft/TypeScript#64658](https://github.com/microsoft/TypeScript/pull/64658) (Open, `For Uncommitted Bug`, **DanielRosenwasser**, **Copilot**)

**Fix Windows module resolution for reserved path segments**

*Use extended path namespaces to prevent Windows reserved device names like con from blocking module resolution.*

 * [2 days ago](https://github.com/microsoft/TypeScript/pull/64658#issuecomment-6023711474) **Copilot** addressed the issue in commit be35d253, retained original fast paths, gated allocation-free component scan to reserved-name paths, and added zero-allocation coverage for the detector
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64658#issuecomment-6045856374) **DanielRosenwasser** said "@copilot does it make sense to just try realpath and do the scan only if that doesn't work? It's extremely uncommon to have these device names."
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64658#issuecomment-6046126151) **Copilot** updated implementation to run original path open first and trigger reserved-component scan only on failure, preventing scan cost on successful realpaths
 * [today](https://github.com/microsoft/TypeScript/pull/64658#issuecomment-6070217751) **jakebailey** said "This fails linting and testing"
 * [today](https://github.com/microsoft/TypeScript/pull/64658#issuecomment-6070384917) **DanielRosenwasser** requested Copilot address CI failures and provided continuous integration failure logs
 * [today](https://github.com/microsoft/TypeScript/pull/64658#issuecomment-6070559076) **Copilot** fixed the Windows short-path expectation, removed t.Parallel() from the allocation test, and adjusted cleanup to satisfy custom lint
 * [today](https://github.com/microsoft/TypeScript/pull/64658#issuecomment-6070609937) **jakebailey** said "I don't think you can just remove Parallel without a nolint directive that says why"

### [PR microsoft/TypeScript#64659](https://github.com/microsoft/TypeScript/pull/64659) (Open, `For Uncommitted Bug`, **johnfav03**)

**Compute signatures of dependent files in parallel on incremental rebuilds**

*Declaration signatures for files dependent on an edited file are now computed in parallel during incremental rebuilds to significantly reduce build times.*

 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/64659#issuecomment-6025077510) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * **typescript-automation[bot]** assigned to **johnfav03**
 * [today](https://github.com/microsoft/TypeScript/pull/64659#issuecomment-6067067676) **resure** described changes to NewWorkGroup API by replacing singleThreaded with concurrency, removed the semaphore, applied limits per group, and reported unchanged performance

### [PR microsoft/TypeScript#64678](https://github.com/microsoft/TypeScript/pull/64678) (Closed, `Author: Team`, `For Uncommitted Bug`, **ahejlsberg**)

**Encapsulate Symbol fields with getters and setters**

*Encapsulate ast.Symbol's exported fields by making them private with getters and setters and updating all usages with regression tests.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/64678#issuecomment-6047016977) **typescript-automation[bot]** provided the requested performance run results in a detailed comparison report
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64678#issuecomment-6047345595) **typescript-automation[bot]** provided tsc user test results and indicated everything looked good
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64678#issuecomment-6047727192) **typescript-automation[bot]** reported successful tsc comparison between baseline and pr on the top 400 repos
 * [today](https://github.com/microsoft/TypeScript/pull/64678#issuecomment-6068992189) **ahejlsberg** said "Merged as part of #64691."
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript#64683](https://github.com/microsoft/TypeScript/issues/64683) (Open, `Bug`, **jakebailey**, **RyanCavanaugh**, **Copilot**)

**Type printer recurses without limit into nested array/tuple types \(stack overflow; can leave later types \`any\`\)**

*TypeScript's type printer now infinitely recurses into nested array and tuple types, causing stack overflows instead of truncation.*

 * created by **ssalbdivad**
 * (today) **RyanCavanaugh** added label `Bug`, and assigned to **Copilot**, **RyanCavanaugh**, **jakebailey**

### [Issue microsoft/TypeScript#64687](https://github.com/microsoft/TypeScript/issues/64687) (Closed, `Bug`, **RyanCavanaugh**, **Copilot**)

**Replacement libs load in an arbitrary order in TypeScript 7: \`sortLibs\` is not stable**

*TypeScript 7's unstable sortLibs causes libReplacement to load libraries in arbitrary order, breaking overload precedence.*

 * created by **rymskip**
 * (today) **RyanCavanaugh** added label `Bug`, set milestone to `Backlog`, and assigned to **Copilot**, **RyanCavanaugh**

### [PR microsoft/TypeScript#64691](https://github.com/microsoft/TypeScript/pull/64691) (Closed, `Author: Team`, `For Uncommitted Bug`, **ahejlsberg**)

**Shared data symbols**

*Splitting Symbol into separate header and shared data parts in the checker reduces instantiated symbol size from 96 to 24 bytes.*

 * [today](https://github.com/microsoft/TypeScript/pull/64691#issuecomment-6063530173) **typescript-automation[bot]** notified that the DT test run failed and asked to check the log
 * [today](https://github.com/microsoft/TypeScript/pull/64691#issuecomment-6063591639) **ahejlsberg** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/64691#issuecomment-6063593410) **typescript-automation[bot]** posted CI build status updates for several test commands
 * [today](https://github.com/microsoft/TypeScript/pull/64691#issuecomment-6064055957) **typescript-automation[bot]** notified that DT test results were ready and unchanged
 * [today](https://github.com/microsoft/TypeScript/pull/64691#issuecomment-6064184107) **typescript-automation[bot]** posted the requested performance run results including compiler metrics and memory usage
 * [today](https://github.com/microsoft/TypeScript/pull/64691#issuecomment-6064188275) **typescript-automation[bot]** provided tsc user test results and indicated everything looked good
 * [today](https://github.com/microsoft/TypeScript/pull/64691#issuecomment-6065021531) **typescript-automation[bot]** reported successful tsc comparison between baseline and pr on the top 400 repos
 * [today](https://github.com/microsoft/TypeScript/pull/64691#issuecomment-6066086195) **ahejlsberg** said "Looks like 5-7% savings in memory overhead."
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript#64692](https://github.com/microsoft/TypeScript/issues/64692) (Open, `Needs Investigation`, **ahejlsberg**)

**\[7\.0 regression\] Object literal passed to a method on a large union creates exponentially many types \(type order dependent\)**

*Contextual typing an object literal against a large union in TypeScript 7.0.2 triggers exponential type instantiations and memory usage regression dependent on union ordering.*

 * created by **ctriley**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **ahejlsberg**

### [PR microsoft/TypeScript#64693](https://github.com/microsoft/TypeScript/pull/64693) (Closed, `For Uncommitted Bug`, **RyanCavanaugh**, **Copilot**)

**Preserve replacement lib order during sorting**

*Implement stable sorting for replacement libraries to preserve their configured order and ensure consistent overload resolution*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * (today) **typescript-automation[bot]** added labels `For Milestone Bug`, `For Uncommitted Bug`, and removed label `For Milestone Bug`

### [PR microsoft/TypeScript#64694](https://github.com/microsoft/TypeScript/pull/64694) (Open, `For Uncommitted Bug`, **RyanCavanaugh**, **Copilot**)

**Bound recursive array and tuple type printing**

*Limit active array and tuple serialization depth to prevent infinite recursion and stack overflows when printing recursive generic types.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [PR microsoft/TypeScript#64695](https://github.com/microsoft/TypeScript/pull/64695) (Open, `For Milestone Bug`, **ahejlsberg**)

**\[experiment\] Skip incompatible discriminants when inferring**

*Experimentally skip incompatible discriminant properties during TypeScript union type inference to reduce workload and validate via tests.*

 * created by **Andarist**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64695#issuecomment-6065354889) **jakebailey** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/64695#issuecomment-6065356820) **typescript-automation[bot]** listed CI job commands and their build statuses with result links
 * [today](https://github.com/microsoft/TypeScript/pull/64695#issuecomment-6065772449) **typescript-automation[bot]** notified that the DT tests results were ready and unchanged
 * [today](https://github.com/microsoft/TypeScript/pull/64695#issuecomment-6065888411) **typescript-automation[bot]** reported tsc user test results and confirmed everything looked good
 * [today](https://github.com/microsoft/TypeScript/pull/64695#issuecomment-6065889237) **typescript-automation[bot]** reported performance run results for the requested comparison
 * [today](https://github.com/microsoft/TypeScript/pull/64695#issuecomment-6066282755) **weswigham** noted that previous JS codebase type comparisons were costly, acknowledged the perf suite improvements, and suggested using discriminateTypeByDiscriminableItems for consistent discrimination method
 * [today](https://github.com/microsoft/TypeScript/pull/64695#issuecomment-6066595594) **typescript-automation[bot]** reported that running the top 400 repos tsc comparison between baseline and pr succeeded without issues

### [PR microsoft/TypeScript#64696](https://github.com/microsoft/TypeScript/pull/64696) (Closed, `Author: Team`, `For Milestone Bug`, **weswigham**)

**Use ensureModifierFlags to calculate jsdoc constructor property modifiers**

*Implement ensureModifierFlags to properly calculate modifier flags for JSDoc constructor properties.*

 * created by **weswigham**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Milestone Bug`, `For Milestone Bug`, and assigned to **weswigham**
 * [today](https://github.com/microsoft/TypeScript/pull/64696#issuecomment-6066958664) **hkleungai** asked if the PR would affect issue #3665 given its example wasn’t in the test suite
 * [today](https://github.com/microsoft/TypeScript/pull/64696#issuecomment-6067934267) **jakebailey** said "I would assume none? You're asking for the old override behavior back, but this just fixes an emit bug?"

### [PR microsoft/TypeScript#64697](https://github.com/microsoft/TypeScript/pull/64697) (Open, `For Uncommitted Bug`)

**feat: add missing properties and JSX attributes code fixes**

*Add missing properties and rectify JSX attribute handling via code fixes.*

 * created by **a-tarasyuk**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [PR microsoft/TypeScript#64698](https://github.com/microsoft/TypeScript/pull/64698) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**AST nodes as handles, offsets into areanas**

*Add support for representing AST nodes as compact handles by using offsets into arenas*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/64698#issuecomment-6069775426) **jakebailey** said "@typescript-bot perf test this"
 * [today](https://github.com/microsoft/TypeScript/pull/64698#issuecomment-6069776858) **typescript-automation[bot]** noted that performance tests started and that the comment would be updated as builds progressed

### [PR microsoft/TypeScript#64699](https://github.com/microsoft/TypeScript/pull/64699) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Switch to \`type SymbolName unique\.Handle\[string\]\`**

*Refactor the SymbolName type to use unique.Handle[string] for testing purposes*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/64699#issuecomment-6069852600) **jakebailey** said "@typescript-bot perf test this"
 * [today](https://github.com/microsoft/TypeScript/pull/64699#issuecomment-6069854530) **typescript-automation[bot]** reported that CI jobs started and that the comment would update as builds progress
 * [today](https://github.com/microsoft/TypeScript/pull/64699#issuecomment-6070367271) **typescript-automation[bot]** posted the performance run results that were requested by @jakebailey

### [Issue microsoft/TypeScript#64700](https://github.com/microsoft/TypeScript/issues/64700) (Open, `Needs Investigation`, **andrewbranch**)

**LSP middleware cannot handle \`textDocument/prepareRename\` errors, which blocks rename in embedded templates**

*The LSP middleware fails to process prepareRename error responses, blocking renames within embedded templates.*

 * created by **mantou132**

### [Issue microsoft/TypeScript#64701](https://github.com/microsoft/TypeScript/issues/64701) (Open, `Bug`)

**typescript\-go: Infinite recursion in inferFromTypes via getReturnTypeOfSignature \(tsc 5\.9 OK\)**

*typescript-go infinite recursion in inferFromTypes via getReturnTypeOfSignature for type-fest overloads blocks oxlint, whereas tsc 5.9 finishes.*

 * created by **jandolezal71**

### [Issue microsoft/TypeScript#64702](https://github.com/microsoft/TypeScript/issues/64702) (Open, `Help Wanted`, `Possible Improvement`)

**\[7\.0 regression\] hover on calls through object properties loses function JSDoc while signature help works**

*Hovering on object property calls in TypeScript 7.0.x omits JSDoc comments whereas signature help still shows them.*

 * created by **lixiaoyan**

### [PR microsoft/TypeScript#64703](https://github.com/microsoft/TypeScript/pull/64703) (Open, `For Backlog Bug`)

**Preserve computed property names in isolated declaration emit**

*Preserve computed identifier and dotted property names in declaration files under --isolatedDeclarations without inferring index signatures and with existing diagnostics.*

 * created by **Trighap52**
 * (later) **typescript-automation[bot]** added labels `For Backlog Bug`, `For Backlog Bug`

### [PR microsoft/TypeScript#64704](https://github.com/microsoft/TypeScript/pull/64704) (Open, `For Backlog Bug`)

**Restore function signature documentation in native hover**

*Hovering function calls now shows the declaration’s JSDoc (even through aliases or wrappers), with fallback to the function’s own comments.*

 * created by **lixiaoyan**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [Issue microsoft/TypeScript#64705](https://github.com/microsoft/TypeScript/issues/64705) (Open, `Bug`)

**False negative issues in function type parameters of ts2824**

*Function type parameter destructuring with unused renamed generics does not trigger the expected TS2824 error.*

 * created by **bvanjoi**

