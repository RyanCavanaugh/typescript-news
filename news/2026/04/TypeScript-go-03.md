# Report for 2026-04-03 (Friday, April 3rd, 2026)

10 different users commented on 15 different issues.

## Recommended Actions

 * Response Recommended
    * @jan-wilhelm reported that the same error occurs on tsc 6.0.2 in [microsoft/TypeScript-go#2880](https://github.com/microsoft/TypeScript-go/issues/2880#issuecomment-4187210683)
    * @RealColdFry provided AST output demonstrating that non-null expressions work correctly in [microsoft/TypeScript-go#3240](https://github.com/microsoft/TypeScript-go/issues/3240#issuecomment-4185921666)

## Activity Summary

### [Issue microsoft/TypeScript-go#2626](https://github.com/microsoft/TypeScript-go/issues/2626) (Closed, `Domain: Editor`, `Needs More Info`)

**Extension softly crashes \(hangs indefinitely\) at sudden**

*The TypeScript extension v0.20260131.1 hangs and shows stale diagnostics when experimental useTsgo and project diagnostics are enabled, requiring restarts.*

 * **piscopancer** added label `Domain: Editor`
 * **RyanCavanaugh** added label `Needs More Info`
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/2626#issuecomment-4172369783) **RyanCavanaugh** said "This is very odd. We'd need some other clues to investigate. What's possibly unusual about your setup?"
 * [later](https://github.com/microsoft/TypeScript-go/issues/2626#issuecomment-4187060048) **piscopancer** said "I will close it for now as have not yet checked the newer versions where it might have been fixed"
 * (later) **piscopancer** closed the issue

### [Issue microsoft/TypeScript-go#2880](https://github.com/microsoft/TypeScript-go/issues/2880) (Open, `bug`, **weswigham**)

**TS4094 for exported class expressions with ES private fields \(tsc handles via name mangling\)**

*tsgo incorrectly errors on exported class expressions using ES private fields, unlike tsc which name-mangles them.*

 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2880#issuecomment-3947117028) **jakebailey** said "Maybe I'm wrong, but I feel like the original behavior was a bug. noEmit just controls whether or not we emit files. The editor is also a "noEmit" situation, but we show these errors there..."
 * (1 week ago) **RyanCavanaugh** added label `bug`, and assigned to **weswigham**
 * [later](https://github.com/microsoft/TypeScript-go/issues/2880#issuecomment-4187210683) **jan-wilhelm** said "This seems to not be tsgo specific. I'm seeing the same error message on tsc 6.0.2, whereas 5.9.3 was not showing it."
 * [later](https://github.com/microsoft/TypeScript-go/issues/2880#issuecomment-4187269594) **jakebailey** provided links to two TypeScript PRs

### [Issue microsoft/TypeScript-go#3173](https://github.com/microsoft/TypeScript-go/issues/3173) (Closed, `Domain: Editor`, **andrewbranch**, **Copilot**)

**When two imports have the same url, updates always apply to the first one\.**

*Auto-import merges additions into the first identical-module import statement instead of updating the appropriate type or value import.*

 * **xyhxx** added label `Domain: Editor`
 * **RyanCavanaugh** assigned to **andrewbranch**
 * **andrewbranch** assigned to **Copilot**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3173#issuecomment-4184775074) **andrewbranch** said "Fixed by #3244 "
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#3217](https://github.com/microsoft/TypeScript-go/pull/3217) (Open)

**Watch cli efficiency update**

*Watch CLI efficiency improvements implement debouncing, configuration caching, and dependency parsing to avoid unnecessary recompilations.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3217#issuecomment-4127784005) **andrewbranch** highlighted missing include wildcard handling and proposed decoupling watcher logic from build logic for LSP integration
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3217#issuecomment-4129133587) **johnfav03** described implementing the change by separating file tracking into a FileWatcher struct with a callback linked to doCycle while keeping caches, program construction, and emitting logic in the Watcher wrapper
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3217#issuecomment-4143654633) **andrewbranch** expressed that the commit wasn’t sufficient for wildcard watching, asked what “incremental skips emit for new unreferenced file” means, and suggested reading the directory recursively to detect new files
 * [today](https://github.com/microsoft/TypeScript-go/pull/3217#issuecomment-4185460956) **andrewbranch** used Copilot to generate tests and discovered multiple race conditions in vfswatch and watcher, linking a commit with detailed results

### [Issue microsoft/TypeScript-go#3240](https://github.com/microsoft/TypeScript-go/issues/3240) (Closed)

**Parser: postfix \`\!\` \(NonNullExpression\) parsed as prefix \`\!\` \(PrefixUnaryExpression\)**

*tsgo parser misparses the postfix non-null assertion operator '!' as a prefix logical-not, producing two statements instead of one.*

 * created by **RealColdFry**
 * (1 week ago) **RealColdFry** closed the issue
 * (today) **RealColdFry** reopened the issue
 * [today](https://github.com/microsoft/TypeScript-go/issues/3240#issuecomment-4185921666) **RealColdFry** demonstrated AST outputs for non-null expressions and property access expressions
 * (today) **RealColdFry** closed the issue

### [PR microsoft/TypeScript-go#3314](https://github.com/microsoft/TypeScript-go/pull/3314) (Closed)

**Fix declaration emit alias reuse for inferred exports**

*Align serializeTypeName’s resolveEntityName call with upstream to preserve imported type aliases in declaration emit and update baselines accordingly.*

 * created by **thromel**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3314#issuecomment-4184928308) **jakebailey** said "Not sure if you have properly cloned the submodule or not, as you are missing other baseline updates that should have happened."
 * [later](https://github.com/microsoft/TypeScript-go/pull/3314#issuecomment-4186676928) **thromel** initialized the TypeScript submodule, ran npm ci, accepted the missing baseline updates, and confirmed that the full test suite now passes

### [PR microsoft/TypeScript-go#3329](https://github.com/microsoft/TypeScript-go/pull/3329) (Closed, **andrewbranch**, **Copilot**)

**Add regression tests for auto\-import preferring matching type\-only declarations \(\#3244\)**

*Add regression tests ensuring auto-import correctly appends value and type imports to matching existing declarations.*

 * **Copilot** assigned to **andrewbranch**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3329#issuecomment-4180824824) **andrewbranch** said "@copilot looks right, but tests are unchanged, so you need to add one"
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3329#issuecomment-4180877695) **Copilot** added three fourslash tests and explained the key test demonstrating the divergence between isTypeOnlyLocation and IsValidTypeOnlyAliasUseSite in an incomplete type argument position
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#3330](https://github.com/microsoft/TypeScript-go/pull/3330) (Closed)

**Fix \-\-showConfig output: add compileOnSave and implied compiler options**

*Add compileOnSave and implied compiler options to the output of the --showConfig flag.*

 * created by **aamoghS**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3330#issuecomment-4179950383) **aamoghS** said "@microsoft-github-policy-service agree"
 * (today) **github-merge-queue[bot]** closed the issue

### [Issue microsoft/TypeScript-go#3336](https://github.com/microsoft/TypeScript-go/issues/3336) (Closed)

**7\.0\.0\-dev\.20260403\.1 lsp diagnostic params fail to unmarshall in Helix**

*Update to LSP client version 7.0.0-dev.20260403.1 breaks Helix diagnostics by failing to unmarshal null previousResultId.*

 * created by **kanashimia**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3336#issuecomment-4184082245) **jakebailey** clarified that null was not allowed for previousResultId according to the spec change in #3313
 * [today](https://github.com/microsoft/TypeScript-go/issues/3336#issuecomment-4184109709) **kanashimia** said "Ok, thanks @jakebailey for a pointer, I will open an issue there."
 * (today) **kanashimia** closed the issue

### [PR microsoft/TypeScript-go#3337](https://github.com/microsoft/TypeScript-go/pull/3337) (Closed)

**Update submodule**

*Update the submodule to include a new test for a fix and correct a diagnostic typo.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3338](https://github.com/microsoft/TypeScript-go/issues/3338) (Open, **mjbvz**)

**TSGO: command 'typescript\.restartTsServer' not found**

*Enabling the TypeScript native preview feature in VSCode 1.113.0 removes the 'typescript.restartTsServer' command.*

 * created by **eblocha**
 * **vs-code-engineering[bot]** assigned to **mjbvz**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3338#issuecomment-4184835689) **jakebailey** pointed out that the provided command didn't restart the new language server and suggested hiding it when tsserver wasn't used

### [PR microsoft/TypeScript-go#3339](https://github.com/microsoft/TypeScript-go/pull/3339) (Closed, **RyanCavanaugh**, **Copilot**)

**Set COPILOT\_AGENT\_TIMEOUT\_MIN to 180 in Copilot setup workflow**

*Increase the Copilot setup workflow timeout to 180 minutes to accommodate longer-running agent tasks.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3339#issuecomment-4185198215) **RyanCavanaugh** said "Creating for bookmarking purposes. Do not merge."
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#3340](https://github.com/microsoft/TypeScript-go/issues/3340) (Open)

**\[ServerErrors\]\[TypeScript\] main vs **

*The TypeScript error-delta pipeline on main failed with server errors and varied outcomes while analyzing 300 repositories.*

 * created by **typescript-bot**

