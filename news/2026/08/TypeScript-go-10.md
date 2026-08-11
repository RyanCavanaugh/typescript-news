# Report for 2026-08-10 (Monday, August 10th, 2026)

13 different users commented on 39 different issues.

## Recommended Actions

 * Response Recommended
    * @thempatel asked for updates on the issue blocking their upgrade to the new compiler in [microsoft/TypeScript-go#4262](https://github.com/microsoft/TypeScript-go/issues/4262#issuecomment-5243474388)
    * @robertkirkman suggested using TERMUX_EXEC__PROC_SELF_EXE and offered to test if applied in [microsoft/TypeScript-go#4734](https://github.com/microsoft/TypeScript-go/pull/4734#issuecomment-5247327150)
    * @robertkirkman reported compilation errors and asked if missing patch could fix them in [microsoft/TypeScript-go#4734](https://github.com/microsoft/TypeScript-go/pull/4734#issuecomment-5248990930)
    * @robertkirkman provided test results confirming PR fixes errors in [microsoft/TypeScript-go#4734](https://github.com/microsoft/TypeScript-go/pull/4734#issuecomment-5249567999)

## Activity Summary

### [Issue microsoft/TypeScript-go#4262](https://github.com/microsoft/TypeScript-go/issues/4262) (Closed, `bug`, `Needs More Info`)

**Non\-deterministic \`TS2305 "has no exported member"\` errors across project references with \`\-\-emitDeclarationOnly\`**

*Flaky TS2305 "has no exported member" errors occur when running --emitDeclarationOnly across project references in a pnpm monorepo using tsgo.*

 * [8 weeks ago](https://github.com/microsoft/TypeScript-go/issues/4262#issuecomment-4715575995) **jakebailey** noted that task launch order shouldn't matter and requested a test to identify the bug
 * [8 weeks ago](https://github.com/microsoft/TypeScript-go/issues/4262#issuecomment-4715657883) **ibesuperv** thanked jakebailey, explained the intended sorting within the locked section to handle non-deterministic iteration over casing variants, and said they would create and share a minimal reproducible test case
 * [1 month ago](https://github.com/microsoft/TypeScript-go/issues/4262#issuecomment-4928897571) **eddking** described the nondeterminism issue on macOS due to Realpath resolving hardlink siblings and linked the fix in #4578
 * [today](https://github.com/microsoft/TypeScript-go/issues/4262#issuecomment-5243474388) **thempatel** asked for updates on the issue and explained it blocked upgrade to the new compiler due to mac osx non-determinism and the need for hardlinks in the pnpm store
 * [today](https://github.com/microsoft/TypeScript-go/issues/4262#issuecomment-5243522704) **jakebailey** said "The discussion was on #4578 but I think that is a dead end; I'll just send another change that kills the fast path I added but that turned out to not work"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4313](https://github.com/microsoft/TypeScript-go/pull/4313) (Open)

**Assign files to checkers using balanced import affinity**

*A FENNEL-based balanced import affinity algorithm replaces round-robin checker assignment to boost checking performance and reduce memory usage by 10%.*

 * [5 days ago](https://github.com/microsoft/TypeScript-go/pull/4313#issuecomment-5194974744) **jakebailey** said "@typescript-bot perf test this faster"
 * [5 days ago](https://github.com/microsoft/TypeScript-go/pull/4313#issuecomment-5194975562) **typescript-automation[bot]** started CI jobs and posted status update
 * [5 days ago](https://github.com/microsoft/TypeScript-go/pull/4313#issuecomment-5195258586) **typescript-automation[bot]** posted the requested perf run results with a detailed comparison report
 * [today](https://github.com/microsoft/TypeScript-go/pull/4313#issuecomment-5244383319) **jakebailey** said "I tested the method from #4856 and it was worse; the FENNEL approach here does a better job across workloads, mui, etc."

### [Issue microsoft/TypeScript-go#4499](https://github.com/microsoft/TypeScript-go/issues/4499) (Closed, `Domain: API and Extensibility`, **andrewbranch**)

**Add \`TupleTypeReference\` interface to the API**

*Introduce a TupleTypeReference interface in the API to facilitate typed handling of tuple types with Checker#isTupleType.*

 * (5 weeks ago) **andrewbranch** added label `Domain: API and Extensibility`, set milestone to `Post-7.0`, and assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4499#issuecomment-5249651653) **mrazauskas** said "Included in #4870"
 * (today) **mrazauskas** closed the issue

### [PR microsoft/TypeScript-go#4557](https://github.com/microsoft/TypeScript-go/pull/4557) (Closed)

**Account nested declaration emits as emit time**

*Track nested declaration emit durations in incremental compilation by moving them from check to emit time and adding regression test.*

 * created by **jakebailey**
 * (2 weeks ago) **jakebailey** closed the issue
 * (2 weeks ago) **jakebailey** reopened the issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/4557#issuecomment-5245989547) **jakebailey** said "This has been redone to just bring it to accounting correctly, the other stuff was junk"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4578](https://github.com/microsoft/TypeScript-go/pull/4578) (Closed)

**Fix nondeterministic Realpath on darwin for hardlinked files**

*Deterministically resolve files with multiple hardlinks on macOS by reconstructing paths from parent directories to prevent intermittent resolution errors.*

 * created by **eddking**
 * [1 month ago](https://github.com/microsoft/TypeScript-go/pull/4578#issuecomment-4928938584) **eddking** said "@microsoft-github-policy-service agree"
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4578#issuecomment-5035875510) **jakebailey** suggested deleting the darwin special case code and testing fallback to EvalSymlinks
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4609](https://github.com/microsoft/TypeScript-go/issues/4609) (Closed, `bug`)

**Extensionless root file panics the compiler: "ScriptKind must be specified when parsing source file"**

*TypeScript 7's compiler panics with a 'ScriptKind must be specified' error when parsing extensionless root files.*

 * created by **elibarzilay**
 * (3 weeks ago) **RyanCavanaugh** added label `bug`, and set milestone to `Post-7.0`
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#4628](https://github.com/microsoft/TypeScript-go/pull/4628) (Closed)

**Handle extensionless root files gracefully instead of panicking**

*Handle extensionless root files by emitting TS6231 diagnostics instead of panicking and defaulting unknown script kinds to TypeScript.*

 * created by **UditDewan**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#4661](https://github.com/microsoft/TypeScript-go/pull/4661) (Closed)

**Fall back to inotify when filesystem has errors in fanotify \(fix watch in Docker\)**

*Automatically switch to inotify backend when fanotify fails on Docker filesystems to detect file changes.*

 * created by **johnfav03**
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4661#issuecomment-5107156400) **jakebailey** said "I think this approach is probably okay, though I do wonder if the fanotify watch backend should just internally fall back to inotify..."
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4661#issuecomment-5145562548) **johnfav03** embedded the inotify fallback into the fanotify backend and asked if it matched the suggestion
 * [today](https://github.com/microsoft/TypeScript-go/pull/4661#issuecomment-5243507982) **johnfav03** explained the fallback mechanism where fanotify failures result in re-registration with inotify for the recursive root
 * (today) **johnfav03** closed the issue

### [PR microsoft/TypeScript-go#4712](https://github.com/microsoft/TypeScript-go/pull/4712) (Open)

**Content mappers**

*Support external content mappers in tsconfig to transform and map unsupported file types into valid TypeScript*

 * [4 days ago](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5211145449) **andrewbranch** said "Another significant change: a content mapper may now emit additional supplemental files as part of any Transform response. PR description updated again."
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5213869402) **johnnyreilly** asked whether the custom transformers functionality would cover what transformers did in the TS API
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5218558612) **andrewbranch** said "No, but custom transformers are still planned, mentioned in #4830. I’ll add ts-loader to the list of projects that needs it!"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5247642853) **andrewbranch** described how third-party VS Code extensions can now contribute bundled content mappers directly, restricted to inferred projects without jsconfig/tsconfig files

### [Issue microsoft/TypeScript-go#4722](https://github.com/microsoft/TypeScript-go/issues/4722) (Open, `bug`, **jakebailey**, **Copilot**)

**Nested nullish coalescing \+ comment \+ ES2018 causes function body to be ignored**

*Transpiling nested nullish coalescing with comments targeting ES2018 misplaces the return statement causing function body to be ignored*

 * **jakebailey** assigned to **jakebailey**
 * (1 week ago) **RyanCavanaugh** added label `bug`, and set milestone to `TypeScript 7.1`
 * [today](https://github.com/microsoft/TypeScript-go/issues/4722#issuecomment-5243143457) **smerrill** apologized for opening a duplicate issue and clarified that a single level of optional chaining triggers the issue

### [PR microsoft/TypeScript-go#4723](https://github.com/microsoft/TypeScript-go/pull/4723) (Open, **jakebailey**, **Copilot**)

**Preserve comments when downleveling arrow expression bodies**

*Maintain leading comments in arrow function expression bodies when downleveling optional chaining by attaching them before the synthesized return statement.*

 * created by **Copilot**
 * (2 weeks ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4723#issuecomment-5243175220) **jakebailey** provided a test case from another issue comment for optional chaining

### [PR microsoft/TypeScript-go#4734](https://github.com/microsoft/TypeScript-go/pull/4734) (Open)

**Add Android ARM64 release target**

*Add Android ARM64 release target to the build configuration*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4734#issuecomment-5151566500) **robertkirkman** explained that typescript-go’s os.Executable fails on Google Play Termux due to Android’s targetSdkVersion restrictions and suggested using the TERMUX_EXEC__PROC_SELF_EXE environment variable
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4734#issuecomment-5151664489) **robertkirkman** provided context that the error is specific to Google Play Termux and noted the binary has the correct interpreter and passes the static linking check
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4734#issuecomment-5235339709) **robertkirkman** described patch-based implementation by the Google Play Termux developer for supporting os.Executable on Android API level 29+, provided patch links, and suggested limiting support to API level 24–28 in CI
 * [today](https://github.com/microsoft/TypeScript-go/pull/4734#issuecomment-5243385164) **jakebailey** suggested filing an upstream proposal to Go for standard library changes and proposed reading an environment variable for Android instead of patching the library
 * [today](https://github.com/microsoft/TypeScript-go/pull/4734#issuecomment-5247327150) **robertkirkman** suggested reading TERMUX_EXEC__PROC_SELF_EXE instead of os.Executable() and offered to test the change
 * [today](https://github.com/microsoft/TypeScript-go/pull/4734#issuecomment-5248508840) **jakebailey** said "It indeed works, when I test it on an emulator. Give it a try once it's built."
 * [today](https://github.com/microsoft/TypeScript-go/pull/4734#issuecomment-5248990930) **robertkirkman** tested both F-Droid and Google Play Termux and reported that while absolute-path tsc commands worked, relative-path TypeScript compilations failed with specific errors, and suspected a missing argv manipulation patch
 * [today](https://github.com/microsoft/TypeScript-go/pull/4734#issuecomment-5249567999) **robertkirkman** tested the latest PR version on both F-Droid Termux and Google Play Termux and confirmed it works, fixes errors, and maintains compatibility when TERMUX_EXEC__PROC_SELF_EXE is unset

### [Issue microsoft/TypeScript-go#4748](https://github.com/microsoft/TypeScript-go/issues/4748) (Open, `Needs Investigation`, **weswigham**)

**Panic: nil pointer in NodeList\.HasTrailingComma during incremental rebuild \(build\-mode declaration printer\) — 7\.0\.2 and current nightly**

*A nil pointer dereference in NodeList.HasTrailingComma triggers a panic during incremental build-mode declaration printing in TypeScript.*

 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/4748#issuecomment-5209111655) **nikeedw** described root cause with a two-file minimal repro, proposed a fix in PR #4842, and requested maintainers’ judgment
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/4748#issuecomment-5220700380) **RyanCavanaugh** warned against sending a PR without signing the CLA, closed the PR without reviewing it, and said it would be archived before automated resolution
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/4748#issuecomment-5221620947) **nikeedw** provided an update on CLA signing and apologized for the churn; resubmitted the branch as PR #4846 and offered maintainers to re-derive the fix if preferred
 * (today) **RyanCavanaugh** added label `Needs Investigation`, removed label `Needs More Info`, set milestone to `Post-7.0`, removed from milestone `Need More Info`, and assigned to **weswigham**

### [PR microsoft/TypeScript-go#4779](https://github.com/microsoft/TypeScript-go/pull/4779) (Open)

**Fix incremental builder re\-emitting entire import closure on non\-shape\-changing edits**

*Incremental builder computes real .d.ts signatures on fresh builds to avoid re-emitting full import closures on non-shape-changing edits.*

 * created by **johnfav03**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4779#issuecomment-5243834859) **jakebailey** said "Eagerly doing dts emit seems scary, but I don't quite know if I can tell if that gut feeling is wrong or not"

### [PR microsoft/TypeScript-go#4797](https://github.com/microsoft/TypeScript-go/pull/4797) (Closed)

**Split heritage clause expression and type nodes**

*Propose splitting heritage clause nodes into distinct expression and type variants to accurately represent type space usage in the AST*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4797#issuecomment-5135976418) **typescript-automation[bot]** announced start of perf test CI jobs and included status links
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4797#issuecomment-5136157447) **Gerrit0** acknowledged that there were two cases he hadn't considered before and agreed it was a good idea
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4797#issuecomment-5136541195) **typescript-automation[bot]** provided the requested performance run results
 * [today](https://github.com/microsoft/TypeScript-go/pull/4797#issuecomment-5243036565) **andrewbranch** said "Is this ready? I think it’s a good idea, and it looks like the one thing I flagged is resolved."
 * [today](https://github.com/microsoft/TypeScript-go/pull/4797#issuecomment-5243203723) **jakebailey** explained that diffs appeared after dropping the compatibility code from Copilot and suggested updating the visitor to skip type-only nodes, noting similar cases existed before
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4809](https://github.com/microsoft/TypeScript-go/issues/4809) (Open, `Crash`, **jakebailey**, **Copilot**)

**LSP exits when parent process PID is not found**

*LSP’s parent-PID watchdog terminates the server when the PID can’t be found in Docker, with a CLI flag to disable it.*

 * [6 days ago](https://github.com/microsoft/TypeScript-go/issues/4809#issuecomment-5181165788) **mj026** noted that vscode language servers have similar behavior with a parent process watchdog and suggested using the --clientProcessId option instead of removing it; offered to provide a PR
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/4809#issuecomment-5222278230) **jakebailey** said "How does that help your case? If you're launching in docker, how would you know the PID ahead of time if it's inside a container or something?"
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/4809#issuecomment-5233282616) **mj026** explained that the real parent process isn't visible in a container and demonstrated that the init process appears as PID 1
 * [today](https://github.com/microsoft/TypeScript-go/issues/4809#issuecomment-5243409670) **jakebailey** said "Given https://github.com/microsoft/vscode-languageserver-node/blob/0b6b07cdbed310771ac26267109c1db22ee62a2b/client/src/node/main.ts#L375 we can probably just use this flag, yeah"

### [PR microsoft/TypeScript-go#4811](https://github.com/microsoft/TypeScript-go/pull/4811) (Closed, **jakebailey**, **Copilot**)

**Remove the LSP parent process watchdog**

*Remove LSP parent process monitoring and watchdog to prevent erroneous exits across containers, relying instead on stdio and signal lifecycle.*

 * created by **Copilot**
 * (1 week ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4823](https://github.com/microsoft/TypeScript-go/pull/4823) (Closed, **RyanCavanaugh**, **Copilot**)

**Preserve await context for exported classes in nested containers**

*Restrict await context for exported classes to top-level declarations while preserving it within async functions and generators.*

 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/4823#issuecomment-5222723233) **Copilot** addressed review feedback by extending the testcase with static-member coverage and updating baselines
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/4823#issuecomment-5223410523) **RyanCavanaugh** said "@copilot CI is failing, and use a proper bit test as suggested"
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/4823#issuecomment-5223523155) **Copilot** updated bitwise context checks per suggestion in commit e7130af9 and clarified the CI failure was due to a transient Go download error
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#4831](https://github.com/microsoft/TypeScript-go/issues/4831) (Open, `Needs More Info`)

**High CPU Usage in Editor \(and Controls for LSP\)**

*Wants a built-in CPU usage limit flag for tsgo's LSP mode to prevent high CPU spikes on low-end laptops.*

 * **DanielRosenwasser** added label `Needs More Info`
 * **RyanCavanaugh** added to milestone `Need More Info`
 * [today](https://github.com/microsoft/TypeScript-go/issues/4831#issuecomment-5241413467) **glav-git** asked what additional information to provide and described reproduction steps of tsgo consuming all resources, provided system details and noted that project complexity contributed to the issue
 * [today](https://github.com/microsoft/TypeScript-go/issues/4831#issuecomment-5243340738) **jakebailey** mentioned that VS Code has commands to start and stop a profile and that it was unclear how to do so outside VS Code

### [Issue microsoft/TypeScript-go#4838](https://github.com/microsoft/TypeScript-go/issues/4838) (Closed, `Needs Investigation`, **johnfav03**)

**\`tsc \-\-watch\` can't handle errors across files**

*TypeScript’s watch mode fails to detect cross-file errors when a variable declaration is removed in a dependent file.*

 * (3 days ago) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `Post-7.0`, and assigned to **johnfav03**
 * (today) **johnfav03** closed the issue

### [PR microsoft/TypeScript-go#4847](https://github.com/microsoft/TypeScript-go/pull/4847) (Open, `Voight-Kampff Anomaly`)

**fix: allow destructured require under module preserve \+ verbatimModuleSyntax**

*Allow destructured require calls in CommonJS modules under --module preserve and --verbatimModuleSyntax by adjusting alias checks to prevent TS1293 errors.*

 * created by **sankalpsthakur**
 * **RyanCavanaugh** added label `Voight-Kampff Anomaly`

### [PR microsoft/TypeScript-go#4848](https://github.com/microsoft/TypeScript-go/pull/4848) (Closed)

**Fix watch diagnostics when global declaration is removed**

*Watch mode now rechecks all affected files when a global declaration is removed to prevent stale diagnostics*

 * created by **johnfav03**
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/4848#issuecomment-5222109644) **jakebailey** asked to split the PR into two commits, first adding the test and baseline and then the fix with the baseline update
 * [today](https://github.com/microsoft/TypeScript-go/pull/4848#issuecomment-5243597254) **johnfav03** said "Just split the test and the fix into two commits; with just the test, a clean build should report TS2304: Cannot find name 'a' whereas the incremental watch incorrectly reports 0 errors. "
 * (today) **johnfav03** closed the issue

### [PR microsoft/TypeScript-go#4849](https://github.com/microsoft/TypeScript-go/pull/4849) (Closed)

**Port transpileModule, transpileDeclaration**

*Port the TS API’s transpileModule, transpileModuleFromFile, transpileDeclaration, and transpileDeclarationFromFile functions.*

 * created by **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#4854](https://github.com/microsoft/TypeScript-go/issues/4854) (Open)

**macOS: allow DYLD\_INSERT\_LIBRARIES in tsgo**

*Add Hardened Runtime entitlements to tsgo’s macOS builds to allow DYLD_INSERT_LIBRARIES for dyld interposition tools.*

 * created by **wan9chi**
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/4854#issuecomment-5230324746) **jakebailey** stated they were limited in options and offered to check with the signing team, noted it seemed strange to un-harden the binary and cursed to rely on track file reads
 * [today](https://github.com/microsoft/TypeScript-go/issues/4854#issuecomment-5244808336) **jakebailey** explained that adhoc codesigning was required before using the signing service and asked if it could be done without a Mac runner in CI
 * [today](https://github.com/microsoft/TypeScript-go/issues/4854#issuecomment-5244815769) **jakebailey** said "Aha! https://github.com/anchore/quill"
 * [today](https://github.com/microsoft/TypeScript-go/issues/4854#issuecomment-5247188757) **jakebailey** confirmed that #4868 works

### [Issue microsoft/TypeScript-go#4864](https://github.com/microsoft/TypeScript-go/issues/4864) (Closed)

**Optional chaining rewrites cause incorrect output**

*In TS 7.0.2, comments before optional chaining rewrites trigger automatic semicolon insertion after return, causing functions to return undefined.*

 * created by **smerrill**
 * (today) **jakebailey** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/issues/4864#issuecomment-5243114440) **jakebailey** said "Duplicate of #4722"

### [PR microsoft/TypeScript-go#4865](https://github.com/microsoft/TypeScript-go/pull/4865) (Open)

**Avoid expensive incremental reconciliation after dependency paths move**

*Detect moved dependency paths in the TypeScript compiler's incremental builds and perform a cold-build snapshot to avoid expensive reconciliation.*

 * created by **johnfav03**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4865#issuecomment-5243653489) **jakebailey** asked to split the changes into two commits and expressed uncertainty about the heuristic approach
 * [today](https://github.com/microsoft/TypeScript-go/pull/4865#issuecomment-5244367310) **johnfav03** split the changes into two commits and explained that the pre-fix baseline forced .d.ts computation and signature updates while the post-fix cold-build baseline showed no signature reconciliation

### [PR microsoft/TypeScript-go#4866](https://github.com/microsoft/TypeScript-go/pull/4866) (Open)

**Add \`\-\-clientProcessId\` like reference LSP server**

*Add a --clientProcessId flag to allow overriding the parent process ID in LSP server initialization.*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#4867](https://github.com/microsoft/TypeScript-go/pull/4867) (Closed)

**Remove macOS realpath fast path**

*Remove the macOS realpath fast path due to incorrect behavior when resolving hard links.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4868](https://github.com/microsoft/TypeScript-go/pull/4868) (Open)

**Add macOS entitlements before signing**

*Introduces a quill-based step to apply macOS entitlements before code signing*

 * created by **jakebailey**

### [Issue microsoft/TypeScript-go#4869](https://github.com/microsoft/TypeScript-go/issues/4869) (Open, `Domain: Editor`)

**Allow settings\.json to configure tssdk without a prompt**

*Provide a settings.json option to automatically opt into the workspace’s tsdk and bypass the prompt.*

 * created by **eagarwal-notion**
 * **eagarwal-notion** added label `Domain: Editor`
 * [today](https://github.com/microsoft/TypeScript-go/issues/4869#issuecomment-5247283849) **RyanCavanaugh** said "This has security implications (tsdk is effectively an arbitrary command), so it's necessary for the user to opt in."

### [PR microsoft/TypeScript-go#4870](https://github.com/microsoft/TypeScript-go/pull/4870) (Open)

**\[api\] Clear up the difference between tuple types and tuple type references**

*Renames and separates the TypeScript API predicates for tuple types and tuple type references to resolve naming mismatches.*

 * created by **andrewbranch**

### [PR microsoft/TypeScript-go#4871](https://github.com/microsoft/TypeScript-go/pull/4871) (Closed)

**Allow initialize requests without rootUri**

*Allow LSP initialize requests to omit the deprecated rootUri property by treating omission as null.*

 * created by **navya9singh**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4871#issuecomment-5247365366) **jakebailey** said "But this is a spec violation, no?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4871#issuecomment-5247372923) **andrewbranch** noted that his approval was only based on `rootUri` deprecation and stated that the root cause is likely a VS bug needing fixes for other properties
 * [today](https://github.com/microsoft/TypeScript-go/pull/4871#issuecomment-5247405427) **jakebailey** noted that rootUri was deprecated yet required and that only rootUri and processId were required but nullable
 * [today](https://github.com/microsoft/TypeScript-go/pull/4871#issuecomment-5247448597) **andrewbranch** acknowledged missing context on null fields and noted that a VS bug fix would make the change unnecessary
 * [today](https://github.com/microsoft/TypeScript-go/pull/4871#issuecomment-5247547819) **navya9singh** explained that the VS client suggested using null for deprecated rootUri, noted VS drops null-valued properties, and said they would follow up with the VSLanguageServerClient team and close the PR
 * (today) **navya9singh** closed the issue

### [PR microsoft/TypeScript-go#4872](https://github.com/microsoft/TypeScript-go/pull/4872) (Open, **andrewbranch**, **Copilot**)

**Preserve local auto\-imports in circular workspace symlink topologies**

*Scope node_modules symlink filtering to exclude only external files so local project auto-imports remain in circular workspace dependencies*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **andrewbranch**
 * [later](https://github.com/microsoft/TypeScript-go/pull/4872#issuecomment-5254331900) **andrewbranch** said "@copilot you need to run node internal/fourslash/_scripts/updateFailing.mts"
 * [later](https://github.com/microsoft/TypeScript-go/pull/4872#issuecomment-5254521950) **Copilot** ran the internal script to update failing tests, removed two tests from failingTests.txt, and re-ran formatting, build, tests, and lint with all green results

### [PR microsoft/TypeScript-go#4873](https://github.com/microsoft/TypeScript-go/pull/4873) (Open)

**fix\(4863\): fix declaration emit for jsdoc functions**

*Corrects the emission of TypeScript declaration files for functions annotated with JSDoc.*

 * created by **a-tarasyuk**

### [Issue microsoft/TypeScript-go#4874](https://github.com/microsoft/TypeScript-go/issues/4874) (Open)

**Add API to get target symbol of instantiated symbol**

*Add a Symbol.getTarget method to expose the underlying target symbol of instantiated symbols*

 * created by **mrazauskas**

### [Issue microsoft/TypeScript-go#4875](https://github.com/microsoft/TypeScript-go/issues/4875) (Open)

**\`@augments\` JSDoc tag causes compilation error in generated declaration file**

*A JSDoc @augments tag mismatched with the extends clause in generated declaration files triggers ts(8023) errors under tsgo.*

 * created by **dragomirtitian**

