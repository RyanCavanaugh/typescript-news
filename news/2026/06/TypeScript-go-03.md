# Report for 2026-06-03 (Wednesday, June 3rd, 2026)

13 different users commented on 103 different issues.

## Recommended Actions

 * Response Recommended
    * @doylio asked if the 'save heap profile' command was faulty and provided profile files in [microsoft/TypeScript-go#3032](https://github.com/microsoft/TypeScript-go/issues/3032#issuecomment-4614469865)
    * @doylio provided environment information in [microsoft/TypeScript-go#3032](https://github.com/microsoft/TypeScript-go/issues/3032#issuecomment-4623028146)
    * @Utsav006 provided a workaround for UTF-16 surrogate handling that may help unblock the inference test case in [microsoft/TypeScript-go#4181](https://github.com/microsoft/TypeScript-go/pull/4181#issuecomment-4622169728)

## Activity Summary

### [Issue microsoft/TypeScript-go#3032](https://github.com/microsoft/TypeScript-go/issues/3032) (Closed, `Domain: Editor`, `Needs More Info`)

**tsgo \-\-lsp memory leak on large projects / triggers OOM**

*The tsgo LSP process in the TypeScript Native Preview extension leaks memory when handling large projects, causing OOM on low-RAM Linux machines.*

 * (12 weeks ago) **andrewbranch** closed the issue
 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/3032#issuecomment-4577836639) **doylio** reported experiencing the issue regularly and provided a heap profile
 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/3032#issuecomment-4578621535) **andrewbranch** said "@doylio it seems like that profile got truncated during upload. Can you try again?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/3032#issuecomment-4614469865) **doylio** attached heap profile files and asked if the 'save heap profile' command was faulty since they couldn't unzip them
 * [today](https://github.com/microsoft/TypeScript-go/issues/3032#issuecomment-4614729351) **andrewbranch** said "Indeed, so strange, all of these are invalid. I've never seen this before. What OS are you on?"
 * [later](https://github.com/microsoft/TypeScript-go/issues/3032#issuecomment-4623028146) **doylio** said "MacOS Tahoe 26.5.1"
 * [later](https://github.com/microsoft/TypeScript-go/issues/3032#issuecomment-4623808592) **andrewbranch** said "@jakebailey any ideas?"

### [Issue microsoft/TypeScript-go#3094](https://github.com/microsoft/TypeScript-go/issues/3094) (Closed, `bug`, **weswigham**)

**Declaration emit proceeds in the presence of TS7056**

*TypeScript emits declarations despite TS7056 errors caused by deeply nested conditional and tag-branded utility types.*

 * [9 weeks ago](https://github.com/microsoft/TypeScript-go/issues/3094#issuecomment-4158824453) **weswigham** provided a status update on declaration emit behaviour in corsa versus strada, mentioned a 4-line diff to align implementations, and noted ongoing debugging of -b unit test failures
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/3094#issuecomment-4455307998) **weswigham** noted that the "inferred type of this node exceeds the maximum length the compiler will serialize" error indicates truncated output and isn’t a workaround for TS roundtrip validity
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript-go#3171](https://github.com/microsoft/TypeScript-go/pull/3171) (Closed, **ahejlsberg**, **RyanCavanaugh**, **Copilot**)

**Fix stack overflow in relater's skipCaching path for recursive tuple types**

*Add depth counters to prevent unbounded recursion and stack overflow in the relater skipCaching path for recursive tuple types.*

 * (6 weeks ago) **RyanCavanaugh** set milestones to `Post-7.0`, `TypeScript 7.0 RC`, and removed from milestone `Post-7.0`
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#3175](https://github.com/microsoft/TypeScript-go/pull/3175) (Closed, **ahejlsberg**, **RyanCavanaugh**, **Copilot**)

**Fix template literal type exponential blowup in addSpans**

*Add growth limits in addSpans to prevent exponential template literal type expansion causing memory exhaustion.*

 * **RyanCavanaugh** assigned to **ahejlsberg**
 * [6 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3175#issuecomment-4264113737) **jakebailey** said "This just adds in a new limit that Strada didn't have. I don't think this is right."
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#3495](https://github.com/microsoft/TypeScript-go/pull/3495) (Open)

**Use JS\-compatible Unicode casing for intrinsic string mappings**

*Implement JavaScript-compatible Unicode casing rules in TypeScript’s intrinsic string mapping functions.*

 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/3495#issuecomment-4598934154) **jakebailey** asked to ensure testing of toLowerCase final-sigma context divergences for strings of the form rΣ
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/3495#issuecomment-4599345981) **Andarist** questioned whether tests were required for all 267 items, noting an existing unit test included a single example of divergence
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3495#issuecomment-4600953236) **jakebailey** said "No, not all of them I don't think, but a few. Or some sort of way to generate them and then use https://github.com/microsoft/typescript-go/tree/main/internal/testutil/jstest to cross check?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3495#issuecomment-4615709778) **jakebailey** said "Just to be clear, I think this PR is fine after my suggested changes. Unfortunate that this is required but obviously JS and Unicode are a terrible pair"

### [Issue microsoft/TypeScript-go#3617](https://github.com/microsoft/TypeScript-go/issues/3617) (Open, `Needs Investigation`, **iisaduan**)

**fix: FindBestPatternMatch incorrectly allows wildcard pattern to override exact match**

*FindBestPatternMatch misuses StarIndex so exact matches set longestMatchPrefixLength to -1, allowing later wildcard patterns to override exact matches.*

 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/3617#issuecomment-4401880065) **RyanCavanaugh** said "@kuishou68 how does this manifest? There's no external-visible behavorial description nor testcase in that PR, so it's hard to know the severity/priority of this"
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/3617#issuecomment-4592514890) **matyasf** described reproduction steps demonstrating incorrect import paths when building with tsgo in a composite TypeScript project
 * [today](https://github.com/microsoft/TypeScript-go/issues/3617#issuecomment-4615071752) **andrewbranch** said "I reduced @matyasf's repro to a compiler test and found that it's not fixed by #3618, so probably not related to this issue."

### [PR microsoft/TypeScript-go#3696](https://github.com/microsoft/TypeScript-go/pull/3696) (Closed, `dependencies`, `devcontainers_package_manager`)

**Bump ghcr\.io/devcontainers/features/node from 1\.7\.1 to 2\.0\.0**

*Update the Node feature in devcontainers from version 1.7.1 to 2.0.0.*

 * (1 month ago) **dependabot[bot]** added labels `devcontainers_package_manager`, `dependencies`, `devcontainers_package_manager`
 * **RyanCavanaugh** added to milestone `Possible Improvement`
 * [later](https://github.com/microsoft/TypeScript-go/pull/3696#issuecomment-4621306986) **jakebailey** said "@dependabot rebase"
 * (later) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3717](https://github.com/microsoft/TypeScript-go/pull/3717) (Closed)

**Proposed actions for symbol baseline diffs**

*Place 'needs investigation' groups at the top of symbol baseline diffs, mirroring the previous procedure.*

 * created by **RyanCavanaugh**
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#3785](https://github.com/microsoft/TypeScript-go/pull/3785) (Closed, `dependencies`, `javascript`)

**Bump fast\-uri from 3\.1\.0 to 3\.1\.2**

*Update fast-uri dependency to v3.1.2 to incorporate security fixes and improve malformed fragment error handling*

 * created by **dependabot[bot]**
 * (3 weeks ago) **dependabot[bot]** added labels `dependencies`, `javascript`
 * **RyanCavanaugh** added to milestone `Possible Improvement`
 * [later](https://github.com/microsoft/TypeScript-go/pull/3785#issuecomment-4621298874) **jakebailey** said "@dependabot rebase"
 * [later](https://github.com/microsoft/TypeScript-go/pull/3785#issuecomment-4621317737) **dependabot[bot]** said "Looks like fast-uri is up-to-date now, so this is no longer needed."
 * (later) **dependabot[bot]** closed the issue

### [Issue microsoft/TypeScript-go#3792](https://github.com/microsoft/TypeScript-go/issues/3792) (Closed, `Needs Investigation`, **andrewbranch**, **Copilot**)

**\[lsp\] Experimental server capabilities should be defined on "experimental" object**

*Align server capabilities with the LSP specification by defining experimental features under the "experimental" property*

 * (2 weeks ago) **RyanCavanaugh** added label `Needs Investigation`, and set milestone to `TypeScript 7.0 RC`
 * **andrewbranch** assigned to **Copilot**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#3826](https://github.com/microsoft/TypeScript-go/pull/3826) (Open)

**Add version & a common session identifier to events from LS clients**

*Include version and common session ID in language server client events to improve version-specific error tracking and correlate diagnostics.*

 * created by **DanielRosenwasser**
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3826#issuecomment-4442659320) **jakebailey** said "I don't think dotted names are legal names for end users of this?"
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3826#issuecomment-4444367810) **DanielRosenwasser** noted no indication that dotted names are illegal for end users and acknowledged possible error
 * **RyanCavanaugh** added to milestone `Possible Improvement`

### [PR microsoft/TypeScript-go#3840](https://github.com/microsoft/TypeScript-go/pull/3840) (Open)

**Don't send bundled file watchers to client**

*Filter out bundled TypeScript library file patterns from LSP server watch requests to prevent invalid client watchers.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3840#issuecomment-4448612870) **xuanduc987** asked if the asset bundling constraint was documented and offered to raise an issue in nixpkgs
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3840#issuecomment-4448739859) **jakebailey** said "No, but it's just hereby build which does all the work to build it, and the herebyfile contains more info about how we build the releases"
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3840#issuecomment-4448742318) **jakebailey** said "I don't think this PR is wrong, but we probably need a test that is conditional on whether or not embedding is enabled"
 * (today) **RyanCavanaugh** set milestones to `TypeScript 7.0 RC`, `Possible Improvement`, and removed from milestone `TypeScript 7.0 RC`

### [PR microsoft/TypeScript-go#3872](https://github.com/microsoft/TypeScript-go/pull/3872) (Open, **RyanCavanaugh**, **Copilot**)

**Reclassify \`nodeModulesAllowJsImportAssignment\` JS emit diffs as accepted baselines**

*Reclassify nodeModulesAllowJsImportAssignment JS emit diffs as accepted baselines reflecting export import changes.*

 * (2 weeks ago) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * [today](https://github.com/microsoft/TypeScript-go/pull/3872#issuecomment-4615664766) **RyanCavanaugh** said "@copilot merge with main"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3872#issuecomment-4615766730) **Copilot** merged origin/main into the branch and resolved the conflict in submoduleTriaged.txt by keeping CJS module.exports entries and dropping nodeModulesAllowJsImportAssignment entries

### [Issue microsoft/TypeScript-go#3873](https://github.com/microsoft/TypeScript-go/issues/3873) (Closed, `Crash`, **DanielRosenwasser**, **andrewbranch**, **Copilot**)

**Fatal crash in \`\(\*Program\)\.SingleThreaded\` on snapshot update**

*The compiler’s Program.SingleThreaded method crashes fatally when updating project snapshots in the language server.*

 * (2 weeks ago) **DanielRosenwasser** added label `Crash`, and assigned to **DanielRosenwasser**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * **andrewbranch** assigned to **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#3874](https://github.com/microsoft/TypeScript-go/pull/3874) (Closed, **DanielRosenwasser**, **Copilot**)

**Fix nil pointer crash in Program\.SingleThreaded on snapshot update**

*Prevent nil pointer crash by adding nil checks in SingleThreaded and skipping CreateProgram when CommandLine is unset.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3874#issuecomment-4463078701) **Copilot** updated the PR description to follow the template and noted that build, test, lint, and format checks passed
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3874#issuecomment-4463100044) **jakebailey** said "no it doesn't, not at all"
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * [today](https://github.com/microsoft/TypeScript-go/pull/3874#issuecomment-4617754830) **andrewbranch** said "This is not it 👎 "
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#3900](https://github.com/microsoft/TypeScript-go/issues/3900) (Closed, `Crash`, **jakebailey**, **Copilot**)

**tsgo source\-map emit panics for an unclosed block**

*Emitting source maps in tsgo causes a slice bounds panic when encountering an unclosed code block.*

 * (2 weeks ago) **jakebailey** assigned to **Copilot**, **jakebailey**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3910](https://github.com/microsoft/TypeScript-go/pull/3910) (Open, **jakebailey**, **Copilot**)

**Fix incorrect renaming of \`arguments\` in non\-reference positions in async downlevel**

*Async downlevel incorrectly renames `arguments` in non-reference contexts, now fixed by using the AST IsIdentifierName utility and label checks.*

 * (2 weeks ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * [later](https://github.com/microsoft/TypeScript-go/pull/3910#issuecomment-4621288307) **jakebailey** said "@copilot merge main"

### [PR microsoft/TypeScript-go#3923](https://github.com/microsoft/TypeScript-go/pull/3923) (Closed, **jakebailey**, **Copilot**)

**Fix source\-map emit panic for unclosed blocks**

*Prevent panics in source-map emission by handling positions beyond EOF when processing unclosed code blocks*

 * (2 weeks ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * [today](https://github.com/microsoft/TypeScript-go/pull/3923#issuecomment-4615624161) **johnfav03** said "@copilot your baselines are stale, please rebase on main, run hereby tests, and accept the baselines"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3923#issuecomment-4615804736) **Copilot** rebased the branch on main, refreshed the stale source-map baselines, and ran the tests successfully
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3935](https://github.com/microsoft/TypeScript-go/pull/3935) (Open)

**Narrow keyword completions for concise arrow expression bodies**

*Port keyword completion filtering to Go so concise arrow function bodies only suggest expression keywords.*

 * created by **DhineshPonnarasan**
 * **RyanCavanaugh** added to milestone `Post-7.0`

### [Issue microsoft/TypeScript-go#3938](https://github.com/microsoft/TypeScript-go/issues/3938) (Closed, `Needs Investigation`, **andrewbranch**)

**Result of getTypeOfLocation for \`PropertyAccessExpression\` and \`ElementAccessExpression\` may be different between 6 and 7**

*Parenthesized and nested property accesses yield incorrect object types in tsgo v7’s getTypeAtLocation compared to TypeScript 6.*

 * (2 weeks ago) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **andrewbranch**
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/3938#issuecomment-4518938609) **jet2jet** described a bug where resolveNodeHandle in session.go returned an unexpected node instance and caused getResolvedSignature to crash for CallExpressions with PropertyAccessExpressions, and provided a stack trace
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#3940](https://github.com/microsoft/TypeScript-go/issues/3940) (Closed, `Domain: Editor`, `Crash`, **DanielRosenwasser**, **Copilot**)

**Fatal server crash at \`loadModuleFromSpecificNodeModulesDirectory\`**

*A fatal server crash occurs in loadModuleFromSpecificNodeModulesDirectory due to a missing nil check on Contents.*

 * (2 weeks ago) **DanielRosenwasser** added labels `Crash`, `Domain: Editor`
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * (later) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3941](https://github.com/microsoft/TypeScript-go/pull/3941) (Closed, **DanielRosenwasser**, **Copilot**)

**Fix nil dereference crash in loadModuleFromSpecificNodeModulesDirectory**

*Add packageInfo.Exists() check in loadModuleFromSpecificNodeModulesDirectory to prevent nil dereference and include concurrent-resolution regression tests.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3941#issuecomment-4474794206) **DanielRosenwasser** said "The test seems insufficient if this is about race conditions. @copilot is there a better test here? Possibly a server test or a programmatic test of our APIs?"
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3941#issuecomment-4474873463) **Copilot** replaced the compiler test with a programmatic race condition test and detailed deterministic reproduction steps
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * [today](https://github.com/microsoft/TypeScript-go/pull/3941#issuecomment-4616864044) **Copilot** described replacing sleep-based polling with channel-based synchronization and referenced commit 4ae3e12
 * [today](https://github.com/microsoft/TypeScript-go/pull/3941#issuecomment-4617480119) **andrewbranch** said "@copilot fix review feedback. Also looks like the code needs formatting."
 * [today](https://github.com/microsoft/TypeScript-go/pull/3941#issuecomment-4617518369) **Copilot** described changes made in commit 559ce3b, including formatting resolver_test.go, adding timeout-guarded waits, and enhancing regression assertions
 * [today](https://github.com/microsoft/TypeScript-go/pull/3941#issuecomment-4617881610) **andrewbranch** said "@copilot lint is failing"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3941#issuecomment-4617935644) **Copilot** fixed lint failure in internal/module/resolver_test.go by removing an unnecessary loop-variable copy and making the successful waitForSignal case explicit, and verified lint and tests passed
 * (later) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3943](https://github.com/microsoft/TypeScript-go/pull/3943) (Open)

**Fix crash inferring constrained variadic tuples with optional elements**

*Fix compiler crash during inference of constrained variadic tuples with optional elements*

 * created by **Andarist**
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3943#issuecomment-4479716867) **jakebailey** said "We have a couple of PRs touching this same code, e.g. #3917, #2928; I feel a little unclear what combo is correct in all of these"
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [PR microsoft/TypeScript-go#3996](https://github.com/microsoft/TypeScript-go/pull/3996) (Open)

**Extract tscInput tests to individual per\-scenario files with imperative edits to improve debuggability**

*Extract tscInput tests into individual scenario files with imperative edits, remove intra-test parallelism, simplify debugging while preserving original tests.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3996#issuecomment-4496173212) **jakebailey** said "Not sure I like this, but at the very least I think the filenames shouldn't start with capital T"
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3996#issuecomment-4500666020) **weswigham** said "The filename shouldn't start with a capital T but the function should, go figure. Fixed."
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3996#issuecomment-4500751011) **weswigham** asked if others preferred keeping test duplication for debuggability or the new test format and offered to delete originals and the extraction script
 * **RyanCavanaugh** added to milestone `Possible Improvement`

### [PR microsoft/TypeScript-go#4015](https://github.com/microsoft/TypeScript-go/pull/4015) (Closed)

**Do not emit declaration files when they contain a declaration emit error**

*Prevent TypeScript from emitting declaration files when declaration emit errors occur.*

 * created by **weswigham**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/4015#issuecomment-4596890943) **jakebailey** said "Needs a main merge but otherwise LGTM"
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript-go#4023](https://github.com/microsoft/TypeScript-go/pull/4023) (Closed)

**TDD Rewrite Subagent**

*Implement a subagent mode to automatically re-execute pull requests with questionable test reliability.*

 * created by **RyanCavanaugh**
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#4024](https://github.com/microsoft/TypeScript-go/pull/4024) (Open)

**Allow nil\-ing out arenas to break the GC link between nodes and the arena they came from**

*Allow arenas to be nilled out to sever GC links between nodes and their originating arenas, reducing diagnostic memory retention.*

 * created by **weswigham**
 * **RyanCavanaugh** added to milestone `Possible Improvement`

### [Issue microsoft/TypeScript-go#4041](https://github.com/microsoft/TypeScript-go/issues/4041) (Closed, `Needs Investigation`, **andrewbranch**)

**Behavior difference: getTypeAtLocation returns method type for private method call**

*tsgo’s getTypeAtLocation incorrectly returns the private method’s function type instead of the call expression’s return type.*

 * (1 week ago) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `Post-7.0`, and assigned to **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#4067](https://github.com/microsoft/TypeScript-go/pull/4067) (Open)

**Fix file rename crashes when dealing with solution configuration files**

*Prevent crashes when renaming solution configuration files by improving file rename handling.*

 * created by **DanielRosenwasser**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [PR microsoft/TypeScript-go#4069](https://github.com/microsoft/TypeScript-go/pull/4069) (Open)

**Fix JS bind expando declaration emit**

*Emit bound JS functions as proper function declarations with preserved expando properties instead of const alias types*

 * created by **cjc0013**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [PR microsoft/TypeScript-go#4078](https://github.com/microsoft/TypeScript-go/pull/4078) (Closed, **DanielRosenwasser**)

**Quick info & find\-all\-refs tests for JSDoc namespaces**

*Add quick info and find-all-references tests for JSDoc namespaces following issue #4073.*

 * created by **DanielRosenwasser**
 * (today) **RyanCavanaugh** assigned to **RyanCavanaugh**, **DanielRosenwasser**, and unassigned **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4078#issuecomment-4617186101) **RyanCavanaugh** said "Needs merge conflict resolution"
 * **RyanCavanaugh** added to milestone `Possible Improvement`

### [Issue microsoft/TypeScript-go#4080](https://github.com/microsoft/TypeScript-go/issues/4080) (Open)

**Add API to detect wherever a symbol is readonly**

*Add APIs to TypeScript's type checker for detecting whether a symbol is readonly or optional.*

 * created by **mrazauskas**
 * **RyanCavanaugh** added to milestone `Post-7.0`

### [Issue microsoft/TypeScript-go#4081](https://github.com/microsoft/TypeScript-go/issues/4081) (Open)

**Add API to get symbol type that respects the \`exactOptionalPropertyTypes\` option**

*Propose enhancing TypeScript’s symbol type retrieval API to honor exactOptionalPropertyTypes for both object and mapped types.*

 * created by **mrazauskas**
 * **RyanCavanaugh** added to milestone `Post-7.0`

### [Issue microsoft/TypeScript-go#4082](https://github.com/microsoft/TypeScript-go/issues/4082) (Closed, `Crash`, **jakebailey**, **Copilot**)

**Panic in declaration emit for a set accessor with no parameters**

*A set accessor without parameters causes a panic in the typescript-go printer due to an AST node type mismatch.*

 * **mds-ant** added label `Crash`
 * (2 days ago) **jakebailey** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4084](https://github.com/microsoft/TypeScript-go/issues/4084) (Closed, `Crash`, **jakebailey**, **Copilot**)

**Panic in \`tryLoadInputFileForPath\` when an exports/imports target equals the declarationDir/outDir**

*A slice bounds panic occurs in tryLoadInputFileForPath when an exports or imports target matches declarationDir or outDir.*

 * **mds-ant** added label `Crash`
 * (2 days ago) **jakebailey** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4085](https://github.com/microsoft/TypeScript-go/issues/4085) (Closed, `Crash`, **jakebailey**, **Copilot**)

**Panic on overlapping wildcard patterns**

*A slice bounds out-of-range panic occurs when resolving modules with overlapping wildcard patterns in typescript-go.*

 * **mds-ant** added label `Crash`
 * (2 days ago) **jakebailey** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4088](https://github.com/microsoft/TypeScript-go/issues/4088) (Closed, **jakebailey**, **Copilot**)

**Expando function inside a namespace emits \`export declare namespace\`**

*tsgo wrongly emits export declare namespace for a function's expando property inside a namespace, breaking the declaration file.*

 * created by **mds-ant**
 * (2 days ago) **jakebailey** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4094](https://github.com/microsoft/TypeScript-go/issues/4094) (Closed, **jakebailey**, **Copilot**)

**Emitted JSX factory differs for @jsx pragma preceded by another @token in the same comment**

*tsgo misparses an @jsx pragma preceded by another token in the same comment, emitting h instead of React.createElement.*

 * created by **mds-ant**
 * (2 days ago) **jakebailey** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4098](https://github.com/microsoft/TypeScript-go/issues/4098) (Closed, **jakebailey**, **Copilot**)

**tsgo drops TS2527 and emits an invalid \.d\.ts when a class member's inferred type is an object literal containing \`this\`**

*tsgo ignores a TS2527 error and produces an invalid .d.ts file when a class method returns an object literal containing this.*

 * created by **mds-ant**
 * (2 days ago) **jakebailey** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4101](https://github.com/microsoft/TypeScript-go/issues/4101) (Open, `Needs More Info`)

**Declaration emit spends significant CPU in getAliasForSymbolInContainer / getAlternativeContainingModules**

*Declaration emit spends excessive CPU time in getAlternativeContainingModules and getAliasForSymbolInContainer, causing slow builds.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/4101#issuecomment-4601359723) **Zzzen** apologized and explained that the codebase is proprietary and cannot be shared due to internal dependencies and complex approval process
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/4101#issuecomment-4601386649) **Zzzen** provided detailed benchmark results showing that PR #4102 reduced wall time by about 14.7% and increased peak memory usage by about 2.3%
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/4101#issuecomment-4606820385) **jakebailey** said "It would be good to be able to get access to this, I'm not really sure I like the way #4102 looks..."
 * (today) **RyanCavanaugh** added label `Needs More Info`, and set milestone to `Possible Improvement`

### [PR microsoft/TypeScript-go#4102](https://github.com/microsoft/TypeScript-go/pull/4102) (Open)

**Cache alias candidates for symbol accessibility**

*Cache alias candidates to optimize symbol accessibility resolution.*

 * created by **Zzzen**
 * **RyanCavanaugh** added to milestone `Possible Improvement`

### [PR microsoft/TypeScript-go#4109](https://github.com/microsoft/TypeScript-go/pull/4109) (Closed, **jakebailey**, **Copilot**)

**Preserve lone surrogate escapes in string literal emit**

*Preserve lone Unicode surrogate escapes during string literal scanning and emission and add regression tests.*

 * created by **Copilot**
 * (4 days ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * [later](https://github.com/microsoft/TypeScript-go/pull/4109#issuecomment-4621276251) **jakebailey** said "#4181 "
 * (later) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4115](https://github.com/microsoft/TypeScript-go/issues/4115) (Closed, **jakebailey**, **Copilot**)

**Exit codes 1 and 2 \(OutputsSkipped vs OutputsGenerated\) are swapped**

*tsgo swaps exit codes 1 and 2 for suppressed versus generated outputs compared to TypeScript 6.0*

 * created by **mds-ant**
 * (2 days ago) **jakebailey** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4117](https://github.com/microsoft/TypeScript-go/issues/4117) (Closed, **jakebailey**, **Copilot**)

**\`\-\-inlineSourceMap\` leaks into \`\-\-declarationMap\` emit**

*tsgo incorrectly applies inlineSourceMap to declarationMap output, embedding inline maps in .d.ts files*

 * created by **mds-ant**
 * (3 days ago) **jakebailey** assigned to **Copilot**, **jakebailey**
 * (today) **gabritto** closed the issue

### [Issue microsoft/TypeScript-go#4118](https://github.com/microsoft/TypeScript-go/issues/4118) (Open, `bug`, **weswigham**)

**Declaration emit drops expando function properties whose assignments are not top\-level expression statements**

*Tsgo's declaration emitter only emits expando function properties assigned as top-level statements and drops those assigned within initializers or blocks.*

 * created by **mds-ant**
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/4118#issuecomment-4595109846) **jakebailey** said "I suspect this is sort of intentional (or at least, was not thought of), given our reparsing system... Does anyone actually do this?"
 * (later) **jakebailey** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#4125](https://github.com/microsoft/TypeScript-go/issues/4125) (Closed, **jakebailey**, **Copilot**)

**'Duplicate function implementation' reported on function redeclaration in checked \.js files**

*tsgo erroneously reports TS2393 duplicate function implementation errors for function redeclarations in checked JavaScript files, whereas TypeScript 6.0 does not.*

 * created by **mds-ant**
 * (2 days ago) **jakebailey** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4127](https://github.com/microsoft/TypeScript-go/issues/4127) (Open)

**JSDoc @satisfies on export default is enforced by tsgo but ignored by tsc**

*tsgo enforces JSDoc @satisfies on export default assignments while tsc ignores the type mismatch*

 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/4127#issuecomment-4594581173) **jakebailey** questioned whether this behavior in 6.0 was an oversight and provided a code snippet that errors
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/4127#issuecomment-4594583449) **jakebailey** said "But maybe the "right" way is to stick @satisfies onto the expression inside the export."
 * [today](https://github.com/microsoft/TypeScript-go/issues/4127#issuecomment-4614286914) **sandersn** recalled intentionally pushing satisfies down to the expression in Corsa and for issue #4128, and noted uncertainty about Strada and possibly not updating CHANGES.md
 * [today](https://github.com/microsoft/TypeScript-go/issues/4127#issuecomment-4616226804) **jakebailey** said "For this / #4128 I do not remember at all what we said or if we even said anything."

### [Issue microsoft/TypeScript-go#4133](https://github.com/microsoft/TypeScript-go/issues/4133) (Closed, **jakebailey**, **Copilot**)

**Unquoted tsconfig\.json keys: tsgo reports each TS1327 twice**

*tsgo reports TS1327 errors twice for each unquoted key in tsconfig.json*

 * created by **mds-ant**
 * (3 days ago) **jakebailey** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4140](https://github.com/microsoft/TypeScript-go/pull/4140) (Closed, **jakebailey**, **Copilot**)

**Align tsconfig JSON key diagnostics with TypeScript**

*Removed duplicate unquoted key TS1327 diagnostics in tsconfig.json, retained parser errors, added TS8009 for optional property tokens, and updated tests.*

 * **Copilot** assigned to **jakebailey**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4140#issuecomment-4607219494) **jakebailey** said "@copilot+gpt-5.5 merge main"
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4140#issuecomment-4607302517) **Copilot** merged origin/main into the PR and resolved the tsconfig parsing test conflict by keeping both sets of coverage; validated with go test and confirmed CodeQL passed
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4141](https://github.com/microsoft/TypeScript-go/pull/4141) (Open, **jakebailey**, **Copilot**)

**Report JSON syntax errors from extended tsconfig files**

*tsgo now surfaces JSON syntax errors in extended tsconfig files and includes regression tests to ensure proper diagnostic attribution.*

 * **Copilot** assigned to **jakebailey**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4141#issuecomment-4607523204) **jakebailey** said "@copilot+gpt-5.5 merge main"
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4141#issuecomment-4607597491) **Copilot** merged main, resolved tsconfig parsing test conflict preserving both tests, and validated tests and build
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * [later](https://github.com/microsoft/TypeScript-go/pull/4141#issuecomment-4621270410) **jakebailey** said "@copilot merge main"
 * [later](https://github.com/microsoft/TypeScript-go/pull/4141#issuecomment-4621380827) **Copilot** merged origin/main, resolved the tsconfig parsing test conflict while preserving both tests, and confirmed validation passed

### [PR microsoft/TypeScript-go#4143](https://github.com/microsoft/TypeScript-go/pull/4143) (Closed, **jakebailey**, **Copilot**)

**Prevent inline source maps in declaration map emit**

*Prevent inline source maps in declaration map emit to ensure .d.ts files link to external .d.ts.map files.*

 * created by **Copilot**
 * (3 days ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * [today](https://github.com/microsoft/TypeScript-go/pull/4143#issuecomment-4615760810) **jakebailey** said "@copilot+gpt-5.5  merge main"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4143#issuecomment-4615875758) **Copilot** merged origin/main into the branch and resolved the emitter conflict in commit 2e6ff05
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript-go#4144](https://github.com/microsoft/TypeScript-go/pull/4144) (Closed)

**fix\(checker\): align template literal inference with tsc UTF\-16 surrog…**

*Template literal inference now splits supplementary Unicode characters into UTF-16 surrogate pairs to match TypeScript’s behavior.*

 * created by **Utsav006**
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/4144#issuecomment-4589427919) **Utsav006** said "@microsoft-github-policy-service agree"
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * [later](https://github.com/microsoft/TypeScript-go/pull/4144#issuecomment-4621262744) **jakebailey** said "I'd rather take https://github.com/microsoft/typescript-go/pull/4181"
 * [later](https://github.com/microsoft/TypeScript-go/pull/4144#issuecomment-4622190110) **Utsav006** said ""Understood! Closing this in favour of #4181. Thanks for taking a look."
 * (later) **Utsav006** closed the issue

### [Issue microsoft/TypeScript-go#4145](https://github.com/microsoft/TypeScript-go/issues/4145) (Closed)

**strict\-family checks \(strictPropertyInitialization, useUnknownInCatchVariables\) incorrectly enabled when only strictNullChecks is set — regression in dev\.20260206\.1**

*tsgo dev.20260206.1 erroneously enables strictPropertyInitialization and useUnknownInCatchVariables when only strictNullChecks is set, resulting in false errors.*

 * created by **JerryPeace**
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/4145#issuecomment-4589740264) **jakebailey** advised checking against TS 6.0 instead of 5.9 and linked the announcement
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#4147](https://github.com/microsoft/TypeScript-go/issues/4147) (Closed, `Needs Investigation`, **andrewbranch**)

**tsgo \-b emits src/ subpath in declaration files where tsc \-b emits types/**

*tsgo -b emits declaration files referencing ./src/* subpaths instead of ./types/* like tsc, causing downstream type errors.*

 * created by **matyasf**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.0 RC`, and assigned to **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#4154](https://github.com/microsoft/TypeScript-go/pull/4154) (Closed, **jakebailey**, **Copilot**)

**Fix spurious TS2393 on function redeclaration in checked \.js files**

*Skip duplicate implementation checking for function redeclarations in JavaScript files in the Go TypeScript port to avoid erroneous TS2393 diagnostics.*

 * **Copilot** assigned to **jakebailey**
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/4154#issuecomment-4596406420) **jakebailey** said "@copilot+claude-opus-4.8 merge main into this PR"
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/4154#issuecomment-4596504613) **Copilot** merged origin/main into the branch, regenerated conflicting baselines, and confirmed build and tests passed
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4157](https://github.com/microsoft/TypeScript-go/pull/4157) (Open, **jakebailey**, **Copilot**)

**Use first @jsx/@jsxfrag pragma to match tsc behavior**

*Use the first @jsx/@jsxfrag pragma in tsgo to match tsc behavior and update utilities and tests accordingly.*

 * created by **Copilot**
 * (2 days ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * [today](https://github.com/microsoft/TypeScript-go/pull/4157#issuecomment-4617097621) **RyanCavanaugh** said "So jsximportsource and jsxruntime use the last pragma, but jsx and jsxfrag use the first? Why are they different?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4157#issuecomment-4617163543) **ahejlsberg** suggested consistently basing directives on the first occurrence and erroring on duplicates with no effect

### [PR microsoft/TypeScript-go#4159](https://github.com/microsoft/TypeScript-go/pull/4159) (Closed, **jakebailey**, **Copilot**)

**Fix swapped OutputsSkipped/OutputsGenerated exit codes**

*Swap tsgo exit code constants for OutputsSkipped and OutputsGenerated to align with tsc's exit statuses.*

 * created by **Copilot**
 * (2 days ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4161](https://github.com/microsoft/TypeScript-go/pull/4161) (Closed, **jakebailey**, **Copilot**)

**Fix panic in declaration emit for a set accessor with no parameters**

*Declaration emit panics for parameterless set accessors because of a malformed type annotation, now fixed by using NewKeywordTypeNode.*

 * created by **Copilot**
 * (2 days ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4162](https://github.com/microsoft/TypeScript-go/pull/4162) (Closed, **jakebailey**, **Copilot**)

**Fix panic in tryLoadInputFileForPath when an exports/imports target equals the declarationDir/outDir**

*Prevent panic by guarding path fragment slicing when exports or imports target equals the declarationDir or outDir*

 * created by **Copilot**
 * (2 days ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4163](https://github.com/microsoft/TypeScript-go/pull/4163) (Closed, **jakebailey**, **Copilot**)

**Fix panic on overlapping wildcard path patterns**

*Fix panic on overlapping wildcard patterns by requiring candidate length >= prefix+suffix and adding regression tests.*

 * **Copilot** assigned to **jakebailey**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4163#issuecomment-4606796387) **jakebailey** said "@copilot Fix your lint failures"
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4163#issuecomment-4606881201) **Copilot** mentioned fixing lint failures by adding t.Parallel() to TestPatternOverlappingMatch in internal/core/pattern_test.go and noting commit 2a206597
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4164](https://github.com/microsoft/TypeScript-go/pull/4164) (Closed, **jakebailey**, **Copilot**)

**Fix expando function in namespace emitting invalid nested \`declare namespace\`**

*Fix generation of invalid nested declare namespace for expando function properties inside ambient namespaces.*

 * created by **Copilot**
 * (2 days ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * [today](https://github.com/microsoft/TypeScript-go/pull/4164#issuecomment-4616258776) **weswigham** said "And I know I said it before, but: we could drop all declares in declaration files (and probably should, some day)"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4165](https://github.com/microsoft/TypeScript-go/pull/4165) (Closed, **jakebailey**, **Copilot**)

**Match TypeScript's per\-line pragma scanning for @jsx in multi\-line comments**

*Only consider the first @-token per line in multi-line comments when parsing pragmas, aligning with TypeScript.*

 * created by **Copilot**
 * (2 days ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4166](https://github.com/microsoft/TypeScript-go/pull/4166) (Closed, **jakebailey**, **Copilot**)

**Report TS2527 for inferred object\-literal types referencing \`this\` in declaration emit**

*Ensure TS2527 errors are reported for inferred object-literal types referencing this by updating pseudotypenodebuilder serialization flags.*

 * created by **Copilot**
 * (2 days ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * [today](https://github.com/microsoft/TypeScript-go/pull/4166#issuecomment-4616022439) **jakebailey** said "@copilot merge main"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4166#issuecomment-4616229676) **Copilot** merged main and updated the post-merge baseline; confirmed tests passed
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4167](https://github.com/microsoft/TypeScript-go/issues/4167) (Closed, **jakebailey**, **Copilot**)

**tsgo mis\-parses \`\.await\` member access as top\-level await in module\-scope JS with JSDoc \(spurious TS1146/TS1161\)**

*tsgo incorrectly interprets .await property access as top-level await in JSDoc-annotated module-scope JavaScript*

 * created by **turadg**
 * (2 days ago) **jakebailey** assigned to **Copilot**, **jakebailey**
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#4169](https://github.com/microsoft/TypeScript-go/pull/4169) (Closed, **jakebailey**, **Copilot**)

**Fix \`\.await\` member access mis\-parsed as top\-level await in JS modules with JSDoc**

*Fixes misinterpretation of `.await` member access in JS modules with JSDoc tags as top-level await.*

 * created by **Copilot**
 * (2 days ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#4171](https://github.com/microsoft/TypeScript-go/pull/4171) (Closed)

**Consolidate LSP logs into single output pane**

*Provide a unified VS Code output channel consolidating TypeScript-native-preview server logs and optional LSP traces with configurable levels.*

 * created by **andrewbranch**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4171#issuecomment-4606607552) **jakebailey** said "LGTM though there are conflicts and maybe @DanielRosenwasser should comment."
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#4172](https://github.com/microsoft/TypeScript-go/pull/4172) (Open)

**Fix redundant undefined wrapping in optional parameter declaration emit**

*Update declaration emission for optional parameters to avoid redundant '| undefined' wrapping when types already include undefined*

 * created by **danyalahmed1995**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [Issue microsoft/TypeScript-go#4180](https://github.com/microsoft/TypeScript-go/issues/4180) (Closed, `Crash`, **jakebailey**, **Copilot**)

**tsgo LSP crashes in WebStorm when opening \.mts file in mixed CJS/ESM repo**

*tsgo LSP panics on .mts files in CJS/ESM projects because the 'mts' languageId yields an unknown script kind without file extension fallback*

 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4180#issuecomment-4612608196) **jakebailey** said "mts isn't the right language ID at all; why is WebStorm sending it?"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4181](https://github.com/microsoft/TypeScript-go/pull/4181) (Open)

**Fix a slew of UTF\-8/UTF\-16 related issues**

*Adopt a WTF-8-inspired approach to fix multiple UTF-8/UTF-16 encoding issues while preserving raw byte storage of source files.*

 * created by **jakebailey**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * [today](https://github.com/microsoft/TypeScript-go/pull/4181#issuecomment-4618040141) **jakebailey** described challenges with UTF-16 surrogate normalization and ambiguity around template string types, and noted attempting fixes in the last push
 * [later](https://github.com/microsoft/TypeScript-go/pull/4181#issuecomment-4622169728) **Utsav006** mentioned a previous workaround for handling split UTF-16 surrogates using Go's utf16.EncodeRune to bypass the re-normalization trap during inference
 * [later](https://github.com/microsoft/TypeScript-go/pull/4181#issuecomment-4623423327) **jakebailey** said "I'll have to think about that, there's just more than just this one place..."

### [PR microsoft/TypeScript-go#4185](https://github.com/microsoft/TypeScript-go/pull/4185) (Closed)

**\[API\] use integer ids, look up node handles by visit\-order index in file**

*Use integer IDs and visit-order index lookups in the API to accelerate node handle resolution for batched calls*

 * created by **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#4186](https://github.com/microsoft/TypeScript-go/pull/4186) (Closed, **andrewbranch**, **Copilot**)

**Move experimental LSP capabilities to \`experimental\` object per spec**

*Move all non-VS experimental LSP client and server capabilities into the experimental field as per spec.*

 * **Copilot** assigned to **andrewbranch**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4186#issuecomment-4607734441) **andrewbranch** said "@copilot I can't believe I'm saying this but I'm not sure you need a test for this. I will validate in actual VS Code end to end."
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4186#issuecomment-4607752496) **Copilot** stated that they would validate in VS Code end-to-end and removed the test in commit 7f2e507
 * [today](https://github.com/microsoft/TypeScript-go/pull/4186#issuecomment-4614941639) **jakebailey** expressed uncertainty about the need to move capabilities into the experimental object, noting only two could be upstreamed into LSP
 * [today](https://github.com/microsoft/TypeScript-go/pull/4186#issuecomment-4615209899) **andrewbranch** used Copilot to implement the change without personal preference and noted it’s preferable to deviate from the spec only when necessary
 * [today](https://github.com/microsoft/TypeScript-go/pull/4186#issuecomment-4615628742) **jakebailey** suggested moving the hover verbosity cap to experimental
 * [today](https://github.com/microsoft/TypeScript-go/pull/4186#issuecomment-4615790631) **andrewbranch** said "@copilot implement Jake's suggestion"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4186#issuecomment-4615873250) **Copilot** implemented Jake's suggestion by updating hover verbosity capability paths in client and server
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#4187](https://github.com/microsoft/TypeScript-go/issues/4187) (Closed, `Crash`)

**panic handling request textDocument/definition**

*A panic occurs in the TypeScript-Go language server when handling a textDocument/definition request due to a missing decorator signature.*

 * created by **Withered-Flower-0422**
 * **Withered-Flower-0422** added label `Crash`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4189](https://github.com/microsoft/TypeScript-go/pull/4189) (Closed, **jakebailey**, **Copilot**)

**Fix overlay script kind fallback for unknown LSP language IDs**

*Update overlay script kind resolution to fall back on file extension for unknown LSP language IDs (e.g., .mts) to prevent crashes.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4189#issuecomment-4615020133) **jakebailey** said "I'm not 100% thrilled that we would need to do this to appease a client, but, it's not the worst thought."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4190](https://github.com/microsoft/TypeScript-go/pull/4190) (Closed)

**fix\(4187\): avoid decorator signature panic on invalid targets**

*Avoid panics by validating decorator targets before signature processing for invalid decorator applications.*

 * created by **a-tarasyuk**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * [today](https://github.com/microsoft/TypeScript-go/pull/4190#issuecomment-4616534724) **a-tarasyuk** confirmed that the same issue existed in the old ts codebase
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4191](https://github.com/microsoft/TypeScript-go/pull/4191) (Closed)

**Fix infinite recursion caused by CFA in loop with destructuring**

*Exclude binding elements from computed property name extraction to prevent infinite recursion in control flow analysis loops with destructuring.*

 * created by **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4191#issuecomment-4614175653) **jakebailey** questioned using the phrase 'This PR fixes microsoft/TypeScript#63192' and suggested opening a Strada PR to properly close the issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/4191#issuecomment-4614819262) **ahejlsberg** noted that they preferred not to use that phrase and that future fixes will be implemented only in the new code base, and asked for suggestions for alternative terminology
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * [today](https://github.com/microsoft/TypeScript-go/pull/4191#issuecomment-4614982946) **jakebailey** said "I meant from the perspective that the phrase will actually close the issue. If we're saying we are not going to backport this to 6.0, then so be it"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4191#issuecomment-4615250669) **RyanCavanaugh** said "We're already routinely closing bugs in the other repo if they've been fixed in 7.0. I don't see a contradiction"
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#4192](https://github.com/microsoft/TypeScript-go/pull/4192) (Closed)

**Stop parsing constructs that make it impossible to erase \`as\`/\`satisfies\`**

*Stop parsing constructs that make it impossible to remove as and satisfies assertions.*

 * created by **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4192#issuecomment-4616145011) **jakebailey** said "Are we waiting on this to run top800 or to do this in Strada to run top800, once that pipeline is reenabled?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4192#issuecomment-4616975125) **ahejlsberg** said "@typescript-bot test this"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4192#issuecomment-4616975573) **typescript-bot** posted CI job status update showing a failed 'test top400' job and a started 'perf test this faster' job
 * [today](https://github.com/microsoft/TypeScript-go/pull/4192#issuecomment-4616984261) **ahejlsberg** asked whether to wait for the Strada pipeline or run top800 on this code base and expressed a strong preference for the latter
 * [today](https://github.com/microsoft/TypeScript-go/pull/4192#issuecomment-4617118053) **typescript-bot** provided the requested performance run results
 * [today](https://github.com/microsoft/TypeScript-go/pull/4192#issuecomment-4617294439) **jakebailey** said "Looks like vscode has one of these somewhere."
 * [today](https://github.com/microsoft/TypeScript-go/pull/4192#issuecomment-4617401909) **ahejlsberg** explained that the parser needs to be more conservative and permit 'as' and 'satisfies' before higher-precedence operators only when no other operators are consumed, with examples
 * [today](https://github.com/microsoft/TypeScript-go/pull/4192#issuecomment-4618071142) **ahejlsberg** said "@typescript-bot test this"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4192#issuecomment-4618071444) **typescript-bot** reported CI job statuses: one failure due to a disabled pipeline and one started build job
 * [today](https://github.com/microsoft/TypeScript-go/pull/4192#issuecomment-4618175338) **typescript-bot** posted the performance run results as requested

### [PR microsoft/TypeScript-go#4193](https://github.com/microsoft/TypeScript-go/pull/4193) (Closed)

**Fix backwards sort order for redirects in getAllModulePaths**

*Properly sort redirect paths in getAllModulePaths by fixing the boolean comparison order.*

 * created by **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#4194](https://github.com/microsoft/TypeScript-go/pull/4194) (Closed)

**Fix nil CommandLine crash**

*Add proper nil handling to avoid application crashes when CommandLine is nil*

 * created by **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#4195](https://github.com/microsoft/TypeScript-go/pull/4195) (Open)

**Allow LSP server to use builtin watcher**

*Allow LSP servers to use the editor's built-in file watcher.*

 * created by **andrewbranch**

