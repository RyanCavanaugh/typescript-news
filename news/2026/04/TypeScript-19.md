# Report for 2026-04-19 (Sunday, April 19th, 2026)

7 different users commented on 9 different issues.

## Recommended Actions

 * Response Recommended
    * @XeroAlpha asked if supporting `export import type thing = foo;` would be a better solution in [microsoft/TypeScript#54855](https://github.com/microsoft/TypeScript/issues/54855#issuecomment-4280787116)

## Activity Summary

### [Issue microsoft/TypeScript#45869](https://github.com/microsoft/TypeScript/issues/45869) (Closed, `Suggestion`, `Declined`)

**Capture type of Promises that never reject**

*Add a type-level mechanism in TypeScript to represent Promises that always resolve and never reject.*

 * [3.3 years ago](https://github.com/microsoft/TypeScript/issues/45869#issuecomment-1344744686) **jamesarosen** described that centralizing a Promise’s never type avoids repeated eslint-ignore comments
 * [3.3 years ago](https://github.com/microsoft/TypeScript/issues/45869#issuecomment-1344799559) **andrewbranch** said "Centralized solution: disable the eslint rule 😄 "
 * [2.2 years ago](https://github.com/microsoft/TypeScript/issues/45869#issuecomment-1875271772) **aovchinn** described a Promise.allSettled scenario with always-resolving promises and suggested marking async functions with handled errors
 * [later](https://github.com/microsoft/TypeScript/issues/45869#issuecomment-4278748673) **nickshanks** described a use case with a try/catch only async function that always resolves and provided a no-op async example

### [Issue microsoft/TypeScript#54855](https://github.com/microsoft/TypeScript/issues/54855) (Open, `Bug`, `Help Wanted`, `Domain: ES Modules`)

**TS:1379 An import alias cannot reference a declaration that was exported using 'export type'**

*Importing a type alias exported using 'export type' triggers TS1379 errors, unlike untyped exports*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [1 year ago](https://github.com/microsoft/TypeScript/issues/54855#issuecomment-2709465995) **zimtsui** said "Since you have imported * as core, just make a normal definition type thing = core.foo; "
 * **RyanCavanaugh** added label `Domain: ES Modules`
 * [later](https://github.com/microsoft/TypeScript/issues/54855#issuecomment-4280787116) **XeroAlpha** proposed supporting `export import type thing = foo` as a better solution for exporting types in namespaces

### [PR microsoft/TypeScript#63396](https://github.com/microsoft/TypeScript/pull/63396) (Closed, `For Uncommitted Bug`, `dependencies`, `github_actions`)

**Bump the github\-actions group with 2 updates**

*Update GitHub Actions group by bumping actions/upload-artifact to v7.0.1 and actions/github-script.*

 * (1 week ago) **dependabot[bot]** added labels `dependencies`, `github_actions`
 * **typescript-bot** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63396#issuecomment-4277250352) **dependabot[bot]** said "Looks like these dependencies are updatable in another way, so this is no longer needed."
 * (today) **dependabot[bot]** closed the issue

### [PR microsoft/TypeScript#63413](https://github.com/microsoft/TypeScript/pull/63413) (Closed, `For Uncommitted Bug`)

**Improve error message for invalid continue target label**

*Update TypeScript compiler to provide a clearer error message when a continue statement targets a label outside an enclosing loop or switch scope.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/63413#issuecomment-4274600471) **jakebailey** said "How specifically did you choose this issue to fix"
 * [yesterday](https://github.com/microsoft/TypeScript/pull/63413#issuecomment-4274730145) **Jah-yee** described selecting issue #30408 due to its clear scope, long-standing status, straightforward fix, and potential developer benefit, and offered further elaboration
 * [yesterday](https://github.com/microsoft/TypeScript/pull/63413#issuecomment-4274813098) **jakebailey** said "Yes, why didn't you read the first thing in the contributing guide?"
 * (today) **Jah-yee** closed the issue

### [PR microsoft/TypeScript#63415](https://github.com/microsoft/TypeScript/pull/63415) (Open, `Author: Team`, `For Uncommitted Bug`, **ahejlsberg**)

**Improve tracking of deeply nested object types**

*Experimentally enhance tracking support for deeply nested object types to improve type analysis accuracy.*

 * [today](https://github.com/microsoft/TypeScript/pull/63415#issuecomment-4275889322) **typescript-bot** reported DT test results with branch-only errors for lodash
 * [today](https://github.com/microsoft/TypeScript/pull/63415#issuecomment-4275903902) **typescript-bot** provided test results comparing main and the pull request merge, noting an infrastructure failure and a new type error
 * [today](https://github.com/microsoft/TypeScript/pull/63415#issuecomment-4275990984) **typescript-bot** reported compilation errors when comparing tsc results on main and PR merge for top 400 repos, highlighting issues in amruthpillai/reactive-resume and github/docs
 * [today](https://github.com/microsoft/TypeScript/pull/63415#issuecomment-4276414638) **ahejlsberg** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/63415#issuecomment-4276414738) **typescript-bot** posted CI build status updates for test top400, user test this, run dt, and perf test this faster
 * [today](https://github.com/microsoft/TypeScript/pull/63415#issuecomment-4276452287) **typescript-bot** reported that DT tests results were ready and unchanged and shared the build log link
 * [today](https://github.com/microsoft/TypeScript/pull/63415#issuecomment-4276463911) **typescript-bot** reported that user tests showed one Git clone failure but otherwise everything looked good
 * [today](https://github.com/microsoft/TypeScript/pull/63415#issuecomment-4276532262) **typescript-bot** provided the requested performance run results in a detailed comparison report
 * [today](https://github.com/microsoft/TypeScript/pull/63415#issuecomment-4276548556) **typescript-bot** reported type checking errors when comparing main and pull/63415 merge across top 400 repositories and highlighted errors in amruthpillai/reactive-resume
 * [today](https://github.com/microsoft/TypeScript/pull/63415#issuecomment-4276548577) **typescript-bot** reported build failures in immich-app/immich from running the top 400 repos suite
 * [today](https://github.com/microsoft/TypeScript/pull/63415#issuecomment-4276938814) **ahejlsberg** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/63415#issuecomment-4276938914) **typescript-bot** posted CI build status updates
 * [today](https://github.com/microsoft/TypeScript/pull/63415#issuecomment-4276987543) **typescript-bot** reported that DT test results were ready and unchanged and provided a log link
 * [today](https://github.com/microsoft/TypeScript/pull/63415#issuecomment-4276998842) **typescript-bot** reported that user tests showed one Git clone failure but otherwise everything looked good
 * [today](https://github.com/microsoft/TypeScript/pull/63415#issuecomment-4277062057) **typescript-bot** reported the performance run results requested by @ahejlsberg
 * [today](https://github.com/microsoft/TypeScript/pull/63415#issuecomment-4277078148) **typescript-bot** reported type checking errors when comparing main and pull/63415 merge across top 400 repositories and highlighted errors in amruthpillai/reactive-resume

### [Issue microsoft/TypeScript#63416](https://github.com/microsoft/TypeScript/issues/63416) (Open)

**JSDoc parser treats \`@foo\` inside fenced code blocks as a tag, breaking hover previews**

*JSDoc parser does not respect fenced code blocks and incorrectly treats @tags inside them as JSDoc tags, breaking hover documentation previews.*

 * created by **BojanRatkovic**
 * [today](https://github.com/microsoft/TypeScript/issues/63416#issuecomment-4276891516) **MartinJohns** said "Duplicate of #58992."

### [PR microsoft/TypeScript#63417](https://github.com/microsoft/TypeScript/pull/63417) (Open, `For Uncommitted Bug`, `dependencies`, `github_actions`)

**Bump the github\-actions group across 1 directory with 4 updates**

*Upgrade four GitHub Actions dependencies (upload-artifact, cache, codeql-action, and github-script) to their latest versions in the root directory.*

 * created by **dependabot[bot]**
 * (today) **dependabot[bot]** added labels `dependencies`, `github_actions`, `dependencies`, `github_actions`
 * **typescript-bot** added label `For Uncommitted Bug`

