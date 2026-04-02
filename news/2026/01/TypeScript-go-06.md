# Report for 2026-01-06 (Tuesday, January 6th, 2026)

5 different users commented on 9 different issues.

## Recommended Actions

 * Response Recommended
    * @rubenferreira97 reported a build hang and provided logs and configuration details in [microsoft/TypeScript-go#1622](https://github.com/microsoft/TypeScript-go/issues/1622#issuecomment-3718503020)
    * @paulintrognon reported intermittent failure requiring reload window in [microsoft/TypeScript-go#2053](https://github.com/microsoft/TypeScript-go/pull/2053#issuecomment-3719035683)
    * @freshp86 provided repro steps as requested in [microsoft/TypeScript-go#2445](https://github.com/microsoft/TypeScript-go/issues/2445#issuecomment-3719228344)

## Activity Summary

### [Issue microsoft/TypeScript-go#1615](https://github.com/microsoft/TypeScript-go/issues/1615) (Open, `Domain: Editor`)

**VSCode Extension blocks Organize Imports**

*The TypeScript Native Preview VSCode extension prevents the Organize Imports command from working until disabled.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1615#issuecomment-3674170187) **JackStandbridgeCS** said "Would love to know if there's an update on this! I've stopped using the extension since it's missing this feature, but would like to return to it for the speed improvements"
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1615#issuecomment-3688522259) **14glwu** said "the same issue"
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/1615#issuecomment-3694964143) **kevcam4891** said "Same! Would love to not have to disable this extension to occasionally organize imports."
 * [today](https://github.com/microsoft/TypeScript-go/issues/1615#issuecomment-3716167778) **NatoBoram** provided links to related issues and pull requests

### [Issue microsoft/TypeScript-go#1622](https://github.com/microsoft/TypeScript-go/issues/1622) (Open, `Crash`, `Domain: Program`, `Domain: Performance`, **sheetalkamat**)

**\[bug\] \`tsgo \-\-build\` uses extreme amounts of memory**

*tsgo --build exhausts over 100GB of memory and crashes when building large monorepos with thousands of TypeScript projects*

 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1622#issuecomment-3654358600) **Knagis** reported that running tsgo with specified flags resulted in a 30GB commit, hung, and could not be killed via task manager
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/1622#issuecomment-3698941951) **spanishpear** reported high memory usage when typechecking a large project and its dependents, noted that tsc was faster, provided profiling details, and asked if the test was configured correctly
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/1622#issuecomment-3700541007) **spanishpear** noted similar performance struggles in tsgolint and pointed to a related issue for potential resolution
 * [later](https://github.com/microsoft/TypeScript-go/issues/1622#issuecomment-3718503020) **rubenferreira97** reported experiencing a process deadlock when running tsgo --build and provided a log file and project configuration details

### [PR microsoft/TypeScript-go#2053](https://github.com/microsoft/TypeScript-go/pull/2053) (Closed)

**Implement auto\-import code actions, port tests and fix some bugs**

*Implement auto-import code actions, port tests, and address remaining import sorting, formatting, symlink, and JSDoc issues*

 * [7 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2053#issuecomment-3545918448) **jakebailey** suggested moving the cursor to the end of the name and using Ctrl+Space to trigger completion to determine if the bug is in the PR or more generic, and recommended filing a separate issue
 * [7 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2053#issuecomment-3546037698) **cpojer** said "I just updated VS Code, and now it appears to be working. That was my last blocker for fully adopting tsgo, thank you!"
 * [7 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2053#issuecomment-3547165717) **cpojer** said "Ah, looks like there are some issues. It only works sometimes, but I have not yet narrowed down when it works and when it doesn't work."
 * [later](https://github.com/microsoft/TypeScript-go/pull/2053#issuecomment-3719035683) **paulintrognon** said "Agree with cpojer: doesn't work all the time. I sometimes have to Reload Window to make it work again."

### [Issue microsoft/TypeScript-go#2445](https://github.com/microsoft/TypeScript-go/issues/2445) (Open, `bug`, **andrewbranch**)

**resolvePackageJsonExports false ignored in tsgo, works in v5\.9 and v6**

*tsgo ignores resolvePackageJsonExports:false causing incorrect import paths in generated d.ts files, unlike TypeScript 5.9 and 6 preview*

 * created by **freshp86**
 * [later](https://github.com/microsoft/TypeScript-go/issues/2445#issuecomment-3719228344) **freshp86** uploaded a minimal repro example

### [Issue microsoft/TypeScript-go#2446](https://github.com/microsoft/TypeScript-go/issues/2446) (Open, **jakebailey**, **Copilot**)

**\`tsgo\` emits invalid code for decorated class methods with \`Symbol\` names**

*When compiling decorated class methods with computed Symbol names, tsgo emits invalid code referencing _a, causing a ReferenceError.*

 * created by **KostyaTretyak**

