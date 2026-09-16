# Report for 2026-09-09 (Wednesday, September 9th, 2026)

23 different users commented on 39 different issues.

## Recommended Actions

 * Response Recommended
    * @MartinZikmund provided deterministic repro steps for the multi-targeting delete issue in [microsoft/TypeScript#50428](https://github.com/microsoft/TypeScript/issues/50428#issuecomment-5621029125)
    * @ericchase reported an internal parser error caused by JSDoc overload with generics in [microsoft/TypeScript#59980](https://github.com/microsoft/TypeScript/issues/59980#issuecomment-5614856466)
    * @devanshj provided example code and pointed to PR #64092 to fix the issue in [microsoft/TypeScript#64192](https://github.com/microsoft/TypeScript/issues/64192#issuecomment-5606700713)
    * @devanshj provided a generic utility implementation as a solution in [microsoft/TypeScript#64192](https://github.com/microsoft/TypeScript/issues/64192#issuecomment-5616093710)
    * @microsoft-github-policy-service requested that the contributor agree to the CLA in [microsoft/TypeScript#64224](https://github.com/microsoft/TypeScript/pull/64224#issuecomment-5611750154)

## Activity Summary

### [Issue microsoft/TypeScript#49638](https://github.com/microsoft/TypeScript/issues/49638) (Closed, `Not a Defect`)

**Combination of intersection type, mapped type and generic type seem to break type checks for nested properties**

*A generic function using an intersection and mapped type improperly permits extra nested properties in TS 4.7.4.*

 * **RyanCavanaugh** added label `Domain: Mapped Types`
 * [today](https://github.com/microsoft/TypeScript/issues/49638#issuecomment-5601082112) **RyanCavanaugh** explained that excess-property checking doesn't apply to generic inference and noted that the optional-`where` variation is now accepted in TypeScript 6.0.3
 * **RyanCavanaugh** added label `Needs Human Review`
 * (today) **RyanCavanaugh** added label `Not a Defect`, and removed labels `Bug`, `Help Wanted`, `Domain: Mapped Types`, `Needs Human Review`
 * [today](https://github.com/microsoft/TypeScript/issues/49638#issuecomment-5606017014) **RyanCavanaugh** said "This is no longer inconsistent with the non-intersected version, which I think is the more-correct set of behaviors."
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#50168](https://github.com/microsoft/TypeScript/issues/50168) (Closed, `Bug`, `Fixed`, `Help Wanted`, `Domain: lib.d.ts`)

**Symbol\.species should in constructor, not instance**

*Symbol.species is incorrectly declared on SharedArrayBuffer instances instead of its constructor in es2017.sharedmemory.d.ts.*

 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#50428](https://github.com/microsoft/TypeScript/issues/50428) (Open, `Visual Studio`, **joj**)

**MsBuild: Target \`TypeScriptDeleteOutputFromOtherConfigs\` can grab tsc\.out from other Configuration**

*TypeScriptDeleteOutputFromOtherConfigs uses a global obj path instead of config-specific IntermediateOutputPath, causing release builds to delete debug outputs.*

 * [1.2 years ago](https://github.com/microsoft/TypeScript/issues/50428#issuecomment-2913587314) **sergiocastelani** described that the build error occurred because TypeScriptDeleteOutputFromOtherConfigs deleted artifacts from other target frameworks, caused chaos in concurrent builds, and provided a sample project as proof
 * [1.2 years ago](https://github.com/microsoft/TypeScript/issues/50428#issuecomment-2914097493) **joj** asked if the workaround of overriding the targets was applicable and offered to add a conditional feature for versions 5.8 and later
 * [1.2 years ago](https://github.com/microsoft/TypeScript/issues/50428#issuecomment-2916229507) **sergiocastelani** mentioned inability to override TypeScriptDeleteOutputFromOtherConfigs and asked for a functional workaround, suggested adjusting TypeScript targets to avoid cross-framework artifact interference
 * [later](https://github.com/microsoft/TypeScript/issues/50428#issuecomment-5621029125) **MartinZikmund** described a multi-targeting variant of the intermediate output delete bug that can silently remove sibling framework artifacts, outlined its outcomes, and provided a deterministic repro

### [Issue microsoft/TypeScript#59980](https://github.com/microsoft/TypeScript/issues/59980) (Open, `Bug`, `Help Wanted`, `Domain: JSDoc`)

**JsDoc with overloads and different generics results in wrong dts output**

*JSDoc overloads with different generics incorrectly produce two string-bound signatures instead of a boolean overload in the .d.ts output.*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [1.6 years ago](https://github.com/microsoft/TypeScript/issues/59980#issuecomment-2613407171) **ljharb** said "This may be related to how you tsdoc in JS won't work properly if the type is a function overload and the generics list from all overloads isn't exactly identical?"
 * **RyanCavanaugh** added label `Domain: JSDoc`
 * [later](https://github.com/microsoft/TypeScript/issues/59980#issuecomment-5614856466) **ericchase** reported that the provided JSDoc overload with generics triggered an internal parser error causing unrelated doc comments to break

### [Issue microsoft/TypeScript#63855](https://github.com/microsoft/TypeScript/issues/63855) (Closed, `Possible Improvement`, **andrewbranch**)

**Improve API performance when using virtual file system**

*Include inline file content and precomputed directory listings in updateSnapshot to eliminate virtual file system IPC calls and improve performance.*

 * (8 weeks ago) **RyanCavanaugh** added labels `Possible Improvement`, `Possible Improvement`, and assigned to **andrewbranch**
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript#64115](https://github.com/microsoft/TypeScript/pull/64115) (Closed, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Add optional VFS parameters to updateSnapshot**

*Add optional VFS parameters to updateSnapshot with helpers for in-memory or layered file systems supporting fallback, symlinks, and removed paths.*

 * [6 days ago](https://github.com/microsoft/TypeScript/pull/64115#issuecomment-5532864937) **weswigham** suggested renaming functions to use "Layer" instead of "overlay" to avoid confusion with overlayFS on the backend
 * [5 days ago](https://github.com/microsoft/TypeScript/pull/64115#issuecomment-5545907874) **andrewbranch** argued that lazy compaction complexity outweighed its benefits, proposed and prototyped an eager clone-on-construction design that removed synchronization code, presented benchmarks showing faster reads/releases but slower snapshot creation, and concluded that eager compaction simplifies code with similar overall performance
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64115#issuecomment-5592043031) **weswigham** updated to main and swapped to eager layer compaction to optimize for reads, mentioning future toggles if needed
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript#64158](https://github.com/microsoft/TypeScript/pull/64158) (Open, `Author: Team`, `For Uncommitted Bug`, **iisaduan**)

**Build Orchestrator API **

*Implement a BuildOrchestrator API to programmatically build, clean, and manage project references in TypeScript 7.1 without watch mode.*

 * (6 days ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/64158#issuecomment-5621539680) **dragomirtitian** asked whether the new BuildOrchestrator supports diagnostics retrieval, file-specific checks, batched emits, and SourceFile access and inquired about plans to add these features

### [Issue microsoft/TypeScript#64166](https://github.com/microsoft/TypeScript/issues/64166) (Closed, `Bug`, **andrewbranch**)

**\`getCompletionsAtPosition\` in API deadlocks when used with \`includeSymbol: true\`**

*getCompletionsAtPosition deadlocks when includeSymbol:true is set due to reuse of the persistent TypeScript checker*

 * (5 days ago) **RyanCavanaugh** added label `Bug`, set milestone to `TypeScript 7.1.0 Beta`, and assigned to **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#64178](https://github.com/microsoft/TypeScript/pull/64178) (Closed, `For Milestone Bug`, **andrewbranch**)

**Prevent deadlock in \`getCompletionsAtPosition\(\.\.\., { includeSymbol: true }\)\` API**

*Remove the program.GetTypeChecker call from getExistingImports and explicitly pass the checker to avoid deadlock in getCompletionsAtPosition with includeSymbol enabled.*

 * (5 days ago) **typescript-automation[bot]** added label `For Milestone Bug`, and assigned to **andrewbranch**
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64178#issuecomment-5597219608) **auvred** said "Fixed the lint error, hadn't noticed it before 🤷‍♂️ "
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#64184](https://github.com/microsoft/TypeScript/pull/64184) (Closed, `For Uncommitted Bug`, **andrewbranch**)

**Fix RefCountCache\.Ref panic race between concurrent snapshot builds**

*Concurrent snapshot building in the TypeScript language server can cause RefCountCache.Ref to panic due to a cache entry race condition.*

 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/64184#issuecomment-5563109701) **NAVEENKUMARKR777** said "@microsoft-github-policy-service agree"
 * (yesterday) **andrewbranch** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/64184#issuecomment-5606971010) **NAVEENKUMARKR777** acknowledged that the stress test failure was caused by the test’s own bug, verified that reverting changes and applying only the snapshot fix resolved the issue, apologized for the noise, and closed the issue

### [Issue microsoft/TypeScript#64192](https://github.com/microsoft/TypeScript/issues/64192) (Open, `Needs Investigation`, **ahejlsberg**)

**Recursive inference through self\-referential object literals**

*Self-referential getters for recursive schemas trigger TypeScript's self-reference errors collapsing to implicit any, requiring Zod-style workarounds.*

 * (yesterday) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **ahejlsberg**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/64192#issuecomment-5594283251) **colinhacks** cross-posted a link to TypeScript PR 64172 for context, highlighted recursive type inference as a high-impact challenge, described Zod 4's loosened type safety workaround, and requested a solution preserving type safety
 * [today](https://github.com/microsoft/TypeScript/issues/64192#issuecomment-5606700713) **devanshj** demonstrated how PR #64091 could fix the recursive typing issue with example TypeScript code and invited testing of PR #64092
 * [later](https://github.com/microsoft/TypeScript/issues/64192#issuecomment-5616093710) **devanshj** demonstrated a generic utility function that solves the circular reference issue without library coupling or API changes

### [PR microsoft/TypeScript#64212](https://github.com/microsoft/TypeScript/pull/64212) (Closed, `For Uncommitted Bug`, **RyanCavanaugh**, **Copilot**)

**Type \`window\.opener\` as nullable \`WindowProxy\`**

*Type window.opener and global opener as nullable WindowProxy and add regression tests confirming their types.*

 * (today) **typescript-automation[bot]** added labels `For Milestone Bug`, `For Uncommitted Bug`, and removed label `For Milestone Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64212#issuecomment-5606434846) **Copilot** removed the test and generated baselines in f2801e0c
 * [today](https://github.com/microsoft/TypeScript/pull/64212#issuecomment-5606466694) **jakebailey** said "This is a generated file so I assume this goes to the other repo?"
 * [today](https://github.com/microsoft/TypeScript/pull/64212#issuecomment-5606605936) **RyanCavanaugh** said "🤦"
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#64214](https://github.com/microsoft/TypeScript/pull/64214) (Open, `For Backlog Bug`)

**Fix getChildren\(\) dropping opening '\<' token when immediately followed by '\<' \(\#64168\)**

*Fix addSyntheticNodes to split '<<' tokens so getChildren includes the missing '<' in consecutive type argument lists.*

 * created by **vaibhavsrv**
 * (today) **typescript-automation[bot]** added labels `For Backlog Bug`, `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64214#issuecomment-5605470327) **vaibhavsrv** rebased the branch onto clean upstream/main to remove deferred import commits and included only the getChildren() fix for issue #64168 with its AST invariant regression test

### [PR microsoft/TypeScript#64215](https://github.com/microsoft/TypeScript/pull/64215) (Closed, `Author: Team`, `For Uncommitted Bug`, **johnfav03**)

**Fix race in write loop marshal recovery test**

*Marshal recovery test for the write loop exhibits a race condition and requires a fix.*

 * created by **johnfav03**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **johnfav03**

### [PR microsoft/TypeScript#64216](https://github.com/microsoft/TypeScript/pull/64216) (Open, `Author: Team`, `For Uncommitted Bug`, **johnfav03**)

**Port \`createSourceFile\` and \`createSourceFileFromFile\`**

*Port createSourceFile and createSourceFileFromFile to the TypeScript API with the defined function signatures.*

 * created by **johnfav03**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **johnfav03**

### [PR microsoft/TypeScript#64217](https://github.com/microsoft/TypeScript/pull/64217) (Closed, `For Uncommitted Bug`)

**Fix compareNodes silently treating unindexed source files as file index 0**

*compareNodes silently treats unindexed files as index 0, causing incorrect file ordering and impacting type inference.*

 * created by **NAVEENKUMARKR777**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64217#issuecomment-5607502683) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (today) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/64217#issuecomment-5607637057) **NAVEENKUMARKR777** acknowledged the assertion oversight, pushed commit 360c29f to enforce documented sorting direction, and confirmed it fails a sign-flipped variant

### [Issue microsoft/TypeScript#64218](https://github.com/microsoft/TypeScript/issues/64218) (Closed)

**checker\.compareNodes treats a source file missing from fileIndexMap as file index 0**

*In the Go checker compareNodes, missing fileIndexMap entries default to zero, causing unindexed files to sort incorrectly and collapse as equal rather than receiving a consistent ordering.*

 * created by **NAVEENKUMARKR777**
 * [today](https://github.com/microsoft/TypeScript/issues/64218#issuecomment-5607621762) **RyanCavanaugh** said "I have questions about this but I'm not engaging with a bot about it. Consult the repo AI policy."
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#64219](https://github.com/microsoft/TypeScript/pull/64219) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**, **johnfav03**)

**Fix FSEvents watches with mismatched path casing**

*WatchManager now normalizes caller and disk path casing to avoid missing FSEvents on macOS.*

 * created by **johnfav03**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **johnfav03**, **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript/pull/64219#issuecomment-5608276589) **jakebailey** questioned whether the change restored previously removed code and linked to a related pull request
 * [today](https://github.com/microsoft/TypeScript/pull/64219#issuecomment-5608705321) **johnfav03** acknowledged issue #64210 and said they would close the PR
 * (today) **johnfav03** closed the issue

### [PR microsoft/TypeScript#64220](https://github.com/microsoft/TypeScript/pull/64220) (Open, `For Milestone Bug`, **johnfav03**)

**Schedule tsc \-b projects by dependency depth so builders do not idle on upstream projects**

*Sort tsc -b build tasks by dependency depth instead of depth-first references to reduce idle time and speed up parallel builds.*

 * created by **christianvuerings**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [PR microsoft/TypeScript#64221](https://github.com/microsoft/TypeScript/pull/64221) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**Fix content mapper LSP race**

*Resolve a race condition in the content mapper of the TypeScript language server to prevent intermittent failures.*

 * created by **andrewbranch**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`, and assigned to **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript#64222](https://github.com/microsoft/TypeScript/issues/64222) (Open, `Needs Investigation`, **johnfav03**)

**tsc \-b: builders idle on upstream projects because projects are scheduled in depth\-first reference order**

*The build orchestrator's depth-first scheduling of project references in tsc -b leads to builder idle time and slower parallel builds.*

 * created by **christianvuerings**

### [PR microsoft/TypeScript#64223](https://github.com/microsoft/TypeScript/pull/64223) (Open, `For Backlog Bug`)

**fix\(checker\): narrow Uppercase/Lowercase/Capitalize/Uncapitalize\<string\> via equality checks**

*Uppercase<string> and related string mapping types now narrow correctly against specific literals and yield errors for impossible comparisons.*

 * created by **erantianantha**
 * (today) **typescript-automation[bot]** added labels `For Backlog Bug`, `For Backlog Bug`

### [PR microsoft/TypeScript#64224](https://github.com/microsoft/TypeScript/pull/64224) (Open, `For Backlog Bug`)

**Fix swapped charCodeAt/codePointAt JSDoc descriptions**

*Correct JSDoc comments for charCodeAt and codePointAt in TypeScript libs to distinguish UTF-16 units from Unicode code points.*

 * created by **techreign**
 * (today) **typescript-automation[bot]** added labels `For Backlog Bug`, `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64224#issuecomment-5611750154) **microsoft-github-policy-service[bot]** prompted the contributor to read and agree to the Contributor License Agreement by replying with the required command

### [Issue microsoft/TypeScript#64225](https://github.com/microsoft/TypeScript/issues/64225) (Closed, `Needs More Info`)

**1\.136\.1: with TS Nightly, the tsconfig\.json does not use \`\-\-runExternalCode\`**

*VS Code 1.136.1 fails to apply the --runExternalCode flag in tsconfig.json with TypeScript nightly, causing content-mapper errors.*

 * **vs-code-engineering[bot]** assigned to **jruales**
 * (yesterday) **jruales** assigned to **dbaeumer**, and unassigned **jruales**
 * **dbaeumer** unassigned **dbaeumer**
 * [later](https://github.com/microsoft/TypeScript/issues/64225#issuecomment-5614729642) **dbaeumer** said "Seems related to TS 7"
 * [later](https://github.com/microsoft/TypeScript/issues/64225#issuecomment-5618456857) **NullVoxPopuli** said "ts CLI has had no issues, afaict"

### [PR microsoft/TypeScript#64226](https://github.com/microsoft/TypeScript/pull/64226) (Open, `For Uncommitted Bug`)

**fix: report optional\-chain tagged templates after non\-null assertions**

*Ensure tagged template expressions following non-null assertions in optional chains correctly trigger TS1358 errors.*

 * created by **camc314**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/64226#issuecomment-5616742706) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."

### [Issue microsoft/TypeScript#64227](https://github.com/microsoft/TypeScript/issues/64227) (Open, `Bug`, `Help Wanted`, `Domain: lib.d.ts`)

**The \`options\` arg of \`Temporal\.ZonedDateTime\.prototype\.toLocaleString\(\)\` currently accepts "illegal" option \`timeZone\`**

*TypeScript’s lib.esnext.temporal.d.ts incorrectly allows a timeZone option for Temporal.ZonedDateTime.prototype.toLocaleString despite the specification forbidding it.*

 * created by **Sector6759**

### [Issue microsoft/TypeScript#64228](https://github.com/microsoft/TypeScript/issues/64228) (Open, `Needs More Info`)

**Incorrect TS1111 when using private generator function in JS**

*VSCode erroneously raises TS1111 error when invoking a private generator method on another instance within a class.*

 * created by **Ecco**

### [Issue microsoft/TypeScript#64229](https://github.com/microsoft/TypeScript/issues/64229) (Open, `Design Limitation`)

**nullish types not narrowed in if block**

*Optional chaining and nullish coalescing conditions do not narrow nullish types within if blocks in TypeScript.*

 * created by **errorx666**

### [PR microsoft/TypeScript#64230](https://github.com/microsoft/TypeScript/pull/64230) (Open, `Author: Team`, `For Uncommitted Bug`, **gabritto**)

**Narrow generic conditional and indexed access return types when checking return statements**

*Port two pull requests to narrow generic conditional and indexed access return types during return statement analysis, fixing related bugs.*

 * created by **gabritto**
 * (later) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **gabritto**

