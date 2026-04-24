# Report for 2026-04-17 (Friday, April 17th, 2026)

12 different users commented on 55 different issues.

## Activity Summary

### [PR microsoft/TypeScript-go#1949](https://github.com/microsoft/TypeScript-go/pull/1949) (Open, **jakebailey**, **Copilot**)

**Fix signature help applicable span for nested calls**

*Improves signature help applicable span for nested function calls to correctly handle empty argument lists and prioritize outer calls.*

 * [19 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1949#issuecomment-3604913495) **Copilot** fixed the empty argument list span, extended it to include a position, made all signature help tests pass, and planned to add tests for nested calls from issue #1419
 * [19 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1949#issuecomment-3608003427) **jakebailey** said "@copilot your PR is not formatted"
 * [19 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1949#issuecomment-3608039844) **Copilot** fixed formatting by running npx hereby format in commit 41f4bca
 * (today) **RyanCavanaugh** set milestones to `TypeScript 7.0 RC`, `TypeScript 7.0 RC`

### [PR microsoft/TypeScript-go#1966](https://github.com/microsoft/TypeScript-go/pull/1966) (Open)

**Add Yarn PnP support**

*Implement native Yarn Plug'n'Play support in TypeScript Go with PnP VFS, API, and manifest handling.*

 * [13 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1966#issuecomment-3754114970) **jdpt0** said "@jakebailey Any chance of getting this PR reviewed again? I, and I'm sure many others, would love to see this get merged before the full release. Many thanks 🙏 "
 * [13 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1966#issuecomment-3756917844) **jakebailey** clarified that deciding on the approach and long-term implications, not PR review, was the blocker
 * [12 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1966#issuecomment-3758895612) **wojtekmaj** supported adding native Plug’n’Play support to typescript-go, cited growing Yarn usage statistics, and explained how patch-based solutions cause maintenance overhead
 * **RyanCavanaugh** added to milestone `Possible Improvement`

### [Issue microsoft/TypeScript-go#2209](https://github.com/microsoft/TypeScript-go/issues/2209) (Closed, `Domain: Editor`, **Copilot**)

**\[lsp\] Go to Definition missing getter when property returns callable interface**

*Go to Definition in TypeScript Go Native only returns the callable interface signature, omitting the getter definition.*

 * (19 weeks ago) **jakebailey** added label `Domain: Editor`, and assigned to **Copilot**
 * **RyanCavanaugh** added to milestone `Post-7.0`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2210](https://github.com/microsoft/TypeScript-go/pull/2210) (Closed, **jakebailey**, **Copilot**)

**Fix Go to Definition for getters returning callable interfaces**

*Go to Definition on properties returning callable interfaces shows both the call signature and the getter declaration by preserving accessors.*

 * created by **Copilot**
 * (19 weeks ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2417](https://github.com/microsoft/TypeScript-go/pull/2417) (Open)

**Support \-\-pprofDir option with \-\-watch**

*Add --pprofDir support to the --watch mode to allow profiling of active processes.*

 * created by **tmm1**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2417#issuecomment-4264088120) **jakebailey** said "#1317 is closed and this PR is out of date; are you planning on updating it?"
 * (today) **RyanCavanaugh** set milestones to `Possible Improvement`, `Possible Improvement`

### [PR microsoft/TypeScript-go#2478](https://github.com/microsoft/TypeScript-go/pull/2478) (Open)

**Exit LSP process if parent process stops existing**

*Implement periodic parent process ID checks in the LSP server to terminate the server when the parent process exits.*

 * [13 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2478#issuecomment-3741141626) **DanielRosenwasser** said "If the parent process no longer exists, won't we get an EOF on standard input or something?"
 * [13 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2478#issuecomment-3741155153) **jakebailey** said "Yeah, I guess that's probably the case..."
 * [13 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2478#issuecomment-3746460286) **DanielRosenwasser** said "https://github.com/microsoft/typescript-go/pull/2499 might explain why an EOF was not sufficient for shutting down."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2478#issuecomment-4269974535) **jakebailey** said "Going to draft this for the time being again, sorry; I want to double check that these comments are actually correct and would rather not cram it in."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2478#issuecomment-4270307434) **andrewbranch** said "I'm not against this if we think we still need it, but it feels like a bug (like #2499 was) if we can't exit just by reading from a STDIN that's no longer connected to anything"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2478#issuecomment-4270354928) **jakebailey** explained that a client could set up a FIFO as the file descriptor for a child process which might never close

### [Issue microsoft/TypeScript-go#2621](https://github.com/microsoft/TypeScript-go/issues/2621) (Open, `bug`, **iisaduan**, **Copilot**)

**Fourslash is broken when making requests in unconfigured \.js files**

*Fourslash requests in unconfigured .js files fail with “no project found” errors, breaking tests such as auto-import completion.*

 * (6 weeks ago) **RyanCavanaugh** added label `bug`, and set milestone to `TypeScript 7.0 RC`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2621#issuecomment-4269361026) **jakebailey** investigated an issue with fourslash tests and explained why the new runner’s server-based approach loads JS files and alters behavior compared to Strada
 * [today](https://github.com/microsoft/TypeScript-go/issues/2621#issuecomment-4270442818) **DanielRosenwasser** suggested switching to use the "state baselining" infrastructure if needed

### [PR microsoft/TypeScript-go#2820](https://github.com/microsoft/TypeScript-go/pull/2820) (Closed, **jakebailey**, **Copilot**)

**Port TypeScript\#63071: Mark downlevelIteration as removed**

*In the Go port of TypeScript, mark the downlevelIteration compiler option as removed by emitting a removed-option diagnostic, skipping related tests, and deleting obsolete baselines.*

 * created by **Copilot**
 * (8 weeks ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2907](https://github.com/microsoft/TypeScript-go/pull/2907) (Open, **RyanCavanaugh**, **Copilot**)

**\[WIP\] Fix issue 63192 in TypeScript repository**

*Add reentrancy guards in TypeScript compiler to prevent infinite recursion during destructuring loop variables with defaults.*

 * **Copilot** assigned to **RyanCavanaugh**
 * [7 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2907#issuecomment-3963094319) **RyanCavanaugh** said "@ahejlsberg the code comments here are a bit much but does this look like a correct CFA fix?"
 * [7 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2907#issuecomment-3963104509) **RyanCavanaugh** said "Via https://github.com/Microsoft/TypeScript/issues/63192"
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [PR microsoft/TypeScript-go#2914](https://github.com/microsoft/TypeScript-go/pull/2914) (Open)

**adds tracing \(\-\-generateTrace\)**

*Implement a tracing feature with --generateTrace to output types.json and trace.json files using a context-based approach.*

 * created by **dimitropoulos**
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/2914#issuecomment-4218382821) **jakebailey** indicated that baselines were unstable and showed a diff with added trace events
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/2914#issuecomment-4219877730) **dimitropoulos** explained that sampled events were skipped entirely in deterministic mode, leaving only B/E pairs with the deterministic counter to produce stable baselines
 * (today) **RyanCavanaugh** set milestones to `Possible Improvement`, `TypeScript 7.0 RC`, and removed from milestone `Possible Improvement`

### [PR microsoft/TypeScript-go#2928](https://github.com/microsoft/TypeScript-go/pull/2928) (Open, **RyanCavanaugh**, **Copilot**)

**Fix crash related to tuple rest arity**

*Prevent nil pointer dereference during variadic tuple rest type inference by adding nil guards and a new compiler test case.*

 * created by **Copilot**
 * (6 weeks ago) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2928#issuecomment-4269802788) **RyanCavanaugh** said "Hoisting comment: This is a fix for https://github.com/microsoft/TypeScript/issues/63199"
 * (today) **RyanCavanaugh** set milestones to `TypeScript 7.0 RC`, `TypeScript 7.0 RC`

### [PR microsoft/TypeScript-go#2954](https://github.com/microsoft/TypeScript-go/pull/2954) (Closed, **andrewbranch**, **Copilot**)

**Port scanner/token navigation fixes from PR \#2888 to \`\_packages/ast\`**

*Port PR #2888 fixes to the TypeScript AST package, refining JSDoc comment scanning and EOF navigation for unterminated nodes.*

 * created by **Copilot**
 * (6 weeks ago) **Copilot** assigned to **Copilot**, **andrewbranch**
 * (today) **jakebailey** closed the issue
 * (today) **jakebailey** reopened the issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/2954#issuecomment-4269571742) **andrewbranch** said "Yeah, I'll fix it after this merges"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2954#issuecomment-4269631800) **jakebailey** said "Ah, fails CI now that the AST was regenerated"
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#2970](https://github.com/microsoft/TypeScript-go/pull/2970) (Open, **ahejlsberg**)

**Fix nil dereference crash during checker initialization when resolving array types**

*Introduce lazy global array type initialization and transient symbol handling to prevent nil dereference crashes during checker initialization*

 * created by **Andarist**
 * (today) **RyanCavanaugh** set milestone to `TypeScript 7.0 RC`, and assigned to **ahejlsberg**

### [PR microsoft/TypeScript-go#3102](https://github.com/microsoft/TypeScript-go/pull/3102) (Open)

**Fix a formatting crash caused by template literal in parser\-recovered property signature**

*Fix formatting crash by ensuring grammar error nodes are processed to prevent misinterpreting template literals in recovered property signatures.*

 * created by **Andarist**
 * (today) **RyanCavanaugh** set milestones to `TypeScript 7.0 RC`, `TypeScript 7.0 RC`

### [PR microsoft/TypeScript-go#3114](https://github.com/microsoft/TypeScript-go/pull/3114) (Closed)

**Don't use full emit resolver just because JSX is enabled**

*Use the full emit resolver only for files containing JSX to avoid unnecessary work and improve concurrency.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3159](https://github.com/microsoft/TypeScript-go/pull/3159) (Open, **jakebailey**, **Copilot**)

**Fix format selection deleting comments when selection ends inside comment trivia**

*Prevent comments from being deleted when formatting selections end inside comment trivia by adjusting trivia range handling.*

 * [1 month ago](https://github.com/microsoft/TypeScript-go/pull/3159#issuecomment-4092680089) **Copilot** fixed broken formatSelectionEditAtEndOfRange_test by capping previousRangeTriviaEnd before comment trivia in consumeTokenAndAdvanceScanner and verified tests pass
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3159#issuecomment-4195608650) **jakebailey** said "@copilot address review comments"
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3159#issuecomment-4195634797) **Copilot** addressed all three review comments in commit 11fd998d by fixing misleading position comments, renaming the test description, and replacing loose assertions with exact checks
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [PR microsoft/TypeScript-go#3171](https://github.com/microsoft/TypeScript-go/pull/3171) (Open, **ahejlsberg**, **RyanCavanaugh**, **Copilot**)

**Fix stack overflow in relater's skipCaching path for recursive tuple types**

*Add depth counters to prevent unbounded recursion and stack overflow in the relater skipCaching path for recursive tuple types.*

 * **RyanCavanaugh** assigned to **ahejlsberg**
 * [1 month ago](https://github.com/microsoft/TypeScript-go/pull/3171#issuecomment-4099158802) **RyanCavanaugh** said "@ahejlsberg this seems like two fixes when only one is needed, but I'm not sure which is preferable (or maybe there's a third option)"
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3171#issuecomment-4264125280) **jakebailey** said "This doesn't seem right, it's just adding a random new depth limiter."
 * (today) **RyanCavanaugh** set milestones to `Post-7.0`, `TypeScript 7.0 RC`, and removed from milestone `Post-7.0`

### [PR microsoft/TypeScript-go#3175](https://github.com/microsoft/TypeScript-go/pull/3175) (Open, **ahejlsberg**, **RyanCavanaugh**, **Copilot**)

**Fix template literal type exponential blowup in addSpans**

*Add growth limits in addSpans to prevent exponential template literal type expansion causing memory exhaustion.*

 * **Copilot** assigned to **RyanCavanaugh**
 * **RyanCavanaugh** assigned to **ahejlsberg**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3175#issuecomment-4264113737) **jakebailey** said "This just adds in a new limit that Strada didn't have. I don't think this is right."
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [PR microsoft/TypeScript-go#3183](https://github.com/microsoft/TypeScript-go/pull/3183) (Closed)

**Accept diffs that just reduce error elaboration**

*Accept diffs reducing error message elaboration for the baselines instanceofOperatorWithInvalidOperands.es2015, usingDeclarations.14, and usingDeclarationsWithIteratorObject.*

 * created by **RyanCavanaugh**
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#3212](https://github.com/microsoft/TypeScript-go/pull/3212) (Open)

**Fix error spans for \`@satisfies\`**

*Fix error span calculation for @satisfies to ensure accurate error highlighting.*

 * created by **Andarist**
 * (today) **RyanCavanaugh** set milestones to `TypeScript 7.0 RC`, `TypeScript 7.0 RC`

### [PR microsoft/TypeScript-go#3216](https://github.com/microsoft/TypeScript-go/pull/3216) (Closed)

**fix: clean up failed pprof startup files**

*Use a start hook to remove partially created CPU profile files on BeginProfiling failures, adding a unit test for cleanup.*

 * created by **buley**
 * **RyanCavanaugh** added to milestone `Possible Improvement`
 * [today](https://github.com/microsoft/TypeScript-go/pull/3216#issuecomment-4270006802) **RyanCavanaugh** said "Hardening internal debug/profiling codepaths against benign failures isn't a great use of churn/risk. It's fine if a local dev has to delete this file manually after killing the process or whatever."
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#3220](https://github.com/microsoft/TypeScript-go/pull/3220) (Open)

**Preserve error elaboration for indexed access type assignments**

*Improve TypeScript diagnostic messages by preserving specific error details for assignments to indexed access types.*

 * created by **WhiteMinds**
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3220#issuecomment-4127991153) **jakebailey** said "Maybe I don't have context here, but, I don't find the new messages more helpful than the existing one..."
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3220#issuecomment-4131552782) **gary-donut** provided an example demonstrating that assignment via this['faa'] yields less precise error messages than direct assignment
 * **RyanCavanaugh** added to milestone `Possible Improvement`

### [PR microsoft/TypeScript-go#3232](https://github.com/microsoft/TypeScript-go/pull/3232) (Open)

**Speed up lookupSymbolChain**

*Optimize lookupSymbolChain by caching alias-only symbol lists per table and refining iteration logic, reducing CPU time by 61%.*

 * created by **jakebailey**
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3232#issuecomment-4129832914) **jakebailey** said "Unfortunately it seems like if I remove these fast paths (which presumably are iffy), and then restrict to just globals, it goes back to having the same perf..."
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3232#issuecomment-4129842233) **jakebailey** drafted a comment admitting overexcitement and lamenting the lack of tests to prove the change wrong
 * [today](https://github.com/microsoft/TypeScript-go/pull/3232#issuecomment-4270043008) **jakebailey** said "To be clear, I pushed to this PR with an updated solution which I believe is as fast and should be correct at the cost of another bit out of the key."
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [PR microsoft/TypeScript-go#3263](https://github.com/microsoft/TypeScript-go/pull/3263) (Open)

**Preserve original comments on params in dts generated by pseudo type node builder under \`removeComments: false\`**

*Declaration files generated by the pseudo type node builder with removeComments disabled fail to preserve original parameter comments.*

 * created by **Andarist**
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3263#issuecomment-4156791336) **jakebailey** said "At some level, I wonder if this is even worth it."
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/3263#issuecomment-4250720724) **Andarist** noted that shouldWriteComment explicitly allows jsdoc-like comments and that the dts emitter configures the printer with onlyPrintJsDocStyle enabled
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [PR microsoft/TypeScript-go#3264](https://github.com/microsoft/TypeScript-go/pull/3264) (Open, **gabritto**)

**support quick info and go to definition on mapped keys**

*Add quick info and go-to-definition support for mapped type keys in TypeScript.*

 * created by **Zzzen**
 * (today) **RyanCavanaugh** set milestone to `TypeScript 7.0 RC`, and assigned to **gabritto**

### [PR microsoft/TypeScript-go#3266](https://github.com/microsoft/TypeScript-go/pull/3266) (Closed, `dependencies`, `javascript`)

**Bump brace\-expansion from 5\.0\.4 to 5\.0\.5**

*Bump the brace-expansion dependency from version 5.0.4 to 5.0.5 to incorporate upstream patches and fixes.*

 * created by **dependabot[bot]**
 * (3 weeks ago) **dependabot[bot]** added labels `dependencies`, `javascript`
 * (today) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/3266#issuecomment-4270555976) **dependabot[bot]** explained how to ignore dependency update notifications or reopen the PR to resolve conflicts

### [PR microsoft/TypeScript-go#3271](https://github.com/microsoft/TypeScript-go/pull/3271) (Open)

**Fix for a snapshot update with a nil CommandLine**

*Add a nil check in NewProjectResponse to prevent panics when handling projects with nil CommandLine during snapshot updates.*

 * created by **navya9singh**
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3271#issuecomment-4145607075) **andrewbranch** said "When does a project have a nil CommandLine?"
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3271#issuecomment-4263449950) **jakebailey** said "Is this handled by #3409? Or is this a different nil config problem?"
 * (today) **RyanCavanaugh** set milestones to `Post-7.0`, `TypeScript 7.0 RC`, and removed from milestone `Post-7.0`

### [PR microsoft/TypeScript-go#3297](https://github.com/microsoft/TypeScript-go/pull/3297) (Open)

**Allow global Symbol computed names during pseudochecker object literal serialization**

*Support global Symbol computed property names in pseudochecker object literal serialization to match Strada’s behavior.*

 * created by **Andarist**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [PR microsoft/TypeScript-go#3305](https://github.com/microsoft/TypeScript-go/pull/3305) (Open, **DanielRosenwasser**, **Copilot**)

**Add "Sort Imports" & "Remove Unused Imports" commands to VS Code extension**

*Register runtime handlers for sortImports and removeUnusedImports commands and adjust disposal order to prevent conflicts with the built-in TypeScript extension.*

 * (2 weeks ago) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/3305#issuecomment-4256048203) **azure-pipelines[bot]** reported that one pipeline was filtered out due to trigger conditions
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [PR microsoft/TypeScript-go#3331](https://github.com/microsoft/TypeScript-go/pull/3331) (Open)

**Use trie for removeStringLiteralsMatchedByTemplateLiterals**

*Port a trie-based implementation for removeStringLiteralsMatchedByTemplateLiterals to fix inaccuracies in template literal matching.*

 * created by **eps1lon**
 * **RyanCavanaugh** added to milestone `Possible Improvement`

### [PR microsoft/TypeScript-go#3334](https://github.com/microsoft/TypeScript-go/pull/3334) (Closed)

**Implement multi\-file doc highlights**

*Implement a new VS Code LSP extension method to support document highlights across multiple files.*

 * created by **jakebailey**
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/3334#issuecomment-4254365695) **azure-pipelines[bot]** reported that one pipeline was filtered out due to trigger conditions
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3391](https://github.com/microsoft/TypeScript-go/pull/3391) (Open)

**Fix inference from unions of arrays with different nesting depths**

*Add a matching pass to infer equally nested arrays first, correcting generic type inference for unions like T[] | T[][]*

 * created by **Yiin**
 * [5 days ago](https://github.com/microsoft/TypeScript-go/pull/3391#issuecomment-4231802984) **Yiin** said "@microsoft-github-policy-service agree"
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [PR microsoft/TypeScript-go#3398](https://github.com/microsoft/TypeScript-go/pull/3398) (Closed)

**Update dependencies**

*Update project dependencies to resolve npm audit vulnerabilities and clean up related package issues.*

 * created by **jakebailey**
 * [4 days ago](https://github.com/microsoft/TypeScript-go/pull/3398#issuecomment-4241355402) **jakebailey** said "Failing due to https://github.com/microsoft/vscode-extension-telemetry/issues/244"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3401](https://github.com/microsoft/TypeScript-go/pull/3401) (Closed)

**Fix file counts, jsx in project telemetry**

*Update project telemetry to accurately categorize files by their declared type and ensure the JSX metric is reported as a string.*

 * created by **jakebailey**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3401#issuecomment-4264189999) **DanielRosenwasser** asked which part of file counting this fix addressed
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3401#issuecomment-4264203781) **jakebailey** admitted that the change fixed nothing related to file counting and that he did not know what was wrong
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3403](https://github.com/microsoft/TypeScript-go/pull/3403) (Open)

**Exposing more endpoints**

*Expose additional API endpoints to expand available functionality.*

 * created by **navya9singh**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [PR microsoft/TypeScript-go#3412](https://github.com/microsoft/TypeScript-go/pull/3412) (Closed)

**fix\(3410\): preserve type arguments in hover for qualified names**

*Qualified name hover tooltips now correctly display preserved type arguments.*

 * created by **a-tarasyuk**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3412#issuecomment-4261910421) **ahejlsberg** clarified that ExpressionWithTypeArguments is now parsed for instantiation expressions and can occur in regular expressions
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3412#issuecomment-4263833864) **weswigham** explained that type nodes only allow expressions at the end of a typeof query and illustrated with parsing examples
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [PR microsoft/TypeScript-go#3414](https://github.com/microsoft/TypeScript-go/pull/3414) (Closed)

**Update CHANGES\.md to reflect that JSDoc types still permit postfix/prefix \`?\`/\`\!\`\.**

*Update CHANGES.md to note that JSDoc type annotations continue to allow prefix and postfix '?' and '!' modifiers.*

 * created by **DanielRosenwasser**
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/3414#issuecomment-4255572022) **azure-pipelines[bot]** reported that one pipeline was filtered out due to trigger conditions
 * (today) **DanielRosenwasser** closed the issue

### [Issue microsoft/TypeScript-go#3422](https://github.com/microsoft/TypeScript-go/issues/3422) (Closed, `Domain: Editor`)

**Wrong function signature and missing invoking description in hover**

*In tsgo, the hover tooltip for callable/constructable types omits the 'new' signature and JSDoc descriptions.*

 * created by **Withered-Flower-0422**
 * **Withered-Flower-0422** added label `Domain: Editor`
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#3424](https://github.com/microsoft/TypeScript-go/pull/3424) (Closed)

**fix\(3422\): fix resolving signature docs on hover**

*Corrects the resolution of function signature documentation when hovering over code elements.*

 * created by **a-tarasyuk**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3424#issuecomment-4270507017) **DanielRosenwasser** said "Thanks!"
 * (today) **DanielRosenwasser** closed the issue

### [Issue microsoft/TypeScript-go#3426](https://github.com/microsoft/TypeScript-go/issues/3426) (Closed, `possible improvement`, **ahejlsberg**)

**tsc produces error, tsgo doesn't with sufficiently nested type**

*TypeScript 6 reports a nested type incompatibility between input and output APIs that tsgo overlooks until a layer is removed.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3426#issuecomment-4262716834) **RyanCavanaugh** investigated and ruled out the issue as a manifestation of TypeScript issue #52912
 * (yesterday) **RyanCavanaugh** unassigned **RyanCavanaugh**, **Copilot**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3426#issuecomment-4271186734) **ahejlsberg** explained that the Copilot minimal repro reproduced the error, described how isDeeplyNestedType’s type ID heuristic miscounts nested types under different checker assignments, and showed how this leads to premature recursion detection after three nesting levels
 * (today) **ahejlsberg** added label `possible improvement`, and removed label `bug`
 * [today](https://github.com/microsoft/TypeScript-go/issues/3426#issuecomment-4271613649) **joshcartme** inquired whether differentiating between generic and concrete types in Copilot's PR was reasonable after building and testing it against his repro and noting tsgo reported the error
 * [later](https://github.com/microsoft/TypeScript-go/issues/3426#issuecomment-4273579488) **ahejlsberg** pointed out that the proposed fix was invalid because generative recursive type references such as Deep<Deep<T>> can lack generic types after instantiation but still require detection

### [PR microsoft/TypeScript-go#3427](https://github.com/microsoft/TypeScript-go/pull/3427) (Closed, **ahejlsberg**, **Copilot**)

**Fix isDeeplyNestedType false positive for concrete TypeReferences in multi\-checker mode**

*Use concrete type instances as recursion identities to eliminate false-positive type compatibility in tsgo’s multi-checker mode.*

 * **Copilot** assigned to **RyanCavanaugh**
 * (yesterday) **RyanCavanaugh** assigned to **ahejlsberg**, and unassigned **RyanCavanaugh**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [PR microsoft/TypeScript-go#3428](https://github.com/microsoft/TypeScript-go/pull/3428) (Closed)

**Fix auto\-import log structure after deduplicating node\_modules package extractions**

*Restructure auto-import timing logs to accurately measure the full build work after deduplicating package extractions.*

 * created by **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#3430](https://github.com/microsoft/TypeScript-go/pull/3430) (Closed)

**Move @typescript/api and @typescript/ast into @typescript/native\-preview for publishing**

*Merge @typescript/api and @typescript/ast into @typescript/native-preview to prevent version mismatches and simplify publishing ahead of TypeScript 7.0.*

 * created by **andrewbranch**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [PR microsoft/TypeScript-go#3431](https://github.com/microsoft/TypeScript-go/pull/3431) (Closed)

**Exports aliases for CJS \`exports\.Foo = \.\.\.\` assignments when appropriate**

*Export alias symbols for CJS exports.Foo assignments on entity names or class expressions to preserve type and namespace semantics.*

 * created by **ahejlsberg**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#3432](https://github.com/microsoft/TypeScript-go/pull/3432) (Open)

**Enable allowJs when inferred project has root JS files**

*Automatically enable allowJs for inferred projects with root JS files and introduce a @noDefaultOpen option to prevent default file openings in fourslash tests.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3432#issuecomment-4269567137) **andrewbranch** asked if compilerOptionsForInferredProjects was being sent by default and noted that default inferred project options enable AllowJs
 * [today](https://github.com/microsoft/TypeScript-go/pull/3432#issuecomment-4269680369) **jakebailey** described that at startup the sent options omitted allowJs and that different tools behaved inconsistently
 * [today](https://github.com/microsoft/TypeScript-go/pull/3432#issuecomment-4270319212) **andrewbranch** said "LGTM but generate is failing"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3432#issuecomment-4270480683) **DanielRosenwasser** said "Why don't we just enable allowJs for inferred projects without adjustments based on root files?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3432#issuecomment-4270499003) **jakebailey** said "We can do that, though I think we still need to force it on like Strada did, lest someone configure the inferred project manually, which is more or less the problem fourslash has."
 * [today](https://github.com/microsoft/TypeScript-go/pull/3432#issuecomment-4270540197) **jakebailey** said "Oh, I'm dumb, the tests I'm referring to are tests which are explicitly trying to test behavior when allowJs is off. Maybe these tests are just bunk"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3432#issuecomment-4270567483) **jakebailey** provided an example diff showing that go-to-definition stopped navigating to the CSS types file when allowJs and allowNonTsExtensions were enabled in an inferred project
 * [today](https://github.com/microsoft/TypeScript-go/pull/3432#issuecomment-4270595230) **andrewbranch** asked whether importing a JavaScript file without type declarations would cause an error in an inferred project when only TypeScript files are opened
 * [today](https://github.com/microsoft/TypeScript-go/pull/3432#issuecomment-4271124900) **DanielRosenwasser** suggested that importing a JS file without TypeScript declarations would not be an error and recommended making allowJs the default for unconfigured projects
 * [today](https://github.com/microsoft/TypeScript-go/pull/3432#issuecomment-4271133192) **jakebailey** said "We actually do not yet support client setting any compiler options."
 * [today](https://github.com/microsoft/TypeScript-go/pull/3432#issuecomment-4271642537) **andrewbranch** confirmed that session.compilerOptionsForInferredProjects was never set in real VS Code and that project.go default options always included --allowJs
 * [today](https://github.com/microsoft/TypeScript-go/pull/3432#issuecomment-4271924781) **jakebailey** mentioned that the issue wasn't urgent, said they would investigate adjusting tests to use defaults, and noted the need to support the VS Code options for those defaults

### [PR microsoft/TypeScript-go#3433](https://github.com/microsoft/TypeScript-go/pull/3433) (Closed)

**Port go\-to\-def code for called declarations**

*Port call resolution code to support go-to-definition for called declarations, resolving issue #2209.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3434](https://github.com/microsoft/TypeScript-go/issues/3434) (Closed)

**Literal\-type overloads disable contextual typing from explicit \<T\> argument**

*Literal-type overloads alongside a generic overload block contextual typing for explicit type arguments, causing $state<Promise<TrendData[]|undefined>>(new Promise) to error.*

 * created by **harshmandan**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3434#issuecomment-4271144765) **RyanCavanaugh** asked if the 6.0 behavior was correct and reported seeing an error in the Playground
 * [today](https://github.com/microsoft/TypeScript-go/issues/3434#issuecomment-4271163638) **harshmandan** said "You're right — my mistake. This happens even in 5.9.3. Closing as not a bug."
 * (today) **harshmandan** closed the issue

### [PR microsoft/TypeScript-go#3435](https://github.com/microsoft/TypeScript-go/pull/3435) (Open)

**Make LS checkers time out after being idle, segment based on use \(take 2\)**

*Restore idle timeouts and usage-based segmentation for language server checkers following safety confirmation in #3429.*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#3436](https://github.com/microsoft/TypeScript-go/pull/3436) (Closed)

**feat: add textDocument/\_vs\_onAutoInsert handler for VS closing tag auto\-insertion**

*Implement Visual Studio–specific _vs_onAutoInsert LSP handler and protocol types to auto-insert closing HTML/JSX tags and fix code generator jsonName bug.*

 * created by **lucygramley**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3436#issuecomment-4271790692) **jakebailey** noted overlap between the code and existing tagClosing.ts and suggested consolidating instead of adding new code

### [Issue microsoft/TypeScript-go#3437](https://github.com/microsoft/TypeScript-go/issues/3437) (Open)

**\[ServerErrors\]\[TypeScript\] main vs **

*The TypeScript error-delta pipeline on the main branch analyzed 300 popular GitHub repos, succeeding on 201 with 8 interesting changes and various failures.*

 * created by **typescript-bot**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3437#issuecomment-4271898551) **typescript-bot** reported a panic during textDocument/formatting with a debug failure false expression and included a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/3437#issuecomment-4271898604) **typescript-bot** reported a panic during textDocument/formatting due to a Debug failure: False expression: Token end is child end
 * [today](https://github.com/microsoft/TypeScript-go/issues/3437#issuecomment-4271898675) **typescript-bot** reported the server connection closed prematurely with an undefined error while processing the elastic/kibana repo
 * [today](https://github.com/microsoft/TypeScript-go/issues/3437#issuecomment-4271898763) **typescript-bot** reported server connection closed prematurely with undefined while processing t4t5/sweetalert and included logs and reproduction steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/3437#issuecomment-4271898817) **typescript-bot** reported a premature server connection closure and provided logs, affected repos, last requests, and repro steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/3437#issuecomment-4271898868) **typescript-bot** reported that the server connection closed prematurely with an undefined error for the n8n repository and provided artifact links, recent editor requests, and repro steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/3437#issuecomment-4271898938) **typescript-bot** reported a panic failure in textDocument/formatting handling due to false expression Token end is child end

### [Issue microsoft/TypeScript-go#3438](https://github.com/microsoft/TypeScript-go/issues/3438) (Closed, `Crash`, **jakebailey**, **Copilot**)

**Referencing a \`\.d\.ts\` file on disk via \`\.ts\` in a paths entry crashes**

*Referencing a `.d.ts` file via a `.ts` path mapping in the TypeScript configuration causes a panic in the type checker.*

 * created by **Mike-Dax**
 * **Mike-Dax** added label `Crash`
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#3439](https://github.com/microsoft/TypeScript-go/pull/3439) (Closed, **jakebailey**, **Copilot**)

**Fix crash when paths entry references \.d\.ts file via \.ts extension**

*Corrects module resolution to prevent crashes when a paths entry specifies a .ts extension but resolves to a .d.ts file.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

