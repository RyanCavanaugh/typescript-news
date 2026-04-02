# Report for 2026-03-04 (Wednesday, March 4th, 2026)

7 different users commented on 7 different issues.

## Recommended Actions

 * Response Recommended
    * @fudom suggested adding another example in the documentation in [microsoft/TypeScript#27706](https://github.com/microsoft/TypeScript/issues/27706#issuecomment-3999318068)

## Activity Summary

### [Issue microsoft/TypeScript#11498](https://github.com/microsoft/TypeScript/issues/11498) (Open, `Suggestion`, `Needs Proposal`)

**Annotate immediately\-invoked functions for inlining flow control analysis**

*Introduce an immediate annotation on function parameters to enable inlining of their callback bodies for precise flow control analysis*

 * [1.5 years ago](https://github.com/microsoft/TypeScript/issues/11498#issuecomment-2313336649) **nicosampler** provided a workaround using a type assertion and expressed gratitude
 * [1.2 years ago](https://github.com/microsoft/TypeScript/issues/11498#issuecomment-2539461702) **AnthonyLenglet** described stumbling into the issue with the provided dbCall and getActivity code and requested implementation of a fix
 * [1 year ago](https://github.com/microsoft/TypeScript/issues/11498#issuecomment-2636942944) **mfplunet** said "Hi, this massive bikeshedding is good to find a proper solution but I think in the meantime we should fix the incorrect error in cases like #61125."
 * [today](https://github.com/microsoft/TypeScript/issues/11498#issuecomment-3999511189) **rChaoz** provided Kotlin contract examples for type narrowing and lambda invocation with links to documentation

### [Issue microsoft/TypeScript#27706](https://github.com/microsoft/TypeScript/issues/27706) (Open, `Suggestion`, `In Discussion`)

**Type inference/narrowing lost after assignment**

*Type narrowing of an unknown variable to string is lost after reassigning it, reverting back to unknown.*

 * [18 weeks ago](https://github.com/microsoft/TypeScript/issues/27706#issuecomment-3435997923) **denis-migdal** described how TypeScript inferred the type of 'name' differently depending on assignment or operation placement
 * [18 weeks ago](https://github.com/microsoft/TypeScript/issues/27706#issuecomment-3446834159) **sparecycles** said "So a guard clause that narrows a type is "weaker" than a reassignment that narrows the type."
 * [18 weeks ago](https://github.com/microsoft/TypeScript/issues/27706#issuecomment-3448424923) **mkmlab-v2** analyzed a TypeScript type narrowing issue after assignment, explained its cause and current discussion status, and proposed temporary workarounds and documentation updates
 * [today](https://github.com/microsoft/TypeScript/issues/27706#issuecomment-3999318068) **fudom** explained that type-guarded string variables revert to unknown after trimming or lowercasing and suggested adding another example

### [Issue microsoft/TypeScript#28306](https://github.com/microsoft/TypeScript/issues/28306) (Open, `Suggestion`, `In Discussion`)

**Strict type\-checking on a per\-file basis "@ts\-strict"**

*Add support for enabling strict TypeScript checks per file using a @ts-strict directive*

 * [3 years ago](https://github.com/microsoft/TypeScript/issues/28306#issuecomment-1422693903) **kepek** said "👍 "
 * [1 year ago](https://github.com/microsoft/TypeScript/issues/28306#issuecomment-2640953344) **ovcharik** introduced the @selectel/ts-check utility to perform strict type checks on changed files in the CI/CD pipeline
 * [14 weeks ago](https://github.com/microsoft/TypeScript/issues/28306#issuecomment-3559047478) **Gibbo3771** reported that the TypeScript strict plugin did not recognise the preprocess comment and enabled strict mode across the entire codebase
 * [later](https://github.com/microsoft/TypeScript/issues/28306#issuecomment-4006012073) **rwalle** noted that with TypeScript 6.0 strict mode will be enabled by default and explained the relevance of strict checking flags for JavaScript and TypeScript projects

### [Issue microsoft/TypeScript#62134](https://github.com/microsoft/TypeScript/issues/62134) (Open, `Suggestion`, `Awaiting More Feedback`)

**All types of ECMAScript NativeErrors are always subtype reduced between themselves**

*TypeScript’s ES5 typings treat all built-in Error subclasses as structurally identical, preventing correct union and narrowing of native errors.*

 * [31 weeks ago](https://github.com/microsoft/TypeScript/issues/62134#issuecomment-3124580503) **jcalz** suggested using class declarations to improve union reduction behavior, noted that class constructors can be called without new, proposed adding literal name properties in interfaces for nominal typing despite mutability concerns
 * (31 weeks ago) **RyanCavanaugh** added labels `Suggestion`, `Awaiting More Feedback`
 * [later](https://github.com/microsoft/TypeScript/issues/62134#issuecomment-4004203982) **iluha168** explained a TypeScript behavior involving unused out variance generics that prevent reduction when generic types differ, provided playground examples, and cautioned that the approach introduces two new interfaces which may cause collisions and should be made private, recommending using classes instead

### [Issue microsoft/TypeScript#63203](https://github.com/microsoft/TypeScript/issues/63203) (Open, `Suggestion`, `Awaiting More Feedback`)

**Narrow a ternary expression to unique symbol type**

*Enable TypeScript to infer a unique symbol type from a ternary expression whose runtime result is constant.*

 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63203#issuecomment-3986114155) **RyanCavanaugh** explained that unique symbols are supposed to be unique but might not be when using Symbol.for and recommended using a cast
 * **RyanCavanaugh** added label `Working as Intended`
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63203#issuecomment-3986157126) **mitar** stated that exporting two unique symbols with Symbol.for or Symbol() did not produce errors, contradicting the earlier example that errors occur without a ternary expression
 * [today](https://github.com/microsoft/TypeScript/issues/63203#issuecomment-4001450559) **typescript-bot** said "This issue has been marked as "Working as Intended" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/issues/63203#issuecomment-4002497546) **mitar** said "I wrote a comment, but nobody replied. :-("

### [Issue microsoft/TypeScript#63212](https://github.com/microsoft/TypeScript/issues/63212) (Open, `Docs`)

**Add JSX\.ElementChildrenAttribute change to TypeScript 5\.8 release notes**

*Document the breaking change in TS 5.8 requiring explicit JSX.ElementChildrenAttribute for children inference*

 * created by **nmattia**

