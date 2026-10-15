# Report for 2026-10-12 (Monday, October 12th, 2026)

18 different users commented on 61 different issues.

## Recommended Actions

 * Response Recommended
    * @scottohara asked for documentation updates and maintainer attention to stale TSconfig reference in [microsoft/TypeScript#63392](https://github.com/microsoft/TypeScript/issues/63392#issuecomment-6135402346)
    * @elecmonkey asked whether an allowlist for fields should be added in [microsoft/TypeScript#64158](https://github.com/microsoft/TypeScript/pull/64158#issuecomment-6137388740)
    * @rf- asked whether linking an issue is mandatory or optional in [microsoft/TypeScript#64750](https://github.com/microsoft/TypeScript/pull/64750#issuecomment-6130706910)
    * @moznion offered to submit a pull request to fix the issue in [microsoft/TypeScript#64763](https://github.com/microsoft/TypeScript/issues/64763#issuecomment-6139366580)

## Activity Summary

### [Issue microsoft/TypeScript#54099](https://github.com/microsoft/TypeScript/issues/54099) (Closed, `Bug`, `Help Wanted`, `Domain: Decorators`)

**Unknown interface "ClassMethodDecoratorFunction" in documentation for 5\.0\.4 lib\.decorators\.d\.ts**

*TypeScript 5.0.4 decorators.d.ts documentation incorrectly references a non-existent ClassMethodDecoratorFunction interface instead of ClassMethodDecoratorContext.*

 * (3 weeks ago) **RyanCavanaugh** added label `Needs Human Review`, and removed labels `Docs`, `Needs Human Review`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#54338](https://github.com/microsoft/TypeScript/issues/54338) (Closed, `Bug`, `Help Wanted`, `Domain: Decorators`)

**Comment referencing an undefined \`ClassDecoratorFunction\` type**

*decorators.d.ts references an undefined ClassDecoratorFunction type in the library definitions*

 * (3 weeks ago) **RyanCavanaugh** added label `Needs Human Review`, and removed labels `Docs`, `Needs Human Review`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#55989](https://github.com/microsoft/TypeScript/pull/55989) (Closed, `For Milestone Bug`, **navya9singh**)

**Update lib\.dom\.d\.ts: \`MutationObserverInit\.attributeFilter\` can accept an iterator**

*Update lib.dom.d.ts so that MutationObserverInit.attributeFilter accepts iterators in addition to arrays.*

 * **RyanCavanaugh** added to milestone `Post-7.0 lib candidates`
 * (3 weeks ago) **typescript-automation[bot]** added label `For Milestone Bug`, and removed label `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/55989#issuecomment-6130566178) **jakebailey** said "Been a while but this can't get merged here, as it needs to go through the other repo, and also it's in the wrong place now after TS7."
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#63392](https://github.com/microsoft/TypeScript/issues/63392) (Open, `Docs`, **RyanCavanaugh**)

**Review/update https://typescriptlang\.org/tsconfig for TypeScript 6/7**

*Update the TypeScript tsconfig documentation to correct outdated defaults and remove deprecated options for TypeScript versions 6 and 7.*

 * **RyanCavanaugh** assigned to **RyanCavanaugh**
 * [25 weeks ago](https://github.com/microsoft/TypeScript/issues/63392#issuecomment-4245971467) **mkantor** asked if the tsconfig descriptions need separate updates in the TypeScript-Website repository
 * [13 weeks ago](https://github.com/microsoft/TypeScript/issues/63392#issuecomment-4924067326) **jonkoops** opened two PRs on the TypeScript-Website repo to fix the module and moduleResolution defaults in tsconfigRules.ts
 * [today](https://github.com/microsoft/TypeScript/issues/63392#issuecomment-6135402346) **scottohara** reported discrepancies between the 6.0 release announcement, the official TSconfig reference, and the output of tsc --all, and urged updating the stale documentation

### [PR microsoft/TypeScript#63424](https://github.com/microsoft/TypeScript/pull/63424) (Closed, `For Uncommitted Bug`)

**Add \`Intl\.PluralRules\.selectRange\` typing to es2023\.intl**

*Add the missing Intl.PluralRules.selectRange type definition to ES2023 Intl declarations in TypeScript.*

 * **typescript-bot** added label `For Uncommitted Bug`
 * [24 weeks ago](https://github.com/microsoft/TypeScript/pull/63424#issuecomment-4302615156) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [24 weeks ago](https://github.com/microsoft/TypeScript/pull/63424#issuecomment-4302615177) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64158](https://github.com/microsoft/TypeScript/pull/64158) (Closed, `Author: Team`, `For Uncommitted Bug`, **iisaduan**)

**Build Orchestrator API **

*Introduce a BuildOrchestrator API in TS7.1 replacing SolutionBuilder to perform project builds, cleans, and their references with customizable options.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/64158#issuecomment-5839239607) **andrewbranch** said "It would probably be worthwhile to update the PR description to reflect the latest review changes since PRs are all the docs we have for the moment."
 * (2 weeks ago) **iisaduan** closed the issue
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/64158#issuecomment-6054576820) **elecmonkey** asked about adding noEmit to OverrideCompilerOptions and offered to send a PR
 * [today](https://github.com/microsoft/TypeScript/pull/64158#issuecomment-6130417403) **iisaduan** explained that OverrideCompilerOptions were the ones explicitly allowed in the previous compiler and offered to add noEmit and related options via a PR later
 * [today](https://github.com/microsoft/TypeScript/pull/64158#issuecomment-6137388740) **elecmonkey** created a PR adding noEmit, removed JSON name tags to ensure orchestrator options reached the server, and asked whether an allowlist for fields should be added

### [PR microsoft/TypeScript#64307](https://github.com/microsoft/TypeScript/pull/64307) (Open, `For Milestone Bug`, **ahejlsberg**)

**Normalize distributed type parameters in conditional type relationships**

*Ensure target types in TypeScript conditional type relationships are instantiated to properly normalize distributed type parameters.*

 * (today) **typescript-automation[bot]** added label `For Milestone Bug`, and removed label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64307#issuecomment-6121069156) **Andarist** said "thanks @trevorade for extra test cases! :)"
 * [today](https://github.com/microsoft/TypeScript/pull/64307#issuecomment-6130659947) **Andarist** said "@jakebailey i synced this with the recent changes from main, so this should compile now 😉 "

### [PR microsoft/TypeScript#64353](https://github.com/microsoft/TypeScript/pull/64353) (Closed, `For Backlog Bug`)

**Fix invalid decorator examples in lib\.decorators\.d\.ts**

*Rewrite invalid decorator examples in lib.decorators.d.ts to use correct context types and fix syntax errors.*

 * created by **wfatih**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [3 weeks ago](https://github.com/microsoft/TypeScript/pull/64353#issuecomment-5744120251) **wfatih** said "@microsoft-github-policy-service agree"
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#64494](https://github.com/microsoft/TypeScript/issues/64494) (Closed, `Bug`, **weswigham**)

**Decorated class gets \`name === "\_a"\` when a \`\#private\` field initializer references the class \(regression in 7\.0\)**

*Decorated classes with private field initializers referencing the class incorrectly get named `_a` instead of their declared name.*

 * created by **bagbag**
 * (2 weeks ago) **RyanCavanaugh** added label `Bug`, and assigned to **weswigham**
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript#64505](https://github.com/microsoft/TypeScript/pull/64505) (Closed, `For Uncommitted Bug`, **weswigham**)

**fix\(64494\): fix decorated class names with private member self\-references**

*Corrects decorated class naming to properly preserve private member self-references*

 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/64505#issuecomment-5874738643) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * **typescript-automation[bot]** assigned to **weswigham**
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript#64588](https://github.com/microsoft/TypeScript/pull/64588) (Closed, `For Uncommitted Bug`)

**Restore symbol names in JSX import action titles**

*Restores symbol names in JSX import action titles by porting Strada’s logic and fixes two skipped tests.*

 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64588#issuecomment-5957506745) **jakebailey** said "Copilot absolutely hates this 😄 "
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/64588#issuecomment-6056683833) **Andarist** noted disagreement with Copilot suggestions and asked if anything else should be addressed after adding extra coverage
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/64588#issuecomment-6090647089) **jakebailey** said "Ah, because the review happened during an outage."
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#64590](https://github.com/microsoft/TypeScript/issues/64590) (Closed, `Bug`, **weswigham**)

**Declaration emit writes an import the file cannot resolve when the package has \`exports\`; no TS2883**

*TypeScript’s declaration emit generates unresolved imports for packages with an exports map in pnpm layouts without emitting TS2883 errors*

 * (6 days ago) **RyanCavanaugh** added label `Bug`, set milestone to `TypeScript 7.1.1 RC`, and assigned to **weswigham**
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript#64599](https://github.com/microsoft/TypeScript/pull/64599) (Closed, `For Milestone Bug`, **weswigham**)

**Check package reachability before using exports in declarations**

*Reorder TypeScript’s export resolution logic to ensure package reachability is checked before applying exports in declarations*

 * (6 days ago) **typescript-automation[bot]** added label `For Milestone Bug`, and assigned to **weswigham**
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/64599#issuecomment-6054835458) **Andarist** said "@weswigham I resolved the conflicts, the PR should be ready to land now"
 * (today) **weswigham** closed the issue

### [Issue microsoft/TypeScript#64628](https://github.com/microsoft/TypeScript/issues/64628) (Closed, `Bug`, **weswigham**)

**JSDoc \`@private\` / \`@protected\` are dropped in declaration emit for properties declared by constructor assignment**

*TypeScript 7.0.2 drops JSDoc @private/@protected visibility and types for constructor-assigned properties in declaration files.*

 * (6 days ago) **RyanCavanaugh** added label `Bug`, set milestone to `TypeScript 7.1.1 RC`, and assigned to **weswigham**
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript#64657](https://github.com/microsoft/TypeScript/pull/64657) (Open, `For Milestone Bug`, **weswigham**)

**Show the JSDoc written on an \`import x = a\.x\` alias in hover and completions**

*Enable display of alias-specific JSDoc comments on import aliases during hover and completions.*

 * [5 days ago](https://github.com/microsoft/TypeScript/pull/64657#issuecomment-6048754588) **patrickkettner** offered to widen the PR to show the whole chain on both refs, noting preference for that approach and explaining prior decision to maintain parity with version 6.0
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/64657#issuecomment-6065773879) **weswigham** said "Yeah, if we're gonna change anything here, I'd wanna make it consistent across reference site kinds and include all the docs possible, for sure."
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/64657#issuecomment-6069469752) **patrickkettner** asked whether hover should display both @since tags from alias and implementation or if the alias wins
 * [today](https://github.com/microsoft/TypeScript/pull/64657#issuecomment-6129170180) **weswigham** clarified that only type-providing tags are semantic and assumed other tags are just documentation shown inline

### [PR microsoft/TypeScript#64662](https://github.com/microsoft/TypeScript/pull/64662) (Closed, `Author: Team`, `For Backlog Bug`, **jakebailey**)

**Unify recursive type naming during serialization**

*Unify recursive type naming in serialization by replacing existing recursion trackers with a single approach for name reuse.*

 * [5 days ago](https://github.com/microsoft/TypeScript/pull/64662#issuecomment-6046771773) **typescript-automation[bot]** reported test results comparing baseline and pr and flagged new type errors in bluebird tests
 * [5 days ago](https://github.com/microsoft/TypeScript/pull/64662#issuecomment-6046773996) **typescript-automation[bot]** posted the perf run results requested by @jakebailey
 * [5 days ago](https://github.com/microsoft/TypeScript/pull/64662#issuecomment-6047632196) **typescript-automation[bot]** reported that running the top 400 repos tsc comparison between baseline and pr succeeded without issues
 * [today](https://github.com/microsoft/TypeScript/pull/64662#issuecomment-6130874315) **jakebailey** noted that the issue was superseded by two linked TypeScript issues containing test commits and fixes
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#64687](https://github.com/microsoft/TypeScript/issues/64687) (Closed, `Bug`, **RyanCavanaugh**, **Copilot**)

**Replacement libs load in an arbitrary order in TypeScript 7: \`sortLibs\` is not stable**

*TypeScript 7's unstable sortLibs causes libReplacement to load libraries in arbitrary order, breaking overload precedence.*

 * (4 days ago) **RyanCavanaugh** set milestone to `Backlog`, and assigned to **Copilot**, **RyanCavanaugh**
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#64693](https://github.com/microsoft/TypeScript/pull/64693) (Closed, `For Uncommitted Bug`, **RyanCavanaugh**, **Copilot**)

**Preserve replacement lib order during sorting**

*Implement stable sorting for replacement libraries to preserve their configured order and ensure consistent overload resolution*

 * (4 days ago) **typescript-automation[bot]** added labels `For Milestone Bug`, `For Uncommitted Bug`, and removed label `For Milestone Bug`
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#64695](https://github.com/microsoft/TypeScript/pull/64695) (Open, `For Milestone Bug`, **ahejlsberg**)

**\[experiment\] Skip incompatible discriminants when inferring**

*Experimentally skip incompatible discriminant properties during TypeScript union type inference to reduce workload and validate via tests.*

 * [4 days ago](https://github.com/microsoft/TypeScript/pull/64695#issuecomment-6066282755) **weswigham** noted that previous JS codebase type comparisons were costly, acknowledged the perf suite improvements, and suggested using discriminateTypeByDiscriminableItems for consistent discrimination method
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/64695#issuecomment-6066595594) **typescript-automation[bot]** reported that running the top 400 repos tsc comparison between baseline and pr succeeded without issues
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64695#issuecomment-6113604981) **Andarist** requested a full test rerun to evaluate performance
 * [today](https://github.com/microsoft/TypeScript/pull/64695#issuecomment-6133128517) **jakebailey** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/64695#issuecomment-6133129924) **typescript-automation[bot]** reported the start and completion statuses of CI jobs
 * [today](https://github.com/microsoft/TypeScript/pull/64695#issuecomment-6133475106) **typescript-automation[bot]** notified that DT test results were ready and showed no changes
 * [today](https://github.com/microsoft/TypeScript/pull/64695#issuecomment-6133547696) **typescript-automation[bot]** reported tsc user test results and confirmed everything looked good
 * [today](https://github.com/microsoft/TypeScript/pull/64695#issuecomment-6133547985) **typescript-automation[bot]** provided the requested performance run results for tsc
 * [today](https://github.com/microsoft/TypeScript/pull/64695#issuecomment-6134265513) **typescript-automation[bot]** reported that running the top 400 repos tsc comparison between baseline and pr succeeded without issues

### [PR microsoft/TypeScript#64696](https://github.com/microsoft/TypeScript/pull/64696) (Closed, `Author: Team`, `For Milestone Bug`, **weswigham**)

**Use ensureModifierFlags to calculate jsdoc constructor property modifiers**

*Implement ensureModifierFlags to properly calculate modifier flags for JSDoc constructor properties.*

 * **typescript-automation[bot]** added label `For Milestone Bug`
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/64696#issuecomment-6066958664) **hkleungai** asked if the PR would affect issue #3665 given its example wasn’t in the test suite
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/64696#issuecomment-6067934267) **jakebailey** said "I would assume none? You're asking for the old override behavior back, but this just fixes an emit bug?"
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript#64728](https://github.com/microsoft/TypeScript/pull/64728) (Open, `For Uncommitted Bug`)

**Cache undefined widening properties per symbol, not per name**

*Key the undefined-property widening cache by symbol instead of name to ensure consistent property declarations across unrelated types.*

 * created by **maschwenk**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64728#issuecomment-6129506551) **jakebailey** said "Unless copilot points out something I missed, this fix seems fine"

### [PR microsoft/TypeScript#64729](https://github.com/microsoft/TypeScript/pull/64729) (Open, `For Milestone Bug`, **gabritto**)

**Dedupe identical object literal types before subtype reduction**

*Deduplicate identical object literal types before subtype reduction to prevent O(n²) performance blow-ups when type-checking large JSON arrays*

 * (2 days ago) **typescript-automation[bot]** added label `For Milestone Bug`, and removed label `For Uncommitted Bug`
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/64729#issuecomment-6100584800) **gadcam** said "@typescript-bot It fixes issue #48364"
 * [today](https://github.com/microsoft/TypeScript/pull/64729#issuecomment-6133263114) **jakebailey** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/64729#issuecomment-6133264470) **typescript-automation[bot]** reported CI job statuses with links to build results
 * [today](https://github.com/microsoft/TypeScript/pull/64729#issuecomment-6133664102) **typescript-automation[bot]** provided the results of the requested performance run
 * [today](https://github.com/microsoft/TypeScript/pull/64729#issuecomment-6133846968) **typescript-automation[bot]** notified that the DT test results were ready and unchanged
 * [today](https://github.com/microsoft/TypeScript/pull/64729#issuecomment-6134012975) **typescript-automation[bot]** reported tsc user test results and confirmed everything looked good
 * [today](https://github.com/microsoft/TypeScript/pull/64729#issuecomment-6134415656) **typescript-automation[bot]** reported that running the top 400 repos tsc comparison between baseline and pr succeeded without issues

### [PR microsoft/TypeScript#64732](https://github.com/microsoft/TypeScript/pull/64732) (Open, `For Backlog Bug`)

**Fix inline JSDoc links in optional type positions**

*Ensure inline link, linkcode, and linkplain tags after @throws and @returns are parsed as links instead of type expressions.*

 * created by **mbarinov**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64732#issuecomment-6109636818) **mbarinov** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript/pull/64732#issuecomment-6130609835) **jakebailey** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/64732#issuecomment-6130611511) **typescript-automation[bot]** posted automated build status updates for test commands with start and result links
 * [today](https://github.com/microsoft/TypeScript/pull/64732#issuecomment-6131000957) **typescript-automation[bot]** reported that the DT test results were ready and unchanged
 * [today](https://github.com/microsoft/TypeScript/pull/64732#issuecomment-6131086083) **typescript-automation[bot]** reported the perf run results in a detailed comparison report
 * [today](https://github.com/microsoft/TypeScript/pull/64732#issuecomment-6131105060) **typescript-automation[bot]** reported tsc user test results and confirmed everything looked good
 * [today](https://github.com/microsoft/TypeScript/pull/64732#issuecomment-6131812308) **typescript-automation[bot]** reported that running the top 400 repos tsc comparison between baseline and pr succeeded without issues

### [Issue microsoft/TypeScript#64733](https://github.com/microsoft/TypeScript/issues/64733) (Closed)

**Downlevel \`static {}\` block emit rewrites \`this\.prop\` inside a nested \`function \(\)\` expression to the class alias \`\_a\.prop\`**

*When downleveling class static blocks to ES2021, tsgo wrongly rewrites `this.bar()` inside nested functions as `_a.bar()`, causing runtime errors.*

 * created by **trevorade**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64734](https://github.com/microsoft/TypeScript/pull/64734) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Various memory optimizations**

*Combined memory optimizations reduce memory usage by 22–29% and allocation counts by 3.6–16.6% across nine test scenarios.*

 * [today](https://github.com/microsoft/TypeScript/pull/64734#issuecomment-6126968288) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/64734#issuecomment-6126970184) **typescript-automation[bot]** announced start of performance test jobs and provided build and result links
 * [today](https://github.com/microsoft/TypeScript/pull/64734#issuecomment-6127473879) **typescript-automation[bot]** posted the performance run results for the requested comparison
 * [today](https://github.com/microsoft/TypeScript/pull/64734#issuecomment-6134654273) **jakebailey** removed changes from PR #64735 while retaining issue #64063 and requested performance tests
 * [today](https://github.com/microsoft/TypeScript/pull/64734#issuecomment-6134655235) **typescript-automation[bot]** initiated performance test builds and provided status and results links
 * [today](https://github.com/microsoft/TypeScript/pull/64734#issuecomment-6134989198) **typescript-automation[bot]** provided the performance run results with a comparison report for tsc metrics

### [PR microsoft/TypeScript#64735](https://github.com/microsoft/TypeScript/pull/64735) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Resolve instantiated object members through a shared worker**

*Allow instantiated object members to be resolved properly when used inside shared workers.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/64735#issuecomment-6111932716) **jakebailey** said "@typescript-bot perf test this faster"
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64735#issuecomment-6111933678) **typescript-automation[bot]** announced that performance test jobs started and would be updated as builds progress
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64735#issuecomment-6112187980) **typescript-automation[bot]** provided the requested performance run results including a detailed baseline vs pr comparison report
 * [today](https://github.com/microsoft/TypeScript/pull/64735#issuecomment-6129177084) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/64735#issuecomment-6129178555) **typescript-automation[bot]** reported that performance tests started and provided links to status and results
 * [today](https://github.com/microsoft/TypeScript/pull/64735#issuecomment-6129638105) **typescript-automation[bot]** posted the requested perf run results comparing baseline and PR, showing symbol count reduction and memory usage improvements

### [PR microsoft/TypeScript#64738](https://github.com/microsoft/TypeScript/pull/64738) (Closed, `For Uncommitted Bug`)

**Keep \`this\` inside functions nested in downleveled static blocks**

*Fix downleveled static blocks incorrectly rewriting this in nested functions to the class alias by using the active visitor.*

 * created by **trevorade**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64739](https://github.com/microsoft/TypeScript/pull/64739) (Closed, `Author: Team`, `For Uncommitted Bug`, **ahejlsberg**)

**Shrink \`ValueSymbolLinks\` by 16 bytes**

*Relocating a boolean into a separate set reduces ValueSymbolLinks memory by 16 bytes (1%) when compiling VS Code.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/64739#issuecomment-6115561958) **ahejlsberg** said "@typescript-bot perf test this faster"
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64739#issuecomment-6115562754) **typescript-automation[bot]** indicated that the performance test job started and provided status and results links
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64739#issuecomment-6115800643) **typescript-automation[bot]** posted performance run results for the requested comparison on the PR
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript#64743](https://github.com/microsoft/TypeScript/pull/64743) (Open, `For Backlog Bug`)

**Fix enum crash when namespace and enum share a name**

*Guard enum value computation and treat ModuleBlock as a member container to prevent compiler panic when a namespace and enum share the same name.*

 * created by **smg99**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/64743#issuecomment-6140428607) **smg99** addressed the AST API invariant review by removing the unrelated KindModuleBlock branch from Node.MemberList() and retaining only the targeted enum guard and regression case; noted that the Microsoft CLA remained pending contributor authorization
 * [later](https://github.com/microsoft/TypeScript/pull/64743#issuecomment-6140953790) **jakebailey** said "If you're not a person who can sign a CLA, I don't think you should be sending PRs"
 * [later](https://github.com/microsoft/TypeScript/pull/64743#issuecomment-6143495673) **smg99** said "@microsoft-github-policy-service agree"

### [PR microsoft/TypeScript#64749](https://github.com/microsoft/TypeScript/pull/64749) (Open, `Author: Team`, `For Uncommitted Bug`, **iisaduan**)

**script to fill out missing api functions**

*Implement a script to fill out missing API function definitions*

 * created by **iisaduan**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **iisaduan**

### [PR microsoft/TypeScript#64750](https://github.com/microsoft/TypeScript/pull/64750) (Open, `For Uncommitted Bug`)

**Add support for Jujutsu conflict markers**

*Extend TypeScript’s conflict marker detection to support Jujutsu-style markers using %, \ and + separators.*

 * created by **rf-**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64750#issuecomment-6130652737) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [today](https://github.com/microsoft/TypeScript/pull/64750#issuecomment-6130706910) **rf-** asked whether opening a linked issue was mandatory or optional
 * [today](https://github.com/microsoft/TypeScript/pull/64750#issuecomment-6130717671) **rf-** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript/pull/64750#issuecomment-6130727617) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/64750#issuecomment-6130729363) **typescript-automation[bot]** posted initial build status with results table
 * [today](https://github.com/microsoft/TypeScript/pull/64750#issuecomment-6131219606) **typescript-automation[bot]** reported the results of the requested perf run

### [PR microsoft/TypeScript#64751](https://github.com/microsoft/TypeScript/pull/64751) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Unify recursive type naming during serialization**

*Unify the naming convention for recursive types during serialization to ensure consistent type identification.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#64752](https://github.com/microsoft/TypeScript/pull/64752) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Bind anonymous recursive types during declaration serialization**

*Implement support for binding anonymous recursive types during declaration serialization.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [Issue microsoft/TypeScript#64754](https://github.com/microsoft/TypeScript/issues/64754) (Closed)

**\[api\] createSnapshot never returns when the opened tsconfig\.json has a circular extends**

*createSnapshot hangs indefinitely on projects whose tsconfig.json files have circular extends.*

 * created by **cplieger**

### [PR microsoft/TypeScript#64755](https://github.com/microsoft/TypeScript/pull/64755) (Closed, `For Uncommitted Bug`)

**\[api\] Leave a config out of its own extended source files**

*Skip adding a tsconfig file to its own ExtendedSourceFiles list to prevent createSnapshot hangs on circular extends chains*

 * created by **cplieger**
 * (today) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`

### [PR microsoft/TypeScript#64756](https://github.com/microsoft/TypeScript/pull/64756) (Open, `Author: Team`, `For Uncommitted Bug`, **DanielRosenwasser**)

**Try using a map for resolved write\-side types\.**

*Use a map data structure to manage resolved write-side types more efficiently.*

 * created by **DanielRosenwasser**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript/pull/64756#issuecomment-6133830605) **DanielRosenwasser** said "@typescript-bot perf test this"
 * [today](https://github.com/microsoft/TypeScript/pull/64756#issuecomment-6133831900) **typescript-automation[bot]** posted automated build status update
 * [today](https://github.com/microsoft/TypeScript/pull/64756#issuecomment-6134218314) **typescript-automation[bot]** provided the performance run results for the requested comparison
 * [today](https://github.com/microsoft/TypeScript/pull/64756#issuecomment-6134730254) **DanielRosenwasser** said "@typescript-bot perf test this"
 * [today](https://github.com/microsoft/TypeScript/pull/64756#issuecomment-6134731268) **typescript-automation[bot]** indicated that performance test jobs started and provided links to build status and results
 * [today](https://github.com/microsoft/TypeScript/pull/64756#issuecomment-6135074438) **typescript-automation[bot]** posted the requested perf run results with a comparison report including metrics for errors, symbols, types, memory usage, and allocations

### [Issue microsoft/TypeScript#64757](https://github.com/microsoft/TypeScript/issues/64757) (Open)

**Regression in 7\.1 \(\#64553\): R inferred as unknown through a generic type alias call signature with a nested same\-type argument**

*A TypeScript 7.1 regression makes R infer as unknown rather than Req in a nested generic type alias call signature.*

 * created by **kennysarnoski-jarvis**

### [Issue microsoft/TypeScript#64758](https://github.com/microsoft/TypeScript/issues/64758) (Open)

**TS7 LSP: documentHighlight returns nothing when the file path contains '@'**

*DocumentHighlight fails for file paths containing '@' because TS7 LSP server percent-encodes '@' as '%40' while client does not.*

 * created by **snapwich**

### [PR microsoft/TypeScript#64759](https://github.com/microsoft/TypeScript/pull/64759) (Open, `For Uncommitted Bug`)

**Add noEmit to BuildOrchestrator overrideCompilerOptions**

*Add noEmit to BuildOrchestrator overrideCompilerOptions and correct Go-side JSON mapping of compiler options*

 * created by **elecmonkey**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64759#issuecomment-6137076111) **elecmonkey** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript/pull/64759#issuecomment-6137357032) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."

### [Issue microsoft/TypeScript#64760](https://github.com/microsoft/TypeScript/issues/64760) (Open, `Bug`, **weswigham**)

**Declaration emit writes = Infinity initializers for overflowing number literals \(invalid \.d\.ts, TS1254\)**

*TypeScript's declaration emit incorrectly uses Infinity and -Infinity initializers for overflowing numeric literals in .d.ts files, causing TS1254 errors.*

 * created by **sidcraftscode**

### [PR microsoft/TypeScript#64761](https://github.com/microsoft/TypeScript/pull/64761) (Open, `For Uncommitted Bug`)

**Fix invalid declaration emit for constants whose value is Infinity or NaN**

*Replace invalid Infinity, -Infinity, and NaN initializers in declaration files with number type annotations for constants.*

 * created by **sidcraftscode**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64761#issuecomment-6137295006) **sidcraftscode** said "@microsoft-github-policy-service agree"

### [PR microsoft/TypeScript#64762](https://github.com/microsoft/TypeScript/pull/64762) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Fix symbol table kind mask**

*Restore alias caching and the members fast path by ensuring the symbol table kind mask includes all three kind bits.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/64762#issuecomment-6138956554) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/64762#issuecomment-6138957785) **typescript-automation[bot]** reported build status for performance test and provided results link
 * [today](https://github.com/microsoft/TypeScript/pull/64762#issuecomment-6139283586) **typescript-automation[bot]** posted the requested perf run results

### [Issue microsoft/TypeScript#64763](https://github.com/microsoft/TypeScript/issues/64763) (Open, `Won't Fix`)

**Parser: exponential time and memory on nested \`a \< \(b = …\)\` \(failed type argument speculation is retried\)**

*Nested 'a < (b = …)' expressions trigger exponential parsing time and memory growth in TypeScript due to retrying failed type argument speculation.*

 * created by **moznion**
 * [today](https://github.com/microsoft/TypeScript/issues/64763#issuecomment-6139366580) **moznion** said "I’ve already prepared a patch in https://github.com/microsoft/TypeScript/compare/main...moznion:TypeScript:fix/parser-type-arguments-retry, so I’d be happy to submit a pull request to fix this issue."

### [PR microsoft/TypeScript#64764](https://github.com/microsoft/TypeScript/pull/64764) (Closed, `For Uncommitted Bug`)

**Update localization files**

*Update localization files and regenerate corresponding runtime artifacts.*

 * created by **typescript-automation[bot]**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [PR microsoft/TypeScript#64765](https://github.com/microsoft/TypeScript/pull/64765) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Resolve class and interface members through shared layouts**

*Use shared member layouts and lazy resolution for instantiated classes and interfaces to significantly reduce checker memory and symbol creation overhead.*

 * created by **jakebailey**
 * [later](https://github.com/microsoft/TypeScript/pull/64765#issuecomment-6140765272) **jakebailey** said "@typescript-bot test it"
 * (later) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [later](https://github.com/microsoft/TypeScript/pull/64765#issuecomment-6140766616) **typescript-automation[bot]** posted an automated CI status update showing started jobs and links to their results
 * [later](https://github.com/microsoft/TypeScript/pull/64765#issuecomment-6141150189) **typescript-automation[bot]** reported DT test results showing type errors in the mdx package
 * [later](https://github.com/microsoft/TypeScript/pull/64765#issuecomment-6141222275) **typescript-automation[bot]** provided the requested performance run results
 * [later](https://github.com/microsoft/TypeScript/pull/64765#issuecomment-6141228441) **typescript-automation[bot]** reported tsc user test results and confirmed everything looked good
 * [later](https://github.com/microsoft/TypeScript/pull/64765#issuecomment-6142041200) **typescript-automation[bot]** reported that running the top 400 repos tsc comparison between baseline and pr succeeded without issues
 * [later](https://github.com/microsoft/TypeScript/pull/64765#issuecomment-6142282409) **jakebailey** said "@typescript-bot test it"
 * [later](https://github.com/microsoft/TypeScript/pull/64765#issuecomment-6142284071) **typescript-automation[bot]** provided automated CI build status updates for test jobs
 * [later](https://github.com/microsoft/TypeScript/pull/64765#issuecomment-6142671359) **typescript-automation[bot]** reported that DT test results were ready and unchanged
 * [later](https://github.com/microsoft/TypeScript/pull/64765#issuecomment-6142771607) **typescript-automation[bot]** announced the requested performance run results with a detailed comparison report
 * [later](https://github.com/microsoft/TypeScript/pull/64765#issuecomment-6142780972) **typescript-automation[bot]** reported tsc user test results and confirmed everything looked good
 * [later](https://github.com/microsoft/TypeScript/pull/64765#issuecomment-6143576591) **typescript-automation[bot]** reported that running the top 400 repos tsc comparison between baseline and pr succeeded without issues

### [Issue microsoft/TypeScript#64766](https://github.com/microsoft/TypeScript/issues/64766) (Open, `Bug`)

**\`===\` narrowing of a primitive union now produces a non\-widening literal type \(regression from microsoft/typescript\-go\#4781\)**

*Primitive union values narrowed by an equality check now generate non-widening literal types in TypeScript Go, causing assignment errors.*

 * created by **sophiebits**

### [PR microsoft/TypeScript#64767](https://github.com/microsoft/TypeScript/pull/64767) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Replace most ID usage with pointers**

*Replace ID references with direct pointers to eliminate atomic ID loads, enhance locality, and reduce overhead.*

 * created by **jakebailey**
 * (later) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [later](https://github.com/microsoft/TypeScript/pull/64767#issuecomment-6143646033) **jakebailey** said "@typescript-bot perf test this faster"
 * [later](https://github.com/microsoft/TypeScript/pull/64767#issuecomment-6143647694) **typescript-automation[bot]** announced that performance test jobs had started and provided status and results links
 * [later](https://github.com/microsoft/TypeScript/pull/64767#issuecomment-6144129514) **typescript-automation[bot]** posted the requested performance run results

### [Issue microsoft/TypeScript#64768](https://github.com/microsoft/TypeScript/issues/64768) (Closed)

**TS2536 indexing an \`as\`\-remapped mapped type by \`Exclude\<keyof T & string, \.\.\.\>\` \(native 7\.0\.2 only\)**

*TypeScript 7.0.2 incorrectly reports TS2536 when indexing an as-remapped mapped type with Exclude<keyof T & string>.*

 * created by **kokipsiho**

### [Issue microsoft/TypeScript#64769](https://github.com/microsoft/TypeScript/issues/64769) (Open)

**Refactor \> \.\.\.  does nothing /  fails silently for \.tsx components that consume css module style\(s\)**

*Refactoring TSX components that import CSS module styles with “Move to new file” fails silently due to a TypeScript Server error.*

 * created by **IanBellomy**
 * **vs-code-engineering[bot]** assigned to **dbaeumer**
 * **dbaeumer** unassigned **dbaeumer**

### [PR microsoft/TypeScript#64770](https://github.com/microsoft/TypeScript/pull/64770) (Closed, `For Backlog Bug`)

**Fix nil panic when stripInternal elides type alias RHS**

*Substitute any for stripped internal type alias right-hand sides under stripInternal to avoid nil pointer panics during declaration emit.*

 * created by **andre-fajar-n**
 * (later) **typescript-automation[bot]** added labels `For Backlog Bug`, `For Backlog Bug`

### [PR microsoft/TypeScript#64771](https://github.com/microsoft/TypeScript/pull/64771) (Open, `For Milestone Bug`)

**Preserve widening literals when narrowing primitive unions by equality**

*Preserve widened literal types during equality-based narrowing of primitive unions in TypeScript.*

 * created by **Andarist**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [PR microsoft/TypeScript#64772](https://github.com/microsoft/TypeScript/pull/64772) (Closed, `For Uncommitted Bug`)

**Port missing keyof simplification for generic mapped types with name types**

*Port missing keyof simplification support for generic mapped types with name types and correct a misported pull request.*

 * created by **Andarist**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

