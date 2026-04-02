# Report for 2026-02-03 (Tuesday, February 3rd, 2026)

17 different users commented on 40 different issues.

## Recommended Actions

 * Response Recommended
    * @pattobrien reported that the issue still occurred in 7.0.0-dev after the PR merge in [microsoft/TypeScript-go#2648](https://github.com/microsoft/TypeScript-go/issues/2648#issuecomment-3842197513)
    * @Icantjuddle asked for an update on this in [microsoft/TypeScript-go#929](https://github.com/microsoft/TypeScript-go/issues/929#issuecomment-3843884423)
    * @sinclairzx81 asked for testing confirmation that the hotfix resolves the issue in [microsoft/TypeScript-go#929](https://github.com/microsoft/TypeScript-go/issues/929#issuecomment-3845678994)

## Activity Summary

### [Issue microsoft/TypeScript-go#1914](https://github.com/microsoft/TypeScript-go/issues/1914) (Closed, `Domain: Editor`, **Copilot**)

**Change in formatting for anonymous generators**

*tsgo removes the space between the asterisk and parentheses in anonymous generator functions, causing inconsistent formatting with stable TypeScript*

 * [14 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1914#issuecomment-3433395999) **mjbvz** noted that changing defaults would be difficult and asked if the formatting settings defaulted to false
 * [14 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1914#issuecomment-3433406243) **jakebailey** demonstrated that the Strada default format code settings align with the Go implementation by providing TypeScript and Go code snippets
 * [14 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1914#issuecomment-3433992650) **jakebailey** noted that it was blocked on issue #1729 and suggested adopting VS Code's defaults temporarily
 * [today](https://github.com/microsoft/TypeScript-go/issues/1914#issuecomment-3842792259) **jakebailey** said "#1729 was merged, so I believe this is done."
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2576](https://github.com/microsoft/TypeScript-go/issues/2576) (Open, **andrewbranch**)

**Autocompletions and quick fix suggestions try to import from "@types" packages**

*tsgo quick fixes and autocompletions wrongly import from @types packages instead of real modules*

 * created by **kyle-sawatsky**
 * **andrewbranch** assigned to **andrewbranch**

### [Issue microsoft/TypeScript-go#2581](https://github.com/microsoft/TypeScript-go/issues/2581) (Closed, `Domain: Editor`, **DanielRosenwasser**, **andrewbranch**, **Copilot**)

**Autocomplete incorrectly suggests transitive files from monorepo package**

*VS Code’s TypeScript autocomplete inaccurately includes internal files from a transitive monorepo package during auto-import suggestions.*

 * (1 week ago) **DanielRosenwasser** assigned to **Copilot**, **DanielRosenwasser**, **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#2582](https://github.com/microsoft/TypeScript-go/issues/2582) (Open, `Domain: Editor`, **andrewbranch**)

**Auto\-import does not suggest updates from symlinked monorepo package sources**

*VS Code’s auto-import feature does not suggest updated symbols from symlinked packages in a monorepo workspace*

 * created by **ericnorris**
 * **ericnorris** added label `Domain: Editor`
 * **andrewbranch** assigned to **andrewbranch**

### [PR microsoft/TypeScript-go#2584](https://github.com/microsoft/TypeScript-go/pull/2584) (Closed, **DanielRosenwasser**, **Copilot**)

**Fix autocomplete suggesting unexported internal files from monorepo packages**

*Improve package name resolution to prevent autocomplete from suggesting unexported internal files in monorepo packages.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/2584#issuecomment-3801288843) **andrewbranch** described expected behavior of module.GetResolvedEntrypoints and GetModuleSpecifier, expressed confusion about package.json version relevance, and requested a thorough investigation of the root cause
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/2584#issuecomment-3801309418) **andrewbranch** said "@copilot try again"
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/2584#issuecomment-3806965130) **andrewbranch** said "@copilot it's a new day, see if your infrastructure will let you do anything now"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2584#issuecomment-3842742837) **RyanCavanaugh** said "@copilot+claude-opus-4.5 try again"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2584#issuecomment-3842941375) **Copilot** described the root cause of empty package names leading to incorrect auto-import behavior and the applied fix
 * [today](https://github.com/microsoft/TypeScript-go/pull/2584#issuecomment-3843005778) **andrewbranch** asked whether a versionless package.json was intended to produce an empty PackageId and suggested running the full test suite after changing it
 * [today](https://github.com/microsoft/TypeScript-go/pull/2584#issuecomment-3843076448) **Copilot** acknowledged the issue and changed getPackageId to include the package name even without a version, updated baselines, and confirmed tests passed
 * [today](https://github.com/microsoft/TypeScript-go/pull/2584#issuecomment-3843201548) **andrewbranch** questioned why withPackageId checks both name and version and asked about the consequences of the fix
 * [today](https://github.com/microsoft/TypeScript-go/pull/2584#issuecomment-3843311457) **sheetalkamat** explained that package ID was used for deduplicating files by package name and version and noted that Strada doesn’t support duplicate package detection but Corsa might
 * [today](https://github.com/microsoft/TypeScript-go/pull/2584#issuecomment-3843495637) **andrewbranch** instructed @copilot to update package name resolution to prioritize PackageID, p.resolver.GetPackageScopeForPath, then directory-based name, avoid empty strings, and run tests, accept baselines, lint, and format for merge readiness
 * [today](https://github.com/microsoft/TypeScript-go/pull/2584#issuecomment-3843564658) **Copilot** implemented the requested package name priority order in commit 9a8dd4eb and confirmed tests passed with clean baselines, lint, and format
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#2620](https://github.com/microsoft/TypeScript-go/pull/2620) (Closed)

**Bring back async API, allow API connection to LSP process**

*Reintroduce a decoupled async JSON-RPC API client and server in the LSP to enable external extensions to query TypeScript state.*

 * created by **andrewbranch**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2620#issuecomment-3836765880) **jakebailey** suggested using gensync for clever codegen to alleviate async function coloring annoyance in TypeScript client code
 * [today](https://github.com/microsoft/TypeScript-go/pull/2620#issuecomment-3843063540) **andrewbranch** explained why the API requires clients to release objects and demonstrated using statements for automatic cleanup
 * [today](https://github.com/microsoft/TypeScript-go/pull/2620#issuecomment-3843140487) **gabritto** explained that the API requires explicit cleanup of symbols and types across remote calls, provided a using-syntax example, and asked what happens to returned objects when the project changes
 * [today](https://github.com/microsoft/TypeScript-go/pull/2620#issuecomment-3843551857) **andrewbranch** explained that the client controlled when to adopt the latest LSP session snapshot, allowing it to retain older objects indefinitely and reuse source files and symbols, and postponed implementing automatic purging for simplicity

### [Issue microsoft/TypeScript-go#2630](https://github.com/microsoft/TypeScript-go/issues/2630) (Closed, `Domain: Editor`, **andrewbranch**)

**Multiple Language Client instances persist after TSDK switch**

*Switching to the TypeScript native-preview SDK in VS Code leaves duplicate language client instances, showing the previous fix was incomplete.*

 * created by **rubenferreira97**
 * **rubenferreira97** added label `Domain: Editor`
 * **andrewbranch** assigned to **andrewbranch**

### [PR microsoft/TypeScript-go#2645](https://github.com/microsoft/TypeScript-go/pull/2645) (Closed)

**Add first\-class unused baseline tracking**

*Add unused baseline tracking to hereby test by incorporating TestMain to record baselines, flag unknown files, and emit .delete files.*

 * created by **jakebailey**
 * (yesterday) **jakebailey** closed the issue
 * (yesterday) **jakebailey** reopened the issue
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2646](https://github.com/microsoft/TypeScript-go/pull/2646) (Closed, **jakebailey**, **Copilot**)

**Fix import elision with type\-only usage**

*Fix import elision logic in tsgo to prevent emitting require statements for imports used exclusively in type positions*

 * created by **Copilot**
 * (yesterday) **Copilot** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2646#issuecomment-3842846854) **jakebailey** told copilot that the fix was partial and instructed it to think harder, compare with checker.ts, and use print debugging and go test -v to fully fix it
 * [today](https://github.com/microsoft/TypeScript-go/pull/2646#issuecomment-3842964797) **Copilot** fixed the import clause elision bug by visiting the import clause first and eliding entire import declarations when the clause became nil
 * [today](https://github.com/microsoft/TypeScript-go/pull/2646#issuecomment-3845052292) **jakebailey** investigated and determined that splitting the old TS transform into a type eraser and an import elider caused the issue and suggested removing the import elider
 * [today](https://github.com/microsoft/TypeScript-go/pull/2646#issuecomment-3845194672) **jakebailey** said "Sent https://github.com/microsoft/typescript-go/pull/2673 instead"
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2648](https://github.com/microsoft/TypeScript-go/issues/2648) (Open, `Crash`)

**panic handling request textDocument/codeAction: textDocument/codeAction returned ErrNeedsAutoImports even after enabling auto imports**

*TypeScript LSP panics on codeAction requests returning ErrNeedsAutoImports despite auto imports being enabled*

 * **pattobrien** added label `Crash`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2648#issuecomment-3840929021) **tomredman** reported that the error persisted since version 0.20260129.1, provided environment details, and included a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/2648#issuecomment-3841032189) **tomredman** removed autoImport excludes to resolve the error and suggested the issue was a duplicate of microsoft/typescript-go#2598
 * [today](https://github.com/microsoft/TypeScript-go/issues/2648#issuecomment-3842197513) **pattobrien** confirmed that removing autoImport excludes fixed the error and noted that the issue persisted after the PR merge
 * [today](https://github.com/microsoft/TypeScript-go/issues/2648#issuecomment-3842484579) **andrewbranch** said "@iisaduan looks like #2616 wasn't sufficient ☹️ "

### [Issue microsoft/TypeScript-go#2649](https://github.com/microsoft/TypeScript-go/issues/2649) (Open, `Crash`, **DanielRosenwasser**, **Copilot**)

**LSP Panic: strings: negative Repeat count when formatting JSDoc within nested scope**

*The TypeScript LSP server panics with a negative repeat count error when formatting nested JSDoc comments.*

 * [today](https://github.com/microsoft/TypeScript-go/issues/2649#issuecomment-3840618713) **DanielRosenwasser** said they couldn't reproduce the issue in Neovim and suggested guarding against negative tab size values
 * **DanielRosenwasser** added label `Needs More Info`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2649#issuecomment-3840802482) **ButbkaDrug** reported that tsgo consistently crashes when code starts on the first line, provided a code snippet and a workaround, and noted inconsistent trimming of first letters
 * **DanielRosenwasser** removed label `Needs More Info`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2649#issuecomment-3843883710) **DanielRosenwasser** said "Okay, now that it's properly formatted it repros."
 * (today) **DanielRosenwasser** assigned to **Copilot**, **DanielRosenwasser**

### [Issue microsoft/TypeScript-go#2651](https://github.com/microsoft/TypeScript-go/issues/2651) (Closed, `Domain: Editor`, **jakebailey**, **Copilot**)

**Different behaviour of \`editor\.action\.smartSelect\` vs built\-in TS**

*smartSelect.expand includes surrounding quotes when selecting bracketed strings with the TS native preview extension but not with the built-in TypeScript.*

 * created by **aantia**
 * **aantia** added label `Domain: Editor`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2651#issuecomment-3842802461) **jakebailey** clarified that issue #1914 was unrelated and explained that issue #1939 powered smart select, noting that his PR wasn't a pure port and might need fixing
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2651#issuecomment-3845450009) **starball5** said "(related on Stack Overflow: How to change the VSCode SmartSelect interaction with quotation marks)"

### [Issue microsoft/TypeScript-go#2652](https://github.com/microsoft/TypeScript-go/issues/2652) (Closed, **jakebailey**, **Copilot**)

**\`resolveJsonModule\` is not defaulted to \`true\` when \`module\` is \`nodenext\`**

*When using module: nodenext, resolveJsonModule isn’t enabled by default, causing JSON imports to fail in tsgo.*

 * created by **abrahamguo**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2652#issuecomment-3841251001) **abrahamguo** said "This feature was introduced into TS in typescript#61805, and ported to tsgo in #1797, but it looks like this specific feature was missed."
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**, **Copilot**, and unassigned **Copilot**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2652#issuecomment-3842679762) **jakebailey** described a simple porting bug where ESNext was used instead of NodeNext in a switch statement
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2653](https://github.com/microsoft/TypeScript-go/issues/2653) (Closed, `bug`, **ahejlsberg**)

**Static properties on manual \(pre\-ES6\) classes can't be declared and then defined**

*tsgo incorrectly reports duplicate identifier errors when declaring and defining static properties on pre-ES6 classes.*

 * created by **peetklecha**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2653#issuecomment-3842789026) **ahejlsberg** explained that the expando declaration is classified as a property, causing a conflict with the method declaration, and suggested changing the static declaration to property style to resolve it
 * [today](https://github.com/microsoft/TypeScript-go/issues/2653#issuecomment-3842795168) **ahejlsberg** said "But I can also see arguments for why this shouldn't be an error..."

### [Issue microsoft/TypeScript-go#2654](https://github.com/microsoft/TypeScript-go/issues/2654) (Open, `wontfix`)

**Empty array can now be assigned to a bespoke property on a function**

*tsgo allows assigning an empty array to an undeclared function property inferring never[], whereas TypeScript 5.9 reports error TS7008*

 * created by **peetklecha**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2654#issuecomment-3842382017) **jakebailey** said "Why is it expected that this errors?"

### [Issue microsoft/TypeScript-go#2655](https://github.com/microsoft/TypeScript-go/issues/2655) (Open, `wontfix`)

**Incorrect type error when assigning to an index in a \`{}\[\]\`\-typed field where the index is any\-typed and field is defined in a base class in a JS file**

*tsgo wrongly reports type errors when assigning to an any-indexed element of a {}[] field in a JS base class.*

 * created by **peetklecha**

### [Issue microsoft/TypeScript-go#2656](https://github.com/microsoft/TypeScript-go/issues/2656) (Open)

**Exports are no longer recognized in js modules which contain functions with parameter called \`module\` which have \`module\.exports =\` in their body**

*A function parameter named module with module.exports in it prevents tsgo from recognizing exports while TypeScript 5.9 accepts them.*

 * created by **peetklecha**

### [PR microsoft/TypeScript-go#2657](https://github.com/microsoft/TypeScript-go/pull/2657) (Closed, **jakebailey**, **Copilot**)

**Fix resolveJsonModule default for nodenext module**

*Default resolveJsonModule to true for the nodenext module kind by updating the GetResolveJsonModule switch-case to include it.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2658](https://github.com/microsoft/TypeScript-go/pull/2658) (Closed, **jakebailey**, **Copilot**)

**Fix smart select to include inner content selection for string literals**

*Enable inner content selection and template literal handling for smartSelect.expand in the Go port, matching TypeScript behavior with bounds checks*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#2659](https://github.com/microsoft/TypeScript-go/pull/2659) (Closed)

**Fix generate CI task flakes**

*CI generate tasks are flaky because tests produce baselines only after initial failures, requiring repeated runs.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2659#issuecomment-3843088796) **gabritto** asked why tests produced baselines after failing for other reasons
 * [today](https://github.com/microsoft/TypeScript-go/pull/2659#issuecomment-3843128793) **jakebailey** said "They're "server" style tests which log out info from the test itself"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2660](https://github.com/microsoft/TypeScript-go/pull/2660) (Closed)

**Adjust request failure reporting**

*Update request failure reporting sanitizer to strip memory offsets, goroutine info, and slashes in RequestMethod while retaining line numbers.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** closed the issue

### [Issue microsoft/TypeScript-go#2661](https://github.com/microsoft/TypeScript-go/issues/2661) (Open, `Domain: Editor`)

**auto\-import adds inline type modifier to existing import type statement**

*Auto-import incorrectly adds inline type modifiers to named imports in an import type statement, causing a TS2206 error.*

 * created by **mrvissercb**
 * **mrvissercb** added label `Domain: Editor`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2661#issuecomment-3843462895) **mrvissercb** said "Originally reported here: https://github.com/microsoft/vscode/issues/292038"

### [PR microsoft/TypeScript-go#2662](https://github.com/microsoft/TypeScript-go/pull/2662) (Open, `dependencies`, `javascript`)

**Bump @isaacs/brace\-expansion from 5\.0\.0 to 5\.0\.1**

*Bump @isaacs/brace-expansion dependency from version 5.0.0 to 5.0.1.*

 * created by **dependabot[bot]**
 * (today) **dependabot[bot]** added labels `dependencies`, `javascript`, `dependencies`, `javascript`

### [PR microsoft/TypeScript-go#2663](https://github.com/microsoft/TypeScript-go/pull/2663) (Closed)

**Sort index types by indexFlags, not flags again**

*Change index type sorting logic to compare indexFlags instead of flags for correct ordering*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2664](https://github.com/microsoft/TypeScript-go/pull/2664) (Open, **DanielRosenwasser**, **Copilot**)

**Fix panic on negative indentation in JSDoc formatting within nested scopes**

*The JSDoc formatter panics on sentinel negative indentation in nested scopes, so negative indentation now short-circuits formatting.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **DanielRosenwasser**

### [PR microsoft/TypeScript-go#2665](https://github.com/microsoft/TypeScript-go/pull/2665) (Closed)

**MayBe: Fix flaky formatting on type**

*Update the MayBe type's formatting logic to eliminate flaky output behavior.*

 * created by **sheetalkamat**

### [Issue microsoft/TypeScript-go#2666](https://github.com/microsoft/TypeScript-go/issues/2666) (Open)

**\`tsc \-\-build\` fails to invalidate incremental cache after dependency update**

*TypeScript incremental builds fail to invalidate cache after dependency updates, ignoring type changes until tsconfig.tsbuildinfo is deleted.*

 * created by **rubenferreira97**

### [Issue microsoft/TypeScript-go#2667](https://github.com/microsoft/TypeScript-go/issues/2667) (Open, **DanielRosenwasser**, **Copilot**)

**Quick info/hover on ambient module shows \`namespace\` keyword**

*Quick info on ambient module declarations erroneously displays the ‘namespace’ keyword instead of ‘module’.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** assigned to **Copilot**, **DanielRosenwasser**

### [PR microsoft/TypeScript-go#2668](https://github.com/microsoft/TypeScript-go/pull/2668) (Open, **DanielRosenwasser**, **Copilot**)

**Fix hover text for ambient modules to display "module" instead of "namespace"**

*Update quick info hover for ambient modules to correctly display 'module' instead of 'namespace'.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **DanielRosenwasser**

### [Issue microsoft/TypeScript-go#2669](https://github.com/microsoft/TypeScript-go/issues/2669) (Closed, `Crash`, **gabritto**)

**Completions crash for unrecognized ambiently\-defined file extensions**

*Completions for import paths with ambiently-declared nonstandard file extensions crash the TypeScript server due to unexpected extension handling.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** added label `Crash`, and assigned to **gabritto**

### [Issue microsoft/TypeScript-go#2670](https://github.com/microsoft/TypeScript-go/issues/2670) (Closed, `Crash`, **DanielRosenwasser**)

**Document highlights crash when missing \`catch\` and \`finally\` clauses**

*Document highlights request on a try statement missing catch or finally triggers a nil pointer panic in the TypeScript server.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** added label `Crash`, and assigned to **DanielRosenwasser**

### [Issue microsoft/TypeScript-go#2671](https://github.com/microsoft/TypeScript-go/issues/2671) (Open, `Crash`, **andrewbranch**, **Copilot**)

**LS request crash when \`package\.json\` bizarrely maps specifier to \`\.ts\` file**

*The TypeScript language server crashes resolving imports when package.json’s imports field maps specifiers to .ts files.*

 * created by **DanielRosenwasser**
 * **DanielRosenwasser** added label `Crash`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2671#issuecomment-3844761361) **DanielRosenwasser** said "I'm sure there's something simpler here with ambient modules, but I don't know what it is."

### [PR microsoft/TypeScript-go#2672](https://github.com/microsoft/TypeScript-go/pull/2672) (Closed)

**Fix document highlights crashes on missing tokens/nodes**

*Handle missing tokens or nodes to prevent crashes in document highlighting functionality.*

 * created by **DanielRosenwasser**

### [PR microsoft/TypeScript-go#2673](https://github.com/microsoft/TypeScript-go/pull/2673) (Open)

**Remove isElisionBlocked**

*Remove the outdated isElisionBlocked function to resolve import elision conflicts after splitting transformers.*

 * created by **jakebailey**

### [Issue microsoft/TypeScript-go#2674](https://github.com/microsoft/TypeScript-go/issues/2674) (Closed, `Crash`)

**Crash when fetching adjusted position of malformed variable declaration**

*Requesting completions at a malformed variable declaration causes an index-out-of-range panic in the language service.*

 * created by **DanielRosenwasser**
 * **DanielRosenwasser** added label `Crash`

### [Issue microsoft/TypeScript-go#2675](https://github.com/microsoft/TypeScript-go/issues/2675) (Open)

**Untitled files only respect \`javascript\.\` settings**

*Untitled TypeScript files ignore typescript.inlayHints settings under tsgo and only respect JavaScript inlay hint configurations.*

 * created by **DanielRosenwasser**

### [PR microsoft/TypeScript-go#2676](https://github.com/microsoft/TypeScript-go/pull/2676) (Closed)

**Fix failing tests for hovers/quick info on \`this\`**

*The tests validating hover and quick info behavior for the ‘this’ keyword are failing and require fixes.*

 * created by **DanielRosenwasser**

### [PR microsoft/TypeScript-go#2677](https://github.com/microsoft/TypeScript-go/pull/2677) (Closed)

**fix\(2674\): fix identifier name lookup in variable declaration lists**

*Fix identifier name lookup in variable declaration lists to resolve issue 2674.*

 * created by **a-tarasyuk**

### [Issue microsoft/TypeScript-go#929](https://github.com/microsoft/TypeScript-go/issues/929) (Open, `Domain: Type Checking`, `Type Ordering`)

**Errors in @types/jsdom, @sinclair/typebox**

*TypeScript Native Preview triggers TS2321 excessive stack depth errors in @sinclair/typebox definitions via @types/jsdom in jest-environment-jsdom*

 * [34 weeks ago](https://github.com/microsoft/TypeScript-go/issues/929#issuecomment-2960201068) **Andarist** identified a type ordering issue in the relater code causing deep recursion due to flipped union ordering in Corsa
 * **ahejlsberg** added label `Type Ordering`
 * [23 weeks ago](https://github.com/microsoft/TypeScript-go/issues/929#issuecomment-3212360998) **jakebailey** reported that projects using jest now failed due to @jest/schemas depending on @sinclair/typebox causing TypeScript errors without skipLibCheck, discovered while testing build mode in DefinitelyTyped-tools
 * [today](https://github.com/microsoft/TypeScript-go/issues/929#issuecomment-3843884423) **Icantjuddle** said "Any update on this? "
 * [today](https://github.com/microsoft/TypeScript-go/issues/929#issuecomment-3843892128) **jakebailey** said "For typebox, my understanding is that a newer version already fixed it, but jest and others still depend on an old version. It'd probably be worth asking for a backport upstream?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/929#issuecomment-3845678994) **sinclairzx81** published a hotfix for TS7 in TypeBox 0.27.10, provided update instructions, and asked for testing confirmation

