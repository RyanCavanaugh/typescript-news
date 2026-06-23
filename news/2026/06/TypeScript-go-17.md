# Report for 2026-06-17 (Wednesday, June 17th, 2026)

13 different users commented on 21 different issues.

## Recommended Actions

 * Response Recommended
    * @doylio provided a heap profile attachment in [microsoft/TypeScript-go#3032](https://github.com/microsoft/TypeScript-go/issues/3032#issuecomment-4741315097)
    * @typescript-automation[bot] reported that a perf run failed in [microsoft/TypeScript-go#3362](https://github.com/microsoft/TypeScript-go/pull/3362#issuecomment-4735426623)
    * @mrazauskas asked if this PR should close issue #2851 and requested the PR motivation in [microsoft/TypeScript-go#4337](https://github.com/microsoft/TypeScript-go/pull/4337#issuecomment-4738685584)

## Activity Summary

### [Issue microsoft/TypeScript-go#3032](https://github.com/microsoft/TypeScript-go/issues/3032) (Closed, `Domain: Editor`, `Needs More Info`)

**tsgo \-\-lsp memory leak on large projects / triggers OOM**

*The tsgo LSP process in the TypeScript Native Preview extension leaks memory when handling large projects, causing OOM on low-RAM Linux machines.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/3032#issuecomment-4623028146) **doylio** said "MacOS Tahoe 26.5.1"
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/3032#issuecomment-4623808592) **andrewbranch** said "@jakebailey any ideas?"
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/3032#issuecomment-4634340466) **jakebailey** said "I have no idea, the only way I can think this is breaking is due to truncation but if the process is not exiting, there's no reason for it."
 * [later](https://github.com/microsoft/TypeScript-go/issues/3032#issuecomment-4741315097) **doylio** shared a heap profile attachment

### [PR microsoft/TypeScript-go#3362](https://github.com/microsoft/TypeScript-go/pull/3362) (Open)

**Replace most ID usage with pointers**

*Propose replacing most ID fields with pointers in Go to leverage pointer comparability and reduce overhead.*

 * [10 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3362#issuecomment-4208296421) **typescript-bot** reported starting jobs and provided build status and results links
 * [10 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3362#issuecomment-4208449180) **typescript-bot** provided the performance run results for the requested baseline vs pr comparison
 * **RyanCavanaugh** added to milestone `Possible Improvement`
 * [today](https://github.com/microsoft/TypeScript-go/pull/3362#issuecomment-4735126530) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3362#issuecomment-4735127438) **typescript-automation[bot]** announced the start of the perf test job and provided status and result links
 * [today](https://github.com/microsoft/TypeScript-go/pull/3362#issuecomment-4735426623) **typescript-automation[bot]** said "@jakebailey, the perf run you requested failed. You can check the log here."
 * [today](https://github.com/microsoft/TypeScript-go/pull/3362#issuecomment-4735830791) **typescript-automation[bot]** posted the requested perf run results for jakebailey including comparison metrics

### [PR microsoft/TypeScript-go#4337](https://github.com/microsoft/TypeScript-go/pull/4337) (Open)

**API: add checker methods to get true and false types of a conditional type**

*Add API checker methods for obtaining the true and false branch types of a conditional type.*

 * **RyanCavanaugh** added to milestone `Post-7.0`
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4337#issuecomment-4726236305) **mrazauskas** asked to link to issue #2851 and suggested adding getTrueType() and getFalseType() to ConditionalType
 * [today](https://github.com/microsoft/TypeScript-go/pull/4337#issuecomment-4731859787) **piotrtomiak** asked what “link” referred to and said they would implement the change after PR 4341 merged due to needing a Type–projectId association
 * [today](https://github.com/microsoft/TypeScript-go/pull/4337#issuecomment-4738685584) **mrazauskas** responded that they originally thought the PR could close issue #2851 but then noted they seem different domains and that the PR’s motivation is missing

### [Issue microsoft/TypeScript-go#4347](https://github.com/microsoft/TypeScript-go/issues/4347) (Open, `Needs More Info`)

**CPU usage spikes to 80% to 100% when using \`tsgo \-\-lsp \-\-stdio\`**

*tsgo's LSP process uses 80-100% CPU when typing in TypeScript files larger than 100 lines*

 * created by **epicmet**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4347#issuecomment-4732756773) **DanielRosenwasser** noted that the project’s heavy checker work and allocations were impacting GC, asked if the issue persisted in TypeScript 6, and pointed to performance trace documentation
 * **DanielRosenwasser** added label `Needs More Info`

### [PR microsoft/TypeScript-go#4351](https://github.com/microsoft/TypeScript-go/pull/4351) (Closed)

**Deduplicate declaration emit for this\-assigned methods**

*Deduplicate declaration emissions of this-assigned methods and correct late binding for static methods to ensure accurate type checking.*

 * created by **weswigham**

### [Issue microsoft/TypeScript-go#4352](https://github.com/microsoft/TypeScript-go/issues/4352) (Open)

**Behavior difference: Block comments on \`@typedef\` structural types are not preserved, if they are imported and reconstructed as inline types in another file**

*tsgo fails to preserve block comments on @typedef structural types when they are imported and reconstructed as inline types*

 * created by **hkleungai**

### [PR microsoft/TypeScript-go#4353](https://github.com/microsoft/TypeScript-go/pull/4353) (Closed)

**API: make it possible to open file in inferred projects through API **

*Enable the API to open files from node_modules in inferred projects even when not in the import graph.*

 * created by **piotrtomiak**

### [Issue microsoft/TypeScript-go#4354](https://github.com/microsoft/TypeScript-go/issues/4354) (Closed, `Domain: Editor`, **gabritto**)

**No editor error for invalid tsconfig settings**

*TypeScript 7 native preview fails to report editor errors for invalid tsconfig compilerOptions values that TypeScript 6 previously flagged*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** added label `Domain: Editor`, set milestones to `Post-7.0`, `TypeScript 7.0 Stable`, removed from milestone `Post-7.0`, and assigned to **gabritto**

### [PR microsoft/TypeScript-go#4355](https://github.com/microsoft/TypeScript-go/pull/4355) (Closed)

**fix\(4354\): add tsconfig option errors from project diagnostics**

*Add a tsconfig option to enable reporting of project diagnostic errors.*

 * created by **a-tarasyuk**

### [PR microsoft/TypeScript-go#4356](https://github.com/microsoft/TypeScript-go/pull/4356) (Closed)

**Re\-allow nested cjs export assignments in declaration emit**

*Restore support for nested CJS export assignments in declaration emit, update export ordering and naming, and revise related tests.*

 * created by **weswigham**

### [PR microsoft/TypeScript-go#4357](https://github.com/microsoft/TypeScript-go/pull/4357) (Open)

**Lint on all OSs**

*Run lint checks on all operating systems in CI to simplify maintenance and avoid omissions.*

 * created by **jakebailey**

### [Issue microsoft/TypeScript-go#4358](https://github.com/microsoft/TypeScript-go/issues/4358) (Open, **jakebailey**, **Copilot**)

**SourceFile\.ContainsNonASCII can be false for non\-ASCII in string literal fast path**

*Non-ASCII characters inside simple string literals bypass detection in SourceFile.ContainsNonASCII, resulting in incorrect UTF-16 position mapping.*

 * created by **CPunisher**
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#4359](https://github.com/microsoft/TypeScript-go/issues/4359) (Open, `Domain: Editor`, **jakebailey**, **Copilot**)

**Missing some completion and hover document in namespaced JSX intrinsic element**

*VSCode’s TypeScript JSX support lacks attribute completions and hover documentation for namespaced JSX intrinsic elements like foo:bar*

 * created by **hjkcai**
 * **hjkcai** added label `Domain: Editor`

### [PR microsoft/TypeScript-go#4360](https://github.com/microsoft/TypeScript-go/pull/4360) (Open, **jakebailey**, **Copilot**)

**Fix non\-ASCII detection for source file position maps**

*Enhance non-ASCII detection and position mapping to compute correct UTF-16 offsets with a shared helper and regression tests.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#4361](https://github.com/microsoft/TypeScript-go/issues/4361) (Open, **jakebailey**, **Copilot**)

**${configDir} path candidate resolving is incorrect when extending base config**

*Extending a base tsconfig in TypeScript 7 causes `${configDir}` paths to resolve to the project root instead of the current package.*

 * created by **Matthieu7503**
 * (later) **jakebailey** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#4362](https://github.com/microsoft/TypeScript-go/pull/4362) (Open, **jakebailey**, **Copilot**)

**Fix ${configDir} path candidate resolving in extended config**

*Ensure ${configDir} is correctly resolved for path mappings inherited from extended configurations*

 * created by **Copilot**
 * (later) **Copilot** assigned to **Copilot**, **jakebailey**
 * [later](https://github.com/microsoft/TypeScript-go/pull/4362#issuecomment-4743158672) **jakebailey** said "@copilot+gpt-5.5 you left this as WIP; are you done?"
 * [later](https://github.com/microsoft/TypeScript-go/pull/4362#issuecomment-4743297883) **Copilot** confirmed completion and provided final validation steps and commit hash

### [Issue microsoft/TypeScript-go#4363](https://github.com/microsoft/TypeScript-go/issues/4363) (Open, **jakebailey**, **Copilot**)

**Behavior difference: Comment above \`@typedef\` does not become comment for the corresponding emitted type in tsgo**

*tsgo fails to preserve JSDoc comments above @typedef by emitting them after the generated type declaration*

 * created by **hkleungai**

### [PR microsoft/TypeScript-go#4364](https://github.com/microsoft/TypeScript-go/pull/4364) (Open)

**Add default\.pgo file for main entrypoint**

*Add a default.pgo file for the main entrypoint to utilize the new performance infrastructure*

 * created by **jakebailey**
 * [later](https://github.com/microsoft/TypeScript-go/pull/4364#issuecomment-4743658006) **jakebailey** said "@typescript-bot perf test this faster"
 * [later](https://github.com/microsoft/TypeScript-go/pull/4364#issuecomment-4743658692) **typescript-automation[bot]** notified of job start and provided links to build status and results

