# Report for 2026-01-28 (Wednesday, January 28th, 2026)

17 different users commented on 19 different issues.

## Recommended Actions

 * Response Recommended
    * @goestav provided a workaround using zero width space characters with examples in [microsoft/TypeScript#49273](https://github.com/microsoft/TypeScript/issues/49273#issuecomment-3812408981)
    * @kettanaito provided reproduction steps and related links in [microsoft/TypeScript#61524](https://github.com/microsoft/TypeScript/issues/61524#issuecomment-3812451304)
    * @kettanaito provided repro steps including test commands and links in [microsoft/TypeScript#61524](https://github.com/microsoft/TypeScript/issues/61524#issuecomment-3816433446)
    * @pluma asked for the pull request to be reviewed in [microsoft/TypeScript#63046](https://github.com/microsoft/TypeScript/pull/63046#issuecomment-3813202826)
    * @fisker asked if a class extending (B<T>) is equivalent to extending B<T> in [microsoft/TypeScript#63065](https://github.com/microsoft/TypeScript/issues/63065#issuecomment-3818110721)

## Activity Summary

### [Issue microsoft/TypeScript#49273](https://github.com/microsoft/TypeScript/issues/49273) (Open, `Bug`, `Help Wanted`, `Domain: JSDoc`)

**\`@\` character in code block renders poorly in tooltip**

*VS Code hover tooltips fail to render '@' symbols in TypeScript code blocks inside documentation comments.*

 * [3.6 years ago](https://github.com/microsoft/TypeScript/issues/49273#issuecomment-1145144887) **graphemecluster** said "Duplicate of #48976. 😢"
 * [3 years ago](https://github.com/microsoft/TypeScript/issues/49273#issuecomment-1401232357) **KostyaTretyak** said "By the way, this behavior is observed only if there are no characters other than a space before the @ symbol."
 * **RyanCavanaugh** added label `Domain: JSDoc`
 * [today](https://github.com/microsoft/TypeScript/issues/49273#issuecomment-3812408981) **goestav** suggested using zero width space characters as a workaround and provided code examples and screenshots illustrating the behavior

### [Issue microsoft/TypeScript#61524](https://github.com/microsoft/TypeScript/issues/61524) (Open, `Bug`, `Help Wanted`, `Domain: check: Variance Relationships`, `Fix Available`)

**Error: Debug Failure\. No error for last overload signature**

*TypeScript nightly v5.9.0-dev crashes with "Debug Failure. No error for last overload signature" during overload resolution in a generic function.*

 * **RyanCavanaugh** added label `Domain: Variance Relationships`
 * **typescript-bot** added label `Fix Available`
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/61524#issuecomment-3765704531) **janhesters** reported seeing the Debug Failure crash on TypeScript 5.9.3 in a project with heavy generated types and provided detailed reproduction steps
 * [today](https://github.com/microsoft/TypeScript/issues/61524#issuecomment-3812451304) **kettanaito** shared links to a GitHub issue and pull request containing a reproduction test and noted that Vitest hung instead of throwing an error
 * [today](https://github.com/microsoft/TypeScript/issues/61524#issuecomment-3812609059) **Andarist** requested commit information to reproduce the issue
 * [today](https://github.com/microsoft/TypeScript/issues/61524#issuecomment-3814281494) **Andarist** provided a TypeScript reproduction snippet extracted from kettanaito's issue report
 * [later](https://github.com/microsoft/TypeScript/issues/61524#issuecomment-3816433446) **kettanaito** provided reproduction steps for the issue, linking to a pull request and test commands

### [PR microsoft/TypeScript#63031](https://github.com/microsoft/TypeScript/pull/63031) (Closed, `For Milestone Bug`, **RyanCavanaugh**, **Copilot**)

**Change default of \`types\` to \`\[\]\` in tsconfig\.json**

*Default tsconfig.json types array is now empty, with '*' wildcard support to maintain legacy inclusion and boost performance.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/63031#issuecomment-3806941798) **RyanCavanaugh** said "@copilot fix the comments"
 * [yesterday](https://github.com/microsoft/TypeScript/pull/63031#issuecomment-3806983979) **Copilot** addressed all comments, fixed wildcard checking logic in compiler functions, and updated tests in commit 7f169c1
 * [yesterday](https://github.com/microsoft/TypeScript/pull/63031#issuecomment-3807247167) **Copilot** extracted the types wildcard check, created a typesIncludesWildcard() helper function, and updated six occurrences across multiple files
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#63046](https://github.com/microsoft/TypeScript/pull/63046) (Open, `For Backlog Bug`)

**Introduce ES2025 target & Add missing ScriptTargetFeatures**

*Introduce ES2025 compilation target and add missing type definitions for RegExp.escape and Intl.DurationFormat in TypeScript.*

 * **typescript-bot** added label `For Backlog Bug`
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/63046#issuecomment-3795392377) **typescript-bot** thanked the author for the PR, cautioned to preserve TSServer API compatibility, and pinged reviewers for extra review
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/63046#issuecomment-3795392404) **typescript-bot** advised to document breaking changes on the wiki and notify DanielRosenwasser and RyanCavanaugh
 * [today](https://github.com/microsoft/TypeScript/pull/63046#issuecomment-3813202826) **pluma** said "Can we please get this reviewed? I know the country is burning and everyone is being replaced by AI but this would be really useful for those of us who deal with audiences across different languages."
 * [today](https://github.com/microsoft/TypeScript/pull/63046#issuecomment-3813940828) **jakebailey** said "We have a lot of these lib related PRs; it's absolutely our intention to review all of them as soon as we can, we've just had a bunch of other stuff that has been a bit more pressing."
 * [today](https://github.com/microsoft/TypeScript/pull/63046#issuecomment-3813947467) **jakebailey** noted that mixing esnext and ES2025 changes in a single PR made it hard to distinguish new work from moves and suggested reviewing individual ESNext PRs and creating a dedicated ES2025 PR
 * [today](https://github.com/microsoft/TypeScript/pull/63046#issuecomment-3814011569) **petamoriken** explained that only two files were added and offered to split the PR if preferred

### [PR microsoft/TypeScript#63052](https://github.com/microsoft/TypeScript/pull/63052) (Closed, `For Backlog Bug`)

**feat: comprehensive Type Hierarchy LSP support**

*Implement comprehensive LSP Type Hierarchy support in the TypeScript service, enabling supertype and subtype navigation for classes, interfaces, and type aliases.*

 * **typescript-bot** added label `For Backlog Bug`
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/63052#issuecomment-3796968192) **jakebailey** advised that the PR would not be accepted and suggested sending it to the typescript-go repo or waiting until this repo becomes the Go code
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/63052#issuecomment-3796975568) **kbrilla** acknowledged the suggestion and thanked the contributor for the information
 * [later](https://github.com/microsoft/TypeScript/pull/63052#issuecomment-3817674049) **kbrilla** migrated the PR to the microsoft/typescript-go repository
 * [later](https://github.com/microsoft/TypeScript/pull/63052#issuecomment-3817674958) **kbrilla** said "migrated to https://github.com/microsoft/typescript-go/pull/2602 "
 * (later) **kbrilla** closed the issue

### [PR microsoft/TypeScript#63055](https://github.com/microsoft/TypeScript/pull/63055) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Support FORCE\_COLOR**

*Add support for the FORCE_COLOR environment variable to force colored console output.*

 * (yesterday) **typescript-bot** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#63056](https://github.com/microsoft/TypeScript/pull/63056) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Eliminate \`tests/lib/lib\.d\.ts\`, fix up fourslash to use real libs and defaults**

*Overhauled fourslash tests by removing tests/lib/lib.d.ts, using real standard libs with caching, and fixing option handling.*

 * (yesterday) **typescript-bot** added labels `Author: Team`, `For Uncommitted Bug`
 * [yesterday](https://github.com/microsoft/TypeScript/pull/63056#issuecomment-3808793633) **jakebailey** said "I'll note that after this, there's no reason to have @libFiles at all; the only uses are for react.d.ts which can be loaded via a triple-slash reference just fine."
 * [today](https://github.com/microsoft/TypeScript/pull/63056#issuecomment-3812836599) **jakebailey** said "This is inconsistently OOMing the Mac runners. I guess I'll have to go look to see if I've increased memory usage with this or something."
 * [today](https://github.com/microsoft/TypeScript/pull/63056#issuecomment-3812890603) **jakebailey** showed before-and-after images and noted file size increased from 25GB to 40GB
 * [today](https://github.com/microsoft/TypeScript/pull/63056#issuecomment-3812899518) **jakebailey** said "It's the caching registry I added; it must be subtly wrong."
 * [today](https://github.com/microsoft/TypeScript/pull/63056#issuecomment-3813131181) **jakebailey** attached a screenshot and indicated success
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#63057](https://github.com/microsoft/TypeScript/issues/63057) (Closed, `Working as Intended`)

**Module resolution: self\-references file are resolved after 5\.7**

*Updating to TypeScript 5.7+ causes self-referenced imports outside the configured rootDir to fail resolution with “file is not under rootDir” errors.*

 * created by **FoundTheWOUT**
 * **RyanCavanaugh** added label `Working as Intended`
 * [today](https://github.com/microsoft/TypeScript/issues/63057#issuecomment-3813057040) **RyanCavanaugh** said "This is a correct error. The resolution resolved to a .ts file, not a .d.ts file. You need to have built a first in this scenario, and/or used a project reference."
 * [today](https://github.com/microsoft/TypeScript/issues/63057#issuecomment-3815368718) **FoundTheWOUT** thanked the maintainer, described complex dependency issues, applied a rootDir-based exports configuration, noted an auto-import path problem, and switched to building types for the entire library
 * (today) **FoundTheWOUT** closed the issue

### [Issue microsoft/TypeScript#63058](https://github.com/microsoft/TypeScript/issues/63058) (Closed, `Not a Defect`)

**Partial\<\> with generics is throwing: Type 'xxx' is not assignable to type 'Partial\<T\>'\.**

*TypeScript rejects returning `{ time: 0 }` from a generic getPartial<T extends Timed>() as Partial<T> while the same literal assignment to a Partial<T> variable compiles.*

 * created by **jozefchutka**
 * [today](https://github.com/microsoft/TypeScript/issues/63058#issuecomment-3811349951) **MartinJohns** explained why the error was correct for getPartial and identified an issue in getPartial2 while referencing issue #9825
 * [today](https://github.com/microsoft/TypeScript/issues/63058#issuecomment-3811843827) **jcalz** mentioned a StackOverflow question and issue #51645 related to getPartial(), explained that indexing a generic variable with a specific key widens it to its constraint causing unsoundness, and noted no specific issue exists
 * **RyanCavanaugh** added label `Not a Defect`

### [Issue microsoft/TypeScript#63059](https://github.com/microsoft/TypeScript/issues/63059) (Open, `Suggestion`, `Awaiting More Feedback`)

**Narrow object property indexed by another object's property of unique symbol type \(like \`Symbol\.iterator\`\)**

*Allow TypeScript’s type narrowing to work for bracket notation property access when the key is a unique symbol property of an object*

 * created by **jcalz**

### [PR microsoft/TypeScript#63060](https://github.com/microsoft/TypeScript/pull/63060) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Remove compiler runner libFiles option entirely**

*Remove the compiler runner’s libFiles option and standardize on reference paths for including .lib files.*

 * created by **jakebailey**
 * (today) **typescript-bot** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#63061](https://github.com/microsoft/TypeScript/issues/63061) (Open, `Not a Defect`)

**\`export type\` vs \`export { type }\` with augmentations**

*export { type } re-exports do not allow module augmentations to access types, unlike export type*

 * created by **skirtles-code**
 * [later](https://github.com/microsoft/TypeScript/issues/63061#issuecomment-3817254000) **mkantor** said "I just tested typescript-go and the behavior is the same there (perhaps this issue should be filed in that repository; see #62827)."

### [Issue microsoft/TypeScript#63062](https://github.com/microsoft/TypeScript/issues/63062) (Closed)

**Request to Participate and Share Academic Survey on Code Review in OSS Security**

*Request permission to share an anonymous academic survey on how developers identify security issues during OSS code reviews.*

 * created by **morshedniaz**

### [Issue microsoft/TypeScript#63063](https://github.com/microsoft/TypeScript/issues/63063) (Closed)

**JSDoc comments containing glob patterns \(e\.g\., \`\*\*/\*\.md\`\) incorrectly parsed as TypeScript code**

*TypeScript incorrectly parses glob patterns like **/*.md within JSDoc comments as code, causing syntax errors across multiple versions.*

 * created by **cc01cc**
 * [later](https://github.com/microsoft/TypeScript/issues/63063#issuecomment-3817668040) **MartinJohns** explained that */ ends multiline comments in JavaScript and advised escaping the slash (e.g. **\\/*.md).
 * [later](https://github.com/microsoft/TypeScript/issues/63063#issuecomment-3817715996) **cc01cc** thanked the commenter and confirmed that escaping the slash (`**\/*.md`) resolves the issue
 * (later) **cc01cc** closed the issue

### [PR microsoft/TypeScript#63064](https://github.com/microsoft/TypeScript/pull/63064) (Open, `For Backlog Bug`)

**fix\(lib\): reorder Array\#reduce/reduceRight overloads in lib\.d\.ts**

*Reorder Array#reduce and reduceRight overloads in lib.d.ts to prioritize the generic initialValue overload and fix type inference*

 * created by **taronsung**
 * **typescript-bot** added label `For Backlog Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/63064#issuecomment-3817773533) **taronsung** said "@microsoft-github-policy-service agree"

### [Issue microsoft/TypeScript#63065](https://github.com/microsoft/TypeScript/issues/63065) (Closed, `Question`)

**Is \`\`class A extends \(B\<T\>\)\<T\> {}\`\` valid code?**

*Asking whether the syntax `class A extends (B<T>)<T> {}` is valid TypeScript code without errors.*

 * created by **fisker**
 * [later](https://github.com/microsoft/TypeScript/issues/63065#issuecomment-3818110721) **fisker** asked if extending (B<T>) and B<T> produced the same behavior
 * [later](https://github.com/microsoft/TypeScript/issues/63065#issuecomment-3818424016) **mkantor** observed multiple errors in the linked playground and noted that some remained after defining B and T
 * [later](https://github.com/microsoft/TypeScript/issues/63065#issuecomment-3818446531) **mkantor** clarified that the two cases weren't equivalent and explained that parentheses likely create an instantiation expression

