# Report for 2026-11-03 (Tuesday, November 3rd, 2026)

26 different users commented on 104 different issues.

## Recommended Actions

 * Response Recommended
    * @jasonkuhrt provided detailed reproduction and test results in [microsoft/TypeScript#51109](https://github.com/microsoft/TypeScript/issues/51109#issuecomment-6610448669)
    * @trackoor provided repro steps and resolution info in [microsoft/TypeScript#64999](https://github.com/microsoft/TypeScript/issues/64999#issuecomment-6628171008)

## Activity Summary

### [Issue microsoft/TypeScript#51109](https://github.com/microsoft/TypeScript/issues/51109) (Open, `Suggestion`, `Awaiting More Feedback`)

**Name overload term/type module re\-export as namespace**

*Enable merging a type alias and a module namespace re-export using the same identifier via export * as syntax.*

 * [4 years ago](https://github.com/microsoft/TypeScript/issues/51109#issuecomment-1291010957) **cruhl** reported that `export * as Point from "./Point"` failed to recognize Point as a value and produced a ts(2693) error
 * [4 years ago](https://github.com/microsoft/TypeScript/issues/51109#issuecomment-1291021920) **cruhl** demonstrated that it worked by sharing screenshots
 * [4 years ago](https://github.com/microsoft/TypeScript/issues/51109#issuecomment-1292866508) **cruhl** confirmed that it worked and provided a screenshot
 * [today](https://github.com/microsoft/TypeScript/issues/51109#issuecomment-6610448669) **jasonkuhrt** reported that the example now compiles since TypeScript 4.9 but type-only re-exports still fail, explained the alias exclusion behavior and noted that inline import() types remain the only working spelling

### [Issue microsoft/TypeScript#62244](https://github.com/microsoft/TypeScript/issues/62244) (Closed, `Bug`, `Help Wanted`, `Domain: JSDoc`)

**JSDoc tags not parsed when a type may be present**

*TypeScript does not resolve JSDoc {@link C} tags in @throws comments when a type may be present.*

 * [1 year ago](https://github.com/microsoft/TypeScript/issues/62244#issuecomment-3369227126) **garretwilson** asked if there was any workaround syntax for `@throws` to enable a clickable link to the type in VS Code hover
 * [1 year ago](https://github.com/microsoft/TypeScript/issues/62244#issuecomment-3401080785) **hjalm8** described a workaround using markdown links and @link tag to make @throws reference clickable in VS Code
 * **RyanCavanaugh** added label `Domain: JSDoc`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#64097](https://github.com/microsoft/TypeScript/issues/64097) (Closed, `Bug`, **RyanCavanaugh**, **Copilot**)

**On TypeScript 7, Call hierarchy shows a full absolute path instead of file name \+ relative path**

*TypeScript 7 native-preview’s call hierarchy feature incorrectly displays full absolute file paths instead of file names with relative paths.*

 * (9 weeks ago) **RyanCavanaugh** set milestone to `Backlog`, and assigned to **Copilot**, **RyanCavanaugh**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64108](https://github.com/microsoft/TypeScript/pull/64108) (Closed, `Author: Team`, `For Uncommitted Bug`, **RyanCavanaugh**, **Copilot**)

**Fix call hierarchy file node paths**

*Display file basenames with project-relative directories in call hierarchy nodes instead of absolute file paths.*

 * **typescript-automation[bot]** added label `Author: Team`
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/64108#issuecomment-6542774931) **Copilot** merged main and updated call hierarchy to use initialized workspace folders with typed paths, noted build, tests, lint, and format passed but CodeQL was blocked by a Git diff timeout
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64108#issuecomment-6591918806) **jakebailey** said "I don't hate it. @andrewbranch Do you have any feelings about this?"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64205](https://github.com/microsoft/TypeScript/pull/64205) (Open, `For Uncommitted Bug`, **johnfav03**)

**fix\(project\): re\-read cached file contents on didChangeWatchedFiles Created event**

*Add support for didChangeWatchedFiles Created events to reload cached file contents and prevent stale diagnostics.*

 * created by **erantianantha**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * **typescript-automation[bot]** assigned to **johnfav03**

### [Issue microsoft/TypeScript#64431](https://github.com/microsoft/TypeScript/issues/64431) (Open, `Bug`, **RyanCavanaugh**, **Copilot**)

**TS7031 false positive for nested object binding pattern with \`= {}\` default in an annotated parameter \(regression from \#64043\)**

*Nested object destructuring with default {} in a typed parameter erroneously triggers TS7031 errors after PR #64043*

 * **RyanCavanaugh** assigned to **RyanCavanaugh**
 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/64431#issuecomment-6041533127) **Konan69** described contextually typed parameters triggering TS7031 errors in recent nightly, validated that #64440 removes the errors, suggested adding test cases, and opened #64671 with an alternative patch
 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/64431#issuecomment-6297398470) **connorshea** mentioned encountering the same regression when using typescript@next, noting it did not occur in their 7.0 dev release but appeared in ts 7.1
 * [today](https://github.com/microsoft/TypeScript/issues/64431#issuecomment-6610691604) **connorshea** provided a reproduction case showing errors in TypeScript 7.1.0-dev but not in 7.0.2

### [PR microsoft/TypeScript#64659](https://github.com/microsoft/TypeScript/pull/64659) (Closed, `Domain: Performance`, `For Uncommitted Bug`, **johnfav03**)

**Compute signatures of dependent files in parallel on incremental rebuilds**

*Declaration signatures for files dependent on an edited file are now computed in parallel during incremental rebuilds to significantly reduce build times.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/64659#issuecomment-6273501427) **typescript-automation[bot]** reported that test results comparing baseline and PR looked good
 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/64659#issuecomment-6274117618) **typescript-automation[bot]** reported that tsc runs on the top 400 repos comparing baseline and pr succeeded
 * **jakebailey** added label `Domain: Performance`
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript#64661](https://github.com/microsoft/TypeScript/issues/64661) (Closed, `Bug`)

**Class names \`eval\` and \`arguments\` are not reported as invalid strict mode bindings**

*TypeScript fails to report errors for class names 'eval' or 'arguments' as invalid strict-mode bindings, causing runtime errors.*

 * created by **JLHwung**
 * (3 weeks ago) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64682](https://github.com/microsoft/TypeScript/pull/64682) (Closed, `For Backlog Bug`)

**Report strict\-mode errors for class names eval and arguments**

*Report TS1210 strict-mode errors for class declarations and expressions named 'eval' or 'arguments' during binding.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/64682#issuecomment-6590034331) **typescript-automation[bot]** reported tsc user test results and confirmed everything looked good
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64682#issuecomment-6590279722) **typescript-automation[bot]** provided the results of the requested performance run
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64682#issuecomment-6591057613) **typescript-automation[bot]** reported that running the top 400 repos tsc comparison between baseline and pr succeeded without issues
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64732](https://github.com/microsoft/TypeScript/pull/64732) (Closed, `For Backlog Bug`)

**Fix inline JSDoc links in optional type positions**

*Ensure inline link, linkcode, and linkplain tags after @throws and @returns are parsed as links instead of type expressions.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/64732#issuecomment-6264594274) **mbarinov** said "Hi @jakebailey, thanks for running the additional tests. Do you have any feedback or additional checks you'd like me to run before this is ready to merge?"
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64732#issuecomment-6589191750) **jakebailey** suggested rebasing on main and splitting into separate test and fix commits
 * [today](https://github.com/microsoft/TypeScript/pull/64732#issuecomment-6608048340) **mbarinov** rebased the branch onto main and split the changes into two commits as requested
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64825](https://github.com/microsoft/TypeScript/pull/64825) (Closed, `For Milestone Bug`, **johnfav03**)

**\[api\] Reparse extended configs cached under another resolution stack**

*Extended config cache wrongly reuses entries from circular tsconfig chains, causing snapshot panics or hangs without proper resolution stack context.*

 * (1 week ago) **typescript-automation[bot]** added label `For Milestone Bug`, removed label `For Uncommitted Bug`, and assigned to **johnfav03**
 * [today](https://github.com/microsoft/TypeScript/pull/64825#issuecomment-6619849102) **cplieger** split the pull request into three focused fixes addressing issues #64824, #65300, and #65301
 * (today) **cplieger** closed the issue

### [Issue microsoft/TypeScript#64864](https://github.com/microsoft/TypeScript/issues/64864) (Closed, **andrewbranch**, **Copilot**)

**Some JS API types don't match their runtime values**

*Several TypeScript JS API type definitions in the sync and AST packages misrepresent actual runtime property types, causing mismatches.*

 * created by **auvred**
 * **jakebailey** assigned to **andrewbranch**
 * **andrewbranch** assigned to **Copilot**
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript#64974](https://github.com/microsoft/TypeScript/issues/64974) (Open, `Bug`)

**7\.1: destructured parameter with a \`= {}\` default loses its contextual type \(TS7031\)**

*TypeScript 7.1 regression causes destructured parameters with a default {} to lose their contextual types and trigger implicit any errors.*

 * [1 week ago](https://github.com/microsoft/TypeScript/issues/64974#issuecomment-6447340132) **jltrv** reported two additional regression variants in TypeScript 7.1.0-dev affecting nested default-initialized patterns and non-empty object literal defaults and quantified their impact
 * (4 days ago) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/64974#issuecomment-6610623048) **connorshea** said "I think this may be the same issue as #64431?"

### [Issue microsoft/TypeScript#64980](https://github.com/microsoft/TypeScript/issues/64980) (Closed, `Bug`)

**\`\-\-experimentalDecorators\`: decorated \`abstract\` property is emitted as a class field \(regression in 7\.0\)**

*TypeScript 7.0 regressively emits a class field for decorated abstract properties, shadowing prototype decorators instead of erasing the field.*

 * created by **simleb**
 * (4 days ago) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64982](https://github.com/microsoft/TypeScript/pull/64982) (Closed, `For Backlog Bug`)

**erase decorated abstract properties under experimentalDecorators with define semantics**

*Prevent decorated abstract class properties from emitting instance fields under experimentalDecorators with useDefineForClassFields.*

 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64982#issuecomment-6589155506) **jakebailey** said "Ideally this would be two commits, one that adds the test and "bad" baselines, then a second commit that shows the fix plus baseline update"
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64982#issuecomment-6594506148) **1-DARK** said " Hi @jakebailey,  done. Split into two commits: the first adds the tests with the current (bad) baselines, and the second contains the fix plus the baseline diff."
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#64999](https://github.com/microsoft/TypeScript/issues/64999) (Open, `Bug`, `Domain: Parser`)

**Top\-level await reparse keeps statements it already consumed when it reaches the end of the file**

*TypeScript's top-level await reparse retains already consumed statements at file end, causing overlapping parse nodes.*

 * (yesterday) **RyanCavanaugh** added labels `Bug`, `Domain: Parser`, and set milestone to `Backlog`
 * [later](https://github.com/microsoft/TypeScript/issues/64999#issuecomment-6628171008) **trackoor** demonstrated that the parser rejected valid module code with top-level await in for loops, provided reproduction steps and error details across multiple TS versions, noted that the parser.go change from #64993 fixes the issue, and suggested using a test262 case

### [PR microsoft/TypeScript#65001](https://github.com/microsoft/TypeScript/pull/65001) (Closed, `Author: Team`, `For Uncommitted Bug`, `dependencies`, `javascript`)

**Bump qs from 6\.16\.0 to 6\.17\.1**

*Upgrade qs from 6.16.0 to 6.17.1 to incorporate bug fixes and improvements.*

 * (6 days ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`
 * [6 days ago](https://github.com/microsoft/TypeScript/pull/65001#issuecomment-6481703030) **jakebailey** said "Well, see you in a week"
 * (today) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/65001#issuecomment-6615793890) **dependabot[bot]** explained how to ignore dependency update notifications or reopen the PR to resolve conflicts

### [PR microsoft/TypeScript#65016](https://github.com/microsoft/TypeScript/pull/65016) (Closed, `For Uncommitted Bug`)

**fix\(65011\): preserve contextual types for destructured parameter defaults**

*TS 7.1 destructured defaults lose contextual types and trigger TS7031 errors, so padding now occurs only without contextual type.*

 * created by **timurzvural**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#65039](https://github.com/microsoft/TypeScript/pull/65039) (Closed, `For Uncommitted Bug`)

**fix\(64998\): defer index signature value types for keyof circularity**

*Multi-checker builds emit index signature value types as any from circular eager resolution, now using deferred and lazy resolution.*

 * created by **timurzvural**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#65052](https://github.com/microsoft/TypeScript/issues/65052) (Closed)

**7\.0 regression: inherited members are sorted by position, so an empty subinterface changes assignability**

*TypeScript 7.0 regresses interface assignability by sorting inherited members by position, wrongly allowing assignments in empty subinterfaces.*

 * created by **pearofducks**
 * [today](https://github.com/microsoft/TypeScript/issues/65052#issuecomment-6601443980) **timurzvural** provided additional examples triggering the empty-extends/shared-member-layout unsoundness in abstract classes and interfaces
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript#65063](https://github.com/microsoft/TypeScript/pull/65063) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**Fix AST optionality**

*Update AST node definitions to make type-related properties and tokens optional or non-null as needed.*

 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/65063#issuecomment-6532131676) **RyanCavanaugh** questioned why IndexSignatureDeclaration.type being optional is the only syntax error in the list
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/65063#issuecomment-6532745343) **andrewbranch** clarified that the error is a grammar error and proposed either keeping the node optional or making it a parse error with a missing identifier
 * [today](https://github.com/microsoft/TypeScript/pull/65063#issuecomment-6609532002) **andrewbranch** decided to make `interface I { [p: string] }` a syntactically legal implicit `any`, extracted that into a separate PR, and removed index signature changes from this PR
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#65064](https://github.com/microsoft/TypeScript/pull/65064) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**\[experiment\] fully order independent type checking**

*Make the type checker fully order independent by replacing ID-based caching with content-based memos and order-variant tests.*

 * [2 days ago](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6567487859) **typescript-automation[bot]** reported new TypeScript errors for implicit any return types in functions _rebuild and recur during tsc comparison
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6567682690) **typescript-automation[bot]** provided the perf run results requested by @jakebailey
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6568122632) **typescript-automation[bot]** reported build comparison results for top 400 repos showing new TypeScript errors
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6625694747) **jakebailey** requested the TypeScript bot to run various tests
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6625695932) **typescript-automation[bot]** said "Hey @jakebailey, this PR is in an unmergable state, so is missing a merge commit to run against; please resolve conflicts and try again."
 * [later](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6625844953) **jakebailey** requested the TypeScript bot to run various tests
 * [later](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6625847118) **typescript-automation[bot]** reported CI jobs starting and listed commands with status and result links
 * [later](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6626536895) **typescript-automation[bot]** posted DT test results showing branch-only errors in d3-selection due to a TS2769 overload mismatch
 * [later](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6626572032) **typescript-automation[bot]** reported new TypeScript errors in user tests comparing baseline and pr and asked for review
 * [later](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6626808573) **typescript-automation[bot]** shared the perf run results requested by @jakebailey
 * [later](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6628509191) **typescript-automation[bot]** reported tsc comparison results on the top 1000 repos, noted build failures in OmniRoute and PeerTube, and asked to review an interesting change

### [PR microsoft/TypeScript#65065](https://github.com/microsoft/TypeScript/pull/65065) (Closed, `For Uncommitted Bug`)

**fix\(65052\): keep inherited member order from the base type**

*Preserve base-type declaration order for inherited interface members to correct variance assignment errors in empty subtypes.*

 * created by **timurzvural**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#65066](https://github.com/microsoft/TypeScript/pull/65066) (Closed, `Domain: Performance`, `For Uncommitted Bug`)

**Add getSymbolDocumentations and getMembersOfType for API surface extraction**

*Add getSymbolDocumentations and getMembersOfType to batch-fetch JSDoc documentation and filtered type members in one request for efficient API surface extraction.*

 * (4 days ago) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * **jakebailey** added label `Domain: Performance`
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#65072](https://github.com/microsoft/TypeScript/pull/65072) (Closed, `For Uncommitted Bug`)

**fix\(65071\): resurrect dirty\.SyncMap entries after Delete in LoadOrStore**

*Resurrect deleted dirty.SyncMap entries in LoadOrStore to prevent nil returns after tombstones.*

 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/65072#issuecomment-6551598550) **aetherxeg-source** proposed a test for stale-reference concerns when reusing the same SyncMapEntry after deletion and requested clarification of the intended entry lifetime contract
 * [yesterday](https://github.com/microsoft/TypeScript/pull/65072#issuecomment-6592336553) **timurzvural** explained the intended contract of SyncMap entry identity, justified why new entry generation wasn’t needed, offered to revisit if a stronger API guard is desired, and noted the test consolidation commit
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#65073](https://github.com/microsoft/TypeScript/pull/65073) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Compute CommonJSModuleIndicator in the parser**

*Move CommonJSModuleIndicator computation from the binding phase into the parser to enable earlier, consistent file reuse without race conditions.*

 * [3 days ago](https://github.com/microsoft/TypeScript/pull/65073#issuecomment-6548778038) **jakebailey** said "@typescript-bot perf test this faster"
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/65073#issuecomment-6548778973) **typescript-automation[bot]** announced starting jobs with status and results links
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/65073#issuecomment-6549314978) **typescript-automation[bot]** posted the requested perf run results with a detailed comparison report for tsc metrics
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#65075](https://github.com/microsoft/TypeScript/issues/65075) (Closed, `Duplicate`)

**typescript/ast/scanner: scan\(\) never advances past \`\#\` not followed by an identifier start \(7\.1\.0\-beta\)**

*TypeScript 7.1.0-beta’s AST scanner scan method fails to advance past '#' not followed by an identifier, causing infinite loops.*

 * created by **ilterugur**
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/65075#issuecomment-6544425849) **MartinJohns** said "Duplicate of #64490."
 * **RyanCavanaugh** added label `Duplicate`

### [PR microsoft/TypeScript#65081](https://github.com/microsoft/TypeScript/pull/65081) (Closed, `For Backlog Bug`)

**fix\(65078\): keep empty spans for missing nodes when skipping trivia**

*Preserve empty spans for missing nodes when skipping trivia to avoid negative-length diagnostic ranges and crashes.*

 * (3 days ago) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Backlog Bug`, and removed label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/65081#issuecomment-6618226109) **RyanCavanaugh** said "I don't think the AI understands the bug here. Let's have a smarter agent look at this one."
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#65088](https://github.com/microsoft/TypeScript/pull/65088) (Open, `For Backlog Bug`)

**Reject pending async API requests when the connection closes**

*Drain complete responses and reject any remaining pending asynchronous API requests when the connection closes.*

 * created by **wsjwu58-cmd**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/65088#issuecomment-6557153358) **wsjwu58-cmd** said "@microsoft-github-policy-service agree"
 * (today) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`

### [Issue microsoft/TypeScript#65089](https://github.com/microsoft/TypeScript/issues/65089) (Open, `Bug`)

**Async API requests remain pending after the RPC connection closes**

*Asynchronous API requests via the RPC client remain pending and never settle after the connection closes.*

 * created by **wsjwu58-cmd**
 * (today) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#65090](https://github.com/microsoft/TypeScript/issues/65090) (Closed, `Bug`, **RyanCavanaugh**, **Copilot**)

**Native compiler API resolves a default\-parameter reference to a body function binding**

*The TypeScript native compiler API incorrectly resolves default parameter references to an inner function declaration instead of the outer variable.*

 * created by **CaliLuke**
 * (today) **RyanCavanaugh** added label `Bug`, set milestone to `Backlog`, and assigned to **Copilot**, **RyanCavanaugh**

### [Issue microsoft/TypeScript#65092](https://github.com/microsoft/TypeScript/issues/65092) (Open, `Suggestion`, `Declined`)

**Feature Request: Allow Content Mappers to opt\-in to transforming files end in built\-in extensions**

*Enable content mappers to opt in to transforming built-in TypeScript/JavaScript file extensions with scoped applicability and avoid duplicate LSP registrations.*

 * (yesterday) **RyanCavanaugh** added labels `Suggestion`, `Declined`
 * [yesterday](https://github.com/microsoft/TypeScript/issues/65092#issuecomment-6590654364) **loopingz** noted that in version 7.1.0-dev.20260929.1 additional SQL validation was possible and suggested leaving the decision to the user
 * [today](https://github.com/microsoft/TypeScript/issues/65092#issuecomment-6616085979) **RyanCavanaugh** explained why failing to block wouldn't work and listed issues with outputExtensions, refactorings, and multiple CMs for .ts files

### [PR microsoft/TypeScript#65093](https://github.com/microsoft/TypeScript/pull/65093) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **ahejlsberg**)

**Use SymbolTables instead of maps for member layouts**

*Replacing maps with SymbolTables for member layouts reduces memory usage and restores declared member ordering from TypeScript 6.0.*

 * [2 days ago](https://github.com/microsoft/TypeScript/pull/65093#issuecomment-6564652774) **typescript-automation[bot]** reported the results of the requested perf run
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/65093#issuecomment-6565124402) **typescript-automation[bot]** provided build comparison results for top 400 repos between baseline and PR and noted an interesting change
 * **jakebailey** added label `Domain: Performance`
 * [today](https://github.com/microsoft/TypeScript/pull/65093#issuecomment-6609345302) **jakebailey** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/65093#issuecomment-6609347684) **typescript-automation[bot]** posted job status updates for 'test top400', 'user test this', 'run dt', and 'perf test this faster'
 * [today](https://github.com/microsoft/TypeScript/pull/65093#issuecomment-6610285291) **typescript-automation[bot]** notified that DT test results were ready and unchanged
 * [today](https://github.com/microsoft/TypeScript/pull/65093#issuecomment-6610741407) **typescript-automation[bot]** provided perf run results in a detailed comparison report
 * [today](https://github.com/microsoft/TypeScript/pull/65093#issuecomment-6611713084) **typescript-automation[bot]** reported build comparison results for top 400 repos showing new TypeScript errors
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript#65095](https://github.com/microsoft/TypeScript/issues/65095) (Open, `Bug`)

**TypeScript 7 memory grows without bound on a next\-intl call with a missing namespace and ICU arguments \(6\.0 stays at 2\.5 GB\)**

*TypeScript 7.0.2's memory usage grows indefinitely when compiling next-intl with a missing namespace and ICU arguments, unlike versions 6.0.3 and 5.9.3.*

 * created by **jcoulaud**
 * (today) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#65097](https://github.com/microsoft/TypeScript/issues/65097) (Closed, `Needs Investigation`, **andrewbranch**, **Copilot**)

**Content mappers: a relative \`package\` path loads the package\.json of the nearest folder with node\_modules**

*A relative contentMappers package path resolves unexpectedly to the nearest node_modules package.json rather than the target mapper folder.*

 * (yesterday) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **andrewbranch**
 * **andrewbranch** assigned to **Copilot**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#65099](https://github.com/microsoft/TypeScript/pull/65099) (Closed, `For Backlog Bug`)

**Report TS2516 for non\-consecutive abstract method declarations**

*Skip misnamed implementation checks for abstract methods so TS2516 is reported when their declarations are non-consecutive.*

 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [yesterday](https://github.com/microsoft/TypeScript/pull/65099#issuecomment-6576739844) **Shadow0Bit** said "@microsoft-github-policy-service agree"
 * [yesterday](https://github.com/microsoft/TypeScript/pull/65099#issuecomment-6589221073) **jakebailey** suggested splitting the changes into two commits for easier review
 * [today](https://github.com/microsoft/TypeScript/pull/65099#issuecomment-6623279107) **Shadow0Bit** said "Sure thing, I've split it into two commits."

### [PR microsoft/TypeScript#65105](https://github.com/microsoft/TypeScript/pull/65105) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**, **Copilot**)

**Resolve relative content mapper packages, always resolve from the config that declares the mapper**

*Reject relative and absolute content mapper paths before node_modules resolution, resolve them from their declaring config, and report TS18075.*

 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [yesterday](https://github.com/microsoft/TypeScript/pull/65105#issuecomment-6589273825) **andrewbranch** questioned rejecting resolution without detailed diagnostics and asked why relative or absolute paths to package directories aren't allowed
 * [yesterday](https://github.com/microsoft/TypeScript/pull/65105#issuecomment-6589698521) **Copilot** explained that there was no principled reason to prohibit directory paths, updated resolution logic to support relative and absolute directory paths with improved diagnostics, and added test coverage
 * [today](https://github.com/microsoft/TypeScript/pull/65105#issuecomment-6611651258) **andrewbranch** said "@copilot fix the "previously missed" comment from the review"
 * [today](https://github.com/microsoft/TypeScript/pull/65105#issuecomment-6612194005) **Copilot** fixed directory mappers to allow resolved paths inside an open workspace and deny outside-workspace directories; added regression coverage and validated with `npx hereby validate`
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript#65107](https://github.com/microsoft/TypeScript/issues/65107) (Closed, `Won't Fix`)

**Native tsc: merge conflict markers after U\+2028/U\+2029 are not recognized \(false TS1109 instead of TS1185\)**

*Native tsc fails to detect merge conflict markers following Unicode line or paragraph separators (U+2028/U+2029), raising TS1109 instead of TS1185.*

 * created by **timurzvural**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/65107#issuecomment-6591478204) **RyanCavanaugh** said "Same answer as #65108"
 * **RyanCavanaugh** added label `Won't Fix`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#65109](https://github.com/microsoft/TypeScript/issues/65109) (Open, `Suggestion`)

**Let an ambient module declaration with import attributes refer to the module it matched**

*Allow ambient module declarations with import attributes to reference the matched module's resolved type.*

 * created by **alvaro-cuesta**
 * **RyanCavanaugh** added label `Suggestion`

### [PR microsoft/TypeScript#65110](https://github.com/microsoft/TypeScript/pull/65110) (Closed, `For Uncommitted Bug`)

**fix\(project\): refresh content mappers when an open watchedFiles path is saved**

*Refresh content mapper projects upon saving open watched files by introducing a DiskChangedWhileOpen file change event*

 * created by **timurzvural**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#65111](https://github.com/microsoft/TypeScript/pull/65111) (Closed, `For Uncommitted Bug`)

**Add regression test for checkJs method assignment contextual typing \(\#65086\)**

*Add a regression test verifying that checkJs correctly contextual-types lambda parameters in top-level and IIFE object and class method assignments.*

 * created by **timurzvural**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#65112](https://github.com/microsoft/TypeScript/pull/65112) (Closed, `For Uncommitted Bug`)

**fix\(api\): keep related diagnostic text without a file location**

*Preserve related diagnostic messages without a file location when formatting errors with context*

 * created by **timurzvural**
 * (yesterday) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#65113](https://github.com/microsoft/TypeScript/pull/65113) (Closed, `For Uncommitted Bug`)

**fix\(binder\): resolve default\-param refs to outer bindings, not body**

*Ensure default parameter initializers resolve to outer scope bindings instead of inner function, class, or enum declarations*

 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [yesterday](https://github.com/microsoft/TypeScript/pull/65113#issuecomment-6590367737) **jakebailey** suggested splitting the changes into two commits for easier review
 * [yesterday](https://github.com/microsoft/TypeScript/pull/65113#issuecomment-6591310031) **timurzvural** split into two commits: added a fourslash test for default-param outer bindings go-to-definition coverage and fixed binder resolution to reference outer bindings
 * (today) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/65113#issuecomment-6618150688) **RyanCavanaugh** said ""(unless downlevel emit would move the initializer into the body)." refers to a situation that no longer exists (ES5 emit)"

### [Issue microsoft/TypeScript#65114](https://github.com/microsoft/TypeScript/issues/65114) (Open, `Needs Investigation`, **andrewbranch**)

**Content mappers that run \`node\` need it on the PATH in VS Code, while tsserver never did**

*VS Code’s TypeScript 7 content mappers require node on PATH, unlike tsserver plugins, causing .mdx mapping failures.*

 * created by **alvaro-cuesta**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **andrewbranch**

### [PR microsoft/TypeScript#65115](https://github.com/microsoft/TypeScript/pull/65115) (Closed, `Domain: Performance`, `For Uncommitted Bug`)

**fix\(compiler\): skip loading files matched by attributed pattern ambients**

*Skip loading files for imports whose attributes match pattern ambient module declarations, avoiding unnecessary or invalid parsing.*

 * created by **timurzvural**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * **jakebailey** added label `Domain: Performance`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#65123](https://github.com/microsoft/TypeScript/issues/65123) (Open, `Suggestion`)

**Honor @deprecated on a literal member of a union**

*Enable JSDoc @deprecated annotations on individual union literal members to produce editor warnings for deprecated values.*

 * created by **patrickkettner**
 * **RyanCavanaugh** added label `Suggestion`

### [Issue microsoft/TypeScript#65127](https://github.com/microsoft/TypeScript/issues/65127) (Open, `Bug`)

**Native tsc: interface\-only string index signatures no longer simplify under generic indexed access \(regressed in \#65059\)**

*PR #65059 regression prevents interface-only string index signatures from simplifying under generic indexed access in native tsc.*

 * created by **timurzvural**
 * [today](https://github.com/microsoft/TypeScript/issues/65127#issuecomment-6598730391) **timurzvural** described a native≠classic failure for a class with only a string index signature and provided example code
 * (today) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`

### [PR microsoft/TypeScript#65129](https://github.com/microsoft/TypeScript/pull/65129) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Remove unused parameters from recursive functions**

*Eliminate unused parameters in recursive functions that are only passed in recursive calls.*

 * (yesterday) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#65135](https://github.com/microsoft/TypeScript/issues/65135) (Open, `Needs Investigation`, **andrewbranch**)

**Native tsc: GetEmitModuleFormatOfFile ignores content\-mapper VirtualFileName \(\*\.mts treated as CJS under module:commonjs\)**

*Native Go TypeScript compiler ignores virtual .mts filenames when determining emit module format, defaulting to CommonJS.*

 * created by **timurzvural**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/65135#issuecomment-6597862392) **timurzvural** described false TS1287 and TS1295 diagnostics on content-mapped virtual .mts files under verbatimModuleSyntax with module: commonjs
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **andrewbranch**

### [Issue microsoft/TypeScript#65137](https://github.com/microsoft/TypeScript/issues/65137) (Closed, `Working as Intended`)

**Native \-\-isolatedDeclarations silently emits exported array binding patterns \(misses TS9019\)**

*Native tsc with --isolatedDeclarations silently permits exported array destructuring, missing TS9019 errors and emitting invalid declarations.*

 * created by **timurzvural**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/65137#issuecomment-6597989774) **timurzvural** identified additional silent cases where binding patterns without element initializers did not trigger TS9019 diagnostics, with code examples
 * [yesterday](https://github.com/microsoft/TypeScript/issues/65137#issuecomment-6598059124) **timurzvural** pointed out that even with explicit type annotations, native TypeScript still silently emitted exported binding patterns without diagnostics, affecting any pattern lacking an initializer
 * [today](https://github.com/microsoft/TypeScript/issues/65137#issuecomment-6612840637) **RyanCavanaugh** challenged the interpretation of the issue as a bug and asserted that the emitted .d.ts file was valid and correctly represented the input code
 * (today) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** added label `Working as Intended`

### [Issue microsoft/TypeScript#65142](https://github.com/microsoft/TypeScript/issues/65142) (Closed)

**Native: \`exports\.f = function\(\){}; exports\.f\.x = …\` misses expando namespace in \.d\.ts \(false TS2339\)**

*Native tsc doesn’t recognize expando assignments on functions assigned via exports.f, dropping merged namespaces in .d.ts and reporting TS2339 errors.*

 * created by **timurzvural**
 * [today](https://github.com/microsoft/TypeScript/issues/65142#issuecomment-6598665461) **timurzvural** noted that the root gap also appeared for non-function exports prop assignments and provided code examples
 * [today](https://github.com/microsoft/TypeScript/issues/65142#issuecomment-6615913662) **RyanCavanaugh** said "Expando changes are documented"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#65143](https://github.com/microsoft/TypeScript/issues/65143) (Closed)

**Native declaration emit drops \`C\.prototype\.m = …\` methods \(JS constructor / class\)**

*Native TypeScript compiler fails to include JS constructor and class prototype-assigned methods in declaration files while classic emit does.*

 * created by **timurzvural**
 * [today](https://github.com/microsoft/TypeScript/issues/65143#issuecomment-6598669391) **timurzvural** noted that Object.defineProperty on C.prototype adding get/set x is omitted in native .d.ts while classic synthesizes accessors
 * [today](https://github.com/microsoft/TypeScript/issues/65143#issuecomment-6612671267) **RyanCavanaugh** said "This was covered in the release notes / changes.md."
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#65148](https://github.com/microsoft/TypeScript/issues/65148) (Open, `Bug`)

**Native printer: \`new \(C?\.\(\)\.D\)\` emits as \`new \(C?\.\(\)\)\.D\` \(optional call trips hasUnparenthesizedCall\)**

*The TypeScript native printer misparenthesizes new expressions with optional call and member chains, printing new (C?.()).D() instead of new (C?.().D)().*

 * created by **timurzvural**
 * [today](https://github.com/microsoft/TypeScript/issues/65148#issuecomment-6599096865) **timurzvural** described that same-precedence bail affected as/satisfies in member chains and gave an example of printing discrepancy
 * (today) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`

### [PR microsoft/TypeScript#65160](https://github.com/microsoft/TypeScript/pull/65160) (Closed, `For Uncommitted Bug`)

**Retain configured projects for API\-opened files on closeProjects**

*Prevent closing configured projects needed by API-opened files when applying closeProjects in snapshot updates.*

 * created by **1-DARK**
 * (today) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/65160#issuecomment-6612766451) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript#65167](https://github.com/microsoft/TypeScript/issues/65167) (Open, `Bug`)

**Native LS: JSDoc \`@this\` / \`@param\` types are \`any\` for hover & completions \(checker OK\)**

*Native TypeScript language service does not provide completions for JSDoc @this-annotated functions in JavaScript, though type checking works.*

 * created by **timurzvural**
 * [today](https://github.com/microsoft/TypeScript/issues/65167#issuecomment-6601366789) **timurzvural** described missing native hover and completion support for JSDoc @param types on function parameters
 * [today](https://github.com/microsoft/TypeScript/issues/65167#issuecomment-6601386952) **timurzvural** described that call-site signature help showed parameters as any on the native host for a JSDoc-typed function while the classic host displayed correct types
 * (today) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/65167#issuecomment-6624972361) **1-DARK** explained that the issue was due to missing JS filename, demonstrated that specifying a .js file fixes completions, added a regression test, and suggested closing the issue as not a bug

### [Issue microsoft/TypeScript#65170](https://github.com/microsoft/TypeScript/issues/65170) (Closed, `Bug`, **RyanCavanaugh**, **Copilot**)

**Erasing \`as\` or \`satisfies\` can expose an invalid left operand of \`\*\*\`**

*Under erasableSyntaxOnly mode, erasing 'as' or 'satisfies' assertions can expose unparenthesized operands for '**', resulting in invalid JavaScript without diagnostics.*

 * created by **magic-akari**
 * (today) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`
 * [later](https://github.com/microsoft/TypeScript/issues/65170#issuecomment-6627538836) **magic-akari** said "What is the intended direction for fixing this? Should these expressions be rejected only with erasableSyntaxOnly, or should they be rejected in all configurations?"

### [Issue microsoft/TypeScript#65172](https://github.com/microsoft/TypeScript/issues/65172) (Closed)

**Native declaration emit drops \`Object\.defineProperty\(C\.prototype, …\)\` accessors**

*Native TypeScript declaration emit omits prototype getters/setters defined via Object.defineProperty, breaking accessor declarations in .d.ts files.*

 * created by **timurzvural**
 * [today](https://github.com/microsoft/TypeScript/issues/65172#issuecomment-6601836127) **timurzvural** clarified that tsc/CHANGES.md drops constructor-function and prototype expando support in favor of class, noted that class + Object.defineProperty(Class.prototype, …) path still works, and mentioned that the function C() form shows defineProperty-on-prototype emit but may be out of scope
 * [today](https://github.com/microsoft/TypeScript/issues/65172#issuecomment-6602664732) **hkleungai** suggested updating change.md to explicitly deprecate prototype-style methods in all scenarios
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#65174](https://github.com/microsoft/TypeScript/issues/65174) (Closed)

**Native tsc: presence of \`assert\` import suppresses TS2856 on \`with\` imports \(CJS\)**

*In native tsc, an import assertion suppresses TS2856 errors for JSON imports using 'with' attributes in CommonJS modules.*

 * created by **timurzvural**
 * [today](https://github.com/microsoft/TypeScript/issues/65174#issuecomment-6602405240) **timurzvural** provided a related matrix showing TypeScript error codes for with and assert imports under different module settings
 * [today](https://github.com/microsoft/TypeScript/issues/65174#issuecomment-6612570929) **RyanCavanaugh** said "Dropping support for with was in the release notes. This is not a bug."
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#65175](https://github.com/microsoft/TypeScript/issues/65175) (Closed, `Working as Intended`)

**Native tsc: \`assert\` under unsupported \`\-\-module\` reports TS2880 instead of TS2821**

*Native tsc reports TS2880 rather than TS2821 for import assertions under unsupported --module settings like es2020.*

 * created by **timurzvural**
 * [today](https://github.com/microsoft/TypeScript/issues/65175#issuecomment-6602435843) **timurzvural** said "Same assert-handling area as #65174."
 * **RyanCavanaugh** added label `Working as Intended`
 * [today](https://github.com/microsoft/TypeScript/issues/65175#issuecomment-6610104069) **RyanCavanaugh** mentioned that this is in the release notes and attached an image
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#65279](https://github.com/microsoft/TypeScript/pull/65279) (Closed, `For Uncommitted Bug`)

**Erase types in preserved const enum initializers**

*Remove types from const enum initializers to ensure valid JavaScript output when constant evaluation fails while retaining the const modifier.*

 * created by **magic-akari**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/65279#issuecomment-6609363924) **jakebailey** suggested splitting the changes into two commits for easier review
 * [today](https://github.com/microsoft/TypeScript/pull/65279#issuecomment-6609480641) **magic-akari** agreed to split the changes into two commits as requested
 * [today](https://github.com/microsoft/TypeScript/pull/65279#issuecomment-6609601023) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [today](https://github.com/microsoft/TypeScript/pull/65279#issuecomment-6609842312) **magic-akari** explained that the change affected emit during error recovery, that the compiler still reported TS2474 and stripped type syntax from enum initializers to match TS6, and offered to close the PR if the edge case was too minor
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#65281](https://github.com/microsoft/TypeScript/issues/65281) (Closed, `Not a Defect`)

**Native LS: missing TS80004 suggestion and "Annotate with type from JSDoc" quick fix**

*Native TypeScript LSP fails to offer TS80004 suggestion or 'Annotate with type from JSDoc' quick fix for JSDoc annotations.*

 * created by **timurzvural**
 * [today](https://github.com/microsoft/TypeScript/issues/65281#issuecomment-6609142709) **RyanCavanaugh** said "@timurzvural I am going to ban you for spamming if you don't stop this immediately"
 * [today](https://github.com/microsoft/TypeScript/issues/65281#issuecomment-6609304875) **RyanCavanaugh** stated that agent-driven bulk contributions were not permitted, deleted the issues, and asked for acknowledgment
 * [today](https://github.com/microsoft/TypeScript/issues/65281#issuecomment-6609329051) **RyanCavanaugh** said "Applying a 3-day block to stop incoming spam"
 * **RyanCavanaugh** added label `Not a Defect`

### [PR microsoft/TypeScript#65283](https://github.com/microsoft/TypeScript/pull/65283) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**Make index signature declarations without a type annotation an implicit any, not a grammar error**

*Index signature declarations without explicit type annotations now default to implicit any rather than causing a grammar error.*

 * created by **andrewbranch**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#65284](https://github.com/microsoft/TypeScript/pull/65284) (Open, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**Restrict content mapper extensions to a single dot**

*Prohibit content mapper extensions with multiple dots to simplify implementation and avoid confusing moduleSuffixes interactions.*

 * created by **andrewbranch**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript/pull/65284#issuecomment-6612111669) **jakebailey** said "Would this break say, .tar.gz?"
 * [today](https://github.com/microsoft/TypeScript/pull/65284#issuecomment-6612147209) **andrewbranch** said "Yep, exactly."
 * [today](https://github.com/microsoft/TypeScript/pull/65284#issuecomment-6612192072) **andrewbranch** proposed prohibiting overlapping extension registrations to reduce complexity

### [PR microsoft/TypeScript#65285](https://github.com/microsoft/TypeScript/pull/65285) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Reject malformed API string table offsets**

*Add bounds checking and error handling to reject malformed API string table offsets causing server crashes.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#65286](https://github.com/microsoft/TypeScript/pull/65286) (Open, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Negated Types: Remove the concept of control\-flow made "fresh" negations**

*Allow full negated types in control flow instead of fresh negations, potentially breaking exact type matches and increasing overhead.*

 * created by **weswigham**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **weswigham**

### [Issue microsoft/TypeScript#65287](https://github.com/microsoft/TypeScript/issues/65287) (Closed, `Bug`, **weswigham**, **Copilot**)

**Downlevel emit of \`\|\|=\`, \`&&=\`, \`??=\` and \`\*\*=\` evaluates a member target twice when it has \`\!\`, \`as\` or \`satisfies\`**

*Downlevel emit of ||=, &&=, ??=, and **= with type-only assertions duplicates target evaluation, causing side effects.*

 * created by **zloirock**
 * (today) **RyanCavanaugh** added label `Bug`, set milestone to `Backlog`, assigned to **Copilot**, **RyanCavanaugh**, **Copilot**, **weswigham**, and unassigned **Copilot**, **RyanCavanaugh**
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript#65288](https://github.com/microsoft/TypeScript/pull/65288) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Reject visitor removal of required children**

*Reject visitors returning null for required AST children to prevent invalid tree construction and downstream errors.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/65288#issuecomment-6613622432) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/65288#issuecomment-6613624250) **typescript-automation[bot]** reported performance test jobs started and provided result links
 * [today](https://github.com/microsoft/TypeScript/pull/65288#issuecomment-6614912562) **typescript-automation[bot]** provided perf run results for the requested comparison

### [PR microsoft/TypeScript#65289](https://github.com/microsoft/TypeScript/pull/65289) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**Add \`\-\-disableDynamicImportExtensionRewriting\`**

*Add `--disableDynamicImportExtensionRewriting` compiler flag to suppress extension rewriting for dynamic import and require calls when `--rewriteRelativeImportExtensions` is enabled.*

 * created by **andrewbranch**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript/pull/65289#issuecomment-6615580819) **RyanCavanaugh** said "We're using isStringLiteralLike ("foo" and NoSubstitutionLiteral) in checker but isStringLiteral in the emitter ("foo" only) - intentional or oversight?"
 * [today](https://github.com/microsoft/TypeScript/pull/65289#issuecomment-6616115768) **andrewbranch** said "It was a previous oversight. Fixed in the latest commit."
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript#65290](https://github.com/microsoft/TypeScript/issues/65290) (Open)

**\`tsc \-\-watch\` in virtual machine fails with \`fanotify\_mark on '\.\.\.' failed: invalid cross\-device link\` trying to watch parent directories**

*tsc --watch in TypeScript 7 fails on virtiofs-mounted directories with 'invalid cross-device link' fanotify_mark error*

 * created by **michael42**

### [PR microsoft/TypeScript#65291](https://github.com/microsoft/TypeScript/pull/65291) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Add order dependence tests**

*Add a checkOrder test option with fuzzed ordering variants to uncover and eliminate over 500 order-dependent bugs.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#65292](https://github.com/microsoft/TypeScript/pull/65292) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Various order dependence fixes**

*Remove reliance on caches and arbitrary IDs to enforce deterministic ordering and consistent type identity*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#65293](https://github.com/microsoft/TypeScript/pull/65293) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Make checker behavior order independent**

*Adopt a memo-based state system to eliminate order dependence in the TypeScript checker, unify recursion handling, and manage cycles robustly.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/65293#issuecomment-6616507155) **Copilot** reported failure of custom setup steps during the Copilot code review run

### [PR microsoft/TypeScript#65295](https://github.com/microsoft/TypeScript/pull/65295) (Closed, `Author: Team`, `For Uncommitted Bug`, **RyanCavanaugh**, **Copilot**)

**\[WIP\] Fix downlevel emit of logical assignment operators**

*TypeScript’s downlevel emit of logical and exponentiation assignment operators incorrectly evaluates asserted or cast member targets twice, leading to unintended side effects.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Milestone Bug`, `For Milestone Bug`, `For Milestone Bug`, `For Uncommitted Bug`, and removed label `For Milestone Bug`
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#65296](https://github.com/microsoft/TypeScript/pull/65296) (Open, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Negated Types: Consider assertions invertible and create negated narrowings in false branches of assertion narrowings**

*Suggests making type guard assertions invertible to produce negated narrowings, but warns of potential unsoundness when guards are less precise.*

 * created by **weswigham**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **weswigham**

### [PR microsoft/TypeScript#65297](https://github.com/microsoft/TypeScript/pull/65297) (Closed, `Author: Team`, `For Uncommitted Bug`, **RyanCavanaugh**, **Copilot**)

**Preserve single evaluation of wrapped compound assignment targets**

*Unwrap type erasure wrappers before lowering compound assignments to avoid duplicate evaluation of property or element access targets.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `Author: Team`, `For Milestone Bug`, `For Milestone Bug`, `For Uncommitted Bug`, and removed label `For Milestone Bug`
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript#65298](https://github.com/microsoft/TypeScript/pull/65298) (Open, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Negated Types: Remove the \`TypeFacts\` abstraction and make type refinements directly**

*Refactor negated types to eliminate the TypeFacts abstraction and apply type refinements directly using improved control flow.*

 * created by **weswigham**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **weswigham**

### [PR microsoft/TypeScript#65299](https://github.com/microsoft/TypeScript/pull/65299) (Closed, `Author: Team`, `For Uncommitted Bug`, **RyanCavanaugh**, **Copilot**)

**Respect parameter\-initializer scope for body function declarations**

*Include function declarations in parameter-initializer scope checks to prevent inner functions from shadowing outer bindings during type checking.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `Author: Team`, `For Milestone Bug`, `For Uncommitted Bug`, and removed label `For Milestone Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/65299#issuecomment-6619726294) **RyanCavanaugh** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/65299#issuecomment-6619727792) **typescript-automation[bot]** updated CI build statuses for test top400, user test this, run dt, and perf test this faster
 * [today](https://github.com/microsoft/TypeScript/pull/65299#issuecomment-6620253597) **typescript-automation[bot]** notified that the DT test results were ready and unchanged
 * [today](https://github.com/microsoft/TypeScript/pull/65299#issuecomment-6620312943) **typescript-automation[bot]** reported that everything looked good after running user tests with tsc comparing baseline and pr
 * [today](https://github.com/microsoft/TypeScript/pull/65299#issuecomment-6620501535) **typescript-automation[bot]** reported the perf run results for the requested comparison
 * [today](https://github.com/microsoft/TypeScript/pull/65299#issuecomment-6621052262) **typescript-automation[bot]** reported that the tsc comparison of the top 400 repos between baseline and PR showed no issues

### [Issue microsoft/TypeScript#65300](https://github.com/microsoft/TypeScript/issues/65300) (Open)

**\[api\] Concurrent createSnapshot calls can deadlock on projects entering one extends cycle**

*Concurrent TypeScript async API createSnapshot calls deadlock when tsconfig files form a circular extends cycle.*

 * created by **cplieger**

### [Issue microsoft/TypeScript#65301](https://github.com/microsoft/TypeScript/issues/65301) (Open)

**\[api\] createSnapshot drops options a project inherits through a circular extends chain**

*createSnapshot drops inherited strict option when tsconfig files form a circular extends chain*

 * created by **cplieger**

### [PR microsoft/TypeScript#65302](https://github.com/microsoft/TypeScript/pull/65302) (Open, `For Uncommitted Bug`)

**\[api\] Parse a new owner cache entry without holding its lock**

*Move parsing out of lock in OwnerCache.LoadAndAcquire to avoid deadlocks on circular config extensions*

 * created by **cplieger**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [PR microsoft/TypeScript#65303](https://github.com/microsoft/TypeScript/pull/65303) (Open, `For Uncommitted Bug`)

**\[api\] Reparse extended configs cached under another resolution stack**

*Circular extends chains cause incomplete extended configs to be cached incorrectly, resulting in wrong compiler options in API projects.*

 * created by **cplieger**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [PR microsoft/TypeScript#65304](https://github.com/microsoft/TypeScript/pull/65304) (Open, `For Milestone Bug`, **johnfav03**)

**\[api\] Own the configs a cached extended config extends**

*GetExtendedConfig’s cache hit doesn’t add ownership for extended configs, causing panics on missing entries.*

 * created by **cplieger**
 * (today) **typescript-automation[bot]** added label `For Milestone Bug`, and assigned to **johnfav03**

### [PR microsoft/TypeScript#65305](https://github.com/microsoft/TypeScript/pull/65305) (Open, `Domain: Performance`, `For Uncommitted Bug`)

**API: poll briefly before blocking on the sync channel**

*The TypeScript API’s synchronous channel now polls for up to 100 microseconds before blocking to reduce latency and improve performance.*

 * created by **WinterYukky**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [Issue microsoft/TypeScript#65306](https://github.com/microsoft/TypeScript/issues/65306) (Open)

**Escaped get/set/static followed by a line break is parsed as an accessor/static modifier instead of a field name \(TS1260\)**

*TypeScript misparses escaped get, set, or static identifiers at line endings as class member modifiers instead of field names, triggering TS1260 errors.*

 * created by **trackoor**

### [PR microsoft/TypeScript#65307](https://github.com/microsoft/TypeScript/pull/65307) (Open, `For Backlog Bug`)

**Add fourslash test for JSDoc @this/@param types in JS files**

*Add a fourslash test verifying that JSDoc @this and @param types in JS files power completions, hover, and signature help.*

 * created by **1-DARK**
 * [today](https://github.com/microsoft/TypeScript/pull/65307#issuecomment-6624971578) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (today) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Backlog Bug`, and removed label `For Uncommitted Bug`

### [PR microsoft/TypeScript#65308](https://github.com/microsoft/TypeScript/pull/65308) (Open, `Domain: Performance`, `For Backlog Bug`)

**Stop unbounded memory growth after type complexity limits are hit**

*Improve TypeScript checker to stop unbounded memory growth by halting expensive type expansions after reporting complexity-limit errors.*

 * created by **1-DARK**
 * **typescript-automation[bot]** added label `For Backlog Bug`

### [Issue microsoft/TypeScript#65309](https://github.com/microsoft/TypeScript/issues/65309) (Closed, `Bug`, **RyanCavanaugh**, **Copilot**)

**TS1450 \(wrong number of \`import\(\)\` arguments\) is reported with category "message" instead of "error"**

*The wrong number of import() arguments triggers TS1450 diagnostics with category message rather than error, misleading editors and tools.*

 * created by **trackoor**

### [Issue microsoft/TypeScript#65310](https://github.com/microsoft/TypeScript/issues/65310) (Open)

**Unicode data is still 15\.1: identifiers and RegExp property values from Unicode 16/17 are rejected**

*TypeScript still uses Unicode 15.1 data, causing identifiers and RegExp Unicode properties from Unicode 16/17 to be rejected.*

 * created by **trackoor**

### [Issue microsoft/TypeScript#65311](https://github.com/microsoft/TypeScript/issues/65311) (Open, `Bug`)

**\`in\` inside an array literal in a \`for\` initializer is a syntax error \(\`for \(let i = 0, a = \[k in o\]; …\)\`\)**

*TypeScript incorrectly treats ‘in’ inside array literals within for-loop initializers as syntax errors, unlike similar contexts.*

 * created by **trackoor**
 * [later](https://github.com/microsoft/TypeScript/issues/65311#issuecomment-6629428265) **MartinJohns** said "Why would you ever write code like this?"

### [PR microsoft/TypeScript#65312](https://github.com/microsoft/TypeScript/pull/65312) (Closed, `For Milestone Bug`, **RyanCavanaugh**)

**Report an error when erasing as/satisfies exposes an invalid left operand of \*\***

*Report errors when using as/satisfies to wrap unary, await, or type assertions as the left operand of exponentiation.*

 * created by **0xABCD01**
 * **typescript-automation[bot]** added label `For Backlog Bug`

### [Issue microsoft/TypeScript#65313](https://github.com/microsoft/TypeScript/issues/65313) (Open)

**Content mappers for tagged template literals**

*Propose supporting content mappers for tagged template literals to type-check embedded languages without altering emitted code.*

 * created by **OliverJAsh**
 * [later](https://github.com/microsoft/TypeScript/issues/65313#issuecomment-6632676916) **hkleungai** noted existing IDE extensions like es6-string-html that provide syntax highlighting on multiline string literals and suggested using jsdoc-style directives on pure strings instead of limiting to tagged template literals

