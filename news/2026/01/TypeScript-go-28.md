# Report for 2026-01-28 (Wednesday, January 28th, 2026)

17 different users commented on 20 different issues.

## Recommended Actions

 * Response Recommended
    * @scarf005 asked what to do to fix a panic error when running tsgo typecheck in [microsoft/TypeScript-go#1531](https://github.com/microsoft/TypeScript-go/issues/1531#issuecomment-3815132905)
    * @valentinmelusson asked for a rough ETA on adding the isolated declarations errors in [microsoft/TypeScript-go#2427](https://github.com/microsoft/TypeScript-go/issues/2427#issuecomment-3816683513)
    * @tats-u asked if Corsa could inherit JSDoc for the top overload declaration like Strada in [microsoft/TypeScript-go#2599](https://github.com/microsoft/TypeScript-go/issues/2599#issuecomment-3815144737)

## Activity Summary

### [Issue microsoft/TypeScript-go#1531](https://github.com/microsoft/TypeScript-go/issues/1531) (Open, `Crash`, `Domain: Program`, **sheetalkamat**)

**tsgo panics with invalid UTF\-8 when marshalling build info**

*tsgo panics during build info marshalling because it encounters invalid UTF-8 in diagnostic messages.*

 * **jakebailey** added label `Domain: Program`
 * **RyanCavanaugh** assigned to **sheetalkamat**
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1531#issuecomment-3746812464) **gabritto** said "Related: #2336"
 * [today](https://github.com/microsoft/TypeScript-go/issues/1531#issuecomment-3815132905) **scarf005** asked what to do to fix a panic error in tsgo typecheck and reported that removing .tsbuildinfo did not help

### [Issue microsoft/TypeScript-go#1622](https://github.com/microsoft/TypeScript-go/issues/1622) (Closed, `Crash`, `Domain: Program`, `Domain: Performance`, **sheetalkamat**)

**\[bug\] \`tsgo \-\-build\` uses extreme amounts of memory**

*tsgo --build exhausts over 100GB of memory and crashes when building large monorepos with thousands of TypeScript projects*

 * [1 month ago](https://github.com/microsoft/TypeScript-go/issues/1622#issuecomment-3700541007) **spanishpear** noted similar performance struggles in tsgolint and pointed to a related issue for potential resolution
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1622#issuecomment-3718503020) **rubenferreira97** reported experiencing a process deadlock when running tsgo --build and provided a log file and project configuration details
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1622#issuecomment-3720038671) **jakebailey** said "@rubenferreira97 that is totally unrelated to this issue; please file a new issue with a repro."
 * [today](https://github.com/microsoft/TypeScript-go/issues/1622#issuecomment-3814613904) **sheetalkamat** said "Can you please try build from https://github.com/microsoft/typescript-go/pull/2604 to see if it helps"

### [Issue microsoft/TypeScript-go#2243](https://github.com/microsoft/TypeScript-go/issues/2243) (Closed, `Crash`, **sheetalkamat**)

**Crash in incremental**

*Tsgo incremental crashes on a specific branch, temporarily fixed by disabling incremental or switching @typescript/native-preview versions.*

 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/2243#issuecomment-3801827440) **jakebailey** said "I don't think this is crashing anymore, on main."
 * (2 days ago) **jakebailey** closed the issue
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/2243#issuecomment-3801828260) **jakebailey** said "@justinsmid "
 * [later](https://github.com/microsoft/TypeScript-go/issues/2243#issuecomment-3816869800) **justinsmid** reported that they have not encountered the issue recently and will open a new issue if it recurs

### [PR microsoft/TypeScript-go#2331](https://github.com/microsoft/TypeScript-go/pull/2331) (Open)

**Organize Imports**

*Implement functionality to automatically organize and sort imports within source files.*

 * created by **johnfav03**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2331#issuecomment-3812744149) **jakebailey** said "Has this been tested in the editor itself yet?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2331#issuecomment-3813168824) **johnfav03** recommitted the change to CodeActionProvider and tested it locally in the editor using the VSCode codebase
 * [today](https://github.com/microsoft/TypeScript-go/pull/2331#issuecomment-3814667929) **jakebailey** tested import organizing and found the shebang repeated before each import
 * [today](https://github.com/microsoft/TypeScript-go/pull/2331#issuecomment-3814678385) **jakebailey** reported import reorganization and indentation loss in two TypeScript files

### [Issue microsoft/TypeScript-go#2383](https://github.com/microsoft/TypeScript-go/issues/2383) (Closed, `Domain: Editor`, **gabritto**)

**LSP: Path suggestion missing \(import/export\)**

*Path completion suggestions for import/export statements are missing in tsgo, unlike in TypeScript 5.9.*

 * [6 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2383#issuecomment-3657318588) **andrewbranch** said "Yes and no; we have a list of failing/differing tests, and I traced these to a function that was empty except for a code comment."
 * **andrewbranch** unassigned **andrewbranch**
 * **DanielRosenwasser** added label `Domain: Editor`
 * (today) **gabritto** closed the issue

### [Issue microsoft/TypeScript-go#2427](https://github.com/microsoft/TypeScript-go/issues/2427) (Open, `bug`)

**\`isolatedDeclarations\` is not yet implemented**

*tsgo does not implement the isolatedDeclarations compiler option, so it fails to report missing annotations unlike tsc 5.9.*

 * **DanielRosenwasser** added label `bug`
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2427#issuecomment-3720630512) **jakebailey** said "See also #1693, #2459"
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2427#issuecomment-3731130416) **jakebailey** said "To be clear, the linked issue adds some of the code to start getting us there, but not the errors."
 * [later](https://github.com/microsoft/TypeScript-go/issues/2427#issuecomment-3816683513) **valentinmelusson** asked for a rough ETA on adding isolated declarations errors support

### [PR microsoft/TypeScript-go#2434](https://github.com/microsoft/TypeScript-go/pull/2434) (Open)

**Experiment: Quantified Types**

*Seeking a TypeScript function signature to consume an array of heterogeneous Layer objects without collapsing distinct generics.*

 * [5 days ago](https://github.com/microsoft/TypeScript-go/pull/2434#issuecomment-3793031614) **clinuxrulz** proposed an effect pipe example and stated it could only be implemented via existential types
 * [4 days ago](https://github.com/microsoft/TypeScript-go/pull/2434#issuecomment-3794171335) **devanshj** suggested implementing `pipe` without existential types using finite overloads and provided example links
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2434#issuecomment-3808239583) **clinuxrulz** observed that types weren't inferred in the chain and provided an infinite params example
 * [today](https://github.com/microsoft/TypeScript-go/pull/2434#issuecomment-3812220747) **devanshj** acknowledged that the finite one infers the types and called the infinite example silly

### [Issue microsoft/TypeScript-go#2490](https://github.com/microsoft/TypeScript-go/issues/2490) (Closed, `Crash`, **ahejlsberg**, **Copilot**)

**Completions panic \(nil pointer\) in JSDoc union return type of method with params**

*Completions request causes a nil pointer panic in the language server for JSDoc function types with union return types.*

 * **DanielRosenwasser** assigned to **DanielRosenwasser**
 * (2 days ago) **ahejlsberg** assigned to **ahejlsberg**, and unassigned **DanielRosenwasser**
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#2580](https://github.com/microsoft/TypeScript-go/issues/2580) (Closed, `Crash`, **DanielRosenwasser**, **Copilot**)

**textDocument/completion runtime error: invalid memory address or nil pointer dereference**

*textDocument/completion handler in the TypeScript-Go language server panics with a nil pointer dereference when computing import statement completions.*

 * **DanielRosenwasser** assigned to **DanielRosenwasser**
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2580#issuecomment-3803855923) **sanny-io** thanked the maintainer and apologized for not narrowing down the crash context
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2580#issuecomment-3806975306) **DanielRosenwasser** said "Don't sweat it! Sorry, I wasn't trying to say your repro wasn't helpful, it was more for the agent 😄"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2580#issuecomment-3812635338) **gabritto** said "Fixed by #2589."
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript-go#2586](https://github.com/microsoft/TypeScript-go/pull/2586) (Closed)

**Consistently map reparsed JSDoc nodes in \`GetReparsedNodeForNode\`**

*Track and map reparsed JSDoc node clones to ensure GetReparsedNodeForNode and related checker functions use them for consistent symbol assignment*

 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/2586#issuecomment-3802616759) **DanielRosenwasser** said "@copilot try again"
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/2586#issuecomment-3802617084) **Copilot** said "@DanielRosenwasser I've opened a new pull request, #2588, to work on those changes. Once the pull request is ready, I'll request review from you."
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2586#issuecomment-3805820822) **ahejlsberg** explained that checker methods should guard on nodes and retrieve reparsed nodes when relevant, noting only declaration names and type nodes are reparsed and expression nodes need no remapping
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#2587](https://github.com/microsoft/TypeScript-go/pull/2587) (Closed)

**Module specifier completions**

*Port module specifier completion logic to support relative and non-relative imports while planning future registry-based optimizations.*

 * created by **gabritto**
 * (today) **gabritto** closed the issue

### [Issue microsoft/TypeScript-go#2598](https://github.com/microsoft/TypeScript-go/issues/2598) (Closed, `Crash`, **iisaduan**)

**Auto\-imports broken in JS files when user preferences are used**

*Applying user preferences in JavaScript files causes auto-import suggestions to fail and trigger a panic in the TypeScript-Go server*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2598#issuecomment-3809217241) **DanielRosenwasser** reported a panic error when opening in a Codespace environment related to auto imports
 * (yesterday) **DanielRosenwasser** assigned to **Copilot**, **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2598#issuecomment-3814398057) **andrewbranch** reported inability to reproduce the issue and attached a screenshot
 * [today](https://github.com/microsoft/TypeScript-go/issues/2598#issuecomment-3814441202) **andrewbranch** said "Which of these things can you reproduce reliably? I can think of some fixes/improvements, but no way to write a reliable repro."
 * [today](https://github.com/microsoft/TypeScript-go/issues/2598#issuecomment-3814516402) **DanielRosenwasser** described consistent reproduction steps using a codespace from microsoft/vscode by pasting `PictureInPictureEvent` and requesting completions
 * [today](https://github.com/microsoft/TypeScript-go/issues/2598#issuecomment-3814599660) **andrewbranch** explained that he couldn’t reproduce locally due to stale code, identified that issue #2370 caused the auto-import registry to always use TypeScript-specific preferences even for JavaScript files, realized the TS/JS preference split was confusing, and suggested cleaning up the settings handling in v7.0
 * [today](https://github.com/microsoft/TypeScript-go/issues/2598#issuecomment-3814607950) **andrewbranch** speculated that few users would set different auto-import preferences per file type and realized that most would likely only define it for a single language
 * [today](https://github.com/microsoft/TypeScript-go/issues/2598#issuecomment-3814623664) **jakebailey** discussed issues with separate JS and TS settings, explained inability to determine user preference from fully resolved client settings, suggested unifying to a js/ts setting, and noted that onChangeConfiguration prevents overrides
 * [today](https://github.com/microsoft/TypeScript-go/issues/2598#issuecomment-3814624997) **iisaduan** said "Am I understanding it right that typescript..... settings being specified, a .js file is opened, and then autoimports is crashed because of the preferences mismatch?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2598#issuecomment-3814627589) **andrewbranch** described that completions asked for a registry with file-specific preferences but registry building unconditionally used config.TS(), and said that he was preparing a fix to have the Registry store combined preferences
 * [today](https://github.com/microsoft/TypeScript-go/issues/2598#issuecomment-3814635623) **iisaduan** noted that incorrect preferences likely caused a registry lookup failure and that javascript preferences should default to the typescript settings
 * [today](https://github.com/microsoft/TypeScript-go/issues/2598#issuecomment-3814639412) **jakebailey** clarified that the client always sends fully resolved options including defaults from package.json
 * [today](https://github.com/microsoft/TypeScript-go/issues/2598#issuecomment-3814649669) **iisaduan** said "I'll take a look. I remember it being nil but that was waaay back when I first made the RequestConfiguration command"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2598#issuecomment-3814649929) **andrewbranch** explained that GetPreferences checks if the .js property is nil but noted it is always initialized via CopyOrDefault in NewUserConfig and Copy
 * [today](https://github.com/microsoft/TypeScript-go/issues/2598#issuecomment-3814667686) **iisaduan** said "Makes sense-- one too many .CopyOrDefaults. I'm debugging it now"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2598#issuecomment-3814671027) **andrewbranch** concluded that storing the whole UserConfig on the Registry didn’t make sense, identified two bugs, and agreed to abandon the changes and consider killing the pattern
 * (today) **andrewbranch** assigned to **iisaduan**, and unassigned **DanielRosenwasser**, **andrewbranch**, **Copilot**

### [Issue microsoft/TypeScript-go#2599](https://github.com/microsoft/TypeScript-go/issues/2599) (Closed, `bug`, **ahejlsberg**, **Copilot**)

**JSDoc for overloads and implementation is not displayed**

*VS Code TS Native Preview fails to show JSDoc for non-top overloads and implementation of overloaded TypeScript functions.*

 * (yesterday) **DanielRosenwasser** assigned to **Copilot**, **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2599#issuecomment-3811719304) **ahejlsberg** explained that the changes to overload count display were intentional and compared how Strada and Corsa show overload information
 * [today](https://github.com/microsoft/TypeScript-go/issues/2599#issuecomment-3815144737) **tats-u** said "I see, but the disappearance of JSDoc matters much more. Can Corsa inherit the JSDoc for the top overload declaration like Strada (include 6)?"
 * [later](https://github.com/microsoft/TypeScript-go/issues/2599#issuecomment-3818238847) **ahejlsberg** agreed that Corsa should inherit the JSDoc for the top overload declaration like Strada

### [PR microsoft/TypeScript-go#2600](https://github.com/microsoft/TypeScript-go/pull/2600) (Closed, **DanielRosenwasser**, **Copilot**)

**Fix race conditions in auto\-imports causing server crashes**

*Fix race conditions in auto-import handling by filtering nil project references and retrying completions without imports to prevent server crashes.*

 * created by **Copilot**
 * (yesterday) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#2603](https://github.com/microsoft/TypeScript-go/pull/2603) (Closed, **sheetalkamat**, **Copilot**)

**Remove unused entriesCount from parseCache**

*Removed unused entriesCount field and atomic import from parseCache, eliminating dead code.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **sheetalkamat**
 * (today) **sheetalkamat** closed the issue

### [PR microsoft/TypeScript-go#2604](https://github.com/microsoft/TypeScript-go/pull/2604) (Closed)

**Some of the changes to improve \-\-build memory footprint**

*Improved build memory footprint by fixing writerPool retention, restricting source file caching to d.ts/json, and adjusting builder concurrency flag.*

 * created by **sheetalkamat**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2604#issuecomment-3816025185) **Zzzen** said "Would you mind pushing a beta build? I’d love to give it a spin."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2604#issuecomment-3816055377) **jakebailey** said "We don't have a way to do that; you'd have to build from source"
 * [later](https://github.com/microsoft/TypeScript-go/pull/2604#issuecomment-3816395284) **Zzzen** reported continuing to encounter OOM errors and noticed that tsgo consumed significantly more memory compared to tsc

### [PR microsoft/TypeScript-go#2605](https://github.com/microsoft/TypeScript-go/pull/2605) (Closed)

**Diff \`findAllReferences\`**

*Compute baseline diffs for findAllReferences results to streamline pull request reviews.*

 * created by **gabritto**

### [Issue microsoft/TypeScript-go#2606](https://github.com/microsoft/TypeScript-go/issues/2606) (Closed, **gabritto**)

**Module specifier completion icons are lazily loaded/generic until item selection**

*Module import suggestions in IntelliSense initially display generic icons and only update to actual file-type icons after selection.*

 * created by **rubenferreira97**
 * **jakebailey** assigned to **gabritto**

### [Issue microsoft/TypeScript-go#961](https://github.com/microsoft/TypeScript-go/issues/961) (Open, `bug`, `Domain: Emit`, `Domain: Type Checking`, **jakebailey**)

**tsgo fails to resolve namespace symbols in non\-extends contexts across files**

*tsgo fails to qualify namespace symbols A and Afunc outside extends contexts across files, causing incorrect JS and runtime errors.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/961#issuecomment-3808167779) **dtscd** mentioned struggling to understand the use case for namespaces in TypeScript given file-based organization requiring re-annotation on refactor
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/961#issuecomment-3808175525) **jakebailey** explained typical uses of namespaces and asked for clarification on re-annotating namespace decorations
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/961#issuecomment-3808188925) **dtscd** described moving code between files under the same namespace and the extra annotation needed if namespaces no longer merged across files
 * [later](https://github.com/microsoft/TypeScript-go/issues/961#issuecomment-3817986645) **magic-akari** described expected compiler error output

