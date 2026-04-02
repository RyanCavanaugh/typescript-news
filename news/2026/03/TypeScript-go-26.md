# Report for 2026-03-26 (Thursday, March 26th, 2026)

21 different users commented on 57 different issues.

## Recommended Actions

 * Response Recommended
    * @frankeld confirmed that the issue was resolved in 7.0.0-dev.20260321.1 and identified the likely fix PR #2459 in [microsoft/TypeScript-go#1671](https://github.com/microsoft/TypeScript-go/issues/1671#issuecomment-4143443723)

## Activity Summary

### [Issue microsoft/TypeScript-go#1671](https://github.com/microsoft/TypeScript-go/issues/1671) (Closed, `Domain: Type Checking`, `Domain: Declaration Emit`, **weswigham**)

**tsgo stalls during \-\-noEmit typecheck**

*Running tsgo --noEmit on a project with hundreds of Zod schema files hangs indefinitely while tsc completes type checking quickly.*

 * (21 weeks ago) **ahejlsberg** assigned to **ahejlsberg**, **weswigham**, and unassigned **ahejlsberg**
 * [later](https://github.com/microsoft/TypeScript-go/issues/1671#issuecomment-4143443723) **frankeld** said "Looks like this is resolved with 7.0.0-dev.20260321.1 and tsgo-stall no longer hangs. Likely fix PR: #2459"
 * [later](https://github.com/microsoft/TypeScript-go/issues/1671#issuecomment-4143518414) **jakebailey** said "Yeah, I'm going to consider this done."
 * (later) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#1724](https://github.com/microsoft/TypeScript-go/issues/1724) (Open, `Domain: Editor`, **DanielRosenwasser**, **iisaduan**, **Copilot**)

**"Sort Imports" & "Remove Unused Imports" commands are missing**

*When using tsgo with TypeScript 5.8, the Sort Imports and Remove Unused Imports commands are missing from the VSCode command palette.*

 * created by **PeterStaev**
 * **jakebailey** added label `Domain: Editor`
 * (today) **DanielRosenwasser** set milestone to `TypeScript 7.0 RC`, and assigned to **iisaduan**

### [Issue microsoft/TypeScript-go#1894](https://github.com/microsoft/TypeScript-go/issues/1894) (Open, `Domain: Editor`, **jakebailey**)

**Add semantic highlighting support for editors**

*Add support for semantic highlighting in editors to match the feature availability in VS Code.*

 * created by **mjbvz**
 * **mjbvz** added label `Domain: Editor`
 * (today) **DanielRosenwasser** set milestone to `TypeScript 7.0 RC`, and assigned to **jakebailey**

### [Issue microsoft/TypeScript-go#2244](https://github.com/microsoft/TypeScript-go/issues/2244) (Open, `Domain: Editor`, **gabritto**)

**Port \`update imports on file rename/move\` support**

*Request to port support for automatically updating imports when files are renamed or relocated*

 * [15 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2244#issuecomment-3633217310) **GitMurf** asked if there was a discussion on how tsgo will implement file rename LSP methods and offered to help test from a Neovim perspective
 * [15 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2244#issuecomment-3633225247) **jakebailey** said "I assume we'd do it the same way as VS Code, just over LSP (which LSP is mostly a thin wrapper over)."
 * **RyanCavanaugh** assigned to **gabritto**
 * **DanielRosenwasser** added to milestone `TypeScript 7.0 RC`

### [PR microsoft/TypeScript-go#2407](https://github.com/microsoft/TypeScript-go/pull/2407) (Closed)

**Rewrite matchFiles to not use regexp2, remove other regexp uses**

*Rewrites matchFiles to remove regexp2 and minimize regex usage, achieving significant performance gains.*

 * created by **jakebailey**
 * [10 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2407#issuecomment-3741353531) **jakebailey** said "This needs more work, unfortunately."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2407#issuecomment-4135895201) **jakebailey** tested a Copilot-based reimplementation, noted negligible practical differences from the old regex version, and offered to remove the old implementation due to improved design and performance
 * (today) **jakebailey** closed the issue
 * [later](https://github.com/microsoft/TypeScript-go/pull/2407#issuecomment-4142066600) **camc314** said "This is awesome!"

### [Issue microsoft/TypeScript-go#2632](https://github.com/microsoft/TypeScript-go/issues/2632) (Closed)

**\`@param\` JSDoc requires parameter names, did not in 6\.0 and prior**

*Omitting parameter names in JSDoc @param tags prevents TypeScript from reporting argument type mismatches under noImplicitAny.*

 * [7 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2632#issuecomment-3836132764) **a-tarasyuk** said "@DanielRosenwasser If I remember correctly, earlier versions also required a parameter name. Is this intentional, or is it a new feature to make it optional?"
 * [7 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2632#issuecomment-3836891087) **DanielRosenwasser** said "I probably complained to @sandersn about it then and I'll complain about it in 7.0 too. 😄"
 * [1 month ago](https://github.com/microsoft/TypeScript-go/issues/2632#issuecomment-3959962309) **a-tarasyuk** said "@DanielRosenwasser I’ve opened a PR to address this — could you confirm whether the current behavior is intentional?"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2647](https://github.com/microsoft/TypeScript-go/pull/2647) (Closed)

**fix\(2632\): allow missing names in jsdoc param tags**

*Enable JSDoc @param tags to omit parameter names without causing errors*

 * created by **a-tarasyuk**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2701](https://github.com/microsoft/TypeScript-go/issues/2701) (Closed)

**Declaration emit for named inferred types used in further inference inlines inferred types instead of naming them**

*tsgo inlines inferred types in declaration emit even when named, causing slower type checking in consuming packages.*

 * [1 month ago](https://github.com/microsoft/TypeScript-go/issues/2701#issuecomment-3927069363) **privatenumber** provided additional reproduction steps and real-world impact data showing tsgo produces significantly larger declaration output and errors compared to tsc
 * [1 month ago](https://github.com/microsoft/TypeScript-go/issues/2701#issuecomment-3928362389) **jakebailey** asked to report the missing .d.ts files separately
 * [1 month ago](https://github.com/microsoft/TypeScript-go/issues/2701#issuecomment-3928857325) **privatenumber** said "Sorry about that — the 48 missing files were a measurement error on my end. Both tsc and tsgo produce all 4,710 .d.ts files. I've updated my previous comment with corrected numbers."
 * [today](https://github.com/microsoft/TypeScript-go/issues/2701#issuecomment-4137500062) **jakebailey** said "@chriskrycho Is this now fixed since #2459?"

### [Issue microsoft/TypeScript-go#2857](https://github.com/microsoft/TypeScript-go/issues/2857) (Open, `Domain: Editor`, **andrewbranch**)

**Formatters get stuck**

*The extension’s LSP-based formatter intermittently hangs during format-on-save on MacOS, never returning a response.*

 * **mjbvz** added label `Domain: Editor`
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2857#issuecomment-4016355936) **SibtainOcn** investigated lock contention in snapshotUpdateMu causing dispatch loop stalls and proposed moving GetLanguageService into an async goroutine with PR #2857
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2857#issuecomment-4016378111) **jakebailey** said "That suggestion would just re-break the bugs fixed by #2765..."
 * (today) **DanielRosenwasser** set milestone to `TypeScript 7.0 RC`, and assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2857#issuecomment-4138974027) **DanielRosenwasser** said "I haven't seen this in a while - maybe with assertions on we'll uncover more of these."

### [PR microsoft/TypeScript-go#3176](https://github.com/microsoft/TypeScript-go/pull/3176) (Closed)

**Fix ref count cache inconsistencies**

*Revert cache ref-count simplification so parse cache entries start with refCount 1 and prevent premature deletion.*

 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/3176#issuecomment-4121947181) **jakebailey** said "I've been trying to get get a failing run of TestDuplicatePackageServices_fileChanges for what feels like months now, it's almost certainly nothing related to this PR."
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/3176#issuecomment-4121984148) **andrewbranch** said "Oh, geez, I didn't know that and this PR did touch duplicate file stuff, so I thought it was my fault."
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3176#issuecomment-4130474601) **andrewbranch** said "@gabritto and/or @iisaduan was looking into running the fuzzer against this to hopefully get some extra validation before merging."
 * [today](https://github.com/microsoft/TypeScript-go/pull/3176#issuecomment-4137534610) **gabritto** tested the fuzzer for extra validation before merging
 * [today](https://github.com/microsoft/TypeScript-go/pull/3176#issuecomment-4137873150) **typescript-bot** reported that tsserver comparisons on the top 10 repos between main and refs/pull/3176/merge looked good
 * [today](https://github.com/microsoft/TypeScript-go/pull/3176#issuecomment-4138432881) **typescript-bot** reported that the new server no longer reported a 'Server connection closed prematurely' error in remix-run/react-router and provided detailed results and repro steps
 * [today](https://github.com/microsoft/TypeScript-go/pull/3176#issuecomment-4138432989) **typescript-bot** reported panic stack trace during textDocument/rename cross-project handling
 * [today](https://github.com/microsoft/TypeScript-go/pull/3176#issuecomment-4138433067) **typescript-bot** reported a panic handling a textDocument/formatting request when running the top 100 repos suite
 * [today](https://github.com/microsoft/TypeScript-go/pull/3176#issuecomment-4138433136) **typescript-bot** reported a panic stack trace from textDocument/definition when running the top 100 repos suite

### [Issue microsoft/TypeScript-go#3192](https://github.com/microsoft/TypeScript-go/issues/3192) (Closed, **weswigham**, **jakebailey**, **Copilot**)

**0320 vs 0321**

*The workglow build fails when using tsgo 7.0.0-dev.20260321.1 but succeeds with the previous day's 20260320.1 version.*

 * **jakebailey** assigned to **weswigham**
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/3192#issuecomment-4121065100) **weswigham** explained that extending const type parameters to `as const satisfies` broke isolated-declarations inference because `as const` implies a fully const tree, noted that strada’s typeFromArrayLiteral never wraps tuples in `readonly`, and mentioned a drive-by fix in corsa
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/3192#issuecomment-4121941514) **Andarist** noted an extra note from old design meeting notes and mentioned that although `satisfies` composes better, it’s not ID-friendly
 * [today](https://github.com/microsoft/TypeScript-go/issues/3192#issuecomment-4137565567) **weswigham** stated that #3246 fixed the issue by triggering an ID error to force inferred type printback instead of node reuse, noted that only inner node reuse attempts are affected, and mentioned that Strada also has the bug but it's hidden by the fix in Corsa
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript-go#3195](https://github.com/microsoft/TypeScript-go/pull/3195) (Open)

**API encode/decode fixes**

*Fixed API encoder/decoder by adding missing node properties, assigning a HeritageClause token type, and extending isTypeNode to recognize type keywords.*

 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/3195#issuecomment-4113515688) **virtulis** agreed that encoder changes were unnecessary and only the properties getter was needed, suggested adding a flag for getNamedChild to handle non-optional properties, proposed tests for round-trip consistency, and declined to commit due to CLA restrictions
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/3195#issuecomment-4113555719) **virtulis** suggested generating a full list of properties with the generateFactory script and using defineProperty to dynamically define getters on RemoteNode to avoid manual listings and solve the optional vs empty NodeList issue
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3195#issuecomment-4129065241) **virtulis** said "Added the roundtrip test, made it go through everything and print each error since there's multiple different failures present."
 * [today](https://github.com/microsoft/TypeScript-go/pull/3195#issuecomment-4138050178) **virtulis** described adding output comparisons to roundtrip tests, flooding the console with diffs, fixing a broken TypeOperator, and noting disappearing object spreads

### [PR microsoft/TypeScript-go#3234](https://github.com/microsoft/TypeScript-go/pull/3234) (Closed, **andrewbranch**, **Copilot**)

**Add diagnostic API methods**

*Add API methods for syntactic, semantic, suggestion, config file parsing, and declaration diagnostics with async server calls and range-based tests.*

 * created by **Copilot**
 * (yesterday) **Copilot** assigned to **Copilot**, **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3234#issuecomment-4136224992) **andrewbranch** said "@copilot address review feedback and format"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3234#issuecomment-4136298113) **Copilot** removed omitempty from reportsUnnecessary and reportsDeprecated, ran the formatter, and noted retention of the getGlobalDiagnostics test due to a pre-existing type assertion bug
 * [today](https://github.com/microsoft/TypeScript-go/pull/3234#issuecomment-4136624785) **andrewbranch** said "@copilot just remove getGlobalDiagnostics from the API for now."
 * [today](https://github.com/microsoft/TypeScript-go/pull/3234#issuecomment-4136685418) **Copilot** removed getGlobalDiagnostics from the Go protocol, session handler, and TypeScript Program class along with its tests in both async and sync suites

### [PR microsoft/TypeScript-go#3235](https://github.com/microsoft/TypeScript-go/pull/3235) (Closed)

**Add project info, progress indicators**

*Port project info features from the old TypeScript extension and add progress indicators for project loading and ATA operations.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3236](https://github.com/microsoft/TypeScript-go/pull/3236) (Closed)

**Use an empty NoParams type instead of any for no param messages**

*Use an empty NoParams struct instead of any for no-parameter messages to remove any(nil) from generated LSP types.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3238](https://github.com/microsoft/TypeScript-go/issues/3238) (Closed)

**Consider using \`process\.execve\` in tsgo\.js ?**

*Proposes using experimental process.execve instead of execFileSync in tsgo.js to avoid spawning extra Node processes.*

 * created by **kanashimia**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3238#issuecomment-4135945340) **jakebailey** said "Yes, we'd totally accept a PR for this."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3239](https://github.com/microsoft/TypeScript-go/pull/3239) (Closed)

**Accept baseline differences**

*Integrate the first batch of approved baseline differences into the project’s testing baseline.*

 * created by **ahejlsberg**
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#3240](https://github.com/microsoft/TypeScript-go/issues/3240) (Closed)

**Parser: postfix \`\!\` \(NonNullExpression\) parsed as prefix \`\!\` \(PrefixUnaryExpression\)**

*tsgo parser misparses the postfix non-null assertion operator '!' as a prefix logical-not, producing two statements instead of one.*

 * created by **RealColdFry**
 * (today) **RealColdFry** closed the issue

### [PR microsoft/TypeScript-go#3241](https://github.com/microsoft/TypeScript-go/pull/3241) (Closed)

**Use process\.execve where it is supported**

*Update the tsgo wrapper to use experimental process.execve instead of execFileSync to eliminate extra Node process overhead.*

 * created by **kanashimia**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3241#issuecomment-4136715511) **kanashimia** agreed with microsoft-github-policy-service
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3242](https://github.com/microsoft/TypeScript-go/issues/3242) (Open, `bug`, **RyanCavanaugh**, **Copilot**)

**No error for values named 'Object' \(in CommonJS\)**

*TypeScript incorrectly permits a class named Object to be used with object spread in CommonJS modules without reporting an error.*

 * created by **DanielRosenwasser**

### [Issue microsoft/TypeScript-go#3243](https://github.com/microsoft/TypeScript-go/issues/3243) (Closed, `Domain: Editor`, **andrewbranch**, **Copilot**)

**Auto\-import adds type to value import instead of using existing import type \(Follow\-up to PR \#2978\)**

*Auto-import adds type specifiers to value import statements instead of merging them into existing type-only import blocks.*

 * created by **rubenferreira97**
 * (today) **andrewbranch** added label `Domain: Editor`, and assigned to **Copilot**, **andrewbranch**

### [PR microsoft/TypeScript-go#3244](https://github.com/microsoft/TypeScript-go/pull/3244) (Closed, **andrewbranch**, **Copilot**)

**Fix auto\-import to prefer existing \`import type\` declarations**

*Modify auto-import logic to prefer merging type imports into existing `import type` declarations instead of adding inline type modifiers on value imports.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3244#issuecomment-4137439470) **andrewbranch** said "@copilot+claude-opus-4.6 since this causes existing tests to be removed from the failing list, you can delete your new test."
 * [today](https://github.com/microsoft/TypeScript-go/pull/3244#issuecomment-4137493300) **Copilot** removed the new test file because existing tests already covered it

### [PR microsoft/TypeScript-go#3245](https://github.com/microsoft/TypeScript-go/pull/3245) (Closed)

**Use Go regexp for autoImportSpecifierExcludeRegexes, remove regexp2**

*Replace regexp2 with Go's built-in regexp for autoImportSpecifierExcludeRegexes to simplify dependencies and reduce binary size.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3246](https://github.com/microsoft/TypeScript-go/pull/3246) (Closed)

**Do not reuse input expression nodes to generate type nodes for contextually typed const array literal expressions**

*Avoid reusing input expression nodes when generating type nodes for contextually typed const array literals and adjust the pseudochecker’s isContextuallyTyped logic.*

 * created by **weswigham**
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript-go#3247](https://github.com/microsoft/TypeScript-go/pull/3247) (Closed)

**Dummy change to test CI please ignore**

*A dummy code change was submitted to test the continuous integration pipeline.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3248](https://github.com/microsoft/TypeScript-go/pull/3248) (Closed)

**fix\(3242\): check class name collisions with Object**

*Add validation to detect and prevent user-defined class names from colliding with the built-in Object type.*

 * created by **a-tarasyuk**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3248#issuecomment-4138521730) **jakebailey** suggested expanding checks further referencing issue #2087 and noted checks were only in non-ESM files
 * [today](https://github.com/microsoft/TypeScript-go/pull/3248#issuecomment-4138529774) **jakebailey** said "To be clear, that other PR could be overcomplicated, so I'm not saying to close this, rather that there's a wider range of missing code we seem to need."
 * (today) **a-tarasyuk** closed the issue

### [Issue microsoft/TypeScript-go#3249](https://github.com/microsoft/TypeScript-go/issues/3249) (Open, `possible improvement`)

**Report perf measurements from extension**

*Collect and report performance metrics for language service operations in the extension to track regressions and improvements.*

 * created by **DanielRosenwasser**
 * **DanielRosenwasser** added to milestone `TypeScript 7.0 RC`

### [Issue microsoft/TypeScript-go#3250](https://github.com/microsoft/TypeScript-go/issues/3250) (Open, `feature parity`)

**Reimplement "find file references"**

*Reimplement find file references for JS/TS files by extending multi-project search beyond document positions.*

 * created by **DanielRosenwasser**

### [Issue microsoft/TypeScript-go#3251](https://github.com/microsoft/TypeScript-go/issues/3251) (Open, `Crash`, **DanielRosenwasser**, **Copilot**)

**Signature help assertion failure**

*An assertion failure in the Go language server's signature help getContainingArgumentInfo crashes without known repro steps, possibly tied to reparsing.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** added label `Crash`, and assigned to **Copilot**, **DanielRosenwasser**

### [PR microsoft/TypeScript-go#3252](https://github.com/microsoft/TypeScript-go/pull/3252) (Open, **DanielRosenwasser**, **Copilot**)

**Fix signature help assertion failure by marking all DeepCloneReparse descendants as reparsed**

*Mark all DeepCloneReparse descendants as reparsed to prevent signature help assertion failures from JSDoc-derived node positions.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **DanielRosenwasser**

### [Issue microsoft/TypeScript-go#3253](https://github.com/microsoft/TypeScript-go/issues/3253) (Closed, `bug`)

**Inconsistent output from \-\-listFilesOnly**

*tsgo’s --listFilesOnly option returns non-deterministic file listings across runs when importing from complex node_modules packages*

 * created by **matthewvalentine**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3253#issuecomment-4139334905) **jakebailey** said "For tsgo, can you try passing --deduplicatePackages false and see if that stabilizes it?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/3253#issuecomment-4139355908) **jakebailey** said "Tested it myself, and that does indeed fix it. Thanks, I've been looking for this kind of repro for a flaky test I've been trying to figure out."

### [PR microsoft/TypeScript-go#3254](https://github.com/microsoft/TypeScript-go/pull/3254) (Closed)

**Sort peer deps in readPackageJsonPeerDependencies**

*Add alphabetical sorting of peer dependencies in readPackageJsonPeerDependencies to ensure consistent ordering.*

 * created by **jakebailey**

### [Issue microsoft/TypeScript-go#3255](https://github.com/microsoft/TypeScript-go/issues/3255) (Closed)

**Cannot find name 'global' when extending global\.Set**

*Extending global.Set in tsgo fails because it cannot resolve the global identifier.*

 * created by **MulverineX**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3255#issuecomment-4140001570) **jakebailey** suggested using `globalThis` instead of Node's `global` and noted that extending `global.Set` errors without a repro
 * [today](https://github.com/microsoft/TypeScript-go/issues/3255#issuecomment-4140048421) **MulverineX** suggested that the TypeScript behavior might be more accurate than the JS implementation, provided a link to the tsconfig, and noted testing in TypeScript 5
 * [today](https://github.com/microsoft/TypeScript-go/issues/3255#issuecomment-4140355922) **jakebailey** pointed out that TypeScript 6 defaults types to [] and provided a link to the announcement
 * [today](https://github.com/microsoft/TypeScript-go/issues/3255#issuecomment-4140423858) **MulverineX** said "Oh okay neat! Alright, this is WAI then."
 * (today) **MulverineX** closed the issue

### [Issue microsoft/TypeScript-go#3256](https://github.com/microsoft/TypeScript-go/issues/3256) (Closed)

**\[ServerErrors\]\[TypeScript\] main vs **

*The main branch pipeline analyzing 300 popular TypeScript GitHub repositories successfully processed 211 repos—detecting 21 interesting changes, with six clone failures, 71 timeouts, and 12 unknown failures.*

 * created by **typescript-bot**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3256#issuecomment-4140021456) **typescript-bot** reported a panic in textDocument/documentHighlight due to a debug failure 'Should only get Alias here', including a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/3256#issuecomment-4140021496) **typescript-bot** reported a panic during cross-project rename handling due to an invalid memory address or nil pointer dereference
 * [today](https://github.com/microsoft/TypeScript-go/issues/3256#issuecomment-4140021537) **typescript-bot** reported a panic handling a textDocument/formatting request due to a debug failure
 * [today](https://github.com/microsoft/TypeScript-go/issues/3256#issuecomment-4140021583) **typescript-bot** reported a panic in request textDocument/completion due to index out of range
 * [today](https://github.com/microsoft/TypeScript-go/issues/3256#issuecomment-4140021623) **typescript-bot** reported a panic handling textDocument/formatting request due to a debug failure: False expression: Token end is child end
 * [today](https://github.com/microsoft/TypeScript-go/issues/3256#issuecomment-4140021679) **typescript-bot** reported a server connection closed prematurely error with undefined and included artifacts, last requests, and reproduction steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/3256#issuecomment-4140021731) **typescript-bot** reported a server connection closed prematurely error for HumanSignal/label-studio, included artifact links, last requests, and reproduction steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/3256#issuecomment-4140021787) **typescript-bot** reported that the server connection closed prematurely with undefined error during operations on colinhacks/zod
 * [today](https://github.com/microsoft/TypeScript-go/issues/3256#issuecomment-4140021831) **typescript-bot** reported server connection closed prematurely with undefined and provided logs, affected repo, last requests, and repro steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/3256#issuecomment-4140021871) **typescript-bot** reported a panic during textDocument/rename handling due to invalid memory address or nil pointer dereference
 * [today](https://github.com/microsoft/TypeScript-go/issues/3256#issuecomment-4140021916) **typescript-bot** reported a panic during textDocument/rename due to a nil pointer dereference
 * [today](https://github.com/microsoft/TypeScript-go/issues/3256#issuecomment-4140021958) **typescript-bot** reported a panic in textDocument/rename due to invalid memory address or nil pointer dereference
 * [today](https://github.com/microsoft/TypeScript-go/issues/3256#issuecomment-4140021995) **typescript-bot** reported a panic during textDocument/rename handling due to an invalid memory address or nil pointer dereference
 * [today](https://github.com/microsoft/TypeScript-go/issues/3256#issuecomment-4140022037) **typescript-bot** reported a panic during textDocument/rename due to an invalid memory address or nil pointer dereference
 * (later) **gabritto** closed the issue

### [PR microsoft/TypeScript-go#3257](https://github.com/microsoft/TypeScript-go/pull/3257) (Open)

**Add perf / project telemetry**

*Add togglable events for project metadata and periodic performance telemetry, including file counts, compiler options, memory usage, and GC metrics.*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#3258](https://github.com/microsoft/TypeScript-go/pull/3258) (Closed)

**Fix file dedupe fourslash flake**

*Incomplete cycle detection in UpdateProgram and reusing modified package.json files provoke intermittent fourslash dedupe flakes.*

 * created by **jakebailey**

### [Issue microsoft/TypeScript-go#3259](https://github.com/microsoft/TypeScript-go/issues/3259) (Open, `possible improvement`)

**Proposal: Flatten the AST to speed up tsgo**

*Proposes flattening tsgo’s AST into a flat array to reduce garbage collection scanning overhead and improve performance.*

 * created by **no-yan**
 * [later](https://github.com/microsoft/TypeScript-go/issues/3259#issuecomment-4143065149) **jakebailey** noted that implementing data-oriented design would be painful and that Go’s new "green tea" garbage collector and existing arena allocation likely already provide most benefits, added that Go’s concurrent GC might run on idle cores and suggested that excessive allocations elsewhere could be the real issue
 * [later](https://github.com/microsoft/TypeScript-go/issues/3259#issuecomment-4143117997) **jakebailey** acknowledged GOGC was disabled and wondered if adjusting it during compilation could improve performance

### [PR microsoft/TypeScript-go#3260](https://github.com/microsoft/TypeScript-go/pull/3260) (Closed)

**Suppress process\.execve warning on windows**

*Suppress the experimental process.execve warning on Windows by gating its code path based on the operating system.*

 * created by **kanashimia**
 * [later](https://github.com/microsoft/TypeScript-go/pull/3260#issuecomment-4143082257) **jakebailey** said "We can do this, but this implies that the only reason we don't print a warning on other platforms is due to a race condition, which isn't thrilling."
 * (later) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3261](https://github.com/microsoft/TypeScript-go/pull/3261) (Closed)

**Fix enum diagnostic \(deleted\)**

*Resolve minor discrepancies in enum diagnostic output to align with baseline expectations.*

 * created by **ahejlsberg**
 * (later) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#3262](https://github.com/microsoft/TypeScript-go/pull/3262) (Closed)

**Fix enum diagnostic**

*Adjust enum diagnostic output to match the established baseline expectations.*

 * created by **ahejlsberg**
 * (later) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#3263](https://github.com/microsoft/TypeScript-go/pull/3263) (Open)

**Preserve original comments on params in dts generated by pseudo type node builder under \`removeComments: false\`**

*Declaration files generated by the pseudo type node builder with removeComments disabled fail to preserve original parameter comments.*

 * created by **Andarist**

### [PR microsoft/TypeScript-go#3264](https://github.com/microsoft/TypeScript-go/pull/3264) (Open)

**support quick info and go to definition on mapped keys**

*Add quick info and go-to-definition support for mapped type keys in TypeScript.*

 * created by **Zzzen**

### [PR microsoft/TypeScript-go#3265](https://github.com/microsoft/TypeScript-go/pull/3265) (Closed)

**Fix dts emit for type params for object methods in const context**

*Correct generation of d.ts definitions for type parameters of object methods declared in const contexts.*

 * created by **Andarist**

### [PR microsoft/TypeScript-go#3266](https://github.com/microsoft/TypeScript-go/pull/3266) (Open, `dependencies`, `javascript`)

**Bump brace\-expansion from 5\.0\.4 to 5\.0\.5**

*Bump the brace-expansion dependency from version 5.0.4 to 5.0.5 to incorporate upstream patches and fixes.*

 * created by **dependabot[bot]**
 * (later) **dependabot[bot]** added labels `dependencies`, `javascript`

### [Issue microsoft/TypeScript-go#3267](https://github.com/microsoft/TypeScript-go/issues/3267) (Closed, `Crash`)

**panic when \`declarationMap\` is enabled**

*A recent change causes enabling declarationMap to panic with a slice bounds out-of-range error during source map emission.*

 * created by **liuxingbaoyu**
 * **liuxingbaoyu** added label `Crash`

