# Report for 2026-01-22 (Thursday, January 22nd, 2026)

13 different users commented on 35 different issues.

## Recommended Actions

 * Response Recommended
    * @rubnogueira provided repro steps as requested in [microsoft/TypeScript-go#2460](https://github.com/microsoft/TypeScript-go/issues/2460#issuecomment-3789803553)
    * @Titozzz reported increased RAM usage up to 40 GB and rollbacks in [microsoft/TypeScript-go#2561](https://github.com/microsoft/TypeScript-go/issues/2561#issuecomment-3789506705)
    * @kratos-respawned reported 92GB memory usage for the language server in [microsoft/TypeScript-go#2561](https://github.com/microsoft/TypeScript-go/issues/2561#issuecomment-3790085897)
    * @rubnogueira provided a link to the issue and noted the fix isn't in the latest release in [microsoft/TypeScript-go#2573](https://github.com/microsoft/TypeScript-go/issues/2573#issuecomment-3790702573)

## Activity Summary

### [Issue microsoft/TypeScript-go#1691](https://github.com/microsoft/TypeScript-go/issues/1691) (Closed, `Crash`, **andrewbranch**)

**\[lsp\] panic with slice bounds out of range \[:\-1\] when typing anything in a source file**

*LSP server panics with a slice bounds out of range [-1] error during completions when typing in source files.*

 * **RyanCavanaugh** assigned to **sheetalkamat**
 * (9 weeks ago) **ahejlsberg** assigned to **andrewbranch**, and unassigned **sheetalkamat**
 * [today](https://github.com/microsoft/TypeScript-go/issues/1691#issuecomment-3786079191) **andrewbranch** said "All the code in this stack got deleted in #2390 "
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#1756](https://github.com/microsoft/TypeScript-go/pull/1756) (Closed)

**lsp: prevent out\-of\-range panic in autoimports/completions when symbol name or position is invalid \(fixes \#1691\)**

*Add bounds checks and safe defaults to LSP completions and auto-imports to prevent panics on invalid positions or symbol names.*

 * created by **arash-mosavi**
 * [16 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1756#issuecomment-3341456340) **arash-mosavi** said "@microsoft-github-policy-service agree"
 * [15 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1756#issuecomment-3385382094) **jakebailey** said "These fixes could be plausible, but need fourslash tests to verify."
 * [today](https://github.com/microsoft/TypeScript-go/pull/1756#issuecomment-3786080917) **andrewbranch** said "Superseded by #2390 "
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#1943](https://github.com/microsoft/TypeScript-go/issues/1943) (Closed, `Needs More Info`, **andrewbranch**)

**\`export \* from …\` sometimes behaves differently in \`tsgo\` than in \`tsc\` or \`tsgo\` LSP**

*tsgo in a private monorepo fails to resolve types re-exported with export * from, whereas tsc and the LSP succeed.*

 * [9 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1943#issuecomment-3544647059) **jakebailey** said "@chriskrycho have you been able to come up with a repro?"
 * **jakebailey** added label `Needs More Info`
 * [9 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1943#issuecomment-3558080586) **chriskrycho** confirmed that the repro worked as expected, reported being stumped, and said they would check on a more recent nightly and follow up
 * [today](https://github.com/microsoft/TypeScript-go/issues/1943#issuecomment-3786075256) **andrewbranch** said "@chriskrycho do you ever see this anymore?"

### [Issue microsoft/TypeScript-go#1967](https://github.com/microsoft/TypeScript-go/issues/1967) (Closed, `Crash`, **andrewbranch**)

**Request textDocument/documentSymbol failed\.**

*The TypeScript language server intermittently fails textDocument/documentSymbol requests with “no project found for URI” errors when saving files in a monorepo.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1967#issuecomment-3726528187) **andrewbranch** said "I think I probably fixed this in #2456, but without a repro, there’s no way of knowing."
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/1967#issuecomment-3728472084) **rubnogueira** said "Thank you! This was still happening frequently in our codebase, but I just updated to 0.20260109.1 and I will report back if the fix is working."
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/1967#issuecomment-3748520962) **PaulRBerg** reported that the issue persisted with version 7.0.0-dev.20260113.1 when AI agents modified many files and that they could not provide a repro
 * [today](https://github.com/microsoft/TypeScript-go/issues/1967#issuecomment-3786064148) **andrewbranch** said "Meant to close this in #2549 "
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#2022](https://github.com/microsoft/TypeScript-go/issues/2022) (Closed, `Crash`, **andrewbranch**)

**panic handling completionItem/resolve**

*The TypeScript-Go language server panics and crashes while handling a completionItem/resolve request due to an error in its completion resolution logic.*

 * created by **pedro757**
 * **pedro757** added label `Crash`
 * **andrewbranch** assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2022#issuecomment-3786073639) **andrewbranch** said "Meant to close this in #2390 "
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#2106](https://github.com/microsoft/TypeScript-go/issues/2106) (Closed, `Crash`, **ahejlsberg**)

**Panic when retrieving namespace information in \`textDocument/definition\`**

*Aggregating namespace imports from the main effect package causes a nil pointer dereference panic during textDocument/definition handling.*

 * created by **richardvanbergen**
 * **richardvanbergen** added label `Crash`
 * **RyanCavanaugh** assigned to **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2106#issuecomment-3787095479) **ahejlsberg** said "No longer reproduces, I'm assuming the issue was fixed. Closing."
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#2131](https://github.com/microsoft/TypeScript-go/issues/2131) (Closed, `Crash`, **ahejlsberg**)

**panic handling request textDocument/inlayHint: runtime error: slice bounds out of range**

*TypeScript-Go LSP server panics with slice bounds out of range error during inlay hint handling when switching tabs.*

 * **rubnogueira** added label `Crash`
 * [9 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2131#issuecomment-3556521103) **lukpsaxo** said "Related to #2077  ?"
 * **RyanCavanaugh** assigned to **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2131#issuecomment-3787076980) **ahejlsberg** said "I'm going to close this as a duplicate of #2077."
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#2238](https://github.com/microsoft/TypeScript-go/issues/2238) (Open, `Crash`, **ahejlsberg**)

**fatal error: concurrent map read and map write**

*A fatal concurrent map read/write panic occurs in the Typescript-Go link store while resolving import aliases.*

 * **charlag** added label `Crash`
 * [6 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2238#issuecomment-3617676644) **jakebailey** said "It seems like we are still somehow concurrency unsafe through HandleNoEmitOnError. Incremental is still not doing the expected locking."
 * **RyanCavanaugh** assigned to **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2238#issuecomment-3787068104) **ahejlsberg** said "@charlag No longer seems to reproduce, issue was likely fixed. Can you confirm that this is no longer an issue?"

### [Issue microsoft/TypeScript-go#2383](https://github.com/microsoft/TypeScript-go/issues/2383) (Closed, `Domain: Editor`, **gabritto**)

**LSP: Path suggestion missing \(import/export\)**

*Path completion suggestions for import/export statements are missing in tsgo, unlike in TypeScript 5.9.*

 * **andrewbranch** assigned to **gabritto**
 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2383#issuecomment-3657264640) **besserwisser** asked if there was a list of to-dos
 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2383#issuecomment-3657318588) **andrewbranch** said "Yes and no; we have a list of failing/differing tests, and I traced these to a function that was empty except for a code comment."
 * **andrewbranch** unassigned **andrewbranch**

### [Issue microsoft/TypeScript-go#2418](https://github.com/microsoft/TypeScript-go/issues/2418) (Closed)

**\[BUG\] tsgo list more files than tsc**

*tsgo’s --listFilesOnly output includes extra files compared to tsc, breaking basic tsgo --noEmit CI checks.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/2418#issuecomment-3756717309) **jakebailey** said "I unfortunately don't know how to work on this without a repro I can test and debug myself ☹️ "
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/2418#issuecomment-3757238865) **HananoshikaYomaru** provided repository link and reproduction steps
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2418#issuecomment-3781314395) **jakebailey** said "Looking at the state on main, I actually think this was #2361. Can you retry with a newer build and see if they behave similarly?"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2434](https://github.com/microsoft/TypeScript-go/pull/2434) (Open)

**Experiment: Quantified Types**

*Seeking a TypeScript function signature to consume an array of heterogeneous Layer objects without collapsing distinct generics.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2434#issuecomment-3705776547) **devanshj** noted that reverse mapped types simplified the example, provided a motivating code snippet, and said they would further refine the PR
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2434#issuecomment-3705823991) **Andarist** suggested using reverse mapped types from two TypeScript PRs and provided a playground example
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2434#issuecomment-3705842553) **devanshj** said "Yeah I think in theory you could pull it off with reverse mapped types and with some enhancements in the checker but then quantified types are nicer to read/understand... so I'm a bit biased haha"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2434#issuecomment-3787582505) **Diggsey** expressed desire for quantified types and argued that reverse mapped types leak complexity compared to quantified types, noting that function types already support quantification

### [Issue microsoft/TypeScript-go#2455](https://github.com/microsoft/TypeScript-go/issues/2455) (Open, `Needs More Info`)

**TSGO not reporting TS2548**

*TSGO reports TS6133 but omits the TS2548 error when spreading a value typed as unknown[]|null.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2455#issuecomment-3725009336) **ahejlsberg** showed error output from tsgo and tsc with noUnusedLocals enabled, reporting errors TS6133 and TS2488 for spreading a null value
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/2455#issuecomment-3729341477) **Titozzz** said "I'll try to either narrow it down to a small reproduction, or, find what causes my issue and will be back to you. "
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/2455#issuecomment-3738468999) **Titozzz** noted that omitting or setting a deprecated ‘target’ to “es5” reproduced the issue and asked about an incremental caching annoyance and whether to open a new issue
 * [today](https://github.com/microsoft/TypeScript-go/issues/2455#issuecomment-3786769504) **ahejlsberg** asked for the tsconfig.json file and clarified if part of the repro was missing

### [Issue microsoft/TypeScript-go#2460](https://github.com/microsoft/TypeScript-go/issues/2460) (Closed, `Crash`, **ahejlsberg**)

**textDocument/inlayHint: Cannot create token from reparsed node of kind KindFunctionExpression**

*textDocument/inlayHint request panics due to inability to create a token from a reparsed function expression node*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/2460#issuecomment-3730026130) **a-tarasyuk** provided a minimal repro code example
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/2460#issuecomment-3730068931) **rubnogueira** asked whether the provided repro was sufficient or if they should create one, and reported an inlayHint error when opening js files with logs
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/2460#issuecomment-3743948547) **rubnogueira** reported a crash when opening Gruntfile.js at the require line
 * [later](https://github.com/microsoft/TypeScript-go/issues/2460#issuecomment-3789803553) **rubnogueira** provided a minimal repro link and described how to trigger the alert by opening Gruntfile.js

### [Issue microsoft/TypeScript-go#2506](https://github.com/microsoft/TypeScript-go/issues/2506) (Open, `Domain: Editor`, **andrewbranch**)

**Stale module resolution error after linking pnpm workspace dependency due to watcher configuration/handling**

*VS Code’s watcher ignoring directory-level symlink events outside its file-extension glob causes stale module resolution errors after pnpm workspace linking.*

 * (1 week ago) **andrewbranch** added label `Domain: Editor`, and assigned to **andrewbranch**
 * (yesterday) **andrewbranch** closed the issue
 * (today) **andrewbranch** reopened the issue

### [PR microsoft/TypeScript-go#2514](https://github.com/microsoft/TypeScript-go/pull/2514) (Closed)

**fix: allow references to unexported types**

*Fix declaration emit errors when indirectly referencing unexported types by reusing existing type nodes*

 * created by **raimannma**
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/2514#issuecomment-3754619979) **raimannma** agreed to the contributor license agreement by replying '@microsoft-github-policy-service agree'
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/2514#issuecomment-3756733257) **jakebailey** said "I would think this conflicts with #1693 / #2459"
 * (later) **raimannma** closed the issue

### [Issue microsoft/TypeScript-go#2550](https://github.com/microsoft/TypeScript-go/issues/2550) (Closed, `Crash`, **andrewbranch**)

**Crash for auto\-imports from untitled file to saved tsx file**

*Auto-import completions from an untitled JavaScript buffer to a saved TSX file cause a nil pointer dereference crash.*

 * created by **DanielRosenwasser**
 * (2 days ago) **DanielRosenwasser** added label `Crash`, and assigned to **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#2551](https://github.com/microsoft/TypeScript-go/issues/2551) (Closed, `Domain: Performance`, **ahejlsberg**)

**2x slower than tsc on a NestJS codebase**

*tsgo type checking on a NestJS application is twice as slow as tsc due to excessive memory allocations in getSiblingsOfContext.*

 * **RyanCavanaugh** unassigned **Copilot**
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/2551#issuecomment-3776476318) **RyanCavanaugh** presented a reproduction case showing compilation timings of 11.2s in tsgo and 5.3s in tsc
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/2551#issuecomment-3776631389) **FelixMalfait** said "Wow thanks for jumping on that so quickly!"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2551#issuecomment-3785369517) **jakebailey** compared performance metrics before and after applying #2567 and against tsc
 * (today) **ahejlsberg** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/issues/2551#issuecomment-3786348028) **prastoin** expressed enthusiasm for TypeScript and appreciation for the quick fix

### [Issue microsoft/TypeScript-go#2555](https://github.com/microsoft/TypeScript-go/issues/2555) (Open, `Domain: Editor`)

**Installing Native Preview broke TS Imports**

*Installing VS Code’s Native Preview TypeScript extension on macOS breaks TypeScript auto-import suggestions despite reverting settings and reinstalling the editor.*

 * **tikki100** added label `Domain: Editor`
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2555#issuecomment-3778473834) **rubnogueira** suggested including the "node" types in tsconfig.json and referenced a TypeScript issue for defaults
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2555#issuecomment-3779894761) **tikki100** reported that the suggestion did not resolve the issue and provided detailed reproduction steps
 * [later](https://github.com/microsoft/TypeScript-go/issues/2555#issuecomment-3789626673) **rubnogueira** explained that with TypeScript 6.0 the tsconfig.json “types” array defaults to empty and requires explicitly listing relevant React types

### [PR microsoft/TypeScript-go#2556](https://github.com/microsoft/TypeScript-go/pull/2556) (Closed)

**\[Experiment\] avoid OrderedMap in widening context properties**

*Experiment to avoid using OrderedMap for widening context properties by exploring alternative data structures*

 * created by **a-tarasyuk**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2556#issuecomment-3780643034) **DanielRosenwasser** said "I'm guessing you also tried NewOrderedMapWithSizeHint and there's too much indirection for that to be compiled away."
 * (today) **a-tarasyuk** closed the issue

### [Issue microsoft/TypeScript-go#2557](https://github.com/microsoft/TypeScript-go/issues/2557) (Closed, `Domain: Editor`)

**Suggestions freeze and stop working until I close and open the file again**

*TypeScript suggestions and IntelliSense features freeze in a specific file until it’s closed and reopened*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2557#issuecomment-3782009190) **andrewbranch** described stale errors persisting across language server restarts and causing crashes when requesting code fixes
 * [today](https://github.com/microsoft/TypeScript-go/issues/2557#issuecomment-3783442883) **rubnogueira** expressed happiness that the issue was reproduced, noted it occurred in both VSCode and Cursor, offered additional context, and affirmed that Corsa's pros outweigh the inconvenience
 * [today](https://github.com/microsoft/TypeScript-go/issues/2557#issuecomment-3783645878) **lukpsaxo** reported that TypeScript stopped updating on file edits over the last two days, requiring file reopen or plugin restart, and shared logs illustrating the issue
 * **andrewbranch** removed label `Needs More Info`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2557#issuecomment-3785934101) **andrewbranch** said "Not a VS Code bug after all, false alarm 😅 "
 * (today) **andrewbranch** closed the issue
 * [later](https://github.com/microsoft/TypeScript-go/issues/2557#issuecomment-3789569396) **rubnogueira** confirmed that the fix works and expressed gratitude

### [Issue microsoft/TypeScript-go#2559](https://github.com/microsoft/TypeScript-go/issues/2559) (Open, `Crash`, **andrewbranch**, **Copilot**)

**Quick fix crash when promoting type\-only import to value and existing type import precedes new value import**

*Converting a type-only import to a value import via quick fix panics the TypeScript language server.*

 * created by **DanielRosenwasser**
 * (yesterday) **DanielRosenwasser** added label `Crash`, and assigned to **jakebailey**
 * (today) **DanielRosenwasser** assigned to **andrewbranch**, and unassigned **jakebailey**
 * **andrewbranch** assigned to **Copilot**

### [Issue microsoft/TypeScript-go#2561](https://github.com/microsoft/TypeScript-go/issues/2561) (Open, `Crash`)

**v0\.20260119\.1 crashes ts server for large project, v0\.20260116\.1 works**

*TypeScript Native Preview v0.20260119.1 crashes the TS server on large, high-memory projects, whereas v0.20260116.1 works.*

 * created by **austinfennacy**
 * **austinfennacy** added label `Crash`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2561#issuecomment-3787010907) **DanielRosenwasser** suggested that a regression might stem from PR 2499, that PR 2568 could have fixed it, and asked to try version 0.20260122.4
 * [later](https://github.com/microsoft/TypeScript-go/issues/2561#issuecomment-3789506705) **Titozzz** said "Just FYI we also noticed that since 3-4 days, and team members have either rolled back to a previous version or disabled tsgo. Someone noticed RAM usage up to 40 Go from the server!"
 * [later](https://github.com/microsoft/TypeScript-go/issues/2561#issuecomment-3790085897) **kratos-respawned** reported that the language server memory usage reached 92GB

### [PR microsoft/TypeScript-go#2562](https://github.com/microsoft/TypeScript-go/pull/2562) (Closed)

**Fix porting bug in resolveAutomaticTypeDirectives**

*Fix resolveAutomaticTypeDirectives mapping undefined to ResolutionModeNone to align with TypeScript and prevent duplicate type directives*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2562#issuecomment-3786224432) **jakebailey** said "I'm not sure. The relationship between ResolutionMode and ModuleKind means we are seemingly potentially missing some cases, so I can't even replicate this problem in Strada..."
 * (today) **jakebailey** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/2562#issuecomment-3786344394) **jakebailey** demonstrated two failing unit tests when forcing Strada with casts and noted missing tests for reuseProgramStructure

### [PR microsoft/TypeScript-go#2563](https://github.com/microsoft/TypeScript-go/pull/2563) (Closed)

**Don't request auto imports in untitled files**

*Prevent automatic import requests from being sent in untitled files.*

 * created by **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2563#issuecomment-3785306933) **andrewbranch** said "I’m pretty sure they mostly don’t work, but we don’t bail out early like this. We probably compute them and then filter them out because they have absolute paths."
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#2564](https://github.com/microsoft/TypeScript-go/pull/2564) (Closed)

**Always bundle extension**

*Bundle the extension’s dependencies to fix null extension errors and incorporate problem matchers without extra installs.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2566](https://github.com/microsoft/TypeScript-go/issues/2566) (Closed, `Domain: Editor`)

**suggestor does not suggest the module name when typing it**

*The tsgo extension does not auto-suggest local module file names when typing import paths like tsserver does.*

 * created by **Redaloukil**
 * **Redaloukil** added label `Domain: Editor`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2566#issuecomment-3785289598) **rubenferreira97** identified the issue as a duplicate of #2383, noted the delayed migration to tsgo due to the missing feature, and predicted further issues
 * [today](https://github.com/microsoft/TypeScript-go/issues/2566#issuecomment-3785981444) **andrewbranch** said "Yep, this is a duplicate and the features is currently in progress."
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#2567](https://github.com/microsoft/TypeScript-go/pull/2567) (Closed)

**Cache widening contexts for nested object literals**

*Cache widening contexts for nested object literal spreads to reduce type-checking time from 17 seconds to under 0.1 seconds.*

 * created by **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2567#issuecomment-3785366096) **jakebailey** compared performance metrics before and after changes in the twenty-server package and against tsc
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#2568](https://github.com/microsoft/TypeScript-go/pull/2568) (Closed)

**Don’t use request context for sending responses**

*Checking the request context for cancellation when sending responses causes undelivered error messages and hung clients.*

 * created by **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#2569](https://github.com/microsoft/TypeScript-go/pull/2569) (Open, **andrewbranch**, **Copilot**)

**Fix getVisualListRange bug in formatting \(partial fix for import promotion crash\)**

*Use GetStartOfNode instead of Pos in getVisualListRange to skip trivia and prevent import promotion formatting crashes.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2569#issuecomment-3786251778) **andrewbranch** said "Love to see a debug assertion ignored with a comment that says “yeah yeah but in rare cases the invariants we asserted simply don’t hold” 🙄 "
 * [today](https://github.com/microsoft/TypeScript-go/pull/2569#issuecomment-3786268497) **andrewbranch** said "@copilot where is your test? You're not allowed to make a fix without proving that you reproduced the crash in a test first."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2569#issuecomment-3786317916) **Copilot** added a test reproducing the crash with verbatimModuleSyntax; acknowledged the fix was inadequate; analyzed the root cause involving tracker deletion/insertion handling; proposed implementing a proper move operation and reverting the current fix
 * [today](https://github.com/microsoft/TypeScript-go/pull/2569#issuecomment-3786355488) **andrewbranch** said "@copilot keep the test but revert the attempted fix"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2569#issuecomment-3786377009) **Copilot** reverted the attempted fixes to internal/ls/autoimport/fix.go and internal/ls/change/delete.go and preserved the test TestCodeFixPromoteTypeOnlyOrderingCrash
 * [today](https://github.com/microsoft/TypeScript-go/pull/2569#issuecomment-3786474230) **andrewbranch** traced the issue to getVisualListRange in indent.go, compared Corsa and Strada outputs, pointed to Strada implementation, and suggested using print debugging or writing a unit test
 * [today](https://github.com/microsoft/TypeScript-go/pull/2569#issuecomment-3786614767) **Copilot** traced the problem to getVisualListRange in indent.go, updated it to use astnav.GetStartOfNode instead of next.Pos() to correct the range calculation, and added comprehensive tests
 * [today](https://github.com/microsoft/TypeScript-go/pull/2569#issuecomment-3786716239) **andrewbranch** said "@copilot seems like tests are still failing"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2569#issuecomment-3786881437) **Copilot** fixed tests failing by addressing two bugs in getVisualListRange and import reordering logic
 * [today](https://github.com/microsoft/TypeScript-go/pull/2569#issuecomment-3786979320) **Copilot** reverted to a simple fix in commit a1301d95 and removed complex autoimport and investigation changes

### [PR microsoft/TypeScript-go#2570](https://github.com/microsoft/TypeScript-go/pull/2570) (Closed, **RyanCavanaugh**, **Copilot**)

**Fix \-\-showConfig to print enum names instead of integers**

*Modify --showConfig to output enum option names rather than numeric values by adding custom JSON marshaling methods*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2570#issuecomment-3786444909) **jakebailey** suggested using go-json-experiment’s type override system instead of adding MarshalJSON methods for showConfig because the current approach yields suboptimal tsbuildinfo
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#2571](https://github.com/microsoft/TypeScript-go/pull/2571) (Closed, **RyanCavanaugh**, **Copilot**)

**Fix \-\-showConfig to print enumerated value names, not integers**

*Update --showConfig to serialize compiler and watch option enums as their string names instead of numeric codes.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2571#issuecomment-3786845813) **jakebailey** asked if this was the same as #2570 and noted missing tests for --showConfig
 * [today](https://github.com/microsoft/TypeScript-go/pull/2571#issuecomment-3786881330) **jakebailey** criticized the approach as hopeless and suggested porting the old code using compiler options declarations instead of JSON packages

### [Issue microsoft/TypeScript-go#2572](https://github.com/microsoft/TypeScript-go/issues/2572) (Closed, `Crash`, `Needs More Info`, **andrewbranch**)

**no project found for URI: textDocument/foldingRange and textDocument/diagnostic**

*Language server folding range and diagnostic requests fail for vitest.config.ts because it’s not included in any TypeScript project*

 * created by **rubnogueira**
 * **rubnogueira** added label `Crash`

### [Issue microsoft/TypeScript-go#2573](https://github.com/microsoft/TypeScript-go/issues/2573) (Open, `Domain: Editor`, `Needs More Info`, **andrewbranch**)

**Seems like language server can't keep up with changes made in editor**

*The language server can't keep pace with editor changes, reporting outdated errors until it's restarted.*

 * created by **ilbrando**
 * **ilbrando** added label `Domain: Editor`
 * [later](https://github.com/microsoft/TypeScript-go/issues/2573#issuecomment-3790702573) **rubnogueira** noted that the issue was already solved in a previous issue but not in the latest release

### [Issue microsoft/TypeScript-go#2574](https://github.com/microsoft/TypeScript-go/issues/2574) (Open, `Crash`)

**panic: cache entry not found \[recovered, repanicked\]**

*A panic occurs in typescript-go v7.0.0-dev when cloning project snapshots due to a missing cache entry.*

 * created by **joepjoosten**
 * **joepjoosten** added label `Crash`

