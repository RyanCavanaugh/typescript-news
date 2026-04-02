# Report for 2026-03-05 (Thursday, March 5th, 2026)

11 different users commented on 10 different issues.

## Recommended Actions

 * Response Recommended
    * @OldStarchy asked about concerns with implementing transformation of private constructor parameter syntax in [microsoft/TypeScript#36282](https://github.com/microsoft/TypeScript/issues/36282#issuecomment-4008476586)
    * @denis-migdal provided a workaround suggestion in [microsoft/TypeScript#43553](https://github.com/microsoft/TypeScript/issues/43553#issuecomment-4006970891)
    * @caomingpei suggested considering default compiler behavior in ts-go migration due to recursive type expansion in [microsoft/TypeScript#63197](https://github.com/microsoft/TypeScript/issues/63197#issuecomment-4010047218)

## Activity Summary

### [Issue microsoft/TypeScript#28306](https://github.com/microsoft/TypeScript/issues/28306) (Open, `Suggestion`, `In Discussion`)

**Strict type\-checking on a per\-file basis "@ts\-strict"**

*Add support for enabling strict TypeScript checks per file using a @ts-strict directive*

 * [1 year ago](https://github.com/microsoft/TypeScript/issues/28306#issuecomment-2640953344) **ovcharik** introduced the @selectel/ts-check utility to perform strict type checks on changed files in the CI/CD pipeline
 * [15 weeks ago](https://github.com/microsoft/TypeScript/issues/28306#issuecomment-3559047478) **Gibbo3771** reported that the TypeScript strict plugin did not recognise the preprocess comment and enabled strict mode across the entire codebase
 * [today](https://github.com/microsoft/TypeScript/issues/28306#issuecomment-4006012073) **rwalle** noted that with TypeScript 6.0 strict mode will be enabled by default and explained the relevance of strict checking flags for JavaScript and TypeScript projects
 * [today](https://github.com/microsoft/TypeScript/issues/28306#issuecomment-4006311800) **codethief** explained that for existing projects strict mode must be enabled incrementally because enabling it project-wide is daunting

### [Issue microsoft/TypeScript#36282](https://github.com/microsoft/TypeScript/issues/36282) (Open, `Suggestion`, `Awaiting More Feedback`)

**Allow \`\#\`\-private names in parameter property positions**

*Allow using #private names in TypeScript constructor parameters to automatically declare and initialize private class fields.*

 * [5 years ago](https://github.com/microsoft/TypeScript/issues/36282#issuecomment-769794761) **blixt** suggested allowing readonly #field constructor parameters to auto assign private fields to ease refactoring and asked to remove invalid 'private #field' syntax
 * [4.2 years ago](https://github.com/microsoft/TypeScript/issues/36282#issuecomment-986082728) **sdegutis** said "Can I vote for this too?"
 * [4.2 years ago](https://github.com/microsoft/TypeScript/issues/36282#issuecomment-986140895) **sdegutis** questioned whether private fields must be accessed via this in the constructor or if local access can be omitted
 * [today](https://github.com/microsoft/TypeScript/issues/36282#issuecomment-4008476586) **OldStarchy** asked about concerns and naming decisions for implementing a transformation from private constructor parameters to private class fields

### [Issue microsoft/TypeScript#42856](https://github.com/microsoft/TypeScript/issues/42856) (Closed, `Suggestion`, `Out of Scope`)

**Revisit support for \`::\` operator**

*Revisit support for the ES Next :: bind operator in TypeScript now that it has reached stage 1.*

 * [5 years ago](https://github.com/microsoft/TypeScript/issues/42856#issuecomment-781500748) **RyanCavanaugh** reiterated that new runtime-observable syntax isn't added unless it's at Stage 3 and that active proposals are monitored and feedback is provided
 * [5 years ago](https://github.com/microsoft/TypeScript/issues/42856#issuecomment-781564813) **ackvf** said "Alright! Get it. Too bad, I would love to see some syntactic sugar for binding."
 * (5 years ago) **ackvf** closed the issue
 * [today](https://github.com/microsoft/TypeScript/issues/42856#issuecomment-4009939081) **asd585140-glitch** said "حفظ وتطبيق"

### [Issue microsoft/TypeScript#43553](https://github.com/microsoft/TypeScript/issues/43553) (Open, `Suggestion`, `Awaiting More Feedback`)

**Different types based on visibility**

*Enable class properties and getters/setters to have distinct types depending on access visibility levels.*

 * [1.3 years ago](https://github.com/microsoft/TypeScript/issues/43553#issuecomment-2477426114) **Fasteroid** said "Hate to necro this, but I'd really love to see this too.  I'm running into Jet's exact problem with "dumb" getter/setters that shouldn't have to exist.  Any plans for this yet?"
 * [34 weeks ago](https://github.com/microsoft/TypeScript/issues/43553#issuecomment-3042042801) **denis-migdal** said "+1 this would indeed be a quite useful feature."
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/43553#issuecomment-3993282168) **denis-migdal** discussed a similar feature and described two workarounds using identity functions or internal interfaces to handle readonly-to-mutable conversions
 * [today](https://github.com/microsoft/TypeScript/issues/43553#issuecomment-4006970891) **denis-migdal** provided a workaround using an internals property with a code example

### [Issue microsoft/TypeScript#63085](https://github.com/microsoft/TypeScript/issues/63085) (Open, `Planning`)

**TypeScript 6\.0 Iteration Plan**

*The TypeScript 6.0 iteration plan details milestone dates and scheduled compiler additions, language improvements, breaking changes, and deprecations.*

 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-3987821803) **DanielRosenwasser** said "@typescript-bot bump release-6.0"
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-3987822011) **typescript-bot** posted an automated build status update for bump release-6.0
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-3987851804) **typescript-bot** said "Hey, @DanielRosenwasser! I've set the version of release-6.0 to 6.0.1-rc for you."
 * [later](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-4010254515) **HolgerJeromin** suggested mentioning the deprecation of `module=none` in the 6.0-rc1 announcement blog post

### [Issue microsoft/TypeScript#63197](https://github.com/microsoft/TypeScript/issues/63197) (Closed, `Bug`, `Fixed`)

**Fatal OOM crash on recursive template literal type**

*A recursive template literal type definition causes a fatal out-of-memory crash in TypeScript versions 5.9.3 and 6.0.0-beta.*

 * [6 days ago](https://github.com/microsoft/TypeScript/issues/63197#issuecomment-3975868967) **RyanCavanaugh** requested the actual minimal repro for the issue and noted that long compilation time isn't a security issue
 * [6 days ago](https://github.com/microsoft/TypeScript/issues/63197#issuecomment-3975896004) **james-pre** provided environment details, a CI reproduction link, an example type causing the crash, and the tsconfig configuration
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63197#issuecomment-3984559138) **mkantor** provided a minimized reproduction case demonstrating the crash
 * [today](https://github.com/microsoft/TypeScript/issues/63197#issuecomment-4010047218) **caomingpei** described that the issue related to typescript-go#2125 shared a root cause of unbounded recursive type expansion and suggested considering default compiler behavior in a future ts-go migration

### [Issue microsoft/TypeScript#63203](https://github.com/microsoft/TypeScript/issues/63203) (Closed, `Suggestion`, `Awaiting More Feedback`)

**Narrow a ternary expression to unique symbol type**

*Enable TypeScript to infer a unique symbol type from a ternary expression whose runtime result is constant.*

 * [yesterday](https://github.com/microsoft/TypeScript/issues/63203#issuecomment-4001450559) **typescript-bot** said "This issue has been marked as "Working as Intended" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (yesterday) **typescript-bot** closed the issue
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63203#issuecomment-4002497546) **mitar** said "I wrote a comment, but nobody replied. :-("
 * **RyanCavanaugh** removed label `Working as Intended`
 * (today) **RyanCavanaugh** reopened the issue
 * [today](https://github.com/microsoft/TypeScript/issues/63203#issuecomment-4006504011) **RyanCavanaugh** clarified that the bug was allowing Symbol.for to be used as a unique symbol and expressed reluctance to change it
 * [today](https://github.com/microsoft/TypeScript/issues/63203#issuecomment-4006799380) **mitar** argued that Symbol.for with a constant string produces a unique symbol, noted TypeScript's inability to infer identical symbols from multiple potentially nondeterministic calls, and asserted that a single declaration always yields a unique symbol
 * [today](https://github.com/microsoft/TypeScript/issues/63203#issuecomment-4007424683) **snarbles2** clarified that Symbol.for doesn’t create a locally unique symbol because it retrieves symbols from the global registry
 * [today](https://github.com/microsoft/TypeScript/issues/63203#issuecomment-4007746416) **RyanCavanaugh** agreed with snarbles2 and explained that unique symbols guarantee referential uniqueness so two distinct consts cannot be identical
 * (today) **RyanCavanaugh** added labels `Suggestion`, `Awaiting More Feedback`
 * [today](https://github.com/microsoft/TypeScript/issues/63203#issuecomment-4008115160) **mitar** suggested opening another issue for Symbol.for concerns and clarified that symbols from Symbol.for and Symbol() should be unique and type-equal
 * [today](https://github.com/microsoft/TypeScript/issues/63203#issuecomment-4008439421) **RyanCavanaugh** clarified that the Symbol.for return type isn't tied to the string literal and that Symbol.for('none') shouldn't be a unique symbol, noting any defect lies here
 * [today](https://github.com/microsoft/TypeScript/issues/63203#issuecomment-4008486650) **mitar** proposed making symbols work like constant string types in a separate namespace and implementing Symbol.for and Symbol() accordingly to match JavaScript behavior

### [Issue microsoft/TypeScript#63210](https://github.com/microsoft/TypeScript/issues/63210) (Open, `Needs More Info`)

**6\.0\.20260301 Causing general instability and hanging operations**

*Updating to extension version 6.0.20260301 causes indefinite tsconfig initialization, hung TS Server commands, and file renaming failures in VS Code.*

 * created by **netjordanlee**
 * **RyanCavanaugh** added label `Needs More Info`
 * [today](https://github.com/microsoft/TypeScript/issues/63210#issuecomment-4007893981) **RyanCavanaugh** said "We need a way to repro this issue"

### [Issue microsoft/TypeScript#63211](https://github.com/microsoft/TypeScript/issues/63211) (Closed, `Duplicate`)

**switch case does not create separate block scope for let declarations**

*The TypeScript compiler fails to enforce block scoping for let declarations in switch cases, allowing variables to leak across branches.*

 * created by **duanshixuan**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63211#issuecomment-3996505247) **MartinJohns** said "Duplicate of #19503. Used search terms: switch let in:title"
 * **RyanCavanaugh** added label `Duplicate`

### [Issue microsoft/TypeScript#63213](https://github.com/microsoft/TypeScript/issues/63213) (Closed)

**Closed by author**

*The author retracted the issue and closed it because it was opened in error.*

 * created by **ScienceArtist**
 * [later](https://github.com/microsoft/TypeScript/issues/63213#issuecomment-4012562199) **MartinJohns** said "Kids, don't forget to report comments and users like this."

