# Report for 2026-08-07 (Friday, August 7th, 2026)

11 different users commented on 25 different issues.

## Recommended Actions

 * Response Recommended
    * @nikeedw updated on CLA signing and resubmitted the PR #4846 in [microsoft/TypeScript-go#4748](https://github.com/microsoft/TypeScript-go/issues/4748#issuecomment-5221620947)
    * @nikeedw provided measurements and test results as requested in [microsoft/TypeScript-go#4846](https://github.com/microsoft/TypeScript-go/pull/4846#issuecomment-5222176600)
    * @typescript-automation[bot] reported a runtime panic due to index out of range in [microsoft/TypeScript-go#4851](https://github.com/microsoft/TypeScript-go/issues/4851#issuecomment-5223442669)
    * @typescript-automation[bot] reported a panic handling textDocument/diagnostic request in [microsoft/TypeScript-go#4851](https://github.com/microsoft/TypeScript-go/issues/4851#issuecomment-5223442715)
    * @typescript-automation[bot] reported a panic in textDocument/diagnostic in [microsoft/TypeScript-go#4851](https://github.com/microsoft/TypeScript-go/issues/4851#issuecomment-5223442770)
    * @typescript-automation[bot] reported a panic due to unhandled node kind in jsx initializer in [microsoft/TypeScript-go#4851](https://github.com/microsoft/TypeScript-go/issues/4851#issuecomment-5223442811)
    * @typescript-automation[bot] reported a panic in textDocument/diagnostic request in [microsoft/TypeScript-go#4851](https://github.com/microsoft/TypeScript-go/issues/4851#issuecomment-5223442853)
    * @typescript-automation[bot] reported a panic during textDocument/diagnostic handling in [microsoft/TypeScript-go#4851](https://github.com/microsoft/TypeScript-go/issues/4851#issuecomment-5223442885)
    * @typescript-automation[bot] provided repro steps as requested in [microsoft/TypeScript-go#4851](https://github.com/microsoft/TypeScript-go/issues/4851#issuecomment-5223442922)
    * @typescript-automation[bot] provided repro steps and error details in [microsoft/TypeScript-go#4851](https://github.com/microsoft/TypeScript-go/issues/4851#issuecomment-5223442965)
    * @typescript-automation[bot] reported server connection error and provided repro steps in [microsoft/TypeScript-go#4851](https://github.com/microsoft/TypeScript-go/issues/4851#issuecomment-5223442995)
    * @typescript-automation[bot] provided repro steps as requested in [microsoft/TypeScript-go#4851](https://github.com/microsoft/TypeScript-go/issues/4851#issuecomment-5223443037)
    * @typescript-automation[bot] reported a server connection closed prematurely error and provided repro steps in [microsoft/TypeScript-go#4851](https://github.com/microsoft/TypeScript-go/issues/4851#issuecomment-5223443088)
    * @typescript-automation[bot] provided repro steps and error logs in [microsoft/TypeScript-go#4851](https://github.com/microsoft/TypeScript-go/issues/4851#issuecomment-5223443160)
    * @typescript-automation[bot] reported server connection closed error for freeCodeCamp/freeCodeCamp in [microsoft/TypeScript-go#4851](https://github.com/microsoft/TypeScript-go/issues/4851#issuecomment-5223443247)
    * @typescript-automation[bot] reported a panic during textDocument/diagnostic that needs investigation in [microsoft/TypeScript-go#4851](https://github.com/microsoft/TypeScript-go/issues/4851#issuecomment-5223443309)
    * @typescript-automation[bot] reported a panic during textDocument/diagnostic handling in [microsoft/TypeScript-go#4851](https://github.com/microsoft/TypeScript-go/issues/4851#issuecomment-5223443362)
    * @typescript-automation[bot] reported a panic error in JSX transformer in [microsoft/TypeScript-go#4851](https://github.com/microsoft/TypeScript-go/issues/4851#issuecomment-5223443422)
    * @typescript-automation[bot] reported a panic in textDocument/diagnostic handling in [microsoft/TypeScript-go#4851](https://github.com/microsoft/TypeScript-go/issues/4851#issuecomment-5223443481)

## Activity Summary

### [Issue microsoft/TypeScript-go#4520](https://github.com/microsoft/TypeScript-go/issues/4520) (Open, `Domain: Editor`)

**Bug Report: Severe memory leak triggered by "TypeScript \(Native Preview\)" extension**

*Enabling the TypeScript Native Preview extension in an empty folder without package.json causes a persistent memory leak until VS Code is closed.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/4520#issuecomment-4952534039) **Skykill** reported that their three.js case reproduced with a minimal CLI setup, filed issue #4612 with repro steps and analysis, and suggested cross-linking due to a potential common underlying cause
 * **RyanCavanaugh** added to milestone `Need More Info`
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/4520#issuecomment-5166782518) **talkstream** provided an additional data point for the memory leak issue, including environment details and OS-level snapshot measurements showing a tsgo process growing from 163 MB to over 3 GB across five days
 * [today](https://github.com/microsoft/TypeScript-go/issues/4520#issuecomment-5222954507) **jakebailey** explained that the @typescript/native-preview channel stopped publishing since TypeScript 7 GA shipping, noted that nightlies moved to the main typescript package, and advised capturing a heap profile via VS Code’s command palette for leaking processes

### [PR microsoft/TypeScript-go#4674](https://github.com/microsoft/TypeScript-go/pull/4674) (Open, `Voight-Kampff Anomaly`)

**Preserve JSDoc @property comments when reconstructing typedef types**

*Preserve JSDoc @property comments on typedefs when reconstructing inline types in generated .d.ts files.*

 * created by **veksa**
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4674#issuecomment-5016285782) **veksa** said "@microsoft-github-policy-service agree"
 * **RyanCavanaugh** added label `Voight-Kampff Anomaly`

### [Issue microsoft/TypeScript-go#4748](https://github.com/microsoft/TypeScript-go/issues/4748) (Open, `Needs Investigation`, **weswigham**)

**Panic: nil pointer in NodeList\.HasTrailingComma during incremental rebuild \(build\-mode declaration printer\) — 7\.0\.2 and current nightly**

*A nil pointer dereference in NodeList.HasTrailingComma triggers a panic during incremental build-mode declaration printing in TypeScript.*

 * **RyanCavanaugh** added to milestone `Need More Info`
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/4748#issuecomment-5121048546) **RyanCavanaugh** requested repro steps and suggested bisecting to an anonymized code subset
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/4748#issuecomment-5209111655) **nikeedw** described root cause with a two-file minimal repro, proposed a fix in PR #4842, and requested maintainers’ judgment
 * [today](https://github.com/microsoft/TypeScript-go/issues/4748#issuecomment-5220700380) **RyanCavanaugh** warned against sending a PR without signing the CLA, closed the PR without reviewing it, and said it would be archived before automated resolution
 * [today](https://github.com/microsoft/TypeScript-go/issues/4748#issuecomment-5221620947) **nikeedw** provided an update on CLA signing and apologized for the churn; resubmitted the branch as PR #4846 and offered maintainers to re-derive the fix if preferred

### [Issue microsoft/TypeScript-go#4802](https://github.com/microsoft/TypeScript-go/issues/4802) (Closed)

**workspace/symbol returns results from projects outside the workspace folder**

*The TypeScript language server’s workspace/symbol command erroneously returns symbols from external project folders, leading to duplicates, slow queries, and high memory usage.*

 * created by **stewartmcgown**
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/4802#issuecomment-5145002995) **jakebailey** said "We were missing js/ts.workspaceSymbols.scope support; #4805 adds it, at the expense of an LSP extension."
 * **RyanCavanaugh** added to milestone `Possible Improvement`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4805](https://github.com/microsoft/TypeScript-go/pull/4805) (Closed)

**Support js/ts\.workspaceSymbols\.scope and extra textDocument param on workspace/symbol request**

*Add js/ts.workspaceSymbols.scope support and an extra textDocument parameter to filter workspace symbol requests to a document’s projects.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4805#issuecomment-5222971090) **jakebailey** said "Going to merge this, but, it won't work until we do another extension publish. So it won't yet be "fixed"."
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4806](https://github.com/microsoft/TypeScript-go/issues/4806) (Closed, `Crash`, `Needs Investigation`, **johnfav03**)

**LSP watcher panics when Close races with WatchFiles**

*TypeScript LSP file watcher's concurrent Close and WatchFiles calls race, triggering a panic from nil map assignment.*

 * (1 week ago) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.1`, and assigned to **johnfav03**
 * (today) **johnfav03** closed the issue

### [Issue microsoft/TypeScript-go#4809](https://github.com/microsoft/TypeScript-go/issues/4809) (Open, `Crash`, **jakebailey**, **Copilot**)

**LSP exits when parent process PID is not found**

*LSP’s parent-PID watchdog terminates the server when the PID can’t be found in Docker, with a CLI flag to disable it.*

 * **jakebailey** assigned to **jakebailey**
 * **RyanCavanaugh** added to milestone `Post-7.0`
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/4809#issuecomment-5181165788) **mj026** noted that vscode language servers have similar behavior with a parent process watchdog and suggested using the --clientProcessId option instead of removing it; offered to provide a PR
 * [today](https://github.com/microsoft/TypeScript-go/issues/4809#issuecomment-5222278230) **jakebailey** said "How does that help your case? If you're launching in docker, how would you know the PID ahead of time if it's inside a container or something?"

### [PR microsoft/TypeScript-go#4823](https://github.com/microsoft/TypeScript-go/pull/4823) (Closed, **RyanCavanaugh**, **Copilot**)

**Preserve await context for exported classes in nested containers**

*Restrict await context for exported classes to top-level declarations while preserving it within async functions and generators.*

 * **Copilot** assigned to **RyanCavanaugh**
 * [4 days ago](https://github.com/microsoft/TypeScript-go/pull/4823#issuecomment-5171393580) **Copilot** explained that export class was removed from invalid test locations and updated tests to use plain class in nested contexts while retaining export class only where syntactically legal
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/4823#issuecomment-5182341856) **RyanCavanaugh** said "This fixes microsoft/TypeScript#63712"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4823#issuecomment-5222479639) **RyanCavanaugh** said "@copilot address code review comments"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4823#issuecomment-5222723233) **Copilot** addressed review feedback by extending the testcase with static-member coverage and updating baselines
 * [today](https://github.com/microsoft/TypeScript-go/pull/4823#issuecomment-5223410523) **RyanCavanaugh** said "@copilot CI is failing, and use a proper bit test as suggested"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4823#issuecomment-5223523155) **Copilot** updated bitwise context checks per suggestion in commit e7130af9 and clarified the CI failure was due to a transient Go download error

### [PR microsoft/TypeScript-go#4825](https://github.com/microsoft/TypeScript-go/pull/4825) (Open)

**Fix deprecated contextual property memory regression**

*Update deprecation diagnostics to prevent memory ballooning from deferred processing and discard duplicate entries.*

 * [4 days ago](https://github.com/microsoft/TypeScript-go/pull/4825#issuecomment-5175249558) **jakebailey** confirmed that it worked while using more memory and requested the TypeScript bot to run a performance test
 * [4 days ago](https://github.com/microsoft/TypeScript-go/pull/4825#issuecomment-5175250058) **typescript-automation[bot]** indicated that performance tests started and provided links to status and results
 * [4 days ago](https://github.com/microsoft/TypeScript-go/pull/4825#issuecomment-5175461378) **typescript-automation[bot]** posted requested perf run results
 * [today](https://github.com/microsoft/TypeScript-go/pull/4825#issuecomment-5221609904) **jakebailey** said "Part of the problem with the checker diags is that we add them and then modify them, which makes deduping sort of annoying. We could fix that, though."
 * [today](https://github.com/microsoft/TypeScript-go/pull/4825#issuecomment-5222030816) **jakebailey** said "I took a stab at it. PTAL"

### [Issue microsoft/TypeScript-go#4831](https://github.com/microsoft/TypeScript-go/issues/4831) (Open, `Needs More Info`)

**High CPU Usage in Editor \(and Controls for LSP\)**

*Wants a built-in CPU usage limit flag for tsgo's LSP mode to prevent high CPU spikes on low-end laptops.*

 * created by **DanielRosenwasser**
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/4831#issuecomment-5188485799) **DanielRosenwasser** said "@glav-git have you taken a profile to see what the cause is? Totally freezing your machine is extreme and unexpected."
 * **DanielRosenwasser** added label `Needs More Info`
 * **RyanCavanaugh** added to milestone `Need More Info`

### [Issue microsoft/TypeScript-go#4838](https://github.com/microsoft/TypeScript-go/issues/4838) (Closed, `Needs Investigation`, **johnfav03**)

**\`tsc \-\-watch\` can't handle errors across files**

*TypeScript’s watch mode fails to detect cross-file errors when a variable declaration is removed in a dependent file.*

 * created by **Withered-Flower-0422**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `Post-7.0`, and assigned to **johnfav03**

### [PR microsoft/TypeScript-go#4841](https://github.com/microsoft/TypeScript-go/pull/4841) (Open, **weswigham**)

**Fix false\-positive TS2354 for native private class field access with importHelpers at dated targets**

*With importHelpers enabled and a dated ECMAScript target, the Go port of TypeScript wrongly reports TS2354 on native private class field access.*

 * created by **astegmaier**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4841#issuecomment-5209140467) **astegmaier** noted that the PR contained the discussed bug fix and disclosed that the reproduction was hand-crafted while the PR itself was agent-generated
 * **RyanCavanaugh** assigned to **weswigham**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4841#issuecomment-5222455672) **astegmaier** verified a regression, pushed a fix restoring the check for native class decorators with static private/auto-accessor elements, retained the original improvements, and added three new tests

### [PR microsoft/TypeScript-go#4842](https://github.com/microsoft/TypeScript-go/pull/4842) (Closed)

**Fix crash when a call signature's type parameter cannot be reused**

*Call signature type parameter reuse failure currently produces nil AST nodes unchecked, causing a printer crash.*

 * created by **nikeedw**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4842#issuecomment-5215747276) **nikeedw** thanked CI for green results, declined to sign the CLA, suggested treating the PR as a proposal rather than merging, and noted the change may only address a symptom
 * (today) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/4842#issuecomment-5221610012) **nikeedw** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4842#issuecomment-5221622351) **nikeedw** stated that they had signed the CLA, apologized for their mistake, noted that the PR was superseded by another one and could not be reopened, and linked to related context

### [Issue microsoft/TypeScript-go#4844](https://github.com/microsoft/TypeScript-go/issues/4844) (Closed)

**CONTRIBUTING\.md out of date**

*CONTRIBUTING.md still limits acceptable changes to TypeScript 6.0/7.0 differences even though TypeScript 7.0 has been officially released.*

 * created by **eagarwal-notion**

### [PR microsoft/TypeScript-go#4845](https://github.com/microsoft/TypeScript-go/pull/4845) (Closed)

**Fix LSP Watcher panic when Close races with WatchFiles**

*A race between WatchFiles and Close in the LSP Watcher can cause a panic by writing to a nil watch map after reconcile.*

 * created by **johnfav03**
 * (today) **johnfav03** closed the issue

### [PR microsoft/TypeScript-go#4846](https://github.com/microsoft/TypeScript-go/pull/4846) (Open)

**Fix crash when a call signature's type parameter cannot be reused**

*A printer dereference crash occurs when pseudoTypeToNode’s SingleCallSignature branch appends a nil type parameter from reuseNode without fallback.*

 * created by **nikeedw**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4846#issuecomment-5222019357) **nikeedw** noted that the crash site was previously fixed by PR #3485 with a similar pattern and that this PR applies the same fix to another node-builder path, but warned that other producers could still yield nil and suggested a more general solution might be needed
 * [today](https://github.com/microsoft/TypeScript-go/pull/4846#issuecomment-5222176600) **nikeedw** provided a detailed static and dynamic survey showing that on main, NodeList constructions produce no nil elements in the test suite and only one nil in the two-file repro scenario

### [PR microsoft/TypeScript-go#4847](https://github.com/microsoft/TypeScript-go/pull/4847) (Open, `Voight-Kampff Anomaly`)

**fix: allow destructured require under module preserve \+ verbatimModuleSyntax**

*Allow destructured require calls in CommonJS modules under --module preserve and --verbatimModuleSyntax by adjusting alias checks to prevent TS1293 errors.*

 * created by **sankalpsthakur**

### [PR microsoft/TypeScript-go#4848](https://github.com/microsoft/TypeScript-go/pull/4848) (Closed)

**Fix watch diagnostics when global declaration is removed**

*Watch mode now rechecks all affected files when a global declaration is removed to prevent stale diagnostics*

 * created by **johnfav03**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4848#issuecomment-5222109644) **jakebailey** asked to split the PR into two commits, first adding the test and baseline and then the fix with the baseline update

### [PR microsoft/TypeScript-go#4849](https://github.com/microsoft/TypeScript-go/pull/4849) (Closed)

**Port transpileModule, transpileDeclaration**

*Port the TS API’s transpileModule, transpileModuleFromFile, transpileDeclaration, and transpileDeclarationFromFile functions.*

 * created by **andrewbranch**

### [Issue microsoft/TypeScript-go#4850](https://github.com/microsoft/TypeScript-go/issues/4850) (Open, `Needs Investigation`, **weswigham**)

**Difference in behavior of enum used as field key in emit vs non\-emit type check**

*Enum-based record keys resolve as enum types internally but emit as string literals in declaration files.*

 * created by **chriskrycho**

### [Issue microsoft/TypeScript-go#4851](https://github.com/microsoft/TypeScript-go/issues/4851) (Open, `Needs Investigation`, **johnfav03**)

**\[ServerErrors\]\[TypeScript\] main vs **

*The Azure pipeline run on TypeScript's main branch analyzed 300 popular GitHub repositories, detected 27 changes, and encountered multiple timeouts, clone failures, and unknown errors.*

 * created by **typescript-automation[bot]**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4851#issuecomment-5223442669) **typescript-automation[bot]** reported a runtime panic due to index out of range with a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/4851#issuecomment-5223442715) **typescript-automation[bot]** reported a panic handling textDocument/diagnostic request and provided stack trace, affected repo, and replay commands
 * [today](https://github.com/microsoft/TypeScript-go/issues/4851#issuecomment-5223442770) **typescript-automation[bot]** reported a panic in textDocument/diagnostic with a stack trace for the siyuan-note/siyuan repo
 * [today](https://github.com/microsoft/TypeScript-go/issues/4851#issuecomment-5223442811) **typescript-automation[bot]** reported a panic due to an unhandled node kind in the JSX initializer
 * [today](https://github.com/microsoft/TypeScript-go/issues/4851#issuecomment-5223442853) **typescript-automation[bot]** reported a panic in textDocument/diagnostic request with stack trace and affected repo transloadit/uppy
 * [today](https://github.com/microsoft/TypeScript-go/issues/4851#issuecomment-5223442885) **typescript-automation[bot]** reported a panic during textDocument/diagnostic handling with a detailed stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/4851#issuecomment-5223442922) **typescript-automation[bot]** reported a server connection closed prematurely error and provided repro steps for vercel/ai
 * [today](https://github.com/microsoft/TypeScript-go/issues/4851#issuecomment-5223442965) **typescript-automation[bot]** reported that the server connection closed prematurely and included affected repo details, last requests, and repro steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/4851#issuecomment-5223442995) **typescript-automation[bot]** reported a server connection closed prematurely error and provided affected repo details and repro steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/4851#issuecomment-5223443037) **typescript-automation[bot]** reported server connection closed prematurely error for stablyai/orca and provided repro steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/4851#issuecomment-5223443088) **typescript-automation[bot]** reported a server connection closed prematurely error for KeygraphHQ/shannon and provided raw error details, replay commands, and repro steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/4851#issuecomment-5223443160) **typescript-automation[bot]** reported that the server connection closed prematurely with undefined error and provided affected repo details, last requests, and repro steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/4851#issuecomment-5223443247) **typescript-automation[bot]** reported premature server connection closure error with undefined for freeCodeCamp/freeCodeCamp and included error artifacts, last requests, and repro steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/4851#issuecomment-5223443309) **typescript-automation[bot]** reported a panic in textDocument/diagnostic for sequelize/sequelize with stack trace and artifact links
 * [today](https://github.com/microsoft/TypeScript-go/issues/4851#issuecomment-5223443362) **typescript-automation[bot]** reported a panic during textDocument/diagnostic request and logged a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/4851#issuecomment-5223443422) **typescript-automation[bot]** reported a panic error in JSX transformer with a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/4851#issuecomment-5223443481) **typescript-automation[bot]** reported a panic in handling textDocument/diagnostic with a stack trace and affected repo details

### [PR microsoft/TypeScript-go#4852](https://github.com/microsoft/TypeScript-go/pull/4852) (Open)

**Preserve enum computed property names in declarations**

*Retain enum computed property names in declarations to prevent inlining values from breaking enum types.*

 * created by **jakebailey**

