# Report for 2026-08-24 (Monday, August 24th, 2026)

26 different users commented on 66 different issues.

## Recommended Actions

 * Response Recommended
    * @MulverineX requested that types be implemented instead of vendored in [microsoft/TypeScript#63248](https://github.com/microsoft/TypeScript/pull/63248#issuecomment-5398875333)
    * @uncaught provided requested log excerpt in [microsoft/TypeScript#63946](https://github.com/microsoft/TypeScript/issues/63946#issuecomment-5411240428)
    * @denis-migdal asked about officially encouraged patterns and proposed creating an index to reduce duplicate issues in [microsoft/TypeScript#63979](https://github.com/microsoft/TypeScript/issues/63979#issuecomment-5401226810)
    * @snarbles2 suggested linking a community-maintained resource from the official docs and hosting it in a wiki-like repo in [microsoft/TypeScript#63979](https://github.com/microsoft/TypeScript/issues/63979#issuecomment-5401336118)
    * @denis-migdal asked if a site already exists and inquired about TS's requirements for ownership, linking, triage, and promotion in [microsoft/TypeScript#63979](https://github.com/microsoft/TypeScript/issues/63979#issuecomment-5405840236)

## Activity Summary

### [Issue microsoft/TypeScript#47731](https://github.com/microsoft/TypeScript/issues/47731) (Open, `Bug`, `Help Wanted`, `Domain: check: Control Flow`)

**Narrow subtype\-reduction\-prone unions to their narrowest constituent**

*TypeScript fails to narrow a union to its assigned subtype inside an if branch, retaining an overly broad type.*

 * [4.5 years ago](https://github.com/microsoft/TypeScript/issues/47731#issuecomment-1030309558) **paul-marechal** explained understanding of the object type, provided examples illustrating the ergonomic issue with type narrowing, and suggested a potential change to improve ergonomics
 * [4.5 years ago](https://github.com/microsoft/TypeScript/issues/47731#issuecomment-1030457806) **fatcerberus** agreed that the behavior is less ergonomic, clarified that it followed type system rules and that fixing would require adding an ad-hoc rule, and noted that RyanCavanaugh had renamed the issue and agreed it's a bug
 * **RyanCavanaugh** added label `Domain: Control Flow`
 * [today](https://github.com/microsoft/TypeScript/issues/47731#issuecomment-5401724445) **nimeratus** said "I think the narrowing could be narrower than anything in the union, for example here it could be narrowed into [] no it seems like that could break a.push()"

### [PR microsoft/TypeScript#63248](https://github.com/microsoft/TypeScript/pull/63248) (Open, `For Backlog Bug`, `Voight-Kampff Anomaly`)

**Add lib types for JSON\.rawJSON, JSON\.isRawJSON, and reviver context**

*Add TypeScript declarations for ES2025’s JSON.rawJSON, JSON.isRawJSON, and JSON.parse reviver context*

 * [18 weeks ago](https://github.com/microsoft/TypeScript/pull/63248#issuecomment-4270116628) **RyanCavanaugh** said "@afurm future automated comments will result in a block; any automated activity we want to occur in this repo we will set up ourselves or already have"
 * [16 weeks ago](https://github.com/microsoft/TypeScript/pull/63248#issuecomment-4346296546) **MulverineX** said "@RyanCavanaugh the commandLineParser.ts has since been removed, is there a reason this PR is not proceeding?"
 * **RyanCavanaugh** added label `Voight-Kampff Anomaly`
 * [today](https://github.com/microsoft/TypeScript/pull/63248#issuecomment-5398875333) **MulverineX** said "Even if this is a bot this is still something that needs to get implemented, its pretty annoying to have to vendor these types in"

### [Issue microsoft/TypeScript#63749](https://github.com/microsoft/TypeScript/issues/63749) (Closed, `Bug`, `Fix Available`, **ahejlsberg**)

**\[7\.0\] Can't access field if it is protected in one constituent of an intersection \(type order dependent\)**

*TypeScript 7 erroneously prevents accessing a property protected in one part of an intersection type when constituent order differs.*

 * (yesterday) **ahejlsberg** added label `Fix Available`, set milestone to `TypeScript 7.1`, and removed from milestone `Backlog`
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript#63750](https://github.com/microsoft/TypeScript/issues/63750) (Closed, `Bug`)

**tsgo: parser nil\-pointer panic when a JSDoc @overload tags an anonymous default\-export function**

*tsgo’s parser crashes with a nil-pointer panic when a JSDoc @overload tags an anonymous default-export function*

 * **RyanCavanaugh** added to milestone `TypeScript 7.1`
 * **typescript-automation[bot]** added label `Fix Available`
 * **jakebailey** removed label `Fix Available`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#63761](https://github.com/microsoft/TypeScript/issues/63761) (Open, `Bug`, **weswigham**, **RyanCavanaugh**, **Copilot**)

**Panic "Diagnostic emitted without context" ts\-go in declaration emit for \`export default\` arrow/function expression with non\-portable inferred return type**

*Native TypeScript compiler panics on declaration emit for default-exported arrow functions with non-portable inferred return types*

 * created by **suyash-vyas**
 * [5 days ago](https://github.com/microsoft/TypeScript/issues/63761#issuecomment-5344526924) **suyash-vyas** said "Filed here rather than typescript-go since new activity there is locked for the repo move (https://github.com/microsoft/typescript-go/issues/4918). Happy to raise a fix :)"
 * (today) **RyanCavanaugh** added label `Bug`, set milestone to `TypeScript 7.1`, and assigned to **weswigham**, **Copilot**, **RyanCavanaugh**

### [PR microsoft/TypeScript#63765](https://github.com/microsoft/TypeScript/pull/63765) (Closed, `For Uncommitted Bug`, `dependencies`, `go`)

**Bump go\.mongodb\.org/mongo\-driver from 1\.17\.6 to 1\.17\.7 in /tools**

*Upgrade the MongoDB Go driver in /tools from v1.17.6 to v1.17.7 to include bug fixes and deprecation updates*

 * **dependabot[bot]** added label `go`
 * (5 days ago) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63765#issuecomment-5398495573) **dependabot[bot]** said "Looks like go.mongodb.org/mongo-driver is no longer a dependency, so this is no longer needed."
 * (today) **dependabot[bot]** closed the issue

### [PR microsoft/TypeScript#63766](https://github.com/microsoft/TypeScript/pull/63766) (Closed, `For Uncommitted Bug`, `dependencies`, `go`)

**Bump software\.sslmate\.com/src/go\-pkcs12 from 0\.7\.0 to 0\.7\.2 in /tools**

*Upgrades the go-pkcs12 dependency from version 0.7.0 to 0.7.2 in the tools directory.*

 * **dependabot[bot]** added label `go`
 * (5 days ago) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63766#issuecomment-5398696202) **jakebailey** said "Pointless but, ok"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#63767](https://github.com/microsoft/TypeScript/pull/63767) (Closed, `For Uncommitted Bug`, `dependencies`, `go`)

**Bump github\.com/aws/aws\-sdk\-go\-v2/service/s3 from 1\.96\.2 to 1\.97\.3 in /tools**

*Update AWS SDK Go v2 S3 service dependency in the tools directory from version 1.96.2 to 1.97.3.*

 * **dependabot[bot]** added label `go`
 * (5 days ago) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63767#issuecomment-5398496571) **dependabot[bot]** said "Looks like github.com/aws/aws-sdk-go-v2/service/s3 is no longer a dependency, so this is no longer needed."
 * (today) **dependabot[bot]** closed the issue

### [PR microsoft/TypeScript#63768](https://github.com/microsoft/TypeScript/pull/63768) (Closed, `For Uncommitted Bug`, `dependencies`, `go`)

**Bump github\.com/aws/aws\-sdk\-go\-v2/aws/protocol/eventstream from 1\.7\.5 to 1\.7\.8 in /tools**

*Upgrade aws-sdk-go-v2 eventstream protocol dependency from version 1.7.5 to 1.7.8 in tools*

 * (5 days ago) **dependabot[bot]** added labels `dependencies`, `go`
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63768#issuecomment-5398499624) **dependabot[bot]** said "Looks like github.com/aws/aws-sdk-go-v2/aws/protocol/eventstream is no longer a dependency, so this is no longer needed."
 * (today) **dependabot[bot]** closed the issue

### [Issue microsoft/TypeScript#63806](https://github.com/microsoft/TypeScript/issues/63806) (Open, `Needs Investigation`, **DanielRosenwasser**)

**Reimplement "find file references"**

*Reimplement find file references for JS/TS files by extending multi-project search beyond document positions.*

 * created by **DanielRosenwasser**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `Backlog`, and assigned to **DanielRosenwasser**

### [Issue microsoft/TypeScript#63858](https://github.com/microsoft/TypeScript/issues/63858) (Open, `Infrastructure`, `Needs Investigation`, **jakebailey**)

**Publish an official wasip1 \(WASI\) build artifact of tsgo**

*Publish an official Go WASI (wasip1) WebAssembly build artifact of tsgo alongside native binaries in releases.*

 * [1 month ago](https://github.com/microsoft/TypeScript/issues/63858#issuecomment-5351507568) **jakebailey** noted that editor use was useless because paths were exposed over the wire and pointed nowhere and error messages were misleading, and reported success providing `argv0` in some hosts but that not all hosts allow it
 * [1 month ago](https://github.com/microsoft/TypeScript/issues/63858#issuecomment-5351507588) **calvinrp** suggested embedding by default and adding a --lib-dir flag or environment variable for editor hosts
 * [1 month ago](https://github.com/microsoft/TypeScript/issues/63858#issuecomment-5351507607) **jakebailey** said "Not sure, I think it will also depend on what we do in the playground."
 * [today](https://github.com/microsoft/TypeScript/issues/63858#issuecomment-5400907269) **trobertson-graymatterllc** described that this approach could enable in-browser compilation, eliminate pre-compilation for development and live design, and support TypeScript as a first-tier language replacement for JavaScript

### [Issue microsoft/TypeScript#63860](https://github.com/microsoft/TypeScript/issues/63860) (Closed, `Needs Investigation`, **johnfav03**)

**\[ServerErrors\]\[TypeScript\] main vs **

*The TypeScript main branch error-delta pipeline tested 300 repositories, analyzing 198, reporting 10 interesting changes, 188 unchanged, and various failures.*

 * [5 weeks ago](https://github.com/microsoft/TypeScript/issues/63860#issuecomment-5351507895) **typescript-automation[bot]** reported server connection closed prematurely error with affected repos, old server result, last requests, and repro steps
 * (5 weeks ago) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **johnfav03**
 * (today) **johnfav03** closed the issue

### [PR microsoft/TypeScript#63932](https://github.com/microsoft/TypeScript/pull/63932) (Closed, `Author: Team`, `For Milestone Bug`, **ahejlsberg**)

**Fix \`getDeclarationModifierFlagsFromSymbolEx\` for synthetic properties**

*Fix accessibility checks so protected setters on synthetic properties in unions and intersections block writes.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/63932#issuecomment-5388679120) **typescript-automation[bot]** reported that the DT test results were ready and unchanged
 * [yesterday](https://github.com/microsoft/TypeScript/pull/63932#issuecomment-5388778630) **typescript-automation[bot]** reported that TypeScript compilation tests on the top 400 repos passed successfully comparing main to the PR merge
 * **ahejlsberg** added to milestone `TypeScript 7.1`
 * [today](https://github.com/microsoft/TypeScript/pull/63932#issuecomment-5399051706) **jakebailey** said "There's a suppressed comment but seems plausible?"
 * [today](https://github.com/microsoft/TypeScript/pull/63932#issuecomment-5399169703) **ahejlsberg** argued that speculating about abstract properties on union or intersection types was dubious because abstract members were implementation-specific and interfaces couldn't be abstract
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript#63937](https://github.com/microsoft/TypeScript/pull/63937) (Closed, `Author: Team`, `For Uncommitted Bug`, **weswigham**, **andrewbranch**)

**Add arbitrary API request batching**

*Add a batchRequests method and tick-based auto-batching with manual batchContext support for async API clients*

 * (4 days ago) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63937#issuecomment-5396890510) **dragomirtitian** suggested that the PR looked promising and asked for public exposure of batched requests, describing their internal yield*-based batching library
 * [today](https://github.com/microsoft/TypeScript/pull/63937#issuecomment-5399409788) **weswigham** described a follow-up plan to add an API output that maps async function input into generators and a sync API driver for batching

### [Issue microsoft/TypeScript#63946](https://github.com/microsoft/TypeScript/issues/63946) (Closed, `Needs Investigation`, **andrewbranch**)

**LSP Panic: overlay not found for changed file**

*LSP panics with ‘overlay not found for changed file’ when editing WSL files in PhpStorm after upgrading to tsserver v7.*

 * created by **uncaught**
 * **RyanCavanaugh** added label `Needs More Info`
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63946#issuecomment-5373176093) **RyanCavanaugh** said "We need either an LSP log, or some way to repro this in a supported editor (VS, VS Code)"
 * [later](https://github.com/microsoft/TypeScript/issues/63946#issuecomment-5411240428) **uncaught** provided a portion of idea.log from the IDE showing logs before a crash

### [Issue microsoft/TypeScript#63949](https://github.com/microsoft/TypeScript/issues/63949) (Open, `Bug`)

**\[7\.0 regression\] Type parameter default is ignored when the call sits inside a callback passed to a generic function**

*TypeScript 7.0 ignores default type parameters for calls inside callbacks passed to generic functions, causing type errors.*

 * created by **exoRift**
 * [today](https://github.com/microsoft/TypeScript/issues/63949#issuecomment-5400383233) **RyanCavanaugh** confirmed and provided a shorter reproduction snippet
 * (today) **RyanCavanaugh** added label `Bug`, set milestone to `Backlog`, and assigned to **Copilot**, **RyanCavanaugh**

### [PR microsoft/TypeScript#63952](https://github.com/microsoft/TypeScript/pull/63952) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Fix binder race**

*A concurrent data race occurs in Binder.setCommonJSModuleIndicator during call expression binding in TypeScript CI.*

 * (3 days ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/63952#issuecomment-5401639838) **jakebailey** described the problematic flow in TypeScript's project.go where BindSourceFiles was called too late
 * [today](https://github.com/microsoft/TypeScript/pull/63952#issuecomment-5401687855) **jakebailey** said "@typescript-bot perf test this"
 * [today](https://github.com/microsoft/TypeScript/pull/63952#issuecomment-5401688493) **typescript-automation[bot]** announced that perf test jobs had started and that the comment would be updated with build status
 * [today](https://github.com/microsoft/TypeScript/pull/63952#issuecomment-5401975340) **typescript-automation[bot]** posted the requested performance run results with a comparison report showing metrics for errors, symbols, types, memory usage, and allocations
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#63953](https://github.com/microsoft/TypeScript/pull/63953) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Update Go dependencies**

*Update Go module dependencies, including unused transitive ones, to satisfy Dependabot requirements.*

 * (3 days ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#63954](https://github.com/microsoft/TypeScript/pull/63954) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Replace Quill CLI with focused Mach\-O tool**

*Replace Quill CLI with a minimal Mach-O tool that extracts only entitlement data for security alerts and dependency counts.*

 * (3 days ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/63954#issuecomment-5378114581) **jakebailey** said "I missed your approval, I should have just left it the way it was"
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#63959](https://github.com/microsoft/TypeScript/issues/63959) (Open, `Docs`)

**The new \`\-\-lsp\` flag is not mentioned in \`tsc \-\-help\`'s output**

*The new --lsp flag isn’t listed in tsc --help or tsc --help --all output, making it hard to find.*

 * [today](https://github.com/microsoft/TypeScript/issues/63959#issuecomment-5391927215) **frou** criticized calling the omission patronising and questioned the assumption that all normal users use VSCode
 * [today](https://github.com/microsoft/TypeScript/issues/63959#issuecomment-5391964867) **jakebailey** asked for the context in which the flag documentation was missing
 * [today](https://github.com/microsoft/TypeScript/issues/63959#issuecomment-5392026205) **frou** explained that they installed TypeScript 7 and tweaked their Emacs config to use the new native LSP instead of typescript-language-server for TypeScript files
 * (today) **RyanCavanaugh** added label `Docs`, and set milestone to `Backlog`

### [PR microsoft/TypeScript#63961](https://github.com/microsoft/TypeScript/pull/63961) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Use pinned gzip for localization generation**

*Generate localization files using a pinned klauspost/compress gzip implementation to ensure consistent outputs across Go toolchains.*

 * (2 days ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63961#issuecomment-5397796900) **jakebailey** said "Actually, on second thought, my followup commit is a problem because it means every added or removed diagnostic changes every gz file. I'll undo that for now"
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#63962](https://github.com/microsoft/TypeScript/issues/63962) (Open, `Bug`)

**Crash: class\-level decorator on an anonymous class panics during ES decorator emit**

*Using a class decorator on an unnamed class triggers a TypeScript compiler panic during ES decorator emission*

 * created by **daniellockyer**
 * (today) **RyanCavanaugh** added label `Bug`, and set milestone to `TypeScript 7.1`

### [Issue microsoft/TypeScript#63963](https://github.com/microsoft/TypeScript/issues/63963) (Open, `Bug`)

**Crash: malformed object destructuring assignment panics in class fields transform**

*TypeScript compiler panics when processing a malformed object destructuring assignment in class fields transform*

 * created by **daniellockyer**
 * (today) **RyanCavanaugh** added label `Bug`, and set milestone to `TypeScript 7.1`

### [Issue microsoft/TypeScript#63964](https://github.com/microsoft/TypeScript/issues/63964) (Open, `Bug`)

**Crash: malformed \`super\` destructuring in a decorated class static block panics**

*The Go-based TypeScript compiler panics on malformed super destructuring in a decorated class static block*

 * created by **daniellockyer**
 * (today) **RyanCavanaugh** added label `Bug`, and set milestone to `TypeScript 7.1`

### [Issue microsoft/TypeScript#63965](https://github.com/microsoft/TypeScript/issues/63965) (Open, `Bug`)

**Crash: optional chain \+ tagged template panics the optional\-chain transform**

*Combining optional chaining with a tagged template literal (e?.``()) triggers a compiler panic due to unhandled KindTaggedTemplateExpression.*

 * created by **daniellockyer**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63965#issuecomment-5386604706) **bigboateng** put up a fix in #63968, described the root cause in the optional-chain transform, and detailed how the fix handles tagged templates
 * (today) **RyanCavanaugh** added label `Bug`, and set milestone to `TypeScript 7.1`

### [Issue microsoft/TypeScript#63966](https://github.com/microsoft/TypeScript/issues/63966) (Open, `Possible Improvement`)

**Performance regression for declaration emit of an oversized inferred type**

*TypeScript 7’s declaration emit for nested inferred types now uses significantly more memory and time and still produces TS7056 errors*

 * [yesterday](https://github.com/microsoft/TypeScript/issues/63966#issuecomment-5385271015) **yunasora** requested assignment to investigate and fix the declaration emit performance regression with tests and benchmarks
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63966#issuecomment-5391700327) **jakebailey** said "Did you have an actual project which hit this, or did you just find this with an LLM looking at the code?"
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63966#issuecomment-5391743046) **daniellockyer** explained that they found the repro via an LLM while improving memory usage of tsc/tsgo and noted they had other bugs tied to private projects for which they needed minimal public repros
 * (today) **RyanCavanaugh** added label `Possible Improvement`, and set milestone to `Backlog`

### [PR microsoft/TypeScript#63967](https://github.com/microsoft/TypeScript/pull/63967) (Closed, `For Milestone Bug`)

**fix: panic on nil point on name check**

*Add a nil name check in checkNonIdentifierName to prevent nil pointer panics during name validation.*

 * created by **Dansyuqri**
 * **typescript-automation[bot]** added label `For Milestone Bug`
 * [yesterday](https://github.com/microsoft/TypeScript/pull/63967#issuecomment-5385591182) **Dansyuqri** quoted the Contributor License Agreement and the instructions for agreeing via the microsoft-github-policy-service
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#63969](https://github.com/microsoft/TypeScript/pull/63969) (Open, `For Uncommitted Bug`)

**Avoid cloning cached declaration types after truncation**

*Prevent cloning of cached declaration type nodes after truncation threshold is reached, drastically improving compile performance.*

 * (yesterday) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [yesterday](https://github.com/microsoft/TypeScript/pull/63969#issuecomment-5386818021) **butros10games** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript/pull/63969#issuecomment-5401140601) **butros10games** moved the truncation check to the start of visitAndTransformType, updated test expectations, and confirmed the full test suite passed

### [Issue microsoft/TypeScript#63970](https://github.com/microsoft/TypeScript/issues/63970) (Open, `Suggestion`, `Awaiting More Feedback`)

**Inconsistent typing of endless generators between functions and lambdas**

*TypeScript infers void return for named infinite generators but never for generator lambdas, causing incompatible assignment errors.*

 * created by **jacekkopecky**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63970#issuecomment-5387542405) **Andarist** explained that the behavior was deliberate for backwards compatibility and linked to the TypeScript rules for auto-inferring never return types
 * (today) **RyanCavanaugh** added labels `Suggestion`, `Awaiting More Feedback`

### [Issue microsoft/TypeScript#63975](https://github.com/microsoft/TypeScript/issues/63975) (Open, `Docs`)

**compilerOptions\.plugins is not inherited through tsconfig "extends"**

*compilerOptions.plugins defined in a base tsconfig.json are not inherited when using extends due to missing merge logic.*

 * created by **vickvu**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63975#issuecomment-5391680191) **jakebailey** said "We don't even support plugins?"
 * [today](https://github.com/microsoft/TypeScript/issues/63975#issuecomment-5391942569) **vickvu** asked if there were other unsupported features in TS 7.x and whether watch and watchOptions were still supported
 * (today) **RyanCavanaugh** added label `Docs`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#63976](https://github.com/microsoft/TypeScript/issues/63976) (Closed)

**Excessive string allocations in \`projectReferenceDtsFakingVfs\`**

*The directoryExistsIfProjectReferenceDeclDir method in projectReferenceDtsFakingVfs excessively allocates ephemeral strings, causing significant memory overhead.*

 * created by **auvred**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#63977](https://github.com/microsoft/TypeScript/pull/63977) (Closed, `For Uncommitted Bug`)

**Avoid allocations when checking project reference declaration directories**

*Replace allocation-heavy project reference directory checks with ContainsPath to eliminate allocations and improve textDocument/references performance.*

 * created by **auvred**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#63979](https://github.com/microsoft/TypeScript/issues/63979) (Closed, `Out of Scope`, `Docs`)

**Official guidelines to build complex types**

*Proposal to add official TypeScript guidelines detailing supported tips, patterns, and pitfalls for constructing complex type definitions.*

 * created by **denis-migdal**
 * [today](https://github.com/microsoft/TypeScript/issues/63979#issuecomment-5399758066) **DanielRosenwasser** explained that the website’s learning materials focus on common day-to-day patterns and defer advanced recipes to Q&A sites to avoid overwhelming learners
 * (today) **DanielRosenwasser** added labels `Out of Scope`, `Docs`
 * [today](https://github.com/microsoft/TypeScript/issues/63979#issuecomment-5401226810) **denis-migdal** asked what the officially encouraged patterns were and proposed creating an index with guidance on pattern support status
 * [today](https://github.com/microsoft/TypeScript/issues/63979#issuecomment-5401336118) **snarbles2** suggested hosting a community-maintained resource of advanced techniques and linking it from official docs to enable contributions and track version-specific issues
 * [today](https://github.com/microsoft/TypeScript/issues/63979#issuecomment-5405840236) **denis-migdal** asked whether a website already existed and what requirements TS would have regarding repo ownership, external links, issue triage notifications, and promotion

### [PR microsoft/TypeScript#63980](https://github.com/microsoft/TypeScript/pull/63980) (Open, `For Backlog Bug`)

**Re\-order Array\#reduce and Array\#reduceRight overloads in lib\.es5\.d\.ts**

*Prioritize generic Array#reduce and reduceRight overloads before same-type overloads in lib.es5.d.ts to improve type inference*

 * created by **sundeep8967**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63980#issuecomment-5400942975) **sundeep8967** said "@microsoft-github-policy-service agree"

### [Issue microsoft/TypeScript#63981](https://github.com/microsoft/TypeScript/issues/63981) (Closed, `Bug`, `Fix Available`, **ahejlsberg**)

**\`TS2454\` false positive when a callback mutates an outer \`let\` and returns the enclosing function's parameter**

*TypeScript 7 falsely reports TS2454 when a closure compound-assigns an outer let and returns its parameter prior to that let’s initialization.*

 * created by **bent0b0x**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **ahejlsberg**

### [Issue microsoft/TypeScript#63982](https://github.com/microsoft/TypeScript/issues/63982) (Closed, `Working as Intended`)

**Regression, TS2304: @template\-tag no longer works with @type\-tag in JSDoc**

*Generic JSDoc functions using @template and @type tags now trigger TS2304 errors after upgrading to TypeScript 7.0.*

 * created by **Teascade**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **sandersn**
 * [later](https://github.com/microsoft/TypeScript/issues/63982#issuecomment-5408754492) **Andarist** highlighted that TypeScript 6 leaked a type parameter, noted that TypeScript 7 behavior was better, and mentioned that whether the two tags should be a valid combination is a separate question
 * [later](https://github.com/microsoft/TypeScript/issues/63982#issuecomment-5412184965) **ahejlsberg** explained that the @template tag shouldn't affect a @type tag and provided the correct example syntax for the id function
 * (later) **ahejlsberg** added label `Working as Intended`, removed label `Needs Investigation`, and unassigned **sandersn**

### [PR microsoft/TypeScript#63983](https://github.com/microsoft/TypeScript/pull/63983) (Closed)

**Speed up CI with more jobs, less work**

*Propose parallelizing CI tests and disabling coverage in merge queues to reduce merge queue time by 40%.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#63984](https://github.com/microsoft/TypeScript/pull/63984) (Closed, **ahejlsberg**)

**Fix TS2454 false positive for closed\-over mutable variables**

*Removing the premature early return in ensureAssignmentsMarked fixes false TS2454 errors for top-level let variables captured by closures.*

 * created by **mohit-nayak**
 * [today](https://github.com/microsoft/TypeScript/pull/63984#issuecomment-5399185261) **mohit-nayak** said "@microsoft-github-policy-service agree"
 * **RyanCavanaugh** assigned to **ahejlsberg**

### [PR microsoft/TypeScript#63985](https://github.com/microsoft/TypeScript/pull/63985) (Closed)

**Fix extension launching**

*Updates launch settings, renames the extension, corrects executable resolution, and removes unused code to restore extension launching.*

 * created by **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript/pull/63985#issuecomment-5399993996) **jakebailey** said "Ah, CI is mad because we are using -w with a name not a path"
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript#63986](https://github.com/microsoft/TypeScript/pull/63986) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Don't reuse emit resolvers cross\-file**

*Reusing emit resolvers across files leads to race conditions that alter declaration emit outputs.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/63986#issuecomment-5400339804) **DanielRosenwasser** asked whether newEmitResolver allocated two closures per call and suggested running isValueAliasDeclaration in a loop and lazily initializing aliasMarkingVisitor
 * [today](https://github.com/microsoft/TypeScript/pull/63986#issuecomment-5400350577) **DanielRosenwasser** said "Also, is it worth running a perf test on here just to be safe?"
 * [today](https://github.com/microsoft/TypeScript/pull/63986#issuecomment-5400888385) **jakebailey** said "Another hit on main: https://github.com/microsoft/TypeScript/actions/runs/32760252400/job/97537150724"
 * [today](https://github.com/microsoft/TypeScript/pull/63986#issuecomment-5400897261) **jakebailey** acknowledged that it allocated two closures per call, clarified it was only once per file and not a hotspot, and suggested refactoring

### [PR microsoft/TypeScript#63987](https://github.com/microsoft/TypeScript/pull/63987) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Redo localization for onboarding**

*Reorganize localization files by dropping .json.gz and reintroducing loc directory; add VS Code localization; use build tag to exclude localization.*

 * created by **jakebailey**

### [PR microsoft/TypeScript#63988](https://github.com/microsoft/TypeScript/pull/63988) (Closed, **RyanCavanaugh**, **Copilot**)

**\[WIP\] Fix type parameter default ignored in callback**

*Implement a compiler fix and regression test for TypeScript’s callback inference path that ignores default type parameters.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**

### [PR microsoft/TypeScript#63989](https://github.com/microsoft/TypeScript/pull/63989) (Open, `For Uncommitted Bug`, **RyanCavanaugh**, **Copilot**)

**Fix panic in declaration emit for \`export default\` arrow/function expression with unnameable inferred return type**

*Default-exported arrow or function expressions with unnameable inferred return types cause a compiler panic due to missing diagnostic context.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript/pull/63989#issuecomment-5401122264) **Copilot** implemented the change by moving the diagnostic context assignment and PushErrorFallbackNode above the unwrapped assignment, sharing them across all branches, and adding a PopErrorFallbackNode before each return

### [Issue microsoft/TypeScript#63990](https://github.com/microsoft/TypeScript/issues/63990) (Open, `Bug`)

**Generic recursive function infers incorrect return type**

*TypeScript’s generic recursive function infers return type T instead of the correct union T|number when recursing with numbers.*

 * created by **kwshi**
 * [today](https://github.com/microsoft/TypeScript/issues/63990#issuecomment-5402928942) **RyanCavanaugh** said "Yeah, this is a bug where we think we can sideline this as never, but that logic shouldn't be used when the function has a generic return type."
 * (today) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`

### [PR microsoft/TypeScript#63991](https://github.com/microsoft/TypeScript/pull/63991) (Closed)

**Update and pin GHA actions**

*Update and pin GitHub Actions dependencies not handled by Dependabot.*

 * created by **jakebailey**

### [PR microsoft/TypeScript#63992](https://github.com/microsoft/TypeScript/pull/63992) (Closed)

**Update publish naming**

*Standardize publish naming conventions in preparation for creating pipelines.*

 * created by **jakebailey**

### [PR microsoft/TypeScript#63993](https://github.com/microsoft/TypeScript/pull/63993) (Closed)

**Make bundled/lib the canonical lib file source**

*Use bundled/lib as the primary source for library files, eliminate file generation, and update the DOM lib generator migration script.*

 * created by **jakebailey**

### [PR microsoft/TypeScript#63994](https://github.com/microsoft/TypeScript/pull/63994) (Closed)

**docs\(readme\): update blog link to devblogs and use relative CONTRIBUTING\.md links**

*Update README to use the new devblogs.microsoft.com/typescript link and relative CONTRIBUTING.md references*

 * created by **loulanyue**

### [Issue microsoft/TypeScript#63995](https://github.com/microsoft/TypeScript/issues/63995) (Closed, `Bug`)

**Leading Unicode escapes and surrogate pair escapes are not parsed in RegExp group names**

*Leading Unicode, extended Unicode, and surrogate pair escapes in regex group names are not parsed correctly, causing errors.*

 * created by **graphemecluster**

### [PR microsoft/TypeScript#63996](https://github.com/microsoft/TypeScript/pull/63996) (Closed, `For Backlog Bug`)

**Fix scanning issues related to Unicode escapes in RegExp group names and refactor identifier scanning**

*Refactor identifier scanning to correctly parse and normalize Unicode escapes and surrogate pairs in RegExp group names, preventing TS1514 errors.*

 * created by **graphemecluster**
 * [later](https://github.com/microsoft/TypeScript/pull/63996#issuecomment-5407137733) **graphemecluster** said "All checks passed, so I am leaving the diff files here. If they are to be removed, feel free to do so on my behalf."
 * [later](https://github.com/microsoft/TypeScript/pull/63996#issuecomment-5412038641) **jakebailey** said "We definitely don't want the diffs, we just don't have anything that checks for extra baselines (my mistake for not retaining that)"

### [Issue microsoft/TypeScript#63997](https://github.com/microsoft/TypeScript/issues/63997) (Closed, `Needs Investigation`, **andrewbranch**)

**Path mappings parsing uses too much memory for projects with many references and paths**

*TypeScript’s path mapping parser allocates ParsedPatterns for every module resolution, causing excessive memory use in large projects with numerous paths.*

 * created by **auvred**

### [PR microsoft/TypeScript#63998](https://github.com/microsoft/TypeScript/pull/63998) (Closed)

**Reduce path\-mapping cache memory usage for projects with many paths**

*Move immutable parsed path-mapping patterns into a shared Resolver cache to reduce memory usage and improve module resolution performance.*

 * created by **auvred**

### [PR microsoft/TypeScript#63999](https://github.com/microsoft/TypeScript/pull/63999) (Open, `For Backlog Bug`)

**Don't ignore all generic self tail calls when collecting the return type of a function**

*Include recursive generic tail calls with incompatible arguments in return type inference while ignoring only calls with explicit type arguments.*

 * created by **Andarist**

### [PR microsoft/TypeScript#64000](https://github.com/microsoft/TypeScript/pull/64000) (Open, `For Uncommitted Bug`)

**Expose Checker\.getAwaitedType on the unstable API**

*Expose getAwaitedType on the TypeScript unstable API to allow consumers to recursively obtain the resolved type of awaited expressions.*

 * created by **baptistejamin**
 * [later](https://github.com/microsoft/TypeScript/pull/64000#issuecomment-5410558963) **baptistejamin** agreed with microsoft-github-policy-service

### [PR microsoft/TypeScript#64001](https://github.com/microsoft/TypeScript/pull/64001) (Open, `For Uncommitted Bug`)

**Expose Checker\.getTypeOfPropertyOfType on the unstable API**

*Expose Checker.getTypeOfPropertyOfType through the TypeScript unstable API to return a named property’s type or undefined.*

 * created by **baptistejamin**

### [PR microsoft/TypeScript#64002](https://github.com/microsoft/TypeScript/pull/64002) (Open, `For Uncommitted Bug`)

**Expose Checker\.getIndexInfoOfType on the unstable API**

*Expose Checker.getIndexInfoOfType in TypeScript’s unstable API to mirror the Go checker and enable typescript-eslint’s isTypeReadonly functionality.*

 * created by **baptistejamin**

### [Issue microsoft/TypeScript#64003](https://github.com/microsoft/TypeScript/issues/64003) (Closed)

**JSDoc @enum does not create a type \(TS2749 on \.d\.ts consumers\)**

*JSDoc @enum on a constant object doesn't generate a type in emitted .d.ts files, leading to TS2749 errors for consumers.*

 * created by **bun-unsafe**
 * [later](https://github.com/microsoft/TypeScript/issues/64003#issuecomment-5412090105) **jakebailey** said "All of these were intentionally removed and have alternatives: https://github.com/microsoft/TypeScript/blob/main/tsc/CHANGES.md"
 * [later](https://github.com/microsoft/TypeScript/issues/64003#issuecomment-5412351169) **bun-unsafe** described encountering a regression in TypeScript 7’s declaration output for a JSDoc enum fixture, noted using Copilot to draft the patch, and apologized after realizing the change was intentional per CHANGES.md
 * (later) **bun-unsafe** closed the issue

### [PR microsoft/TypeScript#64004](https://github.com/microsoft/TypeScript/pull/64004) (Closed)

**Fix JSDoc @enum so the tagged name is a type as well as a value**

*Adjust JSDoc @enum on const objects to emit both a type alias and the corresponding value object.*

 * created by **bun-unsafe**
 * [later](https://github.com/microsoft/TypeScript/pull/64004#issuecomment-5411761022) **bun-unsafe** said "@microsoft-github-policy-service agree"
 * [later](https://github.com/microsoft/TypeScript/pull/64004#issuecomment-5412080191) **jakebailey** pointed out that everything being added back was intentionally removed and linked to the TypeScript CHANGES.md
 * [later](https://github.com/microsoft/TypeScript/pull/64004#issuecomment-5412175900) **bun-unsafe** acknowledged that @enum and Closure function types were intentionally removed in Corsa, said they would close the PR, and apologized
 * (later) **bun-unsafe** closed the issue
 * [later](https://github.com/microsoft/TypeScript/pull/64004#issuecomment-5412245473) **jakebailey** said "Why did you choose to work on this? Does this personally affect you?"
 * [later](https://github.com/microsoft/TypeScript/pull/64004#issuecomment-5412282465) **bun-unsafe** acknowledged a perceived regression in enum declaration emit but realized it was intentional and apologized for the noise

### [Issue microsoft/TypeScript#64005](https://github.com/microsoft/TypeScript/issues/64005) (Closed)

**JSDoc @enum does not create a type \(TS2749 on \.d\.ts consumers\)**

*JSDoc @enum on a constant object doesn't generate a type in emitted .d.ts files, leading to TS2749 errors for consumers.*

 * created by **bun-unsafe**
 * [later](https://github.com/microsoft/TypeScript/issues/64005#issuecomment-5411650813) **bun-unsafe** said "Duplicate of #64003."
 * (later) **bun-unsafe** closed the issue

### [Issue microsoft/TypeScript#64006](https://github.com/microsoft/TypeScript/issues/64006) (Closed, `Working as Intended`)

**Excess property checking lost through a generic mapped\-type parameter \(regression in 6\.0\)**

*TypeScript 6.0 regression causes generic mapped types to bypass excess property checks for nested object literals containing a valid key.*

 * created by **BrianP8701**

