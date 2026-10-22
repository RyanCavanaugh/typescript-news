# Report for 2026-10-20 (Tuesday, October 20th, 2026)

32 different users commented on 56 different issues.

## Recommended Actions

 * Response Recommended
    * @jaydenfyi provided a workaround for JSON const behavior and linked the content mapper implementation in [microsoft/TypeScript#32063](https://github.com/microsoft/TypeScript/issues/32063#issuecomment-6312789386)
    * @BananaAcid asked if it had been implemented in any capacity in [microsoft/TypeScript#32830](https://github.com/microsoft/TypeScript/issues/32830#issuecomment-6319176762)
    * @lishaduck asked if the API surface was frozen after the beta release and if further changes remained possible in [microsoft/TypeScript#64040](https://github.com/microsoft/TypeScript/pull/64040#issuecomment-6300165939)
    * @salemkode provided repro steps and error details in [microsoft/TypeScript#64605](https://github.com/microsoft/TypeScript/issues/64605#issuecomment-6299246463)
    * @rajnish-verma-22172 offered to work on the issue and outlined a plan in [microsoft/TypeScript#64742](https://github.com/microsoft/TypeScript/issues/64742#issuecomment-6308382258)
    * @jclaessens97 provided repro steps as requested in [microsoft/TypeScript#64757](https://github.com/microsoft/TypeScript/issues/64757#issuecomment-6318384069)
    * @kennysarnoski-jarvis provided reproduction results and analysis in [microsoft/TypeScript#64757](https://github.com/microsoft/TypeScript/issues/64757#issuecomment-6319872131)
    * @damerlanaga99-source provided debug configuration snippet in [microsoft/TypeScript#64889](https://github.com/microsoft/TypeScript/issues/64889#issuecomment-6311453284)
    * @microsoft-github-policy-service requested CLA agreement in [microsoft/TypeScript#64894](https://github.com/microsoft/TypeScript/pull/64894#issuecomment-6309091346)

## Activity Summary

### [Issue microsoft/TypeScript#32063](https://github.com/microsoft/TypeScript/issues/32063) (Open, `Suggestion`, `Awaiting More Feedback`)

**import ConstJson from '\./config\.json' as const;**

*Allow importing a JSON config file with a const modifier to infer literal union types for its values.*

 * [15 weeks ago](https://github.com/microsoft/TypeScript/issues/32063#issuecomment-4883967601) **james-pre** explained how to use npm v12's built-in dependency patching to patch TypeScript by adding a patchedDependencies entry in package.json and linking to a gist-hosted patch file
 * [15 weeks ago](https://github.com/microsoft/TypeScript/issues/32063#issuecomment-4885857717) **Chinoman10** described how to use npm’s built-in dependency patching in v12 to apply a TypeScript patch and noted that Bun’s patch feature is faster
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/32063#issuecomment-6055145510) **michaelhazan** noted that TypeScript 7's go compiler prevented previous patching and asked why the feature wasn't part of TypeScript
 * [later](https://github.com/microsoft/TypeScript/issues/32063#issuecomment-6312789386) **jaydenfyi** recommended using .json5 via motherload after TS broke const.json support and provided a TS 7.1 content mapper workaround with a GitHub link

### [Issue microsoft/TypeScript#32830](https://github.com/microsoft/TypeScript/issues/32830) (Open, `Suggestion`, `Awaiting More Feedback`)

**Configure from package\.json**

*Support configuring TypeScript compiler options and project settings in package.json to declutter project roots.*

 * [2.3 years ago](https://github.com/microsoft/TypeScript/issues/32830#issuecomment-2168509098) **pgbradbury** advised that critics could opt out and argued that the request only added an option rather than enforcing a style
 * [2.3 years ago](https://github.com/microsoft/TypeScript/issues/32830#issuecomment-2168741545) **ljharb** described being forced to download the tsconfig twice due to package.json config
 * [2.3 years ago](https://github.com/microsoft/TypeScript/issues/32830#issuecomment-2169026994) **cobaltt7** suggested passing package.json through a build step to remove extra keys and minify it, allowing tsconfig to be included
 * [later](https://github.com/microsoft/TypeScript/issues/32830#issuecomment-6319176762) **BananaAcid** said "was it implemented in any capacity by now?"

### [Issue microsoft/TypeScript#63703](https://github.com/microsoft/TypeScript/issues/63703) (Open, `Planning`)

**TypeScript 7\.1 Iteration Plan**

*Roadmap for TypeScript 7.1 detailing milestones and features across compiler, editor productivity, and performance enhancements.*

 * [yesterday](https://github.com/microsoft/TypeScript/issues/63703#issuecomment-6276787389) **typescript-automation[bot]** provided build status update
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63703#issuecomment-6276993692) **typescript-automation[bot]** said "Hey, @DanielRosenwasser! I've pulled main into release-7.1 for you."
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63703#issuecomment-6285163659) **erlichmen** asked when the 7.1.0-beta artifacts would be published and if users needed to build from the release-7.1 branch
 * [today](https://github.com/microsoft/TypeScript/issues/63703#issuecomment-6297602298) **DanielRosenwasser** announced the beta release and creation of the v7.1-beta tag

### [PR microsoft/TypeScript#64040](https://github.com/microsoft/TypeScript/pull/64040) (Open, `For Uncommitted Bug`)

**Replace Node interface with discriminated unions **

*Replace the Node interface with discriminated union types for improved type safety.*

 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [7 weeks ago](https://github.com/microsoft/TypeScript/pull/64040#issuecomment-5471848926) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [7 weeks ago](https://github.com/microsoft/TypeScript/pull/64040#issuecomment-5474929267) **typescript-automation[bot]** said "The TypeScript team hasn't accepted the linked issue #56275. If you can get it accepted, this PR will have a better chance of being reviewed."
 * [today](https://github.com/microsoft/TypeScript/pull/64040#issuecomment-6300165939) **lishaduck** said "Now that the beta is out, is the API surface effectively frozen? Is this still a possibility?"

### [PR microsoft/TypeScript#64169](https://github.com/microsoft/TypeScript/pull/64169) (Open, `For Backlog Bug`)

**Preserve \`\<\` in \`getChildren\(\)\` when type arguments begin with \`\<\`**

*Update getChildren() to preserve the leading “<” token when type arguments begin with “<”*

 * (6 weeks ago) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64169#issuecomment-6156966758) **jakebailey** said "Is there an equivalent to this in Corsa?"
 * [later](https://github.com/microsoft/TypeScript/pull/64169#issuecomment-6314625081) **Andarist** said "@jakebailey i doublechecked with Strada and it had the same bug"

### [Issue microsoft/TypeScript#64431](https://github.com/microsoft/TypeScript/issues/64431) (Open, `Bug`, **RyanCavanaugh**, **Copilot**)

**TS7031 false positive for nested object binding pattern with \`= {}\` default in an annotated parameter \(regression from \#64043\)**

*Nested object destructuring with default {} in a typed parameter erroneously triggers TS7031 errors after PR #64043*

 * (3 weeks ago) **RyanCavanaugh** assigned to **Copilot**, **RyanCavanaugh**
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/64431#issuecomment-6041533127) **Konan69** described contextually typed parameters triggering TS7031 errors in recent nightly, validated that #64440 removes the errors, suggested adding test cases, and opened #64671 with an alternative patch
 * [today](https://github.com/microsoft/TypeScript/issues/64431#issuecomment-6297398470) **connorshea** mentioned encountering the same regression when using typescript@next, noting it did not occur in their 7.0 dev release but appeared in ts 7.1

### [PR microsoft/TypeScript#64586](https://github.com/microsoft/TypeScript/pull/64586) (Closed, `For Backlog Bug`)

**Restore index signature details in property hovers**

*Restore index signature details in TypeScript property hover tooltips to show key and value type information.*

 * (2 weeks ago) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64586#issuecomment-6154874697) **jakebailey** said "This PR needs a merge from main"
 * [later](https://github.com/microsoft/TypeScript/pull/64586#issuecomment-6314725767) **Andarist** said "@jakebailey done"

### [Issue microsoft/TypeScript#64605](https://github.com/microsoft/TypeScript/issues/64605) (Open, `Needs Investigation`, **gabritto**)

**TS5115 in published Zod 4\.5–4\.6 types after \#64372**

*Zod 4.5.0–4.6.5 z.json() types cause TS5115 infinite circularity errors in TypeScript 7.1 nightlies after PR #64372, impacting ~62M weekly downloads.*

 * **RyanCavanaugh** assigned to **gabritto**
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/64605#issuecomment-6053406731) **RedesignedRobot** traced the cause of a recursive member resolution issue introduced by #64372, proposed a fix that preserves declared members on a stack during inheritance resolution, reported passing tests and a cleaned-up baseline, and offered to open a PR
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/64605#issuecomment-6084855435) **rsnodgrass** confirmed the issue reproduced with TypeScript 7.1.0-dev and Zod 4.6.5, provided minimal reproduction code and version comparison, and requested review
 * [today](https://github.com/microsoft/TypeScript/issues/64605#issuecomment-6299246463) **salemkode** confirmed reproduction on typescript@7.1.0-beta with a standalone zod example and provided reproduction steps and error output

### [PR microsoft/TypeScript#64679](https://github.com/microsoft/TypeScript/pull/64679) (Open, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Add snapshot\.rebase\(newBaseSnapshot, changes\)**

*Add snapshot.rebase(newBaseSnapshot, changes) to overlay synthetic filesystem changes from an old snapshot onto a new one.*

 * (1 week ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64679#issuecomment-6279317955) **andrewbranch** suggested renaming the API to use snapshot.update({ fileSystem: ... }) with createFileSystemWithBase for layering synthetic file system updates
 * [today](https://github.com/microsoft/TypeScript/pull/64679#issuecomment-6302584141) **weswigham** asked which additional data should be merged in a snapshot "rebase" and noted that reusing ASTs would require reworking program construction
 * [today](https://github.com/microsoft/TypeScript/pull/64679#issuecomment-6303338637) **andrewbranch** described concerns about ambiguity in the rebase API's unspecified base snapshot and potential confusion when using it on non-LSP snapshots

### [Issue microsoft/TypeScript#64707](https://github.com/microsoft/TypeScript/issues/64707) (Open, `Bug`)

**JSDoc\-generated namespaces not merged with default exports**

*TypeScript does not merge JSDoc-created namespaces into default-exported classes, resulting in unresolved namespace member errors.*

 * created by **donmccurdy**
 * **RyanCavanaugh** added label `Bug`

### [Issue microsoft/TypeScript#64708](https://github.com/microsoft/TypeScript/issues/64708) (Open, `Bug`)

**Unbounded memory in declaration emit for an inferred type built from non\-exported recursive aliases \(also hit by \`\-\-noEmit \-\-watch\`\)**

*TypeScript's declaration emit and watch mode trigger unbounded memory growth when inferring exported types from non-exported recursive aliases.*

 * created by **mattleonowicz**
 * **RyanCavanaugh** added label `Bug`

### [Issue microsoft/TypeScript#64715](https://github.com/microsoft/TypeScript/issues/64715) (Closed, `Fixed`)

**\`\-\-incremental\` keeps stale diagnostics after a change in a \`declare global\` block of a package declaration file \(7\.0\.2, regression from 6\.0\.3\)**

*TypeScript’s --incremental retains stale errors after modifying declare global block in a package .d.ts file, regressing from v6.0.3 to v7.0.2.*

 * created by **plum117**
 * [later](https://github.com/microsoft/TypeScript/issues/64715#issuecomment-6319369187) **RyanCavanaugh** said "This seems to be fixed in latest - I can confirm the repro on 7.0 but not 7.1-nightly."
 * **RyanCavanaugh** added label `Fixed`
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#64719](https://github.com/microsoft/TypeScript/issues/64719) (Open, `Possible Improvement`)

**\`export \*\` resolution allocates per re\-exported name, slowing checks of barrels over large modules**

*Per-name allocations during export * resolution cause excessive memory allocations and significant slowdowns when type-checking large barrel chains.*

 * created by **gwkline**
 * (later) **RyanCavanaugh** added label `Possible Improvement`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#64720](https://github.com/microsoft/TypeScript/issues/64720) (Closed)

**Declaration diagnostics allocate a diagnostic selector closure for every declaration visited**

*Declaration diagnostics allocate a diagnostic selector closure for each visited declaration, causing performance overhead.*

 * created by **gwkline**
 * [today](https://github.com/microsoft/TypeScript/issues/64720#issuecomment-6295601315) **gwkline** said "Closing with #64723; the win is too small to pursue on its own."
 * (today) **gwkline** closed the issue

### [Issue microsoft/TypeScript#64721](https://github.com/microsoft/TypeScript/issues/64721) (Closed)

**Module specifier generation rescans package\.json \`exports\` and tsconfig \`paths\` for every importing file**

*Module specifier generation repeatedly rescans package.json exports and tsconfig paths per import, slowing declaration emit.*

 * created by **gwkline**
 * [today](https://github.com/microsoft/TypeScript/issues/64721#issuecomment-6295602190) **gwkline** said "Closing with #64724; withdrawn to keep focus on #64722."
 * (today) **gwkline** closed the issue

### [PR microsoft/TypeScript#64722](https://github.com/microsoft/TypeScript/pull/64722) (Open, `For Backlog Bug`)

**Merge export \* tables without per\-name collision trackers**

*Improve performance of export * by merging tables directly, pre-sizing them, and only tracking collisions when needed.*

 * created by **gwkline**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64722#issuecomment-6100021037) **gwkline** said "@microsoft-github-policy-service agree"
 * (later) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`

### [PR microsoft/TypeScript#64723](https://github.com/microsoft/TypeScript/pull/64723) (Closed, `For Uncommitted Bug`)

**Create declaration emit diagnostic selectors on demand**

*Delay creation of symbol accessibility diagnostic selectors until needed during declaration file emission to eliminate unnecessary allocations and improve performance.*

 * created by **gwkline**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64723#issuecomment-6295599026) **gwkline** said "Withdrawing: the time win is too small to justify reviewer attention on its own. Keeping #64722, which is the change that actually moves check time."
 * (today) **gwkline** closed the issue

### [PR microsoft/TypeScript#64724](https://github.com/microsoft/TypeScript/pull/64724) (Closed, `For Uncommitted Bug`)

**Cache exports lookups and path patterns in module specifier generation**

*Cache exports and paths lookups in the module specifier generator to reduce redundant resolution work.*

 * created by **gwkline**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64724#issuecomment-6295599958) **gwkline** said "Withdrawing to keep the review queue focused on #64722. The emit-side caching here is a larger host/interface change than the win warrants right now."
 * (today) **gwkline** closed the issue

### [Issue microsoft/TypeScript#64725](https://github.com/microsoft/TypeScript/issues/64725) (Open, `Bug`, **RyanCavanaugh**, **iisaduan**, **Copilot**)

**Crash \(nil pointer in getPropertyOfObjectType\) under \-\-noLib when a global import x = T\.m names a type**

*Compiler crashes with nil pointer dereference in getPropertyOfObjectType when using a global import alias for a type under --noLib*

 * created by **YuanchengJiang**
 * (later) **RyanCavanaugh** added label `Bug`, and assigned to **iisaduan**, **Copilot**, **RyanCavanaugh**

### [Issue microsoft/TypeScript#64730](https://github.com/microsoft/TypeScript/issues/64730) (Closed, `Fixed`)

**TS 7\.0 reports declaration\-emit diagnostics \(e\.g\. TS2527\) under \-\-noEmit when other semantic errors exist; TS 6\.0 does not \(undocumented difference\)**

*TypeScript 7.0 reports declaration-emit diagnostics under --noEmit when other semantic errors are present, unlike 6.0.*

 * created by **seunghyun-24**
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/64730#issuecomment-6123969870) **jakebailey** said "Is this a problem, or something you just happened to notice?"
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/64730#issuecomment-6158338383) **seunghyun-24** explained that they just noticed the issue during a pilot study comparing TS conformance test outputs between tsc 6.0 and 7.0
 * [later](https://github.com/microsoft/TypeScript/issues/64730#issuecomment-6319483186) **RyanCavanaugh** said "This appears to be fixed. Repros in 7.0.2 but not 7.1 nightly"
 * **RyanCavanaugh** added label `Fixed`
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#64742](https://github.com/microsoft/TypeScript/issues/64742) (Open, `Bug`)

**Language server \(tsc \-\-lsp\) exits with code 1 after \`shutdown\` and \`exit\`**

*TypeScript 7's LSP server unexpectedly exits with code 1 after receiving shutdown and exit notifications*

 * created by **creasty**
 * (6 days ago) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/64742#issuecomment-6308382258) **rajnish-verma-22172** offered to add an LSP lifecycle regression test for clean shutdown/exit and implement minimal changes to distinguish valid and invalid shutdown sequences

### [Issue microsoft/TypeScript#64757](https://github.com/microsoft/TypeScript/issues/64757) (Open, `Needs Investigation`, **ahejlsberg**)

**Regression in 7\.1 \(\#64553\): R inferred as unknown through a generic type alias call signature with a nested same\-type argument**

*A TypeScript 7.1 regression makes R infer as unknown rather than Req in a nested generic type alias call signature.*

 * created by **kennysarnoski-jarvis**
 * [later](https://github.com/microsoft/TypeScript/issues/64757#issuecomment-6318384069) **jclaessens97** reported a type inference regression in TypeScript 7.1-dev causing incorrect 'unknown' results with a generic alias in Prisma nested selects and provided a reproduction case
 * (later) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **ahejlsberg**
 * [later](https://github.com/microsoft/TypeScript/issues/64757#issuecomment-6319872131) **kennysarnoski-jarvis** ran the repro locally and confirmed regression TS2571 on nightly builds, described inference failure conditions and downstream tool impact

### [Issue microsoft/TypeScript#64758](https://github.com/microsoft/TypeScript/issues/64758) (Open, `Bug`)

**TS7 LSP: documentHighlight returns nothing when the file path contains '@'**

*DocumentHighlight fails for file paths containing '@' because TS7 LSP server percent-encodes '@' as '%40' while client does not.*

 * created by **snapwich**
 * **RyanCavanaugh** added label `Bug`

### [Issue microsoft/TypeScript#64769](https://github.com/microsoft/TypeScript/issues/64769) (Open, `Bug`)

**Refactor \> \.\.\.  does nothing /  fails silently for \.tsx components that consume css module style\(s\)**

*Refactoring TSX components that import CSS module styles with “Move to new file” fails silently due to a TypeScript Server error.*

 * created by **IanBellomy**
 * **vs-code-engineering[bot]** assigned to **dbaeumer**
 * **dbaeumer** unassigned **dbaeumer**
 * **RyanCavanaugh** added label `Bug`

### [PR microsoft/TypeScript#64821](https://github.com/microsoft/TypeScript/pull/64821) (Open, `For Backlog Bug`)

**Clear auto\-import specifier cache when module specifier preferences change**

*Clear auto-import specifier cache on any module specifier preference change to ensure updated import suggestions for open files.*

 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [5 days ago](https://github.com/microsoft/TypeScript/pull/64821#issuecomment-6201876867) **RyanCavanaugh** challenged the claim that the cache was only cleared on preference changes and requested checking relevant preference values before clearing the cache
 * [5 days ago](https://github.com/microsoft/TypeScript/pull/64821#issuecomment-6202441973) **lsh4711** changed cache clearing to only trigger when ModuleSpecifierPreferences changed, added an Equal method to UserPreferences and added a unit test for it
 * [later](https://github.com/microsoft/TypeScript/pull/64821#issuecomment-6314482381) **lsh4711** asked whether to wait for the PR to land or open the follow-up as a stacked PR

### [PR microsoft/TypeScript#64870](https://github.com/microsoft/TypeScript/pull/64870) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Checker affinity tweaks**

*Tweak checker affinity settings to optimize resource allocation and improve performance*

 * [today](https://github.com/microsoft/TypeScript/pull/64870#issuecomment-6286227764) **jakebailey** said "@typescript-bot perf test"
 * [today](https://github.com/microsoft/TypeScript/pull/64870#issuecomment-6286229347) **typescript-automation[bot]** reported start of perf test build jobs and provided status and results links
 * [today](https://github.com/microsoft/TypeScript/pull/64870#issuecomment-6286762401) **typescript-automation[bot]** reported the results of the requested performance run
 * [today](https://github.com/microsoft/TypeScript/pull/64870#issuecomment-6296288450) **jakebailey** said "@typescript-bot perf test"
 * [today](https://github.com/microsoft/TypeScript/pull/64870#issuecomment-6296290466) **typescript-automation[bot]** announced that CI performance tests had started and that results would be updated as builds progressed
 * [today](https://github.com/microsoft/TypeScript/pull/64870#issuecomment-6296439993) **jakebailey** described follow-up experiments with spreading directory areas, reported inconsistent performance regressions across projects, and parked the PR as a draft
 * [today](https://github.com/microsoft/TypeScript/pull/64870#issuecomment-6296873758) **typescript-automation[bot]** posted requested performance run results in a comparison report
 * [today](https://github.com/microsoft/TypeScript/pull/64870#issuecomment-6297488734) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/64870#issuecomment-6297490582) **typescript-automation[bot]** reported that the perf test started and provided links to build status and results
 * [today](https://github.com/microsoft/TypeScript/pull/64870#issuecomment-6298053666) **typescript-automation[bot]** reported the performance run results requested by @jakebailey

### [PR microsoft/TypeScript#64879](https://github.com/microsoft/TypeScript/pull/64879) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**\[api\] Remove package\.json "imports"**

*Remove package.json imports to support direct CDN loading and output enums in a top-level distribution folder*

 * (yesterday) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64879#issuecomment-6278891207) **andrewbranch** said "Actually, I guess we could just put the enums in some other top-level directory besides dist, similar to vendor"
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#64885](https://github.com/microsoft/TypeScript/pull/64885) (Open, `For Backlog Bug`)

**fix\(64883\): fix asi before escaped keyword class members**

*Adjust automatic semicolon insertion behavior to correctly handle escaped keyword names in class members.*

 * created by **a-tarasyuk**
 * (today) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64885#issuecomment-6300646990) **jakebailey** demonstrated a hang on tests using unicode escape sequences in TypeScript files

### [PR microsoft/TypeScript#64886](https://github.com/microsoft/TypeScript/pull/64886) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**, **Copilot**)

**Align JS API AST types with runtime values**

*Align TypeScript JS API AST types with runtime node values by marking fields nullable, defaulting flags, and adding tokens.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **andrewbranch**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#64887](https://github.com/microsoft/TypeScript/pull/64887) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Handle missing release tags correctly**

*Handle GitHub’s missing-tag error response correctly instead of using it as a commit SHA to permit new release tags.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `Author: Team`, `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64888](https://github.com/microsoft/TypeScript/pull/64888) (Open, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**\[api\] Reduce allocations and megamorphic object penalty from generator methods**

*Optimize generator methods to reduce object allocations and megamorphic call penalties, improving microbenchmark performance.*

 * created by **andrewbranch**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript/pull/64888#issuecomment-6297633598) **andrewbranch** said "@typescript-bot perf test api"
 * [today](https://github.com/microsoft/TypeScript/pull/64888#issuecomment-6297635506) **typescript-automation[bot]** noted that the perf test api job started and provided links to build status and results
 * [today](https://github.com/microsoft/TypeScript/pull/64888#issuecomment-6298203638) **typescript-automation[bot]** reported performance results for the requested perf run to andrewbranch

### [Issue microsoft/TypeScript#64889](https://github.com/microsoft/TypeScript/issues/64889) (Open, `Bug`)

**\`emitDecoratorMetadata\` emits a ReferenceError for a default \`import type\` from an unresolvable module**

*emitDecoratorMetadata erroneously emits runtime code for a default type-only import from an unresolvable module, causing a ReferenceError.*

 * created by **blickly**
 * [later](https://github.com/microsoft/TypeScript/issues/64889#issuecomment-6311453284) **damerlanaga99-source** provided a VS Code debugging configuration snippet

### [PR microsoft/TypeScript#64890](https://github.com/microsoft/TypeScript/pull/64890) (Closed, `For Uncommitted Bug`)

**Update and rename set\-version\.yaml to set\-version\-windows\.yml**

*Rename set-version.yaml to set-version-windows.yml and revise its configuration accordingly.*

 * created by **ethereumliquidcreator**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64890#issuecomment-6301530472) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#64891](https://github.com/microsoft/TypeScript/issues/64891) (Open, `Needs Investigation`, **ahejlsberg**)

**7\.1 regression: declaration order of recursive generic interfaces changes assignability \(TS2322\)**

*TypeScript 7.1 regression causes erroneous TS2322 when assigning DS<{total:M},string> to DS<Record<string,M>,string> due to declaration order change.*

 * created by **chrisolszewski**
 * [today](https://github.com/microsoft/TypeScript/issues/64891#issuecomment-6307221109) **shahinsamiur** described investigating the problem and developing a solution to the variance calculation implementation changes, and said they would provide updates or a PR when ready

### [Issue microsoft/TypeScript#64892](https://github.com/microsoft/TypeScript/issues/64892) (Open, `Needs Investigation`, **ahejlsberg**)

**\[7\.1 Regression\] Unexpected behaviour change from Stronger Distributive Type checks**

*Upgrading to TypeScript 7.1 introduces stricter distributive checks causing TS2345 errors in generic callback methods.*

 * created by **hkleungai**

### [PR microsoft/TypeScript#64893](https://github.com/microsoft/TypeScript/pull/64893) (Open, `For Uncommitted Bug`)

**fix\(checker\): resolve TS2322 regression in circular generic interface variance calculation**

*Eliminate unsafe stack restarts in circular generic interface variance computation to fix a TS2322 regression.*

 * created by **shahinsamiur**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64893#issuecomment-6308636552) **shahinsamiur** said "@microsoft-github-policy-service agree"

### [PR microsoft/TypeScript#64894](https://github.com/microsoft/TypeScript/pull/64894) (Open, `For Backlog Bug`)

**Fix LSP exit status after shutdown**

*Correct LSP server exit codes by tracking shutdown completion and distinguishing valid versus premature exit sequences.*

 * created by **rajnish-verma-22172**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64894#issuecomment-6309091346) **microsoft-github-policy-service[bot]** asked the user to agree to the Contributor License Agreement by replying with the required command

### [Issue microsoft/TypeScript#64895](https://github.com/microsoft/TypeScript/issues/64895) (Open, `Bug`)

**panic: Unhandled case in Node\.MemberList: KindVariableDeclarationList on merged namespace/enum element access**

*TypeScript 7.0.2 panics with an unhandled KindVariableDeclarationList error when accessing a namespace-exported constant in an enum.*

 * created by **muh-syaipullah**
 * [later](https://github.com/microsoft/TypeScript/issues/64895#issuecomment-6311271344) **Andarist** said "this is already being fixed by https://github.com/microsoft/TypeScript/pull/64746"

### [PR microsoft/TypeScript#64896](https://github.com/microsoft/TypeScript/pull/64896) (Open, `For Backlog Bug`)

**Recognize unresolved type\-only default imports during alias lookup**

*Ensure alias lookup correctly identifies unresolved type-only default imports.*

 * created by **Andarist**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [Issue microsoft/TypeScript#64897](https://github.com/microsoft/TypeScript/issues/64897) (Closed)

**tsc \-b no\-op build ~5x slower in 7\.1\.0\-beta \(isContentMapperSupplementalBuildInfoPath scans every root per file\)**

*TypeScript 7.1.0-beta's tsc -b no-op builds are five times slower because isContentMapperSupplementalBuildInfoPath scans every root for each file*

 * created by **todor-a**

### [PR microsoft/TypeScript#64898](https://github.com/microsoft/TypeScript/pull/64898) (Closed, `For Uncommitted Bug`)

**fix: avoid repeated root scans in no\-op builds**

*Eliminates redundant root file scanning in no-op builds to significantly improve build performance.*

 * created by **a-tarasyuk**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [Issue microsoft/TypeScript#64899](https://github.com/microsoft/TypeScript/issues/64899) (Open, `Bug`)

**JSDocTypeLiteral\.jsdocPropertyTags returns only the first tag**

*JSDocTypeLiteral.jsdocPropertyTags accessor in TypeScript v7 erroneously returns only the first property tag instead of all tags.*

 * created by **mourner**

### [PR microsoft/TypeScript#64900](https://github.com/microsoft/TypeScript/pull/64900) (Open, `For Backlog Bug`)

**Fix unused renaming detection in function types**

*Enhance unused-renaming checks in generic function types to properly ignore type-only references.*

 * created by **wickstudio**
 * (later) **typescript-automation[bot]** added labels `For Backlog Bug`, `For Backlog Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/64900#issuecomment-6317648836) **wickstudio** said "@microsoft-github-policy-service agree"

### [PR microsoft/TypeScript#64901](https://github.com/microsoft/TypeScript/pull/64901) (Open, `For Backlog Bug`)

**fix: map constructor param type**

*Fixes incorrect type inference for Map constructor parameters by reordering overloads and adding tests.*

 * created by **tbknl**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/64901#issuecomment-6318429701) **tbknl** said "@microsoft-github-policy-service agree"

### [PR microsoft/TypeScript#64902](https://github.com/microsoft/TypeScript/pull/64902) (Open, `Author: Team`, `For Uncommitted Bug`, **RyanCavanaugh**, **Copilot**)

**Prevent noLib crash when an import\-equals alias references a type**

*Guard property-specific diagnostics under --noLib to prevent crashes when import-equals aliases reference types.*

 * created by **Copilot**
 * (later) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * (later) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`

### [Issue microsoft/TypeScript#64923](https://github.com/microsoft/TypeScript/issues/64923) (Open, **dbaeumer**)

**Support workspace specific typescript version**

*Allow the extension to use a workspace-specific TypeScript version rather than a global one.*

 * **RyanCavanaugh** unassigned **mjbvz**
 * **vs-code-engineering[bot]** assigned to **dbaeumer**
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/64923#issuecomment-6340576842) **dbaeumer** said "@RyanCavanaugh any reason why you moved this to VS Code? The new TS7 extension handles this setting. VS Code by default doesn't expand variables in settings."
 * [later](https://github.com/microsoft/TypeScript/issues/64923#issuecomment-6340576951) **vs-code-engineering[bot]** closed the issue after it lacked the requested information for 7 days
 * (later) **vs-code-engineering[bot]** closed the issue

