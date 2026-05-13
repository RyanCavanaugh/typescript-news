# Report for 2026-05-10 (Sunday, May 10th, 2026)

8 different users commented on 16 different issues.

## Recommended Actions

 * Response Recommended
    * @hegrec asked about plans to merge this PR in [microsoft/TypeScript-go#3616](https://github.com/microsoft/TypeScript-go/pull/3616#issuecomment-4418086735)

## Activity Summary

### [Issue microsoft/TypeScript-go#3566](https://github.com/microsoft/TypeScript-go/issues/3566) (Closed, `Domain: Declaration Emit`, `Needs Investigation`, **weswigham**, **RyanCavanaugh**, **Copilot**)

**Baselines: Late\-bound computed property \[prop\] preserved instead of resolved to plain prop**

*Late-bound computed property [prop] syntax is preserved instead of being resolved to plain prop*

 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/3566#issuecomment-4408960638) **weswigham** said "I agree, both are equivalent and now we use the []s because we're actually traversing the input nodes (which use brackets) instead of generating the type whole-cloth from symbol information."
 * (2 days ago) **RyanCavanaugh** assigned to **Copilot**, **RyanCavanaugh**
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#3567](https://github.com/microsoft/TypeScript-go/issues/3567) (Closed, `Domain: Declaration Emit`, `Needs Investigation`, **weswigham**, **RyanCavanaugh**, **Copilot**)

**Baselines: Symbol getter/setter declaration emit change**

*Declaration outputs now change the return type of symbol getters/setters to undefined and introduce a new Symbol.toPrimitive overload.*

 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/3567#issuecomment-4409041197) **weswigham** described that the new output was preferable but retained duplicate declarations per the garbage-in-garbage-out principle and identified a Strada bug conflating getters and methods and eliding the method due to overload detection
 * (2 days ago) **RyanCavanaugh** assigned to **Copilot**, **RyanCavanaugh**
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#3569](https://github.com/microsoft/TypeScript-go/issues/3569) (Closed, `Domain: Declaration Emit`, `Needs Investigation`, **weswigham**, **RyanCavanaugh**, **Copilot**)

**Baselines: Declaration emit simplification of class extending built\-in Array**

*Declaration emit now simplifies classes extending built-in Array by dropping the generic parameter and removing inherited constructor overloads.*

 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/3569#issuecomment-4408936938) **weswigham** explained that the outputs were functionally identical and the new output better matched the input source, noted improvements in static block this assignment declarations, and clarified why <any> was generated for extends positions
 * (2 days ago) **RyanCavanaugh** assigned to **Copilot**, **RyanCavanaugh**
 * (later) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#3616](https://github.com/microsoft/TypeScript-go/pull/3616) (Open)

**API \`emit\` support to generate \.d\.ts / \.js files from sources**

*Expose compiler emit in TSGO API and TypeScript client to generate .js and .d.ts files using virtual FS*

 * created by **pfumagalli**
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3616#issuecomment-4323425060) **pfumagalli** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3616#issuecomment-4418086735) **hegrec** asked if the PR would be merged and explained their use case for wrapping the emission pipeline with the virtual file system to capture d.ts content
 * [later](https://github.com/microsoft/TypeScript-go/pull/3616#issuecomment-4420025854) **pfumagalli** said "Resolved conflicts with upstream..."

### [PR microsoft/TypeScript-go#3778](https://github.com/microsoft/TypeScript-go/pull/3778) (Closed, **RyanCavanaugh**, **Copilot**)

**Accept symbolDeclarationEmit12\.js baseline change**

*Accept the updated symbolDeclarationEmit12.js baseline to preserve duplicate [Symbol.toPrimitive] overloads and correct getter versus method return types*

 * created by **Copilot**
 * (2 days ago) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * (later) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#3779](https://github.com/microsoft/TypeScript-go/pull/3779) (Closed, **RyanCavanaugh**, **Copilot**)

**Accept late\-bound computed property baseline diffs**

*Accept baseline diffs for late-bound computed property tests as won’t-fix given semantically equivalent bracket notation*

 * created by **Copilot**
 * (2 days ago) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * (later) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#3780](https://github.com/microsoft/TypeScript-go/pull/3780) (Closed, **RyanCavanaugh**, **Copilot**)

**Accept baseline: declaration emit simplification of class extending built\-in Array**

*Baseline update simplifies JavaScript Array subclass declarations by removing redundant generics and overloads and correctly emitting static assignments.*

 * created by **Copilot**
 * (2 days ago) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * (later) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#3786](https://github.com/microsoft/TypeScript-go/pull/3786) (Closed)

**Fix crashes related to call hierarchy container names for computed properties**

*Resolves crashes due to incorrect call hierarchy container naming for computed properties.*

 * created by **Andarist**
 * (later) **gabritto** closed the issue

### [Issue microsoft/TypeScript-go#3788](https://github.com/microsoft/TypeScript-go/issues/3788) (Closed)

**Behavior difference: callback contextual typing — \`tsc@5\.9\.3\` passes, \`tsc@6\.0\.3\` / \`tsgo\` fail**

*TypeScript 6.0.3 and tsgo misinfer callback parameter types under pnpm enableGlobalVirtualStore symlinks, causing TS7031 errors that 5.9.3 did not produce.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3788#issuecomment-4412914876) **Andarist** said "It would be great if you could pull all of the relevant 3rd party types into a single file - a good repro usually can be created in a single import-less TS playground."
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3788#issuecomment-4412927439) **dougludlow** expressed uncertainty and specified that the import issue occurred only with pnpm’s enableGlobalVirtualStore, working in TypeScript v5.9.3 but failing in v6/v7
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3788#issuecomment-4413473493) **Andarist** said "Ah, I'm sorry! I've missed that this specifically requires enableGlobalVirtualStore"
 * [later](https://github.com/microsoft/TypeScript-go/issues/3788#issuecomment-4419577723) **Andarist** pointed out that TS 5.9 did not error as claimed due to default noImplicitAny and lacked contextual typing, and suggested using --traceResolution to inspect module resolution
 * [later](https://github.com/microsoft/TypeScript-go/issues/3788#issuecomment-4421743724) **dougludlow** thanked for the --traceResolution hint and acknowledged misconfigured peer dependencies
 * (later) **dougludlow** closed the issue

### [PR microsoft/TypeScript-go#3794](https://github.com/microsoft/TypeScript-go/pull/3794) (Closed)

**Remove assertion that doesn't hold after excessive stack depth overflow**

*Remove assertion that fails after excessive stack depth overflow causing spurious failures*

 * created by **ahejlsberg**
 * [later](https://github.com/microsoft/TypeScript-go/pull/3794#issuecomment-4420526658) **ahejlsberg** noted that the assertion in reportRelationError can fail due to stack overflows and suggested removing it
 * [later](https://github.com/microsoft/TypeScript-go/pull/3794#issuecomment-4420743416) **ahejlsberg** noted Copilot's successful single-file repro but found it slow and limited to strict:false, decided against adding it to the test suite, and added a cautionary comment about type relation assumptions

### [Issue microsoft/TypeScript-go#3795](https://github.com/microsoft/TypeScript-go/issues/3795) (Closed, `wontfix`)

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

