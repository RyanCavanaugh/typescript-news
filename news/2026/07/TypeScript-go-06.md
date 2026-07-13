# Report for 2026-07-06 (Monday, July 6th, 2026)

13 different users commented on 48 different issues.

## Recommended Actions

 * Response Recommended
    * @proyectoramirez asked for instructions on testing the PR in a yarn project in [microsoft/TypeScript-go#1966](https://github.com/microsoft/TypeScript-go/pull/1966#issuecomment-4905614254)
    * @acutmore reported that the fix was in #4549 in [microsoft/TypeScript-go#4548](https://github.com/microsoft/TypeScript-go/issues/4548#issuecomment-4901398372)
    * @acutmore confirmed that the patch fixes the benchmark case in #4548 in [microsoft/TypeScript-go#4549](https://github.com/microsoft/TypeScript-go/pull/4549#issuecomment-4901474940)

## Activity Summary

### [PR microsoft/TypeScript-go#1966](https://github.com/microsoft/TypeScript-go/pull/1966) (Open, `No linked issue`)

**Add Yarn PnP support**

*Add native Yarn Plug'n'Play support to TypeScript Go with VFS integration and manifest handling following PnP specification.*

 * **RyanCavanaugh** added label `No linked issue`
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1966#issuecomment-4707217638) **GGomez99** provided the full link to the linked issue and asked if it should be linked differently
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1966#issuecomment-4709751672) **SerenModz21** suggested adding "Closes #460" to the PR description to properly link the issue and provided a documentation link
 * [later](https://github.com/microsoft/TypeScript-go/pull/1966#issuecomment-4905614254) **proyectoramirez** said "What is a good way to try this PR in a yarn project?"

### [PR microsoft/TypeScript-go#3252](https://github.com/microsoft/TypeScript-go/pull/3252) (Closed, **DanielRosenwasser**, **Copilot**)

**Fix signature help assertion failure by marking all DeepCloneReparse descendants as reparsed**

*Mark all DeepCloneReparse descendants as reparsed to prevent signature help assertion failures from JSDoc-derived node positions.*

 * (14 weeks ago) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * [13 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3252#issuecomment-4164496027) **DanielRosenwasser** said "I actually can't repro the crash with the test case here."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3706](https://github.com/microsoft/TypeScript-go/pull/3706) (Closed, **DanielRosenwasser**, **Copilot**)

**Fix JSDoc @param qualified name error: produce TS2749 instead of TS2503**

*Implement two-step JSDoc qualified name resolution in JS files to produce TS2749 instead of TS2503 errors.*

 * (9 weeks ago) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * [9 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3706#issuecomment-4375172726) **Copilot** clarified that the PR only changed the error message from TS2503 to TS2749 and did not resolve obj.foo as typeof obj.foo in type position
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3722](https://github.com/microsoft/TypeScript-go/issues/3722) (Closed, `Domain: Editor`, **jakebailey**, **Copilot**)

**custom tsgo path is now ignored**

*VS Code's TypeScript native-preview ignores the configured custom tsgo path and launches its bundled tsgo instead.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/3722#issuecomment-4709558358) **jakebailey** said "We are currently moving everything around in prep for a release; it wouldn't be helpful to get a PR for this outside the team, no."
 * (2 weeks ago) **jakebailey** set milestone to `TypeScript 7.0 Stable`, and removed from milestone `TypeScript 7.0 RC`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3727](https://github.com/microsoft/TypeScript-go/issues/3727) (Closed, `Domain: Editor`, `possible improvement`, **jakebailey**)

**Unify tsdk between built\-in and native preview extensions**

*Share the built-in tsdk setting with the native preview and choose the TypeScript server based on useTsGo and tsdk directory.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/3727#issuecomment-4674445561) **andrewbranch** proposed a flowchart outlining the priority of settings in deciding between Corsa and Strada and the TypeScript SDK
 * (2 weeks ago) **jakebailey** set milestone to `TypeScript 7.0 Stable`, and removed from milestone `TypeScript 7.0 RC`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3733](https://github.com/microsoft/TypeScript-go/issues/3733) (Closed, `Domain: Editor`, `Needs More Info`)

**No autocomplete for local symbols and some global types when creating a new file**

*VS Code fails to autocomplete or auto-import local symbols and ESNext types like Temporal in new TypeScript files until restart.*

 * **RyanCavanaugh** added to milestone `Post-7.0`
 * [7 weeks ago](https://github.com/microsoft/TypeScript-go/issues/3733#issuecomment-4481422378) **RyanCavanaugh** asked which aspect (12,000 files, monorepo, tsconfig, etc.) was causing the issue
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/3733#issuecomment-4877704092) **jansedlon** said "@RyanCavanaugh Sorry it took me so long to get back to it. PR here #4529 "
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3942](https://github.com/microsoft/TypeScript-go/issues/3942) (Closed, `Domain: Editor`, `Crash`, **andrewbranch**)

**Fatal server crash at \`markProjectsAffectedByConfigChanges\`**

*Server crashes in markProjectsAffectedByConfigChanges when updating project snapshots after configuration changes.*

 * (6 weeks ago) **RyanCavanaugh** set milestone to `Post-7.0`, and assigned to **Copilot**, **RyanCavanaugh**
 * (today) **andrewbranch** closed the issue
 * (today) **andrewbranch** assigned to **andrewbranch**, and unassigned **RyanCavanaugh**, **Copilot**

### [PR microsoft/TypeScript-go#3987](https://github.com/microsoft/TypeScript-go/pull/3987) (Closed, **RyanCavanaugh**, **Copilot**)

**Avoid fatal panic on stale config\-retainer project paths in project rebuild flow**

*Prevent panic in markProjectsAffectedByConfigChanges by skipping stale project paths and add a regression test to verify safe handling.*

 * (6 weeks ago) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * **RyanCavanaugh** added to milestone `Post-7.0`
 * [today](https://github.com/microsoft/TypeScript-go/pull/3987#issuecomment-4898266145) **andrewbranch** said "Fixed by #4546"
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#4017](https://github.com/microsoft/TypeScript-go/issues/4017) (Closed, `Domain: Editor`, `possible improvement`)

**Extension does not respect \`js/ts\.locale\`**

*The extension ignores js/ts.locale settings and always displays English error messages because it does not send locale to the server.*

 * (6 weeks ago) **DanielRosenwasser** set milestone to `Possible Improvement`, and unassigned **iisaduan**
 * [6 weeks ago](https://github.com/microsoft/TypeScript-go/issues/4017#issuecomment-4505111440) **DanielRosenwasser** noted that the feature automatically takes effect when using "Configure Display Language" and suggested gathering feedback before considering overrides
 * [today](https://github.com/microsoft/TypeScript-go/issues/4017#issuecomment-4897652991) **DanielRosenwasser** said "We'll reopen if people provide feedback."
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#4031](https://github.com/microsoft/TypeScript-go/pull/4031) (Closed)

**Possible tests for refcount cache issues**

*Develop test cases to identify and diagnose issues in the reference count cache.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** closed the issue

### [Issue microsoft/TypeScript-go#4215](https://github.com/microsoft/TypeScript-go/issues/4215) (Closed, `Domain: API and Extensibility`)

**\`SourceFile\` is missing \`\.getLineStarts\(\)\` and \`\.getLineAndCharacterOfPosition\(\)\`**

*Add getLineStarts() and getLineAndCharacterOfPosition() getters to SourceFile for convenient API usage.*

 * created by **mrazauskas**
 * (1 month ago) **RyanCavanaugh** added label `Domain: API and Extensibility`, and set milestone to `Post-7.0`
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#4366](https://github.com/microsoft/TypeScript-go/pull/4366) (Closed, **jakebailey**, **Copilot**)

**Fix namespaced JSX intrinsic completions and hover**

*Add attribute completions and hover support for namespaced JSX elements by updating context recognition and quick-info resolution.*

 * **Copilot** assigned to **jakebailey**
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4366#issuecomment-4745452398) **jakebailey** said "@copilot a now non-failing test needs to be removed from  internal/fourslash/_scripts/failingTests.txt"
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4366#issuecomment-4745572053) **Copilot** removed the now-passing TestQuickInfoOnNewKeyword01 from failingTests.txt
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4380](https://github.com/microsoft/TypeScript-go/issues/4380) (Open, `Needs Investigation`, **johnfav03**)

**\[ServerErrors\]\[TypeScript\] main vs **

*Server errors occurred in the TypeScript main branch pipeline while analyzing 300 popular GitHub repositories, causing timeouts and other failures.*

 * (1 week ago) **RyanCavanaugh** set milestone to `Post-7.0`, and assigned to **johnfav03**
 * (6 days ago) **johnfav03** closed the issue
 * (today) **johnfav03** reopened the issue

### [Issue microsoft/TypeScript-go#4388](https://github.com/microsoft/TypeScript-go/issues/4388) (Closed, `bug`)

**Parameters not automatically filled for JSdoc comments**

*JSDoc comment skeletons generated by tsgo omit @param tags, unlike the default TypeScript 6.0 behavior.*

 * (5 days ago) **jakebailey** closed the issue
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/4388#issuecomment-4889323880) **crystalfp** asked when the fix would be available and noted that the problem still persisted with the specified version
 * [today](https://github.com/microsoft/TypeScript-go/issues/4388#issuecomment-4894864042) **jakebailey** attached an image and said they tested the example explicitly
 * [today](https://github.com/microsoft/TypeScript-go/issues/4388#issuecomment-4894925036) **crystalfp** thanked and reported that it worked in another project and said they would investigate differences between the two projects
 * [today](https://github.com/microsoft/TypeScript-go/issues/4388#issuecomment-4900774066) **crystalfp** said "Now started working everywhere. After an update of @typescript/native-preview maybe. Anyway, thanks for your effort!"

### [PR microsoft/TypeScript-go#4416](https://github.com/microsoft/TypeScript-go/pull/4416) (Closed, `Voight-Kampff Anomaly`)

**Fix panic in checker\.GetTypeArguments for non\-reference types \(\#4338\)**

*Guard exported Checker.GetTypeArguments to return an empty slice for non-reference types instead of panicking.*

 * created by **UditDewan**
 * **RyanCavanaugh** added to milestone `Post-7.0`
 * **RyanCavanaugh** added label `Voight-Kampff Anomaly`

### [PR microsoft/TypeScript-go#4420](https://github.com/microsoft/TypeScript-go/pull/4420) (Closed)

**\[api\] Add SourceFile line mapping methods**

*Add line mapping methods to the SourceFile API to map between source and generated code lines.*

 * [4 days ago](https://github.com/microsoft/TypeScript-go/pull/4420#issuecomment-4865510235) **mrazauskas** suggested implementing a TextFile utility class for generic line mapping to support formatting of TSConfig parsing diagnostics
 * [4 days ago](https://github.com/microsoft/TypeScript-go/pull/4420#issuecomment-4866814595) **andrewbranch** thanked for realizing the PR wasn’t merged, noted that tsconfig files have SourceFiles, and asked if exposing an API to fetch them would suffice
 * [4 days ago](https://github.com/microsoft/TypeScript-go/pull/4420#issuecomment-4867307173) **mrazauskas** suggested that using getConfigFileParsingDiagnostics to obtain a tsconfig SourceFile might suffice and asked whether to open a separate issue for SourceFile handling
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#4458](https://github.com/microsoft/TypeScript-go/pull/4458) (Closed)

**Vendor dprint plugins**

*Vendor copies of dprint plugins in the repository and add a script to update them, avoiding firewall fetch issues.*

 * created by **jakebailey**
 * [6 days ago](https://github.com/microsoft/TypeScript-go/pull/4458#issuecomment-4848601346) **jakebailey** said "dprint is getting "plugins via node_modules" so I'll hold off."
 * (later) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4476](https://github.com/microsoft/TypeScript-go/issues/4476) (Closed, `Domain: Editor`, **gabritto**)

**Only show notifications for failed LSP responses in VS Code Insiders**

*Only surface failed language server response notifications by default in VS Code Insiders, with an optional setting for others.*

 * (1 week ago) **DanielRosenwasser** added label `Domain: Editor`, set milestone to `TypeScript 7.0 Stable`, and assigned to **gabritto**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4482](https://github.com/microsoft/TypeScript-go/pull/4482) (Closed, **DanielRosenwasser**, **Copilot**)

**Fix auto\-imports crash in GetSourceOfProjectReferenceIfOutputIncluded**

*Prevent aliasResolver panics in GetSourceOfProjectReferenceIfOutputIncluded by returning file.FileName() and adding a regression test*

 * [6 days ago](https://github.com/microsoft/TypeScript-go/pull/4482#issuecomment-4846312221) **DanielRosenwasser** said "@copilot+gpt-5.5 the test didn't fail locally without the fix, so I think you are lying about having found a repro."
 * [6 days ago](https://github.com/microsoft/TypeScript-go/pull/4482#issuecomment-4846497464) **Copilot** acknowledged the repro issue, replaced the test in ca8f0490 to force node builder module specifier generation, and verified that it failed when GetSourceOfProjectReferenceIfOutputIncluded was unimplemented
 * [6 days ago](https://github.com/microsoft/TypeScript-go/pull/4482#issuecomment-4847110711) **DanielRosenwasser** said "@copilot+gpt-5.5 you changed a bunch of different functions - do we have tests that actually trigger the panics that they issue?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4482#issuecomment-4896635000) **Copilot** addressed tests for panic-triggering functions in commit 77a9afa1 and outlined the remaining regression exercise of the auto-import export-extraction path
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#4489](https://github.com/microsoft/TypeScript-go/pull/4489) (Closed)

**New extension layout**

*Restructure the TypeScript extension with the new TS7 layout under its native-preview identity, updating settings and packaging.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4499](https://github.com/microsoft/TypeScript-go/issues/4499) (Open, `Domain: API and Extensibility`, **andrewbranch**)

**Add \`TupleTypeReference\` interface to the API**

*Introduce a TupleTypeReference interface in the API to facilitate typed handling of tuple types with Checker#isTupleType.*

 * created by **mrazauskas**
 * (today) **andrewbranch** added label `Domain: API and Extensibility`, set milestone to `Post-7.0`, and assigned to **andrewbranch**

### [Issue microsoft/TypeScript-go#4502](https://github.com/microsoft/TypeScript-go/issues/4502) (Open, `Domain: API and Extensibility`, **andrewbranch**)

**\`Program\` is missing \`\.getSourceFiles\(\)\` getter**

*Add a getSourceFiles() getter to Program to return all SourceFile instances and ease filtering.*

 * created by **mrazauskas**
 * (today) **andrewbranch** added label `Domain: API and Extensibility`, set milestone to `Post-7.0`, and assigned to **andrewbranch**

### [Issue microsoft/TypeScript-go#4503](https://github.com/microsoft/TypeScript-go/issues/4503) (Closed, `Domain: API and Extensibility`, **andrewbranch**)

**Add APIs that set the compiler options programatically**

*Provide an API to programmatically set or update compiler options for inferred and configured projects.*

 * created by **mrazauskas**
 * (today) **andrewbranch** added label `Domain: API and Extensibility`, set milestone to `Post-7.0`, and assigned to **andrewbranch**

### [Issue microsoft/TypeScript-go#4519](https://github.com/microsoft/TypeScript-go/issues/4519) (Closed, `Domain: API and Extensibility`, **andrewbranch**)

**Consider exporting the \`inferredProjectName\` constant from the API**

*Propose exporting the inferredProjectName constant from the API to prevent breaking changes and facilitate reliable detection of inferred projects.*

 * created by **mrazauskas**
 * (today) **andrewbranch** added label `Domain: API and Extensibility`, set milestone to `Post-7.0`, and assigned to **andrewbranch**

### [PR microsoft/TypeScript-go#4529](https://github.com/microsoft/TypeScript-go/pull/4529) (Closed)

**Fix wildcard directories being dropped for "\./"\-prefixed includes with dot\-directory excludes**

*Wildcard directories defined by './'-prefixed include patterns are incorrectly dropped when dot-directory excludes are present, preventing new file detection.*

 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/4529#issuecomment-4874013472) **jansedlon** said "@microsoft-github-policy-service agree"
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/4529#issuecomment-4877759536) **jakebailey** said "Can you point to the Strada code, if this is just a porting bug?"
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/4529#issuecomment-4880819285) **jansedlon** pointed to the normalizePath implementation and explained how simpleNormalizePath strips './' segments to prevent the bug
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4534](https://github.com/microsoft/TypeScript-go/pull/4534) (Closed)

**Update tooling deps: npm/json and devcontainer lock**

*Add json to _scripts dependencies and generate package-lock.json and devcontainer-lock.json to pin tooling versions.*

 * created by **MasterTLF**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4535](https://github.com/microsoft/TypeScript-go/pull/4535) (Closed, `Voight-Kampff Anomaly`)

**Emit expando properties for functions that only become visible late in declaration emit**

*Defer expando property assignment processing so properties on functions only marked visible late are correctly emitted.*

 * created by **UditDewan**
 * **RyanCavanaugh** added label `Voight-Kampff Anomaly`

### [Issue microsoft/TypeScript-go#4536](https://github.com/microsoft/TypeScript-go/issues/4536) (Closed, `Domain: API and Extensibility`, **andrewbranch**)

**\`Type\` object is missing \`\.getCallSignatures\(\)\` and \`\.getConstructSignatures\(\)\` getters in the API**

*Implement missing getCallSignatures and getConstructSignatures getters on the Type object to align with Strada’s API.*

 * created by **mrazauskas**
 * (today) **andrewbranch** added label `Domain: API and Extensibility`, set milestone to `Post-7.0`, and assigned to **andrewbranch**
 * [later](https://github.com/microsoft/TypeScript-go/issues/4536#issuecomment-4905155803) **mrazauskas** reconsidered adding methods to Checker and realized getSignaturesOfType sufficed
 * (later) **mrazauskas** closed the issue

### [Issue microsoft/TypeScript-go#4539](https://github.com/microsoft/TypeScript-go/issues/4539) (Open, `Domain: API and Extensibility`, **andrewbranch**)

**Add \`StructuredType\` type to the API**

*Add StructuredType type to the API for use with TypeFlags.StructuredType checks and casting.*

 * created by **mrazauskas**
 * (today) **andrewbranch** added label `Domain: API and Extensibility`, set milestone to `Post-7.0`, and assigned to **andrewbranch**

### [PR microsoft/TypeScript-go#4542](https://github.com/microsoft/TypeScript-go/pull/4542) (Closed)

**Fix data race in \`snapshotFSBuilder\.GetAccessibleEntries\(\)\`**

*Prevent data races by cloning Files and Directories slices in snapshotFSBuilder.GetAccessibleEntries.*

 * created by **johnfav03**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4542#issuecomment-4895238771) **jakebailey** asked how the backing array had spare capacity and who was appending, and suggested using slices.Clip on creation instead of clone
 * [today](https://github.com/microsoft/TypeScript-go/pull/4542#issuecomment-4895652042) **johnfav03** explained that appending originated from readDirectoriesIntoEntries and that parallel config loading could cause multiple goroutines to call GetAccessibleEntries on the same path concurrently
 * [today](https://github.com/microsoft/TypeScript-go/pull/4542#issuecomment-4895679463) **jakebailey** said "What is readDirectoriesIntoEntries? I don't see that func in the repo"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4542#issuecomment-4895693925) **johnfav03** said "Sorry, I misspoke - readDirectoryIntoEntries"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4542#issuecomment-4895706149) **jakebailey** said "It seems to me the problem then is not this, but rather that those calls mutate the directories not under a lock"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4542#issuecomment-4895966745) **johnfav03** proposed performing readDirectoryIntoEntries on a local copy and then using LoadOrStore to eliminate shared mutation entirely
 * (today) **johnfav03** closed the issue

### [PR microsoft/TypeScript-go#4543](https://github.com/microsoft/TypeScript-go/pull/4543) (Closed)

**New setting to control whether error notifications are displayed**

*Introduce a user setting with auto, never, and always options to manage LSP error notifications display.*

 * created by **gabritto**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4544](https://github.com/microsoft/TypeScript-go/issues/4544) (Closed)

**test**

*Issue titled 'test' contains only placeholder text 'asdf' and lacks actionable details.*

 * created by **dmitrykobets-msft**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4544#issuecomment-4896154535) **dmitrykobets-msft** said "sorry, was creating an issue for another project and it auto-selected this repo"
 * (today) **dmitrykobets-msft** closed the issue

### [Issue microsoft/TypeScript-go#4545](https://github.com/microsoft/TypeScript-go/issues/4545) (Closed, `Domain: Editor`, `Crash`, **andrewbranch**)

**Fatal server crash at \`\(\*configFileRegistryBuilder\)\.invalidateCache\`**

*The server experiences a fatal crash while invalidating its configuration file registry cache.*

 * created by **andrewbranch**
 * (today) **andrewbranch** added labels `Domain: Editor`, `Crash`, and assigned to **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#4546](https://github.com/microsoft/TypeScript-go/pull/4546) (Closed)

**Release configs of removed project references**

*Provide release configurations for project references that were removed.*

 * created by **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#4547](https://github.com/microsoft/TypeScript-go/pull/4547) (Closed)

**Fix bulk cache invalidation of non\-existent referenced configs**

*Fix bulk cache invalidation to skip stubbed registry entries with nil commandLine for missing tsconfig references during watch events.*

 * created by **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#4548](https://github.com/microsoft/TypeScript-go/issues/4548) (Closed, `Domain: API and Extensibility`, **andrewbranch**)

**NodeList loop performance**

*Array iteration methods inherited by RemoteNodeList behave in quadratic time due to linked list access, while forEachNode provides linear iteration.*

 * created by **acutmore**
 * [later](https://github.com/microsoft/TypeScript-go/issues/4548#issuecomment-4901398372) **acutmore** said "Fixed in #4549"

### [PR microsoft/TypeScript-go#4549](https://github.com/microsoft/TypeScript-go/pull/4549) (Closed)

**\[api\] Optimize RemoteNodeList child access**

*RemoteNodeList access is optimized by reading raw buffer next pointers and caching them to improve iteration from O(n²) to O(n).*

 * created by **andrewbranch**
 * [later](https://github.com/microsoft/TypeScript-go/pull/4549#issuecomment-4901474940) **acutmore** said "Nice fix! Applying this patch locally I can confirm it fixes the benchmark case in #4548"

### [PR microsoft/TypeScript-go#4550](https://github.com/microsoft/TypeScript-go/pull/4550) (Closed)

**Set up stable / nightly extension split, other prep**

*Configure separate stable and nightly extension builds and related preparatory work, currently disabled.*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#4551](https://github.com/microsoft/TypeScript-go/pull/4551) (Open)

**Preserve pseudotype when serializing autoType declarations**

*Declaration serialization incorrectly emits ‘any’ for auto-typed variables initialized with null or undefined instead of preserving their pseudotypes.*

 * created by **revyh**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4551#issuecomment-4899558059) **revyh** said "@microsoft-github-policy-service agree"

### [PR microsoft/TypeScript-go#4552](https://github.com/microsoft/TypeScript-go/pull/4552) (Open)

**Add versions of get\*Diagostics that allow passing in an array of files\.**

*Enable passing multiple files to get*Diagnostics to batch diagnostic requests and reduce performance overhead.*

 * created by **dragomirtitian**

### [Issue microsoft/TypeScript-go#4553](https://github.com/microsoft/TypeScript-go/issues/4553) (Open, `Domain: API and Extensibility`, **andrewbranch**, **Copilot**)

**Add \`\.getConstraint\(\)\` and \`\.getDefault\(\)\` getter to \`TypeParameter\`**

*Add getConstraint() and getDefault() methods to TypeParameter for consistency with other type classes.*

 * created by **mrazauskas**

### [PR microsoft/TypeScript-go#4554](https://github.com/microsoft/TypeScript-go/pull/4554) (Closed)

**Move dprint plugins to npm**

*Publish dprint plugins to npm to circumvent firewall restrictions and eliminate manual pre-seeding in Copilot agent setup.*

 * created by **jakebailey**

