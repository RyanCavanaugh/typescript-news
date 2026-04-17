# Report for 2026-04-16 (Thursday, April 16th, 2026)

13 different users commented on 60 different issues.

## Recommended Actions

 * Response Recommended
    * @jeff-computers asked how to trigger a restart in [microsoft/TypeScript-go#3338](https://github.com/microsoft/TypeScript-go/issues/3338#issuecomment-4268557698)

## Activity Summary

### [PR microsoft/TypeScript-go#1099](https://github.com/microsoft/TypeScript-go/pull/1099) (Closed)

**Type width in error messages**

*Adjust the Go-based TypeScript compiler to format long type expressions on separate lines when they exceed 30 characters.*

 * created by **bjatkin**
 * [42 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1099#issuecomment-3009335200) **jakebailey** said "I'm going to mark this as a draft. I don't think we've accepted this feature, and the direction of new features like this needs to be from the TypeScript repo into this one."
 * [today](https://github.com/microsoft/TypeScript-go/pull/1099#issuecomment-4264857571) **jakebailey** said "Thanks, but I'm going to close this; we're not accepting this kind of change at this point, but we can discuss it on the main repo after 7.0."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#1550](https://github.com/microsoft/TypeScript-go/pull/1550) (Closed)

**Reduce string copies and allocations when emitting inlined sourcemaps**

*Optimize the emission of inlined sourcemaps by minimizing string copying and memory allocations.*

 * [35 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1550#issuecomment-3172290822) **dzbarsky** said "@microsoft-github-policy-service agre"
 * [35 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1550#issuecomment-3172291031) **dzbarsky** said "@microsoft-github-policy-service agree"
 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1550#issuecomment-4013304463) **jakebailey** clarified that the PR already used string concatenation for the sourceMappingURL in the WriteComment call
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#1770](https://github.com/microsoft/TypeScript-go/pull/1770) (Closed)

**Organize imports for TypeScript and JavaScript**

*Expose TypeScript and JavaScript import organizer via LSP command in VS Code, preserving blank lines and sorting imports*

 * [23 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1770#issuecomment-3493026664) **jakebailey** advised merging with main to check for duplicate helpers and suggested reusing the existing command name or using the when clause
 * [19 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1770#issuecomment-3606626496) **mkantor** asked whether microsoft/TypeScript#60431 still occurred with this implementation
 * [9 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1770#issuecomment-3872878146) **jakebailey** said "I think #2331 supersedes this?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/1770#issuecomment-4262157418) **jakebailey** said "This is an old PR; if anything, all that's left is a simple command, e.g. #3305."
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2115](https://github.com/microsoft/TypeScript-go/issues/2115) (Open, `possible improvement`)

**Refactor checker pool to limit checker creation for foreground tasks, segment diagnostic checkers**

*Refactor the checker pool to separate foreground and diagnostic tasks, minimizing redundant checker creation and resource usage*

 * (2 weeks ago) **RyanCavanaugh** added label `possible improvement`, and set milestone to `Possible Improvement`
 * (yesterday) **jakebailey** closed the issue
 * (today) **jakebailey** reopened the issue

### [PR microsoft/TypeScript-go#2151](https://github.com/microsoft/TypeScript-go/pull/2151) (Closed)

**fix error missing bug for referencing files are not existing**

*Add error handling for references to files that do not exist.*

 * created by **TranNhatHan**
 * [20 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2151#issuecomment-3576769662) **TranNhatHan** said "Is there any issue that causes the test to fail?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2151#issuecomment-4263008310) **jakebailey** said "Superseded by #3206"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2203](https://github.com/microsoft/TypeScript-go/pull/2203) (Closed, **jakebailey**, **Copilot**)

**Fix multiline ternary expression formatting with tabs**

*Ensure consistent tab-based indentation for multiline ternary expressions to prevent mixed tabs and spaces.*

 * **Copilot** assigned to **jakebailey**
 * [19 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2203#issuecomment-3609061306) **jakebailey** said "@copilot You forgot to run test/format/lint/etc"
 * [19 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2203#issuecomment-3609108881) **Copilot** fixed formatting, linting, and tests in commit a38bd7ab and confirmed all checks passed
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2251](https://github.com/microsoft/TypeScript-go/pull/2251) (Closed)

**  Fix: Add mutex protection for projects map to prevent race conditions**

*Add mutex-based read and write locking for the API projects map to prevent concurrent data races.*

 * [18 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2251#issuecomment-3619742802) **Catsayer-Chan** said " @microsoft-github-policy-service agree"
 * [18 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2251#issuecomment-3629402303) **jakebailey** said "Where are you using this API such that it matters for you? It's not guaranteed to work and I'm not sure we are expecting people to use it truly concurrently on the client side yet?"
 * [9 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2251#issuecomment-3880087810) **jakebailey** said "The API code has changed a lot since this PR was sent. Is this still needed?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2251#issuecomment-4262163982) **jakebailey** said "This is really behind and I haven't gotten a reply. I'm going to close this for housekeeping reasons."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2417](https://github.com/microsoft/TypeScript-go/pull/2417) (Open)

**Support \-\-pprofDir option with \-\-watch**

*Add --pprofDir support to the --watch mode to allow profiling of active processes.*

 * created by **tmm1**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2417#issuecomment-4264088120) **jakebailey** said "#1317 is closed and this PR is out of date; are you planning on updating it?"

### [PR microsoft/TypeScript-go#2419](https://github.com/microsoft/TypeScript-go/pull/2419) (Closed)

**Fix: Handle Negative VLQ Offsets in Source Maps for VSCode Jump to Definition**

*Clamp inverted ranges caused by negative VLQ offsets in source maps to restore correct VSCode jump to definition behavior.*

 * [14 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2419#issuecomment-3720619871) **jakebailey** said "We were all on vacation 🙂 "
 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2419#issuecomment-4014752158) **jakebailey** said "This PR needs to be updated after #3005 fixed a bug in this same code. @sethconvex are you willing to do it, or should I push to your PR?"
 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2419#issuecomment-4014846681) **sethconvex** mentioned that he would take a look next week
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2434](https://github.com/microsoft/TypeScript-go/pull/2434) (Closed)

**Experiment: Quantified Types**

*Seeking a TypeScript function signature to consume an array of heterogeneous Layer objects without collapsing distinct generics.*

 * [11 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2434#issuecomment-3794171335) **devanshj** suggested implementing `pipe` without existential types using finite overloads and provided example links
 * [11 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2434#issuecomment-3808239583) **clinuxrulz** observed that types weren't inferred in the chain and provided an infinite params example
 * [11 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2434#issuecomment-3812220747) **devanshj** acknowledged that the finite one infers the types and called the infinite example silly
 * [today](https://github.com/microsoft/TypeScript-go/pull/2434#issuecomment-4263139901) **RyanCavanaugh** said "Closing for housekeeping reasons (feature PRs, which should be for approved issues, would only happen post-7.0, which will be back in the TypeScript repo)"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#2533](https://github.com/microsoft/TypeScript-go/issues/2533) (Open, `bug`, `Domain: Declaration Emit`, **weswigham**)

**Multiple differences in declaration emit for CommonJS exports**

*TypeScript’s declaration emitter for CommonJS exports uses typeof module.exports, emits duplicate var declarations, and emits var instead of const.*

 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/2533#issuecomment-4247535574) **RyanCavanaugh** said "Confirmed all three still exist in nightly"
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/2533#issuecomment-4247896788) **ahejlsberg** noted support for multiple assignments to module.exports and exports.XXX and recommended emitting only the first occurrence to prevent duplicate declarations
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/2533#issuecomment-4247979575) **ahejlsberg** described other JS declaration emit issues, noting missing x and y properties in class C and duplicate namespace declarations for obj and f
 * [today](https://github.com/microsoft/TypeScript-go/issues/2533#issuecomment-4263797893) **weswigham** explained that the last two items were intentional to align with the reparsing strategy, outlined how to align with the old emit by duplicating binder work, and identified the first issue as a bug likely caused by overzealous node reuse

### [PR microsoft/TypeScript-go#2539](https://github.com/microsoft/TypeScript-go/pull/2539) (Closed)

**Add support for importing JSON modules "as const"**

*Enable an opt-in compiler option importJsonAsConst to import JSON modules with const semantics.*

 * created by **james-pre**
 * [12 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2539#issuecomment-3764651309) **james-pre** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2539#issuecomment-4263140568) **RyanCavanaugh** said "Closing for housekeeping reasons (feature PRs, which should be for approved issues, would only happen post-7.0, which will be back in the TypeScript repo)"
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#2597](https://github.com/microsoft/TypeScript-go/pull/2597) (Closed)

**internal/transformers/tstransformers: fix unqualified references across merged namespace**

*Fix qualification of symbols from previous namespace blocks to support multiple merged namespace declarations in one file*

 * created by **dtscd**
 * [11 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2597#issuecomment-3807590715) **dtscd** said "@microsoft-github-policy-service agree company="Solid Core Data Inc""
 * [11 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2597#issuecomment-3807635094) **jakebailey** said "Is this not just going away from microsoft/TypeScript#54500?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2597#issuecomment-4263010167) **jakebailey** said "I think this is actually already fixed now"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2629](https://github.com/microsoft/TypeScript-go/pull/2629) (Closed)

**Experiment: Distribute Control Flow**

*TypeScript fails to distribute union types when mapping over a discriminated union array and returning the same object*

 * created by **devanshj**
 * [9 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2629#issuecomment-3880082988) **jakebailey** said "I don't know that this is in scope: https://github.com/microsoft/typescript-go/blob/main/CONTRIBUTING.md#scope-of-acceptable-changes"
 * [9 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2629#issuecomment-3880240293) **devanshj** said "I see yeah that's okay this is anyway a throw away POC... I'm more interested in knowing the typescript team's thoughts on this idea than getting this merged :)"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2629#issuecomment-4263141993) **RyanCavanaugh** said "Closing for housekeeping reasons (feature PRs, which should be for approved issues, would only happen post-7.0, which will be back in the TypeScript repo)"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#2701](https://github.com/microsoft/TypeScript-go/issues/2701) (Closed)

**Declaration emit for named inferred types used in further inference inlines inferred types instead of naming them**

*tsgo inlines inferred types in declaration emit even when named, causing slower type checking in consuming packages.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2701#issuecomment-4154924127) **RyanCavanaugh** mentioned that Nightly now emitted the expected code snippet
 * (2 weeks ago) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/issues/2701#issuecomment-4259805234) **chriskrycho** checked notifications, began bumping to the latest nightly, and planned to switch the last package from tsc to tsgo after confirmation
 * [today](https://github.com/microsoft/TypeScript-go/issues/2701#issuecomment-4264417445) **chriskrycho** said "Update: #2459 also had some fixes that we need to go chase down before landing it, and I’m off till the 27th, but should land it early that week; will report back then!"

### [Issue microsoft/TypeScript-go#2780](https://github.com/microsoft/TypeScript-go/issues/2780) (Open, `Domain: Editor`, `Needs More Info`, **andrewbranch**)

**High memory consumption in a large pnpm monorepo**

*PR #2502 causes minor edits in a large pnpm monorepo to spike the TypeScript extension memory from ~700MB to ~35GB.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-4253201729) **andrewbranch** said "Yes, that's the only way I can make progress, unless I just happen to stumble upon the same root cause as your repro as I'm investigating other performance issues."
 * [today](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-4259962263) **AndreiTS** said "@andrewbranch I want to share a video and a private repo with this problem, where I can send you?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-4261231001) **andrewbranch** said "{firstname}.{lastname}@microsoft.com. Thanks!"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-4262619314) **andrewbranch** said "@AndreiTS I think the issue in your video is #3423."
 * [later](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-4267836701) **AndreiTS** confirmed that the issue matched #3423 and reported it was fixed in the new tsgo version with about 1.3 GiB RAM usage

### [PR microsoft/TypeScript-go#3084](https://github.com/microsoft/TypeScript-go/pull/3084) (Closed)

**Port LSP update imports on file rename support**

*Adds support to update import paths via LSP when files are renamed or moved to ensure correct relative references.*

 * [1 month ago](https://github.com/microsoft/TypeScript-go/pull/3084#issuecomment-4076493957) **jakebailey** explained that they avoid adding unit tests for this behavior and expected existing fourslash tests to be converted, since they cannot verify the ported tests otherwise
 * [1 month ago](https://github.com/microsoft/TypeScript-go/pull/3084#issuecomment-4086273176) **anchmelev** reworked the test conversion to use the converted fourslash path, added verify.getEditsForFileRename support, switched to generated tests for rename cases, fixed a parsing/conversion issue, and confirmed tests passed locally
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3084#issuecomment-4115238828) **anchmelev** requested another review after addressing earlier feedback by moving coverage to the converted fourslash path and porting getEditsForFileRename cases
 * [today](https://github.com/microsoft/TypeScript-go/pull/3084#issuecomment-4262143218) **jakebailey** said "This was superseded by #3358."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3171](https://github.com/microsoft/TypeScript-go/pull/3171) (Open, **ahejlsberg**, **RyanCavanaugh**, **Copilot**)

**Fix stack overflow in relater's skipCaching path for recursive tuple types**

*Add depth counters to prevent unbounded recursion and stack overflow in the relater skipCaching path for recursive tuple types.*

 * **Copilot** assigned to **RyanCavanaugh**
 * **RyanCavanaugh** assigned to **ahejlsberg**
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3171#issuecomment-4099158802) **RyanCavanaugh** said "@ahejlsberg this seems like two fixes when only one is needed, but I'm not sure which is preferable (or maybe there's a third option)"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3171#issuecomment-4264125280) **jakebailey** said "This doesn't seem right, it's just adding a random new depth limiter."

### [PR microsoft/TypeScript-go#3175](https://github.com/microsoft/TypeScript-go/pull/3175) (Open, **ahejlsberg**, **RyanCavanaugh**, **Copilot**)

**Fix template literal type exponential blowup in addSpans**

*Add growth limits in addSpans to prevent exponential template literal type expansion causing memory exhaustion.*

 * (3 weeks ago) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * **RyanCavanaugh** assigned to **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3175#issuecomment-4264113737) **jakebailey** said "This just adds in a new limit that Strada didn't have. I don't think this is right."

### [PR microsoft/TypeScript-go#3179](https://github.com/microsoft/TypeScript-go/pull/3179) (Closed)

**Fix issue \#3014 **

*In tsgo watch mode, an empty tsconfig files array prevented the initial build and TS18002 diagnostic, causing a silent hang.*

 * (3 weeks ago) **JaskiratAnand** closed the issue
 * (3 weeks ago) **JaskiratAnand** reopened the issue
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3179#issuecomment-4118771089) **JaskiratAnand** described fixing tsgo --watch hang on empty files array in tsconfig.json, added a regression test, and requested maintainers' review
 * [today](https://github.com/microsoft/TypeScript-go/pull/3179#issuecomment-4263452695) **jakebailey** said "Superseded by #3217"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3211](https://github.com/microsoft/TypeScript-go/pull/3211) (Closed)

**Fix typo in README definitions section**

*Correct the typo in the definitions section of the README.*

 * created by **colin99d**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3271](https://github.com/microsoft/TypeScript-go/pull/3271) (Open)

**Fix for a snapshot update with a nil CommandLine**

*Add a nil check in NewProjectResponse to prevent panics when handling projects with nil CommandLine during snapshot updates.*

 * created by **navya9singh**
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3271#issuecomment-4145607075) **andrewbranch** said "When does a project have a nil CommandLine?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3271#issuecomment-4263449950) **jakebailey** said "Is this handled by #3409? Or is this a different nil config problem?"

### [Issue microsoft/TypeScript-go#3338](https://github.com/microsoft/TypeScript-go/issues/3338) (Open, `possible improvement`, **mjbvz**)

**TSGO: command 'typescript\.restartTsServer' not found**

*Enabling the TypeScript native preview feature in VSCode 1.113.0 removes the 'typescript.restartTsServer' command.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/3338#issuecomment-4184835689) **jakebailey** pointed out that the provided command didn't restart the new language server and suggested hiding it when tsserver wasn't used
 * (2 days ago) **RyanCavanaugh** added label `possible improvement`, and set milestone to `Possible Improvement`
 * [later](https://github.com/microsoft/TypeScript-go/issues/3338#issuecomment-4268557698) **jeff-computers** said "@jakebailey thank you kindly - in the meantime how should we trigger a restart?"
 * [later](https://github.com/microsoft/TypeScript-go/issues/3338#issuecomment-4268631646) **sbetav** mentioned a specific command to restart the TypeScript Go server

### [PR microsoft/TypeScript-go#3352](https://github.com/microsoft/TypeScript-go/pull/3352) (Closed)

**Fix export default dts widening**

*Emit const _default assignments copying initializers for export defaults to more accurately reflect source behavior.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3355](https://github.com/microsoft/TypeScript-go/pull/3355) (Closed)

**Switch to new CI runner system**

*Adopt a new CI runner system to address current issues, leveraging its compatibility with our single-image pools.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3355#issuecomment-4195301938) **jakebailey** said "This won't work without a pool change (so far)"
 * [6 days ago](https://github.com/microsoft/TypeScript-go/pull/3355#issuecomment-4226977450) **jakebailey** said "This will fail until I can update the pool config, but I can't do that until nobody's running jobs, which sounds like a weekend merge."
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3355#issuecomment-4256396982) **azure-pipelines[bot]** reported that one pipeline was filtered out due to trigger conditions
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3392](https://github.com/microsoft/TypeScript-go/pull/3392) (Closed, `dependencies`, `github_actions`)

**Bump actions/upload\-artifact from 7\.0\.0 to 7\.0\.1 in the github\-actions group across 1 directory**

*Update actions/upload-artifact from version 7.0.0 to 7.0.1 in the GitHub Actions configuration*

 * (3 days ago) **dependabot[bot]** added labels `github_actions`, `dependencies`, `github_actions`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3396](https://github.com/microsoft/TypeScript-go/pull/3396) (Closed)

**Use methods for client cap resolution**

*Replace top-level functions with methods for client cap resolution to simplify implementation and shorten names.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3401](https://github.com/microsoft/TypeScript-go/pull/3401) (Open)

**Fix file counts, jsx in project telemetry**

*Update project telemetry to accurately categorize files by their declared type and ensure the JSX metric is reported as a string.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3401#issuecomment-4264189999) **DanielRosenwasser** asked which part of file counting this fix addressed
 * [today](https://github.com/microsoft/TypeScript-go/pull/3401#issuecomment-4264203781) **jakebailey** admitted that the change fixed nothing related to file counting and that he did not know what was wrong

### [PR microsoft/TypeScript-go#3412](https://github.com/microsoft/TypeScript-go/pull/3412) (Open)

**fix\(3410\): preserve type arguments in hover for qualified names**

*Qualified name hover tooltips now correctly display preserved type arguments.*

 * created by **a-tarasyuk**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3412#issuecomment-4261910421) **ahejlsberg** clarified that ExpressionWithTypeArguments is now parsed for instantiation expressions and can occur in regular expressions
 * [today](https://github.com/microsoft/TypeScript-go/pull/3412#issuecomment-4263833864) **weswigham** explained that type nodes only allow expressions at the end of a typeof query and illustrated with parsing examples

### [PR microsoft/TypeScript-go#3415](https://github.com/microsoft/TypeScript-go/pull/3415) (Closed)

**Add VS client caps, use VS diagnostic format when asked**

*Add support for Visual Studio client capabilities and enable Visual Studio diagnostic formatting on demand.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3415#issuecomment-4256417310) **azure-pipelines[bot]** reported that one pipeline was filtered out due to trigger conditions
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3415#issuecomment-4257460709) **jakebailey** said "/azp where"
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3415#issuecomment-4257461045) **azure-pipelines[bot]** notified that Azure DevOps orgs were getting events for this repository
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3416](https://github.com/microsoft/TypeScript-go/issues/3416) (Closed, `Domain: Editor`, **jakebailey**)

**isolatedDeclarations quickfix: Parens not added to single arrow func param**

*The isolatedDeclarations quickfix incorrectly adds type annotations to single arrow function parameters without parentheses, producing invalid syntax.*

 * (yesterday) **RyanCavanaugh** added label `Domain: Editor`, and assigned to **jakebailey**
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3416#issuecomment-4257561923) **jakebailey** reported that the bug was preexisting and provided a TS Playground link
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3417](https://github.com/microsoft/TypeScript-go/issues/3417) (Closed, `Domain: Editor`)

**Default type param not displayed in hover**

*Hover tooltip in tsgo extension omits default type parameter for generic types compared to TS6.0*

 * created by **Withered-Flower-0422**
 * **Withered-Flower-0422** added label `Domain: Editor`
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript-go#3418](https://github.com/microsoft/TypeScript-go/pull/3418) (Closed)

**Fix missing parens in ID fixes**

*Restore missing parentheses in ID fixes to correct related errors in both core and Strada.*

 * created by **jakebailey**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3418#issuecomment-4257595864) **azure-pipelines[bot]** reported that one pipeline was filtered out due to trigger conditions
 * (today) **jakebailey** closed the issue
 * (today) **jakebailey** reopened the issue
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3419](https://github.com/microsoft/TypeScript-go/pull/3419) (Closed)

**Avoid panicking on duplicate document close notifications**

*Prevent runtime panics by ignoring duplicate document close notifications from misbehaving clients.*

 * created by **Andarist**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3419#issuecomment-4264103337) **jakebailey** said "I feel iffy on this; this is probably one of the worst things a client can do and I'm not sure it's realistic?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3419#issuecomment-4264151385) **andrewbranch** argued that enforcing invariants improved internal consistency and aided bug detection, since permissive code makes finding future bugs harder
 * (later) **Andarist** closed the issue

### [PR microsoft/TypeScript-go#3420](https://github.com/microsoft/TypeScript-go/pull/3420) (Closed)

**Fix hover display of default type parameters**

*Ensure hover tooltips correctly display default type parameters in the TypeScript-Go extension*

 * created by **Andarist**
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript-go#3421](https://github.com/microsoft/TypeScript-go/pull/3421) (Closed)

**Fixed an issue with empty type argument lists not being reported on instantiation expressions**

*Compiler now detects and reports empty generic type argument lists in instantiation expressions.*

 * created by **Andarist**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3423](https://github.com/microsoft/TypeScript-go/issues/3423) (Closed, `Crash`)

**Memory usage spiked in version 7\.0\.0\-dev\.20260416\.1**

*Memory usage increased from about 1.1GB to 6GB after upgrading to version 7.0.0-dev.20260416.1*

 * [today](https://github.com/microsoft/TypeScript-go/issues/3423#issuecomment-4261450546) **sbking** provided two heap profile attachments for diffing
 * [today](https://github.com/microsoft/TypeScript-go/issues/3423#issuecomment-4261468808) **jakebailey** asked the user to try disabling semantic highlighting by setting editor.semanticHighlighting.enabled to false
 * [today](https://github.com/microsoft/TypeScript-go/issues/3423#issuecomment-4261499932) **sbking** provided a heap profile with the setting disabled
 * (today) **jakebailey** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/issues/3423#issuecomment-4262703657) **jakebailey** said "@sbking Can you try again with the version we just put out on the marketplace?"

### [PR microsoft/TypeScript-go#3425](https://github.com/microsoft/TypeScript-go/pull/3425) (Closed)

**Revert "Make LS checkers time out after being idle, segment based on use"**

*Revert recent LS checker idle-timeout and segmentation changes to resolve a suspected memory retention bug in the checker pool.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3426](https://github.com/microsoft/TypeScript-go/issues/3426) (Open, `bug`, **ahejlsberg**)

**tsc produces error, tsgo doesn't with sufficiently nested type**

*TypeScript 6 reports a nested type incompatibility between input and output APIs that tsgo overlooks until a layer is removed.*

 * created by **joshcartme**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3426#issuecomment-4262636150) **RyanCavanaugh** provided a minimal repro demonstrating that tsgo misses a structural assignability error under specific multi-hop import and array interface conditions
 * (today) **RyanCavanaugh** added label `bug`, and assigned to **ahejlsberg**, **Copilot**, **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3426#issuecomment-4262716834) **RyanCavanaugh** investigated and ruled out the issue as a manifestation of TypeScript issue #52912
 * (today) **RyanCavanaugh** unassigned **RyanCavanaugh**, **Copilot**

### [PR microsoft/TypeScript-go#3427](https://github.com/microsoft/TypeScript-go/pull/3427) (Open, **ahejlsberg**, **Copilot**)

**Fix isDeeplyNestedType false positive for concrete TypeReferences in multi\-checker mode**

*Use concrete type instances as recursion identities to eliminate false-positive type compatibility in tsgo’s multi-checker mode.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * (today) **RyanCavanaugh** assigned to **ahejlsberg**, and unassigned **RyanCavanaugh**

### [PR microsoft/TypeScript-go#3428](https://github.com/microsoft/TypeScript-go/pull/3428) (Open)

**Fix auto\-import log structure after deduplicating node\_modules package extractions**

*Restructure auto-import timing logs to accurately measure the full build work after deduplicating package extractions.*

 * created by **andrewbranch**

### [PR microsoft/TypeScript-go#3429](https://github.com/microsoft/TypeScript-go/pull/3429) (Closed)

**Ensure request cancel is always called**

*Always invoke cancellation functions from WithCancel and WithTimeout during complex request ordering*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3430](https://github.com/microsoft/TypeScript-go/pull/3430) (Open)

**Move @typescript/api and @typescript/ast into @typescript/native\-preview for publishing**

*Merge @typescript/api and @typescript/ast into @typescript/native-preview to prevent version mismatches and simplify publishing ahead of TypeScript 7.0.*

 * created by **andrewbranch**

### [PR microsoft/TypeScript-go#3431](https://github.com/microsoft/TypeScript-go/pull/3431) (Open)

**Exports aliases for CJS \`exports\.Foo = \.\.\.\` assignments when appropriate**

*Export alias symbols for CJS exports.Foo assignments on entity names or class expressions to preserve type and namespace semantics.*

 * created by **ahejlsberg**

### [PR microsoft/TypeScript-go#731](https://github.com/microsoft/TypeScript-go/pull/731) (Closed)

**Unify the way anonymous class symbols are printed in error messages**

*Use GetNameOfDeclaration and unify anonymous class labels to '(Anonymous class)' in error messages.*

 * [42 weeks ago](https://github.com/microsoft/TypeScript-go/pull/731#issuecomment-3003410042) **Andarist** said "Sure, I can port this to Strada"
 * [42 weeks ago](https://github.com/microsoft/TypeScript-go/pull/731#issuecomment-3003838072) **Andarist** created a PR porting the changes to Strada and reverted new tests here since they will come to Corsa after bumping the submodule
 * [42 weeks ago](https://github.com/microsoft/TypeScript-go/pull/731#issuecomment-3005411892) **jakebailey** said "I'd leave the tests here; it's fine for tests to be "duplicated" between the two temporarily. The names will not conflict."
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#988](https://github.com/microsoft/TypeScript-go/issues/988) (Closed, `Domain: Type Checking`, `Type Ordering`, `Domain: Performance`, **jakebailey**)

**tsgo "Type instantiation is excessively deep and possibly infinite" error when using react\-hook\-form**

*tsgo reports excessively deep type instantiation errors on two react-hook-form forms when spreading useForm into FormProvider, unlike tsc.*

 * **RyanCavanaugh** assigned to **jakebailey**
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/988#issuecomment-4158122110) **jakebailey** said "@justinsmid I haven't looked at this in a while; with #2459 merged it's possible this won't happen anymore. Have you used tsgo recently?"
 * **RyanCavanaugh** added to milestone `Possible Improvement`
 * [later](https://github.com/microsoft/TypeScript-go/issues/988#issuecomment-4267792358) **justinsmid** apologized for missing the comment, confirmed continued use of tsgo, reported the original error was resolved and memory usage normalized, noted occasional memory usage issues are tracked elsewhere, and suggested closing the issue
 * (later) **jakebailey** closed the issue

