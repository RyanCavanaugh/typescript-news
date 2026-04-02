# Report for 2026-02-09 (Monday, February 9th, 2026)

9 different users commented on 29 different issues.

## Recommended Actions

 * Response Recommended
    * @virtuallyunknown provided testing confirmation and version details in [microsoft/TypeScript-go#2444](https://github.com/microsoft/TypeScript-go/issues/2444#issuecomment-3874988236)

## Activity Summary

### [Issue microsoft/TypeScript-go#1531](https://github.com/microsoft/TypeScript-go/issues/1531) (Closed, `Crash`, `Domain: Program`, **sheetalkamat**, **gabritto**)

**tsgo panics with invalid UTF\-8 when marshalling build info**

*tsgo panics during build info marshalling because it encounters invalid UTF-8 in diagnostic messages.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1531#issuecomment-3746812464) **gabritto** said "Related: #2336"
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/1531#issuecomment-3815132905) **scarf005** asked what to do to fix a panic error in tsgo typecheck and reported that removing .tsbuildinfo did not help
 * **gabritto** assigned to **gabritto**
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript-go#1604](https://github.com/microsoft/TypeScript-go/pull/1604) (Closed)

**Always provide ModuleSpecifierGenerationHost to NodeBuilder**

*Ensure NodeBuilder always receives a ModuleSpecifierGenerationHost for consistent module specifier generation.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#1615](https://github.com/microsoft/TypeScript-go/issues/1615) (Closed, `Domain: Editor`)

**VSCode Extension blocks Organize Imports**

*The TypeScript Native Preview VSCode extension prevents the Organize Imports command from working until disabled.*

 * [6 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1615#issuecomment-3688522259) **14glwu** said "the same issue"
 * [6 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1615#issuecomment-3694964143) **kevcam4891** said "Same! Would love to not have to disable this extension to occasionally organize imports."
 * [1 month ago](https://github.com/microsoft/TypeScript-go/issues/1615#issuecomment-3716167778) **NatoBoram** provided links to related issues and pull requests
 * [today](https://github.com/microsoft/TypeScript-go/issues/1615#issuecomment-3872877288) **jakebailey** said "This should have been closed by #2331."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#1770](https://github.com/microsoft/TypeScript-go/pull/1770) (Open)

**Organize imports for TypeScript and JavaScript**

*Expose TypeScript and JavaScript import organizer via LSP command in VS Code, preserving blank lines and sorting imports*

 * [17 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1770#issuecomment-3385605813) **jakebailey** acknowledged the suggestion and expressed uncertainty about registering the same command as the main TS extension
 * [13 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1770#issuecomment-3493026664) **jakebailey** advised merging with main to check for duplicate helpers and suggested reusing the existing command name or using the when clause
 * [9 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1770#issuecomment-3606626496) **mkantor** asked whether microsoft/TypeScript#60431 still occurred with this implementation
 * [today](https://github.com/microsoft/TypeScript-go/pull/1770#issuecomment-3872878146) **jakebailey** said "I think #2331 supersedes this?"

### [Issue microsoft/TypeScript-go#2275](https://github.com/microsoft/TypeScript-go/issues/2275) (Closed, `Domain: Editor`, **sheetalkamat**)

**Race condition detected between program updates and ATA\(?\)**

*Concurrent program updates and automatic type acquisition operations trigger a race condition, causing unexpected completion responses.*

 * created by **DanielRosenwasser**
 * **DanielRosenwasser** assigned to **sheetalkamat**
 * **jakebailey** added label `Domain: Editor`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2336](https://github.com/microsoft/TypeScript-go/issues/2336) (Closed, `Crash`, **jakebailey**, **gabritto**, **Copilot**)

**Crash for signature help in arrow function parameters**

*Signature help invoked on arrow function parameters crashes the TypeScript server without a stack trace*

 * [1 month ago](https://github.com/microsoft/TypeScript-go/issues/2336#issuecomment-3720210437) **gabritto** asked where the old compiler escaped internal types and noted that Strada returned "__type(...)" as label
 * [1 month ago](https://github.com/microsoft/TypeScript-go/issues/2336#issuecomment-3720242722) **jakebailey** clarified that symbol names with __ prefixes sometimes leaked, which was unacceptable in Go code due to the UTF-8 trick, and that they had not found a better alternative
 * **gabritto** assigned to **gabritto**
 * (today) **gabritto** closed the issue

### [Issue microsoft/TypeScript-go#2402](https://github.com/microsoft/TypeScript-go/issues/2402) (Open, `Crash`, **jakebailey**, **Copilot**)

**tsgo takes forever to compile, 325seconds vs typescript 42seconds**

*tsgo watch compilation takes 325s versus TypeScript’s 42s, and the reporter requests help diagnosing and resolving the slowdown.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2402#issuecomment-3797224077) **jakebailey** said "I'm sure we can come up with a better way to do this, this code hasn't been optimized. It was never an issue in the old compiler since strings were already UTF-16."
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2402#issuecomment-3798254127) **jogibear9988** noted that adding newlines to codegen reduced compilation to 24 seconds with ts-go and sourcemaps but left the issue unresolved in ts-go, suggested leaving the issue open, and mentioned the largest generated file was a js file
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/2402#issuecomment-3805742727) **ffmiruz** mentioned wanting confirmation of the approach, noted that iterating over bytes was necessary, suggested checking for ASCII-ness for optimization with a rune fallback, and provided benchmark results
 * (later) **jakebailey** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#2444](https://github.com/microsoft/TypeScript-go/issues/2444) (Open, `Domain: Editor`)

**Missing code actions \(\`editor\.codeActionsOnSave\`\) with \`typescript\.experimental\.useTsgo\` in VSCode**

*Enabling typescript.experimental.useTsgo in VSCode disables most code actions on save, preventing missing imports from being added automatically.*

 * created by **virtuallyunknown**
 * **virtuallyunknown** added label `Domain: Editor`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2444#issuecomment-3872879855) **jakebailey** said "I believe #2331 implemented these, but I don't know if they'll show in the editor like this. Worth testing on the next nightly."
 * [today](https://github.com/microsoft/TypeScript-go/issues/2444#issuecomment-3873543629) **iisaduan** noted that `source.OrganizeImports`, `source.removedUnusedImports`, and `source.sortImporrts` were implemented with #2331 and mentioned that the rest remained unported
 * (today) **virtuallyunknown** closed the issue
 * (today) **virtuallyunknown** reopened the issue
 * [today](https://github.com/microsoft/TypeScript-go/issues/2444#issuecomment-3874988236) **virtuallyunknown** reported that settings worked as expected and listed available code actions, noted testing details, and apologized for accidentally closing the issue

### [PR microsoft/TypeScript-go#2569](https://github.com/microsoft/TypeScript-go/pull/2569) (Closed, **andrewbranch**, **Copilot**)

**Fix getVisualListRange bug in formatting \(partial fix for import promotion crash\)**

*Use GetStartOfNode instead of Pos in getVisualListRange to skip trivia and prevent import promotion formatting crashes.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2569#issuecomment-3786716239) **andrewbranch** said "@copilot seems like tests are still failing"
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2569#issuecomment-3786881437) **Copilot** fixed tests failing by addressing two bugs in getVisualListRange and import reordering logic
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2569#issuecomment-3786979320) **Copilot** reverted to a simple fix in commit a1301d95 and removed complex autoimport and investigation changes
 * [today](https://github.com/microsoft/TypeScript-go/pull/2569#issuecomment-3873204123) **andrewbranch** said "I don't have time to fix the bad formatting right now, but I think we should accept the crash fix and do a follow-up sweep of formatting fixes."

### [Issue microsoft/TypeScript-go#2609](https://github.com/microsoft/TypeScript-go/issues/2609) (Open, `Domain: Type Checking`, `Type Ordering`, **ahejlsberg**)

**Type instantiation is excessively deep and possibly infinite\.**

*tsgo throws a deep, possibly infinite type instantiation error for TanStack Form with zod that TypeScript 5.9 compiles without issue.*

 * (1 week ago) **ahejlsberg** added labels `Type Ordering`, `Domain: Type Checking`
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/2609#issuecomment-3855592321) **TkDodo** inquired if anything could be improved in the TanStack form typings
 * [today](https://github.com/microsoft/TypeScript-go/issues/2609#issuecomment-3874708331) **jakebailey** suggested testing the TS 6.0 nightly with --stableTypeOrdering to try out the new algorithm

### [PR microsoft/TypeScript-go#2634](https://github.com/microsoft/TypeScript-go/pull/2634) (Closed)

**Fix panic when marshaling build info with invalid UTF\-8**

*Sanitize diagnostic message arguments by replacing invalid UTF-8 sequences with the Unicode replacement character to avoid JSON marshaling panics.*

 * created by **scarf005**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2634#issuecomment-3874979579) **scarf005** said "fixed by #2704"
 * (today) **scarf005** closed the issue

### [Issue microsoft/TypeScript-go#2653](https://github.com/microsoft/TypeScript-go/issues/2653) (Closed, `bug`, **ahejlsberg**)

**Static properties on manual \(pre\-ES6\) classes can't be declared and then defined**

*tsgo incorrectly reports duplicate identifier errors when declaring and defining static properties on pre-ES6 classes.*

 * created by **peetklecha**
 * [6 days ago](https://github.com/microsoft/TypeScript-go/issues/2653#issuecomment-3842789026) **ahejlsberg** explained that the expando declaration is classified as a property, causing a conflict with the method declaration, and suggested changing the static declaration to property style to resolve it
 * [6 days ago](https://github.com/microsoft/TypeScript-go/issues/2653#issuecomment-3842795168) **ahejlsberg** said "But I can also see arguments for why this shouldn't be an error..."
 * [today](https://github.com/microsoft/TypeScript-go/issues/2653#issuecomment-3873053632) **ahejlsberg** proposed creating expando assignment declarations only for properties without regular declarations and planned to submit a PR
 * (today) **ahejlsberg** added label `bug`, and assigned to **ahejlsberg**
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#2654](https://github.com/microsoft/TypeScript-go/issues/2654) (Open, `wontfix`)

**Empty array can now be assigned to a bespoke property on a function**

*tsgo allows assigning an empty array to an undeclared function property inferring never[], whereas TypeScript 5.9 reports error TS7008*

 * created by **peetklecha**
 * [6 days ago](https://github.com/microsoft/TypeScript-go/issues/2654#issuecomment-3842382017) **jakebailey** said "Why is it expected that this errors?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2654#issuecomment-3873255780) **ahejlsberg** explained that tsc infers any[] but tsgo infers never[] in strict mode and any[] in non-strict mode and endorsed tsgo's behavior
 * **ahejlsberg** added label `wontfix`

### [PR microsoft/TypeScript-go#2680](https://github.com/microsoft/TypeScript-go/pull/2680) (Closed, **andrewbranch**, **Copilot**)

**Fix module resolver bug exposed by malformed package\.json import patterns**

*Fix module resolver bug that crashed the language server with malformed package.json wildcard import patterns*

 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/2680#issuecomment-3862627198) **Copilot** fixed test failures by adding missing reference baselines
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/2680#issuecomment-3863080260) **Copilot** explained that all tests now passed after adding missing baselines
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/2680#issuecomment-3864768635) **Copilot** described the changes in commit 85d2d5e1, preserved the first panic, inlined extraction logic in the second block, updated tests and baselines with directives, and renamed tests
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#2699](https://github.com/microsoft/TypeScript-go/issues/2699) (Open)

**tsgo resolves inherited include/exclude globs differently than tsc when using extends**

*tsgo resolves inherited include globs relative to the child config rather than the parent, causing a different output structure than tsc.*

 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/2699#issuecomment-3861948071) **jakebailey** provided a link to the repro directory, suggested setting rootDir to "../../", and noted that includes are not inherited
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/2699#issuecomment-3861987821) **mabels** ran builds with tsc and tsgo and demonstrated that tsgo scattered .js and .js.map files throughout the monorepo
 * [today](https://github.com/microsoft/TypeScript-go/issues/2699#issuecomment-3872036706) **Knagis** highlighted a contradiction between the TypeScript tsconfig inheritance docs and @jakebailey’s earlier statement
 * [today](https://github.com/microsoft/TypeScript-go/issues/2699#issuecomment-3872875730) **jakebailey** suggested that multiple bugs were causing the issue, including a missing rootDir error message and an includes-related problem
 * [today](https://github.com/microsoft/TypeScript-go/issues/2699#issuecomment-3872883472) **jakebailey** pointed to an existing implementation in tsconfigparsing.go
 * [today](https://github.com/microsoft/TypeScript-go/issues/2699#issuecomment-3874700604) **jakebailey** said "In any case, resetting this conversation, someone just needs to investigate what's going on here. Sorry for the false start."

### [PR microsoft/TypeScript-go#2702](https://github.com/microsoft/TypeScript-go/pull/2702) (Closed)

**Fix race when copying lazy computed values for updateProgram**

*Fix race condition when updateProgram copies lazily computed values.*

 * created by **sheetalkamat**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2703](https://github.com/microsoft/TypeScript-go/issues/2703) (Closed, `bug`, `Domain: JSX`, **ahejlsberg**)

**JSX render prop children incorrectly intersects with \`{}\`**

*ts-go erroneously intersects JSX render prop children with {} leading to assignment errors absent in TypeScript 6.0.*

 * created by **karmeleon**
 * (today) **DanielRosenwasser** added labels `bug`, `Domain: JSX`, and assigned to **ahejlsberg**

### [PR microsoft/TypeScript-go#2704](https://github.com/microsoft/TypeScript-go/pull/2704) (Closed)

**Allow invalid UTF\-8**

*Update JSON marshalling to accept invalid UTF-8 so internal symbol prefixes no longer cause crashes.*

 * created by **gabritto**
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/2704#issuecomment-3862508414) **sheetalkamat** updated branch with pre-leave tests, referenced the tsc test for incremental checks, and suggested updating the baseline sanitizer to support symbol IDs in names
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript-go#2713](https://github.com/microsoft/TypeScript-go/pull/2713) (Closed, `dependencies`, `github_actions`)

**Bump github/codeql\-action from 4\.32\.0 to 4\.32\.2 in the github\-actions group across 1 directory**

*Upgrade github/codeql-action from 4.32.0 to 4.32.2 to update the default CodeQL bundle to v2.24.1.*

 * (today) **dependabot[bot]** added labels `github_actions`, `dependencies`, `github_actions`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2714](https://github.com/microsoft/TypeScript-go/pull/2714) (Closed)

**Update npm deps, dprint plugins**

*Update npm dependencies, improve LSP diagnostics, and upgrade dprint plugins to fix audit warnings and avoid empty Go file crashes.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2715](https://github.com/microsoft/TypeScript-go/pull/2715) (Closed)

**Defer binding of expando assignments and give them lower priority**

*Defer expando property assignment binding until after other declarations and create declaration sites only for names lacking regular declarations.*

 * created by **ahejlsberg**
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#2716](https://github.com/microsoft/TypeScript-go/pull/2716) (Open)

**Implement sync API without NAPI**

*A pure JavaScript synchronous child process API using fs.readSync/writeSync replaces the napi-rs module with comparable performance.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2716#issuecomment-3873671799) **jakebailey** said "Seemingly this does not work on Windows, which hangs. I didn't exactly test there, so, fair."

### [PR microsoft/TypeScript-go#2717](https://github.com/microsoft/TypeScript-go/pull/2717) (Open)

**\[draft\] parse formatting options in initialization **

*Implement a draft parser for formatting options during initialization to facilitate sharing and testing*

 * created by **iisaduan**

### [PR microsoft/TypeScript-go#2718](https://github.com/microsoft/TypeScript-go/pull/2718) (Closed)

**Update submodule to latest 6\.0 main pre\-beta**

*Update the project submodule to the latest 6.0 main pre-beta release, integrating new library changes and basic ES2025 support.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2719](https://github.com/microsoft/TypeScript-go/pull/2719) (Open, **jakebailey**, **Copilot**)

**Optimize source map character offset calculation with correct UTF\-16 counting**

*Optimize source map offsets by using an O(1) ASCII path and proper UTF-16 code unit counting to improve compile performance.*

 * created by **Copilot**
 * (later) **Copilot** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#2720](https://github.com/microsoft/TypeScript-go/issues/2720) (Closed, `Crash`, **ahejlsberg**)

**panic handling request textDocument/hover**

*The TypeScript Go LSP server panics with a nil pointer dereference error when processing textDocument/hover requests.*

 * created by **christophe-g**
 * **christophe-g** added label `Crash`

### [Issue microsoft/TypeScript-go#787](https://github.com/microsoft/TypeScript-go/issues/787) (Closed)

**\`UnionToTuple\` type returns "inverted" tuple in TSGO compared to TypeScript 5\.8\.3 and gives type error**

*TSGO's UnionToTuple type generates tuples in reverse order compared to TypeScript 5.8.3, causing type errors*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/787#issuecomment-3866952237) **juhort** asked whether the union order would always be the same given identical generic inputs, avoiding issues like the one mentioned by LukeAbby
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/787#issuecomment-3867504473) **jakebailey** said "Yes, correct."
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/787#issuecomment-3867505544) **jakebailey** said "In the 6.0 nightly, you can now also pass --stableTypeOrdering to try this sorting out early."
 * [today](https://github.com/microsoft/TypeScript-go/issues/787#issuecomment-3872828964) **alexwork1611** thanked for the information about the --stableTypeOrdering flag

