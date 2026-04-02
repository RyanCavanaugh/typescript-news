# Report for 2025-11-30 (Sunday, November 30th, 2025)

8 different users commented on 8 different issues.

## Recommended Actions

 * Response Recommended
    * @codpro2005 proposed a compiler change for implicit type inference constraints in [microsoft/TypeScript#51108](https://github.com/microsoft/TypeScript/issues/51108#issuecomment-3595819448)
    * @silverwind asked if the UNDEFINED_VOID_ONLY symbol could be removed once this fix is released in [microsoft/TypeScript#57840](https://github.com/microsoft/TypeScript/issues/57840#issuecomment-3597292551)

## Activity Summary

### [Issue microsoft/TypeScript#51108](https://github.com/microsoft/TypeScript/issues/51108) (Open, `Suggestion`, `Experimentation Needed`)

**Carry over source constraints to the inferred type parameter**

*Enable TypeScript to carry over existing source constraints when inferring type variables so they maintain their original bounds.*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [3.1 years ago](https://github.com/microsoft/TypeScript/issues/51108#issuecomment-1284867401) **rusmisel** encountered the same issue with the DeepKeyedBy type, mentioned using ts-ignore as a workaround, and suggested it should work without it
 * [2.7 years ago](https://github.com/microsoft/TypeScript/issues/51108#issuecomment-1439826624) **Andarist** asked what the use cases were for using infer constraints to break constraint relationships beyond avoiding recursion limits
 * [later](https://github.com/microsoft/TypeScript/issues/51108#issuecomment-3595819448) **codpro2005** summarized points about verbose TypeScript inference workarounds and proposed compiler support for implicit constraints

### [Issue microsoft/TypeScript#57840](https://github.com/microsoft/TypeScript/issues/57840) (Closed, `Bug`, `Help Wanted`, `Domain: check: Type Inference`)

**Return type incorrectly inferred as void**

*TypeScript infers a bare return as void instead of undefined in functions declared to return Promise<undefined> or undefined.*

 * [1.6 years ago](https://github.com/microsoft/TypeScript/issues/57840#issuecomment-2010501800) **RyanCavanaugh** clarified that union contextual types do not cause errors, provided code examples, and suggested using someType as the fix
 * **RyanCavanaugh** added label `Domain: Type Inference`
 * (1 month ago) **jakebailey** closed the issue
 * [later](https://github.com/microsoft/TypeScript/issues/57840#issuecomment-3597292551) **silverwind** asked if the `UNDEFINED_VOID_ONLY` unique symbol could be removed once the fix was released

### [Issue microsoft/TypeScript#62816](https://github.com/microsoft/TypeScript/issues/62816) (Closed, `Question`)

**\`tsc\` transpile js to js converts Set iteration loops to invalid numeric key indexing**

*Transpiling JavaScript with tsc’s allowJs option converts Set for-of loops into invalid .length-based index loops.*

 * [2 days ago](https://github.com/microsoft/TypeScript/issues/62816#issuecomment-3591045909) **MartinJohns** explained that specifying input files on the command line ignores tsconfig and that without a specified target the compiler defaults to ES5
 * [yesterday](https://github.com/microsoft/TypeScript/issues/62816#issuecomment-3591683354) **sparr** thanked the maintainers and expressed confusion about invalid code being "working as intended"
 * [yesterday](https://github.com/microsoft/TypeScript/issues/62816#issuecomment-3591703024) **MartinJohns** explained that downleveling to ES5 intentionally produced the correct for-of loop code and that enabling type checks would warn about missing length properties
 * [later](https://github.com/microsoft/TypeScript/issues/62816#issuecomment-3596641898) **nmain** suggested using the downlevelIteration option and explained that ES6 features like Set and iterators can't be polyfilled properly

### [Issue microsoft/TypeScript#62817](https://github.com/microsoft/TypeScript/issues/62817) (Closed)

**Suggestion: Automatic Structural Constraints for \`infer\` Types**

*Introduce automatic structural constraints for inferred types in TypeScript to preserve their known shape.*

 * created by **codpro2005**
 * [later](https://github.com/microsoft/TypeScript/issues/62817#issuecomment-3595271135) **Andarist** said "duplicate of https://github.com/microsoft/TypeScript/issues/51108"
 * (later) **codpro2005** closed the issue

### [PR microsoft/TypeScript#62818](https://github.com/microsoft/TypeScript/pull/62818) (Open, `For Backlog Bug`)

**Add deprecation warning for computed property names in enums**

*Introduce a suggestion diagnostic with an auto-fix to deprecate computed property names in enums ahead of fully disallowing them.*

 * created by **magic-akari**
 * **typescript-bot** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/62818#issuecomment-3594616882) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [today](https://github.com/microsoft/TypeScript/pull/62818#issuecomment-3594616895) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (today) **typescript-bot** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`

### [Issue microsoft/TypeScript#62819](https://github.com/microsoft/TypeScript/issues/62819) (Closed, `Duplicate`)

**invalid behavior of \`satisfies\`**

*TypeScript’s satisfies operator fails to flag extra spread properties from a const union object while direct object literals error*

 * created by **salisbury-espinosa**
 * [later](https://github.com/microsoft/TypeScript/issues/62819#issuecomment-3596691093) **MartinJohns** said "Duplicate of #39998."

