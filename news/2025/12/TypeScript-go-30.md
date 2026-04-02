# Report for 2025-12-30 (Tuesday, December 30th, 2025)

4 different users commented on 4 different issues.

## Activity Summary

### [Issue microsoft/TypeScript-go#1622](https://github.com/microsoft/TypeScript-go/issues/1622) (Open, `Crash`, `Domain: Program`, `Domain: Performance`, **sheetalkamat**)

**\[bug\] \`tsgo \-\-build\` uses extreme amounts of memory**

*tsgo --build exhausts over 100GB of memory and crashes when building large monorepos with thousands of TypeScript projects*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1622#issuecomment-3647124648) **Knagis** suggested using an NDA path to share the private codebase and described its structure as React TSX files, Jest and Playwright specs, declaration-only emits, with few symlinks and path aliases
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1622#issuecomment-3654358600) **Knagis** reported that running tsgo with specified flags resulted in a 30GB commit, hung, and could not be killed via task manager
 * [today](https://github.com/microsoft/TypeScript-go/issues/1622#issuecomment-3698941951) **spanishpear** reported high memory usage when typechecking a large project and its dependents, noted that tsc was faster, provided profiling details, and asked if the test was configured correctly
 * [today](https://github.com/microsoft/TypeScript-go/issues/1622#issuecomment-3700541007) **spanishpear** noted similar performance struggles in tsgolint and pointed to a related issue for potential resolution

### [Issue microsoft/TypeScript-go#2414](https://github.com/microsoft/TypeScript-go/issues/2414) (Closed)

**there are like 30 tsgo lsp servers**

*Approximately 30 tsgo LSP server instances are running in a devcontainer, indicating a possible extension or VS Code bug.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/2414#issuecomment-3677940754) **jakebailey** said "Yeah, green in htop means threads; I personally disable showing userspace threads in htop."
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/2414#issuecomment-3678473411) **alita-moore** said "TIL, I think this issue can be closed then"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2414#issuecomment-3699011420) **ItsHarper** said "Why not close it yourself, instead of leaving clutter?"
 * (today) **alita-moore** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/issues/2414#issuecomment-3700771477) **alita-moore** expressed uncertainty about closing the issue without maintainer approval and closed it

### [PR microsoft/TypeScript-go#2434](https://github.com/microsoft/TypeScript-go/pull/2434) (Open)

**Experiment: Quantified Types**

*Looking for a TypeScript typing approach to consume a heterogeneous array of Layer objects without collapsing types into a union.*

 * created by **devanshj**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2434#issuecomment-3700061096) **gabritto** said "This seems like a duplicate of https://github.com/microsoft/TypeScript/issues/14466."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2434#issuecomment-3700068875) **devanshj** acknowledged forgetting to link the existing issue and noted that the PR implements a quantified type

### [PR microsoft/TypeScript-go#2435](https://github.com/microsoft/TypeScript-go/pull/2435) (Closed)

**Support identifier location in inlay hints**

*Update Corsa’s inlay hint implementation to record identifier symbol locations in a separate map and adjust tests avoiding URI conversions.*

 * created by **gabritto**

