# Report for 2026-02-01 (Sunday, February 1st, 2026)

11 different users commented on 16 different issues.

## Recommended Actions

 * Response Recommended
    * @gggdomi provided repro steps in [microsoft/TypeScript-go#1905](https://github.com/microsoft/TypeScript-go/issues/1905#issuecomment-3834957222)
    * @abelcha asked if the tradeoff isn't worth it and a guard makes more sense in [microsoft/TypeScript-go#2623](https://github.com/microsoft/TypeScript-go/pull/2623#issuecomment-3834947424)
    * @tats-u reported a regression in JSDoc display and provided repro steps in [microsoft/TypeScript-go#2627](https://github.com/microsoft/TypeScript-go/pull/2627#issuecomment-3833435879)

## Activity Summary

### [Issue microsoft/TypeScript-go#1905](https://github.com/microsoft/TypeScript-go/issues/1905) (Open, `Crash`, **sheetalkamat**)

**panic: vfs: path is not absolute**

*The VFS implementation panics when given a URL-based path because it expects an absolute filesystem path.*

 * [8 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1905#issuecomment-3604712273) **IOLOII** shared a configuration map
 * [8 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1905#issuecomment-3604718075) **IOLOII** reported a crash when opening JavaScript or TypeScript files in a Vue project using the plugin and offered to provide repro steps later
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1905#issuecomment-3744284117) **marcomow** reported a similar issue when using Deno 2.6.4 with --unstable-tsgo and provided the resulting RPC panic stack trace
 * [later](https://github.com/microsoft/TypeScript-go/issues/1905#issuecomment-3834957222) **gggdomi** reported seeing a panic in the latest extension version when importing excellentexport from Skypack, noting the code had worked until a few days ago

### [PR microsoft/TypeScript-go#2459](https://github.com/microsoft/TypeScript-go/pull/2459) (Open)

**Port \-\-isolatedDeclarations related node builder logic, with baseline updates**

*Port node builder logic for the --isolatedDeclarations option and apply baseline updates for review.*

 * created by **weswigham**
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/2459#issuecomment-3827377748) **Zzzen** described testing the branch and noting the type emit was cleaner, reported still hitting OOM, and asked for tips on pinpointing memory usage
 * [later](https://github.com/microsoft/TypeScript-go/pull/2459#issuecomment-3835290600) **Zzzen** reported that setting GOMEMLIMIT=10GiB enabled full compilation and expressed excitement for the PR to land

### [PR microsoft/TypeScript-go#2613](https://github.com/microsoft/TypeScript-go/pull/2613) (Closed)

**Implement telemetry reporting in extension**

*Introduce telemetry reporting in the extension and language server using @vscode/extension-telemetry to capture usage and errors.*

 * created by **DanielRosenwasser**
 * (later) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#2623](https://github.com/microsoft/TypeScript-go/pull/2623) (Open)

**Fix inlay hints panic: guard against stale line map in LineAndCharacterToPosition**

*Prevent inlay hint panics by guarding against stale line map offsets in LineAndCharacterToPosition*

 * created by **abelcha**
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/2623#issuecomment-3827319301) **jakebailey** said "I don't think we should do this. If this happens, the caller is at fault and needs to be fixed. It can only be a symptom of a worse problem above."
 * [later](https://github.com/microsoft/TypeScript-go/pull/2623#issuecomment-3834947424) **abelcha** questioned whether recomputing line maps on every request was worth the performance hit and suggested using a guard instead

### [PR microsoft/TypeScript-go#2627](https://github.com/microsoft/TypeScript-go/pull/2627) (Closed)

**Multiple improvements to Quick Info**

*Enhance Quick Info to reuse first-overload JSDoc, correctly display symbol meanings, fix translation bug, and improve 'this' hover info.*

 * created by **ahejlsberg**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2627#issuecomment-3830445876) **jakebailey** said "Failure is a test flake I believe #2628 fixes"
 * (yesterday) **jakebailey** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/2627#issuecomment-3833435879) **tats-u** reported a regression where JSDoc for imported functions were not displayed and provided reproduction steps
 * [later](https://github.com/microsoft/TypeScript-go/pull/2627#issuecomment-3835934514) **ahejlsberg** said "@tats-u Yeah, there's an issue with carrying forward JSDoc through imported aliases. I'll have a fix up soon."

### [PR microsoft/TypeScript-go#2628](https://github.com/microsoft/TypeScript-go/pull/2628) (Closed)

**Fix dedupe/redirect nondeterminism**

*Ensure deterministic deduplication and redirection ordering by updating comparison logic and removing misleading stable sorts.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2630](https://github.com/microsoft/TypeScript-go/issues/2630) (Open, `Domain: Editor`, **andrewbranch**)

**Multiple Language Client instances persist after TSDK switch**

*Switching to the TypeScript native-preview SDK in VS Code leaves duplicate language client instances, showing the previous fix was incomplete.*

 * created by **rubenferreira97**
 * **rubenferreira97** added label `Domain: Editor`

### [Issue microsoft/TypeScript-go#2631](https://github.com/microsoft/TypeScript-go/issues/2631) (Closed, **DanielRosenwasser**)

**Code lenses and inlay hints only respected from \`javascript\.\` settings since \`0\.20260127\.1\`**

*After v0.20260127.1, VS Code ignores TypeScript inlay hint and code lens settings unless defined under javascript.*

 * created by **DanielRosenwasser**
 * [later](https://github.com/microsoft/TypeScript-go/issues/2631#issuecomment-3833892969) **DanielRosenwasser** identified that trimming the file extension's leading dot caused ExtensionIsTs to fail and suggested adding a server test
 * **DanielRosenwasser** assigned to **DanielRosenwasser**

### [Issue microsoft/TypeScript-go#2632](https://github.com/microsoft/TypeScript-go/issues/2632) (Open)

**\`@param\` JSDoc requires parameter names, did not in 6\.0 and prior**

*Omitting parameter names in JSDoc @param tags prevents TypeScript from reporting argument type mismatches under noImplicitAny.*

 * created by **DanielRosenwasser**

### [PR microsoft/TypeScript-go#2633](https://github.com/microsoft/TypeScript-go/pull/2633) (Closed)

**Leave extension as\-is for TS extension comparison\.**

*Preserve the original file extension during TypeScript extension comparisons and discuss server or VS Code extension tests.*

 * created by **DanielRosenwasser**

### [PR microsoft/TypeScript-go#2634](https://github.com/microsoft/TypeScript-go/pull/2634) (Open)

**Fix panic when marshaling build info with invalid UTF\-8**

*Sanitize diagnostic message arguments by replacing invalid UTF-8 sequences with the Unicode replacement character to avoid JSON marshaling panics.*

 * created by **scarf005**

### [PR microsoft/TypeScript-go#2635](https://github.com/microsoft/TypeScript-go/pull/2635) (Closed, `dependencies`, `github_actions`)

**Bump the github\-actions group across 2 directories with 2 updates**

*Bump GitHub Actions dependencies by updating codeql-action to 4.32.0 and actions/cache in the setup-go directory.*

 * created by **dependabot[bot]**
 * (later) **dependabot[bot]** added labels `dependencies`, `github_actions`, `dependencies`, `github_actions`

### [Issue microsoft/TypeScript-go#2636](https://github.com/microsoft/TypeScript-go/issues/2636) (Open, **jakebailey**, **Copilot**)

**tsgo emits a \`require\` statement when a value is imported without the \`type\` keyword but only used in type\-level positions**

*tsgo incorrectly emits a require call for value imports used only in type positions, causing unwanted side effects at runtime.*

 * created by **psm14**

### [Issue microsoft/TypeScript-go#2637](https://github.com/microsoft/TypeScript-go/issues/2637) (Open, `Domain: Editor`)

**Update import via Quick Fix breaks import formatting**

*Quick Fix import update breaks one-line named import formatting by adding an extra newline and misplacing the closing bracket.*

 * created by **erengeez**
 * **erengeez** added label `Domain: Editor`

### [Issue microsoft/TypeScript-go#2638](https://github.com/microsoft/TypeScript-go/issues/2638) (Open)

**tsgo emits class field declarations for conditionally assigned fields that tsc doesn't**

*tsgo emits explicit class field declarations for optional or conditionally initialized properties that tsc omits, causing different runtime behavior.*

 * created by **psm14**

