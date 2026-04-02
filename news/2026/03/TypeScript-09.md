# Report for 2026-03-09 (Monday, March 9th, 2026)

12 different users commented on 42 different issues.

## Recommended Actions

 * Response Recommended
    * @titoBouzout asked what is needed to move this issue forward and if it could be resolved for TypeScript 6 in [microsoft/TypeScript#55182](https://github.com/microsoft/TypeScript/issues/55182#issuecomment-4025468380)
    * @Voltra provided detailed reproduction steps and error context in [microsoft/TypeScript#60114](https://github.com/microsoft/TypeScript/issues/60114#issuecomment-4026507586)
    * @veeceey asked if anything should be updated in [microsoft/TypeScript#63141](https://github.com/microsoft/TypeScript/pull/63141#issuecomment-4031356220)

## Activity Summary

### [Issue microsoft/TypeScript#40904](https://github.com/microsoft/TypeScript/issues/40904) (Open, `Suggestion`, `Awaiting More Feedback`)

**Interface merging for any property names does not allow type narrowing**

*Interface merging of an any index signature with a specific property type is rejected due to mismatched types.*

 * (5.4 years ago) **RyanCavanaugh** added labels `Awaiting More Feedback`, `Suggestion`
 * [5.4 years ago](https://github.com/microsoft/TypeScript/issues/40904#issuecomment-702814343) **RyanCavanaugh** said "We've historically stopped declaration merging at the property level but I don't think there's any reason in principle this couldn't be supported if there are enough motivating use cases for it"
 * [later](https://github.com/microsoft/TypeScript/issues/40904#issuecomment-4031944370) **brillout** said "Use case: being able to narrow down the type of import.meta.env."

### [PR microsoft/TypeScript#54475](https://github.com/microsoft/TypeScript/pull/54475) (Closed, `For Backlog Bug`, **rbuckton**)

**Properly emit super not root statement errors with class fields**

*Properly report errors for disallowed super calls in classes with parameter properties and exempt non-downleveled private fields*

 * created by **Josh-Cena**
 * **typescript-bot** added label `For Backlog Bug`
 * **RyanCavanaugh** assigned to **rbuckton**
 * (today) **Josh-Cena** closed the issue

### [Issue microsoft/TypeScript#54500](https://github.com/microsoft/TypeScript/issues/54500) (Open, `Discussion`, `Fix Available`)

**6\.0 Deprecation List**

*Proposed deprecations of outdated TypeScript 6.0 compiler options, with full removal planned for version 7.0.*

 * [1 month ago](https://github.com/microsoft/TypeScript/issues/54500#issuecomment-3861434363) **RyanCavanaugh** said "Edited to un-deprecate enum merging and cross-namespace value referencing; these are in 7.0 already and removing them wouldn't produce the upside I had hoped for."
 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/54500#issuecomment-3874952761) **DanielRosenwasser** said "I think we also passed on conditional import fallbacks: https://github.com/microsoft/TypeScript/issues/50762"
 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/54500#issuecomment-3927313490) **HolgerJeromin** expressed concern about the removal of module:none in TypeScript 6.0-beta and its potential to lock projects on older versions
 * [later](https://github.com/microsoft/TypeScript/issues/54500#issuecomment-4029987037) **n9** expressed agreement and mentioned that the amd module format with outFile is useful for enterprise systems serving as foundation for internal DSLs

### [Issue microsoft/TypeScript#55182](https://github.com/microsoft/TypeScript/issues/55182) (Open, `Suggestion`, `Awaiting More Feedback`)

**Enforce property rules on kebab\-cased JSX attributes**

*Enable TypeScript to enforce property rules on kebab-cased JSX attributes by using template literal types.*

 * [1.4 years ago](https://github.com/microsoft/TypeScript/issues/55182#issuecomment-2398912772) **trusktr** suggested adding a strictJsxProps compiler option to prevent silent failures from misspelled JSX props while preserving backwards compatibility
 * [36 weeks ago](https://github.com/microsoft/TypeScript/issues/55182#issuecomment-3016876530) **JulianCataldo** reported that excess property checks in JSX erroneously bypassed hyphenated custom element attributes, described it as a bug, and proposed a heuristic solution with a TypeScript plugin snippet
 * [1 month ago](https://github.com/microsoft/TypeScript/issues/55182#issuecomment-3861385142) **whittede** said "+1 to the original idea in this thread, it would be super useful and would reduce debug time when trying to figure out why attributes are throwing errors or not passing along data."
 * [today](https://github.com/microsoft/TypeScript/issues/55182#issuecomment-4025468380) **titoBouzout** asked whether the issue could be resolved in TypeScript 6 with strict typings for dashed HTML/component attributes and inquired what is needed to move the issue forward

### [Issue microsoft/TypeScript#60114](https://github.com/microsoft/TypeScript/issues/60114) (Open, `Needs Investigation`, **weswigham**)

**Regression Bug: Error "The type of this node cannot be serialized because its property '\[fooSymbol\]' cannot be serialized\." happens but potentially avoidable automatically\.**

*A regression in TypeScript 4.8 causes serialization errors for nodes with symbol properties in generics that earlier versions exported without issues.*

 * (1.4 years ago) **RyanCavanaugh** set milestone to `TypeScript 5.7.0`, and assigned to **weswigham**
 * [18 weeks ago](https://github.com/microsoft/TypeScript/issues/60114#issuecomment-3476287885) **caeus** said "Still happening in 5.9.2 in similar cases, but only if compilerOptions.declararion is set to true"
 * [today](https://github.com/microsoft/TypeScript/issues/60114#issuecomment-4026507586) **Voltra** described receiving TS4118 serialization errors for array/tuple types in TypeScript 5.9.3 when using an as const object

### [PR microsoft/TypeScript#63141](https://github.com/microsoft/TypeScript/pull/63141) (Open, `For Backlog Bug`)

**Fix Debug Failure crash when importing from mapped type module exports**

*The TypeScript compiler crashes when importing a mapped-type re-exported symbol due to missing mapped symbol flags propagation.*

 * created by **veeceey**
 * **typescript-bot** added label `For Backlog Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/63141#issuecomment-4031356220) **veeceey** said "checking in on this — let me know if there's anything I should update"

### [Issue microsoft/TypeScript#63214](https://github.com/microsoft/TypeScript/issues/63214) (Open, `Discussion`)

**Google feedback on TS 6\.0\-beta**

*Google’s TypeScript team finds the TS 6.0-beta upgrade manageable with minor code tweaks for strict defaults and deprecated namespace syntax while anticipating deprecation challenges in TS 7.0.*

 * created by **cecilyhunt**
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63214#issuecomment-4015049709) **DanielRosenwasser** asked whether upgrading to TS 6.0 would still be difficult without the ignoreDeprecations option
 * **RyanCavanaugh** added label `Discussion`

### [Issue microsoft/TypeScript#63216](https://github.com/microsoft/TypeScript/issues/63216) (Closed, `Duplicate`)

**\`keyof\` behaves differently with index signatures created using \`Record\`**

*The keyof operator returns string|number for an explicit {[x: string]: unknown} index signature but only string for Record<string, unknown> despite both supporting numeric indexing.*

 * [yesterday](https://github.com/microsoft/TypeScript/issues/63216#issuecomment-4016548263) **mkantor** expressed agreement with not displaying the type as an index signature and suggested opening a separate issue since the current behavior was misleading
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63216#issuecomment-4016764287) **MartinJohns** clarified that issue #45447 was not the same, explained that keyof {[x: string]: any} and keyof Record<string, any> return different results, and noted confusion due to a display issue
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63216#issuecomment-4017187645) **jcalz** said "Duplicate #31013"
 * [today](https://github.com/microsoft/TypeScript/issues/63216#issuecomment-4025537931) **RyanCavanaugh** provided an automatically generated analysis and list of similar issues

### [Issue microsoft/TypeScript#63218](https://github.com/microsoft/TypeScript/issues/63218) (Open, `Suggestion`, `Awaiting More Feedback`)

**Error \(2320\) when extending interfaces where a property is both readonly and readwrite\.**

*Extending two interfaces that declare the same property as readonly and writable erroneously triggers a conflict error*

 * created by **denis-migdal**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63218#issuecomment-4015967785) **denis-migdal** noticed that a property’s readonly status varied depending on the order of extends and provided a playground example
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63218#issuecomment-4017183362) **denis-migdal** provided two code examples illustrating missing TypeScript errors for getter/setter implementations
 * [today](https://github.com/microsoft/TypeScript/issues/63218#issuecomment-4025537993) **RyanCavanaugh** provided an automated analysis listing similar issues
 * [today](https://github.com/microsoft/TypeScript/issues/63218#issuecomment-4025817238) **denis-migdal** compared proposed bugs against existing issues and found no clear duplicates while highlighting confusion around readonly behavior

### [Issue microsoft/TypeScript#63223](https://github.com/microsoft/TypeScript/issues/63223) (Open, `Bug`, `Domain: flag: isolatedDeclarations`)

**Toggling \`isolatedModules\` in \`tsconfig\.json\` while running the compiler in \`watch\` mode, doesn't re\-emit \`const enums\`, unlike toggling \`preserveConstEnums\`, which does**

*Unlike preserveConstEnums toggles, changing isolatedModules in watch mode does not re-emit const enums until a full rebuild.*

 * created by **rotemdan**
 * [today](https://github.com/microsoft/TypeScript/issues/63223#issuecomment-4025538117) **RyanCavanaugh** provided an automated list of similar issues

### [Issue microsoft/TypeScript#63225](https://github.com/microsoft/TypeScript/issues/63225) (Open, `Needs Investigation`)

**\`Omit\` causes function to lose contextual typing**

*Omitting keys from AssertableState<T> in TypeScript 6.0 causes function parameters to lose contextual typing and default to any.*

 * created by **dragomirtitian**
 * [later](https://github.com/microsoft/TypeScript/issues/63225#issuecomment-4029620365) **Andarist** said "Bisects to https://github.com/microsoft/TypeScript/pull/60528 . I'll investigate it"

### [PR microsoft/TypeScript#63226](https://github.com/microsoft/TypeScript/pull/63226) (Closed)

**Use optional chaining for getMemoryUsage in GcTimer**

*Use optional chaining instead of non-null assertions for getMemoryUsage in GcTimer.run to avoid runtime errors.*

 * created by **phitonias**
 * [today](https://github.com/microsoft/TypeScript/pull/63226#issuecomment-4026613668) **phitonias** said "@microsoft-github-policy-service agree [company="stb"]"
 * [later](https://github.com/microsoft/TypeScript/pull/63226#issuecomment-4030290040) **MartinJohns** said "Your changes don't align with your description."

### [Issue microsoft/TypeScript#63227](https://github.com/microsoft/TypeScript/issues/63227) (Open, `Needs Investigation`, **ahejlsberg**)

**Inference from result of generic function no longer produces a union**

*TypeScript 6 regression: deepEqual’s generic inference from compact fails to produce a union of optional and required properties.*

 * created by **dragomirtitian**

### [Issue microsoft/TypeScript#63228](https://github.com/microsoft/TypeScript/issues/63228) (Closed, `Needs Investigation`, **jakebailey**)

**TypeScript 6 API Bug \- \`isSourceFileDefaultLibrary\` false negative on program structure reuse**

*In TypeScript 6.0.0-beta, isSourceFileDefaultLibrary incorrectly returns false for default library files when reusing program structure.*

 * created by **StyleShit**

