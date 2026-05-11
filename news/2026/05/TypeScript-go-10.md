# Report for 2026-05-10 (Sunday, May 10th, 2026)

8 different users commented on 7 different issues.

## Recommended Actions

 * Response Recommended
    * @hegrec asked about plans to merge this PR in [microsoft/TypeScript-go#3616](https://github.com/microsoft/TypeScript-go/pull/3616#issuecomment-4418086735)

## Activity Summary

### [PR microsoft/TypeScript-go#3616](https://github.com/microsoft/TypeScript-go/pull/3616) (Open)

**API \`emit\` support to generate \.d\.ts / \.js files from sources**

*Expose compiler emit in TSGO API and TypeScript client to generate .js and .d.ts files using virtual FS*

 * created by **pfumagalli**
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3616#issuecomment-4323425060) **pfumagalli** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3616#issuecomment-4418086735) **hegrec** asked if the PR would be merged and explained their use case for wrapping the emission pipeline with the virtual file system to capture d.ts content
 * [later](https://github.com/microsoft/TypeScript-go/pull/3616#issuecomment-4420025854) **pfumagalli** said "Resolved conflicts with upstream..."

### [Issue microsoft/TypeScript-go#3788](https://github.com/microsoft/TypeScript-go/issues/3788) (Closed)

**Behavior difference: callback contextual typing — \`tsc@5\.9\.3\` passes, \`tsc@6\.0\.3\` / \`tsgo\` fail**

*TypeScript 6.0.3 and tsgo misinfer callback parameter types under pnpm enableGlobalVirtualStore symlinks, causing TS7031 errors that 5.9.3 did not produce.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3788#issuecomment-4412914876) **Andarist** said "It would be great if you could pull all of the relevant 3rd party types into a single file - a good repro usually can be created in a single import-less TS playground."
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3788#issuecomment-4412927439) **dougludlow** expressed uncertainty and specified that the import issue occurred only with pnpm’s enableGlobalVirtualStore, working in TypeScript v5.9.3 but failing in v6/v7
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3788#issuecomment-4413473493) **Andarist** said "Ah, I'm sorry! I've missed that this specifically requires enableGlobalVirtualStore"
 * [later](https://github.com/microsoft/TypeScript-go/issues/3788#issuecomment-4419577723) **Andarist** pointed out that TS 5.9 did not error as claimed due to default noImplicitAny and lacked contextual typing, and suggested using --traceResolution to inspect module resolution
 * [later](https://github.com/microsoft/TypeScript-go/issues/3788#issuecomment-4421743724) **dougludlow** thanked for the --traceResolution hint and acknowledged misconfigured peer dependencies
 * (later) **dougludlow** closed the issue

### [PR microsoft/TypeScript-go#3794](https://github.com/microsoft/TypeScript-go/pull/3794) (Open)

**Remove assertion that doesn't hold after excessive stack depth overflow**

*Remove assertion that fails after excessive stack depth overflow causing spurious failures*

 * created by **ahejlsberg**
 * [later](https://github.com/microsoft/TypeScript-go/pull/3794#issuecomment-4420526658) **ahejlsberg** noted that the assertion in reportRelationError can fail due to stack overflows and suggested removing it
 * [later](https://github.com/microsoft/TypeScript-go/pull/3794#issuecomment-4420743416) **ahejlsberg** noted Copilot's successful single-file repro but found it slow and limited to strict:false, decided against adding it to the test suite, and added a cautionary comment about type relation assumptions

### [Issue microsoft/TypeScript-go#3795](https://github.com/microsoft/TypeScript-go/issues/3795) (Open)

**tsc & tsgo difference in project reference build order**

*tsgo’s build order compiles the service project before util’s declaration files are emitted, causing import errors on the first build.*

 * created by **SPGoding**

### [PR microsoft/TypeScript-go#3796](https://github.com/microsoft/TypeScript-go/pull/3796) (Open)

**Hoist named class/function expressions assigned to module\.exports in JS declaration emit**

*Fix JS declaration emit to synthesize and hoist named classes or functions assigned to module.exports instead of default fallback.*

 * created by **inq**
 * [later](https://github.com/microsoft/TypeScript-go/pull/3796#issuecomment-4420076536) **inq** said "@microsoft-github-policy-service agree"

### [PR microsoft/TypeScript-go#3797](https://github.com/microsoft/TypeScript-go/pull/3797) (Closed, **ahejlsberg**, **Copilot**)

**Add standalone single\-file repro for relater overflow assertion in issue 3791**

*Add a standalone single-file TypeScript reproduction of the Relater.reportRelationError assertion panic under tsgo for issue 3791.*

 * created by **Copilot**
 * (later) **Copilot** assigned to **Copilot**, **ahejlsberg**
 * (later) **ahejlsberg** closed the issue

