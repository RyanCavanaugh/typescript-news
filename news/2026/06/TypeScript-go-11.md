# Report for 2026-06-11 (Thursday, June 11th, 2026)

19 different users commented on 46 different issues.

## Recommended Actions

 * Moderation
    * @apostate0 posted rude content in [microsoft/TypeScript-go#4291](https://github.com/microsoft/TypeScript-go/pull/4291#issuecomment-4692383357)
 * Response Recommended
    * @typescript-automation[bot] reported build failures due to ReferenceError: __dirname is not defined in [microsoft/TypeScript-go#3435](https://github.com/microsoft/TypeScript-go/pull/3435#issuecomment-4684621266)
    * @hesam-oxe provided fix details in PR #4291 in [microsoft/TypeScript-go#3481](https://github.com/microsoft/TypeScript-go/issues/3481#issuecomment-4688740491)
    * @typescript-automation[bot] provided performance run results as requested in [microsoft/TypeScript-go#4242](https://github.com/microsoft/TypeScript-go/pull/4242#issuecomment-4692080264)
    * @klydra asked about log casing differences and switching to trace output and provided logs for review in [microsoft/TypeScript-go#4259](https://github.com/microsoft/TypeScript-go/issues/4259#issuecomment-4692381794)
    * @ibesuperv provided requested information in [microsoft/TypeScript-go#4274](https://github.com/microsoft/TypeScript-go/pull/4274#issuecomment-4686407223)

## Activity Summary

### [Issue microsoft/TypeScript-go#2533](https://github.com/microsoft/TypeScript-go/issues/2533) (Closed, `bug`, `Domain: Declaration Emit`, **weswigham**)

**Multiple differences in declaration emit for CommonJS exports**

*TypeScript’s declaration emitter for CommonJS exports uses typeof module.exports, emits duplicate var declarations, and emits var instead of const.*

 * [1 month ago](https://github.com/microsoft/TypeScript-go/issues/2533#issuecomment-4409207996) **weswigham** discussed the pros and cons of emitting duplicate declarations for multiple module export assignments and questioned whether to merge or error on them, concluding that emitting duplicates mirrors TS var redeclarations
 * [1 month ago](https://github.com/microsoft/TypeScript-go/issues/2533#issuecomment-4409859940) **RyanCavanaugh** said "@weswigham is what I'm hearing "wontfix"? I tend to agree if so. @ahejlsberg good w/ you too?"
 * [1 month ago](https://github.com/microsoft/TypeScript-go/issues/2533#issuecomment-4409931266) **weswigham** suggested to retag and track separate issues individually
 * [today](https://github.com/microsoft/TypeScript-go/issues/2533#issuecomment-4683899363) **ahejlsberg** explained that removing duplicate declarations would require symbolic binding and noted that the CommonJS emit produces identical duplicate var declarations which only add noise and overhead
 * [today](https://github.com/microsoft/TypeScript-go/issues/2533#issuecomment-4684951278) **weswigham** explained that differing type annotations can cause validation issues, described the current first-in-wins export behavior, and mentioned opening issue #4284 to implement simple dedupe logic
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript-go#3379](https://github.com/microsoft/TypeScript-go/pull/3379) (Open, **DanielRosenwasser**, **Copilot**)

**Fix declaration emit panics for CommonJS exports**

*Fix declaration emit panics by preserving diagnostic contexts for named and object-form CommonJS exports referencing inaccessible symbols.*

 * [1 month ago](https://github.com/microsoft/TypeScript-go/pull/3379#issuecomment-4425665109) **jakebailey** said "@copilot+claude-opus-4.7 If you undo your fixes, your test doesn't actually crash."
 * [1 month ago](https://github.com/microsoft/TypeScript-go/pull/3379#issuecomment-4425736135) **Copilot** confirmed that reverting the fixes caused the test to pass without crashing, tested various scenarios without reproducing the panic, removed the speculative pre-check, retained the structural fix, adjusted the test to a sanity check, and requested a reproduction case that crashes
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * [today](https://github.com/microsoft/TypeScript-go/pull/3379#issuecomment-4685512856) **jakebailey** said "@copilot+gpt-5.5 merge main and try again. try as hard as you can to find a crash. do not guess at a fix."
 * [today](https://github.com/microsoft/TypeScript-go/pull/3379#issuecomment-4685738016) **Copilot** merged main, verified the original repro no longer crashes, identified a related crash with export-assignment diagnostics, and applied a narrow fix preserving diagnostic context

### [PR microsoft/TypeScript-go#3435](https://github.com/microsoft/TypeScript-go/pull/3435) (Open)

**Make LS checkers time out after being idle, segment based on use \(take 2\)**

*Language server checkers will now automatically time out after periods of inactivity and are segmented based on usage.*

 * [1 month ago](https://github.com/microsoft/TypeScript-go/pull/3435#issuecomment-4423528862) **typescript-bot** reported CI tests for tsserver top200 as started and provided build and results links
 * [1 month ago](https://github.com/microsoft/TypeScript-go/pull/3435#issuecomment-4425033761) **typescript-bot** reported TS server comparison results showing that the new server no longer reported a panic error and asked to take a look
 * [1 month ago](https://github.com/microsoft/TypeScript-go/pull/3435#issuecomment-4425033906) **typescript-bot** reported a panic in textDocument/signatureHelp due to debug assertion "Not a subspan" with accompanying stack trace
 * [today](https://github.com/microsoft/TypeScript-go/pull/3435#issuecomment-4683703779) **jakebailey** said "This PR is interacting poorly with the ID fixing, for some reason. Looking into it"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3435#issuecomment-4684620402) **jakebailey** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3435#issuecomment-4684621266) **typescript-automation[bot]** reported build job failures for test top400 and perf test due to ReferenceError: __dirname is not defined
 * [today](https://github.com/microsoft/TypeScript-go/pull/3435#issuecomment-4684869533) **jakebailey** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3435#issuecomment-4684870297) **typescript-automation[bot]** reported starting of jobs and provided links to their statuses and results
 * [today](https://github.com/microsoft/TypeScript-go/pull/3435#issuecomment-4685087817) **typescript-automation[bot]** reported the requested performance run results
 * [today](https://github.com/microsoft/TypeScript-go/pull/3435#issuecomment-4685331613) **typescript-automation[bot]** reported that everything looked good when comparing `main` and `refs/pull/3435/merge` on the top 400 repos using tsc

### [Issue microsoft/TypeScript-go#3475](https://github.com/microsoft/TypeScript-go/issues/3475) (Open, `possible improvement`)

**Test harness doesn't report errors from unrecognized compiler options**

*The test harness fails to report errors for unrecognized compiler options, resulting in empty error outputs.*

 * created by **RyanCavanaugh**
 * **RyanCavanaugh** added to milestone `Post-7.0`
 * [today](https://github.com/microsoft/TypeScript-go/issues/3475#issuecomment-4685804721) **iisaduan** described that tsconfig parsing errors weren't reported by the testing harness and suggested future changes to report them
 * **iisaduan** added label `possible improvement`

### [Issue microsoft/TypeScript-go#3481](https://github.com/microsoft/TypeScript-go/issues/3481) (Open, `help wanted`)

**Corsa differences in \`export=\` module augmentation**

*Corsa changes how export= module augmentation works, causing differences in exported name visibility.*

 * (5 weeks ago) **RyanCavanaugh** added label `help wanted`, and set milestone to `Post-7.0`
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/3481#issuecomment-4642469732) **apostate0** described that augmentExportEquals2.errors.txt.diff wasn't a real bug but caused by duplicate filename directives and asked why they're used; identified a real semantic regression in exportAssignmentMembersVisibleInAugmentation.errors.txt.diff due to module augmentation symbol lookup and suggested a root cause in checker.go
 * [later](https://github.com/microsoft/TypeScript-go/issues/3481#issuecomment-4688695434) **hesam-oxe** offered to investigate the augmentation merge issue by examining checker.go:1409-1438 and tracing through getAccessibleSymbolChain and merge logic to fix binding propagation
 * [later](https://github.com/microsoft/TypeScript-go/issues/3481#issuecomment-4688740491) **hesam-oxe** opened PR #4291 that fixed mergeModuleAugmentation symbol propagation by copying main module exports, initializing target exports, including parent exports, and enabling recursive parent search

### [Issue microsoft/TypeScript-go#3617](https://github.com/microsoft/TypeScript-go/issues/3617) (Closed, `Voight-Kampff Anomaly`, **iisaduan**)

**fix: FindBestPatternMatch incorrectly allows wildcard pattern to override exact match**

*FindBestPatternMatch misuses StarIndex so exact matches set longestMatchPrefixLength to -1, allowing later wildcard patterns to override exact matches.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/3617#issuecomment-4615071752) **andrewbranch** said "I reduced @matyasf's repro to a compiler test and found that it's not fixed by #3618, so probably not related to this issue."
 * (yesterday) **iisaduan** added label `Voight-Kampff Anomaly`, and removed label `Needs Investigation`
 * (today) **RyanCavanaugh** set milestone to `Post-7.0`, and removed from milestone `TypeScript 7.0 RC`
 * [today](https://github.com/microsoft/TypeScript-go/issues/3617#issuecomment-4684272216) **RyanCavanaugh** said "Closing per https://github.com/microsoft/typescript-go/pull/3618#issuecomment-4684267050, I don't think this is "real" in any sense. Please log an issue with a user-visible repro if there is one."
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#3618](https://github.com/microsoft/TypeScript-go/pull/3618) (Closed, `Voight-Kampff Anomaly`)

**fix: prevent wildcard pattern from overriding exact match in FindBestPatternMatch**

*Assign math.MaxInt for exact matches in FindBestPatternMatch to ensure wildcard patterns cannot override exact matches.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3618#issuecomment-4598338818) **kuishou68** followed up on the PR, added requested test cases, and requested another review
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3618#issuecomment-4608256862) **kuishou68** added test cases and requested a re-review
 * **RyanCavanaugh** added label `Voight-Kampff Anomaly`
 * [today](https://github.com/microsoft/TypeScript-go/pull/3618#issuecomment-4684267050) **RyanCavanaugh** said "We've asked multiple times for what the user-visible manifestation of this is and gotten what appear to be machine-generated comments in response. Closing both."
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#3719](https://github.com/microsoft/TypeScript-go/issues/3719) (Closed, `bug`, **iisaduan**)

**Support localized user\-facing strings in VS Code extension**

*Add localization support by moving user-facing strings into package.nls.json and using vscode-l10n tools.*

 * (5 weeks ago) **RyanCavanaugh** added label `bug`, set milestone to `TypeScript 7.0 RC`, and assigned to **iisaduan**
 * (today) **iisaduan** closed the issue

### [PR microsoft/TypeScript-go#3771](https://github.com/microsoft/TypeScript-go/pull/3771) (Closed, **RyanCavanaugh**, **Copilot**)

**Accept CJS export alias and element access pattern baseline diffs**

*Accept five baseline diffs reflecting Corsa’s correct export alias and element access handling over Strada’s mangled outputs.*

 * (1 month ago) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * [today](https://github.com/microsoft/TypeScript-go/pull/3771#issuecomment-4685180549) **iisaduan** said "Closed by #3822"
 * (today) **iisaduan** closed the issue

### [PR microsoft/TypeScript-go#3834](https://github.com/microsoft/TypeScript-go/pull/3834) (Closed)

**add localization for extension**

*Add localization support to the TypeScript VS Code extension by integrating non-English translation files and enabling pseudo-language testing.*

 * created by **iisaduan**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3834#issuecomment-4675814391) **DanielRosenwasser** said "This is basically good to go, but I'm wondering if @jakebailey has thoughts on the generation."
 * [today](https://github.com/microsoft/TypeScript-go/pull/3834#issuecomment-4683550385) **iisaduan** said "Since we will (eventually) publish with vscode, we will join their language packs, which are localized by their localization team, and we can pull from there"
 * (today) **iisaduan** closed the issue

### [Issue microsoft/TypeScript-go#3908](https://github.com/microsoft/TypeScript-go/issues/3908) (Closed, **jakebailey**, **Copilot**)

**tsgo incorrectly renames arguments destructuring property when targeting ES2015**

*When targeting ES2015, tsgo wrongly renames destructured property 'arguments' to 'arguments_1' in async functions.*

 * (3 weeks ago) **jakebailey** assigned to **Copilot**, **jakebailey**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3910](https://github.com/microsoft/TypeScript-go/pull/3910) (Closed, **jakebailey**, **Copilot**)

**Fix incorrect renaming of \`arguments\` in non\-reference positions in async downlevel**

*Fix async downlevel transform by preserving non-reference `arguments` uses in destructuring and JSX using `IsIdentifierName` and `IsLabelName`.*

 * **Copilot** assigned to **jakebailey**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3910#issuecomment-4621288307) **jakebailey** said "@copilot merge main"
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4011](https://github.com/microsoft/TypeScript-go/issues/4011) (Closed, `bug`, **weswigham**)

**Property names from JSDoc types not escaped in declaration files**

*Declaration files generated by tsgo fail to quote hyphenated JSDoc property names, leading to syntax errors.*

 * (3 weeks ago) **RyanCavanaugh** assigned to **weswigham**, and unassigned **RyanCavanaugh**, **Copilot**
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript-go#4026](https://github.com/microsoft/TypeScript-go/pull/4026) (Open)

**Rebuilt CLI watcher around new \`fswatch\` package**

*The CLI watch command was rewritten to use OS-level fswatch events instead of polling, reducing idle CPU usage to under 1%.*

 * (3 days ago) **RyanCavanaugh** added label `No linked issue`, and set milestone to `Possible Improvement`
 * **johnfav03** removed label `No linked issue`
 * [today](https://github.com/microsoft/TypeScript-go/pull/4026#issuecomment-4685842782) **jakebailey** said "I didn't have time to look or test before I had to leave for the day but I intend to look in the morning "

### [PR microsoft/TypeScript-go#4058](https://github.com/microsoft/TypeScript-go/pull/4058) (Closed)

**Reparse non\-identifier jsdoc names where possible, error otherwise**

*The parser now reparses non-identifier JSDoc names when possible and errors on unsupported nameless typedef patterns.*

 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * [6 days ago](https://github.com/microsoft/TypeScript-go/pull/4058#issuecomment-4635078850) **DanielRosenwasser** asked whether backtick-wrapped property names still work with the PR
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/4058#issuecomment-4652004433) **weswigham** said "IIRC, it should - we parse both backticks and square brackets as jsdoc member name "quotes" (not changed here)."
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript-go#4195](https://github.com/microsoft/TypeScript-go/pull/4195) (Closed)

**Allow LSP server to use builtin watcher**

*Allow LSP servers to use the editor's built-in file watcher.*

 * created by **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#4206](https://github.com/microsoft/TypeScript-go/issues/4206) (Closed, `bug`, `Domain: Declaration Emit`, **weswigham**)

**Behavior difference: tsgo fails to infer type for undeclared class member when assignment happen inside \`new Promise\` callback**

*tsgo omits the undeclared class member `_resource` in declaration output when first assigned inside a Promise callback, unlike tsc.*

 * (6 days ago) **ahejlsberg** added labels `bug`, `Domain: Declaration Emit`, and set milestone to `TypeScript 7.0 RC`
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript-go#4238](https://github.com/microsoft/TypeScript-go/pull/4238) (Closed, `No linked issue`)

**Several performance optimizations for the scanner's hot path**

*Various per-commit optimizations to the scanner's hot path improve parsing performance by about 9.4% while keeping memory usage stable.*

 * [today](https://github.com/microsoft/TypeScript-go/pull/4238#issuecomment-4682011926) **typescript-automation[bot]** reported the requested performance run results
 * [today](https://github.com/microsoft/TypeScript-go/pull/4238#issuecomment-4682146434) **jakebailey** said "I like where this PR is now; much more contained. Are you planning on pushing anything else?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4238#issuecomment-4682201403) **mds-ant** mentioned having another scanner change to propose in a separate PR and indicated the current PR was ready for review
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4242](https://github.com/microsoft/TypeScript-go/pull/4242) (Open)

**Fix stack overflow crash in base constraint resolution**

*Add recursion limiting to base constraint resolution for conditional types to prevent stack overflow crashes.*

 * created by **ahejlsberg**
 * **RyanCavanaugh** added to milestone `Post-7.0`
 * [later](https://github.com/microsoft/TypeScript-go/pull/4242#issuecomment-4691899262) **ahejlsberg** said "@typescript-bot test it"
 * [later](https://github.com/microsoft/TypeScript-go/pull/4242#issuecomment-4691899984) **typescript-automation[bot]** reported start and completion statuses for 'test top400' and 'perf test this faster' jobs with result links
 * [later](https://github.com/microsoft/TypeScript-go/pull/4242#issuecomment-4692080264) **typescript-automation[bot]** provided the requested performance comparison results for tsc
 * [later](https://github.com/microsoft/TypeScript-go/pull/4242#issuecomment-4692363178) **typescript-automation[bot]** reported that everything looked good after running the top 400 repos with tsc comparing main and the pull request merge
 * (later) **RyanCavanaugh** set milestone to `TypeScript 7.0 RC`, and removed from milestone `Post-7.0`

### [Issue microsoft/TypeScript-go#4259](https://github.com/microsoft/TypeScript-go/issues/4259) (Closed, `Crash`)

**panic: cache entry not found \[recovered, repanicked\] \- exponentially increasingly random sporadic crashes until full VSCode Restart**

*Intermittent ‘cache entry not found’ panics in typescript-go cause exponentially increasing VSCode crashes until a full restart.*

 * **klydra** added label `Crash`
 * [today](https://github.com/microsoft/TypeScript-go/issues/4259#issuecomment-4678451986) **DanielRosenwasser** noted difficulty reproducing and asked if ESLint was the only extension performing actions on save and if TypeScript was formatting/organizing imports on save
 * [today](https://github.com/microsoft/TypeScript-go/issues/4259#issuecomment-4682036453) **klydra** described isolating ESLint as the only extension performing transformations on save and shared configuration settings and logs
 * [today](https://github.com/microsoft/TypeScript-go/issues/4259#issuecomment-4683197801) **DanielRosenwasser** asked if any log messages had differing casing or path separators and if they could switch the output pane to Trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/4259#issuecomment-4683203333) **DanielRosenwasser** said "(though I suppose that might have much more than you would prefer to share)"
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * (today) **RyanCavanaugh** closed the issue
 * [later](https://github.com/microsoft/TypeScript-go/issues/4259#issuecomment-4692381794) **klydra** asked additional diagnostic questions about log path casing and trace output, noted multiple crashes, and provided recent trace-verbosity log files

### [PR microsoft/TypeScript-go#4260](https://github.com/microsoft/TypeScript-go/pull/4260) (Closed)

**Fix stack overflow caused by simplification of recursive type**

*TypeScript now removes self-referential indexed access types from unions during simplification to prevent infinite recursion.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4260#issuecomment-4673053762) **jakebailey** said "@typescript-bot test top800"
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4260#issuecomment-4673054365) **typescript-automation[bot]** reported build status for the test top800 command, indicating it started and completed with links
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4260#issuecomment-4673703508) **typescript-automation[bot]** provided the results of running the top 800 repos with tsc comparing main and the PR merge and noted everything looked good
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * (later) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#4262](https://github.com/microsoft/TypeScript-go/issues/4262) (Open, `bug`, `Needs More Info`)

**Non\-deterministic \`TS2305 "has no exported member"\` errors across project references with \`\-\-emitDeclarationOnly\`**

*Flaky TS2305 "has no exported member" errors occur when running --emitDeclarationOnly across project references in a pnpm monorepo using tsgo.*

 * created by **benkeen**
 * (today) **RyanCavanaugh** added labels `bug`, `Needs More Info`
 * [today](https://github.com/microsoft/TypeScript-go/issues/4262#issuecomment-4685847391) **RyanCavanaugh** indicated it was a bug, requested a repro to diagnose, and suggested using AI with a link to instructions

### [PR microsoft/TypeScript-go#4263](https://github.com/microsoft/TypeScript-go/pull/4263) (Closed)

**TS GO API: add getCompletionsAtPosition to the API and support includeSymbols**

*Add getCompletionsAtPosition API with includeSymbols support by defining internal CompletionList and CompletionItem types.*

 * created by **piotrtomiak**
 * **RyanCavanaugh** added to milestone `Post-7.0`
 * [today](https://github.com/microsoft/TypeScript-go/pull/4263#issuecomment-4684807333) **piotrtomiak** said "@gabritto - thanks for quick review!"
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript-go#4264](https://github.com/microsoft/TypeScript-go/pull/4264) (Closed)

**Walk class children to find this property assignments beyond top level**

*Walk class members to detect nested this.property assignments during JavaScript declaration emission*

 * created by **weswigham**
 * (today) **weswigham** closed the issue

### [Issue microsoft/TypeScript-go#4272](https://github.com/microsoft/TypeScript-go/issues/4272) (Closed, **jakebailey**, **Copilot**)

**LSP: initialize rejected when initializationOptions is null**

*tsgo's LSP server rejects null initializationOptions values contrary to the LSP specification, preventing Emacs lsp-mode from initializing properly.*

 * created by **Macavirus**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4272#issuecomment-4683459003) **jakebailey** said "Yeah, you're right; we should be alowing null here."
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**
 * (later) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#4273](https://github.com/microsoft/TypeScript-go/pull/4273) (Closed)

**API: Add declaration property to IndexInfo\.**

*Add the missing declaration property to the IndexInfo object to enable WebStorm integration.*

 * created by **piotrtomiak**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#4274](https://github.com/microsoft/TypeScript-go/pull/4274) (Open)

**Fix CFA stack overflow crash in for loops where initializer throws**

*Add an early bailout in for-loop binding to avoid stack overflow when the initializer throws*

 * created by **ibesuperv**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4274#issuecomment-4679008732) **ibesuperv** agreed with microsoft-github-policy-service
 * [today](https://github.com/microsoft/TypeScript-go/pull/4274#issuecomment-4686407223) **ibesuperv** addressed both review comments by adding dummy break/continue targets and a new test case in the latest commit

### [Issue microsoft/TypeScript-go#4275](https://github.com/microsoft/TypeScript-go/issues/4275) (Closed, **jakebailey**, **Copilot**)

**\`tsconfig\.json\` included as JSON input reports TS1006 self\-reference**

*Importing and including tsconfig.json causes a TS1006 self-reference error in tsgo 7.0.0-dev.20260610.1 but not in TypeScript 6.0.3*

 * created by **rubenferreira97**
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4278](https://github.com/microsoft/TypeScript-go/pull/4278) (Closed)

**API: Fix nil panic for instantiated types**

*Nil pointer dereference crash when retrieving instantiated types in TS Go API proxy during tests*

 * created by **piotrtomiak**
 * (today) **piotrtomiak** closed the issue

### [PR microsoft/TypeScript-go#4279](https://github.com/microsoft/TypeScript-go/pull/4279) (Closed, **jakebailey**, **Copilot**)

**Fix false TS1006 for included tsconfig JSON imports**

*Restrict self-reference diagnostics to triple-slash references and prevent included tsconfig.json imports from incorrectly triggering TS1006 errors.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4280](https://github.com/microsoft/TypeScript-go/pull/4280) (Open, `possible improvement`)

**VS enhanced hover support**

*Restores Visual Studio enhanced hover support by attaching raw classification tokens and icon metadata to LSP hover responses when VSSupportsVisualStudioExtensions is enabled.*

 * created by **navya9singh**
 * **navya9singh** added label `possible improvement`

### [PR microsoft/TypeScript-go#4281](https://github.com/microsoft/TypeScript-go/pull/4281) (Closed, **jakebailey**, **Copilot**)

**LSP: accept null initializationOptions**

*Modify Go LSP generator and server to accept null initializationOptions and treat it as empty options*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4282](https://github.com/microsoft/TypeScript-go/pull/4282) (Closed)

**Release the speculatively acquired dirty file by its own key**

*Release the speculatively fetched dirty file by its original key to prevent ownership leaks and subsequent cache panics.*

 * created by **mds-ant**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4282#issuecomment-4684116010) **RyanCavanaugh** provided a fallback rebuild safety test generated by GPT-5.5
 * [today](https://github.com/microsoft/TypeScript-go/pull/4282#issuecomment-4684742648) **mds-ant** said "@RyanCavanaugh Please feel free to take over the PR and create a new one with this test (and any other changes you might want to make) included!"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4282#issuecomment-4685075797) **RyanCavanaugh** said "Picked up at #4285"
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#4283](https://github.com/microsoft/TypeScript-go/pull/4283) (Open)

**Optimize intersections / prop intersections further**

*Optimize intersection and property intersection computations further using insights from profiling data.*

 * created by **jakebailey**
 * **RyanCavanaugh** added to milestone `Post-7.0`

### [PR microsoft/TypeScript-go#4284](https://github.com/microsoft/TypeScript-go/pull/4284) (Closed)

**Dedupe cjs export assignments**

*Deduplicate CommonJS export assignments to avoid mismatched type declarations being emitted in TypeScript output.*

 * created by **weswigham**
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript-go#4285](https://github.com/microsoft/TypeScript-go/pull/4285) (Closed, **RyanCavanaugh**, **Copilot**)

**fix: release speculative parse\-cache acquire using the acquired file's own key**

*Reuses the original speculatively acquired source file pointer for cache release to prevent over-dereferencing and panics during rebuild fallback.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4285#issuecomment-4685073046) **RyanCavanaugh** said "This fix was via #4282 cc @mds-ant, plus a testcase generated locally"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4285#issuecomment-4685102885) **jakebailey** said "Tested locally and reverting the fix does reproduce the crash!"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#4286](https://github.com/microsoft/TypeScript-go/issues/4286) (Closed, **DanielRosenwasser**)

**completionItem/resolve crash for non\-identifier auto\-import**

*CompletionItem.resolve crashes when auto-importing a non-identifier export name containing a hyphen.*

 * created by **DanielRosenwasser**
 * **DanielRosenwasser** assigned to **DanielRosenwasser**
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#4287](https://github.com/microsoft/TypeScript-go/pull/4287) (Closed)

**Don't provide auto\-imports for non\-identifiers**

*Auto-import suggestions now exclude symbols with non-identifier names to avoid invalid code completions.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#4288](https://github.com/microsoft/TypeScript-go/pull/4288) (Open)

**Allow LSP server to use builtin watcher on Windows and macOS**

*Enable LSP server's built-in file system watcher on Windows and macOS while deferring other platforms.*

 * created by **andrewbranch**

### [Issue microsoft/TypeScript-go#4289](https://github.com/microsoft/TypeScript-go/issues/4289) (Open)

**diagnostics APIs position uses UTF\-8 encoding**

*IPC diagnostics APIs return positions in UTF-8, whereas AST and completion APIs use UTF-16 mapping, causing inconsistency.*

 * created by **jasonlyu123**

### [PR microsoft/TypeScript-go#4290](https://github.com/microsoft/TypeScript-go/pull/4290) (Open)

**fix: error on private property access in generic intersection types**

*Implement checking for conflicting private properties in Go’s generic intersection indexed access to correctly report errors.*

 * created by **hesam-oxe**

### [PR microsoft/TypeScript-go#4291](https://github.com/microsoft/TypeScript-go/pull/4291) (Open)

**fix: propagate module bindings to augmentation body for accessible symbol resolution**

*Propagate main module’s exported bindings into module augmentations to restore accessible symbol resolution chain.*

 * created by **hesam-oxe**
 * [later](https://github.com/microsoft/TypeScript-go/pull/4291#issuecomment-4690088520) **jakebailey** said "This needs tests if we are to accept it"
 * [later](https://github.com/microsoft/TypeScript-go/pull/4291#issuecomment-4691303716) **apostate0** thanked the contributor, reminded them to read the contribution guidelines, and noted that required tests were missing
 * [later](https://github.com/microsoft/TypeScript-go/pull/4291#issuecomment-4692383357) **apostate0** criticized the PR’s implementation as risky and misguided, highlighted missing changes, redundant code, formatting errors, and advised closing the PR and learning from it

### [Issue microsoft/TypeScript-go#4292](https://github.com/microsoft/TypeScript-go/issues/4292) (Open, `Domain: Editor`)

**Can't enable TypeScript native preview in VS Code**

*VS Code fails to activate the experimental TypeScript Native Preview and continues using the previous TypeScript version.*

 * created by **denexapp**
 * **denexapp** added label `Domain: Editor`

### [Issue microsoft/TypeScript-go#4293](https://github.com/microsoft/TypeScript-go/issues/4293) (Open)

**Behavior difference: Expando function emit between tsc & tsgo**

*Expando functions emit differently between TypeScript’s tsc and tsgo, with tsgo omitting certain post-bind attributes.*

 * created by **hkleungai**

