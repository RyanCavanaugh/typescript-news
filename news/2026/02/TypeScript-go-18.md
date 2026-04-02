# Report for 2026-02-18 (Wednesday, February 18th, 2026)

14 different users commented on 34 different issues.

## Recommended Actions

 * Response Recommended
    * @jbeaudoin-lf asked for support for require & module.exports composition to be ported to the new compiler or a new compilerOption in [microsoft/TypeScript-go#1685](https://github.com/microsoft/TypeScript-go/issues/1685#issuecomment-3921701899)
    * @johnnycheng0210 asked why the old configuration persisted when switching back to a single project config in [microsoft/TypeScript-go#2020](https://github.com/microsoft/TypeScript-go/pull/2020#issuecomment-3924761855)
    * @johnnycheng0210 asked whether requiring a window reload between config changes is preferred in [microsoft/TypeScript-go#2020](https://github.com/microsoft/TypeScript-go/pull/2020#issuecomment-3924764987)
    * @privatenumber provided repro steps and real-world impact data as requested in [microsoft/TypeScript-go#2701](https://github.com/microsoft/TypeScript-go/issues/2701#issuecomment-3927069363)
    * @jlaneve provided detailed investigation results clarifying the root cause of the errors in [microsoft/TypeScript-go#2830](https://github.com/microsoft/TypeScript-go/issues/2830#issuecomment-3924340752)
    * @jlaneve provided repro steps in [microsoft/TypeScript-go#2830](https://github.com/microsoft/TypeScript-go/issues/2830#issuecomment-3924382349)

## Activity Summary

### [Issue microsoft/TypeScript-go#1685](https://github.com/microsoft/TypeScript-go/issues/1685) (Open, `Domain: Type Checking`, `Domain: JS`, **sandersn**)

**\`ts\-check\` used with \`@typedef\` causes an error on \`module\.exports = \.\.\.\`**

*Combining @ts-check and @typedef in a CommonJS file causes a TS2309 export assignment error with tsgo.*

 * [16 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1685#issuecomment-3462917504) **jakebailey** said "#1688 would have fixed this but was closed"
 * [15 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1685#issuecomment-3470371464) **jakebailey** provided a test case demonstrating the variant of the problem with sample files, compiler errors, and behavior differences when removing module.exports
 * [15 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1685#issuecomment-3470397129) **jakebailey** suggested using `module.exports.nothing = undefined` as a workaround for type-only files to generate separate declarations
 * [today](https://github.com/microsoft/TypeScript-go/issues/1685#issuecomment-3921701899) **jbeaudoin-lf** described encountering TS2309 errors when composing modules using require & module.exports under @ts-check and requested that the behavior be supported in the new compiler via compilerOptions

### [PR microsoft/TypeScript-go#2020](https://github.com/microsoft/TypeScript-go/pull/2020) (Open)

**Support for custom configurations**

*Enable passing custom tsconfig file names to the tsgo LSP to support solution-style repository configurations.*

 * [15 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2020#issuecomment-3493021126) **jakebailey** said "I'm not sure what happened with your PRs, but can you keep the one you intend us to look at open and keep pushing to that one?"
 * [14 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2020#issuecomment-3499951692) **johnnycheng0210** said "ah sorry - i was rebasing PR's - i will close the previous PR and use this one instead"
 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2020#issuecomment-3746994608) **jakebailey** said "One thing this might be missing is some handling of on-change events; (*Session).Configure handles things; maybe pendingConfigChanges is sufficient to catch this?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2020#issuecomment-3924738291) **jakebailey** tested a TypeScript configuration change with a custom tsconfig and observed that disabling strict removed the error but undoing the config didn't refresh diagnostics until restart, which he found suspicious
 * [today](https://github.com/microsoft/TypeScript-go/pull/2020#issuecomment-3924761855) **johnnycheng0210** reported similar behavior with findAllReferences when switching project configurations, observed that results didn't update after reverting to single project config, and asked why the old configuration persisted
 * [today](https://github.com/microsoft/TypeScript-go/pull/2020#issuecomment-3924764987) **johnnycheng0210** wondered if requiring a window reload between custom config file name changes would be preferred as a simpler approach

### [Issue microsoft/TypeScript-go#2636](https://github.com/microsoft/TypeScript-go/issues/2636) (Closed, **jakebailey**, **Copilot**)

**tsgo emits a \`require\` statement when a value is imported without the \`type\` keyword but only used in type\-level positions**

*tsgo incorrectly emits a require call for value imports used only in type positions, causing unwanted side effects at runtime.*

 * created by **psm14**
 * (2 weeks ago) **jakebailey** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2664](https://github.com/microsoft/TypeScript-go/pull/2664) (Closed, **DanielRosenwasser**, **Copilot**)

**Fix panic on negative indentation in JSDoc formatting within nested scopes**

*The JSDoc formatter panics on sentinel negative indentation in nested scopes, so negative indentation now short-circuits formatting.*

 * created by **Copilot**
 * (2 weeks ago) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#2673](https://github.com/microsoft/TypeScript-go/pull/2673) (Closed)

**Remove isElisionBlocked**

*Remove the outdated isElisionBlocked function to resolve import elision conflicts after splitting transformers.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2684](https://github.com/microsoft/TypeScript-go/issues/2684) (Closed, `Crash`, **andrewbranch**, **Copilot**)

**nil source file in aliasResolve\.GetSourceFile**

*A nil source file causes a segmentation fault in aliasResolver.GetSourceFile during module resolution.*

 * **jakebailey** added label `Crash`
 * (2 weeks ago) **andrewbranch** assigned to **andrewbranch**, **Copilot**
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#2701](https://github.com/microsoft/TypeScript-go/issues/2701) (Open)

**Declaration emit for named inferred types used in further inference inlines inferred types instead of naming them**

*tsgo inlines inferred types in declaration emit even when named, causing slower type checking in consuming packages.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/2701#issuecomment-3861931441) **chriskrycho** provided additional exploration showing that patching canReuseTypeNode() in Strada to always return false inlined types instead of reusing references
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/2701#issuecomment-3861992981) **jakebailey** said "I would expect this to be fixed by #1693 / #2459, then."
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/2701#issuecomment-3863092956) **chriskrycho** confirmed that the change fixes the issue and reduces type-check time by ~95% (from ~469s to ~24s)
 * [later](https://github.com/microsoft/TypeScript-go/issues/2701#issuecomment-3927069363) **privatenumber** provided additional reproduction steps and real-world impact data showing tsgo produces significantly larger declaration output and errors compared to tsc

### [PR microsoft/TypeScript-go#2813](https://github.com/microsoft/TypeScript-go/pull/2813) (Closed)

**New IPC API client features**

*Updates the TypeScript IPC API client to use immutable snapshots for state and lifecycle management and adds Go support code.*

 * created by **andrewbranch**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2813#issuecomment-3918014132) **andrewbranch** said "My handling of SourceFileAffectingOptions needs to be updated after Jake's changes in main. I think it wasn't quite right before, anyway."
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#2814](https://github.com/microsoft/TypeScript-go/pull/2814) (Closed, **andrewbranch**, **Copilot**)

**Fix nil pointer dereference in aliasResolver\.GetSourceFile**

*aliasResolver.GetSourceFile crashes when host.GetSourceFile returns nil due to symlink path mismatches in the auto-import cache*

 * (yesterday) **Copilot** assigned to **Copilot**, **andrewbranch**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2814#issuecomment-3918724221) **Copilot** rejected the race explanation and documented the file existence caching, symlink path mismatch theory, and nil-unsafe binder fix in commit 720f0d6b
 * [today](https://github.com/microsoft/TypeScript-go/pull/2814#issuecomment-3921704615) **Copilot** confirmed the stale cachedvfs theory didn't hold and described reproduction steps for a symlink path mismatch issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/2814#issuecomment-3921852238) **Copilot** deleted the investigation file, removed an unnecessary nil check, and added brief comments at the remaining nil checks
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#2815](https://github.com/microsoft/TypeScript-go/issues/2815) (Closed, `bug`, `Crash`, **DanielRosenwasser**, **Copilot**)

**Panic in signatureHelp for contextual signature help on methods/function expressions**

*Requesting contextual signature help on a constructor method expression triggers an index out of range panic.*

 * (yesterday) **DanielRosenwasser** added labels `bug`, `Crash`, and assigned to **DanielRosenwasser**
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#2816](https://github.com/microsoft/TypeScript-go/pull/2816) (Closed, **DanielRosenwasser**, **Copilot**)

**Fix panic in signature help for contextual signatures with only construct signatures**

*Use a length check to prevent index out of range panics in signature help when only construct signatures exist.*

 * created by **Copilot**
 * (yesterday) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#2823](https://github.com/microsoft/TypeScript-go/pull/2823) (Closed)

**Don't bundle extension package\.json, read from extension context**

*Don't bundle package.json into the extension and instead read it from the extension context to ensure publish info is updated.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2824](https://github.com/microsoft/TypeScript-go/issues/2824) (Open, `Domain: API and Extensibility`, **andrewbranch**)

**API usage patterns for complex editor extensions**

*Exploring IPC-based API features for a Go TS server to replace TS Server plugins and support Vue editor extensions*

 * created by **andrewbranch**
 * (today) **andrewbranch** added label `Domain: API and Extensibility`, and assigned to **andrewbranch**

### [Issue microsoft/TypeScript-go#2825](https://github.com/microsoft/TypeScript-go/issues/2825) (Open, `question`)

**How will native library dependencies's CVEs be handled?**

*How can pnpm audit expose CVEs in native Go module dependencies and help downstream users identify related supply-chain vulnerabilities?*

 * created by **philipwhiuk**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2825#issuecomment-3923737892) **DanielRosenwasser** stated that they would publish an appropriate patch if a dependency had a CVE, report risks with the prior version, and involve @jakebailey's input
 * **DanielRosenwasser** added label `question`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2825#issuecomment-3923751113) **jakebailey** noted encoding/json/v2 upcoming change, explained scanner over-reporting issues and govulncheck's advantages, and stated that forced rebuilds may be needed albeit unlikely given the small dependency set

### [PR microsoft/TypeScript-go#2826](https://github.com/microsoft/TypeScript-go/pull/2826) (Closed)

**Add replay test**

*Add a replay test and launch configuration to run fuzzer-generated replay scripts for convenient debugging with an optional replay flag.*

 * created by **gabritto**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2826#issuecomment-3923770808) **DanielRosenwasser** suggested using dlv exec instead of the usual binary path and noted that tsgo's Node.js startup complicates locating the native executable
 * [today](https://github.com/microsoft/TypeScript-go/pull/2826#issuecomment-3923875141) **gabritto** suggested running with dlv exec, reminded to use an unoptimized binary for debugging, and proposed relying on a repo test workflow unless the fuzzer client grows more complex
 * [today](https://github.com/microsoft/TypeScript-go/pull/2826#issuecomment-3924019220) **DanielRosenwasser** clarified that there was no optimization level, only differing build flags such as nodebug
 * [today](https://github.com/microsoft/TypeScript-go/pull/2826#issuecomment-3924022307) **DanielRosenwasser** said "Thinking about this some more, I think it's okay to have two replay scripts - one in the repo for ease of iteration, and one published on npm that's just JS/TS."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2826#issuecomment-3924023028) **jakebailey** clarified that there is an optimization level when using a debug build or launch task
 * [today](https://github.com/microsoft/TypeScript-go/pull/2826#issuecomment-3924028923) **DanielRosenwasser** said "I think we are saying the same thing - there's no -O3 vs -O0, but there are times where the build differs based on race-detection, assertion checks, etc., right?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2826#issuecomment-3924033190) **jakebailey** said "The default build Go does is effectively -O3. Launching with delve (or, building with build:debug) is effectively -O0 -g."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2826#issuecomment-3924036109) **jakebailey** said "This doesn't really have to be a test, though, since you can use a go run task (like we have for tsgo) that takes args."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2826#issuecomment-3924062674) **gabritto** pointed out that making it not a test would slightly complicate reuse of the LSP client
 * [today](https://github.com/microsoft/TypeScript-go/pull/2826#issuecomment-3924064421) **jakebailey** acknowledged that avoiding a test would require introducing a new main package, noting it would be icky but feasible
 * (today) **gabritto** closed the issue

### [Issue microsoft/TypeScript-go#2827](https://github.com/microsoft/TypeScript-go/issues/2827) (Closed, `Crash`, **andrewbranch**)

**panic handling request completionItem/resolve: completion list needs auto imports**

*A panic occurs in completionItem/resolve due to missing auto imports during Redocly/redoc fuzzer replay.*

 * created by **gabritto**
 * **gabritto** added label `Crash`
 * **andrewbranch** assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2827#issuecomment-3924128232) **DanielRosenwasser** reproduced a completions crash after fiddling with settings and noted that custom.d.ts was included in tsconfig.json while styled-patch.d.ts was not

### [Issue microsoft/TypeScript-go#2828](https://github.com/microsoft/TypeScript-go/issues/2828) (Closed)

**"panic: Debug failure\. False expression: Token end is child end" in CI**

*CI panics with 'Token end is child end' assertion failure in the TypeScript-Go formatter, and the failing test is unknown.*

 * created by **jakebailey**

### [Issue microsoft/TypeScript-go#2829](https://github.com/microsoft/TypeScript-go/issues/2829) (Open)

**\[ServerErrors\]\[TypeScript\] linux\-x64\-7\.0\.0\-dev\.20260218\.1 vs **

*The linux-x64-7.0.0-dev.20260218.1 TypeScript pipeline reported 76 interesting changes, 59 unchanged results, 6 clone failures, 158 timeouts, and 1 unknown failure when analyzing 300 popular repositories.*

 * created by **typescript-bot**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2829#issuecomment-3924076422) **typescript-bot** reported a panic handling request completionItem/resolve due to completion list needing auto imports
 * [today](https://github.com/microsoft/TypeScript-go/issues/2829#issuecomment-3924076461) **typescript-bot** reported a panic during completionItem/resolve with an auto imports error and provided a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/2829#issuecomment-3924076503) **typescript-bot** reported a panic when handling completionItem/resolve and included a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/2829#issuecomment-3924076545) **typescript-bot** reported a panic in completionItem/resolve due to missing auto imports
 * [today](https://github.com/microsoft/TypeScript-go/issues/2829#issuecomment-3924076582) **typescript-bot** reported a panic in request handling for completionItem/resolve due to missing auto imports
 * [today](https://github.com/microsoft/TypeScript-go/issues/2829#issuecomment-3924076619) **typescript-bot** reported panic handling request completionItem/resolve due to completion list needing auto imports
 * [today](https://github.com/microsoft/TypeScript-go/issues/2829#issuecomment-3924076658) **typescript-bot** reported a panic during completionItem/resolve due to missing auto imports and included a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/2829#issuecomment-3924076704) **typescript-bot** reported a panic handling completionItem/resolve due to completion list needing auto imports
 * [today](https://github.com/microsoft/TypeScript-go/issues/2829#issuecomment-3924076735) **typescript-bot** reported a panic handling request textDocument/completion due to a missing cache entry and provided a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/2829#issuecomment-3924076762) **typescript-bot** reported a panic when handling textDocument/completion due to inability to create token from reparsed node of kind KindTypeLiteral
 * [today](https://github.com/microsoft/TypeScript-go/issues/2829#issuecomment-3924076793) **typescript-bot** reported a runtime panic due to invalid memory address or nil pointer dereference in textDocument/completion handling
 * [today](https://github.com/microsoft/TypeScript-go/issues/2829#issuecomment-3924076825) **typescript-bot** reported a server connection closed prematurely error on elastic/kibana and provided artifact references, replay commands, last requests, and repro steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/2829#issuecomment-3924076864) **typescript-bot** reported server connection closed prematurely and provided affected repos, logs, and repro steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/2829#issuecomment-3924076907) **typescript-bot** reported a server connection closed prematurely error on facebook/docusaurus with related logs, requests, and reproduction steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/2829#issuecomment-3924126975) **gabritto** said ""panic handling request completionItem/resolve: completion list needs auto imports" is in #2827"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2829#issuecomment-3924192677) **gabritto** noted that 'Server connection closed prematurely: undefined' errors seemed to be OOMs and said they would update the message accordingly, pointed to PR #2826 for debugging replays, and described manual fixes to replay files due to a fuzzer issue

### [Issue microsoft/TypeScript-go#2830](https://github.com/microsoft/TypeScript-go/issues/2830) (Open, `Type Ordering`)

**TS2859/TS2590: bigint template literal types composed with distributive conditional cause 'excessively deep' errors not present in tsc**

*bigint-based template literal types in JSX props cause tsgo to report excessive type complexity errors but not tsc*

 * created by **jlaneve**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2830#issuecomment-3924340752) **jlaneve** updated that bigint template literals were not the cause and identified unresolved distributive conditional types as the trigger for the TS2590/TS2859 errors
 * [today](https://github.com/microsoft/TypeScript-go/issues/2830#issuecomment-3924359307) **jakebailey** said "Do you have a repro that doesn't involve pulling in any imports?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2830#issuecomment-3924360036) **jlaneve** explained that the error was caused by tsgo’s instantiation limit being hit due to unresolved distributive conditional types combined with Chakra Input’s complex responsive props and confirmed the root cause was not Chakra-specific
 * [today](https://github.com/microsoft/TypeScript-go/issues/2830#issuecomment-3924382349) **jlaneve** provided a minimal repro demonstrating that the type complexity of InputProps triggers TS errors
 * [today](https://github.com/microsoft/TypeScript-go/issues/2830#issuecomment-3924386199) **jlaneve** said "in the spirit of transparency these comments / repros were generated with the help of claude code, but I figured it'd be worth posting because this is a real issue we're running into"

### [PR microsoft/TypeScript-go#2831](https://github.com/microsoft/TypeScript-go/pull/2831) (Closed)

**\[@typescript/api\] Batch of Checker and Type APIs**

*Add TypeScript API enhancements with checker queries, intrinsic type getters, symbol fetchers, type hierarchy classes, and new enums and flags.*

 * created by **andrewbranch**

### [Issue microsoft/TypeScript-go#2832](https://github.com/microsoft/TypeScript-go/issues/2832) (Closed)

**SIGSEGV \(segmentation fault\) on Linux when type\-checking @tanstack/react\-table \+ @chakra\-ui/react generic component**

*Type-checking a package using @tanstack/react-table and @chakra-ui/react generics causes tsgo to crash with a segmentation fault on Linux.*

 * created by **jlaneve**
 * (today) **jlaneve** closed the issue

### [PR microsoft/TypeScript-go#2833](https://github.com/microsoft/TypeScript-go/pull/2833) (Closed)

**Fix infinite forEachChild loop on some nodes in JS API **

*Caching nodes by text position instead of node index causes an infinite forEachChild loop in the JS API.*

 * created by **auvred**

### [PR microsoft/TypeScript-go#2834](https://github.com/microsoft/TypeScript-go/pull/2834) (Closed)

**Optimize bool to byte conversion in API encoder**

*Optimize the Go API encoder by replacing slow bool-to-byte conversions with a more efficient implementation.*

 * created by **auvred**

### [PR microsoft/TypeScript-go#2835](https://github.com/microsoft/TypeScript-go/pull/2835) (Closed)

**6\.4x speedup of AST materialization in JS API**

*Several optimizations in the JavaScript API speed up AST materialization by 6.4× and correct benchmarks by resetting the source file cache.*

 * created by **auvred**

### [Issue microsoft/TypeScript-go#2836](https://github.com/microsoft/TypeScript-go/issues/2836) (Open)

**Cache \`getExePath\(\)\` for performance reasons**

*Cache getExePath results to avoid redundant lookups and improve tsgo invocation performance.*

 * created by **tido64**

### [PR microsoft/TypeScript-go#2837](https://github.com/microsoft/TypeScript-go/pull/2837) (Closed)

**Clone comment list of reparsed JSDoc comments**

*Clone the comment list of reparsed JSDoc comments to prevent the reported crash.*

 * created by **ahejlsberg**

### [Issue microsoft/TypeScript-go#313](https://github.com/microsoft/TypeScript-go/issues/313) (Open, `Domain: Binder`)

**binder: expando declarations don't show up on symbol**

*Expando declarations are not emitted on default exports, interface merges, overloaded functions, keyword-named expandos, or element accesses.*

 * created by **sandersn**
 * [52 weeks ago](https://github.com/microsoft/TypeScript-go/issues/313#issuecomment-2669908966) **sandersn** described the discrepancy in namespace declarations for `Point` between Strada and Corsa and proposed a synthetic JS-only namespace feature for `Point.zero`, outlining binder, checker, and language service requirements
 * **jakebailey** added label `Domain: Binder`
 * [today](https://github.com/microsoft/TypeScript-go/issues/313#issuecomment-3923610589) **ahejlsberg** noted that the binder was working as intended, pointed out remaining declaration emit differences captured in baselines, and asked to close the issue

### [Issue microsoft/TypeScript-go#314](https://github.com/microsoft/TypeScript-go/issues/314) (Closed, `Domain: Binder`)

**runner: module specifier \`"\./sub"\` of dynamic import has no symbol**

*Dynamic import specifier "./sub" lacks symbol resolution, leading to declaration emit failures for reexported namespaces and related expressions.*

 * created by **sandersn**
 * [52 weeks ago](https://github.com/microsoft/TypeScript-go/issues/314#issuecomment-2669927169) **sandersn** noted a minor difference in alias symbols for dynamic imports between Strada and Corsa and mentioned duplicate test failures due to issue #312
 * **jakebailey** added label `Domain: Binder`
 * [today](https://github.com/microsoft/TypeScript-go/issues/314#issuecomment-3923628546) **ahejlsberg** said "No differences in baselines at this point. Closing."
 * (today) **ahejlsberg** closed the issue

