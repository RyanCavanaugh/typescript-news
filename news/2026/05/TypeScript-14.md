# Report for 2026-05-14 (Thursday, May 14th, 2026)

7 different users commented on 22 different issues.

## Recommended Actions

 * Response Recommended
    * @supernovus asked if a forked PR adding a 'serviceworker' lib definition would be merged in [microsoft/TypeScript#11781](https://github.com/microsoft/TypeScript/issues/11781#issuecomment-4454858857)
    * @spaceemotion asked whether the change in behavior between 5.x and 6.x was a limitation rather than a bug in [microsoft/TypeScript#63461](https://github.com/microsoft/TypeScript/issues/63461#issuecomment-4460049200)
    * @paoloricciuti asked why inference occurs before declaration and indicated it feels like a bug in [microsoft/TypeScript#63477](https://github.com/microsoft/TypeScript/issues/63477#issuecomment-4452751445)

## Activity Summary

### [Issue microsoft/TypeScript#11781](https://github.com/microsoft/TypeScript/issues/11781) (Open, `Suggestion`, `Help Wanted`, `Domain: lib.d.ts`)

**Service Worker typings**

*Include built-in Service Worker type definitions in TypeScript’s default library, matching existing community @types packages.*

 * [36 weeks ago](https://github.com/microsoft/TypeScript/issues/11781#issuecomment-3243343623) **eighty4** solved the issue with project references for scoping libraries and noted their limitation in bundler-built webapps requiring noEmit: false
 * [31 weeks ago](https://github.com/microsoft/TypeScript/issues/11781#issuecomment-3377075608) **FusillyCode** explained that previous solutions broke Firefox compatibility and provided a workaround using skipLibCheck and custom ServiceWorkerGlobalScope casting
 * [5 weeks ago](https://github.com/microsoft/TypeScript/issues/11781#issuecomment-4199635479) **vadimmos** said "Is there any progress on this issue? Are developers still doomed to write ServiceWorker code with one eye on the documentation, without the ability to rely on autocompletion and type checking tools?"
 * [today](https://github.com/microsoft/TypeScript/issues/11781#issuecomment-4454858857) **supernovus** noted that Service Worker support in TypeScript remained unaddressed and asked if a forked PR adding a 'serviceworker' lib would be merged

### [Issue microsoft/TypeScript#36772](https://github.com/microsoft/TypeScript/issues/36772) (Open, `Bug`, `Domain: check: Control Flow`, `Fix Available`, `Rescheduled`)

**Type not narrowed by === when equivalent type guard works**

*TypeScript fails to narrow a generic type parameter using a direct `=== 'a'` comparison, unlike a custom type guard.*

 * (1.7 years ago) **RyanCavanaugh** added label `Domain: Control Flow`, set milestone to `TypeScript 5.7.0`, and removed from milestone `TypeScript 5.5.0`
 * (today) **RyanCavanaugh** set milestone to `Backlog`, removed from milestone `TypeScript 5.7.0`, and unassigned **ahejlsberg**
 * **typescript-bot** added label `Fix Available`

### [Issue microsoft/TypeScript#63461](https://github.com/microsoft/TypeScript/issues/63461) (Closed, `Design Limitation`)

**\[6\.x\] Getting'unassingable to type' when returning value from method that needs to infer generic from parameters**

*TypeScript 6.x fails to infer the generic type for mapTo, marking the 'label' literal as unassignable.*

 * **RyanCavanaugh** added label `Design Limitation`
 * [4 days ago](https://github.com/microsoft/TypeScript/issues/63461#issuecomment-4416972950) **typescript-bot** said "This issue has been marked as "Design Limitation" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (4 days ago) **typescript-bot** closed the issue
 * [later](https://github.com/microsoft/TypeScript/issues/63461#issuecomment-4460049200) **spaceemotion** asked whether the behavior change between versions 5.x and 6.x was a limitation rather than a bug

### [PR microsoft/TypeScript#63471](https://github.com/microsoft/TypeScript/pull/63471) (Closed, `For Backlog Bug`)

**Clarify charCodeAt and codePointAt documentation**

*Revise JSDoc for charCodeAt to specify UTF-16 code units and for codePointAt to mention Unicode code points.*

 * **typescript-bot** added label `For Backlog Bug`
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/63471#issuecomment-4425528242) **jakebailey** asked how the bug was determined to be worth fixing given the contributing guidelines and asked what tool was used to send the PR
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/63471#issuecomment-4425606887) **MukundaKatta** said "I used VS Code with GitHub Copilot assistance for drafting/editing, but I reviewed and prepared the final change manually before submitting the PR."
 * [today](https://github.com/microsoft/TypeScript/pull/63471#issuecomment-4454425049) **RyanCavanaugh** said "Closing because this PR doesn't pass CI. Please correctly test locally before pushing PRs."
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#63475](https://github.com/microsoft/TypeScript/pull/63475) (Closed, `For Uncommitted Bug`)

**Fix minor typos in protocol\.ts **

*Correct spelling errors in protocol.ts JSDoc comments without affecting runtime behavior*

 * (today) **typescript-bot** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63475#issuecomment-4448613123) **typescript-bot** thanked the author for the PR, cautioned to preserve TSServer API compatibility, and pinged reviewers for extra review
 * [today](https://github.com/microsoft/TypeScript/pull/63475#issuecomment-4454413159) **RyanCavanaugh** said "This doesn't meet the 6.0 patch bar. See https://github.com/microsoft/TypeScript/issues/62963#issuecomment-4100336368"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63476](https://github.com/microsoft/TypeScript/issues/63476) (Open, `Duplicate`)

**\`===\` is not strong enough to narrow equal values to the same type**

*TypeScript's strict equality check doesn't narrow an unknown input to a specific string literal union type.*

 * created by **danon**
 * [today](https://github.com/microsoft/TypeScript/issues/63476#issuecomment-4449294554) **Hamzaa6296** reproduced the issue, proposed updating the type narrowing logic for === between unknown and a generic type T, and asked if the team would accept a PR
 * [today](https://github.com/microsoft/TypeScript/issues/63476#issuecomment-4451293547) **jcalz** marked the issue as a duplicate of #36772
 * [today](https://github.com/microsoft/TypeScript/issues/63476#issuecomment-4452487438) **RyanCavanaugh** provided an automated analysis listing similar issues for potential duplication
 * **RyanCavanaugh** added label `Duplicate`
 * [later](https://github.com/microsoft/TypeScript/issues/63476#issuecomment-4458703337) **khalil-mhiri-cyber** said "I can work on this issue if you need"

### [Issue microsoft/TypeScript#63477](https://github.com/microsoft/TypeScript/issues/63477) (Open, `Duplicate`)

**\`NoInfer\` on second generic parameter doesn't pick up inference from sibling methods**

*Using NoInfer on the second generic parameter prevents B from being inferred from the b() return type, defaulting to object.*

 * created by **paoloricciuti**
 * [today](https://github.com/microsoft/TypeScript/issues/63477#issuecomment-4452487606) **RyanCavanaugh** provided an automated response listing similar issues and suggesting the behavior might be intended
 * [today](https://github.com/microsoft/TypeScript/issues/63477#issuecomment-4452551414) **jcalz** questioned NoInfer relevance, explained that this is issue #47599, and provided a code example and playground link illustrating the supported inference per #48538
 * [today](https://github.com/microsoft/TypeScript/issues/63477#issuecomment-4452751445) **paoloricciuti** questioned why it could infer `a()` before its declaration and suggested it might be a bug
 * [today](https://github.com/microsoft/TypeScript/issues/63477#issuecomment-4453104326) **jcalz** said "Because a() isn't context-sensitive.  It has no parameters to infer. Please read #47599 and #48538 "
 * **RyanCavanaugh** added label `Duplicate`

### [PR microsoft/TypeScript#63478](https://github.com/microsoft/TypeScript/pull/63478) (Closed, `For Uncommitted Bug`)

**Refine label diagnostics for unresolved targets**

*Refine labeled break/continue diagnostics to report missing labels, invalid targets, and preserve existing forward-reference diagnostics.*

 * created by **MukundaKatta**
 * **typescript-bot** added label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/63478#issuecomment-4460376867) **RyanCavanaugh** said "This does not meet the 6.0 patch bar. See https://github.com/microsoft/TypeScript/issues/62963#issuecomment-4100336368"
 * (later) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#63479](https://github.com/microsoft/TypeScript/pull/63479) (Open, `For Milestone Bug`)

**fix: correct diagnostic code 6910**

*Correct diagnostic code for the module option message from 69010 to 6910 for proper sequential ordering.*

 * created by **MukundaKatta**
 * **typescript-bot** added label `For Milestone Bug`

