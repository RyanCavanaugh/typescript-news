# Report for 2026-05-29 (Friday, May 29th, 2026)

5 different users commented on 6 different issues.

## Recommended Actions

 * Response Recommended
    * @jacekkopecky provided repro steps and a simplified example in [microsoft/TypeScript#43429](https://github.com/microsoft/TypeScript/issues/43429#issuecomment-4583036195)

## Activity Summary

### [Issue microsoft/TypeScript#41548](https://github.com/microsoft/TypeScript/issues/41548) (Closed, `Bug`, `Fix Available`, `Domain: check: Excess Property Checking`, `Has Repro`, **Copilot**)

**Compile error if I named last array destructuring element\.**

*TypeScript incorrectly flags an excess property error for objects passed to a generic function when using array destructuring that binds only the last element.*

 * **typescript-bot** added label `Fix Available`
 * **RyanCavanaugh** added label `Domain: Excess Property Checking`
 * [6 days ago](https://github.com/microsoft/TypeScript/issues/41548#issuecomment-4524987622) **heroboy** observed that the code had no errors in version 6.0.3 and asked if the issue was fixed
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript#43429](https://github.com/microsoft/TypeScript/issues/43429) (Open, `Bug`, `Domain: check: Type Inference`)

**Spread Tuple Union In Function Errors**

*Spreading a union of fixed-length tuples into function parameters incorrectly triggers a TypeScript error by treating the tuple as empty.*

 * (5.1 years ago) **RyanCavanaugh** added labels `Bug`, `Domain: Type Inference`, and set milestone to `Backlog`
 * [later](https://github.com/microsoft/TypeScript/issues/43429#issuecomment-4583036195) **jacekkopecky** demonstrated a simpler reproduction where a union of constant tuples was not recognized as a tuple type and triggered a spread argument error

### [Issue microsoft/TypeScript#63514](https://github.com/microsoft/TypeScript/issues/63514) (Closed, `Not a Defect`)

**Reassigning of inferred \`object\` with Indexed access value does not widen it's type**

*Reassigning an inferred object via indexed access in TypeScript fails to widen its type beyond object.*

 * [today](https://github.com/microsoft/TypeScript/issues/63514#issuecomment-4575229248) **nmain** pointed out that the `as` cast was unsafe and suggested using the @typescript-eslint/no-unsafe-type-assertion rule
 * [today](https://github.com/microsoft/TypeScript/issues/63514#issuecomment-4575913496) **MartinJohns** suggested using the '@typescript-eslint/no-unsafe-type-assertion' rule and clarified thinking about forbidding indexing with any or never types
 * [today](https://github.com/microsoft/TypeScript/issues/63514#issuecomment-4575968627) **nmain** said "https://typescript-eslint.io/rules/no-unsafe-member-access/ handles an any indexer but not a never indexer."
 * [today](https://github.com/microsoft/TypeScript/issues/63514#issuecomment-4577327383) **svenvandescheur** explained that never is a valid keyof and that any opts out of type checks, referenced related issues, and noted that defaulting to any and never feels counterintuitive versus using unknown or treating never as a noop
 * [today](https://github.com/microsoft/TypeScript/issues/63514#issuecomment-4577403452) **nmain** explained that the `never` type contains no values, thus satisfies all predicates, and that asserting a value as `never` implies unreachable code

### [Issue microsoft/TypeScript#63515](https://github.com/microsoft/TypeScript/issues/63515) (Closed, `Not a Defect`)

**Excess property check on nested object literals dropped in 6\.0 when parameter is a generic "Exact" mapped\-type guard**

*TypeScript 6.0 stops reporting nested excess properties in object literals when using a generic Exact mapped-type guard.*

 * created by **RHOOPH**
 * [today](https://github.com/microsoft/TypeScript/issues/63515#issuecomment-4576549268) **snarbles2** analyzed type inference differences between TS 5.9.3 and 6.0 and concluded the issue wasn't with EPC
 * **RyanCavanaugh** added label `Not a Defect`
 * [today](https://github.com/microsoft/TypeScript/issues/63515#issuecomment-4577630364) **RyanCavanaugh** explained that simulated exact types aren't perfect and that two different function signatures having different behavior isn't a bug

### [PR microsoft/TypeScript#63516](https://github.com/microsoft/TypeScript/pull/63516) (Closed, `For Backlog Bug`, `Voight-Kampff Anomaly`)

**Update toFixed/toExponential/toPrecision digit range in docs to match the spec**

*Update Number.prototype.toFixed, toExponential, and toPrecision documentation to reflect the ES2018 spec’s increased digit limits of 0–100 and 1–100.*

 * created by **ibondarenko1**
 * **typescript-bot** added label `For Backlog Bug`

