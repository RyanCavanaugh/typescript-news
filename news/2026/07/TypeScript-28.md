# Report for 2026-07-28 (Tuesday, July 28th, 2026)

9 different users commented on 9 different issues.

## Recommended Actions

 * Response Recommended
    * @gershy-clutch asked if there was any downside to preventing unique symbol to symbol widening besides performance and compatibility concerns in [microsoft/TypeScript#55901](https://github.com/microsoft/TypeScript/issues/55901#issuecomment-5107506041)
    * @BhariGowda suggested verifying the PR’s gate coverage and adding a test case for the regex reuse scenario in [microsoft/TypeScript#63682](https://github.com/microsoft/TypeScript/issues/63682#issuecomment-5116907655)
    * @typescript-automation[bot] asked to review the build comparison results in [microsoft/TypeScript#63688](https://github.com/microsoft/TypeScript/pull/63688#issuecomment-5111330274)
    * @BhariGowda asked whether to keep the PR open or close it based on team preference in [microsoft/TypeScript#63690](https://github.com/microsoft/TypeScript/pull/63690#issuecomment-5119975473)
    * @BhariGowda asked whether to proceed here or wait for maintainer direction in [microsoft/TypeScript#63690](https://github.com/microsoft/TypeScript/pull/63690#issuecomment-5120058166)

## Activity Summary

### [Issue microsoft/TypeScript#55901](https://github.com/microsoft/TypeScript/issues/55901) (Open, `Suggestion`, `In Discussion`)

**unique symbol lost on assignment to const despite type assertion **

*Type assertion on a unique symbol assigned to const widens it to symbol rather than preserving its unique type.*

 * (2.8 years ago) **RyanCavanaugh** added labels `Suggestion`, `In Discussion`
 * [1.6 years ago](https://github.com/microsoft/TypeScript/issues/55901#issuecomment-2508042177) **luisfonsivevo** described encountering the bug frequently when using symbols as keys and illustrated it with a code sample
 * [today](https://github.com/microsoft/TypeScript/issues/55901#issuecomment-5107506041) **gershy-clutch** said "Is there a downside to preventing the unique symbol -> symbol widening, other than performance (and potential backwards compatibility concerns)?"

### [Issue microsoft/TypeScript#63679](https://github.com/microsoft/TypeScript/issues/63679) (Open, `Bug`, `Help Wanted`)

**Should not allow \`import\.defer?\.\('x'\)\`**

*Prevent optional chaining calls on import.defer so import.defer?.('x') is correctly rejected.*

 * (yesterday) **RyanCavanaugh** added labels `Bug`, `Help Wanted`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/63679#issuecomment-5112356051) **nightcityblade** said "Hi, I'd like to work on this. I'll submit a PR shortly."
 * [today](https://github.com/microsoft/TypeScript/issues/63679#issuecomment-5112374252) **nightcityblade** said "I need to step back from this one after reviewing the repository's maintenance-mode contribution guidance, so this issue is available for others."

### [Issue microsoft/TypeScript#63682](https://github.com/microsoft/TypeScript/issues/63682) (Open, `Bug`, `Help Wanted`)

**ES2025 regex syntax \(duplicate named groups, pattern modifiers\) is not gated by \`target\`**

*TypeScript does not enforce target-based errors for ES2025 regex features such as duplicate named groups and pattern modifiers.*

 * (yesterday) **RyanCavanaugh** added labels `Bug`, `Help Wanted`, and set milestone to `Backlog`
 * [later](https://github.com/microsoft/TypeScript/issues/63682#issuecomment-5116907655) **BhariGowda** described the root cause of the issue, endorsed the fix in #63689, suggested verifying the version gate covers both scanner-level and regex reuse paths, and recommended adding a test case for the specific regex reuse scenario to prevent regressions

### [Issue microsoft/TypeScript#63684](https://github.com/microsoft/TypeScript/issues/63684) (Closed)

**كود**

*Submitted issue titled 'كود' containing only a link to the TypeScript issue creation page.*

 * created by **503badrr**
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63685](https://github.com/microsoft/TypeScript/issues/63685) (Closed)

**JSDoc \`@type\` does not type a Promise in TypeScript Playground**

*JSDoc @type {Promise<number>} annotations in TypeScript Playground don’t infer the Promise’s resolved type, making .then callback argument unknown.*

 * created by **arka-prat-juno**
 * [today](https://github.com/microsoft/TypeScript/issues/63685#issuecomment-5103325944) **MartinJohns** reported inability to reproduce the issue after switching to JavaScript mode and removing TypeScript code, and noted that JSDoc typing does not work in TypeScript
 * [today](https://github.com/microsoft/TypeScript/issues/63685#issuecomment-5104862358) **jcalz** explained that the Playground file type must be set to JS instead of TS and provided a link
 * [today](https://github.com/microsoft/TypeScript/issues/63685#issuecomment-5113698421) **arka-prat-juno** said "oh oof, thanks"
 * (today) **arka-prat-juno** closed the issue

### [Issue microsoft/TypeScript#63686](https://github.com/microsoft/TypeScript/issues/63686) (Closed, `Question`)

**\`\!\` does not narrow discriminated unions when \`strict\` is \`false\`**

*Using !result.ok fails to narrow the discriminated union to the false branch when strict mode is disabled*

 * created by **LancesLance56**
 * [today](https://github.com/microsoft/TypeScript/issues/63686#issuecomment-5106772100) **MartinJohns** explained that with strictNullChecks disabled every type may be nullish, causing result.ok to be null and !result.ok to evaluate to true
 * [today](https://github.com/microsoft/TypeScript/issues/63686#issuecomment-5106782611) **jcalz** noted that the playground link did not reproduce the issue, demonstrated how disabling strictNullChecks allows undefined assignments leading to true !result.ok and potential runtime errors, and recommended keeping strictNullChecks enabled
 * **RyanCavanaugh** added label `Question`
 * (today) **LancesLance56** closed the issue

### [PR microsoft/TypeScript#63688](https://github.com/microsoft/TypeScript/pull/63688) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Remove see/link special casing entirely in TS files**

*Eliminate all special casing of see/link tags in TypeScript files to test the effect.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/63688#issuecomment-5110420222) **jakebailey** said "@typescript-bot test top999"
 * [today](https://github.com/microsoft/TypeScript/pull/63688#issuecomment-5110420906) **typescript-automation[bot]** started CI jobs and posted a status table with result links
 * [today](https://github.com/microsoft/TypeScript/pull/63688#issuecomment-5111330274) **typescript-automation[bot]** provided TypeScript build comparison results between main and the PR merge and noted unused variable errors in compiler-explorer and Effect-TS/effect

### [PR microsoft/TypeScript#63689](https://github.com/microsoft/TypeScript/pull/63689) (Closed, `For Backlog Bug`)

**Gate ES2025 regex syntax \(duplicate named groups, pattern modifiers\) behind target**

*Gate duplicate named capturing groups and regex pattern modifiers behind the ES2025 target with corresponding errors and tests.*

 * created by **sumukhl17-lgtm**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/63689#issuecomment-5116430017) **sumukhl17-lgtm** said "@microsoft-github-policy-service agree"
 * [later](https://github.com/microsoft/TypeScript/pull/63689#issuecomment-5118257043) **MartinJohns** said "@sumukhl17-lgtm You implemented the change in the wrong repository. See https://github.com/microsoft/TypeScript/blob/main/CONTRIBUTING.md"

### [PR microsoft/TypeScript#63690](https://github.com/microsoft/TypeScript/pull/63690) (Closed, `For Backlog Bug`)

**fix\(parser\): disallow optional chaining on import\.defer**

*Disallow optional chaining invocation on import.defer by emitting a TS18062 diagnostic*

 * created by **BhariGowda**
 * (later) **typescript-automation[bot]** added labels `For Backlog Bug`, `For Backlog Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/63690#issuecomment-5117653481) **BhariGowda** said "@microsoft-github-policy-service agree"
 * [later](https://github.com/microsoft/TypeScript/pull/63690#issuecomment-5118251663) **MartinJohns** said "@BhariGowda You implemented the change in the wrong repository. See: https://github.com/microsoft/TypeScript/blob/main/CONTRIBUTING.md"
 * [later](https://github.com/microsoft/TypeScript/pull/63690#issuecomment-5119975473) **BhariGowda** thanked for the heads up, filed microsoft/typescript-go#4789, and offered to port the fix there while deferring on PR status to the team's preference
 * (later) **BhariGowda** closed the issue
 * (later) **BhariGowda** reopened the issue
 * [later](https://github.com/microsoft/TypeScript/pull/63690#issuecomment-5120058166) **BhariGowda** reopened issue microsoft/typescript-go#4789, noted that a maintainer pointed to microsoft/TypeScript#63679 as the correct tracking location, and offered to proceed here or wait for guidance
 * [later](https://github.com/microsoft/TypeScript/pull/63690#issuecomment-5120170374) **MartinJohns** mentioned that issues are tracked here and pull requests should be made in the TypeScript-Go repository, noting TypeScript 7.0 is no longer written in TypeScript or JavaScript
 * [later](https://github.com/microsoft/TypeScript/pull/63690#issuecomment-5120194140) **BhariGowda** said "Understood, closing this and will submit the fix to microsoft/typescript-go. Thanks for the clarification!"
 * (later) **BhariGowda** closed the issue

