# Report for 2026-05-17 (Sunday, May 17th, 2026)

8 different users commented on 9 different issues.

## Recommended Actions

 * Response Recommended
    * @user451421541757324 asked if any workarounds were found in [microsoft/TypeScript#54488](https://github.com/microsoft/TypeScript/issues/54488#issuecomment-4476938963)

## Activity Summary

### [Issue microsoft/TypeScript#54488](https://github.com/microsoft/TypeScript/issues/54488) (Open, `Suggestion`, `In Discussion`)

**\`satisfies\` should work with imported / referenced values**

*Enable TypeScript’s satisfies operator to apply to imported or referenced values (e.g. JSON imports) rather than only inline literals.*

 * [2.9 years ago](https://github.com/microsoft/TypeScript/issues/54488#issuecomment-1577206615) **matthew-dean** thanked for the clarification and agreed that using 'satisfies' with 'as const' would meet requirements without a .d.ts, and noted that contextual typing on JSON might be useful in some scenarios
 * (2.9 years ago) **RyanCavanaugh** added labels `Suggestion`, `In Discussion`
 * [later](https://github.com/microsoft/TypeScript/issues/54488#issuecomment-4476938963) **user451421541757324** asked if any workarounds were found given TypeScript's evolution

### [Issue microsoft/TypeScript#60649](https://github.com/microsoft/TypeScript/issues/60649) (Open, `Suggestion`, `Awaiting More Feedback`)

**should error on assignment that shadows a prototype method**

*TypeScript should report an error when assigning an instance property in a constructor that shadows an existing prototype method*

 * [1.4 years ago](https://github.com/microsoft/TypeScript/issues/60649#issuecomment-2510667433) **bradzacher** explained that the Flow error was caused by Flow treating all methods as readonly rather than the previously suggested reason
 * (1.4 years ago) **RyanCavanaugh** added labels `Suggestion`, `Awaiting More Feedback`
 * [later](https://github.com/microsoft/TypeScript/issues/60649#issuecomment-4477510263) **kirkwaiblinger** said "I guess this could be considered a special case of https://github.com/microsoft/TypeScript/issues/22315 (all methods readonly), which I would also support. "

### [Issue microsoft/TypeScript#63465](https://github.com/microsoft/TypeScript/issues/63465) (Closed, `Won't Fix`)

**Implement interface codefix is offered when the implemented interface type is invalid**

*Implement interface codefix is offered even when the implemented interface has invalid type arguments or unresolved symbols.*

 * **RyanCavanaugh** added label `Won't Fix`
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63465#issuecomment-4461413095) **RyanCavanaugh** said "I don't see the point of trying to "fix" this when there's no right answer to begin with."
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63465#issuecomment-4461907364) **danyalahmed1995** said "Understandable I see your point of having no clear answer for the "fix" You already answered this on PR#63466 that this doesn't meet the bar for 6.0 patch.Feel free to close it."
 * [today](https://github.com/microsoft/TypeScript/issues/63465#issuecomment-4473487211) **typescript-bot** said "This issue has been marked as "Won't Fix" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-bot** closed the issue

### [Issue microsoft/TypeScript#63476](https://github.com/microsoft/TypeScript/issues/63476) (Closed, `Duplicate`)

**\`===\` is not strong enough to narrow equal values to the same type**

*TypeScript's strict equality check doesn't narrow an unknown input to a specific string literal union type.*

 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63476#issuecomment-4452487438) **RyanCavanaugh** provided an automated analysis listing similar issues for potential duplication
 * **RyanCavanaugh** added label `Duplicate`
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63476#issuecomment-4458703337) **khalil-mhiri-cyber** said "I can work on this issue if you need"
 * [today](https://github.com/microsoft/TypeScript/issues/63476#issuecomment-4473486961) **typescript-bot** said "This issue has been marked as "Duplicate" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-bot** closed the issue

### [Issue microsoft/TypeScript#63486](https://github.com/microsoft/TypeScript/issues/63486) (Closed, `Suggestion`, `Out of Scope`)

**\[Feature Request\] Official native AOT binary compiler**

*Propose Microsoft develop an official TypeScript native AOT compiler to generate cross-platform binaries with native library linking and UI/GPU support.*

 * created by **adevart**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63486#issuecomment-4468699394) **MartinJohns** said "This is out of scope. Check the Viability Checklist again."
 * (later) **RyanCavanaugh** added labels `Suggestion`, `Out of Scope`
 * [later](https://github.com/microsoft/TypeScript/issues/63486#issuecomment-4479351292) **RyanCavanaugh** said "TypeScript is a type checker for JavaScript, not a runtime stack."
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63487](https://github.com/microsoft/TypeScript/issues/63487) (Closed, `Duplicate`)

**Type\-narrowing on array elements persists after array mutations**

*TypeScript incorrectly preserves array element type-narrowing after mutative operations like shift, leading to false errors.*

 * created by **raydog**
 * [today](https://github.com/microsoft/TypeScript/issues/63487#issuecomment-4472011859) **MartinJohns** said "This is essentially another duplicate of #9998. And a duplicate of #31334."
 * **RyanCavanaugh** added label `Duplicate`

### [PR microsoft/TypeScript#63488](https://github.com/microsoft/TypeScript/pull/63488) (Closed)

**fix\(lib\): add missing JSDoc to ReadonlySet and fix Set\#size grammar**

*Add missing JSDoc for ReadonlySet methods and fix the grammar in Set#size documentation.*

 * created by **Zelys-DFKH**
 * [today](https://github.com/microsoft/TypeScript/pull/63488#issuecomment-4472046489) **Zelys-DFKH** said "Closing to revise before resubmission — draft opened prematurely."
 * (today) **Zelys-DFKH** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/63488#issuecomment-4472098027) **MartinJohns** said "There are already open PR to fix these issues. Why open another one?"

### [PR microsoft/TypeScript#63489](https://github.com/microsoft/TypeScript/pull/63489) (Open, `For Uncommitted Bug`)

**Fix \`es2020\.intl\.d\.ts\` formatting**

*Correct inconsistent formatting in the es2020.intl.d.ts TypeScript declaration file.*

 * created by **turansky**
 * **typescript-bot** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63489#issuecomment-4472153592) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [today](https://github.com/microsoft/TypeScript/pull/63489#issuecomment-4472153608) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."

