# Report for 2026-09-26 (Saturday, September 26th, 2026)

11 different users commented on 23 different issues.

## Recommended Actions

 * Response Recommended
    * @krutoo asked for documentation for the syntax in [microsoft/TypeScript#46135](https://github.com/microsoft/TypeScript/issues/46135#issuecomment-5855347964)
    * @nikelborm provided repro steps and repository in [microsoft/TypeScript#63819](https://github.com/microsoft/TypeScript/issues/63819#issuecomment-5851213246)
    * @im-alok74 asked if the team would consider a new access modifier, whether discussion should be consolidated on issue #5228, and if there's a design doc or precedent to follow in [microsoft/TypeScript#64478](https://github.com/microsoft/TypeScript/issues/64478#issuecomment-5856146747)

## Activity Summary

### [Issue microsoft/TypeScript#46135](https://github.com/microsoft/TypeScript/issues/46135) (Closed, `Suggestion`, `Awaiting More Feedback`, **gabritto**)

**Ambient Module Declarations for Import Attributes \(formerly known as Import Assertions\)**

*Enable ambient module declarations based on import attributes to provide type definitions for CSS modules and asset URL imports.*

 * (3 weeks ago) **gabritto** closed the issue
 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/46135#issuecomment-5498379097) **jonathantneal** said "Thank you so incredibly much, @gabritto . 🙏❤️"
 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/46135#issuecomment-5498844938) **RyanCavanaugh** stated that it will not be backported to 6.0
 * [later](https://github.com/microsoft/TypeScript/issues/46135#issuecomment-5855347964) **krutoo** said "Can someone share docs for this syntax?"

### [Issue microsoft/TypeScript#51376](https://github.com/microsoft/TypeScript/issues/51376) (Open, `Bug`, `Help Wanted`, `Domain: Related Error Spans`)

**Spread operator with wrong optional property raises error on incorrect source line**

*TypeScript misreports error location when spreading an object with an optional property into a stricter type*

 * (2 days ago) **RyanCavanaugh** removed labels `Needs More Info`, `Needs Human Review`
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/51376#issuecomment-5821544888) **RyanCavanaugh** provided a clearer repro example illustrating that the error span remained on the property instead of the spread and suggested highlighting the entire literal when a spread may contribute to the type
 * [later](https://github.com/microsoft/TypeScript/issues/51376#issuecomment-5856047355) **im-alok74** described the root cause and implemented a fix for issue #64480, tested both repros, and added regression tests

### [Issue microsoft/TypeScript#63807](https://github.com/microsoft/TypeScript/issues/63807) (Open, `Possible Improvement`)

**Proposal: Flatten the AST to speed up tsgo**

*Proposes flattening tsgo’s AST into a flat array to reduce garbage collection scanning overhead and improve performance.*

 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63807#issuecomment-5826174145) **no-yan** reported migrating TypeScript's AST to a store-based representation, highlighted performance improvements, and solicited feedback on the design
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63807#issuecomment-5840843205) **RyanCavanaugh** observed that parsing is trivially parallelizable but overall pipeline performance gains require refactoring the checker due to increased memory traffic and potential Store+index bugs
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63807#issuecomment-5841085160) **andrewbranch** mentioned that the binary format resembles the API’s AST encoder output, expressed regret about not parsing directly into a buffer for zero-copy NAPI usage, and suggested the proposal is almost sufficient to share storage with a JS client
 * [later](https://github.com/microsoft/TypeScript/issues/63807#issuecomment-5853880206) **no-yan** thanked maintainers and said they would measure cross-file traversal performance, assess resource impact, and decide on pursuing the Checker migration direction

### [Issue microsoft/TypeScript#63819](https://github.com/microsoft/TypeScript/issues/63819) (Open, `Needs Investigation`, **andrewbranch**)

**project reference resolution fails when workspace is opened through a symlinked root path**

*tsgo fails to resolve project references and reports TS2307 errors when the workspace root is opened via a symlink*

 * (20 weeks ago) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **andrewbranch**
 * [20 weeks ago](https://github.com/microsoft/TypeScript/issues/63819#issuecomment-5351503368) **andrewbranch** said "N.B. the error occurs both in Corsa and in Strada. The fix looks behaviorally correct but I need to check performance impact."
 * [today](https://github.com/microsoft/TypeScript/issues/63819#issuecomment-5851213246) **nikelborm** described facing the same TS2367 error when using symlinked directories and provided a reproduction repository with steps

### [PR microsoft/TypeScript#64466](https://github.com/microsoft/TypeScript/pull/64466) (Open, `For Uncommitted Bug`)

**Fix language server retaining pre\-edit program and its checkers after program clone**

*Prevent TypeScript language server cloned programs from retaining previous program checker pools to reduce memory leaks.*

 * created by **ghost2023**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64466#issuecomment-5846290311) **ghost2023** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript/pull/64466#issuecomment-5850307599) **jakebailey** said "I think there's actually another one of these in ReuseProgram via processedFiles."

### [PR microsoft/TypeScript#64470](https://github.com/microsoft/TypeScript/pull/64470) (Closed, `For Uncommitted Bug`)

**Fixed a crash on JSX emit trying to emit unexpectedly recovered \`BinaryExpression\` in a JSX attribute**

*Fixed crash during JSX emission when an unexpectedly recovered binary expression appears in a JSX attribute.*

 * created by **Andarist**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64470#issuecomment-5848348825) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."

### [PR microsoft/TypeScript#64471](https://github.com/microsoft/TypeScript/pull/64471) (Closed, `For Uncommitted Bug`)

**Fix crash in \`isolatedDeclarations\` on \`this\.x = …\` assignments**

*Fix a crash in the isolatedDeclarations stage caused by this.x assignment expressions.*

 * created by **Andarist**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64471#issuecomment-5848471053) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."

### [PR microsoft/TypeScript#64472](https://github.com/microsoft/TypeScript/pull/64472) (Open, `For Uncommitted Bug`)

**Fix crash on malformed object destructuring assignment in decorated class**

*Correct compiler crash caused by malformed object destructuring assignments within decorated classes.*

 * created by **Andarist**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64472#issuecomment-5849059261) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."

### [PR microsoft/TypeScript#64473](https://github.com/microsoft/TypeScript/pull/64473) (Open, `For Uncommitted Bug`)

**test\(tsc\): Symlinked projects or the ones with symlinked parents should work**

*Add a new failing test and vfstest patch to validate TypeScript compiler builds in projects with symlinked directories or parents.*

 * created by **nikelborm**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64473#issuecomment-5851202123) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."

### [Issue microsoft/TypeScript#64474](https://github.com/microsoft/TypeScript/issues/64474) (Closed, `Suggestion`, `Domain: Performance`, **ahejlsberg**)

**checker builds member tables and intersection props it never uses**

*The TypeScript checker’s eager member and intersection property instantiation causes high memory use and is optimized to build needed properties.*

 * created by **maschwenk**
 * [today](https://github.com/microsoft/TypeScript/issues/64474#issuecomment-5852758422) **maschwenk** described the benchmarking methodology and results comparing main and PR commits, including hardware specifications, commands, scenarios, replication details, performance and memory improvements, and a gist link

### [PR microsoft/TypeScript#64475](https://github.com/microsoft/TypeScript/pull/64475) (Open, `For Uncommitted Bug`, **ahejlsberg**)

**build member tables of instantiated classes/interfaces lazily**

*Build member tables for instantiated classes and interfaces lazily, instantiating only accessed members and reusing existing symbols.*

 * created by **maschwenk**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [PR microsoft/TypeScript#64476](https://github.com/microsoft/TypeScript/pull/64476) (Closed, `For Milestone Bug`, **ahejlsberg**)

**only build intersection props that can reduce it to never**

*Modify TypeScript’s intersection type reduction to skip creating properties that cannot reduce to never, reducing memory and improving performance.*

 * created by **maschwenk**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [Issue microsoft/TypeScript#64477](https://github.com/microsoft/TypeScript/issues/64477) (Open)

**TS6059 error count flakes between runs unless \-\-singleThreaded**

*TypeScript’s TS6059 error count fluctuates between parallel compilations but remains consistent when using --singleThreaded.*

 * created by **maschwenk**

### [Issue microsoft/TypeScript#64478](https://github.com/microsoft/TypeScript/issues/64478) (Open)

**An \`internal\` property modifier as an alternative to \`protected\`**

*Introduce an internal modifier that keeps properties visible in type definitions but accessible only within class methods.*

 * created by **denis-migdal**
 * [later](https://github.com/microsoft/TypeScript/issues/64478#issuecomment-5855231995) **MartinJohns** said "Duplicate of #5228."
 * [later](https://github.com/microsoft/TypeScript/issues/64478#issuecomment-5856146747) **im-alok74** asked if the TypeScript team would consider a new access modifier, whether discussion should be consolidated on the existing issue, and if there’s a design doc precedent for adding modifiers
 * [later](https://github.com/microsoft/TypeScript/issues/64478#issuecomment-5856323072) **denis-migdal** clarified that the issue was not a duplicate, explained the desired package visibility as public in declaration files, and suggested renaming ‘internal’ due to ambiguity
 * [later](https://github.com/microsoft/TypeScript/issues/64478#issuecomment-5856738197) **MartinJohns** apologized for the mistake and noted the issue was a duplicate of #37487
 * [later](https://github.com/microsoft/TypeScript/issues/64478#issuecomment-5857413979) **denis-migdal** explained that their suggestion provides a public-facing property that is inaccessible externally but writable internally to serve as an internal interface for helper functions, offering more flexibility and type safety than protected

### [PR microsoft/TypeScript#64479](https://github.com/microsoft/TypeScript/pull/64479) (Open, `For Uncommitted Bug`)

**Fix flaky diagnostic added by declaration emit for untyped module imports**

*Resolves crash caused by inconsistent diagnostic messages emitted during declaration file generation for untyped module imports.*

 * created by **Andarist**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/64479#issuecomment-5855046316) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."

### [PR microsoft/TypeScript#64480](https://github.com/microsoft/TypeScript/pull/64480) (Open, `For Backlog Bug`)

**Fix incorrect error location when a spread overrides an explicit property \(\#51376\)**

*Attribute type assignability errors to overriding spread expressions rather than the earlier explicit properties in object literals.*

 * created by **im-alok74**
 * (later) **typescript-automation[bot]** added labels `For Backlog Bug`, `For Backlog Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/64480#issuecomment-5856112934) **im-alok74** said "@microsoft-github-policy-service agree"

### [PR microsoft/TypeScript#64481](https://github.com/microsoft/TypeScript/pull/64481) (Closed, `Author: Team`, `For Backlog Bug`, **ahejlsberg**)

**Don't reduce intersections of mappings of the same object type**

*Prevent TypeScript from reducing intersections of homomorphic object mappings to enable recursive Zod schemas*

 * created by **ahejlsberg**
 * (later) **typescript-automation[bot]** added labels `Author: Team`, `For Backlog Bug`, and assigned to **ahejlsberg**
 * [later](https://github.com/microsoft/TypeScript/pull/64481#issuecomment-5857421924) **ahejlsberg** said "@typescript-bot test it"
 * [later](https://github.com/microsoft/TypeScript/pull/64481#issuecomment-5857422515) **typescript-automation[bot]** reported CI jobs starting and their status with result links

