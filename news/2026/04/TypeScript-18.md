# Report for 2026-04-18 (Saturday, April 18th, 2026)

5 different users commented on 3 different issues.

## Recommended Actions

 * Response Recommended
    * @OldStarchy asked why the inaccurate legacy decorator types are kept despite not reflecting the compiler implementation in [microsoft/TypeScript#63346](https://github.com/microsoft/TypeScript/issues/63346#issuecomment-4275256298)
    * @Jah-yee asked if any additional changes were needed in [microsoft/TypeScript#63413](https://github.com/microsoft/TypeScript/pull/63413#issuecomment-4274563771)

## Activity Summary

### [Issue microsoft/TypeScript#63346](https://github.com/microsoft/TypeScript/issues/63346) (Closed, `Question`)

**Experimental \(deprecated\) decorators are included by default**

*The ESNext library includes legacy experimental decorator types by default, causing conflicts with new decorator definitions.*

 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63346#issuecomment-4257328096) **OldStarchy** clarified that '*.d.ts' files are included globally without imports and that adding an export does not address the default inclusion of legacy decorators, and pointed out the specific type name conflict
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63346#issuecomment-4257346566) **OldStarchy** identified issue 29828 as the closest match and suggested removing types instead of fixing, noting that replacing legacy decorator types could invert the problem for projects relying on the legacy syntax
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63346#issuecomment-4261818948) **RyanCavanaugh** explained that a global type-name invariant doesn't exist and recommended exporting types in modules to avoid conflicts
 * [today](https://github.com/microsoft/TypeScript/issues/63346#issuecomment-4275256298) **OldStarchy** questioned the accuracy of legacy decorator types and argued they prevented defining correct ambient decorator types

### [PR microsoft/TypeScript#63413](https://github.com/microsoft/TypeScript/pull/63413) (Closed, `For Uncommitted Bug`)

**Improve error message for invalid continue target label**

*Update TypeScript compiler to provide a clearer error message when a continue statement targets a label outside an enclosing loop or switch scope.*

 * (today) **Jah-yee** reopened the issue
 * [today](https://github.com/microsoft/TypeScript/pull/63413#issuecomment-4273656495) **Jah-yee** thanked for feedback and explained that the PR addressed issue #30408 by improving the diagnostic error message
 * [today](https://github.com/microsoft/TypeScript/pull/63413#issuecomment-4273921308) **jakebailey** asked to disclaim what tool was used to send the PR
 * [today](https://github.com/microsoft/TypeScript/pull/63413#issuecomment-4274563771) **Jah-yee** thanked the reviewers, disclosed AI assistance by OpenClaw, explained that the agent helped implement the diagnostic message improvement for issue #30408, confirmed author review of changes, described how the PR addresses the confusing continue statement error, and asked if any additional changes were needed
 * [today](https://github.com/microsoft/TypeScript/pull/63413#issuecomment-4274600471) **jakebailey** said "How specifically did you choose this issue to fix"
 * [today](https://github.com/microsoft/TypeScript/pull/63413#issuecomment-4274730145) **Jah-yee** described selecting issue #30408 due to its clear scope, long-standing status, straightforward fix, and potential developer benefit, and offered further elaboration
 * [today](https://github.com/microsoft/TypeScript/pull/63413#issuecomment-4274813098) **jakebailey** said "Yes, why didn't you read the first thing in the contributing guide?"

### [PR microsoft/TypeScript#63415](https://github.com/microsoft/TypeScript/pull/63415) (Open, `Author: Team`, `For Uncommitted Bug`, **ahejlsberg**)

**Improve tracking of deeply nested object types**

*Experimentally enhance tracking support for deeply nested object types to improve type analysis accuracy.*

 * created by **ahejlsberg**
 * (today) **typescript-bot** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript/pull/63415#issuecomment-4274699260) **typescript-bot** advised to document breaking changes on the wiki and notify DanielRosenwasser and RyanCavanaugh
 * [today](https://github.com/microsoft/TypeScript/pull/63415#issuecomment-4274699403) **ahejlsberg** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/63415#issuecomment-4274699495) **typescript-bot** started CI jobs for 'test top400', 'user test this', 'run dt', and 'perf test this faster', reporting that the last test failed
 * [today](https://github.com/microsoft/TypeScript/pull/63415#issuecomment-4274713554) **ahejlsberg** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/63415#issuecomment-4274713633) **typescript-bot** reported CI job starts and provided status and result links
 * [today](https://github.com/microsoft/TypeScript/pull/63415#issuecomment-4274718529) **typescript-bot** said "@ahejlsberg, the perf run you requested failed. You can check the log here."
 * [today](https://github.com/microsoft/TypeScript/pull/63415#issuecomment-4274729038) **typescript-bot** reported DT test results with branch-only errors for lodash
 * [today](https://github.com/microsoft/TypeScript/pull/63415#issuecomment-4274737318) **typescript-bot** said "@ahejlsberg, the perf run you requested failed. You can check the log here."
 * [today](https://github.com/microsoft/TypeScript/pull/63415#issuecomment-4274742394) **typescript-bot** provided test results comparing main and the pull request merge, noting an infrastructure failure and a new type error
 * [today](https://github.com/microsoft/TypeScript/pull/63415#issuecomment-4274755826) **typescript-bot** reported DT test results with branch-only errors for lodash
 * [today](https://github.com/microsoft/TypeScript/pull/63415#issuecomment-4274762058) **typescript-bot** provided test results comparing main and the pull request merge, noting an infrastructure failure and a new type error
 * [today](https://github.com/microsoft/TypeScript/pull/63415#issuecomment-4274803110) **typescript-bot** reported compilation errors when comparing tsc results on main and PR merge for top 400 repos, highlighting issues in amruthpillai/reactive-resume and github/docs
 * [today](https://github.com/microsoft/TypeScript/pull/63415#issuecomment-4274834263) **typescript-bot** reported compilation errors when comparing tsc results on main and PR merge for top 400 repos, highlighting issues in amruthpillai/reactive-resume and github/docs
 * [later](https://github.com/microsoft/TypeScript/pull/63415#issuecomment-4275852356) **ahejlsberg** said "@typescript-bot test it"
 * [later](https://github.com/microsoft/TypeScript/pull/63415#issuecomment-4275852472) **typescript-bot** posted CI job status updates for test commands with links to build results
 * [later](https://github.com/microsoft/TypeScript/pull/63415#issuecomment-4275876491) **typescript-bot** said "@ahejlsberg, the perf run you requested failed. You can check the log here."
 * [later](https://github.com/microsoft/TypeScript/pull/63415#issuecomment-4275889322) **typescript-bot** reported DT test results with branch-only errors for lodash
 * [later](https://github.com/microsoft/TypeScript/pull/63415#issuecomment-4275903902) **typescript-bot** provided test results comparing main and the pull request merge, noting an infrastructure failure and a new type error
 * [later](https://github.com/microsoft/TypeScript/pull/63415#issuecomment-4275990984) **typescript-bot** reported compilation errors when comparing tsc results on main and PR merge for top 400 repos, highlighting issues in amruthpillai/reactive-resume and github/docs

