# Report for 2026-10-10 (Saturday, October 10th, 2026)

15 different users commented on 21 different issues.

## Recommended Actions

 * Response Recommended
    * @alshdavid suggested adding support for remote declaration files in TypeScript's language server in [microsoft/TypeScript#28985](https://github.com/microsoft/TypeScript/issues/28985#issuecomment-6105953953)
    * @Ankith-B asked if the proposed approach is acceptable before opening a PR in [microsoft/TypeScript#33866](https://github.com/microsoft/TypeScript/issues/33866#issuecomment-6110643262)
    * @mahesh-desu asked to be assigned to the issue in [microsoft/TypeScript#57640](https://github.com/microsoft/TypeScript/issues/57640#issuecomment-6100164636)
    * @andre-fajar-n asked how to reproduce the bug in [microsoft/TypeScript#64668](https://github.com/microsoft/TypeScript/issues/64668#issuecomment-6106820085)
    * @YuanchengJiang provided repro steps as requested in [microsoft/TypeScript#64668](https://github.com/microsoft/TypeScript/issues/64668#issuecomment-6107485244)

## Activity Summary

### [Issue microsoft/TypeScript#28985](https://github.com/microsoft/TypeScript/issues/28985) (Open, `Suggestion`, `Awaiting More Feedback`)

**Remote declaration file**

*Enable referencing and importing TypeScript declaration (.d.ts) files directly from remote URLs.*

 * [5.3 years ago](https://github.com/microsoft/TypeScript/issues/28985#issuecomment-866751031) **kaaninel** said "Deno deals with this partially but afaik on typescript side there is no development so far. @BahaaZidan "
 * [5.2 years ago](https://github.com/microsoft/TypeScript/issues/28985#issuecomment-871908738) **pixelamit** asked how to share common logic via Single-spa utility and requested a working POC link
 * [31 weeks ago](https://github.com/microsoft/TypeScript/issues/28985#issuecomment-3996676287) **arkhipovdenis** shared a tool called ts-remote for generating and fetching consolidated remote TypeScript definitions in microfrontend projects and invited feedback
 * [today](https://github.com/microsoft/TypeScript/issues/28985#issuecomment-6105953953) **alshdavid** described a zero-bundler JIT transpilation setup using importmap and explained the need for npm install to obtain types; suggested enabling remote declaration files in the TypeScript language server

### [Issue microsoft/TypeScript#33866](https://github.com/microsoft/TypeScript/issues/33866) (Open, `Bug`, `Help Wanted`, `Domain: lib.d.ts`)

**Add types for window\.performance\.getEntriesByType**

*Add definitions to TypeScript’s standard library for window.performance.getEntriesByType to return properly typed PerformanceMark, PerformanceMeasure, and PerformanceResourceTiming entries.*

 * [3.5 years ago](https://github.com/microsoft/TypeScript/issues/33866#issuecomment-1501082692) **schickling** said "Is someone aware of any available NPM package that provides the missing types as a workaround for now?"
 * [1.2 years ago](https://github.com/microsoft/TypeScript/issues/33866#issuecomment-3120028664) **RyanCavanaugh** confirmed that the requested specialization was still absent in version 5.9 and pointed out that the OP's code example used `.navigator` instead of `.performance`, suggesting clarification of the current behavior
 * [1.1 years ago](https://github.com/microsoft/TypeScript/issues/33866#issuecomment-3125929003) **DerGernTod** highlighted that performance.getEntriesByName supports a second argument for entry type and suggested typing its return types accordingly
 * [later](https://github.com/microsoft/TypeScript/issues/33866#issuecomment-6110643262) **Ankith-B** offered to implement the change in TypeScript-DOM-lib-generator using additionalSignatures and described the prepared overloads for Performance entries, noted tests passed, and asked whether to proceed with a PR or use a different approach

### [Issue microsoft/TypeScript#57640](https://github.com/microsoft/TypeScript/issues/57640) (Open, `Bug`, `Help Wanted`, `Domain: Parser`)

**JS \| Optional chaining left hand assignment not detected as syntax error\.**

*VS Code fails to flag invalid left-hand assignment using optional chaining in JavaScript files.*

 * [1.7 years ago](https://github.com/microsoft/TypeScript/issues/57640#issuecomment-2568447792) **RyanCavanaugh** said "I think it'd still be preferable if we saw grammar errors in JS, it just means this is a bigger work item than this specific issue"
 * **RyanCavanaugh** added label `Domain: Parser`
 * [yesterday](https://github.com/microsoft/TypeScript/issues/57640#issuecomment-6078924694) **ehoogeveen-medweb** described that plain JS files already run the full checker and that optional-access diagnostics were being filtered out due to missing codes in the plainJSErrors allowlist, listed the five relevant diagnostic codes, explained a local patch adding them which reported no extra errors, and suggested applying the same five-line change in the Go implementation while noting a limitation for TS2780 cases
 * [today](https://github.com/microsoft/TypeScript/issues/57640#issuecomment-6100164636) **mahesh-desu** asked to be assigned to implement addition of TS2777–2781 to the plainJSErrors allowlist and extend grammar-error tests

### [Issue microsoft/TypeScript#64134](https://github.com/microsoft/TypeScript/issues/64134) (Open, `Bug`, `Needs Human Review`, **RyanCavanaugh**, **Copilot**)

**\`sourceMap\` emit is disproportionately slow for files containing one very large object literal**

*Source map generation in TypeScript 7 is significantly slower than in TypeScript 6 for files with a large object literal.*

 * (5 weeks ago) **RyanCavanaugh** added label `Needs Human Review`, and assigned to **Copilot**, **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript/issues/64134#issuecomment-6102276283) **trevorade** provided extra data points demonstrating that source map emission time grows quadratically with line length and that patch #64138 restores performance

### [Issue microsoft/TypeScript#64668](https://github.com/microsoft/TypeScript/issues/64668) (Open, `Bug`)

**panic: Unhandled case in Node\.MemberList**

*TypeScript compiler panics with an unhandled Node.MemberList case when evaluating an enum member that references a class in a merged namespace.*

 * created by **YuanchengJiang**
 * (3 days ago) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`
 * [later](https://github.com/microsoft/TypeScript/issues/64668#issuecomment-6106820085) **andre-fajar-n** said "Could you share how to reproduce this bug? @YuanchengJiang "
 * [later](https://github.com/microsoft/TypeScript/issues/64668#issuecomment-6107485244) **YuanchengJiang** provided reproduction steps including tsc command, commit hashes, build configuration, and OS details

### [Issue microsoft/TypeScript#64706](https://github.com/microsoft/TypeScript/issues/64706) (Open, `Bug`)

**Declaration emit renames value references when a shadowed type parameter shares its parameter's name**

*TypeScript declaration emit incorrectly renames value references in nested functions when inner and outer type parameters share the same name.*

 * created by **jasonkuhrt**
 * [today](https://github.com/microsoft/TypeScript/issues/64706#issuecomment-6101243821) **maricastroc** reproduced the issue on main, traced it to declaration emit identifier rewriting, and prepared a fix and regression tests while awaiting issue triage before opening a PR per the contribution guidelines

### [PR microsoft/TypeScript#64722](https://github.com/microsoft/TypeScript/pull/64722) (Open, `For Uncommitted Bug`)

**Merge export \* tables without per\-name collision trackers**

*Optimize export * symbol merging by eliminating per-name collision trackers and reducing table allocations.*

 * created by **gwkline**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64722#issuecomment-6100021037) **gwkline** said "@microsoft-github-policy-service agree"

### [Issue microsoft/TypeScript#64727](https://github.com/microsoft/TypeScript/issues/64727) (Open)

**TS 7: declaration emit property order depends on which other files are in the program**

*TypeScript 7’s declaration emitter produces inconsistent property ordering in generated d.ts files depending on which files are included in the program.*

 * created by **maschwenk**
 * [today](https://github.com/microsoft/TypeScript/issues/64727#issuecomment-6099523263) **maschwenk** said "I have no idea if this is something we care about or not so please feel free to dismiss"

### [PR microsoft/TypeScript#64728](https://github.com/microsoft/TypeScript/pull/64728) (Open, `For Uncommitted Bug`)

**Cache undefined widening properties per symbol, not per name**

*Key the undefined-property widening cache by symbol instead of name to ensure consistent property declarations across unrelated types.*

 * created by **maschwenk**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [PR microsoft/TypeScript#64729](https://github.com/microsoft/TypeScript/pull/64729) (Open, `For Milestone Bug`, **gabritto**)

**Dedupe identical object literal types before subtype reduction**

*Deduplicate identical object literal types before subtype reduction to prevent O(n²) performance blow-ups when type-checking large JSON arrays*

 * created by **gadcam**
 * (today) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64729#issuecomment-6100547125) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (today) **typescript-automation[bot]** added label `For Milestone Bug`, removed label `For Uncommitted Bug`, and assigned to **gabritto**
 * [today](https://github.com/microsoft/TypeScript/pull/64729#issuecomment-6100584800) **gadcam** said "@typescript-bot It fixes issue #48364"

### [Issue microsoft/TypeScript#64730](https://github.com/microsoft/TypeScript/issues/64730) (Open)

**TS 7\.0 reports declaration\-emit diagnostics \(e\.g\. TS2527\) under \-\-noEmit when other semantic errors exist; TS 6\.0 does not \(undocumented difference\)**

*TypeScript 7.0 reports declaration-emit diagnostics under --noEmit when other semantic errors are present, unlike 6.0.*

 * created by **seunghyun-24**

### [PR microsoft/TypeScript#64731](https://github.com/microsoft/TypeScript/pull/64731) (Open, `For Backlog Bug`)

**fix: Fix nil pointer panic in getLateBoundSymbol under \-\-noCheck**

*Declaration-only emit with --noCheck triggers a nil pointer panic in getLateBoundSymbol because the parent symbol can be nil.*

 * created by **andre-fajar-n**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64731#issuecomment-6105151890) **andre-fajar-n** said "@microsoft-github-policy-service agree"

### [PR microsoft/TypeScript#64732](https://github.com/microsoft/TypeScript/pull/64732) (Open, `For Backlog Bug`)

**Fix inline JSDoc links in optional type positions**

*Ensure inline link, linkcode, and linkplain tags after @throws and @returns are parsed as links instead of type expressions.*

 * created by **mbarinov**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/64732#issuecomment-6109636818) **mbarinov** said "@microsoft-github-policy-service agree"

### [Issue microsoft/TypeScript#64733](https://github.com/microsoft/TypeScript/issues/64733) (Closed)

**Downlevel \`static {}\` block emit rewrites \`this\.prop\` inside a nested \`function \(\)\` expression to the class alias \`\_a\.prop\`**

*When downleveling class static blocks to ES2021, tsgo wrongly rewrites `this.bar()` inside nested functions as `_a.bar()`, causing runtime errors.*

 * created by **trevorade**

### [PR microsoft/TypeScript#64734](https://github.com/microsoft/TypeScript/pull/64734) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Various memory optimizations**

*Combined memory optimizations reduce memory usage by 22–29% and allocation counts by 3.6–16.6% across nine test scenarios.*

 * created by **jakebailey**
 * (later) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [later](https://github.com/microsoft/TypeScript/pull/64734#issuecomment-6110569980) **jakebailey** said "@typescript-bot perf test this faster"
 * [later](https://github.com/microsoft/TypeScript/pull/64734#issuecomment-6110570961) **typescript-automation[bot]** posted build status update with links to started jobs and results
 * [later](https://github.com/microsoft/TypeScript/pull/64734#issuecomment-6110842190) **typescript-automation[bot]** posted the requested performance comparison report for the baseline versus PR

### [Issue microsoft/TypeScript#64769](https://github.com/microsoft/TypeScript/issues/64769) (Open)

**Refactor \> \.\.\.  does nothing /  fails silently for \.tsx components that consume css module style\(s\)**

*Refactoring TSX components that import CSS module styles with “Move to new file” fails silently due to a TypeScript Server error.*

 * created by **IanBellomy**
 * **vs-code-engineering[bot]** assigned to **dbaeumer**

