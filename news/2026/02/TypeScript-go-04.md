# Report for 2026-02-04 (Wednesday, February 4th, 2026)

13 different users commented on 35 different issues.

## Recommended Actions

 * Response Recommended
    * @rubenferreira97 asked how to profile a hanging process since `--pprofDir` only emitted data on completion and building #2459 still hangs in [microsoft/TypeScript-go#2678](https://github.com/microsoft/TypeScript-go/issues/2678#issuecomment-3848715309)
    * @rubenferreira97 suggested adding a flag to capture initial duration for debugging and offered further help in [microsoft/TypeScript-go#2678](https://github.com/microsoft/TypeScript-go/issues/2678#issuecomment-3849135940)

## Activity Summary

### [Issue microsoft/TypeScript-go#1905](https://github.com/microsoft/TypeScript-go/issues/1905) (Closed, `Crash`, **sheetalkamat**)

**panic: vfs: path is not absolute**

*The VFS implementation panics when given a URL-based path because it expects an absolute filesystem path.*

 * [9 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1905#issuecomment-3604718075) **IOLOII** reported a crash when opening JavaScript or TypeScript files in a Vue project using the plugin and offered to provide repro steps later
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1905#issuecomment-3744284117) **marcomow** reported a similar issue when using Deno 2.6.4 with --unstable-tsgo and provided the resulting RPC panic stack trace
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/1905#issuecomment-3834957222) **gggdomi** reported seeing a panic in the latest extension version when importing excellentexport from Skypack, noting the code had worked until a few days ago
 * (today) **sheetalkamat** closed the issue

### [PR microsoft/TypeScript-go#2620](https://github.com/microsoft/TypeScript-go/pull/2620) (Closed)

**Bring back async API, allow API connection to LSP process**

*Reintroduce a decoupled async JSON-RPC API client and server in the LSP to enable external extensions to query TypeScript state.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2620#issuecomment-3843063540) **andrewbranch** explained why the API requires clients to release objects and demonstrated using statements for automatic cleanup
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2620#issuecomment-3843140487) **gabritto** explained that the API requires explicit cleanup of symbols and types across remote calls, provided a using-syntax example, and asked what happens to returned objects when the project changes
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2620#issuecomment-3843551857) **andrewbranch** explained that the client controlled when to adopt the latest LSP session snapshot, allowing it to retain older objects indefinitely and reuse source files and symbols, and postponed implementing automatic purging for simplicity
 * [today](https://github.com/microsoft/TypeScript-go/pull/2620#issuecomment-3850390977) **andrewbranch** asked what version of tinybench was installed, noted v3.1.1 lacked that many lines, and mentioned that Jake changed it in main

### [PR microsoft/TypeScript-go#2623](https://github.com/microsoft/TypeScript-go/pull/2623) (Open)

**Fix inlay hints panic: guard against stale line map in LineAndCharacterToPosition**

*Prevent inlay hint panics by guarding against stale line map offsets in LineAndCharacterToPosition*

 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/2623#issuecomment-3834947424) **abelcha** questioned whether recomputing line maps on every request was worth the performance hit and suggested using a guard instead
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/2623#issuecomment-3837337190) **DanielRosenwasser** described two cases needing handling: '/resolve'-like requests with content length changes causing non-existent positions, and logic operating on nodes with source text from the wrong file; and noted the need to recalculate or dismiss outdated line maps
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/2623#issuecomment-3837346475) **DanielRosenwasser** noted a potential issue with the snapshot implementation and explained that snapshots prevent data state inconsistencies
 * [today](https://github.com/microsoft/TypeScript-go/pull/2623#issuecomment-3849685810) **DanielRosenwasser** opened an issue to track discussion on unexplained issues

### [Issue microsoft/TypeScript-go#2650](https://github.com/microsoft/TypeScript-go/issues/2650) (Open, `Crash`, **jakebailey**, **Copilot**)

**Specifying declaration files in "moduleSuffixes" leads to panic**

*Including declaration files in moduleSuffixes triggers a panic in typescript-go’s checker during external module resolution.*

 * created by **voronin-ivan**
 * **voronin-ivan** added label `Crash`
 * (later) **jakebailey** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#2651](https://github.com/microsoft/TypeScript-go/issues/2651) (Closed, `Domain: Editor`, **jakebailey**, **Copilot**)

**Different behaviour of \`editor\.action\.smartSelect\` vs built\-in TS**

*smartSelect.expand includes surrounding quotes when selecting bracketed strings with the TS native preview extension but not with the built-in TypeScript.*

 * (yesterday) **jakebailey** assigned to **Copilot**, **jakebailey**
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2651#issuecomment-3845450009) **starball5** said "(related on Stack Overflow: How to change the VSCode SmartSelect interaction with quotation marks)"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2658](https://github.com/microsoft/TypeScript-go/pull/2658) (Closed, **jakebailey**, **Copilot**)

**Fix smart select to include inner content selection for string literals**

*Enable inner content selection and template literal handling for smartSelect.expand in the Go port, matching TypeScript behavior with bounds checks*

 * created by **Copilot**
 * (yesterday) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2665](https://github.com/microsoft/TypeScript-go/pull/2665) (Closed)

**MayBe: Fix flaky formatting on type**

*Update the MayBe type's formatting logic to eliminate flaky output behavior.*

 * created by **sheetalkamat**
 * (today) **sheetalkamat** closed the issue

### [Issue microsoft/TypeScript-go#2669](https://github.com/microsoft/TypeScript-go/issues/2669) (Closed, `Crash`, **gabritto**)

**Completions crash for unrecognized ambiently\-defined file extensions**

*Completions for import paths with ambiently-declared nonstandard file extensions crash the TypeScript server due to unexpected extension handling.*

 * created by **DanielRosenwasser**
 * (yesterday) **DanielRosenwasser** added label `Crash`, and assigned to **gabritto**
 * (today) **gabritto** closed the issue

### [Issue microsoft/TypeScript-go#2670](https://github.com/microsoft/TypeScript-go/issues/2670) (Closed, `Crash`, **DanielRosenwasser**)

**Document highlights crash when missing \`catch\` and \`finally\` clauses**

*Document highlights request on a try statement missing catch or finally triggers a nil pointer panic in the TypeScript server.*

 * created by **DanielRosenwasser**
 * (yesterday) **DanielRosenwasser** added label `Crash`, and assigned to **DanielRosenwasser**
 * (today) **DanielRosenwasser** closed the issue

### [Issue microsoft/TypeScript-go#2671](https://github.com/microsoft/TypeScript-go/issues/2671) (Open, `Crash`, **andrewbranch**, **Copilot**)

**LS request crash when \`package\.json\` bizarrely maps specifier to \`\.ts\` file**

*The TypeScript language server crashes resolving imports when package.json’s imports field maps specifiers to .ts files.*

 * created by **DanielRosenwasser**
 * **DanielRosenwasser** added label `Crash`
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2671#issuecomment-3844761361) **DanielRosenwasser** said "I'm sure there's something simpler here with ambient modules, but I don't know what it is."
 * **DanielRosenwasser** assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2671#issuecomment-3849109195) **andrewbranch** said "It sure looks like this should crash via batch compilation too..."
 * **andrewbranch** assigned to **Copilot**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2671#issuecomment-3849156368) **DanielRosenwasser** said "It looks like it- maybe I wasn't running on a new-enough version of tsgo when I tried."

### [PR microsoft/TypeScript-go#2672](https://github.com/microsoft/TypeScript-go/pull/2672) (Closed)

**Fix document highlights crashes on missing tokens/nodes**

*Handle missing tokens or nodes to prevent crashes in document highlighting functionality.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** closed the issue

### [Issue microsoft/TypeScript-go#2674](https://github.com/microsoft/TypeScript-go/issues/2674) (Closed, `Crash`)

**Crash when fetching adjusted position of malformed variable declaration**

*Requesting completions at a malformed variable declaration causes an index-out-of-range panic in the language service.*

 * created by **DanielRosenwasser**
 * **DanielRosenwasser** added label `Crash`
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#2676](https://github.com/microsoft/TypeScript-go/pull/2676) (Closed)

**Fix failing tests for hovers/quick info on \`this\`**

*The tests validating hover and quick info behavior for the ‘this’ keyword are failing and require fixes.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#2677](https://github.com/microsoft/TypeScript-go/pull/2677) (Closed)

**fix\(2674\): fix identifier name lookup in variable declaration lists**

*Fix identifier name lookup in variable declaration lists to resolve issue 2674.*

 * created by **a-tarasyuk**
 * (today) **DanielRosenwasser** closed the issue

### [Issue microsoft/TypeScript-go#2678](https://github.com/microsoft/TypeScript-go/issues/2678) (Open)

**\`tsgo \-\-build\` hangs indefinitely**

*After upgrading from @sinclair/typebox 0.34.48 to typebox 1.0.81, tsgo --build hangs indefinitely during type-checking and declaration emission.*

 * created by **rubenferreira97**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2678#issuecomment-3848482663) **jakebailey** suggested pulling fixes from #1693 or #2459 and noted that the --pprofDir flag collects the profiling info
 * [today](https://github.com/microsoft/TypeScript-go/issues/2678#issuecomment-3848715309) **rubenferreira97** reported that `--pprofDir` only created a 0KB profile file when tsgo finished and asked how to profile a hanging process, noting that build #2459 still hung
 * [today](https://github.com/microsoft/TypeScript-go/issues/2678#issuecomment-3848719531) **jakebailey** said "It does, yeah. Sorry, I realized the implication of it hanging after I replied."
 * [today](https://github.com/microsoft/TypeScript-go/issues/2678#issuecomment-3849135940) **rubenferreira97** suggested adding a flag to capture a specific initial duration for debugging and offered further assistance

### [PR microsoft/TypeScript-go#2679](https://github.com/microsoft/TypeScript-go/pull/2679) (Closed)

**Fix unknown extension crash in completions**

*Update path completions to gracefully handle unsupported file extensions and prevent crashes.*

 * created by **gabritto**
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript-go#2680](https://github.com/microsoft/TypeScript-go/pull/2680) (Closed, **andrewbranch**, **Copilot**)

**Fix module resolver bug exposed by malformed package\.json import patterns**

*Fix module resolver bug that crashed the language server with malformed package.json wildcard import patterns*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2680#issuecomment-3849529032) **andrewbranch** pointed out that the panic was correct in the first if block and shouldn't be changed, noted a misleading panic message in the second block, and suggested fixing it in the module resolver
 * [today](https://github.com/microsoft/TypeScript-go/pull/2680#issuecomment-3849562676) **Copilot** explained that the panic exposed a module resolver bug where the TS extension flag was set from the package.json pattern instead of the original module specifier and noted its fix in commit 90aa27c0
 * [today](https://github.com/microsoft/TypeScript-go/pull/2680#issuecomment-3849602497) **Copilot** restored both panics and explained that the first was correct and the second is now a valid assertion after the module resolver fix

### [Issue microsoft/TypeScript-go#2681](https://github.com/microsoft/TypeScript-go/issues/2681) (Closed, `help wanted`, `Crash`)

**textDocument/completion: runtime error: invalid memory address or nil pointer dereference**

*The TypeScript Go LSP server panics with a nil pointer dereference during textDocument/completion requests.*

 * created by **sanny-io**
 * **sanny-io** added label `Crash`
 * (today) **DanielRosenwasser** added label `help wanted`, assigned to **DanielRosenwasser**, and unassigned **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2681#issuecomment-3849539979) **DanielRosenwasser** provided minimal repros and explained that reserved keywords disrupt parsing, causing a stray colon token, and noted the code change to direct Parent.Parent access

### [Issue microsoft/TypeScript-go#2682](https://github.com/microsoft/TypeScript-go/issues/2682) (Open, `Crash`)

**Various language server commands crash during position retrieval**

*Language server commands like hover crash due to LineAndCharacterToPosition mapping errors potentially caused by outdated snapshots or other unknown conditions.*

 * created by **DanielRosenwasser**
 * **DanielRosenwasser** added label `Crash`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2682#issuecomment-3849620766) **andrewbranch** described a code path introduced by PR #1767 that triggered disk reads for line map content and suggested separating disk-allowed reads to trigger a distinct panic when files aren’t found

### [Issue microsoft/TypeScript-go#2683](https://github.com/microsoft/TypeScript-go/issues/2683) (Open)

**TS2590: "Expression produces a union type that is too complex to represent" on generics types**

*A generic type union in the @regle monorepo triggers TS2590 errors due to overly complex inferred types in newer TypeScript versions*

 * created by **victorgarciaesgi**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2683#issuecomment-3849958583) **jakebailey** suggested that a union ordering issue in UnionToTuple was causing the problem and recommended testing with --stableTypeOrdering on the PR build
 * [later](https://github.com/microsoft/TypeScript-go/issues/2683#issuecomment-3852054349) **victorgarciaesgi** thanked the maintainer, noted that UnionToTuple produced a TS2321 error on a simple inferring generic, and said they would try stableTypeOrdering

### [Issue microsoft/TypeScript-go#2684](https://github.com/microsoft/TypeScript-go/issues/2684) (Open, `Crash`, **andrewbranch**)

**nil source file in aliasResolve\.GetSourceFile**

*A nil source file causes a segmentation fault in aliasResolver.GetSourceFile during module resolution.*

 * created by **jakebailey**
 * **jakebailey** added label `Crash`
 * **andrewbranch** assigned to **andrewbranch**

### [PR microsoft/TypeScript-go#2685](https://github.com/microsoft/TypeScript-go/pull/2685) (Closed)

**Handle urls in import path by making vfs not panic on Url paths**

*Modify the virtual file system to properly handle URL-based import paths without causing panics.*

 * created by **sheetalkamat**
 * (today) **sheetalkamat** closed the issue

### [Issue microsoft/TypeScript-go#2686](https://github.com/microsoft/TypeScript-go/issues/2686) (Open, `Domain: Editor`, **andrewbranch**)

**Packages \`pnpm link\`ed from outside the workspace trigger no watch events when changed**

*Linked external packages don’t trigger watch events on changes, preventing diagnostic updates until the server restarts.*

 * created by **andrewbranch**
 * **andrewbranch** added label `Domain: Editor`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2686#issuecomment-3850202915) **sheetalkamat** described how Strada watched `node_modules/package` for links and otherwise `node_modules` for failed lookups and linked the relevant pull request

### [PR microsoft/TypeScript-go#2687](https://github.com/microsoft/TypeScript-go/pull/2687) (Closed)

**fix\(2681\): prevent nil parent context in import\-attributes**

*Add validation to import-attributes to prevent a nil parent context from causing errors.*

 * created by **a-tarasyuk**

### [PR microsoft/TypeScript-go#2688](https://github.com/microsoft/TypeScript-go/pull/2688) (Open, **RyanCavanaugh**, **Copilot**)

**Port TypeScript PR \#63054: Default \`types\` to \`\[\]\`, support \`"\*"\` wildcard**

*Default compilerOptions.types to an empty array and add support for the "*" wildcard to control automatic @types discovery.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**

### [PR microsoft/TypeScript-go#2689](https://github.com/microsoft/TypeScript-go/pull/2689) (Closed)

**Start targeting TS 6\.0 behavior**

*Bump TypeScript submodule to main, port key compiler settings, and adjust or skip tests for TypeScript 6.0 compliance.*

 * created by **jakebailey**

### [Issue microsoft/TypeScript-go#2690](https://github.com/microsoft/TypeScript-go/issues/2690) (Open, `Crash`, **andrewbranch**)

**Panic \- inlayHint \- bad line number \- from autofix/auto\-formatting setup**

*The language server panics during inlayHint requests because an autofix formatting change produces an out-of-range line number.*

 * created by **lukpsaxo**
 * **lukpsaxo** added label `Crash`
 * **DanielRosenwasser** assigned to **andrewbranch**

### [Issue microsoft/TypeScript-go#2691](https://github.com/microsoft/TypeScript-go/issues/2691) (Closed, `Crash`)

**panic: runtime error: invalid memory address or nil pointer dereference**

*Typescript-go panics with a nil pointer dereference in source file binding while resolving external modules*

 * created by **voronin-ivan**
 * **voronin-ivan** added label `Crash`
 * [later](https://github.com/microsoft/TypeScript-go/issues/2691#issuecomment-3854481475) **jakebailey** said "Dupe of #2684 "
 * (later) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2692](https://github.com/microsoft/TypeScript-go/issues/2692) (Open, **jakebailey**, **Copilot**)

**tsgo does not respect \`esModuleInterop\` in certain cases**

*tsgo ignores the esModuleInterop setting when importing named exports from CommonJS JavaScript files with allowJs enabled, causing TS2497 errors.*

 * created by **psm14**
 * [later](https://github.com/microsoft/TypeScript-go/issues/2692#issuecomment-3854498259) **jakebailey** said "Feels like https://github.com/microsoft/typescript-go/issues/1054, potentially "
 * (later) **jakebailey** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#2693](https://github.com/microsoft/TypeScript-go/pull/2693) (Open, **jakebailey**, **Copilot**)

**Fix esModuleInterop not being respected for JS CommonJS imports**

*tsgo incorrectly reports TS2497 for named exports from CommonJS JavaScript files despite esModuleInterop being enabled*

 * created by **Copilot**
 * (later) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#2694](https://github.com/microsoft/TypeScript-go/pull/2694) (Open, **jakebailey**, **Copilot**)

**Fix panic when moduleSuffixes resolves to declaration files**

*Fix panic by extracting file extensions from the original candidate path when moduleSuffixes includes declaration file suffixes.*

 * created by **Copilot**
 * (later) **Copilot** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#929](https://github.com/microsoft/TypeScript-go/issues/929) (Open, `Domain: Type Checking`, `Type Ordering`)

**Errors in @types/jsdom, @sinclair/typebox**

*TypeScript Native Preview triggers TS2321 excessive stack depth errors in @sinclair/typebox definitions via @types/jsdom in jest-environment-jsdom*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/929#issuecomment-3843884423) **Icantjuddle** said "Any update on this? "
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/929#issuecomment-3843892128) **jakebailey** said "For typebox, my understanding is that a newer version already fixed it, but jest and others still depend on an old version. It'd probably be worth asking for a backport upstream?"
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/929#issuecomment-3845678994) **sinclairzx81** published a hotfix for TS7 in TypeBox 0.27.10, provided update instructions, and asked for testing confirmation
 * [today](https://github.com/microsoft/TypeScript-go/issues/929#issuecomment-3850324039) **jakebailey** said "Tested it in DefinitelyTyped-tools and it does indeed work (transitive dep via jest). Thank you!"

