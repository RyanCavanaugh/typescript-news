# Report for 2026-09-07 (Monday, September 7th, 2026)

13 different users commented on 49 different issues.

## Recommended Actions

 * Response Recommended
    * @devanshj suggested closing the issue as it appears fixed in [microsoft/TypeScript#46724](https://github.com/microsoft/TypeScript/issues/46724#issuecomment-5585782895)

## Activity Summary

### [Issue microsoft/TypeScript#44024](https://github.com/microsoft/TypeScript/issues/44024) (Closed, `Bug`, `Fixed`, `Domain: JSX/TSX`, `Rescheduled`, `Needs Human Review`, **weswigham**)

**TypeError: Cannot read property 'get' of undefined at Object\.getJSXImplicitImportBase**

*Running Jest tests in a nested monorepo UI package triggers a TypeError in TypeScript getJSXImplicitImportBase.*

 * (2.1 years ago) **RyanCavanaugh** added label `Domain: JSX/TSX`, set milestone to `TypeScript 5.7.0`, and removed from milestone `TypeScript 5.5.0`
 * [today](https://github.com/microsoft/TypeScript/issues/44024#issuecomment-5573676555) **RyanCavanaugh** noted that the issue was fixed by PR #48862, confirmed that the crash in 4.2.4 was resolved in 6.0.3 and the native compiler, and that the PR base commit reproduced the crash while the merged commit did not
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#44325](https://github.com/microsoft/TypeScript/issues/44325) (Closed, `Bug`, `Fixed`, `Domain: Mapped Types`, `Rescheduled`, `Needs Human Review`, **ahejlsberg**)

**The results of the 'Mapped Types' distribution have changed\.**

*Mapped types no longer distribute over unions in TypeScript 4.3.2, merging property types into a single union.*

 * (2.1 years ago) **RyanCavanaugh** added label `Domain: Mapped Types`, set milestone to `TypeScript 5.7.0`, and removed from milestone `TypeScript 5.5.0`
 * [today](https://github.com/microsoft/TypeScript/issues/44325#issuecomment-5574064089) **RyanCavanaugh** explained that the mapped conditional issue was fixed in 5.4.0-dev.20240217 and that the merge for #57362 accepts both assignment directions
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#45406](https://github.com/microsoft/TypeScript/issues/45406) (Open, `Bug`, `Needs More Info`, `Rescheduled`, `Domain: check: Type Circularity`, `Needs Human Review`, **armanio123**)

**"Maximum call stack size exceeded" in JavaScript IntelliSense following specific module import**

*VSCode JavaScript IntelliSense crashes with a maximum call stack size exceeded error and only shows snippet suggestions after importing passport-shopify.*

 * (2.1 years ago) **RyanCavanaugh** added label `Domain: Type Circularity`, set milestone to `TypeScript 5.7.0`, and removed from milestone `TypeScript 5.5.0`
 * [today](https://github.com/microsoft/TypeScript/issues/45406#issuecomment-5575226941) **RyanCavanaugh** failed to reproduce the maximum call stack size exceeded error with TS 4.3.5 using passport-shopify@0.1.2 and requested the lockfile or full dependency tree
 * (today) **RyanCavanaugh** added labels `Needs Human Review`, `Needs More Info`

### [Issue microsoft/TypeScript#45435](https://github.com/microsoft/TypeScript/issues/45435) (Closed, `Bug`, `Domain: API: Transforms`, `Needs Human Review`)

**transpileModule miscompiles const/let to var without renaming, shadowing globals**

*transpileModule incorrectly downcompiles block-scoped const to var without renaming, unintentionally shadowing the global console object*

 * [2.7 years ago](https://github.com/microsoft/TypeScript/issues/45435#issuecomment-1834020213) **frigus02** reported another instance of emit difference with ts.transpileModule based on noLib setting and asked if isolatedModules could flag it
 * [2.7 years ago](https://github.com/microsoft/TypeScript/issues/45435#issuecomment-1852090218) **frigus02** described an issue with window variable collision in ES5 emit, provided a playground link and a commit with a proposed change to always rename block-scoped names, and asked if the change was feasible and performant
 * **RyanCavanaugh** added label `Domain: Transforms`
 * [today](https://github.com/microsoft/TypeScript/issues/45435#issuecomment-5573466009) **RyanCavanaugh** explained that transpileModule belongs to the pre-TypeScript-7 JavaScript Compiler API, has been superseded, and is not actionable on the supported API surface
 * **RyanCavanaugh** added label `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#45560](https://github.com/microsoft/TypeScript/issues/45560) (Closed, `Bug`, `Fixed`, `Domain: Mapped Types`, `Needs Human Review`)

**Mapped types lose type information**

*Mapped types over tuple unions lose specific element types and widen indexed access to boolean instead of true.*

 * [12 weeks ago](https://github.com/microsoft/TypeScript/issues/45560#issuecomment-4676880644) **mwg-ofx** said "I wonder if such a change could be reconsidered after the Go migration is complete, given the significant speed boost it provides."
 * [12 weeks ago](https://github.com/microsoft/TypeScript/issues/45560#issuecomment-4682464840) **RyanCavanaugh** said "By "unacceptable perf hits" we mean like 40%, and people are already complaining that tsgo isn't fast enough in material-ui."
 * **jakebailey** removed label `Fix Available`
 * [today](https://github.com/microsoft/TypeScript/issues/45560#issuecomment-5575738948) **RyanCavanaugh** explained that the example failed with TS2322 in 5.1.0-dev.20230313 due to widened indexed access to boolean, and that PR #53098 deferred resolution so the “yes” discriminant is preserved and the code is accepted in later TypeScript versions
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#45576](https://github.com/microsoft/TypeScript/issues/45576) (Closed, `Bug`, `Fixed`, `Domain: check: Type Circularity`, `Needs Human Review`)

**Stack overflow on certain platforms**

*Recursive type definitions in jasmine Matchers produce unbounded instantiation and trigger a stack overflow in TypeScript*

 * [4.7 years ago](https://github.com/microsoft/TypeScript/issues/45576#issuecomment-991378316) **charlescapps** said "I just verified I don't get this Maximum call stack size exceeded error on version 4.5.2 of typescript, so this is likely a regression in the current latest release - 4.5.3 at time of writing."
 * (2.5 years ago) **RyanCavanaugh** added label `Domain: Type Circularity`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/45576#issuecomment-5575944568) **RyanCavanaugh** reported that the browser-worker stack overflow no longer occurred and that the Playground now reports TS2589 as expected across multiple TypeScript versions
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#45844](https://github.com/microsoft/TypeScript/issues/45844) (Closed, `Bug`, `Fixed`, `Domain: Declaration Emit`, `Rescheduled`, `Needs Human Review`, **armanio123**)

**Namespaces get stripped in object literals**

*TypeScript emits declaration files that strip namespace qualifiers from types in object literal method parameters.*

 * (2.1 years ago) **RyanCavanaugh** added label `Domain: Declaration Emit`, set milestone to `TypeScript 5.7.0`, and removed from milestone `TypeScript 5.5.0`
 * [today](https://github.com/microsoft/TypeScript/issues/45844#issuecomment-5577019411) **RyanCavanaugh** stated that the issue was fixed by PR #58085 and provided version-specific declaration signature details
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#46020](https://github.com/microsoft/TypeScript/issues/46020) (Closed, `Bug`, `Needs Investigation`, `Domain: Conditional Types`, `Rescheduled`, `Needs Human Review`, **sandersn**)

**\[4\.3, 4\.4\] Inline filtering mapped type conditional with \`infer\` fails**

*In TypeScript 4.3 and 4.4, inlining a mapped type in a conditional with an inferred type incorrectly triggers the false branch when a separate type declaration works correctly.*

 * (2.1 years ago) **RyanCavanaugh** added label `Domain: Conditional Types`, set milestone to `TypeScript 5.7.0`, and removed from milestone `TypeScript 5.5.0`
 * [today](https://github.com/microsoft/TypeScript/issues/46020#issuecomment-5578182073) **RyanCavanaugh** identified the issue as a duplicate of #44143 and explained why the inline mapped key filter causes the inferred result to become never
 * **RyanCavanaugh** added label `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#46036](https://github.com/microsoft/TypeScript/issues/46036) (Closed, `Bug`, `Fixed`, `Help Wanted`, `Domain: lib.d.ts`, `Needs Human Review`)

**Incorrect type declaration for CryptoKeyPair**

*TypeScript v4.4 incorrectly makes CryptoKeyPair properties optional despite the W3C spec requiring both privateKey and publicKey.*

 * [4.8 years ago](https://github.com/microsoft/TypeScript/issues/46036#issuecomment-950870031) **saschanaz** concluded that CryptoKeyPair fields should be non-optional and said they would reopen the PR
 * [4.8 years ago](https://github.com/microsoft/TypeScript/issues/46036#issuecomment-950889860) **saschanaz** said "Also filed https://github.com/w3c/webcrypto/issues/290."
 * **RyanCavanaugh** added label `Domain: lib.d.ts`
 * [today](https://github.com/microsoft/TypeScript/issues/46036#issuecomment-5578357674) **RyanCavanaugh** noted that CryptoKeyPair required both privateKey and publicKey and that an empty object assignment was rejected with TS2739 in several TypeScript versions, referencing the required-member override added in linked PRs
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#46216](https://github.com/microsoft/TypeScript/issues/46216) (Closed, `Bug`, `Fixed`, `Crash`, `Domain: LS: Inlay Hints`, `Needs Human Review`)

**Crash in inlay hints: "Cannot read property 'kind' of undefined"**

*VS Code TypeScript inlay hints crashes with 'Cannot read property kind of undefined' error when using JSDoc callback typedefs.*

 * (4.9 years ago) **andrewbranch** added labels `Crash`, `Domain: Inlay Hints`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/46216#issuecomment-5579008809) **RyanCavanaugh** stated that the crash when computing parameter-name inlay hints for JSDoc function-type parameters was fixed by PR #47684
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#46256](https://github.com/microsoft/TypeScript/issues/46256) (Closed, `Bug`, `Fixed`, `Help Wanted`, `Effort: Moderate`, `Domain: JS Emit`, `Needs Human Review`)

** After tsc converts the js file, it does not meet expectations**

*tsc's ES2015 transpilation incorrectly handles Unicode escape \u{62} in template literals, resulting in undefined cooked values*

 * (4.4 years ago) **DanielRosenwasser** added labels `Help Wanted`, `Effort: Moderate`
 * **RyanCavanaugh** added label `Domain: JS Emit`
 * [today](https://github.com/microsoft/TypeScript/issues/46256#issuecomment-5579190242) **RyanCavanaugh** announced that PR #51837 fixed the ES2015 transform to correctly preserve the tagged template's cooked and raw values and noted the incorrect cooked entry persisted through 5.1.0-dev.20230324 but was resolved in 5.1.0-dev.20230325 and later.
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#46374](https://github.com/microsoft/TypeScript/issues/46374) (Closed, `Bug`, `Fixed`, `Domain: Error Messages`, `Rescheduled`, `Needs Human Review`, **sandersn**)

**Unexpected error message when using tagged union in an nested object\.**

*TypeScript 4.5-beta incorrectly reports an error when narrowing a tagged union inside a nested object.*

 * (2.5 years ago) **RyanCavanaugh** set milestones to `TypeScript 5.5.0`, `TypeScript 5.7.0`, and removed from milestone `TypeScript 5.5.0`
 * [today](https://github.com/microsoft/TypeScript/issues/46374#issuecomment-5579962176) **RyanCavanaugh** described that diagnostics now report missing LinearGradientObject properties for nested color objects instead of misassigning "linear", and noted the change was introduced in PR #53709 and present since TS 5.1.0-dev and retained in TS 6.0.3
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#46375](https://github.com/microsoft/TypeScript/issues/46375) (Closed, `Bug`, `Domain: classes`, `Needs Human Review`)

**Member classes with ES2020 private fields do not respect assignment compatibility**

*Member classes with ES2020 private fields are incorrectly considered incompatible in assignments despite having compatible structures.*

 * **sandersn** added label `Bug`
 * [4 years ago](https://github.com/microsoft/TypeScript/issues/46375#issuecomment-1229259503) **gibbok** reproduced a bug in TypeScript 4.7.4 where unrelated class instances are considered comparable
 * **RyanCavanaugh** added label `Domain: classes`
 * [today](https://github.com/microsoft/TypeScript/issues/46375#issuecomment-5580057175) **RyanCavanaugh** explained that TypeScript has a per-invocation class-identity limitation for private fields and linked related issues
 * **RyanCavanaugh** added label `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#46425](https://github.com/microsoft/TypeScript/issues/46425) (Closed, `Bug`, `Fixed`, `Domain: check: Control Flow`, `Needs Human Review`)

**'used before being assigned' error inside a type alias**

*TypeScript reports 'used before being assigned' for a Symbol as a computed key in a type alias before its declaration.*

 * **andrewbranch** added to milestone `Backlog`
 * [3.3 years ago](https://github.com/microsoft/TypeScript/issues/46425#issuecomment-1529032334) **jespertheend** said "Seems like this is fixed in TypeScript 5, just like #47259"
 * **RyanCavanaugh** added label `Domain: Control Flow`
 * [today](https://github.com/microsoft/TypeScript/issues/46425#issuecomment-5580422709) **RyanCavanaugh** confirmed the issue was fixed in TypeScript starting with version 5.0.0-dev.20221231 and in 6.0.3, noting that PR #50824 addressed forward references in computed properties
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#46633](https://github.com/microsoft/TypeScript/issues/46633) (Open, `Bug`, `Needs More Info`, `Domain: Declaration Emit`, `Needs Human Review`)

**Inconsistent order of properties inferred from a generic type**

*TypeScript's --watch compiler emits declaration files with non-deterministic property ordering, causing unnecessary rebuilds.*

 * (4.8 years ago) **andrewbranch** added label `Domain: Declaration Emit`, and set milestone to `Backlog`
 * [4.7 years ago](https://github.com/microsoft/TypeScript/issues/46633#issuecomment-993336842) **dko-slapdash** provided additional examples for literal type alternatives and noted random reordering issues
 * [later](https://github.com/microsoft/TypeScript/issues/46633#issuecomment-5580866824) **RyanCavanaugh** requested a runnable reproduction including project files, tsconfig.json, TypeScript command, unrelated edit, and consecutive emitted .d.ts outputs
 * (later) **RyanCavanaugh** added labels `Needs Human Review`, `Needs More Info`

### [Issue microsoft/TypeScript#46724](https://github.com/microsoft/TypeScript/issues/46724) (Closed, `Bug`, `Needs More Info`, `Domain: Declaration Emit`, `Needs Human Review`)

**Optional parameter makes the compiler resolve types prematurely for declaration**

*Making the parameter optional causes the compiler to prematurely resolve the conditional Key type to unknown[] in the declaration.*

 * (4.8 years ago) **andrewbranch** added label `Bug`, and set milestone to `Backlog`
 * **RyanCavanaugh** added label `Domain: Declaration Emit`
 * [later](https://github.com/microsoft/TypeScript/issues/46724#issuecomment-5581577189) **RyanCavanaugh** noted that the provided Playground source didn’t reproduce the reported output and requested the exact source, compiler command, or configuration that produces the incorrect declaration
 * (later) **RyanCavanaugh** added labels `Needs Human Review`, `Needs More Info`
 * [later](https://github.com/microsoft/TypeScript/issues/46724#issuecomment-5585782895) **devanshj** concluded that Playground v4.4.4 and v6.0.3 produce the correct output and suggested closing the issue
 * (later) **devanshj** closed the issue

### [Issue microsoft/TypeScript#46750](https://github.com/microsoft/TypeScript/issues/46750) (Closed, `Bug`, `Fixed`, `Help Wanted`, `Effort: Moderate`, `Domain: Comment Emit`, `Needs Human Review`)

**Code blocks for \`@typedef\` do not preserve indentation in the generated \`\.d\.ts\` file\.**

*Indentation within code fences in @typedef comments is not preserved in the generated .d.ts file.*

 * (4.8 years ago) **andrewbranch** added label `Help Wanted`, and set milestone to `Backlog`
 * [4.8 years ago](https://github.com/microsoft/TypeScript/issues/46750#issuecomment-964732124) **Gerrit0** said "There's a few usages of @typedoc, where I'm pretty sure you meant @typedef here ;)"
 * [later](https://github.com/microsoft/TypeScript/issues/46750#issuecomment-5581702028) **RyanCavanaugh** noted that the reported @typedef declaration output still removed two-space code-block indentation in TS 4.4.3 and 6.0.3 and that TS 7.1.0-dev.20260907.1 preserved the original indentation
 * (later) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#46867](https://github.com/microsoft/TypeScript/issues/46867) (Open, `Bug`, `Domain: Conditional Types`, `Needs Human Review`)

**Possible eager resolution of type parameters**

*Wrapping the Equals utility type with one predetermined tuple type triggers unexpected eager resolution and false comparisons.*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [4.8 years ago](https://github.com/microsoft/TypeScript/issues/46867#issuecomment-974227658) **RyanCavanaugh** suggested a simpler working definition for Equals
 * **RyanCavanaugh** added label `Domain: Conditional Types`
 * [later](https://github.com/microsoft/TypeScript/issues/46867#issuecomment-5581958636) **RyanCavanaugh** explained that the Equals pattern’s behavior was implementation-defined, linked to the documentation, and suggested using a two-way assignability check for structural comparison
 * **RyanCavanaugh** added label `Needs Human Review`

### [Issue microsoft/TypeScript#46975](https://github.com/microsoft/TypeScript/issues/46975) (Closed, `Bug`, `Domain: Conditional Types`, `Needs Human Review`)

**Generic conditional type narrowing doesn't cascade as expected**

*Generic conditional type narrowing fails to exclude undefined in subsequent type usage, causing assignment errors.*

 * [4.7 years ago](https://github.com/microsoft/TypeScript/issues/46975#issuecomment-986283576) **jack-williams** referenced a related discussion and shared a working TypeScript type definition
 * [52 weeks ago](https://github.com/microsoft/TypeScript/issues/46975#issuecomment-3263631719) **titouandk** described encountering a similar issue with ReturnType and conditional types producing a union before narrowing, explained why it occurs, and provided a workaround using inference
 * **RyanCavanaugh** added label `Domain: Conditional Types`
 * [later](https://github.com/microsoft/TypeScript/issues/46975#issuecomment-5582471940) **RyanCavanaugh** pointed out that the issue was a duplicate, explained how conditional types track constraints in the true branch, and suggested reversing the test to correctly constrain the type
 * **RyanCavanaugh** added label `Needs Human Review`
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#47128](https://github.com/microsoft/TypeScript/issues/47128) (Closed, `Bug`, `Fixed`, `Domain: Conditional Types`, `Needs Human Review`)

**Inconsistency for whether partialed tuple is assignable to rest parameter**

*TypeScript inconsistently handles tuple Partial types in conditional versus non-conditional rest parameter definitions, causing D1 to fail while D2 succeeds.*

 * (4.7 years ago) **RyanCavanaugh** added labels `Bug`, `Domain: Conditional Types`, and set milestone to `Backlog`
 * [later](https://github.com/microsoft/TypeScript/issues/47128#issuecomment-5583755629) **RyanCavanaugh** described that the issue was fixed by PR #57122 and that TS2370 errors ceased in 5.4.0-dev.20240219, TypeScript 6.0.3, and the current native compiler
 * (later) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#47147](https://github.com/microsoft/TypeScript/issues/47147) (Closed, `Bug`, `Fixed`, `Domain: check: Type Inference`, `Needs Human Review`)

**Inference lost on params of key\-value function map**

*Mapping over an object of functions by key in TypeScript causes loss of parameter type inference*

 * [4.7 years ago](https://github.com/microsoft/TypeScript/issues/47147#issuecomment-995616283) **robertojmm** said "@ahejlsberg is there any walk around / alternative for doing this?"
 * [4.7 years ago](https://github.com/microsoft/TypeScript/issues/47147#issuecomment-996253537) **ahejlsberg** retracted earlier claim and clarified that the example works on nightly builds with consistent string-based enum names and offered a workaround for TypeScript 4.5 and earlier
 * **RyanCavanaugh** added label `Domain: Type Inference`
 * [later](https://github.com/microsoft/TypeScript/issues/47147#issuecomment-5584005249) **RyanCavanaugh** reported that the computed enum-member form bug was fixed in TypeScript 6.0.3, resolving TS7006 diagnostics under --noImplicitAny
 * (later) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#47150](https://github.com/microsoft/TypeScript/issues/47150) (Closed, `Bug`, `Domain: This-Typing`, `Needs Human Review`)

**Inference not work in object getter when use ThisType with additional fields**

*Object getter ‘this’ type inference fails when using ThisType with additional fields.*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [4.2 years ago](https://github.com/microsoft/TypeScript/issues/47150#issuecomment-1152226671) **vincent-yao27** demonstrated a similar issue with ThisType and generic constraints, sharing screenshots and code showing that removing the generic constraint makes it work
 * **RyanCavanaugh** added label `Domain: This-Typing`
 * [later](https://github.com/microsoft/TypeScript/issues/47150#issuecomment-5584157785) **RyanCavanaugh** noted that although the report predated issue #47599, he later consolidated the getter/ThisType family into that omnibus and tracked it by #47599
 * **RyanCavanaugh** added label `Needs Human Review`
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#47196](https://github.com/microsoft/TypeScript/issues/47196) (Closed, `Bug`, `Fixed`, `Domain: Intersection`, `Needs Human Review`)

**Intersection with object with property names colliding with that of \`Object\` results in unintended types of those properties\.**

*Intersecting object types that define properties matching built-in Object keys yields incorrect property type inference.*

 * (4.6 years ago) **RyanCavanaugh** added labels `Bug`, `Domain: Intersection`, and set milestone to `Backlog`
 * [later](https://github.com/microsoft/TypeScript/issues/47196#issuecomment-5584413163) **RyanCavanaugh** reported that both the valueOf and constructor intersection cases were fixed in PR #54753 and now compile without errors starting in 5.4.0-dev.20231130 and later
 * (later) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#47233](https://github.com/microsoft/TypeScript/issues/47233) (Closed, `Bug`, `Fixed`, `Domain: check: Type Inference`, `Needs Human Review`)

**Generic extending union type inference error**

*TypeScript incorrectly reports TS2322 when assigning a generic type parameter extending a union to the same union intersection.*

 * (4.6 years ago) **RyanCavanaugh** added labels `Bug`, `Domain: Type Inference`, and set milestone to `Backlog`
 * [later](https://github.com/microsoft/TypeScript/issues/47233#issuecomment-5584718016) **RyanCavanaugh** reported that the issue was fixed in 4.8.0-dev.20220528, TypeScript 6.0.3, and the current native build via PR #49119
 * (later) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#47258](https://github.com/microsoft/TypeScript/issues/47258) (Open, `Bug`, `Help Wanted`, `Domain: Binder`, `Needs Human Review`)

**Conflicting declaration merging doesn't fail in \.d\.ts files**

*TypeScript’s declaration merging for .d.ts files ignores conflicting interface member types instead of reporting an error based on import order.*

 * (4.6 years ago) **RyanCavanaugh** added labels `Help Wanted`, `Domain: Binder`, and set milestone to `Backlog`
 * [later](https://github.com/microsoft/TypeScript/issues/47258#issuecomment-5584847210) **RyanCavanaugh** explained that skipLibCheck skips all .d.ts files causing conflicts not to be diagnosed and that disabling skipLibCheck produces the expected error
 * **RyanCavanaugh** added label `Needs Human Review`

### [Issue microsoft/TypeScript#47259](https://github.com/microsoft/TypeScript/issues/47259) (Closed, `Bug`, `Fixed`, `Help Wanted`, `Domain: JSDoc`, `Needs Human Review`)

**Unable to use Symbol as key for jsdoc \`@typedef\`**

*Using a Symbol as a computed key in a JSDoc typedef causes TS2454 under strictNullChecks.*

 * [3.8 years ago](https://github.com/microsoft/TypeScript/issues/47259#issuecomment-1317399906) **VanillaMaster** noted that defining the type above the function prevented the error and supplied a code example
 * [3.3 years ago](https://github.com/microsoft/TypeScript/issues/47259#issuecomment-1529032058) **jespertheend** said "Seems like this has been fixed in TypeScript 5"
 * **RyanCavanaugh** added label `Domain: JSDoc`
 * [later](https://github.com/microsoft/TypeScript/issues/47259#issuecomment-5584994733) **RyanCavanaugh** stated that the JSDoc @typedef issue stopped reporting TS2454 starting with 5.0.0-dev.20221231 due to PR #50824
 * (later) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#47273](https://github.com/microsoft/TypeScript/issues/47273) (Closed, `Bug`, `Fixed`, `Help Wanted`, `Domain: Parser`, `Needs Human Review`)

**createProgarm with @typescript/vfs fails for target ES2021**

*Using @typescript/vfs to createProgram with compiler target ES2021 produces an internal error.*

 * [4.6 years ago](https://github.com/microsoft/TypeScript/issues/47273#issuecomment-1015589312) **dpilch** thanked the suggestion and confirmed that wrapping require.resolve('typescript') with path.dirname resolved the issue, referencing the TypeScript-Website example
 * [3.3 years ago](https://github.com/microsoft/TypeScript/issues/47273#issuecomment-1521245381) **Matsuuu** said "Submitted a relating issue to this to the vfs project https://github.com/microsoft/TypeScript-Website/issues/2801"
 * **RyanCavanaugh** added label `Domain: Parser`
 * [later](https://github.com/microsoft/TypeScript/issues/47273#issuecomment-5585276839) **RyanCavanaugh** described the failure cause in @typescript/vfs’s library map due to an omitted lib.es2021.intl.d.ts, noted that the issue occurred in v1.3.5 and was fixed in v1.5.0 and v1.6.4, and referenced a PR that resolved it
 * (later) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#47346](https://github.com/microsoft/TypeScript/issues/47346) (Closed, `Bug`, `Fixed`, `Help Wanted`, `Domain: check: Control Flow`, `Needs Human Review`)

**Extra check in expression cause invalid type narrowing**

*Redundant property checks or unnecessary optional chaining within expressions incorrectly narrow union types to never in TypeScript.*

 * **RyanCavanaugh** added label `Help Wanted`
 * [3.5 years ago](https://github.com/microsoft/TypeScript/issues/47346#issuecomment-1408382784) **Kcazer** described a behavior change in TypeScript 4.9.4 where certain property-in-operator checks no longer produced errors and inferred properties as unknown instead of their original types
 * **RyanCavanaugh** added label `Domain: Control Flow`
 * [later](https://github.com/microsoft/TypeScript/issues/47346#issuecomment-5585849685) **RyanCavanaugh** explained that the redundant 'a' in value check causing a TS2345 error was fixed in 5.1.0-dev.20230324 and later by PR #53435
 * (later) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#47358](https://github.com/microsoft/TypeScript/issues/47358) (Closed, `Bug`, `Fixed`, `Domain: Declaration Emit`, `Needs Human Review`)

**\`\-\-emitDeclarationOnly\` cannot be used together with \`\-p jsconfig\.json\`**

*Using the --emitDeclarationOnly compiler flag with a jsconfig.json project incorrectly triggers a TS5053 noEmit conflict error.*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [4.6 years ago](https://github.com/microsoft/TypeScript/issues/47358#issuecomment-1010344718) **RyanCavanaugh** said "noEmit is the default when processing jsconfig files, so you'd need to write tsc --noEmit false --declaration [...]. This could probably be made more ergonomic"
 * **RyanCavanaugh** added label `Domain: Declaration Emit`
 * [later](https://github.com/microsoft/TypeScript/issues/47358#issuecomment-5586594650) **RyanCavanaugh** described that the issue was fixed in PR #59071 and advised passing --noEmit false to generate declaration output
 * (later) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#47425](https://github.com/microsoft/TypeScript/issues/47425) (Closed, `Bug`, `Fixed`, `Help Wanted`, `Domain: JSDoc`, `Needs Human Review`)

**TS2302 when using two generics with the same name in JSDoc, but not in TypeScript\.**

*Static JSDoc method generics mistakenly reference class-level type parameters when using duplicate generic names, triggering a TS2302 error.*

 * (4.6 years ago) **RyanCavanaugh** added labels `Help Wanted`, `Domain: JSDoc`, and set milestone to `Backlog`
 * [later](https://github.com/microsoft/TypeScript/issues/47425#issuecomment-5587817786) **RyanCavanaugh** explained that the JSDoc method template now took precedence over the class template and noted that the TS2302 error occurred in 4.9.0-dev.20220919 but not in subsequent versions
 * (later) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63873](https://github.com/microsoft/TypeScript/issues/63873) (Closed, `Needs Investigation`, **andrewbranch**)

**Add batched assignability checks into the \`Checker API\`**

*Add batched type assignability checks and optional quantifiers to the Checker API for improved performance.*

 * (1 month ago) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **andrewbranch**
 * [6 days ago](https://github.com/microsoft/TypeScript/issues/63873#issuecomment-5504529919) **weswigham** said "Since https://github.com/microsoft/TypeScript/pull/63937 and https://github.com/microsoft/TypeScript/pull/64023 you should be able to batch up whatever API calls you want - that work well for you?"
 * [later](https://github.com/microsoft/TypeScript/issues/63873#issuecomment-5586268987) **artem1458** said "@weswigham It completely solves my use-case, thanks!"
 * (later) **artem1458** closed the issue

### [Issue microsoft/TypeScript#64154](https://github.com/microsoft/TypeScript/issues/64154) (Open, `Domain: API`, **andrewbranch**)

**\[API\] Redesign client\-side snapshot state model**

*Redesign the client-side snapshot state model to unify overlapping updateSnapshot, createProgram, and virtual filesystem operations into a coherent transition system.*

 * [4 days ago](https://github.com/microsoft/TypeScript/issues/64154#issuecomment-5532977627) **DanielRosenwasser** asked whether dirty meant the program was out of date with respect to disk after applying changes
 * [4 days ago](https://github.com/microsoft/TypeScript/issues/64154#issuecomment-5533077334) **DanielRosenwasser** considered whether to expose a program update method without snapshot.update and suggested requiring snapshot.update or returning a [Program, Snapshot] pair
 * **DanielRosenwasser** added label `Domain: API`
 * [today](https://github.com/microsoft/TypeScript/issues/64154#issuecomment-5578800244) **mrazauskas** suggested adding an option to programmatically set implied/enforced compiler options via api.createSnapshot and discussed a workaround using a virtual tsconfig file

### [Issue microsoft/TypeScript#64167](https://github.com/microsoft/TypeScript/issues/64167) (Closed, `Question`)

**LSP completion echoes the unresolved identifier currently being typed as a Text item**

*TypeScript's LSP server returns unresolved Text completions identical to the typed identifier, creating useless no-op suggestion entries.*

 * **RyanCavanaugh** added label `Question`
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/64167#issuecomment-5548058704) **DanielRosenwasser** clarified that sortText: 18 corresponded to SortTextJavascriptIdentifiers, demonstrated its effect in a ts-checked JavaScript file, and noted the downside of immediate identifier suggestions
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/64167#issuecomment-5548132079) **DanielRosenwasser** suggested that the editor could filter out LSP Text completions and provided a VS Code setting snippet
 * [today](https://github.com/microsoft/TypeScript/issues/64167#issuecomment-5577664742) **typescript-automation[bot]** said "This issue has been marked as "Question" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-automation[bot]** closed the issue

### [Issue microsoft/TypeScript#64182](https://github.com/microsoft/TypeScript/issues/64182) (Open, `Domain: Content Mappers`, **andrewbranch**)

**Allow content\-mappers to return declarations instead of source files**

*Allow TypeScript content mappers to return declaration files (.d.ts, .d.cts, .d.mts) instead of source files to bypass module syntax restrictions.*

 * created by **remcohaszing**
 * [today](https://github.com/microsoft/TypeScript/issues/64182#issuecomment-5567326791) **remcohaszing** explained that TypeScript allowed CJS syntax in .cts files with module=esnext but the content-mapper treated them as .ts and provided a reproduction link
 * (later) **andrewbranch** added label `Domain: Content Mappers`, set milestone to `TypeScript 7.1.0 Beta`, and assigned to **andrewbranch**

### [Issue microsoft/TypeScript#64189](https://github.com/microsoft/TypeScript/issues/64189) (Open)

**Add \`GenericType\` type to the API**

*Add a GenericType type to the API to represent TypeReference targets and expose their typeParameters.*

 * created by **mrazauskas**

### [PR microsoft/TypeScript#64190](https://github.com/microsoft/TypeScript/pull/64190) (Open, `For Uncommitted Bug`)

**\[api\] Add \`GenericType\` type**

*Adds a missing GenericType type definition to the TypeScript compiler API.*

 * created by **mrazauskas**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [PR microsoft/TypeScript#64191](https://github.com/microsoft/TypeScript/pull/64191) (Open, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**, **jakebailey**)

**Fix FSEvents routing for differently cased watch paths**

*Modify FSEvents routing logic to handle watch paths that differ only by case correctly.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**, **andrewbranch**

### [Issue microsoft/TypeScript#64192](https://github.com/microsoft/TypeScript/issues/64192) (Open)

**Recursive inference through self\-referential object literals**

*TypeScript cannot infer recursive types in self-referential object literal schemas, causing them to default to any without workaround.*

 * created by **colinhacks**

### [PR microsoft/TypeScript#64193](https://github.com/microsoft/TypeScript/pull/64193) (Open, `For Uncommitted Bug`, **andrewbranch**)

**fix\(tsoptions\): don't mutate ParsedCommandLine errors when computing CommonSourceDirectory**

*Modify ParsedCommandLine.CommonSourceDirectory to pass nil for source file checks and prevent mutating its Errors.*

 * created by **erantianantha**
 * (today) **typescript-automation[bot]** added label `For Uncommitted Bug`, and assigned to **andrewbranch**

### [PR microsoft/TypeScript#64194](https://github.com/microsoft/TypeScript/pull/64194) (Open, `For Backlog Bug`)

**fix\(checker\): cap template literal type size to avoid unbounded growth**

*Cap template literal type size with character and placeholder limits to prevent infinite type instantiation and memory exhaustion.*

 * created by **ekalinin**
 * **typescript-automation[bot]** added label `For Backlog Bug`

### [Issue microsoft/TypeScript#64195](https://github.com/microsoft/TypeScript/issues/64195) (Open)

**LSP: file contents are not re\-read when \`didChangeWatchedFiles\` reports \`Created\` \(type 1\) for a file already in the program**

*LSP server fails to reload existing files when a Created file watcher event occurs, leading to stale content.*

 * created by **shuto-masuda**

### [Issue microsoft/TypeScript#64196](https://github.com/microsoft/TypeScript/issues/64196) (Open)

**Native \`tsc\` ignores SIGINT and SIGTERM while compiling — Ctrl\-C does not interrupt a build, and the process exits 0**

*Native TypeScript compiler version 7 ignores SIGINT and SIGTERM during builds, making Ctrl-C ineffective and returning exit code 0.*

 * created by **rafaelnajman**

### [Issue microsoft/TypeScript#64197](https://github.com/microsoft/TypeScript/issues/64197) (Open)

**Excess property checks silently skipped for nested object literals at reverse\-mapped\-type inference sites \(regression in 6\.0\)**

*TypeScript 6.0 regression stops flagging excess properties on nested object literals in generic reverse-mapped type inference.*

 * created by **quithyot**
 * [later](https://github.com/microsoft/TypeScript/issues/64197#issuecomment-5584520796) **MartinJohns** said "Very likely a duplicate of #64006."

