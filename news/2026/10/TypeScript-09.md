# Report for 2026-10-09 (Friday, October 9th, 2026)

17 different users commented on 41 different issues.

## Recommended Actions

 * Response Recommended
    * @colinhacks reported that Zod's object types still had indexing and ordering issues in TS 7.1.0-dev.20261006.1 in [microsoft/TypeScript#32562](https://github.com/microsoft/TypeScript/issues/32562#issuecomment-6091289592)
    * @adilalperenciftci asked for a review of the revised getUnionSignatures approach in [microsoft/TypeScript#64360](https://github.com/microsoft/TypeScript/pull/64360#issuecomment-6096350640)
    * @rsnodgrass provided repro steps as requested in [microsoft/TypeScript#64605](https://github.com/microsoft/TypeScript/issues/64605#issuecomment-6084855435)

## Activity Summary

### [Issue microsoft/TypeScript#23185](https://github.com/microsoft/TypeScript/issues/23185) (Open, `Suggestion`, `Help Wanted`, `Good First Issue`, `Domain: Error Messages`)

**Cannot Load Custom Definition File in Repository**

*TypeScript cannot locate and use a custom .d.ts file for the ‘messageformat’ module despite various tsconfig settings.*

 * **RyanCavanaugh** removed label `PursuitFellowship`
 * [5 weeks ago](https://github.com/microsoft/TypeScript/issues/23185#issuecomment-5490016410) **LeonxLJX** said "I'd like to take this one — I'll follow up with a PR. (claiming via @LeonxLJX)"
 * [5 weeks ago](https://github.com/microsoft/TypeScript/issues/23185#issuecomment-5492444388) **LeonxLJX** said "Hi! I'd like to fix custom definition file loading. Plan: reproduce, fix the resolution, add a test. May I be assigned?"
 * [later](https://github.com/microsoft/TypeScript/issues/23185#issuecomment-6098045419) **mahesh-desu** offered to implement diagnostic improvements for failed non-relative module resolutions by checking for global declare modules and adding tests

### [Issue microsoft/TypeScript#32562](https://github.com/microsoft/TypeScript/issues/32562) (Open, `Suggestion`, `Awaiting More Feedback`, `Domain: Mapped Types`)

**Change property modifier in mapped type based on condition**

*Allow TypeScript mapped types to conditionally make properties optional or required based on their types*

 * (7.2 years ago) **RyanCavanaugh** added labels `Suggestion`, `Domain: Mapped Types`
 * [5.2 years ago](https://github.com/microsoft/TypeScript/issues/32562#issuecomment-886163346) **codinsonn** noted that the Merge<T> approach expanded Date types into object shapes and asked how to prevent this
 * [today](https://github.com/microsoft/TypeScript/issues/32562#issuecomment-6091289592) **colinhacks** described a limitation in Zod's object type inference causing indexing and optional key ordering issues in TS 7.1.0-dev

### [Issue microsoft/TypeScript#58696](https://github.com/microsoft/TypeScript/issues/58696) (Closed, `Bug`, `Help Wanted`, `Domain: Declaration Emit`)

**Non\-exported recursive type alias is inlined until it falls back to any in declarations**

*Non-exported recursive type aliases are inlined in declarations into deeply nested conditionals that end in any instead of erroring.*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [2.3 years ago](https://github.com/microsoft/TypeScript/issues/58696#issuecomment-2179220873) **ghost** figured out the issue was due to alias imports in the library's type declarations
 * **RyanCavanaugh** added label `Domain: Declaration Emit`
 * [today](https://github.com/microsoft/TypeScript/issues/58696#issuecomment-6088563668) **jakebailey** said "This was actually fixed by https://github.com/microsoft/typescript-go/pull/4507"
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#63700](https://github.com/microsoft/TypeScript/issues/63700) (Closed, `Suggestion`, `Committed`, `Domain: lib.d.ts`)

**Support recent \`Iterator\`/\`Iterator\.prototype\` methods in \`esnext\` \(eventually \`es2027\`\)**

*Add TC39 stage 3 and stage 4 Iterator methods zip, zipKeyed, chunks, join, and includes to TypeScript 7.1 esnext.*

 * **DanielRosenwasser** added to milestone `TypeScript 7.1`
 * **typescript-automation[bot]** added label `Fix Available`
 * **jakebailey** removed label `Fix Available`
 * (today) **DanielRosenwasser** closed the issue

### [Issue microsoft/TypeScript#63875](https://github.com/microsoft/TypeScript/issues/63875) (Closed, `Suggestion`, `Committed`, **andrewbranch**)

**API feature roadmap**

*API feature roadmap for TypeScript 7.1 outlining plugin replacements and top-level utilities with rough cost estimates.*

 * [5 weeks ago](https://github.com/microsoft/TypeScript/issues/63875#issuecomment-5522708727) **johnnyreilly** reported that the PR branch did not reliably improve build times and provided detailed benchmark results for Mac, Ubuntu, and Windows
 * [5 weeks ago](https://github.com/microsoft/TypeScript/issues/63875#issuecomment-5531936803) **andrewbranch** said "These are at least much better than your first table 😄 I think we can probably find more significant improvements, but I won't be able to dig into this more until after the beta release."
 * [5 weeks ago](https://github.com/microsoft/TypeScript/issues/63875#issuecomment-5532005314) **andrewbranch** announced intent to hide past conversations and previewed a significant refactor causing breaking changes and linked to issue for details
 * [today](https://github.com/microsoft/TypeScript/issues/63875#issuecomment-6087012143) **andrewbranch** said "Closing this out with updated status in #64709."
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#64095](https://github.com/microsoft/TypeScript/pull/64095) (Closed, `For Milestone Bug`)

**feat: add iterator methods to esnext**

*Add iterator methods to ESNext type definitions to support iteration protocols.*

 * created by **a-tarasyuk**
 * **typescript-automation[bot]** added label `For Milestone Bug`
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript#64233](https://github.com/microsoft/TypeScript/pull/64233) (Open, `For Milestone Bug`)

**fix\(64231\): avoid parsing async\(\) calls as typed arrows in conditionals**

*Prevent parser from misinterpreting async() calls in conditionals as typed arrow functions.*

 * [1 month ago](https://github.com/microsoft/TypeScript/pull/64233#issuecomment-5626219351) **typescript-automation[bot]** reported comparison results for the top 800 repos with tsc and stated everything looked good
 * (1 month ago) **typescript-automation[bot]** added label `For Milestone Bug`, and removed label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64233#issuecomment-6089574663) **jakebailey** suggested covering spread arguments after async and nested JS cases and noted pre-existing failures

### [PR microsoft/TypeScript#64360](https://github.com/microsoft/TypeScript/pull/64360) (Open, `For Backlog Bug`)

**Fix union overload signature ordering instability**

*Generate exact-arity variants for union signatures with optional parameters to ensure stable overload resolution without ad-hoc sorting.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/64360#issuecomment-5766137973) **jakebailey** said "This seems a bit too ad-hoc and out of place for the kind of thing we normally do. It is suspicious that nothing else changed, either, and that it's purely additive?"
 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/64360#issuecomment-5767834549) **adilalperenciftci** dropped the post-sorting approach and replaced it with expanding optional-parameter signatures into exact-arity variants in getUnionSignatures so findMatchingSignatures matches without extra sorting
 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/64360#issuecomment-5843031820) **adilalperenciftci** rebased cleanly on current main and asked if the revised getUnionSignatures arity expansion was preferable or if union overload matching should be handled differently
 * [later](https://github.com/microsoft/TypeScript/pull/64360#issuecomment-6096350640) **adilalperenciftci** followed up on the PR, stated the branch was rebased cleanly on main with no conflicts, and asked for a review of the revised getUnionSignatures approach

### [PR microsoft/TypeScript#64588](https://github.com/microsoft/TypeScript/pull/64588) (Closed, `For Uncommitted Bug`)

**Restore symbol names in JSX import action titles**

*Restores symbol names in JSX import action titles by porting Strada’s logic and fixes two skipped tests.*

 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64588#issuecomment-5953399343) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64588#issuecomment-5957506745) **jakebailey** said "Copilot absolutely hates this 😄 "
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64588#issuecomment-6056683833) **Andarist** noted disagreement with Copilot suggestions and asked if anything else should be addressed after adding extra coverage
 * [today](https://github.com/microsoft/TypeScript/pull/64588#issuecomment-6090647089) **jakebailey** said "Ah, because the review happened during an outage."

### [Issue microsoft/TypeScript#64605](https://github.com/microsoft/TypeScript/issues/64605) (Open, `Needs Investigation`, **gabritto**)

**TS5115 in published Zod 4\.5–4\.6 types after \#64372**

*Zod 4.5.0–4.6.5 z.json() types cause TS5115 infinite circularity errors in TypeScript 7.1 nightlies after PR #64372, impacting ~62M weekly downloads.*

 * (3 days ago) **RyanCavanaugh** set milestone to `TypeScript 7.1.1 RC`, and assigned to **gabritto**
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/64605#issuecomment-6053406731) **RedesignedRobot** traced the cause of a recursive member resolution issue introduced by #64372, proposed a fix that preserves declared members on a stack during inheritance resolution, reported passing tests and a cleaned-up baseline, and offered to open a PR
 * [today](https://github.com/microsoft/TypeScript/issues/64605#issuecomment-6084855435) **rsnodgrass** confirmed the issue reproduced with TypeScript 7.1.0-dev and Zod 4.6.5, provided minimal reproduction code and version comparison, and requested review

### [Issue microsoft/TypeScript#64631](https://github.com/microsoft/TypeScript/issues/64631) (Closed, `Bug`, **andrewbranch**)

**\[api\] A nested request from a resolveModuleName callback gets another request's answer**

*Nested module resolution requests within a resolveModuleName callback sometimes return other requests’ results, causing incorrect resolutions.*

 * created by **cplieger**
 * (3 days ago) **RyanCavanaugh** added label `Bug`, and assigned to **andrewbranch**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64639](https://github.com/microsoft/TypeScript/pull/64639) (Closed, `For Uncommitted Bug`, **andrewbranch**)

**\[api\] Answer nested requests on the sync connection in stack order**

*SyncConn.Call’s nested requests could interleave and receive incorrect responses, now fixed by enforcing stack-order handling.*

 * [3 days ago](https://github.com/microsoft/TypeScript/pull/64639#issuecomment-6026775863) **jakebailey** said "Yeah, I blindly assigned this to you, but now that I look, I suspect there's a better design here"
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/64639#issuecomment-6026835681) **andrewbranch** described having tried to block unrelated client callbacks until the request stack cleared, noted the difficulty distinguishing them from reentrant calls, and suggested context plumbing could work though complicated
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/64639#issuecomment-6033522494) **cplieger** thanked reviewers and described the smaller version changes including reduced shape, context plumbing, use of sync.Cond, and notification handling
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64664](https://github.com/microsoft/TypeScript/pull/64664) (Closed, `For Uncommitted Bug`)

**Update localization files**

*Update localization files and regenerate corresponding runtime artifacts.*

 * created by **typescript-automation[bot]**
 * (2 days ago) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#64669](https://github.com/microsoft/TypeScript/issues/64669) (Open, `Bug`)

**runtime error: invalid memory address or nil pointer dereference in getMembersOfSymbol**

*Assigning a computed property to a function causes a nil pointer panic in getMembersOfSymbol during declaration-only emit.*

 * created by **YuanchengJiang**
 * (2 days ago) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`
 * [later](https://github.com/microsoft/TypeScript/issues/64669#issuecomment-6097977422) **andre-fajar-n** said "I will work on this issue"

### [PR microsoft/TypeScript#64694](https://github.com/microsoft/TypeScript/pull/64694) (Open, `For Uncommitted Bug`, **RyanCavanaugh**, **Copilot**)

**Bound recursive array and tuple type printing**

*Limit active array and tuple serialization depth to prevent infinite recursion and stack overflows when printing recursive generic types.*

 * (yesterday) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64694#issuecomment-6089916581) **jakebailey** opined that the change was probably fine, hoped it would interact well with #64662, and requested the TypeScript bot to run tests
 * [today](https://github.com/microsoft/TypeScript/pull/64694#issuecomment-6089917824) **typescript-automation[bot]** reported build statuses for test top400, user test this, run dt, and perf test this faster
 * [today](https://github.com/microsoft/TypeScript/pull/64694#issuecomment-6089949495) **jakebailey** provided review feedback outlining two coverage gaps and suggesting tests
 * [today](https://github.com/microsoft/TypeScript/pull/64694#issuecomment-6090257706) **typescript-automation[bot]** reported that the DT test results were ready and unchanged
 * [today](https://github.com/microsoft/TypeScript/pull/64694#issuecomment-6090272100) **typescript-automation[bot]** reported tsc user test results and confirmed everything looked good
 * [today](https://github.com/microsoft/TypeScript/pull/64694#issuecomment-6090282721) **typescript-automation[bot]** reported the requested perf run results
 * [today](https://github.com/microsoft/TypeScript/pull/64694#issuecomment-6090885423) **typescript-automation[bot]** reported that running the top 400 repos tsc comparison between baseline and pr succeeded without issues

### [Issue microsoft/TypeScript#64706](https://github.com/microsoft/TypeScript/issues/64706) (Open, `Bug`)

**Declaration emit renames value references when a shadowed type parameter shares its parameter's name**

*TypeScript declaration emit incorrectly renames value references in nested functions when inner and outer type parameters share the same name.*

 * created by **jasonkuhrt**

### [Issue microsoft/TypeScript#64707](https://github.com/microsoft/TypeScript/issues/64707) (Open)

**JSDoc\-generated namespaces not merged with default exports**

*TypeScript does not merge JSDoc-created namespaces into default-exported classes, resulting in unresolved namespace member errors.*

 * created by **donmccurdy**

### [Issue microsoft/TypeScript#64708](https://github.com/microsoft/TypeScript/issues/64708) (Open)

**Unbounded memory in declaration emit for an inferred type built from non\-exported recursive aliases \(also hit by \`\-\-noEmit \-\-watch\`\)**

*TypeScript's declaration emit and watch mode trigger unbounded memory growth when inferring exported types from non-exported recursive aliases.*

 * created by **mattleonowicz**

### [Issue microsoft/TypeScript#64709](https://github.com/microsoft/TypeScript/issues/64709) (Open, `Discussion`, `Domain: API`, **andrewbranch**)

**API status as of 7\.1 beta, versioning/compatibility plan ahead**

*TypeScript 7.1 beta removes unstable API prefixes, outlines backward-compatible versioning, experimental API strategy, missing feature triage, and upcoming docs.*

 * created by **andrewbranch**
 * (today) **andrewbranch** added labels `Discussion`, `Domain: API`, and assigned to **andrewbranch**

### [Issue microsoft/TypeScript#64710](https://github.com/microsoft/TypeScript/issues/64710) (Open, **johnfav03**)

**\[ServerErrors\]\[JavaScript\] main**

*CI tests on the main branch reported server errors, timeouts, and unknown failures while analyzing 300 popular TypeScript repositories.*

 * created by **typescript-automation[bot]**
 * [today](https://github.com/microsoft/TypeScript/issues/64710#issuecomment-6090296476) **typescript-automation[bot]** reported a panic during textDocument/diagnostic handling with a stack trace and details for chartjs/Chart.js
 * [today](https://github.com/microsoft/TypeScript/issues/64710#issuecomment-6090297018) **typescript-automation[bot]** reported a server connection closed prematurely error with undefined and provided affected repo, artifact links, last requests, and repro steps
 * [today](https://github.com/microsoft/TypeScript/issues/64710#issuecomment-6090297648) **typescript-automation[bot]** reported a server connection closed prematurely error for the vuejs/vue-cli repository with associated logs and repro steps

### [PR microsoft/TypeScript#64711](https://github.com/microsoft/TypeScript/pull/64711) (Closed, `Author: Team`, `For Uncommitted Bug`, **ahejlsberg**)

**Dense link stores**

*Switching paged link stores to dense allocation cuts wasted storage and memory usage by up to 9% in multi-checker compilations.*

 * created by **ahejlsberg**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript/pull/64711#issuecomment-6090517240) **ahejlsberg** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/64711#issuecomment-6090518373) **typescript-automation[bot]** posted CI build status updates for test top400, user test this, run dt, and perf test this faster
 * [today](https://github.com/microsoft/TypeScript/pull/64711#issuecomment-6090801666) **typescript-automation[bot]** notified that DT test results were ready and unchanged
 * [today](https://github.com/microsoft/TypeScript/pull/64711#issuecomment-6090868732) **typescript-automation[bot]** posted the requested performance run results including comparison metrics for errors, symbols, types, and memory usage
 * [today](https://github.com/microsoft/TypeScript/pull/64711#issuecomment-6091080523) **typescript-automation[bot]** provided tsc user test results and indicated everything looked good
 * (today) **ahejlsberg** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/64711#issuecomment-6091297926) **typescript-automation[bot]** reported successful tsc comparison between baseline and pr on the top 400 repos

### [PR microsoft/TypeScript#64712](https://github.com/microsoft/TypeScript/pull/64712) (Open, `Author: Team`, `For Backlog Bug`, **jakebailey**)

** Fix compiler option invalidation in incremental builds**

*Audit and fix incorrect incremental build invalidation for compiler options, build-info persistence, global file ordering, and deletions.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`, `For Backlog Bug`, removed label `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#64713](https://github.com/microsoft/TypeScript/pull/64713) (Open, `For Backlog Bug`)

**Copy JSDoc from mapped type properties in declaration emit**

*Copy JSDoc comments for mapped type properties by falling back to their first declaration when valueDeclaration is missing.*

 * created by **colinhacks**
 * **typescript-automation[bot]** added label `For Backlog Bug`

### [Issue microsoft/TypeScript#64714](https://github.com/microsoft/TypeScript/issues/64714) (Open, **johnfav03**)

**\[ServerErrors\]\[TypeScript\] main**

*The TypeScript main build pipeline encountered server errors analyzing 300 repositories, successfully completing 147 analyses and logging several timeouts, clone failures, and unknown errors.*

 * created by **typescript-automation[bot]**
 * [today](https://github.com/microsoft/TypeScript/issues/64714#issuecomment-6091661594) **typescript-automation[bot]** reported a panic handling textDocument/completion due to path containing a URL query or fragment
 * [today](https://github.com/microsoft/TypeScript/issues/64714#issuecomment-6091662030) **typescript-automation[bot]** reported a server connection closed prematurely for babel/babel and provided error details, recent requests, and repro steps
 * [today](https://github.com/microsoft/TypeScript/issues/64714#issuecomment-6091662486) **typescript-automation[bot]** reported a server connection closing prematurely with undefined error for openclaw/openclaw and included affected repo details, logs, and repro steps

### [Issue microsoft/TypeScript#64715](https://github.com/microsoft/TypeScript/issues/64715) (Open)

**\`\-\-incremental\` keeps stale diagnostics after a change in a \`declare global\` block of a package declaration file \(7\.0\.2, regression from 6\.0\.3\)**

*TypeScript’s --incremental retains stale errors after modifying declare global block in a package .d.ts file, regressing from v6.0.3 to v7.0.2.*

 * created by **plum117**

### [PR microsoft/TypeScript#64716](https://github.com/microsoft/TypeScript/pull/64716) (Open, `For Backlog Bug`)

**Re\-scan '\<\<' when parsing type arguments in heritage clauses, typeof queries, and JSX**

*Adjust parser to split '<<' tokens into two '<' when parsing type arguments in heritage clauses, typeof queries, and JSX.*

 * created by **ahmad65saad**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64716#issuecomment-6093450032) **ahmad65saad** agreed with microsoft-github-policy-service

### [PR microsoft/TypeScript#64717](https://github.com/microsoft/TypeScript/pull/64717) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Refresh no\-input diagnostics when wildcard files change**

*Ensure no-input diagnostics are refreshed whenever wildcard file patterns are changed.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#64718](https://github.com/microsoft/TypeScript/pull/64718) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Preserve checking globals before declaration signature generation**

*Preserve global checking before declaration signature generation to prevent unexpected diffs introduced by issue #64452.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [Issue microsoft/TypeScript#64719](https://github.com/microsoft/TypeScript/issues/64719) (Open)

**\`export \*\` resolution allocates per re\-exported name, slowing checks of barrels over large modules**

*Per-name allocations during export * resolution cause excessive memory allocations and significant slowdowns when type-checking large barrel chains.*

 * created by **gwkline**

### [Issue microsoft/TypeScript#64720](https://github.com/microsoft/TypeScript/issues/64720) (Open)

**Declaration diagnostics allocate a diagnostic selector closure for every declaration visited**

*Declaration diagnostics allocate a diagnostic selector closure for each visited declaration, causing performance overhead.*

 * created by **gwkline**

### [Issue microsoft/TypeScript#64721](https://github.com/microsoft/TypeScript/issues/64721) (Open)

**Module specifier generation rescans package\.json \`exports\` and tsconfig \`paths\` for every importing file**

*Module specifier generation repeatedly rescans package.json exports and tsconfig paths per import, slowing declaration emit.*

 * created by **gwkline**

### [PR microsoft/TypeScript#64722](https://github.com/microsoft/TypeScript/pull/64722) (Open, `For Uncommitted Bug`)

**Merge export \* tables without per\-name collision trackers**

*Optimize export * symbol merging by eliminating per-name collision trackers and reducing table allocations.*

 * created by **gwkline**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [PR microsoft/TypeScript#64723](https://github.com/microsoft/TypeScript/pull/64723) (Open, `For Uncommitted Bug`)

**Create declaration emit diagnostic selectors on demand**

*Delay creation of symbol accessibility diagnostic selectors until needed during declaration file emission to eliminate unnecessary allocations and improve performance.*

 * created by **gwkline**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [PR microsoft/TypeScript#64724](https://github.com/microsoft/TypeScript/pull/64724) (Open, `For Uncommitted Bug`)

**Cache exports lookups and path patterns in module specifier generation**

*Cache exports and paths lookups in the module specifier generator to reduce redundant resolution work.*

 * created by **gwkline**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [Issue microsoft/TypeScript#64725](https://github.com/microsoft/TypeScript/issues/64725) (Open)

**Crash \(nil pointer in getPropertyOfObjectType\) under \-\-noLib when a global import x = T\.m names a type**

*Compiler crashes with nil pointer dereference in getPropertyOfObjectType when using a global import alias for a type under --noLib*

 * created by **YuanchengJiang**

### [PR microsoft/TypeScript#64726](https://github.com/microsoft/TypeScript/pull/64726) (Open, `For Backlog Bug`)

**Improve error when an unresolved import matches a global namespace**

*Provide a dedicated TS95210 error that recommends quoting an ambient module when a non-relative import conflicts with a global namespace.*

 * created by **mahesh-desu**
 * (later) **typescript-automation[bot]** added labels `For Backlog Bug`, `For Backlog Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/64726#issuecomment-6098553897) **mahesh-desu** said "@microsoft-github-policy-service agree"

### [Issue microsoft/TypeScript#64727](https://github.com/microsoft/TypeScript/issues/64727) (Open)

**TS 7: declaration emit property order depends on which other files are in the program**

*TypeScript 7’s declaration emitter produces inconsistent property ordering in generated d.ts files depending on which files are included in the program.*

 * created by **maschwenk**

