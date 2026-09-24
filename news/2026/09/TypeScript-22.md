# Report for 2026-09-22 (Tuesday, September 22nd, 2026)

19 different users commented on 58 different issues.

## Recommended Actions

 * Response Recommended
    * @guillaume-mueller requested an option to disable rewriting ts extensions in [microsoft/TypeScript#61050](https://github.com/microsoft/TypeScript/issues/61050#issuecomment-5780504005)
    * @unrevised6419 provided repro steps and examples in [microsoft/TypeScript#63960](https://github.com/microsoft/TypeScript/issues/63960#issuecomment-5795427296)
    * @leonidaz provided verification results as requested in [microsoft/TypeScript#64351](https://github.com/microsoft/TypeScript/issues/64351#issuecomment-5779864254)
    * @typescript-automation[bot] provided automated build comparison results and requested review in [microsoft/TypeScript#64372](https://github.com/microsoft/TypeScript/pull/64372#issuecomment-5787027455)
    * @typescript-automation[bot] provided requested perf run results in [microsoft/TypeScript#64388](https://github.com/microsoft/TypeScript/pull/64388#issuecomment-5780363579)
    * @lotexiu provided the actual code context as requested in [microsoft/TypeScript#64398](https://github.com/microsoft/TypeScript/issues/64398#issuecomment-5795007816)
    * @lotexiu asked how to properly prevent this type issue in [microsoft/TypeScript#64398](https://github.com/microsoft/TypeScript/issues/64398#issuecomment-5795490682)
    * @rexdotsh offered a fix and requested verification and milestone assignment before filing a PR in [microsoft/TypeScript#64405](https://github.com/microsoft/TypeScript/issues/64405#issuecomment-5793012334)

## Activity Summary

### [Issue microsoft/TypeScript#59047](https://github.com/microsoft/TypeScript/issues/59047) (Closed, `Bug`, `Needs More Info`, `Domain: Crashes`, **iisaduan**)

**TS Server fatal error:  Maximum call stack size exceeded**

*TS Server crashes with maximum call stack size exceeded error when opening a file containing syntax errors in VS Code*

 * (4 days ago) **RyanCavanaugh** added labels `Needs Human Review`, `Needs More Info`
 * [yesterday](https://github.com/microsoft/TypeScript/issues/59047#issuecomment-5762226464) **yunxu1019** said "你在这几个溢出的函数外添加个临时的递归计数器，超过一定的域值输出当前节点就可以了吧。我在最近的版本的vscode上已经无法复现了，打开以后语法引擎只是不停地转圈，不会再崩溃了。"
 * [today](https://github.com/microsoft/TypeScript/issues/59047#issuecomment-5780263287) **RyanCavanaugh** said "I don't think this still repros. Please log a new issue with sufficient information if you're still seeing it. Thanks!"
 * (today) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#59920](https://github.com/microsoft/TypeScript/issues/59920) (Closed, `Bug`, `Domain: JavaScript`, **jakebailey**)

**function object parameter destructure field without default value will be ignored**

*After upgrading to TypeScript 5.6, function parameter destructuring with defaulted properties ignores non-default fields, causing unknown property errors.*

 * [1.9 years ago](https://github.com/microsoft/TypeScript/issues/59920#issuecomment-2379478733) **ahejlsberg** explained that the issue pertained to type inference from code with errors, noted the root cause was a longstanding difference between array and object destructuring defaults, and indicated no strong reason to change the behavior
 * **RyanCavanaugh** added label `Domain: JavaScript`
 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/59920#issuecomment-5432044798) **jakebailey** described attempting a Copilot-based fix but rejecting it for special-casing JS and opted to try Anders' suggestion instead
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#61050](https://github.com/microsoft/TypeScript/issues/61050) (Open, `Suggestion`, `Awaiting More Feedback`)

**Alternative to rewriteRelativeImportExtensions & allowImportingTsExtensions**

*Propose a generic compiler feature to rewrite .ts import paths to .js as an alternative to rewriteRelativeImportExtensions or allowImportingTsExtensions.*

 * (1.6 years ago) **RyanCavanaugh** added labels `Suggestion`, `Awaiting More Feedback`
 * [1.5 years ago](https://github.com/microsoft/TypeScript/issues/61050#issuecomment-2715620973) **BretHudson** expressed enthusiasm and described discovering the new flag’s interaction with allowImportingTsExtensions, noting annoyance at VSCode importing modules without the .js extension
 * [today](https://github.com/microsoft/TypeScript/issues/61050#issuecomment-5780504005) **guillaume-mueller** requested an option to disable ts extension rewriting to avoid injecting __rewriteRelativeImportExtensions

### [Issue microsoft/TypeScript#61892](https://github.com/microsoft/TypeScript/issues/61892) (Open, `Bug`, `Help Wanted`, `Domain: flag: isolatedDeclarations`)

**Preserve computed property in \`\-\-isolatedDeclarations\` emit**

*Update TypeScript’s --isolatedDeclarations flag to emit computed property declarations in .d.ts files without errors.*

 * [52 weeks ago](https://github.com/microsoft/TypeScript/issues/61892#issuecomment-3313726069) **teague2** shared a Branded mixin implementation and code example to dynamically create classes and address issues with isolatedDeclarations
 * [52 weeks ago](https://github.com/microsoft/TypeScript/issues/61892#issuecomment-3314178111) **bradzacher** suggested using a #private property as a brand and explained that true private properties make a class nominal, enabling a `this.#brand === config.brand` check
 * **RyanCavanaugh** added label `Domain: Isolated Declarations`
 * [later](https://github.com/microsoft/TypeScript/issues/61892#issuecomment-5797356825) **chriskrycho** noted that constructor assignment didn’t work with private fields or the phantom type pattern

### [Issue microsoft/TypeScript#63603](https://github.com/microsoft/TypeScript/issues/63603) (Closed, `Bug`, `Domain: LS: Completion Lists`)

**Issue: TypeScript autocomplete for template literal types ignores user's Quote Style preference**

*Autocomplete suggestions for template literal type keys always use double quotes, ignoring the user's configured quote style preference.*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [10 weeks ago](https://github.com/microsoft/TypeScript/issues/63603#issuecomment-4977767143) **cooperbuilds** analyzed the hover implementation, identified that only one declaration's JSDoc is used, and asked if a PR to use merged documentation would be welcome
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/63603#issuecomment-5662383909) **anbv29** asked to work on the issue
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#63960](https://github.com/microsoft/TypeScript/issues/63960) (Open, `Needs More Info`)

**TS 7\.0\.2 \(tsgo\): augmentation of a type\-only re\-exported interface resolves order\-dependently — same file set passes via explicit include list, fails via directory glob**

*TypeScript 7.0.2's directory-glob file input causes it to ignore augmentations on type-only re-exported interfaces, unlike explicit include lists.*

 * created by **DoodleBears**
 * [1 month ago](https://github.com/microsoft/TypeScript/issues/63960#issuecomment-5416706267) **RyanCavanaugh** explained inability to reproduce the issue using a synthetic test case and requested the full program snapshot with tsconfig variants
 * **RyanCavanaugh** added label `Needs More Info`
 * [later](https://github.com/microsoft/TypeScript/issues/63960#issuecomment-5795427296) **unrevised6419** explained that module augmentation created a new Register interface overriding the original and provided videos and a reproduction repo demonstrating the issue

### [PR microsoft/TypeScript#63987](https://github.com/microsoft/TypeScript/pull/63987) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Redo localization for onboarding**

*Reorganize localization files and pipeline to match loc team expectations and automate diagnostics exports and translation sync via PRs.*

 * [4 days ago](https://github.com/microsoft/TypeScript/pull/63987#issuecomment-5736824989) **DanielRosenwasser** mentioned adding support for localizing the VS Code extension strings, modeled after other Microsoft extensions' repos, and cc'd TylerLeonhardt
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/63987#issuecomment-5736854965) **DanielRosenwasser** said "Just to recap other convos we've had with @iisaduan and Tyler, the plan was that will be ship as a built-in extension for VS Code, so I just want to make sure we're doing the right thing."
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/63987#issuecomment-5736936820) **jakebailey** mentioned the need to submit localization files to the loc team, commit them for VSIX publishing, and have VS Code adjust outputs for special builds
 * [today](https://github.com/microsoft/TypeScript/pull/63987#issuecomment-5783691884) **jakebailey** referred to Tyler’s guidance that marketplace extensions should include localizations and approved the PR
 * [today](https://github.com/microsoft/TypeScript/pull/63987#issuecomment-5784502727) **jakebailey** said "Okay, I removed the vscode stuff, since that's still in the air."

### [PR microsoft/TypeScript#64043](https://github.com/microsoft/TypeScript/pull/64043) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Align object binding defaults with arrays**

*Implement consistent default value handling in object destructuring to match array bindings*

 * (3 weeks ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#64089](https://github.com/microsoft/TypeScript/issues/64089) (Closed, `Needs Investigation`, **andrewbranch**)

**FSEvents watcher drops events when requested casing differs from disk casing**

*The macOS FSEvents watcher drops events when requested path casing differs from disk casing because WatchManager lowercases paths.*

 * created by **andrewbranch**
 * (2 weeks ago) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **andrewbranch**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64153](https://github.com/microsoft/TypeScript/pull/64153) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Ban case blocks with just "break", top level break**

*Ban Go case blocks containing only a break statement and remove any redundant top-level break statements.*

 * (2 weeks ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64158](https://github.com/microsoft/TypeScript/pull/64158) (Open, `Author: Team`, `For Uncommitted Bug`, **iisaduan**)

**Build Orchestrator API **

*Implement a BuildOrchestrator API to programmatically build, clean, and manage project references in TypeScript 7.1 without watch mode.*

 * [4 days ago](https://github.com/microsoft/TypeScript/pull/64158#issuecomment-5729268673) **dragomirtitian** explained their usage of the incremental program APIs and workflow, including creating an incremental compiler host, caching ASTs, invoking diagnostics, and emitting changed files
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/64158#issuecomment-5732995165) **andrewbranch** described how declaration file AST caching now works automatically via strategic program snapshots, referenced Jake’s prototype commit, and mentioned developing a snapshot-backed incremental program prototype for future testing
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64158#issuecomment-5766275697) **dragomirtitian** acknowledged automatic parse cache behavior, noted uncertainty about its reliability, and expressed eagerness to try the upcoming prototype
 * [today](https://github.com/microsoft/TypeScript/pull/64158#issuecomment-5786468443) **andrewbranch** said "@dragomirtitian I have a draft up at https://github.com/microsoft/TypeScript/pull/64401; it probably has some bugs, but can you see if that direction meets your needs?"

### [PR microsoft/TypeScript#64204](https://github.com/microsoft/TypeScript/pull/64204) (Closed, `Author: Team`, `For Milestone Bug`, **andrewbranch**)

**Replace \`api\.updateSnapshot\`**

*Refactor snapshot API by removing api.updateSnapshot and introducing createSnapshot, getCurrentLanguageServerSnapshot, and snapshot.update operations.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/64204#issuecomment-5766425880) **andrewbranch** said "Hm, I've investigated, but I can't reproduce that. Can you get Claude to generate a contained repro, or even repro instructions tied to a specific commit of your PR?"
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64204#issuecomment-5771867307) **johnnyreilly** wondered if the issue only surfaced on Windows, noted that Claude had reproduced it, and linked the Windows failure
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64204#issuecomment-5771872346) **johnnyreilly** provided a minimal ts-loader/webpack-free repro with instructions that reproduces the issue only on Windows
 * [today](https://github.com/microsoft/TypeScript/pull/64204#issuecomment-5784252672) **andrewbranch** mentioned inadvertently fixing the issue with PR #64391 due to drive letter lowercasing affecting case-sensitive file lookups
 * [today](https://github.com/microsoft/TypeScript/pull/64204#issuecomment-5789729944) **johnnyreilly** said "Oh nice! I'll try and test with the latest nightly today and report back "
 * [later](https://github.com/microsoft/TypeScript/pull/64204#issuecomment-5791438694) **johnnyreilly** said "Your diagnosis is correct - I see C going in and c coming out. Maybe we should be handling it better on our side"
 * [later](https://github.com/microsoft/TypeScript/pull/64204#issuecomment-5792047627) **johnnyreilly** moved ts-loader to use normalized filenames for previousSnapshot.update and createSnapshot, resolving the problem and removing the workaround

### [PR microsoft/TypeScript#64210](https://github.com/microsoft/TypeScript/pull/64210) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Fix case sensitivity fswatch and users**

*Normalize macOS fsevents paths and store both canonical and original paths to ensure accurate file watcher matching.*

 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64210#issuecomment-5691848244) **jakebailey** said "This is nasty, I'm going to try and simplify it, but I think it can only be simpler by doing less precise tracking..."
 * [6 days ago](https://github.com/microsoft/TypeScript/pull/64210#issuecomment-5702061437) **jakebailey** said "It doesn't save much code to simplify it, with much worse downsides, sadly."
 * [6 days ago](https://github.com/microsoft/TypeScript/pull/64210#issuecomment-5702140819) **jakebailey** said "The FS overlay stuff very much conflicted, so, I have to figure that out"
 * [today](https://github.com/microsoft/TypeScript/pull/64210#issuecomment-5784324759) **jakebailey** split the PR into separate commits addressing three issues: casing difference (#64089), an overlay bug, and symlink invalidation (#64351)
 * [today](https://github.com/microsoft/TypeScript/pull/64210#issuecomment-5784704604) **jakebailey** said "I'm going to not bother with 3 as I don't think any normal client would do that, but for 4-8, that depends on this PR, so I'll send that later."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64220](https://github.com/microsoft/TypeScript/pull/64220) (Closed, `For Milestone Bug`, **johnfav03**)

**Schedule tsc \-b projects by dependency depth to reduce builder idle time on upstream projects**

*Sort topologically built TypeScript projects by dependency depth rather than references-first to reduce builder idle time and speed up large monorepo builds.*

 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64220#issuecomment-5686328009) **typescript-automation[bot]** posted performance run results for tsc comparing baseline to pr
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/64220#issuecomment-5749572773) **Freakazo** tested the branch on a large monorepo and observed performance gains (median 38.24s to 28.39s) with increased memory usage (~5.4GB to ~6.9GB), and noted most benchmarks don’t use the -b flag
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64220#issuecomment-5766071230) **jakebailey** clarified that only the xstate benchmark used -b, where the optimization had the biggest impact
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#64222](https://github.com/microsoft/TypeScript/issues/64222) (Closed, `Needs Investigation`, **johnfav03**)

**tsc \-b: builders idle on upstream projects because projects are scheduled in depth\-first reference order**

*The build orchestrator's depth-first scheduling of project references in tsc -b leads to builder idle time and slower parallel builds.*

 * (1 week ago) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `Backlog`, and assigned to **johnfav03**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64348](https://github.com/microsoft/TypeScript/pull/64348) (Closed, `For Uncommitted Bug`)

**LEGO: Pull request from lego/hb\_5378966c\-b857\-470a\-8675\-daebef4a6da1\_20260919100320174 to main**

*Automated pull request adding localized lcls updates from branch lego/hb_5378966c-b857-470a-8675-daebef4a6da1_20260919100320174 to main.*

 * created by **csigs**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#64350](https://github.com/microsoft/TypeScript/issues/64350) (Closed, `Needs Investigation`, **andrewbranch**)

**Content mappers: composite projects report TS6307 for supplemental virtual outputs**

*Composite projects using content mappers emitting supplemental files fail TS6307 because those outputs aren’t included in the project file list.*

 * created by **leonidaz**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **andrewbranch**

### [Issue microsoft/TypeScript#64351](https://github.com/microsoft/TypeScript/issues/64351) (Open, `Bug`, **jakebailey**)

**tsc \-\-watch never recompiles on macOS since 7\.1\.0\-dev\.20260811\.1**

*On macOS with TypeScript 7.1.0-dev.20260811.1 and later nightly builds, tsc --watch stops detecting file changes and never recompiles.*

 * created by **leonidaz**
 * [today](https://github.com/microsoft/TypeScript/issues/64351#issuecomment-5772532438) **jakebailey** said "Can you try #64210 just to see?"
 * [today](https://github.com/microsoft/TypeScript/issues/64351#issuecomment-5779864254) **leonidaz** verified that PR #64210 fixed the watch regression and provided detailed local test results
 * [today](https://github.com/microsoft/TypeScript/issues/64351#issuecomment-5784637279) **jakebailey** said "Thanks. I'm scoping #64210 specifically down to the other issue, but I should be able to send a different Pr to fix this one."
 * (today) **RyanCavanaugh** added label `Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#64359](https://github.com/microsoft/TypeScript/pull/64359) (Closed, `For Backlog Bug`)

**Respect quote preference for object property completions**

*Respect user quote style preferences for non-identifier property completions in object literals.*

 * created by **yksr-melt**
 * (3 days ago) **typescript-automation[bot]** added labels `For Backlog Bug`, `For Backlog Bug`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64361](https://github.com/microsoft/TypeScript/pull/64361) (Closed, `For Uncommitted Bug`)

**LEGO: Pull request from lego/hb\_5378966c\-b857\-470a\-8675\-daebef4a6da1\_20260920092305213 to main**

*Merge localized lcls updates from branch lego/hb_5378966c-b857-470a-8675-daebef4a6da1_20260920092305213 into main.*

 * created by **csigs**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#64368](https://github.com/microsoft/TypeScript/issues/64368) (Open, `Needs Investigation`, **andrewbranch**)

**Content mapper: allowing document highlight result from other language\-servers**

*Propose returning null instead of empty arrays for content-mapper document highlight results to enable fallback from other language servers.*

 * created by **jasonlyu123**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **andrewbranch**

### [PR microsoft/TypeScript#64369](https://github.com/microsoft/TypeScript/pull/64369) (Closed, `For Uncommitted Bug`)

**LEGO: Pull request from lego/hb\_5378966c\-b857\-470a\-8675\-daebef4a6da1\_20260921092356953 to main**

*Merge updated localized LCL strings from lego/hb_5378966c-b857-470a-8675-daebef4a6da1 branch into main.*

 * created by **csigs**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64372](https://github.com/microsoft/TypeScript/pull/64372) (Open, `Author: Team`, `For Milestone Bug`, **ahejlsberg**)

**Restore idempotency to \`resolveObjectTypeMembers\`**

*Reestablish idempotent resolveObjectTypeMembers by blocking eager base class type argument resolution and improving circular type instantiation errors.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/64372#issuecomment-5765261701) **ahejlsberg** said "Trying tests again..."
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64372#issuecomment-5765610733) **typescript-automation[bot]** reported test results comparing main to the pull request merge, noted two unrelated infrastructure failures, and confirmed that everything else looked good
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64372#issuecomment-5766063918) **typescript-automation[bot]** reported tsc comparison results for the top 400 repos and highlighted build failures in stablyai/orca
 * [today](https://github.com/microsoft/TypeScript/pull/64372#issuecomment-5784006093) **ahejlsberg** said "@typescript-bot test top1000"
 * [today](https://github.com/microsoft/TypeScript/pull/64372#issuecomment-5784007411) **typescript-automation[bot]** started CI build for test top1000
 * [today](https://github.com/microsoft/TypeScript/pull/64372#issuecomment-5785660564) **ahejlsberg** said "@typescript-bot test top1000"
 * [today](https://github.com/microsoft/TypeScript/pull/64372#issuecomment-5785661549) **typescript-automation[bot]** reported that the test top1000 job had started with status and results links
 * [today](https://github.com/microsoft/TypeScript/pull/64372#issuecomment-5787027455) **typescript-automation[bot]** reported automated build comparison results across the top 1000 repos and noted an interesting change

### [PR microsoft/TypeScript#64376](https://github.com/microsoft/TypeScript/pull/64376) (Open, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Negated Types: Change the meaning of \`{}\` to \`unknown & not null & not undefined\`**

*Redefine {} as non-null unknown instead of unknown, null, or undefined and enhance type-origin tracking for literal unions.*

 * (yesterday) **weswigham** reopened the issue
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64376#issuecomment-5765206099) **weswigham** said "@typescript-bot test top1000"
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64376#issuecomment-5765207254) **typescript-automation[bot]** said "Hey @weswigham, this PR changed while I was preparing the test run. Please try again."
 * [today](https://github.com/microsoft/TypeScript/pull/64376#issuecomment-5781570769) **weswigham** said "@typescript-bot test top1000"
 * [today](https://github.com/microsoft/TypeScript/pull/64376#issuecomment-5781572035) **typescript-automation[bot]** announced that jobs had started and test top1000 build had begun with updates to follow

### [Issue microsoft/TypeScript#64378](https://github.com/microsoft/TypeScript/issues/64378) (Open, `Possible Improvement`)

**Performance: exponential check time as a chain of generic calls grows \(index signature in the inferred spec type\)**

*A string index signature in a generic command spec type causes exponentially slower TypeScript checks for long call chains.*

 * created by **alan-albuquerque**
 * (today) **RyanCavanaugh** added label `Possible Improvement`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/64378#issuecomment-5780416195) **RyanCavanaugh** said "@ahejlsberg maybe worth looking at"

### [PR microsoft/TypeScript#64381](https://github.com/microsoft/TypeScript/pull/64381) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Move enum generator into tools scripts**

*Relocate the enum generator from the Herebyfile into the scripts directory alongside other TypeScript code generators.*

 * (yesterday) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64383](https://github.com/microsoft/TypeScript/pull/64383) (Closed, `For Uncommitted Bug`)

**LEGO: Pull request from lego/hb\_5378966c\-b857\-470a\-8675\-daebef4a6da1\_20260922092326260 to main**

*Merge localized LCL files from LEGO branch hb_5378966c-b857-470a-8675-daebef4a6da1_20260922092326260 into main.*

 * created by **csigs**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#64384](https://github.com/microsoft/TypeScript/issues/64384) (Open, `Bug`)

**Panic in \`TupleNormalizer\.normalize\` \(nil \`currentNode\`\) when declaration emit resolves an oversized tuple type under \`\-\-noCheck\`**

*Under --noCheck declaration emit, resolving an oversized recursive tuple type triggers a nil pointer dereference panic in TupleNormalizer.normalize.*

 * created by **YuanchengJiang**
 * (today) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`

### [PR microsoft/TypeScript#64385](https://github.com/microsoft/TypeScript/pull/64385) (Open, `For Backlog Bug`)

**Fix panic when declaration emit resolves an oversized tuple type**

*Declaration-only mode panics with a nil pointer when resolving tuple types exceeding size limits.*

 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64385#issuecomment-5778789346) **jakebailey** suggested that the user had not run npm install recently
 * [today](https://github.com/microsoft/TypeScript/pull/64385#issuecomment-5779242206) **mohit-nayak** acknowledged that node_modules was stale, ran npm ci, confirmed formatting and tests passed, and updated the checklist
 * [today](https://github.com/microsoft/TypeScript/pull/64385#issuecomment-5779986625) **jakebailey** asked whether test cases could be provided to trigger the other cases
 * [today](https://github.com/microsoft/TypeScript/pull/64385#issuecomment-5780467087) **mohit-nayak** provided repros for six additional scenarios showing silent diagnostics and assertion failures under various type-checking paths
 * (today) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64385#issuecomment-5787625510) **jakebailey** said "@weswigham Do you have any thoughts about this?"
 * [today](https://github.com/microsoft/TypeScript/pull/64385#issuecomment-5788183773) **weswigham** identified potential instability in the currentNode error-reporting mechanism under arbitrary entrypoints and suggested reporting diagnostics on the type symbol's declaration to remove currentNode dependence

### [Issue microsoft/TypeScript#64386](https://github.com/microsoft/TypeScript/issues/64386) (Open, `Needs Investigation`, **johnfav03**)

**\`\-\-incremental\` retains stale diagnostics when augmenting a re\-exported interface**

*TypeScript incremental builds with a re-exported interface augmentation incorrectly retain stale diagnostics until the build cache is cleared.*

 * created by **infomiho**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `Backlog`, and assigned to **johnfav03**

### [Issue microsoft/TypeScript#64387](https://github.com/microsoft/TypeScript/issues/64387) (Open, `Suggestion`, `Domain: API`)

**SyncRpcChannel reads private \`stdout\.\_handle\.fd\`, breaking the sync API on non\-Node runtimes \(Bun\)**

*SyncRpcChannel’s reliance on Node’s private stdout._handle.fd breaks on non-Node runtimes like Bun, so the issue proposes using POSIX FIFOs for a public blocking file descriptor instead.*

 * created by **cairn-intern**
 * [today](https://github.com/microsoft/TypeScript/issues/64387#issuecomment-5783588821) **RyanCavanaugh** referenced the upstream bun issue, pointed to an open PR for adding compatibility, and explained that manually creating pipes posed security concerns

### [PR microsoft/TypeScript#64388](https://github.com/microsoft/TypeScript/pull/64388) (Open, `For Backlog Bug`)

**\[perf\]\[experiment\] fix\(64378\): add a cache to avoid repeated type arg inference**

*Introduce a cache for type argument inference to eliminate repeated inference and significantly improve performance.*

 * created by **a-tarasyuk**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64388#issuecomment-5779998153) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/64388#issuecomment-5779999564) **typescript-automation[bot]** noted that build jobs started and included status and results links
 * [today](https://github.com/microsoft/TypeScript/pull/64388#issuecomment-5780363579) **typescript-automation[bot]** provided the requested perf run results
 * (today) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`

### [PR microsoft/TypeScript#64389](https://github.com/microsoft/TypeScript/pull/64389) (Closed, `For Backlog Bug`)

**Treat \`never\` as non\-mutable\-array\-like when deciding readonly tuples**

*Exclude never from mutable-array-like detection so const-asserted tuples remain readonly when contextual type is never*

 * created by **Darqula**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64389#issuecomment-5779781853) **Darqula** presented the Contributor License Agreement text and signing instructions

### [Issue microsoft/TypeScript#64390](https://github.com/microsoft/TypeScript/issues/64390) (Closed)

**TypeScript 7 \(native\) silently accepts mismatched types past the relater depth fuse**

*TypeScript 7 native compiler silently accepts type mismatches in deeply nested types by removing depth-limit errors.*

 * created by **ChloeVPin**
 * [today](https://github.com/microsoft/TypeScript/issues/64390#issuecomment-5780334610) **RyanCavanaugh** said "Appreciate the disclosure. We have enough organically-encountered issues to not require agents to go looking for additional ones 😉"
 * (today) **ChloeVPin** closed the issue

### [PR microsoft/TypeScript#64391](https://github.com/microsoft/TypeScript/pull/64391) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**\[api\] Fix two filename case sensitivity issues**

*Fix Windows drive letter casing across the API and eliminate client-side directory inference to prevent case-insensitive conflicts*

 * created by **andrewbranch**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript/pull/64391#issuecomment-5783339837) **andrewbranch** identified a conversion path from file name to URI and back that could cause lossy conversions and fixed it in the latest commit
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#64392](https://github.com/microsoft/TypeScript/pull/64392) (Closed, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Onboard loc and vendoring to code generation caching**

*Onboard loc and vendoring to code generation caching by sharing file fingerprints to avoid duplicate hashing and reduce generate time from 10s to 4s*

 * created by **weswigham**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`, and assigned to **weswigham**
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript#64393](https://github.com/microsoft/TypeScript/pull/64393) (Closed, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Just check package\.json for vendor code up\-to\-date\-ness**

*Simplify vendor dependency updates by verifying their versions in package.json instead of inspecting node_modules.*

 * created by **weswigham**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `Author: Team`, `For Uncommitted Bug`, and assigned to **weswigham**
 * (today) **weswigham** closed the issue

### [Issue microsoft/TypeScript#64394](https://github.com/microsoft/TypeScript/issues/64394) (Open, `API Request`, **andrewbranch**)

**\# \[API\] \`getJSDocCommentsAndTags\` is no longer exposed**

*TS7 removed getJSDocCommentsAndTags, so the API needs an equivalent that returns full JSDoc nodes including descriptions and tags*

 * created by **dragomirtitian**
 * (today) **RyanCavanaugh** added label `API Request`, and assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript/issues/64394#issuecomment-5784854686) **andrewbranch** clarified JSDoc API guidelines with three cases for exposing or omitting functionality
 * [later](https://github.com/microsoft/TypeScript/issues/64394#issuecomment-5795022573) **dragomirtitian** suggested exposing getJSDocCommentsAndTags in the new API to match the old implementation and address JSDoc tag standardization

### [PR microsoft/TypeScript#64395](https://github.com/microsoft/TypeScript/pull/64395) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Run and fix codegen tests, make codegen caches per repo root**

*Fix failing codegen tests and isolate codegen caches per repository root to avoid shared worktree conflicts*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/64395#issuecomment-5784426537) **weswigham** stated that Go uses a global build cache and they preferred not cluttering their workspace
 * [today](https://github.com/microsoft/TypeScript/pull/64395#issuecomment-5784439707) **jakebailey** noted that Go uses a global build cache and mentioned that it doesn’t place it in /tmp
 * [today](https://github.com/microsoft/TypeScript/pull/64395#issuecomment-5785027138) **jakebailey** said "Still failing? This is so weird"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64396](https://github.com/microsoft/TypeScript/pull/64396) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Normalize document URIs during decoding**

*Apply vscode-uri-compatible normalization during URI decoding to convert empty or relative file paths into valid filenames.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#64397](https://github.com/microsoft/TypeScript/pull/64397) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**\[api\] Parse tsconfig plugins for external error reporting, expose MappedType properties**

*Enable parsing of tsconfig plugins for external error reporting and expose MappedType properties in the API.*

 * created by **andrewbranch**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`, and assigned to **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript#64398](https://github.com/microsoft/TypeScript/issues/64398) (Closed, `Unactionable`)

**Generic argument narrowed from \`T \| undefined\` collapses a dependent conditional return type to \`never\`/\`undefined\`**

*Narrowing generic parameters from T|undefined through truthiness checks erroneously collapses a dependent conditional return type to never/undefined.*

 * created by **lotexiu**
 * [today](https://github.com/microsoft/TypeScript/issues/64398#issuecomment-5786328589) **RyanCavanaugh** asked why the bug report wasn't minimal and why Keys<T> was chosen over keyof T
 * [later](https://github.com/microsoft/TypeScript/issues/64398#issuecomment-5795007816) **lotexiu** clarified that the initial typing was illustrative and provided the full TypeScript code context with detailed type definitions
 * [later](https://github.com/microsoft/TypeScript/issues/64398#issuecomment-5795084529) **lotexiu** explained they didn't remember the exact reason for creating TObject and TNonObject and recalled having a typing problem; mentioned they were creating a library for learning; shared their repository link; offered to provide further explanations later
 * [later](https://github.com/microsoft/TypeScript/issues/64398#issuecomment-5795490682) **lotexiu** suggested that using `X extends infer R` might act as a cache causing type narrowing issues and asked how to prevent the problem properly
 * [later](https://github.com/microsoft/TypeScript/issues/64398#issuecomment-5796253507) **lotexiu** explained that avoiding `infer R` resolved one issue but that another typing problem required using `as Raw` or `NonNullable` and still needed adjustments
 * [later](https://github.com/microsoft/TypeScript/issues/64398#issuecomment-5796556349) **lotexiu** said "Well, for now, I'll adjust my type definitions to the most appropriate approach—applying NonNullable—and check if other parts of the project are facing this same issue so I can fix them."

### [Issue microsoft/TypeScript#64399](https://github.com/microsoft/TypeScript/issues/64399) (Open, `Design Notes`)

**Design Meeting Notes, 2026\-09\-22**

*Exploring syntax proposals to support satisfies-style whole-signature annotations on TypeScript function declarations.*

 * created by **DanielRosenwasser**
 * **DanielRosenwasser** added label `Design Notes`

### [PR microsoft/TypeScript#64400](https://github.com/microsoft/TypeScript/pull/64400) (Open, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Run code generation on build**

*Automatically run code generation during both build and watch processes to eliminate manual regeneration steps.*

 * created by **weswigham**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`, and assigned to **weswigham**
 * [today](https://github.com/microsoft/TypeScript/pull/64400#issuecomment-5788559466) **weswigham** removed integration-style tests from generatedFile.test.mts as they didn’t focus on caching functionality

### [PR microsoft/TypeScript#64401](https://github.com/microsoft/TypeScript/pull/64401) (Open, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**\[api\] Add createIncrementalProgram**

*Implement createIncrementalProgram API enabling emit to update program state by returning a new snapshot and program.*

 * created by **andrewbranch**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **andrewbranch**

### [PR microsoft/TypeScript#64402](https://github.com/microsoft/TypeScript/pull/64402) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Use lazy map for diagnostic keyToMessage, speeding up go build**

*Optimize diagnostic keyToMessage by using a lazy map to reduce Go build time and improve startup performance.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64403](https://github.com/microsoft/TypeScript/pull/64403) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Pin VS Code localization tooling**

*Pin VS Code localization tooling to control excessive dependencies and submit upstream pull requests to reduce them.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/64403#issuecomment-5786680275) **jakebailey** said "Adds 100 deps and an npm warning. So annoying"
 * [today](https://github.com/microsoft/TypeScript/pull/64403#issuecomment-5786798370) **weswigham** acknowledged that dependencies were dodging analysis by being installed late and suggested acknowledging the problem rather than hiding it
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64404](https://github.com/microsoft/TypeScript/pull/64404) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Watch alias invalidation**

*Updates file watchers to track symlink alias changes so watch mode detects file modifications across different paths.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [Issue microsoft/TypeScript#64405](https://github.com/microsoft/TypeScript/issues/64405) (Open, `Needs Investigation`, **johnfav03**)

**Incremental check emits locationless TS2589 after a comment\-only edit in TypeScript 7**

*TypeScript 7’s incremental compiler erroneously emits a locationless TS2589 error after a comment-only edit despite cold and fresh checks passing.*

 * created by **rexdotsh**
 * [later](https://github.com/microsoft/TypeScript/issues/64405#issuecomment-5793012334) **rexdotsh** provided a fix and regression tests on a fork and offered to file a PR once the issue was verified and added to the Backlog milestone

### [PR microsoft/TypeScript#64406](https://github.com/microsoft/TypeScript/pull/64406) (Closed, `For Uncommitted Bug`)

**LEGO: Pull request from lego/hb\_5378966c\-b857\-470a\-8675\-daebef4a6da1\_20260923092305406 to main**

*Pull request to merge localized lcls updates from lego/hb_5378966c-b857-470a-8675-daebef4a6da1 branch into main.*

 * created by **csigs**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (later) **jakebailey** closed the issue

