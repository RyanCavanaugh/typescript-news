# Report for 2026-03-08 (Sunday, March 8th, 2026)

8 different users commented on 10 different issues.

## Recommended Actions

 * Response Recommended
    * @umeshmore45 provided information about a fix in PR #63222 in [microsoft/TypeScript#61591](https://github.com/microsoft/TypeScript/issues/61591#issuecomment-4022079373)
    * @psnet asked if there is a stable TS7 release and if it is widely adopted in [microsoft/TypeScript#63149](https://github.com/microsoft/TypeScript/issues/63149#issuecomment-4024819323)

## Activity Summary

### [Issue microsoft/TypeScript#1897](https://github.com/microsoft/TypeScript/issues/1897) (Closed, `Suggestion`, `Declined`)

**Please provide a \`json\` basic type**

*Introduce a built-in json type in TypeScript to accurately model JSON data and resolve existing typing limitations.*

 * [42 weeks ago](https://github.com/microsoft/TypeScript/issues/1897#issuecomment-2884475712) **ceifa** described encountering a type instantiation depth error when using the @yawaramin type with other types and provided a solution by adding a max depth of recursion
 * [42 weeks ago](https://github.com/microsoft/TypeScript/issues/1897#issuecomment-2887684813) **ahrjarrett** suggested using the approach from issue #12936 to implement JsonValue and provided a TypeScript code example with a playground link
 * [42 weeks ago](https://github.com/microsoft/TypeScript/issues/1897#issuecomment-2888230415) **mindplay-dk** said "Maybe when TSGo arrives we can actually have this rather essential feature? ☺️"
 * [later](https://github.com/microsoft/TypeScript/issues/1897#issuecomment-4023572606) **IanBellomy** pointed out missing protection against Infinity and linked a related issue

### [Issue microsoft/TypeScript#28682](https://github.com/microsoft/TypeScript/issues/28682) (Open, `Suggestion`, `In Discussion`, `Domain: Literal Types`)

**Add a \-\-strictNaNChecks option, and a NaN / integer / float type to avoid runtime NaN errors**

*Add a --strictNaNChecks compiler option and dedicated NaN, integer, and float types to prevent runtime NaN errors.*

 * [1.3 years ago](https://github.com/microsoft/TypeScript/issues/28682#issuecomment-2463729154) **Akindin** argued that integer types remain useful for libraries and custom utilities by improving assignability and enabling typeguards
 * [1.3 years ago](https://github.com/microsoft/TypeScript/issues/28682#issuecomment-2463731416) **Akindin** recommended restraining usage of numbers outside valid ranges to prevent infinite loops
 * [1.2 years ago](https://github.com/microsoft/TypeScript/issues/28682#issuecomment-2485657146) **Rudxain** suggested using refinement types with a restricted or alternative predicate language to ensure sanity
 * [later](https://github.com/microsoft/TypeScript/issues/28682#issuecomment-4023538237) **IanBellomy** suggested adding an int type to avoid Infinity in JSON serialization and linked to a related issue

### [Issue microsoft/TypeScript#61591](https://github.com/microsoft/TypeScript/issues/61591) (Open, `Bug`, `Help Wanted`, `Domain: Declaration Emit`)

**TS4055 when generating declaration for return type that uses type of paramter for protected methods**

*Protected methods with return types derived from a parameter's keyof type trigger TS4055/TS4073 errors.*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [46 weeks ago](https://github.com/microsoft/TypeScript/issues/61591#issuecomment-2816024737) **zhanghai** acknowledged that typeof propertyName had no functional benefit and explained they used it to shorten long interface names
 * **RyanCavanaugh** added label `Domain: Declaration Emit`
 * [later](https://github.com/microsoft/TypeScript/issues/61591#issuecomment-4022079373) **umeshmore45** said "Hey, I fixed this in PR #63222."

### [Issue microsoft/TypeScript#62634](https://github.com/microsoft/TypeScript/issues/62634) (Open, `Suggestion`, `Awaiting More Feedback`)

**Suggestion: make hover tooltips more readable by showing the generic parameters names instead of their value \(in some cases\)\.\.**

*Show generic parameter names instead of their full types by default in hover tooltips to improve readability.*

 * **RyanCavanaugh** added label `Awaiting More Feedback`
 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/62634#issuecomment-3874832301) **Ayoub-glitsh** praised the proposal’s DX improvements and offered to help implement a prototype
 * [5 days ago](https://github.com/microsoft/TypeScript/issues/62634#issuecomment-3993576433) **denis-migdal** thanked the respondent and suggested creating a VSCode extension using the TS language server as a proof of concept
 * [later](https://github.com/microsoft/TypeScript/issues/62634#issuecomment-4024718236) **Ayoub-glitsh** suggested building a VS Code extension as a prototype to experiment with displaying generic parameter names and heuristics for hover tooltips

### [Issue microsoft/TypeScript#63100](https://github.com/microsoft/TypeScript/issues/63100) (Closed)

**TS wrong calculate case sensitive repo as case insensitive filesystem**

*TypeScript incorrectly treats case-sensitive overlayfs repositories on macOS as case-insensitive, leading to ESLint file inclusion errors for capitalized filenames.*

 * created by **baymer**
 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/63100#issuecomment-3880022174) **RyanCavanaugh** provided an automatically generated analysis of similar issues with links and similarity percentages
 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/63100#issuecomment-3898662414) **RyanCavanaugh** said "What's a standalone way to repro this (is there one) ?"
 * [later](https://github.com/microsoft/TypeScript/issues/63100#issuecomment-4024578573) **RyanCavanaugh** said "Closing due to lack of repro"
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63149](https://github.com/microsoft/TypeScript/issues/63149) (Closed)

**\[TS\]: Incorrect handling of \`JSDoc\` description of interface property**

*VS Code incorrectly strips parentheses-enclosed JSX tags from interface property JSDoc descriptions in hover tooltips.*

 * **mjbvz** unassigned **mjbvz**
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/63149#issuecomment-3957875823) **adhnannp** said "i will work on this, could you assign this to me @psnet "
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/63149#issuecomment-3961175857) **RyanCavanaugh** provided an automated analysis listing similar issues
 * [later](https://github.com/microsoft/TypeScript/issues/63149#issuecomment-4024765387) **RyanCavanaugh** said "Please test this in TS7 and, if it doesn't work there, log a new issue with an isolated repro. Thanks!"
 * (later) **RyanCavanaugh** closed the issue
 * [later](https://github.com/microsoft/TypeScript/issues/63149#issuecomment-4024819323) **psnet** asked if a stable TS7 release existed and was widely adopted

### [Issue microsoft/TypeScript#63203](https://github.com/microsoft/TypeScript/issues/63203) (Closed, `Suggestion`, `Awaiting More Feedback`)

**Narrow a ternary expression to unique symbol type**

*Enable TypeScript to infer a unique symbol type from a ternary expression whose runtime result is constant.*

 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63203#issuecomment-4008115160) **mitar** suggested opening another issue for Symbol.for concerns and clarified that symbols from Symbol.for and Symbol() should be unique and type-equal
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63203#issuecomment-4008439421) **RyanCavanaugh** clarified that the Symbol.for return type isn't tied to the string literal and that Symbol.for('none') shouldn't be a unique symbol, noting any defect lies here
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63203#issuecomment-4008486650) **mitar** proposed making symbols work like constant string types in a separate namespace and implementing Symbol.for and Symbol() accordingly to match JavaScript behavior
 * [later](https://github.com/microsoft/TypeScript/issues/63203#issuecomment-4024473596) **snarbles2** explained the difference between unique symbols and the global registry and suggested branding symbols for stronger typing
 * [later](https://github.com/microsoft/TypeScript/issues/63203#issuecomment-4024537224) **mkantor** suggested using Symbol.description instead of inventing a custom `_brand` property

### [Issue microsoft/TypeScript#63219](https://github.com/microsoft/TypeScript/issues/63219) (Open, `Suggestion`, `Awaiting More Feedback`)

**Allow primitive LHS to \`instanceof\` operator if RHS is a custom \`hasInstance\`**

*Enable using instanceof with primitive left-hand values when the right-hand side defines a custom Symbol.hasInstance method.*

 * created by **xuld**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63219#issuecomment-4016296812) **MartinJohns** said "Duplicate of #59492."
 * (later) **RyanCavanaugh** added labels `Suggestion`, `Awaiting More Feedback`

### [PR microsoft/TypeScript#63224](https://github.com/microsoft/TypeScript/pull/63224) (Open, `dependencies`, `github_actions`)

**Bump the github\-actions group with 2 updates**

*Upgrade GitHub Actions by bumping actions/setup-node from 6.2.0 to 6.3.0 and updating the github/codeql-action.*

 * created by **dependabot[bot]**
 * (today) **dependabot[bot]** added labels `dependencies`, `github_actions`, `dependencies`, `github_actions`

