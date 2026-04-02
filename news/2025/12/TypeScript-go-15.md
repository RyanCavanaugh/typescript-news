# Report for 2025-12-15 (Monday, December 15th, 2025)

11 different users commented on 23 different issues.

## Recommended Actions

 * Response Recommended
    * @besserwisser asked if there was a list of to-dos in [microsoft/TypeScript-go#2383](https://github.com/microsoft/TypeScript-go/issues/2383#issuecomment-3657264640)

## Activity Summary

### [Issue microsoft/TypeScript-go#1080](https://github.com/microsoft/TypeScript-go/issues/1080) (Open, `Domain: Program`)

**Deduplicate doubly\-installed packages**

*Duplicated installations of the same npm package across workspaces lead to instances TypeScript tolerates but break Go type compatibility.*

 * [6 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1080#issuecomment-3458576531) **jakebailey** referred to PR 62684 showing minimal breakage, described a potential implementation of a load plus dedupe pass, and expressed preference not to reintroduce the idea
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/1080#issuecomment-3644998431) **jakebailey** asked users to try building PR #2361 from source to see if it fixed their issues
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/1080#issuecomment-3650241893) **Benjamin-Dobell** reported that building PR #2361 did not fix the reproduction and provided the error output
 * [today](https://github.com/microsoft/TypeScript-go/issues/1080#issuecomment-3656907954) **jakebailey** acknowledged that their attempt couldn't resolve the symbols deduplication issue and that hacking the checker avoided some errors but didn't fix class nominality
 * [today](https://github.com/microsoft/TypeScript-go/issues/1080#issuecomment-3657175627) **jakebailey** said "@Benjamin-Dobell Can you try #2361 again? With the latest version, your example appears to work for me."
 * [today](https://github.com/microsoft/TypeScript-go/issues/1080#issuecomment-3658550958) **Benjamin-Dobell** confirmed that the example worked with the latest version and expressed appreciation, noting that typescript-go significantly benefits their large GodotJS-based TypeScript game project

### [PR microsoft/TypeScript-go#1556](https://github.com/microsoft/TypeScript-go/pull/1556) (Closed)

**fix: improve panic message for unspecified ScriptKind in \`Parser::initializeState\`**

*Enhance the panic message in Parser::initializeState to include the filename when ScriptKind is unknown for easier debugging*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/1556#issuecomment-3630516495) **jakebailey** said "Honestly, I think we can just take this; NewSourceFile already panics with a filename. I would just merge from main, however."
 * (yesterday) **jakebailey** closed the issue
 * (yesterday) **jakebailey** reopened the issue
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#1947](https://github.com/microsoft/TypeScript-go/pull/1947) (Open)

**fix: panic in \`regexp\.MustCompile\` when building wildcarddirectories with non ascii characters**

*Handle non-ASCII characters in wildcard directory patterns to prevent regexp.MustCompile panics.*

 * (yesterday) **jakebailey** closed the issue
 * (yesterday) **jakebailey** reopened the issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/1947#issuecomment-3655915844) **camc314** explained that getWildcardDirectories produced invalid regex escapes from Windows file paths containing non-ASCII characters, causing a panic, and noted that percent-encoded paths avoid the issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/1947#issuecomment-3656699559) **jakebailey** asked if decoding from URI format should occur before passing filesystem paths and inquired which code path allowed encoded paths through

### [PR microsoft/TypeScript-go#2257](https://github.com/microsoft/TypeScript-go/pull/2257) (Closed)

**fix\(2212\): make enum constant inlining consistent with Strada behavior**

*Adjust enum constant inlining implementation to match Strada behavior and resolve related inconsistencies.*

 * created by **a-tarasyuk**
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/2257#issuecomment-3628450472) **jakebailey** asked how much of the runtime changes were necessary to fix the linked issue and whether it was impossible to resolve
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/2257#issuecomment-3628561180) **a-tarasyuk** suggested replicating evaluateEntity logic from the checker to resolve the issue without the full GetEnumMemberValue dependency
 * (today) **a-tarasyuk** closed the issue

### [PR microsoft/TypeScript-go#2262](https://github.com/microsoft/TypeScript-go/pull/2262) (Closed)

**fix\(2260\): Inherited methods not merging JSDoc comments**

*Inherited methods fail to merge their JSDoc comments, resulting in missing inherited documentation.*

 * created by **a-tarasyuk**
 * (today) **a-tarasyuk** closed the issue

### [Issue microsoft/TypeScript-go#2284](https://github.com/microsoft/TypeScript-go/issues/2284) (Closed, `Crash`, **ahejlsberg**)

**Crash in \`getBaseTypes\`**

*The TypeScript Go internal checker panics with a nil pointer dereference in getBaseTypes during type checking.*

 * **ahejlsberg** assigned to **ahejlsberg**
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/2284#issuecomment-3649899671) **ahejlsberg** provided a short reproduction demonstrating the crash and announced plans to submit a PR to fix it
 * (yesterday) **ahejlsberg** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/issues/2284#issuecomment-3656798595) **DorianListens** said "Happy to confirm that as of 7.0.0-dev.20251215.1 we're no longer seeing this crash. Thanks y'all!"

### [PR microsoft/TypeScript-go#2288](https://github.com/microsoft/TypeScript-go/pull/2288) (Open)

**Use xxhash for composite checker keys instead of strings**

*Switch from string-based map keys to 128-bit xxhash keys to improve memory efficiency in Go composite type checking.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2288#issuecomment-3658195657) **ahejlsberg** said "In general, in places where we now write a fixed number of bytes (e.g. four bytes for a type ID), we don't need separators between multiple consecutive IDs."

### [Issue microsoft/TypeScript-go#2349](https://github.com/microsoft/TypeScript-go/issues/2349) (Closed, `Domain: Editor`, **ahejlsberg**)

**Support JSDoc \`\<caption\>\` tags for IntelliSense**

*Add support for multiline JSDoc <caption> tags in IntelliSense to match single-line behavior.*

 * created by **mjbvz**
 * (3 days ago) **jakebailey** added label `Domain: Editor`, and assigned to **ahejlsberg**
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#2366](https://github.com/microsoft/TypeScript-go/issues/2366) (Open)

**Diagnostics not shown in file peek views**

*Reference peek views in TypeScript no longer display diagnostics such as deprecation warnings across files.*

 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/2366#issuecomment-3648014391) **mjbvz** said "Yes maybe an lsp issue? cc @dbaeumer "
 * [today](https://github.com/microsoft/TypeScript-go/issues/2366#issuecomment-3654930647) **dbaeumer** assumed the new TS extension used pull diagnostics, noted that VS Code did not represent peek view editors in the tab model, and asked if there was a way to detect peek editor tabs
 * [today](https://github.com/microsoft/TypeScript-go/issues/2366#issuecomment-3655002832) **jakebailey** stated that they currently exclusively used pull diagnostic as tsserver did before and suggested that the TS extension’s error requests may have already solved the issue
 * [today](https://github.com/microsoft/TypeScript-go/issues/2366#issuecomment-3656646368) **lramos15** expressed uncertainty about detecting peek editor tabs and suggested using the text document API instead of the tabs API
 * [today](https://github.com/microsoft/TypeScript-go/issues/2366#issuecomment-3657052572) **bpasero** said "@jrieken might have guidance"
 * [later](https://github.com/microsoft/TypeScript-go/issues/2366#issuecomment-3659745686) **jrieken** said "Peek editors aren't tab-editors and I think the visible editors route needs to be taken here."

### [PR microsoft/TypeScript-go#2373](https://github.com/microsoft/TypeScript-go/pull/2373) (Open)

**Switch dprint to new gofumpt Wasm plugin**

*Adopt the new gofumpt Wasm plugin in dprint to improve formatting performance by over 67× and fix Windows reliability issues.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2373#issuecomment-3657967572) **jakebailey** said "Drafting for now until the next version, there are some fixes there I will want to pull in."

### [PR microsoft/TypeScript-go#2374](https://github.com/microsoft/TypeScript-go/pull/2374) (Closed)

**Support \`\<caption\>\</caption\>\` in JSDoc \`@example\` tags**

*Enable support for <caption> tags inside JSDoc @example blocks.*

 * created by **ahejlsberg**
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#2378](https://github.com/microsoft/TypeScript-go/pull/2378) (Closed, **DanielRosenwasser**, **Copilot**)

**Fix crashes in decorators transform compiling VS Code**

*Fixes two crashes in decorators transform caused by missing nil checks and incorrect modifier indexing, adds tests and updates baselines.*

 * created by **Copilot**
 * (yesterday) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * (today) **DanielRosenwasser** closed the issue

### [Issue microsoft/TypeScript-go#2380](https://github.com/microsoft/TypeScript-go/issues/2380) (Open)

**Explosion in emit time on VS Code**

*Removing the --noEmit flag in VS Code’s TypeScript compilation causes the emit phase to jump to 74 seconds.*

 * created by **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2380#issuecomment-3658416211) **jakebailey** described swapping the emit resolver to getResolvedSymbolOrNil which passes tests and provided benchmark results

### [Issue microsoft/TypeScript-go#2383](https://github.com/microsoft/TypeScript-go/issues/2383) (Open, **andrewbranch**, **gabritto**)

**LSP: Path suggestion missing \(import/export\)**

*Path completion suggestions for import/export statements are missing in tsgo, unlike in TypeScript 5.9.*

 * created by **besserwisser**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2383#issuecomment-3655514582) **dalisoft** said "Maybe related to https://github.com/microsoft/typescript-go/issues/2189"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2383#issuecomment-3655614357) **besserwisser** thanked and stated uncertainty about whether auto import equates to file path completion in insert mode
 * [today](https://github.com/microsoft/TypeScript-go/issues/2383#issuecomment-3656759441) **andrewbranch** said "Module path completions are a known to-do."
 * (today) **andrewbranch** assigned to **andrewbranch**, **gabritto**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2383#issuecomment-3657264640) **besserwisser** asked if there was a list of to-dos
 * [today](https://github.com/microsoft/TypeScript-go/issues/2383#issuecomment-3657318588) **andrewbranch** said "Yes and no; we have a list of failing/differing tests, and I traced these to a function that was empty except for a code comment."

### [PR microsoft/TypeScript-go#2385](https://github.com/microsoft/TypeScript-go/pull/2385) (Closed, `dependencies`, `github_actions`)

**Bump the github\-actions group across 2 directories with 4 updates**

*Update GitHub Actions dependencies: bump codecov-action, upload-artifact, and codeql-action in the root and actions/cache in the setup-go directory.*

 * (today) **dependabot[bot]** added labels `github_actions`, `dependencies`, `github_actions`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2387](https://github.com/microsoft/TypeScript-go/issues/2387) (Open)

**Diagnostics don't refresh after file rename**

*After renaming a file, TypeScript diagnostics sometimes fail to update until the server is reloaded.*

 * created by **mjbvz**

### [Issue microsoft/TypeScript-go#2388](https://github.com/microsoft/TypeScript-go/issues/2388) (Open, `Crash`)

**Request textDocument/codeLens failed\. Message: InternalError: panic handling request textDocument/codeLens: runtime error: invalid memory**

*The TypeScript-Go language server panics due to a nil pointer dereference when handling textDocument/codeLens requests in VS Code.*

 * created by **mjbvz**
 * **mjbvz** added label `Crash`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2388#issuecomment-3657654809) **mjbvz** said "Seeing similar issues for a lot of other requests too, such as diagnostics "

### [PR microsoft/TypeScript-go#2389](https://github.com/microsoft/TypeScript-go/pull/2389) (Open)

**Multiple fixes to JSDoc display in quick info and signature help**

*Enable display of JSDoc comments from @param, @callback, @overload, @typedef, and @property tags in quick info and signature help.*

 * created by **ahejlsberg**

### [PR microsoft/TypeScript-go#2390](https://github.com/microsoft/TypeScript-go/pull/2390) (Open)

**New auto\-import infrastructure**

*Redesigned auto-import collection and caching infrastructure in the Corsa port now supports snapshot-based LSP, improved parallelization, and retains existing fix generation logic.*

 * created by **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2390#issuecomment-3658351037) **jakebailey** mentioned that removing devDependencies from search would prevent auto imports in build scripts or tests

### [Issue microsoft/TypeScript-go#2391](https://github.com/microsoft/TypeScript-go/issues/2391) (Open)

**can support vue?**

*Request for Vue.js support and configuration guidance to replicate the tool’s React project performance.*

 * created by **DankeBIBI**

### [Issue microsoft/TypeScript-go#2392](https://github.com/microsoft/TypeScript-go/issues/2392) (Open)

**can support vue?**

*Request for Vue.js support and configuration guidance to replicate the tool’s React project performance.*

 * created by **DankeBIBI**

