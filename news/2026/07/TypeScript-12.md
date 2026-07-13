# Report for 2026-07-12 (Sunday, July 12th, 2026)

2 different users commented on 9 different issues.

## Recommended Actions

 * Response Recommended
    * @dilame provided repro steps as requested in [microsoft/TypeScript#54206](https://github.com/microsoft/TypeScript/issues/54206#issuecomment-4957193622)

## Activity Summary

### [Issue microsoft/TypeScript#54206](https://github.com/microsoft/TypeScript/issues/54206) (Open, `Needs Investigation`, **rbuckton**)

**Incorrect class \#private fields initialization order with target ES2022 and useDefineForClassFields set to false **

*TypeScript 5.0.4 incorrectly orders private class field initialization under ES2022 target with useDefineForClassFields disabled.*

 * (2 years ago) **RyanCavanaugh** set milestone to `TypeScript 5.6.0`, and removed from milestone `TypeScript 5.1.1`
 * [1.4 years ago](https://github.com/microsoft/TypeScript/issues/54206#issuecomment-2645137837) **parzhitsky** explained preferring inline field initialization and assumed it should work for private fields given TypeScript behavior described in an issue comment
 * [later](https://github.com/microsoft/TypeScript/issues/54206#issuecomment-4957193622) **dilame** confirmed the issue still reproduced on both stable and nightly, provided compiler options and minimal repro code, and detailed the runtime failure and workaround

### [Issue microsoft/TypeScript#55908](https://github.com/microsoft/TypeScript/issues/55908) (Open, `Suggestion`, `Awaiting More Feedback`)

**Keyword for inferring a new type from destructured parameters**

*Add a new from keyword to allow TypeScript to infer parameter types from destructured object types*

 * (2.7 years ago) **RyanCavanaugh** added labels `Suggestion`, `Awaiting More Feedback`
 * [2.2 years ago](https://github.com/microsoft/TypeScript/issues/55908#issuecomment-2045729363) **Yona-Appletree** suggested enabling type inference for destructured function arguments in defineAction
 * [later](https://github.com/microsoft/TypeScript/issues/55908#issuecomment-4956529812) **denis-migdal** suggested using Partial<Person> in the satisfies clause and Partial<Context> in the defineAction signature

### [Issue microsoft/TypeScript#63643](https://github.com/microsoft/TypeScript/issues/63643) (Open)

**Reusable callbacks: When destructuring, missing properties should be excluded from the infered type\.**

*TypeScript should infer destructured callback parameters using only the referenced properties instead of requiring the entire type.*

 * created by **denis-migdal**

