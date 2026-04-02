# Report for 2025-12-15 (Monday, December 15th, 2025)

17 different users commented on 32 different issues.

## Recommended Actions

 * Response Recommended
    * @developer-bandi reported that they have reflected requested changes in the PR in [microsoft/TypeScript#60646](https://github.com/microsoft/TypeScript/pull/60646#issuecomment-3659820449)
    * @krisztianb reported that the deprecation marker applied to all method signatures instead of just the intended one in [microsoft/TypeScript#61264](https://github.com/microsoft/TypeScript/issues/61264#issuecomment-3660614606)
    * @freshp86 reported a gap in moduleResolution options and provided contextual details in [microsoft/TypeScript#62206](https://github.com/microsoft/TypeScript/issues/62206#issuecomment-3657546540)
    * @freshp86 asked whether they should file a new feature request in [microsoft/TypeScript#62206](https://github.com/microsoft/TypeScript/issues/62206#issuecomment-3657758740)
    * @AryanBagade asked @RyanCavanaugh to review the PR in [microsoft/TypeScript#62895](https://github.com/microsoft/TypeScript/pull/62895#issuecomment-3657586110)
    * @thromel asked whether the new strict-mode check should be unconditional or strict-mode dependent in [microsoft/TypeScript#62899](https://github.com/microsoft/TypeScript/pull/62899#issuecomment-3657093047)
    * @rubiesonthesky pointed out that the description linked to the wrong issue in [microsoft/TypeScript#62900](https://github.com/microsoft/TypeScript/pull/62900#issuecomment-3657696139)

## Activity Summary

### [Issue microsoft/TypeScript#23155](https://github.com/microsoft/TypeScript/issues/23155) (Closed, `External`, `Fix Available`)

**Type error in Buffer\.from\(\)**

*Passing a value of type string|Buffer to Buffer.from triggers a TypeScript compilation error despite existing overloads for string and Buffer.*

 * [7.6 years ago](https://github.com/microsoft/TypeScript/issues/23155#issuecomment-381717681) **inlined** retracted previous comments, suggested exposing the type in types/node/v8 and removing the comment elsewhere, acknowledged missing the collapsed overload, pointed out a discrepancy in NodeJS Buffer.from documentation, and asked whether the docs should be trusted when reviewing the codebase
 * [7.6 years ago](https://github.com/microsoft/TypeScript/issues/23155#issuecomment-381749286) **Flarna** found that TypeScript's lib.es6.d.ts already included typed arrays, proposed adding them or defining a TypedArray alias, noted other commented locations needing updates, and clarified Node.js docs discrepancy between v4 and master suggesting a PR to update the docs
 * **typescript-bot** added label `Fix Available`

### [Issue microsoft/TypeScript#23572](https://github.com/microsoft/TypeScript/issues/23572) (Open, `Bug`, `Domain: check: Control Flow`, `Fix Available`, **Copilot**)

**Exhaustiveness checking against an enum only works when the enum has \>1 member\.**

*TypeScript's exhaustiveness checking on a discriminated union fails when the enum used for the discriminant has only one member.*

 * (20 weeks ago) **RyanCavanaugh** added label `Domain: Control Flow`, removed label `Fix Available`, and unassigned **Copilot**
 * [today](https://github.com/microsoft/TypeScript/issues/23572#issuecomment-3657279775) **RyanCavanaugh** said "Naive version of this is very bad (see PR #62114)"
 * **RyanCavanaugh** assigned to **Copilot**
 * (today) **typescript-bot** added labels `Fix Available`, `Fix Available`

### [PR microsoft/TypeScript#49552](https://github.com/microsoft/TypeScript/pull/49552) (Closed, `Experiment`, `Author: Team`, `For Uncommitted Bug`, **rbuckton**)

**More specific TemplateStringsArray type for tagged templates**

*Proposal to refine TemplateStringsArray types in TypeScript to enable literal-aware interpolation for tagged templates*

 * [37 weeks ago](https://github.com/microsoft/TypeScript/pull/49552#issuecomment-2755704370) **porsager** said "Pleeeeease reconsider merging this! I mean... Doom was implemented in Typescript but we can't do this? 😥"
 * [18 weeks ago](https://github.com/microsoft/TypeScript/pull/49552#issuecomment-3173673073) **sosoba** noted that Ts 5.9 still didn't provide types for TemplateStringsArray
 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/49552#issuecomment-3590394392) **diegoimbert** said "Would really love it, it would enable me to have typed sqlQUERIES in Windmill :)"
 * (today) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/49552#issuecomment-3657312887) **typescript-bot** said "The TypeScript team hasn't accepted the linked issue #33304. If you can get it accepted, this PR will have a better chance of being reviewed."

### [PR microsoft/TypeScript#51913](https://github.com/microsoft/TypeScript/pull/51913) (Closed)

**\[wip\] Remove \`objectAllocator\` concept**

*Remove the objectAllocator concept from the system to simplify resource allocation logic.*

 * [1.6 years ago](https://github.com/microsoft/TypeScript/pull/51913#issuecomment-2062866718) **typescript-bot** provided detailed performance benchmark results as requested
 * [1.6 years ago](https://github.com/microsoft/TypeScript/pull/51913#issuecomment-2064407991) **rbuckton** said "I still have a bit more investigating to do into the memory overhead in self-build-src-public-api, but this is close enough to turn it into an actual PR."
 * [1.6 years ago](https://github.com/microsoft/TypeScript/pull/51913#issuecomment-2064433682) **jakebailey** asked for confirmation to review the PR despite the [WIP] title
 * (today) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/51913#issuecomment-3657312877) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."

### [PR microsoft/TypeScript#58362](https://github.com/microsoft/TypeScript/pull/58362) (Closed, `Author: Team`, `For Uncommitted Bug`, **rbuckton**)

**Perform bounds\-checking on string input in scanner**

*Perform bounds checking across the scanner's string input and introduce a lint rule to catch unchecked charCodeAt or codePointAt calls.*

 * [1.6 years ago](https://github.com/microsoft/TypeScript/pull/58362#issuecomment-2083737706) **rbuckton** noted no noticeable performance improvement and suggested only adopting the change if bounds checking enforcement is valued for correctness and stability
 * [1.6 years ago](https://github.com/microsoft/TypeScript/pull/58362#issuecomment-2083822430) **DanielRosenwasser** said "It seems like parse is (only very slightly) worse - I wonder what happens if you switch that initial call in scan to the old unchecked version, but I'm guessing it's more death by a thousand cuts."
 * [1.6 years ago](https://github.com/microsoft/TypeScript/pull/58362#issuecomment-2083841524) **rbuckton** said "It may be that some code paths aren't run enough times to be optimized and thus the functions aren't inlined. I'll have to look at it in deopt-explorer."
 * (today) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/58362#issuecomment-3657312856) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."

### [PR microsoft/TypeScript#59190](https://github.com/microsoft/TypeScript/pull/59190) (Closed, `For Uncommitted Bug`)

**Make AST nodes monomorphic\.**

*Convert all AST nodes to monomorphic definitions to streamline the compiler’s internal representation.*

 * [1.4 years ago](https://github.com/microsoft/TypeScript/pull/59190#issuecomment-2215495882) **jakebailey** said "@typescript-bot perf test this"
 * [1.4 years ago](https://github.com/microsoft/TypeScript/pull/59190#issuecomment-2215495942) **typescript-bot** reported starting of performance tests and provided status and results links
 * [1.4 years ago](https://github.com/microsoft/TypeScript/pull/59190#issuecomment-2215546575) **typescript-bot** provided the requested performance run results
 * (today) **dragomirtitian** closed the issue

### [PR microsoft/TypeScript#59191](https://github.com/microsoft/TypeScript/pull/59191) (Closed, `For Uncommitted Bug`)

**Make types monomorphic**

*Convert all types to monomorphic forms as part of issue #58928.*

 * [1.4 years ago](https://github.com/microsoft/TypeScript/pull/59191#issuecomment-2215495825) **jakebailey** said "@typescript-bot perf test this"
 * [1.4 years ago](https://github.com/microsoft/TypeScript/pull/59191#issuecomment-2215495890) **typescript-bot** reported that performance tests started and provided links to build results
 * [1.4 years ago](https://github.com/microsoft/TypeScript/pull/59191#issuecomment-2215668045) **typescript-bot** posted the requested performance run results
 * (today) **dragomirtitian** closed the issue

### [PR microsoft/TypeScript#59192](https://github.com/microsoft/TypeScript/pull/59192) (Closed, `For Uncommitted Bug`)

**Make Signature monomorphic**

*Restrict function signatures to monomorphic types as part of implementing issue #58928*

 * [1.4 years ago](https://github.com/microsoft/TypeScript/pull/59192#issuecomment-2215495781) **jakebailey** said "@typescript-bot perf test this"
 * [1.4 years ago](https://github.com/microsoft/TypeScript/pull/59192#issuecomment-2215495816) **typescript-bot** provided automated build status update
 * [1.4 years ago](https://github.com/microsoft/TypeScript/pull/59192#issuecomment-2215630536) **typescript-bot** provided the requested perf run results
 * (today) **dragomirtitian** closed the issue

### [PR microsoft/TypeScript#59623](https://github.com/microsoft/TypeScript/pull/59623) (Closed, `Author: Team`, `For Uncommitted Bug`, **rbuckton**)

**Experiment: Always report \`useDefineForClassFields\`\-related errors even when disabled**

*Enable reporting of useDefineForClassFields-related errors even when disabled to assess dependency on initializer ordering.*

 * [1.3 years ago](https://github.com/microsoft/TypeScript/pull/59623#issuecomment-2287412639) **typescript-bot** reported tsc results for the top 400 repos comparing main to the PR and noted a google/blockly build failure
 * **DanielRosenwasser** added to milestone `TypeScript 5.7.0`
 * [41 weeks ago](https://github.com/microsoft/TypeScript/pull/59623#issuecomment-2683277723) **trevorade** noted that the commit likely missed a change to make isBlockScopedNameDeclaredBeforeUse ignore emitStandardClassFields when called from checkPropertyNotUsedBeforeDeclaration and that they needed to update the code to make TS2729 universally emitted
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#59992](https://github.com/microsoft/TypeScript/pull/59992) (Closed, `Author: Team`, `For Uncommitted Bug`, **rbuckton**)

**\[WIP\] Experimental Slim \`AstNode\` API **

*Introduce an experimental slim AstNode API to provide monomorphic AST node access for improved compiler performance and backwards compatibility.*

 * [1.1 years ago](https://github.com/microsoft/TypeScript/pull/59992#issuecomment-2392175661) **rbuckton** said "@typescript-bot perf test faster"
 * [1.1 years ago](https://github.com/microsoft/TypeScript/pull/59992#issuecomment-2392175758) **typescript-bot** started CI jobs for `perf test faster` and posted status and results links
 * [1.1 years ago](https://github.com/microsoft/TypeScript/pull/59992#issuecomment-2392251512) **typescript-bot** provided perf run results
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#60334](https://github.com/microsoft/TypeScript/pull/60334) (Closed, `Author: Team`, `For Milestone Bug`, **rbuckton**)

**Add special inference rule for 'T \| PromiseLike\<T\>'**

*Add inference rule and performance shortcut for unions of T with Promise<T> or PromiseLike<T> to infer union types directly.*

 * [1.1 years ago](https://github.com/microsoft/TypeScript/pull/60334#issuecomment-2434109486) **typescript-bot** reported tsserver exited prematurely with signal SIGABRT on backstage/backstage while comparing main and refs/pull/60334/merge and provided repro steps
 * [1.1 years ago](https://github.com/microsoft/TypeScript/pull/60334#issuecomment-2434109495) **typescript-bot** reported server exit errors in elastic/kibana from the top 200 repos suite and provided logs and repro steps
 * [1.1 years ago](https://github.com/microsoft/TypeScript/pull/60334#issuecomment-2436253526) **rbuckton** said "This needs a bit more work, so I'm converting it to a draft."
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#60646](https://github.com/microsoft/TypeScript/pull/60646) (Open, `For Backlog Bug`)

**Add the type of Intl\.DurationFormat to the lib\.**

*Add initial type definitions for the Intl.DurationFormat API to the TypeScript standard library declarations*

 * [25 weeks ago](https://github.com/microsoft/TypeScript/pull/60646#issuecomment-2994276018) **Wiktor102** said "Is this PR being worked on? It seems to be pretty important, given that for almost 4 months now, this API has had the "Baseline Newly available" status."
 * [6 weeks ago](https://github.com/microsoft/TypeScript/pull/60646#issuecomment-3480333874) **Standard8** said "It looks like there's just one change remaining to complete this. Would it be possible that it could happen soon, or should someone take over (or maybe a maintainer can change the branch?)?"
 * [today](https://github.com/microsoft/TypeScript/pull/60646#issuecomment-3654395110) **smorimoto** said "Gentle ping"
 * [later](https://github.com/microsoft/TypeScript/pull/60646#issuecomment-3659820449) **developer-bandi** apologized for the delay and reflected the requested changes in the PR

### [PR microsoft/TypeScript#61262](https://github.com/microsoft/TypeScript/pull/61262) (Closed)

**\[WIP\] Disallow merging of \`enum\` declarations**

*Assess the impact of disallowing merged enum declarations on code behavior.*

 * [37 weeks ago](https://github.com/microsoft/TypeScript/pull/61262#issuecomment-2766559937) **rbuckton** said "@typescript-bot test top999"
 * [37 weeks ago](https://github.com/microsoft/TypeScript/pull/61262#issuecomment-2766560137) **typescript-bot** started test jobs and posted status and results links
 * [37 weeks ago](https://github.com/microsoft/TypeScript/pull/61262#issuecomment-2767291625) **typescript-bot** reported build results for the top 999 repos with tsc, noted an interesting change, and detailed failures in microsoft/azuredatastudio
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#61264](https://github.com/microsoft/TypeScript/issues/61264) (Open, `Needs More Info`)

**\`Element\.getElementsByTagName\` marked as deprecated**

*Element.getElementsByTagName is wrongly flagged as deprecated on union-typed Elements in TypeScript lib v5.6.3.*

 * [41 weeks ago](https://github.com/microsoft/TypeScript/issues/61264#issuecomment-2685066299) **snarbles2** asked what the reporter saw when going to the member definition and noted they couldn't reproduce the issue
 * [41 weeks ago](https://github.com/microsoft/TypeScript/issues/61264#issuecomment-2685437475) **nmain** reproduced the issue in VSCode and noted uncertainty about whether the error stemmed from VSCode, TypeScript, or their integration while showing that quick info and go-to-definition both displayed the first overload
 * [31 weeks ago](https://github.com/microsoft/TypeScript/issues/61264#issuecomment-2860323292) **apttap** reproduced the issue in nvim with a union type and demonstrated a deprecated error on the return statement, then described a workaround by casting to HTMLElement
 * [later](https://github.com/microsoft/TypeScript/issues/61264#issuecomment-3660614606) **krisztianb** reported that the @deprecated marker wrongly marked all method signatures as deprecated, causing warnings everywhere

### [Issue microsoft/TypeScript#62206](https://github.com/microsoft/TypeScript/issues/62206) (Closed, `Suggestion`, `Breaking Change`, `Committed`, `Fix Available`, **andrewbranch**)

**Deprecate, remove \`\-\-moduleResolution classic\`**

*TypeScript will deprecate `--moduleResolution classic` in 6.0 and remove it by 7.0, recommending `nodenext` or `bundler` instead.*

 * [14 weeks ago](https://github.com/microsoft/TypeScript/issues/62206#issuecomment-3251084361) **DanielRosenwasser** said "Note: this is a bit iffy since the default might still be classic, but it'll be deprecated."
 * **typescript-bot** added label `Fix Available`
 * (7 weeks ago) **andrewbranch** closed the issue
 * [today](https://github.com/microsoft/TypeScript/issues/62206#issuecomment-3657546540) **freshp86** endorsed the suggestion, explained that a moduleResolution mode for browser-targeted ESM without bundling is missing, and illustrated inefficiencies of using NodeNext with a trace from Chromium's build
 * [today](https://github.com/microsoft/TypeScript/issues/62206#issuecomment-3657576330) **andrewbranch** clarified that the trace was looking for a package.json "type" setting rather than node_modules resolutions, noted that cached lookups eliminate performance cost, and agreed that no existing resolution mode perfectly fits browser-based ESM
 * [today](https://github.com/microsoft/TypeScript/issues/62206#issuecomment-3657758740) **freshp86** acknowledged the negligible performance impact, suggested using import/export detection for browser ESM resolution, warned about lookups reaching outside the project root, and asked whether to file a new feature request

### [PR microsoft/TypeScript#62523](https://github.com/microsoft/TypeScript/pull/62523) (Closed, `For Backlog Bug`)

**fix\(62487\): Completion after initialized class property with const assertion and no semicolon**

*Enable code completion after initializing class properties with const assertions without requiring a trailing semicolon*

 * created by **a-tarasyuk**
 * **typescript-bot** added label `For Backlog Bug`
 * (today) **a-tarasyuk** closed the issue

### [PR microsoft/TypeScript#62567](https://github.com/microsoft/TypeScript/pull/62567) (Closed, `Breaking Change`, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**Deprecate esModuleInterop and allowSyntheticDefaultImports \(default to true\)**

*Deprecate the esModuleInterop and allowSyntheticDefaultImports compiler options by enabling them by default.*

 * [7 weeks ago](https://github.com/microsoft/TypeScript/pull/62567#issuecomment-3434602068) **typescript-bot** notified that DT test results were ready and provided links to detailed logs
 * [7 weeks ago](https://github.com/microsoft/TypeScript/pull/62567#issuecomment-3434630007) **jakebailey** said "Uh oh"
 * [yesterday](https://github.com/microsoft/TypeScript/pull/62567#issuecomment-3652613304) **LukeAbby** said "Heads up, because there's no issue with "Breaking Change" the only way I discovered this was by having the error and finding this PR. Not sure how big of a deal that is though."
 * **jakebailey** added label `Breaking Change`

### [PR microsoft/TypeScript#62684](https://github.com/microsoft/TypeScript/pull/62684) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**\[experiment\] Remove package deduplication**

*Experimentally remove package deduplication to assess the negative impact of not resolving typescript-go issue 1080.*

 * (4 days ago) **typescript-bot** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#62886](https://github.com/microsoft/TypeScript/issues/62886) (Closed, `Duplicate`)

**composite typescript project types should not leak into excluded files**

*Composite TypeScript projects' types settings in referenced tsconfigs are leaking into excluded files.*

 * [3 days ago](https://github.com/microsoft/TypeScript/issues/62886#issuecomment-3647591319) **RyanCavanaugh** noted that the issue duplicated #33094 and suggested a way to specify alternative tsconfig files while ignoring tsconfig.json
 * **RyanCavanaugh** added label `Duplicate`
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/62886#issuecomment-3648941857) **valler** explained that TS Server was leaking types across referenced projects due to tsconfig.json and package.json combination and noted that include/files/types settings seemed to be ignored
 * [today](https://github.com/microsoft/TypeScript/issues/62886#issuecomment-3658322144) **typescript-bot** said "This issue has been marked as "Duplicate" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-bot** closed the issue

### [PR microsoft/TypeScript#62889](https://github.com/microsoft/TypeScript/pull/62889) (Closed, `Author: Team`, `For Uncommitted Bug`, **RyanCavanaugh**)

**Add note re: PRs to CONTRIBUTING\.md**

*Add a note to CONTRIBUTING.md outlining pull request guidelines per the 6.0/7.0 plan.*

 * (4 days ago) **typescript-bot** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **RyanCavanaugh**
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#62894](https://github.com/microsoft/TypeScript/pull/62894) (Open, `Author: Team`, `For Uncommitted Bug`, **sheetalkamat**)

**Handle resolution watching when its dynamic scriptInfo**

*Stop watching failed lookup paths, inferred typeRoots, and typing installer locations for dynamic scripts using unwatchable or default directories.*

 * (3 days ago) **typescript-bot** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **sheetalkamat**
 * [today](https://github.com/microsoft/TypeScript/pull/62894#issuecomment-3656739718) **jakebailey** asked what constituted a dynamic script and whether custom file extensions would be affected, and whether the fix should be backported to 5.9 given the 6.0 timeline

### [PR microsoft/TypeScript#62895](https://github.com/microsoft/TypeScript/pull/62895) (Open, `For Backlog Bug`)

**Fix ClassDecoratorContext\.name to use literal class name \(\#62870\)**

*Emit the literal class name for decorator context name rather than accessing the static name property*

 * created by **AryanBagade**
 * **typescript-bot** added label `For Backlog Bug`
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/62895#issuecomment-3649150576) **AryanBagade** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript/pull/62895#issuecomment-3657586110) **AryanBagade** requested @RyanCavanaugh to review the PR

### [Issue microsoft/TypeScript#62896](https://github.com/microsoft/TypeScript/issues/62896) (Open, `Bug`, `Help Wanted`, `Fix Available`)

**Using declarations like a statement leads to strange bugs\.**

*Using var and function declarations as statements in blocks leads to inconsistent compile-time and runtime errors in TypeScript.*

 * created by **olegdunkan**
 * [today](https://github.com/microsoft/TypeScript/issues/62896#issuecomment-3656466958) **nmain** explained that using a var before initialization is type-unsafe and that TypeScript’s inability to prove a loop executes at least once isn’t a compiler bug
 * [today](https://github.com/microsoft/TypeScript/issues/62896#issuecomment-3656897387) **RyanCavanaugh** clarified that the first case was not a bug and the second was a proper parse error under strict mode
 * (today) **RyanCavanaugh** added labels `Bug`, `Help Wanted`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/62896#issuecomment-3657071793) **MartinJohns** said "It sounds like it's a regression: #7122"
 * [today](https://github.com/microsoft/TypeScript/issues/62896#issuecomment-3657501332) **jakebailey** clarified that strict mode wasn't assumed until version 7.0 and that submitting a PR now was premature
 * [today](https://github.com/microsoft/TypeScript/issues/62896#issuecomment-3657606667) **jakebailey** said "Hm, no: https://github.com/microsoft/TypeScript/issues/54500#:~:text=for%20RWC%20run.-,alwaysStrict,-The%20alwaysStrict%20flag"
 * [today](https://github.com/microsoft/TypeScript/issues/62896#issuecomment-3657635079) **RyanCavanaugh** said "I also misspoke because this should be handled according to the existing strictMode logic for 6.0, since it'll be possible to turn off alwaysStrict in 6.0. 7.0 can be more aggressive."
 * [today](https://github.com/microsoft/TypeScript/issues/62896#issuecomment-3657641271) **RyanCavanaugh** clarified that issue #7122 concerned cases where a function declared inside a conditional could be called illegally in certain modes and noted that single-line conditional function declarations have never errored
 * (today) **RyanCavanaugh** set milestone to `Dormant`, and removed from milestone `Backlog`
 * **typescript-bot** added label `Fix Available`

### [PR microsoft/TypeScript#62897](https://github.com/microsoft/TypeScript/pull/62897) (Closed, `For Uncommitted Bug`, `dependencies`, `github_actions`)

**Bump the github\-actions group with 4 updates**

*Bump four GitHub Action dependencies: upload-artifact to v6.0.0, codecov-action, actions/cache, and codeql-action.*

 * (yesterday) **dependabot[bot]** added labels `dependencies`, `github_actions`
 * **typescript-bot** added label `For Uncommitted Bug`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#62898](https://github.com/microsoft/TypeScript/issues/62898) (Open, `Duplicate`)

**Disallow objects with extra properties from being assigned to wider types**

*Track extra object properties to prevent assigning them to wider types and avoid incorrect typing*

 * created by **twilkinson3421**
 * [today](https://github.com/microsoft/TypeScript/issues/62898#issuecomment-3656614510) **nmain** said "If this was applied to all existing types, it would be a massive breaking change.  If it was applied only to specific opt-in types, it'd be https://github.com/microsoft/TypeScript/issues/12936."
 * **RyanCavanaugh** added label `Duplicate`

### [PR microsoft/TypeScript#62899](https://github.com/microsoft/TypeScript/pull/62899) (Open, `For Milestone Bug`)

**Report error for function declarations as statement children in strict mode**

*TypeScript reports TS1256 errors when function declarations appear as direct children of if, while, for, or labeled statements in strict mode.*

 * created by **thromel**
 * **typescript-bot** added label `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/62899#issuecomment-3657093047) **thromel** asked whether the new strict-mode error check should report unconditionally or only in strict mode
 * [today](https://github.com/microsoft/TypeScript/pull/62899#issuecomment-3657498448) **jakebailey** corrected that TypeScript does not assume strict mode at all times and suggested delaying until 7.0
 * [today](https://github.com/microsoft/TypeScript/pull/62899#issuecomment-3657608542) **jakebailey** referenced a TypeScript issue and suggested reporting only when isStrictMode is true, noting the option will be removed in a later or earlier PR
 * (today) **typescript-bot** added label `For Milestone Bug`, and removed label `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/62899#issuecomment-3658546964) **thromel** said "@jakebailey Thanks for the clarification! I've updated the PR to only report the error when inStrictMode is true, consistent with other strict mode checks."

### [PR microsoft/TypeScript#62900](https://github.com/microsoft/TypeScript/pull/62900) (Open, `For Milestone Bug`, **RyanCavanaugh**, **Copilot**)

**Fix exhaustiveness checking for single\-member enums in switch statements**

*Modify switch exhaustiveness checking to correctly narrow single-member enums to never in default cases.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * **typescript-bot** added label `For Milestone Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/62900#issuecomment-3657696139) **rubiesonthesky** said "The description links to wrong issue with Fixed comment. The correct issue is below it, but it was surprising to end up in an issue that was already closed and didn’t seem related."
 * [today](https://github.com/microsoft/TypeScript/pull/62900#issuecomment-3658055225) **RyanCavanaugh** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/62900#issuecomment-3658055366) **typescript-bot** posted automated CI job start and completion statuses
 * [today](https://github.com/microsoft/TypeScript/pull/62900#issuecomment-3658100201) **typescript-bot** notified that the DT test results were ready and unchanged, with a link to the build log
 * [today](https://github.com/microsoft/TypeScript/pull/62900#issuecomment-3658115124) **typescript-bot** reported test results and noted a git clone failure but otherwise everything passed
 * [today](https://github.com/microsoft/TypeScript/pull/62900#issuecomment-3658174099) **typescript-bot** reported the performance run results requested by @RyanCavanaugh
 * [today](https://github.com/microsoft/TypeScript/pull/62900#issuecomment-3658238166) **typescript-bot** reported that results of running the top 400 repos with tsc comparing main and the pull request merge looked good

### [Issue microsoft/TypeScript#62901](https://github.com/microsoft/TypeScript/issues/62901) (Closed, `Working as Intended`)

**Inconsistent reference when type parameter is involved in This\-Typing**

*TypeScript inconsistently infers j’s narrowed type with a this-based type guard depending on generic parameter usage.*

 * created by **hkleungai**
 * [today](https://github.com/microsoft/TypeScript/issues/62901#issuecomment-3657333643) **MartinJohns** explained that J<string> was identical to J<number> when the type parameter was unused and pointed to the FAQ guidance on avoiding unused type parameters
 * **RyanCavanaugh** added label `Working as Intended`
 * [today](https://github.com/microsoft/TypeScript/issues/62901#issuecomment-3657417492) **hkleungai** tested a change from string|number to string|boolean and found the issue persisted
 * [today](https://github.com/microsoft/TypeScript/issues/62901#issuecomment-3657517247) **MartinJohns** explained that J<string>, J<number>, J<boolean>, and J<number | string> were identical types and asked why the else-block result shouldn't be never
 * (today) **hkleungai** closed the issue
 * [today](https://github.com/microsoft/TypeScript/issues/62901#issuecomment-3657555558) **MartinJohns** explained how structural typing in TypeScript makes two interface instantiations incompatible when they have differing properties but identical when they don’t
 * [today](https://github.com/microsoft/TypeScript/issues/62901#issuecomment-3658901584) **hkleungai** thanked the maintainer for the detailed explanation and acknowledged not being used to think that deeply on this side of TypeScript

### [PR microsoft/TypeScript#62902](https://github.com/microsoft/TypeScript/pull/62902) (Open, `For Backlog Bug`)

**Fix \_\_setFunctionName overriding custom static name property**

*Modify __setFunctionName helper to preserve custom static name properties on decorated classes.*

 * created by **pranshugupta01**
 * **typescript-bot** added label `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/62902#issuecomment-3657395828) **pranshugupta01** agreed with microsoft-github-policy-service

### [Issue microsoft/TypeScript#62903](https://github.com/microsoft/TypeScript/issues/62903) (Open)

**erasableSyntaxOnly: support commonjs require/exports in \.cts files**

*Allow CommonJS require and module.exports syntax inside .cts files when erasableSyntaxOnly is enabled.*

 * created by **Knagis**

