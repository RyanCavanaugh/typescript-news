# Report for 2026-06-30 (Tuesday, June 30th, 2026)

13 different users commented on 45 different issues.

## Recommended Actions

 * Response Recommended
    * @typescript-automation[bot] provided the requested perf run results in [microsoft/TypeScript-go#3369](https://github.com/microsoft/TypeScript-go/pull/3369#issuecomment-4847820197)
    * @mrazauskas asked if a type.isMissingType method could be added to support removeMissingType implementation in user code in [microsoft/TypeScript-go#4081](https://github.com/microsoft/TypeScript-go/issues/4081#issuecomment-4850717408)
    * @hkleungai asked to reopen the issue for better compatibility in [microsoft/TypeScript-go#4205](https://github.com/microsoft/TypeScript-go/issues/4205#issuecomment-4849976772)
    * @typescript-automation[bot] provided performance run results as requested in [microsoft/TypeScript-go#4313](https://github.com/microsoft/TypeScript-go/pull/4313#issuecomment-4848601089)

## Activity Summary

### [Issue microsoft/TypeScript-go#2851](https://github.com/microsoft/TypeScript-go/issues/2851) (Closed, **andrewbranch**)

**Add \`\.getTrueType\(\)\` and \`\.getFalseType\(\)\` to \`ConditionalType\`**

*Add getTrueType() and getFalseType() methods to ConditionalType so it returns instantiated true and false branch types.*

 * created by **mrazauskas**
 * **jakebailey** assigned to **andrewbranch**
 * **RyanCavanaugh** added to milestone `Post-7.0`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2851#issuecomment-4850504999) **mrazauskas** noted that it got added in #4431
 * (today) **mrazauskas** closed the issue

### [PR microsoft/TypeScript-go#3369](https://github.com/microsoft/TypeScript-go/pull/3369) (Open, `No linked issue`)

**Limit loader/emitter to GOMAXPROCS**

*Limit parsing and emitting workloads to a GOMAXPROCS-sized goroutine pool to prevent unbounded concurrency and stack growth.*

 * (9 weeks ago) **jakebailey** reopened the issue
 * (7 weeks ago) **RyanCavanaugh** added label `No linked issue`, and set milestone to `Possible Improvement`
 * [today](https://github.com/microsoft/TypeScript-go/pull/3369#issuecomment-4847634269) **jakebailey** said "@typescript-bot perf test this"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3369#issuecomment-4847634796) **typescript-automation[bot]** reported that performance test jobs started and provided links to build status and results
 * [today](https://github.com/microsoft/TypeScript-go/pull/3369#issuecomment-4847820197) **typescript-automation[bot]** provided the perf run results as requested

### [Issue microsoft/TypeScript-go#3475](https://github.com/microsoft/TypeScript-go/issues/3475) (Closed, `possible improvement`)

**Test harness doesn't report errors from unrecognized compiler options**

*The test harness fails to report errors for unrecognized compiler options, resulting in empty error outputs.*

 * **RyanCavanaugh** added to milestone `Post-7.0`
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/3475#issuecomment-4685804721) **iisaduan** described that tsconfig parsing errors weren't reported by the testing harness and suggested future changes to report them
 * **iisaduan** added label `possible improvement`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3518](https://github.com/microsoft/TypeScript-go/pull/3518) (Closed)

**fix\(native\-preview\): preserve lone surrogate string literals**

*Preserve lone UTF-16 surrogate literals in native-preview by adding WTF-8 decoding for binary AST while retaining UTF-8 fallback*

 * **RyanCavanaugh** added to milestone `Possible Improvement`
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3518#issuecomment-4837029679) **jakebailey** asked for confirmation that only the text decoder changed, suggested no version bump, and requested a performance comparison
 * [today](https://github.com/microsoft/TypeScript-go/pull/3518#issuecomment-4843209284) **TorinAsakura** confirmed reading correctly, removed the protocol version bump, added a fast path for native TextDecoder, provided microbenchmarks comparing native and WTF-8 decoders, and concluded the change is a client-side bugfix without a protocol change
 * [today](https://github.com/microsoft/TypeScript-go/pull/3518#issuecomment-4845911771) **jakebailey** asked @andrewbranch if he had concerns about splitting the file on certain characters and concatenating, noting that binary data was already sent as non-text
 * [today](https://github.com/microsoft/TypeScript-go/pull/3518#issuecomment-4846442160) **andrewbranch** said "This looks right to me, but Copilot points out that 0xED is also common in Korean Hangul syllables without being a surrogate, so suggests looking for the second byte before taking the slow path 😄 "
 * [today](https://github.com/microsoft/TypeScript-go/pull/3518#issuecomment-4846871285) **jakebailey** said "We already use surrogateUTF8Lead in Go to see if we need to decode. If that's the case then we have a wider problem and should probably fix it in both places? Maybe not in this PR unless it's easy"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3518#issuecomment-4847056807) **andrewbranch** said "I think it would be as easy as checking the range of the byte after surrogateUTF8Lead when it's present, but it's not a blocker for me."
 * [today](https://github.com/microsoft/TypeScript-go/pull/3518#issuecomment-4847069066) **jakebailey** said "Yes, later would be good, both at the same time"
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3549](https://github.com/microsoft/TypeScript-go/issues/3549) (Closed, `Domain: Declaration Emit`, `Needs Investigation`, **weswigham**)

**Baselines: Missing generic type arguments no longer auto\-filled with any \(produces TS2314 errors\)**

*Generic types without explicit parameters now emit bare types instead of defaulting to any, causing TS2314 errors*

 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/3549#issuecomment-4814275769) **jakebailey** said "I don't think this is fixed. The one file mentioned above was not deleted by #3745."
 * (4 days ago) **jakebailey** reopened the issue
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/3549#issuecomment-4815105764) **hkleungai** said "Does it mean https://github.com/microsoft/typescript-go/issues/4204 will eventually still be addressed as well?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/3549#issuecomment-4847630628) **weswigham** explained that with noImplicitAny false there's no error on Promise in jsdoc emitting Promise<any> as per PR 4492, whereas with noImplicitAny true there's an error on Promise as expected
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript-go#3881](https://github.com/microsoft/TypeScript-go/pull/3881) (Open)

**Expose ImportAdder to IPC API**

*Expose ImportAdder via the IPC API to allow external processes to add imports programmatically.*

 * created by **andrewbranch**
 * **andrewbranch** added to milestone `Post-7.0`

### [Issue microsoft/TypeScript-go#4081](https://github.com/microsoft/TypeScript-go/issues/4081) (Open, `Domain: API and Extensibility`, **andrewbranch**)

**Add API to get symbol type that respects the \`exactOptionalPropertyTypes\` option**

*Propose enhancing TypeScript’s symbol type retrieval API to honor exactOptionalPropertyTypes for both object and mapped types.*

 * created by **mrazauskas**
 * **RyanCavanaugh** added to milestone `Post-7.0`
 * [today](https://github.com/microsoft/TypeScript-go/issues/4081#issuecomment-4850717408) **mrazauskas** asked if a type.isMissingType method could be added to support removeMissingType implementation in user code
 * (later) **andrewbranch** added label `Domain: API and Extensibility`, and assigned to **andrewbranch**

### [Issue microsoft/TypeScript-go#4205](https://github.com/microsoft/TypeScript-go/issues/4205) (Closed, `wontfix`)

**Behavior difference: For \`@param {\.\.\.} \[outer\.inner\]\`, tsc emits \`inner?: \.\.\. \| undefined\`, but tsgo emits \`inner?: \.\.\.;\`**

*A discrepancy where tsgo generates `inner?: string;` instead of `inner?: string | undefined;` for optional nested JSDoc parameters.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/4205#issuecomment-4633207969) **RyanCavanaugh** said "tsgo behavior looks better to me; this is fine."
 * (3 weeks ago) **RyanCavanaugh** closed the issue
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/4205#issuecomment-4634944783) **hkleungai** requested consistent `| undefined` emission in tsgo to avoid consumer issues with exactOptionalPropertyTypes
 * [today](https://github.com/microsoft/TypeScript-go/issues/4205#issuecomment-4849976772) **hkleungai** said "Hello @RyanCavanaugh @andrewbranch , please consider reopen this issue, for the sake of better compatibility, like https://github.com/microsoft/typescript-go/pull/4497 does. 🫡 "

### [Issue microsoft/TypeScript-go#4216](https://github.com/microsoft/TypeScript-go/issues/4216) (Closed, `Domain: API and Extensibility`)

**\`Node\` is missing \`getFullStart\(\)\`, \`getStart\(\)\` and other getters**

*Add missing getters (getFullStart, getStart, getFullWidth, getWidth, getLeadingTriviaWidth, getFullText, getText) to Node to improve API usability.*

 * (3 weeks ago) **RyanCavanaugh** added label `Domain: API and Extensibility`, and set milestone to `Post-7.0`
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/4216#issuecomment-4697657824) **oMatheusmol** implemented position and text getters on both node types and deferred child/token getters for a follow-up
 * [today](https://github.com/microsoft/TypeScript-go/issues/4216#issuecomment-4845699422) **mrazauskas** said "Got added in https://github.com/microsoft/typescript-go/pull/4308"
 * (today) **mrazauskas** closed the issue

### [PR microsoft/TypeScript-go#4313](https://github.com/microsoft/TypeScript-go/pull/4313) (Open)

**Assign checkers with cost/import\-aware algorithm**

*Use longest-processing-time scheduling combined with bounded import-graph refinement to assign files to checkers, reducing memory usage and improving type-checking performance.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4313#issuecomment-4838562747) **jakebailey** said "@typescript-bot perf test this faster"
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4313#issuecomment-4838563652) **typescript-automation[bot]** started perf test jobs and provided status and results links
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4313#issuecomment-4838688100) **typescript-automation[bot]** posted the requested perf run results with tsc comparison metrics
 * [today](https://github.com/microsoft/TypeScript-go/pull/4313#issuecomment-4845973114) **jakebailey** confirmed the result was expected and asked if the PR was explained enough
 * [today](https://github.com/microsoft/TypeScript-go/pull/4313#issuecomment-4846407122) **ahejlsberg** said "I like the improvements, even if it mostly seems to be around memory consumption. I'm surprised the initial compile time improvement for VS Code evaporated. Any idea why?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4313#issuecomment-4848161412) **jakebailey** said "It was my last change; the weird count stuff is apparently load bearing in vscode. I'm going to have to think about a more principled way to weight files..."
 * [today](https://github.com/microsoft/TypeScript-go/pull/4313#issuecomment-4848472829) **jakebailey** described a two-phase algorithm for work-balanced assignment and import-graph locality refinement using longest-processing-time scheduling and graph-based moves under a load cap
 * [today](https://github.com/microsoft/TypeScript-go/pull/4313#issuecomment-4848474610) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4313#issuecomment-4848474935) **typescript-automation[bot]** reported the start of performance test jobs and provided status and results links
 * [today](https://github.com/microsoft/TypeScript-go/pull/4313#issuecomment-4848601089) **typescript-automation[bot]** reported the performance run results including comparisons for errors, symbols, types, and memory usage
 * [today](https://github.com/microsoft/TypeScript-go/pull/4313#issuecomment-4848626121) **jakebailey** said "Uh oh, xstate has some checker association dependence."

### [PR microsoft/TypeScript-go#4346](https://github.com/microsoft/TypeScript-go/pull/4346) (Closed, **andrewbranch**, **Copilot**)

**Fix RemoteNodeList inherited array methods throwing \`this\.view\.getUint32 is not a function\`**

*Define Symbol.species on RemoteNodeList to return plain Array so inherited filter, map, and slice methods avoid view.getUint32 errors.*

 * created by **Copilot**
 * (2 weeks ago) **Copilot** assigned to **Copilot**, **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#4380](https://github.com/microsoft/TypeScript-go/issues/4380) (Closed, `Needs Investigation`, **johnfav03**)

**\[ServerErrors\]\[TypeScript\] main vs **

*Server errors occurred in the TypeScript main branch pipeline while analyzing 300 popular GitHub repositories, causing timeouts and other failures.*

 * (6 days ago) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `Post-7.0`, and assigned to **johnfav03**
 * (today) **johnfav03** closed the issue

### [Issue microsoft/TypeScript-go#4388](https://github.com/microsoft/TypeScript-go/issues/4388) (Closed, `bug`)

**Parameters not automatically filled for JSdoc comments**

*JSDoc comment skeletons generated by tsgo omit @param tags, unlike the default TypeScript 6.0 behavior.*

 * (1 week ago) **RyanCavanaugh** added label `bug`, and set milestone to `Post-7.0`
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/4388#issuecomment-4786221145) **crystalfp** reported that VS Code displayed a warning stating Vue.volar plugins would not load because TypeScript Native Preview was enabled globally and suggested this might explain the behavior change
 * [today](https://github.com/microsoft/TypeScript-go/issues/4388#issuecomment-4849992184) **jakebailey** stated that VS Code's TS extension disabled JSDoc snippets and concluded that they needed to port it over

### [Issue microsoft/TypeScript-go#4405](https://github.com/microsoft/TypeScript-go/issues/4405) (Closed, `Needs Investigation`, **andrewbranch**)

**App using programmatic APIs fails to typecheck with \`exactOptionalPropertyTypes: true\` and \`@types/node\` v24**

*With exactOptionalPropertyTypes enabled and @types/node v24 installed, programmatic API imports fail to compile due to type incompatibilities.*

 * (6 days ago) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `Post-7.0`, and assigned to **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#4443](https://github.com/microsoft/TypeScript-go/pull/4443) (Open)

**Fixed build mode false negative from export\-star facade**

*Fix false negative TypeScript build-mode error caused by export-star facade usage.*

 * created by **johnfav03**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4443#issuecomment-4836710462) **jakebailey** noted that the proposal seemed reasonable but contained a lot of text for the key and requested a vibe check from @andrewbranch
 * [today](https://github.com/microsoft/TypeScript-go/pull/4443#issuecomment-4847066127) **andrewbranch** said "This should be marked for post-7.0, right?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4443#issuecomment-4847080467) **johnfav03** agreed that marking the issue for post-7.0 was appropriate because it also existed in 6.0 and wasn't time-critical
 * [today](https://github.com/microsoft/TypeScript-go/pull/4443#issuecomment-4847081152) **jakebailey** acknowledged the referenced issue and clarified that they had thought it was a new bug
 * **johnfav03** added to milestone `Post-7.0`

### [PR microsoft/TypeScript-go#4458](https://github.com/microsoft/TypeScript-go/pull/4458) (Open)

**Vendor dprint plugins**

*Vendor copies of dprint plugins in the repository and add a script to update them, avoiding firewall fetch issues.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4458#issuecomment-4848601346) **jakebailey** said "dprint is getting "plugins via node_modules" so I'll hold off."

### [PR microsoft/TypeScript-go#4460](https://github.com/microsoft/TypeScript-go/pull/4460) (Closed)

**Clean up completed submoduleTriaged items**

*Clean up the submoduleTriaged tracker by removing items marked as completed.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4469](https://github.com/microsoft/TypeScript-go/issues/4469) (Closed)

**const enum in ambient declare namespace causes import alias to be incorrectly elided in emitted JS**

*Declaring a const enum in an ambient namespace causes an import alias to be omitted from emitted JavaScript.*

 * created by **vborioni-onit**
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/4469#issuecomment-4836985207) **jakebailey** said "Can you make a repo for this instead of uploading a zip to OneDrive? Hard to trust an arbitrary download and zip file 😄 "
 * [today](https://github.com/microsoft/TypeScript-go/issues/4469#issuecomment-4841327866) **vborioni-onit** shared a link to the reproduction repository on GitHub
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4471](https://github.com/microsoft/TypeScript-go/pull/4471) (Closed)

**Reduce code size of lsproto package, use JSON roundtripping in fourslash**

*Reduce lsproto binary size by 580KB by deferring type decoding, employing JSON roundtrips in fourslash, and using reflection-based unmarshalling.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4478](https://github.com/microsoft/TypeScript-go/issues/4478) (Closed, **DanielRosenwasser**, **Copilot**)

**Crash from nil Contents of package\.json resolved through peerDependencies**

*The Go module resolver panics when attempting to read peerDependencies from a nil package.json.*

 * created by **DanielRosenwasser**
 * (yesterday) **DanielRosenwasser** assigned to **Copilot**, **DanielRosenwasser**
 * (today) **jakebailey** closed the issue
 * **DanielRosenwasser** added to milestone `TypeScript 7.0 Stable`

### [PR microsoft/TypeScript-go#4479](https://github.com/microsoft/TypeScript-go/pull/4479) (Closed, **DanielRosenwasser**, **Copilot**)

**Avoid nil package\.json crash when resolving peer dependencies**

*The resolver now treats nil-content peer dependency package.json entries as missing metadata to prevent panics during resolution.*

 * created by **Copilot**
 * (yesterday) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4480](https://github.com/microsoft/TypeScript-go/pull/4480) (Closed)

**Run symbol\-returning completion on the API checker**

*Use CheckerLifetimeAPI in handleGetCompletionsAtPosition to ensure consistent symbol resolution, avoid nil-pointer panics, and add documentation and a regression test.*

 * created by **Vorobey31415**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4480#issuecomment-4841415885) **Vorobey31415** said "@microsoft-github-policy-service agree company="JetBrains""
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#4482](https://github.com/microsoft/TypeScript-go/pull/4482) (Open, **DanielRosenwasser**, **Copilot**)

**Fix auto\-imports crash in GetSourceOfProjectReferenceIfOutputIncluded**

*Prevent aliasResolver panics in GetSourceOfProjectReferenceIfOutputIncluded by returning file.FileName() and adding a regression test*

 * created by **Copilot**
 * (yesterday) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4482#issuecomment-4845950612) **jakebailey** said "This seems pretty believable."
 * [today](https://github.com/microsoft/TypeScript-go/pull/4482#issuecomment-4846312221) **DanielRosenwasser** said "@copilot+gpt-5.5 the test didn't fail locally without the fix, so I think you are lying about having found a repro."
 * [today](https://github.com/microsoft/TypeScript-go/pull/4482#issuecomment-4846497464) **Copilot** acknowledged the repro issue, replaced the test in ca8f0490 to force node builder module specifier generation, and verified that it failed when GetSourceOfProjectReferenceIfOutputIncluded was unimplemented
 * [today](https://github.com/microsoft/TypeScript-go/pull/4482#issuecomment-4847110711) **DanielRosenwasser** said "@copilot+gpt-5.5 you changed a bunch of different functions - do we have tests that actually trigger the panics that they issue?"

### [Issue microsoft/TypeScript-go#4484](https://github.com/microsoft/TypeScript-go/issues/4484) (Open)

**project reference { "path": "" } is ignored**

*tsgo build ignores project references with an empty path (""), while tsc correctly includes them unless changed to "./".*

 * created by **HolgerJeromin**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4484#issuecomment-4845719290) **jakebailey** suggested not silently ignoring an empty string and instead erroring or using "." or "./"
 * [today](https://github.com/microsoft/TypeScript-go/issues/4484#issuecomment-4850821788) **HolgerJeromin** agreed with the suggestion and noted that fixing is quick and poses no problem

### [PR microsoft/TypeScript-go#4485](https://github.com/microsoft/TypeScript-go/pull/4485) (Closed, **jakebailey**, **Copilot**)

**Fix const enum elision on merged symbols**

*Fix const enum elision for merged symbols to ensure proper code generation*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4485#issuecomment-4845728563) **jakebailey** said "@copilot+claude-opus-4.8 retitle and re-describe this PR"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4486](https://github.com/microsoft/TypeScript-go/pull/4486) (Closed)

**Use workspace/diagnostics for global diagnostics**

*Using workspace/diagnostics to work around VS Code diagnostic naming problems triggers repeated diagnostic request loops.*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#4487](https://github.com/microsoft/TypeScript-go/pull/4487) (Closed)

**Rename LSP push diag collection**

*Rename the LSP push diagnostic collection to avoid conflicts with the pull diagnostic collection.*

 * created by **jakebailey**
 * (later) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4488](https://github.com/microsoft/TypeScript-go/pull/4488) (Closed)

**Fix project\-reference redirect bug for symlinked subpaths**

*Correct project-reference redirects for symlinked subpaths to prevent misrouting.*

 * created by **johnfav03**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4488#issuecomment-4847479452) **jakebailey** said "Something is wrong with this PR, it is hanging in CI in the new code. "

### [PR microsoft/TypeScript-go#4489](https://github.com/microsoft/TypeScript-go/pull/4489) (Open)

**New extension layout**

*Redesigns the TypeScript extension into vscode-typescript 7 and a native-preview nightly extension with updated installation, settings, and packaging.*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#4490](https://github.com/microsoft/TypeScript-go/pull/4490) (Closed)

**Fixed formatting for dotted tag names**

*Adjust formatting logic to correctly handle dotted tag names in generated code*

 * created by **johnfav03**
 * (today) **johnfav03** closed the issue

### [PR microsoft/TypeScript-go#4491](https://github.com/microsoft/TypeScript-go/pull/4491) (Closed)

**Fix fswatch on windows**

*Implement support and resolve issues enabling the fswatch file monitoring utility to function correctly on Windows.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4492](https://github.com/microsoft/TypeScript-go/pull/4492) (Closed)

**Fix jsdoc type reference reuse check TODO to use new corsa jsdoc node remapping logic**

*Use new Corsa JSDoc node remapping logic for type reference reuse checks while retaining existing compatibility checks.*

 * created by **weswigham**
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript-go#4493](https://github.com/microsoft/TypeScript-go/pull/4493) (Closed)

**\[api\] Batch of improvements, fixes, and additions**

*Batch API improvements including optional constructor, enhanced symbol and type methods, metadata retrieval, and bug fixes.*

 * created by **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4493#issuecomment-4848299474) **jakebailey** said "LGTM but I'm not the one touching the client code downstream 😄 "
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#4494](https://github.com/microsoft/TypeScript-go/pull/4494) (Open)

**fix\(tsoptions\): validate project reference fields**

*Validate project reference path and circular options in tsconfig and report diagnostics for invalid or missing values.*

 * created by **TorinAsakura**

### [PR microsoft/TypeScript-go#4495](https://github.com/microsoft/TypeScript-go/pull/4495) (Closed)

**Fix fswatch coalescing**

*Fix fswatch event coalescing under heavy load, resolving macOS and Windows errors and temporarily disabling coalescing on Windows.*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#4496](https://github.com/microsoft/TypeScript-go/pull/4496) (Open)

**fix\(lsp\): support TypeScript source action kinds**

*Add support for TypeScript-specific .ts-suffixed source action kinds alongside existing generic kinds for compatibility.*

 * created by **TorinAsakura**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4496#issuecomment-4848080613) **jakebailey** suggested looking at the vscode repo's typescript-language-features extension and questioned whether implementing the feature was critical since old extensions could not do it
 * [today](https://github.com/microsoft/TypeScript-go/pull/4496#issuecomment-4848251335) **TorinAsakura** rechecked vscode and explained that the PR targets multi-server LSP scenarios rather than matching the current extension and wires actual handling to support generic source.removeUnusedImports as an escape hatch for clients

### [PR microsoft/TypeScript-go#4497](https://github.com/microsoft/TypeScript-go/pull/4497) (Closed)

**\[api\] Fix compatibility with older @types/node and exactOptionalPropertyTypes**

*Fix API compatibility with older @types/node versions and projects using TypeScript’s exactOptionalPropertyTypes option.*

 * created by **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#4498](https://github.com/microsoft/TypeScript-go/pull/4498) (Closed)

**\[api\] Fix generated \.text type for JSDocText**

*Treat JSDocText .text property as a single string in TS AST generation instead of string array.*

 * created by **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#4499](https://github.com/microsoft/TypeScript-go/issues/4499) (Open)

**Add \`TupleTypeReference\` interface to the API**

*Introduce a TupleTypeReference interface in the API to facilitate typed handling of tuple types with Checker#isTupleType.*

 * created by **mrazauskas**

### [Issue microsoft/TypeScript-go#4500](https://github.com/microsoft/TypeScript-go/issues/4500) (Closed, `Porting PR`)

**Port TypeScript PR \#\[NNNNN\]**

*Port changes from microsoft/TypeScript PR #[NNNNN] into this Go implementation, translating edits or explaining if not applicable.*

 * created by **fisallllll280-code**
 * **fisallllll280-code** added label `Porting PR`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4501](https://github.com/microsoft/TypeScript-go/issues/4501) (Closed, `Porting PR`)

**Port TypeScript PR \#\[NNNNN\]**

*Port changes from microsoft/TypeScript PR #[NNNNN] into this Go implementation, translating edits or explaining if not applicable.*

 * created by **fisallllll280-code**
 * **fisallllll280-code** added label `Porting PR`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4502](https://github.com/microsoft/TypeScript-go/issues/4502) (Open)

**\`Program\` is missing \`\.getSourceFiles\(\)\` getter**

*Add a getSourceFiles() getter to Program to return all SourceFile instances and ease filtering.*

 * created by **mrazauskas**

### [Issue microsoft/TypeScript-go#4503](https://github.com/microsoft/TypeScript-go/issues/4503) (Open)

**Add APIs that set the compiler options programatically**

*Provide an API to programmatically set or update compiler options for inferred and configured projects.*

 * created by **mrazauskas**

