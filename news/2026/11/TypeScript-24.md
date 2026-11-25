# Report for 2026-11-24 (Tuesday, November 24th, 2026)

14 different users commented on 41 different issues.

## Recommended Actions

 * Response Recommended
    * @magurotuna provided additional test cases in submitted issue #65667 in [microsoft/TypeScript#65657](https://github.com/microsoft/TypeScript/issues/65657#issuecomment-7167049728)

## Activity Summary

### [Issue microsoft/TypeScript#63227](https://github.com/microsoft/TypeScript/issues/63227) (Open, `Not a Defect`, **ahejlsberg**)

**Inference from result of generic function no longer produces a union**

*Generic function inference no longer produces the expected union type in TypeScript 6.0, causing a valid deepEqual call to fail.*

 * [37 weeks ago](https://github.com/microsoft/TypeScript/issues/63227#issuecomment-4032636619) **Andarist** said "bisects to https://github.com/microsoft/TypeScript/pull/62502"
 * (36 weeks ago) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **ahejlsberg**
 * [later](https://github.com/microsoft/TypeScript/issues/63227#issuecomment-7167408434) **ahejlsberg** explained that the behavior was an intended effect of #62502, resulting from how inference candidates and regular versus literal object types were prioritized
 * (later) **ahejlsberg** added label `Not a Defect`, and removed label `Needs Investigation`

### [PR microsoft/TypeScript#64257](https://github.com/microsoft/TypeScript/pull/64257) (Open, `For Backlog Bug`)

**Fix non\-null discriminant narrowing consistency**

*Fix discriminant equality narrowing so small and large nullable unions consistently preserve null, undefined, and void constituents.*

 * [1 month ago](https://github.com/microsoft/TypeScript/pull/64257#issuecomment-6458080251) **z0rimo** asked @RyanCavanaugh to review the revised implementation and confirm whether the approach was acceptable
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64257#issuecomment-7109435783) **jakebailey** recommended force-pushing a cleaner commit history with separate test/baseline and fix commits
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64257#issuecomment-7124131251) **z0rimo** reworked the PR history into two commits: one adding the regression test with failing baselines and another containing the fix with updated baselines
 * [today](https://github.com/microsoft/TypeScript/pull/64257#issuecomment-7150161113) **z0rimo** updated the implementation to address review feedback, avoid a full union scan, document benchmark results and the alias-narrowing trade-off, and confirm that full validation passed locally

### [PR microsoft/TypeScript#64307](https://github.com/microsoft/TypeScript/pull/64307) (Closed, `For Milestone Bug`, **ahejlsberg**)

**Normalize distributed type parameters in conditional type relationships**

*Normalize both source and target distributed type parameters in conditional type relationships to fix regressions in type mapping.*

 * **typescript-automation[bot]** added label `For Milestone Bug`
 * [6 weeks ago](https://github.com/microsoft/TypeScript/pull/64307#issuecomment-6121069156) **Andarist** said "thanks @trevorade for extra test cases! :)"
 * [6 weeks ago](https://github.com/microsoft/TypeScript/pull/64307#issuecomment-6130659947) **Andarist** said "@jakebailey i synced this with the recent changes from main, so this should compile now 😉 "
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript#64375](https://github.com/microsoft/TypeScript/pull/64375) (Open, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Negated Types**

*Proposes adding negated types with `not T` syntax and control-flow support to preserve constraints and improve union filtering.*

 * [9 weeks ago](https://github.com/microsoft/TypeScript/pull/64375#issuecomment-5765204612) **weswigham** said "@typescript-bot test top1000"
 * [9 weeks ago](https://github.com/microsoft/TypeScript/pull/64375#issuecomment-5765206104) **typescript-automation[bot]** reported that the `test top1000` job started and provided links to its build status and results
 * [9 weeks ago](https://github.com/microsoft/TypeScript/pull/64375#issuecomment-5766455684) **typescript-automation[bot]** reported results from comparing the top 1,000 repositories with the main branch and the pull request merge, highlighting changed TypeScript errors for maintainer review
 * [today](https://github.com/microsoft/TypeScript/pull/64375#issuecomment-7144504191) **weswigham** announced that negated type control-flow behavior would be merged behind an opt-in compiler flag, while broader changes to invertible type guards would require future explicit syntax due to compatibility concerns
 * (today) **weswigham** closed the issue
 * (today) **weswigham** reopened the issue

### [PR microsoft/TypeScript#64376](https://github.com/microsoft/TypeScript/pull/64376) (Closed, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Negated Types: Change the meaning of \`{}\` to \`unknown & not null & not undefined\`**

*Change `{}` semantics to exclude null and undefined, while replacing literal-union normalization exceptions with enhanced type-origin tracking.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/64376#issuecomment-7116834657) **typescript-automation[bot]** reported that the requested jobs had started, with failures recorded for `run dt` and `perf test this faster`
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64376#issuecomment-7122046439) **typescript-automation[bot]** reported that the DT test run had failed and linked to the build log
 * [today](https://github.com/microsoft/TypeScript/pull/64376#issuecomment-7133481365) **typescript-automation[bot]** said "@weswigham, the perf run you requested failed. You can check the log here."
 * [today](https://github.com/microsoft/TypeScript/pull/64376#issuecomment-7141849983) **weswigham** said "@typescript-bot pack this"
 * [today](https://github.com/microsoft/TypeScript/pull/64376#issuecomment-7141852601) **typescript-automation[bot]** reported that the automated `pack this` job started and completed with results available.
 * [today](https://github.com/microsoft/TypeScript/pull/64376#issuecomment-7142050383) **github-actions[bot]** provided an installable package and playground for commit 128b0903a32142ae8b45fefd1e28af12e96c7b0b to support testing
 * [today](https://github.com/microsoft/TypeScript/pull/64376#issuecomment-7144949980) **weswigham** concluded that the proposed aliasing change added breakage and complexity without a motivating benefit, and said work would continue in PR #64375
 * (today) **weswigham** closed the issue

### [Issue microsoft/TypeScript#64437](https://github.com/microsoft/TypeScript/issues/64437) (Closed, `Bug`, **ahejlsberg**)

**\`keyof\` over computed property keys yields widening literal types, unlike the same object with literal keys**

*`keyof` on objects with computed property keys widens literal key unions to `string`, unlike equivalent objects with literal keys.*

 * (8 weeks ago) **RyanCavanaugh** added label `Needs Investigation`, removed label `Needs More Info`, and assigned to **ahejlsberg**
 * (today) **ahejlsberg** added label `Bug`, and removed label `Needs Investigation`
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript#64515](https://github.com/microsoft/TypeScript/pull/64515) (Closed, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Negated Types: Define Extract and Exclude in terms of intersections and negations**

*Proposes redefining Extract and Exclude using intersections and negations, while noting potential regressions such as Extract<T, any> becoming any.*

 * (8 weeks ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **weswigham**
 * [today](https://github.com/microsoft/TypeScript/pull/64515#issuecomment-7140218562) **weswigham** said "@typescript-bot test this"
 * [today](https://github.com/microsoft/TypeScript/pull/64515#issuecomment-7140222194) **typescript-automation[bot]** reported that the top400, user test, DT, and performance test jobs had started and linked to their build results
 * [today](https://github.com/microsoft/TypeScript/pull/64515#issuecomment-7141132467) **typescript-automation[bot]** reported that the DefinitelyTyped tests found branch-only TypeScript errors in the mdx package's Preact test configuration, where several `props` parameters implicitly had an `any` type
 * [today](https://github.com/microsoft/TypeScript/pull/64515#issuecomment-7141132761) **typescript-automation[bot]** reported additional DefinitelyTyped test results showing branch-only type errors in the ffi-napi tests
 * [today](https://github.com/microsoft/TypeScript/pull/64515#issuecomment-7141133035) **typescript-automation[bot]** reported additional DefinitelyTyped test results showing branch-only errors in the mpv-script package, including unused @ts-expect-error directives and type mismatches
 * [today](https://github.com/microsoft/TypeScript/pull/64515#issuecomment-7141133327) **typescript-automation[bot]** reported additional DefinitelyTyped test results showing branch-only TypeScript compile errors in clerk.io and react-blessed
 * [today](https://github.com/microsoft/TypeScript/pull/64515#issuecomment-7141133642) **typescript-automation[bot]** reported additional DefinitelyTyped test results showing node/v24 branch-only TS2345 errors for Buffer and BigInt64Array in globals-dom.ts
 * [today](https://github.com/microsoft/TypeScript/pull/64515#issuecomment-7141852440) **weswigham** said "@typescript-bot pack this"
 * [today](https://github.com/microsoft/TypeScript/pull/64515#issuecomment-7141855317) **typescript-automation[bot]** reported that the automated build job started and completed successfully
 * [today](https://github.com/microsoft/TypeScript/pull/64515#issuecomment-7142053100) **github-actions[bot]** provided an installable package and playground for testing commit 5d931b81cc9e0badf680bd8ec61853f21170a165
 * [today](https://github.com/microsoft/TypeScript/pull/64515#issuecomment-7144761135) **typescript-automation[bot]** provided the requested performance run results comparing the baseline and PR
 * [today](https://github.com/microsoft/TypeScript/pull/64515#issuecomment-7144900663) **weswigham** reported that the experiment caused widespread breakage in `Extract`, would be pursued in PR #64375, and would not be included in the core negated types PR
 * (today) **weswigham** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/64515#issuecomment-7145427040) **typescript-automation[bot]** reported one infrastructure failure and a new TS2345 error in bcryptjs when comparing baseline and PR user-test results
 * [today](https://github.com/microsoft/TypeScript/pull/64515#issuecomment-7145428151) **typescript-automation[bot]** reported additional TypeScript errors found while running the user test suite, including new TS2345 errors in the Effect repository
 * [today](https://github.com/microsoft/TypeScript/pull/64515#issuecomment-7145429253) **typescript-automation[bot]** reported new TypeScript errors found in webpack while running the user tests suite

### [Issue microsoft/TypeScript#64673](https://github.com/microsoft/TypeScript/issues/64673) (Closed, `Needs Investigation`, **ahejlsberg**)

**TS2719 "Two different types with this name exist" between identical generic signatures with a distributive conditional parameter type \(regression from \#64237\)**

*Regression causes TS2719 when assigning identical generic signatures whose parameter uses a distributive conditional type.*

 * **RyanCavanaugh** added to milestone `TypeScript 7.1.1 RC`
 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/64673#issuecomment-6590090051) **tim-smart** reported that the TypeScript 7.1 regression also affected the Effect library, provided reproductions involving generic conditional return types and `catchTag`, and noted that the issue was absent in 7.0.2 and fixed by #64307
 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/64673#issuecomment-6704853284) **trackoor** reported that vuejs/core's `toHandlerKey` failed strict TypeScript checks in specific 7.1 nightly builds, provided a reduced reproduction and version range, and noted that #64307 fixed the issue
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript#64892](https://github.com/microsoft/TypeScript/issues/64892) (Closed, `Needs Investigation`, **ahejlsberg**)

**\[7\.1 Regression\] Unexpected behaviour change from Stronger Distributive Type checks**

*TypeScript 7.1 introduces TS2345 errors when invoking callbacks with generic parameters in conditionally typed methods.*

 * created by **hkleungai**
 * (1 month ago) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **ahejlsberg**
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript#64936](https://github.com/microsoft/TypeScript/pull/64936) (Open, `Domain: Performance`, `For Backlog Bug`)

**Avoid rebuilding later LSP project references**

*Avoid repeatedly rebuilding later LSP project references when a clean loaded project already contains the opened file.*

 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [1 month ago](https://github.com/microsoft/TypeScript/pull/64936#issuecomment-6368320130) **chengchuu** said "@microsoft-github-policy-service agree"
 * **jakebailey** added label `Domain: Performance`
 * [today](https://github.com/microsoft/TypeScript/pull/64936#issuecomment-7144097438) **andrewbranch** said "@chengchuu can you take a look at the "previously missed issue" from the Copilot review? Looks plausible. Thanks!"
 * [today](https://github.com/microsoft/TypeScript/pull/64936#issuecomment-7152406298) **chengchuu** mentioned that the follow-up preserved earlier `Find` positions for built projects, shared refreshes between paired `Find` and `Create` requests, and passed race tests and repository validation

### [PR microsoft/TypeScript#65010](https://github.com/microsoft/TypeScript/pull/65010) (Closed, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Negated Types: Constrain Promise\<T\> to forbid Thenable T**

*Constrain Promise<T> to reject potentially thenable primitive intersections without causing widespread breaking changes.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506934472) **typescript-automation[bot]** reported additional TypeScript errors found in the top 400 repositories suite, including constraint failures across vercel/chatbot files
 * [3 weeks ago](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506935501) **typescript-automation[bot]** reported additional top-400-repository suite results showing TypeScript constraint errors in the oh-my-claudecode project
 * [3 weeks ago](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-6506936436) **typescript-automation[bot]** reported additional changes found by the top-400-repositories suite, including TypeScript errors in the oh-my-codex project
 * [today](https://github.com/microsoft/TypeScript/pull/65010#issuecomment-7144841636) **weswigham** explained that the Promise constraint experiment was too breaking for core TypeScript, shared a declaration workaround for testing, and invited feedback on viable constraints
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript#65034](https://github.com/microsoft/TypeScript/pull/65034) (Closed, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Negated Types: Make conditional type produce substitutions with negated constraints in \(some\) false branches **

*Enable conditional types to infer negated constraints in false branches when primitive union constraints can be safely partitioned.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/65034#issuecomment-7116643264) **typescript-automation[bot]** reported new TS2367 errors in the Effect user-test results when comparing the baseline and PR, and asked the maintainer to investigate
 * [yesterday](https://github.com/microsoft/TypeScript/pull/65034#issuecomment-7117846521) **typescript-automation[bot]** reported results from comparing the baseline and PR TypeScript compiler runs across the top 400 repositories and flagged unexpected changes for review
 * [today](https://github.com/microsoft/TypeScript/pull/65034#issuecomment-7125759541) **typescript-automation[bot]** said "@weswigham, the perf run you requested failed. You can check the log here."
 * [today](https://github.com/microsoft/TypeScript/pull/65034#issuecomment-7141874497) **weswigham** said "@typescript-bot pack this"
 * [today](https://github.com/microsoft/TypeScript/pull/65034#issuecomment-7141877494) **typescript-automation[bot]** reported that the automated "pack this" job started and completed with results available
 * [today](https://github.com/microsoft/TypeScript/pull/65034#issuecomment-7142077195) **github-actions[bot]** provided an installable package and playground for commit bd55784b4b08337d3d54d49cdf2fc355094956eb, along with testing instructions
 * [today](https://github.com/microsoft/TypeScript/pull/65034#issuecomment-7144689496) **weswigham** reported that the experiment was complete, work would continue in #64375, and the proposal might be revisited after PR #64984 merged to reduce breaking changes
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript#65286](https://github.com/microsoft/TypeScript/pull/65286) (Closed, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Negated Types: Remove the concept of control\-flow made "fresh" negations**

*Enable full negated types in control-flow analysis instead of transient fresh negations, while addressing impacts on exact matching and performance.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/65286#issuecomment-7116325770) **typescript-automation[bot]** reported additional changes from the top 400 repositories suite, including build failures and TypeScript property errors in kortix-ai/CompanyOS
 * [yesterday](https://github.com/microsoft/TypeScript/pull/65286#issuecomment-7116326801) **typescript-automation[bot]** provided additional top-400 repository suite results, including VS Code projects that failed to build with the old TypeScript compiler and detailed diagnostics
 * [yesterday](https://github.com/microsoft/TypeScript/pull/65286#issuecomment-7116327797) **typescript-automation[bot]** reported additional top-400-repository suite results, including build failures and TypeScript errors in Supabase projects
 * [today](https://github.com/microsoft/TypeScript/pull/65286#issuecomment-7141876684) **weswigham** said "@typescript-bot pack this"
 * [today](https://github.com/microsoft/TypeScript/pull/65286#issuecomment-7141879827) **typescript-automation[bot]** reported that the automated `pack this` job started and linked to its results
 * [today](https://github.com/microsoft/TypeScript/pull/65286#issuecomment-7142200457) **github-actions[bot]** provided an installable package and playground for testing commit 6e68877c2b54e747e07cbb182807e5fe2124b069
 * [today](https://github.com/microsoft/TypeScript/pull/65286#issuecomment-7142661861) **weswigham** said "@typescript-bot perf test this"
 * [today](https://github.com/microsoft/TypeScript/pull/65286#issuecomment-7142665625) **typescript-automation[bot]** reported that the performance test job started and linked to its results
 * [today](https://github.com/microsoft/TypeScript/pull/65286#issuecomment-7142761086) **weswigham** said "Note form design: put this behind a flag"
 * [today](https://github.com/microsoft/TypeScript/pull/65286#issuecomment-7143844688) **typescript-automation[bot]** reported that the requested performance run results were available and included baseline-versus-PR compiler comparison data
 * [today](https://github.com/microsoft/TypeScript/pull/65286#issuecomment-7144612693) **weswigham** mentioned that the experiment was complete, work would continue in #64375, and the change would be merged into the base PR behind an opt-in flag because it could expose existing compilation failures, including some not caused by provably incorrect code
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript#65296](https://github.com/microsoft/TypeScript/pull/65296) (Closed, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Negated Types: Consider assertions invertible and create negated narrowings in false branches of assertion narrowings**

*Consider whether assertion narrowings should produce negated types in false branches, despite unsoundness when guards are less specific than their checks.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/65296#issuecomment-7113955054) **typescript-automation[bot]** reported that the DefinitelyTyped test run completed and identified branch-only errors in jquery/v3 and regex-not, including three type expectation mismatches in jquery/v3
 * [yesterday](https://github.com/microsoft/TypeScript/pull/65296#issuecomment-7114003930) **typescript-automation[bot]** reported new TypeScript errors found when comparing baseline and PR user-test results and asked the maintainer to review them
 * [yesterday](https://github.com/microsoft/TypeScript/pull/65296#issuecomment-7114192319) **typescript-automation[bot]** said "@weswigham, the perf run you requested failed. You can check the log here."
 * [today](https://github.com/microsoft/TypeScript/pull/65296#issuecomment-7141879600) **weswigham** said "@typescript-bot pack this"
 * [today](https://github.com/microsoft/TypeScript/pull/65296#issuecomment-7141882869) **typescript-automation[bot]** reported that the automated `pack this` job started and provided links to its run and results
 * [today](https://github.com/microsoft/TypeScript/pull/65296#issuecomment-7142075290) **github-actions[bot]** provided an installable npm package and playground for testing commit 8db7e43b9088cf298625f027b33112bdd0989c53
 * [today](https://github.com/microsoft/TypeScript/pull/65296#issuecomment-7144567304) **weswigham** reported that the experiment was complete, that work would continue in #64375, and that follow-up might occur after negated types merge pending new syntax for distinguishing type guards
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript#65298](https://github.com/microsoft/TypeScript/pull/65298) (Closed, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Negated Types: Remove the \`TypeFacts\` abstraction and make type refinements directly**

*Refactor negated types to remove the TypeFacts abstraction and implement type refinements directly, while evaluating performance implications.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/65298#issuecomment-7114839298) **typescript-automation[bot]** reported additional top-400-repository suite results, including PixiJS build failures and TypeScript errors observed with the old compiler
 * [yesterday](https://github.com/microsoft/TypeScript/pull/65298#issuecomment-7114840452) **typescript-automation[bot]** reported additional TypeScript changes and build errors found while running the top 400 repositories suite
 * [yesterday](https://github.com/microsoft/TypeScript/pull/65298#issuecomment-7114841583) **typescript-automation[bot]** reported additional changes from the top 400 repositories suite, including build failures and a TS2367 diagnostic in teableio/teable
 * [today](https://github.com/microsoft/TypeScript/pull/65298#issuecomment-7141882658) **weswigham** said "@typescript-bot pack this"
 * [today](https://github.com/microsoft/TypeScript/pull/65298#issuecomment-7141885465) **typescript-automation[bot]** reported that the automated `pack this` job started and provided links to its status and results
 * [today](https://github.com/microsoft/TypeScript/pull/65298#issuecomment-7142100373) **github-actions[bot]** provided an installable package and playground for commit 4c12244a932c6b169a887afd744fa6dbb28713ad
 * [today](https://github.com/microsoft/TypeScript/pull/65298#issuecomment-7144540168) **weswigham** said "Experiment done, work will continue in #64375 - this one's not gonna be taken. It's a big perf loss, even if conceptually building types is "sufficient"."
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript#65517](https://github.com/microsoft/TypeScript/pull/65517) (Closed, `For Milestone Bug`, **andrewbranch**)

**feat\(content\-mapper\): add diagnostic\-code selectors**

*Add diagnostic-code selectors to content-mapper directives, enabling code-specific suppression with protocol v10 support and validation for invalid selectors.*

 * (5 days ago) **typescript-automation[bot]** added label `For Milestone Bug`, removed label `For Uncommitted Bug`, and assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript/pull/65517#issuecomment-7146417229) **andrewbranch** explained that the change would not be included in 7.1 due to insufficient time to discuss alternatives before the release lock, and invited continued discussion on the original issue
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#65573](https://github.com/microsoft/TypeScript/pull/65573) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**Filter out more diagnostics from content mapper synthesized code**

*Filter verbatimModuleSyntax and isolatedModules diagnostics from synthesized content-mapper code while retaining them within user-authored verbatim ranges.*

 * (6 days ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/65573#issuecomment-7144061267) **andrewbranch** declined to make the change for now to preserve the option of enabling JS emit for content mappers in the future, noting that the issue was not currently critical
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#65647](https://github.com/microsoft/TypeScript/pull/65647) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**Allow getSymbol on any Node, overload for Declaration**

*Update `getSymbol` to accept any `Node` while preserving definite results for `Declaration`, and narrow `isExternalModule` accordingly.*

 * (yesterday) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#65648](https://github.com/microsoft/TypeScript/pull/65648) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**Enable ESLint on packages/typescript**

*Enable ESLint for packages/typescript by adopting Strada’s configuration and resolving existing violations using the experimental TypeScript 7 backend.*

 * (yesterday) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript/pull/65648#issuecomment-7137154937) **gabritto** said "This is pretty minor, but I feel like since the advent of inlay hints, the parameter name rule is perhaps unnecessary."
 * [today](https://github.com/microsoft/TypeScript/pull/65648#issuecomment-7137665106) **jakebailey** said "I wouldn't agree, given most code I read is not anywhere with inlay hints (and then I don't enable them anyway)"
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript#65654](https://github.com/microsoft/TypeScript/issues/65654) (Open, `Bug`, **RyanCavanaugh**, **Copilot**)

**Checking a generic indexed access against a large union of literal aliases takes 16 s on 7\.0\.2 \(5\.9 s on 5\.9\.3\)**

*TypeScript 7.0.2 significantly slows type-checking a generic indexed access against large unions of literal aliases compared with 5.9.3.*

 * created by **AlexandreDemartin**
 * (today) **RyanCavanaugh** added label `Bug`, set milestone to `Backlog`, and assigned to **Copilot**, **RyanCavanaugh**

### [PR microsoft/TypeScript#65656](https://github.com/microsoft/TypeScript/pull/65656) (Open, `For Backlog Bug`)

**Add tests for uncovered module resolution and specifier paths**

*Adds compiler tests covering three previously untested module resolution and declaration-emission paths without changing compiler behavior.*

 * created by **magurotuna**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/65656#issuecomment-7137693605) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (today) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`

### [Issue microsoft/TypeScript#65657](https://github.com/microsoft/TypeScript/issues/65657) (Open, `Possible Improvement`)

**No tests cover some module resolution and module specifier cases**

*Add compiler tests covering previously untested module resolution and module specifier code paths, based on bugs found in tsrs.*

 * created by **magurotuna**
 * [today](https://github.com/microsoft/TypeScript/issues/65657#issuecomment-7148268608) **RyanCavanaugh** requested that the additional test cases be combined into a single follow-up PR
 * (today) **RyanCavanaugh** added label `Possible Improvement`, and set milestone to `Backlog`
 * [later](https://github.com/microsoft/TypeScript/issues/65657#issuecomment-7167049728) **magurotuna** said "Thanks! I submitted #65667 with 25 more test cases that we added to tsrs."

### [PR microsoft/TypeScript#65658](https://github.com/microsoft/TypeScript/pull/65658) (Open, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Enum\.A & "a" should be Enum\.A and not never**

*Fix enum literal narrowing so an enum member with a string value remains its enum type rather than narrowing to never.*

 * created by **weswigham**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **weswigham**
 * [today](https://github.com/microsoft/TypeScript/pull/65658#issuecomment-7138267756) **weswigham** said "@typescript-bot perf test this"
 * [today](https://github.com/microsoft/TypeScript/pull/65658#issuecomment-7138271912) **typescript-automation[bot]** reported that the performance test job had started and linked to its results
 * [today](https://github.com/microsoft/TypeScript/pull/65658#issuecomment-7140292451) **typescript-automation[bot]** provided the requested performance run results comparing baseline and PR metrics
 * [today](https://github.com/microsoft/TypeScript/pull/65658#issuecomment-7140931838) **weswigham** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/65658#issuecomment-7140934420) **typescript-automation[bot]** reported the statuses and results links for the initiated test, user test, DefinitelyTyped, and performance test jobs
 * [today](https://github.com/microsoft/TypeScript/pull/65658#issuecomment-7141599697) **typescript-automation[bot]** reported new TypeScript errors in type-fest user tests when comparing the baseline and PR builds
 * [today](https://github.com/microsoft/TypeScript/pull/65658#issuecomment-7141612676) **typescript-automation[bot]** reported that the DefinitelyTyped test results were unchanged and linked the build log
 * [today](https://github.com/microsoft/TypeScript/pull/65658#issuecomment-7142120847) **typescript-automation[bot]** provided the requested performance-run results comparing the baseline and pull request
 * [today](https://github.com/microsoft/TypeScript/pull/65658#issuecomment-7142879360) **typescript-automation[bot]** reported that testing the top 400 repositories with tsc showed no differences between the baseline and PR and that everything looked good
 * [today](https://github.com/microsoft/TypeScript/pull/65658#issuecomment-7145301843) **weswigham** reported that tests passed, performance remained good, and only TypeFest was affected because its conditional types captured the checker bug and would be updated

### [PR microsoft/TypeScript#65659](https://github.com/microsoft/TypeScript/pull/65659) (Closed, `Author: Team`, `For Uncommitted Bug`, **ahejlsberg**)

**Use regular \(non\-widening\) literal types for computed property names**

*Use regular, non-widening literal types when inferring computed property names.*

 * created by **ahejlsberg**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript/pull/65659#issuecomment-7141745509) **ahejlsberg** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/65659#issuecomment-7141748327) **typescript-automation[bot]** reported that the requested test and performance jobs started and posted links to their build results
 * [today](https://github.com/microsoft/TypeScript/pull/65659#issuecomment-7142410726) **typescript-automation[bot]** reported that the user tests comparing the baseline and PR with tsc passed and everything looked good
 * [today](https://github.com/microsoft/TypeScript/pull/65659#issuecomment-7142422316) **typescript-automation[bot]** reported that the DT test results were ready and unchanged, with a link to the build log
 * [today](https://github.com/microsoft/TypeScript/pull/65659#issuecomment-7142690227) **typescript-automation[bot]** reported that the requested performance run results were available and included baseline-versus-PR comparison metrics
 * [today](https://github.com/microsoft/TypeScript/pull/65659#issuecomment-7143708751) **typescript-automation[bot]** reported that testing the top 400 repositories with `tsc` showed no differences between the baseline and PR and that everything looked good
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript#65660](https://github.com/microsoft/TypeScript/issues/65660) (Closed, `Not a Defect`)

**Checking a long \`else if\` chain over numeric literals is cubic in its length**

*TypeScript checking long else-if chains of numeric literal comparisons scales cubically, causing disproportionate compile-time increases as the chain grows.*

 * created by **javabetatester**
 * **RyanCavanaugh** added label `Not a Defect`
 * [today](https://github.com/microsoft/TypeScript/issues/65660#issuecomment-7148209030) **RyanCavanaugh** said "This is not a documented invariant, and checking arbitrarily large machine-generated state machines isn't a design goal of TypeScript."
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#65661](https://github.com/microsoft/TypeScript/issues/65661) (Closed, `Won't Fix`)

**tsc is quadratic in the number of errors on one long line**

*TypeScript 7.1 introduces quadratic error-reporting time for many diagnostics on a single long line, unlike the linear scaling in 6.0.3.*

 * created by **javabetatester**
 * **RyanCavanaugh** added label `Won't Fix`
 * [today](https://github.com/microsoft/TypeScript/issues/65661#issuecomment-7148118521) **RyanCavanaugh** dismissed the request to investigate super-linear scaling using synthetic cases with 8,000 errors
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#65662](https://github.com/microsoft/TypeScript/issues/65662) (Open, `Not a Defect`)

**Regression in 7\.1 nightly: recursive types cause TS5115 error \(infinitely circular types\)**

*A TypeScript 7.1 nightly regression incorrectly reports TS5115 for valid recursive types that compiled without errors in 7.0.2.*

 * created by **fabon-f**
 * [today](https://github.com/microsoft/TypeScript/issues/65662#issuecomment-7144729806) **ahejlsberg** said "This is a known difference and an intended error. See my comment here which includes a proposed fix for that library. "
 * **ahejlsberg** added label `Not a Defect`

### [PR microsoft/TypeScript#65663](https://github.com/microsoft/TypeScript/pull/65663) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Move release maintenance workflows to Azure Pipelines**

*Move release maintenance workflows to Azure Pipelines, including using the AzDO UI for VS Code extension version bumping.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#65664](https://github.com/microsoft/TypeScript/pull/65664) (Open, `Author: Team`, `For Uncommitted Bug`, **RyanCavanaugh**, **Copilot**)

**Cache the constraint of generic indexed access types**

*Cache constraints for generic indexed access types to avoid repeated union reconstruction and significantly improve type-checking performance.*

 * created by **RyanCavanaugh**
 * (today) **RyanCavanaugh** assigned to **Copilot**, **RyanCavanaugh**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Milestone Bug`, `For Milestone Bug`, `For Uncommitted Bug`, and removed label `For Milestone Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/65664#issuecomment-7153540474) **RyanCavanaugh** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/65664#issuecomment-7153542296) **typescript-automation[bot]** reported that the requested test and build jobs had started, with completed results linked for most jobs and performance results still pending
 * [today](https://github.com/microsoft/TypeScript/pull/65664#issuecomment-7154037988) **typescript-automation[bot]** reported that the DT test results were ready and unchanged, and linked the build log
 * [today](https://github.com/microsoft/TypeScript/pull/65664#issuecomment-7154054608) **typescript-automation[bot]** reported that user tests comparing the baseline and PR with tsc passed without issues
 * [today](https://github.com/microsoft/TypeScript/pull/65664#issuecomment-7154226220) **typescript-automation[bot]** reported the requested performance-run results, including baseline-versus-PR compiler metrics
 * [today](https://github.com/microsoft/TypeScript/pull/65664#issuecomment-7154969544) **typescript-automation[bot]** reported that testing the top 400 repositories with tsc showed no differences between the baseline and PR, with everything looking good

### [PR microsoft/TypeScript#65665](https://github.com/microsoft/TypeScript/pull/65665) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Fix more LS escaping related bugs**

*Fix additional escaping-related bugs in LS across areas not covered by the previous pull request.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#65666](https://github.com/microsoft/TypeScript/pull/65666) (Open, `For Uncommitted Bug`)

**Distinguish between non\-distributed and distributed type parameters in mapped types too**

*Fix mapped types to distinguish distributed and non-distributed type parameters, preventing invalid inferred instantiations that violate parameter constraints.*

 * created by **Andarist**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/65666#issuecomment-7161306610) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."

### [PR microsoft/TypeScript#65667](https://github.com/microsoft/TypeScript/pull/65667) (Open, `For Backlog Bug`)

**Add tests for path edge cases in resolution, emit, and builds**

*Add comprehensive compiler and Go tests covering path edge cases in resolution, declaration emit, source maps, configuration, and builds.*

 * created by **magurotuna**
 * **typescript-automation[bot]** added label `For Backlog Bug`

