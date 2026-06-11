# Report for 2026-06-08 (Monday, June 8th, 2026)

6 different users commented on 13 different issues.

## Recommended Actions

 * Response Recommended
    * @ibesuperv asked to be assigned to the issue in [microsoft/TypeScript#63092](https://github.com/microsoft/TypeScript/issues/63092#issuecomment-4655578718)
    * @typescript-automation[bot] reported failure when looking for the build artifact in [microsoft/TypeScript#63539](https://github.com/microsoft/TypeScript/pull/63539#issuecomment-4653064001)
    * @typescript-automation[bot] provided an installable tgz and instructions for testing in [microsoft/TypeScript#63539](https://github.com/microsoft/TypeScript/pull/63539#issuecomment-4653345441)

## Activity Summary

### [Issue microsoft/TypeScript#56855](https://github.com/microsoft/TypeScript/issues/56855) (Open, `Bug`, `Help Wanted`, `Domain: check: Type Inference`)

**Generic type inference failed**

*Including an unused default generic parameter in a TypeScript function with ThisType causes the 'context' type to be inferred as unknown.*

 * [2.4 years ago](https://github.com/microsoft/TypeScript/issues/56855#issuecomment-1877349984) **Andarist** said "This likely belongs to this umbrella issue: https://github.com/microsoft/TypeScript/issues/47599"
 * [2.4 years ago](https://github.com/microsoft/TypeScript/issues/56855#issuecomment-1877392927) **jfet97** explained that the if condition inside instantiateContextualType was too eager, causing unintended default type instantiations and suggested two alternative condition changes that fix the issue but produce failing baselines
 * **RyanCavanaugh** added label `Domain: Type Inference`
 * [today](https://github.com/microsoft/TypeScript/issues/56855#issuecomment-4651613385) **mkantor** stated that TypeScript 6.0 fixed the issue, linked a play example showing correct inference, and suggested that PR #62243 resolved it

### [Issue microsoft/TypeScript#62933](https://github.com/microsoft/TypeScript/issues/62933) (Open, `Bug`, `Domain: check: Type Circularity`)

**Maximum call stack size exceeded in isTypeAssignableTo when using recursive template literal types in a generic context**

*Using recursive template literal types inside a generic context causes checker.isTypeAssignableTo to exceed the maximum call stack size.*

 * [21 weeks ago](https://github.com/microsoft/TypeScript/issues/62933#issuecomment-3716440620) **RyanCavanaugh** said "Confirmed Andarist's crash repros in TS7"
 * (21 weeks ago) **RyanCavanaugh** added labels `Bug`, `Domain: check: Type Circularity`
 * [today](https://github.com/microsoft/TypeScript/issues/62933#issuecomment-4652729703) **ahejlsberg** said "No longer repros with tsgo."

### [Issue microsoft/TypeScript#62993](https://github.com/microsoft/TypeScript/issues/62993) (Open, `Bug`, `Help Wanted`, `Fix Available`, `Domain: Crashes`, **RyanCavanaugh**, **Copilot**)

**Crash: RangeError: Maximum call stack size exceeded in addTypesToUnion when using incomplete keyof type annotation on object destructuring**

*Compiler crashes with a RangeError in addTypesToUnion when destructuring an object with an incomplete keyof annotation under strict mode*

 * (20 weeks ago) **typescript-bot** added labels `Fix Available`, `Fix Available`
 * **RyanCavanaugh** added label `Domain: Crashes`
 * [today](https://github.com/microsoft/TypeScript/issues/62993#issuecomment-4652675010) **ahejlsberg** said "No longer repros with tsgo. Likely fixed by https://github.com/microsoft/typescript-go/pull/4191."

### [Issue microsoft/TypeScript#63090](https://github.com/microsoft/TypeScript/issues/63090) (Open, `Bug`, `Help Wanted`, `Domain: check: Type Circularity`)

**Crash: RangeError: Maximum call stack size exceeded during type serialization of recursive distributive mapped types**

*Recursive distributive mapped types trigger a compiler stack overflow error in TypeScript 5.7.3 and later.*

 * (16 weeks ago) **RyanCavanaugh** added label `Domain: check: Type Circularity`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/63090#issuecomment-4650612002) **iroquoispliskin2** said "Hey, if the issue is still open, would you mind I give it a shot?"
 * [today](https://github.com/microsoft/TypeScript/issues/63090#issuecomment-4652555368) **ahejlsberg** said "The issue doesn't repro with tsgo. It was likely fixed by https://github.com/microsoft/typescript-go/pull/3833."

### [Issue microsoft/TypeScript#63092](https://github.com/microsoft/TypeScript/issues/63092) (Open, `Bug`, `Help Wanted`, `Domain: check: Control Flow`)

**Crash: RangeError: Maximum call stack size exceeded in isReachableFlowNodeWorker with complex for loop headers**

*TypeScript's compiler crashes with a maximum call stack size exceeded error when analyzing reachability in complex for loop headers.*

 * (16 weeks ago) **RyanCavanaugh** added labels `Help Wanted`, `Domain: check: Control Flow`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/63092#issuecomment-4655578718) **ibesuperv** said "Yo if this issue still exists can you please assign me"

### [Issue microsoft/TypeScript#63441](https://github.com/microsoft/TypeScript/issues/63441) (Open, `Bug`, `Domain: check: Type Circularity`)

**\`symbolToNode\` stack overflow when using recursive types and functions with type parameters**

*Recursive generic functions and types cause TypeScript's symbolToNode to exceed the maximum call stack size.*

 * [5 weeks ago](https://github.com/microsoft/TypeScript/issues/63441#issuecomment-4338973674) **RyanCavanaugh** said "Repros in tsgo as well"
 * [5 weeks ago](https://github.com/microsoft/TypeScript/issues/63441#issuecomment-4339631166) **RyanCavanaugh** shared a Go stack trace from the typescript-go checker
 * **RyanCavanaugh** added label `Domain: check: Type Circularity`
 * [today](https://github.com/microsoft/TypeScript/issues/63441#issuecomment-4651671411) **ahejlsberg** said "No longer repros in tsgo. Probably was fixed by https://github.com/microsoft/typescript-go/pull/3833."

### [PR microsoft/TypeScript#63529](https://github.com/microsoft/TypeScript/pull/63529) (Closed, `For Uncommitted Bug`, `dependencies`, `github_actions`)

**Bump the github\-actions group across 1 directory with 7 updates**

*Update seven GitHub Actions in the root directory to their latest versions.*

 * (6 days ago) **dependabot[bot]** added labels `dependencies`, `github_actions`
 * **typescript-bot** added label `For Uncommitted Bug`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#63538](https://github.com/microsoft/TypeScript/pull/63538) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Switch from bot PAT to GitHub App token via Azure Key Vault**

*Configure authentication to use a GitHub App token stored in Azure Key Vault instead of a bot PAT.*

 * (3 days ago) **typescript-bot** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#63539](https://github.com/microsoft/TypeScript/pull/63539) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**ignore me, testing bot**

*A placeholder issue created to test the bot’s functionality and can be ignored.*

 * [2 days ago](https://github.com/microsoft/TypeScript/pull/63539#issuecomment-4640039030) **jakebailey** said "@typescript-bot test top100"
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/63539#issuecomment-4640039237) **typescript-automation[bot]** reported CI jobs started and displayed a status table
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/63539#issuecomment-4640250342) **typescript-automation[bot]** reported that running tsc on the top 400 repos comparing main and the pull request produced no issues
 * [today](https://github.com/microsoft/TypeScript/pull/63539#issuecomment-4653009649) **jakebailey** said "@typescript-bot pack this"
 * [today](https://github.com/microsoft/TypeScript/pull/63539#issuecomment-4653010414) **typescript-automation[bot]** posted build status update
 * [today](https://github.com/microsoft/TypeScript/pull/63539#issuecomment-4653064001) **typescript-automation[bot]** said "Hey @jakebailey, something went wrong when looking for the build artifact. (You can check the log here)."
 * [today](https://github.com/microsoft/TypeScript/pull/63539#issuecomment-4653091570) **jakebailey** said "@typescript-bot pack this"
 * [today](https://github.com/microsoft/TypeScript/pull/63539#issuecomment-4653092444) **typescript-automation[bot]** started jobs and updated the comment with build statuses
 * [today](https://github.com/microsoft/TypeScript/pull/63539#issuecomment-4653150441) **typescript-automation[bot]** packed an installable tgz and provided installation instructions
 * [today](https://github.com/microsoft/TypeScript/pull/63539#issuecomment-4653303326) **jakebailey** said "@typescript-bot pack this"
 * [today](https://github.com/microsoft/TypeScript/pull/63539#issuecomment-4653304051) **typescript-automation[bot]** reported that the 'pack this' build job started and passed with links to logs
 * [today](https://github.com/microsoft/TypeScript/pull/63539#issuecomment-4653345441) **typescript-automation[bot]** provided an installable tgz link and instructions for testing by referencing it in package.json and running npm install
 * [today](https://github.com/microsoft/TypeScript/pull/63539#issuecomment-4653929942) **jakebailey** said "@typescript-bot pack this"
 * [today](https://github.com/microsoft/TypeScript/pull/63539#issuecomment-4653930415) **typescript-automation[bot]** reported that the 'pack this' job started and provided result links
 * [today](https://github.com/microsoft/TypeScript/pull/63539#issuecomment-4653966728) **typescript-automation[bot]** provided an installable tgz with testing instructions and links to a playground and npm module
 * [today](https://github.com/microsoft/TypeScript/pull/63539#issuecomment-4654181284) **jakebailey** said "@typescript-bot pack this"
 * [today](https://github.com/microsoft/TypeScript/pull/63539#issuecomment-4654181697) **typescript-automation[bot]** posted a build status update indicating jobs had started and included status links
 * [today](https://github.com/microsoft/TypeScript/pull/63539#issuecomment-4654216462) **typescript-automation[bot]** provided an installable tgz link and instructions for testing via package.json, and shared a playground link and npm module reference

### [PR microsoft/TypeScript#63543](https://github.com/microsoft/TypeScript/pull/63543) (Closed, `For Backlog Bug`, `Voight-Kampff Anomaly`)

**Fix wildcard export target containment in auto\-imports**

*Apply containment validation to wildcard export targets in auto-imports to prevent out-of-package file enumeration*

 * **RyanCavanaugh** added label `Voight-Kampff Anomaly`
 * [yesterday](https://github.com/microsoft/TypeScript/pull/63543#issuecomment-4645878227) **scarab-systems** updated the PR to address review feedback, force-pushed an amended commit, reviewed changes, reran validation tests locally, and offered to make further adjustments
 * [today](https://github.com/microsoft/TypeScript/pull/63543#issuecomment-4650804019) **RyanCavanaugh** said "Thanks for the disclosures. Honestly, I'm not sure how to be more clear that this repo isn't accepting new dev contributions unless they meet the 6.0 critical patch bar. Any ideas?"
 * [today](https://github.com/microsoft/TypeScript/pull/63543#issuecomment-4651054128) **scarab-systems** acknowledged the clarification and stated they would close the PR to avoid noise
 * [today](https://github.com/microsoft/TypeScript/pull/63543#issuecomment-4651061267) **scarab-systems** acknowledged misunderstanding of the repo posture, said they would close the PR and only open future dev PRs if maintainers request them or they meet the 6.0 critical patch criteria, and suggested updating the PR template or policy bot to clarify review policy
 * (today) **scarab-systems** closed the issue

### [PR microsoft/TypeScript#63544](https://github.com/microsoft/TypeScript/pull/63544) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Update git identity from typescript\-bot to typescript\-automation\[bot\]**

*Update repository configuration to use “typescript-automation[bot]” instead of “typescript-bot” as the Git commit identity*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

