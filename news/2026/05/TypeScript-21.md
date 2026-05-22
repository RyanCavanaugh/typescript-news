# Report for 2026-05-21 (Thursday, May 21st, 2026)

7 different users commented on 7 different issues.

## Recommended Actions

 * Response Recommended
    * @maxired reported that tsc -b reports errors not shown in VSCode due to project reference redirect behavior in [microsoft/TypeScript#58692](https://github.com/microsoft/TypeScript/issues/58692#issuecomment-4518295031)
    * @voxpelli asked when the issues occur in practice in [microsoft/TypeScript#63497](https://github.com/microsoft/TypeScript/issues/63497#issuecomment-4513118282)

## Activity Summary

### [Issue microsoft/TypeScript#20110](https://github.com/microsoft/TypeScript/issues/20110) (Open, `Suggestion`, `Awaiting More Feedback`)

**Feature request: allow user to merge extended arrays in tsconfig files**

*Add support for merging arrays from extended tsconfig files using a spread-like syntax*

 * [1.6 years ago](https://github.com/microsoft/TypeScript/issues/20110#issuecomment-2345749213) **floratmin** said "Monorepo plus fastify plugins becomes copy + paste hell."
 * [1.1 years ago](https://github.com/microsoft/TypeScript/issues/20110#issuecomment-2722778304) **airtonix** advised to only use typescript.compilerOptions.paths for monorepo package entrypoints and to use relative paths within packages
 * [1.1 years ago](https://github.com/microsoft/TypeScript/issues/20110#issuecomment-2781852893) **top-master** argued that the feature request is optional, criticized Microsoft's handling speed, and urged a fork to rewrite the TypeScript compiler in Rust or C++
 * [today](https://github.com/microsoft/TypeScript/issues/20110#issuecomment-4510604151) **tofrankie** said "👀 Looking forward to the next steps..."

### [Issue microsoft/TypeScript#32392](https://github.com/microsoft/TypeScript/issues/32392) (Open, `Suggestion`, `Awaiting More Feedback`)

**Preserve comments with object destructuring assignment**

*Preserve and display JSDoc comments for properties when using object destructuring assignments in TypeScript*

 * [2.8 years ago](https://github.com/microsoft/TypeScript/issues/32392#issuecomment-1640633376) **yolilufei** said "is there any progress, please?"
 * [1.8 years ago](https://github.com/microsoft/TypeScript/issues/32392#issuecomment-2211007664) **nathanchase** expressed frustration about missing IntelliSense on destructured composable properties
 * [5 weeks ago](https://github.com/microsoft/TypeScript/issues/32392#issuecomment-4263114003) **zoltanium** noted the issue had lingered for seven years, speculated about it gaining traction, and volunteered to investigate specific code segments
 * [today](https://github.com/microsoft/TypeScript/issues/32392#issuecomment-4510709179) **Moto42** described forgetting that the feature doesn't work and added using Promise.all for grouping DB operations to the use-case list

### [Issue microsoft/TypeScript#51011](https://github.com/microsoft/TypeScript/issues/51011) (Open, `Suggestion`, `Awaiting More Feedback`)

**Allow circular constraints**

*Allow immediate circular generic constraints in TypeScript so types can extend themselves without errors.*

 * [3.6 years ago](https://github.com/microsoft/TypeScript/issues/51011#issuecomment-1264464482) **devanshj** explained that the workaround isn't simple, proposed embracing circular constraints, and provided TypeScript code to prove the claim
 * [2.6 years ago](https://github.com/microsoft/TypeScript/issues/51011#issuecomment-1754634794) **brad-jones** explained difficulty with TypeScript type algebra while designing a type-safe DSL for DAGs and showed several code attempts
 * [2.5 years ago](https://github.com/microsoft/TypeScript/issues/51011#issuecomment-1788481941) **devanshj** provided a TypeScript code example implementing Dagfile and DagDSL
 * [today](https://github.com/microsoft/TypeScript/issues/51011#issuecomment-4513832492) **jcalz** asked why F-bounded generic circularity is problematic and what scenarios cause real issues

### [Issue microsoft/TypeScript#58692](https://github.com/microsoft/TypeScript/issues/58692) (Open, `Suggestion`, `Awaiting More Feedback`)

**\[isolatedDeclarations\] An option like disableSourceOfProjectReferenceRedirect, but configurable on the referenced project's end**

*Add a per-project compiler option to disable source-based project reference redirects for isolatedDeclarations-enabled projects to improve responsiveness.*

 * [1.9 years ago](https://github.com/microsoft/TypeScript/issues/58692#issuecomment-2140766833) **MichaelMitchell-at** said "That explanation makes sense, thanks!"
 * (1.9 years ago) **RyanCavanaugh** added labels `Suggestion`, `Awaiting More Feedback`
 * [later](https://github.com/microsoft/TypeScript/issues/58692#issuecomment-4518295031) **maxired** reported that tsc -b reported errors not shown in VSCode due to project reference redirect behavior in a TypeScript monorepo

### [Issue microsoft/TypeScript#63493](https://github.com/microsoft/TypeScript/issues/63493) (Closed, `Suggestion`, `Awaiting More Feedback`, `Domain: LS: Auto-import`)

**Configuration to auto\-import with inline type specifiers**

*Implement a config option to auto-import types using inline specifiers or top-level import syntax.*

 * [yesterday](https://github.com/microsoft/TypeScript/issues/63493#issuecomment-4503389849) **RyanCavanaugh** explained that using `import { type foo }` instead of `import type { foo }` triggers a runtime import under --verbatimModuleSyntax because that flag preserves the author’s original syntax intent
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63493#issuecomment-4503497934) **angrybacon** asked whether a verbatim option could drop type-only imports at runtime
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63493#issuecomment-4503592174) **RyanCavanaugh** clarified that the request was the opposite of why the flag was created and pointed to previous discussions
 * [today](https://github.com/microsoft/TypeScript/issues/63493#issuecomment-4513567217) **angrybacon** said "Thank you for the extra context, I believe this can be closed"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63497](https://github.com/microsoft/TypeScript/issues/63497) (Open, `Help Wanted`, `Domain: lib.d.ts`)

**DOM: \`Element\#matches\(\)\` incorrectly narrows types**

*Using Element.matches with a specific tag name inside a negated condition incorrectly narrows the element's type to never.*

 * [yesterday](https://github.com/microsoft/TypeScript/issues/63497#issuecomment-4503605208) **voxpelli** provided TypeScript code suggestion for proper fix using SpecificHTMLElementTagNameMap and SpecificSVGElementTagNameMap, excluding MathML
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63497#issuecomment-4505501992) **Derugon** apologized for simplified snippet and clarified actual use case using conditional matches that triggers the 'never' type error
 * [today](https://github.com/microsoft/TypeScript/issues/63497#issuecomment-4505625574) **Derugon** suggested a proper fix for element.matches narrowing issues and provided test cases with playground links
 * [today](https://github.com/microsoft/TypeScript/issues/63497#issuecomment-4513118282) **voxpelli** asked when the issues were encountered in practice and provided a working example link
 * [today](https://github.com/microsoft/TypeScript/issues/63497#issuecomment-4514725394) **MartinJohns** noted that the example worked only because of the null-conditional operator and would fail if the value were non-null or explicitly checked for null

### [Issue microsoft/TypeScript#63498](https://github.com/microsoft/TypeScript/issues/63498) (Open, `Needs Investigation`)

**\`js/ts\.preferences\.autoImportFileExcludePatterns\` is not reflected promptly in IntelliSense suggestions**

*Changes to js/ts.preferences.autoImportFileExcludePatterns are not promptly reflected in IntelliSense import suggestions*

 * created by **heroboy**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and set milestone to `Backlog`

