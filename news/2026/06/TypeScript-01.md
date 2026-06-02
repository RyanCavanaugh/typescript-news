# Report for 2026-06-01 (Monday, June 1st, 2026)

10 different users commented on 22 different issues.

## Recommended Actions

 * Response Recommended
    * @ritschwumm asked where the `as` operator precedence is documented in [microsoft/TypeScript#63527](https://github.com/microsoft/TypeScript/issues/63527#issuecomment-4602727661)
    * @snarbles2 asked if “erasable syntax only” implies “blankable” or if that was just assumed in [microsoft/TypeScript#63527](https://github.com/microsoft/TypeScript/issues/63527#issuecomment-4603029422)

## Activity Summary

### [Issue microsoft/TypeScript#43368](https://github.com/microsoft/TypeScript/issues/43368) (Open, `Suggestion`, `Awaiting More Feedback`)

**Suggestion: Allow getters to have predicate return types**

*Enable TypeScript class getters to have user-defined type predicate return types for type guards.*

 * [39 weeks ago](https://github.com/microsoft/TypeScript/issues/43368#issuecomment-3243558010) **qolity** described encountering incorrect type inference with a property-based isRight approach and explaining why the type predicate method, though accurate, is prone to accidental misuse
 * [11 weeks ago](https://github.com/microsoft/TypeScript/issues/43368#issuecomment-4046270378) **alex-at-happening** said "That would be awesome to have it in TS"
 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/43368#issuecomment-4410653140) **owenoak** said "+1 for this"
 * [later](https://github.com/microsoft/TypeScript/issues/43368#issuecomment-4600711749) **MaestroDD0S** said "+1 "

### [Issue microsoft/TypeScript#63481](https://github.com/microsoft/TypeScript/issues/63481) (Open, `Help Wanted`, `Domain: lib.d.ts`, `Possible Improvement`)

**\`ReadonlySet\` lacks documentation for \`has\`, \`forEach\` and \`size\`**

*ReadonlySet<T> in lib.es2015.collection.d.ts lacks documentation for its has, forEach, and size members.*

 * (2 weeks ago) **RyanCavanaugh** added labels `Domain: lib.d.ts`, `Possible Improvement`
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/63481#issuecomment-4531194717) **vitalysinitsin** said "I'd like to do that!"
 * [today](https://github.com/microsoft/TypeScript/issues/63481#issuecomment-4594935599) **RyanCavanaugh** said "Can people PLEASE stop sending PRs when there's already an open identical PR open for the issue? What is going on??"
 * [today](https://github.com/microsoft/TypeScript/issues/63481#issuecomment-4595081680) **vitalysinitsin** noted that there were enough people looking into the issue and that they would bow out
 * [today](https://github.com/microsoft/TypeScript/issues/63481#issuecomment-4595148889) **RyanCavanaugh** appreciated the check before PRing and noted that Claude’s issue search list top issue often attracts multiple PRs regardless of the docs

### [PR microsoft/TypeScript#63508](https://github.com/microsoft/TypeScript/pull/63508) (Closed, `For Backlog Bug`)

**Add missing JSDoc to ReadonlySet and ReadonlyMap members**

*Add JSDoc comments to ReadonlySet and ReadonlyMap methods to match their mutable counterparts.*

 * **typescript-bot** added label `For Backlog Bug`
 * [5 days ago](https://github.com/microsoft/TypeScript/pull/63508#issuecomment-4559385934) **MartinJohns** said "Why another one? There's already #63483 and #63488. Seems to be done by AI."
 * [5 days ago](https://github.com/microsoft/TypeScript/pull/63508#issuecomment-4559644821) **TxsharDev** thanked MartinJohns, noted that #63488 was closed and #63483 only covered ReadonlySet, added JSDoc to ReadonlyMap methods to fill the same documentation gap, offered to remove the ReadonlySet portion if maintainers preferred, and clarified that the JSDoc was hand-written rather than AI-generated
 * [today](https://github.com/microsoft/TypeScript/pull/63508#issuecomment-4595017578) **RyanCavanaugh** closed the pull request because it duplicated work and contained unhelpful commentary on JavaScript Map semantics
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63512](https://github.com/microsoft/TypeScript/issues/63512) (Closed, `Not a Defect`)

**Missing JSDoc annotations in esnext lib declaration files**

*ESNext lib declaration files are missing JSDoc @param and @returns annotations, undermining IntelliSense documentation consistency.*

 * created by **Se3do**
 * [today](https://github.com/microsoft/TypeScript/issues/63512#issuecomment-4594969497) **RyanCavanaugh** argued that adding tautological comments was noise and that feedback-driven actionable comments were needed
 * (today) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** added label `Not a Defect`

### [PR microsoft/TypeScript#63513](https://github.com/microsoft/TypeScript/pull/63513) (Closed, `For Uncommitted Bug`)

**Add missing JSDoc param and returns tags to lib\.d\.ts esnext files**

*Add missing JSDoc @param and @returns annotations to esnext lib.d.ts APIs including Error.isError, Date.toTemporalInstant, Atomics.pause, Map/WeakMap getOrInsert, Array.fromAsync, and Uint8Array.fromHex.*

 * created by **Se3do**
 * **typescript-bot** added label `For Uncommitted Bug`
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/63513#issuecomment-4562709948) **Se3do** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript/pull/63513#issuecomment-4594971656) **RyanCavanaugh** said "Linked issue is rejected."
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#63516](https://github.com/microsoft/TypeScript/pull/63516) (Open, `For Backlog Bug`, `Voight-Kampff Anomaly`)

**Update toFixed/toExponential/toPrecision digit range in docs to match the spec**

*Update Number.prototype.toFixed, toExponential, and toPrecision documentation to reflect the ES2018 spec’s increased digit limits of 0–100 and 1–100.*

 * created by **ibondarenko1**
 * **typescript-bot** added label `For Backlog Bug`
 * **RyanCavanaugh** added label `Voight-Kampff Anomaly`

### [PR microsoft/TypeScript#63518](https://github.com/microsoft/TypeScript/pull/63518) (Closed, `For Backlog Bug`)

**fix: Inconsistencies in ESM\-style imports of accessibility\-modified proper\.\.\.**

*Resolve inconsistencies in ESM-style imports of accessibility-modified class exports by updating checker logic and related documentation.*

 * created by **arnavnagzirkar**
 * **typescript-bot** added label `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63518#issuecomment-4594906811) **RyanCavanaugh** said "https://github.com/microsoft/TypeScript/pull/63521#issuecomment-4594858123"
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#63519](https://github.com/microsoft/TypeScript/pull/63519) (Closed, `For Backlog Bug`)

**fix: \`silentNeverType\` leak in contextual parameter types coming from anon\.\.\.**

*Propagate NonInferrableType flags to anonymous object type instantiations to prevent silentNeverType leaking in contextual parameter types.*

 * created by **arnavnagzirkar**
 * **typescript-bot** added label `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63519#issuecomment-4594865254) **RyanCavanaugh** said "https://github.com/microsoft/TypeScript/pull/63521#issuecomment-4594858123"
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#63520](https://github.com/microsoft/TypeScript/pull/63520) (Closed, `For Backlog Bug`)

**fix: Deprecation error message reporting method type as deprecated instead\.\.\.**

*Add an identifier check in addDeprecatedSuggestionWithSignature to display the deprecated method name instead of its full signature in deprecation messages.*

 * created by **arnavnagzirkar**
 * **typescript-bot** added label `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63520#issuecomment-4594862655) **RyanCavanaugh** said "https://github.com/microsoft/TypeScript/pull/63521#issuecomment-4594858123"
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#63521](https://github.com/microsoft/TypeScript/pull/63521) (Closed, `For Backlog Bug`)

**fix: Incorrect report of self\-referencing type for static fields**

*Prevent false circularity errors when inferring static property initializer types in generic class expressions by detecting in-progress symbol resolutions.*

 * created by **arnavnagzirkar**
 * **typescript-bot** added label `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63521#issuecomment-4594858123) **RyanCavanaugh** noted that the change didn't meet the 6.0 patch bar and asked how Copilot was invoked
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#63524](https://github.com/microsoft/TypeScript/pull/63524) (Closed, `For Backlog Bug`, `Voight-Kampff Anomaly`)

**feat\(lib\): add Math\.sumPrecise type definition \(ES2026\)**

*Add Math.sumPrecise type definition to TypeScript library declarations for ES2026.*

 * created by **godfengliang**
 * **typescript-bot** added label `For Backlog Bug`
 * **RyanCavanaugh** added label `Voight-Kampff Anomaly`
 * [today](https://github.com/microsoft/TypeScript/pull/63524#issuecomment-4594888219) **RyanCavanaugh** said "https://github.com/microsoft/TypeScript/blob/main/CONTRIBUTING.md#use-of-ai-assistance"
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#63525](https://github.com/microsoft/TypeScript/pull/63525) (Open, `For Uncommitted Bug`)

**Fix JSDoc grammar typo: 'returns a undefined' → 'returns undefined'**

*Grammar typo corrected in JSDoc for SymbolConstructor.keyFor by changing '@returns a undefined' to '@returns undefined'*

 * created by **driphtyio**
 * **typescript-bot** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63525#issuecomment-4599055168) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [today](https://github.com/microsoft/TypeScript/pull/63525#issuecomment-4599055185) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [today](https://github.com/microsoft/TypeScript/pull/63525#issuecomment-4599055199) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [today](https://github.com/microsoft/TypeScript/pull/63525#issuecomment-4599056099) **microsoft-github-policy-service[bot]** requested that the contributor read and agree to the CLA by replying with a specific command

### [PR microsoft/TypeScript#63526](https://github.com/microsoft/TypeScript/pull/63526) (Open, `For Backlog Bug`)

**Allow element access on enum as computed property name in type literal**

*Permit using enum members with non-identifier names as computed property keys in type literals by treating bracket access expressions as late-bindable.*

 * created by **driphtyio**
 * (today) **typescript-bot** added labels `For Backlog Bug`, `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63526#issuecomment-4599078574) **microsoft-github-policy-service[bot]** requested that the contributor read and agree to the CLA by replying with a specific command
 * [today](https://github.com/microsoft/TypeScript/pull/63526#issuecomment-4599078577) **microsoft-github-policy-service[bot]** requested that the contributor read and agree to the CLA by replying with a specific command

### [Issue microsoft/TypeScript#63527](https://github.com/microsoft/TypeScript/issues/63527) (Open)

**\`erasableSyntaxOnly\` should error on unerasable \`as\`/\`satisfies\`**

*ErasableSyntaxOnly should report errors for as or satisfies expressions that cannot be safely removed.*

 * created by **robpalme**
 * [later](https://github.com/microsoft/TypeScript/issues/63527#issuecomment-4602727661) **ritschwumm** expressed surprise at the `as` operator precedence and wondered where it was documented
 * [later](https://github.com/microsoft/TypeScript/issues/63527#issuecomment-4603029422) **snarbles2** mentioned inability to find documentation for the `as` operator precedence and asked whether “erasable syntax only” implies “blankable” or if that was merely assumed
 * [later](https://github.com/microsoft/TypeScript/issues/63527#issuecomment-4603595943) **acutmore** questioned whether “erasable syntax only” implies “blankable” and referenced a precedent banning old `<Type>val` assertion syntax with an example illustrating the need for parentheses

