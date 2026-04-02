# Report for 2026-01-21 (Wednesday, January 21st, 2026)

24 different users commented on 47 different issues.

## Recommended Actions

 * Moderation
    * @louwers posted rude content in [microsoft/TypeScript#51556](https://github.com/microsoft/TypeScript/issues/51556#issuecomment-3783274021)
    * @lolmaus used uncivil language towards another user in [microsoft/TypeScript#51556](https://github.com/microsoft/TypeScript/issues/51556#issuecomment-3784038641)
 * Response Recommended
    * @jonathantneal provided a pull request for review in [microsoft/TypeScript#46135](https://github.com/microsoft/TypeScript/issues/46135#issuecomment-3784607037)
    * @okadurin confirmed that the issue was still valid and reproducible in [microsoft/TypeScript#51622](https://github.com/microsoft/TypeScript/issues/51622#issuecomment-3780894739)
    * @justinfagnani reported ongoing complaints about the verbosity of auto-accessors in [microsoft/TypeScript#54240](https://github.com/microsoft/TypeScript/issues/54240#issuecomment-3780932892)
    * @justinfagnani asked about whether the issue could be revisited and proposed a solution in [microsoft/TypeScript#55669](https://github.com/microsoft/TypeScript/issues/55669#issuecomment-3780913402)
    * @justinfagnani asked for clarification on valler's analogy in [microsoft/TypeScript#62630](https://github.com/microsoft/TypeScript/issues/62630#issuecomment-3780881723)
    * @justinfagnani reported that the construction doesn't support type narrowing and provided a code example in [microsoft/TypeScript#62630](https://github.com/microsoft/TypeScript/issues/62630#issuecomment-3781279691)
    * @rugk suggested adding documentation on Promise void handling in [microsoft/TypeScript#63028](https://github.com/microsoft/TypeScript/issues/63028#issuecomment-3781015419)
    * @themaxgross asked if export or the temporal dead zone might be causing the confusing behavior in [microsoft/TypeScript#63029](https://github.com/microsoft/TypeScript/issues/63029#issuecomment-3781506915)
    * @letusgitcommit asked for feedback on the proposed workaround in [microsoft/TypeScript#63037](https://github.com/microsoft/TypeScript/issues/63037#issuecomment-3783918038)
    * @letusgitcommit provided a link to a related issue in [microsoft/TypeScript#63037](https://github.com/microsoft/TypeScript/issues/63037#issuecomment-3784118990)

## Activity Summary

### [Issue microsoft/TypeScript#12936](https://github.com/microsoft/TypeScript/issues/12936) (Open, `Suggestion`, `Awaiting More Feedback`)

**Exact Types**

*Introduce an Exact<T> type (e.g. |T|) to enforce exact object types and disallow extra properties.*

 * [36 weeks ago](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-2864039225) **niti2539** provided a workaround solution with screenshots illustrating various type matching scenarios
 * [13 weeks ago](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3419149140) **shoxter** asked why the holdout existed and whether technical reasons or maintainers' opposition and if the v7 release and Go implementation address it
 * [7 weeks ago](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3587413546) **RobertSandiford** asked why the feature was on hold, inquired if technical constraints or maintainer opposition caused it, and asked if v7 or the Go implementation fixes it, and raised concerns about interoperability between exact and loose object types
 * [later](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3784926982) **AntonVoronezh** proposed the 'Exorcist' fix example and suggested an 'I Mean It' operator (!) to enforce exact types in TypeScript
 * [later](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3785027582) **adrian-gierakowski** praised the "I Mean It" Operator
 * [later](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3785027582) **adrian-gierakowski** praised the "I Mean It" Operator
 * [later](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3785027582) **adrian-gierakowski** praised the "I Mean It" Operator
 * [later](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3785027582) **adrian-gierakowski** praised the "I Mean It" Operator
 * [later](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3785027582) **adrian-gierakowski** praised the "I Mean It" Operator
 * [later](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3785027582) **adrian-gierakowski** praised the "I Mean It" Operator
 * [later](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3785027582) **adrian-gierakowski** praised the "I Mean It" Operator
 * [later](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3785027582) **adrian-gierakowski** praised the "I Mean It" Operator
 * [later](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3785027582) **adrian-gierakowski** praised the "I Mean It" Operator
 * [later](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3785027582) **adrian-gierakowski** praised the "I Mean It" Operator
 * [later](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3785027582) **adrian-gierakowski** praised the "I Mean It" Operator
 * [later](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3785027582) **adrian-gierakowski** praised the "I Mean It" Operator
 * [later](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3785027582) **adrian-gierakowski** praised the "I Mean It" Operator
 * [later](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3785027582) **adrian-gierakowski** praised the "I Mean It" Operator
 * [later](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3785027582) **adrian-gierakowski** praised the "I Mean It" Operator

### [Issue microsoft/TypeScript#17002](https://github.com/microsoft/TypeScript/issues/17002) (Open, `Suggestion`, `In Discussion`, `Domain: lib.d.ts`, `Fix Available`)

**Array\.isArray type narrows to any\[\] for ReadonlyArray\<T\>**

*Array.isArray fails to correctly narrow a union including ReadonlyArray<T>, resulting in an any[] type instead of ReadonlyArray<T>.*

 * [41 weeks ago](https://github.com/microsoft/TypeScript/issues/17002#issuecomment-2781717755) **jonlepage** posted a TypeScript solution extending ArrayConstructor with isArray and linked to a playground
 * [41 weeks ago](https://github.com/microsoft/TypeScript/issues/17002#issuecomment-2782169204) **A-EbrahimRSA** thanked the commenter, noted they'd seen the workaround, and expressed preference for using the built-in .isArray method
 * [41 weeks ago](https://github.com/microsoft/TypeScript/issues/17002#issuecomment-2787918238) **oconnorjoseph** said "Our team just ran into this issue with the readonly keyword as well. We would very much appreciate for this to work natively."
 * [later](https://github.com/microsoft/TypeScript/issues/17002#issuecomment-3784982171) **spalt08** offered another workaround using Array.isArray to define a readonly array type guard

### [Issue microsoft/TypeScript#46135](https://github.com/microsoft/TypeScript/issues/46135) (Open, `Suggestion`, `Awaiting More Feedback`)

**Ambient Module Declarations for Import Attributes \(formerly known as Import Assertions\)**

*Enable ambient module declarations based on import attributes to provide type definitions for CSS modules and asset URL imports.*

 * [18 weeks ago](https://github.com/microsoft/TypeScript/issues/46135#issuecomment-3284241553) **AFatNiBBa** said "Is there anything new on this?"
 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/46135#issuecomment-3692946297) **otomad** suggested supporting the inline grab module type and provided a TypeScript code example
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/46135#issuecomment-3745345018) **justinfagnani** noted that major browsers, Node, Deno, Bun, Rollup, and Webpack support CSS and JSON modules with import attributes, and asked if that provides enough platform support for TypeScript support
 * [later](https://github.com/microsoft/TypeScript/issues/46135#issuecomment-3784607037) **jonathantneal** created a pull request for the issue

### [Issue microsoft/TypeScript#51556](https://github.com/microsoft/TypeScript/issues/51556) (Open, `Suggestion`, `Awaiting More Feedback`)

**Support \`satisfies\` operator on functions**

*Allow the TypeScript satisfies operator to be used after function declarations to preserve return types.*

 * [38 weeks ago](https://github.com/microsoft/TypeScript/issues/51556#issuecomment-2827467674) **RebeccaStevens** suggested moving the `satisfies` keyword forward for easier readability and provided an example
 * [38 weeks ago](https://github.com/microsoft/TypeScript/issues/51556#issuecomment-2827490110) **mark-dr** argued that using a complex ‘satisfies’ type annotation would harm readability by distancing the function name from its parameters
 * [29 weeks ago](https://github.com/microsoft/TypeScript/issues/51556#issuecomment-3014068113) **marcospgp** noted that exporting a function type isn't possible and requested the feature to enable type checking and hinting for user functions
 * [today](https://github.com/microsoft/TypeScript/issues/51556#issuecomment-3782348788) **rafa-br34** said "Crazy how it has been 3 years and this is still unimplemented."
 * [later](https://github.com/microsoft/TypeScript/issues/51556#issuecomment-3783274021) **louwers** said "@rafa-br34 You just sent a notification to 337 (or more) people following this issue without providing any new information. This is bad GitHub etiquette."
 * [later](https://github.com/microsoft/TypeScript/issues/51556#issuecomment-3784038641) **lolmaus** criticized a user for sending mass notifications without new information, argued that Microsoft profits from TypeScript and should address issues, and defended loudly raising developer concerns

### [Issue microsoft/TypeScript#51622](https://github.com/microsoft/TypeScript/issues/51622) (Closed, `Needs Investigation`, `Fix Available`, **weswigham**)

**Different Declaration output for same code from js and ts file**

*TypeScript emits different import paths in .d.ts files for identical JavaScript versus TypeScript sources, causing type mismatches.*

 * [3.1 years ago](https://github.com/microsoft/TypeScript/issues/51622#issuecomment-1341321797) **daKmoR** asked if maintainers needed further assistance and questioned if the reproduction was sufficient, then provided a more complex monorepo example illustrating path resolution issues
 * **weswigham** added label `Fix Available`
 * (3 years ago) **weswigham** closed the issue
 * [today](https://github.com/microsoft/TypeScript/issues/51622#issuecomment-3780894739) **okadurin** said "The issue is still valid and the actual behaviour part is reproducible"

### [Issue microsoft/TypeScript#54240](https://github.com/microsoft/TypeScript/issues/54240) (Open, `Suggestion`, `In Discussion`)

**Accessors should be allowed to be optional**

*Allow optional accessors in TypeScript to streamline decorator usage and match optional property behavior.*

 * [2.3 years ago](https://github.com/microsoft/TypeScript/issues/54240#issuecomment-1707501401) **rbuckton** explained that accessor transforms fields into get/set pairs and optionality indicates potentially missing fields, recommended defining properties as `accessor x: Foo | undefined` and updating the codemod to remove `?` and add `| undefined`, and discussed the historical semantics of optional class fields
 * [2.3 years ago](https://github.com/microsoft/TypeScript/issues/54240#issuecomment-1708838557) **justinfagnani** explained that although a code mod could handle dropping optionality and adding | undefined, not everyone will use it and it increases boilerplate for new code; argued that treating `?` as shorthand for `| undefined` is intuitive and consistent for auto-accessors
 * [1.2 years ago](https://github.com/microsoft/TypeScript/issues/54240#issuecomment-2442227079) **justinfagnani** complained about the extra boilerplate required for optional accessors when using decorators and requested optional accessor support to reduce verbosity
 * [today](https://github.com/microsoft/TypeScript/issues/54240#issuecomment-3780932892) **justinfagnani** said "We're still hearing complaints from Lit developers migrating to standard decorators that auto-accessors are painfully verbose."

### [Issue microsoft/TypeScript#55669](https://github.com/microsoft/TypeScript/issues/55669) (Open, `Suggestion`, `Awaiting More Feedback`)

**Experimental decorators do not get access to the initial value when using auto\-accessors**

*Auto-accessor assignments in experimental decorator mode bypass the setter, preventing decorators from accessing initial values.*

 * [2.3 years ago](https://github.com/microsoft/TypeScript/issues/55669#issuecomment-1732167260) **trusktr** questioned the need to support both legacy and standard decorators simultaneously, suggested using useDefineForClassFields:true to drop accessor and simplify upgrading, and outlined implementation strategies
 * [2.3 years ago](https://github.com/microsoft/TypeScript/issues/55669#issuecomment-1732182154) **justinfagnani** explained that experimental decorators differ in capabilities from standard decorators, clarified why useDefineForClassFields couldn't be used for Lit, and asserted that the accessor decorator is the correct approach
 * [2.3 years ago](https://github.com/microsoft/TypeScript/issues/55669#issuecomment-1732187017) **trusktr** suggested replacing own properties with getters/setters and asserted negligible performance impact based on personal experience
 * [today](https://github.com/microsoft/TypeScript/issues/55669#issuecomment-3780913402) **justinfagnani** asked whether the issue could be revisited and suggested running the initial value through the setter
 * **RyanCavanaugh** unassigned **rbuckton**
 * [today](https://github.com/microsoft/TypeScript/issues/55669#issuecomment-3781057424) **RyanCavanaugh** said "@justinfagnani isn't this enormously likely to break someone who was depending on the setter not running?"
 * [today](https://github.com/microsoft/TypeScript/issues/55669#issuecomment-3781149794) **justinfagnani** explained that experimental decorators with auto-accessors are rare outside Lit migrations, reported testing confirmed compatibility, and suggested deprecating and closing the experimental decorator code
 * [today](https://github.com/microsoft/TypeScript/issues/55669#issuecomment-3781210654) **RyanCavanaugh** noted that there was no reasonable path to deprecate experimental decorators due to extensive usage and reluctance to break users or expand configuration
 * (today) **RyanCavanaugh** added labels `Suggestion`, `Awaiting More Feedback`, and removed label `Needs Investigation`

### [Issue microsoft/TypeScript#62195](https://github.com/microsoft/TypeScript/issues/62195) (Open, `Suggestion`, `Breaking Change`, `Committed`, `Fix Available`, **RyanCavanaugh**, **Copilot**)

**Change default of \`types\` to \`\[\]\` in \`tsconfig\.json\`**

*Default tsconfig.json types now empty in TS 6.0, requiring explicit 'types' entries or imports and supporting '*' for legacy inclusion.*

 * [24 weeks ago](https://github.com/microsoft/TypeScript/issues/62195#issuecomment-3157093307) **Jamesernator** asked whether these changes or other TS7 updates would facilitate per-file scoped libs, such as excluding DOM in worker.ts or limiting globals in .test.ts files
 * [24 weeks ago](https://github.com/microsoft/TypeScript/issues/62195#issuecomment-3157094969) **jakebailey** said "No, it would not. That still requires multiple configs."
 * **DanielRosenwasser** assigned to **RyanCavanaugh**
 * **RyanCavanaugh** assigned to **Copilot**
 * (today) **typescript-bot** added labels `Fix Available`, `Fix Available`

### [Issue microsoft/TypeScript#62196](https://github.com/microsoft/TypeScript/issues/62196) (Open, `Suggestion`, `Breaking Change`, `Committed`, **jakebailey**)

**Deprecate \`\-\-target es5\`, make lowest target \`es2015\`**

*Deprecate --target es5 in TypeScript 6.0, raise the minimum target to ES2015, and update library inclusion and downlevel iteration handling.*

 * [6 weeks ago](https://github.com/microsoft/TypeScript/issues/62196#issuecomment-3634794340) **csvn** explained possible TS team motivations for deprecating only ES5, described trends toward isolatedModules and bundler-based downleveling, and noted the difficulty of querying recent ES5 project usage on GitHub
 * [6 weeks ago](https://github.com/microsoft/TypeScript/issues/62196#issuecomment-3636417235) **guilhermesimoes** questioned TypeScript's long-term vision after observing a liked comment suggesting bundlers handle down-leveling and acknowledged the maintenance complexity of ES5
 * [6 weeks ago](https://github.com/microsoft/TypeScript/issues/62196#issuecomment-3636428371) **guilhermesimoes** questioned the repository count, noted telemetry showing ES5 usage could be a floor, and asked how the 8% was calculated
 * (today) **RyanCavanaugh** assigned to **jakebailey**, and unassigned **iisaduan**

### [Issue microsoft/TypeScript#62198](https://github.com/microsoft/TypeScript/issues/62198) (Open, `Suggestion`, `Breaking Change`, `Committed`, **jakebailey**)

**Change default \`\-\-target\` to latest ECMAScript version**

*Change TypeScript’s default target from ES5 to the latest ECMAScript version to promote modern runtime support.*

 * [14 weeks ago](https://github.com/microsoft/TypeScript/issues/62198#issuecomment-3399328312) **DanielRosenwasser** described that the team decided to default to the latest stable ECMAScript target (e.g., es2025, es2026) and to update it periodically instead of using a name like escurrent
 * [14 weeks ago](https://github.com/microsoft/TypeScript/issues/62198#issuecomment-3400167733) **kirkwaiblinger** asked whether updating the default value would be subject to the 2.5 year breaking change cadence
 * [14 weeks ago](https://github.com/microsoft/TypeScript/issues/62198#issuecomment-3402451976) **RyanCavanaugh** said "No, the default would be "whatever was currently current at the time of the beta" the same way esnext is a moving target"
 * (today) **RyanCavanaugh** assigned to **jakebailey**, and unassigned **Copilot**, **RyanCavanaugh**

### [Issue microsoft/TypeScript#62213](https://github.com/microsoft/TypeScript/issues/62213) (Open, `Suggestion`, `Breaking Change`, `Committed`, `Fix Available`, **weswigham**, **RyanCavanaugh**, **Copilot**)

**Assume \`"use strict"\` everywhere by default**

*Default-enable strict mode in TypeScript 6.0 by removing the --alwaysStrict flag to improve performance and simplify AST sharing.*

 * **DanielRosenwasser** assigned to **weswigham**
 * [10 weeks ago](https://github.com/microsoft/TypeScript/issues/62213#issuecomment-3498785245) **jakebailey** proposed deprecating `--alwaysStrict false` in 6.0 and removing it in 7.0
 * [10 weeks ago](https://github.com/microsoft/TypeScript/issues/62213#issuecomment-3498844333) **jakebailey** said "Note that the implication here is that we unconditionally emit "use strict" in non-ESM files."
 * (today) **RyanCavanaugh** assigned to **Copilot**, **RyanCavanaugh**
 * (today) **typescript-bot** added labels `Fix Available`, `Fix Available`, `Fix Available`

### [Issue microsoft/TypeScript#62630](https://github.com/microsoft/TypeScript/issues/62630) (Open, `Suggestion`, `Awaiting More Feedback`)

**Allow classes to implement unions of object types**

*Allow classes to implement unions of object types with identical properties for discriminated type narrowing.*

 * **RyanCavanaugh** added label `Awaiting More Feedback`
 * [9 weeks ago](https://github.com/microsoft/TypeScript/issues/62630#issuecomment-3530882333) **valler** clarified that extending from a union isn't supported and explained differences between union of signatures and overloads, questioned how interfaces could extend unions, and provided a non-class analogy
 * [9 weeks ago](https://github.com/microsoft/TypeScript/issues/62630#issuecomment-3531871254) **valler** discussed a lack of use case for implementing `class C implements A | B` versus assigning a constructor type `new() => A | B`, explained that type inference already covers the latter and existing signatures accept unions, and contrasted it with the different semantics of a union of constructor signatures
 * [today](https://github.com/microsoft/TypeScript/issues/62630#issuecomment-3780881723) **justinfagnani** explained that he kept interfaces and union types, dropped the class, and demonstrated the existing mutation problem, and asked valler to clarify the analogy
 * [today](https://github.com/microsoft/TypeScript/issues/62630#issuecomment-3781173035) **DanielRosenwasser** asked if the provided code snippet met the requirements
 * [today](https://github.com/microsoft/TypeScript/issues/62630#issuecomment-3781279691) **justinfagnani** reported that the proposed construction failed to narrow 'this' in methods and demonstrated the type error with a code snippet

### [Issue microsoft/TypeScript#63001](https://github.com/microsoft/TypeScript/issues/63001) (Open, `Needs Investigation`, **DanielRosenwasser**)

**Global 'this' capture logic is slightly wrong in \`\-\-noImplicitThis\`**

*Arrow functions within functions typed with globalThis incorrectly trigger a --noImplicitThis global this capture error.*

 * created by **DanielRosenwasser**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63001#issuecomment-3774685642) **RyanCavanaugh** provided an automated analysis with similar issues for potential duplicates and noted the behavior might be intentional
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **DanielRosenwasser**

### [Issue microsoft/TypeScript#63004](https://github.com/microsoft/TypeScript/issues/63004) (Open, `Bug`)

**Explicit \`never\` return type in \`catch\` block & condition in \`finally\` marks the whole \`finally\` block as unreachable**

*TypeScript incorrectly flags a conditional finally block as unreachable when a catch handler calls a function declared to return never.*

 * created by **d-fischer**
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63004#issuecomment-3765286934) **Andarist** said "https://github.com/microsoft/TypeScript/pull/61265 fixes this too"
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63004#issuecomment-3774685680) **RyanCavanaugh** generated an automated response listing similar issues
 * (today) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#63005](https://github.com/microsoft/TypeScript/issues/63005) (Open, `Bug`, `Help Wanted`, `Domain: Crashes`)

**Crash： when inferring from a tuple with middle rest elements and trailing variadic elements**

*TS compiler crashes when inferring a tuple with both middle rest and trailing variadic elements.*

 * (yesterday) **RyanCavanaugh** added labels `Bug`, `Help Wanted`, and set milestone to `Backlog`
 * **RyanCavanaugh** added label `Domain: Crashes`

### [PR microsoft/TypeScript#63006](https://github.com/microsoft/TypeScript/pull/63006) (Open, `For Milestone Bug`, **RyanCavanaugh**)

**Don't try to narrow type of a symbol within RHS of its declaration**

*Prevent the TypeScript compiler from applying type narrowing to a symbol within its own declaration’s right-hand side.*

 * created by **Andarist**
 * (4 days ago) **typescript-bot** added label `For Milestone Bug`, and assigned to **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript/pull/63006#issuecomment-3781565259) **jakebailey** said "Do we need a different approach? Or can we just match? (Why the difference?)"
 * [today](https://github.com/microsoft/TypeScript/pull/63006#issuecomment-3781616736) **Andarist** mentioned that Strada could match Corsa’s patch but this PR predates Corsa’s and since they removed a node flag thought it worth review, and offered to close it
 * [today](https://github.com/microsoft/TypeScript/pull/63006#issuecomment-3781630260) **jakebailey** said "Oh, I just want them to match; I don't think that a method that saves us a flag is bad, just trying to understand how to align things."

### [PR microsoft/TypeScript#63013](https://github.com/microsoft/TypeScript/pull/63013) (Closed, `For Uncommitted Bug`, `dependencies`, `github_actions`)

**Bump the github\-actions group across 1 directory with 3 updates**

*Bump actions/setup-node to v6.2.0 and update actions/cache and github/codeql-action in the root directory*

 * (3 days ago) **dependabot[bot]** added labels `dependencies`, `github_actions`
 * **typescript-bot** added label `For Uncommitted Bug`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#63015](https://github.com/microsoft/TypeScript/issues/63015) (Open, `Bug`, `Fix Available`, `Domain: Crashes`, **gabritto**)

**Regression Crash: RangeError: Maximum call stack size exceeded in isThisInTypeQuery on Nightly**

*Nightly TypeScript crashes with RangeError stack overflow when type-checking a union of call signatures with differing return types*

 * (yesterday) **RyanCavanaugh** added label `Bug`, and set milestone to `TypeScript 6.0.0`
 * **typescript-bot** added label `Fix Available`
 * **RyanCavanaugh** added label `Domain: Crashes`

### [PR microsoft/TypeScript#63023](https://github.com/microsoft/TypeScript/pull/63023) (Closed, `Author: Team`, `For Uncommitted Bug`, **DanielRosenwasser**)

**Turn \`// @strict\` off in all failing fourslash tests which do not contain baseline calls**

*Apply a script to disable // @strict in all failing fourslash tests that lack baseline calls.*

 * (yesterday) **typescript-bot** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **DanielRosenwasser**
 * (today) **DanielRosenwasser** closed the issue

### [Issue microsoft/TypeScript#63027](https://github.com/microsoft/TypeScript/issues/63027) (Closed, `Won't Fix`)

**\`ts\.getTextOfJSDocComment\` is stripping leading \`http\` when the jsdoc starts with an absolute URL\.**

*ts.getTextOfJSDocComment strips the http prefix from absolute URLs in JSDoc comments.*

 * created by **JeanMeche**
 * **RyanCavanaugh** added label `Won't Fix`
 * [today](https://github.com/microsoft/TypeScript/issues/63027#issuecomment-3780406373) **RyanCavanaugh** said "With 6.0 going into maintenance mode and this potentially breaking other API use cases, this isn't something we're going to be changing."
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63028](https://github.com/microsoft/TypeScript/issues/63028) (Closed, `Not a Defect`)

**\(ES2024\) The resolving function in Promise\.withResolvers\(\) is not allowed to be passed no arguments \(void\) unless explicitly specified**

*In ES2024, Promise.withResolvers() erroneously treats its resolve function as requiring arguments unless explicitly typed as void.*

 * created by **rugk**
 * [today](https://github.com/microsoft/TypeScript/issues/63028#issuecomment-3780269967) **IllusionMH** explained that the behavior aligned with the `resolve` parameter requirements in the Promise constructor and linked to the TypeScript 4.1 release notes
 * [today](https://github.com/microsoft/TypeScript/issues/63028#issuecomment-3781015419) **rugk** thanked for the link, tested the old-school Promise approach and confirmed the error, found the void handling unexpected, and suggested adding documentation on Promise handling
 * **RyanCavanaugh** added label `Not a Defect`
 * [today](https://github.com/microsoft/TypeScript/issues/63028#issuecomment-3781046115) **RyanCavanaugh** explained that explicitly using Promise.withResolvers<void> was unnecessary since void is the default and that TypeScript errs on the side of safety distinguishing omitted versus provided arguments, suggesting resolve(undefined) to omit values

### [Issue microsoft/TypeScript#63029](https://github.com/microsoft/TypeScript/issues/63029) (Closed, `Working as Intended`)

**Top\-level variable type narrowing not matched within a function**

*TypeScript fails to retain top-level ENV_VAR’s narrowed string type inside the getEnvVars() function.*

 * created by **themaxgross**
 * [today](https://github.com/microsoft/TypeScript/issues/63029#issuecomment-3781348432) **RyanCavanaugh** provided alternative code snippets for handling environment variable initialization and type checking
 * **RyanCavanaugh** added label `Working as Intended`
 * [today](https://github.com/microsoft/TypeScript/issues/63029#issuecomment-3781506915) **themaxgross** suggested testing code demonstrating confusing TypeScript behavior with variable declarations and the temporal dead zone, and asked if that might be the issue
 * [today](https://github.com/microsoft/TypeScript/issues/63029#issuecomment-3781860250) **RyanCavanaugh** said "Right, you can observe ENV_VAR having the value undefined from getEnvVars (through some hypothetical indirect call), but OTHER_VAR is either a TDZ violation or a string, never undefined."

### [PR microsoft/TypeScript#63030](https://github.com/microsoft/TypeScript/pull/63030) (Open, `For Milestone Bug`, **RyanCavanaugh**, **Copilot**)

**Deprecate alwaysStrict: false in TypeScript 6\.0**

*TypeScript 6.0 deprecates alwaysStrict=false, emitting warnings and requiring ignoreDeprecations to silence them ahead of its removal in 7.0.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * (today) **typescript-bot** added labels `For Milestone Bug`, `For Milestone Bug`

### [PR microsoft/TypeScript#63031](https://github.com/microsoft/TypeScript/pull/63031) (Closed, `For Milestone Bug`, **RyanCavanaugh**, **Copilot**)

**Change default of \`types\` to \`\[\]\` in tsconfig\.json**

*Default tsconfig.json types array is now empty, with '*' wildcard support to maintain legacy inclusion and boost performance.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * (today) **typescript-bot** added labels `For Milestone Bug`, `For Milestone Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63031#issuecomment-3781900715) **jakebailey** said "Annoyingly the use of ` means it's not easy for a potential twoslash comment to target it, since  is for variants, but, I don't even think twoslash supports types` anyway"

### [Issue microsoft/TypeScript#63032](https://github.com/microsoft/TypeScript/issues/63032) (Closed, `Working as Intended`)

**Narrowing readonly class instance using \`instanceof\` results in mutability**

*Narrowing a Readonly class instance with instanceof incorrectly drops its readonly properties and permits assignments.*

 * created by **jsejcksn**
 * [later](https://github.com/microsoft/TypeScript/issues/63032#issuecomment-3783332231) **MartinJohns** clarified that the code behaved as intended and explained that Readonly<T> only marks properties as readonly via the interface and doesn’t enforce immutability

### [Issue microsoft/TypeScript#63033](https://github.com/microsoft/TypeScript/issues/63033) (Open)

**Autocomplete incorrectly suggests transitive files from monorepo package**

*Autocomplete incorrectly suggests unexported internal files from a monorepo package despite its exports configuration.*

 * created by **ericnorris**

### [Issue microsoft/TypeScript#63034](https://github.com/microsoft/TypeScript/issues/63034) (Closed)

**\`Record\<string, T\> satisfies Record\<"literal", T\>\`**

*TypeScript incorrectly allows Record<string, number> to satisfy Record<'literal', number> even though the ‘literal’ property isn’t guaranteed.*

 * created by **paperclover**
 * [today](https://github.com/microsoft/TypeScript/issues/63034#issuecomment-3782416511) **MartinJohns** said "Duplicate of #62796."
 * [later](https://github.com/microsoft/TypeScript/issues/63034#issuecomment-3783462558) **paperclover** said "thank you for finding. "
 * (later) **paperclover** closed the issue

### [PR microsoft/TypeScript#63035](https://github.com/microsoft/TypeScript/pull/63035) (Closed, `For Uncommitted Bug`)

**Add messageformat types**

*Add TypeScript type definitions for the messageformat library to improve type safety*

 * created by **aprameyak**
 * [today](https://github.com/microsoft/TypeScript/pull/63035#issuecomment-3782352197) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * **typescript-bot** added label `For Uncommitted Bug`

### [PR microsoft/TypeScript#63036](https://github.com/microsoft/TypeScript/pull/63036) (Open, `For Uncommitted Bug`)

**Add support for import attributes in ambient module declarations**

*Enable import attributes in ambient module declarations to ensure correct parsing, module resolution, type checking, and diagnostics.*

 * created by **jonathantneal**
 * **typescript-bot** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63036#issuecomment-3782583818) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [today](https://github.com/microsoft/TypeScript/pull/63036#issuecomment-3782583826) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [today](https://github.com/microsoft/TypeScript/pull/63036#issuecomment-3782584168) **typescript-bot** advised to document breaking changes on the wiki and notify DanielRosenwasser and RyanCavanaugh
 * [today](https://github.com/microsoft/TypeScript/pull/63036#issuecomment-3782592823) **jonathantneal** said "@microsoft-github-policy-service agree"

### [Issue microsoft/TypeScript#63037](https://github.com/microsoft/TypeScript/issues/63037) (Closed)

**tsc 5\.9\.3 is not transpiling**

*Upgrading to TypeScript 5.9.3 breaks transpilation in a simple monorepo project despite unchanged tsconfig and code.*

 * created by **letusgitcommit**
 * [later](https://github.com/microsoft/TypeScript/issues/63037#issuecomment-3783918038) **letusgitcommit** said "Experienced the same behavior on typescript 5.9.2. It would appear the problem was mitigated by deleting the tsconfig.buildinfo file. Thoughts?"
 * [later](https://github.com/microsoft/TypeScript/issues/63037#issuecomment-3784118990) **letusgitcommit** provided a link to a related issue as an answer
 * (later) **letusgitcommit** closed the issue

