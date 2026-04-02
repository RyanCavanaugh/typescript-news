# Report for 2026-01-21 (Wednesday, January 21st, 2026)

18 different users commented on 31 different issues.

## Recommended Actions

 * Response Recommended
    * @OliverJAsh reported that the issue still occurs in the latest nightly and pinpointed the commit where it last did not occur in [microsoft/TypeScript-go#2239](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3780405999)
    * @rubnogueira provided confirmation that the latest code fixes the memory issue in [microsoft/TypeScript-go#2239](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3780538678)
    * @Moltenship provided repro steps and heap profiles as requested in [microsoft/TypeScript-go#2239](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3782854830)
    * @rubenferreira97 asked whether the issue was wrongly closed in [microsoft/TypeScript-go#2369](https://github.com/microsoft/TypeScript-go/issues/2369#issuecomment-3784608098)
    * @tikki100 provided reproduction steps and reported the issue persisted in [microsoft/TypeScript-go#2555](https://github.com/microsoft/TypeScript-go/issues/2555#issuecomment-3779894761)
    * @rubnogueira emailed logs and asked if they missed anything relevant in [microsoft/TypeScript-go#2557](https://github.com/microsoft/TypeScript-go/issues/2557#issuecomment-3780511722)
    * @rubnogueira provided repro steps and a reproduction repository link in [microsoft/TypeScript-go#2557](https://github.com/microsoft/TypeScript-go/issues/2557#issuecomment-3781529261)
    * @rubnogueira offered additional context and asked if more information is needed in [microsoft/TypeScript-go#2557](https://github.com/microsoft/TypeScript-go/issues/2557#issuecomment-3783442883)
    * @lukpsaxo reported a TypeScript update issue and provided logs in [microsoft/TypeScript-go#2557](https://github.com/microsoft/TypeScript-go/issues/2557#issuecomment-3783645878)

## Activity Summary

### [Issue microsoft/TypeScript-go#1983](https://github.com/microsoft/TypeScript-go/issues/1983) (Closed, `Domain: Editor`, `Crash`, **andrewbranch**)

**textDocument/diagnostic failed**

*textDocument/diagnostic requests repeatedly panic due to missing parse cache entries in the TypeScript Go project snapshot clone*

 * **jakebailey** added label `Crash`
 * [9 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1983#issuecomment-3550064071) **andrewbranch** reproduced a failure to find a project for a file and provided reproduction steps
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/1983#issuecomment-3774151638) **andrewbranch** said "Note that the panic stack traces here are unrelated to the UI error message. I’m going to treat this issue is tracking the “project not found” error message, not the panic."
 * [today](https://github.com/microsoft/TypeScript-go/issues/1983#issuecomment-3780804866) **andrewbranch** asked whether the same panic could still be reproduced, explained how the error message and stack frames would differ, and mentioned having a repro and fix for issue #2428
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#2239](https://github.com/microsoft/TypeScript-go/issues/2239) (Closed, `Needs More Info`)

**take too much memory**

*tsgo extension consumes about 17GB of RAM on macOS M1, causing heavy swapping and slowing VS Code.*

 * (yesterday) **andrewbranch** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3777897123) **MartinCura** said "awesome! how often is a new extension release cut? or can i install from a commit?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3778827946) **jakebailey** said "We release majorly, so it's already out."
 * [today](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3780405999) **OliverJAsh** reported that the issue still occurred in the latest nightly and did not reproduce before a specific commit
 * [today](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3780538678) **rubnogueira** confirmed that the latest code fixes the memory issue after compiling the .vsix from source and noted that the PR was merged on the 21st and the last release was on the 20th
 * [today](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3780559293) **jakebailey** expressed frustration about an outage during last night's release build and said he would rerun the release manually
 * [today](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3780562892) **andrewbranch** reminded that the issue did not reproduce before commit 38353bd4d704efd6d00ec277087bbca5a7d050ff and noted that the fix in #2553 corrected changes introduced in that commit
 * [today](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3780803103) **jakebailey** said "Unfortunately it's not an outage, but something different. I am looking into it :("
 * [today](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3782713289) **jakebailey** said "Okay, it's been resolved, so the latest version on npm and in VS Code should have the most recent fixes."
 * [today](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3782764903) **oorestisime** said "Big thanks people! "
 * [today](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3782854830) **Moltenship** reported similar memory consumption issue after the recent fix and provided environment details along with heap and allocation profile attachments

### [Issue microsoft/TypeScript-go#2299](https://github.com/microsoft/TypeScript-go/issues/2299) (Closed, `Crash`, **DanielRosenwasser**, **sheetalkamat**, **Copilot**)

**Crash on find\-all\-references on \`this\`**

*VS Code's find-all-references on the `this` keyword panics with a slice bounds out of range error.*

 * [6 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2299#issuecomment-3639548679) **DanielRosenwasser** said "Also happens on the this at https://github.com/microsoft/TypeScript/blob/366da34ae60b458e97c880fedf33298d6842ddd6/src/server/project.ts#L945"
 * (1 week ago) **DanielRosenwasser** assigned to **Copilot**, **DanielRosenwasser**
 * (today) **sheetalkamat** closed the issue

### [Issue microsoft/TypeScript-go#2369](https://github.com/microsoft/TypeScript-go/issues/2369) (Closed, `Domain: Editor`, **DanielRosenwasser**)

**Code Lens provider registration error after switching tsdk location**

*Switching TypeScript SDK paths triggers a duplicate code lens command registration error and launches two language server instances.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/2369#issuecomment-3731130662) **DanielRosenwasser** said "Sure, that one does and that's easy. I'm working on other stuff that the Client needs to manage though."
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/2369#issuecomment-3731135262) **jakebailey** said "All in all, I would personally say we should just require there only be one Client at a time, then use globals or something"
 * (1 week ago) **DanielRosenwasser** closed the issue
 * [later](https://github.com/microsoft/TypeScript-go/issues/2369#issuecomment-3784608098) **rubenferreira97** asked whether the issue was wrongly closed and reported that multiple TypeScript (Native Preview) options appeared when using the native-preview TSDK

### [Issue microsoft/TypeScript-go#2418](https://github.com/microsoft/TypeScript-go/issues/2418) (Closed)

**\[BUG\] tsgo list more files than tsc**

*tsgo’s --listFilesOnly output includes extra files compared to tsc, breaking basic tsgo --noEmit CI checks.*

 * [6 days ago](https://github.com/microsoft/TypeScript-go/issues/2418#issuecomment-3755484687) **HananoshikaYomaru** misunderstood the operation of "includes" and "excludes", intended to exclude TypeScript errors from specific files but could not figure out why tsgo and tsc behaved differently
 * [6 days ago](https://github.com/microsoft/TypeScript-go/issues/2418#issuecomment-3756717309) **jakebailey** said "I unfortunately don't know how to work on this without a repro I can test and debug myself ☹️ "
 * [6 days ago](https://github.com/microsoft/TypeScript-go/issues/2418#issuecomment-3757238865) **HananoshikaYomaru** provided repository link and reproduction steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/2418#issuecomment-3781314395) **jakebailey** said "Looking at the state on main, I actually think this was #2361. Can you retry with a newer build and see if they behave similarly?"

### [Issue microsoft/TypeScript-go#2428](https://github.com/microsoft/TypeScript-go/issues/2428) (Closed, `Crash`)

**\[Panic Report\] cache entry not found \[recovered, repanicked\] \(version: 7\.0\.0\-dev\.20251227\.1\)**

*TypeScript-Go language server panics with a “cache entry not found” error during snapshot cloning.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2428#issuecomment-3694592033) **lukeapage** noted a duplicate or related discussion and provided a link
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2428#issuecomment-3694948339) **renatoaraujoc** mentioned that the issue caused the IntelliJ LSP to crash and require restarts, and that switching files prevented the code analyzer from firing unless the LSP was restarted; he believed it was an IntelliJ issue unrelated to typescript-go
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/2428#issuecomment-3726043330) **andrewbranch** said "We’ve never gotten a repro for this panic; if you have one, we really need it 🙏 "
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#2462](https://github.com/microsoft/TypeScript-go/pull/2462) (Closed, **RyanCavanaugh**, **Copilot**)

**Port PR \#61376: Fix spurious "used before being assigned" errors in for of/in loops**

*Port TypeScript PR to fix misleading "used before being assigned" errors for variables in for-in and for-of loops.*

 * (1 week ago) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * [6 days ago](https://github.com/microsoft/TypeScript-go/pull/2462#issuecomment-3757028702) **Copilot** added the upstream PR test as a local test in testdata/tests/cases/compiler/unusedLocalsInForInOrOf1.ts with corresponding baselines
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#2483](https://github.com/microsoft/TypeScript-go/pull/2483) (Closed)

**Fix extended config ref counting**

*Fix the reference counting logic for extended tsconfig configurations and source file caching to ensure accurate resource cleanup.*

 * created by **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#2493](https://github.com/microsoft/TypeScript-go/pull/2493) (Closed, **DanielRosenwasser**, **Copilot**)

**Fix slice bounds panic in find\-all\-references for \`this\` across files**

*Add validation and fallback search to prevent slice bounds panics when finding 'this' references across multiple files.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/2493#issuecomment-3742468916) **Copilot** added a test case reproducing the panic when using a large-file container to search a small file, showing it panics without the fix and succeeds with it
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/2493#issuecomment-3742522497) **DanielRosenwasser** said "@copilot no, we prefer a "fourslash"-style test. Create a language service test with // @filename: ... etc."
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/2493#issuecomment-3742575608) **Copilot** replaced the test with a fourslash-style test in commit 5e5f67e and described its use of // @Filename directives to verify cross-file 'this' references
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2498](https://github.com/microsoft/TypeScript-go/pull/2498) (Open)

**Declaration \(d\.ts\) output diff breakdown as seen in \`effect\`**

*Comparison of tsc and tsgo declaration file outputs highlighting syntax and type alias differences in the Effect v4 codebase.*

 * created by **fubhy**
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/2498#issuecomment-3744922224) **jakebailey** said "You should test with #2459, this is still a WIP area"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2498#issuecomment-3781320725) **jakebailey** said "I am a little confused as to how these are high-priority issues; are these not all identical semantically?"
 * [later](https://github.com/microsoft/TypeScript-go/pull/2498#issuecomment-3783734964) **fubhy** clarified that most signature changes were semantically identical except one altering the return type and noted other adjustments were QoL/readability improvements

### [Issue microsoft/TypeScript-go#2503](https://github.com/microsoft/TypeScript-go/issues/2503) (Open)

**Autocomplete and auto\-import is slower in JSX context**

*JSX tag autocomplete and auto-import in TypeScript monorepos remains slow (~1s vs ~100ms) due to expensive contextual type computation.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/2503#issuecomment-3750663993) **jansedlon** noted that JSX autocomplete was usually slower (1s-2s) compared to outside (500ms-1.5s) in 80% of cases and offered to provide screen recordings
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/2503#issuecomment-3751004372) **jansedlon** shared four videos demonstrating tsserver, native TS branch, and their fix performance, and asked how stable Typescript LSP performance should be
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/2503#issuecomment-3752145034) **gabritto** requested a repro project or CPU profile log to investigate JSX completions slowness
 * [later](https://github.com/microsoft/TypeScript-go/issues/2503#issuecomment-3784284733) **jansedlon** said "Hey grabritto, sorry for the delay. I tried it today and for some reason it worked fine. When it happens again, i will take a cpu profile and send it to you"

### [Issue microsoft/TypeScript-go#2506](https://github.com/microsoft/TypeScript-go/issues/2506) (Open, `Domain: Editor`, **andrewbranch**)

**Stale module resolution error after linking pnpm workspace dependency due to watcher configuration/handling**

*VS Code’s watcher ignoring directory-level symlink events outside its file-extension glob causes stale module resolution errors after pnpm workspace linking.*

 * created by **andrewbranch**
 * (1 week ago) **andrewbranch** added label `Domain: Editor`, and assigned to **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#2543](https://github.com/microsoft/TypeScript-go/pull/2543) (Closed, `dependencies`, `github_actions`)

**Bump the github\-actions group across 1 directory with 2 updates**

*Update GitHub Actions in the root directory by bumping actions/setup-node to v6.2.0 and upgrading github/codeql-action.*

 * (2 days ago) **dependabot[bot]** added labels `github_actions`, `dependencies`, `github_actions`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2545](https://github.com/microsoft/TypeScript-go/issues/2545) (Closed)

**\`tsgo \-b \-v\` differs in output directory**

*tsgo’s `-b -v` build command emits output into dist/src/ rather than the expected dist/ directory.*

 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/2545#issuecomment-3770967313) **TheArcaneBrony** said "Ah, I figured it out... i was doing rm -rf dist/*, but tsconfig.tsbuildinfo was moved from dist/ to ./, which was causing it to skip compilation at all..."
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2545#issuecomment-3774517511) **sheetalkamat** demonstrated the expected TS5011 error in TypeScript 6.0 when rootDir was not specified
 * (yesterday) **sheetalkamat** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/issues/2545#issuecomment-3779942855) **jakebailey** said "Should we port that error from TS 6.0, just for the time being until 6.0 is properly out as the stable version?"

### [PR microsoft/TypeScript-go#2549](https://github.com/microsoft/TypeScript-go/pull/2549) (Closed)

**Include overlays in all file systems used in snapshot building**

*Incorporate overlays into tsconfig root discovery and model file opens as creates and closes as deletes to resolve snapshot errors.*

 * created by **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#2552](https://github.com/microsoft/TypeScript-go/pull/2552) (Closed)

**Fix incorrect search in all files when searching for container**

*Update search functionality to correctly find occurrences of “container” when searching across all files*

 * created by **sheetalkamat**
 * (today) **sheetalkamat** closed the issue

### [Issue microsoft/TypeScript-go#2555](https://github.com/microsoft/TypeScript-go/issues/2555) (Open, `Domain: Editor`)

**Installing Native Preview broke TS Imports**

*Installing VS Code’s Native Preview TypeScript extension on macOS breaks TypeScript auto-import suggestions despite reverting settings and reinstalling the editor.*

 * created by **tikki100**
 * **tikki100** added label `Domain: Editor`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2555#issuecomment-3778473834) **rubnogueira** suggested including the "node" types in tsconfig.json and referenced a TypeScript issue for defaults
 * [today](https://github.com/microsoft/TypeScript-go/issues/2555#issuecomment-3779894761) **tikki100** reported that the suggestion did not resolve the issue and provided detailed reproduction steps

### [PR microsoft/TypeScript-go#2556](https://github.com/microsoft/TypeScript-go/pull/2556) (Closed)

**\[Experiment\] avoid OrderedMap in widening context properties**

*Experiment to avoid using OrderedMap for widening context properties by exploring alternative data structures*

 * created by **a-tarasyuk**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2556#issuecomment-3780643034) **DanielRosenwasser** said "I'm guessing you also tried NewOrderedMapWithSizeHint and there's too much indirection for that to be compiled away."

### [Issue microsoft/TypeScript-go#2557](https://github.com/microsoft/TypeScript-go/issues/2557) (Closed, `Domain: Editor`)

**Suggestions freeze and stop working until I close and open the file again**

*TypeScript suggestions and IntelliSense features freeze in a specific file until it’s closed and reopened*

 * created by **rubnogueira**
 * **rubnogueira** added label `Domain: Editor`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2557#issuecomment-3780175165) **andrewbranch** provided steps to enable and view trace logs in the typescript-native-preview LSP output pane for debugging
 * **andrewbranch** added label `Needs More Info`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2557#issuecomment-3780511722) **rubnogueira** said "@andrewbranch I emailed you with some logs since they contain private info. I don't see anything relevant, and it's very verbose, so maybe I'm missing something."
 * [today](https://github.com/microsoft/TypeScript-go/issues/2557#issuecomment-3781529261) **rubnogueira** created a reproduction repository and noted the issue was easier to trigger in large codebases, mentioning it could occur inside and outside the rootDir and providing a video link
 * [today](https://github.com/microsoft/TypeScript-go/issues/2557#issuecomment-3781978785) **andrewbranch** reviewed the logs, attributed the issue to a VS Code bug that stopped diagnostics requests, and asked @mjbvz for insight
 * [today](https://github.com/microsoft/TypeScript-go/issues/2557#issuecomment-3781982366) **andrewbranch** asked DanielRosenwasser if the repro matched stale errors he’d seen previously
 * [today](https://github.com/microsoft/TypeScript-go/issues/2557#issuecomment-3781997961) **andrewbranch** said "Wow, I was able to repro this immediately with @rubnogueira’s example repo, and can confirm that we’re in a good state while the client just stops asking for new errors."
 * [today](https://github.com/microsoft/TypeScript-go/issues/2557#issuecomment-3782009190) **andrewbranch** described stale errors persisting across language server restarts and causing crashes when requesting code fixes
 * [later](https://github.com/microsoft/TypeScript-go/issues/2557#issuecomment-3783442883) **rubnogueira** expressed happiness that the issue was reproduced, noted it occurred in both VSCode and Cursor, offered additional context, and affirmed that Corsa's pros outweigh the inconvenience
 * [later](https://github.com/microsoft/TypeScript-go/issues/2557#issuecomment-3783645878) **lukpsaxo** reported that TypeScript stopped updating on file edits over the last two days, requiring file reopen or plugin restart, and shared logs illustrating the issue

### [Issue microsoft/TypeScript-go#2558](https://github.com/microsoft/TypeScript-go/issues/2558) (Closed, `bug`, **RyanCavanaugh**, **Copilot**)

**Incorrect output using \`export = NamedInput\`**

*tsgo incorrectly emits `module.exports = Foo` instead of `module.exports = Foo_1.Foo` when exporting a named import via export =, causing a runtime ReferenceError.*

 * created by **psm14**
 * (today) **RyanCavanaugh** added label `bug`, and assigned to **Copilot**, **RyanCavanaugh**
 * (later) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2559](https://github.com/microsoft/TypeScript-go/issues/2559) (Open, `Crash`, **andrewbranch**, **Copilot**)

**Quick fix crash when promoting type\-only import to value and existing type import precedes new value import**

*Converting a type-only import to a value import via quick fix panics the TypeScript language server.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** added label `Crash`, and assigned to **jakebailey**

### [PR microsoft/TypeScript-go#2560](https://github.com/microsoft/TypeScript-go/pull/2560) (Closed, **RyanCavanaugh**, **Copilot**)

**Fix export = named import to emit correct property access**

*Update the appendExportEqualsIfNeeded function to correctly emit property access in CommonJS export assignments for named imports.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2560#issuecomment-3781562786) **RyanCavanaugh** said "@copilot you need to run tests and accept modified baselines"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2560#issuecomment-3781607714) **Copilot** ran tests and accepted modified baselines for es6ImportNamedImportInExportAssignment.js, errorForConflictingExportEqualsValue.js, and declarationEmitExportAssignment.js
 * [today](https://github.com/microsoft/TypeScript-go/pull/2560#issuecomment-3782122651) **jakebailey** said "Pushed that to the PR, just so it's done now."
 * (later) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2561](https://github.com/microsoft/TypeScript-go/issues/2561) (Open, `Crash`)

**v0\.20260119\.1 crashes ts server for large project, v0\.20260116\.1 works**

*TypeScript Native Preview v0.20260119.1 crashes the TS server on large, high-memory projects, whereas v0.20260116.1 works.*

 * created by **austinfennacy**
 * **austinfennacy** added label `Crash`

### [PR microsoft/TypeScript-go#2562](https://github.com/microsoft/TypeScript-go/pull/2562) (Closed)

**Fix porting bug in resolveAutomaticTypeDirectives**

*Fix resolveAutomaticTypeDirectives mapping undefined to ResolutionModeNone to align with TypeScript and prevent duplicate type directives*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#2563](https://github.com/microsoft/TypeScript-go/pull/2563) (Closed)

**Don't request auto imports in untitled files**

*Prevent automatic import requests from being sent in untitled files.*

 * created by **andrewbranch**

### [PR microsoft/TypeScript-go#2564](https://github.com/microsoft/TypeScript-go/pull/2564) (Closed)

**Always bundle extension**

*Bundle the extension’s dependencies to fix null extension errors and incorporate problem matchers without extra installs.*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#2565](https://github.com/microsoft/TypeScript-go/pull/2565) (Open)

**Experiment with emulating typing within editor in fourslash tests**

*Experiment with emulating typing in Corsa's fourslash tests like Strada to improve tests despite diagnostic errors and timeouts.*

 * created by **DanielRosenwasser**

### [Issue microsoft/TypeScript-go#2566](https://github.com/microsoft/TypeScript-go/issues/2566) (Closed, `Domain: Editor`)

**suggestor does not suggest the module name when typing it**

*The tsgo extension does not auto-suggest local module file names when typing import paths like tsserver does.*

 * created by **Redaloukil**
 * **Redaloukil** added label `Domain: Editor`

### [PR microsoft/TypeScript-go#2567](https://github.com/microsoft/TypeScript-go/pull/2567) (Closed)

**Cache widening contexts for nested object literals**

*Cache widening contexts for nested object literal spreads to reduce type-checking time from 17 seconds to under 0.1 seconds.*

 * created by **ahejlsberg**

