# Report for 2026-09-05 (Saturday, September 5th, 2026)

8 different users commented on 28 different issues.

## Recommended Actions

 * Response Recommended
    * @stavalfi-oasis asked if memory leaks would be fixed in [microsoft/TypeScript#63703](https://github.com/microsoft/TypeScript/issues/63703#issuecomment-5553421244)

## Activity Summary

### [Issue microsoft/TypeScript#41065](https://github.com/microsoft/TypeScript/issues/41065) (Closed, `Bug`, `Domain: check: Type Inference`, `Needs Human Review`)

**Default generic type is improperly constrained in conditional types\.**

*The compiler incorrectly infers a default generic as never instead of number when used in conditional type constraints.*

 * [5.9 years ago](https://github.com/microsoft/TypeScript/issues/41065#issuecomment-707681568) **RyanCavanaugh** noted that the issue shouldn't happen but was hard to diagnose without a reproduction case free of undefined behavior and that they wouldn't allocate time to fix it without such a repro
 * [5.9 years ago](https://github.com/microsoft/TypeScript/issues/41065#issuecomment-707851124) **DavidANeil** resolved the issue by writing a different IsNullable implementation without UnionToIntersection and shared the final solution
 * **RyanCavanaugh** added label `Domain: Type Inference`
 * [today](https://github.com/microsoft/TypeScript/issues/41065#issuecomment-5553301257) **RyanCavanaugh** explained that generic defaults are only used when inference can’t choose a candidate, described how contextual inference selected never in the example, and noted the helper-specific issue was resolved
 * **RyanCavanaugh** added label `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#41268](https://github.com/microsoft/TypeScript/issues/41268) (Closed, `Bug`, `Fixed`, `Help Wanted`, `Domain: Error Messages`, `Needs Human Review`)

**Not all leading tab characters in diagnostic messages are replaced with spaces**

*Default TypeScript error diagnostics only replace the first leading tab with a space, resulting in excessive indentation.*

 * (5.8 years ago) **RyanCavanaugh** added labels `help wanted`, `Domain: Error Messages`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/41268#issuecomment-5554758421) **RyanCavanaugh** described that PR #42649 fixed the tab rendering issue in specified TypeScript versions and provided related commit references
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#41515](https://github.com/microsoft/TypeScript/issues/41515) (Closed, `Bug`, `Fixed`, `Domain: tslib and Helper Functions`, `Needs Human Review`)

**importHelpers \+ module: es2015/esnext emits unused helper imports**

*Using importHelpers with ES2015 modules and downlevelIteration incorrectly imports unused tslib helpers, such as __read.*

 * (5.8 years ago) **RyanCavanaugh** added labels `Bug`, `Domain: tslib and Helper Functions`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/41515#issuecomment-5555442076) **RyanCavanaugh** described the fix in PR #41523 and observed that 4.2.0-dev.20210105 emitted an unused tslib import while 4.2.0-dev.20210106 corrected it
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#41530](https://github.com/microsoft/TypeScript/issues/41530) (Closed, `Bug`, `Fixed`, `Domain: check: Control Flow`, `Needs Human Review`)

**Type discrimination broken on generic, mapped type values when \`strictNullChecks:false\`**

*With strictNullChecks disabled, TypeScript cannot narrow function versus string values in a generic mapped type.*

 * [5.6 years ago](https://github.com/microsoft/TypeScript/issues/41530#issuecomment-764471733) **dragomirtitian** argued that in the generic case the `instanceof` behavior was wrong and provided a TypeScript example with a Playground link
 * [5.5 years ago](https://github.com/microsoft/TypeScript/issues/41530#issuecomment-780375143) **turtleflyer** provided another TypeScript sample demonstrating an error when calling a conditional function type
 * **RyanCavanaugh** added label `Domain: Control Flow`
 * [today](https://github.com/microsoft/TypeScript/issues/41530#issuecomment-5555595447) **RyanCavanaugh** reported that the strictNullChecks: false mapped-type example emitted TS2349 through 4.3.0-dev.20210319 and was fixed in commit 15fae38b while its parent still reported TS2349, and clarified that the runIfFunction<T> example is a separate case
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#41672](https://github.com/microsoft/TypeScript/issues/41672) (Closed, `Bug`, `Fixed`, `Domain: Declaration Emit`, `Needs Human Review`)

**TS JSDoc visibility error**

*Using InstanceType<BaseFactory['Base']> in JSDoc triggers a TS9006 private name visibility error.*

 * **sandersn** unassigned **sandersn**
 * [2 years ago](https://github.com/microsoft/TypeScript/issues/41672#issuecomment-2303803072) **Ethan-Arrowood** reported a TS9006 error when extending EventEmitter without a constructor and observed adding one resolved it but considered the behavior unexpected
 * **RyanCavanaugh** added label `Domain: Declaration Emit`
 * [today](https://github.com/microsoft/TypeScript/issues/41672#issuecomment-5555929371) **RyanCavanaugh** described fixes to JSDoc declaration-emit behavior, including updated error reporting from TS9006 to TS1340, use of typeof import for typedefs, corrected @param forms, EventEmitter subclass declarations, and referenced PR #41760
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#41770](https://github.com/microsoft/TypeScript/issues/41770) (Closed, `Bug`, `Has Repro`, `Domain: classes`, `Needs Human Review`)

**Error when trying to assign a subclass of a base class with generics to \`typeof\` of that base class**

*TypeScript rejects assigning a generic subclass to typeof its base class with a type error that’s silenced by adding a redundant constructor overload.*

 * [5.7 years ago](https://github.com/microsoft/TypeScript/issues/41770#issuecomment-737546978) **RyanCavanaugh** said "There are other ways to do it, but that's probably the best one."
 * [4.4 years ago](https://github.com/microsoft/TypeScript/issues/41770#issuecomment-1098572794) **typescript-bot** provided repro bot results showing a deprecation error TS5107 for moduleResolution=node10
 * **RyanCavanaugh** added label `Domain: classes`
 * [today](https://github.com/microsoft/TypeScript/issues/41770#issuecomment-5556009949) **RyanCavanaugh** explained that both assignments should error due to the generic constructor type and recommended using an intermediate class for a common constructor type
 * **RyanCavanaugh** added label `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#41778](https://github.com/microsoft/TypeScript/issues/41778) (Closed, `Bug`, `Fixed`, `Help Wanted`, `Domain: Conditional Types`, `Experimentation Needed`, `Needs Human Review`)

**Generic type sometimes returns never instead of actual template parameter type**

*Classify generic type incorrectly returns never for enum comparisons in TypeScript 3.6 and later.*

 * [5.5 years ago](https://github.com/microsoft/TypeScript/issues/41778#issuecomment-797500440) **MaximeKjaer** provided a minimized bug reproduction demonstrating unexpected conditional type behavior
 * [4.2 years ago](https://github.com/microsoft/TypeScript/issues/41778#issuecomment-1134648051) **jcalz** suggested that the issue duplicated or related to #21998 and asked why the intersection of an enum and its wider literal just be the enum, especially for string enums
 * **RyanCavanaugh** added label `Domain: Conditional Types`
 * [today](https://github.com/microsoft/TypeScript/issues/41778#issuecomment-5556098111) **RyanCavanaugh** noted that the numeric-enum assignability issue was fixed in 5.0.0-dev.20221117 by PR #51561 and that the string-enum case was separately addressed in later versions
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#41797](https://github.com/microsoft/TypeScript/issues/41797) (Closed, `Bug`, `Domain: check: Control Flow`, `Needs Human Review`)

**Incorrect any type distilled from extended generic after typeof check**

*TypeScript incorrectly infers item.id as any after an instanceof check on a generically typed class with an extra property.*

 * [4.5 years ago](https://github.com/microsoft/TypeScript/issues/41797#issuecomment-1030853972) **yuvalbl** asked for updates on the issue and provided a simplified repro scenario
 * [3.3 years ago](https://github.com/microsoft/TypeScript/issues/41797#issuecomment-1518247512) **kevincox** said "This appears to be a duplicate of https://github.com/microsoft/TypeScript/issues/17253"
 * **RyanCavanaugh** added label `Domain: Control Flow`
 * [today](https://github.com/microsoft/TypeScript/issues/41797#issuecomment-5556113612) **RyanCavanaugh** marked the issue as duplicate of #17253 and explained that instanceof narrows a generic class constructor with any type parameters, causing members like DropdownItem.id to become any
 * **RyanCavanaugh** added label `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#41935](https://github.com/microsoft/TypeScript/issues/41935) (Closed, `Bug`, `Fixed`, `Domain: Error Messages`, `Needs Human Review`)

**Incorrect error message when referencing non\-existent type**

*TypeScript incorrectly reports missing exported members when JSDoc annotations reference non-existent nested types or properties.*

 * (5.7 years ago) **RyanCavanaugh** added labels `Bug`, `Domain: Error Messages`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/41935#issuecomment-5556142715) **RyanCavanaugh** described that the incorrect TS2694 errors for foo.bar.I.y and I.x were resolved in 4.5.0-dev.20210904 via PR #45354 (commit 1d51dfa), and that later builds correctly report TS2713 for those accesses and TS2694 for foo.bar.X
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#42079](https://github.com/microsoft/TypeScript/issues/42079) (Closed, `Bug`, `Fixed`, `Domain: Declaration Emit`, `Rescheduled`, `Needs Human Review`, **weswigham**)

**Syntax error in emitted declaration's generic arguments**

*Declaration emit incorrectly uses the generic type parameter T in the nested constant, causing a TS2304 error*

 * (2.2 years ago) **weswigham** set milestone to `Backlog`, and removed from milestone `TypeScript 5.5.0`
 * **jakebailey** removed label `Fix Available`
 * [today](https://github.com/microsoft/TypeScript/issues/42079#issuecomment-5556345054) **RyanCavanaugh** reported that TS 7.1.0-dev emitted nested as PublicWrap<{ foo: number; }, {}> with concrete hover info, whereas TS 4.2.0-dev and 6.0.3 emitted PublicWrap<T, {}> causing a TS2304 error for T
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#42153](https://github.com/microsoft/TypeScript/issues/42153) (Closed, `Bug`, `Domain: API`, `Domain: Parser`, `Needs Human Review`)

**Boolean literal should be LiteralExpression**

*isLiteralExpression fails to recognize boolean literal nodes TrueLiteral and FalseLiteral as LiteralExpression*

 * (5.6 years ago) **andrewbranch** added label `Bug`, and set milestone to `Backlog`
 * **RyanCavanaugh** added label `Domain: Parser`
 * [today](https://github.com/microsoft/TypeScript/issues/42153#issuecomment-5556403406) **RyanCavanaugh** clarified that isLiteralExpression is part of the pre-TypeScript-7 API, that parsing true yields a TrueKeyword on which isLiteralExpression returns false in TS 4.1.0-beta and 6.0.3, and distinguished this from related issues
 * **RyanCavanaugh** added label `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#42172](https://github.com/microsoft/TypeScript/issues/42172) (Closed, `Bug`, `Fixed`, `Domain: JSDoc`, `Needs Human Review`)

**Assertion call error for property typed via JSDoc qualified name**

*The TypeScript compiler erroneously rejects assertion calls on JSDoc-typed properties for missing explicit type annotations.*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [2.7 years ago](https://github.com/microsoft/TypeScript/issues/42172#issuecomment-1866585208) **opiation** described that explicit JSDoc type annotations did not resolve the error and provided code examples, a workaround, and a playground link
 * **RyanCavanaugh** added label `Domain: JSDoc`
 * [today](https://github.com/microsoft/TypeScript/issues/42172#issuecomment-5556712267) **RyanCavanaugh** noted that the issue was fixed in the native compiler and detailed version-specific repro results, and clarified that issue #42174 involves a separate @this JSDoc path
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#42174](https://github.com/microsoft/TypeScript/issues/42174) (Closed, `Bug`, `Fixed`, `Domain: JSDoc`, `Needs Human Review`)

**Assertion call error with JSDoc '@this' tag**

*TypeScript ignores JSDoc @this tags when inferring assertion methods, causing an erroneous "Assertions require every name in the call target to be declared with an explicit type annotation" error.*

 * (5.6 years ago) **RyanCavanaugh** added labels `Bug`, `Domain: JSDoc`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/42174#issuecomment-5556837089) **RyanCavanaugh** explained that the issue was fixed in current native TypeScript, described the error codes in various versions, showed the explicit receiver type in declaration emit, and clarified separation from another issue
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#42214](https://github.com/microsoft/TypeScript/issues/42214) (Closed, `Bug`, `Fixed`, `Help Wanted`, `Domain: classes`, `Needs Human Review`)

**'super\.prop' should only be allowed for accessors**

*Restrict super.property access in TypeScript to actual accessors and disallow it for regular data properties.*

 * [5.2 years ago](https://github.com/microsoft/TypeScript/issues/42214#issuecomment-863567506) **pbrennand-francis** explained that they spent a long time debugging this issue in Angular development and suggested having the compiler catch the error
 * (4.5 years ago) **RyanCavanaugh** added labels `Help Wanted`, `Domain: classes`
 * [today](https://github.com/microsoft/TypeScript/issues/42214#issuecomment-5557422628) **RyanCavanaugh** described that the issue was fixed in current TypeScript, noting that with --target es2016 super.method and super.accessor are accepted while super.prop reports TS2855, and referenced the relevant PR and commit
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#42283](https://github.com/microsoft/TypeScript/issues/42283) (Closed, `Bug`, `Fixed`, `Help Wanted`, `Domain: JSDoc`, `Needs Human Review`)

**JSDoc \`@template\` generic with promise not resolved with CommonJS Export**

*JSDoc @template generics on Promise-returning functions exported via CommonJS modules aren’t inferred, unlike ESM exports.*

 * **RyanCavanaugh** added label `Domain: JSDoc`
 * [5.4 years ago](https://github.com/microsoft/TypeScript/issues/42283#issuecomment-809033411) **Zzzen** said "Cannot reproduce. Guess it is fixed by chance"
 * [3.7 years ago](https://github.com/microsoft/TypeScript/issues/42283#issuecomment-1342995561) **karlhorky** reported that the issue still persisted due to a missing JSDoc feature and opened a new reproduction issue
 * [later](https://github.com/microsoft/TypeScript/issues/42283#issuecomment-5557945637) **RyanCavanaugh** reported that quick info for CommonJS function exports was fixed in TypeScript 6.0.3 and the current 7.1.0-dev and noted that the object-literal export case is tracked separately
 * (later) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#42383](https://github.com/microsoft/TypeScript/issues/42383) (Closed, `Bug`, `Fixed`, `Domain: check: Type Circularity`, `Needs Human Review`)

**Error inheriting class B from class A that contains a method that takes a parameter of type B and returns this when decorated with multiple mixins**

*Using two mixins on a base class with a method taking and returning the subclass triggers a recursive base type error.*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [5.6 years ago](https://github.com/microsoft/TypeScript/issues/42383#issuecomment-764044852) **RyanCavanaugh** said "This is a true type circularity, but one that we are normally able to handle, so it's weird that this is happening"
 * **RyanCavanaugh** added label `Domain: Type Circularity`
 * [later](https://github.com/microsoft/TypeScript/issues/42383#issuecomment-5558055304) **RyanCavanaugh** reported that the issue was fixed in TypeScript 4.3.0-dev.20210428 and later, referenced the PR and commit, and noted clean compilation in TS 6.0.3 and TS 7.1.0-dev.20260906.1
 * (later) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (later) **RyanCavanaugh** closed the issue
 * [later](https://github.com/microsoft/TypeScript/issues/42383#issuecomment-5559490024) **AlmostBearded** thanked for fixing the issue

### [Issue microsoft/TypeScript#42452](https://github.com/microsoft/TypeScript/issues/42452) (Closed, `Bug`, `Fixed`, `Help Wanted`, `Domain: Parser`, `Needs Human Review`)

**Typescript supports less valid variable names characters than javascript**

*TypeScript incorrectly rejects identifiers containing zero-width non-joiner characters that JavaScript allows, a regression introduced between versions 3.5.1 and 3.6.3.*

 * (5.6 years ago) **RyanCavanaugh** added labels `help wanted`, `Domain: Parser`, and set milestone to `Backlog`
 * [later](https://github.com/microsoft/TypeScript/issues/42452#issuecomment-5558134338) **RyanCavanaugh** noted that the issue was fixed in 5.5.0-dev.20240514, contrasted behavior with 5.5.0-dev.20240513, and linked the relevant PR and commits
 * (later) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#42645](https://github.com/microsoft/TypeScript/issues/42645) (Closed, `Bug`, `Fixed`, `Domain: Declaration Emit`, `Needs Human Review`)

**TS4082, TS4060 occurs in a surprising way**

*TypeScript inconsistently handles identically returning a locally declared class when default-exported, triggering TS4082/TS4060 errors.*

 * [5.5 years ago](https://github.com/microsoft/TypeScript/issues/42645#issuecomment-774707025) **NickHeiner** said "I'm fine with them both being an error. :smile: "
 * [3.4 years ago](https://github.com/microsoft/TypeScript/issues/42645#issuecomment-1493699160) **GaoJuqian** said "This problem also occurs when I use multiple tsconfig.json (tsconfig.node.json) and refer to the includes in the wrong file.🤯"
 * **RyanCavanaugh** added label `Domain: Declaration Emit`
 * [later](https://github.com/microsoft/TypeScript/issues/42645#issuecomment-5558458698) **RyanCavanaugh** noted that PR #49440 also fixed TS4082 errors in named local-class declaration emissions starting in 4.8.0-dev.20220609
 * (later) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#42715](https://github.com/microsoft/TypeScript/issues/42715) (Closed, `Bug`, `Fixed`, `Domain: check: Excess Property Checking`, `Needs Human Review`)

**Incorrect excess property error when assigning to intersected array**

*TypeScript incorrectly infers children as Route[] in intersected types, causing excess property errors on RouteWithTitle items*

 * (5.3 years ago) **sandersn** removed label `Fix Available`, and unassigned **sandersn**
 * **RyanCavanaugh** added label `Domain: Excess Property Checking`
 * [later](https://github.com/microsoft/TypeScript/issues/42715#issuecomment-5558936253) **RyanCavanaugh** detailed the version timeline and PR sequence resolving the TS2322 issue with nested RouteWithTitle
 * (later) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#42793](https://github.com/microsoft/TypeScript/issues/42793) (Closed, `Bug`, `Fixed`, `Help Wanted`, `Domain: Something Else`, `Needs Human Review`)

**Template string literal highlighting breaks on ternary operator with typeof**

*Syntax highlighting in VSCode fails to recognize the closing backtick in template literals that use a ternary operator with typeof.*

 * (5.5 years ago) **RyanCavanaugh** added labels `help wanted`, `Domain: Something Else`, and set milestone to `Backlog`
 * [later](https://github.com/microsoft/TypeScript/issues/42793#issuecomment-5560228547) **RyanCavanaugh** attributed the fix to an upstream TypeScript TextMate grammar change and explained that it allows `?` to terminate the `typeof` grammar context, resolving highlighting issues
 * (later) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#42809](https://github.com/microsoft/TypeScript/issues/42809) (Closed, `Bug`, `Help Wanted`, `Domain: lib.d.ts`, `Needs Human Review`)

**navigator\.share is not always a function**

*TypeScript wrongly assumes navigator.share is always defined rather than optional in unsupported browsers.*

 * [4.7 years ago](https://github.com/microsoft/TypeScript/issues/42809#issuecomment-995372375) **rizadh** said "Ran into the same issue. Discovered that using navigator['share'] instead also works around the Typescript error, at least with my installed version of TypeScript 4.5.3."
 * [4.6 years ago](https://github.com/microsoft/TypeScript/issues/42809#issuecomment-1003123444) **jnastaskin** reported that using navigator['share'] worked around the TypeScript error and expressed thanks
 * [2.3 years ago](https://github.com/microsoft/TypeScript/issues/42809#issuecomment-2096683785) **gettersgetmore** said "or 'share' in navigator"
 * [later](https://github.com/microsoft/TypeScript/issues/42809#issuecomment-5560361179) **RyanCavanaugh** explained that Navigator.share is included in DOM libs by policy once in spec, noted TS2774 due to strictNullChecks, and suggested using a runtime feature check for unsupported browsers
 * **RyanCavanaugh** added label `Needs Human Review`
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#42974](https://github.com/microsoft/TypeScript/issues/42974) (Closed, `Bug`, `Fixed`, `Rescheduled`, `Domain: Crashes`, `Needs Human Review`, **orta**)

**JS and TS language service die on template literal expression**

*VS Code’s TypeScript and JavaScript language service repeatedly crashes when parsing a template literal filter expression containing `${string}`.*

 * (2.1 years ago) **RyanCavanaugh** added label `Domain: Crashes`, set milestone to `TypeScript 5.7.0`, and removed from milestone `TypeScript 5.5.0`
 * [later](https://github.com/microsoft/TypeScript/issues/42974#issuecomment-5559764181) **RyanCavanaugh** explained that PR #41693 fixed infinite recursion in getTypeFacts on pattern template-literal types and that TS 4.2.0-dev.20201127 and later return diagnostics instead of terminating the server
 * (later) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63703](https://github.com/microsoft/TypeScript/issues/63703) (Open, `Planning`)

**TypeScript 7\.1 Iteration Plan**

*Roadmap for TypeScript 7.1 detailing milestones and features across compiler, editor productivity, and performance enhancements.*

 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63703#issuecomment-5520894104) **Flarette** argued that compiler depth limits hinder progress and proposed making them configurable via a flag, citing the Jevons paradox and compute innovation history
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63703#issuecomment-5546345126) **RyanCavanaugh** argued that library authors control declaration file behaviors, leading to unpredictable deep instantiation that degrades type-checking performance and harms the developer experience
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63703#issuecomment-5546478556) **RyanCavanaugh** explained that content mappers aim to move complex meta-programming type inference into a static process to generate faster .d.ts files and suggested SQL/GraphQL parser projects investigate this
 * [today](https://github.com/microsoft/TypeScript/issues/63703#issuecomment-5553421244) **stavalfi-oasis** said "great work thank you!! are you also planning to fix all memory leaks? latest version gets to 30-40+ GB RAM quite often (from vscode)"
 * [today](https://github.com/microsoft/TypeScript/issues/63703#issuecomment-5553473110) **jakebailey** said "Please file an issue if you have something that reproduces."
 * [today](https://github.com/microsoft/TypeScript/issues/63703#issuecomment-5554066590) **earthboundkid** reminded participants to keep comments on-topic and focus on 7.1 progress

### [PR microsoft/TypeScript#64138](https://github.com/microsoft/TypeScript/pull/64138) (Open, `For Uncommitted Bug`, **RyanCavanaugh**, **Copilot**)

**Speed up source map emit for large single\-line object literals**

*Optimize source map emission by caching UTF-16 column calculations to avoid quadratic scanning for large single-line object literals.*

 * (3 days ago) **typescript-automation[bot]** added label `For Uncommitted Bug`, and removed label `For Milestone Bug`
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/64138#issuecomment-5517346468) **jakebailey** said "Interesting, I think we have this same optimization somewhere else? I had thought for this specifically, actually."
 * [today](https://github.com/microsoft/TypeScript/pull/64138#issuecomment-5554242611) **DanielRosenwasser** listed related issues and pull requests

### [Issue microsoft/TypeScript#64154](https://github.com/microsoft/TypeScript/issues/64154) (Open, `Domain: API`, **andrewbranch**)

**\[API\] Redesign client\-side snapshot state model**

*Redesign the client-side snapshot state model to unify overlapping updateSnapshot, createProgram, and virtual filesystem operations into a coherent transition system.*

 * [2 days ago](https://github.com/microsoft/TypeScript/issues/64154#issuecomment-5532599380) **DanielRosenwasser** discussed naming options for the snapshot function and weighed potential misinterpretations
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/64154#issuecomment-5532977627) **DanielRosenwasser** asked whether dirty meant the program was out of date with respect to disk after applying changes
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/64154#issuecomment-5533077334) **DanielRosenwasser** considered whether to expose a program update method without snapshot.update and suggested requiring snapshot.update or returning a [Program, Snapshot] pair
 * **DanielRosenwasser** added label `Domain: API`

### [PR microsoft/TypeScript#64181](https://github.com/microsoft/TypeScript/pull/64181) (Open, `For Milestone Bug`, **gabritto**)

**Disallow 'readonly' modifier in ambient module import attributes types**

*Add TS1558 diagnostic to reject 'readonly' modifiers on import attributes type properties in ambient module declarations.*

 * created by **erantianantha**
 * (today) **typescript-automation[bot]** added label `For Milestone Bug`, and assigned to **gabritto**
 * [today](https://github.com/microsoft/TypeScript/pull/64181#issuecomment-5554336440) **erantianantha** said "@microsoft-github-policy-service agree"

### [Issue microsoft/TypeScript#64182](https://github.com/microsoft/TypeScript/issues/64182) (Open, `Domain: Content Mappers`, **andrewbranch**)

**Allow content\-mappers to return declarations instead of source files**

*Allow TypeScript content mappers to return declaration files (.d.ts, .d.cts, .d.mts) instead of source files to bypass module syntax restrictions.*

 * created by **remcohaszing**

