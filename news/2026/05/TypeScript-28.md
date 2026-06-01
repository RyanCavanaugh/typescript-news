# Report for 2026-05-28 (Thursday, May 28th, 2026)

6 different users commented on 8 different issues.

## Recommended Actions

 * Response Recommended
    * @nmain asked if the repro was correct and noted a possible compiler flags discrepancy in [microsoft/TypeScript#63514](https://github.com/microsoft/TypeScript/issues/63514#issuecomment-4573971134)
    * @svenvandescheur asked why indexed access with a key typed never becomes any and why assigning any does not widen variable types in [microsoft/TypeScript#63514](https://github.com/microsoft/TypeScript/issues/63514#issuecomment-4574532804)
    * @nmain provided a suggested eslint rule to forbid unsafe type assertions in [microsoft/TypeScript#63514](https://github.com/microsoft/TypeScript/issues/63514#issuecomment-4575229248)
    * @nmain pointed out that the rule handles an `any` indexer but not a `never` indexer in [microsoft/TypeScript#63514](https://github.com/microsoft/TypeScript/issues/63514#issuecomment-4575968627)

## Activity Summary

### [Issue microsoft/TypeScript#63510](https://github.com/microsoft/TypeScript/issues/63510) (Closed, `AI Spam`)

**TypeScript compiler incorrectly reports duplicate identifiers for types and variables**

*TypeScript incorrectly flags user-defined types and variables as duplicate identifiers when they collide with built-in names.*

 * created by **sulthonzh**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63510#issuecomment-4560487720) **MartinJohns** explained that there was no built-in Event type and suggested using `noLib` to exclude standard declaration files
 * [today](https://github.com/microsoft/TypeScript/issues/63510#issuecomment-4565283139) **mkantor** explained that the errors occurred because the code was in global scope and suggested adding imports, exports, or forcing moduleDetection to avoid them
 * [today](https://github.com/microsoft/TypeScript/issues/63510#issuecomment-4567233994) **RyanCavanaugh** said "Bot"
 * (today) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** added label `AI Spam`

### [Issue microsoft/TypeScript#63514](https://github.com/microsoft/TypeScript/issues/63514) (Open)

**Reassigning of inferred \`object\` with Indexed access value does not widen it's type**

*Reassigning an inferred object via indexed access in TypeScript fails to widen its type beyond object.*

 * created by **svenvandescheur**
 * [later](https://github.com/microsoft/TypeScript/issues/63514#issuecomment-4573971134) **nmain** asked to verify the example repro and suggested compiler flags might differ
 * [later](https://github.com/microsoft/TypeScript/issues/63514#issuecomment-4574131065) **svenvandescheur** clarified the TS playground example with better comments, explained that any/unknown meant an unknown value rather than strictly any, advised against using object, and confirmed the default flags were unchanged
 * [later](https://github.com/microsoft/TypeScript/issues/63514#issuecomment-4574341742) **MartinJohns** explained that the behavior was by design, noting that a never-typed key yields any for the indexed access and assigning any does not change the variable’s type
 * [later](https://github.com/microsoft/TypeScript/issues/63514#issuecomment-4574532804) **svenvandescheur** questioned why indexed access with a key typed as never became any and why assigning an any value to a variable did not widen its type
 * [later](https://github.com/microsoft/TypeScript/issues/63514#issuecomment-4574809425) **MartinJohns** explained that never was a valid keyof, justified using any for dynamic index access, and referenced related issues and eslint possibilities
 * [later](https://github.com/microsoft/TypeScript/issues/63514#issuecomment-4575229248) **nmain** pointed out that the `as` cast was unsafe and suggested using the @typescript-eslint/no-unsafe-type-assertion rule
 * [later](https://github.com/microsoft/TypeScript/issues/63514#issuecomment-4575913496) **MartinJohns** suggested using the '@typescript-eslint/no-unsafe-type-assertion' rule and clarified thinking about forbidding indexing with any or never types
 * [later](https://github.com/microsoft/TypeScript/issues/63514#issuecomment-4575968627) **nmain** said "https://typescript-eslint.io/rules/no-unsafe-member-access/ handles an any indexer but not a never indexer."

### [Issue microsoft/TypeScript#63515](https://github.com/microsoft/TypeScript/issues/63515) (Closed, `Not a Defect`)

**Excess property check on nested object literals dropped in 6\.0 when parameter is a generic "Exact" mapped\-type guard**

*TypeScript 6.0 stops reporting nested excess properties in object literals when using a generic Exact mapped-type guard.*

 * created by **RHOOPH**
 * [later](https://github.com/microsoft/TypeScript/issues/63515#issuecomment-4576549268) **snarbles2** analyzed type inference differences between TS 5.9.3 and 6.0 and concluded the issue wasn't with EPC

