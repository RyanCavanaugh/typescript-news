# Report for 2026-02-10 (Tuesday, February 10th, 2026)

11 different users commented on 41 different issues.

## Recommended Actions

 * Response Recommended
    * @AFatNiBBa asked how to express the constructor behavior in the type of `f` in [microsoft/TypeScript#63126](https://github.com/microsoft/TypeScript/issues/63126#issuecomment-3884625398)
    * @AFatNiBBa pointed out workaround failure when the function is not called directly and clarified expectations for noCtor in [microsoft/TypeScript#63126](https://github.com/microsoft/TypeScript/issues/63126#issuecomment-3884682547)

## Activity Summary

### [Issue microsoft/TypeScript#14841](https://github.com/microsoft/TypeScript/issues/14841) (Open, `Suggestion`, `Domain: LS: Completion Lists`, `Experience Enhancement`)

**Autocompletion for mapped type with inferred keys and values all the same\.**

*Autocomplete doesn't suggest the 'x' property for object literals matching a mapped type with uniform inferred value types.*

 * **RyanCavanaugh** added to milestone `Future`
 * **weswigham** removed label `Suggestion`
 * **RyanCavanaugh** added label `Suggestion`
 * [today](https://github.com/microsoft/TypeScript/issues/14841#issuecomment-3880250387) **mkantor** said "This has been addressed. As far back as TypeScript 4.1 I see x suggested in your example code."

### [Issue microsoft/TypeScript#26662](https://github.com/microsoft/TypeScript/issues/26662) (Open, `Suggestion`, `Domain: LS: Completion Lists`, `VS Code Tracked`, `Experience Enhancement`)

**Intellisense for generic parameterized string literal function arguments not working**

*VSCode Intellisense fails to suggest string literal keys for a generic function’s parameter after typing begins.*

 * [7.4 years ago](https://github.com/microsoft/TypeScript/issues/26662#issuecomment-415883222) **njgraf512** asked for confirmation on what 'mid-call' referred to and suggested adding string suggestions to the autocomplete list
 * **weswigham** removed label `Suggestion`
 * **RyanCavanaugh** added label `Suggestion`
 * [today](https://github.com/microsoft/TypeScript/issues/26662#issuecomment-3880281227) **mkantor** mentioned inability to reproduce the described behavior in the playground using TypeScript versions as old as 3.3

### [Issue microsoft/TypeScript#37700](https://github.com/microsoft/TypeScript/issues/37700) (Closed, `Suggestion`, `Declined`)

**Optional chaining of unknown should be unknown**

*Allow optional chaining on values with unknown type, yielding unknown result instead of a type error.*

 * [2.5 years ago](https://github.com/microsoft/TypeScript/issues/37700#issuecomment-1676285550) **zanminkian** pointed out that the code would cause a TypeScript compile error and that using 'any' or type assertions to fix it is discouraged
 * [1 year ago](https://github.com/microsoft/TypeScript/issues/37700#issuecomment-2618294005) **NicholasAntidormi** asked to reconsider disallowing optional chaining on `unknown`, noting it reduces utility and forces boilerplate with examples
 * [13 weeks ago](https://github.com/microsoft/TypeScript/issues/37700#issuecomment-3502891186) **JuanGalilea** suggested that allowing optional chaining on any object property would reduce the painpoints of Object.keys returning string[] instead of keyof T
 * [later](https://github.com/microsoft/TypeScript/issues/37700#issuecomment-3884374420) **grundb** provided a helper function that performs a sequence of optional chaining property accesses on an unknown input
 * [later](https://github.com/microsoft/TypeScript/issues/37700#issuecomment-3884443938) **adrian-gierakowski** critiqued the helper function as overly heavy-handed and noted that the result should only be unknown when chaining on an unknown input
 * [later](https://github.com/microsoft/TypeScript/issues/37700#issuecomment-3884461544) **grundb** acknowledged that the helper function was heavy-handed but handled the common case of chaining unknown values
 * [later](https://github.com/microsoft/TypeScript/issues/37700#issuecomment-3884491782) **adrian-gierakowski** provided a TypeScript implementation of an optionalChain function with a recursive GetPath type and demonstrated its behavior through various usage examples
 * [later](https://github.com/microsoft/TypeScript/issues/37700#issuecomment-3884786810) **mfulton26** said "https://github.com/sindresorhus/dot-prop can be used to "get, set, or delete a property from a nested object using a dot path [or an array path]" that will return undefined for nonexistent paths."

### [Issue microsoft/TypeScript#47518](https://github.com/microsoft/TypeScript/issues/47518) (Open, `Suggestion`, `Help Wanted`, `Domain: LS: Completion Lists`, `Experience Enhancement`)

**Missing IntelliSense suggestions in a partial mapped generic argument**

*IntelliSense suggestions are missing for valid mapped type properties in inline Partial generic arguments in TypeScript 4.5.4.*

 * (4 years ago) **RyanCavanaugh** added labels `Suggestion`, `Help Wanted`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/47518#issuecomment-3880263626) **mkantor** said "This seems to have been addressed. In TypeScript 4.6 and later I see only getProp1 and getProp2 in the suggestions."

### [PR microsoft/TypeScript#58000](https://github.com/microsoft/TypeScript/pull/58000) (Closed, **sheetalkamat**)

**Reduce timeout for symlink Watching tests**

*Reduce the default timeout for symlink watching tests to speed up test execution and prevent delays.*

 * (1.8 years ago) **sheetalkamat** closed the issue
 * [26 weeks ago](https://github.com/microsoft/TypeScript/pull/58000#issuecomment-3178337557) **sgnobst** commended the code changes and noted no significant issues
 * [26 weeks ago](https://github.com/microsoft/TypeScript/pull/58000#issuecomment-3178351099) **sgnobst** commended the code changes and noted no significant issues
 * **typescript-bot** assigned to **sheetalkamat**

### [Issue microsoft/TypeScript#62868](https://github.com/microsoft/TypeScript/issues/62868) (Closed, `Design Notes`)

**Design Meeting Notes, 12/9/2025**

*Plan to merge and backport new moduleResolution options supporting '#/*' package.json imports for bundler, nodenext, and Node20.*

 * created by **DanielRosenwasser**
 * **DanielRosenwasser** added label `Design Notes`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63092](https://github.com/microsoft/TypeScript/issues/63092) (Open)

**Crash: RangeError: Maximum call stack size exceeded in isReachableFlowNodeWorker with complex for loop headers**

*TypeScript's compiler crashes with a maximum call stack size exceeded error when analyzing reachability in complex for loop headers.*

 * created by **na7ure-a**
 * [6 days ago](https://github.com/microsoft/TypeScript/issues/63092#issuecomment-3849747076) **Andarist** provided a repro case that might point at the root cause
 * [today](https://github.com/microsoft/TypeScript/issues/63092#issuecomment-3880022124) **RyanCavanaugh** provided an automated analysis with a list of similar issues

### [Issue microsoft/TypeScript#63100](https://github.com/microsoft/TypeScript/issues/63100) (Open)

**TS wrong calculate case sensitive repo as case insensitive filesystem**

*TypeScript incorrectly treats case-sensitive overlayfs repositories on macOS as case-insensitive, leading to ESLint file inclusion errors for capitalized filenames.*

 * created by **baymer**
 * [today](https://github.com/microsoft/TypeScript/issues/63100#issuecomment-3880022174) **RyanCavanaugh** provided an automatically generated analysis of similar issues with links and similarity percentages

### [Issue microsoft/TypeScript#63109](https://github.com/microsoft/TypeScript/issues/63109) (Open)

**Clarify tsconfig extends resolution**

*Clarify and update tsconfig.json 'extends' resolution documentation to explain Node.js-style specifier handling.*

 * created by **valler**
 * [today](https://github.com/microsoft/TypeScript/issues/63109#issuecomment-3880022212) **RyanCavanaugh** provided an auto-generated list of similar issues

### [Issue microsoft/TypeScript#63112](https://github.com/microsoft/TypeScript/issues/63112) (Open)

**Infer works differently for interface and type alias**

*TypeScript infer in conditional types correctly matches index signatures on type aliases but fails for interfaces.*

 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63112#issuecomment-3864688383) **UnVuTWFu** described wanting to pass a generic type and extract specific types via conditional types, noted interface returned never while type alias worked
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63112#issuecomment-3864767667) **mkantor** asked if the provided code snippet matched the requirements
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63112#issuecomment-3864946734) **MartinJohns** stated that it compiled just fine
 * [today](https://github.com/microsoft/TypeScript/issues/63112#issuecomment-3880022274) **RyanCavanaugh** provided an auto-generated list of similar issues and suggested closing if duplicate

### [Issue microsoft/TypeScript#63114](https://github.com/microsoft/TypeScript/issues/63114) (Open)

**No autocomplete suggestions for object property values within type arguments**

*TypeScript 5.9.3 fails to show autocomplete suggestions for string literal object property values used as generic type arguments.*

 * created by **jedwards1211**
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63114#issuecomment-3865154812) **mkantor** noted that the issue was fixed in v6.0.0-dev.20260204 by PR #62170
 * [today](https://github.com/microsoft/TypeScript/issues/63114#issuecomment-3880022345) **RyanCavanaugh** thanked the user and listed similar issues with related percentages

### [Issue microsoft/TypeScript#63115](https://github.com/microsoft/TypeScript/issues/63115) (Open)

**Support loading remote types**

*Enable TypeScript to load remote type definitions in config files via URLs, removing the need for type-only dependencies.*

 * created by **danciudev**
 * [today](https://github.com/microsoft/TypeScript/issues/63115#issuecomment-3879372756) **nmain** dismissed adding package management features to TypeScript, noting their package manager already provides integrity checks, dependency management, caching, security audits, version resolution, and more, and that typeAcquisition only covers a limited non-.ts use case
 * [today](https://github.com/microsoft/TypeScript/issues/63115#issuecomment-3879591843) **danciudev** clarified that the proposal adds a type discovery mechanism akin to JSON $schema rather than a dependency manager to save on unnecessary package installation traffic
 * [today](https://github.com/microsoft/TypeScript/issues/63115#issuecomment-3882810476) **guillaumebrunerie** clarified that devDependencies is the perfect solution since tools like eslint must be installed and type definitions should match the project version

### [Issue microsoft/TypeScript#63121](https://github.com/microsoft/TypeScript/issues/63121) (Open)

**Display files with errors summary in \`\-\-watch\` mode**

*Enhance tsc --watch to display a summary of files with errors and their counts after each compilation*

 * created by **dwjohnston**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63121#issuecomment-3874818261) **Ayoub-glitsh** offered to implement a file-level error summary in --watch mode pending maintainer approval
 * [today](https://github.com/microsoft/TypeScript/issues/63121#issuecomment-3880022447) **RyanCavanaugh** provided an automated list of similar issues

### [PR microsoft/TypeScript#63124](https://github.com/microsoft/TypeScript/pull/63124) (Closed, `For Uncommitted Bug`)

**feat\(watch\): show file\-level error summary in watch mode**

*Update watch mode to display a detailed per-file error summary using getErrorSummaryText and a new diagnostic message*

 * **typescript-bot** added label `For Uncommitted Bug`
 * [yesterday](https://github.com/microsoft/TypeScript/pull/63124#issuecomment-3871128563) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [yesterday](https://github.com/microsoft/TypeScript/pull/63124#issuecomment-3872885080) **suvendukungfu** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript/pull/63124#issuecomment-3879594789) **RyanCavanaugh** said "https://github.com/microsoft/TypeScript/blob/main/CONTRIBUTING.md#note"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63125](https://github.com/microsoft/TypeScript/issues/63125) (Open)

**Inline typing for object destructuring in function parameters**

*Enable inline type annotations for object destructuring in function parameters to avoid redundant type repetition.*

 * created by **benhatsor**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63125#issuecomment-3874804343) **MartinJohns** said "Duplicate of #29526."
 * [today](https://github.com/microsoft/TypeScript/issues/63125#issuecomment-3879406232) **RyanCavanaugh** said "@Ayoub-glitsh turn off your script"
 * [today](https://github.com/microsoft/TypeScript/issues/63125#issuecomment-3879681439) **Ayoub-glitsh** said "@RyanCavanaugh noted "

### [Issue microsoft/TypeScript#63126](https://github.com/microsoft/TypeScript/issues/63126) (Open)

**Overloads should be filtered by unmet constraints of type parameters**

*TypeScript should filter out overloaded signatures with unmet type parameter constraints, showing only the compatible overload.*

 * created by **AFatNiBBa**
 * [later](https://github.com/microsoft/TypeScript/issues/63126#issuecomment-3884338049) **snarbles2** expressed concern about unintended silent member disappearance and suggested that permissible arguments shouldn't be constrained, illustrating with a code example
 * [later](https://github.com/microsoft/TypeScript/issues/63126#issuecomment-3884625398) **AFatNiBBa** explained that the call and constructor signatures of `f` are separate, demonstrated with examples how returning a primitive in a constructor is ignored at runtime, and requested a way to express this behavior in `f`’s type
 * [later](https://github.com/microsoft/TypeScript/issues/63126#issuecomment-3884682547) **AFatNiBBa** noted that the workaround failed when the function wasn’t called directly, demonstrated the difference in inferred types with original, workaround, and noCtor, and argued that noCtor should work since Array.flatMap doesn’t accept constructors

