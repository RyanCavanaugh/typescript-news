# Report for 2026-05-18 (Monday, May 18th, 2026)

11 different users commented on 16 different issues.

## Recommended Actions

 * Response Recommended
    * @JohanRonnblom asked for clarification on how undefined separator could be harmful and about the resulting type error in [microsoft/TypeScript#63456](https://github.com/microsoft/TypeScript/issues/63456#issuecomment-4482691858)
    * @niledas asked for a review of the PR in [microsoft/TypeScript#63483](https://github.com/microsoft/TypeScript/pull/63483#issuecomment-4485867222)
    * @angrybacon provided a link to a possibly related issue in [microsoft/TypeScript#63493](https://github.com/microsoft/TypeScript/issues/63493#issuecomment-4487563985)
    * @danyalahmed1995 suggested that maintainer guidance is needed before implementation in [microsoft/TypeScript#63493](https://github.com/microsoft/TypeScript/issues/63493#issuecomment-4488450779)

## Activity Summary

### [Issue microsoft/TypeScript#54160](https://github.com/microsoft/TypeScript/issues/54160) (Closed, `Design Limitation`)

**Type hole: everything is assignable to element of generic indexable**

*A generic function returning T[0] erroneously accepts any value instead of enforcing the inferred tuple element type.*

 * [2.6 years ago](https://github.com/microsoft/TypeScript/issues/54160#issuecomment-1754004825) **mkantor** provided TypeScript code examples showing that writing to properties of generic inputs caused type unsafety and suggested it reflected the same underlying problem
 * [2.5 years ago](https://github.com/microsoft/TypeScript/issues/54160#issuecomment-1754701386) **awerlogus** said "@mkantor You may be looking for https://github.com/microsoft/TypeScript/issues/39915"
 * (2.2 years ago) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript/issues/54160#issuecomment-4480232274) **mkantor** stumbled across unsound legal code concerning default values for destructured properties of type parameters and linked an example

### [Issue microsoft/TypeScript#60483](https://github.com/microsoft/TypeScript/issues/60483) (Closed, `Unactionable`)

**Object\.keys: Return Non\-widening literal types for type\-inferred objects while maintaining existing behavior for type\-assigned objects**

*Enhance TypeScript’s Object.keys overloads to return precise literal key types for type-inferred objects while preserving string[] for explicitly typed objects*

 * [1.5 years ago](https://github.com/microsoft/TypeScript/issues/60483#issuecomment-2471204247) **RyanCavanaugh** noted that the proposed language change did not prevent additional properties and demonstrated the issue with a TypeScript example
 * (1.5 years ago) **nakjun12** closed the issue
 * [1.5 years ago](https://github.com/microsoft/TypeScript/issues/60483#issuecomment-2480363270) **nakjun12** asked for clarification about the design decision allowing Object.values() to have narrower types despite similar runtime concerns
 * [today](https://github.com/microsoft/TypeScript/issues/60483#issuecomment-4482940329) **peterflynn** referred to debate in #38520 and explained that Object.values() and Object.entries() types remain unchanged to avoid a breaking change after ten years

### [Issue microsoft/TypeScript#63456](https://github.com/microsoft/TypeScript/issues/63456) (Open, `Suggestion`, `Awaiting More Feedback`)

**String\.split\(\) method's separator argument should allow undefined**

*Allow undefined as separator in String.split to return the full string array per spec.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/63456#issuecomment-4372476749) **RyanCavanaugh** explained that the split behavior is entirely defined by the spec, highlighted the significant difference between split() and split(c), and requested a code sample with a strong feedback signal to consider changing it
 * (2 weeks ago) **RyanCavanaugh** added labels `Suggestion`, `Awaiting More Feedback`
 * [today](https://github.com/microsoft/TypeScript/issues/63456#issuecomment-4482691858) **JohanRonnblom** questioned how splitting with undefined could be harmful and argued that MDN specifies split(undefined) returns the original string in an array, so found the type error surprising

### [PR microsoft/TypeScript#63483](https://github.com/microsoft/TypeScript/pull/63483) (Open, `For Backlog Bug`)

**docs: add JSDoc comments to ReadonlySet interface**

*Add JSDoc comments to the ReadonlySet interface to improve its documentation.*

 * created by **niledas**
 * **typescript-bot** added label `For Backlog Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/63483#issuecomment-4485867222) **niledas** said "Hi @RyanCavanaugh, please help review this small PR. Let me know if you have any suggestions."

### [Issue microsoft/TypeScript#63490](https://github.com/microsoft/TypeScript/issues/63490) (Open, `Duplicate`)

**Improve control\-flow narrowing for Object\.hasOwn\(obj, key\)**

*TypeScript should treat Object.hasOwn(obj, key) as a type guard to narrow key availability for safer property access.*

 * created by **eng-same**
 * [today](https://github.com/microsoft/TypeScript/issues/63490#issuecomment-4480192501) **MartinJohns** said "Duplicate of #44253."
 * **RyanCavanaugh** added label `Duplicate`

### [PR microsoft/TypeScript#63491](https://github.com/microsoft/TypeScript/pull/63491) (Open, `For Uncommitted Bug`)

**63480**

*Corrects a grammar typo in the JSDoc for the Set#size method by changing 'the Set' to 'in the Set'. *

 * created by **driphtyio**
 * **typescript-bot** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63491#issuecomment-4483689354) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [today](https://github.com/microsoft/TypeScript/pull/63491#issuecomment-4483689362) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [later](https://github.com/microsoft/TypeScript/pull/63491#issuecomment-4487784135) **MartinJohns** said "Duplicate of #63482."

### [PR microsoft/TypeScript#63492](https://github.com/microsoft/TypeScript/pull/63492) (Open, `For Uncommitted Bug`)

**Fix typo in README: behavorial \-\> behavioral**

*Correct the misspelled word “behavorial” to “behavioral” in the README file.*

 * created by **Lefgk**
 * **typescript-bot** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63492#issuecomment-4484937242) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [today](https://github.com/microsoft/TypeScript/pull/63492#issuecomment-4484937258) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [later](https://github.com/microsoft/TypeScript/pull/63492#issuecomment-4487776201) **MartinJohns** quoted the pull request template warning against sending typo-fix-only PRs

### [Issue microsoft/TypeScript#63493](https://github.com/microsoft/TypeScript/issues/63493) (Open)

**Configuration to auto\-import with inline type specifiers**

*Implement a config option to auto-import types using inline specifiers or top-level import syntax.*

 * created by **angrybacon**
 * [later](https://github.com/microsoft/TypeScript/issues/63493#issuecomment-4487563985) **angrybacon** said "Possibly related https://github.com/microsoft/TypeScript/issues/54664"
 * [later](https://github.com/microsoft/TypeScript/issues/63493#issuecomment-4488450779) **danyalahmed1995** noted that the request was reasonable but did not meet the bar for a TS 7 change and recommended maintainer guidance before implementation
 * [later](https://github.com/microsoft/TypeScript/issues/63493#issuecomment-4488958755) **MartinJohns** clarified that the TS7 bar applies to pull requests not issues, noting the codebase switch to Go to minimize porting changes

### [Issue microsoft/TypeScript#63494](https://github.com/microsoft/TypeScript/issues/63494) (Open)

**Typo in README: 'behavorial' should be 'behavioral'**

*The README incorrectly spells 'behavioral' as 'behavorial'.*

 * created by **Lefgk**

