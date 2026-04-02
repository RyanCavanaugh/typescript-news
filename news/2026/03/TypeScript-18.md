# Report for 2026-03-18 (Wednesday, March 18th, 2026)

13 different users commented on 15 different issues.

## Recommended Actions

 * Response Recommended
    * @Finesse asked about options for achieving source code concealment via private field minification and why const enum is allowed in [microsoft/TypeScript#31670](https://github.com/microsoft/TypeScript/issues/31670#issuecomment-4088397826)
    * @michAtEl suggested adding a configurable truncation limit or expandable hover panel for long type descriptions in [microsoft/TypeScript#41860](https://github.com/microsoft/TypeScript/issues/41860#issuecomment-4088331169)
    * @newives reported that the TypeScript 6.0 Final Release job failed to launch in [microsoft/TypeScript#63085](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-4087494508)
    * @newives asked if a specific release date was available in [microsoft/TypeScript#63085](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-4087648587)

## Activity Summary

### [Issue microsoft/TypeScript#22914](https://github.com/microsoft/TypeScript/issues/22914) (Open, `Suggestion`, `Awaiting More Feedback`, `Domain: LS: Organize Imports`)

**Organize imports should remove blank lines within imports**

*Organize imports preserves blank lines between import statements and shifts them instead of removing them.*

 * [6.2 years ago](https://github.com/microsoft/TypeScript/issues/22914#issuecomment-571585640) **PeterStaev** said "+1 to have a flag to allow keeping spaces/groups. "
 * [2.6 years ago](https://github.com/microsoft/TypeScript/issues/22914#issuecomment-1629887969) **jakebailey** noted that imports are no longer moved between groups after those PRs but blank lines between groups are still not removed, so the issue remains partly unresolved
 * [2.6 years ago](https://github.com/microsoft/TypeScript/issues/22914#issuecomment-1664711007) **codesman** described manual import grouping as a maintenance burden with little value and prone to disagreements, noting tooling support eases it but arbitrary sorting remains cumbersome
 * [today](https://github.com/microsoft/TypeScript/issues/22914#issuecomment-4084106730) **Yogu** highlighted that using automatic import formatters without grouping options can leave blank lines and misgrouped imports

### [Issue microsoft/TypeScript#31670](https://github.com/microsoft/TypeScript/issues/31670) (Closed, `Discussion`)

**The future of the "private" keyword**

*Discussion of TypeScript’s plan to retain its existing private keyword while supporting new JavaScript private fields (#fields) and associated rules.*

 * [2.2 years ago](https://github.com/microsoft/TypeScript/issues/31670#issuecomment-1859038998) **trusktr** noted that compiling `private` to soft runtime privacy using symbols under an option would be appealing but falls outside TypeScript's goals
 * (2 years ago) **RyanCavanaugh** closed the issue
 * [20 weeks ago](https://github.com/microsoft/TypeScript/issues/31670#issuecomment-3436325273) **ArrayIterator** mentioned that the private visibility modifier could be dangerous as it might be exposed when objects are stringified
 * [later](https://github.com/microsoft/TypeScript/issues/31670#issuecomment-4088397826) **Finesse** asked about using a TypeScript flag to prepend '#' to private fields for minification benefits and inquired why const enum emit is allowed
 * [later](https://github.com/microsoft/TypeScript/issues/31670#issuecomment-4090013416) **snarbles2** explained that transpiling private to # is not simple due to semantic differences, backward-compatibility concerns, and potential confusion, and clarified that const enums are permitted because they are grandfathered from before TypeScript's type-directed emit stance

### [Issue microsoft/TypeScript#40635](https://github.com/microsoft/TypeScript/issues/40635) (Open, `Suggestion`, `Awaiting More Feedback`)

**Don't require to implement optional abstract properties**

*Allow subclasses of abstract classes to skip implementing properties declared as optional in TypeScript.*

 * [1.2 years ago](https://github.com/microsoft/TypeScript/issues/40635#issuecomment-2560384155) **miguel-leon** described encountering an impossible TypeScript requirement for subclasses to optionally implement methods and expressed skepticism about change due to limited impact
 * [1.1 years ago](https://github.com/microsoft/TypeScript/issues/40635#issuecomment-2593099119) **RobbieTheWagner** said "I am hitting the same issue as @miguel-leon. I would like to define a method signature in the parent and have children optionally implement it. I have not found a way to do so with TS yet."
 * [40 weeks ago](https://github.com/microsoft/TypeScript/issues/40635#issuecomment-2957555405) **gusborg88** said "I support this issue im having this exact problem right now"
 * [later](https://github.com/microsoft/TypeScript/issues/40635#issuecomment-4089959457) **pzuraq** suggested allowing abstract classes to declare optional abstract fields to enable subclasses to choose between getters or fields for accessors

### [Issue microsoft/TypeScript#41860](https://github.com/microsoft/TypeScript/issues/41860) (Open, `Suggestion`, `Domain: Error Messages`, `Awaiting More Feedback`)

**Richer Diagnostic Display Meta\-Issue**

*Enhance diagnostics with multi-line type displays, highlighted error spans, and diff-style color-coded comparisons.*

 * (20 weeks ago) **RyanCavanaugh** added labels `Suggestion`, `Awaiting More Feedback`, and removed label `Meta-Issue`
 * [later](https://github.com/microsoft/TypeScript/issues/41860#issuecomment-4088331169) **michAtEl** suggested adding a configurable truncation limit, a “show full type” action, or an expandable/scrollable hover panel to prevent long type alias descriptions from being truncated in VS Code

### [Issue microsoft/TypeScript#4881](https://github.com/microsoft/TypeScript/issues/4881) (Open, `Suggestion`, `Needs Proposal`)

**Request: Class Decorator Mutation**

*Enable TypeScript to correctly type-check class decorators that add properties for mixins.*

 * [1 week ago](https://github.com/microsoft/TypeScript/issues/4881#issuecomment-4014984624) **yhaskell** illustrated that Zod validation in function form works correctly and expressed expectation that decorator form should behave similarly, providing code examples
 * [today](https://github.com/microsoft/TypeScript/issues/4881#issuecomment-4081810296) **cgauld** argued that decorated function types should reflect changes in function shape and that enforcing non-changing decorators belongs to linting tools
 * [today](https://github.com/microsoft/TypeScript/issues/4881#issuecomment-4081810296) **cgauld** argued that decorated function types should reflect changes in function shape and that enforcing non-changing decorators belongs to linting tools
 * [today](https://github.com/microsoft/TypeScript/issues/4881#issuecomment-4084291238) **iyobo** insisted that decorators affecting function inputs and outputs should manifest in the type system down to generics
 * [today](https://github.com/microsoft/TypeScript/issues/4881#issuecomment-4084291238) **iyobo** insisted that decorators affecting function inputs and outputs should manifest in the type system down to generics
 * [today](https://github.com/microsoft/TypeScript/issues/4881#issuecomment-4085396431) **lolmaus** argued that the decorator design was settled at Stage 3 and criticized TypeScript’s refusal to implement decorator mutations as frustrating and ridiculous
 * [today](https://github.com/microsoft/TypeScript/issues/4881#issuecomment-4085396431) **lolmaus** argued that the decorator design was settled at Stage 3 and criticized TypeScript’s refusal to implement decorator mutations as frustrating and ridiculous
 * [today](https://github.com/microsoft/TypeScript/issues/4881#issuecomment-4085488077) **HolgerJeromin** noted that not implementing decorator mutations isn't a refusal and that resource constraints and TS7 stabilization timeline make addressing it now ineffective
 * [today](https://github.com/microsoft/TypeScript/issues/4881#issuecomment-4085488077) **HolgerJeromin** noted that not implementing decorator mutations isn't a refusal and that resource constraints and TS7 stabilization timeline make addressing it now ineffective

### [Issue microsoft/TypeScript#60632](https://github.com/microsoft/TypeScript/issues/60632) (Open, `Suggestion`, `Awaiting More Feedback`)

**Enable Type Checking for Custom File Extensions**

*Add support in tsconfig.json for type-checking files with custom extensions (e.g., .xsjs, .xsjslib).*

 * (1.2 years ago) **RyanCavanaugh** added labels `Suggestion`, `Awaiting More Feedback`
 * [21 weeks ago](https://github.com/microsoft/TypeScript/issues/60632#issuecomment-3415022801) **Labernator** said "This would help me a lot as well! I also have server side JS files with different endings than .js"
 * [today](https://github.com/microsoft/TypeScript/issues/60632#issuecomment-4085606617) **elibarzilay** argued that suffixes for TypeScript scripts are a bad idea because executables should be language-agnostic and require no suffix

### [Issue microsoft/TypeScript#63085](https://github.com/microsoft/TypeScript/issues/63085) (Open, `Planning`)

**TypeScript 6\.0 Iteration Plan**

*The TypeScript 6.0 iteration plan details milestone dates and scheduled compiler additions, language improvements, breaking changes, and deprecations.*

 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-4070606069) **typescript-bot** said "Hey, @DanielRosenwasser! I've set the version of release-6.0 to 6.0.2 for you."
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-4076617359) **webrcost4** summarized the TS 6.0 release changes and asked about breaking defaults, migration strategies, and adoption of stricter settings across large codebases
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-4076769397) **DanielRosenwasser** explained that iteration plans and pre-releases are intended for testing and that feedback should be provided in separate issues
 * [today](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-4087494508) **newives** reported that the TypeScript 6.0 Final Release job failed to launch
 * [today](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-4087508959) **jakebailey** said "That run is unrelated to a release."
 * [today](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-4087648587) **newives** asked if a specific release date was available

### [Issue microsoft/TypeScript#63264](https://github.com/microsoft/TypeScript/issues/63264) (Closed, `Duplicate`)

**Return statement required even when not needed**

*TypeScript incorrectly requires a return statement in an exhaustively covered function over a closed union, causing a missing return error.*

 * created by **eliashakuni**
 * [today](https://github.com/microsoft/TypeScript/issues/63264#issuecomment-4081968705) **MartinJohns** said "Duplicate of #21985."
 * **RyanCavanaugh** added label `Duplicate`

### [Issue microsoft/TypeScript#63266](https://github.com/microsoft/TypeScript/issues/63266) (Closed, `Duplicate`)

**Omit keyof any**

*Clarify why TypeScript defines Omit<T, K> with K extending keyof any instead of extending keyof T like Pick does.*

 * created by **fudom**
 * [today](https://github.com/microsoft/TypeScript/issues/63266#issuecomment-4082874384) **MartinJohns** said "Duplicate of #30825."
 * **RyanCavanaugh** added label `Duplicate`

### [PR microsoft/TypeScript#63267](https://github.com/microsoft/TypeScript/pull/63267) (Closed)

**Fix crash in visitEachChildOfIndexSignatureDeclaration when type is missing**

*Replace Debug.checkDefined with non-null assertion in visitEachChildOfIndexSignatureDeclaration to gracefully handle undefined types in malformed index signatures.*

 * created by **mango766**

### [Issue microsoft/TypeScript#63268](https://github.com/microsoft/TypeScript/issues/63268) (Closed, `Bug`, `Fixed`)

**Crash: TypeError: Cannot read properties of undefined \(reading 'flags'\) at tryGetDeclaredTypeOfSymbol when using typeof this in arrow function parameter**

*Using 'typeof this' in an arrow function parameter triggers a TypeError crash in the TypeScript compiler.*

 * created by **na7ure-a**

### [Issue microsoft/TypeScript#63269](https://github.com/microsoft/TypeScript/issues/63269) (Open, `Bug`, `Domain: check: Type Circularity`)

**Regression: RangeError: Maximum call stack size exceeded in instantiateTypeWorker with recursive intersections and invalid type queries**

*Recursive intersection and invalid type query patterns cause a RangeError maximum call stack size exceeded in instantiateTypeWorker in TypeScript 5.7.3 through 5.9.3 and nightly builds.*

 * created by **na7ure-a**

