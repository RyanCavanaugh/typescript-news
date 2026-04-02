# Report for 2025-12-09 (Tuesday, December 9th, 2025)

24 different users commented on 55 different issues.

## Recommended Actions

 * Response Recommended
    * @Azzerty23 said they would open a PR for Better Auth in [microsoft/TypeScript-go#2162](https://github.com/microsoft/TypeScript-go/issues/2162#issuecomment-3633624829)
    * @safareli reported having the same issue with pnpm in [microsoft/TypeScript-go#2233](https://github.com/microsoft/TypeScript-go/issues/2233#issuecomment-3633964119)
    * @abelcha provided process samples for investigation in [microsoft/TypeScript-go#2239](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3633459027)
    * @GitMurf asked whether the tsgo port has implemented didRenameFiles in [microsoft/TypeScript-go#2244](https://github.com/microsoft/TypeScript-go/issues/2244#issuecomment-3633179151)
    * @GitMurf asked if there was a decision on how tsgo will implement file rename/move LSP methods and offered to help test in [microsoft/TypeScript-go#2244](https://github.com/microsoft/TypeScript-go/issues/2244#issuecomment-3633217310)
    * @maishivamhoo123 asked to be assigned to the issue in [microsoft/TypeScript-go#2306](https://github.com/microsoft/TypeScript-go/issues/2306#issuecomment-3635317555)

## Activity Summary

### [Issue microsoft/TypeScript-go#1622](https://github.com/microsoft/TypeScript-go/issues/1622) (Open, `Crash`, `Domain: Program`, `Domain: Performance`, **sheetalkamat**)

**\[bug\] \`tsgo \-\-build\` uses extreme amounts of memory**

*tsgo --build exhausts over 100GB of memory and crashes when building large monorepos with thousands of TypeScript projects*

 * [11 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1622#issuecomment-3323629265) **mjames-c** cross-posted a reference, noted high memory usage but no longer OOMed, and asked if the default for --maxConcurrentProjects equals the number of CPU cores
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/1622#issuecomment-3628462817) **maxkostow** mentioned that the LSP lacked --singleThreaded support, described tuning GOGC/GOMEMLIMIT via the VS Code extension, and suggested exposing these settings until better defaults exist
 * [today](https://github.com/microsoft/TypeScript-go/issues/1622#issuecomment-3632620368) **Knagis** reported the same issue with high memory usage and OOM when building ~1000 TS projects and noted that using --singleThreaded worked fine and remained faster than tsc
 * [today](https://github.com/microsoft/TypeScript-go/issues/1622#issuecomment-3633202774) **jakebailey** said "@sheetalkamat Can you resurrect your change to limit the number of concurrent project builds? We have --checkers, but I think we were also wanting to add --builders to control that number."

### [PR microsoft/TypeScript-go#1721](https://github.com/microsoft/TypeScript-go/pull/1721) (Closed)

**Add \`@types/node\` to extension**

*Add @types/node to the extension to support type definitions for Node’s path module.*

 * created by **mjbvz**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/1721#issuecomment-3630535269) **jakebailey** said "Is this PR still needed? The repo root has @types/node already."
 * (today) **mjbvz** closed the issue

### [PR microsoft/TypeScript-go#1793](https://github.com/microsoft/TypeScript-go/pull/1793) (Closed)

**added gating for user preferences for auto imports**

*Introduces and tests new user preferences for auto-import behaviors including specifier style, exclusions, and path renaming.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1793#issuecomment-3564502868) **jakebailey** said "Is the test generator just missing these options such that all tests are new handwritten ones?"
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1793#issuecomment-3571968884) **johnfav03** asked if the test generator lacked options requiring all handwritten tests and noted that Isabel said to use BaselineAutoImportsCompletions because the codefixProvider hadn't been ported
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1793#issuecomment-3572276025) **andrewbranch** said "Codefixes were ported in #2053 "
 * (today) **johnfav03** closed the issue

### [Issue microsoft/TypeScript-go#1882](https://github.com/microsoft/TypeScript-go/issues/1882) (Open, `Needs More Info`)

**Renaming/moving file breaks imports**

*Renaming a TypeScript file in tsgo leads to TS6307 errors due to missing project file listing, unlike TypeScript 5.8.*

 * **jakebailey** removed label `Domain: Editor`
 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1882#issuecomment-3476196383) **jakebailey** said "This isn't enough info to diagnose; did this happen in the editor? In watch mode?"
 * **jakebailey** added label `Needs More Info`
 * [today](https://github.com/microsoft/TypeScript-go/issues/1882#issuecomment-3633334604) **GitMurf** added a note to help others encountering the same issue
 * [today](https://github.com/microsoft/TypeScript-go/issues/1882#issuecomment-3633341647) **jakebailey** suggested that file change/watch updates should suffice instead of didRenameFiles and requested LSP logs
 * [today](https://github.com/microsoft/TypeScript-go/issues/1882#issuecomment-3633387689) **GitMurf** confirmed correct behavior in VSCode and Neovim and stated intent to update the earlier comment

### [PR microsoft/TypeScript-go#1965](https://github.com/microsoft/TypeScript-go/pull/1965) (Open)

**Fix various module emit differences**

*Address multiple discrepancies in module emissions discovered while reviewing issue #1963.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/1965#issuecomment-3634728277) **jakebailey** said "I think this is reviewable now."

### [Issue microsoft/TypeScript-go#2127](https://github.com/microsoft/TypeScript-go/issues/2127) (Closed, `Crash`, **Copilot**)

**Panics when extra closing JSX tag**

*TypeScript-Go language server panics with an interface conversion error when encountering an extra closing JSX tag during code completion.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2127#issuecomment-3559043771) **jakebailey** showed a panic in isThis caused by an unexpected interface conversion despite guarding Text() calls by KindIdentifier
 * **jakebailey** removed label `Needs More Info`
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2127#issuecomment-3568394196) **ahejlsberg** said "Sounds like some code somewhere is calling factory.NewToken(ast.Identifier)!"
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript-go#2142](https://github.com/microsoft/TypeScript-go/pull/2142) (Closed)

**Place DO NOT EDIT comment on top of generated fourslash tests**

*Add a DO NOT EDIT comment to generated fourslash test files so Go tooling, GitHub diffs, and Copilot ignore them.*

 * created by **jakebailey**
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2142#issuecomment-3563504869) **gabritto** said "Did the conversion script fail to format?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2142#issuecomment-3633466011) **jakebailey** suggested updating the Copilot instructions since generated files aren't formatted and changes would cause unnecessary churn
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2162](https://github.com/microsoft/TypeScript-go/issues/2162) (Closed, `Domain: Type Checking`, **ahejlsberg**)

**Type inference lost for callback parameter**

*Using ts-go configuration causes TypeScript to lose type inference for the organization plugin's sendInvitationEmail callback parameter.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2162#issuecomment-3627832636) **jakebailey** noted that bisect identified TypeScript pull request #58910 as the change, which backported a fix from the Go code that also addressed multiple TS issues Andarist had been working on
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2162#issuecomment-3628193990) **Andarist** noted that the change introduced a return type inference regression affecting contextual types, demonstrated by making 'options' non-optional, and suggested there might be a better fix
 * [today](https://github.com/microsoft/TypeScript-go/issues/2162#issuecomment-3632929653) **Azzerty23** demonstrated that removing optionality in the failing example made it work and provided a TS playground link
 * [today](https://github.com/microsoft/TypeScript-go/issues/2162#issuecomment-3633044512) **Andarist** explained that FilterMatching produced Record<string, any> for an optional-property constraint but never for a required-property constraint, illustrating how required properties make Record<string, any> incompatible
 * [today](https://github.com/microsoft/TypeScript-go/issues/2162#issuecomment-3633194332) **Azzerty23** said "I understand better, thank you for the detailed explanation!"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2162#issuecomment-3633253412) **ahejlsberg** explained that TypeScript uses parameter and return type inferences before applying constraints, described why the example infers Record<string, any> instead of OrganizationOptions, and suggested using a NoInfer marker in the return type of organization as a fix
 * [today](https://github.com/microsoft/TypeScript-go/issues/2162#issuecomment-3633624829) **Azzerty23** thanked maintainers for the clear breakdown and said they would open a PR for Better Auth and let the team close the issue

### [PR microsoft/TypeScript-go#2191](https://github.com/microsoft/TypeScript-go/pull/2191) (Closed)

**fix: Enable getExePath to work on Node 16**

*Enable getExePath compatibility on Node 16 to restore tsgo preview functionality*

 * [6 days ago](https://github.com/microsoft/TypeScript-go/pull/2191#issuecomment-3607619015) **jakebailey** said "There is, in _packages/native-preview/package.json."
 * [6 days ago](https://github.com/microsoft/TypeScript-go/pull/2191#issuecomment-3610150040) **aapoalas** thanked for pointing out the file location and fixed the package.json and formatting check
 * [today](https://github.com/microsoft/TypeScript-go/pull/2191#issuecomment-3631638131) **aapoalas** said "@jakebailey my apologies for the ping; need workflow approval at least :)"
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2204](https://github.com/microsoft/TypeScript-go/issues/2204) (Closed, `Domain: Editor`)

**\[bug\] TSGO fails to follow re\-exports when finding references**

*TSGO does not follow re-exports when finding references, preventing accurate cross-module symbol resolution.*

 * created by **mjames-c**
 * **mjames-c** added label `Domain: Editor`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2204#issuecomment-3632975979) **RohinBhargava** said "+1"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2204#issuecomment-3633373190) **jakebailey** said "https://github.com/microsoft/typescript-go/pull/2304 should fix this. One missing function, one flipped condition."
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2227](https://github.com/microsoft/TypeScript-go/issues/2227) (Open, `Domain: Editor`)

**Port \`move to file\` refactoring**

*Reintroduce the Move to file refactoring from TypeScript 6 into the language server to restore essential automated code relocation functionality.*

 * created by **mjbvz**
 * **jakebailey** added label `Domain: Editor`

### [Issue microsoft/TypeScript-go#2228](https://github.com/microsoft/TypeScript-go/issues/2228) (Open, `Domain: Editor`, **gabritto**)

**No JS Doc template completions**

*The ts-go extension lacks support for the JSDoc template completion feature introduced in TypeScript 6.0 for VSCode.*

 * created by **mjbvz**
 * **gabritto** assigned to **gabritto**
 * **jakebailey** added label `Domain: Editor`

### [Issue microsoft/TypeScript-go#2229](https://github.com/microsoft/TypeScript-go/issues/2229) (Open, `Domain: Editor`, **Copilot**)

**Should not allow renaming keywords**

*TS-go erroneously permits renaming on keywords and parentheses instead of failing early via prepareRename*

 * created by **mjbvz**
 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/2229#issuecomment-3614402370) **mjbvz** said "In 6.0 we do allow triggering renames on class and similar keywords but this shifts the rename to the class name instead"
 * **jakebailey** assigned to **Copilot**
 * **jakebailey** added label `Domain: Editor`

### [Issue microsoft/TypeScript-go#2230](https://github.com/microsoft/TypeScript-go/issues/2230) (Open, `Domain: Editor`, **Copilot**)

**Should not allow renaming parts of the standard library**

*Prevent users from renaming built-in standard library functions like setTimeout.*

 * (5 days ago) **mjbvz** added label `Crash`, and removed label `Crash`
 * **jakebailey** assigned to **Copilot**
 * **jakebailey** added label `Domain: Editor`

### [Issue microsoft/TypeScript-go#2233](https://github.com/microsoft/TypeScript-go/issues/2233) (Open, `Domain: Declaration Emit`, **weswigham**)

**Project references indirect dependencies: Error 2742 Inferred type of xxx \.\.\.**

*tsgo reports a TS2742 error when a package infers a type from an indirect project reference without directly referencing the originating package*

 * created by **johnpyp**
 * (4 days ago) **ahejlsberg** added label `Domain: Declaration Emit`, and assigned to **weswigham**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2233#issuecomment-3633964119) **safareli** said "have same issue with pnpm"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2233#issuecomment-3633988288) **dimitraz** said "Likewise"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2233#issuecomment-3634836621) **sanny-io** said "@dimitraz @samdcoding please use the thumbs up instead. It is more considerate of subscribers watching issues."

### [Issue microsoft/TypeScript-go#2239](https://github.com/microsoft/TypeScript-go/issues/2239) (Open, `Needs More Info`)

**take too much memory**

*tsgo extension consumes about 17GB of RAM on macOS M1, causing heavy swapping and slowing VS Code.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3628151855) **jakebailey** said "No, there is no equivalent to that. #1808 perhaps."
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3628246716) **maxired** confirmed that running vscode with the GOMEMLIMIT variable set worked, noted that 2048MiB was sufficient, and said they would report any further crashes
 * [today](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3631565394) **maxired** said "Actually even with GOMEMLIMIT=2048MiB, after half a day working, my tsgo would eat 13GB of ram, while I have only 6 files opened in vscode"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3633459027) **abelcha** explained that the setting did not apply with the native preview extension, noted that Node was not involved in launching the language server, suggested tsgo was not enabled, proposed a cursor issue, and attached process samples

### [Issue microsoft/TypeScript-go#2244](https://github.com/microsoft/TypeScript-go/issues/2244) (Open, `Domain: Editor`)

**Port \`update imports on file rename/move\` support**

*Request to port support for automatically updating imports when files are renamed or relocated*

 * **mjbvz** added label `Crash`
 * **gabritto** removed label `Crash`
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/2244#issuecomment-3619129053) **mmgeorge** said "Just tried tsgo's ls today and ran into this as well. It's unbelievably faster on our codebase though! Tempted to stick with it for now and just swap ls when I need to do a bunch of file renaming. "
 * [today](https://github.com/microsoft/TypeScript-go/issues/2244#issuecomment-3633179151) **GitMurf** asked why LSP renaming via workspace/didRenameFiles did not work and whether the tsgo port has not implemented didRenameFiles
 * [today](https://github.com/microsoft/TypeScript-go/issues/2244#issuecomment-3633188170) **jakebailey** said "Yes, this LSP method is not implemented yet."
 * **jakebailey** added label `Domain: Editor`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2244#issuecomment-3633217310) **GitMurf** asked if there was a discussion on how tsgo will implement file rename LSP methods and offered to help test from a Neovim perspective
 * [today](https://github.com/microsoft/TypeScript-go/issues/2244#issuecomment-3633225247) **jakebailey** said "I assume we'd do it the same way as VS Code, just over LSP (which LSP is mostly a thin wrapper over)."

### [PR microsoft/TypeScript-go#2259](https://github.com/microsoft/TypeScript-go/pull/2259) (Open, **DanielRosenwasser**, **Copilot**)

**Fix nil pointer dereference in completion at property start after JSDoc**

*Fixed a nil pointer panic when requesting completions at a JSDoc-preceded property start by correcting variable shadowing, adding a nil check, and adding a regression test.*

 * created by **Copilot**
 * (3 days ago) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2259#issuecomment-3634678530) **DanielRosenwasser** requested the location of the tests and suggested merging from upstream and rerunning `hereby generate`
 * [today](https://github.com/microsoft/TypeScript-go/pull/2259#issuecomment-3634739558) **Copilot** added a test in TestCompletionJSDocBeforePropertyNoCrash for the crash scenario and merged from main with code generation run

### [PR microsoft/TypeScript-go#2264](https://github.com/microsoft/TypeScript-go/pull/2264) (Closed)

**Fix empty wildcard match on exports**

*Wildcard package.json exports with empty matches (e.g., './foo/*/index.js') cause a slice bounds out-of-range panic when resolving imports*

 * created by **lauckhart**
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/2264#issuecomment-3622535929) **lauckhart** agreed with microsoft-github-policy-service
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2264#issuecomment-3629388944) **jakebailey** asked if a test could be added for the fix and suggested replicating the original code approach
 * [today](https://github.com/microsoft/TypeScript-go/pull/2264#issuecomment-3634311515) **lauckhart** added coverage tests in specifiers_test.go and noted a potential false positive in the original code’s prefix/suffix matching
 * [today](https://github.com/microsoft/TypeScript-go/pull/2264#issuecomment-3634471641) **jakebailey** questioned whether splitting the string before checking avoided the false positive
 * [today](https://github.com/microsoft/TypeScript-go/pull/2264#issuecomment-3634605544) **lauckhart** explained that independent startsWith and endsWith checks cause 'foo/*/index.js' to match 'foo/index.js' and asked if this could cause problems in non-contrived scenarios
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2272](https://github.com/microsoft/TypeScript-go/pull/2272) (Open)

**Revamp user preferences serialization/deserialization**

*Refactor user preferences serialization to use struct tags and reflection enabling JSON round-trip and nested configurations.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2272#issuecomment-3634599760) **jakebailey** said "I think I'm going to wait for the other two user pref related PRs to finish and just fix this PR instead of forcing that on everyone."

### [Issue microsoft/TypeScript-go#2279](https://github.com/microsoft/TypeScript-go/issues/2279) (Open, `Domain: Editor`, **gabritto**)

**Add snippet completions for methods**

*Implement snippet completions in ts-go so selecting a base class method suggestion inserts its full signature and stub.*

 * created by **mjbvz**
 * **gabritto** assigned to **gabritto**
 * **jakebailey** added label `Domain: Editor`

### [Issue microsoft/TypeScript-go#2280](https://github.com/microsoft/TypeScript-go/issues/2280) (Open, `Domain: Editor`, **gabritto**)

**Port \`implement interface\` quick fix**

*Port the implement interface quick fix from TypeScript to TS-Go to provide automated interface implementation support.*

 * created by **mjbvz**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2280#issuecomment-3632504763) **Tyriar** said "This is up there with most used quick fixes."
 * **jakebailey** added label `Domain: Editor`

### [Issue microsoft/TypeScript-go#2281](https://github.com/microsoft/TypeScript-go/issues/2281) (Open, `Domain: Editor`)

**Port \`Convert parameters to destructed object\` refactoring**

*Assess porting of the Convert parameters to destructured object refactoring given its bugs and low usage or explore Copilot support.*

 * created by **mjbvz**
 * **jakebailey** added label `Domain: Editor`

### [Issue microsoft/TypeScript-go#2282](https://github.com/microsoft/TypeScript-go/issues/2282) (Open)

**Request for official prebuilt Windows binaries \(tsgo\.exe\) published via GitHub Releases, without requiring npm\.**

*Officially distribute Windows tsgo.exe binaries via GitHub Releases to enable TypeScript use without npm.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2282#issuecomment-3629095008) **jakebailey** said "Blazor? Are you just looking for a NuGet package?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2282#issuecomment-3630893984) **PaulHuizer** pondered delivering TsGo.exe via NuGet as an MsBuild target and suggested a tsgo.exe integrating into MsBuild to compile TypeScript
 * [today](https://github.com/microsoft/TypeScript-go/issues/2282#issuecomment-3631797657) **jakebailey** said "If you're using vue or any other lib, isn't it implied that you already are using npm?"
 * [later](https://github.com/microsoft/TypeScript-go/issues/2282#issuecomment-3636626028) **PaulHuizer** explained that they used Blazor SSR, Vue Global, and ES Modules, preferring TypeScript via TsGen for the BFF API, and that Node.js was only needed for TS compilation, with TsGo potentially eliminating the Node.js requirement

### [PR microsoft/TypeScript-go#2283](https://github.com/microsoft/TypeScript-go/pull/2283) (Closed)

**Fix perfromance when there's lots of error**

*Change DiagnosticsCollection to sort lazily before GetDiagnostics, replacing insertion sort to improve performance with many errors.*

 * created by **GabrielCastro**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2283#issuecomment-3629437536) **jakebailey** said "This looks fine, but you should run hereby format."
 * (yesterday) **jakebailey** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/2283#issuecomment-3635213002) **jakebailey** said "This turns out to be unsafe; it causes a data race when concurrently accessing processor diagnostics. We don't see the problem in main, though, only on a WIP branch I have for bringing back #2197."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2283#issuecomment-3635234359) **jakebailey** said "And, since it sorts the list on the fly, if something previously grabbed a list of diags (say, the global diags), and then they changed later, the list would potentially be concurrently modified."

### [Issue microsoft/TypeScript-go#2286](https://github.com/microsoft/TypeScript-go/issues/2286) (Closed, `Crash`, **Copilot**)

**Panic in completions request within import attributes**

*The TypeScript-Go language server panics when requesting completions inside import attribute syntax due to an unhandled AST.ImportAttribute case.*

 * created by **DanielRosenwasser**
 * (yesterday) **DanielRosenwasser** added label `Crash`, and assigned to **Copilot**
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#2293](https://github.com/microsoft/TypeScript-go/pull/2293) (Closed, **DanielRosenwasser**, **Copilot**)

**Fix panic in completions within import attributes**

*Replaced Node.Text() case with an explicit lambda in completions to prevent panics in import attribute suggestions.*

 * created by **Copilot**
 * (yesterday) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * (today) **DanielRosenwasser** closed the issue

### [Issue microsoft/TypeScript-go#2294](https://github.com/microsoft/TypeScript-go/issues/2294) (Closed, `Crash`, **DanielRosenwasser**)

**Crash for signature help in type arguments with any/unknown call target**

*Signature help for type arguments in calls with unknown or any targets crashes due to a nil pointer dereference.*

 * created by **DanielRosenwasser**
 * (yesterday) **DanielRosenwasser** added label `Crash`, and assigned to **DanielRosenwasser**
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#2295](https://github.com/microsoft/TypeScript-go/pull/2295) (Closed)

**Fix signature help crash for type arguments when call target is unresolved**

*Handle unresolved call targets to prevent signature help from crashing when type arguments are provided.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** closed the issue

### [Issue microsoft/TypeScript-go#2296](https://github.com/microsoft/TypeScript-go/issues/2296) (Closed, `Crash`, **Copilot**)

**Crash for completions after end of array literal when contextually typed by tuple**

*Requesting completions immediately after a tuple-typed array literal triggers an index out-of-range panic in the TypeScript-Go LSP*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** added label `Crash`, and assigned to **Copilot**
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#2297](https://github.com/microsoft/TypeScript-go/pull/2297) (Closed, **DanielRosenwasser**, **Copilot**)

**Fix completion crash after closing bracket in contextually\-typed array literals**

*Completion after a tuple-typed array literal’s closing bracket crashes due to unhandled CloseBracketToken causing an out-of-range error.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#2298](https://github.com/microsoft/TypeScript-go/pull/2298) (Closed)

**Format errors in \`\(\*Server\)\.recover\`\.**

*Formatting errors in the Server.recover method lead to incorrect data recovery.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** closed the issue

### [Issue microsoft/TypeScript-go#2301](https://github.com/microsoft/TypeScript-go/issues/2301) (Open, `Crash`, **andrewbranch**)

**Crash for value usage of type\-only import**

*TypeScript language service crashes when completing or resolving a type-only import used as a value.*

 * created by **DanielRosenwasser**
 * **DanielRosenwasser** added label `Crash`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2301#issuecomment-3632258226) **Twacqwq** suggested rewriting the logic in Go and linked to the relevant TypeScript code
 * **DanielRosenwasser** assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2301#issuecomment-3633621249) **DanielRosenwasser** suggested commenting out lines 2181-2183 in completions.go and leaving a // !!! comment
 * [today](https://github.com/microsoft/TypeScript-go/issues/2301#issuecomment-3634818717) **andrewbranch** said "This will all be deleted soon"

### [Issue microsoft/TypeScript-go#2303](https://github.com/microsoft/TypeScript-go/issues/2303) (Open)

**Silently stopped evaluating files\.**

*tsgo silently fails to report missing type references in .d.ts files, while the standard TypeScript extension still catches them.*

 * created by **tzjames**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2303#issuecomment-3631905884) **tzjames** reported that the service crashed more widely, then restarted and resumed working, and provided the error stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/2303#issuecomment-3633602059) **DanielRosenwasser** said "Does this happen in any .d.ts file in your project? Can you repro it with just a .d.ts file and a tsconfig.json?"

### [PR microsoft/TypeScript-go#2304](https://github.com/microsoft/TypeScript-go/pull/2304) (Closed)

**Fix getReferencedSymbolsForSymbol, implement getReferencesAtExportSpecifier**

*Port getReferencesAtExportSpecifier, correct the inverted condition in getReferencedSymbolsForSymbol, and enhance fourslash to display proper error messages.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2305](https://github.com/microsoft/TypeScript-go/pull/2305) (Closed)

**Update deps**

*A request to update the project's dependencies to address vulnerabilities found by npm audit.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2306](https://github.com/microsoft/TypeScript-go/issues/2306) (Closed, `Domain: Editor`, **ahejlsberg**)

**The \`@see\` JSDoc tag cannot create links from URLs**

*Hover tooltips for JSDoc @see URLs are rendered incorrectly and not clickable in the TS Native Preview extension.*

 * created by **csvn**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2306#issuecomment-3635317555) **maishivamhoo123** said "@team can you please assign this issue to me? i love to contribute to this ?"
 * [later](https://github.com/microsoft/TypeScript-go/issues/2306#issuecomment-3637419123) **csvn** suggested starting a PR and linking to the issue since non-maintainers are not usually assigned issues
 * [later](https://github.com/microsoft/TypeScript-go/issues/2306#issuecomment-3637524090) **jakebailey** said "You can't assign a non-member, no, and even if so: https://github.com/microsoft/TypeScript/blob/main/CONTRIBUTING.md#issue-claiming"
 * [later](https://github.com/microsoft/TypeScript-go/issues/2306#issuecomment-3637583842) **csvn** said "Ah, sorry. I hadn't read that part 😅 "

### [PR microsoft/TypeScript-go#2307](https://github.com/microsoft/TypeScript-go/pull/2307) (Closed)

**Add \-\-builders to limit number of projects can build concurrently**

*Introduce a --builders flag to limit how many projects can be built concurrently.*

 * created by **sheetalkamat**

### [PR microsoft/TypeScript-go#2308](https://github.com/microsoft/TypeScript-go/pull/2308) (Closed)

**Create tokens with the right data**

*Ensure GetOrCreateToken constructs tokens with appropriate data for each token kind to avoid crashes.*

 * created by **gabritto**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2308#issuecomment-3634304573) **DanielRosenwasser** said "I am pretty sure this might be related to https://github.com/microsoft/typescript-go/issues/2127"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2308#issuecomment-3634782727) **gabritto** said "Ok, hopefully I didn't forget anything this time."
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript-go#2309](https://github.com/microsoft/TypeScript-go/pull/2309) (Closed)

**Fix contextual type for array completions**

*Enhance array completion contextual typing to handle commas in non-literal argument lists and prevent incorrect spread index usage.*

 * created by **gabritto**
 * (today) **gabritto** closed the issue

### [Issue microsoft/TypeScript-go#2310](https://github.com/microsoft/TypeScript-go/issues/2310) (Open)

**TypeScript for \.Net Projects**

*Custom MSBuild targets file and instructions to compile TypeScript 7 in .NET projects with tsgo until official support arrives.*

 * created by **joj**

### [PR microsoft/TypeScript-go#2311](https://github.com/microsoft/TypeScript-go/pull/2311) (Closed)

**Genericize ref counting caches; fix extended config cache bug**

*Make reference-counted caches generic for shared use and fix a bug in extended config caching.*

 * created by **andrewbranch**

### [Issue microsoft/TypeScript-go#2312](https://github.com/microsoft/TypeScript-go/issues/2312) (Closed, `Crash`, **Copilot**)

**Signature help crash on call target when nested call has trailing comma**

*Quickly requesting signature help on a nested call expression with a trailing comma causes an index out-of-range panic.*

 * created by **DanielRosenwasser**
 * **DanielRosenwasser** added label `Crash`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2312#issuecomment-3635060135) **DanielRosenwasser** speculated that a semantic command raced with signature help causing it to sometimes use resolved data and making the issue hard to reproduce in the editor
 * [today](https://github.com/microsoft/TypeScript-go/issues/2312#issuecomment-3635144716) **DanielRosenwasser** provided a minimal repro example requesting signature help at a marker with generic outer and inner calls having trailing commas
 * **DanielRosenwasser** assigned to **Copilot**

### [Issue microsoft/TypeScript-go#2313](https://github.com/microsoft/TypeScript-go/issues/2313) (Closed, `bug`, `Domain: Editor`, **ahejlsberg**)

**Bare TypeScript code in \`@example\` is interpreted as Markdown/HTML**

*Unfenced TypeScript code in JSDoc @example tags is parsed as Markdown/HTML under tsgo, causing formatting issues.*

 * created by **tats-u**

### [PR microsoft/TypeScript-go#2314](https://github.com/microsoft/TypeScript-go/pull/2314) (Closed)

**Reapply Program diagnostic func update, CheckerPool cleanup**

*Reapply program diagnostic updates with concurrent per-file checking, thread-safe diagnostics collection, and CheckerPool cleanup.*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#2315](https://github.com/microsoft/TypeScript-go/pull/2315) (Closed, **DanielRosenwasser**, **Copilot**)

**Fix signature help crash when nested call has trailing comma**

*Signature help requests crash in nested calls with trailing commas due to an out-of-bounds argument index*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2315#issuecomment-3635766541) **Copilot** fixed the test to use the minimal repro with the correct marker position to reproduce the crash

### [Issue microsoft/TypeScript-go#2316](https://github.com/microsoft/TypeScript-go/issues/2316) (Closed, `Domain: Editor`)

**Using the TypeScript \(Native Preview\) extension, there is no smart implementation prompt in vscode**

*The TypeScript (Native Preview) extension in VS Code on Windows 11 fails to display the smart implementation prompt.*

 * created by **EnochGao**
 * **EnochGao** added label `Domain: Editor`
 * (later) **jakebailey** closed the issue
 * [later](https://github.com/microsoft/TypeScript-go/issues/2316#issuecomment-3637281932) **jakebailey** said "#2280"

### [Issue microsoft/TypeScript-go#2317](https://github.com/microsoft/TypeScript-go/issues/2317) (Open)

**Console is not cleared in watch mode \(also does not show the 0 error count output\)**

*tsgo’s watch mode fails to clear the console between builds and omits the “Found 0 errors” message*

 * created by **gitter-me**

### [Issue microsoft/TypeScript-go#2318](https://github.com/microsoft/TypeScript-go/issues/2318) (Closed, `bug`, `Domain: Emit`)

**\`experimentalDecorators\` doesn't transform the output**

*tsgo does not convert experimental TypeScript decorators into __decorate function calls, unlike tsc.*

 * created by **jycouet**
 * [later](https://github.com/microsoft/TypeScript-go/issues/2318#issuecomment-3635932378) **DanielRosenwasser** said "Yeah, it's currently a known gap and the work is in progress. "
 * (later) **DanielRosenwasser** added labels `bug`, `Domain: Emit`
 * [later](https://github.com/microsoft/TypeScript-go/issues/2318#issuecomment-3637289416) **jakebailey** said "#914"
 * (later) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2319](https://github.com/microsoft/TypeScript-go/pull/2319) (Closed)

**fix\(2271\): Invalid declaration emit for enum value type**

*Corrects invalid enum value type declaration emissions to produce accurate declaration files.*

 * created by **a-tarasyuk**

