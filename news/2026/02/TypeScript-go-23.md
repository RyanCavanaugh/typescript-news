# Report for 2026-02-23 (Monday, February 23rd, 2026)

14 different users commented on 33 different issues.

## Activity Summary

### [Issue microsoft/TypeScript-go#2194](https://github.com/microsoft/TypeScript-go/issues/2194) (Closed, `Domain: Editor`, **Copilot**)

**Destructured interface members lack inherited JSDoc comments**

*Destructured interface members in VS Code fail to display inherited JSDoc hover comments.*

 * created by **Bertie690**
 * **Bertie690** added label `Domain: Editor`
 * **jakebailey** assigned to **Copilot**
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#2195](https://github.com/microsoft/TypeScript-go/pull/2195) (Closed, **jakebailey**, **Copilot**)

**Fix missing JSDoc comments on destructured interface properties**

*Retrieve JSDoc comments from interface properties for destructured binding elements in hover and signature help aligned with TypeScript implementation*

 * **Copilot** assigned to **jakebailey**
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/2195#issuecomment-3937388968) **jakebailey** said "@copilot pull and merge main in. when you pull, make sure you have done git submodule update as to not accidentally move the submodule backward. on conflicts, git does not update submodules."
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/2195#issuecomment-3937481152) **Copilot** merged main into the branch, updated the submodule, and resolved conflicts in hover.go and signaturehelp.go incorporating the commentOnly parameter
 * (today) **DanielRosenwasser** closed the issue

### [Issue microsoft/TypeScript-go#2223](https://github.com/microsoft/TypeScript-go/issues/2223) (Closed, `Domain: Editor`)

**Request textDocument/foldingRange failed\.**

*The TypeScript language server panics with a token cache mismatch error when requesting folding ranges in a compiled JavaScript file.*

 * [11 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2223#issuecomment-3614758634) **jakebailey** described also encountering the issue in a .ncurc.cjs file and struggling to integrate it into a fourslash test suite
 * [6 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2223#issuecomment-3730907291) **jfirebaugh** provided a minimal reproduction snippet
 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2223#issuecomment-3763299411) **jycouet** provided an additional code snippet with an import statement for Page from '@playwright/test'
 * [today](https://github.com/microsoft/TypeScript-go/issues/2223#issuecomment-3947856597) **gabritto** said "Fixed by #2789."
 * (today) **gabritto** closed the issue

### [Issue microsoft/TypeScript-go#2402](https://github.com/microsoft/TypeScript-go/issues/2402) (Closed, `Crash`, **jakebailey**, **Copilot**)

**tsgo takes forever to compile, 325seconds vs typescript 42seconds**

*tsgo watch compilation takes 325s versus TypeScript’s 42s, and the reporter requests help diagnosing and resolving the slowdown.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2402#issuecomment-3941359888) **jakebailey** stated that the previous analysis added nothing new and encouraged a fix submission while noting the issue's complexity due to emit phase line map changes
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2402#issuecomment-3941829062) **jogibear9988** apologized for distracting and mentioned asking Copilot to explain why it works in JS but not in Go
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2402#issuecomment-3941938891) **jakebailey** said "Try #2872 to see if it fixes your case."
 * (today) **jakebailey** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/issues/2402#issuecomment-3947144542) **jogibear9988** apologized for not testing due to the class fields transformer not being implemented and reverted the codebase to normal TypeScript

### [Issue microsoft/TypeScript-go#2780](https://github.com/microsoft/TypeScript-go/issues/2780) (Open, `Domain: Editor`, `Needs More Info`, **andrewbranch**)

**High memory consumption in a large pnpm monorepo**

*PR #2502 causes minor edits in a large pnpm monorepo to spike the TypeScript extension memory from ~700MB to ~35GB.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-3941537584) **andrewbranch** asked for the package or file causing the issue and requested debug details and dependency files to reproduce
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-3942722362) **shinichy** mentioned inability to share code from private repo, noted that bucket.DependencyNames was nil and len(bucket.Paths) was 0, and offered to create a public repo to reproduce the issue
 * [today](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-3943840500) **justinsmid** reported experiencing excessive memory usage and provided cache stats and a heap profile, noting the project was private but accessible to Jake Bailey
 * [today](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-3945883495) **andrewbranch** noted that the profile showed 9.5 GB of usage, explained that a nil DependencyNames bucket leads to gathering auto-imports from the entire directory, and suggested debugging computeDependenciesForNodeModulesDirectory

### [Issue microsoft/TypeScript-go#2822](https://github.com/microsoft/TypeScript-go/issues/2822) (Open, `Domain: Editor`, **andrewbranch**)

**Harden LSP against requests for files that don't have open projects**

*Enhance the LSP to gracefully handle requests for files not in open projects to avoid errors.*

 * created by **andrewbranch**
 * (6 days ago) **andrewbranch** added label `Domain: Editor`, and assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2822#issuecomment-3948026886) **DanielRosenwasser** mentioned that VS Code also requests diagnostics after closing files and provided logs and reproduction steps via 'close others'

### [Issue microsoft/TypeScript-go#2824](https://github.com/microsoft/TypeScript-go/issues/2824) (Open, `Domain: API and Extensibility`, **andrewbranch**)

**API usage patterns for complex editor extensions**

*Exploring IPC-based API features for a Go TS server to replace TS Server plugins and support Vue editor extensions*

 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-3935891423) **andrewbranch** asked if his understanding of Svelte project service file discovery was correct and if other languages faced similar situations
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-3936069400) **chriskrycho** explained that projects adopt TypeScript’s module resolution semantics and likened the necessary tooling transformations to TSX/JSX syntactic shenanigans
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-3936221722) **aheber** described two main actions: dynamically modifying the resolved tsconfig to register module paths and lying about non-JS files as importable modules by intercepting read/write operations; explained desire to avoid on-disk declaration files and tsconfig edits while retaining refactoring support; asked if tsgo’s architecture can support intercepting file write actions for virtual modules
 * [today](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-3947458101) **andrewbranch** clarified that they meant injecting types via TypeScript syntax in virtual files that don’t exist on disk, rather than inserting types directly into type resolution via a JS object API

### [Issue microsoft/TypeScript-go#2867](https://github.com/microsoft/TypeScript-go/issues/2867) (Closed, **DanielRosenwasser**, **Copilot**)

**tsgo formatter doesn't format imports the same as TS TS**

*tsgo’s formatter does not reformat multi-line import statements like TypeScript’s built-in formatter, causing commit errors.*

 * (3 days ago) **DanielRosenwasser** assigned to **Copilot**, **DanielRosenwasser**
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/2867#issuecomment-3938629699) **erengeez** said "Automatic importing with autocomplete or Quick Fix actually adds extra newline as I described in #2637 which creates this exact situation. Will the PR fix it also?"
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#2869](https://github.com/microsoft/TypeScript-go/pull/2869) (Closed, **DanielRosenwasser**, **Copilot**)

**fix: formatter correctly moves \`}\` to new line for multiline import braces**

*Ensure the tsgo formatter places the closing brace on a new line for multiline import statements and update relevant tests.*

 * created by **Copilot**
 * (3 days ago) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#2872](https://github.com/microsoft/TypeScript-go/pull/2872) (Closed)

**Speed up source map emit with printer\-local monotomic cache**

*Introducing a printer-local monotonic cache for source map emission achieves up to 230× speedup and cuts memory allocations.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2876](https://github.com/microsoft/TypeScript-go/pull/2876) (Closed)

**Pre\-grow TextWriter in emit**

*Pre-growing the TextWriter buffer in emit reduces allocations by ~3% and memory usage by up to 13% in benchmarks.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2877](https://github.com/microsoft/TypeScript-go/pull/2877) (Closed)

**\[@typescript/api\] Add generated node factory, two\-way AST encoding/decoding, emitter\.printNode**

*Add generated node factory and forEachChild visitor, two-way AST encoding/decoding, and new typeToTypeNode, typeToString, and printNode API calls.*

 * created by **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#2878](https://github.com/microsoft/TypeScript-go/pull/2878) (Closed)

**OrganizeImports unit tests port**

*Ported most OrganizeImports unit tests from TypeScript to tsgo.*

 * created by **johnfav03**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2878#issuecomment-3946939006) **jakebailey** said "Are these doable as fourslash tests? They were unit tests originally I know, but, it seems out of place."
 * (today) **johnfav03** closed the issue

### [PR microsoft/TypeScript-go#2879](https://github.com/microsoft/TypeScript-go/pull/2879) (Closed)

**Hopefully settle line endings / position mapping**

*Renamed various position-mapping functions, introduced a UTF16Offset type, and corrected line-ending and source-map offset calculations.*

 * created by **jakebailey**

### [Issue microsoft/TypeScript-go#2880](https://github.com/microsoft/TypeScript-go/issues/2880) (Open)

**TS4094 for exported class expressions with ES private fields \(tsc handles via name mangling\)**

*tsgo incorrectly errors on exported class expressions using ES private fields, unlike tsc which name-mangles them.*

 * created by **duci9y**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2880#issuecomment-3947117028) **jakebailey** said "Maybe I'm wrong, but I feel like the original behavior was a bug. noEmit just controls whether or not we emit files. The editor is also a "noEmit" situation, but we show these errors there..."

### [Issue microsoft/TypeScript-go#2881](https://github.com/microsoft/TypeScript-go/issues/2881) (Open)

**\[ServerErrors\]\[JavaScript\] linux\-x64\-7\.0\.0\-dev\.20260223\.1 vs **

*The linux-x64-7.0.0-dev.20260223.1 pipeline on 300 TypeScript repos detected three interesting changes, two clone failures, nineteen timeouts, and three unknown failures.*

 * created by **typescript-bot**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2881#issuecomment-3947789231) **typescript-bot** reported a panic during cross-project handling for textDocument/references due to an unexpected KindIdentifier in a KindFunctionExpression's trivia
 * [today](https://github.com/microsoft/TypeScript-go/issues/2881#issuecomment-3947789265) **typescript-bot** reported server connection closed prematurely with undefined error and listed the affected repository and recent requests
 * [today](https://github.com/microsoft/TypeScript-go/issues/2881#issuecomment-3947789311) **typescript-bot** reported a server connection closed prematurely error with affected repository details, last requests, and repro steps

### [Issue microsoft/TypeScript-go#2882](https://github.com/microsoft/TypeScript-go/issues/2882) (Open, `Crash`)

**Probable nil entry from specifier cache in auto\-import completions**

*Auto-import completions may fail or crash due to a nil entry in the specifier cache with no known repro steps.*

 * created by **DanielRosenwasser**
 * **DanielRosenwasser** added label `Crash`

### [PR microsoft/TypeScript-go#2883](https://github.com/microsoft/TypeScript-go/pull/2883) (Closed)

**Don't allocate intermediate tokens in \`FindChildOfKind\(\)\`\.**

*Modify FindChildOfKind to defer GetOrCreateToken calls and avoid unnecessary token allocations until the specific token is found.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** assigned to **jakebailey**, **gabritto**, and unassigned **jakebailey**, **gabritto**
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#2885](https://github.com/microsoft/TypeScript-go/pull/2885) (Closed)

**Fix retrieval of named children in JS RemoteNode**

*Adjust the JS RemoteNode getNamedChild logic to iterate immediate child nodes and correctly return a BinaryExpression’s operatorToken.*

 * created by **auvred**
 * [later](https://github.com/microsoft/TypeScript-go/pull/2885#issuecomment-3949981990) **auvred** said "Oh, this was already fixed in https://github.com/microsoft/typescript-go/pull/2877"
 * (later) **auvred** closed the issue

### [Issue microsoft/TypeScript-go#2886](https://github.com/microsoft/TypeScript-go/issues/2886) (Closed, `Domain: Editor`)

**Incorrect formatting after override modifier**

*Formatting fails to remove extra spaces following the override modifier in TypeScript class methods.*

 * created by **itrapashko**
 * **itrapashko** added label `Domain: Editor`

### [PR microsoft/TypeScript-go#2887](https://github.com/microsoft/TypeScript-go/pull/2887) (Closed)

**Fix formatting after override keyword**

*Adjust code formatting rules to correctly format code following the override keyword.*

 * created by **itrapashko**
 * [later](https://github.com/microsoft/TypeScript-go/pull/2887#issuecomment-3952283432) **itrapashko** said "I'm not sure where to put the test. I ended up putting it to the internal/fourslash/tests folder."

### [PR microsoft/TypeScript-go#2888](https://github.com/microsoft/TypeScript-go/pull/2888) (Open)

**Fixed a class member completion crash after JSDoc comment with degenerate JSDoc tag in it**

*Resolve class member completion crashes caused by malformed JSDoc tags in comments.*

 * created by **Andarist**

### [Issue microsoft/TypeScript-go#2889](https://github.com/microsoft/TypeScript-go/issues/2889) (Closed)

**Tsgo considers wrong API usage as correct \- difference in typechecking**

*tsgo wrongly treats improper use of orderBy in attachments as valid and infers incorrect types, unlike TypeScript’s stricter checks*

 * created by **jansedlon**

### [Issue microsoft/TypeScript-go#2890](https://github.com/microsoft/TypeScript-go/issues/2890) (Closed, `Crash`)

**panic handling request textDocument/inlayHint**

*The TypeScript-Go LSP server panics on textDocument/inlayHint requests because ComputedPropertyName AST nodes are unhandled.*

 * created by **Zzzen**
 * **Zzzen** added label `Crash`

### [PR microsoft/TypeScript-go#2891](https://github.com/microsoft/TypeScript-go/pull/2891) (Closed)

**fix\(ast\): handle computed property names in Node\.Text**

*Add support for computed property names in Node.Text AST generation*

 * created by **Zzzen**
 * [later](https://github.com/microsoft/TypeScript-go/pull/2891#issuecomment-3952520923) **ahejlsberg** clarified that Node.Text was intended only as an accessor for nodes with a text property and recommended not calling it on nodes without that property

### [PR microsoft/TypeScript-go#2892](https://github.com/microsoft/TypeScript-go/pull/2892) (Closed)

**Fixed a crash on computed property name when computing inlay hints**

*Computing inlay hints now correctly handles computed property names without crashing.*

 * created by **Andarist**

### [PR microsoft/TypeScript-go#2893](https://github.com/microsoft/TypeScript-go/pull/2893) (Closed)

**Improve CommonJS support**

*Enhance Corsa’s CommonJS support by allowing multiple module.exports assignments, supporting JSDoc typedef imports, and aligning export behavior with Strada.*

 * created by **ahejlsberg**

