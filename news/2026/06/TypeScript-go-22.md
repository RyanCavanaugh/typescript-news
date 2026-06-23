# Report for 2026-06-22 (Monday, June 22nd, 2026)

15 different users commented on 38 different issues.

## Recommended Actions

 * Response Recommended
    * @safal207 provided reproduction steps and benchmark results for TypeScript 7 RC in [microsoft/TypeScript-go#1493](https://github.com/microsoft/TypeScript-go/issues/1493#issuecomment-4776440202)
    * @typescript-automation[bot] provided performance run results as requested in [microsoft/TypeScript-go#4239](https://github.com/microsoft/TypeScript-go/pull/4239#issuecomment-4770330390)
    * @crystalfp reported that disabling other extensions did not resolve the issue in [microsoft/TypeScript-go#4388](https://github.com/microsoft/TypeScript-go/issues/4388#issuecomment-4776578634)
    * @typescript-automation[bot] reported successful tsc runs on top 400 repos in [microsoft/TypeScript-go#4389](https://github.com/microsoft/TypeScript-go/pull/4389#issuecomment-4770703379)

## Activity Summary

### [Issue microsoft/TypeScript-go#1493](https://github.com/microsoft/TypeScript-go/issues/1493) (Open, `Domain: CLI`, **jakebailey**, **Copilot**)

**Exit code for type error is incorrect starting from \`7\.0\.0\-dev\.20250724\.1\`**

*tsgo in @typescript/native-preview@7.0.0-dev.20250724.1 returns exit code 1 for type errors instead of the expected code 2.*

 * [46 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1493#issuecomment-3145752282) **sheetalkamat** clarified that the code was correct as it represented ExitStatusDiagnosticsPresent_OutputsSkipped despite upcoming enum value changes
 * (45 weeks ago) **alexsch01** closed the issue
 * [45 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1493#issuecomment-3161144971) **alexsch01** said "Accidentally closed the issue but the issue is still happening in newest builds"
 * [today](https://github.com/microsoft/TypeScript-go/issues/1493#issuecomment-4776440202) **safal207** reproduced the issue with TypeScript 7 RC across all three GitHub-hosted operating systems and reported consistent diagnostic codes and outputs, linking to a reproducible harness and detailed benchmark results
 * (later) **jakebailey** reopened the issue
 * (later) **jakebailey** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#3848](https://github.com/microsoft/TypeScript-go/issues/3848) (Closed, `Domain: Editor`, **DanielRosenwasser**)

**Issue warning when extensions try to contribute TSServer plugins that while \`useTsgo\` is on**

*Warn users when extensions contribute TSServer plugins with useTsgo enabled, offering Dismiss, Disable Native Preview, and Don't Show Again options.*

 * **DanielRosenwasser** added label `Domain: Editor`
 * (4 days ago) **jakebailey** set milestone to `TypeScript 7.0 Stable`, and removed from milestone `TypeScript 7.0 RC`
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#4063](https://github.com/microsoft/TypeScript-go/pull/4063) (Closed)

**Warn on TSServer Plugin Contributions from other extensions**

*Display warnings when external extensions contribute TSServer plugins in both single-folder and multi-root workspaces*

 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * (4 days ago) **jakebailey** set milestone to `TypeScript 7.0 Stable`, and removed from milestone `TypeScript 7.0 RC`
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#4234](https://github.com/microsoft/TypeScript-go/pull/4234) (Closed, `No linked issue`)

**Skip mark/rewind in \`tryParseTypeArgumentsInExpression\` when token isn't \`\<\`**

*Optimize tryParseTypeArgumentsInExpression by skipping parser mark/rewind overhead when the token isn't '<', improving performance.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4234#issuecomment-4652926633) **typescript-automation[bot]** noted CI jobs started and linked to results
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4234#issuecomment-4653159218) **typescript-automation[bot]** provided the requested performance run results
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4234#issuecomment-4761761427) **mds-ant** said "@jakebailey @DanielRosenwasser Are there any changes you'd like me to make here? If not, are we good to merge this PR?"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4239](https://github.com/microsoft/TypeScript-go/pull/4239) (Open, `No linked issue`)

**Replace ForEachReturnStatement closure with direct kind\-switched walk**

*Replace ForEachReturnStatement closure with a direct kind-switched recursive function to reduce allocations and improve performance.*

 * [today](https://github.com/microsoft/TypeScript-go/pull/4239#issuecomment-4766974869) **mds-ant** said "@DanielRosenwasser The small perf regressions are a little surprising. Could we re-run the benchmarks, just to make sure those weren't just noise?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4239#issuecomment-4770071961) **DanielRosenwasser** said "@typescript-bot perf test this"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4239#issuecomment-4770072931) **typescript-automation[bot]** reported the start of performance tests and provided links to build status and results
 * [today](https://github.com/microsoft/TypeScript-go/pull/4239#issuecomment-4770330390) **typescript-automation[bot]** provided the requested TypeScript compiler performance run results in a detailed comparison report

### [PR microsoft/TypeScript-go#4240](https://github.com/microsoft/TypeScript-go/pull/4240) (Closed, `No linked issue`)

**Inline \`GetCombinedNodeFlags\` and \`GetCombinedModifierFlags\` bodies**

*Inline flag computations by replacing generic helper with direct node field reads, boosting performance by about 27%.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4240#issuecomment-4652521791) **jakebailey** said "Hm, but as the copilot comment notes, this involves a copy paste"
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4240#issuecomment-4658350219) **mds-ant** noted that code duplication was necessary to enable the optimization, explained the trade-offs of a shared helper, and offered to close the PR if the duplication is unwanted
 * [today](https://github.com/microsoft/TypeScript-go/pull/4240#issuecomment-4766982146) **mds-ant** said "@jakebailey Are you happy merging this, or would you rather not? The win is measurable in relative terms, but small in absolute terms."
 * [today](https://github.com/microsoft/TypeScript-go/pull/4240#issuecomment-4770844703) **jakebailey** said "I'm still not sure; obviously it's measurable, but there's a balance between code duplication and how much this benefits real-world code."
 * [today](https://github.com/microsoft/TypeScript-go/pull/4240#issuecomment-4772686404) **mds-ant** said "Yeah, that's fair. I'm happy to close this one out if you'd rather not take on the duplication."
 * (later) **mds-ant** closed the issue

### [Issue microsoft/TypeScript-go#4319](https://github.com/microsoft/TypeScript-go/issues/4319) (Closed, `Domain: API and Extensibility`, **andrewbranch**, **Copilot**)

**Add \`StringLiteral\`, \`NumberLiteral\` and others to the API**

*Extend the API with distinct literal types, properly support bigint values, and preserve negative bigint signs.*

 * (6 days ago) **RyanCavanaugh** added label `Domain: API and Extensibility`, and set milestone to `Post-7.0`
 * **andrewbranch** assigned to **Copilot**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4319#issuecomment-4775915822) **mrazauskas** said "Got added in #4344"
 * (today) **mrazauskas** closed the issue

### [Issue microsoft/TypeScript-go#4335](https://github.com/microsoft/TypeScript-go/issues/4335) (Open, `Needs Investigation`, **andrewbranch**, **Copilot**)

**checker\.getBaseTypes panics for type alias to generic interface instantiation**

*checker.getBaseTypes panics with a nil pointer dereference when processing a type alias to a generic interface instantiation*

 * **RyanCavanaugh** added to milestone `Post-7.0`
 * **andrewbranch** assigned to **Copilot**
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/4335#issuecomment-4752576072) **ahejlsberg** explained that getBaseTypes was being called on a type reference and suggested calling getTarget first
 * [today](https://github.com/microsoft/TypeScript-go/issues/4335#issuecomment-4770603293) **andrewbranch** asked whether the type flags disagreed with the underlying data after encountering a panic in c.getBaseTypes
 * [today](https://github.com/microsoft/TypeScript-go/issues/4335#issuecomment-4776387189) **ahejlsberg** clarified that the getBaseTypes function should test for ObjectFlagsClassOrInterface|ObjectFlagsTuple to return nil on plain type references and explained why the existing code still works

### [PR microsoft/TypeScript-go#4341](https://github.com/microsoft/TypeScript-go/pull/4341) (Open)

**API: make object registries project\-specific to avoid id collisions on types and signatures**

*Make object registries project-specific to prevent ID collisions on types and signatures and facilitate checker method refactoring.*

 * created by **piotrtomiak**
 * [later](https://github.com/microsoft/TypeScript-go/pull/4341#issuecomment-4776701704) **piotrtomiak** suggested improving symbol caching by moving the data cache to the Snapshot level and proposed relocating Checker methods to the Symbol interface for a more intuitive API
 * [later](https://github.com/microsoft/TypeScript-go/pull/4341#issuecomment-4780656375) **andrewbranch** said "I'm not sure that's a goal, since those Checker methods are identical to Strada. Either way, having Symbol reference equality (within a snapshot but across projects) is a hard requirement."
 * [later](https://github.com/microsoft/TypeScript-go/pull/4341#issuecomment-4780993512) **piotrtomiak** said "Ok, got it. I'll move symbols down to the snapshot level then, keeping types and signatures at project level. OK?"

### [PR microsoft/TypeScript-go#4344](https://github.com/microsoft/TypeScript-go/pull/4344) (Closed, **andrewbranch**, **Copilot**)

**Add per\-kind literal type interfaces and decode BigInt literal values to \`bigint\` in the API**

*Introduce per-kind literal type interfaces and decode BigInt literal strings into actual bigint values in the native-preview API*

 * **Copilot** assigned to **andrewbranch**
 * [6 days ago](https://github.com/microsoft/TypeScript-go/pull/4344#issuecomment-4725005441) **andrewbranch** said "@copilot address review feedback, though the “only call BigInt(...) when the payload value is actually a string” sounds overly defensive to me"
 * [6 days ago](https://github.com/microsoft/TypeScript-go/pull/4344#issuecomment-4725077495) **Copilot** addressed review feedback by updating value handling to treat undefined and null as absent, allowing null on the wire, and retaining BigInt decoding keyed on the BigIntLiteral flag
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#4345](https://github.com/microsoft/TypeScript-go/pull/4345) (Open, **andrewbranch**, **Copilot**)

**Fix getBaseTypes panic on type reference instantiations**

*Change getBaseTypes guard flags to exclude plain type references and prevent nil pointer panics on generic instantiations.*

 * **Copilot** assigned to **andrewbranch**
 * [6 days ago](https://github.com/microsoft/TypeScript-go/pull/4345#issuecomment-4724979237) **andrewbranch** said "@copilot what do you mean this mirrors Strada? I don't see anything like this code in Strada."
 * [6 days ago](https://github.com/microsoft/TypeScript-go/pull/4345#issuecomment-4725013121) **Copilot** acknowledged overstatement and corrected the wording, explained the behavioral equivalence and redirect mechanism compared to Strada, and noted the fix in commit 1e9b
 * [later](https://github.com/microsoft/TypeScript-go/pull/4345#issuecomment-4780674562) **andrewbranch** said "@copilot this is wrong. Check the latest conversation in https://github.com/microsoft/typescript-go/issues/4335 and update accordingly."
 * [later](https://github.com/microsoft/TypeScript-go/pull/4345#issuecomment-4780728949) **Copilot** updated the guard to use ObjectFlagsClassOrInterface|ObjectFlagsTuple, removed the ref.target redirect, and reverted commit bb5ad67 per Anders' guidance

### [PR microsoft/TypeScript-go#4353](https://github.com/microsoft/TypeScript-go/pull/4353) (Closed)

**API: make it possible to open file in inferred projects through API **

*Enable the API to open files from node_modules in inferred projects even when not in the import graph.*

 * created by **piotrtomiak**
 * (later) **piotrtomiak** closed the issue

### [Issue microsoft/TypeScript-go#4354](https://github.com/microsoft/TypeScript-go/issues/4354) (Closed, `Domain: Editor`, **gabritto**)

**No editor error for invalid tsconfig settings**

*TypeScript 7 native preview fails to report editor errors for invalid tsconfig compilerOptions values that TypeScript 6 previously flagged*

 * (5 days ago) **DanielRosenwasser** set milestones to `Post-7.0`, `TypeScript 7.0 Stable`, and removed from milestone `Post-7.0`
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript-go#4355](https://github.com/microsoft/TypeScript-go/pull/4355) (Closed)

**fix\(4354\): add tsconfig option errors from project diagnostics**

*Add a tsconfig option to enable reporting of project diagnostic errors.*

 * created by **a-tarasyuk**
 * (today) **gabritto** closed the issue

### [Issue microsoft/TypeScript-go#4372](https://github.com/microsoft/TypeScript-go/issues/4372) (Closed, **jakebailey**, **Copilot**)

**7\.0\.1\-rc binary in watch mode fails to resolve symlinks in node\_modules**

*TypeScript 7.0.1-rc watch mode fails to resolve or watch symlinked node_modules dependencies, causing fanotify errors.*

 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/4372#issuecomment-4754870819) **nikelborm** said "I'll try :D"
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/4372#issuecomment-4754939390) **nikelborm** said "It no longer throws errors, and changes propagate between packages properly"
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/4372#issuecomment-4754941073) **nikelborm** said "Thanks! 🫶 "
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4376](https://github.com/microsoft/TypeScript-go/pull/4376) (Closed, **jakebailey**, **Copilot**)

**Fix watches on symlinked directories**

*Fix watch mode on symlinked directories by resolving watch roots to physical paths and preserving symlink paths in events.*

 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/4376#issuecomment-4753955393) **jakebailey** reported a Windows test failure in TestWalkDirDoesNotFollowRootSymlinkedDir for root symlinked directory
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/4376#issuecomment-4754033402) **Copilot** fixed the Windows walkDir root check to reject reparse-point roots to match the generic implementation and test expectations in commit 5b44de91
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/4376#issuecomment-4754780349) **jakebailey** said "This PR basically just allows directory watches on dirs that are symlinks. It turns out that Node previously allowed such a thing. And TS treats symlinks to dirs as dirs, so it all "worked"."
 * [today](https://github.com/microsoft/TypeScript-go/pull/4376#issuecomment-4770517541) **andrewbranch** said "lspwatcher handles this itself, so that special handling should be removed."
 * [today](https://github.com/microsoft/TypeScript-go/pull/4376#issuecomment-4770599045) **jakebailey** said "Indeed, yes."
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4381](https://github.com/microsoft/TypeScript-go/issues/4381) (Open, **jakebailey**, **Copilot**)

**Behavior difference: \`\.state\` emit is missing on react component**

*tsgo incorrectly omits emitting React component state initializations inside constructors for JavaScript files, unlike tsc.*

 * [today](https://github.com/microsoft/TypeScript-go/issues/4381#issuecomment-4765925506) **hkleungai** clarified that they intentionally name files with js/ts suffix to differentiate transpiler behavior and visualize both mapping to the same main.d.ts file
 * [today](https://github.com/microsoft/TypeScript-go/issues/4381#issuecomment-4766441812) **nikelborm** clarified that he meant import statements placement rather than file suffixes, noting that in the provided snippet the import statements were at the end of the file
 * [today](https://github.com/microsoft/TypeScript-go/issues/4381#issuecomment-4766499771) **hkleungai** said "Ohh, that. I believe it is existing tsc behaviors on js file, before tsgo happens."
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#4382](https://github.com/microsoft/TypeScript-go/pull/4382) (Open)

**fix\(relater\): add property comparison cache fast path to avoid false TS2321**

*Add a relation-cache fast path in property-type comparisons to avoid false TS2321 errors for large object literals*

 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/4382#issuecomment-4757235439) **maoger** said "@microsoft-github-policy-service agree"
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/4382#issuecomment-4758527237) **jakebailey** stated that they were not going to be raising any limits
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/4382#issuecomment-4758968472) **maoger** removed the stack depth limit change, relied on a relation-cache fast path to avoid redundant stack pushes, confirmed tests passed and baseline unaffected, and marked the PR ready for review
 * [today](https://github.com/microsoft/TypeScript-go/pull/4382#issuecomment-4770428841) **jakebailey** asked about the origin and rationale of the change, its presence in TS 6, the absence of an issue, real-codebase experience, and AI-assistance disclosure

### [PR microsoft/TypeScript-go#4384](https://github.com/microsoft/TypeScript-go/pull/4384) (Closed)

**Fix panic on non\-string include/exclude/files in extended configs**

*Prevent tsgo from panicking when extended config include, exclude, or files fields contain non-string values.*

 * created by **oMatheusmol**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4388](https://github.com/microsoft/TypeScript-go/issues/4388) (Open)

**Parameters not automatically filled for JSdoc comments**

*JSDoc comment skeletons generated by tsgo omit @param tags, unlike the default TypeScript 6.0 behavior.*

 * created by **crystalfp**
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/4388#issuecomment-4765261220) **jakebailey** said "You haven't turned off the main TS extension, right? That's what should be doing this still."
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/4388#issuecomment-4765277247) **crystalfp** installed the Typescript native preview extension and enabled it with the 'Enable (experimental)' command then observed that disabling it reverted to v6 behavior
 * [today](https://github.com/microsoft/TypeScript-go/issues/4388#issuecomment-4776578634) **crystalfp** said "Nothing change disabling all the other extensions."

### [PR microsoft/TypeScript-go#4389](https://github.com/microsoft/TypeScript-go/pull/4389) (Open)

**Prefer covariant inferences with deeper type argument nesting**

*Prioritize covariant type inferences originating from more deeply nested type arguments to improve inference quality.*

 * [today](https://github.com/microsoft/TypeScript-go/pull/4389#issuecomment-4770130395) **jakebailey** said "@typescript-bot test top400"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4389#issuecomment-4770149372) **jakebailey** said "@typescript-bot test top400"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4389#issuecomment-4770150195) **typescript-automation[bot]** reported CI test top400 job started and linked to build status and results
 * [today](https://github.com/microsoft/TypeScript-go/pull/4389#issuecomment-4770703379) **typescript-automation[bot]** reported successful tsc runs on top 400 repos comparing main and the PR merge
 * **ahejlsberg** added to milestone `TypeScript 7.0 Stable`

### [Issue microsoft/TypeScript-go#4392](https://github.com/microsoft/TypeScript-go/issues/4392) (Open, `Crash`, **DanielRosenwasser**, **Copilot**)

**panic: cache entry not found \[recovered, repanicked\]**

*TypeScript server v7.0.0-dev panics with 'cache entry not found' while handling file open and config updates.*

 * created by **motopods**
 * **motopods** added label `Crash`
 * (today) **DanielRosenwasser** assigned to **Copilot**, **DanielRosenwasser**

### [PR microsoft/TypeScript-go#4394](https://github.com/microsoft/TypeScript-go/pull/4394) (Closed)

**Fix generated Is\* guards for type\-parameter\-kinded nodes**

*Correct Is* guard generation for type-parameter-kinded nodes to eliminate broken JavaScript due to fallthrough.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4395](https://github.com/microsoft/TypeScript-go/pull/4395) (Open)

**Devirtualize ForEachChild and IterChildren**

*Generate specialized implementations for ForEachChild and IterChildren to eliminate interface calls and improve inlining.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4395#issuecomment-4770210933) **jakebailey** said "@typescript-bot perf test this"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4395#issuecomment-4770211791) **typescript-automation[bot]** started jobs and provided build status and result links
 * [today](https://github.com/microsoft/TypeScript-go/pull/4395#issuecomment-4770451413) **typescript-automation[bot]** provided the results of the requested performance run with a detailed comparison report

### [PR microsoft/TypeScript-go#4396](https://github.com/microsoft/TypeScript-go/pull/4396) (Open, **jakebailey**, **Copilot**)

**Emit JS constructor \`this\` properties in declarations**

*Emit JS constructor-assigned properties in .d.ts files even when inherited so React-style this.state appears in declarations*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#4397](https://github.com/microsoft/TypeScript-go/pull/4397) (Closed)

**docs: add descriptive comment to tsgo entry point**

*Add a descriptive comment block to the tsgo.js entry point explaining its purpose and performance fallback mechanism.*

 * created by **Lang-Qiu**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4397#issuecomment-4770942351) **jakebailey** said "I do not think we need a comment explaining what our entrypoint does, and this breaks formatting and has no associated issue, and is seemingly AI generated."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4398](https://github.com/microsoft/TypeScript-go/pull/4398) (Closed)

**Watcher performance improvements**

*Reuse single-file programs and skip unnecessary operations in the watcher while using a watchSetDirty flag for rebuilds.*

 * created by **johnfav03**
 * (today) **johnfav03** closed the issue

### [PR microsoft/TypeScript-go#4399](https://github.com/microsoft/TypeScript-go/pull/4399) (Open)

**Watcher performance improvements**

*Implement single-file program reuse, skip redundant operations, and track rebuild requirements with watchSetDirty to improve watcher performance.*

 * created by **johnfav03**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4399#issuecomment-4773796433) **jakebailey** said "Do you have any data about how this affects things?"
 * [later](https://github.com/microsoft/TypeScript-go/pull/4399#issuecomment-4780787469) **johnfav03** provided benchmark results showing single-file edits had a 50% rebuild time decrease and higher-volume edits saw about 10% improvement

### [PR microsoft/TypeScript-go#4400](https://github.com/microsoft/TypeScript-go/pull/4400) (Open, **DanielRosenwasser**, **Copilot**)

**Fix parse cache ref race during cloned program updates**

*Implements new parse-cache reference methods to avoid race conditions and panics when cloned programs reuse SourceFile pointers.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **DanielRosenwasser**

### [PR microsoft/TypeScript-go#4401](https://github.com/microsoft/TypeScript-go/pull/4401) (Open)

**Default to GOGC=50**

*Default the Go garbage collector threshold (GOGC) to 50 to achieve substantial memory savings without degrading performance.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4401#issuecomment-4773584596) **jakebailey** said "@typescript-bot perf test this"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4401#issuecomment-4773585143) **typescript-automation[bot]** posted build job status with links to the started and results pages
 * [today](https://github.com/microsoft/TypeScript-go/pull/4401#issuecomment-4773774427) **typescript-automation[bot]** notified that the requested performance run results were available
 * [today](https://github.com/microsoft/TypeScript-go/pull/4401#issuecomment-4773780014) **jakebailey** said "Huh... Worse?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4401#issuecomment-4773785662) **jakebailey** said "Well, more worse than I was expecting anyway"

### [PR microsoft/TypeScript-go#4402](https://github.com/microsoft/TypeScript-go/pull/4402) (Open)

**\[api\] Flesh out project/file open state management**

*Enhance the API client's updateSnapshot to support opening and closing files and projects, enabling inferred projects and tsconfig auto-discovery.*

 * created by **andrewbranch**

### [Issue microsoft/TypeScript-go#4403](https://github.com/microsoft/TypeScript-go/issues/4403) (Open, **jakebailey**)

**Regression: CJS emit drops namespace qualifier on RHS of module\-scope \`export const { … } = importedValue\` → ReferenceError**

*Module-scope export const destructuring in CommonJS emit drops the import namespace qualifier and causes a ReferenceError.*

 * created by **thaoula**
 * **jakebailey** assigned to **jakebailey**

### [PR microsoft/TypeScript-go#4404](https://github.com/microsoft/TypeScript-go/pull/4404) (Open)

**Add repro for CommonJS export destructuring emit**

*Add a reproduction example showing CommonJS export destructuring emission*

 * created by **jakebailey**

### [Issue microsoft/TypeScript-go#4405](https://github.com/microsoft/TypeScript-go/issues/4405) (Open)

**App using programmatic APIs fails to typecheck with \`exactOptionalPropertyTypes: true\` and \`@types/node\` v24**

*With exactOptionalPropertyTypes enabled and @types/node v24 installed, programmatic API imports fail to compile due to type incompatibilities.*

 * created by **mrazauskas**

### [Issue microsoft/TypeScript-go#4406](https://github.com/microsoft/TypeScript-go/issues/4406) (Open)

**Independent cross\-platform benchmark of TypeScript 7\.0\.1 RC vs TypeScript 6\.0\.3**

*Reproducible cross-platform benchmark shows TypeScript 7.0.1 RC outperforms 6.0.3 by 4.6–6.5× across diverse build scenarios with identical outputs.*

 * created by **safal207**

### [PR microsoft/TypeScript-go#4407](https://github.com/microsoft/TypeScript-go/pull/4407) (Open, **jakebailey**, **Copilot**)

**Restore tsgo exit code for type errors**

*Restore tsgo exit code 2 for type errors by mapping tsc diagnostic statuses in cmd/tsgo and adding focused regression tests.*

 * created by **Copilot**
 * (later) **Copilot** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#4408](https://github.com/microsoft/TypeScript-go/issues/4408) (Open, **ahejlsberg**)

**Regression: recursive conditional\+mapped "serialize" type no longer proves \`Transform\<X\>\` assignable to \`X\` on deeply\-nested compound types \(native\-preview; works in tsc\)**

*A regression in @typescript/native-preview fails to prove recursive mapped serialize types as identity for deeply nested compound types.*

 * created by **dimofeev**
 * **jakebailey** assigned to **ahejlsberg**

### [PR microsoft/TypeScript-go#4409](https://github.com/microsoft/TypeScript-go/pull/4409) (Open)

**\[feature request\] Support type predicate getters for control flow narrowing**

*Support type predicate getters so accessing getters can narrow receiver types in control flow checks*

 * created by **js2me**
 * [later](https://github.com/microsoft/TypeScript-go/pull/4409#issuecomment-4779021262) **js2me** said "@microsoft-github-policy-service agree"
 * **RyanCavanaugh** added to milestone `Possible Improvement`

