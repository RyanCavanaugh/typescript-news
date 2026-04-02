# Report for 2026-03-16 (Monday, March 16th, 2026)

13 different users commented on 42 different issues.

## Recommended Actions

 * Response Recommended
    * @anchmelev requested a review on their PR for LSP import updates in [microsoft/TypeScript-go#3084](https://github.com/microsoft/TypeScript-go/pull/3084#issuecomment-4069834603)

## Activity Summary

### [PR microsoft/TypeScript-go#2107](https://github.com/microsoft/TypeScript-go/pull/2107) (Closed)

**Suggested changes to \#2026 \(Implement RegExp literal syntax checking\)**

*Suggests changes to enhance RegExp literal syntax checking in the jabaile/regexp-errors branch as a supplement to PR #2026.*

 * created by **graphemecluster**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2107#issuecomment-4072377458) **graphemecluster** said "Closing since #3061 is merged."
 * (today) **graphemecluster** closed the issue

### [Issue microsoft/TypeScript-go#2212](https://github.com/microsoft/TypeScript-go/issues/2212) (Closed, `Domain: Emit`, **jakebailey**)

**Incorrect import elision when enum value references another enum from a different module**

*tsgo wrongly elides imports when an enum references values from another module's enum, causing undefined runtime errors.*

 * [14 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2212#issuecomment-3617384891) **jakebailey** explained that enums were initially handled without const inlining but recommended restoring the previous behavior
 * (1 week ago) **jakebailey** added label `Domain: Emit`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2229](https://github.com/microsoft/TypeScript-go/issues/2229) (Closed, `Domain: Editor`, **jakebailey**, **Copilot**)

**Should not allow renaming keywords**

*TS-go erroneously permits renaming on keywords and parentheses instead of failing early via prepareRename*

 * (1 week ago) **jakebailey** assigned to **Copilot**, **jakebailey**, and unassigned **Copilot**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2230](https://github.com/microsoft/TypeScript-go/issues/2230) (Closed, `Domain: Editor`)

**Should not allow renaming parts of the standard library**

*Prevent users from renaming built-in standard library functions like setTimeout.*

 * (14 weeks ago) **jakebailey** added label `Domain: Editor`, assigned to **Copilot**, and unassigned **Copilot**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2506](https://github.com/microsoft/TypeScript-go/issues/2506) (Closed, `Domain: Editor`, **andrewbranch**)

**Stale module resolution error after linking pnpm workspace dependency due to watcher configuration/handling**

*VS Code’s watcher ignoring directory-level symlink events outside its file-extension glob causes stale module resolution errors after pnpm workspace linking.*

 * **andrewbranch** added label `Domain: Editor`
 * (7 weeks ago) **andrewbranch** closed the issue
 * (7 weeks ago) **andrewbranch** reopened the issue
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#2686](https://github.com/microsoft/TypeScript-go/issues/2686) (Open, `Domain: Editor`, **andrewbranch**)

**Packages \`pnpm link\`ed from outside the workspace trigger no watch events when changed**

*Linked external packages don’t trigger watch events on changes, preventing diagnostic updates until the server restarts.*

 * **andrewbranch** added label `Domain: Editor`
 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2686#issuecomment-3850202915) **sheetalkamat** described how Strada watched `node_modules/package` for links and otherwise `node_modules` for failed lookups and linked the relevant pull request
 * **andrewbranch** assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2686#issuecomment-4069900531) **andrewbranch** said "Related: https://github.com/microsoft/vscode/issues/3025"

### [Issue microsoft/TypeScript-go#2993](https://github.com/microsoft/TypeScript-go/issues/2993) (Closed, `bug`, `Domain: Editor`, **andrewbranch**, **iisaduan**, **Copilot**)

**Auto import does not get its own line**

*Auto-importing readFileSync inserts its import on the same line as the previous import instead of a new line.*

 * **DanielRosenwasser** assigned to **iisaduan**
 * (3 days ago) **andrewbranch** assigned to **Copilot**, **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#3012](https://github.com/microsoft/TypeScript-go/issues/3012) (Open)

**\[ServerErrors\]\[TypeScript\] main vs **

*The main branch Azure pipeline reported clone failures, timeouts, and server errors during analysis of 300 TypeScript repositories, yielding 53 significant changes.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/3012#issuecomment-4015173777) **typescript-bot** reported a panic during textDocument/formatting due to a debug failure: False expression: Token end is child end
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/3012#issuecomment-4015173799) **typescript-bot** reported a panic handling textDocument/formatting request due to a debug failure: Token end is child end
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/3012#issuecomment-4015173817) **typescript-bot** reported a panic in textDocument/formatting due to a false expression 'Token end is child end' with a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/3012#issuecomment-4068851896) **gabritto** provided a table summarizing error messages, stack trace links, comment counts, affected repositories, and related pull requests

### [Issue microsoft/TypeScript-go#3025](https://github.com/microsoft/TypeScript-go/issues/3025) (Open)

**\[ServerErrors\]\[TypeScript\] main vs **

*An Azure Pipeline run on the TypeScript main branch encountered server errors and mixed results across 300 popular GitHub repositories.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/3025#issuecomment-4020210383) **typescript-bot** reported that the server connection closed prematurely with an undefined error for the colinhacks/zod repository
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/3025#issuecomment-4020210395) **typescript-bot** reported a server connection closing prematurely with undefined and provided affected repos and reproduction steps
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/3025#issuecomment-4020210407) **typescript-bot** reported a panic handling textDocument/rangeFormatting due to a debug failure
 * [today](https://github.com/microsoft/TypeScript-go/issues/3025#issuecomment-4068930190) **gabritto** listed five error messages with stack trace links, comment counts, and affected repositories

### [Issue microsoft/TypeScript-go#3044](https://github.com/microsoft/TypeScript-go/issues/3044) (Closed, `bug`, **RyanCavanaugh**, **Copilot**)

**Regex parsing/validation isn't implemented yet**

*tsgo does not report syntax errors in invalid regular expressions that TypeScript 6.0 catches due to missing regex parsing validation*

 * [6 days ago](https://github.com/microsoft/TypeScript-go/issues/3044#issuecomment-4032702691) **jakebailey** said "I'm pretty sure this is a part of the unported regex errors and can't be done individually."
 * [6 days ago](https://github.com/microsoft/TypeScript-go/issues/3044#issuecomment-4033032398) **Andarist** said "FWIW, I'm working on porting this for some time already: https://github.com/Andarist/typescript-go/tree/port/55600 ;p"
 * [6 days ago](https://github.com/microsoft/TypeScript-go/issues/3044#issuecomment-4033046373) **jakebailey** said "Same except I gave up 😄 "
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3061](https://github.com/microsoft/TypeScript-go/pull/3061) (Closed)

**Port Regular Expressions checking**

*Introduce a faithful port of the existing regular expression checking code.*

 * [5 days ago](https://github.com/microsoft/TypeScript-go/pull/3061#issuecomment-4040726976) **Andarist** said "It doesn't report the exact same errors as that PR in the regularExpressionDuplicateCapturingGroupName test - but what it does report is consistent with Strada"
 * [5 days ago](https://github.com/microsoft/TypeScript-go/pull/3061#issuecomment-4042850773) **jakebailey** said "Okay. Strada alignment is of course good 😄 "
 * [4 days ago](https://github.com/microsoft/TypeScript-go/pull/3061#issuecomment-4050922704) **jakebailey** said "In general, I would recheck that all of the comments are present too."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3073](https://github.com/microsoft/TypeScript-go/pull/3073) (Closed)

**Port missing \_\_makeTemplateObject transform, fix octal scanning**

*Add the missing __makeTemplateObject transform to handle ES2018+ template literal escapes with subtree optimization and correct octal scanning.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3082](https://github.com/microsoft/TypeScript-go/pull/3082) (Closed, **andrewbranch**, **Copilot**)

**API: Add modifierFlags, getResolvedSymbol, fix BlockScoped flags and empty NodeList mask encoding**

*Implements modifierFlags and getResolvedSymbol in the TypeScript API and fixes block-scoped flags and empty NodeList mask encoding in the binary protocol*

 * [4 days ago](https://github.com/microsoft/TypeScript-go/pull/3082#issuecomment-4051023204) **Copilot** listed the commits containing tests and described their coverage across async and sync API suites
 * [4 days ago](https://github.com/microsoft/TypeScript-go/pull/3082#issuecomment-4051065262) **andrewbranch** said "@copilot format"
 * [4 days ago](https://github.com/microsoft/TypeScript-go/pull/3082#issuecomment-4051093786) **Copilot** formatted code in commit fa81eb8 and noted that dprint reformatted import ordering and switch-case style in node.ts
 * [today](https://github.com/microsoft/TypeScript-go/pull/3082#issuecomment-4070503658) **andrewbranch** said "@copilot+claude-opus-4.6 fix failing API test build"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3082#issuecomment-4070555606) **Copilot** fixed two type errors in the API test build by casting Node to any for modifierFlags and typing refNode as Identifier for getResolvedSymbol
 * [today](https://github.com/microsoft/TypeScript-go/pull/3082#issuecomment-4070623320) **andrewbranch** suggested placing the property on nodes that also had modifiers
 * [today](https://github.com/microsoft/TypeScript-go/pull/3082#issuecomment-4070692270) **Copilot** fixed the missing modifierFlags issue by adding a readonly modifierFlags property to relevant node interfaces, generating the ModifierFlags enum, excluding modifierFlags from factory generation, and removing (as any) casts in tests
 * [today](https://github.com/microsoft/TypeScript-go/pull/3082#issuecomment-4070855916) **andrewbranch** said "@copilot only generate one ModifierFlags enum! Before you stop work, review your own code and ask yourself whether I'm likely to approve it, based on my review comments so far."
 * [today](https://github.com/microsoft/TypeScript-go/pull/3082#issuecomment-4070932777) **Copilot** removed duplicate `ModifierFlags` entry from enumDefs and consolidated its generation in @typescript/ast with updated imports in @typescript/api
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#3084](https://github.com/microsoft/TypeScript-go/pull/3084) (Open)

**Port LSP update imports on file rename support**

*Adds support to update import paths via LSP when files are renamed or moved to ensure correct relative references.*

 * created by **anchmelev**
 * [4 days ago](https://github.com/microsoft/TypeScript-go/pull/3084#issuecomment-4052113218) **anchmelev** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3084#issuecomment-4069834603) **anchmelev** pinged the reviewer for a review on LSP import updates including file rename/move support and tests
 * [today](https://github.com/microsoft/TypeScript-go/pull/3084#issuecomment-4070678965) **DanielRosenwasser** asked why the tests didn't use the typical fourslash test harness and whether existing tests from the old compiler were considered for porting
 * [today](https://github.com/microsoft/TypeScript-go/pull/3084#issuecomment-4071505057) **anchmelev** thanked DanielRosenwasser, moved the semantic workspace/willRenameFiles coverage to the fourslash harness, trimmed direct server tests to LSP wire-up assertions, added relevant getEditsForFileRename coverage for non-relative imports, and omitted directory/tsconfig-specific variants

### [PR microsoft/TypeScript-go#3090](https://github.com/microsoft/TypeScript-go/pull/3090) (Closed, **andrewbranch**, **Copilot**)

**Fix auto import not getting its own line**

*Ensure auto-imports are inserted with a trailing newline and preserve header comments when added before existing imports.*

 * created by **Copilot**
 * (3 days ago) **Copilot** assigned to **Copilot**, **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3090#issuecomment-4069911319) **andrewbranch** said "@copilot+claude-opus-4.6 add a test for Isabel's comment and fix, again using _submodules/TypeScript as the source of truth for the proper implementation."
 * [today](https://github.com/microsoft/TypeScript-go/pull/3090#issuecomment-4069964349) **Copilot** added TestAutoImportNewLineWithHeaderComment and fixed skipping header comments for first imports; updated InsertNodeBefore to accept an optional LeadingTriviaOption variadic parameter
 * [today](https://github.com/microsoft/TypeScript-go/pull/3090#issuecomment-4070306698) **andrewbranch** said "Nice, a lot of failing tests fixed with this"
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#3092](https://github.com/microsoft/TypeScript-go/pull/3092) (Closed)

**Rework enums back into a more Strada\-like form**

*Restore enum emission to the previous Strada-like approach by removing custom checker-less code and reinstating the emit resolver.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3095](https://github.com/microsoft/TypeScript-go/pull/3095) (Closed)

**Watch directories and react to symlink directory creation**

*Enhance directory watcher to detect symlink directory creation and handle directory deletion events*

 * created by **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#3101](https://github.com/microsoft/TypeScript-go/pull/3101) (Closed, `dependencies`, `github_actions`)

**Bump github/codeql\-action from 4\.32\.6 to 4\.33\.0 in the github\-actions group across 1 directory**

*Bump the GitHub CodeQL Action dependency from version 4.32.6 to 4.33.0 in the main workflow directory.*

 * (today) **dependabot[bot]** added labels `github_actions`, `dependencies`, `github_actions`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3103](https://github.com/microsoft/TypeScript-go/pull/3103) (Closed)

**Fixed a signature help crash related to tagged template calls**

*Fixed a crash in signature help that occurred when processing tagged template calls.*

 * created by **Andarist**
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript-go#3104](https://github.com/microsoft/TypeScript-go/pull/3104) (Closed)

**Block renames in keywords/stdlib, add prepareRename**

*Implement prepareRename to block renames of keywords and standard library identifiers, maintain fallback prechecks, and extend fourslash tests.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3105](https://github.com/microsoft/TypeScript-go/pull/3105) (Closed)

**Fix a document highlight crash caused by expression in type parameter declaration**

*Prevent document highlight from crashing by properly handling expressions within type parameter declarations.*

 * created by **Andarist**
 * (today) **gabritto** closed the issue

### [Issue microsoft/TypeScript-go#3106](https://github.com/microsoft/TypeScript-go/issues/3106) (Closed, **jakebailey**, **Copilot**)

**Project reference redirect uses wrong tsconfig when file belongs to multiple sub\-projects \(breaks customConditions/moduleSuffixes\)**

*When a file belongs to multiple composite tsconfigs, tsgo uses the wrong project reference redirect, ignoring customConditions and moduleSuffixes.*

 * created by **tian000**
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#3107](https://github.com/microsoft/TypeScript-go/pull/3107) (Closed, **jakebailey**, **Copilot**)

**Fix project reference redirect ordering when file belongs to multiple sub\-projects**

*Reverse project reference mapping order to apply parent tsconfig mappings before child projects, preserving customConditions and moduleSuffixes.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#3108](https://github.com/microsoft/TypeScript-go/pull/3108) (Closed)

**Fix panic caused by importing a type\-only alias using \`require\(\.\.\.\)\` in JS**

*Using require to import a module that exports only a type alias in CommonJS JS causes a compiler panic.*

 * created by **ahejlsberg**
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#3109](https://github.com/microsoft/TypeScript-go/pull/3109) (Closed)

**Fix project reference redirect for files in multiple sub\-projects**

*Reorder initMapperWorker to copy parent project maps before sub-project recursion so child mappings override parent ones and customConditions/moduleSuffixes apply correctly*

 * created by **tian000**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3109#issuecomment-4070015068) **jakebailey** said "This is just a copy and paste of #3107 re-attributed to you... Why send it?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3109#issuecomment-4070030148) **tian000** said "Closing as duplicate of #3107 which implements the same fix (reordering maps.Copy before recursion in initMapperWorker to match TypeScript's parseProjectReferenceConfigFile behavior)."
 * (today) **tian000** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/3109#issuecomment-4070053939) **tian000** said "My bad @jakebailey should've checked first! Ty for the fix :) "

### [PR microsoft/TypeScript-go#3110](https://github.com/microsoft/TypeScript-go/pull/3110) (Closed)

**Big omnibus of JS emit differences**

*Addresses miscellaneous JavaScript emit differences by extracting destructuring code to ensure consistent CommonJS output.*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#3111](https://github.com/microsoft/TypeScript-go/pull/3111) (Closed)

**Fix type of \`this\` in non\-strict mode \.js files**

*Add missing code to correctly type `this` in non-strict mode JavaScript files.*

 * created by **ahejlsberg**
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#3112](https://github.com/microsoft/TypeScript-go/pull/3112) (Closed)

**Fix quoted rename prefix/suffix**

*Reintroduce missing quote detection logic to properly handle rename prefixes and suffixes.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3113](https://github.com/microsoft/TypeScript-go/pull/3113) (Closed)

**Stop converting lsproto Ranges/Positions to pointers and back**

*Eliminate unnecessary pointer conversions for lsproto Ranges and Positions to simplify code and reduce overhead.*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#3114](https://github.com/microsoft/TypeScript-go/pull/3114) (Open)

**Don't use full emit resolver just because JSX is enabled**

*Use the full emit resolver only for files containing JSX to avoid unnecessary work and improve concurrency.*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#3115](https://github.com/microsoft/TypeScript-go/pull/3115) (Closed)

**Avoid extra allocations for enum inlining comments**

*Use a single builder for enum inlining comments to eliminate extra allocations from replacements and concatenations.*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#3116](https://github.com/microsoft/TypeScript-go/pull/3116) (Closed)

**Remove gofumpt as go\.mod tool, use dprint**

*Switch code formatting tooling from gofumpt to dprint in go.mod to reduce dependencies and avoid version skew.*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#3117](https://github.com/microsoft/TypeScript-go/pull/3117) (Open)

**Don't use parent pointer in classfields\.go visitPrivateIdentifier**

*Handle private identifier visits in classfields.go at a higher level to avoid dubious parent pointer usage.*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#3118](https://github.com/microsoft/TypeScript-go/pull/3118) (Open)

**Fix difference between checker and binder resolvers**

*Re-align checker and binder resolvers by restoring getReferencedValueOrAliasSymbol and replacing obsolete symbol resolution functions.*

 * created by **jakebailey**

### [Issue microsoft/TypeScript-go#3119](https://github.com/microsoft/TypeScript-go/issues/3119) (Closed)

**Formatter adds a space at the end of file containing a class**

*tsgo's formatter adds an unwanted trailing space after a class's closing brace, unlike typescript@6.0 which omits it.*

 * created by **PeterStaev**

### [Issue microsoft/TypeScript-go#3120](https://github.com/microsoft/TypeScript-go/issues/3120) (Open, `Crash`)

**thread exhaustion \- program exceeds 10000\-thread limit \- one off error**

*An unreproducible Go runtime crash arises when the program exceeds the 10000-thread limit.*

 * created by **lukpsaxo**
 * **lukpsaxo** added label `Crash`

### [Issue microsoft/TypeScript-go#3121](https://github.com/microsoft/TypeScript-go/issues/3121) (Open, `Needs More Info`)

**extension gets uninstalled after around an hour on vscodium**

*The TypeScript Native Preview extension installed in VSCodium on Linux is uninstalled after about an hour for being flagged problematic.*

 * created by **huseeiin**

### [PR microsoft/TypeScript-go#3122](https://github.com/microsoft/TypeScript-go/pull/3122) (Closed)

**Fix issue in \`checkIndexConstraints\`**

*Port fix and tests from an unported pull request to correct index constraint checking in TypeScript*

 * created by **ahejlsberg**

