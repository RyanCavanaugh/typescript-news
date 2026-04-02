# Report for 2026-03-27 (Friday, March 27th, 2026)

17 different users commented on 83 different issues.

## Recommended Actions

 * Response Recommended
    * @brokenmass asked to leave the issue open until they test the new build in [microsoft/TypeScript-go#2234](https://github.com/microsoft/TypeScript-go/issues/2234#issuecomment-4144822504)
    * @fadookie provided additional reproduction details after testing --singleThreaded mode in [microsoft/TypeScript-go#3276](https://github.com/microsoft/TypeScript-go/issues/3276#issuecomment-4145822935)

## Activity Summary

### [Issue microsoft/TypeScript-go#2115](https://github.com/microsoft/TypeScript-go/issues/2115) (Open, `possible improvement`)

**Refactor checker pool to limit checker creation for foreground tasks, segment diagnostic checkers**

*Refactor the checker pool to separate foreground and diagnostic tasks, minimizing redundant checker creation and resource usage*

 * created by **jakebailey**
 * **RyanCavanaugh** added label `possible improvement`

### [Issue microsoft/TypeScript-go#2125](https://github.com/microsoft/TypeScript-go/issues/2125) (Open, `possible improvement`)

**Unbounded memory consumption with recursive conditional types causes compilation OOM**

*Recursive conditional types on large numeric and string unions lead the TypeScript compiler to run out of memory and crash.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2125#issuecomment-4011388398) **dougludlow** suggested adding an upper memory usage limit to terminate the tsgo process when it grows unbounded, reporting that it used 20–30+ GB and caused daily unresponsiveness
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2125#issuecomment-4011601474) **jakebailey** said "Editor growth is probably unrelated, and if you have a repro that would be very appreciated in a new issue."
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2125#issuecomment-4012842570) **caomingpei** noted that the tsgo process triggered by VS Code consumed 20–30+ GB of memory causing unresponsiveness, suggested constraining editor/plugin integrations with explicit resource limits or startup parameters, and highlighted a difference between tsc and ts-go default behaviors
 * **RyanCavanaugh** added label `possible improvement`

### [Issue microsoft/TypeScript-go#2136](https://github.com/microsoft/TypeScript-go/issues/2136) (Closed)

**nodeModulesExportsSourceTs\.ts is unstable in concurrent emit**

*nodeModulesExportsSourceTs.ts fails under concurrent emit due to baseline diffs and a missing inner module declaration file.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2136#issuecomment-4144036602) **RyanCavanaugh** said "Presuming fixed for now"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#2186](https://github.com/microsoft/TypeScript-go/issues/2186) (Open, `bug`, **gabritto**)

**Broken assignability and quick info due to erroneously deferring keyof T since \#51621**

*Erroneously deferring keyof T since PR 51621 causes unsimplified quick info and invalid type assignments.*

 * created by **LukeAbby**
 * **RyanCavanaugh** added label `bug`

### [Issue microsoft/TypeScript-go#2214](https://github.com/microsoft/TypeScript-go/issues/2214) (Closed)

**TS2304 when consuming a non\-module global namespace object**

*tsgo fails to resolve a non-module global namespace defined in a referenced composite project, causing TS2304 in the consuming module.*

 * (16 weeks ago) **jakebailey** closed the issue
 * (16 weeks ago) **jakebailey** reopened the issue
 * [16 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2214#issuecomment-3613017603) **HolgerJeromin** thanked the previous commenter and explained switching from module:none to moduleDetection:legacy didn't resolve the namespace issue, and noted that module:none was removed as per issue #2085
 * [today](https://github.com/microsoft/TypeScript-go/issues/2214#issuecomment-4144112361) **RyanCavanaugh** explained that the behavior was intended, noted the namespace wasn’t found because the file wasn’t included in the program, and advised to include the output folder’s .d.ts files or an equivalent solution
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#2220](https://github.com/microsoft/TypeScript-go/issues/2220) (Open, `bug`, **weswigham**)

**\[pnpm\] The inferred type of 'xxx' cannot be named without a reference to '\.pnpm/xxx'**

*tsgo 7.0.0-dev errors on inferring return types from PNPM-installed packages, requiring explicit annotations due to unnameable ".pnpm" path references.*

 * created by **aramissennyeydd**
 * [16 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2220#issuecomment-3614655373) **brokenmass** showed that updating the customRender signature removed the error and detailed the inferred versus expected types
 * [15 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2220#issuecomment-3629578583) **rubnogueira** said "#1034 solved some of my issues, but like the main post, I still have one specific dependency that has the same error."
 * (today) **RyanCavanaugh** added label `bug`, and assigned to **weswigham**

### [Issue microsoft/TypeScript-go#2234](https://github.com/microsoft/TypeScript-go/issues/2234) (Closed, `Needs More Info`)

**tsgo eagerly resolve the type of inferred function Expression**

*tsgo eagerly resolves inferred function expression types, causing Record<keyof TestInterface, string> to collapse to Record<never, string> without explicit annotations.*

 * [15 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2234#issuecomment-3642213777) **MisterJimson** explained that tsgo failed to apply SST’s module augmentations, causing TS2339 errors on Config.STAGE and Config.API_URL and making tsgo unusable for SST v2 projects
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2234#issuecomment-3971552911) **arcanis** asked whether declaration emit reuse would be addressed before tsgo became stable and noted errors persisted in symlinked codebase testing
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2234#issuecomment-3971565320) **jakebailey** said "Yes, for sure. You could try #1693 built from source to see."
 * [today](https://github.com/microsoft/TypeScript-go/issues/2234#issuecomment-4144196208) **RyanCavanaugh** said "@MisterJimson / @brokenmass can you try again on nightly?"
 * **RyanCavanaugh** added label `Needs More Info`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2234#issuecomment-4144792986) **MisterJimson** said "As of like 4 weeks ago I am no longer seeing the issue. Apologies I forgot to follow up."
 * (today) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/issues/2234#issuecomment-4144822504) **brokenmass** said "@RyanCavanaugh would you be so kind to leave this open until I test the new build (tomorrow or Monday)?"
 * (today) **RyanCavanaugh** reopened the issue

### [Issue microsoft/TypeScript-go#2276](https://github.com/microsoft/TypeScript-go/issues/2276) (Open, `bug`, **weswigham**)

**TS2742: The inferred type of 'default' cannot be named**

*Using tsgo to export stylex through a mapped type produces TS2742 errors requiring a default export type annotation.*

 * created by **jfirebaugh**
 * (today) **RyanCavanaugh** added label `bug`, and assigned to **weswigham**

### [Issue microsoft/TypeScript-go#2277](https://github.com/microsoft/TypeScript-go/issues/2277) (Open, `bug`, **weswigham**)

**TS2742: The inferred type of \.\.\. cannot be named\.\.\.**

*pnpm's nested node_modules structure triggers TS2742 inferred type naming errors for Express handler exports under TSGo*

 * created by **jfirebaugh**
 * (today) **RyanCavanaugh** added label `bug`, and assigned to **weswigham**

### [Issue microsoft/TypeScript-go#2278](https://github.com/microsoft/TypeScript-go/issues/2278) (Closed, `bug`, **andrewbranch**)

**TS2305: Module '"@stylexjs/babel\-plugin"' has no exported member 'Options'\.**

*tsgo compilation reports TS2305 error saying '@stylexjs/babel-plugin' has no exported 'Options' member while TypeScript 5.9 does not*

 * [15 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2278#issuecomment-3628955187) **jakebailey** said "But, 5.9 and 6.0 do not seem to complain."
 * [15 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2278#issuecomment-3643232296) **DanielRosenwasser** said "Does 5.9/6.0 run into an issue with "module": "nodenext"?"
 * [14 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2278#issuecomment-3646839251) **jfirebaugh** said "No errors with 5.9 or 6.0 when adding "module": "nodenext" to the above repro."
 * (today) **RyanCavanaugh** added label `bug`, and assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2278#issuecomment-4144422203) **andrewbranch** said "This was fixed by #2946 / #3157 "
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#2282](https://github.com/microsoft/TypeScript-go/issues/2282) (Open, `possible improvement`, **joj**)

**Request for official prebuilt Windows binaries \(tsgo\.exe\) published via GitHub Releases, without requiring npm\.**

*Officially distribute Windows tsgo.exe binaries via GitHub Releases to enable TypeScript use without npm.*

 * [15 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2282#issuecomment-3636626028) **PaulHuizer** explained that they used Blazor SSR, Vue Global, and ES Modules, preferring TypeScript via TsGen for the BFF API, and that Node.js was only needed for TS compilation, with TsGo potentially eliminating the Node.js requirement
 * [15 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2282#issuecomment-3638056870) **joj** asked how Blazor dependencies were being managed, how Vue was integrated, and which IDE was used, and mentioned working on a nuget package for tsgo.exe without npm/node dependencies but without an ETA
 * [15 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2282#issuecomment-3638425819) **PaulHuizer** praised tsgo.exe as a NuGet package without npm/node dependencies
 * (today) **RyanCavanaugh** added label `possible improvement`, and assigned to **joj**

### [Issue microsoft/TypeScript-go#2310](https://github.com/microsoft/TypeScript-go/issues/2310) (Open, `possible improvement`, **joj**)

**TypeScript for \.Net Projects**

*Custom MSBuild targets file and instructions to compile TypeScript 7 in .NET projects with tsgo until official support arrives.*

 * created by **joj**
 * (today) **RyanCavanaugh** added label `possible improvement`, and assigned to **joj**

### [Issue microsoft/TypeScript-go#2317](https://github.com/microsoft/TypeScript-go/issues/2317) (Open, `bug`, **johnfav03**)

**Console is not cleared in watch mode \(also does not show the 0 error count output\)**

*tsgo’s watch mode fails to clear the console between builds and omits the “Found 0 errors” message*

 * created by **gitter-me**
 * [15 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2317#issuecomment-3638431035) **jakebailey** said "This comes down to us not using a diagnostic message in DoCycle, and so TryClearScreen does not detect the starting message and does not issue the screen clearing codes."
 * [15 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2317#issuecomment-3638438200) **jakebailey** said "Well, rather, I think the watch mode for non-build-mode is just not using the right messages."
 * (today) **RyanCavanaugh** added label `bug`, and assigned to **johnfav03**

### [Issue microsoft/TypeScript-go#2334](https://github.com/microsoft/TypeScript-go/issues/2334) (Open, **DanielRosenwasser**)

**Questionable code lenses for object type members on a single line**

*Suppress code lenses on object type members defined inline when their parent and siblings share the same line.*

 * created by **DanielRosenwasser**
 * **RyanCavanaugh** assigned to **DanielRosenwasser**

### [Issue microsoft/TypeScript-go#2362](https://github.com/microsoft/TypeScript-go/issues/2362) (Closed, `duplicate`)

**LSP diagnostics not working in Emacs's eglot**

*tsgo LSP server fails to publish diagnostics to Emacs’s eglot unlike typescript-language-server, possibly due to client capabilities mismatch.*

 * [14 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2362#issuecomment-3652555217) **jakebailey** compared the new language server’s diagnostic behavior to tsserver, noting it only showed diagnostics for opened files and referenced issue #2169 for unopened files
 * [14 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2362#issuecomment-3654617423) **joaotavora** explained that he had two open documents and expected the language server to maintain a dependency graph for diagnostic pulls, criticized VSCode's approach as inefficient, and noted having long ago left JavaScript land
 * [9 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2362#issuecomment-3769773262) **dstaley** noted that Nova currently only supports textDocument.publishDiagnostics and expressed doubt that supporting push diagnostics would be justified
 * **RyanCavanaugh** added label `duplicate`

### [Issue microsoft/TypeScript-go#2364](https://github.com/microsoft/TypeScript-go/issues/2364) (Open, `possible improvement`)

**Provide document links in tsconfig/jsconfig files**

*Enable TypeScript to provide document links for extends, files, and references in tsconfig/jsconfig to improve IntelliSense consistency and reduce bugs.*

 * created by **mjbvz**
 * [14 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2364#issuecomment-3647749264) **jakebailey** suggested adding JSON file patterns to the document selector to limit tsconfig JSON files
 * **RyanCavanaugh** added label `possible improvement`

### [Issue microsoft/TypeScript-go#2379](https://github.com/microsoft/TypeScript-go/issues/2379) (Closed, **andrewbranch**)

**TS2307 can't resolve type that import from pkg/dist directly**

*TypeScript fails to resolve types imported from a package’s dist folder, triggering TS2307 errors and any type fallbacks*

 * created by **ChangeHow**
 * [14 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2379#issuecomment-3651551480) **DanielRosenwasser** explained that the issue was caused by removal of support for --moduleResolution node10 and asked if the same issues occurred with nodenext or bundler
 * [14 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2379#issuecomment-3651559068) **ChangeHow** confirmed the same bundler mode bug and provided log output
 * (today) **RyanCavanaugh** added label `bug`, and assigned to **andrewbranch**

### [Issue microsoft/TypeScript-go#2384](https://github.com/microsoft/TypeScript-go/issues/2384) (Closed, `question`)

**slow Code Completion with use valibot schema define**

*TypeScript code completion becomes significantly slow when using Valibot to define large schemas.*

 * [14 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2384#issuecomment-3672562862) **ahejlsberg** explained that parse trees and binding information are cached but types are recomputed on every change, described the high cost of inferring types for a 4000-line expression, provided performance metrics comparing old and new compilers, and concluded that reducing compute is the only way to improve speed
 * [14 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2384#issuecomment-3672670301) **wszgrcy** thanked the maintainer, provided a link to the type file, and asked for modification suggestions to reduce type computation costs
 * [11 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2384#issuecomment-3706542883) **fabian-hiller** suggested that the pipe function's 20 overload signatures may be causing the slowdown due to missing generic-related optimizations and provided a simplified example signature
 * **RyanCavanaugh** added label `question`

### [Issue microsoft/TypeScript-go#2387](https://github.com/microsoft/TypeScript-go/issues/2387) (Open, `bug`, **iisaduan**)

**Diagnostics don't refresh after file rename**

*After renaming a file, TypeScript diagnostics sometimes fail to update until the server is reloaded.*

 * created by **mjbvz**
 * [14 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2387#issuecomment-3661474214) **lukeapage** said "Maybe https://github.com/microsoft/typescript-go/issues/2133"
 * [12 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2387#issuecomment-3695197345) **renatoaraujoc** said "Happening here too, I thought this was an IntelliJ bug using ts-go."
 * (today) **RyanCavanaugh** added label `bug`, and assigned to **iisaduan**

### [Issue microsoft/TypeScript-go#2394](https://github.com/microsoft/TypeScript-go/issues/2394) (Open, `possible improvement`)

**Enable IntelliSense in staged files**

*Enable IntelliSense features like go-to-definition and document outline for staged files opened from the source control view.*

 * [14 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2394#issuecomment-3662455444) **jakebailey** queried if the files had been opened via the TypeScript language features or as untitled files and noted that tsserver doesn’t support arbitrary URIs
 * [14 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2394#issuecomment-3662496414) **mjbvz** mentioned that git: files were ignored due to non-file URI challenges and suggested TS-go add basic support for other virtual file system schemes
 * [14 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2394#issuecomment-3662503421) **jakebailey** said "Ah, so this is a feature request, not a bug report?"
 * **RyanCavanaugh** added label `possible improvement`

### [Issue microsoft/TypeScript-go#2403](https://github.com/microsoft/TypeScript-go/issues/2403) (Closed)

**tsgo hangs with class/namespace merge \+ recursive types \+ declaration:true**

*tsgo hangs indefinitely on code using class/namespace merges with recursive types when declaration:true is enabled despite tsc compiling it successfully*

 * [14 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2403#issuecomment-3671845303) **jakebailey** said "If it's new in the latest nightly, then it's https://github.com/microsoft/typescript-go/issues/2411 which will be fixed in  7.0.0-dev.20251218.3 (releasing as we speak)."
 * [14 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2403#issuecomment-3672335273) **JonasBa** said "Thanks @jakebailey, I can confirm that the new release fixes the issues. Appreciate the fast turnaround here, tsgo is awesome 🫶 "
 * [13 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2403#issuecomment-3674341723) **PaulRBerg** confirmed that it works now and thanked @jakebailey
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#2424](https://github.com/microsoft/TypeScript-go/issues/2424) (Open, `possible improvement`)

**Request for support for additional architectures**

*Support and a roadmap are requested for riscv64, ppc64le, and loong64 architectures in typescript-go.*

 * [13 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2424#issuecomment-3690771942) **jakebailey** noted that testing and releasing on additional platforms would be infeasible, stated that the current list matches VS Code marketplace support, and asked how the commonality of those platforms was determined
 * [11 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2424#issuecomment-3720653589) **jakebailey** noted that esbuild builds all variants without testing and cautioned about the signing overhead with many optional dependencies
 * [11 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2424#issuecomment-3721623829) **darkyzhou** clarified whether the concern about adding more architectures was mainly about increased CI running time and proposed starting support for riscv64, loong64, ppc64le, and s390x on Linux
 * **RyanCavanaugh** added label `possible improvement`

### [Issue microsoft/TypeScript-go#2443](https://github.com/microsoft/TypeScript-go/issues/2443) (Open, `documentation`, **RyanCavanaugh**)

**\[Doc\]: paths map value points to removed baseUrl value**

*Inline documentation incorrectly references the removed baseUrl option for computing paths map values.*

 * created by **tanepiper**
 * [11 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2443#issuecomment-3720182702) **jakebailey** mentioned the source of the tooltips in schemastore and suggested updating them with neutral language
 * **RyanCavanaugh** added label `documentation`

### [Issue microsoft/TypeScript-go#2457](https://github.com/microsoft/TypeScript-go/issues/2457) (Open, `feature parity`, **jakebailey**)

**Proposal: Prettified type display in hover output**

*Add optional settings to display prettified, expanded types in hover output for better readability.*

 * created by **sQVe**
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2457#issuecomment-3974008251) **EvgenyOrekhov** stated that VS Code now supports this natively and showed how to increase hover verbosity by clicking '+'
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2457#issuecomment-4005963689) **rubnogueira** said "This is part of TypeScript 5.9: https://devblogs.microsoft.com/typescript/announcing-typescript-5-9-beta/#expandable-hovers-(preview) but it's not implemented in tsgo."
 * **RyanCavanaugh** added label `feature parity`

### [PR microsoft/TypeScript-go#2498](https://github.com/microsoft/TypeScript-go/pull/2498) (Closed)

**Declaration \(d\.ts\) output diff breakdown as seen in \`effect\`**

*Comparison of tsc and tsgo declaration file outputs highlighting syntax and type alias differences in the Effect v4 codebase.*

 * [9 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2498#issuecomment-3783734964) **fubhy** clarified that most signature changes were semantically identical except one altering the return type and noted other adjustments were QoL/readability improvements
 * [8 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2498#issuecomment-3791516119) **jakebailey** asked why getConfig function declaration included undefined return in the emitted output
 * [8 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2498#issuecomment-3791520658) **jakebailey** confirmed that #2459 will preserve types as-written to support the "before" suggestion
 * [today](https://github.com/microsoft/TypeScript-go/pull/2498#issuecomment-4144290561) **jakebailey** said "#2459 was merged. I'm pretty sure everything should be fine now. If not, please file a bug."
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2504](https://github.com/microsoft/TypeScript-go/issues/2504) (Open, `bug`, **weswigham**)

**TS4023 "cannot be named" \- tsgo not allowing references to unexported types**

*TypeScript-Go misreports TS4023 for exported wrappers that infer unexported types via Parameters<typeof> from another module.*

 * created by **johnpyp**
 * (today) **RyanCavanaugh** added label `bug`, and assigned to **weswigham**

### [Issue microsoft/TypeScript-go#2505](https://github.com/microsoft/TypeScript-go/issues/2505) (Open, `bug`, **weswigham**)

**Circular type exported from namespace cannot be named**

*ts-go fails to generate declarations for a function using a circular namespace type alias, emitting an unnameable external type error.*

 * created by **Retsam**
 * (today) **RyanCavanaugh** added label `bug`, and assigned to **weswigham**

### [Issue microsoft/TypeScript-go#2640](https://github.com/microsoft/TypeScript-go/issues/2640) (Open, `bug`, **johnfav03**)

**tsgo \-\-watch is lagging and sometimes not emitting at all**

*tsgo watch mode intermittently fails to emit updates promptly or at all when source files change*

 * created by **tharakadesilva**
 * (today) **RyanCavanaugh** added label `bug`, and assigned to **johnfav03**

### [Issue microsoft/TypeScript-go#2656](https://github.com/microsoft/TypeScript-go/issues/2656) (Open, `bug`, **ahejlsberg**)

**Exports are no longer recognized in js modules which contain functions with parameter called \`module\` which have \`module\.exports =\` in their body**

*A function parameter named module with module.exports in it prevents tsgo from recognizing exports while TypeScript 5.9 accepts them.*

 * created by **peetklecha**
 * (today) **RyanCavanaugh** added label `bug`, and assigned to **ahejlsberg**

### [Issue microsoft/TypeScript-go#2683](https://github.com/microsoft/TypeScript-go/issues/2683) (Open, `bug`, **gabritto**)

**TS2590: "Expression produces a union type that is too complex to represent" on generics types**

*A generic type union in the @regle monorepo triggers TS2590 errors due to overly complex inferred types in newer TypeScript versions*

 * [7 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2683#issuecomment-3852054349) **victorgarciaesgi** thanked the maintainer, noted that UnionToTuple produced a TS2321 error on a simple inferring generic, and said they would try stableTypeOrdering
 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2683#issuecomment-3905132004) **victorgarciaesgi** described narrowing down the issue to a recursive type and fixing it with additional isAny and isUnknown checks, noted a crash in one package and inconsistent tsconfig include behavior, and said they would open another issue
 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2683#issuecomment-3908046091) **victorgarciaesgi** found that the type helper crashed when augmenting a tuple with an optional first parameter and provided working and crashing examples
 * **RyanCavanaugh** added label `bug`

### [Issue microsoft/TypeScript-go#2699](https://github.com/microsoft/TypeScript-go/issues/2699) (Closed, `question`)

**tsgo resolves inherited include/exclude globs differently than tsc when using extends**

*tsgo resolves inherited include globs relative to the child config rather than the parent, causing a different output structure than tsc.*

 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2699#issuecomment-3903727524) **mabels** tested nightly 6.0, reported the same TS6059 errors in versions 6 and 7, noted the regression only between 5.9.x and 6/7, and proposed closing the issue
 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2699#issuecomment-3903732821) **jakebailey** suggested that fixing the rootDir issue would align behaviors and proposed porting the warning to version 7.0 if feasible
 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2699#issuecomment-3903750817) **mabels** stated they no longer needed the warning port and would skip version 6.x because tsc felt too slow compared to tsgo
 * (today) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** added label `question`

### [Issue microsoft/TypeScript-go#2762](https://github.com/microsoft/TypeScript-go/issues/2762) (Open, `documentation`, **DanielRosenwasser**)

**Reconsider tsconfig membership lookups for \`\.d\.ts\` files in \`composite\`**

*TypeScript 6.0 and 7.0 unexpectedly exclude .d.ts files listed in tsconfig due to composite and rootDir changes*

 * created by **DanielRosenwasser**
 * (today) **RyanCavanaugh** added label `documentation`, and assigned to **DanielRosenwasser**
 * (today) **DanielRosenwasser** closed the issue
 * (today) **DanielRosenwasser** reopened the issue

### [Issue microsoft/TypeScript-go#2781](https://github.com/microsoft/TypeScript-go/issues/2781) (Open, `possible improvement`, **andrewbranch**)

**resolving library types with import assignment \`import = require\(\)\` fails**

*Named and default type exports from @sendgrid/mail included via import assignment work in TypeScript 6.0 but tsgo reports missing members and default-only import errors.*

 * **jakebailey** removed label `wontfix`
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2781#issuecomment-3992980470) **jakebailey** said "Related: https://github.com/microsoft/typescript-go/issues/1380"
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2781#issuecomment-3993660455) **ahejlsberg** confirmed that even with PR #2946 the `@sendgrid/mail` package would error due to both exported value symbols and an export assignment
 * (today) **RyanCavanaugh** added label `possible improvement`, and assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2781#issuecomment-4145838987) **andrewbranch** explained sendgrid's declaration intent and provided corrected TypeScript export patterns

### [Issue microsoft/TypeScript-go#2791](https://github.com/microsoft/TypeScript-go/issues/2791) (Open, `possible improvement`)

**\[Feature Request\] Static C library**

*Enable tsgo distribution as a static and/or dynamic C library for embedding in native applications such as Rust.*

 * created by **alshdavid**
 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2791#issuecomment-3906042750) **jakebailey** referred to a discussion link, noted it may be possible with caveats, and asked whether IPC or Wasm would work for the use case
 * **RyanCavanaugh** added label `possible improvement`

### [Issue microsoft/TypeScript-go#2836](https://github.com/microsoft/TypeScript-go/issues/2836) (Open, `possible improvement`)

**Cache \`getExePath\(\)\` for performance reasons**

*Cache getExePath results to avoid redundant lookups and improve tsgo invocation performance.*

 * created by **tido64**
 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2836#issuecomment-3928400257) **jakebailey** questioned where caching would occur and explained why postinstall is avoided and no slowdown seems to come from platform checks
 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2836#issuecomment-3928421769) **jakebailey** said "If the import is that slow, we could switch to using plain FS lookups, since peer deps must be "peers" in a parent dir..."
 * **RyanCavanaugh** added label `possible improvement`

### [Issue microsoft/TypeScript-go#2859](https://github.com/microsoft/TypeScript-go/issues/2859) (Closed)

**\`gql\.tada\` performing better with \`\-\-singleThreaded\` than without it**

*tsgo without --singleThreaded runs significantly slower than with it when generating gql.tada types due to union caching inefficiencies.*

 * [1 month ago](https://github.com/microsoft/TypeScript-go/issues/2859#issuecomment-3944449861) **evsasse** attached profiling and log files for default and single-threaded runs and offered to provide additional information
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2859#issuecomment-4058286993) **ahejlsberg** analyzed fragment file dependencies, measured command performance, and concluded that tsgo is ~6x faster than tsc and behaves as expected
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/2859#issuecomment-4060416384) **evsasse** thanked Anders and said they would refine the minimal reproduction while noting unexpected compiler performance differences
 * **RyanCavanaugh** added label `Needs More Info`

### [Issue microsoft/TypeScript-go#2880](https://github.com/microsoft/TypeScript-go/issues/2880) (Open, `bug`, **weswigham**)

**TS4094 for exported class expressions with ES private fields \(tsc handles via name mangling\)**

*tsgo incorrectly errors on exported class expressions using ES private fields, unlike tsc which name-mangles them.*

 * created by **duci9y**
 * [1 month ago](https://github.com/microsoft/TypeScript-go/issues/2880#issuecomment-3947117028) **jakebailey** said "Maybe I'm wrong, but I feel like the original behavior was a bug. noEmit just controls whether or not we emit files. The editor is also a "noEmit" situation, but we show these errors there..."
 * (today) **RyanCavanaugh** added label `bug`, and assigned to **weswigham**

### [Issue microsoft/TypeScript-go#3014](https://github.com/microsoft/TypeScript-go/issues/3014) (Open, `bug`, **johnfav03**)

**\`tsgo \-\-watch\` hangs if given a tsconfig\.json with no files**

*tsgo --watch hangs indefinitely when run on a tsconfig.json configuration that specifies no files*

 * created by **DanielRosenwasser**
 * (today) **RyanCavanaugh** added label `bug`, and assigned to **johnfav03**

### [Issue microsoft/TypeScript-go#3054](https://github.com/microsoft/TypeScript-go/issues/3054) (Open, `feature parity`)

**\`tsgo \-\-generateTrace\` appears unimplemented**

*The tsgo CLI’s documented --generateTrace flag requires an argument but does nothing and fails to produce trace output like tsc.*

 * created by **DorianListens**
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/3054#issuecomment-4035059255) **jakebailey** referred to issue #2914 and suggested trying --pprofDir . while noting it might not be specific enough
 * **RyanCavanaugh** added label `feature parity`

### [PR microsoft/TypeScript-go#3057](https://github.com/microsoft/TypeScript-go/pull/3057) (Open)

**fix: invalidate symlinked packages in auto\-import cache**

*Auto-import cache now invalidates correctly for symlinked packages by including them in its tracking map.*

 * created by **ericnorris**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3057#issuecomment-4143747988) **ericnorris** said "@microsoft-github-policy-service agree company="Etsy""

### [Issue microsoft/TypeScript-go#3081](https://github.com/microsoft/TypeScript-go/issues/3081) (Closed)

**Stack overflow in multi\-threaded mode during type instantiation**

*tsgo 7.0.0-dev encounters a goroutine stack overflow in multi-threaded type instantiation on a large React/TypeScript codebase, while single-threaded mode works.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/3081#issuecomment-4059658320) **shahmir-oscilar** found that the error was due to an older react-hook-form version, recommended upgrading to the latest version, and suggested the issue could be closed
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/3081#issuecomment-4059818295) **jakebailey** suggested running TypeScript 6.0 with --stableTypeOrdering to reveal the circular error
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/3081#issuecomment-4061756525) **shahmir-oscilar** tried running TS 6.0 with --stableTypeOrdering and found no errors
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#3086](https://github.com/microsoft/TypeScript-go/issues/3086) (Closed, `Crash`)

**panic: cache entry not found**

*Cloning a project snapshot panics due to a missing RefCountCache entry.*

 * created by **nnnnoel**
 * **nnnnoel** added label `Crash`
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#3118](https://github.com/microsoft/TypeScript-go/pull/3118) (Closed)

**Fix difference between checker and binder resolvers**

*Re-align checker and binder resolvers by restoring getReferencedValueOrAliasSymbol and replacing obsolete symbol resolution functions.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3118#issuecomment-4144324035) **weswigham** discussed the potential for an emit checker mode, noted that PR #1301 addressed some checker-versus-emit issues but introduced regressions, restored getReferencedValueOrAliasSymbol to align with Strada, and asked whether this change regressed VSCode nocheck emit performance or required further fixes
 * [today](https://github.com/microsoft/TypeScript-go/pull/3118#issuecomment-4144343140) **jakebailey** said "I forgot to mention it, but I did check, and it still seems fast. I will recheck."
 * [today](https://github.com/microsoft/TypeScript-go/pull/3118#issuecomment-4145012454) **jakebailey** compared performance metrics of the tsgo binary before #2396, on main, and in this PR using a quick bash script on VSCode

### [PR microsoft/TypeScript-go#3176](https://github.com/microsoft/TypeScript-go/pull/3176) (Closed)

**Fix ref count cache inconsistencies**

*Revert cache ref-count simplification so parse cache entries start with refCount 1 and prevent premature deletion.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3176#issuecomment-4138432989) **typescript-bot** reported panic stack trace during textDocument/rename cross-project handling
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3176#issuecomment-4138433067) **typescript-bot** reported a panic handling a textDocument/formatting request when running the top 100 repos suite
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3176#issuecomment-4138433136) **typescript-bot** reported a panic stack trace from textDocument/definition when running the top 100 repos suite
 * [today](https://github.com/microsoft/TypeScript-go/pull/3176#issuecomment-4143918623) **andrewbranch** Downloaded and tested repros, confirmed they failed on main, and planned to fix the merge conflict before merging
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#3180](https://github.com/microsoft/TypeScript-go/issues/3180) (Closed)

**Union ordering printback differs due to some lack of node reuse**

*Printback output for union types varies in ordering because nodes are not consistently reused.*

 * created by **RyanCavanaugh**
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#3181](https://github.com/microsoft/TypeScript-go/issues/3181) (Closed)

**\`\| undefined\` in optional parameters/properties unexpectedly printed back in types / \.d\.ts emit**

*TypeScript unexpectedly includes `| undefined` in emitted declaration files for optional parameters and properties.*

 * created by **RyanCavanaugh**
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/3181#issuecomment-4113898845) **AlejandroGispert** said "Hi @RyanCavanaugh, if still available I would like to take on this issue."
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/3181#issuecomment-4113962826) **AlejandroGispert** said "Never mind, I see this was already closed. Thanks!"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#3200](https://github.com/microsoft/TypeScript-go/issues/3200) (Closed, `Type Ordering`)

**Complex deeply nested types compile differently**

*Complex deeply nested TypeScript types compile correctly with tsc@6.0 but error under tsgo due to constraint mismatches.*

 * created by **ekwoka**
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/3200#issuecomment-4110001792) **jakebailey** suggested passing --stableTypeOrdering in TypeScript 6.0
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/3200#issuecomment-4110035663) **ekwoka** observed that TypeScript 6.0 and tsgo both failed while the latest TSC succeeded, noted that TSC computed the correct type despite the error claiming 'unknown', and highlighted the curious behavioral difference
 * **RyanCavanaugh** added label `Type Ordering`
 * [today](https://github.com/microsoft/TypeScript-go/issues/3200#issuecomment-4143633232) **RyanCavanaugh** said "Type ordering issues are pretty hard to figure out and even more difficult to explain, unfortunately."
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#3204](https://github.com/microsoft/TypeScript-go/issues/3204) (Closed, `Crash`, **DanielRosenwasser**, **jakebailey**, **Copilot**)

**Panic with \`declarationMap\` in version 7\.0\.0\-dev\.20260323\.1**

*typescript-go 7.0.0-dev.20260323.1 panics with a slice bounds out of range error in scanner.SkipTriviaEx while generating declarationMap*

 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/3204#issuecomment-4115293270) **RohinBhargava** provided another repro link for tsgo-repro-3202
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/3204#issuecomment-4120631561) **DanielRosenwasser** said "You can temporarily turn declarationMap off if you want to unblock yourself until we have a fix."
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/3204#issuecomment-4120992116) **RohinBhargava** said "Yeah, unfortunately I need it on right now, but downgrading is fine for me right now!"
 * (today) **DanielRosenwasser** assigned to **Copilot**, **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3204#issuecomment-4144076140) **jakebailey** said "The changes I have do not actually fix this issue. (referring to a different branch; #3274 should fix this)"

### [PR microsoft/TypeScript-go#3208](https://github.com/microsoft/TypeScript-go/pull/3208) (Closed)

**\[API\] Formatting bug fixes**

*Add PrintNodeOptions support to API and Go printer with emitter.withOptions, fix emitLiteral handling for terminateUnterminatedLiterals, and add related tests.*

 * created by **navya9singh**
 * (today) **navya9singh** closed the issue

### [PR microsoft/TypeScript-go#3217](https://github.com/microsoft/TypeScript-go/pull/3217) (Open)

**Watch cli efficiency update**

*Watch CLI efficiency improvements implement debouncing, configuration caching, and dependency parsing to avoid unnecessary recompilations.*

 * created by **johnfav03**
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/3217#issuecomment-4127784005) **andrewbranch** highlighted missing include wildcard handling and proposed decoupling watcher logic from build logic for LSP integration
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/3217#issuecomment-4129133587) **johnfav03** described implementing the change by separating file tracking into a FileWatcher struct with a callback linked to doCycle while keeping caches, program construction, and emitting logic in the Watcher wrapper
 * [today](https://github.com/microsoft/TypeScript-go/pull/3217#issuecomment-4143654633) **andrewbranch** expressed that the commit wasn’t sufficient for wildcard watching, asked what “incremental skips emit for new unreferenced file” means, and suggested reading the directory recursively to detect new files

### [Issue microsoft/TypeScript-go#3227](https://github.com/microsoft/TypeScript-go/issues/3227) (Open, `possible improvement`, **DanielRosenwasser**, **Copilot**)

**Track file type or extension for failing requests**

*Track file extensions for failing requests to aid in reproducing crashes and identifying language-specific issues.*

 * created by **DanielRosenwasser**
 * (2 days ago) **DanielRosenwasser** assigned to **Copilot**, **DanielRosenwasser**
 * **RyanCavanaugh** added label `possible improvement`

### [PR microsoft/TypeScript-go#3233](https://github.com/microsoft/TypeScript-go/pull/3233) (Closed)

**adding to isTypeNode\(\)**

*Extend isTypeNode to include keyword, expression, and JSDoc type nodes, preventing visitEachChild assertion failures.*

 * created by **navya9singh**
 * (today) **navya9singh** closed the issue

### [Issue microsoft/TypeScript-go#3242](https://github.com/microsoft/TypeScript-go/issues/3242) (Open, `bug`, **RyanCavanaugh**, **Copilot**)

**No error for values named 'Object' \(in CommonJS\)**

*TypeScript incorrectly permits a class named Object to be used with object spread in CommonJS modules without reporting an error.*

 * created by **DanielRosenwasser**
 * (today) **RyanCavanaugh** added label `bug`, and assigned to **Copilot**, **RyanCavanaugh**

### [Issue microsoft/TypeScript-go#3249](https://github.com/microsoft/TypeScript-go/issues/3249) (Open, `possible improvement`)

**Report perf measurements from extension**

*Collect and report performance metrics for language service operations in the extension to track regressions and improvements.*

 * created by **DanielRosenwasser**
 * **DanielRosenwasser** added to milestone `TypeScript 7.0 RC`
 * **RyanCavanaugh** added label `possible improvement`

### [Issue microsoft/TypeScript-go#3250](https://github.com/microsoft/TypeScript-go/issues/3250) (Open, `feature parity`)

**Reimplement "find file references"**

*Reimplement find file references for JS/TS files by extending multi-project search beyond document positions.*

 * created by **DanielRosenwasser**
 * **RyanCavanaugh** added label `feature parity`

### [Issue microsoft/TypeScript-go#3253](https://github.com/microsoft/TypeScript-go/issues/3253) (Closed, `bug`)

**Inconsistent output from \-\-listFilesOnly**

*tsgo’s --listFilesOnly option returns non-deterministic file listings across runs when importing from complex node_modules packages*

 * created by **matthewvalentine**
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3253#issuecomment-4139334905) **jakebailey** said "For tsgo, can you try passing --deduplicatePackages false and see if that stabilizes it?"
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3253#issuecomment-4139355908) **jakebailey** said "Tested it myself, and that does indeed fix it. Thanks, I've been looking for this kind of repro for a flaky test I've been trying to figure out."
 * **RyanCavanaugh** added label `bug`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3254](https://github.com/microsoft/TypeScript-go/pull/3254) (Closed)

**Sort peer deps in readPackageJsonPeerDependencies**

*Add alphabetical sorting of peer dependencies in readPackageJsonPeerDependencies to ensure consistent ordering.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3258](https://github.com/microsoft/TypeScript-go/pull/3258) (Closed)

**Fix file dedupe fourslash flake**

*Incomplete cycle detection in UpdateProgram and reusing modified package.json files provoke intermittent fourslash dedupe flakes.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3259](https://github.com/microsoft/TypeScript-go/issues/3259) (Open, `possible improvement`)

**Proposal: Flatten the AST to speed up tsgo**

*Proposes flattening tsgo’s AST into a flat array to reduce garbage collection scanning overhead and improve performance.*

 * created by **no-yan**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3259#issuecomment-4143065149) **jakebailey** noted that implementing data-oriented design would be painful and that Go’s new "green tea" garbage collector and existing arena allocation likely already provide most benefits, added that Go’s concurrent GC might run on idle cores and suggested that excessive allocations elsewhere could be the real issue
 * [today](https://github.com/microsoft/TypeScript-go/issues/3259#issuecomment-4143117997) **jakebailey** acknowledged GOGC was disabled and wondered if adjusting it during compilation could improve performance
 * **RyanCavanaugh** added label `possible improvement`
 * [today](https://github.com/microsoft/TypeScript-go/issues/3259#issuecomment-4144353592) **DanielRosenwasser** explained that replacing pointers with indexes would complicate API by requiring arena context and noted that slimming down nodeData was risky with minimal savings
 * [today](https://github.com/microsoft/TypeScript-go/issues/3259#issuecomment-4144699877) **ahejlsberg** suggested disabling GC for command-line compiles due to minimal GC-eligible allocations
 * [today](https://github.com/microsoft/TypeScript-go/issues/3259#issuecomment-4147318834) **no-yan** clarified that the goal was reducing GC scan cost rather than DoD/locality, explained that GC still scans contiguous nodes containing pointers, suggested making large pointer-free regions to avoid scanning, and recommended disabling or tuning GC for command-line compiles

### [Issue microsoft/TypeScript-go#3267](https://github.com/microsoft/TypeScript-go/issues/3267) (Closed, `Crash`)

**panic when \`declarationMap\` is enabled**

*A recent change causes enabling declarationMap to panic with a slice bounds out-of-range error during source map emission.*

 * created by **liuxingbaoyu**
 * **liuxingbaoyu** added label `Crash`
 * [today](https://github.com/microsoft/TypeScript-go/issues/3267#issuecomment-4144061981) **DanielRosenwasser** said "I believe this is a duplicate of #3204."
 * (today) **DanielRosenwasser** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/issues/3267#issuecomment-4145055987) **liuxingbaoyu** said "Sorry, I searched, but for some reason I don't find that."

### [PR microsoft/TypeScript-go#3268](https://github.com/microsoft/TypeScript-go/pull/3268) (Open, **RyanCavanaugh**, **Copilot**)

**Fix missing TS2725 error for class named 'Object' in non\-ES2015 modules**

*Implement a collision check in the Go TypeScript checker to report TS2725 when a class is named 'Object' in CommonJS modules.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3268#issuecomment-4143847388) **jakebailey** said "Why not fix #2087 and fix all of these?"

### [PR microsoft/TypeScript-go#3269](https://github.com/microsoft/TypeScript-go/pull/3269) (Closed)

**Fix document highlights for require property destructuring**

*Fix document highlight handling to prevent crashes when destructuring properties from require calls.*

 * created by **Andarist**
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript-go#3270](https://github.com/microsoft/TypeScript-go/pull/3270) (Closed, **DanielRosenwasser**, **Copilot**)

**Fix declarationMap panic on cross\-file reused nodes**

*Add bounds checks to prevent slice bounds panics when emitting declaration maps for AST nodes reused from other files.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3270#issuecomment-4144391482) **DanielRosenwasser** said "This is not a good fix. You can only emit a position if a given node belongs to the containing tree, and that's not always the case."
 * [today](https://github.com/microsoft/TypeScript-go/pull/3270#issuecomment-4144421535) **jakebailey** said "This is wrong. #3274"

### [PR microsoft/TypeScript-go#3271](https://github.com/microsoft/TypeScript-go/pull/3271) (Open)

**Fix for a snapshot update with a nil CommandLine**

*Add a nil check in NewProjectResponse to prevent panics when handling projects with nil CommandLine during snapshot updates.*

 * created by **navya9singh**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3271#issuecomment-4145607075) **andrewbranch** said "When does a project have a nil CommandLine?"

### [PR microsoft/TypeScript-go#3272](https://github.com/microsoft/TypeScript-go/pull/3272) (Closed)

**Investigate stylex Options import regression**

*Investigate and resolve the regression preventing proper import of Options in stylex*

 * created by **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#3273](https://github.com/microsoft/TypeScript-go/pull/3273) (Closed)

**Remove "open a PR" from agent instructions**

*Remove the 'open a PR' agent instruction to stop Copilot subagents from inadvertently creating pull requests.*

 * created by **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#3274](https://github.com/microsoft/TypeScript-go/pull/3274) (Closed)

**Fix declarationMap crash, text ranges**

*Improves text range handling in declarationMap to prevent crashes and resolve related bugs.*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#3275](https://github.com/microsoft/TypeScript-go/pull/3275) (Closed)

**perf: remove extra func call in \`getConditionalTypeInstantiation\`**

*Eliminate an unnecessary function call in getConditionalTypeInstantiation to clean up the code and slightly improve performance.*

 * created by **camc314**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3276](https://github.com/microsoft/TypeScript-go/issues/3276) (Closed, `bug`, **ahejlsberg**)

**Intermittent typecheck error on optional inline object method parameter**

*tsgo intermittently produces a typecheck error for an optional inline object method parameter in a large TypeScript codebase*

 * created by **fadookie**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3276#issuecomment-4145755997) **RyanCavanaugh** thanked and provided a reproduction case with code files and noted compiler behaviors with and without the --singleThreaded flag
 * [today](https://github.com/microsoft/TypeScript-go/issues/3276#issuecomment-4145779446) **RyanCavanaugh** provided a single-file version to demonstrate triggerability depending on resolution order of incoming files
 * [today](https://github.com/microsoft/TypeScript-go/issues/3276#issuecomment-4145822935) **fadookie** thanked the maintainers and reported that using --singleThreaded mode reproduced the error when importing ProblematicInterface in a separate file but not when consuming it in the same file
 * (today) **RyanCavanaugh** added label `bug`, and assigned to **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3276#issuecomment-4145837663) **RyanCavanaugh** described Copilot’s proposed fix to skip the type cache for binding elements and outlined the root cause involving optional types being cached due to goroutine scheduling

### [PR microsoft/TypeScript-go#3277](https://github.com/microsoft/TypeScript-go/pull/3277) (Open, **DanielRosenwasser**, **Copilot**)

**Implement "find file references"**

*Implement a VS Code command and LSP extension to find all files importing or referencing a given JavaScript/TypeScript file.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **DanielRosenwasser**

### [Issue microsoft/TypeScript-go#3278](https://github.com/microsoft/TypeScript-go/issues/3278) (Closed, `Domain: Editor`, **jakebailey**)

**Add one\-time prompt to enable extension**

*Add a one-time prompt to enable the native preview language server when the extension is first activated.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** added label `Domain: Editor`, and assigned to **jakebailey**

### [PR microsoft/TypeScript-go#3279](https://github.com/microsoft/TypeScript-go/pull/3279) (Closed)

**Set js/ts\.experimental\.useTsgo on first run**

*Automatically enable the js/ts.experimental.useTsgo setting on first activation when unset.*

 * created by **jakebailey**

### [Issue microsoft/TypeScript-go#3280](https://github.com/microsoft/TypeScript-go/issues/3280) (Closed)

**\[ServerErrors\]\[TypeScript\] main vs **

*The TypeScript main branch pipeline analyzing 300 popular GitHub repositories encountered server errors and yielded mixed analysis outcomes.*

 * created by **typescript-bot**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3280#issuecomment-4145864485) **typescript-bot** reported a panic during textDocument/rename request due to a nil pointer dereference with accompanying stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/3280#issuecomment-4145864512) **typescript-bot** reported a panic during textDocument/rename due to slice bounds out of range
 * [today](https://github.com/microsoft/TypeScript-go/issues/3280#issuecomment-4145864540) **typescript-bot** reported a panic during textDocument/formatting with a Debug failure and stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/3280#issuecomment-4145864565) **typescript-bot** reported a panic in textDocument/formatting with a debug failure assertion and provided a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/3280#issuecomment-4145864600) **typescript-bot** reported a runtime panic due to an index out of range error in textDocument/completion
 * [today](https://github.com/microsoft/TypeScript-go/issues/3280#issuecomment-4145864654) **typescript-bot** reported a premature server connection closure and provided error details with affected repository information, request logs, and repro steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/3280#issuecomment-4145864685) **typescript-bot** reported server connection closed prematurely with undefined error and provided raw error logs and replay commands
 * [today](https://github.com/microsoft/TypeScript-go/issues/3280#issuecomment-4145864700) **typescript-bot** reported a server connection closed prematurely error and supplied reproduction steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/3280#issuecomment-4145864719) **typescript-bot** reported that the server connection closed prematurely with undefined and provided affected repository details, raw error text, replay commands, recent requests, and repro steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/3280#issuecomment-4145864751) **typescript-bot** reported a server connection closed prematurely error with affected repos and replay commands
 * [today](https://github.com/microsoft/TypeScript-go/issues/3280#issuecomment-4145864801) **typescript-bot** reported a runtime panic while handling textDocument/completion due to index out of range

### [Issue microsoft/TypeScript-go#3281](https://github.com/microsoft/TypeScript-go/issues/3281) (Closed)

**\[ServerErrors\]\[TypeScript\] main vs **

*The TypeScript error-deltas pipeline reported errors, timeouts, and failures while analyzing 300 popular GitHub repositories on main.*

 * created by **typescript-bot**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3281#issuecomment-4145960484) **typescript-bot** reported a panic handling request textDocument/rangeFormatting with a debug failure: False expression: Token end is child end
 * [today](https://github.com/microsoft/TypeScript-go/issues/3281#issuecomment-4145960503) **typescript-bot** reported a runtime panic with stack trace and provided repro steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/3281#issuecomment-4145960517) **typescript-bot** reported a panic during cross-project handling of textDocument/rename due to an invalid memory address or nil pointer dereference
 * [today](https://github.com/microsoft/TypeScript-go/issues/3281#issuecomment-4145960540) **typescript-bot** reported a panic due to invalid memory address or nil pointer dereference during textDocument/rename
 * [today](https://github.com/microsoft/TypeScript-go/issues/3281#issuecomment-4145960565) **typescript-bot** reported a panic in rangeFormatting due to a debug failure (False expression: Token end is child end) and provided the stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/3281#issuecomment-4145960582) **typescript-bot** reported a panic: unimplemented error with stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/3281#issuecomment-4145960612) **typescript-bot** reported a panic due to a debug failure in textDocument/rangeFormatting
 * [today](https://github.com/microsoft/TypeScript-go/issues/3281#issuecomment-4145960647) **typescript-bot** reported a panic in textDocument/formatting due to a debug failure and provided a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/3281#issuecomment-4145960697) **typescript-bot** reported a runtime panic caused by invalid memory address or nil pointer dereference during cross-project handling
 * [today](https://github.com/microsoft/TypeScript-go/issues/3281#issuecomment-4145960800) **typescript-bot** reported a server connection closed prematurely error and supplied affected repo, error artifacts, last requests, and repro steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/3281#issuecomment-4145960901) **typescript-bot** reported a premature server connection closure and provided affected repo, raw error text, replay commands, request logs, and reproduction steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/3281#issuecomment-4145960967) **typescript-bot** reported a server connection closed prematurely error and provided affected repos, request logs, and repro steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/3281#issuecomment-4145961000) **typescript-bot** reported a premature server connection closure error with undefined message and provided affected repos, error artifacts, recent requests, and repro steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/3281#issuecomment-4145961026) **typescript-bot** reported a panic during textDocument/formatting due to a debug failure "False expression: Token end is child end"

