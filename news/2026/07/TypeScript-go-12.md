# Report for 2026-07-12 (Saturday, July 11th, 2026)

8 different users commented on 9 different issues.

## Recommended Actions

 * Response Recommended
    * @XiNiHa asked if the behavior was intended and should be fixed from the library side in [microsoft/TypeScript-go#4579](https://github.com/microsoft/TypeScript-go/issues/4579#issuecomment-4949748665)

## Activity Summary

### [Issue microsoft/TypeScript-go#4572](https://github.com/microsoft/TypeScript-go/issues/4572) (Open)

**Overloaded assertion in inferred\-return function expression loses destructured discriminant narrowing**

*An overloaded assert in an arrow function without a return type annotation prevents TypeScript from narrowing a destructured discriminant property.*

 * created by **adri1wald**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4572#issuecomment-4947548278) **Andarist** said "bisects to https://github.com/microsoft/typescript-go/pull/2542 , potential fix at https://github.com/microsoft/typescript-go/pull/4606"

### [Issue microsoft/TypeScript-go#4579](https://github.com/microsoft/TypeScript-go/issues/4579) (Open)

**tsgo typechecks slower than TS6**

*tsgo typechecking is over five times slower than TypeScript 6 on the same codebase.*

 * created by **XiNiHa**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4579#issuecomment-4948371190) **ahejlsberg** attributed the performance regression to a change in #3445, explained that TS7's deeper analysis led to more type instantiations compared to TS6, and suggested simplifying the types
 * [today](https://github.com/microsoft/TypeScript-go/issues/4579#issuecomment-4949748665) **XiNiHa** said "Do you mean the behavior is expected/intended? Should it be fixed from the library side?"

### [PR microsoft/TypeScript-go#4605](https://github.com/microsoft/TypeScript-go/pull/4605) (Open)

**Fix hover crash for generic members of merged aliases**

*Prevents hover crashes when inspecting generic members of merged type aliases.*

 * created by **Andarist**

### [PR microsoft/TypeScript-go#4606](https://github.com/microsoft/TypeScript-go/pull/4606) (Open)

**Keep dependent destructuring narrowing during re\-entrant checks**

*Preserve narrowed types of dependent destructured variables during re-entrant type checking.*

 * created by **Andarist**

### [Issue microsoft/TypeScript-go#4607](https://github.com/microsoft/TypeScript-go/issues/4607) (Open, `Crash`)

**TypeScript 7\.0 Can't compile \`webpack\`**

*TypeScript 7.0 compiler panics with unexpected JSTypeAliasDeclaration nodes while compiling webpack*

 * created by **avivkeller**
 * **avivkeller** added label `Crash`

### [Issue microsoft/TypeScript-go#4608](https://github.com/microsoft/TypeScript-go/issues/4608) (Open)

**Identical resolved program produces 157 vs 662,155 diagnostics depending on whether the tsconfig is passed directly or through a pass\-through extends**

*Using a pass-through tsconfig that simply extends the main config results in drastically more TypeScript diagnostics than direct config usage.*

 * created by **michaeldanish**

### [Issue microsoft/TypeScript-go#4609](https://github.com/microsoft/TypeScript-go/issues/4609) (Open)

**Extensionless root file panics the compiler: "ScriptKind must be specified when parsing source file"**

*TypeScript 7's compiler panics with a 'ScriptKind must be specified' error when parsing extensionless root files.*

 * created by **elibarzilay**

### [Issue microsoft/TypeScript-go#4610](https://github.com/microsoft/TypeScript-go/issues/4610) (Open, `Domain: Editor`)

**Renaming a file can be very slow in some edge cases**

*File renames with tsgo in VSCode can take 15s due to quadratic import specifier updates on certain .d.ts files.*

 * created by **pascalspadone**
 * **pascalspadone** added label `Domain: Editor`

### [PR microsoft/TypeScript-go#4611](https://github.com/microsoft/TypeScript-go/pull/4611) (Open)

**Update \_scripts tooling deps and lockfiles**

*Update _scripts tooling dependencies, regenerate lockfiles, and add devcontainer lockfile for merging into main.*

 * created by **MasterTLF**
 * [later](https://github.com/microsoft/TypeScript-go/pull/4611#issuecomment-4951714474) **MasterTLF** said "@microsoft-github-policy-service agree"

