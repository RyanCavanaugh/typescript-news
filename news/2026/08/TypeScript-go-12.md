# Report for 2026-08-12 (Wednesday, August 12th, 2026)

12 different users commented on 17 different issues.

## Recommended Actions

 * Response Recommended
    * @lukesandberg asked whether to abandon the approach and requested guidance on signal handler solutions in [microsoft/TypeScript-go#4592](https://github.com/microsoft/TypeScript-go/pull/4592#issuecomment-5269980557)
    * @remcohaszing requested logging capabilities for JSON RPC communication and LSP tracing in [microsoft/TypeScript-go#4712](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5279235915)
    * @sylirre provided resolution information for issue #4718 in [microsoft/TypeScript-go#4734](https://github.com/microsoft/TypeScript-go/pull/4734#issuecomment-5271186367)
    * @itibbers provided repro steps and data for a non-deterministic type-checking bug in [microsoft/TypeScript-go#4834](https://github.com/microsoft/TypeScript-go/issues/4834#issuecomment-5275662911)

## Activity Summary

### [PR microsoft/TypeScript-go#4313](https://github.com/microsoft/TypeScript-go/pull/4313) (Closed)

**Assign files to checkers using balanced import affinity**

*A FENNEL-based balanced import affinity algorithm replaces round-robin checker assignment to boost checking performance and reduce memory usage by 10%.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4313#issuecomment-5195258586) **typescript-automation[bot]** posted the requested perf run results with a detailed comparison report
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/4313#issuecomment-5244383319) **jakebailey** said "I tested the method from #4856 and it was worse; the FENNEL approach here does a better job across workloads, mui, etc."
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4313#issuecomment-5254846282) **RyanCavanaugh** suggested giving a parameter sweep for the remaining constant factor and said the code looked good
 * [today](https://github.com/microsoft/TypeScript-go/pull/4313#issuecomment-5271320890) **jakebailey** said "It did actually sweep that; I did just have it retry and 100 is still the best in what projects I have."
 * [today](https://github.com/microsoft/TypeScript-go/pull/4313#issuecomment-5271326245) **jakebailey** said "I will let it update some comments afterward, though, so will probably push soon when it's done benchmarking"

### [PR microsoft/TypeScript-go#4407](https://github.com/microsoft/TypeScript-go/pull/4407) (Closed, **jakebailey**, **Copilot**)

**Restore tsgo noEmit exit status semantics**

*Restore tsgo’s noEmit exit status semantics by porting tsc’s handleNoEmitOptions logic to ensure exit code 2 for type errors*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4407#issuecomment-5072717269) **jakebailey** said "@copilot+gpt-5.6-sol Merge main and fix conflicts, again!"
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4407#issuecomment-5073004746) **Copilot** merged main and resolved the emit API conflicts, preserved `ForceEmit` through incremental emit option wrapping, and validated all baselines, build, test, lint, and format checks
 * [today](https://github.com/microsoft/TypeScript-go/pull/4407#issuecomment-5269230040) **weswigham** said "@copilot Merge main and fix conflicts, again, again!"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4407#issuecomment-5269510327) **Copilot** merged latest main and resolved the emit helper conflict
 * [today](https://github.com/microsoft/TypeScript-go/pull/4407#issuecomment-5269553391) **jakebailey** said "Sadly my vote still does not count"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4407#issuecomment-5270160368) **weswigham** said "@copilot you broke the build, try again"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4407#issuecomment-5270347126) **jakebailey** said "Nope, they flipped the author order in the commits so now it doesn't think you pushed it"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4407#issuecomment-5270391379) **Copilot** updated the native-preview `noEmit` expectations to match upstream `emitSkipped: false` semantics and confirmed that tests passed
 * [today](https://github.com/microsoft/TypeScript-go/pull/4407#issuecomment-5270480799) **jakebailey** said "Ah, but it finished and then rerequested a review, invalidating it"

### [PR microsoft/TypeScript-go#4592](https://github.com/microsoft/TypeScript-go/pull/4592) (Open)

**Improve responsiveness of \`tsc build\` to interruption**

*Enhance tsc build responsiveness to SIGINT and SIGTERM by threading cancellation contexts through compilation, exiting with proper codes, and adding tests.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4592#issuecomment-5049741466) **lukesandberg** asked if Ctrl+C was handled by default in the old compiler and suggested removing the signal handlers given that interruption reports success in watch mode
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4592#issuecomment-5063525613) **jakebailey** said "The further this goes, the more I wonder if we should simply stop handling signals except in the LS or something. Obviously we never set up any signal handlers in tsc, right?"
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4592#issuecomment-5064330139) **lukesandberg** noted that skipping signal handlers causes crashes with partial outputs and suggested propagating context.Context for LSP timeouts for consistency
 * [today](https://github.com/microsoft/TypeScript-go/pull/4592#issuecomment-5269980557) **lukesandberg** asked whether to abandon the approach, described how removing signal handlers breaks ctrl-c handling in tsc --watch by causing goroutine panics, and proposed possible solutions

### [PR microsoft/TypeScript-go#4712](https://github.com/microsoft/TypeScript-go/pull/4712) (Open)

**Content mappers**

*Support external content mappers in tsconfig to transform and map unsupported file types into valid TypeScript*

 * [5 days ago](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5218558612) **andrewbranch** said "No, but custom transformers are still planned, mentioned in #4830. I’ll add ts-loader to the list of projects that needs it!"
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5247642853) **andrewbranch** described how third-party VS Code extensions can now contribute bundled content mappers directly, restricted to inferred projects without jsconfig/tsconfig files
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5257814665) **remcohaszing** played around with a CLI-based MDX content mapper built from scratch, found it similar to Volar but encountered a generic jsonrpc initialization error. suggested differentiating error messages for various failure causes, proposed mapping MDX VFileMessage fields (source, ruleId, url) to LSP diagnostic properties including code and codeDescription.href, and noted that type errors in unmapped generated content are surfaced to users.
 * [today](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5274755525) **andrewbranch** said "I’ve somewhat reluctantly added a way to support ` and explained why it can’t just translate into // @ts-expect-error`."
 * [today](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5275507907) **andrewbranch** benchmarked a Copilot-generated content mapper against vue-tsc on 222 fixtures, found it 2.4× faster with 24% less memory, noted scaffolding parse and type errors, and shared a branch for reference
 * [later](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5279235915) **remcohaszing** suggested adding logging support via a `tsc --verbose` flag and LSP `log` notifications for both editor and CLI

### [PR microsoft/TypeScript-go#4734](https://github.com/microsoft/TypeScript-go/pull/4734) (Open)

**Add Android ARM64 release target**

*Add Android ARM64 release target to the build configuration*

 * [today](https://github.com/microsoft/TypeScript-go/pull/4734#issuecomment-5266379403) **dlecan** reminded that TS Go didn't work on Ubuntu under Proot/Termux and that raw Termux lacked support for much of the native Node ecosystem due to missing android architecture support, and explained interest in Node/TS on Android for running AI clients like Claude Code
 * [today](https://github.com/microsoft/TypeScript-go/pull/4734#issuecomment-5266678320) **robertkirkman** inquired whether PRs like #4734 and similar ones progressively improved Android architecture support for Node in Termux and noted TS Go issues under proot-distro, suggesting @sylirre might have insights
 * [today](https://github.com/microsoft/TypeScript-go/pull/4734#issuecomment-5268571846) **jakebailey** clarified that the previous remark sounded like a complaint and explained he found the termux case simpler but hadn’t tested the PR since returning from a conference
 * [today](https://github.com/microsoft/TypeScript-go/pull/4734#issuecomment-5270017668) **dlecan** referenced similar PRs in the Node ecosystem and suggested focusing on Android because Node apps run slowly on Proot
 * [today](https://github.com/microsoft/TypeScript-go/pull/4734#issuecomment-5271186367) **sylirre** said "https://github.com/microsoft/typescript-go/issues/4718 will be resolved on the proot side in pending release."

### [Issue microsoft/TypeScript-go#4824](https://github.com/microsoft/TypeScript-go/issues/4824) (Closed, `bug`, **jakebailey**)

**ram use regression from new @deprecated diagnostics**

*A recent @deprecated diagnostics change nearly doubled tsgo’s memory usage causing OOM errors on large monorepos.*

 * (1 week ago) **RyanCavanaugh** added label `bug`, set milestone to `TypeScript 7.1`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4825](https://github.com/microsoft/TypeScript-go/pull/4825) (Closed)

**Fix deprecated contextual property memory regression**

*Update deprecation diagnostics to prevent memory ballooning from deferred processing and discard duplicate entries.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4825#issuecomment-5175461378) **typescript-automation[bot]** posted requested perf run results
 * [5 days ago](https://github.com/microsoft/TypeScript-go/pull/4825#issuecomment-5221609904) **jakebailey** said "Part of the problem with the checker diags is that we add them and then modify them, which makes deduping sort of annoying. We could fix that, though."
 * [5 days ago](https://github.com/microsoft/TypeScript-go/pull/4825#issuecomment-5222030816) **jakebailey** said "I took a stab at it. PTAL"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4825#issuecomment-5269365063) **jakebailey** said "Shockingly it was, due to mistakes earlier in the stack, so I figured I'd leave it"
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4834](https://github.com/microsoft/TypeScript-go/issues/4834) (Open, `bug`, **RyanCavanaugh**, **Copilot**)

**Default concurrent mode misses TS2307 that \`\-\-singleThreaded\` \(and TS 6\.0\) report, for import/export declarations inside non\-scope blocks**

*TypeScript's default concurrent mode omits TS2307 "Cannot find module" errors for import/export declarations inside non-scope blocks, unlike singleThreaded mode and TS 6.0.*

 * (1 week ago) **RyanCavanaugh** set milestone to `Post-7.0`, assigned to **Copilot**, and unassigned **Copilot**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4834#issuecomment-5275662911) **itibbers** reported non-deterministic type-checking output in TypeScript 7.0.2 when using multi-threaded mode with allowJs true and provided repro data showing determinism when single-threaded or allowJs false

### [Issue microsoft/TypeScript-go#4875](https://github.com/microsoft/TypeScript-go/issues/4875) (Open, `Needs Investigation`, **weswigham**, **Copilot**)

**\`@augments\` JSDoc tag causes compilation error in generated declaration file**

*A JSDoc @augments tag mismatched with the extends clause in generated declaration files triggers ts(8023) errors under tsgo.*

 * (yesterday) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `Post-7.0`, and assigned to **weswigham**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4875#issuecomment-5272281606) **weswigham** noted that the @augments check was too strict and suggested moving the check to checkClassLikeDeclaration and using isTypeIdenticalTo for comparison
 * **weswigham** assigned to **Copilot**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4875#issuecomment-5272301744) **jakebailey** said "I don't even know why this is happening in .ts files at all?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/4875#issuecomment-5272315368) **weswigham** said "Also a good point! Honestly, I don't know why we're checking this at all! This is, AFAIK, a lint-consistency level error, at most."

### [PR microsoft/TypeScript-go#4887](https://github.com/microsoft/TypeScript-go/pull/4887) (Closed)

**Make \`NodeHandle\` generic and generate \.Handle members of is\-guards for guarding node handles \(sync and async\)**

*Enable generic NodeHandle support and generate .Handle members on sync and async is-guards to narrow node handles.*

 * created by **weswigham**

### [PR microsoft/TypeScript-go#4888](https://github.com/microsoft/TypeScript-go/pull/4888) (Closed)

**Port \`parseCommandLine\`, \`readConfigFile\`, and \`parseJsonConfigFileContent\`**

*Expose the parseCommandLine, readConfigFile, and parseJsonConfigFileContent functions in the TypeScript API.*

 * created by **johnfav03**

### [PR microsoft/TypeScript-go#4889](https://github.com/microsoft/TypeScript-go/pull/4889) (Open, **weswigham**, **Copilot**)

**Use semantic type identity for JSDoc augments checks**

*Use semantic type identity for JSDoc @augments checks to avoid false mismatches when extending through aliases.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **weswigham**

### [Issue microsoft/TypeScript-go#4890](https://github.com/microsoft/TypeScript-go/issues/4890) (Open, `Domain: Editor`)

**Memory skyrockets with VSCode extension**

*Enabling the VSCode Typescript 7 extension with tsgo on a file using gulp-sass causes the TypeScript server to rapidly exhaust all system memory.*

 * created by **jjspace**
 * **jjspace** added label `Domain: Editor`

### [PR microsoft/TypeScript-go#4891](https://github.com/microsoft/TypeScript-go/pull/4891) (Closed)

**Update submodule**

*Update the submodule to include the recently merged TS repository pull request*

 * created by **jakebailey**
 * (later) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4892](https://github.com/microsoft/TypeScript-go/issues/4892) (Open)

**textDocument/diagnostic on the first\-opened file in a session can silently omit real errors**

*The first diagnostic request in a new tsgo LSP session can silently omit real errors until another file is queried.*

 * created by **cheruvian**

