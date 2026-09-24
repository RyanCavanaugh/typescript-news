# Report for 2026-09-17 (Thursday, September 17th, 2026)

15 different users commented on 43 different issues.

## Recommended Actions

 * Response Recommended
    * @devanshj asked if the PR could type the provided example in [microsoft/TypeScript#64251](https://github.com/microsoft/TypeScript/issues/64251#issuecomment-5719068699)
    * @typescript-automation[bot] provided perf run results as requested in [microsoft/TypeScript#64311](https://github.com/microsoft/TypeScript/pull/64311#issuecomment-5718136601)

## Activity Summary

### [Issue microsoft/TypeScript#44334](https://github.com/microsoft/TypeScript/issues/44334) (Closed, `Bug`, `Needs More Info`, `Domain: lib.d.ts`)

**Breaking change 4\.3 RC: TS2488: Build:Type 'SomeArrayType' must have a '\[Symbol\.iterator\]\(\)' method that returns an iterator\.**

*TypeScript 4.3 RC incorrectly errors TS2488 on array spread when SymbolConstructor is moved to a custom namespace.*

 * [1 week ago](https://github.com/microsoft/TypeScript/issues/44334#issuecomment-5568399979) **RyanCavanaugh** requested the complete custom library and build configuration to reproduce the TS2488 issue
 * (1 week ago) **RyanCavanaugh** added labels `Needs Human Review`, `Needs More Info`
 * [later](https://github.com/microsoft/TypeScript/issues/44334#issuecomment-5729091935) **NoelAbrahams** said "@RyanCavanaugh I no longer have access to that codebase, so, sorry, can't follow this up."
 * (later) **NoelAbrahams** closed the issue

### [PR microsoft/TypeScript#63926](https://github.com/microsoft/TypeScript/pull/63926) (Closed, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Negated Types**

*Add support for a 'not T' negated type operator with canonical simplification rules and enhanced control flow handling*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/63926#issuecomment-5706132673) **typescript-automation[bot]** reported build result differences when comparing main with the pull request merge across the top 1000 repos and highlighted a failure in advaitpaliwal/feynman
 * [yesterday](https://github.com/microsoft/TypeScript/pull/63926#issuecomment-5706132806) **typescript-automation[bot]** reported build failures from the top 1000 repos suite showing TS2322 errors in corsairdev/corsair tsconfig files
 * [yesterday](https://github.com/microsoft/TypeScript/pull/63926#issuecomment-5706132906) **typescript-automation[bot]** reported build errors for diegosouzapw/OmniRoute from the top 1000 repos suite
 * [today](https://github.com/microsoft/TypeScript/pull/63926#issuecomment-5720816912) **weswigham** requested the typescript-bot to test the top1000 and expressed hope for less output
 * [today](https://github.com/microsoft/TypeScript/pull/63926#issuecomment-5720818089) **typescript-automation[bot]** reported that the test top1000 build jobs had started and that it would update status as they complete
 * [today](https://github.com/microsoft/TypeScript/pull/63926#issuecomment-5721053286) **jakebailey** fixed the user test runner using an old version of node and reran tests
 * [today](https://github.com/microsoft/TypeScript/pull/63926#issuecomment-5721054932) **typescript-automation[bot]** reported that the test top1000 job started and indicated the comment will be updated with build results

### [PR microsoft/TypeScript#63986](https://github.com/microsoft/TypeScript/pull/63986) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Don't reuse emit resolvers cross\-file**

*Reusing emit resolvers across files leads to race conditions that alter declaration emit outputs.*

 * (2 weeks ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#63987](https://github.com/microsoft/TypeScript/pull/63987) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Redo localization for onboarding**

*Reorganize localization files and pipeline to match loc team expectations and automate diagnostics exports and translation sync via PRs.*

 * (2 weeks ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/63987#issuecomment-5722003474) **jakebailey** said "One gotcha; we currently prune unused localizations. Not sure if we can do that anymore here, at least in those artifacts."
 * [today](https://github.com/microsoft/TypeScript/pull/63987#issuecomment-5722438642) **jakebailey** said "Classic copilot producing good feedback"

### [Issue microsoft/TypeScript#64154](https://github.com/microsoft/TypeScript/issues/64154) (Closed, `Domain: API`, **andrewbranch**)

**\[API\] Redesign client\-side snapshot state model**

*Redesign the client-side snapshot state model to unify overlapping updateSnapshot, createProgram, and virtual filesystem operations into a coherent transition system.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/64154#issuecomment-5533077334) **DanielRosenwasser** considered whether to expose a program update method without snapshot.update and suggested requiring snapshot.update or returning a [Program, Snapshot] pair
 * **DanielRosenwasser** added label `Domain: API`
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/64154#issuecomment-5578800244) **mrazauskas** suggested adding an option to programmatically set implied/enforced compiler options via api.createSnapshot and discussed a workaround using a virtual tsconfig file
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#64158](https://github.com/microsoft/TypeScript/pull/64158) (Open, `Author: Team`, `For Uncommitted Bug`, **iisaduan**)

**Build Orchestrator API **

*Implement a BuildOrchestrator API to programmatically build, clean, and manage project references in TypeScript 7.1 without watch mode.*

 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64158#issuecomment-5621539680) **dragomirtitian** asked whether the new BuildOrchestrator supports diagnostics retrieval, file-specific checks, batched emits, and SourceFile access and inquired about plans to add these features
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64158#issuecomment-5627049841) **iisaduan** explained the PR scope for build orchestrator diagnostics, deferred watch functionality to a future PR, noted that emit output isn't returned via IPC, and asked which tool was used for per-file diagnostics
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64158#issuecomment-5630670307) **dragomirtitian** asked if the incremental program could be reinstated and noted possible misunderstanding about emit output via VFS writes
 * [today](https://github.com/microsoft/TypeScript/pull/64158#issuecomment-5723381271) **andrewbranch** asked which incremental-specific Program APIs were needed beyond altered construction/emit behavior and whether they used emitBuildInfo(), getSemanticDiagnosticsOfNextAffectedFile(), emitNextAffectedFile(), or others
 * [later](https://github.com/microsoft/TypeScript/pull/64158#issuecomment-5729268673) **dragomirtitian** explained their usage of the incremental program APIs and workflow, including creating an incremental compiler host, caching ASTs, invoking diagnostics, and emitting changed files

### [Issue microsoft/TypeScript#64192](https://github.com/microsoft/TypeScript/issues/64192) (Closed, `Possible Improvement`, **ahejlsberg**)

**Recursive inference through self\-referential object literals**

*Self-referential getters for recursive schemas trigger TypeScript's self-reference errors collapsing to implicit any, requiring Zod-style workarounds.*

 * [1 week ago](https://github.com/microsoft/TypeScript/issues/64192#issuecomment-5594283251) **colinhacks** cross-posted a link to TypeScript PR 64172 for context, highlighted recursive type inference as a high-impact challenge, described Zod 4's loosened type safety workaround, and requested a solution preserving type safety
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/64192#issuecomment-5606700713) **devanshj** demonstrated how PR #64091 could fix the recursive typing issue with example TypeScript code and invited testing of PR #64092
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/64192#issuecomment-5616093710) **devanshj** demonstrated a generic utility function that solves the circular reference issue without library coupling or API changes
 * (today) **ahejlsberg** added label `Possible Improvement`, removed label `Needs Investigation`, and set milestone to `TypeScript 7.1.0 Beta`
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript#64204](https://github.com/microsoft/TypeScript/pull/64204) (Closed, `Author: Team`, `For Milestone Bug`, **andrewbranch**)

**Replace \`api\.updateSnapshot\`**

*Refactor snapshot API by removing api.updateSnapshot and introducing createSnapshot, getCurrentLanguageServerSnapshot, and snapshot.update operations.*

 * (1 week ago) **typescript-automation[bot]** added labels `Author: Team`, `For Milestone Bug`
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64204#issuecomment-5594173035) **andrewbranch** said "I have a refactor on top of this to use strongly typed project IDs that are not just tspath.Path, but it was a big diff so I didn't include it in this branch. It's a very nice cleanup though."
 * [today](https://github.com/microsoft/TypeScript/pull/64204#issuecomment-5721629954) **andrewbranch** described the existing test coverage from sibling snapshots, auto-import snapshots, and temporary file update snapshots that have reinforced immutability guarantees
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#64208](https://github.com/microsoft/TypeScript/pull/64208) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Keep computed\-name reconstruction out of symbol tracking**

*Prevent computed-name reconstruction during symbol tracking by adding a test and implementing a fix for #63986.*

 * (1 week ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64211](https://github.com/microsoft/TypeScript/pull/64211) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Use gotestsum as a Go tool**

*Integrate gotestsum as a Go tool to silence unpinned dependency alerts and streamline the test experience.*

 * (1 week ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64216](https://github.com/microsoft/TypeScript/pull/64216) (Closed, `Author: Team`, `For Uncommitted Bug`, **johnfav03**)

**Port \`createSourceFile\` and \`createSourceFileFromFile\`**

*Port createSourceFile and createSourceFileFromFile to the TypeScript API with the defined function signatures.*

 * (1 week ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **johnfav03**
 * [today](https://github.com/microsoft/TypeScript/pull/64216#issuecomment-5721880148) **jakebailey** said "PR needs a reformat"
 * (today) **johnfav03** closed the issue

### [PR microsoft/TypeScript#64248](https://github.com/microsoft/TypeScript/pull/64248) (Closed, `For Backlog Bug`)

**Infer recursive types through self\-referential object literals**

*Enable correct recursive type inference in self-referential object literals by deferring type constraint checks.*

 * created by **colinhacks**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/64248#issuecomment-5731630437) **ahejlsberg** said "Superseded by #64311 which is now merged."
 * (later) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#64251](https://github.com/microsoft/TypeScript/issues/64251) (Open, `Possible Improvement`)

**Object with all context\-sensitive properties requires at least one non\-context\-sensitive property for inference to work**

*createMachine type inference for context and state fails when all state properties are context-sensitive unless a dummy property is added*

 * [3 days ago](https://github.com/microsoft/TypeScript/issues/64251#issuecomment-5670374974) **RyanCavanaugh** said "@Andarist any thoughts (on this or the PR) ?"
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/64251#issuecomment-5670580961) **RyanCavanaugh** said "Copilot cites #48798 as prior work in this area, with #54029 as a superset of the linked PR"
 * [yesterday](https://github.com/microsoft/TypeScript/issues/64251#issuecomment-5703861215) **Andarist** referenced pull request 54029 as a duplicate of the issue, noted it didn't cover all cases, and mentioned preparing a revised PR for TS Go
 * [today](https://github.com/microsoft/TypeScript/issues/64251#issuecomment-5719068699) **devanshj** noted that Identity was a workaround and asked if the PR could type a provided example

### [PR microsoft/TypeScript#64256](https://github.com/microsoft/TypeScript/pull/64256) (Closed, `For Uncommitted Bug`, `dependencies`, `github_actions`)

**Bump the github\-actions group with 5 updates**

*Upgrade five GitHub Actions packages: azure/login to 3.1.0, download-artifact to 8.0.1, and CodeQL actions to 4.38.0.*

 * (4 days ago) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`, `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64256#issuecomment-5718595056) **dependabot[bot]** said "Looks like these dependencies are updatable in another way, so this is no longer needed."
 * (today) **dependabot[bot]** closed the issue

### [PR microsoft/TypeScript#64258](https://github.com/microsoft/TypeScript/pull/64258) (Closed, `For Uncommitted Bug`)

**Fix spelling of occurred in cross\-project panic handling**

*Renames incorrectly spelled panicsOccured and panicOccured identifiers to panicsOccurred and panicOccurred in crossproject.go.*

 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/64258#issuecomment-5660152614) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/64258#issuecomment-5660166165) **tanvir-ux** said "Linked issue: #64259."
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#64259](https://github.com/microsoft/TypeScript/issues/64259) (Closed)

**Misspelling: panicsOccured / panicOccured in crossproject\.go**

*Correct misspelled identifiers panicsOccured and panicOccured to panicsOccurred and panicOccurred in tsc/internal/ls/crossproject.go*

 * created by **tanvir-ux**
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#64279](https://github.com/microsoft/TypeScript/issues/64279) (Closed, **jakebailey**, **Copilot**)

**JSDoc \`@type\` on a function: the type in a type predicate is never checked \(unused \`@import\` reported, missing names not reported\)**

*TypeScript 7.0.2+ erroneously flags imported types used solely in JSDoc @type function type predicates as unused, causing TS6196 errors.*

 * [yesterday](https://github.com/microsoft/TypeScript/issues/64279#issuecomment-5706943362) **jakebailey** said "No, this form should still work, I'm pretty sure."
 * (yesterday) **jakebailey** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/issues/64279#issuecomment-5720619357) **ljharb** said "also, the types for a function expression vs declaration shouldn't behave differently - they're basically the same thing."
 * [today](https://github.com/microsoft/TypeScript/issues/64279#issuecomment-5720649019) **jakebailey** said "I don't follow; do you have an example where this is broken?"
 * [today](https://github.com/microsoft/TypeScript/issues/64279#issuecomment-5720674636) **ljharb** clarified that he was replying to a previous comment and asserted that every function should accept @type regardless of declaration or expression

### [PR microsoft/TypeScript#64286](https://github.com/microsoft/TypeScript/pull/64286) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Update main for TS7 tagged releases**

*Prepare the main branch for TypeScript 7 tagged releases in anticipation of the upcoming 7.0.3 release.*

 * (2 days ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64287](https://github.com/microsoft/TypeScript/pull/64287) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Update release\-7\.0 for TS7 tagged releases**

*Update the release-7.0 branch with essential changes required for TS7 tagged releases.*

 * (2 days ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64305](https://github.com/microsoft/TypeScript/pull/64305) (Closed, `For Uncommitted Bug`)

**perf: avoid duplicate symbol link lookup in \`GetNameTypeOfSymbol\`**

*Remove redundant TryGet call in GetNameTypeOfSymbol to avoid duplicate symbol link lookup and improve performance.*

 * created by **camc314**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64305#issuecomment-5709911469) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64306](https://github.com/microsoft/TypeScript/pull/64306) (Closed, `For Uncommitted Bug`)

**perf: preallocate instantiated symbol table**

*Preallocate the instantiated symbol table to its known size to avoid intermediate reallocations.*

 * (yesterday) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64306#issuecomment-5710355492) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64311](https://github.com/microsoft/TypeScript/pull/64311) (Closed, `Author: Team`, `For Milestone Bug`, **ahejlsberg**)

**Suppress type argument constraint checks in recursive call resolution**

*Suppress type parameter constraint checks during recursive call resolution to avoid circularity errors in constrained generic functions.*

 * created by **ahejlsberg**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript/pull/64311#issuecomment-5717811436) **ahejlsberg** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/64311#issuecomment-5717812686) **typescript-automation[bot]** posted build status updates
 * (today) **typescript-automation[bot]** added label `For Milestone Bug`, and removed label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64311#issuecomment-5718136601) **typescript-automation[bot]** reported the results of the requested performance run
 * [today](https://github.com/microsoft/TypeScript/pull/64311#issuecomment-5718319197) **typescript-automation[bot]** notified @ahejlsberg that DT test results were ready and unchanged
 * [today](https://github.com/microsoft/TypeScript/pull/64311#issuecomment-5722696435) **ahejlsberg** invoked typescript-bot to run tests
 * [today](https://github.com/microsoft/TypeScript/pull/64311#issuecomment-5722697025) **typescript-automation[bot]** reported build job statuses and results for 'user test this' and 'test top400'
 * [today](https://github.com/microsoft/TypeScript/pull/64311#issuecomment-5722918284) **typescript-automation[bot]** reported infrastructure failures but that tests otherwise passed for the pull request merge
 * [today](https://github.com/microsoft/TypeScript/pull/64311#issuecomment-5723297089) **typescript-automation[bot]** reported that running the top 400 repos with tsc comparing main and the pull request merge showed everything looked good
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript#64312](https://github.com/microsoft/TypeScript/issues/64312) (Open, `Bug`, `Needs Proposal`)

**\`checkJs\` skips \`\.mjs\`/\`\.cjs\` beside a \`\.d\.mts\`/\`\.d\.cts\`, but not \`\.js\` beside a \`\.d\.ts\`**

*TypeScript’s checkJs mode skips .mjs and .cjs files beside .d.mts/.d.cts declarations but not .js beside .d.ts*

 * created by **ljharb**

### [PR microsoft/TypeScript#64313](https://github.com/microsoft/TypeScript/pull/64313) (Closed, `For Uncommitted Bug`, `dependencies`, `github_actions`)

**Bump the github\-actions group across 1 directory with 6 updates**

*Update six GitHub Actions in the repository's root directory to their latest versions including azure/login, download-artifact, codecov, and CodeQL actions.*

 * created by **dependabot[bot]**
 * (today) **dependabot[bot]** added labels `dependencies`, `github_actions`, `dependencies`, `github_actions`
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#64314](https://github.com/microsoft/TypeScript/issues/64314) (Closed, `Duplicate`)

**False\-positive \`unintentional comparison\` error with closures**

*TypeScript’s language service incorrectly flags valid comparisons on a union-typed variable as unintentional after the variable is updated within a closure.*

 * created by **e-kucheriavyi**
 * [today](https://github.com/microsoft/TypeScript/issues/64314#issuecomment-5720680826) **MartinJohns** said "Duplicate of #9998."
 * **RyanCavanaugh** added label `Duplicate`

### [PR microsoft/TypeScript#64315](https://github.com/microsoft/TypeScript/pull/64315) (Closed, `Author: Team`, `For Uncommitted Bug`, **RyanCavanaugh**)

**Update SECURITY\.md with TypeScript security properties**

*Add TypeScript security properties section and reporting guidelines to SECURITY.md with a root link to the wiki.*

 * created by **RyanCavanaugh**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **RyanCavanaugh**
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#64316](https://github.com/microsoft/TypeScript/pull/64316) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Readd Knip unused code checks**

*Reintroduce Knip for unused code detection and remove obsolete code from the repository.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#64317](https://github.com/microsoft/TypeScript/pull/64317) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Cherry\-pick tsgo PR 4535 into release\-7\.0**

*Cherry-pick TypeScript-Go PR 4535 into the release-7.0 branch.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#64318](https://github.com/microsoft/TypeScript/pull/64318) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Cherry\-pick tsgo PR 4658 into release\-7\.0**

*Cherry-pick PR 4658 from tsgo into the release-7.0 branch to resolve issue 64262.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#64319](https://github.com/microsoft/TypeScript/pull/64319) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**Add typed project IDs**

*Replace generic tspath.Path IDs with distinct strongly typed string IDs for configured, inferred, and synthetic projects.*

 * created by **andrewbranch**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **andrewbranch**

### [PR microsoft/TypeScript#64320](https://github.com/microsoft/TypeScript/pull/64320) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**Move printer to top level, add printFile method**

*Relocate the printer to the top level and implement a new printFile method.*

 * created by **andrewbranch**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript/pull/64320#issuecomment-5722694716) **jakebailey** said "Oh, that last suppressed comment might actually be real"
 * [today](https://github.com/microsoft/TypeScript/pull/64320#issuecomment-5723344963) **andrewbranch** said "Ugh sorry, missed a test run after rebase"
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#64321](https://github.com/microsoft/TypeScript/pull/64321) (Open, `For Uncommitted Bug`)

**perf: preallocate inherited member symbol table**

*Preallocate the inherited member symbol table using its known size to avoid unnecessary reallocations.*

 * created by **camc314**
 * [today](https://github.com/microsoft/TypeScript/pull/64321#issuecomment-5724566154) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64321#issuecomment-5725605595) **jakebailey** asked how many hints are too large and whether Go map default sizing matters

### [Issue microsoft/TypeScript#64322](https://github.com/microsoft/TypeScript/issues/64322) (Closed, **jakebailey**, **Copilot**)

**\[Bug\] PrivateIdentifier nodes are omitted from 2020 semantic classifications**

*ECMAScript private fields and methods are omitted from TypeScript 2020 semantic classifications, preventing proper property and method highlighting.*

 * created by **VALLIS-NERIA**
 * [later](https://github.com/microsoft/TypeScript/issues/64322#issuecomment-5732373176) **jakebailey** said "You're linking to code that doesn't exist anymore; 7.0+ has a totally different implementation, can you please try again with the latest version?"

