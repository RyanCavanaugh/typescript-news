# Report for 2026-11-13 (Friday, November 13th, 2026)

11 different users commented on 76 different issues.

## Recommended Actions

 * Response Recommended
    * @insilications asked whether there was a plan in [microsoft/TypeScript#16665](https://github.com/microsoft/TypeScript/issues/16665#issuecomment-6878077603)
    * @alshdavid disputed the duplicate designation and explained that the referenced ticket was different in [microsoft/TypeScript#65355](https://github.com/microsoft/TypeScript/issues/65355#issuecomment-6863152676)

## Activity Summary

### [Issue microsoft/TypeScript#16665](https://github.com/microsoft/TypeScript/issues/16665) (Open, `Suggestion`, `Awaiting More Feedback`, `VS Code Tracked`, `Domain: LS: Signature Help`, `Domain: LS: Quick Info`)

**Include Default Parameter Values in Signature Help **

*Signature help should display default values for optional parameters, such as showing `x = 10` when invoking `foo`.*

 * [1 year ago](https://github.com/microsoft/TypeScript/issues/16665#issuecomment-3402358452) **meduzen** shared screenshots demonstrating the function definition, autocomplete signature, and parameter flyout behavior described by @alystair
 * [1 year ago](https://github.com/microsoft/TypeScript/issues/16665#issuecomment-3403004341) **alystair** said "@RyanCavanaugh see updates above, hopefully this simplifies things significantly on your end."
 * [45 weeks ago](https://github.com/microsoft/TypeScript/issues/16665#issuecomment-3702408931) **stevenvachon** said "Flow might've been the better choice."
 * [later](https://github.com/microsoft/TypeScript/issues/16665#issuecomment-6878077603) **insilications** asked whether there was a plan

### [Issue microsoft/TypeScript#63856](https://github.com/microsoft/TypeScript/issues/63856) (Closed, `Needs Investigation`, **jakebailey**)

**tsc is not resposive to \`ctrl\-c\`**

*tsc ignores Ctrl-C during builds because signal cancellation is not propagated throughout the build, prompting a fix or removal of custom handlers.*

 * [17 weeks ago](https://github.com/microsoft/TypeScript/issues/63856#issuecomment-5351507245) **anthonyshew** provided additional reproduction details showing that `pnpm run dev:ts` required three interrupts to exit while directly invoking `pnpm exec tsc` exited after one
 * **RyanCavanaugh** added to milestone `TypeScript 7.1`
 * [9 weeks ago](https://github.com/microsoft/TypeScript/issues/63856#issuecomment-5591307178) **rafaelnajman** confirmed the signal-handling issue on TypeScript 7.0.2 and a 7.1.0 development build on macOS 15 arm64, reporting that SIGINT and SIGTERM incorrectly exited successfully after completing compilation and that parallel runners leaked compiler processes; provided a self-contained reproduction in #64196 and noted that issue was being closed in favor of this one
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64085](https://github.com/microsoft/TypeScript/pull/64085) (Closed, `Author: Team`, `For Milestone Bug`, **jakebailey**)

**Handle tsc watch and profiling signals**

*Support handling profiling and watch-mode signals in the TypeScript compiler (tsc).*

 * (10 weeks ago) **typescript-automation[bot]** added labels `Author: Team`, `For Milestone Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#64300](https://github.com/microsoft/TypeScript/issues/64300) (Closed, `Needs Investigation`, **jakebailey**)

**\[TS7 LSP\] Panic on document URI "file://" \(empty path\): vfs: path "tsconfig\.json" is not absolute**

*TS7’s native LSP server panics when processing a document with the URI `file://` because it derives a non-absolute `tsconfig.json` path.*

 * [8 weeks ago](https://github.com/microsoft/TypeScript/issues/64300#issuecomment-5707036878) **chenxin-yan** explained that Neovim's `vim.lsp.enable()` auto-attached the TypeScript LSP to matching buffers, including unnamed buffers with an empty `buftype`, which triggered the error
 * (6 weeks ago) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64396](https://github.com/microsoft/TypeScript/pull/64396) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Normalize document URIs during decoding**

*Normalize empty or relative document URIs during decoding using vscode-uri-compatible rules to prevent malformed filenames.*

 * (7 weeks ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64900](https://github.com/microsoft/TypeScript/pull/64900) (Open, `For Backlog Bug`)

**Fix unused renaming detection in function types**

*Correct unused-renaming detection so type-only references in generic function types do not suppress diagnostics for unused destructured value bindings.*

 * (3 weeks ago) **typescript-automation[bot]** added labels `For Backlog Bug`, `For Backlog Bug`
 * [3 weeks ago](https://github.com/microsoft/TypeScript/pull/64900#issuecomment-6317648836) **wickstudio** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript/pull/64900#issuecomment-6862090261) **jakebailey** suggested splitting the changes into separate commits for the failing test and baseline, followed by the fix and updated baseline

### [PR microsoft/TypeScript#65064](https://github.com/microsoft/TypeScript/pull/65064) (Open, `Author: Team`, `For Milestone Bug`, `For Backlog Bug`, **jakebailey**)

**\[experiment\] fully order independent type checking**

*Proposes making type checking fully order-independent, with randomized ordering tests and extensive fixes for cache, traversal, and identifier-dependent behavior.*

 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6853673975) **typescript-automation[bot]** reported that the DT tests completed and exposed a branch-only TypeScript compile error in d3-selection involving incompatible TransitionLike element types
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6853807663) **typescript-automation[bot]** provided the requested performance-run results, including compiler comparison metrics showing increased symbols and memory usage
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6856589252) **typescript-automation[bot]** reported results from comparing the baseline and pull request TypeScript compiler runs across the top 1,000 repositories and flagged unexpected build changes for investigation
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6858331798) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6858334734) **typescript-automation[bot]** reported that the performance test job started and linked to its build results
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6859215173) **typescript-automation[bot]** reported the requested performance-run results, including increased symbols and memory usage in the compiler-unions benchmark
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6871639942) **jakebailey** requested several TypeScript bot tests, including DT, user, top-1000, and performance tests
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6871640974) **typescript-automation[bot]** said "Hey @jakebailey, this PR is in an unmergable state, so is missing a merge commit to run against; please resolve conflicts and try again."
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6872168280) **jakebailey** requested several TypeScript bot tests, including DT, user, top-1000, and performance tests
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6872169318) **typescript-automation[bot]** reported that automated jobs started, with results available for `run dt`, `user test this`, and `perf test this faster`, while `test top1000` remained in progress
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6872486023) **typescript-automation[bot]** reported that the DT tests completed and exposed a branch-only TypeScript compile error in d3-selection involving incompatible TransitionLike element types
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6872500310) **typescript-automation[bot]** reported new TypeScript test errors in `SchemaAST.ts` when comparing the baseline and PR results, and asked maintainers to investigate
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6873157202) **typescript-automation[bot]** said "@jakebailey, the perf run you requested failed. You can check the log here."

### [PR microsoft/TypeScript#65288](https://github.com/microsoft/TypeScript/pull/65288) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Reject visitor removal of required children**

*Ensure visitors cannot remove required child nodes while preserving valid parser-recovered, optional, and elided children.*

 * [1 week ago](https://github.com/microsoft/TypeScript/pull/65288#issuecomment-6613622432) **jakebailey** said "@typescript-bot perf test this faster"
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/65288#issuecomment-6613624250) **typescript-automation[bot]** reported that the performance test job started and linked to its results
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/65288#issuecomment-6614912562) **typescript-automation[bot]** reported that the requested performance run results were available and included compiler benchmark comparison data
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#65292](https://github.com/microsoft/TypeScript/pull/65292) (Open, `Author: Team`, `For Milestone Bug`, `For Backlog Bug`, **jakebailey**)

**Various order dependence fixes**

*Fixes order-dependent behavior by replacing opportunistic cache reads and ID-based ordering with deterministic, content-based ordering and caching.*

 * (1 week ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **typescript-automation[bot]** added labels `For Backlog Bug`, `For Milestone Bug`, and removed label `For Uncommitted Bug`

### [PR microsoft/TypeScript#65293](https://github.com/microsoft/TypeScript/pull/65293) (Open, `Author: Team`, `For Milestone Bug`, `For Backlog Bug`, **jakebailey**)

**Make checker behavior order independent**

*Refactor checker state and cycle handling to make diagnostics, variance calculations, and instantiation limits deterministic regardless of query or processing order.*

 * (1 week ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/65293#issuecomment-6616507155) **Copilot** reported that a custom repository setup step failed during the Copilot code review run and directed maintainers to inspect the workflow failure and configuration
 * (today) **typescript-automation[bot]** added labels `For Backlog Bug`, `For Milestone Bug`, and removed labels `For Uncommitted Bug`, `For Milestone Bug`

### [Issue microsoft/TypeScript#65355](https://github.com/microsoft/TypeScript/issues/65355) (Open, `Suggestion`)

**Remote declaration resolution**

*Request support for resolving remote TypeScript declaration files in browser-based, bundler-free ESM projects without installing runtime dependencies.*

 * [4 days ago](https://github.com/microsoft/TypeScript/issues/65355#issuecomment-6751850958) **alshdavid** clarified that their ticket concerned modeling browser import maps and fetching type definitions from remote URLs without requiring npm installation, unlike the referenced ticket that used local node_modules types
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/65355#issuecomment-6811360610) **typescript-automation[bot]** said "This issue has been marked as "Duplicate" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (2 days ago) **typescript-automation[bot]** closed the issue
 * [today](https://github.com/microsoft/TypeScript/issues/65355#issuecomment-6863152676) **alshdavid** said "It's is not a duplicate. That other ticket is similar but different"

### [Issue microsoft/TypeScript#65415](https://github.com/microsoft/TypeScript/issues/65415) (Open, `Bug`)

**\`jsx: react\-jsxdev\` passes \`this\` to \`jsxDEV\` before \`super\(\)\` returns**

*The `react-jsxdev` transform passes `this` to `jsxDEV` before derived constructors call `super()`, unlike the correct `react-jsx` transform.*

 * created by **trackoor**
 * (3 days ago) **RyanCavanaugh** added label `Bug`, and set milestone to `Dormant`
 * [today](https://github.com/microsoft/TypeScript/issues/65415#issuecomment-6858636266) **yamaankhan20** said "Hi, I'd like to work on this issue. I'll investigate how the JSX transformer emits the self argument for jsxDEV inside super() calls, and add regression tests alongside the fix."

### [Issue microsoft/TypeScript#65445](https://github.com/microsoft/TypeScript/issues/65445) (Closed)

**7\.1 regression: TS5115 for import\("cloudflare:workers"\) with @cloudflare/workers\-types**

*TypeScript 7.1 introduces TS5115 infinite-instantiation errors for dynamic `cloudflare:workers` imports using `@cloudflare/workers-types`.*

 * created by **alon-gb**
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/65445#issuecomment-6801655226) **maschwenk** bisected the regression to microsoft/typescript-go#4687, identified the added anonymous-symbol declarations assignment as the cause, and provided a minimal reproduction and technical explanation involving recursive Provider<any> inference and TS2589/TS5115.
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#65462](https://github.com/microsoft/TypeScript/issues/65462) (Closed)

**Content mappers: report a mapper's diagnostics without stopping type checking**

*Allow content mapper diagnostics to be reported as semantic errors without suppressing unrelated TypeScript type-checking diagnostics.*

 * created by **colinhacks**
 * [today](https://github.com/microsoft/TypeScript/issues/65462#issuecomment-6866042277) **andrewbranch** clarified that the behavior was intentional and documented, explained that content mappers avoid semantic checks for performance, and linked issue #45886 as the broader solution
 * [today](https://github.com/microsoft/TypeScript/issues/65462#issuecomment-6874008531) **colinhacks** said "Understood, thanks 👍"
 * (today) **colinhacks** closed the issue

### [PR microsoft/TypeScript#65463](https://github.com/microsoft/TypeScript/pull/65463) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Preserve formatter alignment across tabs and enum decorators**

*Preserve formatter alignment by handling mixed whitespace tab stops and matching enum keywords after decorators.*

 * (yesterday) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#65465](https://github.com/microsoft/TypeScript/pull/65465) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Avoid slicing truncated source map charset values**

*Prevent panics when truncated data URLs contain incomplete UTF-8 charset prefixes while preserving case-insensitive matching and fallback behavior.*

 * (yesterday) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#65466](https://github.com/microsoft/TypeScript/pull/65466) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Restore the enclosing variance diagnostic context**

*Restore the enclosing variance diagnostic context so variance errors retain their surrounding diagnostic information.*

 * (yesterday) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#65468](https://github.com/microsoft/TypeScript/pull/65468) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Route typed emit paths to per\-file trace threads**

*Fix typed emit paths so tracing routes each path to its corresponding per-file trace thread instead of using `any`.*

 * (yesterday) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#65469](https://github.com/microsoft/TypeScript/pull/65469) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Remove an random accessor from object literal grammar checking**

*Remove the unexplained random accessor from object literal grammar checking.*

 * (yesterday) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#65470](https://github.com/microsoft/TypeScript/pull/65470) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Fix TODO in psuedochecker's typeNodeCouldReferToUndefined**

*Implement the pseudochecker’s typeNodeCouldReferToUndefined TODO and validate its behavior with a test.*

 * (yesterday) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#65471](https://github.com/microsoft/TypeScript/pull/65471) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Return freshly cached post\-super flow results**

*Add the missing return statement so post-super flow results are returned when freshly cached.*

 * (yesterday) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#65472](https://github.com/microsoft/TypeScript/pull/65472) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Fix getAdjustedLocationForDeclaration oops**

*Fix getAdjustedLocationForDeclaration to correctly use its provided parameter.*

 * (yesterday) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#65473](https://github.com/microsoft/TypeScript/pull/65473) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Suggest the ES2015 library for missing Symbol references**

*Update missing Symbol references to suggest the appropriate ES2015 library, likely correcting an accidental find-and-replace error.*

 * (yesterday) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#65474](https://github.com/microsoft/TypeScript/pull/65474) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Fix numeric falsiness and circular config parsing**

*Fix bugs involving numeric falsiness and circular configuration parsing.*

 * (yesterday) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#65476](https://github.com/microsoft/TypeScript/pull/65476) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Restore fourslash marker selection and native JS test discovery**

*Fix fourslash marker iteration and restore native JavaScript test discovery after `_js_test.go` was misinterpreted as a GoOS-specific file.*

 * (yesterday) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#65477](https://github.com/microsoft/TypeScript/pull/65477) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Preserve glob range negation and path boundaries**

*Fix the vendored glob implementation to correctly preserve range negation and enforce path boundaries.*

 * (yesterday) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/65477#issuecomment-6861115833) **jakebailey** said "This one is probably worth a bug report upstream, or I just send a CL"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#65478](https://github.com/microsoft/TypeScript/pull/65478) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Respect Unicode boundaries when scanning symbol references**

*Ensure symbol reference scanning respects Unicode boundaries and refactor duplicated logic into a shared function.*

 * (yesterday) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#65479](https://github.com/microsoft/TypeScript/pull/65479) (Closed, `Author: Team`, `For Milestone Bug`, **jakebailey**, **gabritto**)

**Read declared members while instantiating base types**

*Ensure declared members are read during base-type instantiation by pushing resolvingObjectTypeStack earlier and updating base types.*

 * (yesterday) **typescript-automation[bot]** added labels `Author: Team`, `For Milestone Bug`, and assigned to **gabritto**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#65480](https://github.com/microsoft/TypeScript/pull/65480) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Fix mistaken slice delete in extractFromSymbol**

*Fix an out-of-bounds slice deletion in extractFromSymbol that can cause a crash when the second condition is true.*

 * (yesterday) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#65481](https://github.com/microsoft/TypeScript/pull/65481) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Ignore source files / module declarations in couldContainTypeVariables**

*Update couldContainTypeVariables to skip source file and module declaration nodes when traversing synthetic module wrapper symbols.*

 * (yesterday) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#65485](https://github.com/microsoft/TypeScript/issues/65485) (Open, `Bug`, `Domain: API`)

**API: \`generateTrace\` compiler option is accepted but no trace files are written for programs created through \`typescript/sync\`**

*The typescript/sync API accepts generateTrace but fails to write trace files for configured or synthetic programs.*

 * created by **johnnyreilly**

### [PR microsoft/TypeScript#65486](https://github.com/microsoft/TypeScript/pull/65486) (Open, `For Uncommitted Bug`)

**feat: add support regexp buffer boundary assertions**

*Add support for ECMAScript regular expression buffer boundary assertions proposed in the RegExp Buffer Boundaries specification.*

 * created by **a-tarasyuk**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/65486#issuecomment-6862246299) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."

### [PR microsoft/TypeScript#65487](https://github.com/microsoft/TypeScript/pull/65487) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Update DOM types**

*Updates DOM typings with latest web APIs across speech, storage, networking, accessibility, graphics, performance, and compatibility changes.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/65487#issuecomment-6862349734) **jakebailey** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/65487#issuecomment-6862352041) **typescript-automation[bot]** reported that the requested test and performance jobs had started and linked to their build results
 * [today](https://github.com/microsoft/TypeScript/pull/65487#issuecomment-6862872934) **typescript-automation[bot]** reported that the DT tests completed with branch-only TypeScript errors in the dom-speech-recognition package
 * [today](https://github.com/microsoft/TypeScript/pull/65487#issuecomment-6863278120) **typescript-automation[bot]** reported that user tests comparing the baseline and PR with tsc passed successfully
 * [today](https://github.com/microsoft/TypeScript/pull/65487#issuecomment-6863495358) **typescript-automation[bot]** reported that the requested performance run results were available and included comparison data
 * [today](https://github.com/microsoft/TypeScript/pull/65487#issuecomment-6864140353) **typescript-automation[bot]** reported changed tsc results from comparing the baseline and PR across the top 400 repositories, highlighting new VS Code build errors for review

### [Issue microsoft/TypeScript#65488](https://github.com/microsoft/TypeScript/issues/65488) (Open)

**\[ServerErrors\]\[JavaScript\] main**

*Main reports JavaScript server errors detected while analyzing 300 popular TypeScript repositories, with 34 runs timing out or failing.*

 * created by **typescript-automation[bot]**
 * [today](https://github.com/microsoft/TypeScript/issues/65488#issuecomment-6866102015) **typescript-automation[bot]** reported a panic in `custom/textDocument/sourceDefinition` caused by a path containing a URL query or fragment, along with a stack trace
 * [today](https://github.com/microsoft/TypeScript/issues/65488#issuecomment-6866102902) **typescript-automation[bot]** reported a flaky panic while handling a `textDocument/diagnostic` request in the Chart.js repository and provided stack-trace, artifact, and replay details
 * [today](https://github.com/microsoft/TypeScript/issues/65488#issuecomment-6866103853) **typescript-automation[bot]** reported a premature server connection closure affecting tastejs/todomvc and provided request logs and reproduction steps
 * [today](https://github.com/microsoft/TypeScript/issues/65488#issuecomment-6866104730) **typescript-automation[bot]** reported a runtime slice-bounds panic during cross-project handling in the TypeScript language service

### [PR microsoft/TypeScript#65489](https://github.com/microsoft/TypeScript/pull/65489) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Fix incorrect node type annotations**

*Correct inaccurate node type annotations identified during an audit.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#65490](https://github.com/microsoft/TypeScript/pull/65490) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Match typed\-path lint URL detection to runtime roots**

*Update typed-path lint URL detection to match the runtime’s configured roots.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#65491](https://github.com/microsoft/TypeScript/pull/65491) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Keep formatting fragments out of source\-file statement lists**

*Ensure formatting fragments are excluded from source-file statement lists to comply with their declared types.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#65492](https://github.com/microsoft/TypeScript/pull/65492) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Cancel mapper requests before waiting for host shutdown**

*Cancel pending mapper RPC contexts before waiting for host shutdown to prevent unresponsive mappers from blocking closure.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#65493](https://github.com/microsoft/TypeScript/pull/65493) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Convert patterns in object rest bindings to assignment targets**

*Fix emit to convert nested patterns in object rest bindings into valid assignment targets and avoid printer crashes.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [Issue microsoft/TypeScript#65494](https://github.com/microsoft/TypeScript/issues/65494) (Open)

**\[ServerErrors\]\[TypeScript\] main**

*TypeScript’s main branch error-analysis run reported failures across 300 popular repositories, including timeouts, clone failures, and unknown errors.*

 * created by **typescript-automation[bot]**
 * [today](https://github.com/microsoft/TypeScript/issues/65494#issuecomment-6868344932) **typescript-automation[bot]** reported a panic in `textDocument/completion` when a path contained a URL query or fragment
 * [today](https://github.com/microsoft/TypeScript/issues/65494#issuecomment-6868345660) **typescript-automation[bot]** reported a panic in textDocument/completion caused by a path containing a URL query or fragment, including a stack trace
 * [today](https://github.com/microsoft/TypeScript/issues/65494#issuecomment-6868346386) **typescript-automation[bot]** reported a panic in textDocument/completion when a path contained a URL query or fragment
 * [today](https://github.com/microsoft/TypeScript/issues/65494#issuecomment-6868347090) **typescript-automation[bot]** reported a panic in custom/textDocument/sourceDefinition caused by a path containing a URL query or fragment
 * [today](https://github.com/microsoft/TypeScript/issues/65494#issuecomment-6868347832) **typescript-automation[bot]** reported that the TypeScript server closed prematurely while processing vercel/ai and provided replay artifacts and reproduction steps

### [PR microsoft/TypeScript#65495](https://github.com/microsoft/TypeScript/pull/65495) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Fix kqueue descriptor ownership across watch replacement**

*Ensure kqueue watch replacements update descriptor ownership so stale subscriptions cannot close unrelated files or leak current descriptors.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#65496](https://github.com/microsoft/TypeScript/pull/65496) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Return a missing identifier from parseDecoratedExpression when no class follows**

*Correct parseDecoratedExpression to return a missing identifier, not a declaration, when no class follows.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#65497](https://github.com/microsoft/TypeScript/pull/65497) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Keep instantiated signature arguments out of parameter lists**

*Move instantiated signature argument information from parameter lists to the emit resolver so AST types remain accurate and verifiable.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/65497#issuecomment-6873023136) **jakebailey** said "It turns out we need a similar mechanism for another goofy type printing thing; will come up with some combined PR instead."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#65498](https://github.com/microsoft/TypeScript/pull/65498) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Fix CommonJS declaration emit crashes**

*Fix declaration emit crashes caused by invalid export names from destructured CommonJS requires and template-literal exports.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#65499](https://github.com/microsoft/TypeScript/pull/65499) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Fix JSDoc node types**

*Correct inaccurate JSDoc AST node type declarations, including restoring Identifier as a possible ModuleBody type in Strada.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#65500](https://github.com/microsoft/TypeScript/pull/65500) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Preserve JSON\-RPC error details in string formatting**

*Correct the reversed JSON-RPC error string formatting logic so error details are preserved.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#65501](https://github.com/microsoft/TypeScript/pull/65501) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Don't let TypeQuery have PropertyAccessExpression as ExprName**

*Prevent TypeQuery from using PropertyAccessExpression as ExprName by converting property accesses directly into entity names.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#65502](https://github.com/microsoft/TypeScript/pull/65502) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Stop building invalid type syntax for hover and code fixes**

*Stop generating invalid AST type syntax by storing hover and code-fix type arguments in emit context and updating related APIs and behavior.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [Issue microsoft/TypeScript#65503](https://github.com/microsoft/TypeScript/issues/65503) (Open, `Bug`, `Domain: API`)

**API client: concurrent \`Program\.getSourceFile\` calls for one file stampede the cache, each fetching the file whole**

*Concurrent `Program.getSourceFile` calls for the same file bypass in-flight caching, redundantly fetching and decoding the file multiple times.*

 * created by **SalvatorePreviti**

### [PR microsoft/TypeScript#65504](https://github.com/microsoft/TypeScript/pull/65504) (Open, `For Backlog Bug`)

**Validate wildcard package export targets in the native resolver**

*Validate wildcard package export targets against path-segment restrictions before expansion or resolution in the native Go resolver.*

 * created by **qiyuhuating**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/65504#issuecomment-6876462956) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (later) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`

### [Issue microsoft/TypeScript#65505](https://github.com/microsoft/TypeScript/issues/65505) (Open, `Bug`, `Domain: LS: TSServer`)

**\`workspace/willRenameFiles\` panics with "changes overlap" when the renamed file is loaded by \`import\(\)\` with a \`\.ts\` specifier**

*Renaming a TypeScript file referenced by a dynamic `.ts` import causes `workspace/willRenameFiles` to generate overlapping edits and panic.*

 * created by **SalvatorePreviti**

