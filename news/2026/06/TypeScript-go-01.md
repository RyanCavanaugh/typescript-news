# Report for 2026-06-01 (Monday, June 1st, 2026)

18 different users commented on 104 different issues.

## Recommended Actions

 * Response Recommended
    * @kuishou68 requested a re-review after adding tests in [microsoft/TypeScript-go#3618](https://github.com/microsoft/TypeScript-go/pull/3618#issuecomment-4597839476)
    * @kuishou68 requested a review after adding test cases in [microsoft/TypeScript-go#3618](https://github.com/microsoft/TypeScript-go/pull/3618#issuecomment-4598338818)
    * @alvarosevilla95 provided repro steps for nondeterministic tsgo failures in [microsoft/TypeScript-go#4060](https://github.com/microsoft/TypeScript-go/issues/4060#issuecomment-4595537911)
    * @mscrivo asked about reverting or fixing the linked optimization for macOS in [microsoft/TypeScript-go#4060](https://github.com/microsoft/TypeScript-go/issues/4060#issuecomment-4602713315)
    * @alvarosevilla95 provided repro test results narrowing the commit range in [microsoft/TypeScript-go#4060](https://github.com/microsoft/TypeScript-go/issues/4060#issuecomment-4604057601)
    * @mscrivo provided repro steps as requested in [microsoft/TypeScript-go#4060](https://github.com/microsoft/TypeScript-go/issues/4060#issuecomment-4604143384)
    * @danyalahmed1995 opened PR #4172 with the fix and regression test in [microsoft/TypeScript-go#4079](https://github.com/microsoft/TypeScript-go/issues/4079#issuecomment-4597396462)
    * @danyalahmed1995 provided detailed analysis of UTF-16 vs UTF-8 type inference issue in [microsoft/TypeScript-go#4137](https://github.com/microsoft/TypeScript-go/issues/4137#issuecomment-4597074864)

## Activity Summary

### [PR microsoft/TypeScript-go#3354](https://github.com/microsoft/TypeScript-go/pull/3354) (Closed, **jakebailey**, **Copilot**)

**Fix panic in declaration emit for named CommonJS exports from \.cjs files**

*Add missing diagnostic context in transformCommonJSExport to prevent declaration emit panics for named CommonJS exports in .cjs files.*

 * (8 weeks ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3408](https://github.com/microsoft/TypeScript-go/pull/3408) (Closed, **jakebailey**, **Copilot**)

**Fix JSDoc disappearing on destructured parameters from intersection types**

*Ensure JSDoc comments appear on destructured parameters from intersection types by falling back to symbol declarations when ValueDeclaration is missing.*

 * (6 weeks ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3495](https://github.com/microsoft/TypeScript-go/pull/3495) (Open)

**Use JS\-compatible Unicode casing for intrinsic string mappings**

*Implement JavaScript-compatible Unicode casing rules in TypeScript’s intrinsic string mapping functions.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3495#issuecomment-4486782037) **Andarist** mentioned having used AI assistance to draft an uncommitted audit script for js casing and shared its code
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3495#issuecomment-4488896476) **jakebailey** said "What were the results of the analysis? What is the difference?"
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3495#issuecomment-4489383166) **Andarist** reported no divergences between the implementation and v8 except for toLowerCase final-sigma contexts in rΣ strings, providing example outputs
 * [today](https://github.com/microsoft/TypeScript-go/pull/3495#issuecomment-4598934154) **jakebailey** asked to ensure testing of toLowerCase final-sigma context divergences for strings of the form rΣ
 * [today](https://github.com/microsoft/TypeScript-go/pull/3495#issuecomment-4599345981) **Andarist** questioned whether tests were required for all 267 items, noting an existing unit test included a single example of divergence
 * [later](https://github.com/microsoft/TypeScript-go/pull/3495#issuecomment-4600953236) **jakebailey** said "No, not all of them I don't think, but a few. Or some sort of way to generate them and then use https://github.com/microsoft/typescript-go/tree/main/internal/testutil/jstest to cross check?"

### [PR microsoft/TypeScript-go#3618](https://github.com/microsoft/TypeScript-go/pull/3618) (Open)

**fix: prevent wildcard pattern from overriding exact match in FindBestPatternMatch**

*Assign math.MaxInt for exact matches in FindBestPatternMatch to ensure wildcard patterns cannot override exact matches.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3618#issuecomment-4527804370) **kuishou68** said "I have added the test cases as requested. Could you please take another look?"
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * [today](https://github.com/microsoft/TypeScript-go/pull/3618#issuecomment-4590877856) **kuishou68** explained why they traced tsconfig paths resolution, identified and fixed the StarIndex logic in FindBestPatternMatch, and added the requested test cases while requesting another review
 * [today](https://github.com/microsoft/TypeScript-go/pull/3618#issuecomment-4597839476) **kuishou68** added test cases covering exact match behavior and wildcard patterns in internal/core/pattern_test.go and requested a re-review
 * [today](https://github.com/microsoft/TypeScript-go/pull/3618#issuecomment-4598338818) **kuishou68** followed up on the PR, added requested test cases, and requested another review

### [PR microsoft/TypeScript-go#3702](https://github.com/microsoft/TypeScript-go/pull/3702) (Closed)

**Update dependencies**

*Update npm, Go, golangci-lint, jsonv2, and dprint plugin dependencies (including gofumpt).*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3807](https://github.com/microsoft/TypeScript-go/pull/3807) (Closed, **jakebailey**, **Copilot**)

**Fix stack overflow on circular reference after \`satisfies\`**

*Pass checkMode to skip assignability checks in satisfies expressions during serialization to prevent circular stack overflow*

 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3807#issuecomment-4427900074) **Copilot** described the issue as a porting bug and explained why Strada didn’t hit it due to lacking the pseudochecker path, outlining the cyclic call sequence in the Go port
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3807#issuecomment-4444350161) **weswigham** explained that the issue arose from creating a fresh node builder on each invocation rather than caching it, compared it to strada's behavior, and suggested caching a single node builder for intra-checker usage
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3975](https://github.com/microsoft/TypeScript-go/pull/3975) (Closed, `dependencies`, `javascript`)

**Bump brace\-expansion from 5\.0\.5 to 5\.0\.6**

*Bump brace-expansion dependency from version 5.0.5 to 5.0.6.*

 * created by **dependabot[bot]**
 * (2 weeks ago) **dependabot[bot]** added labels `dependencies`, `javascript`
 * [today](https://github.com/microsoft/TypeScript-go/pull/3975#issuecomment-4596965795) **dependabot[bot]** said "Looks like brace-expansion is up-to-date now, so this is no longer needed."
 * (today) **dependabot[bot]** closed the issue

### [Issue microsoft/TypeScript-go#3983](https://github.com/microsoft/TypeScript-go/issues/3983) (Closed)

**Declaration emit leaks namespace declarations for \`@internal\` functions with static property assignments**

*tsgo includes namespace declarations for internal functions with static property assignments in .d.ts files even when stripInternal is enabled*

 * **RyanCavanaugh** added label `wontfix`
 * [6 days ago](https://github.com/microsoft/TypeScript-go/issues/3983#issuecomment-4549240811) **RyanCavanaugh** said "stripInternal is "use at your own risk""
 * (6 days ago) **RyanCavanaugh** closed the issue
 * (today) **jakebailey** reopened the issue
 * **jakebailey** removed label `wontfix`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3995](https://github.com/microsoft/TypeScript-go/pull/3995) (Closed)

**fix\(declarations\): strip synthesized namespace for @internal expando functions**

*With stripInternal enabled, remove synthesized namespaces for @internal expando functions in declaration output.*

 * created by **Zelys-DFKH**
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3995#issuecomment-4492452751) **RyanCavanaugh** said "Closing automated PRs; please don't run automated coding tools against this repo. We're fully able to do that ourselves."
 * (1 week ago) **RyanCavanaugh** closed the issue
 * (today) **jakebailey** reopened the issue
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3998](https://github.com/microsoft/TypeScript-go/issues/3998) (Closed, `bug`, **andrewbranch**)

**Intermittent \`tsgo \-\-build\` TS2345: \`paths\` \+ \`@types/\*\` conflict \(\`tsc\` accepts\)**

*tsgo --build randomly fails with TS2345 errors caused by conflicting path aliases and @types/react types while tsc builds and single-threaded tsgo builds consistently succeed.*

 * (1 week ago) **RyanCavanaugh** added label `bug`, and set milestone to `TypeScript 7.0 RC`
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/3998#issuecomment-4502041513) **RyanCavanaugh** said "@andrewbranch both Copilot PRs above look plausible but they can't both be right."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4008](https://github.com/microsoft/TypeScript-go/pull/4008) (Closed, **RyanCavanaugh**, **Copilot**)

**Fix intermittent TS2345 with paths \+ @types/\* conflict in concurrent builds**

*Concurrent tsgo builds intermittently fail TS2345 because a race in the packageJsonInfoCache causes path aliases to resolve to @types packages.*

 * (1 week ago) **RyanCavanaugh** closed the issue
 * (3 days ago) **andrewbranch** reopened the issue
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/4008#issuecomment-4579739549) **Copilot** extracted duplicated directory correction into InfoCacheEntry.WithPackageDirectory with explanatory comment
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4015](https://github.com/microsoft/TypeScript-go/pull/4015) (Open)

**Do not emit declaration files when they contain a declaration emit error**

*Prevent TypeScript from emitting declaration files when declaration emit errors occur.*

 * created by **weswigham**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * [today](https://github.com/microsoft/TypeScript-go/pull/4015#issuecomment-4596890943) **jakebailey** said "Needs a main merge but otherwise LGTM"

### [PR microsoft/TypeScript-go#4027](https://github.com/microsoft/TypeScript-go/pull/4027) (Closed, `dependencies`, `javascript`)

**Bump @nevware21/ts\-utils from 0\.13\.0 to 0\.14\.0**

*Upgrade the @nevware21/ts-utils dependency from 0.13.0 to 0.14.0, adding various new array, string, and type inspection helper functions.*

 * (1 week ago) **dependabot[bot]** added labels `javascript`, `dependencies`, `javascript`
 * [today](https://github.com/microsoft/TypeScript-go/pull/4027#issuecomment-4596964912) **dependabot[bot]** said "Looks like @nevware21/ts-utils is up-to-date now, so this is no longer needed."
 * (today) **dependabot[bot]** closed the issue

### [PR microsoft/TypeScript-go#4032](https://github.com/microsoft/TypeScript-go/pull/4032) (Closed, `dependencies`, `javascript`)

**Bump uuid and @azure/msal\-node**

*Remove the unused uuid package and upgrade @azure/msal-node from v5.1.3 to v5.2.2*

 * (1 week ago) **dependabot[bot]** added labels `javascript`, `dependencies`, `javascript`
 * [today](https://github.com/microsoft/TypeScript-go/pull/4032#issuecomment-4596964781) **dependabot[bot]** said "Looks like these dependencies are no longer a dependency, so this is no longer needed."
 * (today) **dependabot[bot]** closed the issue

### [Issue microsoft/TypeScript-go#4035](https://github.com/microsoft/TypeScript-go/issues/4035) (Closed, `bug`, `Domain: Editor`, **gabritto**)

**VSCode bulk save \(Replace All / Save All across many \.ts files\) deadlocks the LSP server**

*Bulk replacing across many .ts files in VSCode deadlocks the TypeScript Native Preview LSP server, which doesn’t restart on reload.*

 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * (4 days ago) **gabritto** added label `bug`, and removed label `Needs Investigation`
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript-go#4036](https://github.com/microsoft/TypeScript-go/pull/4036) (Closed, `dependencies`, `javascript`)

**Bump qs from 6\.15\.1 to 6\.15\.2**

*Bump qs dependency to version 6.15.2 to include multiple stringify and parse fixes and updated tests.*

 * (1 week ago) **dependabot[bot]** added labels `javascript`, `dependencies`, `javascript`
 * [today](https://github.com/microsoft/TypeScript-go/pull/4036#issuecomment-4596965077) **dependabot[bot]** said "Looks like qs is up-to-date now, so this is no longer needed."
 * (today) **dependabot[bot]** closed the issue

### [Issue microsoft/TypeScript-go#4037](https://github.com/microsoft/TypeScript-go/issues/4037) (Closed, `bug`, **ahejlsberg**)

**TS2304 when a generic \(@template\) function JSDoc contains @overload**

*Generic functions documented with @template and @overload produce 'Cannot find name T' TS2304 errors in tsgo.*

 * [6 days ago](https://github.com/microsoft/TypeScript-go/issues/4037#issuecomment-4549213250) **ahejlsberg** proposed a TypeScript overload translation from JSDoc overloads and said they would include it in their PR
 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/4037#issuecomment-4556263858) **ahejlsberg** explained that the JSDoc @type annotation on the variable and tags on the function expression already worked and suggested recommending that pattern for overloads
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/4037#issuecomment-4580165398) **antichris** described having to rewrite code around overloaded arrow functions using single-use consts for type checking, deemed it not ideal but workable, and thanked maintainers
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#4039](https://github.com/microsoft/TypeScript-go/issues/4039) (Open, `Domain: Declaration Emit`, `Domain: Comment Emit`, **jakebailey**, **Copilot**)

**Behavior difference: Inline comment on arrow function parameters is emitted on tsc but not on tsgo**

*tsgo removes inline comments on arrow function parameters that tsc retains, resulting in lost parameter comments*

 * **RyanCavanaugh** added to milestone `Possible Improvement`
 * (6 days ago) **weswigham** added labels `Domain: Declaration Emit`, `Domain: Comment Emit`
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#4046](https://github.com/microsoft/TypeScript-go/issues/4046) (Closed, `Domain: Declaration Emit`)

**Behavior difference: Side\-effect imports of custom file extension are emitted by tsgo but not tsc**

*tsgo emits side-effect imports for custom file extensions in declaration files while tsc omits them.*

 * created by **hkleungai**
 * (6 days ago) **RyanCavanaugh** added label `Domain: Declaration Emit`, and set milestone to `Post-7.0`
 * [today](https://github.com/microsoft/TypeScript-go/issues/4046#issuecomment-4595405263) **jakebailey** said "@andrewbranch @weswigham Is this not the same thing as that previous thread where we were leaving these imports in? (I think the example there was import "fs", but I can't easily find it)"
 * [today](https://github.com/microsoft/TypeScript-go/issues/4046#issuecomment-4595458632) **andrewbranch** said "Yes, this is intentional: https://github.com/microsoft/typescript-go/pull/3756"
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#4047](https://github.com/microsoft/TypeScript-go/pull/4047) (Closed, `dependencies`, `github_actions`)

**Bump the github\-actions group across 1 directory with 2 updates**

*Bump codecov/codecov-action from 6.0.0 to 6.0.1 and update github/codeql-action in the repository root.*

 * (1 week ago) **dependabot[bot]** added labels `github_actions`, `dependencies`, `github_actions`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4057](https://github.com/microsoft/TypeScript-go/issues/4057) (Closed, `Domain: Declaration Emit`, `Needs Investigation`, **weswigham**)

**New isolatedDeclarations error with generic \`this\` parameter inference**

*Using a generic this parameter in a method triggers a TS9008 isolatedDeclarations error under tsgo despite working in TypeScript 6.0.*

 * (6 days ago) **RyanCavanaugh** added label `Domain: Declaration Emit`, set milestone to `TypeScript 7.0 RC`, and assigned to **weswigham**
 * (today) **weswigham** closed the issue

### [Issue microsoft/TypeScript-go#4060](https://github.com/microsoft/TypeScript-go/issues/4060) (Closed, `Crash`, **jakebailey**)

**Data race in module resolver — SIGSEGV in \`loadModuleFromTargetExportOrImport\` / \`OrderedMap\.Keys\` under concurrent goroutines**

*Concurrent access to OrderedMap.Keys within the module resolver's loadModuleFromTargetExportOrImport triggers a data race causing a SIGSEGV.*

 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/4060#issuecomment-4564424105) **mscrivo** identified that the crash started in version 20260515.1 through a binary search and offered to provide repo access
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/4060#issuecomment-4564450769) **mscrivo** suggested a related PR and noted that the issue only occurred on macOS arm machines, not on Linux CI runners
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/4060#issuecomment-4574995897) **anotheri** reported experiencing the same issue and linked to a related issue with additional macOS AMD machine details
 * [today](https://github.com/microsoft/TypeScript-go/issues/4060#issuecomment-4595537911) **alvarosevilla95** reproduced nondeterministic tsgo failures including intermittent module resolution errors and SIGSEGV crashes when looping checks on macOS arm64
 * [later](https://github.com/microsoft/TypeScript-go/issues/4060#issuecomment-4602713315) **mscrivo** said "@DanielRosenwasser can we look at reverting or fixing that linked optimization for macOS?"
 * [later](https://github.com/microsoft/TypeScript-go/issues/4060#issuecomment-4603929052) **jakebailey** said "Have you bisected it down to that specific commit? It's not clear above if that's the case. If this is reproducible, I would like to have that repro so I can fix the code, if it's broken."
 * [later](https://github.com/microsoft/TypeScript-go/issues/4060#issuecomment-4604057601) **alvarosevilla95** reported running the repro on two released binaries around the relevant date, observed 30/30 clean runs on 20260514.1 and 25/30 clean with 5 bad runs on 20260515.1, and noted nondeterministic failures narrowing the suspect commit range to one including #3838
 * [later](https://github.com/microsoft/TypeScript-go/issues/4060#issuecomment-4604143384) **mscrivo** said "@jakebailey here you go: https://github.com/mscrivo/tsgo-resolver-race-repro .. make sure to run it on an arm based mac"

### [PR microsoft/TypeScript-go#4062](https://github.com/microsoft/TypeScript-go/pull/4062) (Closed)

**Check \`this\` params when comparing pseudotype signatures to type signatures**

*Include `this` parameters in comparisons between pseudotype signatures and actual type signatures.*

 * created by **weswigham**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript-go#4065](https://github.com/microsoft/TypeScript-go/pull/4065) (Closed)

**Revise logic for gathering JSDoc \`@template\` type parameters**

*Revise JSDoc @template parameter gathering logic to fix issue 4037 and document differences in CHANGES.md.*

 * created by **ahejlsberg**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/4065#issuecomment-4580869494) **ahejlsberg** explained that Strada collects all @template tags across the JSDoc block and provided an example using separate JSDoc comments for individual overload type parameters
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#4068](https://github.com/microsoft/TypeScript-go/pull/4068) (Closed, `dependencies`, `javascript`)

**Bump tmp from 0\.2\.5 to 0\.2\.7**

*Upgrade tmp dependency from version 0.2.5 to 0.2.7 to include input validation and relative path checks.*

 * (5 days ago) **dependabot[bot]** added labels `javascript`, `dependencies`, `javascript`
 * [today](https://github.com/microsoft/TypeScript-go/pull/4068#issuecomment-4596965012) **dependabot[bot]** said "Looks like tmp is up-to-date now, so this is no longer needed."
 * (today) **dependabot[bot]** closed the issue

### [Issue microsoft/TypeScript-go#4070](https://github.com/microsoft/TypeScript-go/issues/4070) (Closed, `Needs Investigation`, **DanielRosenwasser**, **Copilot**)

**typescript\.native\-preview\.tsdk: relative path in committed \.vscode/settings\.json gets overwritten with absolute path when accepting the workspace version prompt**

*Accepting the workspace version prompt for TypeScript Native Preview converts a relative tsdk path to an absolute one, dirtying settings.*

 * (4 days ago) **RyanCavanaugh** added label `Needs Investigation`, and set milestone to `TypeScript 7.0 RC`
 * **DanielRosenwasser** assigned to **Copilot**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#4072](https://github.com/microsoft/TypeScript-go/pull/4072) (Closed, **DanielRosenwasser**, **Copilot**)

**Fix tsdk relative path overwrite and unnecessary prompt on workspace open**

*Prevent committed relative tsdk paths from being overwritten with absolute paths and suppress redundant workspace version prompts.*

 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/4072#issuecomment-4578683832) **andrewbranch** said "@copilot setting useWorkspaceTsdkStorageKey to false will re-trigger the prompt..."
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/4072#issuecomment-4578730648) **Copilot** fixed prompt suppression logic by setting suppressPromptWorkspaceTsdk when selecting bundled TypeScript and clearing it when switching back
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/4072#issuecomment-4578900164) **Copilot** extracted `relativeWorkspacePath` as a constant and used it for both `joinPath` and the relative tsdk path calculation
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#4079](https://github.com/microsoft/TypeScript-go/issues/4079) (Open)

**Behavior difference: Notable difference regarding optional function argument type emits**

*tsgo outputs extra parentheses and verbose optional argument types unlike tsc’s simpler inferred function signatures.*

 * created by **hkleungai**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4079#issuecomment-4597396462) **danyalahmed1995** opened a PR to focus the fix on declaration emit for optional/defaulted parameters, added a regression test, and updated the baselines

### [Issue microsoft/TypeScript-go#4082](https://github.com/microsoft/TypeScript-go/issues/4082) (Open, `Crash`, **jakebailey**, **Copilot**)

**Panic in declaration emit for a set accessor with no parameters**

*A set accessor without parameters causes a panic in the typescript-go printer due to an AST node type mismatch.*

 * created by **mds-ant**
 * **mds-ant** added label `Crash`
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#4084](https://github.com/microsoft/TypeScript-go/issues/4084) (Open, `Crash`, **jakebailey**, **Copilot**)

**Panic in \`tryLoadInputFileForPath\` when an exports/imports target equals the declarationDir/outDir**

*A slice bounds panic occurs in tryLoadInputFileForPath when an exports or imports target matches declarationDir or outDir.*

 * created by **mds-ant**
 * **mds-ant** added label `Crash`
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#4085](https://github.com/microsoft/TypeScript-go/issues/4085) (Open, `Crash`, **jakebailey**, **Copilot**)

**Panic on overlapping wildcard patterns**

*A slice bounds out-of-range panic occurs when resolving modules with overlapping wildcard patterns in typescript-go.*

 * created by **mds-ant**
 * **mds-ant** added label `Crash`
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#4087](https://github.com/microsoft/TypeScript-go/issues/4087) (Closed)

**Spurious \`export\` modifier injected into a constructor type in \.d\.ts output**

*tsgo incorrectly injects an export modifier into constructor type declarations in generated .d.ts files*

 * created by **mds-ant**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4088](https://github.com/microsoft/TypeScript-go/issues/4088) (Open, **jakebailey**, **Copilot**)

**Expando function inside a namespace emits \`export declare namespace\`**

*tsgo wrongly emits export declare namespace for a function's expando property inside a namespace, breaking the declaration file.*

 * created by **mds-ant**
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#4094](https://github.com/microsoft/TypeScript-go/issues/4094) (Open, **jakebailey**, **Copilot**)

**Emitted JSX factory differs for @jsx pragma preceded by another @token in the same comment**

*tsgo misparses an @jsx pragma preceded by another token in the same comment, emitting h instead of React.createElement.*

 * created by **mds-ant**
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#4098](https://github.com/microsoft/TypeScript-go/issues/4098) (Open, **jakebailey**, **Copilot**)

**tsgo drops TS2527 and emits an invalid \.d\.ts when a class member's inferred type is an object literal containing \`this\`**

*tsgo ignores a TS2527 error and produces an invalid .d.ts file when a class method returns an object literal containing this.*

 * created by **mds-ant**
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#4101](https://github.com/microsoft/TypeScript-go/issues/4101) (Open)

**Declaration emit spends significant CPU in getAliasForSymbolInContainer / getAlternativeContainingModules**

*Declaration emit spends excessive CPU time in getAlternativeContainingModules and getAliasForSymbolInContainer, causing slow builds.*

 * created by **Zzzen**
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/4101#issuecomment-4583182120) **jakebailey** assured that the pprof files contain no sensitive information and can be shared as-is
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/4101#issuecomment-4585528342) **Zzzen** attached a CPU profile file and offered to provide a matching memory profile
 * [today](https://github.com/microsoft/TypeScript-go/issues/4101#issuecomment-4595134848) **jakebailey** said "Is this a regression? Or was it always this bad? I know I tried to improve this in #3232, so I'm curious"
 * [today](https://github.com/microsoft/TypeScript-go/issues/4101#issuecomment-4598707166) **Zzzen** analyzed performance across multiple commits and found the performance regression predates #3232, which only had a noise-level impact
 * [today](https://github.com/microsoft/TypeScript-go/issues/4101#issuecomment-4598726176) **jakebailey** asked to profile with tsc using pprof-it and share a frame graph screenshot
 * [today](https://github.com/microsoft/TypeScript-go/issues/4101#issuecomment-4598858952) **jakebailey** said "Can you try https://github.com/microsoft/typescript-go/pull/4176? (I see you have your own PR but I'm hoping this simpler change works)"
 * [today](https://github.com/microsoft/TypeScript-go/issues/4101#issuecomment-4599453902) **Zzzen** profiled the TypeScript build with pprof-it and PPROF_SANITIZE=on, reported command results including exit code TS5095, timings, memory usage, and main CPU and heap hotspots, and concluded that declaration emit, template-literal type matching, and GC were as significant as module-specifier/symbol-accessibility
 * [today](https://github.com/microsoft/TypeScript-go/issues/4101#issuecomment-4599474595) **Zzzen** tested the PR head against its parent in isolated worktrees and found no wall-time improvement but modestly reduced peak RSS
 * [later](https://github.com/microsoft/TypeScript-go/issues/4101#issuecomment-4600934687) **jakebailey** asked if issue #4102 worked and if the codebase was unavailable even under NDA
 * [later](https://github.com/microsoft/TypeScript-go/issues/4101#issuecomment-4601359723) **Zzzen** apologized and explained that the codebase is proprietary and cannot be shared due to internal dependencies and complex approval process
 * [later](https://github.com/microsoft/TypeScript-go/issues/4101#issuecomment-4601386649) **Zzzen** provided detailed benchmark results showing that PR #4102 reduced wall time by about 14.7% and increased peak memory usage by about 2.3%

### [PR microsoft/TypeScript-go#4114](https://github.com/microsoft/TypeScript-go/pull/4114) (Closed)

**fix\(4087\): fix declaration emit modifiers for constructor types**

*Adjusts declaration file emission to correctly include modifiers on constructor types.*

 * created by **a-tarasyuk**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4115](https://github.com/microsoft/TypeScript-go/issues/4115) (Open, **jakebailey**, **Copilot**)

**Exit codes 1 and 2 \(OutputsSkipped vs OutputsGenerated\) are swapped**

*tsgo swaps exit codes 1 and 2 for suppressed versus generated outputs compared to TypeScript 6.0*

 * created by **mds-ant**
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#4116](https://github.com/microsoft/TypeScript-go/issues/4116) (Open, **jakebailey**, **Copilot**)

**Declaration emit differs for negative numeric const literals**

*tsgo’s declaration emitter transforms negative numeric const literals into -Infinity or approximate values instead of preserving the original literal*

 * created by **mds-ant**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4116#issuecomment-4595112491) **jakebailey** said "Odd that we are not reusing these nodes."
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#4118](https://github.com/microsoft/TypeScript-go/issues/4118) (Open)

**Declaration emit drops expando function properties whose assignments are not top\-level expression statements**

*Tsgo's declaration emitter only emits expando function properties assigned as top-level statements and drops those assigned within initializers or blocks.*

 * created by **mds-ant**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4118#issuecomment-4595109846) **jakebailey** said "I suspect this is sort of intentional (or at least, was not thought of), given our reparsing system... Does anyone actually do this?"

### [Issue microsoft/TypeScript-go#4120](https://github.com/microsoft/TypeScript-go/issues/4120) (Open, **jakebailey**, **Copilot**)

**With multiple \`/\*\* @jsx \*/\` pragmas in one file, tsc uses the first and tsgo uses the last**

*When a file contains multiple /** @jsx */ pragmas, TypeScript’s compiler uses the first pragma but tsgo applies the last.*

 * created by **mds-ant**
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#4122](https://github.com/microsoft/TypeScript-go/issues/4122) (Closed)

**Different emit for import\.defer\(\) in a CommonJS module**

*tsgo emits a Promise.resolve().then wrapper for import.defer in CommonJS modules instead of preserving import.defer calls like TypeScript 6.0*

 * created by **mds-ant**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4122#issuecomment-4594203100) **a-tarasyuk** recalled that import.defer cannot be used with --module commonjs and asked if the lowering should be fixed and what the intended use case is
 * [today](https://github.com/microsoft/TypeScript-go/issues/4122#issuecomment-4594562881) **jakebailey** said "It's definitely an error, but I have no idea why this would be getting transformed; this isn't critical but I would be interested in a PR, sure."

### [Issue microsoft/TypeScript-go#4123](https://github.com/microsoft/TypeScript-go/issues/4123) (Closed, **jakebailey**, **Copilot**)

**\`in\`/\`out\` variance modifiers on a class member leak into the emitted JS**

*tsgo incorrectly preserves TypeScript ‘in’/‘out’ variance modifiers on class members in the emitted JavaScript instead of stripping them.*

 * created by **mds-ant**
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4124](https://github.com/microsoft/TypeScript-go/issues/4124) (Closed, **jakebailey**, **Copilot**)

**Different treatment for zero\-byte tsconfig\.json**

*tsgo returns a TS5083 error for a zero-byte tsconfig.json file, unlike TypeScript 6.0 which accepts it.*

 * created by **mds-ant**
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4125](https://github.com/microsoft/TypeScript-go/issues/4125) (Open, **jakebailey**, **Copilot**)

**'Duplicate function implementation' reported on function redeclaration in checked \.js files**

*tsgo erroneously reports TS2393 duplicate function implementation errors for function redeclarations in checked JavaScript files, whereas TypeScript 6.0 does not.*

 * created by **mds-ant**
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#4126](https://github.com/microsoft/TypeScript-go/issues/4126) (Closed)

**Spurious TS1024 when \`@readonly\` documents a get/set accessor or method in checked JS**

*A JSDoc @readonly on a get accessor in checked JavaScript incorrectly causes a TS1024 error under tsgo.*

 * created by **mds-ant**
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/4126#issuecomment-4586850091) **hkleungai** said "Seems to be a duplicate of https://github.com/microsoft/typescript-go/issues/3683."
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4127](https://github.com/microsoft/TypeScript-go/issues/4127) (Open)

**JSDoc @satisfies on export default is enforced by tsgo but ignored by tsc**

*tsgo enforces JSDoc @satisfies on export default assignments while tsc ignores the type mismatch*

 * created by **mds-ant**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4127#issuecomment-4594569156) **a-tarasyuk** asked whether JSDocSatisfiesTag should apply to a direct ExportAssignment
 * [today](https://github.com/microsoft/TypeScript-go/issues/4127#issuecomment-4594581173) **jakebailey** questioned whether this behavior in 6.0 was an oversight and provided a code snippet that errors
 * [today](https://github.com/microsoft/TypeScript-go/issues/4127#issuecomment-4594583449) **jakebailey** said "But maybe the "right" way is to stick @satisfies onto the expression inside the export."

### [Issue microsoft/TypeScript-go#4128](https://github.com/microsoft/TypeScript-go/issues/4128) (Open)

**JSDoc \`@type\` before \`return expr;\` acts as a type assertion in tsgo but is ignored in tsc**

*Tsgo incorrectly treats JSDoc @type annotations before return as type assertions, causing errors ignored by tsc.*

 * created by **mds-ant**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4128#issuecomment-4595097154) **jakebailey** said "This feels vaguely like #4127"

### [Issue microsoft/TypeScript-go#4129](https://github.com/microsoft/TypeScript-go/issues/4129) (Closed, **jakebailey**, **Copilot**)

**tsgo reports compiler\-option diagnostics even when syntactic errors exist**

*tsgo reports compiler-option errors even when syntactic errors exist, unlike TypeScript which prioritizes syntax diagnostics.*

 * created by **mds-ant**
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#4132](https://github.com/microsoft/TypeScript-go/issues/4132) (Closed, **jakebailey**, **Copilot**)

**tsgo reports different parameter name for incompatible function types**

*tsgo incorrectly uses the tuple rest parameter name 'args' instead of the declared parameter name when reporting incompatible function types*

 * created by **mds-ant**
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#4134](https://github.com/microsoft/TypeScript-go/issues/4134) (Closed, `bug`, **ahejlsberg**)

**tsgo does not report TS2565 for conditionally\-assigned expando function properties**

*tsgo fails to report TS2565 when accessing a conditionally-assigned expando property on a function, unlike TypeScript 6.0.*

 * created by **mds-ant**
 * (today) **ahejlsberg** added label `bug`, set milestone to `TypeScript 7.0 RC`, and assigned to **ahejlsberg**

### [Issue microsoft/TypeScript-go#4136](https://github.com/microsoft/TypeScript-go/issues/4136) (Closed)

**tsgo does not produce TS6053 for a missing root file**

*tsgo does not emit TS6053 file not found error for a missing root file*

 * created by **mds-ant**
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/4136#issuecomment-4589547405) **JoostK** said "https://github.com/microsoft/typescript-go/issues/3753"
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4137](https://github.com/microsoft/TypeScript-go/issues/4137) (Open, **jakebailey**)

**Single\-character template literal inference consumes a full code point in tsgo vs one UTF\-16 code unit in tsc**

*tsgo incorrectly infers single-character template literals by consuming only a UTF-16 code unit, mis-splitting multi-code-point characters like emojis.*

 * created by **mds-ant**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4137#issuecomment-4596974236) **danyalahmed1995** reproduced the issue locally and described a compiler parity discrepancy in emoji handling between tsgo and tsc
 * [today](https://github.com/microsoft/TypeScript-go/issues/4137#issuecomment-4597074864) **danyalahmed1995** investigated the mismatch and explained that naive changes split UTF-8 bytes incorrectly rather than matching tsc's UTF-16 code-unit handling, and noted that tsgo's use of Go strings requires a more complex representation to align with tsc
 * [today](https://github.com/microsoft/TypeScript-go/issues/4137#issuecomment-4597137700) **jakebailey** noted that the issue had a broader root cause, linked related unicode and encoding issues, and suggested using WTF-8 encoding

### [Issue microsoft/TypeScript-go#4148](https://github.com/microsoft/TypeScript-go/issues/4148) (Closed)

**hc\<\> RPC client instantiates ~12× more types under tsgo than tsc \(server app type at parity\)**

*tsgo generates about 12× more type instantiations than tsc when instantiating Hono’s hc<> RPC client over a chained .openapi app*

 * created by **daviduzumeri**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4148#issuecomment-4594566791) **jakebailey** said "Did you run with --checkers 1? The numbers reported are the total of all checkers."
 * [today](https://github.com/microsoft/TypeScript-go/issues/4148#issuecomment-4598283832) **daviduzumeri** said "Winner, winner, chicken dinner. Instantiation was inflated due to parallelism."
 * [today](https://github.com/microsoft/TypeScript-go/issues/4148#issuecomment-4598287059) **daviduzumeri** said "Sorry for the false alarm! No drift from TS6 at all, I think this is something to just take up with Hono in this case."
 * (today) **daviduzumeri** closed the issue

### [PR microsoft/TypeScript-go#4149](https://github.com/microsoft/TypeScript-go/pull/4149) (Closed)

**fix\(4122\): preserve import\.defer in CommonJS emit**

*Preserve import.defer statements when emitting CommonJS modules*

 * created by **a-tarasyuk**

### [PR microsoft/TypeScript-go#4150](https://github.com/microsoft/TypeScript-go/pull/4150) (Closed)

**Use fire and forget client request to avoid deadlocks**

*Switch to fire-and-forget client requests during synchronous handling to avoid server-client deadlocks under heavy load.*

 * created by **gabritto**
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript-go#4151](https://github.com/microsoft/TypeScript-go/pull/4151) (Closed)

**Use an expanding dynamic queue for LSP messages**

*Replace fixed-size message queues with a lock-free, channel-based dynamic queue for LSP messages to prevent deadlocks.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4151#issuecomment-4596311060) **gabritto** said "@typescript-bot perf test this"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4151#issuecomment-4596311720) **typescript-bot** notified that a perf test job started and provided links to the build status and results
 * [today](https://github.com/microsoft/TypeScript-go/pull/4151#issuecomment-4596495578) **typescript-bot** reported the requested performance run results
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4152](https://github.com/microsoft/TypeScript-go/pull/4152) (Closed, **jakebailey**, **Copilot**)

**Use tuple element label for parameter name in incompatible function type diagnostics**

*Modify function type compatibility messages to use a labeled tuple’s element name rather than its rest parameter name.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#4153](https://github.com/microsoft/TypeScript-go/pull/4153) (Closed, **jakebailey**, **Copilot**)

**Suppress compiler\-option diagnostics when syntactic errors exist**

*Update tsgo to suppress compiler-option diagnostics when syntactic errors are present, matching tsc’s behavior.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#4154](https://github.com/microsoft/TypeScript-go/pull/4154) (Open, **jakebailey**, **Copilot**)

**Fix spurious TS2393 on function redeclaration in checked \.js files**

*Skip duplicate implementation checking for function redeclarations in JavaScript files in the Go TypeScript port to avoid erroneous TS2393 diagnostics.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4154#issuecomment-4596406420) **jakebailey** said "@copilot+claude-opus-4.8 merge main into this PR"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4154#issuecomment-4596504613) **Copilot** merged origin/main into the branch, regenerated conflicting baselines, and confirmed build and tests passed

### [PR microsoft/TypeScript-go#4155](https://github.com/microsoft/TypeScript-go/pull/4155) (Closed, **jakebailey**, **Copilot**)

**Treat zero\-byte tsconfig\.json as an empty config**

*Treat zero-byte tsconfig.json files as valid empty configurations instead of reporting read errors.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4156](https://github.com/microsoft/TypeScript-go/pull/4156) (Closed, **jakebailey**, **Copilot**)

**Elide \`in\`/\`out\` variance modifiers from emitted JS**

*TypeScript now removes invalid ‘in’/‘out’ variance modifiers from class members in emitted JS while preserving valid ‘in’ operators and diagnostics.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4156#issuecomment-4596337044) **RyanCavanaugh** noted that syntactic validity of output JS wasn't guaranteed for malformed TS and compared it to a similar existing case
 * [today](https://github.com/microsoft/TypeScript-go/pull/4156#issuecomment-4596343134) **jakebailey** said "A while back I added something to our test harness that verified that all output code parses, and it does; I think surprisingly it was an invariant, we just were lacking many tests."
 * [today](https://github.com/microsoft/TypeScript-go/pull/4156#issuecomment-4596349644) **RyanCavanaugh** said "Yeah seems like a desirable property to have, even if Strada didn't have it"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4157](https://github.com/microsoft/TypeScript-go/pull/4157) (Open, **jakebailey**, **Copilot**)

**Use first @jsx/@jsxfrag pragma to match tsc behavior**

*Use the first @jsx/@jsxfrag pragma in tsgo to match tsc behavior and update utilities and tests accordingly.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#4158](https://github.com/microsoft/TypeScript-go/pull/4158) (Open, **jakebailey**, **Copilot**)

**Preserve source text for negative numeric literals in declaration emit**

*Preserve original source text for top-level negative numeric literals in declaration emit instead of normalizing them.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4158#issuecomment-4595857814) **jakebailey** said "@copilot+claude-opus-4.8 no test??"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4158#issuecomment-4595951958) **Copilot** added a compiler test covering negative and positive numeric literal behaviors with baselines

### [PR microsoft/TypeScript-go#4159](https://github.com/microsoft/TypeScript-go/pull/4159) (Open, **jakebailey**, **Copilot**)

**Fix swapped OutputsSkipped/OutputsGenerated exit codes**

*Swap tsgo exit code constants for OutputsSkipped and OutputsGenerated to align with tsc's exit statuses.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#4160](https://github.com/microsoft/TypeScript-go/pull/4160) (Open, **jakebailey**, **Copilot**)

**Preserve inline parameter comments on inferred function types in declaration emit**

*Retain inline parameter comments in generated declaration files for functions with inferred types by preserving parameter source positions.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#4161](https://github.com/microsoft/TypeScript-go/pull/4161) (Open, **jakebailey**, **Copilot**)

**Fix panic in declaration emit for a set accessor with no parameters**

*Declaration emit panics for parameterless set accessors because of a malformed type annotation, now fixed by using NewKeywordTypeNode.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#4162](https://github.com/microsoft/TypeScript-go/pull/4162) (Open, **jakebailey**, **Copilot**)

**Fix panic in tryLoadInputFileForPath when an exports/imports target equals the declarationDir/outDir**

*Prevent panic by guarding path fragment slicing when exports or imports target equals the declarationDir or outDir*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#4163](https://github.com/microsoft/TypeScript-go/pull/4163) (Open, **jakebailey**, **Copilot**)

**Fix panic on overlapping wildcard path patterns**

*Fix panic on overlapping wildcard patterns by requiring candidate length >= prefix+suffix and adding regression tests.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#4164](https://github.com/microsoft/TypeScript-go/pull/4164) (Open, **jakebailey**, **Copilot**)

**Fix expando function in namespace emitting invalid nested \`declare namespace\`**

*Fix generation of invalid nested declare namespace for expando function properties inside ambient namespaces.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#4165](https://github.com/microsoft/TypeScript-go/pull/4165) (Open, **jakebailey**, **Copilot**)

**Match TypeScript's per\-line pragma scanning for @jsx in multi\-line comments**

*Only consider the first @-token per line in multi-line comments when parsing pragmas, aligning with TypeScript.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#4166](https://github.com/microsoft/TypeScript-go/pull/4166) (Open, **jakebailey**, **Copilot**)

**Report TS2527 for inferred object\-literal types referencing \`this\` in declaration emit**

*Ensure TS2527 errors are reported for inferred object-literal types referencing this by updating pseudotypenodebuilder serialization flags.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#4167](https://github.com/microsoft/TypeScript-go/issues/4167) (Open, **jakebailey**, **Copilot**)

**tsgo mis\-parses \`\.await\` member access as top\-level await in module\-scope JS with JSDoc \(spurious TS1146/TS1161\)**

*tsgo incorrectly interprets .await property access as top-level await in JSDoc-annotated module-scope JavaScript*

 * created by **turadg**
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#4168](https://github.com/microsoft/TypeScript-go/pull/4168) (Closed)

**Fix tsdk selection issues**

*Differentiate TypeScript SDK prompts, fix relative path resolution, prevent untrusted package execution, and respect workspace trust changes*

 * created by **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#4169](https://github.com/microsoft/TypeScript-go/pull/4169) (Open, **jakebailey**, **Copilot**)

**Fix \`\.await\` member access mis\-parsed as top\-level await in JS modules with JSDoc**

*Fixes misinterpretation of `.await` member access in JS modules with JSDoc tags as top-level await.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#4170](https://github.com/microsoft/TypeScript-go/pull/4170) (Closed)

**Switch LSP VS discriminator prop to string literals**

*Switch the LSP VS discriminator property to a string literal type to simplify usage and eliminate model patches.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4171](https://github.com/microsoft/TypeScript-go/pull/4171) (Open)

**Consolidate LSP logs into single output pane**

*Provide a unified VS Code output channel consolidating TypeScript-native-preview server logs and optional LSP traces with configurable levels.*

 * created by **andrewbranch**

### [PR microsoft/TypeScript-go#4172](https://github.com/microsoft/TypeScript-go/pull/4172) (Open)

**Fix redundant undefined wrapping in optional parameter declaration emit**

*Update declaration emission for optional parameters to avoid redundant '| undefined' wrapping when types already include undefined*

 * created by **danyalahmed1995**

### [PR microsoft/TypeScript-go#4173](https://github.com/microsoft/TypeScript-go/pull/4173) (Closed)

**Consistently name VS types with prefix VS**

*Apply the Go-style VS prefix to all relevant types to ensure consistent naming*

 * created by **jakebailey**

