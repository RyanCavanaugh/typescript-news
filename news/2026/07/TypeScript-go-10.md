# Report for 2026-07-10 (Friday, July 10th, 2026)

15 different users commented on 26 different issues.

## Recommended Actions

 * Response Recommended
    * @safal207 provided detailed repro steps and environment as requested in [microsoft/TypeScript-go#1493](https://github.com/microsoft/TypeScript-go/issues/1493#issuecomment-4944032445)
    * @ayosec asked if the issue should be moved to the microsoft/TypeScript repository in [microsoft/TypeScript-go#4583](https://github.com/microsoft/TypeScript-go/issues/4583#issuecomment-4938532006)
    * @ibesuperv asked if further tweaks are needed in [microsoft/TypeScript-go#4589](https://github.com/microsoft/TypeScript-go/issues/4589#issuecomment-4944241900)
    * @typescript-automation[bot] provided performance results as requested in [microsoft/TypeScript-go#4591](https://github.com/microsoft/TypeScript-go/pull/4591#issuecomment-4938930752)
    * @typescript-automation provided test results for the top 1000 repos in [microsoft/TypeScript-go#4591](https://github.com/microsoft/TypeScript-go/pull/4591#issuecomment-4939528081)
    * @typescript-automation[bot] reported a panic in textDocument/hover that needs investigation in [microsoft/TypeScript-go#4601](https://github.com/microsoft/TypeScript-go/issues/4601#issuecomment-4940320848)
    * @typescript-automation[bot] reported a panic handling textDocument/rangeFormatting request in [microsoft/TypeScript-go#4601](https://github.com/microsoft/TypeScript-go/issues/4601#issuecomment-4940320878)
    * @typescript-automation[bot] reported a premature server connection closure for slopus/happy in [microsoft/TypeScript-go#4601](https://github.com/microsoft/TypeScript-go/issues/4601#issuecomment-4940320910)
    * @typescript-automation[bot] reported a server connection closed prematurely error in [microsoft/TypeScript-go#4601](https://github.com/microsoft/TypeScript-go/issues/4601#issuecomment-4940320933)
    * @typescript-automation[bot] reported a premature server connection closure for babel/babel in [microsoft/TypeScript-go#4601](https://github.com/microsoft/TypeScript-go/issues/4601#issuecomment-4940320969)
    * @typescript-automation[bot] provided repro steps as requested in [microsoft/TypeScript-go#4601](https://github.com/microsoft/TypeScript-go/issues/4601#issuecomment-4940320996)
    * @typescript-automation[bot] reported a server connection closed prematurely error for strapi/strapi in [microsoft/TypeScript-go#4601](https://github.com/microsoft/TypeScript-go/issues/4601#issuecomment-4940321025)

## Activity Summary

### [Issue microsoft/TypeScript-go#1493](https://github.com/microsoft/TypeScript-go/issues/1493) (Open, `Domain: CLI`, **jakebailey**, **Copilot**)

**Exit code for type error is incorrect starting from \`7\.0\.0\-dev\.20250724\.1\`**

*tsgo in @typescript/native-preview@7.0.0-dev.20250724.1 returns exit code 1 for type errors instead of the expected code 2.*

 * **RyanCavanaugh** added to milestone `TypeScript 7.0 Stable`
 * (2 days ago) **jakebailey** set milestone to `Post-7.0`, and removed from milestone `TypeScript 7.0 Stable`
 * [later](https://github.com/microsoft/TypeScript-go/issues/1493#issuecomment-4944032445) **safal207** reported that the exit-status difference still reproduces with TypeScript 7.0.2 on all GitHub-hosted OS and provided detailed environment, test profile, and evidence confirming stability for issue #4407

### [PR microsoft/TypeScript-go#3102](https://github.com/microsoft/TypeScript-go/pull/3102) (Open, **DanielRosenwasser**)

**Fix a formatting crash caused by template literal in parser\-recovered property signature**

*Process grammar error nodes to correctly handle template literals in recovered property signatures and prevent formatting crashes.*

 * [1 month ago](https://github.com/microsoft/TypeScript-go/pull/3102#issuecomment-4665116908) **DanielRosenwasser** said "Unfortunately we've got merge conflicts. 🙁"
 * (1 month ago) **RyanCavanaugh** set milestone to `Post-7.0`, and removed from milestone `TypeScript 7.0 RC`
 * [today](https://github.com/microsoft/TypeScript-go/pull/3102#issuecomment-4939912425) **Andarist** said "@DanielRosenwasser I missed the notification in what was a particularly busy month for me - I just fixed those conflicts"

### [PR microsoft/TypeScript-go#4270](https://github.com/microsoft/TypeScript-go/pull/4270) (Closed, **DanielRosenwasser**, **Copilot**)

**Fix fatal error when project reference objects have unexpected types for path and circular**

*Add safe type checks and diagnostics for invalid tsconfig reference paths and circular flags to prevent panics.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4270#issuecomment-4710324046) **Copilot** described adding noEmit and noTypesAndSymbols to the test, removing unnecessary baselines, and explained why no error is emitted in the sourceFile path
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4270#issuecomment-4710457353) **DanielRosenwasser** said "@copilot no the feedback was about issuing error messages when it makes sense to do so. The baselines were fine."
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4270#issuecomment-4710800183) **Copilot** implemented source-location diagnostics for non-string reference.path in tsconfig and updated the test harness to include config file parsing diagnostics, capturing pre-existing baseline drifts
 * (today) **DanielRosenwasser** closed the issue

### [Issue microsoft/TypeScript-go#4462](https://github.com/microsoft/TypeScript-go/issues/4462) (Open, `bug`, **ahejlsberg**)

**Regression \(7\.0\.0\-dev\.20260624\.1\): intersection type member dropped in generic position — TanStack Router \`stripSearchParams\` rejected \(TS2322\), clean in tsc \+ 20260623\.1**

*Upgrading to @typescript/native-preview 7.0.0-dev.20260624.1 drops members from intersection types in generics, triggering TS2322 errors in TanStack Router.*

 * **ahejlsberg** assigned to **ahejlsberg**
 * (3 days ago) **RyanCavanaugh** added label `Needs Investigation`, and set milestone to `Post-7.0`
 * (today) **ahejlsberg** added label `bug`, and removed label `Needs Investigation`

### [Issue microsoft/TypeScript-go#4583](https://github.com/microsoft/TypeScript-go/issues/4583) (Open)

**Some colors make error messages hard to read on white backgrounds\.**

*Diagnosticwriter’s forced bright ANSI color codes make error messages illegible on white backgrounds and should use default colors instead.*

 * created by **ayosec**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4583#issuecomment-4934491424) **jakebailey** questioned whether the issue was new in v7 and linked to existing code
 * [today](https://github.com/microsoft/TypeScript-go/issues/4583#issuecomment-4938532006) **ayosec** noted that the issue also existed in the original compiler and asked if it should be moved to the microsoft/TypeScript repository

### [PR microsoft/TypeScript-go#4586](https://github.com/microsoft/TypeScript-go/pull/4586) (Open, **RyanCavanaugh**, **Copilot**)

**Fix TS2871 false positive for \`??\` operator in nullish coalescing check**

*Modify getSyntacticNullishnessSemantics to separate '??' and '??=' semantics from right controls and eliminate TS2871 false positives.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4586#issuecomment-4937552329) **RyanCavanaugh** said "This is a fix for https://github.com/microsoft/TypeScript/issues/63642"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4586#issuecomment-4937619051) **Copilot** replaced the test case with the minimal repro from the issue comment and updated baselines

### [Issue microsoft/TypeScript-go#4587](https://github.com/microsoft/TypeScript-go/issues/4587) (Open)

**TSX files do not report TypeScript diagnostics, while TS files work correctly \(autocomplete still works\)**

*Enabling tsgo in VS Code’s TypeScript 7 extension causes .tsx files to omit diagnostics while .ts files report errors normally.*

 * created by **pedroGoffi**

### [Issue microsoft/TypeScript-go#4589](https://github.com/microsoft/TypeScript-go/issues/4589) (Open, `Domain: Editor`)

**workspace/diagnostic/refresh is triggered for watch events that cannot affect type checking**

*The VS Code TypeScript language server erroneously triggers diagnostic refreshes for unrelated .svg file changes in node_modules.*

 * created by **mjbvz**
 * **mjbvz** added label `Domain: Editor`
 * [later](https://github.com/microsoft/TypeScript-go/issues/4589#issuecomment-4944241900) **ibesuperv** opened PR #4604 to optimize the Session.DidChangeWatchedFiles path by filtering out irrelevant extensions while preserving cache-invalidation invariants and asked if further tweaks were needed

### [PR microsoft/TypeScript-go#4590](https://github.com/microsoft/TypeScript-go/pull/4590) (Open)

**Fix "Token end is child end" crash on grammar error**

*Formatter crashes due to skipping grammar-error child nodes without advancing the scanner, causing mismatched token and AST child end positions.*

 * created by **johnfav03**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4590#issuecomment-4939918614) **Andarist** said "note that my old PR already fixes this too: https://github.com/microsoft/typescript-go/pull/3102 . I just pushed out the test from this PR there"

### [PR microsoft/TypeScript-go#4591](https://github.com/microsoft/TypeScript-go/pull/4591) (Open)

**Sort by type depth in \`inferFromMatchingTypes\` function**

*Sort matching types by nesting depth in the inferFromMatchingTypes function to resolve regressions such as #4462.*

 * created by **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4591#issuecomment-4938758972) **ahejlsberg** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4591#issuecomment-4938759482) **typescript-automation[bot]** reported that performance test jobs started and provided links to the build and results
 * [today](https://github.com/microsoft/TypeScript-go/pull/4591#issuecomment-4938761201) **ahejlsberg** said "@typescript-bot test top1000"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4591#issuecomment-4938761691) **typescript-automation[bot]** reported build jobs starting and completion status with result links
 * **ahejlsberg** added to milestone `Post-7.0`
 * [today](https://github.com/microsoft/TypeScript-go/pull/4591#issuecomment-4938930752) **typescript-automation[bot]** provided the requested performance run results
 * [today](https://github.com/microsoft/TypeScript-go/pull/4591#issuecomment-4939528081) **typescript-automation[bot]** reported that running tsc on the top 1000 repos showed no issues comparing main and the pull request merge

### [PR microsoft/TypeScript-go#4592](https://github.com/microsoft/TypeScript-go/pull/4592) (Open)

**Improve responsiveness of \`tsc build\` to interruption**

*Improve tsc and tsc build interruption responsiveness by threading cancellation context for prompt aborts and correct exit codes.*

 * created by **lukesandberg**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4592#issuecomment-4939791695) **lukesandberg** said "@microsoft-github-policy-service agree [company="Vercel"]"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4592#issuecomment-4939873881) **lukesandberg** agreed that the company was Vercel

### [Issue microsoft/TypeScript-go#4593](https://github.com/microsoft/TypeScript-go/issues/4593) (Open, `Domain: Editor`)

**File change events always trigger project recheck even if file content hasn't actually changed**

*File watcher change events for unchanged files always trigger a full TypeScript project recheck.*

 * created by **mjbvz**
 * **mjbvz** added label `Domain: Editor`

### [PR microsoft/TypeScript-go#4594](https://github.com/microsoft/TypeScript-go/pull/4594) (Open)

**Fix "Token end is child end" crash when range formatting is inside a JSDoc comment**

*Formatting inside JSDoc causes the scanner to parse backticks as an unclosed template literal, crashing on token end mismatch.*

 * created by **johnfav03**

### [Issue microsoft/TypeScript-go#4595](https://github.com/microsoft/TypeScript-go/issues/4595) (Open, `Domain: Editor`, **johnfav03**)

**File watch events can cause a check/cancel/re\-check storm**

*Batch file watch events in a TypeScript project trigger repeated diagnostic cancellations and re-checks, leading to sustained high CPU usage.*

 * created by **mjbvz**
 * **mjbvz** added label `Domain: Editor`
 * **RyanCavanaugh** assigned to **johnfav03**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4595#issuecomment-4939520056) **RyanCavanaugh** said "@mjbvz I thought I was done getting editor bugs from you! 😜"
 * [today](https://github.com/microsoft/TypeScript-go/issues/4595#issuecomment-4940126284) **mjbvz** said "Ha sorry but looks like you're still stuck with me. Always finding new ways to stress test TypeScript 🙃 "

### [PR microsoft/TypeScript-go#4596](https://github.com/microsoft/TypeScript-go/pull/4596) (Open)

**Fixed mapped types not being considered as homomorphic with substitution constraints**

*Mapped types are now correctly recognized as homomorphic when using substitution constraints in TypeScript.*

 * created by **Andarist**

### [PR microsoft/TypeScript-go#4597](https://github.com/microsoft/TypeScript-go/pull/4597) (Open)

**Normalize \`NoInfer\`red tuple types in rest/spread positions**

*Normalize NoInferred tuple types used in rest and spread operations to resolve related TypeScript inference issues.*

 * created by **Andarist**

### [PR microsoft/TypeScript-go#4598](https://github.com/microsoft/TypeScript-go/pull/4598) (Open)

**Fix optionality stripping when mapping over tuples under EOPT**

*Ensure mapping over tuples under EOPT preserves optionality instead of incorrectly stripping it*

 * created by **Andarist**

### [PR microsoft/TypeScript-go#4599](https://github.com/microsoft/TypeScript-go/pull/4599) (Open)

**Fix crash in CFA when for loop initializer throws**

*Control flow analysis crashes when a for loop initializer throws an exception.*

 * created by **Andarist**

### [PR microsoft/TypeScript-go#4600](https://github.com/microsoft/TypeScript-go/pull/4600) (Open)

**Deduplicate repeated declarations on union/intersection properties**

*Remove duplicate property declarations from union and intersection types.*

 * created by **Andarist**

### [Issue microsoft/TypeScript-go#4601](https://github.com/microsoft/TypeScript-go/issues/4601) (Open)

**\[ServerErrors\]\[TypeScript\] main vs **

*Server errors were reported on the main TypeScript branch during an Azure pipeline run analyzing 300 popular GitHub repositories.*

 * created by **typescript-automation[bot]**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4601#issuecomment-4940320848) **typescript-automation[bot]** reported a panic handling request textDocument/hover with a debug failure
 * [today](https://github.com/microsoft/TypeScript-go/issues/4601#issuecomment-4940320878) **typescript-automation[bot]** reported a panic during textDocument/rangeFormatting due to a debug failure and provided a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/4601#issuecomment-4940320910) **typescript-automation[bot]** reported a server connection closed prematurely with undefined error for slopus/happy and provided error artifacts, replay commands, and repro steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/4601#issuecomment-4940320933) **typescript-automation[bot]** reported a server connection closed prematurely error for drizzle-team/drizzle-orm with error details and repro steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/4601#issuecomment-4940320969) **typescript-automation[bot]** reported that the server connection closed prematurely with an undefined error for the babel/babel repo
 * [today](https://github.com/microsoft/TypeScript-go/issues/4601#issuecomment-4940320996) **typescript-automation[bot]** reported a premature server connection closure error and provided logs, artifact links, and repro steps for cypress-io/cypress
 * [today](https://github.com/microsoft/TypeScript-go/issues/4601#issuecomment-4940321025) **typescript-automation[bot]** reported a server connection closed prematurely error for strapi/strapi

### [PR microsoft/TypeScript-go#4602](https://github.com/microsoft/TypeScript-go/pull/4602) (Open)

**fix\(lsp\): respect editor formatting in organize imports**

*Update the organize imports function to apply the editor's tabSize and indentation settings.*

 * created by **TorinAsakura**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4602#issuecomment-4942220540) **jakebailey** questioned why the existing code using LS formatting options did not work and why patching the LSP with middlewares was necessary
 * [later](https://github.com/microsoft/TypeScript-go/pull/4602#issuecomment-4946957648) **TorinAsakura** noted that the custom plumbing was unnecessary and said they would strip it out, keeping only the small fix and regression test

### [PR microsoft/TypeScript-go#4603](https://github.com/microsoft/TypeScript-go/pull/4603) (Open)

**fix\(checker\): avoid computed enum member stack overflow**

*Prevent stack overflow by skipping dynamic computed enum member names in declared-type construction while preserving TS1164 errors.*

 * created by **ZhiyaoWen999**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4603#issuecomment-4942053581) **ZhiyaoWen999** said "@microsoft-github-policy-service agree"

### [PR microsoft/TypeScript-go#4604](https://github.com/microsoft/TypeScript-go/pull/4604) (Open)

**fix: prevent unnecessary diagnostic refreshes on irrelevant watch events \(\#4589\)**

*Optimize file watch handling by scheduling diagnostics refresh only for relevant TypeScript files and directories, reducing CPU and RPC overhead.*

 * created by **ibesuperv**

