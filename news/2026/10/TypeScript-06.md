# Report for 2026-10-06 (Tuesday, October 6th, 2026)

20 different users commented on 83 different issues.

## Recommended Actions

 * Response Recommended
    * @Konan69 suggested adding test cases and opened PR #64671 in [microsoft/TypeScript#64431](https://github.com/microsoft/TypeScript/issues/64431#issuecomment-6041533127)
    * @atscott asked for a way to push in-memory .ngtypecheck.ts files into TS-Go's VFS in [microsoft/TypeScript#64611](https://github.com/microsoft/TypeScript/issues/64611#issuecomment-6025772172)
    * @atscott provided a detailed list of missing API handlers and snapshot persistence requirements in [microsoft/TypeScript#64611](https://github.com/microsoft/TypeScript/issues/64611#issuecomment-6027930040)
    * @Lojhan asked whether content mapping was the intended way or if another API was planned for this use case in [microsoft/TypeScript#64611](https://github.com/microsoft/TypeScript/issues/64611#issuecomment-6037027784)
    * @splincode asked if a release note should be added in [microsoft/TypeScript#64626](https://github.com/microsoft/TypeScript/pull/64626#issuecomment-6031954122)

## Activity Summary

### [Issue microsoft/TypeScript#59342](https://github.com/microsoft/TypeScript/issues/59342) (Closed, `Needs Investigation`, **sheetalkamat**)

**⚡ Performance: Project service doesn't cache all fs\.realpath **

*typescript-eslint’s parserOptions.projectService makes multiple uncached fs.realpath calls, causing minor performance degradation during linting*

 * [2.2 years ago](https://github.com/microsoft/TypeScript/issues/59342#issuecomment-2236867413) **sheetalkamat** noted that realPath caching was limited to individual projects due to cache invalidation issues (tracked in #55968) and promised to investigate further
 * **sheetalkamat** assigned to **sheetalkamat**
 * [1.2 years ago](https://github.com/microsoft/TypeScript/issues/59342#issuecomment-2997933155) **wagenet** said "@sheetalkamat any news here?"
 * **RyanCavanaugh** added label `Needs Investigation`

### [Issue microsoft/TypeScript#62127](https://github.com/microsoft/TypeScript/issues/62127) (Open, `Bug`)

**"used before being assigned" fires on LHS inside parens/type assertion**

*TypeScript 5.7+ incorrectly reports 'used before being assigned' errors for valid assignments wrapped in parentheses or type assertions on the left-hand side.*

 * created by **jakebailey**
 * **jakebailey** assigned to **Copilot**
 * [1.1 years ago](https://github.com/microsoft/TypeScript/issues/62127#issuecomment-3119876150) **jakebailey** said "This is actually new in 5.6."
 * (today) **RyanCavanaugh** added label `Bug`, set milestone to `Backlog`, and unassigned **Copilot**

### [Issue microsoft/TypeScript#63777](https://github.com/microsoft/TypeScript/issues/63777) (Open, `Infrastructure`)

**Defer baseline comparisons until end of test**

*Current baselining runs comparisons eagerly, causing tests with in-test edits to remain disabled instead of re-enabling them.*

 * created by **DanielRosenwasser**
 * **DanielRosenwasser** assigned to **Copilot**
 * (today) **RyanCavanaugh** added label `Infrastructure`, set milestone to `Backlog`, and unassigned **Copilot**

### [Issue microsoft/TypeScript#63778](https://github.com/microsoft/TypeScript/issues/63778) (Open, `Bug`, **ahejlsberg**)

**TS2322 error in tsgo but not tsc**

*tsgo incorrectly reports a TS2322 error when spreading a union and assigning E.Foo to E.Bar, even though tsc compiles it successfully.*

 * (1.1 years ago) **ahejlsberg** closed the issue
 * [1.1 years ago](https://github.com/microsoft/TypeScript/issues/63778#issuecomment-5351498792) **ahejlsberg** explained the error elaboration logic flaw with union types leading to order-dependent excess property errors and demonstrated it with example code
 * (1.1 years ago) **ahejlsberg** reopened the issue
 * (today) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#63792](https://github.com/microsoft/TypeScript/issues/63792) (Open, `Suggestion`, **DanielRosenwasser**)

**Questionable code lenses for object type members on a single line**

*Suppress code lenses on object type members defined inline when their parent and siblings share the same line.*

 * created by **DanielRosenwasser**
 * **RyanCavanaugh** assigned to **DanielRosenwasser**
 * **RyanCavanaugh** added label `Suggestion`

### [Issue microsoft/TypeScript#63794](https://github.com/microsoft/TypeScript/issues/63794) (Closed, **Copilot**)

**References code lens does not include imports as references**

*The references code lens fails to count imports as references, showing zero references despite TypeScript 6.0 support.*

 * created by **mjbvz**
 * **jakebailey** assigned to **Copilot**
 * (today) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript/issues/63794#issuecomment-6026580411) **RyanCavanaugh** said "I think this has been fixed - can't repro anymore."

### [Issue microsoft/TypeScript#63798](https://github.com/microsoft/TypeScript/issues/63798) (Open, `Needs Investigation`, **DanielRosenwasser**)

**Reconsider tsconfig membership lookups for \`\.d\.ts\` files in \`composite\`**

*TypeScript 6.0 and 7.0 unexpectedly exclude .d.ts files listed in tsconfig due to composite and rootDir changes*

 * **RyanCavanaugh** assigned to **DanielRosenwasser**
 * (27 weeks ago) **DanielRosenwasser** closed the issue
 * (27 weeks ago) **DanielRosenwasser** reopened the issue
 * **RyanCavanaugh** added label `Needs Investigation`

### [Issue microsoft/TypeScript#63803](https://github.com/microsoft/TypeScript/issues/63803) (Open, `Needs Investigation`, `Domain: LS: Auto-import`, **andrewbranch**)

**Missing auto\-import for subpath imports of other local packages**

*VS Code TypeScript auto-imports fail to recognize subpath imports from sibling local workspace packages.*

 * [26 weeks ago](https://github.com/microsoft/TypeScript/issues/63803#issuecomment-5351501609) **psznm** described that import suggestions did not work for relative paths outside the tsconfig directory and provided examples and a workaround
 * [26 weeks ago](https://github.com/microsoft/TypeScript/issues/63803#issuecomment-5351501648) **andrewbranch** explained that files from another package are resolved via node_modules specifiers without computing another name and noted uncertainty about using imports with relative paths to other packages
 * [26 weeks ago](https://github.com/microsoft/TypeScript/issues/63803#issuecomment-5351501674) **psznm** described that deleting node_modules/pkg2 enabled auto imports for "#pkg4/*" but that the workaround failed without including ../pkg2 in tsconfig.json
 * (today) **RyanCavanaugh** added labels `Needs Investigation`, `Domain: LS: Auto-import`

### [Issue microsoft/TypeScript#63809](https://github.com/microsoft/TypeScript/issues/63809) (Open, `Suggestion`, **iisaduan**)

**Missing \`addMissingImports\` code action/code fix**

*VSCode’s editor.codeActionOnSave lacks implementation of TypeScript’s addMissingImports code action and code fix.*

 * [22 weeks ago](https://github.com/microsoft/TypeScript/issues/63809#issuecomment-5351502383) **dhoulb** described that code actions on save no longer automatically add missing imports, causing red squiggles and manual steps and lamented the loss of the previous smooth workflow
 * [22 weeks ago](https://github.com/microsoft/TypeScript/issues/63809#issuecomment-5351502414) **iisaduan** noted that the behavior would resume with the old configuration after naming fixes and suggested adding editor.codeActionsOnSave.source.fixAll set to always or explicit to replicate it now
 * [22 weeks ago](https://github.com/microsoft/TypeScript/issues/63809#issuecomment-5351502443) **dhoulb** said "That's amazing, thanks so much @iisaduan — can confirm I tested and it worked."
 * **RyanCavanaugh** added label `Suggestion`

### [Issue microsoft/TypeScript#63810](https://github.com/microsoft/TypeScript/issues/63810) (Open, `Suggestion`, **iisaduan**)

**Missing \`fixAll\` code action/code fix**

*VSCode’s TypeScript Go extension does not support the source.fixAll.ts code action or corresponding individual codefixes for editor.codeActionOnSave.*

 * **iisaduan** assigned to **iisaduan**
 * [24 weeks ago](https://github.com/microsoft/TypeScript/issues/63810#issuecomment-5351502423) **jakebailey** said "Is this done with microsoft/typescript-go#3382? "
 * [22 weeks ago](https://github.com/microsoft/TypeScript/issues/63810#issuecomment-5351502449) **iisaduan** clarified that fixAll runs only a subset of code fixes, referenced relevant issues, and noted the need for an extension update to reveal missing code actions
 * **RyanCavanaugh** added label `Suggestion`

### [Issue microsoft/TypeScript#63811](https://github.com/microsoft/TypeScript/issues/63811) (Open, `Suggestion`, **iisaduan**)

**Missing \`removeUnused\` code fix/code action**

*The removeUnused code action and underlying unused identifier fixes are not implemented for VSCode’s TypeScript codeActionOnSave.*

 * **iisaduan** assigned to **iisaduan**
 * [18 weeks ago](https://github.com/microsoft/TypeScript/issues/63811#issuecomment-5351502581) **a-tarasyuk** asked whether implementing support for removeUnused/removeUnusedImports/unusedIdentifier was still considered useful
 * [18 weeks ago](https://github.com/microsoft/TypeScript/issues/63811#issuecomment-5351502606) **iisaduan** noted that removeUnusedImports was already implemented and that other code actions would be considered for a post-7.0 release pending feedback
 * **RyanCavanaugh** added label `Suggestion`

### [Issue microsoft/TypeScript#63812](https://github.com/microsoft/TypeScript/issues/63812) (Closed, `External`, **DanielRosenwasser**, **andrewbranch**, **mjbvz**, **Copilot**)

**No project found for untitled file**

*VS Code LSP reports a no project found for URI untitled:Untitled-1 error when opening an anonymous unsaved file*

 * **RyanCavanaugh** assigned to **mjbvz**
 * [24 weeks ago](https://github.com/microsoft/TypeScript/issues/63812#issuecomment-5351502763) **mjbvz** said "@andrewbranch You're using Dirk's LSP host, right? Or are you using the VS Code apis directly? "
 * [24 weeks ago](https://github.com/microsoft/TypeScript/issues/63812#issuecomment-5351502778) **DanielRosenwasser** stated that functionality should be handled by the language client and noted the project is on version 10.0.0-next.21, linking to the package.json
 * **RyanCavanaugh** added label `External`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63871](https://github.com/microsoft/TypeScript/issues/63871) (Closed, **andrewbranch**)

**\[API\] Expose globals declared by a source file**

*Expose SourceFile.Locals in the TypeScript JS API to more reliably retrieve global symbols declared in a source file.*

 * created by **Gerrit0**
 * **RyanCavanaugh** assigned to **andrewbranch**
 * [6 weeks ago](https://github.com/microsoft/TypeScript/issues/63871#issuecomment-5369256998) **mrazauskas** said "Seems like .getSymbolsInScope() got added few days ago. Reference: https://github.com/microsoft/typescript-go/pull/4897"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63886](https://github.com/microsoft/TypeScript/issues/63886) (Open, `Bug`, **RyanCavanaugh**)

**Memory skyrockets with VSCode extension**

*Enabling the VSCode Typescript 7 extension with tsgo on a file using gulp-sass causes the TypeScript server to rapidly exhaust all system memory.*

 * [5 weeks ago](https://github.com/microsoft/TypeScript/issues/63886#issuecomment-5427559355) **RyanCavanaugh** said "Can you try again with the latest build? I'm not seeing any memory rise at all when uncommenting"
 * [5 weeks ago](https://github.com/microsoft/TypeScript/issues/63886#issuecomment-5429016630) **jjspace** confirmed issue still occurred, observed that the extension consumed almost 10GB of memory before stabilizing, and provided version info and a system monitor screenshot
 * **RyanCavanaugh** removed label `Needs More Info`
 * (today) **RyanCavanaugh** added label `Bug`, set milestone to `TypeScript 7.1.1 RC`, and assigned to **RyanCavanaugh**

### [PR microsoft/TypeScript#64063](https://github.com/microsoft/TypeScript/pull/64063) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Ditch nodeData interface in favor of generated accessors**

*Replace dynamic nodeData interface with generated accessors to reduce binary size, cut AST symbols, and improve compile performance.*

 * [5 weeks ago](https://github.com/microsoft/TypeScript/pull/64063#issuecomment-5500018137) **typescript-automation[bot]** provided the requested performance run results
 * [5 weeks ago](https://github.com/microsoft/TypeScript/pull/64063#issuecomment-5500189461) **jakebailey** said "Hm, there's something to this, I think, I need to investigate."
 * [1 month ago](https://github.com/microsoft/TypeScript/pull/64063#issuecomment-5592560452) **jakebailey** reintroduced indirection to recover lost performance and noted it made the binary smaller
 * [today](https://github.com/microsoft/TypeScript/pull/64063#issuecomment-6026260616) **jakebailey** said "@typescript-bot perf test this"
 * [today](https://github.com/microsoft/TypeScript/pull/64063#issuecomment-6026261943) **typescript-automation[bot]** started performance test builds and posted status update with links to build results
 * [today](https://github.com/microsoft/TypeScript/pull/64063#issuecomment-6026643943) **typescript-automation[bot]** provided the results of the requested performance run

### [Issue microsoft/TypeScript#64155](https://github.com/microsoft/TypeScript/issues/64155) (Closed, `Suggestion`, **jakebailey**, **Copilot**)

**Should the native TypeScript LSP include top\-level imports in its \`textDocument/documentSymbol\` response?**

*Clarify whether the native TypeScript language server should exclude top-level imports from documentSymbol results as VS Code currently does.*

 * [1 month ago](https://github.com/microsoft/TypeScript/issues/64155#issuecomment-5533063216) **jakebailey** clarified that the filtering was unintentional due to VS Code's TS extension and asked what Visual Studio expects
 * (1 month ago) **jakebailey** assigned to **Copilot**, **jakebailey**
 * **RyanCavanaugh** added label `Suggestion`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64160](https://github.com/microsoft/TypeScript/pull/64160) (Closed, `For Uncommitted Bug`, **jakebailey**, **Copilot**)

**Exclude top\-level imports from document symbols**

*Modify LSP documentSymbol results to omit top-level import and import-equals declarations, aligning with VS Code Outline behavior.*

 * (1 month ago) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/64160#issuecomment-5765997553) **jakebailey** said "Marking as ready for review, but we need to make sure this doesn't regress VS. @joj @navya9singh for awareness."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64411](https://github.com/microsoft/TypeScript/pull/64411) (Open, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Preserve primitive literal union origins without special intersections**

*Preserve literal union origins for string, number, and bigint in completions and quick info without special intersections.*

 * [today](https://github.com/microsoft/TypeScript/pull/64411#issuecomment-6019356961) **jakebailey** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/64411#issuecomment-6019359564) **typescript-automation[bot]** reported that CI jobs were started and provided status and result links
 * [today](https://github.com/microsoft/TypeScript/pull/64411#issuecomment-6019916048) **typescript-automation[bot]** posted the requested performance run results
 * [today](https://github.com/microsoft/TypeScript/pull/64411#issuecomment-6024731101) **typescript-automation[bot]** informed @jakebailey that the DT test run failed and asked to check the log
 * [today](https://github.com/microsoft/TypeScript/pull/64411#issuecomment-6025424761) **jakebailey** said "The DT hang might be real? It's taking much longer?"
 * [today](https://github.com/microsoft/TypeScript/pull/64411#issuecomment-6025430521) **jakebailey** said "Multiple of the top / user tests are also hitting that."
 * [today](https://github.com/microsoft/TypeScript/pull/64411#issuecomment-6026638645) **weswigham** said "I'll look into it before I remove the compat mapped type behavior and simplify the quickinfo to just the origin type."
 * [today](https://github.com/microsoft/TypeScript/pull/64411#issuecomment-6026821305) **weswigham** said "Looks like just a reentrancy bug in the mapped type logic, which is going away anyway, simple fix then."
 * [today](https://github.com/microsoft/TypeScript/pull/64411#issuecomment-6027886986) **weswigham** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/64411#issuecomment-6027888024) **typescript-automation[bot]** reported that CI jobs started and provided status and result links
 * [today](https://github.com/microsoft/TypeScript/pull/64411#issuecomment-6028216027) **typescript-automation[bot]** reported DT test results indicating branch-only type errors in oojs-ui and react packages
 * [today](https://github.com/microsoft/TypeScript/pull/64411#issuecomment-6028235036) **jakebailey** speculated that if DT was exposed over the API they could prefer the new string and noted that the other failures were interesting
 * [today](https://github.com/microsoft/TypeScript/pull/64411#issuecomment-6028254590) **typescript-automation[bot]** reported that test results comparing baseline and PR looked good
 * [today](https://github.com/microsoft/TypeScript/pull/64411#issuecomment-6028261676) **typescript-automation[bot]** reported the perf run results for the requested baseline vs PR comparison
 * [today](https://github.com/microsoft/TypeScript/pull/64411#issuecomment-6028877744) **typescript-automation[bot]** provided build comparison results for the top 400 repos and requested review of interesting changes

### [Issue microsoft/TypeScript#64431](https://github.com/microsoft/TypeScript/issues/64431) (Open, `Bug`, **RyanCavanaugh**, **Copilot**)

**TS7031 false positive for nested object binding pattern with \`= {}\` default in an annotated parameter \(regression from \#64043\)**

*Nested object destructuring with default {} in a typed parameter erroneously triggers TS7031 errors after PR #64043*

 * (1 week ago) **RyanCavanaugh** added label `Bug`, and assigned to **Copilot**, **RyanCavanaugh**
 * [later](https://github.com/microsoft/TypeScript/issues/64431#issuecomment-6041533127) **Konan69** described contextually typed parameters triggering TS7031 errors in recent nightly, validated that #64440 removes the errors, suggested adding test cases, and opened #64671 with an alternative patch

### [PR microsoft/TypeScript#64469](https://github.com/microsoft/TypeScript/pull/64469) (Closed, `For Uncommitted Bug`, **johnfav03**)

**Index re\-exporting modules for declaration emit**

*Optimize TypeScript’s declaration emit performance by caching an export-to-module index to avoid repeated scans during incremental rebuilds*

 * [3 days ago](https://github.com/microsoft/TypeScript/pull/64469#issuecomment-5969259018) **gwkline** provided independent performance benchmarks applying the PR’s checker changes to a large monorepo, reported byte-identical outputs, noted speedups and minor memory increase, described optional incremental changes, highlighted a merge conflict, and offered further tests with a public repro
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/64469#issuecomment-5969338823) **gwkline** provided a link to their final implementation commit
 * **typescript-automation[bot]** assigned to **johnfav03**
 * [today](https://github.com/microsoft/TypeScript/pull/64469#issuecomment-6021277912) **weswigham** asked to split the two changes into separate PRs and noted that each should be evaluated independently
 * [today](https://github.com/microsoft/TypeScript/pull/64469#issuecomment-6025419461) **resure** provided split PR link after splitting the changes into separate PRs

### [PR microsoft/TypeScript#64526](https://github.com/microsoft/TypeScript/pull/64526) (Closed, `For Uncommitted Bug`)

**build members of keyof mapped types lazily**

*Implement lazy member tables for keyof mapped types to defer property symbol creation and enhance performance*

 * created by **maschwenk**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64526#issuecomment-6022090808) **maschwenk** closed the PR due to minimal heap savings and required rework atop future changes
 * (today) **maschwenk** closed the issue

### [Issue microsoft/TypeScript#64565](https://github.com/microsoft/TypeScript/issues/64565) (Open, `Needs Investigation`, **jakebailey**)

**TypeScript 7 VS Code extension: a workspace "typescript" 7\.x package is not detected, only "@typescript/native\-preview", which is no longer published**

*The TypeScript 7 VS Code extension fails to detect standard typescript@7 in workspace, using its bundled compiler instead.*

 * created by **leonidaz**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **jakebailey**

### [Issue microsoft/TypeScript#64576](https://github.com/microsoft/TypeScript/issues/64576) (Open, `Bug`, **andrewbranch**)

**TypeScript 7 VS Code extension: Go to Source Definition does not run in content\-mapped files, although tsc \-\-lsp answers for them**

*Go to Source Definition fails for content-mapped files in the TypeScript 7 VS Code extension due to language ID filtering despite LSP support.*

 * created by **leonidaz**
 * (today) **RyanCavanaugh** added label `Bug`, set milestone to `TypeScript 7.1.1 RC`, and assigned to **andrewbranch**

### [Issue microsoft/TypeScript#64579](https://github.com/microsoft/TypeScript/issues/64579) (Open, `Suggestion`)

**Content mappers: let a mapper opt out of formatting, so tsc \-\-lsp does not offer a formatter that returns no edits**

*Allow mappers to disable formatting registrations in tsc --lsp so editors no longer list ineffective TypeScript formatter*

 * created by **leonidaz**
 * **RyanCavanaugh** added label `Suggestion`

### [Issue microsoft/TypeScript#64580](https://github.com/microsoft/TypeScript/issues/64580) (Open, `Suggestion`)

**TypeScript 7 VS Code extension: let other extensions send requests to tsc \-\-lsp, like typescript\.tsserverRequest**

*Add support in the TypeScript 7 VS Code extension for other extensions to send tsc --lsp requests for content-mapped languages.*

 * created by **leonidaz**
 * **RyanCavanaugh** added label `Suggestion`

### [PR microsoft/TypeScript#64584](https://github.com/microsoft/TypeScript/pull/64584) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**\[api\] Stop dropping dispose Promises in the async API**

*Fix async API to use Symbol.asyncDispose instead of Symbol.dispose to preserve disposal promises and update diagnostics.*

 * (5 days ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript#64585](https://github.com/microsoft/TypeScript/issues/64585) (Open, `Duplicate`)

**TS Symbol typing clashes with standard, idiomatic JS**

*TypeScript’s symbol typing model conflicts with JavaScript’s native Symbol behavior, hindering idiomatic JS symbol usage.*

 * created by **michaelfig**
 * [4 days ago](https://github.com/microsoft/TypeScript/issues/64585#issuecomment-5956824676) **RyanCavanaugh** said "This seems like a straightforward duplicate of #35909, not a separate request"
 * [4 days ago](https://github.com/microsoft/TypeScript/issues/64585#issuecomment-5959601794) **michaelfig** identified the issue as a duplicate of #35909, offered to close it if the Related Work section of #64451 sufficed, and noted uncertainty about satisfying @typescript-automation
 * **RyanCavanaugh** added label `Duplicate`

### [Issue microsoft/TypeScript#64590](https://github.com/microsoft/TypeScript/issues/64590) (Open, `Bug`, **weswigham**)

**Declaration emit writes an import the file cannot resolve when the package has \`exports\`; no TS2883**

*TypeScript’s declaration emit generates unresolved imports for packages with an exports map in pnpm layouts without emitting TS2883 errors*

 * created by **kristojorg**
 * (today) **RyanCavanaugh** added label `Bug`, set milestone to `TypeScript 7.1.1 RC`, and assigned to **weswigham**

### [Issue microsoft/TypeScript#64591](https://github.com/microsoft/TypeScript/issues/64591) (Open, `Bug`, **johnfav03**)

**\`tsc \-b\`: incremental build keeps a declaration that names a removed re\-export, and passes a program a clean build rejects**

*An incremental TypeScript build retains stale declarations for a removed re-export, causing inconsistent successes compared to a clean build.*

 * created by **kristojorg**
 * (today) **RyanCavanaugh** added label `Bug`, set milestone to `TypeScript 7.1.1 RC`, and assigned to **johnfav03**

### [Issue microsoft/TypeScript#64593](https://github.com/microsoft/TypeScript/issues/64593) (Open, `Needs Investigation`, **gabritto**)

**Reverse\-mapped inference exposes private members as public; since \#63932 this rejects \`f\<T\>\(\) as C\`**

*Since PR #63932, reverse-mapped type inference exposes private members as public, causing errors when casting Readonly<Account & T> to Account.*

 * created by **kirkouimet**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.1.1 RC`, and assigned to **gabritto**

### [PR microsoft/TypeScript#64594](https://github.com/microsoft/TypeScript/pull/64594) (Open, `For Milestone Bug`, **gabritto**)

**Skip non\-public members when resolving reverse\-mapped types**

*Skip non-public class members when resolving reverse-mapped types to prevent them from becoming erroneously public.*

 * created by **kirkouimet**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/64594#issuecomment-5956190388) **kirkouimet** said "@microsoft-github-policy-service agree"
 * (today) **typescript-automation[bot]** added label `For Milestone Bug`, removed label `For Uncommitted Bug`, and assigned to **gabritto**

### [PR microsoft/TypeScript#64599](https://github.com/microsoft/TypeScript/pull/64599) (Open, `For Milestone Bug`, **weswigham**)

**Check package reachability before using exports in declarations**

*Reorder TypeScript’s export resolution logic to ensure package reachability is checked before applying exports in declarations*

 * created by **Andarist**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/64599#issuecomment-5957454475) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (today) **typescript-automation[bot]** added label `For Milestone Bug`, removed label `For Uncommitted Bug`, and assigned to **weswigham**

### [Issue microsoft/TypeScript#64602](https://github.com/microsoft/TypeScript/issues/64602) (Open, `Waiting for TC39`)

**Support deferred re\-exports**

*Support Stage 2 TC39 deferred re-export syntax in TypeScript, preserving JavaScript output and declaration types.*

 * created by **a-tarasyuk**
 * (today) **RyanCavanaugh** added labels `Suggestion`, `Waiting for TC39`, and removed label `Suggestion`

### [PR microsoft/TypeScript#64604](https://github.com/microsoft/TypeScript/pull/64604) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Update DOM types**

*Add and refine TypeScript DOM types to support new Web APIs, HTML sanitization, CSS and animation features, and compatibility changes*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/64604#issuecomment-6001196505) **typescript-automation[bot]** announced that jobs were starting and provided links to status and results
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64604#issuecomment-6001590231) **typescript-automation[bot]** reported DT test results showing type errors in d3-fetch and d3-fetch/v2 regarding the crossOrigin property
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64604#issuecomment-6002390913) **jakebailey** said "I guess this is all pretty expected. crossOrigin is the big break now."
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#64605](https://github.com/microsoft/TypeScript/issues/64605) (Open, `Needs Investigation`, **gabritto**)

**TS5115 in published Zod 4\.5–4\.6 types after \#64372**

*Zod 4.5.0–4.6.5 z.json() types cause TS5115 infinite circularity errors in TypeScript 7.1 nightlies after PR #64372, impacting ~62M weekly downloads.*

 * created by **colinhacks**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.1.1 RC`, and assigned to **gabritto**

### [Issue microsoft/TypeScript#64610](https://github.com/microsoft/TypeScript/issues/64610) (Open, `Suggestion`)

**Associate companion files with \`ProjectService\` without Content Mappers**

*Allow ProjectService to include companion files such as .html templates without requiring content mappers.*

 * created by **atscott**
 * **RyanCavanaugh** added label `Suggestion`

### [Issue microsoft/TypeScript#64611](https://github.com/microsoft/TypeScript/issues/64611) (Open, `Suggestion`)

**In\-memory virtual file overlay over LSP without faking \`didOpen\`**

*Add an LSP overlay mechanism to inject synthetic in-memory files into TS-Go’s virtual file system without faking didOpen notifications.*

 * created by **atscott**
 * **RyanCavanaugh** added label `Suggestion`
 * [today](https://github.com/microsoft/TypeScript/issues/64611#issuecomment-6025522276) **weswigham** suggested using content-mapping .ts files to map inner template strings but noted concerns about coordinating chaining
 * [today](https://github.com/microsoft/TypeScript/issues/64611#issuecomment-6025772172) **atscott** explained why content mappers don't fit their architecture and stated the need for a way to push in-memory .ngtypecheck.ts files into TS-Go's VFS
 * [today](https://github.com/microsoft/TypeScript/issues/64611#issuecomment-6026208957) **weswigham** suggested inverting control by using the TypeScript content mapper API directly to let the TS LSP apply mappings and diagnostics, and noted that content mappers can already register for .ng.ts files
 * [today](https://github.com/microsoft/TypeScript/issues/64611#issuecomment-6026534239) **atscott** explained that TS LSP span mapping couldn't directly serve Angular template features due to non-1:1 mappings and multi-hop queries, noted tsgo --api lacks needed language service requests, and mentioned that while the workaround works it's a nice-to-have feature
 * [today](https://github.com/microsoft/TypeScript/issues/64611#issuecomment-6027132277) **weswigham** noted that tsgo --api lacked certain language service requests (hover, definition, rename, references) and offered to prioritize exposing the missing TS6 backing APIs if provided a list, mentioning that @iisaduan is working on an API diff
 * [today](https://github.com/microsoft/TypeScript/issues/64611#issuecomment-6027930040) **atscott** identified gaps in the API surface, listing missing LSP handlers in Project.languageService and required snapshot persistence enhancements
 * [later](https://github.com/microsoft/TypeScript/issues/64611#issuecomment-6037027784) **Lojhan** asked whether content mapping was the intended way or if another API was planned to make transformed source available to the shared TS language server for SQL tagged templates in .ts/.tsx files

### [Issue microsoft/TypeScript#64614](https://github.com/microsoft/TypeScript/issues/64614) (Open, `Bug`, **weswigham**)

**TS 7 declaration emit writes unbound type parameters \(TOutputOut, $Output\) into \.d\.ts where 6\.0 emits any**

*TypeScript 7 declaration emit leaks TOutputOut and $Output into .d.ts instead of using any*

 * created by **nextor2k**
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/64614#issuecomment-5968338199) **Andarist** observed that emitting `any` was not expected behavior and that the declaration emitter should error, but the error was accidentally suppressed in TS6
 * (today) **RyanCavanaugh** added label `Bug`, set milestone to `TypeScript 7.1.1 RC`, and assigned to **weswigham**

### [PR microsoft/TypeScript#64617](https://github.com/microsoft/TypeScript/pull/64617) (Closed, `For Uncommitted Bug`)

**Handle JSDocParameterTag in ast\.GetTypeAnnotationNode**

*Include handling for JSDocParameterTag in ast.GetTypeAnnotationNode to ensure consistency with Node.Type*

 * created by **auvred**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/64617#issuecomment-5967118139) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#64618](https://github.com/microsoft/TypeScript/issues/64618) (Open, `Bug`, **RyanCavanaugh**)

**Non\-enum CLI options with multiple values separated by comma and space aren't whitespace trimmed**

*Comma-separated non-enum TypeScript CLI options retain leading whitespace instead of trimming values.*

 * created by **auvred**
 * (today) **RyanCavanaugh** added label `Bug`, set milestone to `TypeScript 7.1.1 RC`, and assigned to **RyanCavanaugh**

### [PR microsoft/TypeScript#64619](https://github.com/microsoft/TypeScript/pull/64619) (Open, `For Milestone Bug`, **RyanCavanaugh**)

**Trim whitespaces in comma\+space separated string\-list CLI option values**

*Trim whitespace around comma-and-space-separated string-list CLI option values to match TypeScript parser behavior.*

 * created by **auvred**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (today) **typescript-automation[bot]** added label `For Milestone Bug`, removed label `For Uncommitted Bug`, and assigned to **RyanCavanaugh**

### [Issue microsoft/TypeScript#64622](https://github.com/microsoft/TypeScript/issues/64622) (Open, `Bug`, **iisaduan**)

**\[ServerErrors\]\[JavaScript\] main vs **

*The main JavaScript server pipeline analyzed 300 popular TypeScript repos, reporting four interesting changes among 205 successes and various failures.*

 * [3 days ago](https://github.com/microsoft/TypeScript/issues/64622#issuecomment-5972854026) **typescript-automation[bot]** reported a server connection closed prematurely error for gchq/CyberChef and provided error details, last requests, and repro steps
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/64622#issuecomment-5972854485) **typescript-automation[bot]** reported a panic in textDocument/formatting due to a debug failure and included a stack trace
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/64622#issuecomment-5972854878) **typescript-automation[bot]** reported panic handling request for textDocument/diagnostic with stack trace and affected repo details
 * (today) **RyanCavanaugh** added label `Bug`, set milestone to `TypeScript 7.1.1 RC`, and assigned to **iisaduan**

### [Issue microsoft/TypeScript#64623](https://github.com/microsoft/TypeScript/issues/64623) (Open, `Bug`, **iisaduan**)

**\[ServerErrors\]\[TypeScript\] main vs **

*The TypeScript main branch pipeline analyzing 300 popular GitHub repositories encountered server errors, timeouts, and multiple clone failures.*

 * [3 days ago](https://github.com/microsoft/TypeScript/issues/64623#issuecomment-5973552095) **typescript-automation[bot]** reported a panic error due to invalid memory address or nil pointer dereference in the workspace/symbol handler
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/64623#issuecomment-5973552498) **typescript-automation[bot]** reported a premature server connection closure with undefined error for openclaw/openclaw, including error artifacts, recent requests, and repro steps
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/64623#issuecomment-5973552907) **typescript-automation[bot]** reported a panic handling request textDocument/diagnostic for withastro/astro due to flaky diagnostics
 * (today) **RyanCavanaugh** added label `Bug`, set milestone to `TypeScript 7.1.1 RC`, and assigned to **iisaduan**

### [Issue microsoft/TypeScript#64625](https://github.com/microsoft/TypeScript/issues/64625) (Closed, `Possible Improvement`, **weswigham**)

**Declaration emit re\-walks a package\.json \`exports\` map for every declaration \(module specifier cache not shared across node builders\)**

*Declaration emit repeatedly walks the package.json exports map for each declaration, causing significant performance regressions.*

 * (yesterday) **weswigham** added label `Possible Improvement`, and assigned to **weswigham**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/64625#issuecomment-5999865209) **weswigham** said "I've been meaning to get back to this architectural TODO for a bit - I'll clean it up, since someone actually came forward with a project it has outsized impact for."
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript#64626](https://github.com/microsoft/TypeScript/pull/64626) (Open, `For Backlog Bug`)

**Fix stripInternal handling of unrelated leading comments**

*Update stripInternal to check a declaration’s actual JSDoc tags for @internal instead of arbitrary leading comments to avoid unintended removals.*

 * created by **splincode**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/64626#issuecomment-5983058913) **splincode** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript/pull/64626#issuecomment-6026608504) **jakebailey** said "Has anything changed in 2 years? https://github.com/microsoft/TypeScript/issues/57352#issuecomment-1936596153"
 * [today](https://github.com/microsoft/TypeScript/pull/64626#issuecomment-6031954122) **splincode** explained that the patch preserves explicit `@internal` annotations with regression tests, clarified the narrower behavior change for incidental mentions, and offered to add a release note if needed

### [Issue microsoft/TypeScript#64628](https://github.com/microsoft/TypeScript/issues/64628) (Open, `Bug`, **weswigham**)

**JSDoc \`@private\` / \`@protected\` are dropped in declaration emit for properties declared by constructor assignment**

*TypeScript 7.0.2 drops JSDoc @private/@protected visibility and types for constructor-assigned properties in declaration files.*

 * created by **tlouisse**
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/64628#issuecomment-5989252127) **belentani7** described a declaration emit bug where JSDoc visibility annotations on constructor parameter properties are lost in .d.ts, detailed impact, example, expected output, fix location, and workaround, and asked if they should investigate the compiler code path
 * [yesterday](https://github.com/microsoft/TypeScript/issues/64628#issuecomment-5991294419) **tlouisse** said "Yes, it would be great if we can keep using this jsdoc annotation without having to do workarounds"
 * (today) **RyanCavanaugh** added label `Bug`, set milestone to `TypeScript 7.1.1 RC`, and assigned to **weswigham**

### [Issue microsoft/TypeScript#64629](https://github.com/microsoft/TypeScript/issues/64629) (Closed, `Bug`, **andrewbranch**)

**\[api\] createPrograms with a non\-composite projectReferences entry crashes the API server**

*Using createPrograms with a non-composite project reference crashes the TypeScript API server due to a nil pointer dereference*

 * created by **cplieger**
 * (today) **RyanCavanaugh** added label `Bug`, set milestone to `TypeScript 7.1.1 RC`, and assigned to **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript#64630](https://github.com/microsoft/TypeScript/issues/64630) (Closed, `Bug`, **andrewbranch**)

**\[api\] Static and callback module resolutions drop resolvedUsingTsExtension, raising TS2876**

*Static and callback module resolutions drop the resolvedUsingTsExtension flag, resulting in TS2876 errors when using TypeScript’s API.*

 * created by **cplieger**
 * (today) **RyanCavanaugh** added label `Bug`, set milestone to `TypeScript 7.1.1 RC`, and assigned to **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript#64631](https://github.com/microsoft/TypeScript/issues/64631) (Open, `Bug`, **andrewbranch**)

**\[api\] A nested request from a resolveModuleName callback gets another request's answer**

*Nested module resolution requests within a resolveModuleName callback sometimes return other requests’ results, causing incorrect resolutions.*

 * created by **cplieger**
 * (today) **RyanCavanaugh** added label `Bug`, and assigned to **andrewbranch**

### [PR microsoft/TypeScript#64633](https://github.com/microsoft/TypeScript/pull/64633) (Closed, `For Uncommitted Bug`)

**Fix crash in decorator metadata emit for decorated object literal members**

*Fixes a crash in TypeScript’s decorator metadata emission for decorated object literal members.*

 * created by **Andarist**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64633#issuecomment-5990767313) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#64634](https://github.com/microsoft/TypeScript/issues/64634) (Open, `Needs Investigation`, **iisaduan**)

**\[api\] Add \`parseConfigFileTextToJson\(\)\` helper**

*Add a parseConfigFileTextToJson() helper to enable consistent diagnostics when parsing JSON config strings.*

 * created by **mrazauskas**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **iisaduan**

### [Issue microsoft/TypeScript#64635](https://github.com/microsoft/TypeScript/issues/64635) (Open, `Needs Investigation`, **andrewbranch**)

**API server reports TS2345 for a call that tsc accepts on the same project**

*TypeScript’s language server API intermittently reports TS2345 for fitViewportToNodes calls despite tsc compiling the same project without errors.*

 * created by **vivere-dally**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.1.1 RC`, and assigned to **andrewbranch**

### [PR microsoft/TypeScript#64636](https://github.com/microsoft/TypeScript/pull/64636) (Closed, `For Uncommitted Bug`)

**Fix flaky diagnostic added by emit for \`typeof import\(\)\` type qualifiers**

*Resolve flaky diagnostics during emit for typeof import() type qualifiers.*

 * created by **Andarist**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64636#issuecomment-5992621711) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64637](https://github.com/microsoft/TypeScript/pull/64637) (Closed, `For Milestone Bug`, **andrewbranch**)

**\[api\] Report project reference diagnostics on programs without a config file**

*Prevent API server crashes by handling project reference diagnostics on programs lacking a configuration file*

 * created by **cplieger**
 * (yesterday) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * (today) **typescript-automation[bot]** added label `For Milestone Bug`, removed label `For Uncommitted Bug`, and assigned to **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#64638](https://github.com/microsoft/TypeScript/pull/64638) (Closed, `For Milestone Bug`, **andrewbranch**)

**\[api\] Skip disk\-layout import diagnostics for customized module resolutions**

*Skip disk-layout import diagnostics (such as TS2876) for customized module resolutions by adding an internal IsCustomResolution flag.*

 * created by **cplieger**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64638#issuecomment-6022411761) **cplieger** reworked the PR to remove the field, added an internal IsCustomResolution flag to ResolvedModule, and updated the checker to skip the ResolvedUsingTsExtension block when the flag is set
 * [today](https://github.com/microsoft/TypeScript/pull/64638#issuecomment-6026040596) **cplieger** explained that callback results were covered via callbackModuleResolver.resolveModuleName and staticModuleResolutionToResolvedModule, noted the test resolves './c.ts' and reports TS2876 on both imports on main, and mentioned moving the booleans together in ResolvedModule
 * (today) **typescript-automation[bot]** added label `For Milestone Bug`, removed label `For Uncommitted Bug`, and assigned to **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#64639](https://github.com/microsoft/TypeScript/pull/64639) (Open, `For Uncommitted Bug`, **andrewbranch**)

**\[api\] Answer nested requests on the sync connection in stack order**

*SyncConn.Call’s nested requests could interleave and receive incorrect responses, now fixed by enforcing stack-order handling.*

 * created by **cplieger**
 * (yesterday) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * **typescript-automation[bot]** assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript/pull/64639#issuecomment-6026775863) **jakebailey** said "Yeah, I blindly assigned this to you, but now that I look, I suspect there's a better design here"
 * [today](https://github.com/microsoft/TypeScript/pull/64639#issuecomment-6026835681) **andrewbranch** described having tried to block unrelated client callbacks until the request stack cleared, noted the difficulty distinguishing them from reentrant calls, and suggested context plumbing could work though complicated
 * [later](https://github.com/microsoft/TypeScript/pull/64639#issuecomment-6033522494) **cplieger** thanked reviewers and described the smaller version changes including reduced shape, context plumbing, use of sync.Cond, and notification handling

### [Issue microsoft/TypeScript#64641](https://github.com/microsoft/TypeScript/issues/64641) (Open, `Bug`, **andrewbranch**)

**\[api\] Let a program created with createPrograms use content mappers**

*Add an optional contentMappers option to CreateProgramOptions so createProgram-generated programs can apply configured content mappers.*

 * created by **cplieger**
 * (today) **RyanCavanaugh** added label `Bug`, and assigned to **andrewbranch**

### [PR microsoft/TypeScript#64642](https://github.com/microsoft/TypeScript/pull/64642) (Closed, `For Uncommitted Bug`)

**Fix \`workspace/symbol\` crash on an inferred project without a program**

*workspace/symbol requests crash on inferred TypeScript projects without an associated program.*

 * (yesterday) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64642#issuecomment-5995071174) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [today](https://github.com/microsoft/TypeScript/pull/64642#issuecomment-6027175861) **andrewbranch** asked whether the issue was with WithSnapshotLoadingProjectTree not updating the inferred project while the workspace symbol handler included it

### [PR microsoft/TypeScript#64649](https://github.com/microsoft/TypeScript/pull/64649) (Closed, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Cache one nodebuilder per emit resolver, make emit resolver emit context scoped**

*Cache one NodeBuilder per emit resolver and scope each emit resolver to its specific emit context.*

 * (yesterday) **typescript-automation[bot]** added labels `Author: Team`, `Author: Team`, `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64649#issuecomment-6022590447) **jakebailey** expressed liking the change while noting the double pointer looked odd and requested the bot to run tests
 * [today](https://github.com/microsoft/TypeScript/pull/64649#issuecomment-6022592749) **typescript-automation[bot]** reported CI jobs started and provided links to build results
 * [today](https://github.com/microsoft/TypeScript/pull/64649#issuecomment-6023027492) **typescript-automation[bot]** notified that the DT test results were ready and unchanged
 * [today](https://github.com/microsoft/TypeScript/pull/64649#issuecomment-6023098115) **typescript-automation[bot]** reported the performance run results in a detailed table
 * [today](https://github.com/microsoft/TypeScript/pull/64649#issuecomment-6023272670) **typescript-automation[bot]** reported tsc user test results and confirmed everything looked good
 * [today](https://github.com/microsoft/TypeScript/pull/64649#issuecomment-6024002969) **typescript-automation[bot]** reported that running the top 400 repos tsc comparison between baseline and pr succeeded without issues
 * (today) **weswigham** closed the issue

### [Issue microsoft/TypeScript#64650](https://github.com/microsoft/TypeScript/issues/64650) (Closed)

**Auto\-import should not offer a barrel to files inside same package**

*TypeScript auto-import offers barrel exports for internal package files, leading to accidental circular imports.*

 * created by **lonix1**
 * [today](https://github.com/microsoft/TypeScript/issues/64650#issuecomment-6026942010) **RyanCavanaugh** noted that this feature request duplicated issue #51418 and explained that autoImportFileExcludePatterns cannot distinguish importer-sensitive file exclusions
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#64651](https://github.com/microsoft/TypeScript/pull/64651) (Closed, `For Uncommitted Bug`)

**Fix crashes on malformed destructuring assignments during emit**

*Allow processing of malformed destructuring AST nodes by removing strict asserts to prevent emit crashes.*

 * (yesterday) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64651#issuecomment-6011076868) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [today](https://github.com/microsoft/TypeScript/pull/64651#issuecomment-6021288026) **jakebailey** asked if Strada had experienced this problem before or if it was new
 * [today](https://github.com/microsoft/TypeScript/pull/64651#issuecomment-6021855163) **Andarist** explained that Strada had the same assertions and crashes, showed where Strada expected a wider type but asserted a subtype, and noted that the Corsa PR loosens the asserts to match Strada's type allowances
 * [today](https://github.com/microsoft/TypeScript/pull/64651#issuecomment-6026169246) **jakebailey** said "I think this is probably fine but would like @weswigham to take a peek."

### [Issue microsoft/TypeScript#64653](https://github.com/microsoft/TypeScript/issues/64653) (Open, **DanielRosenwasser**, **Copilot**)

**Windows: module resolution fails for paths containing a \`con/\` directory segment \(reserved device name\)**

*TypeScript native on Windows cannot resolve imports from a directory named con, resulting in TS2307 errors after upgrading beyond 6.0.3.*

 * created by **itrapashko**
 * (today) **DanielRosenwasser** assigned to **Copilot**, **DanielRosenwasser**

### [PR microsoft/TypeScript#64654](https://github.com/microsoft/TypeScript/pull/64654) (Open, `For Uncommitted Bug`, **ahejlsberg**)

**check the target of a type reference in isWeakType**

*Modify isWeakType to check the target of type references instead of instantiating generic members, reducing memory usage by 19%.*

 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64654#issuecomment-6017564102) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * **jakebailey** assigned to **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript/pull/64654#issuecomment-6021091959) **jakebailey** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/64654#issuecomment-6021093507) **typescript-automation[bot]** posted build status updates for various CI jobs
 * [today](https://github.com/microsoft/TypeScript/pull/64654#issuecomment-6021352567) **typescript-automation[bot]** notified @jakebailey that the DT test run failed and provided a link to the logs
 * [today](https://github.com/microsoft/TypeScript/pull/64654#issuecomment-6021565310) **typescript-automation[bot]** posted performance run results with a comparison report of baseline versus PR metrics
 * [today](https://github.com/microsoft/TypeScript/pull/64654#issuecomment-6021637755) **typescript-automation[bot]** reported tsc user test results and confirmed everything looked good
 * [today](https://github.com/microsoft/TypeScript/pull/64654#issuecomment-6022484982) **typescript-automation[bot]** reported that running the top 400 repos tsc comparison between baseline and pr succeeded without issues

### [Issue microsoft/TypeScript#64655](https://github.com/microsoft/TypeScript/issues/64655) (Open, `Bug`, **weswigham**)

**Hover ignores the JSDoc written on an \`import f = a\.f\` alias**

*Hover and completion info for import aliases incorrectly show the original declaration's JSDoc instead of the alias's own documentation.*

 * created by **patrickkettner**
 * (today) **RyanCavanaugh** added label `Bug`, set milestone to `TypeScript 7.1.1 RC`, and assigned to **weswigham**

### [Issue microsoft/TypeScript#64656](https://github.com/microsoft/TypeScript/issues/64656) (Open, `Needs Investigation`, **weswigham**)

**Declaration emit errors \(TS5088\) on anonymous cyclic types that 6\.0 elided to \`any\`**

*TypeScript 7’s declaration emitter now errors on anonymous cyclic types instead of eliding them to any, causing breaking changes.*

 * created by **ssalbdivad**
 * [today](https://github.com/microsoft/TypeScript/issues/64656#issuecomment-6020790499) **ssalbdivad** expressed hope that emitting the actual type using internal aliases like _Node would be possible
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.1.1 RC`, and assigned to **weswigham**

### [PR microsoft/TypeScript#64657](https://github.com/microsoft/TypeScript/pull/64657) (Open, `For Milestone Bug`, **weswigham**)

**Show the JSDoc written on an \`import x = a\.x\` alias in hover and completions**

*Enable display of alias-specific JSDoc comments on import aliases during hover and completions.*

 * created by **patrickkettner**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64657#issuecomment-6020915337) **patrickkettner** said "@microsoft-github-policy-service agree"
 * (today) **typescript-automation[bot]** added label `For Milestone Bug`, removed label `For Uncommitted Bug`, and assigned to **weswigham**

### [PR microsoft/TypeScript#64658](https://github.com/microsoft/TypeScript/pull/64658) (Open, `For Uncommitted Bug`, **DanielRosenwasser**, **Copilot**)

**Fix Windows module resolution for reserved path segments**

*Use extended path namespaces to prevent Windows reserved device names like con from blocking module resolution.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64658#issuecomment-6023711474) **Copilot** addressed the issue in commit be35d253, retained original fast paths, gated allocation-free component scan to reserved-name paths, and added zero-allocation coverage for the detector

### [PR microsoft/TypeScript#64659](https://github.com/microsoft/TypeScript/pull/64659) (Open, `For Uncommitted Bug`, **johnfav03**)

**Compute signatures of dependent files in parallel on incremental rebuilds**

*Split signature computation of dependent files into parallel tasks during incremental rebuilds, boosting multi-core performance.*

 * created by **resure**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64659#issuecomment-6025077510) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * **typescript-automation[bot]** assigned to **johnfav03**

### [PR microsoft/TypeScript#64660](https://github.com/microsoft/TypeScript/pull/64660) (Open, `For Backlog Bug`)

**fix: avoid stack overflow on yield in computed method name under contextual typing \(\#62941\)**

*Prevent stack overflow by skipping computed property names when resolving yields in generator method names under contextual typing.*

 * created by **Pitchfork-and-Torch**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64660#issuecomment-6026726718) **Pitchfork-and-Torch** accepted the three error baselines from the containing-function change and updated test error reports accordingly

### [Issue microsoft/TypeScript#64661](https://github.com/microsoft/TypeScript/issues/64661) (Open, `Bug`)

**Class names \`eval\` and \`arguments\` are not reported as invalid strict mode bindings**

*TypeScript fails to report errors for class names 'eval' or 'arguments' as invalid strict-mode bindings, causing runtime errors.*

 * created by **JLHwung**

### [PR microsoft/TypeScript#64662](https://github.com/microsoft/TypeScript/pull/64662) (Open, `Author: Team`, `For Backlog Bug`, **jakebailey**)

**Unify recursive type naming during serialization**

*Unify recursive type naming in serialization by replacing existing recursion trackers with a single approach for name reuse.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Backlog Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/64662#issuecomment-6027174391) **jakebailey** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/64662#issuecomment-6027175567) **typescript-automation[bot]** reported CI build jobs starting and linked to their results for test top400, user test this, run dt, and perf test this faster
 * [today](https://github.com/microsoft/TypeScript/pull/64662#issuecomment-6027452310) **typescript-automation[bot]** reported that the DT test results were ready and unchanged
 * [today](https://github.com/microsoft/TypeScript/pull/64662#issuecomment-6027544711) **typescript-automation[bot]** reported performance run results
 * [today](https://github.com/microsoft/TypeScript/pull/64662#issuecomment-6027595319) **typescript-automation[bot]** reported test results comparing baseline and pr and flagged new type errors in bluebird tests
 * [today](https://github.com/microsoft/TypeScript/pull/64662#issuecomment-6028108984) **typescript-automation[bot]** reported that running the top 400 repos tsc comparison between baseline and pr succeeded without issues

### [PR microsoft/TypeScript#64663](https://github.com/microsoft/TypeScript/pull/64663) (Open, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**, **jakebailey**)

**\[api\] Preserve synchronous IPC exchange order, off\-goroutine**

*Implement off-goroutine IPC request handlers that send callbacks via the message loop to maintain synchronous exchange order.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**, **andrewbranch**

### [PR microsoft/TypeScript#64664](https://github.com/microsoft/TypeScript/pull/64664) (Open, `For Uncommitted Bug`)

**Update localization files**

*Update localization files and regenerate corresponding runtime artifacts.*

 * created by **typescript-automation[bot]**
 * (later) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`

### [Issue microsoft/TypeScript#64665](https://github.com/microsoft/TypeScript/issues/64665) (Closed, `Bug`)

**panic: Debug failure\. False expression: Undeclared private name for property declaration\.**

*Nightly TypeScript panics 'Undeclared private name for property declaration' when compiling a decorated class defining static and instance #a methods.*

 * created by **YuanchengJiang**

### [Issue microsoft/TypeScript#64666](https://github.com/microsoft/TypeScript/issues/64666) (Open, `Bug`)

**panic: Diagnostic emitted without context**

*TypeScript nightly compiler panics with "Diagnostic emitted without context" when generating declarations for an interface extending a labeled interface.*

 * created by **YuanchengJiang**

### [Issue microsoft/TypeScript#64667](https://github.com/microsoft/TypeScript/issues/64667) (Open, `Bug`)

**runtime error: invalid memory address or nil pointer dereference**

*TypeScript compiler panics with a nil pointer dereference when emitting declaration files using --stripInternal on an internal type alias.*

 * created by **YuanchengJiang**

### [Issue microsoft/TypeScript#64668](https://github.com/microsoft/TypeScript/issues/64668) (Open, `Bug`)

**panic: Unhandled case in Node\.MemberList**

*TypeScript compiler panics with an unhandled Node.MemberList case when evaluating an enum member that references a class in a merged namespace.*

 * created by **YuanchengJiang**

### [Issue microsoft/TypeScript#64669](https://github.com/microsoft/TypeScript/issues/64669) (Open, `Bug`)

**runtime error: invalid memory address or nil pointer dereference in getMembersOfSymbol**

*Assigning a computed property to a function causes a nil pointer panic in getMembersOfSymbol during declaration-only emit.*

 * created by **YuanchengJiang**

### [PR microsoft/TypeScript#64670](https://github.com/microsoft/TypeScript/pull/64670) (Closed, `For Backlog Bug`)

**fix\(64665\): fix emit crash for duplicate private names in decorated classes**

*Fixes emit crash due to duplicate private names in decorated classes.*

 * created by **a-tarasyuk**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [PR microsoft/TypeScript#64671](https://github.com/microsoft/TypeScript/pull/64671) (Open, `For Uncommitted Bug`, **RyanCavanaugh**)

**Do not pad binding elements that the parameter's type already types**

*padObjectLiteralType now respects annotated or contextual parameter types for destructured elements, avoiding false TS7031 errors.*

 * created by **Konan69**
 * (later) **typescript-automation[bot]** added label `For Uncommitted Bug`, and assigned to **RyanCavanaugh**

