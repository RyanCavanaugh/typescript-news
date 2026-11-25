# Report for 2026-11-23 (Monday, November 23rd, 2026)

18 different users commented on 49 different issues.

## Recommended Actions

 * Response Recommended
    * @scenerecap provided reproduction steps and evidence for the reported TypeScript narrowing issue in [microsoft/TypeScript#26914](https://github.com/microsoft/TypeScript/issues/26914#issuecomment-7110223255)
    * @sanbei101 asked about the release readiness and timeline in [microsoft/TypeScript#63703](https://github.com/microsoft/TypeScript/issues/63703#issuecomment-7131617043)
    * @mrginglymus provided a similar reproduction and additional context about the affected dependency setup in [microsoft/TypeScript#65601](https://github.com/microsoft/TypeScript/issues/65601#issuecomment-7114336876)
    * @MartinFerret asked whether updating `@opentelemetry/api` to declare `stack?: string | undefined` would be acceptable in [microsoft/TypeScript#65636](https://github.com/microsoft/TypeScript/pull/65636#issuecomment-7110746429)

## Activity Summary

### [Issue microsoft/TypeScript#26914](https://github.com/microsoft/TypeScript/issues/26914) (Open, `Bug`, `Domain: check: Control Flow`)

**Control flow analysis should "work" in unreachable code**

*TypeScript should perform control-flow narrowing in unreachable code instead of reporting impossible errors after an unconditional return.*

 * [1.8 years ago](https://github.com/microsoft/TypeScript/issues/26914#issuecomment-2613114032) **RyanCavanaugh** explained why unreachable code should still be analyzed and recommended using an unrecognized control-flow construct for debugging
 * **RyanCavanaugh** added label `Domain: Control Flow`
 * [yesterday](https://github.com/microsoft/TypeScript/issues/26914#issuecomment-7080495698) **Plecra** outlined a proposition-based control-flow and reachability analysis model for TypeScript type checking, including how unreachable code could be represented
 * [today](https://github.com/microsoft/TypeScript/issues/26914#issuecomment-7110223255) **scenerecap** reported reproducing a TypeScript narrowing issue in an unreachable block after an early return, including a Playground example and recording link

### [Issue microsoft/TypeScript#63427](https://github.com/microsoft/TypeScript/issues/63427) (Open, `Bug`, `Domain: lib.d.ts`)

**Add type definition for Math\.sumPrecise \(ES2025 / TC39 proposal\)**

*Add TypeScript definitions for the ES2026 Math.sumPrecise API to support precise iterable summation without compilation errors.*

 * (9 weeks ago) **RyanCavanaugh** added label `Needs Human Review`, and removed labels `Needs Human Review`, `Help Wanted`
 * [later](https://github.com/microsoft/TypeScript/issues/63427#issuecomment-7136465460) **petamoriken** said "Looks like Math.sumPrecise is already added: https://github.com/microsoft/TypeScript/pull/64096"

### [Issue microsoft/TypeScript#63703](https://github.com/microsoft/TypeScript/issues/63703) (Open, `Planning`)

**TypeScript 7\.1 Iteration Plan**

*The TypeScript 7.1 iteration plan outlines release milestones and planned compiler, editor, library, API, and performance improvements.*

 * [6 days ago](https://github.com/microsoft/TypeScript/issues/63703#issuecomment-6949297487) **sosoba** asked whether the 7.1 RC and stable release plan would be updated
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63703#issuecomment-7047585063) **heXaCo0l** said "@DanielRosenwasser any update on the plan ? "
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63703#issuecomment-7061436783) **remcohaszing** mentioned that a release candidate was reportedly planned for December 1 and a stable release for the second week of December, while noting the information was unconfirmed
 * [later](https://github.com/microsoft/TypeScript/issues/63703#issuecomment-7131617043) **sanbei101** said "Is it almost ready to be released?"

### [Issue microsoft/TypeScript#63979](https://github.com/microsoft/TypeScript/issues/63979) (Closed, `Out of Scope`, `Docs`)

**Official guidelines to build complex types**

*Request official guidelines documenting supported patterns, techniques, and pitfalls for building complex TypeScript type definitions.*

 * [11 weeks ago](https://github.com/microsoft/TypeScript/issues/63979#issuecomment-5566337634) **denis-migdal** suggested documenting TypeScript design practices, including avoiding concrete types as interfaces, defining capacity interfaces, and using symbols for internal data
 * [1 month ago](https://github.com/microsoft/TypeScript/issues/63979#issuecomment-6382208348) **denis-migdal** shared additional TypeScript tips and tricks covering type assertions, safer casting alternatives, friend functions, internal static hooks, and parameter bags, while noting potential inference issues
 * [1 month ago](https://github.com/microsoft/TypeScript/issues/63979#issuecomment-6396284363) **denis-migdal** explained that types and values can share a name for classes or factories, but both must be exported together when the type is defined in another file
 * [today](https://github.com/microsoft/TypeScript/issues/63979#issuecomment-7123928333) **denis-migdal** shared TypeScript guidance on type inferability, assignability, generic inference, type/value distinctions, and assertion guards, while inviting further contributions and noting plans to clean it up later

### [PR microsoft/TypeScript#64257](https://github.com/microsoft/TypeScript/pull/64257) (Open, `For Backlog Bug`)

**Fix non\-null discriminant narrowing consistency**

*Fix discriminant equality narrowing so small and large nullable unions consistently preserve null, undefined, and void constituents.*

 * [10 weeks ago](https://github.com/microsoft/TypeScript/pull/64257#issuecomment-5662956364) **z0rimo** explained that the fix for #62511 also addressed the evaluation-order soundness issue in #64260, reworked mutation analysis around invocation sites, and added tests for union-size inconsistencies and stale facts
 * [8 weeks ago](https://github.com/microsoft/TypeScript/pull/64257#issuecomment-5883585069) **z0rimo** mentioned reworking the fix to use general narrowing for nullable unions in equality and switch cases, and requested another review
 * [3 weeks ago](https://github.com/microsoft/TypeScript/pull/64257#issuecomment-6458080251) **z0rimo** asked @RyanCavanaugh to review the revised implementation and confirm whether the approach was acceptable
 * [today](https://github.com/microsoft/TypeScript/pull/64257#issuecomment-7109435783) **jakebailey** recommended force-pushing a cleaner commit history with separate test/baseline and fix commits
 * [today](https://github.com/microsoft/TypeScript/pull/64257#issuecomment-7124131251) **z0rimo** reworked the PR history into two commits: one adding the regression test with failing baselines and another containing the fix with updated baselines

### [PR microsoft/TypeScript#64376](https://github.com/microsoft/TypeScript/pull/64376) (Closed, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Negated Types: Change the meaning of \`{}\` to \`unknown & not null & not undefined\`**

*Change `{}` semantics to exclude null and undefined, while replacing literal-union normalization exceptions with enhanced type-origin tracking.*

 * [5 weeks ago](https://github.com/microsoft/TypeScript/pull/64376#issuecomment-6272167221) **typescript-automation[bot]** reported that the automated test jobs had started, with `run dt` failing and `perf test this faster` awaiting review while other results were pending
 * [5 weeks ago](https://github.com/microsoft/TypeScript/pull/64376#issuecomment-6272738846) **typescript-automation[bot]** provided the requested performance run results, showing largely unchanged errors and memory usage with small increases in symbols and types
 * [5 weeks ago](https://github.com/microsoft/TypeScript/pull/64376#issuecomment-6278060293) **typescript-automation[bot]** reported that the DT test run failed and provided a link to the build log
 * [today](https://github.com/microsoft/TypeScript/pull/64376#issuecomment-7116832811) **weswigham** said "@typescript-bot test this"
 * [today](https://github.com/microsoft/TypeScript/pull/64376#issuecomment-7116834657) **typescript-automation[bot]** reported that the requested jobs had started, with failures recorded for `run dt` and `perf test this faster`
 * [today](https://github.com/microsoft/TypeScript/pull/64376#issuecomment-7122046439) **typescript-automation[bot]** reported that the DT test run had failed and linked to the build log
 * [later](https://github.com/microsoft/TypeScript/pull/64376#issuecomment-7133481365) **typescript-automation[bot]** said "@weswigham, the perf run you requested failed. You can check the log here."

### [Issue microsoft/TypeScript#64453](https://github.com/microsoft/TypeScript/issues/64453) (Closed, `Needs Investigation`, **weswigham**)

**\`EFNoLeadingComments\` suppresses synthesized leading comments in tsgo; Strada only suppresses source comments**

*tsgo incorrectly suppresses synthesized leading comments with EFNoLeadingComments, unlike Strada, which suppresses only source comments.*

 * [8 weeks ago](https://github.com/microsoft/TypeScript/issues/64453#issuecomment-5862919851) **z0rimo** reported that tsgo incorrectly suppressed synthesized comments under EFNoLeadingComments and EFNoTrailingComments, compared with Strada; opened draft PR #64488 with a compatibility fix and regression tests
 * (7 weeks ago) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **weswigham**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#64488](https://github.com/microsoft/TypeScript/pull/64488) (Closed, `For Uncommitted Bug`, **weswigham**)

**Fix synthesized comment emission with comment flags**

*Restore synthesized comment emission while comment flags suppress source comments, preserving formatting and semantics across synchronous and asynchronous printer APIs.*

 * created by **z0rimo**
 * (8 weeks ago) **typescript-automation[bot]** added label `For Uncommitted Bug`, and assigned to **weswigham**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#65034](https://github.com/microsoft/TypeScript/pull/65034) (Closed, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Negated Types: Make conditional type produce substitutions with negated constraints in \(some\) false branches **

*Enable conditional types to infer negated constraints in false branches when primitive union constraints can be safely partitioned.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript/pull/65034#issuecomment-6508963229) **typescript-automation[bot]** reported changed user-test results between the baseline and PR, including new and missing TypeScript errors, and asked the maintainer to investigate
 * [3 weeks ago](https://github.com/microsoft/TypeScript/pull/65034#issuecomment-6509138446) **typescript-automation[bot]** provided the requested performance run results, including compiler comparison metrics
 * [3 weeks ago](https://github.com/microsoft/TypeScript/pull/65034#issuecomment-6510105307) **typescript-automation[bot]** reported changed TypeScript compiler results from testing the top 400 repositories and asked the maintainer to investigate new TS2367 errors in OmniRoute
 * [today](https://github.com/microsoft/TypeScript/pull/65034#issuecomment-7115160807) **weswigham** said "@typescript-bot test this"
 * [today](https://github.com/microsoft/TypeScript/pull/65034#issuecomment-7115163368) **typescript-automation[bot]** reported that automated test jobs started and linked to their build results, including a failed performance test result
 * [today](https://github.com/microsoft/TypeScript/pull/65034#issuecomment-7116616068) **typescript-automation[bot]** reported that the DT tests produced a new branch-only TS1110 error in the regex-not package’s test file and linked the full build log
 * [today](https://github.com/microsoft/TypeScript/pull/65034#issuecomment-7116643264) **typescript-automation[bot]** reported new TS2367 errors in the Effect user-test results when comparing the baseline and PR, and asked the maintainer to investigate
 * [today](https://github.com/microsoft/TypeScript/pull/65034#issuecomment-7117846521) **typescript-automation[bot]** reported results from comparing the baseline and PR TypeScript compiler runs across the top 400 repositories and flagged unexpected changes for review
 * [later](https://github.com/microsoft/TypeScript/pull/65034#issuecomment-7125759541) **typescript-automation[bot]** said "@weswigham, the perf run you requested failed. You can check the log here."

### [PR microsoft/TypeScript#65064](https://github.com/microsoft/TypeScript/pull/65064) (Open, `Author: Team`, `For Milestone Bug`, `For Backlog Bug`, **jakebailey**)

**\[experiment\] fully order independent type checking**

*Overhauls type checking to produce consistent behavior regardless of traversal, file, cache, or cycle-processing order, with extensive randomized ordering tests.*

 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-7096397631) **typescript-automation[bot]** reported changed user-test results for the `uglify-js` project, including a new TS2339 error and a missing TS2322 error in `compress.js`
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-7096678371) **typescript-automation[bot]** provided the requested performance results, showing increased symbols and memory usage in the Compiler-Unions native benchmark
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-7099241405) **typescript-automation[bot]** reported results from comparing the baseline and PR across the top 1,000 repositories, highlighting new TypeScript build errors in PeerTube and Unleash and asking for investigation
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-7114788229) **jakebailey** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-7114791195) **typescript-automation[bot]** reported the start and linked results of several automated test jobs
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-7115756159) **typescript-automation[bot]** reported that the DT tests produced a branch-only TypeScript overload error in the d3-selection package at d3-selection-tests.ts:1502
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-7116213900) **typescript-automation[bot]** reported changed user-test results for the `uglify-js` project, including a new TS2339 error and a missing TS2322 error in `compress.js`
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-7117256680) **typescript-automation[bot]** reported that testing the top 400 repositories with tsc showed no differences between the baseline and PR, with everything looking good
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-7125492379) **typescript-automation[bot]** reported the requested performance results, including increased symbols and memory usage in the Compiler-Unions native benchmark

### [PR microsoft/TypeScript#65286](https://github.com/microsoft/TypeScript/pull/65286) (Closed, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Negated Types: Remove the concept of control\-flow made "fresh" negations**

*Enable full negated types in control-flow analysis instead of transient fresh negations, while addressing impacts on exact matching and performance.*

 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [5 days ago](https://github.com/microsoft/TypeScript/pull/65286#issuecomment-6991687631) **weswigham** said "@typescript-bot test this"
 * [5 days ago](https://github.com/microsoft/TypeScript/pull/65286#issuecomment-6991689459) **typescript-automation[bot]** said "Hey @weswigham, this PR is in an unmergable state, so is missing a merge commit to run against; please resolve conflicts and try again."
 * [today](https://github.com/microsoft/TypeScript/pull/65286#issuecomment-7114411811) **weswigham** said "@typescript-bot test this"
 * [today](https://github.com/microsoft/TypeScript/pull/65286#issuecomment-7114414269) **typescript-automation[bot]** reported that the requested test and performance jobs had started, with the performance test producing failed results
 * [today](https://github.com/microsoft/TypeScript/pull/65286#issuecomment-7115070969) **typescript-automation[bot]** reported DefinitelyTyped test results showing branch-only errors in the regex-not and pdfmake packages
 * [today](https://github.com/microsoft/TypeScript/pull/65286#issuecomment-7115078106) **typescript-automation[bot]** reported new TS2367 errors in Effect user-test comparisons and asked @weswigham to investigate
 * [today](https://github.com/microsoft/TypeScript/pull/65286#issuecomment-7116180580) **typescript-automation[bot]** said "@weswigham, the perf run you requested failed. You can check the log here."
 * [today](https://github.com/microsoft/TypeScript/pull/65286#issuecomment-7116324846) **typescript-automation[bot]** reported results from comparing baseline and PR TypeScript runs across the top 400 repositories, highlighting unexpected changes and build failures for maintainer review
 * [today](https://github.com/microsoft/TypeScript/pull/65286#issuecomment-7116325770) **typescript-automation[bot]** reported additional changes from the top 400 repositories suite, including build failures and TypeScript property errors in kortix-ai/CompanyOS
 * [today](https://github.com/microsoft/TypeScript/pull/65286#issuecomment-7116326801) **typescript-automation[bot]** provided additional top-400 repository suite results, including VS Code projects that failed to build with the old TypeScript compiler and detailed diagnostics
 * [today](https://github.com/microsoft/TypeScript/pull/65286#issuecomment-7116327797) **typescript-automation[bot]** reported additional top-400-repository suite results, including build failures and TypeScript errors in Supabase projects

### [PR microsoft/TypeScript#65296](https://github.com/microsoft/TypeScript/pull/65296) (Closed, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Negated Types: Consider assertions invertible and create negated narrowings in false branches of assertion narrowings**

*Consider whether assertion narrowings should produce negated types in false branches, despite unsoundness when guards are less specific than their checks.*

 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [5 days ago](https://github.com/microsoft/TypeScript/pull/65296#issuecomment-6991685752) **weswigham** said "@typescript-bot test this"
 * [5 days ago](https://github.com/microsoft/TypeScript/pull/65296#issuecomment-6991687540) **typescript-automation[bot]** said "Hey @weswigham, this PR is in an unmergable state, so is missing a merge commit to run against; please resolve conflicts and try again."
 * [today](https://github.com/microsoft/TypeScript/pull/65296#issuecomment-7113004833) **weswigham** said "@typescript-bot test this"
 * [today](https://github.com/microsoft/TypeScript/pull/65296#issuecomment-7113007735) **typescript-automation[bot]** reported that the requested test, DT, and performance jobs had started, with results linked where available
 * [today](https://github.com/microsoft/TypeScript/pull/65296#issuecomment-7113955054) **typescript-automation[bot]** reported that the DefinitelyTyped test run completed and identified branch-only errors in jquery/v3 and regex-not, including three type expectation mismatches in jquery/v3
 * [today](https://github.com/microsoft/TypeScript/pull/65296#issuecomment-7114003930) **typescript-automation[bot]** reported new TypeScript errors found when comparing baseline and PR user-test results and asked the maintainer to review them
 * [today](https://github.com/microsoft/TypeScript/pull/65296#issuecomment-7114192319) **typescript-automation[bot]** said "@weswigham, the perf run you requested failed. You can check the log here."

### [PR microsoft/TypeScript#65298](https://github.com/microsoft/TypeScript/pull/65298) (Closed, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Negated Types: Remove the \`TypeFacts\` abstraction and make type refinements directly**

*Refactor negated types to remove the TypeFacts abstraction and implement type refinements directly, while evaluating performance implications.*

 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [5 days ago](https://github.com/microsoft/TypeScript/pull/65298#issuecomment-6991690889) **weswigham** said "@typescript-bot test this"
 * [5 days ago](https://github.com/microsoft/TypeScript/pull/65298#issuecomment-6991692786) **typescript-automation[bot]** said "Hey @weswigham, this PR is in an unmergable state, so is missing a merge commit to run against; please resolve conflicts and try again."
 * [today](https://github.com/microsoft/TypeScript/pull/65298#issuecomment-7112770913) **weswigham** said "@typescript-bot test this"
 * [today](https://github.com/microsoft/TypeScript/pull/65298#issuecomment-7112773789) **typescript-automation[bot]** reported that the requested TypeScript test and performance jobs had started and linked to their build and result pages
 * [today](https://github.com/microsoft/TypeScript/pull/65298#issuecomment-7113445178) **typescript-automation[bot]** reported branch-only DT test errors in the assert and jsonwebtoken packages, including unexpected inferred types
 * [today](https://github.com/microsoft/TypeScript/pull/65298#issuecomment-7113492818) **typescript-automation[bot]** reported new TS2322 type errors in compilerRegistry.ts across multiple Effect project configurations and asked the maintainer to investigate the change
 * [today](https://github.com/microsoft/TypeScript/pull/65298#issuecomment-7113743309) **typescript-automation[bot]** reported the requested TypeScript compiler performance results, including baseline-to-PR metric comparisons
 * [today](https://github.com/microsoft/TypeScript/pull/65298#issuecomment-7114838169) **typescript-automation[bot]** reported TypeScript comparison results from running the top 400 repositories and flagged unexpected build changes for maintainer review
 * [today](https://github.com/microsoft/TypeScript/pull/65298#issuecomment-7114839298) **typescript-automation[bot]** reported additional top-400-repository suite results, including PixiJS build failures and TypeScript errors observed with the old compiler
 * [today](https://github.com/microsoft/TypeScript/pull/65298#issuecomment-7114840452) **typescript-automation[bot]** reported additional TypeScript changes and build errors found while running the top 400 repositories suite
 * [today](https://github.com/microsoft/TypeScript/pull/65298#issuecomment-7114841583) **typescript-automation[bot]** reported additional changes from the top 400 repositories suite, including build failures and a TS2367 diagnostic in teableio/teable

### [PR microsoft/TypeScript#65586](https://github.com/microsoft/TypeScript/pull/65586) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**\[api\] AST utility APIs**

*Add AST utility APIs for decorator and modifier checks, ancestor lookup, node flags, formatting settings, rest parameters, and keyword identification.*

 * (4 days ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#65591](https://github.com/microsoft/TypeScript/pull/65591) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**\[api\] Resolution utility APIs**

*Add resolution utility APIs for determining effective type roots, locating TypeScript build-info output files, and resolving type reference directives.*

 * (4 days ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#65599](https://github.com/microsoft/TypeScript/pull/65599) (Closed, `Author: Team`, `For Uncommitted Bug`)

**Update localization files**

*Update localization handbacks and regenerate their corresponding runtime artifacts.*

 * created by **typescript-automation[bot]**
 * (4 days ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#65601](https://github.com/microsoft/TypeScript/issues/65601) (Open)

**7\.1: same package is installed twice in two connected project, TS sees only one \(get TS2883\)**

*TypeScript 7.1 incorrectly reports TS2883 when identical packages are installed in two connected projects and infers a non-portable declaration reference.*

 * created by **elevatebart**
 * [today](https://github.com/microsoft/TypeScript/issues/65601#issuecomment-7114336876) **mrginglymus** said "I have a similar reproduction here https://github.com/mrginglymus/ts2883-regression (thanks to my toaster) - this time found because of a peer dependency on storybook, using yarn's pnpm linker."

### [PR microsoft/TypeScript#65613](https://github.com/microsoft/TypeScript/pull/65613) (Closed, `Author: Team`, `For Milestone Bug`, **andrewbranch**)

**Content mapper diagnostic code selectors**

*Adds diagnostic code selectors to the content mapper, incorporating review feedback from the preceding pull request.*

 * (3 days ago) **typescript-automation[bot]** added labels `Author: Team`, `For Milestone Bug`, and assigned to **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript#65616](https://github.com/microsoft/TypeScript/issues/65616) (Open, `Domain: check: Order Dependence`)

**\`\-\-incremental\`: unused import not reported after an edit when it appears only in an export's inferred type**

*Incremental TypeScript builds fail to report unused imports referenced only in an export’s inferred type after source edits.*

 * created by **bjornpagen**
 * **jakebailey** added label `Domain: check: Order Dependence`

### [PR microsoft/TypeScript#65618](https://github.com/microsoft/TypeScript/pull/65618) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Update deps**

*Update dependencies to accommodate new dprint formatting and resolve an audit finding.*

 * (3 days ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#65619](https://github.com/microsoft/TypeScript/pull/65619) (Open, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Build set instead of binary searching for denormalized origins**

*Optimize denormalized union origin construction by using a type set for membership checks instead of repeated binary searches.*

 * [3 days ago](https://github.com/microsoft/TypeScript/pull/65619#issuecomment-7057734601) **jakebailey** said "@typescript-bot perf test this faster"
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/65619#issuecomment-7057735682) **typescript-automation[bot]** reported that the performance test job started and linked to its build results
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/65619#issuecomment-7058201437) **typescript-automation[bot]** reported the requested performance-run results, including compiler benchmark comparisons between the baseline and pull request
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#65621](https://github.com/microsoft/TypeScript/pull/65621) (Open, `Author: Team`, `For Backlog Bug`, **ahejlsberg**, **jakebailey**)

**Order types, symbols, and nodes by content instead of by ID**

*Order types, symbols, and nodes deterministically by content rather than creation IDs, interning identical types and eliminating ID-dependent output.*

 * [today](https://github.com/microsoft/TypeScript/pull/65621#issuecomment-7096142787) **typescript-automation[bot]** reported that user tests comparing the baseline and PR with tsc passed successfully
 * [today](https://github.com/microsoft/TypeScript/pull/65621#issuecomment-7096316261) **typescript-automation[bot]** reported the requested performance-run results comparing the baseline and pull request, including compiler metrics and memory changes
 * [today](https://github.com/microsoft/TypeScript/pull/65621#issuecomment-7099218572) **typescript-automation[bot]** reported that the top 1,000 repositories showed no differences between the baseline and PR when run with tsc
 * [today](https://github.com/microsoft/TypeScript/pull/65621#issuecomment-7114787709) **jakebailey** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/65621#issuecomment-7114790138) **typescript-automation[bot]** reported the status and results of automated test jobs
 * [today](https://github.com/microsoft/TypeScript/pull/65621#issuecomment-7115551516) **typescript-automation[bot]** reported that the DT test results were ready and unchanged, with a link to the build log
 * [today](https://github.com/microsoft/TypeScript/pull/65621#issuecomment-7115814604) **typescript-automation[bot]** reported that user tests comparing the baseline and PR with tsc passed successfully
 * [today](https://github.com/microsoft/TypeScript/pull/65621#issuecomment-7117060584) **typescript-automation[bot]** reported that testing the top 400 repositories with tsc showed no differences between the baseline and PR, with everything looking good
 * [today](https://github.com/microsoft/TypeScript/pull/65621#issuecomment-7125296192) **typescript-automation[bot]** reported that the requested performance run results were available and included baseline-to-PR compiler comparison metrics

### [PR microsoft/TypeScript#65629](https://github.com/microsoft/TypeScript/pull/65629) (Open, `For Backlog Bug`)

**Fix JSDoc type predicate inference for arrow functions**

*Fix JSDoc type predicate inference for JavaScript arrow functions and expressions by resolving enclosing @type annotations and return signatures.*

 * created by **1abdala**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [yesterday](https://github.com/microsoft/TypeScript/pull/65629#issuecomment-7076473112) **1abdala** reproduced the Contributor License Agreement request and signing instructions
 * [today](https://github.com/microsoft/TypeScript/pull/65629#issuecomment-7109593562) **jakebailey** suggested splitting the changes into separate test and fix commits and renaming the test to something more readable
 * [today](https://github.com/microsoft/TypeScript/pull/65629#issuecomment-7118180688) **1abdala** acknowledged the feedback and agreed to split the commits and rename the test for readability

### [PR microsoft/TypeScript#65630](https://github.com/microsoft/TypeScript/pull/65630) (Open, `For Uncommitted Bug`)

**Fix nested destructured require bindings in declaration emit**

*Declaration emit incorrectly handles nested destructured CommonJS require bindings, requiring corrected transformation logic and regression tests.*

 * created by **mohdshamii**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [yesterday](https://github.com/microsoft/TypeScript/pull/65630#issuecomment-7076753068) **mohdshamii** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript/pull/65630#issuecomment-7109576159) **jakebailey** suggested splitting the changes into separate commits for the failing test and baseline, followed by the fix and updated baseline

### [PR microsoft/TypeScript#65636](https://github.com/microsoft/TypeScript/pull/65636) (Open, `For Backlog Bug`)

**Allow undefined in Error\.stack under exactOptionalPropertyTypes**

*Update Error.stack’s declaration to explicitly allow undefined under exactOptionalPropertyTypes, while documenting compatibility trade-offs and testing broader impact.*

 * created by **MartinFerret**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/65636#issuecomment-7109353106) **jakebailey** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/65636#issuecomment-7109355797) **typescript-automation[bot]** reported the status and results of automated test jobs, including failures for `run dt` and `perf test this faster`
 * [today](https://github.com/microsoft/TypeScript/pull/65636#issuecomment-7110103166) **typescript-automation[bot]** reported that the DT test run failed and provided a link to the build log
 * [today](https://github.com/microsoft/TypeScript/pull/65636#issuecomment-7110135771) **typescript-automation[bot]** reported a new TS2345 error in the Effect project when comparing baseline and PR user-test results, and asked the maintainer to investigate
 * [today](https://github.com/microsoft/TypeScript/pull/65636#issuecomment-7110507278) **typescript-automation[bot]** said "@jakebailey, the perf run you requested failed. You can check the log here."
 * [today](https://github.com/microsoft/TypeScript/pull/65636#issuecomment-7110746429) **MartinFerret** reported a new user-test error in Effect's OtelTracer involving an Error passed to OpenTelemetry's Exception type and suggested allowing `stack?: string | undefined` in `@opentelemetry/api`
 * [today](https://github.com/microsoft/TypeScript/pull/65636#issuecomment-7110876478) **jakebailey** said "@typescript-bot run dt"
 * [today](https://github.com/microsoft/TypeScript/pull/65636#issuecomment-7110879294) **typescript-automation[bot]** reported that the `run dt` job started and completed successfully, linking to its build and results
 * [today](https://github.com/microsoft/TypeScript/pull/65636#issuecomment-7111536670) **typescript-automation[bot]** reported that the DT test results were ready and unchanged, and linked the build log

### [PR microsoft/TypeScript#65639](https://github.com/microsoft/TypeScript/pull/65639) (Open, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Skip unrelated literal\-keyed constituents when narrowing**

*Optimize union narrowing by skipping unrelated literal-keyed constituents, preventing excessive structural checks and complexity errors with large literal unions.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/65639#issuecomment-7108354091) **jakebailey** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/65639#issuecomment-7108357049) **typescript-automation[bot]** reported that the requested test and performance jobs had started and linked their build results
 * [today](https://github.com/microsoft/TypeScript/pull/65639#issuecomment-7109054476) **typescript-automation[bot]** reported that the DT test results were ready and unchanged, and shared a link to the log
 * [today](https://github.com/microsoft/TypeScript/pull/65639#issuecomment-7109160509) **typescript-automation[bot]** reported that user tests comparing the baseline and PR with tsc passed successfully
 * [today](https://github.com/microsoft/TypeScript/pull/65639#issuecomment-7109386831) **typescript-automation[bot]** provided the requested performance run results comparing the baseline and PR
 * [today](https://github.com/microsoft/TypeScript/pull/65639#issuecomment-7109560504) **jakebailey** said "Disappointingly not a perf win, but, oh well"
 * [today](https://github.com/microsoft/TypeScript/pull/65639#issuecomment-7110492448) **typescript-automation[bot]** reported that testing the top 400 repositories with tsc showed no differences between the baseline and PR, with everything looking good
 * **jakebailey** added label `Domain: Performance`

### [Issue microsoft/TypeScript#65640](https://github.com/microsoft/TypeScript/issues/65640) (Open)

**Downlevel \`super\` in static initializers loses \`this\` or emits an invalid assignment when the reference is parenthesized or has \`\!\`, \`as\` or \`satisfies\`**

*Downleveling parenthesized or type-asserted `super` references in static initializers loses method `this` binding and emits invalid assignments below ES2022.*

 * created by **ktfth**

### [Issue microsoft/TypeScript#65641](https://github.com/microsoft/TypeScript/issues/65641) (Open)

**Downlevel async methods lose \`this\` for \`super\.m\` tagged templates and for wrapped \`super\.m\(\)\` calls, and turn wrapped \`super\.x = v\` into a getter\-only write**

*Downleveling async methods mishandles wrapped or tagged super calls and assignments, losing the receiver and converting setter writes into getter-only errors.*

 * created by **ktfth**

### [Issue microsoft/TypeScript#65642](https://github.com/microsoft/TypeScript/issues/65642) (Open)

**Downlevel \`\#private\` destructuring targets and \`\+\+\`/\`\-\-\` operands emit invalid JS when wrapped in parentheses, \`\!\`, \`as\` or \`satisfies\`**

*Downleveling private-field destructuring assignments and update expressions wrapped in syntax constructs emits invalid JavaScript for ES2021 and earlier targets.*

 * created by **ktfth**

### [Issue microsoft/TypeScript#65643](https://github.com/microsoft/TypeScript/issues/65643) (Open)

**Downlevel class fields break \`\.name\`: anonymous classes with \`\#private\` members are named after the temp \(\`\_a\`\), and functions in field initializers get \`""\` or \`"value"\`**

*Downleveling anonymous classes with private fields and functions in class field initializers produces incorrect `.name` values instead of preserving ES2022 naming.*

 * created by **ktfth**

### [Issue microsoft/TypeScript#65644](https://github.com/microsoft/TypeScript/issues/65644) (Open)

**Missing diagnostic for element access after an instantiation expression across a line break**

*TypeScript fails to diagnose element access after a newline-separated, unparenthesized instantiation expression, potentially changing optional-chain evaluation semantics.*

 * created by **magic-akari**

### [PR microsoft/TypeScript#65645](https://github.com/microsoft/TypeScript/pull/65645) (Open, `For Uncommitted Bug`)

**Report element access after an instantiation expression**

*Report TS1477 for non-optional element access after an unparenthesized instantiation expression across a line break.*

 * created by **magic-akari**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [PR microsoft/TypeScript#65646](https://github.com/microsoft/TypeScript/pull/65646) (Open, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**Normalize URI\-valued DocumentIdentifier inputs**

*Normalize and validate URI-valued DocumentIdentifier inputs by delegating JSON unmarshalling to lsproto.DocumentUri.*

 * created by **andrewbranch**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **andrewbranch**

### [PR microsoft/TypeScript#65647](https://github.com/microsoft/TypeScript/pull/65647) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**Allow getSymbol on any Node, overload for Declaration**

*Update `getSymbol` to accept any `Node` while preserving definite results for `Declaration`, and narrow `isExternalModule` accordingly.*

 * created by **andrewbranch**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **andrewbranch**

### [PR microsoft/TypeScript#65648](https://github.com/microsoft/TypeScript/pull/65648) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**Enable ESLint on packages/typescript**

*Enable ESLint for packages/typescript by adopting Strada’s configuration and resolving existing violations using the experimental TypeScript 7 backend.*

 * created by **andrewbranch**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **andrewbranch**

### [PR microsoft/TypeScript#65649](https://github.com/microsoft/TypeScript/pull/65649) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**Preserve text ranges on updated and cloned API nodes**

*Preserve source text ranges when updating or cloning AST nodes to retain shebangs and comments, while supporting suppression of outer clone comments.*

 * created by **andrewbranch**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **andrewbranch**

### [PR microsoft/TypeScript#65650](https://github.com/microsoft/TypeScript/pull/65650) (Open, `For Backlog Bug`)

**Coalesce concurrent async source file requests**

*Coalesce concurrent async source-file requests by canonical path, while clearing failed in-flight entries to allow retries.*

 * created by **emerardd**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/65650#issuecomment-7120886375) **emerardd** said "@microsoft-github-policy-service agree"

### [Issue microsoft/TypeScript#65651](https://github.com/microsoft/TypeScript/issues/65651) (Open)

**tsc panics when a content mapper reports an option diagnostic for a \`contentMappers\` entry inherited through \`extends\`**

*TypeScript’s compiler crashes when a content mapper reports an invalid option for a contentMappers entry inherited through extends.*

 * created by **benpsnyder**

### [PR microsoft/TypeScript#65652](https://github.com/microsoft/TypeScript/pull/65652) (Open, `For Uncommitted Bug`)

**Fix crash locating a content mapper option diagnostic inherited through extends**

*Fix crashes when locating content mapper option diagnostics inherited through extends by tracking and using the declaring configuration file.*

 * created by **benpsnyder**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/65652#issuecomment-7122130993) **benpsnyder** said "@microsoft-github-policy-service agree"

### [Issue microsoft/TypeScript#65653](https://github.com/microsoft/TypeScript/issues/65653) (Open)

**API build orchestrator cannot start a content mapper**

*The API build orchestrator cannot launch configured content mappers with external code enabled, preventing incremental checking for custom file extensions.*

 * created by **baseballyama**

### [Issue microsoft/TypeScript#65654](https://github.com/microsoft/TypeScript/issues/65654) (Open, `Bug`, **RyanCavanaugh**, **Copilot**)

**Checking a generic indexed access against a large union of literal aliases takes 16 s on 7\.0\.2 \(5\.9 s on 5\.9\.3\)**

*TypeScript 7.0.2 significantly slows type-checking a generic indexed access against large unions of literal aliases compared with 5.9.3.*

 * created by **AlexandreDemartin**

### [Issue microsoft/TypeScript#65655](https://github.com/microsoft/TypeScript/issues/65655) (Open)

**Regression from 6\.0: downlevel async methods throw for \`for \(super\.x of \.\.\.\)\` and \`for \(super\.x in \.\.\.\)\` because \`\_super\` only gets a getter**

*Downleveling async methods targeting ES2015/ES2016 fails for `for (super.x of/in ...)` because the generated `_super` proxy lacks a setter.*

 * created by **ktfth**

