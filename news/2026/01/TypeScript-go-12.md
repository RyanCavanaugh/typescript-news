# Report for 2026-01-12 (Monday, January 12th, 2026)

22 different users commented on 48 different issues.

## Recommended Actions

 * Response Recommended
    * @marcomow reported an error with Deno 2.6.4 and provided an error stack trace in [microsoft/TypeScript-go#1905](https://github.com/microsoft/TypeScript-go/issues/1905#issuecomment-3744284117)
    * @marvinroger confirmed that the PR fixed the issue on their 40-package monorepo in [microsoft/TypeScript-go#2233](https://github.com/microsoft/TypeScript-go/issues/2233#issuecomment-3739458196)
    * @hilja reported that the package.json imports field was not respected in [microsoft/TypeScript-go#2422](https://github.com/microsoft/TypeScript-go/issues/2422#issuecomment-3744313385)
    * @rubnogueira reported a crash when opening a Gruntfile.js require line in [microsoft/TypeScript-go#2460](https://github.com/microsoft/TypeScript-go/issues/2460#issuecomment-3743948547)
    * @WonderPanda asked if they could email the lockfile to andrewbranch in [microsoft/TypeScript-go#2467](https://github.com/microsoft/TypeScript-go/issues/2467#issuecomment-3739596731)
    * @jansedlon asked if the logs help and offered to send lockfile in [microsoft/TypeScript-go#2467](https://github.com/microsoft/TypeScript-go/issues/2467#issuecomment-3739666156)
    * @jansedlon provided requested information in [microsoft/TypeScript-go#2467](https://github.com/microsoft/TypeScript-go/issues/2467#issuecomment-3740528696)
    * @marvinroger confirmed that the PR fixes issue #2233 in [microsoft/TypeScript-go#2471](https://github.com/microsoft/TypeScript-go/pull/2471#issuecomment-3739466810)
    * @ThinaticSystem confirmed that the rename symbol feature works correctly after the fix in [microsoft/TypeScript-go#2472](https://github.com/microsoft/TypeScript-go/pull/2472#issuecomment-3739608588)
    * @rubnogueira provided error log confirming the issue in [microsoft/TypeScript-go#2473](https://github.com/microsoft/TypeScript-go/issues/2473#issuecomment-3741052287)
    * @surajrimal07 reported a similar error with logs in [microsoft/TypeScript-go#2473](https://github.com/microsoft/TypeScript-go/issues/2473#issuecomment-3742529672)
    * @lukpsaxo reported a recurring panic after #2482 was fixed in [microsoft/TypeScript-go#2473](https://github.com/microsoft/TypeScript-go/issues/2473#issuecomment-3743143024)
    * @christophe-g reported continued occurrences of the issue after #2482 fix in [microsoft/TypeScript-go#2473](https://github.com/microsoft/TypeScript-go/issues/2473#issuecomment-3743155751)
    * @pedro757 reported the issue still present in version 7.0.0-dev.20260113.1 in [microsoft/TypeScript-go#2473](https://github.com/microsoft/TypeScript-go/issues/2473#issuecomment-3743892331)
    * @bessey reported the same panic error and provided logs and environment details in [microsoft/TypeScript-go#2497](https://github.com/microsoft/TypeScript-go/issues/2497#issuecomment-3744162368)
    * @christophe-g pointed out it was probably the same as issue #2473 in [microsoft/TypeScript-go#2497](https://github.com/microsoft/TypeScript-go/issues/2497#issuecomment-3744908092)

## Activity Summary

### [Issue microsoft/TypeScript-go#1080](https://github.com/microsoft/TypeScript-go/issues/1080) (Closed, `Domain: Program`)

**Deduplicate doubly\-installed packages**

*Duplicated installations of the same npm package across workspaces lead to instances TypeScript tolerates but break Go type compatibility.*

 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/1080#issuecomment-3724795743) **rubenferreira97** added a data point, reported the same private property error, confirmed PR #2361 fixed it, and asked for an ETA on when it would land
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/1080#issuecomment-3725768729) **chriskrycho** warned that using private class fields to resolve the issue is dangerous and risks runtime bugs and advised confirming no runtime bugs
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/1080#issuecomment-3725939108) **rubenferreira97** thanked the maintainer, explained that aliasing Kysely triggered an error despite being the same class and version, and said they might create a simple repro
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#1905](https://github.com/microsoft/TypeScript-go/issues/1905) (Open, `Crash`, **sheetalkamat**)

**panic: vfs: path is not absolute**

*The VFS implementation panics when given a URL-based path because it expects an absolute filesystem path.*

 * **RyanCavanaugh** assigned to **sheetalkamat**
 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1905#issuecomment-3604712273) **IOLOII** shared a configuration map
 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1905#issuecomment-3604718075) **IOLOII** reported a crash when opening JavaScript or TypeScript files in a Vue project using the plugin and offered to provide repro steps later
 * [later](https://github.com/microsoft/TypeScript-go/issues/1905#issuecomment-3744284117) **marcomow** reported a similar issue when using Deno 2.6.4 with --unstable-tsgo and provided the resulting RPC panic stack trace

### [Issue microsoft/TypeScript-go#2011](https://github.com/microsoft/TypeScript-go/issues/2011) (Closed, `Crash`, **jakebailey**)

**"panic: interface conversion: interface is nil, not fs\.FileInfo" in internal/execute/tsctests tests**

*The tsctests in internal/execute panic because a nil interface is incorrectly cast to fs.FileInfo.*

 * created by **jakebailey**
 * **jakebailey** added label `Crash`
 * **RyanCavanaugh** assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2011#issuecomment-3740811651) **jakebailey** said "This was fixed by #2056"
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2233](https://github.com/microsoft/TypeScript-go/issues/2233) (Closed, `Domain: Declaration Emit`, **weswigham**)

**Project references indirect dependencies: Error 2742 Inferred type of xxx \.\.\.**

*tsgo reports a TS2742 error when a package infers a type from an indirect project reference without directly referencing the originating package*

 * [1 month ago](https://github.com/microsoft/TypeScript-go/issues/2233#issuecomment-3649895000) **jordan-cutler** disabled project references by setting composite to false, shared related research links, and asked if the issue was specific to ts-go
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/2233#issuecomment-3725740998) **marvinroger** clarified that the errors occur with npm as well as pnpm, Yarn, and Bun and noted that the issue persists in version 7.0.0-dev.20260108.1
 * [today](https://github.com/microsoft/TypeScript-go/issues/2233#issuecomment-3738637535) **fubhy** reported encountering the same issue with the new Effect codebase and traced it to a small fix in the typescript-go repository
 * [today](https://github.com/microsoft/TypeScript-go/issues/2233#issuecomment-3739458196) **marvinroger** said "@fubhy thanks for this! I can confirm that your PR fixes the issue on our side, on a 40 packages monorepo"
 * (today) **jakebailey** closed the issue
 * [later](https://github.com/microsoft/TypeScript-go/issues/2233#issuecomment-3743192670) **marvinroger** noted that the issue was fixed in version 7.0.0-dev.20260113.1 and thanked fubhy for the quick fix

### [PR microsoft/TypeScript-go#2361](https://github.com/microsoft/TypeScript-go/pull/2361) (Closed)

**Add package deduplication, \-\-deduplicatePackages**

*Implement optional package deduplication via --deduplicatePackages by replacing duplicate package ASTs during collectFiles to match legacy compiler behavior.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2366](https://github.com/microsoft/TypeScript-go/issues/2366) (Closed)

**Diagnostics not shown in file peek views**

*Reference peek views in TypeScript no longer display diagnostics such as deprecation warnings across files.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2366#issuecomment-3659745686) **jrieken** said "Peek editors aren't tab-editors and I think the visible editors route needs to be taken here."
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2366#issuecomment-3669450168) **dbaeumer** fixed the issue in PR 1703 and announced a new next release for verification
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2366#issuecomment-3674604147) **dbaeumer** reported server and client version numbers
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2369](https://github.com/microsoft/TypeScript-go/issues/2369) (Closed, `Domain: Editor`, **DanielRosenwasser**)

**Code Lens provider registration error after switching tsdk location**

*Switching TypeScript SDK paths triggers a duplicate code lens command registration error and launches two language server instances.*

 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/2369#issuecomment-3731107235) **jakebailey** said "The command doesn't use the client at all. It should just be registered outside Client, unconditionally on extension activation."
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/2369#issuecomment-3731130662) **DanielRosenwasser** said "Sure, that one does and that's easy. I'm working on other stuff that the Client needs to manage though."
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/2369#issuecomment-3731135262) **jakebailey** said "All in all, I would personally say we should just require there only be one Client at a time, then use globals or something"
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#2390](https://github.com/microsoft/TypeScript-go/pull/2390) (Closed)

**New auto\-import infrastructure**

*Redesigns TypeScript's auto-import collection infrastructure to support snapshot-based LSP, parallelized data collection, and improved caching.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2390#issuecomment-3735316463) **jansedlon** reported not seeing a difference in autoimport speed after updating to the released version and shared logs from the Go version
 * [today](https://github.com/microsoft/TypeScript-go/pull/2390#issuecomment-3737965364) **rubnogueira** described resolving auto-import issues, noted a 3–4 second initial completion delay, and asked if it was expected behavior
 * [today](https://github.com/microsoft/TypeScript-go/pull/2390#issuecomment-3738018268) **jansedlon** mentioned restarting VSCode and updating from 0.20260111.1 to 0.20260112, then encountering issue #2467 and promised to report when it’s resolved
 * [today](https://github.com/microsoft/TypeScript-go/pull/2390#issuecomment-3741295763) **andrewbranch** announced that tonight's nightly would fix #2467, add the CPU profiling command for the TypeScript Native Preview, and invited users to send profiles via email
 * [later](https://github.com/microsoft/TypeScript-go/pull/2390#issuecomment-3742850259) **jansedlon** said "@andrewbranch  Thank you for fixing this 🙏 I have contacted you on email"

### [Issue microsoft/TypeScript-go#2399](https://github.com/microsoft/TypeScript-go/issues/2399) (Closed, `bug`, **DanielRosenwasser**)

**Implement JSX tag\-closing completions**

*JSX closing tag isn't auto-inserted when using tsgo but works with TypeScript 5.9.*

 * created by **navya9singh**
 * **navya9singh** added label `bug`
 * **DanielRosenwasser** assigned to **DanielRosenwasser**
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#2407](https://github.com/microsoft/TypeScript-go/pull/2407) (Open)

**Rewrite matchFiles to not use regexp2, remove other regexp uses**

*Rewrite matchFiles to remove regexp2 dependency and other regex uses, significantly improving file matching performance.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2407#issuecomment-3741353531) **jakebailey** said "This needs more work, unfortunately."

### [Issue microsoft/TypeScript-go#2422](https://github.com/microsoft/TypeScript-go/issues/2422) (Closed, `Domain: Editor`)

**Auto import does not respect paths**

*Auto import quick fix ignores tsconfig paths and non-relative import preference, using relative paths instead of aliases.*

 * **longzheng** added label `Domain: Editor`
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2422#issuecomment-3685387234) **Bashamega** prompted @longzheng to install the latest extension version and reported inability to reproduce the issue on version 0.20251204.2
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2422#issuecomment-3685399805) **longzheng** reported being on version 0.20251222.1 and that downgrading to version 0.20251204.1 also worked
 * [later](https://github.com/microsoft/TypeScript-go/issues/2422#issuecomment-3744313385) **hilja** noted that the imports field in package.json was not respected

### [PR microsoft/TypeScript-go#2429](https://github.com/microsoft/TypeScript-go/pull/2429) (Closed)

**fix\(2426\): goToDefinition for pattern ambient module no longer goes to implementation **

*goToDefinition for pattern-based ambient modules no longer navigates to their implementation.*

 * created by **a-tarasyuk**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2429#issuecomment-3741086466) **jakebailey** said "PR is failing because the failing tests need to be updated"

### [PR microsoft/TypeScript-go#2451](https://github.com/microsoft/TypeScript-go/pull/2451) (Closed)

**Port the \`jsxClosingTag\` command**

*Port the jsxClosingTag command in the TypeScript Go plugin to resolve issues 2369 and 2399.*

 * created by **DanielRosenwasser**
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/2451#issuecomment-3731398708) **DanielRosenwasser** considered redoing the feature as a server-to-client request and opted for a custom command due to testing infrastructure concerns
 * (today) **DanielRosenwasser** closed the issue

### [Issue microsoft/TypeScript-go#2460](https://github.com/microsoft/TypeScript-go/issues/2460) (Open, `Crash`)

**textDocument/inlayHint: Cannot create token from reparsed node of kind KindFunctionExpression**

*textDocument/inlayHint request panics due to inability to create a token from a reparsed function expression node*

 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/2460#issuecomment-3730012281) **jakebailey** said "Do you have a repro we can test?"
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/2460#issuecomment-3730026130) **a-tarasyuk** provided a minimal repro code example
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/2460#issuecomment-3730068931) **rubnogueira** asked if the provided repro was sufficient or if they should create a new one, and reported an intermittent inlayHint error when opening JS files
 * [later](https://github.com/microsoft/TypeScript-go/issues/2460#issuecomment-3743948547) **rubnogueira** reported a crash when opening Gruntfile.js at the require line

### [PR microsoft/TypeScript-go#2465](https://github.com/microsoft/TypeScript-go/pull/2465) (Closed)

**Update LSP client to 10\.0\.0\-next\.19**

*Upgrade the LSP client to version 10.0.0-next.19 to resolve issue #2366.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2467](https://github.com/microsoft/TypeScript-go/issues/2467) (Closed, `Crash`, **andrewbranch**)

**\[Panic Report\] : panic: module symbol has no non\-augmentation declaration**

*Panic occurs in TypeScript-Go autoimport when a module symbol lacks a non-augmentation declaration*

 * [today](https://github.com/microsoft/TypeScript-go/issues/2467#issuecomment-3738489291) **rvion** said "same; can't use tsgo at all on my project"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2467#issuecomment-3738502725) **gggdomi** said "Same issue here, using yarn. tsgo 0.20260112.1 via VSCode's typescriptteam.native-preview just crashes on launch."
 * [today](https://github.com/microsoft/TypeScript-go/issues/2467#issuecomment-3739018524) **WonderPanda** reported experiencing the issue with tsgo in an NX monorepo using pnpm and noted that downgrading to version 0.20260109.1 resolved the problem
 * **andrewbranch** assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2467#issuecomment-3739458216) **andrewbranch** suggested that someone share a repro, a pnpm lockfile, or build a branch from source with additional logging
 * [today](https://github.com/microsoft/TypeScript-go/issues/2467#issuecomment-3739596731) **WonderPanda** suggested possible fixes and asked andrewbranch if they could email the pnpm lockfile
 * [today](https://github.com/microsoft/TypeScript-go/issues/2467#issuecomment-3739666156) **jansedlon** added logs to the getModuleIDAndFileNameOfModuleSymbol function, posted the resulting error output, and offered to email their lockfile
 * [today](https://github.com/microsoft/TypeScript-go/issues/2467#issuecomment-3739728790) **andrewbranch** said "@jansedlon thank you! Could you print ast.GetSourceFileOfNode(symbol.Declarations[0]).FileName() as well? I think that should be enough to get me a repro."
 * [today](https://github.com/microsoft/TypeScript-go/issues/2467#issuecomment-3739987091) **andrewbranch** said "@WonderPanda or anyone else, you can email me at [firstname].[lastname]@microsoft.com"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2467#issuecomment-3740528696) **jansedlon** apologized for the delay and provided error logs and file content
 * [today](https://github.com/microsoft/TypeScript-go/issues/2467#issuecomment-3740863011) **andrewbranch** said "@jansedlon 🙏 thank you, I can repro with vitest@3.2.4. Will have a fix up for this soon."
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#2470](https://github.com/microsoft/TypeScript-go/issues/2470) (Closed, `Domain: Editor`)

**Rename symbol \(textDocument/rename\) fails for Class Private Elements \(\#\-prefixed fields, methods, etc\)**

*VS Code’s rename command fails to rename TypeScript class private fields, methods, and accessors prefixed with #.*

 * created by **ThinaticSystem**
 * **ThinaticSystem** added label `Domain: Editor`
 * (today) **gabritto** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/issues/2470#issuecomment-3739676740) **ThinaticSystem** thanked the maintainers for the fix, confirmed that it resolved the issue in their environment, and anticipated the next release

### [PR microsoft/TypeScript-go#2471](https://github.com/microsoft/TypeScript-go/pull/2471) (Closed)

**Fix module specifiers to use source file for project reference outputs**

*Use original source filenames instead of compiled outputs when generating module specifiers for project references to avoid TS2742 errors.*

 * created by **fubhy**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2471#issuecomment-3738628457) **fubhy** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2471#issuecomment-3739466810) **marvinroger** said "I  can confirm that this PR fixes the issue I have (#2233) on a 40 packages monorepo."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2471#issuecomment-3740367797) **jakebailey** suggested adding a test in TestBuildTransitiveReferences to verify that the error in tsgo-monorepo-reference-issue is resolved
 * [today](https://github.com/microsoft/TypeScript-go/pull/2471#issuecomment-3740552868) **jakebailey** provided a working unit test example demonstrating inferred types across monorepo project references
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2472](https://github.com/microsoft/TypeScript-go/pull/2472) (Closed)

**fix\(2470\): extend rename eligibility for additional node kinds**

*Extend rename feature to include class private elements by adding support for private identifier nodes.*

 * created by **a-tarasyuk**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2472#issuecomment-3739608588) **ThinaticSystem** thanked and verified the fix locally and confirmed the rename symbol feature worked correctly
 * (today) **gabritto** closed the issue

### [Issue microsoft/TypeScript-go#2473](https://github.com/microsoft/TypeScript-go/issues/2473) (Closed, `Crash`, **andrewbranch**)

**Autocompletion panics**

*Autocompletion and autoimport suggestions trigger a panic due to an unexpected internal symbol name in export.*

 * created by **pedro757**
 * **pedro757** added label `Crash`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2473#issuecomment-3741052287) **rubnogueira** reported encountering the same error and included the related stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/2473#issuecomment-3742529672) **surajrimal07** reported encountering a similar error and provided the stack trace
 * [later](https://github.com/microsoft/TypeScript-go/issues/2473#issuecomment-3743143024) **lukpsaxo** reported that after issue #2482 was fixed, tsgo now frequently panics with 'unexpected internal symbol name in export'
 * [later](https://github.com/microsoft/TypeScript-go/issues/2473#issuecomment-3743155751) **christophe-g** confirmed same behavior after fix to #2482 and apologized for inability to produce a repro
 * [later](https://github.com/microsoft/TypeScript-go/issues/2473#issuecomment-3743892331) **pedro757** reported that the issue was still present in version 7.0.0-dev.20260113.1

### [PR microsoft/TypeScript-go#2474](https://github.com/microsoft/TypeScript-go/pull/2474) (Closed)

**Add pprof commands to VS Code extension**

*Integrate pprof profiling commands into the VS Code extension to enable performance analysis.*

 * created by **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#2475](https://github.com/microsoft/TypeScript-go/pull/2475) (Closed)

**fix: use \`enclosingDeclaration\` for \`resolveName\` in \`trackComputedName\`**

*Replace the location parameter in trackComputedName's resolveName call with enclosingDeclaration to match TypeScript's implementation.*

 * created by **fubhy**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2475#issuecomment-3740196663) **jakebailey** said "The test in this PR passes even if I revert the checker change to main."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2475#issuecomment-3740204711) **fubhy** confirmed the fix worked on the Effect example and said they would fix the test
 * [today](https://github.com/microsoft/TypeScript-go/pull/2475#issuecomment-3740213733) **jakebailey** described original isAccessible function and expressed suspicion of changes, hoping the test would confirm that restoring the function closer to the original code would fix the issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/2475#issuecomment-3740371060) **fubhy** said "@jakebailey Looks like getExportSymbolOfValueSymbolIfExported is the key here."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2475#issuecomment-3740373717) **jakebailey** said "Yes, but that isn't mentioned in the original func that we are porting, no?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2475#issuecomment-3740480714) **fubhy** found where the code diverged between the TypeScript and Go implementations and shared the links
 * [today](https://github.com/microsoft/TypeScript-go/pull/2475#issuecomment-3740578068) **fubhy** shared the corresponding TypeScript code for the trackComputedName function
 * [today](https://github.com/microsoft/TypeScript-go/pull/2475#issuecomment-3740688906) **jakebailey** said "Good catch; can you update the PR title/description? The test does work to show the issue, thanks!"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2475#issuecomment-3740709607) **fubhy** agreed to update the PR title/description but reported that the updated test baseline files seemed borked
 * [today](https://github.com/microsoft/TypeScript-go/pull/2475#issuecomment-3740720510) **jakebailey** said "Yeah, something is regressing here, unfortunately."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2475#issuecomment-3740727133) **jakebailey** said "Ah, the func is missing the fallback case, no?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2475#issuecomment-3740759411) **fubhy** acknowledged the missing fallback case and thanked the commenter
 * [today](https://github.com/microsoft/TypeScript-go/pull/2475#issuecomment-3740761541) **fubhy** said "This should be it then. Thanks for the coaching!"
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2476](https://github.com/microsoft/TypeScript-go/issues/2476) (Open)

**TS4020 error with @ts\-ignore on imports needed for declaration emit**

*Using @ts-ignore on an import required for declaration emit causes tsgo to incorrectly report TS4020 errors.*

 * created by **fubhy**

### [PR microsoft/TypeScript-go#2477](https://github.com/microsoft/TypeScript-go/pull/2477) (Closed)

**Simplify getGlobalTypingsCacheLocation**

*Simplify getGlobalTypingsCacheLocation by relying solely on os.UserCacheDir instead of manual fallback logic.*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#2478](https://github.com/microsoft/TypeScript-go/pull/2478) (Open)

**Exit LSP process if parent process stops existing**

*Implement periodic parent process ID checks in the LSP server to terminate the server when the parent process exits.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2478#issuecomment-3741141626) **DanielRosenwasser** said "If the parent process no longer exists, won't we get an EOF on standard input or something?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2478#issuecomment-3741155153) **jakebailey** said "Yeah, I guess that's probably the case..."

### [PR microsoft/TypeScript-go#2479](https://github.com/microsoft/TypeScript-go/pull/2479) (Closed)

**Exhaustive case snippet completions**

*Add exhaustive case snippet completions with immediate additional text edits and import adder logic, skipping tests pending user preferences.*

 * created by **gabritto**

### [PR microsoft/TypeScript-go#2480](https://github.com/microsoft/TypeScript-go/pull/2480) (Closed)

**Align \`TypeFlags\` values in API package**

*Align TypeFlags values in the API package with the updated Go enum values introduced in PR 1226.*

 * created by **auvred**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2481](https://github.com/microsoft/TypeScript-go/pull/2481) (Closed)

**Clean up CI runner for build task too**

*Add cleanup steps to the CI runner for build tasks to address caching issues similar to those in issue 2464*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2482](https://github.com/microsoft/TypeScript-go/issues/2482) (Closed)

**LSP panic in autoimport: module symbol has no non\-augmentation declaration**

*The TypeScript language server panics with “module symbol has no non-augmentation declaration” during autoimport when completing after a dot.*

 * created by **adri1wald**
 * (today) **jakebailey** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/issues/2482#issuecomment-3740695612) **jakebailey** said "Duplicate of #2467"

### [PR microsoft/TypeScript-go#2483](https://github.com/microsoft/TypeScript-go/pull/2483) (Open)

**Log missing file when extended config cache ref would panic**

*Add logging for missing files to prevent panics when extended config cache references fail to load.*

 * created by **andrewbranch**

### [PR microsoft/TypeScript-go#2484](https://github.com/microsoft/TypeScript-go/pull/2484) (Closed)

**Fix race condition in ProjectCollection\.ConfigFileRegistry**

*A race condition in ProjectCollection.ConfigFileRegistry causes intermittent CI failures and requires synchronization fixes.*

 * created by **fubhy**
 * (today) **fubhy** closed the issue

### [PR microsoft/TypeScript-go#2485](https://github.com/microsoft/TypeScript-go/pull/2485) (Closed)

**Fix race condition in ProjectCollection\.ConfigFileRegistry**

*Resolve intermittent CI failures caused by a race condition in ProjectCollection.ConfigFileRegistry.*

 * created by **fubhy**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2485#issuecomment-3742369544) **fubhy** identified more unrelated race conditions in CI and noted a mutex scope issue in flushChanges
 * [today](https://github.com/microsoft/TypeScript-go/pull/2485#issuecomment-3742561407) **fubhy** mentioned additional race conditions in CI and attempted to fix one by adjusting the mutex scope in flushChanges

### [PR microsoft/TypeScript-go#2486](https://github.com/microsoft/TypeScript-go/pull/2486) (Closed)

**Fix re\-exported module augmentation auto import crash**

*Auto-import no longer crashes on module augmentation re-exports by using merged symbols and a non-panicking utility function.*

 * created by **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#2487](https://github.com/microsoft/TypeScript-go/issues/2487) (Closed, **jakebailey**, **Copilot**)

**Document outline no longer generates nice names for callbacks in tests**

*VSCode document outline no longer generates descriptive test callback names with TS-go, showing only generic “test() callback” labels.*

 * created by **mjbvz**
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#2488](https://github.com/microsoft/TypeScript-go/pull/2488) (Closed, **jakebailey**, **Copilot**)

**Include string literal arguments in document outline callback names**

*Include string and template literal arguments in anonymous test callback names in the document outline.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#2489](https://github.com/microsoft/TypeScript-go/issues/2489) (Closed, `Crash`, **andrewbranch**)

**Unprompted panic from auto\-import indexing**

*Language server auto-import indexing panics with “Cannot index entry with empty name” during stress testing on the webpack repository*

 * created by **DanielRosenwasser**
 * **DanielRosenwasser** added label `Crash`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2489#issuecomment-3741608996) **DanielRosenwasser** provided reproduction steps for a panic in the typescript-native-preview output pane when editing generate-wasm-code.js in the webpack repository
 * **DanielRosenwasser** assigned to **andrewbranch**

### [Issue microsoft/TypeScript-go#2490](https://github.com/microsoft/TypeScript-go/issues/2490) (Open, `Crash`, **DanielRosenwasser**, **Copilot**)

**Completions panic \(nil pointer\) in JSDoc union return type of method with params**

*Completions request causes a nil pointer panic in the language server for JSDoc function types with union return types.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** added label `Crash`, and assigned to **Copilot**, **DanielRosenwasser**

### [PR microsoft/TypeScript-go#2491](https://github.com/microsoft/TypeScript-go/pull/2491) (Open, **DanielRosenwasser**, **Copilot**)

**Fix nil pointer panic in JSDoc callable type completions**

*Add a nil check before accessing paramSymbol.Name to avoid crashes during JSDoc callable type completions with parameters.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2491#issuecomment-3741753660) **DanielRosenwasser** said "I feel like the investigation here is good but I don't understand why the parameter didn't have a symbol."

### [Issue microsoft/TypeScript-go#2492](https://github.com/microsoft/TypeScript-go/issues/2492) (Closed, `Crash`, **DanielRosenwasser**, **Copilot**)

**Signature help crash for signature with binding pattern parameters**

*Signature help panics when encountering binding pattern parameters in function signatures due to an unhandled AST case.*

 * created by **DanielRosenwasser**
 * **DanielRosenwasser** added label `Crash`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2492#issuecomment-3741762237) **DanielRosenwasser** suggested that a missing test might explain the lack of graceful printing of binding patterns and their types, as was done in the old codebase
 * (today) **DanielRosenwasser** assigned to **Copilot**, **DanielRosenwasser**

### [PR microsoft/TypeScript-go#2493](https://github.com/microsoft/TypeScript-go/pull/2493) (Open, **DanielRosenwasser**, **Copilot**)

**Fix slice bounds panic in find\-all\-references for \`this\` across files**

*Add validation and fallback search to prevent slice bounds panics when finding 'this' references across multiple files.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2493#issuecomment-3742393331) **DanielRosenwasser** said "@copilot This needs a test case that always fails without the fix."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2493#issuecomment-3742468916) **Copilot** added a test case reproducing the panic when using a large-file container to search a small file, showing it panics without the fix and succeeds with it
 * [today](https://github.com/microsoft/TypeScript-go/pull/2493#issuecomment-3742522497) **DanielRosenwasser** said "@copilot no, we prefer a "fourslash"-style test. Create a language service test with // @filename: ... etc."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2493#issuecomment-3742575608) **Copilot** replaced the test with a fourslash-style test in commit 5e5f67e and described its use of // @Filename directives to verify cross-file 'this' references

### [PR microsoft/TypeScript-go#2494](https://github.com/microsoft/TypeScript-go/pull/2494) (Closed, **DanielRosenwasser**, **Copilot**)

**Fix signature help crash for binding pattern parameters**

*Fixes a crash in signature help when encountering binding pattern parameters by adding pattern checks and comprehensive tests.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2494#issuecomment-3742381878) **DanielRosenwasser** said "@copilot actually make it possible to review what the signature help is - use VerifyBaselineSignatureHelp (or create it if it doesn't yet exist)."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2494#issuecomment-3742429568) **Copilot** updated the test to use VerifyBaselineSignatureHelp and added a baseline file showing signature help output for all binding pattern cases
 * [later](https://github.com/microsoft/TypeScript-go/pull/2494#issuecomment-3742871708) **DanielRosenwasser** said "@copilot address."

### [PR microsoft/TypeScript-go#2495](https://github.com/microsoft/TypeScript-go/pull/2495) (Closed)

**Fix race condition between flush and snapshot update**

*A race condition between flush and snapshot updates caused stale completions and test failures, now resolved by adding a mutex.*

 * created by **fubhy**

### [Issue microsoft/TypeScript-go#2496](https://github.com/microsoft/TypeScript-go/issues/2496) (Closed)

**Crashes on every syntax error**

*TypeScript-native server crashes whenever syntax errors occur, requiring a restart for each error.*

 * created by **sjtsh**
 * [later](https://github.com/microsoft/TypeScript-go/issues/2496#issuecomment-3743149995) **lukpsaxo** said "the actual panic i think is missing from your snippet but it looks the same as #2473"

### [Issue microsoft/TypeScript-go#2497](https://github.com/microsoft/TypeScript-go/issues/2497) (Closed)

**LSP panic in autoimport: unexpected internal symbol name in export**

*LSP autoimport feature panics with 'unexpected internal symbol name in export' during code completion.*

 * created by **adri1wald**
 * [later](https://github.com/microsoft/TypeScript-go/issues/2497#issuecomment-3744162368) **bessey** reported experiencing the same panic error and clarified using zod@4 instead of posthog-node
 * [later](https://github.com/microsoft/TypeScript-go/issues/2497#issuecomment-3744908092) **christophe-g** said "Probably same as #2473"

### [PR microsoft/TypeScript-go#2498](https://github.com/microsoft/TypeScript-go/pull/2498) (Open)

**Declaration \(d\.ts\) output diff breakdown as seen in \`effect\`**

*Comparison of tsc and tsgo declaration file outputs highlighting syntax and type alias differences in the Effect v4 codebase.*

 * created by **fubhy**
 * [later](https://github.com/microsoft/TypeScript-go/pull/2498#issuecomment-3744922224) **jakebailey** said "You should test with #2459, this is still a WIP area"

