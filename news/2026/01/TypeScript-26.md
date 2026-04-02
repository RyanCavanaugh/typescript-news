# Report for 2026-01-26 (Monday, January 26th, 2026)

4 different users commented on 6 different issues.

## Recommended Actions

 * Response Recommended
    * @supernovus asked why there is still no directive to ignore a specific TS80002 warning in [microsoft/TypeScript#43812](https://github.com/microsoft/TypeScript/issues/43812#issuecomment-3800868415)
    * @wjaspers provided a Playground example demonstrating the issue persists in TS 5.9.3 in [microsoft/TypeScript#52601](https://github.com/microsoft/TypeScript/issues/52601#issuecomment-3801831890)

## Activity Summary

### [Issue microsoft/TypeScript#43812](https://github.com/microsoft/TypeScript/issues/43812) (Open, `Suggestion`, `Awaiting More Feedback`)

**Unable to mark JS functions as not being constructors \(TS80002\)**

*Enable marking JS functions as non-constructors with JSDoc to avoid TS80002 misclassification and broken syntax coloring.*

 * [3.7 years ago](https://github.com/microsoft/TypeScript/issues/43812#issuecomment-1100743949) **Ginden** mentioned a way to mark functions as non-constructors with 'this: void' and noted that JSDoc integration didn't recognize it
 * [3.7 years ago](https://github.com/microsoft/TypeScript/issues/43812#issuecomment-1119003904) **boneskull** reported encountering the same behavior and provided a code workaround; suggested the @this tag may be ignored
 * [2.1 years ago](https://github.com/microsoft/TypeScript/issues/43812#issuecomment-1849024577) **nightwing** reported that functions were still shown as classes in hover tooltips despite using @type and suggested disabling the class detection heuristic when @this or @type was set
 * [today](https://github.com/microsoft/TypeScript/issues/43812#issuecomment-3800868415) **supernovus** complained that existing suggestions for suppressing TS80002 warnings no longer worked in VSCode/Codium and asked why there was still no directive to ignore specific warnings

### [Issue microsoft/TypeScript#52601](https://github.com/microsoft/TypeScript/issues/52601) (Closed, `Not a Defect`)

**Promise\.all sometimes infers incorrect types**

*Promise.all sometimes fails to unwrap async function results, causing the returned array items to be typed as Promise<Response> instead of Response.*

 * [2.9 years ago](https://github.com/microsoft/TypeScript/issues/52601#issuecomment-1416571821) **ritschwumm** described encountering a similar type mismatch error in older TypeScript versions when awaiting a function call and noted that splitting the assignment into two steps or typing the promise directly worked around it
 * [2.9 years ago](https://github.com/microsoft/TypeScript/issues/52601#issuecomment-1418209381) **JavaScriptBach** identified two Promise.all overloads in separate files that caused array types to match the tuple overload, resolved it by merging the definitions with the array overload first, and asked about TypeScript’s overload resolution across files
 * [2.9 years ago](https://github.com/microsoft/TypeScript/issues/52601#issuecomment-1421313774) **JavaScriptBach** said "@RyanCavanaugh I've attached a repro to the issue. Hope you or someone else on the team could take a look. Thanks!"
 * [today](https://github.com/microsoft/TypeScript/issues/52601#issuecomment-3801831890) **wjaspers** reported that the issue still occurred in TypeScript 5.9.3 and provided a Playground example and a related issue link

### [Issue microsoft/TypeScript#62241](https://github.com/microsoft/TypeScript/issues/62241) (Closed, `Bug`, `Domain: ES Modules`, `Fix Available`, **andrewbranch**, **Copilot**)

**Referenced project options not consulted to determine \.d\.ts format for synthetic default export eligibility**

*TypeScript allows default imports from modules without default exports under bundler resolution when synthetic default imports are disabled.*

 * (4 days ago) **andrewbranch** removed label `Fix Available`, and assigned to **Copilot**
 * **typescript-bot** added label `Fix Available`
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#63038](https://github.com/microsoft/TypeScript/pull/63038) (Closed, `For Milestone Bug`, **andrewbranch**, **Copilot**)

**Fix: Consult referenced project options for synthetic default export eligibility**

*Consult referenced projects’ module options for synthetic default export eligibility using correct ES module range and redirect lookups.*

 * [4 days ago](https://github.com/microsoft/TypeScript/pull/63038#issuecomment-3786751704) **Copilot** retained original behavior of getImpliedNodeFormatForEmit on line 3787 and added a conditional check to use getEmitModuleFormatOfFile for project reference declaration files when the implied format was undefined
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/63038#issuecomment-3786758373) **andrewbranch** said "@copilot what happens when you replace line 3787 and delete the rest of your added code? If that's wrong explain to me what's going wrong and why"
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/63038#issuecomment-3786773629) **Copilot** explained that replacing line 3787 and deleting the added code caused the "ambiguous-package" test to fail due to getCompilerOptionsForFile returning the consuming project's options for node_modules packages, leading getEmitModuleFormatOfFile to return ESNext and incorrectly trigger targetMode >= ES2015, and proposed using getRedirectFromSourceFile to distinguish project references from node_modules
 * [today](https://github.com/microsoft/TypeScript/pull/63038#issuecomment-3800690878) **andrewbranch** said "@typescript-bot test top800"
 * [today](https://github.com/microsoft/TypeScript/pull/63038#issuecomment-3800691273) **typescript-bot** reported build jobs started and provided status and result links
 * [today](https://github.com/microsoft/TypeScript/pull/63038#issuecomment-3801399435) **typescript-bot** reported that comparing TypeScript compilation results on the top 800 repos between main and the pull request merge looked good
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#63053](https://github.com/microsoft/TypeScript/pull/63053) (Closed, `For Uncommitted Bug`, `dependencies`, `github_actions`)

**Bump the github\-actions group with 2 updates**

*Upgrade GitHub Actions group by bumping actions/checkout from 6.0.1 to 6.0.2 and updating the github/codeql-action.*

 * **dependabot[bot]** added label `github_actions`
 * (yesterday) **typescript-bot** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * (today) **jakebailey** closed the issue

