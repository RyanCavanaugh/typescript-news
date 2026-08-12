# Report for 2026-08-11 (Tuesday, August 11th, 2026)

16 different users commented on 27 different issues.

## Recommended Actions

 * Response Recommended
    * @NotASithLord asked to retain variadic inference for exports from unchecked JavaScript in [microsoft/TypeScript-go#4421](https://github.com/microsoft/TypeScript-go/pull/4421#issuecomment-5268690654)
    * @remcohaszing provided feedback and suggestions on error messaging and LSP diagnostic mapping in [microsoft/TypeScript-go#4712](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5257814665)
    * @robertkirkman asked whether PRs like #4734 and others progressively improved Android support and sought @sylirre’s insight on TS Go issues under proot-distro in [microsoft/TypeScript-go#4734](https://github.com/microsoft/TypeScript-go/pull/4734#issuecomment-5266678320)
    * @arthurfiorette asked if there's consideration for providing a direct Go Compiler API in [microsoft/TypeScript-go#4830](https://github.com/microsoft/TypeScript-go/issues/4830#issuecomment-5259015659)
    * @KirillTregubov asked if new APIs are planned to streamline typechecking and avoid generating build artifacts in [microsoft/TypeScript-go#4830](https://github.com/microsoft/TypeScript-go/issues/4830#issuecomment-5259733966)
    * @rubenferreira97 asked if js/ts.tsdk.path could be automatically honored in trusted workspaces and ignored otherwise in [microsoft/TypeScript-go#4869](https://github.com/microsoft/TypeScript-go/issues/4869#issuecomment-5258235995)

## Activity Summary

### [Issue microsoft/TypeScript-go#4262](https://github.com/microsoft/TypeScript-go/issues/4262) (Closed, `bug`, `Needs More Info`)

**Non\-deterministic \`TS2305 "has no exported member"\` errors across project references with \`\-\-emitDeclarationOnly\`**

*Flaky TS2305 "has no exported member" errors occur when running --emitDeclarationOnly across project references in a pnpm monorepo using tsgo.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/4262#issuecomment-5243474388) **thempatel** asked for updates on the issue and explained it blocked upgrade to the new compiler due to mac osx non-determinism and the need for hardlinks in the pnpm store
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/4262#issuecomment-5243522704) **jakebailey** said "The discussion was on #4578 but I think that is a dead end; I'll just send another change that kills the fast path I added but that turned out to not work"
 * (yesterday) **jakebailey** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/issues/4262#issuecomment-5257361352) **thempatel** said "thank you so much @jakebailey "

### [PR microsoft/TypeScript-go#4421](https://github.com/microsoft/TypeScript-go/pull/4421) (Closed)

**Add \`arguments\` inference removal to CHANGES\.md**

*Document removal of arguments type inference in CHANGES.md.*

 * created by **weswigham**
 * (6 weeks ago) **weswigham** closed the issue
 * [later](https://github.com/microsoft/TypeScript-go/pull/4421#issuecomment-5268690654) **NotASithLord** demonstrated loss of variadic inference for unchecked JavaScript exports in TS 7.0.2 and asked to retain variadic inference to avoid patching vendored source
 * [later](https://github.com/microsoft/TypeScript-go/pull/4421#issuecomment-5268719786) **jakebailey** said "Wouldn't it make more sense to write a declaration file for the code you're importing? It seems dubious to depend on how external/vendored JS code is analyzed, which has always been best-effort."

### [PR microsoft/TypeScript-go#4712](https://github.com/microsoft/TypeScript-go/pull/4712) (Open)

**Content mappers**

*Allow TypeScript to integrate external content mappers via tsconfig to transform and map unsupported file types into valid syntax.*

 * [4 days ago](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5213869402) **johnnyreilly** asked whether the custom transformers functionality would cover what transformers did in the TS API
 * [4 days ago](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5218558612) **andrewbranch** said "No, but custom transformers are still planned, mentioned in #4830. I’ll add ts-loader to the list of projects that needs it!"
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5247642853) **andrewbranch** described how third-party VS Code extensions can now contribute bundled content mappers directly, restricted to inferred projects without jsconfig/tsconfig files
 * [today](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5257814665) **remcohaszing** played around with a CLI-based MDX content mapper built from scratch, found it similar to Volar but encountered a generic jsonrpc initialization error. suggested differentiating error messages for various failure causes, proposed mapping MDX VFileMessage fields (source, ruleId, url) to LSP diagnostic properties including code and codeDescription.href, and noted that type errors in unmapped generated content are surfaced to users.

### [PR microsoft/TypeScript-go#4734](https://github.com/microsoft/TypeScript-go/pull/4734) (Open)

**Add Android ARM64 release target**

*Add Android ARM64 release target to the build configuration*

 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4734#issuecomment-5248508840) **jakebailey** said "It indeed works, when I test it on an emulator. Give it a try once it's built."
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4734#issuecomment-5248990930) **robertkirkman** tested both F-Droid and Google Play Termux and reported that while absolute-path tsc commands worked, relative-path TypeScript compilations failed with specific errors, and suspected a missing argv manipulation patch
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4734#issuecomment-5249567999) **robertkirkman** tested the latest PR version on both F-Droid Termux and Google Play Termux and confirmed it works, fixes errors, and maintains compatibility when TERMUX_EXEC__PROC_SELF_EXE is unset
 * [today](https://github.com/microsoft/TypeScript-go/pull/4734#issuecomment-5258351836) **jakebailey** expressed dissatisfaction with the PR layout but acknowledged it worked and asked if termux was the only approach or if other Android hacks would be needed
 * [today](https://github.com/microsoft/TypeScript-go/pull/4734#issuecomment-5258453089) **robertkirkman** mentioned that the only full port of Nodejs for Android is available via Termux and provided a link
 * [later](https://github.com/microsoft/TypeScript-go/pull/4734#issuecomment-5266379403) **dlecan** reminded that TS Go didn't work on Ubuntu under Proot/Termux and that raw Termux lacked support for much of the native Node ecosystem due to missing android architecture support, and explained interest in Node/TS on Android for running AI clients like Claude Code
 * [later](https://github.com/microsoft/TypeScript-go/pull/4734#issuecomment-5266678320) **robertkirkman** inquired whether PRs like #4734 and similar ones progressively improved Android architecture support for Node in Termux and noted TS Go issues under proot-distro, suggesting @sylirre might have insights
 * [later](https://github.com/microsoft/TypeScript-go/pull/4734#issuecomment-5268571846) **jakebailey** clarified that the previous remark sounded like a complaint and explained he found the termux case simpler but hadn’t tested the PR since returning from a conference

### [Issue microsoft/TypeScript-go#4830](https://github.com/microsoft/TypeScript-go/issues/4830) (Open, `Domain: API and Extensibility`)

**API feature roadmap**

*Proposed API roadmap for TypeScript 7.1 detailing TS Server plugin replacements and top-level utility API features.*

 * created by **andrewbranch**
 * **andrewbranch** added label `Domain: API and Extensibility`
 * **RyanCavanaugh** added to milestone `TypeScript 7.1`
 * [today](https://github.com/microsoft/TypeScript-go/issues/4830#issuecomment-5259015659) **arthurfiorette** asked if they had considered providing a direct Go Compiler API to enable tooling in faster languages without JS runtime cost
 * [today](https://github.com/microsoft/TypeScript-go/issues/4830#issuecomment-5259528261) **jakebailey** said "When we move repos, we should be doing that, yeah, though perhaps not instantly (we need to settle the major version situation)"
 * [today](https://github.com/microsoft/TypeScript-go/issues/4830#issuecomment-5259733966) **KirillTregubov** asked if using createSolutionBuilderHost and createSolutionBuilder will remain viable or if new APIs are planned to streamline typechecking and avoid generating build artifacts
 * [today](https://github.com/microsoft/TypeScript-go/issues/4830#issuecomment-5260083045) **andrewbranch** asked if any host methods were overridden beyond file system access and requested more details on solution builder properties and methods relied upon
 * [today](https://github.com/microsoft/TypeScript-go/issues/4830#issuecomment-5260320384) **KirillTregubov** described multiple iterations of implementing a TypeScript metric feature, including using the tsc CLI, a programmatic API with a custom ts.System, and an in-memory file system for complex monorepos

### [Issue microsoft/TypeScript-go#4837](https://github.com/microsoft/TypeScript-go/issues/4837) (Open, `Needs Investigation`, **andrewbranch**)

**\[API\] Narrow types of \`Node\` attributes when possible**

*Proposes narrowing Node attribute types in TS 7 by restoring specific typings for JSDocTypedefTag parent, typeExpression, and Node jsDoc.*

 * created by **Gerrit0**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.1`, and assigned to **andrewbranch**

### [Issue microsoft/TypeScript-go#4850](https://github.com/microsoft/TypeScript-go/issues/4850) (Open, `Needs Investigation`, **weswigham**)

**Difference in behavior of enum used as field key in emit vs non\-emit type check**

*Enum-based record keys resolve as enum types internally but emit as string literals in declaration files.*

 * created by **chriskrycho**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `Post-7.0`, and assigned to **weswigham**

### [Issue microsoft/TypeScript-go#4854](https://github.com/microsoft/TypeScript-go/issues/4854) (Closed, `enhancement`, **jakebailey**)

**macOS: allow DYLD\_INSERT\_LIBRARIES in tsgo**

*Add Hardened Runtime entitlements to tsgo’s macOS builds to allow DYLD_INSERT_LIBRARIES for dyld interposition tools.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/4854#issuecomment-5244808336) **jakebailey** explained that adhoc codesigning was required before using the signing service and asked if it could be done without a Mac runner in CI
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/4854#issuecomment-5244815769) **jakebailey** said "Aha! https://github.com/anchore/quill"
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/4854#issuecomment-5247188757) **jakebailey** confirmed that #4868 works
 * (today) **RyanCavanaugh** added label `enhancement`, set milestone to `Possible Improvement`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4859](https://github.com/microsoft/TypeScript-go/issues/4859) (Open, `Needs Investigation`, **andrewbranch**)

**feat\(contentmapper\): support whole\-symbol rename edit projection**

*Support safe whole-symbol rename edit projection in content mappers to map semantic replacements to authored text*

 * created by **ubugeeei**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `Possible Improvement`, and assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4859#issuecomment-5259117776) **andrewbranch** clarified that this feature would not be included in #4712 or TypeScript 7.1 and suggested using a custom extension for complex transforms while remaining open to feedback

### [Issue microsoft/TypeScript-go#4860](https://github.com/microsoft/TypeScript-go/issues/4860) (Open, `Needs Investigation`, **andrewbranch**)

**feat\(contentmapper\): emit declaration maps for mapped inputs**

*Enable generation of declaration maps for content-mapped files by composing transformed-to-authored source mappings and preserving accurate file naming and coordinates.*

 * created by **ubugeeei**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `Possible Improvement`, and assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4860#issuecomment-5259134928) **andrewbranch** said "This is something I want, and think shouldn’t be too difficult, but I don’t consider it a blocker for merging #4712."

### [Issue microsoft/TypeScript-go#4861](https://github.com/microsoft/TypeScript-go/issues/4861) (Open, `Needs Investigation`, **ahejlsberg**)

**Assignment to an \`any\`\-parameterised generic rejected by tsgo, accepted by tsc 6\.0\.3**

*tsgo rejects assigning a typed ObjectSchema<FormData> to AnyObjectSchema while tsc 6.0.3 accepts it.*

 * created by **richardquaite**
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/4861#issuecomment-5239282217) **mrazauskas** said "Could you double-check, please? Something might be mixed up here, because the reproduction steps in the OP are identical to #4862"
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/4861#issuecomment-5239403330) **richardquaite** said "Sorry about that, Please see updated issue"
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `Post-7.0`, and assigned to **ahejlsberg**

### [Issue microsoft/TypeScript-go#4863](https://github.com/microsoft/TypeScript-go/issues/4863) (Open, `Needs Investigation`, **sandersn**)

**TS7 fails to emit types for \`@type\`\-annotated functions when they reference externally\-defined symbols**

*TypeScript 7.0.2 fails to emit declarations for JSDoc @type-annotated JS function declarations when referencing types defined in external .d.ts files.*

 * created by **bananarama92**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `Post-7.0`, and assigned to **sandersn**

### [PR microsoft/TypeScript-go#4868](https://github.com/microsoft/TypeScript-go/pull/4868) (Closed)

**Add macOS entitlements before signing**

*Introduces a quill-based step to apply macOS entitlements before code signing*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4869](https://github.com/microsoft/TypeScript-go/issues/4869) (Open, `Domain: Editor`, **dbaeumer**)

**Allow settings\.json to configure tssdk without a prompt**

*Provide a settings.json option to automatically opt into the workspace’s tsdk and bypass the prompt.*

 * created by **eagarwal-notion**
 * **eagarwal-notion** added label `Domain: Editor`
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/4869#issuecomment-5247283849) **RyanCavanaugh** said "This has security implications (tsdk is effectively an arbitrary command), so it's necessary for the user to opt in."
 * [today](https://github.com/microsoft/TypeScript-go/issues/4869#issuecomment-5258235995) **rubenferreira97** questioned whether VS Code Workspace Trust could serve as the security boundary and suggested honoring js/ts.tsdk.path in trusted workspaces while ignoring it in untrusted ones
 * **RyanCavanaugh** assigned to **dbaeumer**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4869#issuecomment-5258266360) **RyanCavanaugh** said "@dbaeumer what do you think?"
 * [later](https://github.com/microsoft/TypeScript-go/issues/4869#issuecomment-5264844380) **dbaeumer** said "Binding it to workspace trust is fine. We do that in other situations as well (e.g. linter plug-ins, ....)"

### [Issue microsoft/TypeScript-go#4874](https://github.com/microsoft/TypeScript-go/issues/4874) (Open, `Needs Investigation`, **andrewbranch**)

**Add API to get target symbol of instantiated symbol**

*Add a Symbol.getTarget method to expose the underlying target symbol of instantiated symbols*

 * created by **mrazauskas**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.1`, and assigned to **andrewbranch**

### [Issue microsoft/TypeScript-go#4875](https://github.com/microsoft/TypeScript-go/issues/4875) (Open, `Needs Investigation`, **weswigham**)

**\`@augments\` JSDoc tag causes compilation error in generated declaration file**

*A JSDoc @augments tag mismatched with the extends clause in generated declaration files triggers ts(8023) errors under tsgo.*

 * created by **dragomirtitian**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `Post-7.0`, and assigned to **weswigham**

### [Issue microsoft/TypeScript-go#4876](https://github.com/microsoft/TypeScript-go/issues/4876) (Open)

**Impending Repo Move**

*TypeScript development will consolidate in the microsoft/TypeScript repo, briefly locking activity and migrating all issues and PRs.*

 * created by **RyanCavanaugh**
 * **RyanCavanaugh** added to milestone `TypeScript 7.1`

### [Issue microsoft/TypeScript-go#4878](https://github.com/microsoft/TypeScript-go/issues/4878) (Open, `bug`, **RyanCavanaugh**, **Copilot**)

**TS1515 is not reported when the earlier duplicate named group is inside a nested group**

*TypeScript’s regex parser fails to report TS1515 duplicate named group errors when the initial occurrence is nested inside another group.*

 * created by **dayongkr**
 * (today) **RyanCavanaugh** added label `bug`, set milestone to `Post-7.0`, and assigned to **Copilot**, **RyanCavanaugh**

### [PR microsoft/TypeScript-go#4879](https://github.com/microsoft/TypeScript-go/pull/4879) (Closed)

**Fix Darwin realpath test lint failures**

*Fix lint failures in Darwin realpath tests introduced by PR 4867.*

 * created by **andrewbranch**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4880](https://github.com/microsoft/TypeScript-go/issues/4880) (Open, `possible improvement`)

**Bad tsserverPath in the unstable/sync API client surfaces as bare "EPIPE: broken pipe, write" instead of naming the executable**

*Invalid tsserverPath in unstable/sync API client yields a generic EPIPE error instead of naming the missing executable*

 * created by **smm-h**
 * (today) **RyanCavanaugh** added label `possible improvement`, and set milestone to `Possible Improvement`

### [PR microsoft/TypeScript-go#4881](https://github.com/microsoft/TypeScript-go/pull/4881) (Open, **RyanCavanaugh**, **Copilot**)

**Fix TS1515 not reported when duplicate named group is nested inside a group**

*Ensure TS1515 is reported for duplicate named regex capture groups nested within other groups by correctly merging scopes.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4881#issuecomment-5259797450) **RyanCavanaugh** said "Paging @graphemecluster, this is above my regex paygrade"

### [PR microsoft/TypeScript-go#4882](https://github.com/microsoft/TypeScript-go/pull/4882) (Open, `dependencies`, `javascript`)

**Bump js\-yaml from 4\.2\.0 to 4\.3\.1**

*Upgrade js-yaml to 4.3.1 to patch a quadratic complexity vulnerability in !!omap and add a key limit option.*

 * created by **dependabot[bot]**
 * (today) **dependabot[bot]** added labels `dependencies`, `javascript`, `dependencies`, `javascript`

### [PR microsoft/TypeScript-go#4883](https://github.com/microsoft/TypeScript-go/pull/4883) (Open, `dependencies`, `go`)

**Bump go\.mongodb\.org/mongo\-driver from 1\.17\.6 to 1\.17\.7**

*Upgrade go.mongodb.org/mongo-driver to v1.17.7 to fix GSSAPI buffer handling and remove deprecation notices.*

 * created by **dependabot[bot]**
 * (today) **dependabot[bot]** added labels `dependencies`, `go`, `dependencies`, `go`

### [PR microsoft/TypeScript-go#4884](https://github.com/microsoft/TypeScript-go/pull/4884) (Open, `dependencies`, `go`)

**Bump github\.com/aws/aws\-sdk\-go\-v2/service/s3 from 1\.96\.2 to 1\.97\.3**

*Bump AWS SDK Go v2 service/s3 dependency from version 1.96.2 to 1.97.3*

 * created by **dependabot[bot]**
 * (today) **dependabot[bot]** added labels `dependencies`, `go`, `dependencies`, `go`

### [PR microsoft/TypeScript-go#4885](https://github.com/microsoft/TypeScript-go/pull/4885) (Open, `dependencies`, `go`)

**Bump github\.com/aws/aws\-sdk\-go\-v2/aws/protocol/eventstream from 1\.7\.5 to 1\.7\.8**

*Upgrade AWS SDK Go v2 eventstream protocol module from v1.7.5 to v1.7.8*

 * created by **dependabot[bot]**
 * (today) **dependabot[bot]** added labels `dependencies`, `go`

### [PR microsoft/TypeScript-go#4886](https://github.com/microsoft/TypeScript-go/pull/4886) (Closed)

**Do not require tslib for native private class members at ES2022 and later targets**

*Enable TypeScript to omit tslib imports for native private class members when targeting ES2022 or newer.*

 * created by **AbhinavMir**
 * (today) **AbhinavMir** closed the issue

