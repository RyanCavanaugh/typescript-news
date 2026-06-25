# Report for 2026-06-21 (Sunday, June 21st, 2026)

15 different users commented on 15 different issues.

## Recommended Actions

 * Response Recommended
    * @shining-mind suggested providing an API to query the TypeChecker for nodes in a TS-owned file to support embedded template-literal languages in [microsoft/TypeScript-go#2824](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-4768934487)
    * @shining-mind requested type checks for HTML in tagged template literals and CLI support in [microsoft/TypeScript-go#2824](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-4769927814)
    * @epicmet reported that complex node-redis types caused CPU spikes and asked if the LSP server could address it in [microsoft/TypeScript-go#4347](https://github.com/microsoft/TypeScript-go/issues/4347#issuecomment-4762549382)
    * @nikelborm asked whether TypeScript 6.0 adds imports to the end of declaration files in [microsoft/TypeScript-go#4381](https://github.com/microsoft/TypeScript-go/issues/4381#issuecomment-4765872410)
    * @typescript-automation[bot] reported a build failure due to validation errors or warnings in [microsoft/TypeScript-go#4389](https://github.com/microsoft/TypeScript-go/pull/4389#issuecomment-4766364759)

## Activity Summary

### [Issue microsoft/TypeScript-go#2824](https://github.com/microsoft/TypeScript-go/issues/2824) (Open, `Domain: API and Extensibility`, **andrewbranch**)

**API usage patterns for complex editor extensions**

*Exploring IPC-based API features for a Go TS server to replace TS Server plugins and support Vue editor extensions*

 * [11 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-4172677285) **jakebailey** mentioned that Wasm would not help unless a Wasm runtime was shipped or execution was always launched via NAPI
 * [11 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-4172684436) **lppedd** mentioned that shipping a Wasm runtime in the binary could enable a multilanguage plugin ecosystem and was a reasonable idea
 * **RyanCavanaugh** added to milestone `Post-7.0`
 * [later](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-4768934487) **shining-mind** mentioned a use-case involving embedded languages in tagged-template literals, described how the ts-lit-plugin handles completions and type-checking within a single TypeScript file, and suggested adding an API to query the TypeChecker for specific ranges without using a virtual document
 * [later](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-4769820406) **justinfagnani** thanked shining-mind and explained that tagged template literal checkers needed access to the checker to get expression types, compute binding context types, and check assignability with isTypeAssignableTo, adding diagnostics on failure
 * [later](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-4769844699) **jakebailey** said "Editors have the ability to run multiple LSP servers and offer up all info provided by all of them, even on the same file; does TS have to be the hub for your scenario to work?"
 * [later](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-4769881765) **shining-mind** explained that the HTML tag `my-card` resolves to the MyCard class with a typed `title` property and that binding validation requires TypeScript
 * [later](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-4769904119) **jakebailey** said "That isn't what I meant; if we have an API that can be accessed out-of-proc, you can ask for the type in opened files without being "inside" the process. Perhaps we are agreeing?"
 * [later](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-4769927814) **shining-mind** clarified that with an out-of-process API one could request types of opened files and expressed a desire to type-check HTML in tagged template literals with CLI support

### [PR microsoft/TypeScript-go#4239](https://github.com/microsoft/TypeScript-go/pull/4239) (Open, `No linked issue`)

**Replace ForEachReturnStatement closure with direct kind\-switched walk**

*Replace ForEachReturnStatement closure with a direct kind-switched recursive function to reduce allocations and improve performance.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4239#issuecomment-4652072023) **typescript-automation[bot]** provided requested performance run results including a tsc metrics comparison report
 * (1 week ago) **RyanCavanaugh** added label `No linked issue`, and set milestone to `Possible Improvement`
 * [later](https://github.com/microsoft/TypeScript-go/pull/4239#issuecomment-4766974869) **mds-ant** said "@DanielRosenwasser The small perf regressions are a little surprising. Could we re-run the benchmarks, just to make sure those weren't just noise?"
 * [later](https://github.com/microsoft/TypeScript-go/pull/4239#issuecomment-4770071961) **DanielRosenwasser** said "@typescript-bot perf test this"
 * [later](https://github.com/microsoft/TypeScript-go/pull/4239#issuecomment-4770072931) **typescript-automation[bot]** reported the start of performance tests and provided links to build status and results

### [PR microsoft/TypeScript-go#4240](https://github.com/microsoft/TypeScript-go/pull/4240) (Closed, `No linked issue`)

**Inline \`GetCombinedNodeFlags\` and \`GetCombinedModifierFlags\` bodies**

*Inline flag computations by replacing generic helper with direct node field reads, boosting performance by about 27%.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4240#issuecomment-4652510901) **mds-ant** noted that a small but measurable performance win from a codebase audit was worth landing since it didn't add complexity or maintenance burden
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4240#issuecomment-4652521791) **jakebailey** said "Hm, but as the copilot comment notes, this involves a copy paste"
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4240#issuecomment-4658350219) **mds-ant** noted that code duplication was necessary to enable the optimization, explained the trade-offs of a shared helper, and offered to close the PR if the duplication is unwanted
 * [later](https://github.com/microsoft/TypeScript-go/pull/4240#issuecomment-4766982146) **mds-ant** said "@jakebailey Are you happy merging this, or would you rather not? The win is measurable in relative terms, but small in absolute terms."

### [Issue microsoft/TypeScript-go#4347](https://github.com/microsoft/TypeScript-go/issues/4347) (Closed)

**CPU usage spikes to 80% to 100% when using \`tsgo \-\-lsp \-\-stdio\`**

*tsgo's LSP process uses 80-100% CPU when typing in TypeScript files larger than 100 lines*

 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/4347#issuecomment-4732756773) **DanielRosenwasser** noted that the project’s heavy checker work and allocations were impacting GC, asked if the issue persisted in TypeScript 6, and pointed to performance trace documentation
 * **DanielRosenwasser** added label `Needs More Info`
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/4347#issuecomment-4756988233) **epicmet** confirmed that Typescript 6 didn't reproduce the issue, described CPU usage increase with a large file, and provided performance trace files
 * [today](https://github.com/microsoft/TypeScript-go/issues/4347#issuecomment-4762549382) **epicmet** identified the root cause as complex node-redis types causing CPU spikes in the TS LSP with Neovim and noted VSCode fared better

### [Issue microsoft/TypeScript-go#4381](https://github.com/microsoft/TypeScript-go/issues/4381) (Open, **jakebailey**, **Copilot**)

**Behavior difference: \`\.state\` emit is missing on react component**

*tsgo incorrectly omits emitting React component state initializations inside constructors for JavaScript files, unlike tsc.*

 * created by **hkleungai**
 * [later](https://github.com/microsoft/TypeScript-go/issues/4381#issuecomment-4765872410) **nikelborm** asked whether TypeScript 6.0 adds imports to the end of declaration files, expressing surprise
 * [later](https://github.com/microsoft/TypeScript-go/issues/4381#issuecomment-4765925506) **hkleungai** clarified that they intentionally name files with js/ts suffix to differentiate transpiler behavior and visualize both mapping to the same main.d.ts file
 * [later](https://github.com/microsoft/TypeScript-go/issues/4381#issuecomment-4766441812) **nikelborm** clarified that he meant import statements placement rather than file suffixes, noting that in the provided snippet the import statements were at the end of the file
 * [later](https://github.com/microsoft/TypeScript-go/issues/4381#issuecomment-4766499771) **hkleungai** said "Ohh, that. I believe it is existing tsc behaviors on js file, before tsgo happens."

### [Issue microsoft/TypeScript-go#4388](https://github.com/microsoft/TypeScript-go/issues/4388) (Open, `bug`)

**Parameters not automatically filled for JSdoc comments**

*JSDoc comment skeletons generated by tsgo omit @param tags, unlike the default TypeScript 6.0 behavior.*

 * created by **crystalfp**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4388#issuecomment-4765261220) **jakebailey** said "You haven't turned off the main TS extension, right? That's what should be doing this still."
 * [today](https://github.com/microsoft/TypeScript-go/issues/4388#issuecomment-4765277247) **crystalfp** installed the Typescript native preview extension and enabled it with the 'Enable (experimental)' command then observed that disabling it reverted to v6 behavior

### [PR microsoft/TypeScript-go#4389](https://github.com/microsoft/TypeScript-go/pull/4389) (Closed)

**Prefer covariant inferences with deeper type argument nesting**

*Prioritize covariant type inferences originating from more deeply nested type arguments to improve inference quality.*

 * created by **ahejlsberg**
 * [later](https://github.com/microsoft/TypeScript-go/pull/4389#issuecomment-4765972266) **ahejlsberg** said "This PR supersedes #3391, which isn't quite the right way to solve the issue."
 * [later](https://github.com/microsoft/TypeScript-go/pull/4389#issuecomment-4766046185) **ahejlsberg** said "@typescript-bot test it"
 * [later](https://github.com/microsoft/TypeScript-go/pull/4389#issuecomment-4766046734) **typescript-automation[bot]** reported build job statuses and indicated a validation error for `test top400` and a started status for `perf test this faster`
 * [later](https://github.com/microsoft/TypeScript-go/pull/4389#issuecomment-4766233108) **typescript-automation[bot]** reported the performance run results that were requested
 * [later](https://github.com/microsoft/TypeScript-go/pull/4389#issuecomment-4766364200) **ahejlsberg** said "@typescript-bot test top400"
 * [later](https://github.com/microsoft/TypeScript-go/pull/4389#issuecomment-4766364759) **typescript-automation[bot]** reported that the test top400 job failed to queue due to validation errors or warnings
 * [later](https://github.com/microsoft/TypeScript-go/pull/4389#issuecomment-4769725932) **jakebailey** said "@typescript-bot test top400"
 * [later](https://github.com/microsoft/TypeScript-go/pull/4389#issuecomment-4769726780) **typescript-automation[bot]** posted a job status update indicating a validation error prevented queuing the build
 * [later](https://github.com/microsoft/TypeScript-go/pull/4389#issuecomment-4770085449) **ahejlsberg** said "Not understanding why typescript-bot is refusing to run the top400 tests."
 * [later](https://github.com/microsoft/TypeScript-go/pull/4389#issuecomment-4770130395) **jakebailey** said "@typescript-bot test top400"
 * [later](https://github.com/microsoft/TypeScript-go/pull/4389#issuecomment-4770149372) **jakebailey** said "@typescript-bot test top400"
 * [later](https://github.com/microsoft/TypeScript-go/pull/4389#issuecomment-4770150195) **typescript-automation[bot]** reported CI test top400 job started and linked to build status and results

### [PR microsoft/TypeScript-go#4390](https://github.com/microsoft/TypeScript-go/pull/4390) (Closed, `dependencies`, `github_actions`)

**Bump actions/checkout from 6\.0\.3 to 7\.0\.0 in the github\-actions group across 1 directory**

*Update GitHub Action actions/checkout from v6.0.3 to v7.0.0 in the repository root*

 * created by **dependabot[bot]**
 * (later) **dependabot[bot]** added labels `dependencies`, `github_actions`, `dependencies`, `github_actions`
 * (later) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4391](https://github.com/microsoft/TypeScript-go/issues/4391) (Open, `Needs Investigation`, **ahejlsberg**)

**const type parameter doesn't capture string\-literal property when the parameter type is wrapped in Omit\<\.\.\.\>**

*A const type parameter on interface call signatures loses string-literal property inference when the parameter type uses Omit<…>.*

 * created by **IanVS**
 * [later](https://github.com/microsoft/TypeScript-go/issues/4391#issuecomment-4769860340) **jakebailey** said "Bisects to #4242. @ahejlsberg"

### [Issue microsoft/TypeScript-go#4392](https://github.com/microsoft/TypeScript-go/issues/4392) (Open, `Crash`, **DanielRosenwasser**, **andrewbranch**, **Copilot**)

**panic: cache entry not found \[recovered, repanicked\]**

*TypeScript server v7.0.0-dev panics with 'cache entry not found' while handling file open and config updates.*

 * created by **motopods**
 * **motopods** added label `Crash`

### [Issue microsoft/TypeScript-go#4393](https://github.com/microsoft/TypeScript-go/issues/4393) (Closed, `question`)

**typescript@7\.0\.1\-rc: programmatic AST codegen with \`import ts from "typescript"\` fails**

*Missing root export in typescript@7.0.1-rc package prevents importing ts from "typescript", breaking standard programmatic AST code generation.*

 * created by **wizardnet972**
 * [later](https://github.com/microsoft/TypeScript-go/issues/4393#issuecomment-4770115664) **jakebailey** said "The API is unstable; we didn't describe it on purpose. We weren't even sure if we wanted to include it in the package so early. It's not for wider use!"

### [PR microsoft/TypeScript-go#4394](https://github.com/microsoft/TypeScript-go/pull/4394) (Closed)

**Fix generated Is\* guards for type\-parameter\-kinded nodes**

*Correct Is* guard generation for type-parameter-kinded nodes to eliminate broken JavaScript due to fallthrough.*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#4395](https://github.com/microsoft/TypeScript-go/pull/4395) (Open)

**Devirtualize ForEachChild and IterChildren**

*Generate specialized implementations for ForEachChild and IterChildren to eliminate interface calls and improve inlining.*

 * created by **jakebailey**
 * [later](https://github.com/microsoft/TypeScript-go/pull/4395#issuecomment-4770210933) **jakebailey** said "@typescript-bot perf test this"
 * [later](https://github.com/microsoft/TypeScript-go/pull/4395#issuecomment-4770211791) **typescript-automation[bot]** started jobs and provided build status and result links

