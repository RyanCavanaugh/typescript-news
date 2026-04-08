# Report for 2026-04-05 (Sunday, April 5th, 2026)

5 different users commented on 5 different issues.

## Activity Summary

### [Issue microsoft/TypeScript-go#2060](https://github.com/microsoft/TypeScript-go/issues/2060) (Closed, `Needs More Info`)

**Typescript\-go does not infer large generics due to maximum length compiler will serialize**

*typescript-go cannot infer large nested generics for SStruct because the inferred type exceeds the compiler’s maximum serialized length, requiring manual annotations.*

 * [18 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2060#issuecomment-3586819628) **liuxingbaoyu** mentioned that Babel encountered the issue in recent versions and provided reproduction steps and a PR link
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/2060#issuecomment-4172580359) **RyanCavanaugh** said "I'll try to include something in CHANGES.md but this is kind of vague to work from and I'm not sure anyone will read that section anyway 😅"
 * (4 days ago) **RyanCavanaugh** closed the issue
 * [later](https://github.com/microsoft/TypeScript-go/issues/2060#issuecomment-4192244516) **Raynos** said "No worries Ryan, I can't remember what the fix was on my side. Right i had to make it a typed const declaration to skip the inference hell. "

### [Issue microsoft/TypeScript-go#3312](https://github.com/microsoft/TypeScript-go/issues/3312) (Closed, `Domain: Editor`)

**latest release \[0\.20260401\.1\] breaks LSP on VS code**

*Version 0.20260401.1 of the extension fails to load in VS Code 1.113.0 on Linux due to a missing typescript.native-preview-enable command*

 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/3312#issuecomment-4180470533) **jakebailey** expressed inability to see how the issue could occur and asked for additional logs
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/3312#issuecomment-4180756346) **christophe-g** thanked maintainers, reverted to version 0.20260331.1 due to no logs, and promised to report results of issue #3333 when deployed
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/3312#issuecomment-4180780205) **jakebailey** linked the commit range and stated that only the LSP change exists which wouldn’t affect activation
 * [later](https://github.com/microsoft/TypeScript-go/issues/3312#issuecomment-4190963025) **christophe-g** noted that the issue no longer occurred with version 0.20260405.1 and closed it as fixed
 * (later) **christophe-g** closed the issue

### [PR microsoft/TypeScript-go#3346](https://github.com/microsoft/TypeScript-go/pull/3346) (Closed)

**Proper symbols for \`module\` and \`module\.exports\` in CJS files**

*Adds proper symbol definitions for module and module.exports in CommonJS files to improve references, Quick Info, and symbol/type baselines.*

 * created by **ahejlsberg**

### [Issue microsoft/TypeScript-go#3347](https://github.com/microsoft/TypeScript-go/issues/3347) (Closed, **andrewbranch**)

**TS1361: 'defineConfig' cannot be used as a value because it was imported using 'import type'\.**

*tsgo triggers TS1361 complaining that defineConfig imported with import type cannot be used as a value in ESLint config.*

 * created by **314systems**
 * **ahejlsberg** assigned to **andrewbranch**

### [Issue microsoft/TypeScript-go#3348](https://github.com/microsoft/TypeScript-go/issues/3348) (Closed, `Domain: Editor`, **andrewbranch**)

**Auto import adds duplicate imports for namespace exports**

*VS Code auto-import adds duplicate namespace imports for a namespaced export, causing a duplicate identifier error.*

 * created by **yume-chan**
 * **yume-chan** added label `Domain: Editor`

