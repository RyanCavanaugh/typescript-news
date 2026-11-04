# Report for 2026-11-02 (Monday, November 2nd, 2026)

23 different users commented on 97 different issues.

## Recommended Actions

 * Response Recommended
    * @michael42 described a cross-device link error and suggested catching EXDEV in the error handling in [microsoft/TypeScript#63646](https://github.com/microsoft/TypeScript/issues/63646#issuecomment-6586830701)
    * @adalinesimonian asked if Yarn PnP could use package maps with zip paths and whether TypeScript only needs zip support, or if Yarn's approach is incompatible with Node.js package maps in [microsoft/TypeScript#63919](https://github.com/microsoft/TypeScript/pull/63919#issuecomment-6599471936)
    * @tim-smart provided repro steps for breaking change in [microsoft/TypeScript#64656](https://github.com/microsoft/TypeScript/issues/64656#issuecomment-6589749709)
    * @tim-smart provided repro steps and details for the regression affecting the Effect library in [microsoft/TypeScript#64673](https://github.com/microsoft/TypeScript/issues/64673#issuecomment-6590090051)
    * @MadalinWolf asked for a review of the addressed issues in [microsoft/TypeScript#64949](https://github.com/microsoft/TypeScript/pull/64949#issuecomment-6608582702)
    * @timurzvural provided additional repro steps for the unsoundness issue in [microsoft/TypeScript#65052](https://github.com/microsoft/TypeScript/issues/65052#issuecomment-6601443980)
    * @loopingz suggested adding a user option for additional SQL query validation in [microsoft/TypeScript#65092](https://github.com/microsoft/TypeScript/issues/65092#issuecomment-6590654364)
    * @beefstew asked whether an additional Microsoft EULA applies to the npm distribution and clarification on Background Sync report, version, and attribution applicability in [microsoft/TypeScript#65096](https://github.com/microsoft/TypeScript/issues/65096#issuecomment-6583601937)
    * @SegaraRai provided detailed analysis and repro steps of console behavior in [microsoft/TypeScript#65102](https://github.com/microsoft/TypeScript/pull/65102#issuecomment-6586284637)
    * @timurzvural provided reproduction steps for the native≠classic failure in [microsoft/TypeScript#65127](https://github.com/microsoft/TypeScript/issues/65127#issuecomment-6598730391)
    * @timurzvural reported false diagnostics on content-mapped virtual .mts files under verbatimModuleSyntax in [microsoft/TypeScript#65135](https://github.com/microsoft/TypeScript/issues/65135#issuecomment-6597862392)
    * @timurzvural provided repro steps illustrating additional silent cases in [microsoft/TypeScript#65137](https://github.com/microsoft/TypeScript/issues/65137#issuecomment-6597989774)
    * @timurzvural reported important information about a silent emission issue with exported binding patterns in [microsoft/TypeScript#65137](https://github.com/microsoft/TypeScript/issues/65137#issuecomment-6598059124)
    * @timurzvural provided an example of the omission in [microsoft/TypeScript#65143](https://github.com/microsoft/TypeScript/issues/65143#issuecomment-6598669391)
    * @timurzvural provided a repro example and detailed explanation in [microsoft/TypeScript#65148](https://github.com/microsoft/TypeScript/issues/65148#issuecomment-6599096865)
    * @timurzvural reported a broader LS display/completion issue with JSDoc @param types and provided repro steps in [microsoft/TypeScript#65167](https://github.com/microsoft/TypeScript/issues/65167#issuecomment-6601366789)
    * @timurzvural provided reproduction steps for signature help discrepancy in [microsoft/TypeScript#65167](https://github.com/microsoft/TypeScript/issues/65167#issuecomment-6601386952)
    * @hkleungai suggested updating change.md to explicitly deprecate prototype-style methods in [microsoft/TypeScript#65172](https://github.com/microsoft/TypeScript/issues/65172#issuecomment-6602664732)
    * @timurzvural provided a detailed matrix of TypeScript error codes for with/assert imports in [microsoft/TypeScript#65174](https://github.com/microsoft/TypeScript/issues/65174#issuecomment-6602405240)

## Activity Summary

### [Issue microsoft/TypeScript#60913](https://github.com/microsoft/TypeScript/issues/60913) (Open, `Needs Investigation`, **weswigham**)

**\`\./\*\.d\.ts\` required in \`exports\` to avoid \`Cannot be named without a reference to\.\.\. not portable\.\.\.\`**

*Requiring explicit .d.ts exports in package.json to prevent TS 'not portable' errors inadvertently exposes declaration files.*

 * [1 year ago](https://github.com/microsoft/TypeScript/issues/60913#issuecomment-3391374216) **weswigham** explained that TypeScript reduces some types when not visible but treats distributive types like mapped and conditional types as irreducible, so inlining can change behavior and supporting a loosening carve-out is complex
 * [1 year ago](https://github.com/microsoft/TypeScript/issues/60913#issuecomment-3392515574) **ethanresnick** asked about the difference between irreducible and not inlinable types and why TS didn’t fully evaluate bound types before declaration emit
 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/60913#issuecomment-6175793428) **sindresorhus** explained a minimal reproduction of a TypeScript type alias loss issue from a library author perspective and asked if a fallback could preserve the original alias
 * [today](https://github.com/microsoft/TypeScript/issues/60913#issuecomment-6591398131) **jakebailey** said "At least some of the above is handled by #64751/#64752, InlineDeep yes, HelperDeep no."

### [Issue microsoft/TypeScript#63223](https://github.com/microsoft/TypeScript/issues/63223) (Closed, `Bug`, `Domain: flag: isolatedDeclarations`)

**Toggling \`isolatedModules\` in \`tsconfig\.json\` while running the compiler in \`watch\` mode, doesn't re\-emit \`const enums\`, unlike toggling \`preserveConstEnums\`, which does**

*Unlike preserveConstEnums toggles, changing isolatedModules in watch mode does not re-emit const enums until a full rebuild.*

 * (33 weeks ago) **RyanCavanaugh** added labels `Bug`, `Domain: flag: isolatedDeclarations`, and set milestone to `Backlog`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#63646](https://github.com/microsoft/TypeScript/issues/63646) (Closed, `Needs Investigation`, **johnfav03**)

**tsc \-\-watch does not work in docker**

*tsc --watch fails to detect file changes in Docker bind-mounted workspaces on macOS after upgrading to version 7.0.2.*

 * (12 weeks ago) **johnfav03** closed the issue
 * [11 weeks ago](https://github.com/microsoft/TypeScript/issues/63646#issuecomment-5287274144) **danyreyna** said "Thank you for the prompt fix @johnfav03, but will it be available until v7.1?"
 * [11 weeks ago](https://github.com/microsoft/TypeScript/issues/63646#issuecomment-5287292595) **jakebailey** said "We have yet to discuss 7.0 patches (focusing on moving the code back to this repo and then reenabling releasing) but I would suspect this would be on the table"
 * [today](https://github.com/microsoft/TypeScript/issues/63646#issuecomment-6586830701) **michael42** described a virtiofs cross-device link error when using fanotify_mark for parent directories and suggested catching EXDEV to fix it
 * [today](https://github.com/microsoft/TypeScript/issues/63646#issuecomment-6590624808) **jakebailey** said "@michael42 This issue has closed; have you tried a 7.1 nightly?"

### [PR microsoft/TypeScript#63919](https://github.com/microsoft/TypeScript/pull/63919) (Open, `For Uncommitted Bug`)

**Add Yarn PnP module resolution support**

*Add native Yarn Plug’n’Play module resolution support to TypeScript Go, including PnP VFS, API, and manifest handling.*

 * [1 month ago](https://github.com/microsoft/TypeScript/pull/63919#issuecomment-5928111641) **futursolo** suggested using the Node.js API's resolve source code content feature to avoid implementing zip file system
 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/63919#issuecomment-6182431945) **louisscruz** asked about optional Yarn PnP support via a compiler flag and asked @arcanis for a path to Yarn + TypeScript package map support
 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/63919#issuecomment-6186919893) **arcanis** opened issue #64827 to start a discussion about package map support in Yarn + TypeScript
 * [later](https://github.com/microsoft/TypeScript/pull/63919#issuecomment-6599471936) **adalinesimonian** asked if Yarn PnP could use package maps to point to zip archive paths and if TypeScript would only need to support zip paths for PnP, or if Yarn's approach is incompatible with Node.js package maps

### [PR microsoft/TypeScript#64108](https://github.com/microsoft/TypeScript/pull/64108) (Closed, `Author: Team`, `For Uncommitted Bug`, **RyanCavanaugh**, **Copilot**)

**Fix call hierarchy file node paths**

*Display file basenames with project-relative directories in call hierarchy nodes instead of absolute file paths.*

 * [2 days ago](https://github.com/microsoft/TypeScript/pull/64108#issuecomment-6542437743) **jakebailey** said "@copilot+gpt-6.1-sol merge main and do better per the above"
 * **typescript-automation[bot]** added label `Author: Team`
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/64108#issuecomment-6542774931) **Copilot** merged main and updated call hierarchy to use initialized workspace folders with typed paths, noted build, tests, lint, and format passed but CodeQL was blocked by a Git diff timeout
 * [today](https://github.com/microsoft/TypeScript/pull/64108#issuecomment-6591918806) **jakebailey** said "I don't hate it. @andrewbranch Do you have any feelings about this?"

### [Issue microsoft/TypeScript#64605](https://github.com/microsoft/TypeScript/issues/64605) (Closed, `Needs Investigation`, **gabritto**)

**TS5115 in published Zod 4\.5–4\.6 types after \#64372**

*Zod 4.5.0–4.6.5 z.json() types cause TS5115 infinite circularity errors in TypeScript 7.1 nightlies after PR #64372, impacting ~62M weekly downloads.*

 * [1 week ago](https://github.com/microsoft/TypeScript/issues/64605#issuecomment-6426420558) **ebidel** demonstrated that postcss-selector-parser's type definitions still produced TS5115 infinite circular instantiation errors in recent builds and provided reproduction steps and build comparisons
 * [4 days ago](https://github.com/microsoft/TypeScript/issues/64605#issuecomment-6504485324) **jakebailey** said "@ebidel Anders posted a change that fixes that package, was it missed?: https://github.com/microsoft/TypeScript/pull/64372#issuecomment-5804602336"
 * [4 days ago](https://github.com/microsoft/TypeScript/issues/64605#issuecomment-6505184494) **jakebailey** said "I think the thing we don't get is why someone would update to TS 7.1, but then not also be updating zod or a transitive dep on zod?"
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript#64656](https://github.com/microsoft/TypeScript/issues/64656) (Open, `Needs Investigation`, **weswigham**)

**Declaration emit errors \(TS5088\) on anonymous cyclic types that 6\.0 elided to \`any\`**

*TypeScript 7’s declaration emitter now errors on anonymous cyclic types instead of eliding them to any, causing breaking changes.*

 * (3 weeks ago) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.1.1 RC`, and assigned to **weswigham**
 * [today](https://github.com/microsoft/TypeScript/issues/64656#issuecomment-6589749709) **tim-smart** provided a reproduction demonstrating that TypeScript 7.1 errors on a cyclic type where 7.0 emitted any
 * [today](https://github.com/microsoft/TypeScript/issues/64656#issuecomment-6590783155) **jakebailey** said "My opinion is that any implicit any we emitted but didn't say anything about is wrong, hence #64461, though it's a little annoying it didn't come up in our extended test suite. "
 * [today](https://github.com/microsoft/TypeScript/issues/64656#issuecomment-6591262979) **jakebailey** said "I am however curious if #64751 + #64752 fix the issues noted here. I haven't tested yet."
 * [today](https://github.com/microsoft/TypeScript/issues/64656#issuecomment-6591332401) **jakebailey** said "Ah yep, I just checked, and both of your issues are solved by that stack!"

### [PR microsoft/TypeScript#64658](https://github.com/microsoft/TypeScript/pull/64658) (Open, `Author: Team`, `For Uncommitted Bug`, **DanielRosenwasser**, **Copilot**)

**Fix Windows module resolution for reserved path segments**

*Use extended path namespaces to prevent Windows reserved device names like con from blocking module resolution.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript/pull/64658#issuecomment-6070559076) **Copilot** fixed the Windows short-path expectation, removed t.Parallel() from the allocation test, and adjusted cleanup to satisfy custom lint
 * [3 weeks ago](https://github.com/microsoft/TypeScript/pull/64658#issuecomment-6070609937) **jakebailey** said "I don't think you can just remove Parallel without a nolint directive that says why"
 * [today](https://github.com/microsoft/TypeScript/pull/64658#issuecomment-6572393641) **itrapashko** asked DanielRosenwasser to review the outstanding nolint directive note still affecting Windows
 * [today](https://github.com/microsoft/TypeScript/pull/64658#issuecomment-6589252621) **jakebailey** said "@copilot+gpt-6.1-sol see thread above; fix so windows lint will pass correctly"
 * **typescript-automation[bot]** added label `Author: Team`
 * [today](https://github.com/microsoft/TypeScript/pull/64658#issuecomment-6589531201) **Copilot** restored t.Parallel() on the reserved-component behavior test and moved testing.AllocsPerRun to a separate non-parallel test with a paralleltest suppression

### [Issue microsoft/TypeScript#64673](https://github.com/microsoft/TypeScript/issues/64673) (Open, `Needs Investigation`, **ahejlsberg**)

**TS2719 "Two different types with this name exist" between identical generic signatures with a distributive conditional parameter type \(regression from \#64237\)**

*After commit #64237, TypeScript wrongly reports TS2719 for identical generic signatures using distributive conditional types.*

 * (3 weeks ago) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.1.1 RC`, and assigned to **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript/issues/64673#issuecomment-6590090051) **tim-smart** demonstrated a regression in the Effect TypeScript library by providing a repro that triggers TS2719 errors on specific versions

### [PR microsoft/TypeScript#64682](https://github.com/microsoft/TypeScript/pull/64682) (Closed, `For Backlog Bug`)

**Report strict\-mode errors for class names eval and arguments**

*Report TS1210 strict-mode errors for class declarations and expressions named 'eval' or 'arguments' during binding.*

 * (3 weeks ago) **typescript-automation[bot]** added labels `For Backlog Bug`, `For Backlog Bug`
 * [3 weeks ago](https://github.com/microsoft/TypeScript/pull/64682#issuecomment-6055636297) **dmety** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript/pull/64682#issuecomment-6589280417) **jakebailey** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/64682#issuecomment-6589282610) **typescript-automation[bot]** reported CI job statuses for various commands with links to build results
 * [today](https://github.com/microsoft/TypeScript/pull/64682#issuecomment-6589959055) **typescript-automation[bot]** notified that the results of running the DT tests were ready, indicated everything looked the same, and provided a link to the log
 * [today](https://github.com/microsoft/TypeScript/pull/64682#issuecomment-6590034331) **typescript-automation[bot]** reported tsc user test results and confirmed everything looked good
 * [today](https://github.com/microsoft/TypeScript/pull/64682#issuecomment-6590279722) **typescript-automation[bot]** provided the results of the requested performance run
 * [today](https://github.com/microsoft/TypeScript/pull/64682#issuecomment-6591057613) **typescript-automation[bot]** reported that running the top 400 repos tsc comparison between baseline and pr succeeded without issues

### [PR microsoft/TypeScript#64688](https://github.com/microsoft/TypeScript/pull/64688) (Closed, `For Milestone Bug`, **gabritto**)

**Read a type's declared members while its base types resolve**

*Modify resolveObjectTypeMembers to preserve a type's declared members during base type resolution to prevent infinite recursion when resolving self-declared properties.*

 * (3 weeks ago) **typescript-automation[bot]** added label `For Milestone Bug`, and assigned to **gabritto**
 * [3 weeks ago](https://github.com/microsoft/TypeScript/pull/64688#issuecomment-6055991306) **RedesignedRobot** said "@microsoft-github-policy-service agree"
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript#64695](https://github.com/microsoft/TypeScript/pull/64695) (Open, `Domain: Performance`, `For Milestone Bug`, `For Backlog Bug`, **ahejlsberg**)

**\[experiment\] Skip incompatible discriminants when inferring**

*Add experimental logic to skip incompatible discriminants during discriminated union type inference to reduce inference work.*

 * [4 days ago](https://github.com/microsoft/TypeScript/pull/64695#issuecomment-6500291770) **jakebailey** said "@typescript-bot perf test this faster"
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/64695#issuecomment-6500294727) **typescript-automation[bot]** started jobs and updated status table with build links
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/64695#issuecomment-6501621156) **typescript-automation[bot]** posted the requested perf run results
 * [today](https://github.com/microsoft/TypeScript/pull/64695#issuecomment-6586425536) **weswigham** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/64695#issuecomment-6586427794) **typescript-automation[bot]** reported build jobs start and status with links
 * [today](https://github.com/microsoft/TypeScript/pull/64695#issuecomment-6587495913) **typescript-automation[bot]** said "@weswigham, the perf run you requested failed. You can check the log here."
 * [today](https://github.com/microsoft/TypeScript/pull/64695#issuecomment-6587893562) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/64695#issuecomment-6587895644) **typescript-automation[bot]** started CI perf test jobs and posted build status and results links
 * [today](https://github.com/microsoft/TypeScript/pull/64695#issuecomment-6588948856) **typescript-automation[bot]** reported the performance comparison results between baseline and PR as requested
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64695#issuecomment-6598167877) **Andarist** noted that the table results were skewed by the inclusion of another optimization in the PR

### [PR microsoft/TypeScript#64712](https://github.com/microsoft/TypeScript/pull/64712) (Closed, `Author: Team`, `For Backlog Bug`, **jakebailey**)

** Fix compiler option invalidation in incremental builds**

*Audit and fix incorrect incremental build invalidation for compiler options, build-info persistence, global file ordering, and deletions.*

 * (3 weeks ago) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/64712#issuecomment-6525329437) **RyanCavanaugh** said "ping @johnfav03"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64732](https://github.com/microsoft/TypeScript/pull/64732) (Closed, `For Backlog Bug`)

**Fix inline JSDoc links in optional type positions**

*Ensure inline link, linkcode, and linkplain tags after @throws and @returns are parsed as links instead of type expressions.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript/pull/64732#issuecomment-6131105060) **typescript-automation[bot]** reported tsc user test results and confirmed everything looked good
 * [3 weeks ago](https://github.com/microsoft/TypeScript/pull/64732#issuecomment-6131812308) **typescript-automation[bot]** reported that running the top 400 repos tsc comparison between baseline and pr succeeded without issues
 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/64732#issuecomment-6264594274) **mbarinov** said "Hi @jakebailey, thanks for running the additional tests. Do you have any feedback or additional checks you'd like me to run before this is ready to merge?"
 * [today](https://github.com/microsoft/TypeScript/pull/64732#issuecomment-6589191750) **jakebailey** suggested rebasing on main and splitting into separate test and fix commits
 * [later](https://github.com/microsoft/TypeScript/pull/64732#issuecomment-6608048340) **mbarinov** rebased the branch onto main and split the changes into two commits as requested

### [PR microsoft/TypeScript#64751](https://github.com/microsoft/TypeScript/pull/64751) (Open, `Author: Team`, `For Backlog Bug`, **jakebailey**)

**Unify recursive type naming during serialization**

*Centralize recursive type naming during serialization to ensure consistent emitted declarations and prevent any fallback to `any`*

 * (3 weeks ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`

### [PR microsoft/TypeScript#64752](https://github.com/microsoft/TypeScript/pull/64752) (Open, `Author: Team`, `For Milestone Bug`, `For Backlog Bug`, **jakebailey**)

**Bind anonymous recursive types during declaration serialization**

*Emit private type aliases for anonymous recursive types to avoid failures in declaration file emission.*

 * (3 weeks ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **typescript-automation[bot]** added labels `For Backlog Bug`, `For Milestone Bug`, and removed label `For Uncommitted Bug`

### [Issue microsoft/TypeScript#64943](https://github.com/microsoft/TypeScript/issues/64943) (Open, `Bug`, `Domain: Content Mappers`)

**File changed on disk with a content\-mapped or \`\.d\.ts\` extension never triggers workspace/diagnostic/refresh**

*Modifying disk files with content-mapped or .d.ts extensions fails to trigger diagnostic refresh notifications in the TypeScript server*

 * created by **mrlubos**
 * (today) **RyanCavanaugh** added labels `Bug`, `Domain: Content Mappers`, and set milestone to `Backlog`

### [PR microsoft/TypeScript#64944](https://github.com/microsoft/TypeScript/pull/64944) (Open, `For Backlog Bug`)

**Refresh diagnostics when a content\-mapped or declaration file changes on disk**

*Ensure diagnostics are refreshed when content-mapped or .d.ts files change on disk, correcting path.Extension misdetection*

 * (1 week ago) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64944#issuecomment-6374657128) **mrlubos** said "@microsoft-github-policy-service agree company="Hey API""
 * (today) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`

### [PR microsoft/TypeScript#64949](https://github.com/microsoft/TypeScript/pull/64949) (Open, `For Backlog Bug`)

**Fix signature help docs for const function types**

*Add fallback documentation lookup so JSDoc comments on const function type annotations appear in signature help.*

 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64949#issuecomment-6382102547) **MadalinWolf** said "@microsoft-github-policy-service agree"
 * (1 week ago) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/64949#issuecomment-6608582702) **MadalinWolf** requested a review after addressing overload precedence, aliased imports, and @param docs issues with regression tests

### [PR microsoft/TypeScript#64982](https://github.com/microsoft/TypeScript/pull/64982) (Closed, `For Backlog Bug`)

**erase decorated abstract properties under experimentalDecorators with define semantics**

*Prevent decorated abstract class properties from emitting instance fields under experimentalDecorators with useDefineForClassFields.*

 * (6 days ago) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Backlog Bug`, and removed label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64982#issuecomment-6589155506) **jakebailey** said "Ideally this would be two commits, one that adds the test and "bad" baselines, then a second commit that shows the fix plus baseline update"
 * [today](https://github.com/microsoft/TypeScript/pull/64982#issuecomment-6594506148) **1-DARK** said " Hi @jakebailey,  done. Split into two commits: the first adds the tests with the current (bad) baselines, and the second contains the fix plus the baseline diff."

### [Issue microsoft/TypeScript#64987](https://github.com/microsoft/TypeScript/issues/64987) (Closed, `Won't Fix`)

**LSP: newly created file is assigned to the wrong project when the project path contains '\[' / '{' \(or include differs only by case\)**

*Newly created files under directories with square brackets or case-insensitive name differences are assigned to the wrong TypeScript project.*

 * created by **1-DARK**
 * [5 days ago](https://github.com/microsoft/TypeScript/issues/64987#issuecomment-6473611408) **jakebailey** asked if the reporter personally encountered the bug or used an AI agent to find it
 * [5 days ago](https://github.com/microsoft/TypeScript/issues/64987#issuecomment-6473912586) **1-DARK** reproduced the issue end-to-end with the tsgo LSP binary in bracketed directories, observed a false TS2550 error, and offered a repro script while noting it may be an edge case
 * **RyanCavanaugh** added label `Won't Fix`
 * [today](https://github.com/microsoft/TypeScript/issues/64987#issuecomment-6586362694) **RyanCavanaugh** said "We're not in some kind of critical bug shortage here; please prioritize your agents toward useful work."
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#64991](https://github.com/microsoft/TypeScript/issues/64991) (Open, `Bug`, `Domain: API`)

**\`typescript/sync\`: tuples and type literals from \`checker\.typeToTypeNode\` print multi\-line \(SingleLine flag lost\)**

*With TypeScript/sync 7.1.0-dev, checker.typeToTypeNode prints tuple and object type literals as multi-line nodes, losing single-line formatting.*

 * created by **todor-a**
 * (today) **RyanCavanaugh** added labels `Bug`, `Domain: API`, and set milestone to `Backlog`

### [PR microsoft/TypeScript#64993](https://github.com/microsoft/TypeScript/pull/64993) (Open, `For Backlog Bug`)

**Drop statements a top\-level await reparse consumed to the end of the file**

*Prevent top-level await reparsing from copying original statements past EOF to avoid overlapping parsed statements.*

 * created by **roninjin10**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [5 days ago](https://github.com/microsoft/TypeScript/pull/64993#issuecomment-6481192897) **roninjin10** said "@microsoft-github-policy-service agree company="Tevm Inc""
 * (today) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`

### [Issue microsoft/TypeScript#64999](https://github.com/microsoft/TypeScript/issues/64999) (Open, `Bug`, `Domain: Parser`)

**Top\-level await reparse keeps statements it already consumed when it reaches the end of the file**

*TypeScript's top-level await reparse retains already consumed statements at file end, causing overlapping parse nodes.*

 * created by **roninjin10**
 * (today) **RyanCavanaugh** added labels `Bug`, `Domain: Parser`, and set milestone to `Backlog`

### [PR microsoft/TypeScript#65003](https://github.com/microsoft/TypeScript/pull/65003) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Report process CPU time in extended diagnostics**

*Add reporting of process CPU time in extended diagnostics to capture actual CPU usage by the process.*

 * [2 days ago](https://github.com/microsoft/TypeScript/pull/65003#issuecomment-6551774401) **jakebailey** said "@typescript-bot perf test this faster"
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/65003#issuecomment-6551775234) **typescript-automation[bot]** announced starting jobs and provided build status and results links
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/65003#issuecomment-6552261464) **typescript-automation[bot]** posted perf run results showing no significant changes between baseline and PR across metrics like errors, symbols, types, and memory usage
 * [today](https://github.com/microsoft/TypeScript/pull/65003#issuecomment-6585897765) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/65003#issuecomment-6585901091) **typescript-automation[bot]** initiated performance test jobs and posted status links
 * [today](https://github.com/microsoft/TypeScript/pull/65003#issuecomment-6587007213) **typescript-automation[bot]** provided the requested perf run results
 * [today](https://github.com/microsoft/TypeScript/pull/65003#issuecomment-6587698349) **jakebailey** said "Sadly this does not seem to be worth it. Ideally instruction count is what I'd choose but..."
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#65052](https://github.com/microsoft/TypeScript/issues/65052) (Closed)

**7\.0 regression: inherited members are sorted by position, so an empty subinterface changes assignability**

*TypeScript 7.0 regresses interface assignability by sorting inherited members by position, wrongly allowing assignments in empty subinterfaces.*

 * created by **pearofducks**
 * [later](https://github.com/microsoft/TypeScript/issues/65052#issuecomment-6601443980) **timurzvural** provided additional examples triggering the empty-extends/shared-member-layout unsoundness in abstract classes and interfaces

### [PR microsoft/TypeScript#65056](https://github.com/microsoft/TypeScript/pull/65056) (Open, `Domain: Performance`, `For Uncommitted Bug`)

**Avoid resolving property types that cannot be unit types when looking for key properties**

*Prevent resolution of property types that cannot be unit types when searching for key properties.*

 * **jakebailey** added label `Domain: Performance`
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/65056#issuecomment-6527601543) **typescript-automation[bot]** reported the results of the requested perf run including metrics for errors, symbols, types, memory usage, and allocations
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/65056#issuecomment-6528497241) **typescript-automation[bot]** reported that running the top 400 repos tsc comparison between baseline and pr succeeded without issues
 * [today](https://github.com/microsoft/TypeScript/pull/65056#issuecomment-6581967151) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [today](https://github.com/microsoft/TypeScript/pull/65056#issuecomment-6585902636) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/65056#issuecomment-6585906227) **typescript-automation[bot]** announced that it started performance tests and would update as builds complete
 * [today](https://github.com/microsoft/TypeScript/pull/65056#issuecomment-6587585715) **typescript-automation[bot]** provided the requested performance run results

### [PR microsoft/TypeScript#65059](https://github.com/microsoft/TypeScript/pull/65059) (Closed, `Author: Team`, `For Milestone Bug`, **ahejlsberg**, **gabritto**)

**Allow accessing named declared members during a type's resolution**

*Enable accessing both declared and inherited named members during lazy type resolution*

 * [3 days ago](https://github.com/microsoft/TypeScript/pull/65059#issuecomment-6536525512) **typescript-automation[bot]** provided performance run results to @ahejlsberg
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/65059#issuecomment-6537056606) **typescript-automation[bot]** reported successful tsc comparison between baseline and pr on the top 400 repos
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/65059#issuecomment-6544531196) **ahejlsberg** said "No effects on performance and all tests are clear. I think this one is good to go."
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript#65061](https://github.com/microsoft/TypeScript/pull/65061) (Open, `Domain: Performance`, `For Uncommitted Bug`)

**Speed up \`removeSubtypes\` by looking up each target's key property type once per key property name**

*Optimize removeSubtypes to improve performance by caching each key property type per property name.*

 * **jakebailey** added label `Domain: Performance`
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/65061#issuecomment-6530887553) **typescript-automation[bot]** provided the results of the requested performance run
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/65061#issuecomment-6541174030) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [today](https://github.com/microsoft/TypeScript/pull/65061#issuecomment-6589534571) **jakebailey** said "This seems pretty good to me? @ahejlsberg "

### [PR microsoft/TypeScript#65062](https://github.com/microsoft/TypeScript/pull/65062) (Open, `For Backlog Bug`)

**Preserve single\-line emit hints for nodes returned by the API**

*Extend the TypeScript API to serialize and preserve single-line emit hints in node flags for accurate single-line printing.*

 * created by **1-DARK**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (today) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`

### [PR microsoft/TypeScript#65070](https://github.com/microsoft/TypeScript/pull/65070) (Open, `For Backlog Bug`)

**fix\(65069\): preserve contextual types for array\-destructured parameter defaults**

*Ensure that array-destructured function parameters with default empty arrays retain their contextual tuple types by only padding missing elements when no contextual type is present.*

 * created by **timurzvural**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (today) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/65070#issuecomment-6591976716) **RyanCavanaugh** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/65070#issuecomment-6591978549) **typescript-automation[bot]** posted automated CI build job statuses with results and links
 * [today](https://github.com/microsoft/TypeScript/pull/65070#issuecomment-6592453846) **typescript-automation[bot]** reported that the DT test results were ready and unchanged
 * [today](https://github.com/microsoft/TypeScript/pull/65070#issuecomment-6592543087) **typescript-automation[bot]** reported that everything looked good after running user tests with tsc comparing baseline and pr
 * [today](https://github.com/microsoft/TypeScript/pull/65070#issuecomment-6592747094) **typescript-automation[bot]** provided the requested performance run results
 * [today](https://github.com/microsoft/TypeScript/pull/65070#issuecomment-6593418913) **typescript-automation[bot]** reported that the tsc comparison of the top 400 repos between baseline and PR showed no issues

### [PR microsoft/TypeScript#65072](https://github.com/microsoft/TypeScript/pull/65072) (Closed, `For Uncommitted Bug`)

**fix\(65071\): resurrect dirty\.SyncMap entries after Delete in LoadOrStore**

*Resurrect deleted dirty.SyncMap entries in LoadOrStore to prevent nil returns after tombstones.*

 * created by **timurzvural**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/65072#issuecomment-6551598550) **aetherxeg-source** proposed a test for stale-reference concerns when reusing the same SyncMapEntry after deletion and requested clarification of the intended entry lifetime contract
 * [today](https://github.com/microsoft/TypeScript/pull/65072#issuecomment-6592336553) **timurzvural** explained the intended contract of SyncMap entry identity, justified why new entry generation wasn’t needed, offered to revisit if a stronger API guard is desired, and noted the test consolidation commit

### [Issue microsoft/TypeScript#65076](https://github.com/microsoft/TypeScript/issues/65076) (Closed, `Bug`)

**Native tsc reads a literal U\+FFFD in a regex character class as 0xEF \(false TS1517 / TS1516\)**

*TypeScript 7's native tsc misreads a literal U+FFFD in regex character classes as 0xEF, causing false TS1517/TS1516 errors.*

 * created by **evanmarrone**
 * (today) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#65078](https://github.com/microsoft/TypeScript/issues/65078) (Open, `Bug`)

**panic: strings: negative Repeat count with \-\-pretty; TS8010 span for an empty type annotation in JS ends before it starts**

*TypeScript 7.x crashes with a negative Repeat count panic when pretty-printing a TS8010 error for an empty JS type annotation.*

 * created by **THEtheChad**
 * (today) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#65079](https://github.com/microsoft/TypeScript/issues/65079) (Open, `Bug`)

**panic: nil pointer dereference in CreateDiagnosticForNodeInSourceFile for a malformed "files" array in tsconfig\.json**

*TypeScript 7.x crashes with a nil pointer dereference on a malformed 'files' array in tsconfig.json instead of reporting an error.*

 * created by **THEtheChad**
 * (today) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`

### [PR microsoft/TypeScript#65080](https://github.com/microsoft/TypeScript/pull/65080) (Closed, `For Backlog Bug`)

**fix\(65076\): treat literal U\+FFFD as a real rune in regex classes**

*Modify regex literal parsing to recognize real U+FFFD runes in character classes instead of misclassifying them as decode errors.*

 * created by **timurzvural**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (today) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#65081](https://github.com/microsoft/TypeScript/pull/65081) (Closed, `For Backlog Bug`)

**fix\(65078\): keep empty spans for missing nodes when skipping trivia**

*Preserve empty spans for missing nodes when skipping trivia to avoid negative-length diagnostic ranges and crashes.*

 * created by **timurzvural**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (today) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`

### [PR microsoft/TypeScript#65082](https://github.com/microsoft/TypeScript/pull/65082) (Open, `For Backlog Bug`)

**fix\(tsoptions\): don't panic on empty files when AST node is missing**

*Fallback to a compiler diagnostic to avoid panics when tsconfig.json has an empty files array without an AST node*

 * created by **timurzvural**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (today) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/65082#issuecomment-6592509098) **timurzvural** rewrote the comment to explain the nil-node panic under parse recovery and added a test covering valid TS18002 and malformed JSON nil-node fallback cases

### [Issue microsoft/TypeScript#65083](https://github.com/microsoft/TypeScript/issues/65083) (Closed, `Bug`, **RyanCavanaugh**, **Copilot**)

**API: \`tsc\.exe\` opens a visible console window on Windows when the parent process has no console**

*On Windows, using the TypeScript sync API from a GUI process unexpectedly opens a visible tsc.exe console window.*

 * created by **SegaraRai**
 * (today) **RyanCavanaugh** added label `Bug`, set milestone to `Backlog`, and assigned to **Copilot**, **RyanCavanaugh**
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#65091](https://github.com/microsoft/TypeScript/pull/65091) (Closed, `For Milestone Bug`, **RyanCavanaugh**)

**Fill the config cycle into the TS18000 circularity message**

*Include the chain of configuration file paths causing a circular extends error in the TS18000 diagnostic message*

 * created by **cplieger**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [yesterday](https://github.com/microsoft/TypeScript/pull/65091#issuecomment-6560560316) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (today) **typescript-automation[bot]** added label `For Milestone Bug`, removed label `For Uncommitted Bug`, and assigned to **RyanCavanaugh**
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#65092](https://github.com/microsoft/TypeScript/issues/65092) (Open, `Suggestion`, `Declined`)

**Feature Request: Allow Content Mappers to opt\-in to transforming files end in built\-in extensions**

*Enable content mappers to opt in to transforming built-in TypeScript/JavaScript file extensions with scoped applicability and avoid duplicate LSP registrations.*

 * created by **GoodbyeNJN**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/65092#issuecomment-6560928348) **GoodbyeNJN** described a local experiment bypassing extension checks that led to duplicate inlay hints for .ts files and confirmed the cause by filtering out built-in JS/TS extensions
 * [today](https://github.com/microsoft/TypeScript/issues/65092#issuecomment-6586485859) **RyanCavanaugh** clarified that content mappers intentionally exclude language variants of TS and recommended using a .ets extension for new dialects
 * (today) **RyanCavanaugh** added labels `Suggestion`, `Declined`
 * [today](https://github.com/microsoft/TypeScript/issues/65092#issuecomment-6590654364) **loopingz** noted that in version 7.1.0-dev.20260929.1 additional SQL validation was possible and suggested leaving the decision to the user

### [PR microsoft/TypeScript#65093](https://github.com/microsoft/TypeScript/pull/65093) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **ahejlsberg**)

**Use SymbolTables instead of maps for member layouts**

*Replacing maps with SymbolTables for member layouts reduces memory usage and restores declared member ordering from TypeScript 6.0.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/65093#issuecomment-6564527141) **typescript-automation[bot]** provided tsc user test results and indicated everything looked good
 * [yesterday](https://github.com/microsoft/TypeScript/pull/65093#issuecomment-6564652774) **typescript-automation[bot]** reported the results of the requested perf run
 * [yesterday](https://github.com/microsoft/TypeScript/pull/65093#issuecomment-6565124402) **typescript-automation[bot]** provided build comparison results for top 400 repos between baseline and PR and noted an interesting change
 * **jakebailey** added label `Domain: Performance`

### [Issue microsoft/TypeScript#65094](https://github.com/microsoft/TypeScript/issues/65094) (Closed, `Bug`, **RyanCavanaugh**, **Copilot**)

**TS18000 circularity message prints its {0} placeholder instead of the config chain**

*The circular configuration error TS18000 in TypeScript 7.x prints its {0} placeholder instead of listing the tsconfig files in the cycle.*

 * created by **cplieger**
 * (today) **RyanCavanaugh** added label `Bug`, set milestone to `Backlog`, and assigned to **Copilot**, **RyanCavanaugh**
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#65096](https://github.com/microsoft/TypeScript/issues/65096) (Open, `Question`)

**Clarify EULA and Background Sync provenance in TypeScript 5\.9\.3 third\-party notices**

*Clarify the applicable EULA for the DefinitelyTyped entry and the provenance, coverage, and licensing of the Web Background Synchronization notice in TypeScript 5.9.3’s third-party notices.*

 * created by **beefstew**
 * [today](https://github.com/microsoft/TypeScript/issues/65096#issuecomment-6582507904) **RyanCavanaugh** asked which part of the long line was being referred to and who was requiring what and where
 * **RyanCavanaugh** added label `Needs More Info`
 * [today](https://github.com/microsoft/TypeScript/issues/65096#issuecomment-6583601937) **beefstew** asked whether an additional Microsoft EULA applies to the npm distribution and which Background Sync report/version and attribution conditions apply to the npm package
 * **RyanCavanaugh** removed label `Needs More Info`
 * [today](https://github.com/microsoft/TypeScript/issues/65096#issuecomment-6588107945) **RyanCavanaugh** said "I don't have authoritative answers off the top of my head for those questions. I can forward to our Legal to ask, but they'll likely ask what you're trying to determine before giving an answer."
 * [today](https://github.com/microsoft/TypeScript/issues/65096#issuecomment-6589431877) **beefstew** thanked maintainers and described running ORT on his app, noting unresolved license compliance questions
 * **RyanCavanaugh** added label `Question`

### [Issue microsoft/TypeScript#65097](https://github.com/microsoft/TypeScript/issues/65097) (Closed, `Needs Investigation`, **andrewbranch**, **Copilot**)

**Content mappers: a relative \`package\` path loads the package\.json of the nearest folder with node\_modules**

*A relative contentMappers package path resolves unexpectedly to the nearest node_modules package.json rather than the target mapper folder.*

 * created by **onmax**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **andrewbranch**
 * **andrewbranch** assigned to **Copilot**

### [PR microsoft/TypeScript#65099](https://github.com/microsoft/TypeScript/pull/65099) (Open, `For Backlog Bug`)

**Report TS2516 for non\-consecutive abstract method declarations**

*Skip misnamed implementation checks for abstract methods so TS2516 is reported when their declarations are non-consecutive.*

 * created by **Shadow0Bit**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/65099#issuecomment-6576739844) **Shadow0Bit** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript/pull/65099#issuecomment-6589221073) **jakebailey** suggested splitting the changes into two commits for easier review

### [Issue microsoft/TypeScript#65100](https://github.com/microsoft/TypeScript/issues/65100) (Closed)

**getting started**

*Guidance request for getting started with blocks, tools, and framework, seeking collaboration and freelancing opportunities.*

 * created by **Program-creator122**
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#65101](https://github.com/microsoft/TypeScript/issues/65101) (Open, `Duplicate`)

**Can you please add some new features for types: string length getter \(currently \`number\`\), string getter by index \(currently \`string\`\), array multiple spreads \(currently gives the error of type\)**

*Support exact string literal length, precise character indexing types, and multiple tuple spread elements in TypeScript.*

 * created by **mark-sss-coder**
 * [today](https://github.com/microsoft/TypeScript/issues/65101#issuecomment-6581326118) **nmain** suggested searching for each issue independently and identified the first idea as a duplicate of issue #34692
 * **RyanCavanaugh** added label `Duplicate`
 * [today](https://github.com/microsoft/TypeScript/issues/65101#issuecomment-6582413326) **RyanCavanaugh** said "The third is #48992"

### [PR microsoft/TypeScript#65102](https://github.com/microsoft/TypeScript/pull/65102) (Closed, `Author: Team`, `For Uncommitted Bug`, **RyanCavanaugh**, **Copilot**)

**Hide Windows console windows for API subprocesses**

*Add windowsHide:true to both sync and async Windows subprocess launches to hide console windows while preserving IPC and regression tests.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`, `For Milestone Bug`, `For Uncommitted Bug`, and removed labels `For Uncommitted Bug`, `For Milestone Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/65102#issuecomment-6583971728) **jakebailey** said "How is it that we don't need this in https://github.com/microsoft/TypeScript/blob/main/packages/typescript/lib/tsc.js ?"
 * [today](https://github.com/microsoft/TypeScript/pull/65102#issuecomment-6585991116) **DanielRosenwasser** questioned whether the code was needed in tsc.js and speculated it caused a command line window when debugging VS Code
 * [today](https://github.com/microsoft/TypeScript/pull/65102#issuecomment-6586284637) **SegaraRai** explained console allocation difference for spawn between tsc.js and API usage, demonstrated tests on Windows 11 with Node 26, and suggested adding windowsHide to tsc.js is harmless
 * [today](https://github.com/microsoft/TypeScript/pull/65102#issuecomment-6587014744) **DanielRosenwasser** said "@RyanCavanaugh can you have your agent add windowsHide: true to tsc.js?"
 * [today](https://github.com/microsoft/TypeScript/pull/65102#issuecomment-6588187395) **RyanCavanaugh** said "@copilot do as Daniel asks and also just remove the testcase, this level of tweak doesn't require that"
 * [today](https://github.com/microsoft/TypeScript/pull/65102#issuecomment-6588774809) **Copilot** described adding windowsHide: true to the tsc.js launcher, removing the regression test in commit 84263b733, and passing npx validation
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#65103](https://github.com/microsoft/TypeScript/pull/65103) (Closed, `Author: Team`, `For Uncommitted Bug`, **RyanCavanaugh**, **Copilot**)

**Lint missing diagnostic formatting arguments**

*Add lint rule to detect missing formatting arguments in diagnostic messages to prevent unsubstituted placeholders.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/65103#issuecomment-6585744185) **RyanCavanaugh** requested copilot to fix the missing argument based on the diagnostic message
 * [today](https://github.com/microsoft/TypeScript/pull/65103#issuecomment-6586291683) **RyanCavanaugh** said "@copilot you should be using a baseline test, not a unit test, for this change"
 * [today](https://github.com/microsoft/TypeScript/pull/65103#issuecomment-6586551982) **Copilot** fixed the missing diagnostic argument, added a regression test, and reported successful test results
 * [today](https://github.com/microsoft/TypeScript/pull/65103#issuecomment-6587022252) **Copilot** replaced the unit test and test-only checker export with a compiler fixture and diagnostic, type, and symbol baselines; reported tests passed but 'npx hereby validate' remained blocked by the TS18000 circularity lint error
 * [today](https://github.com/microsoft/TypeScript/pull/65103#issuecomment-6588110312) **jakebailey** said "Copilot review will repeatedly come back with infinite lint rule tweaks; feel free to decide a stopping point and say "good enough""
 * [today](https://github.com/microsoft/TypeScript/pull/65103#issuecomment-6588139170) **RyanCavanaugh** said "This found one true positive and zero false positives so that's my "good enough""
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#65104](https://github.com/microsoft/TypeScript/pull/65104) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Reuse programs across edits to files with synthetic imports**

*Enable program reuse in the TypeScript language server when synthetic tslib or JSX runtime imports remain unchanged during edits*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#65105](https://github.com/microsoft/TypeScript/pull/65105) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**, **Copilot**)

**Resolve relative content mapper packages, always resolve from the config that declares the mapper**

*Reject relative and absolute content mapper paths before node_modules resolution, resolve them from their declaring config, and report TS18075.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **andrewbranch**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/65105#issuecomment-6589273825) **andrewbranch** questioned rejecting resolution without detailed diagnostics and asked why relative or absolute paths to package directories aren't allowed
 * [today](https://github.com/microsoft/TypeScript/pull/65105#issuecomment-6589698521) **Copilot** explained that there was no principled reason to prohibit directory paths, updated resolution logic to support relative and absolute directory paths with improved diagnostics, and added test coverage

### [Issue microsoft/TypeScript#65107](https://github.com/microsoft/TypeScript/issues/65107) (Closed, `Won't Fix`)

**Native tsc: merge conflict markers after U\+2028/U\+2029 are not recognized \(false TS1109 instead of TS1185\)**

*Native tsc fails to detect merge conflict markers following Unicode line or paragraph separators (U+2028/U+2029), raising TS1109 instead of TS1185.*

 * created by **timurzvural**
 * [today](https://github.com/microsoft/TypeScript/issues/65107#issuecomment-6591478204) **RyanCavanaugh** said "Same answer as #65108"
 * **RyanCavanaugh** added label `Won't Fix`

### [Issue microsoft/TypeScript#65108](https://github.com/microsoft/TypeScript/issues/65108) (Closed, `Won't Fix`)

**Native tsc: missing “Are you missing a semicolon?” related info when the linebreak is U\+2028/U\+2029**

*When line breaks use U+2028/U+2029, native tsc omits the missing semicolon hint for TS2349 due to flawed rune handling.*

 * created by **timurzvural**
 * **RyanCavanaugh** added label `Won't Fix`
 * [today](https://github.com/microsoft/TypeScript/issues/65108#issuecomment-6591473446) **RyanCavanaugh** said "No one does this and if they don't it's not really important if they get the marginally different error message."
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#65109](https://github.com/microsoft/TypeScript/issues/65109) (Open, `Suggestion`)

**Let an ambient module declaration with import attributes refer to the module it matched**

*Allow ambient module declarations with import attributes to reference the matched module's resolved type.*

 * created by **alvaro-cuesta**

### [PR microsoft/TypeScript#65110](https://github.com/microsoft/TypeScript/pull/65110) (Closed, `For Uncommitted Bug`)

**fix\(project\): refresh content mappers when an open watchedFiles path is saved**

*Refresh content mapper projects upon saving open watched files by introducing a DiskChangedWhileOpen file change event*

 * created by **timurzvural**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [PR microsoft/TypeScript#65111](https://github.com/microsoft/TypeScript/pull/65111) (Closed, `For Uncommitted Bug`)

**Add regression test for checkJs method assignment contextual typing \(\#65086\)**

*Add a regression test verifying that checkJs correctly contextual-types lambda parameters in top-level and IIFE object and class method assignments.*

 * created by **timurzvural**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [PR microsoft/TypeScript#65112](https://github.com/microsoft/TypeScript/pull/65112) (Closed, `For Uncommitted Bug`)

**fix\(api\): keep related diagnostic text without a file location**

*Preserve related diagnostic messages without a file location when formatting errors with context*

 * created by **timurzvural**
 * (today) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`

### [PR microsoft/TypeScript#65113](https://github.com/microsoft/TypeScript/pull/65113) (Closed, `For Uncommitted Bug`)

**fix\(binder\): resolve default\-param refs to outer bindings, not body**

*Ensure default parameter initializers resolve to outer scope bindings instead of inner function, class, or enum declarations*

 * created by **timurzvural**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/65113#issuecomment-6590367737) **jakebailey** suggested splitting the changes into two commits for easier review
 * [today](https://github.com/microsoft/TypeScript/pull/65113#issuecomment-6591310031) **timurzvural** split into two commits: added a fourslash test for default-param outer bindings go-to-definition coverage and fixed binder resolution to reference outer bindings

### [Issue microsoft/TypeScript#65114](https://github.com/microsoft/TypeScript/issues/65114) (Open, `Needs Investigation`, **andrewbranch**)

**Content mappers that run \`node\` need it on the PATH in VS Code, while tsserver never did**

*VS Code’s TypeScript 7 content mappers require node on PATH, unlike tsserver plugins, causing .mdx mapping failures.*

 * created by **alvaro-cuesta**

### [PR microsoft/TypeScript#65115](https://github.com/microsoft/TypeScript/pull/65115) (Closed, `Domain: Performance`, `For Uncommitted Bug`)

**fix\(compiler\): skip loading files matched by attributed pattern ambients**

*Skip loading files for imports whose attributes match pattern ambient module declarations, avoiding unnecessary or invalid parsing.*

 * created by **timurzvural**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#65116](https://github.com/microsoft/TypeScript/pull/65116) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Preserve list and paths options in cached build info**

*List and paths options in cached build info are not preserved following a regression introduced in PR #64712.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#65117](https://github.com/microsoft/TypeScript/pull/65117) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Make auto\-import fix ranking a consistent order**

*Enforce a consistent ranking of auto-import fixes by preventing cyclical preferences between module kinds.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#65118](https://github.com/microsoft/TypeScript/issues/65118) (Open)

**Let a module augmentation with a wildcard add to every file it matches**

*Allow module augmentations using wildcards to extend the declarations of all matching modules with additional exports.*

 * created by **alvaro-cuesta**

### [PR microsoft/TypeScript#65119](https://github.com/microsoft/TypeScript/pull/65119) (Closed, `Author: Team`, `For Uncommitted Bug`, **DanielRosenwasser**)

**Add note on readability for filename directives\.**

*Suggest adding a readability note to filename directives to improve documentation clarity.*

 * created by **DanielRosenwasser**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **DanielRosenwasser**
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript#65120](https://github.com/microsoft/TypeScript/pull/65120) (Open, `For Backlog Bug`)

**fix\(isolatedDeclarations\): report TS9007/TS9008 for return entity names**

*Fix --isolatedDeclarations to report TS9007 and TS9008 for return entity names instead of TS9039 and TS9013*

 * created by **timurzvural**
 * (today) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Backlog Bug`, and removed label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/65120#issuecomment-6597306946) **timurzvural** said "Removed the explanatory comments from lookup.go and diagnostics.go — the logic-only changes remain."
 * [today](https://github.com/microsoft/TypeScript/pull/65120#issuecomment-6597747098) **timurzvural** said "Removed all comments from tsc/internal/pseudochecker/lookup.go and tsc/internal/transformers/declarations/diagnostics.go (40480ab)."

### [PR microsoft/TypeScript#65121](https://github.com/microsoft/TypeScript/pull/65121) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Serialize unreachable concrete mapped types structurally**

*Serialize concrete mapped types structurally in declaration files to prevent naming of unexported helper types*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#65122](https://github.com/microsoft/TypeScript/pull/65122) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Add a static\-PIE entry point and converter for Linux tsc**

*Add a static-PIE entry point and converter to patch Go Linux binaries into position-independent executables without relying on libc’s loader.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [Issue microsoft/TypeScript#65123](https://github.com/microsoft/TypeScript/issues/65123) (Open, `Suggestion`)

**Honor @deprecated on a literal member of a union**

*Enable JSDoc @deprecated annotations on individual union literal members to produce editor warnings for deprecated values.*

 * created by **patrickkettner**

### [Issue microsoft/TypeScript#65127](https://github.com/microsoft/TypeScript/issues/65127) (Open, `Bug`)

**Native tsc: interface\-only string index signatures no longer simplify under generic indexed access \(regressed in \#65059\)**

*PR #65059 regression prevents interface-only string index signatures from simplifying under generic indexed access in native tsc.*

 * created by **timurzvural**
 * [later](https://github.com/microsoft/TypeScript/issues/65127#issuecomment-6598730391) **timurzvural** described a native≠classic failure for a class with only a string index signature and provided example code

### [PR microsoft/TypeScript#65129](https://github.com/microsoft/TypeScript/pull/65129) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Remove unused parameters from recursive functions**

*Eliminate unused parameters in recursive functions that are only passed in recursive calls.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#65131](https://github.com/microsoft/TypeScript/pull/65131) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Update dependencies**

*Update project dependencies to the latest major LSP library versions, resolving all high-severity npm audit warnings.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#65132](https://github.com/microsoft/TypeScript/pull/65132) (Closed, `For Backlog Bug`)

**Match discriminated union constituents when inferring between unions**

*Introduce a matching phase in TypeScript’s union type inference to align discriminated union constituents and prevent incorrect cross-union inferences.*

 * created by **fadhlaouir**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/65132#issuecomment-6597199496) **fadhlaouir** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript/pull/65132#issuecomment-6598177370) **Andarist** said "There is a preexisting work happening in this space here: https://github.com/microsoft/TypeScript/pull/64695"
 * [later](https://github.com/microsoft/TypeScript/pull/65132#issuecomment-6602941817) **fadhlaouir** said "Thanks, I missed that one. Closing in favor of #64695."
 * (later) **fadhlaouir** closed the issue

### [Issue microsoft/TypeScript#65135](https://github.com/microsoft/TypeScript/issues/65135) (Open, `Needs Investigation`, **andrewbranch**)

**Native tsc: GetEmitModuleFormatOfFile ignores content\-mapper VirtualFileName \(\*\.mts treated as CJS under module:commonjs\)**

*Native Go TypeScript compiler ignores virtual .mts filenames when determining emit module format, defaulting to CommonJS.*

 * created by **timurzvural**
 * [today](https://github.com/microsoft/TypeScript/issues/65135#issuecomment-6597862392) **timurzvural** described false TS1287 and TS1295 diagnostics on content-mapped virtual .mts files under verbatimModuleSyntax with module: commonjs

### [Issue microsoft/TypeScript#65137](https://github.com/microsoft/TypeScript/issues/65137) (Closed, `Working as Intended`)

**Native \-\-isolatedDeclarations silently emits exported array binding patterns \(misses TS9019\)**

*Native tsc with --isolatedDeclarations silently permits exported array destructuring, missing TS9019 errors and emitting invalid declarations.*

 * created by **timurzvural**
 * [today](https://github.com/microsoft/TypeScript/issues/65137#issuecomment-6597989774) **timurzvural** identified additional silent cases where binding patterns without element initializers did not trigger TS9019 diagnostics, with code examples
 * [today](https://github.com/microsoft/TypeScript/issues/65137#issuecomment-6598059124) **timurzvural** pointed out that even with explicit type annotations, native TypeScript still silently emitted exported binding patterns without diagnostics, affecting any pattern lacking an initializer

### [Issue microsoft/TypeScript#65142](https://github.com/microsoft/TypeScript/issues/65142) (Closed)

**Native: \`exports\.f = function\(\){}; exports\.f\.x = …\` misses expando namespace in \.d\.ts \(false TS2339\)**

*Native tsc doesn’t recognize expando assignments on functions assigned via exports.f, dropping merged namespaces in .d.ts and reporting TS2339 errors.*

 * created by **timurzvural**
 * [later](https://github.com/microsoft/TypeScript/issues/65142#issuecomment-6598665461) **timurzvural** noted that the root gap also appeared for non-function exports prop assignments and provided code examples

### [Issue microsoft/TypeScript#65143](https://github.com/microsoft/TypeScript/issues/65143) (Closed)

**Native declaration emit drops \`C\.prototype\.m = …\` methods \(JS constructor / class\)**

*Native TypeScript compiler fails to include JS constructor and class prototype-assigned methods in declaration files while classic emit does.*

 * created by **timurzvural**
 * [later](https://github.com/microsoft/TypeScript/issues/65143#issuecomment-6598669391) **timurzvural** noted that Object.defineProperty on C.prototype adding get/set x is omitted in native .d.ts while classic synthesizes accessors

### [Issue microsoft/TypeScript#65148](https://github.com/microsoft/TypeScript/issues/65148) (Open, `Bug`)

**Native printer: \`new \(C?\.\(\)\.D\)\` emits as \`new \(C?\.\(\)\)\.D\` \(optional call trips hasUnparenthesizedCall\)**

*The TypeScript native printer misparenthesizes new expressions with optional call and member chains, printing new (C?.()).D() instead of new (C?.().D)().*

 * created by **timurzvural**
 * [later](https://github.com/microsoft/TypeScript/issues/65148#issuecomment-6599096865) **timurzvural** described that same-precedence bail affected as/satisfies in member chains and gave an example of printing discrepancy

### [PR microsoft/TypeScript#65160](https://github.com/microsoft/TypeScript/pull/65160) (Closed, `For Uncommitted Bug`)

**Retain configured projects for API\-opened files on closeProjects**

*Prevent closing configured projects needed by API-opened files when applying closeProjects in snapshot updates.*

 * created by **1-DARK**
 * (later) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`

### [Issue microsoft/TypeScript#65167](https://github.com/microsoft/TypeScript/issues/65167) (Open, `Bug`)

**Native LS: JSDoc \`@this\` / \`@param\` types are \`any\` for hover & completions \(checker OK\)**

*Native TypeScript language service does not provide completions for JSDoc @this-annotated functions in JavaScript, though type checking works.*

 * created by **timurzvural**
 * [later](https://github.com/microsoft/TypeScript/issues/65167#issuecomment-6601366789) **timurzvural** described missing native hover and completion support for JSDoc @param types on function parameters
 * [later](https://github.com/microsoft/TypeScript/issues/65167#issuecomment-6601386952) **timurzvural** described that call-site signature help showed parameters as any on the native host for a JSDoc-typed function while the classic host displayed correct types

### [Issue microsoft/TypeScript#65170](https://github.com/microsoft/TypeScript/issues/65170) (Open, `Bug`)

**Erasing \`as\` or \`satisfies\` can expose an invalid left operand of \`\*\*\`**

*Under erasableSyntaxOnly mode, erasing 'as' or 'satisfies' assertions can expose unparenthesized operands for '**', resulting in invalid JavaScript without diagnostics.*

 * created by **magic-akari**

### [Issue microsoft/TypeScript#65172](https://github.com/microsoft/TypeScript/issues/65172) (Closed)

**Native declaration emit drops \`Object\.defineProperty\(C\.prototype, …\)\` accessors**

*Native TypeScript declaration emit omits prototype getters/setters defined via Object.defineProperty, breaking accessor declarations in .d.ts files.*

 * created by **timurzvural**
 * [later](https://github.com/microsoft/TypeScript/issues/65172#issuecomment-6601836127) **timurzvural** clarified that tsc/CHANGES.md drops constructor-function and prototype expando support in favor of class, noted that class + Object.defineProperty(Class.prototype, …) path still works, and mentioned that the function C() form shows defineProperty-on-prototype emit but may be out of scope
 * [later](https://github.com/microsoft/TypeScript/issues/65172#issuecomment-6602664732) **hkleungai** suggested updating change.md to explicitly deprecate prototype-style methods in all scenarios

### [Issue microsoft/TypeScript#65174](https://github.com/microsoft/TypeScript/issues/65174) (Closed)

**Native tsc: presence of \`assert\` import suppresses TS2856 on \`with\` imports \(CJS\)**

*In native tsc, an import assertion suppresses TS2856 errors for JSON imports using 'with' attributes in CommonJS modules.*

 * created by **timurzvural**
 * [later](https://github.com/microsoft/TypeScript/issues/65174#issuecomment-6602405240) **timurzvural** provided a related matrix showing TypeScript error codes for with and assert imports under different module settings

### [Issue microsoft/TypeScript#65175](https://github.com/microsoft/TypeScript/issues/65175) (Closed, `Working as Intended`)

**Native tsc: \`assert\` under unsupported \`\-\-module\` reports TS2880 instead of TS2821**

*Native tsc reports TS2880 rather than TS2821 for import assertions under unsupported --module settings like es2020.*

 * created by **timurzvural**
 * [later](https://github.com/microsoft/TypeScript/issues/65175#issuecomment-6602435843) **timurzvural** said "Same assert-handling area as #65174."

### [Issue microsoft/TypeScript#65198](https://github.com/microsoft/TypeScript/issues/65198) (Closed)

**Native LS: JSDoc/checkJs "Ignore this error" / "Disable checking for this file" quick fixes missing**

*Native TypeScript LSP lacks quick fixes for adding @ts-ignore or @ts-nocheck comments to suppress JSDoc/checkJs errors in JavaScript files.*

 * created by **timurzvural**
 * [later](https://github.com/microsoft/TypeScript/issues/65198#issuecomment-6604886535) **timurzvural** said "Duplicate of #65197."
 * (later) **timurzvural** closed the issue

### [Issue microsoft/TypeScript#65226](https://github.com/microsoft/TypeScript/issues/65226) (Closed)

**Native LS: "Move labeled tuple element modifiers to labels" quick fix missing for TS5086**

*The native TypeScript language server reports TS5086 but lacks the 'Move labeled tuple element modifiers to labels' quick fix provided by the classic compiler.*

 * created by **timurzvural**
 * [later](https://github.com/microsoft/TypeScript/issues/65226#issuecomment-6605841675) **timurzvural** said "Closing: classic 6.0.3 offers the quick fix action but applies empty edits (no text change) for this TS5086 repro, so this is not a meaningful native gap."
 * (later) **timurzvural** closed the issue

### [PR microsoft/TypeScript#65279](https://github.com/microsoft/TypeScript/pull/65279) (Closed, `For Uncommitted Bug`)

**Erase types in preserved const enum initializers**

*Remove types from const enum initializers to ensure valid JavaScript output when constant evaluation fails while retaining the const modifier.*

 * created by **magic-akari**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

