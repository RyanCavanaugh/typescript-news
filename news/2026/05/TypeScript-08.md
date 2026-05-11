# Report for 2026-05-08 (Friday, May 8th, 2026)

8 different users commented on 6 different issues.

## Activity Summary

### [Issue microsoft/TypeScript#43368](https://github.com/microsoft/TypeScript/issues/43368) (Open, `Suggestion`, `Awaiting More Feedback`)

**Suggestion: Allow getters to have predicate return types**

*Enable TypeScript class getters to have user-defined type predicate return types for type guards.*

 * [46 weeks ago](https://github.com/microsoft/TypeScript/issues/43368#issuecomment-2993092726) **chespina** expressed frustration with the suggestion to use a method, noted it changed semantics and could introduce breaking changes, mentioned the issue dates back to 2016 and argued that a fundamental language feature is missing and should have higher priority
 * [35 weeks ago](https://github.com/microsoft/TypeScript/issues/43368#issuecomment-3243558010) **qolity** described encountering incorrect type inference with a property-based isRight approach and explaining why the type predicate method, though accurate, is prone to accidental misuse
 * [8 weeks ago](https://github.com/microsoft/TypeScript/issues/43368#issuecomment-4046270378) **alex-at-happening** said "That would be awesome to have it in TS"
 * [today](https://github.com/microsoft/TypeScript/issues/43368#issuecomment-4410653140) **owenoak** said "+1 for this"

### [PR microsoft/TypeScript#61414](https://github.com/microsoft/TypeScript/pull/61414) (Closed, `For Uncommitted Bug`)

**Implement erasable Enum Annotations**

*Implement erasable enum annotations allowing TypeScript to emit valid JavaScript by erasing enum type annotations.*

 * [1.1 years ago](https://github.com/microsoft/TypeScript/pull/61414#issuecomment-2722142531) **typescript-bot** advised to document breaking changes on the wiki and notify DanielRosenwasser and RyanCavanaugh
 * (6 weeks ago) **typescript-bot** closed the issue
 * [6 weeks ago](https://github.com/microsoft/TypeScript/pull/61414#issuecomment-4121453691) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates
 * [later](https://github.com/microsoft/TypeScript/pull/61414#issuecomment-4412252198) **lenovouser** noted that this would be useful now that Node removed the `--experimental-transform-types` flag in v26

### [PR microsoft/TypeScript#63446](https://github.com/microsoft/TypeScript/pull/63446) (Closed, `Author: Team`, `For Uncommitted Bug`, **RyanCavanaugh**)

**Redirect Claude Code to read AGENTS\.md**

*Enable Claude Code to read and process AGENTS.md, which it currently ignores.*

 * (1 week ago) **typescript-bot** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * (1 week ago) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/63446#issuecomment-4411771369) **zanminkian** suggested using the @AGENTS.md snippet as best practice and referenced the documentation link

### [Issue microsoft/TypeScript#63461](https://github.com/microsoft/TypeScript/issues/63461) (Closed, `Design Limitation`)

**\[6\.x\] Getting'unassingable to type' when returning value from method that needs to infer generic from parameters**

*TypeScript 6.x fails to infer the generic type for mapTo, marking the 'label' literal as unassignable.*

 * [today](https://github.com/microsoft/TypeScript/issues/63461#issuecomment-4406385564) **spaceemotion** questioned where to apply NoInfer after noting that return type precedence and assignment to a temporary variable eliminate the error, and checked the tsgo playground where the error appears in output but is not highlighted, wondering if the behavior differs between TS versions
 * [today](https://github.com/microsoft/TypeScript/issues/63461#issuecomment-4406402893) **mkantor** provided a playground link demonstrating where to place the `NoInfer` suggestion so that the return type of `mapTo` becomes `RuntimeList<NoInfer<TTo>>`
 * [today](https://github.com/microsoft/TypeScript/issues/63461#issuecomment-4407822649) **RyanCavanaugh** provided automated analysis on TS 6.0 inference change affecting mapTo and suggested using explicit type arguments or contextual typing to restore inference
 * [today](https://github.com/microsoft/TypeScript/issues/63461#issuecomment-4408374657) **spaceemotion** clarified that TypeScript inferred CastableType instead of Label and explained the compiler's inference behavior
 * [today](https://github.com/microsoft/TypeScript/issues/63461#issuecomment-4408755144) **RyanCavanaugh** recommended using a lookup type instead of a conditional type for reverse inference
 * [today](https://github.com/microsoft/TypeScript/issues/63461#issuecomment-4408990626) **RyanCavanaugh** said "Bisects to https://github.com/microsoft/TypeScript/pull/58910. I don't think this is unexpected given the setup"
 * **RyanCavanaugh** added label `Design Limitation`

### [PR microsoft/TypeScript#63462](https://github.com/microsoft/TypeScript/pull/63462) (Open, `For Uncommitted Bug`, `dependencies`, `javascript`)

**Bump fast\-xml\-builder from 1\.1\.4 to 1\.2\.0**

*Upgrade fast-xml-builder from version 1.1.4 to 1.2.0 to add sanitizeName option and xml-naming support.*

 * created by **dependabot[bot]**
 * (today) **dependabot[bot]** added labels `dependencies`, `javascript`, `dependencies`, `javascript`
 * **typescript-bot** added label `For Uncommitted Bug`

### [Issue microsoft/TypeScript#63463](https://github.com/microsoft/TypeScript/issues/63463) (Open)

**\`default\` keyword is offered in expression\-bodied arrow function completions**

*TypeScript’s completion engine incorrectly suggests ‘default’ in expression-bodied arrow function contexts despite it being invalid.*

 * created by **DhineshPonnarasan**
 * [later](https://github.com/microsoft/TypeScript/issues/63463#issuecomment-4412694071) **mkantor** clarified that `default` isn't special in that position and listed various invalid completions including JavaScript keywords, TypeScript keywords, and built-in type names
 * [later](https://github.com/microsoft/TypeScript/issues/63463#issuecomment-4412781473) **DhineshPonnarasan** agreed the issue was broader than default, identified other invalid completions in expression-bodied arrow functions, reframed the problem as an overly permissive completion set, and said they would investigate further before proposing changes

