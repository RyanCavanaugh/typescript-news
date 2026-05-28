# Report for 2026-05-26 (Tuesday, May 26th, 2026)

8 different users commented on 15 different issues.

## Recommended Actions

 * Response Recommended
    * @davidgilbertson asked for the reasoning behind TypeScript's behavior regarding type inference on parameter reassignment in [microsoft/TypeScript#27706](https://github.com/microsoft/TypeScript/issues/27706#issuecomment-4549698637)
    * @guillaumebrunerie reported that the font dropdown label did not update after changing fonts in [microsoft/TypeScript#63507](https://github.com/microsoft/TypeScript/issues/63507#issuecomment-4546240951)

## Activity Summary

### [Issue microsoft/TypeScript#202](https://github.com/microsoft/TypeScript/issues/202) (Open, `Suggestion`, `In Discussion`)

**Support some non\-structural \(nominal\) type matching**

*Introduce nominal typing in TypeScript to distinguish structurally identical types and prevent unintended type mixing.*

 * [2.1 years ago](https://github.com/microsoft/TypeScript/issues/202#issuecomment-2053756892) **nathan-chappell** said "@craigphicks Great, thanks, cheers."
 * [1 year ago](https://github.com/microsoft/TypeScript/issues/202#issuecomment-2868870489) **emilioplatzer** shared a workaround with example repository and Playground link and explained a typing-by-example approach using string literal types
 * [1 year ago](https://github.com/microsoft/TypeScript/issues/202#issuecomment-2868870489) **emilioplatzer** shared a workaround with example repository and Playground link and explained a typing-by-example approach using string literal types
 * [today](https://github.com/microsoft/TypeScript/issues/202#issuecomment-4549960682) **bluepnume** described how they currently simulate opaque types with intersection types and custom tooling, illustrated how native opaque types and operator overloading would improve their workflow, linked to issue #42218, and expressed strong support
 * [today](https://github.com/microsoft/TypeScript/issues/202#issuecomment-4549960682) **bluepnume** described how they currently simulate opaque types with intersection types and custom tooling, illustrated how native opaque types and operator overloading would improve their workflow, linked to issue #42218, and expressed strong support

### [Issue microsoft/TypeScript#27706](https://github.com/microsoft/TypeScript/issues/27706) (Open, `Suggestion`, `In Discussion`)

**Type inference/narrowing lost after assignment**

*Type narrowing of an unknown variable to string is lost after reassigning it, reverting back to unknown.*

 * [30 weeks ago](https://github.com/microsoft/TypeScript/issues/27706#issuecomment-3446834159) **sparecycles** said "So a guard clause that narrows a type is "weaker" than a reassignment that narrows the type."
 * [30 weeks ago](https://github.com/microsoft/TypeScript/issues/27706#issuecomment-3448424923) **mkmlab-v2** analyzed a TypeScript type narrowing issue after assignment, explained its cause and current discussion status, and proposed temporary workarounds and documentation updates
 * [11 weeks ago](https://github.com/microsoft/TypeScript/issues/27706#issuecomment-3999318068) **fudom** explained that type-guarded string variables revert to unknown after trimming or lowercasing and suggested adding another example
 * [today](https://github.com/microsoft/TypeScript/issues/27706#issuecomment-4549698637) **davidgilbertson** observed that TypeScript did not narrow the type of a reassigned unknown parameter as it did for a new variable and asked for the reasoning behind this behavior

### [Issue microsoft/TypeScript#39114](https://github.com/microsoft/TypeScript/issues/39114) (Open, `Bug`, `Domain: check: Control Flow`, `Has Repro`)

**improper declared type cause narrow type not work when its computed type is not union\.**

*Asserting a non-union variable to a union type prevents TypeScript from narrowing it exhaustively to never.*

 * [4.1 years ago](https://github.com/microsoft/TypeScript/issues/39114#issuecomment-1098572563) **typescript-bot** posted automated repro results showing a TS5107 error about deprecated moduleResolution=node10 and historical reproduction outputs
 * **RyanCavanaugh** added label `Domain: Control Flow`
 * [yesterday](https://github.com/microsoft/TypeScript/issues/39114#issuecomment-4536244675) **wolfe8105** reported that the reproduction now compiles cleanly on current main and asked whether the issue should be closed
 * [today](https://github.com/microsoft/TypeScript/issues/39114#issuecomment-4545996888) **RyanCavanaugh** said "@wolfe8105 how are you checking? x is still B, not never, in the last statement of that block"
 * [today](https://github.com/microsoft/TypeScript/issues/39114#issuecomment-4550709668) **wolfe8105** reported building an algorithm, noted its first test caused extra noise, apologized, and stated the issue was fixed

### [Issue microsoft/TypeScript#42218](https://github.com/microsoft/TypeScript/issues/42218) (Open, `Suggestion`, `Awaiting More Feedback`)

**Proposal: Operator overloading and primitive type declarations**

*Introduce TypeScript syntax for declaring primitive types with operator overload signatures to specify allowable operand and result types.*

 * [4.2 years ago](https://github.com/microsoft/TypeScript/issues/42218#issuecomment-1044217492) **iliazeus** suggested detaching operator overloading from the primitive proposal, proposed a conservative operator overload syntax example, and listed use cases
 * [4 years ago](https://github.com/microsoft/TypeScript/issues/42218#issuecomment-1124248820) **Judahh** said "Work with packages like bignumber.js and dinero.js would improve significantly."
 * [2.5 years ago](https://github.com/microsoft/TypeScript/issues/42218#issuecomment-1820214330) **OldStarchy** described custom primitive types for units in TypeScript and suggested enhancements for operator type inference and implicit casting to number
 * [today](https://github.com/microsoft/TypeScript/issues/42218#issuecomment-4549956453) **bluepnume** expressed strong support for the proposal and described use of branded number primitives and custom math wrappers in a TypeScript codebase

### [Issue microsoft/TypeScript#52313](https://github.com/microsoft/TypeScript/issues/52313) (Open, `Bug`, `Domain: check: Type Inference`, `Has Repro`, `Union Order Dependence`)

**Order of ReadonlySet/ReadonlyMap in union causes differing key inference**

*Union order of ReadonlySet and ReadonlyMap parameters causes inconsistent key type inference in TypeScript.*

 * **jakebailey** added label `Union Order Dependence`
 * **RyanCavanaugh** added label `Domain: Type Inference`
 * [yesterday](https://github.com/microsoft/TypeScript/issues/52313#issuecomment-4535746169) **wolfe8105** reported that the repro now compiled cleanly on main and suggested closing the issue
 * [today](https://github.com/microsoft/TypeScript/issues/52313#issuecomment-4546013771) **RyanCavanaugh** said "@wolfe8105 how are you checking? I still see an error in the Playground on 6.0"

### [Issue microsoft/TypeScript#63503](https://github.com/microsoft/TypeScript/issues/63503) (Closed)

**Name of \`String\.padStart\`'s \`maxLength\` parameter is misleading**

*String.padStart and padEnd’s ‘maxLength’ parameter name misleads by implying maximum output length instead of the actual minimum length.*

 * created by **youngspe**
 * [today](https://github.com/microsoft/TypeScript/issues/63503#issuecomment-4543926827) **nmain** said "Interestingly, the canonical name of the parameter in the ECMAScript spec is maxLength.  Fortunately parameter names don't have any intrinsic meaning, so Typescript can diverge if it wants to."
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#63504](https://github.com/microsoft/TypeScript/pull/63504) (Closed, `For Uncommitted Bug`)

**lib: fix misleading \`maxLength\` param on string pad\* methods**

*Rename the maxLength parameter in String.padStart and padEnd to targetLength and update their documentation to match MDN.*

 * created by **youngspe**
 * **typescript-bot** added label `For Uncommitted Bug`
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/63504#issuecomment-4531146841) **youngspe** said "@microsoft-github-policy-service agree"
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#63505](https://github.com/microsoft/TypeScript/pull/63505) (Closed, `For Backlog Bug`)

**Fix narrowing of destructured discriminated union parameters with defaults**

*Removed initializer guards in checker predicates to restore type narrowing for destructured discriminated union parameters with default values.*

 * **typescript-bot** added label `For Backlog Bug`
 * [yesterday](https://github.com/microsoft/TypeScript/pull/63505#issuecomment-4535358692) **wolfe8105** said "@microsoft-github-policy-service agree"
 * [yesterday](https://github.com/microsoft/TypeScript/pull/63505#issuecomment-4536419332) **MartinJohns** said "@wolfe8105 You should read this: https://github.com/microsoft/TypeScript/issues/62963"
 * [today](https://github.com/microsoft/TypeScript/pull/63505#issuecomment-4545969436) **RyanCavanaugh** said "Seconding Martin's comment. This should be easy to port to the Go codebase, though."
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63507](https://github.com/microsoft/TypeScript/issues/63507) (Open, `Needs More Info`)

**Font bug**

*The TypeScript Playground's code font selection always reverts to Cascadia after changing it.*

 * [today](https://github.com/microsoft/TypeScript/issues/63507#issuecomment-4543905948) **MartinJohns** said "I can't see any issue with TypeScript here, and the description does not make it any clearer. Can you reduce your example to a minimum and describe the issue in more detail?"
 * [today](https://github.com/microsoft/TypeScript/issues/63507#issuecomment-4544050956) **snarbles2** asked whether the option was in the “Customize” settings at the bottom of the playground and noted it worked for them
 * **RyanCavanaugh** added label `Needs More Info`
 * [today](https://github.com/microsoft/TypeScript/issues/63507#issuecomment-4546240951) **guillaumebrunerie** described that changing the font updated the playground but the dropdown label remained 'Cascadia'
 * [today](https://github.com/microsoft/TypeScript/issues/63507#issuecomment-4547275063) **nmain** reported seeing the same issue and questioned the relevance of the code sample

### [PR microsoft/TypeScript#63508](https://github.com/microsoft/TypeScript/pull/63508) (Open, `For Backlog Bug`)

**Add missing JSDoc to ReadonlySet and ReadonlyMap members**

*Add JSDoc comments to ReadonlySet and ReadonlyMap methods to match their mutable counterparts.*

 * created by **TxsharDev**
 * **typescript-bot** added label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/63508#issuecomment-4556208480) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [later](https://github.com/microsoft/TypeScript/pull/63508#issuecomment-4556208485) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [later](https://github.com/microsoft/TypeScript/pull/63508#issuecomment-4556218663) **TxsharDev** said "@microsoft-github-policy-service agree"
 * (later) **typescript-bot** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`

