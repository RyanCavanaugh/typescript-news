# Report for 2026-01-04 (Sunday, January 4th, 2026)

7 different users commented on 6 different issues.

## Recommended Actions

 * Response Recommended
    * @nmain provided an alternative solution using zod and questioned the necessity of the current approach in [microsoft/TypeScript#62944](https://github.com/microsoft/TypeScript/issues/62944#issuecomment-3710383243)
    * @lgarron asked how TypeScript determines if a file is a web worker and reported multiple auto import and indexing issues in [microsoft/TypeScript#62951](https://github.com/microsoft/TypeScript/issues/62951#issuecomment-3710282461)

## Activity Summary

### [Issue microsoft/TypeScript#61770](https://github.com/microsoft/TypeScript/issues/61770) (Open, `Suggestion`, `Awaiting More Feedback`)

**Allow narrowing of unions discriminated by numeric literals using \`\>\` \`\<\` etc**

*TypeScript fails to narrow a [number] | [] union when using args.length > 0, though truthiness or === checks work.*

 * (31 weeks ago) **RyanCavanaugh** added labels `Suggestion`, `Awaiting More Feedback`
 * [31 weeks ago](https://github.com/microsoft/TypeScript/issues/61770#issuecomment-2920822001) **RyanCavanaugh** said "This is implementable using available primitives, just not something that's come up yet."
 * [later](https://github.com/microsoft/TypeScript/issues/61770#issuecomment-3710899811) **Exeteres** provided a simplified TypeScript union type example demonstrating how property narrowing works with equality checks but not with relational checks

### [Issue microsoft/TypeScript#62913](https://github.com/microsoft/TypeScript/issues/62913) (Closed, `Not a Defect`)

**Incorrect rename refactoring in object destructuring**

*Renaming a destructured variable to its original name incorrectly preserves alias syntax instead of simplifying the destructuring.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/62913#issuecomment-3674706268) **dbaeumer** said "https://github.com/user-attachments/assets/11086ffa-dc73-456f-82bf-bd77e64f1ea9"
 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/62913#issuecomment-3674751833) **MartinJohns** said "That's expected to me. You're renaming the variable."
 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/62913#issuecomment-3674755809) **MartinJohns** explained that the behavior was controlled by the setting `javascript.preferences.renameShorthandProperties` / `typescript.preferences.renameShorthandProperties` and pointed to issue #29238
 * [today](https://github.com/microsoft/TypeScript/issues/62913#issuecomment-3709315358) **dbaeumer** explained that the case differed from the referenced issue, argued that an alias was unnecessary, and suggested using a destructuring alias instead

### [Issue microsoft/TypeScript#62944](https://github.com/microsoft/TypeScript/issues/62944) (Open, `Suggestion`, `Declined`)

**Allow inferred object literal optional properties**

*Introduce syntax for inferring optional object literal properties (e.g. prop2?) to allow marking certain properties optional during type inference.*

 * [2 days ago](https://github.com/microsoft/TypeScript/issues/62944#issuecomment-3706222022) **rtcpw** explained that literal object templates in libraries like zod require optional properties to cascade type information and optionality through factory definitions
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/62944#issuecomment-3706224710) **rtcpw** thanked the contributor for suggesting a helper function and said it was a nice workaround
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/62944#issuecomment-3706285199) **MartinJohns** explained that existing helper types could support optional properties and cautioned that the proposed syntax might mislead users
 * [later](https://github.com/microsoft/TypeScript/issues/62944#issuecomment-3710383243) **nmain** mentioned that zod already covered the use case and provided an example

### [Issue microsoft/TypeScript#62951](https://github.com/microsoft/TypeScript/issues/62951) (Closed, `Needs More Info`)

**Preventing \`importScripts\(…\)\` \(ambient declaration\) from being suggested ahead of import statements\.**

*Add a preference to always place import statement completions before ambient importScripts suggestions or remove importScripts from suggestions.*

 * created by **lgarron**
 * [later](https://github.com/microsoft/TypeScript/issues/62951#issuecomment-3709870420) **guillaumebrunerie** suggested that the user's TypeScript configuration was incorrect and recommended using auto imports to add imports automatically
 * [later](https://github.com/microsoft/TypeScript/issues/62951#issuecomment-3710282461) **lgarron** described issues with VS Code auto imports and TypeScript file context detection, including missing suggestions, misindexed files, and import completion errors
 * [later](https://github.com/microsoft/TypeScript/issues/62951#issuecomment-3710541153) **guillaumebrunerie** described how to configure TypeScript to recognize web worker files using a separate tsconfig with the WebWorker lib
 * [later](https://github.com/microsoft/TypeScript/issues/62951#issuecomment-3710760059) **lgarron** stated that lib.d.ts includes WebWorker among its default references and listed them

### [Issue microsoft/TypeScript#62952](https://github.com/microsoft/TypeScript/issues/62952) (Closed, `Bug`, `Fixed`)

**Crash: RangeError: Maximum call stack size exceeded in containsReference when a generic ImportType has malformed arguments in a nested conditional**

*TypeScript crashes with a maximum call stack overflow when nested conditional types reference an improperly parameterized import type.*

 * created by **na7ure-a**

### [Issue microsoft/TypeScript#62954](https://github.com/microsoft/TypeScript/issues/62954) (Open, `Suggestion`, `In Discussion`, `Experimentation Needed`)

**Explicit variance annotations for built\-in \.d\.ts files**

*Proposal to include explicit variance annotations in built-in .d.ts definitions to speed up TypeScript type checking.*

 * created by **akaltar**

