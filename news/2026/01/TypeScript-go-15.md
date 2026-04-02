# Report for 2026-01-15 (Thursday, January 15th, 2026)

17 different users commented on 27 different issues.

## Recommended Actions

 * Response Recommended
    * @evanrh provided additional debug information in [microsoft/TypeScript-go#2239](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3756750707)
    * @Neo0724 reported memory usage details after restart and attempted garbage collection in [microsoft/TypeScript-go#2239](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3757992862)
    * @talldan provided profiling data before and after restarting the language server in [microsoft/TypeScript-go#2239](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3758010438)
    * @HananoshikaYomaru provided repro steps as requested in [microsoft/TypeScript-go#2418](https://github.com/microsoft/TypeScript-go/issues/2418#issuecomment-3757238865)
    * @frangio identified the cause and suggested a temporary fix but asked for the proper fix in [microsoft/TypeScript-go#2511](https://github.com/microsoft/TypeScript-go/issues/2511#issuecomment-3757108569)
    * @frangio confirmed that the fix resolved issue #2511 in [microsoft/TypeScript-go#2520](https://github.com/microsoft/TypeScript-go/pull/2520#issuecomment-3757609285)
    * @Knagis provided helpful version comparison information in [microsoft/TypeScript-go#2522](https://github.com/microsoft/TypeScript-go/issues/2522#issuecomment-3759406281)

## Activity Summary

### [Issue microsoft/TypeScript-go#1708](https://github.com/microsoft/TypeScript-go/issues/1708) (Open, `Domain: Editor`)

**tsgo preview: import suggestions are not aware of paths**

*tsgo preview in Zed lacks path-aware import suggestions provided by vtsls, making it unusable.*

 * [1 month ago](https://github.com/microsoft/TypeScript-go/issues/1708#issuecomment-3647674267) **jakebailey** asked about the priority and requested repro steps if the issue persisted
 * [1 month ago](https://github.com/microsoft/TypeScript-go/issues/1708#issuecomment-3652337668) **longzheng** reproduced the issue after latest changes and shared a repro project with configuration
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/1708#issuecomment-3752807937) **affanshahid** explained how they fixed the issue on Zed by setting importModuleSpecifierPreference in tsgo settings and noted vscode's property mapping difference
 * [today](https://github.com/microsoft/TypeScript-go/issues/1708#issuecomment-3757327834) **longzheng** described using 'importModuleSpecifierPreference' to fix configuration in Zed and VSCode and noted an upcoming PR would correct the parser to use the proper property name
 * [today](https://github.com/microsoft/TypeScript-go/issues/1708#issuecomment-3757811402) **affanshahid** described needing to use both keys to make imports work across different contexts and expressed relief that the issue was fixed

### [Issue microsoft/TypeScript-go#1952](https://github.com/microsoft/TypeScript-go/issues/1952) (Closed, `Crash`, `Needs More Info`, **DanielRosenwasser**, **weswigham**)

**Declaration emit crash**

*The declaration emitter panics with ‘Unknown parent for parameter: KindArrowFunction’ during compilation.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/1952#issuecomment-3752313072) **jakebailey** provided a TypeScript test case that reproduced a compiler panic involving forwardRef and generics
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/1952#issuecomment-3752377037) **jakebailey** referred to a PR that fixed the issue but noted two TypeScript errors remained in the zipped repo
 * [today](https://github.com/microsoft/TypeScript-go/issues/1952#issuecomment-3754427013) **trueadm** said "@jakebailey Thank you so much!"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#1966](https://github.com/microsoft/TypeScript-go/pull/1966) (Open)

**Add Yarn PnP support**

*Implement native Yarn Plug'n'Play support in TypeScript Go with PnP VFS, API, and manifest handling.*

 * [1 month ago](https://github.com/microsoft/TypeScript-go/pull/1966#issuecomment-3665523095) **loynoir** described a workaround using typescript.experimental.useTsgo and a custom tsgo-pnp bash script
 * [1 month ago](https://github.com/microsoft/TypeScript-go/pull/1966#issuecomment-3666320618) **adrian-gierakowski** suggested wrapping the build with nix and provided a flake.nix with instructions for building and running the binary
 * [today](https://github.com/microsoft/TypeScript-go/pull/1966#issuecomment-3754114970) **jdpt0** said "@jakebailey Any chance of getting this PR reviewed again? I, and I'm sure many others, would love to see this get merged before the full release. Many thanks 🙏 "
 * [today](https://github.com/microsoft/TypeScript-go/pull/1966#issuecomment-3756917844) **jakebailey** clarified that deciding on the approach and long-term implications, not PR review, was the blocker
 * [later](https://github.com/microsoft/TypeScript-go/pull/1966#issuecomment-3758895612) **wojtekmaj** supported adding native Plug’n’Play support to typescript-go, cited growing Yarn usage statistics, and explained how patch-based solutions cause maintenance overhead

### [Issue microsoft/TypeScript-go#2239](https://github.com/microsoft/TypeScript-go/issues/2239) (Closed, `Needs More Info`)

**take too much memory**

*tsgo extension consumes about 17GB of RAM on macOS M1, causing heavy swapping and slowing VS Code.*

 * [today](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3753583101) **gp27** provided a memory profile showing around 29GB usage with tsgo v7.0.0-dev.20260114.1 and attached heap and alloc profile files
 * [today](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3754072783) **oorestisime** attached two heap and alloc profile files totalling 13gb
 * [today](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3754321832) **oorestisime** provided heap and alloc profile attachments and described reproducible memory usage increase in VS Code
 * [today](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3756750707) **evanrh** said "I am seeing this behavior in Neovim as well. I'm having trouble getting the memory profiles, but the memory usage was incredibly high in htop."
 * [today](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3756753335) **jakebailey** provided heap profiles, analyzed memory usage dominated by module resolution and symbols, and asked for a heap profile after restarting the language server
 * [today](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3756760084) **jakebailey** provided two heap and alloc profiles showing memory usage around 29GB and 13GB and noted that the second run held 9.23GB with about 4GB unused space largely in ASTs
 * [today](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3757992862) **Neo0724** reported that after restarting the language server memory usage dropped significantly but then increased during editing and did not decrease with garbage collection
 * [today](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3758010438) **talldan** attached heap and alloc profiles from before and after restarting the language server

### [Issue microsoft/TypeScript-go#2418](https://github.com/microsoft/TypeScript-go/issues/2418) (Open)

**\[BUG\] tsgo list more files than tsc**

*tsgo’s --listFilesOnly output includes extra files compared to tsc, breaking basic tsgo --noEmit CI checks.*

 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/2418#issuecomment-3733546667) **HananoshikaYomaru** reported that updating include settings still linted src/migrations and suspected tsgo ignored include/exclude
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2418#issuecomment-3752323213) **jakebailey** said "That's not how include/exclude work. We still follow imports. That's why --explainFiles output should be helpful, since you can look at the output to determine why each file was included."
 * [today](https://github.com/microsoft/TypeScript-go/issues/2418#issuecomment-3755484687) **HananoshikaYomaru** misunderstood the operation of "includes" and "excludes", intended to exclude TypeScript errors from specific files but could not figure out why tsgo and tsc behaved differently
 * [today](https://github.com/microsoft/TypeScript-go/issues/2418#issuecomment-3756717309) **jakebailey** said "I unfortunately don't know how to work on this without a repro I can test and debug myself ☹️ "
 * [today](https://github.com/microsoft/TypeScript-go/issues/2418#issuecomment-3757238865) **HananoshikaYomaru** provided repository link and reproduction steps

### [Issue microsoft/TypeScript-go#2422](https://github.com/microsoft/TypeScript-go/issues/2422) (Closed, `Domain: Editor`)

**Auto import does not respect paths**

*Auto import quick fix ignores tsconfig paths and non-relative import preference, using relative paths instead of aliases.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2422#issuecomment-3685387234) **Bashamega** prompted @longzheng to install the latest extension version and reported inability to reproduce the issue on version 0.20251204.2
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2422#issuecomment-3685399805) **longzheng** reported being on version 0.20251222.1 and that downgrading to version 0.20251204.1 also worked
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/2422#issuecomment-3744313385) **hilja** noted that the imports field in package.json was not respected
 * [today](https://github.com/microsoft/TypeScript-go/issues/2422#issuecomment-3757330600) **longzheng** noted that using typescript.preferences.importModuleSpecifierPreference works, that a config parser bug was fixed in an upcoming PR to use the correct setting name, and kept both settings in their config
 * (today) **longzheng** closed the issue

### [PR microsoft/TypeScript-go#2461](https://github.com/microsoft/TypeScript-go/pull/2461) (Open, **RyanCavanaugh**, **Copilot**)

**Port TypeScript PR \#62950: Ignore computed name parents when looking up containing functions**

*Port PR #62950 to skip computed name nodes when finding containing functions, preventing recursion and fixing yield/await errors in Go.*

 * created by **Copilot**
 * (6 days ago) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2461#issuecomment-3757055052) **Copilot** explained why getContainingFunctionDeclaration wasn't ported due to having no callers and added two new tests (yieldInComputedNameOfContextuallyTypedObjectNoCrash1.ts, classStaticBlock29.ts) in commit c0af02c6
 * [today](https://github.com/microsoft/TypeScript-go/pull/2461#issuecomment-3757097683) **Copilot** confirmed removal of getContainingClassStaticBlock in commit c0af02c6

### [PR microsoft/TypeScript-go#2462](https://github.com/microsoft/TypeScript-go/pull/2462) (Closed, **RyanCavanaugh**, **Copilot**)

**Port PR \#61376: Fix spurious "used before being assigned" errors in for of/in loops**

*Port TypeScript PR to fix misleading "used before being assigned" errors for variables in for-in and for-of loops.*

 * created by **Copilot**
 * (6 days ago) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2462#issuecomment-3757028702) **Copilot** added the upstream PR test as a local test in testdata/tests/cases/compiler/unusedLocalsInForInOrOf1.ts with corresponding baselines

### [PR microsoft/TypeScript-go#2485](https://github.com/microsoft/TypeScript-go/pull/2485) (Closed)

**Fix race condition in ProjectCollection\.ConfigFileRegistry**

*Resolve intermittent CI failures caused by a race condition in ProjectCollection.ConfigFileRegistry.*

 * created by **fubhy**
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/2485#issuecomment-3742369544) **fubhy** identified more unrelated race conditions in CI and noted a mutex scope issue in flushChanges
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/2485#issuecomment-3742561407) **fubhy** mentioned additional race conditions in CI and attempted to fix one by adjusting the mutex scope in flushChanges
 * (today) **jakebailey** assigned to **andrewbranch**, and unassigned **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#2487](https://github.com/microsoft/TypeScript-go/issues/2487) (Closed, **jakebailey**, **Copilot**)

**Document outline no longer generates nice names for callbacks in tests**

*VSCode document outline no longer generates descriptive test callback names with TS-go, showing only generic “test() callback” labels.*

 * created by **mjbvz**
 * (3 days ago) **jakebailey** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2488](https://github.com/microsoft/TypeScript-go/pull/2488) (Closed, **jakebailey**, **Copilot**)

**Include string literal arguments in document outline callback names**

*Include string and template literal arguments in anonymous test callback names in the document outline.*

 * created by **Copilot**
 * (3 days ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2499](https://github.com/microsoft/TypeScript-go/pull/2499) (Closed)

**Fix potential deadlock in case of lsp shutdown**

*Background tasks can block indefinitely sending messages to the outgoingQueue after the writeLoop exits, causing LSP shutdown deadlock.*

 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/2499#issuecomment-3746598756) **jakebailey** thanked for looking into the issue and suggested plumbing a proper context instead of using Background() for long-running operations
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2499#issuecomment-3749326802) **fubhy** proposed an example for plumbing proper context and asked if it aligned with the suggestion
 * [today](https://github.com/microsoft/TypeScript-go/pull/2499#issuecomment-3755196588) **fubhy** said "The latest CI error is again caused by this: https://github.com/microsoft/typescript-go/pull/2485"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2499#issuecomment-3755752364) **jakebailey** said "I don't know how you're hitting these races in CI so often when I don't even remember seeing them anywhere until now 😅"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2499#issuecomment-3755836045) **fubhy** joked about triggering more CI runs due to inexperience with the codebase and Go

### [PR microsoft/TypeScript-go#2508](https://github.com/microsoft/TypeScript-go/pull/2508) (Closed)

**Parse user preferences for completions tests**

*Update the fourslash conversion script to include user preferences in completions tests and fix a manually adjusted test.*

 * created by **gabritto**
 * (today) **gabritto** closed the issue

### [Issue microsoft/TypeScript-go#2511](https://github.com/microsoft/TypeScript-go/issues/2511) (Closed)

**Stale diagnostics on file reload**

*tsgo diagnostics remain stale in Neovim after reloading a changed file until it’s manually edited*

 * created by **frangio**
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2511#issuecomment-3752232412) **jakebailey** said "Is neovim requesting diagnostics again? The language server only does pull diagnostics. We don't push anything, so this is up to the editor."
 * [today](https://github.com/microsoft/TypeScript-go/issues/2511#issuecomment-3755198534) **frangio** stated the client sent didClose, didOpen, and diagnostic messages, provided debug logs, and suggested the bug was caused by ignoring events.closeChange when bundled with events.openChange
 * [today](https://github.com/microsoft/TypeScript-go/issues/2511#issuecomment-3756594416) **jakebailey** requested the user test the code in their editor with added logging to confirm
 * [today](https://github.com/microsoft/TypeScript-go/issues/2511#issuecomment-3757108569) **frangio** confirmed the previous theory was wrong, identified the actual cause in overlayfs.go, and noted that removing events.closeChange = nil and handling closeChange before openChange fixed the bug but was unsure of the proper fix
 * [today](https://github.com/microsoft/TypeScript-go/issues/2511#issuecomment-3757256154) **jakebailey** said "I have a fix, but the test infra is very flaky on this because it's nondeterministic how these changes get batched together..."

### [PR microsoft/TypeScript-go#2512](https://github.com/microsoft/TypeScript-go/pull/2512) (Closed)

**Ignore non\-variable\-declarations in transformExpandoAssignment**

*Ensure transformExpandoAssignment ignores assignments that are not variable declarations.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2512#issuecomment-3756562327) **jakebailey** said "Yeah, if it's annotated, you can't really have expanded on it, is my interpretation"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2514](https://github.com/microsoft/TypeScript-go/pull/2514) (Open)

**fix: allow references to unexported types**

*Fix declaration emit errors when indirectly referencing unexported types by reusing existing type nodes*

 * created by **raimannma**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2514#issuecomment-3754619979) **raimannma** agreed to the contributor license agreement by replying '@microsoft-github-policy-service agree'
 * [today](https://github.com/microsoft/TypeScript-go/pull/2514#issuecomment-3756733257) **jakebailey** said "I would think this conflicts with #1693 / #2459"

### [PR microsoft/TypeScript-go#2515](https://github.com/microsoft/TypeScript-go/pull/2515) (Closed)

**\[LSP\] Process file deletions against tsconfig \`includes\`**

*Trigger tsconfig reloads on file deletions matching includes wildcards to promptly remove deleted source files.*

 * created by **andrewbranch**

### [PR microsoft/TypeScript-go#2516](https://github.com/microsoft/TypeScript-go/pull/2516) (Closed)

**Fix crash on closing untitled file**

*Closing an untitled file causes the application to crash unexpectedly*

 * created by **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#2517](https://github.com/microsoft/TypeScript-go/issues/2517) (Closed, **jakebailey**, **Copilot**)

**Invalid character error on backslash in a jsdoc comment in js files**

*tsgo incorrectly reports a TS1127 invalid character error for a backslash in a JSDoc comment, while TypeScript 5.9 does not.*

 * created by **brendankenny**
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2518](https://github.com/microsoft/TypeScript-go/pull/2518) (Closed, **jakebailey**, **Copilot**)

**Fix invalid character error on backslash in JSDoc comments in JS files**

*tsgo misidentifies backslashes in JSDoc comments as invalid characters in JavaScript files, corrected by refining its scanner and adding tests*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2519](https://github.com/microsoft/TypeScript-go/pull/2519) (Open, **RyanCavanaugh**, **Copilot**)

**Port TypeScript PR \#60528: Fix crash on index type deferral for generic mapped types with name types**

*Port PR #60528 to simplify index type resolution and prevent crashes for generic mapped types with name types, adding tests.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2519#issuecomment-3757187898) **Copilot** added two regression tests from the upstream PR to verify that the type checker didn't crash on complex mapped types

### [PR microsoft/TypeScript-go#2520](https://github.com/microsoft/TypeScript-go/pull/2520) (Closed)

**Fix missing content change during consecutive didClose/didOpen**

*Fixes missing content changes during consecutive didClose/didOpen events but tests remain flaky due to inconsistent event merging.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2520#issuecomment-3757609285) **frangio** said "I can confirm that this fixes #2511 for me."

### [PR microsoft/TypeScript-go#2521](https://github.com/microsoft/TypeScript-go/pull/2521) (Closed)

**Port rootDir default to configFile directory and some module resoluton fixes**

*Port default rootDir to the config file directory and implement several module resolution fixes*

 * created by **sheetalkamat**

### [Issue microsoft/TypeScript-go#2522](https://github.com/microsoft/TypeScript-go/issues/2522) (Open, `Domain: Declaration Emit`, `Crash`, **weswigham**)

**Reexporting @types/micromatch@4\.0\.10 from a \.cjs file crashes**

*Re-exporting @types/micromatch@4.0.10 from a .cjs file crashes the TypeScript declaration transformer with a ‘Diagnostic emitted without context’ panic.*

 * created by **Knagis**
 * **Knagis** added label `Crash`
 * [later](https://github.com/microsoft/TypeScript-go/issues/2522#issuecomment-3759406281) **Knagis** mentioned that version 7.0.0-dev.20251027.1 compiled without crashes but version 7.0.0-dev.20251029.1 crashed

### [Issue microsoft/TypeScript-go#2523](https://github.com/microsoft/TypeScript-go/issues/2523) (Closed, `bug`, **ahejlsberg**)

**Type inference in a discriminated union with jsx**

*JSX discriminated union incorrectly infers child value as any in tsgo instead of boolean in TypeScript 5.9*

 * created by **domarmstrong**

### [PR microsoft/TypeScript-go#2524](https://github.com/microsoft/TypeScript-go/pull/2524) (Open)

**feat: detect deprecated via JSDoc and flag deprecated property access**

*Add deprecation detection to Go checker by using JSDoc tags to flag deprecated property access.*

 * created by **AyomiCoder**

