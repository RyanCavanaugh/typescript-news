# Report for 2026-02-19 (Thursday, February 19th, 2026)

22 different users commented on 45 different issues.

## Recommended Actions

 * Response Recommended
    * @antichris reported additional formatting edge cases that should be acknowledged in [microsoft/TypeScript-go#2201](https://github.com/microsoft/TypeScript-go/issues/2201#issuecomment-3929174370)
    * @nnnnoel asked if the linked PR would be helpful in [microsoft/TypeScript-go#2302](https://github.com/microsoft/TypeScript-go/pull/2302#issuecomment-3930927747)
    * @JoostK asked whether the @typescript/ast and @typescript/api packages would become available on NPM during the preview phase in [microsoft/TypeScript-go#2813](https://github.com/microsoft/TypeScript-go/pull/2813#issuecomment-3935041074)
    * @jasonlyu123 asked if their proposed virtual content approach avoids module resolution callbacks and whether batch or empty-file update strategies would be preferable in [microsoft/TypeScript-go#2824](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-3931160146)
    * @remcohaszing pointed out incorrect naming for Vue declaration files and suggested using name.d.vue.ts in [microsoft/TypeScript-go#2824](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-3935034341)

## Activity Summary

### [PR microsoft/TypeScript-go#1149](https://github.com/microsoft/TypeScript-go/pull/1149) (Closed)

**Make \`anyFunctionType\` a subtype of all function types**

*Enable anyFunctionType to be recognized as a subtype of every function type in TypeScript.*

 * created by **ahejlsberg**
 * (36 weeks ago) **jakebailey** closed the issue
 * (today) **DanielRosenwasser** assigned to **Copilot**, and unassigned **Copilot**

### [Issue microsoft/TypeScript-go#1317](https://github.com/microsoft/TypeScript-go/issues/1317) (Open, `Domain: CLI`, `Domain: Performance`)

**High CPU usage with \-\-watch when idling on MacOS**

*Running tsgo in watch mode on MacOS consumes abnormally high CPU (120–170%) even when idle, unlike tsc -w.*

 * [30 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1317#issuecomment-3114602047) **tmm1** asked what it would take to get incremental and watch working together and reported a panic with stack trace
 * [30 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1317#issuecomment-3114860336) **sheetalkamat** said "@tmm1 please open new issue, providing repro steps to investigate the crash."
 * **jakebailey** added label `Domain: Performance`
 * [today](https://github.com/microsoft/TypeScript-go/issues/1317#issuecomment-3928808922) **nfarina** suggested adding fsevents support and a custom watcher.go to improve watch mode CPU usage by building a local tsgo binary

### [PR microsoft/TypeScript-go#2020](https://github.com/microsoft/TypeScript-go/pull/2020) (Open)

**Support for custom configurations**

*Enable passing custom tsconfig file names to the tsgo LSP to support solution-style repository configurations.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2020#issuecomment-3924738291) **jakebailey** tested a TypeScript configuration change with a custom tsconfig and observed that disabling strict removed the error but undoing the config didn't refresh diagnostics until restart, which he found suspicious
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2020#issuecomment-3924761855) **johnnycheng0210** reported similar behavior with findAllReferences when switching project configurations, observed that results didn't update after reverting to single project config, and asked why the old configuration persisted
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2020#issuecomment-3924764987) **johnnycheng0210** wondered if requiring a window reload between custom config file name changes would be preferred as a simpler approach
 * [today](https://github.com/microsoft/TypeScript-go/pull/2020#issuecomment-3928562337) **jakebailey** said "I'm definitely confused, because when I write a test for this, the test seemingly does the right thing."

### [Issue microsoft/TypeScript-go#2201](https://github.com/microsoft/TypeScript-go/issues/2201) (Open, `Crash`, **Copilot**)

**Bad formatting of multiline ternary expression**

*Formatting multiline ternary expressions with tabs results in inconsistent mixing of tabs and spaces.*

 * created by **mjbvz**
 * **mjbvz** added label `Crash`
 * **jakebailey** assigned to **Copilot**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2201#issuecomment-3929174370) **antichris** described additional misalignment issues in formatting of arrow functions and ternary expressions with leading and trailing commas, providing code examples of incorrect indentation

### [PR microsoft/TypeScript-go#2302](https://github.com/microsoft/TypeScript-go/pull/2302) (Open)

**API over LSP implementation**

*Implements a TS-Go API over the Language Server Protocol using custom messages and lazy-loaded types and symbols.*

 * [10 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2302#issuecomment-3631591516) **aleksei-berezkin** said "@microsoft-github-policy-service agree company="JetBrains""
 * [10 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2302#issuecomment-3631609367) **microsoft-github-policy-service[bot]** informed that the issued command was incorrect and provided correct usage examples
 * [10 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2302#issuecomment-3631616041) **aleksei-berezkin** said "@microsoft-github-policy-service agree company="JetBrains""
 * [today](https://github.com/microsoft/TypeScript-go/pull/2302#issuecomment-3930927747) **nnnnoel** asked if a linked PR would be helpful to support typescript-go in WebStorm
 * [later](https://github.com/microsoft/TypeScript-go/pull/2302#issuecomment-3932853572) **aleksei-berezkin** explained how to configure WebStorm to use TypeScript-Go via a dependency and npm install, and noted that the Service-Powered Type Engine is not yet implemented but available in a fork

### [Issue microsoft/TypeScript-go#2415](https://github.com/microsoft/TypeScript-go/issues/2415) (Closed, `Domain: Declaration Emit`, **weswigham**)

**TS2339: Property does not exist on type**

*Building babel-core with tsgo fails with TS2339 because traverse.visitors.merge isn’t defined on the traverse function type, unlike in TypeScript 5.9.*

 * [8 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2415#issuecomment-3679546005) **ahejlsberg** identified a declaration file emit issue where babel-traverse expando properties were missing from the generated .d.ts file
 * (8 weeks ago) **ahejlsberg** added label `Domain: Declaration Emit`, and assigned to **weswigham**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2623](https://github.com/microsoft/TypeScript-go/pull/2623) (Closed)

**Fix inlay hints panic: guard against stale line map in LineAndCharacterToPosition**

*Prevent inlay hint panics by guarding against stale line map offsets in LineAndCharacterToPosition*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2623#issuecomment-3837337190) **DanielRosenwasser** described two cases needing handling: '/resolve'-like requests with content length changes causing non-existent positions, and logic operating on nodes with source text from the wrong file; and noted the need to recalculate or dismiss outdated line maps
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2623#issuecomment-3837346475) **DanielRosenwasser** noted a potential issue with the snapshot implementation and explained that snapshots prevent data state inconsistencies
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2623#issuecomment-3849685810) **DanielRosenwasser** opened an issue to track discussion on unexplained issues
 * [today](https://github.com/microsoft/TypeScript-go/pull/2623#issuecomment-3930970703) **DanielRosenwasser** said "We appreciate the PR, but ultimately we don't feel like this is the right approach - but also, we think most cases in https://github.com/microsoft/typescript-go/issues/2682 have been resolved."
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#2643](https://github.com/microsoft/TypeScript-go/pull/2643) (Closed)

**Misc customlint updates**

*Proposes several long-planned refactors and enhancements for the customlint tool*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2682](https://github.com/microsoft/TypeScript-go/issues/2682) (Closed, `Crash`)

**Various language server commands crash during position retrieval**

*Language server commands like hover crash due to LineAndCharacterToPosition mapping errors potentially caused by outdated snapshots or other unknown conditions.*

 * created by **DanielRosenwasser**
 * **DanielRosenwasser** added label `Crash`
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2682#issuecomment-3849620766) **andrewbranch** described a code path introduced by PR #1767 that triggered disk reads for line map content and suggested separating disk-allowed reads to trigger a distinct panic when files aren’t found
 * [today](https://github.com/microsoft/TypeScript-go/issues/2682#issuecomment-3929484444) **DanielRosenwasser** said "Telemetry reporting implies that https://github.com/microsoft/typescript-go/pull/2765 probably fixed this."
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#2688](https://github.com/microsoft/TypeScript-go/pull/2688) (Open, **RyanCavanaugh**, **Copilot**)

**Port TypeScript PR \#63054: Default \`types\` to \`\[\]\`, support \`"\*"\` wildcard**

*Port TypeScript PR to make types default to an empty list and use '*' wildcard for automatic type package discovery.*

 * created by **Copilot**
 * (2 weeks ago) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2688#issuecomment-3930903832) **DanielRosenwasser** asked if an error update for core/built-in modules for Node.js was missing
 * [today](https://github.com/microsoft/TypeScript-go/pull/2688#issuecomment-3930910609) **jakebailey** said "@copilot Look into this; recheck the original PR for missing bits."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2688#issuecomment-3930958354) **Copilot** added the missing getCannotResolveModuleNameErrorForSpecificModule function, included beforeEach in test runner cases and NodeJS in node cases, and fixed in commit 6a48e64

### [Issue microsoft/TypeScript-go#2701](https://github.com/microsoft/TypeScript-go/issues/2701) (Open)

**Declaration emit for named inferred types used in further inference inlines inferred types instead of naming them**

*tsgo inlines inferred types in declaration emit even when named, causing slower type checking in consuming packages.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/2701#issuecomment-3861992981) **jakebailey** said "I would expect this to be fixed by #1693 / #2459, then."
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/2701#issuecomment-3863092956) **chriskrycho** confirmed that the change fixes the issue and reduces type-check time by ~95% (from ~469s to ~24s)
 * [today](https://github.com/microsoft/TypeScript-go/issues/2701#issuecomment-3927069363) **privatenumber** provided additional reproduction steps and real-world impact data showing tsgo produces significantly larger declaration output and errors compared to tsc
 * [today](https://github.com/microsoft/TypeScript-go/issues/2701#issuecomment-3928362389) **jakebailey** asked to report the missing .d.ts files separately
 * [today](https://github.com/microsoft/TypeScript-go/issues/2701#issuecomment-3928857325) **privatenumber** said "Sorry about that — the 48 missing files were a measurement error on my end. Both tsc and tsgo produce all 4,710 .d.ts files. I've updated my previous comment with corrected numbers."

### [Issue microsoft/TypeScript-go#2780](https://github.com/microsoft/TypeScript-go/issues/2780) (Open, `Domain: Editor`, `Needs More Info`, **andrewbranch**)

**High memory consumption in a large pnpm monorepo**

*PR #2502 causes minor edits in a large pnpm monorepo to spike the TypeScript extension memory from ~700MB to ~35GB.*

 * **jakebailey** assigned to **andrewbranch**
 * [6 days ago](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-3896509428) **neo773** reproduced the issue on their NestJS monorepo, noting memory usage spiked to ~25-30GB and shared a repository link
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-3906751144) **Moltenship** reported experiencing the same issue, provided a memory profile link, and suggested it might be related to version 0.20251122.1
 * [today](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-3931052114) **andrewbranch** tried to reproduce the memory issue in twentyhq/twenty, described memory usage spike and GC behavior, noted Go's memory retention characteristics, and provided instructions to enable trace logging, capture a heap profile, and copy cache statistics
 * **andrewbranch** added label `Needs More Info`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-3931729619) **shinichy** reported that tsgo got stuck, did not produce a `custom/saveHeapProfile` response in LSP logs, and missed cache statistics information when following reproduction steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-3931736730) **shinichy** said "@neo773 Are you able to reproduce this issue in https://github.com/twentyhq/twenty/? I couldn't reproduce this issue in the repo."

### [Issue microsoft/TypeScript-go#2792](https://github.com/microsoft/TypeScript-go/issues/2792) (Open, `Domain: API and Extensibility`, **andrewbranch**)

**\[Feature request\] Provide "Relater" typechecker api**

*Expose the internal Relater type-checker's isTypeAssignableTo method in the public TypeScript API*

 * created by **artem1458**
 * **DanielRosenwasser** added label `Domain: API and Extensibility`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2792#issuecomment-3929476730) **DanielRosenwasser** said "We're investigating stuff around this. #2831 adds more of the foundation of type-space APIs. I anticipate we'll have relater APIs as well."
 * **DanielRosenwasser** assigned to **andrewbranch**

### [Issue microsoft/TypeScript-go#2798](https://github.com/microsoft/TypeScript-go/issues/2798) (Closed, `Crash`)

**Panic in textDocument/diagnostics on private property assignment at "global" this**

*Assigning a private property to the global this context triggers a nil pointer dereference panic in TypeScript-Go’s LSP diagnostics*

 * created by **apendua**
 * **apendua** added label `Crash`
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/2798#issuecomment-3910617702) **apendua** identified that GetSymbolNameForPrivateIdentifier requires a non-null first argument but thisType.symbol was nil when this was undefined due to export {}
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#2799](https://github.com/microsoft/TypeScript-go/pull/2799) (Closed)

**Add nil assertion for thisType\.symbol**

*Add a nil assertion for thisType.symbol in GetSymbolNameForPrivateIdentifier to handle global this without a symbol.*

 * created by **apendua**
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#2813](https://github.com/microsoft/TypeScript-go/pull/2813) (Closed)

**New IPC API client features**

*Updates the TypeScript IPC API client to use immutable snapshots for state and lifecycle management and adds Go support code.*

 * created by **andrewbranch**
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/2813#issuecomment-3918014132) **andrewbranch** said "My handling of SourceFileAffectingOptions needs to be updated after Jake's changes in main. I think it wasn't quite right before, anyway."
 * (yesterday) **andrewbranch** closed the issue
 * [later](https://github.com/microsoft/TypeScript-go/pull/2813#issuecomment-3935041074) **JoostK** said "Will the @typescript/ast/@typescript/api packages become available on NPM during the preview phase?"

### [Issue microsoft/TypeScript-go#2824](https://github.com/microsoft/TypeScript-go/issues/2824) (Open, `Domain: API and Extensibility`, **andrewbranch**)

**API usage patterns for complex editor extensions**

*Exploring IPC-based API features for a Go TS server to replace TS Server plugins and support Vue editor extensions*

 * created by **andrewbranch**
 * (yesterday) **andrewbranch** added label `Domain: API and Extensibility`, and assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-3928927997) **chriskrycho** highlighted an additional consideration regarding the distinction between language server and CLI for type checking and emit, referencing Glint’s approach of patching tsc paths and synthesizing virtual modules
 * [today](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-3929259078) **auvred** valued CLI typechecking over LSP, expressed desire for TypeScript core to support extension languages, and listed existing workaround projects
 * [today](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-3929425669) **andrewbranch** explained that using the TS API to load a project and get diagnostics would allow transformed files to be substituted and diagnostic positions source-mapped, and argued that embedding the TS API in an external compiler is preferable to hosting plugins in the TS compiler
 * [today](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-3929470201) **remcohaszing** described how to use Volar to create a language server by processing embedded content into virtual files and leveraging existing language services, recommended using the Volar Labs extension to inspect virtual files, explained the transition from a TypeScript-based language server to a TypeScript plugin for improved IntelliSense interoperability, and noted that only the TypeScript plugin matters for current integration
 * [today](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-3929470783) **chriskrycho** argued that tsgo should embed the TypeScript API in an external tool's CLI rather than act as a plugin host, noting that users expect drop-in support for commands like --build and --watch and that the API should be rich enough to enable those features
 * [today](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-3929485280) **remcohaszing** explained that languages need to interoperate and that tsgo should act as a plugin host to provide both CLI and IntelliSense across mixed-language projects
 * [today](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-3929903997) **andrewbranch** explained that the API would support build and watch scenarios without becoming a general-purpose orchestrator, rejected the idea of injecting types via plugins, and described how the proposed architecture already enables multiple extensions to interoperate through a shared LSP server
 * [today](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-3930751819) **DanielRosenwasser** clarified that TypeScript --build still supports .vue and .astro files with parity to <=6.0 to enable tsc-like build experiences
 * [today](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-3930886681) **andrewbranch** asked whether the TypeScript 6.0 CLI supports that or if solution builder APIs must be used, and outlined expectations for the new API's capabilities
 * [today](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-3930924178) **DanielRosenwasser** clarified that he meant using the solution builder APIs instead of the CLI and suggested providing tools similar to the Vue CLI to handle project references and TypeScript file management
 * [today](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-3931160146) **jasonlyu123** described a prototype using LSP as an API with custom file extensions and virtual content requests, asked if this matched the module resolution callback scenario to avoid and suggested batch or empty-file update strategies, and referenced Svelte’s implementation and the need for project file extraction APIs
 * [later](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-3932331598) **remcohaszing** questioned how the --build option related, noted that plugin use implies noEmit, and discussed publishing practices for MDX, CSS, SVG, font, image, Astro, and Vue files
 * [later](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-3932403095) **auvred** provided information on using vue-tsc to emit .vue.d.ts files and noted Ember’s expectations for .d.ts files
 * [later](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-3935034341) **remcohaszing** said "I think this highlights another issue. name.vue.d.ts tells TypeScript there’s a file named name.vue.js. The correct name for a declaration file for a file named name.vue, is name.d.vue.ts."

### [Issue microsoft/TypeScript-go#2827](https://github.com/microsoft/TypeScript-go/issues/2827) (Closed, `Crash`, **andrewbranch**)

**panic handling request completionItem/resolve: completion list needs auto imports**

*A panic occurs in completionItem/resolve due to missing auto imports during Redocly/redoc fuzzer replay.*

 * **gabritto** added label `Crash`
 * **andrewbranch** assigned to **andrewbranch**
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2827#issuecomment-3924128232) **DanielRosenwasser** reproduced a completions crash after fiddling with settings and noted that custom.d.ts was included in tsconfig.json while styled-patch.d.ts was not
 * (today) **gabritto** closed the issue

### [Issue microsoft/TypeScript-go#2830](https://github.com/microsoft/TypeScript-go/issues/2830) (Open, `Type Ordering`)

**TS2859/TS2590: bigint template literal types composed with distributive conditional cause 'excessively deep' errors not present in tsc**

*bigint-based template literal types in JSX props cause tsgo to report excessive type complexity errors but not tsc*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2830#issuecomment-3924360036) **jlaneve** explained that the error was caused by tsgo’s instantiation limit being hit due to unresolved distributive conditional types combined with Chakra Input’s complex responsive props and confirmed the root cause was not Chakra-specific
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2830#issuecomment-3924382349) **jlaneve** provided a minimal repro demonstrating that the type complexity of InputProps triggers TS errors
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2830#issuecomment-3924386199) **jlaneve** said "in the spirit of transparency these comments / repros were generated with the help of claude code, but I figured it'd be worth posting because this is a real issue we're running into"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2830#issuecomment-3928610921) **ahejlsberg** described the problem as a type ordering issue replicable with `tsc --stableTypeOrdering` in TS 6.0 and noted it might occur with plain `tsc` too, concluding there's likely no fix
 * **ahejlsberg** added label `Type Ordering`

### [PR microsoft/TypeScript-go#2831](https://github.com/microsoft/TypeScript-go/pull/2831) (Closed)

**\[@typescript/api\] Batch of Checker and Type APIs**

*Add TypeScript API enhancements with checker queries, intrinsic type getters, symbol fetchers, type hierarchy classes, and new enums and flags.*

 * created by **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#2834](https://github.com/microsoft/TypeScript-go/pull/2834) (Closed)

**Optimize bool to byte conversion in API encoder**

*Optimize the Go API encoder by replacing slow bool-to-byte conversions with a more efficient implementation.*

 * created by **auvred**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2834#issuecomment-3929088387) **jakebailey** said "In context, is this actually faster? I'm pretty sure this function is simple enough to be inlined and so its implementation not matter."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2834#issuecomment-3929348913) **auvred** reported the branch ran faster on their machine despite a low battery
 * [today](https://github.com/microsoft/TypeScript-go/pull/2834#issuecomment-3929487045) **auvred** said "Well, it does indeed inline boolToByte, producing identical asm https://godbolt.org/z/vhdq7bxWa!"
 * (today) **auvred** closed the issue

### [PR microsoft/TypeScript-go#2835](https://github.com/microsoft/TypeScript-go/pull/2835) (Closed)

**6\.4x speedup of AST materialization in JS API**

*Several optimizations in the JavaScript API speed up AST materialization by 6.4× and correct benchmarks by resetting the source file cache.*

 * created by **auvred**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2835#issuecomment-3928471535) **andrewbranch** explained that initializing all source file nodes upfront skews the benchmark because it’s designed for a worst-case scenario and real-world use cases lazily materialize only a small fraction of nodes
 * [today](https://github.com/microsoft/TypeScript-go/pull/2835#issuecomment-3928531012) **auvred** suggested adding an opt-in eager materialization after researching tsgo-powered JS lint rules that touch up to 80% of AST nodes and noting that lazy materialization is slower than parsing with Strada
 * [today](https://github.com/microsoft/TypeScript-go/pull/2835#issuecomment-3928571317) **andrewbranch** said "Yeah, an option to do that would be great! It makes sense that a linter would want to look at the whole file."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2835#issuecomment-3928909689) **auvred** reverted getOrCreateChildAtNodeIndex to lazy materialization after finding performance nearly equivalent to bulk materialization

### [Issue microsoft/TypeScript-go#2836](https://github.com/microsoft/TypeScript-go/issues/2836) (Open)

**Cache \`getExePath\(\)\` for performance reasons**

*Cache getExePath results to avoid redundant lookups and improve tsgo invocation performance.*

 * created by **tido64**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2836#issuecomment-3928400257) **jakebailey** questioned where caching would occur and explained why postinstall is avoided and no slowdown seems to come from platform checks
 * [today](https://github.com/microsoft/TypeScript-go/issues/2836#issuecomment-3928421769) **jakebailey** said "If the import is that slow, we could switch to using plain FS lookups, since peer deps must be "peers" in a parent dir..."

### [PR microsoft/TypeScript-go#2837](https://github.com/microsoft/TypeScript-go/pull/2837) (Closed)

**Clone comment list of reparsed JSDoc comments**

*Clone the comment list of reparsed JSDoc comments to prevent the reported crash.*

 * created by **ahejlsberg**
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#2838](https://github.com/microsoft/TypeScript-go/pull/2838) (Closed)

**Emit declaration when expando property on overloaded functions**

*Emit expando property declarations on overloaded functions only once instead of per overload*

 * created by **liuxingbaoyu**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2839](https://github.com/microsoft/TypeScript-go/issues/2839) (Closed, `bug`, `Domain: Editor`, **DanielRosenwasser**, **Copilot**)

**Cannot "go to definition" of a playwright fixture**

*Editors cannot navigate to definitions of custom Playwright fixtures when using tsgo, though TypeScript 6 supports it.*

 * created by **david-guevara-gorillalogic**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2839#issuecomment-3929597143) **DanielRosenwasser** explained issue with VS Code's alternativeDefinitionCommand, provided a minimal repro and suggested a test baseline
 * (today) **DanielRosenwasser** added labels `bug`, `Domain: Editor`, and assigned to **Copilot**, **DanielRosenwasser**

### [PR microsoft/TypeScript-go#2840](https://github.com/microsoft/TypeScript-go/pull/2840) (Closed)

**Use a plain relative path for getExePath**

*Use a simple relative path in getExePath instead of import.meta.resolve because peer dependencies ensure sibling placement.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2841](https://github.com/microsoft/TypeScript-go/pull/2841) (Closed)

**Fix \`completionItem/resolve\` auto imports crash**

*Prevent completionItem/resolve crashes by removing auto-imports data collection and using existing completion item data.*

 * created by **gabritto**
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript-go#2842](https://github.com/microsoft/TypeScript-go/pull/2842) (Closed, **DanielRosenwasser**, **Copilot**)

**Fix go\-to\-definition for binding elements in ObjectBindingPattern**

*Add and test go-to-definition support for object destructuring binding elements, including rest patterns, and update test baselines accordingly.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **DanielRosenwasser**

### [Issue microsoft/TypeScript-go#2843](https://github.com/microsoft/TypeScript-go/issues/2843) (Closed, **ahejlsberg**)

**Difference in typechecking results for a TSX file in 7\.0\.0\-dev\.20260218\.1 and later**

*A tsgo regression in v7.0.0-dev.20260218.1+ causes Formik onSubmit handler types to mismatch in TSX files, unlike TS 6.0 or earlier tsgo versions.*

 * created by **connorshea**
 * **jakebailey** assigned to **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2843#issuecomment-3930759122) **ahejlsberg** believed the tsgo error was correct and showed the same error occurred with tsc, noted that PR #2803 was merged to fix type inference and align behavior, and said it would be back-ported to TS 6.0
 * [today](https://github.com/microsoft/TypeScript-go/issues/2843#issuecomment-3931756312) **DanielRosenwasser** said "We're looking to bring this behavior back to 6.0 https://github.com/microsoft/TypeScript/pull/63163"

### [PR microsoft/TypeScript-go#2844](https://github.com/microsoft/TypeScript-go/pull/2844) (Closed)

**Add nil check in \`getAllExportsForSymbol\`**

*Add a nil check to getAllExportsForSymbol to prevent crashes when symbol exports are undefined.*

 * created by **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2844#issuecomment-3930454842) **ahejlsberg** said "I did not extract a stand-alone repro as the code is somewhat involved. Another fuzzer run should demonstrate that the issue has been fixed."
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#2845](https://github.com/microsoft/TypeScript-go/pull/2845) (Closed)

**Codegen sync API and all enums**

*Replace sync API code (types, implementation, tests, benchmarks) with async-generated counterparts and auto-generate TypeScript enums from Go source.*

 * created by **andrewbranch**

### [PR microsoft/TypeScript-go#2846](https://github.com/microsoft/TypeScript-go/pull/2846) (Closed)

**Fix emit for non\-local/merged enum/namespace references**

*Fix code emission for non-local and merged enum and namespace references.*

 * created by **jakebailey**

### [Issue microsoft/TypeScript-go#2847](https://github.com/microsoft/TypeScript-go/issues/2847) (Closed, `Crash`, **DanielRosenwasser**)

**panic on go\-to\-type\-definition of tuple type**

*Go-to-type-definition on a tuple type triggers a nil pointer dereference panic in the TypeScript-Go language server.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** added label `Crash`, and assigned to **DanielRosenwasser**
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#2848](https://github.com/microsoft/TypeScript-go/pull/2848) (Closed)

**Fix go\-to\-type\-definition on tuples**

*Add guard logic for symbol-less tuple types to restore go-to-type-definition functionality.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#2849](https://github.com/microsoft/TypeScript-go/pull/2849) (Closed)

**Fix parse cache key not found**

*Move auto-imports host disposal after marking program files as referenced to prevent missing parse cache keys.*

 * created by **gabritto**

### [Issue microsoft/TypeScript-go#2850](https://github.com/microsoft/TypeScript-go/issues/2850) (Open, **andrewbranch**)

**Add \`\.getNonPrimitiveType\(\)\` getter**

*The API is missing the recently introduced .getNonPrimitiveType() getter that exists in Strada.*

 * created by **mrazauskas**

### [Issue microsoft/TypeScript-go#2851](https://github.com/microsoft/TypeScript-go/issues/2851) (Open, **andrewbranch**)

**Add \`\.getTrueType\(\)\` and \`\.getFalseType\(\)\` to \`ConditionalType\`**

*Add getTrueType() and getFalseType() methods to ConditionalType so it returns instantiated true and false branch types.*

 * created by **mrazauskas**

### [PR microsoft/TypeScript-go#2852](https://github.com/microsoft/TypeScript-go/pull/2852) (Closed)

**Fixed an always\-truthy condition in span\`\.go\` \(porting bug\)**

*A condition in span.go was always true due to a porting bug and has been fixed.*

 * created by **Andarist**

### [Issue microsoft/TypeScript-go#648](https://github.com/microsoft/TypeScript-go/issues/648) (Open, `Domain: API and Extensibility`)

**Support embedded JavaScript/TypeScript**

*Enable built-in handling of embedded JavaScript/TypeScript in languages such as MDX, Vue, Svelte, Astro, and Markdown in the Go rewrite.*

 * [9 weeks ago](https://github.com/microsoft/TypeScript-go/issues/648#issuecomment-3655911105) **jasonlyu123** suggested structuring the TypeScript rewrite to officially support custom file extensions and enhance LSP integration
 * [7 weeks ago](https://github.com/microsoft/TypeScript-go/issues/648#issuecomment-3699022588) **ItsHarper** asked why extensions couldn't interoperate and explained that compiler forks can’t interoperate without merging all changes
 * [7 weeks ago](https://github.com/microsoft/TypeScript-go/issues/648#issuecomment-3699085966) **auvred** suggested that a unified plugin architecture could allow language extensions to run in separate processes and be written in any language and noted that tsgo would be a nicer plugin host
 * [today](https://github.com/microsoft/TypeScript-go/issues/648#issuecomment-3928741504) **andrewbranch** opened a related issue (#2824) and requested expert feedback

