# Report for 2026-08-20 (Thursday, August 20th, 2026)

4 different users commented on 3 different issues.

## Recommended Actions

 * Response Recommended
    * @thempatel reported a regression caused by the PR and linked the corresponding issue in [microsoft/TypeScript-go#4775](https://github.com/microsoft/TypeScript-go/pull/4775#issuecomment-5361604061)
    * @johnnyreilly asked if a reported quirk with isolatedDeclarations in transpileModule was meaningful in [microsoft/TypeScript-go#4849](https://github.com/microsoft/TypeScript-go/pull/4849#issuecomment-5358581050)
    * @johnnyreilly provided repro steps and environment details for a panic in transpileDeclaration on Windows in [microsoft/TypeScript-go#4849](https://github.com/microsoft/TypeScript-go/pull/4849#issuecomment-5360469931)

## Activity Summary

### [PR microsoft/TypeScript-go#1966](https://github.com/microsoft/TypeScript-go/pull/1966) (Closed, `No linked issue`, `Unmigrated PR`)

**Add Yarn PnP support**

*Integrate official Yarn Plug’n’Play support into the TypeScript Go compiler to optimize large-scale monorepo builds.*

 * **RyanCavanaugh** added label `Unmigrated PR`
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/1966#issuecomment-5351585811) **RyanCavanaugh** explained that development moved to the main microsoft/TypeScript repository, closed the PR due to lack of transfer functionality, and asked to reopen the change there
 * (yesterday) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/1966#issuecomment-5358472168) **GGomez99** said "PR has been moved to: https://github.com/microsoft/TypeScript/pull/63919 🙇 "

### [PR microsoft/TypeScript-go#4775](https://github.com/microsoft/TypeScript-go/pull/4775) (Closed)

**Retain uninitialized binding patterns for variable declarations in declaration emit**

*Retain uninitialized binding patterns in declaration emit to support exporting binding patterns as isolatedDeclarations.*

 * created by **weswigham**
 * **weswigham** added to milestone `TypeScript 7.1`
 * (3 weeks ago) **weswigham** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/4775#issuecomment-5361604061) **thempatel** said "hey team! i think this PR caused this regression. most of this is over my head but git bisect seems to point to this change"

### [PR microsoft/TypeScript-go#4849](https://github.com/microsoft/TypeScript-go/pull/4849) (Closed)

**Port transpileModule, transpileDeclaration**

*Port TypeScript API methods transpileModule, transpileModuleFromFile, transpileDeclaration, and transpileDeclarationFromFile.*

 * created by **andrewbranch**
 * (1 week ago) **andrewbranch** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/4849#issuecomment-5358581050) **johnnyreilly** reported usage of the new APIs in ts-loader and asked if a noted quirk with isolatedDeclarations in transpileModule was meaningful
 * [today](https://github.com/microsoft/TypeScript-go/pull/4849#issuecomment-5358664733) **andrewbranch** said "Thanks John! Sounds like a bug, will take a look."
 * [today](https://github.com/microsoft/TypeScript-go/pull/4849#issuecomment-5360469931) **johnnyreilly** reported that transpileDeclaration panicked on Windows given an absolute fileName and provided reproduction steps, environment details, and a stack trace

