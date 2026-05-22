# Report for 2026-05-20 (Wednesday, May 20th, 2026)

10 different users commented on 8 different issues.

## Recommended Actions

 * Response Recommended
    * @rickvian asked why VSCode does not support cmd+click on relative referenced files and what the blocker is in [microsoft/TypeScript#47718](https://github.com/microsoft/TypeScript/issues/47718#issuecomment-4505624938)
    * @limwa provided a reduced repro example in [microsoft/TypeScript#62798](https://github.com/microsoft/TypeScript/issues/62798#issuecomment-4503422905)
    * @angrybacon asked whether emitting residual type-only imports was an intended TypeScript feature or a limitation in [microsoft/TypeScript#63493](https://github.com/microsoft/TypeScript/issues/63493#issuecomment-4503007324)
    * @angrybacon asked whether a verbatim option could be provided to drop type-only imports at runtime in [microsoft/TypeScript#63493](https://github.com/microsoft/TypeScript/issues/63493#issuecomment-4503497934)
    * @Derugon provided additional repro steps and clarification in [microsoft/TypeScript#63497](https://github.com/microsoft/TypeScript/issues/63497#issuecomment-4505501992)
    * @Derugon proposed a fix and provided test cases in [microsoft/TypeScript#63497](https://github.com/microsoft/TypeScript/issues/63497#issuecomment-4505625574)

## Activity Summary

### [Issue microsoft/TypeScript#47718](https://github.com/microsoft/TypeScript/issues/47718) (Open, `Suggestion`, `In Discussion`)

**Provide way to link to other files from JSDoc comments **

*Include the source file path in quickInfo documentation responses to enable editors to resolve relative JSDoc file links.*

 * [35 weeks ago](https://github.com/microsoft/TypeScript/issues/47718#issuecomment-3285406966) **tresorama** tried EmilyRosina’s solution but found it only worked within the file defining the JSDocs and not from other files, speculating that the link path is computed from the active file rather than the JSDoc file
 * [23 weeks ago](https://github.com/microsoft/TypeScript/issues/47718#issuecomment-3607486150) **crlmrlck** asked how to link directly to specific symbols using JSDoc @link
 * [11 weeks ago](https://github.com/microsoft/TypeScript/issues/47718#issuecomment-3963918316) **mohammadazeemwani** reported that heading references weren't working and provided a workaround to link directly to the file
 * [later](https://github.com/microsoft/TypeScript/issues/47718#issuecomment-4505624938) **rickvian** asked why VSCode did not support cmd+click on relative referenced files and what the blocker was

### [Issue microsoft/TypeScript#50139](https://github.com/microsoft/TypeScript/issues/50139) (Open, `Bug`, `Help Wanted`, `Domain: check: Control Flow`)

**Discriminated union parameter destructuring doesn't work if the fields have defaults**

*TypeScript loses discriminated union narrowing when destructuring parameters that include default field values*

 * [1.4 years ago](https://github.com/microsoft/TypeScript/issues/50139#issuecomment-2514883467) **jcalz** said "cross-linking https://github.com/microsoft/TypeScript/pull/46266#issuecomment-1462630908"
 * [1.2 years ago](https://github.com/microsoft/TypeScript/issues/50139#issuecomment-2697327640) **gmoniava** said "Ran into this problem too"
 * **RyanCavanaugh** added label `Domain: Control Flow`
 * [today](https://github.com/microsoft/TypeScript/issues/50139#issuecomment-4504919111) **jcalz** offered a workaround using object spread into default values followed by destructuring assignment

### [Issue microsoft/TypeScript#62798](https://github.com/microsoft/TypeScript/issues/62798) (Open, `Bug`, `Help Wanted`, `Domain: check: Variance Relationships`, `Cursed?`)

**Conditional type eagerly calculated to be invariant breaks referential transparency**

*Eager evaluation of conditional type F<T> as invariant breaks referential transparency, making F<{}> extends F<{a:string}> yield false instead of true*

 * [25 weeks ago](https://github.com/microsoft/TypeScript/issues/62798#issuecomment-3574814438) **Andarist** said "I can only confirm that F is measured to be invariant here and that the other example ends up comparing different type aliases so it goes straight~ to the structural comparison."
 * **RyanCavanaugh** added label `Domain: check: Variance Relationships`
 * [11 weeks ago](https://github.com/microsoft/TypeScript/issues/62798#issuecomment-3986082804) **juhort** demonstrated that variance-based checks occurred both ways in the BoxOfIsSupertypeOfString example but only one way in the F<T> example
 * [today](https://github.com/microsoft/TypeScript/issues/62798#issuecomment-4503422905) **limwa** described a type-checker issue where comparing generic instantiations failed but comparing their materialized structural types succeeded, and provided a reduced repro in TypeScript native preview 7.0.0-dev.20260519.1

### [Issue microsoft/TypeScript#63487](https://github.com/microsoft/TypeScript/issues/63487) (Closed, `Duplicate`)

**Type\-narrowing on array elements persists after array mutations**

*TypeScript incorrectly preserves array element type-narrowing after mutative operations like shift, leading to false errors.*

 * created by **raydog**
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63487#issuecomment-4472011859) **MartinJohns** said "This is essentially another duplicate of #9998. And a duplicate of #31334."
 * **RyanCavanaugh** added label `Duplicate`
 * [today](https://github.com/microsoft/TypeScript/issues/63487#issuecomment-4504042530) **typescript-bot** said "This issue has been marked as "Duplicate" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-bot** closed the issue

### [Issue microsoft/TypeScript#63490](https://github.com/microsoft/TypeScript/issues/63490) (Closed, `Duplicate`)

**Improve control\-flow narrowing for Object\.hasOwn\(obj, key\)**

*TypeScript should treat Object.hasOwn(obj, key) as a type guard to narrow key availability for safer property access.*

 * created by **eng-same**
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63490#issuecomment-4480192501) **MartinJohns** said "Duplicate of #44253."
 * **RyanCavanaugh** added label `Duplicate`
 * [today](https://github.com/microsoft/TypeScript/issues/63490#issuecomment-4504042431) **typescript-bot** said "This issue has been marked as "Duplicate" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-bot** closed the issue

### [Issue microsoft/TypeScript#63493](https://github.com/microsoft/TypeScript/issues/63493) (Closed, `Suggestion`, `Awaiting More Feedback`, `Domain: LS: Auto-import`)

**Configuration to auto\-import with inline type specifiers**

*Implement a config option to auto-import types using inline specifiers or top-level import syntax.*

 * [yesterday](https://github.com/microsoft/TypeScript/issues/63493#issuecomment-4489668508) **angrybacon** explained that the lint rule existed to prevent mixed import styles and to group imports consistently to reduce diff noise
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63493#issuecomment-4491115237) **guillaumebrunerie** explained the origin of the rule and referenced another rule forbidding inline type-only imports
 * [today](https://github.com/microsoft/TypeScript/issues/63493#issuecomment-4499494774) **RyanCavanaugh** said "Yeah, no-import-type-side-effects is the rule I'd expect to see. "Consistently" using per-identifier type modifiers hides a material difference in whether a runtime import is desired or not."
 * [today](https://github.com/microsoft/TypeScript/issues/63493#issuecomment-4503007324) **angrybacon** thanked the explanation and asked whether emitting residual type-only imports was an intended TypeScript feature or a limitation
 * [today](https://github.com/microsoft/TypeScript/issues/63493#issuecomment-4503389849) **RyanCavanaugh** explained that using `import { type foo }` instead of `import type { foo }` triggers a runtime import under --verbatimModuleSyntax because that flag preserves the author’s original syntax intent
 * [today](https://github.com/microsoft/TypeScript/issues/63493#issuecomment-4503497934) **angrybacon** asked whether a verbatim option could drop type-only imports at runtime
 * [today](https://github.com/microsoft/TypeScript/issues/63493#issuecomment-4503592174) **RyanCavanaugh** clarified that the request was the opposite of why the flag was created and pointed to previous discussions

### [Issue microsoft/TypeScript#63497](https://github.com/microsoft/TypeScript/issues/63497) (Open, `Help Wanted`, `Domain: lib.d.ts`)

**DOM: \`Element\#matches\(\)\` incorrectly narrows types**

*Using Element.matches with a specific tag name inside a negated condition incorrectly narrows the element's type to never.*

 * created by **Derugon**
 * [today](https://github.com/microsoft/TypeScript/issues/63497#issuecomment-4497649609) **MartinJohns** explained the issue was due to a specific change and suggested a workaround using the string overload
 * [today](https://github.com/microsoft/TypeScript/issues/63497#issuecomment-4499468165) **RyanCavanaugh** provided an automated analysis suggesting similar issues and indicating the behavior might be intended
 * [today](https://github.com/microsoft/TypeScript/issues/63497#issuecomment-4501047251) **nmain** explained that the proposed typeguard signature was incorrect because typeguards are two-sided and HTMLElementTagNameMap members are not structurally distinct subclasses
 * (today) **RyanCavanaugh** added labels `Bug`, `Domain: lib.d.ts`, `Help Wanted`, removed label `Bug`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/63497#issuecomment-4502240964) **RyanCavanaugh** described the provided repro as odd and offered an illustrative code example
 * [today](https://github.com/microsoft/TypeScript/issues/63497#issuecomment-4503524504) **voxpelli** mentioned the issue was due to a specific change, suggested using the string overload workaround, and corrected that the PR first shipped in TS 6.0
 * [today](https://github.com/microsoft/TypeScript/issues/63497#issuecomment-4503605208) **voxpelli** provided TypeScript code suggestion for proper fix using SpecificHTMLElementTagNameMap and SpecificSVGElementTagNameMap, excluding MathML
 * [today](https://github.com/microsoft/TypeScript/issues/63497#issuecomment-4505501992) **Derugon** apologized for simplified snippet and clarified actual use case using conditional matches that triggers the 'never' type error
 * [later](https://github.com/microsoft/TypeScript/issues/63497#issuecomment-4505625574) **Derugon** suggested a proper fix for element.matches narrowing issues and provided test cases with playground links

### [Issue microsoft/TypeScript#63498](https://github.com/microsoft/TypeScript/issues/63498) (Open, `Needs Investigation`)

**\`js/ts\.preferences\.autoImportFileExcludePatterns\` is not reflected promptly in IntelliSense suggestions**

*Changes to js/ts.preferences.autoImportFileExcludePatterns are not promptly reflected in IntelliSense import suggestions*

 * created by **heroboy**

