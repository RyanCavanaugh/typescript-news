# Report for 2026-03-09 (Monday, March 9th, 2026)

12 different users commented on 32 different issues.

## Activity Summary

### [PR microsoft/TypeScript-go#2688](https://github.com/microsoft/TypeScript-go/pull/2688) (Closed, **RyanCavanaugh**, **Copilot**)

**Port TypeScript PR \#63054: Default \`types\` to \`\[\]\`, support \`"\*"\` wildcard**

*Default the types compiler option to an empty array and support a "*" wildcard for automatic type package discovery*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2688#issuecomment-3930958354) **Copilot** added the missing getCannotResolveModuleNameErrorForSpecificModule function, included beforeEach in test runner cases and NodeJS in node cases, and fixed in commit 6a48e64
 * [today](https://github.com/microsoft/TypeScript-go/pull/2688#issuecomment-4021328498) **DanielRosenwasser** said "@copilot merge from main, update the submodule, accept baselines"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2688#issuecomment-4021401123) **Copilot** merged from main, verified submodule contains PR #63054, and accepted baselines in commit df0db5c
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#2775](https://github.com/microsoft/TypeScript-go/pull/2775) (Closed, **jakebailey**, **Copilot**)

**Reject \`import assert\` in parser and checker, remove checker assert/with distinction**

*Reject and deprecate `import assert` syntax by enforcing parse errors, unifying import attribute handling, and adding dynamic import checks.*

 * created by **Copilot**
 * (3 weeks ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2855](https://github.com/microsoft/TypeScript-go/pull/2855) (Closed)

**Share package\.json cache and skip collecting failed lookup locations in auto\-imports**

*Caching package.json and skipping failed lookup locations in auto-imports reduces memory allocation overhead.*

 * created by **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2855#issuecomment-4026367165) **andrewbranch** said "This was included in #2991"
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#2882](https://github.com/microsoft/TypeScript-go/issues/2882) (Closed, `Crash`)

**Probable nil entry from specifier cache in auto\-import completions**

*Auto-import completions may fail or crash due to a nil entry in the specifier cache with no known repro steps.*

 * created by **DanielRosenwasser**
 * **DanielRosenwasser** added label `Crash`
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript-go#2905](https://github.com/microsoft/TypeScript-go/pull/2905) (Closed)

**Fixed a crash on completions with auto\-imports racing with \`DidClose\` notification**

*Prevent completion crashes when auto-import retries race with DidClose by retaining requested file entries and reusing consistent snapshots.*

 * created by **Andarist**
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/2905#issuecomment-3962591123) **andrewbranch** described passing their branch with snapshot adoption checks to gabritto, noted its uncertain status, and suggested retaining that functionality
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript-go#2944](https://github.com/microsoft/TypeScript-go/pull/2944) (Open)

**\[draft\] more formatting tests **

*Add draft formatting tests to validate and troubleshoot the repository’s testing pipelines.*

 * [4 days ago](https://github.com/microsoft/TypeScript-go/pull/2944#issuecomment-4001174323) **typescript-bot** said "Hey @iisaduan, this PR is in an unmergable state, so is missing a merge commit to run against; please resolve conflicts and try again."
 * [4 days ago](https://github.com/microsoft/TypeScript-go/pull/2944#issuecomment-4001359290) **iisaduan** said "@typescript-bot test top100"
 * [4 days ago](https://github.com/microsoft/TypeScript-go/pull/2944#issuecomment-4001359480) **typescript-bot** reported that the top100 tests failed to queue due to validation errors or warnings
 * [today](https://github.com/microsoft/TypeScript-go/pull/2944#issuecomment-4027129395) **iisaduan** said "@typescript-bot test top100"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2944#issuecomment-4027129682) **typescript-bot** reported that the test top100 job failed to queue due to validation errors or warnings

### [PR microsoft/TypeScript-go#2963](https://github.com/microsoft/TypeScript-go/pull/2963) (Closed, **andrewbranch**, **Copilot**)

**Port FindNextToken and FindPrecedingToken from Go to TypeScript**

*Port findNextToken and findPrecedingToken from Go to the TypeScript AST package and validate behavior against Go baselines.*

 * [4 days ago](https://github.com/microsoft/TypeScript-go/pull/2963#issuecomment-3998613280) **andrewbranch** proposed adding baseline generation to Go tests for FindNextToken and FindPrecedingToken and replacing manual TS tests with ones checking their behavior against Go baselines
 * [4 days ago](https://github.com/microsoft/TypeScript-go/pull/2963#issuecomment-3999209824) **andrewbranch** said "@copilot you were interrupted by an error but pushed your work in progress. Please continue."
 * [4 days ago](https://github.com/microsoft/TypeScript-go/pull/2963#issuecomment-3999352126) **Copilot** reported passing baseline-based tests and described two bug fixes in findPrecedingTokenImpl and findRightmostValidToken
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#2978](https://github.com/microsoft/TypeScript-go/pull/2978) (Open, **andrewbranch**, **Copilot**)

**Fix auto\-import type modifier and formatting issues in type\-only import statements**

*Fix inline type modifiers, formatting, indentation, token handling, and import ordering in type-only import statements.*

 * [4 days ago](https://github.com/microsoft/TypeScript-go/pull/2978#issuecomment-4001356213) **Copilot** described changes in commit 31661e1: aligned InsertNodeInListAfter and InsertImportSpecifierAtIndex implementations with TS, removed workaround indentation prefix, and confirmed all tests passed
 * [4 days ago](https://github.com/microsoft/TypeScript-go/pull/2978#issuecomment-4001375518) **andrewbranch** said "@copilot+claude-opus-4.6 you added a bunch to crashingTests.txt. Either it's out of date, or you need to fix the crashes."
 * [4 days ago](https://github.com/microsoft/TypeScript-go/pull/2978#issuecomment-4001504251) **Copilot** fixed crashes in FindNextToken by using tokenFullStart to match TS behavior, causing all 12 previously crashing tests to work (11 removed from both crashing and failing lists and one retaining a wrong-answer failure)
 * [today](https://github.com/microsoft/TypeScript-go/pull/2978#issuecomment-4025687202) **andrewbranch** said "@copilot+claude-opus-4.6 fix merge conflict and address feedback"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2978#issuecomment-4025888666) **Copilot** fixed merge conflict and addressed feedback by deduplicating functions, adding TS comments, and updating failingTests.txt
 * [today](https://github.com/microsoft/TypeScript-go/pull/2978#issuecomment-4025894963) **andrewbranch** said "@copilot+claude-opus-4.6 you messed up the merge, there's still a conflict and this PR now shows a massive diff from the merge commit 😠 "
 * [today](https://github.com/microsoft/TypeScript-go/pull/2978#issuecomment-4025998453) **Copilot** fixed the merge by reverting the bad single-parent commit and re-merging origin/main with a proper two-parent merge, resulting in the PR diff showing only the intended 18 changed files

### [Issue microsoft/TypeScript-go#2985](https://github.com/microsoft/TypeScript-go/issues/2985) (Closed, `Crash`)

**panic: "project bucket missing" in completions**

*Code completions panic with 'project bucket missing' error due to unprepared autoimport registry.*

 * created by **DanielRosenwasser**
 * **DanielRosenwasser** added label `Crash`
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript-go#2986](https://github.com/microsoft/TypeScript-go/pull/2986) (Closed, **andrewbranch**, **Copilot**)

**Add \`symbol\.getExportSymbol\(\)\` and export \`Type\` from API**

*Add asynchronous and synchronous getExportSymbol() methods to the Symbol API and re-export Type in API modules.*

 * created by **Copilot**
 * (4 days ago) **Copilot** assigned to **Copilot**, **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#3016](https://github.com/microsoft/TypeScript-go/pull/3016) (Closed)

**fix: move GetLanguageService to async closure to prevent dispatch loop blocking**

*Relocate GetLanguageService invocation into an asynchronous closure to prevent dispatch loop blocking.*

 * created by **SibtainOcn**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3016#issuecomment-4016380598) **jakebailey** said "Does this not just undo #2765?"
 * (today) **SibtainOcn** closed the issue
 * (today) **SibtainOcn** reopened the issue
 * (today) **SibtainOcn** closed the issue

### [Issue microsoft/TypeScript-go#3018](https://github.com/microsoft/TypeScript-go/issues/3018) (Closed, `bug`, `Domain: Editor`, **ahejlsberg**)

**No quick info for properties accessed via index signature**

*TypeScript 7.0 fails to show quick info on indexed Record<string,string> properties, expected string|undefined.*

 * created by **DanielRosenwasser**
 * **ahejlsberg** assigned to **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3018#issuecomment-4025489330) **ahejlsberg** said "I will be putting up a PR this fixes this as I describe here."
 * (today) **ahejlsberg** added labels `bug`, `Domain: Editor`

### [PR microsoft/TypeScript-go#3022](https://github.com/microsoft/TypeScript-go/pull/3022) (Closed)

**Provide type\-based quick info on symbol\-less nodes**

*Enable quick info tooltips showing inferred type information for code nodes without associated symbols.*

 * created by **Andarist**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3022#issuecomment-4025483658) **ahejlsberg** explained that the current fix approach was incorrect and that existing infrastructure for synthetic symbols wasn’t working properly, and said he would submit a PR to fix it

### [PR microsoft/TypeScript-go#3028](https://github.com/microsoft/TypeScript-go/pull/3028) (Closed)

**fix: pass Config to EmitInput in watch mode to prevent nil panic**

*Ensure Config is passed to EmitInput in watch mode to prevent nil pointer panics.*

 * created by **SibtainOcn**
 * (today) **SibtainOcn** closed the issue

### [PR microsoft/TypeScript-go#3029](https://github.com/microsoft/TypeScript-go/pull/3029) (Closed)

**Add missing \`declarations\` property for \`VariableDeclarationList\` in IPC API**

*Include the missing declarations property in the IPC API definition for VariableDeclarationList to ensure complete interface support.*

 * created by **auvred**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#3030](https://github.com/microsoft/TypeScript-go/pull/3030) (Closed)

**docs: correct setting key for Tsgo in README**

*Correct the Tsgo setting key in the README documentation.*

 * created by **9romise**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3030#issuecomment-4022323674) **9romise** said "@microsoft-github-policy-service agree"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3031](https://github.com/microsoft/TypeScript-go/pull/3031) (Closed, `dependencies`, `github_actions`)

**Bump the github\-actions group across 1 directory with 2 updates**

*Upgrade GitHub Actions in the root directory by bumping actions/setup-node to v6.3.0 and updating github/codeql-action.*

 * (today) **dependabot[bot]** added labels `github_actions`, `dependencies`, `github_actions`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3032](https://github.com/microsoft/TypeScript-go/issues/3032) (Closed, `Domain: Editor`, `Needs More Info`)

**tsgo \-\-lsp memory leak on large projects / triggers OOM**

*The tsgo LSP process in the TypeScript Native Preview extension leaks memory when handling large projects, causing OOM on low-RAM Linux machines.*

 * created by **huseeiin**
 * **huseeiin** added label `Domain: Editor`
 * [today](https://github.com/microsoft/TypeScript-go/issues/3032#issuecomment-4027150933) **andrewbranch** asked for a heap profile
 * [today](https://github.com/microsoft/TypeScript-go/issues/3032#issuecomment-4027155579) **andrewbranch** said "Also, please let us know exactly how much memory the native preview is using after loading vs. the exact same set of open files with native preview disabled."
 * **andrewbranch** added label `Needs More Info`

### [PR microsoft/TypeScript-go#3033](https://github.com/microsoft/TypeScript-go/pull/3033) (Closed)

**Fixed a formatting crash caused by misinterpretation of tokens in reparsed node lists**

*A formatting crash caused by misinterpreting tokens in reparsed node lists has been fixed.*

 * created by **Andarist**

### [PR microsoft/TypeScript-go#3034](https://github.com/microsoft/TypeScript-go/pull/3034) (Closed)

**Move module keyword check back to checker**

*Revert the module keyword check back into the checker after it caused breakages.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3035](https://github.com/microsoft/TypeScript-go/pull/3035) (Closed)

**docs\(native\-preview\): add VS Code extension info and settings snippet**

*Update native-preview documentation with VS Code extension details, settings snippet, and usage examples for improved onboarding.*

 * created by **karimFin**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3035#issuecomment-4027221247) **karimFin** said "@microsoft-github-policy-service agree"
 * (today) **karimFin** closed the issue

### [PR microsoft/TypeScript-go#3036](https://github.com/microsoft/TypeScript-go/pull/3036) (Closed)

**docs\(vscode\): add optional tsgo setting hint in settings template; link CHANGES\.md**

*Add an optional tsgo setting hint to the VSCode settings template and make CHANGES.md clickable in the README.*

 * created by **karimFin**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3036#issuecomment-4027221427) **karimFin** said "@microsoft-github-policy-service agree"
 * (today) **karimFin** closed the issue

### [PR microsoft/TypeScript-go#3037](https://github.com/microsoft/TypeScript-go/pull/3037) (Closed)

**Move extension status entirely into language status bar, drop warning color**

*Integrate extension status into the language status bar without warning color, but struggle with default pinning and visibility.*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#3038](https://github.com/microsoft/TypeScript-go/pull/3038) (Closed)

**Delete failed lookup locations**

*Remove unused per-import failed lookup location tracking to reduce memory consumption in the compiler host.*

 * created by **andrewbranch**

### [PR microsoft/TypeScript-go#3039](https://github.com/microsoft/TypeScript-go/pull/3039) (Closed)

**\[@typescript/api\] Codegen node visitor**

*Implement code generation support for the TypeScript API node visitor to automate visitor scaffolding.*

 * created by **andrewbranch**

### [Issue microsoft/TypeScript-go#3040](https://github.com/microsoft/TypeScript-go/issues/3040) (Open, `Domain: Declaration Emit`, **weswigham**)

**\`TS7056\` for exported generic arrow function with return type \(arrow\-only\)**

*Exporting a generic arrow function with a complex return type triggers TS7056 serialization errors under tsgo but not in TypeScript 6.0 or for function declarations.*

 * created by **rubenferreira97**

### [Issue microsoft/TypeScript-go#3041](https://github.com/microsoft/TypeScript-go/issues/3041) (Closed)

**Global augmentations from @types packages in typeRoots not picked up by tsgo**

*tsgo fails to include global namespace augmentations from typeRoots-based @types packages, unlike tsc.*

 * created by **taneli-linear**
 * [later](https://github.com/microsoft/TypeScript-go/issues/3041#issuecomment-4031410305) **taneli-linear** closed the issue explaining it was an intentional TS6 breaking change requiring explicit `types` entries and not a bug
 * (later) **taneli-linear** closed the issue

### [Issue microsoft/TypeScript-go#3042](https://github.com/microsoft/TypeScript-go/issues/3042) (Closed)

**tsgo doesn't resolve @types for scoped package subpath imports \(@types/scope\_\_pkg convention\)**

*tsgo fails to map scoped subpath imports under @mapbox/mapbox-sdk to corresponding @types/mapbox__mapbox-sdk declarations*

 * created by **taneli-linear**
 * [later](https://github.com/microsoft/TypeScript-go/issues/3042#issuecomment-4031410559) **taneli-linear** closed the issue explaining it was an intentional TS6 breaking change requiring explicit `types` entries and not a bug
 * (later) **taneli-linear** closed the issue

### [Issue microsoft/TypeScript-go#3043](https://github.com/microsoft/TypeScript-go/issues/3043) (Closed, **jakebailey**, **Copilot**)

**Template literal type inference slices multi\-byte characters by byte instead of UTF\-16 code unit**

*Template literal type inference slices multi-byte characters by byte boundaries rather than UTF-16 code units, causing incorrect type inference.*

 * created by **314systems**

### [Issue microsoft/TypeScript-go#3044](https://github.com/microsoft/TypeScript-go/issues/3044) (Open, `bug`, **RyanCavanaugh**, **Copilot**)

**Regex parsing/validation isn't implemented yet**

*tsgo does not report syntax errors in invalid regular expressions that TypeScript 6.0 catches due to missing regex parsing validation*

 * created by **RyanCavanaugh**
 * (later) **RyanCavanaugh** added label `bug`, and assigned to **Copilot**, **RyanCavanaugh**

### [PR microsoft/TypeScript-go#3045](https://github.com/microsoft/TypeScript-go/pull/3045) (Closed, **RyanCavanaugh**, **Copilot**)

**Port scanRegularExpressionWorker to enable regex body validation**

*Port TypeScript's scanRegularExpressionWorker into the Go scanner to enable comprehensive regex literal structural validation and flag error reporting.*

 * created by **Copilot**
 * (later) **Copilot** assigned to **Copilot**, **RyanCavanaugh**

