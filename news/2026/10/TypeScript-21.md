# Report for 2026-10-21 (Wednesday, October 21st, 2026)

26 different users commented on 71 different issues.

## Recommended Actions

 * Response Recommended
    * @ThinkingPlanely asked why TypeScript doesn't infer the overloaded lambda type in [microsoft/TypeScript#47669](https://github.com/microsoft/TypeScript/issues/47669#issuecomment-6329323433)
    * @n-gist asked for suggestions on a better name for the proposed option in [microsoft/TypeScript#64235](https://github.com/microsoft/TypeScript/issues/64235#issuecomment-6339463401)
    * @YevheniiKotyrlo identified a port gap in unstable/ast and suggested adding pos++ after tokenValue = '#' in [microsoft/TypeScript#64490](https://github.com/microsoft/TypeScript/issues/64490#issuecomment-6337208238)
    * @insilications reported that the nightly extension only works when js/ts.tsdk.path is set to node_modules/typescript in [microsoft/TypeScript#64565](https://github.com/microsoft/TypeScript/issues/64565#issuecomment-6322494161)

## Activity Summary

### [Issue microsoft/TypeScript#32063](https://github.com/microsoft/TypeScript/issues/32063) (Open, `Suggestion`, `Awaiting More Feedback`)

**import ConstJson from '\./config\.json' as const;**

*Allow importing a JSON config file with a const modifier to infer literal union types for its values.*

 * [15 weeks ago](https://github.com/microsoft/TypeScript/issues/32063#issuecomment-4885857717) **Chinoman10** described how to use npm’s built-in dependency patching in v12 to apply a TypeScript patch and noted that Bun’s patch feature is faster
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/32063#issuecomment-6055145510) **michaelhazan** noted that TypeScript 7's go compiler prevented previous patching and asked why the feature wasn't part of TypeScript
 * [today](https://github.com/microsoft/TypeScript/issues/32063#issuecomment-6312789386) **jaydenfyi** recommended using .json5 via motherload after TS broke const.json support and provided a TS 7.1 content mapper workaround with a GitHub link
 * [today](https://github.com/microsoft/TypeScript/issues/32063#issuecomment-6328209063) **frolic** said "Looks like @colinhacks released a similar library: https://github.com/colinhacks/motherload"

### [Issue microsoft/TypeScript#47669](https://github.com/microsoft/TypeScript/issues/47669) (Open, `Suggestion`, `Needs Proposal`)

**proper overloading for arrow functions**

*Add explicit language support for overloading arrow functions to improve on current function-type intersection workarounds.*

 * [3.8 years ago](https://github.com/microsoft/TypeScript/issues/47669#issuecomment-1365612300) **DetachHead** said "imo the example in the OP is better because you don't have to duplicate the function name nor do you have to add types to the implementation signature"
 * [3.8 years ago](https://github.com/microsoft/TypeScript/issues/47669#issuecomment-1365973397) **erquhart** acknowledged that neither syntax is materially different and agreed that the suggested syntax is preferable
 * [2.7 years ago](https://github.com/microsoft/TypeScript/issues/47669#issuecomment-1879843520) **craigphicks** suggested using the same algorithm for arrow function overloads as function declarations and upgrading both with return value checking, illustrating with a TypeScript simulation
 * [today](https://github.com/microsoft/TypeScript/issues/47669#issuecomment-6329323433) **ThinkingPlanely** reported that TypeScript didn't infer the overloaded lambda type and asked why specifying the parameter type was necessary

### [PR microsoft/TypeScript#64106](https://github.com/microsoft/TypeScript/pull/64106) (Open, `For Backlog Bug`)

**fix\(58145\): suppress jsdoc for private members**

*Suppresses JSDoc comments for private members to prevent their documentation emission*

 * created by **a-tarasyuk**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [6 days ago](https://github.com/microsoft/TypeScript/pull/64106#issuecomment-6198196465) **jakebailey** said "I think that this looks good, but @weswigham might have some thoughts."
 * [today](https://github.com/microsoft/TypeScript/pull/64106#issuecomment-6326963631) **jakebailey** said "Unclear if this is something we should do post-beta"

### [PR microsoft/TypeScript#64174](https://github.com/microsoft/TypeScript/pull/64174) (Open, `Author: Team`, `For Milestone Bug`, **jakebailey**)

**Add wasip1 support, enabling CLI, API, browser, sync/async**

*Add experimental wasip1-based WebAssembly build of tsc enabling CLI, LSP, and sync/async API use in Node and browser environments.*

 * [5 weeks ago](https://github.com/microsoft/TypeScript/pull/64174#issuecomment-5703265395) **jakebailey** noted that content mappers didn’t exist when they began the work and admitted unfamiliarity with execing and using an existing tsconfig without node
 * [5 weeks ago](https://github.com/microsoft/TypeScript/pull/64174#issuecomment-5703651081) **NullVoxPopuli** expressed surprise at the globalThis.fs interface, asked about standards, and suggested passing fs access options or using a global mock fs
 * [5 weeks ago](https://github.com/microsoft/TypeScript/pull/64174#issuecomment-5704509646) **NullVoxPopuli** indicated that the feature worked somewhat and attached screenshots
 * [today](https://github.com/microsoft/TypeScript/pull/64174#issuecomment-6328669720) **jakebailey** announced readiness for review and that they had dropped the “tsc falls back to wasm” idea because Node’s WASI host did not work on Windows

### [Issue microsoft/TypeScript#64235](https://github.com/microsoft/TypeScript/issues/64235) (Open, `Suggestion`, `Domain: LS: Outlining`, `Experimentation Needed`, **gabritto**)

**Include terminating line in folding ranges when last token has no trailing non\-trivia**

*Propose enhancing lineFoldingOnly support by including closing-brace lines in folding ranges when the terminating line contains no non-trivia content.*

 * (5 weeks ago) **DanielRosenwasser** set milestone to `TypeScript 7.1.0 Beta`, assigned to **gabritto**, and unassigned **DanielRosenwasser**
 * [later](https://github.com/microsoft/TypeScript/issues/64235#issuecomment-6339137692) **n-gist** suggested rules for END pointer positioning for folding regions, argued consistency between including or excluding the closing delimiter is essential, and recommended using variant a)
 * [later](https://github.com/microsoft/TypeScript/issues/64235#issuecomment-6339463401) **n-gist** clarified the connection to a related PR, described two proposed language-server outlining options (`backOffForCode` and `backOffCoincided`), and suggested renaming `backOffForCode` to `backOffForPairedDelimiters` while soliciting better naming

### [Issue microsoft/TypeScript#64490](https://github.com/microsoft/TypeScript/issues/64490) (Closed, `Unactionable`)

**TypeScript 7\.0\.2 scanner does not advance on bare hash**

*TypeScript 7.0.2 scanner gets stuck on a bare '#' and repeatedly returns the same token without advancing.*

 * **RyanCavanaugh** added label `Unactionable`
 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/64490#issuecomment-5923007045) **typescript-automation[bot]** said "This issue has been marked as "Unactionable" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (3 weeks ago) **typescript-automation[bot]** closed the issue
 * [later](https://github.com/microsoft/TypeScript/issues/64490#issuecomment-6337208238) **YevheniiKotyrlo** described that the 6.0.3 and Go scanners advance past '#' when reporting an invalid-character diagnostic, identified a similar gap in the unstable/ast port, and suggested adding pos++ after tokenValue = '#' to fix the reproduction

### [Issue microsoft/TypeScript#64565](https://github.com/microsoft/TypeScript/issues/64565) (Open, `Needs Investigation`, **jakebailey**)

**TypeScript 7 VS Code extension: a workspace "typescript" 7\.x package is not detected, only "@typescript/native\-preview", which is no longer published**

*The TypeScript 7 VS Code extension fails to detect standard typescript@7 in workspace, using its bundled compiler instead.*

 * created by **leonidaz**
 * (2 weeks ago) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/issues/64565#issuecomment-6322494161) **insilications** said "It seems that using the nightly extension, TypeScriptTeam.vscode-typescript-nightly, is now only working if one sets "js/ts.tsdk.path": "node_modules/typescript""

### [Issue microsoft/TypeScript#64582](https://github.com/microsoft/TypeScript/issues/64582) (Closed, `Possible Improvement`)

**Info missing when hover on a proptery compare to TS6**

*TS7 hover on an index-signature property shows only its base type instead of the full index signature info from TS6.*

 * created by **Withered-Flower-0422**
 * (2 weeks ago) **RyanCavanaugh** added label `Possible Improvement`, and set milestone to `Backlog`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64586](https://github.com/microsoft/TypeScript/pull/64586) (Closed, `For Backlog Bug`)

**Restore index signature details in property hovers**

*Restore index signature details in TypeScript property hover tooltips to show key and value type information.*

 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64586#issuecomment-6154874697) **jakebailey** said "This PR needs a merge from main"
 * [today](https://github.com/microsoft/TypeScript/pull/64586#issuecomment-6314725767) **Andarist** said "@jakebailey done"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64695](https://github.com/microsoft/TypeScript/pull/64695) (Open, `For Milestone Bug`, **ahejlsberg**)

**\[experiment\] Skip incompatible discriminants when inferring**

*Experimentally skip incompatible discriminant properties during TypeScript union type inference to reduce workload and validate via tests.*

 * [2 days ago](https://github.com/microsoft/TypeScript/pull/64695#issuecomment-6269790663) **weswigham** noted a neutral to +8% performance impact, suggested caching discriminable item results or re-adding an optional prop fast path to improve performance, and asked for test cases demonstrating improved inference results, referencing a prior PR
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/64695#issuecomment-6270098644) **Andarist** mentioned having implemented the optional prop fast path locally and planning to push it and request a fresh rerun; noted having some test cases and intending to push them later this week; said they would review the linked PR and its tests
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/64695#issuecomment-6272440480) **jakebailey** said "I'd hope we can make the perf better still? I really hope to not make us slower if we can avoid it"
 * [later](https://github.com/microsoft/TypeScript/pull/64695#issuecomment-6335153206) **jakebailey** said "@typescript-bot test it"
 * [later](https://github.com/microsoft/TypeScript/pull/64695#issuecomment-6335154816) **typescript-automation[bot]** reported CI build statuses for test top400, user test this, run dt, and perf test this faster
 * [later](https://github.com/microsoft/TypeScript/pull/64695#issuecomment-6335636996) **typescript-automation[bot]** notified that DT test results were ready and unchanged
 * [later](https://github.com/microsoft/TypeScript/pull/64695#issuecomment-6335790620) **typescript-automation[bot]** reported tsc user test results and confirmed everything looked good
 * [later](https://github.com/microsoft/TypeScript/pull/64695#issuecomment-6335883827) **typescript-automation[bot]** reported the performance run results including metrics for errors, symbols, types, and memory usage
 * [later](https://github.com/microsoft/TypeScript/pull/64695#issuecomment-6336627044) **typescript-automation[bot]** reported that running the top 400 repos tsc comparison between baseline and pr succeeded without issues
 * [later](https://github.com/microsoft/TypeScript/pull/64695#issuecomment-6339601916) **jakebailey** said "@typescript-bot test it"
 * [later](https://github.com/microsoft/TypeScript/pull/64695#issuecomment-6339603645) **typescript-automation[bot]** reported CI jobs starting and completing with status links
 * [later](https://github.com/microsoft/TypeScript/pull/64695#issuecomment-6340024174) **typescript-automation[bot]** notified that the DT test results were ready and unchanged
 * [later](https://github.com/microsoft/TypeScript/pull/64695#issuecomment-6340156079) **typescript-automation[bot]** reported tsc user test results and confirmed everything looked good
 * [later](https://github.com/microsoft/TypeScript/pull/64695#issuecomment-6340173641) **typescript-automation[bot]** posted performance comparison results for the requested perf run
 * [later](https://github.com/microsoft/TypeScript/pull/64695#issuecomment-6341131824) **typescript-automation[bot]** reported that running the top 400 repos tsc comparison between baseline and pr succeeded without issues

### [Issue microsoft/TypeScript#64740](https://github.com/microsoft/TypeScript/issues/64740) (Open, `Needs Investigation`, **andrewbranch**)

**\[API\] \`ConditionalType\` has no counterpart to \`root\` of TypeScript 6 \(the node it was declared with\)**

*TypeScript 7's ConditionalType API lacks a counterpart to the TS6 root property, preventing retrieval of the original conditional type declaration node.*

 * created by **MARCROCK22**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **andrewbranch**

### [PR microsoft/TypeScript#64765](https://github.com/microsoft/TypeScript/pull/64765) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Resolve class and interface members through shared layouts**

*Introduce shared member layouts and lazy resolution for class and interface instantiations to significantly reduce memory usage and symbol creation.*

 * [6 days ago](https://github.com/microsoft/TypeScript/pull/64765#issuecomment-6187296535) **typescript-automation[bot]** reported starting the perf test job and provided status and result links
 * [6 days ago](https://github.com/microsoft/TypeScript/pull/64765#issuecomment-6187748114) **typescript-automation[bot]** provided performance run results for tsc comparing baseline to PR
 * [5 days ago](https://github.com/microsoft/TypeScript/pull/64765#issuecomment-6226103984) **jakebailey** said "Drafting, I think Anders is redoing this"
 * [today](https://github.com/microsoft/TypeScript/pull/64765#issuecomment-6329169034) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/64765#issuecomment-6329170294) **typescript-automation[bot]** reported that perf test jobs started and shared links to status and results
 * [today](https://github.com/microsoft/TypeScript/pull/64765#issuecomment-6329797206) **typescript-automation[bot]** provided the performance run results as requested

### [Issue microsoft/TypeScript#64810](https://github.com/microsoft/TypeScript/issues/64810) (Closed)

**Native LSP watcher shutdown races subscription publication and panics on a nil map**

*A race between LSP watcher shutdown and subscription registration in typescript-go causes a nil map panic.*

 * created by **vizanto**
 * [today](https://github.com/microsoft/TypeScript/issues/64810#issuecomment-6320872400) **RyanCavanaugh** mentioned that the issue was fixed in microsoft/typescript-go#4845
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#64812](https://github.com/microsoft/TypeScript/issues/64812) (Open, `Bug`, `Domain: Declaration Emit`)

**Declaration emit cannot name an exported \`unique symbol\` property key unless the file already imports it**

*Declaration emit cannot name an exported unique symbol property key unless the file already imports it, causing TS4023 errors.*

 * created by **sindresorhus**
 * (today) **RyanCavanaugh** added labels `Bug`, `Domain: Declaration Emit`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#64813](https://github.com/microsoft/TypeScript/issues/64813) (Open, `Bug`, `Crash`, `Domain: check: Control Flow`)

**Crash: \`Unhandled case in resolveStructuredTypeMembers\` when switching on an evolving \`\[\]\` array inside a loop**

*TypeScript compiler crashes with Unhandled case in resolveStructuredTypeMembers when switching on [] array in infinite loop.*

 * created by **YuanchengJiang**
 * (today) **RyanCavanaugh** added labels `Bug`, `Crash`, `Domain: check: Control Flow`, and set milestone to `Backlog`

### [PR microsoft/TypeScript#64814](https://github.com/microsoft/TypeScript/pull/64814) (Open, `For Backlog Bug`)

**Finalize evolving array types before narrowing in switch clauses**

*Ensure evolving array types are finalized before type narrowing occurs in switch clauses*

 * created by **Andarist**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (today) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`

### [Issue microsoft/TypeScript#64820](https://github.com/microsoft/TypeScript/issues/64820) (Open, `Bug`, `Domain: LS: Auto-import`)

**Changing importModuleSpecifier or importModuleSpecifierEnding does not update auto\-import specifiers in open files**

*Changing importModuleSpecifier or importModuleSpecifierEnding preferences does not update auto-import suggestions in already open files until they are reopened.*

 * created by **lsh4711**
 * [6 days ago](https://github.com/microsoft/TypeScript/issues/64820#issuecomment-6196983488) **nepyil** said "حلو"
 * [6 days ago](https://github.com/microsoft/TypeScript/issues/64820#issuecomment-6197000177) **nepyil** posted the word 'نييل'
 * (today) **RyanCavanaugh** added labels `Bug`, `Domain: LS: Auto-import`, and set milestone to `Backlog`

### [PR microsoft/TypeScript#64821](https://github.com/microsoft/TypeScript/pull/64821) (Open, `For Backlog Bug`)

**Clear auto\-import specifier cache when module specifier preferences change**

*Clear auto-import specifier cache on any module specifier preference change to ensure updated import suggestions for open files.*

 * [6 days ago](https://github.com/microsoft/TypeScript/pull/64821#issuecomment-6201876867) **RyanCavanaugh** challenged the claim that the cache was only cleared on preference changes and requested checking relevant preference values before clearing the cache
 * [6 days ago](https://github.com/microsoft/TypeScript/pull/64821#issuecomment-6202441973) **lsh4711** changed cache clearing to only trigger when ModuleSpecifierPreferences changed, added an Equal method to UserPreferences and added a unit test for it
 * [today](https://github.com/microsoft/TypeScript/pull/64821#issuecomment-6314482381) **lsh4711** asked whether to wait for the PR to land or open the follow-up as a stacked PR
 * (today) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`

### [Issue microsoft/TypeScript#64824](https://github.com/microsoft/TypeScript/issues/64824) (Open, `Bug`, **johnfav03**)

**\[api\] createSnapshot panics opening a project that extends into a circular extends chain**

*createSnapshot panics when opening a second TypeScript project that extends into a circular configuration chain*

 * created by **cplieger**
 * (today) **RyanCavanaugh** added labels `Needs Human Review`, `Bug`, removed label `Needs Human Review`, set milestone to `TypeScript 7.1.1 RC`, and assigned to **johnfav03**

### [PR microsoft/TypeScript#64825](https://github.com/microsoft/TypeScript/pull/64825) (Open, `For Milestone Bug`, **johnfav03**)

**\[api\] Reparse extended configs cached under another resolution stack**

*Extended config cache wrongly reuses entries from circular tsconfig chains, causing snapshot panics or hangs without proper resolution stack context.*

 * created by **cplieger**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (today) **typescript-automation[bot]** added label `For Milestone Bug`, removed label `For Uncommitted Bug`, and assigned to **johnfav03**

### [Issue microsoft/TypeScript#64828](https://github.com/microsoft/TypeScript/issues/64828) (Open, `Needs Investigation`, **andrewbranch**)

**Content mappers: go\-to\-definition on an module specifier returns nothing when the target file has more than one span\-map segment**

*Go-to-definition on module specifiers no longer finds .gts files containing multiple span-map segments after content mapper updates.*

 * **RyanCavanaugh** assigned to **andrewbranch**
 * **andrewbranch** added to milestone `TypeScript 7.1.1 RC`
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/64828#issuecomment-6276004130) **NullVoxPopuli-ai-agent** provided a minimal reproduction without Ember or Glint, corrected the trigger to export-from statements, and showed span-mapping outputs across TypeScript versions
 * [today](https://github.com/microsoft/TypeScript/issues/64828#issuecomment-6328616011) **colinhacks** reported that non-relative import specifiers also broke go to definition under TS 7.1.0-beta and provided repro steps

### [Issue microsoft/TypeScript#64838](https://github.com/microsoft/TypeScript/issues/64838) (Open, `Bug`, `Domain: tsc -b`, `Domain: tsc: --incremental`)

**Incremental \`tsc \-\-build\` reports a different result from a clean build after a change to \`package\.json\` dependencies**

*Changing package.json dependencies can cause incremental tsc --build runs to produce stale outputs and erroneous diagnostics compared to clean builds.*

 * created by **jasonkuhrt**
 * [6 days ago](https://github.com/microsoft/TypeScript/issues/64838#issuecomment-6208916296) **jackeddisciple** said "Hey , I would like to investigate on this issue. I’ll work on a fix and submit a PR."
 * (today) **RyanCavanaugh** added labels `Bug`, `Domain: tsc -b`, `Domain: tsc: --incremental`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#64848](https://github.com/microsoft/TypeScript/issues/64848) (Open, `Domain: Performance`, `Possible Improvement`)

**TypeScript 7\.1 regression: quadratic root scanning in settled no\-op builds**

*TypeScript 7.1 regression causes no-op build performance degradation by quadratically scanning roots during up-to-date checks*

 * created by **turadg**
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/64848#issuecomment-6277974971) **sunny-kavixo** thanked the previous commenter and stated an intention to independently verify the regression and share any findings
 * (today) **RyanCavanaugh** added labels `Possible Improvement`, `Domain: Performance`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#64852](https://github.com/microsoft/TypeScript/issues/64852) (Open, `Possible Improvement`)

**Support Jujutsu conflict markers**

*Add parsing support for Jujutsu's custom conflict marker syntax to prevent spurious TypeScript errors*

 * created by **rf-**
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/64852#issuecomment-6278616021) **jakebailey** said "I think we can just do the simple version and it would probably be sufficient."
 * (today) **RyanCavanaugh** added label `Possible Improvement`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#64855](https://github.com/microsoft/TypeScript/issues/64855) (Closed, `Design Limitation`)

**"This expression is not callable\." false positive on union of generic functions where the call is valid for all types in the union**

*TypeScript reports a false "not callable" error when calling a union of compatible generic functions.*

 * [3 days ago](https://github.com/microsoft/TypeScript/issues/64855#issuecomment-6251795447) **jcalz** described known limitation of union call signatures allowing at most one overloaded and one generic member and noted that two generic members prevent unification
 * **RyanCavanaugh** added label `Design Limitation`
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/64855#issuecomment-6275255340) **RyanCavanaugh** explained that there was no sound and performant fix, that the signature reduction rule didn’t apply, and that they wouldn’t add iterative mechanics due to potential exponential checking complexity
 * [today](https://github.com/microsoft/TypeScript/issues/64855#issuecomment-6330385080) **typescript-automation[bot]** said "This issue has been marked as "Design Limitation" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-automation[bot]** closed the issue

### [Issue microsoft/TypeScript#64859](https://github.com/microsoft/TypeScript/issues/64859) (Open, `Bug`, **andrewbranch**, **RyanCavanaugh**, **Copilot**)

**\[API\] Printer attaches source comments to synthesized nodes because the node encoder sends pos \-1 as 0**

*TypeScript’s sync API printer wrongly attaches existing source comments to synthesized nodes when their negative positions are clamped to zero.*

 * created by **Smrtnyk**
 * (today) **RyanCavanaugh** added label `Bug`, set milestone to `TypeScript 7.1.1 RC`, and assigned to **andrewbranch**, **Copilot**, **RyanCavanaugh**

### [Issue microsoft/TypeScript#64860](https://github.com/microsoft/TypeScript/issues/64860) (Open, `Needs Investigation`, **andrewbranch**)

**\[api\] Add back missing: factory\.createUniqueName / createTempVariable \(generated identifiers\)**

*Add createUniqueName, createTempVariable, and related generated identifier functions to TypeScript’s AST factory to restore automatic collision-free name generation.*

 * created by **Smrtnyk**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **andrewbranch**

### [Issue microsoft/TypeScript#64861](https://github.com/microsoft/TypeScript/issues/64861) (Open, `Needs Investigation`, **andrewbranch**)

**\[api\] No replacement for ts\.transform / TransformationContext / custom transformers in program\.emit**

*Requesting custom transformer support in TypeScript 7's native emit API or guidance on a long-term transform-and-emit workflow.*

 * created by **Smrtnyk**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **andrewbranch**

### [Issue microsoft/TypeScript#64862](https://github.com/microsoft/TypeScript/issues/64862) (Open, `Bug`)

**TS7 LSP: every didOpen rebuilds and deletes a non\-matching referenced project**

*TypeScript 7's LSP rebuilds every referenced project on didOpen and deletes non-matching ones before selecting the correct project.*

 * created by **Kiborgik**
 * (today) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#64863](https://github.com/microsoft/TypeScript/issues/64863) (Open, `Bug`, **weswigham**, **RyanCavanaugh**, **Copilot**)

**Panic in \`getSignaturesOfType\` on a decorator's contextual type in JS API**

*Calling checker.getSignaturesOfType on a decorator expression’s contextual type in the TypeScript JS API triggers a Go runtime panic due to a nil pointer dereference*

 * created by **auvred**
 * (today) **RyanCavanaugh** added label `Bug`, set milestone to `TypeScript 7.1.1 RC`, and assigned to **weswigham**, **Copilot**, **RyanCavanaugh**

### [Issue microsoft/TypeScript#64875](https://github.com/microsoft/TypeScript/issues/64875) (Open, `Bug`, `Crash`, `Domain: tsc: --incremental`)

**Incremental compile panics on a failed output write, or never retries it**

*TypeScript incremental compilation panics on failed file writes when declarations are enabled and never retries writes otherwise.*

 * [2 days ago](https://github.com/microsoft/TypeScript/issues/64875#issuecomment-6277364909) **YevheniiKotyrlo** said "Love it! Thank You @sunny-kavixo!"
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/64875#issuecomment-6277558110) **sunny-kavixo** thanked @YevheniiKotyrlo and reported reproducing both behaviors, said they were working on a minimal fix and regression tests, and promised to share an update once validated
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/64875#issuecomment-6283506910) **sunny-kavixo** completed a focused fix for issue #64875 addressing nil-pointer panic and output-write retries, passed regression and validation tests, and requested a maintainer to triage the associated issue and add it to the Backlog milestone
 * (today) **RyanCavanaugh** added labels `Bug`, `Crash`, `Domain: tsc: --incremental`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#64882](https://github.com/microsoft/TypeScript/issues/64882) (Open, `Bug`, **RyanCavanaugh**, **gabritto**, **Copilot**)

**7\.1 regression: import resolving to a non\-module file falls back to a pattern ambient module instead of TS2306**

*TypeScript 7.1 incorrectly applies a pattern ambient module for imports resolving to non-module files instead of reporting TS2306.*

 * created by **harshmandan**
 * (today) **RyanCavanaugh** added label `Bug`, and assigned to **gabritto**, **Copilot**, **RyanCavanaugh**

### [Issue microsoft/TypeScript#64883](https://github.com/microsoft/TypeScript/issues/64883) (Open, `Bug`, `Domain: Parser`)

**Escaped \`in\` / \`instanceof\` after a class field initializer is parsed as a binary operator instead of a new member**

*TypeScript treats Unicode-escaped identifiers matching 'in' and 'instanceof' after class field initializers as binary operators, triggering errors.*

 * created by **JLHwung**
 * (today) **RyanCavanaugh** added labels `Bug`, `Domain: Parser`, and set milestone to `Backlog`

### [PR microsoft/TypeScript#64885](https://github.com/microsoft/TypeScript/pull/64885) (Open, `For Backlog Bug`)

**fix\(64883\): fix asi before escaped keyword class members**

*Adjust automatic semicolon insertion behavior to correctly handle escaped keyword names in class members.*

 * (yesterday) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64885#issuecomment-6300646990) **jakebailey** demonstrated a hang on tests using unicode escape sequences in TypeScript files
 * (today) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`

### [Issue microsoft/TypeScript#64889](https://github.com/microsoft/TypeScript/issues/64889) (Open, `Bug`)

**\`emitDecoratorMetadata\` emits a ReferenceError for a default \`import type\` from an unresolvable module**

*emitDecoratorMetadata erroneously emits runtime code for a default type-only import from an unresolvable module, causing a ReferenceError.*

 * created by **blickly**
 * [today](https://github.com/microsoft/TypeScript/issues/64889#issuecomment-6311453284) **damerlanaga99-source** provided a VS Code debugging configuration snippet
 * (today) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#64891](https://github.com/microsoft/TypeScript/issues/64891) (Open, `Needs Investigation`, **ahejlsberg**)

**7\.1 regression: declaration order of recursive generic interfaces changes assignability \(TS2322\)**

*TypeScript 7.1 regression causes erroneous TS2322 when assigning DS<{total:M},string> to DS<Record<string,M>,string> due to declaration order change.*

 * created by **chrisolszewski**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/64891#issuecomment-6307221109) **shahinsamiur** described investigating the problem and developing a solution to the variance calculation implementation changes, and said they would provide updates or a PR when ready
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **ahejlsberg**

### [Issue microsoft/TypeScript#64892](https://github.com/microsoft/TypeScript/issues/64892) (Open, `Needs Investigation`, **ahejlsberg**)

**\[7\.1 Regression\] Unexpected behaviour change from Stronger Distributive Type checks**

*Upgrading to TypeScript 7.1 introduces stricter distributive checks causing TS2345 errors in generic callback methods.*

 * created by **hkleungai**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **ahejlsberg**

### [Issue microsoft/TypeScript#64895](https://github.com/microsoft/TypeScript/issues/64895) (Open, `Bug`)

**panic: Unhandled case in Node\.MemberList: KindVariableDeclarationList on merged namespace/enum element access**

*TypeScript 7.0.2 panics with an unhandled KindVariableDeclarationList error when accessing a namespace-exported constant in an enum.*

 * created by **muh-syaipullah**
 * [today](https://github.com/microsoft/TypeScript/issues/64895#issuecomment-6311271344) **Andarist** said "this is already being fixed by https://github.com/microsoft/TypeScript/pull/64746"
 * **RyanCavanaugh** added label `Bug`

### [PR microsoft/TypeScript#64896](https://github.com/microsoft/TypeScript/pull/64896) (Open, `For Backlog Bug`)

**Recognize unresolved type\-only default imports during alias lookup**

*Ensure alias lookup correctly identifies unresolved type-only default imports.*

 * created by **Andarist**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (today) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`

### [Issue microsoft/TypeScript#64897](https://github.com/microsoft/TypeScript/issues/64897) (Closed)

**tsc \-b no\-op build ~5x slower in 7\.1\.0\-beta \(isContentMapperSupplementalBuildInfoPath scans every root per file\)**

*TypeScript 7.1.0-beta's tsc -b no-op builds are five times slower because isContentMapperSupplementalBuildInfoPath scans every root for each file*

 * created by **todor-a**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64898](https://github.com/microsoft/TypeScript/pull/64898) (Closed, `For Uncommitted Bug`)

**fix: avoid repeated root scans in no\-op builds**

*Eliminates redundant root file scanning in no-op builds to significantly improve build performance.*

 * created by **a-tarasyuk**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#64899](https://github.com/microsoft/TypeScript/issues/64899) (Open, `Bug`)

**JSDocTypeLiteral\.jsdocPropertyTags returns only the first tag**

*JSDocTypeLiteral.jsdocPropertyTags accessor in TypeScript v7 erroneously returns only the first property tag instead of all tags.*

 * created by **mourner**
 * (today) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`

### [PR microsoft/TypeScript#64903](https://github.com/microsoft/TypeScript/pull/64903) (Open, `Author: Team`, `For Uncommitted Bug`, **RyanCavanaugh**, **Copilot**)

**Preserve synthesized node ranges across API serialization**

*Preserve synthesized node ranges across API serialization and deserialization to prevent source comment misplacement.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Milestone Bug`, `For Milestone Bug`, `For Uncommitted Bug`, and removed label `For Milestone Bug`

### [PR microsoft/TypeScript#64904](https://github.com/microsoft/TypeScript/pull/64904) (Open, `Author: Team`, `For Uncommitted Bug`, **RyanCavanaugh**, **Copilot**)

**Prevent panic when serializing decorator contextual signatures**

*Prevent serialization panic by omitting synthetic decorator signatures lacking source files from API responses while preserving internal checker data.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `Author: Team`, `Author: Team`, `For Milestone Bug`, `For Milestone Bug`, `For Uncommitted Bug`, and removed label `For Milestone Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64904#issuecomment-6323771495) **weswigham** suggested investigating the source of synthetic signature declarations in the checker and making them less synthetic for API serialization
 * [today](https://github.com/microsoft/TypeScript/pull/64904#issuecomment-6324576232) **Copilot** reworked synthetic call-signature declarations to use a shared virtual AST, added tests, and confirmed validation passed
 * [today](https://github.com/microsoft/TypeScript/pull/64904#issuecomment-6326380379) **weswigham** asked @andrewbranch how they felt about the approach

### [PR microsoft/TypeScript#64905](https://github.com/microsoft/TypeScript/pull/64905) (Open, `Author: Team`, `For Uncommitted Bug`, **RyanCavanaugh**, **Copilot**)

**Restore TS2306 for resolved non\-module files matching ambient patterns**

*Restore TS2306 error reporting for script imports incorrectly matched to ambient wildcard modules due to import-attribute support regression.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `Author: Team`, `Author: Team`, `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64905#issuecomment-6323418549) **Andarist** said "@RyanCavanaugh there is already an approved PR for this here: https://github.com/microsoft/TypeScript/pull/64884"

### [PR microsoft/TypeScript#64906](https://github.com/microsoft/TypeScript/pull/64906) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Add tests for check order dependence**

*Add tests that expose and document order-dependent behaviors in checks to ensure consistency.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#64907](https://github.com/microsoft/TypeScript/pull/64907) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Add extra tests for various uncovered parts of the code**

*Add tests for untested code behaviors identified during a recent code review session*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#64908](https://github.com/microsoft/TypeScript/pull/64908) (Open, `For Uncommitted Bug`)

**Improve diagnostic for automatic JSX in script files**

*Script files using automatic JSX now produce TS2884 errors with export {} guidance and updated regression tests.*

 * created by **gabrielvfonseca**
 * (today) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64908#issuecomment-6323178096) **microsoft-github-policy-service[bot]** prompted user to agree to the Contributor License Agreement by replying with a specific command
 * [today](https://github.com/microsoft/TypeScript/pull/64908#issuecomment-6323178137) **microsoft-github-policy-service[bot]** prompted user to agree to the Contributor License Agreement by replying with a specific command

### [PR microsoft/TypeScript#64909](https://github.com/microsoft/TypeScript/pull/64909) (Closed, `Author: Team`, `For Uncommitted Bug`, **johnfav03**)

**Reload cached files for \`Created\` watch events**

*Ensure files replaced by atomic saves trigger cache invalidation on Created events to prevent stale diagnostics.*

 * created by **johnfav03**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **johnfav03**

### [PR microsoft/TypeScript#64910](https://github.com/microsoft/TypeScript/pull/64910) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Avoid unnecessary localization branch rebases**

*Prevent rebasing the localization branch when its files are unchanged to avoid unnecessary commits and review churn.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [Issue microsoft/TypeScript#64911](https://github.com/microsoft/TypeScript/issues/64911) (Open)

**API: \`snapshot\.update\` with both \`removePrograms\` and \`createPrograms\` crashes tsgo \(nil dereference in \`ProjectCollectionBuilder\.HandleAPIRequest\`\)**

*Using snapshot.update with both removePrograms and createPrograms causes a nil dereference panic in the TypeScript sync API*

 * created by **johnnyreilly**

### [Issue microsoft/TypeScript#64912](https://github.com/microsoft/TypeScript/issues/64912) (Open)

**Content mappers: pass an import's query or attributes to \`transform\`**

*Allow content mappers to opt in to receiving import query parameters or import attributes in their transform calls to handle module variants.*

 * created by **colinhacks**

### [PR microsoft/TypeScript#64913](https://github.com/microsoft/TypeScript/pull/64913) (Open, `For Backlog Bug`)

**Fix raw AST child list access**

*Fix raw AST child list access for JSDocTypeLiteral property tags by encoding them with NodeList traversal and adding regression tests*

 * created by **icecold009**
 * **typescript-automation[bot]** added label `For Backlog Bug`

### [PR microsoft/TypeScript#64914](https://github.com/microsoft/TypeScript/pull/64914) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Cherry\-pick PR 64276 to release\-7\.0**

*Apply PR 64276 to the release-7.0 branch to prevent the unstable 7.0 API from logging 'context cancelled' on exit.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#64915](https://github.com/microsoft/TypeScript/pull/64915) (Closed, `Author: Team`, `For Uncommitted Bug`, **ahejlsberg**)

**Lazy member resolution for class and interface types**

*Add lazy member resolution to classes and interfaces using shared member layouts and improved tuple numeric and length sorting.*

 * created by **ahejlsberg**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript/pull/64915#issuecomment-6327080393) **ahejlsberg** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/64915#issuecomment-6327154737) **ahejlsberg** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/64915#issuecomment-6327156444) **typescript-automation[bot]** posted an automated CI status update listing build commands, statuses, and result links
 * [today](https://github.com/microsoft/TypeScript/pull/64915#issuecomment-6327568687) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/64915#issuecomment-6327570324) **typescript-automation[bot]** reported that builds started and provided status links
 * [today](https://github.com/microsoft/TypeScript/pull/64915#issuecomment-6327606596) **typescript-automation[bot]** notified that DT test results were ready and unchanged
 * [today](https://github.com/microsoft/TypeScript/pull/64915#issuecomment-6327661704) **typescript-automation[bot]** provided tsc user test results and indicated everything looked good
 * [today](https://github.com/microsoft/TypeScript/pull/64915#issuecomment-6328054207) **typescript-automation[bot]** said "@jakebailey, the perf run you requested failed. You can check the log here."
 * [today](https://github.com/microsoft/TypeScript/pull/64915#issuecomment-6328126101) **jakebailey** explained that failure was caused by a runtime nil pointer dereference panic in the TypeScript checker
 * [today](https://github.com/microsoft/TypeScript/pull/64915#issuecomment-6328437771) **typescript-automation[bot]** reported build results comparing baseline and PR on top 400 repos, highlighting new compilation errors in reactive-resume
 * [today](https://github.com/microsoft/TypeScript/pull/64915#issuecomment-6328633546) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/64915#issuecomment-6328634784) **typescript-automation[bot]** reported starting the perf test build and linked to the build results
 * [today](https://github.com/microsoft/TypeScript/pull/64915#issuecomment-6328661469) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/64915#issuecomment-6328662673) **typescript-automation[bot]** started the perf test job and provided status and result links
 * [today](https://github.com/microsoft/TypeScript/pull/64915#issuecomment-6329080526) **typescript-automation[bot]** posted the requested perf run results with detailed comparison metrics

### [PR microsoft/TypeScript#64916](https://github.com/microsoft/TypeScript/pull/64916) (Open, `For Uncommitted Bug`)

**Make symbol tables insertion\-ordered**

*Use insertion-ordered symbol tables to eliminate nondeterministic iteration and ensure consistent diagnostics, declaration emissions, and type ID assignments.*

 * created by **dimitropoulos**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64916#issuecomment-6328731460) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [today](https://github.com/microsoft/TypeScript/pull/64916#issuecomment-6328820662) **jakebailey** said "I saw this before and am curious; is all of the benefit actually from the small slice for small tables? Or is the ordering even a concern here?"
 * [today](https://github.com/microsoft/TypeScript/pull/64916#issuecomment-6328839798) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/64916#issuecomment-6328841414) **typescript-automation[bot]** announced CI jobs starting and provided links to the build and results
 * [today](https://github.com/microsoft/TypeScript/pull/64916#issuecomment-6328962016) **dimitropoulos** described that non-deterministic IDs in --generateTrace runs complicated comparisons, suggested making them deterministic, and observed Strada exhibited similar behavior prompting the PR
 * [today](https://github.com/microsoft/TypeScript/pull/64916#issuecomment-6328987094) **jakebailey** proposed adding a lint rule to ban map iteration without explicit opt-ins to ensure independence from symbol table ordering
 * [today](https://github.com/microsoft/TypeScript/pull/64916#issuecomment-6329431244) **typescript-automation[bot]** provided performance run results to @jakebailey
 * [today](https://github.com/microsoft/TypeScript/pull/64916#issuecomment-6329564110) **jakebailey** said "Seems like this causes nondeterminism in the tests, note the concurrent and race tests (which use multi-checker programs) erroring."
 * [later](https://github.com/microsoft/TypeScript/pull/64916#issuecomment-6335492219) **Andarist** clarified that the performance and memory benefit came from the representation rather than ordering; explained testing fixes using @singleThreaded for nondeterminism; noted plans for further ordering fixes

### [Issue microsoft/TypeScript#64917](https://github.com/microsoft/TypeScript/issues/64917) (Open)

**"Content mapper file extension '\.const\.json' is a built\-in extension and cannot be registered by a content mapper\." error is misleading**

*Error message incorrectly labels .const.json as a built-in extension instead of clarifying its conflict with .json or supporting .const.json patterns*

 * created by **DetachHead**

### [PR microsoft/TypeScript#64918](https://github.com/microsoft/TypeScript/pull/64918) (Open, `For Backlog Bug`)

**Fix unique symbol declaration emit imports**

*Automatically generate aliased type-only imports for exported unique symbols to avoid declaration emit errors with computed properties.*

 * created by **WorthOnGit**
 * **typescript-automation[bot]** added label `For Backlog Bug`

### [Issue microsoft/TypeScript#64919](https://github.com/microsoft/TypeScript/issues/64919) (Open)

**API: parameter documentation \(getDocumentationComment / getJsDocTags\) diverges from the classic services in TypeScript 7\.1**

*TypeScript 7.1’s programmatic API getDocumentationComment and getJsDocTags for parameters no longer return inherited JSDoc comments as the classic services did.*

 * created by **WinterYukky**

### [Issue microsoft/TypeScript#64920](https://github.com/microsoft/TypeScript/issues/64920) (Open)

**\[7\.1 API\] Equivalent of \`BuilderProgram\.getAllDependencies\` / batched module resolution**

*Request addition of a Program API for retrieving transitive file dependencies or batched module resolutions in TypeScript 7.1.*

 * created by **nicojs**

### [PR microsoft/TypeScript#64921](https://github.com/microsoft/TypeScript/pull/64921) (Open, `For Uncommitted Bug`)

**Clarify error when content mapper extension ends in a built\-in extension**

*Change TS18066 diagnostic to clarify that content mapper extensions ending in built-in extensions are disallowed.*

 * created by **govardhanchinta99**
 * (later) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/64921#issuecomment-6339608951) **govardhanchinta99** said "@microsoft-github-policy-service agree"

### [PR microsoft/TypeScript#64922](https://github.com/microsoft/TypeScript/pull/64922) (Open, `For Uncommitted Bug`)

**Emit the files of each checker in a deterministic order**

*Ensure each checker emits its files in a consistent, deterministic order to eliminate non-determinism.*

 * created by **Andarist**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/64922#issuecomment-6343818376) **jakebailey** said "@typescript-bot perf test this faster"
 * [later](https://github.com/microsoft/TypeScript/pull/64922#issuecomment-6343820685) **typescript-automation[bot]** announced that the perf test job started and provided links to build status and results
 * [later](https://github.com/microsoft/TypeScript/pull/64922#issuecomment-6344528856) **typescript-automation[bot]** reported the requested performance run results

### [Issue microsoft/TypeScript#64923](https://github.com/microsoft/TypeScript/issues/64923) (Open, **dbaeumer**)

**Support workspace specific typescript version**

*Allow the extension to use a workspace-specific TypeScript version rather than a global one.*

 * [1 week ago](https://github.com/microsoft/TypeScript/issues/64923#issuecomment-6340576842) **dbaeumer** said "@RyanCavanaugh any reason why you moved this to VS Code? The new TS7 extension handles this setting. VS Code by default doesn't expand variables in settings."
 * [today](https://github.com/microsoft/TypeScript/issues/64923#issuecomment-6340576951) **vs-code-engineering[bot]** closed the issue after it lacked the requested information for 7 days
 * (today) **vs-code-engineering[bot]** closed the issue
 * (later) **dbaeumer** reopened the issue
 * [later](https://github.com/microsoft/TypeScript/issues/64923#issuecomment-6340577060) **dbaeumer** said "Moving back to TS since I have not heard from @RyanCavanaugh "

### [PR microsoft/TypeScript#64924](https://github.com/microsoft/TypeScript/pull/64924) (Open, `For Uncommitted Bug`)

**Reuse this\-independent interface member instantiations**

*Reuse instantiations of interface members that don’t depend on `this` to avoid redundant allocations.*

 * created by **777genius**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/64924#issuecomment-6341176161) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (later) **typescript-automation[bot]** added labels `For Backlog Bug`, `For Uncommitted Bug`, and removed labels `For Uncommitted Bug`, `For Backlog Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/64924#issuecomment-6341312406) **777genius** said "@microsoft-github-policy-service agree"
 * [later](https://github.com/microsoft/TypeScript/pull/64924#issuecomment-6344056899) **jakebailey** said "Are there any real world codebases that hit this? Note how none of our benchmarks were affected by that other PR"

### [Issue microsoft/TypeScript#64925](https://github.com/microsoft/TypeScript/issues/64925) (Open)

**Excess synthetic\-this member allocations in nongeneric mapped interface inheritance**

*The TypeScript compiler performs excessive synthetic 'this' member instantiations for nongeneric mapped interface inheritance, leading to unnecessary allocations.*

 * created by **777genius**

