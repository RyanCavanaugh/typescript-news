# Report for 2025-12-14 (Sunday, December 14th, 2025)

5 different users commented on 5 different issues.

## Recommended Actions

 * Response Recommended
    * @smorimoto sent a gentle ping in [microsoft/TypeScript#60646](https://github.com/microsoft/TypeScript/pull/60646#issuecomment-3654395110)
    * @LukeAbby reported discovering the breaking change only after encountering an error and finding the PR in [microsoft/TypeScript#62567](https://github.com/microsoft/TypeScript/pull/62567#issuecomment-3652613304)

## Activity Summary

### [PR microsoft/TypeScript#60005](https://github.com/microsoft/TypeScript/pull/60005) (Open, `For Backlog Bug`)

**Add source mappings for serialized properties with available declaration**

*Enable generating source mappings for serialized properties in output files when their declarations exist*

 * [6 days ago](https://github.com/microsoft/TypeScript/pull/60005#issuecomment-3629396621) **jakebailey** said "We have declaration map tests and go to def baselining, so theoretically it should all be there."
 * [6 days ago](https://github.com/microsoft/TypeScript/pull/60005#issuecomment-3629398877) **jakebailey** said "But, I don't know what the equivalent to projectReferencesSourcemap.ts is in the Go codebase; maybe @sheetalkamat knows."
 * [6 days ago](https://github.com/microsoft/TypeScript/pull/60005#issuecomment-3629440369) **sheetalkamat** said "you should be able to add fourslash test. https://github.com/microsoft/typescript-go/blob/main/internal/fourslash/tests/statedeclarationmaps_test.go"
 * [today](https://github.com/microsoft/TypeScript/pull/60005#issuecomment-3652233315) **RahimGuerfi** said "..."

### [PR microsoft/TypeScript#60646](https://github.com/microsoft/TypeScript/pull/60646) (Open, `For Backlog Bug`)

**Add the type of Intl\.DurationFormat to the lib\.**

*Add initial type definitions for the Intl.DurationFormat API to the TypeScript standard library declarations*

 * [1 year ago](https://github.com/microsoft/TypeScript/pull/60646#issuecomment-2526381158) **jakebailey** indicated that CI was passing and directed to the CONTRIBUTING.md section for managing baselines and recommended running `npx dprint fmt` for formatting
 * [25 weeks ago](https://github.com/microsoft/TypeScript/pull/60646#issuecomment-2994276018) **Wiktor102** said "Is this PR being worked on? It seems to be pretty important, given that for almost 4 months now, this API has had the "Baseline Newly available" status."
 * [5 weeks ago](https://github.com/microsoft/TypeScript/pull/60646#issuecomment-3480333874) **Standard8** said "It looks like there's just one change remaining to complete this. Would it be possible that it could happen soon, or should someone take over (or maybe a maintainer can change the branch?)?"
 * [later](https://github.com/microsoft/TypeScript/pull/60646#issuecomment-3654395110) **smorimoto** said "Gentle ping"

### [PR microsoft/TypeScript#62567](https://github.com/microsoft/TypeScript/pull/62567) (Closed, `Breaking Change`, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**Deprecate esModuleInterop and allowSyntheticDefaultImports \(default to true\)**

*Deprecate the esModuleInterop and allowSyntheticDefaultImports compiler options by enabling them by default.*

 * [7 weeks ago](https://github.com/microsoft/TypeScript/pull/62567#issuecomment-3434581703) **andrewbranch** said "I'll fix anything that turns up on DT tomorrow"
 * [7 weeks ago](https://github.com/microsoft/TypeScript/pull/62567#issuecomment-3434602068) **typescript-bot** notified that DT test results were ready and provided links to detailed logs
 * [7 weeks ago](https://github.com/microsoft/TypeScript/pull/62567#issuecomment-3434630007) **jakebailey** said "Uh oh"
 * [today](https://github.com/microsoft/TypeScript/pull/62567#issuecomment-3652613304) **LukeAbby** said "Heads up, because there's no issue with "Breaking Change" the only way I discovered this was by having the error and finding this PR. Not sure how big of a deal that is though."

### [Issue microsoft/TypeScript#62883](https://github.com/microsoft/TypeScript/issues/62883) (Closed, `Duplicate`)

**Redesign \`\(const\) enum\` and \`namespace\` emit for better treeshaking**

*Propose redesigning TypeScript's enum and namespace code generation using pure IIFEs like esbuild for improved treeshaking.*

 * [3 days ago](https://github.com/microsoft/TypeScript/issues/62883#issuecomment-3644308777) **Septh** expressed surprise and thanked the finder, hoping to bring the seven-year-old duplicate issue back to maintainers' attention
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/62883#issuecomment-3646947172) **MartinJohns** said "Related: https://github.com/microsoft/typescript/wiki/faq#time-marches-on"
 * **RyanCavanaugh** added label `Duplicate`
 * [today](https://github.com/microsoft/TypeScript/issues/62883#issuecomment-3652556714) **typescript-bot** said "This issue has been marked as "Duplicate" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-bot** closed the issue

### [PR microsoft/TypeScript#62897](https://github.com/microsoft/TypeScript/pull/62897) (Closed, `For Uncommitted Bug`, `dependencies`, `github_actions`)

**Bump the github\-actions group with 4 updates**

*Bump four GitHub Action dependencies: upload-artifact to v6.0.0, codecov-action, actions/cache, and codeql-action.*

 * created by **dependabot[bot]**
 * (today) **dependabot[bot]** added labels `dependencies`, `github_actions`, `dependencies`, `github_actions`
 * **typescript-bot** added label `For Uncommitted Bug`

