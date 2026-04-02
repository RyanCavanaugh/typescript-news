# Report for 2026-03-27 (Friday, March 27th, 2026)

11 different users commented on 12 different issues.

## Recommended Actions

 * Response Recommended
    * @5cover proposed using a const modifier for stricter read-only qualification in [microsoft/TypeScript#13347](https://github.com/microsoft/TypeScript/issues/13347#issuecomment-4147868651)
    * @5cover asked whether the operator-based type annotation would include excess property checks and suggested syntax options in [microsoft/TypeScript#56235](https://github.com/microsoft/TypeScript/issues/56235#issuecomment-4145657649)
    * @denis-sokolov asked whether there’s a way to get the module name from ResolvedModuleWithFailedLookupLocations in [microsoft/TypeScript#63307](https://github.com/microsoft/TypeScript/issues/63307#issuecomment-4144403493)
    * @5cover asked where the widening heuristic should draw the line and whether it should avoid implicitly widening across typeof categories for {} literals in [microsoft/TypeScript#63308](https://github.com/microsoft/TypeScript/issues/63308#issuecomment-4144510902)

## Activity Summary

### [Issue microsoft/TypeScript#13347](https://github.com/microsoft/TypeScript/issues/13347) (Open, `Suggestion`, `Awaiting More Feedback`)

**Interface with readonly property is assignable to interface with mutable property**

*Feature request to make TypeScript treat interfaces with readonly properties as incompatible with mutable interfaces to prevent unintended property modifications.*

 * [28 weeks ago](https://github.com/microsoft/TypeScript/issues/13347#issuecomment-3264627576) **denis-migdal** said "I was thinking, this would also enable to specify different types for getter/setter in interfaces."
 * [28 weeks ago](https://github.com/microsoft/TypeScript/issues/13347#issuecomment-3265124405) **phaux** suggested applying in/out variance annotations to properties
 * [25 weeks ago](https://github.com/microsoft/TypeScript/issues/13347#issuecomment-3355166967) **denis-migdal** noted that this would also allow making an attribute non-modifiable in the public interface and modifiable in the protected/private interface, and illustrated it with code examples
 * [later](https://github.com/microsoft/TypeScript/issues/13347#issuecomment-4147868651) **5cover** proposed using a const type modifier as a stronger read-only qualifier and provided examples illustrating its behavior

### [Issue microsoft/TypeScript#38520](https://github.com/microsoft/TypeScript/issues/38520) (Open, `Suggestion`, `Awaiting More Feedback`)

**Object\.values and Object\.entries are unsound and inconsistent with Object\.keys\.**

*Update Object.values and Object.entries to use sound generic types consistent with Object.keys and eliminate current unsound behavior.*

 * [2.8 years ago](https://github.com/microsoft/TypeScript/issues/38520#issuecomment-1582493088) **devinrhode2** suggested ts-extras and Froebel as alternative libraries with typed utilities
 * [2.6 years ago](https://github.com/microsoft/TypeScript/issues/38520#issuecomment-1646797657) **craigphicks** argued that property keys and values have different needs and consistency isn't necessary because keys have limited type range and values require explicit typing
 * [16 weeks ago](https://github.com/microsoft/TypeScript/issues/38520#issuecomment-3599885901) **jedwards1211** suggested adding a compiler option to choose whether Object.keys() returned (keyof T)[] or string[] due to unsound Record<string, T> typing
 * [today](https://github.com/microsoft/TypeScript/issues/38520#issuecomment-4145010456) **billy-the-ape** suggested adding global TypeScript declarations for ObjectConstructor methods to avoid edge-case casting and new packages

### [Issue microsoft/TypeScript#56235](https://github.com/microsoft/TypeScript/issues/56235) (Open, `Suggestion`, `Awaiting More Feedback`)

**Safe type assertion \(upcast / widening\) operator**

*Introduce a safe `as!` type assertion operator that only permits casting to a wider type without altering runtime behavior.*

 * [2.2 years ago](https://github.com/microsoft/TypeScript/issues/56235#issuecomment-1877407785) **raythurnvoid** explained that they had to use `as` with `satisfies` for better IntelliSense, causing redundant `satisfies T as T` with long gRPC-generated types
 * [2 years ago](https://github.com/microsoft/TypeScript/issues/56235#issuecomment-2025651824) **saltman424** requested syntactic sugar for 'satisfies' expressions to avoid duplicating type parameters and linked the related issue
 * [34 weeks ago](https://github.com/microsoft/TypeScript/issues/56235#issuecomment-3141256372) **jcalz** cross-linked `satisfiesas`, `satisfias`, and `sassafras` with two issue comments
 * [today](https://github.com/microsoft/TypeScript/issues/56235#issuecomment-4145657649) **5cover** asked whether the operator model type annotation would mirror standard type annotation semantics including assignability and excess property checks, and suggested syntax variants like 'ascribe', 'be', and 'to'.

### [Issue microsoft/TypeScript#63293](https://github.com/microsoft/TypeScript/issues/63293) (Closed, `Suggestion`, `Declined`)

**Enable all strictness options by default in TypeScript 7\.0**

*Enable all strictness-related compiler options by default in TypeScript 7.0, requiring explicit disabling of unwanted checks.*

 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63293#issuecomment-4122124869) **sakgoyal** disagreed with the complaint and argued that automatic errors improve the ecosystem
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63293#issuecomment-4122161686) **RyanCavanaugh** argued that the proposed flags are stylistic and don't improve correctness and thus aren't automatically beneficial
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63293#issuecomment-4122237645) **sakgoyal** said "Yea I suppose you're right"
 * [today](https://github.com/microsoft/TypeScript/issues/63293#issuecomment-4146323805) **typescript-bot** said "This issue has been marked as "Declined" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-bot** closed the issue

### [Issue microsoft/TypeScript#63307](https://github.com/microsoft/TypeScript/issues/63307) (Closed, `Won't Fix`)

**packageId is not generated when name or version fields are missing**

*TypeScript’s moduleNameResolver should generate packageId for packages missing name or version fields instead of returning undefined.*

 * created by **denis-sokolov**
 * [today](https://github.com/microsoft/TypeScript/issues/63307#issuecomment-4143565509) **RyanCavanaugh** said "Who's doing this and why? What's the observable problem?"
 * **RyanCavanaugh** added label `Needs More Info`
 * [today](https://github.com/microsoft/TypeScript/issues/63307#issuecomment-4144020469) **denis-sokolov** linked the related rushstack issue and mentioned that their broader argument concerned the semantics of the field as part of the public compiler API
 * [today](https://github.com/microsoft/TypeScript/issues/63307#issuecomment-4144156122) **RyanCavanaugh** said "I'm still interested in who's doing this (making package.jsons without these fields) and why"
 * [today](https://github.com/microsoft/TypeScript/issues/63307#issuecomment-4144306717) **denis-sokolov** noted that the version field is optional for private packages and that they had no incentive to include it besides recent TypeScript/api-extractor breakage
 * [today](https://github.com/microsoft/TypeScript/issues/63307#issuecomment-4144363178) **RyanCavanaugh** questioned the supposed defect in TypeScript and attributed the missing packageId issue to API Extractor
 * [today](https://github.com/microsoft/TypeScript/issues/63307#issuecomment-4144403493) **denis-sokolov** challenged the assertion that name plus empty version is meaningless, noted that packageId is still returned with an empty version and that there’s no apparent way to retrieve the module name from ResolvedModuleWithFailedLookupLocations, and argued that name plus empty version uniquely identifies npm packages
 * [today](https://github.com/microsoft/TypeScript/issues/63307#issuecomment-4144421271) **denis-sokolov** added that TypeScript knew the package id when resolving a module
 * [today](https://github.com/microsoft/TypeScript/issues/63307#issuecomment-4144480254) **denis-sokolov** reframed the semantic argument by stating that the version field is meaningless for unpublished packages and that packageId behavior is under-defined for them
 * (today) **RyanCavanaugh** added label `Won't Fix`, and removed label `Needs More Info`
 * [today](https://github.com/microsoft/TypeScript/issues/63307#issuecomment-4144496145) **RyanCavanaugh** noted that changing this wouldn't qualify for a 6.0 patch and that the TS7+ API would likely change making the issue moot

### [Issue microsoft/TypeScript#63308](https://github.com/microsoft/TypeScript/issues/63308) (Closed, `Not a Defect`)

**\`let a = {}\` infers \`{}\` instead of \`object\`, which seems too wide for the initializer**

*Inferring an empty object literal as {} allows primitive assignments instead of preserving its object type*

 * created by **5cover**
 * [today](https://github.com/microsoft/TypeScript/issues/63308#issuecomment-4144338189) **MartinJohns** identified the issue as a duplicate of #60582 and provided an additional example demonstrating the problem
 * **RyanCavanaugh** added label `Not a Defect`
 * [today](https://github.com/microsoft/TypeScript/issues/63308#issuecomment-4144459355) **RyanCavanaugh** explained that determining the correct amount of type widening for mutable declarations is heuristic, illustrating with examples let a = {} and let a = 10
 * [today](https://github.com/microsoft/TypeScript/issues/63308#issuecomment-4144510902) **5cover** asked why {} literals are widened to {} instead of object and whether the widening heuristic should avoid crossing typeof categories
 * [today](https://github.com/microsoft/TypeScript/issues/63308#issuecomment-4144527119) **RyanCavanaugh** argued that the previous inference was begging the question and would introduce a variance discontinuity

### [Issue microsoft/TypeScript#63309](https://github.com/microsoft/TypeScript/issues/63309) (Closed, `Bug`, **RyanCavanaugh**, **Copilot**)

**Regression in 6\.0: type inferred from const with broader type is too narrow**

*TypeScript 6.0 mistakenly narrows a class property initialized from a union-typed constant to a single literal value.*

 * created by **trevorade**
 * [today](https://github.com/microsoft/TypeScript/issues/63309#issuecomment-4145893834) **RyanCavanaugh** said "Bisects to #62243, which is pretty surprising?"
 * (today) **RyanCavanaugh** assigned to **Copilot**, **RyanCavanaugh**

### [PR microsoft/TypeScript#63310](https://github.com/microsoft/TypeScript/pull/63310) (Closed, **RyanCavanaugh**, **Copilot**)

**Mark class property initializers as outside of CFA containers**

*Restore PropertyDeclaration as a control flow container to isolate class property initializer type inference and prevent module-level narrowing leaks*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**

### [Issue microsoft/TypeScript#63311](https://github.com/microsoft/TypeScript/issues/63311) (Closed, `Not a Defect`)

**\`typescript\.d\.ts\` uses ES2015\+ globals \(\`Map\`, \`ReadonlyMap\`\) without \`/// \<reference lib\>\` directive**

*typescript.d.ts uses ES2015 Map and ReadonlyMap without a /// <reference lib='es2015' /> directive, causing type errors outside ES2015 contexts.*

 * created by **baraknaveh**

### [Issue microsoft/TypeScript#63312](https://github.com/microsoft/TypeScript/issues/63312) (Closed)

**Code Review Submission \- Comprehensive Analysis**

*An autonomous AI agent named Eve submits a comprehensive freelance code review for the project.*

 * created by **SuperNovaRobot**
 * [today](https://github.com/microsoft/TypeScript/issues/63312#issuecomment-4147206974) **SuperNovaRobot** said "This is not the appropriate channel for this. Deleting."
 * (today) **SuperNovaRobot** closed the issue
 * [later](https://github.com/microsoft/TypeScript/issues/63312#issuecomment-4147937732) **MartinJohns** said "This is not appropriate anywhere on GitHub. Getting so sick of this AI spam everywhere."

### [Issue microsoft/TypeScript#63313](https://github.com/microsoft/TypeScript/issues/63313) (Closed, `Not a Defect`)

**Type of return value of \`yield\` cannot be inferred from explicitly declared \`TNext\`**

*Generator yield return type isn't inferred from the declared TNext, causing 'i' to be any instead of number.*

 * created by **zimtsui**

### [Issue microsoft/TypeScript#63314](https://github.com/microsoft/TypeScript/issues/63314) (Open, `Suggestion`, `Awaiting More Feedback`)

**Allow structural typing of prototypes**

*Add structural prototype typing to TypeScript so that prototype chain properties are recognized in type checking.*

 * created by **5cover**

