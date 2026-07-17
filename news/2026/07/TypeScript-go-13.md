# Report for 2026-07-13 (Monday, July 13th, 2026)

18 different users commented on 27 different issues.

## Recommended Actions

 * Response Recommended
    * @issy reported experiencing high memory usage on macOS Tahoe and reverting to tsc in [microsoft/TypeScript-go#3032](https://github.com/microsoft/TypeScript-go/issues/3032#issuecomment-4967431244)
    * @Ijtihed asked for consensus and offered to close if needed in [microsoft/TypeScript-go#4218](https://github.com/microsoft/TypeScript-go/pull/4218#issuecomment-4969251422)

## Activity Summary

### [Issue microsoft/TypeScript-go#2310](https://github.com/microsoft/TypeScript-go/issues/2310) (Open, `possible improvement`, **joj**)

**TypeScript for \.Net Projects**

*Custom MSBuild targets file and instructions to compile TypeScript 7 in .NET projects with tsgo until official support arrives.*

 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/2310#issuecomment-4923231836) **HolgerJeromin** reported that the Microsoft.TypeScript.MSBuild 7.0.0-beta NuGet package worked but had a buggy TypeScript build configuration (missing module and target settings in TypeScriptProjectProperties.xaml), showed comparison images, and requested an updated package with TypeScript 7.0.2
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/2310#issuecomment-4927037353) **joj** asked for more information about the setup and a build binlog, and explained the upcoming NuGet update and deprecated options
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/2310#issuecomment-4934360048) **HolgerJeromin** described having old .csproj files with obsolete TypeScript settings that were ignored by ts-msbuild due to tsconfig.json and included a project XML excerpt
 * [today](https://github.com/microsoft/TypeScript-go/issues/2310#issuecomment-4960106408) **joj** acknowledged a bug, explained that the new warnings are redundant when using tsconfig, and said they would fix it

### [Issue microsoft/TypeScript-go#3032](https://github.com/microsoft/TypeScript-go/issues/3032) (Closed, `Domain: Editor`, `Needs More Info`)

**tsgo \-\-lsp memory leak on large projects / triggers OOM**

*The tsgo LSP process in the TypeScript Native Preview extension leaks memory when handling large projects, causing OOM on low-RAM Linux machines.*

 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/issues/3032#issuecomment-4634340466) **jakebailey** said "I have no idea, the only way I can think this is breaking is due to truncation but if the process is not exiting, there's no reason for it."
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/3032#issuecomment-4741315097) **doylio** shared a heap profile attachment
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/3032#issuecomment-4744371800) **jakebailey** said "That one loads, but doesn't provide much interesting besides typical checker stuff, which should be getting cleaned up, including on idle after #3435 too..."
 * [later](https://github.com/microsoft/TypeScript-go/issues/3032#issuecomment-4967431244) **issy** reported experiencing excessive memory usage of the tsgo process on macOS Tahoe and reverting to using tsc
 * [later](https://github.com/microsoft/TypeScript-go/issues/3032#issuecomment-4970992858) **andrewbranch** directed the user to CONTRIBUTING.md for collecting profiles and logs and asked them to open a new issue with actionable info

### [PR microsoft/TypeScript-go#3881](https://github.com/microsoft/TypeScript-go/pull/3881) (Closed)

**Expose ImportAdder to IPC API**

*Expose ImportAdder via the IPC API to allow external processes to add imports programmatically.*

 * created by **andrewbranch**
 * **andrewbranch** added to milestone `Post-7.0`
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#4179](https://github.com/microsoft/TypeScript-go/pull/4179) (Closed, `No linked issue`)

** Add custom/projectFiles LSP request**

*Add a custom LSP request to return all loaded projects and their source files for workspace initialization.*

 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4179#issuecomment-4606882567) **navya9singh** explained how Visual Studio uses partial project information from the snapshot to populate the Roslyn workspace for the Task List and why partial data suffices
 * (5 weeks ago) **RyanCavanaugh** added label `No linked issue`, and set milestone to `Possible Improvement`
 * [today](https://github.com/microsoft/TypeScript-go/pull/4179#issuecomment-4963283128) **navya9singh** said "Fixed on the client side"
 * (today) **navya9singh** closed the issue

### [PR microsoft/TypeScript-go#4218](https://github.com/microsoft/TypeScript-go/pull/4218) (Open, `Voight-Kampff Anomaly`)

**Allow lone & in Unicode sets regexp classes**

*Update native scanner to allow lone & in Unicode Set regex character classes while preserving && intersections.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4218#issuecomment-4785998449) **Ijtihed** explained that they were a junior engineer who picked the issue to learn after browsing rather than from personal need
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4218#issuecomment-4792508870) **RyanCavanaugh** said "@graphemecluster in case you want to see it"
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4218#issuecomment-4796094461) **graphemecluster** noted the small fix looked fine but mentioned preferring to port PR #62716 if its scope met expectations
 * [later](https://github.com/microsoft/TypeScript-go/pull/4218#issuecomment-4969251422) **Ijtihed** said "so what's the consensus here? :) I can close if needed"

### [Issue microsoft/TypeScript-go#4579](https://github.com/microsoft/TypeScript-go/issues/4579) (Closed)

**tsgo typechecks slower than TS6**

*tsgo typechecking is over five times slower than TypeScript 6 on the same codebase.*

 * created by **XiNiHa**
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/4579#issuecomment-4948371190) **ahejlsberg** attributed the performance regression to a change in #3445, explained that TS7's deeper analysis led to more type instantiations compared to TS6, and suggested simplifying the types
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/4579#issuecomment-4949748665) **XiNiHa** said "Do you mean the behavior is expected/intended? Should it be fixed from the library side?"
 * [later](https://github.com/microsoft/TypeScript-go/issues/4579#issuecomment-4970222219) **ahejlsberg** said "@XiNiHa Yes, the behavior is expected. TS6 would similarly slow down if the changes in #3445 were applied to that codebase. The core problem is the complexity and expense of the types."

### [Issue microsoft/TypeScript-go#4619](https://github.com/microsoft/TypeScript-go/issues/4619) (Open, `possible improvement`, **andrewbranch**)

**Improve API performance when using virtual file system**

*Include inline file content and precomputed directory listings in updateSnapshot to eliminate virtual file system IPC calls and improve performance.*

 * created by **dragomirtitian**

### [Issue microsoft/TypeScript-go#4620](https://github.com/microsoft/TypeScript-go/issues/4620) (Open, `Needs Investigation`, **jakebailey**)

**tsc is not resposive to \`ctrl\-c\`**

*tsc fails to respond to ctrl-c due to incomplete propagation of signal handlers in typescript-go*

 * created by **lukesandberg**

### [PR microsoft/TypeScript-go#4621](https://github.com/microsoft/TypeScript-go/pull/4621) (Closed)

**Update Component Governance task display name and properties**

*Improve the Component Governance task by updating its display name in YAML and setting continueOnError to true.*

 * created by **joaquinjulca26**
 * (today) **joaquinjulca26** closed the issue

### [Issue microsoft/TypeScript-go#4622](https://github.com/microsoft/TypeScript-go/issues/4622) (Closed, `Non-regression`)

**High memory usage for packages such as \`@microsoft/teams\.graph\-endpoints\`**

*Importing @microsoft/teams.graph-endpoints in a minimal TypeScript project spikes memory usage by approximately 300 MB, prompting investigation into potential TypeScript-side optimizations.*

 * created by **mjbvz**

### [PR microsoft/TypeScript-go#4623](https://github.com/microsoft/TypeScript-go/pull/4623) (Open)

**Fix continueOnError casing in pipeline YAML and The indentation**

*Updated pipeline YAML to correct continueOnError casing, fix indentation, and improve task display name.*

 * created by **joaquinjulca26**

### [PR microsoft/TypeScript-go#4624](https://github.com/microsoft/TypeScript-go/pull/4624) (Closed)

**Update Copilot setup steps in workflow file**

*Pin Node.js and gopls versions and clarify comments to improve Copilot setup workflow reproducibility.*

 * created by **joaquinjulca26**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4624#issuecomment-4965708338) **jakebailey** said "We shouldn't do any of these "
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4625](https://github.com/microsoft/TypeScript-go/pull/4625) (Closed)

**VS enhanced hover: symbol icon \+ colorized text**

*Extend Corsa's LSP hover responses to include VS-specific icon and syntax coloring metadata for enhanced tooltips.*

 * created by **navya9singh**

### [Issue microsoft/TypeScript-go#4626](https://github.com/microsoft/TypeScript-go/issues/4626) (Open)

**Include \`projectReferences\` in parsed config returned from \`API\#parseConfigFile\(\)\`**

*Include projectReferences in the parsed config returned by API#parseConfigFile to support solution tsconfig files.*

 * created by **mrazauskas**

### [PR microsoft/TypeScript-go#4627](https://github.com/microsoft/TypeScript-go/pull/4627) (Open)

**Include \`projectReferences\` in parsed config**

*The API#parseConfigFile method now includes projectReferences in its parsed configuration output.*

 * created by **mrazauskas**

### [PR microsoft/TypeScript-go#4628](https://github.com/microsoft/TypeScript-go/pull/4628) (Open)

**Handle extensionless root files gracefully instead of panicking**

*Handle extensionless root files by emitting TS6231 diagnostics instead of panicking and defaulting unknown script kinds to TypeScript.*

 * created by **UditDewan**

### [Issue microsoft/TypeScript-go#4629](https://github.com/microsoft/TypeScript-go/issues/4629) (Closed, `Crash`, **weswigham**)

**panic: Unknown parent for parameter: KindArrowFunction**

*typescript-go crashes with panic 'Unknown parent for parameter: KindArrowFunction' during declaration transformation.*

 * created by **tido64**
 * **tido64** added label `Crash`

### [Issue microsoft/TypeScript-go#4630](https://github.com/microsoft/TypeScript-go/issues/4630) (Open, `Needs More Info`)

**"Type instantiation is excessively deep and possibly infinite" error with tsgo in v7**

*Typechecking with tsgo and TypeScript v7.0.2 intermittently fails with excessive stack depth and infinite type instantiation errors, unlike v6.0.*

 * created by **justinsmid**

### [Issue microsoft/TypeScript-go#4631](https://github.com/microsoft/TypeScript-go/issues/4631) (Closed, `Working As Intended`)

**Error TS2590 after migration to Typescript 7\.**

*Migrating a React MUI project to TypeScript 7 causes TS2590 due to excessively complex union types*

 * created by **aleks-elkin**

### [Issue microsoft/TypeScript-go#4632](https://github.com/microsoft/TypeScript-go/issues/4632) (Open, `bug`, **RyanCavanaugh**, **Copilot**)

**experimentalDecorators: a class name used as an object literal key is renamed to the self\-reference alias**

*TypeScript 7.0.2 with experimentalDecorators wrongly renames object literal keys matching a decorated class name to its alias.*

 * created by **omairvaiyani**

### [Issue microsoft/TypeScript-go#4633](https://github.com/microsoft/TypeScript-go/issues/4633) (Open, `Needs Investigation`, **jakebailey**)

**Publish an official wasip1 \(WASI\) build artifact of tsgo**

*Publish an official Go WASI (wasip1) WebAssembly build artifact of tsgo alongside native binaries in releases.*

 * created by **calvinrp**

