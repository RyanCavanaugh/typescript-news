# Report for 2026-09-23 (Wednesday, September 23rd, 2026)

20 different users commented on 340 different issues.

## Activity Summary

### [Issue microsoft/TypeScript#13165](https://github.com/microsoft/TypeScript/issues/13165) (Closed, `Bug`, `Domain: API`)

**Compiler API: no Symbol for Node**

*TypeScript’s compiler API getSymbolAtLocation sometimes returns undefined for identifier nodes in abstract class method declarations and external object property accesses.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/13165#issuecomment-5458035195) **RyanCavanaugh** noted that the pre-TypeScript-7 Compiler API was superseded by TypeScript 7 and closed the request
 * **RyanCavanaugh** added label `Needs Human Review`
 * (3 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#14374](https://github.com/microsoft/TypeScript/issues/14374) (Closed, `Bug`, `Help Wanted`, `Domain: lib.d.ts`, `VS Code Tracked`)

**Dom d\.ts does not define event\.target\.parentNode**

*VSCode autocomplete fails to list parentNode on event.target because the DOM type definitions omit that property.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/14374#issuecomment-5458859058) **RyanCavanaugh** explained that event.target is EventTarget|null rather than Node and demonstrated narrowing it with instanceof Node before accessing parentNode
 * **RyanCavanaugh** added label `Needs Human Review`
 * (3 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#14575](https://github.com/microsoft/TypeScript/issues/14575) (Closed, `Bug`, `Help Wanted`, `Domain: API`, `Domain: JSDoc`)

**JSDoc comment nodes are not traversed and their parents are sent even if they should not**

*JSDoc comment nodes incorrectly retain parent pointers when parent tracking is disabled and aren’t traversed by forEachChild.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/14575#issuecomment-5458869598) **RyanCavanaugh** explained that the behavior was in the pre-TypeScript-7 JavaScript Compiler API, which had been superseded by the TypeScript 7 API and was no longer being developed, and that changes to createSourceFile, JSDoc parent pointers, or forEachChild traversal could not be accepted
 * **RyanCavanaugh** added label `Needs Human Review`
 * (3 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#15514](https://github.com/microsoft/TypeScript/issues/15514) (Closed, `Bug`, `Domain: Something Else`)

**Cannot have array binding patterns without iterable extensions**

*Array destructuring in declarations triggers a missing iterator error instead of a destructuring error, while object destructuring yields no error.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/15514#issuecomment-5458899027) **RyanCavanaugh** demonstrated that the declaration with destructuring parameters produced no diagnostics in TypeScript 2.2.1 and the current nightly
 * **RyanCavanaugh** added label `Needs Human Review`
 * (3 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#16426](https://github.com/microsoft/TypeScript/issues/16426) (Closed, `Bug`, `Domain: Performance`)

**TypeScript Language Service is slow to load projects over network file systems**

*TypeScript's language service is slow on networked file systems because of redundant file stats and needs a predefined file list.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/16426#issuecomment-5482086976) **RyanCavanaugh** identified the report as a duplicate of microsoft/TypeScript#11979 and referenced the broader custom module-resolution hook tracked by microsoft/TypeScript#18896
 * **RyanCavanaugh** added label `Needs Human Review`
 * (3 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#17293](https://github.com/microsoft/TypeScript/issues/17293) (Open, `Bug`, `Domain: Declaration Emit`)

**Unexpected TS4094 with the build parameter \`declaration: true\`**

*TypeScript 2.4.1 incorrectly reports TS4094 on private properties of exported class expressions when declaration files are generated.*

 * [36 weeks ago](https://github.com/microsoft/TypeScript/issues/17293#issuecomment-3735663811) **valler** explained that extending a class with private properties is valid, demonstrated how the given factory pattern breaks instanceof, challenged the relevance of the linked issue, and proposed a constructor-based alternative
 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/17293#issuecomment-5483502779) **RyanCavanaugh** explained that TS4094 is expected for the declaration shape and recommended giving Foo an explicit declaration-facing type to avoid exposing private members
 * **RyanCavanaugh** added label `Needs Human Review`
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#17372](https://github.com/microsoft/TypeScript/issues/17372) (Closed, `Bug`, `Domain: enum`)

**\`const enum\` inside a namespace makes it treated as a value**

*Defining a const enum inside a namespace merged with a const variable incorrectly triggers a redeclaration error in TypeScript.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/17372#issuecomment-5483719505) **RyanCavanaugh** explained that const enums retain value-meaning so they cannot merge with a separate declare const and that making this depend on --preserveConstEnums is not viable
 * **RyanCavanaugh** added label `Needs Human Review`
 * (3 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#17552](https://github.com/microsoft/TypeScript/issues/17552) (Closed, `Bug`, `Domain: API`, `Domain: API: Transforms`)

**File altered by before transform does not remove new unused imports**

*The before-transform API in TypeScript fails to remove imports that become unused after code transformations.*

 * [1 month ago](https://github.com/microsoft/TypeScript/issues/17552#issuecomment-5430918411) **RyanCavanaugh** explained that import usage is determined during checking before `before` transformers run and that transformers must explicitly remove unused imports since automatic rechecking isn't supported
 * **RyanCavanaugh** added label `Needs Human Review`
 * (1 month ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#18537](https://github.com/microsoft/TypeScript/issues/18537) (Open, `Bug`, `Domain: check: Excess Property Checking`)

**Can not specify toString/valueOf methods in object literal**

*TypeScript rejects object literals with toString or valueOf properties absent from the interface despite their presence on Object.prototype.*

 * **RyanCavanaugh** added label `Domain: Excess Property Checking`
 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/18537#issuecomment-5483894736) **RyanCavanaugh** explained that x1 was rejected because it is a fresh object literal without a declared toString member, that x2 assignment is allowed due to structural assignability, referenced the TS FAQ on indirect excess properties, and suggested declaring toString in the interface
 * **RyanCavanaugh** added label `Needs Human Review`
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#18661](https://github.com/microsoft/TypeScript/issues/18661) (Closed, `Bug`, `Domain: Comment Emit`)

**Printer doesn't print jsDoc comments**

*The TypeScript AST printer is not preserving JSDoc comments when printing transformed nodes.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/18661#issuecomment-5483933681) **RyanCavanaugh** described that the example uses the pre-TypeScript-7 JavaScript Compiler API, which has been superseded by TypeScript 7 and cannot be modified
 * **RyanCavanaugh** added label `Needs Human Review`
 * (3 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#19374](https://github.com/microsoft/TypeScript/issues/19374) (Closed, `Bug`, `Domain: Error Messages`)

**Compiler gives two different errors for wrong number of type arguments**

*TypeScript compiler produces inconsistent errors for supplying too many generic type arguments in class extensions versus instantiations.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/19374#issuecomment-5484060587) **RyanCavanaugh** described that the two sites intentionally used different diagnostics, gave examples of TS2707 vs TS2558 errors when given too many type arguments, and noted rejecting common terse wording to preserve context
 * **RyanCavanaugh** added label `Needs Human Review`
 * (3 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#19950](https://github.com/microsoft/TypeScript/issues/19950) (Closed, `Bug`, `Help Wanted`, `Domain: API`, `Domain: API: Transforms`)

**SourceFile\.ambientModuleNames is undefined after transform\(\)**

*Using ts.transform causes transformed SourceFiles to lose ambientModuleNames, causing module resolution failures during compilation.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/19950#issuecomment-5484343232) **RyanCavanaugh** clarified that the requested behavior was part of the pre-TypeScript-7 JavaScript Compiler API, which was no longer maintained and had been superseded by the TypeScript 7 API
 * **RyanCavanaugh** added label `Needs Human Review`
 * (3 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#22467](https://github.com/microsoft/TypeScript/issues/22467) (Closed, `Bug`, `Help Wanted`, `Domain: API`, `Good First Issue`)

**getDefinitionAtPosition doesn't distinguish different kinds in a merged declaration**

*getDefinitionAtPosition incorrectly reports all merged declarations as class rather than distinguishing module, class, and interface*

 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/22467#issuecomment-5485066980) **RyanCavanaugh** said "This concerns the pre-TypeScript 7 JavaScript Compiler API. That API has been superseded by the TypeScript 7 API and is no longer being developed, so this change will not be made."
 * **RyanCavanaugh** added label `Needs Human Review`
 * (3 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#23572](https://github.com/microsoft/TypeScript/issues/23572) (Closed, `Bug`, `Domain: check: Control Flow`)

**Exhaustiveness checking against an enum only works when the enum has \>1 member\.**

*TypeScript's exhaustiveness checking on a discriminated union fails when the enum used for the discriminant has only one member.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/23572#issuecomment-5485477604) **RyanCavanaugh** said "Duplicate of #16976. Both reports concern a non-union object with a literal discriminant remaining assignable after every possible switch case has been handled, rather than narrowing to never."
 * **RyanCavanaugh** added label `Needs Human Review`
 * (3 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#24380](https://github.com/microsoft/TypeScript/issues/24380) (Closed, `Bug`, `Domain: API`, `Domain: API: Transforms`)

**ts\.createJsxOpeningElement throws \`Debug Failure\. False expression\.\`**

*Calling ts.createJsxOpeningElement in a custom transformer on a JSX element triggers a Debug Failure error.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/24380#issuecomment-5485546391) **RyanCavanaugh** explained that the report concerned an outdated pre-TypeScript 7 API that has been superseded and can no longer be addressed
 * **RyanCavanaugh** added label `Needs Human Review`
 * (3 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#25919](https://github.com/microsoft/TypeScript/issues/25919) (Closed, `Bug`, `Domain: enum`)

**Special characters in 'enum' type will be compiled to unicode by default**

*Special characters in enum values compile to unicode escapes while object literals use UTF-8, causing inconsistent encoding.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/25919#issuecomment-5486595426) **RyanCavanaugh** noted that object values preserve non-ASCII text while string enum values are escaped in emitted JavaScript for TS 2.9.1 and nightly 7.1.0-dev.20260831.1
 * **RyanCavanaugh** added label `Needs Human Review`
 * (3 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#26075](https://github.com/microsoft/TypeScript/issues/26075) (Closed, `Bug`, `Help Wanted`, `Domain: API`, `Domain: Literal Types`)

**type\.isLiteral\(\) returns false for boolean literals**

*Following a recent commit, isLiteral() returns false for boolean literals rather than true, breaking API expectations.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/26075#issuecomment-5486731921) **RyanCavanaugh** explained that the pre-7 JavaScript Compiler API had been superseded by the TypeScript 7 API and was no longer being developed, so the requested public API change could not be made
 * **RyanCavanaugh** added label `Needs Human Review`
 * (3 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#26131](https://github.com/microsoft/TypeScript/issues/26131) (Open, `Bug`, `Domain: check: Type Inference`)

**Return type inference error with async functions and Promise\.reject\(\)**

*An async function returning Promise.reject() infers Promise<never> instead of Promise<void>, triggering a TS2322 assignment error.*

 * **RyanCavanaugh** added label `Domain: Type Inference`
 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/26131#issuecomment-5486880712) **RyanCavanaugh** explained that the function is inferred as Promise<undefined> instead of Promise<never>, noted the Promise<void> assignment error, and suggested adding an explicit return type or widening the receiving variable
 * **RyanCavanaugh** added label `Needs Human Review`
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#27014](https://github.com/microsoft/TypeScript/issues/27014) (Closed, `Bug`, `Domain: Conditional Types`)

**Problem with inference for this\['prop'\] with conditional types**

*TypeScript fails to infer Unwrap<this['prop']> for the set function inside a class method.*

 * [1 month ago](https://github.com/microsoft/TypeScript/issues/27014#issuecomment-5429734370) **RyanCavanaugh** explained that `this` is polymorphic in instance methods and illustrated with a `Bar extends Foo` example why generic indexed accesses must use `Unwrap<this["prop"]>`, noting TS2345 errors in different TypeScript versions
 * **RyanCavanaugh** added label `Needs Human Review`
 * (1 month ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#27245](https://github.com/microsoft/TypeScript/issues/27245) (Closed, `Bug`, `Domain: JavaScript`)

**Mix on inline/external defined properties corrupt javascript intellisense**

*VSCode JavaScript IntelliSense fails to recognize properties added after object creation when the object literal already defines other properties.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/27245#issuecomment-5445210648) **RyanCavanaugh** noted that the current nightly build now includes both existing and added properties in completion after 'test.', contrasting with TypeScript 3.1.1 behavior
 * **RyanCavanaugh** added label `Needs Human Review`
 * (3 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#27507](https://github.com/microsoft/TypeScript/issues/27507) (Open, `Bug`, `Domain: Mapped Types`)

**CLI\-only error calling generic function**

*The TypeScript CLI reports a spurious type error when calling the generic function getFirst(i, 'n') despite no error in the editor.*

 * **ahejlsberg** unassigned **ahejlsberg**
 * [1 month ago](https://github.com/microsoft/TypeScript/issues/27507#issuecomment-5416030345) **RyanCavanaugh** confirmed that the CLI/server discrepancy was fixed and both tsc and the language service now report the same diagnostics in the current TypeScript dev build
 * **RyanCavanaugh** added label `Needs Human Review`
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#28352](https://github.com/microsoft/TypeScript/issues/28352) (Closed, `Bug`, `Domain: JSX/TSX`, **weswigham**)

**React function\-returning\-component regression**

*TypeScript 3.2 introduced a regression causing function-returning React components to reject valid JSX props.*

 * **RyanCavanaugh** added label `Needs Human Review`
 * [1 month ago](https://github.com/microsoft/TypeScript/issues/28352#issuecomment-5416055920) **weswigham** clarified that the types in the original post were incorrect, explained the correct type signature for a React component, and noted improved error messaging in modern TS
 * (1 month ago) **weswigham** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#28892](https://github.com/microsoft/TypeScript/issues/28892) (Closed, `Bug`, `Domain: JSX/TSX`)

**Dynamic TagName causing error after version upgrade**

*Upgrading to TypeScript 3.2.2 produces a regression error when using dynamic React tag names that compiled successfully in 3.1.6.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/28892#issuecomment-5491832342) **RyanCavanaugh** explained that the JSX checking behavior is intended and outlined how TypeScript handles prop types for string-typed elements, contrasted behavior between TS 3.1.6 and 3.2.2, and recommended using keyof JSX.IntrinsicElements or parameterized component types
 * **RyanCavanaugh** added label `Needs Human Review`
 * (3 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#28938](https://github.com/microsoft/TypeScript/issues/28938) (Open, `Bug`, `Domain: JSX/TSX`)

**HOC returned component props can not differ from HOC generic props**

*TypeScript 3.3 incorrectly rejects a React higher-order component that pre-fills and omits the required foo prop.*

 * [1.3 years ago](https://github.com/microsoft/TypeScript/issues/28938#issuecomment-2903751808) **keropodium** described how they updated the generic constraints in withBaseProviders to extend BaseProvidersProps and omit its keys for the wrapped component to resolve a TypeScript error
 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/28938#issuecomment-5492056598) **RyanCavanaugh** explained that the error is correct because P can require a narrower foo type making passing foo=0 unsafe and referenced the TypeScript FAQ that describes this distinction
 * **RyanCavanaugh** added label `Needs Human Review`
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#29112](https://github.com/microsoft/TypeScript/issues/29112) (Closed, `Bug`, `Fixed`, `Domain: Mapped Types`)

**Excessive stack depth comparing types with TS 3\.2 **

*TypeScript 3.2.2 fails to compile a generic function using lodash’s PartialDeep and pick due to an excessive stack depth comparing types error.*

 * (3 weeks ago) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (3 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#29132](https://github.com/microsoft/TypeScript/issues/29132) (Closed, `Bug`, `Fixed`, `Domain: This-Typing`)

**Accessing protected properties with \`this\` argument specifier differs with interface**

*TypeScript inconsistently handles protected property access via `this` parameters for generic versus non-generic abstract classes.*

 * (3 weeks ago) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (3 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#29922](https://github.com/microsoft/TypeScript/issues/29922) (Closed, `Bug`, `Fixed`, `Domain: Something Else`)

**Upgrading from 3\.0\.3 to 3\.1\.1 breaks underscore type definition**

*Upgrading TypeScript from 3.0.3 to 3.1.1 breaks underscore type definitions and causes TS2339 errors for methods like each.*

 * (3 weeks ago) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (3 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#30176](https://github.com/microsoft/TypeScript/issues/30176) (Closed, `Bug`, `Domain: JSDoc`)

**JSDoc Class extending Array not supported \(?\)**

*VSCode fails to recognize JSDoc generics on a custom Array subclass, ignoring both element types and its methods.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/30176#issuecomment-5498848809) **RyanCavanaugh** explained that FooArray.<XYZ> required a declared type parameter and provided a corrected JSDoc example for extending Array
 * **RyanCavanaugh** added label `Needs Human Review`
 * (3 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#30451](https://github.com/microsoft/TypeScript/issues/30451) (Closed, `Bug`, `Domain: JSDoc`)

**Inconsistent error reporting for duplicate JSDoc tags**

*TypeScript only flags duplicate JSDoc tags within the same comment while ignoring redundancies across separate comments.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/30451#issuecomment-5499716547) **RyanCavanaugh** stated that the issue was covered by #24996 requesting duplicate JSDoc diagnostics for annotations in separate locations and noted that the original example still lacked a diagnostic for v in TS 3.4.5 or 7.1.0-dev.20260901.1 while v2 reported TS1223
 * **RyanCavanaugh** added label `Needs Human Review`
 * (3 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#30669](https://github.com/microsoft/TypeScript/issues/30669) (Closed, `Bug`, `Domain: lib.d.ts`)

**event argument has no target\.result property on  IDBRequest: success event**

*TypeScript's IDBRequest event definitions omit the result property on event.target, causing errors in onsuccess handlers.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/30669#issuecomment-5500171093) **RyanCavanaugh** noted that the issue duplicated #28293 and reproduced TS2339 for event.target.result in TypeScript dev builds
 * **RyanCavanaugh** added label `Needs Human Review`
 * (3 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#30693](https://github.com/microsoft/TypeScript/issues/30693) (Closed, `Bug`, `Fixed`, `Domain: JS Emit`)

**If not all sources are under rootDir, you only get an error message when combined with outDir, not with outFile**

*Compiling with --outFile causes TypeScript to ignore rootDir and not error on files outside it, causing incorrect AMD outputs.*

 * (3 weeks ago) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (3 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#30708](https://github.com/microsoft/TypeScript/issues/30708) (Closed, `Bug`, `Fixed`, `Domain: Conditional Types`)

**Nested conditional type with generic tuple argument always expands to false branch\.**

*Generic nested conditional types comparing tuples in TypeScript 3.4 wrongly collapse to the false branch instead of preserving dependency.*

 * (3 weeks ago) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (3 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#31066](https://github.com/microsoft/TypeScript/issues/31066) (Closed, `Bug`, `Fixed`, `Domain: lib.d.ts`)

**Compiling async/await to ES5 may fail to warn about missing Promise constructor**

*When targeting ES5, async/await compilation in TypeScript does not error for missing Promise constructor, causing runtime failures.*

 * (3 weeks ago) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (3 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#31426](https://github.com/microsoft/TypeScript/issues/31426) (Open, `Bug`, `Domain: classes`)

**\[3\.5\.0\-dev\.20190516\] Incorrect type error for mixin**

*Using interface-based mixin notation in TypeScript incorrectly reports type errors for property usage in mixin methods.*

 * **jakebailey** removed label `Fix Available`
 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/31426#issuecomment-5509068107) **RyanCavanaugh** explained that the TS2339 error no longer occurs in TypeScript 7.1.0-dev.20260902.1 and is replaced by TS7023 and TS2310 due to a circular Quark mixin declaration, and noted that circularity errors may occur
 * **RyanCavanaugh** added label `Needs Human Review`
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#31549](https://github.com/microsoft/TypeScript/issues/31549) (Open, `Bug`, `Domain: Indexed Access Types`)

**Regression: Type T\[K\] as an array when sliced loses its type**

*TypeScript 3.4.5 regresses by losing the specific T[K] type when slicing a generic array property.*

 * **RyanCavanaugh** added label `Domain: Indexed Access Types`
 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/31549#issuecomment-5509559852) **RyanCavanaugh** explained that the assignment is unsound because slice returns a plain U[] which may not satisfy the original T[K] subtype, referencing the generic-constraint rule and TS2322 diagnostic
 * **RyanCavanaugh** added label `Needs Human Review`
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#31613](https://github.com/microsoft/TypeScript/issues/31613) (Closed, `Bug`, `Needs Proposal`, `Domain: check: Control Flow`)

**Type narrowing not working for unions of tuples with object literals**

*TypeScript does not narrow unions of tuples containing object literals based on discriminant property checks.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/31613#issuecomment-5509999155) **RyanCavanaugh** marked the issue as a duplicate of #18758 and explained that tuple positions versus named outer properties do not affect the control-flow narrowing limitation for nested discriminants
 * **RyanCavanaugh** added label `Needs Human Review`
 * (3 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#32111](https://github.com/microsoft/TypeScript/issues/32111) (Closed, `Bug`, `Needs More Info`, `Crash`, `Domain: Performance`)

**Language service OOM on lodash DT tests when batch compilation succeeds**

*Language service operations for lodash DefinitelyTyped tests cause out-of-memory errors even though batch compilation succeeds.*

 * (3 weeks ago) **RyanCavanaugh** added labels `Needs Human Review`, `Needs More Info`
 * (2 weeks ago) **andrewbranch** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#32210](https://github.com/microsoft/TypeScript/issues/32210) (Closed, `Bug`, `Domain: lib.d.ts`)

**MediaQueryList\.prototype\.addListener & removeListener are marked as deprecated**

*TypeScript deprecates MediaQueryList.addListener and removeListener methods even though they remain supported by the CSS spec.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/32210#issuecomment-5512526735) **RyanCavanaugh** explained that addListener and removeListener remain callable but are correctly marked deprecated in TS 7.1.0-dev and described that DOM declarations reflect platform APIs requiring feature detection for legacy browser support
 * **RyanCavanaugh** added label `Needs Human Review`
 * (3 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#32366](https://github.com/microsoft/TypeScript/issues/32366) (Open, `Bug`, `Domain: JavaScript`)

**JS Typedef merged with default export alias behaves strangely**

*A JSDoc @typedef named 'default' in a JavaScript file causes TypeScript to misinterpret the default import as type-only, erroring on value use.*

 * [7.2 years ago](https://github.com/microsoft/TypeScript/issues/32366#issuecomment-511876421) **sandersn** said "Yep, it's a joke!"
 * [1 month ago](https://github.com/microsoft/TypeScript/issues/32366#issuecomment-5415731469) **RyanCavanaugh** stated that the issue was fixed in current TypeScript and provided diagnostics showing the error in 3.4.5 and its absence in 7.1.0-dev
 * **RyanCavanaugh** added label `Needs Human Review`
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#32435](https://github.com/microsoft/TypeScript/issues/32435) (Closed, `Bug`, `Fixed`, `Domain: lib.d.ts`, `Rescheduled`, **sandersn**)

**The dom\.iterable lib contains many interfaces that should also be in webworker**

*The webworker library currently lacks iterable DOM interfaces like Headers, FormData, and URLSearchParams provided by dom.iterable.*

 * (3 weeks ago) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (3 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#32470](https://github.com/microsoft/TypeScript/issues/32470) (Closed, `Bug`, `Fixed`, `Domain: Parser`)

**should not throw error at \`\.d\.ts\` when \`func\` \+ \`namespace\` has member \`default\`**

*TypeScript throws an error in .d.ts when merging a function and namespace that contains a 'default' member.*

 * (3 weeks ago) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (3 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#32707](https://github.com/microsoft/TypeScript/issues/32707) (Closed, `Bug`, `Fixed`, `Domain: check: Big Unions`)

**Max depth limit does not trigger\. Gives up and resolves type to any**

*Excessive chained generic instantiation bypasses TypeScript’s depth check and defaults deeply nested types to any.*

 * (3 weeks ago) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (3 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#32735](https://github.com/microsoft/TypeScript/issues/32735) (Closed, `Bug`, `Fixed`, `Domain: Conditional Types`)

**Conditional types break with property chaining**

*Recursive conditional type toggling between string and number stops alternating after deep property chaining.*

 * (3 weeks ago) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (3 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#32842](https://github.com/microsoft/TypeScript/issues/32842) (Closed, `Bug`, `Fixed`, `Domain: JSDoc`, `Domain: JavaScript`)

**jsdoc object index signature syntax doesn't instantiate type variables**

*JSDoc’s Object<string, T> index signature syntax doesn’t substitute type parameters whereas the {[s: string]: T} syntax does.*

 * (3 weeks ago) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (3 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#33350](https://github.com/microsoft/TypeScript/issues/33350) (Closed, `Bug`, `Fixed`, `Domain: Declaration Emit`)

**Declaration emit is broken for parameters marked /\* @internal \*/**

*Declaration files incorrectly omit or truncate parameters annotated with /* @internal */, resulting in broken .d.ts signatures.*

 * (3 weeks ago) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (3 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#34162](https://github.com/microsoft/TypeScript/issues/34162) (Closed, `Bug`, `Fixed`, `Domain: check: Error Instability`)

**\-\-noEmitOnError trace has incorrect number of errors**

*Enabling --noEmitOnError causes TypeScript to report two errors instead of one for a single type assignment error.*

 * (3 weeks ago) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (3 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#34846](https://github.com/microsoft/TypeScript/issues/34846) (Closed, `Bug`, `Fixed`, `Domain: tsc -b`)

**Project with project references and outFile fails to build**

*Using project references and outFile in TypeScript causes TS6305 errors indicating referenced output files haven't been built from source.*

 * (3 weeks ago) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (3 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#34860](https://github.com/microsoft/TypeScript/issues/34860) (Closed, `Bug`, `Fixed`, `Domain: Comment Emit`)

**Missing JSDoc description when using arrow functions in \-\-allowJs \+ \-\-declaration**

*Generating declaration files from JavaScript with --allowJs and --declaration omits JSDoc comments on exported arrow functions.*

 * (3 weeks ago) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (3 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#34893](https://github.com/microsoft/TypeScript/issues/34893) (Closed, `Bug`, `Domain: Declaration Emit`, `Domain: JavaScript`)

**Bad \`\.d\.ts\` emit for class expression on \`module\.exports**

*TypeScript's declaration emitter omits exporting a class expression assigned to module.exports.answer, dropping the expected alias in the .d.ts output.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/34893#issuecomment-5444738546) **RyanCavanaugh** noted that the issue was fixed in the 3.7 release line and described how different TypeScript versions emit declaration exports
 * **RyanCavanaugh** added label `Needs Human Review`
 * (3 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#35365](https://github.com/microsoft/TypeScript/issues/35365) (Closed, `Bug`, `Fixed`, `Domain: Module Resolution`)

**Triple slash type reference doesn't use baseUrl/typeRoots**

*Triple slash reference types do not respect baseUrl and typeRoots settings in tsconfig, causing resolution errors.*

 * (3 weeks ago) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (3 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#35374](https://github.com/microsoft/TypeScript/issues/35374) (Closed, `Bug`, `Domain: API`)

**bug \`createTemplateMiddle\(\)\` and \`createTemplateTail\(\)\` do not work with escaped chars**

*createTemplateMiddle and createTemplateTail incorrectly scan raw template spans for ']' rather than '}', causing errors with escaped characters.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/35374#issuecomment-5521437713) **RyanCavanaugh** explained that the issue affects a deprecated pre-TypeScript-7 API no longer maintained
 * **RyanCavanaugh** added label `Needs Human Review`
 * (3 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#35455](https://github.com/microsoft/TypeScript/issues/35455) (Closed, `Bug`, `Help Wanted`, `Effort: Moderate`, `Domain: JSDoc`, **sandersn**)

**JSDocTag width is inconsistent**

*TypeScript’s getWidth returns only the tag name length for JSDocTag but the full comment length for JSDocParameterTag, causing inconsistent widths.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/35455#issuecomment-5521625186) **RyanCavanaugh** explained that the pre-TypeScript-7 JavaScript Compiler API had been superseded by TypeScript 7 API and would no longer be developed
 * **RyanCavanaugh** added label `Needs Human Review`
 * (3 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#35485](https://github.com/microsoft/TypeScript/issues/35485) (Closed, `Bug`, `Fixed`, `Domain: JSDoc`)

**JSDoc optional argument does not generate an error in strict mode**

*JSDoc optional parameters in strict checkJs mode aren’t causing errors for potential undefined property accesses.*

 * (2 weeks ago) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (2 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#35566](https://github.com/microsoft/TypeScript/issues/35566) (Closed, `Bug`, `Domain: Something Else`)

**@types's definition doesn't match its own type**

*An update to @types/power-assert introduced a type mismatch that breaks a global assert declaration in TypeScript.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/35566#issuecomment-5522293674) **RyanCavanaugh** explained that TS2403 arose from duplicate namespace declarations in @types/power-assert, noted the correction in DefinitelyTyped#40903, and recommended removing the redundant global declaration to prevent TS2451
 * **RyanCavanaugh** added label `Needs Human Review`
 * (2 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#35776](https://github.com/microsoft/TypeScript/issues/35776) (Closed, `Bug`, `Fixed`, `Domain: Crashes`)

**Heap of out memory for recursive type**

*Compiling a recursive TypeScript type with over ten nested key parameters exhausts heap memory in versions above 3.4.*

 * (2 weeks ago) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (2 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#35797](https://github.com/microsoft/TypeScript/issues/35797) (Closed, `Bug`, `Fixed`, `Help Wanted`, `Domain: JS Emit`)

**Invalid output emited as the result of javascript file compilation: amd, default export, jsdoc**

*TypeScript’s AMD JavaScript compilation incorrectly prefixes default-exported function property assignments with exports, producing invalid code.*

 * (2 weeks ago) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (2 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#35861](https://github.com/microsoft/TypeScript/issues/35861) (Closed, `Bug`, `Domain: check: Excess Property Checking`)

**Union type checking during assignment fails for boolean and passes for other primitives**

*TypeScript 3.7.2 improperly allows invalid assignments to number|string union types while correctly rejecting boolean|string unions.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/35861#issuecomment-5524468782) **RyanCavanaugh** related the behavior to issue #20863, explained the acceptance of fresh object literals based on known properties in unresolved object-union targets, and noted that the boolean|string case differs due to unit types enabling discrimination
 * **RyanCavanaugh** added label `Needs Human Review`
 * (2 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#35879](https://github.com/microsoft/TypeScript/issues/35879) (Closed, `Bug`, `Fixed`, `Help Wanted`, `Domain: JS Emit`)

**commonjs export binding produces invalid code for increment/decrement in PrefixUnaryExpression**

*TypeScript’s CommonJS export transform fails to parenthesize prefix unary assignments, emitting invalid code like `while (!exports.foo = --foo)`.*

 * (2 weeks ago) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (2 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#35880](https://github.com/microsoft/TypeScript/issues/35880) (Closed, `Bug`, `Fixed`, `Domain: check: Type Inference`)

**ObjectAssignmentRest causes "Property 'foo' does not exist on type '{}'"**

*Object destructuring assignment with rest and default values incorrectly triggers 'Property does not exist' errors.*

 * (2 weeks ago) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (2 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#35901](https://github.com/microsoft/TypeScript/issues/35901) (Closed, `Bug`, `Fixed`, `Domain: Error Messages`)

**Give better error when using private identifier in parameter property**

*Using a private identifier (#prop) in a constructor parameter property triggers multiple misleading errors instead of a focused diagnostic.*

 * (2 weeks ago) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (2 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#35962](https://github.com/microsoft/TypeScript/issues/35962) (Open, `Bug`, `Help Wanted`, `Effort: Moderate`, `Domain: JavaScript`)

**No error for undeclared \#private property in \`\.js\` files**

*Undeclared private field usage (#prop) in .js files lacks error reporting outside of checkJs despite being a syntax error.*

 * **sandersn** unassigned **sandersn**
 * [1 month ago](https://github.com/microsoft/TypeScript/issues/35962#issuecomment-5429427187) **RyanCavanaugh** reported that TS 3.8.0-dev.20200108 accepted test.js without diagnostics but the current native compiler and typescript@next reported error TS1111
 * **RyanCavanaugh** added label `Needs Human Review`
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#36133](https://github.com/microsoft/TypeScript/issues/36133) (Closed, `Bug`, `Fixed`, `Domain: lib.d.ts`)

**No overload expects 5 arguments, but overloads do exist that expect either 5 or 9 arguments \(CanvasRenderingContext2D\.drawImage\)**

*TypeScript reports no overload for CanvasRenderingContext2D.drawImage when using spread syntax with a four-element array and extra parameters*

 * (2 weeks ago) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (2 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#36378](https://github.com/microsoft/TypeScript/issues/36378) (Closed, `Bug`, `Fixed`, `Domain: JSDoc`)

**Jsdoc @this show incorrect type  in inherited method**

*JSDoc @this annotation on a static create method always infers Base instead of preserving subclass types.*

 * (2 weeks ago) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (2 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#36792](https://github.com/microsoft/TypeScript/issues/36792) (Closed, `Bug`, `Fixed`, `Domain: ES Modules`)

**Exported type merged with 'export \* as namespace\.\.\.' only exports type meaning\.**

*Support for merging an exported type with an export * as namespace re-export into a single combined value and type export.*

 * (2 weeks ago) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (2 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#36874](https://github.com/microsoft/TypeScript/issues/36874) (Closed, `Bug`, `Fixed`, `Domain: check: Type Inference`)

**Should be possible to spread \`Parameters\` onto its function**

*TypeScript throws a missing iterator error when spreading a Parameters<F> tuple into a generic function call.*

 * (2 weeks ago) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (2 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#36884](https://github.com/microsoft/TypeScript/issues/36884) (Closed, `Bug`, `Domain: This-Typing`)

**Not performing exhaustiveness checking for this**

*TypeScript doesn’t recognize that ‘this’ becomes never after an instanceof Foo check, causing a missing return error.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/36884#issuecomment-5532859211) **RyanCavanaugh** explained that TS2366 is correct because `this` is a structural constraint and identified the issue as a duplicate of #33481
 * **RyanCavanaugh** added label `Needs Human Review`
 * (2 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#36930](https://github.com/microsoft/TypeScript/issues/36930) (Closed, `Bug`, `Domain: check: Type Inference`)

**If you pass a generic type argument to another generic type, constraints cannot be inferred correctly\.**

*Passing a generic type parameter to another generic type prevents correct constraint inference in TypeScript.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/36930#issuecomment-5533199842) **RyanCavanaugh** noted the issue was a duplicate of #29939 and explained that conditional types remain deferred for unresolved type parameters with constraints as intended
 * **RyanCavanaugh** added label `Needs Human Review`
 * (2 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#37103](https://github.com/microsoft/TypeScript/issues/37103) (Closed, `Bug`, `Domain: Mapped Types`)

**Bug: strictNullChecks \+ object spread \+ computed key**

*TypeScript strictNullChecks does not error when spreading an object and using a computed key assigning undefined to Record<string, string>*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/37103#issuecomment-5533935389) **RyanCavanaugh** identified the issue as a duplicate of another issue concerning computed property in object spread
 * **RyanCavanaugh** added label `Needs Human Review`
 * (2 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#37131](https://github.com/microsoft/TypeScript/issues/37131) (Closed, `Bug`, `Domain: API`, `Domain: Binder`)

**Reference to the function expression identifier in it's body has different symbol**

*In TypeScript 3.8+, running getSemanticDiagnostics causes a function expression’s identifier and its body references to resolve to different symbols.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/37131#issuecomment-5534068063) **RyanCavanaugh** explained that symbol object identity is not guaranteed and recommended using declarations or the language service find-references API, and noted that the TypeScript 6 JavaScript Compiler API is deprecated in favor of the TypeScript 7 API
 * **RyanCavanaugh** added label `Needs Human Review`
 * (2 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#37142](https://github.com/microsoft/TypeScript/issues/37142) (Closed, `Bug`, `Domain: classes`)

**A mixin class must have a constructor with a single rest parameter of type 'any\[\]'\.**

*Nested generic TypeScript mixins trigger error TS2545 stating mixin classes must have a constructor with a single rest parameter of type any[].*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/37142#issuecomment-5534244407) **RyanCavanaugh** marked the issue as a duplicate of #16390 and noted that the generic returned-class case remained the concern
 * **RyanCavanaugh** added label `Needs Human Review`
 * (2 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#37301](https://github.com/microsoft/TypeScript/issues/37301) (Closed, `Bug`, `Fixed`, `Domain: classes`)

**Incorrect codegen and error detection for static property used as computed key in instance property of the same class**

*TypeScript 3.8.3 mishandles using a static class property as a computed instance key, causing compile-time and runtime errors.*

 * (2 weeks ago) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (2 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#37399](https://github.com/microsoft/TypeScript/issues/37399) (Closed, `Bug`, `Domain: JSDoc`)

**Unrecognised JSDoc Namepath**

*JSDoc typedefs using '~' namepaths are unrecognized in TypeScript, resulting in errors and any types.*

 * [1 month ago](https://github.com/microsoft/TypeScript/issues/37399#issuecomment-5430119923) **RyanCavanaugh** noted that the issue was a duplicate of #22158, explained that `testFnB~arg` is a JSDoc namepath rather than a TypeScript qualified type name, and demonstrated that using `testFnB.arg` type-checks correctly with diagnostics reported in TS versions
 * **RyanCavanaugh** added label `Needs Human Review`
 * (1 month ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#37427](https://github.com/microsoft/TypeScript/issues/37427) (Closed, `Bug`, `Fixed`, `Help Wanted`, `Domain: Literal Types`)

**Destructured tuple elements are no longer literals**

*Destructuring a tuple returned by enumerate<Color>() causes its elements to lose literal types and widen to string*

 * (2 weeks ago) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (2 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#37505](https://github.com/microsoft/TypeScript/issues/37505) (Closed, `Bug`, `Fixed`, `Domain: Indexed Access Types`)

**Iteration using for of does not recognize optional arrays in generic mapped types**

*TypeScript incorrectly rejects for-of iteration on a generic optional array with fallback in mapped types*

 * (2 weeks ago) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (2 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#37758](https://github.com/microsoft/TypeScript/issues/37758) (Closed, `Bug`, `Fixed`, `Domain: JSDoc`)

**JSDoc Object\.\<key, value\> Syntax doesn't suport uppercase key type**

*VSCode JSDoc intellisense fails to parse uppercase object key and value types such as Object.<String, Number>.*

 * (2 weeks ago) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (2 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#37842](https://github.com/microsoft/TypeScript/issues/37842) (Closed, `Bug`, `Domain: lib.d.ts`)

**Enhance event type of ServiceWorker \`onstatechange\` listener**

*Adjust TypeScript’s ServiceWorker onstatechange listener declaration so event.target is correctly typed as ServiceWorker instead of EventTarget.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/37842#issuecomment-5444694734) **RyanCavanaugh** marked the issue as a duplicate of microsoft/TypeScript#37841
 * **RyanCavanaugh** added label `Needs Human Review`
 * (3 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#38052](https://github.com/microsoft/TypeScript/issues/38052) (Closed, `Bug`, `Domain: check: Type Inference`)

**Type of function field of union object types not inferred correctly when infer is based on undefined type**

*TypeScript infers a union object's function parameter as any instead of narrowing when its discriminant property is missing.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/38052#issuecomment-5539433901) **RyanCavanaugh** noted that this is the same optional-discriminant contextual typing issue tracked by #31618 and that omitting the optional `false` discriminant leaves the callback parameter typed as `any`
 * **RyanCavanaugh** added label `Needs Human Review`
 * (2 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#38145](https://github.com/microsoft/TypeScript/issues/38145) (Closed, `Bug`, `Fixed`, `Domain: Binder`)

**Generic interface confuses parameter identifier with symbolic property identifier**

*TypeScript reports duplicate identifier errors when a generic type parameter name matches an enum property name in an interface.*

 * (2 weeks ago) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (2 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#38246](https://github.com/microsoft/TypeScript/issues/38246) (Closed, `Bug`, `Domain: JS Emit`)

**Function name not preserved when exported on definition**

*Exporting an arrow function directly causes the compiler to emit an anonymous function, stripping its inferred name and making .name empty.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/38246#issuecomment-5540164453) **RyanCavanaugh** explained that the issue was the same exported-arrow-function naming problem tracked by issue #6433 due to downlevel module emit assigning an anonymous function to an export property preventing name inference
 * **RyanCavanaugh** added label `Needs Human Review`
 * (2 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#38391](https://github.com/microsoft/TypeScript/issues/38391) (Closed, `Bug`, `Help Wanted`, `Domain: API`)

**\`typeChecker\.getTypeArguments\` returns unexpected extra type argument**

*typeChecker.getTypeArguments returns an extra subclass type parameter in addition to the expected generic argument*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/38391#issuecomment-5541281934) **RyanCavanaugh** explained that typeChecker.getTypeArguments was part of a superseded pre-TypeScript-7 API and is no longer actionable
 * **RyanCavanaugh** added label `Needs Human Review`
 * (2 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#38448](https://github.com/microsoft/TypeScript/issues/38448) (Closed, `Bug`, `Fixed`, `Domain: Something Else`)

**Maps are not properly displayed on typescript playground**

*Map objects are rendered as empty objects in the TypeScript Playground console instead of showing their entries.*

 * (2 weeks ago) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (2 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#38700](https://github.com/microsoft/TypeScript/issues/38700) (Closed, `Bug`, `Domain: check: Type Inference`)

**Type is not inferred in an if branch of a user\-defined type guard when object is used for destructuring**

*Destructuring with a rest operator in a user-defined type guard branch isn't recognized as an object type by TypeScript.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/38700#issuecomment-5543733846) **RyanCavanaugh** explained that TreeNode is structurally assignable to RootTreeNode, causing the union to lack disjoint alternatives and trigger TS2700 on object-rest destructuring, and showed how adding `[VALUE]?: never` enforces mutual exclusivity to resolve the error
 * **RyanCavanaugh** added label `Needs Human Review`
 * (2 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#38748](https://github.com/microsoft/TypeScript/issues/38748) (Closed, `Bug`, `Fixed`, `Domain: check: Type Inference`)

**Function parameter that has inferred type has no intellisense in the return , while it has in the rest of the function body**

*Implicit any parameters in a generic TypeScript function do not trigger IntelliSense on returned values while explicit any parameters do.*

 * (2 weeks ago) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (2 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#38838](https://github.com/microsoft/TypeScript/issues/38838) (Closed, `Bug`, `Fixed`, `Domain: lib.d.ts`)

**ElementCSSInlineStyle\.style should not be read\-only**

*TypeScript incorrectly treats ElementCSSInlineStyle.style as read-only, preventing string assignments supported by browsers.*

 * (2 weeks ago) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (2 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#39003](https://github.com/microsoft/TypeScript/issues/39003) (Closed, `Bug`, `Help Wanted`, `Domain: lib.d.ts`)

**HTMLFormControlsCollection namedItem should return only form input elements**

*TypeScript’s HTMLFormControlsCollection.namedItem method is incorrectly typed to return generic Element instead of specific form control types.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/39003#issuecomment-5545683323) **RyanCavanaugh** explained that HTMLFormControlsCollection can include form-associated custom elements without a value property, making removal of Element unsound, and advised narrowing to specific element types before accessing value
 * **RyanCavanaugh** added label `Needs Human Review`
 * (2 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#39075](https://github.com/microsoft/TypeScript/issues/39075) (Closed, `Bug`, `Fixed`, `Domain: check: Type Inference`)

**Unable to cast to generic discriminated union**

*Casting a generic discriminated union in TypeScript 3.9.5 fails with TS2352 despite working in 3.8.3.*

 * (2 weeks ago) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (2 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#39133](https://github.com/microsoft/TypeScript/issues/39133) (Closed, `Bug`, `Domain: check: Type Inference`)

**Fails type check for type unions as keys to the Map constructor**

*TypeScript rejects Map<A|B,V> constructor calls when entry arrays contain both union key types.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/39133#issuecomment-5547164151) **RyanCavanaugh** explained the heterogeneous Map constructor inference limitation, referenced microsoft/TypeScript#37527, and recommended using explicit constructor type arguments or annotating an intermediate tuple array
 * **RyanCavanaugh** added label `Needs Human Review`
 * (2 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#39197](https://github.com/microsoft/TypeScript/issues/39197) (Closed, `Bug`, `Fixed`, `Domain: JS Emit`)

**duplicate Object\.defineProperty when code emit with re\-export a rename**

*TypeScript emits duplicate Object.defineProperty calls when re-exporting a renamed import from the same module*

 * (2 weeks ago) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (2 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#39500](https://github.com/microsoft/TypeScript/issues/39500) (Closed, `Bug`, `Fixed`, `Domain: Error Messages`)

**Unmet parameter type in function call is misleading the compiler when those parameters involve inherited interfaces**

*The compiler incorrectly highlights a type mismatch in generic inherited-interface arguments instead of reporting the missing param4 property.*

 * (2 weeks ago) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (2 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#39520](https://github.com/microsoft/TypeScript/issues/39520) (Open, `Bug`, `Domain: Comment Emit`)

**Head comments are removed in some cases for next \`import\` line**

*TypeScript's compiler erroneously removes head comments preceding import statements when emitting JavaScript output.*

 * **RyanCavanaugh** added label `Domain: Comment Emit`
 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/39520#issuecomment-5548509341) **RyanCavanaugh** explained that TypeScript removes imports used only as types and does not guarantee comment preservation, and recommended using a specialized emit tool for exact comment retention
 * **RyanCavanaugh** added label `Needs Human Review`
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#39592](https://github.com/microsoft/TypeScript/issues/39592) (Closed, `Bug`, `Domain: check: Type Inference`)

**Incorrect type allowed in returned object **

*Optional p1 and p2 properties in the return disable type-checking for p4, letting it accept a number.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/39592#issuecomment-5548627990) **RyanCavanaugh** explained that the issue is a duplicate of #36945 and clarified how excess-property checking works for union types
 * **RyanCavanaugh** added label `Needs Human Review`
 * (2 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#39600](https://github.com/microsoft/TypeScript/issues/39600) (Closed, `Bug`, `Domain: check: Type Inference`)

**\`void\` parameter type produced from generic inference doesn't allow skipping as argument**

*Generic void parameter types incorrectly require arguments, unlike explicit void parameters which can be omitted.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/39600#issuecomment-5548732896) **RyanCavanaugh** explained that the generic void parameter-skipping behavior was tracked in #29131 and that a directly written void parameter may be omitted while a void type via generic or indexed access remains required
 * **RyanCavanaugh** added label `Needs Human Review`
 * (2 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#39650](https://github.com/microsoft/TypeScript/issues/39650) (Closed, `Bug`, `Domain: JSDoc`, `Has Repro`)

**In JSDoc @type is not a type declaration, which it is much more like type conversion\.**

*JSDoc @type acts as a type conversion rather than a declaration, preventing errors for extra object properties.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/39650#issuecomment-5549046661) **RyanCavanaugh** corrected the typo in the typedef name and confirmed that fixing it reproduces the expected error in TypeScript 4.0.2 and the current compiler
 * **RyanCavanaugh** added label `Needs Human Review`
 * (2 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#39811](https://github.com/microsoft/TypeScript/issues/39811) (Closed, `Bug`, `Fixed`, `Rescheduled`, `Domain: check: Error Instability`, **weswigham**)

**tsc reports error that LS does not**

*TypeScript's CLI build reports errors in SendThreadMachine.ts that the editor's language service does not surface when using tsconfig.build.json.*

 * (2 weeks ago) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (2 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#39829](https://github.com/microsoft/TypeScript/issues/39829) (Closed, `Bug`, `Domain: lib.d.ts`, **RyanCavanaugh**, **Copilot**)

**HTMLImageElement\#crossOrigin should use literal union type from allowable values**

*HTMLImageElement.crossOrigin property should use the literal union type 'anonymous' | 'use-credentials' instead of string|null.*

 * (2 weeks ago) **RyanCavanaugh** assigned to **Copilot**, **RyanCavanaugh**
 * (5 days ago) **github-actions[bot]** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#39918](https://github.com/microsoft/TypeScript/issues/39918) (Closed, `Bug`, `Fixed`, `checkJs`, `Domain: JavaScript`)

**Bogus "duplicate identifier" when checking JS code**

*Using allowJs and checkJs with a JSDoc-imported interface in JS incorrectly triggers a duplicate identifier error for the uploads property.*

 * (2 weeks ago) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (2 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#39948](https://github.com/microsoft/TypeScript/issues/39948) (Closed, `Bug`, `Fixed`, `Domain: enum`)

**\`in\` doesn't play good with enum**

*TypeScript's 'in' operator does not properly handle enum-defined keys for property checking and type narrowing.*

 * (2 weeks ago) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (2 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#39991](https://github.com/microsoft/TypeScript/issues/39991) (Closed, `Bug`, `Fixed`, `Help Wanted`, `Effort: Moderate`, `Domain: Error Messages`)

**\[feature request\] Better error messages for decorators \(they are completely not understandable\)**

*Improve TypeScript’s TS1240 decorator error message to clearly indicate when decorator descriptor parameters must be optional.*

 * (2 weeks ago) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (2 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#40081](https://github.com/microsoft/TypeScript/issues/40081) (Closed, `Bug`, `Domain: Conditional Types`)

**Nested conditional type inconsistently causes error with annotations**

*Variable annotations in nested conditional types cause T to be inferred as an array union instead of the element type.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/40081#issuecomment-5551039359) **RyanCavanaugh** noted that the issue demonstrated the same nested conditional-type inference behavior as reported in issue #39409 and requested to track it there
 * **RyanCavanaugh** added label `Needs Human Review`
 * (2 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#40205](https://github.com/microsoft/TypeScript/issues/40205) (Closed, `Bug`, `Fixed`, `Domain: Conditional Types`)

**Wrong function parameters length computing**

*TypeScript ignores parameter lists computed with conditional spread operators, causing incorrect function arity validation.*

 * (2 weeks ago) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (2 weeks ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

