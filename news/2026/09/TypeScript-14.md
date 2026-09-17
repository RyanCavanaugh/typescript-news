# Report for 2026-09-14 (Monday, September 14th, 2026)

22 different users commented on 37 different issues.

## Recommended Actions

 * Response Recommended
    * @typescript-automation[bot] provided perf run results as requested in [microsoft/TypeScript#64252](https://github.com/microsoft/TypeScript/pull/64252#issuecomment-5670695144)
    * @Artyomkun provided important reproduction details and race condition insights in [microsoft/TypeScript#64261](https://github.com/microsoft/TypeScript/issues/64261#issuecomment-5666859147)
    * @noamaanMulla-03 offered to take this up in [microsoft/TypeScript#64272](https://github.com/microsoft/TypeScript/issues/64272#issuecomment-5679083991)

## Activity Summary

### [Issue microsoft/TypeScript#30698](https://github.com/microsoft/TypeScript/issues/30698) (Open, `Suggestion`, `Awaiting More Feedback`)

**Support custom typeof functions**

*Enable TypeScript to infer correct types from custom typeof-like functions without requiring manual casts.*

 * [7.4 years ago](https://github.com/microsoft/TypeScript/issues/30698#issuecomment-484279024) **ExE-Boss** said "Yeah, but then the return type of the type function would be unknown, since the default return value is undeclared, so it’s a syntax error."
 * [5.2 years ago](https://github.com/microsoft/TypeScript/issues/30698#issuecomment-867101723) **mcmath** proposed using a 'where' clause for type guards to avoid ternary operator confusion
 * [4.7 years ago](https://github.com/microsoft/TypeScript/issues/30698#issuecomment-983473387) **ExE-Boss** suggested using a switch-like syntax for conditional return types with the condition preceding the return value
 * [today](https://github.com/microsoft/TypeScript/issues/30698#issuecomment-5672893904) **danfuzz** explained their use case for extending JS types (including null) and wanting switch-based type narrowing to avoid manual casts

### [PR microsoft/TypeScript#64000](https://github.com/microsoft/TypeScript/pull/64000) (Closed, `For Uncommitted Bug`)

**Expose Checker\.getAwaitedType on the unstable API**

*Expose getAwaitedType on the TypeScript unstable API to allow consumers to recursively obtain the resolved type of awaited expressions.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/64000#issuecomment-5410558963) **baptistejamin** agreed with microsoft-github-policy-service
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/64000#issuecomment-5471846926) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [later](https://github.com/microsoft/TypeScript/pull/64000#issuecomment-5676152018) **mrazauskas** said "This got added in #64264"
 * (later) **baptistejamin** closed the issue

### [PR microsoft/TypeScript#64002](https://github.com/microsoft/TypeScript/pull/64002) (Closed, `For Uncommitted Bug`)

**Expose Checker\.getIndexInfoOfType on the unstable API**

*Expose Checker.getIndexInfoOfType in TypeScript’s unstable API to mirror the Go checker and enable typescript-eslint’s isTypeReadonly functionality.*

 * created by **baptistejamin**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/64002#issuecomment-5471847349) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [later](https://github.com/microsoft/TypeScript/pull/64002#issuecomment-5676157646) **mrazauskas** said "This got added in #64264"
 * (later) **baptistejamin** closed the issue

### [Issue microsoft/TypeScript#64195](https://github.com/microsoft/TypeScript/issues/64195) (Open, `Needs Investigation`, **johnfav03**)

**LSP: file contents are not re\-read when \`didChangeWatchedFiles\` reports \`Created\` \(type 1\) for a file already in the program**

*LSP server fails to reload existing files when a Created file watcher event occurs, leading to stale content.*

 * created by **shuto-masuda**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **johnfav03**

### [Issue microsoft/TypeScript#64225](https://github.com/microsoft/TypeScript/issues/64225) (Closed, `Needs More Info`)

**1\.136\.1: with TS Nightly, the tsconfig\.json does not use \`\-\-runExternalCode\`**

*VS Code 1.136.1 fails to apply the --runExternalCode flag in tsconfig.json with TypeScript nightly, causing content-mapper errors.*

 * **dbaeumer** unassigned **dbaeumer**
 * [4 days ago](https://github.com/microsoft/TypeScript/issues/64225#issuecomment-5614729642) **dbaeumer** said "Seems related to TS 7"
 * [4 days ago](https://github.com/microsoft/TypeScript/issues/64225#issuecomment-5618456857) **NullVoxPopuli** said "ts CLI has had no issues, afaict"
 * [today](https://github.com/microsoft/TypeScript/issues/64225#issuecomment-5668256895) **RyanCavanaugh** said "This is the error you see if you're not on the latest extension version - can you confirm that your TS VS Code extension is up to date?"
 * **RyanCavanaugh** added label `Needs More Info`
 * [today](https://github.com/microsoft/TypeScript/issues/64225#issuecomment-5668380437) **NullVoxPopuli** said "yea seems fixed now -- thanks!"
 * (today) **NullVoxPopuli** closed the issue

### [Issue microsoft/TypeScript#64229](https://github.com/microsoft/TypeScript/issues/64229) (Closed, `Design Limitation`)

**nullish types not narrowed in if block**

*Optional chaining and nullish coalescing conditions do not narrow nullish types within if blocks in TypeScript.*

 * [3 days ago](https://github.com/microsoft/TypeScript/issues/64229#issuecomment-5636716584) **errorx666** asked whether the issue was related to using optional chaining in a comparison, noting that nullish values can't be greater than zero so it behaves as intended
 * **RyanCavanaugh** added label `Design Limitation`
 * [today](https://github.com/microsoft/TypeScript/issues/64229#issuecomment-5666272111) **RyanCavanaugh** observed no generalizable pattern and illustrated with an alternative example
 * [today](https://github.com/microsoft/TypeScript/issues/64229#issuecomment-5667133353) **snarbles2** explained that numeric comparison of null is erroneous and that TypeScript should type-check and error on such cases

### [Issue microsoft/TypeScript#64231](https://github.com/microsoft/TypeScript/issues/64231) (Open, `Bug`)

**Parser misinterprets async\(\) calls in conditional expressions as async arrow functions**

*TypeScript parser misinterprets calls to a function named async in ternary expressions as async arrow functions, causing syntax errors.*

 * (3 days ago) **DanielRosenwasser** added label `Bug`, and set milestone to `TypeScript 7.1.0 Beta`
 * [today](https://github.com/microsoft/TypeScript/issues/64231#issuecomment-5662369126) **anbv29** asked if they could work on the issue
 * [today](https://github.com/microsoft/TypeScript/issues/64231#issuecomment-5668025041) **RyanCavanaugh** said "@anbv29 Why do you want to open a third PR for this?"

### [PR microsoft/TypeScript#64234](https://github.com/microsoft/TypeScript/pull/64234) (Closed, `For Milestone Bug`)

**Fix parsing of async\(\) calls in conditional expressions**

*Parser misinterprets async() in conditional expressions as arrow functions, causing syntax errors in .ts and .js files.*

 * [4 days ago](https://github.com/microsoft/TypeScript/pull/64234#issuecomment-5623464092) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (3 days ago) **typescript-automation[bot]** added label `For Milestone Bug`, and removed label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64234#issuecomment-5668128815) **RyanCavanaugh** said "Closing in favor of #64233"
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#64237](https://github.com/microsoft/TypeScript/pull/64237) (Closed, `Author: Team`, `For Milestone Bug`, **ahejlsberg**)

**Distinguish between non\-distributed and distributed type parameters**

*TypeScript now differentiates distributed and non-distributed type parameters in conditional types, reports constraint violations accordingly, and marks distributed parameters with a (distributed) hover indicator.*

 * [3 days ago](https://github.com/microsoft/TypeScript/pull/64237#issuecomment-5642210141) **typescript-automation[bot]** posted build status updates for the ‘user test this’ and ‘test top1000’ jobs
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/64237#issuecomment-5642382933) **typescript-automation[bot]** reported user test results comparing main and refs/pull/64237/merge, noted two package install failures and one git clone failure likely unrelated to the change, and confirmed everything else looked good
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/64237#issuecomment-5642708165) **typescript-automation[bot]** reported build comparison results for the top 1000 repos between main and pull/64237/merge and highlighted failures in triggerdotdev/trigger.dev
 * [today](https://github.com/microsoft/TypeScript/pull/64237#issuecomment-5668480185) **ahejlsberg** said "Tests are clean. Two top 1000 projects have new errors, but those errors are expected."

### [Issue microsoft/TypeScript#64240](https://github.com/microsoft/TypeScript/issues/64240) (Closed, `Bug`, **andrewbranch**)

**API panics when serializing number literal types with \`\+Infinity\` and \`\-Infinity\`**

*TypeScript’s unstable sync API panics when serializing number literal types representing +Infinity or -Infinity.*

 * (today) **RyanCavanaugh** added label `Bug`, set milestone to `Backlog`, and assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript/issues/64240#issuecomment-5675951235) **auvred** tested resolution of NaN in enum constants and added support for NaNs

### [Issue microsoft/TypeScript#64242](https://github.com/microsoft/TypeScript/issues/64242) (Closed, `Needs Investigation`, **andrewbranch**)

**Sporadic \`context canceled\` in \`stderr\` when running TypeScript API in subprocess tests**

*Intermittent 'context canceled' output appears in stderr instead of empty when testing a CLI using TypeScript's API on Ubuntu CI.*

 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.1.1 RC`, and assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript/issues/64242#issuecomment-5674451129) **mrazauskas** noted that the issue also surfaced in CI runs of typescript-eslint and linked to the relevant logs

### [Issue microsoft/TypeScript#64249](https://github.com/microsoft/TypeScript/issues/64249) (Open, `Needs Investigation`, **weswigham**)

**Spurious TS4094 "exported anonymous class type may not be private" error after upgrading from TS6 to TS7**

*Upgrading from TypeScript 6 to 7 causes TS4094 errors on exported anonymous ZodRoute instances due to private class properties.*

 * created by **jedwards1211**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.1.1 RC`, and assigned to **weswigham**

### [Issue microsoft/TypeScript#64251](https://github.com/microsoft/TypeScript/issues/64251) (Open, `Possible Improvement`)

**Object with all context\-sensitive properties requires at least one non\-context\-sensitive property for inference to work**

*createMachine type inference for context and state fails when all state properties are context-sensitive unless a dummy property is added*

 * created by **devanshj**
 * (today) **RyanCavanaugh** added label `Possible Improvement`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/64251#issuecomment-5670374974) **RyanCavanaugh** said "@Andarist any thoughts (on this or the PR) ?"
 * [today](https://github.com/microsoft/TypeScript/issues/64251#issuecomment-5670580961) **RyanCavanaugh** said "Copilot cites #48798 as prior work in this area, with #54029 as a superset of the linked PR"

### [PR microsoft/TypeScript#64252](https://github.com/microsoft/TypeScript/pull/64252) (Open, `For Backlog Bug`)

**Fix reverse mapped type inference when all properties are context\-sensitive**

*Improve reverse mapped type inference to correctly handle scenarios where every property is context-sensitive.*

 * (2 days ago) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/64252#issuecomment-5646221240) **devanshj** thanked the catch and noted that they tweaked userland types to fix the issue, mentioning the compiler was already good
 * [today](https://github.com/microsoft/TypeScript/pull/64252#issuecomment-5670354326) **RyanCavanaugh** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/64252#issuecomment-5670355325) **typescript-automation[bot]** reported the start of CI jobs and their statuses
 * (today) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64252#issuecomment-5670687521) **typescript-automation[bot]** reported the user test results comparing main and PR merge, noting infrastructure failures but otherwise all good
 * [today](https://github.com/microsoft/TypeScript/pull/64252#issuecomment-5670695144) **typescript-automation[bot]** provided the perf run results for the requested comparison report
 * [later](https://github.com/microsoft/TypeScript/pull/64252#issuecomment-5680822580) **devanshj** reported that xstate broke with 14 new errors and said they would investigate whether the break is acceptable or adjust the PR accordingly

### [Issue microsoft/TypeScript#64260](https://github.com/microsoft/TypeScript/issues/64260) (Closed, `Needs More Info`)

**Non\-null discriminant narrowing can use a stale fact after a later assignment**

*Discriminant narrowing with non-null assertions can incorrectly rely on stale facts when assignments occur in comparison or switch expressions, causing missing undefined errors.*

 * created by **z0rimo**
 * [today](https://github.com/microsoft/TypeScript/issues/64260#issuecomment-5670292530) **RyanCavanaugh** said "This doesn't seem like remotely realistic code, more like an attempt to break a heuristic that works in every case except this synthetic counterexample. What led you to this report?"
 * **RyanCavanaugh** added label `Needs More Info`
 * [today](https://github.com/microsoft/TypeScript/issues/64260#issuecomment-5672094434) **z0rimo** clarified that the example arose from validating the implementation for issue #64257 while fixing #62511 and closed the issue as it was a synthetic constraint
 * (today) **z0rimo** closed the issue

### [Issue microsoft/TypeScript#64261](https://github.com/microsoft/TypeScript/issues/64261) (Closed, `Unactionable`)

**Windows 11, Node v26\.8\.2, typescript@7\.0\.2 \(@typescript/native global\), ts7\-eslint@0\.2\.0, ESLint 10\.x\.**

*A writeAllBuf race condition causes intermittent EPIPE broken pipe errors in @typescript-eslint on Windows.*

 * **RyanCavanaugh** added label `Unactionable`
 * (today) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript/issues/64261#issuecomment-5666663441) **Artyomkun** noted that the error lay in the experimental dependencies for version 7, encountered a rare edge case, and advised caution when upgrading to 7.1
 * [today](https://github.com/microsoft/TypeScript/issues/64261#issuecomment-5666859147) **Artyomkun** confirmed that EPIPE occurs when closing the external PowerShell window spawned by VS Code and identified a race in writeAllBuf not checking exitCode before writing

### [Issue microsoft/TypeScript#64262](https://github.com/microsoft/TypeScript/issues/64262) (Open, `Bug`, `Domain: tsc -b`, **jakebailey**)

**Port \`DirWatchSet\` over to TS7**

*Cherry-pick commit e05860d9328a894189b49d9c43fb8a52e6c6d5a2 implementing DirWatchSet into a new 7.0.x branch of the TypeScript repository.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** added labels `Bug`, `Domain: tsc -b`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#64263](https://github.com/microsoft/TypeScript/pull/64263) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**Turn requestfilesystem into a single layer providing project\.FileHandle lookups so it can be used as the top layer above editor overlays**

*Refactor requestfilesystem to return a single FileSourceLayer for project.FileHandle lookups that stacks above editor overlays.*

 * created by **andrewbranch**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#64264](https://github.com/microsoft/TypeScript/pull/64264) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**Add missing APIs needed by typescript\-eslint**

*Adds missing TypeScript compiler APIs required by typescript-eslint and fixes JSX Emit enum values.*

 * created by **andrewbranch**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript#64265](https://github.com/microsoft/TypeScript/issues/64265) (Open, `Suggestion`, `In Discussion`, `Domain: API`)

**No batched \`getContextualType\` in 7\.1 API**

*TypeScript 7.1 nightly builds lack a batched getContextualType API, prompting developers to ask if this omission is intentional.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** added labels `Suggestion`, `In Discussion`, `Domain: API`

### [PR microsoft/TypeScript#64266](https://github.com/microsoft/TypeScript/pull/64266) (Open, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Improve performance of batched requests**

*Automatically batch requests across all API endpoints with code generation, remove hardcoded entrypoints, switch to struct-of-arrays layout for better performance.*

 * created by **weswigham**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **weswigham**

### [PR microsoft/TypeScript#64267](https://github.com/microsoft/TypeScript/pull/64267) (Closed, `Author: Team`, `For Uncommitted Bug`, **DanielRosenwasser**)

**Use a mapped type for \`ExecutedGeneratorResults\`\.**

*Refactor ExecutedGeneratorResults to use a mapped type for improved type safety and maintainability.*

 * created by **DanielRosenwasser**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript/pull/64267#issuecomment-5672543326) **DanielRosenwasser** said "If only I could read."
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript#64268](https://github.com/microsoft/TypeScript/pull/64268) (Open, `For Backlog Bug`)

**lib: ZonedDateTime\.toLocaleString must not accept a timeZone option**

*Restrict ZonedDateTime.toLocaleString’s options type to exclude timeZone by introducing a specialized interface extending Intl.DateTimeFormatOptions.*

 * created by **lukiod**
 * **typescript-automation[bot]** added label `For Backlog Bug`

### [PR microsoft/TypeScript#64269](https://github.com/microsoft/TypeScript/pull/64269) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**\[api\] Refactor requestfilesystem into a stackable layer so it can be used as the top layer above editor overlays**

*Refactor the requestfilesystem API to return a stackable FileSystemLayer so API file changes override editor overlays correctly.*

 * created by **andrewbranch**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **andrewbranch**

### [Issue microsoft/TypeScript#64270](https://github.com/microsoft/TypeScript/issues/64270) (Open)

**Auto\-import completions are not shown inside named imports with TypeScript 7 / tsgo**

*Named import auto-completions are missing in VS Code with TypeScript 7’s native tsgo language server, though they work in TypeScript 6.*

 * created by **devvitor67**

### [Issue microsoft/TypeScript#64272](https://github.com/microsoft/TypeScript/issues/64272) (Open)

**ts1484 Quick fix will dupe comments**

*The TypeScript quick fix for converting an import to 'import type' under verbatimModuleSyntax incorrectly duplicates surrounding comments.*

 * created by **bulebrainbrand**
 * [later](https://github.com/microsoft/TypeScript/issues/64272#issuecomment-5679083991) **noamaanMulla-03** said "Hi, I'd love to take this up :)"
 * [later](https://github.com/microsoft/TypeScript/issues/64272#issuecomment-5679199871) **bulebrainbrand** said "sure! i'm not good at typescript architecture, so may i can't found system which cause this problem. thank you!"

### [Issue microsoft/TypeScript#64273](https://github.com/microsoft/TypeScript/issues/64273) (Closed)

**Crash: unexpected TypeElement: KindPropertyDeclaration**

*A nightly TypeScript compiler build crashes with unexpected TypeElement KindPropertyDeclaration when printing a private interface method*

 * created by **YuanchengJiang**
 * [later](https://github.com/microsoft/TypeScript/issues/64273#issuecomment-5680374232) **a-tarasyuk** said "@RyanCavanaugh, it seems the labels should be extended with a new crash-on-invalid label 😄 "

### [Issue microsoft/TypeScript#64274](https://github.com/microsoft/TypeScript/issues/64274) (Closed)

**\`satisfies\` removes the \`readonly\` constraint from a tuple**

*Using the satisfies operator on a const tuple unexpectedly strips its readonly constraint, unlike with const objects.*

 * created by **Sector6759**
 * [later](https://github.com/microsoft/TypeScript/issues/64274#issuecomment-5679971827) **jcalz** explained that the behavior was working as intended per #55229, clarified the difference between readonly arrays and object types, and noted that this issue was effectively a duplicate of #57107
 * [later](https://github.com/microsoft/TypeScript/issues/64274#issuecomment-5680335147) **Sector6759** said "Thanks a lot for the explanation."
 * (later) **Sector6759** closed the issue

### [PR microsoft/TypeScript#64275](https://github.com/microsoft/TypeScript/pull/64275) (Closed, `For Uncommitted Bug`)

**fix\(64273\): fix declaration emit crash on private method signatures**

*A crash occurring during declaration file emission due to private method signatures has been resolved.*

 * created by **a-tarasyuk**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [PR microsoft/TypeScript#64276](https://github.com/microsoft/TypeScript/pull/64276) (Closed, `Author: Team`, `For Milestone Bug`, **andrewbranch**)

**Ignore sync api\.close\(\)’s SIGTERM for purposes of error printing and exit status**

*Ignore the SIGTERM signal sent by sync api.close() when determining error output and process exit status.*

 * created by **andrewbranch**
 * (later) **typescript-automation[bot]** added labels `Author: Team`, `For Milestone Bug`, and assigned to **andrewbranch**

### [PR microsoft/TypeScript#64277](https://github.com/microsoft/TypeScript/pull/64277) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**Remove FS\(\)\.WalkDir**

*Remove FS().WalkDir from the virtual filesystem due to lack of usage and caching issues.*

 * created by **andrewbranch**
 * (later) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **andrewbranch**

