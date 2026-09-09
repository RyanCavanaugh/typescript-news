# Report for 2026-09-08 (Tuesday, September 8th, 2026)

17 different users commented on 71 different issues.

## Recommended Actions

 * Response Recommended
    * @rafaelnajman provided repro steps and detailed observations in [microsoft/TypeScript#63856](https://github.com/microsoft/TypeScript/issues/63856#issuecomment-5591307178)
    * @colinhacks asked for a solution that avoids tradeoffs in recursive inference support for z.object inputs in [microsoft/TypeScript#64172](https://github.com/microsoft/TypeScript/pull/64172#issuecomment-5594267273)
    * @marwan562 requested review by @copilot in [microsoft/TypeScript#64177](https://github.com/microsoft/TypeScript/pull/64177#issuecomment-5591820174)
    * @typescript-automation provided test results as requested in [microsoft/TypeScript#64187](https://github.com/microsoft/TypeScript/pull/64187#issuecomment-5590509687)
    * @colinhacks asked for a solution that avoids type safety tradeoffs in recursive inference in [microsoft/TypeScript#64192](https://github.com/microsoft/TypeScript/issues/64192#issuecomment-5594283251)

## Activity Summary

### [Issue microsoft/TypeScript#33935](https://github.com/microsoft/TypeScript/issues/33935) (Closed, `Bug`, `Needs More Info`, `Crash`, `Domain: Parser`)

**Debug Failure\. Did not expect PropertyDeclaration to have an Identifier in its trivia**

*A debug assertion failure 'PropertyDeclaration identifier in trivia' frequently occurs (esp. in JSX) and may cause VS crashes.*

 * **RyanCavanaugh** added label `Needs More Info`
 * [5 days ago](https://github.com/microsoft/TypeScript/issues/33935#issuecomment-5532266812) **andrewbranch** said "We can probably assume this code path is no longer quite the same, and will show up differently in TS 7 telemetry if it's still a problem."
 * (5 days ago) **andrewbranch** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#41065](https://github.com/microsoft/TypeScript/issues/41065) (Closed, `Bug`, `Domain: check: Type Inference`)

**Default generic type is improperly constrained in conditional types\.**

*The compiler incorrectly infers a default generic as never instead of number when used in conditional type constraints.*

 * [3 days ago](https://github.com/microsoft/TypeScript/issues/41065#issuecomment-5553301257) **RyanCavanaugh** explained that generic defaults are only used when inference can’t choose a candidate, described how contextual inference selected never in the example, and noted the helper-specific issue was resolved
 * **RyanCavanaugh** added label `Needs Human Review`
 * (3 days ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#42383](https://github.com/microsoft/TypeScript/issues/42383) (Closed, `Bug`, `Fixed`, `Domain: check: Type Circularity`)

**Error inheriting class B from class A that contains a method that takes a parameter of type B and returns this when decorated with multiple mixins**

*Using two mixins on a base class with a method taking and returning the subclass triggers a recursive base type error.*

 * **RyanCavanaugh** added label `Needs Human Review`
 * (2 days ago) **RyanCavanaugh** closed the issue
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/42383#issuecomment-5559490024) **AlmostBearded** thanked for fixing the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#42905](https://github.com/microsoft/TypeScript/issues/42905) (Closed, `Bug`, `Fixed`, `Domain: Declaration Emit`, `Has Repro`)

**Broken emit when \`Infinity\` or \`‑Infinity\` ends up in a type position**

*TypeScript erroneously emits Infinity and -Infinity in type positions, producing invalid declaration files.*

 * (2 days ago) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (2 days ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#43120](https://github.com/microsoft/TypeScript/issues/43120) (Closed, `Bug`, `Help Wanted`, `Domain: tsc -b`)

**TypeScript 4\.2 caches cwd between builds when using the programatic api **

*Using the TypeScript 4.2 programmatic API caches the current working directory between runs, leading to tsconfig.json not found errors.*

 * [2 days ago](https://github.com/microsoft/TypeScript/issues/43120#issuecomment-5560886637) **RyanCavanaugh** advised creating the host with getCurrentDirectory bound to process.cwd instead of using the cached ts.sys current directory and noted the global reset/new-system API was declined and the pre-TypeScript-7 API is no longer developed
 * **RyanCavanaugh** added label `Needs Human Review`
 * (2 days ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#46724](https://github.com/microsoft/TypeScript/issues/46724) (Closed, `Bug`, `Needs More Info`, `Domain: Declaration Emit`)

**Optional parameter makes the compiler resolve types prematurely for declaration**

*Making the parameter optional causes the compiler to prematurely resolve the conditional Key type to unknown[] in the declaration.*

 * **RyanCavanaugh** added label `Needs More Info`
 * [today](https://github.com/microsoft/TypeScript/issues/46724#issuecomment-5585782895) **devanshj** concluded that Playground v4.4.4 and v6.0.3 produce the correct output and suggested closing the issue
 * (today) **devanshj** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#47603](https://github.com/microsoft/TypeScript/issues/47603) (Closed, `Bug`, `Fixed`, `Help Wanted`, `Domain: JSDoc`, `checkJs`, `Needs Human Review`)

**Inconsistent behaviour when accessing setters between TypeScript \(\.ts files\) and TypeScript in JSDoc\.**

*TypeScript’s JSDoc support fails to recognize class setters when accessed via dynamic property names, causing duplicate property errors.*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [4.6 years ago](https://github.com/microsoft/TypeScript/issues/47603#issuecomment-1024953742) **a-tarasyuk** explained that this is a late-bound symbol and provided code examples and an example link
 * **RyanCavanaugh** added label `Domain: JSDoc`
 * [today](https://github.com/microsoft/TypeScript/issues/47603#issuecomment-5588268552) **RyanCavanaugh** reported that PR #55438 fixed the JSDoc literal `name` parameter compilation errors and noted that only version 5.3.0-dev.20230901 was affected and subsequent releases are clean
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#47608](https://github.com/microsoft/TypeScript/issues/47608) (Closed, `Bug`, `Fixed`, `Help Wanted`, `Domain: JSDoc`, `Needs Human Review`)

**JSDoc \`@callback\` tag types are only checked if referenced by code**

*JSDoc @callback tag types in JavaScript files are only validated by TypeScript when they’re referenced, leaving unreferenced callbacks unchecked.*

 * (4.5 years ago) **RyanCavanaugh** added labels `Domain: JSDoc`, `Help Wanted`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/47608#issuecomment-5588430705) **RyanCavanaugh** noted that the issue was fixed in TypeScript 7.1.0-dev and that it reports errors for all three badtype references, unlike TypeScript 6.0.3
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#47691](https://github.com/microsoft/TypeScript/issues/47691) (Closed, `Bug`, `Fixed`, `Domain: Parser`, `Needs Human Review`)

**Ambient accessor declaration does not parse with trailing comma**

*Ambient accessor declarations fail to parse when followed by a trailing comma.*

 * (4.5 years ago) **RyanCavanaugh** added labels `Bug`, `Domain: Parser`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/47691#issuecomment-5588747522) **RyanCavanaugh** noted that PR #49545 fixed the issue and confirmed that comma-separated ambient accessor signatures parsed successfully in TS 4.8.0-dev.20220707 but not in 4.8.0-dev.20220706, and that ambient accessor implementations still reported TS1131 as expected
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#47799](https://github.com/microsoft/TypeScript/issues/47799) (Closed, `Bug`, `Fixed`, `Help Wanted`, `Domain: tsc -b`, `Needs Human Review`)

**tsc won't compile newly added references in watch mode**

*TypeScript’s tsc watch mode fails to compile newly added project references after initial build until restarted.*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [3.8 years ago](https://github.com/microsoft/TypeScript/issues/47799#issuecomment-1285037242) **WearyMonkey** reproduced the issue in TypeScript 4.8.4 and asked for progress
 * **RyanCavanaugh** added label `Domain: tsc -b`
 * [today](https://github.com/microsoft/TypeScript/issues/47799#issuecomment-5589654405) **RyanCavanaugh** noted that the error recurred in TypeScript 7.1.0-dev.20260908.1 under watch build after removing and restoring the root references, while TypeScript 4.5.5 and 6.0.3 reported no errors
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#47858](https://github.com/microsoft/TypeScript/issues/47858) (Closed, `Bug`, `Fixed`, `Help Wanted`, `Domain: check: Type Inference`, `Needs Human Review`)

**'Any' on anonymous function argument response in generic**

*Anonymous returned functions in a generic mapping incorrectly infer their parameter type as any instead of number.*

 * [4.5 years ago](https://github.com/microsoft/TypeScript/issues/47858#issuecomment-1040612678) **benhason1** asked to take the issue
 * [4.5 years ago](https://github.com/microsoft/TypeScript/issues/47858#issuecomment-1041928477) **chbdetta** said "sorry @benhason1 , I didn't see your comment when starting working on this"
 * **RyanCavanaugh** added label `Domain: Type Inference`
 * [today](https://github.com/microsoft/TypeScript/issues/47858#issuecomment-5590061064) **RyanCavanaugh** informed that the issue was fixed in version 5.1.0-dev.20230321 and later and detailed relevant PRs and commits
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#48087](https://github.com/microsoft/TypeScript/issues/48087) (Closed, `Bug`, `Fixed`, `Help Wanted`, `Domain: Declaration Emit`, `Needs Human Review`)

**tsc build declarationMap generates incorrect mappings from JSDoc**

*The declarationMap output from tsc build generates wrong mappings for JSDoc-annotated code.*

 * (4.5 years ago) **RyanCavanaugh** added labels `Help Wanted`, `Domain: Declaration Emit`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/48087#issuecomment-5590676305) **RyanCavanaugh** reported that declaration-map positions remained incorrect in TypeScript 6.0.3 but were corrected in 7.1.0-dev.20260908.1
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#48217](https://github.com/microsoft/TypeScript/issues/48217) (Closed, `Bug`, `Fixed`, `Help Wanted`, `Domain: enum`, `Needs Human Review`)

**Mapping with enum key type and literal value type gives not assignable error\. **

*Defining a mapping with an enum key type and literal value types causes a TypeScript assignment error.*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [4.5 years ago](https://github.com/microsoft/TypeScript/issues/48217#issuecomment-1066981987) **Zzzen** said "Related to #29718"
 * **RyanCavanaugh** added label `Domain: enum`
 * [today](https://github.com/microsoft/TypeScript/issues/48217#issuecomment-5592063253) **RyanCavanaugh** reported that the computed-key TS2418 error was fixed in recent builds by PR #51915
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#48378](https://github.com/microsoft/TypeScript/issues/48378) (Closed, `Bug`, `Fixed`, `Help Wanted`, `Domain: check: Control Flow`, `Needs Human Review`)

**Nested destructuring does not narrow dependent parameters**

*Nested destructuring prevents TypeScript from correctly narrowing the second tuple element based on the first element’s value.*

 * [4.2 years ago](https://github.com/microsoft/TypeScript/issues/48378#issuecomment-1162132154) **jtbandes** asked whether the provided code example exhibited the same issue
 * [4.2 years ago](https://github.com/microsoft/TypeScript/issues/48378#issuecomment-1162512868) **Fireboltofdeath** said "This issue is referring to the control flow analysis of destructured unions so I don't believe this is related to that issue."
 * **RyanCavanaugh** added label `Domain: Control Flow`
 * [today](https://github.com/microsoft/TypeScript/issues/48378#issuecomment-5592684325) **RyanCavanaugh** noted that PR #56306 fixed the nested tuple binding issue and that the example errors in 5.4.0-dev.20231128 but is clean in 5.4.0-dev.20231129, TypeScript 6.0.3, and the current native compiler
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#48451](https://github.com/microsoft/TypeScript/issues/48451) (Closed, `Bug`, `Fixed`, `Help Wanted`, `Domain: lib.d.ts`, `Needs Human Review`)

**\`HTMLMetaElement\` property descriptions**

*Missing or incorrect TypeScript description comments need to be added for HTMLMetaElement’s name, content, httpEquiv, and media properties.*

 * (4.4 years ago) **RyanCavanaugh** added label `Domain: lib.d.ts`, and set milestone to `Backlog`
 * [3.4 years ago](https://github.com/microsoft/TypeScript/issues/48451#issuecomment-1506738484) **Teamop** stated that based on the spec the current MDN link and existing types were correct
 * [today](https://github.com/microsoft/TypeScript/issues/48451#issuecomment-5593107845) **RyanCavanaugh** clarified that current DOM declarations provided distinct property documentation for HTMLMetaElement.content, httpEquiv, media, and name matching the HTML meta-element specification
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#48547](https://github.com/microsoft/TypeScript/issues/48547) (Closed, `Bug`, `Fixed`, `Help Wanted`, `Domain: Declaration Emit`, `Needs Human Review`)

**Ambient type for constructor parameter property with default does not include 'undefined' when the parameter is followed by one without a default**

*Ambient declarations for a constructor parameter property with a default followed by a required parameter omit undefined from its type.*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [4.4 years ago](https://github.com/microsoft/TypeScript/issues/48547#issuecomment-1087377922) **a-tarasyuk** said "@RyanCavanaugh Should TS add undefined in strict/non-strict mode?"
 * [4.4 years ago](https://github.com/microsoft/TypeScript/issues/48547#issuecomment-1087711395) **RyanCavanaugh** said "I would say both? Generally we prefer declaration emit to make strict-friendly output files even if the input project isn't strict"
 * [today](https://github.com/microsoft/TypeScript/issues/48547#issuecomment-5593516381) **RyanCavanaugh** stated that the issue had been fixed in PR #58177, causing TypeScript 5.6.0-dev.20240813 and later to emit constructor(a: number | undefined, b: string) in both strict-null-checking modes
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#49072](https://github.com/microsoft/TypeScript/issues/49072) (Closed, `Bug`, `Fixed`, `Domain: Conditional Types`, `Rescheduled`, `Needs Human Review`, **weswigham**)

**Incorrect error when using generic, class and conditional typing \(\#43237 still exists\)**

*Conditional types with generic class parameters still produce incorrect errors in TypeScript 3.9 and nightly.*

 * (2.1 years ago) **RyanCavanaugh** added label `Domain: Conditional Types`, set milestone to `TypeScript 5.7.0`, and removed from milestone `TypeScript 5.5.0`
 * [today](https://github.com/microsoft/TypeScript/issues/49072#issuecomment-5595240064) **RyanCavanaugh** noted that the issue was fixed by PR #50328 and that the examples compiled cleanly from v4.9.0-dev.20220921 onward
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#49273](https://github.com/microsoft/TypeScript/issues/49273) (Closed, `Bug`, `Help Wanted`, `Domain: JSDoc`, `Needs Human Review`)

**\`@\` character in code block renders poorly in tooltip**

*VS Code hover tooltips fail to render '@' symbols in TypeScript code blocks inside documentation comments.*

 * [3.6 years ago](https://github.com/microsoft/TypeScript/issues/49273#issuecomment-1401232357) **KostyaTretyak** said "By the way, this behavior is observed only if there are no characters other than a space before the @ symbol."
 * **RyanCavanaugh** added label `Domain: JSDoc`
 * [31 weeks ago](https://github.com/microsoft/TypeScript/issues/49273#issuecomment-3812408981) **goestav** suggested using zero width space characters as a workaround and provided code examples and screenshots illustrating the behavior
 * [later](https://github.com/microsoft/TypeScript/issues/49273#issuecomment-5598040802) **RyanCavanaugh** noted that the issue was tracked by #47679 and explained that backtick state wasn't preserved across lines, causing lines beginning with '@' in multiline fenced JSDoc code examples to be misparsed
 * **RyanCavanaugh** added label `Needs Human Review`
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#49352](https://github.com/microsoft/TypeScript/issues/49352) (Closed, `Bug`, `Fixed`, `Help Wanted`, `Domain: check: Control Flow`, `Needs Human Review`)

**Strange narrowing when using instanceof on template class with optional field**

*TypeScript incorrectly narrows a generic subclass with an optional field when using instanceof, causing property errors.*

 * **RyanCavanaugh** added label `Help Wanted`
 * [4.2 years ago](https://github.com/microsoft/TypeScript/issues/49352#issuecomment-1145075551) **RyanCavanaugh** provided simplified code reproducing an instanceof narrowing bug where A1’s optional field wasn’t recognized while A2’s non-null asserted field worked, noting it has existed since v3.3.3 with no other reports
 * **RyanCavanaugh** added label `Domain: Control Flow`
 * [later](https://github.com/microsoft/TypeScript/issues/49352#issuecomment-5599713325) **RyanCavanaugh** noted that the issue was fixed by PR #49625 and that the example compiled cleanly on newer TypeScript versions
 * (later) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#49415](https://github.com/microsoft/TypeScript/issues/49415) (Open, `Bug`, `Help Wanted`, `Domain: lib.d.ts`, `Needs Human Review`, **RyanCavanaugh**, **Copilot**)

**window\.opener should not be typed as any**

*window.opener remains typed as any in TypeScript’s ESNext/dom definitions despite a reported fix*

 * (4.2 years ago) **RyanCavanaugh** added labels `Domain: lib.d.ts`, `Help Wanted`, and set milestone to `Backlog`
 * [later](https://github.com/microsoft/TypeScript/issues/49415#issuecomment-5600287959) **RyanCavanaugh** reported that window.opener was still declared as any in TS 4.7.3 and provided a reproduction snippet demonstrating the issue
 * (later) **RyanCavanaugh** added label `Needs Human Review`, and assigned to **Copilot**, **RyanCavanaugh**

### [Issue microsoft/TypeScript#49511](https://github.com/microsoft/TypeScript/issues/49511) (Closed, `Bug`, `Fixed`, `Help Wanted`, `Domain: This-Typing`, `Needs Human Review`)

**Return type is \`any\` of getter in object passed as generic **

*In TypeScript, passing an inline object containing a getter and method to a generic function causes the getter’s return type to be inferred as any.*

 * [4.2 years ago](https://github.com/microsoft/TypeScript/issues/49511#issuecomment-1155606111) **craigphicks** noted that resolveCallExpression in src/compiler/checker.ts was related
 * [2.3 years ago](https://github.com/microsoft/TypeScript/issues/49511#issuecomment-2102266999) **lqzhgood** said "https://github.com/microsoft/TypeScript/issues/58483"
 * **RyanCavanaugh** added label `Domain: This-Typing`
 * [later](https://github.com/microsoft/TypeScript/issues/49511#issuecomment-5600993814) **RyanCavanaugh** mentioned that the issue was fixed by PR #62243 and described how type inference behavior changed across TypeScript versions
 * (later) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#49526](https://github.com/microsoft/TypeScript/issues/49526) (Open, `Bug`, `Help Wanted`, `Domain: lib.d.ts`, `Docs`, `Needs Human Review`)

**Document the Iterator, Iterable, IterableIterator types**

*Document TypeScript’s standard Iterator, Iterable, and IterableIterator interfaces to clarify their usage.*

 * (4.2 years ago) **RyanCavanaugh** added labels `Help Wanted`, `Domain: lib.d.ts`, and set milestone to `Backlog`
 * (later) **RyanCavanaugh** added labels `Docs`, `Needs Human Review`

### [Issue microsoft/TypeScript#49561](https://github.com/microsoft/TypeScript/issues/49561) (Open, `Bug`, `Help Wanted`, `Domain: lib.d.ts`, `Docs`, `Needs Human Review`)

**Docs of \`charCodeAt\` and \`codePointAt\` are flipped**

*JSDoc descriptions for charCodeAt and codePointAt are reversed in TypeScript’s standard library definitions.*

 * [4.2 years ago](https://github.com/microsoft/TypeScript/issues/49561#issuecomment-1156904132) **fatcerberus** noted that the approach would break apart surrogate pairs and increase garbage collection pressure by creating temporary arrays
 * [4.2 years ago](https://github.com/microsoft/TypeScript/issues/49561#issuecomment-1156905868) **Ciantic** noted interest and suggested updating the docs to clarify that Unicode points typically have glyphs but char codes are just bits
 * **RyanCavanaugh** added to milestone `Backlog`
 * (later) **RyanCavanaugh** added labels `Docs`, `Needs Human Review`

### [Issue microsoft/TypeScript#49609](https://github.com/microsoft/TypeScript/issues/49609) (Closed, `Bug`, `Fixed`, `Help Wanted`, `Domain: lib.d.ts`, `Needs Human Review`)

**AbortController\.abort is missing in lib\.webworker\.d\.ts**

*TypeScript's lib.webworker.d.ts omits the AbortController.abort method, leading to type errors in workers.*

 * [3.9 years ago](https://github.com/microsoft/TypeScript/issues/49609#issuecomment-1281801231) **Tarrowren** provided tsconfig configurations and advised setting types to [] to exclude @types/node so that AbortController.abort need not be removed from lib.webworker.d.ts
 * [3.8 years ago](https://github.com/microsoft/TypeScript/issues/49609#issuecomment-1316473179) **Shin-Ogata** said "I've confirmed that the latest 4.9.3 fixes this issue. 👍 "
 * **RyanCavanaugh** added label `Domain: lib.d.ts`
 * [later](https://github.com/microsoft/TypeScript/issues/49609#issuecomment-5601152271) **RyanCavanaugh** reported that the issue was fixed in 4.9.0-dev.20221026 and that current TypeScript versions compile the example
 * (later) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#49638](https://github.com/microsoft/TypeScript/issues/49638) (Open, `Bug`, `Help Wanted`, `Domain: Mapped Types`, `Needs Human Review`)

**Combination of intersection type, mapped type and generic type seem to break type checks for nested properties**

*A generic function using an intersection and mapped type improperly permits extra nested properties in TS 4.7.4.*

 * [4.2 years ago](https://github.com/microsoft/TypeScript/issues/49638#issuecomment-1163463509) **SevInf** thanked ahejlsberg and asked whether the same issue occurred for another example with an optional 'where' property causing an excess property error
 * [4.2 years ago](https://github.com/microsoft/TypeScript/issues/49638#issuecomment-1163472513) **ahejlsberg** said "Hmm, yeah, something is definitely suspicious there."
 * **RyanCavanaugh** added label `Domain: Mapped Types`
 * [later](https://github.com/microsoft/TypeScript/issues/49638#issuecomment-5601082112) **RyanCavanaugh** explained that excess-property checking doesn't apply to generic inference and noted that the optional-`where` variation is now accepted in TypeScript 6.0.3
 * **RyanCavanaugh** added label `Needs Human Review`

### [Issue microsoft/TypeScript#49683](https://github.com/microsoft/TypeScript/issues/49683) (Closed, `Bug`, `Fixed`, `Help Wanted`, `Domain: lib.d.ts`, `Needs Human Review`)

**Undeprecate navigator\.platform**

*Remove the incorrect deprecation marker from navigator.platform in TypeScript’s DOM library definitions.*

 * (4.1 years ago) **RyanCavanaugh** added labels `Help Wanted`, `Domain: lib.d.ts`, and set milestone to `Backlog`
 * [later](https://github.com/microsoft/TypeScript/issues/49683#issuecomment-5601152397) **RyanCavanaugh** noted that Navigator.platform is no longer marked deprecated in the generated DOM declarations, confirmed its availability in current browsers, and closed the issue as fixed
 * (later) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#49794](https://github.com/microsoft/TypeScript/issues/49794) (Closed, `Bug`, `Domain: API: Transforms`, `Rescheduled`, `Needs Human Review`, **navya9singh**)

**Crash when transformer mutates decorators on classes with initialized static fields**

*Applying a custom class decorator transformer to classes with initialized static fields causes an 'Invalid cast isCallExpression' crash in TypeScript.*

 * (2.1 years ago) **RyanCavanaugh** added label `Domain: Transforms`, set milestone to `TypeScript 5.7.0`, and removed from milestone `TypeScript 5.5.0`
 * [later](https://github.com/microsoft/TypeScript/issues/49794#issuecomment-5601082244) **RyanCavanaugh** said "This affects the pre-TypeScript-7 Compiler API transformer surface. That API has been superseded and is no longer being developed, so this crash cannot be taken as a current compiler change."
 * **RyanCavanaugh** added label `Needs Human Review`
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#50168](https://github.com/microsoft/TypeScript/issues/50168) (Closed, `Bug`, `Fixed`, `Help Wanted`, `Domain: lib.d.ts`, `Needs Human Review`)

**Symbol\.species should in constructor, not instance**

*Symbol.species is incorrectly declared on SharedArrayBuffer instances instead of its constructor in es2017.sharedmemory.d.ts.*

 * (4 years ago) **RyanCavanaugh** added labels `Help Wanted`, `Domain: lib.d.ts`, and set milestone to `Backlog`
 * [later](https://github.com/microsoft/TypeScript/issues/50168#issuecomment-5602375774) **RyanCavanaugh** stated that PR #61271 fixed the issue, described that Symbol.species is now a key of SharedArrayBufferConstructor under --lib es2017 --strict, and noted the affected nightly boundary and passing release versions
 * (later) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63844](https://github.com/microsoft/TypeScript/issues/63844) (Closed, `Crash`, **andrewbranch**)

**panic: cache entry not found \[recovered, repanicked\]**

*TypeScript server v7.0.0-dev panics with 'cache entry not found' while handling file open and config updates.*

 * [10 weeks ago](https://github.com/microsoft/TypeScript/issues/63844#issuecomment-5351505935) **RyanCavanaugh** said "@WerdoxDev thanks, confirmed this locally - the repro is contingent on opening mediasoup.ts + oxfmt.config.ts (I suspect any file from the repo root would do)"
 * [10 weeks ago](https://github.com/microsoft/TypeScript/issues/63844#issuecomment-5351505968) **RyanCavanaugh** said "Foolishly I didn't save my entire log when I reprod it, and now I can't repro it again. @WerdoxDev can you share a full log file by chance?"
 * [10 weeks ago](https://github.com/microsoft/TypeScript/issues/63844#issuecomment-5351505987) **WerdoxDev** attached the complete crash log from today's usage
 * [today](https://github.com/microsoft/TypeScript/issues/63844#issuecomment-5589779942) **andrewbranch** said "This was fixed by https://github.com/microsoft/typescript-go/pull/4457. "cache entry not found" no longer appears in crash telemetry for at least the last 30 days."
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript#63856](https://github.com/microsoft/TypeScript/issues/63856) (Open, `Needs Investigation`, **jakebailey**)

**tsc is not resposive to \`ctrl\-c\`**

*tsc fails to respond to ctrl-c due to incomplete propagation of signal handlers in typescript-go*

 * **RyanCavanaugh** added label `Needs Investigation`
 * [7 weeks ago](https://github.com/microsoft/TypeScript/issues/63856#issuecomment-5351507245) **anthonyshew** described that pnpm run dev:ts hung on one Ctrl+C and required three to exit, whereas pnpm exec tsc exited immediately
 * **RyanCavanaugh** added to milestone `TypeScript 7.1`
 * [today](https://github.com/microsoft/TypeScript/issues/63856#issuecomment-5591307178) **rafaelnajman** confirmed that tsc exits with code 0 on SIGINT and SIGTERM while SIGHUP yields code 129, reported pnpm parallel build runners leaking compiler processes, and provided a self-contained repro

### [Issue microsoft/TypeScript#63924](https://github.com/microsoft/TypeScript/issues/63924) (Closed, `Suggestion`, `Infrastructure`, `Domain: Editor/VS Code Extension`, **jakebailey**)

**Decouple extension publishing from TS compiler**

*Decouple the TS 7 extension’s build and packaging from the TypeScript compiler to enable separate Insiders publishing and future built-in distribution*

 * **DanielRosenwasser** added label `Domain: Editor/VS Code Extension`
 * (1 week ago) **jakebailey** added label `Infrastructure`, and set milestone to `TypeScript 7.1.0 Beta`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64063](https://github.com/microsoft/TypeScript/pull/64063) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Ditch nodeData interface in favor of generated accessors**

*Replacing the dynamic nodeData interface with generated accessors for AST nodes reduces size and speeds compilation.*

 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64063#issuecomment-5499686412) **typescript-automation[bot]** announced that performance tests started and provided links to build status and results
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64063#issuecomment-5500018137) **typescript-automation[bot]** provided the requested performance run results
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64063#issuecomment-5500189461) **jakebailey** said "Hm, there's something to this, I think, I need to investigate."
 * [today](https://github.com/microsoft/TypeScript/pull/64063#issuecomment-5592560452) **jakebailey** reintroduced indirection to recover lost performance and noted it made the binary smaller

### [PR microsoft/TypeScript#64115](https://github.com/microsoft/TypeScript/pull/64115) (Open, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Add optional VFS parameters to updateSnapshot**

*Add optional VFS parameters to updateSnapshot with helpers for in-memory or layered file systems supporting fallback, symlinks, and removed paths.*

 * [5 days ago](https://github.com/microsoft/TypeScript/pull/64115#issuecomment-5530854700) **andrewbranch** asked about renaming createCacheFileSystem to createOverlayFileSystem or createOverlays and mentioned planning other snapshot/state model changes
 * [5 days ago](https://github.com/microsoft/TypeScript/pull/64115#issuecomment-5532864937) **weswigham** suggested renaming functions to use "Layer" instead of "overlay" to avoid confusion with overlayFS on the backend
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/64115#issuecomment-5545907874) **andrewbranch** argued that lazy compaction complexity outweighed its benefits, proposed and prototyped an eager clone-on-construction design that removed synchronization code, presented benchmarks showing faster reads/releases but slower snapshot creation, and concluded that eager compaction simplifies code with similar overall performance
 * [today](https://github.com/microsoft/TypeScript/pull/64115#issuecomment-5592043031) **weswigham** updated to main and swapped to eager layer compaction to optimize for reads, mentioning future toggles if needed

### [PR microsoft/TypeScript#64139](https://github.com/microsoft/TypeScript/pull/64139) (Closed, `Author: Team`, `For Milestone Bug`, **jakebailey**)

**Add independent VS Code extension releases**

*Automate version bumping, tagging, building, signing, and manual publishing of the VS Code extension via GitHub Actions and Azure pipelines.*

 * (6 days ago) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Milestone Bug`, and removed label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64139#issuecomment-5593037602) **jakebailey** mentioned planning to add the playbook to the repo or wiki
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#64143](https://github.com/microsoft/TypeScript/issues/64143) (Closed, `Bug`, **gabritto**)

**readonly is accepted in ambient module import attributes types**

*Ambient module import attributes types in TypeScript incorrectly allow the readonly modifier, leading to ambiguous module matching and merging.*

 * (4 days ago) **RyanCavanaugh** set milestone to `TypeScript 7.1.0 Beta`, removed from milestone `Dormant`, and assigned to **gabritto**
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript#64157](https://github.com/microsoft/TypeScript/pull/64157) (Closed, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Add defer functionality to generator executor**

*Implement a defer function in the api.batch generator executor to queue non-blocking tasks in the current batch context.*

 * (5 days ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **weswigham**
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript#64161](https://github.com/microsoft/TypeScript/pull/64161) (Closed, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Add a \`npx hereby validate\` command to group all repo validations**

*Introduce an npx hereby validate command to run and manage all repository validations in a single step.*

 * (5 days ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **weswigham**
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript#64172](https://github.com/microsoft/TypeScript/pull/64172) (Open, `For Backlog Bug`)

**Infer recursive types through object literal getters**

*Fix recursive type inference in object getters by adding a recursion-depth sentinel to avoid circular resolution errors*

 * created by **colinhacks**
 * (4 days ago) **typescript-automation[bot]** added labels `For Backlog Bug`, `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64172#issuecomment-5591499161) **RyanCavanaugh** demonstrated unsoundness in the unwind mechanism by reproducing four deterministic failures with detailed build information and stack traces
 * [today](https://github.com/microsoft/TypeScript/pull/64172#issuecomment-5593017044) **jakebailey** provided a proof-of-concept implementation using Astra via linked branch and commit
 * [today](https://github.com/microsoft/TypeScript/pull/64172#issuecomment-5594267273) **colinhacks** thanked and described a feature request for improved recursive inference support and input constraints in z.object
 * [today](https://github.com/microsoft/TypeScript/pull/64172#issuecomment-5595011378) **jakebailey** said "Pushed even more code to my branch, which seems to get rid of all errors from your "Zod with every workaround removed" checkout."

### [PR microsoft/TypeScript#64177](https://github.com/microsoft/TypeScript/pull/64177) (Open, `For Backlog Bug`)

**fix\(auto\-import\): don't suggest \# imports that only resolve via condition fallback**

*Update auto-import to no longer suggest imports that resolve only through conditional fallbacks, matching Node’s first-match resolution.*

 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/64177#issuecomment-5549432171) **marwan562** said "@microsoft-github-policy-service agree"
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/64177#issuecomment-5549470668) **marwan562** addressed Copilot comments, updated array and nested conditional handling, added deeper-nesting tests, and confirmed all module specifiers tests passed
 * [today](https://github.com/microsoft/TypeScript/pull/64177#issuecomment-5591820174) **marwan562** described updates to string validity and types-only arrays handling, added suppression for empty and invalid arrays, added a regression test, and noted tests passed before requesting @copilot review

### [PR microsoft/TypeScript#64178](https://github.com/microsoft/TypeScript/pull/64178) (Open, `For Milestone Bug`, **andrewbranch**)

**Prevent deadlock in \`getCompletionsAtPosition\(\.\.\., { includeSymbol: true }\)\` API**

*Remove the program.GetTypeChecker call from getExistingImports and explicitly pass the checker to avoid deadlock in getCompletionsAtPosition with includeSymbol enabled.*

 * created by **auvred**
 * (4 days ago) **typescript-automation[bot]** added label `For Milestone Bug`, and assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript/pull/64178#issuecomment-5597219608) **auvred** said "Fixed the lint error, hadn't noticed it before 🤷‍♂️ "

### [PR microsoft/TypeScript#64181](https://github.com/microsoft/TypeScript/pull/64181) (Closed, `For Milestone Bug`, **gabritto**)

**Disallow 'readonly' modifier in ambient module import attributes types**

*Add TS1558 diagnostic to reject 'readonly' modifiers on import attributes type properties in ambient module declarations.*

 * (3 days ago) **typescript-automation[bot]** added label `For Milestone Bug`, and assigned to **gabritto**
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/64181#issuecomment-5554336440) **erantianantha** said "@microsoft-github-policy-service agree"
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript#64184](https://github.com/microsoft/TypeScript/pull/64184) (Closed, `For Uncommitted Bug`, **andrewbranch**)

**Fix RefCountCache\.Ref panic race between concurrent snapshot builds**

*Concurrent snapshot building in the TypeScript language server can cause RefCountCache.Ref to panic due to a cache entry race condition.*

 * (2 days ago) **typescript-automation[bot]** added label `For Uncommitted Bug`, and assigned to **andrewbranch**
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/64184#issuecomment-5563109701) **NAVEENKUMARKR777** said "@microsoft-github-policy-service agree"
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript#64185](https://github.com/microsoft/TypeScript/issues/64185) (Closed, `Won't Fix`, `Cursed?`)

**Parenthesized computed method names change import\-alias resolution and emitted JavaScript after namespace merging**

*Parenthesizing a computed static method name leads to import alias removal and incorrect emitted JavaScript behavior.*

 * created by **magic-akari**
 * (today) **RyanCavanaugh** added labels `Cursed?`, `Won't Fix`
 * [today](https://github.com/microsoft/TypeScript/issues/64185#issuecomment-5592576942) **RyanCavanaugh** explained why fixing the inconsistency would break existing programs and noted the intentional behavior for type-only targets
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#64186](https://github.com/microsoft/TypeScript/issues/64186) (Open, `Possible Improvement`)

**Narrowing of generic this is inconsistent with variable narrowing**

*TypeScript narrows generic this types inconsistently compared to generic parameters, resulting in unexpected union narrowing behavior.*

 * created by **Andarist**
 * (today) **RyanCavanaugh** added label `Possible Improvement`, and set milestone to `Backlog`

### [PR microsoft/TypeScript#64187](https://github.com/microsoft/TypeScript/pull/64187) (Open, `For Backlog Bug`)

**Fix narrowing of generic this parameters**

*Fix incorrect narrowing of generic this parameters to restore expected type inference behavior.*

 * created by **Andarist**
 * (yesterday) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64187#issuecomment-5589458597) **jakebailey** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/64187#issuecomment-5589459645) **typescript-automation[bot]** reported build jobs status updates
 * [today](https://github.com/microsoft/TypeScript/pull/64187#issuecomment-5589859371) **typescript-automation[bot]** posted the requested perf run results comparing baseline and PR builds for tsc
 * [today](https://github.com/microsoft/TypeScript/pull/64187#issuecomment-5590014370) **typescript-automation[bot]** reported tsc user test results comparing main and the pull request merge, noted two package install and one git clone infrastructure failures, but said everything else looked good
 * [today](https://github.com/microsoft/TypeScript/pull/64187#issuecomment-5590509687) **typescript-automation[bot]** reported that tests comparing main and the pull request merge across the top 400 repositories passed without issues
 * (today) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`

### [PR microsoft/TypeScript#64188](https://github.com/microsoft/TypeScript/pull/64188) (Open, `For Uncommitted Bug`)

**Skip object classification for shared type facts**

*Skip object classification checks for shared type facts to reduce redundant isEmptyObjectType and isFunctionObjectType calls.*

 * created by **Andarist**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64188#issuecomment-5568531975) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [today](https://github.com/microsoft/TypeScript/pull/64188#issuecomment-5589444983) **jakebailey** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/64188#issuecomment-5589446032) **typescript-automation[bot]** posted an automated status update listing build jobs and their statuses with result links
 * [today](https://github.com/microsoft/TypeScript/pull/64188#issuecomment-5589784192) **typescript-automation[bot]** reported the performance run results in a detailed comparison report
 * [today](https://github.com/microsoft/TypeScript/pull/64188#issuecomment-5589784504) **typescript-automation[bot]** reported user test results, noted infrastructure failures unrelated to the change, and confirmed everything else looked good
 * [today](https://github.com/microsoft/TypeScript/pull/64188#issuecomment-5590335811) **typescript-automation[bot]** reported that running the top 400 repos with tsc comparing main and refs/pull/64188/merge looked good

### [Issue microsoft/TypeScript#64189](https://github.com/microsoft/TypeScript/issues/64189) (Open, `API Request`, **andrewbranch**)

**Add \`GenericType\` type to the API**

*Add a GenericType type to the API to represent TypeReference targets and expose their typeParameters.*

 * created by **mrazauskas**
 * (today) **RyanCavanaugh** added label `API Request`, and assigned to **andrewbranch**

### [PR microsoft/TypeScript#64190](https://github.com/microsoft/TypeScript/pull/64190) (Open, `For Uncommitted Bug`, **andrewbranch**)

**\[api\] Add \`GenericType\` type**

*Adds a missing GenericType type definition to the TypeScript compiler API.*

 * created by **mrazauskas**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * **typescript-automation[bot]** assigned to **andrewbranch**

### [PR microsoft/TypeScript#64191](https://github.com/microsoft/TypeScript/pull/64191) (Open, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**, **jakebailey**)

**Fix FSEvents routing for differently cased watch paths**

*Modify FSEvents routing logic to handle watch paths that differ only by case correctly.*

 * (yesterday) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript/pull/64191#issuecomment-5588265990) **jakebailey** described experimenting with Astra over the weekend, noting that it fixed everything; observed incorrect path casing in tspath; stated intention to keep fswatch self-contained and possibly reuse performance improvements for tspath’s ContainsPath checks
 * [today](https://github.com/microsoft/TypeScript/pull/64191#issuecomment-5588316346) **jakebailey** mentioned that kqueue on macOS also had the filename case sensitivity problem and that macOS was the only BSD with canonically insensitive filenames
 * [today](https://github.com/microsoft/TypeScript/pull/64191#issuecomment-5591021718) **jakebailey** noted that the fix resolved fswatch itself but its callers’ path checks could still cause confusion and investigated further

### [Issue microsoft/TypeScript#64192](https://github.com/microsoft/TypeScript/issues/64192) (Open, `Needs Investigation`, **ahejlsberg**)

**Recursive inference through self\-referential object literals**

*Self-referential getters for recursive schemas trigger TypeScript's self-reference errors collapsing to implicit any, requiring Zod-style workarounds.*

 * created by **colinhacks**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript/issues/64192#issuecomment-5594283251) **colinhacks** cross-posted a link to TypeScript PR 64172 for context, highlighted recursive type inference as a high-impact challenge, described Zod 4's loosened type safety workaround, and requested a solution preserving type safety

### [Issue microsoft/TypeScript#64196](https://github.com/microsoft/TypeScript/issues/64196) (Closed)

**Native \`tsc\` ignores SIGINT and SIGTERM while compiling — Ctrl\-C does not interrupt a build, and the process exits 0**

*Native TypeScript compiler version 7 ignores SIGINT and SIGTERM during builds, making Ctrl-C ineffective and returning exit code 0.*

 * created by **rafaelnajman**
 * [today](https://github.com/microsoft/TypeScript/issues/64196#issuecomment-5591033497) **RyanCavanaugh** said "What's the difference between this and #63856?"
 * [today](https://github.com/microsoft/TypeScript/issues/64196#issuecomment-5591317690) **rafaelnajman** closed the issue as a duplicate of #63856 and added missing details to that issue
 * (today) **rafaelnajman** closed the issue
 * (today) **rafaelnajman** closed the issue

### [Issue microsoft/TypeScript#64197](https://github.com/microsoft/TypeScript/issues/64197) (Open, `Duplicate`)

**Excess property checks silently skipped for nested object literals at reverse\-mapped\-type inference sites \(regression in 6\.0\)**

*TypeScript 6.0 regression stops flagging excess properties on nested object literals in generic reverse-mapped type inference.*

 * created by **quithyot**
 * [today](https://github.com/microsoft/TypeScript/issues/64197#issuecomment-5584520796) **MartinJohns** said "Very likely a duplicate of #64006."
 * [today](https://github.com/microsoft/TypeScript/issues/64197#issuecomment-5590744319) **RyanCavanaugh** confirmed that the issue also bisected to #62722 and linked to a related comment
 * **RyanCavanaugh** added label `Duplicate`

### [Issue microsoft/TypeScript#64198](https://github.com/microsoft/TypeScript/issues/64198) (Open, `Infrastructure`, **RyanCavanaugh**, **Copilot**)

**Perhaps there is an incorrect test directive in \`useStrictLikePrologueString01\`**

*The test useStrictLikePrologueString01.ts uses //@target: commonjs instead of //@module: commonjs, indicating an incorrect directive.*

 * created by **bvanjoi**
 * [today](https://github.com/microsoft/TypeScript/issues/64198#issuecomment-5589499131) **RyanCavanaugh** said "It's weird the harness didn't error on this - it really should! I doubt this is the only mistake like this we've made."
 * (today) **RyanCavanaugh** added label `Infrastructure`, set milestone to `Backlog`, and assigned to **Copilot**, **RyanCavanaugh**

### [PR microsoft/TypeScript#64199](https://github.com/microsoft/TypeScript/pull/64199) (Open, `For Backlog Bug`)

**Fix: disallow optional call chaining on import\.defer expressions \(\#63679\)**

*Prevent optional call chaining on import.defer expressions by adding grammar and parser checks to trigger an error*

 * created by **vaibhavsrv**
 * (today) **typescript-automation[bot]** added labels `For Backlog Bug`, `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64199#issuecomment-5588637186) **vaibhavsrv** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript/pull/64199#issuecomment-5588637530) **vaibhavsrv** thanked jakebailey, apologized for fixture confusion, reverted fixture changes, and updated the branch to include only Go compiler fixes, a test case, and reference baselines

### [PR microsoft/TypeScript#64200](https://github.com/microsoft/TypeScript/pull/64200) (Open, `For Uncommitted Bug`, **RyanCavanaugh**, **Copilot**)

**Error on conflicting global test directives; fix tests with duplicate directives**

*Enforce errors on duplicate conflicting global test directives in the Go test harness and update affected tests.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * (today) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Milestone Bug`, `For Uncommitted Bug`, and removed labels `For Uncommitted Bug`, `For Milestone Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64200#issuecomment-5591110687) **Copilot** described adding validation of enum/boolean compiler-option directive values in tests, gated behind a new flag, and accounting for trailing semicolons

### [PR microsoft/TypeScript#64201](https://github.com/microsoft/TypeScript/pull/64201) (Open, `Author: Team`, `For Uncommitted Bug`, **RyanCavanaugh**)

**Restack skill**

*Add a Restack skill that formats PR commit histories for easier review*

 * created by **RyanCavanaugh**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **RyanCavanaugh**

### [PR microsoft/TypeScript#64202](https://github.com/microsoft/TypeScript/pull/64202) (Closed, `For Uncommitted Bug`)

**Fix typos and grammatical issues across codebase**

*Correct spelling and grammar errors across compiler internals, transformers, language service components, and build pipelines.*

 * created by **aguashui**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64202#issuecomment-5591365363) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [today](https://github.com/microsoft/TypeScript/pull/64202#issuecomment-5592660373) **RyanCavanaugh** said "https://github.com/microsoft/TypeScript/blob/main/.github/pull_request_template.md?plain=1#L15"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#64203](https://github.com/microsoft/TypeScript/issues/64203) (Open, `Unactionable`)

**\`\-\-stableTypeOrdering\` defects: compiler hang \(NaN in \`compareNodes\`\), missing \`BigIntLiteral\`, primitive alias bypass, and mapper omissions**

*The --stableTypeOrdering compiler option hangs due to NaN in compareNodes and misorders BigIntLiteral, primitive aliases, and type mappers.*

 * created by **trevorade**
 * [today](https://github.com/microsoft/TypeScript/issues/64203#issuecomment-5592477321) **RyanCavanaugh** noted that the API sample did not hang and no reads of `syntheticFile` occurred; clarified that falling back to declaration order matches 7.0 behavior and explained that unsorted bigints in 7.0 are harmless since bigint literals lack mutual assignability issues
 * **RyanCavanaugh** added label `Unactionable`
 * [today](https://github.com/microsoft/TypeScript/issues/64203#issuecomment-5592506665) **trevorade** apologized and described a fix to compareNodes that safely handled missing fileIndexMap entries and undefined node positions to avoid NaN and infinite hangs
 * [today](https://github.com/microsoft/TypeScript/issues/64203#issuecomment-5592602239) **RyanCavanaugh** said "It sounds like maybe your createProgram call and/or host made some conflicting statements about what files exist? Regardless, this doesn't sound like something we'd patch 6.0 for."
 * [today](https://github.com/microsoft/TypeScript/issues/64203#issuecomment-5597512492) **jakebailey** said "I noticed a few of these originally but avoided sending a PR to not have 6.0 differ, so 7.1 is definitely the right time to fix this class of problem "

### [PR microsoft/TypeScript#64204](https://github.com/microsoft/TypeScript/pull/64204) (Open, `Author: Team`, `For Milestone Bug`, **andrewbranch**)

**Replace \`api\.updateSnapshot\`**

*Replace api.updateSnapshot with api.getCurrentLanguageServerSnapshot and api.createSnapshot, remove latest snapshot tracking, and add snapshot.update operations for creating and ensuring programs.*

 * created by **andrewbranch**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Milestone Bug`, and assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript/pull/64204#issuecomment-5594173035) **andrewbranch** said "I have a refactor on top of this to use strongly typed project IDs that are not just tspath.Path, but it was a big diff so I didn't include it in this branch. It's a very nice cleanup though."

### [PR microsoft/TypeScript#64205](https://github.com/microsoft/TypeScript/pull/64205) (Open, `For Uncommitted Bug`)

**fix\(project\): re\-read cached file contents on didChangeWatchedFiles Created event**

*Improve file-watching to process 'Created' events and reload cached files, preventing stale diagnostics after atomic saves.*

 * created by **erantianantha**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [PR microsoft/TypeScript#64206](https://github.com/microsoft/TypeScript/pull/64206) (Closed, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Benchmark generator API, fix performance of nested \`all\` calls**

*Deferring nested `all` calls to the host executor eliminates their performance overhead and stabilizes benchmark generator execution.*

 * created by **weswigham**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`, and assigned to **weswigham**
 * [today](https://github.com/microsoft/TypeScript/pull/64206#issuecomment-5593558675) **weswigham** apologized to @andrewbranch and described finding modest but meaningful performance gains by using a class implementing the iterator protocol over a native generator for hoisted messages
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript#64207](https://github.com/microsoft/TypeScript/pull/64207) (Closed, `For Uncommitted Bug`, `dependencies`, `javascript`)

**Bump js\-yaml from 4\.3\.1 to 4\.3\.2**

*Upgrade js-yaml dependency from 4.3.1 to 4.3.2 to incorporate merge size limits and security fixes.*

 * created by **dependabot[bot]**
 * (today) **dependabot[bot]** added labels `dependencies`, `javascript`, `dependencies`, `javascript`
 * (today) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`, `For Uncommitted Bug`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64208](https://github.com/microsoft/TypeScript/pull/64208) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Keep computed\-name reconstruction out of symbol tracking**

*Prevent computed-name reconstruction during symbol tracking by adding a test and implementing a fix for #63986.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#64209](https://github.com/microsoft/TypeScript/pull/64209) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Run extension tagging on main**

*Adjust extension tagging workflow to run on the main branch after GitHub security changes caused #64139 to fail.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64210](https://github.com/microsoft/TypeScript/pull/64210) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Fix case sensitivity fswatch and users**

*Enhance filesystem watching to correctly handle case-insensitive macOS paths using a new watchalias package and compiler bookkeeping*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#64211](https://github.com/microsoft/TypeScript/pull/64211) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Use gotestsum as a Go tool**

*Integrate gotestsum as a Go tool to silence unpinned dependency alerts and streamline the test experience.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#64212](https://github.com/microsoft/TypeScript/pull/64212) (Open, `For Uncommitted Bug`, **RyanCavanaugh**, **Copilot**)

**Type \`window\.opener\` as nullable \`WindowProxy\`**

*Type window.opener and global opener as nullable WindowProxy and add regression tests confirming their types.*

 * created by **Copilot**
 * (later) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * (later) **typescript-automation[bot]** added labels `For Milestone Bug`, `For Uncommitted Bug`, and removed label `For Milestone Bug`

### [Issue microsoft/TypeScript#64213](https://github.com/microsoft/TypeScript/issues/64213) (Open)

**The \`strict\` option is confusing since TypeScript 6**

*TypeScript 6 makes strict true by default and false disables multiple strict checks, reversing its original purpose and confusing users.*

 * created by **remcohaszing**
 * [later](https://github.com/microsoft/TypeScript/issues/64213#issuecomment-5603937116) **RyanCavanaugh** questioned who benefits from the proposal and asked for evidence of confusion around strict

