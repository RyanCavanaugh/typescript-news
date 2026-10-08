# Report for 2026-10-07 (Wednesday, October 7th, 2026)

24 different users commented on 56 different issues.

## Recommended Actions

 * Response Recommended
    * @michaelhazan asked why this feature wasn't integrated into TypeScript 7 in [microsoft/TypeScript#32063](https://github.com/microsoft/TypeScript/issues/32063#issuecomment-6055145510)
    * @leonidaz proposed potential solutions for handling non-exact matches in the TS 7.1 content mapper API in [microsoft/TypeScript#63879](https://github.com/microsoft/TypeScript/issues/63879#issuecomment-6047266432)
    * @elecmonkey asked about adding noEmit to OverrideCompilerOptions and offered to send a PR in [microsoft/TypeScript#64158](https://github.com/microsoft/TypeScript/pull/64158#issuecomment-6054576820)
    * @RedesignedRobot asked if they should open a PR with this fix in [microsoft/TypeScript#64605](https://github.com/microsoft/TypeScript/issues/64605#issuecomment-6053406731)

## Activity Summary

### [Issue microsoft/TypeScript#32063](https://github.com/microsoft/TypeScript/issues/32063) (Open, `Suggestion`, `Awaiting More Feedback`)

**import ConstJson from '\./config\.json' as const;**

*Allow importing a JSON config file with a const modifier to infer literal union types for its values.*

 * [19 weeks ago](https://github.com/microsoft/TypeScript/issues/32063#issuecomment-4557907356) **rfon6ngy** expressed support for @james-pre and agreed that patching each update was a pain
 * [13 weeks ago](https://github.com/microsoft/TypeScript/issues/32063#issuecomment-4883967601) **james-pre** explained how to use npm v12's built-in dependency patching to patch TypeScript by adding a patchedDependencies entry in package.json and linking to a gist-hosted patch file
 * [13 weeks ago](https://github.com/microsoft/TypeScript/issues/32063#issuecomment-4885857717) **Chinoman10** described how to use npm’s built-in dependency patching in v12 to apply a TypeScript patch and noted that Bun’s patch feature is faster
 * [later](https://github.com/microsoft/TypeScript/issues/32063#issuecomment-6055145510) **michaelhazan** noted that TypeScript 7's go compiler prevented previous patching and asked why the feature wasn't part of TypeScript

### [Issue microsoft/TypeScript#59342](https://github.com/microsoft/TypeScript/issues/59342) (Closed, `Needs Investigation`, **sheetalkamat**)

**⚡ Performance: Project service doesn't cache all fs\.realpath **

*typescript-eslint’s parserOptions.projectService makes multiple uncached fs.realpath calls, causing minor performance degradation during linting*

 * **sheetalkamat** assigned to **sheetalkamat**
 * [1.2 years ago](https://github.com/microsoft/TypeScript/issues/59342#issuecomment-2997933155) **wagenet** said "@sheetalkamat any news here?"
 * **RyanCavanaugh** added label `Needs Investigation`
 * [today](https://github.com/microsoft/TypeScript/issues/59342#issuecomment-6047913730) **RyanCavanaugh** said "Closing as this is presumably moot in the new implementation"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63879](https://github.com/microsoft/TypeScript/issues/63879) (Open, `Suggestion`)

**feat\(contentmapper\): support whole\-symbol rename edit projection**

*Support safe whole-symbol rename projections in the Content Mapper protocol to correctly map renamed symbols between authored and generated code*

 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63879#issuecomment-5999263358) **andrewbranch** refuted that separate language servers would be required, stating that the API provides access to the existing TypeScript language server process and its state
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63879#issuecomment-6004984124) **leonidaz** tested the 7.1.0-dev server and observed that extensions can connect and see unsaved changes but receive no Organize Imports edits or code fixes
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63879#issuecomment-6007343299) **andrewbranch** requested that the commenter engage in discussion in a personal, concise voice rather than through lengthy AI-generated text
 * [today](https://github.com/microsoft/TypeScript/issues/63879#issuecomment-6047266432) **leonidaz** explained that the TS 7.1 content mapper API only edits tokens when source substrings exactly match generated code, noted this is unrealistic due to formatting differences, and proposed two solutions: naive mapping with formatting loss or client-provided callbacks to adjust edits

### [Issue microsoft/TypeScript#64037](https://github.com/microsoft/TypeScript/issues/64037) (Open, `Bug`, **johnfav03**)

**npx tsc \-w is triggering itself after each build**

*npx tsc --watch enters a build loop because output JavaScript files alongside TypeScript sources continuously retrigger compilation.*

 * [5 weeks ago](https://github.com/microsoft/TypeScript/issues/64037#issuecomment-5441005231) **msab-john** said "I'll see if I can make a small and simple one..."
 * [1 month ago](https://github.com/microsoft/TypeScript/issues/64037#issuecomment-5527566209) **nstepien** described a simple repro of tsc --watch triggering on new directory creation and noted missing logging of the trigger source
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/64037#issuecomment-6002184086) **njmarsh** provided a reproduction case on 7.0.2 showing that writes under excluded directories still triggered rebuilds in watch mode
 * (today) **RyanCavanaugh** added label `Bug`, removed label `Needs More Info`, and assigned to **johnfav03**

### [PR microsoft/TypeScript#64158](https://github.com/microsoft/TypeScript/pull/64158) (Closed, `Author: Team`, `For Uncommitted Bug`, **iisaduan**)

**Build Orchestrator API **

*Introduce a BuildOrchestrator API in TS7.1 replacing SolutionBuilder to perform project builds, cleans, and their references with customizable options.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/64158#issuecomment-5786468443) **andrewbranch** said "@dragomirtitian I have a draft up at https://github.com/microsoft/TypeScript/pull/64401; it probably has some bugs, but can you see if that direction meets your needs?"
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64158#issuecomment-5839239607) **andrewbranch** said "It would probably be worthwhile to update the PR description to reflect the latest review changes since PRs are all the docs we have for the moment."
 * (1 week ago) **iisaduan** closed the issue
 * [later](https://github.com/microsoft/TypeScript/pull/64158#issuecomment-6054576820) **elecmonkey** asked about adding noEmit to OverrideCompilerOptions and offered to send a PR

### [PR microsoft/TypeScript#64307](https://github.com/microsoft/TypeScript/pull/64307) (Open, `For Uncommitted Bug`)

**Normalize distributed type parameters in conditional type relationships**

*Normalize distributed type parameters on both source and target sides in conditional type relationships to resolve asymmetry and fix a regression*

 * (2 weeks ago) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/64307#issuecomment-5712772919) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [today](https://github.com/microsoft/TypeScript/pull/64307#issuecomment-6042790880) **trevorade** requested adding `Fixes #64673` to the PR description to link the issue

### [PR microsoft/TypeScript#64411](https://github.com/microsoft/TypeScript/pull/64411) (Open, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Preserve primitive literal union origins without special intersections**

*Preserve literal union origins for string, number, and bigint in completions and quick info without special intersections.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/64411#issuecomment-6028254590) **typescript-automation[bot]** reported that test results comparing baseline and PR looked good
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64411#issuecomment-6028261676) **typescript-automation[bot]** reported the perf run results for the requested baseline vs PR comparison
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64411#issuecomment-6028877744) **typescript-automation[bot]** provided build comparison results for the top 400 repos and requested review of interesting changes
 * [today](https://github.com/microsoft/TypeScript/pull/64411#issuecomment-6044727646) **weswigham** reported that every failure traced back to removal of mapped type support and described resulting index signature and type identity comparison issues that were fixed
 * [today](https://github.com/microsoft/TypeScript/pull/64411#issuecomment-6044729387) **typescript-automation[bot]** posted an automated build status update for multiple commands
 * [today](https://github.com/microsoft/TypeScript/pull/64411#issuecomment-6045143118) **typescript-automation[bot]** reported branch-only errors in DT tests for oojs-ui and react packages
 * [today](https://github.com/microsoft/TypeScript/pull/64411#issuecomment-6045250469) **typescript-automation[bot]** posted the requested performance run results with detailed comparison metrics
 * [today](https://github.com/microsoft/TypeScript/pull/64411#issuecomment-6045283819) **typescript-automation[bot]** reported that test results comparing baseline and PR looked good
 * [today](https://github.com/microsoft/TypeScript/pull/64411#issuecomment-6045948560) **typescript-automation[bot]** reported build results for the top 400 repos comparing baseline and PR and highlighted failures in pixijs
 * [today](https://github.com/microsoft/TypeScript/pull/64411#issuecomment-6046992714) **weswigham** said "@typescript-bot test it again just to check the further improvements to the control flow logic for retaining literal origins don't break anything new"
 * [today](https://github.com/microsoft/TypeScript/pull/64411#issuecomment-6047064591) **weswigham** requested the typescript-bot to run tests and expressed sadness
 * [today](https://github.com/microsoft/TypeScript/pull/64411#issuecomment-6047066823) **typescript-automation[bot]** posted an automated CI status update with build commands and links
 * [today](https://github.com/microsoft/TypeScript/pull/64411#issuecomment-6047492381) **typescript-automation[bot]** reported branch-only errors in DT tests for oojs-ui and react packages
 * [today](https://github.com/microsoft/TypeScript/pull/64411#issuecomment-6047533096) **typescript-automation[bot]** posted the results of the requested performance run
 * [today](https://github.com/microsoft/TypeScript/pull/64411#issuecomment-6047591133) **typescript-automation[bot]** reported that test results comparing baseline and PR looked good
 * [today](https://github.com/microsoft/TypeScript/pull/64411#issuecomment-6048381655) **typescript-automation[bot]** reported build results for the top 400 repos comparing baseline and PR and highlighted failures in pixijs

### [Issue microsoft/TypeScript#64464](https://github.com/microsoft/TypeScript/issues/64464) (Closed, `Needs Investigation`, **johnfav03**)

**First incremental rebuild after a clean build is up to 75× slower than a full check**

*First incremental rebuild after a clean build can be up to 75× slower than a full type check in TypeScript*

 * created by **resure**
 * (1 week ago) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **johnfav03**
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript#64469](https://github.com/microsoft/TypeScript/pull/64469) (Closed, `For Uncommitted Bug`, **johnfav03**)

**Index re\-exporting modules for declaration emit**

*Optimize TypeScript’s declaration emit performance by caching an export-to-module index to avoid repeated scans during incremental rebuilds*

 * **typescript-automation[bot]** assigned to **johnfav03**
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64469#issuecomment-6021277912) **weswigham** asked to split the two changes into separate PRs and noted that each should be evaluated independently
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64469#issuecomment-6025419461) **resure** provided split PR link after splitting the changes into separate PRs
 * [today](https://github.com/microsoft/TypeScript/pull/64469#issuecomment-6045049497) **weswigham** said "@typescript-bot perf test this"
 * [today](https://github.com/microsoft/TypeScript/pull/64469#issuecomment-6045051563) **typescript-automation[bot]** reported that performance tests had started and provided status and result links
 * [today](https://github.com/microsoft/TypeScript/pull/64469#issuecomment-6045519113) **typescript-automation[bot]** posted the requested perf run results including metrics for errors, symbols, types, memory usage, and memory allocations
 * [today](https://github.com/microsoft/TypeScript/pull/64469#issuecomment-6046261147) **weswigham** observed no performance regression and asked for a large public repository demonstrating the fixed performance issue to add to the perf test suite
 * (today) **weswigham** closed the issue
 * [later](https://github.com/microsoft/TypeScript/pull/64469#issuecomment-6062593250) **resure** provided Spotify's Backstage as a large public repo example and benchmarked performance improvements with metrics

### [PR microsoft/TypeScript#64588](https://github.com/microsoft/TypeScript/pull/64588) (Open, `For Uncommitted Bug`)

**Restore symbol names in JSX import action titles**

*Restores symbol names in JSX import action titles by porting Strada’s logic and fixes two skipped tests.*

 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [5 days ago](https://github.com/microsoft/TypeScript/pull/64588#issuecomment-5953399343) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [5 days ago](https://github.com/microsoft/TypeScript/pull/64588#issuecomment-5957506745) **jakebailey** said "Copilot absolutely hates this 😄 "
 * [later](https://github.com/microsoft/TypeScript/pull/64588#issuecomment-6056683833) **Andarist** noted disagreement with Copilot suggestions and asked if anything else should be addressed after adding extra coverage

### [PR microsoft/TypeScript#64599](https://github.com/microsoft/TypeScript/pull/64599) (Open, `For Milestone Bug`, **weswigham**)

**Check package reachability before using exports in declarations**

*Reorder TypeScript’s export resolution logic to ensure package reachability is checked before applying exports in declarations*

 * (yesterday) **typescript-automation[bot]** added label `For Milestone Bug`, removed label `For Uncommitted Bug`, and assigned to **weswigham**
 * [later](https://github.com/microsoft/TypeScript/pull/64599#issuecomment-6054835458) **Andarist** said "@weswigham I resolved the conflicts, the PR should be ready to land now"

### [Issue microsoft/TypeScript#64605](https://github.com/microsoft/TypeScript/issues/64605) (Open, `Needs Investigation`, **gabritto**)

**TS5115 in published Zod 4\.5–4\.6 types after \#64372**

*Zod 4.5.0–4.6.5 z.json() types cause TS5115 infinite circularity errors in TypeScript 7.1 nightlies after PR #64372, impacting ~62M weekly downloads.*

 * (yesterday) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.1.1 RC`, and assigned to **gabritto**
 * [today](https://github.com/microsoft/TypeScript/issues/64605#issuecomment-6053406731) **RedesignedRobot** traced the cause of a recursive member resolution issue introduced by #64372, proposed a fix that preserves declared members on a stack during inheritance resolution, reported passing tests and a cleaned-up baseline, and offered to open a PR

### [Issue microsoft/TypeScript#64611](https://github.com/microsoft/TypeScript/issues/64611) (Open, `Suggestion`)

**In\-memory virtual file overlay over LSP without faking \`didOpen\`**

*Add an LSP overlay mechanism to inject synthetic in-memory files into TS-Go’s virtual file system without faking didOpen notifications.*

 * [yesterday](https://github.com/microsoft/TypeScript/issues/64611#issuecomment-6027132277) **weswigham** noted that tsgo --api lacked certain language service requests (hover, definition, rename, references) and offered to prioritize exposing the missing TS6 backing APIs if provided a list, mentioning that @iisaduan is working on an API diff
 * [yesterday](https://github.com/microsoft/TypeScript/issues/64611#issuecomment-6027930040) **atscott** identified gaps in the API surface, listing missing LSP handlers in Project.languageService and required snapshot persistence enhancements
 * [today](https://github.com/microsoft/TypeScript/issues/64611#issuecomment-6037027784) **Lojhan** asked whether content mapping was the intended way or if another API was planned to make transformed source available to the shared TS language server for SQL tagged templates in .ts/.tsx files
 * [today](https://github.com/microsoft/TypeScript/issues/64611#issuecomment-6043534577) **andrewbranch** mentioned plans to investigate content mapping for tagged template strings and suggested using a separate server with an API connection and issue #64583 as a workaround
 * [today](https://github.com/microsoft/TypeScript/issues/64611#issuecomment-6047766832) **weswigham** suggested combining PR #64679 with the missing LS APIs to manage state over API connections and avoid resending unchanged FS data
 * [today](https://github.com/microsoft/TypeScript/issues/64611#issuecomment-6048779449) **atscott** said "Oh, yea that looks like it'll work nicely"

### [Issue microsoft/TypeScript#64627](https://github.com/microsoft/TypeScript/issues/64627) (Closed, `Bug`)

**\`import defer "\./a\.js"\` is accepted without an error, and the output drops \`defer\`**

*TypeScript incorrectly accepts and strips 'import defer "./a.js"' instead of reporting a syntax error.*

 * created by **leonidaz**
 * **RyanCavanaugh** added label `Bug`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64640](https://github.com/microsoft/TypeScript/pull/64640) (Closed, `For Uncommitted Bug`)

**fix\(64627\): reject deferred imports without namespace bindings**

*The compiler now rejects deferred imports that lack a namespace binding.*

 * created by **a-tarasyuk**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64642](https://github.com/microsoft/TypeScript/pull/64642) (Closed, `For Uncommitted Bug`)

**Fix \`workspace/symbol\` crash on an inferred project without a program**

*workspace/symbol requests crash on inferred TypeScript projects without an associated program.*

 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/64642#issuecomment-5995071174) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64642#issuecomment-6027175861) **andrewbranch** asked whether the issue was with WithSnapshotLoadingProjectTree not updating the inferred project while the workspace symbol handler included it
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#64647](https://github.com/microsoft/TypeScript/pull/64647) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**\[api\] Expose API client modules from VS Code extension**

*Expose TypeScript API client modules via the VS Code extension so third-party extensions resolve matching client versions for LSP servers.*

 * (2 days ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#64651](https://github.com/microsoft/TypeScript/pull/64651) (Closed, `For Uncommitted Bug`)

**Fix crashes on malformed destructuring assignments during emit**

*Allow processing of malformed destructuring AST nodes by removing strict asserts to prevent emit crashes.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/64651#issuecomment-6021288026) **jakebailey** asked if Strada had experienced this problem before or if it was new
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64651#issuecomment-6021855163) **Andarist** explained that Strada had the same assertions and crashes, showed where Strada expected a wider type but asserted a subtype, and noted that the Corsa PR loosens the asserts to match Strada's type allowances
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64651#issuecomment-6026169246) **jakebailey** said "I think this is probably fine but would like @weswigham to take a peek."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64657](https://github.com/microsoft/TypeScript/pull/64657) (Open, `For Milestone Bug`, **weswigham**)

**Show the JSDoc written on an \`import x = a\.x\` alias in hover and completions**

*Enable display of alias-specific JSDoc comments on import aliases during hover and completions.*

 * (yesterday) **typescript-automation[bot]** added label `For Milestone Bug`, removed label `For Uncommitted Bug`, and assigned to **weswigham**
 * [today](https://github.com/microsoft/TypeScript/pull/64657#issuecomment-6048754588) **patrickkettner** offered to widen the PR to show the whole chain on both refs, noting preference for that approach and explaining prior decision to maintain parity with version 6.0

### [PR microsoft/TypeScript#64658](https://github.com/microsoft/TypeScript/pull/64658) (Open, `For Uncommitted Bug`, **DanielRosenwasser**, **Copilot**)

**Fix Windows module resolution for reserved path segments**

*Use extended path namespaces to prevent Windows reserved device names like con from blocking module resolution.*

 * **Copilot** assigned to **DanielRosenwasser**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64658#issuecomment-6023711474) **Copilot** addressed the issue in commit be35d253, retained original fast paths, gated allocation-free component scan to reserved-name paths, and added zero-allocation coverage for the detector
 * [today](https://github.com/microsoft/TypeScript/pull/64658#issuecomment-6045856374) **DanielRosenwasser** said "@copilot does it make sense to just try realpath and do the scan only if that doesn't work? It's extremely uncommon to have these device names."
 * [today](https://github.com/microsoft/TypeScript/pull/64658#issuecomment-6046126151) **Copilot** updated implementation to run original path open first and trigger reserved-component scan only on failure, preventing scan cost on successful realpaths

### [Issue microsoft/TypeScript#64661](https://github.com/microsoft/TypeScript/issues/64661) (Open, `Bug`)

**Class names \`eval\` and \`arguments\` are not reported as invalid strict mode bindings**

*TypeScript fails to report errors for class names 'eval' or 'arguments' as invalid strict-mode bindings, causing runtime errors.*

 * created by **JLHwung**
 * (today) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`

### [PR microsoft/TypeScript#64662](https://github.com/microsoft/TypeScript/pull/64662) (Open, `Author: Team`, `For Backlog Bug`, **jakebailey**)

**Unify recursive type naming during serialization**

*Unify recursive type naming in serialization by replacing existing recursion trackers with a single approach for name reuse.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/64662#issuecomment-6027544711) **typescript-automation[bot]** reported performance run results
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64662#issuecomment-6027595319) **typescript-automation[bot]** reported test results comparing baseline and pr and flagged new type errors in bluebird tests
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64662#issuecomment-6028108984) **typescript-automation[bot]** reported that running the top 400 repos tsc comparison between baseline and pr succeeded without issues
 * [today](https://github.com/microsoft/TypeScript/pull/64662#issuecomment-6046287675) **jakebailey** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/64662#issuecomment-6046289425) **typescript-automation[bot]** reported CI job statuses with start and result links
 * [today](https://github.com/microsoft/TypeScript/pull/64662#issuecomment-6046696363) **typescript-automation[bot]** notified that the DT tests results were ready and unchanged
 * [today](https://github.com/microsoft/TypeScript/pull/64662#issuecomment-6046771773) **typescript-automation[bot]** reported test results comparing baseline and pr and flagged new type errors in bluebird tests
 * [today](https://github.com/microsoft/TypeScript/pull/64662#issuecomment-6046773996) **typescript-automation[bot]** posted the perf run results requested by @jakebailey
 * [today](https://github.com/microsoft/TypeScript/pull/64662#issuecomment-6047632196) **typescript-automation[bot]** reported that running the top 400 repos tsc comparison between baseline and pr succeeded without issues

### [Issue microsoft/TypeScript#64665](https://github.com/microsoft/TypeScript/issues/64665) (Closed, `Bug`)

**panic: Debug failure\. False expression: Undeclared private name for property declaration\.**

*Nightly TypeScript panics 'Undeclared private name for property declaration' when compiling a decorated class defining static and instance #a methods.*

 * created by **YuanchengJiang**
 * (today) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#64666](https://github.com/microsoft/TypeScript/issues/64666) (Open, `Bug`)

**panic: Diagnostic emitted without context**

*TypeScript nightly compiler panics with "Diagnostic emitted without context" when generating declarations for an interface extending a labeled interface.*

 * created by **YuanchengJiang**
 * (today) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#64667](https://github.com/microsoft/TypeScript/issues/64667) (Open, `Bug`)

**runtime error: invalid memory address or nil pointer dereference**

*TypeScript compiler panics with a nil pointer dereference when emitting declaration files using --stripInternal on an internal type alias.*

 * created by **YuanchengJiang**
 * (today) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#64668](https://github.com/microsoft/TypeScript/issues/64668) (Open, `Bug`)

**panic: Unhandled case in Node\.MemberList**

*TypeScript compiler panics with an unhandled Node.MemberList case when evaluating an enum member that references a class in a merged namespace.*

 * created by **YuanchengJiang**
 * (today) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#64669](https://github.com/microsoft/TypeScript/issues/64669) (Open, `Bug`)

**runtime error: invalid memory address or nil pointer dereference in getMembersOfSymbol**

*Assigning a computed property to a function causes a nil pointer panic in getMembersOfSymbol during declaration-only emit.*

 * created by **YuanchengJiang**
 * (today) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`

### [PR microsoft/TypeScript#64670](https://github.com/microsoft/TypeScript/pull/64670) (Closed, `For Backlog Bug`)

**fix\(64665\): fix emit crash for duplicate private names in decorated classes**

*Fixes emit crash due to duplicate private names in decorated classes.*

 * created by **a-tarasyuk**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (today) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64671](https://github.com/microsoft/TypeScript/pull/64671) (Open, `For Uncommitted Bug`, **RyanCavanaugh**)

**Do not pad binding elements that the parameter's type already types**

*padObjectLiteralType now respects annotated or contextual parameter types for destructured elements, avoiding false TS7031 errors.*

 * created by **Konan69**
 * (today) **typescript-automation[bot]** added label `For Uncommitted Bug`, and assigned to **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript/pull/64671#issuecomment-6042107580) **microsoft-github-policy-service[bot]** requested the user to agree to the Contributor License Agreement by replying with a formatted command

### [Issue microsoft/TypeScript#64672](https://github.com/microsoft/TypeScript/issues/64672) (Closed, `Bug`, **weswigham**, **RyanCavanaugh**, **Copilot**)

**CommonJS emit: \`exports\.x = x;\` is emitted inside a loop body in a function when a loop\-local variable shadows an exported name**

*The CommonJS emitter incorrectly places an export assignment inside a loop when a loop-local variable shadows the export.*

 * created by **trevorade**
 * (today) **RyanCavanaugh** added label `Bug`, and assigned to **Copilot**, **RyanCavanaugh**, **weswigham**
 * (today) **weswigham** closed the issue

### [Issue microsoft/TypeScript#64673](https://github.com/microsoft/TypeScript/issues/64673) (Open, `Needs Investigation`, **ahejlsberg**)

**TS2719 "Two different types with this name exist" between identical generic signatures with a distributive conditional parameter type \(regression from \#64237\)**

*After commit #64237, TypeScript wrongly reports TS2719 for identical generic signatures using distributive conditional types.*

 * created by **trevorade**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.1.1 RC`, and assigned to **ahejlsberg**

### [PR microsoft/TypeScript#64674](https://github.com/microsoft/TypeScript/pull/64674) (Closed, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Make computed property names always checked, regardless of parent grammar errors**

*Always enforce checking of computed property names despite parent grammar errors to prevent hidden diagnostics when using skipLibCheck.*

 * created by **weswigham**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`, and assigned to **weswigham**
 * [today](https://github.com/microsoft/TypeScript/pull/64674#issuecomment-6043451346) **weswigham** doubted that the change would fix most reported flakes and noted the need to observe telemetry results
 * [today](https://github.com/microsoft/TypeScript/pull/64674#issuecomment-6048062798) **jakebailey** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/64674#issuecomment-6048064666) **typescript-automation[bot]** reported CI jobs starting and completing with status and result links
 * [today](https://github.com/microsoft/TypeScript/pull/64674#issuecomment-6048441005) **typescript-automation[bot]** notified that the DT test results were ready and unchanged
 * [today](https://github.com/microsoft/TypeScript/pull/64674#issuecomment-6048475821) **typescript-automation[bot]** reported tsc user test results and confirmed everything looked good
 * [today](https://github.com/microsoft/TypeScript/pull/64674#issuecomment-6048484035) **typescript-automation[bot]** reported the perf run results for the requested comparison
 * (today) **weswigham** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/64674#issuecomment-6049098931) **typescript-automation[bot]** reported that running the top 400 repos tsc comparison between baseline and pr succeeded without issues

### [PR microsoft/TypeScript#64675](https://github.com/microsoft/TypeScript/pull/64675) (Closed, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Try to filter go compiler test files before reading them and building compiler tests**

*Filter Go compiler test files by name or regex before loading to reduce IO and speed up Windows test runs.*

 * created by **weswigham**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **weswigham**
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript#64676](https://github.com/microsoft/TypeScript/pull/64676) (Closed, `For Uncommitted Bug`, **RyanCavanaugh**, **Copilot**)

**Fix CommonJS export assignments for shadowed names in function\-local loops**

*Ensure function-local loops don't generate erroneous CommonJS export assignments for shadowed names.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64676#issuecomment-6046495324) **jakebailey** said "It didn't remove WIP from the title?"
 * (today) **weswigham** closed the issue

### [Issue microsoft/TypeScript#64677](https://github.com/microsoft/TypeScript/issues/64677) (Closed, `Question`)

**Object\.assign does not understand union types**

*Object.assign does not recognize matching union-typed properties, incorrectly flagging literal values as type errors.*

 * created by **prettydiff**
 * [today](https://github.com/microsoft/TypeScript/issues/64677#issuecomment-6047688921) **RyanCavanaugh** explained that Object.assign has no special semantics in TypeScript and suggested adding a type annotation with `as const` as a workaround
 * **RyanCavanaugh** added label `Question`
 * [later](https://github.com/microsoft/TypeScript/issues/64677#issuecomment-6058853215) **prettydiff** said "Thank you very much for the quick response!"
 * (later) **prettydiff** closed the issue

### [PR microsoft/TypeScript#64678](https://github.com/microsoft/TypeScript/pull/64678) (Open, `Author: Team`, `For Uncommitted Bug`, **ahejlsberg**)

**Encapsulate Symbol fields with getters and setters**

*Encapsulate ast.Symbol's exported fields by making them private with getters and setters and updating all usages with regression tests.*

 * created by **ahejlsberg**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript/pull/64678#issuecomment-6046509757) **ahejlsberg** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/64678#issuecomment-6046511336) **typescript-automation[bot]** provided CI job status updates for various test commands
 * [today](https://github.com/microsoft/TypeScript/pull/64678#issuecomment-6046969463) **typescript-automation[bot]** notified that DT test results were ready and unchanged
 * [today](https://github.com/microsoft/TypeScript/pull/64678#issuecomment-6047016977) **typescript-automation[bot]** provided the requested performance run results in a detailed comparison report
 * [today](https://github.com/microsoft/TypeScript/pull/64678#issuecomment-6047345595) **typescript-automation[bot]** provided tsc user test results and indicated everything looked good
 * [today](https://github.com/microsoft/TypeScript/pull/64678#issuecomment-6047727192) **typescript-automation[bot]** reported successful tsc comparison between baseline and pr on the top 400 repos

### [PR microsoft/TypeScript#64679](https://github.com/microsoft/TypeScript/pull/64679) (Open, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Add snapshot\.rebase\(newBaseSnapshot, changes\)**

*Add snapshot.rebase(newBaseSnapshot, changes) to overlay synthetic filesystem changes from an old snapshot onto a new one.*

 * created by **weswigham**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **weswigham**

### [PR microsoft/TypeScript#64680](https://github.com/microsoft/TypeScript/pull/64680) (Open, `Author: Team`, `For Milestone Bug`, **weswigham**)

**Add instantiated symbol mapper into context mapper when reprinting nodes we instantiate before printing**

*Include the instantiated symbol mapper in the node builder context to properly instantiate type parameters when reprinting nodes*

 * created by **weswigham**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Milestone Bug`, and assigned to **weswigham**

### [PR microsoft/TypeScript#64681](https://github.com/microsoft/TypeScript/pull/64681) (Open, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**\[api\] Prepare for beta release**

*Prepare for beta release by renaming and relocating internal APIs, removing unstable prefixes and deprecated functions, and exporting factory.*

 * created by **andrewbranch**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **andrewbranch**

### [PR microsoft/TypeScript#64682](https://github.com/microsoft/TypeScript/pull/64682) (Open, `For Backlog Bug`)

**Report strict\-mode errors for class names eval and arguments**

*Report TS1210 strict-mode errors for class declarations and expressions named 'eval' or 'arguments' during binding.*

 * created by **dmety**
 * (today) **typescript-automation[bot]** added labels `For Backlog Bug`, `For Backlog Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/64682#issuecomment-6055636297) **dmety** said "@microsoft-github-policy-service agree"

### [Issue microsoft/TypeScript#64683](https://github.com/microsoft/TypeScript/issues/64683) (Open)

**Type printer recurses without limit into nested array/tuple types \(stack overflow; can leave later types \`any\`\)**

*TypeScript's type printer now infinitely recurses into nested array and tuple types, causing stack overflows instead of truncation.*

 * created by **ssalbdivad**

### [PR microsoft/TypeScript#64684](https://github.com/microsoft/TypeScript/pull/64684) (Open, `Author: Team`, `For Uncommitted Bug`, **DanielRosenwasser**)

**Use \`link\[T\]\` in place of \`\*Node\` in syntax nodes\.**

*AST node child references now use 32-bit link indices with generated accessor methods instead of 64-bit pointers to reduce memory and CPU overhead under Go’s garbage collector.*

 * created by **DanielRosenwasser**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript/pull/64684#issuecomment-6049696201) **DanielRosenwasser** said "@typescript-bot perf test this"
 * [today](https://github.com/microsoft/TypeScript/pull/64684#issuecomment-6049697074) **typescript-automation[bot]** said "Hey @DanielRosenwasser, this PR is in an unmergable state, so is missing a merge commit to run against; please resolve conflicts and try again."
 * [today](https://github.com/microsoft/TypeScript/pull/64684#issuecomment-6049781741) **DanielRosenwasser** said "@typescript-bot perf test this"
 * [today](https://github.com/microsoft/TypeScript/pull/64684#issuecomment-6049782866) **typescript-automation[bot]** reported that the perf test build job started and provided status and results links
 * [today](https://github.com/microsoft/TypeScript/pull/64684#issuecomment-6050081321) **typescript-automation[bot]** reported performance run results comparing baseline to PR for tsc, showing metrics for errors, symbols, types, memory usage, and memory allocations
 * [later](https://github.com/microsoft/TypeScript/pull/64684#issuecomment-6054635129) **DanielRosenwasser** said "@typescript-bot perf test this"
 * [later](https://github.com/microsoft/TypeScript/pull/64684#issuecomment-6054636949) **typescript-automation[bot]** reported that performance test jobs had started and provided status links
 * [later](https://github.com/microsoft/TypeScript/pull/64684#issuecomment-6055105743) **typescript-automation[bot]** reported the requested perf run results comparing baseline to PR, showing unchanged errors, symbols, and types, and a 4.39% memory usage improvement

### [Issue microsoft/TypeScript#64685](https://github.com/microsoft/TypeScript/issues/64685) (Closed)

**getDocumentationForSymbol docstring is attached to documentationLocationMapper**

*The go doc comment for getDocumentationForSymbol in hover.go is mistakenly attached to the documentationLocationMapper type.*

 * created by **patrickkettner**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64686](https://github.com/microsoft/TypeScript/pull/64686) (Closed, `For Uncommitted Bug`)

**Move the getDocumentationForSymbol docstring onto the function**

*Move the getDocumentationForSymbol docstring from the type declaration onto the function to correct its documentation display.*

 * created by **patrickkettner**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#64687](https://github.com/microsoft/TypeScript/issues/64687) (Open)

**Replacement libs load in an arbitrary order in TypeScript 7: \`sortLibs\` is not stable**

*TypeScript 7's unstable sortLibs causes libReplacement to load libraries in arbitrary order, breaking overload precedence.*

 * created by **rymskip**

### [PR microsoft/TypeScript#64688](https://github.com/microsoft/TypeScript/pull/64688) (Open, `For Milestone Bug`, **gabritto**)

**Read a type's declared members while its base types resolve**

*Modify resolveObjectTypeMembers to preserve a type's declared members during base type resolution to prevent infinite recursion when resolving self-declared properties.*

 * created by **RedesignedRobot**
 * (today) **typescript-automation[bot]** added label `For Milestone Bug`, and assigned to **gabritto**
 * [later](https://github.com/microsoft/TypeScript/pull/64688#issuecomment-6055991306) **RedesignedRobot** said "@microsoft-github-policy-service agree"

### [Issue microsoft/TypeScript#64689](https://github.com/microsoft/TypeScript/issues/64689) (Open)

**TS 7 language server: "Add missing properties" quick fix not offered**

*The TypeScript 7 native language server in VS Code no longer provides the "Add missing properties" quick fix for objects missing required properties as it did in TS 6.0.3.*

 * created by **erengeez**

### [Issue microsoft/TypeScript#64690](https://github.com/microsoft/TypeScript/issues/64690) (Open)

**TS2322: \`const\` type parameter infers \`readonly \[\]\`, rejected through a union return type \(7\.1\.0\-dev regression from typescript\-go\#4591\)**

*A regression in TypeScript 7.1.0-dev causes const type parameters to infer readonly[] instead of string[], resulting in a TS2322 error when returning ok([]) in a union return type.*

 * created by **paoValle**

