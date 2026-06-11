# Report for 2026-06-10 (Wednesday, June 10th, 2026)

17 different users commented on 46 different issues.

## Recommended Actions

 * Response Recommended
    * @klydra provided logs and settings as requested in [microsoft/TypeScript-go#4259](https://github.com/microsoft/TypeScript-go/issues/4259#issuecomment-4682036453)

## Activity Summary

### [Issue microsoft/TypeScript-go#1701](https://github.com/microsoft/TypeScript-go/issues/1701) (Closed, `help wanted`, **jakebailey**)

**surrogate pair and lone surrogate support in stringLiteral**

*tsgo's Go based stringLiteral parser converts lone UTF-16 surrogates into replacement characters, causing lossy token text compared to TypeScript.*

 * [38 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1701#issuecomment-3283625905) **jakebailey** said "Sure, though we of course can't use the syscall package to do this."
 * **RyanCavanaugh** added to milestone `Possible Improvement`
 * **jakebailey** assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3305](https://github.com/microsoft/TypeScript-go/pull/3305) (Open, **DanielRosenwasser**, **Copilot**)

**Add "Sort Imports" & "Remove Unused Imports" commands to VS Code extension**

*Dynamically register Sort Imports and Remove Unused Imports commands in VS Code extension to delegate to built-in actions.*

 * **Copilot** assigned to **DanielRosenwasser**
 * [8 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3305#issuecomment-4256048203) **azure-pipelines[bot]** reported that one pipeline was filtered out due to trigger conditions
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * [today](https://github.com/microsoft/TypeScript-go/pull/3305#issuecomment-4672884790) **iisaduan** said "I remember @DanielRosenwasser was doing some work about commands with duplicated names in the extension. Is that done/are these actions affected?"

### [PR microsoft/TypeScript-go#3397](https://github.com/microsoft/TypeScript-go/pull/3397) (Closed)

**Use GHA runners instead of custom runners**

*Benchmarking shows GitHub-hosted runners run jobs roughly twice as slow as custom runners, questioning their necessity.*

 * created by **jakebailey**
 * **RyanCavanaugh** added to milestone `Possible Improvement`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3489](https://github.com/microsoft/TypeScript-go/issues/3489) (Closed, `bug`, **iisaduan**)

**Lowercase\<"İ"\>\` differs between tsgo and tsc \(Go strings\.ToLower vs JS String\.prototype\.toLowerCase\)**

*tsgo’s Lowercase intrinsic uses Go’s strings.ToLower rather than ECMAScript’s full Unicode case mapping, causing mismatched lowercase results for characters like 'İ'*

 * (5 weeks ago) **RyanCavanaugh** added label `bug`, set milestone to `TypeScript 7.0 RC`, and assigned to **iisaduan**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3495](https://github.com/microsoft/TypeScript-go/pull/3495) (Closed)

**Use JS\-compatible Unicode casing for intrinsic string mappings**

*Update TypeScript’s intrinsic string mappings to apply JavaScript-compatible Unicode casing rules.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3495#issuecomment-4599345981) **Andarist** questioned whether tests were required for all 267 items, noting an existing unit test included a single example of divergence
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3495#issuecomment-4600953236) **jakebailey** said "No, not all of them I don't think, but a few. Or some sort of way to generate them and then use https://github.com/microsoft/typescript-go/tree/main/internal/testutil/jstest to cross check?"
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3495#issuecomment-4615709778) **jakebailey** said "Just to be clear, I think this PR is fine after my suggested changes. Unfortunate that this is required but obviously JS and Unicode are a terrible pair"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3495#issuecomment-4674543934) **jakebailey** listed changes to surrogate handling, rune conversion, unicode data sourcing, identifier data generation, and unicode version pinning
 * [today](https://github.com/microsoft/TypeScript-go/pull/3495#issuecomment-4674804028) **jakebailey** switched to unicode.RangeTable from surrogate pair slices, reduced binary size by 40%, improved speed by up to 3.3×, and reduced code
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3617](https://github.com/microsoft/TypeScript-go/issues/3617) (Open, `Voight-Kampff Anomaly`, **iisaduan**)

**fix: FindBestPatternMatch incorrectly allows wildcard pattern to override exact match**

*FindBestPatternMatch misuses StarIndex so exact matches set longestMatchPrefixLength to -1, allowing later wildcard patterns to override exact matches.*

 * [1 month ago](https://github.com/microsoft/TypeScript-go/issues/3617#issuecomment-4401880065) **RyanCavanaugh** said "@kuishou68 how does this manifest? There's no external-visible behavorial description nor testcase in that PR, so it's hard to know the severity/priority of this"
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/3617#issuecomment-4592514890) **matyasf** described reproduction steps demonstrating incorrect import paths when building with tsgo in a composite TypeScript project
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/3617#issuecomment-4615071752) **andrewbranch** said "I reduced @matyasf's repro to a compiler test and found that it's not fixed by #3618, so probably not related to this issue."
 * (today) **iisaduan** added label `Voight-Kampff Anomaly`, and removed label `Needs Investigation`

### [Issue microsoft/TypeScript-go#3727](https://github.com/microsoft/TypeScript-go/issues/3727) (Open, `Domain: Editor`, `possible improvement`, **jakebailey**)

**Unify tsdk between built\-in and native preview extensions**

*Share the built-in tsdk setting with the native preview and choose the TypeScript server based on useTsGo and tsdk directory.*

 * (3 weeks ago) **DanielRosenwasser** set milestone to `TypeScript 7.0 RC`, and removed from milestone `Possible Improvement`
 * **RyanCavanaugh** assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3727#issuecomment-4674335592) **DanielRosenwasser** outlined a step-by-step approach to determine whether to activate Strada, Corsa, or built-in TypeScript servers based on tsdk and useTsgo settings, including precedence and folder validation
 * [today](https://github.com/microsoft/TypeScript-go/issues/3727#issuecomment-4674445561) **andrewbranch** proposed a flowchart outlining the priority of settings in deciding between Corsa and Strada and the TypeScript SDK

### [PR microsoft/TypeScript-go#3765](https://github.com/microsoft/TypeScript-go/pull/3765) (Closed, **jakebailey**, **Copilot**)

**Fix custom tsgo path: read from \`js/ts\.tsdk\.path\` unified setting**

*Support reading custom tsgo binary path from unified js/ts.tsdk.path setting with fallback to typescript.native-preview.tsdk.*

 * (1 month ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3834](https://github.com/microsoft/TypeScript-go/pull/3834) (Open)

**add localization for extension**

*Add localization support to the TypeScript VS Code extension by integrating non-English translation files and enabling pseudo-language testing.*

 * created by **iisaduan**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * [today](https://github.com/microsoft/TypeScript-go/pull/3834#issuecomment-4675814391) **DanielRosenwasser** said "This is basically good to go, but I'm wondering if @jakebailey has thoughts on the generation."

### [Issue microsoft/TypeScript-go#3899](https://github.com/microsoft/TypeScript-go/issues/3899) (Closed, **jakebailey**, **Copilot**)

**tsgo breaks type soundness for lone\-surrogate string literals**

*tsgo improperly accepts assignments between different lone-surrogate string literals, breaking TypeScript’s type soundness.*

 * (3 weeks ago) **jakebailey** assigned to **Copilot**, **jakebailey**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4045](https://github.com/microsoft/TypeScript-go/issues/4045) (Closed, `bug`, `Domain: Declaration Emit`, `Domain: JS`, `Needs Investigation`, **weswigham**)

**Behavior difference: Notable gap regarding expando declaration on a function between tsc & tsgo**

*tsgo aliases bound functions without namespaces compared to tsc, causing inconsistent type emissions for both PublicInternalBinding and PublicExportedBinding.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/4045#issuecomment-4553479379) **hkleungai** expressed hope that tsgo continued to support expando types and requested a fix for Storybook CSF2 syntax
 * (5 days ago) **RyanCavanaugh** set milestone to `TypeScript 7.0 RC`, and assigned to **weswigham**
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript-go#4069](https://github.com/microsoft/TypeScript-go/pull/4069) (Closed, `Voight-Kampff Anomaly`)

**Fix JS bind expando declaration emit**

*Emit bound JS functions as proper function declarations with preserved expando properties instead of const alias types*

 * created by **cjc0013**
 * (1 week ago) **RyanCavanaugh** added label `Voight-Kampff Anomaly`, and set milestone to `TypeScript 7.0 RC`
 * [today](https://github.com/microsoft/TypeScript-go/pull/4069#issuecomment-4674394852) **weswigham** said "Superseded by #4261"
 * (today) **weswigham** closed the issue

### [Issue microsoft/TypeScript-go#4071](https://github.com/microsoft/TypeScript-go/issues/4071) (Closed, `bug`, **jakebailey**)

**Behavior difference: Emoji string in tsgo emit does not align well with tsc**

*Emoji-containing string literal types emit differently in tsgo than tsc, causing misalignment after recent emoji handling fixes.*

 * **RyanCavanaugh** added label `bug`
 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/4071#issuecomment-4634923755) **RyanCavanaugh** said "The ones where we keep the emoji as-is are Good Actually, but foo and bar not good"
 * **RyanCavanaugh** added to milestone `Possible Improvement`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4092](https://github.com/microsoft/TypeScript-go/issues/4092) (Closed, `bug`, **jakebailey**, **Copilot**)

**Lone surrogate in enum member name / const enum value is corrupted to U\+FFFD in emitted JS**

*tsgo emits U+FFFD in place of lone surrogates in enum member names and const enum values in the generated JavaScript*

 * **jakebailey** assigned to **jakebailey**
 * (5 days ago) **RyanCavanaugh** added label `bug`, and set milestone to `TypeScript 7.0 RC`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4101](https://github.com/microsoft/TypeScript-go/issues/4101) (Open, `Needs More Info`)

**Declaration emit spends significant CPU in getAliasForSymbolInContainer / getAlternativeContainingModules**

*Declaration emit spends excessive CPU time in getAlternativeContainingModules and getAliasForSymbolInContainer, causing slow builds.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/4101#issuecomment-4606820385) **jakebailey** said "It would be good to be able to get access to this, I'm not really sure I like the way #4102 looks..."
 * (1 week ago) **RyanCavanaugh** added label `Needs More Info`, and set milestone to `Possible Improvement`
 * [later](https://github.com/microsoft/TypeScript-go/issues/4101#issuecomment-4680575783) **Zzzen** offered sanitized profiling data and willingness to run experiments and adjust patch

### [Issue microsoft/TypeScript-go#4118](https://github.com/microsoft/TypeScript-go/issues/4118) (Closed, `bug`, `Domain: Declaration Emit`, **weswigham**)

**Declaration emit drops expando function properties whose assignments are not top\-level expression statements**

*Tsgo's declaration emitter only emits expando function properties assigned as top-level statements and drops those assigned within initializers or blocks.*

 * (6 days ago) **ahejlsberg** added labels `bug`, `Domain: Declaration Emit`, and set milestone to `TypeScript 7.0 RC`
 * (today) **weswigham** closed the issue

### [Issue microsoft/TypeScript-go#4119](https://github.com/microsoft/TypeScript-go/issues/4119) (Closed, `bug`, **jakebailey**)

**U\+2028/U\+2029 inside a multi\-line comment leaves 2 stray bytes in emitted JS \(invalid UTF\-8\)**

*tsgo outputs invalid UTF-8 stray bytes when emitting multi-line comments containing U+2028/U+2029 line separators*

 * **jakebailey** assigned to **jakebailey**
 * (5 days ago) **RyanCavanaugh** added label `bug`, and set milestone to `TypeScript 7.0 RC`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4131](https://github.com/microsoft/TypeScript-go/issues/4131) (Closed, `bug`, **jakebailey**, **Copilot**)

**tsgo silently swallows JSON syntax errors in an extended tsconfig\.json file**

*tsgo silently ignores JSON syntax errors in extended tsconfig.json files, causing invalid configurations to go unreported.*

 * **jakebailey** assigned to **jakebailey**
 * (5 days ago) **RyanCavanaugh** added label `bug`, and set milestone to `TypeScript 7.0 RC`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4141](https://github.com/microsoft/TypeScript-go/pull/4141) (Closed, **jakebailey**, **Copilot**)

**Report JSON syntax errors from extended tsconfig files**

*tsgo now surfaces JSON parsing errors from extended tsconfig files by propagating parser diagnostics and adding regression tests*

 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * [6 days ago](https://github.com/microsoft/TypeScript-go/pull/4141#issuecomment-4621270410) **jakebailey** said "@copilot merge main"
 * [6 days ago](https://github.com/microsoft/TypeScript-go/pull/4141#issuecomment-4621380827) **Copilot** merged origin/main, resolved the tsconfig parsing test conflict while preserving both tests, and confirmed validation passed
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4181](https://github.com/microsoft/TypeScript-go/pull/4181) (Closed)

**Fix a slew of UTF\-8/UTF\-16 related issues**

*A series of UTF-8 and UTF-16 encoding bugs are fixed and updates applied across multiple related issues.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4181#issuecomment-4618040141) **jakebailey** described challenges with UTF-16 surrogate normalization and ambiguity around template string types, and noted attempting fixes in the last push
 * [6 days ago](https://github.com/microsoft/TypeScript-go/pull/4181#issuecomment-4622169728) **Utsav006** mentioned a previous workaround for handling split UTF-16 surrogates using Go's utf16.EncodeRune to bypass the re-normalization trap during inference
 * [6 days ago](https://github.com/microsoft/TypeScript-go/pull/4181#issuecomment-4623423327) **jakebailey** said "I'll have to think about that, there's just more than just this one place..."
 * [today](https://github.com/microsoft/TypeScript-go/pull/4181#issuecomment-4672263212) **gabritto** said "What's the issue for tracking intrinsic string mapping?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4181#issuecomment-4672787653) **jakebailey** provided the tracking issue link for intrinsic string mapping
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4198](https://github.com/microsoft/TypeScript-go/pull/4198) (Closed, **jakebailey**, **Copilot**)

**Emit nested expando function assignments in declarations**

*Extend declaration emitter to include nested expando function property assignments within initializers and blocks.*

 * (6 days ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * [4 days ago](https://github.com/microsoft/TypeScript-go/pull/4198#issuecomment-4638216073) **hkleungai** said "Just curious, is this PR also solving the issue I raised in https://github.com/microsoft/typescript-go/issues/4045? If not, also fine :)"
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript-go#4238](https://github.com/microsoft/TypeScript-go/pull/4238) (Open, `No linked issue`)

**Several performance optimizations for the scanner's hot path**

*Various per-commit optimizations to the scanner's hot path improve parsing performance by about 9.4% while keeping memory usage stable.*

 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/4238#issuecomment-4652885657) **jakebailey** criticized the hand-inlining in recent commits and asked to reorganize charAndSize to use outlined slow path with fast inlined path
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/4238#issuecomment-4653588903) **mds-ant** said "That's good feedback. Let me see if we can leverage the "outlined" optimization approach here."
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4238#issuecomment-4658478731) **mds-ant** introduced a new scanASCIIWhile helper to efficiently advance the scanner over ASCII bytes when other inlining approaches exceeded the 80-byte budget
 * [later](https://github.com/microsoft/TypeScript-go/pull/4238#issuecomment-4681769016) **jakebailey** said "@typescript-bot test it"
 * [later](https://github.com/microsoft/TypeScript-go/pull/4238#issuecomment-4681774807) **jakebailey** said "@typescript-bot perf test this faster"
 * [later](https://github.com/microsoft/TypeScript-go/pull/4238#issuecomment-4681775810) **typescript-automation[bot]** reported that performance test jobs were started and provided status and results links
 * [later](https://github.com/microsoft/TypeScript-go/pull/4238#issuecomment-4682011926) **typescript-automation[bot]** reported the requested performance run results
 * [later](https://github.com/microsoft/TypeScript-go/pull/4238#issuecomment-4682146434) **jakebailey** said "I like where this PR is now; much more contained. Are you planning on pushing anything else?"
 * [later](https://github.com/microsoft/TypeScript-go/pull/4238#issuecomment-4682201403) **mds-ant** mentioned having another scanner change to propose in a separate PR and indicated the current PR was ready for review

### [Issue microsoft/TypeScript-go#4259](https://github.com/microsoft/TypeScript-go/issues/4259) (Open, `Crash`)

**panic: cache entry not found \[recovered, repanicked\] \- exponentially increasingly random sporadic crashes until full VSCode Restart**

*Intermittent ‘cache entry not found’ panics in typescript-go cause exponentially increasing VSCode crashes until a full restart.*

 * created by **klydra**
 * **klydra** added label `Crash`
 * [later](https://github.com/microsoft/TypeScript-go/issues/4259#issuecomment-4678451986) **DanielRosenwasser** noted difficulty reproducing and asked if ESLint was the only extension performing actions on save and if TypeScript was formatting/organizing imports on save
 * [later](https://github.com/microsoft/TypeScript-go/issues/4259#issuecomment-4682036453) **klydra** described isolating ESLint as the only extension performing transformations on save and shared configuration settings and logs

### [PR microsoft/TypeScript-go#4260](https://github.com/microsoft/TypeScript-go/pull/4260) (Open)

**Fix stack overflow caused by simplification of recursive type**

*TypeScript now removes self-referential indexed access types from unions during simplification to prevent infinite recursion.*

 * [today](https://github.com/microsoft/TypeScript-go/pull/4260#issuecomment-4671766785) **ahejlsberg** said "@typescript-bot test this"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4260#issuecomment-4671849860) **jakebailey** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4260#issuecomment-4671857206) **jakebailey** said "Ah, GitHub outage "
 * [today](https://github.com/microsoft/TypeScript-go/pull/4260#issuecomment-4673043964) **jakebailey** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4260#issuecomment-4673050307) **jakebailey** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4260#issuecomment-4673053762) **jakebailey** said "@typescript-bot test top800"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4260#issuecomment-4673054365) **typescript-automation[bot]** reported build status for the test top800 command, indicating it started and completed with links
 * [today](https://github.com/microsoft/TypeScript-go/pull/4260#issuecomment-4673703508) **typescript-automation[bot]** provided the results of running the top 800 repos with tsc comparing main and the PR merge and noted everything looked good

### [PR microsoft/TypeScript-go#4261](https://github.com/microsoft/TypeScript-go/pull/4261) (Closed)

**Walk entire file for expando properties and emit them into declarations**

*Collect all file-wide expando properties and emit them in a single namespace declaration with nested support and diagnostic deduplication.*

 * created by **weswigham**
 * (today) **weswigham** closed the issue

### [Issue microsoft/TypeScript-go#4262](https://github.com/microsoft/TypeScript-go/issues/4262) (Open)

**Non\-deterministic \`TS2305 "has no exported member"\` errors across project references with \`\-\-emitDeclarationOnly\`**

*Flaky TS2305 "has no exported member" errors occur when running --emitDeclarationOnly across project references in a pnpm monorepo using tsgo.*

 * created by **benkeen**

### [PR microsoft/TypeScript-go#4263](https://github.com/microsoft/TypeScript-go/pull/4263) (Open)

**TS GO API: add getCompletionsAtPosition to the API and support includeSymbols**

*Add getCompletionsAtPosition API with includeSymbols support by defining internal CompletionList and CompletionItem types.*

 * created by **piotrtomiak**
 * **RyanCavanaugh** added to milestone `Post-7.0`

### [PR microsoft/TypeScript-go#4264](https://github.com/microsoft/TypeScript-go/pull/4264) (Open)

**Walk class children to find this property assignments beyond top level**

*Walk class members to detect nested this.property assignments during JavaScript declaration emission*

 * created by **weswigham**

### [Issue microsoft/TypeScript-go#4265](https://github.com/microsoft/TypeScript-go/issues/4265) (Open, `Crash`, **DanielRosenwasser**, **Copilot**)

**Fatal error from \`nil\` \`Statements\` in JSON source file**

*Parsing a JSON config file with nil Statements in the source file creation triggers a fatal error.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** added label `Crash`, and assigned to **Copilot**, **DanielRosenwasser**

### [PR microsoft/TypeScript-go#4266](https://github.com/microsoft/TypeScript-go/pull/4266) (Open, **DanielRosenwasser**, **Copilot**)

**\[WIP\] Fix fatal error from nil statements in JSON source file**

*Add a failing regression test and implement a minimal fix to prevent nil-statement fatal errors in JSON configs*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **DanielRosenwasser**

### [Issue microsoft/TypeScript-go#4267](https://github.com/microsoft/TypeScript-go/issues/4267) (Open, `Crash`, **DanielRosenwasser**, **Copilot**)

**Unknown file type\(?\) triggers fatal server crash**

*Loading a file with an unrecognized type intermittently triggers a fatal server crash during parsing.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** added label `Crash`, and assigned to **Copilot**, **DanielRosenwasser**

### [PR microsoft/TypeScript-go#4268](https://github.com/microsoft/TypeScript-go/pull/4268) (Open, **DanielRosenwasser**, **Copilot**)

**Avoid project crash for unknown file types**

*Default unknown file script kinds to TypeScript to prevent parser panics when opening unrecognized file types.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **DanielRosenwasser**

### [Issue microsoft/TypeScript-go#4269](https://github.com/microsoft/TypeScript-go/issues/4269) (Open, **DanielRosenwasser**, **Copilot**)

**Fatal error when project reference objects have unexpected types for \`path\` and \`circular\`**

*tsconfig parsing crashes when project references specify non-string values for path or circular properties.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** assigned to **Copilot**, **DanielRosenwasser**

### [PR microsoft/TypeScript-go#4270](https://github.com/microsoft/TypeScript-go/pull/4270) (Open, **DanielRosenwasser**, **Copilot**)

**Fix fatal error when project reference objects have unexpected types for path and circular**

*parseProjectReference now uses safe comma-ok type checks to avoid panics on invalid path or circular values and emit existing diagnostics*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **DanielRosenwasser**

### [PR microsoft/TypeScript-go#4271](https://github.com/microsoft/TypeScript-go/pull/4271) (Closed)

**feat: add shim packages exposing internal compiler API for psgen \(PAR\-19\)**

*Add shim packages re-exporting TypeScript compiler API for psgen with a smoke test and documented fork policy and upgrade cadence.*

 * created by **clintonjrobinson**
 * (today) **clintonjrobinson** closed the issue

### [Issue microsoft/TypeScript-go#4272](https://github.com/microsoft/TypeScript-go/issues/4272) (Open)

**LSP: initialize rejected when initializationOptions is null**

*tsgo's LSP server rejects null initializationOptions values contrary to the LSP specification, preventing Emacs lsp-mode from initializing properly.*

 * created by **Macavirus**

### [PR microsoft/TypeScript-go#4273](https://github.com/microsoft/TypeScript-go/pull/4273) (Open)

**API: Add declaration property to IndexInfo\.**

*Add the missing declaration property to the IndexInfo object to enable WebStorm integration.*

 * created by **piotrtomiak**

### [PR microsoft/TypeScript-go#4274](https://github.com/microsoft/TypeScript-go/pull/4274) (Open)

**Fix CFA stack overflow crash in for loops where initializer throws**

*Add an early bailout in for-loop binding to avoid stack overflow when the initializer throws*

 * created by **ibesuperv**
 * [later](https://github.com/microsoft/TypeScript-go/pull/4274#issuecomment-4679008732) **ibesuperv** agreed with microsoft-github-policy-service

### [Issue microsoft/TypeScript-go#4275](https://github.com/microsoft/TypeScript-go/issues/4275) (Open, **jakebailey**, **Copilot**)

**\`tsconfig\.json\` included as JSON input reports TS1006 self\-reference**

*Importing and including tsconfig.json causes a TS1006 self-reference error in tsgo 7.0.0-dev.20260610.1 but not in TypeScript 6.0.3*

 * created by **rubenferreira97**
 * (later) **jakebailey** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#4276](https://github.com/microsoft/TypeScript-go/pull/4276) (Closed)

**API: Fix nil panic for instantiated types**

*Nil pointer dereference crash when retrieving instantiated types in TS Go API proxy during tests*

 * created by **piotrtomiak**
 * (later) **piotrtomiak** closed the issue

### [PR microsoft/TypeScript-go#4277](https://github.com/microsoft/TypeScript-go/pull/4277) (Closed)

**perf\(checker\): defer orderedSet map allocation until \>16 elements**

*Defer orderedSet map allocation until exceeding 16 elements to reduce memory allocations and improve type intersection performance.*

 * created by **mds-ant**
 * [later](https://github.com/microsoft/TypeScript-go/pull/4277#issuecomment-4681757884) **jakebailey** said "@typescript-bot perf test this"
 * [later](https://github.com/microsoft/TypeScript-go/pull/4277#issuecomment-4681758786) **typescript-automation[bot]** reported that performance test jobs had started and provided links to build and results
 * [later](https://github.com/microsoft/TypeScript-go/pull/4277#issuecomment-4681988280) **typescript-automation[bot]** reported the results of the requested performance run
 * (later) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4278](https://github.com/microsoft/TypeScript-go/pull/4278) (Open)

**API: Fix nil panic for instantiated types**

*Nil pointer dereference crash when retrieving instantiated types in TS Go API proxy during tests*

 * created by **piotrtomiak**

### [PR microsoft/TypeScript-go#4279](https://github.com/microsoft/TypeScript-go/pull/4279) (Open, **jakebailey**, **Copilot**)

**Fix false TS1006 for included tsconfig JSON imports**

*Restrict self-reference diagnostics to triple-slash references and prevent included tsconfig.json imports from incorrectly triggering TS1006 errors.*

 * created by **Copilot**
 * (later) **Copilot** assigned to **Copilot**, **jakebailey**

