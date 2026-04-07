# Report for 2026-04-01 (Wednesday, April 1st, 2026)

17 different users commented on 76 different issues.

## Activity Summary

### [Issue microsoft/TypeScript-go#1010](https://github.com/microsoft/TypeScript-go/issues/1010) (Closed, `Domain: Editor`, `Needs More Info`)

**\[lsp\]\[bug\] LSP sometimes won't successfully restart**

*Restarting the TypeScript Native Preview language server in VS Code sometimes fails to shut down the existing process, leaving zombie tsgo processes.*

 * [43 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1010#issuecomment-2928440184) **jakebailey** said "Is there any chance you could get an LSP message log from the output window, or at least the end of it (sanitized) when this happens?"
 * [43 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1010#issuecomment-2928611162) **mjames-c** shared sanitized LSP server and client logs and noted odd watched directories that seemed unrelated
 * **jakebailey** added label `LSP`
 * **RyanCavanaugh** added label `Needs More Info`
 * [today](https://github.com/microsoft/TypeScript-go/issues/1010#issuecomment-4172510976) **RyanCavanaugh** said "We'll definitely some kind of concrete way to repro this in order to have a chance at fixing it"
 * [today](https://github.com/microsoft/TypeScript-go/issues/1010#issuecomment-4173240346) **mjames-c** said "Closing this out. From my testing this morning seems to be fixed."
 * (today) **mjames-c** closed the issue

### [Issue microsoft/TypeScript-go#1042](https://github.com/microsoft/TypeScript-go/issues/1042) (Open, `Domain: JS`, **sandersn**, **RyanCavanaugh**, **Copilot**)

**Improve \`@overload\` error message to mention name of host function**

*Improve the @overload error message to include the function’s name when missing a return-type annotation.*

 * created by **sandersn**
 * **jakebailey** added label `Domain: JS`
 * (today) **RyanCavanaugh** assigned to **Copilot**, **RyanCavanaugh**, **sandersn**

### [Issue microsoft/TypeScript-go#1062](https://github.com/microsoft/TypeScript-go/issues/1062) (Closed, `Domain: tsconfig`, `Domain: Performance`)

**noEmit slow on Mac M2**

*TypeScript native-preview’s noEmit type checking runs slower than standard tsc on a Mac M2.*

 * **jakebailey** added label `Domain: tsconfig`
 * [35 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1062#issuecomment-3137947557) **jakebailey** said "Been a while, but can you try out #1483?"
 * **jakebailey** added label `Domain: Performance`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#1088](https://github.com/microsoft/TypeScript-go/issues/1088) (Closed, `Domain: Type Checking`)

**Inconsistent behavior between \`tsc\` and \`tsgo\` for \`@ts\-expect\-error\` directive placement**

*Inconsistent handling of @ts-expect-error directive placement for TS2769 overload errors between tsc and tsgo*

 * created by **cartond**
 * **jakebailey** added label `Domain: Type Checking`
 * [42 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1088#issuecomment-2952790544) **muglug** provided a single file reproducer
 * [today](https://github.com/microsoft/TypeScript-go/issues/1088#issuecomment-4171575443) **RyanCavanaugh** said "We don't provide any guarantees on error spans when either error is valid, which is the case here. A type assertion will always be the preferred mechanism to deal with situations like this."
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#1147](https://github.com/microsoft/TypeScript-go/issues/1147) (Open, `Domain: Editor`, `Needs More Info`)

**vs code typescript go extension taking long time to typecheck for large monorepo**

*TypeScript native preview extension in VS Code experiences prolonged hover type-checking in a large monorepo, whereas normal tsc works fine.*

 * [42 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1147#issuecomment-2960341216) **shmdhussain** shared logs after restarting the language server, suspected an issue with the type watcher or number of files checked, and offered to provide further info
 * [42 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1147#issuecomment-2960357559) **shmdhussain** attached LSP server logs after opening a file and watching the TypeScript native preview output
 * **jakebailey** removed label `Needs More Info`
 * [today](https://github.com/microsoft/TypeScript-go/issues/1147#issuecomment-4172933315) **RyanCavanaugh** provided a relevant callstack from the log showing a panic in Node.Expression
 * **RyanCavanaugh** added label `Needs More Info`
 * [today](https://github.com/microsoft/TypeScript-go/issues/1147#issuecomment-4173232162) **RyanCavanaugh** said "We need a repro or at least some clues for sure, there doesn't seem to be any way to get into this state"

### [Issue microsoft/TypeScript-go#1600](https://github.com/microsoft/TypeScript-go/issues/1600) (Closed, `Domain: Editor`, **weswigham**)

**Hovering an optional boolean param in strict mode shows \`param?: boolean \| undefined\`**

*Hovering over an optional boolean parameter in strict mode shows it as boolean | undefined instead of boolean*

 * created by **jakebailey**
 * **jakebailey** added label `Domain: Editor`
 * [32 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1600#issuecomment-3201713699) **jakebailey** said "Unsurprisingly, this comes down to serializeTypeForDeclaration missing node reuse."
 * **RyanCavanaugh** assigned to **weswigham**

### [Issue microsoft/TypeScript-go#1701](https://github.com/microsoft/TypeScript-go/issues/1701) (Open, `help wanted`)

**surrogate pair and lone surrogate support in stringLiteral**

*tsgo's Go based stringLiteral parser converts lone UTF-16 surrogates into replacement characters, causing lossy token text compared to TypeScript.*

 * **jakebailey** added label `help wanted`
 * [28 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1701#issuecomment-3283463061) **hardfist** suggested that Go uses WTF-8 for Windows paths and offered to implement it if acceptable
 * [28 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1701#issuecomment-3283625905) **jakebailey** said "Sure, though we of course can't use the syscall package to do this."
 * **RyanCavanaugh** added to milestone `Possible Improvement`

### [Issue microsoft/TypeScript-go#1708](https://github.com/microsoft/TypeScript-go/issues/1708) (Closed, `Domain: Editor`)

**tsgo preview: import suggestions are not aware of paths**

*tsgo preview in Zed lacks path-aware import suggestions provided by vtsls, making it unusable.*

 * [10 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1708#issuecomment-3752807937) **affanshahid** explained how they fixed the issue on Zed by setting importModuleSpecifierPreference in tsgo settings and noted vscode's property mapping difference
 * [10 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1708#issuecomment-3757327834) **longzheng** described using 'importModuleSpecifierPreference' to fix configuration in Zed and VSCode and noted an upcoming PR would correct the parser to use the proper property name
 * [10 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1708#issuecomment-3757811402) **affanshahid** described needing to use both keys to make imports work across different contexts and expressed relief that the issue was fixed
 * [today](https://github.com/microsoft/TypeScript-go/issues/1708#issuecomment-4172587603) **RyanCavanaugh** said "Seems like this is fixed now. Please log a new issue if not since there are a few subthreads here. Thanks!"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#1709](https://github.com/microsoft/TypeScript-go/issues/1709) (Open, `Domain: Editor`)

**Allow to specify import sorting\.**

*Add importSorting options to tsconfig.json allowing configurable prioritization of import path suggestions.*

 * [10 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1709#issuecomment-3752849908) **jpike88** stated they would investigate dprint as a temporary solution, argued that formatting should be a core part of the official library, and pledged to report back on integration feasibility
 * [10 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1709#issuecomment-3752859491) **jpike88** mentioned they already use a zero-dependency TypeScript plugin to sort imports and expressed concern that lacking similar functionality in tsgo would block upgrades and impact productivity
 * [10 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1709#issuecomment-3752954554) **jakebailey** clarified they lacked bandwidth to work on a new feature while porting existing functionality and noted that dprint's TypeScript plugin used an unrelated Wasm-based system
 * **RyanCavanaugh** added to milestone `Post-7.0`

### [Issue microsoft/TypeScript-go#1741](https://github.com/microsoft/TypeScript-go/issues/1741) (Closed, `Domain: Type Checking`, `Domain: Declaration Emit`, **weswigham**)

**tsgo does not use assertion as a source for the type of  a default export\.**

*tsgo ignores type assertions on default exports, causing private name 'Bar' errors instead of using the asserted type.*

 * (26 weeks ago) **jakebailey** added labels `Domain: Type Checking`, `Domain: Declaration Emit`, and removed label `Type Ordering`
 * **RyanCavanaugh** assigned to **weswigham**

### [Issue microsoft/TypeScript-go#1743](https://github.com/microsoft/TypeScript-go/issues/1743) (Closed, `Domain: Type Checking`, `Type Ordering`)

**New error when inferring return type from similar object types with promises**

*tsgo rejects nested Promise return types with similar object shapes due to a new type inference error.*

 * [27 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1743#issuecomment-3325726114) **RyanCavanaugh** demonstrated that swapping the true and false branches still triggered the same type ordering error in TypeScript 5.8
 * **RyanCavanaugh** added label `Type Ordering`
 * **ahejlsberg** added label `Domain: Type Checking`
 * [today](https://github.com/microsoft/TypeScript-go/issues/1743#issuecomment-4171647607) **RyanCavanaugh** said "I don't think we have any good tiebreakers here"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#1762](https://github.com/microsoft/TypeScript-go/issues/1762) (Closed, `Domain: Declaration Emit`, **weswigham**)

**adding a root dir that is a child of another root dir causes different relative paths in declaration**

*Adding a nested rootDirs entry causes tsgo to generate different relative import paths in declarations compared to TypeScript.*

 * created by **dragomirtitian**
 * **jakebailey** added label `Domain: Declaration Emit`
 * **RyanCavanaugh** assigned to **weswigham**

### [Issue microsoft/TypeScript-go#1771](https://github.com/microsoft/TypeScript-go/issues/1771) (Closed, `Domain: Declaration Emit`, **weswigham**)

**Inferred import type in declaration file uses actual path not use rootdirs path**

*In declaration files, inferred import types use the actual source path instead of the configured rootDirs path.*

 * created by **dragomirtitian**
 * [26 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1771#issuecomment-3356149355) **AlCalzone** said "Possibly related to https://github.com/microsoft/typescript-go/issues/1347, although that issue is about symlinked packages."
 * **jakebailey** added label `Domain: Declaration Emit`
 * **RyanCavanaugh** assigned to **weswigham**

### [Issue microsoft/TypeScript-go#1784](https://github.com/microsoft/TypeScript-go/issues/1784) (Closed, `Domain: Declaration Emit`, **weswigham**)

**type alias is resolved in function type causing type to be unnamable**

*Resolving a type alias in a function signature causes an unnamable external type error during declaration emission in tsgo.*

 * created by **dragomirtitian**
 * **jakebailey** added label `Domain: Declaration Emit`
 * **RyanCavanaugh** assigned to **weswigham**

### [Issue microsoft/TypeScript-go#1874](https://github.com/microsoft/TypeScript-go/issues/1874) (Closed, `Domain: Editor`, **johnfav03**)

**\[LSP\] Remove Unused Imports**

*Re-implement the language server’s functionality for automatically removing unused imports.*

 * created by **marioparaschiv**
 * **jakebailey** added label `Domain: Editor`
 * **RyanCavanaugh** assigned to **johnfav03**
 * [today](https://github.com/microsoft/TypeScript-go/issues/1874#issuecomment-4171989816) **johnfav03** said "Fixed in PR #2331 "
 * (today) **johnfav03** closed the issue

### [Issue microsoft/TypeScript-go#1882](https://github.com/microsoft/TypeScript-go/issues/1882) (Open, `Needs More Info`, **johnfav03**)

**Renaming/moving file breaks imports**

*Renaming a TypeScript file in tsgo leads to TS6307 errors due to missing project file listing, unlike TypeScript 5.8.*

 * [16 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1882#issuecomment-3633341647) **jakebailey** suggested that file change/watch updates should suffice instead of didRenameFiles and requested LSP logs
 * [16 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1882#issuecomment-3633387689) **GitMurf** confirmed correct behavior in VSCode and Neovim and stated intent to update the earlier comment
 * [12 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1882#issuecomment-3714016968) **Netail** described that renaming a directory or file in VSCode broke alias and relative imports while dependency imports still worked
 * **RyanCavanaugh** assigned to **johnfav03**

### [Issue microsoft/TypeScript-go#2021](https://github.com/microsoft/TypeScript-go/issues/2021) (Closed, `Domain: API and Extensibility`, **andrewbranch**)

**source file binary format is not work**

*@typescript/ast’s binary format misreads AST nodes due to empty parameter slots and faulty child indexing assumptions.*

 * created by **quininer**
 * **jakebailey** added label `Domain: API and Extensibility`
 * **RyanCavanaugh** assigned to **andrewbranch**

### [Issue microsoft/TypeScript-go#2060](https://github.com/microsoft/TypeScript-go/issues/2060) (Closed, `Needs More Info`)

**Typescript\-go does not infer large generics due to maximum length compiler will serialize**

*typescript-go cannot infer large nested generics for SStruct because the inferred type exceeds the compiler’s maximum serialized length, requiring manual annotations.*

 * [19 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2060#issuecomment-3547546359) **Raynos** noted that TypeScript 5.x was more tolerant of large unions and abandoned creating a reproduction due to complexity
 * [19 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2060#issuecomment-3547570066) **Raynos** suggested adding the count of types to the error message next to the maximum length
 * [17 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2060#issuecomment-3586819628) **liuxingbaoyu** mentioned that Babel encountered the issue in recent versions and provided reproduction steps and a PR link
 * [today](https://github.com/microsoft/TypeScript-go/issues/2060#issuecomment-4172580359) **RyanCavanaugh** said "I'll try to include something in CHANGES.md but this is kind of vague to work from and I'm not sure anyone will read that section anyway 😅"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#2133](https://github.com/microsoft/TypeScript-go/issues/2133) (Open, `Domain: Editor`, **gabritto**)

**Renaming a file results in mis\-identifying the right sconfig file**

*Renaming a .spec.ts file in VSCode makes editor apply the base tsconfig instead of the local one, causing persistent errors.*

 * [18 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2133#issuecomment-3557108039) **lukpsaxo** shared relevant log snippet showing cache statistics and project configuration steps
 * [18 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2133#issuecomment-3557143441) **lukpsaxo** provided the same log after restarting tsgo
 * [15 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2133#issuecomment-3656242346) **PaulRBerg** reported that the issue persisted in the latest version and forced frequent language server restarts
 * **RyanCavanaugh** assigned to **gabritto**

### [Issue microsoft/TypeScript-go#2139](https://github.com/microsoft/TypeScript-go/issues/2139) (Closed, `Type Ordering`)

**Type inference not behaving correctly using Jotai types**

*TypeScript with tsgo misinfers Jotai atom types, causing BaseDocument to be assigned where Message is required.*

 * created by **wojtekmaj**
 * [18 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2139#issuecomment-3560377336) **jakebailey** identified a union ordering difference, provided a Playground link, and tagged @ahejlsberg for insight on a fix or workaround
 * **jakebailey** added label `Type Ordering`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#2169](https://github.com/microsoft/TypeScript-go/issues/2169) (Open, `Domain: Editor`)

**Support for \`workspace/diagnostic\` from LSP 3\.17**

*Implement LSP 3.17 workspace/diagnostics to provide reliable project-wide diagnostics without opening each file.*

 * created by **versecafe**
 * [17 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2169#issuecomment-3597790119) **jakebailey** expressed support for replacing the experimental enableProjectDiagnostics setting with a request-based LSP system
 * **jakebailey** added label `Domain: Editor`
 * **RyanCavanaugh** added to milestone `Post-7.0`

### [Issue microsoft/TypeScript-go#2182](https://github.com/microsoft/TypeScript-go/issues/2182) (Open, `Domain: Editor`, `Non-regression`)

**Completion does not work for generic type extending tuple or array of all partial type**

*VS Code’s TypeScript completion fails to suggest optional properties in generic functions using tuple parameters combined with mapped Record types.*

 * created by **ishowta**
 * **ishowta** added label `Domain: Editor`
 * (today) **RyanCavanaugh** added label `Non-regression`, and set milestone to `Post-7.0`

### [Issue microsoft/TypeScript-go#2187](https://github.com/microsoft/TypeScript-go/issues/2187) (Open, `Domain: Editor`)

**Broken property suggestions due to a successfully contextually typed function**

*When using a contextually typed callback in makeRequest, TypeScript infers QueryParam as unknown and provides incorrect property suggestions.*

 * created by **LukeAbby**
 * **jakebailey** added label `Domain: Editor`
 * **RyanCavanaugh** added to milestone `Post-7.0`

### [Issue microsoft/TypeScript-go#2213](https://github.com/microsoft/TypeScript-go/issues/2213) (Open, `Domain: Editor`, `Needs More Info`)

**unable to restart the tsgo language server, getting timeout**

*Restarting the tsgo language server via VS Code times out and breaks TypeScript features until the extension is disabled.*

 * created by **shmdhussain**
 * **shmdhussain** added label `Domain: Editor`
 * **RyanCavanaugh** added label `Needs More Info`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2213#issuecomment-4171911287) **RyanCavanaugh** said "There's not much to go on here and we haven't seen other reports of this. Anything unusual about your setup? Any other clues? Without a concrete repro I don't think we have much chance of fixing it"

### [Issue microsoft/TypeScript-go#2216](https://github.com/microsoft/TypeScript-go/issues/2216) (Closed, `Domain: Declaration Emit`, **weswigham**)

**TS4094 exported anonymous class type may not be private or protected**

*tsgo throws TS4094 errors when exporting a function using the Region type from wavesurfer.js because its anonymous class includes private or protected members.*

 * created by **nil1511**
 * (16 weeks ago) **ahejlsberg** added label `Domain: Declaration Emit`, and assigned to **weswigham**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2216#issuecomment-4174660537) **nil1511** confirmed that it was working fine in the latest version
 * (today) **nil1511** closed the issue

### [Issue microsoft/TypeScript-go#2227](https://github.com/microsoft/TypeScript-go/issues/2227) (Open, `Domain: Editor`, **RyanCavanaugh**, **Copilot**)

**Port \`move to file\` refactoring**

*Reintroduce the Move to file refactoring from TypeScript 6 into the language server to restore essential automated code relocation functionality.*

 * created by **mjbvz**
 * **jakebailey** added label `Domain: Editor`
 * (today) **RyanCavanaugh** assigned to **Copilot**, **RyanCavanaugh**

### [Issue microsoft/TypeScript-go#2247](https://github.com/microsoft/TypeScript-go/issues/2247) (Open, `Domain: Editor`, **andrewbranch**)

**Auto\-imports insert \`import\` statement into CJS files**

*TypeScript auto-imports ES module syntax into CommonJS .js files with nodeXX module settings instead of require() despite type commonjs.*

 * created by **gebsh**
 * **gebsh** added label `Domain: Editor`
 * **RyanCavanaugh** assigned to **andrewbranch**

### [Issue microsoft/TypeScript-go#2260](https://github.com/microsoft/TypeScript-go/issues/2260) (Open, `Domain: Editor`)

**Inherited methods not merging JSDoc comments**

*tsgo fails to merge inherited JSDoc comments into overridden methods, showing only new @remarks tags.*

 * **jakebailey** added label `Domain: Editor`
 * [15 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2260#issuecomment-3645658993) **a-tarasyuk** provided a test case and sample QuickInfo output demonstrating JSDoc inheritDocTag behavior
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2260#issuecomment-4001095282) **a-tarasyuk** said "I’m still unclear about what the expected behavior should be. Should we consider this as working as by design?  "
 * **RyanCavanaugh** added to milestone `Post-7.0`

### [Issue microsoft/TypeScript-go#2281](https://github.com/microsoft/TypeScript-go/issues/2281) (Closed, `Domain: Editor`)

**Port \`Convert parameters to destructed object\` refactoring**

*Assess porting of the Convert parameters to destructured object refactoring given its bugs and low usage or explore Copilot support.*

 * created by **mjbvz**
 * **jakebailey** added label `Domain: Editor`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2281#issuecomment-4172376541) **RyanCavanaugh** said "This one is definitely not making the port, barring further evidence."
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#2362](https://github.com/microsoft/TypeScript-go/issues/2362) (Closed, `duplicate`)

**LSP diagnostics not working in Emacs's eglot**

*tsgo LSP server fails to publish diagnostics to Emacs’s eglot unlike typescript-language-server, possibly due to client capabilities mismatch.*

 * [15 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2362#issuecomment-3654617423) **joaotavora** explained that he had two open documents and expected the language server to maintain a dependency graph for diagnostic pulls, criticized VSCode's approach as inefficient, and noted having long ago left JavaScript land
 * [10 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2362#issuecomment-3769773262) **dstaley** noted that Nova currently only supports textDocument.publishDiagnostics and expressed doubt that supporting push diagnostics would be justified
 * **RyanCavanaugh** added label `duplicate`
 * (today) **RyanCavanaugh** closed the issue
 * [later](https://github.com/microsoft/TypeScript-go/issues/2362#issuecomment-4175450673) **edkolev** mentioned that eglot added support for pull diagnostics in December 2025 and corrected the term from push to pull
 * [later](https://github.com/microsoft/TypeScript-go/issues/2362#issuecomment-4175800808) **joaotavora** corrected that "push diagnostics" should be "pull diagnostics"

### [Issue microsoft/TypeScript-go#2386](https://github.com/microsoft/TypeScript-go/issues/2386) (Open, `Domain: Editor`, **gabritto**)

**TS2307 Delete a folder of \`\.ts\` files does not trigger \`ts\(2307\)\` error hint**

*VSCode does not display a ts(2307) missing module error when a referenced folder of .ts files is deleted*

 * created by **ColaFanta**
 * **ColaFanta** added label `Domain: Editor`
 * **RyanCavanaugh** assigned to **gabritto**

### [Issue microsoft/TypeScript-go#2398](https://github.com/microsoft/TypeScript-go/issues/2398) (Open, `Domain: Editor`)

**Client typescript\.native\-preview\-lsp: connection to server is erroring**

*TypeScript Native Preview fails to start in an air-gapped Windows Server to RHEL environment, reporting write EPIPE and execution errors.*

 * created by **brammitch**
 * **brammitch** added label `Domain: Editor`
 * **RyanCavanaugh** added to milestone `Post-7.0`

### [Issue microsoft/TypeScript-go#2443](https://github.com/microsoft/TypeScript-go/issues/2443) (Open, `documentation`, **RyanCavanaugh**)

**\[Doc\]: paths map value points to removed baseUrl value**

*Inline documentation incorrectly references the removed baseUrl option for computing paths map values.*

 * created by **tanepiper**
 * [11 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2443#issuecomment-3720182702) **jakebailey** mentioned the source of the tooltips in schemastore and suggested updating them with neutral language
 * **RyanCavanaugh** added label `documentation`
 * **RyanCavanaugh** assigned to **RyanCavanaugh**

### [Issue microsoft/TypeScript-go#2444](https://github.com/microsoft/TypeScript-go/issues/2444) (Closed, `Domain: Editor`, **iisaduan**)

**Missing code actions \(\`editor\.codeActionsOnSave\`\) with \`typescript\.experimental\.useTsgo\` in VSCode**

*Enabling typescript.experimental.useTsgo in VSCode disables most code actions on save, preventing missing imports from being added automatically.*

 * (6 weeks ago) **johnfav03** closed the issue
 * (6 weeks ago) **iisaduan** reopened the issue
 * [6 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2444#issuecomment-3900454711) **virtuallyunknown** thanked @iisaduan and clarified that they meant behavior when imports are missing before any import happens and said they would check the suggested settings
 * **RyanCavanaugh** assigned to **iisaduan**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2444#issuecomment-4173574611) **iisaduan** separated the remaining unimplemented actions into individual issues (#3318, #3320, #3319) and marked organizeImports, removeUnusedImports, and sortImports as done
 * (today) **iisaduan** closed the issue

### [Issue microsoft/TypeScript-go#2455](https://github.com/microsoft/TypeScript-go/issues/2455) (Closed, `Needs More Info`)

**TSGO not reporting TS2548**

*TSGO reports TS6133 but omits the TS2548 error when spreading a value typed as unknown[]|null.*

 * [11 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2455#issuecomment-3729341477) **Titozzz** said "I'll try to either narrow it down to a small reproduction, or, find what causes my issue and will be back to you. "
 * [11 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2455#issuecomment-3738468999) **Titozzz** noted that omitting or setting a deprecated ‘target’ to “es5” reproduced the issue and asked about an incremental caching annoyance and whether to open a new issue
 * [9 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2455#issuecomment-3786769504) **ahejlsberg** asked for the tsconfig.json file and clarified if part of the repro was missing
 * [today](https://github.com/microsoft/TypeScript-go/issues/2455#issuecomment-4173115060) **RyanCavanaugh** said "Closing due to lack of repro"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#2457](https://github.com/microsoft/TypeScript-go/issues/2457) (Open, `feature parity`, **jakebailey**)

**Proposal: Prettified type display in hover output**

*Add optional settings to display prettified, expanded types in hover output for better readability.*

 * [1 month ago](https://github.com/microsoft/TypeScript-go/issues/2457#issuecomment-3974008251) **EvgenyOrekhov** stated that VS Code now supports this natively and showed how to increase hover verbosity by clicking '+'
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2457#issuecomment-4005963689) **rubnogueira** said "This is part of TypeScript 5.9: https://devblogs.microsoft.com/typescript/announcing-typescript-5-9-beta/#expandable-hovers-(preview) but it's not implemented in tsgo."
 * **RyanCavanaugh** added label `feature parity`
 * **RyanCavanaugh** assigned to **jakebailey**

### [Issue microsoft/TypeScript-go#2555](https://github.com/microsoft/TypeScript-go/issues/2555) (Open, `Domain: Editor`, **andrewbranch**)

**Installing Native Preview broke TS Imports**

*Installing VS Code’s Native Preview TypeScript extension on macOS breaks TypeScript auto-import suggestions despite reverting settings and reinstalling the editor.*

 * [9 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2555#issuecomment-3798728940) **tikki100** said "Related?: https://github.com/microsoft/typescript-go/issues/2582"
 * [9 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2555#issuecomment-3800314263) **ericnorris** stated that their issue was about the types field in package.json, not compilerOptions in tsconfig.json
 * [9 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2555#issuecomment-3809296472) **DanielRosenwasser** informed that a PR addressing the autocomplete issue had been submitted
 * **RyanCavanaugh** assigned to **andrewbranch**

### [Issue microsoft/TypeScript-go#2626](https://github.com/microsoft/TypeScript-go/issues/2626) (Closed, `Domain: Editor`, `Needs More Info`)

**Extension softly crashes \(hangs indefinitely\) at sudden**

*The TypeScript extension v0.20260131.1 hangs and shows stale diagnostics when experimental useTsgo and project diagnostics are enabled, requiring restarts.*

 * created by **piscopancer**
 * **piscopancer** added label `Domain: Editor`
 * **RyanCavanaugh** added label `Needs More Info`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2626#issuecomment-4172369783) **RyanCavanaugh** said "This is very odd. We'd need some other clues to investigate. What's possibly unusual about your setup?"

### [Issue microsoft/TypeScript-go#2637](https://github.com/microsoft/TypeScript-go/issues/2637) (Open, `Domain: Editor`, **johnfav03**)

**Update import via Quick Fix breaks import formatting**

*Quick Fix import update breaks one-line named import formatting by adding an extra newline and misplacing the closing bracket.*

 * created by **erengeez**
 * **erengeez** added label `Domain: Editor`
 * **RyanCavanaugh** assigned to **johnfav03**

### [Issue microsoft/TypeScript-go#2698](https://github.com/microsoft/TypeScript-go/issues/2698) (Closed, `Type Ordering`)

**Behavior Difference: Error TS2456: Type alias circularly references itself**

*tsgo incorrectly reports circular type alias errors for StaticParamList that compile without errors in TypeScript 6.0*

 * [6 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2698#issuecomment-3886882717) **davidjbng** provided a diff that resolved the error and asked if this change is expected during upgrade to tsgo or will be fixed in TypeScript 7
 * **ahejlsberg** added label `Type Ordering`
 * [6 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2698#issuecomment-3887449579) **ahejlsberg** stated that the error was due to type ordering and would not be changed
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#2824](https://github.com/microsoft/TypeScript-go/issues/2824) (Open, `Domain: API and Extensibility`, **andrewbranch**)

**API usage patterns for complex editor extensions**

*Exploring IPC-based API features for a Go TS server to replace TS Server plugins and support Vue editor extensions*

 * [1 month ago](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-3963097012) **johnsoncodehk** suggested a pull-based plugin mechanism for CLI and LSP to resolve non-standard files, outlined cross-language and mapping challenges, and mentioned a concrete PR
 * [1 month ago](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-3965169605) **remcohaszing** suggested using JSON-RPC over IPC, avoiding stdout, and adding an initialize call for plugins to register file extensions, noting uncertainty about the Next.js TypeScript plugin’s functionality
 * [1 month ago](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-3987350807) **atscott** described Angular’s reliance on generating virtual TypeScript files and explained the re-engineering challenges introduced by the proposed TS Go API direction
 * [today](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-4172657295) **lppedd** suggested dynamically loaded WebAssembly binaries via the WASI Component Model, noted uncertainty about Go's WASI support, and mentioned that Rust appeared to have the edge
 * [today](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-4172677285) **jakebailey** mentioned that Wasm would not help unless a Wasm runtime was shipped or execution was always launched via NAPI
 * [today](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-4172684436) **lppedd** mentioned that shipping a Wasm runtime in the binary could enable a multilanguage plugin ecosystem and was a reasonable idea

### [Issue microsoft/TypeScript-go#2830](https://github.com/microsoft/TypeScript-go/issues/2830) (Closed, `Type Ordering`)

**TS2859/TS2590: bigint template literal types composed with distributive conditional cause 'excessively deep' errors not present in tsc**

*bigint-based template literal types in JSX props cause tsgo to report excessive type complexity errors but not tsc*

 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2830#issuecomment-3924386199) **jlaneve** said "in the spirit of transparency these comments / repros were generated with the help of claude code, but I figured it'd be worth posting because this is a real issue we're running into"
 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2830#issuecomment-3928610921) **ahejlsberg** described the problem as a type ordering issue replicable with `tsc --stableTypeOrdering` in TS 6.0 and noted it might occur with plain `tsc` too, concluding there's likely no fix
 * **ahejlsberg** added label `Type Ordering`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#2859](https://github.com/microsoft/TypeScript-go/issues/2859) (Closed)

**\`gql\.tada\` performing better with \`\-\-singleThreaded\` than without it**

*tsgo without --singleThreaded runs significantly slower than with it when generating gql.tada types due to union caching inefficiencies.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2859#issuecomment-4058286993) **ahejlsberg** analyzed fragment file dependencies, measured command performance, and concluded that tsgo is ~6x faster than tsc and behaves as expected
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2859#issuecomment-4060416384) **evsasse** thanked Anders and said they would refine the minimal reproduction while noting unexpected compiler performance differences
 * **RyanCavanaugh** added label `Needs More Info`
 * **RyanCavanaugh** removed label `Needs More Info`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2859#issuecomment-4171870049) **RyanCavanaugh** said "Please log a new issue if you find anything else suspect. Thanks!"
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#2944](https://github.com/microsoft/TypeScript-go/pull/2944) (Open)

**\[draft\] more formatting tests **

*Add draft formatting tests to validate and troubleshoot the repository’s testing pipelines.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2944#issuecomment-4165297450) **typescript-bot** said "@iisaduan, the perf run you requested failed. You can check the log here."
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2944#issuecomment-4166370276) **typescript-bot** provided the requested performance run results including a detailed comparison report table
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2944#issuecomment-4166390637) **typescript-bot** said "@iisaduan, the perf run you requested failed. You can check the log here."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2944#issuecomment-4172313798) **iisaduan** said "@typescript-bot test top100"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2944#issuecomment-4172314407) **typescript-bot** provided a build status update with links to the test top100 job start and results
 * [today](https://github.com/microsoft/TypeScript-go/pull/2944#issuecomment-4172722240) **typescript-bot** reported that running the top 400 repos with tsc comparing main and the PR merge looked good
 * [today](https://github.com/microsoft/TypeScript-go/pull/2944#issuecomment-4173701578) **typescript-bot** said "@iisaduan, the perf run you requested failed. You can check the log here."

### [Issue microsoft/TypeScript-go#2974](https://github.com/microsoft/TypeScript-go/issues/2974) (Open, `Domain: Editor`, **andrewbranch**)

**Missing auto\-import for subpath imports of other local packages**

*VS Code TypeScript auto-imports fail to recognize subpath imports from sibling local workspace packages.*

 * **psznm** added label `Domain: Editor`
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2974#issuecomment-3999163817) **andrewbranch** said "I think this is “working as intended” because the other packages aren’t listed as dependencies. Does it work as you expect if you add them to pkg1's package.json "dependencies"?"
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2974#issuecomment-3999487766) **psznm** tried the suggested changes, added the dependency and moved imports, observed the package import suggestion appear but the subpath import suggestion remain missing
 * **RyanCavanaugh** assigned to **andrewbranch**

### [Issue microsoft/TypeScript-go#3098](https://github.com/microsoft/TypeScript-go/issues/3098) (Closed, `Domain: Editor`)

**"Peek References" does not show matches in other files**

*Enabling typescript.experimental.useTsgo in Cursor prevents Peek References from showing cross-file TypeScript references.*

 * **timephy** added label `Domain: Editor`
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/3098#issuecomment-4087984253) **DanielRosenwasser** said "Those references are in Svelte files. There is currently no stable API that can be used to reimplement support for Svelte, Vue, Astro, etc., and we won't have one until at least TypeScript 7.1."
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/3098#issuecomment-4088563318) **timephy** said "That's sad to hear! I was really enjoying the speed tsgo gives me... Looking forward to when existing integrations will work again 🙌🏽"
 * [today](https://github.com/microsoft/TypeScript-go/issues/3098#issuecomment-4172519656) **RyanCavanaugh** said "Closing since this is firmly in the "need an API" work item"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#3121](https://github.com/microsoft/TypeScript-go/issues/3121) (Closed, `Needs More Info`)

**extension gets uninstalled after around an hour on vscodium**

*The TypeScript Native Preview extension installed in VSCodium on Linux is uninstalled after about an hour for being flagged problematic.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/3121#issuecomment-4077173146) **huseeiin** recommended downloading the VSIX via VS Code’s extensions tab instead of VSCodium and provided a screenshot
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/3121#issuecomment-4087140542) **mjbvz** asked how they set up the marketplace in vscodium and whether they connected to the official marketplace or a different one
 * **RyanCavanaugh** added label `Needs More Info`
 * (today) **RyanCavanaugh** closed the issue
 * [later](https://github.com/microsoft/TypeScript-go/issues/3121#issuecomment-4175811753) **huseeiin** explained that they downloaded the VSIX from VSCode and installed it in VSCodium via the codium --install-extension command

### [Issue microsoft/TypeScript-go#3173](https://github.com/microsoft/TypeScript-go/issues/3173) (Closed, `Domain: Editor`, **andrewbranch**, **Copilot**)

**When two imports have the same url, updates always apply to the first one\.**

*Auto-import merges additions into the first identical-module import statement instead of updating the appropriate type or value import.*

 * created by **xyhxx**
 * **xyhxx** added label `Domain: Editor`
 * **RyanCavanaugh** assigned to **andrewbranch**

### [Issue microsoft/TypeScript-go#3250](https://github.com/microsoft/TypeScript-go/issues/3250) (Open, `feature parity`)

**Reimplement "find file references"**

*Reimplement find file references for JS/TS files by extending multi-project search beyond document positions.*

 * created by **DanielRosenwasser**
 * **RyanCavanaugh** added label `feature parity`
 * **RyanCavanaugh** added to milestone `Post-7.0`

### [Issue microsoft/TypeScript-go#3310](https://github.com/microsoft/TypeScript-go/issues/3310) (Closed, `Domain: Declaration Emit`, **weswigham**)

**Non\-exported interfaces triggers a "cannot be named" error**

*Exported variable using a type alias based on a non-exported interface triggers a "cannot be named" error in TypeScript 7.*

 * created by **DanielRosenwasser**
 * (today) **RyanCavanaugh** added label `Domain: Declaration Emit`, and assigned to **weswigham**

### [PR microsoft/TypeScript-go#3311](https://github.com/microsoft/TypeScript-go/pull/3311) (Open)

**Add expandable hover**

*Implement an expandable hover feature in VSCode by adding a custom API over LSP and swapping hover providers.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3311#issuecomment-4173489594) **jakebailey** suggested that symbolTableToDeclarationStatements might need a rethink now that JS declaration emit has changed

### [PR microsoft/TypeScript-go#3313](https://github.com/microsoft/TypeScript-go/pull/3313) (Closed)

**Disallow explicit null for optional fields**

*Prevent explicit null assignments to optional pointer fields and add tests to cover this and previous fixes.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3314](https://github.com/microsoft/TypeScript-go/pull/3314) (Closed)

**Fix declaration emit alias reuse for inferred exports**

*Align serializeTypeName’s resolveEntityName call with upstream to preserve imported type aliases in declaration emit and update baselines accordingly.*

 * created by **thromel**

### [PR microsoft/TypeScript-go#3315](https://github.com/microsoft/TypeScript-go/pull/3315) (Open, **RyanCavanaugh**, **Copilot**)

**Improve \`@overload\` error message to include host function name**

*Include the host function name in TS7012 JSDoc @overload error messages for clarity*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**

### [PR microsoft/TypeScript-go#3316](https://github.com/microsoft/TypeScript-go/pull/3316) (Closed, **RyanCavanaugh**, **Copilot**)

**Port \`move to file\` refactoring infrastructure**

*Port TypeScript’s Move-to-File refactoring infrastructure to Go, including statement selection, usage analysis, and language server integration stubs.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#3317](https://github.com/microsoft/TypeScript-go/pull/3317) (Closed)

**Fix default cases in custom Registration UnmarshalJSONFrom**

*Add missing error handling for default cases in the custom Registration UnmarshalJSONFrom unmarshaller.*

 * created by **jakebailey**

### [Issue microsoft/TypeScript-go#3318](https://github.com/microsoft/TypeScript-go/issues/3318) (Open, **iisaduan**)

**Missing \`addMissingImports\` code action/code fix**

*VSCode’s editor.codeActionOnSave lacks implementation of TypeScript’s addMissingImports code action and code fix.*

 * created by **iisaduan**
 * **iisaduan** assigned to **iisaduan**

### [Issue microsoft/TypeScript-go#3319](https://github.com/microsoft/TypeScript-go/issues/3319) (Open, **iisaduan**)

**Missing \`fixAll\` code action/code fix**

*VSCode’s TypeScript Go extension does not support the source.fixAll.ts code action or corresponding individual codefixes for editor.codeActionOnSave.*

 * created by **iisaduan**
 * **iisaduan** assigned to **iisaduan**

### [Issue microsoft/TypeScript-go#3320](https://github.com/microsoft/TypeScript-go/issues/3320) (Open, **iisaduan**)

**Missing \`removeUnused\` code fix/code action**

*The removeUnused code action and underlying unused identifier fixes are not implemented for VSCode’s TypeScript codeActionOnSave.*

 * created by **iisaduan**
 * **iisaduan** assigned to **iisaduan**

### [Issue microsoft/TypeScript-go#3321](https://github.com/microsoft/TypeScript-go/issues/3321) (Closed, **jakebailey**, **Copilot**)

**\#\#\# Bug Report: Optional chaining \`\(A?\.B as any\)\.C\(\)\` incorrectly transpiled as \`\(A?\.B\)\.C\(\)\`**

*tsgo 7.0.0-dev erroneously transpiles `(A?.B as any).C()` as `(A?.B).C()`, causing runtime errors when A is undefined.*

 * created by **Tangxinwei**
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3321#issuecomment-4174228658) **jakebailey** disputed tsc's behavior and provided a reproducible example link

### [PR microsoft/TypeScript-go#3322](https://github.com/microsoft/TypeScript-go/pull/3322) (Closed, **jakebailey**, **Copilot**)

**Not a bug: \`\(A?\.B as any\)\.C\(\)\` emit matches tsc behavior**

*TypeScript preserves parentheses in optional chaining with type assertions to match tsc behavior and adds tests for this emit*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3323](https://github.com/microsoft/TypeScript-go/issues/3323) (Closed)

**tsgo stops reporting subsequent errors after TS2880 \(diagnostics short\-circuit vs tsc\)**

*tsgo halts error reporting after the initial TS2880 import assertion error instead of listing subsequent diagnostics.*

 * created by **bamcop**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3323#issuecomment-4174485116) **jakebailey** said "Yes, this is now a parsing error in 7.0."

### [Issue microsoft/TypeScript-go#3324](https://github.com/microsoft/TypeScript-go/issues/3324) (Closed, `bug`, **jakebailey**, **RyanCavanaugh**, **Copilot**)

**Different \`\-\-showConfig\` output**

*tsgo's --showConfig output differs from tsc by omitting file listings, using numeric enum values, and absolute paths.*

 * created by **zaverden**
 * (later) **RyanCavanaugh** assigned to **jakebailey**, **Copilot**, **RyanCavanaugh**

### [Issue microsoft/TypeScript-go#3325](https://github.com/microsoft/TypeScript-go/issues/3325) (Closed, `Domain: Editor`, **RyanCavanaugh**, **Copilot**)

**The declaration of the deconstructing parameters of a function is marked as \`var\` instead of \`parameter\`**

*The Tsgo extension’s hover tooltip incorrectly displays destructured function parameters as var instead of parameter.*

 * created by **Withered-Flower-0422**
 * **Withered-Flower-0422** added label `Domain: Editor`
 * (later) **RyanCavanaugh** assigned to **Copilot**, **RyanCavanaugh**

### [PR microsoft/TypeScript-go#3326](https://github.com/microsoft/TypeScript-go/pull/3326) (Closed, **RyanCavanaugh**, **Copilot**)

**Fix \`\-\-showConfig\` output: add implied compiler options**

*Support emitting implied compiler options in tsgo --showConfig output to align with tsc behavior*

 * created by **Copilot**
 * (later) **Copilot** assigned to **Copilot**, **RyanCavanaugh**

### [PR microsoft/TypeScript-go#3327](https://github.com/microsoft/TypeScript-go/pull/3327) (Closed, **RyanCavanaugh**, **Copilot**)

**Fix destructured binding hover displaying wrong keyword \(\`var\` instead of \`\(parameter\)\`, \`const\`, or \`let\`\)**

*Update hover implementation to ascend destructured bindings and display the correct var, let, const, or parameter prefix.*

 * created by **Copilot**
 * (later) **Copilot** assigned to **Copilot**, **RyanCavanaugh**

### [Issue microsoft/TypeScript-go#516](https://github.com/microsoft/TypeScript-go/issues/516) (Open, `Domain: API and Extensibility`)

**Transformer Plugin or Compiler API**

*Requesting TypeScript team feedback on reintroducing a transformer plugin API versus continuing with the compiler API amid JS-Go integration challenges.*

 * [41 weeks ago](https://github.com/microsoft/TypeScript-go/issues/516#issuecomment-2981249430) **jakebailey** explained that plugin-based solutions require using the TypeScript API or patching tsc, suggested import maps instead of path aliases for package.json projects, and noted the docs advise against pervasive use of path aliases
 * [41 weeks ago](https://github.com/microsoft/TypeScript-go/issues/516#issuecomment-2981283047) **lppedd** mentioned that Nx has been shifting away from path aliases but still supports them for legacy reasons, noted pending Angular support and transformer issues, and requested maintaining compatibility with the previous implementation to avoid further workspace restructuring
 * [28 weeks ago](https://github.com/microsoft/TypeScript-go/issues/516#issuecomment-3292165922) **goloveychuk** proposed providing a typescript-builder npm package that would download the Go compiler and build TypeScript and plugins with remote caching
 * **RyanCavanaugh** added to milestone `Post-7.0`

### [Issue microsoft/TypeScript-go#518](https://github.com/microsoft/TypeScript-go/issues/518) (Closed, `Domain: Module Resolution`, `node10 resolution`)

**Cannot find module '??' or its corresponding type declarations\.**

*A dependency’s package.json exports configuration omits a default types mapping, causing TypeScript to fail finding its type declarations.*

 * **jakebailey** added label `node10 resolution`
 * [16 weeks ago](https://github.com/microsoft/TypeScript-go/issues/518#issuecomment-3615107376) **damiangreen** described following the instructions from the TypeScript blog but encountered a wall of failed imports in a NextJS app and NestJS backend and shared their tsconfig.json
 * [16 weeks ago](https://github.com/microsoft/TypeScript-go/issues/518#issuecomment-3615142974) **jakebailey** said "You can see there are errors in tsconfig.json; baseUrl has been removed. See https://github.com/microsoft/TypeScript/issues/62508#issuecomment-3348649259."
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#650](https://github.com/microsoft/TypeScript-go/issues/650) (Open, `Domain: Porting Meta`, `Domain: Performance`)

**Using pointer address as node/symbol id**

*Use pointer addresses as node and symbol IDs to avoid atomic operations and reduce footprint, with larger keys and non-sequential IDs.*

 * [52 weeks ago](https://github.com/microsoft/TypeScript-go/issues/650#issuecomment-2761131412) **jakebailey** suggested doing the eager version and using safe integer IDs rather than pointer values to ensure IDs fit within JS's Number.MAX_SAFE_INTEGER
 * (43 weeks ago) **jakebailey** added labels `Domain: Porting Meta`, `Domain: Performance`
 * **RyanCavanaugh** added to milestone `Possible Improvement`

### [Issue microsoft/TypeScript-go#919](https://github.com/microsoft/TypeScript-go/issues/919) (Open, `Domain: Editor`)

**extension: command 'typescript\.goToSourceDefinition' not found**

*Using VSCode's Go to Source Definition with the tsgo extension fails with 'typescript.goToSourceDefinition' command not found error.*

 * created by **tmm1**
 * **jakebailey** added label `Domain: LSP`
 * **RyanCavanaugh** added to milestone `Post-7.0`

### [Issue microsoft/TypeScript-go#929](https://github.com/microsoft/TypeScript-go/issues/929) (Closed, `Domain: Type Checking`, `Type Ordering`)

**Errors in @types/jsdom, @sinclair/typebox**

*TypeScript Native Preview triggers TS2321 excessive stack depth errors in @sinclair/typebox definitions via @types/jsdom in jest-environment-jsdom*

 * [8 weeks ago](https://github.com/microsoft/TypeScript-go/issues/929#issuecomment-3843892128) **jakebailey** said "For typebox, my understanding is that a newer version already fixed it, but jest and others still depend on an old version. It'd probably be worth asking for a backport upstream?"
 * [8 weeks ago](https://github.com/microsoft/TypeScript-go/issues/929#issuecomment-3845678994) **sinclairzx81** published a hotfix for TS7 in TypeBox 0.27.10, provided update instructions, and asked for testing confirmation
 * [7 weeks ago](https://github.com/microsoft/TypeScript-go/issues/929#issuecomment-3850324039) **jakebailey** said "Tested it in DefinitelyTyped-tools and it does indeed work (transitive dep via jest). Thank you!"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#977](https://github.com/microsoft/TypeScript-go/issues/977) (Closed, `Domain: Type Checking`, `Type Ordering`)

**Issues with react and redux**

*Three common React Redux test cases produce inconsistent results between ts-go and tsc compilers, as demonstrated in a minimal repro.*

 * [41 weeks ago](https://github.com/microsoft/TypeScript-go/issues/977#issuecomment-2981187745) **ahejlsberg** explained issue with type ordering in the connect overload due to union type ordering differences between compilers and suggested breaking the union into separate overloads in preference order
 * **ahejlsberg** added label `Type Ordering`
 * [41 weeks ago](https://github.com/microsoft/TypeScript-go/issues/977#issuecomment-2981218020) **lukeapage** said "Thanks for the analysis! I’ve raised an issue in the react-redux github."
 * (today) **RyanCavanaugh** closed the issue

