# Report for 2026-11-21 (Saturday, November 21st, 2026)

11 different users commented on 47 different issues.

## Recommended Actions

 * Response Recommended
    * @Plecra proposed a technical approach to reachability analysis and handling unreachable code that maintainers should acknowledge in [microsoft/TypeScript#26914](https://github.com/microsoft/TypeScript/issues/26914#issuecomment-7080495698)

## Activity Summary

### [Issue microsoft/TypeScript#21733](https://github.com/microsoft/TypeScript/issues/21733) (Open, `Bug`, `Domain: check: Type Inference`, `Domain: check: Order Dependence`)

**Differing results for inference produced when identical overload count changes**

*Identical generic overloads produce inconsistent inference results, incorrectly widening the inferred type from Derived to Base.*

 * (8.2 years ago) **RyanCavanaugh** added label `Domain: Type Inference`, set milestone to `Future`, and unassigned **weswigham**
 * **jakebailey** added label `Domain: check: Order Dependence`

### [Issue microsoft/TypeScript#26914](https://github.com/microsoft/TypeScript/issues/26914) (Open, `Bug`, `Domain: check: Control Flow`)

**Control flow analysis should "work" in unreachable code**

*TypeScript should perform control-flow narrowing in unreachable code instead of reporting impossible errors after an unconditional return.*

 * [1.8 years ago](https://github.com/microsoft/TypeScript/issues/26914#issuecomment-2611476848) **difhel** provided TypeScript reproduction code showing that unreachable code failed to preserve nullability narrowing after an early return or throw, and asked whether unreachable code should be analyzed
 * [1.8 years ago](https://github.com/microsoft/TypeScript/issues/26914#issuecomment-2613114032) **RyanCavanaugh** explained why unreachable code should still be analyzed and recommended using an unrecognized control-flow construct for debugging
 * **RyanCavanaugh** added label `Domain: Control Flow`
 * [later](https://github.com/microsoft/TypeScript/issues/26914#issuecomment-7080495698) **Plecra** outlined a proposition-based control-flow and reachability analysis model for TypeScript type checking, including how unreachable code could be represented

### [Issue microsoft/TypeScript#29479](https://github.com/microsoft/TypeScript/issues/29479) (Open, `Bug`, `Domain: check: Type Inference`, `Domain: check: Order Dependence`)

**Generic not inferred inside mapped type parameter**

*TypeScript fails to infer the state generic when passing selectors through a mapped type parameter, incorrectly inferring it as `{}`.*

 * [7.2 years ago](https://github.com/microsoft/TypeScript/issues/29479#issuecomment-526895952) **RyGuy101** shared a curried TypeScript workaround that allowed specifying only the first parameter when creating structured selectors
 * [6.8 years ago](https://github.com/microsoft/TypeScript/issues/29479#issuecomment-583680187) **borispinus** said "now it's unknown, not {}. Is it typescript bug that in this case unknown and State are not compatible? Or expected behavior?"
 * [2.6 years ago](https://github.com/microsoft/TypeScript/issues/29479#issuecomment-2017530683) **Andarist** demonstrated that adding an unused parameter to `Selector` enabled inline selector type inference, while removing it caused both cases to fail
 * **jakebailey** added label `Domain: check: Order Dependence`

### [Issue microsoft/TypeScript#30712](https://github.com/microsoft/TypeScript/issues/30712) (Open, `Bug`, `Domain: check: Type Inference`, `Domain: check: Order Dependence`)

**TS 3\.4: Error when passing dynamically imported generic type as a function argument**

*TypeScript 3.4 incorrectly infers dynamically imported generic component types as `never`, causing function argument type errors.*

 * [5.3 years ago](https://github.com/microsoft/TypeScript/issues/30712#issuecomment-883732371) **ctoth** said "Was lead here experiencing this exact issue. Nothing really useful to say other than that."
 * [3 years ago](https://github.com/microsoft/TypeScript/issues/30712#issuecomment-1794284686) **ibanlopez** asked whether the issue was still being moved from version 3.6 to version 5
 * **RyanCavanaugh** added label `Domain: Type Inference`
 * **jakebailey** added label `Domain: check: Order Dependence`

### [Issue microsoft/TypeScript#31081](https://github.com/microsoft/TypeScript/issues/31081) (Open, `Needs Investigation`, `Domain: check: Order Dependence`, **rbuckton**)

**Weird inference bug where a union is expanded with "never" in the position of generics**

*TypeScript 3.4 incorrectly infers an extra `(props: never)` union branch for generic component promises, breaking otherwise valid type checking.*

 * created by **calebmer**
 * (7.5 years ago) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **rbuckton**
 * **jakebailey** added label `Domain: check: Order Dependence`

### [Issue microsoft/TypeScript#36005](https://github.com/microsoft/TypeScript/issues/36005) (Open, `Bug`, `Domain: This-Typing`, `Domain: check: Order Dependence`)

**this type in conditional type false clause is incorrectly typed**

*TypeScript incorrectly widens `this` to the conditional type’s constraint in the false branch instead of using the declared `{ b: 1 }` type.*

 * (6.8 years ago) **RyanCavanaugh** added labels `Bug`, `Domain: This-Typing`, and set milestone to `Backlog`
 * **jakebailey** added label `Domain: check: Order Dependence`

### [Issue microsoft/TypeScript#38354](https://github.com/microsoft/TypeScript/issues/38354) (Open, `Needs Investigation`, `Domain: check: Order Dependence`)

**Incremental type checking failure \(regression\)**

*Incremental type checking incorrectly reports a type incompatibility after undoing a temporary syntax error in TypeScript 3.7 development builds.*

 * (6.5 years ago) **RyanCavanaugh** added label `Needs Investigation`, and set milestone to `Backlog`
 * [6.5 years ago](https://github.com/microsoft/TypeScript/issues/38354#issuecomment-625607250) **falsandtru** reported a VSCode-only TypeScript error where `HTML('custom-tag')` rejected a custom tag after an initial error, and identified a conflict between `ShadowHostElementTagNameMap` and `HTMLElementTagNameMap` declarations
 * **jakebailey** added label `Domain: check: Order Dependence`

### [Issue microsoft/TypeScript#41213](https://github.com/microsoft/TypeScript/issues/41213) (Open, `Bug`, `Domain: This-Typing`, `Domain: check: Order Dependence`)

**Union of functions with typed \`this\`, fails with no parameters**

*TypeScript fails to contextually type `this` for parameterless functions assigned to unions of function types with typed `this` parameters.*

 * [5.8 years ago](https://github.com/microsoft/TypeScript/issues/41213#issuecomment-766291330) **Zzzen** said "possible related to https://github.com/microsoft/TypeScript/issues/37580"
 * (1 year ago) **RyanCavanaugh** added label `Domain: This-Typing`, and removed label `Help Wanted`
 * **jakebailey** added label `Domain: check: Order Dependence`

### [Issue microsoft/TypeScript#41456](https://github.com/microsoft/TypeScript/issues/41456) (Open, `Bug`, `Domain: check: Type Inference`, `Domain: check: Order Dependence`)

**Incomplete infer for generic types**

*TypeScript fails to infer the generic `Item` type as `string` when deriving it from a mapped loader configuration.*

 * [5 years ago](https://github.com/microsoft/TypeScript/issues/41456#issuecomment-945900704) **zbinlin** asked whether a TypeScript inference example involving an `unknown` parameter and return value represented the same problem
 * **RyanCavanaugh** added label `Domain: Type Inference`
 * [39 weeks ago](https://github.com/microsoft/TypeScript/issues/41456#issuecomment-3926053636) **Hideman42** reported incomplete TypeScript auto-inference in versions 5.9.3 and nightly 6.0.0, provided a Playground reproduction, and noted that explicitly supplying the generic type avoided the error
 * **jakebailey** added label `Domain: check: Order Dependence`

### [Issue microsoft/TypeScript#45286](https://github.com/microsoft/TypeScript/issues/45286) (Open, `Bug`, `Domain: check: Type Inference`, `Domain: check: Order Dependence`)

**Inferred type parameter does not satisfy constraint**

*TypeScript incorrectly infers a constrained generic parameter as `unknown`, violating its dependency on another inferred type parameter.*

 * (5.3 years ago) **RyanCavanaugh** added labels `Bug`, `Domain: Type Inference`, and set milestone to `Backlog`
 * **jakebailey** added label `Domain: check: Order Dependence`

### [Issue microsoft/TypeScript#48135](https://github.com/microsoft/TypeScript/issues/48135) (Open, `Needs Investigation`, `Domain: check: Order Dependence`)

**"Concreting" generic has behavior different from generic inferred via value**

*TypeScript rejects a generic indexed access function despite the index being inferred as a concrete key equivalent to its explicitly specialized counterpart.*

 * (4.7 years ago) **RyanCavanaugh** added label `Needs Investigation`, and set milestone to `Backlog`
 * [3.5 years ago](https://github.com/microsoft/TypeScript/issues/48135#issuecomment-1510615816) **Woodz** reported an incorrect TypeScript error message for a generic function returning `input ?? null` and provided a playground reproduction with the expected diagnostic
 * **jakebailey** added label `Domain: check: Order Dependence`

### [Issue microsoft/TypeScript#48855](https://github.com/microsoft/TypeScript/issues/48855) (Open, `Bug`, `Domain: check: Contextual Types`, `Domain: check: Order Dependence`)

**Contextual type of a property type not inferred with key remapping**

*TypeScript fails to contextually infer event property types in key-remapped mapped types, reporting callback parameters as implicit any.*

 * (4.5 years ago) **andrewbranch** added label `Bug`, and set milestone to `Backlog`
 * **RyanCavanaugh** added label `Domain: Contextual Types`
 * **jakebailey** added label `Domain: check: Order Dependence`

### [Issue microsoft/TypeScript#49459](https://github.com/microsoft/TypeScript/issues/49459) (Open, `Bug`, `Domain: Conditional Types`, `Domain: check: Order Dependence`)

**Tail recursion optimization limit 999 may be manipulated**

*Tail recursion optimization can be manipulated to bypass TypeScript’s 999-instantiation limit, producing incorrect `any` results instead of an error.*

 * [2.7 years ago](https://github.com/microsoft/TypeScript/issues/49459#issuecomment-1936907293) **ENvironmentSet** described how wrapping tail-recursive conditional types in an identity type bypassed the 1000-iteration limit, and traced the behavior to inconsistent `aliasSymbol` handling in the compiler’s `canTailRecurse` logic
 * (1 year ago) **RyanCavanaugh** added label `Domain: Conditional Types`, and removed label `Help Wanted`
 * **jakebailey** added label `Domain: check: Order Dependence`

### [Issue microsoft/TypeScript#50200](https://github.com/microsoft/TypeScript/issues/50200) (Open, `Bug`, `Domain: check: Order Dependence`, `Domain: check: Type Circularity`)

**Unexpected circular reference error TS7022**

*TypeScript incorrectly reports TS7022 for a JavaScript generic class instance whose inferred type references an object declared later.*

 * (3.5 years ago) **RyanCavanaugh** added labels `Help Wanted`, `Domain: Type Circularity`, and removed label `Help Wanted`
 * **jakebailey** added label `Domain: check: Order Dependence`

### [Issue microsoft/TypeScript#51434](https://github.com/microsoft/TypeScript/issues/51434) (Open, `Needs Investigation`, `Domain: check: Order Dependence`)

**Random reports of error 7022 \(implicitly has type 'any' because self\-reference\)**

*TypeScript 4.6+ intermittently reports error 7022 and loses property suggestions in callback code that worked correctly in 4.5.5.*

 * [3.4 years ago](https://github.com/microsoft/TypeScript/issues/51434#issuecomment-1604303875) **voliva** reported that the error no longer reproduced in version 5.0.4 and later, and asked whether to keep the issue open for investigation and a regression test
 * [2.8 years ago](https://github.com/microsoft/TypeScript/issues/51434#issuecomment-1885910576) **tobz1000** reported reproducing the issue with TypeScript 5.3.2 and provided a minimal code example showing that an explicit `undefined` assignment triggers the error while an uninitialized variable does not
 * [51 weeks ago](https://github.com/microsoft/TypeScript/issues/51434#issuecomment-3591758569) **Squidgical** reported another case where mutually referencing callbacks in generic `Record` objects incorrectly triggered circular-reference errors, despite the referenced expressions not affecting the inferred object types
 * **jakebailey** added label `Domain: check: Order Dependence`

### [Issue microsoft/TypeScript#52207](https://github.com/microsoft/TypeScript/issues/52207) (Open, `Bug`, `Domain: This-Typing`, `Domain: check: Order Dependence`)

**ThisType is invalid when using object spread on generic object**

*Object spread on a generic object causes its ThisType annotation to be inferred incorrectly.*

 * [3.8 years ago](https://github.com/microsoft/TypeScript/issues/52207#issuecomment-1381031964) **paul-thebaud** said "OK no problem. I'll wait for any update on this and notify this issue in my package for now. Thanks a lot for those explanation and triage."
 * (1 year ago) **RyanCavanaugh** added label `Domain: This-Typing`, and removed label `Help Wanted`
 * **jakebailey** added label `Domain: check: Order Dependence`

### [Issue microsoft/TypeScript#52432](https://github.com/microsoft/TypeScript/issues/52432) (Open, `Bug`, `Domain: check: Type Inference`, `Domain: check: Order Dependence`)

**Type variable not inferred correctly unless unused declaration is provided**

*TypeScript fails to infer a generic type and contextual `this` correctly unless an unrelated unused overload is declared.*

 * [3.7 years ago](https://github.com/microsoft/TypeScript/issues/52432#issuecomment-1445216242) **Andarist** explained that overload behavior depended on cached inference results and context-sensitive, non-inferrable types, and suggested expanding intra-expression site handling as a potential fix
 * (1 year ago) **RyanCavanaugh** added label `Domain: Type Inference`, and removed label `Help Wanted`
 * **jakebailey** added label `Domain: check: Order Dependence`

### [Issue microsoft/TypeScript#52969](https://github.com/microsoft/TypeScript/issues/52969) (Open, `Bug`, `Domain: This-Typing`, `Domain: check: Order Dependence`)

**【bug】ThisType is invalid when using param on generic object**

*TypeScript incorrectly rejects or mishandles `ThisType` when used with a parameter typed as a generic object.*

 * [3.7 years ago](https://github.com/microsoft/TypeScript/issues/52969#issuecomment-1447572766) **RyanCavanaugh** noted that inference had never been re-entrant as required by the example and expressed uncertainty about whether it was fixable
 * (1 year ago) **RyanCavanaugh** added label `Domain: This-Typing`, and removed label `Help Wanted`
 * **jakebailey** added label `Domain: check: Order Dependence`

### [Issue microsoft/TypeScript#54146](https://github.com/microsoft/TypeScript/issues/54146) (Open, `Bug`, `Domain: check: Big Unions`, `Domain: check: Order Dependence`)

**Type alias preserving logic defeats complexity reduction mechanisms**

*Type alias preservation fails to recognize identical expanded types, triggering erroneous complexity errors when intersecting duplicated large unions.*

 * (3.5 years ago) **weswigham** added labels `Bug`, `Domain: Big Unions`
 * **RyanCavanaugh** added to milestone `Backlog`
 * **jakebailey** added label `Domain: check: Order Dependence`

### [Issue microsoft/TypeScript#54550](https://github.com/microsoft/TypeScript/issues/54550) (Open, `Domain: Conditional Types`, `Possible Improvement`, `Domain: check: Order Dependence`)

**Generic Tuple Optional Parameter spread errors with Type instantiation is excessively deep and possibly infinite\. ts\(2589\)**

*TypeScript reports excessive instantiation depth when recursively spreading optional tuple parameters in a conditional type.*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [2.8 years ago](https://github.com/microsoft/TypeScript/issues/54550#issuecomment-1890380136) **13OnTheCode** provided a TypeScript `StringableParameters` utility type and a Playground link as a proposed solution
 * **RyanCavanaugh** added label `Domain: Conditional Types`
 * **jakebailey** added label `Domain: check: Order Dependence`

### [Issue microsoft/TypeScript#56459](https://github.com/microsoft/TypeScript/issues/56459) (Open, `Bug`, `Domain: check: Type Inference`, `Domain: check: Order Dependence`)

**Inference from annotated parameters of context\-sensitive functions is order dependent **

*TypeScript infers context-sensitive callback parameters differently depending on the object property order, causing the second call to fail.*

 * (3 years ago) **andrewbranch** added label `Bug`, and set milestone to `Backlog`
 * **RyanCavanaugh** added label `Domain: Type Inference`
 * **jakebailey** added label `Domain: check: Order Dependence`

### [Issue microsoft/TypeScript#57462](https://github.com/microsoft/TypeScript/issues/57462) (Open, `Needs Investigation`, `Domain: check: Order Dependence`, **rbuckton**)

**Control flow analysis gets confused by decorators**

*TypeScript’s control-flow analysis incorrectly reports errors for accessing `super` and initialized variables within decorated class fields.*

 * [2.7 years ago](https://github.com/microsoft/TypeScript/issues/57462#issuecomment-1956803556) **nicolo-ribaudo** reported another bug and provided a JavaScript reproduction involving decorators, class fields, and constructor execution
 * (2.7 years ago) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **rbuckton**
 * **jakebailey** added label `Domain: check: Order Dependence`

### [Issue microsoft/TypeScript#57706](https://github.com/microsoft/TypeScript/issues/57706) (Open, `Domain: check: Type Inference`, `Possible Improvement`, `Domain: check: Order Dependence`)

**Unexpected type infer for function first argument with default value since 5\.1**

*TypeScript 5.1 changed generic inference for functions with default-valued parameters, inconsistently inferring the first argument’s type.*

 * (2.6 years ago) **RyanCavanaugh** added label `Domain: Type Inference`, removed label `Help Wanted`, and set milestone to `Backlog`
 * **jakebailey** added label `Domain: check: Order Dependence`

### [Issue microsoft/TypeScript#57788](https://github.com/microsoft/TypeScript/issues/57788) (Open, `Domain: Mapped Types`, `Possible Improvement`, `Domain: check: Order Dependence`)

**Reverse mapped type inference fails to infer from annotated parameters in partially\-inferrable object types**

*Reverse mapped type inference fails to infer annotated parameter types for partially inferrable object properties, producing unknown instead of number.*

 * [2 years ago](https://github.com/microsoft/TypeScript/issues/57788#issuecomment-2461854056) **reucuer** said "ygg"
 * (1 year ago) **RyanCavanaugh** added label `Domain: Mapped Types`, and removed label `Help Wanted`
 * **jakebailey** added label `Domain: check: Order Dependence`

### [Issue microsoft/TypeScript#60544](https://github.com/microsoft/TypeScript/issues/60544) (Open, `Domain: check: Type Inference`, `Possible Improvement`, `Domain: check: Order Dependence`)

**NoInfer not working on callback parameter destructuring**

*NoInfer incorrectly infers `unknown` when a callback parameter is partially destructured, unlike when the parameter is omitted.*

 * (1.9 years ago) **RyanCavanaugh** added label `Domain: Type Inference`, removed label `Help Wanted`, and set milestone to `Backlog`
 * **jakebailey** added label `Domain: check: Order Dependence`

### [Issue microsoft/TypeScript#62220](https://github.com/microsoft/TypeScript/issues/62220) (Open, `Domain: check: Type Inference`, `Possible Improvement`, `Domain: check: Order Dependence`)

**\`as const\` breaks intra expression inference**

*Using `as const` on an object literal breaks contextual type inference for callback parameters, inferring `unknown` instead of the expected input type.*

 * (1.2 years ago) **RyanCavanaugh** added label `Domain: Type Inference`, removed label `Help Wanted`, and set milestone to `Backlog`
 * **jakebailey** added label `Domain: check: Order Dependence`

### [Issue microsoft/TypeScript#63776](https://github.com/microsoft/TypeScript/issues/63776) (Open, `Experimentation Needed`, `Domain: check: Order Dependence`, **RyanCavanaugh**, **Copilot**)

**Inconsistency involving discriminated union and flatMap**

*Go reports a TypeScript type inference error for a flatMap callback returning differently narrowed discriminated-union types, despite the equivalent code compiling in TypeScript.*

 * (13 weeks ago) **RyanCavanaugh** added label `Experimentation Needed`, and assigned to **Copilot**, **RyanCavanaugh**
 * **jakebailey** added label `Domain: check: Order Dependence`

### [Issue microsoft/TypeScript#64531](https://github.com/microsoft/TypeScript/issues/64531) (Open, `Possible Improvement`, `Domain: check: Order Dependence`)

**Support spread in recursive object inference**

*Support recursive object type inference when object literals include spread properties, avoiding implicit `any` errors and matching non-spread behavior.*

 * created by **colinhacks**
 * (7 weeks ago) **RyanCavanaugh** added label `Possible Improvement`, and set milestone to `Backlog`
 * **jakebailey** added label `Domain: check: Order Dependence`

### [PR microsoft/TypeScript#65064](https://github.com/microsoft/TypeScript/pull/65064) (Open, `Author: Team`, `For Milestone Bug`, `For Backlog Bug`, **jakebailey**)

**\[experiment\] fully order independent type checking**

*Overhauls type checking to produce consistent behavior regardless of traversal, file, cache, or cycle-processing order, with extensive randomized ordering tests.*

 * [3 days ago](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6993529747) **typescript-automation[bot]** reported that the DT tests produced a new d3-selection type-checking error in d3-selection-tests.ts at line 1502
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6993569229) **typescript-automation[bot]** reported new TypeScript TS7023 errors in Effect's SchemaAST.ts from the baseline-versus-PR user-test comparison and requested investigation
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6993846052) **typescript-automation[bot]** provided the requested performance results, showing increased symbols and memory usage in the Compiler-Unions benchmark
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-7075264612) **jakebailey** requested TypeScript bot runs for dt, user testing, top1000 testing, and performance testing
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-7075265819) **typescript-automation[bot]** said "Hey @jakebailey, this PR is in an unmergable state, so is missing a merge commit to run against; please resolve conflicts and try again."
 * [later](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-7077289128) **jakebailey** requested TypeScript bot runs for dt, user testing, top1000 testing, and performance testing
 * [later](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-7077290360) **typescript-automation[bot]** reported that automated jobs had started and linked to their build results
 * [later](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-7077606042) **typescript-automation[bot]** reported that the DT test results were ready and identified branch-only SuppressedError failures in the rdfjs__formats-common and jsonld packages
 * [later](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-7077760712) **typescript-automation[bot]** reported new TS7023 TypeScript errors in Effect's SchemaAST.ts when comparing baseline and PR user-test results, and asked the maintainer to investigate
 * [later](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-7077761260) **typescript-automation[bot]** reported additional user-test-suite TypeScript errors in webpack, including incorrect `LogType` usage and `WeakTupleMap`/`MemCache` incompatibilities
 * [later](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-7077869452) **typescript-automation[bot]** reported the requested performance-run results, including compiler metrics comparing the baseline with the pull request

### [Issue microsoft/TypeScript#65571](https://github.com/microsoft/TypeScript/issues/65571) (Closed, `Not a Defect`)

**Declaration emit drops the normalized optional properties of a union of object literals \(\`retries?: undefined\`\)**

*Declaration emit in TypeScript 7.x drops normalized optional properties from unions of object literals, causing consumers to incorrectly reject valid property access.*

 * created by **ktfth**
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/65571#issuecomment-7016512843) **RyanCavanaugh** explained that emitted declaration files do not always preserve source types because type syntax cannot represent certain differences between widened and unwidened object literal unions
 * **RyanCavanaugh** added label `Not a Defect`
 * [today](https://github.com/microsoft/TypeScript/issues/65571#issuecomment-7072012214) **github-actions[bot]** said "This issue has been marked as "Not a Defect" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **github-actions[bot]** closed the issue

### [Issue microsoft/TypeScript#65574](https://github.com/microsoft/TypeScript/issues/65574) (Closed, `Not a Defect`, **ahejlsberg**)

**7\.1 regression: type argument inferred from a union of callback types \(\`R\` \| \`Promise\<R \| void\>\`\) falls back to its constraint**

*TypeScript 7.1 regresses generic inference for unioned callback return types, falling back to the constraint and losing precise route response types.*

 * [2 days ago](https://github.com/microsoft/TypeScript/issues/65574#issuecomment-7024174478) **ahejlsberg** explained that the current behavior matched TypeScript 6.0, described related changes and reversions in TypeScript 7.0 and 7.1, and showed that simplifying the repro produced the expected behavior across compiler versions
 * (2 days ago) **ahejlsberg** added label `Not a Defect`, and removed label `Needs Investigation`
 * [today](https://github.com/microsoft/TypeScript/issues/65574#issuecomment-7072011922) **github-actions[bot]** said "This issue has been marked as "Not a Defect" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **github-actions[bot]** closed the issue

### [Issue microsoft/TypeScript#65607](https://github.com/microsoft/TypeScript/issues/65607) (Open, `Needs Investigation`, `Domain: check: Order Dependence`, **jakebailey**)

**Moving an unrelated \`new Schema\<T\>\(…, options\)\` above a mongoose model turns \`typeof Model extends Model\<infer R\>\` into \`never\`**

*An unrelated Mongoose schema’s declaration order causes TypeScript to infer `never` when extracting a model’s raw type via a conditional type.*

 * created by **jltrv**
 * (yesterday) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **jakebailey**
 * **jakebailey** added label `Domain: check: Order Dependence`

### [PR microsoft/TypeScript#65617](https://github.com/microsoft/TypeScript/pull/65617) (Closed, `Author: Team`, `For Milestone Bug`, **ahejlsberg**)

**Produce union types when instantiating generic contextual types**

*Produce union types instead of selecting individual inference candidates when instantiating generic contextual types inferred from return types.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/65617#issuecomment-7055837443) **jakebailey** said "Looks like some new errors in those benchmarks."
 * [yesterday](https://github.com/microsoft/TypeScript/pull/65617#issuecomment-7055889110) **ahejlsberg** said "@jakebailey It needed a merge from main."
 * [yesterday](https://github.com/microsoft/TypeScript/pull/65617#issuecomment-7056457477) **typescript-automation[bot]** reported that testing the top 400 repositories with `tsc` showed no differences between the baseline and PR and that everything looked good
 * [later](https://github.com/microsoft/TypeScript/pull/65617#issuecomment-7081111305) **ahejlsberg** said "@typescript-bot test it"
 * [later](https://github.com/microsoft/TypeScript/pull/65617#issuecomment-7081112351) **typescript-automation[bot]** reported that the requested test jobs started and provided links to their build results, with performance results still under review
 * [later](https://github.com/microsoft/TypeScript/pull/65617#issuecomment-7081461100) **typescript-automation[bot]** reported that the DT tests completed with unchanged results and provided a link to the build log
 * [later](https://github.com/microsoft/TypeScript/pull/65617#issuecomment-7081509378) **typescript-automation[bot]** reported that the user tests comparing the baseline and PR with tsc passed and everything looked good
 * [later](https://github.com/microsoft/TypeScript/pull/65617#issuecomment-7081653554) **typescript-automation[bot]** provided the requested performance results comparing the baseline and PR

### [PR microsoft/TypeScript#65621](https://github.com/microsoft/TypeScript/pull/65621) (Open, `Author: Team`, `For Backlog Bug`, **ahejlsberg**, **jakebailey**)

**Order types, symbols, and nodes by content instead of by ID**

*Order types, symbols, and nodes deterministically by content rather than creation IDs, interning identical types and eliminating ID-dependent output.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/65621#issuecomment-7059223121) **typescript-automation[bot]** reported that the requested performance run results were available and included compiler baseline-versus-PR comparison metrics
 * [today](https://github.com/microsoft/TypeScript/pull/65621#issuecomment-7060258049) **typescript-automation[bot]** reported results from comparing baseline and PR TypeScript compiler runs across the top 1,000 repositories, highlighting an unexpected change and ClickHouse/ClickStack build failures
 * [today](https://github.com/microsoft/TypeScript/pull/65621#issuecomment-7060258563) **typescript-automation[bot]** reported additional changes from the top 1,000 repositories suite, including build failures and TypeScript errors in vercel/ai examples
 * [today](https://github.com/microsoft/TypeScript/pull/65621#issuecomment-7075264404) **jakebailey** requested TypeScript bot runs for dt, user testing, top1000 testing, and performance testing
 * [today](https://github.com/microsoft/TypeScript/pull/65621#issuecomment-7075265347) **typescript-automation[bot]** said "Hey @jakebailey, this PR is in an unmergable state, so is missing a merge commit to run against; please resolve conflicts and try again."
 * [later](https://github.com/microsoft/TypeScript/pull/65621#issuecomment-7077288845) **jakebailey** requested TypeScript bot runs for dt, user testing, top1000 testing, and performance testing
 * [later](https://github.com/microsoft/TypeScript/pull/65621#issuecomment-7077289841) **typescript-automation[bot]** reported that the requested build and test jobs had started and provided links to their results
 * [later](https://github.com/microsoft/TypeScript/pull/65621#issuecomment-7077600815) **typescript-automation[bot]** reported that the DT tests completed with a branch-only error in the amzn__synthetics-playwright package and linked the full build log
 * [later](https://github.com/microsoft/TypeScript/pull/65621#issuecomment-7077621262) **typescript-automation[bot]** reported new TS2589 errors in type-fest user tests when comparing the baseline and PR, and asked @jakebailey to investigate
 * [later](https://github.com/microsoft/TypeScript/pull/65621#issuecomment-7077728264) **typescript-automation[bot]** reported the requested performance run results, including baseline-versus-PR compiler metrics
 * [later](https://github.com/microsoft/TypeScript/pull/65621#issuecomment-7078975032) **typescript-automation[bot]** reported results from comparing baseline and PR tsc runs across the top 1000 repositories, including new deep-instantiation errors in type-fest and build failures in BlockNote

### [Issue microsoft/TypeScript#65627](https://github.com/microsoft/TypeScript/issues/65627) (Open)

**Declaration emit omits \`resolution\-mode\` when an import type names a \`\.d\.cts\` file of a dual package from an ES module**

*Declaration emit in TypeScript 7.x omits the required `resolution-mode` when referencing `.d.cts` files from ES modules, producing incorrect or unresolvable types.*

 * created by **ktfth**
 * [today](https://github.com/microsoft/TypeScript/issues/65627#issuecomment-7073105902) **hkleungai** said "A duplicate of https://github.com/microsoft/typescript-go/issues/3657."

### [Issue microsoft/TypeScript#65628](https://github.com/microsoft/TypeScript/issues/65628) (Open)

**Declaration emit drops nested destructured \`require\` bindings in JS \(\`const { b: { c } } = require\("\./m"\)\`\)**

*Declaration emit in TypeScript 7.x drops nested destructured CommonJS require bindings, producing invalid or incomplete `.d.ts` files.*

 * created by **ktfth**

### [PR microsoft/TypeScript#65629](https://github.com/microsoft/TypeScript/pull/65629) (Open, `For Backlog Bug`)

**Fix JSDoc type predicate inference for arrow functions**

*Fix JSDoc type predicate inference for JavaScript arrow functions and expressions by resolving enclosing @type annotations and return signatures.*

 * created by **1abdala**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/65629#issuecomment-7076473112) **1abdala** reproduced the Contributor License Agreement request and signing instructions

### [PR microsoft/TypeScript#65630](https://github.com/microsoft/TypeScript/pull/65630) (Open, `For Uncommitted Bug`)

**Fix nested destructured require bindings in declaration emit**

*Declaration emit incorrectly handles nested destructured CommonJS require bindings, requiring corrected transformation logic and regression tests.*

 * created by **mohdshamii**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/65630#issuecomment-7076753068) **mohdshamii** said "@microsoft-github-policy-service agree"

### [PR microsoft/TypeScript#65631](https://github.com/microsoft/TypeScript/pull/65631) (Open, `For Backlog Bug`)

**Skip implicit\-any suggestions for content\-mapped modules**

*Suppress erroneous TS7016 implicit-any suggestions for content-mapped module resolutions while preserving genuine assignment errors.*

 * created by **zzy2008**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/65631#issuecomment-7076937965) **microsoft-github-policy-service[bot]** requested that @zzy2008 review and accept the Contributor License Agreement by replying with the appropriate command

### [PR microsoft/TypeScript#65632](https://github.com/microsoft/TypeScript/pull/65632) (Open, `For Backlog Bug`)

**Simplify string index signatures outside member resolution**

*Fix string-index signature simplification so conditional checks resolve correctly for interfaces, classes, and generic instances during member resolution.*

 * created by **zzy2008**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/65632#issuecomment-7077229192) **zzy2008** said "@microsoft-github-policy-service agree"
 * [later](https://github.com/microsoft/TypeScript/pull/65632#issuecomment-7077986107) **jakebailey** suggested splitting the changes into separate commits for the failing test and baseline, followed by the fix and updated baseline

### [PR microsoft/TypeScript#65633](https://github.com/microsoft/TypeScript/pull/65633) (Open, `For Backlog Bug`)

**Keep root source files when project references form a cycle**

*Ensure project-reference cycles compare normalized config paths so root source files are preserved and expected compiler errors are reported.*

 * created by **zzy2008**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/65633#issuecomment-7077157137) **microsoft-github-policy-service[bot]** requested that @zzy2008 review and accept the Contributor License Agreement by replying with the appropriate command

