# Report for 2026-03-23 (Monday, March 23rd, 2026)

12 different users commented on 19 different issues.

## Recommended Actions

 * Response Recommended
    * @anchmelev asked for another review in [microsoft/TypeScript-go#3084](https://github.com/microsoft/TypeScript-go/pull/3084#issuecomment-4115238828)
    * @JaskiratAnand requested maintainers' review in [microsoft/TypeScript-go#3179](https://github.com/microsoft/TypeScript-go/pull/3179#issuecomment-4118771089)
    * @AlejandroGispert offered to take on the issue in [microsoft/TypeScript-go#3181](https://github.com/microsoft/TypeScript-go/issues/3181#issuecomment-4113898845)
    * @virtulis asked for feedback on using a generated property list to define getters dynamically in [microsoft/TypeScript-go#3195](https://github.com/microsoft/TypeScript-go/pull/3195#issuecomment-4113555719)
    * @RohinBhargava provided a panic trace for a slice bounds out of range error in [microsoft/TypeScript-go#3202](https://github.com/microsoft/TypeScript-go/issues/3202#issuecomment-4112591492)
    * @RohinBhargava said they would provide repro steps as a zip in [microsoft/TypeScript-go#3204](https://github.com/microsoft/TypeScript-go/issues/3204#issuecomment-4114483981)
    * @faradaytrs reported experiencing the same error since version 0320 in [microsoft/TypeScript-go#3204](https://github.com/microsoft/TypeScript-go/issues/3204#issuecomment-4114866426)
    * @RohinBhargava provided repro steps as requested in [microsoft/TypeScript-go#3204](https://github.com/microsoft/TypeScript-go/issues/3204#issuecomment-4115293270)

## Activity Summary

### [PR microsoft/TypeScript-go#2944](https://github.com/microsoft/TypeScript-go/pull/2944) (Open)

**\[draft\] more formatting tests **

*Add draft formatting tests to validate and troubleshoot the repository’s testing pipelines.*

 * [4 days ago](https://github.com/microsoft/TypeScript-go/pull/2944#issuecomment-4093375627) **typescript-bot** said "@@iisaduan, the perf run you requested failed. You can check the log here."
 * [4 days ago](https://github.com/microsoft/TypeScript-go/pull/2944#issuecomment-4093891403) **typescript-bot** said "@iisaduan, the perf run you requested failed. You can check the log here."
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/2944#issuecomment-4100406855) **typescript-bot** said "@iisaduan, the perf run you requested failed. You can check the log here."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2944#issuecomment-4113812716) **typescript-bot** said "@iisaduan, the perf run you requested failed. You can check the log here."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2944#issuecomment-4114084080) **typescript-bot** said "@iisaduan, the perf run you requested failed. You can check the log here."

### [PR microsoft/TypeScript-go#3084](https://github.com/microsoft/TypeScript-go/pull/3084) (Open)

**Port LSP update imports on file rename support**

*Adds support to update import paths via LSP when files are renamed or moved to ensure correct relative references.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3084#issuecomment-4071505057) **anchmelev** thanked DanielRosenwasser, moved the semantic workspace/willRenameFiles coverage to the fourslash harness, trimmed direct server tests to LSP wire-up assertions, added relevant getEditsForFileRename coverage for non-relative imports, and omitted directory/tsconfig-specific variants
 * [6 days ago](https://github.com/microsoft/TypeScript-go/pull/3084#issuecomment-4076493957) **jakebailey** explained that they avoid adding unit tests for this behavior and expected existing fourslash tests to be converted, since they cannot verify the ported tests otherwise
 * [5 days ago](https://github.com/microsoft/TypeScript-go/pull/3084#issuecomment-4086273176) **anchmelev** reworked the test conversion to use the converted fourslash path, added verify.getEditsForFileRename support, switched to generated tests for rename cases, fixed a parsing/conversion issue, and confirmed tests passed locally
 * [today](https://github.com/microsoft/TypeScript-go/pull/3084#issuecomment-4115238828) **anchmelev** requested another review after addressing earlier feedback by moving coverage to the converted fourslash path and porting getEditsForFileRename cases

### [PR microsoft/TypeScript-go#3162](https://github.com/microsoft/TypeScript-go/pull/3162) (Closed)

**Organize imports comment duplication**

*OrganizeImports source action duplicated comments above export statements, resulting in repeated comment blocks.*

 * created by **johnfav03**
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/3162#issuecomment-4099037027) **bradleyayers** clarified that the problem was with exports rather than imports
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/3162#issuecomment-4099443518) **johnfav03** explained that the bug existed for imports in their initial implementation but was fixed in PR review and that they must have overlooked the export case
 * (today) **johnfav03** closed the issue

### [PR microsoft/TypeScript-go#3179](https://github.com/microsoft/TypeScript-go/pull/3179) (Open)

**Fix issue \#3014 **

*In tsgo watch mode, an empty tsconfig files array prevented the initial build and TS18002 diagnostic, causing a silent hang.*

 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/3179#issuecomment-4100894508) **JaskiratAnand** said "@microsoft-github-policy-service agree"
 * (3 days ago) **JaskiratAnand** closed the issue
 * (3 days ago) **JaskiratAnand** reopened the issue
 * [later](https://github.com/microsoft/TypeScript-go/pull/3179#issuecomment-4118771089) **JaskiratAnand** described fixing tsgo --watch hang on empty files array in tsconfig.json, added a regression test, and requested maintainers' review

### [Issue microsoft/TypeScript-go#3181](https://github.com/microsoft/TypeScript-go/issues/3181) (Closed)

**\`\| undefined\` in optional parameters/properties unexpectedly printed back in types / \.d\.ts emit**

*TypeScript unexpectedly includes `| undefined` in emitted declaration files for optional parameters and properties.*

 * created by **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3181#issuecomment-4113898845) **AlejandroGispert** said "Hi @RyanCavanaugh, if still available I would like to take on this issue."
 * [today](https://github.com/microsoft/TypeScript-go/issues/3181#issuecomment-4113962826) **AlejandroGispert** said "Never mind, I see this was already closed. Thanks!"

### [PR microsoft/TypeScript-go#3189](https://github.com/microsoft/TypeScript-go/pull/3189) (Closed)

**Remove \`AssignmentDeclarationMembers\` and \`GlobalExports\` from \`Symbol\`**

*Remove rarely used AssignmentDeclarationMembers and GlobalExports fields from Symbol to reduce memory footprint by relocating their tracking.*

 * created by **ahejlsberg**
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#3195](https://github.com/microsoft/TypeScript-go/pull/3195) (Open)

**API encode/decode fixes**

*Fixed API encoder/decoder by adding missing node properties, assigning a HeritageClause token type, and extending isTypeNode to recognize type keywords.*

 * created by **virtulis**
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/3195#issuecomment-4104786681) **virtulis** agreed with microsoft-github-policy-service
 * [today](https://github.com/microsoft/TypeScript-go/pull/3195#issuecomment-4113515688) **virtulis** agreed that encoder changes were unnecessary and only the properties getter was needed, suggested adding a flag for getNamedChild to handle non-optional properties, proposed tests for round-trip consistency, and declined to commit due to CLA restrictions
 * [today](https://github.com/microsoft/TypeScript-go/pull/3195#issuecomment-4113555719) **virtulis** suggested generating a full list of properties with the generateFactory script and using defineProperty to dynamically define getters on RemoteNode to avoid manual listings and solve the optional vs empty NodeList issue

### [Issue microsoft/TypeScript-go#3202](https://github.com/microsoft/TypeScript-go/issues/3202) (Closed, `Crash`, **andrewbranch**, **jakebailey**, **Copilot**)

**Panic in \`20260321\.1\` release**

*Updating to the 20260321.1 release triggers a nil pointer panic in tsgo type checking, unlike 20260320.1.*

 * created by **walkerdb**
 * **walkerdb** added label `Crash`
 * [today](https://github.com/microsoft/TypeScript-go/issues/3202#issuecomment-4112195424) **walkerdb** said "update: bisected recent commits at @jakebailey's suggestion, the panic first reproduces in https://github.com/microsoft/typescript-go/pull/3157 "
 * [today](https://github.com/microsoft/TypeScript-go/issues/3202#issuecomment-4112591492) **RohinBhargava** upvoted and provided a runtime slice bounds out of range panic trace in tsgo
 * **jakebailey** assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3202#issuecomment-4112660639) **jakebailey** said "A repro would he helpful (I don't think the original reporter has one but maybe @RohinBhargava does?)"
 * [today](https://github.com/microsoft/TypeScript-go/issues/3202#issuecomment-4112665765) **jakebailey** said "Oh, the above stack trace is entirely different and unrelated. Please file a new issue for that"
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3202#issuecomment-4113997735) **RohinBhargava** said "Will do, happy to hop on a call to live debug, if helpful!"
 * [later](https://github.com/microsoft/TypeScript-go/issues/3202#issuecomment-4118780990) **walkerdb** provided a minimal repro including code files and tsconfig
 * [later](https://github.com/microsoft/TypeScript-go/issues/3202#issuecomment-4119188813) **walkerdb** said "hmm actually the above is a panic, but I think it's a different panic than the one originally reported. I'll keep iterating.."
 * [later](https://github.com/microsoft/TypeScript-go/issues/3202#issuecomment-4119423916) **walkerdb** provided a repro for the original panic with code samples and noted it was fixed in PR #3203

### [PR microsoft/TypeScript-go#3203](https://github.com/microsoft/TypeScript-go/pull/3203) (Open, **jakebailey**, **Copilot**)

**Fix missing symbol equality check in getExternalModuleMember**

*Add missing symbol equality check in getExternalModuleMember to avoid nil pointer crash when merging module and variable symbols*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * [later](https://github.com/microsoft/TypeScript-go/pull/3203#issuecomment-4119360088) **andrewbranch** demonstrated that the code sample still crashed and mentioned an alternative was forthcoming

### [Issue microsoft/TypeScript-go#3204](https://github.com/microsoft/TypeScript-go/issues/3204) (Closed, `Crash`, **DanielRosenwasser**, **jakebailey**, **Copilot**)

**Panic with \`declarationMap\` in version 7\.0\.0\-dev\.20260323\.1**

*typescript-go 7.0.0-dev.20260323.1 panics with a slice bounds out of range error in scanner.SkipTriviaEx while generating declarationMap*

 * created by **RohinBhargava**
 * **RohinBhargava** added label `Crash`
 * [today](https://github.com/microsoft/TypeScript-go/issues/3204#issuecomment-4114031861) **RohinBhargava** said "prepping a repro"
 * [today](https://github.com/microsoft/TypeScript-go/issues/3204#issuecomment-4114472869) **DanielRosenwasser** said "Looking at the stack and error, I think the problem is we are probably looking at the wrong file when doing .d.ts emit and reusing nodes. I may be able to look into this."
 * **DanielRosenwasser** assigned to **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3204#issuecomment-4114483981) **RohinBhargava** said "amazing. Am trying to create a minimal repro (the issue occurs in a private codebase), will reply with a zip"
 * (today) **DanielRosenwasser** assigned to **jakebailey**, and unassigned **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3204#issuecomment-4114621338) **DanielRosenwasser** noted that @jakebailey had a separate branch with declaration emit fixes and provided a TypeScript repro demonstrating the slice bounds out-of-range crash
 * [today](https://github.com/microsoft/TypeScript-go/issues/3204#issuecomment-4114866426) **faradaytrs** said "The same error for me since version 0320"
 * [today](https://github.com/microsoft/TypeScript-go/issues/3204#issuecomment-4115293270) **RohinBhargava** provided another repro link for tsgo-repro-3202

