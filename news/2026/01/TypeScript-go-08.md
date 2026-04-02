# Report for 2026-01-08 (Thursday, January 8th, 2026)

14 different users commented on 20 different issues.

## Recommended Actions

 * Response Recommended
    * @rubenferreira97 asked for an ETA for merging PR #2361 in [microsoft/TypeScript-go#1080](https://github.com/microsoft/TypeScript-go/issues/1080#issuecomment-3724795743)
    * @tmcdo1 reported a similar issue with RequestedLanguageService and provided logs and config details in [microsoft/TypeScript-go#1967](https://github.com/microsoft/TypeScript-go/issues/1967#issuecomment-3725018741)
    * @marvinroger provided additional reproduction details confirming the issue occurs across package managers in [microsoft/TypeScript-go#2233](https://github.com/microsoft/TypeScript-go/issues/2233#issuecomment-3725740998)
    * @Yusuf007R asked if the feature was already released in [microsoft/TypeScript-go#2330](https://github.com/microsoft/TypeScript-go/pull/2330#issuecomment-3725219820)
    * @noelkim-prestolabs provided profiling results and attachments as requested in [microsoft/TypeScript-go#2454](https://github.com/microsoft/TypeScript-go/issues/2454#issuecomment-3726576005)
    * @noelkim-prestolabs provided repro steps as requested in [microsoft/TypeScript-go#2454](https://github.com/microsoft/TypeScript-go/issues/2454#issuecomment-3726653619)

## Activity Summary

### [Issue microsoft/TypeScript-go#1080](https://github.com/microsoft/TypeScript-go/issues/1080) (Closed, `Domain: Program`)

**Deduplicate doubly\-installed packages**

*Duplicated installations of the same npm package across workspaces lead to instances TypeScript tolerates but break Go type compatibility.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1080#issuecomment-3656907954) **jakebailey** acknowledged that their attempt couldn't resolve the symbols deduplication issue and that hacking the checker avoided some errors but didn't fix class nominality
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1080#issuecomment-3657175627) **jakebailey** said "@Benjamin-Dobell Can you try #2361 again? With the latest version, your example appears to work for me."
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1080#issuecomment-3658550958) **Benjamin-Dobell** confirmed that the example worked with the latest version and expressed appreciation, noting that typescript-go significantly benefits their large GodotJS-based TypeScript game project
 * [today](https://github.com/microsoft/TypeScript-go/issues/1080#issuecomment-3724795743) **rubenferreira97** added a data point, reported the same private property error, confirmed PR #2361 fixed it, and asked for an ETA on when it would land
 * [today](https://github.com/microsoft/TypeScript-go/issues/1080#issuecomment-3725768729) **chriskrycho** warned that using private class fields to resolve the issue is dangerous and risks runtime bugs and advised confirming no runtime bugs
 * [today](https://github.com/microsoft/TypeScript-go/issues/1080#issuecomment-3725939108) **rubenferreira97** thanked the maintainer, explained that aliasing Kysely triggered an error despite being the same class and version, and said they might create a simple repro

### [PR microsoft/TypeScript-go#1693](https://github.com/microsoft/TypeScript-go/pull/1693) (Open)

**Port \`\-\-isolatedDeclarations\` related node builder logic**

*Refactor and port isolatedDeclarations node builder logic to Go by adding a pseudochecker abstraction and enhancing reuseNode validation.*

 * created by **weswigham**
 * [today](https://github.com/microsoft/TypeScript-go/pull/1693#issuecomment-3726460827) **jakebailey** noted nothing objectionable, asked if pseudo concepts formalized previous logic, and pointed out a wrong emitMethodCalledNew diff
 * [today](https://github.com/microsoft/TypeScript-go/pull/1693#issuecomment-3726625796) **weswigham** provided updates on bugfixes, PR #2459 baseline update, and explained the pseudo type comparison logic with future improvements
 * [today](https://github.com/microsoft/TypeScript-go/pull/1693#issuecomment-3726656248) **weswigham** noted that --isolatedDeclarations support was partial and that error generation logic still needed porting; offered to add it but cautioned about large baseline diffs

### [Issue microsoft/TypeScript-go#1967](https://github.com/microsoft/TypeScript-go/issues/1967) (Open, `Crash`, **andrewbranch**)

**Request textDocument/documentSymbol failed\.**

*The TypeScript language server intermittently fails textDocument/documentSymbol requests with “no project found for URI” errors when saving files in a monorepo.*

 * created by **rubnogueira**
 * **rubnogueira** added label `Crash`
 * **andrewbranch** assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/issues/1967#issuecomment-3725018741) **tmcdo1** reported encountering the same RequestedLanguageService (project not loaded) error in a monorepo with TS Native Preview extension and provided logs and configuration details
 * [today](https://github.com/microsoft/TypeScript-go/issues/1967#issuecomment-3726528187) **andrewbranch** said "I think I probably fixed this in #2456, but without a repro, there’s no way of knowing."
 * [later](https://github.com/microsoft/TypeScript-go/issues/1967#issuecomment-3728472084) **rubnogueira** said "Thank you! This was still happening frequently in our codebase, but I just updated to 0.20260109.1 and I will report back if the fix is working."

### [Issue microsoft/TypeScript-go#2233](https://github.com/microsoft/TypeScript-go/issues/2233) (Closed, `Domain: Declaration Emit`, **weswigham**)

**Project references indirect dependencies: Error 2742 Inferred type of xxx \.\.\.**

*tsgo reports a TS2742 error when a package infers a type from an indirect project reference without directly referencing the originating package*

 * [1 month ago](https://github.com/microsoft/TypeScript-go/issues/2233#issuecomment-3633988288) **dimitraz** said "Likewise"
 * [1 month ago](https://github.com/microsoft/TypeScript-go/issues/2233#issuecomment-3634836621) **sanny-io** said "@dimitraz @samdcoding please use the thumbs up instead. It is more considerate of subscribers watching issues."
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2233#issuecomment-3649895000) **jordan-cutler** disabled project references by setting composite to false, shared related research links, and asked if the issue was specific to ts-go
 * [today](https://github.com/microsoft/TypeScript-go/issues/2233#issuecomment-3725740998) **marvinroger** clarified that the errors occur with npm as well as pnpm, Yarn, and Bun and noted that the issue persists in version 7.0.0-dev.20260108.1

### [PR microsoft/TypeScript-go#2330](https://github.com/microsoft/TypeScript-go/pull/2330) (Closed, **RyanCavanaugh**, **Copilot**)

**Port TypeScript PR \#62844: Gate \`\#/\` subpath imports on NodeNext and Bundler**

*Enable '#/' subpath imports for NodeNext and Bundler modes while preserving Node16 compatibility via a new feature flag.*

 * [1 month ago](https://github.com/microsoft/TypeScript-go/pull/2330#issuecomment-3639698114) **magic-akari** asked whether combining the error cases into a single test would be better
 * [1 month ago](https://github.com/microsoft/TypeScript-go/pull/2330#issuecomment-3639731399) **jakebailey** said "Yeah, it makes separate baselines, so is a pretty good solution to this."
 * (1 month ago) **jakebailey** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/2330#issuecomment-3725219820) **Yusuf007R** asked if it was already released and reported issues with Node.js subpaths in the TypeScript (Native Preview) VSCode extension, noting that disabling it and using the built-in TypeScript worked
 * [today](https://github.com/microsoft/TypeScript-go/pull/2330#issuecomment-3725920290) **andrewbranch** said "Yes, can you provide a specific repro?"

### [Issue microsoft/TypeScript-go#2351](https://github.com/microsoft/TypeScript-go/issues/2351) (Open, `bug`, `Domain: Emit`, **weswigham**)

**Implement es2017\-\>es2016 transform \(async/await\)**

*Add support for ES2016 targets by transforming async functions and await expressions via the newAsyncTransformer.*

 * created by **DanielRosenwasser**
 * **jakebailey** added label `Domain: Emit`
 * (today) **DanielRosenwasser** added label `bug`, and assigned to **weswigham**

### [Issue microsoft/TypeScript-go#2352](https://github.com/microsoft/TypeScript-go/issues/2352) (Open, `bug`, `Domain: Emit`, **weswigham**)

**Implement es2018\-\>es2017 transform \(for await & object rest/spread\)**

*Add transformation for async iteration (for-await-of) to enable targeting ES2017*

 * created by **DanielRosenwasser**
 * **jakebailey** added label `Domain: Emit`
 * (today) **DanielRosenwasser** added label `bug`, and assigned to **weswigham**

### [Issue microsoft/TypeScript-go#2428](https://github.com/microsoft/TypeScript-go/issues/2428) (Open, `Crash`)

**\[Panic Report\] cache entry not found \[recovered, repanicked\] \(version: 7\.0\.0\-dev\.20251227\.1\)**

*TypeScript-Go language server panics with a “cache entry not found” error during snapshot cloning.*

 * **renatoaraujoc** added label `Crash`
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/2428#issuecomment-3694592033) **lukeapage** noted a duplicate or related discussion and provided a link
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/2428#issuecomment-3694948339) **renatoaraujoc** mentioned that the issue caused the IntelliJ LSP to crash and require restarts, and that switching files prevented the code analyzer from firing unless the LSP was restarted; he believed it was an IntelliJ issue unrelated to typescript-go
 * [today](https://github.com/microsoft/TypeScript-go/issues/2428#issuecomment-3726043330) **andrewbranch** said "We’ve never gotten a repro for this panic; if you have one, we really need it 🙏 "

### [Issue microsoft/TypeScript-go#2430](https://github.com/microsoft/TypeScript-go/issues/2430) (Closed, `Domain: Editor`)

**C\# language server stopped working after switching to \.ts file with tsgo enabled**

*Enabling tsgo in a VS Code ASP.NET MVC project breaks C# language server’s go-to-definition and reference features.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/2430#issuecomment-3697359931) **DanielRosenwasser** said "Can you elaborate a bit more on what isn't working? Are you using this from a Razor template or something?"
 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/2430#issuecomment-3706927676) **bjoerni79** apologized for the delay and stated intent to retest with the new version later
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/2430#issuecomment-3707971986) **bjoerni79** reported inability to reproduce the bug on version 0.20260104.1 and requested to close the issue
 * (today) **DanielRosenwasser** closed the issue

### [Issue microsoft/TypeScript-go#2450](https://github.com/microsoft/TypeScript-go/issues/2450) (Open, `bug`, **iisaduan**)

**Review ported code from formatter**

*The Go port of the TypeScript formatter omitted retrieving the preceding token's parent before falling back to previousParent.*

 * created by **DanielRosenwasser**
 * **DanielRosenwasser** assigned to **weswigham**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2450#issuecomment-3725912447) **weswigham** said "Fixed by #2370 - https://github.com/microsoft/typescript-go/pull/2370/files#diff-57e4e12e0839091e4dde6c1f5e10e1438c3d3cd4f4eabdd7ea07530f0aac185dR306"
 * **weswigham** unassigned **weswigham**

### [Issue microsoft/TypeScript-go#2454](https://github.com/microsoft/TypeScript-go/issues/2454) (Closed, **ahejlsberg**)

**\`tsgo\` slow \- too much type and type instantiation without \`\-\-singleThreaded\` options**

*Excessive type instantiation in tsgo results in much slower builds than tsc unless using --singleThreaded.*

 * created by **noelkim-prestolabs**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2454#issuecomment-3724946894) **ahejlsberg** said "Any chance you can share a repro with us? It's practically impossible to diagnose the situation without one."
 * **ahejlsberg** added label `Needs More Info`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2454#issuecomment-3725271955) **DanielRosenwasser** said "Just as a heads up, you can (currently) use --checkers 1 instead of --singleThreaded to get parallel parse/emit, but single-threaded checking."
 * [today](https://github.com/microsoft/TypeScript-go/issues/2454#issuecomment-3725501658) **jakebailey** suggested using tsc with --generateTrace or typeslayer to locate the giant union and offered to send a PR for the growslice fix
 * [today](https://github.com/microsoft/TypeScript-go/issues/2454#issuecomment-3725779662) **ahejlsberg** summarized that a file with very expensive union types was referenced by many files and reconstructed multiple times across concurrent checkers and suggested avoiding the expensive union types as the best remedy
 * [today](https://github.com/microsoft/TypeScript-go/issues/2454#issuecomment-3726576005) **noelkim-prestolabs** reported profiling results for --checkers 1 with metrics and attachments, described expensive union types issue, and offered to provide a repro if issue #2458 cannot resolve it
 * [today](https://github.com/microsoft/TypeScript-go/issues/2454#issuecomment-3726599817) **jakebailey** advised that the linked PR would only partially improve the issue and cautioned about uploading private project files
 * [today](https://github.com/microsoft/TypeScript-go/issues/2454#issuecomment-3726604290) **noelkim-prestolabs** said "I understand, I'll prepare the repro If i can"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2454#issuecomment-3726653619) **noelkim-prestolabs** prepared repro and shared repository link

### [Issue microsoft/TypeScript-go#2455](https://github.com/microsoft/TypeScript-go/issues/2455) (Open, `Needs More Info`)

**TSGO not reporting TS2548**

*TSGO reports TS6133 but omits the TS2548 error when spreading a value typed as unknown[]|null.*

 * created by **Titozzz**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2455#issuecomment-3724992238) **ahejlsberg** reported inability to reproduce the behavior and provided error output from tsgo and tsc
 * **ahejlsberg** added label `Needs More Info`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2455#issuecomment-3725009336) **ahejlsberg** showed error output from tsgo and tsc with noUnusedLocals enabled, reporting errors TS6133 and TS2488 for spreading a null value
 * [later](https://github.com/microsoft/TypeScript-go/issues/2455#issuecomment-3729341477) **Titozzz** said "I'll try to either narrow it down to a small reproduction, or, find what causes my issue and will be back to you. "

### [PR microsoft/TypeScript-go#2456](https://github.com/microsoft/TypeScript-go/pull/2456) (Closed)

**Fix LS bugs triggered by file moving \(and probably other scenarios\)**

*Fixes language service bugs triggered by VS Code file moves and faulty project lookup logic following configuration updates.*

 * created by **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2456#issuecomment-3725944507) **andrewbranch** said "Confirmed this fixes my comment https://github.com/microsoft/typescript-go/issues/1983#issuecomment-3550064071 🎉 "
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#2457](https://github.com/microsoft/TypeScript-go/issues/2457) (Open)

**Proposal: Prettified type display in hover output**

*Add optional settings to display prettified, expanded types in hover output for better readability.*

 * created by **sQVe**

### [PR microsoft/TypeScript-go#2458](https://github.com/microsoft/TypeScript-go/pull/2458) (Closed)

**Preallocate types slice in getLiteralTypeFromProperties**

*Preallocate the types slice in getLiteralTypeFromProperties to reduce allocations and improve performance.*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#2459](https://github.com/microsoft/TypeScript-go/pull/2459) (Open)

**Port \-\-isolatedDeclarations related node builder logic, with baseline updates**

*Port node builder logic for the --isolatedDeclarations option and apply baseline updates for review.*

 * created by **weswigham**

### [Issue microsoft/TypeScript-go#2460](https://github.com/microsoft/TypeScript-go/issues/2460) (Open, `Crash`)

**textDocument/inlayHint: Cannot create token from reparsed node of kind KindFunctionExpression**

*textDocument/inlayHint request panics due to inability to create a token from a reparsed function expression node*

 * created by **rubnogueira**
 * **rubnogueira** added label `Crash`

