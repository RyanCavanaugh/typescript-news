# Report for 2025-12-02 (Tuesday, December 2nd, 2025)

24 different users commented on 51 different issues.

## Recommended Actions

 * Response Recommended
    * @mthines offered to share the file privately for further investigation in [microsoft/TypeScript-go#1326](https://github.com/microsoft/TypeScript-go/pull/1326#issuecomment-3606508213)
    * @urielzen provided repro steps as requested in [microsoft/TypeScript-go#1616](https://github.com/microsoft/TypeScript-go/issues/1616#issuecomment-3604294129)
    * @mkantor asked whether microsoft/TypeScript#60431 still happens with this implementation in [microsoft/TypeScript-go#1770](https://github.com/microsoft/TypeScript-go/pull/1770#issuecomment-3606626496)
    * @IOLOII reported a crash when opening JS/TS files in a Vue project and will provide repro steps later in [microsoft/TypeScript-go#1905](https://github.com/microsoft/TypeScript-go/issues/1905#issuecomment-3604718075)
    * @thien-do reported TS native-preview.tsdk isn't loaded and offered a workaround in [microsoft/TypeScript-go#1946](https://github.com/microsoft/TypeScript-go/issues/1946#issuecomment-3605882941)
    * @adrian-gierakowski asked if this is kept up to date with master in [microsoft/TypeScript-go#1966](https://github.com/microsoft/TypeScript-go/pull/1966#issuecomment-3604090437)
    * @rubnogueira reported a panic error with 'Token cache mismatch: parent' and provided the stack trace in [microsoft/TypeScript-go#2077](https://github.com/microsoft/TypeScript-go/issues/2077#issuecomment-3603910306)
    * @cbovis reported experiencing the same issue in a pnpm monorepo in [microsoft/TypeScript-go#2175](https://github.com/microsoft/TypeScript-go/issues/2175#issuecomment-3606234082)
    * @Sczlog provided additional screenshots as requested in [microsoft/TypeScript-go#2183](https://github.com/microsoft/TypeScript-go/issues/2183#issuecomment-3604772691)
    * @Sczlog provided a minimal reproduction repository in [microsoft/TypeScript-go#2183](https://github.com/microsoft/TypeScript-go/issues/2183#issuecomment-3604889321)
    * @Sczlog provided reproduction steps and identified module type difference as cause in [microsoft/TypeScript-go#2183](https://github.com/microsoft/TypeScript-go/issues/2183#issuecomment-3604941917)
    * @DreierF noted that the issue is a duplicate of microsoft/typescript-go#1034 in [microsoft/TypeScript-go#2185](https://github.com/microsoft/TypeScript-go/issues/2185#issuecomment-3605313108)

## Activity Summary

### [PR microsoft/TypeScript-go#1326](https://github.com/microsoft/TypeScript-go/pull/1326) (Closed)

**Folding Ranges implementation**

*Implements folding range support in the language server and consolidates hint span tests into folding tests.*

 * created by **navya9singh**
 * [18 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1326#issuecomment-3119969098) **DanielRosenwasser** suggested merging from the foldingRangesUpdates branch to sync with main, noted that previous feedback still applied, tested a code snippet with a leading newline locally, and reported a panic crash including a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/pull/1326#issuecomment-3603397892) **navya9singh** mentioned that merging from the foldingRangesUpdates branch would sync with main, noted that existing feedback still applied, reproduced a crash with a sample code snippet and provided the panic stack trace
 * [today](https://github.com/microsoft/TypeScript-go/pull/1326#issuecomment-3603429988) **jakebailey** reported that opening checker.ts caused a crash with an internal panic due to a token cache mismatch
 * [today](https://github.com/microsoft/TypeScript-go/pull/1326#issuecomment-3603592258) **jakebailey** said "Since I pushed, I can't review anymore. Can someone else look?"
 * (today) **jakebailey** closed the issue
 * [later](https://github.com/microsoft/TypeScript-go/pull/1326#issuecomment-3606508213) **mthines** reported that on version 7.0.0-dev.20251203.1 they still encountered the 'Request textDocument/foldingRange failed.' error in VSCode and offered to share the file privately
 * [later](https://github.com/microsoft/TypeScript-go/pull/1326#issuecomment-3607240318) **jakebailey** said "Please file an issue with at least the panic stack trace."

### [Issue microsoft/TypeScript-go#1549](https://github.com/microsoft/TypeScript-go/issues/1549) (Closed, `Crash`, `Domain: Program`, **sheetalkamat**)

**Crash in incremental due to inconsistent casing**

*Incremental compilation crashes when inconsistent file path casing causes duplicate key errors in the ManyToManySet*

 * **RyanCavanaugh** assigned to **gabritto**
 * (6 days ago) **sheetalkamat** assigned to **sheetalkamat**, and unassigned **gabritto**
 * (today) **sheetalkamat** closed the issue

### [PR microsoft/TypeScript-go#1551](https://github.com/microsoft/TypeScript-go/pull/1551) (Open)

**Avoid copying content when writing files**

*Update WriteFile to accept byte slices directly and avoid mutating or copying input data.*

 * created by **dzbarsky**
 * [16 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1551#issuecomment-3172320838) **jakebailey** noted that refactoring file writing to use []byte would be a lot of changes and asked to see benchmarks for the PR
 * [today](https://github.com/microsoft/TypeScript-go/pull/1551#issuecomment-3605003415) **jakebailey** said "@dzbarsky Did you have benchmarks for this, by chance? Not against the change, but I want any use of unsafe to be well-justified."

### [PR microsoft/TypeScript-go#1575](https://github.com/microsoft/TypeScript-go/pull/1575) (Closed)

**perf\(tspath\): avoid string copy in ToFileNameLowerCase**

*Optimize ToFileNameLowerCase by replacing byte slice to string conversion with unsafe.String, boosting performance by 10% and halving allocations.*

 * [15 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1575#issuecomment-3191438757) **camc314** reported that a huge amount of time was spent in Go's GC
 * [15 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1575#issuecomment-3194539248) **Gobd** asked whether the new green tea GC in Go 1.25 helps with GC performance
 * [15 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1575#issuecomment-3194541428) **camc314** mentioned that the greenteagc flag is still experimental and might not be suitable for production and noted that GC overhead remains high so optimizations are still worthwhile
 * [today](https://github.com/microsoft/TypeScript-go/pull/1575#issuecomment-3605011875) **jakebailey** said "Old PR, but if you merge main I think we could probably take it..."

### [Issue microsoft/TypeScript-go#1616](https://github.com/microsoft/TypeScript-go/issues/1616) (Open, `Domain: Type Checking`, `Type Ordering`, **ahejlsberg**)

**The last overload gave the following error\. Type 'unknown' is not assignable to type 'Foo'**

*After updating the TypeScript native-preview extension, DialogConfig calls fail with unknown not assignable to the expected modal confirmation generic type.*

 * **RyanCavanaugh** added label `Needs More Info`
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/1616#issuecomment-3598605809) **RyanCavanaugh** said "We need minimal isolated repro."
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/1616#issuecomment-3598619168) **urielzen** offered to put something together and report back
 * [today](https://github.com/microsoft/TypeScript-go/issues/1616#issuecomment-3604294129) **urielzen** provided a reproduction link with comments and invited questions
 * [today](https://github.com/microsoft/TypeScript-go/issues/1616#issuecomment-3604391251) **RyanCavanaugh** explained TS7's type ordering differences causing AbstractType to be selected before Type$1 and recommended using overloads for inject
 * (today) **RyanCavanaugh** added label `Type Ordering`, removed label `Needs More Info`, and assigned to **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript-go/issues/1616#issuecomment-3604417437) **RyanCavanaugh** provided a minimal example that excluded potential red herrings

### [Issue microsoft/TypeScript-go#1619](https://github.com/microsoft/TypeScript-go/issues/1619) (Closed, `Crash`, `Domain: Program`, **sheetalkamat**)

**Panic in incremental with tsbuildinfo with mismatched \`fileNames\` and \`fileInfos\`**

*Incremental compilation panics with an index out of range error when tsbuildinfo fileNames and fileInfos arrays misalign.*

 * (14 weeks ago) **jakebailey** added label `Domain: Program`, and assigned to **sheetalkamat**
 * [14 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1619#issuecomment-3212977010) **sheetalkamat** identified the issue as a duplicate of issue #1549 and suggested a fix to prevent duplicate files in the program's array
 * (today) **sheetalkamat** closed the issue

### [PR microsoft/TypeScript-go#1770](https://github.com/microsoft/TypeScript-go/pull/1770) (Open)

**Organize imports for TypeScript and JavaScript**

*Expose TypeScript and JavaScript import organizer via LSP command in VS Code, preserving blank lines and sorting imports*

 * [7 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1770#issuecomment-3384996041) **saixiaoxi** questioned how to implement a non-destructive sortImports command within the LSP spec
 * [7 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1770#issuecomment-3385605813) **jakebailey** acknowledged the suggestion and expressed uncertainty about registering the same command as the main TS extension
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1770#issuecomment-3493026664) **jakebailey** advised merging with main to check for duplicate helpers and suggested reusing the existing command name or using the when clause
 * [later](https://github.com/microsoft/TypeScript-go/pull/1770#issuecomment-3606626496) **mkantor** asked whether microsoft/TypeScript#60431 still occurred with this implementation

### [Issue microsoft/TypeScript-go#1866](https://github.com/microsoft/TypeScript-go/issues/1866) (Closed, `Domain: CLI`, **Copilot**)

**Passing \-\-customConditions null it not respected**

*tsgo ignores the --customConditions null flag and continues using tsconfig.json values, unlike tsc which correctly nullifies it*

 * [7 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1866#issuecomment-3390602923) **jakebailey** said "I'm not sure if the CLI parser supports nulling out flags yet. Seemingly not."
 * (7 weeks ago) **jakebailey** added label `Domain: CLI`, and assigned to **Copilot**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#1868](https://github.com/microsoft/TypeScript-go/pull/1868) (Closed, **jakebailey**, **Copilot**)

**Fix \-\-customConditions null not being respected when overriding tsconfig\.json**

*Fix tsgo to respect --customConditions null when merging tsconfig.json by adding raw option parsing support*

 * [7 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1868#issuecomment-3391138929) **Copilot** clarified that the implementation already supported null for unsetting any CompilerOptions and verified it with --lib, --types, and --outDir
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/1868#issuecomment-3599487375) **jakebailey** said "@copilot you did not run the formatter as instructed"
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/1868#issuecomment-3599507154) **Copilot** fixed indentation by running the formatter in commit 81d4e0
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#1905](https://github.com/microsoft/TypeScript-go/issues/1905) (Open, `Crash`, **sheetalkamat**)

**panic: vfs: path is not absolute**

*The VFS implementation panics when given a URL-based path because it expects an absolute filesystem path.*

 * created by **LukeAbby**
 * **LukeAbby** added label `Crash`
 * **RyanCavanaugh** assigned to **sheetalkamat**
 * [today](https://github.com/microsoft/TypeScript-go/issues/1905#issuecomment-3604712273) **IOLOII** shared a configuration map
 * [today](https://github.com/microsoft/TypeScript-go/issues/1905#issuecomment-3604718075) **IOLOII** reported a crash when opening JavaScript or TypeScript files in a Vue project using the plugin and offered to provide repro steps later

### [Issue microsoft/TypeScript-go#1946](https://github.com/microsoft/TypeScript-go/issues/1946) (Open, `Domain: Editor`)

**Support workspace specific typescript version**

*Allow the extension to use a workspace-specific TypeScript version rather than a global one.*

 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1946#issuecomment-3445092209) **ahejlsberg** said "Please be more specific about the issue here."
 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1946#issuecomment-3445096707) **jakebailey** said "I think they are asking for workspace-specific tsdk, which is supported with typescript.native-preview.tsdk, but just doesn't have the VS Code UI bits in place."
 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1946#issuecomment-3449257178) **deathemperor** clarified that they meant the workspace-specific tsdk and thanked @jakebailey
 * [later](https://github.com/microsoft/TypeScript-go/issues/1946#issuecomment-3605882941) **thien-do** reported that typescript.native-preview.tsdk wasn't being picked up with the nightly compiler and offered a dangerous workaround
 * [later](https://github.com/microsoft/TypeScript-go/issues/1946#issuecomment-3605893813) **thien-do** corrected that it should be the directory rather than the file

### [PR microsoft/TypeScript-go#1949](https://github.com/microsoft/TypeScript-go/pull/1949) (Open, **jakebailey**, **Copilot**)

**Fix signature help applicable span for nested calls**

*Improves signature help applicable span for nested function calls to correctly handle empty argument lists and prioritize outer calls.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/1949#issuecomment-3599472557) **Copilot** reverted the changes in commit bed1740 and explained conflicting requirements between TestSignatureHelpWithTriggers02 and the nested calls fix, noting a pre-existing issue and the need for a nuanced approach
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/1949#issuecomment-3599484546) **jakebailey** clarified that the test transforms foo(bar|) into foo(bar(|) and expects bar's signature help, stating that there is no conflict and attributing the confusion to a misunderstanding
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/1949#issuecomment-3599507732) **Copilot** acknowledged a misunderstanding, clarified that signature help should appear inside inner call parentheses, noted that TestSignatureHelpWithTriggers02 was failing, and said they would investigate and fix the span calculation for empty argument lists
 * [today](https://github.com/microsoft/TypeScript-go/pull/1949#issuecomment-3604873836) **jakebailey** encouraged copilot to continue and suggested using print debugging with go test -v
 * [today](https://github.com/microsoft/TypeScript-go/pull/1949#issuecomment-3604913495) **Copilot** fixed the empty argument list span, extended it to include a position, made all signature help tests pass, and planned to add tests for nested calls from issue #1419

### [PR microsoft/TypeScript-go#1966](https://github.com/microsoft/TypeScript-go/pull/1966) (Open)

**Add Yarn PnP support**

*Implement native Yarn Plug'n'Play support in TypeScript Go with PnP VFS, API, and manifest handling.*

 * created by **GGomez99**
 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1966#issuecomment-3456508357) **GGomez99** said "@microsoft-github-policy-service agree company="Datadog""
 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1966#issuecomment-3457072757) **GGomez99** said "I see my tests are not passing in CI, looking into it 🙇 "
 * [today](https://github.com/microsoft/TypeScript-go/pull/1966#issuecomment-3604090437) **adrian-gierakowski** said "is this kept up to date with master? I would like to try it out on a monorepo at work. Thanks!"

### [PR microsoft/TypeScript-go#2043](https://github.com/microsoft/TypeScript-go/pull/2043) (Open, **jakebailey**, **Copilot**)

**Fix nil pointer panic in FormatOnEnter**

*Prevent nil pointer panics in FormatOnEnter by adding nil checks when deriving indentation from AST node lists.*

 * created by **Copilot**
 * (3 weeks ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2043#issuecomment-3602933187) **jakebailey** said "@copilot the panic in https://github.com/microsoft/typescript-go/issues/2042 is clearly not in this function"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2043#issuecomment-3603021388) **Copilot** acknowledged the panic was in getStartLineAndCharacterForNode and added nil checks in that function and its callers

### [Issue microsoft/TypeScript-go#2077](https://github.com/microsoft/TypeScript-go/issues/2077) (Open, `Crash`)

**Inlayhint panic**

*The inlay hint provider panics when handling textDocument/inlayHint requests due to an out-of-range line number.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/2077#issuecomment-3556550111) **lukpsaxo** reported a third panic related to inlay hints, distinct from the original and issue #2131
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/2077#issuecomment-3558670505) **jakebailey** said "The logs would be super helpful. You can send them to jabaile at microsoft.com."
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/2077#issuecomment-3567847077) **lukpsaxo** said "I sent full logs+lsp for a panic on friday and then full logs+lsp for the line mismatch panic today. Subject line contains "Logs for tsgo issue 2077""
 * [today](https://github.com/microsoft/TypeScript-go/issues/2077#issuecomment-3603910306) **rubnogueira** reported a panic with 'Token cache mismatch: parent' error and included a stack trace

### [Issue microsoft/TypeScript-go#2083](https://github.com/microsoft/TypeScript-go/issues/2083) (Closed, `bug`)

**Missing error trying to invoke \`\-\-incremental\` without a tsconfig\.json**

*tsgo silently ignores the --incremental option when compiling a standalone file without a tsconfig.json, unlike tsc which errors TS5074.*

 * created by **RyanCavanaugh**
 * **RyanCavanaugh** added label `bug`
 * (today) **sheetalkamat** closed the issue

### [PR microsoft/TypeScript-go#2104](https://github.com/microsoft/TypeScript-go/pull/2104) (Closed, **jakebailey**, **Copilot**)

**Add missing TS6504 diagnostic for JavaScript files without allowJs**

*Add diagnostic TS6504 for JavaScript files when allowJs is disabled in all inclusion scenarios.*

 * (2 weeks ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2104#issuecomment-3599606585) **jakebailey** reported a data race in includeProcessor concurrent use and provided the stack trace
 * [today](https://github.com/microsoft/TypeScript-go/pull/2104#issuecomment-3604865836) **jakebailey** said "@copilot See above. Make includeProcessor safe for concurrent use."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2104#issuecomment-3604920586) **Copilot** fixed includeProcessor for concurrent use by adding mutex protection to shared fields, added helper methods for safe access, and verified tests passed with the race detector

### [PR microsoft/TypeScript-go#2149](https://github.com/microsoft/TypeScript-go/pull/2149) (Closed, **andrewbranch**, **Copilot**)

**Port codeactions import fixes to new autoimport stack**

*Migrate code action import fixes from the old SymbolExportInfo system to the new autoimport infrastructure.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/2149#issuecomment-3573318157) **Copilot** recovered and pushed changes, fixed panics, added type-only import support, updated tests, and noted remaining tests needing namespace qualification fixes, default export search, and JSDoc import type syntax
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/2149#issuecomment-3573346207) **andrewbranch** said "@copilot can you focus on the JSDoc import type fixes next please"
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/2149#issuecomment-3573390936) **Copilot** implemented support for JSDoc import type fixes including UsagePosition field, pure type export syntax, and type-only import specifiers, and updated tests
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#2150](https://github.com/microsoft/TypeScript-go/pull/2150) (Closed)

**Handle missing error when \`\-\-incremental\` is used incorrectly**

*Ensure TS5074 error is reported when --incremental is used without required conditions*

 * created by **Twacqwq**
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/2150#issuecomment-3566828026) **Twacqwq** agreed to the Contributor License Agreement by replying with '@microsoft-github-policy-service agree'.
 * (today) **sheetalkamat** closed the issue

### [Issue microsoft/TypeScript-go#2154](https://github.com/microsoft/TypeScript-go/issues/2154) (Closed, `Domain: Editor`)

**"Go to definition" is missing within html template strings \(lit\)**

*VS Code ctrl-click go to definition does not work for lit-html template string component tags when using tsgo*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/2154#issuecomment-3568356100) **jakebailey** said "Do you have a tsserver plugin enabled, or an extension that loaded one? Those will not work with tsgo."
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/2154#issuecomment-3592868843) **eamodio** said "Ah, yes this comes from https://marketplace.visualstudio.com/items?itemName=jackolope.lit-analyzer-plugin and it uses a typescript plugin."
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/2154#issuecomment-3593002146) **jakebailey** said "Yes, so this is expected. Existing plugins for tsserver won't work in the new codebase."
 * (today) **eamodio** closed the issue

### [PR microsoft/TypeScript-go#2155](https://github.com/microsoft/TypeScript-go/pull/2155) (Closed)

**Don't disable TS extension in debug launch task**

*Stop force-disabling the TS extension in debug launch tasks and instead warn when tsgo is disabled.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2159](https://github.com/microsoft/TypeScript-go/pull/2159) (Closed)

**Handle file casing when creating program**

*Implement file casing handling and forceConsistentCasingInFileNames checks to avoid duplicate files on case-insensitive file systems.*

 * created by **sheetalkamat**
 * (today) **sheetalkamat** closed the issue

### [Issue microsoft/TypeScript-go#2161](https://github.com/microsoft/TypeScript-go/issues/2161) (Closed)

**Inferred function return type is different from TS 5\.9\.3**

*TypeScript 5.9 correctly narrows getItem’s return type, but tsgo erroneously infers it as never causing property access errors.*

 * created by **In3luki**
 * [later](https://github.com/microsoft/TypeScript-go/issues/2161#issuecomment-3607308419) **Andarist** highlighted inconsistency in return type inference introduced by PR #244 and recommended merging an older PR (#58910) to align behaviors

### [PR microsoft/TypeScript-go#2172](https://github.com/microsoft/TypeScript-go/pull/2172) (Closed)

**Never create more checkers than files in a program**

*Limit the number of checkers in a program to the number of files to prevent wasted resources.*

 * created by **jakebailey**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2172#issuecomment-3599291579) **jakebailey** said "This will conflict with #2159 so I'll wait for that as it's more critical."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2174](https://github.com/microsoft/TypeScript-go/pull/2174) (Closed)

**Server\-to\-client refresh requests for user preference updates**

*Adds server-to-client refresh for inlay hints and code lenses, nested UserPreferences hierarchy, verbose go generate, and fixes inlay hint parsing typos.*

 * created by **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2174#issuecomment-3604438944) **DanielRosenwasser** reported that for VS Code, a refresh request didn't trigger a new inlay hints request
 * (today) **DanielRosenwasser** closed the issue

### [Issue microsoft/TypeScript-go#2175](https://github.com/microsoft/TypeScript-go/issues/2175) (Closed, `Domain: Editor`)

**tsgo doesn't suggest \(autoimport\) of packages in monorepo and tries to use relative path in vscode**

*tsgo’s autoimport in a monorepo bypasses configured package paths and suggests incorrect deep relative imports instead of package names.*

 * created by **darklight9811**
 * [later](https://github.com/microsoft/TypeScript-go/issues/2175#issuecomment-3606234082) **cbovis** said "Same issue here in a pnpm monorepo."

### [Issue microsoft/TypeScript-go#2176](https://github.com/microsoft/TypeScript-go/issues/2176) (Closed, `Domain: Editor`)

**Code folding doesn't work**

*Code folding no longer works in TypeScript files in VS Code Insider using extension version 0.20251202.1*

 * created by **eamodio**
 * **eamodio** added label `Domain: Editor`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2176#issuecomment-3603011918) **jakebailey** said "This is not yet implemented, no. https://github.com/microsoft/typescript-go/pull/1326"
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2177](https://github.com/microsoft/TypeScript-go/issues/2177) (Closed, `Domain: Editor`, **Copilot**)

**Differences/issues with Code Lens references**

*CodeLens shows 70 references in TS mode but only 31 in TSGO mode for the same GitLens file, indicating inconsistent reference counts.*

 * created by **eamodio**
 * **eamodio** added label `Domain: Editor`

### [Issue microsoft/TypeScript-go#2178](https://github.com/microsoft/TypeScript-go/issues/2178) (Closed, **Copilot**)

**tsgo missing TS2540 error with default export**

*tsgo ignores TS2540 read-only assignment error for default-exported Readonly objects.*

 * created by **jfirebaugh**
 * **jakebailey** assigned to **Copilot**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2179](https://github.com/microsoft/TypeScript-go/pull/2179) (Closed, **jakebailey**, **Copilot**)

**Fix TS2540 not reported for readonly properties accessed through imports**

*Imported readonly properties were not reported as TS2540 errors due to a flawed check order, now fixed by reordering checks.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2179#issuecomment-3603632181) **jakebailey** said "@copilot I don't think you ran test/lint/format, as the new test should end up with baselines at the very least"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2179#issuecomment-3603673989) **Copilot** stated that they ran tests, lint, and format, added a `@module: commonjs` directive, and committed baselines in 6ebb498
 * [today](https://github.com/microsoft/TypeScript-go/pull/2179#issuecomment-3603854436) **jakebailey** said "@copilot you need to run hereby test and accept the baselines, then commit that"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2179#issuecomment-3603888880) **Copilot** ran tests and accepted all baselines then committed changes in 34878cc
 * [today](https://github.com/microsoft/TypeScript-go/pull/2179#issuecomment-3603912419) **jakebailey** said "Yikes. We now think you can't do module.exports =  because that is technically readonly?"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2180](https://github.com/microsoft/TypeScript-go/pull/2180) (Closed)

**Remove duplicate findChildOfKind**

*The codebase contains duplicate findChildOfKind functions that should be removed.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2181](https://github.com/microsoft/TypeScript-go/pull/2181) (Closed)

**Temporarily work around golangci\-lint custom git bug**

*Add a temporary workaround for golangci-lint's custom git bug caused by GitHub Actions' regressed git version.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2182](https://github.com/microsoft/TypeScript-go/issues/2182) (Open, `Domain: Editor`)

**Completion does not work for generic type extending tuple or array of all partial type**

*VS Code’s TypeScript completion fails to suggest optional properties in generic functions using tuple parameters combined with mapped Record types.*

 * created by **ishowta**
 * **ishowta** added label `Domain: Editor`

### [Issue microsoft/TypeScript-go#2183](https://github.com/microsoft/TypeScript-go/issues/2183) (Closed, `Needs More Info`)

**cannot resolve type definition with type:module**

*VS Code’s tsgo language service cannot locate Eta’s type declarations in a type:module package despite tsc compiling successfully.*

 * created by **Sczlog**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2183#issuecomment-3604772691) **Sczlog** provided additional screenshots showing missing type definitions in the VSCode bug reporter, presence of type definitions in the package, and successful tsc compilation
 * [today](https://github.com/microsoft/TypeScript-go/issues/2183#issuecomment-3604817683) **DanielRosenwasser** requested tsconfig.json and a minimal repro and noted that tsc was used instead of tsgo
 * **DanielRosenwasser** added label `Needs More Info`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2183#issuecomment-3604843427) **Sczlog** clarified that they used tsgo as a language service while building with tsc and provided a screenshot showing successful compilation
 * [today](https://github.com/microsoft/TypeScript-go/issues/2183#issuecomment-3604889321) **Sczlog** apologized for providing incorrect information, explained that the repo was organized with Yarn Classic and Lerna, reported that removing business code stopped the error, and linked to a minimal reproduction repository
 * [today](https://github.com/microsoft/TypeScript-go/issues/2183#issuecomment-3604941917) **Sczlog** identified the issue as an older eta version, reproduced the problem by freezing to 1.12.3, and noted that switching to the legacy TS language service resolved it, highlighting the module type difference between versions
 * [today](https://github.com/microsoft/TypeScript-go/issues/2183#issuecomment-3605024858) **jakebailey** pointed out that version 1.12.3 was a broken package due to node10-only resolution and suggested testing the TS nightly instead of 5.9
 * [today](https://github.com/microsoft/TypeScript-go/issues/2183#issuecomment-3605025790) **jakebailey** said "I would say that this is (unfortunately), working as expected, just based on the ATTW link above."
 * [today](https://github.com/microsoft/TypeScript-go/issues/2183#issuecomment-3605234764) **Sczlog** provided comparison screenshots between tsc@5.9.3 and nightly tsc@6.0.0-dev
 * (today) **Sczlog** closed the issue

### [PR microsoft/TypeScript-go#2184](https://github.com/microsoft/TypeScript-go/pull/2184) (Closed)

**Make fourslash a real async client**

*Refactor the fourslash runner into an asynchronous LSP client using goroutines and eliminate related initialization hacks.*

 * created by **jakebailey**
 * (later) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2185](https://github.com/microsoft/TypeScript-go/issues/2185) (Closed)

**tsgo on SvelteKit project reporting more issues than tsc**

*tsgo reports inferred type naming errors in SvelteKit-generated files when using Prisma and pnpm, while tsc shows no issues.*

 * created by **KieranP**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2185#issuecomment-3605313108) **DreierF** said "That's likely a duplicate of https://github.com/microsoft/typescript-go/issues/1034"
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2186](https://github.com/microsoft/TypeScript-go/issues/2186) (Open)

**Broken assignability and quick info due to erroneously deferring keyof T since \#51621**

*Erroneously deferring keyof T since PR 51621 causes unsimplified quick info and invalid type assignments.*

 * created by **LukeAbby**

### [Issue microsoft/TypeScript-go#2187](https://github.com/microsoft/TypeScript-go/issues/2187) (Open, `Domain: Editor`)

**Broken property suggestions due to a successfully contextually typed function**

*When using a contextually typed callback in makeRequest, TypeScript infers QueryParam as unknown and provides incorrect property suggestions.*

 * created by **LukeAbby**

### [Issue microsoft/TypeScript-go#2188](https://github.com/microsoft/TypeScript-go/issues/2188) (Open, `Domain: Editor`)

**Mixins Overrides Drop Documentation**

*TypeScript fails to inherit JSDoc comments when a mixin-derived class overrides a static method.*

 * created by **LukeAbby**

### [Issue microsoft/TypeScript-go#2189](https://github.com/microsoft/TypeScript-go/issues/2189) (Open, `Domain: Editor`, **andrewbranch**)

**LSP doesn't offer auto\-importing packages**

*VS Code’s TypeScript LSP does not offer auto-import suggestions for installed packages like `typescript-result`, only built-in modules*

 * created by **jansedlon**
 * **jansedlon** added label `Domain: Editor`

### [Issue microsoft/TypeScript-go#2190](https://github.com/microsoft/TypeScript-go/issues/2190) (Closed)

**Different Behavior of Overriding Global Interface**

*Adding an optional 'cache' property to the global ImportAttributes interface errors in tsgo but not TypeScript 5.9.*

 * created by **sxzz**

### [PR microsoft/TypeScript-go#2191](https://github.com/microsoft/TypeScript-go/pull/2191) (Closed)

**fix: Enable getExePath to work on Node 16**

*Enable getExePath compatibility on Node 16 to restore tsgo preview functionality*

 * created by **aapoalas**
 * [later](https://github.com/microsoft/TypeScript-go/pull/2191#issuecomment-3606482159) **aapoalas** said "@microsoft-github-policy-service agree company="Valmet Automation""
 * [later](https://github.com/microsoft/TypeScript-go/pull/2191#issuecomment-3607527921) **jakebailey** said "I guess we could do this, but you should also update package.json's engines."

### [PR microsoft/TypeScript-go#2192](https://github.com/microsoft/TypeScript-go/pull/2192) (Closed)

**Don't ask for checker immediately in ProvideCodeActions**

*Remove the unused checker invocation in ProvideCodeActions leftover from a previous iteration.*

 * created by **jakebailey**

