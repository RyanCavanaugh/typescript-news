# Report for 2026-06-24 (Wednesday, June 24th, 2026)

14 different users commented on 47 different issues.

## Recommended Actions

 * Response Recommended
    * @freshp86 asked why errors were suppressed when checkJs was set to false in [microsoft/TypeScript-go#4437](https://github.com/microsoft/TypeScript-go/issues/4437#issuecomment-4794121041)
    * @danyalahmed1995 asked whether validation should be moved or reparsed JSDoc modifiers should skip grammar diagnostics for JS/JSX in [microsoft/TypeScript-go#4437](https://github.com/microsoft/TypeScript-go/issues/4437#issuecomment-4796606071)
    * @WoodyWoodsta provided additional debugging information in [microsoft/TypeScript-go#4441](https://github.com/microsoft/TypeScript-go/issues/4441#issuecomment-4800070354)
    * @freshp86 asked if the issue was fully addressed and provided example errors in [microsoft/TypeScript-go#928](https://github.com/microsoft/TypeScript-go/issues/928#issuecomment-4793937514)

## Activity Summary

### [Issue microsoft/TypeScript-go#3610](https://github.com/microsoft/TypeScript-go/issues/3610) (Closed, `Domain: API and Extensibility`, **andrewbranch**)

**API: additional Checker methods for transpiler consumers \(follow\-up to \#3403\)**

*Extend tsgo's IPC Checker with additional high-priority TypeChecker methods identified from transpiler usage data.*

 * (7 weeks ago) **andrewbranch** added label `Domain: API and Extensibility`, set milestone to `Post-7.0`, and assigned to **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#4208](https://github.com/microsoft/TypeScript-go/issues/4208) (Closed, `Needs Investigation`, **andrewbranch**)

**\`isSourceFile\(\)\` is missing in the API**

*The project lacks an isSourceFile() type guard in the API despite having a SourceFile interface.*

 * **RyanCavanaugh** added label `Needs Investigation`
 * (2 weeks ago) **mrazauskas** closed the issue
 * (2 weeks ago) **mrazauskas** reopened the issue
 * **andrewbranch** assigned to **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#4218](https://github.com/microsoft/TypeScript-go/pull/4218) (Open, `Voight-Kampff Anomaly`)

**Allow lone & in Unicode sets regexp classes**

*Update native scanner to allow lone & in Unicode Set regex character classes while preserving && intersections.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4218#issuecomment-4782196616) **Ijtihed** expressed appreciation for the label and asked for an explanation
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4218#issuecomment-4782550377) **RyanCavanaugh** explained that the label is applied to high-PR contributors under the bulk contributors policy and asked why the user decided to fix that particular issue
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4218#issuecomment-4785998449) **Ijtihed** explained that they were a junior engineer who picked the issue to learn after browsing rather than from personal need
 * [today](https://github.com/microsoft/TypeScript-go/pull/4218#issuecomment-4792508870) **RyanCavanaugh** said "@graphemecluster in case you want to see it"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4218#issuecomment-4796094461) **graphemecluster** noted the small fix looked fine but mentioned preferring to port PR #62716 if its scope met expectations

### [Issue microsoft/TypeScript-go#4230](https://github.com/microsoft/TypeScript-go/issues/4230) (Closed, `documentation`)

**Behavior difference: tsgo no longer infer variadic \`args\` type when \`arguments\[\.\.\.\]\` is referenced inside plain js function body**

*tsgo no longer infers variadic args in plain JS functions referencing 'arguments', causing missing rest parameter types.*

 * **RyanCavanaugh** added to milestone `Possible Improvement`
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/4230#issuecomment-4654215064) **ahejlsberg** said "@RyanCavanaugh Agreed. Specifically, in Strada, when a function body references arguments somewhere in an expression, we include a ...args parameter. We no longer do this in Corsa."
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/4230#issuecomment-4656519612) **hkleungai** asked if it was possible to add it back to TS7 and explained issues with arguments inference and jsdoc typing errors
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript-go#4239](https://github.com/microsoft/TypeScript-go/pull/4239) (Open, `No linked issue`)

**Replace ForEachReturnStatement closure with direct kind\-switched walk**

*Replace ForEachReturnStatement closure with a direct kind-switched recursive function to reduce allocations and improve performance.*

 * (today) **mds-ant** closed the issue
 * (today) **DanielRosenwasser** reopened the issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/4239#issuecomment-4790862837) **DanielRosenwasser** said "We're actually not convinced it's a regression - the benchmarking infra has a lot of noise."
 * [today](https://github.com/microsoft/TypeScript-go/pull/4239#issuecomment-4791564716) **jakebailey** said "@typescript-bot perf test this"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4239#issuecomment-4791565226) **typescript-automation[bot]** notified that performance test jobs had started and would update the comment with build status and results
 * [today](https://github.com/microsoft/TypeScript-go/pull/4239#issuecomment-4791792033) **typescript-automation[bot]** reported the results of the requested performance run with detailed comparison metrics

### [Issue microsoft/TypeScript-go#4254](https://github.com/microsoft/TypeScript-go/issues/4254) (Open, `Needs Investigation`, **weswigham**)

**Behavior difference: Notable inconsistencies on type inference for expando arrow function imports**

*Inconsistent handling of expando arrow function imports between tsc and tsgo results in verbose in-place type redefinitions instead of reusing imported component types.*

 * created by **hkleungai**
 * (2 weeks ago) **RyanCavanaugh** added label `Needs Investigation`, and set milestone to `Post-7.0`
 * **weswigham** assigned to **weswigham**

### [Issue microsoft/TypeScript-go#4347](https://github.com/microsoft/TypeScript-go/issues/4347) (Closed)

**CPU usage spikes to 80% to 100% when using \`tsgo \-\-lsp \-\-stdio\`**

*tsgo's LSP process uses 80-100% CPU when typing in TypeScript files larger than 100 lines*

 * **DanielRosenwasser** added label `Needs More Info`
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/4347#issuecomment-4756988233) **epicmet** confirmed that Typescript 6 didn't reproduce the issue, described CPU usage increase with a large file, and provided performance trace files
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/4347#issuecomment-4762549382) **epicmet** identified the root cause as complex node-redis types causing CPU spikes in the TS LSP with Neovim and noted VSCode fared better
 * **RyanCavanaugh** removed label `Needs More Info`
 * [today](https://github.com/microsoft/TypeScript-go/issues/4347#issuecomment-4791728842) **RyanCavanaugh** said "Thanks! The CPU spikes are definitely a lot easier to notice when the server is capable of using all cores. Makes sense."
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#4349](https://github.com/microsoft/TypeScript-go/pull/4349) (Closed)

**Collate\-free import sorting**

*Introduce a collate-free import sorting scheme with customizable ordinal and natural case options to replace and deprecate x/text/collate dependency*

 * created by **jakebailey**
 * **jakebailey** added to milestone `TypeScript 7.0 Stable`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4359](https://github.com/microsoft/TypeScript-go/issues/4359) (Open, `Domain: Editor`, **jakebailey**, **Copilot**)

**Missing some completion and hover document in namespaced JSX intrinsic element**

*VSCode’s TypeScript JSX support lacks attribute completions and hover documentation for namespaced JSX intrinsic elements like foo:bar*

 * **hjkcai** added label `Domain: Editor`
 * (6 days ago) **jakebailey** assigned to **Copilot**, **jakebailey**
 * **RyanCavanaugh** added to milestone `Post-7.0`

### [Issue microsoft/TypeScript-go#4370](https://github.com/microsoft/TypeScript-go/issues/4370) (Open, `Domain: Editor`, **jakebailey**, **Copilot**)

**\`js/ts\.preferences\.useAliasesForRenames\` not respected**

*Disabling js/ts.preferences.useAliasesForRenames has no effect in VS Code’s native TypeScript extension, causing renamed imports to be aliased rather than updated at their source.*

 * **LiamMorrow** added label `Domain: Editor`
 * (6 days ago) **jakebailey** assigned to **Copilot**, **jakebailey**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 Stable`

### [PR microsoft/TypeScript-go#4371](https://github.com/microsoft/TypeScript-go/pull/4371) (Closed, **jakebailey**, **Copilot**)

**Respect useAliasesForRenames in rename edits**

*Rename edits now honor the useAliasesForRenames preference, renaming exported symbols directly when disabled instead of introducing import aliases.*

 * created by **Copilot**
 * (6 days ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 Stable`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4373](https://github.com/microsoft/TypeScript-go/issues/4373) (Open, `Needs Investigation`, **johnfav03**)

**Project\-reference redirect fails for directory \(\`index\.ts\`\) subpaths of symlinked packages**

*Importing a directory subpath from a symlinked, unbuilt project-reference package fails to resolve to source with TS2307.*

 * created by **sverrejoh**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `Post-7.0`, and assigned to **johnfav03**

### [PR microsoft/TypeScript-go#4374](https://github.com/microsoft/TypeScript-go/pull/4374) (Closed)

**Resolve symlinked project\-reference directory \(\`index\.ts\`\) subpaths to source**

*Fix regression causing directory subpath imports in symlinked project references to fail by lazily registering package symlinks.*

 * created by **sverrejoh**
 * (later) **sverrejoh** closed the issue

### [Issue microsoft/TypeScript-go#4378](https://github.com/microsoft/TypeScript-go/issues/4378) (Open, `Needs Investigation`, **johnfav03**)

**\`tsgo \-\-watch\` error: "error starting FSEvents stream" on large \`node\_modules\` since the fswatch rewrite**

*tsgo watch mode fails to initiate its file watcher on large node_modules directories after the fswatch rewrite in recent 7.0.0-dev builds*

 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/4378#issuecomment-4755443201) **Alex-Bond** confirmed compiling and running with commit ce359c1
 * (yesterday) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **johnfav03**
 * **RyanCavanaugh** added to milestone `Post-7.0`

### [PR microsoft/TypeScript-go#4379](https://github.com/microsoft/TypeScript-go/pull/4379) (Open)

**Fix watch coalescing for FSEvents**

*Coalesce dense directory watch sets into recursive ancestor watches on FSEvents and Windows to reduce per-directory streams.*

 * created by **jakebailey**
 * [5 days ago](https://github.com/microsoft/TypeScript-go/pull/4379#issuecomment-4754939213) **jakebailey** said "This is doing this in the layer above fswatch, but, going to try and shove it down..."
 * [today](https://github.com/microsoft/TypeScript-go/pull/4379#issuecomment-4791961250) **jakebailey** suggested coalescing subdirectory watches into a single watch to reduce resource issues at the cost of extra events and asked about using kqueue as a fallback on errors
 * [today](https://github.com/microsoft/TypeScript-go/pull/4379#issuecomment-4792027145) **andrewbranch** said "The other option is to move this into app logic, like the LSP watcher does unconditionally today and conditionally in https://github.com/andrewbranch/typescript-go/tree/lsp-builtin-watcher-granular."
 * [today](https://github.com/microsoft/TypeScript-go/pull/4379#issuecomment-4792161072) **jakebailey** mentioned having implemented it originally but preferring to push down for transparency and indicated needing to optimize the kqueue backend
 * [today](https://github.com/microsoft/TypeScript-go/pull/4379#issuecomment-4792175080) **andrewbranch** said "In my experience, kqueue is untenable for the scale of watches we often try to register. I profiled it and it was all syscall time. Nothing to optimize."
 * [today](https://github.com/microsoft/TypeScript-go/pull/4379#issuecomment-4792182748) **andrewbranch** said "I guess, registering them in parallel would probably help, but I still don't think that's a good approach."
 * [today](https://github.com/microsoft/TypeScript-go/pull/4379#issuecomment-4792202888) **jakebailey** said "Ultimately, I guess my question is why Strada did not have major issues here, given it could only use kqueue as Node via libuv only did not do fsevents."

### [Issue microsoft/TypeScript-go#4380](https://github.com/microsoft/TypeScript-go/issues/4380) (Open, `Needs Investigation`, **johnfav03**)

**\[ServerErrors\]\[TypeScript\] main vs **

*Server errors occurred in the TypeScript main branch pipeline while analyzing 300 popular GitHub repositories, causing timeouts and other failures.*

 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/4380#issuecomment-4755503460) **typescript-automation[bot]** reported a server connection closed prematurely with undefined for the babel/babel repository
 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/4380#issuecomment-4755503486) **typescript-automation[bot]** reported a server connection closed prematurely error for nuxt/nuxt
 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/4380#issuecomment-4755503508) **typescript-automation[bot]** reported that the server connection closed prematurely and provided error logs, affected repository details, recent request traces, and reproduction steps
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `Post-7.0`, and assigned to **johnfav03**

### [Issue microsoft/TypeScript-go#4381](https://github.com/microsoft/TypeScript-go/issues/4381) (Open, **jakebailey**, **Copilot**)

**Behavior difference: \`\.state\` emit is missing on react component**

*tsgo incorrectly omits emitting React component state initializations inside constructors for JavaScript files, unlike tsc.*

 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/4381#issuecomment-4766499771) **hkleungai** said "Ohh, that. I believe it is existing tsc behaviors on js file, before tsgo happens."
 * (2 days ago) **jakebailey** assigned to **Copilot**, **jakebailey**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 Stable`

### [PR microsoft/TypeScript-go#4382](https://github.com/microsoft/TypeScript-go/pull/4382) (Closed)

**fix\(relater\): add property comparison cache fast path to avoid false TS2321**

*Add a relation-cache fast path in property-type comparisons to avoid false TS2321 errors for large object literals*

 * [4 days ago](https://github.com/microsoft/TypeScript-go/pull/4382#issuecomment-4758527237) **jakebailey** stated that they were not going to be raising any limits
 * [4 days ago](https://github.com/microsoft/TypeScript-go/pull/4382#issuecomment-4758968472) **maoger** removed the stack depth limit change, relied on a relation-cache fast path to avoid redundant stack pushes, confirmed tests passed and baseline unaffected, and marked the PR ready for review
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/4382#issuecomment-4770428841) **jakebailey** asked about the origin and rationale of the change, its presence in TS 6, the absence of an issue, real-codebase experience, and AI-assistance disclosure
 * (today) **maoger** closed the issue

### [Issue microsoft/TypeScript-go#4392](https://github.com/microsoft/TypeScript-go/issues/4392) (Open, `Crash`, **DanielRosenwasser**, **andrewbranch**, **Copilot**)

**panic: cache entry not found \[recovered, repanicked\]**

*TypeScript server v7.0.0-dev panics with 'cache entry not found' while handling file open and config updates.*

 * **motopods** added label `Crash`
 * (2 days ago) **DanielRosenwasser** assigned to **Copilot**, **DanielRosenwasser**
 * (today) **RyanCavanaugh** set milestone to `TypeScript 7.0 Stable`, and assigned to **andrewbranch**

### [PR microsoft/TypeScript-go#4400](https://github.com/microsoft/TypeScript-go/pull/4400) (Closed, **DanielRosenwasser**, **andrewbranch**, **Copilot**)

**Fix parse cache ref race during cloned program updates**

*Implements new parse-cache reference methods to avoid race conditions and panics when cloned programs reuse SourceFile pointers.*

 * created by **Copilot**
 * (2 days ago) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * **RyanCavanaugh** assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4400#issuecomment-4792536065) **andrewbranch** argued that snapshots should never be cloned after release and asserted that a credible fix requires reproducing the crash in a real project.Session test, rejecting band-aid solutions
 * [today](https://github.com/microsoft/TypeScript-go/pull/4400#issuecomment-4792709823) **Copilot** reverted unsupported parse-cache refcount changes in f23fd187d and left refcount cache behavior unchanged due to lack of a real project.Session reproduction
 * [today](https://github.com/microsoft/TypeScript-go/pull/4400#issuecomment-4792838774) **andrewbranch** said "Very good PR now, approved"
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#4403](https://github.com/microsoft/TypeScript-go/issues/4403) (Closed, `bug`, **jakebailey**)

**Regression: CJS emit drops namespace qualifier on RHS of module\-scope \`export const { … } = importedValue\` → ReferenceError**

*Module-scope export const destructuring in CommonJS emit drops the import namespace qualifier and causes a ReferenceError.*

 * created by **thaoula**
 * **jakebailey** assigned to **jakebailey**
 * (today) **RyanCavanaugh** added label `bug`, and set milestone to `TypeScript 7.0 Stable`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4404](https://github.com/microsoft/TypeScript-go/pull/4404) (Closed)

**Fix CommonJS export destructuring emit**

*Correct the code generation for destructured exports in CommonJS modules.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4405](https://github.com/microsoft/TypeScript-go/issues/4405) (Open, `Needs Investigation`, **andrewbranch**)

**App using programmatic APIs fails to typecheck with \`exactOptionalPropertyTypes: true\` and \`@types/node\` v24**

*With exactOptionalPropertyTypes enabled and @types/node v24 installed, programmatic API imports fail to compile due to type incompatibilities.*

 * created by **mrazauskas**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `Post-7.0`, and assigned to **andrewbranch**

### [Issue microsoft/TypeScript-go#4408](https://github.com/microsoft/TypeScript-go/issues/4408) (Open, `Needs More Info`)

**Regression: recursive conditional\+mapped "serialize" type no longer proves \`Transform\<X\>\` assignable to \`X\` on deeply\-nested compound types \(native\-preview; works in tsc\)**

*A regression in @typescript/native-preview fails to prove recursive mapped serialize types as identity for deeply nested compound types.*

 * created by **dimofeev**
 * **jakebailey** assigned to **ahejlsberg**
 * (today) **RyanCavanaugh** added labels `Needs Investigation`, `Needs More Info`, removed label `Needs Investigation`, and unassigned **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4408#issuecomment-4792026808) **RyanCavanaugh** requested a concrete repro and suggested using the reduce-repro skill in an AI agent
 * **RyanCavanaugh** added to milestone `Need More Info`

### [Issue microsoft/TypeScript-go#4411](https://github.com/microsoft/TypeScript-go/issues/4411) (Open, `Domain: Editor`, **DanielRosenwasser**, **Copilot**)

**\`isolatedDeclarations\` quick\-fix cannot consistently use auto\-imports**

*IsolatedDeclarations quick-fix fails to auto-import missing types when no existing import is present*

 * (yesterday) **DanielRosenwasser** added label `Domain: Editor`, and assigned to **Copilot**, **DanielRosenwasser**
 * **RyanCavanaugh** added to milestone `Post-7.0`

### [PR microsoft/TypeScript-go#4421](https://github.com/microsoft/TypeScript-go/pull/4421) (Closed)

**Add \`arguments\` inference removal to CHANGES\.md**

*Document removal of arguments type inference in CHANGES.md.*

 * created by **weswigham**
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript-go#4423](https://github.com/microsoft/TypeScript-go/pull/4423) (Closed)

**Fix macOS lspwatcher missing directory recovery**

*Add a macOS lspwatcher missing directory recovery workaround and verify its compatibility on Windows*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4423#issuecomment-4793914706) **jakebailey** said "Superseded by #4379"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4424](https://github.com/microsoft/TypeScript-go/pull/4424) (Closed)

**\[api\] Add missing checker methods**

*Adds missing checker methods by porting JSDoc tag retrieval from Strada to return text as strings.*

 * created by **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#4426](https://github.com/microsoft/TypeScript-go/issues/4426) (Open, `Crash`, **andrewbranch**)

**Panic \(Unhandled case in Type\.Types\) in checker\.Type\.Types for non\-union types \(e\.g\. string\) via the API getTypes\(\)**

*Calling getTypes() on non-union types like string through the API causes an unhandled case panic in Type.Types due to missing guard.*

 * created by **UditDewan**
 * **UditDewan** added label `Crash`
 * (today) **RyanCavanaugh** set milestone to `Post-7.0`, and assigned to **andrewbranch**

### [Issue microsoft/TypeScript-go#4428](https://github.com/microsoft/TypeScript-go/issues/4428) (Open, `Domain: Editor`, **DanielRosenwasser**, **Copilot**)

**\`js/ts\.reportStyleChecksAsWarnings\` is not respected**

*TypeScript 7.0 in VS Code ignores js/ts.reportStyleChecksAsWarnings and always marks unused variables as warnings.*

 * (today) **DanielRosenwasser** added label `Domain: Editor`, and assigned to **Copilot**, **DanielRosenwasser**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 Stable`

### [PR microsoft/TypeScript-go#4429](https://github.com/microsoft/TypeScript-go/pull/4429) (Closed, **DanielRosenwasser**, **Copilot**)

**Fix \`js/ts\.reportStyleChecksAsWarnings\` not being read from VS Code config**

*Add missing config annotation and tests so VS Code js/ts.reportStyleChecksAsWarnings setting is correctly parsed*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#4431](https://github.com/microsoft/TypeScript-go/pull/4431) (Closed)

**API: add checker methods to get true and false types of a conditional type**

*Add API checker methods to fetch true and false branches of a conditional type.*

 * created by **piotrtomiak**
 * **RyanCavanaugh** added to milestone `Post-7.0`

### [Issue microsoft/TypeScript-go#4432](https://github.com/microsoft/TypeScript-go/issues/4432) (Closed)

**\[TS7\] Destructured parameter of an optional function\-typed property loses its contextual type \(spurious TS2322\)**

*Optional function property’s destructured parameter loses its contextual type in TS7, triggering a spurious TS2322 error.*

 * created by **jonnylynchy**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4432#issuecomment-4793899555) **RyanCavanaugh** said "7.0 is intended to match 6.0, which it does (they both issue this error). I'm not sure what delta between 5.8 and 6.0 is relevant here but it's not a typescript-go bug."
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#4433](https://github.com/microsoft/TypeScript-go/pull/4433) (Closed)

**Produce npm packages to release in stages**

*Enable staged npm package releases by generating unordered tarball directories for compatibility with the new publishing mechanism.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4434](https://github.com/microsoft/TypeScript-go/pull/4434) (Closed)

**Generate isSourceFile, fix updateSourceFile/cloneNode/getSynthesizedDeepClone for SourceFiles**

*Added isSourceFile generation, corrected SourceFile cloning/update methods, and fixed redundant RemoteSourceFile array instantiation.*

 * created by **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#4435](https://github.com/microsoft/TypeScript-go/issues/4435) (Closed, `Working As Intended`)

**Different diagnostics and exit code vs tsc for tsconfig using extends \+ baseUrl \+ wildcard paths**

*Classic tsc and typescript-go yield different diagnostics and exit codes for tsconfigs using extends with baseUrl and wildcard paths.*

 * created by **safal207**
 * **RyanCavanaugh** added label `Working As Intended`
 * [today](https://github.com/microsoft/TypeScript-go/issues/4435#issuecomment-4793933260) **RyanCavanaugh** clarified that the deprecated option was removed and behavior change was expected
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#4436](https://github.com/microsoft/TypeScript-go/pull/4436) (Closed)

**Add \`program\.getSourceFileNames\`, \`checker\.getApparentType\`, \`checker\.getImmediateAliasedSymbol\`, \`checker\.getMemberInModuleExports\`, and \`Type\` type guards**

*Add program.getSourceFileNames, checker.getApparentType, checker.getImmediateAliasedSymbol, checker.getMemberInModuleExports, and Type type guards to the TypeScript compiler API.*

 * created by **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#4437](https://github.com/microsoft/TypeScript-go/issues/4437) (Open)

**\`checkJs\` seems to default to true erroneously**

*tsgo implicitly enables checkJs by default, leading to erroneous JSDoc modifier errors in JavaScript files unless checkJs is explicitly disabled.*

 * created by **freshp86**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4437#issuecomment-4794108129) **jakebailey** said "I think part of the confusion is that IIRC these are now early errors in the reparse process, at parse time, not even check errors. Perhaps they should move"
 * [today](https://github.com/microsoft/TypeScript-go/issues/4437#issuecomment-4794121041) **freshp86** asked why certain errors were suppressed when checkJs was false despite explicit configuration
 * [today](https://github.com/microsoft/TypeScript-go/issues/4437#issuecomment-4796606071) **danyalahmed1995** noted that the errors occur during the JSDoc reparse process and asked whether validation should move or reparsed JSDoc modifiers should skip grammar diagnostics for JS/JSX

### [PR microsoft/TypeScript-go#4438](https://github.com/microsoft/TypeScript-go/pull/4438) (Open)

**\[api\] Tighten client\-side type safety of Type subtypes**

*Adjust Type subtype methods to return undefined instead of throwing on unsafe casts and narrow overly broad client-side type definitions.*

 * created by **andrewbranch**

### [Issue microsoft/TypeScript-go#4439](https://github.com/microsoft/TypeScript-go/issues/4439) (Open, `bug`, **andrewbranch**, **Copilot**)

**Feature Request: Permit backward\-compatible version checks at main export**

*Add a main package export for TypeScript 7 to enable backward-compatible version checks and avoid load errors.*

 * created by **kirkwaiblinger**

### [PR microsoft/TypeScript-go#4440](https://github.com/microsoft/TypeScript-go/pull/4440) (Open)

**API: add getChildren and token getters to Node**

*Extend the Node API with getChildren, getChildCount, getChildAt, getFirstToken, and getLastToken methods.*

 * created by **oMatheusmol**

### [Issue microsoft/TypeScript-go#4441](https://github.com/microsoft/TypeScript-go/issues/4441) (Open)

**\`tsgo \-\-watch\` fails to start stream if you run watch instances in parallel**

*Running multiple tsgo --watch processes in parallel on different pnpm workspace packages causes FSEvents stream errors after the first instance.*

 * created by **WoodyWoodsta**
 * [later](https://github.com/microsoft/TypeScript-go/issues/4441#issuecomment-4799973021) **jakebailey** said "This is happening when you run multiple tsc invocations?"
 * [later](https://github.com/microsoft/TypeScript-go/issues/4441#issuecomment-4800016780) **jakebailey** linked a related issue and noted uncertainty about resolving cross-process watcher limits, observing no similar reports in VS Code
 * [later](https://github.com/microsoft/TypeScript-go/issues/4441#issuecomment-4800070354) **WoodyWoodsta** described testing two packages in different sequences and observed that the second invocation always failed, even when the packages were unrelated

### [PR microsoft/TypeScript-go#4442](https://github.com/microsoft/TypeScript-go/pull/4442) (Open, **RyanCavanaugh**, **Copilot**)

**Fix false implicit\-return/unreachable diagnostics in \`try/finally\` with logical assignment \(\`\|\|=\`\)**

*Adjust TypeScript’s reachability caching to prevent erroneous missing-return and unreachable-code diagnostics in try/finally blocks using logical assignment.*

 * created by **Copilot**
 * (later) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * [later](https://github.com/microsoft/TypeScript-go/pull/4442#issuecomment-4800960525) **RyanCavanaugh** said "@typescript-bot test top999"
 * [later](https://github.com/microsoft/TypeScript-go/pull/4442#issuecomment-4800961276) **typescript-automation[bot]** reported starting build jobs with initial status for test top999

### [PR microsoft/TypeScript-go#4443](https://github.com/microsoft/TypeScript-go/pull/4443) (Open)

**Fixed build mode false negative from export\-star facade**

*Fix false negative TypeScript build-mode error caused by export-star facade usage.*

 * created by **johnfav03**

### [Issue microsoft/TypeScript-go#928](https://github.com/microsoft/TypeScript-go/issues/928) (Closed)

**checkJs default has changed in tsgo**

*The TypeScript Go implementation now defaults checkJs to true instead of false, and it is unclear if that change was intentional.*

 * [1 year ago](https://github.com/microsoft/TypeScript-go/issues/928#issuecomment-2915302531) **glenjamin** reported seeing the same behaviour with allowJs and checkJs settings and offered to provide more information
 * [1 year ago](https://github.com/microsoft/TypeScript-go/issues/928#issuecomment-2916957858) **jakebailey** said "What errors are you seeing specifically? I believe I'll have fixed this in #930 when merged. You could build from that PR and check, too."
 * (1 year ago) **jakebailey** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/issues/928#issuecomment-4793937514) **freshp86** asked if the issue was fully addressed and provided example errors from the Chromium codebase
 * [today](https://github.com/microsoft/TypeScript-go/issues/928#issuecomment-4793949616) **jakebailey** said "We closed it as fixed a year ago, so if something is not working for you, please file a new issue"
 * [today](https://github.com/microsoft/TypeScript-go/issues/928#issuecomment-4793965954) **freshp86** said "Sure, let me attempt creating a minimal repro and will file a new bug to track."
 * [today](https://github.com/microsoft/TypeScript-go/issues/928#issuecomment-4794028844) **freshp86** said "Filed https://github.com/microsoft/typescript-go/issues/4437. Let's continue the discussion there. Thanks!"

