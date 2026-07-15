# Report for 2026-07-09 (Thursday, July 9th, 2026)

17 different users commented on 24 different issues.

## Recommended Actions

 * Response Recommended
    * @HolgerJeromin provided the project file excerpt as requested in [microsoft/TypeScript-go#2310](https://github.com/microsoft/TypeScript-go/issues/2310#issuecomment-4934360048)
    * @remcohaszing asked about how plugin execution should work on Windows in [microsoft/TypeScript-go#2824](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-4933547787)
    * @eddking provided root cause analysis and linked fix in #4578 in [microsoft/TypeScript-go#4262](https://github.com/microsoft/TypeScript-go/issues/4262#issuecomment-4928897571)
    * @ibesuperv provided a link to a new PR with improved fixes in [microsoft/TypeScript-go#4274](https://github.com/microsoft/TypeScript-go/pull/4274#issuecomment-4935124288)
    * @AndrewMax reported that Yarn is creating a wrong symlink in [microsoft/TypeScript-go#4567](https://github.com/microsoft/TypeScript-go/issues/4567#issuecomment-4927500771)
    * @AndrewMax provided a minimal reproducible example repository in [microsoft/TypeScript-go#4567](https://github.com/microsoft/TypeScript-go/issues/4567#issuecomment-4928028399)
    * @AkisArou provided a proof-of-concept branch for optimizing watch initialization in [microsoft/TypeScript-go#4582](https://github.com/microsoft/TypeScript-go/pull/4582#issuecomment-4936667616)

## Activity Summary

### [Issue microsoft/TypeScript-go#2310](https://github.com/microsoft/TypeScript-go/issues/2310) (Open, `possible improvement`, **joj**)

**TypeScript for \.Net Projects**

*Custom MSBuild targets file and instructions to compile TypeScript 7 in .NET projects with tsgo until official support arrives.*

 * **RyanCavanaugh** added to milestone `Possible Improvement`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2310#issuecomment-4923231836) **HolgerJeromin** reported that the Microsoft.TypeScript.MSBuild 7.0.0-beta NuGet package worked but had a buggy TypeScript build configuration (missing module and target settings in TypeScriptProjectProperties.xaml), showed comparison images, and requested an updated package with TypeScript 7.0.2
 * [today](https://github.com/microsoft/TypeScript-go/issues/2310#issuecomment-4927037353) **joj** asked for more information about the setup and a build binlog, and explained the upcoming NuGet update and deprecated options
 * [later](https://github.com/microsoft/TypeScript-go/issues/2310#issuecomment-4934360048) **HolgerJeromin** described having old .csproj files with obsolete TypeScript settings that were ignored by ts-msbuild due to tsconfig.json and included a project XML excerpt

### [Issue microsoft/TypeScript-go#2824](https://github.com/microsoft/TypeScript-go/issues/2824) (Open, `Domain: API and Extensibility`, **andrewbranch**)

**API usage patterns for complex editor extensions**

*Exploring IPC-based API features for a Go TS server to replace TS Server plugins and support Vue editor extensions*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-4919145963) **andrewbranch** organized the issue into two separate discussions and clarified what’s already shipping in the unstable API preview
 * [today](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-4924997952) **dummdidumm** asked whether content mappers can be asynchronous and influence LSP features such as diagnostics and rename functionality, or if a separate Svelte LSP is needed to intercept and modify requests
 * [today](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-4925537831) **remcohaszing** addressed unanswered questions about diagnostics mapping, transformer config reliance, TS emit scenarios, and editor integration, and proposed reading the bugs field from package.json and constraining commands to node_modules packages
 * [today](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-4927211282) **andrewbranch** answered questions about async content mappers, LSP influence, JSON-RPC protocol, mapping limitations, and plugin loading in TypeScript
 * [today](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-4928456800) **andrewbranch** explained that parse errors in raw TS script blocks should be mapped correctly rather than treated as invalid plugin states
 * [later](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-4933547787) **remcohaszing** suggested expecting plugins to be executable and determined by their shebang, recommended against using 'bin' due to package manager symlinks, suggested a special field for browser import usage, and questioned how plugin execution should work on Windows
 * [later](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-4935519462) **bartlomieju** described Deno's need for a scheme-aware static mapping API for module resolution and declaration files and explained current workaround and its limitations

### [Issue microsoft/TypeScript-go#4262](https://github.com/microsoft/TypeScript-go/issues/4262) (Open, `bug`, `Needs More Info`)

**Non\-deterministic \`TS2305 "has no exported member"\` errors across project references with \`\-\-emitDeclarationOnly\`**

*Flaky TS2305 "has no exported member" errors occur when running --emitDeclarationOnly across project references in a pnpm monorepo using tsgo.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/4262#issuecomment-4715239745) **ibesuperv** identified the non-deterministic parsing order caused by Go map iteration, proposed sorting task keys for deterministic builds, and offered to submit a PR
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/4262#issuecomment-4715575995) **jakebailey** noted that task launch order shouldn't matter and requested a test to identify the bug
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/4262#issuecomment-4715657883) **ibesuperv** thanked jakebailey, explained the intended sorting within the locked section to handle non-deterministic iteration over casing variants, and said they would create and share a minimal reproducible test case
 * [today](https://github.com/microsoft/TypeScript-go/issues/4262#issuecomment-4928897571) **eddking** described the nondeterminism issue on macOS due to Realpath resolving hardlink siblings and linked the fix in #4578

### [Issue microsoft/TypeScript-go#4269](https://github.com/microsoft/TypeScript-go/issues/4269) (Closed, **DanielRosenwasser**, **Copilot**)

**Fatal error when project reference objects have unexpected types for \`path\` and \`circular\`**

*tsconfig parsing crashes when project references specify non-string values for path or circular properties.*

 * (1 month ago) **DanielRosenwasser** assigned to **Copilot**, **DanielRosenwasser**
 * **RyanCavanaugh** added to milestone `Post-7.0`
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#4274](https://github.com/microsoft/TypeScript-go/pull/4274) (Open, **ahejlsberg**)

**Fix CFA stack overflow crash in for loops where initializer throws**

*Add an early bailout in for-loop binding to avoid stack overflow when the initializer throws*

 * [1 month ago](https://github.com/microsoft/TypeScript-go/pull/4274#issuecomment-4686407223) **ibesuperv** addressed both review comments by adding dummy break/continue targets and a new test case in the latest commit
 * (3 weeks ago) **RyanCavanaugh** set milestone to `Post-7.0`, and assigned to **ahejlsberg**
 * (today) **ibesuperv** closed the issue
 * [later](https://github.com/microsoft/TypeScript-go/pull/4274#issuecomment-4935124288) **ibesuperv** explained that they accidentally synced and force-pushed their fork’s main branch, which closed the PR, and opened a new improved PR addressing previous review feedback

### [PR microsoft/TypeScript-go#4494](https://github.com/microsoft/TypeScript-go/pull/4494) (Closed)

**fix\(tsoptions\): validate project reference fields**

*Validate project reference path and circular options in tsconfig and report diagnostics for invalid or missing values.*

 * created by **TorinAsakura**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#4562](https://github.com/microsoft/TypeScript-go/pull/4562) (Closed)

**Fix concurrent extractionCache read/write**

*Unprotected reads of the shared extractionCache during @types fallback conflict with concurrent worker writes in registryBuilder.updateIndexes, causing data races.*

 * created by **johnfav03**
 * (today) **johnfav03** closed the issue

### [Issue microsoft/TypeScript-go#4567](https://github.com/microsoft/TypeScript-go/issues/4567) (Closed)

**\`tsc\` incorrectly points to v6 rather than v7**

*The npm alias setup for TypeScript 6 and 7 side-by-side assigns the tsc binary to version 6 instead of 7.*

 * [today](https://github.com/microsoft/TypeScript-go/issues/4567#issuecomment-4926594165) **AndrewMax** reported that the suggested config still didn't work and asked @RyanCavanaugh for help
 * [today](https://github.com/microsoft/TypeScript-go/issues/4567#issuecomment-4926910710) **RyanCavanaugh** said "@AndrewMax which package manager, and which version, are you running?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/4567#issuecomment-4927038067) **AndrewMax** specified package manager as Yarn Berry 4.17.1 and asked for advice on resolving the Yarn-related issue
 * [today](https://github.com/microsoft/TypeScript-go/issues/4567#issuecomment-4927500771) **AndrewMax** reported that Yarn created a wrong symlink
 * [today](https://github.com/microsoft/TypeScript-go/issues/4567#issuecomment-4927655404) **RyanCavanaugh** described differing bin conflict semantics across package managers, noted testing on an older Yarn version, and reported inability to prioritize version 7.0 for tsc via dependencies
 * [today](https://github.com/microsoft/TypeScript-go/issues/4567#issuecomment-4927717897) **RyanCavanaugh** suggested adding nmHoistingLimits: dependencies to .yarnrc.yml as a workaround
 * [today](https://github.com/microsoft/TypeScript-go/issues/4567#issuecomment-4928028399) **AndrewMax** provided a minimal reproducible example repository, noted a workaround and its drawback, and referenced a related issue
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#4570](https://github.com/microsoft/TypeScript-go/pull/4570) (Closed, **andrewbranch**, **Copilot**)

**Resolving unchecked assertion in parseProjectReference**

*Replace unchecked assertion in parseProjectReference with explicit validation to prevent runtime errors.*

 * created by **Copilot**
 * (yesterday) **Copilot** assigned to **Copilot**, **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4570#issuecomment-4930225699) **andrewbranch** said "Never mind, this brings parity with Strada but #4494 actually improves on Strada"
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#4577](https://github.com/microsoft/TypeScript-go/pull/4577) (Open)

**Fix stack overflow in inherited JSDoc resolution**

*Resolving inherited JSDoc without cycle detection can cause infinite recursion and stack overflow on circular class references.*

 * created by **johnfav03**

### [PR microsoft/TypeScript-go#4578](https://github.com/microsoft/TypeScript-go/pull/4578) (Open)

**Fix nondeterministic Realpath on darwin for hardlinked files**

*Deterministically resolve files with multiple hardlinks on macOS by reconstructing paths from parent directories to prevent intermittent resolution errors.*

 * created by **eddking**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4578#issuecomment-4928938584) **eddking** said "@microsoft-github-policy-service agree"

### [Issue microsoft/TypeScript-go#4579](https://github.com/microsoft/TypeScript-go/issues/4579) (Open)

**tsgo typechecks slower than TS6**

*tsgo typechecking is over five times slower than TypeScript 6 on the same codebase.*

 * created by **XiNiHa**

### [Issue microsoft/TypeScript-go#4580](https://github.com/microsoft/TypeScript-go/issues/4580) (Open, `Domain: Editor`)

**TS7 plugin is not working with Yarn 4 nodeLinker = pnp**

*TS7’s VSCode plugin and compiler fail to work with Yarn 4 PnP due to missing tsserver and inaccessible cached archives.*

 * created by **zuyetawarmatik**
 * **zuyetawarmatik** added label `Domain: Editor`

### [Issue microsoft/TypeScript-go#4581](https://github.com/microsoft/TypeScript-go/issues/4581) (Open)

**TS2719/TS2322 false positive on a generic type forwarded through an interface \`extends\` boundary \(tsc clean, tsgo fails\)**

*tsgo wrongly reports a TS2719/TS2322 type mismatch when extending and forwarding a library’s generic props interface despite tsc accepting it*

 * created by **alekseigoloviichuk**

### [PR microsoft/TypeScript-go#4582](https://github.com/microsoft/TypeScript-go/pull/4582) (Open)

**Call IsDirCoveredByWatch less often to improve performance**

*Improve tsc --watch performance by reducing redundant IsDirCoveredByWatch calls and optimizing directory caching*

 * created by **terite**
 * [later](https://github.com/microsoft/TypeScript-go/pull/4582#issuecomment-4936667616) **AkisArou** tested the PR with tsgo --build --watch in a large monorepo and observed that watches were not installed after five minutes; prepared a proof-of-concept branch adding an indexed DirectorySet and updating orchestrator.go to use the index, which made watch initialization immediate
 * [later](https://github.com/microsoft/TypeScript-go/pull/4582#issuecomment-4937051430) **terite** clarified that the PR only affected the tsgo --watch code path and explained reasons for not modifying the --build code path due to its prototype status and personal lack of usage

### [Issue microsoft/TypeScript-go#4583](https://github.com/microsoft/TypeScript-go/issues/4583) (Open)

**Some colors make error messages hard to read on white backgrounds\.**

*Diagnosticwriter’s forced bright ANSI color codes make error messages illegible on white backgrounds and should use default colors instead.*

 * created by **ayosec**
 * [later](https://github.com/microsoft/TypeScript-go/issues/4583#issuecomment-4934491424) **jakebailey** questioned whether the issue was new in v7 and linked to existing code

### [PR microsoft/TypeScript-go#4584](https://github.com/microsoft/TypeScript-go/pull/4584) (Open)

**binder: fix stack overflow in CFA when for\-loop initializer is unreachable**

*Prevent stack overflow in control-flow analysis when a for-loop initializer is unreachable by bailing out early to avoid cyclic CFGs.*

 * created by **ibesuperv**

### [Issue microsoft/TypeScript-go#4585](https://github.com/microsoft/TypeScript-go/issues/4585) (Open, `Domain: Editor`)

**Local auto\-imports disappear when a Yarn workspace dependency resolves a subpath back to the current project**

*TypeScript 7 in VS Code fails to suggest local auto-imports when a Yarn workspace dependency resolves a subpath back to the project.*

 * created by **sashamorozov**
 * **sashamorozov** added label `Domain: Editor`

