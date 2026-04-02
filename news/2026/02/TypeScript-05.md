# Report for 2026-02-05 (Thursday, February 5th, 2026)

8 different users commented on 19 different issues.

## Activity Summary

### [Issue microsoft/TypeScript#52460](https://github.com/microsoft/TypeScript/issues/52460) (Closed, `Suggestion`, `Help Wanted`, `Domain: LS: Completion Lists`)

**Path completions for Node\.js subpath imports**

*Path completions for Node.js subpath imports*

 * [47 weeks ago](https://github.com/microsoft/TypeScript/issues/52460#issuecomment-2712953072) **Andarist** said "You could create a repro case and open a new issue about this. It's hard to investigate this given the incomplete provided information."
 * [47 weeks ago](https://github.com/microsoft/TypeScript/issues/52460#issuecomment-2713026866) **mbrevda** said "Please link to the issue from here so that we can follow along"
 * [44 weeks ago](https://github.com/microsoft/TypeScript/issues/52460#issuecomment-2764179306) **anthonyma94** said "@Andarist @mbrevda sorry for the late response, created a new issue #61504."
 * (today) **DanielRosenwasser** set milestone to `TypeScript 5.9.0`, and removed from milestone `Backlog`

### [PR microsoft/TypeScript#59567](https://github.com/microsoft/TypeScript/pull/59567) (Open, `For Backlog Bug`)

**Use numeric literals for BYTES\_PER\_ELEMENT**

*Replace computed BYTES_PER_ELEMENT properties in TypeScript library definitions with explicit numeric literals*

 * [1.5 years ago](https://github.com/microsoft/TypeScript/pull/59567#issuecomment-2277083744) **typescript-bot** reported that user tests passed when comparing main and the pull request merge; everything looked good
 * [1.5 years ago](https://github.com/microsoft/TypeScript/pull/59567#issuecomment-2277088921) **typescript-bot** provided the requested perf run results
 * [1.5 years ago](https://github.com/microsoft/TypeScript/pull/59567#issuecomment-2277153585) **typescript-bot** ran tests on the top 400 repos with tsc and confirmed everything looked good
 * [today](https://github.com/microsoft/TypeScript/pull/59567#issuecomment-3858222349) **jakebailey** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/59567#issuecomment-3858222577) **typescript-bot** posted build status updates for various test jobs
 * [today](https://github.com/microsoft/TypeScript/pull/59567#issuecomment-3858289260) **typescript-bot** reported DT test results were ready and unchanged
 * [today](https://github.com/microsoft/TypeScript/pull/59567#issuecomment-3858310930) **typescript-bot** reported user test results, noted an infrastructure failure, and confirmed everything looked good
 * [today](https://github.com/microsoft/TypeScript/pull/59567#issuecomment-3858434351) **typescript-bot** provided the requested performance run results
 * [today](https://github.com/microsoft/TypeScript/pull/59567#issuecomment-3858504956) **typescript-bot** ran tests on the top 400 repos with tsc and confirmed everything looked good

### [PR microsoft/TypeScript#60656](https://github.com/microsoft/TypeScript/pull/60656) (Closed, `For Backlog Bug`)

**Implement Intl Locale Info proposal**

*Implement support for the Intl.LocaleInfo proposal by adding locale metadata APIs to TypeScript.*

 * created by **printfn**
 * **typescript-bot** added label `For Backlog Bug`
 * [1 year ago](https://github.com/microsoft/TypeScript/pull/60656#issuecomment-2596633257) **erlandsona** reported encountering the same issue when updating TypeScript and expressed support for the update
 * (today) **jakebailey** closed the issue
 * (today) **jakebailey** reopened the issue

### [PR microsoft/TypeScript#61628](https://github.com/microsoft/TypeScript/pull/61628) (Closed, `For Uncommitted Bug`)

**chore: \`string\` type also allows as args in Intl\.NumberFormat\.format**

*Update the Intl.NumberFormat.format type definition to accept string arguments per MDN documentation.*

 * created by **hengistchan**
 * **typescript-bot** added label `For Uncommitted Bug`
 * [40 weeks ago](https://github.com/microsoft/TypeScript/pull/61628#issuecomment-2837850994) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#61817](https://github.com/microsoft/TypeScript/pull/61817) (Open, `For Uncommitted Bug`)

**lib: narrow \`Atomics\.wait\*\` target to SharedArrayBuffer views**

*Restrict Atomics.wait* methods to only accept views over SharedArrayBuffer in their declarations*

 * [35 weeks ago](https://github.com/microsoft/TypeScript/pull/61817#issuecomment-2941989528) **typescript-bot** reported that user tests passed when comparing main to the pull request merge
 * [35 weeks ago](https://github.com/microsoft/TypeScript/pull/61817#issuecomment-2942079290) **typescript-bot** provided requested perf run results to @jakebailey
 * [35 weeks ago](https://github.com/microsoft/TypeScript/pull/61817#issuecomment-2942377886) **typescript-bot** reported that running tsc on the top 400 repos comparing main and the PR merge showed everything looked good
 * (today) **jakebailey** closed the issue
 * (today) **jakebailey** reopened the issue
 * [today](https://github.com/microsoft/TypeScript/pull/61817#issuecomment-3858246585) **jakebailey** said "Failed to look at this properly until now. I am shocked this isn't super breaky?"
 * [today](https://github.com/microsoft/TypeScript/pull/61817#issuecomment-3858318964) **Renegade334** said "I guess the shared view is often going to appear in a context where its type is inferred, rather than annotated? But yes, somewhat surprising"

### [PR microsoft/TypeScript#62013](https://github.com/microsoft/TypeScript/pull/62013) (Closed, `For Backlog Bug`, **RyanCavanaugh**, **Copilot**)

**Add approximatelySign to NumberFormatRangePartTypeRegistry for ES2023**

*Add approximatelySign as a range-only part type in the ES2023 NumberFormatRangePartTypeRegistry to support Intl.NumberFormat.formatRangeToParts.*

 * (30 weeks ago) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * **typescript-bot** added label `For Milestone Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/62013#issuecomment-3858175139) **jakebailey** said "@copilot merge main and address the comments"
 * (today) **typescript-bot** added label `For Uncommitted Bug`, and removed label `For Milestone Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/62013#issuecomment-3858191835) **Copilot** merged main and fixed eslint issues from the merge conflict in harnessGlobals.ts
 * [today](https://github.com/microsoft/TypeScript/pull/62013#issuecomment-3858216882) **jakebailey** said "@copilot Undo those eslint changes, which are wrong, then address Renegade334's comment above."
 * [today](https://github.com/microsoft/TypeScript/pull/62013#issuecomment-3858233318) **Copilot** reverted incorrect eslint changes and updated the test to assign the result to a variable, passing linting and formatting
 * [today](https://github.com/microsoft/TypeScript/pull/62013#issuecomment-3858241101) **jakebailey** asked Copilot to try the comment
 * [today](https://github.com/microsoft/TypeScript/pull/62013#issuecomment-3858253685) **Copilot** created NumberFormatRangePartTypeRegistry, moved approximatelySign there, and updated NumberRangeFormatPart to use NumberFormatRangePartTypes
 * (today) **typescript-bot** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`

### [PR microsoft/TypeScript#62628](https://github.com/microsoft/TypeScript/pull/62628) (Closed, `For Uncommitted Bug`, **RyanCavanaugh**)

**Add lib\.esnext\.temporal**

*Adds ESNext Temporal library definitions to TypeScript with spec-compliant property constraints but without custom calendar support.*

 * [8 weeks ago](https://github.com/microsoft/TypeScript/pull/62628#issuecomment-3629347917) **jakebailey** said "I know there are existing polyfills for Temporal out there in TS; are these types compatible / based off of those? Or fresh?"
 * [8 weeks ago](https://github.com/microsoft/TypeScript/pull/62628#issuecomment-3629743678) **Renegade334** noted that definitions were de novo with no licensing issues and observed that temporal-polyfill and @js-temporal/polyfill were incompatible with lib.d.ts patterns, offering to run interoperability tests
 * [yesterday](https://github.com/microsoft/TypeScript/pull/62628#issuecomment-3850515921) **jakebailey** mentioned reviewing the PR and noted that MDN hasn't updated to reflect the removal of custom calendar support per the latest spec changes
 * [today](https://github.com/microsoft/TypeScript/pull/62628#issuecomment-3857186615) **jakebailey** said "One thing this PR is missing are updates to getScriptTargetFeatures, though not strictly required to compile."

### [PR microsoft/TypeScript#62726](https://github.com/microsoft/TypeScript/pull/62726) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Always set up host in node builder**

*Configure the node builder to always initialize the host environment during setup.*

 * [13 weeks ago](https://github.com/microsoft/TypeScript/pull/62726#issuecomment-3498745668) **typescript-bot** reported test results comparing main and PR merge, noting a git clone failure but otherwise success
 * [13 weeks ago](https://github.com/microsoft/TypeScript/pull/62726#issuecomment-3498857332) **typescript-bot** provided the requested performance run results
 * [13 weeks ago](https://github.com/microsoft/TypeScript/pull/62726#issuecomment-3499002808) **typescript-bot** reported that running tsc on the top 400 repos comparing main and the pull request resulted in no issues
 * [today](https://github.com/microsoft/TypeScript/pull/62726#issuecomment-3855790102) **jakebailey** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/62726#issuecomment-3855790421) **typescript-bot** reported started and completed statuses for test top400, user test this, run dt, and perf test this faster jobs
 * [today](https://github.com/microsoft/TypeScript/pull/62726#issuecomment-3855890078) **typescript-bot** reported that DT test results were ready and unchanged
 * [today](https://github.com/microsoft/TypeScript/pull/62726#issuecomment-3855925877) **typescript-bot** reported test results comparing main and PR merge, noting a git clone failure but otherwise success
 * [today](https://github.com/microsoft/TypeScript/pull/62726#issuecomment-3856039129) **typescript-bot** posted the requested perf run results for tsc
 * [today](https://github.com/microsoft/TypeScript/pull/62726#issuecomment-3856141405) **typescript-bot** reported that running tsc on the top 400 repos comparing main and the pull request resulted in no issues

### [PR microsoft/TypeScript#63046](https://github.com/microsoft/TypeScript/pull/63046) (Closed, `For Backlog Bug`)

**Introduce ES2025 target & Add missing ScriptTargetFeatures**

*Introduce ES2025 compilation target and add missing type definitions for RegExp.escape and Intl.DurationFormat in TypeScript.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/63046#issuecomment-3849354757) **typescript-bot** notified that the DT test results were ready and unchanged
 * [yesterday](https://github.com/microsoft/TypeScript/pull/63046#issuecomment-3849509461) **typescript-bot** provided the requested performance run results
 * [yesterday](https://github.com/microsoft/TypeScript/pull/63046#issuecomment-3849594738) **typescript-bot** provided results of running the top 400 repos with tsc comparing main and PR merge and noted everything looked good
 * [today](https://github.com/microsoft/TypeScript/pull/63046#issuecomment-3857405210) **jakebailey** said "This PR is missing an update to getDefaultLibFileName, which for some reason is a switch case that hardcodes accessing a map of the same keys. That explains the strange lib.d.ts baseline diffs."
 * [today](https://github.com/microsoft/TypeScript/pull/63046#issuecomment-3857495528) **jakebailey** said "I am actually quite confused why these intl changes are in ES2025. Doesn't https://github.com/tc39/proposal-intl-duration-format imply they are ES2024?"
 * [today](https://github.com/microsoft/TypeScript/pull/63046#issuecomment-3858035232) **jakebailey** said "I think I'm just wrong; it's in https://tc39.es/ecma402/2025/ but not https://tc39.es/ecma402/2024/."
 * [today](https://github.com/microsoft/TypeScript/pull/63046#issuecomment-3858172511) **jakebailey** said "I realize I dumped a bunch of changes onto you; if you are too busy, I'm happy to just push the intl changes to the PR directly."
 * [today](https://github.com/microsoft/TypeScript/pull/63046#issuecomment-3858449556) **petamoriken** explained writing the type inline within DurationFormatOptions might make the changes harder to review and apologized for the inconvenience
 * [today](https://github.com/microsoft/TypeScript/pull/63046#issuecomment-3858489090) **petamoriken** offered to have the intl changes pushed directly to the PR if the release timing requires it
 * [later](https://github.com/microsoft/TypeScript/pull/63046#issuecomment-3858774558) **petamoriken** described that in es2023.intl.d.ts and es2022.intl.d.ts types are defined inline within options interfaces, while in es2020.intl.d.ts types like RelativeTimeFormatUnit and RelativeTimeFormatUnitSingular are explicitly defined

### [Issue microsoft/TypeScript#63061](https://github.com/microsoft/TypeScript/issues/63061) (Closed, `Not a Defect`)

**\`export type\` vs \`export { type }\` with augmentations**

*export { type } re-exports do not allow module augmentations to access types, unlike export type*

 * [1 week ago](https://github.com/microsoft/TypeScript/issues/63061#issuecomment-3817254000) **mkantor** said "I just tested typescript-go and the behavior is the same there (perhaps this issue should be filed in that repository; see #62827)."
 * **RyanCavanaugh** added label `Not a Defect`
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63061#issuecomment-3842786736) **RyanCavanaugh** explained reasons for allowing a local type to be exported by name without reuse and that module rules include only the lexical scope of explicitly exported names, consistent with file-level behavior
 * [today](https://github.com/microsoft/TypeScript/issues/63061#issuecomment-3857354651) **typescript-bot** said "This issue has been marked as "Not a Defect" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-bot** closed the issue

### [Issue microsoft/TypeScript#63106](https://github.com/microsoft/TypeScript/issues/63106) (Closed)

**\[High\] Memory Leak in TypeScript**

*Unclosed resource connections in src/TypeScript.ts cause a high-severity memory leak that could crash the service.*

 * created by **admin1douyin**
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63107](https://github.com/microsoft/TypeScript/issues/63107) (Closed)

**\[Medium\] Race Condition in TypeScript**

*A medium-severity race condition in src/TypeScript.js can cause data inconsistencies due to unsynchronized concurrent access to shared variables.*

 * created by **admin1douyin**
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#63108](https://github.com/microsoft/TypeScript/pull/63108) (Open, `For Uncommitted Bug`)

**Fix crash in CFA when for loop initializer throws**

*Control flow analysis crashes when a for loop initializer throws an exception.*

 * created by **Andarist**
 * **typescript-bot** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63108#issuecomment-3858293045) **DanielRosenwasser** said "@tyepscript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/63108#issuecomment-3858300639) **DanielRosenwasser** expressed confusion and posted a link to the TypeScript Bot trigger wiki and a screenshot
 * [today](https://github.com/microsoft/TypeScript/pull/63108#issuecomment-3858301092) **DanielRosenwasser** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/63108#issuecomment-3858301318) **typescript-bot** posted an automated build status update summarizing job commands, statuses, and result links
 * [today](https://github.com/microsoft/TypeScript/pull/63108#issuecomment-3858403817) **typescript-bot** notified that the DT test results were ready and unchanged
 * [today](https://github.com/microsoft/TypeScript/pull/63108#issuecomment-3858426880) **typescript-bot** reported user test results comparing main to the pull request merge, noted one unrelated infrastructure failure, and confirmed everything else looked good
 * [today](https://github.com/microsoft/TypeScript/pull/63108#issuecomment-3858531344) **typescript-bot** posted perf run results for the requested test
 * [today](https://github.com/microsoft/TypeScript/pull/63108#issuecomment-3858649478) **typescript-bot** reported test results for the top 400 repos comparing main and the PR merge and confirmed everything looked good

