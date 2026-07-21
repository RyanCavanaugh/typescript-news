# Report for 2026-07-20 (Monday, July 20th, 2026)

13 different users commented on 36 different issues.

## Recommended Actions

 * Response Recommended
    * @MasterTLF asked if it was resolved in [microsoft/TypeScript-go#4611](https://github.com/microsoft/TypeScript-go/pull/4611#issuecomment-5028999862)
    * @daniele-orlando asked if the updated reproduction worked in [microsoft/TypeScript-go#4686](https://github.com/microsoft/TypeScript-go/issues/4686#issuecomment-5028116077)
    * @typescript-automation[bot] provided the requested performance run results in [microsoft/TypeScript-go#4687](https://github.com/microsoft/TypeScript-go/pull/4687#issuecomment-5027083261)

## Activity Summary

### [PR microsoft/TypeScript-go#4474](https://github.com/microsoft/TypeScript-go/pull/4474) (Closed)

**Big string union optimizations**

*Deferring sorting and disabling suggestion generation in large string unions speeds up tsgo type checking by 3–5×.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4474#issuecomment-4836933649) **typescript-automation[bot]** posted build status update with links to job start and results
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4474#issuecomment-4837145515) **typescript-automation[bot]** posted the requested performance run results
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4474#issuecomment-4837348305) **jakebailey** said "Sort of what I was expecting; nothing in our actual test suite."
 * [later](https://github.com/microsoft/TypeScript-go/pull/4474#issuecomment-5035645688) **jakebailey** said "Closing in favor of #4687"
 * (later) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4553](https://github.com/microsoft/TypeScript-go/issues/4553) (Closed, `Domain: API and Extensibility`, **andrewbranch**, **Copilot**)

**Add \`\.getConstraint\(\)\` and \`\.getDefault\(\)\` getter to \`TypeParameter\`**

*Add getConstraint() and getDefault() methods to TypeParameter for consistency with other type classes.*

 * (1 week ago) **RyanCavanaugh** set milestone to `Post-7.0`, and assigned to **andrewbranch**
 * **andrewbranch** assigned to **Copilot**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#4556](https://github.com/microsoft/TypeScript-go/pull/4556) (Closed, **andrewbranch**, **Copilot**)

**Add getConstraint\(\) and getDefault\(\) getters to TypeParameter**

*Add asynchronous getConstraint() and getDefault() methods to the TypeParameter API for direct retrieval of type parameter constraints and defaults*

 * (1 week ago) **Copilot** assigned to **Copilot**, **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4556#issuecomment-5024026965) **Copilot** reworked both endpoints to follow the getTrueType/getFalseType pattern, removed fetchCheckerType helper, updated server-side functions, and adjusted fetchType return behavior
 * [today](https://github.com/microsoft/TypeScript-go/pull/4556#issuecomment-5024988417) **andrewbranch** said "@copilot address review feedback"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4556#issuecomment-5025202776) **Copilot** addressed review feedback and outlined changes including restoring fetchType behavior, adding fetchOptionalType helper, updating getConstraint and getDefault dispatch logic, modifying server handlers, and regenerating the Sync API
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#4575](https://github.com/microsoft/TypeScript-go/pull/4575) (Closed)

**Create Workspace**

*Request to create a new workspace named Abmc.*

 * created by **leonelmateopucperez05-sudo**
 * (later) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4578](https://github.com/microsoft/TypeScript-go/pull/4578) (Open)

**Fix nondeterministic Realpath on darwin for hardlinked files**

*Deterministically resolve files with multiple hardlinks on macOS by reconstructing paths from parent directories to prevent intermittent resolution errors.*

 * created by **eddking**
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4578#issuecomment-4928938584) **eddking** said "@microsoft-github-policy-service agree"
 * [later](https://github.com/microsoft/TypeScript-go/pull/4578#issuecomment-5035875510) **jakebailey** suggested deleting the darwin special case code and testing fallback to EvalSymlinks

### [Issue microsoft/TypeScript-go#4580](https://github.com/microsoft/TypeScript-go/issues/4580) (Closed, `Domain: Editor`)

**TS7 plugin is not working with Yarn 4 nodeLinker = pnp**

*TS7’s VSCode plugin and compiler fail to work with Yarn 4 PnP due to missing tsserver and inaccessible cached archives.*

 * **RyanCavanaugh** added to milestone `Need More Info`
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/4580#issuecomment-5007287838) **RyanCavanaugh** said ""uses Yarn 4" is not enough info to go on - we really need a concrete repro to investigate."
 * [today](https://github.com/microsoft/TypeScript-go/issues/4580#issuecomment-5019588142) **zuyetawarmatik** provided a reproduction repository link and steps causing a typecheck failure
 * [later](https://github.com/microsoft/TypeScript-go/issues/4580#issuecomment-5035887969) **jakebailey** said "This is just #460"
 * (later) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4587](https://github.com/microsoft/TypeScript-go/issues/4587) (Open, `Needs More Info`, **weswigham**)

**TSX files do not report TypeScript diagnostics, while TS files work correctly \(autocomplete still works\)**

*Enabling tsgo in VS Code’s TypeScript 7 extension causes .tsx files to omit diagnostics while .ts files report errors normally.*

 * created by **pedroGoffi**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `Post-7.0`, and assigned to **weswigham**

### [Issue microsoft/TypeScript-go#4589](https://github.com/microsoft/TypeScript-go/issues/4589) (Open, `Domain: Editor`, `Needs Investigation`, **johnfav03**)

**workspace/diagnostic/refresh is triggered for watch events that cannot affect type checking**

*The VS Code TypeScript language server erroneously triggers diagnostic refreshes for unrelated .svg file changes in node_modules.*

 * created by **mjbvz**
 * **mjbvz** added label `Domain: Editor`
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/4589#issuecomment-4944241900) **ibesuperv** opened PR #4604 to optimize the Session.DidChangeWatchedFiles path by filtering out irrelevant extensions while preserving cache-invalidation invariants and asked if further tweaks were needed
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `Post-7.0`, and assigned to **johnfav03**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4589#issuecomment-5030035555) **ibesuperv** investigated the root cause of CPU spikes during noisy filesystem activity, identified that Session.DidChangeWatchedFiles unconditionally triggered diagnostics refresh for all file events, reproduced the issue, and contrasted PR #4604’s extension-based filter with PR #4637’s content-hash comparison

### [Issue microsoft/TypeScript-go#4608](https://github.com/microsoft/TypeScript-go/issues/4608) (Open, `Needs More Info`)

**Identical resolved program produces 157 vs 662,155 diagnostics depending on whether the tsconfig is passed directly or through a pass\-through extends**

*Using a pass-through tsconfig that simply extends the main config results in drastically more TypeScript diagnostics than direct config usage.*

 * created by **michaeldanish**
 * **RyanCavanaugh** added label `Needs More Info`
 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/4608#issuecomment-4982366337) **RyanCavanaugh** suggested using the repro reduction skill and linked to the TypeScript Maintainer Skills repository
 * **RyanCavanaugh** added to milestone `Need More Info`

### [PR microsoft/TypeScript-go#4611](https://github.com/microsoft/TypeScript-go/pull/4611) (Closed)

**Update \_scripts tooling deps and lockfiles**

*Update _scripts tooling dependencies, regenerate lockfiles, and add devcontainer lockfile for merging into main.*

 * created by **MasterTLF**
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4611#issuecomment-4951714474) **MasterTLF** said "@microsoft-github-policy-service agree"
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4611#issuecomment-4951931688) **MasterTLF** said "fix without second review and approval"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4611#issuecomment-5028999862) **MasterTLF** said "is this resolved"
 * (today) **MasterTLF** closed the issue

### [Issue microsoft/TypeScript-go#4620](https://github.com/microsoft/TypeScript-go/issues/4620) (Open, `Needs Investigation`, **jakebailey**)

**tsc is not resposive to \`ctrl\-c\`**

*tsc fails to respond to ctrl-c due to incomplete propagation of signal handlers in typescript-go*

 * (5 days ago) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **jakebailey**
 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/4620#issuecomment-4983072567) **anthonyshew** described that pnpm run dev:ts hung on one Ctrl+C and required three to exit, whereas pnpm exec tsc exited immediately
 * **RyanCavanaugh** added to milestone `TypeScript 7.1`

### [Issue microsoft/TypeScript-go#4626](https://github.com/microsoft/TypeScript-go/issues/4626) (Closed, `Needs Investigation`, **andrewbranch**)

**Include \`projectReferences\` in parsed config returned from \`API\#parseConfigFile\(\)\`**

*Include projectReferences in the parsed config returned by API#parseConfigFile to support solution tsconfig files.*

 * created by **mrazauskas**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `Post-7.0`, and assigned to **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#4627](https://github.com/microsoft/TypeScript-go/pull/4627) (Closed)

**\[api\] Include \`projectReferences\` in parsed config**

*Include projectReferences in the parsed configuration returned by API#parseConfigFile*

 * created by **mrazauskas**
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#4630](https://github.com/microsoft/TypeScript-go/issues/4630) (Closed, `Needs More Info`)

**"Type instantiation is excessively deep and possibly infinite" error with tsgo in v7**

*Typechecking with tsgo and TypeScript v7.0.2 intermittently fails with excessive stack depth and infinite type instantiation errors, unlike v6.0.*

 * **RyanCavanaugh** added label `Needs More Info`
 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/4630#issuecomment-4982461122) **RyanCavanaugh** suggested attaching a debugger and inspecting the call stack, noted TypeScript lacks source file positioning at the error frame, and recommended using the TypeScript-Maintainer-Skills repro reduction tool to provide a reproduction
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/4630#issuecomment-4989796747) **justinsmid** thanked RyanCavanaugh and said he would move the issue to the tsgo repo after isolating a minimal reproduction
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#4638](https://github.com/microsoft/TypeScript-go/pull/4638) (Closed)

**fix\(declarations\): prevent panic for KindArrowFunction parameter visibility**

*Prevent panics by adding KindArrowFunction and KindFunctionExpression to parameter visibility diagnostics.*

 * created by **kimyeongrae23**
 * [later](https://github.com/microsoft/TypeScript-go/pull/4638#issuecomment-5036137290) **jakebailey** said "#4648"
 * (later) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4651](https://github.com/microsoft/TypeScript-go/pull/4651) (Closed)

**Do not issue diagnostics when fetching parameter types for context\-sensitive parameters**

*Skip diagnostics during out-of-context retrieval of context-sensitive parameter types to avoid false errors in early type assignment.*

 * created by **weswigham**
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript-go#4660](https://github.com/microsoft/TypeScript-go/pull/4660) (Open, **DanielRosenwasser**, **Copilot**)

**Respect configured TypeScript diagnostic locale**

*Respect js/ts.locale and typescript.locale overrides for TypeScript diagnostics, restart the language server on changes, and fallback to auto display language.*

 * created by **Copilot**
 * (4 days ago) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * [later](https://github.com/microsoft/TypeScript-go/pull/4660#issuecomment-5035657322) **jakebailey** said "Maybe it's cleaner to just have a Client hook that sets the current locale, and we update that on user pref change and plumb it that wayh"

### [PR microsoft/TypeScript-go#4668](https://github.com/microsoft/TypeScript-go/pull/4668) (Open, **RyanCavanaugh**, **Copilot**)

**Respect editor tab/space settings when parsing formatting prefs used by organize imports**

*Map editor tabSize and insertSpaces settings to formatting indentSize and convertTabsToSpaces so organizeImports honors editor indentation preferences.*

 * created by **Copilot**
 * (3 days ago) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * [later](https://github.com/microsoft/TypeScript-go/pull/4668#issuecomment-5035895275) **jakebailey** said "This is identical to #4602"

### [Issue microsoft/TypeScript-go#4669](https://github.com/microsoft/TypeScript-go/issues/4669) (Open, `Needs Investigation`, **johnfav03**)

**\[ServerErrors\]\[TypeScript\] main vs **

*The TypeScript main branch error-delta pipeline tested 300 repositories, analyzing 198, reporting 10 interesting changes, 188 unchanged, and various failures.*

 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/4669#issuecomment-5008527371) **typescript-automation[bot]** reported a premature server connection closure with undefined error for babel/babel and included logs, request history, and partial repro steps
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/4669#issuecomment-5008527438) **typescript-automation[bot]** reported that the server connection closed prematurely with undefined while processing nuxt/nuxt
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/4669#issuecomment-5008527499) **typescript-automation[bot]** reported server connection closed prematurely error with affected repos, old server result, last requests, and repro steps
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `Post-7.0`, and assigned to **johnfav03**

### [Issue microsoft/TypeScript-go#4672](https://github.com/microsoft/TypeScript-go/issues/4672) (Open, `bug`, **johnfav03**)

**is Watch out of the prototype phase?**

*Query whether the --watch mode is production-ready given incremental rechecking support and if the README requires updating.*

 * created by **jkpjkpjkp**
 * (today) **RyanCavanaugh** added label `bug`, and assigned to **johnfav03**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4672#issuecomment-5027748004) **RyanCavanaugh** said "Watch is fully supported; we forgot to update the readme"
 * **RyanCavanaugh** added to milestone `TypeScript 7.1`

### [Issue microsoft/TypeScript-go#4673](https://github.com/microsoft/TypeScript-go/issues/4673) (Open, `bug`, **ahejlsberg**)

**False\-positive TS7022 on destructured array element used as a 2\-D index**

*In TypeScript 7.x, destructuring a 2-D array index after control-flow narrowing erroneously triggers a TS7022 implicit any error.*

 * created by **yuki2006**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `Post-7.0`, and assigned to **ahejlsberg**

### [Issue microsoft/TypeScript-go#4677](https://github.com/microsoft/TypeScript-go/issues/4677) (Open, `Domain: Editor`)

**JSDoc \(TSDoc ???\) is not shown for object literal properties on hover**

*In TypeScript 7, VS Code stops displaying JSDoc comments on hover for const object literal properties, losing per-property documentation.*

 * created by **nazmul-nhb**
 * **nazmul-nhb** added label `Domain: Editor`
 * **RyanCavanaugh** added to milestone `Possible Improvement`

### [Issue microsoft/TypeScript-go#4683](https://github.com/microsoft/TypeScript-go/issues/4683) (Open)

**Generic type parameter inferred differently across two call\-site positions with opposite variance \(narrow type vs union\)**

*TypeScript infers D from the columns as MetricWithCardinality rather than the union type when passing data to Table.*

 * created by **valentinmelusson**
 * [later](https://github.com/microsoft/TypeScript-go/issues/4683#issuecomment-5034155386) **Andarist** said "bisects to #4389"

### [Issue microsoft/TypeScript-go#4684](https://github.com/microsoft/TypeScript-go/issues/4684) (Open, `Domain: Editor`)

**VS Code extension does not provide completions for directive comments**

*VS Code extension does not support completions for TypeScript directive comments such as @ts-expect-error.*

 * created by **mrazauskas**
 * **mrazauskas** added label `Domain: Editor`
 * [later](https://github.com/microsoft/TypeScript-go/issues/4684#issuecomment-5035668136) **jakebailey** said "Do I dare claim that not offering these is a feature? 😄 "
 * [later](https://github.com/microsoft/TypeScript-go/issues/4684#issuecomment-5036084028) **mrazauskas** questioned whether the difference was intentional and suggested closing the issue if so

### [Issue microsoft/TypeScript-go#4686](https://github.com/microsoft/TypeScript-go/issues/4686) (Open, `Needs More Info`)

**TypeScript 7\.0\.2 does not infer function generic parameter, TypeScript 6 does**

*TypeScript 7.0.2 fails to infer a function's generic parameter that TypeScript 6 infers correctly.*

 * created by **daniele-orlando**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4686#issuecomment-5027849863) **RyanCavanaugh** said "Please post a code sample or cloneable repro, we are generally averse to arbitrary zips (unsearchable and sketchy)"
 * (today) **RyanCavanaugh** added label `Needs More Info`, and set milestone to `Need More Info`
 * [today](https://github.com/microsoft/TypeScript-go/issues/4686#issuecomment-5028116077) **daniele-orlando** said "@RyanCavanaugh I have updated the issue reproduction description to point to a StackBlitz repository. Does it work for you?"

### [PR microsoft/TypeScript-go#4687](https://github.com/microsoft/TypeScript-go/pull/4687) (Closed)

**Optimize construction of union types**

*Optimize union type construction by collecting, sorting, and deduplicating types, adding suggestion limits, and stabilizing symbol ID assignment.*

 * created by **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4687#issuecomment-5026679382) **ahejlsberg** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4687#issuecomment-5026680373) **typescript-automation[bot]** started build jobs and posted status updates with result links
 * [today](https://github.com/microsoft/TypeScript-go/pull/4687#issuecomment-5027083261) **typescript-automation[bot]** provided the requested performance run results
 * [today](https://github.com/microsoft/TypeScript-go/pull/4687#issuecomment-5027339179) **typescript-automation[bot]** reported successful tsc test results for the top 400 repos comparing main and the pull request merge

### [PR microsoft/TypeScript-go#4688](https://github.com/microsoft/TypeScript-go/pull/4688) (Closed)

** smart\-selection ranges for mapped types**

*Grouping mapped type components into synthetic SyntaxList nodes in Strada prevents selection expansion from skipping intermediate ranges like -readonly modifiers.*

 * created by **navya9singh**
 * (today) **navya9singh** closed the issue

### [PR microsoft/TypeScript-go#4689](https://github.com/microsoft/TypeScript-go/pull/4689) (Closed)

**\[api\] Add Type convenience methods, cache consistently**

*Add missing Type convenience methods and ensure consistent caching of parameterless Type API calls*

 * created by **andrewbranch**
 * (later) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#4690](https://github.com/microsoft/TypeScript-go/pull/4690) (Open, `dependencies`, `javascript`)

**Bump brace\-expansion from 5\.0\.6 to 5\.0\.7**

*The brace-expansion dependency is updated from version 5.0.6 to 5.0.7.*

 * created by **dependabot[bot]**
 * (later) **dependabot[bot]** added labels `dependencies`, `javascript`, `dependencies`, `javascript`

