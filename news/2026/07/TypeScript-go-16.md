# Report for 2026-07-16 (Thursday, July 16th, 2026)

9 different users commented on 26 different issues.

## Recommended Actions

 * Response Recommended
    * @shining-mind asked if the proposal should be moved to the typescript-go repository in [microsoft/TypeScript-go#2824](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-5004116575)

## Activity Summary

### [Issue microsoft/TypeScript-go#2824](https://github.com/microsoft/TypeScript-go/issues/2824) (Open, `Domain: API and Extensibility`, **andrewbranch**)

**API usage patterns for complex editor extensions**

*Exploring IPC-based API features for a Go TS server to replace TS Server plugins and support Vue editor extensions*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-4983029792) **nikelborm** shared a report evaluating and comparing a matrix of bridging strategies
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-4983158061) **andrewbranch** clarified that the issue aimed to achieve TS 7 parity with TS 6 by proposing LSP-only plugins, noted feedback that certain CLI capabilities require central tsc coordination, and argued against expanding to a broad CLI plugin scope to avoid delaying parity
 * [today](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-4991793665) **shining-mind** agreed and asked whether there were plans to create a dedicated feature request for CLI support for typechecking Vue, Svelte, and string template literals
 * [today](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-4994605079) **andrewbranch** said "https://github.com/microsoft/typescript/issues/45886 is basically that."
 * [later](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-5004116575) **shining-mind** asked if the proposal should be moved to the typescript-go repo

### [Issue microsoft/TypeScript-go#4017](https://github.com/microsoft/TypeScript-go/issues/4017) (Open, `Domain: Editor`, `possible improvement`, **DanielRosenwasser**, **Copilot**)

**Extension does not respect \`js/ts\.locale\`**

*The extension ignores js/ts.locale settings and always displays English error messages because it does not send locale to the server.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/4017#issuecomment-4897652991) **DanielRosenwasser** said "We'll reopen if people provide feedback."
 * (1 week ago) **DanielRosenwasser** closed the issue
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/4017#issuecomment-4988337023) **chikujoyayabo** requested reinstating the ability to override the TypeScript server locale to English separate from the global VS Code language due to poor Simplified Chinese translations
 * (today) **DanielRosenwasser** reopened the issue
 * (today) **DanielRosenwasser** set milestone to `TypeScript 7.1`, removed from milestone `Possible Improvement`, and assigned to **Copilot**, **DanielRosenwasser**

### [PR microsoft/TypeScript-go#4443](https://github.com/microsoft/TypeScript-go/pull/4443) (Closed, **andrewbranch**)

**Fixed build mode false negative from export\-star facade**

*Fix false negative TypeScript build-mode error caused by export-star facade usage.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4443#issuecomment-4847081152) **jakebailey** acknowledged the referenced issue and clarified that they had thought it was a new bug
 * **johnfav03** added to milestone `Post-7.0`
 * **RyanCavanaugh** assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4443#issuecomment-4997277857) **johnfav03** realized that the issue was fixed on main by PR #4301 and closed the PR; offered to open a new PR with just the regression test if desired
 * (today) **johnfav03** closed the issue

### [PR microsoft/TypeScript-go#4565](https://github.com/microsoft/TypeScript-go/pull/4565) (Closed, **weswigham**)

**Fix stack overflow in \`checkTypeExpandability\(\)\`**

*checkTypeExpandability fails to track reference type arguments, causing infinite recursion and stack overflow*

 * created by **johnfav03**
 * **RyanCavanaugh** assigned to **weswigham**
 * (today) **johnfav03** closed the issue

### [Issue microsoft/TypeScript-go#4579](https://github.com/microsoft/TypeScript-go/issues/4579) (Closed)

**tsgo typechecks slower than TS6**

*tsgo typechecking is over five times slower than TypeScript 6 on the same codebase.*

 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/4579#issuecomment-4948371190) **ahejlsberg** attributed the performance regression to a change in #3445, explained that TS7's deeper analysis led to more type instantiations compared to TS6, and suggested simplifying the types
 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/4579#issuecomment-4949748665) **XiNiHa** said "Do you mean the behavior is expected/intended? Should it be fixed from the library side?"
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/4579#issuecomment-4970222219) **ahejlsberg** said "@XiNiHa Yes, the behavior is expected. TS6 would similarly slow down if the changes in #3445 were applied to that codebase. The core problem is the complexity and expense of the types."
 * (today) **RyanCavanaugh** closed the issue
 * [later](https://github.com/microsoft/TypeScript-go/issues/4579#issuecomment-5000192828) **igalklebanov** described simplified helper function variants that reduced TypeScript instantiation counts without losing type safety

### [PR microsoft/TypeScript-go#4590](https://github.com/microsoft/TypeScript-go/pull/4590) (Closed)

**Fix "Token end is child end" crash on grammar error**

*Formatter crashes due to skipping grammar-error child nodes without advancing the scanner, causing mismatched token and AST child end positions.*

 * created by **johnfav03**
 * [6 days ago](https://github.com/microsoft/TypeScript-go/pull/4590#issuecomment-4939918614) **Andarist** said "note that my old PR already fixes this too: https://github.com/microsoft/typescript-go/pull/3102 . I just pushed out the test from this PR there"
 * (today) **johnfav03** closed the issue

### [Issue microsoft/TypeScript-go#4607](https://github.com/microsoft/TypeScript-go/issues/4607) (Open, `Crash`, **RyanCavanaugh**, **Copilot**)

**TypeScript 7\.0 Can't compile \`webpack\`**

*TypeScript 7.0 compiler panics with unexpected JSTypeAliasDeclaration nodes while compiling webpack*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/4607#issuecomment-4985037244) **RyanCavanaugh** asked for ideas after reporting TypeScript compilation errors and version details
 * **RyanCavanaugh** added label `Needs More Info`
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/4607#issuecomment-4986414764) **avivkeller** said "Hi! Sorry! It looks like I had declaration: true locally which was a requirement of the error, it seems. I'm still looking for a minimal repro."
 * [today](https://github.com/microsoft/TypeScript-go/issues/4607#issuecomment-4994581572) **RyanCavanaugh** said "No worries! Repro confirmed locally, I can reduce from here."
 * (today) **RyanCavanaugh** removed label `Needs More Info`, set milestone to `TypeScript 7.1`, and assigned to **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4607#issuecomment-4996255239) **weswigham** said "From the just the stack frame, I'm guessing a @typedef merged with a module.exports.Something = whatever."
 * [today](https://github.com/microsoft/TypeScript-go/issues/4607#issuecomment-4997380107) **RyanCavanaugh** provided a reproduction example and reported a compiler panic
 * **RyanCavanaugh** assigned to **Copilot**

### [Issue microsoft/TypeScript-go#4610](https://github.com/microsoft/TypeScript-go/issues/4610) (Open, `Domain: Editor`, `Needs Investigation`, **johnfav03**)

**Renaming a file can be very slow in some edge cases**

*VSCode tsgo file renames can be slow because a third-party .d.ts with repeated imports triggers quadratic path-updater scans.*

 * created by **pascalspadone**
 * **pascalspadone** added label `Domain: Editor`
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.1`, and assigned to **johnfav03**

### [Issue microsoft/TypeScript-go#4619](https://github.com/microsoft/TypeScript-go/issues/4619) (Open, `possible improvement`, **andrewbranch**)

**Improve API performance when using virtual file system**

*Include inline file content and precomputed directory listings in updateSnapshot to eliminate virtual file system IPC calls and improve performance.*

 * created by **dragomirtitian**
 * (yesterday) **RyanCavanaugh** added label `possible improvement`, and assigned to **andrewbranch**
 * **RyanCavanaugh** added to milestone `Possible Improvement`

### [PR microsoft/TypeScript-go#4625](https://github.com/microsoft/TypeScript-go/pull/4625) (Closed)

**VS enhanced hover: symbol icon \+ colorized text**

*Extend Corsa's LSP hover responses to include VS-specific icon and syntax coloring metadata for enhanced tooltips.*

 * created by **navya9singh**
 * (today) **navya9singh** closed the issue

### [PR microsoft/TypeScript-go#4655](https://github.com/microsoft/TypeScript-go/pull/4655) (Open)

**Fix stack overflow in \`getExplicitTypeOfSymbol\(\)\` for self\-referential \`for\.\.\.of\`**

*A self-referential for…of loop where the loop variable iterates over itself causes unbounded recursion in getExplicitTypeOfSymbol and leads to a stack overflow.*

 * created by **johnfav03**

### [PR microsoft/TypeScript-go#4656](https://github.com/microsoft/TypeScript-go/pull/4656) (Closed)

**Fix nil pointer dereference in signature help for error\-recovered parameter types**

*Signature help triggers a nil pointer dereference when error-recovered parameter type nodes are deep-cloned without parent pointers*

 * created by **johnfav03**
 * (today) **johnfav03** closed the issue

### [PR microsoft/TypeScript-go#4657](https://github.com/microsoft/TypeScript-go/pull/4657) (Closed)

**Add even more bails on unchecked identifiers to markLinkedReferences**

*Continue adding bail checks for unchecked identifiers in markLinkedReferences to address remaining diffs*

 * created by **weswigham**

### [PR microsoft/TypeScript-go#4658](https://github.com/microsoft/TypeScript-go/pull/4658) (Open)

**Fix build mode setup stall on large solutions**

*Introduce DirWatchSet to optimize computeDesiredWatches and reduce filesystem watch registration time in large tsc -b --watch solutions.*

 * created by **johnfav03**

### [PR microsoft/TypeScript-go#4659](https://github.com/microsoft/TypeScript-go/pull/4659) (Closed)

**Move baselines mistakenly put into TS\-1 group without TS\-1 into accepted**

*Remove trio of diffs mistakenly assigned to the TS-1 group despite lacking TS-1 consistency diagnostics.*

 * created by **weswigham**

### [PR microsoft/TypeScript-go#4660](https://github.com/microsoft/TypeScript-go/pull/4660) (Open, **DanielRosenwasser**, **Copilot**)

**Respect configured TypeScript diagnostic locale**

*Respect js/ts.locale and typescript.locale overrides for TypeScript diagnostics, restart the language server on changes, and fallback to auto display language.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **DanielRosenwasser**

### [PR microsoft/TypeScript-go#4661](https://github.com/microsoft/TypeScript-go/pull/4661) (Open)

**Fall back to inotify when filesystem has errors in fanotify \(fix watch in Docker\)**

*Fall back to inotify when fanotify watch registration fails on unsupported filesystems like Docker mounts so file changes are detected.*

 * created by **johnfav03**

### [PR microsoft/TypeScript-go#4662](https://github.com/microsoft/TypeScript-go/pull/4662) (Closed)

**Fix declaration emit synthesizing extensionless import\(\) specifier under allowImportingTsExtensions \+ nodenext**

*Declaration emit under allowImportingTsExtensions and nodenext stripped .js extensions from import() specifiers, causing TS2307 errors.*

 * created by **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4662#issuecomment-4997405723) **RyanCavanaugh** said "This is a redo of https://github.com/microsoft/typescript-go/pull/4649 but now GitHub API is down 🙁"

### [PR microsoft/TypeScript-go#4663](https://github.com/microsoft/TypeScript-go/pull/4663) (Open, **RyanCavanaugh**, **Copilot**)

**Fix crash: JSTypeAliasDeclaration passed to GetTypeOfDeclaration during CJS declaration emit**

*Restrict the declaration emit fallback to only inferrable declarations to avoid passing JSTypeAliasDeclaration to GetTypeOfDeclaration and prevent related crashes.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**

### [Issue microsoft/TypeScript-go#4664](https://github.com/microsoft/TypeScript-go/issues/4664) (Open)

**\`tsgo \-\-build\` incremental reports no errors after a dependency update batch that includes a global\-scope \.d\.ts change \(clean build errors\)**

*tsgo --build incremental mode fails to report newly introduced type errors after updating dependencies including a global-scope .d.ts change*

 * created by **martijnwalraven**

### [PR microsoft/TypeScript-go#4665](https://github.com/microsoft/TypeScript-go/pull/4665) (Open)

**Return all files from getFilesAffectedBy when a changed file affects global scope**

*Update getFilesAffectedBy to return all non-default-library files for global-scope changes to fix incremental invalidation.*

 * created by **martijnwalraven**
 * [later](https://github.com/microsoft/TypeScript-go/pull/4665#issuecomment-5001814259) **martijnwalraven** said "@microsoft-github-policy-service agree"

### [PR microsoft/TypeScript-go#4666](https://github.com/microsoft/TypeScript-go/pull/4666) (Open, `Voight-Kampff Anomaly`)

**POC: ambient module declarations keyed on import attributes**

*Proof-of-concept for ambient module declarations keyed by import attributes to support text or bytes file imports in TypeScript's Go port.*

 * created by **bartlomieju**
 * [later](https://github.com/microsoft/TypeScript-go/pull/4666#issuecomment-5004893772) **bartlomieju** said "@microsoft-github-policy-service agree"

