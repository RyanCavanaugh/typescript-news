# Report for 2026-04-14 (Tuesday, April 14th, 2026)

17 different users commented on 97 different issues.

## Recommended Actions

 * Response Recommended
    * @PinkaminaDianePie reported moving back to an older TS version because tsgo wasn't working in [microsoft/TypeScript-go#2420](https://github.com/microsoft/TypeScript-go/issues/2420#issuecomment-4245969438)

## Activity Summary

### [Issue microsoft/TypeScript-go#1380](https://github.com/microsoft/TypeScript-go/issues/1380) (Closed, `Domain: Module Resolution`, `Domain: Type Checking`, **andrewbranch**)

**Broken type import from \`@sendgrid/mail\`**

*tsgo cannot resolve MailDataRequired from @sendgrid/mail and errors on Client import without esModuleInterop under modern tsconfig*

 * [26 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1380#issuecomment-3391034256) **jhorgan24** bumped the issue as the last outstanding test for tsgo and asked if sendgrid isn't exporting its types properly
 * [22 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1380#issuecomment-3504269711) **ahejlsberg** identified that @sendgrid/mail and @sendgrid/client contain both export = and regular export declarations, noting a known issue with merging exports and relating it to issue #1954
 * **ahejlsberg** assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/issues/1380#issuecomment-4246840105) **RyanCavanaugh** said "See #2781 for a longer discussion, but TL;DR we can't really support types that suppress critical "this does not work and you shouldn't do it" errors"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#1882](https://github.com/microsoft/TypeScript-go/issues/1882) (Closed, `Needs More Info`, **johnfav03**)

**Renaming/moving file breaks imports**

*Renaming a TypeScript file in tsgo leads to TS6307 errors due to missing project file listing, unlike TypeScript 5.8.*

 * [13 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1882#issuecomment-3714016968) **Netail** described that renaming a directory or file in VSCode broke alias and relative imports while dependency imports still worked
 * (1 week ago) **RyanCavanaugh** set milestone to `Post-7.0`, and assigned to **johnfav03**
 * (today) **gabritto** closed the issue

### [Issue microsoft/TypeScript-go#2086](https://github.com/microsoft/TypeScript-go/issues/2086) (Closed, `bug`, **Copilot**)

**Missing error when shadowing WeakMap/WeakSet in class private field's scope**

*tsgo fails to report reserved-name errors when shadowing WeakMap or WeakSet in class private field scopes.*

 * [21 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2086#issuecomment-3530294753) **jakebailey** said "This would be a checker bug; recordPotentialCollisionWithWeakMapSetInGeneratedCode was not ported."
 * **jakebailey** assigned to **Copilot**
 * **RyanCavanaugh** added to milestone `Post-7.0`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2087](https://github.com/microsoft/TypeScript-go/pull/2087) (Closed, **jakebailey**, **Copilot**)

**Port missing collision detection checks from checkCollisionsForDeclarationName**

*Add missing TypeScript collision detection checks for WeakMap, WeakSet, Promise, Reflect, and Object class names to Go’s checker.*

 * [21 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2087#issuecomment-3530470992) **Copilot** fixed crash by adding nil check for node.Name(), ran tests, and accepted baselines
 * [21 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2087#issuecomment-3530483653) **jakebailey** said "@copilot there are more checks than just recordPotentialCollisionWithWeakMapSetInGeneratedCode in checkCollisionsForDeclarationName in the old checker. Please port the rest."
 * [21 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2087#issuecomment-3530516698) **Copilot** ported all remaining collision checks including Promise, Reflect, and class name collision detection, confirmed tests passed, and reported firewall blocked connections with instructions for allowlisting
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2133](https://github.com/microsoft/TypeScript-go/issues/2133) (Closed, `Domain: Editor`, **gabritto**)

**Renaming a file results in mis\-identifying the right sconfig file**

*Renaming a .spec.ts file in VSCode makes editor apply the base tsconfig instead of the local one, causing persistent errors.*

 * [17 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2133#issuecomment-3656242346) **PaulRBerg** reported that the issue persisted in the latest version and forced frequent language server restarts
 * (1 week ago) **RyanCavanaugh** set milestone to `TypeScript 7.0 RC`, and assigned to **gabritto**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2133#issuecomment-4246698262) **gabritto** asked if the users still encountered the issue and requested a full reproduction including tsconfig.json, code, and both sets of logs
 * [today](https://github.com/microsoft/TypeScript-go/issues/2133#issuecomment-4247071161) **gabritto** said "Possibly fixed by #2456."
 * [later](https://github.com/microsoft/TypeScript-go/issues/2133#issuecomment-4250103800) **PaulRBerg** said "yeah it appears to be fixed now"
 * [later](https://github.com/microsoft/TypeScript-go/issues/2133#issuecomment-4251116677) **lukpsaxo** said "I haven't seen it in a while, happy to close. Thanks @gabritto "
 * (later) **lukpsaxo** closed the issue

### [Issue microsoft/TypeScript-go#2186](https://github.com/microsoft/TypeScript-go/issues/2186) (Open, `bug`, **gabritto**)

**Broken assignability and quick info due to erroneously deferring keyof T since \#51621**

*Erroneously deferring keyof T since PR 51621 causes unsimplified quick info and invalid type assignments.*

 * created by **LukeAbby**
 * (2 weeks ago) **RyanCavanaugh** added label `bug`, and assigned to **gabritto**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [Issue microsoft/TypeScript-go#2193](https://github.com/microsoft/TypeScript-go/issues/2193) (Open, `Crash`, **jakebailey**)

**"Token cache mismatch: parent" in inlay hints**

*Inlay hints processing panics due to a token cache mismatch for function expression nodes.*

 * **jakebailey** added label `Crash`
 * [18 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2193#issuecomment-3612082813) **IllusionMH** reported concurrent errors for textDocument/inlayHint and textDocument/foldingRange including panic trace for token cache mismatch
 * **RyanCavanaugh** assigned to **jakebailey**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [Issue microsoft/TypeScript-go#2209](https://github.com/microsoft/TypeScript-go/issues/2209) (Open, `Domain: Editor`, **Copilot**)

**\[lsp\] Go to Definition missing getter when property returns callable interface**

*Go to Definition in TypeScript Go Native only returns the callable interface signature, omitting the getter definition.*

 * created by **imbant**
 * (18 weeks ago) **jakebailey** added label `Domain: Editor`, and assigned to **Copilot**
 * **RyanCavanaugh** added to milestone `Post-7.0`

### [Issue microsoft/TypeScript-go#2213](https://github.com/microsoft/TypeScript-go/issues/2213) (Closed, `Domain: Editor`, `Needs More Info`)

**unable to restart the tsgo language server, getting timeout**

*Restarting the tsgo language server via VS Code times out and breaks TypeScript features until the extension is disabled.*

 * **shmdhussain** added label `Domain: Editor`
 * **RyanCavanaugh** added label `Needs More Info`
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/2213#issuecomment-4171911287) **RyanCavanaugh** said "There's not much to go on here and we haven't seen other reports of this. Anything unusual about your setup? Any other clues? Without a concrete repro I don't think we have much chance of fixing it"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#2220](https://github.com/microsoft/TypeScript-go/issues/2220) (Closed, `bug`, **weswigham**)

**\[pnpm\] The inferred type of 'xxx' cannot be named without a reference to '\.pnpm/xxx'**

*tsgo 7.0.0-dev errors on inferring return types from PNPM-installed packages, requiring explicit annotations due to unnameable ".pnpm" path references.*

 * [18 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2220#issuecomment-3629578583) **rubnogueira** said "#1034 solved some of my issues, but like the main post, I still have one specific dependency that has the same error."
 * (2 weeks ago) **RyanCavanaugh** added label `bug`, and assigned to **weswigham**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2220#issuecomment-4247243155) **RyanCavanaugh** reported that the emit no longer errors and provided the emitted TypeScript code
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#2227](https://github.com/microsoft/TypeScript-go/issues/2227) (Open, `Domain: Editor`, **Copilot**)

**Port \`move to file\` refactoring**

*Reintroduce the Move to file refactoring from TypeScript 6 into the language server to restore essential automated code relocation functionality.*

 * **jakebailey** added label `Domain: Editor`
 * (1 week ago) **RyanCavanaugh** assigned to **Copilot**, **RyanCavanaugh**
 * (today) **RyanCavanaugh** set milestone to `TypeScript 7.0 RC`, and unassigned **RyanCavanaugh**

### [Issue microsoft/TypeScript-go#2228](https://github.com/microsoft/TypeScript-go/issues/2228) (Open, `Domain: Editor`, **gabritto**)

**No JS Doc template completions**

*The ts-go extension lacks support for the JSDoc template completion feature introduced in TypeScript 6.0 for VSCode.*

 * created by **mjbvz**
 * **gabritto** assigned to **gabritto**
 * **jakebailey** added label `Domain: Editor`
 * **RyanCavanaugh** added to milestone `Post-7.0`

### [Issue microsoft/TypeScript-go#2238](https://github.com/microsoft/TypeScript-go/issues/2238) (Closed, `Crash`, **ahejlsberg**)

**fatal error: concurrent map read and map write**

*A fatal concurrent map read/write panic occurs in the Typescript-Go link store while resolving import aliases.*

 * [18 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2238#issuecomment-3617676644) **jakebailey** said "It seems like we are still somehow concurrency unsafe through HandleNoEmitOnError. Incremental is still not doing the expected locking."
 * **RyanCavanaugh** assigned to **ahejlsberg**
 * [11 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2238#issuecomment-3787068104) **ahejlsberg** said "@charlag No longer seems to reproduce, issue was likely fixed. Can you confirm that this is no longer an issue?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2238#issuecomment-4247227304) **RyanCavanaugh** said "Closing due to inactivity. Please open a new issue if you're seeing this again. Thanks!"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#2244](https://github.com/microsoft/TypeScript-go/issues/2244) (Closed, `Domain: Editor`, **gabritto**)

**Port \`update imports on file rename/move\` support**

*Request to port support for automatically updating imports when files are renamed or relocated*

 * [17 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2244#issuecomment-3633225247) **jakebailey** said "I assume we'd do it the same way as VS Code, just over LSP (which LSP is mostly a thin wrapper over)."
 * **RyanCavanaugh** assigned to **gabritto**
 * **DanielRosenwasser** added to milestone `TypeScript 7.0 RC`
 * (today) **gabritto** closed the issue

### [Issue microsoft/TypeScript-go#2247](https://github.com/microsoft/TypeScript-go/issues/2247) (Open, `Domain: Editor`, **andrewbranch**, **Copilot**)

**Auto\-imports insert \`import\` statement into CJS files**

*TypeScript auto-imports ES module syntax into CommonJS .js files with nodeXX module settings instead of require() despite type commonjs.*

 * **gebsh** added label `Domain: Editor`
 * **RyanCavanaugh** assigned to **andrewbranch**
 * **andrewbranch** assigned to **Copilot**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [Issue microsoft/TypeScript-go#2276](https://github.com/microsoft/TypeScript-go/issues/2276) (Closed, `bug`, **weswigham**)

**TS2742: The inferred type of 'default' cannot be named**

*Using tsgo to export stylex through a mapped type produces TS2742 errors requiring a default export type annotation.*

 * created by **jfirebaugh**
 * (2 weeks ago) **RyanCavanaugh** added label `bug`, and assigned to **weswigham**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2276#issuecomment-4247223900) **RyanCavanaugh** showed the fixed .d.ts output
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#2277](https://github.com/microsoft/TypeScript-go/issues/2277) (Closed, `bug`, **weswigham**)

**TS2742: The inferred type of \.\.\. cannot be named\.\.\.**

*pnpm's nested node_modules structure triggers TS2742 inferred type naming errors for Express handler exports under TSGo*

 * created by **jfirebaugh**
 * (2 weeks ago) **RyanCavanaugh** added label `bug`, and assigned to **weswigham**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2277#issuecomment-4246992592) **RyanCavanaugh** stated that the issue no longer reproduced and showed the emitted code
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#2279](https://github.com/microsoft/TypeScript-go/issues/2279) (Open, `Domain: Editor`, **gabritto**)

**Add snippet completions for methods**

*Implement snippet completions in ts-go so selecting a base class method suggestion inserts its full signature and stub.*

 * created by **mjbvz**
 * **gabritto** assigned to **gabritto**
 * **jakebailey** added label `Domain: Editor`
 * **RyanCavanaugh** added to milestone `Post-7.0`

### [Issue microsoft/TypeScript-go#2280](https://github.com/microsoft/TypeScript-go/issues/2280) (Open, `Domain: Editor`, **gabritto**)

**Port \`implement interface\` quick fix**

*Port the implement interface quick fix from TypeScript to TS-Go to provide automated interface implementation support.*

 * **gabritto** assigned to **gabritto**
 * [17 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2280#issuecomment-3644087661) **a-tarasyuk** said "@Tyriar, I'm curious, what are some other quick fixes that are among the top five most commonly used? :slightly_smiling_face:"
 * [17 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2280#issuecomment-3644200857) **Tyriar** said "I'm not sure I have 5 commonly used ones actually. It's hard to remember them off the top of my head, I use the promise  await conversion one occasionally is one that comes to mind."
 * **RyanCavanaugh** added to milestone `Post-7.0`

### [Issue microsoft/TypeScript-go#2282](https://github.com/microsoft/TypeScript-go/issues/2282) (Open, `possible improvement`, **joj**)

**Request for official prebuilt Windows binaries \(tsgo\.exe\) published via GitHub Releases, without requiring npm\.**

*Officially distribute Windows tsgo.exe binaries via GitHub Releases to enable TypeScript use without npm.*

 * [17 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2282#issuecomment-3638425819) **PaulHuizer** praised tsgo.exe as a NuGet package without npm/node dependencies
 * (2 weeks ago) **RyanCavanaugh** added label `possible improvement`, and assigned to **joj**
 * **RyanCavanaugh** added to milestone `Possible Improvement`

### [Issue microsoft/TypeScript-go#2310](https://github.com/microsoft/TypeScript-go/issues/2310) (Open, `possible improvement`, **joj**)

**TypeScript for \.Net Projects**

*Custom MSBuild targets file and instructions to compile TypeScript 7 in .NET projects with tsgo until official support arrives.*

 * created by **joj**
 * (2 weeks ago) **RyanCavanaugh** added label `possible improvement`, and assigned to **joj**
 * **RyanCavanaugh** added to milestone `Possible Improvement`

### [Issue microsoft/TypeScript-go#2328](https://github.com/microsoft/TypeScript-go/issues/2328) (Open, `bug`, **weswigham**, **Copilot**)

**Declaration emit with \`\-\-noResolve\` differs from tsc**

*tsgo incorrectly emits ‘any’ for default exports under --noResolve whereas tsc preserves the original types.*

 * [16 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2328#issuecomment-3667553972) **jakebailey** said "Do all of your examples involve as?"
 * [16 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2328#issuecomment-3667562761) **jfirebaugh** said "So far, yeah, that seems to be the trigger."
 * **jakebailey** assigned to **Copilot**
 * (today) **RyanCavanaugh** added label `bug`, set milestone to `TypeScript 7.0 RC`, and assigned to **weswigham**

### [Issue microsoft/TypeScript-go#2334](https://github.com/microsoft/TypeScript-go/issues/2334) (Open, **DanielRosenwasser**)

**Questionable code lenses for object type members on a single line**

*Suppress code lenses on object type members defined inline when their parent and siblings share the same line.*

 * created by **DanielRosenwasser**
 * **RyanCavanaugh** assigned to **DanielRosenwasser**
 * **RyanCavanaugh** added to milestone `Post-7.0`

### [Issue microsoft/TypeScript-go#2367](https://github.com/microsoft/TypeScript-go/issues/2367) (Open, `Domain: Editor`, **Copilot**)

**References code lens does not include imports as references**

*The references code lens fails to count imports as references, showing zero references despite TypeScript 6.0 support.*

 * created by **mjbvz**
 * **jakebailey** assigned to **Copilot**
 * (today) **RyanCavanaugh** added label `Domain: Editor`, and set milestone to `Post-7.0`

### [Issue microsoft/TypeScript-go#2382](https://github.com/microsoft/TypeScript-go/issues/2382) (Open, `Domain: Editor`, **jakebailey**, **Copilot**)

**\[bug\] JS/TS Format Selection can delete comments**

*Formatting a selected portion of a JavaScript or TypeScript block comment unexpectedly removes the comment.*

 * **RedCMD** added label `Domain: Editor`
 * (3 weeks ago) **jakebailey** assigned to **Copilot**, **jakebailey**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [Issue microsoft/TypeScript-go#2386](https://github.com/microsoft/TypeScript-go/issues/2386) (Open, `Domain: Editor`, **gabritto**)

**TS2307 Delete a folder of \`\.ts\` files does not trigger \`ts\(2307\)\` error hint**

*VSCode does not display a ts(2307) missing module error when a referenced folder of .ts files is deleted*

 * created by **ColaFanta**
 * **ColaFanta** added label `Domain: Editor`
 * **RyanCavanaugh** assigned to **gabritto**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [Issue microsoft/TypeScript-go#2387](https://github.com/microsoft/TypeScript-go/issues/2387) (Open, `bug`, **iisaduan**)

**Diagnostics don't refresh after file rename**

*After renaming a file, TypeScript diagnostics sometimes fail to update until the server is reloaded.*

 * [15 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2387#issuecomment-3695197345) **renatoaraujoc** said "Happening here too, I thought this was an IntelliJ bug using ts-go."
 * (2 weeks ago) **RyanCavanaugh** added label `bug`, and assigned to **iisaduan**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [Issue microsoft/TypeScript-go#2420](https://github.com/microsoft/TypeScript-go/issues/2420) (Closed, `Crash`, **iisaduan**)

**vscode extension crashes on start**

*The TypeScript native-preview VSCode extension fails to initialize due to write EPIPE errors and an unterminated quoted string syntax error.*

 * [16 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2420#issuecomment-3685539027) **PinkaminaDianePie** said "@Bashamega i don't even see such a version here https://marketplace.visualstudio.com/items?itemName=TypeScriptTeam.native-preview&ssr=false#version-history"
 * [16 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2420#issuecomment-3685558502) **Bashamega** said "I am using cursor that uses vsx"
 * **RyanCavanaugh** assigned to **iisaduan**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2420#issuecomment-4245953525) **iisaduan** asked whether the issue still reproduced and requested additional information
 * [today](https://github.com/microsoft/TypeScript-go/issues/2420#issuecomment-4245969438) **PinkaminaDianePie** said "No idea. I moved back to the older TS version cause tsgo wasn't working."
 * (today) **PinkaminaDianePie** closed the issue

### [PR microsoft/TypeScript-go#2432](https://github.com/microsoft/TypeScript-go/pull/2432) (Closed)

**Include import specifiers as references in code lens**

*Import specifiers are now properly counted and deduplicated as code lens references, aligning behavior with TypeScript 6.0.*

 * created by **darwin808**
 * [15 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2432#issuecomment-3698447259) **darwin808** agreed with microsoft-github-policy-service
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#2437](https://github.com/microsoft/TypeScript-go/issues/2437) (Open, `Domain: Editor`, **sandersn**)

**TSGo prioritizes \`tsconfig\.json\` over \`jsconfig\.json\` in the same directory, even for file types the former excludes**

*When both config files reside in the same directory, TSGo always prioritizes tsconfig.json over jsconfig.json, disabling JavaScript type checking.*

 * created by **Bertie690**
 * **Bertie690** added label `Domain: Editor`
 * **RyanCavanaugh** assigned to **sandersn**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [Issue microsoft/TypeScript-go#2443](https://github.com/microsoft/TypeScript-go/issues/2443) (Open, `documentation`, **RyanCavanaugh**)

**\[Doc\]: paths map value points to removed baseUrl value**

*Inline documentation incorrectly references the removed baseUrl option for computing paths map values.*

 * [13 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2443#issuecomment-3720182702) **jakebailey** mentioned the source of the tooltips in schemastore and suggested updating them with neutral language
 * (2 weeks ago) **RyanCavanaugh** added label `documentation`, and assigned to **RyanCavanaugh**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [Issue microsoft/TypeScript-go#2501](https://github.com/microsoft/TypeScript-go/issues/2501) (Closed, `Crash`, **iisaduan**)

**textDocument/completion: runtime error: slice bounds out of range \[:2615\] with length 2590**

*The TypeScript-Go language server panics with a slice bounds out of range error during textDocument/completion requests.*

 * [10 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2501#issuecomment-3829141424) **frodi-karlsson** suggested adding bounds checking to LineAndCharacterToPosition to prevent panics when positions exceed text length
 * [10 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2501#issuecomment-3829229887) **jakebailey** expressed concern that having them elsewhere could introduce mismatches and break things, and that this shouldn't be inevitable
 * **RyanCavanaugh** assigned to **iisaduan**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2501#issuecomment-4247475572) **RyanCavanaugh** said "We've merged a few fixes here that should address this. If you see it come up again, please open a new issue with repro and we'll try to investigate further."
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#2504](https://github.com/microsoft/TypeScript-go/issues/2504) (Closed, `bug`, **weswigham**)

**TS4023 "cannot be named" \- tsgo not allowing references to unexported types**

*TypeScript-Go misreports TS4023 for exported wrappers that infer unexported types via Parameters<typeof> from another module.*

 * created by **johnpyp**
 * (2 weeks ago) **RyanCavanaugh** added label `bug`, and assigned to **weswigham**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2504#issuecomment-4247479332) **RyanCavanaugh** said "Emits without error now"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#2505](https://github.com/microsoft/TypeScript-go/issues/2505) (Closed, `bug`, **weswigham**)

**Circular type exported from namespace cannot be named**

*ts-go fails to generate declarations for a function using a circular namespace type alias, emitting an unnameable external type error.*

 * created by **Retsam**
 * (2 weeks ago) **RyanCavanaugh** added label `bug`, and assigned to **weswigham**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2505#issuecomment-4247510710) **RyanCavanaugh** indicated that the issue was fixed and the code now emits without error
 * (today) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/issues/2505#issuecomment-4248004290) **Retsam** said "Thanks, verified the fix in my app, too!"

### [Issue microsoft/TypeScript-go#2522](https://github.com/microsoft/TypeScript-go/issues/2522) (Open, `Domain: Declaration Emit`, `Crash`, **weswigham**)

**Reexporting @types/micromatch@4\.0\.10 from a \.cjs file crashes**

*Re-exporting @types/micromatch@4.0.10 from a .cjs file crashes the TypeScript declaration transformer with a ‘Diagnostic emitted without context’ panic.*

 * [8 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2522#issuecomment-3884449949) **Knagis** reported that it still crashed with version 7.0.0-dev.20260211.1 and provided a panic stack trace
 * (1 week ago) **jakebailey** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2522#issuecomment-4247522078) **RyanCavanaugh** reported that the crash was resolved but a TS4032 error appeared involving a private module
 * (today) **RyanCavanaugh** set milestone to `TypeScript 7.0 RC`, and unassigned **jakebailey**, **Copilot**

### [Issue microsoft/TypeScript-go#2533](https://github.com/microsoft/TypeScript-go/issues/2533) (Open, `bug`, `Domain: Declaration Emit`, **weswigham**)

**Multiple differences in declaration emit for CommonJS exports**

*TypeScript’s declaration emitter for CommonJS exports uses typeof module.exports, emits duplicate var declarations, and emits var instead of const.*

 * (12 weeks ago) **ahejlsberg** added labels `bug`, `Domain: Declaration Emit`, and assigned to **weswigham**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2533#issuecomment-4247535574) **RyanCavanaugh** said "Confirmed all three still exist in nightly"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2533#issuecomment-4247896788) **ahejlsberg** noted support for multiple assignments to module.exports and exports.XXX and recommended emitting only the first occurrence to prevent duplicate declarations
 * [today](https://github.com/microsoft/TypeScript-go/issues/2533#issuecomment-4247979575) **ahejlsberg** described other JS declaration emit issues, noting missing x and y properties in class C and duplicate namespace declarations for obj and f

### [Issue microsoft/TypeScript-go#2555](https://github.com/microsoft/TypeScript-go/issues/2555) (Open, `Domain: Editor`, **andrewbranch**)

**Installing Native Preview broke TS Imports**

*Installing VS Code’s Native Preview TypeScript extension on macOS breaks TypeScript auto-import suggestions despite reverting settings and reinstalling the editor.*

 * [11 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2555#issuecomment-3800314263) **ericnorris** stated that their issue was about the types field in package.json, not compilerOptions in tsconfig.json
 * [10 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2555#issuecomment-3809296472) **DanielRosenwasser** informed that a PR addressing the autocomplete issue had been submitted
 * **RyanCavanaugh** assigned to **andrewbranch**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [Issue microsoft/TypeScript-go#2561](https://github.com/microsoft/TypeScript-go/issues/2561) (Closed, `Crash`, **iisaduan**)

**v0\.20260119\.1 crashes ts server for large project, v0\.20260116\.1 works**

*TypeScript Native Preview v0.20260119.1 crashes the TS server on large, high-memory projects, whereas v0.20260116.1 works.*

 * [11 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2561#issuecomment-3791740211) **austinfennacy** described memory usage issues across versions, noted a crash on version 0.20260119, observed fluctuating memory on 0.20260122.4, and indicated intent to keep auto-update enabled while leaving the issue open
 * [11 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2561#issuecomment-3791903072) **DanielRosenwasser** announced that the issue was solved by PR #2553, noted version 0.20260122.4 as a last-known-good release, and recommended against pinning to a specific extension version
 * **RyanCavanaugh** assigned to **iisaduan**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2561#issuecomment-4247538859) **RyanCavanaugh** said "Closing since we haven't seen any additional reports. Please log a new issue if you run into anything. Thanks!"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#2582](https://github.com/microsoft/TypeScript-go/issues/2582) (Open, `Domain: Editor`, **andrewbranch**)

**Auto\-import does not suggest updates from symlinked monorepo package sources**

*VS Code’s auto-import feature does not suggest updated symbols from symlinked packages in a monorepo workspace*

 * created by **ericnorris**
 * **ericnorris** added label `Domain: Editor`
 * **andrewbranch** assigned to **andrewbranch**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [Issue microsoft/TypeScript-go#2609](https://github.com/microsoft/TypeScript-go/issues/2609) (Closed, `Domain: Type Checking`, `Type Ordering`, **ahejlsberg**)

**Type instantiation is excessively deep and possibly infinite\.**

*tsgo throws a deep, possibly infinite type instantiation error for TanStack Form with zod that TypeScript 5.9 compiles without issue.*

 * **ahejlsberg** added label `Domain: Type Checking`
 * [9 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2609#issuecomment-3855592321) **TkDodo** inquired if anything could be improved in the TanStack form typings
 * [9 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2609#issuecomment-3874708331) **jakebailey** suggested testing the TS 6.0 nightly with --stableTypeOrdering to try out the new algorithm
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#2621](https://github.com/microsoft/TypeScript-go/issues/2621) (Open, `bug`, **iisaduan**, **Copilot**)

**Fourslash is broken when making requests in unconfigured \.js files**

*Fourslash requests in unconfigured .js files fail with “no project found” errors, breaking tests such as auto-import completion.*

 * **iisaduan** assigned to **iisaduan**
 * [10 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2621#issuecomment-3825894034) **DanielRosenwasser** reported that restarting the extension while a .js file was open produced a 'no project found for URI' diagnostic error
 * **RyanCavanaugh** added label `bug`
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [Issue microsoft/TypeScript-go#2666](https://github.com/microsoft/TypeScript-go/issues/2666) (Open, `Needs Investigation`, **johnfav03**)

**\`tsgo \-\-build\` fails to invalidate incremental cache after dependency update**

*tsgo's --build incremental cache does not detect updated dependency types and ignores resulting type errors.*

 * (2 weeks ago) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **johnfav03**
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2666#issuecomment-4161580561) **rubenferreira97** provided a minimal reproduction repository for the build bug using local dependencies
 * [today](https://github.com/microsoft/TypeScript-go/issues/2666#issuecomment-4247911575) **RyanCavanaugh** said "Confirmed repro, thanks @rubenferreira97 "
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [Issue microsoft/TypeScript-go#2683](https://github.com/microsoft/TypeScript-go/issues/2683) (Open, `bug`, **gabritto**)

**TS2590: "Expression produces a union type that is too complex to represent" on generics types**

*A generic type union in the @regle monorepo triggers TS2590 errors due to overly complex inferred types in newer TypeScript versions*

 * [8 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2683#issuecomment-3908046091) **victorgarciaesgi** found that the type helper crashed when augmenting a tuple with an optional first parameter and provided working and crashing examples
 * (2 weeks ago) **RyanCavanaugh** added label `bug`, and assigned to **gabritto**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [Issue microsoft/TypeScript-go#2686](https://github.com/microsoft/TypeScript-go/issues/2686) (Closed, `Domain: Editor`, **andrewbranch**)

**Packages \`pnpm link\`ed from outside the workspace trigger no watch events when changed**

*Linked external packages don’t trigger watch events on changes, preventing diagnostic updates until the server restarts.*

 * [9 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2686#issuecomment-3850202915) **sheetalkamat** described how Strada watched `node_modules/package` for links and otherwise `node_modules` for failed lookups and linked the relevant pull request
 * **andrewbranch** assigned to **andrewbranch**
 * [1 month ago](https://github.com/microsoft/TypeScript-go/issues/2686#issuecomment-4069900531) **andrewbranch** said "Related: https://github.com/microsoft/vscode/issues/3025"
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#2762](https://github.com/microsoft/TypeScript-go/issues/2762) (Open, `documentation`, **DanielRosenwasser**)

**Reconsider tsconfig membership lookups for \`\.d\.ts\` files in \`composite\`**

*TypeScript 6.0 and 7.0 unexpectedly exclude .d.ts files listed in tsconfig due to composite and rootDir changes*

 * **RyanCavanaugh** assigned to **DanielRosenwasser**
 * (2 weeks ago) **DanielRosenwasser** closed the issue
 * (2 weeks ago) **DanielRosenwasser** reopened the issue
 * **RyanCavanaugh** added to milestone `Possible Improvement`

### [Issue microsoft/TypeScript-go#2780](https://github.com/microsoft/TypeScript-go/issues/2780) (Open, `Domain: Editor`, `Needs More Info`, **andrewbranch**)

**High memory consumption in a large pnpm monorepo**

*PR #2502 causes minor edits in a large pnpm monorepo to spike the TypeScript extension memory from ~700MB to ~35GB.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-4238016842) **andrewbranch** explained the registry was working as intended with hard-coded options and could not depend on project compiler options since its contents are shared across projects, noted that building registry contents per node_modules directory with the first project’s options would be incomplete for other projects, and mentioned that `--moduleResolution node` is deprecated in 6.0 and unsupported in 7.0
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-4241230123) **shinichy** said "Hmm, does that mean there's no way to limit the entry point search scope to just the main entry point in tsgo?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-4244950544) **andrewbranch** stated that the issue was likely caused by a fixable logic bug in a code path only exercised by an entrypoint included via "exports", rather than by scanning too many legitimate entrypoints
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-4249139388) **shinichy** said "Ok. What would the fix look like? Do you still need access to the repo that reproduces the issue?"
 * [later](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-4253201729) **andrewbranch** said "Yes, that's the only way I can make progress, unless I just happen to stumble upon the same root cause as your repro as I'm investigating other performance issues."

### [Issue microsoft/TypeScript-go#2781](https://github.com/microsoft/TypeScript-go/issues/2781) (Closed, `possible improvement`, **andrewbranch**)

**resolving library types with import assignment \`import = require\(\)\` fails**

*Named and default type exports from @sendgrid/mail included via import assignment work in TypeScript 6.0 but tsgo reports missing members and default-only import errors.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2781#issuecomment-4145838987) **andrewbranch** explained sendgrid's declaration intent and provided corrected TypeScript export patterns
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/2781#issuecomment-4225015501) **andrewbranch** verified that mixing named exports and export = has intended limitations and concluded there was nothing more to do on the TS side
 * (4 days ago) **andrewbranch** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/issues/2781#issuecomment-4247535535) **controversial** said "Thanks for the thorough investigation!"

### [Issue microsoft/TypeScript-go#2792](https://github.com/microsoft/TypeScript-go/issues/2792) (Open, `Domain: API and Extensibility`, **andrewbranch**)

**\[Feature request\] Provide "Relater" typechecker api**

*Expose the internal Relater type-checker's isTypeAssignableTo method in the public TypeScript API*

 * **DanielRosenwasser** added label `Domain: API and Extensibility`
 * [7 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2792#issuecomment-3929476730) **DanielRosenwasser** said "We're investigating stuff around this. #2831 adds more of the foundation of type-space APIs. I anticipate we'll have relater APIs as well."
 * **DanielRosenwasser** assigned to **andrewbranch**
 * **RyanCavanaugh** added to milestone `Post-7.0`

### [Issue microsoft/TypeScript-go#2850](https://github.com/microsoft/TypeScript-go/issues/2850) (Open, **andrewbranch**)

**Add \`\.getNonPrimitiveType\(\)\` getter**

*The API is missing the recently introduced .getNonPrimitiveType() getter that exists in Strada.*

 * created by **mrazauskas**
 * **jakebailey** assigned to **andrewbranch**
 * **RyanCavanaugh** added to milestone `Post-7.0`

### [Issue microsoft/TypeScript-go#2851](https://github.com/microsoft/TypeScript-go/issues/2851) (Open, **andrewbranch**)

**Add \`\.getTrueType\(\)\` and \`\.getFalseType\(\)\` to \`ConditionalType\`**

*Add getTrueType() and getFalseType() methods to ConditionalType so it returns instantiated true and false branch types.*

 * created by **mrazauskas**
 * **jakebailey** assigned to **andrewbranch**
 * **RyanCavanaugh** added to milestone `Post-7.0`

### [Issue microsoft/TypeScript-go#2875](https://github.com/microsoft/TypeScript-go/issues/2875) (Open, `Crash`, **iisaduan**)

**Occasional error invalid memory address/nil pointer dereference \- codeAction failed**

*TypeScript-Go LSP server intermittently panics with a nil pointer dereference when handling textDocument/codeAction requests.*

 * created by **lukpsaxo**
 * **lukpsaxo** added label `Crash`
 * **RyanCavanaugh** assigned to **iisaduan**
 * **RyanCavanaugh** added to milestone `Post-7.0`

### [Issue microsoft/TypeScript-go#2880](https://github.com/microsoft/TypeScript-go/issues/2880) (Closed, `bug`, **weswigham**)

**TS4094 for exported class expressions with ES private fields \(tsc handles via name mangling\)**

*tsgo incorrectly errors on exported class expressions using ES private fields, unlike tsc which name-mangles them.*

 * **RyanCavanaugh** assigned to **weswigham**
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/2880#issuecomment-4187210683) **jan-wilhelm** said "This seems to not be tsgo specific. I'm seeing the same error message on tsc 6.0.2, whereas 5.9.3 was not showing it."
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/2880#issuecomment-4187269594) **jakebailey** provided links to two TypeScript PRs
 * [today](https://github.com/microsoft/TypeScript-go/issues/2880#issuecomment-4248073142) **RyanCavanaugh** said "Matching 6.0 is expected behavior"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#2953](https://github.com/microsoft/TypeScript-go/issues/2953) (Open, `Crash`, **DanielRosenwasser**, **Copilot**)

**Inlay hints triggers crash during checker initialization**

*Inlay hints cause the TypeScript checker to crash during initialization in the editor.*

 * **DanielRosenwasser** assigned to **DanielRosenwasser**
 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2953#issuecomment-3992836790) **Andarist** shared a contrived Go fourslash test that reproduced an earlier crash and noted it also crashed in Strada requiring esModuleInterop
 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2953#issuecomment-3993412640) **Andarist** provided a TypeScript code snippet illustrating correct augmentation resolution
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [Issue microsoft/TypeScript-go#2974](https://github.com/microsoft/TypeScript-go/issues/2974) (Open, `Domain: Editor`, **andrewbranch**)

**Missing auto\-import for subpath imports of other local packages**

*VS Code TypeScript auto-imports fail to recognize subpath imports from sibling local workspace packages.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/2974#issuecomment-4179268991) **psznm** described that import suggestions did not work for relative paths outside the tsconfig directory and provided examples and a workaround
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/2974#issuecomment-4179560164) **andrewbranch** explained that files from another package are resolved via node_modules specifiers without computing another name and noted uncertainty about using imports with relative paths to other packages
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/2974#issuecomment-4179659897) **psznm** described that deleting node_modules/pkg2 enabled auto imports for "#pkg4/*" but that the workaround failed without including ../pkg2 in tsconfig.json
 * **RyanCavanaugh** added to milestone `Post-7.0`

### [Issue microsoft/TypeScript-go#3054](https://github.com/microsoft/TypeScript-go/issues/3054) (Open, `feature parity`, **jakebailey**)

**\`tsgo \-\-generateTrace\` appears unimplemented**

*The tsgo CLI’s documented --generateTrace flag requires an argument but does nothing and fails to produce trace output like tsc.*

 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/issues/3054#issuecomment-4035059255) **jakebailey** referred to issue #2914 and suggested trying --pprofDir . while noting it might not be specific enough
 * (2 weeks ago) **RyanCavanaugh** added label `feature parity`, and assigned to **jakebailey**
 * **RyanCavanaugh** added to milestone `Post-7.0`

### [Issue microsoft/TypeScript-go#3094](https://github.com/microsoft/TypeScript-go/issues/3094) (Open, `bug`, **weswigham**)

**Declaration emit proceeds in the presence of TS7056**

*TypeScript emits declarations despite TS7056 errors caused by deeply nested conditional and tag-branded utility types.*

 * **RyanCavanaugh** added label `bug`
 * [1 month ago](https://github.com/microsoft/TypeScript-go/issues/3094#issuecomment-4068324272) **hkleungai** noted that the TS4053 error resembled a previously reported issue, argued that ts6 and ts7 should resolve the type reference without error, and referenced related issues #2504 and #3027
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/3094#issuecomment-4158824453) **weswigham** provided a status update on declaration emit behaviour in corsa versus strada, mentioned a 4-line diff to align implementations, and noted ongoing debugging of -b unit test failures
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [Issue microsoft/TypeScript-go#3120](https://github.com/microsoft/TypeScript-go/issues/3120) (Closed, `Crash`, **iisaduan**)

**thread exhaustion \- program exceeds 10000\-thread limit \- one off error**

*An unreproducible Go runtime crash arises when the program exceeds the 10000-thread limit.*

 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/3120#issuecomment-4229269618) **ekazakov14** reported experiencing the same intermittent error in CI/CD with a large project and provided their tsgo version
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3120#issuecomment-4239471509) **jakebailey** said "It's possible that this would be fixed in the same way as #3139."
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3120#issuecomment-4239474401) **jakebailey** said "@ekazakov14 Can you try https://github.com/microsoft/typescript-go/pull/3369 or https://github.com/microsoft/typescript-go/pull/3394?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/3120#issuecomment-4248088280) **RyanCavanaugh** said "I'm going to assert this is a duplicate of #3139 since we don't know any other ways this can happen."
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#3139](https://github.com/microsoft/TypeScript-go/issues/3139) (Closed, `Needs More Info`, **jakebailey**)

**runtime: failed to create new OS thread**

*Running tsgo on a large macFUSE-mounted TypeScript project exhausts OS threads and crashes the Go runtime.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3139#issuecomment-4237844283) **vetptzru** tested the latest changes on macFUSE and reported that everything worked correctly
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3139#issuecomment-4238182509) **jakebailey** said "Can you also try https://github.com/microsoft/typescript-go/pull/3394?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/3139#issuecomment-4243894760) **vetptzru** tested PR #3394 on macFUSE and confirmed it resolved the issue without crashing, observed normal thread counts, and offered to run further tests
 * (today) **RyanCavanaugh** set milestone to `TypeScript 7.0 RC`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3227](https://github.com/microsoft/TypeScript-go/issues/3227) (Open, `possible improvement`, **DanielRosenwasser**, **Copilot**)

**Track file type or extension for failing requests**

*Track file extensions for failing requests to aid in reproducing crashes and identifying language-specific issues.*

 * (2 weeks ago) **DanielRosenwasser** assigned to **Copilot**, **DanielRosenwasser**
 * **RyanCavanaugh** added label `possible improvement`
 * **RyanCavanaugh** added to milestone `Possible Improvement`

### [Issue microsoft/TypeScript-go#3242](https://github.com/microsoft/TypeScript-go/issues/3242) (Open, `bug`, **RyanCavanaugh**, **Copilot**)

**No error for values named 'Object' \(in CommonJS\)**

*TypeScript incorrectly permits a class named Object to be used with object spread in CommonJS modules without reporting an error.*

 * (2 weeks ago) **RyanCavanaugh** added label `bug`, and assigned to **Copilot**, **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3242#issuecomment-4248107590) **RyanCavanaugh** said "#2087"
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [Issue microsoft/TypeScript-go#3251](https://github.com/microsoft/TypeScript-go/issues/3251) (Closed, `Crash`, **DanielRosenwasser**, **Copilot**)

**Signature help assertion failure**

*An assertion failure in the Go language server's signature help getContainingArgumentInfo crashes without known repro steps, possibly tied to reparsing.*

 * (2 weeks ago) **DanielRosenwasser** added label `Crash`, and assigned to **Copilot**, **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3251#issuecomment-4248113395) **RyanCavanaugh** said "Closing in the absence of a repro"
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#3263](https://github.com/microsoft/TypeScript-go/pull/3263) (Open)

**Preserve original comments on params in dts generated by pseudo type node builder under \`removeComments: false\`**

*Declaration files generated by the pseudo type node builder with removeComments disabled fail to preserve original parameter comments.*

 * created by **Andarist**
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3263#issuecomment-4156791336) **jakebailey** said "At some level, I wonder if this is even worth it."
 * [later](https://github.com/microsoft/TypeScript-go/pull/3263#issuecomment-4250720724) **Andarist** noted that shouldWriteComment explicitly allows jsdoc-like comments and that the dts emitter configures the printer with onlyPrintJsDocStyle enabled

### [PR microsoft/TypeScript-go#3268](https://github.com/microsoft/TypeScript-go/pull/3268) (Closed, **RyanCavanaugh**, **Copilot**)

**Fix missing TS2725 error for class named 'Object' in non\-ES2015 modules**

*Implement a collision check in the Go TypeScript checker to report TS2725 when a class is named 'Object' in CommonJS modules.*

 * (2 weeks ago) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3268#issuecomment-4143847388) **jakebailey** said "Why not fix #2087 and fix all of these?"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#3318](https://github.com/microsoft/TypeScript-go/issues/3318) (Open, `Domain: Editor`, **iisaduan**)

**Missing \`addMissingImports\` code action/code fix**

*VSCode’s editor.codeActionOnSave lacks implementation of TypeScript’s addMissingImports code action and code fix.*

 * created by **iisaduan**
 * **iisaduan** assigned to **iisaduan**
 * (today) **RyanCavanaugh** added label `Domain: Editor`, and set milestone to `Post-7.0`

### [Issue microsoft/TypeScript-go#3319](https://github.com/microsoft/TypeScript-go/issues/3319) (Open, **iisaduan**)

**Missing \`fixAll\` code action/code fix**

*VSCode’s TypeScript Go extension does not support the source.fixAll.ts code action or corresponding individual codefixes for editor.codeActionOnSave.*

 * created by **iisaduan**
 * **iisaduan** assigned to **iisaduan**
 * **RyanCavanaugh** added to milestone `Post-7.0`

### [Issue microsoft/TypeScript-go#3320](https://github.com/microsoft/TypeScript-go/issues/3320) (Open, `Domain: Editor`, **iisaduan**)

**Missing \`removeUnused\` code fix/code action**

*The removeUnused code action and underlying unused identifier fixes are not implemented for VSCode’s TypeScript codeActionOnSave.*

 * created by **iisaduan**
 * **iisaduan** assigned to **iisaduan**
 * (today) **RyanCavanaugh** added label `Domain: Editor`, and set milestone to `Post-7.0`

### [Issue microsoft/TypeScript-go#3338](https://github.com/microsoft/TypeScript-go/issues/3338) (Open, `possible improvement`, **mjbvz**)

**TSGO: command 'typescript\.restartTsServer' not found**

*Enabling the TypeScript native preview feature in VSCode 1.113.0 removes the 'typescript.restartTsServer' command.*

 * created by **eblocha**
 * **vs-code-engineering[bot]** assigned to **mjbvz**
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/3338#issuecomment-4184835689) **jakebailey** pointed out that the provided command didn't restart the new language server and suggested hiding it when tsserver wasn't used
 * (today) **RyanCavanaugh** added label `possible improvement`, and set milestone to `Possible Improvement`

### [Issue microsoft/TypeScript-go#3340](https://github.com/microsoft/TypeScript-go/issues/3340) (Closed)

**\[ServerErrors\]\[TypeScript\] main vs **

*The TypeScript error-delta pipeline on main failed with server errors and varied outcomes while analyzing 300 repositories.*

 * created by **typescript-bot**
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#3342](https://github.com/microsoft/TypeScript-go/issues/3342) (Closed, **jakebailey**, **Copilot**)

**\`\-\-showConfig\` does not include \`files\` field**

*tsgo’s --showConfig command fails to include the resolved files list in its output, unlike tsc’s --showConfig.*

 * (1 week ago) **jakebailey** assigned to **Copilot**, **jakebailey**
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/3342#issuecomment-4188373927) **jakebailey** said "Funnily, the original code was not written with the intent that this work, but behaved this way due to a bug!"
 * [today](https://github.com/microsoft/TypeScript-go/issues/3342#issuecomment-4248171288) **RyanCavanaugh** stated that they didn't consider it a defect and noted that --showConfig is meant for humans to determine implied configs, while --explainListFiles is superior for understanding file lists
 * **RyanCavanaugh** added to milestone `Possible Improvement`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3343](https://github.com/microsoft/TypeScript-go/pull/3343) (Closed, **jakebailey**, **Copilot**)

**Fix \`\-\-showConfig\` to include \`files\` field**

*Remove buggy filtering and directly list all resolved files so tsgo --showConfig correctly includes the files field.*

 * created by **Copilot**
 * (1 week ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3357](https://github.com/microsoft/TypeScript-go/issues/3357) (Closed, `Crash`, **DanielRosenwasser**, **weswigham**, **Copilot**)

**Nil pointer derefence in \`\(\*NodeBuilderImpl\)\.addPropertyToElementList\` with  \`\-\-tsBuildInfoFile\`**

*A nil pointer dereference occurs in NodeBuilderImpl.addPropertyToElementList when running with the --tsBuildInfoFile option.*

 * (1 week ago) **DanielRosenwasser** assigned to **Copilot**, **DanielRosenwasser**, **weswigham**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3358](https://github.com/microsoft/TypeScript-go/pull/3358) (Closed, **gabritto**)

**Implement LSP\-based code edits with file renaming**

*Implement LSP willRenameFiles support to perform file renames with module specifier updates and arbitrary extension handling.*

 * created by **Andarist**
 * **gabritto** assigned to **gabritto**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3358#issuecomment-4238669742) **jakebailey** said "This also closes #1882, yes?"
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript-go#3361](https://github.com/microsoft/TypeScript-go/pull/3361) (Closed, **DanielRosenwasser**, **Copilot**)

**Fix nil pointer dereference in addPropertyToElementList**

*Add nil guard for propertySymbol.Parent in addPropertyToElementList to avoid crashes with synthetic union/intersection properties*

 * [6 days ago](https://github.com/microsoft/TypeScript-go/pull/3361#issuecomment-4208150468) **DanielRosenwasser** said "@copilot?"
 * [6 days ago](https://github.com/microsoft/TypeScript-go/pull/3361#issuecomment-4208303140) **Copilot** explained how the previous test didn't crash, described a new mixin-based test that triggered the crash, and confirmed its failure without the fix and success with it
 * [6 days ago](https://github.com/microsoft/TypeScript-go/pull/3361#issuecomment-4208959118) **Copilot** added a test file with --incremental and --tsBuildInfoFile directives confirming the crash in the incremental compilation path
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3364](https://github.com/microsoft/TypeScript-go/issues/3364) (Open, **DanielRosenwasser**, **andrewbranch**, **mjbvz**, **Copilot**)

**No project found for untitled file**

*VS Code LSP reports a no project found for URI untitled:Untitled-1 error when opening an anonymous unsaved file*

 * (6 days ago) **DanielRosenwasser** assigned to **DanielRosenwasser**, **andrewbranch**
 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/3364#issuecomment-4216990910) **andrewbranch** suggested improving the error message and delaying file removal to handle diagnostic requests after closing an untitled file
 * (today) **RyanCavanaugh** set milestone to `Post-7.0`, and assigned to **mjbvz**

### [Issue microsoft/TypeScript-go#3370](https://github.com/microsoft/TypeScript-go/issues/3370) (Closed, `duplicate`)

**Bad inference for param of type T\[\] \| T\[\]\[\]**

*tsgo misinfers the generic type as an extra array level when narrowing T[] | T[][]*

 * created by **jsnajdr**
 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/3370#issuecomment-4213268869) **JoostK** said "Sounds like https://github.com/microsoft/typescript-go/issues/1789"
 * **ahejlsberg** added label `duplicate`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#3371](https://github.com/microsoft/TypeScript-go/issues/3371) (Closed, `Domain: Editor`, **andrewbranch**, **Copilot**)

**Global keywords in code suggestion shadowed by auto imports with same name**

*Code suggestions for global keywords like "function" are shadowed by same-named module auto-imports, hindering keyword completion.*

 * created by **yume-chan**
 * **yume-chan** added label `Domain: Editor`
 * (today) **RyanCavanaugh** set milestone to `TypeScript 7.0 RC`, and assigned to **andrewbranch**
 * **andrewbranch** assigned to **Copilot**
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#3374](https://github.com/microsoft/TypeScript-go/issues/3374) (Open, `Crash`, **DanielRosenwasser**, **Copilot**)

**Code action crash from \`setLastNonTriviaPosition\`**

*A code action crashes the TypeScript printer in setLastNonTriviaPosition while emitting JSX text.*

 * (5 days ago) **DanielRosenwasser** assigned to **DanielRosenwasser**, **Copilot**, and unassigned **Copilot**
 * **RyanCavanaugh** added to milestone `Possible Improvement`

### [Issue microsoft/TypeScript-go#3376](https://github.com/microsoft/TypeScript-go/issues/3376) (Open, `Crash`, **DanielRosenwasser**, **Copilot**)

**nil pointer dereference during diagnostics request**

*A nil pointer dereference occurs during diagnostics requests when resolving a SourceFile path.*

 * (5 days ago) **DanielRosenwasser** assigned to **DanielRosenwasser**, **Copilot**, and unassigned **Copilot**
 * **RyanCavanaugh** added to milestone `Possible Improvement`

### [Issue microsoft/TypeScript-go#3378](https://github.com/microsoft/TypeScript-go/issues/3378) (Open, `Crash`, **DanielRosenwasser**, **Copilot**)

**LSP request failure for diagnostics during type serialization**

*The TypeScript language server fails to generate diagnostics during type serialization due to symbol accessibility errors.*

 * (5 days ago) **DanielRosenwasser** added label `Crash`, and assigned to **Copilot**, **DanielRosenwasser**
 * **RyanCavanaugh** added to milestone `Possible Improvement`

### [Issue microsoft/TypeScript-go#3384](https://github.com/microsoft/TypeScript-go/issues/3384) (Open, `Crash`, **andrewbranch**)

**Crash in adjusting positions for folding ranges**

*Adjusting folding range end positions in the Go language service now crashes due to LineAndCharacterToPosition conversion errors.*

 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/3384#issuecomment-4226616160) **DanielRosenwasser** said "No idea - we only keep the stack around."
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/3384#issuecomment-4227398094) **DanielRosenwasser** suspected the issue stemmed from the snapshotfs implementation because reloadEntry methods didn’t update certain fields and noted difficulty reproducing it end-to-end
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3384#issuecomment-4239589443) **jakebailey** said "Not overwriting those definitely feels like a bug. We should probably shove those off into a sidecar that can be overwritten with a new object each time the content changes."
 * (today) **RyanCavanaugh** set milestone to `TypeScript 7.0 RC`, and assigned to **andrewbranch**
 * [later](https://github.com/microsoft/TypeScript-go/issues/3384#issuecomment-4253249016) **andrewbranch** said "This doesn't look like a bug to me—e.Change clones the file which unsets its line map."

### [Issue microsoft/TypeScript-go#3386](https://github.com/microsoft/TypeScript-go/issues/3386) (Closed)

**\[ServerErrors\]\[TypeScript\] main vs **

*TypeScript CI reported errors in 300 repos, finding 14 changes, 193 unchanged, and 93 clone, timeout, or unknown failures.*

 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/3386#issuecomment-4227338609) **typescript-bot** reported that the server connection closed prematurely with undefined for n8n-io/n8n, included raw error text, artifact links, recent protocol requests, and reproduction steps
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/3386#issuecomment-4227338657) **typescript-bot** reported a panic when handling a textDocument/formatting request due to a debug failure: False expression: Token end is child end
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/3386#issuecomment-4227338675) **typescript-bot** reported a panic in textDocument/formatting request due to a debug failure and included the stack trace
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#3394](https://github.com/microsoft/TypeScript-go/pull/3394) (Closed)

**Limit all OS FS calls with semaphores**

*Use semaphores to limit concurrent OS file system calls as an alternative to #3369 and to resolve issue #3139.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3394#issuecomment-4238183278) **jakebailey** said "@typescript-bot perf test this faster"
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3394#issuecomment-4238183692) **typescript-bot** reported starting CI jobs and provided links to status and results
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3394#issuecomment-4238322677) **typescript-bot** provided the requested perf run results
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3395](https://github.com/microsoft/TypeScript-go/pull/3395) (Closed)

**Fix watching files outside the workspace and realpaths symlinked into programs**

*Use relative path patterns for file watching and reverse-map realpaths to symlink locations to support npm-linked dependencies outside the workspace.*

 * created by **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#3399](https://github.com/microsoft/TypeScript-go/issues/3399) (Closed, `duplicate`)

**instance of narrowing loses property type for a class returned from a generic factory**

*TypeScript fails to narrow a generic factory-produced class’s property type after an instanceof check, allowing invalid assignments.*

 * created by **kljnepk**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3399#issuecomment-4244743808) **ahejlsberg** identified the issue as a duplicate of issue #17253, explained that runtime type information is absent so the compiler substitutes any for generic parameters, and agreed that substituting unknown would be safer though unsound for contravariant positions
 * **ahejlsberg** added label `duplicate`
 * [today](https://github.com/microsoft/TypeScript-go/issues/3399#issuecomment-4245380456) **jakebailey** said "Yes, not sure why this is reported here, this is not unique to tsgo."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3400](https://github.com/microsoft/TypeScript-go/pull/3400) (Closed, **andrewbranch**, **Copilot**)

**Filter non\-contextual keyword auto\-imports to prevent keyword shadowing**

*Filter out auto-imported symbols named after non-contextual reserved keywords to avoid shadowing keyword completions.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#3401](https://github.com/microsoft/TypeScript-go/pull/3401) (Open)

**Fix file counts, jsx in project telemetry**

*Update project telemetry to accurately categorize files by their declared type and ensure the JSX metric is reported as a string.*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#3402](https://github.com/microsoft/TypeScript-go/pull/3402) (Closed)

**Support alternate spellings in JSDoc type annotations**

*Port getIntendedTypeFromJSDocTypeReference to support alternate spellings in JSDoc type annotations aligned with Strada*

 * created by **ahejlsberg**

### [PR microsoft/TypeScript-go#3403](https://github.com/microsoft/TypeScript-go/pull/3403) (Open)

**Exposing more endpoints**

*Expose additional API endpoints to expand available functionality.*

 * created by **navya9singh**

### [Issue microsoft/TypeScript-go#3404](https://github.com/microsoft/TypeScript-go/issues/3404) (Closed, `Domain: Editor`, **jakebailey**, **Copilot**)

**Object\-like type not formatted well with verbosity level 0 in hover**

*Hover tooltips for object types at verbosity level 0 show inline definitions instead of expected multiline formatting with newlines.*

 * created by **Withered-Flower-0422**
 * **Withered-Flower-0422** added label `Domain: Editor`
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#3405](https://github.com/microsoft/TypeScript-go/issues/3405) (Open, `Domain: Editor`, **jakebailey**, **Copilot**)

**JSDoc disapprears after type calculation**

*Hovering over a parameter from an intersection type no longer shows its JSDoc comment after TS type calculation.*

 * created by **Withered-Flower-0422**
 * **Withered-Flower-0422** added label `Domain: Editor`
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#3406](https://github.com/microsoft/TypeScript-go/issues/3406) (Open, `Crash`)

**Unbounded memory and unbounded CPU leads to OOM or crashes container**

*Build process consumes all available CPU and memory, causing container OOM errors or SIGTERM failures.*

 * created by **sroussey**
 * **sroussey** added label `Crash`

### [PR microsoft/TypeScript-go#3407](https://github.com/microsoft/TypeScript-go/pull/3407) (Closed, **jakebailey**, **Copilot**)

**Always format object\-like types multiline in hover**

*Always format object-like types across multiple lines in hover by enabling the multiline flag and updating printer output and tests.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#3408](https://github.com/microsoft/TypeScript-go/pull/3408) (Open, **jakebailey**, **Copilot**)

**Fix JSDoc disappearing on destructured parameters from intersection types**

*Ensure JSDoc comments appear on destructured parameters from intersection types by falling back to symbol declarations when ValueDeclaration is missing.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#3409](https://github.com/microsoft/TypeScript-go/pull/3409) (Closed)

**Fix nil\-config project crash during project tree loading**

*A nil project configuration triggers a crash during project tree loading.*

 * created by **Andarist**

### [Issue microsoft/TypeScript-go#3410](https://github.com/microsoft/TypeScript-go/issues/3410) (Open, `bug`, `Domain: Editor`, **weswigham**)

**Type serializer omits type arguments of outer functions**

*The tsgo type serializer drops outer function generic arguments when hovering on returned classes, displaying makeBox.Box instead of makeBox<string>.Box.*

 * created by **ahejlsberg**
 * (later) **ahejlsberg** added labels `bug`, `Domain: Editor`, set milestone to `TypeScript 7.0 RC`, and assigned to **weswigham**

### [Issue microsoft/TypeScript-go#3411](https://github.com/microsoft/TypeScript-go/issues/3411) (Open, `Domain: Editor`)

**Missing generic type description in hover**

*tsgo hover omits showing instantiated generic types in inherited method signatures, unlike TypeScript 6.0.*

 * created by **Withered-Flower-0422**
 * **Withered-Flower-0422** added label `Domain: Editor`
 * [later](https://github.com/microsoft/TypeScript-go/issues/3411#issuecomment-4253180257) **jakebailey** said "Yes I'm pretty sure this is exactly the same as that linked issue"

