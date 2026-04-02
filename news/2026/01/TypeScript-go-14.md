# Report for 2026-01-14 (Wednesday, January 14th, 2026)

20 different users commented on 27 different issues.

## Recommended Actions

 * Response Recommended
    * @affanshahid provided a configuration fix for Zed using importModuleSpecifierPreference in [microsoft/TypeScript-go#1708](https://github.com/microsoft/TypeScript-go/issues/1708#issuecomment-3752807937)
    * @jpike88 asked if the final change could be squeezed in and if it was straightforward in [microsoft/TypeScript-go#1709](https://github.com/microsoft/TypeScript-go/issues/1709#issuecomment-3752824385)
    * @jpike88 expressed concern about lacking plugin support blocking upgrades to tsgo in [microsoft/TypeScript-go#1709](https://github.com/microsoft/TypeScript-go/issues/1709#issuecomment-3752859491)
    * @jdpt0 asked for the PR to be reviewed again before the full release in [microsoft/TypeScript-go#1966](https://github.com/microsoft/TypeScript-go/pull/1966#issuecomment-3754114970)
    * @gp27 provided repro steps and profiling data for a memory leak in tsgo in [microsoft/TypeScript-go#2239](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3752132666)
    * @gp27 said they would collect it today and post it in [microsoft/TypeScript-go#2239](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3753160825)
    * @talldan provided requested profiling data in [microsoft/TypeScript-go#2239](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3753549210)
    * @gp27 provided profile data as requested in [microsoft/TypeScript-go#2239](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3753583101)
    * @oorestisime provided profile files in [microsoft/TypeScript-go#2239](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3754072783)
    * @oorestisime provided repro steps and profile attachments in [microsoft/TypeScript-go#2239](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3754321832)
    * @HananoshikaYomaru asked why tsgo and tsc have different behaviors in [microsoft/TypeScript-go#2418](https://github.com/microsoft/TypeScript-go/issues/2418#issuecomment-3755484687)
    * @jansedlon provided performance measurements and offered screen recordings in [microsoft/TypeScript-go#2503](https://github.com/microsoft/TypeScript-go/issues/2503#issuecomment-3750663993)
    * @jansedlon asked how stable Typescript LSP performance should be in [microsoft/TypeScript-go#2503](https://github.com/microsoft/TypeScript-go/issues/2503#issuecomment-3751004372)
    * @frangio provided debug logs and suggested a bug cause in [microsoft/TypeScript-go#2511](https://github.com/microsoft/TypeScript-go/issues/2511#issuecomment-3755198534)
    * @raimannma provided CLA agreement as requested in [microsoft/TypeScript-go#2514](https://github.com/microsoft/TypeScript-go/pull/2514#issuecomment-3754619979)

## Activity Summary

### [Issue microsoft/TypeScript-go#1708](https://github.com/microsoft/TypeScript-go/issues/1708) (Open, `Domain: Editor`)

**tsgo preview: import suggestions are not aware of paths**

*tsgo preview in Zed lacks path-aware import suggestions provided by vtsls, making it unusable.*

 * [1 month ago](https://github.com/microsoft/TypeScript-go/issues/1708#issuecomment-3647571345) **marioparaschiv** said "What's the priority on user preferences for the LSP? "
 * [1 month ago](https://github.com/microsoft/TypeScript-go/issues/1708#issuecomment-3647674267) **jakebailey** asked about the priority and requested repro steps if the issue persisted
 * [1 month ago](https://github.com/microsoft/TypeScript-go/issues/1708#issuecomment-3652337668) **longzheng** reproduced the issue after latest changes and shared a repro project with configuration
 * [today](https://github.com/microsoft/TypeScript-go/issues/1708#issuecomment-3752807937) **affanshahid** explained how they fixed the issue on Zed by setting importModuleSpecifierPreference in tsgo settings and noted vscode's property mapping difference

### [Issue microsoft/TypeScript-go#1709](https://github.com/microsoft/TypeScript-go/issues/1709) (Open, `Domain: Editor`)

**Allow to specify import sorting\.**

*Add importSorting options to tsconfig.json allowing configurable prioritization of import path suggestions.*

 * created by **jpike88**
 * **jakebailey** added label `Domain: Editor`
 * [today](https://github.com/microsoft/TypeScript-go/issues/1709#issuecomment-3752824385) **jpike88** said "Hi Jake, thanks for your efforts... our company wants to switch to tsgo, this is the final thing can will allow us to do it. Are you able to squeeze it in? Is it as straightforward as I imagine it is?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/1709#issuecomment-3752833906) **jakebailey** suggested using eslint-simple-import-sort or dprint for import sorting, noting the feature isn’t planned in the current codebase
 * [today](https://github.com/microsoft/TypeScript-go/issues/1709#issuecomment-3752839430) **jpike88** argued against relying on eslint in favor of biome and recommended using tsgo for better performance with the TS LSP
 * [today](https://github.com/microsoft/TypeScript-go/issues/1709#issuecomment-3752849908) **jpike88** stated they would investigate dprint as a temporary solution, argued that formatting should be a core part of the official library, and pledged to report back on integration feasibility
 * [today](https://github.com/microsoft/TypeScript-go/issues/1709#issuecomment-3752859491) **jpike88** mentioned they already use a zero-dependency TypeScript plugin to sort imports and expressed concern that lacking similar functionality in tsgo would block upgrades and impact productivity
 * [today](https://github.com/microsoft/TypeScript-go/issues/1709#issuecomment-3752954554) **jakebailey** clarified they lacked bandwidth to work on a new feature while porting existing functionality and noted that dprint's TypeScript plugin used an unrelated Wasm-based system

### [Issue microsoft/TypeScript-go#1952](https://github.com/microsoft/TypeScript-go/issues/1952) (Closed, `Crash`, `Needs More Info`, **DanielRosenwasser**, **weswigham**)

**Declaration emit crash**

*The declaration emitter panics with ‘Unknown parent for parameter: KindArrowFunction’ during compilation.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1952#issuecomment-3675234201) **trueadm** said "@DanielRosenwasser if you get time, please could you let me know if that repro is of any use, if not, I can try and come up with another."
 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/1952#issuecomment-3730952976) **jakebailey** said "@trueadm I tried out your repro on main and it did not crash. Is this fixed for you in the past few weeks?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/1952#issuecomment-3749948756) **trueadm** said "@jakebailey Unfortunately, it still repros for me using 7.0.0-dev.20260114.1. If you follow the steps in the README.md it should repro for you too."
 * [today](https://github.com/microsoft/TypeScript-go/issues/1952#issuecomment-3750727338) **jakebailey** said "Hm, it does now, I don't know how it didn't when I tested it earlier."
 * [today](https://github.com/microsoft/TypeScript-go/issues/1952#issuecomment-3752313072) **jakebailey** provided a TypeScript test case that reproduced a compiler panic involving forwardRef and generics
 * [today](https://github.com/microsoft/TypeScript-go/issues/1952#issuecomment-3752377037) **jakebailey** referred to a PR that fixed the issue but noted two TypeScript errors remained in the zipped repo
 * [later](https://github.com/microsoft/TypeScript-go/issues/1952#issuecomment-3754427013) **trueadm** said "@jakebailey Thank you so much!"

### [PR microsoft/TypeScript-go#1966](https://github.com/microsoft/TypeScript-go/pull/1966) (Open)

**Add Yarn PnP support**

*Implement native Yarn Plug'n'Play support in TypeScript Go with PnP VFS, API, and manifest handling.*

 * [1 month ago](https://github.com/microsoft/TypeScript-go/pull/1966#issuecomment-3665221573) **adrian-gierakowski** explained go install limitations, asked if the maintainer could build the binary manually, and suggested wrapping the process in nix
 * [1 month ago](https://github.com/microsoft/TypeScript-go/pull/1966#issuecomment-3665523095) **loynoir** described a workaround using typescript.experimental.useTsgo and a custom tsgo-pnp bash script
 * [1 month ago](https://github.com/microsoft/TypeScript-go/pull/1966#issuecomment-3666320618) **adrian-gierakowski** suggested wrapping the build with nix and provided a flake.nix with instructions for building and running the binary
 * [later](https://github.com/microsoft/TypeScript-go/pull/1966#issuecomment-3754114970) **jdpt0** said "@jakebailey Any chance of getting this PR reviewed again? I, and I'm sure many others, would love to see this get merged before the full release. Many thanks 🙏 "

### [Issue microsoft/TypeScript-go#2239](https://github.com/microsoft/TypeScript-go/issues/2239) (Closed, `Needs More Info`)

**take too much memory**

*tsgo extension consumes about 17GB of RAM on macOS M1, causing heavy swapping and slowing VS Code.*

 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3631565394) **maxired** said "Actually even with GOMEMLIMIT=2048MiB, after half a day working, my tsgo would eat 13GB of ram, while I have only 6 files opened in vscode"
 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3633459027) **abelcha** explained that the setting did not apply with the native preview extension, noted that Node was not involved in launching the language server, suggested tsgo was not enabled, proposed a cursor issue, and attached process samples
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3747982109) **talldan** reported experiencing high memory usage up to 50GB while using the native preview plugin for VS Code on the WordPress/gutenberg project and noted it increased further after restarting
 * [today](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3751330496) **jakebailey** advised that the latest extension version allowed taking a heap profile when it got high and that the files were safe to upload without exposing project info
 * [today](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3752132666) **gp27** reported a memory leak in tsgo and provided reproduction steps, profiling data, and environment details
 * [today](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3752140424) **jakebailey** noted that the profile showed 1.86GB on the heap and 3.39GB allocated and asked for a later profile collected further along in the leak
 * [today](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3753160825) **gp27** said "I will collect it today and post it. "
 * [later](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3753549210) **talldan** provided profiling data including heap and alloc profiles and offered to provide more
 * [later](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3753583101) **gp27** provided a memory profile showing around 29GB usage with tsgo v7.0.0-dev.20260114.1 and attached heap and alloc profile files
 * [later](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3754072783) **oorestisime** attached two heap and alloc profile files totalling 13gb
 * [later](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3754321832) **oorestisime** provided heap and alloc profile attachments and described reproducible memory usage increase in VS Code

### [Issue microsoft/TypeScript-go#2341](https://github.com/microsoft/TypeScript-go/issues/2341) (Closed)

**Performance regression with \`\-\-incremental\` between \`native\-preview\-0\.20251211\.1\` and \`0\.20251209\.1\`**

*First-run incremental type checking in native-preview-0.20251211.1 is three times slower than in native-preview-0.20251209.1.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2341#issuecomment-3677655142) **hg** reported that commit b0fed9f5bb0d29327e5ee8ba8e0051592cd76639 introduced a twofold slowdown compared to e93d36401a3f6c19a5e7384abbbf40aa210d7cda and provided benchmark details
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2341#issuecomment-3746122283) **gggdomi** followed up about a ~2x slowdown affecting all projects and noted a repro in the first open source repo tried
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2341#issuecomment-3746172630) **jakebailey** said "I did, it's in my inbox, I just haven't gotten to this item yet"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2341#issuecomment-3752118661) **jakebailey** said "Thanks for the repro; some goroutine tracing led me to #2507."
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2418](https://github.com/microsoft/TypeScript-go/issues/2418) (Open)

**\[BUG\] tsgo list more files than tsc**

*tsgo’s --listFilesOnly output includes extra files compared to tsc, breaking basic tsgo --noEmit CI checks.*

 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/2418#issuecomment-3730926809) **jakebailey** asked for an example of an unexpected file, tsconfig settings, project details, and to compare against TS 6.0
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/2418#issuecomment-3733530689) **HananoshikaYomaru** described a React project’s tsconfig.json and reported that tsgo --noEmit ignored the exclude setting, listing migration files
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/2418#issuecomment-3733546667) **HananoshikaYomaru** reported that updating include settings still linted src/migrations and suspected tsgo ignored include/exclude
 * [today](https://github.com/microsoft/TypeScript-go/issues/2418#issuecomment-3752323213) **jakebailey** said "That's not how include/exclude work. We still follow imports. That's why --explainFiles output should be helpful, since you can look at the output to determine why each file was included."
 * [later](https://github.com/microsoft/TypeScript-go/issues/2418#issuecomment-3755484687) **HananoshikaYomaru** misunderstood the operation of "includes" and "excludes", intended to exclude TypeScript errors from specific files but could not figure out why tsgo and tsc behaved differently

### [PR microsoft/TypeScript-go#2463](https://github.com/microsoft/TypeScript-go/pull/2463) (Closed, **RyanCavanaugh**, **Copilot**)

**Port TypeScript PR \#62789: Fix "never nullish" diagnostic missing expressions wrapped in parentheses**

*Port a fix to ensure parenthesized operands in TypeScript nullish coalescing chains correctly trigger 'never nullish' diagnostics.*

 * created by **Copilot**
 * (5 days ago) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#2479](https://github.com/microsoft/TypeScript-go/pull/2479) (Closed)

**Exhaustive case snippet completions**

*Add exhaustive case snippet completions with immediate additional text edits and import adder logic, skipping tests pending user preferences.*

 * created by **gabritto**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2479#issuecomment-3751120818) **gabritto** asked if additional review was needed and clarified that the completions code was a 1:1 port with edits sent eagerly
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript-go#2491](https://github.com/microsoft/TypeScript-go/pull/2491) (Open, **DanielRosenwasser**, **Copilot**)

**Fix nil pointer panic in JSDoc callable type completions**

*Completing JSDoc callable type signatures with parameters causes a nil pointer panic due to missing symbol nil check.*

 * (2 days ago) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/2491#issuecomment-3741753660) **DanielRosenwasser** said "I feel like the investigation here is good but I don't understand why the parameter didn't have a symbol."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2491#issuecomment-3750868286) **ahejlsberg** explained that JSDoc comments don't bind symbols and described how the parameter in the reparsed object literal type obtains its symbol

### [PR microsoft/TypeScript-go#2499](https://github.com/microsoft/TypeScript-go/pull/2499) (Closed)

**Fix potential deadlock in case of lsp shutdown**

*Background tasks can block indefinitely sending messages to the outgoingQueue after the writeLoop exits, causing LSP shutdown deadlock.*

 * created by **fubhy**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2499#issuecomment-3746598756) **jakebailey** thanked for looking into the issue and suggested plumbing a proper context instead of using Background() for long-running operations
 * [today](https://github.com/microsoft/TypeScript-go/pull/2499#issuecomment-3749326802) **fubhy** proposed an example for plumbing proper context and asked if it aligned with the suggestion
 * [later](https://github.com/microsoft/TypeScript-go/pull/2499#issuecomment-3755196588) **fubhy** said "The latest CI error is again caused by this: https://github.com/microsoft/typescript-go/pull/2485"

### [PR microsoft/TypeScript-go#2502](https://github.com/microsoft/TypeScript-go/pull/2502) (Closed)

**Fix module specifier cache misses in symlinked package directories**

*Fix module specifier cache misses in symlinked package directories to reduce completion times from 8.3 seconds to 120ms.*

 * created by **andrewbranch**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2502#issuecomment-3747135586) **andrewbranch** said "I need to look closer at the project reference specific code. @jansedlon’s draft pointed out that we want those to take the slow path, but I want to see if that’s really necessary."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2502#issuecomment-3748858762) **rubnogueira** said "@andrewbranch happy to provide additional context if needed, thank you!"
 * (today) **andrewbranch** closed the issue
 * [later](https://github.com/microsoft/TypeScript-go/pull/2502#issuecomment-3754158779) **rubnogueira** reported testing the changes with the 0.20260115.1 extension and finding much faster, more reliable autocomplete with no IDE lag

### [Issue microsoft/TypeScript-go#2503](https://github.com/microsoft/TypeScript-go/issues/2503) (Open)

**Autocomplete and auto\-import is slower in JSX context**

*JSX tag autocomplete and auto-import in TypeScript monorepos remains slow (~1s vs ~100ms) due to expensive contextual type computation.*

 * created by **jansedlon**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2503#issuecomment-3750337286) **andrewbranch** expressed uncertainty about whether recommendedCompletion was critical and deferred to @gabritto for clarification; noted that limiting auto-import results to 1000 is possible but adds complexity and should wait until other optimizations are done
 * [today](https://github.com/microsoft/TypeScript-go/issues/2503#issuecomment-3750350827) **andrewbranch** said "I also think it would be worthwhile to investigate why getContextualType is so slow here. If there are easy checker optimizations to be made, that helps CLI compile times, too."
 * [today](https://github.com/microsoft/TypeScript-go/issues/2503#issuecomment-3750464227) **gabritto** said "Is this scenario equally slow when using old/non-native TS?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2503#issuecomment-3750663993) **jansedlon** noted that JSX autocomplete was usually slower (1s-2s) compared to outside (500ms-1.5s) in 80% of cases and offered to provide screen recordings
 * [today](https://github.com/microsoft/TypeScript-go/issues/2503#issuecomment-3751004372) **jansedlon** shared four videos demonstrating tsserver, native TS branch, and their fix performance, and asked how stable Typescript LSP performance should be
 * [today](https://github.com/microsoft/TypeScript-go/issues/2503#issuecomment-3752145034) **gabritto** requested a repro project or CPU profile log to investigate JSX completions slowness

### [Issue microsoft/TypeScript-go#2504](https://github.com/microsoft/TypeScript-go/issues/2504) (Open)

**TS4023 "cannot be named" \- tsgo not allowing references to unexported types**

*TypeScript-Go misreports TS4023 for exported wrappers that infer unexported types via Parameters<typeof> from another module.*

 * created by **johnpyp**

### [Issue microsoft/TypeScript-go#2505](https://github.com/microsoft/TypeScript-go/issues/2505) (Open)

**Circular type exported from namespace cannot be named**

*ts-go fails to generate declarations for a function using a circular namespace type alias, emitting an unnameable external type error.*

 * created by **Retsam**

### [Issue microsoft/TypeScript-go#2506](https://github.com/microsoft/TypeScript-go/issues/2506) (Open, `Domain: Editor`, **andrewbranch**)

**Stale module resolution error after linking pnpm workspace dependency due to watcher configuration/handling**

*VS Code’s watcher ignoring directory-level symlink events outside its file-extension glob causes stale module resolution errors after pnpm workspace linking.*

 * created by **andrewbranch**
 * (today) **andrewbranch** added label `Domain: Editor`, and assigned to **andrewbranch**

### [PR microsoft/TypeScript-go#2507](https://github.com/microsoft/TypeScript-go/pull/2507) (Closed)

**Make GetSemanticDiagnosticsWithoutNoEmitFiltering concurrent again**

*Revert commit #2314 to re-enable concurrent processing in GetSemanticDiagnosticsWithoutNoEmitFiltering after tracing revealed it was mistakenly serialized.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2507#issuecomment-3752012965) **walkerdb** said "Tried a build on our internal repo, which was hitting https://github.com/microsoft/typescript-go/issues/2341 . This change does fix it!"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2508](https://github.com/microsoft/TypeScript-go/pull/2508) (Closed)

**Parse user preferences for completions tests**

*Update the fourslash conversion script to include user preferences in completions tests and fix a manually adjusted test.*

 * created by **gabritto**

### [PR microsoft/TypeScript-go#2509](https://github.com/microsoft/TypeScript-go/pull/2509) (Closed)

**fix\(docs\): builds actually require rust 1\.88 or higher**

*Specify in the documentation that builds require Rust 1.88 or higher due to updated napi dependencies.*

 * created by **walkerdb**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2510](https://github.com/microsoft/TypeScript-go/pull/2510) (Open)

**Replace regex\-based HTML entity parsing with handwritten code**

*Replace regex-based HTML entity parsing with custom handwritten code to eliminate regex usage.*

 * created by **jakebailey**

### [Issue microsoft/TypeScript-go#2511](https://github.com/microsoft/TypeScript-go/issues/2511) (Closed)

**Stale diagnostics on file reload**

*tsgo diagnostics remain stale in Neovim after reloading a changed file until it’s manually edited*

 * created by **frangio**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2511#issuecomment-3752232412) **jakebailey** said "Is neovim requesting diagnostics again? The language server only does pull diagnostics. We don't push anything, so this is up to the editor."
 * [later](https://github.com/microsoft/TypeScript-go/issues/2511#issuecomment-3755198534) **frangio** stated the client sent didClose, didOpen, and diagnostic messages, provided debug logs, and suggested the bug was caused by ignoring events.closeChange when bundled with events.openChange

### [PR microsoft/TypeScript-go#2512](https://github.com/microsoft/TypeScript-go/pull/2512) (Closed)

**Ignore non\-variable\-declarations in transformExpandoAssignment**

*Ensure transformExpandoAssignment ignores assignments that are not variable declarations.*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#2513](https://github.com/microsoft/TypeScript-go/pull/2513) (Closed)

**Support \`Object\.defineProperty\` for expando properties and CommonJS exports in JS files**

*Support Object.defineProperty for expando properties and CommonJS exports in JS files, with type, caching, and emit fixes.*

 * created by **ahejlsberg**

### [PR microsoft/TypeScript-go#2514](https://github.com/microsoft/TypeScript-go/pull/2514) (Open)

**fix: allow references to unexported types**

*Fix declaration emit errors when indirectly referencing unexported types by reusing existing type nodes*

 * created by **raimannma**
 * [later](https://github.com/microsoft/TypeScript-go/pull/2514#issuecomment-3754619979) **raimannma** agreed to the contributor license agreement by replying '@microsoft-github-policy-service agree'

