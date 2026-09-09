# Report for 2026-09-03 (Thursday, September 3rd, 2026)

19 different users commented on 64 different issues.

## Recommended Actions

 * Response Recommended
    * @LeonxLJX asked whether tsconfig.paths should support dot-prefixed directories or is a documented limitation in [microsoft/TypeScript#36922](https://github.com/microsoft/TypeScript/issues/36922#issuecomment-5536210016)
    * @LeonxLJX suggested confirming if the issue reproduces on TS 5.6+ and offered to draft a repro in [microsoft/TypeScript#37100](https://github.com/microsoft/TypeScript/issues/37100#issuecomment-5536209673)
    * @overlookmotel provided additional repro cases and root cause analysis in [microsoft/TypeScript#47410](https://github.com/microsoft/TypeScript/issues/47410#issuecomment-5539932480)
    * @LeonxLJX asked whether the ModuleReference type needs to be callable or propagate across dynamic imports in [microsoft/TypeScript#54022](https://github.com/microsoft/TypeScript/issues/54022#issuecomment-5536210336)
    * @lukpsaxo suggested adding special handling for workspace:* dependencies in tsbuildinfo in [microsoft/TypeScript#58433](https://github.com/microsoft/TypeScript/issues/58433#issuecomment-5537176011)

## Activity Summary

### [Issue microsoft/TypeScript#32111](https://github.com/microsoft/TypeScript/issues/32111) (Closed, `Bug`, `Needs More Info`, `Crash`, `Domain: Performance`, `Needs Human Review`)

**Language service OOM on lodash DT tests when batch compilation succeeds**

*Language service operations for lodash DefinitelyTyped tests cause out-of-memory errors even though batch compilation succeeds.*

 * [yesterday](https://github.com/microsoft/TypeScript/issues/32111#issuecomment-5511285423) **RyanCavanaugh** requested detailed repro information (source file, position, request type, and log or payload) to recreate the language-service request
 * (yesterday) **RyanCavanaugh** added labels `Needs Human Review`, `Needs More Info`
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript#33935](https://github.com/microsoft/TypeScript/issues/33935) (Closed, `Bug`, `Needs More Info`, `Crash`, `Domain: Parser`)

**Debug Failure\. Did not expect PropertyDeclaration to have an Identifier in its trivia**

*A debug assertion failure 'PropertyDeclaration identifier in trivia' frequently occurs (esp. in JSX) and may cause VS crashes.*

 * [yesterday](https://github.com/microsoft/TypeScript/issues/33935#issuecomment-5518914916) **RyanCavanaugh** requested source file, cursor position or diagnostic range, and exact getCodeFixes request or tsserver log to reproduce the PropertyDeclaration failure
 * (yesterday) **RyanCavanaugh** added labels `Needs Human Review`, `Needs More Info`
 * [today](https://github.com/microsoft/TypeScript/issues/33935#issuecomment-5532266812) **andrewbranch** said "We can probably assume this code path is no longer quite the same, and will show up differently in TS 7 telemetry if it's still a problem."
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript#36378](https://github.com/microsoft/TypeScript/issues/36378) (Closed, `Bug`, `Fixed`, `Domain: JSDoc`, `Needs Human Review`)

**Jsdoc @this show incorrect type  in inherited method**

*JSDoc @this annotation on a static create method always infers Base instead of preserving subclass types.*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [6.3 years ago](https://github.com/microsoft/TypeScript/issues/36378#issuecomment-623353162) **Raynos** said "I ran into this issue as well today expecting foo (this: T) and /** @this T */ foo() to behave the same."
 * **RyanCavanaugh** added label `Domain: JSDoc`
 * [today](https://github.com/microsoft/TypeScript/issues/36378#issuecomment-5528929574) **RyanCavanaugh** noted that TypeScript 5.0.0-dev.20230201 fixed the loss of JSDoc receiver types in emitDeclarationOnly builds and referenced PR #51149 and commit 42530c3c
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#36792](https://github.com/microsoft/TypeScript/issues/36792) (Closed, `Bug`, `Fixed`, `Domain: ES Modules`, `Needs Human Review`)

**Exported type merged with 'export \* as namespace\.\.\.' only exports type meaning\.**

*Support for merging an exported type with an export * as namespace re-export into a single combined value and type export.*

 * [5 years ago](https://github.com/microsoft/TypeScript/issues/36792#issuecomment-910363242) **jasonkuhrt** noted that their projects heavily use this pattern and lack tree shaking support, produce eslint warnings, and don't support re-exports, and expressed strong agreement
 * [4.9 years ago](https://github.com/microsoft/TypeScript/issues/36792#issuecomment-941277839) **nexsodev** described encountering missing type exports despite runtime functionality and provided code examples
 * **RyanCavanaugh** added label `Domain: ES Modules`
 * [today](https://github.com/microsoft/TypeScript/issues/36792#issuecomment-5531938079) **RyanCavanaugh** described that PR #50853 resolved the alias resolution issue and noted the diagnostic no longer appears in later versions
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#36874](https://github.com/microsoft/TypeScript/issues/36874) (Closed, `Bug`, `Fixed`, `Domain: check: Type Inference`, `Needs Human Review`)

**Should be possible to spread \`Parameters\` onto its function**

*TypeScript throws a missing iterator error when spreading a Parameters<F> tuple into a generic function call.*

 * [6 years ago](https://github.com/microsoft/TypeScript/issues/36874#issuecomment-685784593) **haggen** said "I'm still uncertain of how to achieve that in strict mode though."
 * [5.7 years ago](https://github.com/microsoft/TypeScript/issues/36874#issuecomment-735715641) **MartinJohns** said "As mentioned by @AlCalzone in #41728, this seems to work when replacing any with any[]."
 * **RyanCavanaugh** added label `Domain: Type Inference`
 * [today](https://github.com/microsoft/TypeScript/issues/36874#issuecomment-5532647824) **RyanCavanaugh** stated that the issue was fixed in TypeScript 5.4, noted that the code compiled without errors in 5.4.0-dev.20240219, and linked the change to PR #57122
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#36884](https://github.com/microsoft/TypeScript/issues/36884) (Closed, `Bug`, `Domain: This-Typing`, `Needs Human Review`)

**Not performing exhaustiveness checking for this**

*TypeScript doesn’t recognize that ‘this’ becomes never after an instanceof Foo check, causing a missing return error.*

 * [6.5 years ago](https://github.com/microsoft/TypeScript/issues/36884#issuecomment-589960764) **tadhgmister** clarified that TypeScript treats `this` like any other variable and that if/else narrowing to `never` still allows a possible branch, and demonstrated that only a discriminated-union switch shows the branch is unreachable
 * [6.5 years ago](https://github.com/microsoft/TypeScript/issues/36884#issuecomment-590251271) **nsmaciej** expressed surprise that instanceof appeared to perform structural checks and asked for rationale for that behavior
 * **RyanCavanaugh** added label `Domain: This-Typing`
 * [today](https://github.com/microsoft/TypeScript/issues/36884#issuecomment-5532859211) **RyanCavanaugh** explained that TS2366 is correct because `this` is a structural constraint and identified the issue as a duplicate of #33481
 * **RyanCavanaugh** added label `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#36922](https://github.com/microsoft/TypeScript/issues/36922) (Open, `Bug`, `Needs More Info`, `Domain: Module Resolution`, `Needs Human Review`)

**tsconfig paths not work if dir name start with dot\.**

*Tsconfig path aliases fail to resolve imports when mapped to a directory starting with a dot.*

 * [3.5 years ago](https://github.com/microsoft/TypeScript/issues/36922#issuecomment-1447628468) **aczekajski** described that the setup worked and suggested adding './.folder/**/*' to the tsconfig include and 'baseUrl': '.' to the tsconfig
 * [2.3 years ago](https://github.com/microsoft/TypeScript/issues/36922#issuecomment-2113483903) **johannes-lindgren** described that Storybook configuration files were not type-checked due to their location in `.storybook` and that adding `.storybook/**/*` to the include setting fixed it
 * **RyanCavanaugh** added label `Domain: Module Resolution`
 * [today](https://github.com/microsoft/TypeScript/issues/36922#issuecomment-5533031630) **RyanCavanaugh** requested complete tsconfig.json, exact compiler output, and project invocation details to diagnose the resolution failure
 * (today) **RyanCavanaugh** added labels `Needs Human Review`, `Needs More Info`
 * [today](https://github.com/microsoft/TypeScript/issues/36922#issuecomment-5536210016) **LeonxLJX** offered to fix the tsconfig.paths resolution bug and asked for maintainer guidance on intended behavior for dot-prefixed directories

### [Issue microsoft/TypeScript#36930](https://github.com/microsoft/TypeScript/issues/36930) (Closed, `Bug`, `Domain: check: Type Inference`, `Needs Human Review`)

**If you pass a generic type argument to another generic type, constraints cannot be inferred correctly\.**

*Passing a generic type parameter to another generic type prevents correct constraint inference in TypeScript.*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [6.5 years ago](https://github.com/microsoft/TypeScript/issues/36930#issuecomment-590058357) **ashidaharo** realized the issue title was wrong, clarified that the compiler can't infer conditional types for generic type arguments, wondered if this is a technical limit rather than a bug, and indicated they would keep the issue open
 * **RyanCavanaugh** added label `Domain: Type Inference`
 * [today](https://github.com/microsoft/TypeScript/issues/36930#issuecomment-5533199842) **RyanCavanaugh** noted the issue was a duplicate of #29939 and explained that conditional types remain deferred for unresolved type parameters with constraints as intended
 * **RyanCavanaugh** added label `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#37100](https://github.com/microsoft/TypeScript/issues/37100) (Open, `Bug`, `Needs More Info`, `Domain: check: Type Inference`, `Needs Human Review`)

**Any type is inferred when function input parameter is set to some value**

*TypeScript infers any for abc’s generic return type when its optional continuation parameter is undefined.*

 * (6.5 years ago) **RyanCavanaugh** added labels `Bug`, `Domain: Type Inference`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/37100#issuecomment-5533776289) **RyanCavanaugh** asked to provide project configuration and exact steps to reproduce the incorrect `any` typing
 * (today) **RyanCavanaugh** added labels `Needs Human Review`, `Needs More Info`
 * [today](https://github.com/microsoft/TypeScript/issues/37100#issuecomment-5536209673) **LeonxLJX** offered to take the issue and described the repro as a narrowed-then-reused trap, diagnosed the root cause in strict flow analysis, outlined workarounds, and suggested confirming reproduction on TS 5.6+ before drafting a focused repro

### [Issue microsoft/TypeScript#37103](https://github.com/microsoft/TypeScript/issues/37103) (Closed, `Bug`, `Domain: Mapped Types`, `Needs Human Review`)

**Bug: strictNullChecks \+ object spread \+ computed key**

*TypeScript strictNullChecks does not error when spreading an object and using a computed key assigning undefined to Record<string, string>*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [6.3 years ago](https://github.com/microsoft/TypeScript/issues/37103#issuecomment-620451407) **arnodb** described a related bug in TypeScript strict mode where spreading an object with an undefined property allows assignment that violates the target interface
 * **RyanCavanaugh** added label `Domain: Mapped Types`
 * [today](https://github.com/microsoft/TypeScript/issues/37103#issuecomment-5533935389) **RyanCavanaugh** identified the issue as a duplicate of another issue concerning computed property in object spread
 * **RyanCavanaugh** added label `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#37131](https://github.com/microsoft/TypeScript/issues/37131) (Closed, `Bug`, `Domain: API`, `Domain: Binder`, `Needs Human Review`)

**Reference to the function expression identifier in it's body has different symbol**

*In TypeScript 3.8+, running getSemanticDiagnostics causes a function expression’s identifier and its body references to resolve to different symbols.*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [6.5 years ago](https://github.com/microsoft/TypeScript/issues/37131#issuecomment-594740573) **RyanCavanaugh** clarified that symbol identity isn't guaranteed and suggested using declarations or the TS language service API's find-all-references functionality
 * **RyanCavanaugh** added label `Domain: Binder`
 * [today](https://github.com/microsoft/TypeScript/issues/37131#issuecomment-5534068063) **RyanCavanaugh** explained that symbol object identity is not guaranteed and recommended using declarations or the language service find-references API, and noted that the TypeScript 6 JavaScript Compiler API is deprecated in favor of the TypeScript 7 API
 * **RyanCavanaugh** added label `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#37142](https://github.com/microsoft/TypeScript/issues/37142) (Closed, `Bug`, `Domain: classes`, `Needs Human Review`)

**A mixin class must have a constructor with a single rest parameter of type 'any\[\]'\.**

*Nested generic TypeScript mixins trigger error TS2545 stating mixin classes must have a constructor with a single rest parameter of type any[].*

 * [1.5 years ago](https://github.com/microsoft/TypeScript/issues/37142#issuecomment-2691196587) **CodeSmith32** asked whether a class decorator could be implemented without suppressing lint or TypeScript errors and requested working examples and a documentation fix
 * [1.2 years ago](https://github.com/microsoft/TypeScript/issues/37142#issuecomment-2889241202) **ZeroVocabulary** noted that passing dependencies via function parameters worked around lack of custom constructors, lamented TypeScript's limitation, and provided example code illustrating a mixin pattern
 * **RyanCavanaugh** added label `Domain: classes`
 * [today](https://github.com/microsoft/TypeScript/issues/37142#issuecomment-5534244407) **RyanCavanaugh** marked the issue as a duplicate of #16390 and noted that the generic returned-class case remained the concern
 * **RyanCavanaugh** added label `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#37301](https://github.com/microsoft/TypeScript/issues/37301) (Closed, `Bug`, `Fixed`, `Domain: classes`, `Needs Human Review`)

**Incorrect codegen and error detection for static property used as computed key in instance property of the same class**

*TypeScript 3.8.3 mishandles using a static class property as a computed instance key, causing compile-time and runtime errors.*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [6.5 years ago](https://github.com/microsoft/TypeScript/issues/37301#issuecomment-597227916) **mohsen1** said "This is probably intended because Chrome also throws the same runtime ReferenceError. "
 * **RyanCavanaugh** added label `Domain: classes`
 * [today](https://github.com/microsoft/TypeScript/issues/37301#issuecomment-5535073710) **RyanCavanaugh** reported that computed property name diagnostics were fixed in 5.4.0-dev.20231202 by PR #56514
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#37427](https://github.com/microsoft/TypeScript/issues/37427) (Closed, `Bug`, `Fixed`, `Help Wanted`, `Domain: Literal Types`, `Needs Human Review`)

**Destructured tuple elements are no longer literals**

*Destructuring a tuple returned by enumerate<Color>() causes its elements to lose literal types and widen to string*

 * (6.4 years ago) **RyanCavanaugh** added labels `help wanted`, `Domain: Literal Types`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/37427#issuecomment-5536784500) **RyanCavanaugh** reported that the issue was fixed in dev builds 6.0.0-dev.20251211 and current TypeScript following PR #62243
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#37505](https://github.com/microsoft/TypeScript/issues/37505) (Closed, `Bug`, `Fixed`, `Domain: Indexed Access Types`, `Needs Human Review`)

**Iteration using for of does not recognize optional arrays in generic mapped types**

*TypeScript incorrectly rejects for-of iteration on a generic optional array with fallback in mapped types*

 * (6.4 years ago) **RyanCavanaugh** added labels `Bug`, `Domain: Indexed Access Types`, and set milestone to `Backlog`
 * [later](https://github.com/microsoft/TypeScript/issues/37505#issuecomment-5537013277) **RyanCavanaugh** reported that the issue was fixed in TypeScript 4.8.0-dev.20220601 by PR #49330 changing the `a || b` type under `--strictNullChecks`
 * (later) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#37758](https://github.com/microsoft/TypeScript/issues/37758) (Closed, `Bug`, `Fixed`, `Domain: JSDoc`, `Needs Human Review`)

**JSDoc Object\.\<key, value\> Syntax doesn't suport uppercase key type**

*VSCode JSDoc intellisense fails to parse uppercase object key and value types such as Object.<String, Number>.*

 * (6.3 years ago) **RyanCavanaugh** added label `Domain: JSDoc`, and set milestone to `Backlog`
 * [4.6 years ago](https://github.com/microsoft/TypeScript/issues/37758#issuecomment-1001605328) **jespertheend** pointed out that JSDoc index signatures ignore key types other than number or string and demonstrated it with examples
 * [later](https://github.com/microsoft/TypeScript/issues/37758#issuecomment-5538176924) **RyanCavanaugh** explained that the issue was fixed in the current native TypeScript 7.1.0-dev, detailed the updated hover type reports for object types, and noted that a later issue was closed as a duplicate
 * (later) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#37760](https://github.com/microsoft/TypeScript/issues/37760) (Open, `Bug`, `Help Wanted`, `Domain: Parser`)

**Parsing issue for call expression with type arguments following left\-shift**

*Using the left-shift operator before a generic call expression in TypeScript causes parsing ambiguity that breaks syntax highlighting.*

 * **sandersn** added label `GraceHopperOSD`
 * (46 weeks ago) **RyanCavanaugh** added label `Domain: Parser`, and removed label `PursuitFellowship`
 * (later) **RyanCavanaugh** added label `Needs Human Review`, and removed label `Needs Human Review`

### [Issue microsoft/TypeScript#38052](https://github.com/microsoft/TypeScript/issues/38052) (Closed, `Bug`, `Domain: check: Type Inference`, `Needs Human Review`)

**Type of function field of union object types not inferred correctly when infer is based on undefined type**

*TypeScript infers a union object's function parameter as any instead of narrowing when its discriminant property is missing.*

 * (6.3 years ago) **RyanCavanaugh** added labels `Bug`, `Domain: Type Inference`, and set milestone to `Backlog`
 * [later](https://github.com/microsoft/TypeScript/issues/38052#issuecomment-5539433901) **RyanCavanaugh** noted that this is the same optional-discriminant contextual typing issue tracked by #31618 and that omitting the optional `false` discriminant leaves the callback parameter typed as `any`
 * **RyanCavanaugh** added label `Needs Human Review`
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#38145](https://github.com/microsoft/TypeScript/issues/38145) (Closed, `Bug`, `Fixed`, `Domain: Binder`, `Needs Human Review`)

**Generic interface confuses parameter identifier with symbolic property identifier**

*TypeScript reports duplicate identifier errors when a generic type parameter name matches an enum property name in an interface.*

 * (6.2 years ago) **RyanCavanaugh** added labels `Bug`, `Domain: Binder`, and set milestone to `Backlog`
 * [later](https://github.com/microsoft/TypeScript/issues/38145#issuecomment-5539943245) **RyanCavanaugh** noted that the issue was fixed in 5.5.0-dev.20240327 and TypeScript 7.1.0-dev.20260904.1 via PR #57717
 * (later) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#38246](https://github.com/microsoft/TypeScript/issues/38246) (Closed, `Bug`, `Domain: JS Emit`, `Needs Human Review`)

**Function name not preserved when exported on definition**

*Exporting an arrow function directly causes the compiler to emit an anonymous function, stripping its inferred name and making .name empty.*

 * (6.3 years ago) **RyanCavanaugh** added labels `Bug`, `Domain: JS Emit`, and set milestone to `Backlog`
 * [later](https://github.com/microsoft/TypeScript/issues/38246#issuecomment-5540164453) **RyanCavanaugh** explained that the issue was the same exported-arrow-function naming problem tracked by issue #6433 due to downlevel module emit assigning an anonymous function to an export property preventing name inference
 * **RyanCavanaugh** added label `Needs Human Review`
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#38391](https://github.com/microsoft/TypeScript/issues/38391) (Closed, `Bug`, `Help Wanted`, `Domain: API`, `Needs Human Review`)

**\`typeChecker\.getTypeArguments\` returns unexpected extra type argument**

*typeChecker.getTypeArguments returns an extra subclass type parameter in addition to the expected generic argument*

 * [5.2 years ago](https://github.com/microsoft/TypeScript/issues/38391#issuecomment-856311996) **RyanCavanaugh** said "This does seem wrong"
 * (5.2 years ago) **RyanCavanaugh** added labels `help wanted`, `Domain: API`
 * [later](https://github.com/microsoft/TypeScript/issues/38391#issuecomment-5541281934) **RyanCavanaugh** explained that typeChecker.getTypeArguments was part of a superseded pre-TypeScript-7 API and is no longer actionable
 * **RyanCavanaugh** added label `Needs Human Review`
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#38448](https://github.com/microsoft/TypeScript/issues/38448) (Closed, `Bug`, `Fixed`, `Domain: Something Else`, `Needs Human Review`)

**Maps are not properly displayed on typescript playground**

*Map objects are rendered as empty objects in the TypeScript Playground console instead of showing their entries.*

 * (6.3 years ago) **RyanCavanaugh** added labels `Bug`, `Domain: Something Else`, and set milestone to `Backlog`
 * [later](https://github.com/microsoft/TypeScript/issues/38448#issuecomment-5542815431) **RyanCavanaugh** described that the Playground now reports console.log(m) as a Map(1) with a size: 1 preview instead of {} and that the original example has the expected Map representation
 * (later) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#47410](https://github.com/microsoft/TypeScript/issues/47410) (Open, `Bug`, `Help Wanted`, `Domain: Parser`)

**Bad parsing behaviour for generic arrow type arguments in class heritage / JSX open element**

*TypeScript incorrectly parses generic arrow function type arguments in class heritage and JSX elements.*

 * (4.6 years ago) **RyanCavanaugh** added labels `Help Wanted`, `Domain: Parser`, and set milestone to `Backlog`
 * [later](https://github.com/microsoft/TypeScript/issues/47410#issuecomment-5539932480) **overlookmotel** reproduced the parsing failure on TypeScript 6.0.3, demonstrated additional affected positions (implements, extends, typeof), showed that inserting a space fixes the parse, and pinpointed the root cause in missing reScanLessThanToken calls

### [Issue microsoft/TypeScript#54022](https://github.com/microsoft/TypeScript/issues/54022) (Open, `Suggestion`, `Awaiting More Feedback`)

**Add an intrinsic "module reference" types that allow definition of type\-checked module path strings and return types**

*Add an intrinsic module reference type for type-checking module path strings and their return types in TypeScript*

 * [3.3 years ago](https://github.com/microsoft/TypeScript/issues/54022#issuecomment-1522826112) **fatcerberus** critiqued the phrasing
 * (3.2 years ago) **RyanCavanaugh** added labels `Suggestion`, `Awaiting More Feedback`
 * [today](https://github.com/microsoft/TypeScript/issues/54022#issuecomment-5536210336) **LeonxLJX** offered to implement an intrinsic ModuleReference type, explained the design gap around treating module specifiers as opaque strings, outlined alternative approaches, and asked whether the type should be callable or support dynamic-import propagation

### [Issue microsoft/TypeScript#58433](https://github.com/microsoft/TypeScript/issues/58433) (Open, `Suggestion`, `Awaiting More Feedback`)

**Compiler Option to monitor external dependencies**

*Add a compilerOptions.dependencyTracking setting to enable incremental build monitoring of external dependencies.*

 * (2.2 years ago) **RyanCavanaugh** added labels `Suggestion`, `Awaiting More Feedback`
 * [1.7 years ago](https://github.com/microsoft/TypeScript/issues/58433#issuecomment-2476359202) **JasonKleban** noted that errors only appear after cleaning tsconfig.tsbuildinfo and asked whether incremental builds track dependency changes
 * [later](https://github.com/microsoft/TypeScript/issues/58433#issuecomment-5537176011) **lukpsaxo** highlighted issues with TS incremental builds in monorepos without project references and suggested treating workspace:* dependencies specially to trigger recompilation

### [Issue microsoft/TypeScript#63875](https://github.com/microsoft/TypeScript/issues/63875) (Open, `Suggestion`, `Committed`, **andrewbranch**)

**API feature roadmap**

*API feature roadmap for TypeScript 7.1 outlining plugin replacements and top-level utilities with rough cost estimates.*

 * [yesterday](https://github.com/microsoft/TypeScript/issues/63875#issuecomment-5513828692) **andrewbranch** described removal of openPrimaryProject call in transpileOnly mode and reported performance improvements and detailed the core patch changes
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63875#issuecomment-5514520912) **johnnyreilly** said "Thanks @andrewbranch! I've applied the git diff and pushed I'll take a look at your other suggestions tomorrow!"
 * [today](https://github.com/microsoft/TypeScript/issues/63875#issuecomment-5522708727) **johnnyreilly** reported that the PR branch did not reliably improve build times and provided detailed benchmark results for Mac, Ubuntu, and Windows
 * [today](https://github.com/microsoft/TypeScript/issues/63875#issuecomment-5531936803) **andrewbranch** said "These are at least much better than your first table 😄 I think we can probably find more significant improvements, but I won't be able to dig into this more until after the beta release."
 * [today](https://github.com/microsoft/TypeScript/issues/63875#issuecomment-5532005314) **andrewbranch** announced intent to hide past conversations and previewed a significant refactor causing breaking changes and linked to issue for details

### [Issue microsoft/TypeScript#63892](https://github.com/microsoft/TypeScript/issues/63892) (Closed, `Needs Investigation`, **andrewbranch**)

**API: \`Node\` is missing \`getChildren\(\)\`, \`getFirstToken\(\)\`, \`getLastToken\(\)\` and related getters**

*The native Node API is missing child and token accessor methods like getChildren, getChildCount, getChildAt, getFirstToken, and getLastToken.*

 * created by **oMatheusmol**
 * (2 weeks ago) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#63893](https://github.com/microsoft/TypeScript/pull/63893) (Closed, `For Uncommitted Bug`, **andrewbranch**)

**API: add getChildren and token getters to Node**

*Add getChildren, getChildCount, getChildAt, getFirstToken, and getLastToken methods to the native TypeScript Node API.*

 * (2 weeks ago) **typescript-automation[bot]** added label `For Uncommitted Bug`, and assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript/pull/63893#issuecomment-5522334962) **oMatheusmol** implemented requested changes, replaced childrenCache with a plain Map, used a shared scanner in getChildren, removed the consumed set, skipped reparsed subtrees, and added 16 .js/.jsx test cases
 * [today](https://github.com/microsoft/TypeScript/pull/63893#issuecomment-5529257798) **oMatheusmol** said "my bad, I forgot to run dprint fmt, haha"
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#64027](https://github.com/microsoft/TypeScript/pull/64027) (Closed, `For Uncommitted Bug`)

**Escape unique\-symbol names in TS4094 diagnostics**

*Properly escape internal unique-symbol names in TS4094 diagnostics to use Strada’s __@brand@1 format instead of raw sentinel characters.*

 * created by **javascript-unsafe**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/64027#issuecomment-5471743973) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (today) **javascript-unsafe** closed the issue

### [PR microsoft/TypeScript#64115](https://github.com/microsoft/TypeScript/pull/64115) (Open, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Add optional VFS parameters to updateSnapshot**

*Add optional VFS parameters to updateSnapshot with helpers for in-memory or layered file systems supporting fallback, symlinks, and removed paths.*

 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/64115#issuecomment-5496806376) **andrewbranch** expressed excitement about the feature, questioned whether the complementary file system use case exists, and worried that multiple access methods could be confusing
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/64115#issuecomment-5498184533) **weswigham** explained that file system layering can be implemented via callbacks and host fallback, recommending mounting `/project/node_modules` as a host mount into the in-memory VFS
 * [today](https://github.com/microsoft/TypeScript/pull/64115#issuecomment-5530854700) **andrewbranch** asked about renaming createCacheFileSystem to createOverlayFileSystem or createOverlays and mentioned planning other snapshot/state model changes
 * [today](https://github.com/microsoft/TypeScript/pull/64115#issuecomment-5532864937) **weswigham** suggested renaming functions to use "Layer" instead of "overlay" to avoid confusion with overlayFS on the backend

### [PR microsoft/TypeScript#64122](https://github.com/microsoft/TypeScript/pull/64122) (Closed, `For Uncommitted Bug`)

**chore: remove \`outFile\`,\`module:amd\` config from test cases**

*Remove outFile and AMD module test configurations and harness logic to reinstate coverage for previously skipped error code tests.*

 * [2 days ago](https://github.com/microsoft/TypeScript/pull/64122#issuecomment-5496947601) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/64122#issuecomment-5496990552) **camc314** said "Hmm actually this makes sense to just remove outFile from all fixtures so that they can start to be tested - i'll update this PR."
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64122#issuecomment-5506628420) **camc314** described fixes for the legacy outFile fixture removal and expanded unsupported compiler option skipping to cover fourslash configs
 * [today](https://github.com/microsoft/TypeScript/pull/64122#issuecomment-5530365880) **jakebailey** said "Thanks!"
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#64145](https://github.com/microsoft/TypeScript/issues/64145) (Closed)

**Completions inside tuple types suggest value symbols instead of types**

*TypeScript completions inside tuple type brackets incorrectly suggest value symbols like 'User' rather than only type symbols such as 'UserTuple'.*

 * created by **luo2430**
 * [today](https://github.com/microsoft/TypeScript/issues/64145#issuecomment-5526948029) **luo2430** said "https://github.com/microsoft/TypeScript/pull/64146"
 * (later) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64146](https://github.com/microsoft/TypeScript/pull/64146) (Closed, `For Uncommitted Bug`)

**Fix completions inside tuple types suggesting value symbols**

*Auto-completion inside tuple type definitions incorrectly suggests value symbols instead of type symbols.*

 * created by **luo2430**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64146#issuecomment-5526934710) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (later) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64150](https://github.com/microsoft/TypeScript/pull/64150) (Open, `For Uncommitted Bug`)

**API: add formatDiagnostic and flattenDiagnosticMessageText**

*Add formatDiagnostic and flattenDiagnosticMessageText helper functions to the API to fully restore v6.x per-diagnostic support.*

 * created by **oMatheusmol**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64150#issuecomment-5529033674) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."

### [Issue microsoft/TypeScript#64151](https://github.com/microsoft/TypeScript/issues/64151) (Closed)

**Add go\.mod file for pkg\.go\.dev support?**

*Add go.mod to enable pkg.go.dev version listings and allow fetching nightly releases.*

 * created by **trevorade**
 * [today](https://github.com/microsoft/TypeScript/issues/64151#issuecomment-5533032406) **jakebailey** explained that the code was in a nested module to avoid tag conflicts and allow versioning changes later, and linked to the pkg.go.dev documentation
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#64152](https://github.com/microsoft/TypeScript/issues/64152) (Open, `Bug`, `Breaking Change`, **DanielRosenwasser**, **Copilot**)

**No error when exporting from global augmentations**

*Exporting bindings introduced via global augmentations incorrectly succeeds instead of erroring like other non-local exports.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** added labels `Bug`, `Breaking Change`, and assigned to **Copilot**, **DanielRosenwasser**

### [PR microsoft/TypeScript#64153](https://github.com/microsoft/TypeScript/pull/64153) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Ban case blocks with just "break", top level break**

*Ban Go case blocks containing only a break statement and remove any redundant top-level break statements.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [Issue microsoft/TypeScript#64154](https://github.com/microsoft/TypeScript/issues/64154) (Open, `Domain: API`, **andrewbranch**)

**\[API\] Redesign client\-side snapshot state model**

*Redesign the client-side snapshot state model to unify overlapping updateSnapshot, createProgram, and virtual filesystem operations into a coherent transition system.*

 * created by **andrewbranch**
 * (today) **andrewbranch** set milestone to `TypeScript 7.1.0 Beta`, and assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript/issues/64154#issuecomment-5532599380) **DanielRosenwasser** discussed naming options for the snapshot function and weighed potential misinterpretations
 * [today](https://github.com/microsoft/TypeScript/issues/64154#issuecomment-5532977627) **DanielRosenwasser** asked whether dirty meant the program was out of date with respect to disk after applying changes
 * [today](https://github.com/microsoft/TypeScript/issues/64154#issuecomment-5533077334) **DanielRosenwasser** considered whether to expose a program update method without snapshot.update and suggested requiring snapshot.update or returning a [Program, Snapshot] pair

### [Issue microsoft/TypeScript#64155](https://github.com/microsoft/TypeScript/issues/64155) (Open, **jakebailey**, **Copilot**)

**Should the native TypeScript LSP include top\-level imports in its \`textDocument/documentSymbol\` response?**

*Clarify whether the native TypeScript language server should exclude top-level imports from documentSymbol results as VS Code currently does.*

 * created by **colecrouter**
 * [today](https://github.com/microsoft/TypeScript/issues/64155#issuecomment-5533063216) **jakebailey** clarified that the filtering was unintentional due to VS Code's TS extension and asked what Visual Studio expects
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript#64156](https://github.com/microsoft/TypeScript/pull/64156) (Closed, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Add tools/custom\-gcl\.exe\.hash to \.gitignore**

*Add tools/custom-gcl.exe.hash to .gitignore to ignore locally generated lint build output.*

 * created by **weswigham**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **weswigham**
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript#64157](https://github.com/microsoft/TypeScript/pull/64157) (Closed, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Add defer functionality to generator executor**

*Implement a defer function in the api.batch generator executor to queue non-blocking tasks in the current batch context.*

 * created by **weswigham**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **weswigham**

### [PR microsoft/TypeScript#64158](https://github.com/microsoft/TypeScript/pull/64158) (Open, `Author: Team`, `For Uncommitted Bug`, **iisaduan**)

**Build Orchestrator API **

*Implement a new BuildOrchestrator API with build, buildReferences, clean, and cleanReferences methods replacing SolutionBuilder*

 * created by **iisaduan**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`, and assigned to **iisaduan**

### [PR microsoft/TypeScript#64159](https://github.com/microsoft/TypeScript/pull/64159) (Open, `Author: Team`, `For Milestone Bug`, **jakebailey**)

**Strongly type file paths**

*Add branded types for absolute, normalized file and directory paths to enforce path invariants and reduce normalization overhead.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Milestone Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#64160](https://github.com/microsoft/TypeScript/pull/64160) (Open, `For Uncommitted Bug`, **jakebailey**, **Copilot**)

**Exclude top\-level imports from document symbols**

*Modify LSP documentSymbol results to omit top-level import and import-equals declarations, aligning with VS Code Outline behavior.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`

### [PR microsoft/TypeScript#64161](https://github.com/microsoft/TypeScript/pull/64161) (Closed, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Add a \`npx hereby validate\` command to group all repo validations**

*Introduce an npx hereby validate command to run and manage all repository validations in a single step.*

 * created by **weswigham**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **weswigham**

### [PR microsoft/TypeScript#64162](https://github.com/microsoft/TypeScript/pull/64162) (Open, `For Uncommitted Bug`, **DanielRosenwasser**, **Copilot**)

**Reject exports from global augmentations**

*Prevent export statements from exporting variables declared inside declare global augmentation blocks.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [PR microsoft/TypeScript#64163](https://github.com/microsoft/TypeScript/pull/64163) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**Decouple snapshot ownership from project\.Session so api\.Session only uses one in LSP mode**

*Extract snapshot cloning and caching into a new host to decouple api.Session from project.Session in LSP mode.*

 * created by **andrewbranch**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **andrewbranch**

### [PR microsoft/TypeScript#64164](https://github.com/microsoft/TypeScript/pull/64164) (Closed, `For Uncommitted Bug`)

**Handle tuple rest parameters in legacy decorator arity checks**

*Modify legacy decorator arity checks to correctly handle tuple rest parameters and eliminate spurious TS1241 errors.*

 * created by **Andarist**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/64164#issuecomment-5536950309) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."

### [PR microsoft/TypeScript#64165](https://github.com/microsoft/TypeScript/pull/64165) (Closed, `For Backlog Bug`)

**Fix crash on private constructors in intersection base types**

*Fix compiler crash triggered by private constructors in intersection base types*

 * created by **Andarist**
 * (later) **typescript-automation[bot]** added labels `For Backlog Bug`, `For Backlog Bug`

### [Issue microsoft/TypeScript#64166](https://github.com/microsoft/TypeScript/issues/64166) (Open, `Bug`, **andrewbranch**)

**\`getCompletionsAtPosition\` in API deadlocks when used with \`includeSymbol: true\`**

*getCompletionsAtPosition deadlocks when includeSymbol:true is set due to reuse of the persistent TypeScript checker*

 * created by **auvred**

### [Issue microsoft/TypeScript#64167](https://github.com/microsoft/TypeScript/issues/64167) (Closed, `Question`)

**LSP completion echoes the unresolved identifier currently being typed as a Text item**

*TypeScript's LSP server returns unresolved Text completions identical to the typed identifier, creating useless no-op suggestion entries.*

 * created by **kuator**

### [Issue microsoft/TypeScript#64168](https://github.com/microsoft/TypeScript/issues/64168) (Open, `Bug`)

**\`getChildren\(\)\` drops the \`\<\` token of a type argument list when immediately followed by another \`\<\`**

*getChildren() removes the first '<' in a '<<' type argument list, causing a gap in AST children*

 * created by **overlookmotel**

### [PR microsoft/TypeScript#64169](https://github.com/microsoft/TypeScript/pull/64169) (Open, `For Backlog Bug`)

**Preserve \`\<\` in \`getChildren\(\)\` when type arguments begin with \`\<\`**

*Update getChildren() to preserve the leading “<” token when type arguments begin with “<”*

 * created by **Andarist**
 * (later) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`

### [PR microsoft/TypeScript#64170](https://github.com/microsoft/TypeScript/pull/64170) (Closed, `For Backlog Bug`)

**fix\(checker\): don't emit typeof for private\-named static methods**

*Declaration emitter avoids generating typeof references for private-named static methods, preventing invalid declaration syntax by using structural type fallbacks.*

 * created by **ekalinin**
 * (later) **typescript-automation[bot]** added labels `For Backlog Bug`, `For Backlog Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/64170#issuecomment-5542763837) **ekalinin** requested that the contributor agree to the Contributor License Agreement by replying with the appropriate bot command

### [Issue microsoft/TypeScript#64171](https://github.com/microsoft/TypeScript/issues/64171) (Open, `Bug`)

**\[Auto\-import\] Quick Fix suggests invalid module specifiers that fail to resolve at runtime**

*Quick Fix auto-import suggests module specifiers that don't resolve at runtime under nodenext import conditions.*

 * created by **alexicum**

