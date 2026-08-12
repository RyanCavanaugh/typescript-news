# Report for 2026-08-09 (Sunday, August 9th, 2026)

11 different users commented on 15 different issues.

## Recommended Actions

 * Response Recommended
    * @robertkirkman provided patch links and implementation details for supporting Android API level 29+ in golang in [microsoft/TypeScript-go#4734](https://github.com/microsoft/TypeScript-go/pull/4734#issuecomment-5235339709)
    * @glav-git asked what additional information would be useful in [microsoft/TypeScript-go#4831](https://github.com/microsoft/TypeScript-go/issues/4831#issuecomment-5241413467)

## Activity Summary

### [PR microsoft/TypeScript-go#4611](https://github.com/microsoft/TypeScript-go/pull/4611) (Closed)

**Add devcontainer feature lockfile**

*Pin devcontainer feature versions and digests by adding a .devcontainer/devcontainer-lock.json for dprint-asdf, github-cli, and node.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4611#issuecomment-5227783445) **MasterTLF** added a devcontainer feature lockfile to pin feature versions and digests, formatted the JSON per repo conventions, and confirmed PR feedback was addressed and tooling checks passed
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4611#issuecomment-5227789531) **MasterTLF** added a devcontainer feature lockfile to pin feature versions and digests, formatted the JSON per repo conventions, and confirmed PR feedback was addressed and tooling checks passed
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4611#issuecomment-5227806043) **MasterTLF** said "unblock merge, fix, merge new, commit, deploy"
 * [later](https://github.com/microsoft/TypeScript-go/pull/4611#issuecomment-5242535845) **RyanCavanaugh** said "Please do whatever you're doing here somewhere else; this isn't a repo for you to talk to your agent in"
 * (later) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#4734](https://github.com/microsoft/TypeScript-go/pull/4734) (Open)

**Add Android ARM64 release target**

*Add Android ARM64 release target to the build configuration*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4734#issuecomment-5147074433) **jakebailey** stated that they would only publish vsce-supported VSIXes and said they would add Android to CI
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4734#issuecomment-5151566500) **robertkirkman** explained that typescript-go’s os.Executable fails on Google Play Termux due to Android’s targetSdkVersion restrictions and suggested using the TERMUX_EXEC__PROC_SELF_EXE environment variable
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4734#issuecomment-5151664489) **robertkirkman** provided context that the error is specific to Google Play Termux and noted the binary has the correct interpreter and passes the static linking check
 * [today](https://github.com/microsoft/TypeScript-go/pull/4734#issuecomment-5235339709) **robertkirkman** described patch-based implementation by the Google Play Termux developer for supporting os.Executable on Android API level 29+, provided patch links, and suggested limiting support to API level 24–28 in CI

### [Issue microsoft/TypeScript-go#4809](https://github.com/microsoft/TypeScript-go/issues/4809) (Open, `Crash`, **jakebailey**, **Copilot**)

**LSP exits when parent process PID is not found**

*LSP’s parent-PID watchdog terminates the server when the PID can’t be found in Docker, with a CLI flag to disable it.*

 * **RyanCavanaugh** added to milestone `Post-7.0`
 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/4809#issuecomment-5181165788) **mj026** noted that vscode language servers have similar behavior with a parent process watchdog and suggested using the --clientProcessId option instead of removing it; offered to provide a PR
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/4809#issuecomment-5222278230) **jakebailey** said "How does that help your case? If you're launching in docker, how would you know the PID ahead of time if it's inside a container or something?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/4809#issuecomment-5233282616) **mj026** explained that the real parent process isn't visible in a container and demonstrated that the init process appears as PID 1

### [Issue microsoft/TypeScript-go#4831](https://github.com/microsoft/TypeScript-go/issues/4831) (Open, `Needs More Info`)

**High CPU Usage in Editor \(and Controls for LSP\)**

*Wants a built-in CPU usage limit flag for tsgo's LSP mode to prevent high CPU spikes on low-end laptops.*

 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/4831#issuecomment-5188485799) **DanielRosenwasser** said "@glav-git have you taken a profile to see what the cause is? Totally freezing your machine is extreme and unexpected."
 * **DanielRosenwasser** added label `Needs More Info`
 * **RyanCavanaugh** added to milestone `Need More Info`
 * [later](https://github.com/microsoft/TypeScript-go/issues/4831#issuecomment-5241413467) **glav-git** asked what additional information to provide and described reproduction steps of tsgo consuming all resources, provided system details and noted that project complexity contributed to the issue

### [PR microsoft/TypeScript-go#4857](https://github.com/microsoft/TypeScript-go/pull/4857) (Closed)

**Fix panic in getTypeOfNode for type\-only import clauses**

*getTypeOfNode panics on type-only import clauses without default import names due to missing symbol*

 * created by **Amey-Thakur**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4857#issuecomment-5234549633) **Amey-Thakur** said "Withdrawing for now. I will resubmit once I have the CLA in place."
 * (today) **Amey-Thakur** closed the issue

### [PR microsoft/TypeScript-go#4858](https://github.com/microsoft/TypeScript-go/pull/4858) (Open)

**Keep JSDoc on expando hosts declared as arrows or function expressions**

*Arrow function and function expression expando hosts lose their JSDoc comments in declaration files because synthesized nodes lack original source locations.*

 * created by **yogesh968**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4858#issuecomment-5236676110) **microsoft-github-policy-service[bot]** prompted the contributor to agree to the CLA by replying with the appropriate command
 * [today](https://github.com/microsoft/TypeScript-go/pull/4858#issuecomment-5236676151) **microsoft-github-policy-service[bot]** prompted the contributor to agree to the CLA by replying with the appropriate command

### [Issue microsoft/TypeScript-go#4859](https://github.com/microsoft/TypeScript-go/issues/4859) (Open, `Needs Investigation`, **andrewbranch**)

**feat\(contentmapper\): support whole\-symbol rename edit projection**

*Support safe whole-symbol rename edit projection in content mappers to map semantic replacements to authored text*

 * created by **ubugeeei**

### [Issue microsoft/TypeScript-go#4860](https://github.com/microsoft/TypeScript-go/issues/4860) (Open, `Needs Investigation`, **andrewbranch**)

**feat\(contentmapper\): emit declaration maps for mapped inputs**

*Enable generation of declaration maps for content-mapped files by composing transformed-to-authored source mappings and preserving accurate file naming and coordinates.*

 * created by **ubugeeei**

### [Issue microsoft/TypeScript-go#4861](https://github.com/microsoft/TypeScript-go/issues/4861) (Open, `Needs Investigation`, **ahejlsberg**)

**Assignment to an \`any\`\-parameterised generic rejected by tsgo, accepted by tsc 6\.0\.3**

*tsgo rejects assigning a typed ObjectSchema<FormData> to AnyObjectSchema while tsc 6.0.3 accepts it.*

 * created by **richardquaite**
 * [later](https://github.com/microsoft/TypeScript-go/issues/4861#issuecomment-5239282217) **mrazauskas** said "Could you double-check, please? Something might be mixed up here, because the reproduction steps in the OP are identical to #4862"
 * [later](https://github.com/microsoft/TypeScript-go/issues/4861#issuecomment-5239403330) **richardquaite** said "Sorry about that, Please see updated issue"

### [Issue microsoft/TypeScript-go#4862](https://github.com/microsoft/TypeScript-go/issues/4862) (Closed)

**Type parameter inferred from an Array\.prototype callback signature instead of the contextual type**

*tsgo infers Theme as an Array.prototype callback signature for merge-sx in MUI Stack's sx prop, causing type errors*

 * created by **richardquaite**
 * [later](https://github.com/microsoft/TypeScript-go/issues/4862#issuecomment-5239019150) **mrazauskas** said "Did you try passing --stableTypeOrdering flag to TS6? Reference: https://www.typescriptlang.org/docs/handbook/release-notes/typescript-6-0.html#the---stabletypeordering-flag"
 * [later](https://github.com/microsoft/TypeScript-go/issues/4862#issuecomment-5239091343) **richardquaite** said "Ah yeah, that reproduces in 6.0.3, thanks for the reply - will close this one."
 * (later) **richardquaite** closed the issue

### [Issue microsoft/TypeScript-go#4863](https://github.com/microsoft/TypeScript-go/issues/4863) (Open, `Needs Investigation`, **sandersn**)

**TS7 fails to emit types for \`@type\`\-annotated functions when they reference externally\-defined symbols**

*TypeScript 7.0.2 fails to emit declarations for JSDoc @type-annotated JS function declarations when referencing types defined in external .d.ts files.*

 * created by **bananarama92**

