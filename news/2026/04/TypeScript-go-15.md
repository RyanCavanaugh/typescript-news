# Report for 2026-04-15 (Wednesday, April 15th, 2026)

17 different users commented on 36 different issues.

## Recommended Actions

 * Response Recommended
    * @AndreiTS asked where to send a video and a private repo with the problem in [microsoft/TypeScript-go#2780](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-4259962263)
    * @cupro29 asked to reopen the issue in [microsoft/TypeScript-go#3251](https://github.com/microsoft/TypeScript-go/issues/3251#issuecomment-4261474389)
    * @sbking reported a memory leak in VSCode TypeScript Native Preview in [microsoft/TypeScript-go#3423](https://github.com/microsoft/TypeScript-go/issues/3423#issuecomment-4261327047)
    * @sbking provided requested heap profile attachments for diffing in [microsoft/TypeScript-go#3423](https://github.com/microsoft/TypeScript-go/issues/3423#issuecomment-4261450546)
    * @sbking provided requested heap profile with the setting disabled in [microsoft/TypeScript-go#3423](https://github.com/microsoft/TypeScript-go/issues/3423#issuecomment-4261499932)

## Activity Summary

### [Issue microsoft/TypeScript-go#1894](https://github.com/microsoft/TypeScript-go/issues/1894) (Closed, `Domain: Editor`, **jakebailey**)

**Add semantic highlighting support for editors**

*Add support for semantic highlighting in editors to match the feature availability in VS Code.*

 * **mjbvz** added label `Domain: Editor`
 * (2 weeks ago) **DanielRosenwasser** set milestone to `TypeScript 7.0 RC`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#1990](https://github.com/microsoft/TypeScript-go/pull/1990) (Closed)

**Implement semantic tokens**

*Implement semantic tokens in the VS Code extension while coordinating multiple checker functionalities for doc highlights, diagnostics, and inlay hints.*

 * [21 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1990#issuecomment-3543481582) **jakebailey** said "Drafting this for now, until we can improve the checker situation IMO"
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1990#issuecomment-4166299067) **DanielRosenwasser** said "If you can add fuzzing support at https://github.com/microsoft/typescript-error-deltas that would be swell. I guess you'd have to wait for the next publish though?"
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1990#issuecomment-4166430646) **jakebailey** said "I'll look into the fuzzing, though this is sort of an irritating call due to the full/range/delta split"
 * [today](https://github.com/microsoft/TypeScript-go/pull/1990#issuecomment-4256465623) **azure-pipelines[bot]** reported that one pipeline was filtered out due to trigger conditions
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2115](https://github.com/microsoft/TypeScript-go/issues/2115) (Open, `possible improvement`)

**Refactor checker pool to limit checker creation for foreground tasks, segment diagnostic checkers**

*Refactor the checker pool to separate foreground and diagnostic tasks, minimizing redundant checker creation and resource usage*

 * created by **jakebailey**
 * (2 weeks ago) **RyanCavanaugh** added label `possible improvement`, and set milestone to `Possible Improvement`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2701](https://github.com/microsoft/TypeScript-go/issues/2701) (Closed)

**Declaration emit for named inferred types used in further inference inlines inferred types instead of naming them**

*tsgo inlines inferred types in declaration emit even when named, causing slower type checking in consuming packages.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2701#issuecomment-4137500062) **jakebailey** said "@chriskrycho Is this now fixed since #2459?"
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2701#issuecomment-4154924127) **RyanCavanaugh** mentioned that Nightly now emitted the expected code snippet
 * (2 weeks ago) **RyanCavanaugh** closed the issue
 * [later](https://github.com/microsoft/TypeScript-go/issues/2701#issuecomment-4259805234) **chriskrycho** checked notifications, began bumping to the latest nightly, and planned to switch the last package from tsc to tsgo after confirmation

### [Issue microsoft/TypeScript-go#2780](https://github.com/microsoft/TypeScript-go/issues/2780) (Open, `Domain: Editor`, `Needs More Info`, **andrewbranch**)

**High memory consumption in a large pnpm monorepo**

*PR #2502 causes minor edits in a large pnpm monorepo to spike the TypeScript extension memory from ~700MB to ~35GB.*

 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-4249139388) **shinichy** said "Ok. What would the fix look like? Do you still need access to the repo that reproduces the issue?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-4253201729) **andrewbranch** said "Yes, that's the only way I can make progress, unless I just happen to stumble upon the same root cause as your repro as I'm investigating other performance issues."
 * [later](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-4259962263) **AndreiTS** said "@andrewbranch I want to share a video and a private repo with this problem, where I can send you?"
 * [later](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-4261231001) **andrewbranch** said "{firstname}.{lastname}@microsoft.com. Thanks!"

### [Issue microsoft/TypeScript-go#3251](https://github.com/microsoft/TypeScript-go/issues/3251) (Closed, `Crash`, **DanielRosenwasser**, **Copilot**)

**Signature help assertion failure**

*An assertion failure in the Go language server's signature help getContainingArgumentInfo crashes without known repro steps, possibly tied to reparsing.*

 * **DanielRosenwasser** assigned to **DanielRosenwasser**
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3251#issuecomment-4248113395) **RyanCavanaugh** said "Closing in the absence of a repro"
 * (yesterday) **RyanCavanaugh** closed the issue
 * [later](https://github.com/microsoft/TypeScript-go/issues/3251#issuecomment-4261474389) **cupro29** demonstrated a repro using an invalid JSX snippet causing the LSP server to panic and requested reopening of the issue

### [PR microsoft/TypeScript-go#3289](https://github.com/microsoft/TypeScript-go/pull/3289) (Closed)

**Fix organize imports crash with traceResolution**

*Fixes the crash occurring during organize imports when traceResolution is enabled.*

 * created by **Andarist**
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript-go#3303](https://github.com/microsoft/TypeScript-go/pull/3303) (Closed)

**Restore fine\-grained ID errors**

*Store fine-grained ID inference errors in inferred types for precise quickfix location reporting.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3303#issuecomment-4254808629) **azure-pipelines[bot]** reported that one pipeline was filtered out due to trigger conditions
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3304](https://github.com/microsoft/TypeScript-go/pull/3304) (Closed)

**Add isolatedDeclarations quickfix**

*Port fourslash generator code to implement an isolatedDeclarations quickfix for improved code fixes.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3304#issuecomment-4255519093) **azure-pipelines[bot]** reported that one pipeline was filtered out due to trigger conditions
 * [today](https://github.com/microsoft/TypeScript-go/pull/3304#issuecomment-4255716916) **azure-pipelines[bot]** reported that one pipeline was filtered out due to trigger conditions
 * [today](https://github.com/microsoft/TypeScript-go/pull/3304#issuecomment-4255948741) **azure-pipelines[bot]** reported that one pipeline was filtered out due to trigger conditions
 * [today](https://github.com/microsoft/TypeScript-go/pull/3304#issuecomment-4256278017) **azure-pipelines[bot]** reported that one pipeline was filtered out due to trigger conditions
 * [today](https://github.com/microsoft/TypeScript-go/pull/3304#issuecomment-4256481763) **azure-pipelines[bot]** reported that one pipeline was filtered out due to trigger conditions
 * [today](https://github.com/microsoft/TypeScript-go/pull/3304#issuecomment-4256520200) **azure-pipelines[bot]** reported that one pipeline was filtered out due to trigger conditions
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3305](https://github.com/microsoft/TypeScript-go/pull/3305) (Open, **DanielRosenwasser**, **Copilot**)

**Add "Sort Imports" & "Remove Unused Imports" commands to VS Code extension**

*Register runtime handlers for sortImports and removeUnusedImports commands and adjust disposal order to prevent conflicts with the built-in TypeScript extension.*

 * created by **Copilot**
 * (2 weeks ago) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3305#issuecomment-4256048203) **azure-pipelines[bot]** reported that one pipeline was filtered out due to trigger conditions

### [Issue microsoft/TypeScript-go#3319](https://github.com/microsoft/TypeScript-go/issues/3319) (Open, **iisaduan**)

**Missing \`fixAll\` code action/code fix**

*VSCode’s TypeScript Go extension does not support the source.fixAll.ts code action or corresponding individual codefixes for editor.codeActionOnSave.*

 * created by **iisaduan**
 * **iisaduan** assigned to **iisaduan**
 * **RyanCavanaugh** added to milestone `Post-7.0`
 * [today](https://github.com/microsoft/TypeScript-go/issues/3319#issuecomment-4257481981) **jakebailey** said "Is this done with #3382? "

### [PR microsoft/TypeScript-go#3334](https://github.com/microsoft/TypeScript-go/pull/3334) (Open)

**Implement multi\-file doc highlights**

*Implement a new VS Code LSP extension method to support document highlights across multiple files.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3334#issuecomment-4254365695) **azure-pipelines[bot]** reported that one pipeline was filtered out due to trigger conditions

### [PR microsoft/TypeScript-go#3350](https://github.com/microsoft/TypeScript-go/pull/3350) (Closed)

**Fix dts porting bug**

*The DTS port misinterprets the syntax list as an external module indicator, although it causes no problems.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3355](https://github.com/microsoft/TypeScript-go/pull/3355) (Closed)

**Switch to new CI runner system**

*Adopt a new CI runner system to address current issues, leveraging its compatibility with our single-image pools.*

 * created by **jakebailey**
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3355#issuecomment-4195301938) **jakebailey** said "This won't work without a pool change (so far)"
 * [5 days ago](https://github.com/microsoft/TypeScript-go/pull/3355#issuecomment-4226977450) **jakebailey** said "This will fail until I can update the pool config, but I can't do that until nobody's running jobs, which sounds like a weekend merge."
 * [today](https://github.com/microsoft/TypeScript-go/pull/3355#issuecomment-4256396982) **azure-pipelines[bot]** reported that one pipeline was filtered out due to trigger conditions

### [PR microsoft/TypeScript-go#3363](https://github.com/microsoft/TypeScript-go/pull/3363) (Closed)

**Make LS checkers time out after being idle, segment based on use**

*Refactor the checker pool to categorize and configure diagnostic, temporary, and API checkers with idle-timeout cleanup via channels.*

 * [5 days ago](https://github.com/microsoft/TypeScript-go/pull/3363#issuecomment-4225848239) **jakebailey** mentioned that they fixed the comments but were uncertain how the changes should work for API users or tsgolint
 * [5 days ago](https://github.com/microsoft/TypeScript-go/pull/3363#issuecomment-4226698206) **jakebailey** said "@camc314 Do you know how this might affect your usage of these checkers? Is there some sort of setting that would make this not break you, if so?"
 * [4 days ago](https://github.com/microsoft/TypeScript-go/pull/3363#issuecomment-4229263846) **camc314** tested the branch on tsgolint and reported it worked fine
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3369](https://github.com/microsoft/TypeScript-go/pull/3369) (Closed)

**Limit loader/emitter to GOMAXPROCS**

*Limit loader and emitter concurrency to GOMAXPROCS to reduce overhead from excessive parallelism*

 * [5 days ago](https://github.com/microsoft/TypeScript-go/pull/3369#issuecomment-4227790293) **jakebailey** said "@typescript-bot perf test this faster"
 * [5 days ago](https://github.com/microsoft/TypeScript-go/pull/3369#issuecomment-4227790485) **typescript-bot** posted update indicating performance test jobs started with status links
 * [5 days ago](https://github.com/microsoft/TypeScript-go/pull/3369#issuecomment-4227905032) **typescript-bot** shared the requested performance run results
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3402](https://github.com/microsoft/TypeScript-go/pull/3402) (Closed)

**Support alternate spellings in JSDoc type annotations**

*Port getIntendedTypeFromJSDocTypeReference to support alternate spellings in JSDoc type annotations aligned with Strada*

 * created by **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3402#issuecomment-4255528331) **azure-pipelines[bot]** reported that one pipeline was filtered out due to trigger conditions
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#3404](https://github.com/microsoft/TypeScript-go/issues/3404) (Closed, `Domain: Editor`, **jakebailey**, **Copilot**)

**Object\-like type not formatted well with verbosity level 0 in hover**

*Hover tooltips for object types at verbosity level 0 show inline definitions instead of expected multiline formatting with newlines.*

 * **Withered-Flower-0422** added label `Domain: Editor`
 * (yesterday) **jakebailey** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3407](https://github.com/microsoft/TypeScript-go/pull/3407) (Closed, **jakebailey**, **Copilot**)

**Always format object\-like types multiline in hover**

*Always format object-like types across multiple lines in hover by enabling the multiline flag and updating printer output and tests.*

 * created by **Copilot**
 * (yesterday) **Copilot** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3407#issuecomment-4253903073) **jakebailey** said "@copilot+claude-opus-4.6 You should do npm run updatefailing, as you seem to have fixed more tests."
 * [today](https://github.com/microsoft/TypeScript-go/pull/3407#issuecomment-4254385587) **azure-pipelines[bot]** reported that one pipeline was filtered out due to trigger conditions
 * [today](https://github.com/microsoft/TypeScript-go/pull/3407#issuecomment-4254385675) **Copilot** updated failing tests by running npm run updatefailing and accepted new baselines for TestJsdocTypedefTagServices
 * [today](https://github.com/microsoft/TypeScript-go/pull/3407#issuecomment-4254398134) **azure-pipelines[bot]** reported that one pipeline was filtered out due to trigger conditions
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3409](https://github.com/microsoft/TypeScript-go/pull/3409) (Closed)

**Fix nil\-config project crash during project tree loading**

*A nil project configuration triggers a crash during project tree loading.*

 * created by **Andarist**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3409#issuecomment-4254796332) **gabritto** described a proposed fix for the fuzzer crash and noted confusion about how a nil command line could occur in the fuzzer
 * (today) **gabritto** closed the issue

### [Issue microsoft/TypeScript-go#3410](https://github.com/microsoft/TypeScript-go/issues/3410) (Open, `bug`, `Domain: Editor`, **weswigham**)

**Type serializer omits type arguments of outer functions**

*The tsgo type serializer drops outer function generic arguments when hovering on returned classes, displaying makeBox.Box instead of makeBox<string>.Box.*

 * (today) **ahejlsberg** added labels `bug`, `Domain: Editor`, and assigned to **weswigham**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3410#issuecomment-4253768345) **a-tarasyuk** asked whether it was acceptable to restore the previous emitter behavior using temporary identifier-attached type arguments via setIdentifierTypeArguments or if a different approach should be used, referencing a related code segment
 * [today](https://github.com/microsoft/TypeScript-go/issues/3410#issuecomment-4253846287) **jakebailey** suggested using ExpressionWithTypeArguments as a modern fix, noting the old approach relied on weird mutations and that printing predates instantiation expressions
 * [today](https://github.com/microsoft/TypeScript-go/issues/3410#issuecomment-4253860186) **ahejlsberg** agreed that using ExpressionWithTypeArguments was the modern fix
 * [today](https://github.com/microsoft/TypeScript-go/issues/3410#issuecomment-4254159917) **weswigham** agreed on using ExpressionWithTypeArguments and suggested adding a node builder flag and leveraging the existing AST for type argument data

### [PR microsoft/TypeScript-go#3412](https://github.com/microsoft/TypeScript-go/pull/3412) (Open)

**fix\(3410\): preserve type arguments in hover for qualified names**

*Qualified name hover tooltips now correctly display preserved type arguments.*

 * created by **a-tarasyuk**

### [Issue microsoft/TypeScript-go#3413](https://github.com/microsoft/TypeScript-go/issues/3413) (Open, `Domain: JS`, `Domain: Parser`, **ahejlsberg**)

**\`?\` can be used as a standalone JSDoc type when followed by \`\|\`**

*? used standalone in JSDoc unions is treated as null or never, resulting in unexpected type inference.*

 * created by **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3413#issuecomment-4255533409) **DanielRosenwasser** explained that supporting prefix '?' and '!' in JSDoc and a leading '|' operator made standalone '?' invalid and caused it to swallow the union type to its right
 * (today) **DanielRosenwasser** added labels `Domain: Parser`, `Domain: JS`, and assigned to **ahejlsberg**

### [PR microsoft/TypeScript-go#3414](https://github.com/microsoft/TypeScript-go/pull/3414) (Open)

**Update CHANGES\.md to reflect that JSDoc types still permit postfix/prefix \`?\`/\`\!\`\.**

*Update CHANGES.md to note that JSDoc type annotations continue to allow prefix and postfix '?' and '!' modifiers.*

 * created by **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3414#issuecomment-4255572022) **azure-pipelines[bot]** reported that one pipeline was filtered out due to trigger conditions

### [PR microsoft/TypeScript-go#3415](https://github.com/microsoft/TypeScript-go/pull/3415) (Closed)

**Add VS client caps, use VS diagnostic format when asked**

*Add support for Visual Studio client capabilities and enable Visual Studio diagnostic formatting on demand.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3415#issuecomment-4256385100) **azure-pipelines[bot]** reported that one pipeline was filtered out due to trigger conditions
 * [today](https://github.com/microsoft/TypeScript-go/pull/3415#issuecomment-4256417310) **azure-pipelines[bot]** reported that one pipeline was filtered out due to trigger conditions
 * [today](https://github.com/microsoft/TypeScript-go/pull/3415#issuecomment-4257460709) **jakebailey** said "/azp where"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3415#issuecomment-4257461045) **azure-pipelines[bot]** notified that Azure DevOps orgs were getting events for this repository

### [Issue microsoft/TypeScript-go#3416](https://github.com/microsoft/TypeScript-go/issues/3416) (Closed, `Domain: Editor`, **jakebailey**)

**isolatedDeclarations quickfix: Parens not added to single arrow func param**

*The isolatedDeclarations quickfix incorrectly adds type annotations to single arrow function parameters without parentheses, producing invalid syntax.*

 * created by **RyanCavanaugh**
 * (today) **RyanCavanaugh** added label `Domain: Editor`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3416#issuecomment-4257561923) **jakebailey** reported that the bug was preexisting and provided a TS Playground link

### [Issue microsoft/TypeScript-go#3417](https://github.com/microsoft/TypeScript-go/issues/3417) (Closed, `Domain: Editor`)

**Default type param not displayed in hover**

*Hover tooltip in tsgo extension omits default type parameter for generic types compared to TS6.0*

 * created by **Withered-Flower-0422**
 * **Withered-Flower-0422** added label `Domain: Editor`

### [PR microsoft/TypeScript-go#3418](https://github.com/microsoft/TypeScript-go/pull/3418) (Closed)

**Fix missing parens in ID fixes**

*Restore missing parentheses in ID fixes to correct related errors in both core and Strada.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3418#issuecomment-4257595864) **azure-pipelines[bot]** reported that one pipeline was filtered out due to trigger conditions

### [PR microsoft/TypeScript-go#3419](https://github.com/microsoft/TypeScript-go/pull/3419) (Closed)

**Avoid panicking on duplicate document close notifications**

*Prevent runtime panics by ignoring duplicate document close notifications from misbehaving clients.*

 * created by **Andarist**

### [PR microsoft/TypeScript-go#3420](https://github.com/microsoft/TypeScript-go/pull/3420) (Closed)

**Fix hover display of default type parameters**

*Ensure hover tooltips correctly display default type parameters in the TypeScript-Go extension*

 * created by **Andarist**

### [PR microsoft/TypeScript-go#3421](https://github.com/microsoft/TypeScript-go/pull/3421) (Closed)

**Fixed an issue with empty type argument lists not being reported on instantiation expressions**

*Compiler now detects and reports empty generic type argument lists in instantiation expressions.*

 * created by **Andarist**

### [Issue microsoft/TypeScript-go#3422](https://github.com/microsoft/TypeScript-go/issues/3422) (Open, `Domain: Editor`)

**Wrong function signature and missing invoking description in hover**

*In tsgo, the hover tooltip for callable/constructable types omits the 'new' signature and JSDoc descriptions.*

 * created by **Withered-Flower-0422**
 * **Withered-Flower-0422** added label `Domain: Editor`

### [Issue microsoft/TypeScript-go#3423](https://github.com/microsoft/TypeScript-go/issues/3423) (Closed, `Crash`)

**Memory usage spiked in version 7\.0\.0\-dev\.20260416\.1**

*Memory usage increased from about 1.1GB to 6GB after upgrading to version 7.0.0-dev.20260416.1*

 * created by **pedro757**
 * **pedro757** added label `Crash`
 * [later](https://github.com/microsoft/TypeScript-go/issues/3423#issuecomment-4260972387) **jakebailey** asked the user to build from source and bisect if they could reproduce the issue consistently
 * [later](https://github.com/microsoft/TypeScript-go/issues/3423#issuecomment-4260979368) **jakebailey** said "And are you referring to the editor? CLI compilation?"
 * [later](https://github.com/microsoft/TypeScript-go/issues/3423#issuecomment-4261327047) **sbking** reported a massive memory leak in VSCode TypeScript Native Preview that consumed increasing RAM until the editor was closed
 * [later](https://github.com/microsoft/TypeScript-go/issues/3423#issuecomment-4261370867) **jakebailey** said "When this happens, can you please run the "Heap Profile" command in the command palette and upload it?"
 * [later](https://github.com/microsoft/TypeScript-go/issues/3423#issuecomment-4261404241) **jakebailey** said "Or, build https://github.com/microsoft/typescript-go/pull/3425 from source and see if that makes the problem go away."
 * [later](https://github.com/microsoft/TypeScript-go/issues/3423#issuecomment-4261450546) **sbking** provided two heap profile attachments for diffing
 * [later](https://github.com/microsoft/TypeScript-go/issues/3423#issuecomment-4261468808) **jakebailey** asked the user to try disabling semantic highlighting by setting editor.semanticHighlighting.enabled to false
 * [later](https://github.com/microsoft/TypeScript-go/issues/3423#issuecomment-4261499932) **sbking** provided a heap profile with the setting disabled

### [PR microsoft/TypeScript-go#3424](https://github.com/microsoft/TypeScript-go/pull/3424) (Open)

**fix\(3422\): fix resolving signature docs on hover**

*Corrects the resolution of function signature documentation when hovering over code elements.*

 * created by **a-tarasyuk**

### [PR microsoft/TypeScript-go#3425](https://github.com/microsoft/TypeScript-go/pull/3425) (Closed)

**Revert "Make LS checkers time out after being idle, segment based on use"**

*Revert recent LS checker idle-timeout and segmentation changes to resolve a suspected memory retention bug in the checker pool.*

 * created by **jakebailey**

