# Report for 2026-08-26 (Wednesday, August 26th, 2026)

24 different users commented on 65 different issues.

## Recommended Actions

 * Response Recommended
    * @brammitch reported that the issue no longer occurs on newer versions and can be closed in [microsoft/TypeScript#63796](https://github.com/microsoft/TypeScript/issues/63796#issuecomment-5428278737)
    * @jjspace provided additional reproduction details and system monitor screenshot in [microsoft/TypeScript#63886](https://github.com/microsoft/TypeScript/issues/63886#issuecomment-5429016630)
    * @typescript-automation[bot] asked the author to resolve merge conflicts in [microsoft/TypeScript#63996](https://github.com/microsoft/TypeScript/pull/63996#issuecomment-5432481327)
    * @typescript-automation[bot] provided test results in [microsoft/TypeScript#63996](https://github.com/microsoft/TypeScript/pull/63996#issuecomment-5432488255)
    * @alexicum asked why auto-import suggestion differs between files and what part of the algorithm causes the difference in [microsoft/TypeScript#64029](https://github.com/microsoft/TypeScript/issues/64029#issuecomment-5431091407)
    * @alexicum provided repro steps and expected behavior for consistent import suggestions in [microsoft/TypeScript#64034](https://github.com/microsoft/TypeScript/issues/64034#issuecomment-5429857364)
    * @msab-john suggested investigating wgo interference causing unnecessary tsc events in [microsoft/TypeScript#64037](https://github.com/microsoft/TypeScript/issues/64037#issuecomment-5429241996)
    * @msab-john asked how to ignore .wasm files in the TypeScript configuration in [microsoft/TypeScript#64037](https://github.com/microsoft/TypeScript/issues/64037#issuecomment-5429326043)
    * @typescript-automation[bot] provided performance results as requested in [microsoft/TypeScript#64039](https://github.com/microsoft/TypeScript/pull/64039#issuecomment-5431205944)
    * @typescript-automation[bot] reported that all tests passed in [microsoft/TypeScript#64041](https://github.com/microsoft/TypeScript/pull/64041#issuecomment-5432871314)
    * @scs0209 asked if they could work on the issue in [microsoft/TypeScript#64050](https://github.com/microsoft/TypeScript/issues/64050#issuecomment-5434695975)

## Activity Summary

### [Issue microsoft/TypeScript#13797](https://github.com/microsoft/TypeScript/issues/13797) (Closed, `VS Code Tracked`, `Domain: JSDoc`, `Not a Defect`)

**JSDoc syntax highlight\. Not supported type '\.\.\.\*'**

*VSCode’s JSDoc syntax highlighting doesn’t recognize Google Closure-Type variadic syntax ‘...*’, leaving types and parameter names unhighlighted.*

 * (8.1 years ago) **mhegazy** set milestone to `Future`, and removed from milestone `TypeScript 3.0`
 * **sandersn** unassigned **sandersn**
 * [today](https://github.com/microsoft/TypeScript/issues/13797#issuecomment-5428529368) **RyanCavanaugh** clarified that TypeScript's JSDoc support uses TypeScript type syntax instead of Closure Compiler-specific grammar and provided an example using a call signature that works in TS 7.1.0-dev with allowJs and checkJs
 * **RyanCavanaugh** added label `Needs Human Review`

### [Issue microsoft/TypeScript#17552](https://github.com/microsoft/TypeScript/issues/17552) (Closed, `Bug`, `Domain: API`, `Domain: API: Transforms`, `Needs Human Review`)

**File altered by before transform does not remove new unused imports**

*The before-transform API in TypeScript fails to remove imports that become unused after code transformations.*

 * (8.1 years ago) **mhegazy** set milestone to `Future`, and removed from milestone `TypeScript 3.0`
 * **RyanCavanaugh** unassigned **rbuckton**
 * [today](https://github.com/microsoft/TypeScript/issues/17552#issuecomment-5430918411) **RyanCavanaugh** explained that import usage is determined during checking before `before` transformers run and that transformers must explicitly remove unused imports since automatic rechecking isn't supported
 * **RyanCavanaugh** added label `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#17588](https://github.com/microsoft/TypeScript/issues/17588) (Open, `Suggestion`, `In Discussion`)

**Allow object types to have property\-like associated types**

*Add property-like associated types to object types and interfaces in TypeScript with new syntax and semantics*

 * [5 years ago](https://github.com/microsoft/TypeScript/issues/17588#issuecomment-909576503) **mzhang28** said "Any alternative ways of achieving the same effect in Typescript today?"
 * [4.7 years ago](https://github.com/microsoft/TypeScript/issues/17588#issuecomment-978265331) **pakoito** described an alternative RPC implementation using TypeScript types and noted that increased complexity can cause parameters to be typed as never, requiring a @ts-expect-error
 * [3.4 years ago](https://github.com/microsoft/TypeScript/issues/17588#issuecomment-1465175607) **julienrf** described a DataHandler example and demonstrated a type-checking error when iterating over a heterogeneous array of handlers
 * [later](https://github.com/microsoft/TypeScript/issues/17588#issuecomment-5437525752) **irfanstract** proposed an alternative encoding for inner types by rewriting type prefix.Bar into InstanceType<typeof prefix.Bar$class> and provided example TypeScript code

### [Issue microsoft/TypeScript#202](https://github.com/microsoft/TypeScript/issues/202) (Open, `Suggestion`, `In Discussion`)

**Support some non\-structural \(nominal\) type matching**

*Introduce nominal typing in TypeScript to distinguish structurally identical types and prevent unintended type mixing.*

 * [1.2 years ago](https://github.com/microsoft/TypeScript/issues/202#issuecomment-2868870489) **emilioplatzer** shared a workaround with example repository and Playground link and explained a typing-by-example approach using string literal types
 * [13 weeks ago](https://github.com/microsoft/TypeScript/issues/202#issuecomment-4549960682) **bluepnume** described how they currently simulate opaque types with intersection types and custom tooling, illustrated how native opaque types and operator overloading would improve their workflow, linked to issue #42218, and expressed strong support
 * [13 weeks ago](https://github.com/microsoft/TypeScript/issues/202#issuecomment-4549960682) **bluepnume** described how they currently simulate opaque types with intersection types and custom tooling, illustrated how native opaque types and operator overloading would improve their workflow, linked to issue #42218, and expressed strong support
 * [today](https://github.com/microsoft/TypeScript/issues/202#issuecomment-5432665580) **irfanstract** proposed allowing interfaces to extend union types to create preserved nominal types and suggested introducing an `Opaque` marker type for distinct opaque types
 * [today](https://github.com/microsoft/TypeScript/issues/202#issuecomment-5432665580) **irfanstract** proposed allowing interfaces to extend union types to create preserved nominal types and suggested introducing an `Opaque` marker type for distinct opaque types

### [Issue microsoft/TypeScript#27014](https://github.com/microsoft/TypeScript/issues/27014) (Closed, `Bug`, `Domain: Conditional Types`, `Needs Human Review`)

**Problem with inference for this\['prop'\] with conditional types**

*TypeScript fails to infer Unwrap<this['prop']> for the set function inside a class method.*

 * (6.5 years ago) **RyanCavanaugh** set milestone to `Backlog`, removed from milestone `TypeScript 3.8.1`, and unassigned **weswigham**
 * [today](https://github.com/microsoft/TypeScript/issues/27014#issuecomment-5429734370) **RyanCavanaugh** explained that `this` is polymorphic in instance methods and illustrated with a `Bar extends Foo` example why generic indexed accesses must use `Unwrap<this["prop"]>`, noting TS2345 errors in different TypeScript versions
 * **RyanCavanaugh** added label `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#31296](https://github.com/microsoft/TypeScript/issues/31296) (Closed, `Suggestion`, `In Discussion`, `Domain: API`)

**API: expose isReadonlySymbol**

*Add an isReadonlySymbol method to TypeChecker to reliably detect if a property is readonly, including mapped types.*

 * [6.5 years ago](https://github.com/microsoft/TypeScript/issues/31296#issuecomment-580577037) **bradzacher** mentioned encountering the issue in typescript-eslint issue #514 and requested exposing isReadonlySymbol from the type checker
 * [3.4 years ago](https://github.com/microsoft/TypeScript/issues/31296#issuecomment-1497127114) **neelance** said "This would be useful for us as well."
 * [1.1 years ago](https://github.com/microsoft/TypeScript/issues/31296#issuecomment-2999895135) **dragomirtitian** mentioned writing a documentation system reliant on type information and asked for the ability to detect readonly status of mapped properties
 * (later) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript#33708](https://github.com/microsoft/TypeScript/issues/33708) (Closed, `Bug`, `Effort: Difficult`, `Domain: Comment Emit`, `Domain: Declaration Emit`)

**Remove useless \`@‍typedef\` comments in \`declaration\`**

*Remove redundant @typedef JSDoc comments in emitted declarations so only the type alias retains documentation.*

 * (6.5 years ago) **RyanCavanaugh** set milestone to `Backlog`, removed from milestone `TypeScript 3.8.1`, and unassigned **weswigham**
 * [today](https://github.com/microsoft/TypeScript/issues/33708#issuecomment-5429770685) **RyanCavanaugh** explained that comment emission is best-effort, referenced the FAQ entry, and advised using an emit tool for precise comment preservation
 * **RyanCavanaugh** added label `Needs Human Review`

### [Issue microsoft/TypeScript#35962](https://github.com/microsoft/TypeScript/issues/35962) (Open, `Bug`, `Help Wanted`, `Effort: Moderate`, `Domain: JavaScript`, `Needs Human Review`)

**No error for undeclared \#private property in \`\.js\` files**

*Undeclared private field usage (#prop) in .js files lacks error reporting outside of checkJs despite being a syntax error.*

 * (6.6 years ago) **sandersn** set milestone to `Backlog`, removed from milestone `TypeScript 3.8.1`, and unassigned **sandersn**
 * [today](https://github.com/microsoft/TypeScript/issues/35962#issuecomment-5429427187) **RyanCavanaugh** reported that TS 3.8.0-dev.20200108 accepted test.js without diagnostics but the current native compiler and typescript@next reported error TS1111
 * **RyanCavanaugh** added label `Needs Human Review`

### [Issue microsoft/TypeScript#37399](https://github.com/microsoft/TypeScript/issues/37399) (Closed, `Bug`, `Domain: JSDoc`, `Needs Human Review`)

**Unrecognised JSDoc Namepath**

*JSDoc typedefs using '~' namepaths are unrecognized in TypeScript, resulting in errors and any types.*

 * (6.4 years ago) **RyanCavanaugh** added labels `Bug`, `Domain: JSDoc`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/37399#issuecomment-5430119923) **RyanCavanaugh** noted that the issue was a duplicate of #22158, explained that `testFnB~arg` is a JSDoc namepath rather than a TypeScript qualified type name, and demonstrated that using `testFnB.arg` type-checks correctly with diagnostics reported in TS versions
 * **RyanCavanaugh** added label `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#59920](https://github.com/microsoft/TypeScript/issues/59920) (Open, `Bug`, `Domain: JavaScript`, **jakebailey**)

**function object parameter destructure field without default value will be ignored**

*After upgrading to TypeScript 5.6, function parameter destructuring with defaulted properties ignores non-default fields, causing unknown property errors.*

 * [1.9 years ago](https://github.com/microsoft/TypeScript/issues/59920#issuecomment-2374958699) **Andarist** assumed the mixed TS/JS codebase situation was valid and explained that the change caused a new error due to an inferred parameter type change
 * [1.9 years ago](https://github.com/microsoft/TypeScript/issues/59920#issuecomment-2379478733) **ahejlsberg** explained that the issue pertained to type inference from code with errors, noted the root cause was a longstanding difference between array and object destructuring defaults, and indicated no strong reason to change the behavior
 * **RyanCavanaugh** added label `Domain: JavaScript`
 * [today](https://github.com/microsoft/TypeScript/issues/59920#issuecomment-5432044798) **jakebailey** described attempting a Copilot-based fix but rejecting it for special-casing JS and opted to try Anders' suggestion instead

### [Issue microsoft/TypeScript#6285](https://github.com/microsoft/TypeScript/issues/6285) (Closed, `Bug`, `Domain: Decorators`, `Needs Human Review`)

**Reference to own class in static variable initialization to a decorated class references undecorated class instead of decorated class**

*A decorated class's static factory property still references the original class instead of the decorated class.*

 * [9.8 years ago](https://github.com/microsoft/TypeScript/issues/6285#issuecomment-256812375) **rbuckton** suggested two alternative code approaches using Object.defineProperty and a Wrapper decorator
 * **mhegazy** added label `Domain: Decorators`
 * **RyanCavanaugh** unassigned **rbuckton**
 * [today](https://github.com/microsoft/TypeScript/issues/6285#issuecomment-5431000956) **RyanCavanaugh** explained that under legacy experimentalDecorators static property initializers run before class decorators and suggested assigning static values after declaration and copying property descriptors to preserve lazy accessors
 * **RyanCavanaugh** added label `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63704](https://github.com/microsoft/TypeScript/issues/63704) (Open, `Suggestion`, `Committed`, `Domain: lib.d.ts`, `ES Next`, **DanielRosenwasser**)

**Add \`es2026\` as valid \`target\` and \`lib\`**

*Add es2026 support with Math.sumPrecise, Iterator.concat, JSON.rawJSON and stringify overloads, Error.isError, default-valued Map/WeakMap methods, Uint8Array hex/base64 methods, and Array.fromAsync.*

 * (3 weeks ago) **DanielRosenwasser** added labels `Committed`, `Domain: lib.d.ts`, `ES Next`
 * [today](https://github.com/microsoft/TypeScript/issues/63704#issuecomment-5432318279) **DanielRosenwasser** said "If we merge https://github.com/microsoft/TypeScript/pull/63429 in first, we'll need to move that into es2026 as well."

### [Issue microsoft/TypeScript#63708](https://github.com/microsoft/TypeScript/issues/63708) (Open, `Possible Improvement`, **ahejlsberg**)

**It is possible to violate generic constraints when distributing union types**

*Distributive union types in TypeScript can bypass generic constraints, allowing invalid B extends A combinations without error.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/63708#issuecomment-5166870235) **snarbles2** asked whether it validated `Show` constraints based on the original types for `A` and `B` and then performed substitution based on the distributed constituents
 * (3 weeks ago) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **ahejlsberg**
 * [later](https://github.com/microsoft/TypeScript/issues/63708#issuecomment-5440619666) **ahejlsberg** explained that conditional types infer `A extends B` in the true branch but cannot express or infer the opposite constraint in the false branch, making this lack of negated types a design limitation
 * (later) **ahejlsberg** added label `Design Limitation`, and removed label `Needs Investigation`

### [Issue microsoft/TypeScript#63754](https://github.com/microsoft/TypeScript/issues/63754) (Open, `Bug`)

**Diagnostic code 8030 being incorrectly generated using JSDoc \`@type\` on a function\.**

*TypeScript 7.0.2's JSDoc @type on a function wrongly triggers diagnostic 8030 by appending '| undefined' to the referenced interface method type.*

 * **typescript-automation[bot]** added label `Fix Available`
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/63754#issuecomment-5331383884) **RyanCavanaugh** demonstrated that the single-file repro worked and recommended removing null/undefined then contextually typing to avoid an implicit any on `s`
 * **jakebailey** removed label `Fix Available`
 * [later](https://github.com/microsoft/TypeScript/issues/63754#issuecomment-5438605277) **jyx-07** opened PR #64052, diagnosed the root cause as union types leaking into signature lookup helpers, applied removeMissingOrUndefinedType at the affected call sites in checker.go, and verified that the original repro now yields no errors while genuine arity mismatches still report correctly

### [Issue microsoft/TypeScript#63789](https://github.com/microsoft/TypeScript/issues/63789) (Open, `Suggestion`)

**Inherited methods not merging JSDoc comments**

*In tsgo overridden methods with @remarks tags lose inherited JSDoc comments rather than merging them from the base class.*

 * [37 weeks ago](https://github.com/microsoft/TypeScript/issues/63789#issuecomment-5351499999) **jakebailey** said "FWIW there is a PR for this in microsoft/typescript-go#2262. @LukeAbby does it do what you expect?"
 * [37 weeks ago](https://github.com/microsoft/TypeScript/issues/63789#issuecomment-5351500032) **LukeAbby** indicated that the PR didn't fully work due to literal JSDoc concatenation and suggested restoring old behavior or adding an opt-in for merging docs with @inheritDoc
 * [36 weeks ago](https://github.com/microsoft/TypeScript/issues/63789#issuecomment-5351500059) **a-tarasyuk** provided a test case and sample QuickInfo output demonstrating JSDoc inheritDocTag behavior
 * **RyanCavanaugh** added label `Suggestion`

### [Issue microsoft/TypeScript#63796](https://github.com/microsoft/TypeScript/issues/63796) (Closed, `Needs More Info`)

**Client typescript\.native\-preview\-lsp: connection to server is erroring**

*TypeScript Native Preview fails to start in an air-gapped Windows Server to RHEL environment, reporting write EPIPE and execution errors.*

 * created by **brammitch**
 * [today](https://github.com/microsoft/TypeScript/issues/63796#issuecomment-5427933022) **RyanCavanaugh** said "I'm not really clear on what SSHing into an air-gapped machine means. Can you clarify the setup here, and check again on the latest build?"
 * **RyanCavanaugh** added label `Needs More Info`
 * [today](https://github.com/microsoft/TypeScript/issues/63796#issuecomment-5428278737) **brammitch** said "This issue is no longer occurring on newer versions, and can be closed."
 * (today) **brammitch** closed the issue

### [Issue microsoft/TypeScript#63802](https://github.com/microsoft/TypeScript/issues/63802) (Closed)

**TS4053 happens when public class method adopts imported type from library**

*Public methods in an exported class using an imported library type cause TS4053 errors with tsgo.*

 * [22 weeks ago](https://github.com/microsoft/TypeScript/issues/63802#issuecomment-5351501466) **hkleungai** stated that the bug may be new or a rediscovery in TypeScript and offered to open an issue in the TypeScript repo if needed
 * (20 weeks ago) **RyanCavanaugh** unassigned **jakebailey**, **Copilot**
 * [today](https://github.com/microsoft/TypeScript/issues/63802#issuecomment-5427821889) **RyanCavanaugh** said "The latest comment doesn't seem like a bug -- if the .d.ts would need to name a type that's not exported from the other module, well, it can't. Please log a new report with clearer expected output."
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63823](https://github.com/microsoft/TypeScript/issues/63823) (Closed, `Possible Improvement`, **jakebailey**)

**\[lsp\] make source action kinds more specific**

*Advertise more specific LSP code action kinds with .ts suffixes to enable TypeScript-specific on-save actions without affecting other servers.*

 * [6 days ago](https://github.com/microsoft/TypeScript/issues/63823#issuecomment-5359778836) **TorinAsakura** requested agreement on .ts handling before opening a new PR
 * **jakebailey** assigned to **jakebailey**
 * [6 days ago](https://github.com/microsoft/TypeScript/issues/63823#issuecomment-5365807837) **rchl** suggested using tsgo suffix for code actions, then reconsidered and proposed ts or typescript might be more appropriate
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#63827](https://github.com/microsoft/TypeScript/issues/63827) (Closed, `Needs More Info`, **andrewbranch**)

**LSP custom/initializeAPISession never responds in stdio mode \(7\.0\.0\-dev\.20260518\.1 / 20260522\.1\)**

*Calling custom/initializeAPISession in tsgo’s stdio LSP mode hangs without JSON-RPC response or socket creation*

 * created by **re-thc**
 * (13 weeks ago) **re-thc** closed the issue
 * (13 weeks ago) **re-thc** reopened the issue
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript/issues/63827#issuecomment-5429278496) **andrewbranch** asked re-thc to test reproduction on the latest nightlies and provide environment details or a self-contained repro
 * (today) **andrewbranch** added label `Needs More Info`, and removed label `Needs Investigation`

### [Issue microsoft/TypeScript#63828](https://github.com/microsoft/TypeScript/issues/63828) (Closed, `API Request`, **andrewbranch**)

**Add API to detect wherever a symbol is readonly**

*Add APIs to TypeScript's type checker for detecting whether a symbol is readonly or optional.*

 * created by **mrazauskas**
 * (5 days ago) **RyanCavanaugh** added label `API Request`, and assigned to **andrewbranch**
 * (later) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript#63849](https://github.com/microsoft/TypeScript/issues/63849) (Closed)

**Bug Report: Severe memory leak triggered by "TypeScript \(Native Preview\)" extension**

*Enabling the TypeScript Native Preview extension in an empty folder without package.json causes a persistent memory leak until VS Code is closed.*

 * [6 weeks ago](https://github.com/microsoft/TypeScript/issues/63849#issuecomment-5351506856) **Skykill** noted that the issue reproduced with a minimal two-line file unaffected by the npm init workaround, filed a separate issue with repro and analysis in microsoft/typescript-go#4612, and cross-linked them for triage due to a potential common checker explosion on intersections containing unions
 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/63849#issuecomment-5351506888) **talkstream** provided an additional data point for the memory leak issue, including environment details and OS-level snapshot measurements showing a tsgo process growing from 163 MB to over 3 GB across five days
 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/63849#issuecomment-5351506916) **jakebailey** explained that the @typescript/native-preview channel stopped publishing since TypeScript 7 GA shipping, noted that nightlies moved to the main typescript package, and advised capturing a heap profile via VS Code’s command palette for leaking processes
 * [today](https://github.com/microsoft/TypeScript/issues/63849#issuecomment-5428004395) **RyanCavanaugh** said "We've fixed a bunch of things since this was reported and many of the comments here seem to be unrelated reports - please log fresh issues on the latest build with specific repros. Thanks!"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63875](https://github.com/microsoft/TypeScript/issues/63875) (Open, `Suggestion`, `Committed`, **andrewbranch**)

**API feature roadmap**

*API feature roadmap for TypeScript 7.1 outlining plugin replacements and top-level utilities with rough cost estimates.*

 * (6 days ago) **RyanCavanaugh** added label `Committed`, and assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript/issues/63875#issuecomment-5427611518) **remojansen** asked for advice on the intended TypeScript 7 extension point for injecting type-derived AST nodes into existing source files
 * [today](https://github.com/microsoft/TypeScript/issues/63875#issuecomment-5429685565) **andrewbranch** explained that the necessary APIs already exist and detailed how to load the program, use AST, symbol, and checker APIs, modify files, and update snapshots, noting that content mappers are supported but recommending using APIs to build a custom CLI
 * [later](https://github.com/microsoft/TypeScript/issues/63875#issuecomment-5437239627) **remojansen** thanked andrewbranch and reported initial PoC progress for ahead-of-time reflect metadata in TypeScript 7, injecting design:symbols and design:arguments at build time using types

### [Issue microsoft/TypeScript#63883](https://github.com/microsoft/TypeScript/issues/63883) (Closed, `Needs Investigation`, **andrewbranch**)

**Add API to get target symbol of instantiated symbol**

*Add a Symbol.getTarget method to expose the underlying target symbol of instantiated symbols*

 * (2 weeks ago) **RyanCavanaugh** added labels `Needs Investigation`, `Needs Investigation`, and set milestone to `TypeScript 7.1`
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript#63886](https://github.com/microsoft/TypeScript/issues/63886) (Open)

**Memory skyrockets with VSCode extension**

*Enabling the VSCode Typescript 7 extension with tsgo on a file using gulp-sass causes the TypeScript server to rapidly exhaust all system memory.*

 * created by **jjspace**
 * **RyanCavanaugh** added label `Needs More Info`
 * [today](https://github.com/microsoft/TypeScript/issues/63886#issuecomment-5427559355) **RyanCavanaugh** said "Can you try again with the latest build? I'm not seeing any memory rise at all when uncommenting"
 * [today](https://github.com/microsoft/TypeScript/issues/63886#issuecomment-5429016630) **jjspace** confirmed issue still occurred, observed that the extension consumed almost 10GB of memory before stabilizing, and provided version info and a system monitor screenshot
 * **RyanCavanaugh** removed label `Needs More Info`

### [PR microsoft/TypeScript#63943](https://github.com/microsoft/TypeScript/pull/63943) (Closed, `For Uncommitted Bug`, **andrewbranch**)

**\[api\] Add \`\.isReadonlySymbol\(\)\` method**

*Add a .isReadonlySymbol() method to the TypeScript checker API for identifying readonly symbols.*

 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [6 days ago](https://github.com/microsoft/TypeScript/pull/63943#issuecomment-5365861584) **typescript-automation[bot]** said "The TypeScript team hasn't accepted the linked issue #63828. If you can get it accepted, this PR will have a better chance of being reviewed."
 * **typescript-automation[bot]** assigned to **andrewbranch**
 * (later) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#63945](https://github.com/microsoft/TypeScript/pull/63945) (Closed, `For Milestone Bug`, **andrewbranch**)

**\[api\] Add \`\.getTargetSymbol\(\)\` method**

*Adds a getTargetSymbol method to the TypeScript compiler API checker to retrieve target symbols.*

 * created by **mrazauskas**
 * (5 days ago) **typescript-automation[bot]** added label `For Milestone Bug`, and assigned to **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript#63946](https://github.com/microsoft/TypeScript/issues/63946) (Closed, `Needs Investigation`, **andrewbranch**)

**LSP Panic: overlay not found for changed file**

*LSP panics with ‘overlay not found for changed file’ when editing WSL files in PhpStorm after upgrading to tsserver v7.*

 * **RyanCavanaugh** added label `Needs More Info`
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63946#issuecomment-5416871816) **RyanCavanaugh** said "That is not an LSP log. We need the commands the editor is sending to the LSP and what the responses were."
 * [today](https://github.com/microsoft/TypeScript/issues/63946#issuecomment-5422984942) **uncaught** apologized, mentioned activating trace logging, and provided a crash log snippet
 * (today) **RyanCavanaugh** added label `Needs Investigation`, removed label `Needs More Info`, assigned to **Copilot**, **RyanCavanaugh**, **andrewbranch**, and unassigned **RyanCavanaugh**, **Copilot**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#63951](https://github.com/microsoft/TypeScript/pull/63951) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Use "\.ts" suffixed code action kinds**

*Advertise .ts-suffixed code action kinds such as source.fixAll.ts and update tests to use them.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/63951#issuecomment-5417191833) **andrewbranch** said "Is this just an opaque identifier that is now less likely to collide with other providers, or does the name get parsed out and used by clients in some way?"
 * [yesterday](https://github.com/microsoft/TypeScript/pull/63951#issuecomment-5417361919) **jakebailey** explained that the .ts suffix allowed users to select only TypeScript fixes in the editor to avoid auto-applying all ESLint fixes
 * [yesterday](https://github.com/microsoft/TypeScript/pull/63951#issuecomment-5417367882) **jakebailey** suggested that content mappers were acceptable since mapping was a provider-specific detail and linters weren't relevant
 * (today) **jakebailey** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/63951#issuecomment-5432991541) **TorinAsakura** analyzed the merged diff and suggested normalizing requested code-action kinds at the API boundary to avoid leaking the .ts suffix into the language service

### [PR microsoft/TypeScript#63955](https://github.com/microsoft/TypeScript/pull/63955) (Closed, `For Uncommitted Bug`, **DanielRosenwasser**)

**Update README social links from Twitter to X**

*Replace two Twitter references in README.md with X to update the social links.*

 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [5 days ago](https://github.com/microsoft/TypeScript/pull/63955#issuecomment-5378282238) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * **typescript-automation[bot]** assigned to **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript/pull/63955#issuecomment-5428252596) **RyanCavanaugh** said "Linked issue is not approved for PR, please check CONTRIBUTING.md"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63958](https://github.com/microsoft/TypeScript/issues/63958) (Open, `Bug`)

**Declaration emit: JSDoc @typedef/@callback comments are separated from their synthesized type when preceded by another declaration**

*Declaration emit for JS files misplaces JSDoc @typedef/@callback comments, detaching them from their synthesized types when preceded by another declaration.*

 * created by **Abdullah-Builds**
 * (today) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`

### [PR microsoft/TypeScript#63996](https://github.com/microsoft/TypeScript/pull/63996) (Closed, `For Backlog Bug`)

**Fix scanning issues related to Unicode escapes in RegExp group names and refactor identifier scanning**

*Refactor identifier scanning to correctly parse and normalize Unicode escapes and surrogate pairs in RegExp group names, preventing TS1514 errors.*

 * created by **graphemecluster**
 * [yesterday](https://github.com/microsoft/TypeScript/pull/63996#issuecomment-5407137733) **graphemecluster** said "All checks passed, so I am leaving the diff files here. If they are to be removed, feel free to do so on my behalf."
 * [yesterday](https://github.com/microsoft/TypeScript/pull/63996#issuecomment-5412038641) **jakebailey** said "We definitely don't want the diffs, we just don't have anything that checks for extra baselines (my mistake for not retaining that)"
 * [today](https://github.com/microsoft/TypeScript/pull/63996#issuecomment-5432057922) **jakebailey** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/63996#issuecomment-5432058459) **typescript-automation[bot]** reported CI build status updates for four commands
 * [today](https://github.com/microsoft/TypeScript/pull/63996#issuecomment-5432257259) **typescript-automation[bot]** reported test results showing two package install failures and one git clone failure, and confirmed everything else looked good
 * [today](https://github.com/microsoft/TypeScript/pull/63996#issuecomment-5432267358) **typescript-automation[bot]** provided the requested performance run results
 * [today](https://github.com/microsoft/TypeScript/pull/63996#issuecomment-5432345439) **jakebailey** said "There's an alloc regression here; I have a fix I could push to the PR if that's fine with you."
 * [today](https://github.com/microsoft/TypeScript/pull/63996#issuecomment-5432449695) **graphemecluster** said "Yes, I'm fine with it."
 * [today](https://github.com/microsoft/TypeScript/pull/63996#issuecomment-5432480953) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/63996#issuecomment-5432481327) **typescript-automation[bot]** said "Hey @jakebailey, this PR is in an unmergable state, so is missing a merge commit to run against; please resolve conflicts and try again."
 * [today](https://github.com/microsoft/TypeScript/pull/63996#issuecomment-5432488255) **typescript-automation[bot]** reported that running the top 400 repos with tsc comparing main and the pull request merge yielded everything looked good
 * [today](https://github.com/microsoft/TypeScript/pull/63996#issuecomment-5432498338) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/63996#issuecomment-5432498806) **typescript-automation[bot]** reported that performance test jobs started and provided links to build and results
 * [today](https://github.com/microsoft/TypeScript/pull/63996#issuecomment-5432686256) **typescript-automation[bot]** provided the results of the requested performance run

### [Issue microsoft/TypeScript#64012](https://github.com/microsoft/TypeScript/issues/64012) (Closed, `Bug`, **ahejlsberg**, **Copilot**)

**Stack overflow narrowing \`as const\` object assigned to loop variable it references**

*TypeScript 7.1.0-dev.20260724.1 crashes with a stack overflow when narrowing an ‘as const’ object referencing its loop variable.*

 * (yesterday) **RyanCavanaugh** added label `Bug`, assigned to **ahejlsberg**, and unassigned **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript/issues/64012#issuecomment-5429348316) **ahejlsberg** attributed the issue to a change to checkAssertion, noted that #64013 and #64018 only worked around it, and said they would submit a PR with the correct fix
 * **ahejlsberg** added to milestone `TypeScript 7.1`
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript#64018](https://github.com/microsoft/TypeScript/pull/64018) (Closed)

**Disable expression type caching in CFA for loops**

*Disable expression type caching during control flow analysis of loops to prevent infinite recursion.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/64018#issuecomment-5417919406) **ahejlsberg** said "@typescript-bot test top1000"
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64018#issuecomment-5417920096) **typescript-automation[bot]** reported that the test top1000 build started and provided status and result links
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64018#issuecomment-5418709492) **typescript-automation[bot]** provided results confirming that everything looked good when comparing tsc runs on the top 1000 repos between main and the PR merge
 * [today](https://github.com/microsoft/TypeScript/pull/64018#issuecomment-5428829565) **ahejlsberg** expressed doubt that the PR was the correct fix and mentioned researching the real cause of the infinite recursion
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript#64023](https://github.com/microsoft/TypeScript/pull/64023) (Closed)

**Additional generator\-based sync API methods**

*Add strongly-typed generator-based synchronous API methods to facilitate request batching parallel to the async API*

 * created by **weswigham**
 * [today](https://github.com/microsoft/TypeScript/pull/64023#issuecomment-5425234177) **dragomirtitian** shared a gist of their batching version, asked if composability functions like all and spawn are possible in this PR version, and mentioned potential open-sourcing
 * [today](https://github.com/microsoft/TypeScript/pull/64023#issuecomment-5428495821) **weswigham** described that api.batch is equivalent to runBatch, noted tests are missing and promised to add them along with a Promise.all helper
 * [today](https://github.com/microsoft/TypeScript/pull/64023#issuecomment-5429110699) **weswigham** extracted the 'all' equivalent helper from the generator-running logic and exported it in the sync API, tested user-composed generator functions, added batch-flattening to the 'all' batch request builder, and removed the API-level 'batchRequests' helper from API and moved it to Client

### [Issue microsoft/TypeScript#64025](https://github.com/microsoft/TypeScript/issues/64025) (Open, `Bug`, **jakebailey**, **Copilot**)

**\`\-\-incremental\`: diagnostics caused by a JSON module are never cleared after the JSON file is fixed \(7\.0\.2\)**

*TypeScript 7.0.2’s incremental mode with resolveJsonModule fails to clear stale JSON import diagnostics after fixing the JSON file, requiring tsbuildinfo deletion to recover.*

 * created by **jmelahman**
 * (yesterday) **jakebailey** assigned to **Copilot**, **jakebailey**
 * (today) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#64029](https://github.com/microsoft/TypeScript/issues/64029) (Closed, `Bug`, **andrewbranch**, **RyanCavanaugh**, **Copilot**)

**Auto\-import ignores barrel \(index\.ts\) when the imported folder name is a prefix of the importing file name**

*VSCode auto-import suggestions ignore barrel index.ts files when the imported folder name prefixes the importing file name.*

 * (today) **RyanCavanaugh** set milestone to `TypeScript 7.1`, and assigned to **Copilot**, **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript/issues/64029#issuecomment-5429021956) **andrewbranch** asked what was meant by ignoring barrel files in 6.0.3 and why barrel files should be prioritized over direct paths when equal length
 * (today) **andrewbranch** added label `Needs More Info`, and removed label `Bug`
 * [today](https://github.com/microsoft/TypeScript/issues/64029#issuecomment-5430672292) **alexicum** described import differences between barrel and direct paths in TypeScript and tsgo, explained how file name and folder ordering cause inconsistent auto-imports, and offered a mental model of index.ts as a module’s public interface
 * (today) **RyanCavanaugh** unassigned **RyanCavanaugh**, **iisaduan**, **Copilot**
 * [today](https://github.com/microsoft/TypeScript/issues/64029#issuecomment-5430781986) **RyanCavanaugh** argued that import resolution issues stem from differing filename conventions rather than mixed behavior and that no universal barrel preference exists
 * **RyanCavanaugh** removed from milestone `TypeScript 7.1`
 * [today](https://github.com/microsoft/TypeScript/issues/64029#issuecomment-5431091407) **alexicum** asked why the auto-import suggestion differed between two files and what part of the algorithm causes the difference

### [PR microsoft/TypeScript#64032](https://github.com/microsoft/TypeScript/pull/64032) (Closed, **andrewbranch**, **Copilot**)

**Fix accessing name on jsdoc link for invalid names**

*In TypeScript 7.0, accessing the name of a JSDoc link tag with an invalid identifier incorrectly returns a sibling node instead of undefined.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript/pull/64032#issuecomment-5431489667) **andrewbranch** said "@copilot what are you doing. no time to waste. hop to it please"

### [Issue microsoft/TypeScript#64033](https://github.com/microsoft/TypeScript/issues/64033) (Closed, `Not a Defect`)

**Type erasure changes directive\-prologue semantics after type\-only declarations**

*Erasing type-only declarations causes subsequent string expressions like use client to become directives rather than ordinary expression statements.*

 * created by **magic-akari**
 * [today](https://github.com/microsoft/TypeScript/issues/64033#issuecomment-5427649472) **RyanCavanaugh** reasoned that type declarations as comments wouldn't affect 'use strict' and demonstrated strict mode behavior
 * **RyanCavanaugh** added label `Not a Defect`
 * [today](https://github.com/microsoft/TypeScript/issues/64033#issuecomment-5427761663) **magic-akari** described that the current type-stripping transform outputs a directive prologue and with statement, stated intent to align the parser and transformer semantics to produce the correct output naturally, and noted implementation challenges with treating erasable syntax transparently due to parser directive detection
 * [today](https://github.com/microsoft/TypeScript/issues/64033#issuecomment-5427860970) **RyanCavanaugh** asked what the type-stripping transform is
 * [today](https://github.com/microsoft/TypeScript/issues/64033#issuecomment-5427887258) **magic-akari** clarified that they meant SWC’s type-strip implementation behavior and noted they were fixing it
 * [today](https://github.com/microsoft/TypeScript/issues/64033#issuecomment-5427987102) **magic-akari** listed three AST viewers and demonstrated that uncommenting the type declaration caused the directives field to become empty
 * [today](https://github.com/microsoft/TypeScript/issues/64033#issuecomment-5428599860) **magic-akari** found that TypeScript treats type alias declarations as statements terminating directive prologue, causing the current type-erasure output to emit an invalid 'use strict' directive
 * [today](https://github.com/microsoft/TypeScript/issues/64033#issuecomment-5428781626) **RyanCavanaugh** argued that automatically parenthesizing directives would be user-hostile and recommended updating the parser/binder to correctly skip type aliases instead of replicating other parsers' bugs

### [Issue microsoft/TypeScript#64034](https://github.com/microsoft/TypeScript/issues/64034) (Open, `Needs More Info`, **andrewbranch**, **RyanCavanaugh**, **Copilot**)

**Auto\-import prioritizes files alphabetically before index\.ts inside a folder, ignoring the barrel**

*VSCode’s TypeScript auto-import in version 7.0.2 prioritizes files by alphabetical order over index.ts barrels, leading to inconsistent import paths.*

 * created by **alexicum**
 * (today) **RyanCavanaugh** added label `Bug`, and assigned to **andrewbranch**, **Copilot**, **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript/issues/64034#issuecomment-5428917896) **andrewbranch** asked for more specific reproduction steps and clarification on expected versus actual behavior
 * (today) **andrewbranch** added label `Needs More Info`, and removed label `Bug`
 * [today](https://github.com/microsoft/TypeScript/issues/64034#issuecomment-5429857364) **alexicum** thanked the maintainer for clarification and provided repro steps along with expected behavior for consistent import suggestions

### [PR microsoft/TypeScript#64035](https://github.com/microsoft/TypeScript/pull/64035) (Open, `For Uncommitted Bug`, **RyanCavanaugh**, **Copilot**)

**Prefer index barrels for relative auto\-imports**

*Update TypeScript auto-import ranking to prefer index.ts barrel re-exports over direct files for relative modules.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**

### [PR microsoft/TypeScript#64036](https://github.com/microsoft/TypeScript/pull/64036) (Closed, **RyanCavanaugh**, **Copilot**)

**Prevent LSP panics on stale document notifications**

*Stale didClose and didChange LSP notifications for non-open documents are now ignored to prevent server panics.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript#64037](https://github.com/microsoft/TypeScript/issues/64037) (Open, `Needs More Info`)

**npx tsc \-w is triggering itself after each build**

*npx tsc --watch enters a build loop because output JavaScript files alongside TypeScript sources continuously retrigger compilation.*

 * created by **msab-john**
 * [today](https://github.com/microsoft/TypeScript/issues/64037#issuecomment-5429241996) **msab-john** discovered that wgo was triggering unnecessary tsc events and suggested investigating the interference
 * [today](https://github.com/microsoft/TypeScript/issues/64037#issuecomment-5429326043) **msab-john** questioned how to configure TypeScript to ignore .wasm files that trigger rebuilds due to wgo updates
 * **RyanCavanaugh** added label `Needs More Info`
 * [today](https://github.com/microsoft/TypeScript/issues/64037#issuecomment-5429365937) **RyanCavanaugh** said "We need a concrete repro in order to investigate"
 * [later](https://github.com/microsoft/TypeScript/issues/64037#issuecomment-5441005231) **msab-john** said "I'll see if I can make a small and simple one..."

### [Issue microsoft/TypeScript#64038](https://github.com/microsoft/TypeScript/issues/64038) (Open)

**Bug Report: Severe memory leak triggered by "TypeScript \(Native Preview\)" extension**

*VS Code’s TypeScript (Native Preview) extension causes memory growth when opening a blank TypeScript file in a project without package.json.*

 * created by **KostyaTretyak**

### [PR microsoft/TypeScript#64039](https://github.com/microsoft/TypeScript/pull/64039) (Closed)

**Fix infinite recursion bug involving \`as const\` assertions in loops**

*Using `as const` assertions within loops triggers infinite recursion in the TypeScript compiler*

 * created by **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript/pull/64039#issuecomment-5430925931) **ahejlsberg** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/64039#issuecomment-5430926683) **typescript-automation[bot]** reported CI build job statuses and result links
 * [today](https://github.com/microsoft/TypeScript/pull/64039#issuecomment-5431144785) **typescript-automation[bot]** reported user test results, noted infrastructure failures, and confirmed that everything else looked good
 * [today](https://github.com/microsoft/TypeScript/pull/64039#issuecomment-5431205944) **typescript-automation[bot]** provided performance run results
 * [today](https://github.com/microsoft/TypeScript/pull/64039#issuecomment-5431331900) **typescript-automation[bot]** notified that the results of running the DT tests were ready and everything looked the same
 * [today](https://github.com/microsoft/TypeScript/pull/64039#issuecomment-5431602052) **typescript-automation[bot]** reported that running tsc on the top 400 repos comparing main and the pull request merge succeeded
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript#64040](https://github.com/microsoft/TypeScript/pull/64040) (Open, `For Uncommitted Bug`)

**Replace Node interface with discriminated unions **

*Replace the Node interface with discriminated union types for improved type safety.*

 * created by **ArnaudBarre**

### [PR microsoft/TypeScript#64041](https://github.com/microsoft/TypeScript/pull/64041) (Closed, **RyanCavanaugh**, **Copilot**)

**Error on misplaced \`use strict\` directives**

*Introduce errors when 'use strict' directives are placed after executable statements or inside nested blocks.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript/pull/64041#issuecomment-5431861983) **RyanCavanaugh** said "Just curious what this would do"
 * [today](https://github.com/microsoft/TypeScript/pull/64041#issuecomment-5431862922) **RyanCavanaugh** said "@typescript-bot run top1000"
 * [today](https://github.com/microsoft/TypeScript/pull/64041#issuecomment-5432223859) **RyanCavanaugh** said "@typescript-bot test top1000"
 * [today](https://github.com/microsoft/TypeScript/pull/64041#issuecomment-5432224635) **typescript-automation[bot]** reported that CI jobs started and provided status and results links
 * [today](https://github.com/microsoft/TypeScript/pull/64041#issuecomment-5432871314) **typescript-automation[bot]** reported test results for top 1000 repos showing everything looked good

### [PR microsoft/TypeScript#64042](https://github.com/microsoft/TypeScript/pull/64042) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**Content mapper auto import formatting panic**

*Reusing synthesized nodes during content mapping caused formatting crashes, fixed by cloning nodes and refactoring the change tracker.*

 * created by **andrewbranch**

### [PR microsoft/TypeScript#64043](https://github.com/microsoft/TypeScript/pull/64043) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Align object binding defaults with arrays**

*Implement consistent default value handling in object destructuring to match array bindings*

 * created by **jakebailey**

### [PR microsoft/TypeScript#64044](https://github.com/microsoft/TypeScript/pull/64044) (Open, `Author: Team`, `For Milestone Bug`, **jakebailey**)

**Speed up narrowing of literal unions**

*Optimizes narrowing of literal unions, cutting user CPU time from around 11 seconds to under 0.1 second.*

 * created by **jakebailey**

### [PR microsoft/TypeScript#64045](https://github.com/microsoft/TypeScript/pull/64045) (Closed)

**Delete pr\_owners\.txt**

*Remove the pr_owners.txt file from the repository since it is no longer used.*

 * created by **jakebailey**

### [PR microsoft/TypeScript#64046](https://github.com/microsoft/TypeScript/pull/64046) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Flip files from CRLF to LF**

*Convert all repository files except testdata and locale directories to LF line endings for consistency.*

 * created by **jakebailey**

### [Issue microsoft/TypeScript#64047](https://github.com/microsoft/TypeScript/issues/64047) (Open, `Suggestion`)

**\(Proposal\) more\-sophisticated CFA, and Narrowing Boolean Types**

*Propose enhancements to TypeScript’s control-flow analysis to track type narrowing across indirections and support boolean variables with type-predicate signatures.*

 * created by **irfanstract**
 * [today](https://github.com/microsoft/TypeScript/issues/64047#issuecomment-5433323789) **Irfan-lab700** said "assign"

### [PR microsoft/TypeScript#64048](https://github.com/microsoft/TypeScript/pull/64048) (Closed)

**Delete defunct GHA workflows**

*Delete obsolete GitHub Actions workflows (LKG, pr-modified-files, release branch artifact) no longer required.*

 * created by **jakebailey**

### [Issue microsoft/TypeScript#64049](https://github.com/microsoft/TypeScript/issues/64049) (Closed, `Won't Fix`)

**Erasing a \`const enum\` can emit an illegal \`"use strict"\` directive**

*Erasing a const enum places a string literal first in a default-parameter function, creating an illegal 'use strict' directive.*

 * created by **magic-akari**
 * **RyanCavanaugh** added label `Won't Fix`
 * [later](https://github.com/microsoft/TypeScript/issues/64049#issuecomment-5441731799) **RyanCavanaugh** ran #64041 to check for misplaced `use strict` directives, found none, and emphasized that disabling `use strict` is not acceptable

### [Issue microsoft/TypeScript#64050](https://github.com/microsoft/TypeScript/issues/64050) (Open, `Needs Investigation`, **andrewbranch**)

**Content mapper duplicated inlay hints**

*Splitting a statement into multiple spans in the content mapper causes duplicate inlay hints due to separate hint generation for each span.*

 * created by **jasonlyu123**
 * [today](https://github.com/microsoft/TypeScript/issues/64050#issuecomment-5434695975) **scs0209** said "I'd like to work on this. Can I try it?"

### [PR microsoft/TypeScript#64051](https://github.com/microsoft/TypeScript/pull/64051) (Closed)

**Create Yeet**

*Add a new Yeet feature to the codebase.*

 * created by **spam71923-bot**
 * (later) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64052](https://github.com/microsoft/TypeScript/pull/64052) (Open, `For Milestone Bug`)

**Fix false positive TS8030 for JSDoc @type on optional interface methods**

*Strip undefined from JSDoc @type annotations on optional interface methods before signature resolution to prevent false TS8030 errors.*

 * created by **jyx-07**
 * [later](https://github.com/microsoft/TypeScript/pull/64052#issuecomment-5438749711) **jyx-07** said "@microsoft-github-policy-service agree"

