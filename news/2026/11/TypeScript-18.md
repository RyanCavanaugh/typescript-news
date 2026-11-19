# Report for 2026-11-18 (Wednesday, November 18th, 2026)

17 different users commented on 89 different issues.

## Recommended Actions

 * Response Recommended
    * @ssalbdivad provided impact details and a proposed module-only workaround for the recursive declaration emit failures in [microsoft/TypeScript#64752](https://github.com/microsoft/TypeScript/pull/64752#issuecomment-6989249311)
    * @mrgrain provided important benchmark data supporting server-side API methods over client-side batching in [microsoft/TypeScript#65051](https://github.com/microsoft/TypeScript/issues/65051#issuecomment-6984953311)
    * @tydavid5 provided verification that the bug reproduced on main and that the fix passed the reproduction and a new regression test in [microsoft/TypeScript#65575](https://github.com/microsoft/TypeScript/pull/65575#issuecomment-7003466885)

## Activity Summary

### [Issue microsoft/TypeScript#63040](https://github.com/microsoft/TypeScript/issues/63040) (Closed, `Bug`, `Domain: check: Type Circularity`, **ahejlsberg**)

**RangeError: Maximum call stack size exceeded in getTypeFromTypeNode when resolving recursive tuple rest with intersection**

*Recursive tuple rest intersection types cause TypeScript 5.7–nightly to crash with a maximum call stack error during type resolution.*

 * (41 weeks ago) **RyanCavanaugh** added labels `Bug`, `Domain: check: Type Circularity`, and assigned to **ahejlsberg**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#63838](https://github.com/microsoft/TypeScript/issues/63838) (Closed, `Needs Investigation`, **andrewbranch**, **Copilot**)

**RemoteNodeList inherited array methods throw this\.view\.getUint32 is not a function**

*RemoteNodeList inherited array methods such as filter fail because accessing list elements invokes an invalid view.getUint32 implementation.*

 * (22 weeks ago) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **andrewbranch**
 * **andrewbranch** assigned to **Copilot**
 * [today](https://github.com/microsoft/TypeScript/issues/63838#issuecomment-6993726815) **andrewbranch** said "Fixed in https://github.com/microsoft/typescript-go/pull/4346"
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript#63877](https://github.com/microsoft/TypeScript/issues/63877) (Closed, `Needs Investigation`, **andrewbranch**)

**\[API\] Narrow types of \`Node\` attributes when possible**

*Restore narrower, runtime-accurate TypeScript types for Node attributes, including JSDoc-related properties, in TS 7.*

 * (14 weeks ago) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.1`, and assigned to **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript#64126](https://github.com/microsoft/TypeScript/issues/64126) (Closed, `Domain: API`, **andrewbranch**)

**\`forEachChild\` is hard to use with async API**

*Improve child traversal for asynchronous APIs by preventing truthy Promises from prematurely stopping `forEachChild` and considering an async traversal alternative.*

 * (11 weeks ago) **DanielRosenwasser** added label `Domain: API`, and assigned to **andrewbranch**
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/64126#issuecomment-6744146515) **TyceHerrman** noted that #64302 added `childrenIter()` for async traversal, largely resolving the issue, and suggested splitting the remaining `forEachChild` async foot-gun concern into a new issue
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript#64182](https://github.com/microsoft/TypeScript/issues/64182) (Open, `Suggestion`, `Domain: Content Mappers`, **andrewbranch**)

**Allow content\-mappers to return declarations instead of source files**

*Allow content mappers for static data formats to return declaration files, avoiding inappropriate module-format and syntax diagnostics.*

 * [6 days ago](https://github.com/microsoft/TypeScript/issues/64182#issuecomment-6831786212) **remcohaszing** asked whether `MappedOutput['extension']` could use `.mjs`, `.cjs`, `.mts`, or `.cts` without `outputExtensions`, and said they might update `css-modules-content-mapper` to emit ESM instead of CJS
 * [6 days ago](https://github.com/microsoft/TypeScript/issues/64182#issuecomment-6832876086) **andrewbranch** clarified that `.mts`/`.mjs` and their counterparts were interchangeable based on `package.json`, as long as input and output formats agreed
 * [5 days ago](https://github.com/microsoft/TypeScript/issues/64182#issuecomment-6851386454) **remcohaszing** proposed hiding TS1295 errors from virtual content-mapper code and passing allowed extensions in transform parameters to resolve module-syntax and extension-mapping issues
 * **andrewbranch** added label `Suggestion`

### [Issue microsoft/TypeScript#64227](https://github.com/microsoft/TypeScript/issues/64227) (Closed, `Bug`, `Domain: lib.d.ts`, **RyanCavanaugh**, **Copilot**)

**The \`options\` arg of \`Temporal\.ZonedDateTime\.prototype\.toLocaleString\(\)\` currently accepts "illegal" option \`timeZone\`**

*Disallow the invalid `timeZone` option in `Temporal.ZonedDateTime.prototype.toLocaleString()` TypeScript definitions.*

 * (1 week ago) **RyanCavanaugh** assigned to **Copilot**, **RyanCavanaugh**, and unassigned **Copilot**
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#64239](https://github.com/microsoft/TypeScript/pull/64239) (Closed, `For Uncommitted Bug`, **ahejlsberg**)

**Fixed a crash related to variadic tuple elements with intersections containing \`InstantiableNonPrimitive\`**

*Fixes a crash when variadic tuple elements involve intersections containing `InstantiableNonPrimitive`.*

 * (9 weeks ago) **typescript-automation[bot]** added label `For Uncommitted Bug`, and assigned to **ahejlsberg**
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/64239#issuecomment-6940209441) **jakebailey** suggested adding a test case for the issue found in #65064 and described the differing inferred types on main versus the proposed fix
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#64483](https://github.com/microsoft/TypeScript/issues/64483) (Closed, `Needs Investigation`, **andrewbranch**)

**\`getChildren\(\)\` includes synthetic NodeObjects, that can't easily be discerned from RemoteNodes**

*getChildren() returns synthetic NodeObjects alongside RemoteNodes without an identifiable distinction, causing errors when consumers process them uniformly.*

 * created by **Qjuh**
 * (7 weeks ago) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript/issues/64483#issuecomment-6993052917) **andrewbranch** said "There's now an isRemoteNode export."
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript#64656](https://github.com/microsoft/TypeScript/issues/64656) (Closed, `Needs Investigation`, **weswigham**)

**Declaration emit errors \(TS5088\) on anonymous cyclic types that 6\.0 elided to \`any\`**

*TypeScript 7 introduces TS5088 declaration emit errors for anonymous cyclic inferred types previously serialized with elided `any`.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/64656#issuecomment-6590783155) **jakebailey** said "My opinion is that any implicit any we emitted but didn't say anything about is wrong, hence #64461, though it's a little annoying it didn't come up in our extended test suite. "
 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/64656#issuecomment-6591262979) **jakebailey** said "I am however curious if #64751 + #64752 fix the issues noted here. I haven't tested yet."
 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/64656#issuecomment-6591332401) **jakebailey** said "Ah yep, I just checked, and both of your issues are solved by that stack!"
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#64683](https://github.com/microsoft/TypeScript/issues/64683) (Closed, `Bug`, **jakebailey**, **RyanCavanaugh**, **Copilot**)

**Type printer recurses without limit into nested array/tuple types \(stack overflow; can leave later types \`any\`\)**

*Type printer infinitely recurses on nested recursive array and tuple types, causing stack overflows and potentially order-dependent type checking or `any` results.*

 * (5 weeks ago) **RyanCavanaugh** added label `Bug`, and assigned to **RyanCavanaugh**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64752](https://github.com/microsoft/TypeScript/pull/64752) (Open, `Author: Team`, `For Milestone Bug`, `For Backlog Bug`, **jakebailey**)

**Bind anonymous recursive types during declaration serialization**

*Emit owner-named private type aliases for anonymous recursive types during declaration serialization, preserving captured type parameters and avoiding failures or any fallbacks.*

 * (2 weeks ago) **typescript-automation[bot]** added labels `For Backlog Bug`, `For Milestone Bug`, and removed label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64752#issuecomment-6989249311) **ssalbdivad** argued for synthesizing aliases only in modules while preserving TS5088 for global scripts, explained that module-local aliases avoid collisions, and reported that recursive exported scopes currently fail declaration emit in TypeScript 7.1 without manual interface annotations
 * [today](https://github.com/microsoft/TypeScript/pull/64752#issuecomment-6989600097) **jakebailey** explained that the 7.1 release branch had been cut, making it unlikely the PR would land beforehand, and said breaking PRs might need to be reverted despite the frustration of preserving silent `any` behavior

### [Issue microsoft/TypeScript#64859](https://github.com/microsoft/TypeScript/issues/64859) (Closed, `Bug`, **andrewbranch**, **RyanCavanaugh**, **Copilot**)

**\[API\] Printer attaches source comments to synthesized nodes because the node encoder sends pos \-1 as 0**

*The TypeScript printer incorrectly attaches source comments to synthesized nodes because the node encoder converts their -1 positions to 0.*

 * (1 month ago) **RyanCavanaugh** set milestone to `TypeScript 7.1.1 RC`, and assigned to **Copilot**, **RyanCavanaugh**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#64903](https://github.com/microsoft/TypeScript/pull/64903) (Closed, `Author: Team`, `For Uncommitted Bug`, **RyanCavanaugh**, **Copilot**)

**Preserve synthesized node ranges across API serialization**

*Preserve synthesized node ranges during API serialization to prevent misplaced or duplicated source comments in printed output.*

 * (1 month ago) **typescript-automation[bot]** added labels `For Milestone Bug`, `For Uncommitted Bug`, and removed label `For Milestone Bug`
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript#64930](https://github.com/microsoft/TypeScript/issues/64930) (Open, `Bug`, **ahejlsberg**)

**7\.1 regression: circular type alias accepts an assignment it should reject \(opposite of \#64891\)**

*TypeScript 7.1 regresses by allowing incompatible circular generic handler assignments that should produce TS2322 errors.*

 * (3 weeks ago) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/64930#issuecomment-6982595670) **Sipixer** reported that version 7.1 also broke untyped `@tanstack/db` collections by inferring `Collection<never, …>`, provided a reproduction showing thousands of production errors, and confirmed the issue persisted in the latest nightly after #65030
 * **RyanCavanaugh** assigned to **ahejlsberg**

### [PR microsoft/TypeScript#64935](https://github.com/microsoft/TypeScript/pull/64935) (Open, `For Milestone Bug`, **ahejlsberg**)

**Don't measure type parameters as independent through circular variance lookups**

*Fix circular variance measurement so mutually recursive type aliases reject incompatible type arguments without misclassifying parameters as independent.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript/pull/64935#issuecomment-6386813789) **typescript-automation[bot]** reported changes from comparing baseline and PR TypeScript compiler results across the top 400 repositories, including new build errors in RSSHub and open-seo, and requested review
 * (3 weeks ago) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`
 * (today) **typescript-automation[bot]** added label `For Milestone Bug`, removed label `For Backlog Bug`, and assigned to **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript/pull/64935#issuecomment-6988358959) **microsoft-github-policy-service[bot]** asked @jasleenkaur-qed42 to review the Contributor License Agreement and reply with the appropriate agreement command

### [PR microsoft/TypeScript#65041](https://github.com/microsoft/TypeScript/pull/65041) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Avoid closure and slice allocations in core helpers and type filtering**

*Optimize core helpers and type filtering to eliminate unnecessary closure and slice allocations.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/65041#issuecomment-6509798630) **typescript-automation[bot]** reported that the performance test job started and linked to its results
 * **jakebailey** added label `Domain: Performance`
 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/65041#issuecomment-6510939371) **typescript-automation[bot]** reported the requested performance run results and included a baseline-versus-PR comparison report
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#65043](https://github.com/microsoft/TypeScript/pull/65043) (Open, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Speed up property and index signature lookups**

*Improve the performance of property and index signature lookups.*

 * **jakebailey** added label `Domain: Performance`
 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/65043#issuecomment-6511137405) **typescript-automation[bot]** reported the requested performance results comparing the baseline and pull request, including compiler metrics and statistical deltas
 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/65043#issuecomment-6531267073) **jakebailey** said "FWIW this looks way better if you view each commit without whitespace, or at least the whole thing https://github.com/microsoft/TypeScript/pull/65043/changes?w=1"
 * [today](https://github.com/microsoft/TypeScript/pull/65043#issuecomment-6986758367) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/65043#issuecomment-6986760760) **typescript-automation[bot]** reported that the performance test job started and linked to its build results
 * [today](https://github.com/microsoft/TypeScript/pull/65043#issuecomment-6987783689) **typescript-automation[bot]** provided the requested performance run results comparing the baseline and PR

### [Issue microsoft/TypeScript#65051](https://github.com/microsoft/TypeScript/issues/65051) (Open, `Suggestion`)

**API: coarse\-grained checker queries for tools that extract a whole API surface \(\`getSymbolDocumentations\`, \`getMembersOfType\`\)**

*Add bulk checker APIs for symbol documentation and type-member metadata to reduce round trips and improve out-of-process API extraction performance.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/65051#issuecomment-6518847399) **aetherxeg-source** proposed adding a differential regression fixture to compare fine-grained and coarse-grained member traversal, covering inheritance, overloads, visibility, filtering, metadata, and ordering
 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/65051#issuecomment-6519041664) **WinterYukky** said "Thanks, good suggestion. I'll add a differential fixture comparing both paths on the same program to the PR."
 * **RyanCavanaugh** added label `Suggestion`
 * [today](https://github.com/microsoft/TypeScript/issues/65051#issuecomment-6984953311) **mrgrain** provided benchmark data showing that client-side batching and caching halved requests without improving wall time, while server-side member traversal reduced both requests and build time; identified remaining per-member calls that could be covered by the proposed declaring-type field

### [PR microsoft/TypeScript#65064](https://github.com/microsoft/TypeScript/pull/65064) (Open, `Author: Team`, `For Milestone Bug`, `For Backlog Bug`, **jakebailey**)

**\[experiment\] fully order independent type checking**

*Proposes making type checking fully order-independent, with randomized ordering tests and extensive fixes for cache, traversal, and identifier-dependent behavior.*

 * [2 days ago](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6934396913) **typescript-automation[bot]** reported new TypeScript errors found when comparing user test results between the baseline and pull request, and asked Jake Bailey to investigate
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6935291785) **typescript-automation[bot]** said "@jakebailey, the perf run you requested failed. You can check the log here."
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6936707599) **typescript-automation[bot]** reported unexpected baseline-versus-PR `tsc` changes found while testing the top 1,000 repositories and asked @jakebailey to investigate
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6992917606) **jakebailey** requested several TypeScript bot tests, including DT, user, top-1000, and performance tests
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6992919964) **typescript-automation[bot]** reported that automated DT, user, top-1000, and performance tests had started, with links to build and available results
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6993529747) **typescript-automation[bot]** reported that the DT tests produced a new d3-selection type-checking error in d3-selection-tests.ts at line 1502
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6993569229) **typescript-automation[bot]** reported new TypeScript TS7023 errors in Effect's SchemaAST.ts from the baseline-versus-PR user-test comparison and requested investigation
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6993846052) **typescript-automation[bot]** provided the requested performance results, showing increased symbols and memory usage in the Compiler-Unions benchmark

### [PR microsoft/TypeScript#65286](https://github.com/microsoft/TypeScript/pull/65286) (Open, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Negated Types: Remove the concept of control\-flow made "fresh" negations**

*Enable full negated types in control-flow analysis instead of transient fresh negations, while addressing impacts on exact matching and performance.*

 * (2 weeks ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **weswigham**
 * [today](https://github.com/microsoft/TypeScript/pull/65286#issuecomment-6991687631) **weswigham** said "@typescript-bot test this"
 * [today](https://github.com/microsoft/TypeScript/pull/65286#issuecomment-6991689459) **typescript-automation[bot]** said "Hey @weswigham, this PR is in an unmergable state, so is missing a merge commit to run against; please resolve conflicts and try again."

### [PR microsoft/TypeScript#65291](https://github.com/microsoft/TypeScript/pull/65291) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Add order dependence tests**

*Add checker ordering tests and fuzzing to detect and preserve fixes for order-dependent analysis failures.*

 * (2 weeks ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/65291#issuecomment-6993015348) **jakebailey** said "Okay, I think now this is ready to go in."

### [PR microsoft/TypeScript#65296](https://github.com/microsoft/TypeScript/pull/65296) (Open, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Negated Types: Consider assertions invertible and create negated narrowings in false branches of assertion narrowings**

*Consider whether assertion narrowings should produce negated types in false branches, despite unsoundness when guards are less specific than their checks.*

 * (2 weeks ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **weswigham**
 * [today](https://github.com/microsoft/TypeScript/pull/65296#issuecomment-6991685752) **weswigham** said "@typescript-bot test this"
 * [today](https://github.com/microsoft/TypeScript/pull/65296#issuecomment-6991687540) **typescript-automation[bot]** said "Hey @weswigham, this PR is in an unmergable state, so is missing a merge commit to run against; please resolve conflicts and try again."

### [PR microsoft/TypeScript#65298](https://github.com/microsoft/TypeScript/pull/65298) (Open, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Negated Types: Remove the \`TypeFacts\` abstraction and make type refinements directly**

*Refactor negated types to remove the TypeFacts abstraction and implement type refinements directly, while evaluating performance implications.*

 * (2 weeks ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **weswigham**
 * [today](https://github.com/microsoft/TypeScript/pull/65298#issuecomment-6991690889) **weswigham** said "@typescript-bot test this"
 * [today](https://github.com/microsoft/TypeScript/pull/65298#issuecomment-6991692786) **typescript-automation[bot]** said "Hey @weswigham, this PR is in an unmergable state, so is missing a merge commit to run against; please resolve conflicts and try again."

### [PR microsoft/TypeScript#65318](https://github.com/microsoft/TypeScript/pull/65318) (Closed, `Author: Team`, `For Uncommitted Bug`, **RyanCavanaugh**, **Copilot**)

**Assert checker errors cannot use the Message diagnostic category**

*Ensure checker assertions reject Message-category error diagnostics while preserving legitimate Message-category related information.*

 * (2 weeks ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/65318#issuecomment-6665469711) **Copilot** removed the added test file in commit 3570fb409 while leaving the assertion unchanged
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#65342](https://github.com/microsoft/TypeScript/pull/65342) (Closed, `Author: Team`, `For Uncommitted Bug`, **RyanCavanaugh**)

**Fix crash in path completions for URLs with a query or fragment**

*Prevent path completion crashes when URL queries or fragments appear in module specifiers or script directories.*

 * (1 week ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **RyanCavanaugh**
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#65396](https://github.com/microsoft/TypeScript/issues/65396) (Closed, `Bug`, `Domain: JSX/TSX`, **RyanCavanaugh**, **Copilot**)

**JSX tag and attribute names starting with \`\#\` are accepted without a syntax error**

*JSX incorrectly accepts tag and attribute names beginning with `#`, producing missing syntax errors and invalid JavaScript output.*

 * (1 week ago) **RyanCavanaugh** set milestone to `Backlog`, and assigned to **Copilot**, **RyanCavanaugh**
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#65431](https://github.com/microsoft/TypeScript/pull/65431) (Closed, `Author: Team`, `For Uncommitted Bug`, **RyanCavanaugh**, **Copilot**)

**Report TS1003 for JSX tag and attribute names starting with \`\#\`**

*Ensure JSX tag, attribute, and namespaced names beginning with `#` report TS1003 instead of parsing and emitting invalid JavaScript.*

 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/65431#issuecomment-6776910218) **RyanCavanaugh** asked to simplify the PR because cascading parse errors from an unlikely syntax pattern did not violate an invariant
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/65431#issuecomment-6777309425) **Copilot** explained that the scanner fix was simplified to leave private JSX identifiers untouched, allowing removal of the astnav rescan workaround and related tests while retaining the parser change and compiler test
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#65434](https://github.com/microsoft/TypeScript/pull/65434) (Closed, `Author: Team`, `For Uncommitted Bug`, **RyanCavanaugh**, **Copilot**)

**Disallow \`timeZone\` option in \`Temporal\.ZonedDateTime\.prototype\.toLocaleString\`**

*Update Temporal ZonedDateTime.toLocaleString typings to reject unsupported timeZone options while preserving valid formatting options and behavior for other Temporal types.*

 * (1 week ago) **typescript-automation[bot]** added labels `For Milestone Bug`, `For Uncommitted Bug`, and removed label `For Milestone Bug`
 * (today) **RyanCavanaugh** closed the issue
 * (today) **RyanCavanaugh** reopened the issue
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#65487](https://github.com/microsoft/TypeScript/pull/65487) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Update DOM types**

*Update DOM library types with the latest web platform APIs, interfaces, options, and compatibility changes across browser features.*

 * [5 days ago](https://github.com/microsoft/TypeScript/pull/65487#issuecomment-6863278120) **typescript-automation[bot]** reported that user tests comparing the baseline and PR with tsc passed successfully
 * [5 days ago](https://github.com/microsoft/TypeScript/pull/65487#issuecomment-6863495358) **typescript-automation[bot]** reported that the requested performance run results were available and included comparison data
 * [5 days ago](https://github.com/microsoft/TypeScript/pull/65487#issuecomment-6864140353) **typescript-automation[bot]** reported changed tsc results from comparing the baseline and PR across the top 400 repositories, highlighting new VS Code build errors for review
 * [today](https://github.com/microsoft/TypeScript/pull/65487#issuecomment-6993200129) **jakebailey** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/65487#issuecomment-6993202285) **typescript-automation[bot]** reported that automated test jobs had started and linked to their build and result statuses
 * [today](https://github.com/microsoft/TypeScript/pull/65487#issuecomment-6993867424) **typescript-automation[bot]** reported DT test results showing branch-only declaration conflicts in dom-webcodecs and dom-speech-recognition
 * [today](https://github.com/microsoft/TypeScript/pull/65487#issuecomment-6993926110) **typescript-automation[bot]** reported that user tests comparing the baseline and PR with tsc passed successfully
 * [today](https://github.com/microsoft/TypeScript/pull/65487#issuecomment-6994198430) **typescript-automation[bot]** provided the requested performance-run results comparing the baseline and PR, including tsc metrics
 * [today](https://github.com/microsoft/TypeScript/pull/65487#issuecomment-6995260591) **typescript-automation[bot]** reported results from comparing baseline and PR builds across the top 400 repositories, highlighting changed TypeScript errors in VS Code involving an undefined MutationObserverInit value

### [PR microsoft/TypeScript#65496](https://github.com/microsoft/TypeScript/pull/65496) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Return a missing identifier from parseDecoratedExpression when no class follows**

*Correct parseDecoratedExpression to return a missing identifier, not a declaration, when no class follows.*

 * (5 days ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#65502](https://github.com/microsoft/TypeScript/pull/65502) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Stop building invalid type syntax for hover and code fixes**

*Stop generating invalid AST type syntax by storing hover and code-fix type arguments in emit context and updating related APIs and behavior.*

 * (5 days ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#65510](https://github.com/microsoft/TypeScript/pull/65510) (Open, `Domain: Performance`, `For Milestone Bug`, `For Backlog Bug`, **johnfav03**)

**Reject structurally incomplete type arguments in expressions**

*Reject structurally incomplete speculative type arguments so relational expressions parse correctly while preserving valid generics, diagnostics, and parser performance.*

 * (3 days ago) **typescript-automation[bot]** added label `For Milestone Bug`, and assigned to **johnfav03**
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/65510#issuecomment-6936175496) **magic-akari** acknowledged that the implementation was more complex than expected because it needed to preserve TypeScript’s error recovery and invalid-input compatibility
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#65511](https://github.com/microsoft/TypeScript/pull/65511) (Closed, `Domain: Performance`, `For Backlog Bug`)

**fix: share in\-flight getSourceFile requests in native\-preview async API \(\#65503\)**

*Share concurrent native-preview `getSourceFile` requests per path to prevent redundant server fetches while allowing retries after failures.*

 * [3 days ago](https://github.com/microsoft/TypeScript/pull/65511#issuecomment-6894375032) **zhengdaodeguL** said "@microsoft-github-policy-service agree"
 * (yesterday) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`
 * **jakebailey** added label `Domain: Performance`
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#65512](https://github.com/microsoft/TypeScript/pull/65512) (Closed, `For Backlog Bug`)

**fix: deduplicate rename edits for dynamic imports with \.ts specifiers**

*Deduplicate duplicate dynamic-import rename edits for `.ts` specifiers to prevent language server overlap panics.*

 * (3 days ago) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Backlog Bug`, and removed label `For Uncommitted Bug`
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#65515](https://github.com/microsoft/TypeScript/pull/65515) (Closed, `For Backlog Bug`)

**fix: resolve JSDoc '\#' links to instance members**

*Fix JSDoc `#` links to resolve instance members instead of static members, matching TS 6 behavior and adding regression coverage.*

 * (3 days ago) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Backlog Bug`, and removed label `For Uncommitted Bug`
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#65518](https://github.com/microsoft/TypeScript/pull/65518) (Closed, `For Backlog Bug`)

**Exempt declare redeclarations from TS2729 use\-before\-init check**

*Exclude ambient `declare` redeclarations from TS2729 use-before-initialization errors while preserving checks for ordinary redeclarations.*

 * (3 days ago) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Backlog Bug`, and removed label `For Uncommitted Bug`
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#65519](https://github.com/microsoft/TypeScript/pull/65519) (Closed, `For Backlog Bug`)

**Fix object rest for\-of lowering skipping direct body statement transformation**

*Fix for-of lowering to transform direct body statements, correctly handling nested object-rest loops and function declarations for pre-ES2018 targets.*

 * (3 days ago) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Backlog Bug`, and removed label `For Uncommitted Bug`
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#65520](https://github.com/microsoft/TypeScript/pull/65520) (Closed, `For Backlog Bug`)

**Fix indexed\-access base constraint losing explicit bound across checker histories**

*Fix retained-checker history bug where indexed-access base constraints lose explicit bounds, causing order-dependent false TS2339 errors.*

 * (3 days ago) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Backlog Bug`, and removed label `For Uncommitted Bug`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#65525](https://github.com/microsoft/TypeScript/issues/65525) (Closed, `Bug`, **andrewbranch**, **Copilot**)

**Missing content\-mapper fallbacks cause internal LSP errors**

*Unknown script kinds without content-mapper fallbacks trigger internal LSP errors across requests for unsupported documents such as Vue files.*

 * (yesterday) **RyanCavanaugh** set milestone to `TypeScript 7.1.1 RC`, and assigned to **andrewbranch**
 * **andrewbranch** assigned to **Copilot**
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript#65526](https://github.com/microsoft/TypeScript/issues/65526) (Open, `Bug`, `Domain: LS: Symbol Navigation`, **DanielRosenwasser**, **Copilot**)

**Duplicate callsite ranges for a single method call in callHierarchy/outgoingCalls**

*TypeScript 7.x reports duplicate callsite ranges for a single interface method invocation in callHierarchy/outgoingCalls.*

 * (yesterday) **RyanCavanaugh** added label `Domain: LS: Symbol Navigation`, and set milestone to `Backlog`
 * [yesterday](https://github.com/microsoft/TypeScript/issues/65526#issuecomment-6960686114) **zhengdaodeguL** reported that #65553 fixed duplicate call-site recording by preventing repeated targets and added regression tests for outgoing and incoming calls
 * (today) **DanielRosenwasser** assigned to **Copilot**, **DanielRosenwasser**

### [PR microsoft/TypeScript#65529](https://github.com/microsoft/TypeScript/pull/65529) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **ahejlsberg**)

**Optimize \`getPropertiesOfUnionOrIntersectionType\`**

*Optimize union property resolution by using the constituent with the fewest properties and no index signatures as the representative.*

 * [2 days ago](https://github.com/microsoft/TypeScript/pull/65529#issuecomment-6931106373) **typescript-automation[bot]** reported that the performance test job started and linked to its results
 * (2 days ago) **ahejlsberg** closed the issue
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/65529#issuecomment-6931828087) **typescript-automation[bot]** provided the requested performance run results comparing the baseline and PR, including compiler metrics
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#65544](https://github.com/microsoft/TypeScript/pull/65544) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**, **RyanCavanaugh**)

**Bound printing of deferred array and tuple references by their node**

*Ensure deferred array and tuple type references are bounded by their node after type references are checked first.*

 * (2 days ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **RyanCavanaugh**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#65546](https://github.com/microsoft/TypeScript/pull/65546) (Closed, `For Backlog Bug`)

**Fix contextual typing loss for computed string keys under circular mapped\-type key constraints \(Fixes \#65530\)**

*Fix contextual typing for computed string keys by preventing circular mapped-type constraints from generating spurious undefined index signatures.*

 * (2 days ago) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Backlog Bug`, and removed label `For Uncommitted Bug`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#65547](https://github.com/microsoft/TypeScript/issues/65547) (Closed, `Bug`, `Domain: Content Mappers`, **DanielRosenwasser**, **Copilot**)

**LSP panics with "slice bounds out of range" after a content mapper fails**

*The LSP panics with a slice-bounds error when handling hover or inlay hints after a content mapper fails during project opening.*

 * created by **auvred**
 * (yesterday) **DanielRosenwasser** assigned to **Copilot**, **DanielRosenwasser**
 * (today) **RyanCavanaugh** added labels `Bug`, `Domain: Content Mappers`
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript#65548](https://github.com/microsoft/TypeScript/pull/65548) (Open, `Domain: Performance`, `For Uncommitted Bug`)

**Skip the combined\-constraint check for a dedicated variance relationship**

*Introduce a dedicated variance-assignability relationship to prevent unbounded combined-constraint recursion and out-of-memory failures during variance measurement.*

 * created by **Amatewasu**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * **jakebailey** added label `Domain: Performance`

### [Issue microsoft/TypeScript#65549](https://github.com/microsoft/TypeScript/issues/65549) (Open, `Bug`)

**TS7 fails assign type predicates via the JSDoc \`@type\` tag to functions without an explicit \`function\` keyword**

*TypeScript 7 fails to infer JSDoc `@type`-annotated arrow functions as type predicates when their bodies contain compound checks.*

 * created by **bananarama92**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/65549#issuecomment-6967157953) **zhengdaodeguL** asked maintainers to assign a milestone so a proposed fix could be submitted as a PR
 * (today) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`

### [PR microsoft/TypeScript#65551](https://github.com/microsoft/TypeScript/pull/65551) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Omit DWARF from race\-instrumented test archives**

*Omit DWARF debug information from race-instrumented test archives to prevent race-mode CI jobs from exhausting disk space.*

 * (yesterday) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`
 * (yesterday) **jakebailey** closed the issue
 * (today) **jakebailey** added label `Domain: Performance`, and removed label `Domain: Performance`

### [PR microsoft/TypeScript#65552](https://github.com/microsoft/TypeScript/pull/65552) (Closed, `For Backlog Bug`)

**Ignore the synthetic this parameter when matching JSDoc params \(Fixes \#65524\)**

*Fix positional JSDoc parameter matching to ignore synthetic or explicit leading `this` parameters, preventing erroneous TS8024 and TS7031 errors.*

 * created by **zhengdaodeguL**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#65553](https://github.com/microsoft/TypeScript/pull/65553) (Closed, `For Backlog Bug`)

**Fix duplicate fromRanges for method calls in call hierarchy outgoing calls**

*Deduplicate duplicate fromRanges in outgoing call hierarchy results by preventing repeated recording of the same call-site target.*

 * created by **zhengdaodeguL**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#65554](https://github.com/microsoft/TypeScript/pull/65554) (Closed, `Author: Team`, `For Uncommitted Bug`, **DanielRosenwasser**, **Copilot**)

**Prevent LSP position\-conversion panic after content mapper failure**

*Clamp LSP position conversions to failed content mappers’ available virtual text to prevent hover and inlay-hint panics.*

 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [yesterday](https://github.com/microsoft/TypeScript/pull/65554#issuecomment-6962177062) **DanielRosenwasser** said "@copilot fix"
 * [yesterday](https://github.com/microsoft/TypeScript/pull/65554#issuecomment-6962692796) **Copilot** explained the regression cause, documented the test coverage, and reported that the fix and validation passed
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript#65557](https://github.com/microsoft/TypeScript/pull/65557) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**, **Copilot**)

**Add missing content\-mapper LSP fallbacks**

*Add missing language server protocol fallbacks for content-mapper functionality.*

 * (yesterday) **typescript-automation[bot]** added labels `For Milestone Bug`, `For Uncommitted Bug`, and removed label `For Milestone Bug`
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript#65558](https://github.com/microsoft/TypeScript/issues/65558) (Open, `Working as Intended`)

**TS7 JSDoc \`@overload\` is ignored on \`const\` arrow function \(works in 6\.0\.2, not in 7\.0\.2\)**

*TypeScript 7.0.2 regresses by ignoring JSDoc `@overload` annotations on `const` arrow functions, unlike function declarations and TypeScript 6.0.3.*

 * created by **abc-abc-ab**
 * [today](https://github.com/microsoft/TypeScript/issues/65558#issuecomment-6977922609) **zhengdaodeguL** asked a maintainer to assign a milestone to the issue before submitting a pull request
 * [today](https://github.com/microsoft/TypeScript/issues/65558#issuecomment-6984746122) **RyanCavanaugh** said "https://github.com/microsoft/TypeScript/blob/e086ad3b8205668290a81baed890c536047003db/tsc/CHANGES.md?plain=1#L325"
 * **RyanCavanaugh** added label `Working as Intended`

### [Issue microsoft/TypeScript#65559](https://github.com/microsoft/TypeScript/issues/65559) (Open, `Not a Defect`)

**Fix: small edits reshuffle the \`\-\-checkers\` partition**

*Small file edits unpredictably reshuffle checker assignments, causing check-time variance; quantizing file weights is proposed to stabilize partitioning.*

 * created by **ubugeeei**
 * **RyanCavanaugh** added label `Not a Defect`
 * [today](https://github.com/microsoft/TypeScript/issues/65559#issuecomment-6984291729) **RyanCavanaugh** clarified that the proposed fix still allowed a one-node change to move a file and alter subsequent assignments, so no invariant could be maintained

### [Issue microsoft/TypeScript#65560](https://github.com/microsoft/TypeScript/issues/65560) (Open, `Bug`, **RyanCavanaugh**, **Copilot**)

**Aliased \`Partial\<{ … }\>\` is duplicated when instantiated again: quadratic inference, spurious TS2859, repeated union members**

*Aliased `Partial` object types are duplicated during instantiation, causing quadratic inference, spurious TS2859 errors, and repeated union members.*

 * created by **GabrielVidal1**
 * (today) **RyanCavanaugh** added label `Bug`, set milestone to `Backlog`, and assigned to **Copilot**, **RyanCavanaugh**

### [PR microsoft/TypeScript#65561](https://github.com/microsoft/TypeScript/pull/65561) (Closed, `For Backlog Bug`)

**Fix checker crash when async iteration awaits an invalid thenable**

*Fix checker crashes when async iteration awaits invalid thenables, ensuring correct diagnostics for yield*, for-await, unions, and repeated conversions.*

 * created by **zhengdaodeguL**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#65562](https://github.com/microsoft/TypeScript/pull/65562) (Open, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **RyanCavanaugh**, **Copilot**)

**Cache homomorphic mapped type constituent instantiations under their re\-instantiation key**

*Cache homomorphic mapped type constituent instantiations under re-instantiation keys to eliminate duplicate types, improve inference performance, and prevent spurious TS2859 errors.*

 * created by **RyanCavanaugh**
 * (today) **RyanCavanaugh** assigned to **Copilot**, **RyanCavanaugh**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Milestone Bug`, `For Milestone Bug`, `For Uncommitted Bug`, and removed label `For Milestone Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/65562#issuecomment-6986011832) **RyanCavanaugh** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/65562#issuecomment-6986014771) **typescript-automation[bot]** reported that the requested test and performance jobs started, with three succeeding and the faster performance test failing
 * **jakebailey** added label `Domain: Performance`
 * [today](https://github.com/microsoft/TypeScript/pull/65562#issuecomment-6986664590) **typescript-automation[bot]** reported that the DT test results were ready and unchanged, with a link to the log
 * [today](https://github.com/microsoft/TypeScript/pull/65562#issuecomment-6986734271) **typescript-automation[bot]** reported that user tests comparing the baseline and PR with tsc passed without issues
 * [today](https://github.com/microsoft/TypeScript/pull/65562#issuecomment-6988021968) **typescript-automation[bot]** reported that testing the top 400 repositories with tsc showed no differences between the baseline and PR, with everything looking good
 * [today](https://github.com/microsoft/TypeScript/pull/65562#issuecomment-6988174683) **typescript-automation[bot]** said "@RyanCavanaugh, the perf run you requested failed. You can check the log here."
 * [today](https://github.com/microsoft/TypeScript/pull/65562#issuecomment-6988327349) **RyanCavanaugh** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/65562#issuecomment-6988329920) **typescript-automation[bot]** reported that the performance test job started and linked to its build results
 * [today](https://github.com/microsoft/TypeScript/pull/65562#issuecomment-6988503615) **DanielRosenwasser** said "Okay but why weren't the types reduced on union construction?"
 * [today](https://github.com/microsoft/TypeScript/pull/65562#issuecomment-6989651778) **typescript-automation[bot]** reported that the requested performance run results were available and included comparison metrics for the compiler-unions scenario

### [Issue microsoft/TypeScript#65563](https://github.com/microsoft/TypeScript/issues/65563) (Closed)

**API: checker queries are answered on one core**

*Enable TypeScript checker API queries to execute concurrently across multiple cores, reducing latency for tools issuing large numbers of requests.*

 * created by **stacks-the-beaver**
 * (today) **stacks-the-beaver** closed the issue

### [Issue microsoft/TypeScript#65564](https://github.com/microsoft/TypeScript/issues/65564) (Closed, `Question`, **andrewbranch**)

**API: checker queries are answered on one core**

*Enable TypeScript checker API queries to execute concurrently across multiple cores, reducing latency for tools issuing large numbers of requests.*

 * created by **mrgrain**
 * (today) **RyanCavanaugh** added label `Question`, and assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript/issues/65564#issuecomment-6989010310) **andrewbranch** explained that the current checker architecture could not support concurrent requests because checkers were not concurrency-safe and lazily owned interconnected types and symbols requiring all snapshot requests to use the same checker
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#65565](https://github.com/microsoft/TypeScript/pull/65565) (Open, `Author: Team`, `For Uncommitted Bug`, **gabritto**)

**Generate content mapper types from json schema**

*Introduce a JSON schema and generation script for content mapper protocol types, enabling typed implementations and validation across languages.*

 * created by **gabritto**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **gabritto**

### [PR microsoft/TypeScript#65566](https://github.com/microsoft/TypeScript/pull/65566) (Open, `Author: Team`, `For Uncommitted Bug`, **DanielRosenwasser**, **Copilot**)

**Deduplicate call hierarchy call\-site ranges**

*Deduplicate duplicate call-site ranges in call hierarchy results while preserving distinct occurrences, with regression coverage for interface method calls.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** assigned to **Copilot**, **DanielRosenwasser**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Milestone Bug`, `For Uncommitted Bug`, and removed label `For Milestone Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/65566#issuecomment-6996059013) **DanielRosenwasser** explained that `recordCallSite` could add the same node twice and proposed exempting the current child node or adding an exception for call-like parent expressions
 * [today](https://github.com/microsoft/TypeScript/pull/65566#issuecomment-6996434011) **Copilot** reported updating the collector to prevent duplicate property/element access records, removing outgoing-range compaction, and passing focused and full validation

### [PR microsoft/TypeScript#65567](https://github.com/microsoft/TypeScript/pull/65567) (Closed, `Author: Team`, `For Milestone Bug`, **weswigham**, **jakebailey**)

**Revert "Report cyclic structures and truncation during declaration emit"**

*Revert declaration emit errors for cyclic structures and truncation because they introduced breaking changes for valid inferred recursive types.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Milestone Bug`, `For Milestone Bug`, and assigned to **jakebailey**, **weswigham**
 * [today](https://github.com/microsoft/TypeScript/pull/65567#issuecomment-6991090649) **jakebailey** expressed uncertainty about mitigating the breaks, noted a tentative PR introducing names, and deferred to a potentially better long-term approach
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#65568](https://github.com/microsoft/TypeScript/issues/65568) (Open)

**7\.0 regression: \-\-generateTrace runs out of memory on type\-fest's merge\-deep\.d\.ts \(6 GB\+, 5\.9 needs 442 MB\)**

*TypeScript 7.0’s --generateTrace causes extreme memory usage and crashes when tracing type-fest’s merge-deep.d.ts, unlike 5.9.*

 * created by **MartinFerret**

### [PR microsoft/TypeScript#65569](https://github.com/microsoft/TypeScript/pull/65569) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Fix kqueue file watcher test failing on macOS**

*Fix the macOS kqueue watcher test by passing the full watch list when pausing or resuming notifications to prevent timeouts.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#65570](https://github.com/microsoft/TypeScript/issues/65570) (Open)

**Declaration emit writes an alias's own type parameter \(\`Labeled\<Label\>\`\) instead of the type argument when the parameter is unused**

*Declaration emit incorrectly replaces an unused type alias argument with the alias’s own type parameter, producing invalid out-of-scope `.d.ts` files.*

 * created by **ktfth**

### [Issue microsoft/TypeScript#65571](https://github.com/microsoft/TypeScript/issues/65571) (Open)

**Declaration emit drops the normalized optional properties of a union of object literals \(\`retries?: undefined\`\)**

*Declaration emit in TypeScript 7.x drops normalized optional properties from unions of object literals, causing consumers to incorrectly reject valid property access.*

 * created by **ktfth**

### [PR microsoft/TypeScript#65572](https://github.com/microsoft/TypeScript/pull/65572) (Closed, `Author: Team`, `For Milestone Bug`, **andrewbranch**)

**Update types for SourceFile\.jsDoc and JSDocTypeDefTag\.typeExpression**

*Update SourceFile.jsDoc and JSDocTypeDefTag.typeExpression types to accurately reflect their possible AST node values.*

 * created by **andrewbranch**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Milestone Bug`, and assigned to **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#65573](https://github.com/microsoft/TypeScript/pull/65573) (Open, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**Filter out more diagnostics from content mapper synthesized code**

*Filter verbatimModuleSyntax and isolatedModules diagnostics from synthesized content-mapper code while retaining them within user-authored verbatim ranges.*

 * created by **andrewbranch**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`, and assigned to **andrewbranch**

### [Issue microsoft/TypeScript#65574](https://github.com/microsoft/TypeScript/issues/65574) (Open)

**7\.1 regression: type argument inferred from a union of callback types \(\`R\` \| \`Promise\<R \| void\>\`\) falls back to its constraint**

*TypeScript 7.1 regresses generic inference for unioned callback return types, falling back to the constraint and losing precise route response types.*

 * created by **kazu-42**

### [PR microsoft/TypeScript#65575](https://github.com/microsoft/TypeScript/pull/65575) (Closed, `For Backlog Bug`)

**Fix contextual typing loss for computed string keys under circular mapped\-type key constraints**

*Fix a regression where circular mapped-type key constraints create a spurious string index signature that causes computed-key callback parameters to lose contextual typing.*

 * created by **tydavid5**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/65575#issuecomment-7003466885) **tydavid5** noted that the change followed the approach from #65546, reproduced the bug on main, and verified the fix with the reproduction and a new regression test
 * [later](https://github.com/microsoft/TypeScript/pull/65575#issuecomment-7003521836) **tydavid5** said "@microsoft-github-policy-service agree"

### [PR microsoft/TypeScript#65576](https://github.com/microsoft/TypeScript/pull/65576) (Closed, `For Backlog Bug`)

**Ignore the synthetic this parameter when matching JSDoc params**

*Fix JSDoc parameter matching to ignore leading synthetic or explicit `this` parameters and prevent incorrect TS7031 and TS8024 errors.*

 * created by **tydavid5**
 * **typescript-automation[bot]** added label `For Backlog Bug`

### [PR microsoft/TypeScript#65577](https://github.com/microsoft/TypeScript/pull/65577) (Closed, `For Backlog Bug`)

**Allow declare redeclarations of inherited properties in field initializers**

*Allow inherited properties redeclared with `declare` in field initializers without triggering TS2729, while preserving errors for actual overwrites and invalid references.*

 * created by **tydavid5**
 * **typescript-automation[bot]** added label `For Backlog Bug`

### [PR microsoft/TypeScript#65578](https://github.com/microsoft/TypeScript/pull/65578) (Closed, `For Backlog Bug`)

**Fix object\-rest lowering for statements directly in a for\-of body**

*Fix object-rest lowering so nested for-of loops and function declarations directly in loop bodies are correctly transformed and executed.*

 * created by **tydavid5**
 * **typescript-automation[bot]** added label `For Backlog Bug`

### [PR microsoft/TypeScript#65579](https://github.com/microsoft/TypeScript/pull/65579) (Closed, `For Backlog Bug`)

**Preserve U\+FEFF when Wtf8Decoder reads payload text**

*Preserve leading and surrogate-adjacent U+FEFF characters in Wtf8Decoder payloads by default while retaining explicit BOM-stripping opt-out behavior.*

 * created by **tydavid5**
 * **typescript-automation[bot]** added label `For Backlog Bug`

### [PR microsoft/TypeScript#65580](https://github.com/microsoft/TypeScript/pull/65580) (Closed, `For Backlog Bug`)

**Resolve JSDoc '\#' links to instance members**

*Fix JSDoc `#` links in the Go port to resolve instance members while preserving `.` links for static members.*

 * created by **tydavid5**
 * **typescript-automation[bot]** added label `For Backlog Bug`

### [Issue microsoft/TypeScript#65581](https://github.com/microsoft/TypeScript/issues/65581) (Open)

**TypeScript 7\.0\.2: Incorrect namespace qualification in import aliases \(import =\)**

*TypeScript 7.0.2 incorrectly emits unqualified namespace references for nested `import =` aliases, causing runtime `ReferenceError`s.*

 * created by **pirobox**

