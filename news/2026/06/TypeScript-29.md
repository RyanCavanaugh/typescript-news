# Report for 2026-06-29 (Monday, June 29th, 2026)

6 different users commented on 9 different issues.

## Recommended Actions

 * Response Recommended
    * @amitbeck reported a CI failure in pull request #13165 in [microsoft/TypeScript#62558](https://github.com/microsoft/TypeScript/issues/62558#issuecomment-4844746669)

## Activity Summary

### [Issue microsoft/TypeScript#48314](https://github.com/microsoft/TypeScript/issues/48314) (Closed, `Needs Investigation`, `Fix Available`, **sheetalkamat**)

**Tsbuild watching packagejson is dependent on whether program was built in the invocation**

*Evaluate whether tsbuild should watch package.json for module resolution changes and how to detect and include it in build dependencies.*

 * (4.2 years ago) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **sheetalkamat**
 * **sheetalkamat** added label `Fix Available`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#62558](https://github.com/microsoft/TypeScript/issues/62558) (Open, `Help Wanted`, `Domain: Declaration Emit`, `Possible Improvement`)

**TS2742 “The inferred type of 'default' cannot be named” with ESLint \`defineConfig\`**

*Using defineConfig from @eslint/config-helpers in a composite TypeScript project triggers TS2742 requiring explicit type annotation.*

 * [37 weeks ago](https://github.com/microsoft/TypeScript/issues/62558#issuecomment-3390997006) **okdecm** reported running into the same issue when building a shareable eslint config
 * [37 weeks ago](https://github.com/microsoft/TypeScript/issues/62558#issuecomment-3396639429) **egorbabintcev** reported encountering the same issue in both shareable eslint configs and regular projects using composite tsconfig
 * **RyanCavanaugh** added label `Domain: Declaration Emit`
 * [later](https://github.com/microsoft/TypeScript/issues/62558#issuecomment-4844746669) **amitbeck** reported encountering a similar issue in a fix to eslint-plugin-turbo, noting a CI failure with a linked error

### [Issue microsoft/TypeScript#63568](https://github.com/microsoft/TypeScript/issues/63568) (Closed, `Needs Investigation`, **ahejlsberg**)

**Regression: 7\.0\.1\-RC Unable to Satisfy Recursive Mapped Type Constraint**

*TypeScript 7.0.1-RC fails to satisfy recursive mapped type constraints that worked in earlier releases.*

 * [6 days ago](https://github.com/microsoft/TypeScript/issues/63568#issuecomment-4783629409) **RyanCavanaugh** presented a simplified TypeScript type example illustrating Wrapped, FromObject, and FromSchema types
 * (5 days ago) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **ahejlsberg**
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript#63597](https://github.com/microsoft/TypeScript/issues/63597) (Open)

**add an option to report an error when \`Symbol\.dispose\`/\`Symbol\.asyncDispose\` objects are used without the \`using\` keyword**

*Add a TypeScript compiler option to error when objects with Symbol.dispose or Symbol.asyncDispose are used without the using keyword.*

 * [today](https://github.com/microsoft/TypeScript/issues/63597#issuecomment-4830914221) **MartinJohns** explained that manual resource management is valid, using database connection pooling and manual disposal at application termination as an example
 * [today](https://github.com/microsoft/TypeScript/issues/63597#issuecomment-4832681103) **DetachHead** questioned whether objects with Symbol.dispose should require using and suggested documentation mention this behavior
 * [today](https://github.com/microsoft/TypeScript/issues/63597#issuecomment-4833162597) **MartinJohns** explained that implementing Symbol.dispose indicates intent to provide explicit resource release and compared it to C#'s IDisposable, then asked how to prevent errors when not using a using statement intentionally
 * [today](https://github.com/microsoft/TypeScript/issues/63597#issuecomment-4838772087) **Renegade334** referred to typescript-eslint/typescript-eslint#8255 to agree that it’s a linter job

### [Issue microsoft/TypeScript#63598](https://github.com/microsoft/TypeScript/issues/63598) (Open)

**"Token end is child end" when '= ${id}id' is used in a property annotation**

*Formatting a property annotation using a malformed template literal triggers a 'Token end is child end' debug failure in TypeScript.*

 * created by **DanielRosenwasser**

### [Issue microsoft/TypeScript#63601](https://github.com/microsoft/TypeScript/issues/63601) (Open)

**@typescript/typescript6 does not have all versions that regular v6 branch has**

*The @typescript/typescript6 npm package lags behind the regular typescript v6 branch, missing versions like 6.0.3.*

 * created by **ZuBB**

### [PR microsoft/TypeScript#63602](https://github.com/microsoft/TypeScript/pull/63602) (Closed, `For Backlog Bug`)

**Fix reachability of code after a try with a branching finally \(\#63583\)**

*Branching finally blocks cause false missing return errors in exhaustive switch-return functions, fixed by disabling shared reachability cache.*

 * created by **CedricConday**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/63602#issuecomment-4844972429) **MartinJohns** reported that Claude failed to read the CLAUDE.md file
 * [later](https://github.com/microsoft/TypeScript/pull/63602#issuecomment-4845360307) **CedricConday** thanked everyone and @MartinJohns for the pointer, acknowledged missing AGENTS.md, noted the repo was in maintenance mode and closed the change as out of scope, and offered to retarget the fix at typescript-go
 * (later) **CedricConday** closed the issue

