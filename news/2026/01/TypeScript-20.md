# Report for 2026-01-20 (Tuesday, January 20th, 2026)

14 different users commented on 153 different issues.

## Activity Summary

### [PR microsoft/TypeScript#42198](https://github.com/microsoft/TypeScript/pull/42198) (Closed, `For Backlog Bug`, **rbuckton**)

**\[Experiment\] feat\(7342\): Decorators not allowed classes expressions**

*Allow decorators on class expression members in TypeScript by adapting Babel’s transform approach.*

 * [4.6 years ago](https://github.com/microsoft/TypeScript/pull/42198#issuecomment-860160946) **canonic-epicure** asked @a-tarasyuk to review a StackOverflow question and provide brief instructions for implementing macros in a TypeScript transformer
 * [4.5 years ago](https://github.com/microsoft/TypeScript/pull/42198#issuecomment-881981467) **trusktr** expressed dislike of the new `@init` feature and proposed a workaround by using class declarations as statements
 * [26 weeks ago](https://github.com/microsoft/TypeScript/pull/42198#issuecomment-3094075004) **ahardin1** said "Any thoughts about reopening this now that the proposal is in stage 3?"
 * [today](https://github.com/microsoft/TypeScript/pull/42198#issuecomment-3774684576) **typescript-bot** said "The TypeScript team hasn't accepted the linked issue #7342. If you can get it accepted, this PR will have a better chance of being reviewed."

### [Issue microsoft/TypeScript#48594](https://github.com/microsoft/TypeScript/issues/48594) (Open, `Suggestion`, `In Discussion`)

**Anonymous type parameters**

*Enable inline anonymous generic constraints for function and type parameters in TypeScript without explicit type parameter declarations.*

 * [3.7 years ago](https://github.com/microsoft/TypeScript/issues/48594#issuecomment-1091754789) **jcalz** questioned whether implicitly added type parameters still need to be mentally tracked and asked what type `Person<Judge>` has under the proposal
 * [3.7 years ago](https://github.com/microsoft/TypeScript/issues/48594#issuecomment-1091930277) **RyanCavanaugh** argued that the proposal merely shoehorned negated types without solving other use cases and violated the golden rule of generics by using anonymous type parameters
 * [3.6 years ago](https://github.com/microsoft/TypeScript/issues/48594#issuecomment-1126633932) **lirannl** acknowledged that requiring explicit anonymous parameters would limit the feature and discussed its utility and limitations
 * [later](https://github.com/microsoft/TypeScript/issues/48594#issuecomment-3778643190) **devanshj** suggested existential types and linked an experimental PR demo, but agreed that negated types were preferable and noted it was unintended usage

### [Issue microsoft/TypeScript#54500](https://github.com/microsoft/TypeScript/issues/54500) (Open, `Discussion`, `Fix Available`)

**6\.0 Deprecation Candidates**

*Deprecation proposals for TypeScript 6.0 include removal of legacy compiler flags and updates to modern defaults*

 * [7 weeks ago](https://github.com/microsoft/TypeScript/issues/54500#issuecomment-3604830790) **michael-small** asked what the scope of `useDefineForClassFields` was in v6/v7 and referenced the proposed deprecation plan in issue #60284
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/54500#issuecomment-3745453163) **RyanCavanaugh** explained that useDefineForClassFields would remain supported in v6/v7 due to widespread dependencies and migration difficulty
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/54500#issuecomment-3764353180) **danilofuchs** asked whether noUncheckedIndexAccess would be enabled by default in strict mode
 * [today](https://github.com/microsoft/TypeScript/issues/54500#issuecomment-3774124466) **RyanCavanaugh** stated that noUncheckedIndexAccess would not be enabled by default in strict mode

### [PR microsoft/TypeScript#57838](https://github.com/microsoft/TypeScript/pull/57838) (Open, `For Uncommitted Bug`, **weswigham**)

**Fixed an issue with apparent mapped type keys**

*Corrected misidentification of apparent mapped type keys to resolve related TypeScript type resolution errors.*

 * [1.1 years ago](https://github.com/microsoft/TypeScript/pull/57838#issuecomment-2508761527) **typescript-bot** reported that the DT test results were ready and unchanged
 * [1.1 years ago](https://github.com/microsoft/TypeScript/pull/57838#issuecomment-2508769702) **typescript-bot** provided performance run results for the requested PR
 * [1.1 years ago](https://github.com/microsoft/TypeScript/pull/57838#issuecomment-2508782390) **typescript-bot** reported that running tsc on the top 400 repos comparing main and the PR merge showed everything looked good
 * [today](https://github.com/microsoft/TypeScript/pull/57838#issuecomment-3774627091) **gabritto** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/57838#issuecomment-3774627329) **typescript-bot** reported CI job statuses and provided result links
 * [today](https://github.com/microsoft/TypeScript/pull/57838#issuecomment-3774710420) **typescript-bot** reported that running the DT tests yielded no changes
 * [today](https://github.com/microsoft/TypeScript/pull/57838#issuecomment-3774734199) **typescript-bot** reported that user tests passed when comparing main and the pull request merge, aside from unrelated infrastructure failures
 * [today](https://github.com/microsoft/TypeScript/pull/57838#issuecomment-3774830273) **typescript-bot** reported the results of the requested performance run
 * [today](https://github.com/microsoft/TypeScript/pull/57838#issuecomment-3774941873) **typescript-bot** reported that running tsc on the top 400 repos comparing main and the PR merge showed everything looked good

