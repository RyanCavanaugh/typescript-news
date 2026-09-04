# Report for 2026-08-30 (Sunday, August 30th, 2026)

16 different users commented on 70 different issues.

## Recommended Actions

 * Response Recommended
    * @tomaswrobel asked whether the issue would fit the merge criteria for post-6.0 patches in [microsoft/TypeScript#46135](https://github.com/microsoft/TypeScript/issues/46135#issuecomment-5479995982)
    * @typescript-automation[bot] reported that the linked issue hasn't been accepted in [microsoft/TypeScript#63919](https://github.com/microsoft/TypeScript/pull/63919#issuecomment-5471741188)
    * @Shivang9983 asked to be assigned the issue in [microsoft/TypeScript#64097](https://github.com/microsoft/TypeScript/issues/64097#issuecomment-5470912738)
    * @Shivang9983 asked to be assigned the issue in [microsoft/TypeScript#64098](https://github.com/microsoft/TypeScript/issues/64098#issuecomment-5470908358)

## Activity Summary

### [Issue microsoft/TypeScript#46135](https://github.com/microsoft/TypeScript/issues/46135) (Closed, `Suggestion`, `Awaiting More Feedback`, **gabritto**)

**Ambient Module Declarations for Import Attributes \(formerly known as Import Assertions\)**

*Enable ambient module declarations based on import attributes to provide type definitions for CSS modules and asset URL imports.*

 * [32 weeks ago](https://github.com/microsoft/TypeScript/issues/46135#issuecomment-3745345018) **justinfagnani** noted that major browsers, Node, Deno, Bun, Rollup, and Webpack support CSS and JSON modules with import attributes, and asked if that provides enough platform support for TypeScript support
 * [31 weeks ago](https://github.com/microsoft/TypeScript/issues/46135#issuecomment-3784607037) **jonathantneal** created a pull request for the issue
 * **gabritto** assigned to **gabritto**
 * [later](https://github.com/microsoft/TypeScript/issues/46135#issuecomment-5479995982) **tomaswrobel** said "Will the issue be implemented in a way that "fit the merge criteria for post-6.0 patches"?"

### [Issue microsoft/TypeScript#59031](https://github.com/microsoft/TypeScript/issues/59031) (Open, `Suggestion`, `Awaiting More Feedback`)

**\`abstract class\` should be usable in expressions**

*Allow abstract classes to be defined inline in expressions to reduce mixin verbosity.*

 * [2.1 years ago](https://github.com/microsoft/TypeScript/issues/59031#issuecomment-2190763728) **stwlam** said "Some additional issue corralling: it looks like the reporter of #32122 was basically running into the same problem, though the errors they pasted aren't the same."
 * (2.1 years ago) **RyanCavanaugh** added labels `Suggestion`, `Awaiting More Feedback`
 * [later](https://github.com/microsoft/TypeScript/issues/59031#issuecomment-5475539450) **IsaacOscar** described use cases for returning abstract mixins with custom names and for passing abstract classes to functions that modify them, provided TypeScript and JavaScript code examples, and shared a solution using Object.defineProperty to set class names

### [Issue microsoft/TypeScript#63129](https://github.com/microsoft/TypeScript/issues/63129) (Open, `Suggestion`, `Awaiting More Feedback`)

**TSC should not error on valid subpath specifier syntax \(TS2877\)**

*TypeScript 5.7 erroneously rejects valid non-relative subpath imports with '.ts' extensions by raising TS2877 errors.*

 * [28 weeks ago](https://github.com/microsoft/TypeScript/issues/63129#issuecomment-3899713546) **valler** said "Edit: no longer relevant. the best workaround so far follows in a later comment."
 * [28 weeks ago](https://github.com/microsoft/TypeScript/issues/63129#issuecomment-3900495979) **valler** said "Edit: no longer relevant. the best workaround so far follows in a later comment."
 * [7 weeks ago](https://github.com/microsoft/TypeScript/issues/63129#issuecomment-4928703170) **valler** described a workaround using an explicit .ts mapping to allow specifiers to end in .ts
 * [today](https://github.com/microsoft/TypeScript/issues/63129#issuecomment-5469869473) **rossipedia** resurrected the issue, argued the solution didn't handle mixed-extension scenarios, suggested suppressing the error when noEmit is true, and proposed separate .ts and .tsx path mappings

### [PR microsoft/TypeScript#63919](https://github.com/microsoft/TypeScript/pull/63919) (Open, `For Uncommitted Bug`)

**Add Yarn PnP module resolution support**

*Add native Yarn Plug’n’Play module resolution support to TypeScript Go, including PnP VFS, API, and manifest handling.*

 * created by **GGomez99**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63919#issuecomment-5471741188) **typescript-automation[bot]** said "The TypeScript team hasn't accepted the linked issue #63769. If you can get it accepted, this PR will have a better chance of being reviewed."

### [PR microsoft/TypeScript#63986](https://github.com/microsoft/TypeScript/pull/63986) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Don't reuse emit resolvers cross\-file**

*Reusing emit resolvers across files leads to race conditions that alter declaration emit outputs.*

 * [6 days ago](https://github.com/microsoft/TypeScript/pull/63986#issuecomment-5400350577) **DanielRosenwasser** said "Also, is it worth running a perf test on here just to be safe?"
 * [6 days ago](https://github.com/microsoft/TypeScript/pull/63986#issuecomment-5400888385) **jakebailey** said "Another hit on main: https://github.com/microsoft/TypeScript/actions/runs/32760252400/job/97537150724"
 * [6 days ago](https://github.com/microsoft/TypeScript/pull/63986#issuecomment-5400897261) **jakebailey** acknowledged that it allocated two closures per call, clarified it was only once per file and not a hotspot, and suggested refactoring
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#63987](https://github.com/microsoft/TypeScript/pull/63987) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Redo localization for onboarding**

*Reorganize localization files by dropping .json.gz and reintroducing loc directory; add VS Code localization; use build tag to exclude localization.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#63989](https://github.com/microsoft/TypeScript/pull/63989) (Open, `For Uncommitted Bug`, **RyanCavanaugh**, **Copilot**)

**Fix panic in declaration emit for \`export default\` arrow/function expression with unnameable inferred return type**

*Default-exported arrow or function expressions with unnameable inferred return types cause a compiler panic due to missing diagnostic context.*

 * (6 days ago) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * [6 days ago](https://github.com/microsoft/TypeScript/pull/63989#issuecomment-5401122264) **Copilot** implemented the change by moving the diagnostic context assignment and PushErrorFallbackNode above the unwrapped assignment, sharing them across all branches, and adding a PopErrorFallbackNode before each return
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [PR microsoft/TypeScript#63996](https://github.com/microsoft/TypeScript/pull/63996) (Closed, `For Backlog Bug`)

**Fix scanning issues related to Unicode escapes in RegExp group names and refactor identifier scanning**

*Refactor identifier scanning to correctly parse and normalize Unicode escapes and surrogate pairs in RegExp group names, preventing TS1514 errors.*

 * [4 days ago](https://github.com/microsoft/TypeScript/pull/63996#issuecomment-5432498806) **typescript-automation[bot]** reported that performance test jobs started and provided links to build and results
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/63996#issuecomment-5432686256) **typescript-automation[bot]** provided the results of the requested performance run
 * (2 days ago) **jakebailey** closed the issue
 * **typescript-automation[bot]** added label `For Backlog Bug`

### [PR microsoft/TypeScript#63999](https://github.com/microsoft/TypeScript/pull/63999) (Open, `For Backlog Bug`)

**Don't ignore all generic self tail calls when collecting the return type of a function**

*Include recursive generic tail calls with incompatible arguments in return type inference while ignoring only calls with explicit type arguments.*

 * [5 days ago](https://github.com/microsoft/TypeScript/pull/63999#issuecomment-5414382815) **typescript-automation[bot]** posted the requested performance run results
 * [5 days ago](https://github.com/microsoft/TypeScript/pull/63999#issuecomment-5414789604) **typescript-automation[bot]** reported that running the top 400 repos with tsc comparing main and the pull request merge yielded good results
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/63999#issuecomment-5423141982) **Andarist** described that recursive self-tail calls could not add new branches to the return type and thus the return type simplifies to Base
 * **typescript-automation[bot]** added label `For Backlog Bug`

### [PR microsoft/TypeScript#64000](https://github.com/microsoft/TypeScript/pull/64000) (Open, `For Uncommitted Bug`)

**Expose Checker\.getAwaitedType on the unstable API**

*Expose getAwaitedType on the TypeScript unstable API to allow consumers to recursively obtain the resolved type of awaited expressions.*

 * created by **baptistejamin**
 * [5 days ago](https://github.com/microsoft/TypeScript/pull/64000#issuecomment-5410558963) **baptistejamin** agreed with microsoft-github-policy-service
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64000#issuecomment-5471846926) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."

### [PR microsoft/TypeScript#64001](https://github.com/microsoft/TypeScript/pull/64001) (Open, `For Uncommitted Bug`)

**Expose Checker\.getTypeOfPropertyOfType on the unstable API**

*Expose Checker.getTypeOfPropertyOfType through the TypeScript unstable API to return a named property’s type or undefined.*

 * created by **baptistejamin**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64001#issuecomment-5471847120) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."

### [PR microsoft/TypeScript#64002](https://github.com/microsoft/TypeScript/pull/64002) (Open, `For Uncommitted Bug`)

**Expose Checker\.getIndexInfoOfType on the unstable API**

*Expose Checker.getIndexInfoOfType in TypeScript’s unstable API to mirror the Go checker and enable typescript-eslint’s isTypeReadonly functionality.*

 * created by **baptistejamin**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64002#issuecomment-5471847349) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."

### [PR microsoft/TypeScript#64014](https://github.com/microsoft/TypeScript/pull/64014) (Open, `Author: Team`, `For Backlog Bug`, **RyanCavanaugh**)

**Matching Strada order of operations in recursive signature resolution**

*Ensure the Go checker returns the cached source-order signature during recursive generic call resolution to prevent incorrect type inference.*

 * created by **RyanCavanaugh**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Backlog Bug`, and assigned to **RyanCavanaugh**

### [PR microsoft/TypeScript#64017](https://github.com/microsoft/TypeScript/pull/64017) (Open, `For Uncommitted Bug`, **weswigham**)

**Fix crash when a call signature's type parameter cannot be reused**

*Missing nil check in call signature type parameter reuse causes crash during incremental declaration file emission.*

 * created by **nikeedw**
 * (today) **typescript-automation[bot]** added label `For Uncommitted Bug`, and assigned to **weswigham**

### [PR microsoft/TypeScript#64019](https://github.com/microsoft/TypeScript/pull/64019) (Open, `For Uncommitted Bug`, **RyanCavanaugh**, **Copilot**)

**Use workspace tsdk settings without an additional prompt**

*Automatically apply workspace-configured TypeScript SDKs in trusted workspaces without extra prompts while preserving security for untrusted workspaces.*

 * created by **Copilot**
 * (5 days ago) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [PR microsoft/TypeScript#64026](https://github.com/microsoft/TypeScript/pull/64026) (Closed, `For Uncommitted Bug`, **jakebailey**, **Copilot**)

**Clear stale incremental diagnostics after JSON module changes**

*Use JSON file content version as its shape signature to invalidate stale incremental diagnostics after JSON module changes.*

 * created by **Copilot**
 * (5 days ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [PR microsoft/TypeScript#64027](https://github.com/microsoft/TypeScript/pull/64027) (Closed, `For Uncommitted Bug`)

**Escape unique\-symbol names in TS4094 diagnostics**

*Properly escape internal unique-symbol names in TS4094 diagnostics to use Strada’s __@brand@1 format instead of raw sentinel characters.*

 * created by **javascript-unsafe**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64027#issuecomment-5471743973) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."

### [Issue microsoft/TypeScript#64029](https://github.com/microsoft/TypeScript/issues/64029) (Closed, `Bug`, **andrewbranch**, **RyanCavanaugh**, **Copilot**)

**Auto\-import ignores barrel \(index\.ts\) when the imported folder name is a prefix of the importing file name**

*VSCode auto-import suggestions ignore barrel index.ts files when the imported folder name prefixes the importing file name.*

 * [4 days ago](https://github.com/microsoft/TypeScript/issues/64029#issuecomment-5430781986) **RyanCavanaugh** argued that import resolution issues stem from differing filename conventions rather than mixed behavior and that no universal barrel preference exists
 * **RyanCavanaugh** removed from milestone `TypeScript 7.1`
 * [4 days ago](https://github.com/microsoft/TypeScript/issues/64029#issuecomment-5431091407) **alexicum** asked why the auto-import suggestion differed between two files and what part of the algorithm causes the difference
 * (later) **RyanCavanaugh** added label `Bug`, removed label `Needs More Info`, and assigned to **andrewbranch**
 * [later](https://github.com/microsoft/TypeScript/issues/64029#issuecomment-5480804959) **RyanCavanaugh** confirmed a bug in tsgo’s circular-import avoidance heuristic and explained that the string-prefix check lacked a path-segment boundary, causing the sum barrel to be incorrectly penalized
 * (later) **RyanCavanaugh** assigned to **Copilot**, **RyanCavanaugh**

### [PR microsoft/TypeScript#64030](https://github.com/microsoft/TypeScript/pull/64030) (Open, `For Milestone Bug`, **RyanCavanaugh**, **Copilot**)

**\[WIP\] Fix TS5097 error for require\(\) in checked JS**

*Restore TS5097 errors for require() calls and side-effect .ts imports in checked JavaScript after TypeScript regression*

 * created by **Copilot**
 * (4 days ago) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * **typescript-automation[bot]** added label `For Milestone Bug`

### [PR microsoft/TypeScript#64031](https://github.com/microsoft/TypeScript/pull/64031) (Closed, `For Uncommitted Bug`, **RyanCavanaugh**, **Copilot**)

**\[WIP\] Fix auto\-import ignoring barrel files with prefix names**

*TypeScript auto-import suggestions omit barrel (index.ts) paths when directory names prefix the importing file’s name.*

 * created by **Copilot**
 * (4 days ago) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (later) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#64035](https://github.com/microsoft/TypeScript/pull/64035) (Open, `For Uncommitted Bug`, **RyanCavanaugh**, **Copilot**)

**Prefer index barrels for relative auto\-imports**

*Update TypeScript auto-import ranking to prefer index.ts barrel re-exports over direct files for relative modules.*

 * created by **Copilot**
 * (4 days ago) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [PR microsoft/TypeScript#64040](https://github.com/microsoft/TypeScript/pull/64040) (Open, `For Uncommitted Bug`)

**Replace Node interface with discriminated unions **

*Replace the Node interface with discriminated union types for improved type safety.*

 * created by **ArnaudBarre**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64040#issuecomment-5471848926) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [later](https://github.com/microsoft/TypeScript/pull/64040#issuecomment-5474929267) **typescript-automation[bot]** said "The TypeScript team hasn't accepted the linked issue #56275. If you can get it accepted, this PR will have a better chance of being reviewed."

### [PR microsoft/TypeScript#64042](https://github.com/microsoft/TypeScript/pull/64042) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**Content mapper auto import formatting panic**

*Reusing synthesized nodes during content mapping caused formatting crashes, fixed by cloning nodes and refactoring the change tracker.*

 * created by **andrewbranch**
 * (3 days ago) **andrewbranch** closed the issue
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **andrewbranch**

### [PR microsoft/TypeScript#64043](https://github.com/microsoft/TypeScript/pull/64043) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Align object binding defaults with arrays**

*Implement consistent default value handling in object destructuring to match array bindings*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#64044](https://github.com/microsoft/TypeScript/pull/64044) (Open, `Author: Team`, `For Milestone Bug`, **jakebailey**)

**Speed up narrowing of literal unions**

*Optimizes narrowing of literal unions, cutting user CPU time from around 11 seconds to under 0.1 second.*

 * [2 days ago](https://github.com/microsoft/TypeScript/pull/64044#issuecomment-5454719239) **jakebailey** said "@typescript-bot perf test this faster"
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/64044#issuecomment-5454720193) **typescript-automation[bot]** posted an update indicating that CI jobs started and linking to status and results
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/64044#issuecomment-5454974119) **typescript-automation[bot]** provided the requested performance run results with a comparison report
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Milestone Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#64046](https://github.com/microsoft/TypeScript/pull/64046) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Flip files from CRLF to LF**

*Convert all repository files except testdata and locale directories to LF line endings for consistency.*

 * created by **jakebailey**
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/64046#issuecomment-5443173686) **jakebailey** said "Nope, gitattributes does it all"
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/64046#issuecomment-5446342051) **jakebailey** reported that gitattributes didn't auto-fix locally created CRLF files and suggested adopting a VS Code setting or adding a task to flip line endings
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#64052](https://github.com/microsoft/TypeScript/pull/64052) (Open, `For Milestone Bug`)

**Fix false positive TS8030 for JSDoc @type on optional interface methods**

*Strip undefined from JSDoc @type annotations on optional interface methods before signature resolution to prevent false TS8030 errors.*

 * created by **jyx-07**
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/64052#issuecomment-5438749711) **jyx-07** said "@microsoft-github-policy-service agree"
 * **typescript-automation[bot]** added label `For Milestone Bug`

### [Issue microsoft/TypeScript#64053](https://github.com/microsoft/TypeScript/issues/64053) (Open, `Needs Investigation`, **andrewbranch**)

**content\-mapper generates inconsistent declaration extensions, making management of package\.json\#exports hard / verbose**

*Content-mapper generates inconsistent declaration file extensions, complicating package.json exports configuration.*

 * [3 days ago](https://github.com/microsoft/TypeScript/issues/64053#issuecomment-5444911489) **andrewbranch** asked if other ecosystems shipped 1:1 compiled output like Ember
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/64053#issuecomment-5445124761) **NullVoxPopuli** mentioned that MDX faced the same problem and suggested that other ecosystems standardize publishing JS to npm to reduce transpilation work
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/64053#issuecomment-5449867169) **remcohaszing** described Ember's and MDX's content-mapped file compilation parallels and proposed TypeScript content mapper configuration to rewrite import extensions
 * [today](https://github.com/microsoft/TypeScript/issues/64053#issuecomment-5472589697) **typescript-automation[bot]** said "This issue has been marked as "Working as Intended" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-automation[bot]** closed the issue
 * [later](https://github.com/microsoft/TypeScript/issues/64053#issuecomment-5480074724) **NullVoxPopuli** said "@typescript-bot "no recent activity"? it was the weekend"
 * (later) **andrewbranch** added label `Needs Investigation`, removed label `Working as Intended`, and assigned to **andrewbranch**
 * (later) **andrewbranch** reopened the issue

### [PR microsoft/TypeScript#64054](https://github.com/microsoft/TypeScript/pull/64054) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Bump and clean up deps, raise min local node version**

*Bump and clean dependencies, raise minimum Node version to 22.18, and replace several packages with built-in features.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#64057](https://github.com/microsoft/TypeScript/pull/64057) (Open, `For Uncommitted Bug`, **ahejlsberg**, **Copilot**)

**Port \`\-\-enforceReadonly\` to the Go compiler**

*Port TypeScript’s --enforceReadonly feature to the Go compiler by adding the flag, updating CLI and diagnostics, and enforcing readonly constraints.*

 * created by **Copilot**
 * (3 days ago) **Copilot** assigned to **Copilot**, **ahejlsberg**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [PR microsoft/TypeScript#64061](https://github.com/microsoft/TypeScript/pull/64061) (Open, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Add pagination of batch requests**

*Implement server-side pagination of batch API responses using maxResponseBytesPerPage to prevent JavaScript string size overflows and simplify encoding.*

 * created by **weswigham**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **weswigham**

### [PR microsoft/TypeScript#64063](https://github.com/microsoft/TypeScript/pull/64063) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Ditch nodeData interface in favor of generated accessors**

*Replacing the dynamic nodeData interface with generated accessors reduces binary size, symbol count, and compile time.*

 * [2 days ago](https://github.com/microsoft/TypeScript/pull/64063#issuecomment-5456775834) **jakebailey** said "@typescript-bot perf test this faster"
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/64063#issuecomment-5456776643) **typescript-automation[bot]** reported that performance test jobs had started and linked to build status and results
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/64063#issuecomment-5457089086) **typescript-automation[bot]** posted the requested perf run results comparing baseline to PR
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#64064](https://github.com/microsoft/TypeScript/pull/64064) (Open, `For Backlog Bug`)

**Fix importHelpers incorrectly requiring tslib for native \#private class members \(\#63728\)**

*Remove unnecessary decorator-based gating so native private class members no longer require tslib for ES2022+ targets*

 * created by **YoussefMansour9**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64064#issuecomment-5471690881) **microsoft-github-policy-service[bot]** requested that the user agree to the Contributor License Agreement by replying with the specified command format

### [PR microsoft/TypeScript#64066](https://github.com/microsoft/TypeScript/pull/64066) (Closed, `For Uncommitted Bug`, **andrewbranch**)

**\[api\] Add \`TupleTypeReference\` interface**

*Add missing TupleTypeReference interface to the TypeScript API to support tuple type references.*

 * created by **mrazauskas**
 * (2 days ago) **andrewbranch** closed the issue
 * (today) **typescript-automation[bot]** added label `For Uncommitted Bug`, and assigned to **andrewbranch**

### [PR microsoft/TypeScript#64072](https://github.com/microsoft/TypeScript/pull/64072) (Open, `For Backlog Bug`)

**fix\(64058\): fix reparse jsdoc @extends type arguments for call expressions**

*Corrects the re-parsing of JSDoc @extends type arguments in call expressions.*

 * created by **a-tarasyuk**
 * (2 days ago) **a-tarasyuk** closed the issue
 * (2 days ago) **a-tarasyuk** reopened the issue
 * **typescript-automation[bot]** added label `For Backlog Bug`

### [Issue microsoft/TypeScript#64073](https://github.com/microsoft/TypeScript/issues/64073) (Closed, `Duplicate`)

**The extends infer for function generics fails\.**

*TypeScript fails to infer conditional extends checks on generic function parameters, causing incorrect type assignments.*

 * created by **vipcxj**
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/64073#issuecomment-5451809803) **MartinJohns** explained that resolving conditional types with unbound generics is deferred and noted duplication of issue #23132
 * **RyanCavanaugh** added label `Duplicate`
 * [today](https://github.com/microsoft/TypeScript/issues/64073#issuecomment-5472589411) **typescript-automation[bot]** said "This issue has been marked as "Duplicate" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-automation[bot]** closed the issue

### [PR microsoft/TypeScript#64074](https://github.com/microsoft/TypeScript/pull/64074) (Open, `For Backlog Bug`)

**Disallow optional calls on import\.defer**

*Introduce parse errors for optional calls on import.defer, including import.defer?.(...) and generic import.defer?.<T>(...), while preserving valid import.defer(...) calls.*

 * created by **HyeonsangKim**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64074#issuecomment-5471743238) **microsoft-github-policy-service[bot]** requested that the contributor read and agree to the CLA by replying with the specified command

### [PR microsoft/TypeScript#64077](https://github.com/microsoft/TypeScript/pull/64077) (Open, `For Backlog Bug`)

**Fixed signature caching issue caused by reentrant signature checking**

*Ports a prior fix and adds an extra commit to resolve reentrant signature caching issues without regressions.*

 * created by **Andarist**
 * **typescript-automation[bot]** added label `For Backlog Bug`

### [PR microsoft/TypeScript#64078](https://github.com/microsoft/TypeScript/pull/64078) (Closed, `For Uncommitted Bug`, **andrewbranch**, **Copilot**)

**Complete the CompilerOptions API surface**

*Expose previously unexported JsxEmit and ModuleResolutionKind enums and include deprecated compatibility options esModuleInterop and allowSyntheticDefaultImports in the CompilerOptions API.*

 * [2 days ago](https://github.com/microsoft/TypeScript/pull/64078#issuecomment-5455947332) **andrewbranch** said "@copilot do not generate deprecated enums. Delete the meaningless tests. Ensure codegen guarantees completeness or a test asserts completeness of generated enums."
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/64078#issuecomment-5456195330) **Copilot** addressed deprecated enum generation and removed API/value tests in commit 561b2d6a, restored deprecated-field filtering with explicit API opt-ins, and updated codegen to automatically export all referenced enums
 * (2 days ago) **andrewbranch** closed the issue
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [PR microsoft/TypeScript#64079](https://github.com/microsoft/TypeScript/pull/64079) (Closed, `For Uncommitted Bug`, **andrewbranch**, **Copilot**)

**Validate DocumentIdentifier arguments in API**

*Add validation for DocumentIdentifier arguments across APIs to report malformed inputs with clear error messages.*

 * (2 days ago) **Copilot** assigned to **Copilot**, **andrewbranch**
 * (2 days ago) **andrewbranch** closed the issue
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [PR microsoft/TypeScript#64080](https://github.com/microsoft/TypeScript/pull/64080) (Closed, `Author: Team`, `For Milestone Bug`, **andrewbranch**)

**\[api\] Fix crash accessing tuple type reference data**

*Updates the TypeScript API to prevent crashes when accessing tuple type references by refining type guards and getTarget behavior.*

 * [2 days ago](https://github.com/microsoft/TypeScript/pull/64080#issuecomment-5456046138) **ahejlsberg** noted that the meaning of `isTupleType` differed between the checker and exposed API and asked what the API’s `isTupleType` does
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/64080#issuecomment-5456093712) **ahejlsberg** explained that synthesized tuple base class instances serve as type references to themselves, having both ObjectFlagsTuple and ObjectFlagsReference set, similar to regular class and interface types
 * (2 days ago) **andrewbranch** closed the issue
 * (today) **typescript-automation[bot]** added labels `For Milestone Bug`, `Author: Team`, and assigned to **andrewbranch**

### [PR microsoft/TypeScript#64081](https://github.com/microsoft/TypeScript/pull/64081) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Make tsconfig move lifetime test deterministic**

*Make the tsconfig move lifetime test tolerate deferred inferred project cleanup to prevent race conditions*

 * created by **jakebailey**
 * (2 days ago) **jakebailey** closed the issue
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#64082](https://github.com/microsoft/TypeScript/pull/64082) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Verify \`go test\` works without node installed**

*Ensure tests and benchmarks run using only Go without requiring Node or the tsc module*

 * created by **jakebailey**
 * (2 days ago) **jakebailey** closed the issue
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#64083](https://github.com/microsoft/TypeScript/pull/64083) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**Fix SymbolFlags\.All value by parsing operator precedence when generating TS enums from Go enums**

*The PR fixes the SymbolFlags.All value by enforcing proper operator precedence in Go-to-TypeScript enum generation.*

 * created by **andrewbranch**
 * (2 days ago) **andrewbranch** closed the issue
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **andrewbranch**

### [PR microsoft/TypeScript#64084](https://github.com/microsoft/TypeScript/pull/64084) (Closed, `For Backlog Bug`)

**Add diagnostic for private identifiers in destructuring patterns**

*Add diagnostic preventing use of private identifiers in destructuring patterns.*

 * created by **youngspe**
 * **typescript-automation[bot]** added label `For Backlog Bug`

### [PR microsoft/TypeScript#64085](https://github.com/microsoft/TypeScript/pull/64085) (Open, `Author: Team`, `For Milestone Bug`, **jakebailey**)

**Handle tsc watch and profiling signals**

*Implement proper signal handling in the TypeScript compiler’s watch and profiling modes to enable graceful shutdown.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Milestone Bug`, and assigned to **jakebailey**

### [Issue microsoft/TypeScript#64087](https://github.com/microsoft/TypeScript/issues/64087) (Open, `Suggestion`)

**Switching on a template literal expression does not narrow the interpolated union variable**

*Switching on a template literal expression (`${foo} pie`) fails to narrow the union variable foo in case clauses.*

 * created by **nick-grain**
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/64087#issuecomment-5458834867) **RyanCavanaugh** said "Why would you write this code this way?"
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/64087#issuecomment-5458953379) **nick-grain** provided a minimal reproducible example of their code
 * **RyanCavanaugh** added label `Suggestion`

### [PR microsoft/TypeScript#64088](https://github.com/microsoft/TypeScript/pull/64088) (Open, `For Uncommitted Bug`, **DanielRosenwasser**, **Copilot**)

**Restore go\-to\-definition for triple\-slash lib references**

*Restore go-to-definition for triple-slash lib references in TypeScript by resolving and indexing referenced libraries.*

 * created by **Copilot**
 * (2 days ago) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [Issue microsoft/TypeScript#64090](https://github.com/microsoft/TypeScript/issues/64090) (Closed, `Working as Intended`)

**transpileModule/transpileDeclaration silently canonicalize fileName and echo the canonical form in diagnostics — undocumented**

*transpileModule and transpileDeclaration silently canonicalize fileName inputs and echo the undocumented normalized path in diagnostics.*

 * created by **johnnyreilly**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/64090#issuecomment-5462454009) **kritharth2005** asked if anyone was working on the issue and offered to investigate and propose a fix
 * **andrewbranch** added label `Working as Intended`

### [PR microsoft/TypeScript#64092](https://github.com/microsoft/TypeScript/pull/64092) (Open, `For Uncommitted Bug`)

**Experiment: Dependent contextual inference**

*Provides an initial prototype implementation of dependent contextual inference for experimental evaluation.*

 * created by **devanshj**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [PR microsoft/TypeScript#64093](https://github.com/microsoft/TypeScript/pull/64093) (Open, `For Milestone Bug`)

**feat: add Promise\.allKeyed and Promise\.allSettledKeyed to esnext**

*Add Promise.allKeyed and Promise.allSettledKeyed methods to the ESNext Promise API.*

 * created by **a-tarasyuk**
 * **typescript-automation[bot]** added label `For Milestone Bug`

### [PR microsoft/TypeScript#64095](https://github.com/microsoft/TypeScript/pull/64095) (Open, `For Milestone Bug`)

**feat: add iterator methods to esnext**

*Add iterator methods to ESNext type definitions to support iteration protocols.*

 * created by **a-tarasyuk**
 * **typescript-automation[bot]** added label `For Milestone Bug`

### [PR microsoft/TypeScript#64096](https://github.com/microsoft/TypeScript/pull/64096) (Open, `For Milestone Bug`, **DanielRosenwasser**)

**feat: add es2026 as a valid target and lib**

*Add ES2026 as a recognized compilation target and library option in TypeScript.*

 * created by **a-tarasyuk**
 * (today) **typescript-automation[bot]** added label `For Milestone Bug`, and assigned to **DanielRosenwasser**

### [Issue microsoft/TypeScript#64097](https://github.com/microsoft/TypeScript/issues/64097) (Open, `Bug`, **RyanCavanaugh**, **Copilot**)

**On TypeScript 7, Call hierarchy shows a full absolute path instead of file name \+ relative path**

*TypeScript 7 native-preview’s call hierarchy feature incorrectly displays full absolute file paths instead of file names with relative paths.*

 * created by **brian-xu-vlt**
 * [today](https://github.com/microsoft/TypeScript/issues/64097#issuecomment-5470912738) **Shivang9983** offered to take up the issue, analyzed the regression in TS7 LSP response formatting, proposed a fix plan, and asked to be assigned

### [Issue microsoft/TypeScript#64098](https://github.com/microsoft/TypeScript/issues/64098) (Open)

**tsconfig \`include\` silently drops \`Foo\.tsx\` when \`foo\.ts\` exists, on a case\-insensitive filesystem**

*TypeScript’s tsconfig include option silently ignores .tsx files on case-insensitive filesystems when a same-named .ts file exists, preventing diagnostics.*

 * created by **jomonkj**
 * [today](https://github.com/microsoft/TypeScript/issues/64098#issuecomment-5470908358) **Shivang9983** offered to work on the issue, described root cause and proposed fix, and requested assignment

### [PR microsoft/TypeScript#64099](https://github.com/microsoft/TypeScript/pull/64099) (Closed, `For Backlog Bug`)

**fix\(62179\): report non\-string\-literal values in import type attributes**

*Add diagnostics to report non-string-literal values in import type attributes.*

 * created by **a-tarasyuk**
 * **typescript-automation[bot]** added label `For Backlog Bug`

### [PR microsoft/TypeScript#64100](https://github.com/microsoft/TypeScript/pull/64100) (Open, `For Backlog Bug`)

**Fixed an issue with mapped property symbol not displaying added \`\| undefined\` when its origin symbol was optional**

*Mapped property symbols now correctly include ‘| undefined’ when their originating symbols are optional.*

 * created by **Andarist**
 * **typescript-automation[bot]** added label `For Backlog Bug`

### [PR microsoft/TypeScript#64101](https://github.com/microsoft/TypeScript/pull/64101) (Closed, `For Uncommitted Bug`)

**fix: propagate private modifiers in implement interface code fix \(\#37782\)**

*Extend the implement interface code fix to detect and apply private modifiers when generating missing class members.*

 * created by **mcontributor**
 * [today](https://github.com/microsoft/TypeScript/pull/64101#issuecomment-5470845836) **mcontributor** said "@microsoft-github-policy-service agree"
 * (today) **mcontributor** closed the issue
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64101#issuecomment-5471809257) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."

### [Issue microsoft/TypeScript#64102](https://github.com/microsoft/TypeScript/issues/64102) (Open, `Suggestion`)

**Proposal: Expose LSP/Language Service capabilities \(e\.g\., rename\) via a tsc subcommand**

*Expose LSP refactoring features like rename through tsc subcommands for CLI tools*

 * created by **trim21**

### [PR microsoft/TypeScript#64103](https://github.com/microsoft/TypeScript/pull/64103) (Closed, `For Milestone Bug`)

**Emit 1/0 and 0/0 instead of Infinity/NaN in enum transforms**

*TypeScript now emits non-finite enum values as 1/0, -(1/0), or 0/0 rather than Infinity/NaN to prevent shadowing.*

 * created by **mturac**
 * **typescript-automation[bot]** added label `For Milestone Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/64103#issuecomment-5480608508) **RyanCavanaugh** identified a policy violation regarding bulk agent-driven contributions
 * (later) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#64104](https://github.com/microsoft/TypeScript/pull/64104) (Closed, `For Uncommitted Bug`, `dependencies`, `github_actions`)

**Bump the github\-actions group with 4 updates**

*Update the github-actions group by upgrading azure/login to v3.0.2 and bumping three CodeQL actions (init, analyze, upload-sarif).*

 * created by **dependabot[bot]**
 * (today) **dependabot[bot]** added labels `dependencies`, `github_actions`
 * (today) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`, `For Uncommitted Bug`

### [Issue microsoft/TypeScript#64105](https://github.com/microsoft/TypeScript/issues/64105) (Closed, `API Request`, **andrewbranch**, **Copilot**)

**\[API\] labeledElementDeclarations is missing in TypeScript 7**

*TypeScript 7’s compiler API no longer includes labeledElementDeclarations, preventing access to tuple element names.*

 * created by **Gerrit0**

### [PR microsoft/TypeScript#64106](https://github.com/microsoft/TypeScript/pull/64106) (Open, `For Backlog Bug`)

**fix\(58145\): suppress jsdoc for private members**

*Suppresses JSDoc comments for private members to prevent their documentation emission*

 * created by **a-tarasyuk**
 * **typescript-automation[bot]** added label `For Backlog Bug`

### [PR microsoft/TypeScript#64107](https://github.com/microsoft/TypeScript/pull/64107) (Closed, `For Uncommitted Bug`, **RyanCavanaugh**, **Copilot**)

**Fix auto\-import barrel ranking for path\-prefix collisions**

*Fix auto-import barrel ranking by requiring path-segment boundaries to avoid misidentifying directories as prefixes of file names.*

 * created by **Copilot**
 * (later) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

