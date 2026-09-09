# Report for 2026-09-04 (Friday, September 4th, 2026)

15 different users commented on 73 different issues.

## Recommended Actions

 * Moderation
    * @KostAlex07 posted a promotional link to an npm package in [microsoft/TypeScript#37792](https://github.com/microsoft/TypeScript/issues/37792#issuecomment-5546771081)
 * Response Recommended
    * @Squidgical asked for an update on the reverted change and its status in the latest release in [microsoft/TypeScript#33014](https://github.com/microsoft/TypeScript/issues/33014#issuecomment-5550932442)
    * @jeffwklein reported issues upgrading to mobx 7 due to tsconfig decorator changes in [microsoft/TypeScript#54240](https://github.com/microsoft/TypeScript/issues/54240#issuecomment-5547308758)
    * @typescript-automation posted test failures requiring maintainer review in [microsoft/TypeScript#64162](https://github.com/microsoft/TypeScript/pull/64162#issuecomment-5548332461)
    * @typescript-automation[bot] provided performance run results as requested in [microsoft/TypeScript#64162](https://github.com/microsoft/TypeScript/pull/64162#issuecomment-5548340379)

## Activity Summary

### [Issue microsoft/TypeScript#31667](https://github.com/microsoft/TypeScript/issues/31667) (Closed, `Bug`, `Needs More Info`, `Domain: JavaScript`)

**Type narrowing in checked JS in module scope doesn't work**

*In checked JavaScript module scope TypeScript doesn’t apply instanceof type narrowing for variables, although it works inside functions.*

 * (2 days ago) **RyanCavanaugh** added labels `Needs Human Review`, `Needs More Info`
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/31667#issuecomment-5517413492) **TedDriggs** said "I have changed companies since filing this. I no longer have access, and am not inclined to re-create a repro."
 * **RyanCavanaugh** removed label `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#33014](https://github.com/microsoft/TypeScript/issues/33014) (Open, `Suggestion`, `In Discussion`, **gabritto**)

**Suggestion for Dependent\-Type\-Like Functions: Conservative Narrowing of Generic Indexed Access Result Type**

*Enhance TypeScript’s type checker to conservatively narrow generic indexed access return types for dependent-type-like functions without new syntax.*

 * (1.8 years ago) **gabritto** closed the issue
 * [1.5 years ago](https://github.com/microsoft/TypeScript/issues/33014#issuecomment-2691314016) **jakebailey** said "Reopening this, since it was reverted in #61136 (but planned for 5.9)."
 * (1.5 years ago) **jakebailey** reopened the issue
 * [later](https://github.com/microsoft/TypeScript/issues/33014#issuecomment-5550932442) **Squidgical** asked for an update on the reverted change and its status in version 7.0.2

### [Issue microsoft/TypeScript#33101](https://github.com/microsoft/TypeScript/issues/33101) (Closed, `Bug`, `Fixed`, `Domain: check: Type Inference`)

**Union types and overloads acts a bit weirdly**

*An overloaded method on a Foo|Bar union incorrectly yields string|Bar for a string overload, whereas object returns behave correctly.*

 * (2 days ago) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (2 days ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#33462](https://github.com/microsoft/TypeScript/issues/33462) (Closed, `Bug`, `Domain: lib.d.ts`)

**document\.createTreewalker and document\.createNodeIterator have missing signature types that which are supported both in IE, Firefox and Chrome**

*TypeScript lib.dom.d.ts is missing IE-supported overloads for document.createTreeWalker and createNodeIterator filter functions and entityReferenceExpansion parameter.*

 * [2 days ago](https://github.com/microsoft/TypeScript/issues/33462#issuecomment-5517060560) **RyanCavanaugh** explained that TypeScript now accepts callable filters for createTreeWalker and createNodeIterator, noted that removing the fourth argument compiles without diagnostics, identified that TS2554 remains for entityReferenceExpansion due to WHATWG DOM definitions, recalled that the IE-specific overload was previously declined and declaration merging was recommended, and stated that lib.dom.d.ts will not include the retired fourth-argument extension
 * **RyanCavanaugh** added label `Needs Human Review`
 * (2 days ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#33654](https://github.com/microsoft/TypeScript/issues/33654) (Closed, `Bug`, `Fixed`, `Help Wanted`, `Domain: Intersection`)

**Intersection type with discriminated union type that includes all possible enum values cannot accept enum type**

*Intersecting a discriminated union with an additional field causes TypeScript to reject enum-typed discriminant assignments.*

 * (2 days ago) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (2 days ago) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** removed label `Needs Human Review`

### [Issue microsoft/TypeScript#33713](https://github.com/microsoft/TypeScript/issues/33713) (Closed, `Bug`, `Needs More Info`, `Needs Investigation`, `Domain: check: Type Circularity`)

**Language service fails to provide type info**

*The TypeScript language service on Windows 10 fails to show type information for recursive types, whereas it works as expected on Ubuntu.*

 * [2 days ago](https://github.com/microsoft/TypeScript/issues/33713#issuecomment-5518279971) **RyanCavanaugh** explained that both the recovered and current TypeScript versions return HTMLHeadingElement for quick-info and asked for the exact editor action or file change causing the transition or an archived tsserver trace
 * (2 days ago) **RyanCavanaugh** added labels `Needs Human Review`, `Needs More Info`
 * **RyanCavanaugh** removed label `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#37792](https://github.com/microsoft/TypeScript/issues/37792) (Closed, `Suggestion`, `Declined`)

**Support for Read\-only Typed Arrays**

*Provide a ReadonlyTypedArray<T> type to statically enforce immutability on TypedArray instances similar to ReadonlyArray<T>.*

 * [1.1 years ago](https://github.com/microsoft/TypeScript/issues/37792#issuecomment-3120737043) **yuhr** said "For those who want just an immutable byte array and don't need it to be an instance of TypedArray, Blob might be useful."
 * [48 weeks ago](https://github.com/microsoft/TypeScript/issues/37792#issuecomment-3344764992) **pNm193** suggested a ReadonlyTypedArray type for immutable typed arrays, described use cases and examples, and detailed workarounds and a compliance checklist
 * [37 weeks ago](https://github.com/microsoft/TypeScript/issues/37792#issuecomment-3646709265) **nonergodic** provided a fully airtight solution implementation with TypeScript code, explanation link, and tests link
 * [today](https://github.com/microsoft/TypeScript/issues/37792#issuecomment-5546771081) **KostAlex07** announced publication of an npm package offering deep immutable types and a readonly typed array

### [Issue microsoft/TypeScript#38700](https://github.com/microsoft/TypeScript/issues/38700) (Closed, `Bug`, `Domain: check: Type Inference`, `Needs Human Review`)

**Type is not inferred in an if branch of a user\-defined type guard when object is used for destructuring**

*Destructuring with a rest operator in a user-defined type guard branch isn't recognized as an object type by TypeScript.*

 * (6.2 years ago) **RyanCavanaugh** added labels `Bug`, `Domain: Type Inference`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/38700#issuecomment-5543733846) **RyanCavanaugh** explained that TreeNode is structurally assignable to RootTreeNode, causing the union to lack disjoint alternatives and trigger TS2700 on object-rest destructuring, and showed how adding `[VALUE]?: never` enforces mutual exclusivity to resolve the error
 * **RyanCavanaugh** added label `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#38748](https://github.com/microsoft/TypeScript/issues/38748) (Closed, `Bug`, `Fixed`, `Domain: check: Type Inference`, `Needs Human Review`)

**Function parameter that has inferred type has no intellisense in the return , while it has in the rest of the function body**

*Implicit any parameters in a generic TypeScript function do not trigger IntelliSense on returned values while explicit any parameters do.*

 * (6.2 years ago) **RyanCavanaugh** added labels `Bug`, `Domain: Type Inference`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/38748#issuecomment-5544195916) **RyanCavanaugh** reported that the issue was fixed in the current native TypeScript 7.1.0-dev, comparing completion behavior between 3.9.2 and the dev build
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#38838](https://github.com/microsoft/TypeScript/issues/38838) (Closed, `Bug`, `Fixed`, `Domain: lib.d.ts`, `Needs Human Review`)

**ElementCSSInlineStyle\.style should not be read\-only**

*TypeScript incorrectly treats ElementCSSInlineStyle.style as read-only, preventing string assignments supported by browsers.*

 * **RyanCavanaugh** added label `Domain: lib.d.ts`
 * [5.6 years ago](https://github.com/microsoft/TypeScript/issues/38838#issuecomment-762189791) **byterider** wondered why MDN warns against assigning a string directly to the style property
 * [2.2 years ago](https://github.com/microsoft/TypeScript/issues/38838#issuecomment-2121345153) **louwers** said "With https://github.com/microsoft/TypeScript/pull/53417 merged we can now add a mutable string setter."
 * [today](https://github.com/microsoft/TypeScript/issues/38838#issuecomment-5544805881) **RyanCavanaugh** described a TS2540 error when assigning to a.style in early dev builds, noted it was resolved in build 5.8.0-dev.20250123 and by PR #60987
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#39003](https://github.com/microsoft/TypeScript/issues/39003) (Closed, `Bug`, `Help Wanted`, `Domain: lib.d.ts`, `Needs Human Review`)

**HTMLFormControlsCollection namedItem should return only form input elements**

*TypeScript’s HTMLFormControlsCollection.namedItem method is incorrectly typed to return generic Element instead of specific form control types.*

 * **sandersn** added label `GraceHopperOSD`
 * [4.7 years ago](https://github.com/microsoft/TypeScript/issues/39003#issuecomment-974480436) **toofarm** said "Bumping this issue. The HTMLFormElement definition is causing erroneous errors in my code when I try to access a form element's value prop"
 * **RyanCavanaugh** removed label `PursuitFellowship`
 * [today](https://github.com/microsoft/TypeScript/issues/39003#issuecomment-5545683323) **RyanCavanaugh** explained that HTMLFormControlsCollection can include form-associated custom elements without a value property, making removal of Element unsound, and advised narrowing to specific element types before accessing value
 * **RyanCavanaugh** added label `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#39075](https://github.com/microsoft/TypeScript/issues/39075) (Closed, `Bug`, `Fixed`, `Domain: check: Type Inference`, `Needs Human Review`)

**Unable to cast to generic discriminated union**

*Casting a generic discriminated union in TypeScript 3.9.5 fails with TS2352 despite working in 3.8.3.*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [6.2 years ago](https://github.com/microsoft/TypeScript/issues/39075#issuecomment-644259861) **RyanCavanaugh** said "We should probably widen up the assertability constraint a little here"
 * **RyanCavanaugh** added label `Domain: Type Inference`
 * [today](https://github.com/microsoft/TypeScript/issues/39075#issuecomment-5546829408) **RyanCavanaugh** confirmed the issue was fixed in the 4.8.0-dev.20220528 and 7.1.0-dev.20260904.1 builds and linked the relevant pull request and commit
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#39133](https://github.com/microsoft/TypeScript/issues/39133) (Closed, `Bug`, `Domain: check: Type Inference`, `Needs Human Review`)

**Fails type check for type unions as keys to the Map constructor**

*TypeScript rejects Map<A|B,V> constructor calls when entry arrays contain both union key types.*

 * [2.8 years ago](https://github.com/microsoft/TypeScript/issues/39133#issuecomment-1787654132) **runarberg** suggested wrapping the tuple in an array and provided a corrected code diff
 * [2.8 years ago](https://github.com/microsoft/TypeScript/issues/39133#issuecomment-1787669167) **jonahallibone** acknowledged the missing array around the tuple and thanked for the correction
 * **RyanCavanaugh** added label `Domain: Type Inference`
 * [today](https://github.com/microsoft/TypeScript/issues/39133#issuecomment-5547164151) **RyanCavanaugh** explained the heterogeneous Map constructor inference limitation, referenced microsoft/TypeScript#37527, and recommended using explicit constructor type arguments or annotating an intermediate tuple array
 * **RyanCavanaugh** added label `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#39197](https://github.com/microsoft/TypeScript/issues/39197) (Closed, `Bug`, `Fixed`, `Domain: JS Emit`, `Needs Human Review`)

**duplicate Object\.defineProperty when code emit with re\-export a rename**

*TypeScript emits duplicate Object.defineProperty calls when re-exporting a renamed import from the same module*

 * (6.2 years ago) **RyanCavanaugh** added labels `Bug`, `Domain: JS Emit`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/39197#issuecomment-5548100954) **RyanCavanaugh** reported that PR #39213 fixed the duplicate alias issue and that newer dev builds emit a single defineProperty call
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#39500](https://github.com/microsoft/TypeScript/issues/39500) (Closed, `Bug`, `Fixed`, `Domain: Error Messages`, `Needs Human Review`)

**Unmet parameter type in function call is misleading the compiler when those parameters involve inherited interfaces**

*The compiler incorrectly highlights a type mismatch in generic inherited-interface arguments instead of reporting the missing param4 property.*

 * (6.1 years ago) **RyanCavanaugh** added labels `Bug`, `Domain: Error Messages`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/39500#issuecomment-5548493994) **RyanCavanaugh** reported that the issue was fixed in version 3.8.3, described updated diagnostic behavior in 4.2.0-dev, and linked to the PR and commit
 * (today) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#39520](https://github.com/microsoft/TypeScript/issues/39520) (Open, `Bug`, `Domain: Comment Emit`, `Needs Human Review`)

**Head comments are removed in some cases for next \`import\` line**

*TypeScript's compiler erroneously removes head comments preceding import statements when emitting JavaScript output.*

 * [6 years ago](https://github.com/microsoft/TypeScript/issues/39520#issuecomment-671269422) **Haroenv** demonstrated that multiline comments within an import preceded by a comma also triggered the issue and linked a reproduction example
 * [5.9 years ago](https://github.com/microsoft/TypeScript/issues/39520#issuecomment-695932911) **wclr** said "This happens if import after comments is removed while compilation (i.e imports only types)."
 * **RyanCavanaugh** added label `Domain: Comment Emit`
 * [today](https://github.com/microsoft/TypeScript/issues/39520#issuecomment-5548509341) **RyanCavanaugh** explained that TypeScript removes imports used only as types and does not guarantee comment preservation, and recommended using a specialized emit tool for exact comment retention
 * **RyanCavanaugh** added label `Needs Human Review`

### [Issue microsoft/TypeScript#39592](https://github.com/microsoft/TypeScript/issues/39592) (Closed, `Bug`, `Domain: check: Type Inference`, `Needs Human Review`)

**Incorrect type allowed in returned object **

*Optional p1 and p2 properties in the return disable type-checking for p4, letting it accept a number.*

 * (6.1 years ago) **RyanCavanaugh** added labels `Bug`, `Domain: Type Inference`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/39592#issuecomment-5548627990) **RyanCavanaugh** explained that the issue is a duplicate of #36945 and clarified how excess-property checking works for union types
 * **RyanCavanaugh** added label `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#39600](https://github.com/microsoft/TypeScript/issues/39600) (Closed, `Bug`, `Domain: check: Type Inference`, `Needs Human Review`)

**\`void\` parameter type produced from generic inference doesn't allow skipping as argument**

*Generic void parameter types incorrectly require arguments, unlike explicit void parameters which can be omitted.*

 * [2.3 years ago](https://github.com/microsoft/TypeScript/issues/39600#issuecomment-2062326197) **kalkronline** provided a minimal example demonstrating that calling comp_ck<void>() errors while void_ck() does not
 * **RyanCavanaugh** added label `Domain: Type Inference`
 * [30 weeks ago](https://github.com/microsoft/TypeScript/issues/39600#issuecomment-3842737535) **aweebit** provided a minimal reproducible example of the TypeScript issue and suggested a workaround using conditional rest parameters
 * [today](https://github.com/microsoft/TypeScript/issues/39600#issuecomment-5548732896) **RyanCavanaugh** explained that the generic void parameter-skipping behavior was tracked in #29131 and that a directly written void parameter may be omitted while a void type via generic or indexed access remains required
 * **RyanCavanaugh** added label `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#39650](https://github.com/microsoft/TypeScript/issues/39650) (Closed, `Bug`, `Domain: JSDoc`, `Has Repro`, `Needs Human Review`)

**In JSDoc @type is not a type declaration, which it is much more like type conversion\.**

*JSDoc @type acts as a type conversion rather than a declaration, preventing errors for extra object properties.*

 * [4.4 years ago](https://github.com/microsoft/TypeScript/issues/39650#issuecomment-1098590578) **typescript-bot** introduced the Repro bot and reported an error that 'moduleResolution=node10' is deprecated and suggested using 'ignoreDeprecations': '6.0'
 * [2.5 years ago](https://github.com/microsoft/TypeScript/issues/39650#issuecomment-1959702494) **rubiesonthesky** identified a typo in the repro code involving 'Entity' vs 'Entitiy'
 * **RyanCavanaugh** added label `Domain: JSDoc`
 * [today](https://github.com/microsoft/TypeScript/issues/39650#issuecomment-5549046661) **RyanCavanaugh** corrected the typo in the typedef name and confirmed that fixing it reproduces the expected error in TypeScript 4.0.2 and the current compiler
 * **RyanCavanaugh** added label `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#39811](https://github.com/microsoft/TypeScript/issues/39811) (Closed, `Bug`, `Fixed`, `Rescheduled`, `Domain: check: Error Instability`, `Needs Human Review`, **weswigham**)

**tsc reports error that LS does not**

*TypeScript's CLI build reports errors in SendThreadMachine.ts that the editor's language service does not surface when using tsconfig.build.json.*

 * (2.1 years ago) **RyanCavanaugh** added label `Domain: Error Instability`, set milestone to `TypeScript 5.7.0`, and removed from milestone `TypeScript 5.5.0`
 * [later](https://github.com/microsoft/TypeScript/issues/39811#issuecomment-5550142551) **RyanCavanaugh** reported that TypeScript 6.0.3's compiler and language service both reported the two TS2322 errors, while the current native compiler and language service both omitted those errors, resolving the previous disagreement
 * (later) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#39829](https://github.com/microsoft/TypeScript/issues/39829) (Open, `Bug`, `Domain: lib.d.ts`, `Needs Human Review`, **RyanCavanaugh**, **Copilot**)

**HTMLImageElement\#crossOrigin should use literal union type from allowable values**

*HTMLImageElement.crossOrigin property should use the literal union type 'anonymous' | 'use-credentials' instead of string|null.*

 * [4 years ago](https://github.com/microsoft/TypeScript/issues/39829#issuecomment-1212161808) **RemyMachado** described redefining the crossOrigin property type to avoid a TS2322 error
 * [2.7 years ago](https://github.com/microsoft/TypeScript/issues/39829#issuecomment-1861110701) **DvzH** reported that crossOrigin was being treated as a required prop in various UI libraries, causing errors in Material UI, Bootstrap, and others
 * [1.5 years ago](https://github.com/microsoft/TypeScript/issues/39829#issuecomment-2688915445) **machineghost** complained that a basic HTML bug was ignored for five years and argued for stricter TypeScript typing of the crossOrigin property based on the MDN reference
 * [later](https://github.com/microsoft/TypeScript/issues/39829#issuecomment-5550255858) **RyanCavanaugh** pointed out that HTMLImageElement.crossOrigin was declared as string|null allowing invalid values and suggested a more precise type for known CORS values
 * (later) **RyanCavanaugh** added label `Needs Human Review`, and assigned to **Copilot**, **RyanCavanaugh**

### [Issue microsoft/TypeScript#39918](https://github.com/microsoft/TypeScript/issues/39918) (Closed, `Bug`, `Fixed`, `checkJs`, `Domain: JavaScript`, `Needs Human Review`)

**Bogus "duplicate identifier" when checking JS code**

*Using allowJs and checkJs with a JSDoc-imported interface in JS incorrectly triggers a duplicate identifier error for the uploads property.*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [5.7 years ago](https://github.com/microsoft/TypeScript/issues/39918#issuecomment-734206955) **kazarmy** reported that using @type any or never achieved the same type inference and propagation as the documented workaround but was undocumented and could break in future TypeScript versions
 * **RyanCavanaugh** added label `Domain: JavaScript`
 * [later](https://github.com/microsoft/TypeScript/issues/39918#issuecomment-5550561562) **RyanCavanaugh** reported that the original allowJs/checkJs project produced TS2300 in TypeScript 3.9.2 and 6.0.3 but compiled without errors in TypeScript 7.0.0-dev and 7.1.0-dev, and that the TS7 JavaScript binder no longer treated the assignment as a duplicate declaration
 * (later) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#39948](https://github.com/microsoft/TypeScript/issues/39948) (Closed, `Bug`, `Fixed`, `Domain: enum`, `Needs Human Review`)

**\`in\` doesn't play good with enum**

*TypeScript's 'in' operator does not properly handle enum-defined keys for property checking and type narrowing.*

 * (6 years ago) **RyanCavanaugh** added labels `Bug`, `Domain: enum`, and set milestone to `Backlog`
 * [later](https://github.com/microsoft/TypeScript/issues/39948#issuecomment-5550682763) **RyanCavanaugh** confirmed that the enum-key form pt.B in el && el[pt.B] was accepted in 4.4.0-dev.20210730 and in current native TypeScript after previously reporting TS7053 in 4.4.0-dev.20210729
 * (later) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#39991](https://github.com/microsoft/TypeScript/issues/39991) (Closed, `Bug`, `Fixed`, `Help Wanted`, `Effort: Moderate`, `Domain: Error Messages`, `Needs Human Review`)

**\[feature request\] Better error messages for decorators \(they are completely not understandable\)**

*Improve TypeScript’s TS1240 decorator error message to clearly indicate when decorator descriptor parameters must be optional.*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [5.8 years ago](https://github.com/microsoft/TypeScript/issues/39991#issuecomment-720893748) **trusktr** provided a small reproduction on the TypeScript playground
 * [1.7 years ago](https://github.com/microsoft/TypeScript/issues/39991#issuecomment-2484294400) **Alexandrialexie** reported that the problem was resolved in v5.0.4 with an updated error message and asked if further changes were needed
 * [later](https://github.com/microsoft/TypeScript/issues/39991#issuecomment-5550906994) **RyanCavanaugh** reported that improved decorator diagnostics were introduced in TS 5.0.0-dev.20230120 via PR #50820, fixing the original property-decorator example issue
 * (later) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#40081](https://github.com/microsoft/TypeScript/issues/40081) (Closed, `Bug`, `Domain: Conditional Types`, `Needs Human Review`)

**Nested conditional type inconsistently causes error with annotations**

*Variable annotations in nested conditional types cause T to be inferred as an array union instead of the element type.*

 * (6 years ago) **RyanCavanaugh** added labels `Bug`, `Domain: Conditional Types`, and set milestone to `Backlog`
 * [later](https://github.com/microsoft/TypeScript/issues/40081#issuecomment-5551039359) **RyanCavanaugh** noted that the issue demonstrated the same nested conditional-type inference behavior as reported in issue #39409 and requested to track it there
 * **RyanCavanaugh** added label `Needs Human Review`
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#40205](https://github.com/microsoft/TypeScript/issues/40205) (Closed, `Bug`, `Fixed`, `Domain: Conditional Types`, `Needs Human Review`)

**Wrong function parameters length computing**

*TypeScript ignores parameter lists computed with conditional spread operators, causing incorrect function arity validation.*

 * (6 years ago) **RyanCavanaugh** added labels `Bug`, `Domain: Conditional Types`, and set milestone to `Backlog`
 * [later](https://github.com/microsoft/TypeScript/issues/40205#issuecomment-5550842861) **RyanCavanaugh** explained that the issue was fixed in 5.9.0-dev.20250220 by PR #56907 and that the compiler now reports TS2345 for the callback instead of accepting it
 * (later) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#40301](https://github.com/microsoft/TypeScript/issues/40301) (Closed, `Bug`, `Domain: Crashes`, `Needs Human Review`)

**Debug Failure\. Illegal value: 200 in signatureToSignatureDeclarationHelper**

*TypeScript crashes with 'Debug Failure. Illegal value: 200' in signatureToSignatureDeclarationHelper when linting node-zwave-js.*

 * (6 years ago) **RyanCavanaugh** added labels `Bug`, `Domain: Crashes`, and set milestone to `Backlog`
 * [later](https://github.com/microsoft/TypeScript/issues/40301#issuecomment-5551363874) **RyanCavanaugh** explained that the failure was caused by an invalid Compiler API call in @fimbul/mimir 0.21.0, noted that version 0.22.0 corrected the SyntaxKind to CallSignature, and recommended upgrading to resolve the error
 * **RyanCavanaugh** added label `Needs Human Review`
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#40393](https://github.com/microsoft/TypeScript/issues/40393) (Closed, `Bug`, `Fixed`, `Domain: check: Control Flow`, `Needs Human Review`)

**Type narrowing fails when there is a break/return in loop**

*Using break or return in a loop causes TypeScript to lose narrow type information after a type guard.*

 * [5.5 years ago](https://github.com/microsoft/TypeScript/issues/40393#issuecomment-773492950) **RyanCavanaugh** clarified that the third clause of the original poster's for loop wasn't unreachable and referenced issue #26914
 * [4.6 years ago](https://github.com/microsoft/TypeScript/issues/40393#issuecomment-1013523262) **iglosiggio** reported that the issue occurs when a break or continue is at the end of a loop and asked if control flow analysis unifies the loop's unreachable end with other continues
 * **RyanCavanaugh** added label `Domain: Control Flow`
 * [later](https://github.com/microsoft/TypeScript/issues/40393#issuecomment-5551974518) **RyanCavanaugh** reported that the issue was fixed in TypeScript 5.8.0-dev.20250123 and the native compiler while older versions still reported TS2365
 * (later) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#40873](https://github.com/microsoft/TypeScript/issues/40873) (Closed, `Bug`, `Fixed`, `Domain: Crashes`, `Needs Human Review`)

**Nested JSON makes tsc throw RangeError with no culprit**

*resolveJsonModule import of deeply nested JSON causes tsc to throw a RangeError and omit file reference.*

 * [5.9 years ago](https://github.com/microsoft/TypeScript/issues/40873#issuecomment-702319047) **RyanCavanaugh** said "I wouldn't be opposed to something like that with ~zeroish performance cost."
 * [5.9 years ago](https://github.com/microsoft/TypeScript/issues/40873#issuecomment-702414105) **pipobscure** suggested not typing .json imports and using any or unknown types possibly behind a typeJSON config flag
 * **RyanCavanaugh** added label `Domain: Crashes`
 * [later](https://github.com/microsoft/TypeScript/issues/40873#issuecomment-5552360849) **RyanCavanaugh** noted that the issue was fixed in the current native TypeScript 7.1.0-dev.20260905.1 but still reproduced in classic TypeScript, and provided reproduction details
 * (later) **RyanCavanaugh** added labels `Fixed`, `Needs Human Review`
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#54240](https://github.com/microsoft/TypeScript/issues/54240) (Open, `Suggestion`, `In Discussion`)

**Accessors should be allowed to be optional**

*Allow optional accessors in TypeScript to streamline decorator usage and match optional property behavior.*

 * [3 years ago](https://github.com/microsoft/TypeScript/issues/54240#issuecomment-1708838557) **justinfagnani** explained that although a code mod could handle dropping optionality and adding | undefined, not everyone will use it and it increases boilerplate for new code; argued that treating `?` as shorthand for `| undefined` is intuitive and consistent for auto-accessors
 * [1.8 years ago](https://github.com/microsoft/TypeScript/issues/54240#issuecomment-2442227079) **justinfagnani** complained about the extra boilerplate required for optional accessors when using decorators and requested optional accessor support to reduce verbosity
 * [32 weeks ago](https://github.com/microsoft/TypeScript/issues/54240#issuecomment-3780932892) **justinfagnani** said "We're still hearing complaints from Lit developers migrating to standard decorators that auto-accessors are painfully verbose."
 * [today](https://github.com/microsoft/TypeScript/issues/54240#issuecomment-5547308758) **jeffwklein** described encountering a cascading effect from removing experimentalDecorators when upgrading to mobx 7, requiring adding accessor to every lit decorator and forcing staying on mobx 6

### [Issue microsoft/TypeScript#61545](https://github.com/microsoft/TypeScript/issues/61545) (Closed, `Bug`, `Help Wanted`, `Domain: Declaration Emit`)

**Missing explicit return type for static methods using private static methods causes return type inference issues in declaration files**

*Public static methods returning private static methods generate invalid .d.ts declarations due to missing explicit return types.*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [1.3 years ago](https://github.com/microsoft/TypeScript/issues/61545#issuecomment-2798865136) **Teruk15** said "Hi!! may I work on this?"
 * **RyanCavanaugh** added label `Domain: Declaration Emit`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#62614](https://github.com/microsoft/TypeScript/issues/62614) (Closed, `Bug`, `Help Wanted`, `Domain: classes`)

**Private constructor in mixin causes "Cannot read properties of undefined \(reading 'declarations'\)"**

*A mixin combining two abstract classes with private constructors crashes the TypeScript compiler due to undefined declarations.*

 * (46 weeks ago) **RyanCavanaugh** added labels `Help Wanted`, `Domain: classes`, and set milestone to `Backlog`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#63325](https://github.com/microsoft/TypeScript/issues/63325) (Closed, `Bug`, `Help Wanted`, `Domain: lib.d.ts`)

**\`lib\.dom\.d\.ts\`: Keyframe interface should allow CSS Typed Object Model objects like CSSTransformValue, etc**

*The Keyframe interface in lib.dom.d.ts should accept CSS Typed Object Model types such as CSSTransformValue.*

 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63325#issuecomment-5492447922) **LeonxLJX** said "I'd like to take this one (`lib.dom.d.ts: Keyframe interface should allow CSS Typed Ob`). I'll look into the root cause and follow up with a PR. (claiming via @LeonxLJX)"
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63325#issuecomment-5492967321) **LeonxLJX** said "I'd like to take this one (`lib.dom.d.ts: Keyframe interface should allow CSS Typed Ob`). I'll dig into the root cause and follow up with a PR shortly. (claiming via @LeonxLJX)"
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63325#issuecomment-5492968303) **LeonxLJX** said "I'd like to take this one (`lib.dom.d.ts: Keyframe interface should allow CSS Typed Ob`). I'll look into the root cause and follow up with a PR. (claiming via @LeonxLJX)"
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#63703](https://github.com/microsoft/TypeScript/issues/63703) (Open, `Planning`)

**TypeScript 7\.1 Iteration Plan**

*Roadmap for TypeScript 7.1 detailing milestones and features across compiler, editor productivity, and performance enhancements.*

 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63703#issuecomment-5519354895) **Flarette** asked if the team planned to revisit instantiation depth limits in the tsgo compiler
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63703#issuecomment-5520213322) **jakebailey** stated that there were no plans to change the limits and referenced a related issue
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63703#issuecomment-5520894104) **Flarette** argued that compiler depth limits hinder progress and proposed making them configurable via a flag, citing the Jevons paradox and compute innovation history
 * [today](https://github.com/microsoft/TypeScript/issues/63703#issuecomment-5546345126) **RyanCavanaugh** argued that library authors control declaration file behaviors, leading to unpredictable deep instantiation that degrades type-checking performance and harms the developer experience
 * [today](https://github.com/microsoft/TypeScript/issues/63703#issuecomment-5546478556) **RyanCavanaugh** explained that content mappers aim to move complex meta-programming type inference into a static process to generate faster .d.ts files and suggested SQL/GraphQL parser projects investigate this

### [PR microsoft/TypeScript#64061](https://github.com/microsoft/TypeScript/pull/64061) (Closed, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Add pagination of batch requests**

*Implement server-side pagination of batch API responses using maxResponseBytesPerPage to prevent JavaScript string size overflows and simplify encoding.*

 * [4 days ago](https://github.com/microsoft/TypeScript/pull/64061#issuecomment-5489578245) **weswigham** discussed using concat vs push(...) based on element count and asked whether continuation tokens should be scoped per API client
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/64061#issuecomment-5497399283) **andrewbranch** said "It's fine if you want to resolve them as wontfix, I'm just looking for a signal of whether you've evaluated them. There's another one about slice cloning in there."
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/64061#issuecomment-5498052776) **weswigham** synced main and made small edits, then explained the tradeoff between cloning slices and retaining storage for batch memory usage
 * (today) **weswigham** closed the issue

### [Issue microsoft/TypeScript#64098](https://github.com/microsoft/TypeScript/issues/64098) (Open, `Bug`, **RyanCavanaugh**, **Copilot**)

**tsconfig \`include\` silently drops \`Foo\.tsx\` when \`foo\.ts\` exists, on a case\-insensitive filesystem**

*TypeScript’s tsconfig include option silently ignores .tsx files on case-insensitive filesystems when a same-named .ts file exists, preventing diagnostics.*

 * created by **jomonkj**
 * [5 days ago](https://github.com/microsoft/TypeScript/issues/64098#issuecomment-5470908358) **Shivang9983** offered to work on the issue, described root cause and proposed fix, and requested assignment
 * [today](https://github.com/microsoft/TypeScript/issues/64098#issuecomment-5547774548) **RyanCavanaugh** explained that file selection should ignore outputs and prefer inputs by separating files into input and output buckets and mentioned ensuring mixed ts/js compilations work correctly
 * (today) **RyanCavanaugh** added label `Bug`, set milestone to `Backlog`, and assigned to **Copilot**, **RyanCavanaugh**

### [PR microsoft/TypeScript#64115](https://github.com/microsoft/TypeScript/pull/64115) (Open, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Add optional VFS parameters to updateSnapshot**

*Add optional VFS parameters to updateSnapshot with helpers for in-memory or layered file systems supporting fallback, symlinks, and removed paths.*

 * [3 days ago](https://github.com/microsoft/TypeScript/pull/64115#issuecomment-5498184533) **weswigham** explained that file system layering can be implemented via callbacks and host fallback, recommending mounting `/project/node_modules` as a host mount into the in-memory VFS
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64115#issuecomment-5530854700) **andrewbranch** asked about renaming createCacheFileSystem to createOverlayFileSystem or createOverlays and mentioned planning other snapshot/state model changes
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64115#issuecomment-5532864937) **weswigham** suggested renaming functions to use "Layer" instead of "overlay" to avoid confusion with overlayFS on the backend
 * [today](https://github.com/microsoft/TypeScript/pull/64115#issuecomment-5545907874) **andrewbranch** argued that lazy compaction complexity outweighed its benefits, proposed and prototyped an eager clone-on-construction design that removed synchronization code, presented benchmarks showing faster reads/releases but slower snapshot creation, and concluded that eager compaction simplifies code with similar overall performance

### [Issue microsoft/TypeScript#64132](https://github.com/microsoft/TypeScript/issues/64132) (Closed)

**getCompletionsAtPosition in API throws "completion list needs auto imports"**

*Using getCompletionsAtPosition in TypeScript 7.0.2’s unstable sync API throws a “completion list needs auto imports” error.*

 * created by **auvred**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#64133](https://github.com/microsoft/TypeScript/pull/64133) (Closed, `For Uncommitted Bug`)

**Add auto\-import retry to getCompletionsAtPosition in API**

*Implement a GetSnapshotWithAutoImports retry in getCompletionsAtPosition to improve auto-import completions*

 * created by **auvred**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64133#issuecomment-5543452376) **auvred** said "The #64166 diff is rather large, so it's probably better to review it separately"
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript#64135](https://github.com/microsoft/TypeScript/issues/64135) (Closed, **jakebailey**, **Copilot**)

**unstable/ast: scanJsDocToken infinite\-loops when a scan range ends on a trailing '\-' \(fix from \#63581 not carried into the AST scanner\)**

*scanJsDocToken in unstable/ast infinite-loops on trailing hyphens due to missing parentheses in its loop condition*

 * created by **nightcabin1**
 * (2 days ago) **jakebailey** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#64136](https://github.com/microsoft/TypeScript/issues/64136) (Closed, `Not a Defect`)

**Regression to \#35004**

*Assertion functions fail with wildcard destructuring imports after upgrading to TypeScript 7, triggering TS2775 errors.*

 * [2 days ago](https://github.com/microsoft/TypeScript/issues/64136#issuecomment-5512454226) **MartinJohns** said "Your issue is the deconstruction, not the wildcard import."
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/64136#issuecomment-5512758602) **valler** thanked maintainers and asked if TS2775 was expected and whether to close or rename the issue
 * [yesterday](https://github.com/microsoft/TypeScript/issues/64136#issuecomment-5525601715) **jcalz** explained that assertion functions require explicit type annotations and that destructuring assignment cannot support them, and suggested framing a feature request as 'allow destructuring assignment of assertion functions'
 * **RyanCavanaugh** added label `Not a Defect`
 * [today](https://github.com/microsoft/TypeScript/issues/64136#issuecomment-5543397736) **RyanCavanaugh** provided a minimal reproduction and stated that the error TS2775 is expected and not a bug or regression

### [PR microsoft/TypeScript#64141](https://github.com/microsoft/TypeScript/pull/64141) (Closed, `For Uncommitted Bug`, **jakebailey**, **Copilot**)

**Prevent infinite loop in unstable AST JSDoc scanner**

*Guard identifier parts and hyphens with range checks in the unstable AST JSDoc scanner to avoid infinite loops.*

 * (2 days ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64142](https://github.com/microsoft/TypeScript/pull/64142) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Avoid async IPC panic on peer close**

*Fixes a race condition that causes an asynchronous IPC panic when the peer connection closes*

 * (2 days ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/64142#issuecomment-5543506959) **jakebailey** said "Funny how clicking review twice gets "no problems" then "two problems""
 * (today) **jakebailey** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/64142#issuecomment-5549851826) **fdtwd8vv45-sketch** instructed Copilot to apply suggested changes from the linked review thread exactly without additional modifications

### [Issue microsoft/TypeScript#64143](https://github.com/microsoft/TypeScript/issues/64143) (Closed, `Bug`, **gabritto**)

**readonly is accepted in ambient module import attributes types**

*Ambient module import attributes types in TypeScript incorrectly allow the readonly modifier, leading to ambiguous module matching and merging.*

 * created by **camc314**
 * (today) **RyanCavanaugh** added label `Bug`, set milestones to `Dormant`, `TypeScript 7.1.0 Beta`, removed from milestone `Dormant`, and assigned to **gabritto**

### [Issue microsoft/TypeScript#64144](https://github.com/microsoft/TypeScript/issues/64144) (Open, `Suggestion`)

**Auto\-delete closing tag when opening tag becomes self\-closed**

*Automatically remove the redundant closing tag when converting an opening tag into a self-closing tag.*

 * (yesterday) **aeschli** assigned to **dbaeumer**, and unassigned **aeschli**
 * **dbaeumer** unassigned **dbaeumer**
 * [today](https://github.com/microsoft/TypeScript/issues/64144#issuecomment-5545585516) **RyanCavanaugh** mentioned that it was surprising and unclear what would happen to `foo` if the tag opener was made self-closing when the tag is empty
 * **RyanCavanaugh** added label `Suggestion`
 * [today](https://github.com/microsoft/TypeScript/issues/64144#issuecomment-5546682496) **monolithed** described the behavior as expected and convenient, noting that IntelliJ IDEA has supported it for years

### [PR microsoft/TypeScript#64162](https://github.com/microsoft/TypeScript/pull/64162) (Open, `For Uncommitted Bug`, **DanielRosenwasser**, **Copilot**)

**Reject exports from global augmentations**

*Prevent export statements from exporting variables declared inside declare global augmentation blocks.*

 * (yesterday) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64162#issuecomment-5548173828) **DanielRosenwasser** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/64162#issuecomment-5548174552) **typescript-automation[bot]** reported build status updates for various test commands with links to job results
 * [today](https://github.com/microsoft/TypeScript/pull/64162#issuecomment-5548332461) **typescript-automation[bot]** reported user test results that compared main and pull request and highlighted infrastructure failures and new TS2661 errors
 * [today](https://github.com/microsoft/TypeScript/pull/64162#issuecomment-5548340379) **typescript-automation[bot]** provided the requested performance run results
 * [today](https://github.com/microsoft/TypeScript/pull/64162#issuecomment-5548406429) **typescript-automation[bot]** informed that the DT tests results were ready and unchanged
 * [today](https://github.com/microsoft/TypeScript/pull/64162#issuecomment-5548522765) **typescript-automation[bot]** reported that running tsc on the top 400 repos comparing main and the PR merge showed everything looked good
 * [today](https://github.com/microsoft/TypeScript/pull/64162#issuecomment-5548559252) **jakebailey** said "DT is not yet working, I suspect this will break a lot there"

### [PR microsoft/TypeScript#64163](https://github.com/microsoft/TypeScript/pull/64163) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**Decouple snapshot ownership from project\.Session so api\.Session only uses one in LSP mode**

*Extract snapshot cloning and caching into a new host to decouple api.Session from project.Session in LSP mode.*

 * (yesterday) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript/pull/64163#issuecomment-5543567204) **andrewbranch** clarified that this fix addressed in-flight handlers during API session closure to prevent panics when forking disposed snapshots and noted it differs from issue #64142
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#64164](https://github.com/microsoft/TypeScript/pull/64164) (Closed, `For Uncommitted Bug`)

**Handle tuple rest parameters in legacy decorator arity checks**

*Modify legacy decorator arity checks to correctly handle tuple rest parameters and eliminate spurious TS1241 errors.*

 * created by **Andarist**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64164#issuecomment-5536950309) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64165](https://github.com/microsoft/TypeScript/pull/64165) (Closed, `For Backlog Bug`)

**Fix crash on private constructors in intersection base types**

*Fix compiler crash triggered by private constructors in intersection base types*

 * created by **Andarist**
 * (today) **typescript-automation[bot]** added labels `For Backlog Bug`, `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64165#issuecomment-5544865175) **jakebailey** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/64165#issuecomment-5544866217) **typescript-automation[bot]** posted automated build status updates for CI jobs test top400, user test this, run dt, and perf test this faster
 * [today](https://github.com/microsoft/TypeScript/pull/64165#issuecomment-5545117001) **typescript-automation[bot]** reported that the tsc user tests passed except for two package install failures and one git clone failure potentially unrelated to the change
 * [today](https://github.com/microsoft/TypeScript/pull/64165#issuecomment-5545171883) **typescript-automation[bot]** provided the requested performance run results including a comparison report and metrics
 * [today](https://github.com/microsoft/TypeScript/pull/64165#issuecomment-5545524380) **typescript-automation[bot]** reported that tsc comparison results for the top 400 repos looked good
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#64166](https://github.com/microsoft/TypeScript/issues/64166) (Open, `Bug`, **andrewbranch**)

**\`getCompletionsAtPosition\` in API deadlocks when used with \`includeSymbol: true\`**

*getCompletionsAtPosition deadlocks when includeSymbol:true is set due to reuse of the persistent TypeScript checker*

 * created by **auvred**
 * (today) **RyanCavanaugh** added label `Bug`, set milestone to `TypeScript 7.1.0 Beta`, and assigned to **andrewbranch**

### [Issue microsoft/TypeScript#64167](https://github.com/microsoft/TypeScript/issues/64167) (Closed, `Question`)

**LSP completion echoes the unresolved identifier currently being typed as a Text item**

*TypeScript's LSP server returns unresolved Text completions identical to the typed identifier, creating useless no-op suggestion entries.*

 * created by **kuator**
 * [today](https://github.com/microsoft/TypeScript/issues/64167#issuecomment-5543692838) **RyanCavanaugh** explained that the behavior was intentional in positions introducing new identifiers to support users with 'complete on space'.
 * **RyanCavanaugh** added label `Question`
 * [today](https://github.com/microsoft/TypeScript/issues/64167#issuecomment-5548058704) **DanielRosenwasser** clarified that sortText: 18 corresponded to SortTextJavascriptIdentifiers, demonstrated its effect in a ts-checked JavaScript file, and noted the downside of immediate identifier suggestions
 * [today](https://github.com/microsoft/TypeScript/issues/64167#issuecomment-5548132079) **DanielRosenwasser** suggested that the editor could filter out LSP Text completions and provided a VS Code setting snippet

### [Issue microsoft/TypeScript#64168](https://github.com/microsoft/TypeScript/issues/64168) (Open, `Bug`)

**\`getChildren\(\)\` drops the \`\<\` token of a type argument list when immediately followed by another \`\<\`**

*getChildren() removes the first '<' in a '<<' type argument list, causing a gap in AST children*

 * created by **overlookmotel**
 * [today](https://github.com/microsoft/TypeScript/issues/64168#issuecomment-5543643908) **RyanCavanaugh** said "We're not making fixes to the TS6 API, but based on the linked PR it looks like there's a TS7 equivalent problem"
 * (today) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`

### [PR microsoft/TypeScript#64169](https://github.com/microsoft/TypeScript/pull/64169) (Open, `For Backlog Bug`)

**Preserve \`\<\` in \`getChildren\(\)\` when type arguments begin with \`\<\`**

*Update getChildren() to preserve the leading “<” token when type arguments begin with “<”*

 * created by **Andarist**
 * (today) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * (today) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`

### [PR microsoft/TypeScript#64170](https://github.com/microsoft/TypeScript/pull/64170) (Closed, `For Backlog Bug`)

**fix\(checker\): don't emit typeof for private\-named static methods**

*Declaration emitter avoids generating typeof references for private-named static methods, preventing invalid declaration syntax by using structural type fallbacks.*

 * (today) **typescript-automation[bot]** added labels `For Backlog Bug`, `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64170#issuecomment-5542763837) **ekalinin** requested that the contributor agree to the Contributor License Agreement by replying with the appropriate bot command
 * [today](https://github.com/microsoft/TypeScript/pull/64170#issuecomment-5544766662) **ekalinin** described additional breaking examples, applied the IsIdentifierText fix, and renamed and relocated the test to declarationEmitStaticMethodNonIdentifierNames to cover private, quoted, computed, numeric, and identifier-named statics
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#64171](https://github.com/microsoft/TypeScript/issues/64171) (Open, `Bug`)

**\[Auto\-import\] Quick Fix suggests invalid module specifiers that fail to resolve at runtime**

*Quick Fix auto-import suggests module specifiers that don't resolve at runtime under nodenext import conditions.*

 * created by **alexicum**
 * (today) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`

### [PR microsoft/TypeScript#64172](https://github.com/microsoft/TypeScript/pull/64172) (Open, `For Backlog Bug`)

**Infer recursive types through object literal getters**

*Fix recursive type inference in object getters by adding a recursion-depth sentinel to avoid circular resolution errors*

 * created by **colinhacks**
 * (today) **typescript-automation[bot]** added labels `For Backlog Bug`, `For Backlog Bug`

### [PR microsoft/TypeScript#64173](https://github.com/microsoft/TypeScript/pull/64173) (Open, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**Port content mapper inspector extension into bundled extension**

*Port the content mapper inspector extension into the main bundled extension for streamlined integration.*

 * created by **andrewbranch**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **andrewbranch**

### [PR microsoft/TypeScript#64174](https://github.com/microsoft/TypeScript/pull/64174) (Open, `Author: Team`, `For Milestone Bug`, **jakebailey**)

**Add wasip1 support, enabling CLI, API, browser, sync/async**

*Add experimental WASI Preview1 support in tsc.wasm, providing CLI, LSP server, and sync/async API access in Node.js and browsers.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Milestone Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#64175](https://github.com/microsoft/TypeScript/pull/64175) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Enable synchronous API connections to existing servers**

*Implement a synchronous API for connecting to existing server processes using Go-managed named pipes.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#64176](https://github.com/microsoft/TypeScript/pull/64176) (Open, `For Uncommitted Bug`, **RyanCavanaugh**, **Copilot**)

**Fix tsconfig \`include\` silently dropping files that differ only by base\-name case**

*tsconfig include patterns on case-insensitive file systems were silently excluding files with names differing only by case*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * (today) **typescript-automation[bot]** added labels `For Milestone Bug`, `For Milestone Bug`, `For Uncommitted Bug`, and removed label `For Milestone Bug`

### [PR microsoft/TypeScript#64177](https://github.com/microsoft/TypeScript/pull/64177) (Open, `For Backlog Bug`)

**fix\(auto\-import\): don't suggest \# imports that only resolve via condition fallback**

*Update auto-import to no longer suggest imports that resolve only through conditional fallbacks, matching Node’s first-match resolution.*

 * created by **marwan562**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64177#issuecomment-5549432171) **marwan562** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript/pull/64177#issuecomment-5549470668) **marwan562** addressed Copilot comments, updated array and nested conditional handling, added deeper-nesting tests, and confirmed all module specifiers tests passed

### [PR microsoft/TypeScript#64178](https://github.com/microsoft/TypeScript/pull/64178) (Open, `For Milestone Bug`, **andrewbranch**)

**Prevent deadlock in \`getCompletionsAtPosition\(\.\.\., { includeSymbol: true }\)\` API**

*Remove the program.GetTypeChecker call from getExistingImports and explicitly pass the checker to avoid deadlock in getCompletionsAtPosition with includeSymbol enabled.*

 * created by **auvred**
 * (today) **typescript-automation[bot]** added label `For Milestone Bug`, and assigned to **andrewbranch**

### [PR microsoft/TypeScript#64179](https://github.com/microsoft/TypeScript/pull/64179) (Open, `For Uncommitted Bug`, **RyanCavanaugh**, **Copilot**)

**Type HTMLImageElement\.crossOrigin as a literal union of known CORS values**

*Narrow HTMLImageElement.crossOrigin in lib.dom.d.ts from string|null to the literal union "anonymous"|"use-credentials"|""|null with new compiler tests and regeneration caveats.*

 * created by **Copilot**
 * (later) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * (later) **typescript-automation[bot]** added labels `For Milestone Bug`, `For Milestone Bug`, `For Uncommitted Bug`, and removed label `For Milestone Bug`

### [PR microsoft/TypeScript#64180](https://github.com/microsoft/TypeScript/pull/64180) (Open, `For Backlog Bug`)

**fix\(declarations\): keep JSDoc @typedef/@callback comments with their type**

*Keep JSDoc @typedef/@callback comments associated with their type declarations even when preceded by other top-level declarations.*

 * created by **ekalinin**
 * **typescript-automation[bot]** added label `For Backlog Bug`

