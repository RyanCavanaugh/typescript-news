# Report for 2026-08-18 (Tuesday, August 18th, 2026)

9 different users commented on 32 different issues.

## Activity Summary

### [Issue microsoft/TypeScript#13565](https://github.com/microsoft/TypeScript/issues/13565) (Closed, `Bug`, `Domain: ES Modules`)

**Error when augmenting UMD module**

*Augmenting a UMD module triggers an error about referencing its global in a module context.*

 * (9.5 years ago) **mhegazy** set milestone to `Future`, and removed from milestone `TypeScript 2.2`
 * **RyanCavanaugh** added label `Domain: ES Modules`
 * [today](https://github.com/microsoft/TypeScript/issues/13565#issuecomment-5331976686) **RyanCavanaugh** showed that the issue was fixed in current TypeScript by providing a three-file example and contrasted TS 2.1.1's error with TS 7.1.0-dev's successful compilation
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#14080](https://github.com/microsoft/TypeScript/issues/14080) (Closed, `Bug`, `Domain: classes`)

**Can not declaration merging for default exported class**

*Default-exported classes in TypeScript cannot be merged with additional declarations, preventing prototype method additions.*

 * [3 years ago](https://github.com/microsoft/TypeScript/issues/14080#issuecomment-1658460871) **zhangone233** said "When will this issue be fixed ？"
 * [1.3 years ago](https://github.com/microsoft/TypeScript/issues/14080#issuecomment-2767101977) **GulgDev** said "Are there any better workarounds than what @neuoy suggested? I have a more complex case in which that would be harder to do."
 * **RyanCavanaugh** added label `Domain: classes`
 * [today](https://github.com/microsoft/TypeScript/issues/14080#issuecomment-5332042038) **RyanCavanaugh** described the correct way to augment a default export in TypeScript and explained why rejecting the augmentation in the OP is correct
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#18295](https://github.com/microsoft/TypeScript/issues/18295) (Closed, `Bug`, `Domain: API`)

**The language service does not resolve symbolic links**

*Add an optional realpath method to LanguageServiceHost to enable symbolic link resolution and prevent related build errors.*

 * (8.1 years ago) **mhegazy** set milestone to `Future`, and removed from milestone `TypeScript 3.0`
 * **RyanCavanaugh** unassigned **rbuckton**
 * [today](https://github.com/microsoft/TypeScript/issues/18295#issuecomment-5332730875) **RyanCavanaugh** said "Moot with new API"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#18717](https://github.com/microsoft/TypeScript/issues/18717) (Closed, `Bug`, `Domain: check: Control Flow`)

**Union type inference failure in generic function**

*TypeScript fails to narrow a union of keyof TData and an object with a name property, causing a compile error when accessing name.*

 * **mhegazy** added to milestone `Future`
 * **sandersn** unassigned **sandersn**
 * **RyanCavanaugh** added label `Domain: Control Flow`
 * [today](https://github.com/microsoft/TypeScript/issues/18717#issuecomment-5332801455) **RyanCavanaugh** said "This is fixed now"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#2137](https://github.com/microsoft/TypeScript/issues/2137) (Closed, `Bug`, `Help Wanted`, `Domain: API`, `Domain: Binder`)

**SourceFileObject\.getNamedDeclarations is missing declarations before methods**

*SourceFileObject.getNamedDeclarations mistakenly omits the 'height' property by replacing it with the 'square' method when symbols are undefined.*

 * (7.4 years ago) **RyanCavanaugh** added label `Domain: Binder`, set milestone to `Backlog`, and removed from milestone `Community`
 * [today](https://github.com/microsoft/TypeScript/issues/2137#issuecomment-5331940180) **RyanCavanaugh** said "This is fixed (and we're rewriting the API anyway)"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#23141](https://github.com/microsoft/TypeScript/issues/23141) (Closed, `Bug`, `Domain: JavaScript`)

**In JS, auto type assignments don't add string index to literal types**

*Assigning a variable in separate branches causes its inferred literal type to omit string index signatures.*

 * (7.7 years ago) **weswigham** removed labels `Salsa`, `Salsa`
 * **sandersn** unassigned **sandersn**
 * [today](https://github.com/microsoft/TypeScript/issues/23141#issuecomment-5332817342) **RyanCavanaugh** reported that the result type was now consistently a union of objects with `a` or `b`, and found it acceptable
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#23362](https://github.com/microsoft/TypeScript/issues/23362) (Closed, `Bug`, `Domain: JavaScript`)

**JSDOC inconsistance casting behavior**

*Two arrow functions annotated as utils.TypeGuard<string> in JS with JSDoc produce inconsistent type-checking results based on parentheses.*

 * (7.7 years ago) **weswigham** removed labels `Salsa`, `Salsa`
 * **sandersn** unassigned **sandersn**
 * [today](https://github.com/microsoft/TypeScript/issues/23362#issuecomment-5332899626) **RyanCavanaugh** said "This is fixed now"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#24269](https://github.com/microsoft/TypeScript/issues/24269) (Closed, `Bug`, `Help Wanted`, `Domain: lib.d.ts`)

**Wrong createElementNS\(\) type definitions**

*Type definitions for Document.createElementNS incorrectly allow creating non-existent SVG elements like componentTransferFunction, textContent, and textPositioning*

 * [7.6 years ago](https://github.com/microsoft/TypeScript/issues/24269#issuecomment-447090310) **inad9300** said "Still wrong in 3.2.2."
 * (7.4 years ago) **RyanCavanaugh** set milestone to `Backlog`, and removed from milestone `Community`
 * [today](https://github.com/microsoft/TypeScript/issues/24269#issuecomment-5332926388) **RyanCavanaugh** clarified that the three SVG element initializations should now be errors and suggested opening an issue with the new lib template if not
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#24895](https://github.com/microsoft/TypeScript/issues/24895) (Closed, `Bug`, `VS Code Tracked`, `Domain: JavaScript`)

**Finding definitions exported by string key does not work**

*VSCode fails to locate definitions for functions exported using string-key bracket syntax like exports['parse'].*

 * (7.7 years ago) **weswigham** removed labels `Salsa`, `Salsa`
 * **sandersn** unassigned **sandersn**
 * [today](https://github.com/microsoft/TypeScript/issues/24895#issuecomment-5332952813) **RyanCavanaugh** said "This is fixed in latest"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#25303](https://github.com/microsoft/TypeScript/issues/25303) (Closed, `Bug`, `Help Wanted`, `Domain: JSDoc`)

**@typedef tags appearing in the next declaration quick info in VSCode**

*JSDoc @typedef tags in .js files incorrectly persist into the hover quick info of subsequent declarations in VSCode*

 * (7.4 years ago) **RyanCavanaugh** set milestone to `Backlog`, and removed from milestone `Community`
 * [6.3 years ago](https://github.com/microsoft/TypeScript/issues/25303#issuecomment-609843958) **arslivinski** reported that the issue was already fixed and provided version and environment details
 * [today](https://github.com/microsoft/TypeScript/issues/25303#issuecomment-5333039359) **RyanCavanaugh** said "Checked in 7.0 as well, this is fixed"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#25349](https://github.com/microsoft/TypeScript/issues/25349) (Closed, `Bug`, `Help Wanted`, `Domain: API`)

**meta: factory function inconsistencies**

*TypeScript factory functions exhibit inconsistent naming, parameter nullability, overloads, decorators, and modifiers, requiring standardization.*

 * **mhegazy** added to milestone `Community`
 * (7.4 years ago) **RyanCavanaugh** set milestone to `Backlog`, and removed from milestone `Community`
 * [today](https://github.com/microsoft/TypeScript/issues/25349#issuecomment-5333056365) **RyanCavanaugh** said "This got touched up in #35282 but this entire API is removed as of 7.0"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#25736](https://github.com/microsoft/TypeScript/issues/25736) (Closed, `Bug`, `Domain: JSDoc`, `checkJs`, `Domain: JavaScript`)

**\`@callback\` is only generic after \`@template\` tag**

*Callback signatures in JSDoc with @template tags do not register type parameters, causing generics errors and infinite recursion in quickinfo*

 * (7.4 years ago) **sandersn** set milestone to `Backlog`, removed from milestone `TypeScript 3.4.0`, and unassigned **sandersn**
 * [today](https://github.com/microsoft/TypeScript/issues/25736#issuecomment-5333065953) **RyanCavanaugh** noted that TypeScript 5.1 intentionally fixed the placement of @template before @callback, provided a reduced repro showing the old and new error messages, and confirmed that reordering the tags resolves the issue
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#27023](https://github.com/microsoft/TypeScript/issues/27023) (Closed, `Bug`, `Domain: JSDoc`)

**Check property declarations in JS**

*Enable IDE recognition of JSDoc type comments on Babel-decorated class properties for accurate type hints*

 * (7.4 years ago) **sandersn** set milestone to `Backlog`, and unassigned **sandersn**
 * **RyanCavanaugh** added label `Domain: JSDoc`
 * [today](https://github.com/microsoft/TypeScript/issues/27023#issuecomment-5333384809) **RyanCavanaugh** reported that the issue was fixed in TypeScript 4.0 and later and demonstrated differing diagnostics across versions
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#2859](https://github.com/microsoft/TypeScript/issues/2859) (Closed, `Bug`, `Domain: Source Maps`)

**Port from old compiler code to emit identifier renames into source map**

*Restore emission of identifier rename mappings in TypeScript source maps to support IE debugger mapping of “this” to “_this”.*

 * **RyanCavanaugh** unassigned **mhegazy**
 * [6.5 years ago](https://github.com/microsoft/TypeScript/issues/2859#issuecomment-584558197) **bentaly** said "Still an issue, would be good to get it addressed"
 * **RyanCavanaugh** added label `Domain: Source Maps`
 * [today](https://github.com/microsoft/TypeScript/issues/2859#issuecomment-5331952604) **RyanCavanaugh** said "ES5 is no longer supported, so this is moot"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#31670](https://github.com/microsoft/TypeScript/issues/31670) (Closed, `Discussion`)

**The future of the "private" keyword**

*Discussion of TypeScript’s plan to retain its existing private keyword while supporting new JavaScript private fields (#fields) and associated rules.*

 * [yesterday](https://github.com/microsoft/TypeScript/issues/31670#issuecomment-5320459312) **ljharb** argued that banning a type-space syntax differed qualitatively from banning a non-standard value-space syntax with false encapsulation and that the proposed `private` keyword offered no practical benefits over existing JavaScript patterns
 * [today](https://github.com/microsoft/TypeScript/issues/31670#issuecomment-5327867983) **snarbles2** pointed out that TypeScript's private has capabilities unavailable to #private and suggested using a linter
 * [today](https://github.com/microsoft/TypeScript/issues/31670#issuecomment-5328307514) **mbrowne** suggested marking the private keyword as deprecated in the official docs due to its non-standard status and availability of native alternatives
 * [today](https://github.com/microsoft/TypeScript/issues/31670#issuecomment-5332662192) **rjgotten** pointed out that private is misnamed and not enforced at runtime, equated a compiler flag to disallow private with a linter option, and suggested improved syntax for symbol usage and unique symbol ergonomics

### [Issue microsoft/TypeScript#3845](https://github.com/microsoft/TypeScript/issues/3845) (Closed, `Bug`, `Breaking Change`, `Help Wanted`, `Domain: enum`)

**Enum types are not checked in binary operators**

*Compound assignment and bitwise operations on enums bypass type checking, allowing incompatible enum types to mix.*

 * (7.4 years ago) **RyanCavanaugh** added label `Domain: enum`, set milestone to `Backlog`, and removed from milestone `Community`
 * [today](https://github.com/microsoft/TypeScript/issues/3845#issuecomment-5331815440) **RyanCavanaugh** noted that the type system would remain incoherent unless both the enum-to-number assignability hole and the A | A typing as number were patched
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#5689](https://github.com/microsoft/TypeScript/issues/5689) (Closed, `Bug`, `Help Wanted`, `Domain: API`)

**Language Service: TypeParameter\.constraint is lazily calculated, but does not have an accessor function**

*Lazily computed type members such as TypeParameter.constraint lack an accessor method, requiring awkward calls like getProperties() to resolve them.*

 * **mhegazy** added to milestone `Community`
 * (7.4 years ago) **RyanCavanaugh** set milestone to `Backlog`, and removed from milestone `Community`
 * [today](https://github.com/microsoft/TypeScript/issues/5689#issuecomment-5333538634) **RyanCavanaugh** said "This was fixed via #20137"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#6281](https://github.com/microsoft/TypeScript/issues/6281) (Closed, `Bug`, `Domain: JSX/TSX`)

**Indentation failure with unclosed JSX element**

*Pressing Enter after an unclosed JSX element inside a namespace causes getIndentationAtPosition to crash with an assertion failure.*

 * **mhegazy** unassigned **vladima**
 * **RyanCavanaugh** unassigned **mhegazy**
 * [3 years ago](https://github.com/microsoft/TypeScript/issues/6281#issuecomment-1663783547) **Andarist** said "The expected result isn't completely clear for me here and I can't assess if this is already fixed or not."
 * [today](https://github.com/microsoft/TypeScript/issues/6281#issuecomment-5333548153) **RyanCavanaugh** said "Tracked at #4332 and has been fixed"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63749](https://github.com/microsoft/TypeScript/issues/63749) (Open, `Bug`, **ahejlsberg**)

**\[7\.0\] Can't access field if it is protected in one constituent of an intersection \(type order dependent\)**

*TypeScript 7 erroneously prevents accessing a property protected in one part of an intersection type when constituent order differs.*

 * [4 days ago](https://github.com/microsoft/TypeScript/issues/63749#issuecomment-5295663639) **RyanCavanaugh** clarified that intersections are order-dependent and proposed allowing access if any constituent is public
 * (4 days ago) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`
 * **ahejlsberg** assigned to **ahejlsberg**

### [Issue microsoft/TypeScript#63754](https://github.com/microsoft/TypeScript/issues/63754) (Open, `Bug`)

**Diagnostic code 8030 being incorrectly generated using JSDoc \`@type\` on a function\.**

*TypeScript 7.0.2's JSDoc @type on a function wrongly triggers diagnostic 8030 by appending '| undefined' to the referenced interface method type.*

 * [yesterday](https://github.com/microsoft/TypeScript/issues/63754#issuecomment-5321512243) **RyanCavanaugh** reported inability to reproduce the issue on the provided files and asked for a self-contained repro including Example visibility, method declaration, and tsconfig options
 * **RyanCavanaugh** added label `Needs More Info`
 * [today](https://github.com/microsoft/TypeScript/issues/63754#issuecomment-5327648214) **Arashiryuu** provided reproduction steps with tsconfig and code demonstrating incorrect hover type info for an optional method in TS 7.0.2
 * (today) **RyanCavanaugh** added label `Bug`, removed label `Needs More Info`, and set milestone to `TypeScript 7.1`
 * **typescript-automation[bot]** added label `Fix Available`
 * [today](https://github.com/microsoft/TypeScript/issues/63754#issuecomment-5331383884) **RyanCavanaugh** demonstrated that the single-file repro worked and recommended removing null/undefined then contextually typing to avoid an implicit any on `s`

### [Issue microsoft/TypeScript#63755](https://github.com/microsoft/TypeScript/issues/63755) (Closed, `Suggestion`, `Awaiting More Feedback`)

**Contextually type \`this\` inside \`function\*\` from a leading thisArg**

*Implement contextual this typing for generator function expressions based on a leading thisArg to infer the enclosing instance type.*

 * **RyanCavanaugh** added label `Awaiting More Feedback`
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63755#issuecomment-5320745088) **RyanCavanaugh** said "I'm a little surprised this doesn't work already. If it's a ~one-line fix we should just do it; maybe there were unforeseen complications originally"
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63755#issuecomment-5324016464) **bun-unsafe** clarified that contextual `this` works for plain functions but not for generator functions and requested applying the existing contextual-`this` rule to function* expressions
 * [later](https://github.com/microsoft/TypeScript/issues/63755#issuecomment-5344505069) **Andarist** asked to share the repro case as a TS playground after verifying that the provided code snippets worked

### [Issue microsoft/TypeScript#63756](https://github.com/microsoft/TypeScript/issues/63756) (Closed)

**There are no 7\.x branches or tags**

*NPM lists 7.x releases for the package but the repository contains no corresponding 7.x branches, tags, or source code.*

 * [yesterday](https://github.com/microsoft/TypeScript/issues/63756#issuecomment-5320506353) **RyanCavanaugh** said "7.0 development was staged at https://github.com/microsoft/TypeScript-go and is moving back into this repo."
 * (yesterday) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript/issues/63756#issuecomment-5330372426) **Pomax** questioned why the issue was closed as not planned, pointed out that the README linked to the wrong repository, and stated that the current 7.x release was untrustworthy due to a bungled process
 * [today](https://github.com/microsoft/TypeScript/issues/63756#issuecomment-5331257146) **RyanCavanaugh** explained that development occurred in the TypeScript-go repo with ample public evidence, argued that tagging releases here would not satisfy everyone, and concluded there is no way to avoid confusion

### [Issue microsoft/TypeScript#63757](https://github.com/microsoft/TypeScript/issues/63757) (Open)

**\[7\.0 API\] \- Accessing name on a jsdoc link that does not have a valid name produces sibling node**

*In TypeScript 7.0’s API, invalid JSDoc link names produce a sibling node instead of undefined.*

 * created by **dragomirtitian**
 * [today](https://github.com/microsoft/TypeScript/issues/63757#issuecomment-5338133199) **MartinJohns** said "Am I missing something? 7.0 doesn't have an API."

### [Issue microsoft/TypeScript#63758](https://github.com/microsoft/TypeScript/issues/63758) (Open, `Needs Investigation`, **RyanCavanaugh**, **Copilot**)

**Investigate decorator initialization order re: renames of classes**

*Verified that computed class-element names require alias substitution to match tsc output, making the exclusion suggestion incorrect.*

 * created by **RyanCavanaugh**

### [Issue microsoft/TypeScript#63759](https://github.com/microsoft/TypeScript/issues/63759) (Closed, `External`)

**\`getReturnType\` stack overflow when using recursive generic function with accumulated type argument**

*getReturnType causes stack overflow when inferring return types for recursive generic functions with accumulated type arguments*

 * created by **StyleShit**

### [Issue microsoft/TypeScript#63760](https://github.com/microsoft/TypeScript/issues/63760) (Open, `Not a Defect`)

**Improve tsdoc for sort\(\)**

*Update the TSDoc example for sort() in es5.d.ts to include the returned sorted array output.*

 * created by **advinans-dennis**

### [Issue microsoft/TypeScript#63761](https://github.com/microsoft/TypeScript/issues/63761) (Open)

**Panic "Diagnostic emitted without context" ts\-go in declaration emit for \`export default\` arrow/function expression with non\-portable inferred return type**

*Native TypeScript compiler panics on declaration emit for default-exported arrow functions with non-portable inferred return types*

 * created by **suyash-vyas**
 * [later](https://github.com/microsoft/TypeScript/issues/63761#issuecomment-5344526924) **suyash-vyas** said "Filed here rather than typescript-go since new activity there is locked for the repo move (https://github.com/microsoft/typescript-go/issues/4918). Happy to raise a fix :)"

### [Issue microsoft/TypeScript#63890](https://github.com/microsoft/TypeScript/issues/63890) (Open, `Needs Investigation`, **andrewbranch**)

**API returns a stale SourceFile after the latest snapshot is disposed**

*After disposing a snapshot, calling updateSnapshot again returns a cached outdated SourceFile instead of reflecting new file edits.*

 * created by **dbaeumer**
 * (later) **andrewbranch** set milestone to `TypeScript 7.1`, and assigned to **andrewbranch**

### [Issue microsoft/TypeScript#9091](https://github.com/microsoft/TypeScript/issues/9091) (Closed, `Bug`, `Domain: Module Resolution`)

**Symlinks not resolved for \`/// \<reference path="\.\.\." /\>\`**

*TypeScript resolves symlinks inconsistently between reference path and module imports, leading to duplicate identifier errors.*

 * [8.8 years ago](https://github.com/microsoft/TypeScript/issues/9091#issuecomment-336300563) **benpetersen** asked if there was a workaround for the issue after no updates in months
 * [6.2 years ago](https://github.com/microsoft/TypeScript/issues/9091#issuecomment-634353976) **btakita** said "This issue is still occurring on an Angular + lerna project. Is there a workaround for this issue?"
 * **RyanCavanaugh** added label `Domain: Module Resolution`
 * [today](https://github.com/microsoft/TypeScript/issues/9091#issuecomment-5331968951) **RyanCavanaugh** confirmed that newer TypeScript versions no longer report TS2451 on both real and symlinked files and that the reduced repro and nested-package scenario compile without diagnostics
 * (today) **RyanCavanaugh** closed the issue

