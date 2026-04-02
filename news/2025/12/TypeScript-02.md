# Report for 2025-12-02 (Tuesday, December 2nd, 2025)

22 different users commented on 519 different issues.

## Activity Summary

### [Issue microsoft/TypeScript#10040](https://github.com/microsoft/TypeScript/issues/10040) (Closed, `Bug`, `Help Wanted`, `Domain: Formatter`, `7.0 LS Migration`)

**TSX related formatting bugs**

*TSX elements and attributes in TypeScript 2.0 beta misindent cursor and formatting in open and self-closing tags.*

 * **mhegazy** added to milestone `Community`
 * (6.7 years ago) **RyanCavanaugh** set milestone to `Backlog`, and removed from milestone `Community`
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/10040#issuecomment-3604485055) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#10091](https://github.com/microsoft/TypeScript/issues/10091) (Closed, `Bug`, `Help Wanted`, `VS Code Tracked`, `Domain: LS: Quick Info`, `7.0 LS Migration`)

**Inconsistent DocComment merging for merged declarations**

*VSCode’s TypeScript support inconsistently merges JSDoc comments for merged function, interface, and namespace declarations.*

 * (6.7 years ago) **RyanCavanaugh** added label `Domain: Quick Info`, set milestone to `Backlog`, and removed from milestone `Community`
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/10091#issuecomment-3604485084) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#10335](https://github.com/microsoft/TypeScript/issues/10335) (Closed, `Bug`, `Help Wanted`, `Domain: Formatter`, `VS Code Tracked`, `7.0 LS Migration`)

**Auto\-indentation problem with promise blocks**

*VSCode's auto-format over-indents closing braces in TypeScript promise .then blocks.*

 * [6.2 years ago](https://github.com/microsoft/TypeScript/issues/10335#issuecomment-533491988) **ki11ua** asked if the indentation issue was fixed yet
 * [5.3 years ago](https://github.com/microsoft/TypeScript/issues/10335#issuecomment-662692305) **tim92109** said "Still no resolution?"
 * [3.7 years ago](https://github.com/microsoft/TypeScript/issues/10335#issuecomment-1063094701) **kimberwarden** said "And still nothing?"
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/10335#issuecomment-3604485129) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#10873](https://github.com/microsoft/TypeScript/issues/10873) (Closed, `Bug`, `VS Code Tracked`, `Domain: LS: TSServer`, `7.0 LS Migration`)

**circular symlink breaks typescript intellisense**

*A circular symbolic link to a parent folder within a VSCode project prevents TypeScript IntelliSense from working.*

 * **mhegazy** added label `VS Code Tracked`
 * (6.3 years ago) **RyanCavanaugh** added label `Domain: TSServer`, and unassigned **zhengbli**
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/10873#issuecomment-3604485153) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#11040](https://github.com/microsoft/TypeScript/issues/11040) (Closed, `Bug`, `Domain: LS: TSServer`, `7.0 LS Migration`)

**programUpToDate check in synchonizeHostData should ignore differences in library files that were injected by the compiler  **

*Update synchronizeHostData’s programUpToDate check to exclude injected library files from file set comparisons to prevent needless rebuilds.*

 * **mhegazy** unassigned **vladima**
 * (6.3 years ago) **RyanCavanaugh** added label `Domain: TSServer`, and unassigned **mhegazy**
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/11040#issuecomment-3604485168) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#11074](https://github.com/microsoft/TypeScript/issues/11074) (Closed, `Bug`, `VS Code Tracked`, `Domain: LS: Smart Indentation`, `7.0 LS Migration`)

**Adjust cursor position on new line or don't emit empty spaces**

*VSCode inserts extra whitespace on new indented lines and leaves the cursor before it instead of at the indentation.*

 * [9.1 years ago](https://github.com/microsoft/TypeScript/issues/11074#issuecomment-251382121) **dbaeumer** explained that VS Code doesn’t move the cursor after formatting due to multi-cursor complexity, described how VS Code’s smart indent and whitespace logic works, and proposed disabling the server’s smart indent logic
 * (6.3 years ago) **RyanCavanaugh** added label `Domain: Smart Indentation`, and unassigned **zhengbli**
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/11074#issuecomment-3604485192) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#11194](https://github.com/microsoft/TypeScript/issues/11194) (Closed, `Bug`, `VS Code Tracked`, `Domain: LS: TSServer`, `7.0 LS Migration`)

**tsconfig\.json options not applied if files section doesn't use extensions**

*VSCode’s TypeScript integration ignores tsconfig.json compilerOptions when a files entry omits file extensions.*

 * **mhegazy** removed from milestone `TypeScript 2.1`
 * (6.3 years ago) **RyanCavanaugh** added label `Domain: TSServer`, and unassigned **zhengbli**
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/11194#issuecomment-3604485216) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#11308](https://github.com/microsoft/TypeScript/issues/11308) (Closed, `Bug`, `Domain: LS: Refactorings`, `7.0 LS Migration`)

**Rename inconsistency for default exports**

*Renaming a default-exported function identifier does not update its imports unless it's declared inline.*

 * [2.2 years ago](https://github.com/microsoft/TypeScript/issues/11308#issuecomment-1692977788) **Andarist** said "I retested this in VS Code and it does seem to work - regardless of the renamed location in a.ts. cc @jakebailey "
 * [2.2 years ago](https://github.com/microsoft/TypeScript/issues/11308#issuecomment-1696190852) **jakebailey** attempted to bisect and suggested adding a test since none was found to verify the fix
 * **RyanCavanaugh** added label `Domain: Refactorings`
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/11308#issuecomment-3604485241) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#11788](https://github.com/microsoft/TypeScript/issues/11788) (Closed, `Bug`, `Domain: LS: Symbol Navigation`, `7.0 LS Migration`)

**Go to implementation misses some implementations**

*Go to implementation for the inherited hello() method fails to include FooBaseImpl’s implementation from the BaseFoo interface.*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [2.2 years ago](https://github.com/microsoft/TypeScript/issues/11788#issuecomment-1695555575) **Andarist** questioned whether the change was correct because FooBaseImpl couldn’t be assigned to the variables and referenced the explicitlyInheritsFrom comment and a test case
 * **RyanCavanaugh** added label `Domain: Symbol Navigation`
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/11788#issuecomment-3604485256) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#12084](https://github.com/microsoft/TypeScript/issues/12084) (Closed, `Bug`, `Domain: Formatter`, `VS Code Tracked`, `7.0 LS Migration`)

**Code Format with object spread in JavaScript files breaks**

*Code formatting in VS Code breaks when using the object spread operator in JavaScript files.*

 * **mhegazy** removed from milestone `TypeScript 2.1.2`
 * **sandersn** unassigned **sandersn**
 * **RyanCavanaugh** added label `Domain: Formatter`
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/12084#issuecomment-3604485288) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#13205](https://github.com/microsoft/TypeScript/issues/13205) (Closed, `Bug`, `Help Wanted`, `Domain: Formatter`, `VS Code Tracked`, `7.0 LS Migration`)

**incorrect formatting on javascript**

*VSCode's JavaScript formatter inserts an extra newline and misindents the second-argument object in function calls.*

 * [8.9 years ago](https://github.com/microsoft/TypeScript/issues/13205#issuecomment-269657812) **saschanaz** said "#3827 "
 * (6.7 years ago) **RyanCavanaugh** set milestone to `Backlog`, and removed from milestone `Community`
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/13205#issuecomment-3604485302) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#13302](https://github.com/microsoft/TypeScript/issues/13302) (Closed, `Bug`, `Domain: LS: Completion Lists`, `7.0 LS Migration`)

**No completions for \`extends\` clause for members of a namespace containing only interfaces and types followed by expression**

*tsserver fails to complete namespace-only interface and type members in an extends clause when followed by an expression.*

 * **mhegazy** added to milestone `Future`
 * **sandersn** unassigned **sandersn**
 * **RyanCavanaugh** added label `Domain: Completion Lists`
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/13302#issuecomment-3604485321) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#13433](https://github.com/microsoft/TypeScript/issues/13433) (Closed, `Bug`, `Domain: LS: Smart Indentation`, `7.0 LS Migration`)

**Incorrect text caret position on fourslash tester**

*smartIndentOnUnclosedFunctionDeclaration04.ts fourslash test reports wrong caret text after newline, getting 'a' instead of expected '('.*

 * (6.3 years ago) **RyanCavanaugh** added labels `Bug`, `Domain: Smart Indentation`, and removed label `Needs Investigation`
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/13433#issuecomment-3604485340) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#13654](https://github.com/microsoft/TypeScript/issues/13654) (Closed, `Bug`, `Domain: LS: Symbol Navigation`, `7.0 LS Migration`)

**Error in find\-all\-references for 3 spread types**

*Find-all-references for property ‘a’ on an object composed of three spread sources only locates the last source’s declaration instead of all.*

 * [7.2 years ago](https://github.com/microsoft/TypeScript/issues/13654#issuecomment-424542742) **ghost** said "@sandersn Any way to fix this without #13288?"
 * **sandersn** unassigned **sandersn**
 * **RyanCavanaugh** added label `Domain: Symbol Navigation`
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/13654#issuecomment-3604485365) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#13822](https://github.com/microsoft/TypeScript/issues/13822) (Closed, `Bug`, `Domain: LS: TSServer`, `7.0 LS Migration`)

**\[typings installer\] ensure that installed @types packages are supported by the current version of the TypeScript**

*Ensure the typings installer updates installed @types packages to versions compatible with the current TypeScript compiler.*

 * (8.7 years ago) **mhegazy** set milestone to `Future`, and removed from milestone `TypeScript 2.3`
 * **RyanCavanaugh** added label `Domain: TSServer`
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/13822#issuecomment-3604485378) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#14073](https://github.com/microsoft/TypeScript/issues/14073) (Closed, `Bug`, `Domain: LS: Symbol Navigation`, `7.0 LS Migration`)

**VSCode compatibility: Find\-all\-references not working for special reference kinds**

*VSCode’s find-all-references feature fails to identify references for labels, string literal types, and primitive type annotations in TypeScript nightly.*

 * **mhegazy** removed from milestone `TypeScript 2.4`
 * [2.2 years ago](https://github.com/microsoft/TypeScript/issues/14073#issuecomment-1695558828) **Andarist** said "All 3 of the mentioned ones seem to work alright today, cc @jakebailey "
 * **RyanCavanaugh** added label `Domain: Symbol Navigation`
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/14073#issuecomment-3604485406) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#14105](https://github.com/microsoft/TypeScript/issues/14105) (Closed, `Bug`, `Domain: LS: Quick Fixes`, `7.0 LS Migration`)

**Implement missing members sometimes writes out inaccessible types**

*The implement missing members code fix produces invalid code by referencing an inaccessible return type from an inner abstract class.*

 * **mhegazy** added to milestone `Future`
 * **amcasey** unassigned **amcasey**
 * [2.2 years ago](https://github.com/microsoft/TypeScript/issues/14105#issuecomment-1695578784) **Andarist** noted that the codefix should check symbol accessibility, suggested using checker.isSymbolAccessible, and recommended crawling through type parameters, parameters, and return types for non-accessible symbols
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/14105#issuecomment-3604485434) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#14461](https://github.com/microsoft/TypeScript/issues/14461) (Closed, `Bug`, `Help Wanted`, `Domain: LS: Symbol Navigation`, `7.0 LS Migration`)

**Can't find definition of a property on an object with an index signature\.**

*TypeScript fails to locate definitions for properties on objects with index signatures and should first attempt literal lookup before erroring.*

 * **RyanCavanaugh** added to milestone `Backlog`
 * **DanielRosenwasser** added label `Domain: Symbol Navigation`
 * [2.2 years ago](https://github.com/microsoft/TypeScript/issues/14461#issuecomment-1695703277) **Andarist** noted that navigation currently goes to the index signature’s definition and suggested closing the issue
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/14461#issuecomment-3604485456) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#14494](https://github.com/microsoft/TypeScript/issues/14494) (Closed, `Bug`, `Help Wanted`, `Domain: Formatter`, `VS Code Tracked`, `7.0 LS Migration`)

**Reformat ternary operator**

*Configure VSCode to format ternary operators with line breaks before the question mark and colon instead of default single-line style.*

 * [5.6 years ago](https://github.com/microsoft/TypeScript/issues/14494#issuecomment-609959751) **ranisalt** said "@isaacalves prettier"
 * [5.6 years ago](https://github.com/microsoft/TypeScript/issues/14494#issuecomment-609966025) **jamesst20** said "@isaacalves I use WebStorm instead"
 * [5.6 years ago](https://github.com/microsoft/TypeScript/issues/14494#issuecomment-609976169) **isaacalves** mentioned that placing the '?' of the ternary operator on a new line produced a nested formatting and noted that they used Prettier with VS Code
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/14494#issuecomment-3604485486) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#14513](https://github.com/microsoft/TypeScript/issues/14513) (Closed, `Bug`, `VS Code Tracked`, `Domain: LS: TSServer`, `7.0 LS Migration`)

**Unicode Character Causing all Lines to Be shifted by one**

*An embedded Unicode line separator in a comment disrupts TSServer line counting, shifting lines and misplacing symbols.*

 * **sandersn** unassigned **sandersn**
 * [5.8 years ago](https://github.com/microsoft/TypeScript/issues/14513#issuecomment-579999009) **mjbvz** said "Still reproducible for me with TS 3.7.5"
 * **RyanCavanaugh** added label `Domain: TSServer`
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/14513#issuecomment-3604485508) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#14531](https://github.com/microsoft/TypeScript/issues/14531) (Closed, `Bug`, `Help Wanted`, `Domain: Formatter`, `VS Code Tracked`, `7.0 LS Migration`)

**Incorrect Formatting For Class With Decorator **

*Decorated TypeScript class formatting incorrectly uses four spaces instead of the configured two-space indent for methods.*

 * [8.1 years ago](https://github.com/microsoft/TypeScript/issues/14531#issuecomment-339580292) **cspotcode** explained that the formatter miscalculates indentation when moving a ClassMember to a new line and asked about intended child indentation behavior
 * (6.7 years ago) **RyanCavanaugh** set milestone to `Backlog`, and removed from milestone `Community`
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/14531#issuecomment-3604485529) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#1507](https://github.com/microsoft/TypeScript/issues/1507) (Closed, `Bug`, `Domain: LS: Symbol Navigation`, `7.0 LS Migration`)

**Find references for shorthand properties**

*Finding references on a shorthand property method call fails to include the actual function definition.*

 * **mhegazy** unassigned **yuit**
 * [7.7 years ago](https://github.com/microsoft/TypeScript/issues/1507#issuecomment-369982010) **OliverJAsh** described an issue where object property value shorthand references were not appearing in find all references
 * **RyanCavanaugh** added label `Domain: Symbol Navigation`
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/1507#issuecomment-3604485554) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#15562](https://github.com/microsoft/TypeScript/issues/15562) (Closed, `Bug`, `VS Code Tracked`, `Domain: LS: Quick Fixes`, `7.0 LS Migration`)

**Filling in an implementation using VS Code will expand types**

*VS Code’s quick fix for implementing interfaces replaces a tuple type alias with its expanded literal tuple in method signatures*

 * **amcasey** unassigned **amcasey**
 * [5.8 years ago](https://github.com/microsoft/TypeScript/issues/15562#issuecomment-576432257) **AnyhowStep** reported that the “Implement interface” quick fix expanded type aliases and long generic type constraints, provided code example and expected vs actual outputs
 * [5.8 years ago](https://github.com/microsoft/TypeScript/issues/15562#issuecomment-579995365) **mjbvz** stated that Tyriar's original example was fixed in TS 3.7.5 but AnyhowStep's example still expanded the types
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/15562#issuecomment-3604485578) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#16265](https://github.com/microsoft/TypeScript/issues/16265) (Closed, `Bug`, `Help Wanted`, `Domain: Formatter`, `VS Code Tracked`, `7.0 LS Migration`)

**Incorrect indent with template literal**

*VSCode misindents arrow functions with template literals, causing the closing brace to be incorrectly aligned.*

 * **mhegazy** added to milestone `Community`
 * (6.7 years ago) **RyanCavanaugh** set milestone to `Backlog`, and removed from milestone `Community`
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/16265#issuecomment-3604485603) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#16297](https://github.com/microsoft/TypeScript/issues/16297) (Closed, `Bug`, `Domain: LS: Quick Fixes`, `7.0 LS Migration`)

**Offers quick suggestion to ignore parse error; but parse error can't be ignored**

*Quick fixes to ignore parse errors appear for transient JavaScript syntax errors in ts-check files but cannot be applied.*

 * (7.4 years ago) **mhegazy** set milestone to `Future`, and removed from milestone `TypeScript 3.0`
 * **RyanCavanaugh** unassigned **mhegazy**
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/16297#issuecomment-3604485626) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#16479](https://github.com/microsoft/TypeScript/issues/16479) (Closed, `Bug`, `Domain: LS: Quick Fixes`, `7.0 LS Migration`)

**Quick fix for variable of wrong type results in ugly formatting**

*The TypeScript quick fix to add an @ts-ignore comment for a wrong-type variable improperly splits and indents the declaration.*

 * (8.2 years ago) **mhegazy** set milestone to `Future`, and removed from milestone `TypeScript 2.6`
 * **amcasey** unassigned **amcasey**
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/16479#issuecomment-3604485645) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#16645](https://github.com/microsoft/TypeScript/issues/16645) (Closed, `Bug`, `Help Wanted`, `Domain: Formatter`, `7.0 LS Migration`)

**Bad automatic formatting when filling in type argument as object literal**

*TypeScript’s automatic formatting inserts an unintended space before object-literal type arguments, converting f<{}>() into f < {}>().*

 * **mhegazy** added to milestone `Community`
 * (6.7 years ago) **RyanCavanaugh** set milestone to `Backlog`, and removed from milestone `Community`
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/16645#issuecomment-3604485672) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#16852](https://github.com/microsoft/TypeScript/issues/16852) (Closed, `Bug`, `Domain: LS: TSServer`, `7.0 LS Migration`)

**\`\-\-globalPlugins\` and \`\-\-pluginProbeLocations\` default to list with empty string**

*--globalPlugins and --pluginProbeLocations split an empty string into [""] instead of [], causing tsserver to attempt loading an empty module*

 * **mhegazy** added to milestone `Future`
 * (6 years ago) **RyanCavanaugh** added label `Domain: TSServer`, and unassigned **RyanCavanaugh**
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/16852#issuecomment-3604485695) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#17151](https://github.com/microsoft/TypeScript/issues/17151) (Closed, `Bug`, `VS Code Tracked`, `Domain: LS: TSServer`, `7.0 LS Migration`, **RyanCavanaugh**)

**Add plugins property on TS Server open request**

*Add an optional plugins array to TS Server open requests to let editors specify which plugins should handle or ignore files.*

 * [6.7 years ago](https://github.com/microsoft/TypeScript/issues/17151#issuecomment-469571809) **mickaelistria** questioned why .html files were parsed by tsserver by default and suggested renaming the issue title to better describe the error
 * [6.5 years ago](https://github.com/microsoft/TypeScript/issues/17151#issuecomment-498446944) **kyliau** asked for guidance on enabling the Angular plugin for HTML files in tsserver and for pointers on contributing the feature
 * [6.5 years ago](https://github.com/microsoft/TypeScript/issues/17151#issuecomment-500018831) **mjbvz** suggested discussing external language support in TypeScript server
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/17151#issuecomment-3604485733) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#1853](https://github.com/microsoft/TypeScript/issues/1853) (Closed, `Bug`, `Visual Studio`, `Help Wanted`, `Domain: LS: Symbol Navigation`, `7.0 LS Migration`)

**findReferences doesn't give results in the right order**

*findReferences returns text span search results out of order when looking for globalTemplateStringsArrayType in checker.ts*

 * (6.7 years ago) **RyanCavanaugh** added label `Domain: Symbol Navigation`, set milestone to `Backlog`, and removed from milestone `Community`
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/1853#issuecomment-3604485751) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#18849](https://github.com/microsoft/TypeScript/issues/18849) (Closed, `Bug`, `VS Code Tracked`, `Domain: LS: TSServer`, `7.0 LS Migration`)

**TS Server: Send error event when a plugin fails to load**

*Add a pluginInitializationFailed error event in TS Server to inform clients when a plugin fails to load.*

 * [7 years ago](https://github.com/microsoft/TypeScript/issues/18849#issuecomment-438881908) **mjbvz** suggested including the change in the IntelliCode plugin to prevent user confusion
 * (6 years ago) **RyanCavanaugh** added label `Domain: TSServer`, and unassigned **RyanCavanaugh**
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/18849#issuecomment-3604485778) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#18917](https://github.com/microsoft/TypeScript/issues/18917) (Closed, `Bug`, `Domain: LS: Refactorings`, `7.0 LS Migration`)

**Don't extract constant to an unreachable location**

*Extracting a constant from an inner function inserts the new local after the outer return, making it unreachable.*

 * (8.1 years ago) **mhegazy** set milestone to `Future`, and removed from milestone `TypeScript 2.6`
 * **amcasey** unassigned **amcasey**
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/18917#issuecomment-3604485812) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#19198](https://github.com/microsoft/TypeScript/issues/19198) (Closed, `Bug`, `Domain: LS: Type Display`, `7.0 LS Migration`)

**typeChecker\.typeToString\(\) should print most derived alias**

*typeChecker.typeToString incorrectly expands type aliases and returns First<string, string> instead of the more derived alias Second<string>.*

 * **RyanCavanaugh** removed label `Needs Investigation`
 * **sandersn** unassigned **sandersn**
 * **RyanCavanaugh** added label `Domain: Type Display`
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/19198#issuecomment-3604485829) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#19313](https://github.com/microsoft/TypeScript/issues/19313) (Closed, `Bug`, `Domain: LS: Quick Fixes`, `7.0 LS Migration`)

**Anonymous function expressions aren't covered for 'infer from usage'**

*Anonymous function expressions don't infer parameter types from usage, prompting a request to extend inference through assignments and exports.*

 * (6.8 years ago) **DanielRosenwasser** assigned to **sandersn**, and unassigned **mhegazy**
 * **sandersn** unassigned **sandersn**
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/19313#issuecomment-3604485854) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#1932](https://github.com/microsoft/TypeScript/issues/1932) (Closed, `Bug`, `Help Wanted`, `Domain: LS: Symbol Navigation`, `7.0 LS Migration`)

**Go to definition includes results from other entity spaces**

*Go to definition on Symbol returns both its var and interface declarations, preventing Visual Studio navigation.*

 * (6.7 years ago) **RyanCavanaugh** set milestone to `Backlog`, and removed from milestone `Community`
 * **DanielRosenwasser** added label `Domain: Symbol Navigation`
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/1932#issuecomment-3604485904) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#19598](https://github.com/microsoft/TypeScript/issues/19598) (Closed, `Bug`, `Domain: LS: Quick Fixes`, `7.0 LS Migration`)

**Implicit any quick fix should infer from JSX component usage**

*Implicit any quick fix should infer specific JSX prop types from component usage instead of defaulting to ReactNode*

 * (7.4 years ago) **mhegazy** set milestone to `Future`, and removed from milestone `TypeScript 3.0`
 * **RyanCavanaugh** unassigned **mhegazy**
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/19598#issuecomment-3604485920) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#19911](https://github.com/microsoft/TypeScript/issues/19911) (Closed, `Bug`, `Domain: LS: Quick Fixes`, `7.0 LS Migration`)

**JSDoc refactor doesn't add type parameters**

*TypeScript’s inline-jsdoc-types refactoring does not preserve JSDoc @template type parameters, causing generics to default to any.*

 * **sandersn** removed from milestone `Backlog`
 * **RyanCavanaugh** added to milestone `Backlog`
 * **sandersn** unassigned **sandersn**
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/19911#issuecomment-3604485955) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#20185](https://github.com/microsoft/TypeScript/issues/20185) (Closed, `Bug`, `Domain: LS: TSServer`, `7.0 LS Migration`)

**TypeScript: aggregate errors for file from all projects**

*VSCode currently only shows TypeScript errors from one tsconfig per shared file and needs to aggregate errors across all projects.*

 * **mhegazy** added to milestone `Future`
 * [6.6 years ago](https://github.com/microsoft/TypeScript/issues/20185#issuecomment-484096071) **OliverJAsh** said "Fixed by #3469"
 * [6.2 years ago](https://github.com/microsoft/TypeScript/issues/20185#issuecomment-528651498) **OliverJAsh** asked whether teething issues getting project references to work in VS Code stemmed from VS Code or the TS server
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/20185#issuecomment-3604485969) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#21830](https://github.com/microsoft/TypeScript/issues/21830) (Closed, `Bug`, `Domain: LS: Quick Fixes`, `7.0 LS Migration`)

**Missing fix suggestions when multiple come from the same JSX element**

*Provide an auto-fix suggestion to import React when using JSX in modules with jsx:'react' setting.*

 * (7.4 years ago) **mhegazy** set milestone to `Future`, and removed from milestone `TypeScript 3.0`
 * **RyanCavanaugh** unassigned **mhegazy**
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/21830#issuecomment-3604485990) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#22222](https://github.com/microsoft/TypeScript/issues/22222) (Closed, `Bug`, `VS Code Tracked`, `Domain: LS: Symbol Navigation`, `7.0 LS Migration`)

**Find All Reference from requiring file to module file works only if not default CommonJS exports**

*VSCode’s Find All References fails to detect cross-file usages of default CommonJS exports, but succeeds for named exports.*

 * (6.5 years ago) **sandersn** set milestone to `Backlog`, and unassigned **sandersn**
 * **RyanCavanaugh** added label `Domain: Symbol Navigation`
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/22222#issuecomment-3604486018) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#22350](https://github.com/microsoft/TypeScript/issues/22350) (Closed, `Bug`, `Domain: JSDoc`, `Domain: LS: Quick Info`, `7.0 LS Migration`)

**JSDoc member documentation not returned by quickInfo**

*QuickInfo hover over object literal properties does not include JSDoc documentation for those members.*

 * **sandersn** unassigned **sandersn**
 * (5.1 years ago) **mjbvz** added labels `Domain: JSDoc`, `Domain: Quick Info`
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/22350#issuecomment-3604486049) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#22357](https://github.com/microsoft/TypeScript/issues/22357) (Closed, `Bug`, `Domain: LS: Quick Fixes`, `7.0 LS Migration`)

**Don't offer to infer parameter type if inferred type is 'any'**

*The IDE offers an unnecessary infer-parameter-type suggestion for function parameters when the inferred type is any.*

 * (7.4 years ago) **mhegazy** set milestone to `Future`, and removed from milestone `TypeScript 3.0`
 * **RyanCavanaugh** unassigned **mhegazy**
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/22357#issuecomment-3604486074) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#23738](https://github.com/microsoft/TypeScript/issues/23738) (Closed, `Bug`, `Help Wanted`, `Domain: LS: Quick Info`, `7.0 LS Migration`)

**Tooltip for function overloaded to mimic variadic types infers wrong overload when called with trailing comma**

*IntelliSense hover tooltip selects the wrong overloaded signature for a variadic function call with a trailing comma*

 * (6.7 years ago) **RyanCavanaugh** set milestone to `Backlog`, and removed from milestone `Community`
 * [3.1 years ago](https://github.com/microsoft/TypeScript/issues/23738#issuecomment-1272803767) **JoseLion** inquired about updates on the issue, described how it affects lint tools, and offered to help with a PR while requesting guidance
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/23738#issuecomment-3604486114) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#23897](https://github.com/microsoft/TypeScript/issues/23897) (Closed, `Bug`, `Domain: LS: Type Display`, `7.0 LS Migration`)

**Repeated mapped type inference causes incorrect typeToString results**

*Chaining combineReducers with mapped type inference results in nested reducer return types inferred as any instead of string.*

 * (6.7 years ago) **RyanCavanaugh** set milestone to `Backlog`, removed from milestone `TypeScript 3.4.0`, and unassigned **weswigham**
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/23897#issuecomment-3604486135) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#24025](https://github.com/microsoft/TypeScript/issues/24025) (Closed, `Bug`, `Domain: LS: Symbol Navigation`, `7.0 LS Migration`)

**Improve references for import type of JS modules**

*Enhance reference finding to correctly handle import type declarations in JavaScript modules.*

 * (6.7 years ago) **sandersn** set milestone to `Backlog`, and unassigned **sandersn**
 * **RyanCavanaugh** added label `Domain: Symbol Navigation`
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/24025#issuecomment-3604486160) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#24409](https://github.com/microsoft/TypeScript/issues/24409) (Closed, `Bug`, `Domain: LS: Completion Lists`, `7.0 LS Migration`)

**Missing type description in suggestion popup**

*TypeScript 3.0 dev build’s suggestion popup omits generic parameters for imported types while fully displaying local types.*

 * (6.7 years ago) **RyanCavanaugh** added label `Domain: Completion Lists`, set milestone to `Backlog`, and removed from milestone `TypeScript 3.4.0`
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/24409#issuecomment-3604486175) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#26260](https://github.com/microsoft/TypeScript/issues/26260) (Closed, `Bug`, `Help Wanted`, `Domain: LS: Refactorings`, `7.0 LS Migration`)

**Refactor "move to function in module scope" moves function past the following variable declaration**

*Extracting a function to module scope erroneously places it after subsequent variable declarations rather than near its original position.*

 * [5.3 years ago](https://github.com/microsoft/TypeScript/issues/26260#issuecomment-673117184) **a-tarasyuk** questioned why the issue was labeled as a bug and provided a code example illustrating statement and function declaration ordering
 * [5.3 years ago](https://github.com/microsoft/TypeScript/issues/26260#issuecomment-673589570) **jessetrinity** said "@AlCalzone was there more context when you originally opened this issue that would help us out?"
 * [5.3 years ago](https://github.com/microsoft/TypeScript/issues/26260#issuecomment-674503808) **AlCalzone** observed that the refactor worked but resulted in illogical function placement, separating logically related functions
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/26260#issuecomment-3604486202) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#26275](https://github.com/microsoft/TypeScript/issues/26275) (Closed, `Bug`, `Domain: LS: Completion Lists`, `7.0 LS Migration`)

**Class method autocompletions not working properly on class with mixins**

*VS Code IntelliSense fails to autocomplete methods on classes composed with mixins using the recompose compose function.*

 * (6.7 years ago) **sandersn** set milestone to `Backlog`, and unassigned **sandersn**
 * **RyanCavanaugh** added label `Domain: Completion Lists`
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/26275#issuecomment-3604486227) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#26384](https://github.com/microsoft/TypeScript/issues/26384) (Closed, `Bug`, `Domain: LS: Completion Lists`, `7.0 LS Migration`)

**Autocomplete fails on inferred type**

*Generic function inference causes autocomplete to suggest every union member instead of the narrowed value type for record values.*

 * (6.7 years ago) **RyanCavanaugh** set milestone to `Backlog`, and unassigned **sheetalkamat**
 * [3.9 years ago](https://github.com/microsoft/TypeScript/issues/26384#issuecomment-1009422971) **alexn-s** said "is there any update on this issue?"
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/26384#issuecomment-3604486252) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#26401](https://github.com/microsoft/TypeScript/issues/26401) (Closed, `Bug`, `Help Wanted`, `Domain: LS: Completion Lists`, `7.0 LS Migration`)

**No completions in global namespace augmentation from original namespace**

*TypeScript code completion in a global namespace augmentation only suggests newly added members and omits original namespace members.*

 * (6.7 years ago) **RyanCavanaugh** added label `help wanted`, set milestone to `Backlog`, and removed from milestone `Community`
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/26401#issuecomment-3604486269) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#26408](https://github.com/microsoft/TypeScript/issues/26408) (Closed, `Bug`, `Domain: LS: Type Display`, `7.0 LS Migration`)

**Contradicting types in tooltip and type checker when inference fails and when using @ts\-ignore**

*Ignoring a generic inference error with NoInfer<T> causes IntelliSense tooltips and the TypeScript compiler to report conflicting types and assignability.*

 * (6.7 years ago) **sandersn** set milestone to `Backlog`, and unassigned **sandersn**
 * **RyanCavanaugh** added label `Domain: Type Display`
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/26408#issuecomment-3604486296) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#26610](https://github.com/microsoft/TypeScript/issues/26610) (Closed, `Bug`, `Domain: LS: Completion Lists`, `7.0 LS Migration`)

**Missing completion for abstract indexed types**

*TypeScript does not provide autocomplete suggestions for subclass-specific keys of an abstract indexed type when using a generic getter.*

 * (7.2 years ago) **RyanCavanaugh** added labels `Bug`, `Domain: Completion Lists`, and set milestone to `Future`
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/26610#issuecomment-3604486321) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#26618](https://github.com/microsoft/TypeScript/issues/26618) (Closed, `Bug`, `Help Wanted`, `Domain: Formatter`, `7.0 LS Migration`)

**Bad formatting adding multiple properties to start of object literal**

*The TypeScript code fix for missing modules incorrectly fails to indent the closing brace of compilerOptions when adding multiple properties.*

 * (6.8 years ago) **RyanCavanaugh** set milestones to `TypeScript 3.4.0`, `Backlog`, and removed from milestone `TypeScript 3.4.0`
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/26618#issuecomment-3604486347) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#27211](https://github.com/microsoft/TypeScript/issues/27211) (Closed, `Bug`, `Domain: LS: Completion Lists`, `7.0 LS Migration`)

**Visual Studio Code intellisense on React component using typescript with union types**

*Visual Studio Code does not provide autocomplete suggestions for discriminated union props like 'myProp' in React components using TypeScript union types.*

 * [7.1 years ago](https://github.com/microsoft/TypeScript/issues/27211#issuecomment-426062886) **weswigham** said "https://github.com/Microsoft/TypeScript/pull/27408 maybe? Unless we also do something in services?"
 * (6.7 years ago) **RyanCavanaugh** added label `Domain: Completion Lists`, and unassigned **weswigham**
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/27211#issuecomment-3604486367) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#27241](https://github.com/microsoft/TypeScript/issues/27241) (Closed, `Bug`, `Domain: LS: Completion Lists`, `Domain: JavaScript`, `7.0 LS Migration`)

**No suggestions for extended classes\.**

*Visual Studio Code Insiders does not suggest inherited methods from an extended class in JavaScript code completions.*

 * (6.7 years ago) **RyanCavanaugh** set milestone to `Backlog`, removed from milestone `TypeScript 3.4.0`, and unassigned **sandersn**
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/27241#issuecomment-3604486393) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#27284](https://github.com/microsoft/TypeScript/issues/27284) (Closed, `Bug`, `Domain: LS: Symbol Navigation`, `7.0 LS Migration`)

**findAllReferences broken when immediately looping over array literal of object literals**

*findAllReferences fails to identify all references of a destructured property when looping directly over an array literal of object literals.*

 * (1.7 years ago) **jakebailey** removed labels `Fix Available`, `Fixed`
 * **RyanCavanaugh** added label `Domain: Symbol Navigation`
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/27284#issuecomment-3604486406) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#27614](https://github.com/microsoft/TypeScript/issues/27614) (Closed, `Bug`, `Needs Proposal`, `In Discussion`, `Domain: LS: Quick Fixes`, `7.0 LS Migration`)

**Odd quick fix ordering for misspelled identifiers**

*Request to reorder quick fixes so misspelled identifier suggestions appear before remove-unused-declarations actions.*

 * **DanielRosenwasser** added label `Needs Proposal`
 * [4.1 years ago](https://github.com/microsoft/TypeScript/issues/27614#issuecomment-936844382) **DanielRosenwasser** suggested improvements to editor diagnostics synchronization including narrower spans, batching multiple diagnostics in one call, range-based fixes, error-code-only requests, and drawing inspiration from editor implementations and refactorings
 * **RyanCavanaugh** added label `Domain: Quick Fixes`
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/27614#issuecomment-3604486423) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#27617](https://github.com/microsoft/TypeScript/issues/27617) (Closed, `Bug`, `Domain: LS: Symbol Navigation`, `7.0 LS Migration`)

**findAllRefs doesn't work for property of \`typeof import\("\./foo"\)\`**

*findAllRefs fails to locate references to properties on modules imported using typeof import.*

 * (6.7 years ago) **RyanCavanaugh** added label `Domain: Symbol Navigation`, set milestone to `Backlog`, and removed from milestone `TypeScript 3.4.0`
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/27617#issuecomment-3604486453) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#27670](https://github.com/microsoft/TypeScript/issues/27670) (Closed, `Bug`, `Domain: LS: TSServer`, `7.0 LS Migration`)

**Automatic typings install does not trigger project refresh**

*VSCode doesn’t refresh the JavaScript project after installing typings automatically, forcing a manual reload to pick them up.*

 * (6.7 years ago) **RyanCavanaugh** added label `Domain: TSServer`, set milestone to `Backlog`, and unassigned **sheetalkamat**
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/27670#issuecomment-3604486471) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#27959](https://github.com/microsoft/TypeScript/issues/27959) (Closed, `Bug`, `Domain: LS: TSServer`, `7.0 LS Migration`)

**Rename file by renaming on an aliased path**

*Renaming a file through an aliased import path in TypeScript triggers an error preventing the module rename.*

 * [2.1 years ago](https://github.com/microsoft/TypeScript/issues/27959#issuecomment-1741792079) **varthc** said "Any update? Thanks!"
 * [2.1 years ago](https://github.com/microsoft/TypeScript/issues/27959#issuecomment-1750299781) **timoisalive** said "Yep, hoping to see a fix to this as well, now that also Expo projects support path aliases (https://docs.expo.dev/guides/typescript/#path-aliases)."
 * [1.4 years ago](https://github.com/microsoft/TypeScript/issues/27959#issuecomment-2203110367) **simplenotezy** asked whether there was a solution for aliased imports or if they were doomed
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/27959#issuecomment-3604486508) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#28007](https://github.com/microsoft/TypeScript/issues/28007) (Closed, `Bug`, `Domain: LS: Quick Fixes`, `7.0 LS Migration`)

**Auto\-import triggers for reserved keyword exports**

*VS Code's TypeScript auto-import feature incorrectly suggests imports for exports aliased to reserved keywords like return, throw, break, and continue.*

 * **weswigham** added label `Domain: Quick Fixes`
 * **RyanCavanaugh** added to milestone `Backlog`
 * [5.2 years ago](https://github.com/microsoft/TypeScript/issues/28007#issuecomment-683783674) **AlCalzone** mentioned encountering the issue when editing a project using tap exporting true/false and asked to prioritize it higher
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/28007#issuecomment-3604486562) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#28083](https://github.com/microsoft/TypeScript/issues/28083) (Closed, `Bug`, `Domain: LS: Quick Info`, `7.0 LS Migration`)

**Quick info on JSX element should show inferred type arguments**

*In TS, Quick Info on a generic JSX element displays only the class signature instead of its inferred type arguments.*

 * **unknown** added label `Domain: Quick Info`
 * [7.1 years ago](https://github.com/microsoft/TypeScript/issues/28083#issuecomment-432390336) **DanielRosenwasser** said "I think this would also fix https://github.com/Microsoft/TypeScript/issues/23716."
 * **RyanCavanaugh** added to milestone `Backlog`
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/28083#issuecomment-3604486596) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#28085](https://github.com/microsoft/TypeScript/issues/28085) (Closed, `Bug`, `Domain: LS: Auto-import`, `7.0 LS Migration`)

**Inconsistency between import fix and moduleNameResolver for baseUrl \+ paths behavior**

*Import code fix erroneously resolves modules using baseUrl instead of applying paths mapping, resulting in invalid import statements.*

 * **unknown** added label `Bug`
 * (6.7 years ago) **RyanCavanaugh** added label `Domain: Auto-import`, and set milestone to `Backlog`
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/28085#issuecomment-3604486620) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#28272](https://github.com/microsoft/TypeScript/issues/28272) (Closed, `Bug`, `Domain: LS: Quick Info`, `7.0 LS Migration`)

**Quick info for array in \`a\.length\` shows \`any\[\]\` even when it should have a type**

*Quick info for an empty-initialized array incorrectly shows any[] for its length property instead of number[] after pushing numbers.*

 * (6.7 years ago) **RyanCavanaugh** set milestone to `Backlog`, and removed from milestone `TypeScript 3.4.0`
 * [6.7 years ago](https://github.com/microsoft/TypeScript/issues/28272#issuecomment-472691236) **RyanCavanaugh** said "The type to show in quickinfo is pretty ambiguous TBH"
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/28272#issuecomment-3604486653) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#28320](https://github.com/microsoft/TypeScript/issues/28320) (Closed, `Bug`, `Domain: LS: Quick Fixes`, `7.0 LS Migration`)

**infer\-from\-usage should infer "truthy" when only undefined is available**

*infer-from-usage incorrectly infers y as undefined rather than boolean | undefined when y is used in a truthy check*

 * (6.7 years ago) **RyanCavanaugh** set milestone to `Backlog`, removed from milestone `TypeScript 3.4.0`, and unassigned **sandersn**
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/28320#issuecomment-3604486671) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#28356](https://github.com/microsoft/TypeScript/issues/28356) (Closed, `Bug`, `Domain: LS: Refactorings`, `7.0 LS Migration`)

**\[1\.28\.2\] Refactor renaming class\-method not renaming bind\(this\) assignments \(Javascript\)**

*Renaming a class method in VSCode does not update references in bind(this) assignments.*

 * (6.7 years ago) **RyanCavanaugh** set milestone to `Backlog`, removed from milestone `TypeScript 3.4.0`, and unassigned **sheetalkamat**
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/28356#issuecomment-3604486689) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#28471](https://github.com/microsoft/TypeScript/issues/28471) (Closed, `Bug`, `Domain: LS: Completion Lists`, `7.0 LS Migration`)

**intellisense suggests inferred type parameter in else branch of conditional type**

*TypeScript IntelliSense incorrectly suggests an inferred type parameter in a conditional type's else branch, causing errors.*

 * (6.7 years ago) **RyanCavanaugh** set milestone to `Backlog`, removed from milestone `TypeScript 3.4.0`, and unassigned **weswigham**
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/28471#issuecomment-3604486703) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#28510](https://github.com/microsoft/TypeScript/issues/28510) (Closed, `Bug`, `Domain: JSDoc`, `Domain: LS: Symbol Navigation`, `7.0 LS Migration`)

**Go to definition on @constructor type fails**

*Go-to-definition on a JSDoc @constructor type reference fails to locate the function definition.*

 * (6.7 years ago) **RyanCavanaugh** set milestone to `Backlog`, and removed from milestone `TypeScript 3.4.0`
 * **DanielRosenwasser** added label `Domain: Symbol Navigation`
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/28510#issuecomment-3604486730) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#28512](https://github.com/microsoft/TypeScript/issues/28512) (Closed, `Bug`, `Domain: LS: Quick Info`, `7.0 LS Migration`, **sheetalkamat**)

**Symbol display of namespace\-function merged symbol at value use should just mention function**

*Symbol display for a merged namespace-function at value use erroneously shows both namespace and function instead of only the function.*

 * **unknown** added label `Domain: Quick Info`
 * (7 years ago) **weswigham** set milestone to `Future`, and assigned to **sheetalkamat**
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/28512#issuecomment-3604486753) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#28680](https://github.com/microsoft/TypeScript/issues/28680) (Closed, `Bug`, `Domain: LS: Refactorings`, `7.0 LS Migration`)

**Incorrect rename of imported declaration**

*Renaming an imported declaration incorrectly adds an alias import instead of renaming the exported declaration.*

 * (6.4 years ago) **sandersn** set milestone to `Backlog`, and unassigned **sandersn**
 * **RyanCavanaugh** added label `Domain: Refactorings`
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/28680#issuecomment-3604486770) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#28747](https://github.com/microsoft/TypeScript/issues/28747) (Closed, `Bug`, `Domain: JSX/TSX`, `Domain: LS: Refactorings`, `7.0 LS Migration`)

**Inference of parameter fail**

*VSCode TypeScript IntelliSense fails to infer suggestions for all undefined function parameters, though it works with only one undefined parameter.*

 * (6.7 years ago) **RyanCavanaugh** set milestone to `Backlog`, removed from milestone `TypeScript 3.4.0`, and unassigned **sandersn**
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/28747#issuecomment-3604486795) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#28764](https://github.com/microsoft/TypeScript/issues/28764) (Closed, `Bug`, `Domain: LS: Quick Fixes`, `7.0 LS Migration`)

**Infer parameter types from usage quick fix infers to any from React component props**

*TypeScript's infer-parameter-types quick fix assigns 'any' to React event handler parameters instead of correct event types.*

 * (6.7 years ago) **RyanCavanaugh** added label `Domain: Quick Fixes`, set milestone to `Backlog`, and unassigned **sandersn**
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/28764#issuecomment-3604486817) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#28766](https://github.com/microsoft/TypeScript/issues/28766) (Closed, `Bug`, `Domain: LS: Quick Fixes`, `7.0 LS Migration`)

**Infer parameter types from usage quick fix does not work for arrow function in class property initializers**

*Quick fix to infer parameter types from usage fails for arrow functions in class property initializers*

 * (6.7 years ago) **RyanCavanaugh** added label `Domain: Quick Fixes`, set milestone to `Backlog`, and removed from milestone `TypeScript 3.4.0`
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/28766#issuecomment-3604486843) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#28895](https://github.com/microsoft/TypeScript/issues/28895) (Closed, `Bug`, `Domain: LS: Symbol Navigation`, `7.0 LS Migration`)

**"2 definitions" returned when defaultProps exists in JS component\.**

*Assigning defaultProps to a JS React component via property assignment causes VSCode to show two definitions.*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [6.6 years ago](https://github.com/microsoft/TypeScript/issues/28895#issuecomment-484371385) **wscops** said "this bug still exist in v3.4.3"
 * **DanielRosenwasser** added label `Domain: Symbol Navigation`
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/28895#issuecomment-3604486854) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#29045](https://github.com/microsoft/TypeScript/issues/29045) (Closed, `Bug`, `Domain: LS: TSServer`, `7.0 LS Migration`)

**Vscode suggests wrong ts auto import path with js extension after having a json import**

*VSCode incorrectly adds .js extension to TypeScript auto-import paths after a JSON import.*

 * [5.7 years ago](https://github.com/microsoft/TypeScript/issues/29045#issuecomment-603228943) **digiperfect-tech** said "+1. Strangely enough, started facing this recently in the last month or so - perhaps after the last update (currently on version 1.42.1)."
 * [3.5 years ago](https://github.com/microsoft/TypeScript/issues/29045#issuecomment-1123646495) **tarjei** said "Has anyone found a solution to this issue?"
 * [3.3 years ago](https://github.com/microsoft/TypeScript/issues/29045#issuecomment-1191306886) **thijs-qv** said "@tarjei "typescript.preferences.importModuleSpecifierEnding": "minimal" seems to work OK for me, it will not use any extension this way."
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/29045#issuecomment-3604486889) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#29194](https://github.com/microsoft/TypeScript/issues/29194) (Closed, `Bug`, `Domain: LS: Quick Fixes`, `7.0 LS Migration`)

**JS type\-checking suggested refactoring produces maximum possible redundant relative module path**

*The JavaScript type-checking refactoring "Infer parameter types from usage" generates unnecessarily long absolute module paths instead of concise relative imports.*

 * [6.9 years ago](https://github.com/microsoft/TypeScript/issues/29194#issuecomment-451274791) **axefrog** said "I'm on Windows 10, drive D, and my literal path strings match the casing stored on the drive."
 * [6.9 years ago](https://github.com/microsoft/TypeScript/issues/29194#issuecomment-451277029) **sheetalkamat** suggested gathering tsserver logs via the TypeScript nightly drop and uploading them using provided steps
 * **RyanCavanaugh** added to milestone `Backlog`
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/29194#issuecomment-3604486913) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#29217](https://github.com/microsoft/TypeScript/issues/29217) (Closed, `Bug`, `Domain: LS: Refactorings`, `7.0 LS Migration`)

**Lots of async\-specific code in computeSuggestionDiagnostics**

*Relocate async-specific logic from computeSuggestionDiagnostics to its dedicated async codefix handler.*

 * (6.4 years ago) **RyanCavanaugh** set milestone to `Backlog`, removed from milestone `TypeScript 3.6.0`, and unassigned **uniqueiniquity**
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/29217#issuecomment-3604486931) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#29227](https://github.com/microsoft/TypeScript/issues/29227) (Closed, `Bug`, `Domain: LS: Completion Lists`, `Crash`, `7.0 LS Migration`)

**Re\-exporting a default export that doesn't exist with allowSyntheticDefaultExports true causes assert failures in getDefaultExportInfoWorker**

*Re-exporting a non-existent default export with allowSyntheticDefaultExports enabled triggers assertion failures in TypeScript’s import completion and auto imports.*

 * [6.9 years ago](https://github.com/microsoft/TypeScript/issues/29227#issuecomment-451251788) **weswigham** clarified that allowSyntheticDefaultExports permits synthetic defaults for interop and attributed the error to the language service's handling of synthetic defaults
 * **RyanCavanaugh** added to milestone `Backlog`
 * [6.3 years ago](https://github.com/microsoft/TypeScript/issues/29227#issuecomment-516940664) **kumarashwin** said "Thank you so much for your investigation! Finally got led to this very post which allowed me to solve the issue of import suggestions not working."
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/29227#issuecomment-3604486956) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#29292](https://github.com/microsoft/TypeScript/issues/29292) (Closed, `Bug`, `Domain: LS: TSServer`, `Domain: LS: Symbol Navigation`, `7.0 LS Migration`)

**Javascript, Nodejs: Go to definition for required file does not work if required file does not contain exports\.**

*Go to definition in VSCode for Node.js requires fails to navigate to modules without exports while working for modules that export values.*

 * **weswigham** added label `Domain: TSServer`
 * **RyanCavanaugh** added to milestone `Backlog`
 * **DanielRosenwasser** added label `Domain: Symbol Navigation`
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/29292#issuecomment-3604486977) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#29517](https://github.com/microsoft/TypeScript/issues/29517) (Closed, `Bug`, `Domain: LS: Signature Help`, `7.0 LS Migration`)

**\[TypeScript\] \[JSDoc\] Placing documentation for function below a decorator of the function \(as opposed to above it\) fails to associate with the function**

*In VS Code, JSDoc comments placed below decorators fail to attach to the decorated function.*

 * (6.8 years ago) **weswigham** added labels `Bug`, `Domain: Signature Help`
 * **RyanCavanaugh** added to milestone `Backlog`
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/29517#issuecomment-3604486996) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#29536](https://github.com/microsoft/TypeScript/issues/29536) (Closed, `Bug`, `Domain: LS: TSServer`, `7.0 LS Migration`)

**tsserver signals TS7017 incorrectly when using a symbol\-indexed property**

*tsserver in VSCode incorrectly flags TS7017 errors for symbol-indexed interface properties that tsc accepts.*

 * (6.8 years ago) **weswigham** added labels `Bug`, `Domain: TSServer`
 * **RyanCavanaugh** added to milestone `Backlog`
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * (today) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript/issues/29536#issuecomment-3604506497) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"

### [Issue microsoft/TypeScript#29730](https://github.com/microsoft/TypeScript/issues/29730) (Closed, `Bug`, `Domain: LS: Quick Fixes`, `7.0 LS Migration`)

**typescript/idea auto create method bug**

*TypeScript IDEA’s auto-create override for a protected rest-parameter method incorrectly omits the spread operator in the super call.*

 * (6.7 years ago) **RyanCavanaugh** added label `Domain: Quick Fixes`, set milestone to `Backlog`, and unassigned **rbuckton**
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * (today) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript/issues/29730#issuecomment-3604506515) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"

### [Issue microsoft/TypeScript#29972](https://github.com/microsoft/TypeScript/issues/29972) (Closed, `Bug`, `Help Wanted`, `Effort: Moderate`, `Domain: LS: Refactorings`, `7.0 LS Migration`)

**Missing comments after applying refactor/codefix**

*Several TypeScript refactors and codefixes unexpectedly remove comments when applied.*

 * (4.1 years ago) **andrewbranch** added label `Effort: Moderate`, and unassigned **jessetrinity**
 * **RyanCavanaugh** added label `Domain: Refactorings`
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * (today) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript/issues/29972#issuecomment-3604506541) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"

### [Issue microsoft/TypeScript#30056](https://github.com/microsoft/TypeScript/issues/30056) (Closed, `Bug`, `Domain: LS: Completion Lists`, `7.0 LS Migration`)

**Intellisense sometimes fails to show anything for Node modules**

*Intellisense intermittently fails to provide completions for Node modules after copy-pasting and editing require statements.*

 * [3.4 years ago](https://github.com/microsoft/TypeScript/issues/30056#issuecomment-1179943739) **xland** said "How about this issue's progress?"
 * [3.4 years ago](https://github.com/microsoft/TypeScript/issues/30056#issuecomment-1181120520) **RyanCavanaugh** said "None, apparently? 😅"
 * **RyanCavanaugh** added label `Domain: Completion Lists`
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * (today) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript/issues/30056#issuecomment-3604506573) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"

### [Issue microsoft/TypeScript#30093](https://github.com/microsoft/TypeScript/issues/30093) (Closed, `Bug`, `Domain: LS: Quick Fixes`, `7.0 LS Migration`)

**Weird type inference for binary plus**

*TypeScript infers x+y operand types as string|number, causing type errors because + can return string or number.*

 * (6.7 years ago) **RyanCavanaugh** set milestone to `Backlog`, removed from milestone `TypeScript 3.4.0`, and unassigned **sandersn**
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * (today) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript/issues/30093#issuecomment-3604506588) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"

### [Issue microsoft/TypeScript#30158](https://github.com/microsoft/TypeScript/issues/30158) (Closed, `Bug`, `Help Wanted`, `Effort: Moderate`, `Domain: Formatter`, `Domain: JSDoc`, `7.0 LS Migration`)

**Smart indentation is wrong following more than one line after JSDoc comments**

*Editor’s automatic indentation incorrectly adds an extra space after pressing enter twice following a JSDoc comment in TypeScript.*

 * (6.4 years ago) **RyanCavanaugh** set milestone to `Backlog`, removed from milestone `TypeScript 3.6.0`, and unassigned **PranavSenthilnathan**
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * (today) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript/issues/30158#issuecomment-3604506620) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"

### [Issue microsoft/TypeScript#30260](https://github.com/microsoft/TypeScript/issues/30260) (Closed, `Bug`, `Help Wanted`, `Domain: LS: Quick Fixes`, `7.0 LS Migration`)

**"Delete all unused declarations" on TS imports removes code in files**

*Delete all unused declarations codefix in VSCode for TypeScript removes body code as well as imports, causing unintended deletions.*

 * [5.9 years ago](https://github.com/microsoft/TypeScript/issues/30260#issuecomment-573306867) **ricklove** described an issue where the tool removed unused declarations beyond imports and suggested a safer 'remove all unused imports' feature
 * [1.1 years ago](https://github.com/microsoft/TypeScript/issues/30260#issuecomment-2405667527) **ravin00** suggested using the Typescript Hero VS Code extension and listed its features and keybindings
 * **RyanCavanaugh** added label `Domain: Quick Fixes`
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * (today) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript/issues/30260#issuecomment-3604506647) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"

### [Issue microsoft/TypeScript#30315](https://github.com/microsoft/TypeScript/issues/30315) (Closed, `Bug`, `Domain: LS: Auto-import`, `7.0 LS Migration`)

**Multiple issues with import quick fixes and project references**

*TypeScript import quick fixes neither suggest missing imports across project references nor generate correct paths for aliased modules.*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [4.3 years ago](https://github.com/microsoft/TypeScript/issues/30315#issuecomment-889128417) **lucasbasquerotto** asked for suggestions on fixing missing auto-imports for shared TypeScript code and later reported that symlinking and adjusting tsconfig resolved the issue
 * **RyanCavanaugh** added label `Domain: Auto-import`
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * (today) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript/issues/30315#issuecomment-3604506670) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"

### [Issue microsoft/TypeScript#30373](https://github.com/microsoft/TypeScript/issues/30373) (Closed, `Bug`, `Domain: LS: Type Display`, `Domain: LS: Quick Info`, `7.0 LS Migration`, **ahejlsberg**)

**QuickInfo misleading with signatures from higher order function type inference**

*TypeScript’s QuickInfo hover displays incorrect generic parameter renaming when inferring types in higher-order functions.*

 * **DanielRosenwasser** assigned to **ahejlsberg**
 * **RyanCavanaugh** added to milestone `Backlog`
 * [6.5 years ago](https://github.com/microsoft/TypeScript/issues/30373#issuecomment-498419518) **ajafff** reported that generated declaration file contained invalid references causing consumer type errors and linked related issues #31605 and #31544
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * (today) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript/issues/30373#issuecomment-3604506723) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"

### [Issue microsoft/TypeScript#30478](https://github.com/microsoft/TypeScript/issues/30478) (Closed, `Bug`, `Help Wanted`, `Effort: Moderate`, `Domain: LS: Refactorings`, `7.0 LS Migration`)

**Move to new file doesn't maintain prologues directives, ts\-check**

*Refactoring a function to a new file omits existing prologue directives like // @ts-check and "use strict".*

 * **DanielRosenwasser** added label `help wanted`
 * (4.3 years ago) **DanielRosenwasser** closed the issue
 * (4.3 years ago) **DanielRosenwasser** reopened the issue
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * (today) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript/issues/30478#issuecomment-3604506735) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"

### [Issue microsoft/TypeScript#31041](https://github.com/microsoft/TypeScript/issues/31041) (Closed, `Bug`, `Domain: LS: Symbol Navigation`, `7.0 LS Migration`)

**Go to definition unnecessary shows export along true definition**

*VSCode’s JavaScript go-to-definition feature unnecessarily displays both the function’s declaration and its module export entry.*

 * (6.6 years ago) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`
 * **DanielRosenwasser** added label `Domain: Symbol Navigation`
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * (today) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript/issues/31041#issuecomment-3604506758) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"

### [Issue microsoft/TypeScript#31091](https://github.com/microsoft/TypeScript/issues/31091) (Closed, `Bug`, `Domain: LS: Symbol Navigation`, `7.0 LS Migration`)

**Invalid Semantic Links for Inferred Type Arguments**

*Go-to-definition and rename fail to resolve property references in calls to generic methods when inferred Partial<TData> type arguments exactly match.*

 * [6.4 years ago](https://github.com/microsoft/TypeScript/issues/31091#issuecomment-510553300) **matt-tingen** described another case where the semantic link between infer U usages wasn't fully established, with operations like rename and find references only affecting the declaration and not other references
 * [5.6 years ago](https://github.com/microsoft/TypeScript/issues/31091#issuecomment-615857348) **hediet** said "Btw. this is still broken in v3.8.3."
 * **RyanCavanaugh** added label `Domain: Symbol Navigation`
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * (today) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript/issues/31091#issuecomment-3604506781) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"

### [Issue microsoft/TypeScript#31173](https://github.com/microsoft/TypeScript/issues/31173) (Closed, `Bug`, `Domain: LS: Quick Fixes`, `7.0 LS Migration`)

**\`paths\` not used for auto import**

*VS Code auto import fails to respect tsconfig paths and adds imports using the physical '_index' path instead of the '@myLib/example_2' alias.*

 * [4.8 years ago](https://github.com/microsoft/TypeScript/issues/31173#issuecomment-762300013) **nautilor** expressed gladness to help
 * [4.8 years ago](https://github.com/microsoft/TypeScript/issues/31173#issuecomment-762371075) **paustint** reported that auto-imports resolved to absolute file paths instead of relative paths in certain cases
 * [4.8 years ago](https://github.com/microsoft/TypeScript/issues/31173#issuecomment-762407375) **nautilor** illustrated that non-relative imports forced VS Code to use absolute paths, causing the import to resolve from the project root
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * (today) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript/issues/31173#issuecomment-3604506805) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"

### [Issue microsoft/TypeScript#31525](https://github.com/microsoft/TypeScript/issues/31525) (Closed, `Bug`, `Domain: LS: Symbol Navigation`, `7.0 LS Migration`)

**CTRL\-Click not working on require\('\.\.\.'\) path**

*Ctrl+Click navigation on relative require('./mocks.js') paths in JavaScript files is not working in VSCode 1.34.0 on Ubuntu 18.04.*

 * (6.4 years ago) **RyanCavanaugh** added labels `Bug`, `Domain: Symbol Navigation`, and set milestone to `Backlog`
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * (today) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript/issues/31525#issuecomment-3604506837) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"

### [Issue microsoft/TypeScript#31559](https://github.com/microsoft/TypeScript/issues/31559) (Closed, `Bug`, `Domain: LS: Symbol Navigation`, `7.0 LS Migration`)

**Go To Definition on call expression of union signature only shows one constituent signature**

*Go To Definition on a call expression for a union-typed function shows only one constituent signature instead of all signatures.*

 * **andrewbranch** added label `Bug`
 * **RyanCavanaugh** added to milestone `Backlog`
 * **DanielRosenwasser** added label `Domain: Symbol Navigation`
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * (today) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript/issues/31559#issuecomment-3604506840) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"

### [Issue microsoft/TypeScript#31630](https://github.com/microsoft/TypeScript/issues/31630) (Closed, `Bug`, `Domain: LS: Completion Lists`, `7.0 LS Migration`)

**Wrong typescript intelisense suggestions**

*VSCode's TypeScript IntelliSense shows wrong nested key suggestions for an overloaded get function despite accurate typings.*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [6.5 years ago](https://github.com/microsoft/TypeScript/issues/31630#issuecomment-497994574) **tanhauhau** said "I'm interested to try on this one. Maybe some pointers where I should start looking into?"
 * **RyanCavanaugh** added label `Domain: Completion Lists`
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * (today) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript/issues/31630#issuecomment-3604506878) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"

### [Issue microsoft/TypeScript#31825](https://github.com/microsoft/TypeScript/issues/31825) (Closed, `Bug`, `Domain: LS: Refactorings`, `7.0 LS Migration`)

**Doesn't support rename refactoring with importing from a module \(yarn workspaces\)**

*Renaming a module file in a Yarn workspace incorrectly updates only the aliased import path and not the local relative import.*

 * (6.4 years ago) **RyanCavanaugh** added labels `Bug`, `Domain: Refactorings`, and set milestone to `Backlog`
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * (today) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript/issues/31825#issuecomment-3604506911) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"

### [Issue microsoft/TypeScript#31898](https://github.com/microsoft/TypeScript/issues/31898) (Closed, `Bug`, `Domain: LS: Completion Lists`, `7.0 LS Migration`)

**Empty function suggestion returned in completionInfo result**

*TypeScript’s completionInfo API returns an unnamed function suggestion (empty name field) at certain cursor positions.*

 * (6.4 years ago) **RyanCavanaugh** added labels `Bug`, `Domain: Completion Lists`, and set milestone to `Backlog`
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * (today) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript/issues/31898#issuecomment-3604506938) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"

### [Issue microsoft/TypeScript#31966](https://github.com/microsoft/TypeScript/issues/31966) (Closed, `Bug`, `Domain: LS: Quick Info`, `7.0 LS Migration`)

**Intellisense mismatch for overload function vs paramaters**

*Hovering over an overloaded function with mismatched arguments displays the first overload instead of the last referenced by the errors.*

 * (6.4 years ago) **RyanCavanaugh** added labels `Bug`, `Domain: Quick Info`, and set milestone to `Backlog`
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * (today) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript/issues/31966#issuecomment-3604506964) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"

### [Issue microsoft/TypeScript#32036](https://github.com/microsoft/TypeScript/issues/32036) (Closed, `Bug`, `Domain: LS: Signature Help`, `7.0 LS Migration`)

**IntelliSense signature help forgets inferred parameter names in completed call**

*IntelliSense signature help reverts inferred tuple parameter names to generic names after a call is completed.*

 * (6.4 years ago) **RyanCavanaugh** added labels `Bug`, `Domain: Signature Help`, and set milestone to `Backlog`
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * (today) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript/issues/32036#issuecomment-3604506979) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"

