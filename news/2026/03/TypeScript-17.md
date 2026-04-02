# Report for 2026-03-17 (Tuesday, March 17th, 2026)

14 different users commented on 17 different issues.

## Recommended Actions

 * Response Recommended
    * @webrcost4 asked which defaults are most likely to break existing projects, recommended migration strategies, and approaches to adopt stricter defaults in [microsoft/TypeScript#63085](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-4076617359)
    * @ackvf reported a bug specific to argument variable rendering in [microsoft/TypeScript#63143](https://github.com/microsoft/TypeScript/issues/63143#issuecomment-4083648015)

## Activity Summary

### [Issue microsoft/TypeScript#17002](https://github.com/microsoft/TypeScript/issues/17002) (Open, `Suggestion`, `In Discussion`, `Domain: lib.d.ts`, `Fix Available`)

**Array\.isArray type narrows to any\[\] for ReadonlyArray\<T\>**

*Array.isArray fails to correctly narrow a union including ReadonlyArray<T>, resulting in an any[] type instead of ReadonlyArray<T>.*

 * [7 weeks ago](https://github.com/microsoft/TypeScript/issues/17002#issuecomment-3784982171) **spalt08** offered another workaround using Array.isArray to define a readonly array type guard
 * [7 weeks ago](https://github.com/microsoft/TypeScript/issues/17002#issuecomment-3786996167) **cahnory** provided an alternative workaround using a type assertion for Array.isArray
 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/17002#issuecomment-3958701606) **niklasholm** suggested using `unknown` and augmenting ArrayConstructor.isArray via global declaration to avoid `any` or type assertions
 * [today](https://github.com/microsoft/TypeScript/issues/17002#issuecomment-4076378007) **slztfn** said "I believe @cahnory solution is the best one so far and it should be in the standard library"
 * [later](https://github.com/microsoft/TypeScript/issues/17002#issuecomment-4080971605) **cahnory** described augmenting ArrayConstructor.isArray to use a readonly unknown[] type guard, compared approaches, noted a minor type-narrowing difference, and expressed a preference for a dedicated helper over standard-library augmentation

### [Issue microsoft/TypeScript#22467](https://github.com/microsoft/TypeScript/issues/22467) (Open, `Bug`, `Help Wanted`, `Domain: API`, `Good First Issue`, `PursuitFellowship`)

**getDefinitionAtPosition doesn't distinguish different kinds in a merged declaration**

*getDefinitionAtPosition incorrectly reports all merged declarations as class rather than distinguishing module, class, and interface*

 * [1 year ago](https://github.com/microsoft/TypeScript/issues/22467#issuecomment-2641282213) **ardentechne** reproduced the bug and provided detailed reproduction steps and sample code
 * **RyanCavanaugh** added label `Domain: API`
 * [yesterday](https://github.com/microsoft/TypeScript/issues/22467#issuecomment-4069921460) **ManishPrakkash** said "Checking in to see if this is still open for a PR? I’d like to help out with the requested changes"
 * [today](https://github.com/microsoft/TypeScript/issues/22467#issuecomment-4076261227) **paigefletcher1282-code** confirmed that the issue was fixed

### [Issue microsoft/TypeScript#27910](https://github.com/microsoft/TypeScript/issues/27910) (Open, `Suggestion`, `Help Wanted`, `Good First Issue`, `Domain: Error Messages`, `Experience Enhancement`, `PursuitFellowship`)

**TS2367: This condition will always return 'false' since the types 'Constructor\<T\>' and 'typeof Child' have no overlap\.**

*Comparing a generic constructor type Constructor<T> to the specific Child class always fails due to incompatible types, causing TS2367.*

 * [5.1 years ago](https://github.com/microsoft/TypeScript/issues/27910#issuecomment-761886530) **ETARAZ** demonstrated a working code snippet assigning t and using a ternary operator
 * [4.8 years ago](https://github.com/microsoft/TypeScript/issues/27910#issuecomment-836730432) **vsDizzy** provided better illustrations with two images
 * [yesterday](https://github.com/microsoft/TypeScript/issues/27910#issuecomment-4069922982) **ManishPrakkash** said "Checking in to see if this is still open for a PR? I’d like to help out with the requested changes"
 * [today](https://github.com/microsoft/TypeScript/issues/27910#issuecomment-4076259171) **paigefletcher1282-code** confirmed it worked for them now

### [Issue microsoft/TypeScript#4881](https://github.com/microsoft/TypeScript/issues/4881) (Open, `Suggestion`, `Needs Proposal`)

**Request: Class Decorator Mutation**

*Enable TypeScript to correctly type-check class decorators that add properties for mixins.*

 * [20 weeks ago](https://github.com/microsoft/TypeScript/issues/4881#issuecomment-3438211558) **matthew-dean** argued that TypeScript's class and decorator restrictions reflect maintainers' bias towards C#-style syntax and limit JavaScript's dynamic capabilities
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/4881#issuecomment-4014984624) **yhaskell** illustrated that Zod validation in function form works correctly and expressed expectation that decorator form should behave similarly, providing code examples
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/4881#issuecomment-4014984624) **yhaskell** illustrated that Zod validation in function form works correctly and expressed expectation that decorator form should behave similarly, providing code examples
 * [later](https://github.com/microsoft/TypeScript/issues/4881#issuecomment-4081810296) **cgauld** argued that decorated function types should reflect changes in function shape and that enforcing non-changing decorators belongs to linting tools
 * [later](https://github.com/microsoft/TypeScript/issues/4881#issuecomment-4081810296) **cgauld** argued that decorated function types should reflect changes in function shape and that enforcing non-changing decorators belongs to linting tools

### [PR microsoft/TypeScript#62350](https://github.com/microsoft/TypeScript/pull/62350) (Open, `For Uncommitted Bug`)

**Control flow analysis for destructured rests**

*Control flow analysis now correctly handles destructured rest properties in TypeScript.*

 * [24 weeks ago](https://github.com/microsoft/TypeScript/pull/62350#issuecomment-3353643706) **jakebailey** said "I feel fairly good about this PR, though I'm a bit shocked it didn't net anything in the extended tests."
 * [23 weeks ago](https://github.com/microsoft/TypeScript/pull/62350#issuecomment-3358443286) **jakebailey** said "@ahejlsberg Curious what you think of this."
 * [today](https://github.com/microsoft/TypeScript/pull/62350#issuecomment-4075129195) **nvmnghia** said "is this deferred until 7.0?"
 * [today](https://github.com/microsoft/TypeScript/pull/62350#issuecomment-4076471212) **jakebailey** said "Or later, because 6.0 is locked, and 7.0 will match 6.0 in behavior."

### [Issue microsoft/TypeScript#63085](https://github.com/microsoft/TypeScript/issues/63085) (Open, `Planning`)

**TypeScript 6\.0 Iteration Plan**

*The TypeScript 6.0 iteration plan details milestone dates and scheduled compiler additions, language improvements, breaking changes, and deprecations.*

 * [yesterday](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-4070560511) **DanielRosenwasser** said "@typescript-bot bump release-6.0"
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-4070560893) **typescript-bot** updated build status for bump release-6.0 jobs
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-4070606069) **typescript-bot** said "Hey, @DanielRosenwasser! I've set the version of release-6.0 to 6.0.2 for you."
 * [today](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-4076617359) **webrcost4** summarized the TS 6.0 release changes and asked about breaking defaults, migration strategies, and adoption of stricter settings across large codebases
 * [today](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-4076769397) **DanielRosenwasser** explained that iteration plans and pre-releases are intended for testing and that feedback should be provided in separate issues

### [Issue microsoft/TypeScript#63143](https://github.com/microsoft/TypeScript/issues/63143) (Open, `Suggestion`, `Awaiting More Feedback`)

**Add switch to disable \_var unused variable prevention**

*Add a tsconfig option to disable automatic ignoring of underscore-prefixed unused variables so the compiler still reports them to IDE.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/63143#issuecomment-3957255323) **guillaumebrunerie** explained that TypeScript errors and ESLint warnings both appear and suggested disabling noUnusedLocals and noUnusedParameters to rely solely on ESLint for consistent styling
 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/63143#issuecomment-3983613552) **ackvf** asked how to configure the IDE to always dim unused variables regardless of disabled extensions or suppressed rules
 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/63143#issuecomment-3986970398) **RyanCavanaugh** explained that the behavior had existed for a long time and that there was little appetite for changing it because it suited the vast majority of users
 * [later](https://github.com/microsoft/TypeScript/issues/63143#issuecomment-4083648015) **ackvf** observed inconsistent rendering of an unused function argument variable as opaque instead of dimmed

### [Issue microsoft/TypeScript#63251](https://github.com/microsoft/TypeScript/issues/63251) (Open, `Suggestion`, `Needs Proposal`)

**Mechanism to specify input source location to find \`package\.json\` instead of output source location when determining module format**

*Provide a mechanism to use source directory instead of output directory when locating package.json for NodeNext module resolution*

 * (yesterday) **RyanCavanaugh** added labels `Suggestion`, `Needs Proposal`
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63251#issuecomment-4069551483) **monsanto** said "Okay, I can workaround this."
 * [today](https://github.com/microsoft/TypeScript/issues/63251#issuecomment-4076264035) **paigefletcher1282-code** suggested adding the workaround to the docs

### [Issue microsoft/TypeScript#63253](https://github.com/microsoft/TypeScript/issues/63253) (Closed, `Docs`, **DanielRosenwasser**)

**Typo in TS 6\.0 blog post: \`temporal\.esnext\` should be \`esnext\.temporal\`**

*The TypeScript 6.0 blog post mistakenly instructs using temporal.esnext instead of the valid esnext.temporal library.*

 * created by **lgarron**
 * (yesterday) **RyanCavanaugh** added label `Docs`, and assigned to **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript/issues/63253#issuecomment-4077092808) **DanielRosenwasser** said "Fixed, thanks!"
 * (today) **DanielRosenwasser** closed the issue

### [Issue microsoft/TypeScript#63257](https://github.com/microsoft/TypeScript/issues/63257) (Closed, `Working as Intended`)

**Clauses instead of Classes**

*The TypeScript handbook mistakenly uses “Clauses” instead of “Classes” in its documentation.*

 * **RyanCavanaugh** added label `Working as Intended`
 * [today](https://github.com/microsoft/TypeScript/issues/63257#issuecomment-4075982744) **RyanCavanaugh** said "Not a typo; when you type class C implements Y, the implements Y part is called a "clause"."
 * (today) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript/issues/63257#issuecomment-4076234735) **paigefletcher1282-code** thanked the reporter and said they would take a look

### [Issue microsoft/TypeScript#63258](https://github.com/microsoft/TypeScript/issues/63258) (Closed)

**Unexpected inferred type when inferred constraint is union \[T extends \(infer I extends number \| infer U extends string\)\]**

*Conditional types using a union of infer constraints unexpectedly infer the string fallback instead of never.*

 * created by **seetyewsiang**
 * (today) **seetyewsiang** closed the issue
 * [today](https://github.com/microsoft/TypeScript/issues/63258#issuecomment-4075288801) **seetyewsiang** stated that adding parentheses fixed the issue and provided a TypeScript Playground link
 * [today](https://github.com/microsoft/TypeScript/issues/63258#issuecomment-4076239733) **paigefletcher1282-code** appreciated the detailed report as very helpful

### [Issue microsoft/TypeScript#63259](https://github.com/microsoft/TypeScript/issues/63259) (Open, `Duplicate`)

**Type narrowing incorrect when providing some function generics when default generics present**

*Functions with default generic parameters don’t correctly narrow union-based argument types when only some generics are explicitly provided.*

 * created by **ChromeQ**
 * [today](https://github.com/microsoft/TypeScript/issues/63259#issuecomment-4079131983) **MartinJohns** stated that generic type inference is all or none and marked the issue as duplicate of #26242

### [PR microsoft/TypeScript#63261](https://github.com/microsoft/TypeScript/pull/63261) (Closed, `dependencies`, `javascript`)

**Bump fast\-xml\-parser from 5\.4\.1 to 5\.5\.6**

*Upgrade fast-xml-parser from v5.4.1 to v5.5.6 for various bug fixes, performance improvements, and new features.*

 * created by **dependabot[bot]**
 * (today) **dependabot[bot]** added labels `dependencies`, `javascript`, `dependencies`, `javascript`

### [Issue microsoft/TypeScript#63263](https://github.com/microsoft/TypeScript/issues/63263) (Closed)

**Flow analusys error in unreachable code**

*TypeScript erroneously reports a ‘Function | null’ type error in code unreachable due to an early return*

 * created by **Busyrev**
 * [later](https://github.com/microsoft/TypeScript/issues/63263#issuecomment-4081341596) **MartinJohns** said "Duplicate of #26914."
 * [later](https://github.com/microsoft/TypeScript/issues/63263#issuecomment-4081412945) **Busyrev** said "Sorry, misclicked and closed as completed"
 * (later) **Busyrev** closed the issue
 * (later) **Busyrev** closed the issue

### [Issue microsoft/TypeScript#63264](https://github.com/microsoft/TypeScript/issues/63264) (Closed, `Duplicate`)

**Return statement required even when not needed**

*TypeScript incorrectly requires a return statement in an exhaustively covered function over a closed union, causing a missing return error.*

 * created by **eliashakuni**
 * [later](https://github.com/microsoft/TypeScript/issues/63264#issuecomment-4081968705) **MartinJohns** said "Duplicate of #21985."

### [Issue microsoft/TypeScript#63266](https://github.com/microsoft/TypeScript/issues/63266) (Closed, `Duplicate`)

**Omit keyof any**

*Clarify why TypeScript defines Omit<T, K> with K extending keyof any instead of extending keyof T like Pick does.*

 * created by **fudom**
 * [later](https://github.com/microsoft/TypeScript/issues/63266#issuecomment-4082874384) **MartinJohns** said "Duplicate of #30825."

