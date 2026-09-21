# Report for 2026-09-18 (Friday, September 18th, 2026)

19 different users commented on 165 different issues.

## Recommended Actions

 * Response Recommended
    * @TechQuery asked which version the fix would be released in in [microsoft/TypeScript#51885](https://github.com/microsoft/TypeScript/issues/51885#issuecomment-5739748405)
    * @rotu asked where TS2317 was appearing in the Workbench in [microsoft/TypeScript#57564](https://github.com/microsoft/TypeScript/issues/57564#issuecomment-5742046277)
    * @M393 provided repro steps as requested in [microsoft/TypeScript#60756](https://github.com/microsoft/TypeScript/issues/60756#issuecomment-5740721604)

## Activity Summary

### [Issue microsoft/TypeScript#39829](https://github.com/microsoft/TypeScript/issues/39829) (Closed, `Bug`, `Domain: lib.d.ts`, `Needs Human Review`, **RyanCavanaugh**, **Copilot**)

**HTMLImageElement\#crossOrigin should use literal union type from allowable values**

*HTMLImageElement.crossOrigin property should use the literal union type 'anonymous' | 'use-credentials' instead of string|null.*

 * (1 week ago) **RyanCavanaugh** added label `Needs Human Review`, and assigned to **Copilot**, **RyanCavanaugh**
 * (today) **github-actions[bot]** closed the issue

### [Issue microsoft/TypeScript#44334](https://github.com/microsoft/TypeScript/issues/44334) (Closed, `Bug`, `Needs More Info`, `Domain: lib.d.ts`)

**Breaking change 4\.3 RC: TS2488: Build:Type 'SomeArrayType' must have a '\[Symbol\.iterator\]\(\)' method that returns an iterator\.**

*TypeScript 4.3 RC incorrectly errors TS2488 on array spread when SymbolConstructor is moved to a custom namespace.*

 * **RyanCavanaugh** added label `Needs More Info`
 * [today](https://github.com/microsoft/TypeScript/issues/44334#issuecomment-5729091935) **NoelAbrahams** said "@RyanCavanaugh I no longer have access to that codebase, so, sorry, can't follow this up."
 * (today) **NoelAbrahams** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#50209](https://github.com/microsoft/TypeScript/issues/50209) (Closed, `Bug`, `Help Wanted`, `Domain: Comment Emit`)

**Repeated single line comment after variable declaration in if/for block when targeting ES5**

*TypeScript 4.7.4 misplaces single-line comments and splits variable declarations in ES5 if/for blocks.*

 * [3.8 years ago](https://github.com/microsoft/TypeScript/issues/50209#issuecomment-1320714408) **RyanCavanaugh** noted that it wasn't assigned to any milestone and recommended preprocessing the TS file before transpilation
 * [3.8 years ago](https://github.com/microsoft/TypeScript/issues/50209#issuecomment-1320732490) **toyobayashi** explained that they wrap preprocessor directives in comments before transpiling with tsc and then remove the comment markers afterward via a Node.js script to preserve directives in the output JavaScript files
 * **RyanCavanaugh** added label `Domain: Comment Emit`
 * **RyanCavanaugh** added label `Needs Human Review`

### [Issue microsoft/TypeScript#50240](https://github.com/microsoft/TypeScript/issues/50240) (Closed, `Bug`, `Fixed`, `Help Wanted`, `Domain: JSDoc`, `Needs Human Review`)

**Contextual 'this' parameter in JSDoc doesn't show correct completions after property assignment on \`this\` in function\-valued object literal property**

*Assigning properties to this inside a function-valued object literal causes JSDoc completions to ignore its defined type.*

 * [3.8 years ago](https://github.com/microsoft/TypeScript/issues/50240#issuecomment-1312607149) **asgoode** noted that the fix didn’t resolve other similar scenarios, tested behaviors across JavaScript and TypeScript in VS Code and the TS Playground with various syntaxes, confirmed that the core problem is the compiler’s constructor function assumptions, and asked if functions should only be treated as constructors when tagged with a @constructor JSDoc
 * [3.7 years ago](https://github.com/microsoft/TypeScript/issues/50240#issuecomment-1338707025) **XHighIntell** reported that the bug still existed on the latest version and provided environment details
 * **RyanCavanaugh** added label `Domain: JSDoc`
 * [today](https://github.com/microsoft/TypeScript/issues/50240#issuecomment-5737445747) **RyanCavanaugh** reported that current TypeScript 7.1.0-dev.20260918.1 included the fix and restored proper completions in the long-form JavaScript property case, contrasting with 4.8.4 which only showed apiBoolean and noting 4.9.3 was already correct
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#50608](https://github.com/microsoft/TypeScript/issues/50608) (Closed, `Bug`, `Fixed`, `Domain: Intersection`, `Needs Human Review`)

**Unexpected assignability**

*TypeScript fails to report an incorrect return type assignment for union types after updating from version 3.5.1 to 3.6.2.*

 * (4 years ago) **andrewbranch** added label `Bug`, and set milestone to `Backlog`
 * **RyanCavanaugh** added label `Domain: Intersection`
 * [today](https://github.com/microsoft/TypeScript/issues/50608#issuecomment-5737488085) **RyanCavanaugh** noted that the assignment was accepted in 4.7.4 and 4.9.0-dev.20221013 but began failing with TS2322 from 4.9.0-dev.20221014 onward due to PR #51140
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#50635](https://github.com/microsoft/TypeScript/issues/50635) (Closed, `Bug`, `Fixed`, `Domain: check: Type Inference`, `Rescheduled`, `Has Repro`, `Needs Human Review`, **andrewbranch**)

**Regression in 4\.8 where string union type widens to string**

*String union types now incorrectly widen to string in TypeScript 4.8, regressing the behavior from 4.7.4.*

 * (2.1 years ago) **RyanCavanaugh** added label `Domain: Type Inference`, and set milestone to `TypeScript 5.7.0`
 * **jakebailey** removed label `Fix Available`
 * [today](https://github.com/microsoft/TypeScript/issues/50635#issuecomment-5737499609) **RyanCavanaugh** noted that the issue was fixed by PR #61668 and that the literal union is preserved from version 5.9.0-dev.20250610 onward
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#50684](https://github.com/microsoft/TypeScript/issues/50684) (Closed, `Bug`, `Fixed`, `Domain: check: Type Inference`, `Needs Human Review`)

**Type inference destructure object**

*TypeScript fails to correctly infer the types of rest properties when destructuring objects.*

 * [4 years ago](https://github.com/microsoft/TypeScript/issues/50684#issuecomment-1242336573) **andrewbranch** said "@herrlegno that’s a duplicate of #241 (congrats, you found a three-digit one!)"
 * **andrewbranch** added to milestone `Backlog`
 * **RyanCavanaugh** added label `Domain: Type Inference`
 * [today](https://github.com/microsoft/TypeScript/issues/50684#issuecomment-5737558759) **RyanCavanaugh** noted that the issue was fixed in PR #50081 and that diagnostics now correctly explain missing properties starting in 5.0.0-dev.20221108 and TypeScript 6.0.3
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#50883](https://github.com/microsoft/TypeScript/issues/50883) (Closed, `Bug`, `Fixed`, `Help Wanted`, `Effort: Moderate`, `Rescheduled`, `Domain: Parser`, `Needs Human Review`, **DanielRosenwasser**)

**Make private field name parsing ecma 262 compliant**

*Support private field names starting with Unicode or extended Unicode escapes per ECMA 262 to fix parse errors.*

 * (2.1 years ago) **RyanCavanaugh** added label `Domain: Parser`, set milestone to `TypeScript 5.7.0`, and removed from milestone `TypeScript 5.5.0`
 * [today](https://github.com/microsoft/TypeScript/issues/50883#issuecomment-5737529492) **RyanCavanaugh** confirmed that the parsing issue with extended Unicode escapes was fixed in version 4.9.0-dev.20221001, TypeScript 6.0.3, and native TypeScript thanks to PR #50918
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#50917](https://github.com/microsoft/TypeScript/issues/50917) (Closed, `Bug`, `Fixed`, `Help Wanted`, `Domain: Declaration Emit`, `Needs Human Review`)

**Module names in declaration files mismatch with keys in dependencies**

*TypeScript with nodenext resolution generates declarations importing from package1 instead of the pkg1 dependency alias.*

 * (3.9 years ago) **RyanCavanaugh** added labels `Help Wanted`, `Domain: Declaration Emit`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/50917#issuecomment-5737616137) **RyanCavanaugh** fixed the package-alias example to emit the declared alias and noted the change in output between TypeScript versions 4.8.3 and 6.0.3
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#51133](https://github.com/microsoft/TypeScript/issues/51133) (Closed, `Bug`, `Fixed`, `Help Wanted`, `Domain: JSDoc`, `Needs Human Review`)

**JSDoc @link masked URL hyperlinks too far**

*VS Code’s JSDoc @link implementation misparses masked URLs by extending hyperlinks beyond the pipe separator.*

 * (3.9 years ago) **RyanCavanaugh** added labels `Help Wanted`, `Domain: JSDoc`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/51133#issuecomment-5737515818) **RyanCavanaugh** reported that TypeScript 7.1.0-dev.20260918.1 splits the URL and link label at the pipe character, whereas 4.9.0-dev.20221007 returned the full inline tag as undivided text
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript/issues/51133#issuecomment-5737804149) **SethFalco** confirmed it worked as expected and noted it was fixed in TypeScript v5.4.2

### [Issue microsoft/TypeScript#51376](https://github.com/microsoft/TypeScript/issues/51376) (Open, `Bug`, `Needs More Info`, `Help Wanted`, `Domain: Related Error Spans`, `Needs Human Review`)

**Spread operator with wrong optional property raises error on incorrect source line**

*TypeScript misreports error location when spreading an object with an optional property into a stricter type*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [3.8 years ago](https://github.com/microsoft/TypeScript/issues/51376#issuecomment-1300397370) **isaacudofia** said "Probably no solution until they fix it, except replacing the … operator with Object.assign"
 * **RyanCavanaugh** added label `Domain: Related Error Spans`
 * [today](https://github.com/microsoft/TypeScript/issues/51376#issuecomment-5737556389) **RyanCavanaugh** requested tsconfig.json settings, editor/extension version, and exact source to reproduce the error
 * (today) **RyanCavanaugh** added labels `Needs Human Review`, `Needs More Info`

### [Issue microsoft/TypeScript#51636](https://github.com/microsoft/TypeScript/issues/51636) (Open, `Bug`, `Help Wanted`, `Domain: lib.d.ts`, `Needs Human Review`, **RyanCavanaugh**, **Copilot**)

**\`Date\.getVarDate\(\)\` function seems incorrectly defined**

*TypeScript incorrectly defines the non-standard ActiveX Date.getVarDate method as a required property instead of removing or making it optional.*

 * (3.8 years ago) **RyanCavanaugh** added labels `Help Wanted`, `Domain: lib.d.ts`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/51636#issuecomment-5737579036) **RyanCavanaugh** pointed out that Date#getVarDate remained declared in lib.scripthost.d.ts and suggested removing it since it is not present in Edge 153
 * (today) **RyanCavanaugh** added label `Needs Human Review`, and assigned to **Copilot**, **RyanCavanaugh**

### [Issue microsoft/TypeScript#51661](https://github.com/microsoft/TypeScript/issues/51661) (Open, `Bug`, `Needs More Info`, `Help Wanted`, `Domain: This-Typing`, `Needs Human Review`)

**Type\-asserting function call on variable initialized using \`this\` causes false implicit\-any in VSCode**

*VSCode's TypeScript support falsely flags implicit-any when using a type-asserting function on a property accessed via untyped `this` in callbacks.*

 * [3.7 years ago](https://github.com/microsoft/TypeScript/issues/51661#issuecomment-1361478725) **OxleyS** identified a source of circularity in type inference and provided call stack details
 * [2.9 years ago](https://github.com/microsoft/TypeScript/issues/51661#issuecomment-1764393743) **wlinna** provided a reproduction case with code samples demonstrating the bug and noted configurations where it did not occur
 * **RyanCavanaugh** added label `Domain: This-Typing`
 * [today](https://github.com/microsoft/TypeScript/issues/51661#issuecomment-5737570095) **RyanCavanaugh** reported inability to reproduce TS7022 in multiple TypeScript versions and requested a server log with specific request ordering
 * (today) **RyanCavanaugh** added labels `Needs Human Review`, `Needs More Info`

### [Issue microsoft/TypeScript#51885](https://github.com/microsoft/TypeScript/issues/51885) (Closed, `Bug`, `Fixed`, `Help Wanted`, `Domain: lib.d.ts`, `Needs Human Review`)

**\[type bug\] fontfaces property is missing from loadingdone event object**

*Update FontFaceSet's onloadingdone handler type from Event to FontFaceSetLoadEvent to expose fontfaces property.*

 * (3.7 years ago) **RyanCavanaugh** added labels `Help Wanted`, `Domain: lib.d.ts`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/51885#issuecomment-5737613564) **RyanCavanaugh** noted that PR #60061 updated the onloadingdone event to FontFaceSetLoadEvent in TS 5.7.0-dev.20240928, enabling event.fontfaces
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript/issues/51885#issuecomment-5739748405) **TechQuery** asked which version the fix would be released in

### [Issue microsoft/TypeScript#52033](https://github.com/microsoft/TypeScript/issues/52033) (Closed, `Bug`, `Fixed`, `Help Wanted`, `Domain: Declaration Emit`, `Needs Human Review`)

**Redundant "has or is using private name" diagnostic when name not found**

*TypeScript erroneously emits a redundant “has or is using private name” error for exported variables with missing type names when declaration generation is enabled.*

 * (3.7 years ago) **RyanCavanaugh** added labels `Help Wanted`, `Domain: Declaration Emit`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/52033#issuecomment-5737628198) **RyanCavanaugh** explained that PR #58536 fixed the issue and described how diagnostics changed in later TypeScript versions
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#52042](https://github.com/microsoft/TypeScript/issues/52042) (Closed, `Bug`, `Fixed`, `Help Wanted`, `Domain: JSDoc`, `Needs Human Review`)

**Irregular behavior of equivalent code between \`\.js\` and \`\.ts\`\.**

*Defining a generic memoize function with JSDoc type imports in a JavaScript file under checkJs/allowJs produces inconsistent type-checking behavior compared to the equivalent TypeScript implementation.*

 * [1.5 years ago](https://github.com/microsoft/TypeScript/issues/52042#issuecomment-2643500138) **regseb** demonstrated a type-checking error with foo when using checkJs but not in TS
 * **RyanCavanaugh** added label `Domain: JSDoc`
 * [47 weeks ago](https://github.com/microsoft/TypeScript/issues/52042#issuecomment-3421095002) **qraynaud** demonstrated that using the imported JSDoc KeyValueMapper type yielded different type inference compared to the inline-defined type for unique symbol keys and values
 * [today](https://github.com/microsoft/TypeScript/issues/52042#issuecomment-5737612829) **RyanCavanaugh** noted that the issue was fixed by PR #56907 and that the tuple callback example now passed starting with version 5.9.0-dev.20250220 and later
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#52430](https://github.com/microsoft/TypeScript/issues/52430) (Closed, `Bug`, `Fixed`, `Help Wanted`, `Domain: check: Control Flow`, `Needs Human Review`)

**Assertion type function not working as expected with everything but ES3 since \>=4\.9\.4**

*Assertion type functions using 'asserts actual is InstanceType<Expects>' no longer narrow types in TypeScript ≥4.9.4 except ES3*

 * [3.6 years ago](https://github.com/microsoft/TypeScript/issues/52430#issuecomment-1405334179) **ahejlsberg** said "Turns out this is fixed by #52392. The issue is that we aren't properly propagating the intersectionState flags when checking signatures in type relations."
 * [3.6 years ago](https://github.com/microsoft/TypeScript/issues/52430#issuecomment-1405343165) **ahejlsberg** said "Ah, nevermind, it isn't fixed by #52392. However, it only reproduces when --strictBindCallApply is enabled."
 * **RyanCavanaugh** added label `Domain: Control Flow`
 * [today](https://github.com/microsoft/TypeScript/issues/52430#issuecomment-5737673446) **RyanCavanaugh** stated that the issue was fixed with --strictBindCallApply and linked to pull request #54753, noting it compiled with recent dev builds and in TypeScript 6.0.3 and the current native compiler
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#52463](https://github.com/microsoft/TypeScript/issues/52463) (Closed, `Bug`, `Fixed`, `Website`, `Domain: Crashes`, `Needs Human Review`)

**Internal compiler error: "DataCloneError: Function object could not be cloned\."**

*TypeScript Playground throws a DataCloneError when compiling a simple conditional type expression across all versions.*

 * (3.6 years ago) **RyanCavanaugh** added labels `Website`, `Domain: Crashes`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/52463#issuecomment-5737661053) **RyanCavanaugh** reported that the Playground handled the original example without a worker cloning failure and that the current Nightly build reported the expected TS2304 diagnostics for B and C without any DataCloneError or postMessage cloning error
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#52912](https://github.com/microsoft/TypeScript/issues/52912) (Closed, `Bug`, `Fixed`, `Help Wanted`, `Cursed?`, `Domain: check: Error Instability`, `Needs Human Review`)

**Undetected illegal assignment of nested array types**

*TypeScript silently allows illegal assignments of nested array types once nesting exceeds three levels.*

 * [3.5 years ago](https://github.com/microsoft/TypeScript/issues/52912#issuecomment-1445152911) **martinwepner** thanked RyanCavanaugh, explained how a nested ORM data structure triggered an undetected type cycle in TypeScript, questioned why cycle detection was difficult, and requested guidance on where to start investigating the codebase
 * [3.5 years ago](https://github.com/microsoft/TypeScript/issues/52912#issuecomment-1447161899) **RyanCavanaugh** clarified that the example shows infinite descent of novel types rather than simple cycles, provided a patch link to remove the recursion depth limit and pointed to failing tests and a demonstration case, and noted that no known fix exists while welcoming PRs
 * **RyanCavanaugh** added label `Domain: Error Instability`
 * [today](https://github.com/microsoft/TypeScript/issues/52912#issuecomment-5737696960) **RyanCavanaugh** reported that native TypeScript 7.1.0-dev.20260918.1 now emits TS2322 errors for Source1/Target1, Source2/Target2, and Source3/Target3 while still reporting the missing someNewProperty error for Source4/Target4, and noted that Classic TypeScript 6.0.3 only reports the Source4/Target4 error and that the nested-array assignment issue is fixed in TS7
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#53111](https://github.com/microsoft/TypeScript/issues/53111) (Closed, `Bug`, `Fixed`, `Help Wanted`, `Domain: Declaration Emit`, `Needs Human Review`)

**TSC emits invalid \.d\.ts file with reserved keywords in identifier position**

*TypeScript emits .d.ts files containing reserved keywords such as 'delete' as identifiers, leading to compilation errors.*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [2.5 years ago](https://github.com/microsoft/TypeScript/issues/53111#issuecomment-1991191200) **jaydenseric** reported a TypeScript 5.4.2 error about reserved word 'delete' in JSDoc links
 * **RyanCavanaugh** added label `Domain: Declaration Emit`
 * [today](https://github.com/microsoft/TypeScript/issues/53111#issuecomment-5737715737) **RyanCavanaugh** noted that the original JavaScript example still emitted an invalid import in TypeScript 6.0.3 but that TypeScript 7.1.0-dev emitted a valid declaration and fixed the issue in the native implementation
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#53276](https://github.com/microsoft/TypeScript/issues/53276) (Closed, `Bug`, `Fixed`, `Domain: Literal Types`, `Needs Human Review`)

**\`unique symbol\`s from the global \`SymbolConstructor\` widen way too eagerly**

*TypeScript incorrectly errors on accessing properties keyed by the built-in unique symbol Symbol.toStringTag because it widens the unique symbol type too eagerly.*

 * [3.5 years ago](https://github.com/microsoft/TypeScript/issues/53276#issuecomment-1472676262) **weswigham** explained that unique symbols subsumed well-known symbols and removed the concept of well-known symbols from the checker’s code
 * [3.5 years ago](https://github.com/microsoft/TypeScript/issues/53276#issuecomment-1472694876) **fatcerberus** described seeing unique symbol as a special nominal type implying unforgeable values
 * **RyanCavanaugh** added to milestone `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/53276#issuecomment-5737759125) **RyanCavanaugh** noted that the original example was fixed, TS7053 errors were resolved by version 5.7.0-dev.20240924 and TypeScript 6.0.3, and linked PR #59860 which makes non-literal computed class members participate in the class type
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#53559](https://github.com/microsoft/TypeScript/issues/53559) (Closed, `Bug`, `Fixed`, `Domain: Error Messages`, `Rescheduled`, `Needs Human Review`, **DanielRosenwasser**)

**Error for explicit return type with no return statements is misleading**

*Compiler error erroneously disallows functions with explicit return types and no return statements despite supporting unknown annotations.*

 * (2.1 years ago) **RyanCavanaugh** set milestone to `TypeScript 5.7.0`, and removed from milestone `TypeScript 5.5.0`
 * **jakebailey** removed label `Fix Available`
 * [today](https://github.com/microsoft/TypeScript/issues/53559#issuecomment-5737789803) **RyanCavanaugh** reported that the issue was fixed by PR #53607 and detailed version behavior
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#53605](https://github.com/microsoft/TypeScript/issues/53605) (Closed, `Bug`, `Help Wanted`, `Domain: Module Resolution`, `Needs Human Review`)

**\`ts\.isUrl\` and \`ts\.pathIsAbsolute\` return false for data urls**

*ts.isUrl and ts.pathIsAbsolute incorrectly return false for data URLs, causing improper path resolution in TypeScript.*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [3.4 years ago](https://github.com/microsoft/TypeScript/issues/53605#issuecomment-1492944997) **Mayank1728** said "Hello @dsherret ! I am ready to grab this, however, i have never contributed to opensource before please can you guide me on what needs to be done exactly ?"
 * **RyanCavanaugh** added label `Domain: Module Resolution`
 * [today](https://github.com/microsoft/TypeScript/issues/53605#issuecomment-5737768485) **RyanCavanaugh** said "The reported behavior is in the pre-TypeScript-7 JavaScript Compiler API. That API has been superseded and is no longer being developed, so this change will not be implemented."
 * **RyanCavanaugh** added label `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#53737](https://github.com/microsoft/TypeScript/issues/53737) (Open, `Bug`, `Needs More Info`, `Help Wanted`, `Domain: JSDoc`, `Needs Human Review`)

**Please Allow Mixins to function properly with new\-able types**

*Mixins defined as generic new-able types returning intersection types aren’t processed correctly, preventing VS Code from offering property completions.*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [3.2 years ago](https://github.com/microsoft/TypeScript/issues/53737#issuecomment-1605742030) **Andarist** said "I can't repro this quickly. Could you prepare a runnable repository that would showcase the problem?"
 * **RyanCavanaugh** added label `Domain: JSDoc`
 * [today](https://github.com/microsoft/TypeScript/issues/53737#issuecomment-5737797371) **RyanCavanaugh** asked for additional reproduction details after failing to reproduce the missing members issue
 * (today) **RyanCavanaugh** added labels `Needs Human Review`, `Needs More Info`

### [Issue microsoft/TypeScript#53775](https://github.com/microsoft/TypeScript/issues/53775) (Closed, `Bug`, `Fixed`, `Help Wanted`, `Domain: Declaration Emit`, `Needs Human Review`)

**Accessors are always reduced to properties in object literal declarations**

*TypeScript declaration generation collapses object literal getters and setters into a single property, losing distinct accessor types.*

 * (3.4 years ago) **RyanCavanaugh** added labels `Help Wanted`, `Domain: Declaration Emit`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/53775#issuecomment-5737829366) **RyanCavanaugh** noted that the issue was fixed by PR #55442 and described the updated declaration-only emit behavior across TypeScript versions
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#53925](https://github.com/microsoft/TypeScript/issues/53925) (Closed, `Bug`, `Help Wanted`, `Domain: API: Transforms`, `Needs Human Review`)

**Typescript emits invalid AMD with custom tranformation of export syntax**

*A custom transformer rewriting export declarations into separate export statements produces invalid AMD module output in TypeScript 4.7.4 and 5.0.4.*

 * (3.4 years ago) **RyanCavanaugh** added labels `Help Wanted`, `Domain: Transforms`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/53925#issuecomment-5737805769) **RyanCavanaugh** explained that the AMD emit behavior for custom transformers in the pre-TypeScript-7 Compiler API used by transpileModule would not change and that the related issue was closed as Won't Fix
 * **RyanCavanaugh** added label `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#54099](https://github.com/microsoft/TypeScript/issues/54099) (Open, `Bug`, `Help Wanted`, `Docs`, `Domain: Decorators`, `Needs Human Review`)

**Unknown interface "ClassMethodDecoratorFunction" in documentation for 5\.0\.4 lib\.decorators\.d\.ts**

*TypeScript 5.0.4 decorators.d.ts documentation incorrectly references a non-existent ClassMethodDecoratorFunction interface instead of ClassMethodDecoratorContext.*

 * [2.1 years ago](https://github.com/microsoft/TypeScript/issues/54099#issuecomment-2269358203) **samueldcorbin** said "In addition to using a type that isn't defined, the example also uses non-existent function syntax."
 * [1.7 years ago](https://github.com/microsoft/TypeScript/issues/54099#issuecomment-2558930168) **d07RiV** said "Even if the function is explicitly typed, it still runs into an issue trying to index this[context.name] :|"
 * **RyanCavanaugh** added label `Domain: Decorators`
 * (today) **RyanCavanaugh** added labels `Docs`, `Needs Human Review`

### [Issue microsoft/TypeScript#54237](https://github.com/microsoft/TypeScript/issues/54237) (Closed, `Bug`, `Fixed`, `Help Wanted`, `Domain: check: Type Inference`, `Needs Human Review`)

**Error when destructuring deep nested object with literal initializers as fallback**

*Destructuring a deeply nested optional object with fallback {} erroneously fails to default missing properties to undefined.*

 * [3.3 years ago](https://github.com/microsoft/TypeScript/issues/54237#issuecomment-1551756061) **RyanCavanaugh** noted that the non-nested version worked as expected
 * [3.3 years ago](https://github.com/microsoft/TypeScript/issues/54237#issuecomment-1553134298) **xsjcTony** noted that an alternative nested destructuring approach also worked, mentioned only the nested object case failed, and updated the playground link
 * **RyanCavanaugh** added label `Domain: Type Inference`
 * [today](https://github.com/microsoft/TypeScript/issues/54237#issuecomment-5737901949) **RyanCavanaugh** noted that PR #59183 fixed the issue and that nested destructuring errored in 5.6.0-dev.20240715 but compiled cleanly in later versions
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#54335](https://github.com/microsoft/TypeScript/issues/54335) (Closed, `Bug`, `Fixed`, `Help Wanted`, `Domain: Intersection`, `Needs Human Review`)

**Types intersected with string literal or 'unique symbol' error on computed property name declaration but only if it's abstract\.**

*Abstract class methods using computed property names from intersected string literal or unique symbol types incorrectly produce errors.*

 * [3.2 years ago](https://github.com/microsoft/TypeScript/issues/54335#issuecomment-1606071481) **Andarist** asked what behavior would be expected here
 * [3.2 years ago](https://github.com/microsoft/TypeScript/issues/54335#issuecomment-1606582405) **miguel-leon** described suggestions for handling incorrect overload detection by either checking primitive indexable types or accepting ambiguity to reduce complexity
 * **RyanCavanaugh** added label `Domain: Intersection`
 * [today](https://github.com/microsoft/TypeScript/issues/54335#issuecomment-5737881460) **RyanCavanaugh** noted that PR #60052 fixed the issue and that abstract computed members originally reported TS1168 in 5.8.0-dev.20250124 but compiled successfully in 5.8.0-dev.20250125, TypeScript 6.0.3, and the current native compiler
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#54338](https://github.com/microsoft/TypeScript/issues/54338) (Open, `Bug`, `Help Wanted`, `Docs`, `Domain: Decorators`, `Needs Human Review`)

**Comment referencing an undefined \`ClassDecoratorFunction\` type**

*decorators.d.ts references an undefined ClassDecoratorFunction type in the library definitions*

 * (3.3 years ago) **RyanCavanaugh** added labels `Help Wanted`, `Domain: Decorators`, and set milestone to `Backlog`
 * (today) **RyanCavanaugh** added labels `Docs`, `Needs Human Review`

### [Issue microsoft/TypeScript#54352](https://github.com/microsoft/TypeScript/issues/54352) (Closed, `Bug`, `Help Wanted`, `Crash`, `Domain: Node ESM`, `Needs Human Review`)

**Crash \`Unhandled type Any\` on ESM\-mode namespace import of \`module\.exports = null\`**

*TypeScript crashes with an “Unhandled type Any” error when namespace-importing a CommonJS module that exports null in ESM mode*

 * (3.3 years ago) **andrewbranch** added label `Crash`, and set milestone to `Backlog`
 * **RyanCavanaugh** added label `Domain: Node ESM`
 * [today](https://github.com/microsoft/TypeScript/issues/54352#issuecomment-5737854921) **RyanCavanaugh** marked the issue as duplicate of #51099 and noted that the crash was fixed by merged PR #51136
 * **RyanCavanaugh** added label `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#54372](https://github.com/microsoft/TypeScript/issues/54372) (Open, `Bug`, `Help Wanted`, `Domain: lib.d.ts`, `Needs Human Review`, **RyanCavanaugh**, **Copilot**)

**\`autocapitalize\` type is incorrect according to MDN**

*HTMLElement.autocapitalize is currently typed as string in TypeScript’s DOM lib instead of a restricted union of valid autocapitalize keywords.*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [3.3 years ago](https://github.com/microsoft/TypeScript/issues/54372#issuecomment-1565006473) **RyanCavanaugh** stated that they generally accepted these breaking changes to prevent typos like using 'character' for autocapitalize
 * [3.3 years ago](https://github.com/microsoft/TypeScript/issues/54372#issuecomment-1565019483) **michaelwarren1106** offered to make a PR and asked if other prop types also needed updating or just the known one
 * [today](https://github.com/microsoft/TypeScript/issues/54372#issuecomment-5737874680) **RyanCavanaugh** noted that HTMLElement.autocapitalize was declared as string in TypeScript, allowing invalid keywords like "character", and suggested using a keyword union to catch errors early
 * (today) **RyanCavanaugh** added label `Needs Human Review`, and assigned to **Copilot**, **RyanCavanaugh**

### [Issue microsoft/TypeScript#54387](https://github.com/microsoft/TypeScript/issues/54387) (Open, `Bug`, `Help Wanted`, `Domain: lib.d.ts`, `Needs Human Review`, **RyanCavanaugh**, **Copilot**)

**Notes about \`String\.replace\`**

*TypeScript's String.replace overloads lack a unified second-parameter union, causing errors when using string-or-function replacements.*

 * [3 years ago](https://github.com/microsoft/TypeScript/issues/54387#issuecomment-1712437149) **graphemecluster** said "I am happy to modify #50452 to fix this."
 * [2.6 years ago](https://github.com/microsoft/TypeScript/issues/54387#issuecomment-1899806758) **jwasnoggin** provided a TypeScript definition allowing a union while preserving Symbol.replace
 * [49 weeks ago](https://github.com/microsoft/TypeScript/issues/54387#issuecomment-3374188716) **electrovir** reported that the implementation blocked union-type replaceValue parameters, causing a compiler error
 * [today](https://github.com/microsoft/TypeScript/issues/54387#issuecomment-5737883099) **RyanCavanaugh** explained that String.prototype.replace runtime behavior accepts either a string or a function but the lib.d.ts overloads reject a union of those types, causing TS2769 in several TypeScript versions
 * (today) **RyanCavanaugh** added label `Needs Human Review`, and assigned to **Copilot**, **RyanCavanaugh**

### [Issue microsoft/TypeScript#54429](https://github.com/microsoft/TypeScript/issues/54429) (Open, `Bug`, `Needs More Info`, `Help Wanted`, `Domain: Binder`, `Needs Human Review`)

**Unexpected "used before its declaration" error when implementing a exported type of a merged namespace**

*Implementing a merged Foo namespace interface in a class triggers a 'used before its declaration' error after redeclaring Foo.*

 * (3.3 years ago) **RyanCavanaugh** added labels `Help Wanted`, `Domain: Binder`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/54429#issuecomment-5737887908) **RyanCavanaugh** could not reproduce the issue on TypeScript 4.7.3 or 5.0.4 and requested exact editor sequence, file contents, actions, error timing, and a tsserver protocol log
 * (today) **RyanCavanaugh** added labels `Needs Human Review`, `Needs More Info`

### [Issue microsoft/TypeScript#54466](https://github.com/microsoft/TypeScript/issues/54466) (Closed, `Bug`, `Fixed`, `Help Wanted`, `Domain: lib.d.ts`, `Needs Human Review`)

**URLSearchParams needs size**

*URLSearchParams.size property is missing from TypeScript's definitions causing a type error when accessed.*

 * (3.3 years ago) **RyanCavanaugh** added label `Domain: lib.d.ts`, and set milestone to `Backlog`
 * [3.1 years ago](https://github.com/microsoft/TypeScript/issues/54466#issuecomment-1649041928) **bencmbrook** noted that URLSearchParams.size rolled out to Chrome and Firefox (Safari experimental) and appeared in dom.generated.d.ts
 * [today](https://github.com/microsoft/TypeScript/issues/54466#issuecomment-5737917156) **RyanCavanaugh** described that URLSearchParams.size was added by PR #54725 and noted TS2339 in 5.2.0-dev.20230621 but acceptance in subsequent versions
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#54742](https://github.com/microsoft/TypeScript/issues/54742) (Closed, `Bug`, `Help Wanted`, `Domain: Comment Emit`, `Needs Human Review`)

**Synthetic comment duplicated 3 times on class with experimental decorators**

*Experimental decorators in TypeScript 5.1 cause synthetic leading comments to be duplicated three times instead of once in transformer output*

 * (3.2 years ago) **RyanCavanaugh** added labels `Help Wanted`, `Domain: Comment Emit`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/54742#issuecomment-5737912120) **RyanCavanaugh** explained that the TS 5.1.6 reproduction emitted four copies of the synthetic leading comment due to the deprecated legacy decorator transform and that the pre-TS7 JS Compiler API will not be further updated
 * **RyanCavanaugh** added label `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#55077](https://github.com/microsoft/TypeScript/issues/55077) (Closed, `Bug`, `Help Wanted`, `Domain: lib.d.ts`, `Needs Human Review`)

**Array\<T\>\.reduce\<U\> method description contains mismatched parameter in description**

*The JSDoc for Array<T>.reduce<U> in lib.es5.d.ts incorrectly names the callback's first parameter accumulator instead of previousValue.*

 * [3.1 years ago](https://github.com/microsoft/TypeScript/issues/55077#issuecomment-1645343063) **kirillkurko** said "Can I try to take this one and address it?"
 * [3 years ago](https://github.com/microsoft/TypeScript/issues/55077#issuecomment-1676393464) **JoshuaKGoldberg** referred kirillkurko to the contributing guide's issue-claiming section and asked if they were still interested in the issue
 * **RyanCavanaugh** added label `Domain: lib.d.ts`
 * [today](https://github.com/microsoft/TypeScript/issues/55077#issuecomment-5737941562) **RyanCavanaugh** clarified that the reduce callback’s first parameter is named previousValue in the TypeScript declaration and that no mismatch exists
 * **RyanCavanaugh** added label `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#55162](https://github.com/microsoft/TypeScript/issues/55162) (Closed, `Bug`, `Fixed`, `Help Wanted`, `Domain: lib.d.ts`, `Needs Human Review`)

**CanvasRenderingContext2D has no reset\(\) method**

*TypeScript’s CanvasRenderingContext2D declaration omits the standard reset() method, causing compile errors.*

 * [3.1 years ago](https://github.com/microsoft/TypeScript/issues/55162#issuecomment-1652864456) **yessGlory17** asked how to update the lib.d.ts file after not finding it in src/lib
 * [3.1 years ago](https://github.com/microsoft/TypeScript/issues/55162#issuecomment-1652882746) **yessGlory17** asked why reset was defined in CanvasState and expressed confusion about the problem
 * [3.1 years ago](https://github.com/microsoft/TypeScript/issues/55162#issuecomment-1665903500) **druckmax** reported the same TypeScript error on CanvasRenderingContext2D.reset and asked if a solution existed, noting that @ts-ignore worked in Chrome and Firefox but failed in Safari
 * [today](https://github.com/microsoft/TypeScript/issues/55162#issuecomment-5737965487) **RyanCavanaugh** noted fix in PR #54725, reported that `context.reset()` errored in 5.2.0-dev.20230621 but compiled cleanly in later builds, and mentioned that the browser API exposes CanvasRenderingContext2D.reset()
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#55210](https://github.com/microsoft/TypeScript/issues/55210) (Open, `Bug`, `Needs More Info`, `Domain: Something Else`, `Needs Human Review`, **iisaduan**)

**\[ServerErrors\]\[TypeScript\] 5\.2\.0\-dev\.20230730**

*TypeScript 5.2.0-dev.20230730 reported server errors and detected changes across analysis of 200 popular GitHub repositories.*

 * (3.1 years ago) **RyanCavanaugh** added labels `Bug`, `Domain: Something Else`, and assigned to **iisaduan**
 * [today](https://github.com/microsoft/TypeScript/issues/55210#issuecomment-5737973132) **RyanCavanaugh** requested attaching the referenced replay logs or providing a self-contained tsserver request sequence to reproduce the crash
 * (today) **RyanCavanaugh** added labels `Needs Human Review`, `Needs More Info`

### [Issue microsoft/TypeScript#55497](https://github.com/microsoft/TypeScript/issues/55497) (Closed, `Bug`, `Help Wanted`, `Effort: Moderate`, `Crash`, `Domain: Crashes`, `Needs Human Review`)

**\`transpileModule\`: debug failure crash**

*transpileModule crashes with a Debug Failure error when processing fuzzer-generated input in TypeScript 5.2.0.*

 * [3 years ago](https://github.com/microsoft/TypeScript/issues/55497#issuecomment-1702932745) **Krytan** offered to solve the issue if it was still open and asked for permission to begin
 * [3 years ago](https://github.com/microsoft/TypeScript/issues/55497#issuecomment-1703080229) **andrewbranch** said "Go for it 👉 https://github.com/microsoft/TypeScript/blob/main/CONTRIBUTING.md#issue-claiming"
 * **RyanCavanaugh** added label `Domain: Crashes`
 * [today](https://github.com/microsoft/TypeScript/issues/55497#issuecomment-5737990416) **RyanCavanaugh** said "transpileModule is part of the pre-TypeScript-7 JavaScript Compiler API, which has been superseded and is no longer being developed. We are therefore not taking new fixes for this API crash."
 * **RyanCavanaugh** added label `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#55526](https://github.com/microsoft/TypeScript/issues/55526) (Closed, `Bug`, `Fixed`, `Domain: flag: exactOptionalPropertyTypes`, `Needs Human Review`)

**Assigning property values square bracket access and exactOptionalPropertyTypes enabled has inconsistent behaviour**

*With exactOptionalPropertyTypes enabled, TypeScript inconsistently allows assigning undefined to optional properties using bracket access when the key is a union but errors when it's a single literal*

 * (3 years ago) **andrewbranch** added label `Bug`, and set milestone to `Backlog`
 * **RyanCavanaugh** added label `Domain: exactOptionalPropertyTypes`
 * [today](https://github.com/microsoft/TypeScript/issues/55526#issuecomment-5738043521) **RyanCavanaugh** explained that PR #54845 fixed dynamic writes under --strictNullChecks and --exactOptionalPropertyTypes and noted that TypeScript 6.0.3 now rejects them
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#55570](https://github.com/microsoft/TypeScript/issues/55570) (Closed, `Bug`, `Domain: Decorators`, `Rescheduled`, `Needs Human Review`, **rbuckton**)

**transpileModule does not elide type only "import equals" under emitDecoratorMetadata**

*TranspileModule with emitDecoratorMetadata and isolatedModules fails to elide type-only import equals, causing runtime errors.*

 * (2.5 years ago) **RyanCavanaugh** set milestones to `TypeScript 5.5.0`, `TypeScript 5.7.0`, and removed from milestone `TypeScript 5.5.0`
 * [today](https://github.com/microsoft/TypeScript/issues/55570#issuecomment-5737994369) **RyanCavanaugh** explained that transpileModule was part of the legacy pre-TypeScript-7 API and would not receive further updates, referencing issue #49450
 * **RyanCavanaugh** added label `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#55989](https://github.com/microsoft/TypeScript/pull/55989) (Open, `For Milestone Bug`, **navya9singh**)

**Update lib\.dom\.d\.ts: \`MutationObserverInit\.attributeFilter\` can accept an iterator**

*Update lib.dom.d.ts so that MutationObserverInit.attributeFilter accepts iterators in addition to arrays.*

 * **typescript-bot** added label `For Backlog Bug`
 * **sandersn** assigned to **navya9singh**
 * **RyanCavanaugh** added to milestone `Post-7.0 lib candidates`
 * (today) **typescript-automation[bot]** added label `For Milestone Bug`, and removed label `For Backlog Bug`

### [Issue microsoft/TypeScript#55990](https://github.com/microsoft/TypeScript/issues/55990) (Open, `Bug`, `Help Wanted`, `Domain: lib.d.ts`, `Needs Human Review`, **RyanCavanaugh**, **Copilot**)

**Update lib\.dom\.d\.ts: \`MutationObserverInit\.attributeFilter\` can accept an iterator**

*Update lib.dom.d.ts to allow MutationObserverInit.attributeFilter to accept string iterators such as Set keys.*

 * (2.9 years ago) **RyanCavanaugh** added labels `Help Wanted`, `Domain: lib.d.ts`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/55990#issuecomment-5738044512) **RyanCavanaugh** explained that MutationObserverInit.attributeFilter was declared as string[] but should accept iterables per spec
 * (today) **RyanCavanaugh** added label `Needs Human Review`, and assigned to **Copilot**, **RyanCavanaugh**

### [Issue microsoft/TypeScript#56024](https://github.com/microsoft/TypeScript/issues/56024) (Closed, `Bug`, `Fixed`, `Help Wanted`, `Domain: This-Typing`, `Needs Human Review`)

**\`this\` parameter not correctly inferred when unrelated type parameter has no inference candidates**

*An unrelated generic parameter without inference candidates prevents correct 'this' type inference in callbacks.*

 * (2.9 years ago) **RyanCavanaugh** added labels `Help Wanted`, `Domain: This-Typing`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/56024#issuecomment-5738086175) **RyanCavanaugh** described how the contextual `this` type was restored in the TypeScript language service and illustrated the difference between TS 5.2.2 and TS 7.1.0-dev in `f1`’s signature
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#56589](https://github.com/microsoft/TypeScript/issues/56589) (Open, `Bug`, `Help Wanted`, `Domain: lib.d.ts`, `Needs Human Review`, **RyanCavanaugh**, **Copilot**)

**MediaStream API should support pan, zoom and tilt**

*Extend TypeScript’s MediaTrackCapabilities and MediaTrackConstraints interfaces to include pan, tilt, and zoom properties for camera control.*

 * [2.8 years ago](https://github.com/microsoft/TypeScript/issues/56589#issuecomment-1832957890) **fatcerberus** asked if types automatically emerged as a new TypeScript feature
 * **RyanCavanaugh** added to milestone `Backlog`
 * [1.7 years ago](https://github.com/microsoft/TypeScript/issues/56589#issuecomment-2514423998) **ivancuric** noticed the issue for other advanced properties and provided a type augmentation workaround
 * [today](https://github.com/microsoft/TypeScript/issues/56589#issuecomment-5738136564) **RyanCavanaugh** reported missing zoom, pan, and tilt properties on MediaTrackCapabilities and MediaTrackConstraintSet causing TS2339 errors
 * (today) **RyanCavanaugh** added label `Needs Human Review`, and assigned to **Copilot**, **RyanCavanaugh**

### [Issue microsoft/TypeScript#56630](https://github.com/microsoft/TypeScript/issues/56630) (Closed, `Bug`, `Fixed`, `Domain: Declaration Emit`, `Needs Human Review`, **weswigham**)

**Declaration emit fails to import symbol on function auto\-property**

*TypeScript declaration emit fails to import a symbol used in a mixin auto-property, causing an undefined reference in .d.ts output.*

 * (2.7 years ago) **RyanCavanaugh** added labels `Bug`, `Domain: Declaration Emit`, and set milestone to `TypeScript 5.4.0`
 * [today](https://github.com/microsoft/TypeScript/issues/56630#issuecomment-5738124426) **RyanCavanaugh** reported that TypeScript 7.1.0-dev.20260918.1 emitted the declaration correctly as [mixin.sym]: boolean, whereas versions 4.3.2 and 6.0.3 still emitted the undeclared [sym]: boolean, but noted that the native declaration emitter now preserves the qualified function property
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#56669](https://github.com/microsoft/TypeScript/issues/56669) (Open, `Bug`, `Help Wanted`, `Domain: JSX/TSX`, `Needs Human Review`)

**Mirror cursor for JSX stops working in some case**

*JSX mirrored cursor editing stops duplicating edits after deleting and typing characters in a component tag*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [1.9 years ago](https://github.com/microsoft/TypeScript/issues/56669#issuecomment-2392530712) **iisaduan** described how parsing recovery no longer recognized JSX tags with props and noted that #57127 fixed the case without props
 * **RyanCavanaugh** added label `Domain: JSX/TSX`
 * **RyanCavanaugh** added label `Needs Human Review`

### [Issue microsoft/TypeScript#56696](https://github.com/microsoft/TypeScript/issues/56696) (Closed, `Bug`, `Help Wanted`, `Domain: JSX/TSX`, `Needs Human Review`)

** Ternary operator breaks syntax highlighting in tsx file**

*A ternary operator in a TSX file causes VS Code to lose syntax highlighting, tag closing, and indentation in the JSX*

 * (2.7 years ago) **RyanCavanaugh** added labels `Help Wanted`, `Domain: JSX/TSX`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/56696#issuecomment-5738144075) **RyanCavanaugh** clarified that the issue originated from VS Code TSX TextMate grammar/editor-tokenization rather than the TypeScript parser or language-service and referenced a related tracked issue
 * **RyanCavanaugh** added label `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#56766](https://github.com/microsoft/TypeScript/issues/56766) (Closed, `Bug`, `Help Wanted`, `Domain: check: Variance Relationships`, `Needs Human Review`)

**Functions with fewer parameters NOT assignable to functions with more parameters defined as tuples union**

*TypeScript rejects assigning a single-parameter function to a union-of-tuples parameter function type, despite allowing similar overloads and intersections.*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [2.6 years ago](https://github.com/microsoft/TypeScript/issues/56766#issuecomment-1879868493) **Andarist** said "Duplicate of https://github.com/microsoft/TypeScript/issues/48663"
 * **RyanCavanaugh** added label `Domain: Variance Relationships`
 * [today](https://github.com/microsoft/TypeScript/issues/56766#issuecomment-5738154388) **RyanCavanaugh** noted that the issue was already tracked by issue #48663 and explained that both reports concerned assigning a one-parameter function to a function type with a rest-parameter union of fixed-length tuples, causing a tuple-length incompatibility
 * **RyanCavanaugh** added label `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#56783](https://github.com/microsoft/TypeScript/issues/56783) (Closed, `Bug`, `Fixed`, `Domain: Declaration Emit`, `Needs Human Review`, **weswigham**)

**Exported const type parameters is not renamed in constraint in another const in type declarations**

*TypeScript’s .d.ts generator fails to rename type parameters in constraints for generic methods on exported constants.*

 * [2.7 years ago](https://github.com/microsoft/TypeScript/issues/56783#issuecomment-1857847094) **mcheshkov** said "Nightly on playground (v5.4.0-dev.20231215) generates broken typings as well: f(): void;"
 * [2.7 years ago](https://github.com/microsoft/TypeScript/issues/56783#issuecomment-1857855005) **mcheshkov** explained ts-proto’s use of a generic with a mapped type to enforce exact types by requiring extra properties to be never
 * **RyanCavanaugh** added label `Domain: Declaration Emit`
 * [today](https://github.com/microsoft/TypeScript/issues/56783#issuecomment-5738189415) **RyanCavanaugh** stated that the issue was fixed in TypeScript 5.5.0-dev.20240517 and later, and that the declaration emitter now preserves P2<{}, I> for Def.baz.f, referencing PR #58539
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#56855](https://github.com/microsoft/TypeScript/issues/56855) (Closed, `Bug`, `Fixed`, `Help Wanted`, `Domain: check: Type Inference`, `Needs Human Review`)

**Generic type inference failed**

*Including an unused default generic parameter in a TypeScript function with ThisType causes the 'context' type to be inferred as unknown.*

 * [2.7 years ago](https://github.com/microsoft/TypeScript/issues/56855#issuecomment-1877392927) **jfet97** explained that the if condition inside instantiateContextualType was too eager, causing unintended default type instantiations and suggested two alternative condition changes that fix the issue but produce failing baselines
 * **RyanCavanaugh** added label `Domain: Type Inference`
 * [14 weeks ago](https://github.com/microsoft/TypeScript/issues/56855#issuecomment-4651613385) **mkantor** stated that TypeScript 6.0 fixed the issue, linked a play example showing correct inference, and suggested that PR #62243 resolved it
 * [today](https://github.com/microsoft/TypeScript/issues/56855#issuecomment-5738174080) **RyanCavanaugh** stated that the issue was fixed by PR #62243 and was resolved from version 6.0.0-dev.20251211 onward
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#56962](https://github.com/microsoft/TypeScript/issues/56962) (Open, `Bug`, `Help Wanted`, `Domain: lib.d.ts`, `Needs Human Review`, **RyanCavanaugh**, **Copilot**)

**Typings for navigator\.connection gone since TS 4\.8**

*navigator.connection type definitions disappeared after upgrading to TypeScript 4.8 and are absent in TS 5.3.*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [2.6 years ago](https://github.com/microsoft/TypeScript/issues/56962#issuecomment-1879478829) **fatcerberus** said "MDN says this is only supported by Chromium-based browsers."
 * [2.6 years ago](https://github.com/microsoft/TypeScript/issues/56962#issuecomment-1881754792) **RyanCavanaugh** recommended revisiting the "two browser support" policy in light of Firefox losing share, Opera adopting Chromium, and Safari lagging behind standards
 * [today](https://github.com/microsoft/TypeScript/issues/56962#issuecomment-5738200921) **RyanCavanaugh** reported that navigator.connection was missing from the DOM declarations, causing TS2339 errors in TypeScript 5.3.3 and the native compiler with --lib es5,dom despite MDN documenting the property and TypeScript 4.5.5 accepting it
 * (today) **RyanCavanaugh** added label `Needs Human Review`, and assigned to **Copilot**, **RyanCavanaugh**

### [Issue microsoft/TypeScript#57514](https://github.com/microsoft/TypeScript/issues/57514) (Open, `Bug`, `Help Wanted`, `Domain: lib.d.ts`, `Needs Human Review`, **RyanCavanaugh**, **Copilot**)

**Intl\.NumberFormat does not model required properties when \`style\` is set to \`currency\`**

*Intl.NumberFormat type definitions do not enforce required currency property when style is set to currency, leading to runtime errors.*

 * (2.5 years ago) **RyanCavanaugh** added label `Domain: lib.d.ts`, and set milestone to `Backlog`
 * [2.4 years ago](https://github.com/microsoft/TypeScript/issues/57514#issuecomment-2032586684) **Renegade334** pointed out that style 'unit' also requires dependent properties and argued that implementing complex union types for future extensibility would compromise simplicity and that lib.d.ts need not guard against every TypeError
 * [today](https://github.com/microsoft/TypeScript/issues/57514#issuecomment-5738238685) **RyanCavanaugh** described that Intl.NumberFormat allowed undefined currency under --strict in TypeScript but caused a runtime error in the browser and suggested modeling required option relationships for currency and unit styles
 * (today) **RyanCavanaugh** added label `Needs Human Review`, and assigned to **Copilot**, **RyanCavanaugh**

### [Issue microsoft/TypeScript#57520](https://github.com/microsoft/TypeScript/issues/57520) (Open, `Bug`, `Help Wanted`, `Domain: lib.d.ts`, `Needs Human Review`, **RyanCavanaugh**, **Copilot**)

**Change type of \`File\` constructor parameter \`fileBits\` to \`Iterable\<BlobPart\>\`**

*Change the File constructor’s fileBits parameter type to Iterable<BlobPart> for accurate DOM typings*

 * (2.5 years ago) **RyanCavanaugh** added labels `Help Wanted`, `Domain: lib.d.ts`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/57520#issuecomment-5738246689) **RyanCavanaugh** described that File() accepts an iterable of BlobPart but TypeScript's DOM declaration incorrectly requires a BlobPart[] and suggested FileConstructor accept Iterable<BlobPart>.
 * (today) **RyanCavanaugh** added label `Needs Human Review`, and assigned to **Copilot**, **RyanCavanaugh**

### [Issue microsoft/TypeScript#57564](https://github.com/microsoft/TypeScript/issues/57564) (Open, `Bug`, `Needs More Info`, `Has Repro`, `Domain: Something Else`, `Needs Human Review`)

**Error not issued when global type is an alias of an object type literal**

*Custom global Array<T> alias as object literal prevents expected type errors for T[] satisfy checks.*

 * [2.5 years ago](https://github.com/microsoft/TypeScript/issues/57564#issuecomment-1967663389) **RyanCavanaugh** noted that adding PromiseConstructorLike created an unintentional dependency causing type aliases not to be flagged and suggested advising users to avoid this usage
 * [2.5 years ago](https://github.com/microsoft/TypeScript/issues/57564#issuecomment-1968434979) **typescript-bot** posted repro bot output showing TS5107 deprecation error for moduleResolution=node10 and reproduction failures across multiple TypeScript versions
 * **RyanCavanaugh** added label `Domain: Something Else`
 * [today](https://github.com/microsoft/TypeScript/issues/57564#issuecomment-5738271447) **RyanCavanaugh** verified the global-Array validation error appears with TS 5.5.0-dev and asked for the exact Workbench configuration or file setup that reproduced the missing diagnostic
 * (today) **RyanCavanaugh** added labels `Needs Human Review`, `Needs More Info`
 * [later](https://github.com/microsoft/TypeScript/issues/57564#issuecomment-5742046277) **rotu** asked where TS2317 was appearing in the Workbench linked in the writeup

### [Issue microsoft/TypeScript#57985](https://github.com/microsoft/TypeScript/issues/57985) (Closed, `Bug`, `Fixed`, `Help Wanted`, `Domain: Binder`, `Needs Human Review`)

**No duplicate identifier error issued if \`const\` declared with function type with expandos**

*A const declared with a function type including expandos fails to trigger duplicate identifier errors on later declarations.*

 * [2.4 years ago](https://github.com/microsoft/TypeScript/issues/57985#issuecomment-2027160918) **rishikeshmmf** demonstrated that assigning a function to Describable resulted in an undefined desc property, concatenating '...more' yielded 'undefined...more', and that f cannot be redeclared
 * [2.3 years ago](https://github.com/microsoft/TypeScript/issues/57985#issuecomment-2083222957) **Andarist** described that the expando adds SymbolFlags.Assignment and that the binder allows assignment declarations to merge with variables regardless of flags
 * **RyanCavanaugh** added label `Domain: Binder`
 * [today](https://github.com/microsoft/TypeScript/issues/57985#issuecomment-5738282045) **RyanCavanaugh** reported that TypeScript 7.1.0-dev.20260918.1 throws TS2451 for both const f declarations after an expando assignment while TypeScript 5.4.3 and classic 6.0.3 did not, and noted that the no-expando form still reports TS2451, restoring the expected check
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#58020](https://github.com/microsoft/TypeScript/issues/58020) (Closed, `Bug`, `Domain: API: Transforms`, `Needs Human Review`, **rbuckton**)

**“Lexical environment is not suspended” when visitEachChile**

*visitEachChild on a function returning an object type with a getter crashes due to 'Lexical environment is suspended' assertion*

 * [1 year ago](https://github.com/microsoft/TypeScript/issues/58020#issuecomment-3175064612) **allangaldinosilva** said "@kalinowskitomasz did you find a solution for this?"
 * [1 year ago](https://github.com/microsoft/TypeScript/issues/58020#issuecomment-3276774731) **TechQuery** mentioned that a downstream package encountered the same Debug Failure error and provided the related bug issue reference and a temporary fix commit
 * **RyanCavanaugh** added label `Domain: Transforms`
 * [today](https://github.com/microsoft/TypeScript/issues/58020#issuecomment-5738282237) **RyanCavanaugh** explained that the crash occurred in the superseded pre-TypeScript-7 JS transformer API and thus cannot be addressed there
 * **RyanCavanaugh** added label `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#58026](https://github.com/microsoft/TypeScript/issues/58026) (Closed, `Bug`, `Fixed`, `Help Wanted`, `Domain: lib.d.ts`, `Needs Human Review`)

**Missing the \`AbortSignal\.any\(\)\` function**

*The dom.d.ts file lacks the AbortSignal.any static method definition added in the TypeScript-DOM-lib-generator.*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [2.3 years ago](https://github.com/microsoft/TypeScript/issues/58026#issuecomment-2104322998) **Teamop** said "looks like done in https://github.com/microsoft/TypeScript/pull/58211, and released in 5.5.0-beta"
 * [1.7 years ago](https://github.com/microsoft/TypeScript/issues/58026#issuecomment-2521632914) **MartinJohns** notified that the issue could be closed and referenced issue #60695
 * [today](https://github.com/microsoft/TypeScript/issues/58026#issuecomment-5738287381) **RyanCavanaugh** noted that AbortSignal.any was added by PR #58211 and that AbortSignal.any([]) reported TS2339 in 5.4.5 but compiled cleanly in 5.5.0-beta, 6.0.3, and current native TypeScript
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#58027](https://github.com/microsoft/TypeScript/issues/58027) (Closed, `Bug`, `Fixed`, `Help Wanted`, `Domain: Crashes`, `Needs Human Review`)

**Debug Failure\. Did not expect ObjectLiteralExpression to have an Identifier in its trivia**

*Hovering over an object literal property with a Unicode key crashes the TypeScript server when targeting ES5*

 * [2.4 years ago](https://github.com/microsoft/TypeScript/issues/58027#issuecomment-2033359445) **fatcerberus** said "I thought \u{1D504} was ES6+ syntax and doesn't work in ES5.  Am I misremembering?"
 * [2.4 years ago](https://github.com/microsoft/TypeScript/issues/58027#issuecomment-2033378610) **jakebailey** said "Could be, I'm no historian 😅"
 * **RyanCavanaugh** added label `Domain: Crashes`
 * [today](https://github.com/microsoft/TypeScript/issues/58027#issuecomment-5738290621) **RyanCavanaugh** fixed the issue in current native TypeScript and noted that TS 5.5.0-dev crashed on hovering `𝔄` whereas TS 7.1.0-dev returned the correct type
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#58209](https://github.com/microsoft/TypeScript/issues/58209) (Closed, `Bug`, `Fixed`, `Help Wanted`, `Domain: JS Emit`, `Needs Human Review`)

**\`const enum\` references in the body of nodes with grammar errors are not inlined**

*Const enum references in code with grammar errors are not inlined, resulting in broken runtime output.*

 * (2.4 years ago) **RyanCavanaugh** added labels `Help Wanted`, `Domain: JS Emit`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/58209#issuecomment-5738329286) **RyanCavanaugh** mentioned that PR #58364 fixed the issue and reported differing inlining behaviors across TypeScript versions
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#58322](https://github.com/microsoft/TypeScript/issues/58322) (Open, `Bug`, `Needs More Info`, `Help Wanted`, `Domain: JSX/TSX`, `Needs Human Review`)

**Auto\-closing of tags within curly braces \`{}\` does not work when parent element is same tag in JSX**

*HTML tags opened inside JSX curly braces aren’t auto-closed when the parent element uses the same tag.*

 * (2.4 years ago) **RyanCavanaugh** added labels `Help Wanted`, `Domain: JSX/TSX`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/58322#issuecomment-5738304573) **RyanCavanaugh** requested the editor host and version that performs the auto-closing action, plus the relevant JSX auto-closing setting and exact keystrokes
 * (today) **RyanCavanaugh** added labels `Needs Human Review`, `Needs More Info`

### [Issue microsoft/TypeScript#58334](https://github.com/microsoft/TypeScript/issues/58334) (Closed, `Bug`, `Fixed`, `Help Wanted`, `Domain: flag: isolatedDeclarations`, `Needs Human Review`)

**\`\-\-isolatedDeclarations\` allows generator functions**

*Generator functions are improperly permitted under --isolatedDeclarations, producing inference-dependent declaration output instead of being disallowed.*

 * (2.4 years ago) **RyanCavanaugh** added labels `Help Wanted`, `Domain: Isolated Declarations`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/58334#issuecomment-5738335852) **RyanCavanaugh** reported that the issue was fixed with --isolatedDeclarations now reporting TS9007 and noted the behavior change between dev builds and inclusion in PR #58628
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#58534](https://github.com/microsoft/TypeScript/issues/58534) (Closed, `Bug`, `Fixed`, `Help Wanted`, `Domain: Node ESM`, `Needs Human Review`)

**Error: Debug Failure when importing \`AssertionError\` from \`node:assert/strict\`**

*TypeScript 5.4.5 crashes with a Debug Failure when importing AssertionError from 'node:assert/strict' under NodeNext module settings.*

 * [1.8 years ago](https://github.com/microsoft/TypeScript/issues/58534#issuecomment-2459439619) **bmenant** offered a workaround using assert.AssertionError and described encountering a tsc Debug Failure when running tests with borp after porting to ESM
 * [1.5 years ago](https://github.com/microsoft/TypeScript/issues/58534#issuecomment-2645958498) **LukeAbby** provided a minimal reproduction with code snippets and noted that the compiler crash persisted but his fix would prevent it in the original package
 * **RyanCavanaugh** added label `Domain: Node ESM`
 * [today](https://github.com/microsoft/TypeScript/issues/58534#issuecomment-5738345839) **RyanCavanaugh** stated that current implementations fixed the crash when hovering AssertionError, observed that TypeScript 5.4.5 crashed while 6.0.3 and the native language service succeeded, and noted that the linked proposal was closed unmerged and thus not credited as the fix
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#58614](https://github.com/microsoft/TypeScript/issues/58614) (Closed, `Bug`, `Help Wanted`, `Domain: Something Else`, `Needs Human Review`)

**TypeScript colorizer confused by comments after colon in class member function signature with Generic return type**

*TypeScript syntax highlighting miscolors class methods with comments placed after the colon before generic return types.*

 * (2.2 years ago) **RyanCavanaugh** added labels `Help Wanted`, `Domain: Something Else`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/58614#issuecomment-5738364194) **RyanCavanaugh** identified the issue as a syntax-coloring problem in the VS Code TextMate grammar and suggested filing it upstream in microsoft/TypeScript-TmLanguage
 * **RyanCavanaugh** added label `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#58644](https://github.com/microsoft/TypeScript/issues/58644) (Open, `Bug`, `Help Wanted`, `Domain: lib.d.ts`, `Needs Human Review`, **RyanCavanaugh**, **Copilot**)

**TS 5\.4\.5: Return type for performance\.getEntriesByType is inaccurate**

*The return type of performance.getEntriesByType is overly generic PerformanceEntry[], preventing access to subclass-specific properties for known entry types.*

 * [2.2 years ago](https://github.com/microsoft/TypeScript/issues/58644#issuecomment-2200739905) **heysujal** questioned what changes they needed to make at a specific line in lib.d.ts
 * [2.2 years ago](https://github.com/microsoft/TypeScript/issues/58644#issuecomment-2200759476) **lll000111** suggested using TypeScript function signature overloads with one overload per entryType string, linked to documentation and a playground demo, and noted the need to define interfaces and inheritance updates
 * [2.1 years ago](https://github.com/microsoft/TypeScript/issues/58644#issuecomment-2245948223) **fahmij8** said "Temporarily I just do entry as PerformanceNavigationTiming"
 * [today](https://github.com/microsoft/TypeScript/issues/58644#issuecomment-5738360075) **RyanCavanaugh** noted that getEntriesByType("navigation") was typed as PerformanceEntry[] causing TS2339 on entry.type and suggested updating the DOM declaration to preserve the literal "navigation" result type
 * (today) **RyanCavanaugh** added label `Needs Human Review`, and assigned to **Copilot**, **RyanCavanaugh**

### [Issue microsoft/TypeScript#58695](https://github.com/microsoft/TypeScript/issues/58695) (Open, `Bug`, `Needs More Info`, `Help Wanted`, `Domain: lib.d.ts`, `Needs Human Review`)

**texSubImage2D missing WebGL2 syntax**

*WebGL2 texSubImage2D type definitions in TypeScript lack an overload for ImageBitmap, causing type errors.*

 * (2.2 years ago) **RyanCavanaugh** added labels `Help Wanted`, `Domain: lib.d.ts`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/58695#issuecomment-5738369349) **RyanCavanaugh** noted that the nine-argument ImageBitmap call compiles with WebGL2RenderingContext but errors with WebGLRenderingContext and asked for the gl declaration, TypeScript version, and compiler options to reproduce the issue
 * (today) **RyanCavanaugh** added labels `Needs Human Review`, `Needs More Info`

### [Issue microsoft/TypeScript#59012](https://github.com/microsoft/TypeScript/issues/59012) (Open, `Bug`, `Help Wanted`, `Domain: lib.d.ts`, `Needs Human Review`, **RyanCavanaugh**, **Copilot**)

**Consider making \`WritableStreamDefaultWriter\.write\(\)\` contravariant**

*Propose making WritableStreamDefaultWriter.write contravariant to enforce correct chunk type compatibility and catch mismatches.*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [1.7 years ago](https://github.com/microsoft/TypeScript/issues/59012#issuecomment-2567129729) **steabert** asked whether bivariance was the underlying issue allowing piping streams with mismatching types
 * **RyanCavanaugh** added label `Domain: lib.d.ts`
 * [today](https://github.com/microsoft/TypeScript/issues/59012#issuecomment-5738397779) **RyanCavanaugh** described that WritableStream remained bivariant under --strict allowing invalid assignments without errors
 * (today) **RyanCavanaugh** added label `Needs Human Review`, and assigned to **Copilot**, **RyanCavanaugh**

### [Issue microsoft/TypeScript#59047](https://github.com/microsoft/TypeScript/issues/59047) (Open, `Bug`, `Needs More Info`, `Domain: Crashes`, `Needs Human Review`, **iisaduan**)

**TS Server fatal error:  Maximum call stack size exceeded**

*TS Server crashes with maximum call stack size exceeded error when opening a file containing syntax errors in VS Code*

 * (2.1 years ago) **RyanCavanaugh** added labels `Bug`, `Domain: Crashes`, and set milestone to `TypeScript 5.6.0`
 * [today](https://github.com/microsoft/TypeScript/issues/59047#issuecomment-5738321489) **RyanCavanaugh** requested that the user attach efront.js and verbose tsserver logs to reproduce the crash
 * (today) **RyanCavanaugh** added labels `Needs Human Review`, `Needs More Info`

### [Issue microsoft/TypeScript#59161](https://github.com/microsoft/TypeScript/issues/59161) (Closed, `Bug`, `Domain: This-Typing`, `Needs Human Review`, **rbuckton**)

**Naked generic type returned from iterator method**

*Generic static generator iterator methods fail to infer the subclass type, returning the uninstantiated type parameter T rather than Child.*

 * **RyanCavanaugh** added to milestone `TypeScript 5.6.0`
 * [1.8 years ago](https://github.com/microsoft/TypeScript/issues/59161#issuecomment-2454892507) **reverofevil** said "@rbuckton Any news on this?"
 * **RyanCavanaugh** added label `Domain: This-Typing`
 * [today](https://github.com/microsoft/TypeScript/issues/59161#issuecomment-5738404941) **RyanCavanaugh** marked the issue as duplicate of #38388 and noted that implicit Symbol.iterator calls by spread or for...of did not instantiate the iterator method's generic this parameter, allowing the type parameter to leak into the element type
 * **RyanCavanaugh** added label `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#59255](https://github.com/microsoft/TypeScript/issues/59255) (Closed, `Bug`, `Domain: Crashes`, `Needs Human Review`, **weswigham**)

**RangeError: Maximum call stack size in getTypeAtLocation in files importing in series with template literals**

*A RangeError maximum call stack size exceeded occurs when linting a long chain of TypeScript modules importing via template literals.*

 * [2 years ago](https://github.com/microsoft/TypeScript/issues/59255#issuecomment-2287050971) **JoshuaKGoldberg** clarified that getTypeAtLocation() overflows regardless of which API is used
 * [2 years ago](https://github.com/microsoft/TypeScript/issues/59255#issuecomment-2287213749) **weswigham** explained that the checker depended on the callstack to track state and suggested ordering getTypeAtLocation calls on leaf node files as a workaround
 * **RyanCavanaugh** added label `Domain: Crashes`
 * [today](https://github.com/microsoft/TypeScript/issues/59255#issuecomment-5738413082) **RyanCavanaugh** explained that getTypeAtLocation belonged to the pre-TypeScript-7 JavaScript Compiler API, is no longer developed, and that the stack overflow arose from recursive import chain checks, with template literals only facilitating the overflow
 * **RyanCavanaugh** added label `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#59401](https://github.com/microsoft/TypeScript/issues/59401) (Open, `Bug`, `Needs More Info`, `Domain: check: Error Instability`, `Needs Human Review`, **gabritto**)

**\`'X' only refers to a type\` error in JSDoc comments**

*Transient “only refers to a type” errors occur when editing JSDoc @link comments, disappearing after subsequent edits*

 * (2 years ago) **RyanCavanaugh** added label `Domain: Error Instability`, set milestone to `TypeScript 5.7.0`, and removed from milestone `TypeScript 5.6.1`
 * [today](https://github.com/microsoft/TypeScript/issues/59401#issuecomment-5738424550) **RyanCavanaugh** requested a self-contained reproduction with source code and tsserver logs covering the diagnostic appearance and disappearance
 * (today) **RyanCavanaugh** added labels `Needs Human Review`, `Needs More Info`

### [Issue microsoft/TypeScript#59679](https://github.com/microsoft/TypeScript/issues/59679) (Closed, `Bug`, `Help Wanted`, `Domain: JSDoc`, `Needs Human Review`)

**\`getTextOfJSDocComment\` introduces a space in JSDoc comments**

*getTextOfJSDocComment incorrectly adds spaces inside JSDoc inline tags, turning {@link entry()} into {@link entry ()}.*

 * (2 years ago) **RyanCavanaugh** added labels `Help Wanted`, `Domain: JSDoc`
 * [2 years ago](https://github.com/microsoft/TypeScript/issues/59679#issuecomment-2297192533) **a-tarasyuk** asked whether to add special nodes to the parser or handle known cases directly in the formatter
 * [today](https://github.com/microsoft/TypeScript/issues/59679#issuecomment-5738433357) **RyanCavanaugh** said "getTextOfJSDocComment is part of the pre-TypeScript-7 JavaScript Compiler API. That API has been superseded and is no longer being developed, so this formatting behavior will not be changed."
 * **RyanCavanaugh** added label `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#59968](https://github.com/microsoft/TypeScript/issues/59968) (Open, `Bug`, `Help Wanted`, `Domain: lib.d.ts`, `Needs Human Review`, **RyanCavanaugh**, **Copilot**)

**Error when accessing CSS property value using kebab case in \`CSSStyleDeclaration\` object**

*TypeScript errors when accessing kebab-case CSS properties on CSSStyleDeclaration because dash-separated properties lack typings.*

 * (2 years ago) **RyanCavanaugh** added labels `Help Wanted`, `Domain: lib.d.ts`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/59968#issuecomment-5738506467) **RyanCavanaugh** described that CSSStyleDeclaration supports dashed CSS property lookups at runtime but reports TS7015 under --noImplicitAny in multiple TypeScript versions, noted that Edge accepts this lookup and referred to DOM lib generator issue 1672
 * (today) **RyanCavanaugh** added label `Needs Human Review`, and assigned to **Copilot**, **RyanCavanaugh**

### [Issue microsoft/TypeScript#60247](https://github.com/microsoft/TypeScript/issues/60247) (Closed, `Bug`, `Fixed`, `Help Wanted`, `Domain: Declaration Emit`, `Needs Human Review`)

**Mapped type with enum keys emits string keys in d\.ts type, but uses enum keys in \.ts type**

*Mapped types with enum keys produce correct enum-keyed TS types but emit string-keyed declarations, causing type mismatches.*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [1.2 years ago](https://github.com/microsoft/TypeScript/issues/60247#issuecomment-2964790098) **bradzacher** provided another repro with a TS Playground link and a code example demonstrating how Omit behaves differently in the IDE versus the .d.ts output
 * **RyanCavanaugh** added label `Domain: Declaration Emit`
 * [today](https://github.com/microsoft/TypeScript/issues/60247#issuecomment-5738585693) **RyanCavanaugh** explained that PR #61211 resolved the issue and that the fix is available in TypeScript 6.0.0-dev.20251031, 6.0.3, and the current native compiler
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#60343](https://github.com/microsoft/TypeScript/issues/60343) (Closed, `Bug`, `Fixed`, `Domain: JSX/TSX`, `Needs Human Review`)

**Inline conditional JSX props spread warns as if unconditional**

*Inline conditional JSX prop spreads incorrectly warn that they always overwrite earlier props, unlike similar object spreads.*

 * (1.8 years ago) **RyanCavanaugh** added labels `Bug`, `Domain: JSX/TSX`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/60343#issuecomment-5738638693) **RyanCavanaugh** stated that the issue was fixed by PR #62656 and that newer TypeScript versions no longer report TS2783 for inline conditional JSX spread
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#60386](https://github.com/microsoft/TypeScript/issues/60386) (Closed, `Bug`, `Help Wanted`, `Domain: check: Excess Property Checking`, `Needs Human Review`)

**Destructuring into an empty object vs an object with existing properties yields different results**

*Spreading a Record<string,string> into a Record<string,number> produces a type error only when the target object has no other properties*

 * [1.8 years ago](https://github.com/microsoft/TypeScript/issues/60386#issuecomment-2451038533) **Andarist** noted that the reported code closely matched previously reported issues and referenced an earlier fix attempt
 * [1.2 years ago](https://github.com/microsoft/TypeScript/issues/60386#issuecomment-2958988115) **zanminkian** said "I am facing the same issue. This bug makes spread operator not type-safe."
 * **RyanCavanaugh** added label `Domain: Excess Property Checking`
 * [today](https://github.com/microsoft/TypeScript/issues/60386#issuecomment-5738595007) **RyanCavanaugh** identified that adding an explicit property to an object literal causes a spread Record<string, V> to escape checking against the target Record<string, U>, mirroring the index-signature spread issue tracked in issue #56431
 * **RyanCavanaugh** added label `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#60514](https://github.com/microsoft/TypeScript/issues/60514) (Closed, `Bug`, `Help Wanted`, `Domain: check: Control Flow`, `Needs Human Review`)

**Weird behaviour with an "evolving any" and a non\-null assertion operator**

*Assigning a number|undefined to an evolving any variable, the non-null assertion operator fails to remove undefined unlike an explicit type assertion.*

 * [1.8 years ago](https://github.com/microsoft/TypeScript/issues/60514#issuecomment-2481197590) **bradzacher** described how TS returns a plain number type for Identifier in a NonNullExpression versus a union type for Identifier in an AsExpression and noted this is observable in the TS API or via ts-ast-viewer
 * [1.8 years ago](https://github.com/microsoft/TypeScript/issues/60514#issuecomment-2481213015) **bgenia** explained that checkIdentifier applies getNonNullableType when the type is automatic and the parent node is a non-null assertion, causing type queries to return non-nullable types, and noted this was introduced in #50092
 * **RyanCavanaugh** added label `Domain: Control Flow`
 * [today](https://github.com/microsoft/TypeScript/issues/60514#issuecomment-5738623567) **RyanCavanaugh** explained that the behavior still occurred in the classic Compiler API and that the API is deprecated with no changes planned
 * **RyanCavanaugh** added label `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#60546](https://github.com/microsoft/TypeScript/issues/60546) (Open, `Bug`, `Help Wanted`, `Domain: lib.d.ts`, `Needs Human Review`, **RyanCavanaugh**, **Copilot**)

**MIDIMessageEvent data is incorrectly typed**

*MIDIMessageEvent.data was mistakenly typed as Uint8Array|null in a recent PR, triggering unwarranted null warnings even though it always returns a Uint8Array.*

 * (1.8 years ago) **RyanCavanaugh** added labels `Help Wanted`, `Domain: lib.d.ts`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/60546#issuecomment-5738638920) **RyanCavanaugh** pointed out that MIDIMessageEvent.data was declared as Uint8Array|null causing a TS18047 error under strict, and recommended updating the generated DOM declaration to match the spec’s non-null definition
 * (today) **RyanCavanaugh** added label `Needs Human Review`, and assigned to **Copilot**, **RyanCavanaugh**

### [Issue microsoft/TypeScript#60756](https://github.com/microsoft/TypeScript/issues/60756) (Open, `Bug`, `Needs More Info`, `Domain: Module Resolution`, `Needs Human Review`)

**Typescript gets confused when renaming by only changing filename case of imported file on Windows**

*TypeScript on Windows fails to recognize case-only filename changes in imports, causing module not found errors.*

 * (1.7 years ago) **RyanCavanaugh** added labels `Bug`, `Domain: Module Resolution`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/60756#issuecomment-5738654712) **RyanCavanaugh** explained that the example used a side-effect import causing TS2304, suggested using a default import, and requested a self-contained repo with reproduction steps, TS version, and editor/tsc command to reproduce the casing diagnostic
 * (today) **RyanCavanaugh** added labels `Needs Human Review`, `Needs More Info`
 * [later](https://github.com/microsoft/TypeScript/issues/60756#issuecomment-5740721604) **M393** described how opening the project in VSCode on Windows showed a casing error for vector.js imported as Vector.js that persisted after renaming the file and attached a test repository

### [Issue microsoft/TypeScript#60764](https://github.com/microsoft/TypeScript/issues/60764) (Closed, `Bug`, `Help Wanted`, `Domain: Conditional Types`, `Needs Human Review`)

**Bug: string is not a string**

*A nested template-literal conditional type misclassifies a string as false, causing a 'true' to 'false' assignment error.*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [1.1 years ago](https://github.com/microsoft/TypeScript/issues/60764#issuecomment-3077138160) **KisaragiEffective** suggested a workaround by unquoting T and included a TypeScript code example
 * **RyanCavanaugh** added label `Domain: Conditional Types`
 * [today](https://github.com/microsoft/TypeScript/issues/60764#issuecomment-5738658956) **RyanCavanaugh** referenced a premature generic conditional-type evaluation tracked in issue #57650, explained that wrapping the type parameter in a template-literal type caused the outer conditional to resolve first making StringIsAString<'s'> false, and noted tracking at #57650
 * **RyanCavanaugh** added label `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#60773](https://github.com/microsoft/TypeScript/issues/60773) (Closed, `Bug`, `Help Wanted`, `Domain: Parser`, `Needs Human Review`)

**The parsed identifier is incomplete due to updateSourceFile\.**

*updateSourceFile method fails to include local variables a and newLocal in the parsed identifier set.*

 * (1.7 years ago) **RyanCavanaugh** added labels `Help Wanted`, `Domain: Parser`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/60773#issuecomment-5738656262) **RyanCavanaugh** said "updateSourceFile is part of the pre-TypeScript-7 Compiler API, which is no longer being developed. Changes to its incremental identifier bookkeeping are therefore not planned."
 * **RyanCavanaugh** added label `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#60838](https://github.com/microsoft/TypeScript/issues/60838) (Open, `Bug`, `Help Wanted`, `Domain: lib.d.ts`, `Needs Human Review`, **RyanCavanaugh**, **Copilot**)

**Inconsistent types between Document scrollingElement and documentElement**

*document.scrollingElement is typed as Element | null but should use the same HTMLElement | null type as document.documentElement*

 * (1.6 years ago) **RyanCavanaugh** added labels `Help Wanted`, `Domain: lib.d.ts`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/60838#issuecomment-5738670878) **RyanCavanaugh** highlighted that document.scrollingElement was declared as Element|null causing a TS2322 assignment error when assigning it to HTMLElement|null
 * (today) **RyanCavanaugh** added label `Needs Human Review`, and assigned to **Copilot**, **RyanCavanaugh**

### [Issue microsoft/TypeScript#60879](https://github.com/microsoft/TypeScript/issues/60879) (Closed, `Bug`, `Fixed`, `Help Wanted`, `Domain: JS Emit`, `Needs Human Review`)

**static block on unnamed class produces invalid javascript**

*A static block in an unnamed default-exported class causes TypeScript to emit invalid JavaScript referencing an undefined default_1*

 * (1.7 years ago) **RyanCavanaugh** added labels `Help Wanted`, `Domain: JS Emit`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/60879#issuecomment-5738684586) **RyanCavanaugh** observed that TypeScript 7.1.0-dev emitted a named default_1 class for export default class static-block cases making references valid, but TypeScript 6.0.3 still emitted invalid references to an undeclared default_1
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#60908](https://github.com/microsoft/TypeScript/issues/60908) (Closed, `Bug`, `Fixed`, `Help Wanted`, `Domain: JSDoc`, `Needs Human Review`)

**Unexpected "'Type' is declared but its value is never read\." error with jsdoc @import syntax**

*JSDoc @import type causes TS6133 'declared but its value is never read' error despite using the type in @type annotation.*

 * (1.4 years ago) **jakebailey** reopened the issue
 * **RyanCavanaugh** added label `Domain: JSDoc`
 * **jakebailey** removed label `Fix Available`
 * [today](https://github.com/microsoft/TypeScript/issues/60908#issuecomment-5738699580) **RyanCavanaugh** confirmed the issue was fixed in nightly 5.9.0-dev.20250318 and later by PR #60921 when using nodenext modules with allowJs, checkJs, and noUnusedLocals
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#60918](https://github.com/microsoft/TypeScript/issues/60918) (Closed, `Bug`, `Help Wanted`, `Domain: API`, `Needs Human Review`)

**The \`parseJsonConfigFileContent\` function does not resolve relative JSON paths**

*parseJsonConfigFileContent fails to resolve JSON files in include when provided a relative tsconfig directory*

 * (1.6 years ago) **RyanCavanaugh** added labels `Help Wanted`, `API`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/60918#issuecomment-5738683530) **RyanCavanaugh** clarified that parseJsonConfigFileContent is part of the pre-TypeScript-7 API and that no changes to its relative-path handling are planned
 * **RyanCavanaugh** added label `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#61110](https://github.com/microsoft/TypeScript/issues/61110) (Open, `Bug`, `Needs More Info`, `Domain: check: Type Circularity`, `Needs Human Review`, **weswigham**)

**RangeError \- Maximum call stack size exceeded \- in tsserver / vscode extension host \- when providing type args to fn lambda**

*Generic function type arguments across workspace packages cause tsserver in VSCode extension host to exceed maximum call stack size.*

 * (1.6 years ago) **RyanCavanaugh** added labels `Bug`, `Domain: Type Circularity`, and set milestone to `TypeScript 5.9.0`
 * [today](https://github.com/microsoft/TypeScript/issues/61110#issuecomment-5738713777) **RyanCavanaugh** asked for exact VS Code version, TypeScript extension/server version, precise completion position or editor action, and a tsserver log to reproduce the error
 * (today) **RyanCavanaugh** added labels `Needs Human Review`, `Needs More Info`

### [Issue microsoft/TypeScript#61209](https://github.com/microsoft/TypeScript/issues/61209) (Closed, `Bug`, `Fixed`, `Help Wanted`, `Domain: lib.d.ts`, `Needs Human Review`)

**\`IDBObjectStore\` \`keyPath\` missing \`null\` type\.**

*TypeScript’s IDBObjectStore.keyPath property type incorrectly omits null despite the IndexedDB specification allowing keyPath to be null.*

 * (1.5 years ago) **RyanCavanaugh** added labels `Help Wanted`, `Domain: lib.d.ts`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/61209#issuecomment-5738735838) **RyanCavanaugh** noted that the issue was fixed by PR 61647 and that IDBObjectStore.keyPath type and assignment behavior is now correct in specified versions
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#61292](https://github.com/microsoft/TypeScript/issues/61292) (Open, `Bug`, `Needs More Info`, `Help Wanted`, `Domain: Node ESM`, `Needs Human Review`)

**strange interaction with \`resolveJsonModule\`, \`createRequire\`, naming it \`require\`, and requiring JSON**

*Naming createRequire's result require in a NodeNext ES module with resolveJsonModule enabled triggers TS errors on JSON imports.*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [1.5 years ago](https://github.com/microsoft/TypeScript/issues/61292#issuecomment-2691816799) **ljharb** said "yup, it's an mjs file (but presumably a .js file in a type module package would behave the same) - iow, it's native ESM."
 * **RyanCavanaugh** added label `Domain: Node ESM`
 * [today](https://github.com/microsoft/TypeScript/issues/61292#issuecomment-5738759610) **RyanCavanaugh** requested the @ljharb/tsconfig version and tsc --showConfig output along with diagnostic output to reproduce the issue
 * (today) **RyanCavanaugh** added labels `Needs Human Review`, `Needs More Info`

### [Issue microsoft/TypeScript#61314](https://github.com/microsoft/TypeScript/issues/61314) (Closed, `Bug`, `Domain: LS: Suggestion Diagnostics`, `7.0 LS Migration`, `Needs Human Review`, **sandersn**)

**checker\.getSuggestionDiagnostics fails with \`TypeError: Cannot read properties of undefined \(reading 'parent'\)\`**

*checker.getSuggestionDiagnostics throws a TypeError reading undefined 'parent' when processing a JavaScript file with a JSDoc @return this annotation*

 * (48 weeks ago) **RyanCavanaugh** added labels `Domain: Suggestion Diagnostics`, `7.0 LS Migration`
 * [40 weeks ago](https://github.com/microsoft/TypeScript/issues/61314#issuecomment-3634662108) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * [today](https://github.com/microsoft/TypeScript/issues/61314#issuecomment-5738732574) **RyanCavanaugh** explained that the exception occurred in the pre-TypeScript-7 JavaScript Compiler API path used by checker.getSuggestionDiagnostics, which is deprecated, and that the TypeScript language service was replaced by the native LSP implementation
 * **RyanCavanaugh** added label `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#61441](https://github.com/microsoft/TypeScript/issues/61441) (Closed, `Bug`, `Help Wanted`, `Domain: Node ESM`, `Needs Human Review`)

**Allow \`import\.meta\.url\` when \`module\` is \`node16\` or \`node18\`**

*TypeScript currently disallows import.meta.url when module is set to node16 or node18 despite those Node versions supporting it.*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [1.5 years ago](https://github.com/microsoft/TypeScript/issues/61441#issuecomment-2733575959) **ExE-Boss** said "@typescript-bot run repros"
 * **RyanCavanaugh** added label `Domain: Node ESM`
 * [today](https://github.com/microsoft/TypeScript/issues/61441#issuecomment-5738772743) **RyanCavanaugh** clarified that node16 and node18 modes permitted import.meta in ESM, that TypeScript 5.8.2 and the native compiler accepted the example, and how module modes determined by package.json affected import.meta diagnostics
 * **RyanCavanaugh** added label `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#61540](https://github.com/microsoft/TypeScript/issues/61540) (Closed, `Bug`, `Fixed`, `Domain: Mapped Types`, `Needs Human Review`, **weswigham**)

**\[bug:7\.5\.3\] Mapper class explicite field regression**

*TypeScript 5.7.3 fails to infer primitive class field types within mapper classes without explicit annotations*

 * (1.4 years ago) **RyanCavanaugh** added label `Domain: Mapped Types`, set milestone to `TypeScript 5.9.0`, and assigned to **weswigham**
 * [today](https://github.com/microsoft/TypeScript/issues/61540#issuecomment-5738837608) **RyanCavanaugh** reported that the issue was fixed in the native TypeScript build 7.1.0-dev.20260918.1 and described the corrected Quick Info display
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#61552](https://github.com/microsoft/TypeScript/issues/61552) (Closed, `Bug`, `Fixed`, `Help Wanted`, `Domain: check: Type Inference`, `Needs Human Review`)

**Incorrect type inference for generic class in JavaScript**

*VS Code incorrectly infers C<T[][]> for a generic class constructor call inside the class itself instead of the expected C<T[]>.*

 * (1.4 years ago) **RyanCavanaugh** added labels `Help Wanted`, `Domain: Type Inference`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/61552#issuecomment-5738807022) **RyanCavanaugh** reported that the class-local call inference changed from C<T[][]> in TypeScript 5.8.3 to C<T[]> in TypeScript 6.0.3, matching the constructor argument
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#61678](https://github.com/microsoft/TypeScript/issues/61678) (Closed, `Bug`, `Fixed`, `Domain: flag: exactOptionalPropertyTypes`, `Needs Human Review`, **ahejlsberg**)

**With exactOptionalPropertyTypes enabled, assigning a union with missing literal properties is incorrectly allowed**

*Under exactOptionalPropertyTypes, using a generic function to return a discriminated union allows missing required properties but direct returns error.*

 * (1.3 years ago) **RyanCavanaugh** added labels `Bug`, `Domain: exactOptionalPropertyTypes`, and assigned to **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript/issues/61678#issuecomment-5738841401) **RyanCavanaugh** noted that native compiler 7.1.0-dev.20260918.1 fixed the TS2322 error under strictNullChecks and exactOptionalPropertyTypes for both functionCall and directReturn, and contrasted this with classic 6.0.3’s behavior
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#61717](https://github.com/microsoft/TypeScript/issues/61717) (Closed, `Bug`, `Fixed`, `Help Wanted`, `Domain: tsc -b`, `Needs Human Review`)

**\`tsc \-\-build \-\-watch\` produces stray \`\.js\`/\`\.js\.map\` files when adding a file to upstream project**

*tsc --build --watch in TS 5.6+ wrongly emits stray .js/.js.map files into upstream project src when switching branches.*

 * (1.3 years ago) **RyanCavanaugh** added label `Domain: tsc -b`, and set milestone to `Backlog`
 * [20 weeks ago](https://github.com/microsoft/TypeScript/issues/61717#issuecomment-4359135572) **otech47** shared detailed reproduction context for a bug emitting stray .d.ts files under tsc --watch in a Yarn workspaces monorepo, noting dependencies on large file checkouts and long watcher uptime
 * [today](https://github.com/microsoft/TypeScript/issues/61717#issuecomment-5738855851) **RyanCavanaugh** reported that tsc --build --watch no longer created project1/src/multiply.js or its .map in TypeScript 6.0.3 but did in 5.9.3
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#61718](https://github.com/microsoft/TypeScript/issues/61718) (Closed, `Bug`, `Fixed`, `Help Wanted`, `Domain: Declaration Emit`, `Needs Human Review`)

**Emitted declarations for JS file do not import a class if it's re\-exported**

*When emitting declarations for JavaScript files, TypeScript fails to include imports for re-exported classes.*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [1.2 years ago](https://github.com/microsoft/TypeScript/issues/61718#issuecomment-3005051291) **adelekekismath** said "Would it be possible to assign me to this topic?"
 * **RyanCavanaugh** added label `Domain: Declaration Emit`
 * [today](https://github.com/microsoft/TypeScript/issues/61718#issuecomment-5738846719) **RyanCavanaugh** demonstrated that TypeScript 7.1.0-dev.20260918.1 emitted the correct declarations with allowJs, checkJs, and declaration emit enabled, contrasted it with TypeScript 6.0.3’s incorrect output, and traced the regression to PR #55472
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#61768](https://github.com/microsoft/TypeScript/issues/61768) (Open, `Bug`, `Domain: lib.d.ts`, `Needs Human Review`, **sandersn**, **RyanCavanaugh**, **Copilot**)

**\`IntegerTypedArray\` type required for use with \`crypto\.getRandomValues\`**

*crypto.getRandomValues TypeScript definitions need to restrict parameters to integer typed arrays and exclude null and float arrays.*

 * (1.2 years ago) **RyanCavanaugh** added label `Domain: lib.d.ts`, and assigned to **sandersn**
 * [29 weeks ago](https://github.com/microsoft/TypeScript/issues/61768#issuecomment-3945060746) **aryzing** mentioned that the same would apply to crypto.subtle.importKey and linked the MDN documentation
 * [today](https://github.com/microsoft/TypeScript/issues/61768#issuecomment-5738858486) **RyanCavanaugh** reported that crypto.getRandomValues still accepted Float64Array and lost typed-array members in TypeScript 6.0.3, despite browser rejections, and provided a reproduction snippet
 * (today) **RyanCavanaugh** added label `Needs Human Review`, and assigned to **Copilot**, **RyanCavanaugh**

### [Issue microsoft/TypeScript#61862](https://github.com/microsoft/TypeScript/issues/61862) (Closed, `Bug`, `Help Wanted`, `Domain: Decorators`, `Needs Human Review`)

**Class decorators run before class static side is fully defined when downleveling**

*Decorators for classes in downleveled TypeScript execute before static fields are set, causing decorators to see undefined values.*

 * (1.2 years ago) **RyanCavanaugh** added label `Domain: Decorators`, and set milestone to `Backlog`
 * [40 weeks ago](https://github.com/microsoft/TypeScript/issues/61862#issuecomment-3632036122) **miyaokamarina** explained the correct behavior of decorator and class static initialization order and illustrated it with example code
 * [today](https://github.com/microsoft/TypeScript/issues/61862#issuecomment-5738863999) **RyanCavanaugh** explained that decorate is called before static x initialization and showed use of addInitializer to log x after initialization, noting consistency across TS 5.6.3 and the native compiler with specified flags
 * **RyanCavanaugh** added label `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#62048](https://github.com/microsoft/TypeScript/issues/62048) (Open, `Bug`, `Help Wanted`, `Domain: lib.d.ts`, `Needs Human Review`, **RyanCavanaugh**, **Copilot**)

**Intl\.Collator\#compare method type does not match spec**

*The TypeScript Intl.Collator.compare is incorrectly typed as a method instead of a spec-compliant getter returning a bound function.*

 * [1.1 years ago](https://github.com/microsoft/TypeScript/issues/62048#issuecomment-3077145563) **RyanCavanaugh** said "@bdpartridge no, otherwise by that logic Math.max("hello", "world") would be valid because its inputs are also coerced to string"
 * [1.1 years ago](https://github.com/microsoft/TypeScript/issues/62048#issuecomment-3079294005) **bdpartridge** said "@RyanCavanaugh Good point. Since the string coercion might be surprising, it's probably best to just stick with what's intended."
 * **RyanCavanaugh** added label `Domain: lib.d.ts`
 * [today](https://github.com/microsoft/TypeScript/issues/62048#issuecomment-5738894976) **RyanCavanaugh** explained that Intl.Collator#compare is a bound function in Edge and works with an undefined receiver, and suggested modeling it as a readonly function-valued property with this:void
 * (today) **RyanCavanaugh** added label `Needs Human Review`, and assigned to **Copilot**, **RyanCavanaugh**

