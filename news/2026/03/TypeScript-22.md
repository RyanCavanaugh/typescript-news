# Report for 2026-03-22 (Sunday, March 22nd, 2026)

9 different users commented on 15 different issues.

## Recommended Actions

 * Response Recommended
    * @TomStrepsil asked about whether this change will land in the next major version of TypeScript in [microsoft/TypeScript#61079](https://github.com/microsoft/TypeScript/pull/61079#issuecomment-4106726437)
    * @TomStrepsil provided a link to the newly opened issue in [microsoft/TypeScript#61079](https://github.com/microsoft/TypeScript/pull/61079#issuecomment-4106750870)
    * @AlejandroGispert offered to help fix the issue in [microsoft/TypeScript#63276](https://github.com/microsoft/TypeScript/issues/63276#issuecomment-4106954431)

## Activity Summary

### [PR microsoft/TypeScript#61079](https://github.com/microsoft/TypeScript/pull/61079) (Closed, `For Uncommitted Bug`)

**Fix RegExpIndicesArray by adding undefined to type definition**

*Update RegExpIndicesArray type definition to include undefined for unmatched capture groups.*

 * (6 weeks ago) **jakebailey** closed the issue
 * (6 weeks ago) **jakebailey** reopened the issue
 * (6 weeks ago) **jakebailey** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/61079#issuecomment-4106726437) **TomStrepsil** inquired about the change landing in the next major version and suggested extending the interface definition with an example demonstrating group indices behavior
 * [today](https://github.com/microsoft/TypeScript/pull/61079#issuecomment-4106742567) **stefnotch** asked TomStrepsil to open an issue for changing the type definition of the groups and suggested landing it in Typescript 6
 * [today](https://github.com/microsoft/TypeScript/pull/61079#issuecomment-4106750870) **TomStrepsil** opened a new issue for changing the type definition of `groups`

### [Issue microsoft/TypeScript#63085](https://github.com/microsoft/TypeScript/issues/63085) (Open, `Planning`)

**TypeScript 6\.0 Iteration Plan**

*The TypeScript 6.0 iteration plan details milestone dates and scheduled compiler additions, language improvements, breaking changes, and deprecations.*

 * [4 days ago](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-4087648587) **newives** asked if a specific release date was available
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-4094003838) **simonbuchan** joked about looking like a fool for promising the release on the 17th
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-4099966321) **RyanCavanaugh** said "We hit some issues when testing in Visual Studio, so 23 is the new 17"
 * [later](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-4111624942) **RyanCavanaugh** said "6.0.0 RC was already released, see https://devblogs.microsoft.com/typescript/announcing-typescript-6-0-rc/ or npm install typescript@rc"

### [PR microsoft/TypeScript#63255](https://github.com/microsoft/TypeScript/pull/63255) (Closed)

**fix\(compiler\): small improvement to error message handling**

*Update two comments in parser.ts to correct grammar in parseErrorForMissingSemicolonAfter documentation*

 * created by **Vikash9546**
 * [6 days ago](https://github.com/microsoft/TypeScript/pull/63255#issuecomment-4067366563) **MartinJohns** quoted the pull request template advising against submitting typo-only PRs
 * [yesterday](https://github.com/microsoft/TypeScript/pull/63255#issuecomment-4104515404) **niranjannnnn55-bot** described a PR that corrected minor typos in parseErrorForMissingSemicolonAfter documentation comments and noted that the build passed locally while tests failed with EMFILE errors unrelated to the change
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63264](https://github.com/microsoft/TypeScript/issues/63264) (Closed, `Duplicate`)

**Return statement required even when not needed**

*TypeScript incorrectly requires a return statement in an exhaustively covered function over a closed union, causing a missing return error.*

 * [4 days ago](https://github.com/microsoft/TypeScript/issues/63264#issuecomment-4081968705) **MartinJohns** said "Duplicate of #21985."
 * **RyanCavanaugh** added label `Duplicate`
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63264#issuecomment-4097300406) **Withered-Flower-0422** suggested writing testFunction with an ArgType union and throwing an error for invalid arguments
 * [today](https://github.com/microsoft/TypeScript/issues/63264#issuecomment-4107471867) **typescript-bot** said "This issue has been marked as "Duplicate" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-bot** closed the issue

### [Issue microsoft/TypeScript#63275](https://github.com/microsoft/TypeScript/issues/63275) (Closed, `Question`)

**TypeScript enum emit inconsistency**

*TypeScript 5.x now emits enum members with const string values as string-enum style instead of reverse-mapping, influenced by annotations.*

 * created by **magic-akari**
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63275#issuecomment-4099773091) **RyanCavanaugh** explained enum initializer rules and answered questions about intentionality, documentation, and compatibility
 * **RyanCavanaugh** added label `Question`
 * [today](https://github.com/microsoft/TypeScript/issues/63275#issuecomment-4107472034) **typescript-bot** said "This issue has been marked as "Question" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-bot** closed the issue

### [Issue microsoft/TypeScript#63276](https://github.com/microsoft/TypeScript/issues/63276) (Closed)

**Missing \`undefined\` for hover**

*VSCode's hover tooltip for a type with several optional properties only displays '| undefined' on the first property, omitting it on the others when exactOptionalPropertyTypes is false.*

 * created by **Withered-Flower-0422**
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63276#issuecomment-4097328396) **ace-tk** said "Can u please review the fixes i made."
 * [today](https://github.com/microsoft/TypeScript/issues/63276#issuecomment-4106954431) **AlejandroGispert** offered to look at and fix the issue if still open
 * [today](https://github.com/microsoft/TypeScript/issues/63276#issuecomment-4107444408) **Withered-Flower-0422** said "I think the fixes @ace-tk made should work."

### [Issue microsoft/TypeScript#63281](https://github.com/microsoft/TypeScript/issues/63281) (Open, `Suggestion`, `Awaiting More Feedback`)

**RegExpIndicesArray \- Named group indices can be undefined**

*TypeScript’s RegExpIndicesArray incorrectly assumes named regex group index arrays are always defined, missing errors for undefined groups.*

 * created by **TomStrepsil**

### [PR microsoft/TypeScript#63282](https://github.com/microsoft/TypeScript/pull/63282) (Closed)

**gh pr checkout 63282 \- Updates Azure Pipeline**

*Update the Azure Pipeline configuration for improved continuous integration workflows.*

 * created by **ghost**
 * (today) **unknown** closed the issue

### [PR microsoft/TypeScript#63283](https://github.com/microsoft/TypeScript/pull/63283) (Closed)

**Patch 1**

*Pull request 'Patch 1' contains just the default PR template and lacks any described changes or linked issue.*

 * created by **ghost**
 * (today) **unknown** closed the issue

### [PR microsoft/TypeScript#63284](https://github.com/microsoft/TypeScript/pull/63284) (Closed)

**Create CI workflow in self\-check\.yml**

*Implement a CI workflow in self-check.yml to run tests, coverage, linting, and additional checks*

 * created by **ghost**
 * (today) **unknown** closed the issue

### [PR microsoft/TypeScript#63285](https://github.com/microsoft/TypeScript/pull/63285) (Closed, `dependencies`, `github_actions`)

**Bump the github\-actions group with 3 updates**

*Bump three GitHub Actions dependencies: codecov/codecov-action to 5.5.3, actions/cache, and github/codeql-action.*

 * created by **dependabot[bot]**
 * (today) **dependabot[bot]** added labels `dependencies`, `github_actions`, `dependencies`, `github_actions`

### [Issue microsoft/TypeScript#63287](https://github.com/microsoft/TypeScript/issues/63287) (Closed, `Bug`, `Fixed`)

**\`rewriteRelativeImportExtensions\` does not rewrite dynamic \`import\(\)\` extensions inside classes with decorators**

*rewriteRelativeImportExtensions fails to rewrite file extensions for dynamic import calls inside class methods with decorators*

 * created by **DashwoodIce9**
 * [later](https://github.com/microsoft/TypeScript/issues/63287#issuecomment-4111534224) **RyanCavanaugh** said "Verified repro in TS6, but this is fixed in TS7"
 * (later) **RyanCavanaugh** added labels `Bug`, `Fixed`
 * (later) **RyanCavanaugh** closed the issue

