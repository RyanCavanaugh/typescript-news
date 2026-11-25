# Report for 2026-11-19 (Thursday, November 19th, 2026)

14 different users commented on 56 different issues.

## Activity Summary

### [Issue microsoft/TypeScript#64429](https://github.com/microsoft/TypeScript/issues/64429) (Closed, `API Request`, **andrewbranch**)

**\[api\] Add back missing: \`setEmitFlags\` and \`addSynthetic\*Comment\`**

*Add Go API support for emit flags and synthetic comments on synthesized nodes, matching TypeScript’s existing functionality.*

 * created by **dragomirtitian**
 * (7 weeks ago) **RyanCavanaugh** added label `API Request`, and assigned to **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#64500](https://github.com/microsoft/TypeScript/pull/64500) (Closed, `For Uncommitted Bug`, **andrewbranch**)

**Add support for setting emit flags and synthetic comments**

*Add support for configuring emit flags and preserving synthetic comments.*

 * [7 weeks ago](https://github.com/microsoft/TypeScript/pull/64500#issuecomment-5873403732) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * **typescript-automation[bot]** assigned to **andrewbranch**
 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/64500#issuecomment-6541748893) **el-j** explained that #65058 overlaps with this PR, recommended this PR’s design, identified complementary JSDoc fixes, and offered additional tests for edge cases
 * [today](https://github.com/microsoft/TypeScript/pull/64500#issuecomment-7020519578) **andrewbranch** said "These commits were merged in https://github.com/microsoft/TypeScript/pull/65447"
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript#64653](https://github.com/microsoft/TypeScript/issues/64653) (Closed, **DanielRosenwasser**, **Copilot**)

**Windows: module resolution fails for paths containing a \`con/\` directory segment \(reserved device name\)**

*TypeScript 7’s Windows native module resolution fails for paths containing a reserved `con/` directory, breaking declaration imports and re-exports.*

 * created by **itrapashko**
 * (6 weeks ago) **DanielRosenwasser** assigned to **Copilot**, **DanielRosenwasser**
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#64658](https://github.com/microsoft/TypeScript/pull/64658) (Closed, `Author: Team`, `For Uncommitted Bug`, **DanielRosenwasser**, **Copilot**)

**Fix Windows module resolution for reserved path segments**

*Fix Windows module resolution for paths containing reserved device-name segments, including regression coverage for directories and declaration files.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/64658#issuecomment-6589252621) **jakebailey** said "@copilot+gpt-6.1-sol see thread above; fix so windows lint will pass correctly"
 * **typescript-automation[bot]** added label `Author: Team`
 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/64658#issuecomment-6589531201) **Copilot** restored parallel execution for the reserved-component behavior test, moved allocation measurement to a separate non-parallel test, and committed the fix as 54e0b672
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#64808](https://github.com/microsoft/TypeScript/pull/64808) (Open, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **DanielRosenwasser**)

**Share a single cache for all type relationships and propagate results hierarchically**

*Consolidate separate type-relationship caches into a shared hierarchical cache to reduce overlap and improve memory efficiency.*

 * [5 weeks ago](https://github.com/microsoft/TypeScript/pull/64808#issuecomment-6162006945) **typescript-automation[bot]** reported that the performance test job started and linked to its results
 * [5 weeks ago](https://github.com/microsoft/TypeScript/pull/64808#issuecomment-6162361810) **typescript-automation[bot]** reported the requested performance results, including a 2.27% reduction in memory usage for the tsc Compiler-Unions benchmark
 * **jakebailey** added label `Domain: Performance`
 * [today](https://github.com/microsoft/TypeScript/pull/64808#issuecomment-7015802429) **RyanCavanaugh** said "Marking as draft until we have consensus on this approach"

### [PR microsoft/TypeScript#65043](https://github.com/microsoft/TypeScript/pull/65043) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Speed up property and index signature lookups**

*Optimize property and index signature lookups to improve TypeScript performance.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/65043#issuecomment-6986758367) **jakebailey** said "@typescript-bot perf test this faster"
 * [yesterday](https://github.com/microsoft/TypeScript/pull/65043#issuecomment-6986760760) **typescript-automation[bot]** reported that the performance test job started and linked to its build results
 * [yesterday](https://github.com/microsoft/TypeScript/pull/65043#issuecomment-6987783689) **typescript-automation[bot]** provided the requested performance run results comparing the baseline and PR
 * [today](https://github.com/microsoft/TypeScript/pull/65043#issuecomment-7022330349) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/65043#issuecomment-7022333104) **typescript-automation[bot]** reported that the performance test failed because the bot lacked permission to edit the Azure DevOps build pipeline configuration
 * [today](https://github.com/microsoft/TypeScript/pull/65043#issuecomment-7022878172) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/65043#issuecomment-7022880469) **typescript-automation[bot]** reported that the performance test job started and linked to its results
 * [today](https://github.com/microsoft/TypeScript/pull/65043#issuecomment-7023819926) **typescript-automation[bot]** provided the requested performance benchmark results comparing the baseline and pull request
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#65291](https://github.com/microsoft/TypeScript/pull/65291) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Add order dependence tests**

*Add checker ordering tests and fuzzing to detect and preserve fixes for order-dependent analysis failures.*

 * (2 weeks ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`
 * [yesterday](https://github.com/microsoft/TypeScript/pull/65291#issuecomment-6993015348) **jakebailey** said "Okay, I think now this is ready to go in."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#65388](https://github.com/microsoft/TypeScript/pull/65388) (Open, `Author: Team`, `For Uncommitted Bug`, **DanielRosenwasser**)

**🤖 Pick PR \#64632 \(Restart a file's imports when a lat\.\.\.\) into release\-7\.0**

*Requests cherry-picking PR #64632 into release-7.0 to restart a file’s imports when latency-related conditions occur.*

 * (1 week ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **DanielRosenwasser**
 * (today) **RyanCavanaugh** closed the issue
 * (today) **RyanCavanaugh** reopened the issue

### [PR microsoft/TypeScript#65447](https://github.com/microsoft/TypeScript/pull/65447) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**Add support for setting emit flags and synthetic comments**

*Adds support for configuring emitter flags and synthetic comments while refactoring shared async-related emitter code.*

 * (1 week ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript/pull/65447#issuecomment-7020496674) **andrewbranch** clarified that the properties were inherited from Strada’s `CommentRange` and `SyntheticCommentRange` types, described newline positions relative to comments, and noted that both could exist on a synthetic comment
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#65449](https://github.com/microsoft/TypeScript/pull/65449) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**Fix incorrect last bytes sent API timing data from nested requests**

*Correct the last-bytes-sent API timing data so nested requests report accurate values.*

 * (1 week ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#65493](https://github.com/microsoft/TypeScript/pull/65493) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Convert patterns in object rest bindings to assignment targets**

*Fix emit to convert nested patterns in object rest bindings into valid assignment targets and avoid printer crashes.*

 * (6 days ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#65498](https://github.com/microsoft/TypeScript/pull/65498) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Fix CommonJS declaration emit crashes**

*Fix declaration emit crashes caused by invalid export names from destructured CommonJS requires and template-literal exports.*

 * (6 days ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#65505](https://github.com/microsoft/TypeScript/issues/65505) (Open, `Bug`, `Domain: LS: TSServer`, **DanielRosenwasser**, **Copilot**)

**\`workspace/willRenameFiles\` panics with "changes overlap" when the renamed file is loaded by \`import\(\)\` with a \`\.ts\` specifier**

*Renaming a TypeScript file referenced by a dynamic `.ts` import causes `workspace/willRenameFiles` to generate overlapping edits and panic.*

 * (2 days ago) **RyanCavanaugh** added labels `Bug`, `Domain: LS: TSServer`, and set milestone to `Backlog`
 * (today) **DanielRosenwasser** assigned to **Copilot**, **DanielRosenwasser**

### [Issue microsoft/TypeScript#65516](https://github.com/microsoft/TypeScript/issues/65516) (Open, `Needs Investigation`, **andrewbranch**)

**Content mapper ignore directives need diagnostic\-code selectors**

*Add diagnostic-code selectors to content-mapper ignore directives so framework diagnostics can be suppressed without hiding unrelated errors.*

 * created by **ubugeeei**
 * (2 days ago) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **andrewbranch**
 * **andrewbranch** added to milestone `TypeScript 7.1.1 RC`

### [PR microsoft/TypeScript#65517](https://github.com/microsoft/TypeScript/pull/65517) (Closed, `For Milestone Bug`, **andrewbranch**)

**feat\(content\-mapper\): add diagnostic\-code selectors**

*Add diagnostic-code selectors to content-mapper directives, enabling code-specific suppression with protocol v10 support and validation for invalid selectors.*

 * created by **ubugeeei**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/65517#issuecomment-6912561753) **ubugeeei** said "@microsoft-github-policy-service agree"
 * (today) **typescript-automation[bot]** added label `For Milestone Bug`, removed label `For Uncommitted Bug`, and assigned to **andrewbranch**

### [PR microsoft/TypeScript#65545](https://github.com/microsoft/TypeScript/pull/65545) (Closed, `Author: Team`, `For Uncommitted Bug`)

**Update localization files**

*Update localization handbacks and regenerate their corresponding runtime artifacts.*

 * created by **typescript-automation[bot]**
 * (3 days ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#65560](https://github.com/microsoft/TypeScript/issues/65560) (Closed, `Bug`, **RyanCavanaugh**, **Copilot**)

**Aliased \`Partial\<{ … }\>\` is duplicated when instantiated again: quadratic inference, spurious TS2859, repeated union members**

*Aliased `Partial` object types are duplicated during instantiation, causing quadratic inference, spurious TS2859 errors, and repeated union members.*

 * (yesterday) **RyanCavanaugh** added label `Bug`, set milestone to `Backlog`, and assigned to **RyanCavanaugh**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#65562](https://github.com/microsoft/TypeScript/pull/65562) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **RyanCavanaugh**, **Copilot**)

**Cache homomorphic mapped type constituent instantiations under their re\-instantiation key**

*Cache homomorphic mapped type constituent instantiations under re-instantiation keys to eliminate duplicate types, improve inference performance, and prevent spurious TS2859 errors.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/65562#issuecomment-6988329920) **typescript-automation[bot]** reported that the performance test job started and linked to its build results
 * [yesterday](https://github.com/microsoft/TypeScript/pull/65562#issuecomment-6988503615) **DanielRosenwasser** said "Okay but why weren't the types reduced on union construction?"
 * [yesterday](https://github.com/microsoft/TypeScript/pull/65562#issuecomment-6989651778) **typescript-automation[bot]** reported that the requested performance run results were available and included comparison metrics for the compiler-unions scenario
 * [today](https://github.com/microsoft/TypeScript/pull/65562#issuecomment-7019172249) **jakebailey** said "This needs a merge from main and baseline reaccept"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#65565](https://github.com/microsoft/TypeScript/pull/65565) (Closed, `Author: Team`, `For Uncommitted Bug`, **gabritto**)

**Generate content mapper types from json schema**

*Introduce a JSON schema and generation script for content mapper protocol types, enabling typed implementations and validation across languages.*

 * (yesterday) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **gabritto**
 * (today) **gabritto** closed the issue

### [Issue microsoft/TypeScript#65570](https://github.com/microsoft/TypeScript/issues/65570) (Open, `Bug`, **RyanCavanaugh**, **Copilot**)

**Declaration emit writes an alias's own type parameter \(\`Labeled\<Label\>\`\) instead of the type argument when the parameter is unused**

*Declaration emit incorrectly replaces an unused type alias argument with the alias’s own type parameter, producing invalid out-of-scope `.d.ts` files.*

 * created by **ktfth**
 * (today) **RyanCavanaugh** added label `Bug`, set milestone to `Backlog`, and assigned to **Copilot**, **RyanCavanaugh**

### [Issue microsoft/TypeScript#65571](https://github.com/microsoft/TypeScript/issues/65571) (Closed, `Not a Defect`)

**Declaration emit drops the normalized optional properties of a union of object literals \(\`retries?: undefined\`\)**

*Declaration emit in TypeScript 7.x drops normalized optional properties from unions of object literals, causing consumers to incorrectly reject valid property access.*

 * created by **ktfth**
 * [today](https://github.com/microsoft/TypeScript/issues/65571#issuecomment-7016512843) **RyanCavanaugh** explained that emitted declaration files do not always preserve source types because type syntax cannot represent certain differences between widened and unwidened object literal unions
 * **RyanCavanaugh** added label `Not a Defect`

### [Issue microsoft/TypeScript#65574](https://github.com/microsoft/TypeScript/issues/65574) (Closed, `Not a Defect`, **ahejlsberg**)

**7\.1 regression: type argument inferred from a union of callback types \(\`R\` \| \`Promise\<R \| void\>\`\) falls back to its constraint**

*TypeScript 7.1 regresses generic inference for unioned callback return types, falling back to the constraint and losing precise route response types.*

 * created by **kazu-42**
 * [today](https://github.com/microsoft/TypeScript/issues/65574#issuecomment-7017356660) **RyanCavanaugh** said "Bisects to https://github.com/microsoft/typescript-go/pull/4591"
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript/issues/65574#issuecomment-7024174478) **ahejlsberg** explained that the current behavior matched TypeScript 6.0, described related changes and reversions in TypeScript 7.0 and 7.1, and showed that simplifying the repro produced the expected behavior across compiler versions
 * (today) **ahejlsberg** added label `Not a Defect`, and removed label `Needs Investigation`

### [PR microsoft/TypeScript#65575](https://github.com/microsoft/TypeScript/pull/65575) (Closed, `For Backlog Bug`)

**Fix contextual typing loss for computed string keys under circular mapped\-type key constraints**

*Fix a regression where circular mapped-type key constraints create a spurious string index signature that causes computed-key callback parameters to lose contextual typing.*

 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/65575#issuecomment-7003466885) **tydavid5** noted that the change followed the approach from #65546, reproduced the bug on main, and verified the fix with the reproduction and a new regression test
 * [today](https://github.com/microsoft/TypeScript/pull/65575#issuecomment-7003521836) **tydavid5** said "@microsoft-github-policy-service agree"
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#65576](https://github.com/microsoft/TypeScript/pull/65576) (Closed, `For Backlog Bug`)

**Ignore the synthetic this parameter when matching JSDoc params**

*Fix JSDoc parameter matching to ignore leading synthetic or explicit `this` parameters and prevent incorrect TS7031 and TS8024 errors.*

 * created by **tydavid5**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#65577](https://github.com/microsoft/TypeScript/pull/65577) (Closed, `For Backlog Bug`)

**Allow declare redeclarations of inherited properties in field initializers**

*Allow inherited properties redeclared with `declare` in field initializers without triggering TS2729, while preserving errors for actual overwrites and invalid references.*

 * created by **tydavid5**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#65578](https://github.com/microsoft/TypeScript/pull/65578) (Closed, `For Backlog Bug`)

**Fix object\-rest lowering for statements directly in a for\-of body**

*Fix object-rest lowering so nested for-of loops and function declarations directly in loop bodies are correctly transformed and executed.*

 * created by **tydavid5**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#65579](https://github.com/microsoft/TypeScript/pull/65579) (Closed, `For Backlog Bug`)

**Preserve U\+FEFF when Wtf8Decoder reads payload text**

*Preserve leading and surrogate-adjacent U+FEFF characters in Wtf8Decoder payloads by default while retaining explicit BOM-stripping opt-out behavior.*

 * created by **tydavid5**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#65580](https://github.com/microsoft/TypeScript/pull/65580) (Closed, `For Backlog Bug`)

**Resolve JSDoc '\#' links to instance members**

*Fix JSDoc `#` links in the Go port to resolve instance members while preserving `.` links for static members.*

 * created by **tydavid5**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * (today) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/65580#issuecomment-7015314196) **RyanCavanaugh** said "Bulk closing, see https://github.com/microsoft/TypeScript/blob/main/CONTRIBUTING.md#no-undirected-activity"

### [PR microsoft/TypeScript#65582](https://github.com/microsoft/TypeScript/pull/65582) (Open, `Author: Team`, `For Uncommitted Bug`, **gabritto**)

**Content mapper docs**

*Request to create or improve documentation for the content mapper.*

 * created by **gabritto**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **gabritto**

### [PR microsoft/TypeScript#65583](https://github.com/microsoft/TypeScript/pull/65583) (Open, `Author: Team`, `For Uncommitted Bug`, **DanielRosenwasser**, **Copilot**)

**Avoid duplicate file rename edits for dynamic imports**

*Deduplicate dynamic import references during traversal to prevent overlapping file-rename edits and language-server panics.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** assigned to **Copilot**, **DanielRosenwasser**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Milestone Bug`, `For Milestone Bug`, `For Milestone Bug`, `For Uncommitted Bug`, and removed label `For Milestone Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/65583#issuecomment-7021411391) **DanielRosenwasser** asked Copilot to explain why the same node might be processed twice and requested an explicit comment documenting the cause and the need to track lastNode
 * [today](https://github.com/microsoft/TypeScript/pull/65583#issuecomment-7022015958) **Copilot** explained that text scanning could match `import` or `require` at both the call and argument positions, which could resolve to the same AST node, and reported that the focused test and `npx hereby validate` passed
 * [today](https://github.com/microsoft/TypeScript/pull/65583#issuecomment-7024291477) **DanielRosenwasser** suggested testing a dynamic import involving `.default` and requested context explaining why `import` inside a string was collected
 * [today](https://github.com/microsoft/TypeScript/pull/65583#issuecomment-7024603631) **Copilot** added test context in `dd85f6110` explaining that the `import` prefix in `./imported.ts` caused the same AST node to be collected twice, and reported that the focused test and `npx hereby validate` passed

### [PR microsoft/TypeScript#65584](https://github.com/microsoft/TypeScript/pull/65584) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**\[api\] Add \`type\.isClass\(\)\` predicate guard**

*Add a `type.isClass()` predicate guard to the API for identifying class types.*

 * created by **andrewbranch**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript/pull/65584#issuecomment-7026053215) **andrewbranch** identified incorrect false-branch narrowing caused by treating class and interface types as the same `InterfaceType`, and suggested excluding the behavior from the API
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#65585](https://github.com/microsoft/TypeScript/pull/65585) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**\[api\] Checker node builder APIs**

*Expose checker APIs for building declarations, converting symbols and types to syntax, and formatting signatures and predicates.*

 * created by **andrewbranch**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#65586](https://github.com/microsoft/TypeScript/pull/65586) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**\[api\] AST utility APIs**

*Add AST utility APIs for decorator and modifier checks, ancestor lookup, node flags, formatting settings, rest parameters, and keyword identification.*

 * created by **andrewbranch**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **andrewbranch**

### [PR microsoft/TypeScript#65587](https://github.com/microsoft/TypeScript/pull/65587) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**\[api\] Diagnostic utility APIs**

*Add API utilities for flattening diagnostic messages and sorting and deduplicating diagnostics.*

 * created by **andrewbranch**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#65588](https://github.com/microsoft/TypeScript/pull/65588) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**\[api\] export existing JSDoc helpers**

*Export the existing JSDoc helper functions `getJSDocParameterTags`, `getJSDocTypeParameterTags`, and `isJSDocLinkLike` through the API.*

 * created by **andrewbranch**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#65589](https://github.com/microsoft/TypeScript/pull/65589) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**\[api\] Checker query APIs**

*Add checker and signature query APIs for retrieving symbols, type arguments, assignment pattern types, optional parameters, and property access validity.*

 * created by **andrewbranch**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#65590](https://github.com/microsoft/TypeScript/pull/65590) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**\[api\] AST predicate APIs**

*Add API predicate functions for identifying AST node categories and structures that cannot be auto-generated.*

 * created by **andrewbranch**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **andrewbranch**

### [PR microsoft/TypeScript#65591](https://github.com/microsoft/TypeScript/pull/65591) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**\[api\] Resolution utility APIs**

*Add resolution utility APIs for determining effective type roots, locating TypeScript build-info output files, and resolving type reference directives.*

 * created by **andrewbranch**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **andrewbranch**

### [PR microsoft/TypeScript#65592](https://github.com/microsoft/TypeScript/pull/65592) (Open, `For Backlog Bug`)

**Fix formatting of locationless related diagnostics**

*Fix diagnostic formatting to preserve locationless related messages and nested chains while conditionally displaying available location context.*

 * created by **TheNightCoder21**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/65592#issuecomment-7021634815) **TheNightCoder21** said "@microsoft-github-policy-service agree"

### [PR microsoft/TypeScript#65593](https://github.com/microsoft/TypeScript/pull/65593) (Closed, `For Milestone Bug`, **RyanCavanaugh**)

**Keep requested alias type arguments when instantiation leaves union/intersection members unchanged**

*Preserve requested alias type arguments during instantiation to prevent invalid declaration output when union or intersection members remain unchanged.*

 * created by **ktfth**
 * (today) **typescript-automation[bot]** added labels `For Backlog Bug`, `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/65593#issuecomment-7023282460) **ktfth** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript/pull/65593#issuecomment-7024404383) **jakebailey** suggested splitting the changes into separate commits for the failing test and baseline, followed by the fix and updated baseline
 * (today) **typescript-automation[bot]** added label `For Milestone Bug`, removed label `For Backlog Bug`, and assigned to **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript/pull/65593#issuecomment-7030479171) **RyanCavanaugh** said "Closing in favor of #65594 which has clearer baselines and maybe a second-bug-in-a-trenchcoat fix as well"
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#65594](https://github.com/microsoft/TypeScript/pull/65594) (Open, `Author: Team`, `For Uncommitted Bug`, **RyanCavanaugh**, **Copilot**)

**Fix declaration emit leaking an alias's unused type parameter \(\`Labeled\<Label\>\`\)**

*Fix declaration emit so imported union or intersection aliases preserve their supplied type arguments instead of leaking unused parameters.*

 * created by **RyanCavanaugh**
 * (today) **RyanCavanaugh** assigned to **Copilot**, **RyanCavanaugh**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Milestone Bug`, `For Uncommitted Bug`, and removed label `For Milestone Bug`

### [PR microsoft/TypeScript#65595](https://github.com/microsoft/TypeScript/pull/65595) (Open, `For Backlog Bug`)

**Reuse the written name for unique\-symbol keys when it resolves the same in the destination scope**

*Ensure declaration emit reuses written names for unique-symbol keys when they resolve consistently, avoiding invalid SymbolConstructor references and lost keys.*

 * created by **ktfth**
 * **typescript-automation[bot]** added label `For Backlog Bug`

### [Issue microsoft/TypeScript#65596](https://github.com/microsoft/TypeScript/issues/65596) (Open)

**Declaration emit drops non\-identifier expando members of a \`const\` arrow function that also has identifier members**

*Declaration emit incorrectly drops non-identifier properties from const arrow functions when identifier expando members are also present.*

 * created by **ktfth**

### [Issue microsoft/TypeScript#65597](https://github.com/microsoft/TypeScript/issues/65597) (Open, **RyanCavanaugh**, **Copilot**)

**Downlevel optional chaining loses \`this\` for parenthesized callees with \`\!\`, \`as\` or type arguments, and for parenthesized template tags**

*Downlevel optional chaining incorrectly loses the method receiver for parenthesized callees using non-null assertions, type assertions, type arguments, or template tags.*

 * created by **zloirock**

### [Issue microsoft/TypeScript#65598](https://github.com/microsoft/TypeScript/issues/65598) (Closed, `Bug`)

**Calls through \`\#private\` members lose \`this\` below ES2022 when the callee is parenthesized or has \`\!\`, \`as\` or \`satisfies\`**

*Downlevel compilation loses the correct `this` receiver for calls through `#private` methods when callees are parenthesized or type-modified.*

 * created by **zloirock**

### [PR microsoft/TypeScript#65599](https://github.com/microsoft/TypeScript/pull/65599) (Closed, `Author: Team`, `For Uncommitted Bug`)

**Update localization files**

*Update localization handbacks and regenerate their corresponding runtime artifacts.*

 * created by **typescript-automation[bot]**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`

### [Issue microsoft/TypeScript#65600](https://github.com/microsoft/TypeScript/issues/65600) (Open, **RyanCavanaugh**, **Copilot**)

**7\.0 regression: expando property on a function declaration is dropped when a merged namespace exports a type with the same name \(TS2339\)**

*TypeScript 7.0 regresses by dropping function expando properties when merged namespaces export a type with the same name, causing TS2339 errors.*

 * created by **MartinFerret**

### [Issue microsoft/TypeScript#65601](https://github.com/microsoft/TypeScript/issues/65601) (Open)

**7\.1: same package is installed twice in two connected project, TS sees only one \(get TS2883\)**

*TypeScript 7.1 incorrectly reports TS2883 when identical packages are installed in two connected projects and infers a non-portable declaration reference.*

 * created by **elevatebart**

### [PR microsoft/TypeScript#65602](https://github.com/microsoft/TypeScript/pull/65602) (Closed, `For Milestone Bug`)

**fix\(65598\): preserve this binding in wrapped private member calls**

*Ensure wrapped calls to private members preserve the correct `this` binding.*

 * created by **a-tarasyuk**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

