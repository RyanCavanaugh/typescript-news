# Report for 2026-01-20 (Tuesday, January 20th, 2026)

16 different users commented on 27 different issues.

## Recommended Actions

 * Response Recommended
    * @nirweiner2 confirmed the issue and provided environment details in [microsoft/TypeScript-go#2239](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3773710486)
    * @AndreMaz asked if a linked comment was enough to isolate the source of the issue in [microsoft/TypeScript-go#2239](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3774443589)
    * @ashah360 reported that reverting to release 0.20251204.2 reduced memory usage in [microsoft/TypeScript-go#2239](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3775224374)
    * @MartinCura asked how often a new extension release is cut and whether they can install from a commit in [microsoft/TypeScript-go#2239](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3777897123)
    * @chriskrycho confirmed that the fix resolved a stack overflow in their code in [microsoft/TypeScript-go#2532](https://github.com/microsoft/TypeScript-go/pull/2532#issuecomment-3775381395)

## Activity Summary

### [Issue microsoft/TypeScript-go#1315](https://github.com/microsoft/TypeScript-go/issues/1315) (Closed, `Domain: Editor`, `Crash`, **andrewbranch**)

**vscode \- panic \- project not found**

*The Microsoft TypeScript Go language server intermittently panics with "project not found" during diagnostics after switching branches that change tsconfig files.*

 * [25 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1315#issuecomment-3115358915) **mjames-c** reported encountering a panic when navigating between TypeScript projects with project references, and provided file layout and repro steps
 * [25 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1315#issuecomment-3115360613) **jakebailey** said "There's a big refactor of the language server @andrewbranch's been working on which should make this sort of issue a thing of the past."
 * [20 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1315#issuecomment-3236541902) **lukpsaxo** reported a popup diagnostic error due to a filename typo and noted it shouldn't occur
 * [today](https://github.com/microsoft/TypeScript-go/issues/1315#issuecomment-3774137611) **andrewbranch** said "Rolling this into https://github.com/microsoft/typescript-go/issues/1967 as the code in the original stack no longer exists"
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#1319](https://github.com/microsoft/TypeScript-go/issues/1319) (Closed, `Domain: Editor`, `Crash`, **andrewbranch**)

**vscode \- panic \- file not found**

*Switching to a branch that deletes an open file causes the VSCode TypeScript extension to panic.*

 * [25 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1319#issuecomment-3130956102) **lukpsaxo** reported a panic stack trace when moving a file
 * [20 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1319#issuecomment-3235928521) **lukpsaxo** reported a new stack trace showing diagnostic failures for file:///x.ts due to missing project and noting no panic occurred
 * **jakebailey** assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/issues/1319#issuecomment-3774130938) **andrewbranch** said "Rolling this into #1967 as the code in the original stack no longer exists"
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#1465](https://github.com/microsoft/TypeScript-go/issues/1465) (Closed, `Crash`, `Domain: Program`, **sheetalkamat**)

**Intermittent crash with \-\-incremental**

*tsgo intermittently crashes when run with --incremental on large projects in frequent CI pipelines*

 * (6 weeks ago) **sheetalkamat** closed the issue
 * [6 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1465#issuecomment-3617924178) **jakebailey** said "The above user was testing yesterdays build, but I will extract that to a new issue"
 * (4 days ago) **sheetalkamat** reopened the issue
 * (today) **sheetalkamat** closed the issue

### [Issue microsoft/TypeScript-go#1983](https://github.com/microsoft/TypeScript-go/issues/1983) (Closed, `Domain: Editor`, `Crash`, **andrewbranch**)

**textDocument/diagnostic failed**

*textDocument/diagnostic requests repeatedly panic due to missing parse cache entries in the TypeScript Go project snapshot clone*

 * (9 weeks ago) **andrewbranch** reopened the issue
 * **jakebailey** added label `Crash`
 * [9 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1983#issuecomment-3550064071) **andrewbranch** reproduced a failure to find a project for a file and provided reproduction steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/1983#issuecomment-3774151638) **andrewbranch** said "Note that the panic stack traces here are unrelated to the UI error message. I’m going to treat this issue is tracking the “project not found” error message, not the panic."

### [Issue microsoft/TypeScript-go#2239](https://github.com/microsoft/TypeScript-go/issues/2239) (Closed, `Needs More Info`)

**take too much memory**

*tsgo extension consumes about 17GB of RAM on macOS M1, causing heavy swapping and slowing VS Code.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3767242958) **dream2333** said "same"
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3768557703) **MartinCura** described experiencing increasing memory usage in tsgo on each save, tested it, attached a heap profile and screenshot, and suggested periodic restarts
 * [today](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3772234647) **rubnogueira** described IDE performance degrading over time due to high RAM usage with pnpm and tsconfig project references after fixes #2390 and #2502
 * [today](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3773710486) **nirweiner2** confirmed experiencing the issue and mentioned using pnpm, tsconfig, project references, and a large codebase
 * [today](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3774443589) **AndreMaz** asked if the linked issue comment was enough to isolate the source of the issue and offered to provide additional info
 * [today](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3775169353) **jakebailey** said "I think @andrewbranch might have a better idea, given it's the auto import rewrite that seems to have caused this"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3775221469) **andrewbranch** noted that the issue was opened weeks before the bad commit
 * [today](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3775224374) **ashah360** said "Switching to a previous release for now (0.20251204.2) solved this for me. Memory consumption was peaking at around ~70gigs, now back down to <10 ."
 * (today) **andrewbranch** closed the issue
 * [later](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3777897123) **MartinCura** said "awesome! how often is a new extension release cut? or can i install from a commit?"
 * [later](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3778827946) **jakebailey** said "We release majorly, so it's already out."

### [PR microsoft/TypeScript-go#2491](https://github.com/microsoft/TypeScript-go/pull/2491) (Open, **DanielRosenwasser**, **Copilot**)

**Fix nil pointer panic in JSDoc callable type completions**

*Completing JSDoc callable type signatures with parameters causes a nil pointer panic due to missing symbol nil check.*

 * **Copilot** assigned to **DanielRosenwasser**
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/2491#issuecomment-3741753660) **DanielRosenwasser** said "I feel like the investigation here is good but I don't understand why the parameter didn't have a symbol."
 * [6 days ago](https://github.com/microsoft/TypeScript-go/pull/2491#issuecomment-3750868286) **ahejlsberg** explained that JSDoc comments don't bind symbols and described how the parameter in the reparsed object literal type obtains its symbol
 * [today](https://github.com/microsoft/TypeScript-go/pull/2491#issuecomment-3775001659) **DanielRosenwasser** said "@ahejlsberg said that the real issue is that we need to get the reparsed node (via getReparsedNodeForNode) - not sure where the best place is to put this but figure it out @copilot."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2491#issuecomment-3775047626) **Copilot** described exporting GetReparsedNodeForNode and using it in getSignatureFromDeclaration to fix the reparsed parameter node issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/2491#issuecomment-3775306263) **DanielRosenwasser** said "We think the call to getReparsedNodeForNode should have happened at a "more general" place and not exported from the package. @copilot try to figure something else out."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2491#issuecomment-3775355912) **Copilot** investigated a non-exported use of getReparsedNodeForNode, identified performance issues during type checking, and applied a minimal nil check fix in commit f000b0e6

### [PR microsoft/TypeScript-go#2515](https://github.com/microsoft/TypeScript-go/pull/2515) (Closed)

**\[LSP\] Process file deletions against tsconfig \`includes\`**

*Trigger tsconfig reloads on file deletions matching includes wildcards to promptly remove deleted source files.*

 * created by **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2515#issuecomment-3774216643) **andrewbranch** said "Incorporating this into a larger PR"
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#2525](https://github.com/microsoft/TypeScript-go/pull/2525) (Closed, **RyanCavanaugh**, **Copilot**)

**Fix stack overflow when checking destructuring with self\-referencing shorthand**

*Shorthand self-referencing in object destructuring with a union type causes infinite recursion and stack overflow.*

 * created by **Copilot**
 * (4 days ago) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#2532](https://github.com/microsoft/TypeScript-go/pull/2532) (Closed)

**Incremental fixes**

*Resolve stack overflow errors caused by reference cycles with const enum usage through incremental fixes.*

 * created by **sheetalkamat**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2532#issuecomment-3775381395) **chriskrycho** confirmed that the fix resolved a stack overflow in their code path
 * (today) **sheetalkamat** closed the issue

### [Issue microsoft/TypeScript-go#2545](https://github.com/microsoft/TypeScript-go/issues/2545) (Closed)

**\`tsgo \-b \-v\` differs in output directory**

*tsgo’s `-b -v` build command emits output into dist/src/ rather than the expected dist/ directory.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2545#issuecomment-3770951841) **TheArcaneBrony** reported that the change omitted some code, causing a MODULE_NOT_FOUND error for a missing file
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2545#issuecomment-3770956577) **jakebailey** asked for the full repro and noted that warning messages hadn’t historically been used
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2545#issuecomment-3770967313) **TheArcaneBrony** said "Ah, I figured it out... i was doing rm -rf dist/*, but tsconfig.tsbuildinfo was moved from dist/ to ./, which was causing it to skip compilation at all..."
 * [today](https://github.com/microsoft/TypeScript-go/issues/2545#issuecomment-3774517511) **sheetalkamat** demonstrated the expected TS5011 error in TypeScript 6.0 when rootDir was not specified
 * (today) **sheetalkamat** closed the issue

### [Issue microsoft/TypeScript-go#2546](https://github.com/microsoft/TypeScript-go/issues/2546) (Closed)

**\[Typo\] Possible typo in JSDoc string for \`Math\.trunc\(…\)\` function \(lib\.es2015\.core\.d\.ts\)**

*Correct the JSDoc in lib.es2015.core.d.ts to fix ‘the a numeric expression’ typo in the Math.trunc comment.*

 * created by **o-m12a**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2546#issuecomment-3773725095) **jakebailey** said "This needs to happen in the main repo, as lib files are just a copy of that repo's contents and must match between v6 and v7."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2547](https://github.com/microsoft/TypeScript-go/pull/2547) (Closed)

**Fix a typo in the JSDoc of \`Math\.trunc\(…\)\`**

*Corrects a typo in the JSDoc comment for the Math.trunc function.*

 * created by **o-m12a**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2547#issuecomment-3773715806) **jakebailey** said "This is a generated file from the main repo; please send a PR there."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2548](https://github.com/microsoft/TypeScript-go/pull/2548) (Closed)

**Remove code related to dead compiler options**

*Remove obsolete compiler option handling by dropping related code and associated diffs.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2549](https://github.com/microsoft/TypeScript-go/pull/2549) (Closed)

**Include overlays in all file systems used in snapshot building**

*Incorporate overlays into tsconfig root discovery and model file opens as creates and closes as deletes to resolve snapshot errors.*

 * created by **andrewbranch**

### [Issue microsoft/TypeScript-go#2550](https://github.com/microsoft/TypeScript-go/issues/2550) (Closed, `Crash`, **andrewbranch**)

**Crash for auto\-imports from untitled file to saved tsx file**

*Auto-import completions from an untitled JavaScript buffer to a saved TSX file cause a nil pointer dereference crash.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** added label `Crash`, and assigned to **andrewbranch**

### [Issue microsoft/TypeScript-go#2551](https://github.com/microsoft/TypeScript-go/issues/2551) (Closed, `Domain: Performance`, **ahejlsberg**)

**2x slower than tsc on a NestJS codebase**

*tsgo type checking on a NestJS application is twice as slow as tsc due to excessive memory allocations in getSiblingsOfContext.*

 * created by **FelixMalfait**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2551#issuecomment-3775576129) **RyanCavanaugh** confirmed a repro and provided extended diagnostics with metrics comparing tsc and tsgo performance
 * (today) **RyanCavanaugh** added label `Domain: Performance`, and assigned to **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2551#issuecomment-3775614699) **RyanCavanaugh** asked whether any functions in the codebase had a very large number of object-literal return statements
 * [today](https://github.com/microsoft/TypeScript-go/issues/2551#issuecomment-3775797439) **jakebailey** instrumented the code and observed that a specific call took 5 minutes to resolve
 * [today](https://github.com/microsoft/TypeScript-go/issues/2551#issuecomment-3776104329) **RyanCavanaugh** reported that commenting out the call reduced compile time from 139s to 2s and offered to isolate a repro
 * [today](https://github.com/microsoft/TypeScript-go/issues/2551#issuecomment-3776215289) **ahejlsberg** said "Crazy. We must be missing some caching somewhere."
 * [today](https://github.com/microsoft/TypeScript-go/issues/2551#issuecomment-3776273128) **RyanCavanaugh** provided a gist with repro instructions and timing data indicating a performance speedup when making a function non-generic
 * (today) **RyanCavanaugh** assigned to **Copilot**, **RyanCavanaugh**, and unassigned **RyanCavanaugh**, **Copilot**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2551#issuecomment-3776476318) **RyanCavanaugh** presented a reproduction case showing compilation timings of 11.2s in tsgo and 5.3s in tsc
 * [today](https://github.com/microsoft/TypeScript-go/issues/2551#issuecomment-3776631389) **FelixMalfait** said "Wow thanks for jumping on that so quickly!"

### [PR microsoft/TypeScript-go#2552](https://github.com/microsoft/TypeScript-go/pull/2552) (Closed)

**Fix incorrect search in all files when searching for container**

*Update search functionality to correctly find occurrences of “container” when searching across all files*

 * created by **sheetalkamat**

### [PR microsoft/TypeScript-go#2553](https://github.com/microsoft/TypeScript-go/pull/2553) (Closed)

**Remove accidental method pointer**

*Accidental method pointer to toPath on compilerHost retained projectCollectionBuilder and needs to be removed.*

 * created by **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#2554](https://github.com/microsoft/TypeScript-go/pull/2554) (Closed, **RyanCavanaugh**, **Copilot**)

**Add minimal repro for spread intersection performance issue**

*A minimal TypeScript reproduction demonstrates exponential type checking slowdown caused by nested spreads on intersection-based discriminated unions.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2554#issuecomment-3776486606) **RyanCavanaugh** said "Nice"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#2555](https://github.com/microsoft/TypeScript-go/issues/2555) (Open, `Domain: Editor`)

**Installing Native Preview broke TS Imports**

*Installing VS Code’s Native Preview TypeScript extension on macOS breaks TypeScript auto-import suggestions despite reverting settings and reinstalling the editor.*

 * created by **tikki100**
 * **tikki100** added label `Domain: Editor`
 * [later](https://github.com/microsoft/TypeScript-go/issues/2555#issuecomment-3778473834) **rubnogueira** suggested including the "node" types in tsconfig.json and referenced a TypeScript issue for defaults

### [PR microsoft/TypeScript-go#2556](https://github.com/microsoft/TypeScript-go/pull/2556) (Closed)

**\[Experiment\] avoid OrderedMap in widening context properties**

*Experiment to avoid using OrderedMap for widening context properties by exploring alternative data structures*

 * created by **a-tarasyuk**

### [Issue microsoft/TypeScript-go#2557](https://github.com/microsoft/TypeScript-go/issues/2557) (Closed, `Domain: Editor`)

**Suggestions freeze and stop working until I close and open the file again**

*TypeScript suggestions and IntelliSense features freeze in a specific file until it’s closed and reopened*

 * created by **rubnogueira**
 * **rubnogueira** added label `Domain: Editor`

