# Report for 2025-12-10 (Wednesday, December 10th, 2025)

18 different users commented on 40 different issues.

## Recommended Actions

 * Response Recommended
    * @tif-calin asked for an update on fixing the event type in [microsoft/TypeScript#28293](https://github.com/microsoft/TypeScript/issues/28293#issuecomment-3639705197)
    * @json-derulo provided important information about Firefox support and a link to the issue tracker in [microsoft/TypeScript#61713](https://github.com/microsoft/TypeScript/issues/61713#issuecomment-3641060663)
    * @Scalahansolo asked when and how the PR marked for TS 6.0 would land in TS 7 in [microsoft/TypeScript#62844](https://github.com/microsoft/TypeScript/pull/62844#issuecomment-3638995505)
    * @Semmu provided repro steps for tsserver crash in [microsoft/TypeScript#62869](https://github.com/microsoft/TypeScript/issues/62869#issuecomment-3639512384)
    * @Semmu provided additional reproduction details and a workaround in [microsoft/TypeScript#62869](https://github.com/microsoft/TypeScript/issues/62869#issuecomment-3639517265)
    * @sAchin-680 asked to be assigned and offered to open a PR in [microsoft/TypeScript#62870](https://github.com/microsoft/TypeScript/issues/62870#issuecomment-3641999947)
    * @robpalme reported that the compiler crashed when provoking the intended checker error and provided a StackBlitz link in [microsoft/TypeScript#62876](https://github.com/microsoft/TypeScript/pull/62876#issuecomment-3641045349)

## Activity Summary

### [Issue microsoft/TypeScript#28293](https://github.com/microsoft/TypeScript/issues/28293) (Open, `Bug`, `Domain: lib.d.ts`)

**Broken IndexedDB event typings in 3\.1\.5**

*IndexedDB onsuccess events in TypeScript 3.1.5 incorrectly type evt.target as EventTarget, preventing direct access to result.*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [6.4 years ago](https://github.com/microsoft/TypeScript/issues/28293#issuecomment-512286142) **sandersn** explained that ProgressEvent now had a type parameter controlling the type of target and that the fix involved passing the type in from the subclass declaration
 * [6.1 years ago](https://github.com/microsoft/TypeScript/issues/28293#issuecomment-548192258) **tonitrnel** proposed a TypeScript snippet showing how to open an indexedDB database and handle the onsuccess event
 * [today](https://github.com/microsoft/TypeScript/issues/28293#issuecomment-3639705197) **tif-calin** mentioned that the workaround worked but TypeScript should support idiomatic MDN code and asked for an update on fixing the event type

### [PR microsoft/TypeScript#53346](https://github.com/microsoft/TypeScript/pull/53346) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Use iterators to avoid calculating all properties of UnionOrIntersectionType**

*Implement iterators in getPropertiesOfUnionOrIntersectionType to enable early exit and achieve a 44% speedup.*

 * [1.4 years ago](https://github.com/microsoft/TypeScript/pull/53346#issuecomment-2193712082) **typescript-bot** reported that CI jobs had started and provided links to build status and results
 * [1.4 years ago](https://github.com/microsoft/TypeScript/pull/53346#issuecomment-2193829699) **typescript-bot** provided the performance run results requested by @jakebailey
 * [1.4 years ago](https://github.com/microsoft/TypeScript/pull/53346#issuecomment-2195817969) **jakebailey** said "Wow, now this PR gets a 10% speedup in mui-docs."
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#54925](https://github.com/microsoft/TypeScript/issues/54925) (Open, `Suggestion`, `Feature Update`)

**Numeric Range Types \(Feature Update\)**

*Introduce numeric and character range types (0..15, 0...1, 'a'..'d') to represent bounded values in type definitions.*

 * [today](https://github.com/microsoft/TypeScript/issues/54925#issuecomment-3636576684) **KrystilizeNevaDies** asked why `0..32767` being a subtype of `5` mattered and proposed expanding conditional types to simplify logic
 * [today](https://github.com/microsoft/TypeScript/issues/54925#issuecomment-3636600953) **shaedrich** suggested differentiating integer and floating-point ranges using `0..100` and `0...100` syntax, noting Ruby's similar inclusive/exclusive range notation
 * [today](https://github.com/microsoft/TypeScript/issues/54925#issuecomment-3636617328) **KrystilizeNevaDies** said "@shaedrich I feel like if a float implementation is possible, an int implementation is pretty low priority since we should be able to model all int operations as types."
 * [today](https://github.com/microsoft/TypeScript/issues/54925#issuecomment-3639435722) **mostpinkest** said "Whilst you can currently model int ranges with types, they quickly run up against performance impacts and built-in limits with larger ranges. "
 * [today](https://github.com/microsoft/TypeScript/issues/54925#issuecomment-3639815670) **KrystilizeNevaDies** proposed using bounds as eager floating point intervals in TypeScript and provided example code

### [Issue microsoft/TypeScript#55124](https://github.com/microsoft/TypeScript/issues/55124) (Closed, `Duplicate`)

**Use keyof to get the union name in generic comprehensions\. If the key value contains an ordinary function, the type hint is lost**

*Keyof extraction of nested object keys in TypeScript loses function property types in WebStorm, causing type errors.*

 * [2.3 years ago](https://github.com/microsoft/TypeScript/issues/55124#issuecomment-1652781319) **typescript-bot** said "This issue has been marked as "Duplicate" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (2.3 years ago) **typescript-bot** closed the issue
 * (today) **gabritto** closed the issue

### [Issue microsoft/TypeScript#55489](https://github.com/microsoft/TypeScript/issues/55489) (Closed, `Duplicate`)

**Iterable gets resolved incorrectly if value is passed directly and element has method**

*TypeScript incorrectly infers an iterable’s element type when passed directly as a literal containing objects with methods.*

 * [2.2 years ago](https://github.com/microsoft/TypeScript/issues/55489#issuecomment-1694539403) **typescript-bot** said "This issue has been marked as "Duplicate" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (2.2 years ago) **typescript-bot** closed the issue
 * (today) **gabritto** closed the issue

### [Issue microsoft/TypeScript#55732](https://github.com/microsoft/TypeScript/issues/55732) (Closed, `Needs More Info`)

**Debug Failure\. False expression\.**

*Opening a specific .dot file causes tsserver to throw a Debug Failure: False expression error.*

 * [2.2 years ago](https://github.com/microsoft/TypeScript/issues/55732#issuecomment-1719049986) **Innei** stated they couldn't create a minimal reproduction and only observed the error when opening the specified file
 * [2.2 years ago](https://github.com/microsoft/TypeScript/issues/55732#issuecomment-1719112441) **Andarist** suggested bisecting the code and iteratively reducing the file and its imports to isolate the issue
 * (1.3 years ago) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript/issues/55732#issuecomment-3638999554) **DanielRosenwasser** found a repro while testing the rewrite and linked the relevant issue and pull request

### [Issue microsoft/TypeScript#56067](https://github.com/microsoft/TypeScript/issues/56067) (Closed, `Duplicate`)

**Arrow functions behave inconsistently with classic functions**

*Mixing arrow and method definitions for getState and getData prevents TypeScript from inferring their return types in actions.*

 * [2.1 years ago](https://github.com/microsoft/TypeScript/issues/56067#issuecomment-1763228151) **typescript-bot** said "This issue has been marked as "Duplicate" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (2.1 years ago) **typescript-bot** closed the issue
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript#56072](https://github.com/microsoft/TypeScript/pull/56072) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Shortcut relations in getNarrowedTypeWorker when comparing literals**

*Pre-check literal equality in getNarrowedTypeWorker to skip redundant relation calls and speed up union-narrowing by over four times.*

 * [1.8 years ago](https://github.com/microsoft/TypeScript/pull/56072#issuecomment-1901426385) **typescript-bot** reported the perf run results for the requested comparison
 * [35 weeks ago](https://github.com/microsoft/TypeScript/pull/56072#issuecomment-2775795188) **sandersn** asked whether the results indicated that this was worth pursuing and whether to keep it open, noting that a quick glance at the latest perf run didn't show anything substantial
 * [35 weeks ago](https://github.com/microsoft/TypeScript/pull/56072#issuecomment-2776135914) **jakebailey** said "You can see the relevant benchmark in the original post; our current test suite doesn't have a case like this."
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#57572](https://github.com/microsoft/TypeScript/issues/57572) (Closed, `Duplicate`)

**generics can only detect arrow function in object but not function expression**

*A TypeScript generic incorrectly fails to infer callback parameter types for object function expressions but works for arrow functions.*

 * [1.7 years ago](https://github.com/microsoft/TypeScript/issues/57572#issuecomment-1974161180) **typescript-bot** said "This issue has been marked as "Duplicate" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (1.7 years ago) **typescript-bot** closed the issue
 * (today) **gabritto** closed the issue

### [Issue microsoft/TypeScript#58630](https://github.com/microsoft/TypeScript/issues/58630) (Closed, `Duplicate`)

**Function generic unmatched: Matching hehavior is difference between arrow functions and normal function**

*TypeScript incorrectly rejects module state definitions using normal function syntax while accepting arrow function equivalents in createStore options.*

 * [1.5 years ago](https://github.com/microsoft/TypeScript/issues/58630#issuecomment-2157017306) **typescript-bot** said "This issue has been marked as "Duplicate" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (1.5 years ago) **typescript-bot** closed the issue
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript#58638](https://github.com/microsoft/TypeScript/pull/58638) (Closed, `Breaking Change`, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**Always resolve package\.json exports in type reference directives**

*The TypeScript compiler should consistently resolve package.json exports when processing type reference directives.*

 * [1.5 years ago](https://github.com/microsoft/TypeScript/pull/58638#issuecomment-2128270621) **typescript-bot** reported build failures for TanStack/query and Tencent/omi integrations when running the top 400 repos suite with the old tsc
 * [1.5 years ago](https://github.com/microsoft/TypeScript/pull/58638#issuecomment-2128270628) **typescript-bot** reported additional build failures from the top 400 repos suite, detailing 4 of 34 failures in xcatliu/typescript-tutorial and 4 of 9 failures in youzan/vant due to missing type definitions
 * [1.5 years ago](https://github.com/microsoft/TypeScript/pull/58638#issuecomment-2129981235) **andrewbranch** said "Lol, this might be too breaky as-is 😆 "
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#58700](https://github.com/microsoft/TypeScript/pull/58700) (Closed, `Author: Team`, `For Milestone Bug`, **andrewbranch**)

**Proposal: Prioritize declaration file resolutions when declaration extension is explicitly specified**

*Prioritize resolution of .d.ts declaration files when an import path explicitly specifies a .d.ts extension.*

 * [1.5 years ago](https://github.com/microsoft/TypeScript/pull/58700#issuecomment-2142645814) **andrewbranch** said "Yep, exactly. Could you explain how this would be useful for you? The motivation for this in #58353 is pretty narrow and specific."
 * [1.5 years ago](https://github.com/microsoft/TypeScript/pull/58700#issuecomment-2142802747) **robpalme** explained that explicit .d.ts resolution improves flexibility in custom JavaScript environments and provides escape hatches for advanced pipelines
 * [1.5 years ago](https://github.com/microsoft/TypeScript/pull/58700#issuecomment-2149431839) **robpalme** described a migration issue with verbatimModuleSyntax where index-resolution caused runtime errors, showed a type-only import workaround, and asked for a long-term solution to enforce explicit extensions in imports
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#58824](https://github.com/microsoft/TypeScript/pull/58824) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Only use resolutionStart when pushing resolution stack**

*Always use the complete resolution stack for non-circularity-checking operations instead of limiting to resolutionStart.*

 * [1.4 years ago](https://github.com/microsoft/TypeScript/pull/58824#issuecomment-2166930342) **jakebailey** provided a trace link and suggested searching for calls longer than 50ms to identify expensive operations
 * [1.4 years ago](https://github.com/microsoft/TypeScript/pull/58824#issuecomment-2166954909) **jakebailey** recovered roughly 50% of the loss by applying a single variance reset and noted that the getResolvedSignature reset comment implied it would run only once but wasn’t implemented that way
 * [1.4 years ago](https://github.com/microsoft/TypeScript/pull/58824#issuecomment-2167182340) **mikearnaldi** clarified that only Anders' PR fixed the bug and prioritized correctness over performance
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#59759](https://github.com/microsoft/TypeScript/pull/59759) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Use a trie to quickly skip templates in union creation**

*Introduce a prefix-suffix trie to efficiently skip template-literal matches and eliminate redundant string literals in union type creation.*

 * [1.2 years ago](https://github.com/microsoft/TypeScript/pull/59759#issuecomment-2310699819) **typescript-bot** reported that tsc user tests comparing main and refs/pull/59759/merge passed without issues
 * [1.2 years ago](https://github.com/microsoft/TypeScript/pull/59759#issuecomment-2310798470) **typescript-bot** posted the requested performance run results with a detailed comparison report
 * [1.2 years ago](https://github.com/microsoft/TypeScript/pull/59759#issuecomment-2310826491) **typescript-bot** reported that running the top 400 repos with tsc on main and the pull request merge yielded no errors
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#60039](https://github.com/microsoft/TypeScript/pull/60039) (Closed, `Author: Team`, `For Milestone Bug`, **andrewbranch**)

**Set impliedNodeFormat based on redirectedReference options**

*Automatically determine and assign the impliedNodeFormat from redirectedReference options during TypeScript module resolution.*

 * [1 year ago](https://github.com/microsoft/TypeScript/pull/60039#issuecomment-2515085791) **andrewbranch** said "@typescript-bot pack this"
 * [1 year ago](https://github.com/microsoft/TypeScript/pull/60039#issuecomment-2515086034) **typescript-bot** posted build status update for `pack this` job
 * [1 year ago](https://github.com/microsoft/TypeScript/pull/60039#issuecomment-2515090058) **typescript-bot** provided installable tgz with instructions for testing and shared playground and npm module links
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#60260](https://github.com/microsoft/TypeScript/pull/60260) (Closed, `Author: Team`, `For Milestone Bug`, **andrewbranch**)

**Fix codefix\-triggered auto import of aliased exports**

*Fix codefix-triggered auto-import feature to correctly resolve and import aliased exports.*

 * (1.1 years ago) **typescript-bot** added labels `Author: Team`, `For Milestone Bug`
 * [1.1 years ago](https://github.com/microsoft/TypeScript/pull/60260#issuecomment-2436366877) **andrewbranch** explained that the add-missing-members codefix lost important import metadata resulting in incorrect auto-import behavior and why extending addImportFromExportedSymbol’s signature was insufficient
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#60433](https://github.com/microsoft/TypeScript/pull/60433) (Closed, `Author: Team`, `For Uncommitted Bug`, **RyanCavanaugh**)

**Error on syntactically impossible ===s to undefined**

*Implements placeholder errors for impossible === undefined comparisons to detect and log their usage in top800*

 * [1 year ago](https://github.com/microsoft/TypeScript/pull/60433#issuecomment-2518968795) **Jack-Works** said "Can you add this case? typeof x === undefined. This one does not error and very hard to find."
 * [50 weeks ago](https://github.com/microsoft/TypeScript/pull/60433#issuecomment-2557779676) **brad4d** thanked the maintainer, noted that almost all cases were broken code, and asked if comparing undefined to a non-undefined type could ever be useful
 * [50 weeks ago](https://github.com/microsoft/TypeScript/pull/60433#issuecomment-2557997315) **Jack-Works** asked why type errors were treated differently from other non-working code
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#61450](https://github.com/microsoft/TypeScript/pull/61450) (Closed, `Author: Team`, `For Uncommitted Bug`, **RyanCavanaugh**)

**Ban non\-ambient namespaces written with \`module\` keyword**

*Assess prevalence of non-ambient namespaces declared with the module keyword and propose banning them.*

 * [37 weeks ago](https://github.com/microsoft/TypeScript/pull/61450#issuecomment-2744239008) **typescript-bot** reported that the DT test results were ready and unchanged
 * [37 weeks ago](https://github.com/microsoft/TypeScript/pull/61450#issuecomment-2744477736) **typescript-bot** provided tsc build comparison results for top GitHub repos and asked maintainers to review unexpected failures
 * [37 weeks ago](https://github.com/microsoft/TypeScript/pull/61450#issuecomment-2744530509) **RyanCavanaugh** described gl-matrix's process for building and patching index.d.ts using a custom build script
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#61608](https://github.com/microsoft/TypeScript/pull/61608) (Closed, `Author: Team`, `For Backlog Bug`, **RyanCavanaugh**)

**Check expression operand equivalence in isMatchingReference before computing property key equivalence**

*Update isMatchingReference to check expression operand equivalence before computing property key equivalence for potential optimization.*

 * [33 weeks ago](https://github.com/microsoft/TypeScript/pull/61608#issuecomment-2822642195) **typescript-bot** posted the performance run results comparing baseline and PR for tsc
 * [33 weeks ago](https://github.com/microsoft/TypeScript/pull/61608#issuecomment-2822713261) **typescript-bot** reported successful comparison results for the top 400 repos between main and the pull request merge
 * [28 weeks ago](https://github.com/microsoft/TypeScript/pull/61608#issuecomment-2911746212) **nemunemuii** said "@typescript-bot test this"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#61713](https://github.com/microsoft/TypeScript/issues/61713) (Open, `Bug`, `Help Wanted`, `Domain: lib.d.ts`)

**Missing Intl\.Locale\.prototype\.getWeekInfo\(\)**

*Intl.Locale.prototype.getWeekInfo is absent from ESNext's type definitions despite being supported in major browsers and Node.js.*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [29 weeks ago](https://github.com/microsoft/TypeScript/issues/61713#issuecomment-2888467031) **wlib** said "There's also this related PR that's been on hold https://github.com/microsoft/TypeScript/pull/58084"
 * [14 weeks ago](https://github.com/microsoft/TypeScript/issues/61713#issuecomment-3234065303) **mauroviniciussilva** said "Any updates on this issue or in the related pull request? As I've seen, the latest update on the mentioned pull request is from 2024."
 * [later](https://github.com/microsoft/TypeScript/issues/61713#issuecomment-3641060663) **json-derulo** noted that Firefox did not support the function and provided a link to the issue tracker

### [PR microsoft/TypeScript#62034](https://github.com/microsoft/TypeScript/pull/62034) (Closed, `Author: Team`, `For Milestone Bug`, **RyanCavanaugh**)

**Qualify enum member names when referencing in value position**

*Qualify enum member names in value positions to ensure correct referencing during declaration emission.*

 * (21 weeks ago) **typescript-bot** added labels `Author: Team`, `For Milestone Bug`, and assigned to **RyanCavanaugh**
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#62204](https://github.com/microsoft/TypeScript/issues/62204) (Closed, `Duplicate`)

**TypeScript falls back to generic constraint instead of inferred type when object contains function properties**

*TypeScript falls back to generic constraint instead of inferred type when object includes function properties, causing incorrect parameter inference.*

 * [15 weeks ago](https://github.com/microsoft/TypeScript/issues/62204#issuecomment-3217544689) **typescript-bot** said "This issue has been marked as "Duplicate" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (15 weeks ago) **typescript-bot** closed the issue
 * (today) **gabritto** closed the issue

### [Issue microsoft/TypeScript#62211](https://github.com/microsoft/TypeScript/issues/62211) (Closed, `Suggestion`, `Breaking Change`, `Committed`, `Fix Available`, **RyanCavanaugh**, **Copilot**)

**Deprecate, remove support for using \`module\` in place of \`namespace\`**

*TypeScript 6.0 will deprecate and error on using the module keyword for namespaces, with errors enforced by default in 7.0.*

 * (14 weeks ago) **DanielRosenwasser** assigned to **RyanCavanaugh**, **Copilot**
 * (7 weeks ago) **RyanCavanaugh** closed the issue
 * (later) **DanielRosenwasser** reopened the issue
 * **typescript-bot** added label `Fix Available`

### [PR microsoft/TypeScript#62243](https://github.com/microsoft/TypeScript/pull/62243) (Closed, `For Uncommitted Bug`)

**Improve inference by not considering thisless functions to be context\-sensitive**

*Treat object literal methods that don’t reference ‘this’ as non-context-sensitive to improve TypeScript’s type inference and fix related issues.*

 * [2 days ago](https://github.com/microsoft/TypeScript/pull/62243#issuecomment-3629464729) **jakebailey** said "The perf run shows 5 new errors in vscode; I am not sure why they are not showing up in the top or user tests..."
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/62243#issuecomment-3629485744) **Andarist** said "@jakebailey thanks for noticing, I'll look into it"
 * [yesterday](https://github.com/microsoft/TypeScript/pull/62243#issuecomment-3632609139) **Andarist** mentioned that PR #282223 should address the VS Code break and proposed a performant version of PR #57421 as a general fix, noting his local prototype was out of scope and only partial
 * [today](https://github.com/microsoft/TypeScript/pull/62243#issuecomment-3638551436) **gabritto** reported a TS2783 build error in steven-tey/novel caused by type cast and improved inference
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript#62730](https://github.com/microsoft/TypeScript/pull/62730) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**DOM update 2025\-12\-10**

*Update the DOM to include the latest changes made on December 10, 2025.*

 * [1 month ago](https://github.com/microsoft/TypeScript/pull/62730#issuecomment-3501279525) **typescript-bot** provided comparative compilation results for the top 800 repos showing build failures and changes between main and the PR
 * [1 month ago](https://github.com/microsoft/TypeScript/pull/62730#issuecomment-3518483680) **jakebailey** said "@Renegade334 Do these differences seem correct to you? I think these are a result of the change you just made."
 * [1 month ago](https://github.com/microsoft/TypeScript/pull/62730#issuecomment-3518581633) **Renegade334** noted that the top800 errors matched the ArrayBufferView assignability errors introduced in version 5.9 and were hidden by a WebSocket#send() override
 * [today](https://github.com/microsoft/TypeScript/pull/62730#issuecomment-3639604511) **jakebailey** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/62730#issuecomment-3639604624) **typescript-bot** posted build status updates for multiple test commands
 * [today](https://github.com/microsoft/TypeScript/pull/62730#issuecomment-3639659653) **typescript-bot** reported DT branch-only compile errors in the dom-navigation package
 * [today](https://github.com/microsoft/TypeScript/pull/62730#issuecomment-3639673318) **typescript-bot** ran user tests comparing main with the PR merge, noted one Git clone failure, and found everything else good
 * [today](https://github.com/microsoft/TypeScript/pull/62730#issuecomment-3639719897) **typescript-bot** posted the requested perf run results for tsc with detailed comparison metrics
 * [today](https://github.com/microsoft/TypeScript/pull/62730#issuecomment-3639794378) **typescript-bot** reported build results for top 400 repos and highlighted new TS2345 errors in microsoft/vscode comparing main and the pull request

### [PR microsoft/TypeScript#62844](https://github.com/microsoft/TypeScript/pull/62844) (Closed, `For Milestone Bug`)

**Allow subpath imports that start with \`\#/\`**

*Allow subpath imports starting with '#/' in package.json imports to mirror matching exports entries.*

 * (yesterday) **typescript-bot** added label `For Milestone Bug`, and removed label `For Uncommitted Bug`
 * (yesterday) **andrewbranch** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/62844#issuecomment-3638995505) **Scalahansolo** said "Excuse my ignorance, but for a PR like this that is marked for TS 6.0, when / what is the process for this landing in TS 7?"
 * [today](https://github.com/microsoft/TypeScript/pull/62844#issuecomment-3639169765) **RyanCavanaugh** said "Great question! It needs to be ported now. I started https://github.com/microsoft/typescript-go/pull/2330 and we'll see how that goes"

### [Issue microsoft/TypeScript#62849](https://github.com/microsoft/TypeScript/issues/62849) (Closed, `Not a Defect`)

**The existence of /// reference directives in dependencies breaks explicit typeRoots ordering**

*Dependencies using triple-slash reference directives load their type definitions before custom typeRoots, ignoring explicit typeRoots ordering.*

 * **RyanCavanaugh** added label `Needs More Info`
 * [today](https://github.com/microsoft/TypeScript/issues/62849#issuecomment-3636406132) **a-non-a-mouse** demonstrated that renaming the file to index.d.ts didn't change error behavior and argued that child projects shouldn't hijack global types
 * [today](https://github.com/microsoft/TypeScript/issues/62849#issuecomment-3636539018) **a-non-a-mouse** argued that adding a new dependency should never cause other types to break
 * [today](https://github.com/microsoft/TypeScript/issues/62849#issuecomment-3638323531) **RyanCavanaugh** clarified that TypeScript does care about file names and recommended using --traceResolution, observed different behavior, argued that child projects shouldn’t hijack global types or leak outside TypeScript itself, and rejected the invariant that adding dependencies should never break other types due to potential conflicts
 * (today) **RyanCavanaugh** added label `Not a Defect`, and removed label `Needs More Info`
 * [today](https://github.com/microsoft/TypeScript/issues/62849#issuecomment-3638906355) **a-non-a-mouse** argued that it was the same issue and advocated resolving typeRoots first to eliminate hard conflicts between globals while preserving mergeable definitions, noting that external globals should be constrained at package boundaries

### [Issue microsoft/TypeScript#62850](https://github.com/microsoft/TypeScript/issues/62850) (Closed, `Not a Defect`)

**Typescript fail to pick up error with Nullish Coalescing Operator**

*TypeScript incorrectly allows using 'something.tagsArray ?? {}' to assign an optional Tag array to a boolean map without error.*

 * [3 days ago](https://github.com/microsoft/TypeScript/issues/62850#issuecomment-3623876771) **jcalz** explained that TypeScript infers the union of an array literal and an empty object as {} and thus allows assignment to a weak object type due to missing property normalization not applying to arrays
 * **RyanCavanaugh** added label `Not a Defect`
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/62850#issuecomment-3628000323) **RyanCavanaugh** said "This is admittedly annoying, but I don't see a way to fix it without making something else substantially worse"
 * [today](https://github.com/microsoft/TypeScript/issues/62850#issuecomment-3639656792) **typescript-bot** said "This issue has been marked as "Not a Defect" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-bot** closed the issue

### [Issue microsoft/TypeScript#62853](https://github.com/microsoft/TypeScript/issues/62853) (Closed, `Duplicate`)

**Inconsistent behaviour of Record or Enum and mapped type**

*TypeScript’s Record type does not error on missing enum or const-object keys while equivalent mapped types correctly report errors.*

 * [2 days ago](https://github.com/microsoft/TypeScript/issues/62853#issuecomment-3626744322) **MartinJohns** said "Duplicate of #62796."
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/62853#issuecomment-3627388958) **jcalz** identified the duplication of issue #29698 concerning contravariance of Record<K, V>, provided a minimal example, and noted that issue #62796 was misfocused on noUncheckedIndexedAccess
 * **RyanCavanaugh** added label `Duplicate`
 * [today](https://github.com/microsoft/TypeScript/issues/62853#issuecomment-3639656705) **typescript-bot** said "This issue has been marked as "Duplicate" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-bot** closed the issue

### [Issue microsoft/TypeScript#62869](https://github.com/microsoft/TypeScript/issues/62869) (Closed, `Needs More Info`)

**\`tsserver\` checks stop updating when encountering certain \(perfectly valid\) code, basically error checking freezes**

*tsserver on a remote VS Code SSH setup freezes and stops reporting errors when encountering certain valid Remix TypeScript code.*

 * [yesterday](https://github.com/microsoft/TypeScript/issues/62869#issuecomment-3634876097) **Semmu** mentioned finding the root cause and provided diagnostic logs and exception stack trace
 * [yesterday](https://github.com/microsoft/TypeScript/issues/62869#issuecomment-3635182352) **Semmu** resolved the issue by simplifying branded string type definitions to avoid self-referencing, confirmed tsserver no longer errored, provided before/after code snippets and helpful resources, and suggested closing the issue
 * (yesterday) **Semmu** closed the issue
 * [today](https://github.com/microsoft/TypeScript/issues/62869#issuecomment-3638349586) **RyanCavanaugh** said "That's a legitimate TS bug; if you can boil this down to a reproducible example we'd be interested to fix it. Thanks!"
 * [today](https://github.com/microsoft/TypeScript/issues/62869#issuecomment-3639295633) **Semmu** said "Ohh, in that case I will try to create a PoC repo!"
 * [today](https://github.com/microsoft/TypeScript/issues/62869#issuecomment-3639512384) **Semmu** provided a minimal TypeScript snippet that caused tsserver to exceed call stack due to recursive branded type instantiation
 * [today](https://github.com/microsoft/TypeScript/issues/62869#issuecomment-3639517265) **Semmu** said "Also it only happens if both types are self-referencing. Changing one of them is enough to circumvent this bug."

### [Issue microsoft/TypeScript#62870](https://github.com/microsoft/TypeScript/issues/62870) (Open, `Bug`, `Help Wanted`, `Domain: Decorators`)

**ES  \`ClassDecoratorContext\.name\` has incorrect value with static \`name\`**

*ClassDecoratorContext.name returns the static name property's value instead of the actual class name literal.*

 * (yesterday) **RyanCavanaugh** added labels `Help Wanted`, `Domain: Decorators`, and set milestone to `Backlog`
 * [later](https://github.com/microsoft/TypeScript/issues/62870#issuecomment-3641999947) **sAchin-680** asked to be assigned, offered to open a PR, and identified that the issue came from using renamedClassThis.name invoking the user-defined getter instead of the literal class name

### [PR microsoft/TypeScript#62873](https://github.com/microsoft/TypeScript/pull/62873) (Closed, `For Uncommitted Bug`)

**ES2020: fix String\.prototype\.matchAll type and description**

*Correct the TypeScript type definitions and documentation for ES2020’s String.prototype.matchAll method.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/62873#issuecomment-3634372909) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [yesterday](https://github.com/microsoft/TypeScript/pull/62873#issuecomment-3634372940) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [yesterday](https://github.com/microsoft/TypeScript/pull/62873#issuecomment-3634399398) **typescript-bot** said "The TypeScript team hasn't accepted the linked issue #55843. If you can get it accepted, this PR will have a better chance of being reviewed."
 * [today](https://github.com/microsoft/TypeScript/pull/62873#issuecomment-3639384957) **DanielRosenwasser** said "v6 will be in TS, v7 will be the Go-based implementation."
 * [today](https://github.com/microsoft/TypeScript/pull/62873#issuecomment-3639401039) **ljharb** said "phew, thanks :-)"

### [PR microsoft/TypeScript#62875](https://github.com/microsoft/TypeScript/pull/62875) (Closed, `For Uncommitted Bug`)

**Allow const JSON imports with type narrowing**

*Allow JSON imports marked with const to be treated as literal types for type narrowing.*

 * **typescript-bot** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/62875#issuecomment-3637407735) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [today](https://github.com/microsoft/TypeScript/pull/62875#issuecomment-3637768927) **hnakrapunt** said "@microsoft-github-policy-service agree company="NVIDIA""
 * (today) **hnakrapunt** closed the issue

### [PR microsoft/TypeScript#62876](https://github.com/microsoft/TypeScript/pull/62876) (Closed, `Author: Team`, `For Milestone Bug`, **RyanCavanaugh**)

**Deprecate \`module\` syntax**

*Deprecate and error on all ‘module’ and ‘declare module’ syntax forms in TypeScript*

 * created by **RyanCavanaugh**
 * (today) **typescript-bot** added labels `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`, and assigned to **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript/pull/62876#issuecomment-3639235208) **RyanCavanaugh** said "@typescript-bot test top800"
 * [today](https://github.com/microsoft/TypeScript/pull/62876#issuecomment-3639235404) **typescript-bot** provided a build status update for test top800
 * [today](https://github.com/microsoft/TypeScript/pull/62876#issuecomment-3639573914) **typescript-bot** reported that everything looked good after running tsc on the top 800 repos comparing main and the pull request
 * (later) **typescript-bot** added label `For Milestone Bug`, and removed label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/62876#issuecomment-3640806500) **DanielRosenwasser** said "@typescript-bot pack this"
 * [later](https://github.com/microsoft/TypeScript/pull/62876#issuecomment-3640806861) **typescript-bot** reported build jobs starting and provided status links
 * [later](https://github.com/microsoft/TypeScript/pull/62876#issuecomment-3640821944) **typescript-bot** provided an installable tgz and testing instructions along with playground and npm module links
 * [later](https://github.com/microsoft/TypeScript/pull/62876#issuecomment-3641045349) **robpalme** thanked the author for the pack and reported that provoking the intended checker error crashed the compiler, including a StackBlitz link and the error message

### [PR microsoft/TypeScript#62878](https://github.com/microsoft/TypeScript/pull/62878) (Closed, `For Backlog Bug`)

**Reorder Array\#reduce overloads for better type inference**

*Reorder Array#reduce and reduceRight overloads to ensure proper inference of generic initial value types in TypeScript.*

 * created by **majiayu000**
 * **typescript-bot** added label `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/62878#issuecomment-3640377376) **majiayu000** said "Closing this PR as the implementation needs further review. The JSDoc comments were not properly moved with their corresponding function overloads. Will resubmit after proper analysis."
 * (today) **majiayu000** closed the issue

### [PR microsoft/TypeScript#62879](https://github.com/microsoft/TypeScript/pull/62879) (Closed, `For Backlog Bug`)

**Reorder Array\#reduce overloads for better type inference**

*Swap generic and non-generic overload order for Array#reduce to restore correct type inference when initialValue is assignable to element type.*

 * created by **majiayu000**
 * **typescript-bot** added label `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/62879#issuecomment-3640555626) **majiayu000** said "Closing this PR due to incomplete baseline updates. The change requires updating 24+ test baseline files, which wasn't fully addressed. Thank you for reviewing."
 * (today) **majiayu000** closed the issue

### [Issue microsoft/TypeScript#62880](https://github.com/microsoft/TypeScript/issues/62880) (Open, `Needs Investigation`, **andrewbranch**)

**subpath imports should play well with project references**

*TypeScript project references misinterpret Node.js subpath imports like '#bob/module' as internal files, causing TS6307 build errors.*

 * created by **valler**

### [Issue microsoft/TypeScript#62881](https://github.com/microsoft/TypeScript/issues/62881) (Closed, `7.0 LS Migration`)

**unactionable warning: All type parameters are unused\. \(6205\)**

*Declaration merging to extend ColumnMeta with unused type parameter TData triggers warning 6205 and results in conflicting declarations.*

 * created by **jendrikw**

