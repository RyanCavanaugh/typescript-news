# Report for 2026-03-26 (Thursday, March 26th, 2026)

12 different users commented on 13 different issues.

## Recommended Actions

 * Response Recommended
    * @theengineear asked if there are existing solutions and suggested adding a flag or changing default behavior in [microsoft/TypeScript#58145](https://github.com/microsoft/TypeScript/issues/58145#issuecomment-4136885140)
    * @jobergner provided repro steps as requested in [microsoft/TypeScript#63195](https://github.com/microsoft/TypeScript/issues/63195#issuecomment-4143431748)
    * @dagecko reported active exploits affecting over 20,000 repositories and asked to confirm it was on the radar in [microsoft/TypeScript#63301](https://github.com/microsoft/TypeScript/pull/63301#issuecomment-4136224590)

## Activity Summary

### [Issue microsoft/TypeScript#58145](https://github.com/microsoft/TypeScript/issues/58145) (Open, `Bug`, `Help Wanted`, `Domain: Declaration Emit`)

**Declaration emit of private properties should strip jsdoc**

*TypeScript's declaration file emission currently retains JSDoc comments on private class members but should strip them out.*

 * (1.9 years ago) **RyanCavanaugh** added labels `Help Wanted`, `Domain: Declaration Emit`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/58145#issuecomment-4136885140) **theengineear** described confusion caused by private interface changes affecting emitted .d.ts diffs and requested a flag or behavior change to limit public contract diffs

### [Issue microsoft/TypeScript#63195](https://github.com/microsoft/TypeScript/issues/63195) (Open, `Needs More Info`)

**Debug Failure: "No error for last overload signature" crash when CustomTypeOptions\.resources uses typeof on a large \(~10k line\) JSON file**

*TypeScript crashes with 'No error for last overload signature' when using typeof on a large JSON for i18next CustomTypeOptions.resources.*

 * **RyanCavanaugh** added label `Needs More Info`
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/63195#issuecomment-4058537717) **RyanCavanaugh** said "Still can't repro this. Can you set up a cloneable repo?"
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/63195#issuecomment-4066964354) **paigefletcher1282-code** confirmed experiencing the issue and asked for it to be fixed
 * [later](https://github.com/microsoft/TypeScript/issues/63195#issuecomment-4143431748) **jobergner** shared a reproduction repository for the issue

### [Issue microsoft/TypeScript#63294](https://github.com/microsoft/TypeScript/issues/63294) (Closed, `Duplicate`)

**Omit\<UnionType, "NonDiscriminatedKey"\> cause failure in destructed type**

*Using Omit to remove a property from a discriminated union and then reintroducing it causes type resolution failures.*

 * **RyanCavanaugh** added label `Duplicate`
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63294#issuecomment-4121982017) **yarden-app** questioned why Omit's Pick implementation wasn't distributive and acknowledged that it wouldn't be changed due to being a breaking change
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63294#issuecomment-4122016065) **RyanCavanaugh** said "The current behavior is not super justifiable, but the results in https://github.com/microsoft/TypeScript/pull/53188 show how wildly disruptive it would be to change them."
 * [today](https://github.com/microsoft/TypeScript/issues/63294#issuecomment-4139458320) **typescript-bot** said "This issue has been marked as "Duplicate" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-bot** closed the issue

### [PR microsoft/TypeScript#63301](https://github.com/microsoft/TypeScript/pull/63301) (Closed)

**fix: pin 5 unpinned action\(s\)**

*Pins five unpinned third-party GitHub Actions to specific commit SHAs to remediate high-severity CI/CD security vulnerabilities.*

 * created by **dagecko**
 * [today](https://github.com/microsoft/TypeScript/pull/63301#issuecomment-4135951091) **jakebailey** said "Note that these are all actions owned by our team and are unpinned on purpose. I do not think we need this."
 * (today) **jakebailey** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/63301#issuecomment-4136224590) **dagecko** acknowledged the unpinned team-owned repos policy, warned of ongoing exploits affecting over 20,000 repositories, and appreciated the quick review

### [Issue microsoft/TypeScript#63303](https://github.com/microsoft/TypeScript/issues/63303) (Closed)

**TypeScript 6\.0\.2 assumes \`let x: \<type\> \| null\` is always null when set by an inner function**

*TypeScript 6.0.2 wrongly narrows a function|null variable to null after it is assigned inside an inner function.*

 * created by **SunsetFi**
 * [today](https://github.com/microsoft/TypeScript/issues/63303#issuecomment-4137710653) **MartinJohns** said "Duplicate of #9998."
 * [today](https://github.com/microsoft/TypeScript/issues/63303#issuecomment-4137753666) **SunsetFi** said "Looks like this goes way back.  I have no idea why I only encountered this now, but definitely not 6.0.2"
 * (today) **SunsetFi** closed the issue
 * [today](https://github.com/microsoft/TypeScript/issues/63303#issuecomment-4137765159) **MartinJohns** said "It's been like that for a long time. It definitely did not change between 5.9 and 6.0."

### [PR microsoft/TypeScript#63304](https://github.com/microsoft/TypeScript/pull/63304) (Closed)

**fix: allow enum member references with non\-identifier names as computed property names**

*Allow computed property names in type literals to reference enum members with non-identifier names via element access expressions*

 * created by **cyphercodes**
 * [today](https://github.com/microsoft/TypeScript/pull/63304#issuecomment-4138330841) **jakebailey** stated that PRs of this kind were not being accepted post-6.0, closed non-qualifying PRs, and provided criteria and next-step guidance
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#63305](https://github.com/microsoft/TypeScript/pull/63305) (Closed, **RyanCavanaugh**, **Copilot**)

**Add coding agent instructions: refuse PRs unless maintenance mode is acknowledged**

*Add a prominent maintenance-mode warning to coding agent instructions that refuses PRs until explicit acknowledgment.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#63306](https://github.com/microsoft/TypeScript/pull/63306) (Closed)

**Sort JSDoc @param completions by argument position**

*Adjust JSDoc @param completion sortText to include each parameter’s index, ensuring suggestion order matches the function signature*

 * created by **Vi-Ku**
 * [later](https://github.com/microsoft/TypeScript/pull/63306#issuecomment-4143356233) **RyanCavanaugh** noted that the repo is closed except for critical bugfixes and provided relevant links
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63307](https://github.com/microsoft/TypeScript/issues/63307) (Closed, `Won't Fix`)

**packageId is not generated when name or version fields are missing**

*TypeScript’s moduleNameResolver should generate packageId for packages missing name or version fields instead of returning undefined.*

 * created by **denis-sokolov**
 * [later](https://github.com/microsoft/TypeScript/issues/63307#issuecomment-4143565509) **RyanCavanaugh** said "Who's doing this and why? What's the observable problem?"
 * **RyanCavanaugh** added label `Needs More Info`

