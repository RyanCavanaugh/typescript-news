# Report for 2026-05-25 (Monday, May 25th, 2026)

7 different users commented on 22 different issues.

## Recommended Actions

 * Response Recommended
    * @wolfe8105 asked whether the issue should be closed in [microsoft/TypeScript#39114](https://github.com/microsoft/TypeScript/issues/39114#issuecomment-4536244675)
    * @wolfe8105 asked whether the issue should be closed in [microsoft/TypeScript#52313](https://github.com/microsoft/TypeScript/issues/52313#issuecomment-4535746169)
    * @YukiCodepth offered to work on the issue and update the release notes documentation in [microsoft/TypeScript#63212](https://github.com/microsoft/TypeScript/issues/63212#issuecomment-4536146400)
    * @snarbles2 asked if this was in the “Customize” options at the bottom of the playground in [microsoft/TypeScript#63507](https://github.com/microsoft/TypeScript/issues/63507#issuecomment-4544050956)

## Activity Summary

### [Issue microsoft/TypeScript#32392](https://github.com/microsoft/TypeScript/issues/32392) (Open, `Suggestion`, `Awaiting More Feedback`)

**Preserve comments with object destructuring assignment**

*Preserve and display JSDoc comments for properties when using object destructuring assignments in TypeScript*

 * [1.8 years ago](https://github.com/microsoft/TypeScript/issues/32392#issuecomment-2211007664) **nathanchase** expressed frustration about missing IntelliSense on destructured composable properties
 * [5 weeks ago](https://github.com/microsoft/TypeScript/issues/32392#issuecomment-4263114003) **zoltanium** noted the issue had lingered for seven years, speculated about it gaining traction, and volunteered to investigate specific code segments
 * [4 days ago](https://github.com/microsoft/TypeScript/issues/32392#issuecomment-4510709179) **Moto42** described forgetting that the feature doesn't work and added using Promise.all for grouping DB operations to the use-case list
 * [today](https://github.com/microsoft/TypeScript/issues/32392#issuecomment-4536800696) **zoltanium** informed that TypeScript is in code freeze until it's ported to Go, the repository is unmonitored with only catastrophic crash PRs accepted, and issues won't be addressed until version 7.0 at the earliest

### [Issue microsoft/TypeScript#39114](https://github.com/microsoft/TypeScript/issues/39114) (Open, `Bug`, `Domain: check: Control Flow`, `Has Repro`)

**improper declared type cause narrow type not work when its computed type is not union\.**

*Asserting a non-union variable to a union type prevents TypeScript from narrowing it exhaustively to never.*

 * [5.8 years ago](https://github.com/microsoft/TypeScript/issues/39114#issuecomment-660293346) **typescript-bot** said "Heya @orta, I've started to run the code sample repros for you. Here's the link to my best guess at the log."
 * [4.1 years ago](https://github.com/microsoft/TypeScript/issues/39114#issuecomment-1098572563) **typescript-bot** posted automated repro results showing a TS5107 error about deprecated moduleResolution=node10 and historical reproduction outputs
 * **RyanCavanaugh** added label `Domain: Control Flow`
 * [today](https://github.com/microsoft/TypeScript/issues/39114#issuecomment-4536244675) **wolfe8105** reported that the reproduction now compiles cleanly on current main and asked whether the issue should be closed

### [Issue microsoft/TypeScript#52313](https://github.com/microsoft/TypeScript/issues/52313) (Open, `Bug`, `Domain: check: Type Inference`, `Has Repro`, `Union Order Dependence`)

**Order of ReadonlySet/ReadonlyMap in union causes differing key inference**

*Union order of ReadonlySet and ReadonlyMap parameters causes inconsistent key type inference in TypeScript.*

 * [2.5 years ago](https://github.com/microsoft/TypeScript/issues/52313#issuecomment-1780617179) **typescript-bot** posted automated repro results showing deprecation error TS5107 for moduleResolution=node10 and slower performance
 * **jakebailey** added label `Union Order Dependence`
 * **RyanCavanaugh** added label `Domain: Type Inference`
 * [today](https://github.com/microsoft/TypeScript/issues/52313#issuecomment-4535746169) **wolfe8105** reported that the repro now compiled cleanly on main and suggested closing the issue

### [Issue microsoft/TypeScript#63212](https://github.com/microsoft/TypeScript/issues/63212) (Open, `Docs`)

**Add JSX\.ElementChildrenAttribute change to TypeScript 5\.8 release notes**

*Document the breaking change in TS 5.8 requiring explicit JSX.ElementChildrenAttribute for children inference*

 * created by **nmattia**
 * (11 weeks ago) **RyanCavanaugh** added label `Docs`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/63212#issuecomment-4536146400) **YukiCodepth** said "Hi, I would like to work on this issue and update the release notes documentation."

### [Issue microsoft/TypeScript#63503](https://github.com/microsoft/TypeScript/issues/63503) (Closed)

**Name of \`String\.padStart\`'s \`maxLength\` parameter is misleading**

*String.padStart and padEnd’s ‘maxLength’ parameter name misleads by implying maximum output length instead of the actual minimum length.*

 * created by **youngspe**
 * [later](https://github.com/microsoft/TypeScript/issues/63503#issuecomment-4543926827) **nmain** said "Interestingly, the canonical name of the parameter in the ECMAScript spec is maxLength.  Fortunately parameter names don't have any intrinsic meaning, so Typescript can diverge if it wants to."

### [PR microsoft/TypeScript#63505](https://github.com/microsoft/TypeScript/pull/63505) (Closed, `For Backlog Bug`)

**Fix narrowing of destructured discriminated union parameters with defaults**

*Removed initializer guards in checker predicates to restore type narrowing for destructured discriminated union parameters with default values.*

 * (today) **typescript-bot** added labels `For Backlog Bug`, `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63505#issuecomment-4535358692) **wolfe8105** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript/pull/63505#issuecomment-4536419332) **MartinJohns** said "@wolfe8105 You should read this: https://github.com/microsoft/TypeScript/issues/62963"

### [Issue microsoft/TypeScript#63507](https://github.com/microsoft/TypeScript/issues/63507) (Open, `Needs More Info`)

**Font bug**

*The TypeScript Playground's code font selection always reverts to Cascadia after changing it.*

 * created by **Liam1-dev**
 * [later](https://github.com/microsoft/TypeScript/issues/63507#issuecomment-4543905948) **MartinJohns** said "I can't see any issue with TypeScript here, and the description does not make it any clearer. Can you reduce your example to a minimum and describe the issue in more detail?"
 * [later](https://github.com/microsoft/TypeScript/issues/63507#issuecomment-4544050956) **snarbles2** asked whether the option was in the “Customize” settings at the bottom of the playground and noted it worked for them
 * **RyanCavanaugh** added label `Needs More Info`

