# Report for 2026-08-17 (Monday, August 17th, 2026)

12 different users commented on 71 different issues.

## Recommended Actions

 * Response Recommended
    * @typescript-automation[bot] provided performance results as requested in [microsoft/TypeScript-go#4839](https://github.com/microsoft/TypeScript-go/pull/4839#issuecomment-5319198280)
    * @lukesandberg provided a link to a proposed solution branch in [microsoft/TypeScript-go#4911](https://github.com/microsoft/TypeScript-go/pull/4911#issuecomment-5321232461)
    * @lukesandberg asked for help with PR permissions in [microsoft/TypeScript-go#4911](https://github.com/microsoft/TypeScript-go/pull/4911#issuecomment-5321296935)
    * @typescript-automation[bot] provided perf run results as requested in [microsoft/TypeScript-go#4913](https://github.com/microsoft/TypeScript-go/pull/4913#issuecomment-5330768512)

## Activity Summary

### [Issue microsoft/TypeScript-go#2850](https://github.com/microsoft/TypeScript-go/issues/2850) (Closed, **andrewbranch**)

**Add \`\.getNonPrimitiveType\(\)\` getter**

*The API is missing the recently introduced .getNonPrimitiveType() getter that exists in Strada.*

 * created by **mrazauskas**
 * **jakebailey** assigned to **andrewbranch**
 * **RyanCavanaugh** added to milestone `Post-7.0`
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#3297](https://github.com/microsoft/TypeScript-go/pull/3297) (Closed, `No linked issue`, `Unmigrated PR`, **weswigham**)

**Allow global Symbol computed names during pseudochecker object literal serialization**

*Support global Symbol computed property names in pseudochecker object literal serialization to match Strada’s behavior.*

 * (10 weeks ago) **RyanCavanaugh** set milestone to `Post-7.0`, removed from milestone `TypeScript 7.0 RC`, and assigned to **weswigham**
 * **jakebailey** added label `Unmigrated PR`

### [PR microsoft/TypeScript-go#3331](https://github.com/microsoft/TypeScript-go/pull/3331) (Closed, `Unmigrated PR`)

**Use trie for removeStringLiteralsMatchedByTemplateLiterals**

*Adopt a trie-based implementation for removeStringLiteralsMatchedByTemplateLiterals to resolve TypeScript issue 63342.*

 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/3331#issuecomment-5297607770) **jakebailey** said "@typescript-bot perf test this faster"
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/3331#issuecomment-5297608752) **typescript-automation[bot]** started build jobs and posted status and results links
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/3331#issuecomment-5297880991) **typescript-automation[bot]** posted perf run results for the requested tsc performance comparison
 * **RyanCavanaugh** added label `Unmigrated PR`

### [Issue microsoft/TypeScript-go#3374](https://github.com/microsoft/TypeScript-go/issues/3374) (Closed, `Crash`, **DanielRosenwasser**, **Copilot**)

**Code action crash from \`setLastNonTriviaPosition\`**

*A code action crashes the TypeScript printer in setLastNonTriviaPosition while emitting JSX text.*

 * (18 weeks ago) **DanielRosenwasser** assigned to **Copilot**, and unassigned **Copilot**
 * **RyanCavanaugh** added to milestone `Possible Improvement`
 * [today](https://github.com/microsoft/TypeScript-go/issues/3374#issuecomment-5318397092) **DanielRosenwasser** said "#3712 fixed this - however, #3375 has a test case. We'll just close this issue out by adding a test case."
 * (today) **DanielRosenwasser** assigned to **Copilot**, and unassigned **Copilot**
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#3375](https://github.com/microsoft/TypeScript-go/pull/3375) (Closed, **DanielRosenwasser**, **Copilot**)

**Fix index out of bounds panic in setLastNonTriviaPosition for empty strings**

*Add a bounds check to the trailing whitespace loop in setLastNonTriviaPosition to prevent panics on empty strings*

 * (18 weeks ago) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * **RyanCavanaugh** added to milestone `Possible Improvement`
 * [today](https://github.com/microsoft/TypeScript-go/pull/3375#issuecomment-5318157857) **RyanCavanaugh** said "Conflicted, let's pick it up after the move"
 * (today) **RyanCavanaugh** closed the issue
 * (today) **DanielRosenwasser** reopened the issue
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#3515](https://github.com/microsoft/TypeScript-go/pull/3515) (Closed, `No linked issue`, **navya9singh**)

**Expose formatNodeForInsertion in internal API**

*Add the formatNodeForInsertion function to the library’s internal API to enable its use by external modules.*

 * (10 weeks ago) **RyanCavanaugh** set milestone to `Possible Improvement`, and removed from milestone `TypeScript 7.0 RC`
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/3515#issuecomment-5298704595) **RyanCavanaugh** said "Do we still need this?"
 * (today) **andrewbranch** closed the issue
 * (today) **andrewbranch** reopened the issue
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#3619](https://github.com/microsoft/TypeScript-go/pull/3619) (Closed, `No linked issue`, `Unmigrated PR`)

**perf: Make \`NodeArray\` no longer inherit from \`Array\`**

*Detach NodeArray from Array prototype to prevent direct array method usage and achieve significant performance gains.*

 * **RyanCavanaugh** added to milestone `Possible Improvement`
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/3619#issuecomment-5296902234) **jakebailey** said "Is this still needed? Did we end up doing this another way?"
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/3619#issuecomment-5297822444) **andrewbranch** described making improvements to preserve array element access while noting the proposal still performs better but sacrifices direct indexing
 * **RyanCavanaugh** added label `Unmigrated PR`

### [Issue microsoft/TypeScript-go#3659](https://github.com/microsoft/TypeScript-go/issues/3659) (Closed, `bug`)

**Behavior difference: JSDoc comments are stripped for mapped types**

*Mapped types in TypeScript 7 beta strip JSDoc comments from original properties, unlike TypeScript 6.0.3.*

 * (14 weeks ago) **RyanCavanaugh** added label `bug`, and set milestone to `Post-7.0`
 * [1 month ago](https://github.com/microsoft/TypeScript-go/issues/3659#issuecomment-5013217308) **christopher-buss** reported losing JSDoc in mapped types and identified TypeScript versions where docs are dropped
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3663](https://github.com/microsoft/TypeScript-go/pull/3663) (Closed)

**Fix hover JSDoc for mapped type properties**

*Fix JSDoc hover tooltips for mapped type properties to display accurate documentation.*

 * **RyanCavanaugh** added to milestone `Post-7.0`
 * (3 weeks ago) **DanielRosenwasser** set milestone to `TypeScript 7.1`, and removed from milestone `Post-7.0`
 * [today](https://github.com/microsoft/TypeScript-go/pull/3663#issuecomment-5320534638) **jakebailey** said "Turns out, I merged #4685, which had some overlap here; I'm going to quick fix this."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3690](https://github.com/microsoft/TypeScript-go/pull/3690) (Closed, `Unmigrated PR`)

**fix: handle symlink workspace roots in project reference redirects**

*Ensure project reference redirects correctly resolve symlinked workspace roots in TypeScript*

 * created by **Zzzen**
 * **RyanCavanaugh** added to milestone `Post-7.0`
 * [today](https://github.com/microsoft/TypeScript-go/pull/3690#issuecomment-5321189158) **jakebailey** said "I tested this and yeah, https://github.com/microsoft/TypeScript/issues/63819#issuecomment-4408371311 is correct, this adds a lot of realpath checks that I think we need to be caching"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3690#issuecomment-5321197739) **jakebailey** described asking Copilot locally to implement the parent directory realpath cache, noted it worked well, and suggested reopening on the main TS repo if this repo closes first
 * **jakebailey** added label `Unmigrated PR`

### [PR microsoft/TypeScript-go#3720](https://github.com/microsoft/TypeScript-go/pull/3720) (Closed)

**Prompt after 5 consecutive server restarts in a session**

*Add a prompt after five consecutive server restarts to gather non-developer users’ reasons, with a possible phased rollout.*

 * created by **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3720#issuecomment-5318191384) **DanielRosenwasser** said "This hasn't been an issue really."
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#3728](https://github.com/microsoft/TypeScript-go/pull/3728) (Closed, `No linked issue`, `Unmigrated PR`)

**Fix keyof deferred for non\-generic substitution types \(\#2186\)**

*Resolve keyof immediately for non-generic substitution types instead of deferring, fixing indexed access assignability and quick info.*

 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/3728#issuecomment-5298456989) **typescript-automation[bot]** reported build start and completion statuses for test top400 and perf test this faster
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/3728#issuecomment-5298657492) **typescript-automation[bot]** reported performance run results for the requested baseline..pr comparison, including errors, symbols, types, memory usage, and memory allocations
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/3728#issuecomment-5298948718) **typescript-automation[bot]** reported that everything looked good after comparing main and the pull request across the top 400 repositories with tsc
 * **RyanCavanaugh** added label `Unmigrated PR`

### [PR microsoft/TypeScript-go#3935](https://github.com/microsoft/TypeScript-go/pull/3935) (Closed, `No linked issue`, `Unmigrated PR`)

**Narrow keyword completions for concise arrow expression bodies**

*Port keyword completion filtering to Go so concise arrow function bodies only suggest expression keywords.*

 * (10 weeks ago) **RyanCavanaugh** added label `No linked issue`, and set milestone to `Post-7.0`
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/3935#issuecomment-5298337051) **jakebailey** said "I think this PR would have been fine, had it added a test for what it was trying to do."
 * **RyanCavanaugh** added label `Unmigrated PR`

### [PR microsoft/TypeScript-go#3943](https://github.com/microsoft/TypeScript-go/pull/3943) (Closed, `No linked issue`, `Unmigrated PR`)

**Fix crash inferring constrained variadic tuples with optional elements**

*Fix compiler crash during inference of constrained variadic tuples with optional elements*

 * (10 weeks ago) **RyanCavanaugh** added label `No linked issue`, set milestone to `Post-7.0`, and removed from milestone `TypeScript 7.0 RC`
 * **RyanCavanaugh** added label `Unmigrated PR`

### [PR microsoft/TypeScript-go#4197](https://github.com/microsoft/TypeScript-go/pull/4197) (Closed, `No linked issue`, `Unmigrated PR`)

**prevent bundled library paths from being watched in resolution lookup**

*Skip watching embedded bundled library paths in resolution lookup glob patterns while still including real library directories.*

 * **RyanCavanaugh** added to milestone `Post-7.0`
 * [9 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4197#issuecomment-4696402624) **RyanCallahan312** tracked down the issue to a project using Effect-TS/tsgo and decided to disable neovim's workspace.didChangeWatchedFiles.dynamicRegistration as the solution
 * [9 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4197#issuecomment-4696430103) **jakebailey** said "They're patching us and then shipping the code? If so, they really need to ship us properly."
 * **RyanCavanaugh** added label `Unmigrated PR`

### [PR microsoft/TypeScript-go#4248](https://github.com/microsoft/TypeScript-go/pull/4248) (Closed, **DanielRosenwasser**, **Copilot**)

**Fix fatal panic on non\-absolute path in VFS**

*Update VFS RootLength, SplitPath, and RootAndPath to return defaults for non-absolute paths instead of panicking.*

 * [9 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4248#issuecomment-4661516807) **Copilot** added a focused regression test covering ResolveModuleName('./foo', '', ...) to exercise the non-absolute VFS lookup path that previously panicked; noted in commit f7f88aae
 * [9 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4248#issuecomment-4662353054) **DanielRosenwasser** said "@copilot can you investigate adding a real world example as a compiler or fourslash test that fails without any fix?"
 * [9 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4248#issuecomment-4662531216) **Copilot** investigated compiler and fourslash test normalization and determined that no real-world test could reproduce the panic without giving false confidence
 * (today) **jakebailey** closed the issue
 * (today) **jakebailey** reopened the issue

### [PR microsoft/TypeScript-go#4274](https://github.com/microsoft/TypeScript-go/pull/4274) (Closed, **ahejlsberg**)

**Fix CFA stack overflow crash in for loops where initializer throws**

*Add an early bailout in for-loop binding to avoid stack overflow when the initializer throws*

 * **RyanCavanaugh** added to milestone `Post-7.0`
 * (5 weeks ago) **ibesuperv** closed the issue
 * (1 month ago) **ibesuperv** reopened the issue
 * [later](https://github.com/microsoft/TypeScript-go/pull/4274#issuecomment-5325899344) **ibesuperv** said " I noticed the original issue (#63092) was closed via #4599 — is this PR still needed, or should I close it? Happy either way."
 * [later](https://github.com/microsoft/TypeScript-go/pull/4274#issuecomment-5327326037) **jakebailey** said "No, we shouldn't need this one anymore, but thanks for sending it."
 * (later) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4297](https://github.com/microsoft/TypeScript-go/pull/4297) (Closed, `Unmigrated PR`)

**Push per\-file diagnostics for clients without pull diagnostics support**

*Implement per-file push diagnostics for clients with publishDiagnostics but no pull support, sending open/change/close updates without affecting pull-capable clients.*

 * created by **christianvuerings**
 * [8 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4297#issuecomment-4744853071) **christianvuerings** asked @jakebailey to take a look at the PR and noted that Claude code didn't support pull diagnostics and TypeScript Go didn't support push diagnostics
 * [8 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4297#issuecomment-4745627690) **jakebailey** said "We haven't had time to test it; we'd have to disable pull diags and test in VS Code and make sure it works. Push diagnostics get tricky when dealing with LS restarts and other racy ish conditions."
 * **jakebailey** added label `Unmigrated PR`

### [PR microsoft/TypeScript-go#4336](https://github.com/microsoft/TypeScript-go/pull/4336) (Closed, **jakebailey**, **Copilot**)

**Fix JS declaration emit for dangling top\-level block comments**

*Use NotEmittedStatement nodes to preserve dangling top-level block comments in TypeScript declaration output, including CommonJS modules.*

 * (8 weeks ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * **RyanCavanaugh** added to milestone `Post-7.0`
 * [today](https://github.com/microsoft/TypeScript-go/pull/4336#issuecomment-5318280872) **jakebailey** prompted Copilot to think better and threatened to discard the PR if it didn’t work

### [PR microsoft/TypeScript-go#4343](https://github.com/microsoft/TypeScript-go/pull/4343) (Closed, **DanielRosenwasser**, **Copilot**)

**Ignore stray close events for unopened files**

*Ignore close events for files without open overlays by treating them as no-ops to prevent snapshot panics.*

 * (8 weeks ago) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * [8 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4343#issuecomment-4725100250) **DanielRosenwasser** expressed confusion about receiving a didClose for an already-closed file and speculated editor behavior
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#4422](https://github.com/microsoft/TypeScript-go/pull/4422) (Closed, `Unmigrated PR`)

**Use auto\-imports for \`isolatedDeclarations\` fixes**

*Add auto-import suggestions for fixes applied to code under the isolatedDeclarations setting.*

 * created by **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4422#issuecomment-5320580628) **DanielRosenwasser** suggested auto-import logic bounded by the current program and fallback behavior when imports aren't available
 * [today](https://github.com/microsoft/TypeScript-go/pull/4422#issuecomment-5321315528) **DanielRosenwasser** said "@copilot tests are failing"

### [PR microsoft/TypeScript-go#4440](https://github.com/microsoft/TypeScript-go/pull/4440) (Closed, `Unmigrated PR`, **andrewbranch**)

**API: add getChildren and token getters to Node**

*Extend the Node API with getChildren, getChildCount, getChildAt, getFirstToken, and getLastToken methods.*

 * created by **oMatheusmol**
 * **jakebailey** assigned to **andrewbranch**
 * **andrewbranch** added label `Unmigrated PR`

### [PR microsoft/TypeScript-go#4449](https://github.com/microsoft/TypeScript-go/pull/4449) (Closed)

**restore JSDoc member name check for private identifier references**

*Restores the JSDoc member name validation for private identifiers in isValidReferencePosition by implementing the missing helper.*

 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4449#issuecomment-4906335658) **jakebailey** said "What is this for? You're making the baselines worse?"
 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4449#issuecomment-4917489457) **aamoghS** fixed the parser to retain private identifier nodes in JSDoc @see tags, tightened up isJSDocMemberName to avoid normal this.#x matches, updated the checker to resolve private identifiers, and refreshed the baselines
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/4449#issuecomment-5297852487) **aamoghS** rebased onto latest main and explained that the fourslash baseline for TestFindAllReferencesJSDocPrivateIdentifier showed bidirectional references between the #field declaration and @see C.#field, and clarified that isJSDocMemberName remains limited to JSDoc QualifiedName contexts so ordinary this.#x is unchanged
 * [today](https://github.com/microsoft/TypeScript-go/pull/4449#issuecomment-5321028475) **jakebailey** criticized the change as incorrect and questioned the underlying bug and AST correctness
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4450](https://github.com/microsoft/TypeScript-go/pull/4450) (Closed, `Unmigrated PR`)

**implement getContextNode for ForOf, ForIn, and Switch statements**

*Implement getContextNode support for ForOf, ForIn, and Switch statements to prevent nil returns that break cross-project find references and go-to-definition functionality*

 * created by **aamoghS**
 * (today) **jakebailey** added labels `Unmigrated PR`, `Unmigrated PR`, and removed label `Unmigrated PR`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4496](https://github.com/microsoft/TypeScript-go/pull/4496) (Closed, `Unmigrated PR`)

**fix\(lsp\): support TypeScript source action kinds**

*Advertise and support TypeScript-specific source action kinds suffixed with .ts in the LSP server while maintaining generic kinds for backward compatibility.*

 * created by **TorinAsakura**
 * [6 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4496#issuecomment-4848080613) **jakebailey** suggested looking at the vscode repo's typescript-language-features extension and questioned whether implementing the feature was critical since old extensions could not do it
 * [6 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4496#issuecomment-4848251335) **TorinAsakura** rechecked vscode and explained that the PR targets multi-server LSP scenarios rather than matching the current extension and wires actual handling to support generic source.removeUnusedImports as an escape hatch for clients
 * [today](https://github.com/microsoft/TypeScript-go/pull/4496#issuecomment-5321335781) **jakebailey** observed that only the TypeScript language server and similar JS tools add these suffixes, while pyright/pylance, gopls, and rust-analyzer do not

### [Issue microsoft/TypeScript-go#4502](https://github.com/microsoft/TypeScript-go/issues/4502) (Closed, `Domain: API and Extensibility`, **andrewbranch**)

**\`Program\` is missing \`\.getSourceFiles\(\)\` getter**

*Add a getSourceFiles() getter to Program to return all SourceFile instances and ease filtering.*

 * (6 weeks ago) **andrewbranch** added label `Domain: API and Extensibility`, set milestone to `Post-7.0`, and assigned to **andrewbranch**
 * [later](https://github.com/microsoft/TypeScript-go/issues/4502#issuecomment-5330761493) **mrazauskas** thanked Andrew Branch, noted that retrieving every SourceFile was a mistake, suggested that getSourceFileMetadata include isDeclarationFile instead, and said they would open a new issue to request it
 * (later) **mrazauskas** closed the issue

### [PR microsoft/TypeScript-go#4530](https://github.com/microsoft/TypeScript-go/pull/4530) (Closed)

**Fix: Correctly flag always\-truthy exported and imported enum conditions \(ts2845\)**

*Fix ts2845 by ensuring always-truthy enum conditions are flagged for exported and imported enums*

 * created by **thinkapoorv**
 * [6 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4530#issuecomment-4874825598) **thinkapoorv** requested CLA agreement and provided the Contributor License Agreement text
 * [today](https://github.com/microsoft/TypeScript-go/pull/4530#issuecomment-5320182332) **jakebailey** said "This PR needs a lot of work, and is unlikely to be fixed before we move repos anyway; I'm just going to close it"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4533](https://github.com/microsoft/TypeScript-go/pull/4533) (Closed, **andrewbranch**)

**\[api\] Add \`\.getNonPrimitiveType\(\)\` getter**

*Introduce a .getNonPrimitiveType() getter in the API to access non-primitive types.*

 * created by **mrazauskas**
 * **jakebailey** assigned to **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#4539](https://github.com/microsoft/TypeScript-go/issues/4539) (Closed, `Domain: API and Extensibility`, **andrewbranch**)

**Add \`StructuredType\` type to the API**

*Add StructuredType type to the API for use with TypeFlags.StructuredType checks and casting.*

 * (6 weeks ago) **andrewbranch** added label `Domain: API and Extensibility`, set milestone to `Post-7.0`, and assigned to **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#4540](https://github.com/microsoft/TypeScript-go/pull/4540) (Closed, **andrewbranch**)

**\[api\] Add \`StructuredType\` type**

*Add the missing StructuredType type to the API.*

 * created by **mrazauskas**
 * **jakebailey** assigned to **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#4552](https://github.com/microsoft/TypeScript-go/pull/4552) (Closed, **andrewbranch**)

**Add versions of get\*Diagostics that allow passing in an array of files\.**

*Enable passing multiple files to get*Diagnostics to batch diagnostic requests and reduce performance overhead.*

 * created by **dragomirtitian**
 * **jakebailey** assigned to **andrewbranch**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4555](https://github.com/microsoft/TypeScript-go/pull/4555) (Closed, `Unmigrated PR`, **andrewbranch**)

**Add batched version for several API functions\.**

*Add batched versions of several API functions to reduce IPC overhead and improve performance.*

 * created by **dragomirtitian**
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4555#issuecomment-5129174620) **dragomirtitian** agreed that a generic batching API would be useful, noted that their sync API use precludes next-tick batching, and described their existing batching library
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4555#issuecomment-5134149432) **weswigham** explained that using a single checker/LS instance for the whole batch caches diagnostics and negates benefits of a bespoke entrypoint
 * **jakebailey** assigned to **andrewbranch**
 * **andrewbranch** added label `Unmigrated PR`

### [PR microsoft/TypeScript-go#4564](https://github.com/microsoft/TypeScript-go/pull/4564) (Closed, **andrewbranch**)

**Add native\-preview API: getSourceFiles and StructuredType**

*Extend native-preview API with Program.getSourceFiles and introduce StructuredType with an isStructuredType predicate.*

 * created by **aamoghS**
 * **jakebailey** assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4564#issuecomment-5320782189) **andrewbranch** explained that StructuredType was added in #4540, getSourceFiles was intentionally omitted due to expense, getSourceFileNames was added, and invited opening a new PR in the TypeScript repo after the move
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#4592](https://github.com/microsoft/TypeScript-go/pull/4592) (Closed)

**Improve responsiveness of \`tsc build\` to interruption**

*Improve tsc build responsiveness to SIGINT/SIGTERM by threading cancellation contexts for immediate exit and proper exit codes.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4592#issuecomment-5064330139) **lukesandberg** noted that skipping signal handlers causes crashes with partial outputs and suggested propagating context.Context for LSP timeouts for consistency
 * [5 days ago](https://github.com/microsoft/TypeScript-go/pull/4592#issuecomment-5269980557) **lukesandberg** asked whether to abandon the approach, described how removing signal handlers breaks ctrl-c handling in tsc --watch by causing goroutine panics, and proposed possible solutions
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/4592#issuecomment-5296197926) **jakebailey** suggested limiting or omitting signal handling and aiming to fix it in a patch release
 * [today](https://github.com/microsoft/TypeScript-go/pull/4592#issuecomment-5320986201) **jakebailey** proposed dropping the signals, mentioned preparing a PR, and stated he would close the issue to move things along
 * (today) **jakebailey** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/4592#issuecomment-5321063769) **jakebailey** said "Made microsoft/typescript-go#4911."

### [PR microsoft/TypeScript-go#4598](https://github.com/microsoft/TypeScript-go/pull/4598) (Closed)

**Fix optionality stripping when mapping over tuples under EOPT**

*Ensure mapping over tuples under EOPT preserves optionality instead of incorrectly stripping it*

 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/4598#issuecomment-5298988302) **typescript-automation[bot]** provided automated update on build statuses for `test top400` and `perf test this faster`
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/4598#issuecomment-5299152020) **typescript-automation[bot]** provided the requested performance run results
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/4598#issuecomment-5299389527) **typescript-automation[bot]** reported that the tsc run on the top 400 repos comparing main and the pull request merge looked good
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4599](https://github.com/microsoft/TypeScript-go/pull/4599) (Closed)

**Fix crash in CFA when for loop initializer throws**

*Control flow analysis crashes when a for loop initializer throws an exception.*

 * created by **Andarist**
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#4650](https://github.com/microsoft/TypeScript-go/pull/4650) (Closed, **RyanCavanaugh**, **Copilot**)

**Fix: experimentalDecorators renames class name in object literal key/member name positions**

*Prevent experimentalDecorators from renaming class names in object literal keys and member names by skipping identifier substitution in declaration positions.*

 * created by **Copilot**
 * (1 month ago) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4650#issuecomment-5319831690) **Copilot** addressed the code review comment in commit b6398ec by adding visitBindingElement and a matching KindBindingElement case, and updated the regression test to cover the const { C: x } case
 * [today](https://github.com/microsoft/TypeScript-go/pull/4650#issuecomment-5321088559) **Copilot** investigated the CR comment on computed class-element names, verified tsgo matches tsc behavior, and concluded the suggested change was incorrect
 * [today](https://github.com/microsoft/TypeScript-go/pull/4650#issuecomment-5321100529) **jakebailey** said "Yikes, if Strada (and Corsa right now) is wrong, then we should first commit the test showing the bug, and then commit the fix + baseline update"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4650#issuecomment-5321106723) **jakebailey** said "That is, if it's actually a bug, given ordering matters; definitely needs a spec read"

### [PR microsoft/TypeScript-go#4682](https://github.com/microsoft/TypeScript-go/pull/4682) (Closed, **andrewbranch**)

**\[api\] Always update inferred project if one is open**

*Automatically refresh an open inferred project when its contents change without requiring new file openings.*

 * created by **piotrtomiak**
 * **jakebailey** assigned to **andrewbranch**
 * **RyanCavanaugh** added label `Unmigrated PR`
 * **andrewbranch** removed label `Unmigrated PR`
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#4700](https://github.com/microsoft/TypeScript-go/pull/4700) (Closed, **andrewbranch**)

**Expose getFullyQualifiedName on the API Checker**

*Expose getFullyQualifiedName on the unstable Checker API to support symbol identification for compiler-based tooling.*

 * created by **WinterYukky**
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4700#issuecomment-5040980972) **WinterYukky** said "@microsoft-github-policy-service agree"
 * **jakebailey** assigned to **andrewbranch**
 * **RyanCavanaugh** added label `Unmigrated PR`
 * **andrewbranch** removed label `Unmigrated PR`
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#4701](https://github.com/microsoft/TypeScript-go/pull/4701) (Closed, `Unmigrated PR`, **andrewbranch**)

**\[api\] Add \`\.getNonMissingTypeOfSymbol\(\)\` getter**

*Add a .getNonMissingTypeOfSymbol() API getter to retrieve the non-missing type of a symbol.*

 * created by **mrazauskas**
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4701#issuecomment-5077494102) **mrazauskas** noted inconsistent usage of GetTypeOfSymbol methods between api/session and ls/api and asked if it was an oversight
 * **jakebailey** assigned to **andrewbranch**
 * **RyanCavanaugh** added label `Unmigrated PR`
 * [today](https://github.com/microsoft/TypeScript-go/pull/4701#issuecomment-5320677368) **andrewbranch** said "Since this has merge conflicts, I will cherry-pick this in after we move repos."
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#4703](https://github.com/microsoft/TypeScript-go/pull/4703) (Closed, `Unmigrated PR`)

**Store value symbol links inline on checker\-created symbols**

*Value symbol links for checker-created symbols are stored inline to eliminate paged store overhead and improve check performance.*

 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/4703#issuecomment-5299086842) **jakebailey** said "@typescript-bot perf test this faster"
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/4703#issuecomment-5299087312) **typescript-automation[bot]** announced that performance tests had started and provided links to build status and results
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/4703#issuecomment-5299251811) **typescript-automation[bot]** provided perf run results in a detailed comparison report
 * [today](https://github.com/microsoft/TypeScript-go/pull/4703#issuecomment-5318688618) **jakebailey** said "This is big and invasive enough that I don't think I want to see this merge before the repo move."
 * **jakebailey** added label `Unmigrated PR`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4712](https://github.com/microsoft/TypeScript-go/pull/4712) (Closed)

**Content mappers**

*Implement content mappers that enable TypeScript to include unsupported file types by transforming them via tsconfig settings.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5306567880) **remcohaszing** proposed validating content mapper options with contextual diagnostics via a new or extended API
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5309110710) **remcohaszing** published an experimental MDX content mapper, reported false positive mapping errors during type checking, and asked whether the bug was in this PR or his implementation
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5309348759) **escaton** shared early testing results and included project cloc statistics and tsconfig.json configuration
 * [today](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5318587603) **andrewbranch** explained that the mapper bug was caused by using UTF-8 offsets with JS’s UTF-16 string indexing and recommended using UTF-16

### [PR microsoft/TypeScript-go#4723](https://github.com/microsoft/TypeScript-go/pull/4723) (Closed, **jakebailey**, **Copilot**)

**Preserve comments when downleveling arrow expression bodies**

*Adjust arrow function downleveling to preserve comment placement by applying original source ranges to synthesized return statements.*

 * (3 weeks ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4723#issuecomment-5243175220) **jakebailey** provided a test case from another issue comment for optional chaining
 * [today](https://github.com/microsoft/TypeScript-go/pull/4723#issuecomment-5318108076) **jakebailey** said "You're definitely right, but Strada double sets too: https://github.com/microsoft/TypeScript/blob/5848bc5157b22ff7f4e3369f4645a514a433b15f/src/compiler/factory/nodeConverters.ts#L54-L60"

### [PR microsoft/TypeScript-go#4741](https://github.com/microsoft/TypeScript-go/pull/4741) (Closed, `Unmigrated PR`)

**Allocate node and symbol IDs in per\-checker blocks**

*Allocates node and symbol IDs in per-checker contiguous blocks to reduce contention and memory usage and enhance performance.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4741#issuecomment-5079055305) **jakebailey** said "@typescript-bot perf test this"
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4741#issuecomment-5079055587) **typescript-automation[bot]** reported that perf test jobs started and linked to build and results
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4741#issuecomment-5079144193) **typescript-automation[bot]** provided the performance comparison report for the requested perf run
 * **jakebailey** added label `Unmigrated PR`
 * [today](https://github.com/microsoft/TypeScript-go/pull/4741#issuecomment-5320253183) **jakebailey** said "Same diff as the other PR; we're moving repos and while this isn't exactly wrong I don't think we're going to merge this right now. But we can reopen this on the other repo in the future."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4784](https://github.com/microsoft/TypeScript-go/pull/4784) (Closed)

**Build checker cache keys in an inline buffer with one\-shot hashing**

*Use a small inline buffer and one-shot xxh3 hashing in the checker cache key builder to reduce overhead.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4784#issuecomment-5119247572) **jakebailey** mentioned uncertainty about maintenance cost, said he would review the test file, and noted that key builder logic might become obsolete in a future Go release
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4784#issuecomment-5120023481) **jakebailey** said "Mainly, we already have checker_test.go. It just really loves adding new files"
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4784#issuecomment-5120254247) **typescript-automation[bot]** posted the requested performance run results with detailed comparison metrics
 * [today](https://github.com/microsoft/TypeScript-go/pull/4784#issuecomment-5320263355) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4784#issuecomment-5320264226) **typescript-automation[bot]** reported CI performance tests started and provided links to status and results
 * [today](https://github.com/microsoft/TypeScript-go/pull/4784#issuecomment-5320538076) **typescript-automation[bot]** posted the requested performance run results with a detailed comparison report for metrics such as errors, symbols, types, and memory usage
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4786](https://github.com/microsoft/TypeScript-go/pull/4786) (Closed, `Unmigrated PR`)

**Shrink \`ast\.Symbol\` from 96 to 80 bytes**

*Move unused ast.Symbol fields into a lazily allocated extra struct to shrink symbol size and reduce memory usage.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4786#issuecomment-5138267278) **jakebailey** said "@typescript-bot perf test this faster"
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4786#issuecomment-5138267835) **typescript-automation[bot]** announced start of performance tests and linked to build status and results
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4786#issuecomment-5138487457) **typescript-automation[bot]** posted the requested perf run results including a detailed comparison report
 * **RyanCavanaugh** added label `Unmigrated PR`
 * (later) **mds-ant** closed the issue

### [PR microsoft/TypeScript-go#4791](https://github.com/microsoft/TypeScript-go/pull/4791) (Closed, **andrewbranch**)

**Add getSymbolOfSourceFile to the API**

*Introduce getSymbolOfSourceFile to directly retrieve a source file’s symbol without loading its AST*

 * created by **dragomirtitian**
 * **jakebailey** assigned to **andrewbranch**
 * **RyanCavanaugh** added label `Unmigrated PR`
 * **jakebailey** removed label `Unmigrated PR`
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#4803](https://github.com/microsoft/TypeScript-go/pull/4803) (Closed, **andrewbranch**)

**Fix panic when serializing empty tuple array literal types**

*Serializing an array literal typed as an empty tuple triggers a tsgo server panic due to mismatched type flags.*

 * created by **artem1458**
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4803#issuecomment-5144209590) **artem1458** said "@microsoft-github-policy-service agree"
 * **jakebailey** assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4803#issuecomment-5320821964) **andrewbranch** expressed that the proposed solution was incorrect and said they would reopen a better fix PR after the repo is moved back
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#4807](https://github.com/microsoft/TypeScript-go/issues/4807) (Closed, `bug`, **ahejlsberg**)

**False “Excessive stack depth” on circular types linked through arrays \(regression from \#3445\)**

*tsgo 7.0.2 erroneously reports excessive stack depth comparing circular interfaces connected via optional arrays, a regression from TypeScript 6.0*

 * (2 weeks ago) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `Post-7.0`, and assigned to **ahejlsberg**
 * [later](https://github.com/microsoft/TypeScript-go/issues/4807#issuecomment-5329498520) **ahejlsberg** explained that the 100-level stack depth error is unnecessary and proposed stopping type relating instead of erroring, and said they would submit a PR to implement the change
 * (later) **ahejlsberg** added label `bug`, and removed label `Needs Investigation`

### [PR microsoft/TypeScript-go#4829](https://github.com/microsoft/TypeScript-go/pull/4829) (Closed, **RyanCavanaugh**, **Copilot**)

**Fix go\-to\-definition for multi\-source declaration maps**

*When declaration maps reference different source files, go-to-definition now prioritizes the identifier mapping file to correct erroneous file links.*

 * (1 week ago) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/4829#issuecomment-5295665751) **Copilot** explained that targetSelectionLoc is now authoritative for TargetUri, context mapping only provides a broader TargetRange when URIs match, otherwise the selection range is used, and noted it was addressed in commit d9ec7ca9
 * [today](https://github.com/microsoft/TypeScript-go/pull/4829#issuecomment-5318181175) **RyanCavanaugh** said "Not confident enough in this one yet. Pick up post-move."
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#4839](https://github.com/microsoft/TypeScript-go/pull/4839) (Closed, **sandersn**)

**fix\(63726\): fix declaration emit for multiline jsdoc literal types**

*Ensure TypeScript declaration files accurately emit multiline JSDoc literal types.*

 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/4839#issuecomment-5299160812) **jakebailey** said "The suppressed comment actually seems possibly true, have not checked."
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/4839#issuecomment-5299242468) **jakebailey** said "Checked, and what it noted is already a 6.0 problem, so nothing new"
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/4839#issuecomment-5299292423) **jakebailey** suggested adding JSDoc type expression detection and stripping prefixes in GetTextOfNodeFromSourceText
 * [today](https://github.com/microsoft/TypeScript-go/pull/4839#issuecomment-5318860593) **jakebailey** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4839#issuecomment-5318861417) **typescript-automation[bot]** reported test jobs starting and provided links to their build and result status
 * [today](https://github.com/microsoft/TypeScript-go/pull/4839#issuecomment-5319198280) **typescript-automation[bot]** provided performance run results comparing baseline to PR for tsc
 * (today) **jakebailey** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/4839#issuecomment-5319634646) **typescript-automation[bot]** reported that running the top 400 repos with tsc on main versus the pull request merge succeeded without issues

### [PR microsoft/TypeScript-go#4846](https://github.com/microsoft/TypeScript-go/pull/4846) (Closed, `Unmigrated PR`)

**Fix crash when a call signature's type parameter cannot be reused**

*TypeScript Go printer crashes when reuseNode fails and inserts a nil type parameter into a call signature.*

 * created by **nikeedw**
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4846#issuecomment-5222019357) **nikeedw** explained that the crash matched a previous bug, described how the earlier PR fixed one producer by adding a guard against nil nodes, showed the analogous fix in this PR, and warned that other unchecked node-builder paths could still yield nil and cause similar SIGSEGV crashes
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4846#issuecomment-5222176600) **nikeedw** provided a detailed static and dynamic survey showing that on main, NodeList constructions produce no nil elements in the test suite and only one nil in the two-file repro scenario
 * **RyanCavanaugh** added label `Unmigrated PR`

### [PR microsoft/TypeScript-go#4877](https://github.com/microsoft/TypeScript-go/pull/4877) (Closed)

**Gate ES2025 regex syntax behind target**

*Compiler enforces ES2025 regex syntax gating for the 'v' flag and duplicate named capture groups based on target.*

 * created by **dayongkr**
 * [6 days ago](https://github.com/microsoft/TypeScript-go/pull/4877#issuecomment-5255324707) **dayongkr** said "@microsoft-github-policy-service agree"
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/4877#issuecomment-5302292364) **dayongkr** acknowledged landing of #4881, merged it resolving the nested case, refined the duplicate diagnostic range, updated the test matrix, and requested review
 * **RyanCavanaugh** added label `Unmigrated PR`
 * [today](https://github.com/microsoft/TypeScript-go/pull/4877#issuecomment-5322215945) **dayongkr** said "@jakebailey license/cla has been stuck in pending and never reported back. (CLA is signed on my end)"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4902](https://github.com/microsoft/TypeScript-go/pull/4902) (Closed, `Unmigrated PR`)

**Fix transpile test diffs**

*Urgently fix the newly introduced transpile test diffs before they are deleted.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4902#issuecomment-5320675150) **jakebailey** said "I'm not confident enough at this stage. I don't like that we will lose the diffs but we can just do some trickery I guess in a separate PR to try and fix the bugs."
 * **jakebailey** added label `Unmigrated PR`

### [PR microsoft/TypeScript-go#4903](https://github.com/microsoft/TypeScript-go/pull/4903) (Closed, `Unmigrated PR`)

**Remove AST node self pointers**

*Remove self-referencing pointers from AST nodes now that unsafe code is confined to generated code.*

 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/4903#issuecomment-5296092622) **typescript-automation[bot]** reported that performance test jobs started and provided links to build status and results
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/4903#issuecomment-5296374795) **typescript-automation[bot]** provided the requested performance comparison results for the tsc run
 * **jakebailey** added label `Unmigrated PR`
 * [today](https://github.com/microsoft/TypeScript-go/pull/4903#issuecomment-5317644096) **DanielRosenwasser** said "I wonder why the compiler self builds seem to use more memory, and why xstate still gets slower in checking."
 * [today](https://github.com/microsoft/TypeScript-go/pull/4903#issuecomment-5317984406) **jakebailey** said "Yeah, those are the primary problems"

### [Issue microsoft/TypeScript-go#4904](https://github.com/microsoft/TypeScript-go/issues/4904) (Open, `Needs Investigation`, **johnfav03**)

**\[ServerErrors\]\[TypeScript\] main vs **

*The TypeScript main branch pipeline analyzed 300 popular GitHub repositories, reporting 29 detected changes, 147 no-changes, and several clone, timeout, and unknown failures.*

 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/4904#issuecomment-5299218377) **typescript-automation[bot]** reported a panic in the textDocument/diagnostic handler with stack trace for makeplane/plane
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/4904#issuecomment-5299218416) **typescript-automation[bot]** reported a panic due to invalid memory address or nil pointer dereference with stack trace
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/4904#issuecomment-5299218479) **typescript-automation[bot]** reported a panic during a textDocument/diagnostic request, including a stack trace and details for pubkey/rxdb
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **johnfav03**

### [PR microsoft/TypeScript-go#4905](https://github.com/microsoft/TypeScript-go/pull/4905) (Closed, `dependencies`, `github_actions`)

**Bump the github\-actions group across 1 directory with 5 updates**

*Bump versions of five GitHub Actions in the repository root, including actions/checkout, actions/setup-node, and CodeQL actions.*

 * (today) **dependabot[bot]** added labels `github_actions`, `dependencies`, `github_actions`
 * (today) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/4905#issuecomment-5318317007) **dependabot[bot]** notified that closing the pull request will not ignore dependencies in future and directed to configure ignore rules in dependabot.yml

### [PR microsoft/TypeScript-go#4906](https://github.com/microsoft/TypeScript-go/pull/4906) (Closed)

**Fix tsdk resolution for npm aliases**

*Adjust tsdk resolution to properly handle npm aliases in reported and additional cases, pending extension republishing.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4907](https://github.com/microsoft/TypeScript-go/pull/4907) (Closed, **DanielRosenwasser**, **Copilot**)

**Add regression coverage for the JSX text formatting crash**

*Added regression test to verify JSX text formatting in arrow-function returns no longer crashes the formatter.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * (today) **DanielRosenwasser** closed the issue

### [Issue microsoft/TypeScript-go#4908](https://github.com/microsoft/TypeScript-go/issues/4908) (Closed, `bug`, `Domain: Editor`, **DanielRosenwasser**, **Copilot**)

**Go\-to\-definition does not work at the right edge of a JSX tag name**

*Go-to-definition fails when invoked at the right edge of a JSX tag name in the updated codebase.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** added labels `bug`, `Domain: Editor`, and assigned to **Copilot**, **DanielRosenwasser**

### [PR microsoft/TypeScript-go#4909](https://github.com/microsoft/TypeScript-go/pull/4909) (Closed, **DanielRosenwasser**, **Copilot**)

**Fix go\-to\-definition functionality at JS JSX tag edge**

*Align go-to-definition token selection at JSX tag name edges and add focused tests and validations*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * (today) **DanielRosenwasser** closed the issue
 * (today) **DanielRosenwasser** reopened the issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/4909#issuecomment-5320593803) **DanielRosenwasser** said "@copilot+gpt-5.6-sol you added the test but not the fix."
 * [today](https://github.com/microsoft/TypeScript-go/pull/4909#issuecomment-5320856805) **Copilot** implemented the touching-token fix, refined existing completion behavior, and added an accepted definition baseline for the JSX go-to-definition test

### [PR microsoft/TypeScript-go#4910](https://github.com/microsoft/TypeScript-go/pull/4910) (Closed)

**Fix extension temp paths on macOS**

*Correct extension temporary path resolution to handle symlinked TMP directories on macOS.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4911](https://github.com/microsoft/TypeScript-go/pull/4911) (Closed, `Unmigrated PR`)

**Better handle signals in tsc CLI**

*Enhance the TypeScript compiler CLI to properly handle operating system signals and interruptions*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4911#issuecomment-5321094101) **DanielRosenwasser** said "Wasn't part of the original intent for handling signals to do something special during profiling?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4911#issuecomment-5321120303) **jakebailey** remarked that profiling watch mode would be required and proposed postponing a more complex cancellation or exit hook solution
 * [today](https://github.com/microsoft/TypeScript-go/pull/4911#issuecomment-5321232461) **lukesandberg** reported odd panics on ctrl-c in watch mode build and shared a link to an alternative implementation avoiding the issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/4911#issuecomment-5321285533) **jakebailey** said "That's plausible, but that platform code would belong in osutil."
 * [today](https://github.com/microsoft/TypeScript-go/pull/4911#issuecomment-5321287755) **jakebailey** said "Feel free to open it, I just assumed you wouldn't reply so quickly 😄 "
 * [today](https://github.com/microsoft/TypeScript-go/pull/4911#issuecomment-5321296935) **lukesandberg** said "I don't have permissions to open PRs anymore"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4911#issuecomment-5321319271) **jakebailey** said "If you restore the branch in microsoft/typescript-go#4592, I can reopen it"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4911#issuecomment-5321374632) **lukesandberg** mentioned that the commit was on a different branch and suggested cherry-picking it

### [PR microsoft/TypeScript-go#4912](https://github.com/microsoft/TypeScript-go/pull/4912) (Closed, `dependencies`, `go`)

**Bump software\.sslmate\.com/src/go\-pkcs12 from 0\.7\.0 to 0\.7\.2**

*Upgrade software.sslmate.com/src/go-pkcs12 dependency from version 0.7.0 to 0.7.2.*

 * created by **dependabot[bot]**
 * (today) **dependabot[bot]** added labels `dependencies`, `go`, `dependencies`, `go`
 * (today) **jakebailey** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/4912#issuecomment-5321221221) **dependabot[bot]** explained how to ignore dependency update notifications or reopen the PR to resolve conflicts

### [PR microsoft/TypeScript-go#4913](https://github.com/microsoft/TypeScript-go/pull/4913) (Closed)

**Improve recursion identities and \`isDeeplyNestedType\`**

*Refine recursion identities for indexed access types and eliminate excessive stack depth errors in isDeeplyNestedType.*

 * created by **ahejlsberg**
 * [later](https://github.com/microsoft/TypeScript-go/pull/4913#issuecomment-5330407109) **ahejlsberg** said "@typescript-bot test it"
 * [later](https://github.com/microsoft/TypeScript-go/pull/4913#issuecomment-5330408300) **typescript-automation[bot]** reported that CI jobs started and updated their statuses with links to results
 * [later](https://github.com/microsoft/TypeScript-go/pull/4913#issuecomment-5330768512) **typescript-automation[bot]** provided performance run results

