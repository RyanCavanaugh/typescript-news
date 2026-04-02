# Report for 2026-03-07 (Saturday, March 7th, 2026)

6 different users commented on 10 different issues.

## Activity Summary

### [Issue microsoft/TypeScript-go#2780](https://github.com/microsoft/TypeScript-go/issues/2780) (Open, `Domain: Editor`, `Needs More Info`, **andrewbranch**)

**High memory consumption in a large pnpm monorepo**

*PR #2502 causes minor edits in a large pnpm monorepo to spike the TypeScript extension memory from ~700MB to ~35GB.*

 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-4006364171) **andrewbranch** explained that the VS Code extension ships daily and that users can use either its bundled version or point to the latest @typescript/native-preview versions via the typescript.native-preview.tsdk preference
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-4006434882) **andrewbranch** described different causes for high memory usage, mentioned a pending PR with optimizations, and asked @shinichy about signing an NDA and sharing their repo for offline debugging
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-4009619194) **shinichy** said "@andrewbranch I'm not sure if an NDA is possible at my company, but I'll look into it. I'll send an email anyway. Thanks for your help!"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-4018362467) **shinichy** described that a generated re-export file with many subpath exports caused checker.getExportsOfModuleWorker to recurse deeply, and asked how to skip visiting the generated export and why the Strada language service didn’t exhibit the issue

### [PR microsoft/TypeScript-go#3017](https://github.com/microsoft/TypeScript-go/pull/3017) (Closed)

**Fixed a rescanning crash related to \`JsxNamespacedName\` with dashes**

*A crash occurring during rescanning of JSX namespaced names with dashes has been resolved.*

 * created by **Andarist**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3017#issuecomment-4017158964) **DanielRosenwasser** said "Thank you!"
 * (today) **DanielRosenwasser** closed the issue

### [Issue microsoft/TypeScript-go#3018](https://github.com/microsoft/TypeScript-go/issues/3018) (Closed, `bug`, `Domain: Editor`, **ahejlsberg**)

**No quick info for properties accessed via index signature**

*TypeScript 7.0 fails to show quick info on indexed Record<string,string> properties, expected string|undefined.*

 * created by **DanielRosenwasser**

### [PR microsoft/TypeScript-go#3019](https://github.com/microsoft/TypeScript-go/pull/3019) (Closed)

**Fix out\-of\-range document symbol error**

*Typing 'export =' followed by a space in an empty TypeScript file triggers documentSymbol to fail due to out-of-range selection.*

 * created by **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3019#issuecomment-4017989682) **Copilot** said "@DanielRosenwasser I've opened a new pull request, #3020, to work on those changes. Once the pull request is ready, I'll request review from you."

### [PR microsoft/TypeScript-go#3020](https://github.com/microsoft/TypeScript-go/pull/3020) (Closed, **DanielRosenwasser**, **Copilot**)

**Add regression test for incomplete \`export =\` document symbol crash**

*Add a regression test to ensure textDocument/documentSymbol handles incomplete export = without crashing and reports valid selection ranges*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **DanielRosenwasser**

### [PR microsoft/TypeScript-go#3021](https://github.com/microsoft/TypeScript-go/pull/3021) (Closed)

**Fixed a format selection crash in reparsed JSDoc nodes**

*Fixed a crash triggered by format selection in reparsed JSDoc nodes.*

 * created by **Andarist**

### [PR microsoft/TypeScript-go#3022](https://github.com/microsoft/TypeScript-go/pull/3022) (Closed)

**Provide type\-based quick info on symbol\-less nodes**

*Enable quick info tooltips showing inferred type information for code nodes without associated symbols.*

 * created by **Andarist**

### [Issue microsoft/TypeScript-go#3023](https://github.com/microsoft/TypeScript-go/issues/3023) (Closed)

**tsc needs \`"types": \["node"\]\`, tsgo doesn't**

*tsc requires adding node types to tsconfig to recognize process globals, whereas tsgo doesn’t produce errors.*

 * created by **s-h-a-d-o-w**

### [PR microsoft/TypeScript-go#3024](https://github.com/microsoft/TypeScript-go/pull/3024) (Closed)

**Fixes a crash when requesting implementations for a module referenced by a tripleslash directive**

*Fix crash when requesting implementations for modules referenced by triple-slash directives.*

 * created by **Andarist**

