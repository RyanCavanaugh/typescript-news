# Report for 2026-09-02 (Wednesday, September 2nd, 2026)

20 different users commented on 60 different issues.

## Recommended Actions

 * Response Recommended
    * @TedDriggs indicated they changed companies and could not re-create a repro in [microsoft/TypeScript#31667](https://github.com/microsoft/TypeScript/issues/31667#issuecomment-5517413492)
    * @Flarette asked if the team plans to revisit instantiation depth limits in the tsgo compiler in [microsoft/TypeScript#63703](https://github.com/microsoft/TypeScript/issues/63703#issuecomment-5519354895)
    * @Flarette proposed making limits configurable via a compiler flag in [microsoft/TypeScript#63703](https://github.com/microsoft/TypeScript/issues/63703#issuecomment-5520894104)
    * @johnnyreilly provided benchmark results for PR performance across operating systems in [microsoft/TypeScript#63875](https://github.com/microsoft/TypeScript/issues/63875#issuecomment-5522708727)
    * @jacekkopecky asked for clarification on the inconsistency in never return types and suggested revisiting the corner case in [microsoft/TypeScript#63970](https://github.com/microsoft/TypeScript/issues/63970#issuecomment-5516823860)
    * @nstepien provided reproduction steps and noted missing watch mode logging in [microsoft/TypeScript#64037](https://github.com/microsoft/TypeScript/issues/64037#issuecomment-5527566209)
    * @seanxuu asked for confirmation that the target repository is appropriate in [microsoft/TypeScript#64118](https://github.com/microsoft/TypeScript/issues/64118#issuecomment-5521839695)
    * @typescript-automation[bot] provided perf run results as requested in [microsoft/TypeScript#64131](https://github.com/microsoft/TypeScript/pull/64131#issuecomment-5514035269)
    * @valler asked if TS2775 is expected and whether they should close or rename the issue in [microsoft/TypeScript#64136](https://github.com/microsoft/TypeScript/issues/64136#issuecomment-5512758602)

## Activity Summary

### [Issue microsoft/TypeScript#31667](https://github.com/microsoft/TypeScript/issues/31667) (Closed, `Bug`, `Needs More Info`, `Domain: JavaScript`)

**Type narrowing in checked JS in module scope doesn't work**

*In checked JavaScript module scope TypeScript doesn’t apply instanceof type narrowing for variables, although it works inside functions.*

 * [today](https://github.com/microsoft/TypeScript/issues/31667#issuecomment-5510264647) **RyanCavanaugh** couldn't reproduce the reported errors from the provided files and requested the tsconfig.json, any declarations or imports, the exact tsc command, and diagnostics on the guarded calls
 * (today) **RyanCavanaugh** added labels `Needs Human Review`, `Needs More Info`
 * [today](https://github.com/microsoft/TypeScript/issues/31667#issuecomment-5517413492) **TedDriggs** said "I have changed companies since filing this. I no longer have access, and am not inclined to re-create a repro."

### [Issue microsoft/TypeScript#32210](https://github.com/microsoft/TypeScript/issues/32210) (Closed, `Bug`, `Domain: lib.d.ts`, `Needs Human Review`)

**MediaQueryList\.prototype\.addListener & removeListener are marked as deprecated**

*TypeScript deprecates MediaQueryList.addListener and removeListener methods even though they remain supported by the CSS spec.*

 * [5.9 years ago](https://github.com/microsoft/TypeScript/issues/32210#issuecomment-701427252) **robertn702** clarified that TypeScript warns developers against using the old API, defended trusting static typing, and recommended marking addEventListener and removeEventListener as optional properties to balance deprecation notices and usage
 * [5.9 years ago](https://github.com/microsoft/TypeScript/issues/32210#issuecomment-701712114) **Maxim-Mazurok** praised the solution of leaving the deprecation warning and making addEventListener and removeEventListener optional properties
 * **RyanCavanaugh** added label `Domain: lib.d.ts`
 * [today](https://github.com/microsoft/TypeScript/issues/32210#issuecomment-5512526735) **RyanCavanaugh** explained that addListener and removeListener remain callable but are correctly marked deprecated in TS 7.1.0-dev and described that DOM declarations reflect platform APIs requiring feature detection for legacy browser support
 * **RyanCavanaugh** added label `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#32435](https://github.com/microsoft/TypeScript/issues/32435) (Closed, `Bug`, `Fixed`, `Domain: lib.d.ts`, `Rescheduled`, `Needs Human Review`, **sandersn**)

**The dom\.iterable lib contains many interfaces that should also be in webworker**

*The webworker library currently lacks iterable DOM interfaces like Headers, FormData, and URLSearchParams provided by dom.iterable.*

 * (2 years ago) **RyanCavanaugh** added label `Domain: lib.d.ts`, set milestone to `TypeScript 5.7.0`, and removed from milestone `TypeScript 5.5.0`
 * [today](https://github.com/microsoft/TypeScript/issues/32435#issuecomment-5513403610) **RyanCavanaugh** noted that PR #40500 added the separately selectable webworker.iterable library, described how various TypeScript versions handle the command and error, and referenced the origin of the declarations
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#32470](https://github.com/microsoft/TypeScript/issues/32470) (Closed, `Bug`, `Fixed`, `Domain: Parser`, `Needs Human Review`)

**should not throw error at \`\.d\.ts\` when \`func\` \+ \`namespace\` has member \`default\`**

*TypeScript throws an error in .d.ts when merging a function and namespace that contains a 'default' member.*

 * (7.1 years ago) **RyanCavanaugh** added labels `Bug`, `Domain: Parser`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/32470#issuecomment-5513805049) **RyanCavanaugh** fixed the declaration emission issue in TS 4.0.0-dev.20200611 and described the successful export behavior in later versions
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#32707](https://github.com/microsoft/TypeScript/issues/32707) (Closed, `Bug`, `Fixed`, `Domain: check: Big Unions`, `Needs Human Review`)

**Max depth limit does not trigger\. Gives up and resolves type to any**

*Excessive chained generic instantiation bypasses TypeScript’s depth check and defaults deeply nested types to any.*

 * [7 years ago](https://github.com/microsoft/TypeScript/issues/32707#issuecomment-521822889) **AnyhowStep** shared a cleaner version of the hack with links to the implementation and utility type, noted its limitation with union types, and provided an extra test
 * (6.9 years ago) **RyanCavanaugh** added label `Domain: Big Unions`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/32707#issuecomment-5514506135) **RyanCavanaugh** reported that the issue was fixed in TypeScript 3.7.0-dev.20190926 via PR #33050 which defers type-argument resolution and avoids eager recursive expansion, and noted that PR #32611 was closed unmerged and not the fix
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#32735](https://github.com/microsoft/TypeScript/issues/32735) (Closed, `Bug`, `Fixed`, `Domain: Conditional Types`, `Needs Human Review`)

**Conditional types break with property chaining**

*Recursive conditional type toggling between string and number stops alternating after deep property chaining.*

 * (7 years ago) **RyanCavanaugh** added labels `Bug`, `Domain: Conditional Types`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/32735#issuecomment-5514894657) **RyanCavanaugh** reported that #45025 fixed the issue and that version 4.5.0-dev.20210818 and the current nightly no longer report errors
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#32842](https://github.com/microsoft/TypeScript/issues/32842) (Closed, `Bug`, `Fixed`, `Domain: JSDoc`, `Domain: JavaScript`, `Needs Human Review`)

**jsdoc object index signature syntax doesn't instantiate type variables**

*JSDoc’s Object<string, T> index signature syntax doesn’t substitute type parameters whereas the {[s: string]: T} syntax does.*

 * (7 years ago) **sandersn** added label `Domain: JavaScript`, and unassigned **sandersn**
 * [3.5 years ago](https://github.com/microsoft/TypeScript/issues/32842#issuecomment-1444442277) **SamB** shared a Playground testcase demonstrating that variables escape their scope without producing an Internal Compiler Error
 * [today](https://github.com/microsoft/TypeScript/issues/32842#issuecomment-5515201571) **RyanCavanaugh** reported that the issue was fixed in TypeScript 7.1.0-dev.20260902.1 and noted that TypeScript 5.9.3 still emitted TS2322 while the dev build accepted both cases, instantiating Object<string, T> as Object<string, number> for new C(1)
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#33101](https://github.com/microsoft/TypeScript/issues/33101) (Closed, `Bug`, `Fixed`, `Domain: check: Type Inference`)

**Union types and overloads acts a bit weirdly**

*An overloaded method on a Foo|Bar union incorrectly yields string|Bar for a string overload, whereas object returns behave correctly.*

 * [7 years ago](https://github.com/microsoft/TypeScript/issues/33101#issuecomment-525973460) **keithlayne** described overload-ordering quirks in unions and intersections and asked for guidance on the correct overload order
 * [5.5 years ago](https://github.com/microsoft/TypeScript/issues/33101#issuecomment-785010256) **thetutlage** said "Its kind of sad that verified bugs are not getting fixed for years. :("
 * **RyanCavanaugh** added label `Domain: Type Inference`
 * [today](https://github.com/microsoft/TypeScript/issues/33101#issuecomment-5516188277) **RyanCavanaugh** explained that the inference issue was fixed in newer dev versions by PR #55447 and closed the issue
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#33350](https://github.com/microsoft/TypeScript/issues/33350) (Closed, `Bug`, `Fixed`, `Domain: Declaration Emit`, `Needs Human Review`)

**Declaration emit is broken for parameters marked /\* @internal \*/**

*Declaration files incorrectly omit or truncate parameters annotated with /* @internal */, resulting in broken .d.ts signatures.*

 * [7 years ago](https://github.com/microsoft/TypeScript/issues/33350#issuecomment-530063342) **sheetalkamat** explained that the issues were caused by d.ts emission through transform and provided example commands and outputs
 * **RyanCavanaugh** added to milestone `Backlog`
 * [3.9 years ago](https://github.com/microsoft/TypeScript/issues/33350#issuecomment-1248055960) **juanrgm** reported a TypeScript 4.8.3 parse error in generated definitions and asked for a workaround
 * [today](https://github.com/microsoft/TypeScript/issues/33350#issuecomment-5516589199) **RyanCavanaugh** explained that the issue was fixed by retiring the affected build path in TS 5.5, noting that 'prepend' was removed and linking PRs #57452 and #57472
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#33462](https://github.com/microsoft/TypeScript/issues/33462) (Closed, `Bug`, `Domain: lib.d.ts`)

**document\.createTreewalker and document\.createNodeIterator have missing signature types that which are supported both in IE, Firefox and Chrome**

*TypeScript lib.dom.d.ts is missing IE-supported overloads for document.createTreeWalker and createNodeIterator filter functions and entityReferenceExpansion parameter.*

 * (6.9 years ago) **RyanCavanaugh** added label `Domain: lib.d.ts`, and set milestone to `Backlog`
 * [5 years ago](https://github.com/microsoft/TypeScript/issues/33462#issuecomment-912517410) **mrttrifork** reported that TypeScript 4.4 broke builds by removing NodeFilter and the fourth expandEntityReferences parameter from document.createTreeWalker, impacting IE11 support
 * [today](https://github.com/microsoft/TypeScript/issues/33462#issuecomment-5517060560) **RyanCavanaugh** explained that TypeScript now accepts callable filters for createTreeWalker and createNodeIterator, noted that removing the fourth argument compiles without diagnostics, identified that TS2554 remains for entityReferenceExpansion due to WHATWG DOM definitions, recalled that the IE-specific overload was previously declined and declaration merging was recommended, and stated that lib.dom.d.ts will not include the retired fourth-argument extension
 * **RyanCavanaugh** added label `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#33654](https://github.com/microsoft/TypeScript/issues/33654) (Closed, `Bug`, `Fixed`, `Help Wanted`, `Domain: Intersection`)

**Intersection type with discriminated union type that includes all possible enum values cannot accept enum type**

*Intersecting a discriminated union with an additional field causes TypeScript to reject enum-typed discriminant assignments.*

 * (4.5 years ago) **RyanCavanaugh** added label `Domain: Intersection`, set milestone to `Backlog`, and removed from milestone `TypeScript 4.6.1`
 * [today](https://github.com/microsoft/TypeScript/issues/33654#issuecomment-5517984029) **RyanCavanaugh** described that the return { id, type, value } assignment was fixed in PR #36663 and noted that the same intersection assignment error varied across different TypeScript dev versions
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#33713](https://github.com/microsoft/TypeScript/issues/33713) (Closed, `Bug`, `Needs More Info`, `Needs Investigation`, `Domain: check: Type Circularity`)

**Language service fails to provide type info**

*The TypeScript language service on Windows 10 fails to show type information for recursive types, whereas it works as expected on Ubuntu.*

 * (6.8 years ago) **sandersn** added label `Needs Investigation`, and set milestone to `Backlog`
 * **RyanCavanaugh** added label `Domain: Type Circularity`
 * [today](https://github.com/microsoft/TypeScript/issues/33713#issuecomment-5518279971) **RyanCavanaugh** explained that both the recovered and current TypeScript versions return HTMLHeadingElement for quick-info and asked for the exact editor action or file change causing the transition or an archived tsserver trace
 * (today) **RyanCavanaugh** added labels `Needs Human Review`, `Needs More Info`

### [Issue microsoft/TypeScript#33935](https://github.com/microsoft/TypeScript/issues/33935) (Closed, `Bug`, `Needs More Info`, `Crash`, `Domain: Parser`)

**Debug Failure\. Did not expect PropertyDeclaration to have an Identifier in its trivia**

*A debug assertion failure 'PropertyDeclaration identifier in trivia' frequently occurs (esp. in JSX) and may cause VS crashes.*

 * [4.6 years ago](https://github.com/microsoft/TypeScript/issues/33935#issuecomment-1017211889) **DanielRosenwasser** said "FWIW there's https://github.com/microsoft/TypeScript/issues/44154 if that gives you any clues."
 * [4.6 years ago](https://github.com/microsoft/TypeScript/issues/33935#issuecomment-1018845633) **andrewbranch** said "I don’t think anything JSX-related helps with this one."
 * **RyanCavanaugh** added label `Domain: Parser`
 * [today](https://github.com/microsoft/TypeScript/issues/33935#issuecomment-5518914916) **RyanCavanaugh** requested source file, cursor position or diagnostic range, and exact getCodeFixes request or tsserver log to reproduce the PropertyDeclaration failure
 * (today) **RyanCavanaugh** added labels `Needs Human Review`, `Needs More Info`

### [Issue microsoft/TypeScript#34162](https://github.com/microsoft/TypeScript/issues/34162) (Closed, `Bug`, `Fixed`, `Domain: check: Error Instability`, `Needs Human Review`)

**\-\-noEmitOnError trace has incorrect number of errors**

*Enabling --noEmitOnError causes TypeScript to report two errors instead of one for a single type assignment error.*

 * (6.8 years ago) **RyanCavanaugh** added labels `Bug`, `Domain: Error Instability`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/34162#issuecomment-5519272403) **RyanCavanaugh** noted that the issue was fixed in version 3.8.0-dev.20191213 and described the behavior differences in error reporting with noEmitOnError
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#34846](https://github.com/microsoft/TypeScript/issues/34846) (Closed, `Bug`, `Fixed`, `Domain: tsc -b`, `Needs Human Review`)

**Project with project references and outFile fails to build**

*Using project references and outFile in TypeScript causes TS6305 errors indicating referenced output files haven't been built from source.*

 * [6.3 years ago](https://github.com/microsoft/TypeScript/issues/34846#issuecomment-629566971) **hcapp01** suggested exposing useSourceOfProjectReferenceRedirect as a compiler option as a workaround since outFile is disabled intentionally
 * (5.9 years ago) **RyanCavanaugh** added label `Domain: tsc -b`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/34846#issuecomment-5519937850) **RyanCavanaugh** reported that TS6305 errors still occurred with outFile in TypeScript 6.0.3, noted that outFile support was removed in TypeScript 7 and that a removed-option diagnostic was added
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#34860](https://github.com/microsoft/TypeScript/issues/34860) (Closed, `Bug`, `Fixed`, `Domain: Comment Emit`, `Needs Human Review`)

**Missing JSDoc description when using arrow functions in \-\-allowJs \+ \-\-declaration**

*Generating declaration files from JavaScript with --allowJs and --declaration omits JSDoc comments on exported arrow functions.*

 * [2.4 years ago](https://github.com/microsoft/TypeScript/issues/34860#issuecomment-2018972528) **turadg** questioned whether fixing the JSDoc emission bug was still worthwhile after four years
 * [2.1 years ago](https://github.com/microsoft/TypeScript/issues/34860#issuecomment-2213844841) **mwaeckerlin** asked if there was still no solution and reported that JSDoc did not recognize functions, parameters, and return values in TypeScript files
 * [1.9 years ago](https://github.com/microsoft/TypeScript/issues/34860#issuecomment-2384078804) **daveycodez** demonstrated how adding a JSDoc @type annotation resolved the half-decade-old problem by showing code examples before and after
 * [today](https://github.com/microsoft/TypeScript/issues/34860#issuecomment-5520183195) **RyanCavanaugh** described that TypeScript’s declaration emitter fixed the JSDoc preservation issue in TS 7 dev and later builds while noting it remained in the classic compiler
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#35365](https://github.com/microsoft/TypeScript/issues/35365) (Closed, `Bug`, `Fixed`, `Domain: Module Resolution`, `Needs Human Review`)

**Triple slash type reference doesn't use baseUrl/typeRoots**

*Triple slash reference types do not respect baseUrl and typeRoots settings in tsconfig, causing resolution errors.*

 * (6.7 years ago) **sandersn** added label `Bug`, and set milestone to `Backlog`
 * **RyanCavanaugh** added label `Domain: Module Resolution`
 * [today](https://github.com/microsoft/TypeScript/issues/35365#issuecomment-5521397798) **RyanCavanaugh** reported that TypeScript 5.1.6 resolved the TS2688 error and that removing the retired baseUrl and moduleResolution options enabled the reference to compile without errors
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#35374](https://github.com/microsoft/TypeScript/issues/35374) (Closed, `Bug`, `Domain: API`, `Needs Human Review`)

**bug \`createTemplateMiddle\(\)\` and \`createTemplateTail\(\)\` do not work with escaped chars**

*createTemplateMiddle and createTemplateTail incorrectly scan raw template spans for ']' rather than '}', causing errors with escaped characters.*

 * (6.6 years ago) **RyanCavanaugh** added labels `Bug`, `Domain: API`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/35374#issuecomment-5521437713) **RyanCavanaugh** explained that the issue affects a deprecated pre-TypeScript-7 API no longer maintained
 * **RyanCavanaugh** added label `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#35455](https://github.com/microsoft/TypeScript/issues/35455) (Closed, `Bug`, `Help Wanted`, `Effort: Moderate`, `Domain: JSDoc`, `Needs Human Review`, **sandersn**)

**JSDocTag width is inconsistent**

*TypeScript’s getWidth returns only the tag name length for JSDocTag but the full comment length for JSDocParameterTag, causing inconsistent widths.*

 * **sandersn** added label `GraceHopperOSD`
 * (45 weeks ago) **RyanCavanaugh** added label `Domain: JSDoc`, and removed label `PursuitFellowship`
 * [today](https://github.com/microsoft/TypeScript/issues/35455#issuecomment-5521625186) **RyanCavanaugh** explained that the pre-TypeScript-7 JavaScript Compiler API had been superseded by TypeScript 7 API and would no longer be developed
 * **RyanCavanaugh** added label `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#35485](https://github.com/microsoft/TypeScript/issues/35485) (Closed, `Bug`, `Fixed`, `Domain: JSDoc`, `Needs Human Review`)

**JSDoc optional argument does not generate an error in strict mode**

*JSDoc optional parameters in strict checkJs mode aren’t causing errors for potential undefined property accesses.*

 * (6.6 years ago) **RyanCavanaugh** added labels `Bug`, `Domain: JSDoc`, and set milestone to `Backlog`
 * [later](https://github.com/microsoft/TypeScript/issues/35485#issuecomment-5522069994) **RyanCavanaugh** noted that the issue was fixed in 4.0.0-dev.20200709 by PR #39487 correcting optional JSDoc handling, with earlier dev versions producing differing diagnostics
 * (later) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#35566](https://github.com/microsoft/TypeScript/issues/35566) (Closed, `Bug`, `Domain: Something Else`, `Needs Human Review`)

**@types's definition doesn't match its own type**

*An update to @types/power-assert introduced a type mismatch that breaks a global assert declaration in TypeScript.*

 * (6.7 years ago) **RyanCavanaugh** added labels `Bug`, `Domain: Something Else`, and set milestone to `Backlog`
 * [later](https://github.com/microsoft/TypeScript/issues/35566#issuecomment-5522293674) **RyanCavanaugh** explained that TS2403 arose from duplicate namespace declarations in @types/power-assert, noted the correction in DefinitelyTyped#40903, and recommended removing the redundant global declaration to prevent TS2451
 * **RyanCavanaugh** added label `Needs Human Review`
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#35776](https://github.com/microsoft/TypeScript/issues/35776) (Closed, `Bug`, `Fixed`, `Domain: Crashes`, `Needs Human Review`)

**Heap of out memory for recursive type**

*Compiling a recursive TypeScript type with over ten nested key parameters exhausts heap memory in versions above 3.4.*

 * (6.7 years ago) **RyanCavanaugh** added labels `Bug`, `Domain: Crashes`, and set milestone to `Backlog`
 * [later](https://github.com/microsoft/TypeScript/issues/35776#issuecomment-5523301310) **RyanCavanaugh** confirmed the issue was fixed in 3.9.0-dev.20200403 and referenced PR #37776 and commit 7317292
 * (later) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#35797](https://github.com/microsoft/TypeScript/issues/35797) (Closed, `Bug`, `Fixed`, `Help Wanted`, `Domain: JS Emit`, `Needs Human Review`)

**Invalid output emited as the result of javascript file compilation: amd, default export, jsdoc**

*TypeScript’s AMD JavaScript compilation incorrectly prefixes default-exported function property assignments with exports, producing invalid code.*

 * (4.5 years ago) **RyanCavanaugh** added labels `Help Wanted`, `Domain: JS Emit`, and set milestone to `Backlog`
 * [later](https://github.com/microsoft/TypeScript/issues/35797#issuecomment-5523515819) **RyanCavanaugh** explained that the issue was fixed by retiring AMD output in TypeScript 7, described behavior of various TS versions, and referenced the related issue and PR
 * (later) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#35861](https://github.com/microsoft/TypeScript/issues/35861) (Closed, `Bug`, `Domain: check: Excess Property Checking`, `Needs Human Review`)

**Union type checking during assignment fails for boolean and passes for other primitives**

*TypeScript 3.7.2 improperly allows invalid assignments to number|string union types while correctly rejecting boolean|string unions.*

 * (6.6 years ago) **RyanCavanaugh** added labels `Bug`, `Domain: Excess Property Checking`, and set milestone to `Backlog`
 * [later](https://github.com/microsoft/TypeScript/issues/35861#issuecomment-5524468782) **RyanCavanaugh** related the behavior to issue #20863, explained the acceptance of fresh object literals based on known properties in unresolved object-union targets, and noted that the boolean|string case differs due to unit types enabling discrimination
 * **RyanCavanaugh** added label `Needs Human Review`
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#35879](https://github.com/microsoft/TypeScript/issues/35879) (Closed, `Bug`, `Fixed`, `Help Wanted`, `Domain: JS Emit`, `Needs Human Review`)

**commonjs export binding produces invalid code for increment/decrement in PrefixUnaryExpression**

*TypeScript’s CommonJS export transform fails to parenthesize prefix unary assignments, emitting invalid code like `while (!exports.foo = --foo)`.*

 * (4.5 years ago) **RyanCavanaugh** added labels `Help Wanted`, `Domain: JS Emit`, and removed label `Rescheduled`
 * [later](https://github.com/microsoft/TypeScript/issues/35879#issuecomment-5524712666) **RyanCavanaugh** confirmed that the issue was fixed by comparing the emitted code in TS 4.1.6 and TS 4.2.4 and referencing merged PRs #41156 and #42676
 * (later) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#35880](https://github.com/microsoft/TypeScript/issues/35880) (Closed, `Bug`, `Fixed`, `Domain: check: Type Inference`, `Needs Human Review`)

**ObjectAssignmentRest causes "Property 'foo' does not exist on type '{}'"**

*Object destructuring assignment with rest and default values incorrectly triggers 'Property does not exist' errors.*

 * (6.6 years ago) **RyanCavanaugh** added labels `Bug`, `Domain: Type Inference`, and set milestone to `Backlog`
 * [later](https://github.com/microsoft/TypeScript/issues/35880#issuecomment-5524969366) **RyanCavanaugh** stated that the issue was fixed in 5.6.0-dev.20240716 and linked the PR for the change
 * (later) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#35901](https://github.com/microsoft/TypeScript/issues/35901) (Closed, `Bug`, `Fixed`, `Domain: Error Messages`, `Needs Human Review`)

**Give better error when using private identifier in parameter property**

*Using a private identifier (#prop) in a constructor parameter property triggers multiple misleading errors instead of a focused diagnostic.*

 * (6.6 years ago) **RyanCavanaugh** added labels `Bug`, `Domain: Error Messages`, and set milestone to `Backlog`
 * [later](https://github.com/microsoft/TypeScript/issues/35901#issuecomment-5525710237) **RyanCavanaugh** mentioned that PR #36188 fixed the issue and that dev versions now report only the targeted TS18009 diagnostic
 * (later) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#36133](https://github.com/microsoft/TypeScript/issues/36133) (Closed, `Bug`, `Fixed`, `Domain: lib.d.ts`, `Needs Human Review`)

**No overload expects 5 arguments, but overloads do exist that expect either 5 or 9 arguments \(CanvasRenderingContext2D\.drawImage\)**

*TypeScript reports no overload for CanvasRenderingContext2D.drawImage when using spread syntax with a four-element array and extra parameters*

 * [5.9 years ago](https://github.com/microsoft/TypeScript/issues/36133#issuecomment-706998134) **Wineric** said "Having the same issue"
 * [5.3 years ago](https://github.com/microsoft/TypeScript/issues/36133#issuecomment-836314409) **michael-freidgeim-webjet** said "Related issue https://github.com/microsoft/TypeScript/issues/42418"
 * **RyanCavanaugh** added label `Domain: lib.d.ts`
 * [later](https://github.com/microsoft/TypeScript/issues/36133#issuecomment-5526602707) **RyanCavanaugh** reported that the TS2575 error was fixed in 4.0.0-dev.20200605 and newer builds due to improved tuple handling in call arity checks
 * (later) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#61979](https://github.com/microsoft/TypeScript/issues/61979) (Closed, `Bug`, `Help Wanted`, `Domain: check: Contextual Types`)

**Missing errors in generic functions in context\-sensitive arguments**

*TypeScript fails to report errors for generic functions with context-sensitive parameters when the inferred return type mismatches.*

 * (1.1 years ago) **RyanCavanaugh** added labels `Help Wanted`, `Domain: Contextual Types`, and set milestone to `Backlog`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#63703](https://github.com/microsoft/TypeScript/issues/63703) (Open, `Planning`)

**TypeScript 7\.1 Iteration Plan**

*Roadmap for TypeScript 7.1 detailing milestones and features across compiler, editor productivity, and performance enhancements.*

 * [1 month ago](https://github.com/microsoft/TypeScript/issues/63703#issuecomment-5146188990) **dasa** said "2027, is that a typo?"
 * [1 month ago](https://github.com/microsoft/TypeScript/issues/63703#issuecomment-5146248499) **DanielRosenwasser** said "Sure is! 🫠🤦‍♂️"
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63703#issuecomment-5501016536) **DanielRosenwasser** announced that the beta release would be delayed by two weeks for additional API testing, with further details on RC and final release dates to follow
 * [today](https://github.com/microsoft/TypeScript/issues/63703#issuecomment-5519354895) **Flarette** asked if the team planned to revisit instantiation depth limits in the tsgo compiler
 * [today](https://github.com/microsoft/TypeScript/issues/63703#issuecomment-5520213322) **jakebailey** stated that there were no plans to change the limits and referenced a related issue
 * [today](https://github.com/microsoft/TypeScript/issues/63703#issuecomment-5520894104) **Flarette** argued that compiler depth limits hinder progress and proposed making them configurable via a flag, citing the Jevons paradox and compute innovation history

### [Issue microsoft/TypeScript#63867](https://github.com/microsoft/TypeScript/issues/63867) (Open, `Needs More Info`)

**\`tsc \-\-watch\` doesn't recompile on file change**

*TypeScript 7.0.2 stops tsc --build --watch from detecting file changes in a monorepo*

 * [1 month ago](https://github.com/microsoft/TypeScript/issues/63867#issuecomment-5351508388) **jakebailey** said "Can you please try the nightly instead of 7.0.2?"
 * [1 month ago](https://github.com/microsoft/TypeScript/issues/63867#issuecomment-5351508407) **rkistner** said "@jakebailey Using 7.1.0-dev.20260804.1 appears to resolve the issue for me: No high CPU usage after building; detecting changes and Ctrl+C run instantly."
 * [1 month ago](https://github.com/microsoft/TypeScript/issues/63867#issuecomment-5351508426) **haines** confirmed the high CPU usage after building and noted that the dev version resolved the issue for them
 * [later](https://github.com/microsoft/TypeScript/issues/63867#issuecomment-5525832300) **jkazimierczak-eficode** reported experiencing the same project-references tsconfig watch issue and confirmed that updating to nightly 7.1.0-dev.20260901.1 resolved it

### [Issue microsoft/TypeScript#63875](https://github.com/microsoft/TypeScript/issues/63875) (Open, `Suggestion`, `Committed`, **andrewbranch**)

**API feature roadmap**

*API feature roadmap for TypeScript 7.1 outlining plugin replacements and top-level utilities with rough cost estimates.*

 * [6 days ago](https://github.com/microsoft/TypeScript/issues/63875#issuecomment-5437239627) **remojansen** thanked andrewbranch and reported initial PoC progress for ahead-of-time reflect metadata in TypeScript 7, injecting design:symbols and design:arguments at build time using types
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63875#issuecomment-5482240339) **johnnyreilly** said "As discussed in https://github.com/microsoft/TypeScript/issues/64090, it would be handy to expose the path normalisation function."
 * [today](https://github.com/microsoft/TypeScript/issues/63875#issuecomment-5510502588) **johnnyreilly** shared a benchmark test pack and snapshot results comparing performance of the old and new TypeScript APIs in ts-loader
 * [today](https://github.com/microsoft/TypeScript/issues/63875#issuecomment-5513828692) **andrewbranch** described removal of openPrimaryProject call in transpileOnly mode and reported performance improvements and detailed the core patch changes
 * [today](https://github.com/microsoft/TypeScript/issues/63875#issuecomment-5514520912) **johnnyreilly** said "Thanks @andrewbranch! I've applied the git diff and pushed I'll take a look at your other suggestions tomorrow!"
 * [later](https://github.com/microsoft/TypeScript/issues/63875#issuecomment-5522708727) **johnnyreilly** reported that the PR branch did not reliably improve build times and provided detailed benchmark results for Mac, Ubuntu, and Windows

### [PR microsoft/TypeScript#63893](https://github.com/microsoft/TypeScript/pull/63893) (Closed, `For Uncommitted Bug`, **andrewbranch**)

**API: add getChildren and token getters to Node**

*Add getChildren, getChildCount, getChildAt, getFirstToken, and getLastToken methods to the native TypeScript Node API.*

 * created by **oMatheusmol**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * **typescript-automation[bot]** assigned to **andrewbranch**
 * [later](https://github.com/microsoft/TypeScript/pull/63893#issuecomment-5522334962) **oMatheusmol** implemented requested changes, replaced childrenCache with a plain Map, used a shared scanner in getChildren, removed the consumed set, skipped reparsed subtrees, and added 16 .js/.jsx test cases

### [Issue microsoft/TypeScript#63924](https://github.com/microsoft/TypeScript/issues/63924) (Closed, `Suggestion`, `Infrastructure`, `Domain: Editor/VS Code Extension`, **jakebailey**)

**Decouple extension publishing from TS compiler**

*Decouple the TS 7 extension’s build and packaging from the TypeScript compiler to enable separate Insiders publishing and future built-in distribution*

 * (1 week ago) **DanielRosenwasser** added label `Domain: Editor/VS Code Extension`, and assigned to **jakebailey**
 * **jakebailey** added label `Infrastructure`
 * **jakebailey** added to milestone `TypeScript 7.1.0 Beta`

### [PR microsoft/TypeScript#63968](https://github.com/microsoft/TypeScript/pull/63968) (Open, `For Milestone Bug`)

**Fix panic in the optional\-chain transform when a chain ends in a tagged template**

*Update the optional-chain transformer to correctly handle tagged template heads rather than panicking and include regression tests.*

 * created by **bigboateng**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/63968#issuecomment-5386598913) **bigboateng** said "@microsoft-github-policy-service agree"
 * (later) **typescript-automation[bot]** added label `For Milestone Bug`, and removed label `For Uncommitted Bug`

### [Issue microsoft/TypeScript#63970](https://github.com/microsoft/TypeScript/issues/63970) (Open, `Suggestion`, `Awaiting More Feedback`)

**Inconsistent typing of endless generators between functions and lambdas**

*TypeScript infers void return for named infinite generators but never for generator lambdas, causing incompatible assignment errors.*

 * [1 week ago](https://github.com/microsoft/TypeScript/issues/63970#issuecomment-5387542405) **Andarist** explained that the behavior was deliberate for backwards compatibility and linked to the TypeScript rules for auto-inferring never return types
 * (1 week ago) **RyanCavanaugh** added labels `Suggestion`, `Awaiting More Feedback`
 * [today](https://github.com/microsoft/TypeScript/issues/63970#issuecomment-5516823860) **jacekkopecky** asked why method declarations and function expressions handle never returns inconsistently and suggested revisiting the corner case

### [Issue microsoft/TypeScript#64037](https://github.com/microsoft/TypeScript/issues/64037) (Open, `Needs More Info`)

**npx tsc \-w is triggering itself after each build**

*npx tsc --watch enters a build loop because output JavaScript files alongside TypeScript sources continuously retrigger compilation.*

 * **RyanCavanaugh** added label `Needs More Info`
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/64037#issuecomment-5429365937) **RyanCavanaugh** said "We need a concrete repro in order to investigate"
 * [6 days ago](https://github.com/microsoft/TypeScript/issues/64037#issuecomment-5441005231) **msab-john** said "I'll see if I can make a small and simple one..."
 * [later](https://github.com/microsoft/TypeScript/issues/64037#issuecomment-5527566209) **nstepien** described a simple repro of tsc --watch triggering on new directory creation and noted missing logging of the trigger source

### [Issue microsoft/TypeScript#64089](https://github.com/microsoft/TypeScript/issues/64089) (Open, `Needs Investigation`, **andrewbranch**)

**FSEvents watcher drops events when requested casing differs from disk casing**

*The macOS FSEvents watcher drops events when requested path casing differs from disk casing because WatchManager lowercases paths.*

 * created by **andrewbranch**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **andrewbranch**

### [Issue microsoft/TypeScript#64118](https://github.com/microsoft/TypeScript/issues/64118) (Open, `Docs`)

**dom\.generated\.d\.ts is missing from this repo while still referenced in the docs**

*The documentation still references dom.generated.d.ts, but that file is missing from the repository.*

 * created by **funkyfuture**
 * **RyanCavanaugh** added label `Docs`
 * [today](https://github.com/microsoft/TypeScript/issues/64118#issuecomment-5521839695) **seanxuu** offered to work on the documentation issue, planned to update the tutorial link to the current DOM type-definition baseline, and asked for confirmation of the target repository

### [PR microsoft/TypeScript#64131](https://github.com/microsoft/TypeScript/pull/64131) (Closed, `For Backlog Bug`)

**Fixed \`anyFunctionType\` leak**

*Recreates the pull request to fix the anyFunctionType leak in TypeScript.*

 * created by **Andarist**
 * (today) **typescript-automation[bot]** added labels `For Backlog Bug`, `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64131#issuecomment-5513664030) **jakebailey** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/64131#issuecomment-5513665230) **typescript-automation[bot]** posted updated build status table for test, user test, dt, and perf jobs
 * [today](https://github.com/microsoft/TypeScript/pull/64131#issuecomment-5513955020) **typescript-automation[bot]** reported user test results showing two package install failures and one git clone failure but otherwise everything looked good
 * [today](https://github.com/microsoft/TypeScript/pull/64131#issuecomment-5514035269) **typescript-automation[bot]** provided the perf run results requested by @jakebailey
 * [today](https://github.com/microsoft/TypeScript/pull/64131#issuecomment-5514407187) **typescript-automation[bot]** reported that running tsc on the top 400 repos comparing main and the pull request merge yielded no issues
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#64134](https://github.com/microsoft/TypeScript/issues/64134) (Open, `Bug`, **RyanCavanaugh**, **Copilot**)

**\`sourceMap\` emit is disproportionately slow for files containing one very large object literal**

*Source map generation in TypeScript 7 is significantly slower than in TypeScript 6 for files with a large object literal.*

 * created by **ken7253**
 * (today) **RyanCavanaugh** added label `Bug`, set milestone to `Backlog`, and assigned to **Copilot**, **RyanCavanaugh**

### [Issue microsoft/TypeScript#64135](https://github.com/microsoft/TypeScript/issues/64135) (Closed, **jakebailey**, **Copilot**)

**unstable/ast: scanJsDocToken infinite\-loops when a scan range ends on a trailing '\-' \(fix from \#63581 not carried into the AST scanner\)**

*scanJsDocToken in unstable/ast infinite-loops on trailing hyphens due to missing parentheses in its loop condition*

 * created by **nightcabin1**
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript#64136](https://github.com/microsoft/TypeScript/issues/64136) (Closed, `Not a Defect`)

**Regression to \#35004**

*Assertion functions fail with wildcard destructuring imports after upgrading to TypeScript 7, triggering TS2775 errors.*

 * created by **valler**
 * [today](https://github.com/microsoft/TypeScript/issues/64136#issuecomment-5512454226) **MartinJohns** said "Your issue is the deconstruction, not the wildcard import."
 * [today](https://github.com/microsoft/TypeScript/issues/64136#issuecomment-5512758602) **valler** thanked maintainers and asked if TS2775 was expected and whether to close or rename the issue
 * [later](https://github.com/microsoft/TypeScript/issues/64136#issuecomment-5525601715) **jcalz** explained that assertion functions require explicit type annotations and that destructuring assignment cannot support them, and suggested framing a feature request as 'allow destructuring assignment of assertion functions'

### [PR microsoft/TypeScript#64137](https://github.com/microsoft/TypeScript/pull/64137) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Fix TestContentMapperOpenFileExcludedByConfigChange race**

*Fix a race condition in the TestContentMapperOpenFileExcludedByConfigChange test similar to the fix applied in issue 64081.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64138](https://github.com/microsoft/TypeScript/pull/64138) (Open, `For Uncommitted Bug`, **RyanCavanaugh**, **Copilot**)

**Speed up source map emit for large single\-line object literals**

*Optimize source map emission by caching UTF-16 column calculations to avoid quadratic scanning for large single-line object literals.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * (today) **typescript-automation[bot]** added labels `For Milestone Bug`, `For Milestone Bug`, `For Uncommitted Bug`, and removed label `For Milestone Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64138#issuecomment-5517346468) **jakebailey** said "Interesting, I think we have this same optimization somewhere else? I had thought for this specifically, actually."

### [PR microsoft/TypeScript#64139](https://github.com/microsoft/TypeScript/pull/64139) (Closed, `Author: Team`, `For Milestone Bug`, **jakebailey**)

**Add independent VS Code extension releases**

*Automate version bumping, tagging, building, signing, and manual publishing of the VS Code extension via GitHub Actions and Azure pipelines.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, `For Milestone Bug`, removed label `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#64140](https://github.com/microsoft/TypeScript/pull/64140) (Open, `For Uncommitted Bug`, `dependencies`, `javascript`)

**Bump fast\-uri from 3\.1\.5 to 3\.1\.7**

*Upgrade fast-uri from version 3.1.5 to 3.1.7 to address multiple high-severity security vulnerabilities*

 * created by **dependabot[bot]**
 * (today) **dependabot[bot]** added labels `dependencies`, `javascript`, `dependencies`, `javascript`
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [PR microsoft/TypeScript#64141](https://github.com/microsoft/TypeScript/pull/64141) (Closed, `For Uncommitted Bug`, **jakebailey**, **Copilot**)

**Prevent infinite loop in unstable AST JSDoc scanner**

*Guard identifier parts and hyphens with range checks in the unstable AST JSDoc scanner to avoid infinite loops.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [PR microsoft/TypeScript#64142](https://github.com/microsoft/TypeScript/pull/64142) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Avoid async IPC panic on peer close**

*Fixes a race condition that causes an asynchronous IPC panic when the peer connection closes*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [Issue microsoft/TypeScript#64143](https://github.com/microsoft/TypeScript/issues/64143) (Closed, `Bug`, **gabritto**)

**readonly is accepted in ambient module import attributes types**

*Ambient module import attributes types in TypeScript incorrectly allow the readonly modifier, leading to ambiguous module matching and merging.*

 * created by **camc314**

### [Issue microsoft/TypeScript#64144](https://github.com/microsoft/TypeScript/issues/64144) (Open, `Suggestion`)

**Auto\-delete closing tag when opening tag becomes self\-closed**

*Automatically remove the redundant closing tag when converting an opening tag into a self-closing tag.*

 * created by **monolithed**
 * **vs-code-engineering[bot]** assigned to **aeschli**
 * [later](https://github.com/microsoft/TypeScript/issues/64144#issuecomment-5524285935) **aeschli** said "Thats with TSX/JSX, correct?"
 * (later) **aeschli** assigned to **dbaeumer**, and unassigned **aeschli**
 * **dbaeumer** unassigned **dbaeumer**

### [Issue microsoft/TypeScript#64145](https://github.com/microsoft/TypeScript/issues/64145) (Closed)

**Completions inside tuple types suggest value symbols instead of types**

*TypeScript completions inside tuple type brackets incorrectly suggest value symbols like 'User' rather than only type symbols such as 'UserTuple'.*

 * created by **luo2430**
 * [later](https://github.com/microsoft/TypeScript/issues/64145#issuecomment-5526948029) **luo2430** said "https://github.com/microsoft/TypeScript/pull/64146"

### [PR microsoft/TypeScript#64146](https://github.com/microsoft/TypeScript/pull/64146) (Closed, `For Uncommitted Bug`)

**Fix completions inside tuple types suggesting value symbols**

*Auto-completion inside tuple type definitions incorrectly suggests value symbols instead of type symbols.*

 * created by **luo2430**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/64146#issuecomment-5526934710) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."

### [PR microsoft/TypeScript#64149](https://github.com/microsoft/TypeScript/pull/64149) (Closed, `For Uncommitted Bug`)

**deew**

*Pull request 'deew' includes only the standard submission checklist without any associated issue or substantive code changes.*

 * created by **ancasnyk**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/64149#issuecomment-5527828077) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (later) **ancasnyk** closed the issue

