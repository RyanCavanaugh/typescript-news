# Report for 2026-11-11 (Wednesday, November 11th, 2026)

20 different users commented on 44 different issues.

## Recommended Actions

 * Response Recommended
    * @dummdidumm provided important context about prior TSX limitations and a possible workaround for changing trigger-character behavior in [microsoft/TypeScript#65326](https://github.com/microsoft/TypeScript/issues/65326#issuecomment-6807783900)
    * @xxangelmamxx asked whether they could work on the issue in [microsoft/TypeScript#65379](https://github.com/microsoft/TypeScript/issues/65379#issuecomment-6805712603)
    * @ghorner2 provided a repository link for maintainers to review the reported issue in [microsoft/TypeScript#65385](https://github.com/microsoft/TypeScript/issues/65385#issuecomment-6804272038)
    * @roxyroo123456-bot reported a regression between versions 6 and 7 with a specific code example and expected diagnostic behavior in [microsoft/TypeScript#65433](https://github.com/microsoft/TypeScript/issues/65433#issuecomment-6811416302)
    * @mrclrchtr provided additional reproduction details and clarified the remaining configuration-matching gap in [microsoft/TypeScript#65443](https://github.com/microsoft/TypeScript/issues/65443#issuecomment-6811846940)

## Activity Summary

### [Issue microsoft/TypeScript#64182](https://github.com/microsoft/TypeScript/issues/64182) (Open, `Domain: Content Mappers`, **andrewbranch**)

**Allow content\-mappers to return declarations instead of source files**

*Allow content mappers for static data formats to return declaration files, avoiding inappropriate module-format and syntax diagnostics.*

 * (9 weeks ago) **andrewbranch** added label `Domain: Content Mappers`, set milestone to `TypeScript 7.1.0 Beta`, and assigned to **andrewbranch**
 * **andrewbranch** removed from milestone `TypeScript 7.1.0 Beta`
 * [today](https://github.com/microsoft/TypeScript/issues/64182#issuecomment-6810719994) **andrewbranch** explained that the module format bug was fixed in #65432, but declaration file extensions must agree with the assigned module format to preserve declaration substitutability, and noted that this restriction reduced the motivation for returning declarations from Transform responses
 * [later](https://github.com/microsoft/TypeScript/issues/64182#issuecomment-6825097778) **remcohaszing** clarified that the `.cts` extension should produce declaration filenames such as `styles.d.css.cts`, then withdrew the earlier feature request after realizing it was based on a premature conclusion
 * [later](https://github.com/microsoft/TypeScript/issues/64182#issuecomment-6828331596) **andrewbranch** explained that `styles.d.css.cts` was not a recognized extension format and caused project-reference, incremental-compilation, and module-resolution issues

### [Issue microsoft/TypeScript#64362](https://github.com/microsoft/TypeScript/issues/64362) (Closed, `Needs Investigation`, `Domain: Content Mappers`, **andrewbranch**)

**Content mappers: more granular resolution, and default extensions in the manifest**

*Request content mappers support path-specific resolution and default manifest extensions, enabling dedicated files like blob.toml without claiming entire extensions.*

 * (7 weeks ago) **RyanCavanaugh** added label `Domain: Content Mappers`, and assigned to **andrewbranch**
 * [6 days ago](https://github.com/microsoft/TypeScript/issues/64362#issuecomment-6671076292) **dummdidumm** explained that content mappers incorrectly prefer `.svelte` implementations over adjacent `.d.svelte.ts` declarations in Svelte packages and proposed excluding `node_modules` from content mapping
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript#64974](https://github.com/microsoft/TypeScript/issues/64974) (Closed, `Bug`)

**7\.1: destructured parameter with a \`= {}\` default loses its contextual type \(TS7031\)**

*TypeScript 7.1 regresses contextual typing for destructured optional parameters with `{}` defaults, incorrectly reporting binding elements as implicitly `any`.*

 * (1 week ago) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/64974#issuecomment-6610623048) **connorshea** said "I think this may be the same issue as #64431?"
 * [today](https://github.com/microsoft/TypeScript/issues/64974#issuecomment-6801596375) **maschwenk** reported that the original snippet regressed from clean to TS7031 between nightly builds, bisected the change to commit 07d1338bac, and noted that several related PR heads cleared the issue while the #65070 array example also reproduced the error in earlier releases

### [Issue microsoft/TypeScript#65008](https://github.com/microsoft/TypeScript/issues/65008) (Closed, `Working as Intended`)

**lib\.dom\.d\.ts: Transformer is missing the \`cancel\` member that WHATWG Streams defines**

*Add the missing WHATWG Streams `cancel` member to TypeScript’s DOM `Transformer` interface so valid TransformStream handlers compile.*

 * [1 week ago](https://github.com/microsoft/TypeScript/issues/65008#issuecomment-6507251988) **timurzvural** opened a fix adding `Transformer.cancel` and `TransformerCancelCallback` to the DOM and Web Worker type definitions, along with a fixture update and compiler regression test
 * **RyanCavanaugh** added label `Working as Intended`
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/65008#issuecomment-6749745363) **RyanCavanaugh** explained that the behavior was expected because DOM libraries followed the generator’s browser-engine support policy, and noted that Node-specific support could be added locally using matching `any` type-parameter defaults
 * [today](https://github.com/microsoft/TypeScript/issues/65008#issuecomment-6811362488) **typescript-automation[bot]** said "This issue has been marked as "Working as Intended" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-automation[bot]** closed the issue

### [PR microsoft/TypeScript#65047](https://github.com/microsoft/TypeScript/pull/65047) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**Allow content mapper registrations to filter their files with an \`include\` glob, inherit default \`extension\` from manifest**

*Allow content mapper registrations to filter files with an include glob and inherit default extensions from the manifest.*

 * (1 week ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#65064](https://github.com/microsoft/TypeScript/pull/65064) (Open, `Author: Team`, `For Milestone Bug`, `For Backlog Bug`, **jakebailey**)

**\[experiment\] fully order independent type checking**

*Proposes making type checking fully order-independent, with randomized ordering tests and extensive fixes for cache, traversal, and identifier-dependent behavior.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6790427183) **typescript-automation[bot]** reported new TypeScript TS7023 errors in SchemaAST.ts when comparing baseline and PR user-test results
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6790645397) **typescript-automation[bot]** reported the requested performance results, including increased symbols and memory usage in the compiler-unions benchmark
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6792655057) **typescript-automation[bot]** reported top-1000-repository tsc comparison results, highlighting unexpected build changes in PeerTube and Effect-TS
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6806420412) **blickly** reported that the PR’s `getIndexedAccessKey` change fixed an uncovered user-visible regression from 6.0, provided reproduction cases and a playground link, and noted that the regression affected a large codebase migration to 7.1
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6810936579) **jakebailey** said "I looked into that, and that's actually just a straight up bug that's a one line fix, somehow applied in this PR"
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6811075641) **jakebailey** said "https://github.com/microsoft/TypeScript/pull/65450"
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6811134651) **jakebailey** requested TypeScript bot runs for dt, user testing, top1000 testing, and performance testing
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6811136294) **typescript-automation[bot]** reported that automated builds had started for the requested test commands and linked their results
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6811585273) **typescript-automation[bot]** reported that the DT tests found a branch-only TypeScript compile error in d3-selection at d3-selection-tests.ts:1502
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6811839297) **typescript-automation[bot]** reported that the requested performance run results were available and showed increased symbols and memory usage for the Compiler-Unions native scenario
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6811863495) **typescript-automation[bot]** reported new TypeScript errors in the Effect project’s user-test comparison and asked the maintainer to investigate the changes
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6813575722) **typescript-automation[bot]** reported changed top-1000-repository build results between the baseline and PR, including new TypeScript errors in PeerTube and Effect-TS, and asked the maintainer to investigate

### [Issue microsoft/TypeScript#65084](https://github.com/microsoft/TypeScript/issues/65084) (Closed, `Needs Investigation`, **andrewbranch**, **Copilot**)

**Content mappers: saving a \`watchedFiles\` file that is open in the editor never re\-runs \`openProject\` \(stale types until the language server is restarted\)**

*Saving an open editor file listed in a content mapper’s `watchedFiles` fails to rerun `openProject`, leaving types stale.*

 * created by **toiroakr**
 * (yesterday) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **andrewbranch**
 * **andrewbranch** assigned to **Copilot**
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript#65326](https://github.com/microsoft/TypeScript/issues/65326) (Open, `Needs Investigation`, **andrewbranch**)

**Allow to influence trigger characters for files with content\-mappers**

*Request an API allowing content mappers to define additional completion trigger characters for embedded file types such as Svelte.*

 * (2 days ago) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **andrewbranch**
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/65326#issuecomment-6754508009) **andrewbranch** said "I think this is a reasonable feature request, but I'm also curious if for this particular case you considered emitting TSX for Svelte files?"
 * [today](https://github.com/microsoft/TypeScript/issues/65326#issuecomment-6807783900) **dummdidumm** explained that a previous TSX-based approach had syntax and error-message limitations, and suggested changing only trigger-character behavior through an alternative workaround

### [PR microsoft/TypeScript#65352](https://github.com/microsoft/TypeScript/pull/65352) (Closed, `For Backlog Bug`)

**lib: remove obsolete Atomics\.pause parameter**

*Remove the obsolete optional parameter from the Atomics.pause declaration and update conformance baselines to expect TS2554 for argument-bearing calls.*

 * (6 days ago) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Backlog Bug`, and removed label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/65352#issuecomment-6819927705) **JemmyIndex** reported that the concurrent test job failed due to a transient download error from proxy.golang.org, noted that all other checks passed, and requested rerunning the failed jobs

### [Issue microsoft/TypeScript#65355](https://github.com/microsoft/TypeScript/issues/65355) (Open, `Suggestion`)

**Remote declaration resolution**

*Request support for resolving remote TypeScript declaration files in browser-based, bundler-free ESM projects without installing runtime dependencies.*

 * **RyanCavanaugh** added label `Duplicate`
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/65355#issuecomment-6750067519) **RyanCavanaugh** identified the issue as a duplicate of #35749
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/65355#issuecomment-6751850958) **alshdavid** clarified that their ticket concerned modeling browser import maps and fetching type definitions from remote URLs without requiring npm installation, unlike the referenced ticket that used local node_modules types
 * [today](https://github.com/microsoft/TypeScript/issues/65355#issuecomment-6811360610) **typescript-automation[bot]** said "This issue has been marked as "Duplicate" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-automation[bot]** closed the issue

### [Issue microsoft/TypeScript#65357](https://github.com/microsoft/TypeScript/issues/65357) (Closed, `Not a Defect`)

**TypeScript 7\.1: in checks always succeed for child properties on RemoteNode, breaking type narrowing**

*TypeScript 7.1 RemoteNode prototypes make `in` checks for child properties always succeed, breaking type narrowing and causing runtime errors.*

 * [5 days ago](https://github.com/microsoft/TypeScript/issues/65357#issuecomment-6685266543) **k-taro56** clarified that the issue concerned runtime behavior changes since version 6.0
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/65357#issuecomment-6750082572) **RyanCavanaugh** said "6.0 and 7.0 API are not intended to work identically, and in isn't a documented/sound way of doing these checks."
 * **RyanCavanaugh** added label `Not a Defect`
 * [today](https://github.com/microsoft/TypeScript/issues/65357#issuecomment-6811361694) **typescript-automation[bot]** said "This issue has been marked as "Not a Defect" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-automation[bot]** closed the issue

### [Issue microsoft/TypeScript#65365](https://github.com/microsoft/TypeScript/issues/65365) (Closed, `Not a Defect`)

**TS2589 in 7\.1 on code that 5\.9 and 6\.0 accept, caused by stable union ordering \(6\.0 with \-\-stableTypeOrdering does not finish\)**

*TypeScript 7.1 reports TS2589 on valid recursive conditional and intersection types due to stable union ordering, unlike 5.9 and 6.0.*

 * created by **yusufyildiz34**
 * **RyanCavanaugh** added label `Not a Defect`
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/65365#issuecomment-6750101306) **RyanCavanaugh** clarified that the behavior was not a TS7 regression, existed in TS6 with `--stableTypeOrdering`, and that reporting TS2589 was preferable to a non-terminating check
 * [today](https://github.com/microsoft/TypeScript/issues/65365#issuecomment-6811361240) **typescript-automation[bot]** said "This issue has been marked as "Not a Defect" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-automation[bot]** closed the issue

### [Issue microsoft/TypeScript#65379](https://github.com/microsoft/TypeScript/issues/65379) (Open, `Bug`, `Domain: Declaration Emit`)

**Declaration emit writes \`\[SymbolConstructor\.iterator\]\` as a computed key when a \`SymbolConstructor\` value is in scope**

*Declaration emit regressed in TypeScript 7.x, incorrectly emitting `[SymbolConstructor.iterator]` instead of `[S.iterator]` when `SymbolConstructor` is in scope.*

 * (2 days ago) **RyanCavanaugh** added labels `Bug`, `Domain: Declaration Emit`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/65379#issuecomment-6805712603) **xxangelmamxx** said "Hi! I'd love to give this issue a try if it's still available! I'm new to contributing to TypeScript, but I'd really appreciate the opportunity to help. Would that be okay?"

### [Issue microsoft/TypeScript#65385](https://github.com/microsoft/TypeScript/issues/65385) (Open, `Needs Investigation`, **joj**)

**VisualStudio 2026 \- Razor Class Library**

*Adding Microsoft.TypeScript.MSBuild 7.0.1 to Razor or Blazor projects causes Visual Studio to repeatedly detect changes, prompt reloads, or prevent applications from running.*

 * **RyanCavanaugh** added label `Needs More Info`
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/65385#issuecomment-6750712289) **RyanCavanaugh** requested a minimal Razor/Blazor project, the exact Visual Studio version, reproduction steps, the project file, and relevant build or ActivityLog output for the reload loop
 * [today](https://github.com/microsoft/TypeScript/issues/65385#issuecomment-6799205771) **ghorner2** provided reproduction steps for a Blazor WASM project using Microsoft.Typescript.MSBuild and a sample tsconfig.json
 * [today](https://github.com/microsoft/TypeScript/issues/65385#issuecomment-6804272038) **ghorner2** provided a GitHub repository link to demonstrate the issue

### [Issue microsoft/TypeScript#65386](https://github.com/microsoft/TypeScript/issues/65386) (Closed, `Design Limitation`)

**Semantic tokens re\-check files on a cold query checker after diagnostics already checked them**

*Semantic token requests redundantly re-type-check edited files after diagnostics, and should reuse the completed diagnostics checker to reduce latency.*

 * created by **hood**
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/65386#issuecomment-6752482533) **RyanCavanaugh** reported that the proposed reuse was unsafe because checker order sensitivity and cross-file operations could suppress circular-instantiation diagnostics, and provided a minimal reproduction and test results demonstrating the issue
 * **RyanCavanaugh** added label `Design Limitation`
 * [today](https://github.com/microsoft/TypeScript/issues/65386#issuecomment-6811363540) **typescript-automation[bot]** said "This issue has been marked as "Design Limitation" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-automation[bot]** closed the issue

### [PR microsoft/TypeScript#65428](https://github.com/microsoft/TypeScript/pull/65428) (Open, `Domain: Performance`, `For Backlog Bug`)

**Bound template literal expansion while computing base constraints**

*Bound template literal expansion during base-constraint computation to prevent excessive type creation and memory usage for large recursive conditional types.*

 * created by **Keviniscool-boy**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [yesterday](https://github.com/microsoft/TypeScript/pull/65428#issuecomment-6771780522) **Keviniscool-boy** said "@microsoft-github-policy-service agree"
 * **jakebailey** added label `Domain: Performance`

### [Issue microsoft/TypeScript#65433](https://github.com/microsoft/TypeScript/issues/65433) (Open, `Bug`, `Help Wanted`, `Good First Issue`)

**Incorrect error message when ASI errors involve a nonstandard newline**

*TypeScript 7 omits the “Are you missing a semicolon?” diagnostic when ASI errors involve a U+2028 paragraph separator.*

 * (yesterday) **RyanCavanaugh** added labels `Help Wanted`, `Good First Issue`, and removed label `Good First Issue`
 * [today](https://github.com/microsoft/TypeScript/issues/65433#issuecomment-6811416302) **roxyroo123456-bot** reported that TypeScript 7 stopped adding the “Are you missing a semicolon?” sub-error for a U+2028 paragraph separator after an arrow function expression, unlike TypeScript 6

### [PR microsoft/TypeScript#65435](https://github.com/microsoft/TypeScript/pull/65435) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Cache missing property names of unions**

*Cache missing property names for union types to improve performance when repeatedly checking nonexistent properties.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/65435#issuecomment-6780954398) **typescript-automation[bot]** reported that the performance test job started and linked to its build results
 * [yesterday](https://github.com/microsoft/TypeScript/pull/65435#issuecomment-6781664460) **typescript-automation[bot]** reported the requested performance results comparing the baseline and pull request, including compiler metrics and a slight memory increase
 * (yesterday) **jakebailey** closed the issue
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#65439](https://github.com/microsoft/TypeScript/pull/65439) (Closed, `For Backlog Bug`)

**Emit "Are you missing a semicolon?" for ASI across U\+2028/U\+2029**

*Restore missing-semicolon diagnostics for accidental calls split by U+2028 or U+2029 line separators in the native compiler.*

 * created by **amalsaidov**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * (yesterday) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/65439#issuecomment-6808133340) **amalsaidov** said "Thanks for taking a look 🙏"

### [PR microsoft/TypeScript#65442](https://github.com/microsoft/TypeScript/pull/65442) (Closed, `For Backlog Bug`)

**Emit TS2734 for ASI errors involving nonstandard newlines**

*Ensure accidental calls across U+2028 and U+2029 line breaks emit the related TS2734 semicolon diagnostic.*

 * created by **bodapatisaikrishna**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#65443](https://github.com/microsoft/TypeScript/issues/65443) (Open, `API Request`, **andrewbranch**)

**API: expose config include/exclude matching and supported extensions**

*Expose public APIs for determining whether config files include or exclude paths and retrieving supported file extensions, including newly created files.*

 * created by **mrclrchtr**
 * [today](https://github.com/microsoft/TypeScript/issues/65443#issuecomment-6801590230) **andrewbranch** said "Though not the central point of the issue, the problem with your example code is that s1.update is missing ensurePrograms: true."
 * (today) **andrewbranch** added label `API Request`, and assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript/issues/65443#issuecomment-6811846940) **mrclrchtr** confirmed that `ensurePrograms: true` resolves created files, corrected the example, and described remaining config-coverage gaps involving nonexistent paths and imported files outside `include`

### [Issue microsoft/TypeScript#65444](https://github.com/microsoft/TypeScript/issues/65444) (Open, `Bug`, `Domain: LS: Refactorings`)

**7\.0 regression: \`prepareRename\` placeholder includes quotes and brackets**

*TypeScript 7.0 regresses `prepareRename` by including quotes and brackets in property rename placeholders, producing invalid syntax when renamed.*

 * created by **mizdra**

### [Issue microsoft/TypeScript#65445](https://github.com/microsoft/TypeScript/issues/65445) (Closed)

**7\.1 regression: TS5115 for import\("cloudflare:workers"\) with @cloudflare/workers\-types**

*TypeScript 7.1 introduces TS5115 infinite-instantiation errors for dynamic `cloudflare:workers` imports using `@cloudflare/workers-types`.*

 * created by **alon-gb**
 * [today](https://github.com/microsoft/TypeScript/issues/65445#issuecomment-6801655226) **maschwenk** bisected the regression to microsoft/typescript-go#4687, identified the added anonymous-symbol declarations assignment as the cause, and provided a minimal reproduction and technical explanation involving recursive Provider<any> inference and TS2589/TS5115.

### [PR microsoft/TypeScript#65446](https://github.com/microsoft/TypeScript/pull/65446) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**, **Copilot**)

**Refresh content mapper configuration when open watched files are saved**

*Refresh content mapper configuration when saving open watched files, preserving hidden disk changes without falsely invalidating overlay source text.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **andrewbranch**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `Author: Team`, `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/65446#issuecomment-6804740197) **andrewbranch** said "@copilot+gpt-6.1-sol fix previously missed issues"
 * [today](https://github.com/microsoft/TypeScript/pull/65446#issuecomment-6805120929) **Copilot** reported that the previously missed issues were fixed in 19cd34b6b, regression coverage was added, validation and secret scanning passed, and CodeQL was skipped due to the database size limit
 * [today](https://github.com/microsoft/TypeScript/pull/65446#issuecomment-6805800280) **andrewbranch** said "@copilot+gpt-6.1-sol fix previously missed issue"
 * [today](https://github.com/microsoft/TypeScript/pull/65446#issuecomment-6806276074) **Copilot** reported that commit 99982aae9 fixed disk-change provenance across symlink alias expansion, added a regression test preserving unsaved overlay text, and passed validation and secret scanning while skipping CodeQL due to database size limits
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#65447](https://github.com/microsoft/TypeScript/pull/65447) (Open, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**Add support for setting emit flags and synthetic comments**

*Adds support for configuring emitter flags and synthetic comments while refactoring shared async-related emitter code.*

 * created by **andrewbranch**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **andrewbranch**

### [PR microsoft/TypeScript#65448](https://github.com/microsoft/TypeScript/pull/65448) (Open, `For Backlog Bug`)

**Fix duplicate comments on fields following a decorated field**

*Fix duplicate comments after decorated fields by assigning synthesized __runInitializers calls the replaced initializer’s source range.*

 * created by **TimonGaertner**
 * **typescript-automation[bot]** added label `For Backlog Bug`

### [PR microsoft/TypeScript#65449](https://github.com/microsoft/TypeScript/pull/65449) (Open, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**Fix incorrect last bytes sent API timing data from nested requests**

*Correct the last-bytes-sent API timing data so nested requests report accurate values.*

 * created by **andrewbranch**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **andrewbranch**

### [PR microsoft/TypeScript#65450](https://github.com/microsoft/TypeScript/pull/65450) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Key deferred indexed access types by their persistent access flags**

*Fix a porting bug so deferred indexed access types are keyed by persistent access flags rather than all access flags.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/65450#issuecomment-6811109670) **jakebailey** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/65450#issuecomment-6811111466) **typescript-automation[bot]** reported that all requested test jobs started, with results available for most jobs and performance results still pending review
 * [today](https://github.com/microsoft/TypeScript/pull/65450#issuecomment-6811587465) **typescript-automation[bot]** reported that user tests comparing the baseline and PR with tsc passed successfully
 * [today](https://github.com/microsoft/TypeScript/pull/65450#issuecomment-6811587717) **typescript-automation[bot]** reported that the DT test results were ready and unchanged, linking to the build log
 * [today](https://github.com/microsoft/TypeScript/pull/65450#issuecomment-6811765621) **typescript-automation[bot]** provided the requested performance run results comparing the baseline and PR
 * [today](https://github.com/microsoft/TypeScript/pull/65450#issuecomment-6812456020) **typescript-automation[bot]** reported that testing the top 400 repositories with tsc showed no differences between the baseline and PR, with everything looking good

### [Issue microsoft/TypeScript#65451](https://github.com/microsoft/TypeScript/issues/65451) (Open, `Bug`, `Domain: API`)

**Native API createSourceFile panics for numeric literals whose normalized text is longer than the source**

*Native API createSourceFile panics when numeric literals normalize to text longer than their original source spelling.*

 * created by **AkisArou**

### [Issue microsoft/TypeScript#65452](https://github.com/microsoft/TypeScript/issues/65452) (Open, `Bug`, `Domain: Crashes`)

**Checker crashes on yield\* of a synchronous iterable containing an invalid thenable**

*TypeScript crashes while checking `yield*` over a synchronous iterable containing an invalid thenable instead of reporting a diagnostic.*

 * created by **AkisArou**

### [Issue microsoft/TypeScript#65453](https://github.com/microsoft/TypeScript/issues/65453) (Open, `Suggestion`)

**\[Formatter\] add new options for blank lines**

*Add formatter options to remove unnecessary blank lines and limit consecutive blank lines in TypeScript code.*

 * created by **jmevel**

### [PR microsoft/TypeScript#65454](https://github.com/microsoft/TypeScript/pull/65454) (Closed, `For Backlog Bug`)

**fix: detect Unicode line separators in ASI diagnostics**

*Fix accidental-call diagnostics to recognize multi-byte Unicode line separators by decoding the final UTF-8 rune before ASI checks.*

 * created by **falakahuja**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/65454#issuecomment-6828429172) **falakahuja** said "@microsoft-github-policy-service agree"

