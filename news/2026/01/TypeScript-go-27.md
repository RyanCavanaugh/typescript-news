# Report for 2026-01-27 (Tuesday, January 27th, 2026)

13 different users commented on 30 different issues.

## Recommended Actions

 * Response Recommended
    * @Moltenship provided repro steps and memory profiles as requested in [microsoft/TypeScript-go#2239](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3811376292)
    * @clinuxrulz reported missing type inference in chained calls in [microsoft/TypeScript-go#2434](https://github.com/microsoft/TypeScript-go/pull/2434#issuecomment-3808239583)
    * @ffmiruz asked which behavior is correct for error reporting between tsc and tsgo in [microsoft/TypeScript-go#2583](https://github.com/microsoft/TypeScript-go/issues/2583#issuecomment-3806457628)
    * @dtscd asked if a PR to correct namespace assignments would be accepted in [microsoft/TypeScript-go#961](https://github.com/microsoft/TypeScript-go/issues/961#issuecomment-3806351229)
    * @dtscd asked for more nuanced resolution behavior regarding cross-file namespaces in [microsoft/TypeScript-go#961](https://github.com/microsoft/TypeScript-go/issues/961#issuecomment-3807692564)
    * @dtscd requested tsgo to issue an error when it can resolve types but cannot perform the final transformation in [microsoft/TypeScript-go#961](https://github.com/microsoft/TypeScript-go/issues/961#issuecomment-3807733217)
    * @dtscd asked for clarification on the use case for namespaces in [microsoft/TypeScript-go#961](https://github.com/microsoft/TypeScript-go/issues/961#issuecomment-3808167779)

## Activity Summary

### [Issue microsoft/TypeScript-go#2239](https://github.com/microsoft/TypeScript-go/issues/2239) (Closed, `Needs More Info`)

**take too much memory**

*tsgo extension consumes about 17GB of RAM on macOS M1, causing heavy swapping and slowing VS Code.*

 * [6 days ago](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3782713289) **jakebailey** said "Okay, it's been resolved, so the latest version on npm and in VS Code should have the most recent fixes."
 * [6 days ago](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3782764903) **oorestisime** said "Big thanks people! "
 * [6 days ago](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3782854830) **Moltenship** reported similar memory consumption issue after the recent fix and provided environment details along with heap and allocation profile attachments
 * [later](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3811376292) **Moltenship** reported that memory consumption exceeded the set limit when finding references on version 1.108.1, provided heap and allocation profiles, and noted the issue persists from extension version 0.20251122.1 onward

### [PR microsoft/TypeScript-go#2434](https://github.com/microsoft/TypeScript-go/pull/2434) (Open)

**Experiment: Quantified Types**

*Seeking a TypeScript function signature to consume an array of heterogeneous Layer objects without collapsing distinct generics.*

 * [5 days ago](https://github.com/microsoft/TypeScript-go/pull/2434#issuecomment-3787582505) **Diggsey** expressed desire for quantified types and argued that reverse mapped types leak complexity compared to quantified types, noting that function types already support quantification
 * [4 days ago](https://github.com/microsoft/TypeScript-go/pull/2434#issuecomment-3793031614) **clinuxrulz** proposed an effect pipe example and stated it could only be implemented via existential types
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/2434#issuecomment-3794171335) **devanshj** suggested implementing `pipe` without existential types using finite overloads and provided example links
 * [today](https://github.com/microsoft/TypeScript-go/pull/2434#issuecomment-3808239583) **clinuxrulz** observed that types weren't inferred in the chain and provided an infinite params example

### [Issue microsoft/TypeScript-go#2460](https://github.com/microsoft/TypeScript-go/issues/2460) (Closed, `Crash`, **ahejlsberg**)

**textDocument/inlayHint: Cannot create token from reparsed node of kind KindFunctionExpression**

*textDocument/inlayHint request panics due to inability to create a token from a reparsed function expression node*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2460#issuecomment-3730068931) **rubnogueira** asked whether the provided repro was sufficient or if they should create one, and reported an inlayHint error when opening js files with logs
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2460#issuecomment-3743948547) **rubnogueira** reported a crash when opening Gruntfile.js at the require line
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/2460#issuecomment-3789803553) **rubnogueira** provided a minimal repro link and described how to trigger the alert by opening Gruntfile.js
 * **ahejlsberg** assigned to **ahejlsberg**
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#2469](https://github.com/microsoft/TypeScript-go/pull/2469) (Closed)

**Update JsxOpeningElement type**

*Correct the JsxOpeningElement type to reflect that it can only appear as a child of a JsxElement rather than as an Expression.*

 * created by **ArnaudBarre**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2469#issuecomment-3806630317) **andrewbranch** said "It's Expression in Strada, but it ends up not mattering. I agree it doesn’t make sense to consider it an expression."
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#2528](https://github.com/microsoft/TypeScript-go/pull/2528) (Closed, **RyanCavanaugh**, **Copilot**)

**\[WIP\] Fix stack overflow in code type checking**

*Resolve stack overflow in TypeScript strict type checking for destructured union types with circular references.*

 * created by **Copilot**
 * (1 week ago) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * (today) **DanielRosenwasser** closed the issue

### [Issue microsoft/TypeScript-go#2540](https://github.com/microsoft/TypeScript-go/issues/2540) (Closed)

**Should handle \`FORCE\_COLOR\` environment variable**

*Support the FORCE_COLOR environment variable to override TTY detection and enable colored output for exec calls*

 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/2540#issuecomment-3794012015) **silverwind** stated that an env var check was sufficient for FORCE_COLOR support and that using FORCE_COLOR simplified color handling by delegating to the user
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/2540#issuecomment-3794020457) **jakebailey** said "I don't think we need anything more fancy (see how picocolors does it). We wouldn't take on a dep for this anyhow, since we need to be able to test it, via our own host abstraction."
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/2540#issuecomment-3794030946) **silverwind** said "Yeah FORCE_COLOR support would be sufficient to get color output in cases where stdout is not a TTY, like on CI environments."
 * [today](https://github.com/microsoft/TypeScript-go/issues/2540#issuecomment-3807292909) **jakebailey** said "Give #2596 a try."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2541](https://github.com/microsoft/TypeScript-go/pull/2541) (Closed)

**Update CHANGES\.md to reflect \#2513**

*Update CHANGES.md to reflect changes introduced by pull request #2513*

 * created by **ahejlsberg**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2555](https://github.com/microsoft/TypeScript-go/issues/2555) (Open, `Domain: Editor`)

**Installing Native Preview broke TS Imports**

*Installing VS Code’s Native Preview TypeScript extension on macOS breaks TypeScript auto-import suggestions despite reverting settings and reinstalling the editor.*

 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/2555#issuecomment-3794827972) **bastiankistner** described lacking import autocompletions, noted go-to-definition works, recalled it worked previously, and offered to post logs/traces
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2555#issuecomment-3798728940) **tikki100** said "Related?: https://github.com/microsoft/typescript-go/issues/2582"
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2555#issuecomment-3800314263) **ericnorris** stated that their issue was about the types field in package.json, not compilerOptions in tsconfig.json
 * [today](https://github.com/microsoft/TypeScript-go/issues/2555#issuecomment-3809296472) **DanielRosenwasser** informed that a PR addressing the autocomplete issue had been submitted

### [PR microsoft/TypeScript-go#2571](https://github.com/microsoft/TypeScript-go/pull/2571) (Closed, **RyanCavanaugh**, **Copilot**)

**Fix \-\-showConfig to print enumerated value names, not integers**

*Update --showConfig to serialize compiler and watch option enums as their string names instead of numeric codes.*

 * **Copilot** assigned to **RyanCavanaugh**
 * [5 days ago](https://github.com/microsoft/TypeScript-go/pull/2571#issuecomment-3786845813) **jakebailey** asked if this was the same as #2570 and noted missing tests for --showConfig
 * [5 days ago](https://github.com/microsoft/TypeScript-go/pull/2571#issuecomment-3786881330) **jakebailey** criticized the approach as hopeless and suggested porting the old code using compiler options declarations instead of JSON packages
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#2572](https://github.com/microsoft/TypeScript-go/issues/2572) (Closed, `Crash`, `Needs More Info`, **andrewbranch**)

**no project found for URI: textDocument/foldingRange and textDocument/diagnostic**

*Language server folding range and diagnostic requests fail for vitest.config.ts because it’s not included in any TypeScript project*

 * **andrewbranch** assigned to **andrewbranch**
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2572#issuecomment-3800785869) **andrewbranch** requested logs from the textDocument/didOpen request and explained tsconfig resolution with composite projects and overlapping directories
 * **andrewbranch** added label `Needs More Info`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2572#issuecomment-3807819913) **rubnogueira** said "Closing this issue, I've not been able to reproduce this since I created this issue, and I believe that it is fixed."
 * (today) **rubnogueira** closed the issue

### [Issue microsoft/TypeScript-go#2580](https://github.com/microsoft/TypeScript-go/issues/2580) (Closed, `Crash`, **DanielRosenwasser**, **Copilot**)

**textDocument/completion runtime error: invalid memory address or nil pointer dereference**

*textDocument/completion handler in the TypeScript-Go language server panics with a nil pointer dereference when computing import statement completions.*

 * (yesterday) **DanielRosenwasser** assigned to **Copilot**, **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2580#issuecomment-3803855923) **sanny-io** thanked the maintainer and apologized for not narrowing down the crash context
 * [today](https://github.com/microsoft/TypeScript-go/issues/2580#issuecomment-3806975306) **DanielRosenwasser** said "Don't sweat it! Sorry, I wasn't trying to say your repro wasn't helpful, it was more for the agent 😄"

### [Issue microsoft/TypeScript-go#2583](https://github.com/microsoft/TypeScript-go/issues/2583) (Closed, `duplicate`, **ahejlsberg**)

**tsgo fails to report TS2769 for mutually\-exclusive object overloads**

*tsgo does not report TS2769 for mutually exclusive object overloads while tsc correctly flags the error.*

 * created by **r253hmdryou**
 * (yesterday) **ahejlsberg** added label `bug`, and assigned to **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2583#issuecomment-3806457628) **ffmiruz** described how tsc and tsgo differ in error reporting locations and asked which behavior was correct
 * [today](https://github.com/microsoft/TypeScript-go/issues/2583#issuecomment-3806568300) **jakebailey** said "This is #1088, then?"
 * **ahejlsberg** removed label `bug`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2583#issuecomment-3806745269) **ahejlsberg** acknowledged that marking it as a bug was premature and that the tsgo behavior was an intended difference per issue #1088
 * **ahejlsberg** added label `duplicate`
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#2584](https://github.com/microsoft/TypeScript-go/pull/2584) (Open, **DanielRosenwasser**, **Copilot**)

**Fix autocomplete suggesting unexported internal files from monorepo packages**

*Adjust autocomplete import logic to ignore empty package names and prevent suggesting unexported internal files in monorepo packages.*

 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/2584#issuecomment-3797320611) **ericnorris** noted that having a version field prevented auto-import from leaking transitive files and suggested investigating allowing an empty version field
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2584#issuecomment-3801288843) **andrewbranch** described expected behavior of module.GetResolvedEntrypoints and GetModuleSpecifier, expressed confusion about package.json version relevance, and requested a thorough investigation of the root cause
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2584#issuecomment-3801309418) **andrewbranch** said "@copilot try again"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2584#issuecomment-3806965130) **andrewbranch** said "@copilot it's a new day, see if your infrastructure will let you do anything now"

### [PR microsoft/TypeScript-go#2589](https://github.com/microsoft/TypeScript-go/pull/2589) (Closed, **DanielRosenwasser**, **Copilot**)

**Fix nil pointer dereference in import statement completions**

*Add nil check to prevent nil pointer dereference panic in import statement completions after typing keywords.*

 * created by **Copilot**
 * (yesterday) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2589#issuecomment-3806987994) **DanielRosenwasser** said "@copilot format"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2589#issuecomment-3807023592) **Copilot** formatted code in commit 7e1f796a
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2590](https://github.com/microsoft/TypeScript-go/issues/2590) (Closed, `Crash`, **DanielRosenwasser**, **Copilot**)

**Completions crash after \`import\` when statement is preceded by JSDoc**

*Requesting completions immediately after an import statement that follows a JSDoc comment triggers a panic crash.*

 * (today) **DanielRosenwasser** added label `Crash`, and assigned to **Copilot**, **DanielRosenwasser**
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#2591](https://github.com/microsoft/TypeScript-go/pull/2591) (Closed, **DanielRosenwasser**, **Copilot**)

**Fix crash when completing after import preceded by JSDoc**

*Completion requests after an import preceded by JSDoc comments panic due to node.Pos() including comment trivia.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2591#issuecomment-3809305475) **DanielRosenwasser** said "@copilot accept baselines."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2591#issuecomment-3809333998) **Copilot** described that baselines were accepted and synced with no changes needed
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#2592](https://github.com/microsoft/TypeScript-go/pull/2592) (Closed)

**Support \`Object\.defineProperty\` in document symbols**

*Add support for Object.defineProperty in document symbols and refactor code to allow direct symbol name passing in special cases.*

 * created by **gabritto**

### [PR microsoft/TypeScript-go#2593](https://github.com/microsoft/TypeScript-go/pull/2593) (Closed)

**Exclude reparsed nodes from inlay hints**

*Modify the inlay hints feature to ignore reparsed nodes, ensuring hints only appear for stable code segments.*

 * created by **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2593#issuecomment-3807125411) **DanielRosenwasser** asked to add the regression test from issue 2460 in another PR and provided the test code
 * [today](https://github.com/microsoft/TypeScript-go/pull/2593#issuecomment-3807126186) **Copilot** said "@DanielRosenwasser I've opened a new pull request, #2595, to work on those changes. Once the pull request is ready, I'll request review from you."
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#2594](https://github.com/microsoft/TypeScript-go/pull/2594) (Closed)

**Skip flaky formatting test for now**

*Skip a flaky formatting test in CI by marking it as skipped to prevent intermittent failures.*

 * created by **gabritto**
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript-go#2595](https://github.com/microsoft/TypeScript-go/pull/2595) (Open, **DanielRosenwasser**, **Copilot**)

**Add regression test for inlay hints crash on reparsed nodes**

*Adds a JavaScript regression test to ensure inlayHint no longer panics on reparsed function expression nodes in module exports*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **DanielRosenwasser**

### [PR microsoft/TypeScript-go#2596](https://github.com/microsoft/TypeScript-go/pull/2596) (Closed)

**Support FORCE\_COLOR**

*Add support for the FORCE_COLOR environment variable to enable forced colored output in tsgo.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2597](https://github.com/microsoft/TypeScript-go/pull/2597) (Open)

**internal/transformers/tstransformers: fix unqualified references across merged namespace**

*Fix qualification of symbols from previous namespace blocks to support multiple merged namespace declarations in one file*

 * created by **dtscd**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2597#issuecomment-3807590715) **dtscd** said "@microsoft-github-policy-service agree company="Solid Core Data Inc""
 * [today](https://github.com/microsoft/TypeScript-go/pull/2597#issuecomment-3807635094) **jakebailey** said "Is this not just going away from microsoft/TypeScript#54500?"

### [Issue microsoft/TypeScript-go#2598](https://github.com/microsoft/TypeScript-go/issues/2598) (Closed, `Crash`, **iisaduan**)

**Auto\-imports broken in JS files when user preferences are used**

*Applying user preferences in JavaScript files causes auto-import suggestions to fail and trigger a panic in the TypeScript-Go server*

 * created by **DanielRosenwasser**
 * **DanielRosenwasser** added label `Crash`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2598#issuecomment-3808528734) **DanielRosenwasser** described reproducing a server crash by entering `PictureInPictureEvent` in vscode/gulpfile.mjs and hovering, which caused a nil pointer panic and segmentation fault stack trace
 * **DanielRosenwasser** assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2598#issuecomment-3809217241) **DanielRosenwasser** reported a panic error when opening in a Codespace environment related to auto imports
 * (today) **DanielRosenwasser** assigned to **Copilot**, **DanielRosenwasser**

### [Issue microsoft/TypeScript-go#2599](https://github.com/microsoft/TypeScript-go/issues/2599) (Closed, `bug`, **ahejlsberg**, **Copilot**)

**JSDoc for overloads and implementation is not displayed**

*VS Code TS Native Preview fails to show JSDoc for non-top overloads and implementation of overloaded TypeScript functions.*

 * created by **tats-u**
 * (today) **DanielRosenwasser** assigned to **Copilot**, **DanielRosenwasser**
 * [later](https://github.com/microsoft/TypeScript-go/issues/2599#issuecomment-3811719304) **ahejlsberg** explained that the changes to overload count display were intentional and compared how Strada and Corsa show overload information

### [PR microsoft/TypeScript-go#2600](https://github.com/microsoft/TypeScript-go/pull/2600) (Closed, **DanielRosenwasser**, **Copilot**)

**Fix race conditions in auto\-imports causing server crashes**

*Fix race conditions in auto-import handling by filtering nil project references and retrying completions without imports to prevent server crashes.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **DanielRosenwasser**

### [PR microsoft/TypeScript-go#2601](https://github.com/microsoft/TypeScript-go/pull/2601) (Open, **DanielRosenwasser**, **Copilot**)

**Display "\(\+N overload\)" suffix for function overloads in hover**

*Hover tooltips for TypeScript functions, methods, and constructors now include a (+N overload) suffix when additional overloads exist.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **DanielRosenwasser**

### [PR microsoft/TypeScript-go#2602](https://github.com/microsoft/TypeScript-go/pull/2602) (Open)

**feat: comprehensive Type Hierarchy LSP support**

*Adds comprehensive LSP-based Type Hierarchy support in TypeScript language service for navigating class, interface, and type alias supertypes and subtypes.*

 * created by **kbrilla**

### [Issue microsoft/TypeScript-go#961](https://github.com/microsoft/TypeScript-go/issues/961) (Open, `bug`, `Domain: Emit`, `Domain: Type Checking`, **jakebailey**)

**tsgo fails to resolve namespace symbols in non\-extends contexts across files**

*tsgo fails to qualify namespace symbols A and Afunc outside extends contexts across files, causing incorrect JS and runtime errors.*

 * (33 weeks ago) **jakebailey** added labels `Domain: Emit`, `Domain: Type Checking`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/issues/961#issuecomment-3806351229) **dtscd** reported encountering namespace assignment issue in a single file and asked if a PR to correct it would be accepted
 * [today](https://github.com/microsoft/TypeScript-go/issues/961#issuecomment-3807604637) **dtscd** mentioned sending PR #2597 that applied a small fix following tsgo's design to solve a real world problem for a large TypeScript project
 * [today](https://github.com/microsoft/TypeScript-go/issues/961#issuecomment-3807616138) **jakebailey** believed the intent in 6.0 and 7.0 was to not do that and linked related issue and PR
 * [today](https://github.com/microsoft/TypeScript-go/issues/961#issuecomment-3807692564) **dtscd** explained that the proposed change breaks cross-file namespaces and suggested carrying the tiny patch themselves, and asked for more nuanced same-file versus cross-file resolution behavior
 * [today](https://github.com/microsoft/TypeScript-go/issues/961#issuecomment-3807698758) **jakebailey** asked where the feature is used and noted deprecation of outFile and prepend
 * [today](https://github.com/microsoft/TypeScript-go/issues/961#issuecomment-3807733217) **dtscd** described migrating from tsc to tsgo and encountering an issue with namespace transformations and requested tsgo to emit an error when resolution succeeds but transformation fails
 * [today](https://github.com/microsoft/TypeScript-go/issues/961#issuecomment-3807741679) **jakebailey** noted that missing errors were the major concern, suggested reverting changes and discussing with the team
 * [today](https://github.com/microsoft/TypeScript-go/issues/961#issuecomment-3807742826) **jakebailey** said "The cross-file stuff is certainly pretty bad, and if we don't do that, doing it within a file only is already pretty strange."
 * [today](https://github.com/microsoft/TypeScript-go/issues/961#issuecomment-3808143225) **dtscd** said "I've been thinking about this. If you do bring this up, if namespaces aren't going to be supported even in the same file, then I would recommend you advertise ts6+ will drop them all together."
 * [today](https://github.com/microsoft/TypeScript-go/issues/961#issuecomment-3808150259) **jakebailey** said "If we do what we suggested, they're supported, but you can't just assume that you can write cross-namespace references unqualified, which requires type analysis to emit properly."
 * [today](https://github.com/microsoft/TypeScript-go/issues/961#issuecomment-3808167779) **dtscd** mentioned struggling to understand the use case for namespaces in TypeScript given file-based organization requiring re-annotation on refactor
 * [today](https://github.com/microsoft/TypeScript-go/issues/961#issuecomment-3808175525) **jakebailey** explained typical uses of namespaces and asked for clarification on re-annotating namespace decorations
 * [today](https://github.com/microsoft/TypeScript-go/issues/961#issuecomment-3808188925) **dtscd** described moving code between files under the same namespace and the extra annotation needed if namespaces no longer merged across files

