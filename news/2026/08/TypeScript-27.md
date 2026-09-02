# Report for 2026-08-27 (Thursday, August 27th, 2026)

30 different users commented on 72 different issues.

## Recommended Actions

 * Response Recommended
    * @kebi-gizachew asked if their proposed approach aligned with team expectations in [microsoft/TypeScript#53362](https://github.com/microsoft/TypeScript/issues/53362#issuecomment-5447302599)
    * @NullVoxPopuli asked how to generate declarations for compiled-to-JS code in [microsoft/TypeScript#64053](https://github.com/microsoft/TypeScript/issues/64053#issuecomment-5444506654)
    * @typescript-automation[bot] provided requested performance results in [microsoft/TypeScript#64063](https://github.com/microsoft/TypeScript/pull/64063#issuecomment-5448369410)

## Activity Summary

### [Issue microsoft/TypeScript#13797](https://github.com/microsoft/TypeScript/issues/13797) (Closed, `VS Code Tracked`, `Domain: JSDoc`, `Not a Defect`)

**JSDoc syntax highlight\. Not supported type '\.\.\.\*'**

*VSCode’s JSDoc syntax highlighting doesn’t recognize Google Closure-Type variadic syntax ‘...*’, leaving types and parameter names unhighlighted.*

 * **sandersn** unassigned **sandersn**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/13797#issuecomment-5428529368) **RyanCavanaugh** clarified that TypeScript's JSDoc support uses TypeScript type syntax instead of Closure Compiler-specific grammar and provided an example using a call signature that works in TS 7.1.0-dev with allowJs and checkJs
 * **RyanCavanaugh** added label `Needs Human Review`
 * (today) **RyanCavanaugh** added label `Not a Defect`, and removed labels `Bug`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#18408](https://github.com/microsoft/TypeScript/issues/18408) (Open, `Suggestion`, `Awaiting More Feedback`)

**proposal:symbol enum**

*Add symbol enum syntax to generate enums whose members are unique Symbol values.*

 * [5.9 years ago](https://github.com/microsoft/TypeScript/issues/18408#issuecomment-703174511) **cosmoarunn** suggested an alternative TypeScript implementation for TodoActionTypes and offered a simplified type union
 * [5.8 years ago](https://github.com/microsoft/TypeScript/issues/18408#issuecomment-713130404) **polomsky** shared an improved solution using Symbols for compile-time and runtime enum protection
 * [3.3 years ago](https://github.com/microsoft/TypeScript/issues/18408#issuecomment-1502199442) **alaboudi** suggested representing enum values as Symbols by default to promote better coding standards
 * [today](https://github.com/microsoft/TypeScript/issues/18408#issuecomment-5442548193) **Somnium7** shared a small library called ts-symbol-enum that avoids key name repetition and provided example code and links

### [Issue microsoft/TypeScript#27245](https://github.com/microsoft/TypeScript/issues/27245) (Closed, `Bug`, `Domain: JavaScript`, `Needs Human Review`)

**Mix on inline/external defined properties corrupt javascript intellisense**

*VSCode JavaScript IntelliSense fails to recognize properties added after object creation when the object literal already defines other properties.*

 * **RyanCavanaugh** added to milestone `Future`
 * **sandersn** unassigned **sandersn**
 * **mjbvz** added label `Domain: JavaScript`
 * [today](https://github.com/microsoft/TypeScript/issues/27245#issuecomment-5445210648) **RyanCavanaugh** noted that the current nightly build now includes both existing and added properties in completion after 'test.', contrasting with TypeScript 3.1.1 behavior
 * **RyanCavanaugh** added label `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#27808](https://github.com/microsoft/TypeScript/issues/27808) (Open, `Suggestion`, `In Discussion`)

**Feature Request: "extends oneof" generic constraint; allows for narrowing type parameters**

*Add a 'T extends oneof(A, B, C)' generic constraint to require a type parameter matches at least one specified type.*

 * [44 weeks ago](https://github.com/microsoft/TypeScript/issues/27808#issuecomment-3423305652) **RyanCavanaugh** said "Please don't post enormous AI summaries. Leave that to me 🙂"
 * [44 weeks ago](https://github.com/microsoft/TypeScript/issues/27808#issuecomment-3424718513) **lyle45** asked to repost their implementation without AI-generated content and requested feedback on its merit
 * [44 weeks ago](https://github.com/microsoft/TypeScript/issues/27808#issuecomment-3429568523) **RyanCavanaugh** said "I'm not really sure what you're trying to accomplish with it, so I can't speak to how to better achieve that goal"
 * [today](https://github.com/microsoft/TypeScript/issues/27808#issuecomment-5446557862) **irfanstract** suggested making the simple identifier `oneof` a special marker type with one-of semantics and provided illustrative TypeScript code examples

### [Issue microsoft/TypeScript#29188](https://github.com/microsoft/TypeScript/issues/29188) (Closed, `Design Limitation`)

**Conditional type does not narrow union type**

*TypeScript’s conditional type fails to narrow an Array<any> | Specification union in a recursive Mapping type, causing a type error.*

 * [7.5 years ago](https://github.com/microsoft/TypeScript/issues/29188#issuecomment-459936687) **falsandtru** said "Duplicate of #21937."
 * **RyanCavanaugh** added to milestone `Backlog`
 * [5.6 years ago](https://github.com/microsoft/TypeScript/issues/29188#issuecomment-756301061) **TotallyNotChase** asked if union object types could be narrowed using the 'in' operator for conditional types and provided examples
 * [today](https://github.com/microsoft/TypeScript/issues/29188#issuecomment-5445540101) **RyanCavanaugh** explained that S[key] remains a generic type in the false branch because TypeScript lacks negated-type operations and that only the true branch can track the Specification constraint, referencing relevant FAQ entries
 * (today) **RyanCavanaugh** added labels `Needs Human Review`, `Design Limitation`, and removed labels `Bug`, `Domain: Conditional Types`, `Needs Human Review`
 * [today](https://github.com/microsoft/TypeScript/issues/29188#issuecomment-5445952540) **weswigham** said "Also, just... ref https://github.com/microsoft/TypeScript/pull/63926. "

### [Issue microsoft/TypeScript#29350](https://github.com/microsoft/TypeScript/issues/29350) (Closed, `Bug`, `Domain: Performance`, `Domain: Conditional Types`)

**Exponential compilation slowdown with property accessors and conditional types**

*TypeScript compilation slows exponentially with nested generic property accessor overloads and conditional types*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/29350#issuecomment-5415071249) **RyanCavanaugh** stated that the performance regression was fixed in the current compiler and provided benchmark timings across multiple TypeScript versions
 * **RyanCavanaugh** added label `Needs Human Review`
 * **RyanCavanaugh** removed label `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#31307](https://github.com/microsoft/TypeScript/issues/31307) (Closed, `Bug`, `Domain: JSDoc`, `checkJs`, `Domain: check: Type Inference`)

**Unable to add generic function overload for module default export**

*Module default-export generic overload fails to infer HTMLAnchorElement for tagged template calls, returning HTMLElement.*

 * (7.3 years ago) **weswigham** added labels `Domain: JSDoc`, `Domain: Type Inference`
 * **RyanCavanaugh** added to milestone `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/31307#issuecomment-5445714326) **RyanCavanaugh** said "This works now"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#32367](https://github.com/microsoft/TypeScript/issues/32367) (Open, `Bug`, `Domain: JavaScript`, **sandersn**)

**JS typedef merged with default export class behaves strangely**

*A JSDoc typedef named 'default' merged with a default-export class triggers inconsistent type resolution and errors on value usage.*

 * [2 days ago](https://github.com/microsoft/TypeScript/issues/32367#issuecomment-5415676054) **RyanCavanaugh** mentioned that the issue was fixed in the current nightly and that the default import is now usable as a value without diagnostics
 * **RyanCavanaugh** added label `Needs Human Review`
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/32367#issuecomment-5417803594) **weswigham** noted that the current nightly compiles files without diagnostics despite duplicate type-level default exports and suggested it should report a Duplicate identifier error
 * [today](https://github.com/microsoft/TypeScript/issues/32367#issuecomment-5445732587) **RyanCavanaugh** said "Isn't the bare typedef default just declaring a local non-exported thing named default ? Would be illegal in TS but this isn't TS"
 * [today](https://github.com/microsoft/TypeScript/issues/32367#issuecomment-5445829779) **weswigham** said "typedefs are always exported."

### [Issue microsoft/TypeScript#33708](https://github.com/microsoft/TypeScript/issues/33708) (Closed, `Bug`, `Effort: Difficult`, `Domain: Comment Emit`, `Domain: Declaration Emit`)

**Remove useless \`@‍typedef\` comments in \`declaration\`**

*Remove redundant @typedef JSDoc comments in emitted declarations so only the type alias retains documentation.*

 * **RyanCavanaugh** unassigned **weswigham**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/33708#issuecomment-5429770685) **RyanCavanaugh** explained that comment emission is best-effort, referenced the FAQ entry, and advised using an emit tool for precise comment preservation
 * **RyanCavanaugh** added label `Needs Human Review`
 * **RyanCavanaugh** removed label `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#34893](https://github.com/microsoft/TypeScript/issues/34893) (Closed, `Bug`, `Domain: Declaration Emit`, `Domain: JavaScript`, `Needs Human Review`)

**Bad \`\.d\.ts\` emit for class expression on \`module\.exports**

*TypeScript's declaration emitter omits exporting a class expression assigned to module.exports.answer, dropping the expected alias in the .d.ts output.*

 * (6.8 years ago) **DanielRosenwasser** added labels `Domain: Declaration Emit`, `Domain: JavaScript`
 * **RyanCavanaugh** added to milestone `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/34893#issuecomment-5444738546) **RyanCavanaugh** noted that the issue was fixed in the 3.7 release line and described how different TypeScript versions emit declaration exports
 * **RyanCavanaugh** added label `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#37842](https://github.com/microsoft/TypeScript/issues/37842) (Closed, `Bug`, `Domain: lib.d.ts`, `Needs Human Review`)

**Enhance event type of ServiceWorker \`onstatechange\` listener**

*Adjust TypeScript’s ServiceWorker onstatechange listener declaration so event.target is correctly typed as ServiceWorker instead of EventTarget.*

 * (6.2 years ago) **RyanCavanaugh** added labels `Bug`, `Domain: lib.d.ts`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/37842#issuecomment-5444694734) **RyanCavanaugh** marked the issue as a duplicate of microsoft/TypeScript#37841
 * **RyanCavanaugh** added label `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#40540](https://github.com/microsoft/TypeScript/issues/40540) (Closed, `Bug`, `Domain: Declaration Emit`, `Needs Human Review`)

**Bad declaration emit for CommonJS element\-access export of identifier with space asserts**

*Incorrect generation of TypeScript declaration files for CommonJS element-access exports with spaced identifiers.*

 * (5.9 years ago) **sandersn** added labels `Bug`, `Domain: Declaration Emit`
 * [5.9 years ago](https://github.com/microsoft/TypeScript/issues/40540#issuecomment-692148487) **sandersn** said "Probable workaround for this bad emit: install @types/webidl-conversions."
 * [today](https://github.com/microsoft/TypeScript/issues/40540#issuecomment-5445171947) **RyanCavanaugh** stated that the issue was fixed in the current nightly and provided example outputs from TS 4.0.2 and the nightly
 * **RyanCavanaugh** added label `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#41755](https://github.com/microsoft/TypeScript/issues/41755) (Closed, `Bug`, `Fixed`, `Help Wanted`, `Effort: Moderate`, `Domain: API: Transforms`, `Needs Human Review`)

**Parser does not reject \`await a as any \*\* 1\`**

*Parser fails to reject await a as any ** 1 even though await is disallowed as an exponentiation operand*

 * [5.6 years ago](https://github.com/microsoft/TypeScript/issues/41755#issuecomment-755315688) **jonhue** suggested there was no emit bug, proposed two options to address the inconsistency between `await a ** 2` and `await a as any ** 2`, and asked for feedback
 * [5.6 years ago](https://github.com/microsoft/TypeScript/issues/41755#issuecomment-755448256) **JLHwung** said "@a-tarasyuk @jonhue Note that in TC39 November 2020 meeting we have reached consensus that await x ** 1 is illegal, so current engines (except TS!) are not conforming to the spec."
 * [5.6 years ago](https://github.com/microsoft/TypeScript/issues/41755#issuecomment-755455258) **RyanCavanaugh** described frustration about fixing tricky parser bugs and amusement at spec changing to match behavior
 * [today](https://github.com/microsoft/TypeScript/issues/41755#issuecomment-5445500640) **RyanCavanaugh** explained that the parser diagnostic wasn't expected due to operator grouping and that an emit bug in 4.2.0-dev.20201201 was fixed in the current nightly and native compilers
 * (today) **RyanCavanaugh** added labels `Needs Human Review`, `Fixed`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#41918](https://github.com/microsoft/TypeScript/issues/41918) (Closed, `Bug`, `Help Wanted`, `Effort: Moderate`, `Domain: Error Messages`, `Needs Human Review`)

**Strange error: string is not a string type **

*TypeScript emits a confusing 'string is not a string type' error when iterating strings without downlevelIteration.*

 * [5.7 years ago](https://github.com/microsoft/TypeScript/issues/41918#issuecomment-744014118) **aminpaks** reproduced the error without the flag and asked if it was odd that different settings led to different error messages
 * [5.7 years ago](https://github.com/microsoft/TypeScript/issues/41918#issuecomment-744020832) **aminpaks** asked how to write tests passing arguments and reported getting an unexpected TS2461 error
 * [5.7 years ago](https://github.com/microsoft/TypeScript/issues/41918#issuecomment-744022369) **aminpaks** asked for guidance as a first-time contributor
 * [today](https://github.com/microsoft/TypeScript/issues/41918#issuecomment-5445308222) **RyanCavanaugh** explained that with `--target es5 --lib es2015`, TypeScript 4.1.2 issued TS2569, TypeScript 5.9.3 issued TS2802, and TypeScript 7 dropped support for `--target es5`.
 * **RyanCavanaugh** added label `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#42691](https://github.com/microsoft/TypeScript/issues/42691) (Closed, `Bug`, `Fixed`, `Domain: Declaration Emit`, `Needs Human Review`)

**if tsconfig\.json contains paths section, generated declaration for implicit type uses wrong dynamic import**

*TypeScript emits wrong relative dynamic import paths in generated declaration files when tsconfig.json path mappings are used.*

 * (5.5 years ago) **RyanCavanaugh** added labels `Bug`, `Domain: Declaration Emit`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/42691#issuecomment-5446313292) **RyanCavanaugh** announced that the declaration-emit regression was fixed, noted that lib/mylib.ts required a declare on its bodyless libFunc to avoid TS2391, and reported that 3.1.0-dev.20180721 emits import("mylib") versus 3.1.0-dev.20180724 emits import("../lib/mylib"), and that TypeScript 5.9.3 and the current 7.1.0-dev compilers emit import("mylib") with the equivalent paths configuration
 * (today) **RyanCavanaugh** added labels `Needs Human Review`, `Fixed`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#43441](https://github.com/microsoft/TypeScript/issues/43441) (Closed, `Bug`, `Fixed`, `Domain: JSDoc`, `Needs Human Review`)

**JSDoc @param and @returns types cannot access typeof other @params**

*JSDoc type annotations cannot use typeof references to other @param parameters or in @returns, causing name lookup failures.*

 * [5.4 years ago](https://github.com/microsoft/TypeScript/issues/43441#issuecomment-810594300) **sandersn** said "It's new to me -- those TS types seem weird and undesirable to me, so it's likely that my JS semantics are just wrong compared to TS."
 * [5.4 years ago](https://github.com/microsoft/TypeScript/issues/43441#issuecomment-810600136) **andrewbranch** said "It’s a contrived example. The motivation is basically to avoid repeating verbose types if a later parameter or return type can be expressed in terms of a parameter type."
 * [5.4 years ago](https://github.com/microsoft/TypeScript/issues/43441#issuecomment-810982120) **awerlogus** said "Related: https://github.com/microsoft/TypeScript/issues/43403"
 * [today](https://github.com/microsoft/TypeScript/issues/43441#issuecomment-5446342206) **RyanCavanaugh** reported that the issue no longer reproduced and that TypeScript 4.3.0-dev.20210327 reported TS2304 errors while newer versions accepted the example
 * (today) **RyanCavanaugh** added labels `Needs Human Review`, `Fixed`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#53362](https://github.com/microsoft/TypeScript/issues/53362) (Open, `Suggestion`, `Awaiting More Feedback`)

**Improve string split return type of first array index**

*Propose updating TypeScript’s split method types to return a non-empty tuple when using literal string separators.*

 * [1.2 years ago](https://github.com/microsoft/TypeScript/issues/53362#issuecomment-2943003583) **EzioMercer** provided stricter TypeScript overloads for String.prototype.split when limit is 0 and when separator is a string, including code examples and a playground link
 * [1.2 years ago](https://github.com/microsoft/TypeScript/issues/53362#issuecomment-2943782986) **zardoy** asked EzioMercer to open their version of the PR and lamented that the issue remained annoying
 * [1.2 years ago](https://github.com/microsoft/TypeScript/issues/53362#issuecomment-2947974461) **EzioMercer** said "@zardoy I will try. Why did you dislike my issue?)"
 * [today](https://github.com/microsoft/TypeScript/issues/53362#issuecomment-5447302599) **kebi-gizachew** proposed refining the String.prototype.split overloads in lib.es5.d.ts to improve inference, planned to validate changes with tests, and asked if this approach aligned with team expectations
 * [later](https://github.com/microsoft/TypeScript/issues/53362#issuecomment-5454744138) **zardoy** offered to refine String.prototype.split overloads to improve inference and asked for confirmation

### [Issue microsoft/TypeScript#59729](https://github.com/microsoft/TypeScript/issues/59729) (Closed, `Help Wanted`, `Domain: check: Type Inference`, `Possible Improvement`, `Union Order Dependence`)

**The order of values ​​in a union affects the correct type inference**

*Union member order in subscribe’s payload signature affects correct inference of the handler’s options type.*

 * [1.9 years ago](https://github.com/microsoft/TypeScript/issues/59729#issuecomment-2375321168) **olegdunkan** mentioned that the second approach also worked and guessed that the checker prioritized the second constituent to avoid digging into SkipCheckForWhile<T>, though they could be wrong
 * (1.9 years ago) **RyanCavanaugh** added labels `Union Order Dependence`, `Domain: Type Inference`
 * (later) **dartess** closed the issue

### [Issue microsoft/TypeScript#60927](https://github.com/microsoft/TypeScript/issues/60927) (Closed, `Not a Defect`, **ahejlsberg**)

**\`RangeError: Maximum call stack size exceeded\` Regression in \#52392**

*PR #52392 regression causes a RangeError: Maximum call stack size exceeded when instantiating recursively defined generic types.*

 * (1.6 years ago) **RyanCavanaugh** added label `Domain: Type Circularity`, set milestone to `TypeScript 5.8.0`, and assigned to **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript/issues/60927#issuecomment-5445112237) **ahejlsberg** said "This no longer crashes in TS 7. Both the CLI and the language service produce the "excessively deep and possibly infinite" error."
 * (today) **ahejlsberg** added label `Not a Defect`, and removed labels `Bug`, `Domain: check: Type Circularity`

### [Issue microsoft/TypeScript#62796](https://github.com/microsoft/TypeScript/issues/62796) (Open, `Suggestion`, `Awaiting More Feedback`)

**\`noUncheckedIndexedAccess\` should forbid unsound \`Record\<string, string\>\` → \`Record\<"k", string\>\` coercion**

*TypeScript should forbid unsound coercion from Record<string,string> to Record<'k',string> when noUncheckedIndexedAccess is enabled.*

 * [39 weeks ago](https://github.com/microsoft/TypeScript/issues/62796#issuecomment-3572627590) **jendrikw** said "I only use record types with the value type including undefined: Record. Record works way better (read: stricter) that way."
 * [39 weeks ago](https://github.com/microsoft/TypeScript/issues/62796#issuecomment-3572750326) **andersk** noted that noUncheckedIndexedAccess documentation omitted arrays, provided an out-of-bounds array access test case link, and agreed that enabling the flag helps find unsound indexed code
 * [37 weeks ago](https://github.com/microsoft/TypeScript/issues/62796#issuecomment-3627476213) **jcalz** noted that the issue duplicated #29698 and asked whether fixing #29698 would resolve the problem without touching noUncheckedIndexedAccess
 * [today](https://github.com/microsoft/TypeScript/issues/62796#issuecomment-5446874852) **irfanstract** said "yes, this (and #29698) should be flagged under strict, or strictNullChecks, or noUncheckedIndexedAccess."

### [Issue microsoft/TypeScript#63708](https://github.com/microsoft/TypeScript/issues/63708) (Open, `Possible Improvement`, **ahejlsberg**)

**It is possible to violate generic constraints when distributing union types**

*Distributive union types in TypeScript can bypass generic constraints, allowing invalid B extends A combinations without error.*

 * [today](https://github.com/microsoft/TypeScript/issues/63708#issuecomment-5440619666) **ahejlsberg** explained that conditional types infer `A extends B` in the true branch but cannot express or infer the opposite constraint in the false branch, making this lack of negated types a design limitation
 * (today) **ahejlsberg** added label `Design Limitation`, and removed label `Needs Investigation`
 * [today](https://github.com/microsoft/TypeScript/issues/63708#issuecomment-5447287228) **aweebit** said "@ahejlsberg your comment seems to be an answer to @jcalz's comment. In my original example, the YYY branches are completely irrelevant."
 * [today](https://github.com/microsoft/TypeScript/issues/63708#issuecomment-5447448451) **aweebit** asserted that TypeScript should error when it lacks information to verify a constraint and illustrated an alternative conditional type example
 * [later](https://github.com/microsoft/TypeScript/issues/63708#issuecomment-5453841089) **ahejlsberg** agreed that assumptions made involving distributed A didn't always hold and explained that distributed A should behave as a new type variable extending the non-distributed A, noting naming confusion
 * (later) **ahejlsberg** added label `Possible Improvement`, and removed label `Design Limitation`

### [Issue microsoft/TypeScript#63757](https://github.com/microsoft/TypeScript/issues/63757) (Closed, `API Request`, **andrewbranch**, **Copilot**)

**\[7\.0 API\] \- Accessing name on a jsdoc link that does not have a valid name produces sibling node**

*In TypeScript 7.0’s API, invalid JSDoc link names produce a sibling node instead of undefined.*

 * (6 days ago) **RyanCavanaugh** added label `API Request`, and assigned to **andrewbranch**
 * **andrewbranch** assigned to **Copilot**
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript#63775](https://github.com/microsoft/TypeScript/issues/63775) (Closed, `Not a Defect`, **ahejlsberg**)

**difference in typecheck with 5\.8 \(broken type inference\)**

*TypeScript 5.9 incorrectly reports message.options as possibly undefined in a subscribe callback when using an intersection with {}*

 * [1 year ago](https://github.com/microsoft/TypeScript/issues/63775#issuecomment-5351498470) **birgersp** described encountering a false positive TS18048 error when using parameter properties across packages and provided code examples in version 7.0.0-dev.20250704.1
 * [1 year ago](https://github.com/microsoft/TypeScript/issues/63775#issuecomment-5351498507) **birgersp** observed differing compiled output between tsc and tsgo for a class with a timestamp property and suggested it may not be the same issue
 * [1 year ago](https://github.com/microsoft/TypeScript/issues/63775#issuecomment-5351498532) **jakebailey** said "Not the same issue, no. You're correct to file separately in microsoft/typescript-go#1478."
 * [today](https://github.com/microsoft/TypeScript/issues/63775#issuecomment-5445070419) **ahejlsberg** said "As described above, this is a type ordering issue and TS 6 reports the same error with -stableTypeOrdering."
 * **ahejlsberg** added label `Not a Defect`
 * [later](https://github.com/microsoft/TypeScript/issues/63775#issuecomment-5449475199) **dartess** said "The issue was opened as a potential update issue, and since this is expected behavior, I think it should be closed."
 * (later) **dartess** closed the issue

### [Issue microsoft/TypeScript#63781](https://github.com/microsoft/TypeScript/issues/63781) (Closed, `Working as Intended`, **ahejlsberg**)

**Error on function type that comes from a function declaration that is declared after usage site**

*tsgo reports an error on arr.map when using typeof on a function declared later in a union, unlike TypeScript 5.8.*

 * created by **dragomirtitian**
 * [48 weeks ago](https://github.com/microsoft/TypeScript/issues/63781#issuecomment-5351499011) **jakebailey** said "Surely this is yet another type ordering problem, since symbols are sorted by declaration location and swapping the order will mean the function sorts earlier..."
 * **RyanCavanaugh** assigned to **ahejlsberg**
 * **ahejlsberg** added label `Working as Intended`
 * [today](https://github.com/microsoft/TypeScript/issues/63781#issuecomment-5444964687) **ahejlsberg** said "This is indeed a type ordering issue and TS 6 reports the same error with -stabletypeordering. That said, without -stabletypeordering TS6 throws an assertion, which is interesting."

### [Issue microsoft/TypeScript#63829](https://github.com/microsoft/TypeScript/issues/63829) (Closed, **andrewbranch**)

**Add API to get symbol type that respects the \`exactOptionalPropertyTypes\` option**

*Add a TypeScript API method to retrieve symbol types that respect the exactOptionalPropertyTypes option for mapped types without valueDeclaration.*

 * created by **mrazauskas**
 * **andrewbranch** assigned to **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#63950](https://github.com/microsoft/TypeScript/pull/63950) (Closed, `Author: Team`, `For Uncommitted Bug`, **gabritto**)

**Add \`createProgram\` to API**

*Add a createProgram API to create and evolve TypeScript programs by applying file changes to snapshots and optional old programs.*

 * (6 days ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **gabritto**
 * [today](https://github.com/microsoft/TypeScript/pull/63950#issuecomment-5446808532) **gabritto** said "Leaving the diagnostics file thing for a separate PR."

### [PR microsoft/TypeScript#63956](https://github.com/microsoft/TypeScript/pull/63956) (Closed, `For Uncommitted Bug`, **andrewbranch**)

**\[api\] Add \`\.getNonMissingTypeOfSymbol\(\)\` method**

*Add getNonMissingTypeOfSymbol method to TypeScript checker to retrieve symbol types with exact optional property types*

 * created by **mrazauskas**
 * (6 days ago) **typescript-automation[bot]** added label `For Uncommitted Bug`, and assigned to **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript#63979](https://github.com/microsoft/TypeScript/issues/63979) (Closed, `Out of Scope`, `Docs`)

**Official guidelines to build complex types**

*Proposal to add official TypeScript guidelines detailing supported tips, patterns, and pitfalls for constructing complex type definitions.*

 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63979#issuecomment-5401336118) **snarbles2** suggested hosting a community-maintained resource of advanced techniques and linking it from official docs to enable contributions and track version-specific issues
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63979#issuecomment-5405840236) **denis-migdal** asked whether a website already existed and what requirements TS would have regarding repo ownership, external links, issue triage notifications, and promotion
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63979#issuecomment-5415860403) **DanielRosenwasser** admitted finding the situation a catch-22 and encouraged the user to create their own guide
 * [today](https://github.com/microsoft/TypeScript/issues/63979#issuecomment-5448151349) **typescript-automation[bot]** said "This issue has been marked as "Out of Scope" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-automation[bot]** closed the issue
 * [today](https://github.com/microsoft/TypeScript/issues/63979#issuecomment-5448739708) **denis-migdal** critiqued the bot’s two-day response window as too short and explained being busy

### [Issue microsoft/TypeScript#63982](https://github.com/microsoft/TypeScript/issues/63982) (Closed, `Working as Intended`)

**Regression, TS2304: @template\-tag no longer works with @type\-tag in JSDoc**

*Generic JSDoc functions using @template and @type tags now trigger TS2304 errors after upgrading to TypeScript 7.0.*

 * (2 days ago) **ahejlsberg** added label `Working as Intended`, removed label `Needs Investigation`, and unassigned **sandersn**
 * [today](https://github.com/microsoft/TypeScript/issues/63982#issuecomment-5448151109) **typescript-automation[bot]** said "This issue has been marked as "Working as Intended" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-automation[bot]** closed the issue

### [Issue microsoft/TypeScript#64006](https://github.com/microsoft/TypeScript/issues/64006) (Closed, `Working as Intended`)

**Excess property checking lost through a generic mapped\-type parameter \(regression in 6\.0\)**

*TypeScript 6.0 regression causes generic mapped types to bypass excess property checks for nested object literals containing a valid key.*

 * [2 days ago](https://github.com/microsoft/TypeScript/issues/64006#issuecomment-5413144238) **Andarist** identified that the issue bisected to a TypeScript PR and explained that EPC shouldn't happen in inference contexts because inferred types are intentionally subtypes
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/64006#issuecomment-5416596919) **RyanCavanaugh** expressed agreement and noted that Subset<T, Args> tries to emulate exact types in TS which lacks exact types, making a better definition of f difficult without a useful generic type parameter
 * **RyanCavanaugh** added label `Working as Intended`
 * [today](https://github.com/microsoft/TypeScript/issues/64006#issuecomment-5448150879) **typescript-automation[bot]** said "This issue has been marked as "Working as Intended" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-automation[bot]** closed the issue

### [PR microsoft/TypeScript#64023](https://github.com/microsoft/TypeScript/pull/64023) (Closed)

**Additional generator\-based sync API methods**

*Add strongly-typed generator-based synchronous API methods to facilitate request batching parallel to the async API*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/64023#issuecomment-5425234177) **dragomirtitian** shared a gist of their batching version, asked if composability functions like all and spawn are possible in this PR version, and mentioned potential open-sourcing
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64023#issuecomment-5428495821) **weswigham** described that api.batch is equivalent to runBatch, noted tests are missing and promised to add them along with a Promise.all helper
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64023#issuecomment-5429110699) **weswigham** extracted the 'all' equivalent helper from the generator-running logic and exported it in the sync API, tested user-composed generator functions, added batch-flattening to the 'all' batch request builder, and removed the API-level 'batchRequests' helper from API and moved it to Client
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript#64032](https://github.com/microsoft/TypeScript/pull/64032) (Closed, **andrewbranch**, **Copilot**)

**Fix accessing name on jsdoc link for invalid names**

*In TypeScript 7.0, accessing the name of a JSDoc link tag with an invalid identifier incorrectly returns a sibling node instead of undefined.*

 * (yesterday) **Copilot** assigned to **Copilot**, **andrewbranch**
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64032#issuecomment-5431489667) **andrewbranch** said "@copilot what are you doing. no time to waste. hop to it please"
 * [today](https://github.com/microsoft/TypeScript/pull/64032#issuecomment-5442380004) **andrewbranch** said "@copilot yesterday was not your day. today is a new one full of possibility"
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#64041](https://github.com/microsoft/TypeScript/pull/64041) (Closed, **RyanCavanaugh**, **Copilot**)

**Error on misplaced \`use strict\` directives**

*Introduce errors when 'use strict' directives are placed after executable statements or inside nested blocks.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/64041#issuecomment-5432223859) **RyanCavanaugh** said "@typescript-bot test top1000"
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64041#issuecomment-5432224635) **typescript-automation[bot]** reported that CI jobs started and provided status and results links
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64041#issuecomment-5432871314) **typescript-automation[bot]** reported test results for top 1000 repos showing everything looked good
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#64042](https://github.com/microsoft/TypeScript/pull/64042) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**Content mapper auto import formatting panic**

*Reusing synthesized nodes during content mapping caused formatting crashes, fixed by cloning nodes and refactoring the change tracker.*

 * created by **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#64044](https://github.com/microsoft/TypeScript/pull/64044) (Open, `Author: Team`, `For Milestone Bug`, **jakebailey**)

**Speed up narrowing of literal unions**

*Optimizes narrowing of literal unions, cutting user CPU time from around 11 seconds to under 0.1 second.*

 * created by **jakebailey**
 * [later](https://github.com/microsoft/TypeScript/pull/64044#issuecomment-5454719239) **jakebailey** said "@typescript-bot perf test this faster"
 * [later](https://github.com/microsoft/TypeScript/pull/64044#issuecomment-5454720193) **typescript-automation[bot]** posted an update indicating that CI jobs started and linking to status and results

### [PR microsoft/TypeScript#64045](https://github.com/microsoft/TypeScript/pull/64045) (Closed)

**Delete pr\_owners\.txt**

*Remove the pr_owners.txt file from the repository since it is no longer used.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64046](https://github.com/microsoft/TypeScript/pull/64046) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Flip files from CRLF to LF**

*Convert all repository files except testdata and locale directories to LF line endings for consistency.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/64046#issuecomment-5443173686) **jakebailey** said "Nope, gitattributes does it all"
 * [today](https://github.com/microsoft/TypeScript/pull/64046#issuecomment-5446342051) **jakebailey** reported that gitattributes didn't auto-fix locally created CRLF files and suggested adopting a VS Code setting or adding a task to flip line endings

### [Issue microsoft/TypeScript#64047](https://github.com/microsoft/TypeScript/issues/64047) (Open, `Suggestion`)

**\(Proposal\) more\-sophisticated CFA, and Narrowing Boolean Types**

*Propose enhancements to TypeScript’s control-flow analysis to track type narrowing across indirections and support boolean variables with type-predicate signatures.*

 * created by **irfanstract**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/64047#issuecomment-5433323789) **Irfan-lab700** said "assign"
 * **RyanCavanaugh** added label `Suggestion`
 * [today](https://github.com/microsoft/TypeScript/issues/64047#issuecomment-5441872610) **RyanCavanaugh** asked if the suggestion encompassed multiple features as a single request

### [PR microsoft/TypeScript#64048](https://github.com/microsoft/TypeScript/pull/64048) (Closed)

**Delete defunct GHA workflows**

*Delete obsolete GitHub Actions workflows (LKG, pr-modified-files, release branch artifact) no longer required.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#64049](https://github.com/microsoft/TypeScript/issues/64049) (Closed, `Won't Fix`)

**Erasing a \`const enum\` can emit an illegal \`"use strict"\` directive**

*Erasing a const enum places a string literal first in a default-parameter function, creating an illegal 'use strict' directive.*

 * created by **magic-akari**
 * **RyanCavanaugh** added label `Won't Fix`
 * [today](https://github.com/microsoft/TypeScript/issues/64049#issuecomment-5441731799) **RyanCavanaugh** ran #64041 to check for misplaced `use strict` directives, found none, and emphasized that disabling `use strict` is not acceptable
 * [today](https://github.com/microsoft/TypeScript/issues/64049#issuecomment-5441981277) **magic-akari** suggested that the scan may have missed some cases and provided links to specific test files for review
 * [today](https://github.com/microsoft/TypeScript/issues/64049#issuecomment-5442218368) **magic-akari** said "If TypeScript does not plan to address this, I think we can treat it as unspecified or implementation-dependent behavior, with no canonical interpretation, and close the issue on that basis."

### [Issue microsoft/TypeScript#64050](https://github.com/microsoft/TypeScript/issues/64050) (Open, `Needs Investigation`, **andrewbranch**)

**Content mapper duplicated inlay hints**

*Splitting a statement into multiple spans in the content mapper causes duplicate inlay hints due to separate hint generation for each span.*

 * created by **jasonlyu123**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/64050#issuecomment-5434695975) **scs0209** said "I'd like to work on this. Can I try it?"
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.1`, and assigned to **andrewbranch**

### [Issue microsoft/TypeScript#64053](https://github.com/microsoft/TypeScript/issues/64053) (Open, `Needs Investigation`, **andrewbranch**)

**content\-mapper generates inconsistent declaration extensions, making management of package\.json\#exports hard / verbose**

*Content-mapper generates inconsistent declaration file extensions, complicating package.json exports configuration.*

 * created by **NullVoxPopuli**
 * [today](https://github.com/microsoft/TypeScript/issues/64053#issuecomment-5444127214) **RyanCavanaugh** explained that the filename format was intentional to avoid conflicts when mapping files to .d.ts
 * **RyanCavanaugh** added label `Working as Intended`
 * [today](https://github.com/microsoft/TypeScript/issues/64053#issuecomment-5444506654) **NullVoxPopuli** asked how to generate declarations for compiled-to-JS code when extensions are changed by an external tool
 * [today](https://github.com/microsoft/TypeScript/issues/64053#issuecomment-5444742399) **andrewbranch** questioned how to know that the external build tool transforms avatar.gts to avatar.js rather than avatar.gts.js or avatar.gts/index.js and why it wouldn’t rewrite declaration file imports
 * [today](https://github.com/microsoft/TypeScript/issues/64053#issuecomment-5444861891) **NullVoxPopuli** suggested adding a verbose tsconfig.json declaration setting with extension mappings and an externallyCompiledToJS flag to streamline TS handling across file types
 * [today](https://github.com/microsoft/TypeScript/issues/64053#issuecomment-5444911489) **andrewbranch** asked if other ecosystems shipped 1:1 compiled output like Ember
 * [today](https://github.com/microsoft/TypeScript/issues/64053#issuecomment-5445124761) **NullVoxPopuli** mentioned that MDX faced the same problem and suggested that other ecosystems standardize publishing JS to npm to reduce transpilation work
 * [later](https://github.com/microsoft/TypeScript/issues/64053#issuecomment-5449867169) **remcohaszing** described Ember's and MDX's content-mapped file compilation parallels and proposed TypeScript content mapper configuration to rewrite import extensions

### [PR microsoft/TypeScript#64054](https://github.com/microsoft/TypeScript/pull/64054) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Bump and clean up deps, raise min local node version**

*Bump and clean dependencies, raise minimum Node version to 22.18, and replace several packages with built-in features.*

 * created by **jakebailey**

### [Issue microsoft/TypeScript#64055](https://github.com/microsoft/TypeScript/issues/64055) (Open, `Needs Investigation`, **andrewbranch**)

**debug extension / mode for content\-mapper**

*A debugging mode for content-mapper similar to Volar Labs' tool to diagnose missing completions and hovers in VSCode projects.*

 * created by **NullVoxPopuli**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript/issues/64055#issuecomment-5444199681) **andrewbranch** mentioned having prototyped a feature, ported it into the built-in TS extension, and planned to include it as a first-class feature

### [Issue microsoft/TypeScript#64056](https://github.com/microsoft/TypeScript/issues/64056) (Open, `Bug`, `Domain: Editor/VS Code Extension`, **weswigham**)

**Investigate inconsistencies in editor diagnostic reporting**

*Intermittent flashing of various TypeScript diagnostic codes in the editor occurs due to request ordering inconsistencies.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** added labels `Bug`, `Domain: Editor/VS Code Extension`, set milestone to `TypeScript 7.1.1 RC`, and assigned to **weswigham**
 * [today](https://github.com/microsoft/TypeScript/issues/64056#issuecomment-5444809205) **weswigham** referred to server logs entries from another issue as more immediately actionable and relevant

### [PR microsoft/TypeScript#64057](https://github.com/microsoft/TypeScript/pull/64057) (Open, `For Uncommitted Bug`, **ahejlsberg**, **Copilot**)

**Port \`\-\-enforceReadonly\` to the Go compiler**

*Port TypeScript’s --enforceReadonly feature to the Go compiler by adding the flag, updating CLI and diagnostics, and enforcing readonly constraints.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **ahejlsberg**

### [Issue microsoft/TypeScript#64058](https://github.com/microsoft/TypeScript/issues/64058) (Open, `Bug`)

**TS7: \`@extends\` is ignored when the heritage is a call expression \(Base\.extend\(\)\)**

*TypeScript 7’s JSDoc @extends tag is ignored for classes extending via call expressions (Base.extend()), causing unexpected type argument errors.*

 * created by **NullVoxPopuli**

### [Issue microsoft/TypeScript#64059](https://github.com/microsoft/TypeScript/issues/64059) (Closed, `Bug`, `Domain: Declaration Emit`, **weswigham**)

**Declaration emit drops \`readonly\` from a nested object literal under a \`const\` type parameter \(7\.0\.2, 7\.1\.0\-dev; correct in 6\.0\.3\)**

*TypeScript 7’s declaration output drops readonly modifiers on nested object literal properties under a const type parameter, regressing from version 6.0.3.*

 * created by **SvabhuG**
 * (today) **ahejlsberg** added labels `Bug`, `Domain: Declaration Emit`, set milestone to `TypeScript 7.1`, and assigned to **weswigham**
 * (today) **SvabhuG** closed the issue
 * [today](https://github.com/microsoft/TypeScript/issues/64059#issuecomment-5446830179) **ahejlsberg** said "@SvabhuG Is there a reason you closed this again?"

### [PR microsoft/TypeScript#64060](https://github.com/microsoft/TypeScript/pull/64060) (Closed)

**Enhance jsonvalue\_test\.go with edge case tests**

*Add unit tests for jsonvalueToAny covering empty objects, boolean values, and floating-point numbers to ensure robust parsing.*

 * created by **denizguney**

### [PR microsoft/TypeScript#64061](https://github.com/microsoft/TypeScript/pull/64061) (Open, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Add pagination of batch requests**

*Implement server-side pagination of batch API responses using maxResponseBytesPerPage to prevent JavaScript string size overflows and simplify encoding.*

 * created by **weswigham**

### [Issue microsoft/TypeScript#64062](https://github.com/microsoft/TypeScript/issues/64062) (Closed, `External`)

**LSP causes client to watch thousands of files**

*TypeScript LSP server's file watcher registers a project-wide glob, watching thousands of files and exhausting file descriptors.*

 * created by **CamJN**

### [PR microsoft/TypeScript#64063](https://github.com/microsoft/TypeScript/pull/64063) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Ditch nodeData interface in favor of generated accessors**

*Replacing the dynamic nodeData interface with generated accessors reduces binary size, symbol count, and compile time.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/64063#issuecomment-5448174610) **jakebailey** said "@typescript-bot perf test this"
 * [today](https://github.com/microsoft/TypeScript/pull/64063#issuecomment-5448175071) **typescript-automation[bot]** reported CI jobs started and provided build status and results links
 * [today](https://github.com/microsoft/TypeScript/pull/64063#issuecomment-5448369410) **typescript-automation[bot]** provided the performance comparison report for the requested perf run

### [PR microsoft/TypeScript#64064](https://github.com/microsoft/TypeScript/pull/64064) (Open, `For Backlog Bug`)

**Fix importHelpers incorrectly requiring tslib for native \#private class members \(\#63728\)**

*Remove unnecessary decorator-based gating so native private class members no longer require tslib for ES2022+ targets*

 * created by **YoussefMansour9**

### [Issue microsoft/TypeScript#64065](https://github.com/microsoft/TypeScript/issues/64065) (Closed, `API Request`, **andrewbranch**)

**Add \`TupleTypeReference\` interface to the API**

*Introduce a TupleTypeReference interface to the TypeScript API to enable tuple-specific type handling.*

 * created by **mrazauskas**

### [PR microsoft/TypeScript#64066](https://github.com/microsoft/TypeScript/pull/64066) (Closed, `For Uncommitted Bug`, **andrewbranch**)

**\[api\] Add \`TupleTypeReference\` interface**

*Add missing TupleTypeReference interface to the TypeScript API to support tuple type references.*

 * created by **mrazauskas**

### [Issue microsoft/TypeScript#64067](https://github.com/microsoft/TypeScript/issues/64067) (Closed, `API Request`, **andrewbranch**, **Copilot**)

**\[API\] CompilerOptions references enums that aren't exported, and omits options tsc accepts**

*In TypeScript 7, the public CompilerOptions API references unexported enums (JsxEmit, ModuleResolutionKind) and excludes accepted options like esModuleInterop.*

 * created by **knutwannheden**

### [Issue microsoft/TypeScript#64068](https://github.com/microsoft/TypeScript/issues/64068) (Closed, `API Request`, **andrewbranch**, **Copilot**)

**\[API\] An invalid DocumentIdentifier fails with a TypeError from path\.js rather than a message naming the argument**

*Providing {fileName} instead of a string or {uri} to getSourceFile throws an opaque TypeError rather than a descriptive argument error.*

 * created by **knutwannheden**

### [Issue microsoft/TypeScript#64069](https://github.com/microsoft/TypeScript/issues/64069) (Open, `API Request`, **andrewbranch**)

**\[API\] No module resolution API: no counterpart to ts\.resolveModuleName**

*TypeScript's API lacks a standalone module resolution function equivalent to ts.resolveModuleName, preventing external resolution queries.*

 * created by **knutwannheden**

### [Issue microsoft/TypeScript#64070](https://github.com/microsoft/TypeScript/issues/64070) (Open, `API Request`, **andrewbranch**)

**\[API\] No jsDocParsingMode, and reparsed JSDoc types appear as syntax on the declarations they document**

*TypeScript 7.x API lacks a jsDocParsingMode option and reparses JSDoc types into type annotations, breaking source reproduction and error reporting.*

 * created by **knutwannheden**

### [Issue microsoft/TypeScript#64071](https://github.com/microsoft/TypeScript/issues/64071) (Closed)

**@typescript/old declares a tsc bin that wins over typescript@7 when the 6\.0 compat package is installed**

*@typescript/old declares a tsc bin that shadows TypeScript@7, causing npm scripts to run tsc version 6.*

 * created by **knutwannheden**
 * [later](https://github.com/microsoft/TypeScript/issues/64071#issuecomment-5454115800) **jakebailey** noted that they had no control as transitive dependencies are placed in bin by the package manager and suggested renaming packages to reorder them
 * [later](https://github.com/microsoft/TypeScript/issues/64071#issuecomment-5454198403) **knutwannheden** confirmed that npm's hoisting behavior causes the tsc alias conflict, clarified that renaming the alias doesn't help, and suggested workarounds
 * (later) **knutwannheden** closed the issue
 * [later](https://github.com/microsoft/TypeScript/issues/64071#issuecomment-5454738897) **RyanCavanaugh** said "See also https://github.com/npm/cli/issues/9868 , https://github.com/yarnpkg/berry/issues/7215"

### [PR microsoft/TypeScript#64072](https://github.com/microsoft/TypeScript/pull/64072) (Open, `For Backlog Bug`)

**fix\(64058\): fix reparse jsdoc @extends type arguments for call expressions**

*Corrects the re-parsing of JSDoc @extends type arguments in call expressions.*

 * created by **a-tarasyuk**
 * (later) **a-tarasyuk** closed the issue
 * (later) **a-tarasyuk** reopened the issue

### [Issue microsoft/TypeScript#64073](https://github.com/microsoft/TypeScript/issues/64073) (Closed, `Duplicate`)

**The extends infer for function generics fails\.**

*TypeScript fails to infer conditional extends checks on generic function parameters, causing incorrect type assignments.*

 * created by **vipcxj**
 * [later](https://github.com/microsoft/TypeScript/issues/64073#issuecomment-5451809803) **MartinJohns** explained that resolving conditional types with unbound generics is deferred and noted duplication of issue #23132

### [PR microsoft/TypeScript#64074](https://github.com/microsoft/TypeScript/pull/64074) (Open, `For Backlog Bug`)

**Disallow optional calls on import\.defer**

*Introduce parse errors for optional calls on import.defer, including import.defer?.(...) and generic import.defer?.<T>(...), while preserving valid import.defer(...) calls.*

 * created by **HyeonsangKim**

### [Issue microsoft/TypeScript#64075](https://github.com/microsoft/TypeScript/issues/64075) (Closed, `Working as Intended`)

**Content mappers: let TypeScript send \`transform\` requests in parallel, not to one queue**

*Allow TypeScript to run content mapper transform requests concurrently on multiple processes instead of serializing them on one thread.*

 * created by **johanrd**

