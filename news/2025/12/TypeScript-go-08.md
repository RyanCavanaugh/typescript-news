# Report for 2025-12-08 (Monday, December 8th, 2025)

29 different users commented on 74 different issues.

## Recommended Actions

 * Response Recommended
    * @debugtheworldbot asked about progress and reported an issue with the organize imports action in [microsoft/TypeScript-go#1615](https://github.com/microsoft/TypeScript-go/issues/1615#issuecomment-3631232480)
    * @maxkostow suggested exposing GOGC/GOMEMLIMIT settings in the VS Code extension until better defaults are available in [microsoft/TypeScript-go#1622](https://github.com/microsoft/TypeScript-go/issues/1622#issuecomment-3628462817)
    * @Knagis provided reproduction details and a workaround with --singleThreaded in [microsoft/TypeScript-go#1622](https://github.com/microsoft/TypeScript-go/issues/1622#issuecomment-3632620368)
    * @Azzerty23 provided a TS playground link demonstrating that removing optionality resolves the issue in [microsoft/TypeScript-go#2162](https://github.com/microsoft/TypeScript-go/issues/2162#issuecomment-3632929653)
    * @rubnogueira provided reproduction details in [microsoft/TypeScript-go#2189](https://github.com/microsoft/TypeScript-go/issues/2189#issuecomment-3629567310)
    * @rubnogueira reported that one dependency still errors after applying #1034 in [microsoft/TypeScript-go#2220](https://github.com/microsoft/TypeScript-go/issues/2220#issuecomment-3629578583)
    * @maxired asked if there is a setting for tsgo similar to typescript.tsserver.maxTsServerMemory in [microsoft/TypeScript-go#2239](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3628146107)
    * @maxired provided confirmation that the proposed solution worked in [microsoft/TypeScript-go#2239](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3628246716)
    * @maxired reported high memory usage of tsgo despite GOMEMLIMIT setting in [microsoft/TypeScript-go#2239](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3631565394)
    * @aem provided full tsconfig as requested in [microsoft/TypeScript-go#2265](https://github.com/microsoft/TypeScript-go/issues/2265#issuecomment-3629073177)
    * @aem offered to provide repro steps and requested access coordination in [microsoft/TypeScript-go#2265](https://github.com/microsoft/TypeScript-go/issues/2265#issuecomment-3629170279)
    * @aem asked whether to keep the issue open or rename it to track the high performance cost of source map generation functions in [microsoft/TypeScript-go#2265](https://github.com/microsoft/TypeScript-go/issues/2265#issuecomment-3629282410)
    * @tzjames reported errors and provided logs in [microsoft/TypeScript-go#2303](https://github.com/microsoft/TypeScript-go/issues/2303#issuecomment-3631905884)

## Activity Summary

### [PR microsoft/TypeScript-go#1556](https://github.com/microsoft/TypeScript-go/pull/1556) (Open)

**fix: improve panic message for unspecified ScriptKind in \`Parser::initializeState\`**

*Enhance the panic message in Parser::initializeState to include the filename when ScriptKind is unknown for easier debugging*

 * [17 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1556#issuecomment-3175656306) **jakebailey** said "I think we avoid including user-specified data in panics/throws just because that means we can't collect it for telemetry on errors. But maybe the old code already broke this rule?"
 * [17 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1556#issuecomment-3175792209) **camc314** noted that many panics include extra debugging info, provided counts of total panics and formatted panics, and asked if telemetry could match only the first part of the panic string
 * [17 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1556#issuecomment-3175851583) **jakebailey** pointed out that searching for just prints in panics isn't sufficient and mentioned that there is no current API, warning that usage comes without warranty and isn't optimized for external use
 * [today](https://github.com/microsoft/TypeScript-go/pull/1556#issuecomment-3630516495) **jakebailey** said "Honestly, I think we can just take this; NewSourceFile already panics with a filename. I would just merge from main, however."

### [Issue microsoft/TypeScript-go#1615](https://github.com/microsoft/TypeScript-go/issues/1615) (Open, `Domain: Editor`)

**VSCode Extension blocks Organize Imports**

*The TypeScript Native Preview VSCode extension prevents the Organize Imports command from working until disabled.*

 * [15 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1615#issuecomment-3211190101) **jakebailey** said "It's not blocked, it's just not implemented yet."
 * [15 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1615#issuecomment-3213526047) **richardbutler** said "Apologies, I didn't realise it was a responsibility of the loaded extension, I had assumed it was a VSCode native command."
 * **jakebailey** added label `Domain: Editor`
 * [later](https://github.com/microsoft/TypeScript-go/issues/1615#issuecomment-3631232480) **debugtheworldbot** said "Any progress? For now (v0.20251204.2) it shows No organize imports action available"

### [Issue microsoft/TypeScript-go#1622](https://github.com/microsoft/TypeScript-go/issues/1622) (Open, `Crash`, `Domain: Program`, `Domain: Performance`, **sheetalkamat**)

**\[bug\] \`tsgo \-\-build\` uses extreme amounts of memory**

*tsgo --build exhausts over 100GB of memory and crashes when building large monorepos with thousands of TypeScript projects*

 * [11 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1622#issuecomment-3321811729) **spanishpear** asked how to help test the PR and locate branch deploy options after experiencing the issue across projects
 * [11 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1622#issuecomment-3321860198) **sheetalkamat** said "You would need to build from https://github.com/microsoft/typescript-go/pull/1745 to test it out"
 * [10 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1622#issuecomment-3323629265) **mjames-c** cross-posted a reference, noted high memory usage but no longer OOMed, and asked if the default for --maxConcurrentProjects equals the number of CPU cores
 * [today](https://github.com/microsoft/TypeScript-go/issues/1622#issuecomment-3628462817) **maxkostow** mentioned that the LSP lacked --singleThreaded support, described tuning GOGC/GOMEMLIMIT via the VS Code extension, and suggested exposing these settings until better defaults exist
 * [later](https://github.com/microsoft/TypeScript-go/issues/1622#issuecomment-3632620368) **Knagis** reported the same issue with high memory usage and OOM when building ~1000 TS projects and noted that using --singleThreaded worked fine and remained faster than tsc

### [PR microsoft/TypeScript-go#1721](https://github.com/microsoft/TypeScript-go/pull/1721) (Closed)

**Add \`@types/node\` to extension**

*Add @types/node to the extension to support type definitions for Node’s path module.*

 * created by **mjbvz**
 * [today](https://github.com/microsoft/TypeScript-go/pull/1721#issuecomment-3630535269) **jakebailey** said "Is this PR still needed? The repo root has @types/node already."

### [PR microsoft/TypeScript-go#1734](https://github.com/microsoft/TypeScript-go/pull/1734) (Closed)

**fix\(checker\): apply discriminant\-based contextual typing for object literals \(fixes \#1727\)**

*Applies discriminant-based union narrowing to object literal contextual typing in tsgo to correctly type callback parameters.*

 * [11 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1734#issuecomment-3314960567) **arash-mosavi** expressed agreement with microsoft-github-policy-service
 * [11 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1734#issuecomment-3315161628) **arash-mosavi** described adding discriminant-based contextual typing and a reverse inference algorithm for indexed access types, added comprehensive tests and baselines, and asked for workflow approval
 * [11 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1734#issuecomment-3317843058) **ahejlsberg** said "@arash-mosavi Appreciate your PR, but unfortunately I don't think we want to merge it. See my explanation here: https://github.com/microsoft/typescript-go/issues/1727#issuecomment-3317815996."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#1947](https://github.com/microsoft/TypeScript-go/pull/1947) (Open)

**fix: panic in \`regexp\.MustCompile\` when building wildcarddirectories with non ascii characters**

*Handle non-ASCII characters in wildcard directory patterns to prevent regexp.MustCompile panics.*

 * [6 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1947#issuecomment-3444271531) **jakebailey** clarified that the latest commit didn't align with their intent to replace Go's regexp usage in getWildcardDirectories and asked if using regexp.QuoteMeta would suffice
 * [6 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1947#issuecomment-3446588651) **camc314** clarified intent to revert the previous commit, explained the necessity of escaping for GetRegularExpressionForWildcard, and updated wildcarddirectories to use regexp2
 * [6 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1947#issuecomment-3446876374) **jakebailey** said "Why does Strada not need the escaping change, though?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/1947#issuecomment-3630513577) **jakebailey** said "Honestly, this PR is probably fine. It would be good to make a test that would have crashed before. But, I would like to have this change upstreamed."

### [Issue microsoft/TypeScript-go#2054](https://github.com/microsoft/TypeScript-go/issues/2054) (Open, `Domain: Build Mode`, `Needs More Info`, **sheetalkamat**)

**Semantics of \-\-stopBuildOnErrors has changed, now stops build on first error, instead of first project**

*tsgo’s --stopBuildOnErrors now halts the build and suppresses errors after the first failure rather than only skipping subsequent projects.*

 * **jakebailey** added label `Domain: Build Mode`
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2054#issuecomment-3572680890) **sheetalkamat** said "can you please paste config of workspaces/lib/tsconfig.json .. does it have noEmitOnError"
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/2054#issuecomment-3576069209) **Raynos** noted that noEmitOnError was set to true in the tsconfig
 * [today](https://github.com/microsoft/TypeScript-go/issues/2054#issuecomment-3629345499) **sheetalkamat** requested a minimal repro and noted surprising ordering of semantic and declaration emit errors
 * **sheetalkamat** added label `Needs More Info`

### [Issue microsoft/TypeScript-go#2162](https://github.com/microsoft/TypeScript-go/issues/2162) (Closed, `Domain: Type Checking`, **ahejlsberg**)

**Type inference lost for callback parameter**

*Using ts-go configuration causes TypeScript to lose type inference for the organization plugin's sendInvitationEmail callback parameter.*

 * **jakebailey** assigned to **ahejlsberg**
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/2162#issuecomment-3614826616) **Azzerty23** provided a TypeScript code example demonstrating type inference differences in BetterAuth plugin options and related generic functions
 * [today](https://github.com/microsoft/TypeScript-go/issues/2162#issuecomment-3627069093) **ahejlsberg** mentioned that it failed with TS 6.0 nightly and provided a repro link
 * [today](https://github.com/microsoft/TypeScript-go/issues/2162#issuecomment-3627832636) **jakebailey** noted that bisect identified TypeScript pull request #58910 as the change, which backported a fix from the Go code that also addressed multiple TS issues Andarist had been working on
 * [today](https://github.com/microsoft/TypeScript-go/issues/2162#issuecomment-3628193990) **Andarist** noted that the change introduced a return type inference regression affecting contextual types, demonstrated by making 'options' non-optional, and suggested there might be a better fix
 * [later](https://github.com/microsoft/TypeScript-go/issues/2162#issuecomment-3632929653) **Azzerty23** demonstrated that removing optionality in the failing example made it work and provided a TS playground link

### [Issue microsoft/TypeScript-go#2177](https://github.com/microsoft/TypeScript-go/issues/2177) (Closed, `Domain: Editor`, **Copilot**)

**Differences/issues with Code Lens references**

*CodeLens shows 70 references in TS mode but only 31 in TSGO mode for the same GitLens file, indicating inconsistent reference counts.*

 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/2177#issuecomment-3614149905) **DanielRosenwasser** suggested wiring up find-all-references across projects similarly to server requests and provided a sample fourslash test as a starting example
 * **DanielRosenwasser** assigned to **Copilot**
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/2177#issuecomment-3614212798) **sheetalkamat** said "I am working on cross project implememtations and code lens right now"
 * (today) **sheetalkamat** closed the issue

### [Issue microsoft/TypeScript-go#2189](https://github.com/microsoft/TypeScript-go/issues/2189) (Open, `Domain: Editor`, **andrewbranch**)

**LSP doesn't offer auto\-importing packages**

*VS Code’s TypeScript LSP does not offer auto-import suggestions for installed packages like `typescript-result`, only built-in modules*

 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/2189#issuecomment-3614124821) **jansedlon** answered that the project was closed-source
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2189#issuecomment-3623465376) **kieranm** said "We are seeing a bit of slowness with import suggestions right now too. We have a pnpm monorepo which is closed source but we can give access privately if volunteers are needed!"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2189#issuecomment-3627394893) **andrewbranch** said "@kieranm that would be great! If you need an email for me, you can use my first name dot last name @microsoft.com."
 * [today](https://github.com/microsoft/TypeScript-go/issues/2189#issuecomment-3629567310) **rubnogueira** reproduced the issue in a monorepo with PNPM where imports were suggested on Ctrl + Space but not inserted until restarting the IDE

### [PR microsoft/TypeScript-go#2191](https://github.com/microsoft/TypeScript-go/pull/2191) (Closed)

**fix: Enable getExePath to work on Node 16**

*Enable getExePath compatibility on Node 16 to restore tsgo preview functionality*

 * [5 days ago](https://github.com/microsoft/TypeScript-go/pull/2191#issuecomment-3607606185) **aapoalas** noted that the package.json file had no engines field
 * [5 days ago](https://github.com/microsoft/TypeScript-go/pull/2191#issuecomment-3607619015) **jakebailey** said "There is, in _packages/native-preview/package.json."
 * [5 days ago](https://github.com/microsoft/TypeScript-go/pull/2191#issuecomment-3610150040) **aapoalas** thanked for pointing out the file location and fixed the package.json and formatting check
 * [later](https://github.com/microsoft/TypeScript-go/pull/2191#issuecomment-3631638131) **aapoalas** said "@jakebailey my apologies for the ping; need workflow approval at least :)"

### [Issue microsoft/TypeScript-go#2204](https://github.com/microsoft/TypeScript-go/issues/2204) (Closed, `Domain: Editor`)

**\[bug\] TSGO fails to follow re\-exports when finding references**

*TSGO does not follow re-exports when finding references, preventing accurate cross-module symbol resolution.*

 * created by **mjames-c**
 * **mjames-c** added label `Domain: Editor`
 * [later](https://github.com/microsoft/TypeScript-go/issues/2204#issuecomment-3632975979) **RohinBhargava** said "+1"

### [PR microsoft/TypeScript-go#2207](https://github.com/microsoft/TypeScript-go/pull/2207) (Closed)

**Port document symbol tests \+ fixes**

*Port Strada document symbol tests to Corsa baselines, fix failures, support expandos and name truncation, and document remaining differences.*

 * created by **gabritto**
 * (today) **gabritto** closed the issue

### [Issue microsoft/TypeScript-go#2220](https://github.com/microsoft/TypeScript-go/issues/2220) (Open)

**\[pnpm\] The inferred type of 'xxx' cannot be named without a reference to '\.pnpm/xxx'**

*tsgo 7.0.0-dev errors on inferring return types from PNPM-installed packages, requiring explicit annotations due to unnameable ".pnpm" path references.*

 * created by **aramissennyeydd**
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/2220#issuecomment-3614121652) **samdcoding** said "+1 we are seeing quite a few of these errors as well"
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/2220#issuecomment-3614655373) **brokenmass** showed that updating the customRender signature removed the error and detailed the inferred versus expected types
 * [today](https://github.com/microsoft/TypeScript-go/issues/2220#issuecomment-3629578583) **rubnogueira** said "#1034 solved some of my issues, but like the main post, I still have one specific dependency that has the same error."

### [PR microsoft/TypeScript-go#2225](https://github.com/microsoft/TypeScript-go/pull/2225) (Closed, **DanielRosenwasser**, **Copilot**)

**Fix CodeLens references to search across project references**

*Modify CodeLens to count references across projects by using a unified multi-project search helper.*

 * (4 days ago) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * [4 days ago](https://github.com/microsoft/TypeScript-go/pull/2225#issuecomment-3614946561) **Copilot** refactored the code to extract multi-project search logic into a reusable helper and updated handlers to use it
 * [today](https://github.com/microsoft/TypeScript-go/pull/2225#issuecomment-3628507874) **DanielRosenwasser** said "Closing in favor of #2235."
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#2235](https://github.com/microsoft/TypeScript-go/pull/2235) (Closed)

**Implementations, CodeLens, IncomingCalls across projects**

*Enable CodeLens, Implementations, and IncomingCalls features to work across multiple projects.*

 * created by **sheetalkamat**
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/2235#issuecomment-3618991016) **sheetalkamat** said "Failure is because of not correctly calling recover to assign request for panic. will take a look . "
 * (today) **sheetalkamat** closed the issue

### [Issue microsoft/TypeScript-go#2239](https://github.com/microsoft/TypeScript-go/issues/2239) (Open, `Needs More Info`)

**take too much memory**

*tsgo extension consumes about 17GB of RAM on macOS M1, causing heavy swapping and slowing VS Code.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3623769762) **abelcha** described experiencing the same issue with the bun repository
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3623793210) **jakebailey** said "This codebase isn't in JS, so the runtime you use to run it cannot be the problem "
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3623812556) **abelcha** clarified that the codebase includes some JS/TS code, resolved the memory issue by disabling the bundled Node resolver in TypeScript settings, and offered to provide logs or traces if needed
 * [today](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3628122354) **maxired** thanked abelcha for the suggestion and noted intent to try the settings; apologized to jakebailey and described the private repo as complex with TypeScript references across five to six projects and at least two levels of references
 * [today](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3628130328) **jakebailey** clarified that the setting did not apply when using the native preview extension, explained that Node was never involved in launching the language server in the new codebase, and suggested that tsgo was likely not enabled
 * [today](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3628146107) **maxired** said "@jakebailey what I can also tell you is that when I was using node, I had a typescript.tsserver.maxTsServerMemory to 3GB. Is there a similar setting for tsgo ?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3628151855) **jakebailey** said "No, there is no equivalent to that. #1808 perhaps."
 * [today](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3628246716) **maxired** confirmed that running vscode with the GOMEMLIMIT variable set worked, noted that 2048MiB was sufficient, and said they would report any further crashes
 * [later](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3631565394) **maxired** said "Actually even with GOMEMLIMIT=2048MiB, after half a day working, my tsgo would eat 13GB of ram, while I have only 6 files opened in vscode"

### [Issue microsoft/TypeScript-go#2241](https://github.com/microsoft/TypeScript-go/issues/2241) (Closed, `Crash`, **gabritto**, **Copilot**)

**Crash when code contains disposer logic\. Request textDocument/inlayHint failed\.**

*The TypeScript Go LSP panics on inlayHint requests for disposer logic code after encountering an unexpected PropertyAccessExpression.*

 * **jinliming2** added label `Crash`
 * **jakebailey** assigned to **Copilot**
 * **gabritto** assigned to **gabritto**
 * (today) **gabritto** closed the issue

### [Issue microsoft/TypeScript-go#2245](https://github.com/microsoft/TypeScript-go/issues/2245) (Closed, `Domain: JS`, `Crash`, **ahejlsberg**)

**Folding range crash in JS file for \`exports\.property = CallExpression\(ObjectLiteral\)\`**

*The TypeScript Go LSP panics computing folding ranges for an export assignment call expression with an object literal.*

 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/2245#issuecomment-3618910449) **DanielRosenwasser** noted a similar issue using module.exports = {} that caused a token cache mismatch error
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/2245#issuecomment-3620827969) **DanielRosenwasser** said "Maybe something related to how we re-parse JS constructs for TS?"
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/2245#issuecomment-3621034523) **jakebailey** said "Yes, I think the astnav caching is incorrect given it's only based on positions"
 * (today) **RyanCavanaugh** added label `Crash`, and assigned to **navya9singh**

### [Issue microsoft/TypeScript-go#2248](https://github.com/microsoft/TypeScript-go/issues/2248) (Closed, `Crash`, **DanielRosenwasser**)

**Crash from ATA followed by request with no file\-watching client capability**

*TypeScript language server crashes when handling documentSymbol requests after initializing without file-watching capabilities and repeatedly opening and closing a file.*

 * **DanielRosenwasser** assigned to **DanielRosenwasser**
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/2248#issuecomment-3619501950) **DanielRosenwasser** attributed the crash to WatchedFiles not being initialized due to a missing didChangeWatchedFiles in his script and noted uncertainty about why earlier snapshot creation didn’t crash
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/2248#issuecomment-3619508434) **DanielRosenwasser** said "Looks like it's not about repeating the operation, it's about waiting until ATA finishes. If you run the commands and wait long enough after running, it triggers the crash. I have a fix."
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#2251](https://github.com/microsoft/TypeScript-go/pull/2251) (Open)

**  Fix: Add mutex protection for projects map to prevent race conditions**

*Add mutex-based read and write locking for the API projects map to prevent concurrent data races.*

 * created by **Catsayer-Chan**
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/2251#issuecomment-3619729436) **microsoft-github-policy-service[bot]** reminded the contributor to read and agree to the Contributor License Agreement by replying with the specified command
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/2251#issuecomment-3619742802) **Catsayer-Chan** said " @microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2251#issuecomment-3629402303) **jakebailey** said "Where are you using this API such that it matters for you? It's not guaranteed to work and I'm not sure we are expecting people to use it truly concurrently on the client side yet?"

### [PR microsoft/TypeScript-go#2252](https://github.com/microsoft/TypeScript-go/pull/2252) (Closed)

**Make \`\(\*WatchedFiles\[T\]\)\.Clone\` propagate \`nil\`**

*Modify the Clone method of WatchedFiles[T] to return nil when the receiver is nil.*

 * created by **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2252#issuecomment-3628513697) **jakebailey** said "Where do we end up trying to call clone on nil? I can imagine this fix works, but I'm not sure why we even get that far"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2252#issuecomment-3628650734) **sheetalkamat** described where typingsWatch is used in DidUpdateATAState to gather and watch ATA files
 * [today](https://github.com/microsoft/TypeScript-go/pull/2252#issuecomment-3628724962) **DanielRosenwasser** explained that when the workspace.didChangeWatchedFiles capability is not set, the server disables WatchEnabled and conditionally omits typings and other watchers, so the watcher isn’t always created
 * (today) **DanielRosenwasser** closed the issue

### [Issue microsoft/TypeScript-go#2254](https://github.com/microsoft/TypeScript-go/issues/2254) (Closed, `Crash`, **Copilot**)

**Completions crash in call to \`new Map\(\.\.\.\)\`\.**

*Requesting completions at array element positions in new Map(...) triggers an index-out-of-range panic in the typescript-go LSP server.*

 * created by **DanielRosenwasser**
 * (2 days ago) **DanielRosenwasser** added label `Crash`, and assigned to **Copilot**
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#2257](https://github.com/microsoft/TypeScript-go/pull/2257) (Open)

**fix\(2212\): make enum constant inlining consistent with Strada behavior**

*Adjust enum constant inlining implementation to match Strada behavior and resolve related inconsistencies.*

 * created by **a-tarasyuk**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2257#issuecomment-3628450472) **jakebailey** asked how much of the runtime changes were necessary to fix the linked issue and whether it was impossible to resolve
 * [today](https://github.com/microsoft/TypeScript-go/pull/2257#issuecomment-3628561180) **a-tarasyuk** suggested replicating evaluateEntity logic from the checker to resolve the issue without the full GetEnumMemberValue dependency

### [PR microsoft/TypeScript-go#2258](https://github.com/microsoft/TypeScript-go/pull/2258) (Closed, **DanielRosenwasser**, **Copilot**)

**Fix completions crash and enable contextual type completions in array literals**

*Prevent completions panic inside array literals (e.g., in Map constructors), enable contextual type-based suggestions for array elements and tuple contexts, and remove incorrect '-1' property completions.*

 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/2258#issuecomment-3621466169) **DanielRosenwasser** questioned whether this change belonged in the language service layer and described undesirable completions behavior for union literals
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/2258#issuecomment-3621466298) **DanielRosenwasser** said "@copilot try to address."
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/2258#issuecomment-3621474913) **Copilot** addressed completion issues after '[' in array literals by adding special handling for OpenBracketToken and CommaToken in the language service, preventing invalid tokens from reaching the checker and enabling string literal completions, all fixed in commit 90ca278a
 * [today](https://github.com/microsoft/TypeScript-go/pull/2258#issuecomment-3629565630) **jakebailey** said "Why does this need to differ so much from the original one in Strada?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2258#issuecomment-3629634281) **DanielRosenwasser** explained that indexing at -1 in JavaScript yields undefined, demonstrated a completions bug when using -1 index on a non-array-like type yielding string-literal suggestions, and requested Copilot to add a test case
 * [today](https://github.com/microsoft/TypeScript-go/pull/2258#issuecomment-3629677316) **Copilot** explained the JavaScript indexing rationale and added a test case verifying that properties named '-1' are not suggested, confirming the edge case fix
 * (today) **DanielRosenwasser** closed the issue

### [Issue microsoft/TypeScript-go#2260](https://github.com/microsoft/TypeScript-go/issues/2260) (Open, `Domain: Editor`)

**Inherited methods not merging JSDoc comments**

*tsgo fails to merge inherited JSDoc comments into overridden methods, showing only new @remarks tags.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2260#issuecomment-3621939537) **ahejlsberg** agreed that derived methods without JSDoc should inherit from base but cautioned against always merging inherited documentation due to potential confusion
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2260#issuecomment-3621953805) **ahejlsberg** explained that the old language service processed summary and remarks sections independently, causing mismatched inherited JSDoc and noted preference for the new behavior
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2260#issuecomment-3623586239) **LukeAbby** mentioned they had assumed the behavior was intentional and requested a way to simulate the old behavior with @inheritDoc, noting the pattern’s extensive use and clarifying the summary/remarks merging behavior
 * [today](https://github.com/microsoft/TypeScript-go/issues/2260#issuecomment-3628460459) **jakebailey** said "FWIW there is a PR for this in #2262. @LukeAbby does it do what you expect?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2260#issuecomment-3628872763) **LukeAbby** indicated that the PR didn't fully work due to literal JSDoc concatenation and suggested restoring old behavior or adding an opt-in for merging docs with @inheritDoc

### [PR microsoft/TypeScript-go#2264](https://github.com/microsoft/TypeScript-go/pull/2264) (Closed)

**Fix empty wildcard match on exports**

*Wildcard package.json exports with empty matches (e.g., './foo/*/index.js') cause a slice bounds out-of-range panic when resolving imports*

 * created by **lauckhart**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2264#issuecomment-3622535929) **lauckhart** agreed with microsoft-github-policy-service
 * [today](https://github.com/microsoft/TypeScript-go/pull/2264#issuecomment-3629388944) **jakebailey** asked if a test could be added for the fix and suggested replicating the original code approach

### [Issue microsoft/TypeScript-go#2265](https://github.com/microsoft/TypeScript-go/issues/2265) (Open)

**Sourcemap generation consuming significant resources while sourcemaps are disabled**

*tsgo build spends the majority of CPU time in source map emission functions despite sourceMap and declarationMap being disabled.*

 * created by **aem**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2265#issuecomment-3628832993) **jakebailey** attached two screenshot images
 * [today](https://github.com/microsoft/TypeScript-go/issues/2265#issuecomment-3628891104) **jakebailey** asked for the full config and whether inlineSourceMaps were enabled and noted poor performance
 * [today](https://github.com/microsoft/TypeScript-go/issues/2265#issuecomment-3629073177) **aem** mentioned that inline source maps were disabled, assumed sourceMap setting didn’t apply to declaration-only emits, and provided the full tsconfig
 * [today](https://github.com/microsoft/TypeScript-go/issues/2265#issuecomment-3629140180) **jakebailey** said "There's no reason whatsoever why this code should even be active for you. It would be very helpful if there were a repro of this that were public (or, something we could give you an NDA for)"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2265#issuecomment-3629170279) **aem** said "I'll see if I can get a minimal repro working in something public this evening, otherwise I can chat with folks internally to see if we can get you access to the repo for a bit to try and debug!"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2265#issuecomment-3629282410) **aem** explained that the issue was caused by a misconfigured project reference and asked whether to keep the issue open or rename/close and open a new one to address source map generation performance costs
 * [today](https://github.com/microsoft/TypeScript-go/issues/2265#issuecomment-3629367097) **jakebailey** noted that another repo with dts source map emit enabled would speed progress, mentioned TS string encoding benefits, and acknowledged the code was wrong
 * [today](https://github.com/microsoft/TypeScript-go/issues/2265#issuecomment-3629373435) **aem** said "Makes sense. Let me see if I can minimally repro the performance diff between "declarationMaps": true and "declarationMaps": false and I'll update here if I can do so"

### [PR microsoft/TypeScript-go#2267](https://github.com/microsoft/TypeScript-go/pull/2267) (Closed)

**Port \-\-stripInternal**

*Add support for the --stripInternal flag to the compiler to remove internal declarations from generated output.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2267#issuecomment-3628576832) **weswigham** noted that 7.0 improved --stripInternal support in JS by using the normal declaration emitter instead of the node builder so @internal is now respected
 * [today](https://github.com/microsoft/TypeScript-go/pull/2267#issuecomment-3628587945) **jakebailey** said "Yay better architecutre!"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2268](https://github.com/microsoft/TypeScript-go/pull/2268) (Closed)

**\[CHANGES\.md\] replace bitwise\-OR with logical\-OR for expando declarations**

*Use logical OR instead of bitwise OR for expando declarations in CHANGES.md since the current example is unintended and nonfunctional.*

 * created by **k-yle**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2269](https://github.com/microsoft/TypeScript-go/pull/2269) (Closed, `dependencies`, `github_actions`)

**Bump the github\-actions group across 1 directory with 3 updates**

*Update GitHub Actions dependencies in the root directory by bumping actions/checkout, setup-node, and codeql-action versions.*

 * (today) **dependabot[bot]** added labels `github_actions`, `dependencies`, `github_actions`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2270](https://github.com/microsoft/TypeScript-go/pull/2270) (Closed)

**Fix a typo in user preference parsing**

*Fix the casing typo in includeInlayFunctionParameterTypeHints so that the user preference is parsed correctly*

 * created by **indietyp**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2271](https://github.com/microsoft/TypeScript-go/issues/2271) (Closed, `bug`, `Domain: Declaration Emit`, **weswigham**)

**Invalid declaration emit for enum value type**

*tsgo generates invalid declaration files by emitting enum references as import(...).A instead of import(...).Teams.A, causing a namespace error.*

 * created by **jfirebaugh**
 * (today) **ahejlsberg** added labels `Domain: Declaration Emit`, `bug`, and assigned to **weswigham**

### [PR microsoft/TypeScript-go#2272](https://github.com/microsoft/TypeScript-go/pull/2272) (Open)

**Revamp user preferences serialization/deserialization**

*Refactor user preferences serialization to use struct tags and reflection enabling JSON round-trip and nested configurations.*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#2273](https://github.com/microsoft/TypeScript-go/pull/2273) (Closed)

**Fix inlay hints crash with property access expression**

*Support identifiers and property/element access expressions in computed property names to fix inlay hints crash.*

 * created by **gabritto**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2273#issuecomment-3628421862) **gabritto** said "Forgot to push the baselines 🙁"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2273#issuecomment-3628497997) **DanielRosenwasser** noted that using a computed property name with Symbol[...] still caused an inlay hint crash and suggested adding an early guard for unsupported node types
 * [today](https://github.com/microsoft/TypeScript-go/pull/2273#issuecomment-3628522030) **gabritto** asked how the provided code sample crashes and noted inability to reproduce with their PR
 * [today](https://github.com/microsoft/TypeScript-go/pull/2273#issuecomment-3628617559) **gabritto** asked how the crash occurred, said they couldn't reproduce it with their PR, and said they would add a test for element accesses
 * [today](https://github.com/microsoft/TypeScript-go/pull/2273#issuecomment-3628640688) **DanielRosenwasser** clarified that inlay hints shouldn't be produced for certain declarations and suggested modifying visitVariableLikeDeclaration or isHintableDeclaration accordingly
 * [today](https://github.com/microsoft/TypeScript-go/pull/2273#issuecomment-3628688824) **gabritto** explained that the updated function only visited type nodes produced by the checker and thus only handled a limited number of well-formed ASTs
 * (today) **gabritto** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/2273#issuecomment-3628804271) **DanielRosenwasser** said "Oh, duh, I misunderstood, sorry."

### [PR microsoft/TypeScript-go#2274](https://github.com/microsoft/TypeScript-go/pull/2274) (Closed)

**Reenable fail\-fast in merge queues**

*Re-enable fail-fast in merge queues to abort remaining jobs immediately upon the first failure.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2275](https://github.com/microsoft/TypeScript-go/issues/2275) (Open, `Domain: Editor`, **sheetalkamat**)

**Race condition detected between program updates and ATA\(?\)**

*Concurrent program updates and automatic type acquisition operations trigger a race condition, causing unexpected completion responses.*

 * created by **DanielRosenwasser**
 * **DanielRosenwasser** assigned to **sheetalkamat**

### [Issue microsoft/TypeScript-go#2276](https://github.com/microsoft/TypeScript-go/issues/2276) (Open)

**TS2742: The inferred type of 'default' cannot be named**

*Using tsgo to export stylex through a mapped type produces TS2742 errors requiring a default export type annotation.*

 * created by **jfirebaugh**

### [Issue microsoft/TypeScript-go#2277](https://github.com/microsoft/TypeScript-go/issues/2277) (Open)

**TS2742: The inferred type of \.\.\. cannot be named\.\.\.**

*pnpm's nested node_modules structure triggers TS2742 inferred type naming errors for Express handler exports under TSGo*

 * created by **jfirebaugh**

### [Issue microsoft/TypeScript-go#2278](https://github.com/microsoft/TypeScript-go/issues/2278) (Open)

**TS2305: Module '"@stylexjs/babel\-plugin"' has no exported member 'Options'\.**

*tsgo compilation reports TS2305 error saying '@stylexjs/babel-plugin' has no exported 'Options' member while TypeScript 5.9 does not*

 * created by **jfirebaugh**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2278#issuecomment-3628947678) **jakebailey** said "This package looks quite broken. https://arethetypeswrong.github.io/?p=%40stylexjs%2Fbabel-plugin%400.17.2"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2278#issuecomment-3628955187) **jakebailey** said "But, 5.9 and 6.0 do not seem to complain."

### [Issue microsoft/TypeScript-go#2279](https://github.com/microsoft/TypeScript-go/issues/2279) (Open, `Domain: Editor`, **gabritto**)

**Add snippet completions for methods**

*Implement snippet completions in ts-go so selecting a base class method suggestion inserts its full signature and stub.*

 * created by **mjbvz**
 * **gabritto** assigned to **gabritto**

### [Issue microsoft/TypeScript-go#2280](https://github.com/microsoft/TypeScript-go/issues/2280) (Open, `Domain: Editor`, **gabritto**)

**Port \`implement interface\` quick fix**

*Port the implement interface quick fix from TypeScript to TS-Go to provide automated interface implementation support.*

 * created by **mjbvz**
 * [later](https://github.com/microsoft/TypeScript-go/issues/2280#issuecomment-3632504763) **Tyriar** said "This is up there with most used quick fixes."

### [Issue microsoft/TypeScript-go#2281](https://github.com/microsoft/TypeScript-go/issues/2281) (Open, `Domain: Editor`)

**Port \`Convert parameters to destructed object\` refactoring**

*Assess porting of the Convert parameters to destructured object refactoring given its bugs and low usage or explore Copilot support.*

 * created by **mjbvz**

### [Issue microsoft/TypeScript-go#2282](https://github.com/microsoft/TypeScript-go/issues/2282) (Open)

**Request for official prebuilt Windows binaries \(tsgo\.exe\) published via GitHub Releases, without requiring npm\.**

*Officially distribute Windows tsgo.exe binaries via GitHub Releases to enable TypeScript use without npm.*

 * created by **PaulHuizer**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2282#issuecomment-3629095008) **jakebailey** said "Blazor? Are you just looking for a NuGet package?"
 * [later](https://github.com/microsoft/TypeScript-go/issues/2282#issuecomment-3630893984) **PaulHuizer** pondered delivering TsGo.exe via NuGet as an MsBuild target and suggested a tsgo.exe integrating into MsBuild to compile TypeScript
 * [later](https://github.com/microsoft/TypeScript-go/issues/2282#issuecomment-3631797657) **jakebailey** said "If you're using vue or any other lib, isn't it implied that you already are using npm?"

### [PR microsoft/TypeScript-go#2283](https://github.com/microsoft/TypeScript-go/pull/2283) (Closed)

**Fix perfromance when there's lots of error**

*Change DiagnosticsCollection to sort lazily before GetDiagnostics, replacing insertion sort to improve performance with many errors.*

 * created by **GabrielCastro**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2283#issuecomment-3629437536) **jakebailey** said "This looks fine, but you should run hereby format."
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2284](https://github.com/microsoft/TypeScript-go/issues/2284) (Closed, `Crash`, **ahejlsberg**)

**Crash in \`getBaseTypes\`**

*The TypeScript Go internal checker panics with a nil pointer dereference in getBaseTypes during type checking.*

 * created by **DorianListens**
 * **DorianListens** added label `Crash`

### [Issue microsoft/TypeScript-go#2285](https://github.com/microsoft/TypeScript-go/issues/2285) (Open, `Domain: Editor`)

**Backticked JSDOC \`{@link}\`s in tagless descriptions docblocks are broken**

*Backticked JSDoc {@link} tags in tagless description comments fail to render properly in VS Code hover tooltips.*

 * **vs-code-engineering[bot]** assigned to **mjbvz**
 * (21 weeks ago) **mjbvz** added labels `bug`, `javascript`
 * (today) **mjbvz** removed labels `bug`, `javascript`, and unassigned **mjbvz**

### [Issue microsoft/TypeScript-go#2286](https://github.com/microsoft/TypeScript-go/issues/2286) (Closed, `Crash`, **Copilot**)

**Panic in completions request within import attributes**

*The TypeScript-Go language server panics when requesting completions inside import attribute syntax due to an unhandled AST.ImportAttribute case.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** added label `Crash`, and assigned to **Copilot**

### [Issue microsoft/TypeScript-go#2287](https://github.com/microsoft/TypeScript-go/issues/2287) (Open, `Crash`)

**textDocument/codeAction Token cache mismatch: KindCloseBraceToken \!= KindCommaToken**

*textDocument/codeAction request panics due to token cache mismatch between close brace and comma tokens in the TypeScript-Go extension.*

 * created by **rubnogueira**
 * **rubnogueira** added label `Crash`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2287#issuecomment-3629966736) **DanielRosenwasser** asked for a full repro or high-level placeholders for the edited function and expected auto-imported functions
 * [today](https://github.com/microsoft/TypeScript-go/issues/2287#issuecomment-3630417535) **rubnogueira** said "Unfortunately I don't have a repro and I don't remember how I did it, but I will report here if it happens again."

### [PR microsoft/TypeScript-go#2288](https://github.com/microsoft/TypeScript-go/pull/2288) (Open)

**Use xxhash for composite checker keys instead of strings**

*Switch from string-based map keys to 128-bit xxhash keys to improve memory efficiency in Go composite type checking.*

 * created by **jakebailey**

### [Issue microsoft/TypeScript-go#2289](https://github.com/microsoft/TypeScript-go/issues/2289) (Closed, `Domain: JS`, `Crash`, **ahejlsberg**)

**Completions crash in JSDoc object type literal**

*Requesting completions inside a JSDoc object type literal crashes the TypeScript server due to a token cache mismatch.*

 * created by **DanielRosenwasser**
 * **DanielRosenwasser** added label `Crash`

### [Issue microsoft/TypeScript-go#2290](https://github.com/microsoft/TypeScript-go/issues/2290) (Open, `Domain: JS`, `Crash`)

**Crash for completions after JSDoc \`\*\` on line following string\-named property signature**

*TypeScript Go language server panics when requesting completions after a JSDoc asterisk following a string-named property signature.*

 * created by **DanielRosenwasser**
 * **DanielRosenwasser** added label `Crash`

### [PR microsoft/TypeScript-go#2291](https://github.com/microsoft/TypeScript-go/pull/2291) (Closed)

**chore: fix some minor issues in the comments**

*Address minor typos and inconsistencies in code comments across the repository.*

 * created by **xiaolinny**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2291#issuecomment-3630106168) **xiaolinny** said "@microsoft-github-policy-service agree"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2292](https://github.com/microsoft/TypeScript-go/pull/2292) (Closed)

**Use array for tokenToText**

*Switch tokenToText from a map to a fixed-size array to optimize profiling performance.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2293](https://github.com/microsoft/TypeScript-go/pull/2293) (Closed, **DanielRosenwasser**, **Copilot**)

**Fix panic in completions within import attributes**

*Replaced Node.Text() case with an explicit lambda in completions to prevent panics in import attribute suggestions.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **DanielRosenwasser**

### [Issue microsoft/TypeScript-go#2294](https://github.com/microsoft/TypeScript-go/issues/2294) (Closed, `Crash`, **DanielRosenwasser**)

**Crash for signature help in type arguments with any/unknown call target**

*Signature help for type arguments in calls with unknown or any targets crashes due to a nil pointer dereference.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** added label `Crash`, and assigned to **DanielRosenwasser**

### [PR microsoft/TypeScript-go#2295](https://github.com/microsoft/TypeScript-go/pull/2295) (Closed)

**Fix signature help crash for type arguments when call target is unresolved**

*Handle unresolved call targets to prevent signature help from crashing when type arguments are provided.*

 * created by **DanielRosenwasser**

### [Issue microsoft/TypeScript-go#2296](https://github.com/microsoft/TypeScript-go/issues/2296) (Closed, `Crash`, **Copilot**)

**Crash for completions after end of array literal when contextually typed by tuple**

*Requesting completions immediately after a tuple-typed array literal triggers an index out-of-range panic in the TypeScript-Go LSP*

 * created by **DanielRosenwasser**
 * (later) **DanielRosenwasser** added label `Crash`, and assigned to **Copilot**

### [PR microsoft/TypeScript-go#2297](https://github.com/microsoft/TypeScript-go/pull/2297) (Closed, **DanielRosenwasser**, **Copilot**)

**Fix completion crash after closing bracket in contextually\-typed array literals**

*Completion after a tuple-typed array literal’s closing bracket crashes due to unhandled CloseBracketToken causing an out-of-range error.*

 * created by **Copilot**
 * (later) **Copilot** assigned to **Copilot**, **DanielRosenwasser**

### [PR microsoft/TypeScript-go#2298](https://github.com/microsoft/TypeScript-go/pull/2298) (Closed)

**Format errors in \`\(\*Server\)\.recover\`\.**

*Formatting errors in the Server.recover method lead to incorrect data recovery.*

 * created by **DanielRosenwasser**

### [Issue microsoft/TypeScript-go#2299](https://github.com/microsoft/TypeScript-go/issues/2299) (Open, `Crash`, **sheetalkamat**)

**Crash on find\-all\-references on \`this\`**

*VS Code's find-all-references on the `this` keyword panics with a slice bounds out of range error.*

 * created by **DanielRosenwasser**
 * **DanielRosenwasser** added label `Crash`

### [Issue microsoft/TypeScript-go#2300](https://github.com/microsoft/TypeScript-go/issues/2300) (Closed, `Crash`)

**Inlay hints crash with element access name**

*TypeScript’s inlay hints feature crashes when encountering element access property names like Symbol['dispose'].*

 * created by **DanielRosenwasser**
 * **DanielRosenwasser** added label `Crash`

### [Issue microsoft/TypeScript-go#2301](https://github.com/microsoft/TypeScript-go/issues/2301) (Open, `Crash`, **andrewbranch**)

**Crash for value usage of type\-only import**

*TypeScript language service crashes when completing or resolving a type-only import used as a value.*

 * created by **DanielRosenwasser**
 * **DanielRosenwasser** added label `Crash`
 * [later](https://github.com/microsoft/TypeScript-go/issues/2301#issuecomment-3632258226) **Twacqwq** suggested rewriting the logic in Go and linked to the relevant TypeScript code

### [PR microsoft/TypeScript-go#2302](https://github.com/microsoft/TypeScript-go/pull/2302) (Open)

**API over LSP implementation**

*Implements a TS-Go API over the Language Server Protocol using custom messages and lazy-loaded types and symbols.*

 * created by **aleksei-berezkin**
 * [later](https://github.com/microsoft/TypeScript-go/pull/2302#issuecomment-3631591516) **aleksei-berezkin** said "@microsoft-github-policy-service agree company="JetBrains""
 * [later](https://github.com/microsoft/TypeScript-go/pull/2302#issuecomment-3631609367) **microsoft-github-policy-service[bot]** informed that the issued command was incorrect and provided correct usage examples
 * [later](https://github.com/microsoft/TypeScript-go/pull/2302#issuecomment-3631616041) **aleksei-berezkin** said "@microsoft-github-policy-service agree company="JetBrains""

### [Issue microsoft/TypeScript-go#2303](https://github.com/microsoft/TypeScript-go/issues/2303) (Open)

**Silently stopped evaluating files\.**

*tsgo silently fails to report missing type references in .d.ts files, while the standard TypeScript extension still catches them.*

 * created by **tzjames**
 * [later](https://github.com/microsoft/TypeScript-go/issues/2303#issuecomment-3631905884) **tzjames** reported that the service crashed more widely, then restarted and resumed working, and provided the error stack trace

