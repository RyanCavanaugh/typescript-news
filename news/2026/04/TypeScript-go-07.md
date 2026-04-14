# Report for 2026-04-07 (Tuesday, April 7th, 2026)

6 different users commented on 16 different issues.

## Recommended Actions

 * Response Recommended
    * @xenokratos provided reproduction details and a screenshot in [microsoft/TypeScript-go#2780](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-4205839648)
    * @vetptzru asked for confirmation or correction of their analysis in [microsoft/TypeScript-go#3139](https://github.com/microsoft/TypeScript-go/issues/3139#issuecomment-4206708107)

## Activity Summary

### [PR microsoft/TypeScript-go#2006](https://github.com/microsoft/TypeScript-go/pull/2006) (Closed)

**Fix encode and decode bug for binary ast**

*Binary AST encoding/decoding mismanages empty function parameters and incorrectly indexes child nodes.*

 * created by **quininer**
 * (later) **quininer** closed the issue

### [Issue microsoft/TypeScript-go#2780](https://github.com/microsoft/TypeScript-go/issues/2780) (Open, `Domain: Editor`, `Needs More Info`, **andrewbranch**)

**High memory consumption in a large pnpm monorepo**

*PR #2502 causes minor edits in a large pnpm monorepo to spike the TypeScript extension memory from ~700MB to ~35GB.*

 * [1 month ago](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-4018362467) **shinichy** described that a generated re-export file with many subpath exports caused checker.getExportsOfModuleWorker to recurse deeply, and asked how to skip visiting the generated export and why the Strada language service didn’t exhibit the issue
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-4047475814) **dbrxnds** said "Update: Unfortunately I just seemed to have gotten last time when I said things improved. These past 2 days have been the same as before."
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-4158120316) **ozyx** reported experiencing a massive memory leak in a large pnpm monorepo when using tsgo and offered to gather debug info
 * [later](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-4205839648) **xenokratos** reported experiencing the same issue on a large monorepo and attached a screenshot

### [Issue microsoft/TypeScript-go#3139](https://github.com/microsoft/TypeScript-go/issues/3139) (Open, `Needs More Info`)

**runtime: failed to create new OS thread**

*Running tsgo on a large macFUSE-mounted TypeScript project exhausts OS threads and crashes the Go runtime.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/3139#issuecomment-4123683587) **jakebailey** expressed uncertainty about reproducing the issue, suggested runtime tracing might help, and asked why the issue had so many reactions
 * [6 days ago](https://github.com/microsoft/TypeScript-go/issues/3139#issuecomment-4170466384) **vetptzru** dug into the codebase and identified that the file parser spawns unbounded goroutines which block on readSema, causing OS thread exhaustion on slow filesystems, and suggested using a pre-spawn semaphore approach
 * [6 days ago](https://github.com/microsoft/TypeScript-go/issues/3139#issuecomment-4170683318) **jakebailey** questioned how the cause was determined and challenged the explanation of the Go scheduler
 * [later](https://github.com/microsoft/TypeScript-go/issues/3139#issuecomment-4206708107) **vetptzru** admitted that readSema did not hold an OS thread, proposed that unbounded module resolution goroutines making FileExists/DirectoryExists syscalls could exhaust threads on slow filesystems, and requested correction if mistaken

### [Issue microsoft/TypeScript-go#3348](https://github.com/microsoft/TypeScript-go/issues/3348) (Closed, `Domain: Editor`, **andrewbranch**)

**Auto import adds duplicate imports for namespace exports**

*VS Code auto-import adds duplicate namespace imports for a namespaced export, causing a duplicate identifier error.*

 * created by **yume-chan**
 * **yume-chan** added label `Domain: Editor`
 * **RyanCavanaugh** assigned to **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#3353](https://github.com/microsoft/TypeScript-go/pull/3353) (Closed)

**Re\-add incremental mode diagnostic chain repopulation**

*Reintroduce diagnostic chain repopulation in incremental mode to ensure stable incremental results.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3356](https://github.com/microsoft/TypeScript-go/pull/3356) (Closed)

**Update readme status table**

*Update the README status table because it has not been updated in a while.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3357](https://github.com/microsoft/TypeScript-go/issues/3357) (Open, `Crash`, **DanielRosenwasser**, **weswigham**, **Copilot**)

**Nil pointer derefence in \`\(\*NodeBuilderImpl\)\.addPropertyToElementList\` with  \`\-\-tsBuildInfoFile\`**

*A nil pointer dereference occurs in NodeBuilderImpl.addPropertyToElementList when running with the --tsBuildInfoFile option.*

 * created by **LukeAbby**
 * **LukeAbby** added label `Crash`
 * (today) **DanielRosenwasser** assigned to **Copilot**, **DanielRosenwasser**

### [PR microsoft/TypeScript-go#3358](https://github.com/microsoft/TypeScript-go/pull/3358) (Open, **gabritto**)

**Implement LSP\-based code edits with file renaming**

*Implement LSP willRenameFiles support to perform file renames with module specifier updates and arbitrary extension handling.*

 * created by **Andarist**
 * **gabritto** assigned to **gabritto**

### [PR microsoft/TypeScript-go#3359](https://github.com/microsoft/TypeScript-go/pull/3359) (Closed)

**Properly recognize all symbol flags on imported reexported symbols in completions code**

*Enhance completions code to correctly detect all symbol flags on imported and reexported symbols.*

 * created by **Andarist**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#3360](https://github.com/microsoft/TypeScript-go/pull/3360) (Closed)

**Fix symlink parsing in tests**

*Update the test case parser to correctly handle symlink definitions without ‘->’ by creating actual links and deduping real paths.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3360#issuecomment-4201001057) **andrewbranch** said "Feel free to leave the auto-import tests failing. I'm planning to go through the remaining failing auto-imports tests when I have time."
 * [today](https://github.com/microsoft/TypeScript-go/pull/3360#issuecomment-4201019680) **jakebailey** said "Done!"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3361](https://github.com/microsoft/TypeScript-go/pull/3361) (Open, **DanielRosenwasser**, **Copilot**)

**Fix nil pointer dereference in addPropertyToElementList**

*Add nil guard for propertySymbol.Parent in addPropertyToElementList to avoid crashes with synthetic union/intersection properties*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3361#issuecomment-4202878806) **DanielRosenwasser** said "@copilot go."

