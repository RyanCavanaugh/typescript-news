# Report for 2026-04-06 (Monday, April 6th, 2026)

14 different users commented on 35 different issues.

## Recommended Actions

 * Response Recommended
    * @samdcoding provided reproduction steps and error logs in [microsoft/TypeScript-go#2959](https://github.com/microsoft/TypeScript-go/issues/2959#issuecomment-4194260358)
    * @limwa asked if a contributed fix for the heuristic would be welcome in [microsoft/TypeScript-go#3341](https://github.com/microsoft/TypeScript-go/issues/3341#issuecomment-4194345559)
    * @youngspe asked for a preferred way of writing a declaration file that re-exports an ES module as a CommonJS module across TS versions in [microsoft/TypeScript-go#3347](https://github.com/microsoft/TypeScript-go/issues/3347#issuecomment-4194504236)
    * @abrahamguo asked why direct imports from @eslint/config-helpers did not reproduce the issue and if eslint/lib/types/config-api.d.ts could be the cause in [microsoft/TypeScript-go#3347](https://github.com/microsoft/TypeScript-go/issues/3347#issuecomment-4198818076)

## Activity Summary

### [Issue microsoft/TypeScript-go#1600](https://github.com/microsoft/TypeScript-go/issues/1600) (Closed, `Domain: Editor`, **weswigham**)

**Hovering an optional boolean param in strict mode shows \`param?: boolean \| undefined\`**

*Hovering over an optional boolean parameter in strict mode shows it as boolean | undefined instead of boolean*

 * **jakebailey** added label `Domain: Editor`
 * [32 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1600#issuecomment-3201713699) **jakebailey** said "Unsurprisingly, this comes down to serializeTypeForDeclaration missing node reuse."
 * **RyanCavanaugh** assigned to **weswigham**
 * [today](https://github.com/microsoft/TypeScript-go/issues/1600#issuecomment-4195590031) **jakebailey** noted the fix in #2459 and attached an image
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#1704](https://github.com/microsoft/TypeScript-go/issues/1704) (Closed, `Domain: Editor`, `Crash`, **iisaduan**, **Copilot**)

**textDocument/completion Could not find symbol**

*TypeScript Go LSP crashes on completions complaining it cannot find the 'sourceMapsEnabled' symbol in graceful-fs types.*

 * [27 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1704#issuecomment-3330936550) **andrewbranch** provided reproduction steps for a module resolution issue with null exports in the TS repo
 * **jakebailey** assigned to **Copilot**
 * [24 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1704#issuecomment-3412037108) **DanielRosenwasser** said "I think https://github.com/microsoft/typescript-go/pull/1844 is on this one even though it didn't link back."
 * [today](https://github.com/microsoft/TypeScript-go/issues/1704#issuecomment-4195582259) **jakebailey** said "Tested and this one does not happen anymore. I'm sure it was the snapshot stuff that fixed it a while back"
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#1741](https://github.com/microsoft/TypeScript-go/issues/1741) (Closed, `Domain: Type Checking`, `Domain: Declaration Emit`, **weswigham**)

**tsgo does not use assertion as a source for the type of  a default export\.**

*tsgo ignores type assertions on default exports, causing private name 'Bar' errors instead of using the asserted type.*

 * (27 weeks ago) **jakebailey** added labels `Domain: Type Checking`, `Domain: Declaration Emit`
 * **RyanCavanaugh** assigned to **weswigham**
 * [today](https://github.com/microsoft/TypeScript-go/issues/1741#issuecomment-4194882780) **jakebailey** said "This was fixed in #2459."
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#1762](https://github.com/microsoft/TypeScript-go/issues/1762) (Closed, `Domain: Declaration Emit`, **weswigham**)

**adding a root dir that is a child of another root dir causes different relative paths in declaration**

*Adding a nested rootDirs entry causes tsgo to generate different relative import paths in declarations compared to TypeScript.*

 * created by **dragomirtitian**
 * **jakebailey** added label `Domain: Declaration Emit`
 * **RyanCavanaugh** assigned to **weswigham**
 * [today](https://github.com/microsoft/TypeScript-go/issues/1762#issuecomment-4194922893) **jakebailey** said "This appears to be fixed."
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#1771](https://github.com/microsoft/TypeScript-go/issues/1771) (Closed, `Domain: Declaration Emit`, **weswigham**)

**Inferred import type in declaration file uses actual path not use rootdirs path**

*In declaration files, inferred import types use the actual source path instead of the configured rootDirs path.*

 * [26 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1771#issuecomment-3356149355) **AlCalzone** said "Possibly related to https://github.com/microsoft/typescript-go/issues/1347, although that issue is about symlinked packages."
 * **jakebailey** added label `Domain: Declaration Emit`
 * **RyanCavanaugh** assigned to **weswigham**
 * [today](https://github.com/microsoft/TypeScript-go/issues/1771#issuecomment-4194905880) **jakebailey** said "This appears to be fixed."
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#1784](https://github.com/microsoft/TypeScript-go/issues/1784) (Closed, `Domain: Declaration Emit`, **weswigham**)

**type alias is resolved in function type causing type to be unnamable**

*Resolving a type alias in a function signature causes an unnamable external type error during declaration emission in tsgo.*

 * created by **dragomirtitian**
 * **jakebailey** added label `Domain: Declaration Emit`
 * **RyanCavanaugh** assigned to **weswigham**
 * [today](https://github.com/microsoft/TypeScript-go/issues/1784#issuecomment-4194884136) **jakebailey** said "This was fixed in #2459."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2944](https://github.com/microsoft/TypeScript-go/pull/2944) (Open)

**\[draft\] more formatting tests **

*Add draft formatting tests to validate and troubleshoot the repository’s testing pipelines.*

 * [5 days ago](https://github.com/microsoft/TypeScript-go/pull/2944#issuecomment-4172314407) **typescript-bot** provided a build status update with links to the test top100 job start and results
 * [5 days ago](https://github.com/microsoft/TypeScript-go/pull/2944#issuecomment-4172722240) **typescript-bot** reported that running the top 400 repos with tsc comparing main and the PR merge looked good
 * [5 days ago](https://github.com/microsoft/TypeScript-go/pull/2944#issuecomment-4173701578) **typescript-bot** said "@iisaduan, the perf run you requested failed. You can check the log here."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2944#issuecomment-4194633940) **typescript-bot** reported the requested performance run results
 * [today](https://github.com/microsoft/TypeScript-go/pull/2944#issuecomment-4194658037) **typescript-bot** said "@iisaduan, the perf run you requested failed. You can check the log here."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2944#issuecomment-4194708449) **typescript-bot** reported the requested perf run results with comparison metrics for compiler-unions between baseline and PR
 * [today](https://github.com/microsoft/TypeScript-go/pull/2944#issuecomment-4194728797) **typescript-bot** said "@iisaduan, the perf run you requested failed. You can check the log here."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2944#issuecomment-4195097404) **typescript-bot** provided the requested perf run results
 * [today](https://github.com/microsoft/TypeScript-go/pull/2944#issuecomment-4195115801) **typescript-bot** said "@iisaduan, the perf run you requested failed. You can check the log here."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2944#issuecomment-4195436692) **iisaduan** said "@typescript-bot perf test this"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2944#issuecomment-4195437043) **typescript-bot** noted that CI build started and posted status update
 * [today](https://github.com/microsoft/TypeScript-go/pull/2944#issuecomment-4195501446) **typescript-bot** posted the requested performance run results

### [Issue microsoft/TypeScript-go#2959](https://github.com/microsoft/TypeScript-go/issues/2959) (Open, `Crash`, **iisaduan**)

**panic handling request textDocument/definition: bad line number**

*The TypeScript Go LSP server panics in textDocument/definition when an out-of-range line number is passed to the line-and-character to position converter.*

 * created by **Zzzen**
 * **Zzzen** added label `Crash`
 * **RyanCavanaugh** assigned to **iisaduan**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2959#issuecomment-4194260358) **samdcoding** provided reproduction steps and logs demonstrating an IDE 'bad line number' error when restoring a modified TS file

### [PR microsoft/TypeScript-go#3159](https://github.com/microsoft/TypeScript-go/pull/3159) (Open, **jakebailey**, **Copilot**)

**Fix format selection deleting comments when selection ends inside comment trivia**

*Prevent comments from being deleted when formatting selections end inside comment trivia by adjusting trivia range handling.*

 * **Copilot** assigned to **jakebailey**
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3159#issuecomment-4092429944) **jakebailey** said "@copilot+claude-opus-4.6 you must not have run the tests. you broke formatSelectionEditAtEndOfRange_test"
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3159#issuecomment-4092680089) **Copilot** fixed broken formatSelectionEditAtEndOfRange_test by capping previousRangeTriviaEnd before comment trivia in consumeTokenAndAdvanceScanner and verified tests pass
 * [today](https://github.com/microsoft/TypeScript-go/pull/3159#issuecomment-4195608650) **jakebailey** said "@copilot address review comments"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3159#issuecomment-4195634797) **Copilot** addressed all three review comments in commit 11fd998d by fixing misleading position comments, renaming the test description, and replacing loose assertions with exact checks

### [PR microsoft/TypeScript-go#3217](https://github.com/microsoft/TypeScript-go/pull/3217) (Open)

**Watch cli efficiency update**

*Watch CLI efficiency improvements implement debouncing, configuration caching, and dependency parsing to avoid unnecessary recompilations.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3217#issuecomment-4129133587) **johnfav03** described implementing the change by separating file tracking into a FileWatcher struct with a callback linked to doCycle while keeping caches, program construction, and emitting logic in the Watcher wrapper
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3217#issuecomment-4143654633) **andrewbranch** expressed that the commit wasn’t sufficient for wildcard watching, asked what “incremental skips emit for new unreferenced file” means, and suggested reading the directory recursively to detect new files
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/3217#issuecomment-4185460956) **andrewbranch** used Copilot to generate tests and discovered multiple race conditions in vfswatch and watcher, linking a commit with detailed results
 * [today](https://github.com/microsoft/TypeScript-go/pull/3217#issuecomment-4194915866) **johnfav03** thanked for the race tests and added mutexes to the Watcher and FileWatcher structs to fix race conditions and confirmed no race warnings with Copilot tests

### [Issue microsoft/TypeScript-go#3310](https://github.com/microsoft/TypeScript-go/issues/3310) (Closed, `Domain: Declaration Emit`, **weswigham**)

**Non\-exported interfaces triggers a "cannot be named" error**

*Exported variable using a type alias based on a non-exported interface triggers a "cannot be named" error in TypeScript 7.*

 * created by **DanielRosenwasser**
 * (5 days ago) **RyanCavanaugh** added label `Domain: Declaration Emit`, and assigned to **weswigham**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3310#issuecomment-4195497953) **jakebailey** said "#3314 should have closed this"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3333](https://github.com/microsoft/TypeScript-go/pull/3333) (Closed)

**Activate extension on typescript\.native\-preview\.enable**

*Enable extension activation when the typescript.native-preview.enable setting is enabled.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3341](https://github.com/microsoft/TypeScript-go/issues/3341) (Closed)

**Suggested autocompletions are not accepted by the compiler**

*TypeScript’s autocomplete for the attributes option erroneously suggests "age" despite it being excluded by forbiddenAttributes.*

 * created by **limwa**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3341#issuecomment-4194124655) **RyanCavanaugh** explained that completions sometimes yielded a wider union than accepted to facilitate code modifications and clarified that literal completions are not guaranteed to align strictly with inferred types
 * [today](https://github.com/microsoft/TypeScript-go/issues/3341#issuecomment-4194345559) **limwa** proposed refining the autocompletion heuristic to consider undefined properties for suggestions and asked if a contributed fix would be welcome
 * [today](https://github.com/microsoft/TypeScript-go/issues/3341#issuecomment-4194452129) **RyanCavanaugh** explained that changing the behavior was risky and preferred not to implement it given its minor annoyance relative to missing values
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#3345](https://github.com/microsoft/TypeScript-go/pull/3345) (Open)

**Reparse CJS export assignments only when not shadowed by locals**

*Parser now tracks local module and exports shadowing to prevent misparsing CommonJS export assignments.*

 * created by **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3345#issuecomment-4193866387) **jakebailey** noted that cjs-module-lexer expected nested declarations as exports but that the ESM loader would not error and would bind them as undefined
 * [today](https://github.com/microsoft/TypeScript-go/pull/3345#issuecomment-4194649465) **ahejlsberg** explained that cjs-module-lexer didn't perform scope analysis and discussed complications with module detection in TypeScript regarding mixed CJS/ESM code
 * [today](https://github.com/microsoft/TypeScript-go/pull/3345#issuecomment-4194814881) **jakebailey** noted that reparsing was problematic because ESM constructs may appear later, mentioned that PR #3167 attempted to solve it in the binder, and expressed dissatisfaction with doing binder-esque work in the parser
 * [today](https://github.com/microsoft/TypeScript-go/pull/3345#issuecomment-4194857584) **ahejlsberg** agreed and suggested eliminating JSExportAssignment and CommonJSExport reparsing in reparseCommonJS and instead binding and checking them as in Strada, ignoring CJS constructs in ESM modules

### [Issue microsoft/TypeScript-go#3347](https://github.com/microsoft/TypeScript-go/issues/3347) (Closed, **andrewbranch**)

**TS1361: 'defineConfig' cannot be used as a value because it was imported using 'import type'\.**

*tsgo triggers TS1361 complaining that defineConfig imported with import type cannot be used as a value in ESLint config.*

 * created by **314systems**
 * **ahejlsberg** assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3347#issuecomment-4194141803) **andrewbranch** diagnosed a TypeScript 6.0 bug and noted that tsgo works as intended, pointing out that @eslint/config-helpers should not have used import type
 * (today) **andrewbranch** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/issues/3347#issuecomment-4194504236) **youngspe** noted a related ESLint bug and asked for a preferred way to write a declaration file re-exporting an ES module as a CommonJS module compatible with TS versions before 5.8 and from 7.0 onward
 * [today](https://github.com/microsoft/TypeScript-go/issues/3347#issuecomment-4194594359) **andrewbranch** explained that TypeScript declaration files are generated artifacts and argued that properly supporting ESM and CJS requires two independent sets of declaration files, noting that the current hand-authored files misrepresent the builds and cause compatibility errors
 * [today](https://github.com/microsoft/TypeScript-go/issues/3347#issuecomment-4194623925) **andrewbranch** mentioned that many people write type definitions in a CJS context and re-export them from an ESM entrypoint to avoid duplicating declaration files, noting this works for named exports but can cause default export issues
 * [later](https://github.com/microsoft/TypeScript-go/issues/3347#issuecomment-4198818076) **abrahamguo** asked why direct imports from @eslint/config-helpers did not reproduce the issue and suggested that eslint/lib/types/config-api.d.ts might be responsible
 * [later](https://github.com/microsoft/TypeScript-go/issues/3347#issuecomment-4200241330) **andrewbranch** assumed the import was from an ESM file and explained the resolved import path

### [Issue microsoft/TypeScript-go#3348](https://github.com/microsoft/TypeScript-go/issues/3348) (Open, `Domain: Editor`, **andrewbranch**)

**Auto import adds duplicate imports for namespace exports**

*VS Code auto-import adds duplicate namespace imports for a namespaced export, causing a duplicate identifier error.*

 * created by **yume-chan**
 * **yume-chan** added label `Domain: Editor`
 * **RyanCavanaugh** assigned to **andrewbranch**

### [PR microsoft/TypeScript-go#3349](https://github.com/microsoft/TypeScript-go/pull/3349) (Open)

**Add Go to Source Definition**

*Add Go to Source Definition feature using a no-dts resolver with client-side commands, server-side toggles, and tests*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#3350](https://github.com/microsoft/TypeScript-go/pull/3350) (Open)

**Fix dts porting bug**

*The DTS port misinterprets the syntax list as an external module indicator, although it causes no problems.*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#3351](https://github.com/microsoft/TypeScript-go/pull/3351) (Closed)

**Fix specifiers for declaration files**

*Restore missing code to correct specifiers in TypeScript declaration files.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3352](https://github.com/microsoft/TypeScript-go/pull/3352) (Open)

**Fix export default dts widening**

*Prevent widening of export default assignments in .d.ts serialization and fix literal type handling broken by the big shortcut.*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#3353](https://github.com/microsoft/TypeScript-go/pull/3353) (Open)

**Re\-add incremental mode diagnostic chain repopulation**

*Reintroduce diagnostic chain repopulation in incremental mode to ensure stable incremental results.*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#3354](https://github.com/microsoft/TypeScript-go/pull/3354) (Open, **jakebailey**, **Copilot**)

**Fix panic in declaration emit for named CommonJS exports from \.cjs files**

*Add missing diagnostic context in transformCommonJSExport to prevent declaration emit panics for named CommonJS exports in .cjs files.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#3355](https://github.com/microsoft/TypeScript-go/pull/3355) (Open)

**Switch to new CI runner system**

*Adopt a new CI runner system to address current issues, leveraging its compatibility with our single-image pools.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3355#issuecomment-4195301938) **jakebailey** said "This won't work without a pool change (so far)"

### [PR microsoft/TypeScript-go#3356](https://github.com/microsoft/TypeScript-go/pull/3356) (Open)

**Update readme status table**

*Update the README status table because it has not been updated in a while.*

 * created by **jakebailey**

### [Issue microsoft/TypeScript-go#3357](https://github.com/microsoft/TypeScript-go/issues/3357) (Open, `Crash`)

**Nil pointer derefence in \`\(\*NodeBuilderImpl\)\.addPropertyToElementList\` with  \`\-\-tsBuildInfoFile\`**

*A nil pointer dereference occurs in NodeBuilderImpl.addPropertyToElementList when running with the --tsBuildInfoFile option.*

 * created by **LukeAbby**
 * **LukeAbby** added label `Crash`

### [PR microsoft/TypeScript-go#3358](https://github.com/microsoft/TypeScript-go/pull/3358) (Open)

**Implement LSP\-based code edits with file renaming**

*Add support for performing Language Server Protocol code edits that include automatic file renaming handling.*

 * created by **Andarist**

### [PR microsoft/TypeScript-go#3359](https://github.com/microsoft/TypeScript-go/pull/3359) (Open)

**Properly recognize all symbol flags on imported reexported symbols in completions code**

*Enhance completions code to correctly detect all symbol flags on imported and reexported symbols.*

 * created by **Andarist**

